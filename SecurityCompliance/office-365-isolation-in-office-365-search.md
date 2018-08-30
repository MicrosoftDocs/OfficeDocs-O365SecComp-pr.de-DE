---
title: Office 365-Mandantenisolation in Office 365-Suche
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Eine Erläuterung der mandantenisolation in Office 365-Suche.'
ms.openlocfilehash: cc73f3c157ffd20b3891a6b7c58e7d0b2adf4e55
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528849"
---
# <a name="tenant-isolation-in-office-365-search"></a>Mandantenisolation in Office 365-Suche
SharePoint Online-Suche verwendet ein Mandant Trennung Modell, das die Effizienz der freigegebenen Datenstrukturen mit Schutz gegen Informationen verloren gehen, zwischen Mandanten ausgeglichen. Mit diesem Modell zu verhindern, dass wir die Suchfunktionen aus:
- Rückgabe von Abfrageergebnissen, die Dokumente aus anderen Mandanten enthalten
- Verfügbarmachen von über ausreichend Informationen in den Abfrageergebnissen angezeigt, dass ein geübt Benutzer Informationen zu anderen Mandanten ableiten konnte
- Anzeigen von Schema oder Einstellungen aus einer anderen Mandanten
- Mischen von Analytics processing zwischen Mandanten oder Speichern der Ergebnisse im falschen Mandanten
- Verwenden von Wörterbucheinträge aus einer anderen Mandanten

Für jede Art von Mandantendaten verwenden wir eine oder mehrere Schutzebenen im Code, um versehentliche Eindruck von Informationen zu verhindern. Die wichtigsten Daten hat die meisten Schutzebenen um sicherzustellen, dass Sie ein einzelner Fehler tatsächliche oder wahrgenommene Informationslecks führen nicht.

## <a name="tenant-separation-for-the-search-index"></a>Mandanten Trennung für den Suchindex
Der Suchindex wird auf dem Datenträger, auf den Servern, die indexkomponenten hosten gespeichert und die Mandanten die Indexdateien freigeben. Indizierte Dokumente einen Mandanten sind nur für Abfragen für diese Mandanten angezeigt. Drei unabhängige Mechanismen zu verhindern, dass Informationslecks:
- Mandanten-ID-Filterung
- Mandanten ID Begriff voranstellen
- ACL-Überprüfung

Alle drei Mechanismen müssten ausfallen für die Suche auf Dokumente, die dem falschen Mandanten zurückgegeben.

## <a name="tenant-id-filtering-and-tenant-id-term-prefixing"></a>Mandanten-ID-Filterung und Mandanten-ID Begriff voranstellen
Suche Präfixe jeder Begriff, der in den Volltextindex mit der Mandanten-ID indiziert ist Angenommen, wenn der Begriff "*Foo*" für einen Mandanten mit der ID "*123*" indiziert ist, der Eintrag in der Volltextindex ist "*123foo.*"

Jede Abfrage wird zum Einschließen von der Mandanten-ID unter Verwendung der sogenannten Mandanten-ID-Filterung konvertiert. Beispielsweise wird die Abfrage "*Foo*" in "<*Guid*>. konvertiert *"Foo"* UND *TenantID*: <*Guid*> ", wobei <*Guid*> den Mandanten Ausführen der Abfrage darstellt. Diese Abfrage Konvertierung in jeder Indexknoten auftritt, und Verarbeitung der Abfrage weder Inhalt kann es beeinflussen. Da jede Abfrage die Mandanten-ID hinzugefügt wird, kann nicht die Häufigkeit von einem Ausdruck in anderen Mandanten Schlüsseltokens im besten Übereinstimmung in einem Mandanten ranking abgeleitet werden.

Mandanten ID Begriff voranstellen tritt nur in den Volltextindex. Mit denen sich Suchvorgängen, z. B. "*Titel: Foo*", die eine synthetische Suchindex, in dem Begriffe vorangestellt werden nicht durch Mandanten-ID Stattdessen werden der Name des Felds mit denen sich Suchvorgänge vorangestellt. Beispielsweise wird die Abfrage "*Titel: Foo*" in konvertiert "*fields.title:foo und fields.tenantID*: <*Guid*>." Da die Häufigkeit eines Begriffs Bewertung von Treffer im Suchindex synthetische beeinflussen nicht, besteht keine Notwendigkeit zur Mandanten Trennung Begriff vorangestellt. Für eine Suche fielded wie "*Titel: Foo*" hängt Mandanten-ID-Filterung nach Abfrage Konvertierung Content Trennung Mandanten.

## <a name="document-access-control-list-checks"></a>Liste überprüft Dokument Access Steuerelement
Suche steuert den Zugriff auf Dokumente über ACLs, die im Suchindex gespeichert sind. Jedes Element wird mit einem Satz von Ausdrücken in einem speziellen ACL-Feld indiziert. Das ACL-Feld enthält einen Begriff pro Gruppen- oder Benutzernamen, die das Dokument anzeigen können. Jede Abfrage wird mit einer Liste von Access-Steuerelement (Entry, ACE) ausgedrückt, eine für jede Gruppe erweitert, zu der der authentifizierte Benutzer gehört.

Beispielsweise eine Abfrage wie "<*Guid*>. *Foo und TenantID*: <*Guid*> "wird:" <*Guid*>. *Foo und TenantID*: <*Guid*> *AND* (*DocACL:*<*ace1*> *OR DocACL*: <*ace2*> *OR DocACL*: <*ace3*> *... *)"

Da Benutzer und Gruppen-IDs und daher ACEs sind eindeutig, dadurch wird eine zusätzliche Sicherheitsebene zwischen Mandanten für Dokumente, die nur für einige Benutzer sichtbar sind. Die gleichen wird die Groß-/Kleinschreibung für die spezielle "alle Benutzer mit Ausnahme von externen Benutzern" ACE, der im Mandanten Empfängerbenutzer Zugriff gewährt. Da die Zugriffssteuerungseinträge für "Jeder" für alle Mandanten identisch sind, Mandanten Trennung für Öffentliche Dokumente richtet sich jedoch Mandanten-ID-Filterung. Verweigern Sie ACEs werden ebenfalls unterstützt. Die Abfrage anspruchserweiterung Fügt eine Klausel, die ein Dokument aus dem Ergebnis entfernt, wenn eine Übereinstimmung mit einen Deny-ZUGRIFFSSTEUERUNGSEINTRAG vorhanden ist.

Der Index ist in Exchange Online-Suche auf Postfach-ID für einzelne Benutzer Postfächer anstelle von Mandanten-ID (Abonnement-ID) wie in SharePoint Online partitioniert. Der Partitionierung Mechanismus ist identisch mit SharePoint Online, aber es gibt keine ACL filtern.

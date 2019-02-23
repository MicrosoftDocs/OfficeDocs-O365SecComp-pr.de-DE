---
title: Office 365-Mandanten Isolierung in Office 365-Suche
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine Erläuterung der Mandanten Isolierung in der Office 365-Suche.'
ms.openlocfilehash: fa9ba75f6ae5b0b89e3565ffb0e6f022ab36f81b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216865"
---
# <a name="tenant-isolation-in-office-365-search"></a>Mandantenisolation in der Office 365-Suche
Bei der SharePoint Online-Suche wird ein Mandanten Trennungsmodell verwendet, das die Effizienz freigegebener Datenstrukturen mit dem Schutz vor Datenverlust zwischen Mandanten abgleicht. Bei diesem Modell wird verhindert, dass die Suchfunktionen:
- Zurückgeben von Abfrageergebnissen, die Dokumente von anderen Mandanten enthalten
- Verfügbar machen ausreichender Informationen in Abfrageergebnissen, dass ein qualifizierter Benutzerinformationen zu anderen Mandanten ableiten kann
- Anzeigen von Schema oder Einstellungen eines anderen Mandanten
- Mischen von Analyse Verarbeitungsinformationen zwischen Mandanten oder Speichern von Ergebnissen im falschen Mandanten
- Verwenden von Wörterbucheinträgen eines anderen Mandanten

Für jeden Typ von Mandantendaten verwenden wir eine oder mehrere Schutzebenen im Code, um versehentliches Auslaufen von Informationen zu verhindern. Die kritischsten Daten verfügen über die meisten Schutzschichten, um sicherzustellen, dass ein einzelner Fehler nicht zu tatsächlichen oder vermeintlichen Informationslecks führt.

## <a name="tenant-separation-for-the-search-index"></a>MandantenTrennung für den suchIndex
Der Suchindex wird auf dem Datenträger auf den Servern gespeichert, auf denen die Indexkomponenten gehostet werden, und die Mandanten teilen die Indexdateien. Indizierte Dokumente eines Mandanten sind nur für Abfragen für diesen Mandanten sichtbar. Drei unabhängige Mechanismen verhindern Informationslecks:
- Mandanten-ID-Filterung
- Mandanten-ID-Präfix
- ACL-Prüfungen

Alle drei Mechanismen müssten fehlschlagen, damit die Suche Dokumente an den falschen Mandanten zurückgibt.

## <a name="tenant-id-filtering-and-tenant-id-term-prefixing"></a>Mandanten-ID-Filterung und Mandanten-ID-Präfix
Such Präfixe alle im Volltextindex indizierten Ausdrücke mit der Mandanten-ID. Wenn der Ausdruck "*foo*" beispielsweise für einen Mandanten mit der ID "*123*" indiziert ist, lautet der Eintrag im Volltextindex "123foo"*.*

Jede Abfrage wird in die Mandanten-ID mit dem Prozess Mandanten-ID-Filterung konvertiert. Beispielsweise wird die Abfrage "*foo*" in "<*GUID*>" konvertiert. *foo* UND *mandantEN*-ID: <*GUID*_GT_ ", wobei <*GUID*> den Mandanten darstellt, der die Abfrage ausführt. Diese Abfrage Konvertierung erfolgt innerhalb jedes Index Knotens, und weder die Abfrage-noch die Inhaltsverarbeitung kann Sie beeinflussen. Da die Mandanten-ID jeder Abfrage hinzugefügt wird, kann die Häufigkeit eines Ausdrucks in anderen Mandanten nicht abgeleitet werden, indem die Best Match-Rangfolge in einem Mandanten betrachtet wird.

Das Präfix für die Mandanten-ID wird nur im Volltextindex angezeigt. Feld Suchen, wie "*Title: foo*", wechseln zu einem synthetischen Suchindex, in dem Ausdrücke nicht der Mandanten-ID vorangestellt werden. Stattdessen wird FIELDED searchs der Feldname vorangestellt. Die Abfrage "*Title: foo*" wird beispielsweise in "Fields *. Title: foo und Fields. Mandantin*: <*GUID*>." konvertiert. Da die Häufigkeit eines Ausdrucks die Rangfolge der Treffer im synthetischen Suchindex nicht beeinflusst, besteht keine Notwendigkeit für eine mandantentrennung nach Begriffs Präfix. Für eine Feld Suche wie "*Title: foo*" hängt die Inhalts Trennung des Mandanten von der Mandanten-ID-Filterung nach der Abfrage Konvertierung ab.

## <a name="document-access-control-list-checks"></a>ÜberPrüfungen der Dokumentzugriffs Steuerungsliste
Die Suche steuert den Zugriff auf Dokumente über ACLs, die im Suchindex gespeichert sind. Jedes Element wird mit einem Satz von Begriffen in einem speziellen ACL-Feld indiziert. Das ACL-Feld enthält einen Ausdruck pro Gruppe oder Benutzer, der das Dokument anzeigen kann. Jede Abfrage wird mit einer Liste von ACE-Ausdrücken (Access Control Entry, Zugriffssteuerungseintrag) ergänzt, eine für jede Gruppe, zu der der authentifizierte Benutzer gehört.

Beispiel: eine Abfrage wie "<*GUID*>. *foo und mandantEN-* ID: <*GUID*> "wird:" <*GUID*>. *foo und Mandanten-* ID: <-*GUID*> *und* (*docACL:*<*ace1*> *oder docACL*: <*ace2*> *oder docACL*: <*ace3*> *... *)"

Da Benutzer-und Gruppen-IDs und damit auch ACEs eindeutig sind, bietet dies eine zusätzliche Sicherheitsstufe zwischen Mandanten für Dokumente, die für einige Benutzer nur sichtbar sind. Das gleiche gilt für das besondere "alle außer externen Benutzer"-ACE, die regulären Benutzern im Mandanten Zugriff gewährt. Da ACEs für "alle" jedoch für alle Mandanten identisch sind, hängt die mandantentrennung für öffentliche Dokumente von der Mandanten-ID-Filterung ab. Deny-ACEs werden ebenfalls unterstützt. Die Abfrageerweiterung fügt eine Klausel hinzu, die ein Dokument aus dem Ergebnis entfernt, wenn eine Übereinstimmung mit einem Deny-ACE vorliegt.

In der Exchange Online-Suche wird der Index für die Postfächer der einzelnen Benutzer anstelle der Mandanten-ID (Abonnement-ID), wie in SharePoint Online, partitioniert. Der Partitionierungs Mechanismus ist identisch mit SharePoint Online, aber es gibt keine ACL-Filterung.

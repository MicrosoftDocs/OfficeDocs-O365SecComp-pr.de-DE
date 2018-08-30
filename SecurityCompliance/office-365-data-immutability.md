---
title: Office 365 Daten Unveränderbarkeit
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
description: Definiert und erklärt Unveränderbarkeit Daten oder Daten, die erkannt werden müssen und kann nicht gelöscht oder geändert werden.
ms.openlocfilehash: 3a9e897734c1805e25a2e2dd5e0c5f8a3e3de3fd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529725"
---
# <a name="immutability-in-office-365"></a>Unveränderbarkeit in Office 365
Einige Organisationen, Einhaltung von Vorschriften, interne Governance Anforderungen oder Rechtsstreitigkeiten Risiko erfordern Sie die Beibehaltung von e-Mails und zugehörigen Daten in einem Formular sichtbar. Alle Daten im System müssen sichtbar sein, und keines davon gelöscht oder geändert werden. Der Industriestandard Begriff hierfür ist "Unveränderbarkeit." 

Herkömmliche Methoden des erzielen von Unveränderbarkeit haben in der Regel durch Verschieben von e-Mail-Nachrichten in einen separaten, schreibgeschützten Speicherort gearbeitet. Während dieser Systeme den Zweck der Postfachelemente für die Ermittlung beibehalten haben, beeinflussen sie häufig die Benutzeroberfläche auf erhebliche Weise durch Entfernen von Elementen aus dem üblichen täglichen Workflow beibehalten. Für IT-Experten erfordert diese Vorgehensweise zum Unveränderbarkeit der Bereitstellung und Wartung von einer separaten Infrastruktur für Server und Speicherung. Ermittlung selbst erfolgt mit Tools, die außerhalb der Mailsystem mit zugeordneten Bereitstellung und Wartungskosten.

Durch die Konfiguration von Compliance-Archivierung und permanentes Richtlinienfeatures der Archivierung in Office 365 und in Verbindung mit Diensten in Office 365-Suite, wie Exchange Online, SharePoint Online, OneDrive für Unternehmen und Skype für Unternehmen, Archivierung in Office 365 kann beibehalten und aufbewahren viele Klassen von eingehenden und ausgehenden interne Daten einschließlich:
- Eingehende und ausgehende e-Mail-Kommunikation
- Bücher und Datensätze im e-Mail-Format oder in freigegebene Dokumente online enthalten
- Besprechungsanfragen
- Faxnachrichten
- Sofortnachrichten
- Während onlinebesprechungen freigegebene Dokumente
- Voicemails

Microsoft hat darüber hinaus Add-On-Funktionen für [Archivierung von Daten](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) aus anderen Quellen durch die Integration mit Drittanbieter-Daten erfassen und Management-Lösungen entwickelt. Nachdem Daten von Dritten importiert wurde, können Sie Office 365 Compliance-Features mit den Daten, einschließlich der Aufbewahrung für eventuelle Rechtsstreitigkeiten, Compliance-eDiscovery und halten, Compliance-Suche, Compliance-Archivierung, Überwachung und Aufbewahrungsrichtlinien anwenden. Wenn ein Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird, werden angenommen, Drittanbieter-Daten beibehalten. Sie können Drittanbieter-Daten mithilfe von Compliance-eDiscovery oder Compliance-Suche suchen. Oder Sie können anwenden, Archivierung und Aufbewahrungsrichtlinien auf Drittanbieter-Daten wie für Microsoft Data. Kurz gesagt, helfen Archivierung von Drittanbieter-Daten in Office 365 Ihrer Organisation, die Einhaltung der behördlichen und behördlichen Richtlinien bleiben.

Archivierung in Office 365 bietet Sicherheit And Exchange Commission (s) Regel 17a-4-kompatible Speicher und behält permanente Dateien aller Daten in einem nicht einmal beschreibbaren, nicht löschbar Format von Compliance-Archivierung und permanentes Richtlinien gesammelten , einschließlich permanentes sperren. Insbesondere:
- Alle Datensätze, die mit den oben aufgeführten Aufbewahrungsrichtlinien gespeichert sind, werden in einem Bereich dedizierter Speicher außerhalb des Bereichs des Benutzers menschliche Stimme übertragen beibehalten. Geändert darüber hinaus nur autorisierte Benutzer können zugreifen und diese Datensätze durchsuchen, aber kann nicht oder löschen diese.
- Metadaten für jedes Element enthält einen Zeitstempel, der verwendet wird, bei der Berechnung der Dauer der Beibehaltung. Zeitstempel werden angewendet, wenn ein neues Element empfangen wird oder erstellt und anschließend geändert oder entfernt Sie aus den Metadaten.
- Archivierung in Office 365 ermöglicht Benutzern unterschiedliche Aufbewahrungsrichtlinien kombinieren und halten Sie Aktionen zum Erstellen von differenzierte Aufbewahrungsrichtlinien zum Definieren des Typ oder den Speicherort der Elemente in unveränderbarer Form beibehalten werden soll, und die Dauer der Beibehaltung der solche.
- Das Beibehaltung der Sperre Feature können Benutzer auswählen, ob sie der Richtlinie eine restriktive Richtlinie machen möchten. Eine restriktive Richtlinie verhindert, dass jeder Benutzer die Möglichkeit, zu entfernen, deaktivieren oder ändern Sie die Aufbewahrungsrichtlinie. Dies bedeutet, dass nach permanentes Sperre aktiviert ist, kann nicht deaktiviert werden und keinen Mechanismus vorhanden ist, unter welche alle Daten aus vorhandenen Verwalter, die durch die Aufbewahrung gesammelt wurden Richtlinien überschrieben werden möglicherweise geändert, gelöscht oder, während gelöscht die Permanentes Punkt. Darüber hinaus kann der festgelegten Zeitraum durch permanentes Sperre Haltestatus nicht verkürzte oder verringert werden. Es kann jedoch sein verlängert, im Fall einer gesetzliche Vorgabe Aufbewahrung der gespeicherten Daten, wie bereits erwähnt oben fort. Beibehaltung der Sperre gewährleistet, dass niemand, auch nicht Administratoren oder die mit bestimmten Steuerungszugriff möglicherweise ändern Sie die Einstellungen oder überschreiben oder Löschen von Daten, die gespeichert wurde, Archivierung in Office 365 in einer Reihe mit der Anleitung in 2003 Version s dargelegten Tastatureingabe festgelegt wird Richtlinie 17a-4.

Für Kunden besser verstehen, wie Office 365 genutzt werden können, um die behördlichen Vorschriften, insbesondere in Bezug auf die Regel 17a-4-Anforderungen erfüllen, wir haben ein [Whitepaper](https://go.microsoft.com/fwlink/?linkid=830440) , die Exchange Online-Archivierung, SharePoint Online OneDrive abdeckt veröffentlicht für Unternehmen und Skype für Unternehmen. Das Whitepaper enthält eine detaillierte Analyse der Archivierung Office 365-Features und Funktionen für jedes der Anforderungen unter Richtlinie 17a-4 s auch und regulierten Kunden veranschaulicht, wie Office 365 Archivierung zu erfüllen, diese aktivieren können Requirements.
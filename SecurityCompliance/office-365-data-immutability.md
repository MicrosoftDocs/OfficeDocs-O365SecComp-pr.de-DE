---
title: Office 365 Unveränderlichkeit von Daten
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Definiert und erläutert die Daten Unveränderlichkeit in Office 365.
ms.openlocfilehash: bc9805be446ad1d696e20a4bee6e449b311970fe
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622445"
---
# <a name="immutability-in-office-365"></a>Unveränderbarkeit in Office 365

Compliance, interne Steuerungsanforderungen oder Prozessrisiken erfordern Organisationen, e-Mails und zugehörige Daten in einem auffindbaren Format zu erhalten. Alle Daten im System müssen auffindbar sein, und nichts davon kann zerstört oder geändert werden. Der branchenübliche Ausdruck dafür ist "Unveränderlichkeit".

Herkömmliche Methoden für die Unveränderlichkeit bewirkten in der Regel, dass e-Mail-Nachrichten an einen separaten, schreibgeschützten Speicherort verschoben wurden. Während solche Systeme dem Zweck dienen, Postfachelemente für die Ermittlung zu erhalten, wirkt sich dies häufig auf die Benutzerfreundlichkeit aus, indem konservierte Elemente aus dem üblichen täglichen Workflow entfernt werden. Für IT-Experten erfordert dieser unveränderliche Ansatz die Bereitstellung und fortlaufende Wartung einer separaten Server-und Speicherinfrastruktur. Die Ermittlung wird mit Tools außerhalb des e-Mail-Systems durchgeführt und umfasst die zugehörigen Bereitstellungs-und Wartungskosten.

Durch Compliance-Archivierungs-und Aufbewahrungsrichtlinien Features der Archivierung in Office 365 und seinen Diensten können Sie viele Klassen von eingehenden, internen und ausgehenden Daten beibehalten und beibehalten. Dies umfasst Folgendes:

- Eingehende und ausgehende e-Mail-Kommunikation
- Bücher und Datensätze, die in e-Mail-Formularen oder in freigegebenen Onlinedokumenten enthalten sind
- Besprechungsanfragen
- Faxnachrichten
- Sofortnachrichten
- In Onlinebesprechungen freigegebene Dokumente
- Voicemails

Darüber hinaus hat Microsoft Add-on-Funktionen entwickelt, um die [Archivierung von Daten](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) aus anderen Quellen durch Integration in Datenerfassung und Verwaltungslösungen von Drittanbietern zu ermöglichen. Nachdem Sie Daten von Drittanbietern importiert haben, können Sie Office 365 Kompatibilitätsfeatures auf die Daten anwenden, einschließlich:

- [Aufbewahrung für eventuelle Rechtsstreitigkeiten](create-a-litigation-hold.md)
- [Compliance-eDiscovery und-Aufbewahrung](manage-legal-investigations.md)
- [Compliance-Suche](search-for-content.md)
- [In-Situ-Archivierung](enable-archive-mailboxes.md)
- [Postfachüberwachung](enable-mailbox-auditing.md)
- [Aufbewahrungsrichtlinien](retention-policies.md)

Wenn beispielsweise ein Postfach in das Beweissicherungsverfahren gestellt wird, werden drittanbieterdaten beibehalten. Sie können drittanbieterdaten mithilfe der in-Place-eDiscovery-oder Compliance-Suche durchsuchen. Sie können auch Archivierungs-und Aufbewahrungsrichtlinien auf drittanbieterdaten anwenden, genau wie für Microsoft-Daten. Durch das Archivieren von drittanbieterdaten in Office 365 kann Ihre Organisation mit behördlichen und behördlichen Richtlinien kompatibel bleiben.

Die Archivierung in Office 365 bietet Wertpapier-und Exchange Commission (sec) Rule 17a-4-konformen Speicher. Office 365 behält permanente Dateien aller Daten bei, die in einem nicht wiederbeschreibbaren, nicht löschbaren Format mithilfe von in-Place-Aufbewahrungsrichtlinien und Erhaltungs Richtlinien erfasst werden, einschließlich der Aufbewahrungs Sperre.

Insbesondere gilt:

- Alle Datensätze, die mit den oben genannten Aufbewahrungsrichtlinien gespeichert wurden, werden in einem dedizierten Speicherbereich außerhalb des Zuständigkeitsbereichs des normalen Benutzers aufbewahrt. Nur autorisierte Benutzer können auf diese Datensätze zugreifen und diese durchsuchen, Sie können Sie jedoch nicht ändern oder löschen.
- Metadaten für jedes Element enthalten einen Zeitstempel, der bei der Berechnung der Aufbewahrungsdauer verwendet wird. Zeitstempel werden angewendet, wenn ein neues Element empfangen oder erstellt wird und nicht geändert oder aus den Metadaten entfernt werden kann.
- Durch die Archivierung in Office 365 können Benutzer verschiedene Aufbewahrungsrichtlinien kombinieren und Aktionen durchführen, um granulare Aufbewahrungsrichtlinien zu erstellen. Diese Richtlinien definieren den Typ oder den Speicherort der aufbewahrten Elemente und die Dauer der Aufbewahrung.
- Mit dem Feature für die Aufbewahrungs Sperre können Benutzer auswählen, ob die Richtlinie restriktiv sein soll. Eine restriktive Richtlinie verhindert, dass alle Benutzer die Aufbewahrungsrichtlinie entfernen, deaktivieren oder Änderungen daran vornehmen können. Dies bedeutet, dass wenn die Erhaltungs Sperre aktiviert ist, Sie nicht deaktiviert werden kann und kein Mechanismus vorhanden ist, unter dem alle von den Aufbewahrungsrichtlinien erfassten Daten von vorhandenen Depotbanken überschrieben, geändert, gelöscht oder gelöscht werden können, während die Aufbewahrungszeitraum. Außerdem darf der Aufbewahrungszeitraum, der durch die Erhaltungs Sperre festgelegt wurde, nicht verkürzt oder verringert werden. Sie kann jedoch im Fall einer gesetzlichen Anforderung zur Fortsetzung der Speicherung der gespeicherten Daten, wie oben erwähnt, verlängert werden. Durch die Aufbewahrungs Sperre wird sichergestellt, dass niemand, nicht einmal Administratoren oder Personen mit bestimmtem Steuerungszugriff, die Einstellungen ändern oder Daten, die gespeichert wurden, überschreiben oder löschen können, wodurch die Archivierung in Office 365 entsprechend den Anweisungen in der 2003-Version von SEC ausgeführt wird. Regel 17a-4.

Um zu verstehen, wie Office 365 Ihnen bei der Erfüllung gesetzlicher Verpflichtungen hilft, insbesondere im Hinblick auf Regel 17a-4-Anforderungen, lesen Sie dieses [Whitepaper](https://go.microsoft.com/fwlink/?linkid=830440) , das Exchange Online Archivierung, SharePoint Online, OneDrive für Unternehmen und Skype for Business umfasst. Das Whitepaper enthält auch eine ausführliche Analyse der Office 365 Archivierungs Features und-Funktionen für die einzelnen Anforderungen unter sec-Regel 17a-4 und zeigt den regulierten Kunden, wie die Office 365 Archivierung Ihnen die Erfüllung dieser Anforderungen ermöglichen kann. Anforderungen.
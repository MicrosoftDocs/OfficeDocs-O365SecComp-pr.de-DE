---
title: Office 365 Daten Unveränderlichkeit
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Definiert und erläutert Daten Unveränderlichkeit oder Daten, die auffindbar und nicht zerstört oder geändert werden müssen.
ms.openlocfilehash: ab7bfc3795da761eacc9e9aa7d41e69e482fc411
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090877"
---
# <a name="immutability-in-office-365"></a>Unveränderbarkeit in Office 365
Für einige Organisationen ist die Aufbewahrung von e-Mails und zugehörigen Daten in einer auffindbaren Form für die Einhaltung von Vorschriften, internen Steuerungsanforderungen oder Rechtsstreitigkeiten erforderlich. Alle Daten im System müssen auffindbar sein, und keines davon kann zerstört oder geändert werden. Die branchenübliche Bezeichnung dafür ist "Unveränderlichkeit". 

Herkömmliche Methoden zum Erreichen der Unveränderlichkeit haben in der Regel durch das Bewegen von e-Mail-Nachrichten an einen separaten, schreibgeschützten Speicherort funktioniert. Während solche Systeme dem Zweck dienen, Postfachelemente für die Erkennung beizubehalten, haben Sie häufig Auswirkungen auf die Benutzerfreundlichkeit, indem Sie aufbewahrte Elemente aus dem üblichen täglichen Workflow entfernen. Für IT-Experten erfordert dieser Ansatz für die Unveränderlichkeit die Bereitstellung und laufende Wartung einer separaten Server-und Speicherinfrastruktur. Die Ermittlung selbst wird mit Tools außerhalb des e-Mail-Systems mit zugehörigen Bereitstellungs-und Wartungskosten durchgeführt.

Durch die Konfiguration der in-Place-Aufbewahrungs-und-Richtlinienfeatures für die Archivierung in Office 365 und in Verbindung mit Diensten in der Office 365-Suite, wie Exchange Online, SharePoint Online, OneDrive for Business und Skype for Business, die Archivierung in Office 365 kann viele Klassen von eingehenden, internen und ausgehenden Daten beibehalten und beibehalten, einschließlich:
- Eingehende und ausgehende e-Mail-Kommunikation
- Im e-Mail-Formular oder in freigegebenen Onlinedokumenten enthaltene Bücher und Datensätze
- Besprechungsanfragen
- Faxe
- Sofortnachrichten
- Während Onlinebesprechungen freigegebene Dokumente
- Voicemails

Darüber hinaus hat Microsoft Add-on-Features entwickelt, um die [Archivierung von Daten](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) aus anderen Quellen durch Integration in Datenerfassungs-und Verwaltungslösungen von Drittanbietern zu ermöglichen. Nachdem drittanbieterdaten importiert wurden, können Sie die Office-365-Kompatibilitätsfeatures auf die Daten anwenden, einschließlich des Rechtsstreits, in-situ-eDiscovery und-Speicherung, Compliance-Suche, in-situ-Archivierung,-Überwachung und-AufbewahrungsRichtlinien. Wenn beispielsweise ein Postfach in den Rechtsstreit versetzt wird, werden Daten von Drittanbietern beibehalten. Sie können drittanbieterdaten mithilfe der in-Place-eDiscovery-oder Compliance-Suche durchsuchen. Sie können auch Archivierungs-und Aufbewahrungsrichtlinien auf drittanbieterdaten anwenden, genau wie für Microsoft-Daten. Kurz gesagt, die Archivierung von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien kompatibel bleibt.

Die Archivierung in Office 365 bietet die Regel 17a-4-konforme Speicherung der Securities and Exchange Commission (SEC) und behält permanente Dateien aller Daten bei, die in einem nicht-ReWriteable, nicht löschbaren Format mithilfe von in-situ-Aufbewahrungsrichtlinien und-Richtlinien erfasst werden. , einschließlich der Aufbewahrungs Sperre. Speziell
- Alle Datensätze, die mit den oben aufgeführten Aufbewahrungsrichtlinien gespeichert werden, werden in einem dedizierten Speicherbereich außerhalb des Bereichs des normalen Benutzers aufbewahrt. Darüber hinaus können nur autorisierte Benutzer auf diese Datensätze zugreifen und diese durchsuchen, jedoch nicht ändern oder löschen.
- Metadaten für jedes Element enthalten einen Zeitstempel, der bei der Berechnung der Aufbewahrungsdauer verwendet wird. Zeitstempel werden angewendet, wenn ein neues Element empfangen oder erstellt wird und nicht nachträglich geändert oder aus den Metadaten entfernt werden kann.
- Die Archivierung in Office 365 ermöglicht Benutzern das Kombinieren verschiedener Aufbewahrungsrichtlinien und das Speichern von Aktionen zum Erstellen detaillierter Aufbewahrungsrichtlinien, um den Typ oder den Speicherort der Elemente zu definieren, die in unveränderbarer Form aufbewahrt werden sollen, und die Dauer einer solchen Aufbewahrung.
- Mit dem Feature zur Aufbewahrungs Sperre können Benutzer auswählen, ob Sie die Richtlinie als restriktive Richtlinie festlegen möchten. Eine restriktive Richtlinie verbietet jedem Benutzer die Möglichkeit, die Aufbewahrungsrichtlinie zu entfernen, zu deaktivieren oder Änderungen daran vorzunehmen. Dies bedeutet, dass nach der Aktivierung der Aufbewahrungs Sperre nicht deaktiviert werden kann, und es ist kein Mechanismus vorhanden, unter dem alle Daten aus vorhandenen Verwaltern, die durch die Aufbewahrungsrichtlinien erfasst wurden, während des Vorgangs überschrieben, geändert, gelöscht oder gelöscht werden können. Aufbewahrungszeitraum. Außerdem darf der durch die Aufbewahrungs Sperre festgelegte Aufbewahrungszeitraum nicht gekürzt oder verringert werden. Sie kann jedoch verlängert werden, wenn es sich um eine gesetzliche Anforderung zur Fortsetzung der Speicherung der gespeicherten Daten handelt (siehe oben). Die Aufbewahrungs Sperre stellt sicher, dass niemand, nicht einmal Administratoren oder Personen mit bestimmtem Steuerungszugriff, die Einstellungen ändern oder überschreiben oder Löschen von gespeicherten Daten möglicherweise durchführen, sodass die Archivierung in Office 365 mit den in der 2003-Release von SEC beschriebenen Anweisungen erfolgt. Regel 17a-4.

Um Kunden besser zu verstehen, wie Office 365 zur Erfüllung ihrer gesetzlichen Verpflichtungen genutzt werden kann, insbesondere im Hinblick auf die Regel 17a-4-Anforderungen, haben wir ein [Whitepaper](https://go.microsoft.com/fwlink/?linkid=830440) veröffentlicht, das die Exchange Online-Archivierung, SharePoint Online, OneDrive für Unternehmen und Skype for Business. Das Whitepaper enthält auch eine eingehende Analyse der Office 365-Archivierungs Features und-Funktionen für jede der Anforderungen unter der SEC-Regel 17a-4 und demonstriert für regulierte Kunden, wie Sie mit der Office 365-Archivierung diese erfüllen können. Anforderungen.
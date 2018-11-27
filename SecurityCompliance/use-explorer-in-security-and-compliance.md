---
title: Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
description: Erfahren Sie mehr über Explorer (auch als Bedrohung Explorer bezeichnet) in das Wertpapier &amp; Compliance Center.
ms.openlocfilehash: c5b6273120c605cb4233f62b5c52c6a794e554eb
ms.sourcegitcommit: 0cc6083bd8cb2f7bbf18847149c6d5239f2a6403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "26699928"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center

Wenn Ihre Organisation über [Office 365 Bedrohungsanalyse](office-365-ti.md)verfügt und Sie über die erforderlichen Berechtigungen verfügen, können Sie Explorer zum Identifizieren und Analysieren von Bedrohungen verwenden. Sie können beispielsweise identifizieren und Löschen von böswilligen e-Mail, die übermittelt wurde oder finden Sie unter Schadsoftware, die von Office 365-Sicherheitsfeatures abgefangen wurde. Explorer (auch als Bedrohung Explorer bezeichnet) ist ein leistungsfähiges nahezu in Echtzeit-Bericht in das Wertpapier &amp; Compliance Center.
  
![Wechseln Sie zu Threat Management \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Mit Explorer in die Sicherheit &amp; Compliance Center, navigieren Sie zur **Bedrohung Management** \> **Explorer**.
      
## <a name="explorer-overview"></a>Übersicht über Explorer

Explorer zeigt Informationen zu verdächtige Schadsoftware in e-Mail-Dateien in Office 365, als auch Sicherheitsrisiken und andere Risiken für Ihre Organisation. Wenn Sie Explorer zum ersten Mal öffnen, zeigt die Standardansicht erkannte Schadsoftware aus antivirus für die letzten 7 Tage. Explorer kann auch anzeigen Security Features zum Schutz in Office 365, einschließlich [Sichere Links](atp-safe-links.md) und [Sichere Anlagen](atp-safe-attachments.md) und zum Anzeigen von Daten für den letzten 30 Tagen geändert werden kann.
  
![Explorer zeigt Informationen über die wichtigste Schadsoftware und Zielgruppe](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Verwenden Sie im Menü Ansicht ändern, welche Informationen angezeigt werden.
  
![Für Explorer im Menü Ansicht](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Explorer verfügt über mehrere filtern und Abfragefunktionen, die Sie in den Details der Drilldown erfolgen soll wie oben geplant, Benutzer und oberen Malware-Familien ermöglichen. Jede Art von Bericht bietet eine Vielzahl von Methoden zum Anzeigen und Erforschen von Daten.

> [!IMPORTANT]
> Verwenden Sie Platzhalterzeichen, wie ein Sternchen (*) oder ein Fragezeichen (?), mit Explorer nicht. Wenn Sie im Feld Betreff für e-Mail-Nachrichten suchen, führt Explorer übereinstimmenden und Rendite Teilergebnisse eine Platzhaltersuche ähnelt.

## <a name="email--malware"></a>E-Mail- \> Schadsoftware

In dieser Ansicht werden e-Mail-Nachrichten, die als mit Malware identifiziert.  

Anzeigen von Informationen in das Diagramm durch Malware-Familie, Absenderdomäne, Absender-IP, Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365) und Erkennung-Technologie (wie die Schadsoftware erkannt wurde).  

![Anzeigen von Daten über erkannte Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

Unterhalb des Diagramms, Anzeigen von Details zu oberen Malware-Familien geplant Top-Benutzer und weitere Details zu bestimmten Nachrichten. 

## <a name="email--phish"></a>E-Mail- \> Phishing

In dieser Ansicht werden e-Mail-Nachrichten, die als Phishing versucht identifiziert.  

Anzeigen von Informationen durch Absenderdomäne, Absender-IP und Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365). 

![Anzeigen von Daten über e-Mail, die als Phishing-Versuche](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten Nachrichten an. 

## <a name="email--user-reported"></a>E-Mail- \> Benutzer gemeldet

In dieser Ansicht werden e-Mail, dass Benutzer als Junk, keine Junk-e- oder Phishing-e-Mail-gemeldet haben.  

Anzeigen von Informationen durch Berichtstyp (des Benutzers Bestimmung, dass die e-Mail-Nachricht Junk, keine Junk-e- oder Phishing war) sowie durch Übermittlung Grund (Gründe, warum e-Mail an einer bestimmten Position, wie eine Filterrichtlinie für Spam, eine e-Mail-Fluss-Regel, eine Liste der blockierten Absender, eine Liste sicherer Absender aufgetreten ist usw.).  

![Anzeigen von Daten über e-Mail-Benutzer als Junk, keine Junk-e- oder Phishing gemeldet](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten e-Mail-Nachrichten, wie die Betreffzeile, IP-Adresse des Absenders, der Benutzer, der die Nachricht als Junk-e-, nicht Junk, oder Phishing und mehr gemeldet an. 

## <a name="email--all-mail"></a>E-Mail- \> alle e-Mail-Nachrichten

Diese Ansichten zeigt eine alle-nach-oben-Ansicht der e-Mail-Aktivität, einschließlich e-Mail identifiziert wie böswilligen Fälligkeitsdatum Phishing oder Schadsoftware, sowie alle unbeabsichtigte Mail (normaler e-Mails, spam und Massen-Mail). 

> [!NOTE]
> Wenn Sie eine Fehlermeldung erhalten, die liest **zu viele Daten anzeigen**, fügen Sie einen Filter und einschränken den Datumsbereich, die Sie anzeigen möchten. 

Anwenden eines Filters, **Absender**auswählen, wählen Sie ein Element in der Liste, und klicken Sie dann auf die Schaltfläche Aktualisieren. In unserem Beispiel haben wir die **Erkennung Technologie** als Filter (stehen mehrere Optionen zur Verfügung) verwendet. Anzeigen von Informationen von Absender Domäne des Absenders Empfänger Betreff Dateiname der Anlage Malware-Familie Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365), Erkennung-Technologie (wie die Schadsoftware erkannt wurde) und Weitere. 

![Informationen zu erkannten e-Mail nach Erkennung Technologie-Daten anzeigen](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten e-Mail-Nachrichten, wie die Betreffzeile, Empfänger, Absender, Status und usw. an. 

## <a name="content--malware"></a>Content \> Schadsoftware

In dieser Ansicht werden die Dateien, die als böswillige in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams erkannt wurden.

Anzeigen von Informationen nach Malware Familie Erkennung-Technologie (wie die Schadsoftware erkannt wurde), und die Arbeitslast (OneDrive, SharePoint oder Teams). 

![Anzeigen von Daten über erkannte Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Unterhalb des Diagramms zeigen Sie weitere Details zu bestimmten Dateien, beispielsweise Dateiname der Anlage, Arbeitslast, Dateigröße, der letzten der Datei und vieles mehr Änderung an. 
  
## <a name="new-click-to-filter-capabilities"></a>(Neu!) Klicken Sie auf Filterfunktionen

Neue ist-Explorer die Möglichkeit, per Mausklick filtern. Seit Ende Mai 2018, wenn Sie ein Element in der Legende klicken, wird, dass das Element einen Filter für den Bericht an. Nehmen wir beispielsweise an, dass wir die Malware Ansicht im Explorer angezeigt werden:
  
![Wechseln Sie zu Threat Management \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Klicken Sie dann auf **ATP Detonationsfestigkeit** in diesem Diagramm Ergebnisse in einer Ansicht wie folgt: 
  
![Explorer gefiltert, sodass nur ATO Detonationsfestigkeit Ergebnisse angezeigt.](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
In dieser Ansicht wird nun Daten für Dateien gesucht, die von [Office 365 ATP sichere Anlagen](atp-safe-attachments.md)detonated wurden. Unterhalb des Diagramms sehen wir Details zu bestimmten e-Mail-Nachrichten, die Anlagen, die vom ATP sichere Anlagen erkannt wurden.
  
![Spezifische Details zu e-Mail-Nachrichten mit erkannten Anlagen](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Ein oder mehrere Elemente auswählen, wird im Menü **Aktionen** , das bietet mehrere Optionen für die ausgewählten Elemente auswählen aktiviert. 
  
![Auswählen eines Elements aktiviert im Menü Aktionen](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
Die Möglichkeit zum Filtern in einem Klick, und navigieren Sie zu speziellen Details können Sie viel Zeit in Untersuchen von Bedrohungen speichern.
  
## <a name="how-do-i-get-explorer"></a>Wie erhalte ich Explorer?

Explorer ist in [Office 365 Bedrohungsanalyse](office-365-ti.md)enthalten. 

Sie benötigen die entsprechende Berechtigungen, wie einer Sicherheitsadministrator oder Sicherheit Leser, zum Anzeigen und Verwenden der Explorer erteilt. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Finden und Untersuchen von böswilligen e-Mail, die (Office 365 Bedrohungsanalyse) übermittelt wurde](investigate-malicious-email-that-was-delivered.md)
  
[Antispam- und Antischadsoftwareschutz in Office 365](anti-spam-and-anti-malware-protection.md)
  


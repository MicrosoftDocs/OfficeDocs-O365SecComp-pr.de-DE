---
title: Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
description: Erfahren Sie mehr über Explorer (auch als Bedrohung Explorer bezeichnet) in das Wertpapier &amp; Compliance Center.
ms.openlocfilehash: 51228101ba75eb2d51b2594db50f679ff107ed46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530031"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center

Wenn Ihre Organisation [Office 365 Bedrohungsanalyse verfügt](office-365-ti.md)und Sie über die erforderlichen [Berechtigungen im Office 365-Sicherheit und Compliance Center](permissions-in-the-security-and-compliance-center.md)verfügen, können Sie Explorer zum Identifizieren und Analysieren von Bedrohungen verwenden. Sie können beispielsweise identifizieren und Löschen von böswilligen e-Mail, die übermittelt wurde oder finden Sie unter Schadsoftware, die von Office 365-Sicherheitsfeatures abgefangen wurde. Explorer (auch als Bedrohung Explorer bezeichnet) ist ein leistungsfähiges nahezu in Echtzeit-Bericht in das Wertpapier &amp; Compliance Center.
  
![Wechseln Sie zu Threat Management \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Mit Explorer in die Sicherheit &amp; Compliance Center, navigieren Sie zur **Bedrohung Management** \> **Explorer**.
      
## <a name="explorer-overview"></a>Übersicht über Explorer

Explorer zeigt Informationen zu verdächtige Schadsoftware in e-Mail-Dateien in Office 365, als auch Sicherheitsrisiken und andere Risiken für Ihre Organisation. Wenn Sie Explorer zum ersten Mal öffnen, zeigt die Standardansicht erkannte Schadsoftware aus antivirus. Explorer kann auch Security Features zum Schutz in Office 365, einschließlich [Sichere Links](atp-safe-links.md) und [Sichere Anlagen](atp-safe-attachments.md)anzeigen.
  
![Explorer zeigt Informationen über die wichtigste Schadsoftware und Zielgruppe](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Verwenden Sie im Menü Ansicht ändern, welche Informationen angezeigt werden.
  
![Für Explorer im Menü Ansicht](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Explorer verfügt über mehrere filtern und Abfragefunktionen, die Sie in den Details der Drilldown erfolgen soll wie oben geplant, Benutzer und oberen Malware-Familien ermöglichen. Jede Art von Bericht bietet eine Vielzahl von Methoden zum Anzeigen und Durchsuchen von Daten, wie in der folgenden Tabelle beschrieben.
  
|**Auszuwählende Option**|**Zum Anzeigen dieser Daten**|
|:-----|:-----|
|**E-Mail** \> **Schadsoftware** <br/> |E-Mail-Nachrichten, die als mit Malware identifiziert.  <br/> Anzeigen von Informationen in das Diagramm durch Malware-Familie, Absenderdomäne, Absender-IP, Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365) und Erkennung-Technologie (wie die Schadsoftware erkannt wurde).  <br/> ![Anzeigen von Daten über erkannte Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)           <br/> Unterhalb des Diagramms, Anzeigen von Details zu oberen Malware-Familien geplant Top-Benutzer und weitere Details zu bestimmten Nachrichten.  <br/> |
|**E-Mail** \> **Phishing** <br/> |E-Mail-Nachrichten, die als Phishing versucht identifiziert.  <br/> Anzeigen von Informationen durch Absenderdomäne, Absender-IP und Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365).  <br/> ![Anzeigen von Daten über e-Mail, die als Phishing-Versuche](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png)           <br/> Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten Nachrichten an.  <br/> |
|**E-Mail** \> **Benutzer gemeldet** <br/> |E-Mail, die Benutzer als Junk, keine Junk-e- oder Phishing-e-Mail gemeldet haben.  <br/> Anzeigen von Informationen durch Berichtstyp (des Benutzers Bestimmung, dass die e-Mail-Nachricht Junk, keine Junk-e- oder Phishing war) sowie durch Übermittlung Grund (Gründe, warum e-Mail an einer bestimmten Position, wie eine Filterrichtlinie für Spam, eine e-Mail-Fluss-Regel, eine Liste der blockierten Absender, eine Liste sicherer Absender aufgetreten ist usw.).  <br/> ![Anzeigen von Daten über e-Mail-Benutzer als Junk, keine Junk-e- oder Phishing gemeldet](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)           <br/> Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten e-Mail-Nachrichten, wie die Betreffzeile, IP-Adresse des Absenders, der Benutzer, der die Nachricht als Junk-e-, nicht Junk, oder Phishing und mehr gemeldet an.  <br/> |
|**E-Mail** \> **Alle e-Mail-Nachrichten** <br/> |Eine Ansicht alle Skalieren der e-Mail-Aktivität, einschließlich e-Mail, die als böswillige aufgrund von Phishing oder Schadsoftware, als identifiziert nun alle unbeabsichtigte Mail (normaler e-Mails, spam und Massen-Mail).  <br/> > [!NOTE]> Wenn Sie eine Fehlermeldung erhalten, die liest **zu viele Daten anzuzeigenden**, fügen Sie einen Filter und einschränken den Datumsbereich, die Sie anzeigen möchten. Anwenden eines Filters, **Absender**auswählen, wählen Sie ein Element in der Liste, und klicken Sie dann auf die Schaltfläche Aktualisieren. In unserem Beispiel haben wir die **Erkennung Technologie** als Filter (stehen mehrere Optionen zur Verfügung) verwendet.           Anzeigen von Informationen von Absender Domäne des Absenders Empfänger Betreff Dateiname der Anlage Malware-Familie Schutzstatus (Aktionen, die von den Features zum Schutz Bedrohung und Richtlinien in Office 365), Erkennung-Technologie (wie die Schadsoftware erkannt wurde) und Weitere.<br/> ![Informationen zu erkannten e-Mail nach Erkennung Technologie-Daten anzeigen](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png)           <br/> Unterhalb des Diagramms können zeigen Sie weitere Details zu bestimmten e-Mail-Nachrichten, wie die Betreffzeile, Empfänger, Absender, Status und usw. an.  <br/> |
|**Inhalt** \> **Schadsoftware** <br/> |Dateien, die als böswillige in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, identifiziert wurden.  <br/> Anzeigen von Informationen nach Malware Familie Erkennung-Technologie (wie die Schadsoftware erkannt wurde), und die Arbeitslast (OneDrive, SharePoint oder Teams).  <br/> ![Anzeigen von Daten über erkannte Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)           <br/> Unterhalb des Diagramms zeigen Sie weitere Details zu bestimmten Dateien, beispielsweise Dateiname der Anlage, Arbeitslast, Dateigröße, der letzten der Datei und vieles mehr Änderung an.  <br/> |
  
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

Explorer ist in [Office 365 Bedrohungsanalyse](office-365-ti.md)enthalten. Benötigen Sie die entsprechenden [Berechtigungen zugewiesen werden, in der Office 365-Sicherheit und Compliance Center](permissions-in-the-security-and-compliance-center.md), wie Sicherheitsadministrator oder Sicherheit Leser, anzeigen und Verwenden von Explorer.
  
## <a name="related-topics"></a>Verwandte Themen

[Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Finden und Untersuchen von böswilligen e-Mail, die (Office 365 Bedrohungsanalyse) übermittelt wurde](investigate-malicious-email-that-was-delivered.md)
  
[Antispam- und Antischadsoftwareschutz in Office 365](anti-spam-and-anti-malware-protection.md)
  


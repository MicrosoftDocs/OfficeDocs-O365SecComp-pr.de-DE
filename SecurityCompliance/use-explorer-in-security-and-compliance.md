---
title: Verwenden des Explorers im Security &amp; Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Informationen zu Explorer (auch als Bedrohungs-Explorer bezeichnet) &amp; im Security Compliance Center.
ms.openlocfilehash: 4a28626d0e643d7a7b96a34656e7678c71a86c66
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241967"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Verwenden des Explorers im Security &amp; Compliance Center

Wenn Ihre Organisation über [Office 365 Threat Intelligence](office-365-ti.md)verfügt und Sie über die erforderlichen Berechtigungen verfügen, können Sie mithilfe von Explorer Bedrohungen erkennen und analysieren. Sie können beispielsweise infizierte e-Mails identifizieren und löschen, die übermittelt wurden, oder Malware, die von den Office 365-Sicherheitsfeatures abgefangen wurde. Explorer (auch als Bedrohungs-Explorer bezeichnet) ist ein leistungsfähiger Near Real-Time- &amp; Bericht im Security Compliance Center.
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Um Explorer zu verwenden, wechseln Sie &amp; im Security Compliance Center zu **Threat Management** \> **Explorer**.

> [!IMPORTANT]
> Beginnend im Februar 2019 und über die nächsten Monate hinaus wird Office 365 Threat Intelligence zu Office 365 Advanced Threat Protection Plan 2 mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Übersicht über den Explorer

Der Explorer zeigt Informationen zu mutmaßlicher Schadsoftware in e-Mails und Dateien in Office 365 sowie andere Sicherheitsbedrohungen und-Risiken für Ihre Organisation an. Wenn Sie den Explorer zum ersten Mal öffnen, zeigt die Standardansicht Malware-Entdeckungen von Antivirensoftware für die letzten 7 Tage. Der Explorer kann auch Sicherheitsschutz Features in Office 365, einschließlich [sicherer Links](atp-safe-links.md) und [sicherer Anlagen](atp-safe-attachments.md) , anzeigen und so geändert werden, dass Daten für die letzten 30 Tage angezeigt werden.
  
![Explorer zeigt Informationen zu Top-Schadsoftware und zu den Ziel Benutzern](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Verwenden Sie das Menü Ansicht, um zu ändern, welche Informationen angezeigt werden.
  
![Das Menü "Ansicht" für Explorer](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Der Explorer verfügt über mehrere Filter-und Abfragefunktionen, mit denen Sie Details wie die wichtigsten Zielbenutzer, die wichtigsten Schadsoftware-Familien und vieles mehr eingehen können. Jede Art von Bericht bietet eine Vielzahl von Möglichkeiten zum Anzeigen und Durchsuchen von Daten.

> [!IMPORTANT]
> Verwenden Sie keine Platzhalterzeichen wie ein Sternchen (*) oder ein Fragezeichen (?) mit Explorer. Wenn Sie im Feld Betreff für e-Mail-Nachrichten suchen, führt der Explorer eine partielle Übereinstimmung aus und liefert Ergebnisse, die der Platzhaltersuche ähneln.

## <a name="email--malware"></a>E \> -Mail-Schadsoftware

In dieser Ansicht werden e-Mail-Nachrichten mit Schadsoftware angezeigt.  

Anzeigen von Informationen im Diagramm anhand der Schadsoftware-Familie, der Absenderdomäne, der Absender-IP-Adresse, des Schutzstatus (Aktionen, die von ihren Threat Protection-Features und-Richtlinien in Office 365 ausgeführt wurden) und der Erkennungstechnologie (wie die Schadsoftware erkannt wurde).  

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

Sehen Sie sich unter dem Diagrammdetails zu den häufigsten Schadsoftware-Familien, die wichtigsten Zielbenutzer und weitere Details zu bestimmten Nachrichten an. 

## <a name="email--phish"></a>E \> -Mail-Phishing

Diese Ansicht zeigt e-Mail-Nachrichten an, die als Phishing-Versuche identifiziert wurden.  

Anzeigen von Informationen nach Absenderdomäne, Absender-IP und Schutzstatus (Aktionen, die von ihren Funktionen zum Schutz vor Bedrohungen in Office 365 ausgeführt werden). 

![Anzeigen von Daten über e-Mails, die als Phishing-Versuche identifiziert wurden](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten an. 

## <a name="email--user-reported"></a>E \> -Mail-Benutzer gemeldet

In dieser Ansicht werden e-Mails angezeigt, die von Benutzern als Junk-e-Mail oder Phishing-Nachricht gemeldet wurden.  

Informationen nach Berichtstyp anzeigen (die Bestimmung des Benutzers, dass es sich bei der e-Mail um Junk-e-Mail, nicht um Junk oder Phishing handelt) und nach Zustellungs Grund (Gründe dafür, warum e-Mails an einen bestimmten Speicherort gesendet wurden, beispielsweise eine Spamfilter Richtlinie, eine Nachrichtenfluss Regel, eine Liste blockierter Absender, eine Liste sicherer Absender, usw.).  

![Anzeigen von Daten über e-Mail-Benutzer, die als Junk, nicht als Junk oder Phishing gemeldet wurden](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

Zeigen Sie unterhalb des Diagramms weitere Details zu bestimmten e-Mail-Nachrichten wie Betreff, die IP-Adresse des Absenders, der Benutzer, der die Nachricht als Junk, nicht Junk oder Phishing gemeldet hat, und vieles mehr an. 

## <a name="email--all-mail"></a>Alle \> e-Mails senden

Diese Ansichten zeigen eine Übersicht über e-Mail-Aktivitäten, einschließlich e-Mails, die aufgrund von Phishing oder Schadsoftware als böswillig identifiziert wurden, sowie für alle nicht-böswilligen e-Mails (normale e-Mail, Spam und Massensendungen). 

> [!NOTE]
> Wenn Sie eine Fehlermeldung erhalten, die zu **viele anzuzeigende Daten**liest, fügen Sie einen Filter hinzu, und schränken Sie gegebenenfalls den angezeigten Datums Umfang ein. 

Wenn Sie einen Filter anwenden möchten, wählen Sie **Absender**aus, wählen Sie ein Element in der Liste aus, und klicken Sie dann auf die Schaltfläche Aktualisieren. In unserem Beispiel wurde die **Erkennungstechnologie** als Filter verwendet (es stehen mehrere Optionen zur Verfügung). Anzeigen von Informationen nach Absender, Absenderdomäne, Empfänger, Betreff, Anlage Dateiname, Schadsoftware-Familie, Schutzstatus (Aktionen, die von ihren Threat Protection-Features und-Richtlinien in Office 365 ausgeführt werden), Erkennungstechnologie (wie die Schadsoftware erkannt wurde) und mehr. 

![Anzeigen von Daten zu erkannten e-Mails anhand der Erkennungstechnologie](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten e-Mail-Nachrichten an, beispielsweise Betreff, Empfänger, Absender, Status usw. 

## <a name="content--malware"></a>Inhalts \> -Schadsoftware

Diese Ansicht zeigt Dateien, die in SharePoint Online, OneDrive for Business und Microsoft Teams als schädlich identifiziert wurden.

Anzeigen von Informationen nach Malwarefamilie, Erkennungstechnologie (wie die Malware erkannt wurde) und Arbeitslast (OneDrive, SharePoint oder Teams). 

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Dateien an, beispielsweise Dateiname der Anlage, Arbeitsauslastung, Dateigröße, wer die Datei zuletzt geändert hat, und vieles mehr. 
  
## <a name="new-click-to-filter-capabilities"></a>(Neu!) Click-to-Filter-Funktionen

Neu in Explorer ist die Möglichkeit zum Filtern. Ab Ende Mai 2018 wird das Element, wenn Sie auf ein Element in der Legende klicken, zu einem Filter für den Bericht. Nehmen wir beispielsweise an, dass Sie die Malware Ansicht im Explorer betrachten:
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Wenn Sie in diesem Diagramm auf **ATP-Detonation** klicken, wird eine Ansicht wie die folgende angezeigt: 
  
![Explorer gefiltert, um nur die Ergebnisse der ATO-Detonation anzuzeigen](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
In dieser Ansicht betrachten wir nun Daten für Dateien, die von [Office 365 ATP Safe Attachments](atp-safe-attachments.md)gezündet wurden. Unter dem Diagramm können Details zu bestimmten e-Mail-Nachrichten mit Anlagen angezeigt werden, die von sicheren ATP-Anlagen erkannt wurden.
  
![Spezifische Details zu e-Mail-Nachrichten mit erkannten Anlagen](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Durch Auswählen eines oder mehrerer Elemente wird das Menü " **Aktionen** " aktiviert, das verschiedene Auswahlmöglichkeiten für die ausgewählten Elemente bietet. 
  
![Durch Auswählen eines Elements wird das Menü "Aktionen" aktiviert.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
Die Möglichkeit, mit einem Klick zu filtern und zu bestimmten Details zu navigieren, kann Ihnen viel Zeit bei der Untersuchung von Bedrohungen ersparen.
  
## <a name="how-do-i-get-explorer"></a>Wie erhalte ich einen Explorer?

Explorer ist in der [Office 365 Threat Intelligence](office-365-ti.md)enthalten. 

Sie müssen über die entsprechenden Berechtigungen verfügen, beispielsweise solche, die einem Sicherheitsadministrator oder einem Sicherheits Leser erteilt wurden, um den Explorer anzuzeigen und zu verwenden. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Suchen und untersuchen von gelieferten Schad-e-Mails (Office 365 Threat Intelligence)](investigate-malicious-email-that-was-delivered.md)
  
[Antispam- und Antischadsoftwareschutz in Office 365](anti-spam-and-anti-malware-protection.md)
  


---
title: Ansichten des Sicherheitsrisiken-Explorers
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: Erfahren Sie mehr über die verschiedenen Arten von Ansichten im Explorer (auch als Bedrohungs-Explorer bezeichnet) als Teil von Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: bcfa044db6844d9459b3dd62d9ced1cd37a999ec
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260553"
---
# <a name="threat-explorer-views"></a>Ansichten des Sicherheitsrisiken-Explorers

[Threat Explorer](use-explorer-in-security-and-compliance.md) ist ein leistungsstarkes, nahezu Echtzeit-Tool, mit dessen Hilfe Sicherheitsteams untersuchen und auf Bedrohungen im Security &amp; Compliance Center reagieren können. Der Explorer zeigt Informationen zu mutmaßlicher Schadsoftware und Phishing in e-Mails und Dateien in Office 365 sowie andere Sicherheitsbedrohungen und-Risiken für Ihre Organisation an. 

Wenn Sie Explorer zuerst öffnen, werden in der Standardansicht e-Mail-Malware-Entdeckungen für die letzten 7 Tage angezeigt. 

![Sicherheitsrisiken-Explorer](media/ThreatExplorerFirstOpened.png)

Der Explorer kann auch Sicherheitsschutz Features in Office 365, einschließlich [sicherer Links](atp-safe-links.md) und [sicherer Anlagen](atp-safe-attachments.md) , anzeigen und so geändert werden, dass Daten für die letzten 30 Tage angezeigt werden. 

> [!NOTE]
> Wenn Sie ein Testabonnement für Office 365 Advanced Threat Protection Plan 2 oder Office 365 E5 haben, werden nur Erkennungs-und e-Mail-Daten für die letzten 7 Tage angezeigt.
  
Verwenden Sie das Menü **Ansicht** , um zu ändern, welche Informationen angezeigt werden. Mit QuickInfos können Sie bestimmen, welche Ansicht verwendet werden soll.
  
![Ansicht im Menü "Bedrohungs-Explorer"](media/ThreatExplorerViewMenu.png)

Nachdem Sie eine Ansicht ausgewählt haben, können Sie Filter anwenden und Abfragen einrichten, um eine weitere Analyse durchzuführen. Die folgenden Abschnitte enthalten eine kurze Übersicht über die verschiedenen im Explorer verfügbaren Ansichten.  

## <a name="email--malware"></a>E-Mail-> Schadsoftware

Um diesen Bericht anzuzeigen, wählen Sie im Explorer die Option**e-Mail-** > **Schadsoftware** **anzeigen** > aus. In dieser Ansicht werden Informationen zu e-Mail-Nachrichten angezeigt, die als Schadsoftware identifiziert wurden.  

![Anzeigen von Daten zu als Schadsoftware identifizierten e-Mails](media/ExplorerEmailMalwareMenu.png) 

Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen. Verwenden Sie diese Liste, um Daten nach Absender, Empfänger, Absenderdomäne, Betreff, Erkennungstechnologie, Schutzstatus und mehr anzuzeigen. 

Wenn Sie beispielsweise sehen möchten, welche Aktionen für erkannte e-Mail-Nachrichten durchgeführt wurden, wählen Sie in der Liste **Schutzstatus** aus. Wählen Sie eine Option aus, und klicken Sie dann auf die Schaltfläche Aktualisieren, um den Filter auf Ihren Bericht anzuwenden.

![Optionen für den Status von BedrohungsSchutz für Threat Explorer](media/ThreatExplorerProtectionStatusOptions.png)

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten an. Wenn Sie ein Element in der Liste auswählen, wird ein Ausklappbereich geöffnet, in dem Sie mehr über das ausgewählte Element erfahren. 

![Bedrohungs-Explorer mit geöffnetem Flyout](media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a>E-Mail->-Phishing

Um diesen Bericht anzuzeigen, wählen Sie im Explorer die Option**e-Mail-** > **Phishing** **anzeigen** > aus. Diese Ansicht zeigt e-Mail-Nachrichten an, die als Phishing-Versuche identifiziert wurden.  

![Anzeigen von Daten über e-Mails, die als Phishing-Versuche identifiziert wurden](media/ThreatExplorerEmailPhish.png) 

Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen. Verwenden Sie diese Liste, um Daten nach Absender, Empfänger, Absenderdomäne, Absender-IP, URL-Domäne, klicken Sie auf Urteil und vieles mehr. 

Wenn Sie beispielsweise sehen möchten, welche Aktionen ausgeführt wurden, als Personen auf URLs geklickt haben, die als Phishing-Versuche identifiziert wurden, wählen Sie in der Liste **auf Urteil klicken** aus, wählen Sie eine oder mehrere Optionen aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.

![Klicken Sie auf Urteils Optionen für den Phishingbericht](media/ThreatExplorerEmailPhishClickVerdictOptions.png)

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten, URL-Klicks, URLs und e-Mail-Ursprung an. 

![Als Phishing erkannte URLs in e-Mail-Nachrichten](media/ThreatExplorerEmailPhishURLs.png)

Wenn Sie ein Element in der Liste auswählen, beispielsweise eine erkannte URL, wird ein Fensterausschnitt geöffnet, in dem Sie mehr über das ausgewählte Element erfahren. 

![Details zu einer festgestellten URL](media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--user-reported"></a>E-Mail-> vom Benutzer gemeldet

Um diesen Bericht anzuzeigen, wählen Sie im Explorer die Option**e-Mail** > **-Benutzer** **anzeigen** > . In dieser Ansicht werden e-Mails angezeigt, die von Benutzern als Junk-e-Mail oder Phishing-Nachricht gemeldet wurden. 

![Von Benutzern gemeldete e-Mail-Nachrichten](media/ThreatExplorerEmailUserReportedViewOptions.png) 

Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen. Verwenden Sie diese Liste, um Informationen nach Absender, Empfänger, Berichtstyp anzuzeigen (die Bestimmung des Benutzers, dass es sich um Junk-e-Mail-Nachricht, nicht um Junk oder Phishing handelt) und vieles mehr. 

Wenn Sie beispielsweise Informationen zu e-Mail-Nachrichten anzeigen möchten, die als Phishing-Versuche gemeldet wurden, klicken Sie auf **Absender** > **Berichttyp**, wählen Sie **Phishing**aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.

![Für Berichttyp Filter ausgewählter Phishingfilter](media/ThreatExplorerEmailUserReportedPhishSelected.png)

Zeigen Sie unterhalb des Diagramms weitere Details zu bestimmten e-Mail-Nachrichten wie Betreff, die IP-Adresse des Absenders, der Benutzer, der die Nachricht als Junk, nicht Junk oder Phishing gemeldet hat, und vieles mehr an. 

![Nachrichten, die als Phishing-Versuche gemeldet wurden](media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

Wählen Sie ein Element in der Liste aus, um zusätzliche Details anzuzeigen.

## <a name="email--all-email"></a>E-Mail-> alle e-Mails

Um diesen Bericht anzuzeigen, wählen Sie im Explorer die Option**** > **alle**e-Mails **anzeigen** > . Diese Ansichten zeigen eine Übersicht über e-Mail-Aktivitäten, einschließlich e-Mails, die aufgrund von Phishing oder Schadsoftware als böswillig identifiziert wurden, sowie für alle nicht-böswilligen e-Mails (normale e-Mail, Spam und Massensendungen). 

> [!NOTE]
> Wenn Sie eine Fehlermeldung erhalten, die zu **viele anzuzeigende Daten**liest, fügen Sie einen Filter hinzu, und schränken Sie gegebenenfalls den angezeigten Datums Umfang ein. 

Wenn Sie einen Filter anwenden möchten, wählen Sie **Absender**aus, wählen Sie ein Element in der Liste aus, und klicken Sie dann auf die Schaltfläche Aktualisieren. In unserem Beispiel wurde die **Erkennungstechnologie** als Filter verwendet (es stehen mehrere Optionen zur Verfügung). Anzeigen von Informationen nach Absender, Absenderdomäne, Empfänger, Betreff, Anlage Dateiname, Schadsoftware-Familie, Schutzstatus (Aktionen, die von ihren Threat Protection-Features und-Richtlinien in Office 365 ausgeführt werden), Erkennungstechnologie (wie die Schadsoftware erkannt wurde) und mehr. 

![Anzeigen von Daten zu erkannten e-Mails anhand der Erkennungstechnologie](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten e-Mail-Nachrichten an, beispielsweise Betreff, Empfänger, Absender, Status usw. 

## <a name="content--malware"></a>Inhalts > Schadsoftware

Klicken Sie zum Anzeigen dieses Berichts im Explorer auf **** > **Inhalts** > -**Malware**anzeigen. Diese Ansicht zeigt Dateien, die von [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business und Microsoft Teams](atp-for-spo-odb-and-teams.md)als bösartig identifiziert wurden.

Anzeigen von Informationen nach Malwarefamilie, Erkennungstechnologie (wie die Malware erkannt wurde) und Arbeitslast (OneDrive, SharePoint oder Teams). 

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Dateien an, beispielsweise Dateiname der Anlage, Arbeitsauslastung, Dateigröße, wer die Datei zuletzt geändert hat, und vieles mehr. 
  
## <a name="click-to-filter-capabilities"></a>Click-to-Filter-Funktionen

Mit Explorer können Sie einen Filter in einem Klick anwenden. Klicken Sie auf ein Element in der Legende, und dieses Element wird ein Filter für den Bericht. Nehmen wir beispielsweise an, dass Sie die Malware Ansicht im Explorer betrachten:
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Wenn Sie in diesem Diagramm auf **ATP-Detonation** klicken, wird eine Ansicht wie die folgende angezeigt: 
  
![Explorer gefiltert, um nur Ergebnisse der ATP-Detonation anzuzeigen](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
In dieser Ansicht betrachten wir nun Daten für Dateien, die von [Office 365 ATP Safe Attachments](atp-safe-attachments.md)gezündet wurden. Unter dem Diagramm können Details zu bestimmten e-Mail-Nachrichten mit Anlagen angezeigt werden, die von sicheren ATP-Anlagen erkannt wurden.
  
![Spezifische Details zu e-Mail-Nachrichten mit erkannten Anlagen](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Durch Auswählen eines oder mehrerer Elemente wird das Menü " **Aktionen** " aktiviert, das verschiedene Auswahlmöglichkeiten für die ausgewählten Elemente bietet. 
  
![Durch Auswählen eines Elements wird das Menü "Aktionen" aktiviert.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
Die Möglichkeit, mit einem Klick zu filtern und zu bestimmten Details zu navigieren, kann Ihnen viel Zeit bei der Untersuchung von Bedrohungen ersparen.

## <a name="queries-and-filters"></a>Abfragen und Filter

Der Explorer verfügt über mehrere leistungsstarke Filter und Abfragefunktionen, mit denen Sie Details wie die wichtigsten Zielbenutzer, die wichtigsten Malware Familien, die Erkennungstechnologie und vieles mehr eingehen können. Jede Art von Bericht bietet eine Vielzahl von Möglichkeiten zum Anzeigen und Durchsuchen von Daten.

> [!IMPORTANT]
> Verwenden Sie in der Abfrage Leiste für Explorer keine Platzhalterzeichen wie ein Sternchen (*) oder ein Fragezeichen (?). Wenn Sie im Feld Betreff für e-Mail-Nachrichten suchen, führt der Explorer eine partielle Übereinstimmung aus und liefert Ergebnisse, die der Platzhaltersuche ähneln.

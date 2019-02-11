---
title: Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definieren Sie die Aktivität Richtlinien mit Office 365-Cloud-App-Sicherheit, um Benachrichtigungen einrichten ausgelöst, wenn bestimmte Aktivitäten auftreten oder zu häufig vorkommen. Durch das Einrichten von Richtlinien für Warnungen ausgelöst, benachrichtigt werden können und bestimmte Vorgänge überwachen.
ms.openlocfilehash: af364e7ff96f6d18b60d3267c5992d4c5533ea8c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29604092"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security

Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](anomaly-detection-policies-in-ocas.md) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
Mit Office 365 Cloud App-Sicherheit auslösen erweiterte Cloud Informationsverwaltungsrichtlinien Warnungen für bestimmte Aktivitäten, die auftreten oder zu häufig vorkommen. Nehmen wir beispielsweise bei ein Benutzer versucht, sich bei Office 365 anmelden und ein Fehler auftritt, 70 Mal in einer Minute. Angenommen Sie, ein anderer Benutzer 7.000 Dateien Downloads oder angezeigt wird, in Kanada angemeldet sein, wenn der Benutzer an einem anderen Standort werden soll. Oder schlechter, nehmen Sie an, dass die Person Konto gefährdet, und ein Angreifer dieses Konto Zugriff auf die Cloud apps Ihrer Organisation und vertrauliche Daten verwendet.
  
Wenn Sie ein [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)sind, benachrichtigen Aktivität Benachrichtigungen, dass Sie, wenn Ereignisse wie diese auftreten. Sie können dann übernehmen bestimmte Aktionen, wie beispielsweise ein Benutzerkonto aussetzen, bis Sie untersuchen können, was passiert ist.
  
> [!NOTE]
> Office 365 Cloud App-Sicherheitsrichtlinien unterscheiden sich von [Warnen Richtlinien in die Office 365-Sicherheit &amp; Compliance Center](alert-policies.md). Cloud-Umgebung Ihrer Organisation verwalten der Aktivität in diesem Artikel beschriebenen Richtlinien sind in der Cloud App Sicherheit in Office 365-Portal definiert und können Ihnen helfen. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen:

Stellen Sie Folgendes sicher:
  
- Ihre Organisation verfügt [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).
    
- [Protokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Office 365-Umgebung aktiviert. 
    
- Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.
    
## <a name="create-a-new-activity-policy"></a>Erstellen einer neuen Richtlinie Aktivität

1. Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zum Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung. <br>Dadurch gelangen Sie zur Seite Office 365 Cloud App-Sicherheitsrichtlinien.<br>![Wenn Sie das Cloud-App Sicherheit in Office 365-Portal aufrufen, beginnen Sie mit der Seite Richtlinien](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. Klicken Sie auf **Richtlinie erstellen**, und wählen Sie dann auf **Richtlinie Aktivität**.<br>![Wenn Sie eine Richtlinie in O365 CAS erstellen, können Sie zwischen Aktivität und Normalbetriebswerte Richtlinien auswählen.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. Geben Sie auf der Seite **die Aktivität Richtlinie erstellen** den **Richtliniennamen** und eine **Beschreibung**ein. Um die Richtlinie auf eine entsprechende Standardvorlage basieren soll, wählen Sie in der Liste **Vorlagen für Gruppenrichtlinien** , oder erstellen Sie eine eigene Richtlinie ohne eine Vorlage.<br>![Sie können mit Office 365-Cloud-App-Sicherheit Aktivität Richtlinien erstellen.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. Wählen Sie eine **Richtlinie Schweregrad** (niedrig, Mittel oder hoch), mit denen gemessen, wie schwerwiegend für Sie ist, wenn diese Richtlinie eine Warnung ausgelöst wird. So können Sie Warnungen gefiltert werden, wenn Sie später überprüfen möchten. 
    
5. Wählen Sie eine **Kategorie** für diese Richtlinie. Dies hilft Ihnen filtern und Sortieren Warnungen, die ausgelöst wurden, oder wenn Sie diese Änderungen vornehmen können Sie feststellen, Gruppenrichtlinien. 
    
6. Wählen Sie **über Benutzeraktivität – Filter** einrichten, andere Aktionen oder Metriken, die eine Warnung basierend auf dieser Richtlinie ausgelöst werden. 
    
7. Klicken Sie unter **Aktivität Parametern entsprechen**Geben Sie an, ob eine Richtlinie Verletzung ausgelöst wird, wenn eine einzelne Aktivität die Filter entspricht, oder ob eine angegebene Anzahl von Aktivitäten wiederholt erforderlich ist, bevor die Warnung löst.<br>Wenn Sie **wiederholt Aktivität**auswählen, geben Sie die Anzahl der Aktivitäten, den Zeitrahmen und gibt an, ob eine Verletzung für einen Benutzer in eine bestimmte app oder für den gleichen Benutzer mit einer beliebigen app zählen wird.
    
8. Optional können Sie **Create-Benachrichtigung** , die zusätzliche Benachrichtigungen Erhalt von Benachrichtigungen aus dieser Richtlinie (per e-Mail, Textnachricht oder beides) erstellen auswählen.<br>**Stellen Sie sicher, dass Ihre e-Mail-Anbieter von gesendeten e-Mails nicht blockiert `no-reply@cloudappsecurity.com` **. 
  
9. Wählen Sie die **Aktionen** , die ausgeführt werden sollte, wenn eine Warnung ausgegeben wird, zu der Benutzer muss der Benutzer erneut anmelden für Office 365-apps. 
    
10. Wählen Sie **Create** zum Abschließen der Erstellung der Richtlinie. 
    
## <a name="next-steps"></a>Nächste Schritte

- [Anomalie Erkennungsrichtlinien](anomaly-detection-policies-in-ocas.md)
    
- [Integrieren von Ihrem Server SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)
    


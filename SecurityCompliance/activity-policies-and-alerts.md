---
title: Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definieren Sie Aktivitätsrichtlinien mit Office 365 Cloud App Security, um Warnungen einzurichten, die ausgelöst werden, wenn bestimmte Aktivitäten zu häufig stattfinden. Durch das Einrichten von Richtlinien zum Auslösen von Warnungen können Sie über bestimmte Aktivitäten benachrichtigt werden und diese überwachen.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219765"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](anomaly-detection-policies-in-ocas.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |
   
Mit Office 365 Cloud App Security lösen erweiterte Cloud-Verwaltungsrichtlinien Warnungen für bestimmte Aktivitäten aus, die passieren oder zu häufig auftreten. Nehmen Sie beispielsweise an, ein Benutzer versucht, sich bei Office 365 anzumelden und schlägt in einer Minute 70-mal fehl. Nehmen wir an, dass ein anderer Benutzer 7.000-Dateien herunterlädt oder anscheinend aus Kanada angemeldet ist, wenn sich dieser Benutzer an einem anderen Standort befinden soll. Oder schlimmer noch: angenommen, das Konto eines Benutzers wurde kompromittiert, und ein Angreifer verwendet dieses Konto, um auf Cloud-apps und vertrauliche Daten Ihrer Organisation zuzugreifen.
  
Wenn Sie ein [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)sind, Benachrichtigen Sie Aktivitäts Warnungen, wenn Ereignisse wie diese auftreten. Sie können dann bestimmte Aktionen ausführen, beispielsweise das Anhalten eines Benutzerkontos, bis Sie untersuchen können, was passiert ist.
  
> [!NOTE]
> Office 365 Cloud App-Sicherheitsrichtlinien unterscheiden sich von [Warnungsrichtlinien im office 365 &amp; Security Compliance Center](alert-policies.md). Die in diesem Artikel beschriebenen Aktivitätsrichtlinien sind im Sicherheitsportal der Office 365 Cloud App definiert und können Ihnen dabei helfen, die Cloud-Umgebung Ihrer Organisation besser zu verwalten. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Stellen Sie Folgendes sicher:
  
- Ihre Organisation verfügt über [Office 365 Cloud App Security](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).
    
- Die [Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für ihre Office 365-Umgebung aktiviert. 
    
- Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.
    
## <a name="create-a-new-activity-policy"></a>Erstellen einer neuen Aktivitätsrichtlinie

1. Wechseln Sie als globaler Administrator oder Sicherheitsadministrator zum Sicherheitsportal der Cloud-app ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an. <br>Dadurch gelangen Sie zur Seite Office 365 Cloud App Security Policies.<br>![Wenn Sie zum Office 365 Cloud App Security Portal wechseln, beginnen Sie mit der Seite Richtlinien](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. Klicken Sie auf **Richtlinie erstellen**, und wählen Sie dann **Aktivitätsrichtlinie**aus.<br>![Wenn Sie eine Richtlinie in O365-CAS erstellen, können Sie zwischen Aktivitätsrichtlinien und Erkennungsrichtlinien für Anomalien wählen.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. Geben Sie auf der Seite **Aktivitätsrichtlinie erstellen** den Namen und die **Beschreibung**der **Richtlinie** an. Wenn Sie die Richtlinie auf einer Standardvorlage basieren möchten, wählen Sie eine in der Liste **Richtlinienvorlage** aus, oder erstellen Sie Ihre eigene Richtlinie, ohne eine Vorlage zu verwenden.<br>![Sie können Aktivitätsrichtlinien mit Office 365 Cloud App Security erstellen.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. Wählen Sie einen **Richtlinien Schweregrad** (niedrig, Mittel oder hoch) aus, der misst, wie schwerwiegend es für Sie ist, wenn diese Richtlinie eine Warnung auslöst. Dadurch können Sie Warnungen filtern, wenn Sie Sie später überprüfen. 
    
5. Wählen Sie eine **Kategorie** für diese Richtlinie aus. Dadurch können Sie Warnungen Filtern und sortieren, die ausgelöst wurden, oder Gruppenrichtlinien, wenn Sie Sie überprüfen, um Änderungen vorzunehmen. 
    
6. Wählen Sie **Aktivitäts Filter** aus, um andere Aktionen oder Metriken einzurichten, die eine Warnung basierend auf dieser Richtlinie auslösen. 
    
7. Geben Sie unter **Vorgangs Übereinstimmungsparameter**an, ob eine Richtlinienverletzung ausgelöst wird, wenn eine einzelne Aktivität mit den Filtern übereinstimmt oder ob eine angegebene Anzahl von wiederholten Aktivitäten vor dem Auslösen der Warnung erforderlich ist.<br>Wenn Sie **wiederholte Aktivität**auswählen, geben Sie die Anzahl der Aktivitäten, den Zeitrahmen und an, ob eine Verletzung für einen Benutzer innerhalb einer bestimmten app oder für denselben Benutzer mit einer beliebigen App gezählt werden soll.
    
8. Optional können Sie **Alert erstellen** auswählen, um zusätzliche Benachrichtigungen für den Empfang von Benachrichtigungen von dieser Richtlinie zu erstellen (per e-Mail, Textnachricht oder beides).<br>**Stellen Sie sicher, dass Ihr e-Mail-Anbieter `no-reply@cloudappsecurity.com`e-Mails, die gesendet werden, nicht blockiert **. 
  
9. Wählen Sie die **Aktionen** aus, die ausgeführt werden sollen, wenn eine Warnung ausgelöst wird, um den Benutzer anzuhalten, oder wenn der Benutzer sich erneut bei Office 365-Apps anmelden muss. 
    
10. Klicken Sie auf **Erstellen** , um die Erstellung der Richtlinie abzuschließen. 
    
## <a name="next-steps"></a>Nächste Schritte

- [Erkennungsrichtlinien für Anomalien](anomaly-detection-policies-in-ocas.md)
    
- [Integrieren Ihres SIEM-Servers](integrate-your-siem-server-with-office-365-cas.md)
    
- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
- [Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)
    


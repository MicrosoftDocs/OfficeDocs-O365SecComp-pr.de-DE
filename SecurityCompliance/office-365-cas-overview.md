---
title: Übersicht über Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Office 365-Cloud-App-Sicherheit können Sie Einblicke in verdächtige Aktivitäten in Office 365, sodass Sie Situationen, die potenziell problematisch und untersuchen können bei Bedarf Ausführen einer Aktion zum Beheben von Sicherheitsproblemen. '
ms.openlocfilehash: edce16edca822bed30c78f34cf141b23f2b2fb8c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382548"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Übersicht über Office 365 Cloud App Security
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|Sie sind hier!  <br/> [Nächster Schritt](get-ready-for-office-365-cas.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Office 365-Cloud-App-Sicherheit ist in Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann Office 365-Cloud-App-Sicherheit als Add-on erworben werden. (Als ein globaler Administrator in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on). 
  
Office 365-Cloud-App-Sicherheit gibt Ihnen einen Einblick in die verdächtige Aktivitäten in Office 365, sodass Sie Situationen, die potenziell problematisch und untersuchen können bei Bedarf Ausführen einer Aktion zum Beheben von Sicherheitsproblemen. Mit Office 365 Cloud App-Sicherheit können Sie Benachrichtigungen der ausgelösten Warnungen für untypischen oder verdächtigen Aktivitäten, finden Sie unter wie Ihrer Organisation Daten in Office 365 zugegriffen und verwendet, Benutzerkonten verdächtige Aktivitäten auf Anhalten und erfordern Benutzer melden Sie sich dann wieder anmelden für apps für Office 365 nach dem eine Warnung ausgelöst wurde. Lesen Sie diesen Artikel, um einen Überblick über die Sicherheit in Office 365 Cloud App-Features und Funktionen erhalten.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>So finden Sie das Cloud App Sicherheit in Office 365-portal

> [!NOTE]
> Zugriff auf das Cloud-App Sicherheit in Office 365-Portal, müssen Sie ein Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheit Reader sein. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
Sie können Cloud App Sicherheit in Office 365-Portal abrufen, indem Sie auf [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) von und Anmelden bei. 

Sie können auch abrufen es aus der Office 365-Sicherheit &amp; Compliance Center. Hier ist eine gute Möglichkeit zur Verfügung:
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**. <br/>![Wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Falls die Office 365-Cloud-App-Sicherheit noch nicht aktiviert, und Sie sind ein globaler Administrator, [Office 365-Cloud-App-Sicherheit zu aktivieren](turn-on-office-365-cas.md).)
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**. 
    
## <a name="policies"></a>Policies

Office 365 funktioniert Cloud App-Sicherheit mit Richtlinien, die für Ihre Organisation definiert sind. Mit Office 365 Cloud App-Sicherheit ruft Ihrer Organisation viele vordefinierte Anomalie Erkennungsrichtlinien und mehrere Vorlagen für Richtlinien Aktivität ab. Diese Richtlinien dienen zum Erkennen allgemeiner Bildschirmdarstellung auftreten, Identifizieren von Benutzern von einem riskant IP-Adresse anmelden, Ransomware Aktivitäten zu erkennen, Administrator private IP-Adressen und weitere Aktivitäten zu erkennen.
  
![Wählen Sie im Portal CAS Steuerelement \> Vorlagen anzeigen oder Erstellen von Vorlagen für Benutzerrechterichtlinien](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
Um/Richtlinienvorlagen, in der Cloud App Sicherheit in Office 365-Portal Verwendung anzeigen, wechseln Sie zum **Steuerelement** \> **Vorlagen**. 
  
![Wählen Sie im Portal O365 CAS Steuerelement](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Weitere Informationen zu Richtlinien finden Sie unter den folgenden Ressourcen:
  
- [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Benachrichtigungen

Wenn Richtlinien definiert sind, benachrichtigen Sie Warnungen zu verdächtigen oder untypischen Aktivitäten, die erkannt wurden. Wählen Sie zum Anzeigen von Benachrichtigungen für Ihre Organisation **Warnungen** in der Navigationsleiste oben auf dem Bildschirm. 
  
![Klicken Sie auf der Seite Warnungen finden Sie unter Benachrichtigungen, die ausgelöst wurden und Aktionen.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
Warnungen dann ausgelöst werden, können Sie überprüfen, um weitere Informationen darüber, was passiert. Wenn die Aktivität weiterhin verdächtigen ist, können Sie Aktion nutzen. Beispielsweise können Sie einen Benutzer über ein Problem benachrichtigt werden Anhalten eines Benutzers anmelden bei Office 365, oder vom Benutzer für apps für Office 365 anmelden.
  
Weitere Informationen zu Benachrichtigungen finden Sie in den folgenden Ressourcen:
  
- [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Lesen Sie und führen Sie einer Aktion auf Office 365 Cloud App-Sicherheitshinweise aus](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Aktivitätsprotokolle

Anzeigen von Informationen über die Benutzeraktivitäten auf Ihrer Seite Aktivität Protokoll in Office 365-Cloud-App-Sicherheit.
  
![Wählen Sie im Portal O365 CAS untersuchen \> Aktivitätsprotokolls](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
Auf dieser Seite, in der Cloud App Sicherheit in Office 365-Portal, wechseln Sie zu **untersuchen** \> **Aktivitätsprotokolls**. 
  
![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Sie können die Protokolle der Web-Datenverkehr mit Office 365 Cloud App-Sicherheit zu verwenden. Weitere Details, die in diesen enthaltenen Protokolldateien, besseren Einblick in die Sie in Benutzeraktivität. Sie können Protokolldateien von Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo auch, Sophos, Kalmare, Websence, Zscaler und vieles mehr.
  
[Informationen Sie zu Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>OAuth-apps

Sie können mit Office 365 Cloud App-Sicherheit ermöglichen oder verhindern, dass Personen in Ihrer Organisation Drittanbieter-apps verwenden können, die Zugriff auf Daten in Office 365.
  
![In Office 365-CAS können Sie die Seite OAuth Verwalten von apps aus dem Menü untersuchen zugreifen.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Wenn Sie diese Seite erhalten möchten, wechseln Sie zu **untersuchen** \> **OAuth-apps**. 
  
![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Verwalten von OAuth-Apps mit Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Cloud-Discovery-Dashboard

Das **Cloud-Discovery-Dashboard**, auch als **Produktivität App Discovery**bezeichnet werden Informationen zu Cloud app-Nutzung in Ihrer Organisation. Sie können Informationen zu apps, Benutzer, Datenverkehr, Transaktionen und viele weitere verwenden dieses Dashboards anzeigen. Das Cloud-Discovery-Dashboard ähnelt der folgenden Abbildung: 
  
![Wählen Sie im Office 365 CAS-Portal Discover \> Cloud Discovery-Dashboard](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Auf diesem Dashboard, in der Cloud App Sicherheit in Office 365-Portal finden **Discover** \> **Cloud Discovery-Dashboard**. 
  
![Wählen Sie im Office 365 CAS-Portal Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Nächste Schritte

- Rufen Sie die [Anwendungsfälle für Office 365 Cloud App-Sicherheit und Benutzerhandbuch](https://aka.ms/O365CASGuide)
    
- [Einstieg in Office 365 Cloud App Security](get-ready-for-office-365-cas.md)
    


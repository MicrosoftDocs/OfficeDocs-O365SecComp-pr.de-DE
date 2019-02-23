---
title: Übersicht über Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Office 365 Cloud App Security bietet Ihnen Einblicke in verdächtige Aktivitäten in Office 365, damit Sie potenziell problematische Situationen untersuchen und gegebenenfalls Maßnahmen zur Behebung von Sicherheitsproblemen ergreifen können. '
ms.openlocfilehash: 974858a547d9af2db600f9856efbce619a3b38e4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220175"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Übersicht über Office 365 Cloud App Security
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|Sie sind hier!  <br/> [Nächster Schritt](get-ready-for-office-365-cas.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Office 365 Cloud App Security ist in Office 365 Enterprise E5 verfügbar. Wenn Ihre Organisation ein anderes Office 365 Enterprise-Abonnement verwendet, kann Office 365 Cloud App Security als Add-on erworben werden. (klicken sie als globaler administrator im Office 365 admin center auf **abrechnungs** \> **abonnements hinzufügen**.) Weitere Informationen finden Sie unter [office 365 Platform Service Description: office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) und [kaufen oder Bearbeiten eines add-ons für Office 365 for Business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on). 
  
Office 365 Cloud App Security bietet Ihnen Einblicke in verdächtige Aktivitäten in Office 365, damit Sie potenziell problematische Situationen untersuchen und bei Bedarf Maßnahmen zur Behebung von Sicherheitsproblemen ergreifen können. Mit Office 365 Cloud App Security können Sie Benachrichtigungen über ausgelöste Warnungen für atypische oder verdächtige Aktivitäten erhalten, Informationen dazu, wie die Daten Ihrer Organisation in Office 365 zugegriffen und verwendet werden, Benutzerkonten, die verdächtige Aktivitäten ausstellen, anhalten und Benutzer melden sich wieder bei Office 365-apps an, nachdem eine Warnung ausgelöst wurde. Lesen Sie diesen Artikel, um einen Überblick über die Sicherheitsfeatures und-Funktionen von Office 365 Cloud APP zu erhalten.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>So finden Sie das Office 365 Cloud App Security Portal

> [!NOTE]
> Um auf das Office 365 Cloud App Security Portal zuzugreifen, müssen Sie ein globaler Office 365-Administrator, Sicherheitsadministrator oder Sicherheits Leser sein. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
Sie können das Office 365 Cloud App-Sicherheitsportal aufrufen, indem Sie [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) sich anmelden. 

Sie können auch über das Office 365 Security &amp; Compliance Center dorthin gelangen. Hier ist eine gute Möglichkeit, dies zu tun:
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. (Dadurch gelangen Sie zum Security &amp; Compliance Center.)
    
2. Wählen Sie im &amp; Security Compliance Center **Alerts** \> **Manage Advanced Alerts**aus. <br/>![Wählen Sie erweiterte Benachrichtigungen verwalten aus, um zu Office 365 Cloud App Security zu wechseln.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Wenn Office 365 Cloud App Security noch nicht aktiviert ist und Sie ein globaler Administrator sind, [Aktivieren Sie office 365 Cloud App Security](turn-on-office-365-cas.md).)
    
3. Wählen Sie **Gehe zu Office 365 Cloud App Security**. 
    
## <a name="policies"></a>Policies

Office 365 Cloud App Security arbeitet mit den Richtlinien, die für Ihre Organisation definiert sind. Mit Office 365 Cloud App Security erhält Ihre Organisation viele vordefinierte Anomalie-Erkennungsrichtlinien und mehrere Vorlagen für Aktivitätsrichtlinien. Diese Richtlinien sollen allgemeine Anomalien erkennen, Benutzer identifizieren, die sich von einer riskanten IP-Adresse anmelden, Ransomware-Aktivitäten erkennen, Administratoraktivitäten von nicht-unternehmensinternen IP-Adressen erkennen und vieles mehr.
  
![Wählen Sie im CAS-Portal Steuer \> Elementvorlagen aus, um Richtlinienvorlagen anzuzeigen oder zu erstellen.](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
um richtlinienvorlagen anzuzeigen und zu verwenden, navigieren sie im Office 365 Cloud App Security-portal zu **steuerelement** \> **vorlagen**. 
  
![Wählen Sie im O365-CAS-Portal die Option Steuerelement](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Weitere Informationen zu Richtlinien finden Sie in den folgenden Ressourcen:
  
- [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Benachrichtigungen

Wenn Richtlinien definiert sind, Benachrichtigen Sie Warnungen über verdächtige oder atypische Aktivitäten, die erkannt wurden. Um Benachrichtigungen für Ihre Organisation anzuzeigen, wählen Sie in der Navigationsleiste am oberen Rand des Bildschirms **Benachrichtigungen** aus. 
  
![Auf der Seite Warnungen werden Warnungen angezeigt, die ausgelöst wurden, und alle ausgeführten Aktionen.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
Wenn Warnungen ausgelöst werden, können Sie diese überarbeiten, um mehr über die Vorgehensweise zu erfahren. Wenn die Aktivität weiterhin verdächtig ist, können Sie Maßnahmen ergreifen. Sie können beispielsweise einen Benutzer über ein Problem informieren, einen Benutzer davon abhalten, sich bei Office 365 anzumelden, oder einen Benutzer zur Anmeldung bei Office 365-apps auffordern.
  
Weitere Informationen zu Warnungen finden Sie in den folgenden Ressourcen:
  
- [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Überwachen und Aktionen für Office 365 Cloud App Security Alerts](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Aktivitätsprotokolle

Informationen zu Benutzeraktivitäten auf der Aktivitätsprotokoll Seite in Office 365 Cloud App Security.
  
![Wählen Sie im O365-CAS-Portal \> die Option Aktivitätsprotokoll untersuchen aus.](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
um zu dieser seite zu gelangen, navigieren sie im sicherheitsportal der Office 365 Cloud-App zum **untersuchen** \> des **aktivitätsprotokolls**. 
  
![Wählen Sie im O365-CAS-Portal untersuchen aus.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Sie können Ihre Web-Traffic-Protokolle auch mit Office 365 Cloud App Security verwenden. Je mehr Details in diesen Protokolldateien enthalten sind, desto besser ist die Sichtbarkeit in der Benutzeraktivität. Sie können Protokolldateien von Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler und mehr verwenden.
  
[Informationen zu Webtraffic-Protokollen und Datenquellen für Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>OAuth-apps

Mit Office 365 Cloud App Security können Sie zulassen oder verhindern, dass Personen in Ihrer Organisation Drittanbieter-Apps verwenden, die auf Daten in Office 365 zugreifen.
  
![In O365-CAS können Sie über das Menü untersuchen auf die Seite OAuth-apps verwalten zugreifen.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Um zu dieser Seite zu gelangen, wechseln Sie zu **OAuth apps** **untersuchen** \> . 
  
![Wählen Sie im O365-CAS-Portal untersuchen aus.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Verwalten von OAuth-Apps mit Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Cloud Discovery-Dashboard

Das **Cloud Discovery-Dashboard**, auch als Produktivitäts- **App-Erkennung**bezeichnet, zeigt Informationen zur Verwendung von Cloud-apps in Ihrer Organisation. Mithilfe dieses Dashboards können Sie Informationen zu apps, Benutzern, Datenverkehr, Transaktionen und mehr anzeigen. Das Cloud Discovery-Dashboard ähnelt der folgenden Abbildung: 
  
![Wählen Sie im Office 365-CAS-Portal \> Discover Cloud Discovery Dashboard aus.](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
um zu diesem dashboard zu gelangen, navigieren sie im sicherheitsportal der Office 365 cloud-App zu **Discover** \> **cloud Discovery dashboard**. 
  
![Wählen Sie im Office 365-CAS-Portal Discover aus.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Nächste Schritte

- Abrufen der [Office 365 Cloud App Security Use Cases und Usage Guide](https://aka.ms/O365CASGuide)
    
- [Einstieg in Office 365 Cloud App Security](get-ready-for-office-365-cas.md)
    


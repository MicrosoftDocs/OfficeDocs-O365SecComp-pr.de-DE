---
title: Einstieg in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Erste Schritte mit Office 365-Cloud-App-Sicherheit
ms.openlocfilehash: 1d1ae464278a5d9aafa5a176298f03174b6a37dc
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603696"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Einstieg in Office 365 Cloud App Security
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](turn-on-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
Beim Vorbereiten zu aktivieren und Office 365-Cloud App-Sicherheit (vormals Advanced Security Management) für Ihre Organisation zu implementieren, gibt es einige Dinge bedenken. Verwenden Sie diesen Artikel als Leitfaden zum Planen von Office 365-Cloud-App-Sicherheit.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>Schritt 1: Identifizieren Sie und schützen Sie Ihrer Administratorkonten globalen und Sicherheit

Globale Administratoren Sicherheitsadministratoren und Sicherheit Leser können auf das Office 365-Cloud-App-Sicherheit Portal zeigen Sie Richtlinien und Hinweise überprüfen Integritätsberichte zugreifen. Globale Administratoren und Sicherheitsadministratoren können Richtlinien definieren und weiteren Aktionen zum Schutz Ihrer Organisation. (Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).) Überprüfen Sie Ihrer Organisation Benutzerkonten, die als Vorsichtsmaßnahme Berechtigungen erweiterte. 
  
 **[Schützen von Office 365 globaler Administratorkonten](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>Schritt 2: Aktivieren der überwachungsprotokollierung für Ihre Organisation

In der Reihenfolge für Office 365-Cloud-App-Sicherheit korrekt funktioniert muss überwachungsprotokollierung aktiviert werden. Dies wird normalerweise von einem Exchange Online-Administrator oder ein globaler Administrator ausgeführt.
  
 **[Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md)**. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>Schritt 3: Navigieren Sie zur Cloud App Sicherheit in Office 365-portal

Sie können Cloud App Sicherheit in Office 365-Portal abrufen, indem Sie auf [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) von und Anmelden bei. 

Sie können auch abrufen es aus der Office 365-Sicherheit &amp; Compliance Center. Hier ist eine gute Möglichkeit zur Verfügung:

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und Anmeldung (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)
    
2. Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit** , fahren Sie mit der Cloud App Sicherheit in Office 365-Portal.<br> ![Wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>Wenn Sie das Cloud-App Sicherheit in Office 365-Portal aufrufen, ist auf der erste Seite finden Sie unter der Richtlinien-Seite, die in der folgenden Abbildung ähnelt:<br>![Wenn Sie das Cloud-App Sicherheit in Office 365-Portal aufrufen, beginnen Sie mit der Seite Richtlinien](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)<br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>Schritt 4: Definieren von Richtlinien und Benachrichtigungen einrichten &amp; Aktionen

Globale Administratoren und Sicherheitsadministratoren definieren Sie Richtlinien in Office 365-Cloud-App-Sicherheit. Während der Verarbeitung Richtlinien definieren werden Warnungen und Aktionen auch festgelegt. Eine Benachrichtigung ist eine Benachrichtigung, anhand von Kriterien, die in einer Ansicht angezeigt wird, oder per e-Mail gesendet wird. 
  
Es gibt zwei Arten von Warnungen in Office 365-Cloud-App-Sicherheit: Anomalie Erkennung Warnungen, die verdächtigen Aktivitäten zu erkennen und Aktivität Warnungen, die für Aktivitäten, die möglicherweise untypischen für Ihre Organisation definiert sind. Alerts benachrichtigen globale Administratoren und Sicherheitsadministratoren, wenn in Ihrer Office 365-Umgebung, die für Ihre Organisation ungewöhnlich ist eine Aktivität stattgefunden hat.
  
Finden Sie in den folgenden Ressourcen, um mehr zu erfahren:
  
- [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md)
    
- [Lesen Sie und führen Sie einer Aktion auf Office 365 Cloud App-Sicherheitshinweise aus](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a>Schritt 5: Informationen Sie zur Verwendung von Ihrer Organisation cloud

Als globaler Administrator, Sicherheitsadministrator oder Sicherheit Leser erhalten Sie zur Verwendung von Ihrer Organisation Cloud über Berichte und einer Cloud-Discovery-Dashboard (auch als Produktivität App Discovery bezeichnet). Das Dashboard zeigt Informationen über Benutzer, apps, Webdatenverkehr und Risikoebenen.
  
![Wählen Sie im Office 365 CAS-Portal Discover \> Cloud Discovery-Dashboard](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
So wechseln zur Produktivität App Discovery-Dashboard, in der Cloud App Sicherheit in Office 365-Portal, wählen Sie **Discover** \> **Cloud Discovery-Dashboard**.
  
![Wählen Sie im Office 365 CAS-Portal Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
Um Berichte mit den Informationen zu füllen, die Sie benötigen, laden Sie die Protokolldateien aus Ihrer Organisation Firewalls und Proxys. Finden Sie weitere Informationen finden Sie unter den folgenden Ressourcen:
  
- [Erstellen von app-Discovery-Berichten in Office 365-Cloud-App-Sicherheit](create-app-discovery-reports-in-ocas.md)
    
- [Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a>Schritt 6: Verwalten von apps, die Ihre Organisation die Access Office 365 verwendet

Als globaler Administrator oder Sicherheitsadministrator können Sie apps, wie benutzerdefinierte apps oder Drittanbieter-apps, die auf ihren Geräten mit Office 365 Personen in Ihrer Organisation verwenden verwalten. Nehmen wir beispielsweise bei einer Person eine benutzerdefinierte Anwendung heruntergeladen wurde, die sie mit Office 365 verwenden möchten. Sie können überprüfen die apps, die Benutzern verwendet werden, nicht vertrauenswürdigen apps sperren oder Markieren von apps für Ihre Zwecke Tracking ausdrücklich genehmigt hat. [Verwalten von OAuth-apps mithilfe von Office 365-Cloud-App-Sicherheit](manage-app-permissions-in-ocas.md).
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a>Schritt 7: Verwenden des SIEM Servers mit Office 365-Cloud-App-Sicherheit

Ist Ihre Organisation einen Sicherheit und Ereignissen (SIEM) Verwaltungsserver verwendet? Office 365 Cloud App-Sicherheit können jetzt mit Ihrem SIEM Server zum Aktivieren der zentralisierten Überwachung von Warnungen integrieren. Integration mit einem Dienst SIEM können Sie besser schützen einer Cloud-Anwendung verwalten Ihrem Workflow üblichen Sicherheit, Sicherheitsverfahren automatisieren und Korrelation zwischen Cloud-basierten und lokale Ereignisse. Der SIEM-Agent auf dem Server ausgeführt wird, Benachrichtigungen von Office 365-Cloud-App-Sicherheit abruft und überträgt diese Warnungen in Ihrem SIEM-Server. Finden Sie unter [SIEM-Integration mit Office 365-Cloud-App-Sicherheit](integrate-your-siem-server-with-office-365-cas.md).
  
## <a name="next-steps"></a>Nächste Schritte

- [Aktivieren von Office 365 Cloud App Security](turn-on-office-365-cas.md)
    
- Versuchen Sie unsere [Test Lab Guide](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) Hands-On-Erfahrung, in dem Sie veranschaulichen die leistungsstarken Funktionen von Office 365-Cloud-App-Sicherheit und erstellen eine Machbarkeitsstudie können. 
    


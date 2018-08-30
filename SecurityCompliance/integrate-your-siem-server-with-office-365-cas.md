---
title: Integrieren von Ihrem Server SIEM mit Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Sie können Ihre SIEM Server mit Office 365-Cloud-App-Sicherheit integriert. Lesen Sie diesen Artikel, um Sie erhalten einen Überblick über die Funktionsweise und wie es einrichten.
ms.openlocfilehash: 6b9d51d91d4b1ae55dd0dd16a92872daa4ecef90
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23043263"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Integrieren von Ihrem Server SIEM mit Office 365-Cloud-App-Sicherheit
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](utilization-activities-for-ocas.md) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
Sie können die [Office 365-Cloud-App-Sicherheit](get-ready-for-office-365-cas.md) mit der Sicherheit und Ereignissen (SIEM) Verwaltungsserver zum Aktivieren der zentralisierten Überwachung von Warnungen integrieren. Dies ist besonders wichtig für Organisationen, die mithilfe von Clouddiensten und lokale serveranwendungen. Integrieren von in einem SIEM Server kann Ihr Sicherheitsteam besser schützen Ihrer Office 365-Applikationen Beibehaltung des Workflows üblichen Sicherheit durch Automatisierung bestimmte Sicherheitsverfahren und Korrelation zwischen cloudbasierten und lokale Ereignisse.  
  
Wenn Sie zunächst den Server SIEM mit Office 365-Cloud-App-Sicherheit integrieren, werden Warnungen aus den letzten zwei Tagen die SIEM-Server als auch alle Benachrichtigungen aus dann auf weitergeleitet (basierend auf alle Filter, die Sie auswählen). Wenn Sie dieses Feature für einen längeren Zeitraum, deaktivieren, wenn Sie es erneut aktivieren, wird es die letzten zwei Tagen von Benachrichtigungen und klicken Sie dann alle Benachrichtigungen für anschließend weitergeleitet werden.
 
## <a name="siem-integration-architecture"></a>Architektur für die Integration von SIEM

Ein Agent SIEM ist im Netzwerk der Organisation eingerichtet. Wenn bereitgestellt und konfiguriert ist, ruft der SIEM-Agent die Datentypen, die konfiguriert wurden (Benachrichtigungen) mithilfe von Office 365 Cloud App Sicherheit Rest-APIs. Der Datenverkehr wird dann über einen verschlüsselten HTTPS-Kanal an Port 443 gesendet.
  
Wenn ein SIEM-Agent Daten aus Office 365-Cloud-App-Sicherheit abruft, sendet er die Syslog-Nachrichten zum lokalen SIEM-Server mit der Netzwerkkonfigurationen, die während des Setups (TCP oder UDP mit einem benutzerdefinierten Port) bereitgestellt werden.

![Architektur SIEM und Cloud App-Sicherheit](media/siem-architecture.png)

## <a name="supported-siem-servers"></a>Unterstützte SIEM-Server

Office 365-Cloud-App-Sicherheit unterstützt derzeit die folgenden SIEM-Server:
- Micro Fokus ArcSight
- Generische CEF

## <a name="prerequisites"></a>Voraussetzungen

- Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Aufgaben in diesem Artikel beschrieben werden. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- Sie müssen [Office 365-Cloud-App-Sicherheit aktiviert](turn-on-office-365-cas.md) für Ihre Organisation verfügen.

- [Protokollierung](turn-audit-log-search-on-or-off.md) muss für Office 365 aktiviert werden

- Sie müssen einen standard-Server sein, der zum Konfigurieren der Integration von SIEM Server die folgenden Anforderungen erfüllt:
    - Betriebssystem: Windows oder Linux (Dies kann einen virtuellen Computer sein)
    - CPU: 2
    - Festplattenspeicher: 20 GB
    - RAM: 2 GB
    - [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installiert
    - Firewall gemäß der Beschreibung in [netzwerkanforderungen](https://docs.microsoft.com/cloud-app-security/network-requirements) konfiguriert

- Benötigen Sie Details zu Ihren **Remote Syslog Host** und **Syslot Portnummer**ein. Netzwerkadministrator oder Sicherheitsadministrator sollten Sie finden diese Informationen helfen können. 

- Sie müssen die [JAR-Datei](https://go.microsoft.com/fwlink/?linkid=838596) herunterladen, Sie Ihre Server SIEM integriert müssen, [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) akzeptieren.
 
## <a name="integrate-office-365-cloud-app-security"></a>Integrieren von Office 365-Cloud-App-Sicherheit
    
### <a name="step-1-set-it-up-in-the-office-365-cloud-app-security-portal"></a>Schritt 1: Richten Sie es in die Cloud App Sicherheit in Office 365-Portal ein

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</br>
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Klicken Sie auf **Einstellungen** \> **Security Extensions**.</br>
![Wählen Sie Einstellungen > Sicherheit Erweiterungen](media/Settings-SecurityExtensions.png)

5. Wählen Sie **Agent SIEM hinzufügen**.</br>![Wählen Sie Agent SIEM hinzufügen.](media/SIEMAgents.png)
    
6. Wählen Sie auf **Assistenten starten**.</br>![Holen Sie sich Hilfe, oder starten Sie den Assistenten](media/HelpOrWizard.png) 
    
7. Geben Sie im **allgemeinen** Schritt einen Namen, und **Wählen Sie Ihre SIEM-Format aus** , und legen Sie eine beliebige **Erweiterte Einstellungen** , die für dieses Format relevant sind. Wählen Sie dann **Weiter**.</br>![Geben Sie einen Namen und Typ](media/ChooseAgentTypeAndName.png)
    
8. Geben Sie im Schritt **Remote Syslog** die IP-Adresse oder den Hostnamen der **Remote Syslog Host** und die **Portnummer Syslog**. Wählen Sie TCP oder UDP als Protokoll Remote Syslog. (Sie können arbeiten mit Ihrem Netzwerkadministrator oder Sicherheitsadministrator, um diese Informationen zu erhalten, wenn sie Ihnen keine.) Wählen Sie dann **Weiter**.</br>![Geben Sie Remote Syslog-details](media/ArcSightS1Syslog.png)
  
9. Im Schritt **Datentypen** einen der folgenden Schritte aus, und klicken Sie dann auf **Weiter**:
    - Behalten Sie die Standardeinstellung **Alle Warnungen**</br>OR
    - Klicken Sie auf **Alle Benachrichtigungen**, und wählen Sie dann auf **bestimmten Filter**. Definieren Sie Filter an, um die Arten von Benachrichtigungen wählen Sie auf Ihrem Server SIEM senden möchten.</br>![Datentypen Schritt des Assistenten](media/ArcSightS1ExportOptions.png)
  
10. Klicken Sie auf dem Bildschirm Herzlichen Glückwunsch kopieren Sie das Token, und speichern Sie sie zur späteren Verwendung.</br>![SIEM Agent erstellt Bildschirm](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> Zu diesem Zeitpunkt eine SIEM-Agenten in Office 365-Cloud-App-Sicherheit eingerichtet haben, aber Ihre SIEM-Server-Integration ist noch nicht abgeschlossen. Fahren Sie fort mit dem nächsten Schritt fort Ihrer SIEM-Server-Integration.

Nachdem Sie klicken Sie auf Schließen, und klicken Sie im Assistenten auf dem Bildschirm des Security Extensions lassen, sehen Sie den Agent SIEM, die, den Sie in der Tabelle hinzugefügt. Es wird weist den Status **erstellt** , bis es später verbunden ist.

![SIEM Agent erstellt](media/SIEMAgentCreated.png)
    
### <a name="step-2-download-the-jar-file-and-run-it-on-your-server"></a>Schritt 2: Laden Sie die JAR-Datei, und führen Sie es auf dem server

1. Laden Sie das [Microsoft Cloud App-SIEM-Sicherheitsmonitor](https://go.microsoft.com/fwlink/?linkid=838596) , und Entzippen Sie den Ordner. (Sie müssen [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) zustimmen, um fortzufahren.) 
    
2. Extrahieren Sie die JAR-Datei aus der ZIP-Ordner, und führen sie auf dem Server.
    
3. Nach der Ausführung der Datei, führen Sie den folgenden aus: Befehl:</br>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
#### <a name="important-notes"></a>Wichtige Hinweise:

- Der Dateiname kann je nach der Version des Agents SIEM variieren. 

- Es wird empfohlen, dass Sie die JAR-Füllung auf dem Server, während der Serverinstallation ausführen.
    - **Windows**: Führen Sie als geplante Aufgabe, und stellen Sie sicher, zum Konfigurieren der Task **ausgeführt wird, ob der Benutzer oder nicht angemeldet ist** , und deaktivieren Sie die Option **Task beenden, wenn er länger als ausgeführt wird** .

    - **Linux**: Hinzufügen des Befehls Ausführen mit einer **&** an die `rc.local` Datei. </br>Beispiel:</br> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- Parameter in Klammern [] sind optional und sollte verwendet werden, falls relevant. Verwenden Sie die folgenden Variablen:
    - **DIRNAME** ist der Pfad zu dem Verzeichnis, den, das Sie für den lokalen Agent Debugprotokolle verwenden möchten.
    - **Adresse [: PORT]** Proxy-Server-Adresse und Port, die der Server für die Verbindung mit dem Internet verwendet wird.
    - **TOKEN** ist das SIEM-Agent-Token, die, das Sie in der ersten Prozedur kopiert.
    - Um Hilfe zu erhalten, geben Sie ein `-h`. 
  
### <a name="step-3-validate-that-the-siem-agent-is-working"></a>Schritt 3: Überprüfen Sie, ob der Agent SIEM funktionsfähig ist

1. Stellen Sie sicher, dass der Status des SIEM-Agents in der Cloud App Sicherheit in Office 365-Portal wird nicht als **Verbindungsfehler** angezeigt oder **getrennt** und, es sind keine Benachrichtigungen Agent.</br>Beispielsweise sehen hier Sie, dass der Server SIEM verbunden ist:</br>![SIEM Server verbunden](media/siem-connected.png)</br>Und Hier können wir sehen, dass der SIEM getrennt ist:</br>![SIEM Server nicht verbunden](media/siem-not-connected.png) 
  
2. Stellen Sie in Ihrem Server Syslog/SIEM sicher, dass Sie sehen, dass Benachrichtigungen von Sicherheit in Office 365 Cloud App angekommen sind.
  
## <a name="regenerating-your-token"></a>Erneutes Generieren des Tokens

Wenn Sie Ihr Token verlieren, können Sie sie wiederherstellen. Suchen Sie in der Tabelle die Zeile für den SIEM-Agent. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann **erneut generieren Token**.

![Generieren Sie ein Token durch Klicken auf die Schaltfläche mit den Auslassungszeichen für Ihre SIEM-Agent neu](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
## <a name="editing-your-siem-agent"></a>Bearbeiten des SIEM-Agents

Suchen Sie die Zeile für den Agent SIEM, um Ihre SIEM-Agent in der Tabelle zu bearbeiten. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann auf **Bearbeiten**. Wenn Sie den Agent SIEM bearbeiten, müssen Sie nicht die JAR-Datei erneut ausführen; automatisch aktualisiert.

![Um Ihre SIEM-Agent zu bearbeiten, wählen Sie die Auslassungspunkte, und wählen Sie dann auf Bearbeiten.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
## <a name="deleting-your-siem-agent"></a>Löschen der SIEM-Agenten

Suchen Sie die Zeile für den Agent SIEM, um Ihre SIEM-Agent in der Tabelle zu löschen. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann auf **Löschen**.

![Um einen Agent SIEM zu löschen, wählen Sie die Auslassungspunkte, und wählen Sie dann auf Löschen.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

## <a name="sample-logfiles"></a>Beispiel-Protokolldateien

Es folgt ein Beispiel der Alerts-Protokolldatei, die auf einen Server SIEM gesendet werden können:

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

Und es folgt ein Beispiel im CEF-format


|Name des Felds CEF  | Beschreibung  |
|---------|---------|
|Starten     | Warnung Zeitstempel        |
|Ende     | Warnung Zeitstempel        |
|RT     | Warnung Zeitstempel        |
|msg     | Warnen Sie Beschreibung, wie in der Cloud App Sicherheit in Office 365-Portal dargestellt        |
|suser     | Warnung Betreff Benutzer        |
|destinationServiceName     | Benachrichtigung, die app, wie Office 365, SharePoint oder OneDrive stammen        |
|csLabel     | Variiert (Etiketten müssen verschiedene Bedeutungen). In der Regel werden die Beschriftungen selbsterklärend, wie TargetObjects.        |
|cs     | Informationen, die ein Label (beispielsweise die Zielbenutzer einer Warnung gemäß den Anweisungen in das Label-Beispiel)        |
  
## <a name="next-steps"></a>Nächste Schritte

- [Auslastung Aktivitäten nach der Einführung der Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    
- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)
    


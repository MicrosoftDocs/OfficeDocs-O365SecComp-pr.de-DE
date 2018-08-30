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
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="076aa-104">Integrieren von Ihrem Server SIEM mit Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="076aa-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="076aa-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="076aa-105">****Evaluation** \>**</span></span>|<span data-ttu-id="076aa-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="076aa-106">****Planning** \>**</span></span>|<span data-ttu-id="076aa-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="076aa-107">****Deployment** \>**</span></span>|<span data-ttu-id="076aa-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="076aa-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="076aa-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="076aa-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="076aa-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="076aa-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="076aa-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="076aa-111">You are here!</span></span>  <br/> [<span data-ttu-id="076aa-112">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="076aa-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="076aa-113">Starten Sie die Nutzung</span><span class="sxs-lookup"><span data-stu-id="076aa-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="076aa-p102">Sie können die [Office 365-Cloud-App-Sicherheit](get-ready-for-office-365-cas.md) mit der Sicherheit und Ereignissen (SIEM) Verwaltungsserver zum Aktivieren der zentralisierten Überwachung von Warnungen integrieren. Dies ist besonders wichtig für Organisationen, die mithilfe von Clouddiensten und lokale serveranwendungen. Integrieren von in einem SIEM Server kann Ihr Sicherheitsteam besser schützen Ihrer Office 365-Applikationen Beibehaltung des Workflows üblichen Sicherheit durch Automatisierung bestimmte Sicherheitsverfahren und Korrelation zwischen cloudbasierten und lokale Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="076aa-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="076aa-p103">Wenn Sie zunächst den Server SIEM mit Office 365-Cloud-App-Sicherheit integrieren, werden Warnungen aus den letzten zwei Tagen die SIEM-Server als auch alle Benachrichtigungen aus dann auf weitergeleitet (basierend auf alle Filter, die Sie auswählen). Wenn Sie dieses Feature für einen längeren Zeitraum, deaktivieren, wenn Sie es erneut aktivieren, wird es die letzten zwei Tagen von Benachrichtigungen und klicken Sie dann alle Benachrichtigungen für anschließend weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="076aa-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>
 
## <a name="siem-integration-architecture"></a><span data-ttu-id="076aa-119">Architektur für die Integration von SIEM</span><span class="sxs-lookup"><span data-stu-id="076aa-119">SIEM integration architecture</span></span>

<span data-ttu-id="076aa-p104">Ein Agent SIEM ist im Netzwerk der Organisation eingerichtet. Wenn bereitgestellt und konfiguriert ist, ruft der SIEM-Agent die Datentypen, die konfiguriert wurden (Benachrichtigungen) mithilfe von Office 365 Cloud App Sicherheit Rest-APIs. Der Datenverkehr wird dann über einen verschlüsselten HTTPS-Kanal an Port 443 gesendet.</span><span class="sxs-lookup"><span data-stu-id="076aa-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="076aa-123">Wenn ein SIEM-Agent Daten aus Office 365-Cloud-App-Sicherheit abruft, sendet er die Syslog-Nachrichten zum lokalen SIEM-Server mit der Netzwerkkonfigurationen, die während des Setups (TCP oder UDP mit einem benutzerdefinierten Port) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="076aa-123">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Architektur SIEM und Cloud App-Sicherheit](media/siem-architecture.png)

## <a name="supported-siem-servers"></a><span data-ttu-id="076aa-125">Unterstützte SIEM-Server</span><span class="sxs-lookup"><span data-stu-id="076aa-125">Supported SIEM servers</span></span>

<span data-ttu-id="076aa-126">Office 365-Cloud-App-Sicherheit unterstützt derzeit die folgenden SIEM-Server:</span><span class="sxs-lookup"><span data-stu-id="076aa-126">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="076aa-127">Micro Fokus ArcSight</span><span class="sxs-lookup"><span data-stu-id="076aa-127">Micro Focus ArcSight</span></span>
- <span data-ttu-id="076aa-128">Generische CEF</span><span class="sxs-lookup"><span data-stu-id="076aa-128">Generic CEF</span></span>

## <a name="prerequisites"></a><span data-ttu-id="076aa-129">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="076aa-129">Prerequisites</span></span>

- <span data-ttu-id="076aa-p105">Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Aufgaben in diesem Artikel beschrieben werden. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="076aa-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="076aa-132">Sie müssen [Office 365-Cloud-App-Sicherheit aktiviert](turn-on-office-365-cas.md) für Ihre Organisation verfügen.</span><span class="sxs-lookup"><span data-stu-id="076aa-132">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="076aa-133">[Protokollierung](turn-audit-log-search-on-or-off.md) muss für Office 365 aktiviert werden</span><span class="sxs-lookup"><span data-stu-id="076aa-133">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="076aa-134">Sie müssen einen standard-Server sein, der zum Konfigurieren der Integration von SIEM Server die folgenden Anforderungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="076aa-134">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="076aa-135">Betriebssystem: Windows oder Linux (Dies kann einen virtuellen Computer sein)</span><span class="sxs-lookup"><span data-stu-id="076aa-135">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="076aa-136">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="076aa-136">CPU: 2</span></span>
    - <span data-ttu-id="076aa-137">Festplattenspeicher: 20 GB</span><span class="sxs-lookup"><span data-stu-id="076aa-137">Disk space: 20 GB</span></span>
    - <span data-ttu-id="076aa-138">RAM: 2 GB</span><span class="sxs-lookup"><span data-stu-id="076aa-138">RAM: 2 GB</span></span>
    - <span data-ttu-id="076aa-139">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installiert</span><span class="sxs-lookup"><span data-stu-id="076aa-139">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="076aa-140">Firewall gemäß der Beschreibung in [netzwerkanforderungen](https://docs.microsoft.com/cloud-app-security/network-requirements) konfiguriert</span><span class="sxs-lookup"><span data-stu-id="076aa-140">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="076aa-p106">Benötigen Sie Details zu Ihren **Remote Syslog Host** und **Syslot Portnummer**ein. Netzwerkadministrator oder Sicherheitsadministrator sollten Sie finden diese Informationen helfen können.</span><span class="sxs-lookup"><span data-stu-id="076aa-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="076aa-143">Sie müssen die [JAR-Datei](https://go.microsoft.com/fwlink/?linkid=838596) herunterladen, Sie Ihre Server SIEM integriert müssen, [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="076aa-143">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="integrate-office-365-cloud-app-security"></a><span data-ttu-id="076aa-144">Integrieren von Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="076aa-144">Integrate Office 365 Cloud App Security</span></span>
    
### <a name="step-1-set-it-up-in-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="076aa-145">Schritt 1: Richten Sie es in die Cloud App Sicherheit in Office 365-Portal ein</span><span class="sxs-lookup"><span data-stu-id="076aa-145">Step 1: Set it up in the Office 365 Cloud App Security portal</span></span>

1. <span data-ttu-id="076aa-p107">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="076aa-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="076aa-148">Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="076aa-148">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="076aa-p108">Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="076aa-p108">Choose **Go to Office 365 Cloud App Security**. </span></span></br>
    <span data-ttu-id="076aa-150">![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-150">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="076aa-151">Klicken Sie auf **Einstellungen** \> **Security Extensions**.</span><span class="sxs-lookup"><span data-stu-id="076aa-151">Click **Settings** \> **Security extensions**.</span></span></br>
<span data-ttu-id="076aa-152">![Wählen Sie Einstellungen > Sicherheit Erweiterungen](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-152">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

5. <span data-ttu-id="076aa-153">Wählen Sie **Agent SIEM hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="076aa-153">Choose **Add SIEM agent**.</span></span></br><span data-ttu-id="076aa-154">![Wählen Sie Agent SIEM hinzufügen.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-154">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
6. <span data-ttu-id="076aa-155">Wählen Sie auf **Assistenten starten**.</span><span class="sxs-lookup"><span data-stu-id="076aa-155">Choose **Start wizard**.</span></span></br><span data-ttu-id="076aa-156">![Holen Sie sich Hilfe, oder starten Sie den Assistenten](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-156">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
7. <span data-ttu-id="076aa-p109">Geben Sie im **allgemeinen** Schritt einen Namen, und **Wählen Sie Ihre SIEM-Format aus** , und legen Sie eine beliebige **Erweiterte Einstellungen** , die für dieses Format relevant sind. Wählen Sie dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="076aa-p109">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span></br><span data-ttu-id="076aa-159">![Geben Sie einen Namen und Typ](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-159">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
8. <span data-ttu-id="076aa-p110">Geben Sie im Schritt **Remote Syslog** die IP-Adresse oder den Hostnamen der **Remote Syslog Host** und die **Portnummer Syslog**. Wählen Sie TCP oder UDP als Protokoll Remote Syslog. (Sie können arbeiten mit Ihrem Netzwerkadministrator oder Sicherheitsadministrator, um diese Informationen zu erhalten, wenn sie Ihnen keine.) Wählen Sie dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="076aa-p110">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span></br><span data-ttu-id="076aa-163">![Geben Sie Remote Syslog-details](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-163">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
9. <span data-ttu-id="076aa-164">Im Schritt **Datentypen** einen der folgenden Schritte aus, und klicken Sie dann auf **Weiter**:</span><span class="sxs-lookup"><span data-stu-id="076aa-164">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="076aa-165">Behalten Sie die Standardeinstellung **Alle Warnungen**</span><span class="sxs-lookup"><span data-stu-id="076aa-165">Keep the default setting of **All Alerts**</span></span></br><span data-ttu-id="076aa-166">OR</span><span class="sxs-lookup"><span data-stu-id="076aa-166">OR</span></span>
    - <span data-ttu-id="076aa-p111">Klicken Sie auf **Alle Benachrichtigungen**, und wählen Sie dann auf **bestimmten Filter**. Definieren Sie Filter an, um die Arten von Benachrichtigungen wählen Sie auf Ihrem Server SIEM senden möchten.</span><span class="sxs-lookup"><span data-stu-id="076aa-p111">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span></br><span data-ttu-id="076aa-169">![Datentypen Schritt des Assistenten](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-169">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
10. <span data-ttu-id="076aa-170">Klicken Sie auf dem Bildschirm Herzlichen Glückwunsch kopieren Sie das Token, und speichern Sie sie zur späteren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="076aa-170">On the Congratulations screen, copy the token and save it for later.</span></span></br>![SIEM Agent erstellt Bildschirm](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="076aa-p112">Zu diesem Zeitpunkt eine SIEM-Agenten in Office 365-Cloud-App-Sicherheit eingerichtet haben, aber Ihre SIEM-Server-Integration ist noch nicht abgeschlossen. Fahren Sie fort mit dem nächsten Schritt fort Ihrer SIEM-Server-Integration.</span><span class="sxs-lookup"><span data-stu-id="076aa-p112">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="076aa-p113">Nachdem Sie klicken Sie auf Schließen, und klicken Sie im Assistenten auf dem Bildschirm des Security Extensions lassen, sehen Sie den Agent SIEM, die, den Sie in der Tabelle hinzugefügt. Es wird weist den Status **erstellt** , bis es später verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="076aa-p113">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![SIEM Agent erstellt](media/SIEMAgentCreated.png)
    
### <a name="step-2-download-the-jar-file-and-run-it-on-your-server"></a><span data-ttu-id="076aa-177">Schritt 2: Laden Sie die JAR-Datei, und führen Sie es auf dem server</span><span class="sxs-lookup"><span data-stu-id="076aa-177">Step 2: Download the JAR file and run it on your server</span></span>

1. <span data-ttu-id="076aa-p114">Laden Sie das [Microsoft Cloud App-SIEM-Sicherheitsmonitor](https://go.microsoft.com/fwlink/?linkid=838596) , und Entzippen Sie den Ordner. (Sie müssen [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) zustimmen, um fortzufahren.)</span><span class="sxs-lookup"><span data-stu-id="076aa-p114">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="076aa-180">Extrahieren Sie die JAR-Datei aus der ZIP-Ordner, und führen sie auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="076aa-180">Extract the .jar file from the zipped folder and run it on your server.</span></span>
    
3. <span data-ttu-id="076aa-181">Nach der Ausführung der Datei, führen Sie den folgenden aus: Befehl:</span><span class="sxs-lookup"><span data-stu-id="076aa-181">After running the file, run the following: command:</span></span></br>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
#### <a name="important-notes"></a><span data-ttu-id="076aa-182">Wichtige Hinweise:</span><span class="sxs-lookup"><span data-stu-id="076aa-182">Important notes</span></span>

- <span data-ttu-id="076aa-183">Der Dateiname kann je nach der Version des Agents SIEM variieren.</span><span class="sxs-lookup"><span data-stu-id="076aa-183">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="076aa-184">Es wird empfohlen, dass Sie die JAR-Füllung auf dem Server, während der Serverinstallation ausführen.</span><span class="sxs-lookup"><span data-stu-id="076aa-184">We recommend that you run the JAR fill on your server during server setup.</span></span>
    - <span data-ttu-id="076aa-185">**Windows**: Führen Sie als geplante Aufgabe, und stellen Sie sicher, zum Konfigurieren der Task **ausgeführt wird, ob der Benutzer oder nicht angemeldet ist** , und deaktivieren Sie die Option **Task beenden, wenn er länger als ausgeführt wird** .</span><span class="sxs-lookup"><span data-stu-id="076aa-185">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="076aa-186">**Linux**: Hinzufügen des Befehls Ausführen mit einer **&** an die `rc.local` Datei.</span><span class="sxs-lookup"><span data-stu-id="076aa-186">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> </br><span data-ttu-id="076aa-187">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="076aa-187">Example:</span></span></br> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="076aa-p115">Parameter in Klammern [] sind optional und sollte verwendet werden, falls relevant. Verwenden Sie die folgenden Variablen:</span><span class="sxs-lookup"><span data-stu-id="076aa-p115">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>
    - <span data-ttu-id="076aa-190">**DIRNAME** ist der Pfad zu dem Verzeichnis, den, das Sie für den lokalen Agent Debugprotokolle verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="076aa-190">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>
    - <span data-ttu-id="076aa-191">**Adresse [: PORT]** Proxy-Server-Adresse und Port, die der Server für die Verbindung mit dem Internet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="076aa-191">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>
    - <span data-ttu-id="076aa-192">**TOKEN** ist das SIEM-Agent-Token, die, das Sie in der ersten Prozedur kopiert.</span><span class="sxs-lookup"><span data-stu-id="076aa-192">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>
    - <span data-ttu-id="076aa-193">Um Hilfe zu erhalten, geben Sie ein `-h`.</span><span class="sxs-lookup"><span data-stu-id="076aa-193">To get help, type `-h`.</span></span> 
  
### <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="076aa-194">Schritt 3: Überprüfen Sie, ob der Agent SIEM funktionsfähig ist</span><span class="sxs-lookup"><span data-stu-id="076aa-194">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="076aa-195">Stellen Sie sicher, dass der Status des SIEM-Agents in der Cloud App Sicherheit in Office 365-Portal wird nicht als **Verbindungsfehler** angezeigt oder **getrennt** und, es sind keine Benachrichtigungen Agent.</span><span class="sxs-lookup"><span data-stu-id="076aa-195">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span></br><span data-ttu-id="076aa-196">Beispielsweise sehen hier Sie, dass der Server SIEM verbunden ist:</span><span class="sxs-lookup"><span data-stu-id="076aa-196">For example, here we can see the SIEM server is connected:</span></span></br><span data-ttu-id="076aa-197">![SIEM Server verbunden](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-197">![SIEM server connected](media/siem-connected.png)</span></span></br><span data-ttu-id="076aa-198">Und Hier können wir sehen, dass der SIEM getrennt ist:</span><span class="sxs-lookup"><span data-stu-id="076aa-198">And here, we can see the SIEM server is disconnected:</span></span></br><span data-ttu-id="076aa-199">![SIEM Server nicht verbunden](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="076aa-199">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="076aa-200">Stellen Sie in Ihrem Server Syslog/SIEM sicher, dass Sie sehen, dass Benachrichtigungen von Sicherheit in Office 365 Cloud App angekommen sind.</span><span class="sxs-lookup"><span data-stu-id="076aa-200">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="regenerating-your-token"></a><span data-ttu-id="076aa-201">Erneutes Generieren des Tokens</span><span class="sxs-lookup"><span data-stu-id="076aa-201">Regenerating your token</span></span>

<span data-ttu-id="076aa-p116">Wenn Sie Ihr Token verlieren, können Sie sie wiederherstellen. Suchen Sie in der Tabelle die Zeile für den SIEM-Agent. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann **erneut generieren Token**.</span><span class="sxs-lookup"><span data-stu-id="076aa-p116">If you lose your token, you can always regenerate it. In the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Regenerate token**.</span></span>

![Generieren Sie ein Token durch Klicken auf die Schaltfläche mit den Auslassungszeichen für Ihre SIEM-Agent neu](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
## <a name="editing-your-siem-agent"></a><span data-ttu-id="076aa-206">Bearbeiten des SIEM-Agents</span><span class="sxs-lookup"><span data-stu-id="076aa-206">Editing your SIEM agent</span></span>

<span data-ttu-id="076aa-p117">Suchen Sie die Zeile für den Agent SIEM, um Ihre SIEM-Agent in der Tabelle zu bearbeiten. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann auf **Bearbeiten**. Wenn Sie den Agent SIEM bearbeiten, müssen Sie nicht die JAR-Datei erneut ausführen; automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="076aa-p117">To edit your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Edit**. If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.</span></span>

![Um Ihre SIEM-Agent zu bearbeiten, wählen Sie die Auslassungspunkte, und wählen Sie dann auf Bearbeiten.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
## <a name="deleting-your-siem-agent"></a><span data-ttu-id="076aa-211">Löschen der SIEM-Agenten</span><span class="sxs-lookup"><span data-stu-id="076aa-211">Deleting your SIEM agent</span></span>

<span data-ttu-id="076aa-p118">Suchen Sie die Zeile für den Agent SIEM, um Ihre SIEM-Agent in der Tabelle zu löschen. Klicken Sie auf die Auslassungspunkte, und wählen Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="076aa-p118">To delete your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Delete**.</span></span>

![Um einen Agent SIEM zu löschen, wählen Sie die Auslassungspunkte, und wählen Sie dann auf Löschen.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

## <a name="sample-logfiles"></a><span data-ttu-id="076aa-215">Beispiel-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="076aa-215">Sample logfiles</span></span>

<span data-ttu-id="076aa-216">Es folgt ein Beispiel der Alerts-Protokolldatei, die auf einen Server SIEM gesendet werden können:</span><span class="sxs-lookup"><span data-stu-id="076aa-216">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="076aa-217">Und es folgt ein Beispiel im CEF-format</span><span class="sxs-lookup"><span data-stu-id="076aa-217">And here's a sample in CEF format</span></span>


|<span data-ttu-id="076aa-218">Name des Felds CEF</span><span class="sxs-lookup"><span data-stu-id="076aa-218">CEF field name</span></span>  | <span data-ttu-id="076aa-219">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="076aa-219">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="076aa-220">Starten</span><span class="sxs-lookup"><span data-stu-id="076aa-220">start</span></span>     | <span data-ttu-id="076aa-221">Warnung Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="076aa-221">alert timestamp</span></span>        |
|<span data-ttu-id="076aa-222">Ende</span><span class="sxs-lookup"><span data-stu-id="076aa-222">end</span></span>     | <span data-ttu-id="076aa-223">Warnung Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="076aa-223">alert timestamp</span></span>        |
|<span data-ttu-id="076aa-224">RT</span><span class="sxs-lookup"><span data-stu-id="076aa-224">rt</span></span>     | <span data-ttu-id="076aa-225">Warnung Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="076aa-225">alert timestamp</span></span>        |
|<span data-ttu-id="076aa-226">msg</span><span class="sxs-lookup"><span data-stu-id="076aa-226">msg</span></span>     | <span data-ttu-id="076aa-227">Warnen Sie Beschreibung, wie in der Cloud App Sicherheit in Office 365-Portal dargestellt</span><span class="sxs-lookup"><span data-stu-id="076aa-227">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="076aa-228">suser</span><span class="sxs-lookup"><span data-stu-id="076aa-228">suser</span></span>     | <span data-ttu-id="076aa-229">Warnung Betreff Benutzer</span><span class="sxs-lookup"><span data-stu-id="076aa-229">alert subject user</span></span>        |
|<span data-ttu-id="076aa-230">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="076aa-230">destinationServiceName</span></span>     | <span data-ttu-id="076aa-231">Benachrichtigung, die app, wie Office 365, SharePoint oder OneDrive stammen</span><span class="sxs-lookup"><span data-stu-id="076aa-231">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="076aa-232">csLabel</span><span class="sxs-lookup"><span data-stu-id="076aa-232">csLabel</span></span>     | <span data-ttu-id="076aa-p119">Variiert (Etiketten müssen verschiedene Bedeutungen). In der Regel werden die Beschriftungen selbsterklärend, wie TargetObjects.</span><span class="sxs-lookup"><span data-stu-id="076aa-p119">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="076aa-235">cs</span><span class="sxs-lookup"><span data-stu-id="076aa-235">cs</span></span>     | <span data-ttu-id="076aa-236">Informationen, die ein Label (beispielsweise die Zielbenutzer einer Warnung gemäß den Anweisungen in das Label-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="076aa-236">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |
  
## <a name="next-steps"></a><span data-ttu-id="076aa-237">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="076aa-237">Next steps</span></span>

- [<span data-ttu-id="076aa-238">Auslastung Aktivitäten nach der Einführung der Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="076aa-238">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="076aa-239">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="076aa-239">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="076aa-240">Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="076aa-240">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    


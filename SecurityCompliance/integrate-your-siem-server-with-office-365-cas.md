---
title: Integrieren Ihres SIEM-Servers in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Sie können Ihren SIEM-Server mit Office 365 Cloud App Security integrieren. Lesen Sie diesen Artikel, um sich einen Überblick über die Funktionsweise und die Einrichtung zu verschaffen.
ms.openlocfilehash: b4baeda3cb836c0b1aa528d29176bbf4321d1fe2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215875"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="3bed2-104">Integrieren Ihres SIEM-Servers in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3bed2-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="3bed2-105">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3bed2-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="3bed2-106">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3bed2-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="3bed2-107">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3bed2-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="3bed2-108">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="3bed2-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="3bed2-109">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="3bed2-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="3bed2-110">Planung starten</span><span class="sxs-lookup"><span data-stu-id="3bed2-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="3bed2-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="3bed2-111">You are here!</span></span>  <br/> [<span data-ttu-id="3bed2-112">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="3bed2-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="3bed2-113">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="3bed2-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="3bed2-114">Übersicht und Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3bed2-114">Overview and prerequisites</span></span>

<span data-ttu-id="3bed2-p102">Sie können [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) in ihren Security Information and Event Management (SIEM)-Server integrieren, um eine zentralisierte Überwachung von Warnungen zu ermöglichen. Dies gilt insbesondere für Organisationen, die Cloud-Dienste und lokale Serveranwendungen verwenden. Die Integration mit einem SIEM-Server ermöglicht es Ihrem Sicherheitsteam, Ihre Office 365-Anwendungen besser zu schützen und gleichzeitig ihren üblichen Sicherheits Workflow beizubehalten, indem Sie bestimmte Sicherheitsverfahren automatisieren und zwischen Cloud-basierten und lokalen Ereignissen korrelieren.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="3bed2-p103">Wenn Sie Ihren SIEM-Server zunächst mit der Office 365 Cloud App-Sicherheit integrieren, werden Warnungen der letzten beiden Tage an den SIEM-Server und alle Warnungen von dann an weitergeleitet (basierend auf den von Ihnen ausgewählten Filtern). Wenn Sie dieses Feature über einen längeren Zeitraum hinweg deaktivieren, werden Sie darüber hinaus die letzten zwei Tage mit Warnungen und dann alle Benachrichtigungen weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="3bed2-120">SIEM-Integrationsarchitektur</span><span class="sxs-lookup"><span data-stu-id="3bed2-120">SIEM integration architecture</span></span>

<span data-ttu-id="3bed2-p104">Ein SIEM-Agent ist im Netzwerk Ihrer Organisation eingerichtet. Bei der Bereitstellung und Konfiguration zieht der SIEM-Agent die konfigurierten Datentypen (Warnungen) mithilfe von Office 365 Cloud App Security RESTFUL-APIs. Der Datenverkehr wird dann über einen verschlüsselten HTTPS-Kanal an der Schnittstelle 443 gesendet.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="3bed2-124">Wenn ein SIEM-Agent Daten aus Office 365 Cloud App Security abruft, sendet er die Syslog-Nachrichten mithilfe der Netzwerkkonfigurationen, die während des Setups bereitgestellt werden (TCP oder UDP mit einem benutzerdefinierten Port).</span><span class="sxs-lookup"><span data-stu-id="3bed2-124">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![SIEM-und Cloud-App-Sicherheitsarchitektur](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="3bed2-126">Unterstützte SIEM-Server</span><span class="sxs-lookup"><span data-stu-id="3bed2-126">Supported SIEM servers</span></span>

<span data-ttu-id="3bed2-127">Office 365 Cloud App Security unterstützt derzeit die folgenden SIEM-Server:</span><span class="sxs-lookup"><span data-stu-id="3bed2-127">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="3bed2-128">Micro Focus ArcSight</span><span class="sxs-lookup"><span data-stu-id="3bed2-128">Micro Focus ArcSight</span></span>
- <span data-ttu-id="3bed2-129">Generisches CEF</span><span class="sxs-lookup"><span data-stu-id="3bed2-129">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3bed2-130">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3bed2-130">Prerequisites</span></span>

- <span data-ttu-id="3bed2-p105">Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können. Weitere Informationen finden Sie unter [Permissions &amp; in the Office 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="3bed2-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="3bed2-133">Sie müssen [Office 365 Cloud App Security](turn-on-office-365-cas.md) für Ihre Organisation aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="3bed2-133">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="3bed2-134">Die [Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) muss für Office 365 aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3bed2-134">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="3bed2-135">Zum Konfigurieren der SIEM-Server Integration benötigen Sie einen Standardserver, der die folgenden Anforderungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="3bed2-135">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="3bed2-136">Betriebssystem: Windows oder Linux (Dies kann ein virtueller Computer sein)</span><span class="sxs-lookup"><span data-stu-id="3bed2-136">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="3bed2-137">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="3bed2-137">CPU: 2</span></span>
    - <span data-ttu-id="3bed2-138">Speicherplatz: 20 GB</span><span class="sxs-lookup"><span data-stu-id="3bed2-138">Disk space: 20 GB</span></span>
    - <span data-ttu-id="3bed2-139">RAM: 2 GB</span><span class="sxs-lookup"><span data-stu-id="3bed2-139">RAM: 2 GB</span></span>
    - <span data-ttu-id="3bed2-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installiert</span><span class="sxs-lookup"><span data-stu-id="3bed2-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="3bed2-141">Firewall gemäß der Beschreibung unter [Netzwerkanforderungen](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="3bed2-141">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="3bed2-p106">Sie benötigen Details zu Ihrem **Remote-syslog-Host** und zur Syslot-Portierungs **Nummer**. Ein Netzwerkadministrator oder Sicherheitsadministrator sollte Ihnen bei der Lokalisierung dieser Informationen behilflich sein.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="3bed2-144">Sie müssen den [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) zustimmen, um die [JAR-Datei](https://go.microsoft.com/fwlink/?linkid=838596) herunterzuladen, die Sie für die Integration Ihres Siem-Servers benötigen.</span><span class="sxs-lookup"><span data-stu-id="3bed2-144">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="3bed2-145">Schritt 1: Einrichten eines SIEM-Agents in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3bed2-145">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="3bed2-146">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="3bed2-146">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="3bed2-147">Klicken Sie auf **Sicherheitserweiterungen**für **Einstellungen** \> und dann auf Siem-Agents.</span><span class="sxs-lookup"><span data-stu-id="3bed2-147">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="3bed2-148">![Auswählen von Einstellungen > Sicherheitserweiterungen](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-148">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

3. <span data-ttu-id="3bed2-149">Wählen Sie **Add Siem Agent**aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-149">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="3bed2-150">![Wählen Sie Add SIEM Agent aus.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-150">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
4. <span data-ttu-id="3bed2-151">Wählen Sie **Start-Assistent**aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-151">Choose **Start wizard**.</span></span><br/><span data-ttu-id="3bed2-152">![Abrufen von Hilfe oder Starten des Assistenten](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-152">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
5. <span data-ttu-id="3bed2-p107">Geben Sie im Abschnitt **Allgemein** einen Namen ein, und **Wählen Sie Ihr Siem-Format** aus, und legen Sie alle für dieses Format relevanten **erweiterten Einstellungen** fest. Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p107">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="3bed2-155">![Angeben eines Namens und Typs](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-155">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
6. <span data-ttu-id="3bed2-p108">Geben Sie im **Remote-syslog** -Schritt die IP-Adresse oder den Hostnamen des Remote-syslog- **Hosts** und die syslog- **Portierungs Nummer**an. Wählen Sie TCP oder UDP als Remote-syslog-Protokoll aus. (Sie können mit Ihrem Netzwerkadministrator oder Sicherheitsadministrator zusammenarbeiten, um diese Details zu erhalten, wenn Sie diese nicht haben.) Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p108">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="3bed2-159">![Angeben von Remote-syslog-Details](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-159">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
7. <span data-ttu-id="3bed2-160">Führen Sie im Schritt **Datentypen** einen der folgenden Schritte aus, und klicken Sie dann auf **weiter**:</span><span class="sxs-lookup"><span data-stu-id="3bed2-160">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="3bed2-161">Standardeinstellung **aller Warnungen** beibehalten</span><span class="sxs-lookup"><span data-stu-id="3bed2-161">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="3bed2-162">ODER</span><span class="sxs-lookup"><span data-stu-id="3bed2-162">OR</span></span>
    - <span data-ttu-id="3bed2-p109">Klicken Sie auf **alle Warnungen**, und wählen Sie dann **bestimmte Filter**aus. Definieren Sie Filter, um die Arten von Warnungen auszuwählen, die Sie an Ihren SIEM-Server senden möchten.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p109">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="3bed2-165">![Datentypen Schritt des Assistenten](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-165">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
8. <span data-ttu-id="3bed2-166">Kopieren Sie auf dem Bildschirm Glückwünsche das Token, und speichern Sie es für später.</span><span class="sxs-lookup"><span data-stu-id="3bed2-166">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![SIEM-Agent erstellter Bildschirm](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="3bed2-p110">Zu diesem Zeitpunkt haben Sie einen SIEM-Agent in Office 365 Cloud App Security eingerichtet, aber ihre SIEM-Server Integration ist noch nicht abgeschlossen. Fahren Sie mit dem nächsten Schritt fort, um Ihre SIEM-Server Integration weiterzuführen.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p110">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="3bed2-p111">Nachdem Sie auf Schließen und den Assistenten verlassen haben, können Sie auf dem Bildschirm Sicherheitserweiterungen den SIEM-Agent sehen, den Sie in der Tabelle hinzugefügt haben. Er zeigt den Status **erstellt** an, bis er später verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p111">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![SIEM-Agent erstellt](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="3bed2-173">Schritt 2: Herunterladen einer JAR-Datei und ausführen auf Ihrem SIEM-Server</span><span class="sxs-lookup"><span data-stu-id="3bed2-173">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="3bed2-p112">Laden Sie den [Microsoft Cloud App Security Siem-Agent](https://go.microsoft.com/fwlink/?linkid=838596) herunter, und entpacken Sie den Ordner. (Sie müssen den [Software-Lizenzbedingungen](https://go.microsoft.com/fwlink/?linkid=862491) zustimmen, um fortzufahren.)</span><span class="sxs-lookup"><span data-stu-id="3bed2-p112">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="3bed2-176">Extrahieren Sie die JAR-Datei aus dem gezippten Ordner, und führen Sie Sie auf Ihrem SIEM-Server aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-176">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="3bed2-177">Führen Sie nach dem Ausführen der Datei den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="3bed2-177">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="3bed2-178">Wichtige Hinweise:</span><span class="sxs-lookup"><span data-stu-id="3bed2-178">Important notes</span></span>

- <span data-ttu-id="3bed2-179">Der Dateiname kann je nach der Version des SIEM-Agents unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="3bed2-179">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="3bed2-180">Es wird empfohlen, dass Sie die JAR-Datei auf Ihrem SIEM-Server während des Server Setups ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bed2-180">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="3bed2-181">**Windows**: Ausführen als geplante Aufgabe, indem Sie sicherstellen, dass Sie die Aufgabe so konfigurieren, dass Sie **ausgeführt wird, unabhängig davon, ob der Benutzer angemeldet ist** , und die **Aufgabe beenden, wenn Sie länger als Option ausgeführt** wird.</span><span class="sxs-lookup"><span data-stu-id="3bed2-181">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="3bed2-182">**Linux**: Fügen Sie den Befehl ausführen mit **&** der `rc.local` Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bed2-182">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="3bed2-183">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3bed2-183">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="3bed2-p113">Parameter in eckigen Klammern [] sind optional und sollten nur verwendet werden, wenn relevant. Verwenden Sie die folgenden Variablen:</span><span class="sxs-lookup"><span data-stu-id="3bed2-p113">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>

    - <span data-ttu-id="3bed2-186">**Dirname** ist der Pfad zu dem Verzeichnis, das Sie für lokale Agent-Debug-Protokolle verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3bed2-186">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="3bed2-187">**Address [:P Ort]** ist die Proxyserveradresse und-Portierung, die der Server für die Verbindung mit dem Internet verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bed2-187">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="3bed2-188">**Token** ist das Siem-Agent-Token, das Sie im ersten Verfahren kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="3bed2-188">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="3bed2-189">Um Hilfe zu erhalten, `-h`geben Sie.</span><span class="sxs-lookup"><span data-stu-id="3bed2-189">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="3bed2-190">Schritt 3: überPrüfen, ob der SIEM-Agent funktioniert</span><span class="sxs-lookup"><span data-stu-id="3bed2-190">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="3bed2-191">Stellen Sie sicher, dass der Status des SIEM-Agents im Sicherheitsportal der Office 365 Cloud-APP nicht als **Verbindungsfehler** angezeigt wird und keine Agent-Benachrichtigungen vorhanden sind. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3bed2-191">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="3bed2-192">Beispielsweise können wir hier sehen, ob der SIEM-Server verbunden ist:</span><span class="sxs-lookup"><span data-stu-id="3bed2-192">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="3bed2-193">![SIEM-Server verbunden](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-193">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="3bed2-194">Und hier sehen wir, dass der SIEM-Server getrennt ist:</span><span class="sxs-lookup"><span data-stu-id="3bed2-194">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="3bed2-195">![SIEM-Server nicht verbunden](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-195">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="3bed2-196">Stellen Sie sicher, dass in Ihrem syslog/SIEM-Server Warnungen aus Office 365 Cloud App Security angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3bed2-196">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="3bed2-197">Wie die Logfiles aussehen</span><span class="sxs-lookup"><span data-stu-id="3bed2-197">What the logfiles look like</span></span>

<span data-ttu-id="3bed2-198">Es folgt ein Beispiel für Warnungs-Logfiles, die an einen SIEM-Server gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="3bed2-198">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="3bed2-199">Und hier ein weiteres Beispiel, diesmal im CEF-Format:</span><span class="sxs-lookup"><span data-stu-id="3bed2-199">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="3bed2-200">CEF-Feldname</span><span class="sxs-lookup"><span data-stu-id="3bed2-200">CEF field name</span></span>  | <span data-ttu-id="3bed2-201">Description</span><span class="sxs-lookup"><span data-stu-id="3bed2-201">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="3bed2-202">Start</span><span class="sxs-lookup"><span data-stu-id="3bed2-202">start</span></span>     | <span data-ttu-id="3bed2-203">Warnungszeit Stempel</span><span class="sxs-lookup"><span data-stu-id="3bed2-203">alert timestamp</span></span>        |
|<span data-ttu-id="3bed2-204">Ende</span><span class="sxs-lookup"><span data-stu-id="3bed2-204">end</span></span>     | <span data-ttu-id="3bed2-205">Warnungszeit Stempel</span><span class="sxs-lookup"><span data-stu-id="3bed2-205">alert timestamp</span></span>        |
|<span data-ttu-id="3bed2-206">RT</span><span class="sxs-lookup"><span data-stu-id="3bed2-206">rt</span></span>     | <span data-ttu-id="3bed2-207">Warnungszeit Stempel</span><span class="sxs-lookup"><span data-stu-id="3bed2-207">alert timestamp</span></span>        |
|<span data-ttu-id="3bed2-208">msg</span><span class="sxs-lookup"><span data-stu-id="3bed2-208">msg</span></span>     | <span data-ttu-id="3bed2-209">Warnungsbeschreibung im Office 365 Cloud App Security Portal</span><span class="sxs-lookup"><span data-stu-id="3bed2-209">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="3bed2-210">suser</span><span class="sxs-lookup"><span data-stu-id="3bed2-210">suser</span></span>     | <span data-ttu-id="3bed2-211">Warnungs Betreff-Benutzer</span><span class="sxs-lookup"><span data-stu-id="3bed2-211">alert subject user</span></span>        |
|<span data-ttu-id="3bed2-212">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="3bed2-212">destinationServiceName</span></span>     | <span data-ttu-id="3bed2-213">Warnungs Absender-APP, wie Office 365, SharePoint oder OneDrive</span><span class="sxs-lookup"><span data-stu-id="3bed2-213">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="3bed2-214">csLabel</span><span class="sxs-lookup"><span data-stu-id="3bed2-214">csLabel</span></span>     | <span data-ttu-id="3bed2-p114">Variiert (Bezeichnungen haben unterschiedliche Bedeutungen). Beschriftungen sind in der Regel selbsterklärend, wie targetObjects.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p114">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="3bed2-217">cs</span><span class="sxs-lookup"><span data-stu-id="3bed2-217">cs</span></span>     | <span data-ttu-id="3bed2-218">Informationen, die einer Bezeichnung entsprechen (beispielsweise der Zielbenutzer einer Warnung gemäß dem Bezeichnungs Beispiel)</span><span class="sxs-lookup"><span data-stu-id="3bed2-218">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="3bed2-219">Zusätzliche Aufgaben (je nach Bedarf)</span><span class="sxs-lookup"><span data-stu-id="3bed2-219">Additional tasks (as needed)</span></span>

<span data-ttu-id="3bed2-p115">Nachdem Sie Ihren SIEM-Server konfiguriert und mit Office 365 Cloud App Security integriert haben, müssen Sie möglicherweise ein Token erneut generieren, einen SIEM-Agent bearbeiten oder einen SIEM-Agent löschen. In den folgenden Abschnitten wird beschrieben, wie Sie diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bed2-p115">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent. The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="3bed2-222">Erneutes Generieren eines Tokens</span><span class="sxs-lookup"><span data-stu-id="3bed2-222">Regenerate a token</span></span>

<span data-ttu-id="3bed2-223">Wenn Sie Ihr Token verlieren, können Sie es erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="3bed2-223">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="3bed2-224">wählen sie im Office 365 Cloud App security portal[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() die option**sicherheitserweiterungen**für **einstellungen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-224">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="3bed2-225">Suchen Sie in der Tabelle die Zeile für den SIEM-Agent.</span><span class="sxs-lookup"><span data-stu-id="3bed2-225">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="3bed2-226">Klicken Sie auf die Ellipsen, und wählen Sie dann **Token erneut generieren**aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-226">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="3bed2-227">![Generieren Sie ein Token erneut, indem Sie auf die Auslassungspunkte für Ihren SIEM-Agent klicken.](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-227">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="3bed2-228">Bearbeiten eines SIEM-Agents</span><span class="sxs-lookup"><span data-stu-id="3bed2-228">Edit a SIEM agent</span></span>

1. <span data-ttu-id="3bed2-229">wählen sie im Office 365 Cloud App security portal[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() die option**sicherheitserweiterungen**für **einstellungen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-229">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="3bed2-230">Suchen Sie die Zeile für den SIEM-Agent.</span><span class="sxs-lookup"><span data-stu-id="3bed2-230">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="3bed2-p116">Klicken Sie auf die Ellipsen, und wählen Sie dann **Bearbeiten**aus. (Wenn Sie den SIEM-Agent bearbeiten, müssen Sie die JAR-Datei nicht erneut ausführen; Sie wird automatisch aktualisiert.)</span><span class="sxs-lookup"><span data-stu-id="3bed2-p116">Click the ellipses, and then choose **Edit**. (If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.) </span></span><br/><span data-ttu-id="3bed2-233">![Um Ihren SIEM-Agent zu bearbeiten, wählen Sie die Ellipsen aus und klicken dann auf Bearbeiten.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-233">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="3bed2-234">Löschen eines SIEM-Agents</span><span class="sxs-lookup"><span data-stu-id="3bed2-234">Delete a SIEM agent</span></span>

1. <span data-ttu-id="3bed2-235">wählen sie im Office 365 Cloud App security portal[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() die option**sicherheitserweiterungen**für **einstellungen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-235">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="3bed2-236">Suchen Sie die Zeile für den SIEM-Agent.</span><span class="sxs-lookup"><span data-stu-id="3bed2-236">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="3bed2-237">Klicken Sie auf die Ellipsen, und wählen Sie dann **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="3bed2-237">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="3bed2-238">![Wenn Sie einen SIEM-Agent löschen möchten, wählen Sie die Ellipse aus, und wählen Sie dann löschen aus.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="3bed2-238">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="3bed2-239">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3bed2-239">Next steps</span></span>

- [<span data-ttu-id="3bed2-240">Nutzungsaktivitäten nach der Einführung von Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3bed2-240">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="3bed2-241">Überarbeiten und Aktionen für Warnungen</span><span class="sxs-lookup"><span data-stu-id="3bed2-241">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="3bed2-242">Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="3bed2-242">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    


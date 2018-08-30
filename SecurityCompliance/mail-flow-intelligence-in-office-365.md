---
title: Mail Flow Intelligence in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'Normalerweise verwenden Sie eine Verbindung zum Weiterleiten von Nachrichten aus Office 365-Organisation für Ihre lokale messaging-Umgebung. Sie können auch eine Verbindung zum Weiterleiten von Nachrichten aus Office 365 zu einer Partnerorganisation verwenden. Wenn Office 365 diese Nachrichten über den Connector können nicht übermittelt werden, sind sie Office 365 in der Warteschlange. '
ms.openlocfilehash: 4effbb783d6ba8f3b33d0aed446e031193d2f2a3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002720"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="2c9c1-105">Mail Flow Intelligence in Office 365</span><span class="sxs-lookup"><span data-stu-id="2c9c1-105">Mail flow intelligence in Office 365</span></span>
  
<span data-ttu-id="2c9c1-p102">In der Regel verwenden Sie einen Konnektor zum Weiterleiten von Nachrichten aus Ihrer Office 365-Organisation in Ihre lokale Nachrichtenumgebung. Sie können auch einen Konnektor verwenden, um Nachrichten von Office 365 zu einer Partnerorganisation weiterzuleiten. Wenn Office 365 diese Nachrichten nicht über den Konnektor senden kann, werden sie in die Office 365-Warteschlange gestellt. Office 365 versucht 48 Stunden, die Nachrichten zu senden. Nach 48 Stunden läuft die Nachricht in der Warteschlange ab, und die Nachricht wird an den ursprünglichen Absender in einem Unzustellbarkeitsbericht zurückgegeben (auch bekannt als NDR oder Unzustellbarkeitsnachricht).</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p102">Typically, you use a connector to route messages from your Office 365 organization to your on-premises messaging environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>
  
<span data-ttu-id="2c9c1-p103">Office 365 generiert einen Fehler, wenn eine Nachricht nicht mithilfe eines Konnektors gesendet werden kann. In diesem Thema werden die am häufigsten auftretenden Fehler und die dazugehörigen Lösungen beschrieben. Warteschlangen- und Benachrichtigungsfehler für unzustellbare Nachrichten, die über Konnektoren gesendet werden, sind als intelligente Nachrichtenübermittlung bekannt.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p103">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as mailflow intelligence.</span></span>
  
 <span data-ttu-id="2c9c1-114">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="2c9c1-114">**Contents**</span></span>
  
- [<span data-ttu-id="2c9c1-115">Fehlercode: 450 4.4.312 DNS-Abfragefehler</span><span class="sxs-lookup"><span data-stu-id="2c9c1-115">Error code: 450 4.4.312 DNS query failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [<span data-ttu-id="2c9c1-116">Fehlercode: 450 4.4.315 Timeout bei der Verbindung</span><span class="sxs-lookup"><span data-stu-id="2c9c1-116">Error code: 450 4.4.315 Connection timed out</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [<span data-ttu-id="2c9c1-117">Fehlercode: 450 4.4.316 Verbindung abgelehnt</span><span class="sxs-lookup"><span data-stu-id="2c9c1-117">Error code: 450 4.4.316 Connection refused</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [<span data-ttu-id="2c9c1-118">Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server</span><span class="sxs-lookup"><span data-stu-id="2c9c1-118">Error code: 450 4.4.317 Cannot connect to remote server</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [<span data-ttu-id="2c9c1-119">Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen</span><span class="sxs-lookup"><span data-stu-id="2c9c1-119">Error code: 450 4.4.318 Connection was closed abruptly</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [<span data-ttu-id="2c9c1-120">Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler</span><span class="sxs-lookup"><span data-stu-id="2c9c1-120">Error code: 450 4.7.320 Certificate validation failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="2c9c1-121">Fehlercode: 450 4.4.312 DNS-Abfragefehler</span><span class="sxs-lookup"><span data-stu-id="2c9c1-121">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="2c9c1-p104">Dieser Fehler bedeutet in der Regel, dass Office 365 versucht hat, eine Verbindung zum intelligenten Host herzustellen, der im Konnektor angegeben ist, aber die DNS-Abfrage zum Ermitteln der IP-Adressen des intelligenten Hosts ist fehlgeschlagen. Mögliche Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p104">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host IP addresses failed. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="2c9c1-124">Es gibt ein Problem mit dem DNS-Hostingdienst Ihrer Domäne (Partei, die die autoritativen Namensserver für Ihre Domäne verwaltet).</span><span class="sxs-lookup"><span data-stu-id="2c9c1-124">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>
    
- <span data-ttu-id="2c9c1-125">Ihre Domäne ist vor kurzem abgelaufen. D.h. der MX-Eintrag kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-125">Your domain has recently expired, so the MX record can't be retrieved.</span></span>
    
- <span data-ttu-id="2c9c1-126">Der MX-Eintrag Ihrer Domäne hat sich kürzlich geändert, und die Office 365-DNS-Server enthalten weiterhin zuvor zwischengespeicherte DNS-Informationen für Ihre Domäne.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-126">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>
    
<span data-ttu-id="2c9c1-127">Sie müssen das DNS-Problem beheben, indem Sie mit Ihrem DNS-Hostingdienst arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-127">You need to fix the DNS issue by working with your DNS hosting service.</span></span>
  
<span data-ttu-id="2c9c1-128">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-128">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="2c9c1-129">Fehlercode: 450 4.4.315 Timeout bei der Verbindung</span><span class="sxs-lookup"><span data-stu-id="2c9c1-129">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="2c9c1-p105">Dies bedeutet normalerweise, dass Office 365 keine Verbindung mit dem Ziel-Messagingserver herstellen kann. Die Fehlerdetails erläutern das Problem. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p105">Typically, this means Office 365 can't connect to the destination messaging server. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="2c9c1-133">Ihr lokaler Messagingserver ist ausgefallen.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-133">Your on-premises messaging server is down.</span></span>
    
- <span data-ttu-id="2c9c1-134">Es ist ein Fehler in den Einstellungen des intelligenten Hosts des Konnektors vorhanden. Office 365 versucht, ein Verbindung zur falschen IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-134">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>
    
<span data-ttu-id="2c9c1-p106">Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor. Wenn beispielsweise der Nachrichtenfluss korrekt funktioniert hat und Sie die Konnektoreinstellungen nicht geändert haben, müssen Sie in Ihrer lokalen Messagingumgebung prüfen, ob der Server ausgefallen ist oder ob Änderungen an Ihrer Netzwerkinfrastruktur vorgenommen wurden (beispielsweise Änderung der Internet-Dienstanbieter, sodass sie jetzt eine andere IP-Adresse haben).</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p106">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises messaging environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed Internet service providers, so you now have different IP addresses).</span></span>
  
<span data-ttu-id="2c9c1-137">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-137">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="2c9c1-138">Fehlercode: 450 4.4.316 Verbindung abgelehnt</span><span class="sxs-lookup"><span data-stu-id="2c9c1-138">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="2c9c1-p107">Dieser Fehler bedeutet normalerweise, dass Office 365 einen Fehler beim Versuch festgestellt hat, eine Verbindung mit dem Ziel-Messagingserver herzustellen. Eine mögliche Ursache für diesen Fehler ist, dass Ihre Firewall Verbindungen von Office 365-IP-Adressen blockiert. Dieser Fehler ist möglicherweise beabsichtigt, wenn Sie Ihr lokales Messaging-System vollständig zu Office 365 migriert haben und die lokale Messaging-Umgebung herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p107">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination messaging server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises messaging system to Office 365 and shut down your on-premises messaging environment..</span></span>
  
- <span data-ttu-id="2c9c1-p108">Wenn Ihre lokale Umgebung Postfächer aufweist, müssen Sie Ihre Firewalleinstellungen ändern, um Verbindungen von Office 365-IP-Adressen auf TCP-Port 25 zu Ihren lokalen Messagingservern zuzulassen. Eine Liste der Office 365-IP-Adressen finden Sie unter [Office 365-URLs und -IP-Adressbereiche](https://go.microsoft.com/fwlink/p/?linkid=228887).</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p108">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises messaging servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=228887).</span></span>
    
- <span data-ttu-id="2c9c1-p109">Wenn keine weiteren Nachrichten an Ihre lokale Umgebung übermittelt werden sollen, klicken Sie in der Warnung auf **Jetzt korrigieren**, damit Office 365 die Nachrichten mit ungültigen Empfängern sofort ablehnen kann. Dadurch wird das Risiko verringert, dass das Kontingent für ungültige Empfänger Ihrer Organisation überschritten wird, wodurch die normale Nachrichtenübermittlung beeinträchtigt werden könnte. Alternativ können Sie das Problem mit den folgenden Anweisungen manuell beheben:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p109">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span> 
    
  - <span data-ttu-id="2c9c1-p110">Deaktivieren oder Löschen der Verbindung von Office 365 mit der lokalen Umgebung: Office 365 Administrationscenter \> **Admin zentriert** \> **Exchange** \> **E-Mail-Fluss** \> **Connectors** \> wählen Sie die Verbindung mit dem Wert **von** **Office 365** und die **zu** **Ihrer Organisation e-Mail-Server**-Wert. Löschen Sie den Connector, indem Sie auf **Löschen**![Löschsymbol](media/ITPro-EAC-DeleteIcon.gif), oder deaktivieren Sie den Connector durch Klicken auf **Bearbeiten** ![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.gif) , und **schalten Sie ihn**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p110">Disable or delete the connector from Office 365 to your on-premises environment: Office 365 admin center \> **Admin centers** \> **Exchange** \> **Mail flow** \> **Connectors** \> select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server**. Delete the connector by clicking **Delete**![Delete icon](media/ITPro-EAC-DeleteIcon.gif), or disable the connector by clicking **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif) and unchecking **Turn it on**.</span></span>
    
  - <span data-ttu-id="2c9c1-p111">Ändern Sie die akzeptierte Domäne in Office 365, die Ihrer lokalen Nachrichtenumgebung zugeordnet ist, von **Internes Relay** in **Autorisierend**. Anweisungen finden Sie unter [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p111">Change the accepted domain in Office 365 that's associated with your on-premises messaging environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span></span>
    
    <span data-ttu-id="2c9c1-p112">**Hinweis**: in der Regel diese Änderungen werden zwischen 30 Minuten und einer Stunde wirksam wird. Nach einer Stunde stellen Sie sicher, dass die Fehlermeldung nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p112">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>
    
<span data-ttu-id="2c9c1-153">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-153">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="2c9c1-154">Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server</span><span class="sxs-lookup"><span data-stu-id="2c9c1-154">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="2c9c1-p113">Dieser Fehler bedeutet normalerweise, dass Office 365 mit dem Ziel-Messagingserver verbunden ist, aber der Server mit einem sofortigen Fehler geantwortet hat oder nicht die Verbindungsanforderungen erfüllt. Die Fehlerdetails erläutern das Problem. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p113">Typically, this error means Office 365 connected to the destination messaging server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="2c9c1-158">Der Ziel-Messagingserver hat mit dem Fehler „Dienst nicht verfügbar" geantwortet. Dies bedeutet, dass der Server nicht mit Office 365 kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-158">The destination messaging server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>
    
- <span data-ttu-id="2c9c1-159">Der Konnektor erfordert gemäß Konfiguration TLS, aber der Ziel-Messagingserver unterstützt TLS nicht.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-159">The connector is configured to require TLS, but the destination messaging server doesn't support TLS.</span></span>
    
<span data-ttu-id="2c9c1-160">Überprüfen Sie die TLS-Einstellungen und Zertifikate auf Ihren lokalen Messagingservern und die TLS-Einstellungen auf dem Konnektor.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-160">Verify the TLS settings and certificates on your on-premises messaging servers, and the TLS settings on the connector.</span></span>
  
<span data-ttu-id="2c9c1-161">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-161">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="2c9c1-162">Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen</span><span class="sxs-lookup"><span data-stu-id="2c9c1-162">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="2c9c1-p114">Dieser Fehler bedeutet normalerweise, dass Office 365 Probleme hat, mit Ihrer lokalen Messagingumgebung zu kommunizieren, sodass die Verbindung getrennt wurde. Mögliche Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p114">Typically, this error means Office 365 is having difficulty communicating with your on-premises messaging environment, so the connection was dropped. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="2c9c1-165">Ihre Firewall verwendet SMTP-Paketprüfungsregeln, und diese Regeln funktionieren nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-165">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>
    
- <span data-ttu-id="2c9c1-166">Ihr lokaler Messagingserver funktioniert nicht korrekt (Beispiele: Dienst hängt, Dienst stürzt ab oder geringe Systemressourcen), was zu einem Server-Timeout und zum Schließen der Verbindung mit Office 365 führt.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-166">Your on-premises messaging server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>
    
- <span data-ttu-id="2c9c1-p115">Es treten Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 auf. Wenn das Problem weiterhin besteht, wenden Sie sich zur Behebung des Problems an Ihr Netzwerkteam.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p115">There are network issues between your on-premises environment and Office 365. If the problem persists, contact your network team to troubleshoot the issue.</span></span>
    
<span data-ttu-id="2c9c1-169">Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-169">Find out which scenario applies to you, and make the necessary corrections.</span></span>
  
<span data-ttu-id="2c9c1-170">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-170">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="2c9c1-171">Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler</span><span class="sxs-lookup"><span data-stu-id="2c9c1-171">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="2c9c1-p116">Dieser Fehler bedeutet normalerweise, dass Office 365 beim Versuch, das Zertifikat des Ziel-Messagingservers zu überprüfen, einen Fehler festgestellt hat. Die Fehlerdetails erläutern den Fehler. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p116">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination messaging server. The error details will explain the error. For example:</span></span>
  
- <span data-ttu-id="2c9c1-175">Zertifikat abgelaufen</span><span class="sxs-lookup"><span data-stu-id="2c9c1-175">Certificate expired</span></span>
    
- <span data-ttu-id="2c9c1-176">Konflikt mit dem Zertifikatantragsteller</span><span class="sxs-lookup"><span data-stu-id="2c9c1-176">Certificate subject mismatch</span></span>
    
- <span data-ttu-id="2c9c1-177">Zertifikat ist nicht mehr gültig</span><span class="sxs-lookup"><span data-stu-id="2c9c1-177">Certificate is no longer valid</span></span>
    
<span data-ttu-id="2c9c1-178">Aktualisieren Sie das Zertifikat oder den Konnektor, sodass Nachrichten in der Warteschlange in Office 365 gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-178">Please fix the certificate or the connector so that queued messages in Office 365can be delivered.</span></span>
  
<span data-ttu-id="2c9c1-179">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="other-error-codes"></a><span data-ttu-id="2c9c1-180">Andere Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2c9c1-180">Other error codes</span></span>

<span data-ttu-id="2c9c1-p117">Office 365 hat Probleme beim Senden von Nachrichten an Ihren lokalen Messagingserver oder Partner-Messagingserver. Verwenden Sie die Informationen zum **Zielserver** im Fehler, um das Problem in Ihrer Umgebung zu untersuchen, oder ändern Sie den Konnektor bei einem Konfigurationsfehler.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-p117">Office 365 is having difficulty delivering messages to your on-premises or partner messaging server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 
  
<span data-ttu-id="2c9c1-183">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="2c9c1-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  


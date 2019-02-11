---
title: Mail Flow Intelligence in Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Administratoren können sich über die Fehlercodes informieren, die Übermittlung von Nachrichten mithilfe von Connectors in Office 365 (auch bekannt als e-Mail-Fluss Intelligence) zugeordnet sind.
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327087"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="bf701-103">Mail Flow Intelligence in Office 365</span><span class="sxs-lookup"><span data-stu-id="bf701-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="bf701-p101">In der Regel verwenden Sie eine Verbindung zum Weiterleiten von e-Mail-Nachrichten von Office 365-Organisation an Ihre lokale e-Mail-Umgebung. Sie können auch eine Verbindung zum Weiterleiten von Nachrichten aus Office 365 zu einer Partnerorganisation verwenden. Wenn Office 365 diese Nachrichten über den Connector können nicht übermittelt werden, sind sie Office 365 in der Warteschlange. Office 365 wird weiterhin zum Wiederholen der Übermittlung für jede Nachricht 48 Stunden. Nach 48 Stunden läuft die Nachricht in der Warteschlange, und die Nachricht wird an den ursprünglichen Absender in einen non-Delivery Report (auch bekannt als ein Unzustellbarkeitsbericht oder Springeffekt Nachricht) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf701-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="bf701-p102">Office 365 generiert einen Fehler, wenn eine Nachricht mit einem Connector übermittelt werden kann. In diesem Thema werden die häufigsten Fehler und deren Lösung beschrieben. Queuing und Benachrichtigung Fehler für unzustellbare Nachrichten über Connectors ist allgemein, als _e-Mail-Fluss Intelligence_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf701-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="bf701-112">Fehlercode: 450 4.4.312 DNS-Abfragefehler</span><span class="sxs-lookup"><span data-stu-id="bf701-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="bf701-p103">Dieser Fehler bedeutet normalerweise, Office 365 haben versucht, an den Smarthost verbinden, die in den Connector, aber die DNS-Abfrage zum Suchen von den Smarthost IP-Adressen konnte nicht angegeben ist. Die möglichen Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="bf701-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="bf701-115">Es gibt ein Problem mit dem DNS-Hostingdienst Ihrer Domäne (Partei, die die autoritativen Namensserver für Ihre Domäne verwaltet).</span><span class="sxs-lookup"><span data-stu-id="bf701-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="bf701-116">Ihre Domäne ist vor kurzem abgelaufen. D.h. der MX-Eintrag kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bf701-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="bf701-117">Der MX-Eintrag Ihrer Domäne hat sich kürzlich geändert, und die Office 365-DNS-Server enthalten weiterhin zuvor zwischengespeicherte DNS-Informationen für Ihre Domäne.</span><span class="sxs-lookup"><span data-stu-id="bf701-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="bf701-118">Wie behebe ich Fehlercode 450 4.4.312?</span><span class="sxs-lookup"><span data-stu-id="bf701-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="bf701-119">Arbeiten Sie mit Ihrer DNS-Hostingdienst zu identifizieren und beheben Sie das Problem mit der Domäne.</span><span class="sxs-lookup"><span data-stu-id="bf701-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="bf701-120">Wenn der Fehler aus der Partnerorganisation (beispielsweise eine 3. Partei Cloud-Dienstanbieter) ist, wenden Sie sich an Ihren Händler, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="bf701-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="bf701-121">Fehlercode: 450 4.4.315 Timeout bei der Verbindung</span><span class="sxs-lookup"><span data-stu-id="bf701-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="bf701-p104">In der Regel bedeutet dies, dass Office 365 e-Mail auf den Zielserver keine Verbindung herstellen können. Die Fehlerdetails werden das Problem erläutert. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bf701-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="bf701-125">Ihren lokalen e-Mail-Server ist ausgefallen.</span><span class="sxs-lookup"><span data-stu-id="bf701-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="bf701-126">Es ist ein Fehler in den Einstellungen des intelligenten Hosts des Konnektors vorhanden. Office 365 versucht, ein Verbindung zur falschen IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bf701-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="bf701-127">Wie behebe ich Fehlercode 450 4.4.315?</span><span class="sxs-lookup"><span data-stu-id="bf701-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="bf701-p105">Erfahren Sie, welches Szenario für Sie gilt, und Korrekturen Sie die erforderlichen. Beispielsweise müssen wenn e-Mail-Fluss ordnungsgemäß arbeitet, und Sie nicht die Connectoreinstellungen geändert haben, überprüfen Sie die lokalen e-Mail-Umgebung, ob der Server ausgefallen ist, oder ob wurden alle Änderungen an die Netzwerkinfrastruktur (z. b Sie haben Internetdienstanbietern, geändert, sodass Sie verschiedene IP-Adressen haben).</span><span class="sxs-lookup"><span data-stu-id="bf701-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="bf701-130">Wenn der Fehler aus der Partnerorganisation (beispielsweise eine 3. Partei Cloud-Dienstanbieter) ist, wenden Sie sich an Ihren Händler, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="bf701-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="bf701-131">Fehlercode: 450 4.4.316 Verbindung abgelehnt</span><span class="sxs-lookup"><span data-stu-id="bf701-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="bf701-p106">Dieser Fehler bedeutet normalerweise, dass Office 365 einen Fehler aufgetreten ist, bei dem Versuch, mit dem Ziel e-Mail-Server herstellen. Eine mögliche Ursache für diesen Fehler ist, dass die Firewall Verbindungen von Office 365-IP-Adressen blockiert. Oder dieser Fehler möglicherweise entwurfsbedingt Wenn Sie vollständig migriert haben Ihre lokale e-Mail-System zu Office 365, und fahren Sie Ihre lokale e-Mail-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bf701-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="bf701-135">Wie behebe ich Fehlercode 450 4.4.316?</span><span class="sxs-lookup"><span data-stu-id="bf701-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="bf701-p107">Wenn Sie Postfächer in Ihrer lokalen Umgebung haben, müssen Sie zum Ändern Ihrer Firewalleinstellungen, um Verbindungen von Office 365 IP-Adressen auf TCP-Port 25 mit Ihrem lokalen e-Mail-Servern zu ermöglichen. Eine Übersicht über die Office 365-IP-Adressen finden Sie unter [Office 365-URLs und IP-Adressbereiche](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf701-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="bf701-p108">Wenn keine weiteren Nachrichten an Ihre lokale Umgebung übermittelt werden sollen, klicken Sie in der Warnung auf **Jetzt korrigieren**, damit Office 365 die Nachrichten mit ungültigen Empfängern sofort ablehnen kann. Dadurch wird das Risiko verringert, dass das Kontingent für ungültige Empfänger Ihrer Organisation überschritten wird, wodurch die normale Nachrichtenübermittlung beeinträchtigt werden könnte. Alternativ können Sie das Problem mit den folgenden Anweisungen manuell beheben:</span><span class="sxs-lookup"><span data-stu-id="bf701-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="bf701-141">Deaktivieren Sie in der [Exchange-Verwaltungskonsole (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365 oder löschen Sie den Connector, der e-Mail von Office 365 mit der lokalen e-Mail-Umgebung übermittelt:</span><span class="sxs-lookup"><span data-stu-id="bf701-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="bf701-142">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Connectors**.</span><span class="sxs-lookup"><span data-stu-id="bf701-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="bf701-143">Wählen Sie die Verbindung mit dem Wert **von** **Office 365** und \*\*den Wert **Ihrer Organisation e-Mail-Server** \*\* , und führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="bf701-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="bf701-144">Löschen Sie den Connector, indem Sie auf **Löschen** ![Symbol "entfernen"](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="bf701-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="bf701-145">Deaktivieren Sie den Connector durch Klicken auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) , und **schalten Sie ihn**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf701-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="bf701-p109">Ändern Sie die akzeptierte Domäne in Office 365, die Ihre lokalen e-Mail-Umgebung von **Internes Relay** **authoritative**zugeordnet ist. Anweisungen finden Sie unter [Manage akzeptierte Domänen im Exchange, Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span><span class="sxs-lookup"><span data-stu-id="bf701-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="bf701-p110">**Hinweis**: in der Regel diese Änderungen werden zwischen 30 Minuten und einer Stunde wirksam wird. Nach einer Stunde stellen Sie sicher, dass die Fehlermeldung nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf701-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="bf701-150">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="bf701-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="bf701-151">Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server</span><span class="sxs-lookup"><span data-stu-id="bf701-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="bf701-p111">Dieser Fehler bedeutet normalerweise, Office 365 mit dem Ziel e-Mail-Server verbunden, aber der Server mit einem sofortige Fehler geantwortet, oder die Verbindung Anforderungen nicht erfüllen. Die Fehlerdetails werden das Problem erläutert. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bf701-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="bf701-155">Ziel e-Mail Serverantwort mit einer Fehlermeldung "Dienst nicht verfügbar" gibt den Server an kann keine Kommunikation mit Office 365 verwalten.</span><span class="sxs-lookup"><span data-stu-id="bf701-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="bf701-156">Der Connector wird so konfiguriert, dass TLS erforderlich, aber der Ziel-e-Mail-Server unterstützt TLS nicht.</span><span class="sxs-lookup"><span data-stu-id="bf701-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="bf701-157">Wie behebe ich Fehlercode 450 4.4.317?</span><span class="sxs-lookup"><span data-stu-id="bf701-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="bf701-158">Überprüfen Sie die TLS-Einstellungen und die Zertifikate auf Ihren lokalen e-Mail-Servern und die TLS-Einstellungen für den Connector ein.</span><span class="sxs-lookup"><span data-stu-id="bf701-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="bf701-159">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="bf701-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="bf701-160">Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen</span><span class="sxs-lookup"><span data-stu-id="bf701-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="bf701-p112">Dieser Fehler bedeutet normalerweise, dass Office 365 ist haben Probleme bei Kommunikation mit Ihrer lokalen e-Mail-Umgebung, damit die Verbindung unterbrochen wurde. Die möglichen Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="bf701-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="bf701-163">Ihre Firewall verwendet SMTP-Paketprüfungsregeln, und diese Regeln funktionieren nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="bf701-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="bf701-164">Ihren lokalen e-Mail-Server ist nicht arbeiten ordnungsgemäß (z. B., Dienst hängt, Abstürze oder geringe Systemressourcen), welcher den Server zu Timeouts verursacht, und schließen Sie die Verbindung zu Office 365.</span><span class="sxs-lookup"><span data-stu-id="bf701-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="bf701-165">Es treten Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 auf.</span><span class="sxs-lookup"><span data-stu-id="bf701-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="bf701-166">Wie behebe ich Fehlercode 450 4.4.318?</span><span class="sxs-lookup"><span data-stu-id="bf701-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="bf701-167">Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor.</span><span class="sxs-lookup"><span data-stu-id="bf701-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="bf701-168">Wenn das Problem durch Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 verursacht wird, wenden Sie sich an Ihr Netzwerkteam, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="bf701-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="bf701-169">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="bf701-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="bf701-170">Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler</span><span class="sxs-lookup"><span data-stu-id="bf701-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="bf701-p113">Dieser Fehler bedeutet normalerweise, dass Office 365-Fehler beim Versuch, die das Zertifikat des Zielservers e-Mails zu überprüfen. Die Fehlerdetails werden den Fehler erläutert. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bf701-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="bf701-174">Zertifikat abgelaufen</span><span class="sxs-lookup"><span data-stu-id="bf701-174">Certificate expired</span></span>

- <span data-ttu-id="bf701-175">Konflikt mit dem Zertifikatantragsteller</span><span class="sxs-lookup"><span data-stu-id="bf701-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="bf701-176">Zertifikat ist nicht mehr gültig</span><span class="sxs-lookup"><span data-stu-id="bf701-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="bf701-177">Wie behebe ich Fehlercode 450 4.7.320?</span><span class="sxs-lookup"><span data-stu-id="bf701-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="bf701-178">Beheben das Zertifikat oder die Einstellungen für den Connector, damit Nachrichten in Office 365 in der Warteschlange geliefert werden können.</span><span class="sxs-lookup"><span data-stu-id="bf701-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="bf701-179">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="bf701-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="bf701-180">Andere Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bf701-180">Other error codes</span></span>

<span data-ttu-id="bf701-p114">Office 365 ist Probleme übermitteln von Nachrichten an Ihre lokale oder partner-e-Mail-Server. Verwenden Sie die Informationen **Zielserver** Fehler, um das Problem in Ihrer Umgebung zu überprüfen, oder ändern Sie den Connector aus, wenn ein Konfigurationsfehler.</span><span class="sxs-lookup"><span data-stu-id="bf701-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="bf701-183">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="bf701-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

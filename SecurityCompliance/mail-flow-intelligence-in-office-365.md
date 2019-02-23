---
title: Mail Flow Intelligence in Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Administratoren erhalten Informationen zu den Fehlercodes, die der Nachrichtenübermittlung mithilfe von Connectors in Office 365 (auch bekannt als Nachrichtenfluss-Intelligence) zugeordnet sind.
ms.openlocfilehash: a679a3a50c2333a9f66509b69ec06ee96960bc83
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218715"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="026fc-103">Mail Flow Intelligence in Office 365</span><span class="sxs-lookup"><span data-stu-id="026fc-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="026fc-p101">In der Regel verwenden Sie einen Connector zum Weiterleiten von e-Mail-Nachrichten von Ihrer Office 365-Organisation an Ihre lokale e-Mail-Umgebung. Sie können auch einen Connector zum Weiterleiten von Nachrichten von Office 365 an eine Partnerorganisation verwenden. Wenn Office 365 diese Nachrichten nicht über den Connector übermitteln kann, werden Sie in der Warteschlange in Office 365. In Office 365 wird die Übermittlung für jede Nachricht für 48 Stunden fortgesetzt. Nach 48 Stunden läuft die Nachricht in der Warteschlange ab, und die Nachricht wird an den ursprünglichen Absender in einem Unzustellbarkeitsbericht (auch bekannt als NDR oder Bounce-Nachricht) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="026fc-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="026fc-p102">Office 365 generiert einen Fehler, wenn eine Nachricht nicht mithilfe eines Connectors übermittelt werden kann. Die häufigsten Fehler und deren Lösungen werden in diesem Thema beschrieben. Kollektiv werden Warteschlangen-und Benachrichtigungsfehler für unzustellbare Nachrichten, die über Connectors gesendet werden, als Nachrichtenübermittlungs _Nachrichten_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="026fc-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="026fc-112">Fehlercode: 450 4.4.312 DNS-Abfragefehler</span><span class="sxs-lookup"><span data-stu-id="026fc-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="026fc-p103">Dieser Fehler weist in der Regel darauf hin, dass Office 365 versucht hat, eine Verbindung mit dem im Connector angegebenen Smarthost herzustellen, aber die DNS-Abfrage zum Auffinden der IP-Adressen des Smarthosts ist fehlgeschlagen. Mögliche Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="026fc-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="026fc-115">Es gibt ein Problem mit dem DNS-Hostingdienst Ihrer Domäne (Partei, die die autoritativen Namensserver für Ihre Domäne verwaltet).</span><span class="sxs-lookup"><span data-stu-id="026fc-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="026fc-116">Ihre Domäne ist vor kurzem abgelaufen. D.h. der MX-Eintrag kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="026fc-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="026fc-117">Der MX-Eintrag Ihrer Domäne hat sich kürzlich geändert, und die Office 365-DNS-Server enthalten weiterhin zuvor zwischengespeicherte DNS-Informationen für Ihre Domäne.</span><span class="sxs-lookup"><span data-stu-id="026fc-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="026fc-118">Wie behebe ich den Fehlercode 450 4.4.312?</span><span class="sxs-lookup"><span data-stu-id="026fc-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="026fc-119">Arbeiten Sie mit Ihrem DNS-Hostingdienst zusammen, um das Problem mit Ihrer Domäne zu identifizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="026fc-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="026fc-120">Wenn der Fehler von ihrer Partnerorganisation stammt (beispielsweise einem Cloud-Dienstanbieter eines Drittanbieters), wenden Sie sich an Ihren Partner, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="026fc-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="026fc-121">Fehlercode: 450 4.4.315 Timeout bei der Verbindung</span><span class="sxs-lookup"><span data-stu-id="026fc-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="026fc-p104">In der Regel ist dies der Fall, dass Office 365 keine Verbindung zum Ziel-e-Mail-Server herstellen kann. Die Fehlerdetails erläutern das Problem. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="026fc-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="026fc-125">Der lokale e-Mail-Server ist ausgefallen.</span><span class="sxs-lookup"><span data-stu-id="026fc-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="026fc-126">Es ist ein Fehler in den Einstellungen des intelligenten Hosts des Konnektors vorhanden. Office 365 versucht, ein Verbindung zur falschen IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="026fc-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="026fc-127">Wie behebe ich den Fehlercode 450 4.4.315?</span><span class="sxs-lookup"><span data-stu-id="026fc-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="026fc-p105">Finden Sie heraus, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor. Wenn der e-Mail-Fluss beispielsweise ordnungsgemäß funktioniert hat und Sie die Connectoreinstellungen nicht geändert haben, müssen Sie Ihre lokale e-Mail-Umgebung überprüfen, um festzustellen, ob der Server ausgefallen ist, oder wenn Änderungen an Ihrer Netzwerkinfrastruktur vorgenommen wurden (beispielsweise Sie haben Internetdienstanbieter geändert, sodass Sie jetzt über unterschiedliche IP-Adressen verfügen).</span><span class="sxs-lookup"><span data-stu-id="026fc-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="026fc-130">Wenn der Fehler von ihrer Partnerorganisation stammt (beispielsweise einem Cloud-Dienstanbieter eines Drittanbieters), wenden Sie sich an Ihren Partner, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="026fc-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="026fc-131">Fehlercode: 450 4.4.316 Verbindung abgelehnt</span><span class="sxs-lookup"><span data-stu-id="026fc-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="026fc-p106">Dieser Fehler hat zur Folge, dass Office 365 einen Verbindungsfehler festgestellt hat, als er versucht hat, eine Verbindung mit dem Ziel-e-Mail-Server herzustellen. Eine mögliche Ursache für diesen Fehler ist, dass Ihre Firewall Verbindungen von Office 365-IP-Adressen blockiert. Oder dieser Fehler ist möglicherweise beabsichtigt, wenn Sie Ihr lokales e-Mail-System vollständig zu Office 365 migriert haben und Ihre lokale e-Mail-Umgebung Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="026fc-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="026fc-135">Wie behebe ich den Fehlercode 450 4.4.316?</span><span class="sxs-lookup"><span data-stu-id="026fc-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="026fc-p107">Wenn Sie Postfächer in Ihrer lokalen Umgebung haben, müssen Sie Ihre Firewalleinstellungen so ändern, dass Verbindungen von Office 365-IP-Adressen am TCP-Anschluss 25 an Ihre lokalen e-Mail-Server zulässig sind. Eine Liste der Office 365-IP-Adressen finden Sie unter [office 365-URLs und IP-Adressbereiche](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span><span class="sxs-lookup"><span data-stu-id="026fc-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="026fc-p108">Wenn keine weiteren Nachrichten an Ihre lokale Umgebung übermittelt werden sollen, klicken Sie in der Warnung auf **Jetzt korrigieren**, damit Office 365 die Nachrichten mit ungültigen Empfängern sofort ablehnen kann. Dadurch wird das Risiko verringert, dass das Kontingent für ungültige Empfänger Ihrer Organisation überschritten wird, wodurch die normale Nachrichtenübermittlung beeinträchtigt werden könnte. Alternativ können Sie das Problem mit den folgenden Anweisungen manuell beheben:</span><span class="sxs-lookup"><span data-stu-id="026fc-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="026fc-141">Deaktivieren oder löschen Sie in der [Exchange-Verwaltungskonsole (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365 den Connector, der E-Mails von Office 365 an Ihre lokale e-Mail-Umgebung zustellt:</span><span class="sxs-lookup"><span data-stu-id="026fc-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="026fc-142">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> \*\*\*\*-Konnektoren.</span><span class="sxs-lookup"><span data-stu-id="026fc-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="026fc-143">Wählen Sie den Connector mit dem Wert **von** **Office 365** und dem Wert **für** den **e-Mail-Server Ihrer Organisation** aus, und führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="026fc-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="026fc-144">Löschen Sie den Connector, indem Sie auf **Löschen** ![entfernen (Symbol)](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="026fc-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="026fc-145">Deaktivieren Sie den Connector, \*\*\*\* ![indem Sie auf](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) Bearbeitungssymbol bearbeiten klicken und die Option **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="026fc-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="026fc-p109">Ändern Sie die akzeptierte Domäne in Office 365, die Ihrer lokalen e-Mail-Umgebung zugeordnet ist, von **internem Relay** zu **autorisierend**. Anweisungen finden Sie unter [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span><span class="sxs-lookup"><span data-stu-id="026fc-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="026fc-p110">**Hinweis**: diese Änderungen dauern in der Regel zwischen 30 Minuten und einer Stunde. Vergewissern Sie sich nach einer Stunde, dass der Fehler nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="026fc-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="026fc-150">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="026fc-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="026fc-151">Fehlercode: 450 4.4.317 Fehler beim Herstellen der Verbindung mit Remote-Server</span><span class="sxs-lookup"><span data-stu-id="026fc-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="026fc-p111">Dieser Fehler bedeutet NormalerWeise, dass Office 365 mit dem Ziel-e-Mail-Server verbunden ist, der Server jedoch mit einem unmittelbaren Fehler reagiert hat oder die Verbindungsanforderungen nicht erfüllt. Die Fehlerdetails erläutern das Problem. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="026fc-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="026fc-155">Der Ziel-e-Mail-Server hat mit dem Fehler "Dienst nicht verfügbar" geantwortet, was darauf hinweist, dass der Server die Kommunikation mit Office 365 nicht aufrecht erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="026fc-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="026fc-156">Der Connector ist so konfiguriert, dass er TLS erfordert, aber der Ziel-e-Mail-Server unterstützt TLS nicht.</span><span class="sxs-lookup"><span data-stu-id="026fc-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="026fc-157">Wie behebe ich den Fehlercode 450 4.4.317?</span><span class="sxs-lookup"><span data-stu-id="026fc-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="026fc-158">Überprüfen Sie die TLS-Einstellungen und-Zertifikate auf Ihren lokalen e-Mail-Servern und die TLS-Einstellungen für den Connector.</span><span class="sxs-lookup"><span data-stu-id="026fc-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="026fc-159">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="026fc-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="026fc-160">Fehlercode: 450 4.4.318 Verbindung wurde plötzlich geschlossen</span><span class="sxs-lookup"><span data-stu-id="026fc-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="026fc-p112">Dieser Fehler bedeutet NormalerWeise, dass Office 365 mit Ihrer lokalen e-Mail-Umgebung nicht kommunizieren kann, sodass die Verbindung unterbrochen wurde. Mögliche Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="026fc-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="026fc-163">Ihre Firewall verwendet SMTP-Paketprüfungsregeln, und diese Regeln funktionieren nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="026fc-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="026fc-164">Der lokale e-Mail-Server funktioniert nicht ordnungsgemäß (beispielsweise der Dienst hängt, stürzt ab, oder Systemressourcen mit geringer Leistung), wodurch der Server ausfällt und die Verbindung zu Office 365 geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="026fc-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="026fc-165">Es treten Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 auf.</span><span class="sxs-lookup"><span data-stu-id="026fc-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="026fc-166">Wie behebe ich den Fehlercode 450 4.4.318?</span><span class="sxs-lookup"><span data-stu-id="026fc-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="026fc-167">Erfahren Sie, welches Szenario für Sie gilt, und nehmen Sie die erforderlichen Korrekturen vor.</span><span class="sxs-lookup"><span data-stu-id="026fc-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="026fc-168">Wenn das Problem durch Netzwerkprobleme zwischen Ihrer lokalen Umgebung und Office 365 verursacht wird, wenden Sie sich an Ihr Netzwerkteam, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="026fc-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="026fc-169">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="026fc-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="026fc-170">Fehlercode: 450 4.7.320 Zertifikatüberprüfungsfehler</span><span class="sxs-lookup"><span data-stu-id="026fc-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="026fc-p113">Dieser Fehler hat zur Folge, dass Office 365 beim Versuch, das Zertifikat des Ziel-e-Mail-Servers zu überprüfen, einen Fehler festgestellt hat. Die Fehlerdetails erläutern den Fehler. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="026fc-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="026fc-174">Zertifikat abgelaufen</span><span class="sxs-lookup"><span data-stu-id="026fc-174">Certificate expired</span></span>

- <span data-ttu-id="026fc-175">Konflikt mit dem Zertifikatantragsteller</span><span class="sxs-lookup"><span data-stu-id="026fc-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="026fc-176">Zertifikat ist nicht mehr gültig</span><span class="sxs-lookup"><span data-stu-id="026fc-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="026fc-177">Wie behebe ich den Fehlercode 450 4.7.320?</span><span class="sxs-lookup"><span data-stu-id="026fc-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="026fc-178">Beheben Sie das Zertifikat oder die Einstellungen für den Connector, damit in der Warteschlange Nachrichten in Office 365 zugestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="026fc-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="026fc-179">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="026fc-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="026fc-180">Andere Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="026fc-180">Other error codes</span></span>

<span data-ttu-id="026fc-p114">Office 365 hat Schwierigkeiten bei der Übermittlung von Nachrichten an Ihren lokalen oder Partner-e-Mail-Server. Verwenden Sie die Informationen zum **Zielserver** in dem Fehler, um das Problem in Ihrer Umgebung zu untersuchen, oder ändern Sie den Connector, wenn ein Konfigurationsfehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="026fc-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="026fc-183">Wenn der Fehler von Ihrer Partnerorganisation generiert wurde (beispielsweise einem Drittanbieter von Clouddiensten), müssen Sie sich zur Problembehebung an Ihren Partner wenden.</span><span class="sxs-lookup"><span data-stu-id="026fc-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

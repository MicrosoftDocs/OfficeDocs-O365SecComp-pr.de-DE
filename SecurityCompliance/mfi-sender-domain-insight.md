---
title: Beheben von Absenderdomänen Einblicken
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren erfahren mehr über die Fehlerbehebung der Absenderdomäne im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 6d98d2a2660c24a77db58215faa0de1a4a18ea1a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722882"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="17b31-103">Beheben von Absenderdomänen Einblicken</span><span class="sxs-lookup"><span data-stu-id="17b31-103">Fix sender domain insight</span></span>

> [!NOTE]
> <span data-ttu-id="17b31-104">Die in diesem Thema beschriebenen Features wurden nicht für alle Office 365-Organisationen bereitgestellt und können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="17b31-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="17b31-105">Office 365 erfordert Nachrichten, die von internen lokalen e-Mail-Umgebungen an Office 365 gesendet werden, um bestimmte Sicherheitskriterien zu erfüllen:</span><span class="sxs-lookup"><span data-stu-id="17b31-105">Office 365 requires messages sending from internal on-premises email environments to Office 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="17b31-106">Sie haben einen eingehenden Connector in Office 365 erstellt, um SMTP-Verbindungen von Ihrem lokalen e-Mail-Server mithilfe der Quell-IP-Adresse oder eines Zertifikats zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="17b31-106">You've created an inbound connector in Office 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="17b31-107">Sie haben ihren lokalen e-Mail-Server so konfiguriert, dass er e-Mails über Office 365 an External World weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="17b31-107">You've configured your on-premises email server to relay email via Office 365 to external world.</span></span>

- <span data-ttu-id="17b31-108">In Ihrer Konfiguration ist eine der folgenden Aussagen true:</span><span class="sxs-lookup"><span data-stu-id="17b31-108">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="17b31-109">Die e-Mail-Domäne des Absenders ist in Ihrer Office 365-Organisation registriert.</span><span class="sxs-lookup"><span data-stu-id="17b31-109">The sender's email domain is registered in your Office 365 organization.</span></span> <span data-ttu-id="17b31-110">Weitere Informationen finden Sie unter Hinzufügen von Domänen in Office 365.</span><span class="sxs-lookup"><span data-stu-id="17b31-110">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="17b31-111">Der lokale e-Mail-Server ist für die Verwendung eines Zertifikats zum Senden von e-Mails an Office 365 konfiguriert, das Zertifikat enthält oder genau mit einem Domänennamen übereinstimmt, den Sie in Office 365 registriert haben, und Sie haben einen zertifikatbasierten Connector in Office 365 mit dem Domänen.</span><span class="sxs-lookup"><span data-stu-id="17b31-111">Your on-premises email server is configured to use a certificate to send email to Office 365, the certificate contains or exactly matches a domain name that you've registered in Office 365, and you've created a certificate based connector in Office 365 with that domain.</span></span> 

<span data-ttu-id="17b31-112">Nachrichten, die die Kriterien nicht erfüllen, werden der Organisation nicht zugeordnet und können zurückgewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="17b31-112">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="17b31-113">Die Einblicke in die **Absenderdomäne von Fix** zeigen Ihnen e-Mails von Ihrer lokalen Umgebung, die nicht den Kriterien entsprechen, hilft Ihnen bei der Identifizierung potenziell gefährdeter Computer und Benutzerkonten in Ihrer lokalen e-Mail-Umgebung und unterstützt Sie bei der Durchführung Korrekturaktionen.</span><span class="sxs-lookup"><span data-stu-id="17b31-113">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![Die FehlerbeHebung der Absenderdomäne im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/sender-domain-insight-selected.png)

<span data-ttu-id="17b31-115">Wenn Sie auf **Details anzeigen**klicken, werden Sie zu einem anderen Widget mit weiteren Details geführt, wie im folgenden Diagramm dargestellt:</span><span class="sxs-lookup"><span data-stu-id="17b31-115">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![Das Widget "Details" in der FehlerbeHebung der Absenderdomäne](media/sender-domain-view-details.png)

<span data-ttu-id="17b31-117">Der eingehende Connector, der zum übermitteln der Nachrichten an Office 365 verwendet wurde, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17b31-117">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="17b31-118">Sie können auch auf **Beispiel Nachrichten-IDs anzeigen** klicken, um Details zu den Nachrichten anzuzeigen, die von Ihrer lokalen e-Mail-Umgebung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="17b31-118">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="17b31-119">Da diese Nachrichten von Office 365 abgelehnt wurden, können Sie die Nachrichtenablaufverfolgung nicht verwenden, aber die Beispiel Nachrichten-IDs verwenden, um die Nachrichten in Ihrer lokalen e-Mail-Umgebung nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="17b31-119">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![Anzeigen von Beispiel Nachrichten-IDs in der FehlerbeHebung der Absenderdomäne](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a><span data-ttu-id="17b31-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17b31-121">See also</span></span>

<span data-ttu-id="17b31-122">Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="17b31-122">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>

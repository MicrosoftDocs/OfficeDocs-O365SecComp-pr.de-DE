---
title: SCL-Bewertungen (Spam Confidence Level)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
description: Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
ms.openlocfilehash: 4b8eea798bc46396e06da2c6ba0573c019d7a9b7
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002904"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="33370-106">SCL-Bewertungen (Spam Confidence Level)</span><span class="sxs-lookup"><span data-stu-id="33370-106">Spam confidence levels</span></span>

<span data-ttu-id="33370-p102">Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="33370-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="33370-111">**SCL-Bewertung**</span><span class="sxs-lookup"><span data-stu-id="33370-111">**SCL Rating**</span></span>|<span data-ttu-id="33370-112">**Spam Confidence-Interpretation**</span><span class="sxs-lookup"><span data-stu-id="33370-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="33370-113">**Standardaktion**</span><span class="sxs-lookup"><span data-stu-id="33370-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="33370-114">-1</span><span class="sxs-lookup"><span data-stu-id="33370-114">-1</span></span>  <br/> |<span data-ttu-id="33370-115">Kein Spam von einem sicheren Absender, Empfänger oder einer als sicher gelisteten IP-Adresse (vertrauenswürdiger Partner)</span><span class="sxs-lookup"><span data-stu-id="33370-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner)</span></span>  <br/> |<span data-ttu-id="33370-116">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="33370-116">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="33370-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="33370-117">0, 1</span></span>  <br/> |<span data-ttu-id="33370-118">Kein Spam, weil die Nachricht überprüft und als spamfrei eingestuft wurde</span><span class="sxs-lookup"><span data-stu-id="33370-118">Non-spam because the message was scanned and determined to be clean</span></span>  <br/> |<span data-ttu-id="33370-119">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="33370-119">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="33370-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="33370-120">5, 6</span></span>  <br/> | <span data-ttu-id="33370-121">Spam</span><span class="sxs-lookup"><span data-stu-id="33370-121">Spam</span></span>  <br/> |<span data-ttu-id="33370-122">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="33370-122">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="33370-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="33370-123">7, 8, 9</span></span>  <br/> |<span data-ttu-id="33370-124">Spam mit hoher Vertrauenswürdigkeit</span><span class="sxs-lookup"><span data-stu-id="33370-124">High confidence spam</span></span>  <br/> |<span data-ttu-id="33370-125">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="33370-125">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
   
> [!TIP]
> <span data-ttu-id="33370-p103">SCL-Bewertung 2, 3, 4, 7 und 8 werden vom Dienst nicht festgelegt. SCL-Bewertung 5 oder 6 wird als Spam angesehen, das weniger sicher, dass Spam als SCL-Bewertung 9, sein, die bestimmte Spam betrachtet wird. Verschiedene Aktionen für Spam und vertrauenswürdige Spam können über Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole konfiguriert werden. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](configure-your-spam-filter-policies.md). Sie können auch die SCL-Bewertung für Nachrichten festlegen, die bestimmte Suchkriterien mithilfe von Transportregeln, wie unter [Verwenden von e-Mail-Flussregeln zum Spam Confidence Level (SCL) in Nachrichten festgelegt](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Wenn Sie eine Transportregel verwenden, um die SCL-Wert von 7, 8 und 9 festgelegt wird die Nachricht als vertrauenswürdige Spam behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="33370-p103">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service. An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam. Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). You can also set the SCL rating for messages that match specific conditions by using Transport rules, as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). If you use a transport rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="33370-p104">![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="33370-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   


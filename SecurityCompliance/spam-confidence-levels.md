---
title: SCL-Bewertungen (Spam Confidence Level)
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275645"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="f27ab-106">SCL-Bewertungen (Spam Confidence Level)</span><span class="sxs-lookup"><span data-stu-id="f27ab-106">Spam confidence levels</span></span>

<span data-ttu-id="f27ab-p102">Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f27ab-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="f27ab-111">**SCL-Bewertung**</span><span class="sxs-lookup"><span data-stu-id="f27ab-111">**SCL Rating**</span></span>|<span data-ttu-id="f27ab-112">**Spam Confidence-Interpretation**</span><span class="sxs-lookup"><span data-stu-id="f27ab-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="f27ab-113">**Standardaktion**</span><span class="sxs-lookup"><span data-stu-id="f27ab-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f27ab-114">-1</span><span class="sxs-lookup"><span data-stu-id="f27ab-114">-1</span></span>  <br/> |<span data-ttu-id="f27ab-115">Kein Spam von einem sicheren Absender, Empfänger oder einer als sicher gelisteten IP-Adresse (vertrauenswürdiger Partner)</span><span class="sxs-lookup"><span data-stu-id="f27ab-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner)</span></span>  <br/> |<span data-ttu-id="f27ab-116">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="f27ab-116">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="f27ab-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="f27ab-117">0, 1</span></span>  <br/> |<span data-ttu-id="f27ab-118">Kein Spam, weil die Nachricht überprüft und als spamfrei eingestuft wurde</span><span class="sxs-lookup"><span data-stu-id="f27ab-118">Non-spam because the message was scanned and determined to be clean</span></span>  <br/> |<span data-ttu-id="f27ab-119">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="f27ab-119">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="f27ab-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="f27ab-120">5, 6</span></span>  <br/> | <span data-ttu-id="f27ab-121">Spam</span><span class="sxs-lookup"><span data-stu-id="f27ab-121">Spam</span></span>  <br/> |<span data-ttu-id="f27ab-122">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="f27ab-122">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="f27ab-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="f27ab-123">7, 8, 9</span></span>  <br/> |<span data-ttu-id="f27ab-124">Spam mit hoher Vertrauenswürdigkeit</span><span class="sxs-lookup"><span data-stu-id="f27ab-124">High confidence spam</span></span>  <br/> |<span data-ttu-id="f27ab-125">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="f27ab-125">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
   
> [!TIP]
> <span data-ttu-id="f27ab-p103">SCL-Bewertungen von 2, 3, 4, 7 und 8 werden vom Dienst nicht festgelegt. Eine SCL-Bewertung von 5 oder 6 wird als mutmaßlicher Spam betrachtet, der weniger sicher ist als Spam als eine SCL-Bewertung von 9, die als bestimmter Spam angesehen wird. Unterschiedliche Aktionen für Spam und Spam mit hoher Vertrauenswürdigkeit können über Ihre Inhaltsfilter Richtlinien in der Exchange-Verwaltungskonsole konfiguriert werden. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md). Sie können die SCL-Bewertung für Nachrichten, die bestimmte Bedingungen erfüllen, auch mithilfe von Transport Regeln festlegen, wie in [Verwenden von Nachrichtenfluss Regeln beschrieben, um SCL (Spam Confidence Level) in Nachrichten festzulegen](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Wenn Sie eine Transportregel zum Festlegen der SCL-Bewertung von 7, 8 oder 9 verwenden, wird die Nachricht als Spam mit hoher Vertrauenswürdigkeit behandelt.</span><span class="sxs-lookup"><span data-stu-id="f27ab-p103">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service. An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam. Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). You can also set the SCL rating for messages that match specific conditions by using Transport rules, as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). If you use a transport rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="f27ab-p104">![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="f27ab-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   


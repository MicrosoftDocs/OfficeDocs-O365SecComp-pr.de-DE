---
title: SCL-Bewertungen (Spam Confidence Level)
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
ms.openlocfilehash: 48ca02bf3f6549c5acc1147ea477b9d22f1c76e1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260673"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="8648d-106">SCL-Bewertungen (Spam Confidence Level)</span><span class="sxs-lookup"><span data-stu-id="8648d-106">Spam confidence levels</span></span>

<span data-ttu-id="8648d-p102">Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="8648d-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="8648d-111">**SCL-Bewertung**</span><span class="sxs-lookup"><span data-stu-id="8648d-111">**SCL Rating**</span></span>|<span data-ttu-id="8648d-112">**Spam Confidence-Interpretation**</span><span class="sxs-lookup"><span data-stu-id="8648d-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="8648d-113">**Standardaktion**</span><span class="sxs-lookup"><span data-stu-id="8648d-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8648d-114">-1</span><span class="sxs-lookup"><span data-stu-id="8648d-114">-1</span></span>|<span data-ttu-id="8648d-115">Nicht-Spam, der von einem sicheren Absender, einem sicheren Empfänger oder einer sicheren aufgeführten IP-Adresse stammt (vertrauenswürdiger Partner).</span><span class="sxs-lookup"><span data-stu-id="8648d-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner).</span></span>|<span data-ttu-id="8648d-116">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="8648d-116">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="8648d-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="8648d-117">0, 1</span></span>|<span data-ttu-id="8648d-118">Nicht-Spam, da die Nachricht gescannt und als sauber festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8648d-118">Non-spam because the message was scanned and determined to be clean.</span></span>|<span data-ttu-id="8648d-119">Die Nachricht wird in das Postfach des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="8648d-119">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="8648d-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="8648d-120">5, 6</span></span>|<span data-ttu-id="8648d-121">Spam</span><span class="sxs-lookup"><span data-stu-id="8648d-121">Spam</span></span>|<span data-ttu-id="8648d-122">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="8648d-122">Deliver the message to the recipients' Junk Email folder.</span></span>|
|<span data-ttu-id="8648d-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="8648d-123">7, 8, 9</span></span>|<span data-ttu-id="8648d-124">Spam mit hoher Vertrauenswürdigkeit</span><span class="sxs-lookup"><span data-stu-id="8648d-124">High confidence spam</span></span>|<span data-ttu-id="8648d-125">Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.</span><span class="sxs-lookup"><span data-stu-id="8648d-125">Deliver the message to the recipients' Junk Email folder.</span></span>|
   
> [!TIP]
> <span data-ttu-id="8648d-126">SCL-Bewertungen von 2, 3, 4, 7 und 8 werden vom Dienst nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8648d-126">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service.</span></span> <span data-ttu-id="8648d-127">Eine SCL-Bewertung von 5 oder 6 wird als mutmaßlicher Spam betrachtet, der weniger sicher ist als Spam als eine SCL-Bewertung von 9, die als bestimmter Spam angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="8648d-127">An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam.</span></span> <span data-ttu-id="8648d-128">Unterschiedliche Aktionen für Spam und Spam mit hoher Vertrauenswürdigkeit können über Ihre Inhaltsfilter Richtlinien in der Exchange-Verwaltungskonsole konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8648d-128">Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="8648d-129">Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8648d-129">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="8648d-130">Sie können die SCL-Bewertung für Nachrichten, die bestimmte Bedingungen erfüllen, auch mithilfe von Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) festlegen, wie in [Verwenden von Nachrichtenfluss Regeln beschrieben, um SCL (Spam Confidence Level) in Nachrichten festzulegen](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8648d-130">You can also set the SCL rating for messages that match specific conditions by using mail flow rules (also known as transport rules), as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span></span> <span data-ttu-id="8648d-131">Wenn Sie eine e-Mail-Fluss Regel zum Festlegen der SCL-Bewertung von 7, 8 oder 9 verwenden, wird die Nachricht als Spam mit hoher Vertrauenswürdigkeit behandelt.</span><span class="sxs-lookup"><span data-stu-id="8648d-131">If you use a mail flow rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="8648d-p104">![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="8648d-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span>|
   


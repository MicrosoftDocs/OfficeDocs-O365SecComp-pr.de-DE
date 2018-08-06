---
title: BCL-Werte (Bulk Complaint Level)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
description: Versender von Massen-E-Mails arbeiten mit verschiedenen Sendemustern, Inhalterstellungsverfahren und Listenbeschaffungsarten. Einige von ihnen sind gute Absender, die erwünschte Nachrichten mit relevantem Inhalt an Ihre Abonnenten senden. Diese Nachrichten führen zu wenigen Beschwerden von Empfängern. Andere Absender verwenden unerwünschte Nachrichten, die den Kriterien für Spam sehr nahekommen und zu vielen Beschwerden von Empfängern führen. Um zwischen diesen Typen von Massen-E-Mail-Absendern zu unterscheiden, werden ihren Nachrichten BCL-Bewertungen (Bulk Complaint Level) zugewiesen. BCL-Bewertungen können zwischen 1 und 9 liegen - je nachdem, wie wahrscheinlich es ist, dass die Massen-E-Mail zu Beschwerden führen. Ein Absender mit dem BCL-Wert 9 wird wahrscheinlich mehr Beschwerden von Empfängern erhalten, was mit einem BCL-Wert von 3 wahrscheinlich nicht der Fall ist. Microsoft arbeitet sowohl mit internen Quellen als auch mit Quellen von Drittanbietern, um die Absender von Massen-E-Mails zu identifizieren und den passenden BCL-Wert zu bestimmen. Diese Bewertung wird in der X-Microsoft-Antispam-Kopfzeile jeder Nachricht angezeigt. Weitere Informationen zu dieser Nachrichtenkopfzeile finden Sie unter Antispam-Nachrichtenkopfzeilen.
ms.openlocfilehash: adf179ba4a309f2ed22275179013b576888960c6
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026262"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="cae69-112">BCL-Werte (Bulk Complaint Level)</span><span class="sxs-lookup"><span data-stu-id="cae69-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="cae69-p102">Versender von Massen-E-Mails arbeiten mit verschiedenen Sendemustern, Inhalterstellungsverfahren und Listenbeschaffungsarten. Einige von ihnen sind gute Absender, die erwünschte Nachrichten mit relevantem Inhalt an Ihre Abonnenten senden. Diese Nachrichten führen zu wenigen Beschwerden von Empfängern. Andere Absender verwenden unerwünschte Nachrichten, die den Kriterien für Spam sehr nahekommen und zu vielen Beschwerden von Empfängern führen. Um zwischen diesen Typen von Massen-E-Mail-Absendern zu unterscheiden, werden ihren Nachrichten BCL-Bewertungen (Bulk Complaint Level) zugewiesen. BCL-Bewertungen können zwischen 1 und 9 liegen - je nachdem, wie wahrscheinlich es ist, dass die Massen-E-Mail zu Beschwerden führen. Ein Absender mit dem BCL-Wert 9 wird wahrscheinlich mehr Beschwerden von Empfängern erhalten, was mit einem BCL-Wert von 3 wahrscheinlich nicht der Fall ist. Microsoft arbeitet sowohl mit internen Quellen als auch mit Quellen von Drittanbietern, um die Absender von Massen-E-Mails zu identifizieren und den passenden BCL-Wert zu bestimmen. Diese Bewertung wird in der **X-Microsoft-Antispam**-Kopfzeile jeder Nachricht angezeigt. Weitere Informationen zu dieser Nachrichtenkopfzeile finden Sie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="cae69-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="cae69-123">Sie können BCL-Werte verwenden, um die für Ihre Organisation gewünschte Massenfilterungsebene festzulegen, indem Sie die Schritte unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="cae69-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="cae69-p103">Weitere BCL-Werte werden hinzugefügt und hier in Zukunft eingeschlossen. In der folgenden Tabelle werden die aktuell verwendeten BCL-Werte aufgelistet und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cae69-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cae69-126">**BCL-Wert**</span><span class="sxs-lookup"><span data-stu-id="cae69-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="cae69-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cae69-127">**Description**</span></span> <br/> |
|<span data-ttu-id="cae69-128">0</span><span class="sxs-lookup"><span data-stu-id="cae69-128">0</span></span>  <br/> |<span data-ttu-id="cae69-129">Die Nachricht stammt nicht von einem Massen-E-Mail-Absender.</span><span class="sxs-lookup"><span data-stu-id="cae69-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="cae69-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="cae69-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="cae69-131">Die Nachricht stammt von einem Massen-E-Mail-Absender, aber führt zu wenigen Beschwerden.</span><span class="sxs-lookup"><span data-stu-id="cae69-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="cae69-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="cae69-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="cae69-133">Die Nachricht stammt von einem Massen-E-Mail-Absender und führt zu einer gemischten Anzahl von Beschwerden.</span><span class="sxs-lookup"><span data-stu-id="cae69-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="cae69-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="cae69-134">8, 9</span></span>  <br/> |<span data-ttu-id="cae69-135">Die Nachricht stammt von einem Massen-E-Mail-Absender und führt zu einer hohen Anzahl von Beschwerden.</span><span class="sxs-lookup"><span data-stu-id="cae69-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   


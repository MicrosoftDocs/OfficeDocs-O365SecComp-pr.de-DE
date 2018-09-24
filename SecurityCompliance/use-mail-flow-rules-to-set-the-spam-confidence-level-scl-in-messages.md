---
title: 'Verwenden von Nachrichtenflussregeln zum Festlegen der SCL-Bewertung (Spam Confidence Level) in Nachrichten '
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: Sie können eine Transportregel erstellen, mit der der SCL-Wert (Spam Confidence Level) einer E-Mail-Nachricht festgelegt wird. Die SCL-Bewertung ist ein Maßstab dafür, wie wahrscheinlich es ist, dass es sich bei einer Nachricht um Spam handelt. Spam sind unverlangt zugesandte (und normalerweise unerwünschte) E-Mail-Nachrichten. Dieser Dienst kann verschiedene Aktionen für eine Nachricht ausführen, die von ihrer SCL-Bewertung abhängen. Sie können z. B. die Spam-Inhaltsfilterung für Nachrichten umgehen, die von Mitarbeitern Ihrer Organisation gesendet werden, weil Sie darauf vertrauen, dass intern gesendete Nachrichten von Kollegen kein Spam sind. Die Verwendung von Transportregeln zur Festlegung des SCL-Wertes einer Nachricht gibt Ihnen bessere Kontrolle über den Umgang mit Spam.
ms.openlocfilehash: 97b9a62e76efea134af5bb1bb7bd25a98bb466d2
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972277"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="e1965-108">Verwenden von Nachrichtenflussregeln zum Festlegen der SCL-Bewertung (Spam Confidence Level) in Nachrichten </span><span class="sxs-lookup"><span data-stu-id="e1965-108">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="e1965-p102">Sie können eine Transportregel erstellen, mit der der SCL-Wert (Spam Confidence Level) einer E-Mail-Nachricht festgelegt wird. Die SCL-Bewertung ist ein Maßstab dafür, wie wahrscheinlich es ist, dass es sich bei einer Nachricht um Spam handelt. Spam sind unverlangt zugesandte (und normalerweise unerwünschte) E-Mail-Nachrichten. Dieser Dienst kann verschiedene Aktionen für eine Nachricht ausführen, die von ihrer SCL-Bewertung abhängen. Sie können z. B. die Spam-Inhaltsfilterung für Nachrichten umgehen, die von Mitarbeitern Ihrer Organisation gesendet werden, weil Sie darauf vertrauen, dass intern gesendete Nachrichten von Kollegen kein Spam sind. Die Verwendung von Transportregeln zur Festlegung des SCL-Wertes einer Nachricht gibt Ihnen bessere Kontrolle über den Umgang mit Spam.</span><span class="sxs-lookup"><span data-stu-id="e1965-p102">You can create a transport rule that sets the spam confidence level (SCL) of an email message. The SCL is a measure of how likely a message is to be spam. Spam is unsolicited (and typically unwanted) email messages. The service takes different action on a message depending on its SCL rating. For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam. Using transport rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="e1965-115">**Was sollten Sie wissen, bevor Sie beginnen?**</span><span class="sxs-lookup"><span data-stu-id="e1965-115">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="e1965-116">Geschätzte Zeit bis zum Abschließen dieses Verfahrens: 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e1965-116">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="e1965-p103">Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "Transportregeln" im [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) oder [Featureberechtigungen in EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e1965-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="e1965-119">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="e1965-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="e1965-120">So erstellen Sie eine Transportregel, mit der der SCL-Wert einer Nachricht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="e1965-120">To create a transport rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="e1965-121">Navigieren Sie in der Exchange-Verwaltungskonsole (EAC) zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="e1965-121">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="e1965-122">Klicken Sie auf **Neu**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Eine neue Regel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e1965-122">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="e1965-123">Geben Sie einen Namen für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="e1965-123">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="e1965-124">Klicken Sie auf **Weitere Optionen**, und geben Sie anschließend unter **Diese Regel anwenden, wenn** eine Bedingung an, durch die die Aktion ausgelöst wird, die Sie für diese Regel festlegen (in diesem Falle die Festlegung des SCL-Werts).</span><span class="sxs-lookup"><span data-stu-id="e1965-124">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="e1965-125">Sie können z. B. festlegen **Der Absender** \> **ist intern/extern** und anschließend im Dialogfeld **Absenderposition auswählen** auf die Option **Innerhalb meiner Organisation** und auf **OK** klicken.</span><span class="sxs-lookup"><span data-stu-id="e1965-125">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span><br/>
    <span data-ttu-id="e1965-126">![Absenderstandort auswählen](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="e1965-126">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="e1965-127">Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="e1965-127">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="e1965-128">Wählen sie im Dialogfeld **SCL angeben** einen der folgenden Werte aus, und klicken Sie auf **OK**:</span><span class="sxs-lookup"><span data-stu-id="e1965-128">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="e1965-129">**Spamfilter umgehen** - Mit dieser Option wird der SCL-Wert auf -1 gesetzt, was bedeutet, dass keine Inhaltsfilterung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1965-129">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="e1965-130">**0-4** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Nachricht zur weiteren Verarbeitung an den Inhaltsfilter weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e1965-130">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="e1965-p104">**5, 6** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Aktion durchgeführt, die in der entsprechenden Inhaltsfilterrichtlinie für **Spam** festgelegt ist. Die Standardaktion ist das Senden der Nachricht an den Junk-E-Mail-Ordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e1965-p104">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="e1965-p105">**7-9** - Wenn Sie den SCL auf einen dieser Werte setzen, wird die Aktion durchgeführt, die in der entsprechenden Inhaltsfilterrichtlinie für **Nachricht mit hoher Spamwahrscheinlichkeit** festgelegt ist. Die Standardaktion ist das Senden der Nachricht an den Junk-E-Mail-Ordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e1965-p105">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="e1965-p106">Weitere Informationen zum Konfigurieren Ihrer Inhaltsfilterrichtlinien finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md). Weitere Informationen zu SCL-Werten in diesem Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e1965-p106">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="e1965-137">Geben Sie zusätzliche Eigenschaften für die Regel an, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e1965-137">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="e1965-138">Weitere Informationen über die zusätzlichen Eigenschaften, die Sie für diese Regel auswählen oder festlegen können, erhalten Sie unter [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span><span class="sxs-lookup"><span data-stu-id="e1965-138">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e1965-139">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="e1965-139">How do you know this worked?</span></span>

<span data-ttu-id="e1965-p107">Wenn Sie verifizieren möchten, dass das Verfahren ordnungsgemäß funktioniert, senden Sie eine E-Mail-Nachricht an einen Mitarbeiter in Ihrer Organisation, und prüfen Sie, ob die erwartete Aktion mit der Nachricht durchgeführt wird. Wenn Sie z. B. **den SCL-Wert (Spam Confidence Level)** auf **Spamfilterung umgehen** setzen, sollte die Nachricht an das Postfach des angegebenen Empfängers gesendet werden. Wenn Sie allerdings **den SCL-Wert (Spam Confidence Level)** auf **9** gesetzt haben und die Aktion in der entsprechenden Inhaltsfilterungsrichtlinie für eine **Nachricht mit hoher Spamwahrscheinlichkeit** darin besteht, die Nachricht in den Junk-E-Mail-Ordner zu verschieben, sollte die Nachricht an den Junk-E-Mail-Ordner des angegebenen Empfängers gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1965-p107">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  


---
title: Dynamische Übermittlung und Anzeigen einer Vorschau mit Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/28/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Wenn Sie Ihre ATP sichere Anlagen Richtlinien eingerichtet haben, wählen Sie dynamische Übermittlung Nachricht Verzögerungen bei der vermieden, und aktivieren Personen für die Vorschau von Anlagen, die gescannt werden.
ms.openlocfilehash: 23017f4f995dfe6a90479d83af9522531d7bf96b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528856"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="0891c-103">Dynamische Übermittlung und Anzeigen einer Vorschau mit Office 365 ATP sichere Anlagen</span><span class="sxs-lookup"><span data-stu-id="0891c-103">Dynamic delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="0891c-p101">Dynamische Übermittlung ist eine Option, die für die ausgewählt werden kann. In diesem Artikel erfahren Sie mehr über dynamische Übermittlung und Anlage Preview-Funktionen in [ATP sichere Anlagen in Office 365](atp-safe-attachments.md)zu lesen.</span><span class="sxs-lookup"><span data-stu-id="0891c-p101">Dynamic delivery is an option that can be selected for . Read this article to learn about dynamic delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="0891c-106">Wie dynamische Übermittlung Works</span><span class="sxs-lookup"><span data-stu-id="0891c-106">How dynamic delivery works</span></span>

<span data-ttu-id="0891c-p102">Wenn Sie [sichere Anlagen ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-attachments-policies.md), Sie über mehrere Optionen für **Blockieren**, **Ersetzen**und **Dynamische Übermittlung**können. Abhängig davon, wie Ihre Richtlinien konfiguriert sind können e-Mail-Empfänger eine geringfügige Verzögerung in e-Mail-Übermittlung bemerken, wenn deren Anhänge überprüft werden. Wählen Sie zum Vermeiden von Nachricht verzögert **Dynamische Übermittlung**.</span><span class="sxs-lookup"><span data-stu-id="0891c-p102">When you [set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md), you can choose from several options, such as **Block**, **Replace**, and **Dynamic Delivery**. Depending on how your policies are configured, email recipients can experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
<span data-ttu-id="0891c-p103">Die Option dynamische Übermittlung entfällt e-Mail Verzögerungen durch den Textkörper einer e-Mail-Nachricht über mit einem Platzhalter für jede e-Mail-Anlage senden. Der Platzhalter bleibt, bis die Anlage vom [ATP sichere Anlagen in Office 365](atp-safe-attachments.md)überprüft wird. E-Mail-Empfängern gelesen und reagieren auf ihre e-Mail-Nachrichten sofort, wissen, dass ihre Anlagen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="0891c-p103">The dynamic delivery option eliminates email delays by sending the body of an email message through with a placeholder for each email attachment. The placeholder remains until the attachment is scanned by [ATP Safe Attachments in Office 365](atp-safe-attachments.md). Email recipients can read and respond to their email messages right away, knowing that their attachments are being analyzed.</span></span>
  
<span data-ttu-id="0891c-p104">Die meisten PDF-Dateien und Office während ATP Überprüfung ausgeführt wird, können Dokumente im abgesicherten Modus angezeigt werden. Wenn eine Anlage nicht kompatibel mit der dynamischen Delivery-Vorschau ist, sehen erst, e-Mail-Empfänger den Anlage Platzhalter ATP sichere Anlagen Überprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0891c-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the dynamic delivery previewer, email recipients see the attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>
  
<span data-ttu-id="0891c-p105">Jede Anlage deaktiviert ist, wird es automatisch auf die ursprüngliche e-Mail-Nachricht angefügt. Wenn eine Anlage böswilligen werden bestimmt wird, wird es zur Quarantäne, gesendet, in dem eine Person in Ihrer Organisation Security Team (wie ein globaler Office 365-Administrator oder Sicherheitsadministrator) können [Nachrichten in Quarantäne in Office 365 verwalten](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="0891c-p105">As each attachment is cleared, it is automatically reattached to the original email message. If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="0891c-117">Was geschieht, wenn jemand einer e-Mail, weiterleitet enthält eine Anlage?</span><span class="sxs-lookup"><span data-stu-id="0891c-117">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="0891c-p106">Nehmen Sie an, dass eine Organisation dynamische Übermittlung für die [sichere Anlagen ATP-Richtlinie](set-up-atp-safe-attachments-policies.md), und eine Person empfängt eine e-Mail, die eine Anlage enthält. Nun nehmen wir an diese Person ist die e-Mail-Nachricht an eine andere Person weiterleiten. Was ist los? Das hängt davon ab, ob die zusätzliche Empfänger in ATP sichere Anlagen Richtlinien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0891c-p106">Suppose that an organization is using dynamic delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person is about to forward the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="0891c-122">Wenn Sie ein Empfänger über eine sichere Anlagen ATP-Richtlinie mit der Option dynamische Übermittlung sind, sieht der Empfänger den Platzhalter die Möglichkeit, kompatible Dateien eine Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0891c-122">If a recipient is covered by an ATP Safe Attachments policy using the dynamic delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="0891c-123">Wenn Sie ein Empfänger nicht durch eine Richtlinie ATP sichere Anlagen behandelt wird, werden dann der e-Mail- und die Anlage, ohne ATP sichere Anlagen scannen oder Anlage Platzhalter durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0891c-123">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="0891c-124">Erforderlich für dynamische Übermittlung funktioniert?</span><span class="sxs-lookup"><span data-stu-id="0891c-124">What's required for dynamic delivery to work?</span></span>

- <span data-ttu-id="0891c-125">Ihre Organisation muss [Office 365 erweiterte Schutz](office-365-atp.md) verfügen.</span><span class="sxs-lookup"><span data-stu-id="0891c-125">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="0891c-126">Richtlinien müssen für sichere ATP-Anlagen mit der Option dynamische Übermittlung (finden Sie unter [Set up ATP sichere Anlagen Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)) definiert werden</span><span class="sxs-lookup"><span data-stu-id="0891c-126">Policies must be defined for ATP Safe Attachments using the dynamic delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="0891c-127">E-Mail von Ihrer Organisation muss in Office 365 gehostet werden</span><span class="sxs-lookup"><span data-stu-id="0891c-127">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="0891c-128">Gibt es Szenarien für die dynamische Übermittlung nicht verfügbar ist?</span><span class="sxs-lookup"><span data-stu-id="0891c-128">Are there scenarios for which dynamic delivery is not available?</span></span>

<span data-ttu-id="0891c-p107">Es gibt bestimmte Szenarien, in denen dynamische Übermittlung nicht unterstützt wird. Hierzu gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="0891c-p107">There are certain scenarios in which dynamic delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="0891c-131">E-Mail-Nachrichten in öffentlichen Ordnern</span><span class="sxs-lookup"><span data-stu-id="0891c-131">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="0891c-132">E-Mail-Nachrichten, die nicht weitergeleitet werden und dann wieder in das Postfach des Benutzers mithilfe von benutzerdefinierten Regeln</span><span class="sxs-lookup"><span data-stu-id="0891c-132">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="0891c-133">Nachrichten, die (automatisch oder manuell) aus dem gehosteten Postfach und in anderen Standorten, einschließlich Archivordner verschoben werden</span><span class="sxs-lookup"><span data-stu-id="0891c-133">Messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="0891c-134">Nachrichten, die gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="0891c-134">Messages that are deleted</span></span>
    
- <span data-ttu-id="0891c-135">Ordner eines Benutzers Postfach suchen, die in einen fehlerhaften Zustand befindet</span><span class="sxs-lookup"><span data-stu-id="0891c-135">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="0891c-p108">Umgebungen, in denen ein Exchange Online-Administrator Exclaimer aktiviert hat. (Siehe [Nachrichten mit Anlagen werden nicht zugestellt werden, wenn ATP dynamische Übermittlung und Exclaimer verwendet werden](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span><span class="sxs-lookup"><span data-stu-id="0891c-p108">Environments in which an Exchange Online admin has enabled Exclaimer. (See [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="0891c-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0891c-138">Related topics</span></span>

[<span data-ttu-id="0891c-139">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0891c-139">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="0891c-140">ATP sichere Anlagen in Office 365</span><span class="sxs-lookup"><span data-stu-id="0891c-140">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="0891c-141">Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365</span><span class="sxs-lookup"><span data-stu-id="0891c-141">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="0891c-142">ATP sichere Links in Office 365</span><span class="sxs-lookup"><span data-stu-id="0891c-142">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)

[<span data-ttu-id="0891c-143">Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="0891c-143">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  


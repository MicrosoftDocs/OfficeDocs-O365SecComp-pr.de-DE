---
title: Dynamische bereit-und Vorschau mit Office 365 ATP Safe Attachments
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Bei der Einrichtung Ihrer Richtlinien für sichere ATP-Anlagen wählen Sie dynamische Übermittlung aus, um Verzögerungen bei Nachrichten zu vermeiden und Personen eine Vorschau der zu überprüfenden Anhänge zu ermöglichen.
ms.openlocfilehash: 1fb221d28a4089db8a4278903107c610d6825f5e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218395"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="3e969-103">Dynamische bereit-und Vorschau mit Office 365 ATP Safe Attachments</span><span class="sxs-lookup"><span data-stu-id="3e969-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="3e969-p101">**Zusammenfassung**: dynamische Bereitstellung ist eine Option, die für [sichere ATP-Anlagen](atp-safe-attachments.md)ausgewählt werden kann. Lesen Sie diesen Artikel, um mehr über dynamische zuBereitungen und Anlagenvorschau Funktionen in [ATP Safe Attachments in Office 365](atp-safe-attachments.md)zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="3e969-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="3e969-p102">Wenn Sie [Richtlinien für sichere Anlagen für ATP](set-up-atp-safe-attachments-policies.md) für Ihre Organisation einrichten, gibt es mehrere Optionen für die Behandlung von e-Mail-Anlagen. Hierzu gehört das **blockieren**, **ersetzen**und die **dynamische Bereitstellung**. Je nach Konfiguration von ATP-Richtlinien für sichere Anlagen können e-Mail-Empfänger bei der Überprüfung ihrer Anlagen möglicherweise eine kleine Verzögerung bei der e-Mail-Zusendung erfahren. Um Verzögerungen bei Nachrichten zu vermeiden, wählen Sie **dynamische Übermittlung**.</span><span class="sxs-lookup"><span data-stu-id="3e969-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="3e969-110">Funktionsweise der dynamischen zuSendung</span><span class="sxs-lookup"><span data-stu-id="3e969-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="3e969-p103">Die dynamische Zustellung verhindert e-Mail-Verzögerungen, indem der Textkörper einer e-Mail-Nachricht an den Empfänger mit einem Platzhalter für jede e-Mail-Anlage gesendet wird. Der Platzhalter bleibt so lange erhalten, bis eine Kopie der Anlage gescannt und durch [ATP Safe Attachments](atp-safe-attachments.md)sichergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e969-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="3e969-113">Jeder Anhang kann geöffnet oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3e969-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="3e969-114">Wenn eine Anlage als bösartig festgelegt wird, wird Sie an die Quarantäne gesendet, in der eine Person im Sicherheitsteam Ihrer Organisation (beispielsweise ein globaler Office 365-Administrator oder Sicherheitsadministrator) [isolierte Nachrichten in office 365 verwalten](manage-quarantined-messages-and-files.md)kann.</span><span class="sxs-lookup"><span data-stu-id="3e969-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="3e969-p104">Die meisten PDFs und Office-Dokumente können während der ATP-Überprüfung im abgesicherten Modus angezeigt werden. Wenn eine Anlage nicht mit der dynamischen zuStellungs Vorschau kompatibel ist, wird den e-Mail-Empfängern ein Anlagen Platzhalter angezeigt, bis die Überprüfung der ATP Safe Attachments abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3e969-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

> [!TIP]
> <span data-ttu-id="3e969-117">Wenn Sie ein mobiles Gerät verwenden und PDFs zunächst nicht in der Vorschau für die dynamische Lieferung gerendert werden, versuchen Sie, sich mit Ihrem mobilen Browser bei Office 365 anzumelden.</span><span class="sxs-lookup"><span data-stu-id="3e969-117">If you're using a mobile device, and PDFs are not rendering in Dynamic Delivery previewer at first, try signing into Office 365 using your mobile browser.</span></span>

<span data-ttu-id="3e969-118">Bei der dynamischen Bereitstellung können Personen sofort lesen und auf Ihre e-Mail-Nachrichten Antworten, während Ihre Anlagen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e969-118">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="3e969-p105">Die Überprüfung von ATP Safe Attachments erfolgt in derselben Region, in der sich Ihre Office 365-Daten befinden. Weitere Informationen zur Geografie des Rechenzentrums finden Sie unter [wo befinden sich Ihre Daten?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="3e969-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="3e969-121">Was geschieht, wenn jemand eine e-Mail weiterleitet, die eine Anlage enthält?</span><span class="sxs-lookup"><span data-stu-id="3e969-121">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="3e969-p106">Angenommen, eine Organisation verwendet die dynamische Bereitstellung für Ihre [ATP-Richtlinie für sichere Anlagen](set-up-atp-safe-attachments-policies.md), und jemand erhält eine e-Mail, die eine Anlage enthält. Nehmen wir an, diese Person leitet die e-Mail-Nachricht an einen anderen weiter. Was ist los? Es hängt davon ab, ob die zusätzlichen Empfänger in den Richtlinien für ATP Safe Attachments enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3e969-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="3e969-126">Wenn ein Empfänger von einer Richtlinie für sichere Anlagen mit ATP-Datenträgern unter Verwendung der Option für die dynamische Lieferung abgedeckt wird, sieht der Empfänger den Platzhalter mit der Möglichkeit, eine Vorschau der kompatiblen Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3e969-126">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="3e969-127">Wenn ein Empfänger nicht durch eine ATP-Richtlinie für sichere Anlagen abgedeckt wird, werden die e-Mail und die Anlage ohne ATP Safe Attachments Scanning oder Attachment Placeholders durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3e969-127">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="3e969-128">Was ist erforderlich, damit die dynamische bereitgestellt wird?</span><span class="sxs-lookup"><span data-stu-id="3e969-128">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="3e969-129">Ihre Organisation muss [Office 365 Advanced Threat Protection](office-365-atp.md) besitzen.</span><span class="sxs-lookup"><span data-stu-id="3e969-129">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="3e969-130">Richtlinien müssen für ATP-sichere Anlagen mithilfe der Option für die dynamische Bereitstellung definiert werden (siehe [Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="3e969-130">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="3e969-131">Die e-Mail Ihrer Organisation muss in Office 365 gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="3e969-131">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="3e969-132">Gibt es Szenarien, für die die dynamische Bereitstellungen nicht verfügbar ist?</span><span class="sxs-lookup"><span data-stu-id="3e969-132">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="3e969-p107">Es gibt bestimmte Szenarien, in denen die dynamische Bereitstellungen nicht unterstützt werden. Hierzu gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3e969-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="3e969-135">E-Mail-Nachrichten in öffentlichen Ordnern</span><span class="sxs-lookup"><span data-stu-id="3e969-135">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="3e969-136">E-Mail-Nachrichten, die mithilfe benutzerdefinierter Regeln aus dem Postfach des Benutzers weitergeleitet werden</span><span class="sxs-lookup"><span data-stu-id="3e969-136">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="3e969-137">E-Mail-Nachrichten, die (automatisch oder manuell) aus dem gehosteten Postfach und an andere Speicherorte verschoben werden, einschließlich Archivordnern</span><span class="sxs-lookup"><span data-stu-id="3e969-137">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="3e969-138">Gelöschte e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3e969-138">Email messages that are deleted</span></span>
    
- <span data-ttu-id="3e969-139">Der Post Fach Suchordner eines Benutzers im Fehlerzustand</span><span class="sxs-lookup"><span data-stu-id="3e969-139">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="3e969-p108">Umgebungen, in denen ein Exchange Online-Administrator den ausforderungs Server aktiviert hat. Weitere Informationen finden Sie unter [Nachrichten mit Anlagen werden nicht übermittelt, wenn die dynamische Bereitstellung von ATP und](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery) des Ausweises verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e969-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="3e969-142">Mit [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md)verSchlüsselte Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3e969-142">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>


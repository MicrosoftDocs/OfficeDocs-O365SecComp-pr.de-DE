---
title: Dynamische Übermittlung und Anzeigen der Vorschau mit Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Wenn Sie Ihre ATP sichere Anlagen Richtlinien eingerichtet haben, wählen Sie dynamische Übermittlung Nachricht Verzögerungen bei der vermieden, und aktivieren Personen für die Vorschau von Anlagen, die gescannt werden.
ms.openlocfilehash: 95c270e871c3febb13eef8c4374d996fc763315b
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769829"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="5c580-103">Dynamische Übermittlung und Anzeigen der Vorschau mit Office 365 ATP sichere Anlagen</span><span class="sxs-lookup"><span data-stu-id="5c580-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="5c580-p101">**Zusammenfassung**: Dynamische Übermittlung ist eine Option, die für [Sichere Anlagen ATP](atp-safe-attachments.md)ausgewählt werden kann. In diesem Artikel erfahren Sie mehr über dynamische Übermittlung und Anlage Preview-Funktionen in [ATP sichere Anlagen in Office 365](atp-safe-attachments.md)zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5c580-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="5c580-p102">Wenn [Richtlinien ATP sichere Anlagen eingerichtet sind](set-up-atp-safe-attachments-policies.md) für Ihre Organisation mehrere Optionen für die Behandlung von e-Mail-Anlagen vorhanden sind. Dazu gehören **Blockieren**, **Ersetzen**und **Dynamische Übermittlung**. Je nach der Richtlinien für sichere Anlagen ATP Konfiguration möglicherweise e-Mail-Empfänger eine geringfügige Verzögerung in e-Mail-Übermittlung bemerken, wenn deren Anhänge überprüft werden. Wählen Sie zum Vermeiden von Nachricht verzögert **Dynamische Übermittlung**.</span><span class="sxs-lookup"><span data-stu-id="5c580-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="5c580-110">Funktionsweise von dynamische Übermittlung</span><span class="sxs-lookup"><span data-stu-id="5c580-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="5c580-p103">Dynamische Übermittlung entfällt e-Mail Verzögerungen durch den Textkörper einer e-Mail-Nachricht über an den Empfänger mit einem Platzhalter für jede e-Mail-Anlage senden. Der Platzhalter bleibt, bis eine Kopie der Anlage überprüft und sicher durch [ATP sichere Anlagen](atp-safe-attachments.md)bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="5c580-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="5c580-113">Jede Anlage deaktiviert ist, steht er öffnen oder herunterladen.</span><span class="sxs-lookup"><span data-stu-id="5c580-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="5c580-114">Wenn eine Anlage böswilligen werden bestimmt wird, wird es zur Quarantäne, gesendet, in dem eine Person in Ihrer Organisation Security Team (wie ein globaler Office 365-Administrator oder Sicherheitsadministrator) können [Nachrichten in Quarantäne in Office 365 verwalten](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="5c580-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="5c580-p104">Die meisten PDF-Dateien und Office während ATP Überprüfung ausgeführt wird, können Dokumente im abgesicherten Modus angezeigt werden. Wenn eine Anlage nicht kompatibel mit der dynamischen Delivery-Vorschau ist, sehen erst, e-Mail-Empfänger einen Anlage Platzhalter ATP sichere Anlagen Überprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5c580-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

<span data-ttu-id="5c580-117">Mit der dynamischen Übermittlung Personen gelesen und reagieren auf ihre e-Mail-Nachrichten sofort, während die Anlagen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="5c580-117">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="5c580-p105">ATP sichere Anlagen scannen akzeptiert platzieren im selben Bereich, in dem sich Ihre Office 365-Daten befinden. Weitere Informationen zum Data Center Geografie, finden Sie unter [, wo wird Ihre Daten befinden?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="5c580-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="5c580-120">Was geschieht, wenn jemand einer e-Mail, weiterleitet enthält eine Anlage?</span><span class="sxs-lookup"><span data-stu-id="5c580-120">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="5c580-p106">Nehmen Sie an, dass eine Organisation dynamische Übermittlung für die [sichere Anlagen ATP-Richtlinie](set-up-atp-safe-attachments-policies.md), und eine Person empfängt eine e-Mail, die eine Anlage enthält. Nun nehmen Sie an die Person die e-Mail-Nachricht an eine andere Person weiterleitet. Was ist los? Das hängt davon ab, ob die zusätzliche Empfänger in ATP sichere Anlagen Richtlinien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5c580-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="5c580-125">Wenn Sie ein Empfänger über eine sichere Anlagen ATP-Richtlinie mit der Option dynamische Übermittlung sind, sieht der Empfänger den Platzhalter die Möglichkeit, kompatible Dateien eine Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c580-125">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="5c580-126">Wenn Sie ein Empfänger nicht durch eine Richtlinie ATP sichere Anlagen behandelt wird, werden dann der e-Mail- und die Anlage, ohne ATP sichere Anlagen scannen oder Anlage Platzhalter durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5c580-126">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="5c580-127">Erforderlich für dynamische Übermittlung funktioniert?</span><span class="sxs-lookup"><span data-stu-id="5c580-127">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="5c580-128">Ihre Organisation muss [Office 365 erweiterte Schutz](office-365-atp.md) verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c580-128">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="5c580-129">Richtlinien müssen für sichere ATP-Anlagen mit der Option dynamische Übermittlung (finden Sie unter [Set up ATP sichere Anlagen Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)) definiert werden</span><span class="sxs-lookup"><span data-stu-id="5c580-129">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="5c580-130">E-Mail von Ihrer Organisation muss in Office 365 gehostet werden</span><span class="sxs-lookup"><span data-stu-id="5c580-130">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="5c580-131">Gibt es Szenarien für die dynamische Übermittlung nicht verfügbar ist?</span><span class="sxs-lookup"><span data-stu-id="5c580-131">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="5c580-p107">Es gibt bestimmte Szenarien, in denen dynamische Übermittlung nicht unterstützt wird. Hierzu gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5c580-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="5c580-134">E-Mail-Nachrichten in öffentlichen Ordnern</span><span class="sxs-lookup"><span data-stu-id="5c580-134">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="5c580-135">E-Mail-Nachrichten, die nicht weitergeleitet werden und dann wieder in das Postfach des Benutzers mithilfe von benutzerdefinierten Regeln</span><span class="sxs-lookup"><span data-stu-id="5c580-135">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="5c580-136">E-Mail-Nachrichten (automatisch oder manuell) aus dem gehosteten Postfach und in anderen Standorten, einschließlich Archivordner verschoben werden</span><span class="sxs-lookup"><span data-stu-id="5c580-136">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="5c580-137">E-Mail-Nachrichten, die gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="5c580-137">Email messages that are deleted</span></span>
    
- <span data-ttu-id="5c580-138">Ordner eines Benutzers Postfach suchen, die in einen fehlerhaften Zustand befindet</span><span class="sxs-lookup"><span data-stu-id="5c580-138">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="5c580-p108">Umgebungen, in denen ein Exchange Online-Administrator Exclaimer aktiviert hat. Um dieses Problem zu beheben, finden Sie unter [Nachrichten mit Anlagen werden nicht zugestellt werden, wenn ATP dynamische Übermittlung und Exclaimer verwendet werden](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="5c580-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="5c580-141">Verschlüsselte Nachrichten mit [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="5c580-141">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>
    

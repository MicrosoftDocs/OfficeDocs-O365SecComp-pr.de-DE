---
title: E-Mail-Threading
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ca4823ecfc06ddc0ef6f6840ad55fec492ac472c
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030115"
---
# <a name="email-threading"></a><span data-ttu-id="dad71-102">E-Mail-Threading</span><span class="sxs-lookup"><span data-stu-id="dad71-102">Email threading</span></span>

<span data-ttu-id="dad71-103">Betrachten Sie eine e-Mail-Unterhaltung, die schon eine Weile geht.</span><span class="sxs-lookup"><span data-stu-id="dad71-103">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="dad71-104">In den meisten Fällen enthält die letzte e-Mail des Threads den Inhalt aller vorhergehenden e-Mails. durch das Überprüfen der letzten e-Mail erhalten Sie einen vollständigen Kontext der Unterhaltung im Thread.</span><span class="sxs-lookup"><span data-stu-id="dad71-104">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="dad71-105">E-Mail-Threading identifiziert solche e-Mails, sodass Prüfer einen Bruchteil der gesammelten Dokumente überarbeiten können, ohne dass ein Kontext verloren geht.</span><span class="sxs-lookup"><span data-stu-id="dad71-105">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="dad71-106">Was bewirkt die e-Mail-Threading?</span><span class="sxs-lookup"><span data-stu-id="dad71-106">What does email threading do?</span></span>

<span data-ttu-id="dad71-107">E-Mail-Threading analysiert jede e-Mail und desconstructs Sie an einzelne Nachrichten. jede e-Mail ist eine Kette von einzelnen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dad71-107">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="dad71-108">Dann analysiert sie alle e-Mails im Arbeitssatz, um zu bestimmen, ob eine e-Mail eindeutige Inhalte enthält oder ob die Kette vollständig in einer anderen e-Mail enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dad71-108">Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="dad71-109">Am Ende werden e-Mails in vier Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="dad71-109">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="dad71-110">**Inclusive**: die letzte Nachricht in der e-Mail hat eindeutige Inhalte, und die e-Mail verfügt über alle Anhänge, die in anderen e-Mails enthalten waren, von denen der Inhalt vollständig in dieser e-Mail enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dad71-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="dad71-111">**Inklusive minus**: die letzte Nachricht in der e-Mail hat eindeutige Inhalte, aber die e-Mail enthält nicht einige der Anhänge, die in anderen e-Mails enthalten waren, von denen der Inhalt vollständig in dieser e-Mail enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dad71-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="dad71-112">**Inklusive Kopie**: eine exakte Kopie einer inklusive/inklusive minus-e-Mail</span><span class="sxs-lookup"><span data-stu-id="dad71-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="dad71-113">**None**: der Inhalt dieser e-Mail ist vollständig in mindestens einer e-Mail enthalten, die als inclusive/inklusive minus gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="dad71-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="dad71-114">Wie unterscheidet sich das von Outlook?</span><span class="sxs-lookup"><span data-stu-id="dad71-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="dad71-115">Auf einen Blick klingt dies sehr ähnlich wie Konversations Gruppierungen in Outlook.</span><span class="sxs-lookup"><span data-stu-id="dad71-115">At a glance, this sounds very similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="dad71-116">Es gibt jedoch einige wichtige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="dad71-116">However, there are some important distinctions.</span></span> <span data-ttu-id="dad71-117">Betrachten Sie eine e-Mail-Unterhaltung, die in zwei Unterhaltungen verzweigt wurde; Beispielsweise hat jemand auf eine e-Mail geantwortet, die nicht die neueste in der Unterhaltung ist, sodass die letzten beiden e-Mails in der Unterhaltung einen eindeutigen Inhalt aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dad71-117">Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="dad71-118">Outlook würde die e-Mails weiterhin in einer einzigen Unterhaltung gruppieren; das Lesen der letzten e-Mail würde bedeuten, dass der Kontext der letzten e-Mail, die auch eindeutigen Inhalt enthält, fehlt.</span><span class="sxs-lookup"><span data-stu-id="dad71-118">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="dad71-119">Da e-Mail-Threading jede e-Mail in einzelne Komponenten auswertet und vergleicht, würde das e-Mail-Threading beide der letzten beiden e-Mails als inclusive markieren, um sicherzustellen, dass Sie keinen Kontext verpassen, solange Sie alle als inclusive markierten e-Mails lesen.</span><span class="sxs-lookup"><span data-stu-id="dad71-119">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
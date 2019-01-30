---
title: Threading-e-Mail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 2340128f508a3be389afce86596f7e6395a0bb7e
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607809"
---
# <a name="email-threading"></a><span data-ttu-id="497da-102">Threading-e-Mail</span><span class="sxs-lookup"><span data-stu-id="497da-102">Email threading</span></span>
<span data-ttu-id="497da-p101">Erwägen Sie eine e-Mail-Unterhaltung, die für eine Weile schon hat. In den meisten Fällen muss die letzte e-Mail auf dem Thread den Inhalt aller vorherigen e-Mails enthalten; So überprüfen Sie die letzte e-Mail erhalten einen vollständigen Kontext der Unterhaltung, die im Thread erfolgt. Derartige e-Mails threading-e-Mail identifiziert werden, so dass Bearbeiter einen Bruchteil gesammelten Dokumente überprüfen können, ohne zu einem beliebigen Kontext verlieren.</span><span class="sxs-lookup"><span data-stu-id="497da-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="497da-106">Was macht threading-e-Mail?</span><span class="sxs-lookup"><span data-stu-id="497da-106">What does email threading do?</span></span>
<span data-ttu-id="497da-p102">E-Mail-threading jede e-Mail- und Desconstructs analysiert, um einzelne Nachrichten; Jede e-Mail ist eine Kette von einzelnen Nachrichten. Klicken Sie dann, analysiert alle e-Mails des Arbeitssatzes, um zu bestimmen, ob eine e-Mail-Nachricht eindeutig Inhalt aufweist oder ob die Kette vollständig in eine andere e-Mail-Adresse enthalten ist. Am Ende sind-e-Mails in vier Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="497da-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>
- <span data-ttu-id="497da-110">Inclusives: die letzte Nachricht in der e-Mail eindeutigen Inhalt und die e-Mail-Nachricht hat alle Anlagen, die in anderen e-Mails enthalten waren, von denen die Inhalte vollständig in dieser e-Mail enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="497da-110">Inclusives: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="497da-111">Minus inklusive: die letzte Meldung in der e-Mail hat eindeutige Inhalt, die e-Mail enthält jedoch keine einige der Anlagen, die in anderen e-Mails enthalten waren, von denen die Inhalte vollständig in diese e-Mail enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="497da-111">Inclusive minus: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="497da-112">Inklusive Kopie: eine genaue Kopie eines inklusive/inklusive minus e-Mail</span><span class="sxs-lookup"><span data-stu-id="497da-112">Inclusive copy: an exact copy of an inclusive/inclusive minus email</span></span>
- <span data-ttu-id="497da-113">None: Der Inhalt dieser e-Mail ist vollständig in mindestens eine e-Mail-Nachricht enthalten, die als inklusive/inklusive Minuszeichen gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="497da-113">None: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="497da-114">Wie ist es sich von Unterhaltungen in Outlook?</span><span class="sxs-lookup"><span data-stu-id="497da-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="497da-p103">Auf einen Blick hört Unterhaltung Gruppen in Outlook sehr ähnlich. Es gibt jedoch einige wichtige Unterschiede. Verwenden Sie eine e-Mail-Unterhaltung, die in zwei Unterhaltung verzweigt, haben Sie; beispielsweise geantwortet einer Person an eine e-Mail, die nicht die neuesten in der Unterhaltung ist, sodass die letzten beiden e-Mails in der Unterhaltung sowohl eindeutigen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="497da-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="497da-p104">Outlook wird weiterhin die e-Mails in einem einzelnen Gespräch Gruppe; nur die letzte e-Mail-Nachrichten lesen bedeutet fehlende im Kontext der e-Mail vorletzten, die auch eindeutigen Inhalt enthält. Da threading-e-Mail, jede e-Mail in einzelne Komponenten analysiert und miteinander verglichen, würde threading-e-Mail-Markieren beider die letzten beiden e-Mails als Inclusives, um sicherzustellen, dass Sie alle Kontext verpassen, solange Sie alle e-Mails als inklusive markiert gelesen.</span><span class="sxs-lookup"><span data-stu-id="497da-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>
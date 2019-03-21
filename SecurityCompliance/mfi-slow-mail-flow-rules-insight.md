---
title: Einblick für langsame Nachrichtenflussregeln
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Administratoren erfahren mehr über die langsamen Nachrichtenfluss Regeln im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center.
ms.openlocfilehash: e1ce23c94cd5260d8a7a7ebd99521a4a6f5c7b0a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720255"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="ac8fd-103">Einblick für langsame Nachrichtenflussregeln</span><span class="sxs-lookup"><span data-stu-id="ac8fd-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="ac8fd-104">Ineffiziente Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) können zu Verzögerungen bei der Nachrichtenübermittlung für Ihre Organisation führen.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="ac8fd-105">Dieser Einblick meldet Nachrichtenfluss Regeln, die sich auf den Nachrichtenfluss Ihrer Organisation auswirken.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="ac8fd-106">Beispiele für diese Regeln sind:</span><span class="sxs-lookup"><span data-stu-id="ac8fd-106">Examples of these types of rules are:</span></span>

- <span data-ttu-id="ac8fd-107">Bedingungen, die für umfangreiche Gruppen **Mitglied sind** .</span><span class="sxs-lookup"><span data-stu-id="ac8fd-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="ac8fd-108">Bedingungen, die einen komplexen regulären Ausdruck (Regex)-Mustervergleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="ac8fd-109">Bedingungen, die die Inhaltsüberprüfung in Anlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="ac8fd-110">Die Einblicke helfen Ihnen bei der Identifizierung und Optimierung von Nachrichtenfluss Regeln, um die Verzögerungen bei der Nachrichtenübermittlung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Eine langsame Nachrichtenfluss Regel Einblicke in das Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="ac8fd-112">Wenn Sie auf **Details anzeigen**klicken, wird ein Flyout-Bereich angezeigt, in dem Sie die Regel überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-112">When you click **View details**, a flyout pane appears where you can review the rule.</span></span> <span data-ttu-id="ac8fd-113">Klicken Sie im Flyoutbereich auch auf **Beispiel Nachrichten anzeigen** , um zu sehen, welche Art von Nachrichten von der Regel betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="ac8fd-113">In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![Flyout-Bereich nach dem Klicken auf Details anzeigen in einem langsamen Nachrichtenfluss Regeln Einblicke in das Nachrichtenfluss-Dashboard](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

## <a name="see-also"></a><span data-ttu-id="ac8fd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac8fd-115">See also</span></span>

<span data-ttu-id="ac8fd-116">Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights.md).</span><span class="sxs-lookup"><span data-stu-id="ac8fd-116">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights.md).</span></span>

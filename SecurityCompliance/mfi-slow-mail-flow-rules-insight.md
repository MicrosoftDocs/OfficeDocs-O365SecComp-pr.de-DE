---
title: Langsame Mail Flow Regeln Erkenntnisse
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Administratoren können über die langsame Mail Flow Regeln Einblicke im Dashboard Mail Flow in die Sicherheit in Office 365 Compliance Center & informieren.
ms.openlocfilehash: 930ea7c57d896c75c6af1333f2bf202b56270199
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685457"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="8e7c5-103">Langsame Mail Flow Regeln Erkenntnisse</span><span class="sxs-lookup"><span data-stu-id="8e7c5-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="8e7c5-p101">Ineffiziente e-Mail-Flussregeln (auch als Transportregeln bezeichnet) können zu Mail Flow Verzögerungen für Ihre Organisation führen. Diese Erkenntnisse meldet e-Mail-Flussregeln, die auf Ihrer Organisation e-Mail-Fluss auswirken. Beispiele für diese Art von Regeln sind:</span><span class="sxs-lookup"><span data-stu-id="8e7c5-p101">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization. This insight reports mail flow rules that have an impact on your organization's mail flow. Examples of these types of rules are:</span></span>

- <span data-ttu-id="8e7c5-107">Bedingungen, die **Mitglied ist** für große Gruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="8e7c5-108">Bedingungen, die komplexe reguläre Ausdrücke (Regex) Mustervergleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="8e7c5-109">Bedingungen, mit denen Inhalt in Anlagen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="8e7c5-110">Die Einblicke helfen Ihnen zu identifizieren und e-Mail-Flussregeln zur Verringerung von e-Mail-Fluss Verzögerungen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Ein langsame e-Mail-Fluss Regeln Erkenntnisse im Dashboard Mail Flow in der Office 365-Sicherheit & Compliance Center](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="8e7c5-p102">Wenn Sie auf **Details anzeigen**klicken, wird ein Dropdown-Bereich, in dem Sie die Regel überprüfen können. Klicken Sie im Bereich flyoutmenü können klicken **Beispiel Meldungen** , um herauszufinden, welche Art von Nachrichten von der Regel betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="8e7c5-p102">When you click **View details**, a flyout pane appears where you can review the rule. In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![Dropdown-Bereich nach dem Klicken auf Details anzeigen bei einer langsamen Nachrichtenübermittlung Regeln Einblicke in die e-Mail-Fluss-dashboard](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

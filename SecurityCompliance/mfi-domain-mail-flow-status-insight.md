---
title: Übersicht über die Nachrichtenflussstatus der oberen Domäne
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren können sich über den Status des Nachrichtenflusses im Nachrichtenfluss-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: 851ef1438f111a36f69563670bbd0835a9956edc
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868591"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="e4935-103">Übersicht über die Nachrichtenflussstatus der oberen Domäne</span><span class="sxs-lookup"><span data-stu-id="e4935-103">Top domain mail flow status insight</span></span>

<span data-ttu-id="e4935-104">Die **Nachrichtenflussstatus-** Einblicke der oberen Domänen bieten Ihnen den aktuellen Status der Domänen Ihrer Organisation im Hinblick auf den Nachrichtenfluss.</span><span class="sxs-lookup"><span data-stu-id="e4935-104">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="e4935-105">Diese Einblicke helfen Ihnen bei der Identifizierung und Problembehandlung von Domänen, die Auswirkungen auf die ***Nachrichtenübermittlung*** haben (beispielsweise können keine externen e-Mails empfangen werden), insbesondere Domänen Ablauf oder Domänen mit falschen MX-Einträgen.</span><span class="sxs-lookup"><span data-stu-id="e4935-105">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![Die obere Domänen-Fluss Status Einblicke im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="e4935-107">Wenn Sie im Insight auf **Details anzeigen** klicken, wird ein Flyout angezeigt, in dem Sie weitere Details zum Status jeder Domäne sehen.</span><span class="sxs-lookup"><span data-stu-id="e4935-107">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="e4935-108">Ein grünes Häkchen für eine Domäne gibt den aktuellen MX-Eintrag an (wenn Sie zum Dashboard für Nachrichtenfluss Einblicke navigieren) entspricht dem Wert, den wir im Datensatz haben, und dass die Domäne während der letzten zwei Stunden e-Mails empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="e4935-108">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="e4935-109">Ein rotes x für eine Domäne gibt an, dass der MX-Eintrag geändert wurde und dass die Domäne während der letzten 6 Stunden keine e-Mails erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="e4935-109">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="e4935-110">Dies weist darauf hin, dass Ihre Domäne abgelaufen ist oder dass der MX-Eintrag falsch aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e4935-110">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="e4935-111">Erkundigen Sie sich bei Ihrer Domänenregistrierungsstelle oder Ihrem DNS-Hostingdienst, ob die Domäne abgelaufen ist oder ob der MX-Eintrag der Domäne falsch ist.</span><span class="sxs-lookup"><span data-stu-id="e4935-111">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![Das Detail Flyout im oberen Domänen-Fluss Status Einblicke](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="e4935-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4935-113">See also</span></span>

<span data-ttu-id="e4935-114">Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e4935-114">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>

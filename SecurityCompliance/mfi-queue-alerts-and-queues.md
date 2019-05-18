---
title: Warteschlangenwarnungen und Warteschlangen
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Administratoren können Informationen zu Warteschlangen Warnungen und Warteschlangen im Nachrichtenfluss-Dashboard im Security & Compliance Center erhalten.
ms.openlocfilehash: 149a1d82b3627037db2ab5c6e1427c79a49535bd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158757"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="b01d4-103">Warteschlangenwarnungen und Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="b01d4-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="b01d4-104">Warteschlangen Warnungen</span><span class="sxs-lookup"><span data-stu-id="b01d4-104">Queue alerts</span></span>

<span data-ttu-id="b01d4-105">Wenn Nachrichten nicht von Ihrer Office 365 Organisation an Ihre lokalen oder Partner-e-Mail-Server mithilfe von Connectors gesendet werden können, werden die Nachrichten in Office 365 in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="b01d4-105">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365.</span></span> <span data-ttu-id="b01d4-106">Häufige Beispiele, die diese Bedingung verursachen, sind:</span><span class="sxs-lookup"><span data-stu-id="b01d4-106">Common examples that cause this condition are:</span></span>

- <span data-ttu-id="b01d4-107">Der Connector ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b01d4-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="b01d4-108">In Ihrer lokalen Umgebung wurden Netzwerk-oder Firewall-Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="b01d4-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="b01d4-109">Office 365 wird die Zustellung für 48 Stunden fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b01d4-109">Office 365 will continue to retry to delivery for 48 hours.</span></span> <span data-ttu-id="b01d4-110">Nach 48 Stunden laufen die Nachrichten ab und werden an die Absender in Unzustellbarkeitsberichten (auch als Unzustellbarkeitsberichte oder Bounce-Nachrichten bezeichnet) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b01d4-110">After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="b01d4-111">Wenn das e-Mail-Volumen in der Warteschlange den vordefinierten Schwellenwert überschreitet (der Standardwert ist 2000 Nachrichten), sind die Warnungen im Nachrichtenfluss-Dashboard bei **den letzten Warnungen**verfügbar, und Administratoren erhalten eine e-Mail-Benachrichtigung (an Ihre alternative e-Mail-Adresse). .</span><span class="sxs-lookup"><span data-stu-id="b01d4-111">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address).</span></span> <span data-ttu-id="b01d4-112">Informationen zum Konfigurieren des warnungsschwellenwerts, des täglichen Benachrichtigungs Grenzwerts und/oder der Empfänger der Warnung finden Sie im Abschnitt **Anpassen von Warteschlangen Warnungen** weiter unten.</span><span class="sxs-lookup"><span data-stu-id="b01d4-112">To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Warteschlangen Warnungen im Bereich "zuletzt verwendete Benachrichtigungen" im Nachrichtenfluss-Dashboard im Security & Compliance Center](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="b01d4-114">Anpassen von Warteschlangen Warnungen</span><span class="sxs-lookup"><span data-stu-id="b01d4-114">Customize queue alerts</span></span>

<span data-ttu-id="b01d4-115">Einblicke in den Nachrichtenfluss erstellen eine Warnungs Richtlinie mit dem Namen " **Nachrichten wurden verzögert** (das Kontrollkästchen **e-Mail-Benachrichtigungen senden** " im Beispielbildschirm Screenshot unten) finden Sie unter **Alerts** \> **Alert Policies**.</span><span class="sxs-lookup"><span data-stu-id="b01d4-115">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**.</span></span> <span data-ttu-id="b01d4-116">Sie können den Schwellenwert und die Benachrichtigungsempfänger ändern, indem Sie auf die Richtlinie klicken.</span><span class="sxs-lookup"><span data-stu-id="b01d4-116">You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Warnungs Navigation](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="b01d4-118">Es wird ein neues Blade für Richtlinieninformationen angezeigt, und Sie können nun auf **Richtlinie bearbeiten**klicken.</span><span class="sxs-lookup"><span data-stu-id="b01d4-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Richtlinie bearbeiten ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="b01d4-120">Das Informationsblatt wird in die **Bearbeitungs Richtlinie**geändert.</span><span class="sxs-lookup"><span data-stu-id="b01d4-120">The information blade will change to the **Edit Policy**.</span></span> <span data-ttu-id="b01d4-121">Sie können nun die Empfänger für die Benachrichtigungs-e-Mail, den Grenzwert für die Anzahl der pro Tag gesendeten Benachrichtigungen und den minimalen Schwellenwert für die Auslösung der Warnung ändern (200 oder mehr).</span><span class="sxs-lookup"><span data-stu-id="b01d4-121">You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Bearbeiten des Richtlinien Blatts](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="b01d4-123">Warnungsdetails für Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="b01d4-123">Queue alert details</span></span>

<span data-ttu-id="b01d4-124">Wenn Sie auf die Warnung klicken, werden die Warnungsdetails in einem Flyout-Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b01d4-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Auswählen einer Warteschlangen Warnung im Bereich "zuletzt verwendete Benachrichtigungen" im Nachrichtenfluss-Dashboard im Security & Compliance Center](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Das Flyout "Details zur Warteschlangen Warnung" im Security & Compliance Center](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="b01d4-127">Sie können in den Warnungsdetails auf **Warteschlange anzeigen** klicken, um die Warteschlangendetails, Probleme und Links zu den verfügbaren Korrekturen in einem neuen Flyout-Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b01d4-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Das Flyout "Details zur Warteschlangen Warnung" im Security & Compliance Center](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Warteschlange in den Warnungsdetails anzeigen](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="b01d4-130">Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="b01d4-130">Queues</span></span>

<span data-ttu-id="b01d4-131">Auch wenn das Nachrichten Volume in der Warteschlange den Schwellenwert nicht überschreitet, können Sie weiterhin den Bereich **Warteschlangen** im Nachrichtenfluss-Dashboard verwenden, um Nachrichten anzuzeigen, die länger als eine Stunde in die Warteschlange gestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b01d4-131">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour.</span></span> <span data-ttu-id="b01d4-132">Sie können den Bereich **warte** Schlangen verwenden, um die Anzahl der in der Warteschlange befindlichen Nachrichten zu überwachen (der Wert 0 gibt an, dass der Nachrichtenfluss ordnungsgemäß ist), und es wird eine Aktion ausgeführt, bevor die Anzahl der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b01d4-132">You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Warteschlangen im Nachrichtenfluss-Dashboard im Security & Compliance Center](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="b01d4-134">Wenn Sie auf die Anzahl der Warteschlangen Nachrichten in **warte**Schlangen klicken, werden die Warteschlangendetails und Anleitungen für die Behebung des Problems in einem Flyout-Bereich angezeigt (dasselbe Flyout, das angezeigt wird, nachdem Sie im Detail einer Warteschlangen Warnung auf **Warteschlange anzeigen** klicken).</span><span class="sxs-lookup"><span data-stu-id="b01d4-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Warteschlangendetails](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="see-also"></a><span data-ttu-id="b01d4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b01d4-136">See also</span></span>

<span data-ttu-id="b01d4-137">Weitere Informationen zu anderen e-Mail-Fluss-Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Mail Flow Insights in the Security & Compliance Center](mail-flow-insights.md).</span><span class="sxs-lookup"><span data-stu-id="b01d4-137">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights.md).</span></span>

---
title: Warteschlange Warnungen und Warteschlangen
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Administratoren können über Warteschlange Warnungen und Warteschlangen im Dashboard Mail Flow in die Sicherheit in Office 365 Compliance Center & informieren.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685463"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="5c981-103">Warteschlange Warnungen und Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="5c981-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="5c981-104">Warteschlange Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5c981-104">Queue alerts</span></span>

<span data-ttu-id="5c981-p101">Wenn Nachrichten an Ihre lokale von Office 365-Organisation gesendet werden können oder Partner e-Mail-Servern mithilfe von Connectors, werden die Nachrichten in Office 365 in der Warteschlange. Sind gängige Beispiele, die diese Bedingung verursachen:</span><span class="sxs-lookup"><span data-stu-id="5c981-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="5c981-107">Der Verbindung ist nicht richtig konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5c981-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="5c981-108">Netzwerke oder der Firewall geändert wurden in Ihrer lokalen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5c981-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="5c981-p102">Office 365 wird weiterhin bis hin zur Bereitstellung für 48 Stunden wiederholen. Nach 48 Stunden, die Nachrichten läuft und an die Absender in Unzustellbarkeitsberichte zurückgegeben (auch bekannt als eine Unzustellbarkeitsberichte oder aufprallen Nachrichten).</span><span class="sxs-lookup"><span data-stu-id="5c981-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="5c981-p103">Wenn das Volume e-Mail in der Warteschlange den vordefinierten Schwellenwert überschreitet (der Standardwert ist 2000-Nachrichten), Benachrichtigungen werden in der e-Mail-Fluss Dashboard am **letzten**verfügbar sein, und Administratoren erhalten eine e-Mail-Benachrichtigung (an ihre alternative e-Mail-Adresse) . Konfigurieren der Warnschwellenwert, tägliche Benachrichtigung Grenzwert und/oder Empfänger der Warnung finden Sie weiter unten im Abschnitt **Anpassen Warteschlange Warnungen** .</span><span class="sxs-lookup"><span data-stu-id="5c981-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Warteschlange Warnungen im Bereich zuletzt verwendete Benachrichtigungen des Dashboards Mail Flow in der Office 365-Sicherheit & Compliance Center](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="5c981-114">Anpassen der Warteschlange Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5c981-114">Customize queue alerts</span></span>

<span data-ttu-id="5c981-p104">Mail Flow Insights erstellen Sie eine Warnung Richtlinie benannten **Nachrichten verzögert wurden** ( **senden e-Mail-Benachrichtigungen** das Kontrollkästchen in der Beispiel-Screenshot) **Benachrichtigungen** gefunden \> **Benachrichtigung Richtlinien**. Sie können den Schwellenwert und Benachrichtigung Empfänger geändert werden, indem Sie auf die Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5c981-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Alerts-Navigation](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="5c981-118">Sehen Sie einen neue Richtlinie Informationen Blade, Sie können nun auf **Richtlinie bearbeiten**klicken.</span><span class="sxs-lookup"><span data-stu-id="5c981-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Richtlinie bearbeiten ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="5c981-p105">Das Informationen Blade ändert sich der **Richtlinie bearbeiten**. Sie können jetzt die Empfänger für die Warnung e-Mails, die den Grenzwert für die Anzahl der Benachrichtigungen gesendet pro Tag und den kleinsten Schwellenwert zum Auslösen der Benachrichtigung (200 oder mehr) ändern.</span><span class="sxs-lookup"><span data-stu-id="5c981-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Richtlinie Blade bearbeiten](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="5c981-123">Warteschlange Warnungsdetails</span><span class="sxs-lookup"><span data-stu-id="5c981-123">Queue alert details</span></span>

<span data-ttu-id="5c981-124">Wenn Sie die Benachrichtigung klicken, werden die Details der Warnung in einem Dropdown-Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c981-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Wählen Sie eine Warteschlange Warnung im Bereich zuletzt verwendete Benachrichtigungen des Dashboards Mail Flow in der Office 365-Sicherheit & Compliance Center](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Die Warteschlange alert Details flyoutmenü in der Office 365-Sicherheit & Compliance Center](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="5c981-127">Sie können in den Warnungsdetails an die Warteschlange Details, Probleme und Links zu verfügbaren Updates in einen neuen Fensterausschnitt flyoutmenü finden Sie unter **Warteschlange anzeigen** klicken.</span><span class="sxs-lookup"><span data-stu-id="5c981-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Die Warteschlange alert Details flyoutmenü in der Office 365-Sicherheit & Compliance Center](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Warteschlange in den Warnungsdetails anzeigen](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="5c981-130">Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="5c981-130">Queues</span></span>

<span data-ttu-id="5c981-p106">Auch wenn die Nachricht in der Warteschlange Lautstärke des Schwellenwerts noch nicht weiterhin können Sie Bereich **Warteschlangen** des e-Mail-Fluss Dashboards Nachrichten anzuzeigen, die für mehr als eine Stunde zurückgestellt wurden. Den Bereich **Warteschlangen** können Sie überwachen die Anzahl der Nachrichten in der Warteschlange (der Wert 0 gibt an, dass e-Mail-Fluss OK ist) und Maßnahmen ergreifen, bevor die Anzahl der Nachrichten in der Warteschlange zu groß wird.</span><span class="sxs-lookup"><span data-stu-id="5c981-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Warteschlangen im Dashboard Mail Flow in der Office 365-Sicherheit & Compliance Center](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="5c981-134">Wenn Sie die Anzahl der Nachrichten in **Warteschlangen**, die Warteschlange-Details in der Warteschlange klicken, und Richtlinien zum Beheben des Problems in einem Dropdown-Bereich (der gleichen flyoutmenü, die angezeigt wird, klicken Sie in den Details einer Warteschlange Warnung **Warteschlange anzeigen** ) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c981-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Warteschlange-details](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

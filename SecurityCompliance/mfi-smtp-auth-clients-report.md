---
title: SMTP-Authentifizierungsclients (Bericht)
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren können sich über den Bericht über SMTP-Authentifizierungsclients im Nachrichtenfluss-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: fde5be59e2b8a86b2bac6fc793293d8887670746
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158597"
---
# <a name="smtp-auth-clients-report"></a><span data-ttu-id="db79e-103">SMTP-Authentifizierungsclients (Bericht)</span><span class="sxs-lookup"><span data-stu-id="db79e-103">SMTP Auth clients report</span></span>

<span data-ttu-id="db79e-104">Der Bericht über **SMTP-Authentifizierungsclients** zeigt die Verwendung des SMTP-Authentifizierungs Client-Übermittlungsprotokolls durch Benutzer oder Systemkonten in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="db79e-104">The **SMTP Auth clients** report highlights the use of the SMTP Auth client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="db79e-105">Dieses Legacy Protokoll (das den Endpunkt SMTP.office365.com verwendet) bietet nur die Standardauthentifizierung und ist anfällig für die Verwendung durch kompromittierte Konten zum Senden von e-Mails.</span><span class="sxs-lookup"><span data-stu-id="db79e-105">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span>  <span data-ttu-id="db79e-106">In diesem Bericht können Sie nach ungewöhnlichen Aktivitäten suchen.</span><span class="sxs-lookup"><span data-stu-id="db79e-106">This report allows you to check for unusual activity.</span></span> <span data-ttu-id="db79e-107">Außerdem werden die TLS-Nutzungsdaten für Clients oder Geräte mithilfe der SMTP-Authentifizierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db79e-107">It also shows the TLS usage data for clients or devices using SMTP Auth.</span></span>

<span data-ttu-id="db79e-108">Das Widget, das im Nachrichtenfluss-Dashboard angezeigt wird, gibt die Anzahl der Benutzer oder Dienstkonten an, die in den letzten 7 Tagen das SMTP-Authentifizierungsprotokoll verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="db79e-108">The widget that's shown in the Mail Flow dashboard indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Der Bericht über SMTP-Authentifizierungsclients im Nachrichtenfluss-Dashboard im Security & Compliance Center](media/smtp-auth-clients-report-selected.png)

<span data-ttu-id="db79e-110">Durch Klicken auf das Widget wird ein Flyout geöffnet, das eine aggregierte Ansicht der TLS-Nutzung und-Volumes für die letzte Woche enthält.</span><span class="sxs-lookup"><span data-stu-id="db79e-110">Clicking on the widget opens a flyout that provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Das Flyout im Bericht "SMTP AUTH Clients"](media/smtp-auth-clients-flyout.png)

<span data-ttu-id="db79e-112">Wenn Sie auf den Link **SMTP AUTH Clients Report** klicken, werden zwei Hauptdaten Pivots und zwei Datenansichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db79e-112">When you click on the **SMTP Auth Clients Report** link, you'll see two main data pivots and two data views.</span></span> <span data-ttu-id="db79e-113">Die Daten Pivots sind das **sendende Volume** und die **TLS-Verwendung**.</span><span class="sxs-lookup"><span data-stu-id="db79e-113">The data pivots are the **Sending Volume** and **TLS Usage**.</span></span> <span data-ttu-id="db79e-114">Die Datenansichten sind das Diagramm und die Detailtabelle.</span><span class="sxs-lookup"><span data-stu-id="db79e-114">The data views are the chart and the details table.</span></span>

<span data-ttu-id="db79e-115">Die Ansicht **sendende Volumes** zeigt die Anzahl der Nachrichten an, die mit SMTP-Authentifizierung für den angegebenen Zeitraum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="db79e-115">The **Sending Volume** view shows the number of messages that were sent using SMTP Auth for the specified time range.</span></span> <span data-ttu-id="db79e-116">Sie können den Bereich anpassen, indem Sie auf **Filter**klicken.</span><span class="sxs-lookup"><span data-stu-id="db79e-116">You can adjust the range by clicking **Filters**.</span></span> <span data-ttu-id="db79e-117">Das Diagramm ist nach Absenderdomäne organisiert.</span><span class="sxs-lookup"><span data-stu-id="db79e-117">The chart is organized by sender domain.</span></span> <span data-ttu-id="db79e-118">Sie können separate Daten für jede Domäne anzeigen, indem Sie die Domäne in der Dropdownliste **Daten anzeigen für** auswählen.</span><span class="sxs-lookup"><span data-stu-id="db79e-118">You can see separate data for each domain by selecting the domain in the **Show data for** drop down.</span></span>

![Senden des Volumes im Bericht "SMTP AUTH Clients"](media/smtp-auth-clients-report-sending-volume.png)

<span data-ttu-id="db79e-120">Sie können detaillierte Informationen zu den Absendern und ihren Nachrichten Zählern anzeigen, indem Sie auf **Tabelle Details anzeigen**klicken.</span><span class="sxs-lookup"><span data-stu-id="db79e-120">You can view detailed information about the senders and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="db79e-121">Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="db79e-121">To return to the chart, click **View report**.</span></span>

![Tabelle "Details" für das Senden des Volumes im Bericht "SMTP AUTH Clients"](media/smtp-auth-clients-report-details-sending-volume.png)

<span data-ttu-id="db79e-123">Der **TLS-Verwendungs** Pivot ist aufgrund der bevorstehenden veralteten Version von TLS 1.0 und TLS 1.1 in Office 365 wichtig.</span><span class="sxs-lookup"><span data-stu-id="db79e-123">The **TLS Usage** pivot is important due to the upcoming deprecation of TLS1.0 and TLS1.1 in Office 365.</span></span> <span data-ttu-id="db79e-124">Viele ältere Geräte und Anwendungen können keine e-Mails senden, wenn Sie nur TLS 1.0 mit SMTP-Authentifizierung verwenden können. Mit diesem Pivot können Sie Benutzer und Systemkonten identifizieren und ausführen, die noch ältere Versionen von TLS verwenden.</span><span class="sxs-lookup"><span data-stu-id="db79e-124">Many legacy devices and applications will be unable to send email if they are only capable of using TLS1.0 with SMTP Auth. This pivot allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

![TLS-Verwendung im Bericht "SMTP AUTH Clients"](media/smtp-auth-clients-report-tls-usage.png)

<span data-ttu-id="db79e-126">Sie können detaillierte Informationen über die Absender, die Versionen von TLS, die Sie mit SMTP-Authentifizierung verwenden, und deren Nachrichtenanzahl anzeigen, indem Sie auf **Detailtabelle anzeigen**klicken.</span><span class="sxs-lookup"><span data-stu-id="db79e-126">You can view detailed information about the senders, the versions of TLS they are using with SMTP Auth, and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="db79e-127">Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="db79e-127">To return to the chart, click **View report**.</span></span>

<span data-ttu-id="db79e-128">Sie können auch eine detailliertere Version des Berichts herunterladen, indem Sie auf Anforderungsbericht klicken.</span><span class="sxs-lookup"><span data-stu-id="db79e-128">You can also download a more detailed version of the report by clicking Request report.</span></span>

![Tabelle "Details" für die TLS-Verwendung im Bericht "SMTP AUTH Clients"](media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a><span data-ttu-id="db79e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db79e-130">See also</span></span>

<span data-ttu-id="db79e-131">Weitere Informationen zu anderen e-Mail-Fluss-Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="db79e-131">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>

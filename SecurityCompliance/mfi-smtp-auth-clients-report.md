---
title: Bericht über SMTP-AUTH-Clients
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren erfahren mehr über den Bericht über SMTP-AUTH-Clients im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: b6698345a89edf52e4ee14cea144cb88ff080583
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252553"
---
# <a name="smtp-auth-clients-report"></a><span data-ttu-id="2f37e-103">Bericht über SMTP-AUTH-Clients</span><span class="sxs-lookup"><span data-stu-id="2f37e-103">SMTP Auth clients report</span></span>

> [!NOTE]
> <span data-ttu-id="2f37e-104">Die in diesem Thema beschriebenen Features wurden nicht für alle Office 365-Organisationen bereitgestellt und können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2f37e-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="2f37e-105">Im Bericht **SMTP AUTH Clients** wird die Verwendung des SMTP-AUTH-Client Übermittlungsprotokolls durch Benutzer oder Systemkonten in Ihrer Organisation hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="2f37e-105">The **SMTP Auth clients** report highlights the use of the SMTP Auth client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="2f37e-106">Dieses Legacy Protokoll (das den Endpunkt smtp.office365.com verwendet) bietet nur die Standardauthentifizierung und ist anfällig dafür, von kompromittierten Konten zum Senden von e-Mails verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="2f37e-106">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span>  <span data-ttu-id="2f37e-107">Mit diesem Bericht können Sie nach ungewöhnlichen Aktivitäten suchen.</span><span class="sxs-lookup"><span data-stu-id="2f37e-107">This report allows you to check for unusual activity.</span></span> <span data-ttu-id="2f37e-108">Außerdem werden die TLS-Verwendungsdaten für Clients oder Geräte mit SMTP-Authentifizierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f37e-108">It also shows the TLS usage data for clients or devices using SMTP Auth.</span></span>

<span data-ttu-id="2f37e-109">Das im e-Mail-Fluss-Dashboard angezeigte Widget gibt die Anzahl der Benutzer oder Dienstkonten an, die das SMTP-Authentifizierungsprotokoll in den letzten 7 Tagen verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2f37e-109">The widget that's shown in the Mail Flow dashboard indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Der Bericht über SMTP-AUTH-Clients im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center](media/smtp-auth-clients-report-selected.png)

<span data-ttu-id="2f37e-111">Wenn Sie auf das Widget klicken, wird ein Flyout geöffnet, das eine aggregierte Ansicht der TLS-Nutzung und-Volumes für die letzte Woche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2f37e-111">Clicking on the widget opens a flyout that provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Das Flyout im Bericht über SMTP-AUTH-Clients](media/smtp-auth-clients-flyout.png)

<span data-ttu-id="2f37e-113">Wenn Sie auf den Link **SMTP-AUTH-Clients melden** klicken, werden zwei Hauptdaten Pivots und zwei Datenansichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f37e-113">When you click on the **SMTP Auth Clients Report** link, you'll see two main data pivots and two data views.</span></span> <span data-ttu-id="2f37e-114">Die Daten Pivots sind die **sendelautstärke** und die **TLS-Verwendung**.</span><span class="sxs-lookup"><span data-stu-id="2f37e-114">The data pivots are the **Sending Volume** and **TLS Usage**.</span></span> <span data-ttu-id="2f37e-115">Die Datenansichten sind das Diagramm und die Detailtabelle.</span><span class="sxs-lookup"><span data-stu-id="2f37e-115">The data views are the chart and the details table.</span></span>

<span data-ttu-id="2f37e-116">Die **sendenDe Volumen** Ansicht zeigt die Anzahl der Nachrichten an, die über SMTP-Authentifizierung für den angegebenen Zeitraum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="2f37e-116">The **Sending Volume** view shows the number of messages that were sent using SMTP Auth for the specified time range.</span></span> <span data-ttu-id="2f37e-117">Sie können den Range anpassen, indem Sie auf **Filter**klicken.</span><span class="sxs-lookup"><span data-stu-id="2f37e-117">You can adjust the range by clicking **Filters**.</span></span> <span data-ttu-id="2f37e-118">Das Diagramm wird nach der Absenderdomäne organisiert.</span><span class="sxs-lookup"><span data-stu-id="2f37e-118">The chart is organized by sender domain.</span></span> <span data-ttu-id="2f37e-119">Sie können für jede Domäne separate Daten anzeigen, indem Sie die Domäne in der Dropdownliste **Daten anzeigen für** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f37e-119">You can see separate data for each domain by selecting the domain in the **Show data for** drop down.</span></span>

![Senden von Volumes im SMTP-AUTH-Clientbericht](media/smtp-auth-clients-report-sending-volume.png)

<span data-ttu-id="2f37e-121">Sie können detaillierte Informationen zu den Absendern und deren Anzahl von Nachrichten anzeigen, indem Sie auf **Details-Tabelle anzeigen**klicken.</span><span class="sxs-lookup"><span data-stu-id="2f37e-121">You can view detailed information about the senders and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="2f37e-122">Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2f37e-122">To return to the chart, click **View report**.</span></span>

![Details-Tabelle zum Senden von Volumes im SMTP-AUTH-Clientbericht](media/smtp-auth-clients-report-details-sending-volume.png)

<span data-ttu-id="2f37e-124">Die **TLS-Verwendungs** Pivot ist wichtig aufgrund der bevorstehenden veraltet von TLS 1.0 und TLS 1.1 in Office 365.</span><span class="sxs-lookup"><span data-stu-id="2f37e-124">The **TLS Usage** pivot is important due to the upcoming deprecation of TLS1.0 and TLS1.1 in Office 365.</span></span> <span data-ttu-id="2f37e-125">Viele ältere Geräte und Anwendungen können keine e-Mails senden, wenn Sie nur TLS 1.0 mit SMTP-Authentifizierung verwenden können. Mit diesem Pivot können Sie Benutzer und Systemkonten, die noch ältere Versionen von TLS verwenden, identifizieren und Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="2f37e-125">Many legacy devices and applications will be unable to send email if they are only capable of using TLS1.0 with SMTP Auth. This pivot allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

![TLS-Verwendung im Bericht über SMTP-AUTH-Clients](media/smtp-auth-clients-report-tls-usage.png)

<span data-ttu-id="2f37e-127">Sie können detaillierte Informationen über die Absender, die Versionen von TLS, die Sie mit SMTP-Authentifizierung verwenden, und ihre Nachrichtenanzahl anzeigen, indem Sie auf **Details anzeigen-Tabelle**klicken.</span><span class="sxs-lookup"><span data-stu-id="2f37e-127">You can view detailed information about the senders, the versions of TLS they are using with SMTP Auth, and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="2f37e-128">Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2f37e-128">To return to the chart, click **View report**.</span></span>

<span data-ttu-id="2f37e-129">Sie können auch eine detailliertere Version des Berichts herunterladen, indem Sie auf Bericht anfordern klicken.</span><span class="sxs-lookup"><span data-stu-id="2f37e-129">You can also download a more detailed version of the report by clicking Request report.</span></span>

![Details-Tabelle für TLS-Verwendung im Bericht "SMTP-AUTH-Clients"](media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a><span data-ttu-id="2f37e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f37e-131">See also</span></span>

<span data-ttu-id="2f37e-132">Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="2f37e-132">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>

---
title: Nachrichtenübermittlung und Einblicke im Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: Administratoren können sich über das Nachrichtenfluss-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: c7c1a6a16c908f42098500c1015b3c3994175818
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155877"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a><span data-ttu-id="fc641-103">Nachrichtenübermittlung und Einblicke im Security & Compliance Center</span><span class="sxs-lookup"><span data-stu-id="fc641-103">Mail flow insights in the Security & Compliance Center</span></span>

<span data-ttu-id="fc641-104">Administratoren können das Nachrichtenfluss-Dashboard im Security & Compliance Center verwenden, um Trends, Einblicke zu ermitteln und Aktionen zum Beheben von Problemen im Zusammenhang mit dem Nachrichtenfluss in Ihrer Office 365 Organisation durchführen.</span><span class="sxs-lookup"><span data-stu-id="fc641-104">Admins can use mail flow dashboard in the Security & Compliance Center to discover trends, insights and take actions to fix issues related to mail flow in their Office 365 organization.</span></span>

<span data-ttu-id="fc641-105">Die im e-Mail-Fluss-Dashboard verfügbaren Einblicke, Berichte und Widgets sind:</span><span class="sxs-lookup"><span data-stu-id="fc641-105">The insights, reports, and widgets that are available in the mail flow dashboard are:</span></span>

- [<span data-ttu-id="fc641-106">Nachrichtenfluss-Zuordnungsbericht</span><span class="sxs-lookup"><span data-stu-id="fc641-106">Mail flow map report</span></span>](mfi-mail-flow-map-report.md)

- [<span data-ttu-id="fc641-107">Einblick in den Domänen Nachrichtenflussstatus</span><span class="sxs-lookup"><span data-stu-id="fc641-107">Domain mail flow status insight</span></span>](mfi-domain-mail-flow-status-insight.md)

- [<span data-ttu-id="fc641-108">SMTP-Authentifizierungsclients (Bericht)</span><span class="sxs-lookup"><span data-stu-id="fc641-108">SMTP Auth clients report</span></span>](mfi-smtp-auth-clients-report.md)

- [<span data-ttu-id="fc641-109">Absenderdomänen Einblicke</span><span class="sxs-lookup"><span data-stu-id="fc641-109">Sender domain insight</span></span>](mfi-sender-domain-insight.md)

- [<span data-ttu-id="fc641-110">Unzustellbarkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="fc641-110">Non-delivery report</span></span>](mfi-non-delivery-report.md)

- [<span data-ttu-id="fc641-111">Bericht über nicht akzeptierte Domänen</span><span class="sxs-lookup"><span data-stu-id="fc641-111">Non-accepted domain report</span></span>](mfi-non-accepted-domain-report.md)

- [<span data-ttu-id="fc641-112">Fluss eingehenden und ausgehender E-Mails</span><span class="sxs-lookup"><span data-stu-id="fc641-112">Outbound and inbound mail flow</span></span>](mfi-outbound-and-inbound-mail-flow.md)

- [<span data-ttu-id="fc641-113">Warteschlangenwarnungen und Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="fc641-113">Queue alerts and Queues</span></span>](mfi-queue-alerts-and-queues.md)

- [<span data-ttu-id="fc641-114">Bericht über automatisch weitergeleitete Nachrichten</span><span class="sxs-lookup"><span data-stu-id="fc641-114">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)

- [<span data-ttu-id="fc641-115">Einblick für E-Mail-Schleife</span><span class="sxs-lookup"><span data-stu-id="fc641-115">Mail loop insight</span></span>](mfi-mail-loop-insight.md)

- [<span data-ttu-id="fc641-116">Einblick für langsame Nachrichtenflussregeln</span><span class="sxs-lookup"><span data-stu-id="fc641-116">Slow mail flow rules insight</span></span>](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a><span data-ttu-id="fc641-117">Erforderliche Berechtigungen zum Anzeigen des Nachrichtenfluss-Dashboards</span><span class="sxs-lookup"><span data-stu-id="fc641-117">Permissions required to view the mail flow dashboard</span></span>

<span data-ttu-id="fc641-118">Das Nachrichtenfluss-Dashboard steht für Folgendes zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="fc641-118">The mail flow dashboard is available to:</span></span>

- <span data-ttu-id="fc641-119">Mitglieder der **globalen Administratorrolle Office 365** .</span><span class="sxs-lookup"><span data-stu-id="fc641-119">Members of the **Office 365 global administrator** role.</span></span>

- <span data-ttu-id="fc641-120">Mitglieder Office 365 Rolle " **Exchange-Administrator** ".</span><span class="sxs-lookup"><span data-stu-id="fc641-120">Members of **Office 365 Exchange administrator** role.</span></span>

- <span data-ttu-id="fc641-121">Mitglieder der **Rolle "Nachrichtenfluss-Administrator** " im Security & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="fc641-121">Members of the **Mail flow administrator role** in the Security & Compliance Center.</span></span> <span data-ttu-id="fc641-122">Wenn diese Rolle explizit einem Benutzer zugewiesen ist, der kein Mitglied der globalen Administrator-oder Exchange-Administratorrolle ist:</span><span class="sxs-lookup"><span data-stu-id="fc641-122">If this role is explicitly assigned to a user who isn't a member of the global administrator or Exchange administrator roles:</span></span>

  - <span data-ttu-id="fc641-123">Der Benutzer muss sich direkt bei [https://protection.office.com](https://protection.office.com)dem Security & Compliance Center anmelden.</span><span class="sxs-lookup"><span data-stu-id="fc641-123">The user must log in to the Security & Compliance Center directly at [https://protection.office.com](https://protection.office.com).</span></span>

  - <span data-ttu-id="fc641-124">Der Benutzer verfügt nur über eine schreibgeschützte Berechtigung für das Nachrichtenfluss-Dashboard.</span><span class="sxs-lookup"><span data-stu-id="fc641-124">The user will only have read-only permission to the mail flow dashboard.</span></span>

  - <span data-ttu-id="fc641-125">Der Benutzer hat keinen Zugriff auf das Office 365-Verwaltungsportal.</span><span class="sxs-lookup"><span data-stu-id="fc641-125">The user won't have access to the Office 365 admin portal.</span></span>

<span data-ttu-id="fc641-126">Weitere Informationen zur Rolle Office 365 globalen Administrators finden Sie unter [Informationen zu Office 365 Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="fc641-126">For more information about the Office 365 global administrator role, see [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span></span>

<span data-ttu-id="fc641-127">Informationen zum Zuweisen von Sicherheits & Compliance Center-Rollen zu Benutzern finden Sie unter [Gewähren von Benutzern Zugriff auf das Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="fc641-127">For information on assigning Security & Compliance Center roles to users, see [Give users access to the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span></span>

## <a name="where-to-find-the-mail-flow-dashboard"></a><span data-ttu-id="fc641-128">So finden Sie das Nachrichtenfluss-Dashboard</span><span class="sxs-lookup"><span data-stu-id="fc641-128">Where to find the mail flow dashboard</span></span>

1. <span data-ttu-id="fc641-129">Wechseln Sie zum Security & Compliance Center unter [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="fc641-129">Go to the Security & Compliance Center at [https://protection.office.com](https://protection.office.com).</span></span>

2. <span data-ttu-id="fc641-130">Erweitern Sie **Nachrichtenfluss** , und wählen Sie dann **Dashboard**aus.</span><span class="sxs-lookup"><span data-stu-id="fc641-130">Expand **Mail flow** and then select **Dashboard**.</span></span>

   ![Das Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/mail-flow-dashboard-v2.png)

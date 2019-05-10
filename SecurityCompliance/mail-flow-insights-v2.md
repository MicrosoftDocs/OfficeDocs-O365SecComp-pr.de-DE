---
title: Nachrichtenübermittlung und Einblicke im Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: Administratoren können sich über das Nachrichtenübermittlungs-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: 80aa6b773d63b6c98293fa2787d38ad393e67b37
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868623"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a><span data-ttu-id="def38-103">Nachrichtenübermittlung und Einblicke im Security & Compliance Center</span><span class="sxs-lookup"><span data-stu-id="def38-103">Mail flow insights in the Security & Compliance Center</span></span>

<span data-ttu-id="def38-104">Administratoren können das Nachrichtenfluss-Dashboard im Security & Compliance Center verwenden, um Trends, Einblicke und Maßnahmen zur Behebung von Problemen im Zusammenhang mit dem Nachrichtenfluss in Ihrer Office 365-Organisation zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="def38-104">Admins can use mail flow dashboard in the Security & Compliance Center to discover trends, insights and take actions to fix issues related to mail flow in their Office 365 organization.</span></span>

<span data-ttu-id="def38-105">Die im e-Mail-Fluss-Dashboard verfügbaren Einblicke, Berichte und Widgets sind:</span><span class="sxs-lookup"><span data-stu-id="def38-105">The insights, reports, and widgets that are available in the mail flow dashboard are:</span></span>

- [<span data-ttu-id="def38-106">Bericht über Nachrichtenfluss Karte</span><span class="sxs-lookup"><span data-stu-id="def38-106">Mail flow map report</span></span>](mfi-mail-flow-map-report.md)

- [<span data-ttu-id="def38-107">Nachrichtenflussstatus der Domäne-Einblicke</span><span class="sxs-lookup"><span data-stu-id="def38-107">Domain mail flow status insight</span></span>](mfi-domain-mail-flow-status-insight.md)

- [<span data-ttu-id="def38-108">Bericht über SMTP-AUTH-Clients</span><span class="sxs-lookup"><span data-stu-id="def38-108">SMTP Auth clients report</span></span>](mfi-smtp-auth-clients-report.md)

- [<span data-ttu-id="def38-109">Einblicke in die Absenderdomäne</span><span class="sxs-lookup"><span data-stu-id="def38-109">Sender domain insight</span></span>](mfi-sender-domain-insight.md)

- [<span data-ttu-id="def38-110">Unzustellbarkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="def38-110">Non-delivery report</span></span>](mfi-non-delivery-report.md)

- [<span data-ttu-id="def38-111">Bericht über nicht akzeptierte Domänen</span><span class="sxs-lookup"><span data-stu-id="def38-111">Non-accepted domain report</span></span>](mfi-non-accepted-domain-report.md)

- [<span data-ttu-id="def38-112">Fluss eingehenden und ausgehender E-Mails</span><span class="sxs-lookup"><span data-stu-id="def38-112">Outbound and inbound mail flow</span></span>](mfi-outbound-and-inbound-mail-flow.md)

- [<span data-ttu-id="def38-113">Warteschlangenwarnungen und Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="def38-113">Queue alerts and Queues</span></span>](mfi-queue-alerts-and-queues.md)

- [<span data-ttu-id="def38-114">Bericht über automatisch weitergeleitete Nachrichten</span><span class="sxs-lookup"><span data-stu-id="def38-114">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)

- [<span data-ttu-id="def38-115">Einblick für E-Mail-Schleife</span><span class="sxs-lookup"><span data-stu-id="def38-115">Mail loop insight</span></span>](mfi-mail-loop-insight.md)

- [<span data-ttu-id="def38-116">Einblick für langsame Nachrichtenflussregeln</span><span class="sxs-lookup"><span data-stu-id="def38-116">Slow mail flow rules insight</span></span>](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a><span data-ttu-id="def38-117">Erforderliche Berechtigungen zum Anzeigen des Nachrichtenübermittlungs-Dashboards</span><span class="sxs-lookup"><span data-stu-id="def38-117">Permissions required to view the mail flow dashboard</span></span>

<span data-ttu-id="def38-118">Das e-Mail-Fluss-Dashboard ist verfügbar für:</span><span class="sxs-lookup"><span data-stu-id="def38-118">The mail flow dashboard is available to:</span></span>

- <span data-ttu-id="def38-119">Mitglieder der **globalen Administratorrolle von Office 365** .</span><span class="sxs-lookup"><span data-stu-id="def38-119">Members of the **Office 365 global administrator** role.</span></span>

- <span data-ttu-id="def38-120">Mitglieder der **Office 365-Exchange-Administrator** Rolle.</span><span class="sxs-lookup"><span data-stu-id="def38-120">Members of **Office 365 Exchange administrator** role.</span></span>

- <span data-ttu-id="def38-121">Mitglieder der **Rolle "Nachrichtenfluss Administrator** " im Security & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="def38-121">Members of the **Mail flow administrator role** in the Security & Compliance Center.</span></span> <span data-ttu-id="def38-122">Wenn diese Rolle explizit einem Benutzer zugewiesen ist, der kein Mitglied der globalen Administrator-oder Exchange-Administratorrollen ist:</span><span class="sxs-lookup"><span data-stu-id="def38-122">If this role is explicitly assigned to a user who isn't a member of the global administrator or Exchange administrator roles:</span></span>

  - <span data-ttu-id="def38-123">Der Benutzer muss sich im Security & Compliance Center direkt bei [https://protection.office.com](https://protection.office.com)anmelden.</span><span class="sxs-lookup"><span data-stu-id="def38-123">The user must log in to the Security & Compliance Center directly at [https://protection.office.com](https://protection.office.com).</span></span>

  - <span data-ttu-id="def38-124">Der Benutzer verfügt nur über Leseberechtigungen für das e-Mail-Fluss-Dashboard.</span><span class="sxs-lookup"><span data-stu-id="def38-124">The user will only have read-only permission to the mail flow dashboard.</span></span>

  - <span data-ttu-id="def38-125">Der Benutzer hat keinen Zugriff auf das Office 365-Verwaltungsportal.</span><span class="sxs-lookup"><span data-stu-id="def38-125">The user won't have access to the Office 365 admin portal.</span></span>

<span data-ttu-id="def38-126">Weitere Informationen zur Rolle des globalen Administrators von Office 365 finden Sie unter [Informationen zu Office 365-Verwaltungsrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="def38-126">For more information about the Office 365 global administrator role, see [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span></span>

<span data-ttu-id="def38-127">Informationen zum Zuweisen von Security & Compliance Center-Rollen zu Benutzern finden Sie unter [Gewähren von Benutzern Zugriff auf das Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="def38-127">For information on assigning Security & Compliance Center roles to users, see [Give users access to the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span></span>

## <a name="where-to-find-the-mail-flow-dashboard"></a><span data-ttu-id="def38-128">Wo finden Sie das Nachrichtenfluss-Dashboard</span><span class="sxs-lookup"><span data-stu-id="def38-128">Where to find the mail flow dashboard</span></span>

1. <span data-ttu-id="def38-129">Wechseln Sie zum Security & Compliance Center unter [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="def38-129">Go to the Security & Compliance Center at [https://protection.office.com](https://protection.office.com).</span></span>

2. <span data-ttu-id="def38-130">Erweitern Sie **Nachrichtenfluss** , und wählen Sie dann **Dashboard**aus.</span><span class="sxs-lookup"><span data-stu-id="def38-130">Expand **Mail flow** and then select **Dashboard**.</span></span>

   ![Das e-Mail-Fluss-Dashboard im Office 365 Security & Compliance Center](media/mail-flow-dashboard-v2.png)

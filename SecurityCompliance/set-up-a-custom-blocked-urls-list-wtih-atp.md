---
title: Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Hier erfahren Sie, wie Sie eine Liste der blockierten URLs für Ihre Organisation mit Office 365 erweiterte Threat Protection einrichten. Blockierte URLs werden auf e-Mail-Nachrichten und Office-Dokumenten gemäß Ihrer ATP sichere Links Richtlinien angewendet.
ms.openlocfilehash: 4d8c9c669310137d3f491f5a79c93f4d6af71ac5
ms.sourcegitcommit: d6a28c4f6db6a676ca960173e8ff8f17d4aa1c4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2019
ms.locfileid: "29755316"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="e90be-104">Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="e90be-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="e90be-p102">Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation eine benutzerdefinierte Liste von Website-Adressen (URLs verwendet) haben, die blockiert werden. Wenn eine URL blockiert wird, Personen, die Links zu den blockierten URL klicken Sie auf einer [Seite Warnung](atp-safe-links-warning-pages.md) wird aufgerufen, die in der folgenden Abbildung ähneln:</span><span class="sxs-lookup"><span data-stu-id="e90be-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Diese Website wird blockiert.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="e90be-108">Die Liste der blockierte URLs von Office 365-Security-Team Ihrer Organisation definiert ist, und dieser Liste gilt für alle Benutzer in der Organisation, die von sicheren Links zu Office 365 ATP Richtlinien abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="e90be-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="e90be-109">Lesen Sie diesen Artikel erfahren, wie Ihre Organisation benutzerdefinierte blockierte URLs Liste für [ATP sichere Links in Office 365](atp-safe-links.md)einrichten.</span><span class="sxs-lookup"><span data-stu-id="e90be-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="e90be-110">Zeigen Sie an oder bearbeiten Sie eine benutzerdefinierte Liste der blockierten URLs</span><span class="sxs-lookup"><span data-stu-id="e90be-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="e90be-p103">[ATP sichere Links in Office 365](atp-safe-links.md) verwendet mehrere Listen, einschließlich Ihrer Organisation benutzerdefinierte blockierte URLs Liste. Wenn Sie die erforderlichen Berechtigungen verfügen, können Sie benutzerdefinierte Liste in Ihrer Organisation einrichten. Zu diesem Zweck Ihrer Organisation Standardrichtlinie sichere Links bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e90be-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="e90be-114">Um ATP Richtlinien bearbeiten (oder definieren), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="e90be-114">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="e90be-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="e90be-115">Role</span></span>  |<span data-ttu-id="e90be-116">WHERE/wie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e90be-116">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="e90be-117">Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="e90be-117">Office 365 Global Administrator</span></span> |<span data-ttu-id="e90be-p104">Die Person, die zum Erwerben von Office 365 angemeldet ist ein globaler Administrator in der Standardeinstellung. (Siehe [zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) , um mehr zu erfahren.)</span><span class="sxs-lookup"><span data-stu-id="e90be-p104">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="e90be-120">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="e90be-120">Security Administrator</span></span> |<span data-ttu-id="e90be-121">Azure Active Directory-Verwaltungskonsole ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="e90be-121">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="e90be-122">Verwaltung von Exchange Online-Organisation</span><span class="sxs-lookup"><span data-stu-id="e90be-122">Exchange Online Organization Management</span></span> |<span data-ttu-id="e90be-123">Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="e90be-123">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="e90be-124">oder</span><span class="sxs-lookup"><span data-stu-id="e90be-124">or</span></span> <br>  <span data-ttu-id="e90be-125">PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="e90be-125">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="e90be-126">Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="e90be-126">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="e90be-127">Anzeigen oder bearbeiten eine benutzerdefinierte Liste der blockierte URLs</span><span class="sxs-lookup"><span data-stu-id="e90be-127">To view or edit a custom blocked URLs list</span></span>
  
1. <span data-ttu-id="e90be-128">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule.</span><span class="sxs-lookup"><span data-stu-id="e90be-128">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="e90be-129">Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Policy** \> **Sichere Links**.</span><span class="sxs-lookup"><span data-stu-id="e90be-129">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="e90be-130">Klicken Sie im Abschnitt **Richtlinien, die für die gesamte Organisation gelten,** **Standard**wählen Sie aus, und wählen Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten hat einen Stift).</span><span class="sxs-lookup"><span data-stu-id="e90be-130">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="e90be-131">![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für sichere Links Protection bearbeiten](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="e90be-131">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="e90be-p105">Dadurch können Sie Ihrer Liste der blockierten URLs anzuzeigen. Zunächst verfügen Sie möglicherweise keine hier aufgeführten URLs.</span><span class="sxs-lookup"><span data-stu-id="e90be-p105">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="e90be-134">![Liste der URLs in der Standardrichtlinie für sichere Links blockiert](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="e90be-134">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="e90be-135">Feld **Geben Sie eine gültige URL** auswählen, geben Sie eine URL ein, und wählen Sie dann auf das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="e90be-135">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="e90be-136">Wenn Sie das Hinzufügen von URLs in der unteren rechten Ecke des Bildschirms abgeschlossen haben, wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e90be-136">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="e90be-137">Einige Dinge im Hinterkopf behalten</span><span class="sxs-lookup"><span data-stu-id="e90be-137">A few things to keep in mind</span></span>

<span data-ttu-id="e90be-138">Während Sie URLs zur Kontaktliste hinzufügen, sollten beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="e90be-138">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="e90be-p106">Schließen Sie keinen Schrägstrich ( **/**) am Ende der URL. Beispielsweise statt `http://www.contoso.com/`, geben Sie `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="e90be-p106">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="e90be-p107">Sie können eine Domäne-only-URL angeben (wie `contoso.com` oder `tailspintoys.com`). Dies wird blockiert, Klicks für jede URL, die die Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="e90be-p107">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="e90be-p108">Sie können eine Unterdomäne angeben (wie `toys.contoso.com*`) ohne zu eine vollständige Domäne blockieren (wie `contoso.com`). Dadurch Block klickt auf einen beliebigen URL, die die Unterdomäne enthält, aber es nicht blockieren Klicks auf eine URL, die die vollständige Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="e90be-p108">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="e90be-p109">Sie können bis zu drei Platzhalter Sternchen einschließen (\*) pro URL. Die folgende Tabelle enthält einige Beispiele für die Eingabe und Einfluss auf diese Einträge haben.</span><span class="sxs-lookup"><span data-stu-id="e90be-p109">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="e90be-147">**Beispieleintrag**</span><span class="sxs-lookup"><span data-stu-id="e90be-147">**Example Entry**</span></span>|<span data-ttu-id="e90be-148">**Sinn und Zweck**</span><span class="sxs-lookup"><span data-stu-id="e90be-148">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e90be-149">`contoso.com`oder`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="e90be-149">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="e90be-150">Blockiert die Domäne, untergeordnete Domänen und Pfade, wie `https://www.contoso.com`, `http://sub.contoso.com`, und`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="e90be-150">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="e90be-151">Eine Website blockiert `http://contoso.com/a` aber keine zusätzliche Pfade`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="e90be-151">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="e90be-152">Eine Website blockiert `http://contoso.com/a` und wie Sie zusätzliche Pfade`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="e90be-152">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="e90be-153">Blöcke eine Unterdomäne (in diesem Fall "Toys"), aber zulassen Klicks zu anderen Domänen-URLs (wie `http://contoso.com` oder `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="e90be-153">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="e90be-154">Gewusst wie: Definieren von Ausnahmen für bestimmte Benutzer in einer Organisation</span><span class="sxs-lookup"><span data-stu-id="e90be-154">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="e90be-p110">Bestimmte Gruppen können URLs anzuzeigen, die für andere Benutzer blockiert werden soll, können Sie eine sichere Links ATP Richtlinie angeben, die für bestimmte Empfänger gilt. Finden Sie unter [Einrichten einer benutzerdefinierten "nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="e90be-p110">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  


---
title: Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 12/11/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Hier erfahren Sie, wie Sie eine Liste der blockierten URLs für Ihre Organisation mit Office 365 erweiterte Threat Protection einrichten. Blockierte URLs werden auf e-Mail-Nachrichten und Office-Dokumenten gemäß Ihrer ATP sichere Links Richtlinien angewendet.
ms.openlocfilehash: 25f01b767726ebf02d5da5d18444fa0428f144ac
ms.sourcegitcommit: 031781d0eecf33baabcd03ea53546d41076062b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2018
ms.locfileid: "27240528"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="492a2-104">Richten Sie eine benutzerdefinierte blockierte URLs Liste mit sicheren Links zu Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="492a2-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="492a2-p102">Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation eine benutzerdefinierte Liste von Website-Adressen (URLs verwendet) haben, die blockiert werden. Wenn eine URL blockiert wird, Personen, die Links zu den blockierten URL klicken Sie auf einer [Seite Warnung](atp-safe-links-warning-pages.md) wird aufgerufen, die in der folgenden Abbildung ähneln:</span><span class="sxs-lookup"><span data-stu-id="492a2-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Diese Website wird blockiert.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="492a2-108">Die Liste der blockierte URLs von Office 365-Security-Team Ihrer Organisation definiert ist, und dieser Liste gilt für alle Benutzer in der Organisation, die von sicheren Links zu Office 365 ATP Richtlinien abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="492a2-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="492a2-109">Lesen Sie diesen Artikel erfahren, wie Ihre Organisation benutzerdefinierte blockierte URLs Liste für [ATP sichere Links in Office 365](atp-safe-links.md)einrichten.</span><span class="sxs-lookup"><span data-stu-id="492a2-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="492a2-110">Zeigen Sie an oder bearbeiten Sie eine benutzerdefinierte Liste der blockierten URLs</span><span class="sxs-lookup"><span data-stu-id="492a2-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="492a2-p103">[ATP sichere Links in Office 365](atp-safe-links.md) verwendet mehrere Listen, einschließlich Ihrer Organisation benutzerdefinierte blockierte URLs Liste. Wenn Sie die erforderlichen Berechtigungen verfügen, können Sie benutzerdefinierte Liste in Ihrer Organisation einrichten. Zu diesem Zweck Ihrer Organisation Standardrichtlinie sichere Links bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="492a2-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="492a2-114">Wechseln Sie zu [https://security.microsoft.com](https://security.microsoft.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule.</span><span class="sxs-lookup"><span data-stu-id="492a2-114">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="492a2-115">Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Policy** \> **Sichere Links**.</span><span class="sxs-lookup"><span data-stu-id="492a2-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="492a2-116">Klicken Sie im Abschnitt **Richtlinien, die für die gesamte Organisation gelten,** **Standard**wählen Sie aus, und wählen Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten hat einen Stift).</span><span class="sxs-lookup"><span data-stu-id="492a2-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="492a2-117">![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für sichere Links Protection bearbeiten](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="492a2-117">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="492a2-p104">Dadurch können Sie Ihrer Liste der blockierten URLs anzuzeigen. Zunächst verfügen Sie möglicherweise keine hier aufgeführten URLs.</span><span class="sxs-lookup"><span data-stu-id="492a2-p104">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="492a2-120">![Liste der URLs in der Standardrichtlinie für sichere Links blockiert](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="492a2-120">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="492a2-121">Feld **Geben Sie eine gültige URL** auswählen, geben Sie eine URL ein, und wählen Sie dann auf das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="492a2-121">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="492a2-122">Wenn Sie das Hinzufügen von URLs in der unteren rechten Ecke des Bildschirms abgeschlossen haben, wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="492a2-122">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="492a2-123">Einige Dinge im Hinterkopf behalten</span><span class="sxs-lookup"><span data-stu-id="492a2-123">A few things to keep in mind</span></span>

<span data-ttu-id="492a2-124">Während Sie URLs zur Kontaktliste hinzufügen, sollten beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="492a2-124">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="492a2-p105">Schließen Sie keinen Schrägstrich ( **/**) am Ende der URL. Beispielsweise statt `http://www.contoso.com/`, geben Sie `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="492a2-p105">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="492a2-p106">Sie können eine Domäne-only-URL angeben (wie `contoso.com` oder `tailspintoys.com`). Dies wird blockiert, Klicks für jede URL, die die Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="492a2-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="492a2-p107">Sie können eine Unterdomäne angeben (wie `toys.contoso.com*`) ohne zu eine vollständige Domäne blockieren (wie `contoso.com`). Dadurch Block klickt auf einen beliebigen URL, die die Unterdomäne enthält, aber es nicht blockieren Klicks auf eine URL, die die vollständige Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="492a2-p107">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="492a2-p108">Sie können bis zu drei Platzhalter Sternchen einschließen (\*) pro URL. Die folgende Tabelle enthält einige Beispiele für die Eingabe und Einfluss auf diese Einträge haben.</span><span class="sxs-lookup"><span data-stu-id="492a2-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="492a2-133">**Beispieleintrag**</span><span class="sxs-lookup"><span data-stu-id="492a2-133">**Example Entry**</span></span>|<span data-ttu-id="492a2-134">**Sinn und Zweck**</span><span class="sxs-lookup"><span data-stu-id="492a2-134">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="492a2-135">`contoso.com`oder`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="492a2-135">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="492a2-136">Blockiert die Domäne, untergeordnete Domänen und Pfade, wie `https://www.contoso.com`, `http://sub.contoso.com`, und`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="492a2-136">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="492a2-137">Eine Website blockiert `http://contoso.com/a` aber keine zusätzliche Pfade`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="492a2-137">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="492a2-138">Eine Website blockiert `http://contoso.com/a` und wie Sie zusätzliche Pfade`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="492a2-138">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="492a2-139">Blöcke eine Unterdomäne (in diesem Fall "Toys"), aber zulassen Klicks zu anderen Domänen-URLs (wie `http://contoso.com` oder `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="492a2-139">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="492a2-140">Gewusst wie: Definieren von Ausnahmen für bestimmte Benutzer in einer Organisation</span><span class="sxs-lookup"><span data-stu-id="492a2-140">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="492a2-p109">Bestimmte Gruppen können URLs anzuzeigen, die für andere Benutzer blockiert werden soll, können Sie eine sichere Links ATP Richtlinie angeben, die für bestimmte Empfänger gilt. Finden Sie unter [Einrichten einer benutzerdefinierten "nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="492a2-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  


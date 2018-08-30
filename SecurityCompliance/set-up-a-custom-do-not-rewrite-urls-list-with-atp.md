---
title: Richten Sie eine benutzerdefinierte-nicht-zum Umschreiben von Adressen URLs-Liste mit sicheren Links zu Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: Beim Einrichten Ihrer ATP sichere Links Richtlinien können Sie eine Not Rewrite einschließen ' Liste der URLs zum Aktivieren von einigen Personen in Ihrer Organisation Websites besuchen, die Sie in der Liste enthalten.
ms.openlocfilehash: 780b4e5d194ad89acf12b052c81f8af21234eea3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529217"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="98858-103">Richten Sie eine benutzerdefinierte-nicht-zum Umschreiben von Adressen URLs-Liste mit sicheren Links zu Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="98858-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="98858-p101">Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihrer Organisation eine [benutzerdefinierte blockierte URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)so, dass beim Klicken Sie auf Personen Web-Adressen (URLs) in e-Mail-Nachrichten oder bestimmte Office-Dokumente, sie werden daran gehindert unterschiedlich sein und sollte diesen URLs. Ihrer Organisation kann auch benutzerdefinierte "nicht rewrite" Listen für bestimmte Gruppen in Ihrer Organisation haben. Eine Liste "nicht rewrite" kann einige Personen URLs zu besuchen, die andernfalls [ATP sichere](atp-safe-links.md)Links in Office 365 blockiert sind.</span><span class="sxs-lookup"><span data-stu-id="98858-p101">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs. Your organization can also have custom "do not rewrite" lists for specific groups in your organization. A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="98858-107">In diesem Artikel wird beschrieben, wie eine Liste der URLs an, die von sicheren Links ATP untersucht, und einige wichtige Punkte zu bedenken ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="98858-107">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>
    
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="98858-108">Wichtige Punkte zu bedenken</span><span class="sxs-lookup"><span data-stu-id="98858-108">Important points to keep in mind</span></span>

- <span data-ttu-id="98858-109">Alle URLs, die Sie in der Liste "nicht rewrite" angeben, werden von ATP sichere Links Scan für die Empfänger die Angabe ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="98858-109">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
    
- <span data-ttu-id="98858-p102">Wenn Sie eine Liste "nicht rewrite" für eine sichere Links ATP Richtlinie angeben, können Sie bis zu drei Platzhalter Sternchen einschließen (\*). Platzhalter (\*) wird angenommen, dass für Einträge wie `contoso.com`, die nicht explizit einschließen Präfixe oder Unterdomänen, wie `http://` oder `https://`. Dies bedeutet, dass einen Eintrag wie `contoso.com` ähnelt `\*contoso.com\*` für die Liste "nicht rewrite".</span><span class="sxs-lookup"><span data-stu-id="98858-p102">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*). Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`. This means an entry, such as `contoso.com` is similar to `\*contoso.com\*` for your "do not rewrite" list.</span></span>
    
    <span data-ttu-id="98858-113">Die folgende Tabelle Listen Beispiele für die Eingabe und Einfluss auf diese Einträge haben.</span><span class="sxs-lookup"><span data-stu-id="98858-113">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="98858-114">**Beispieleintrag**</span><span class="sxs-lookup"><span data-stu-id="98858-114">**Example Entry**</span></span>|<span data-ttu-id="98858-115">**Sinn und Zweck**</span><span class="sxs-lookup"><span data-stu-id="98858-115">**What It Does**</span></span>|
|:-----|:-----|
|`\*contoso.com\*`  <br/> |<span data-ttu-id="98858-116">Können bestimmte Empfänger eine Domäne, untergeordnete Domänen und Pfade, z. B. Besuchen `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, oder`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="98858-116">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="98858-117">Können bestimmte Empfänger eine Website wie `http://contoso.com/a`, aber nicht Pfade`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="98858-117">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a\*`  <br/> |<span data-ttu-id="98858-118">Können bestimmte Empfänger eine Website wie `http://contoso.com/a` und Pfade wie`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="98858-118">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
- <span data-ttu-id="98858-p103">Wenn Sie bereits eine Liste mit URLs in der Liste "nicht rewrite" verfügen, stellen Sie sicher, überprüfen Sie die Liste und Hinzufügen von Platzhaltern nach Bedarf. Beispielsweise, wenn Ihre vorhandene Liste hat ein Eintrag wie `http://contoso.com/a` und Pfade wie sollen `http://contoso.com/a/b` fügen Sie einen Platzhalter in der Richtlinie den Eintrag, sodass es aussieht `http://contoso.com/a\*`.</span><span class="sxs-lookup"><span data-stu-id="98858-p103">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate. For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a\*`.</span></span>
    
- <span data-ttu-id="98858-p104">Schließen Sie einen Schrägstrich (/) nicht in den URLs, die Sie in der Liste "nicht rewrite" angeben. Beispielsweise geben, sondern `contoso.com/` Geben Sie in der Liste "nicht rewrite" `contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="98858-p104">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list. For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
## <a name="set-up-a-do-not-rewrite-list-for-specific-groups"></a><span data-ttu-id="98858-123">Richten Sie eine Liste "nicht rewrite" für bestimmte Gruppen</span><span class="sxs-lookup"><span data-stu-id="98858-123">Set up a "do not rewrite" list for specific groups</span></span>

<span data-ttu-id="98858-p105">Sichere Links ATP Protection verwendet mehrere Listen, einschließlich der Liste der blockierten URLs Ihrer Organisation und den Listen "nicht rewrite" für Ausnahmen. Wenn Sie die erforderlichen Berechtigungen verfügen, können Sie Ihre benutzerdefinierte Listen "nicht rewrite" einrichten. Hierzu beim Hinzufügen oder Bearbeiten von Richtlinien für sichere Links, die für bestimmte Empfänger in Ihrer Organisation gelten.</span><span class="sxs-lookup"><span data-stu-id="98858-p105">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions. If you have the necessary permissions, you can set up your custom "do not rewrite" lists. You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 
  
1. <span data-ttu-id="98858-127">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule.</span><span class="sxs-lookup"><span data-stu-id="98858-127">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="98858-128">Im Navigationsbereich unter **Threat Management** \> **Richtlinie** \> **Sichere Links**.</span><span class="sxs-lookup"><span data-stu-id="98858-128">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="98858-p106">Wählen Sie im Abschnitt **Richtlinien, die auf bestimmte Empfänger anzuwenden** , **New** (neue Schaltfläche ähnelt ein Pluszeichen ( **+**)) zum Erstellen einer neuen Richtlinie. (Alternativ können Sie eine vorhandene Richtlinie bearbeiten.)</span><span class="sxs-lookup"><span data-stu-id="98858-p106">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy. (Alternatively, you can edit an existing policy.)</span></span>
    
    ![Wählen Sie neu aus, um eine sichere Links Richtlinie für bestimmte e-Mail-Empfänger hinzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. <span data-ttu-id="98858-132">Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="98858-132">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="98858-133">Klicken Sie im Abschnitt **Schreiben Sie die folgenden URLs nicht** wählen Sie das Feld **Geben Sie eine gültige URL** und geben Sie eine URL ein, und wählen Sie dann auf das Pluszeichen (+).</span><span class="sxs-lookup"><span data-stu-id="98858-133">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="98858-p107">**Angewendet auf** Sie im Abschnitt wählen Sie **der Empfänger ist Mitglied von**, und wählen Sie dann die Kontaktgruppen, die in der Richtlinie enthalten sein sollen. Wählen Sie **Hinzufügen**, und wählen Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="98858-p107">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy. Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="98858-136">Wenn Sie das Hinzufügen von URLs in der unteren rechten Ecke des Bildschirms abgeschlossen haben, wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="98858-136">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="98858-p108">Stellen Sie sicher, dass Sie die benutzerdefinierte Liste der blockierten URLs Ihrer Organisation überprüfen. Finden Sie unter [Einrichten einer benutzerdefinierten blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span><span class="sxs-lookup"><span data-stu-id="98858-p108">Make sure to review your organization's custom list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="98858-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="98858-139">Related topics</span></span>

[<span data-ttu-id="98858-140">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="98858-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="98858-141">ATP sichere Links in Office 365</span><span class="sxs-lookup"><span data-stu-id="98858-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="98858-142">Einrichten von sicheren Links ATP Richtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="98858-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="98858-143">Richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links</span><span class="sxs-lookup"><span data-stu-id="98858-143">Set up a custom blocked URLs list using ATP Safe Links</span></span>](set-up-a-custom-blocked-urls-list-wtih-atp.md)

[<span data-ttu-id="98858-144">Anzeigen von Berichten für Office 365 erweiterte Threat Protection</span><span class="sxs-lookup"><span data-stu-id="98858-144">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="98858-145">Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="98858-145">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  


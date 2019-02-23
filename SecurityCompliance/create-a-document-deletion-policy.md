---
title: Erstellen einer Dokumentlöschrichtlinie
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: Organisationen müssen häufig Dokumente aufgrund von Konformitäts-, rechtlicher und anderer Bestimmungen für einen bestimmten Zeitraum aufbewahren. Wenn Dokumente aber länger als nötig aufbewahrt werden, kann dies für die Organisation rechtliche Folgen haben.
ms.openlocfilehash: f666d652e2e1a0a5ffd099fd0005f498598604db
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220555"
---
# <a name="create-a-document-deletion-policy"></a><span data-ttu-id="fec8a-104">Erstellen einer Dokumentlöschrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fec8a-104">Create a document deletion policy</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fec8a-p102">Es wird empfohlen, eine Aufbewahrungsrichtlinie oder Bezeichnungen zu verwenden, die im Security &amp; Compliance Center anstelle einer Dokument Löschrichtlinie erstellt wurden. Dokument Löschrichtlinien arbeiten weiterhin nebeneinander mit Aufbewahrungsrichtlinien, aber wenn Sie Inhalte in Office 365 beibehalten oder löschen müssen, empfiehlt es sich, eine Aufbewahrungsrichtlinie zu verwenden. Weitere Informationen finden Sie unter [Verwenden einer Aufbewahrungsrichtlinie anstelle dieser Features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span><span class="sxs-lookup"><span data-stu-id="fec8a-p102">Moving forward, we recommend that you use a retention policy or labels created in the Security &amp; Compliance Center instead of a document deletion policy. Document deletion policies will continue to work side by side with retention policies, but if you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy. For more information, see [Use a retention policy instead of these features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span></span> 
  
<span data-ttu-id="fec8a-p103">Organisationen müssen häufig Dokumente aufgrund von Konformitäts-, rechtlicher und anderer Bestimmungen für einen bestimmten Zeitraum aufbewahren. Wenn Dokumente aber länger als nötig aufbewahrt werden, kann dies für die Organisation rechtliche Folgen haben.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p103">Organizations are often required to retain documents for a certain period of time due to compliance, legal, or other regulations. However, retaining documents for longer than required can expose the organization to legal risk.</span></span>
  
<span data-ttu-id="fec8a-110">Mit einer Dokument Löschrichtlinie können Sie das Risiko proaktiv verringern, indem Sie Dokumente auf einer Website nach einem bestimmten Zeitraum löschen, beispielsweise fünf Jahre nach dem Erstellen der Dokumente in den OneDrive-Websites von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="fec8a-110">With a document deletion policy, you can proactively reduce risk by deleting documents in a site after a specific period of time—for example, you can delete documents in users' OneDrive for Business sites five years after the documents were created.</span></span> 
  
<span data-ttu-id="fec8a-p104">Nach dem Erstellen einer Dokumentlöschrichtlinie können Sie sie einer Vorlage für Websitesammlung zuweisen, damit die Richtlinie für alle Websitesammlungen, die aus dieser Vorlage erstellt werden, verfügbar ist. Sie können außerdem einer bestimmten Websitesammlung eine Richtlinie zuweisen, die alle Richtlinien, die der Vorlage für diese Websitesammlung möglicherweise schon zugewiesen wurden, außer Kraft setzt.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p104">After you create a document deletion policy, you can assign it to a site collection template, so that the policy is available to all site collections created from that template. You can also assign a policy to a specific a site collection, which overrides any policies that may have been assigned to the template for that site collection.</span></span>
  
![Startseite von Document Deletion Policy Center](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a><span data-ttu-id="fec8a-114">Richtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="fec8a-114">Policy templates</span></span>

<span data-ttu-id="fec8a-p105">Sie können eine Dokumentlöschrichtlinie von Grund auf neu erstellen oder eine unserer Beispielrichtlinien verwenden. Im Compliance Policy Center finden Sie Beispielrichtlinien, die Sie entweder sofort verwenden oder als Ausgangsbasis verwenden und umbenennen oder ändern können.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p105">You can create a document deletion policy from scratch, or you can use one of the sample policies. The Compliance Policy Center includes sample policies that you can use as is, or you can use them as a starting point and then rename or modify them.</span></span>
  
![Beispiel von Dokumentlöschrichtlinien](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a><span data-ttu-id="fec8a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fec8a-118">Examples of how to use document deletion policies</span></span>

<span data-ttu-id="fec8a-p106">Einer Websitesammlung oder einer websitesammlungsvorlage kann eine weitere Richtlinie zugewiesen werden, und jede dieser Richtlinien kann eine oder mehrere Regeln aufweisen. Es kann jedoch nur eine Richtlinie pro Website aktiv sein, und es kann nur eine Löschregel geben, die jederzeit für die Bibliotheken innerhalb der Website aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p106">A site collection or a site collection template can have one more policies assigned to it, and each of those policies can have one or more rules. However, there can be only one policy that's active per site, and there can be only one deletion rule that's active at any time for the libraries within the site.</span></span>
  
![Diagramm der Beziehungen zwischen Richtlinien](media/IP-Two-policies-four-rules.png)
  
<span data-ttu-id="fec8a-122">Außerdem können Sie eine Richtlinie als obligatorisch oder Standard und eine Löschregel als Standardregel auswählen:</span><span class="sxs-lookup"><span data-stu-id="fec8a-122">In addition, you can select a policy as mandatory or default, and you can select a deletion rule as a default rule:</span></span> 
  
- <span data-ttu-id="fec8a-p107">**Obligatorische Richtlinie** Wenn eine Richtlinie als obligatorisch gekennzeichnet ist, kann der Websitesammlung oder-Vorlage nur eine Richtlinie zugewiesen werden. Die Richtlinie muss als Standard gekennzeichnet werden und auf alle Websites angewendet werden. Websitebesitzer können die Richtlinie nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p107">**Mandatory policy**When a policy is marked as mandatory, only one policy can be assigned to the site collection or template. The policy must be marked as default and will be applied to all sites. Site owners cannot opt out of the policy.</span></span>
    
- <span data-ttu-id="fec8a-126">**Standardrichtlinie** Wenn eine Richtlinie als Standard festgelegt ist, wird die Richtlinie automatisch auf allen Websites aktiviert, denen Sie zugewiesen wurde, ohne dass eine Aktion für den Websitebesitzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-126">**Default policy**When a policy is set as default, the policy is automatically active in all sites that it's assigned to with no action required by site owner.</span></span>
    
- <span data-ttu-id="fec8a-127">**Standardregel** Wenn eine Löschregel als Standard festgelegt wird, wird Sie automatisch auf alle Bibliotheken in den Websites angewendet, die die Richtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-127">**Default rule**When a deletion rule is set as default, it is automatically applied to all libraries in the sites that use the policy.</span></span>
    
<span data-ttu-id="fec8a-128">Die folgenden Beispiele erläutern, wann Sie möglicherweise eine obligatorische Richtlinie oder Standardrichtlinien und -regeln verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="fec8a-128">The following examples explain when you might want to use a mandatory policy or default policies and rules.</span></span>
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a><span data-ttu-id="fec8a-129">Beispiel 1: Anwenden einer einzelnen Richtlinie mit einer einzelnen Regel auf eine Vorlage für Websitesammlung</span><span class="sxs-lookup"><span data-stu-id="fec8a-129">Example 1: Apply a single policy with a single rule to a site collection template</span></span>

<span data-ttu-id="fec8a-p108">Angenommen, Sie möchten eine Dokumentlöschrichtlinie für eine vielfältige Reihe von unstrukturierten Inhalten erzwingen, z. B. alle Websites von OneDrive for Business oder alle Teamwebsites. Wenn Sie sicherstellen möchten, dass eine einzelne Dokumentlöschrichtlinie auf allen Websites aktiv ist, die von einer Vorlage für Websitesammlung erstellt wurde, können Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="fec8a-p108">You may want to enforce a document deletion policy across a broad range of unstructured content, such as all OneDrive for Business sites or all team sites. If you want to ensure that a single document deletion policy is active in all sites created from a site collection template, you can:</span></span>
  
1. <span data-ttu-id="fec8a-132">Erstellen Sie eine einzelne Richtlinie mit einer einzelnen Standardlöschregel.</span><span class="sxs-lookup"><span data-stu-id="fec8a-132">Create a single policy with a single default deletion rule.</span></span>
    
2. <span data-ttu-id="fec8a-133">Legen Sie die Richtlinie als obligatorisch und Standard fest.</span><span class="sxs-lookup"><span data-stu-id="fec8a-133">Set the policy as mandatory and default.</span></span>
    
3. <span data-ttu-id="fec8a-134">Weisen Sie die Richtlinie einer Vorlage für Websitesammlung zu.</span><span class="sxs-lookup"><span data-stu-id="fec8a-134">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="fec8a-p109">In diesem Beispiel wird die Standardlöschregel auf alle Bibliotheken in allen Websitesammlungen angewendet, die aufgrund der Vorlage erstellt wurden, und die Websitebesitzer können die Richtlinie nicht abwählen. Dies ist die einfachste Möglichkeit, um eine Dokumentlöschrichtlinie umfassend und strikt zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p109">In this example, the default deletion rule will be applied to all libraries in all site collections created from the template, and site owners cannot opt out of the policy. This is the simplest way to broadly and rigidly enforce a document deletion policy.</span></span>
  
![Diagramm einer einzelnen obligatorischen Richtlinie](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a><span data-ttu-id="fec8a-138">Beispiel 2: Anwenden einer einzelnen Richtlinie mit mehreren Regeln auf eine websitesammlungsvorlage</span><span class="sxs-lookup"><span data-stu-id="fec8a-138">Example 2: Apply a single policy with several rules to a site collection template</span></span>

<span data-ttu-id="fec8a-p110">Websitebesitzer wissen oft am besten, welche Art von Inhalten ihre Website enthält, sodass Sie Websitebesitzern die Auswahl der für ihre Website am besten geeigneten Löschregel ermöglichen können. Sie können auch zulassen, dass Websitebesitzer die Richtlinie ganz abwählen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p110">Site owners often know best what type of content their site contains, so you may choose to allow site owners to select the deletion rule that best applies to their site. You may also want to allow site owners to opt out of a policy entirely.</span></span>
  
<span data-ttu-id="fec8a-p111">Auch dann können Sie die Richtlinien noch zentral erstellen und verwalten. Sie können auch eine Richtlinie und Regel als den Standard auswählen, sodass eine Richtlinie so lange aktiv ist, bis der Websitebesitzer eine andere auswählt oder die Richtlinie abwählt. Wenn Sie Websitebesitzern diese Flexibilität bieten möchten, können Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="fec8a-p111">At the same time, you can still centrally create and manage the policies. You can also select one policy and rule as the default, so that a policy is always in effect until the site owner chooses a different one or opts out. If you want to provide such flexibility to site owners, you can:</span></span>
  
1. <span data-ttu-id="fec8a-143">Erstellen Sie eine einzelne Richtlinie mit mehreren Löschregeln, und legen Sie eine Regel als den Standard fest.</span><span class="sxs-lookup"><span data-stu-id="fec8a-143">Create a single policy with several deletion rules, and set one rule as the default.</span></span>
    
2. <span data-ttu-id="fec8a-144">Legen Sie die Richtlinie als die Standardrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="fec8a-144">Set the policy as the default policy.</span></span>
    
3. <span data-ttu-id="fec8a-145">Weisen Sie die Richtlinie einer Vorlage für Websitesammlung zu.</span><span class="sxs-lookup"><span data-stu-id="fec8a-145">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="fec8a-146">Websitebesitzer können eine der alternativen Löschregeln auswählen, die Richtlinie abwählen oder nichts unternehmen und die Standardrichtlinie und -regel übernehmen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-146">Site owners can select one of the alternate deletion rules, opt out of the policy, or do nothing and be subject to the default policy and rule.</span></span>
  
![Diagramm einer Richtlinie mit vielen Regeln](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a><span data-ttu-id="fec8a-148">Beispiel 3: Anwenden mehrerer Richtlinien mit mindestens einer Regel auf eine Websitesammlung</span><span class="sxs-lookup"><span data-stu-id="fec8a-148">Example 3: Apply several policies with one or more rules to a site collection</span></span>

<span data-ttu-id="fec8a-p112">In diesem Beispiel haben Websitebesitzer die höchste Flexibilität, weil sie aus mehreren Richtlinien auswählen und nach der Auswahl einer Richtlinie oft aus mehreren Regeln auswählen können. Eine Richtlinie und eine Regel sind als der Standard festgelegt, sodass eine Richtlinie so lange aktiv ist, bis der Websitebesitzer eine andere auswählt oder die Richtlinie abwählt. Beachten Sie Folgendes: Wenn Sie keine Richtlinie und Regel als Standard festlegen, sind auf der Website keine Richtlinien oder Regeln für die Dokumentbibliotheken aktiv, bis der Websitebesitzer eine Aktion durchführt, um sie auszuwählen und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p112">This example provides the maximum flexibility to site owners because they can choose from several policies, and after selecting a policy they can often choose from several rules. One policy and rule are set as default, so that a policy is always in effect until the site owner chooses a different one or opts out. Note that if you do not set a policy and rule as the default, then no policies or rules will be active for the document libraries in the site until the site owner takes action to select and apply them.</span></span>
  
<span data-ttu-id="fec8a-p113">Im Unterschied zu den vorherigen beiden Beispielen werden diese Richtlinien einer bestimmten Websitesammlung zugewiesen, nicht der Vorlage für Websitesammlung. Die Richtlinien können also gezielter für den Inhalt in einer bestimmten Websitesammlung angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p113">Unlike the previous two examples, these policies are assigned to a specific site collection — not the site collection template. This means the policies can be more specifically tailored for the content in a specific site collection.</span></span>
  
<span data-ttu-id="fec8a-p114">Richtlinien und Regeln werden vererbt. Websitebesitzer können für ihre Website eine Richtlinie und Regel auswählen, und alle Unterwebsites erben die Richtlinie von der übergeordneten Website. Ein Besitzer einer Unterwebsite kann aber die Vererbung aufheben, indem er eine andere Richtlinie und Regel auswählt, die wiederum für alle Unterwebsites gilt, bis die Vererbung wieder aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p114">Policies and rules are inherited. Site owners can select a policy and rule for their site, and all subsites inherit the policy from the parent. However, an owner of a subsite can break inheritance by selecting a different policy and rule, which in turn applies to all subsites until inheritance is broken again.</span></span>
  
<span data-ttu-id="fec8a-156">Um dieses Szenario einzurichten, können Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="fec8a-156">To set up this scenario, you can:</span></span>
  
1. <span data-ttu-id="fec8a-157">Erstellen Sie mehrere Richtlinien, die jeweils mindestens eine Regel enthalten.</span><span class="sxs-lookup"><span data-stu-id="fec8a-157">Create several policies that each contains one or more rules.</span></span>
    
2. <span data-ttu-id="fec8a-158">Legen Sie eine Richtlinie und Regel als den Standard fest.</span><span class="sxs-lookup"><span data-stu-id="fec8a-158">Set a policy and rule as the default.</span></span>
    
3. <span data-ttu-id="fec8a-159">Weisen Sie die Richtlinien einer bestimmten Websitesammlung zu.</span><span class="sxs-lookup"><span data-stu-id="fec8a-159">Assign the policies to a specific site collection.</span></span>
    
<span data-ttu-id="fec8a-160">Außerdem werden die Richtlinien und Regeln für eine bestimmte Websitesammlung angepasst, bei der die Websitebesitzer die Vererbung aufheben können, indem sie die Richtlinie und Regel auswählen, die sich am besten für ihre Website eignet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-160">In addition, the policies and rules are tailored to a specific site collection, where site owners can break inheritance by selecting the policy and rule that best applies to their site.</span></span>
  
![Diagramm mit vielen Richtlinien und Regeln](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a><span data-ttu-id="fec8a-162">Erstellen einer Dokumentlöschrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fec8a-162">Create a document deletion policy</span></span>

1. <span data-ttu-id="fec8a-p115">Navigieren Sie im Office &amp; 365Security Compliance Center zur **Aufbewahrung**von **Datenverwaltung** \> . Klicken Sie unter **Löschen**auf **Dokument Löschrichtlinien für SharePoint Online und OneDrive for Business verwalten**. Das Dokument Löschrichtlinien Center wird in einer neuen Registerkarte des Browsers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p115">In the Office 365Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
    <span data-ttu-id="fec8a-p116">Wenn Sie zum ersten Mal vom Security &amp; Compliance Center zum Dokument Löschrichtlinien Center navigieren, wird das Richtlinien Center automatisch für Sie erstellt. Alternativ können Sie das Richtlinien Center manuell erstellen, indem Sie [die Websitesammlung erstellen](http://go.microsoft.com/fwlink/p/?LinkID=404342) und auf der Registerkarte **Enterprise** die Option **Compliance Policy Center** auswählen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p116">The first time you navigate from the Security &amp; Compliance Center to the Document Deletion Policy Center, the policy center is automatically created for you. Alternatively, you can manually create the policy center by [creating the site collection](http://go.microsoft.com/fwlink/p/?LinkID=404342) and choosing **Compliance Policy Center** on the **Enterprise** tab.</span></span> 
    
2. <span data-ttu-id="fec8a-168">Wählen Sie **Löschrichtlinien**aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-168">Choose **Deletion Policies**.</span></span>
    
    ![Option "Löschrichtlinien"](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="fec8a-170">Wählen Sie **Neues Element** aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-170">Choose **new item**.</span></span>
    
4. <span data-ttu-id="fec8a-p117">Geben Sie einen Namen und eine Beschreibung für die Richtlinie ein. Websitebesitzer wählen eine Richtlinie möglicherweise aufgrund ihres Namens und ihrer Beschreibung aus. Geben Sie daher ausreichende Informationen an, damit sie die richtige Richtlinie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p117">Enter a policy name and description. Site owners may be selecting a policy for their site based on this name and description, so include enough information for them to choose the correct policy.</span></span>
    
5. <span data-ttu-id="fec8a-173">Um eine Regel zu erstellen, wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-173">To create a rule, choose **New**.</span></span>
    
6. <span data-ttu-id="fec8a-174">Geben Sie einen Namen ein, und wählen Sie die folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="fec8a-174">Enter a name and choose the following options:</span></span>
    
  - <span data-ttu-id="fec8a-p118">Wählen Sie aus, ob die Regel Dokumente dauerhaft löschen oder in den Papierkorb löschen soll. Der Papierkorb bietet ein Sicherheitsnetz in der zweiten Stufe, bevor ein Element dauerhaft aus einer Website gelöscht wird. Weitere Informationen zum Papierkorb finden Sie unter [leeren des Papierkorbs oder Wiederherstellen der Dateien](http://go.microsoft.com/fwlink/p/?LinkID=404348).</span><span class="sxs-lookup"><span data-stu-id="fec8a-p118">Choose whether the rule will permanently delete documents or delete them to the Recycle Bin. The Recycle Bin provides a second-stage safety net before an item is permanently deleted from a site. For more information about the Recycle Bin, see [Empty the Recycle Bin or restore your files](http://go.microsoft.com/fwlink/p/?LinkID=404348).</span></span>
    
  - <span data-ttu-id="fec8a-178">Wählen Sie aus, ob das Löschdatum ab dem Datum der Dokumenterstellung oder der letzten Dokumentänderung berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fec8a-178">Choose whether the deletion date is calculated from the date when a document was created or last modified.</span></span>
    
  - <span data-ttu-id="fec8a-179">Geben Sie die Anzahl der Tage, Monate oder Jahre als Zeitraum ein, nach dem das Dokument gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fec8a-179">Enter a number of days, months, or years as the time period after which a document will be deleted.</span></span>
    
  - <span data-ttu-id="fec8a-p119">Wählen Sie, ob die Regel eine Standardregel ist. Die erste Regel, die Sie erstellen, wird automatisch als die Standardregel festgelegt. Eine Standardregel wird automatisch auf alle Bibliotheken auf den Websites angewendet, die die Richtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p119">Choose whether the rule is a default rule. The first rule that you create is automatically set as the default rule. A default rule is automatically applied to all libraries in the sites that use the policy.</span></span>
    
![Seite "Neue Löschregel"](media/IP-New-deletion-rule.png)
  
7. <span data-ttu-id="fec8a-184">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-184">Click **Save**.</span></span>
    
8. <span data-ttu-id="fec8a-p120">Erstellen Sie zusätzliche Regeln, wenn Sie zulassen möchten, dass Websitebesitzer andere Regeln auswählen und auf ihre Website anwenden können. Falls vorhanden wird die Standardregel angewendet, wenn der Websitebesitzer keine Aktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p120">Create additional rules if you want site owners to be able to choose different rules to apply to their site. The default rule, if any, will be applied if the site owner takes no action.</span></span>
    
9. <span data-ttu-id="fec8a-187">Wenn Sie eine Regel aus einer Richtlinie entfernen möchten, wählen Sie die Regel aus, klicken Sie auf **Löschen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-187">To remove a rule from a policy, select the rule, click **Delete**, and then click **OK**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fec8a-188">Wenn Sie eine Regel löschen und die Richtlinie keine Standardregel enthält, wird für diese Richtlinie keine Regel angewendet, d. h., es werden keine Dokumente gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fec8a-188">If you delete a rule, and the policy does not contain a default rule, then no rule will be in effect for that policy—in other words, no documents will be deleted.</span></span> 
  
![Meldung zum Bestäntigen des Entfernens einer Regel für eine Richtlinie](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a><span data-ttu-id="fec8a-190">Zuweisen der Dokumentlöschrichtlinie zu einer Vorlage für Websitesammlung</span><span class="sxs-lookup"><span data-stu-id="fec8a-190">Assign the document deletion policy to a site collection template</span></span>

<span data-ttu-id="fec8a-191">Durch das Zuweisen einer Richtlinie zu einer Vorlage für Websitesammlung machen Sie die Richtlinie für alle Websitesammlungen verfügbar, die aufgrund dieser Vorlage erstellt werden, einschließlich bereits vorhandener und künftiger Websitesammlungen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-191">By assigning a policy to a site collection template, you make the policy available to all site collections created from that template, including both existing site collections and site collections created in the future.</span></span>
  
<span data-ttu-id="fec8a-p121">Es ist wichtig zu wissen, dass es sich bei dem für eine Dokument Löschrichtlinie angegebenen Zeitraum um die Zeit seit dem Erstellen oder Ändern des Dokuments handelt, nicht um den Zeitpunkt, zu dem die Richtlinie zugewiesen wurde. Wenn Sie die Richtlinie zum ersten Mal zuweisen, werden alle Dokumente auf der Website ausgewertet, und wenn Sie die Kriterien erfüllen, werden Sie gelöscht. Dies gilt für alle vorhandenen Dokumente, nicht nur für neue Dokumente, die seit dem Zuweisen der Richtlinie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p121">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="fec8a-p122">Navigieren Sie im &amp; Security Compliance Center zur **Aufbewahrung**von **Datenverwaltung** \> . Klicken Sie unter **Löschen**auf **Dokument Löschrichtlinien für SharePoint Online und OneDrive for Business verwalten**. Das Dokument Löschrichtlinien Center wird in einer neuen Registerkarte des Browsers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p122">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="fec8a-198">Wählen Sie **Richtlinienzuweisungen für Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-198">Choose **Policy Assignments for Templates**.</span></span>
    
    ![Option "Richtlinienzuweisungen für Vorlagen"](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. <span data-ttu-id="fec8a-200">Wählen Sie **Neues Element** aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-200">Choose **new item**.</span></span>
    
4. <span data-ttu-id="fec8a-201">Führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="fec8a-201">Do one of the following:</span></span>
    
  - <span data-ttu-id="fec8a-202">Um die Richtlinie einer Vorlage für Websitesammlung wie die Teamwebsitevorlage zuzuweisen, wählen Sie **Vorlage für Websitesammlung zuweisen** aus, und wählen Sie die Vorlage für Websitesammlung.</span><span class="sxs-lookup"><span data-stu-id="fec8a-202">To assign the policy to a site collection template such as the Team Site template, select **Assign to site collection template**, and then select the site collection template.</span></span>
    
  - <span data-ttu-id="fec8a-203">Wenn Sie die Richtlinie dem einen Laufwerk für Unternehmen der Benutzer zuweisen möchten, wählen Sie **OneDrive für Business-Vorlage zuweisen**aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-203">To assign the policy to users' One Drive for Business, choose **Assign to OneDrive for Business Template**, highlighted below.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fec8a-204">Wenn Sie eine Richtlinie zu einer Vorlage für Websitesammlung zuweisen, wird die Richtlinie für bereits vorhandene Websitesammlungen, die aufgrund dieser Vorlage erstellt wurden, und für künftige Websitesammlungen verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="fec8a-204">When you assign a policy to a site collection template, that policy will be available both to existing site collections created from that template and to site collections created in the future.</span></span> 
  
![Seite "Vorlage wählen" mit der Option "OneDrive"](media/IP-Choose-a-template.png)
  
5. <span data-ttu-id="fec8a-206">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-206">Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fec8a-p123">Jeder Vorlage kann nur eine Gruppe von Richtlinien zugewiesen werden. Wenn eine Fehlermeldung angezeigt wird, dass dieser Vorlage bereits Richtlinien zugewiesen wurden, wählen \*\*\*\* \> Sie im linken Navigations \> Bereich " **Websitesammlung zuweisen** " aus wählen Sie eine Websitesammlung aus, um die Gruppe von Richtlinien anzuzeigen und zu verwalten, die bereits vorhanden sind. zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p123">Each template can have only one set of policies assigned to it. If you see an error saying that this template already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** in the left navigation \> select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
6. <span data-ttu-id="fec8a-p124">Wählen Sie **zugewiesene Richtlinien verwalten**aus, wählen Sie die Richtlinien aus, die Sie zuweisen möchten, und wählen Sie dann aus, ob eine Richtlinie die Standardrichtlinie ist. Wenn Sie eine Standardrichtlinie festlegen, haben alle Websites, die der Richtlinie zugewiesen sind, automatisch die Richtlinie aktiv, ohne dass für den Websitebesitzer eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p124">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![Seite "Richtlinien hinzufügen und verwalten"](media/IP-Add-and-manage-policies-page.png)
  
7. <span data-ttu-id="fec8a-212">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-212">Click **Save**.</span></span>
    
8. <span data-ttu-id="fec8a-p125">Wenn Sie die Richtlinie auf allen Websites erzwingen möchten, ohne zuzulassen, dass Websitebesitzer sie abwählen können, wählen Sie **Richtlinie als obligatorisch kennzeichnen** aus. Wenn Sie eine Richtlinie als obligatorisch kennzeichnen, kann einer Vorlage für Websitesammlung nur diese einzelne Richtlinie zugewiesen werden. Die Richtlinie muss außerdem als Standard gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p125">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection template. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="fec8a-216">Wenn diese Option ausgegraut ist, wählen Sie **Zugewiesene Richtlinien verwalten** aus, und stellen Sie sicher, dass mindestens eine Richtlinie zugewiesen und als Standard festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-216">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
9. <span data-ttu-id="fec8a-217">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-217">Click **Save**.</span></span>
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a><span data-ttu-id="fec8a-218">Zuweisen der Dokumentlöschrichtlinie zu einer Websitesammlung</span><span class="sxs-lookup"><span data-stu-id="fec8a-218">Assign the document deletion policy to a site collection</span></span>

<span data-ttu-id="fec8a-p126">Durch das Zuweisen einer Richtlinie zu einer bestimmten Websitesammlung machen Sie die Richtlinie nur für diese Websitesammlung verfügbar. Sie können also Richtlinien näher an den Inhalt in der Websitesammlung anpassen. Außerdem setzen Richtlinien, die einer bestimmten Websitesammlung zugewiesen werden, alle Richtlinien, die der Vorlage für diese Websitesammlung zugewiesen sind, außer Kraft. Zum Beispiel setzt eine Richtlinie, die der (aus der Teamwebsitevorlage erstellten) Websitesammlung Vertriebsabteilung zugewiesen ist, alle Richtlinien außer Kraft, die der Teamwebsitevorlage zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p126">By assigning a policy to a specific site collection, you make the policy available only to that specific site collection. This means you can tailor policies more closely to the content in the site collection. Also, policies assigned to a specific site collection will override any policies that are assigned to the template for that site collection. For example, a policy assigned to the Sales Department site collection (created from the Team Site template) will override any policies assigned to the Team Site template.</span></span>
  
<span data-ttu-id="fec8a-p127">Es ist wichtig zu wissen, dass es sich bei dem für eine Dokument Löschrichtlinie angegebenen Zeitraum um die Zeit seit dem Erstellen oder Ändern des Dokuments handelt, nicht um den Zeitpunkt, zu dem die Richtlinie zugewiesen wurde. Wenn Sie die Richtlinie zum ersten Mal zuweisen, werden alle Dokumente auf der Website ausgewertet, und wenn Sie die Kriterien erfüllen, werden Sie gelöscht. Dies gilt für alle vorhandenen Dokumente, nicht nur für neue Dokumente, die seit dem Zuweisen der Richtlinie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p127">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="fec8a-p128">Navigieren Sie im &amp; Security Compliance Center zur **Aufbewahrung**von **Datenverwaltung** \> . Wählen Sie unter **Löschen**die Option **Dokument Löschrichtlinien für SharePoint Online und OneDrive for Business verwalten**aus. Das Dokument Löschrichtlinien Center wird in einer neuen Registerkarte des Browsers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p128">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="fec8a-229">Wählen Sie **Richtlinienzuweisungen für Websitesammlungen**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-229">Choose **Policy Assignments for Site Collections**.</span></span>
    
    ![Option "Richtlinienzuweisungen für Websitesammlungen"](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. <span data-ttu-id="fec8a-231">Wählen Sie **Neues Element** aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-231">Choose **new item**.</span></span>
    
4. <span data-ttu-id="fec8a-p129">Wählen Sie **Websitesammlung auswählen**aus. Suchen Sie nach der Websitesammlung nach Name oder URL, wählen Sie die Websitesammlung aus, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p129">Choose **Choose a site collection**. Search for the site collection by name or URL, select the site collection and click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fec8a-p130">Jeder Websitesammlung kann nur eine Gruppe von Richtlinien zugewiesen werden. Wenn eine Fehlermeldung angezeigt wird, dass dieser Websitesammlung bereits Richtlinien zugewiesen wurden, wählen Sie **"** \> der **Websitesammlung zuweisen** " aus, und wählen Sie eine Websitesammlung aus, um die bereits zugewiesenen Richtlinien anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p130">Each site collection can have only one set of policies assigned to it. If you see an error saying that this site collection already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** and select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
![Seite "Websitesammlung auswählen"](media/IP-Choose-a-site-collection-page.png)
  
5. <span data-ttu-id="fec8a-p131">Wählen Sie **zugewiesene Richtlinien verwalten**aus, wählen Sie die Richtlinien aus, die Sie zuweisen möchten, und wählen Sie dann aus, ob eine Richtlinie die Standardrichtlinie ist. Wenn Sie eine Standardrichtlinie festlegen, haben alle Websites, die der Richtlinie zugewiesen sind, automatisch die Richtlinie aktiv, ohne dass für den Websitebesitzer eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p131">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![Seite "Richtlinien hinzufügen und verwalten"](media/IP-Add-and-manage-policies-page.png)
  
6. <span data-ttu-id="fec8a-240">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-240">Click **Save**.</span></span>
    
7. <span data-ttu-id="fec8a-p132">Wenn Sie die Richtlinie auf allen Websites erzwingen möchten, ohne zuzulassen, dass Websitebesitzer sie abwählen können, wählen Sie **Richtlinie als obligatorisch kennzeichnen** aus. Wenn Sie eine Richtlinie als obligatorisch kennzeichnen, kann einer Websitesammlung nur diese einzelne Richtlinie zugewiesen werden. Die Richtlinie muss außerdem als Standard gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p132">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="fec8a-244">Wenn diese Option ausgegraut ist, wählen Sie **Zugewiesene Richtlinien verwalten** aus, und stellen Sie sicher, dass mindestens eine Richtlinie zugewiesen und als Standard festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fec8a-244">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
8. <span data-ttu-id="fec8a-245">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-245">Click **Save**.</span></span>
    
## <a name="delete-a-policy-assignment"></a><span data-ttu-id="fec8a-246">Löschen einer Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="fec8a-246">Delete a policy assignment</span></span>

<span data-ttu-id="fec8a-247">Wenn Sie eine Zuweisung löschen, werden die zugewiesenen Richtlinien nicht mehr auf die Websites in der Websitesammlung oder Vorlage für Websitesammlung angewendet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-247">When you delete an assignment, the assigned policies will no longer apply to any sites in the site collection or site collection template.</span></span>
  
1. <span data-ttu-id="fec8a-p133">Navigieren Sie im &amp; Security Compliance Center zur **Aufbewahrung**von **Datenverwaltung** \> . Wählen Sie unter **Löschen**die Option **Dokument Löschrichtlinien für SharePoint Online und OneDrive for Business verwalten**aus. Das Dokument Löschrichtlinien Center wird in einer neuen Registerkarte des Browsers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p133">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="fec8a-251">Wählen Sie entweder \*\*Richtlinienzuweisungen für Vorlagen \*\* oder **Richtlinienzuweisungen für Websitesammlungen**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-251">Choose either **Policy Assignments for Templates** or **Policy Assignments for Site Collections**.</span></span>
    
3. <span data-ttu-id="fec8a-252">Wählen Sie das Zuordnungselement aus, und klicken Sie auf **Element löschen**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-252">Select the assignment item and click **Delete Item**.</span></span>
    
    ![Befehl "Element löschen" für Richtlinienzuweisung](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a><span data-ttu-id="fec8a-254">Löschen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fec8a-254">Delete a policy</span></span>

<span data-ttu-id="fec8a-p134">Sie können keine Richtlinie löschen, die verwendet wird. Bevor Sie eine Richtlinie löschen können, müssen Sie zuerst alle Zuordnungen zu Websitesammlungen und Websitesammlungsvorlagen löschen, die diese Richtlinie enthalten – siehe den vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p134">You can't delete a policy that's in use. Before you can delete a policy, you first need to delete all assignments to site collections and site collection templates that include that policy—see the previous section.</span></span>
  
1. <span data-ttu-id="fec8a-p135">Wählen Sie im &amp; Security Compliance \> Center in der linken Navigations \> Leiste unter **Delete** \> Manage Document Deletion Policies \> for SharePoint Online und OneDrive die **Aufbewahrung** von **Datenverwaltung** aus. \*\* für Unternehmen\*\*. Das Dokument Löschrichtlinien Center wird in einer neuen Registerkarte des Browsers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p135">In the Security &amp; Compliance Center \> choose **Data management** \> **Retention** in the left navigation \> under **Delete** \> **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="fec8a-259">Wählen Sie \* \* Löschrichtlinien \* \* aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-259">Choose \*\* Deletion Policies \*\*.</span></span>
    
    ![Option "Löschrichtlinien"](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="fec8a-261">Wählen Sie die Richtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-261">Select the policy.</span></span>
    
4. <span data-ttu-id="fec8a-262">Klicken Sie auf \> der Register \> Karte Menü Band **Elemente** auf **Richtlinie entfernen**.</span><span class="sxs-lookup"><span data-stu-id="fec8a-262">On the Ribbon \> **Items** tab \> **Remove Policy**.</span></span>
    
    ![Schaltfläche "Richtlinie entfernen" auf Menüband](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. <span data-ttu-id="fec8a-p136">Wenn die Richtlinie verwendet wird, werden Sie gefragt, ob Sie die Richtlinie aus allen Websitesammlungen entfernen möchten, in denen Sie verwendet wird. Wenn Sie sicher sind, wählen Sie **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="fec8a-p136">If the policy is in use, you'll be asked if you want to remove the policy from all of the site collections where it's being used. If you're sure, choose **OK**.</span></span>
    
    ![Bestätigungsmeldung für "Richtlinie löschen"](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a><span data-ttu-id="fec8a-267">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fec8a-267">See also</span></span>

[<span data-ttu-id="fec8a-268">Übersicht über Dokumentlöschrichtlinien</span><span class="sxs-lookup"><span data-stu-id="fec8a-268">Overview of document deletion policies</span></span>](document-deletion-policies.md)

[<span data-ttu-id="fec8a-269">Anwenden oder Entfernen einer Dokumentlöschrichtlinie für eine Website</span><span class="sxs-lookup"><span data-stu-id="fec8a-269">Apply or remove a document deletion policy for a site</span></span>](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 


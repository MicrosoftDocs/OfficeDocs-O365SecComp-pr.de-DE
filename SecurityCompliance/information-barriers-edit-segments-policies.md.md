---
title: Bearbeiten oder Entfernen von Richtlinien für Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Hier erfahren Sie, wie Sie Richtlinien für Informationsbarrieren bearbeiten oder entfernen.
ms.openlocfilehash: e6bed4df2329d426f86bd4cde07bdc7d1a2792cd
ms.sourcegitcommit: 7c48ce016fa9f45a3813467f7c5a2fd72f9b8f49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2019
ms.locfileid: "35215648"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="d887b-103">Bearbeiten oder Entfernen von Richtlinien für Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d887b-103">Edit or remove information barrier policies (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="d887b-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d887b-104">Overview</span></span>

<span data-ttu-id="d887b-105">Nachdem Sie [Richtlinien für Informationsbarrieren definiert](information-barriers-policies.md)haben, müssen Sie möglicherweise im Rahmen der [Problembehandlung](information-barriers-troubleshooting.md) oder als regelmäßige Wartung Änderungen an diesen Richtlinien oder an Ihren Benutzersegmenten vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d887b-105">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="d887b-106">Verwenden Sie diesen Artikel als Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="d887b-106">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d887b-107">Um die in diesem Artikel beschriebenen Aufgaben ausführen zu können, muss Ihnen eine entsprechende Rolle zugewiesen sein, beispielsweise eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="d887b-107">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="d887b-108">-Microsoft 365 Enterprise-Global-Administrator</span><span class="sxs-lookup"><span data-stu-id="d887b-108">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="d887b-109">-Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="d887b-109">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="d887b-110">-Compliance-Administrator</span><span class="sxs-lookup"><span data-stu-id="d887b-110">- Compliance Administrator</span></span><br/><span data-ttu-id="d887b-111">-IB-Compliance-Management (Dies ist eine neue Rolle!)</span><span class="sxs-lookup"><span data-stu-id="d887b-111">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="d887b-112">Weitere Informationen zu den Voraussetzungen für Informationsbarrieren finden Sie unter Prerequisites [(for Information Barrier Policies)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="d887b-112">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="d887b-113">Stellen Sie sicher, dass Sie [eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d887b-113">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="d887b-114">Bearbeiten von Benutzerkonto Attributen</span><span class="sxs-lookup"><span data-stu-id="d887b-114">Edit user account attributes</span></span>

<span data-ttu-id="d887b-115">Verwenden Sie dieses Verfahren zum Bearbeiten von Attributen, die für die Segmentierung von Benutzern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d887b-115">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="d887b-116">Wenn Sie beispielsweise ein Department-Attribut verwenden und für ein oder mehrere Benutzerkonten derzeit keine Werte für die Abteilung aufgeführt sind, müssen Sie diese Benutzerkonten bearbeiten, um Abteilungsinformationen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="d887b-116">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="d887b-117">Benutzerkontoattribute werden für die Definition von Segmenten verwendet, sodass Richtlinien für Informationsbarrieren zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="d887b-117">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="d887b-118">Verwenden Sie zum Anzeigen von Details für ein bestimmtes Benutzerkonto, wie Attributwerte und zugewiesene Segmente, das Cmdlet **Get-InformationBarrierRecipientStatus** mit Identitäts Parametern.</span><span class="sxs-lookup"><span data-stu-id="d887b-118">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

   <span data-ttu-id="d887b-119">Syntax`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="d887b-119">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 
    
   <span data-ttu-id="d887b-120">Sie können einen beliebigen Wert verwenden, der jeden Benutzer eindeutig identifiziert, beispielsweise Name, Alias, Distinguished Name, kanonischer Domänenname, e-Mail-Adresse oder GUID.</span><span class="sxs-lookup"><span data-stu-id="d887b-120">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 
    
   <span data-ttu-id="d887b-121">Beispiel: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="d887b-121">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 
    
   <span data-ttu-id="d887b-122">In diesem Beispiel wird auf zwei Benutzerkonten in Office 365 verwiesen: *meganb* für *Megan*und *alexw* für *Alex*.</span><span class="sxs-lookup"><span data-stu-id="d887b-122">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
   <span data-ttu-id="d887b-123">(Sie können dieses Cmdlet auch für einen einzelnen Benutzer verwenden: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="d887b-123">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> 
    
2. <span data-ttu-id="d887b-124">Bestimmen Sie, welches Attribut Sie für Ihr Benutzerkontoprofil (en) bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d887b-124">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="d887b-125">Weitere Informationen finden Sie unter [Attribute for Information Barrier Policies (Preview)](information-barriers-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d887b-125">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="d887b-126">Bearbeiten Sie ein oder mehrere Benutzerkonten, um Werte für das Attribut einzuschließen, das Sie im vorherigen Schritt ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d887b-126">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="d887b-127">Verwenden Sie dazu eines der folgenden Verfahren:</span><span class="sxs-lookup"><span data-stu-id="d887b-127">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="d887b-128">Informationen zum Bearbeiten eines einzelnen Kontos finden Sie unter [Hinzufügen oder Aktualisieren der Profilinformationen eines Benutzers mithilfe von Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="d887b-128">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="d887b-129">Informationen zum Bearbeiten mehrerer Konten (oder zum Bearbeiten eines einzelnen Kontos mithilfe von PowerShell) finden Sie unter [Konfigurieren von Benutzerkontoeigenschaften mit Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="d887b-129">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="d887b-130">Bearbeiten eines Segments</span><span class="sxs-lookup"><span data-stu-id="d887b-130">Edit a segment</span></span>

<span data-ttu-id="d887b-131">Verwenden Sie dieses Verfahren bearbeiten der Definition eines Benutzersegments.</span><span class="sxs-lookup"><span data-stu-id="d887b-131">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="d887b-132">Beispielsweise können Sie den Namen eines Segments oder den Filter ändern, der verwendet wird, um zu bestimmen, wer im Segment enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d887b-132">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="d887b-133">Verwenden Sie das Cmdlet **Get-OrganizationSegment** , um alle vorhandenen Segmente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d887b-133">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="d887b-134">Syntax`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="d887b-134">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="d887b-135">Es wird eine Liste mit Segmenten und Details für jede, wie Segmenttyp, den UserGroupFilter-Wert, der erstellt oder zuletzt geändert, Guid, und so weiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d887b-135">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="d887b-136">Drucken oder speichern Sie die Liste der Segmente als Referenz später.</span><span class="sxs-lookup"><span data-stu-id="d887b-136">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="d887b-137">Wenn Sie beispielsweise ein Segment bearbeiten möchten, müssen Sie dessen Namen oder den Wert ermitteln (dieser wird mit dem Parameter Identity verwendet).</span><span class="sxs-lookup"><span data-stu-id="d887b-137">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="d887b-138">Verwenden Sie zum Bearbeiten eines Segments das Cmdlet " **OrganizationSegment** " mit dem Parameter " **Identity** " und den relevanten Details.</span><span class="sxs-lookup"><span data-stu-id="d887b-138">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="d887b-139">Syntax`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="d887b-139">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="d887b-140">Beispiel: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="d887b-140">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="d887b-141">In diesem Beispiel haben wir für das Segment mit dem GUID- *c96e0837-C232-4a8a-841e-ef45787d8fcd*den Namen der Abteilung in "HRDept" geändert.</span><span class="sxs-lookup"><span data-stu-id="d887b-141">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="d887b-142">Wenn Sie die Bearbeitung von Segmenten für Ihre Organisation abgeschlossen haben, können Sie die Richtlinien für Informationsbarrieren entweder [definieren](information-barriers-policies.md#part-2-define-information-barrier-policies) oder [Bearbeiten](#edit-a-policy) .</span><span class="sxs-lookup"><span data-stu-id="d887b-142">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="d887b-143">Bearbeiten einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d887b-143">Edit a policy</span></span>

1. <span data-ttu-id="d887b-144">Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d887b-144">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="d887b-145">Syntax`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="d887b-145">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="d887b-146">Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="d887b-146">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="d887b-147">Beachten Sie die GUID und den Namen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d887b-147">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="d887b-148">Verwenden Sie das Cmdlet "InformationBarrierPolicy" mit einem **Identity** **-** Parameter, und geben Sie die Änderungen an, die Sie vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="d887b-148">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="d887b-149">Beispiel: angenommen, eine Richtlinie wurde definiert, um zu verhindern, dass das *Forschungs* Segment mit den *Vertriebs* -und *Marketing* Segmenten kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="d887b-149">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="d887b-150">Die Richtlinie wurde mithilfe dieses Cmdlets definiert:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="d887b-150">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="d887b-151">Angenommen, wir möchten diese ändern, damit Personen im *Forschungs* Segment nur mit Personen im *HR* -Segment kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="d887b-151">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="d887b-152">Um diese Änderung vorzunehmen, verwenden wir dieses Cmdlet:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="d887b-152">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="d887b-153">In diesem Beispiel haben wir "SegmentsBlocked" in "SegmentsAllowed" geändert und das *HR* -Segment angegeben.</span><span class="sxs-lookup"><span data-stu-id="d887b-153">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="d887b-154">Wenn Sie die Bearbeitung einer Richtlinie abgeschlossen haben, sollten Sie Ihre Änderungen übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d887b-154">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="d887b-155">(Weitere Informationen finden Sie unter [Apply Information Barrier Policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span><span class="sxs-lookup"><span data-stu-id="d887b-155">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="d887b-156">Festlegen einer Richtlinie auf inaktiver Status</span><span class="sxs-lookup"><span data-stu-id="d887b-156">Set a policy to inactive status</span></span>

1. <span data-ttu-id="d887b-157">Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d887b-157">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="d887b-158">Syntax`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="d887b-158">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="d887b-159">Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie ändern möchten (oder entfernen).</span><span class="sxs-lookup"><span data-stu-id="d887b-159">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="d887b-160">Beachten Sie die GUID und den Namen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d887b-160">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="d887b-161">Um den Status der Richtlinie auf inaktiv festzulegen, verwenden Sie das Cmdlet "InformationBarrierPolicy" mit einem Identity-Parameter und dem State **-** Parameter auf "inaktiv" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d887b-161">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="d887b-162">Syntax`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="d887b-162">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="d887b-163">In diesem Beispiel wird eine Richtlinie für Informationsbarrieren festgelegt, die GUID *43c37853-EA10-4b90-a23d-ab8c9377247* in einen inaktiven Status hat.</span><span class="sxs-lookup"><span data-stu-id="d887b-163">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="d887b-164">Verwenden Sie das Cmdlet **Start-InformationBarrierPoliciesApplication** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d887b-164">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="d887b-165">Syntax`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="d887b-165">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="d887b-166">Änderungen werden angewendet, Benutzer nach Benutzer, für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="d887b-166">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="d887b-167">Wenn Ihre Organisation groß ist, kann es 24 Stunden (oder mehr) dauern, bis dieser Prozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d887b-167">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="d887b-168">(Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.)</span><span class="sxs-lookup"><span data-stu-id="d887b-168">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="d887b-169">Zu diesem Zeitpunkt werden mindestens eine Richtlinie für Informationsbarrieren auf inaktiver Status festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d887b-169">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="d887b-170">Von hier aus können Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d887b-170">From here, you can do any of the following:</span></span>
- <span data-ttu-id="d887b-171">Beibehalten (eine auf inaktiven Status festgelegte Richtlinie hat keine Auswirkungen auf die Benutzer)</span><span class="sxs-lookup"><span data-stu-id="d887b-171">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="d887b-172">Bearbeiten einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d887b-172">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="d887b-173">Entfernen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d887b-173">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="d887b-174">Entfernen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d887b-174">Remove a policy</span></span>

1. <span data-ttu-id="d887b-175">Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d887b-175">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="d887b-176">Syntax`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="d887b-176">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="d887b-177">Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="d887b-177">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="d887b-178">Beachten Sie die GUID und den Namen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d887b-178">Note the policy's GUID and name.</span></span> <span data-ttu-id="d887b-179">Stellen Sie sicher, dass die Richtlinie auf inaktiver Status festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d887b-179">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="d887b-180">Verwenden Sie das Cmdlet **Remove-InformationBarrierPolicy** mit einem Identity-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d887b-180">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="d887b-181">Syntax`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="d887b-181">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="d887b-182">Beispiel: nehmen wir an, dass eine Richtlinie mit GUID- *43c37853-EA10-4b90-a23d-ab8c93772471*entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d887b-182">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="d887b-183">Zu diesem Zweck verwenden wir dieses Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d887b-183">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="d887b-184">Bestätigen Sie die Änderung, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d887b-184">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="d887b-185">Wiederholen Sie die Schritte 1-2 für jede Richtlinie, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="d887b-185">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="d887b-186">Wenn Sie das Entfernen von Richtlinien abgeschlossen haben, wenden Sie die Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="d887b-186">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="d887b-187">Verwenden Sie dazu das Cmdlet **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="d887b-187">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="d887b-188">Syntax`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="d887b-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="d887b-189">Änderungen werden angewendet, Benutzer nach Benutzer, für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="d887b-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="d887b-190">Wenn Ihre Organisation groß ist, kann es 24 Stunden (oder mehr) dauern, bis dieser Prozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d887b-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="d887b-191">Beenden einer Richtlinienanwendung</span><span class="sxs-lookup"><span data-stu-id="d887b-191">Stop a policy application</span></span>

<span data-ttu-id="d887b-192">Wenn Sie die Anwendung von Richtlinien für Informationsbarrieren gestartet haben und diese Richtlinien nicht mehr angewendet werden sollen, verwenden Sie das folgende Verfahren.</span><span class="sxs-lookup"><span data-stu-id="d887b-192">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="d887b-193">Denken Sie daran, dass es ungefähr 30-35 Minuten dauern wird, bis der Prozess beginnt.</span><span class="sxs-lookup"><span data-stu-id="d887b-193">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="d887b-194">Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** , um den Status der neuesten Informations Barriere-Richtlinienanwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d887b-194">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="d887b-195">Syntax`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="d887b-195">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="d887b-196">Beachten Sie die GUID der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d887b-196">Note the application's GUID.</span></span>

2. <span data-ttu-id="d887b-197">Verwenden Sie das Cmdlet **Stop-InformationBarrierPoliciesApplication** mit einem Identity-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d887b-197">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="d887b-198">Syntax`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="d887b-198">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="d887b-199">Beispiel: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="d887b-199">Example: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

    <span data-ttu-id="d887b-200">In diesem Beispiel wird das Anwenden von Richtlinien für Informationsbarrieren angehalten.</span><span class="sxs-lookup"><span data-stu-id="d887b-200">In this example, we are stopping information barrier policies from being applied.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d887b-201">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="d887b-201">Related articles</span></span>

[<span data-ttu-id="d887b-202">Hier erhalten Sie einen Überblick über Informationsbarrieren</span><span class="sxs-lookup"><span data-stu-id="d887b-202">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="d887b-203">Definieren von Richtlinien für Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d887b-203">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="d887b-204">Weitere Informationen zu Informationsbarrieren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d887b-204">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="d887b-205">Attribute für Richtlinien für Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d887b-205">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="d887b-206">Problembehandlung bei Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d887b-206">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)

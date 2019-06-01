---
title: Problembehandlung bei Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Verwenden Sie diesen Artikel als Leitfaden für die Problembehandlung von Informationsbarrieren.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668301"
---
# <a name="troubleshooting-information-barriers-preview"></a><span data-ttu-id="d3a37-103">Problembehandlung bei Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d3a37-103">Troubleshooting information barriers (Preview)</span></span>

<span data-ttu-id="d3a37-104">Informationsbarrieren können dazu beitragen, dass Ihre Organisation weiterhin den gesetzlichen Bestimmungen und Branchenvorschriften entspricht.</span><span class="sxs-lookup"><span data-stu-id="d3a37-104">Information barriers can help your organization remain compliant with legal requirements and industry regulations.</span></span> <span data-ttu-id="d3a37-105">Beispielsweise können Sie mit Informationsbarrieren die Kommunikation zwischen bestimmten Benutzergruppen einschränken, um einen Interessenkonflikt oder andere Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d3a37-105">For example, with information barriers, you can restrict communication between specific groups of users to avoid a conflict of interest or other issues.</span></span> <span data-ttu-id="d3a37-106">Weitere Informationen finden Sie unter [Information Barriers (Preview)](information-barriers.md).</span><span class="sxs-lookup"><span data-stu-id="d3a37-106">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span>

<span data-ttu-id="d3a37-107">Dieser Artikel enthält Anleitungen, die Sie verwenden können, um Antworten auf Fragen zu erhalten oder Probleme zu beheben, die mit Informationsbarrieren auftreten können.</span><span class="sxs-lookup"><span data-stu-id="d3a37-107">This article provides guidance you can use to get answers to questions or resolve issues that may arise with information barriers.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="d3a37-108">Bevor Sie beginnen...</span><span class="sxs-lookup"><span data-stu-id="d3a37-108">Before you begin...</span></span>

<span data-ttu-id="d3a37-109">Um die in diesem Artikel beschriebenen Aufgaben ausführen zu können, muss Ihnen eine entsprechende Rolle zugewiesen sein, beispielsweise eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="d3a37-109">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span>
- <span data-ttu-id="d3a37-110">Microsoft 365 Enterprise-Global-Administrator</span><span class="sxs-lookup"><span data-stu-id="d3a37-110">Microsoft 365 Enterprise Global Administrator</span></span>
- <span data-ttu-id="d3a37-111">Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="d3a37-111">Office 365 Global Administrator</span></span>
- <span data-ttu-id="d3a37-112">Complianceadministrator</span><span class="sxs-lookup"><span data-stu-id="d3a37-112">Compliance Administrator</span></span>
- <span data-ttu-id="d3a37-113">IB-Konformitätsverwaltung (Dies ist eine neue Rolle!)</span><span class="sxs-lookup"><span data-stu-id="d3a37-113">IB Compliance Management (this is a new role!)</span></span>

<span data-ttu-id="d3a37-114">Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Berechtigungen im Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d3a37-114">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="d3a37-115">Weitere Informationen zu den Voraussetzungen für Informationsbarrieren finden Sie unter Prerequisites [(for Information Barrier Policies)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="d3a37-115">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span>

<span data-ttu-id="d3a37-116">Stellen Sie außerdem sicher, dass Sie [eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d3a37-116">Also, make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a><span data-ttu-id="d3a37-117">Problem: Personen werden unerwartet für die Kommunikation in Microsoft Teams blockiert</span><span class="sxs-lookup"><span data-stu-id="d3a37-117">Issue: People are unexpectedly blocked from communicating in Microsoft Teams</span></span> 

<span data-ttu-id="d3a37-118">In diesem Fall melden Personen unerwartete Probleme, die in Microsoft Teams miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d3a37-118">In this case, people are reporting unexpected issues communicating in Microsoft Teams.</span></span> <span data-ttu-id="d3a37-119">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="d3a37-119">Examples:</span></span>
- <span data-ttu-id="d3a37-120">Ein Benutzer kann keinen anderen Benutzer in Microsoft Teams finden oder mit ihm kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d3a37-120">A user is unable to find or communicate with another user in Microsoft Teams.</span></span>
- <span data-ttu-id="d3a37-121">Ein Benutzer kann einen anderen Benutzer in Microsoft Teams nicht anzeigen oder auswählen.</span><span class="sxs-lookup"><span data-stu-id="d3a37-121">A user cannot see or select another user in Microsoft Teams.</span></span>
- <span data-ttu-id="d3a37-122">Ein Benutzer kann Nachrichten an einen anderen Benutzer in Microsoft Teams anzeigen, aber nicht senden.</span><span class="sxs-lookup"><span data-stu-id="d3a37-122">A user can see, but cannot send messages to, another user in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="d3a37-123">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d3a37-123">What to do</span></span>

1. <span data-ttu-id="d3a37-124">Bestimmen Sie, ob die Benutzer von einer Informations Sperrrichtlinie betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="d3a37-124">Determine whether the users are affected by an information barrier policy.</span></span> <span data-ttu-id="d3a37-125">Verwenden Sie dazu das Cmdlet **Get-InformationBarrierRecipientStatus** mit dem Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="d3a37-125">To do this, use the **Get-InformationBarrierRecipientStatus** cmdlet with the Identity parameter.</span></span> 

    <span data-ttu-id="d3a37-126">Die Syntax lautet`Get-InformationBarrierRecipientStatus -Identity`</span><span class="sxs-lookup"><span data-stu-id="d3a37-126">The syntax is `Get-InformationBarrierRecipientStatus -Identity`</span></span>

    <span data-ttu-id="d3a37-127">Sie können jeden Identitätswert verwenden, der jeden Empfänger eindeutig identifiziert, beispielsweise Name, Alias, DN (Distinguished Name), kanonischer DN, e-Mail-Adresse oder GUID.</span><span class="sxs-lookup"><span data-stu-id="d3a37-127">You can use any identity value that uniquely identifies each recipient, such as Name, Alias, Distinguished name (DN), Canonical DN, Email address, or GUID.</span></span>

    <span data-ttu-id="d3a37-128">Beispiel: `Get-InformationBarrierRecipientStatus -Identity meganb`</span><span class="sxs-lookup"><span data-stu-id="d3a37-128">Example: `Get-InformationBarrierRecipientStatus -Identity meganb`</span></span>

    <span data-ttu-id="d3a37-129">In diesem Beispiel wird ein Alias (*meganb*) für den Parameter Identity verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3a37-129">In this example, we are using an alias (*meganb*) for the Identity parameter.</span></span> <span data-ttu-id="d3a37-130">Dieses Cmdlet gibt Informationen zurück, die angeben, ob der Benutzer von einer Richtlinie für Informationsbarrieren betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="d3a37-130">This cmdlet will return information that indicates whether the user is affected by an information barrier policy.</span></span> <span data-ttu-id="d3a37-131">(Suchen Sie nach \* ExoPolicyId \<: GUID>.)</span><span class="sxs-lookup"><span data-stu-id="d3a37-131">(Look for \*ExoPolicyId: \<GUID>.)</span></span>

    <span data-ttu-id="d3a37-132">Wenn die Benutzer nicht in Richtlinien für Informationsbarrieren enthalten sind, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="d3a37-132">If the users are not included in information barrier policies, contact support.</span></span> <span data-ttu-id="d3a37-133">Führen Sie andernfalls die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d3a37-133">Otherwise, proceed to the next step.</span></span>

2. <span data-ttu-id="d3a37-134">Finden Sie heraus, welche Segmente in einer Informations Sperrrichtlinie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d3a37-134">Find out which segments are included in an information barrier policy.</span></span> <span data-ttu-id="d3a37-135">Verwenden Sie dazu das `Get-InformationBarrierPolicy` Cmdlet mit dem Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="d3a37-135">To do this, use the `Get-InformationBarrierPolicy` cmdlet with the Identity parameter.</span></span> <span data-ttu-id="d3a37-136">Verwenden Sie Details wie die Richtlinien-GUID (ExoPolicyId), die Sie während des vorherigen Schritts erhalten haben, als Identitätswert.</span><span class="sxs-lookup"><span data-stu-id="d3a37-136">Use details, such as the policy GUID (ExoPolicyId) you received during the previous step, as an identity value.</span></span>

    <span data-ttu-id="d3a37-137">Beispiel: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span><span class="sxs-lookup"><span data-stu-id="d3a37-137">Example: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span></span>

    <span data-ttu-id="d3a37-138">In diesem Beispiel werden detaillierte Informationen zur Richtlinie mit Informationsbarrieren abgerufen, die ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*enthält.</span><span class="sxs-lookup"><span data-stu-id="d3a37-138">In this example, we are getting detailed information about the information barrier policy that has ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span></span>
    
    <span data-ttu-id="d3a37-139">Suchen Sie nach dem Ausführen des Cmdlets in den Ergebnissen nach **AssignedSegment**-, **SegmentsAllowed**-und **SegmentsBlocked** -Werten.</span><span class="sxs-lookup"><span data-stu-id="d3a37-139">After you run the cmdlet, in the results, look for **AssignedSegment**, **SegmentsAllowed**, and **SegmentsBlocked** values.</span></span>

    <span data-ttu-id="d3a37-140">Beispiel: nach dem Ausführen `Get-InformationBarrierPolicy` des Cmdlets haben wir in der Ergebnisliste Folgendes gesehen:</span><span class="sxs-lookup"><span data-stu-id="d3a37-140">Example: After running the `Get-InformationBarrierPolicy` cmdlet, we saw the following in our list of results:</span></span>

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    <span data-ttu-id="d3a37-141">In diesem Fall können wir sehen, dass eine Informations Barriere-Richtlinie Personen betrifft, die sich in den Segmenten Vertrieb und Forschung befinden.</span><span class="sxs-lookup"><span data-stu-id="d3a37-141">In this case, we can see that an information barrier policy affects people who are in the Sales and Research segments.</span></span> <span data-ttu-id="d3a37-142">In diesem Fall werden Personen im Vertrieb daran gehindert, mit Personen in der Forschung zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d3a37-142">In this case, people in Sales are prevented from communicating with people in Research.</span></span> <span data-ttu-id="d3a37-143">Wenn dies richtig erscheint, funktionieren Informationsbarrieren wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="d3a37-143">If this seems correct, then information barriers are working as expected.</span></span> <span data-ttu-id="d3a37-144">Wenn dies nicht der Fall ist, fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="d3a37-144">If not, proceed to the next step.</span></span>

4. <span data-ttu-id="d3a37-145">Stellen Sie sicher, dass ihre Segmente ordnungsgemäß definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d3a37-145">Make sure your segments are defined correctly.</span></span> <span data-ttu-id="d3a37-146">Verwenden Sie dazu das `Get-OrganizationSegment` Cmdlet, und überprüfen Sie die Ergebnisliste.</span><span class="sxs-lookup"><span data-stu-id="d3a37-146">To do this, use the `Get-OrganizationSegment` cmdlet, and review the list of results.</span></span> 

    <span data-ttu-id="d3a37-147">Um Details für ein bestimmtes Segment anzuzeigen, verwenden Sie `Get-OrganizationSegment` das-Cmdlet mit einem Identity-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3a37-147">To view details for a specific segment, use the `Get-OrganizationSegment` cmdlet with an Identity parameter.</span></span> 

    <span data-ttu-id="d3a37-148">Beispiel: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span><span class="sxs-lookup"><span data-stu-id="d3a37-148">Example: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span></span>

    <span data-ttu-id="d3a37-149">In diesem Beispiel werden Informationen zu dem Segment abgerufen, das über GUID- *c96e0837-C232-4a8a-841e-ef45787d8fcd*verfügt.</span><span class="sxs-lookup"><span data-stu-id="d3a37-149">In this example, we are getting information about the segment that has GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span></span>

    <span data-ttu-id="d3a37-150">Überprüfen Sie die Details für das Segment.</span><span class="sxs-lookup"><span data-stu-id="d3a37-150">Review the details for the segment.</span></span> <span data-ttu-id="d3a37-151">Bearbeiten Sie bei Bedarf [ein Segment](information-barriers-policies.md#edit-a-segment), und verwenden Sie dann das `Start-InformationBarrierPoliciesApplication` Cmdlet erneut.</span><span class="sxs-lookup"><span data-stu-id="d3a37-151">If necessary, [edit a segment](information-barriers-policies.md#edit-a-segment), and then re-use the `Start-InformationBarrierPoliciesApplication` cmdlet.</span></span>

    <span data-ttu-id="d3a37-152">Wenn Sie weiterhin Probleme mit ihrer Richtlinie zu Informationsbarrieren haben, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="d3a37-152">If you are still having issues with your information barrier policy, contact support.</span></span>
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a><span data-ttu-id="d3a37-153">Problem: der Anwendungsprozess für Informationsbarrieren dauert zu lange.</span><span class="sxs-lookup"><span data-stu-id="d3a37-153">Issue: The information barrier application process is taking too long</span></span>

<span data-ttu-id="d3a37-154">Nach dem Ausführen des Cmdlets **Start-InformationBarrierPoliciesApplication** dauert es sehr lange, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d3a37-154">After running the **Start-InformationBarrierPoliciesApplication** cmdlet, the process is taking a really long time to finish.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="d3a37-155">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d3a37-155">What to do</span></span>

1. <span data-ttu-id="d3a37-156">Beachten Sie, dass beim Ausführen des Cmdlets für die Richtlinienanwendung für alle Konten in Ihrer Organisation Richtlinien für Informationsbarrieren angewendet (oder entfernt) werden, Benutzer nach Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d3a37-156">Keep in mind that when you run the policy application cmdlet, information barrier policies are being applied (or removed), user by user, for all accounts in your organization.</span></span> <span data-ttu-id="d3a37-157">Wenn Sie viele Benutzer haben, dauert es eine Weile, bis Sie verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d3a37-157">If you have a lot of users, it will take a while to process.</span></span> <span data-ttu-id="d3a37-158">(Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.)</span><span class="sxs-lookup"><span data-stu-id="d3a37-158">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span> 

2. <span data-ttu-id="d3a37-159">Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** , um den Status zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d3a37-159">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet to verify status.</span></span>

    <span data-ttu-id="d3a37-160">Syntax`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="d3a37-160">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="d3a37-161">Verwenden Sie zum Anzeigen des Status für alle Richtlinien Anwendungen für Informationsbarrieren`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="d3a37-161">To display status for all information barrier policy applications, use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span>

    <span data-ttu-id="d3a37-162">Dadurch werden Informationen darüber angezeigt, ob die Richtlinienanwendung abgeschlossen, ein Fehler aufgetreten ist oder ausgeführt wird..</span><span class="sxs-lookup"><span data-stu-id="d3a37-162">This will display information about whether policy application completed, failed, or is in progress..</span></span>

3. <span data-ttu-id="d3a37-163">Führen Sie je nach den Ergebnissen von Schritt 2 einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d3a37-163">Depending on the results of step 2, take one of the following steps:</span></span>

    - <span data-ttu-id="d3a37-164">Wenn die Anwendung nicht gestartet wurde und seit der Ausführung des **Start-InformationBarrierPoliciesApplication-** Cmdlets mehr als 45 Minuten dauern, überprüfen Sie Ihr Überwachungsprotokoll, um zu ermitteln, ob Fehler in Richtlinien Definitionen vorliegen, oder aus einem anderen Grund, warum die die Anwendung wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3a37-164">If the application has not started, and it has been more than 45 minutes since the **Start-InformationBarrierPoliciesApplication** cmdlet has been run, review your audit log to see if there are any errors in policy definitions, or some other reason why the application has not started.</span></span>

    - <span data-ttu-id="d3a37-165">Wenn die Anwendung fehlgeschlagen ist, überprüfen Sie Ihre Segmente und Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d3a37-165">If the application has failed, review your segments and policies.</span></span> <span data-ttu-id="d3a37-166">Bearbeiten Sie gegebenenfalls [Segmente](information-barriers-policies.md#edit-a-segment) und/oder [Bearbeiten Sie Richtlinien](information-barriers-policies.md#edit-a-policy), und führen Sie dann das Cmdlet **Start-InformationBarrierPoliciesApplication** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d3a37-166">If necessary, [edit segments](information-barriers-policies.md#edit-a-segment) and/or [edit policies](information-barriers-policies.md#edit-a-policy), and then run the **Start-InformationBarrierPoliciesApplication** cmdlet again.</span></span>

    - <span data-ttu-id="d3a37-167">Wenn die Anwendung noch ausgeführt wird, lassen Sie mehr Zeit für ihre Ausführung zu.</span><span class="sxs-lookup"><span data-stu-id="d3a37-167">If the application is still in progress, allow more time for it to complete.</span></span> <span data-ttu-id="d3a37-168">Wenn es sich um mehrere Tage handelt, wenden Sie sich an den Support.</span><span class="sxs-lookup"><span data-stu-id="d3a37-168">If it has been several days, contact support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3a37-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d3a37-169">Related topics</span></span>

[<span data-ttu-id="d3a37-170">Definieren von Richtlinien für Informationsbarrieren in Microsoft Teams (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d3a37-170">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="d3a37-171">Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d3a37-171">Information barriers (Preview)</span></span>](information-barriers.md)




---
title: Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Nach der Deaktivierung eines Office 365-Postfachs können Sie die Dauer des Haltestatus oder die der dem inaktiven Postfach zugewiesene Aufbewahrungsrichtlinie für Office 365 ändern. Die Aufbewahrungsdauer definiert, wie lange Elemente im Ordner "Wiederherstellbare Elemente" aufbewahrt werden.
ms.openlocfilehash: f51750a0e822a4786f332639203b08ba4b5e2ba7
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295888"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="03343-104">Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365</span><span class="sxs-lookup"><span data-stu-id="03343-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="03343-p102">Ein inaktives Postfach wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Ein Postfach wird inaktiv, wenn das Postfach in einem Beweissicherungsverfahren, in einem In-Situ-Speicher, in einer Office 365-Aufbewahrungsrichtlinie oder in einem Haltebereich platziert, der mit einem eDiscovery-Fall verknüpft ist, und das entsprechende Office 365-Benutzerkonto gelöscht wird. Die Inhalte eines inaktiven Postfachs werden für die Dauer der Archivierung beibehalten, die für das Postfach aktiviert wurde, bevor es inaktiv gemacht wurde. Die Aufbewahrungsdauer definiert die Aufbewahrungsdauer von Elementen im Ordner „Wiederherstellbare Elemente". Wenn die Aufbewahrungsdauer für ein Element im Ordner „Wiederherstellbare Elemente" abläuft, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht. Nachdem ein Postfach als inaktiv markiert wurde, können Sie die Aufbewahrungsdauer oder die Office 365-Aufbewahrungsrichtlinie für das inaktive Postfach ändern.</span><span class="sxs-lookup"><span data-stu-id="03343-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="03343-p103">Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers.</span><span class="sxs-lookup"><span data-stu-id="03343-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="03343-116">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="03343-116">Before you begin</span></span>

- <span data-ttu-id="03343-p104">Zum Ändern der Aufbewahrungsdauer für ein Beweissicherungsverfahren für ein aktives Postfach müssen Sie die Exchange Online PowerShell verwenden. Sie können nicht die Exchange-Verwaltungskonsole (EAC) verwenden. Sie können Exchange Online PowerShell oder die Exchange-Verwaltungskonsole jedoch verwenden, um die Aufbewahrungsdauer für einen In-Situ-Speicher zu ändern. Sie können die Office 365 Security &amp; Compliance Center oder die Security &amp; Compliance Center PowerShell zum Ändern der Aufbewahrungsdauer für eine Office 365-Aufbewahrungsrichtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="03343-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="03343-121">Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell oder Security &amp; Compliance Center PowerShell finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="03343-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - <span data-ttu-id="03343-122">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="03343-122">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)</span></span>
    
  - [<span data-ttu-id="03343-123">Herstellen einer Verbindung mit Office 365 Security &amp; Compliance Center PowerShell</span><span class="sxs-lookup"><span data-stu-id="03343-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="03343-p105">Beachten Sie, dass Haltebereiche, die eDiscovery-Fällen zugeordnet sind, unendliche Haltebereiche sind, was bedeutet, dass es keine Dauer gibt, die geändert werden kann. Elemente werden dauerhaft aufbewahrt oder bis der Haltebereich entfernt wird und das inaktive Postfach gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="03343-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="03343-126">Weitere Informationen zu inaktiven Postfächern finden Sie unter inAktive [Postfächer in Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="03343-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="03343-127">Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach</span><span class="sxs-lookup"><span data-stu-id="03343-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="03343-128">Da unterschiedliche Haltebereiche oder eine oder mehrere Office 365-Aufbewahrungsrichtlinien für ein inaktives Postfach aktiviert werden können, besteht der erste Schritt darin, die Haltebereiche für ein inaktives Postfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="03343-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="03343-129">Führen Sie in Exchange Online PowerShell den folgenden Befehl aus, um die Informationen zu Haltebereichen für alle inaktiven Postfächer in Ihrer Organisation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="03343-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="03343-p106">Der Wert von **true** für die **LitigationHoldEnabled** -Eigenschaft gibt an, dass das inaktive Postfach in einem Rechtsstreit gehalten wird. Wenn ein in-situ-Speicher, eine eDiscovery-Speicherung oder eine Office 365-Aufbewahrungsrichtlinie in einem inaktiven Postfach platziert wird, wird als Wert für die **InPlaceHolds** -Eigenschaft eine GUID für die halte-oder Aufbewahrungsrichtlinie angezeigt. Das folgende Beispiel zeigt die Ergebnisse für 5 inaktive Postfächer.</span><span class="sxs-lookup"><span data-stu-id="03343-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
<span data-ttu-id="03343-133">In der folgenden Tabelle sind fünf unterschiedliche Haltebereichstypen aufgeführt, die verwendet wurden, um die einzelnen Postfächer als inaktiv zu markieren.</span><span class="sxs-lookup"><span data-stu-id="03343-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="03343-134">**Inaktives Postfach**</span><span class="sxs-lookup"><span data-stu-id="03343-134">**Inactive mailbox**</span></span>|<span data-ttu-id="03343-135">**Haltebereichstyp**</span><span class="sxs-lookup"><span data-stu-id="03343-135">**Hold type**</span></span>|<span data-ttu-id="03343-136">**Wie Sie den Haltebereich für das inaktive Postfach erkennen**</span><span class="sxs-lookup"><span data-stu-id="03343-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03343-137">Ann Beebe</span><span class="sxs-lookup"><span data-stu-id="03343-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="03343-138">Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="03343-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="03343-139">Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.</span><span class="sxs-lookup"><span data-stu-id="03343-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="03343-140">Pilar Pinilla</span><span class="sxs-lookup"><span data-stu-id="03343-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="03343-141">Compliance-Archiv</span><span class="sxs-lookup"><span data-stu-id="03343-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="03343-p107">Die  *InPlaceHolds*  -Eigenschaft enthält die GUID des In-Situ-Speichers, in dem das inaktive Postfach platziert wird. Sie können erkennen, dass es sich hierbei um einen In-Situ-Speichern handelt, da die ID nicht mit einem Präfix beginnt.  </span><span class="sxs-lookup"><span data-stu-id="03343-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="03343-144">Sie können den `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` Befehl in Exchange Online PowerShell verwenden, um Informationen zum in-situ-Speicher für das inaktive Postfach zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="03343-144">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="03343-145">Mario Necaise</span><span class="sxs-lookup"><span data-stu-id="03343-145">Mario Necaise</span></span>  <br/> |<span data-ttu-id="03343-146">Organisationsweite Office 365-Aufbewahrungsrichtlinie in der Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="03343-146">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="03343-p108">Die *InPlaceHolds* -Eigenschaft ist leer. Dies weist darauf hin, dass eine oder mehrere organisationsweite oder (Exchange-weite) Office 365-Aufbewahrungsrichtlinien auf das inaktive Postfach angewendet werden. In diesem Fall können Sie den `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl in Exchange Online PowerShell ausführen, um eine Liste der GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen. Die GUID für organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer angewendet werden `mbx` , beginnen mit dem Präfix; Beispiel `mbxa3056bb15562480fadb46ce523ff7b02`.</span><span class="sxs-lookup"><span data-stu-id="03343-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <br/><span data-ttu-id="03343-151">Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu ermitteln, die auf das inaktive Postfach angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="03343-151">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span>  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|<span data-ttu-id="03343-152">Carol Olson</span><span class="sxs-lookup"><span data-stu-id="03343-152">Carol Olson</span></span>  <br/> |<span data-ttu-id="03343-153">Office 365-Aufbewahrungsrichtlinie in Security &amp; Compliance Center angewendet auf bestimmte Postfächer</span><span class="sxs-lookup"><span data-stu-id="03343-153">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="03343-p109">Die  *InPlaceHolds*  -Eigenschaft enthält die GUID der Office 365-Aufbewahrungsrichtlinie, die auf das inaktive Postfach angewendet wird. Sie können erkennen, dass es sich hierbei um eine Aufbewahrungsrichtlinie handelt, die auf bestimmte Postfächer angewendet wurde, da die GUID mit dem Präfix  `mbx` beginnt. Wenn die GUID der Aufbewahrungsrichtlinie, die auf das inaktive Postfach angewendet wird, mit dem Präfix  `skp` beginnt, würde dies darauf hindeuten, dass die Aufbewahrungsrichtlinie auf Skype for Business-Unterhaltungen angewendet wird.  </span><span class="sxs-lookup"><span data-stu-id="03343-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="03343-157">Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu ermitteln, die auf das inaktive Postfach angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="03343-157">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/><span data-ttu-id="03343-158">Entfernen Sie unbedingt das `mbx` Präfix oder `skp` , wenn Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="03343-158">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="03343-159">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="03343-159">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="03343-160">eDiscovery-Fall in der Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="03343-160">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="03343-p110">Die  *InPlaceHolds*  -Eigenschaft enthält die GUID des eDiscovery-Falls, in dem das inaktive Postfach platziert wird. Sie können erkennen, dass es sich hierbei um einen eDiscovery-Fall handelt, da die GUID mit dem Präfix  `UniH` beginnt.  </span><span class="sxs-lookup"><span data-stu-id="03343-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="03343-p111">Sie können das `Get-CaseHoldPolicy` Cmdlet im Security &amp; Compliance Center PowerShell verwenden, um Informationen über den eDiscovery-Fall abzurufen, dem der Haltebereich für das inaktive Postfach zugeordnet ist. Sie können beispielsweise den Befehl `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` ausführen, um den Namen der Groß-/Kleinschreibung für das inaktive Postfach anzuzeigen. Achten Sie darauf, das `UniH` Präfix zu entfernen, wenn Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="03343-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="03343-166">Führen Sie die folgenden Befehle aus, um den eDiscovery-Fall zu identifizieren, mit dem der Haltebereich für das inaktive Postfach verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="03343-166">To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.</span></span>  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> <span data-ttu-id="03343-p112">**Hinweis:** Es wird nicht empfohlen, eDiscovery-Speicher für inaktive Postfächer zu verwenden. Das liegt daran, dass eDiscovery-Fälle für bestimmte, zeitlich gebundene Fälle im Zusammenhang mit einem rechtlichen Problem vorgesehen sind. Zu einem bestimmten Zeitpunkt wird möglicherweise ein Rechtsstreit beendet, und die dem Fall zugeordneten haltebereiche werden entfernt, und der eDiscovery-Fall wird geschlossen (oder gelöscht). Wenn ein Haltebereich in einem inaktiven Postfach einem eDiscovery-Fall zugeordnet ist und der Haltestatus freigegeben oder der eDiscovery-Fall geschlossen oder gelöscht wird, wird das inaktive Postfach dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="03343-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="03343-171">Weitere Informationen zu Office 365-Aufbewahrungsrichtlinien finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="03343-171">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="03343-172">Schritt 2: Ändern der Aufbewahrungsdauer für ein inaktives Postfach</span><span class="sxs-lookup"><span data-stu-id="03343-172">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="03343-173">Nachdem Sie ermittelt haben, welche Art von Haltebereich für das inaktive Postfach aktiviert ist (und ob es mehrere Haltebereiche gibt), wird im nächsten Schritt die Dauer des Haltebereichs geändert.</span><span class="sxs-lookup"><span data-stu-id="03343-173">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="03343-174">Ändern der Dauer für ein Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="03343-174">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="03343-p113">Im Folgenden erfahren Sie, wie Sie die Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer für ein Beweissicherungsverfahren verwenden, das auf einem inaktiven Postfach platziert wird. Sie können nicht die EAC verwenden. Führen Sie zum Ändern der Aufbewahrungsdauer den folgenden Befehl aus. In diesem Beispiel wird die Aufbewahrungsdauer auf unbegrenzt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="03343-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="03343-179">Dadurch werden die Elemente im inaktiven Postfach unbegrenzt beibehalten oder bis der Haltebereich entfernt oder die Aufbewahrungsdauer in einen anderen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="03343-179">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="03343-p114">Die beste Methode zum Identifizieren eines inaktiven Postfachs ist die Verwendung des **Distinguished Name** oder des **Exchange GUID** -Werts. Durch Verwenden eines dieser Werte können Sie verhindern, versehentlich das falsche Postfach anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03343-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="03343-182">Ändern der Dauer für einen In-Situ-Speicher</span><span class="sxs-lookup"><span data-stu-id="03343-182">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="03343-183">Sie können die Exchange-Verwaltungskonsole oder Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer für einen In-Situ-Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="03343-183">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="03343-184">Verwenden von EAC zum Ändern der Aufbewahrungsdauer</span><span class="sxs-lookup"><span data-stu-id="03343-184">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="03343-p115">Wenn Sie den Namen des in-situ-Speichers kennen, den Sie ändern möchten, fahren Sie mit dem nächsten Schritt fort. Führen Sie andernfalls den folgenden Befehl aus, um den Namen des in-situ-Speichers abzurufen, der im inaktiven Postfach platziert wird. Verwenden Sie die in-situ-Aufbewahrungs-GUID, die Sie in [Schritt 1](#step-1-identify-the-holds-on-an-inactive-mailbox)abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="03343-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="03343-188">Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.</span><span class="sxs-lookup"><span data-stu-id="03343-188">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="03343-189">Wählen Sie den in-situ-Speicher aus, den Sie ändern möchten \*\*\*\* ![, und klicken](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Sie dann auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="03343-189">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="03343-190">Klicken Sie auf der Eigenschaftenseite für den \*\*in-situ-eDiscovery &amp; \*\* -Speicher auf **in-situ-Aufbewahrung**.</span><span class="sxs-lookup"><span data-stu-id="03343-190">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="03343-191">Nehmen Sie auf Grundlage der aktuellen Aufbewahrungsdauer eine der folgenden Aktionen vor:</span><span class="sxs-lookup"><span data-stu-id="03343-191">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="03343-192">Klicken Sie auf **Dauerhaft aufbewahren**, um Elemente für einen unbegrenzten Zeitraum aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="03343-192">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="03343-p116">Klicken Sie auf **Anzahl von Tagen angeben, die Elemente in Bezug auf Ihr Empfangsdatum enthalten** sollen, um Elemente für einen bestimmten Zeitraum aufzubewahren. Geben Sie die Anzahl der Tage ein, für die Sie Elemente speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="03343-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![Screenshot: Ändern der Dauer für einen In-Situ-Speicher](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="03343-196">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="03343-196">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="03343-197">Verwenden von Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer</span><span class="sxs-lookup"><span data-stu-id="03343-197">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="03343-p117">Wenn Sie den Namen des in-situ-Speichers kennen, den Sie ändern möchten, fahren Sie mit dem nächsten Schritt fort. Führen Sie andernfalls den folgenden Befehl aus, um den Namen des in-situ-Speichers abzurufen, der im inaktiven Postfach platziert wird. Verwenden Sie die in-situ-Aufbewahrungs-GUID, die Sie in [Schritt 1](#step-1-identify-the-holds-on-an-inactive-mailbox)abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="03343-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="03343-p118">Führen Sie zum Ändern der Aufbewahrungsdauer den folgenden Befehl aus. In diesem Beispiel wird die Aufbewahrungsdauer in 2.555 Tage (etwa 7 Jahre) geändert.</span><span class="sxs-lookup"><span data-stu-id="03343-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="03343-203">Verwenden Sie  _-ItemHoldPeriod unlimited_, um die Aufbewahrungsdauer in einen unbegrenzten Zeitraum zu ändern.</span><span class="sxs-lookup"><span data-stu-id="03343-203">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="03343-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03343-204">More information</span></span>

- <span data-ttu-id="03343-p119">**Wie wird die Aufbewahrungsdauer für ein Element in einem inaktiven Postfach berechnet?** Die Dauer wird anhand des ursprünglichen Datums berechnet, an dem ein Postfach empfangen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="03343-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="03343-p120">**Was geschieht, wenn die Aufbewahrungsdauer abläuft?** Wenn die Aufbewahrungsdauer für ein Postfachelement im Ordner „Wiederherstellbare Elemente" abläuft, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht. Wenn für den auf dem inaktiven Postfach platzierten Haltebereich keine Dauer angegeben ist, werden Elemente im Ordner „Wiederherstellbare Elemente" niemals gelöscht (es sei denn, die Aufbewahrungsdauer für das inaktive Postfach wird geändert).</span><span class="sxs-lookup"><span data-stu-id="03343-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="03343-p121">**Wird eine Exchange-Aufbewahrungsrichtlinie für inaktive Postfächer weiterhin verarbeitet?** Wenn eine Exchange-Aufbewahrungsrichtlinie (Messaging-Datensatzverwaltung, MRM-Funktion inExchange Online) auf ein Postfach angewendet wurde, als es als inaktiv markiert wurde, werden die Löschrichtlinien (hierbei handelt es sich um Aufbewahrungstags mit der Aufbewahrungsaktion **Delete** ) weiterhin auf das inaktive Postfach angewendet. Mit einer Löschrichtlinie markierte Elemente werden demnach in den Ordner „Wiederherstellbare Elemente" verschoben, wenn die Aufbewahrungsrichtlinie abläuft. Diese Elemente werden dann aus dem inaktiven Postfach gelöscht, wenn die Aufbewahrungsdauer für ein Element abläuft.</span><span class="sxs-lookup"><span data-stu-id="03343-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="03343-p122">Umgekehrt werden einem inaktiven Postfach zugewiesene Archivrichtlinien (mit der Aufbewahrungsaktion **MoveToArchive** konfigurierte Aufbewahrungstags) ignoriert, die in der Aufbewahrungsrichtlinie enthalten sind. Elemente in einem inaktiven Postfach, die mit einer Archivrichtlinie markiert sind, verbleiben demnach im primären Postfach, wenn die Aufbewahrungsdauer abläuft. Sie werden nicht in das Archivpostfach oder in den Ordner „Wiederherstellbare Elemente" im Archivpostfach verschoben. Da sich ein Benutzer nicht an einem inaktiven Postfach anmelden kann, gibt es keinen Grund, Rechenzentrumsressourcen für das Verarbeiten von Archivrichtlinien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="03343-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="03343-p123">**Führen Sie einen der folgenden Befehle aus, um die neue Aufbewahrungsdauer zu überprüfen.** Der erste Befehl ist für das Beweissicherungsverfahren, der zweite für den In-Situ-Speicher.</span><span class="sxs-lookup"><span data-stu-id="03343-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="03343-p124">**Wie bei regulären Postfächern verarbeitet der Assistent für verwaltete Ordner auch inaktive Postfächer.** In Exchange Online verarbeitet der Assistent für verwaltete Ordner Postfächer einmal alle sieben Tage. Nachdem Sie die Aufbewahrungsdauer für ein inaktives Postfach geändert haben, können Sie das Cmdlet **Start-ManagedFolderAssistant** verwenden, um die Verarbeitung der neuen Aufbewahrungsdauer für das inaktive Postfach sofort zu starten. Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="03343-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="03343-p125">**Wenn viele Haltebereiche für ein inaktives Postfach aktiviert werden, werden nicht alle Haltebereich-GUIDs angezeigt.** Sie können den folgenden Befehl ausführen, um die GUIDs für alle Haltebereiche (mit Ausnahme von Beweissicherungsverfahren) für ein inaktives Postfach anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="03343-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```

---
title: Konfigurieren von privileged Access Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: In diesem Thema erfahren Sie mehr über das Konfigurieren von privileged Access Management in Office 365
ms.openlocfilehash: e086e93c268fe4de627bef30d3ac7aed8e6b1f98
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265237"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="1570c-103">Konfigurieren von privileged Access Management in Office 365</span><span class="sxs-lookup"><span data-stu-id="1570c-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1570c-104">Dieses Thema enthält Informationen zur Bereitstellung und Konfiguration von Features, die derzeit nur in Office 365 E5 und Advanced Compliance-SKUs verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1570c-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="1570c-105">Dieses Thema führt Sie durch die Aktivierung und Konfiguration der privilegierten Zugriffsverwaltung in Ihrer Office 365-Organisation.</span><span class="sxs-lookup"><span data-stu-id="1570c-105">This topic guides you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="1570c-106">Sie können entweder das Microsoft 365 Admin Center oder die Exchange-Verwaltungs-PowerShell verwenden, um den privilegierten Zugriff zu verwalten und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1570c-106">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="1570c-107">Aktivieren und Konfigurieren der Verwaltung privilegierter Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="1570c-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="1570c-108">Führen Sie die folgenden Schritte aus, um den privilegierten Zugriff in Ihrer Office 365-Organisation einzurichten und zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="1570c-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="1570c-109">Schritt 1: Erstellen der Gruppe einer genehmigenden Person</span><span class="sxs-lookup"><span data-stu-id="1570c-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="1570c-110">Bevor Sie mit dem Verwenden von Berechtigungszugriff beginnen, bestimmen Sie, wer die Genehmigungsautorität für eingehende Anforderungen für den Zugriff auf erhöhte und privilegierte Aufgaben benötigt.</span><span class="sxs-lookup"><span data-stu-id="1570c-110">Before you start using privilege access, determine who needs approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="1570c-111">Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist, kann Zugriffsanforderungen genehmigen.</span><span class="sxs-lookup"><span data-stu-id="1570c-111">Any user who is part of the Approvers’ group is able to approve access requests.</span></span> <span data-ttu-id="1570c-112">Dies wird durch das Erstellen einer e-Mail-aktivierten Sicherheitsgruppe in Office 365 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1570c-112">This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="1570c-113">Schritt 2: Aktivieren des privilegierten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="1570c-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="1570c-114">Privilegierter Zugriff muss in Office 365 explizit mit der standardmäßigen genehmigenden Gruppe aktiviert werden, einschließlich einer Reihe von Systemkonten, die Sie aus der Zugriffssteuerung für privilegierte Zugriffsverwaltung ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="1570c-114">Privileged access must be explicitly enabled in Office 365 with the default approver group, including a set of system accounts that you want excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="1570c-115">Schritt 3: Erstellen einer Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="1570c-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="1570c-116">Durch das Erstellen einer Genehmigungsrichtlinie können Sie die spezifischen Genehmigungsanforderungen für einzelne Aufgaben definieren.</span><span class="sxs-lookup"><span data-stu-id="1570c-116">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="1570c-117">Die Optionen für den Genehmigungs sind **automatisch** oder **manuell**.</span><span class="sxs-lookup"><span data-stu-id="1570c-117">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="1570c-118">Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen</span><span class="sxs-lookup"><span data-stu-id="1570c-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="1570c-119">Nach der Aktivierung erfordert der privilegierte Zugriff Genehmigungen für alle Aufgaben, für die eine zugehörige Genehmigungsrichtlinie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1570c-119">Once enabled, privileged access requires approvals for any task that has an associated approval policy defined.</span></span> <span data-ttu-id="1570c-120">Für Aufgaben, die in einer Genehmigungsrichtlinie enthalten sind, müssen Benutzer die Zugriffsgenehmigung anfordern und erhalten, um die zum Ausführen der Aufgabe erforderlichen Berechtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1570c-120">For tasks included in an approval policy, users must request and be granted access approval to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="1570c-121">Nachdem die Genehmigung erteilt wurde, kann der anfordernde Benutzer die vorgesehene Aufgabe ausführen, und der privilegierte Zugriff autorisiert und führt die Aufgabe im Namen des Benutzers aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-121">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on behalf of the user.</span></span> <span data-ttu-id="1570c-122">Die Genehmigung bleibt für die angeforderte Dauer (Standarddauer 4 Stunden) gültig, während der der anfordernde die vorgesehene Aufgabe mehrmals ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="1570c-122">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="1570c-123">Alle derartigen Ausführungen werden protokolliert und für die Sicherheits-und Konformitätsüberwachung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="1570c-123">All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="1570c-124">Wenn Sie die Exchange-Verwaltungsshell zum Aktivieren und Konfigurieren des privilegierten Zugriffs verwenden möchten, führen Sie die Schritte unter [Herstellen einer Verbindung mit Exchange Online PowerShell mithilfe der mehr](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) stufigen Authentifizierung zum Herstellen einer Verbindung mit Exchange Online PowerShell mit ihrem Office 365 aus. Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="1570c-124">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="1570c-125">Sie müssen die mehrstufige Authentifizierung für Ihre Office 365-Organisation nicht aktivieren, um die Schritte zum Aktivieren des privilegierten Zugriffs beim Herstellen einer Verbindung mit Exchange Online PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1570c-125">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="1570c-126">Beim Herstellen einer Verbindung mit mehrstufiger Authentifizierung wird ein OAuth-Token erstellt, das von privilegiertem Zugriff zum Signieren von Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1570c-126">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="1570c-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="1570c-127"></span></span>

## <a name="step-1-create-an-approvers-group"></a><span data-ttu-id="1570c-128">Schritt 1: Erstellen der Gruppe einer genehmigenden Person</span><span class="sxs-lookup"><span data-stu-id="1570c-128">Step 1: Create an approver's group</span></span>

1. <span data-ttu-id="1570c-129">Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1570c-129">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="1570c-130">Wechseln Sie im Admin Center zu **Gruppen** > **Hinzufügen einer Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="1570c-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="1570c-131">Wählen Sie **e-Mail-aktivierte Sicherheitsgruppe** aus, und füllen Sie die Felder **Name**, **Gruppen-e-Mail-Adresse**und **Beschreibung** für die neue Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-131">Select **mail-enabled security group** and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="1570c-132">Speichern Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1570c-132">Save the group.</span></span> <span data-ttu-id="1570c-133">Es kann einige Minuten dauern, bis die Gruppe vollständig konfiguriert ist und im Microsoft 365 Admin Center angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1570c-133">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="1570c-134">Wählen Sie die Gruppe neuer genehmigender aus, und wählen Sie **Bearbeiten** aus, um Benutzer zur Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1570c-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="1570c-135">Speichern Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1570c-135">Save the group.</span></span>

<span data-ttu-id="1570c-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="1570c-136"></span></span>

## <a name="step-2-enable-privileged-access"></a><span data-ttu-id="1570c-137">Schritt 2: Aktivieren des privilegierten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="1570c-137">Step 2: Enable privileged access</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-138">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-138">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="1570c-139">Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1570c-139">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="1570c-140">Navigieren Sie im Admin Center zu **Einstellungen > Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-141">Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .</span><span class="sxs-lookup"><span data-stu-id="1570c-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="1570c-142">Weisen Sie die Gruppe der genehmigenden Personen, die Sie in Schritt 1 erstellt haben, als **Standardgruppe für genehmigende**Personen zu.</span><span class="sxs-lookup"><span data-stu-id="1570c-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="1570c-143">**Speichern** und **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="1570c-143">**Save** and **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-144">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-144">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-145">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu aktivieren und die Gruppe der genehmigenden Personen zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="1570c-145">To enable privileged access and to assign the approver's group, run the following command in Exchange Online PowerShell:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="1570c-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="1570c-147">Das Feature "System Konten" wird bereitgestellt, um sicherzustellen, dass bestimmte Automatisierungen in Ihrer Organisation ohne Abhängigkeit vom privilegierten Zugriff funktionieren können, es wird jedoch empfohlen, dass diese Ausnahmen außergewöhnlich sind und diese zulässig sind. regelmäßig.</span><span class="sxs-lookup"><span data-stu-id="1570c-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="1570c-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="1570c-148"></span></span>

## <a name="step-3-create-an-access-policy"></a><span data-ttu-id="1570c-149">Schritt 3: Erstellen einer Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="1570c-149">Step 3: Create an access policy</span></span>

<span data-ttu-id="1570c-150">Sie können bis zu 30 privilegierte Zugriffsrichtlinien für Ihre Office 365-Organisation erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1570c-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-151">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-151">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="1570c-152">Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1570c-152">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="1570c-153">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-154">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="1570c-155">Wählen Sie **Richtlinien konfigurieren** aus, und wählen Sie **Richtlinie hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="1570c-156">Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="1570c-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="1570c-157">**Richtlinientyp**: Aufgabe, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="1570c-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="1570c-158">**Richtlinienbereich**: Exchange</span><span class="sxs-lookup"><span data-stu-id="1570c-158">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="1570c-159">**Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien aus</span><span class="sxs-lookup"><span data-stu-id="1570c-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="1570c-160">\*\*\*\* Genehmigungs: manuell oder automatisch</span><span class="sxs-lookup"><span data-stu-id="1570c-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="1570c-161">**Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte genehmigende Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="1570c-162">Klicken Sie auf **Erstellen** und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="1570c-162">Select **Create** and then **Close**.</span></span> <span data-ttu-id="1570c-163">Es kann einige Minuten dauern, bis die Richtlinie vollständig konfiguriert und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1570c-163">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-164">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-164">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-165">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsrichtlinie zu erstellen und zu definieren:</span><span class="sxs-lookup"><span data-stu-id="1570c-165">To create and define an approval policy, run the following command in Exchange Online PowerShell:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="1570c-166">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="1570c-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="1570c-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="1570c-168">Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen</span><span class="sxs-lookup"><span data-stu-id="1570c-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="1570c-169">Anfordern einer Erhöhungs Autorisierung zum Ausführen privilegierter Aufgaben</span><span class="sxs-lookup"><span data-stu-id="1570c-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="1570c-170">Anforderungen für den privilegierten Zugriff sind bis zu 24 Stunden nach der Übermittlung der Anforderung gültig.</span><span class="sxs-lookup"><span data-stu-id="1570c-170">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="1570c-171">Wenn diese nicht genehmigt oder verweigert werden, werden die Anforderungen ablaufen, und der Zugriff wird nicht genehmigt.</span><span class="sxs-lookup"><span data-stu-id="1570c-171">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-172">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-172">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="1570c-173">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://admin.microsoft.com) an.</span><span class="sxs-lookup"><span data-stu-id="1570c-173">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="1570c-174">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-175">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="1570c-176">Wählen Sie **neue Anforderung**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-176">Select **New request**.</span></span> <span data-ttu-id="1570c-177">Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="1570c-177">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="1570c-178">**Anforderungstyp**: Aufgabe, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="1570c-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="1570c-179">**Anforderungsbereich**: Exchange</span><span class="sxs-lookup"><span data-stu-id="1570c-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="1570c-180">**Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1570c-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="1570c-181">**Dauer (Stunden)**: Anzahl der Stunden des angeforderten Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="1570c-181">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="1570c-182">Es gibt keine Begrenzung für die Anzahl der Stunden, die angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="1570c-182">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="1570c-183">**Kommentare**: Textfeld für Kommentare in Bezug auf ihre Zugriffsanforderung</span><span class="sxs-lookup"><span data-stu-id="1570c-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="1570c-184">Klicken Sie auf **Speichern** und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="1570c-184">Select **Save** and then **Close**.</span></span> <span data-ttu-id="1570c-185">Ihre Anfrage wird per e-Mail an die Gruppe der genehmigenden Person gesendet.</span><span class="sxs-lookup"><span data-stu-id="1570c-185">Your request will be sent to the approver's group via email.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-186">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-186">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-187">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsanforderung an die Gruppe der genehmigenden Personen zu erstellen und zu übermitteln:</span><span class="sxs-lookup"><span data-stu-id="1570c-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="1570c-188">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="1570c-189">Anzeigen des Status von Ansichts Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1570c-189">View status of elevation requests</span></span>
<span data-ttu-id="1570c-190">Nachdem eine Genehmigungsanforderung erstellt wurde, kann der Status der Höhen Anforderung im Admin Center oder in der Exchange-Verwaltungs-PowerShell mithilfe der ID der Anforderung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1570c-190">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-191">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-191">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="1570c-192">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://admin.microsoft.com) an.</span><span class="sxs-lookup"><span data-stu-id="1570c-192">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="1570c-193">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-193">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-194">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="1570c-195">Wählen Sie **Ansicht** aus, um übermittelte Anforderungen nach dem Status Ausstehend, **genehmigt**, **verweigert**oder **Kunden** zu filtern. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1570c-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-196">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-196">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-197">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Status einer Genehmigungsanforderung für eine bestimmte Anforderungs-ID anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="1570c-197">Run the following command in Exchange Online PowerShell to view an approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="1570c-198">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="1570c-199">Genehmigen einer Elevation-Autorisierungsanforderung</span><span class="sxs-lookup"><span data-stu-id="1570c-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="1570c-200">Bei der Erstellung einer Genehmigungsanforderung erhalten Mitglieder der entsprechenden genehmigenden Gruppe eine e-Mail-Benachrichtigung und können die Anforderung genehmigen, die der Anforderungs-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1570c-200">When an approval request is created, members of the relevant approver group receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="1570c-201">Der Anforderer wird über eine e-Mail-Nachricht über die Genehmigung oder Ablehnung der Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="1570c-201">The requestor is notified of the request approval or denial via email message.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-202">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-202">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="1570c-203">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://admin.microsoft.com) an.</span><span class="sxs-lookup"><span data-stu-id="1570c-203">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="1570c-204">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-204">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-205">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="1570c-206">Wählen Sie eine aufgeführte Anforderung aus, um die Details anzuzeigen und Aktionen für die Anforderung durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="1570c-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="1570c-207">Wählen \*\*\*\* Sie genehmigen aus, um die Anforderung zu genehmigen, oder wählen Sie **verweigern** , um die Anforderung zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="1570c-207">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="1570c-208">Zuvor genehmigten Anforderungen kann der Zugriff widerrufen werden, indem Sie **REVOKE**auswählen.</span><span class="sxs-lookup"><span data-stu-id="1570c-208">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-209">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-209">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-210">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Erhöhungs Autorisierungsanforderung zu genehmigen:</span><span class="sxs-lookup"><span data-stu-id="1570c-210">To approve an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="1570c-211">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="1570c-212">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Ansichts Autorisierungsanforderung zu verweigern:</span><span class="sxs-lookup"><span data-stu-id="1570c-212">To deny an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="1570c-213">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1570c-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="1570c-214">Löschen einer Richtlinie für privilegierten Zugriff in Office 365</span><span class="sxs-lookup"><span data-stu-id="1570c-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="1570c-215">Wenn Sie in Ihrer Organisation nicht mehr benötigt werden, können Sie eine privilegierte Zugriffsrichtlinie löschen.</span><span class="sxs-lookup"><span data-stu-id="1570c-215">If it is no longer needed in your organization, you can delete a privileged access policy.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-216">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-216">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="1570c-217">Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1570c-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="1570c-218">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-218">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-219">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="1570c-220">Wählen Sie **Richtlinien konfigurieren**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="1570c-221">Wählen Sie die Richtlinie aus, die Sie löschen möchten, und wählen Sie dann **Richtlinie entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="1570c-222">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="1570c-222">Select **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-223">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-223">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-224">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine privilegierte Zugriffsrichtlinie zu löschen:</span><span class="sxs-lookup"><span data-stu-id="1570c-224">To delete a privileged access policy, run the following command in Exchange Online Powershell:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="1570c-225">Deaktivieren des privilegierten Zugriffs in Office 365</span><span class="sxs-lookup"><span data-stu-id="1570c-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="1570c-226">Bei Bedarf können Sie die privilegierte Zugriffsverwaltung für Ihre Organisation deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1570c-226">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="1570c-227">Durch das Deaktivieren des privilegierten Zugriffs werden keine zugehörigen Genehmigungsrichtlinien oder genehmigenden Gruppen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1570c-227">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="1570c-228">Im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="1570c-228">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="1570c-229">Melden Sie sich beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mit Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1570c-229">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="1570c-230">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="1570c-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="1570c-231">Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .</span><span class="sxs-lookup"><span data-stu-id="1570c-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="1570c-232">In der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="1570c-232">In Exchange Management PowerShell</span></span>

<span data-ttu-id="1570c-233">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="1570c-233">To disable privileged access, run the following command in Exchange Online Powershell:</span></span>

```
Disable-ElevatedAccessControl
```
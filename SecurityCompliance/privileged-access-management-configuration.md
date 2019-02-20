---
title: Konfigurieren von privileged Access Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: In diesem Thema erfahren Sie mehr über das Konfigurieren von privileged Access Management in Office 365
ms.openlocfilehash: 63780da59afb245b35916a1e7a5b2eb780d535a8
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090917"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="deced-103">Konfigurieren von privileged Access Management in Office 365</span><span class="sxs-lookup"><span data-stu-id="deced-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="deced-104">Dieses Thema enthält Informationen zur Bereitstellung und Konfiguration von Features, die derzeit nur in Office 365 E5 und Advanced Compliance-SKUs verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="deced-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="deced-p101">In diesem Thema erfahren Sie, wie Sie die privilegierte Zugriffsverwaltung in Ihrer Office 365-Organisation aktivieren und konfigurieren. Sie können entweder das Microsoft 365 Admin Center oder die Exchange-Verwaltungs-PowerShell verwenden, um den privilegierten Zugriff zu verwalten und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="deced-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="deced-107">Aktivieren und Konfigurieren der Verwaltung privilegierter Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="deced-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="deced-108">Führen Sie die folgenden Schritte aus, um den privilegierten Zugriff in Ihrer Office 365-Organisation einzurichten und zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="deced-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="deced-109">Schritt 1: Erstellen der Gruppe einer genehmigenden Person</span><span class="sxs-lookup"><span data-stu-id="deced-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="deced-p102">Bevor Sie mit dem Verwenden von Berechtigungszugriff beginnen, bestimmen Sie, wer über Genehmigungsautorität für eingehende Anforderungen für den Zugriff auf erhöhte und privilegierte Aufgaben verfügt. Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist, kann Zugriffsanforderungen genehmigen. Dies wird durch das Erstellen einer e-Mail-aktivierten Sicherheitsgruppe in Office 365 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="deced-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="deced-113">Schritt 2: Aktivieren des privilegierten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="deced-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="deced-114">Privilegierter Zugriff muss explizit in Office 365 mit der standardmäßigen genehmigenden Gruppe aktiviert werden und eine Reihe von Systemkonten enthalten, die Sie aus der Zugriffssteuerung für die privilegierte Zugriffsverwaltung ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="deced-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="deced-115">Schritt 3: Erstellen einer Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="deced-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="deced-p103">Durch das Erstellen einer Genehmigungsrichtlinie können Sie die spezifischen Genehmigungsanforderungen für einzelne Aufgaben definieren. Die Optionen für den Genehmigungs sind **automatisch** oder **manuell**.</span><span class="sxs-lookup"><span data-stu-id="deced-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="deced-118">Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen</span><span class="sxs-lookup"><span data-stu-id="deced-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="deced-p104">Nach der Aktivierung erfordert der privilegierte Zugriff Genehmigungen für die Ausführung von Aufgaben, für die eine zugehörige Genehmigungsrichtlinie definiert ist. Benutzer, die Aufgaben ausführen müssen, die in der Genehmigungsrichtlinie enthalten sind, müssen die Zugriffsgenehmigung anfordern und erhalten, um die zum Ausführen der Aufgabe erforderlichen Berechtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="deced-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="deced-p105">Nachdem die Genehmigung erteilt wurde, kann der anfordernde Benutzer die vorgesehene Aufgabe ausführen, und der privilegierte Zugriff autorisiert und führt die Aufgabe im Namen der Benutzer aus. Die Genehmigung bleibt für die angeforderte Dauer (Standarddauer 4 Stunden) gültig, während der der anfordernde die vorgesehene Aufgabe mehrmals ausführen kann. Alle derartigen Ausführungen werden protokolliert und für die Sicherheits-und Konformitätsüberwachung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="deced-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="deced-p106">Wenn Sie die Exchange-Verwaltungsshell zum Aktivieren und Konfigurieren des privilegierten Zugriffs verwenden möchten, führen Sie die Schritte unter [Herstellen einer Verbindung mit Exchange Online PowerShell mithilfe der mehr](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) stufigen Authentifizierung zum Herstellen einer Verbindung mit Exchange Online PowerShell mit ihrem Office 365 aus. Anmeldeinformationen. Sie müssen die mehrstufige Authentifizierung für Ihre Office 365-Organisation nicht aktivieren, um die Schritte zum Aktivieren des privilegierten Zugriffs beim Herstellen einer Verbindung mit Exchange Online PowerShell zu verwenden. Beim Herstellen einer Verbindung mit mehrstufiger Authentifizierung wird ein OAuth-Token erstellt, das von privilegiertem Zugriff zum Signieren von Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="deced-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="deced-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="deced-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="deced-128">Schritt 1: Erstellen einer Gruppe von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="deced-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="deced-129">Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="deced-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="deced-130">Wechseln Sie im Admin Center zu **Gruppen** > **Hinzufügen einer Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="deced-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="deced-131">Wählen Sie den Gruppentyp **e-Mail-aktivierte Sicherheitsgruppe** aus, und füllen Sie dann die Felder **Name**, **Gruppen-e-Mail-Adresse**und **Beschreibung** für die neue Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="deced-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="deced-p107">Speichern Sie die Gruppe. Es kann einige Minuten dauern, bis die Gruppe vollständig konfiguriert ist und im Office 365 Admin Center angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="deced-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="deced-134">Wählen Sie die Gruppe neuer genehmigender aus, und wählen Sie **Bearbeiten** aus, um Benutzer zur Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="deced-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="deced-135">Speichern Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="deced-135">Save the group.</span></span>

<span data-ttu-id="deced-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="deced-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="deced-137">Schritt 2: Aktivieren des privilegierten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="deced-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-138">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-139">Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="deced-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="deced-140">Navigieren Sie im Admin Center zu **Einstellungen > Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-141">Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .</span><span class="sxs-lookup"><span data-stu-id="deced-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="deced-142">Weisen Sie die Gruppe der genehmigenden Personen, die Sie in Schritt 1 erstellt haben, als **Standardgruppe für genehmigende**Personen zu.</span><span class="sxs-lookup"><span data-stu-id="deced-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="deced-143">**Speichern** und **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="deced-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-144">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-145">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu aktivieren und die Gruppe der genehmigenden Personen zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="deced-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="deced-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="deced-147">Das Feature "System Konten" wird bereitgestellt, um sicherzustellen, dass bestimmte Automatisierungen in Ihrer Organisation ohne Abhängigkeit vom privilegierten Zugriff funktionieren können, es wird jedoch empfohlen, dass diese Ausnahmen außergewöhnlich sind und diese zulässig sind. regelmäßig.</span><span class="sxs-lookup"><span data-stu-id="deced-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="deced-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="deced-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="deced-149">Schritt 3: Erstellen einer Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="deced-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="deced-150">Sie können bis zu 30 privilegierte Zugriffsrichtlinien für Ihre Office 365-Organisation erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="deced-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-151">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-152">Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="deced-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="deced-153">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-154">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="deced-155">Wählen Sie **Richtlinien konfigurieren** aus, und wählen Sie **Richtlinie hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="deced-156">Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="deced-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="deced-157">**Richtlinientyp**: Aufgabe, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="deced-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="deced-158">**Richtlinienbereich**: Exchange oder Office 365</span><span class="sxs-lookup"><span data-stu-id="deced-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="deced-159">**Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien aus</span><span class="sxs-lookup"><span data-stu-id="deced-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="deced-160">\*\*\*\* Genehmigungs: manuell oder automatisch</span><span class="sxs-lookup"><span data-stu-id="deced-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="deced-161">**Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte genehmigende Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="deced-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="deced-p108">Klicken Sie auf **Erstellen** und dann auf **Schließen**. Es kann einige Minuten dauern, bis die Richtlinie vollständig konfiguriert und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="deced-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-164">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-165">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsrichtlinie zu erstellen und zu definieren:</span><span class="sxs-lookup"><span data-stu-id="deced-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="deced-166">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="deced-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="deced-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="deced-168">Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen</span><span class="sxs-lookup"><span data-stu-id="deced-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="deced-169">Anfordern einer Erhöhungs Autorisierung zum Ausführen privilegierter Aufgaben</span><span class="sxs-lookup"><span data-stu-id="deced-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="deced-p109">Anforderungen für den privilegierten Zugriff sind bis zu 24 Stunden nach der Übermittlung der Anforderung gültig. Wenn diese nicht genehmigt oder verweigert werden, werden die Anforderungen ablaufen, und der Zugriff wird nicht genehmigt.</span><span class="sxs-lookup"><span data-stu-id="deced-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-172">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-173">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.</span><span class="sxs-lookup"><span data-stu-id="deced-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="deced-174">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-175">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="deced-p110">Wählen Sie **neue Anforderung**aus. Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="deced-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="deced-178">**Anforderungstyp**: Aufgabe, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="deced-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="deced-179">**Anforderungsbereich**: Exchange</span><span class="sxs-lookup"><span data-stu-id="deced-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="deced-180">**Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="deced-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="deced-p111">**Dauer (Stunden)**: Anzahl der Stunden des angeforderten Zugriffs. Es gibt keine Begrenzung für die Anzahl der Stunden, die angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="deced-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="deced-183">**Kommentare**: Textfeld für Kommentare in Bezug auf ihre Zugriffsanforderung</span><span class="sxs-lookup"><span data-stu-id="deced-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="deced-p112">Klicken Sie auf **Speichern** und dann auf **Schließen**. Ihre Anfrage wird per e-Mail an die Gruppe der genehmigenden Person gesendet.</span><span class="sxs-lookup"><span data-stu-id="deced-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-186">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-187">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsanforderung an die Gruppe der genehmigenden Personen zu erstellen und zu übermitteln:</span><span class="sxs-lookup"><span data-stu-id="deced-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="deced-188">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="deced-189">Anzeigen des Status von Ansichts Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deced-189">View status of elevation requests</span></span>
<span data-ttu-id="deced-190">Nachdem eine Genehmigungsanforderung erstellt wurde, kann der Status der Höhen Anforderung im Admin Center oder in der Exchange-Verwaltungs-PowerShell mithilfe der ID der Anforderung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="deced-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-191">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-192">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.</span><span class="sxs-lookup"><span data-stu-id="deced-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="deced-193">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-194">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="deced-195">Wählen Sie **Ansicht** aus, um übermittelte Anforderungen nach dem Status Ausstehend, **genehmigt**, **verweigert**oder **Kunden** zu filtern. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="deced-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-196">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-197">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Status einer Genehmigungsanforderung für eine bestimmte Anforderungs-ID anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="deced-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="deced-198">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="deced-199">Genehmigen einer Elevation-Autorisierungsanforderung</span><span class="sxs-lookup"><span data-stu-id="deced-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="deced-p113">Wenn eine Genehmigungsanforderung erstellt wird, erhalten Mitglieder der entsprechenden genehmigenden Gruppe eine e-Mail-Benachrichtigung und können die Anforderung genehmigen, die der Anforderungs-ID zugeordnet ist. Der Anforderer wird über eine e-Mail-Nachricht über die Genehmigung oder Ablehnung der Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="deced-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-202">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-203">Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.</span><span class="sxs-lookup"><span data-stu-id="deced-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="deced-204">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-205">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="deced-206">Wählen Sie eine aufgeführte Anforderung aus, um die Details anzuzeigen und Aktionen für die Anforderung durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="deced-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="deced-p114">Wählen \*\*\*\* Sie genehmigen aus, um die Anforderung zu genehmigen, oder wählen Sie **verweigern** , um die Anforderung zu verweigern. Zuvor genehmigten Anforderungen kann der Zugriff widerrufen werden, indem Sie **REVOKE**auswählen.</span><span class="sxs-lookup"><span data-stu-id="deced-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-209">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-210">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Elevation-Autorisierungsanforderung zu genehmigen:</span><span class="sxs-lookup"><span data-stu-id="deced-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="deced-211">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="deced-212">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Elevation-Autorisierungsanforderung zu verweigern:</span><span class="sxs-lookup"><span data-stu-id="deced-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="deced-213">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="deced-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="deced-214">Löschen einer Richtlinie für privilegierten Zugriff in Office 365</span><span class="sxs-lookup"><span data-stu-id="deced-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="deced-215">Sie können eine Richtlinie für den privilegierten Zugriff löschen, wenn Sie in Ihrer Organisation nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="deced-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-216">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-217">Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="deced-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="deced-218">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-219">Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="deced-220">Wählen Sie **Richtlinien konfigurieren**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="deced-221">Wählen Sie die Richtlinie aus, die Sie löschen möchten, und wählen Sie dann **Richtlinie entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="deced-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="deced-222">Klicken Sie auf **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="deced-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-223">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-224">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine privilegierte Zugriffsrichtlinie zu löschen:</span><span class="sxs-lookup"><span data-stu-id="deced-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="deced-225">Deaktivieren des privilegierten Zugriffs in Office 365</span><span class="sxs-lookup"><span data-stu-id="deced-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="deced-p115">Bei Bedarf können Sie die privilegierte Zugriffsverwaltung für Ihre Organisation deaktivieren. Durch das Deaktivieren des privilegierten Zugriffs werden keine zugehörigen Genehmigungsrichtlinien oder genehmigenden Gruppen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="deced-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="deced-228">Verwenden des Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="deced-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="deced-229">Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="deced-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="deced-230">Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="deced-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="deced-231">Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .</span><span class="sxs-lookup"><span data-stu-id="deced-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="deced-232">Verwenden der Exchange-Verwaltungs-PowerShell</span><span class="sxs-lookup"><span data-stu-id="deced-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="deced-233">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="deced-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```
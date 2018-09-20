---
title: Konfigurieren von Systemzugriff Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Verwenden Sie in diesem Thema, um weitere Informationen zum Konfigurieren der Systemzugriff Management in Office 365
ms.openlocfilehash: b2b6ab18687617c0da3425f4ee60cf81074f6f69
ms.sourcegitcommit: 15dfa0c83aa88816c18e30a44a49e36e733d952c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2018
ms.locfileid: "24021401"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="582b3-103">Konfigurieren von Systemzugriff Management in Office 365</span><span class="sxs-lookup"><span data-stu-id="582b3-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="582b3-104">In diesem Thema werden die Hinweise zur Bereitstellung und Konfiguration für derzeit nur in Office 365 E5 und erweiterte Compliance-SKUs verfügbaren Features behandelt.</span><span class="sxs-lookup"><span data-stu-id="582b3-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="582b3-p101">In diesem Thema führt Sie durch Aktivieren und Konfigurieren von Systemzugriff Management in Office 365-Organisation. Sie können entweder die mit Berechtigungen Zugriff, die Microsoft 365 Admin Center oder Exchange Management PowerShell zum Verwalten und verwenden.</span><span class="sxs-lookup"><span data-stu-id="582b3-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="582b3-107">Aktivieren und Konfigurieren der Verwaltung von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="582b3-108">Führen Sie diese Schritte zum Einrichten und Verwenden von Systemzugriff in Office 365-Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="582b3-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="582b3-109">Schritt 1: Erstellen einer genehmigenden Person Gruppe</span><span class="sxs-lookup"><span data-stu-id="582b3-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="582b3-p102">Bevor Sie mit Berechtigung Access beginnen, bestimmen Sie die Genehmigungsberechtigung für eingehende Anforderungen für den Zugriff auf Aufgaben mit erhöhten Rechten und Berechtigungen besitzen. Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist werden Genehmigen von zugriffsanforderungen. Dies ist aktiviert, indem Sie eine e-Mail-aktivierte Sicherheitsgruppe in Office 365 erstellen.</span><span class="sxs-lookup"><span data-stu-id="582b3-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="582b3-113">Schritt 2: Aktivieren von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="582b3-114">Systemzugriff muss explizit aktiviert werden in Office 365 mit der Standardgruppe genehmigende Person und einschließlich einer Reihe von Systemkonten, die Sie aus der Systemzugriff Management Zugriffssteuerung ausgeschlossen werden möchten.</span><span class="sxs-lookup"><span data-stu-id="582b3-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="582b3-115">Schritt 3: Erstellen einer Richtlinie für den Zugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="582b3-p103">Erstellen einer Richtlinie für die Genehmigung können Sie die Genehmigung von bestimmten Anforderungen an einzelne Aufgaben bezogenen definieren. Die Typ von Genehmigungsoptionen werden **automatisch** oder **manuell**.</span><span class="sxs-lookup"><span data-stu-id="582b3-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="582b3-118">Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /</span><span class="sxs-lookup"><span data-stu-id="582b3-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="582b3-p104">Aktiviert, privilegierten Zugriff erfordert Genehmigungen für das Ausführen aller Aufgaben, die eine Genehmigung zugeordnete Richtlinie definiert wurde. Benutzer müssen zum Ausführen von Aufgaben, die eine Genehmigung Richtlinie müssen anfordern und zugriffsgenehmigung, um die erforderlichen Berechtigungen zum Ausführen der Aufgabe lassen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="582b3-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="582b3-p105">Nachdem die Zustimmung eingeholt wurde, der anfordernde Benutzer kann den beabsichtigten Vorgang ausführen und Systemzugriff autorisieren und Ausführen die Aufgabe im Auftrag eines Benutzers wird. Die Genehmigung bleibt gültig für den angeforderten Dauer (Dauer der Standardwert lautet 4 Stunden), in dem die anfordernde Person die vorgesehene Aufgabe mehrmals führen kann. Alle solchen Ausführungen sind angemeldet und für Sicherheit und Compliance Überwachung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="582b3-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="582b3-p106">Wenn Sie Exchange Management PowerShell zur Aktivierung und Konfiguration Systemzugriff verwenden möchten, führen Sie die Schritte in Verbindung mit Exchange Online PowerShell mit Ihrer Office 365 [Connect to Exchange Online PowerShell mithilfe von Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) Anmeldeinformationen. Sie müssen nicht die mehrstufige Authentifizierung für Office 365-Organisation mit den Schritten um Systemzugriff zu ermöglichen, während eine Verbindung mit Exchange Online PowerShell aktivieren. Herstellen einer Verbindung mit Multi-Factor Authentication erstellt ein OAuth-Token, das vom Systemzugriff für die Anmeldung Ihre Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="582b3-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="582b3-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="582b3-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="582b3-128">Schritt 1: Erstellen einer genehmigenden Person Gruppe</span><span class="sxs-lookup"><span data-stu-id="582b3-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="582b3-129">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="582b3-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="582b3-130">Wechseln Sie in der Verwaltungskonsole **Gruppen** > **Gruppe hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="582b3-131">Wählen Sie die **e-Mail-aktivierte Sicherheitsgruppe** Gruppentyp aus, und führen Sie dann die Felder **Name**, **Gruppe e-Mail-Adresse**und **Beschreibung** für die neue Gruppe.</span><span class="sxs-lookup"><span data-stu-id="582b3-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="582b3-p107">Speichern Sie die Gruppe. Es dauert ein paar Minuten für die Gruppe vollständig konfiguriert werden und in der Office 365-Verwaltungskonsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="582b3-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="582b3-134">Wählen Sie die neue genehmigende Person aus, und wählen Sie zum Hinzufügen von Benutzern der Gruppe **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="582b3-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="582b3-135">Speichern Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="582b3-135">Save the group.</span></span>

<span data-ttu-id="582b3-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="582b3-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="582b3-137">Schritt 2: Aktivieren von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-138">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-139">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="582b3-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="582b3-140">Wechseln Sie in der Verwaltungskonsole zur **Einstellungen > Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-141">Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .</span><span class="sxs-lookup"><span data-stu-id="582b3-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="582b3-142">Weisen Sie in Schritt 1 als den **Standard-Gruppe der genehmigenden Personen**erstellten Gruppe der genehmigenden Person.</span><span class="sxs-lookup"><span data-stu-id="582b3-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="582b3-143">**Speichern** und **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-144">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-145">Führen Sie den folgenden Befehl in Exchange Online PowerShell Systemzugriff aktivieren und der genehmigenden Person Gruppe zuweisen:</span><span class="sxs-lookup"><span data-stu-id="582b3-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="582b3-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="582b3-147">Systemkonten, dass das Feature um sicherzustellen, dass bestimmte der Automatisierung innerhalb Ihrer Organisation zur Verfügung gestellt wird ohne Abhängigkeit an Systemzugriff arbeiten können, aber es wird empfohlen, dass solche Ausschlüsse außergewöhnliche werden und die zulässigen genehmigt und überwacht werden sollte Führen Sie regelmäßige.</span><span class="sxs-lookup"><span data-stu-id="582b3-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="582b3-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="582b3-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="582b3-149">Schritt 3: Erstellen einer Richtlinie für den Zugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-149">Step 3 - Create an access policy</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-150">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-150">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-151">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="582b3-151">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="582b3-152">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-152">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-153">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-153">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="582b3-154">Wählen Sie **Richtlinien konfigurieren** , und wählen Sie **eine Richtlinie hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-154">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="582b3-155">Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:</span><span class="sxs-lookup"><span data-stu-id="582b3-155">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="582b3-156">**Richtlinientyp**: Vorgangs-, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="582b3-156">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="582b3-157">**Richtlinie auf Benutzerebene**: Exchange oder Office 365</span><span class="sxs-lookup"><span data-stu-id="582b3-157">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="582b3-158">**Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="582b3-158">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="582b3-159">**Typ der statusgenehmigung**: manuell oder automatisch</span><span class="sxs-lookup"><span data-stu-id="582b3-159">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="582b3-160">**Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte Gruppe der genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="582b3-160">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="582b3-p108">Wählen Sie **Erstellen** und dann auf **Schließen**. Es kann einige Minuten für die Richtlinie vollständig konfiguriert und aktiviert worden ist.</span><span class="sxs-lookup"><span data-stu-id="582b3-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-163">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-163">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-164">Führen Sie folgenden Befehl in Exchange Online PowerShell zum Erstellen und eine Genehmigung zu definieren:</span><span class="sxs-lookup"><span data-stu-id="582b3-164">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="582b3-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-165">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="582b3-166"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="582b3-166"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="582b3-167">Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /</span><span class="sxs-lookup"><span data-stu-id="582b3-167">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="582b3-168">Elevation-Autorisierung auszuführende Aufgaben privilegierte anfordern</span><span class="sxs-lookup"><span data-stu-id="582b3-168">Requesting elevation authorization to execute privileged tasks</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-169">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-169">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-170">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="582b3-170">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="582b3-171">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-172">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="582b3-p109">Wählen Sie **neue Anforderung**. Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:</span><span class="sxs-lookup"><span data-stu-id="582b3-p109">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="582b3-175">**Anforderungstyp**: Vorgangs-, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="582b3-175">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="582b3-176">**Bereich anfordern**: Exchange</span><span class="sxs-lookup"><span data-stu-id="582b3-176">**Request scope**: Exchange</span></span>

    <span data-ttu-id="582b3-177">**Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="582b3-177">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="582b3-178">**Dauer (in Stunden)**: Anzahl von Stunden für den angeforderten Zugriff</span><span class="sxs-lookup"><span data-stu-id="582b3-178">**Duration (hours)**: Number of hours of requested access</span></span>

    <span data-ttu-id="582b3-179">**Kommentare**: Textfeld für Kommentare im Zusammenhang mit Ihrer Access-Anforderung</span><span class="sxs-lookup"><span data-stu-id="582b3-179">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="582b3-p110">Wählen Sie **Speichern** und dann auf **Schließen**. Ihre Anforderung wird der genehmigenden Person Gruppe per e-Mail gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="582b3-p110">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-182">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-182">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-183">Führen Sie den folgenden Befehl in Exchange Online PowerShell zum Erstellen und senden eine Aufforderung zur Genehmigung an die Gruppe der genehmigenden Person:</span><span class="sxs-lookup"><span data-stu-id="582b3-183">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="582b3-184">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-184">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="582b3-185">Anzeigen des Status der Elevation-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="582b3-185">View status of elevation requests</span></span>
<span data-ttu-id="582b3-186">Nach dem Erstellen einer genehmigungsanforderung Elevation Anforderungsstatus in der Verwaltungskonsole überprüft werden kann oder im Exchange Management PowerShell Anforderung mit der zugeordnete ID.</span><span class="sxs-lookup"><span data-stu-id="582b3-186">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-187">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-187">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-188">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="582b3-188">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="582b3-189">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-189">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-190">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-190">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="582b3-191">Wählen Sie **Ansicht** zum Filtern von weitergeleiteten Anfragen nach dem Status **ausstehender**, **genehmigt**, **verweigert**oder **Kunden Lockbox** .</span><span class="sxs-lookup"><span data-stu-id="582b3-191">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-192">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-192">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-193">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Anforderung Genehmigungsstatus für eine bestimmte Anforderung ID anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="582b3-193">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="582b3-194">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-194">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="582b3-195">Eine Erhöhung Autorisierung Anforderung genehmigen</span><span class="sxs-lookup"><span data-stu-id="582b3-195">Approving an elevation authorization request</span></span>
<span data-ttu-id="582b3-196">Wenn eine Aufforderung zur Genehmigung erstellt wird, Mitglied der Gruppe relevanten genehmigende Person erhält eine e-Mail-Benachrichtigung und genehmigen die Anforderung der Anforderung ID zugeordnet werden kann</span><span class="sxs-lookup"><span data-stu-id="582b3-196">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-197">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-197">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-198">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="582b3-198">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="582b3-199">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-199">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-200">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="582b3-200">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="582b3-201">Wählen Sie eine aufgelistete Anforderung, um die Details anzuzeigen und auszuführende Aktion auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="582b3-201">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="582b3-p111">Wählen Sie **Genehmigen** genehmigen die Anforderung, oder wählen Sie **Verweigern** , um die Anforderung zu verweigern. Zuvor können genehmigte Anforderungen durch Auswählen von **Sperren**widerrufen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="582b3-p111">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-204">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-204">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-205">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung genehmigen:</span><span class="sxs-lookup"><span data-stu-id="582b3-205">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="582b3-206">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-206">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="582b3-207">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung zu verweigern:</span><span class="sxs-lookup"><span data-stu-id="582b3-207">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="582b3-208">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="582b3-208">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="582b3-209">Deaktivieren Sie Systemzugriff in Office 365</span><span class="sxs-lookup"><span data-stu-id="582b3-209">Disable privileged access in Office 365</span></span>

<span data-ttu-id="582b3-p112">Falls erforderlich, können Sie für Ihre Organisation Systemzugriff Management deaktivieren. Deaktivieren von Berechtigungen wird Access keine zugehörigen Genehmigung Richtlinien oder eine genehmigende Person Gruppen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="582b3-p112">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="582b3-212">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="582b3-212">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="582b3-213">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="582b3-213">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="582b3-214">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="582b3-214">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="582b3-215">Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .</span><span class="sxs-lookup"><span data-stu-id="582b3-215">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="582b3-216">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="582b3-216">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="582b3-217">Führen Sie den folgenden Befehl in Exchange Online Powershell, um Systemzugriff zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="582b3-217">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```
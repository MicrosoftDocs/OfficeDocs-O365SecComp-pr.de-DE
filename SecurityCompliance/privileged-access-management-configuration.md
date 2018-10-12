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
ms.openlocfilehash: 13d278c8e8555aa069035c2f03b23db69a475b43
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522256"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="d8f7a-103">Konfigurieren von Systemzugriff Management in Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f7a-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8f7a-104">In diesem Thema werden die Hinweise zur Bereitstellung und Konfiguration für derzeit nur in Office 365 E5 und erweiterte Compliance-SKUs verfügbaren Features behandelt.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="d8f7a-p101">In diesem Thema führt Sie durch Aktivieren und Konfigurieren von Systemzugriff Management in Office 365-Organisation. Sie können Microsoft 365 Admin Center oder Exchange Management PowerShell verwenden, verwalten und Systemzugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="d8f7a-107">Aktivieren und Konfigurieren der Verwaltung von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="d8f7a-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="d8f7a-108">Führen Sie diese Schritte zum Einrichten und Verwenden von Systemzugriff in Office 365-Organisation aus:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="d8f7a-109">Schritt 1: Erstellen einer genehmigenden Person Gruppe</span><span class="sxs-lookup"><span data-stu-id="d8f7a-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="d8f7a-p102">Bevor Sie mit Berechtigung Access beginnen, bestimmen Sie die Genehmigungsberechtigung für eingehende Anforderungen für den Zugriff auf Aufgaben mit erhöhten Rechten und Berechtigungen besitzen. Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist werden Genehmigen von zugriffsanforderungen. Dies ist aktiviert, indem Sie eine e-Mail-aktivierte Sicherheitsgruppe in Office 365 erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="d8f7a-113">Schritt 2: Aktivieren von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="d8f7a-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="d8f7a-114">Systemzugriff muss explizit aktiviert werden in Office 365 mit der Standardgruppe genehmigende Person und einschließlich einer Reihe von Systemkonten, die Sie aus der Systemzugriff Management Zugriffssteuerung ausgeschlossen werden möchten.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="d8f7a-115">Schritt 3: Erstellen einer Richtlinie für den Zugriff</span><span class="sxs-lookup"><span data-stu-id="d8f7a-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="d8f7a-p103">Erstellen einer Richtlinie für die Genehmigung können Sie die Genehmigung von bestimmten Anforderungen an einzelne Aufgaben bezogenen definieren. Die Typ von Genehmigungsoptionen werden **automatisch** oder **manuell**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="d8f7a-118">Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /</span><span class="sxs-lookup"><span data-stu-id="d8f7a-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="d8f7a-p104">Aktiviert, privilegierten Zugriff erfordert Genehmigungen für das Ausführen aller Aufgaben, die eine Genehmigung zugeordnete Richtlinie definiert wurde. Benutzer müssen zum Ausführen von Aufgaben, die eine Genehmigung Richtlinie müssen anfordern und zugriffsgenehmigung, um die erforderlichen Berechtigungen zum Ausführen der Aufgabe lassen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="d8f7a-p105">Nachdem die Zustimmung eingeholt wurde, der anfordernde Benutzer kann den beabsichtigten Vorgang ausführen und Systemzugriff autorisieren und Ausführen die Aufgabe im Auftrag eines Benutzers wird. Die Genehmigung bleibt gültig für den angeforderten Dauer (Dauer der Standardwert lautet 4 Stunden), in dem die anfordernde Person die vorgesehene Aufgabe mehrmals führen kann. Alle solchen Ausführungen sind angemeldet und für Sicherheit und Compliance Überwachung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="d8f7a-p106">Wenn Sie Exchange Management PowerShell zur Aktivierung und Konfiguration Systemzugriff verwenden möchten, führen Sie die Schritte in Verbindung mit Exchange Online PowerShell mit Ihrer Office 365 [Connect to Exchange Online PowerShell mithilfe von Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) Anmeldeinformationen. Sie müssen nicht die mehrstufige Authentifizierung für Office 365-Organisation mit den Schritten um Systemzugriff zu ermöglichen, während eine Verbindung mit Exchange Online PowerShell aktivieren. Herstellen einer Verbindung mit Multi-Factor Authentication erstellt ein OAuth-Token, das vom Systemzugriff für die Anmeldung Ihre Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="d8f7a-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="d8f7a-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="d8f7a-128">Schritt 1: Erstellen einer genehmigenden Person Gruppe</span><span class="sxs-lookup"><span data-stu-id="d8f7a-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="d8f7a-129">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="d8f7a-130">Wechseln Sie in der Verwaltungskonsole **Gruppen** > **Gruppe hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="d8f7a-131">Wählen Sie die **e-Mail-aktivierte Sicherheitsgruppe** Gruppentyp aus, und führen Sie dann die Felder **Name**, **Gruppe e-Mail-Adresse**und **Beschreibung** für die neue Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="d8f7a-p107">Speichern Sie die Gruppe. Es dauert ein paar Minuten für die Gruppe vollständig konfiguriert werden und in der Office 365-Verwaltungskonsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="d8f7a-134">Wählen Sie die neue genehmigende Person aus, und wählen Sie zum Hinzufügen von Benutzern der Gruppe **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="d8f7a-135">Speichern Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-135">Save the group.</span></span>

<span data-ttu-id="d8f7a-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="d8f7a-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="d8f7a-137">Schritt 2: Aktivieren von Systemzugriff</span><span class="sxs-lookup"><span data-stu-id="d8f7a-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-138">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-139">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="d8f7a-140">Wechseln Sie in der Verwaltungskonsole zur **Einstellungen > Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-141">Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="d8f7a-142">Weisen Sie in Schritt 1 als den **Standard-Gruppe der genehmigenden Personen**erstellten Gruppe der genehmigenden Person.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="d8f7a-143">**Speichern** und **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-144">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-145">Führen Sie den folgenden Befehl in Exchange Online PowerShell Systemzugriff aktivieren und der genehmigenden Person Gruppe zuweisen:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="d8f7a-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="d8f7a-147">Systemkonten, dass das Feature um sicherzustellen, dass bestimmte der Automatisierung innerhalb Ihrer Organisation zur Verfügung gestellt wird ohne Abhängigkeit an Systemzugriff arbeiten können, aber es wird empfohlen, dass solche Ausschlüsse außergewöhnliche werden und die zulässigen genehmigt und überwacht werden sollte Führen Sie regelmäßige.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="d8f7a-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="d8f7a-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="d8f7a-149">Schritt 3: Erstellen einer Richtlinie für den Zugriff</span><span class="sxs-lookup"><span data-stu-id="d8f7a-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="d8f7a-150">Sie können erstellen und Konfigurieren von bis zu 30 Systemzugriff Richtlinien für Office 365-Organisation.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-151">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-152">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="d8f7a-153">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-154">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="d8f7a-155">Wählen Sie **Richtlinien konfigurieren** , und wählen Sie **eine Richtlinie hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="d8f7a-156">Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="d8f7a-157">**Richtlinientyp**: Vorgangs-, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="d8f7a-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="d8f7a-158">**Richtlinie auf Benutzerebene**: Exchange oder Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f7a-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="d8f7a-159">**Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d8f7a-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="d8f7a-160">**Typ der statusgenehmigung**: manuell oder automatisch</span><span class="sxs-lookup"><span data-stu-id="d8f7a-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="d8f7a-161">**Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte Gruppe der genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="d8f7a-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="d8f7a-p108">Wählen Sie **Erstellen** und dann auf **Schließen**. Es kann einige Minuten für die Richtlinie vollständig konfiguriert und aktiviert worden ist.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-164">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-165">Führen Sie folgenden Befehl in Exchange Online PowerShell zum Erstellen und eine Genehmigung zu definieren:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="d8f7a-166">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="d8f7a-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="d8f7a-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="d8f7a-168">Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /</span><span class="sxs-lookup"><span data-stu-id="d8f7a-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="d8f7a-169">Elevation-Autorisierung auszuführende Aufgaben privilegierte anfordern</span><span class="sxs-lookup"><span data-stu-id="d8f7a-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="d8f7a-p109">Anforderungen für Systemzugriff gelten für bis zu 24 Stunden, nachdem die Anforderung gesendet wird. Wenn nicht genehmigt oder abgelehnt, die Anfragen ablaufen und Zugriff ist nicht genehmigt.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-172">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-173">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="d8f7a-174">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-175">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="d8f7a-p110">Wählen Sie **neue Anforderung**. Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="d8f7a-178">**Anforderungstyp**: Vorgangs-, Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="d8f7a-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="d8f7a-179">**Bereich anfordern**: Exchange</span><span class="sxs-lookup"><span data-stu-id="d8f7a-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="d8f7a-180">**Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d8f7a-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="d8f7a-p111">**Dauer (in Stunden)**: Anzahl von Stunden für den angeforderten Zugriff. Es ist kein Grenzwert für die Anzahl der Stunden, die angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="d8f7a-183">**Kommentare**: Textfeld für Kommentare im Zusammenhang mit Ihrer Access-Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="d8f7a-p112">Wählen Sie **Speichern** und dann auf **Schließen**. Ihre Anforderung wird der genehmigenden Person Gruppe per e-Mail gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-186">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-187">Führen Sie den folgenden Befehl in Exchange Online PowerShell zum Erstellen und senden eine Aufforderung zur Genehmigung an die Gruppe der genehmigenden Person:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="d8f7a-188">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="d8f7a-189">Anzeigen des Status der Elevation-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8f7a-189">View status of elevation requests</span></span>
<span data-ttu-id="d8f7a-190">Nach dem Erstellen einer genehmigungsanforderung Elevation Anforderungsstatus in der Verwaltungskonsole überprüft werden kann oder im Exchange Management PowerShell Anforderung mit der zugeordnete ID.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-191">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-192">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="d8f7a-193">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-194">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="d8f7a-195">Wählen Sie **Ansicht** zum Filtern von weitergeleiteten Anfragen nach dem Status **ausstehender**, **genehmigt**, **verweigert**oder **Kunden Lockbox** .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-196">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-197">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Anforderung Genehmigungsstatus für eine bestimmte Anforderung ID anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="d8f7a-198">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="d8f7a-199">Eine Erhöhung Autorisierung Anforderung genehmigen</span><span class="sxs-lookup"><span data-stu-id="d8f7a-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="d8f7a-p113">Wenn eine Aufforderung zur Genehmigung erstellt wird, Mitglied der Gruppe relevanten genehmigende Person erhält eine e-Mail-Benachrichtigung und genehmigen die Anforderung der Anforderung ID zugeordnet werden kann Der Requestor wird die Anforderung zur Genehmigung oder Ablehnung per e-Mail-Nachricht benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-202">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-203">Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="d8f7a-204">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-205">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="d8f7a-206">Wählen Sie eine aufgelistete Anforderung, um die Details anzuzeigen und auszuführende Aktion auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="d8f7a-p114">Wählen Sie **Genehmigen** genehmigen die Anforderung, oder wählen Sie **Verweigern** , um die Anforderung zu verweigern. Zuvor können genehmigte Anforderungen durch Auswählen von **Sperren**widerrufen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-209">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-210">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung genehmigen:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="d8f7a-211">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="d8f7a-212">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung zu verweigern:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="d8f7a-213">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="d8f7a-214">Löschen einer Richtlinie Systemzugriff in Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f7a-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="d8f7a-215">Sie können eine Richtlinie Systemzugriff löschen, wenn es in Ihrer Organisation nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-216">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-217">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="d8f7a-218">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-219">Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="d8f7a-220">Wählen Sie **Richtlinien konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="d8f7a-221">Wählen Sie die Richtlinie, den, die Sie löschen möchten, und wählen Sie **Richtlinie zu entfernen**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="d8f7a-222">Wählen Sie **Schließen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-223">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-224">Führen Sie den folgenden Befehl in Exchange Online Powershell, um eine Richtlinie Systemzugriff zu löschen:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="d8f7a-225">Deaktivieren Sie Systemzugriff in Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f7a-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="d8f7a-p115">Falls erforderlich, können Sie für Ihre Organisation Systemzugriff Management deaktivieren. Deaktivieren von Berechtigungen wird Access keine zugehörigen Genehmigung Richtlinien oder eine genehmigende Person Gruppen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="d8f7a-228">Verwenden das Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="d8f7a-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="d8f7a-229">Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="d8f7a-230">Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.</span><span class="sxs-lookup"><span data-stu-id="d8f7a-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="d8f7a-231">Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .</span><span class="sxs-lookup"><span data-stu-id="d8f7a-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="d8f7a-232">Verwenden von PowerShell für Exchange-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d8f7a-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="d8f7a-233">Führen Sie den folgenden Befehl in Exchange Online Powershell, um Systemzugriff zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d8f7a-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```
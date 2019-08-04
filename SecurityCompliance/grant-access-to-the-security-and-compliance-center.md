---
title: 'Erteilen von Benutzern den Zugriff auf das Compliance Center für Office 365 Security #a0'
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: 'Benutzer müssen Berechtigungen im Office 365 Security #a0 Compliance Center zugewiesen werden, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können.'
ms.openlocfilehash: ea774648efcfe80461eae937f80856acaf1db224
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2019
ms.locfileid: "35792011"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a><span data-ttu-id="ba47e-103">Erteilen von Benutzern den Zugriff auf das Compliance Center für Office 365 Security #a0</span><span class="sxs-lookup"><span data-stu-id="ba47e-103">Give users access to the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="ba47e-104">Benutzer müssen Berechtigungen im Office 365 Security #a0 Compliance Center zugewiesen werden, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ba47e-104">Users need to be assigned permissions in the Office 365 Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="ba47e-105">Als Office 365 globaler Administrator oder Mitglied der Mitglied-Rollengruppe im Security #a0 Compliance Center können Sie diese Berechtigungen Benutzern erteilen.</span><span class="sxs-lookup"><span data-stu-id="ba47e-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="ba47e-106">Benutzer können nur die Sicherheits-oder Kompatibilitätsfeatures verwalten, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="ba47e-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="ba47e-107">Weitere Informationen zu den verschiedenen Berechtigungen, die Sie Benutzern im Security #a0 Compliance Center erteilen können, finden Sie unter [Berechtigungen im Office 365 Security #a1 Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="ba47e-107">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="ba47e-108">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="ba47e-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="ba47e-109">Sie müssen ein Office 365 globaler Administrator oder ein Mitglied der Rollengruppe Mitglied im Security #a0 Compliance Center sein, um die Schritte in diesem Artikel ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ba47e-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="ba47e-110">Rollengruppen für das Security #a0 Compliance Center haben möglicherweise ähnliche Namen wie die Rollengruppen in Exchange Online, sind aber nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="ba47e-110">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="ba47e-111">Rollengruppenmitgliedschaften werden nicht zwischen Exchange Online und dem Security #a0 Compliance Center freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ba47e-111">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="ba47e-112">Partner mit Delegierten Zugriffsberechtigungen (DAP) mit verwalten im Namen von (AOBO) Berechtigungen können nicht auf das Sicherheits #a0 Compliance Center zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba47e-112">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="ba47e-113">Verwenden des Admin Centers, um einem anderen Benutzer Zugriff auf das Security #a0 Compliance Center zu gewähren</span><span class="sxs-lookup"><span data-stu-id="ba47e-113">Use the admin center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="ba47e-114">[Melden Sie sich bei Office 365 an, und wechseln Sie zum Admin Center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="ba47e-114">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>

2. <span data-ttu-id="ba47e-115">Öffnen Sie im Microsoft 365 Admin Center **Admin** Center, und klicken Sie dann auf **Sicherheit #a0 Kompatibilität**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-115">In the Microsoft 365 admin center, open **Admin centers** and then click **Security & Compliance**.</span></span>

3. <span data-ttu-id="ba47e-116">Wechseln Sie im Security #a0 Compliance Center zu **Berechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-116">In the Security & Compliance Center, go to **Permissions**.</span></span>

4. <span data-ttu-id="ba47e-117">Wählen Sie in der Liste die Rollengruppe aus, der Sie den Benutzer hinzufügen möchten, \*\*\*\* ![und klicken Sie](media/O365-MDM-CreatePolicy-EditIcon.gif)auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ba47e-117">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

5. <span data-ttu-id="ba47e-118">Klicken Sie auf der Eigenschaftenseite der Rollengruppe unter **Mitglieder**auf Add-](media/ITPro-EAC-AddIcon.gif) Symbol **Hinzufügen**![, und wählen Sie den Namen des Benutzers (oder der Benutzer) aus, den Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba47e-118">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

6. <span data-ttu-id="ba47e-119">Wenn Sie alle Benutzer ausgewählt haben, die Sie der Rollengruppe hinzufügen möchten, klicken Sie auf **hinzu\> fügen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-119">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

7. <span data-ttu-id="ba47e-120">Klicken Sie auf **Speichern**, um die Änderungen an der Rollengruppe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba47e-120">Click **Save** to save the changes to the role group.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="ba47e-121">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="ba47e-121">How do you know this worked?</span></span>

1. <span data-ttu-id="ba47e-122">Wechseln Sie im Security #a0 Compliance Center zu **Berechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="ba47e-122">In the Security & Compliance Center, go to **Permissions**.</span></span>

2. <span data-ttu-id="ba47e-123">Wählen Sie in der Liste die Rollengruppe aus, um die Mitglieder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba47e-123">From the list, select the role group to view the members.</span></span>

3. <span data-ttu-id="ba47e-124">Auf der rechten Seite in den Rollengruppen Details können Sie die Mitglieder der Rollengruppe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba47e-124">On the right, in the role group details, you can view the members of the role group.</span></span>

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="ba47e-125">Verwenden von PowerShell, um einem anderen Benutzer Zugriff auf das Security #a0 Compliance Center zu gewähren</span><span class="sxs-lookup"><span data-stu-id="ba47e-125">Use PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="ba47e-126">Stellen [Sie eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell her](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="ba47e-126">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="ba47e-127">Verwenden Sie den Befehl **Add-RoleGroupMember** , um einen Benutzer zur Rolle "Organisationsverwaltung" hinzuzufügen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba47e-127">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span>

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   <span data-ttu-id="ba47e-128">**Parameter**:</span><span class="sxs-lookup"><span data-stu-id="ba47e-128">**Parameters**:</span></span>
  
   - <span data-ttu-id="ba47e-129">_Identity_ ist die Rollengruppe, der Sie ein Mitglied hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba47e-129">_Identity_ is the role group to add a member to.</span></span>

   - <span data-ttu-id="ba47e-130">_Mitglied_ ist das Postfach, die universelle Sicherheitsgruppe (Universal Security Group, USG) oder der Computer, der der Rollengruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba47e-130">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="ba47e-131">Sie können immer nur ein Element angeben.</span><span class="sxs-lookup"><span data-stu-id="ba47e-131">You can specify only one member at a time.</span></span>

<span data-ttu-id="ba47e-132">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="ba47e-132">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="ba47e-133">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="ba47e-133">How do you know this worked?</span></span>

<span data-ttu-id="ba47e-134">Verwenden Sie das Cmdlet **Get-RoleGroupMember** , um die Mitglieder in der Rollengruppe "Organisationsverwaltung" anzuzeigen, um zu überprüfen, ob Sie Benutzern Zugriff auf das Security #a0 Compliance Center gegeben haben, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba47e-134">To verify that you've given users access to the Security & Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span>
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

<span data-ttu-id="ba47e-135">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="ba47e-135">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>

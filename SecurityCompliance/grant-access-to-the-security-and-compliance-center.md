---
title: Erteilen von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
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
description: Benutzer müssen Berechtigungen im Office 365 Security &amp; Compliance Center erhalten, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können.
ms.openlocfilehash: aa0d1e9af6eb547bbb145d06cabfc431028ec4f0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154297"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="902b7-103">Erteilen von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="902b7-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="902b7-104">Benutzer müssen Berechtigungen im Office 365 Security &amp; Compliance Center erhalten, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können.</span><span class="sxs-lookup"><span data-stu-id="902b7-104">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="902b7-105">Als Office 365 globaler Administrator oder Mitglied der Mitglied-Rollengruppe im Security &amp; Compliance Center können Sie diese Berechtigungen Benutzern erteilen.</span><span class="sxs-lookup"><span data-stu-id="902b7-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="902b7-106">Benutzer können nur die Sicherheits-oder Kompatibilitätsfeatures verwalten, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="902b7-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="902b7-107">Weitere Informationen zu den verschiedenen Berechtigungen, die Sie Benutzern im Security &amp; Compliance Center erteilen können, finden Sie unter [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="902b7-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="902b7-108">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="902b7-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="902b7-109">Sie müssen ein Office 365 globaler Administrator oder ein Mitglied der Rollengruppe Mitglied im Security &amp; Compliance Center sein, um die Schritte in diesem Artikel ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="902b7-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="902b7-110">Rollengruppen für das Security &amp; Compliance Center haben möglicherweise ähnliche Namen wie die Rollengruppen in Exchange Online, sind aber nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="902b7-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="902b7-111">Rollengruppenmitgliedschaften werden nicht zwischen Exchange Online und dem Security &amp; Compliance Center freigegeben.</span><span class="sxs-lookup"><span data-stu-id="902b7-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="902b7-112">Verwenden des Office 365 admin Centers, um einem anderen Benutzer Zugriff auf &amp; das Security Compliance Center zu gewähren</span><span class="sxs-lookup"><span data-stu-id="902b7-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="902b7-113">[Melden Sie sich bei Office 365 an, und wechseln Sie zum Admin Center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="902b7-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
2. <span data-ttu-id="902b7-114">Öffnen Sie im Office 365 Admin Center **Admin** Center, und klicken Sie dann auf **Sicherheits &amp; Kompatibilität**.</span><span class="sxs-lookup"><span data-stu-id="902b7-114">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
    
3. <span data-ttu-id="902b7-115">Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="902b7-115">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="902b7-116">Wählen Sie in der Liste die Rollengruppe aus, der Sie den Benutzer hinzufügen möchten, \*\*\*\* ![und klicken Sie](media/O365_MDM_CreatePolicy_EditIcon.gif)auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="902b7-116">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="902b7-117">Klicken Sie auf der Eigenschaftenseite der Rollengruppe unter **Mitglieder**auf Add-](media/ITPro-EAC-AddIcon.gif) Symbol **Hinzufügen**![, und wählen Sie den Namen des Benutzers (oder der Benutzer) aus, den Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="902b7-117">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="902b7-118">Wenn Sie alle Benutzer ausgewählt haben, die Sie der Rollengruppe hinzufügen möchten, klicken Sie auf **hinzu\> fügen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="902b7-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="902b7-119">Klicken Sie auf **Speichern**, um die Änderungen an der Rollengruppe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="902b7-119">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="902b7-120">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="902b7-120">How do you know this worked?</span></span>

1. <span data-ttu-id="902b7-121">Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="902b7-121">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="902b7-122">Wählen Sie in der Liste die Rollengruppe aus, um die Mitglieder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="902b7-122">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="902b7-123">Auf der rechten Seite in den Rollengruppen Details können Sie die Mitglieder der Rollengruppe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="902b7-123">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="902b7-124">Verwenden von PowerShell, um einem anderen Benutzer Zugriff auf &amp; das Security Compliance Center zu gewähren</span><span class="sxs-lookup"><span data-stu-id="902b7-124">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="902b7-125">Stellen [Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="902b7-125">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="902b7-126">Verwenden Sie den Befehl **Add-RoleGroupMember** , um einen Benutzer zur Rolle "Organisationsverwaltung" hinzuzufügen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="902b7-126">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="902b7-127">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="902b7-127">**Parameters**</span></span>
  
- <span data-ttu-id="902b7-128">_-Identity_ ist die Rollengruppe, der Sie ein Mitglied hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="902b7-128">_-Identity_ is the role group to add a member to.</span></span> 
    
- <span data-ttu-id="902b7-129">_Mitglied_ ist das Postfach, die universelle Sicherheitsgruppe (Universal Security Group, USG) oder der Computer, der der Rollengruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="902b7-129">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="902b7-130">Sie können immer nur ein Element angeben.</span><span class="sxs-lookup"><span data-stu-id="902b7-130">You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="902b7-131">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="902b7-131">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="902b7-132">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="902b7-132">How do you know this worked?</span></span>

<span data-ttu-id="902b7-133">Um zu überprüfen, ob Sie Benutzern Zugriff auf das &amp; Security Compliance Center gegeben haben, verwenden Sie das Cmdlet **Get-RoleGroupMember** , um die Mitglieder in der Rollengruppe Organisationsverwaltung anzuzeigen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="902b7-133">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="902b7-134">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="902b7-134">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  


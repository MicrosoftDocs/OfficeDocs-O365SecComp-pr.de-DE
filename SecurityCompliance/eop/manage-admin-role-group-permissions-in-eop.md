---
title: Verwalten der Berechtigungen der Administratorrollen-Gruppenberechtigungen in EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: In Microsoft Exchange Online Protection (EOP) können Sie die Exchange-Verwaltungskonsole verwenden, um einen Benutzer als Mitglied zu einer oder mehreren Rollengruppen hinzuzufügen, sodass er die Berechtigungen für bestimmte Verwaltungsaufgaben erhält. Darüber hinaus können Sie einen Benutzer über die Exchange-Verwaltungskonsole aus Rollengruppen entfernen.
ms.openlocfilehash: b773b541b85288b4cb4deaa075cc0346d6bcc646
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002974"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="f71b6-104">Verwalten der Berechtigungen der Administratorrollen-Gruppenberechtigungen in EOP</span><span class="sxs-lookup"><span data-stu-id="f71b6-104">Manage admin role group permissions in EOP</span></span>
  
<span data-ttu-id="f71b6-p102">In Microsoft Exchange Online Protection (EOP) können Sie die Exchange-Verwaltungskonsole verwenden, um einen Benutzer als Mitglied zu einer oder mehreren Rollengruppen hinzuzufügen, sodass er die Berechtigungen für bestimmte Verwaltungsaufgaben erhält. Darüber hinaus können Sie einen Benutzer über die Exchange-Verwaltungskonsole aus Rollengruppen entfernen.</span><span class="sxs-lookup"><span data-stu-id="f71b6-p102">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f71b6-107">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="f71b6-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="f71b6-108">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5-10 Minuten</span><span class="sxs-lookup"><span data-stu-id="f71b6-108">Estimated time to complete: 5-10 minutes</span></span>
    
- <span data-ttu-id="f71b6-p103">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="f71b6-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="f71b6-p104">Bestimmte Berechtigungen in Office 365 entsprechen Berechtigungen der Administratorrollengruppen in EOP. Weitere Informationen finden Sie in der Spalte "Rolle in Exchange Online" im Abschnitt "Für welche Dienste gelten meine Office 365-Berechtigungen?" unter [Zuweisen von Adminrollen](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span><span class="sxs-lookup"><span data-stu-id="f71b6-p104">Certain permissions in Office 365 map to EOP admin role group permissions. For more information, see the "Role in Exchange Online" column in the "Which services do my Office 365 permissions extend to?" section in [Assigning Admin Roles](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span></span>
    
- <span data-ttu-id="f71b6-114">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.</span><span class="sxs-lookup"><span data-stu-id="f71b6-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="f71b6-p105">Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="f71b6-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="what-do-you-want-to-do"></a><span data-ttu-id="f71b6-118">Was möchten Sie machen?</span><span class="sxs-lookup"><span data-stu-id="f71b6-118">What do you want to do?</span></span>

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="f71b6-119">Zuweisen von Mitgliedern zu Administratorrollengruppen mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="f71b6-119">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="f71b6-120">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Berechtigungen** \> **Administratorrollen**, klicken Sie auf die Rollengruppe, dem Sie den Benutzer oder Benutzer hinzufügen möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](../media/ITPro-EAC-EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="f71b6-120">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to add the user or users to, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="f71b6-p106">Klicken Sie unter **Mitglieder** auf Hinzufügen ![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif). Das Fenster zur Auswahl von Mitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f71b6-p106">Under Members, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). The Select Members window will appear.</span></span>
    
3. <span data-ttu-id="f71b6-123">Suchen Sie nach den Benutzern, die hinzugefügt werden sollen, oder wählen Sie die Benutzer aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="f71b6-123">Search for the user or users that you wish to add, or select them from the list.</span></span>
    
4. <span data-ttu-id="f71b6-p107">Wenn Sie die Benutzer ausgewählt haben, die hinzugefügt werden sollen, klicken Sie auf **Hinzufügen** und anschließend auf **OK**. Das Fenster zur Auswahl von Mitgliedern wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="f71b6-p107">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>
    
5. <span data-ttu-id="f71b6-p108">Wie Sie sehen, wurde der Benutzer zum Fenster **Mitglieder** hinzugefügt. Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f71b6-p108">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f71b6-128">Nachdem Sie Mitglieder hinzugefügt oder aus der Rollengruppe entfernt haben, müssen sich die betroffenen Benutzer möglicherweise abmelden und dann erneut anmelden, um die Änderung ihrer Administratorrechten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="f71b6-128">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="f71b6-129">Entfernen von Mitgliedern aus Administratorrollengruppen mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="f71b6-129">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="f71b6-130">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Berechtigungen** \> **Administratorrollen**, klicken Sie auf die Rollengruppe, die Sie aus der Benutzer entfernen möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](../media/ITPro-EAC-EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="f71b6-130">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="f71b6-131">Wählen Sie unterhalb von **Mitglieder** die Benutzer aus, die entfernt werden sollen, und klicken Sie auf Entfernen ![Entfernen (Symbol)](../media/ITPro-EAC-RemoveIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="f71b6-131">Under Members, select the user or users that you want to remove and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="f71b6-p109">Klicken Sie auf **Speichern**, um die Änderung an der Rollengruppe zu speichern und zur Seite **Administratorrollen** zurückzukehren. Überprüfen Sie im Detailfenster für die ausgewählte Rollengruppe, ob das Mitglied nicht länger unter Mitglieder aufgeführt wird, um sicherzustellen, dass der Benutzer erfolgreich aus der Administratorrollengruppe entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f71b6-p109">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f71b6-134">Nachdem Sie Mitglieder hinzugefügt oder aus der Rollengruppe entfernt haben, müssen sich die betroffenen Benutzer möglicherweise abmelden und dann erneut anmelden, um die Änderung ihrer Administratorrechten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="f71b6-134">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="f71b6-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f71b6-135">For more information</span></span>

[<span data-ttu-id="f71b6-136">Featureberechtigungen in EOP</span><span class="sxs-lookup"><span data-stu-id="f71b6-136">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
  


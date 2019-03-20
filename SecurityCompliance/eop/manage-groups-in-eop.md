---
title: Verwalten von Gruppen in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Sie können Exchange Online Protection (EOP) zur Erstellung E-Mail-aktivierter Gruppen für eine Exchange-Organisation verwenden. Sie können EOP auch verwenden, um Gruppeneigenschaften zu definieren oder zu aktualisieren, über die Mitgliedschaften, E-Mail-Adressen und andere Aspekte von Gruppen festgelegt werden.
ms.openlocfilehash: db649e4fd955d13e50e96007e8e38fe2c1de5b4d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693301"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="2d83f-104">Verwalten von Gruppen in EOP</span><span class="sxs-lookup"><span data-stu-id="2d83f-104">Manage groups in EOP</span></span>

 <span data-ttu-id="2d83f-p102">Sie können Exchange Online Protection (EOP) zur Erstellung E-Mail-aktivierter Gruppen für eine Exchange-Organisation verwenden. Sie können EOP auch verwenden, um Gruppeneigenschaften zu definieren oder zu aktualisieren, über die Mitgliedschaften, E-Mail-Adressen und andere Aspekte von Gruppen festgelegt werden. Sie können je nach Bedarf Verteiler- oder Sicherheitsgruppen anlegen. Diese Gruppen können mithilfe des Exchange Admin Center (EAC) oder über Windows Remote-PowerShell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span> 
  
## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="2d83f-109">Arten von E-Mail-aktivierten Gruppen</span><span class="sxs-lookup"><span data-stu-id="2d83f-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="2d83f-110">Sie können für Ihre Exchange-Organisation zwei Arten von Gruppen erstellen:</span><span class="sxs-lookup"><span data-stu-id="2d83f-110">You can create two types of groups for your Exchange organization:</span></span>
  
- <span data-ttu-id="2d83f-p103">[Erstellen einer Gruppe im EAC](manage-groups-in-eop.md) (auch als Verteilergruppen bezeichnet) sind Sammlungen von E-Mail-Benutzern, z. B. Teams oder andere spontan gebildete Gruppen, die E-Mails zu einem gemeinsamen Thema senden oder empfangen müssen. Verteilergruppen sind exklusiv für die Verteilung von E-Mail-Nachrichten vorgesehen. In EOP wird mit dem Begriff "Verteilergruppe" jede E-Mail-aktivierte Gruppe bezeichnet, egal, ob sie sich in einem Sicherheitskontext befindet oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p103">[Create a group in the EAC](manage-groups-in-eop.md) (also known as distribution groups) are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest. Distribution groups are exclusively for distributing email messages. In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>
    
- <span data-ttu-id="2d83f-p104">[Bearbeiten oder Entfernen einer Gruppe im EAC](manage-groups-in-eop.md) (auch als Sicherheitsgruppen bezeichnet) sind Sammlungen von E-Mail-Benutzern, die Zugangsberechtigungen für Administratorrollen benötigen. Sie könnten z. B. bestimmten Gruppen von Benutzern Berechtigungen für Administratorrollen gewähren, sodass diese Benutzer dann Anti-Span- und Anti-Malware-Einstellungen konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p104">[Edit or remove a group in the EAC](manage-groups-in-eop.md) (also known as security groups) are collections of email users who need access permissions for Admin roles. For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2d83f-p105">Standardmäßig ist für alle neuen E-Mail-aktivierten Sicherheitsgruppen die Authentifizierung aller Absender erforderlich. Auf diese Weise wird verhindert, dass externe Absender Nachrichten an E-Mail-aktivierte Sicherheitsgruppen senden können.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="2d83f-118">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="2d83f-118">Before you begin</span></span>

- <span data-ttu-id="2d83f-p106">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter Eintrag "Verteilergruppen und Sicherheitsgruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2d83f-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="2d83f-121">Beachten Sie, dass beim Erstellen und Verwalten von Gruppen mithilfe von Remote-PowerShell-Cmdlets eine Drosselung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="2d83f-121">Be aware that when creating and managing groups by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="2d83f-122">Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="2d83f-122">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="2d83f-123">Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online Protection mithilfe der Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="2d83f-123">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
    
- <span data-ttu-id="2d83f-124">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="2d83f-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="2d83f-p107">Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="2d83f-p107">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="2d83f-128">Erstellen einer Gruppe im EAC</span><span class="sxs-lookup"><span data-stu-id="2d83f-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="2d83f-129">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="2d83f-129">In the Exchange admin center (EAC), go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="2d83f-p108">Klicken Sie auf **Neu**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif) und anschließend je nach Bedarf auf **Verteilergruppe** oder auf **Sicherheitsgruppe**. Zur Unterscheidung siehe [Arten von E-Mail-aktivierten Gruppen](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="2d83f-p108">Click **New**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **Distribution group** or **Security group**, depending on your needs. See [Types of mail-enabled groups](manage-groups-in-eop.md) for the distinction.</span></span> 
    
3. <span data-ttu-id="2d83f-132">Füllen Sie auf der Seite **Neue Verteilergruppe** oder **Neue Sicherheitsgruppe** die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="2d83f-132">On the **New distribution group** or **New security group** page, complete the following fields:</span></span> 
    
  - <span data-ttu-id="2d83f-p109">**Anzeigename** Geben Sie einen Anzeigenamen ein, der in Ihrer Organisation eindeutig ist und für die EOP-Benutzer einen Sinn ergibt. Der Anzeigename ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p109">**Display name** Type a display name that's unique to your organization and meaningful to EOP users. The display name is required.</span></span> 
    
  - <span data-ttu-id="2d83f-p110">**Alias** Geben Sie einen Gruppenalias mit einer Länge von bis zu 64 Zeichen ein, der in Ihrer Organisation eindeutig ist. Wenn ein EOP-Benutzer diesen Alias in die Zeile An: einer E-Mail eingibt, wird er in den Anzeigenamen der Gruppe aufgelöst. Wenn Sie den Alias ändern, wird die primäre SMTP-Adresse für die Gruppe ebenfalls geändert und enthält dann den neuen Alias. Der Alias ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p110">**Alias** Type a group alias of up to 64 characters that's unique to your organization. EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name. If you change the alias, the primary SMTP address for the group also changes and will contain the new alias. The alias is required.</span></span> 
    
  - <span data-ttu-id="2d83f-139">**Beschreibung** Geben Sie eine Beschreibung der Gruppe ein, sodass der Zweck der Gruppe erkennbar ist.</span><span class="sxs-lookup"><span data-stu-id="2d83f-139">**Description** Type a description of the group so that people will know the purpose of the group.</span></span> 
    
  - <span data-ttu-id="2d83f-p111">**Besitzer** Standardmäßig ist die Person, die eine Gruppe erstellt, der Besitzer. Sie können Besitzer hinzufügen, indem Sie auf **Hinzufügen**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif) klicken. Jede Gruppe muss mindestens einen Besitzer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p111">**Owners** By default, the person who creates the group is the owner. You can add an owner by choosing **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). All groups must have at least one owner.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2d83f-143">Besitzer von Gruppen müssen kein Mitglied der jeweiligen Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="2d83f-143">Owners don't have to be members of the group.</span></span> 
  
  - <span data-ttu-id="2d83f-p112">**Mitglieder** Verwenden Sie diesen Abschnitt zum Hinzufügen von Mitgliedern und um anzugeben, ob eine Genehmigung erforderlich ist, damit Personen der Gruppe beitreten bzw. diese verlassen können. Klicken Sie zum Hinzufügen von Mitgliedern zur Gruppe auf **Hinzufügen**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="2d83f-p112">**Members** Use this section to add group members and to specify whether approval is required for people to join or leave the group. To add members to the group, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="2d83f-146">Klicken Sie auf **OK**, um zur Ursprungsseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2d83f-146">Click **OK** to return to the original page.</span></span> 
    
5. <span data-ttu-id="2d83f-p113">Wenn Sie fertig sind, klicken Sie auf **Speichern**, um die Gruppe zu erstellen. Die neue Gruppe sollte in der Liste der Gruppen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p113">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span> 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="2d83f-149">Bearbeiten oder Entfernen einer Gruppe im EAC</span><span class="sxs-lookup"><span data-stu-id="2d83f-149">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="2d83f-150">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="2d83f-150">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="2d83f-151">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2d83f-151">Do one of the following:</span></span>
    
  - <span data-ttu-id="2d83f-152">So bearbeiten Sie eine Gruppe: Klicken Sie in der Liste der Gruppen auf die Verteiler-oder Sicherheitsgruppe, die Sie anzeigen oder ändern möchten, \*\*\*\* ![und klicken Sie](../media/ITPro-EAC-EditIcon.gif)dann auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2d83f-152">To edit a group: In the list of groups, click the distribution or security group that you want to view or change, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span> <span data-ttu-id="2d83f-153">Sie können je nach Bedarf allgemeine Einstellungen aktualisieren sowie Gruppenbesitzer oder Gruppenmitglieder hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="2d83f-153">You can update general settings, add or remove group owners, and add or remove group members, as needed.</span></span>
    
  - <span data-ttu-id="2d83f-154">So entfernen Sie eine Gruppe Markieren Sie die Gruppe, und klicken Sie auf **Entfernen**![Entfernen (Symbol)](../media/ITPro-EAC-RemoveIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="2d83f-154">To remove a group: Select the group and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="2d83f-155">Wenn Sie die Änderungen vorgenommen haben, klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2d83f-155">When you're finished making your changes, click **Save**.</span></span>
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="2d83f-156">Erstellen, Bearbeiten oder Entfernen einer Gruppe mithilfe von Windows Remote-PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d83f-156">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="2d83f-p115">Diese Abschnitt enthält Informationen zum Erstellen von Gruppen und Ändern der Eigenschaften der Gruppen mithilfe von Windows Remote-PowerShell. Es wird außerdem gezeigt, wie eine vorhandene Gruppe entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p115">This section provides information about creating groups and changing their properties by using remote Windows PowerShell. It also shows how to remove an existing group.</span></span> 
  
 <span data-ttu-id="2d83f-159">**So erstellen Sie eine Gruppe mithilfe von Windows Remote-PowerShell**</span><span class="sxs-lookup"><span data-stu-id="2d83f-159">**To create a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="2d83f-p116">In diesem Beispiel wird das [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx)-Cmdlet verwendet, um eine Verteilergruppe mit dem Alias "itadmin" und dem Namen "IT Administrators" zu erstellen. Außerdem werden Benutzer als Mitglieder der Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p116">This example uses the [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span> 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

<span data-ttu-id="2d83f-162">Wenn Sie statt einer Verteilergruppe eine Sicherheitsgruppe erstellen möchten, geben Sie stattdessen  `-Type "Security"` an.</span><span class="sxs-lookup"><span data-stu-id="2d83f-162">To create a security group instead of a distribution group, specify  `-Type "Security"` instead.</span></span> 
  
<span data-ttu-id="2d83f-163">Um zu überprüfen, ob die Gruppe "IT Administrators" erfolgreich erstellt wurde, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet aus, um Informationen über die neue Gruppe anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="2d83f-163">To verify that you've successfully created the IT Administrators group, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to display information about the new group:</span></span> 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

<span data-ttu-id="2d83f-164">Um eine Liste der Mitglieder in der Gruppe anzuzeigen, führen Sie das [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx)-Cmdlet wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="2d83f-164">To get a list of members in the group, run the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

<span data-ttu-id="2d83f-165">Um eine vollständige Liste aller Ihrer Gruppen anzuzeigen, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="2d83f-165">To get a full list of all your groups, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 <span data-ttu-id="2d83f-166">**So ändern Sie die Eigenschaften einer Gruppe mithilfe von Windows Remote-PowerShell**</span><span class="sxs-lookup"><span data-stu-id="2d83f-166">**To change the properties of a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="2d83f-p117">Verwenden Sie die Cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) und [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx), um Eigenschaften für Gruppen anzuzeigen und zu ändern. Ein Vorteil der Verwendung von Remote-PowerShell gegenüber dem EAC ist, dass damit Eigenschaften für mehrere Gruppe geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p117">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlets to view and change properties for groups. An advantage of using remote PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span> 
  
<span data-ttu-id="2d83f-169">Hier einige Beispiele für die Verwendung von Windows Remote-PowerShell zur Änderung von Gruppeneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2d83f-169">Here are some examples of using remote Windows PowerShell to change group properties.</span></span>
  
<span data-ttu-id="2d83f-170">In diesem Beispiel wird das [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx)-Cmdlet verwendet, um die primäre SMTP-Adresse (auch als die Antwortadresse bezeichnet) für die Gruppe "Seattle Employees" in "sea.employees@contoso.com" zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2d83f-170">This example uses the [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet to change the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span> 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

<span data-ttu-id="2d83f-p118">Um zu prüfen, ob Sie die Eigenschaften einer Gruppe erfolgreich geändert haben, überprüfen Sie die Änderungen mithilfe des [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlets. Ein Vorteil der Verwendung von Remote-PowerShell besteht darin, dass Sie mehrere Eigenschaften für mehrere Gruppen anzeigen können. Führen Sie im obigen Beispiel, in dem die primäre SMTP-Adressgruppe geändert wurde, folgenden Befehl aus, um den neuen Wert zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="2d83f-p118">To verify that you've successfully changed the properties for a group, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. One advantage of using remote PowerShell is that you can view multiple properties for multiple groups. In the previous example where the primary SMTP address group was changed, run the following command to verify the new value:</span></span> 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

<span data-ttu-id="2d83f-p119">In diesem Beispiel wird das [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx)-Cmdlet verwendet, um alle Mitglieder der Gruppe "Seattle Employees" zu aktualisieren. Verwenden Sie ein Komma, um alle Mitglieder voneinander zu trennen.</span><span class="sxs-lookup"><span data-stu-id="2d83f-p119">This example uses the [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet to update all the members of the Seattle Employees group. Use a comma to separate all members.</span></span> 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

<span data-ttu-id="2d83f-176">Um eine Liste aller Mitglieder in der Gruppe "Seattle Employees" abzurufen, verwenden Sie wie folgt das [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx)-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d83f-176">To get the list of all the members in the group Seattle Employees, use the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 <span data-ttu-id="2d83f-177">**So entfernen Sie eine Gruppe mithilfe von Windows Remote-PowerShell**</span><span class="sxs-lookup"><span data-stu-id="2d83f-177">**To remove a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="2d83f-178">In diesem Beispiel wird das [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx)-Cmdlet verwendet, um eine Verteilergruppe mit dem Namen "IT Administrators" zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2d83f-178">This example uses the [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet to remove a distribution group named IT Administrators.</span></span> 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

<span data-ttu-id="2d83f-179">Um zu überprüfen, ob die Gruppe entfernt wurde, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus, und überprüfen Sie, ob die Gruppe (in diesem Fall ("IT Administrators") gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="2d83f-179">To verify that the group was removed, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows, and confirm that the group (in this case "It Administrators") was deleted.</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```



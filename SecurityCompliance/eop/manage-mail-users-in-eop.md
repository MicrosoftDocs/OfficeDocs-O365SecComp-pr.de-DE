---
title: Verwalten von E-Mail-Benutzern in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP).
ms.openlocfilehash: b0093c64a0fcb5997b474e7bd491c0915164b77e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341026"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="457a8-103">Verwalten von E-Mail-Benutzern in EOP</span><span class="sxs-lookup"><span data-stu-id="457a8-103">Manage mail users in EOP</span></span>

<span data-ttu-id="457a8-p101">Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP). Es gibt mehrere Möglichkeiten zur Verwaltung von Benutzern in EOP.</span><span class="sxs-lookup"><span data-stu-id="457a8-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="457a8-p102">Verwenden der Verzeichnissynchronisierung zum Verwalten von e-Mail-Benutzern: Wenn Ihr Unternehmen über vorhandene Benutzerkonten in einer lokalen Active Directory-Umgebung verfügt, können Sie diese Konten mit Azure Active Directory (AD) synchronisieren, wobei eine Kopie der Konten in der Cloud gespeichert wird. Wenn Sie Ihre vorhandenen Benutzerkonten mit Azure Active Directory synchronisieren, können Sie diese Benutzer im Bereich **Empfänger** der Exchange-Verwaltungskonsole anzeigen. Die Verwendung der Verzeichnissynchronisierung wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="457a8-p102">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud. When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC). Using directory synchronization is recommended.</span></span> 
    
- <span data-ttu-id="457a8-p103">Verwalten von E-Mail-Benutzern über die Exchange Admin Center: Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center. Dies ist der einfachste Weg, E-Mail-Benutzer hinzuzufügen, und hilfreich, um jeweils einen Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="457a8-p103">Use the EAC to manage mail users: Add and manage mail users directly in the EAC. This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>
    
- <span data-ttu-id="457a8-p104">Verwalten von E-Mail-Benutzern mithilfe der Windows Remote-PowerShell: Hinzufügen und Verwalten von E-Mail-Benutzern durch die Ausführung der Windows Remote-PowerShell. Diese Methode ist hilfreich, um mehrere Datensätze hinzuzufügen und Skripts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="457a8-p104">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell. This method is useful for adding multiple records and creating scripts.</span></span>
    
> [!NOTE]
> <span data-ttu-id="457a8-113">Sie können Benutzer im Office 365 Admin Center hinzufügen. Diese Benutzer können allerdings nicht als E-Mail-Empfänger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="457a8-113">You can add users in the Office 365 admin center, however these users can't be used as mail recipients.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="457a8-114">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="457a8-114">Before you begin</span></span>

- <span data-ttu-id="457a8-p105">Für die Verfahren in diesem Thema sind bestimmte Berechtigungen erforderlich. Informationen zu den Berechtigungen finden Sie in den einzelnen Verfahren.</span><span class="sxs-lookup"><span data-stu-id="457a8-p105">Procedures in this topic require specific permissions. See each procedure for its permissions information.</span></span>
    
- <span data-ttu-id="457a8-117">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.</span><span class="sxs-lookup"><span data-stu-id="457a8-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="457a8-p106">Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="457a8-p106">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="457a8-121">Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung</span><span class="sxs-lookup"><span data-stu-id="457a8-121">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="457a8-122">In diesem Abschnitt finden Sie weitere Informationen zum Verwalten von E-Mail-Benutzern mithilfe von Verzeichnissynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="457a8-122">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="457a8-p107">Wenn Sie Verzeichnissynchronisierung zur Verwaltung der Empfänger verwenden, können Sie Benutzer dennoch im Office 365 Admin Center hinzufügen und verwalten. Sie werden dann jedoch nicht mit dem lokalen Active Directory synchronisiert. Dies liegt daran, dass bei der Verzeichnissynchronisierung nur Empfänger aus dem lokalen Active Directory mit der Cloud synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="457a8-p107">If you use directory synchronization to manage your recipients, you can still add and manage users in the Office 365 admin center, but they will not be synchronized with your on-premises Active Directory. This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="457a8-p108">Die Verwendung der Verzeichnissynchronisierung wird für die Verwendung mit den folgenden Features empfohlen: > **Outlook-Listen sicherer Absender und blockierter Absender** -Wenn Sie mit dem Dienst synchronisiert werden, haben diese Listen Vorrang vor der Spamfilterung im Dienst. Dadurch können Benutzer ihre eigenen Listen für sichere Absender und blockierte Absender auf Benutzer-oder Domänenebene verwalten. > **Directory based Edge Blocking (Blockierung)** – Weitere Informationen zu Blockierung finden Sie unter [Use Directory based Edge Blocking to Reject Messages Sent to invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). >- **Spamquarantäne** für Endbenutzer – für den Zugriff auf die Spamquarantäne für Endbenutzer müssen Endbenutzer eine gültige Office 365-Benutzer-ID und ein Kennwort besitzen. EOP-Kunden, die lokale Postfächer schützen, müssen gültige e-Mail-Benutzer sein. >- **Nachrichtenfluss Regeln** : Wenn Sie die Verzeichnissynchronisierung verwenden, werden Ihre vorhandenen Active Directory-Benutzer und-Gruppen automatisch in die Cloud hochgeladen, und Sie können dann Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) erstellen, die bestimmte Benutzer und/ oder Gruppen, ohne Sie manuell über das EAC oder die Exchange Online Protection PowerShell hinzufügen zu müssen. Beachten Sie, dass [dynamische Verteilergruppen](https://go.microsoft.com/fwlink/?LinkId=507569) nicht über die Verzeichnissynchronisierung synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="457a8-p108">Using directory synchronization is recommended for use with the following features: > **Outlook safe sender and blocked sender lists** - When synchronized to the service, these lists will take precedence over spam filtering in the service. This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis. > **Directory Based Edge Blocking (DBEB)** - For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). > **End user spam quarantine** - In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users. > **Mail flow rules** - When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell. Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span> 
  
 <span data-ttu-id="457a8-132">**Bevor Sie beginnen**</span><span class="sxs-lookup"><span data-stu-id="457a8-132">**Before you begin**</span></span>
  
<span data-ttu-id="457a8-133">Rufen Sie die erforderlichen Berechtigungen ab, und bereiten Sie die Verzeichnissynchronisierung vor, wie unter [Vorbereiten der Verzeichnissynchronisierung](https://go.microsoft.com/fwlink/p/?LinkId=308908) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-133">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories"></a><span data-ttu-id="457a8-134">So synchronisieren Sie Benutzerverzeichnisse</span><span class="sxs-lookup"><span data-stu-id="457a8-134">To synchronize user directories</span></span>

1. <span data-ttu-id="457a8-135">Aktivieren Sie die Verzeichnissynchronisierung, wie unter [Aktivieren der Verzeichnissynchronisierung](https://go.microsoft.com/fwlink/p/?LinkId=308909) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-135">Activate directory synchronization, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>
    
2. <span data-ttu-id="457a8-136">Richten Sie den Computer für die Verzeichnissynchronisierung ein, wie unter [Einrichten des Computers für die Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/p/?LinkId=308911) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-136">Set up your directory synchronization computer, as described in [Set up your directory sync computer](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span></span>
    
3. <span data-ttu-id="457a8-137">Synchronisieren Sie die Verzeichnisse, wie unter [Synchronisieren der Verzeichnisse mithilfe des Konfigurations-Assistenten](http://go.microsoft.com/fwlink/?LinkId=308912) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-137">Synchronize your directories, as described in [Use the Configuration Wizard to sync your directories](http://go.microsoft.com/fwlink/?LinkId=308912).</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="457a8-p109">Wenn Sie den Konfigurationsassistent für Azure Active Directory-Synchronisierungstool abschließen, wird in Ihrer Active Directory-Gesamtstruktur das Konto **MSOL_AD_SYNC** erstellt. Dieses Konto wird zum Lesen und Synchronisieren der lokalen Active Directory-Informationen verwendet. Damit die Verzeichnissynchronisierung ordnungsgemäß ausgeführt wird, müssen Sie sicherstellen, dass TCP 443 auf dem lokalen Verzeichnissynchronisierungsserver geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="457a8-p109">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span> 
  
4. <span data-ttu-id="457a8-141">Aktivieren Sie die synchronisierten Benutzer, wie unter [Aktivieren synchronisierter Benutzer](http://go.microsoft.com/fwlink/p/?LinkId=308913) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-141">Activate synced users, as described in [Activate synced users](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span></span>
    
5. <span data-ttu-id="457a8-142">Verwalten Sie die Verzeichnissynchronisierung, wie unter [Verwalten der Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/p/?LinkId=308915) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457a8-142">Manage directory synchronization, as described in [Manage directory synchronization](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span></span>
    
6. <span data-ttu-id="457a8-p110">Überprüfen Sie, ob EOP korrekt synchronisiert. Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**, und vergewissern Sie sich, dass die Liste der Benutzer in Ihrer lokalen Umgebung korrekt synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="457a8-p110">Verify that EOP is synchronizing correctly. In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span> 
    
## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="457a8-145">Verwalten von E-Mail-Benutzern über die Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="457a8-145">Use the EAC to manage mail users</span></span>

<span data-ttu-id="457a8-146">In diesem Abschnitt finden Sie Informationen über das Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center.</span><span class="sxs-lookup"><span data-stu-id="457a8-146">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
 <span data-ttu-id="457a8-147">**Bevor Sie beginnen**</span><span class="sxs-lookup"><span data-stu-id="457a8-147">**Before you begin**</span></span>
  
<span data-ttu-id="457a8-p111">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="457a8-p111">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
  
### <a name="to-add-a-mail-user-in-the-eac"></a><span data-ttu-id="457a8-150">So fügen Sie einen E-Mail-Benutzer in EAC hinzu</span><span class="sxs-lookup"><span data-stu-id="457a8-150">To add a mail user in the EAC</span></span>

1. <span data-ttu-id="457a8-151">Erstellen Sie einen E-Mail-Benutzer, indem Sie in der Verwaltungskonsole **Empfänger** \> **Kontakte** aufrufen und dann auf **Neu +** klicken.</span><span class="sxs-lookup"><span data-stu-id="457a8-151">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>
    
2. <span data-ttu-id="457a8-152">Geben Sie auf der Seite **Neuer E-Mail-Benutzer** die folgenden Benutzerinformationen ein:</span><span class="sxs-lookup"><span data-stu-id="457a8-152">On the **New mail user** page, enter the user's information, including the following:</span></span> 
    
   ****

|<span data-ttu-id="457a8-153">**E-Mail-Benutzereigenschaft**</span><span class="sxs-lookup"><span data-stu-id="457a8-153">**Mail user property**</span></span>|<span data-ttu-id="457a8-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="457a8-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="457a8-155">**Vorname**, **Initialen**, **Nachname**</span><span class="sxs-lookup"><span data-stu-id="457a8-155">**First name**, **Initials**, and **Last name**</span></span> <br/> |<span data-ttu-id="457a8-156">Geben Sie den vollständigen Benutzernamen in die entsprechenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="457a8-156">Type the user's full name in the appropriate boxes.</span></span>  <br/> |
|<span data-ttu-id="457a8-157">**Anzeigename**</span><span class="sxs-lookup"><span data-stu-id="457a8-157">**Display name**</span></span> <br/> |<span data-ttu-id="457a8-p112">Geben Sie einen Namen mit bis zu 64 Zeichen ein. Dieses Feld wird automatisch mit den Namen aufgefüllt, die Sie in den Feldern **Vorname**, **Initialen** und **Nachname** eingegeben haben. Der Anzeigename ist erforderlich.  </span><span class="sxs-lookup"><span data-stu-id="457a8-p112">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.  </span></span><br/> |
|<span data-ttu-id="457a8-161">**Alias**</span><span class="sxs-lookup"><span data-stu-id="457a8-161">**Alias**</span></span> <br/> |<span data-ttu-id="457a8-p113">Geben Sie einen eindeutigen Alias mit bis zu 64 Zeichen für den Benutzer ein. Der Aliasname ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="457a8-p113">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>  <br/> |
|<span data-ttu-id="457a8-164">**Externe E-Mail-Adresse**</span><span class="sxs-lookup"><span data-stu-id="457a8-164">**External email address**</span></span> <br/> |<span data-ttu-id="457a8-165">Geben Sie die externe E-Mail-Adresse des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="457a8-165">Type the external email address of the user.</span></span>  <br/> |
|<span data-ttu-id="457a8-166">**Benutzer-ID**</span><span class="sxs-lookup"><span data-stu-id="457a8-166">**User id**</span></span> <br/> |<span data-ttu-id="457a8-p114">Geben Sie den Namen ein, den der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Der Anmeldename des Benutzers setzt sich aus einem Benutzernamen auf der linken Seite des at-Zeichens (@) und einem Suffix auf der rechten Seite zusammen. Normalerweise ist das Suffix der Name der Domäne, in der sich das Benutzerkonto befindet.</span><span class="sxs-lookup"><span data-stu-id="457a8-p114">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>  <br/> |
|<span data-ttu-id="457a8-170">**Neues Kennwort**</span><span class="sxs-lookup"><span data-stu-id="457a8-170">**New password**</span></span> <br/> |<span data-ttu-id="457a8-p115">Geben Sie das Kennwort ein, das der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Stellen Sie sicher, dass das angegebene Kennwort den Anforderungen hinsichtlich Länge, Komplexität und Verlauf der Domäne entspricht, in der Sie das Benutzerkonto erstellen.</span><span class="sxs-lookup"><span data-stu-id="457a8-p115">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>  <br/> |
|<span data-ttu-id="457a8-173">**Kennwort bestätigen**</span><span class="sxs-lookup"><span data-stu-id="457a8-173">**Confirm password**</span></span> <br/> |<span data-ttu-id="457a8-174">Geben Sie das Kennwort zur Bestätigung erneut ein.</span><span class="sxs-lookup"><span data-stu-id="457a8-174">Retype the password to confirm it.</span></span>  <br/> |
   
3. <span data-ttu-id="457a8-p116">Klicken Sie auf **Speichern**, um den neuen E-Mail-Benutzer zu erstellen. Der neue Benutzer sollte in der Benutzerliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="457a8-p116">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span> 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a><span data-ttu-id="457a8-177">So bearbeiten oder entfernen Sie einen E-Mail-Benutzer in EAC</span><span class="sxs-lookup"><span data-stu-id="457a8-177">To edit or remove a mail user in the EAC</span></span>

- <span data-ttu-id="457a8-p117">Wechseln Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Kontakte**. Klicken Sie in der Liste der Benutzer auf den Benutzer, den Sie anzeigen oder ändern möchten, und wählen \*\*\*\* ![Sie dann Bearbeitungs](../media/ITPro-EAC-EditIcon.gif) Symbol bearbeiten aus, um die Benutzereinstellungen nach Bedarf zu aktualisieren. Sie können den Namen, den Alias oder die Kontaktinformationen des Benutzers ändern und detaillierte Informationen zur Rolle des Benutzers in der Organisation aufzeichnen. Sie können auch einen Benutzer auswählen und dann **Remove**![Remove Icon](../media/ITPro-EAC-RemoveIcon.gif) wählen, um es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="457a8-p117">In the EAC, go to **Recipients** \> **Contacts**. In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed. You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization. You can also select a user and then choose **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a><span data-ttu-id="457a8-182">Verwalten von E-Mail-Benutzern mithilfe der Windows Remote-PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a8-182">Use remote Windows PowerShell to manage mail users</span></span>

<span data-ttu-id="457a8-183">In diesem Abschnitt finden Sie Informationen dazu, wie Sie E-Mail-Benutzer mithilfe der Windows Remote-PowerShell hinzufügen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="457a8-183">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
 <span data-ttu-id="457a8-184">**Bevor Sie beginnen**</span><span class="sxs-lookup"><span data-stu-id="457a8-184">**Before you begin**</span></span>
  
- <span data-ttu-id="457a8-p118">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="457a8-p118">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
    
- <span data-ttu-id="457a8-187">Beachten Sie, dass beim Erstellen von E-Mail-Benutzer mithilfe von Remote-PowerShell-Cmdlets eine Drosselung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="457a8-187">Be aware that when creating mail users by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="457a8-188">Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="457a8-188">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="457a8-189">Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online Protection mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="457a8-189">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
 <span data-ttu-id="457a8-190">**So fügen Sie einen E-Mail-Benutzer mithilfe von Remote-PowerShell hinzu**</span><span class="sxs-lookup"><span data-stu-id="457a8-190">**To add a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="457a8-191">In diesem Beispiel wird anhand des [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx)-Cmdlets für Jeffrey Zeng ein E-Mail-aktiviertes Benutzerkonto mit den folgenden Angaben erstellt:</span><span class="sxs-lookup"><span data-stu-id="457a8-191">This example uses the [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span> 
  
- <span data-ttu-id="457a8-192">Der Vorname ist "Jeffrey" und der Nachname ist "Zeng".</span><span class="sxs-lookup"><span data-stu-id="457a8-192">The first name is Jeffrey and the last name is Zeng.</span></span>
    
- <span data-ttu-id="457a8-193">Der Name ist "Jeffrey", und der Anzeigename ist "Jeffrey Zeng".</span><span class="sxs-lookup"><span data-stu-id="457a8-193">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>
    
- <span data-ttu-id="457a8-194">Der Alias ist "jeffreyz".</span><span class="sxs-lookup"><span data-stu-id="457a8-194">The alias is jeffreyz.</span></span>
    
- <span data-ttu-id="457a8-195">Die externe E-Mail-Adresse ist "jzeng@tailspintoys.com".</span><span class="sxs-lookup"><span data-stu-id="457a8-195">The external email address is jzeng@tailspintoys.com.</span></span>
    
- <span data-ttu-id="457a8-196">Der Office 365-Anmeldename ist "jeffreyz@contoso.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="457a8-196">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>
    
- <span data-ttu-id="457a8-197">Das Kennwort lautet "Pa$$word1".</span><span class="sxs-lookup"><span data-stu-id="457a8-197">The password is Pa$$word1.</span></span>
    
```
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 <span data-ttu-id="457a8-198">**So stellen Sie sicher, dass es funktioniert hat**</span><span class="sxs-lookup"><span data-stu-id="457a8-198">**To verify that this worked**</span></span>
  
<span data-ttu-id="457a8-199">Führen Sie wie folgt das [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx)-Cmdlet aus, um Informationen zu dem neuen E-Mail-Benutzer Jeffrey Zeng anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="457a8-199">Run the [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet as follows to display information about new mail user Jeffrey Zeng:</span></span> 
  
```
Get-User "Jeffrey Zeng"

```

 <span data-ttu-id="457a8-200">**So bearbeiten Sie die Eigenschaften eines E-Mail-Benutzers mithilfe von Remote-PowerShell**</span><span class="sxs-lookup"><span data-stu-id="457a8-200">**To edit the properties of a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="457a8-201">Verwenden Sie die Cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) und [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx), um Eigenschaften für E-Mail-Benutzer anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="457a8-201">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlets to view or change properties for mail users.</span></span> 
  
<span data-ttu-id="457a8-202">In diesem Beispiel wird die externe E-Mail-Adresse für Pilar Pinella festgelegt.</span><span class="sxs-lookup"><span data-stu-id="457a8-202">This example sets the external email address for Pilar Pinilla.</span></span>
  
```
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="457a8-203">In diesem Beispiel wird die Eigenschaft "Company" für alle E-Mail-Benutzer in "Contoso" geändert.</span><span class="sxs-lookup"><span data-stu-id="457a8-203">This example sets the Company property for all mail users to Contoso.</span></span>
  
```
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 <span data-ttu-id="457a8-204">**So stellen Sie sicher, dass es funktioniert hat**</span><span class="sxs-lookup"><span data-stu-id="457a8-204">**To verify that this worked**</span></span>
  
<span data-ttu-id="457a8-p119">Verwenden Sie im vorherigen Beispiel, in dem wir die Eigenschaften für den E-Mail-Benutzer Pilar Pinella geändert haben, das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet, um die Änderungen zu überprüfen. (Beachten Sie, dass Sie für mehrere E-Mail-Kontakte mehrere Eigenschaften anzeigen können.)</span><span class="sxs-lookup"><span data-stu-id="457a8-p119">In the previous example where we changed the properties for mail user Pilar Pinella, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. (Note that you can view multiple properties for multiple mail contacts.)</span></span> 
  
```
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

<span data-ttu-id="457a8-207">Führen Sie für das vorherige Beispiel, in dem die Eigenschaft "Company" für alle E-Mail-Benutzer auf "Contoso" festgelegt wurde, den folgenden Befehl aus, um die Änderungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="457a8-207">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="457a8-208">Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="457a8-208">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span> 
  
 <span data-ttu-id="457a8-209">**So entfernen einen E-Mail-Benutzer mithilfe von Remote-PowerShell**</span><span class="sxs-lookup"><span data-stu-id="457a8-209">**To remove a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="457a8-210">In diesem Beispiel wird das [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx)-Cmdlet verwendet, um den Benutzer Jeffrey Zeng zu löschen:</span><span class="sxs-lookup"><span data-stu-id="457a8-210">This example uses the [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet to delete user Jeffrey Zeng:</span></span> 
  
```
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="457a8-211">**So stellen Sie sicher, dass es funktioniert hat**</span><span class="sxs-lookup"><span data-stu-id="457a8-211">**To verify that this worked**</span></span>
  
<span data-ttu-id="457a8-p120">Führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus. Es sollte eine Fehlermeldung angezeigt werden, da der Benutzer nicht mehr existiert.</span><span class="sxs-lookup"><span data-stu-id="457a8-p120">Run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows. You should get an error message since the user no longer exists.</span></span> 
  
```
Get-Recipient Jeffrey | fl
```



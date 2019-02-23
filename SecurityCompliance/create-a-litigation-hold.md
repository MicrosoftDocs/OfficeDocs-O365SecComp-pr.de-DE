---
title: Erstellen eines Rechtsstreits in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218655"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="85c36-102">Erstellen eines Rechtsstreits in Office 365</span><span class="sxs-lookup"><span data-stu-id="85c36-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="85c36-p101">Sie können ein Postfach für die Aufbewahrung von Rechtsstreitigkeiten platzieren, um alle Postfachinhalte beizubehalten, einschließlich gelöschter Elemente und der ursprünglichen Versionen geänderter Elemente. Wenn Sie ein Benutzerpostfach für die Beweissicherung festlegen, werden Inhalte im Archivpostfach des Benutzers (falls aktiviert) ebenfalls beibehalten. Wenn Sie einen Haltestatus erstellen, können Sie eine Aufbewahrungsdauer (auch als *zeitbasierte Aufbewahrung*bezeichnet) angeben, sodass gelöschte und geänderte Elemente für einen bestimmten Zeitraum aufbewahrt und dann endgültig aus dem Postfach gelöscht werden. Oder Sie können Inhalte auf unbestimmte Zeit aufbewahren (so genannte *unendliche Haltestatus*) oder bis die Beweissicherung entfernt wird. Wenn Sie einen Zeitraum für die Aufbewahrungsdauer angeben, wird er ab dem Datum berechnet, an dem eine Nachricht empfangen oder ein Postfachelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="85c36-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="85c36-108">Hier erfahren Sie, was passiert, wenn Sie einen Rechtsstreit halten.</span><span class="sxs-lookup"><span data-stu-id="85c36-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="85c36-109">Elemente, die vom Benutzer dauerhaft gelöscht werden, werden für die Dauer des haltebereichs im Ordner "Wiederherstellbare Elemente" im Postfach des Benutzers aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="85c36-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="85c36-110">Elemente, die vom Benutzer aus dem Ordner "Wiederherstellbare Elemente" gelöscht werden, werden für die Dauer des haltebereichs beibehalten.</span><span class="sxs-lookup"><span data-stu-id="85c36-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="85c36-111">Das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" wurde von 30 GB auf 110 GB erhöht.</span><span class="sxs-lookup"><span data-stu-id="85c36-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="85c36-112">Elemente in den primären und archivpostfächern des Benutzers werden beibehalten</span><span class="sxs-lookup"><span data-stu-id="85c36-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="85c36-113">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="85c36-113">Before you begin</span></span>

- <span data-ttu-id="85c36-p102">Um ein Exchange Online-Postfach für die Aufbewahrung von Rechtsstreitigkeiten zu aktivieren, muss ihm eine Exchange Online-Plan 2-Lizenz zugewiesen sein. Wenn einem Postfach eine Exchange Online-Plan 1-Lizenz zugewiesen ist, müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, um es in der Warteschleife zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="85c36-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="85c36-116">AufbewahrungsPflicht für ein Postfach im Office 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="85c36-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="85c36-117">Im folgenden finden Sie die Schritte, mit denen Sie mit dem Office 365 Admin Center ein maibox in den Prozess halten können.</span><span class="sxs-lookup"><span data-stu-id="85c36-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="85c36-118">Wechseln Sie https://portal.office.com/adminportal/home zu, und melden Sie sich mit ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="85c36-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="85c36-119">Klicken Sie im linken Navigationsbereich auf**aktive Benutzer Benutzer** . \*\*\*\* > </span><span class="sxs-lookup"><span data-stu-id="85c36-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="85c36-120">Wählen Sie den Benutzer aus, dessen Postfach Sie bei der Beweissicherung platzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="85c36-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="85c36-121">Klicken Sie auf der Seite "Fly-Out" auf **e-Mail-Einstellungen**, und klicken Sie dann neben **rechtsStreit anhalten**auf **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="85c36-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="85c36-122">Klicken Sie auf der Seite für die **Beweis** Sicherung auf die Umschaltfläche, um das Verfahren für die Aufbewahrung zu aktivieren, und füllen Sie die folgenden optionalen Einstellungen aus:</span><span class="sxs-lookup"><span data-stu-id="85c36-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    <span data-ttu-id="85c36-p103">a. **Hold-Dauer (Tage)** – verwenden Sie dieses Feld, um einen zeitbasierten Haltebereich zu erstellen, und geben Sie an, wie lange Postfachelemente aufbewahrt werden, wenn das Postfach in den Rechtsstreit versetzt wird. Die Dauer wird anhand des Datums berechnet, an dem ein Postfachelement empfangen oder erstellt wird. Wenn Sie dieses Feld leer lassen, werden Elemente dauerhaft oder bis zum Entfernen des haltebereichs aufbewahrt. Verwenden Sie Days, um die Dauer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85c36-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="85c36-p104">b. **Hinweis** : Verwenden Sie dieses Feld, um dem Benutzer mitzuteilen, dass sein Postfach in einem Rechtsstreit gehalten wird. Der Hinweis wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn er Outlook 2010 oder höher verwendet. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.</span><span class="sxs-lookup"><span data-stu-id="85c36-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="85c36-p105">c. **Webseite** – verwenden Sie dieses Feld, um den Benutzer zu einer Website zu leiten, um weitere Informationen zur Aufbewahrung von Rechtsstreitigkeiten zu erhalten. Diese URL wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn Sie Outlook 2010 oder höher verwenden. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.</span><span class="sxs-lookup"><span data-stu-id="85c36-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="85c36-137">Klicken Sie auf speichern, um die Beweis **Sicherung** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85c36-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="85c36-138">Nachdem Sie den Haltebereich erstellt haben, wird in den e-Mail-Einstellungen auf der Seite "Fly-Out" angezeigt, dass für den ausgewählten Benutzer die Option "Beweissicherung" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="85c36-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

<span data-ttu-id="85c36-140">Weitere Informationen zum Erstellen und Verwalten von Rechtsstreitigkeiten und zum Verwenden von Exchange Online PowerShell zum Massen Erstellen von Rechtsstreitigkeiten finden Sie unter [platzieren eines Postfachs in der Beweis](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold)Sicherung.</span><span class="sxs-lookup"><span data-stu-id="85c36-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>

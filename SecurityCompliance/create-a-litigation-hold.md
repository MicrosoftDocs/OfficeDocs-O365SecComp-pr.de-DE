---
title: Erstellen Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: 18b3b3a42e5671b1507522c89faaa4ae34198831
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529848"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="0d2b9-102">Erstellen Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten in Office 365</span><span class="sxs-lookup"><span data-stu-id="0d2b9-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="0d2b9-p101">Sie können ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten, die beibehalten werden alle Inhalt von Postfächern, einschließlich der gelöschten Elemente und der ursprünglichen Versionen geänderter Objekte platzieren. Wenn Sie ein Benutzerpostfach beweissicherungsverfahrens einleiten, wird Inhalt im Archivpostfach des Benutzers (falls aktiviert) auch beibehalten. Wenn Sie einen Haltestatus erstellen, können Sie eine Warteschleife Dauer (auch als *zeitbasierte Aufbewahrung*bezeichnet) angeben, sodass gelöscht und geänderte Elemente für einen bestimmten Zeitraum aufbewahrt und dauerhaft aus dem Postfach gelöscht werden. Oder Sie können nur Inhalt auf unbestimmte Zeit beibehalten (eine *unendliche Warteschleife*genannt) oder bis die Aufbewahrung für eventuelle Rechtsstreitigkeiten entfernt wird. Wenn Sie einen Haltestatus Dauer angeben, wird ab dem Datum berechnet eine Nachricht empfangen oder ein Postfach-Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="0d2b9-108">Hier ist, was geschieht, wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="0d2b9-109">Elemente, die vom Benutzer endgültig gelöscht werden, werden im Ordner "wiederherstellbare Elemente" im Postfach des Benutzers für die Dauer des Haltestatus beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="0d2b9-110">Elemente, die vom Benutzer aus dem Ordner wiederherstellbare Elemente gelöscht werden, werden für die Dauer des Haltestatus beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="0d2b9-111">Das Speicherkontingent für "wiederherstellbare Elemente" wird von 30 GB auf 110 GB erhöht.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="0d2b9-112">Elemente des Benutzers primärer und die archivpostfächer werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="0d2b9-113">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="0d2b9-113">Before you begin</span></span>

- <span data-ttu-id="0d2b9-p102">Um ein Exchange Online-Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten zu platzieren, müssen sie eine Lizenz für Exchange Online – Plan 2 zugewiesen werden. Wenn ein Postfach eine Exchange Online – Plan 1-Lizenz zugewiesen ist, müssten Sie weisen Sie ihr eine separate Lizenz der Exchange Online-Archivierung auf platziert halten.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="0d2b9-116">Platzieren eines Postfachs Aufbewahrung für eventuelle Rechtsstreitigkeiten im Office 365 Administrationscenter</span><span class="sxs-lookup"><span data-stu-id="0d2b9-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="0d2b9-117">Hier sind die Schritte, um eine Maibox auf Aufbewahrung für eventuelle Rechtsstreitigkeiten im Office 365 Admin Center zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="0d2b9-118">Wechseln Sie zu https://portal.office.com/adminportal/home und melden Sie sich über das globale Administratorkonto.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="0d2b9-119">Klicken Sie auf **Benutzer** > **aktive Benutzer** im linken Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="0d2b9-120">Wählen Sie den Benutzer, deren Postfach Sie beweissicherungsverfahrens platzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="0d2b9-121">Klicken Sie auf der Seite hinausfliegenden klicken Sie auf **E-Mail-Einstellungen**, und klicken Sie dann auf **Bearbeiten** , neben **Aufbewahrung für eventuelle Rechtsstreitigkeiten**.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="0d2b9-122">Klicken Sie auf der Seite **Aufbewahrung für eventuelle Rechtsstreitigkeiten** auf die Umschaltfläche, um Aufbewahrung für eventuelle Rechtsstreitigkeiten zu aktivieren, und schließen Sie die folgenden optionalen Einstellungen, die angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="0d2b9-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1.PNG](media/O365-LitigationHold1.png)

    <span data-ttu-id="0d2b9-p103">a. **halten Dauer (in Tagen)** -verwenden Sie dieses Feld zum Erstellen einer zeitbasierte Aufbewahrung und angeben, wie lange Postfachelemente gehalten werden, wenn das Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird. Ein Element Postfach empfangen oder erstellt wird, wird die Dauer ab dem Datum berechnet. Wenn Sie dieses Feld leer lassen, werden Elemente aufrechterhalten, auf unbestimmte Zeit oder, bis die Sperre entfernt wurde. Verwenden von Tagen die Dauer angeben.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="0d2b9-p104">b. **Hinweis** - verwenden Sie dieses Feld informiert den Benutzer, den ihr Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten ist. Die Notiz wird auf der Seite Kontoinformationen in das Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. Zugriff auf dieser Seite können Benutzer die **Datei** in Outlook klicken.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="0d2b9-p105">c. **Webseite** - verwenden Sie dieses Feld, um den Benutzer auf eine Website für Weitere Informationen zur Aufbewahrung für eventuelle Rechtsstreitigkeiten zu leiten. Diese URL wird auf der Seite Kontoinformationen in das Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. Zugriff auf dieser Seite können Benutzer die **Datei** in Outlook klicken.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="0d2b9-137">Klicken Sie auf **Speichern** , um die Aufbewahrung für eventuelle Rechtsstreitigkeiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="0d2b9-138">Nachdem Sie den Haltestatus erstellen, die e-Mail-Einstellungen auf der Seite hinausfliegenden zeigt an, Aufbewahrung für eventuelle Rechtsstreitigkeiten für den ausgewählten Benutzer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0d2b9-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2.PNG](media/O365-LitigationHold2.png)

<span data-ttu-id="0d2b9-140">Weitere Informationen zum Erstellen und Verwalten von Rechtsstreitigkeiten enthält und erstellen mithilfe von Exchange Online PowerShell Massen-Aufbewahrung für eventuelle enthält finden Sie unter [Place ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="0d2b9-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>

---
title: Suchen nach und Löschen von Nachrichten – Administratorhilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: Mithilfe des Cmdlets Search-Mailbox können Administratoren Benutzerpostfächer durchsuchen und anschließend Nachrichten aus Postfächern löschen.
ms.openlocfilehash: ed110c4a3e36a93970af99e9548aa293d94307fd
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026582"
---
# <a name="search-for-and-delete-messages---admin-help"></a><span data-ttu-id="692b3-103">Suchen nach und Löschen von Nachrichten – Administratorhilfe</span><span class="sxs-lookup"><span data-stu-id="692b3-103">Search for and delete messages - Admin help</span></span>
  
<span data-ttu-id="692b3-104">Mithilfe des Cmdlets **Search-Mailbox** können Administratoren Benutzerpostfächer durchsuchen und anschließend Nachrichten aus Postfächern löschen.</span><span class="sxs-lookup"><span data-stu-id="692b3-104">Administrators can use the **Search-Mailbox** cmdlet to search user mailboxes and then delete messages from a mailbox.</span></span> 
  
<span data-ttu-id="692b3-p101">Um Nachrichten in einem Schritt zu suchen und zu löschen, führen Sie das Cmdlet **Search-Mailbox** mit der Option  _DeleteContent_ aus. Dabei können Sie jedoch keine Suchergebnisse in einer Vorschau anzeigen und kein Protokoll der von der Suche zurückgegebenen Nachrichten generieren. Außerdem löschen Sie ggf. versehentlich Nachrichten, die Sie gar nicht löschen wollten. Um ein Protokoll der von der Suche gefundenen Nachrichten in der Vorschau anzuzeigen, bevor sie gelöscht werden, führen Sie das Cmdlet **Search-Mailbox** mit der Option  _LogOnly_ aus.</span><span class="sxs-lookup"><span data-stu-id="692b3-p101">To search and delete messages in one step, run the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch. However, when you do this, you can't preview search results or generate a log of messages that will be returned by the search, and you may inadvertently delete messages that you didn't intend to. To preview a log of the messages found in the search before they're deleted, run the **Search-Mailbox** cmdlet with the  _LogOnly_ switch.</span></span> 
  
<span data-ttu-id="692b3-p102">Als zusätzliche Schutzmaßnahme können Sie die Nachrichten zuerst in ein anderes Postfach kopieren; dazu verwenden Sie die Parameter  _TargetMailbox_ und  _TargetFolder_. So behalten Sie eine Kopie der gelöschten Nachrichten für den Fall, dass Sie wieder auf sie zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="692b3-p102">As an additional safeguard, you can first copy the messages to another mailbox by using the  _TargetMailbox_ and  _TargetFolder_ parameters. By doing this, you retain a copy of the deleted messages in case you need to access them again.</span></span> 
  
## <a name="what-do-i-need-to-know-before-i-begin"></a><span data-ttu-id="692b3-110">Was muss ich wissen, bevor ich beginne?</span><span class="sxs-lookup"><span data-stu-id="692b3-110">What do I need to know before I begin?</span></span>
<span data-ttu-id="692b3-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="692b3-111"></span></span>

- <span data-ttu-id="692b3-p103">Geschätzte Zeit bis zum Abschließen des Vorgangs: 10 Minuten. Die tatsächliche Zeit kann von der Größe des Postfachs und der Suchabfrage abhängen.</span><span class="sxs-lookup"><span data-stu-id="692b3-p103">Estimated time to complete: 10 minutes. The actual time may vary depending on the size of the mailbox and the search query.</span></span>
    
- <span data-ttu-id="692b3-p104">Diese Verfahren können nicht in der Exchange-Verwaltungskonsole ausgeführt werden. Sie müssen die Shell verwenden.</span><span class="sxs-lookup"><span data-stu-id="692b3-p104">You can't use the Exchange admin center (EAC) to perform these procedures. You must use the Shell.</span></span>
    
- <span data-ttu-id="692b3-116">Ihnen müssen die beiden folgenden Verwaltungsrollen zugewiesen sein, damit Sie in den Benutzerpostfächern nach Nachrichten suchen und Nachrichten löschen können:</span><span class="sxs-lookup"><span data-stu-id="692b3-116">You need to be assigned both of the following management roles to search for and delete messages in users' mailboxes:</span></span>
    
  - <span data-ttu-id="692b3-p105">**Postfachsuche** Dieser Rolle können Sie über mehrere Postfächer in Ihrer Organisation nach Nachrichten gesucht. Administratoren sind nicht dieser Rolle standardmäßig zugewiesen. Um sich selbst, damit Sie Postfächer suchen können diese Rolle zuweisen möchten, fügen Sie selbst als Mitglied der Rollengruppe "Discoveryverwaltung" hinzu. Finden Sie unter [Hinzufügen eines Benutzers auf die Rolle "Discoveryverwaltung"](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).</span><span class="sxs-lookup"><span data-stu-id="692b3-p105">**Mailbox Search** This role allows you to search for messages across multiple mailboxes in your organization. Administrators aren't assigned this role by default. To assign yourself this role so that you can search mailboxes, add yourself as a member of the Discovery Management role group. See [Add a User to the Discovery Management Role Group](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).</span></span>
    
  - <span data-ttu-id="692b3-p106">**Postfach-Import/Export** Dieser Rolle können Sie Nachrichten aus dem Postfach eines Benutzers zu löschen. Standardmäßig ist nicht dieser Rolle alle Rollengruppe zugewiesen. Um Nachrichten aus den Postfächern der Benutzer zu löschen, können Sie die Rolle Postfach Import/Export der Rollengruppe "Organisationsverwaltung" hinzufügen. Weitere Informationen finden Sie im Abschnitt "Hinzufügen eine Rolle zu einer Rollengruppe" in [Rollengruppen verwalten](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) .</span><span class="sxs-lookup"><span data-stu-id="692b3-p106">**Mailbox Import Export** This role allows you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group. For more information, see the "Add a role to a role group" section in [Manage Role Groups](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) .</span></span> 
    
- <span data-ttu-id="692b3-p107">Wenn für das Postfach, aus dem Sie Nachrichten löschen möchten, die Wiederherstellung einzelner Elemente aktiviert ist, müssen Sie diese Funktion zuerst deaktivieren. Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren der Wiederherstellung einzelner Elemente für ein Postfach](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).</span><span class="sxs-lookup"><span data-stu-id="692b3-p107">If the mailbox from which you want to delete messages has single item recovery enabled, you must first disable the feature. For more information, see [Enable or disable single item recovery for a mailbox](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).</span></span>
    
- <span data-ttu-id="692b3-p108">Wenn das Postfach aus dem Sie Nachrichten löschen möchten, in die Warteschleife gestellt wird, wird empfohlen, dass Sie mit der Verwaltung von Datensätzen und die rechtsabteilung vor den Haltestatus entfernen und löschen den Inhalt von Postfächern überprüfen. Nachdem Sie Genehmigung erhalten haben, befolgen Sie die Schritte im Thema [Der Ordner für wiederherstellbare Elemente Clean](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx)aus.</span><span class="sxs-lookup"><span data-stu-id="692b3-p108">If the mailbox from which you want to delete messages is placed on hold, we recommend that you check with your records management or legal department before removing the hold and deleting the mailbox content. After you obtain approval, follow the steps listed in the topic [Clean Up the Recoverable Items Folder](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).</span></span>
    
- <span data-ttu-id="692b3-p109">Mithilfe des Cmdlets **Search-Mailbox** können maximal 10.000 Postfächer durchsucht werden. Wenn Sie eine Exchange Online-Organisation mit mehr als 10.000 Postfächern haben, können Sie die Funktion „Compliancesuche" (oder das entsprechende Cmdlet **New-ComplianceSearch** ) verwenden, um eine unbegrenzte Anzahl von Postfächern zu durchsuchen. Anschließend können Sie mit dem Cmdlet **New-ComplianceSearchAction** die Nachrichten löschen, die von der Compliancesuche zurückgegeben wurden. Weitere Informationen finden Sie unter [Suchen und Löschen von E-Mail-Nachrichten in Ihrer Office 365-Organisation - Administratorhilfe](https://go.microsoft.com/fwlink/p/?LinkId=786856).</span><span class="sxs-lookup"><span data-stu-id="692b3-p109">You can search a maximum of 10,000 mailboxes using the **Search-Mailbox** cmdlet. If you're an Exchange Online organization and have more than 10,000 mailboxes, you can use the Compliance Search feature (or the corresponding **New-ComplianceSearch** cmdlet) to search an unlimited number of mailboxes. Then you can use the **New-ComplianceSearchAction** cmdlet to delete the messages returned by a compliance search. For more information, see [Search for and delete email messages from your Office 365 organization](https://go.microsoft.com/fwlink/p/?LinkId=786856).</span></span>
    
- <span data-ttu-id="692b3-p110">Wenn Sie eine Suchabfrage (durch Verwendung des Parameters  *SearchQuery*  ) einschließen, gibt das Cmdlet **Search-Mailbox** maximal 10.000 Elemente in den Suchergebnissen zurück. Wenn Sie also eine Suchabfrage einschließen, müssen Sie den Befehl **Search-Mailbox** möglicherweise mehrere Male ausführen, um mehr als 10.000 Elemente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="692b3-p110">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
    
- <span data-ttu-id="692b3-p111">Archivpostfach des Benutzers wird auch gesucht werden soll, wenn Sie das **Search-Mailbox** -Cmdlet ausführen. In ähnlicher Weise werden Elemente in der primären Archivpostfach beim Verwenden mit dem Cmdlet **Search-Mailbox** mit _der Option deletecontent_ gelöscht. Um dies zu verhindern, können Sie die Option *DoNotIncludeArchive* einschließen. Darüber hinaus wird empfohlen, dass Sie _der Option deletecontent_ nicht verwenden zum Löschen von Nachrichten in Exchange Online Postfächer, die automatisch erweitert Archivierung aktiviert, da unerwartete Datenverluste auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="692b3-p111">The user's archive mailbox will also be searched when you run the **Search-Mailbox** cmdlet. Similarly, items in the primary archive mailbox will be deleted when you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch. To prevent this, you can include the  *DoNotIncludeArchive*  switch. Also, we recommend that you don't use the  _DeleteContent_ switch to delete messages in Exchange Online mailboxes that have auto-expanding archiving enabled because unexpected data loss may occur.</span></span> 
    
## <a name="search-messages-and-log-the-search-results"></a><span data-ttu-id="692b3-139">Suchen von Nachrichten und Protokollieren der Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="692b3-139">Search messages and log the search results</span></span>
<span data-ttu-id="692b3-140"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="692b3-140"></span></span>

<span data-ttu-id="692b3-p112">In diesem Beispiel wird das Postfach von April Stewart nach Nachrichten mit dem Satz "Your bank statement" im Betrefffeld durchsucht. Die Suchergebnisse werden im Postfach des Administrators im Ordner "SearchAndDeleteLog" protokolliert. Nachrichten werden nicht in das Zielpostfach kopiert und nicht aus diesem gelöscht.</span><span class="sxs-lookup"><span data-stu-id="692b3-p112">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and logs the search results in the SearchAndDeleteLog folder of the administrator's mailbox. Messages aren't copied to or deleted from the target mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="692b3-143">In diesem Beispiel werden alle Postfächer in der Organisation nach Nachrichten durchsucht, an die ein beliebiger Typ von Datei mit dem Namen "Trojan" angefügt ist. Anschließend wird eine Protokollnachricht an das Administratorpostfach gesendet.</span><span class="sxs-lookup"><span data-stu-id="692b3-143">This example searches all mailboxes in the organization for messages that have any type of attached file that contains the word "Trojan" in the filename and sends a log message to the administrator's mailbox.</span></span>
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

<span data-ttu-id="692b3-144">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span><span class="sxs-lookup"><span data-stu-id="692b3-144">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>
  
[<span data-ttu-id="692b3-145">Nach oben</span><span class="sxs-lookup"><span data-stu-id="692b3-145">Return to top</span></span>](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="search-and-delete-messages"></a><span data-ttu-id="692b3-146">Suchen und Löschen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="692b3-146">Search and delete messages</span></span>
<span data-ttu-id="692b3-147"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="692b3-147"></span></span>

<span data-ttu-id="692b3-p113">In diesem Beispiel wird das Postfach von April Stewart nach Nachrichten mit dem Satz "Your bank statement" im Betrefffeld durchsucht. Die Nachrichten werden aus dem Quellpostfach gelöscht, ohne dass die Suchergebnisse in einen anderen Ordner kopiert werden. Wie bereits erklärt muss Ihnen die Verwaltungsrolle "Postfachimport/-export" zugewiesen sein, damit Sie Nachrichten aus einem Benutzerpostfach löschen können.</span><span class="sxs-lookup"><span data-stu-id="692b3-p113">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field and deletes the messages from the source mailbox without copying the search results to another folder. As previously explained, you need to be assigned the Mailbox Import Export management role to delete messages from a user's mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="692b3-p114">Wenn Sie das Cmdlet **Search-Mailbox** mit der Option  _DeleteContent_ verwenden, werden Nachrichten dauerhaft aus dem Quellpostfach gelöscht. Bevor Sie Nachrichten dauerhaft löschen, sollten Sie mit der Option  _LogOnly_ ein Protokoll der von der Suche gefundenen Nachrichten generieren, bevor sie gelöscht werden, oder die Nachrichten in ein anderes Postfach kopieren, bevor Sie sie aus dem Quellpostfach löschen.</span><span class="sxs-lookup"><span data-stu-id="692b3-p114">When you use the **Search-Mailbox** cmdlet with the  _DeleteContent_ switch, messages are permanently deleted from the source mailbox. Before you permanently delete messages, we recommend that you either use the  _LogOnly_ switch to generate a log of the messages found in the search before they're deleted or copy the messages to another mailbox before deleting them from the source mailbox.</span></span> 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

<span data-ttu-id="692b3-152">In diesem Beispiel wird das Postfach von April Stewart nach Nachrichten mit dem Satz "Your bank statement" im Betrefffeld durchsucht. Die Suchergebnisse werden in den Ordner "AprilStewart-DeletedMessages" im Postfach "BackupMailbox" kopiert und aus dem Postfach von April Stewart gelöscht.</span><span class="sxs-lookup"><span data-stu-id="692b3-152">This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the Subject field, copies the search results to the folder AprilStewart-DeletedMessages in the mailbox BackupMailbox, and deletes the messages from April's mailbox.</span></span>
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

<span data-ttu-id="692b3-153">In diesem Beispiel werden alle Postfächer in der Organisation nach Nachrichten mit der Betreffzeile "Laden Sie diese Datei herunter" durchsucht und dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="692b3-153">This example searches all mailboxes in the organization for messages with the subject line "Download this file", and then permanently deletes them.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

<span data-ttu-id="692b3-154">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span><span class="sxs-lookup"><span data-stu-id="692b3-154">For detailed syntax and parameter information, see [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).</span></span>
  
[<span data-ttu-id="692b3-155">Nach oben</span><span class="sxs-lookup"><span data-stu-id="692b3-155">Return to top</span></span>](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="using-the--loglevel-full-parameter"></a><span data-ttu-id="692b3-156">Verwenden des Parameters -LogLevel Full</span><span class="sxs-lookup"><span data-stu-id="692b3-156">Using the -LogLevel Full parameter</span></span>
<span data-ttu-id="692b3-157"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="692b3-157"></span></span>

<span data-ttu-id="692b3-p115">In einigen der Beispiele oben wurde der Parameter  _LogLevel_ mit dem Wert  `Full` verwendet, um detaillierte Informationen zu den vom Cmdlet **Search-Mailbox** zurückgegebenen Ergebnissen zu protokollieren. Wenn Sie diesen Parameter verwendet haben, wird eine E-Mail-Nachricht erstellt und an das im Parameter  _TargetMailbox_ angegebene Postfach gesendet. Die Protokolldatei (eine CSV-formatierte Datei mit dem Namen „Results.csv") ist dieser E-Mail-Nachricht angefügt und wird in dem Ordner abgelegt, der im Parameter  _TargetFolder_ angegeben ist. Die Protokolldatei enthält eine Zeile für jede Nachricht, die in den vom Cmdlet **Search-Mailbox** zurückgegebenen Suchergebnissen aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="692b3-p115">In some of the previous examples, the  _LogLevel_ parameter, with the  `Full` value is used to log detailed information about the results returned by the **Search-Mailbox** cmdlet. When you included this parameter, an email message is created and sent to the mailbox specified by the  _TargetMailbox_ parameter. The log file (which is a CSV-formatted file named Search Results.csv) is attached to this email message, and will be located in the folder specified by the  _TargetFolder_ parameter. The log file contains a row for each message that's included in the search results when you run the **Search-Mailbox** cmdlet.</span></span> 
  


---
title: BULK Import externe Kontakte zu Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Hier erfahren Sie, wie Administratoren können Exchange Online PowerShell und eine CSV-Datei zu Massen-Importieren von externen Kontakten in der globalen Adressliste.
ms.openlocfilehash: 4bde56d49ccf94dc91993df90e1ae693e25c961a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528939"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a><span data-ttu-id="8507d-103">BULK Import externe Kontakte zu Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8507d-103">Bulk import external contacts to Exchange Online</span></span>

<span data-ttu-id="8507d-104">**Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von Kontakten in Ihrem Postfach? Finden Sie unter [Importieren von Kontakten in Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span><span class="sxs-lookup"><span data-stu-id="8507d-104">**This article is for administrators. Are you trying to import contacts to your own mailbox? See [Import contacts to Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span></span>
   
<span data-ttu-id="8507d-p101">Hat Ihr Unternehmen? vielen vorhandenen Geschäftskontakten, die im freigegebenen Adressbuch (auch als "die globalen Adressliste" bezeichnet) enthalten sein sollen in Exchange Online Möchten Sie als Mitglieder von Verteilergruppen, wie Sie mit Benutzern in Ihrem Unternehmen können externe Kontakte hinzufügen? Importieren Sie externe Kontakte in Exchange Online, wenn Ja, Sie Exchange Online PowerShell und einer Datei (durch Kommas getrennte Werte) an Massen verwenden können. Es ist ein dreistufiger Prozess:</span><span class="sxs-lookup"><span data-stu-id="8507d-p101">Does your company have lots of existing business contacts that you want to include in the shared address book (also called the global address list) in Exchange Online? Do you want to add external contacts as members of distribution groups, just like you can with users inside your company? If so, you can use Exchange Online PowerShell and a CSV (Comma Separated Value) file to bulk import external contacts into Exchange Online. It's a three-step process:</span></span>
  
[<span data-ttu-id="8507d-109">Schritt 1: Erstellen einer CSV-Datei, die Informationen über die externe Kontakte enthält.</span><span class="sxs-lookup"><span data-stu-id="8507d-109">Step 1: Create a CSV file that contains information about the external contacts</span></span>](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[<span data-ttu-id="8507d-110">Schritt 2: Erstellen von externen Kontakten mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="8507d-110">Step 2: Create the external contacts with PowerShell</span></span>](#step-2-create-the-external-contacts-with-powershell) 

[<span data-ttu-id="8507d-111">Schritt 3: Hinzufügen von Informationen zu den Eigenschaften des externen Kontakten</span><span class="sxs-lookup"><span data-stu-id="8507d-111">Step 3: Add information to the properties of the external contacts</span></span>](#step-3-add-information-to-the-properties-of-the-external-contacts)

<span data-ttu-id="8507d-112">Nachdem Sie diese Schritte, um Kontakte importieren abgeschlossen haben, können Sie diese zusätzlichen Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="8507d-112">After you complete these steps to import contacts, you can perform these additional tasks:</span></span>
  
- [<span data-ttu-id="8507d-113">Mehrere externe Kontakte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8507d-113">Add more external contacts</span></span>](bulk-import-external-contacts.md#AddMore)
  
- [<span data-ttu-id="8507d-114">Ausblenden von externen Kontakten aus dem freigegebenen Adressbuch</span><span class="sxs-lookup"><span data-stu-id="8507d-114">Hide external contacts from the shared address book</span></span>](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a><span data-ttu-id="8507d-115">Schritt 1: Erstellen einer CSV-Datei, die Informationen über die externe Kontakte enthält.</span><span class="sxs-lookup"><span data-stu-id="8507d-115">Step 1: Create a CSV file that contains information about the external contacts</span></span>

<span data-ttu-id="8507d-116">Der erste Schritt besteht eine CSV-Datei erstellen, die Informationen für jeden externen Kontakt enthält, die Sie zu Exchange Online importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8507d-116">The first step is to create a CSV file that contains information about each external contact that you want to import to Exchange Online.</span></span> 
  
1. <span data-ttu-id="8507d-117">Kopieren Sie den folgenden Text in eine Textdatei in Microsoft Editor, und speichern sie auf Ihrem Desktop als eine CSV-Datei mithilfe von Filename Suffix CSV; beispielsweise ExternalContacts.csv.</span><span class="sxs-lookup"><span data-stu-id="8507d-117">Copy the following text to a text file in NotePad, and save it to your desktop as a CSV file by using a filename suffix of .csv; for example, ExternalContacts.csv.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="8507d-118">Wenn Ihre Sprache Sonderzeichen (wie **Å**, **Ä**und **Ö** in Schwedisch) speichern Sie die CSV-Datei mit UTF-8- oder anderen Unicode-Codierung enthält, wenn Sie im Editor die Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="8507d-118">If your language contains special characters (such as **å**, **ä**, and **ö** in Swedish) save the CSV file with UTF-8 or other Unicode encoding when you save the file in NotePad.</span></span> 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    <span data-ttu-id="8507d-p102">Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Eigenschaften des Kontakte, die beim Importieren zu Exchange Online verwendet werden können. Name der Eigenschaft wird durch ein Komma getrennt. Jede Zeile unter der Überschrift steht der Eigenschaftswerte für den Import von einem externen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="8507d-p102">The first row, or header row, of the CSV file lists the properties of contacts that can be used when you import them to Exchange Online. Each property name is separated by a comma. Each row under the header row represents the property values for importing a single external contact.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8507d-p103">Dieser Text enthält Beispieldaten, die Sie löschen können. Aber nicht löschen Sie oder ändern Sie die erste Zeile (Kopfzeile). Sie enthält alle Eigenschaften für die externe Kontakte.</span><span class="sxs-lookup"><span data-stu-id="8507d-p103">This text includes sample data, which you can delete. But don't delete or change the first (header) row. It contains all of the properties for the external contacts.</span></span> 
  
2. <span data-ttu-id="8507d-125">Öffnen Sie die CSV-Datei in Microsoft Excel so bearbeiten Sie die CSV-Datei, da es wesentlich einfacher ist zu Excel verwenden, um die CSV-Datei zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8507d-125">Open the CSV file in Microsoft Excel to edit the CSV file because it's much easier to use Excel to edit the CSV file.</span></span>
    
3. <span data-ttu-id="8507d-p104">Erstellen Sie eine Zeile für jeden Kontakt, den Sie zu Exchange Online importieren möchten. Füllen Sie so viele der Zellen wie möglich. Diese Informationen werden im freigegebenen Adressbuch für jeden Kontakt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8507d-p104">Create a row for each contact that you want to import to Exchange Online. Populate as many of the cells as possible. This information will be displayed in the shared address book for each contact.</span></span> 
    
    > [!IMPORTANT]
    >  <span data-ttu-id="8507d-p105">Die folgenden Eigenschaften (die in der Kopfzeile der ersten vier Elemente sind) sind erforderlich, um einen externen Kontakt zu erstellen und in der CSV-Datei aufgefüllt werden müssen: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. PowerShell-Befehl, den Sie in Schritt2 ausführen werden die Werte für diese Eigenschaften verwenden, um die Kontakte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8507d-p105">The following properties (which are the first four items in the header row) are required to create an external contact and must be populated in the CSV file: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. The PowerShell command that you run in Step 2 will use the values for these properties to create the contacts.</span></span> 

## <a name="step-2-create-the-external-contacts-with-powershell"></a><span data-ttu-id="8507d-131">Schritt 2: Erstellen von externen Kontakten mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="8507d-131">Step 2: Create the external contacts with PowerShell</span></span>

<span data-ttu-id="8507d-132">Im nächsten Schritt wird die CSV-Datei verwenden, die Sie in Schritt 1 erstellt haben, und PowerShell-Skripte zur Bulk Importieren der externe Kontakte, die in der CSV-Datei zu Exchange Online aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8507d-132">The next step is to use the CSV file that you created in Step 1 and PowerShell to bulk import the external contacts listed in the CSV file to Exchange Online.</span></span> 
  
1.  <span data-ttu-id="8507d-p106">Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Achten Sie darauf, dass Sie den Benutzernamen und das Kennwort für Ihr Office 365 globaler Administrator-Konto verwenden, beim Herstellen der Verbindung zu Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8507d-p106">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Be sure to use the user name and password for your Office 365 global administrator account when you connect to Exchange Online PowerShell.</span></span> 
    
2. <span data-ttu-id="8507d-136">Nachdem Sie zu Exchange Online PowerShell verbunden haben, fahren Sie mit der desktop-Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert; beispielsweise `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="8507d-136">After you connect PowerShell to Exchange Online, go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="8507d-137">Führen Sie den folgenden Befehl zum Erstellen von externen Kontakten aus:</span><span class="sxs-lookup"><span data-stu-id="8507d-137">Run the following command to create the external contacts:</span></span>

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    <span data-ttu-id="8507d-p107">Es kann eine Weile zum Erstellen der neuen Kontakte, je nachdem, wie viele importierten dauern. Wenn der Befehl abgeschlossen wird ausgeführt, PowerShell zeigt eine Liste der neuen Kontakte, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="8507d-p107">It might take a while to create the new contacts, depending on how many you're importing. When the command is finished running, PowerShell displays a list of the new contacts that were created.</span></span> 
    
4. <span data-ttu-id="8507d-140">Um die neue externe Kontakte angezeigt, besuchen Sie die Exchange-Verwaltungskonsole (EAC), und klicken Sie dann auf **Empfänger** \> **Kontakte**.</span><span class="sxs-lookup"><span data-stu-id="8507d-140">To view the new external contacts, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="8507d-141">Anweisungen für die Verbindung mit der Exchange-Verwaltungskonsole finden Sie unter [Exchange Admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span><span class="sxs-lookup"><span data-stu-id="8507d-141">For instructions for connecting to the EAC, see [Exchange admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span></span> 
  
5. <span data-ttu-id="8507d-142">Klicken Sie auf **Aktualisieren** , falls erforderlich, ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) an, die Liste aktualisieren und die externen Kontakte, die importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8507d-142">If necessary, click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list and see the external contacts that were imported.</span></span> 
    
    <span data-ttu-id="8507d-143">Die importierten Kontakte werden in im freigegebenen Adressbuch in Outlook und Outlook im Web angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8507d-143">The imported contacts will appear in the shared address book in Outlook and Outlook on the web.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8507d-144">Sie können auch die Kontakte in Office 365 Administrationscenter anzeigen, indem Sie auf **Benutzer** \> **Kontakte**.</span><span class="sxs-lookup"><span data-stu-id="8507d-144">You can also view the contacts in the Office 365 admin center by going to **Users** \> **Contacts**.</span></span> 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a><span data-ttu-id="8507d-145">Schritt 3: Hinzufügen von Informationen zu den Eigenschaften des externen Kontakten</span><span class="sxs-lookup"><span data-stu-id="8507d-145">Step 3: Add information to the properties of the external contacts</span></span>

<span data-ttu-id="8507d-p108">Nach dem Ausführen des Befehls in Schritt2 externe Kontakte erstellt werden, jedoch können sie die Informationen Kontakts oder der Organisation, die die Informationen aus der Großteil der Zellen in der CSV-Datei ist nicht enthalten. Dies ist, da beim Erstellen neuer externe Kontakte nur die erforderlichen Eigenschaften aufgefüllt werden. Machen Sie sich keine Gedanken Sie, wenn Sie alle Informationen, die in der CSV-Datei gefüllt haben. Wenn es nicht vorhanden ist, werden nicht es hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8507d-p108">After you run the command in Step 2, the external contacts are created, but they don't contain any of the contact or organization information, which is the information from the most of the cells in the CSV file. This is because when you create new external contacts, only the required properties are populated. Don't worry if you don't have all the information populated in the CSV file. If it's not there, it won't be added.</span></span>
  
1.  <span data-ttu-id="8507d-p109">Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="8507d-p109">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="8507d-152">Wechseln Sie zum desktop-Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert; beispielsweise `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="8507d-152">Go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="8507d-153">Führen Sie die folgenden zwei Befehle aus, um die anderen Eigenschaften aus der CSV-Datei an die externe Kontakte hinzuzufügen, die Sie in Schritt2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8507d-153">Run the following two commands to add the other properties from the CSV file to the external contacts that you created in Step 2.</span></span>
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > <span data-ttu-id="8507d-p110">Der Parameter _Manager_ kann problematisch sein. Wenn die Zelle in der CSV-Datei leer ist, erhalten Sie eine Fehlermeldung und keiner der Informationen über die Eigenschaft wird auf den Kontakt hinzugefügt werden. Wenn Sie keinen Manager angeben müssen, klicken Sie dann einfach löschen ` -Manager $_.Manager ` aus dem vorherigen PowerShell-Befehl.</span><span class="sxs-lookup"><span data-stu-id="8507d-p110">The  _Manager_ parameter might be problematic. If the cell is blank in the CSV file, you will get an error and none of the property information will be added to the contact. If you don't need to specify a manager, then just delete  ` -Manager $_.Manager ` from the previous PowerShell command.</span></span> 
  
    <span data-ttu-id="8507d-157">Erneut, kann es eine Weile so aktualisieren Sie die Kontakte aus, je nachdem, wie viele Sie in Schritt 1 importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8507d-157">Again, it might take a while to update the contacts, depending on how many you imported in Step 1.</span></span> 
    
4. <span data-ttu-id="8507d-158">So überprüfen, dass die Eigenschaften der Kontakte hinzugefügt wurden:</span><span class="sxs-lookup"><span data-stu-id="8507d-158">To verify that the properties were added to the contacts:</span></span> 
    
1. <span data-ttu-id="8507d-159">Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**.</span><span class="sxs-lookup"><span data-stu-id="8507d-159">In the EAC, go to **Recipients** \> **Contacts**.</span></span>
    
2. <span data-ttu-id="8507d-160">Klicken Sie auf einen Kontakt, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) Eigenschaften des Kontakts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8507d-160">Click a contact and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) to display the contact's properties.</span></span> 
    
<span data-ttu-id="8507d-p111">Das wars! Benutzer können die Kontakte und Weitere Informationen im Outlook-Adressbuch und Outlook im Web finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="8507d-p111">That's it! Users can see the contacts and the additional information in the address book Outlook and Outlook on the web.</span></span>
  
## <a name="add-more-external-contacts"></a><span data-ttu-id="8507d-163">Mehrere externe Kontakte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8507d-163">Add more external contacts</span></span>

<span data-ttu-id="8507d-p112">Sie können wiederholen Sie die Schritte 1 bis Schritt 3, um neue externe Kontakte in Exchange Online hinzuzufügen. Sie oder ein Benutzer in Ihrem Unternehmen können einfach eine neue Zeile in der CSV-Datei für den neuen Kontakt hinzufügen. Anschließend können Sie die PowerShell-Befehle ausführen, aus Schritt2 und Schritt 3 zum Erstellen und Hinzufügen von Informationen zu den neuen Kontakten.</span><span class="sxs-lookup"><span data-stu-id="8507d-p112">You can repeat Steps 1 through Step 3 to add new external contacts in Exchange Online. You or users in your company can just add a new row in the CSV file for the new contact. Then you can run the PowerShell commands from Step 2 and Step 3 to create and add information to the new contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8507d-p113">Wenn Sie den Befehl zum Erstellen von neuer Kontakten ausführen, erhalten Sie möglicherweise eine Fehlermeldung ausgegeben, dass die Kontakte, die bereits zuvor erstellten vorhanden sind. Jedoch neuer Kontakt hinzufügen möchten die CSV-Datei wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="8507d-p113">When you run the command to create new contacts, you might get an error saying that the contacts that were created earlier already exist. But any new contact added to the CSV file is created.</span></span> 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a><span data-ttu-id="8507d-169">Ausblenden von externen Kontakten aus dem freigegebenen Adressbuch ></span><span class="sxs-lookup"><span data-stu-id="8507d-169">Hide external contacts from the shared address book></span></span>

<span data-ttu-id="8507d-p114">In einigen Unternehmen können externe Kontakte, so dass sie als Mitglieder von Verteilergruppen hinzugefügt werden können. In diesem Szenario können sie externe Kontakte aus dem freigegebenen Adressbuch ausblenden möchten. Hier ist wie:</span><span class="sxs-lookup"><span data-stu-id="8507d-p114">Some companies may use external contacts only so they can be added as members of distribution groups. In this scenario, they may want to hide external contacts from the shared address book. Here's how:</span></span>
  
1.  <span data-ttu-id="8507d-p115">Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="8507d-p115">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="8507d-175">Wenn Sie einen externen Kontakt ausblenden möchten, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="8507d-175">To hide a single external contact, run the following command.</span></span>
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    <span data-ttu-id="8507d-176">Beispielsweise Pilar Pinilla aus dem freigegebenen Adressbuch ausblenden möchten, führen Sie diesen Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="8507d-176">For example, to hide Pilar Pinilla from the shared address book, run this command:</span></span>

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. <span data-ttu-id="8507d-177">Wenn Sie alle externe Kontakten aus dem freigegebenen Adressbuch ausblenden möchten, führen Sie diesen Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="8507d-177">To hide all external contacts from the shared address book, run this command:</span></span>

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

<span data-ttu-id="8507d-178">Nachdem Sie diese ausblenden, externe Kontakte werden nicht im freigegebenen Adressbuch angezeigt, jedoch können Sie diese weiterhin als Mitglieder einer Verteilergruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8507d-178">After you hide them, external contacts aren't displayed in the shared address book, but you can still add them as members of a distribution group.</span></span>

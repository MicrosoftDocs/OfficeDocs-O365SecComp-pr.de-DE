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
# <a name="bulk-import-external-contacts-to-exchange-online"></a>BULK Import externe Kontakte zu Exchange Online

**Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von Kontakten in Ihrem Postfach? Finden Sie unter [Importieren von Kontakten in Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Hat Ihr Unternehmen? vielen vorhandenen Geschäftskontakten, die im freigegebenen Adressbuch (auch als "die globalen Adressliste" bezeichnet) enthalten sein sollen in Exchange Online Möchten Sie als Mitglieder von Verteilergruppen, wie Sie mit Benutzern in Ihrem Unternehmen können externe Kontakte hinzufügen? Importieren Sie externe Kontakte in Exchange Online, wenn Ja, Sie Exchange Online PowerShell und einer Datei (durch Kommas getrennte Werte) an Massen verwenden können. Es ist ein dreistufiger Prozess:
  
[Schritt 1: Erstellen einer CSV-Datei, die Informationen über die externe Kontakte enthält.](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Schritt 2: Erstellen von externen Kontakten mit PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Schritt 3: Hinzufügen von Informationen zu den Eigenschaften des externen Kontakten](#step-3-add-information-to-the-properties-of-the-external-contacts)

Nachdem Sie diese Schritte, um Kontakte importieren abgeschlossen haben, können Sie diese zusätzlichen Aufgaben ausführen:
  
- [Mehrere externe Kontakte hinzufügen](bulk-import-external-contacts.md#AddMore)
  
- [Ausblenden von externen Kontakten aus dem freigegebenen Adressbuch](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Schritt 1: Erstellen einer CSV-Datei, die Informationen über die externe Kontakte enthält.

Der erste Schritt besteht eine CSV-Datei erstellen, die Informationen für jeden externen Kontakt enthält, die Sie zu Exchange Online importieren möchten. 
  
1. Kopieren Sie den folgenden Text in eine Textdatei in Microsoft Editor, und speichern sie auf Ihrem Desktop als eine CSV-Datei mithilfe von Filename Suffix CSV; beispielsweise ExternalContacts.csv.
    
    > [!TIP]
    > Wenn Ihre Sprache Sonderzeichen (wie **Å**, **Ä**und **Ö** in Schwedisch) speichern Sie die CSV-Datei mit UTF-8- oder anderen Unicode-Codierung enthält, wenn Sie im Editor die Datei speichern. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Eigenschaften des Kontakte, die beim Importieren zu Exchange Online verwendet werden können. Name der Eigenschaft wird durch ein Komma getrennt. Jede Zeile unter der Überschrift steht der Eigenschaftswerte für den Import von einem externen Kontakt. 
    
    > [!NOTE]
    > Dieser Text enthält Beispieldaten, die Sie löschen können. Aber nicht löschen Sie oder ändern Sie die erste Zeile (Kopfzeile). Sie enthält alle Eigenschaften für die externe Kontakte. 
  
2. Öffnen Sie die CSV-Datei in Microsoft Excel so bearbeiten Sie die CSV-Datei, da es wesentlich einfacher ist zu Excel verwenden, um die CSV-Datei zu bearbeiten.
    
3. Erstellen Sie eine Zeile für jeden Kontakt, den Sie zu Exchange Online importieren möchten. Füllen Sie so viele der Zellen wie möglich. Diese Informationen werden im freigegebenen Adressbuch für jeden Kontakt angezeigt werden. 
    
    > [!IMPORTANT]
    >  Die folgenden Eigenschaften (die in der Kopfzeile der ersten vier Elemente sind) sind erforderlich, um einen externen Kontakt zu erstellen und in der CSV-Datei aufgefüllt werden müssen: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. PowerShell-Befehl, den Sie in Schritt2 ausführen werden die Werte für diese Eigenschaften verwenden, um die Kontakte zu erstellen. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Schritt 2: Erstellen von externen Kontakten mit PowerShell

Im nächsten Schritt wird die CSV-Datei verwenden, die Sie in Schritt 1 erstellt haben, und PowerShell-Skripte zur Bulk Importieren der externe Kontakte, die in der CSV-Datei zu Exchange Online aufgelistet. 
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Achten Sie darauf, dass Sie den Benutzernamen und das Kennwort für Ihr Office 365 globaler Administrator-Konto verwenden, beim Herstellen der Verbindung zu Exchange Online PowerShell. 
    
2. Nachdem Sie zu Exchange Online PowerShell verbunden haben, fahren Sie mit der desktop-Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert; beispielsweise `C:\Users\Administrator\desktop`.
    
3. Führen Sie den folgenden Befehl zum Erstellen von externen Kontakten aus:

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    Es kann eine Weile zum Erstellen der neuen Kontakte, je nachdem, wie viele importierten dauern. Wenn der Befehl abgeschlossen wird ausgeführt, PowerShell zeigt eine Liste der neuen Kontakte, die erstellt wurden. 
    
4. Um die neue externe Kontakte angezeigt, besuchen Sie die Exchange-Verwaltungskonsole (EAC), und klicken Sie dann auf **Empfänger** \> **Kontakte**. 
    
    > [!TIP]
    > Anweisungen für die Verbindung mit der Exchange-Verwaltungskonsole finden Sie unter [Exchange Admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. Klicken Sie auf **Aktualisieren** , falls erforderlich, ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) an, die Liste aktualisieren und die externen Kontakte, die importiert wurden. 
    
    Die importierten Kontakte werden in im freigegebenen Adressbuch in Outlook und Outlook im Web angezeigt.
    
    > [!NOTE]
    > Sie können auch die Kontakte in Office 365 Administrationscenter anzeigen, indem Sie auf **Benutzer** \> **Kontakte**. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Schritt 3: Hinzufügen von Informationen zu den Eigenschaften des externen Kontakten

Nach dem Ausführen des Befehls in Schritt2 externe Kontakte erstellt werden, jedoch können sie die Informationen Kontakts oder der Organisation, die die Informationen aus der Großteil der Zellen in der CSV-Datei ist nicht enthalten. Dies ist, da beim Erstellen neuer externe Kontakte nur die erforderlichen Eigenschaften aufgefüllt werden. Machen Sie sich keine Gedanken Sie, wenn Sie alle Informationen, die in der CSV-Datei gefüllt haben. Wenn es nicht vorhanden ist, werden nicht es hinzugefügt werden.
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Wechseln Sie zum desktop-Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert; beispielsweise `C:\Users\Administrator\desktop`.
    
3. Führen Sie die folgenden zwei Befehle aus, um die anderen Eigenschaften aus der CSV-Datei an die externe Kontakte hinzuzufügen, die Sie in Schritt2 erstellt haben.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > Der Parameter _Manager_ kann problematisch sein. Wenn die Zelle in der CSV-Datei leer ist, erhalten Sie eine Fehlermeldung und keiner der Informationen über die Eigenschaft wird auf den Kontakt hinzugefügt werden. Wenn Sie keinen Manager angeben müssen, klicken Sie dann einfach löschen ` -Manager $_.Manager ` aus dem vorherigen PowerShell-Befehl. 
  
    Erneut, kann es eine Weile so aktualisieren Sie die Kontakte aus, je nachdem, wie viele Sie in Schritt 1 importiert wurden. 
    
4. So überprüfen, dass die Eigenschaften der Kontakte hinzugefügt wurden: 
    
1. Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**.
    
2. Klicken Sie auf einen Kontakt, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) Eigenschaften des Kontakts angezeigt. 
    
Das wars! Benutzer können die Kontakte und Weitere Informationen im Outlook-Adressbuch und Outlook im Web finden Sie unter.
  
## <a name="add-more-external-contacts"></a>Mehrere externe Kontakte hinzufügen

Sie können wiederholen Sie die Schritte 1 bis Schritt 3, um neue externe Kontakte in Exchange Online hinzuzufügen. Sie oder ein Benutzer in Ihrem Unternehmen können einfach eine neue Zeile in der CSV-Datei für den neuen Kontakt hinzufügen. Anschließend können Sie die PowerShell-Befehle ausführen, aus Schritt2 und Schritt 3 zum Erstellen und Hinzufügen von Informationen zu den neuen Kontakten.
  
> [!NOTE]
> Wenn Sie den Befehl zum Erstellen von neuer Kontakten ausführen, erhalten Sie möglicherweise eine Fehlermeldung ausgegeben, dass die Kontakte, die bereits zuvor erstellten vorhanden sind. Jedoch neuer Kontakt hinzufügen möchten die CSV-Datei wird erstellt. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Ausblenden von externen Kontakten aus dem freigegebenen Adressbuch >

In einigen Unternehmen können externe Kontakte, so dass sie als Mitglieder von Verteilergruppen hinzugefügt werden können. In diesem Szenario können sie externe Kontakte aus dem freigegebenen Adressbuch ausblenden möchten. Hier ist wie:
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Wenn Sie einen externen Kontakt ausblenden möchten, führen Sie den folgenden Befehl aus.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Beispielsweise Pilar Pinilla aus dem freigegebenen Adressbuch ausblenden möchten, führen Sie diesen Befehl ein:

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Wenn Sie alle externe Kontakten aus dem freigegebenen Adressbuch ausblenden möchten, führen Sie diesen Befehl aus:

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

Nachdem Sie diese ausblenden, externe Kontakte werden nicht im freigegebenen Adressbuch angezeigt, jedoch können Sie diese weiterhin als Mitglieder einer Verteilergruppe hinzufügen.

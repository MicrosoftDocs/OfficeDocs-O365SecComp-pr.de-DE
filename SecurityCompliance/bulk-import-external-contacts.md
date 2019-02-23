---
title: Massenimport externer Kontakte in Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Erfahren Sie, wie Administratoren Exchange Online PowerShell und eine CSV-Datei verwenden können, um externe Kontakte in die globale Adressliste zu importieren.
ms.openlocfilehash: a38565d5cbff61a954914bf156fb1bac0814c815
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215915"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Massenimport externer Kontakte in Exchange Online

**Dieser Artikel richtet sich an Administratoren. Versuchen Sie, Kontakte in Ihr eigenes Postfach zu importieren? Weitere Informationen finden Sie unter [Importieren von Kontakten in Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Verfügt Ihr Unternehmen über viele vorhandene Geschäftskontakte, die in das freigegebene Adressbuch (auch als globale Adressliste bezeichnet) in Exchange Online eingeschlossen werden sollen? Möchten Sie externe Kontakte als Mitglieder von Verteilergruppen hinzufügen, genau wie mit Benutzern in Ihrem Unternehmen? In diesem Fall können Sie mit Exchange Online PowerShell und einer CSV-Datei (durch trennzeichengetrennte Werte) externe Kontakte in Exchange Online Massenimportieren. Es handelt sich um einen dreistufigen Prozess:
  
[Schritt 1: Erstellen einer CSV-Datei mit Informationen zu den externen Kontakten](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Schritt 2: Erstellen der externen Kontakte mit PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Schritt 3: Hinzufügen von Informationen zu den Eigenschaften der externen Kontakte](#step-3-add-information-to-the-properties-of-the-external-contacts)

Nachdem Sie diese Schritte zum Importieren von Kontakten ausgeführt haben, können Sie diese zusätzlichen Aufgaben ausführen:
  
- [Hinzufügen weiterer externer Kontakte](bulk-import-external-contacts.md#AddMore)
  
- [Ausblenden externer Kontakte aus dem freigegebenen Adressbuch](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Schritt 1: Erstellen einer CSV-Datei mit Informationen zu den externen Kontakten

Im ersten Schritt erstellen Sie eine CSV-Datei mit Informationen zu jedem externen Kontakt, den Sie in Exchange Online importieren möchten. 
  
1. Kopieren Sie den folgenden Text in eine Textdatei im Editor, und speichern Sie ihn als CSV-Datei unter Verwendung eines Datei Suffixes von. CSV auf Ihrem Desktop. Beispiel: ExternalContacts. CSV.
    
    > [!TIP]
    > Wenn Ihre Sprache Sonderzeichen enthält (beispielsweise **å**, **ä**und **ö** in Schwedisch), speichern Sie die CSV-Datei mit UTF-8 oder einer anderen Unicode-Codierung, wenn Sie die Datei im Editor speichern. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    In der ersten Zeile oder Kopfzeile der CSV-Datei sind die Eigenschaften von Kontakten aufgeführt, die beim Importieren in Exchange Online verwendet werden können. Jeder Eigenschaften Name wird durch ein Komma getrennt. Jede Zeile unter der Kopfzeile stellt die Eigenschaftswerte für den Import eines einzelnen externen Kontakts dar. 
    
    > [!NOTE]
    > Dieser Text enthält Beispieldaten, die Sie löschen können. Löschen oder ändern Sie jedoch nicht die erste Zeile (Kopfzeile). Sie enthält alle Eigenschaften für die externen Kontakte. 
  
2. Öffnen Sie die CSV-Datei in Microsoft Excel, um die CSV-Datei zu bearbeiten, da es viel einfacher ist, Excel zum Bearbeiten der CSV-Datei zu verwenden.
    
3. Erstellen Sie eine Zeile für jeden Kontakt, den Sie in Exchange Online importieren möchten. Füllen Sie so viele Zellen wie möglich aus. Diese Informationen werden im freigegebenen Adressbuch für jeden Kontakt angezeigt. 
    
    > [!IMPORTANT]
    >  Die folgenden Eigenschaften (die ersten vier Elemente in der Kopfzeile) sind erforderlich, um einen externen Kontakt zu erstellen und müssen in der CSV-Datei aufgefüllt werden: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. Der PowerShell-Befehl, den Sie in Schritt 2 ausführen, verwendet die Werte für diese Eigenschaften, um die Kontakte zu erstellen. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Schritt 2: Erstellen der externen Kontakte mit PowerShell

Der nächste Schritt besteht darin, die CSV-Datei zu verwenden, die Sie in Schritt 1 und PowerShell erstellt haben, um die in der CSV-Datei aufgeführten externen Kontakte in Exchange Online zu importieren. 
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anleitungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Achten Sie darauf, beim Herstellen einer Verbindung mit Exchange Online PowerShell den Benutzernamen und das Kennwort für das globale Administratorkonto von Office 365 zu verwenden. 
    
2. Nachdem Sie PowerShell mit Exchange Online verbunden haben, wechseln Sie zum Desktop Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert haben. Beispiel `C:\Users\Administrator\desktop`.
    
3. Führen Sie den folgenden Befehl aus, um die externen Kontakte zu erstellen:

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    Es kann eine Weile dauern, bis die neuen Kontakte erstellt werden, je nachdem, wie viele Sie importieren. Wenn der Befehl ausgeführt wird, zeigt PowerShell eine Liste der neuen Kontakte an, die erstellt wurden. 
    
4. Um die neuen externen Kontakte anzuzeigen, wechseln Sie zum Exchange-Verwaltungskonsole (EAC), und klicken Sie dann auf **Empfänger** \> **Kontakte**. 
    
    > [!TIP]
    > Anweisungen zum Herstellen einer Verbindung mit der EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. Klicken Sie **** ![bei Bedarf auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren, um die Liste zu aktualisieren und die importierten externen Kontakte anzuzeigen. 
    
    Die importierten Kontakte werden im freigegebenen Adressbuch in Outlook und Outlook im Web angezeigt.
    
    > [!NOTE]
    > sie können die kontakte im Office 365 admin center auch anzeigen, indem sie zu **benutzer** \> **kontakte**wechseln. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Schritt 3: Hinzufügen von Informationen zu den Eigenschaften der externen Kontakte

Nachdem Sie den Befehl in Schritt 2 ausgeführt haben, werden die externen Kontakte erstellt, Sie enthalten jedoch keine Kontakt-oder Organisationsinformationen, also die Informationen der meisten Zellen in der CSV-Datei. Der Grund ist, dass beim Erstellen neuer externer Kontakte nur die erforderlichen Eigenschaften aufgefüllt werden. Machen Sie sich keine Sorgen, wenn Sie nicht alle Informationen in der CSV-Datei aufgefüllt haben. Wenn er nicht vorhanden ist, wird er nicht hinzugefügt.
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anleitungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Wechseln Sie zum Desktop Ordner, in dem Sie die CSV-Datei in Schritt 1 gespeichert haben. Beispiel `C:\Users\Administrator\desktop`.
    
3. Führen Sie die folgenden beiden Befehle aus, um die anderen Eigenschaften aus der CSV-Datei zu den externen Kontakten hinzuzufügen, die Sie in Schritt 2 erstellt haben.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > Der _Manager-_ Parameter ist möglicherweise problematisch. Wenn die Zelle in der CSV-Datei leer ist, erhalten Sie eine Fehlermeldung, und keine der Eigenschaftsinformationen wird dem Kontakt hinzugefügt. Wenn Sie keinen Manager angeben müssen, löschen ` -Manager $_.Manager ` Sie einfach den vorherigen PowerShell-Befehl. 
  
    Auch hier kann es eine Weile dauern, bis die Kontakte aktualisiert werden, je nachdem, wie viele Sie in Schritt 1 importiert haben. 
    
4. So überprüfen Sie, ob die Eigenschaften den Kontakten hinzugefügt wurden: 
    
1. Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**.
    
2. Klicken Sie auf einen Kontakt, **** ![und klicken Sie](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) dann auf Bearbeitungssymbol bearbeiten, um die Eigenschaften des Kontakts anzuzeigen. 
    
Das wars! Benutzer können die Kontakte und die zusätzlichen Informationen im Adressbuch Outlook und Outlook im Web anzeigen.
  
## <a name="add-more-external-contacts"></a>Hinzufügen weiterer externer Kontakte

Sie können die Schritte 1 bis 3 wiederholen, um in Exchange Online neue externe Kontakte hinzuzufügen. Sie oder Benutzer in Ihrem Unternehmen können einfach eine neue Zeile in der CSV-Datei für den neuen Kontakt hinzufügen. Anschließend können Sie die PowerShell-Befehle aus Schritt 2 und Schritt 3 ausführen, um die neuen Kontakte zu erstellen und Informationen hinzuzufügen.
  
> [!NOTE]
> Wenn Sie den Befehl zum Erstellen neuer Kontakte ausführen, erhalten Sie möglicherweise eine Fehlermeldung, dass die zuvor erstellten Kontakte bereits vorhanden sind. Jeder neue Kontakt, der der CSV-Datei hinzugefügt wird, wird erstellt. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Ausblenden externer Kontakte aus der freigegebenen Adresse book>

Einige Unternehmen verwenden möglicherweise nur externe Kontakte, damit Sie als Mitglieder von Verteilergruppen hinzugefügt werden können. In diesem Szenario möchten Sie möglicherweise externe Kontakte aus dem freigegebenen Adressbuch ausblenden. So geht 's:
  
1.  Verbinden Sie PowerShell mit Ihrer Exchange Online-Organisation. Schrittweise Anleitungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Führen Sie den folgenden Befehl aus, um einen einzelnen externen Kontakt auszublenden.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Um beispielsweise Pilar Pinilla aus dem freigegebenen Adressbuch auszublenden, führen Sie den folgenden Befehl aus:

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Führen Sie den folgenden Befehl aus, um alle externen Kontakte aus dem freigegebenen Adressbuch auszublenden:

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

Nachdem Sie sie ausgeblendet haben, werden externe Kontakte nicht im freigegebenen Adressbuch angezeigt, aber Sie können Sie weiterhin als Mitglieder einer Verteilergruppe hinzufügen.

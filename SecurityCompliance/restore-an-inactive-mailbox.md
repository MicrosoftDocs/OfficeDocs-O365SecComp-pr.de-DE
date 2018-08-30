---
title: Wiederherstellen eines inaktiven Postfachs in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Wenn ein neuer Mitarbeiter oder einem anderen Benutzer Zugriff auf den Inhalt eines inaktiven Postfachs in Office 365 erforderlich ist, können Sie wiederherstellen (den Inhalt des inaktiven Postfachs auf ein vorhandenes Postfach oder Zusammenführen).
ms.openlocfilehash: e0add2b63a48edc27795143324c83153b15dcf8c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528926"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Wiederherstellen eines inaktiven Postfachs in Office 365

Ein inaktives Postfach (eine Art vorläufig gelöschtes Postfach) wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Wenn ein anderer Mitarbeiter die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt oder dieser Mitarbeiter in Ihre Organisation zurückkehrt, gibt es zwei Möglichkeiten, den Inhalt des inaktiven Postfachs wieder für einen Benutzer verfügbar zu machen: 
  
- **Rückspeichern eines inaktiven Postfachs** Wenn ein anderer Mitarbeiter die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt oder ein anderer Benutzer Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in ein vorhandenes Postfach rückspeichern (oder ihn mit diesem zusammenführen). Sie können auch das Archiv aus einem inaktiven Postfach rückspeichern. Nach dem Rückspeichern bleibt das inaktive Postfach als ein solches erhalten. In diesem Thema werden die Verfahren zum Rückspeichern eines inaktiven Postfachs beschrieben. 
    
- **Wiederherstellen ein inaktives Postfachs** Wenn der departed Mitarbeiter für Ihre Organisation zurückgibt, oder wenn ein neuer Mitarbeiter eingestellt wird, die auf die Verantwortlichkeiten des Mitarbeiters departed angewendet werden, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Diese Methode konvertiert inaktive Postfach in ein neues Postfach mit dem Inhalt des inaktiven Postfachs an. Nachdem es wiederhergestellt wird, ist das inaktive Postfach nicht mehr vorhanden. Eine schrittweise Anleitung finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](recover-an-inactive-mailbox.md).
    
Finden Sie **Weitere Informationen** im Abschnitt in diesem Artikel finden Sie weitere Informationen zu den Unterschieden zwischen wiederherstellen und Wiederherstellen eines inaktiven Postfachs an. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Exchange Online PowerShell zum Wiederherstellen eines inaktiven Postfachs verwenden. Sie können nicht im Exchange Administrationscenter (EAC) verwenden. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Führen Sie den folgenden Befehl in Exchange Online PowerShell um Identitätsinformationen für die inaktiver Postfächer in Ihrer Organisation abzurufen. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     Verwenden Sie die von diesem Befehl zurückgegebenen Informationen zum Rückspeichern eines bestimmten inaktiven Postfachs.
    
- Weitere Informationen zu inaktiver Postfächer finden Sie unter [inaktiver Postfächer in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="restore-an-inactive-mailbox"></a>Rückspeichern eines inaktiven Postfachs

Verwenden Sie das Cmdlet **New-MailboxRestoreRequest** mit den Parametern  _SourceMailbox_ und  _TargetMailbox_, um den Inhalt eines inaktiven Postfachs in ein vorhandenes Postfach rückzuspeichern. Weitere Informationen zu diesem Cmdlet finden Sie unter [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).
  
1. Erstellen Sie eine Variable, die die Eigenschaften des inaktiven Postfachs enthält. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGUID** zum Identifizieren des inaktiven Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können. 
  
2. Speichern Sie den Inhalt des inaktiven Postfachs in ein vorhandenes Postfach zurück. Die Inhalte des inaktiven Postfachs (Quellpostfachs) werden in den entsprechenden Ordnern im vorhandenen Postfach (Zielpostfach) zusammengeführt.
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   Alternativ können Sie einen übergeordneten Ordner im Zielpostfach angeben, in den die Inhalte aus dem inaktiven Postfach rückgespeichert werden sollen. Wenn der angegebene Zielordner oder die angegebene Zielordnerstruktur nicht bereits im Zielpostfach vorhanden ist, wird es bzw. sie während des Rückspeichervorgangs erstellt. 
    
    Im folgenden Beispiel werden Postfachelemente und Unterordner aus einem inaktiven Postfach in die übergeordnete Ordnerstruktur des Zielpostfachs in einen Ordner namens "Inactive Mailbox" kopiert.
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a>Rückspeichern des Archivs aus einem inaktiven Postfach

Wenn ein inaktives Postfach ein Archivpostfach enthält, können Sie es auch im Archivpostfach eines vorhandenen Postfachs rückspeichern. Zum Rückspeichern des Archivs aus einem inaktiven Postfach müssen Sie die Schalter  _SourceIsArchive_ und  _TargetIsAchive_ dem Befehl hinzufügen, der zum Rückspeichern eines inaktiven Postfachs verwendet wird. 
  
1. Erstellen Sie eine Variable, die die Eigenschaften des inaktiven Postfachs enthält. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGUID** zum Identifizieren des inaktiven Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können. 
  
2. Speichern Sie den Inhalt des Archivs aus dem inaktiven Postfach (Quellarchiv) in das Archiv eines vorhandenen Postfachs (Zielarchiv) zurück. Im folgenden Beispiel wird der Inhalt aus dem Quellarchiv in einen Ordner namens "Inactive Mailbox" im Archiv des Zielpostfachs kopiert.

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a>Weitere Informationen

- **Was ist der Hauptunterschied zwischen dem Wiederherstellen und dem Rückspeichern eines inaktiven Postfachs?** Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach im Grunde in ein neues Postfach umgewandelt. Der Inhalt und die Ordnerstruktur des inaktiven Postfachs werden beibehalten, und das Postfach wird mit einem neuen Benutzerkonto verknüpft. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Alle Änderungen am Inhalt des neuen Postfachs wirken sich auf den Inhalt aus, der ursprünglich im inaktiven Postfach archiviert wurde. Wenn Sie ein inaktives Postfach hingegen rückspeichern, wird der Inhalt lediglich in ein anderes Postfach kopiert. Das inaktive Postfach bleibt als ein solches erhalten. Änderungen am Inhalt des Zielpostfachs wirken sich nicht auf den ursprünglichen Inhalt des inaktiven Postfachs aus. Das inaktive Postfach kann weiterhin mithilfe der [Inhaltssuche](run-a-content-search-in-the-security-and-compliance-center.md) im Office 365 Security &amp; Compliance Center durchsucht werden. Sein Inhalt kann in ein anderes Postfach rückgespeichert werden, oder es kann zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden. 
    
- **Wie suchen Sie nach inaktiven Postfächern?** Zum Abrufen einer Liste der inaktiven Postfächer in Ihrer Organisation und Anzeigen von Informationen, die für das Rückspeichern eines inaktiven Postfachs nützlich sind, können Sie den folgenden Befehl ausführen. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **Verwenden Sie ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie zum Aufbewahren von Inhalten in inaktiven Postfächern.** Wenn Sie den Status eines inaktiven Postfachs nach dem Rückspeichern beibehalten möchten, können Sie für das Zielpostfach das [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286) aktivieren oder eine [Office 365- Aufbewahrungsrichtlinie](retention-policies.md) anwenden, bevor Sie das inaktive Postfach rückspeichern. Dies verhindert das dauerhafte Löschen von Elementen aus dem inaktiven Postfach, nachdem sie in das Zielpostfach rückgespeichert wurden. 
    
- **Enable Aufbewahrungszeit für das Zielpostfach vor dem Wiederherstellen eines inaktiven Postfachs.** Da Postfachelemente aus eines inaktiven Postfachs alte sein können, sollten Sie das Anhalten der Aufbewahrungszeit für das Zielpostfach aktivieren, vor dem Wiederherstellen eines inaktiven Postfachs. Wenn Sie platzieren ein Postfachs zur Aufbewahrung von halten, die Aufbewahrungsrichtlinie, die ihm zugewiesen wird, bis das Anhalten der Aufbewahrungszeit entfernt wird oder bis die Aufbewahrungszeit Ablauf verarbeitet wird. Dies gibt den Besitzer der Ziel-Postfach Zeit zum Verwalten von ALTER Nachrichten aus dem Postfach inaktiv. Andernfalls kann die Aufbewahrungsrichtlinie alte Elemente löschen (oder Elemente in das Archivpostfach verschieben, sofern sie aktiviert sind), die abgelaufen basierend auf der aufbewahrungseinstellungen für das Zielpostfach konfiguriert. Weitere Informationen finden Sie unter [Place ein Postfach auf Retention hold im Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Welche Funktion hat die Option „AllowLegacyDNMismatch"?** In den vorherigen Beispielen zum Rückspeichern eines inaktiven Postfachs wird die Option **AllowLegacyDNMismatch** verwendet, um das Rückspeichern des inaktiven Postfachs in ein anderes Zielpostfach zu erlauben. Ziel eines typischen Rückspeicherszenarios ist das Rückspeichern von Inhalten, bei denen das Quell- und Zielpostfach identisch sind. Standardmäßig prüft das Cmdlet **New-MailboxRestoreRequest** daher, ob der Wert der Eigenschaft **LegacyExchangeDN** für das Quell- und Zielpostfach identisch ist. Durch diese Prüfung wird vermieden, dass Sie versehentlich ein Quellpostfach im falschen Zielpostfach rückspeichern. Wenn Sie versuchen, ein inaktives Postfach ohne die Option **AllowLegacyDNMismatch** rückzuspeichern, kann es zu einem Fehler kommen, wenn das Quell- und Zielpostfach unterschiedliche Werte für die Eigenschaft **LegacyExchangeDN** aufweisen. 
    
- **Sie können andere Parameter mit dem Cmdlet "New-MailboxRestoreRequest" verwenden, um verschiedene Rückspeicherszenarien für inaktive Postfächer zu implementieren.** Sie können beispielsweise den folgenden Befehl ausführen, um das Archiv aus dem inaktiven Postfach im primären Postfach des Zielpostfachs rückzuspeichern. 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  Mit dem folgenden Befehl können auch das inaktive primäre Postfach im Archiv des Zielpostfachs rückspeichern.

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- **Welche Funktion hat der Parameter "TargetRootFolder"?** Wie bereits erläutert, können Sie den Parameter **TargetRootFolder** verwenden, um einen Ordner in der oberen Ebene der Ordnerstruktur (den Stammordner) im Zielpostfach anzugeben, in den der Inhalt des inaktiven Postfachs rückgespeichert werden soll. Wenn Sie diesen Parameter nicht verwenden, werden Postfachelemente aus dem inaktiven Postfach in den entsprechenden Standardordnern des Zielpostfachs zusammengeführt, und benutzerdefinierte Ordner werden im Stammverzeichnis des Zielpostfachs neu erstellt. Die folgenden Abbildungen veranschaulichen die Unterschiede zwischen Verwendung oder Nichtverwendung des Parameters **TargetRootFolder**. 
    
    **Ordnerhierarchie im Zielpostfach, wenn der Parameter "TargetRootFolder" nicht verwendet wird**
    
    ![Screenshot: Der Parameter „TargetRootFolder' wird nicht verwendet.](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    **Ordnerhierarchie im Zielpostfach, wenn der Parameter "TargetRootFolder" verwendet wird**
    
    ![Screenshot: Der Parameter „TargetRootFolder' wird verwendet.](media/300da592-7323-48db-b8a4-07012259d113.png)

  


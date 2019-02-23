---
title: Wiederherstellen eines inaktiven Postfachs in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: 'Wenn ein ehemaliger Mitarbeiter zu Ihrer Organisation zurückkehrt oder ein neuer Mitarbeiter für die Übernahme der Aufgaben eines abgemeldeten Mitarbeiters eingestellt wird, können Sie den Inhalt des inaktiven Postfachs in Office 365 wiederherstellen. Wenn Sie ein inaktives Postfach wiederherstellen, wird es in ein neues Postfach konvertiert, das den Inhalt des inaktiven Postfachs enthält. '
ms.openlocfilehash: bebcf5cbb569c9e2e591294a084defea15af4c0f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216135"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Wiederherstellen eines inaktiven Postfachs in Office 365

Ein inaktives Postfach (eine Art vorläufig gelöschtes Postfach) wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Wenn ein anderer Mitarbeiter die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt oder dieser Mitarbeiter in Ihre Organisation zurückkehrt, gibt es zwei Möglichkeiten, den Inhalt des inaktiven Postfachs wieder verfügbar zu machen: 
  
- **Wiederherstellen eines inaktiven Postfachs** Wenn der ehemalige Mitarbeiter in Ihre Organisation zurückkehrt oder ein neuer Mitarbeiter eingestellt wird, der die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt, können Sie den Inhalt des inaktiven Postfachs wiederherstellen. Bei dieser Methode wird das inaktive Postfach in ein neues, aktives Postfach mit dem Inhalt des inaktiven Postfachs umgewandelt. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. In diesem Thema werden die Verfahren dieser Methode beschrieben. 
    
- **Wiederherstellen eines** inaktiven Postfachs Wenn ein anderer Mitarbeiter die Aufgaben des ehemaligen Mitarbeiters übernimmt oder ein anderer Benutzer Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in einem vorhandenen Postfach wiederherstellen (oder zusammenführen). Sie können das Archiv auch aus einem inaktiven Postfach wiederherstellen. Die Verfahren für diese Methode finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md).
    
Im Abschnitt [Weitere Informationen](recover-an-inactive-mailbox.md#moreinfo) finden Sie weitere Details zu den Unterschieden zwischen dem Rückspeichern und Wiederherstellen eines inaktiven Postfachs und eine Beschreibung, was passiert, wenn ein inaktives Postfach wiederhergestellt wird.
  
> [!NOTE]
> Wir haben den Stichtag für das Erstellen eines neuen in-situ-Speichers verschoben, um ein Postfach inaktiv zu machen. Aber zu einem späteren Zeitpunkt können Sie keine neuen in-situ-Speicher in Exchange Online erstellen. Zu diesem Zeitpunkt können nur Rechtsstreitigkeiten und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer im in-situ-Speicher werden jedoch weiterhin unterstützt, und Sie können weiterhin die in-situ-Speicher für inaktive Postfächer verwalten. Dazu gehört das Ändern der Dauer eines in-situ-Speichers und das permanente Löschen eines inaktiven Postfachs durch Entfernen des in-situ-Speichers. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Zum Wiederherstellen eines inaktiven Postfachs müssen Sie Exchange Online PowerShell verwenden. Die Exchange-Verwaltungskonsole kann nicht verwendet werden. Schrittweise Anleitungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Führen Sie den folgenden Befehl aus, um die Identitätsinformationen für die inaktiven Postfächer in Ihrer Organisation abzurufen. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    Verwenden Sie die von diesem Befehl zurückgegebenen Informationen, um ein bestimmtes inaktives Postfach wiederherzustellen.
    
- Weitere Informationen zu inaktiven Postfächern finden Sie unter inAktive [Postfächer in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="recover-an-inactive-mailbox"></a>Wiederherstellen eines inaktiven Postfachs

Verwenden Sie das Cmdlet **New-Mailbox** mit dem Parameter *InactiveMailbox* , um ein inaktives Postfach wiederherzustellen. 
  
1. Erstellen Sie eine Variable, die die Eigenschaften des inaktiven Postfachs enthält. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGUID** zum Identifizieren des inaktiven Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können. 
  
2. In diesem Beispiel werden die im vorherigen Befehl abgerufenen Eigenschaften verwendet und das inaktive Postfach für den Benutzer Ann Beebe in ein aktives Postfach wiederhergestellt. Stellen Sie sicher, dass die für die Parameter *Name* und *MicrosoftOnlineServicesID* angegebenen Werte innerhalb Ihrer Organisation eindeutig sind. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    Die primäre SMTP-Adresse für das wiederhergestellte inaktive Postfach hat den gleichen Wert wie der durch den *MICROSOFTONLINESERVICESID* -Parameter. 
    
Nach dem Wiederherstellen eines inaktiven Postfachs wird auch ein neues Office 365-Benutzerkonto erstellt. Sie müssen dieses Benutzerkonto aktivieren, indem Sie eine Lizenz zuweisen. Weitere Informationen zum Zuweisen von Lizenzen im Office 365 Admin Center finden Sie unter [Zuweisen von Lizenzen und Aufheben der Zuweisung von Lizenzen für Office 365 Business](https://go.microsoft.com/fwlink/p/?LinkId=276798).
  
## <a name="more-information"></a>Weitere Informationen

- **Was ist der Hauptunterschied zwischen dem Wiederherstellen und dem Rückspeichern eines inaktiven Postfachs?** Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach im Wesentlichen in ein neues Postfach umgewandelt, wobei Inhalt und Ordnerstruktur des inaktiven Postfachs beibehalten werden und das Postfach mit einem neuen Benutzerkonto verknüpft wird. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Alle Änderungen am Inhalt des neuen Postfachs wirken sich auf den Inhalt aus, der ursprünglich im inaktiven Postfach archiviert wurde. Wenn Sie hingegen ein inaktives Postfach rückspeichern, wird der Inhalt lediglich in ein anderes Postfach kopiert. Das inaktive Postfach bleibt als ein solches erhalten. Änderungen am Inhalt des Zielpostfachs wirken sich nicht auf die ursprünglichen Inhalte des inaktiven Postfachs aus. Das inaktive Postfach kann weiterhin mithilfe der Compliance-eDiscovery durchsucht werden. Sein Inhalt kann in ein anderes Postfach rückgespeichert werden, oder es kann zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden. 
    
- **Was geschieht, wenn Sie ein inaktives Postfach wiederherstellen?** Wenn Sie ein inaktives Postfach wiederherstellen, geschieht Folgendes: 
    
  - Das Beweissicherungsverfahren (sofern für das inaktive Postfach aktiviert ) wird entfernt.
    
  - Compliance-Archive werden entfernt. Dies bedeutet, dass das inaktive Postfach als Quellpostfach aus dem Compliance-Archiv und der Compliance-eDiscovery-Suche entfernt wird. 
    
  - Das inaktive Postfach wird aus allen Office 365-Aufbewahrungsrichtlinien entfernt, die darauf angewendet wurden.
    
  - Der Zeitraum für die Wiederherstellung einzelner Elemente (der von der Postfacheigenschaft **RetainDeletedItemsFor** bestimmt wird) wird auf 30 Tage festgelegt. Wenn in Exchange Online ein neues Postfach erstellt wird, ist dieser Aufbewahrungszeitraum auf 14 Tage festgelegt. Durch Festlegen dieser Eigenschaft auf den Höchstwert von 30 Tagen bleibt Ihnen mehr Zeit zum Wiederherstellen von Daten, die (endgültig) aus dem inaktiven Postfach gelöscht wurden. Sie können die Wiederherstellung einzelner Elemente auch deaktivieren oder den Wiederherstellungszeitraum für einzelne Elemente wieder auf den Standardwert von 14 Tagen zurücksetzen. Weitere Informationen finden Sie unter [Enable or disable single item recovery for a mailbox](https://go.microsoft.com/fwlink/?linkid=856769).
    
  - Das Anhalten der Aufbewahrungszeit ist aktiviert, und der dazugehörige Zeitraum ist auf 30 Tage festgelegt. Dies bedeutet, dass die standardmäßige Exchange-Aufbewahrungsrichtlinie und alle unternehmens- oder Exchange-weiten Office 365-Aufbewahrungsrichtlinien, die dem neuen Postfach zugewiesen sind, 30 Tage lang nicht verarbeitet werden. Dadurch wird dem zurückkehrenden Mitarbeiter oder neuen Besitzer des wiederhergestellten inaktiven Postfachs Zeit zum Verwalten alter Nachrichten eingeräumt. Andernfalls kann die Exchange- oder Office 365-Aufbewahrungsrichtlinie alte Postfachelemente löschen (oder Elemente in das Archivpostfach verschieben, sofern aktiviert), die basierend auf den Aufbewahrungseinstellungen, die für die Exchange- oder Office 365-Aufbewahrungsrichtlinien konfiguriert wurden, abgelaufen sind. Nach 30 Tagen läuft das Anhalten der Aufbewahrungszeit ab. Die Postfacheigenschaft **RetentionHoldEnabled** wird auf **False** festgelegt, und der Assistent für verwaltete Ordner beginnt mit der Verarbeitung der dem Postfach zugewiesenen Richtlinien. Wenn Sie diese zusätzliche Zeit nicht benötigen, können Sie das Anhalten der Aufbewahrungszeit einfach aufheben. Alternativ können Sie die Dauer des Anhaltens der Aufbewahrungszeit erhöhen, indem Sie den Befehl **Set-Mailbox -EndDateForRetentionHold** verwenden. Weitere Informationen finden Sie unter [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Aktivieren Sie das Beweissicherungsverfahren für das wiederhergestellte Postfach, wenn Sie den ursprünglichen Zustand des inaktiven Postfachs bewahren müssen.** Um zu verhindern, dass der neue Besitzer des Postfachs oder die Aufbewahrungsrichtlinie Nachrichten aus dem wiederhergestellten inaktiven Postfach endgültig löscht, können Sie für das Postfach das Beweissicherungsverfahren aktivieren. Weitere Informationen finden Sie unter [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286).
    
- **Welche Benutzer-ID können Sie verwenden, wenn Sie ein inaktives Postfach wiederherstellen?** Wenn Sie ein inaktives Postfach wiederherstellen, kann sich der Wert, den Sie für den *MicrosoftOnlineServicesID* -Parameter angeben, von der ursprünglichen, die dem inaktiven Postfach zugeordnet war, unterscheiden. Sie können auch die ursprüngliche Benutzer-ID verwenden. Wie bereits erwähnt, stellen Sie jedoch sicher, dass die für *Name* und *MicrosoftOnlineServicesID* verwendeten Werte innerhalb Ihrer Organisation eindeutig sind, wenn Sie das inaktive Postfach wiederherstellen. 
    
- **Was geschieht, wenn die Aufbewahrungszeit für das inaktive Postfach nicht abgelaufen ist?** Wenn ein inaktives Postfach vor weniger als 30 Tagen vorläufig gelöscht wurde, kann es nicht mit dem Befehl **New-Mailbox -InactiveMailbox** wiederhergestellt werden. Sie müssen es wiederherstellen, indem Sie das entsprechende Office 365-Benutzerkonto wiederherstellen. Weitere Informationen finden Sie unter [Löschen oder Wiederherstellen von Benutzern](https://go.microsoft.com/fwlink/p/?LinkId=279162).
    
- **Woher weiß ich, ob der Aufbewahrungszeitraum für vorläufig gelöschte Postfächer für ein inaktives Postfach abgelaufen ist?** Führen Sie hierzu den folgenden Befehl aus. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    Wenn die Eigenschaft **ExternalDirectoryObjectId** keinen Wert hat, ist die Aufbewahrungszeit abgelaufen, und Sie können das inaktive Postfach wiederherstellen, indem Sie den Befehl **New-Mailbox -InactiveMailbox** ausführen. Wenn die Eigenschaft **ExternalDirectoryObjectId** einen Wert hat, ist die Aufbewahrungszeit für vorläufig gelöschte Postfächer nicht abgelaufen, und Sie müssen das inaktive Postfach wiederherstellen, indem Sie das Office 365-Benutzerkonto wiederherstellen. Siehe [Löschen oder Wiederherstellen von Benutzern](https://go.microsoft.com/fwlink/p/?LinkId=279162)
    
- **Erwägen Sie, das Archivpostfach nach der Wiederherstellung eines inaktiven Postfachs zu aktivieren.** Dadurch kann der zurückgegebene Benutzer oder neue Mitarbeiter alte Nachrichten in das Archivpostfach verschieben. Wenn die Aufbewahrungsdauer abgelaufen ist, verschiebt die Archivierungsrichtlinie, die Teil der Exchange Online-Postfächern standardmäßigen Exchange-Aufbewahrungsrichtlinie ist, Elemente, die mindestens zwei Jahre alt sind, in das Archivpostfach. Wenn Sie das Archivpostfach nicht aktivieren, verbleiben Elemente, die älter als zwei Jahre sind, im primären Postfach des Benutzers. Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im Office 365 &amp; Security Compliance Center](enable-archive-mailboxes.md).
 
---
title: Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.
ms.openlocfilehash: 70feb265e95741406dbf170c6be70bd83b2ec081
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223524"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online

Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.
  
> [!NOTE]
> Wir haben den Stichtag für die Erstellung neuer in-situ-Speicher in Exchange Online (in Office 365-und Exchange Online-eigenständigen Plänen) verschoben. Sie können jedoch noch in diesem oder Anfang des nächsten Jahres neue in-situ-Speicher in Exchange Online erstellen. Als Alternative zur Verwendung von in-Place-Speicher können Sie [eDiscovery-Fälle](https://go.microsoft.com/fwlink/?linkid=780738) oder [Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?linkid=827811) im Office 365 Security &amp; Compliance Center verwenden. Nach der Außerkraftsetzung neuer in-situ-Speicher können Sie weiterhin vorhandene in-situ-Aufbewahrungen ändern, und das Erstellen neuer in-situ-Speicher in Exchange Server 2013 und Exchange-hybridbereitstellungen wird weiterhin unterstützt. Und Sie können weiterhin Postfächer in einem Rechtsstreit halten. 
  
Möglicherweise haben Sie eine Situation, in der eine Person Ihre Organisation verlassen hat, und ihr entsprechendes Benutzerkonto und Postfach gelöscht wurden. Anschließend erkennen Sie, dass die Informationen im Postfach aufbewahrt werden müssen. Was können Sie tun? Wenn der Aufbewahrungszeitraum für gelöschte Postfächer noch nicht abgelaufen ist, können Sie das gelöschte Postfach (das sogenannte Soft-Deleted Mailbox) in den Speicher einordnen und als inaktives Postfach festlegen. Ein *inaktives Postfach* wird verwendet, um die e-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Die Inhalte eines inaktiven Postfachs werden für die Dauer des in-situ-Speichers aufbewahrt, der bei der Deaktivierung des Postfachs für das gelöscht wurde. Nachdem das Postfach deaktiviert wurde, können Sie das Postfach durchsuchen, indem Sie in-Place eDiscovery in Exchange Online, Inhaltssuche im Office 365 Security &amp; Compliance Center oder im eDiscovery Center in SharePoint Online verwenden. 
  
> [!NOTE]
> In Exchange Online ist ein vorläufig gelöschtes Postfach ein Postfach, das zwar gelöscht wurde, aber innerhalb eines bestimmten Aufbewahrungszeitraums wiederhergestellt werden kann. Dieser Aufbewahrungszeitraum für vorläufig gelöschte Postfächer beträgt in Exchange Online 30 Tage. Das bedeutet, dass das Postfach innerhalb von 30 Tagen nach dem vorläufigen Löschen wiederhergestellt werden kann. Nach 30 Tagen wird ein vorläufig gelöschtes Postfach für das dauerhafte Löschen markiert und kann dann nicht mehr wiederhergestellt oder inaktiviert werden. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen:

- Sie müssen das **New-MailboxSearch** -Cmdlet in Windows PowerShell verwenden, um einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach zu erstellen. Sie können nicht das Exchange-Verwaltungskonsole (EAC) oder das eDiscovery Center in SharePoint Online verwenden. 
    
- Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.
    
- Führen Sie den folgenden Befehl aus, um die Identitätsinformationen zu den vorläufig gelöschten Postfächern in Ihrer Organisation abzurufen. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Weitere Informationen zu inaktiven Postfächern finden Sie unter Übersicht über inaktive [Postfächer in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Erstellen eines In-Situ-Speichers für ein vorläufig gelöschtes Postfach, um daraus ein inaktives Postfach zu machen

Verwenden Sie das **New-MailboxSearch** -Cmdlet, um aus dem vorläufig gelöschten Postfach ein inaktives Postfach zu machen. Weitere Informationen finden Sie unter [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).
  
1. Erstellen Sie eine Variable, die die Eigenschaften des vorläufig gelöschten Postfachs enthält. 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGuid** zum Identifizieren des vorläufig gelöschten Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können. 
  
2. Erstellen Sie einen In-Situ-Speicher und wenden Sie ihn auf das vorläufig gelöschte Postfach an. In diesem Beispiel wird nicht angegeben, wie lange der Speicher aktiv sein soll. Das bedeutet, dass Elemente auf unbestimmte Zeit oder bis der In-Situ-Speicher für das inaktive Postfach entfernt wird, beibehalten werden.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   Beim Erstellen des In-Situ-Speichers können Sie auch eine Aufbewahrungsdauer angeben. In diesem Beispiel werden Elemente im inaktiven Postfach für ca. 7 Jahre aufbewahrt.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. Führen Sie nach ein paar Augenblicken einen der folgenden Befehle aus, um sicherzustellen, dass es sich bei dem vorläufig gelöschten Postfach um ein inaktives Postfach handelt.
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    Oder
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a>Weitere Informationen

Nachdem Sie aus einem vorläufig gelöschten Postfach ein inaktives Postfach gemacht haben, gibt es eine Reihe von Methoden, mit denen Sie das Postfach verwalten können. Weitere Informationen finden Sie unter:
  
- [Ändern der Aufbewahrungsdauer für ein inaktives Postfach](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [Wiederherstellen eines inaktiven Postfachs](recover-an-inactive-mailbox.md)
    
- [Rückspeichern eines inaktiven Postfachs](restore-an-inactive-mailbox.md)
    
- [Löschen eines](delete-an-inactive-mailbox.md) inaktiven Postfachs (durch Entfernen des haltebereichs)

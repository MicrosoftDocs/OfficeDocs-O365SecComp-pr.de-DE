---
title: Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.
ms.openlocfilehash: 226929764fe39b99f526301029d4a41e2fa486cc
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027612"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online

Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.
  
> [!NOTE]
> Wir haben den Stichtag (1. Juli 2017) für das Erstellen neuer In-Situ-Speicher in Exchange Online (in Office 365 und eigenständigen Exchange Online-Plänen) verschoben. Im späteren Verlauf dieses Jahres oder Anfang des nächsten Jahres können Sie keine neuen In-Situ-Speicher mehr in Exchange Online erstellen. Als Alternative zur Verwendung von In-Situ-Speichern können Sie [eDiscovery-Fälle](https://go.microsoft.com/fwlink/?linkid=780738) oder [Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?linkid=827811) im Office 365-Sicherheit &amp; Compliance Center verwenden. Sobald die Erstellung neuer In-Situ-Speicher eingestellt ist, können vorhandene In-Situ-Speicher weiterhin geändert werden, und das Erstellen neuer In-Situ-Speicher in Exchange Server 2013- und Exchange-Hybridbereitstellungen wird weiterhin unterstützt. Und Sie können weiterhin Postfächer im Beweissicherungsverfahren platzieren. 
  
Sie müssen möglicherweise eine Situation, in dem eine Person hat Ihre Organisation verlassen, und ihre entsprechendes Benutzerkonto und Postfach gelöscht wurden. Anschließend stellen Sie fest, dass die Informationen in das Postfach, das beibehalten werden soll. Was können Sie tun? Wenn die Aufbewahrungszeit für gelöschte Postfächer abgelaufen ist, können Sie auf das gelöschte Postfach (mit der Bezeichnung eines vorläufig gelöschten Postfachs) halten an In-Place Hold und ein inaktives Postfachs erleichtern. Ein *inaktives Postfach* wird verwendet, um einem früheren Mitarbeiter e-Mail beibehalten, nachdem er in Ihrer Organisation verlassen hat. Der Inhalt eines inaktiven Postfachs wird beibehalten, für die Dauer der In-Place Hold, die für das vorläufig gelöschte Postfach gesetzt wird, wenn sie als inaktiv festgelegt wurde. Nach das Postfach inaktive erfolgt, suchen Sie das Postfach mithilfe von Compliance-eDiscovery in Exchange Online, Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center oder das eDiscovery Center in SharePoint Online. 
  
> [!NOTE]
> In Exchange Online ist ein vorläufig gelöschtes Postfach ein Postfach, das zwar gelöscht wurde, aber innerhalb eines bestimmten Aufbewahrungszeitraums wiederhergestellt werden kann. Dieser Aufbewahrungszeitraum für vorläufig gelöschte Postfächer beträgt in Exchange Online 30 Tage. Das bedeutet, dass das Postfach innerhalb von 30 Tagen nach dem vorläufigen Löschen wiederhergestellt werden kann. Nach 30 Tagen wird ein vorläufig gelöschtes Postfach für das dauerhafte Löschen markiert und kann dann nicht mehr wiederhergestellt oder inaktiviert werden. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen
<a name="sectionSection0"> </a>

- Sie müssen das **New-MailboxSearch** -Cmdlet in Windows PowerShell verwenden, um einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach zu erstellen. Sie können nicht das Exchange-Verwaltungskonsole (EAC) oder das eDiscovery Center in SharePoint Online verwenden. 
    
- Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.
    
- Führen Sie den folgenden Befehl aus, um die Identitätsinformationen zu den vorläufig gelöschten Postfächern in Ihrer Organisation abzurufen. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Weitere Informationen zu inaktiven Postfächern finden Sie unter [Inaktive Postfächer in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Erstellen eines In-Situ-Speichers für ein vorläufig gelöschtes Postfach, um daraus ein inaktives Postfach zu machen
<a name="sectionSection1"> </a>

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
<a name="sectionSection2"> </a>

Nachdem Sie aus einem vorläufig gelöschten Postfach ein inaktives Postfach gemacht haben, gibt es eine Reihe von Methoden, mit denen Sie das Postfach verwalten können. Weitere Informationen finden Sie unter:
  
- [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Exchange Online](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [Wiederherstellen eines inaktiven Postfachs in Exchange Online](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [Rückspeichern eines inaktiven Postfachs in Exchange Online](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [Aufheben der Aufbewahrung für ein inaktives Postfach in Exchange Online](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    


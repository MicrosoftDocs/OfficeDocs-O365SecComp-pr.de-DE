---
title: Verwalten von E-Mail-Benutzern in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP).
ms.openlocfilehash: b0093c64a0fcb5997b474e7bd491c0915164b77e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341026"
---
# <a name="manage-mail-users-in-eop"></a>Verwalten von E-Mail-Benutzern in EOP

Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP). Es gibt mehrere Möglichkeiten zur Verwaltung von Benutzern in EOP.
  
- Verwenden der Verzeichnissynchronisierung zum Verwalten von e-Mail-Benutzern: Wenn Ihr Unternehmen über vorhandene Benutzerkonten in einer lokalen Active Directory-Umgebung verfügt, können Sie diese Konten mit Azure Active Directory (AD) synchronisieren, wobei eine Kopie der Konten in der Cloud gespeichert wird. Wenn Sie Ihre vorhandenen Benutzerkonten mit Azure Active Directory synchronisieren, können Sie diese Benutzer im Bereich **Empfänger** der Exchange-Verwaltungskonsole anzeigen. Die Verwendung der Verzeichnissynchronisierung wird empfohlen. 
    
- Verwalten von E-Mail-Benutzern über die Exchange Admin Center: Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center. Dies ist der einfachste Weg, E-Mail-Benutzer hinzuzufügen, und hilfreich, um jeweils einen Benutzer hinzuzufügen.
    
- Verwalten von E-Mail-Benutzern mithilfe der Windows Remote-PowerShell: Hinzufügen und Verwalten von E-Mail-Benutzern durch die Ausführung der Windows Remote-PowerShell. Diese Methode ist hilfreich, um mehrere Datensätze hinzuzufügen und Skripts zu erstellen.
    
> [!NOTE]
> Sie können Benutzer im Office 365 Admin Center hinzufügen. Diese Benutzer können allerdings nicht als E-Mail-Empfänger verwendet werden. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Für die Verfahren in diesem Thema sind bestimmte Berechtigungen erforderlich. Informationen zu den Berechtigungen finden Sie in den einzelnen Verfahren.
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung

In diesem Abschnitt finden Sie weitere Informationen zum Verwalten von E-Mail-Benutzern mithilfe von Verzeichnissynchronisierung.
  
> [!IMPORTANT]
> Wenn Sie Verzeichnissynchronisierung zur Verwaltung der Empfänger verwenden, können Sie Benutzer dennoch im Office 365 Admin Center hinzufügen und verwalten. Sie werden dann jedoch nicht mit dem lokalen Active Directory synchronisiert. Dies liegt daran, dass bei der Verzeichnissynchronisierung nur Empfänger aus dem lokalen Active Directory mit der Cloud synchronisiert werden. 
  
> [!TIP]
>  Die Verwendung der Verzeichnissynchronisierung wird für die Verwendung mit den folgenden Features empfohlen: > **Outlook-Listen sicherer Absender und blockierter Absender** -Wenn Sie mit dem Dienst synchronisiert werden, haben diese Listen Vorrang vor der Spamfilterung im Dienst. Dadurch können Benutzer ihre eigenen Listen für sichere Absender und blockierte Absender auf Benutzer-oder Domänenebene verwalten. > **Directory based Edge Blocking (Blockierung)** – Weitere Informationen zu Blockierung finden Sie unter [Use Directory based Edge Blocking to Reject Messages Sent to invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). >- **Spamquarantäne** für Endbenutzer – für den Zugriff auf die Spamquarantäne für Endbenutzer müssen Endbenutzer eine gültige Office 365-Benutzer-ID und ein Kennwort besitzen. EOP-Kunden, die lokale Postfächer schützen, müssen gültige e-Mail-Benutzer sein. >- **Nachrichtenfluss Regeln** : Wenn Sie die Verzeichnissynchronisierung verwenden, werden Ihre vorhandenen Active Directory-Benutzer und-Gruppen automatisch in die Cloud hochgeladen, und Sie können dann Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) erstellen, die bestimmte Benutzer und/ oder Gruppen, ohne Sie manuell über das EAC oder die Exchange Online Protection PowerShell hinzufügen zu müssen. Beachten Sie, dass [dynamische Verteilergruppen](https://go.microsoft.com/fwlink/?LinkId=507569) nicht über die Verzeichnissynchronisierung synchronisiert werden können. 
  
 **Bevor Sie beginnen**
  
Rufen Sie die erforderlichen Berechtigungen ab, und bereiten Sie die Verzeichnissynchronisierung vor, wie unter [Vorbereiten der Verzeichnissynchronisierung](https://go.microsoft.com/fwlink/p/?LinkId=308908) beschrieben.
  
### <a name="to-synchronize-user-directories"></a>So synchronisieren Sie Benutzerverzeichnisse

1. Aktivieren Sie die Verzeichnissynchronisierung, wie unter [Aktivieren der Verzeichnissynchronisierung](https://go.microsoft.com/fwlink/p/?LinkId=308909) beschrieben.
    
2. Richten Sie den Computer für die Verzeichnissynchronisierung ein, wie unter [Einrichten des Computers für die Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/p/?LinkId=308911) beschrieben.
    
3. Synchronisieren Sie die Verzeichnisse, wie unter [Synchronisieren der Verzeichnisse mithilfe des Konfigurations-Assistenten](http://go.microsoft.com/fwlink/?LinkId=308912) beschrieben.
    
    > [!IMPORTANT]
    > Wenn Sie den Konfigurationsassistent für Azure Active Directory-Synchronisierungstool abschließen, wird in Ihrer Active Directory-Gesamtstruktur das Konto **MSOL_AD_SYNC** erstellt. Dieses Konto wird zum Lesen und Synchronisieren der lokalen Active Directory-Informationen verwendet. Damit die Verzeichnissynchronisierung ordnungsgemäß ausgeführt wird, müssen Sie sicherstellen, dass TCP 443 auf dem lokalen Verzeichnissynchronisierungsserver geöffnet ist. 
  
4. Aktivieren Sie die synchronisierten Benutzer, wie unter [Aktivieren synchronisierter Benutzer](http://go.microsoft.com/fwlink/p/?LinkId=308913) beschrieben.
    
5. Verwalten Sie die Verzeichnissynchronisierung, wie unter [Verwalten der Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/p/?LinkId=308915) beschrieben.
    
6. Überprüfen Sie, ob EOP korrekt synchronisiert. Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**, und vergewissern Sie sich, dass die Liste der Benutzer in Ihrer lokalen Umgebung korrekt synchronisiert wird. 
    
## <a name="use-the-eac-to-manage-mail-users"></a>Verwalten von E-Mail-Benutzern über die Exchange Admin Center

In diesem Abschnitt finden Sie Informationen über das Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center.
  
 **Bevor Sie beginnen**
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).
  
### <a name="to-add-a-mail-user-in-the-eac"></a>So fügen Sie einen E-Mail-Benutzer in EAC hinzu

1. Erstellen Sie einen E-Mail-Benutzer, indem Sie in der Verwaltungskonsole **Empfänger** \> **Kontakte** aufrufen und dann auf **Neu +** klicken.
    
2. Geben Sie auf der Seite **Neuer E-Mail-Benutzer** die folgenden Benutzerinformationen ein: 
    
   ****

|**E-Mail-Benutzereigenschaft**|**Beschreibung**|
|:-----|:-----|
|**Vorname**, **Initialen**, **Nachname** <br/> |Geben Sie den vollständigen Benutzernamen in die entsprechenden Felder ein.  <br/> |
|**Anzeigename** <br/> |Geben Sie einen Namen mit bis zu 64 Zeichen ein. Dieses Feld wird automatisch mit den Namen aufgefüllt, die Sie in den Feldern **Vorname**, **Initialen** und **Nachname** eingegeben haben. Der Anzeigename ist erforderlich.  <br/> |
|**Alias** <br/> |Geben Sie einen eindeutigen Alias mit bis zu 64 Zeichen für den Benutzer ein. Der Aliasname ist erforderlich.  <br/> |
|**Externe E-Mail-Adresse** <br/> |Geben Sie die externe E-Mail-Adresse des Benutzers ein.  <br/> |
|**Benutzer-ID** <br/> |Geben Sie den Namen ein, den der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Der Anmeldename des Benutzers setzt sich aus einem Benutzernamen auf der linken Seite des at-Zeichens (@) und einem Suffix auf der rechten Seite zusammen. Normalerweise ist das Suffix der Name der Domäne, in der sich das Benutzerkonto befindet.  <br/> |
|**Neues Kennwort** <br/> |Geben Sie das Kennwort ein, das der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Stellen Sie sicher, dass das angegebene Kennwort den Anforderungen hinsichtlich Länge, Komplexität und Verlauf der Domäne entspricht, in der Sie das Benutzerkonto erstellen.  <br/> |
|**Kennwort bestätigen** <br/> |Geben Sie das Kennwort zur Bestätigung erneut ein.  <br/> |
   
3. Klicken Sie auf **Speichern**, um den neuen E-Mail-Benutzer zu erstellen. Der neue Benutzer sollte in der Benutzerliste angezeigt werden. 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a>So bearbeiten oder entfernen Sie einen E-Mail-Benutzer in EAC

- Wechseln Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Kontakte**. Klicken Sie in der Liste der Benutzer auf den Benutzer, den Sie anzeigen oder ändern möchten, und wählen **** ![Sie dann Bearbeitungs](../media/ITPro-EAC-EditIcon.gif) Symbol bearbeiten aus, um die Benutzereinstellungen nach Bedarf zu aktualisieren. Sie können den Namen, den Alias oder die Kontaktinformationen des Benutzers ändern und detaillierte Informationen zur Rolle des Benutzers in der Organisation aufzeichnen. Sie können auch einen Benutzer auswählen und dann **Remove**![Remove Icon](../media/ITPro-EAC-RemoveIcon.gif) wählen, um es zu löschen. 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a>Verwalten von E-Mail-Benutzern mithilfe der Windows Remote-PowerShell

In diesem Abschnitt finden Sie Informationen dazu, wie Sie E-Mail-Benutzer mithilfe der Windows Remote-PowerShell hinzufügen und verwalten.
  
 **Bevor Sie beginnen**
  
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).
    
- Beachten Sie, dass beim Erstellen von E-Mail-Benutzer mithilfe von Remote-PowerShell-Cmdlets eine Drosselung auftreten kann.
    
- Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.
    
- Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online Protection mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).
    
 **So fügen Sie einen E-Mail-Benutzer mithilfe von Remote-PowerShell hinzu**
  
In diesem Beispiel wird anhand des [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx)-Cmdlets für Jeffrey Zeng ein E-Mail-aktiviertes Benutzerkonto mit den folgenden Angaben erstellt: 
  
- Der Vorname ist "Jeffrey" und der Nachname ist "Zeng".
    
- Der Name ist "Jeffrey", und der Anzeigename ist "Jeffrey Zeng".
    
- Der Alias ist "jeffreyz".
    
- Die externe E-Mail-Adresse ist "jzeng@tailspintoys.com".
    
- Der Office 365-Anmeldename ist "jeffreyz@contoso.onmicrosoft.com".
    
- Das Kennwort lautet "Pa$$word1".
    
```
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 **So stellen Sie sicher, dass es funktioniert hat**
  
Führen Sie wie folgt das [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx)-Cmdlet aus, um Informationen zu dem neuen E-Mail-Benutzer Jeffrey Zeng anzuzeigen: 
  
```
Get-User "Jeffrey Zeng"

```

 **So bearbeiten Sie die Eigenschaften eines E-Mail-Benutzers mithilfe von Remote-PowerShell**
  
Verwenden Sie die Cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) und [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx), um Eigenschaften für E-Mail-Benutzer anzuzeigen oder zu ändern. 
  
In diesem Beispiel wird die externe E-Mail-Adresse für Pilar Pinella festgelegt.
  
```
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

In diesem Beispiel wird die Eigenschaft "Company" für alle E-Mail-Benutzer in "Contoso" geändert.
  
```
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 **So stellen Sie sicher, dass es funktioniert hat**
  
Verwenden Sie im vorherigen Beispiel, in dem wir die Eigenschaften für den E-Mail-Benutzer Pilar Pinella geändert haben, das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet, um die Änderungen zu überprüfen. (Beachten Sie, dass Sie für mehrere E-Mail-Kontakte mehrere Eigenschaften anzeigen können.) 
  
```
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

Führen Sie für das vorherige Beispiel, in dem die Eigenschaft "Company" für alle E-Mail-Benutzer auf "Contoso" festgelegt wurde, den folgenden Befehl aus, um die Änderungen zu überprüfen:
  
```
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind. 
  
 **So entfernen einen E-Mail-Benutzer mithilfe von Remote-PowerShell**
  
In diesem Beispiel wird das [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx)-Cmdlet verwendet, um den Benutzer Jeffrey Zeng zu löschen: 
  
```
Remove-EOPMailUser -Identity Jeffrey
```

 **So stellen Sie sicher, dass es funktioniert hat**
  
Führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus. Es sollte eine Fehlermeldung angezeigt werden, da der Benutzer nicht mehr existiert. 
  
```
Get-Recipient Jeffrey | fl
```



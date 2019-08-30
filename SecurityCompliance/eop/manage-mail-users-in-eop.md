---
title: Verwalten von E-Mail-Benutzern in EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP).
ms.openlocfilehash: 48d530be17a7e75f6e179a50067b1b9526606cb0
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676715"
---
# <a name="manage-mail-users-in-eop"></a>Verwalten von E-Mail-Benutzern in EOP

Die Definition von E-Mail-Benutzern ist ein wichtiger Teil des Verwaltung des Exchange Online Protection-Diensts (EOP). Es gibt mehrere Möglichkeiten zur Verwaltung von Benutzern in EOP.
  
- Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung: Falls Ihr Unternehmen über vorhandene Benutzerkonten in einer lokalen Active Directory-Umgebung verfügt, können Sie diese Konten mit Azure Active Directory (AD) synchronisieren, wo eine Kopie der Konten in der Cloud gespeichert wird. Beim Synchronisieren vorhandener Benutzerkonten mit Azure Active Directory können Sie diese Benutzer im Bereich **Empfänger** von Exchange Admin Center (EAC) anzeigen. Es wird empfohlen, Verzeichnissynchronisierung zu verwenden. 

- Verwalten von E-Mail-Benutzern über die Exchange Admin Center: Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center. Dies ist der einfachste Weg, E-Mail-Benutzer hinzuzufügen, und hilfreich, um jeweils einen Benutzer hinzuzufügen.

- Verwalten von E-Mail-Benutzern mithilfe der Windows Remote-PowerShell: Hinzufügen und Verwalten von E-Mail-Benutzern durch die Ausführung der Windows Remote-PowerShell. Diese Methode ist hilfreich, um mehrere Datensätze hinzuzufügen und Skripts zu erstellen.

> [!NOTE]
> Sie können Benutzer im Microsoft 365 Admin Center hinzufügen, jedoch können diese Benutzer nicht als e-Mail-Empfänger verwendet werden.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Informationen zum Öffnen des Exchange Admin Center finden Sie unter [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).

- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md).

- Beachten Sie, dass beim Erstellen von e-Mail-Benutzern mithilfe von Exchange Online Protection PowerShell-Cmdlets möglicherweise Einschränkungen auftreten.

- In den PowerShell-Befehlen in diesem Thema wird eine Batch Verarbeitungsmethode verwendet, die zu einer Ausbreitungs Verzögerung von ein paar Minuten führt, bevor die Ergebnisse der Befehle angezeigt werden.

- Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, können Sie unter [Verbinden mit PowerShell in Exchange Online Protection](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx) nachlesen.

- Informationen zu Tastenkombinationen, die möglicherweise für die Verfahren in diesem Thema gelten, finden Sie unter [Tastenkombinationen für das Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).

> [!TIP]
> Liegt ein Problem vor? Fragen Sie im Forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) nach Hilfe.
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung

In diesem Abschnitt finden Sie weitere Informationen zum Verwalten von E-Mail-Benutzern mithilfe von Verzeichnissynchronisierung.
  
> [!NOTE]
> Wenn Sie die Verzeichnissynchronisierung zum Verwalten Ihrer Empfänger verwenden, können Sie dennoch Benutzer im Microsoft 365 Admin Center hinzufügen und verwalten, Sie werden jedoch nicht mit Ihrer lokalen Active Directory synchronisiert. Dies liegt daran, dass die Verzeichnissynchronisierung nur Empfänger von Ihrem lokalen Active Directory zur Cloud synchronisiert. <br/><br/> Die Verzeichnissynchronisierung wird für die Verwendung mit den folgenden Features empfohlen: <br/><br/>• **Listen sicherer Absender und blockierter Absender in Outlook**: Wenn Sie mit dem Dienst synchronisiert werden, haben diese Listen Vorrang vor der Spamfilterung im Dienst. Dadurch können Benutzer ihre eigene Liste sicherer und blockierter Absender auf Benutzer- oder Domänenbasis verwalten. <br/><br/>• **Verzeichnisbasierte Edge-Blockierung (Blockierung)**: Weitere Informationen zu Blockierung finden Sie unter [Verwenden der verzeichnisbasierten Edge-Blockierung zum ablehnen von Nachrichten, die an ungültige Empfänger gesendet](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)werden. <br/><br/>• **Spamquarantäne**für Endbenutzer: um auf die Spamquarantäne von Endbenutzern zugreifen zu können, benötigen Endbenutzer eine gültige Office 365 Benutzer-ID und ein Kennwort. EOP-Kunden, die lokale Postfächer schützen, müssen gültige E-Mail-Benutzer sein. <br/><br/>• **Nachrichtenfluss Regeln**: Wenn Sie die Verzeichnissynchronisierung verwenden, werden Ihre vorhandenen Active Directory Benutzer und Gruppen automatisch in die Cloud hochgeladen, und Sie können dann Nachrichtenfluss Regeln (auch bekannt als Transportregeln) erstellen, die auf bestimmte Benutzer und/oder Gruppen ohne manuelles Hinzufügen über die Exchange-Verwaltungskonsole oder Exchange Online Protection PowerShell. Bitte beachten Sie, dass [dynamische Verteilungsgruppen](https://go.microsoft.com/fwlink/?LinkId=507569) nicht über die Verzeichnissynchronisierung synchronisiert werden können.
  
Rufen Sie die erforderlichen Berechtigungen ab, und bereiten Sie die Verzeichnissynchronisierung vor, wie unter [Vorbereiten der Verzeichnissynchronisierung](https://go.microsoft.com/fwlink/p/?LinkId=308908) beschrieben.
  
### <a name="to-synchronize-user-directories-with-azure-active-directory-connect-aad-connect"></a>So synchronisieren Sie Benutzerverzeichnisse mit Azure Active Directory Connect (AAD Connect)

Um Benutzer mit Azure Active Directory (AAD) zu synchronisieren, müssen Sie zunächst die **Verzeichnissynchronisierung aktivieren**, wie unter [Activate Directory Synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909)beschrieben.

Im nächsten Schritt wird die Installation und Konfiguration eines lokalen Computers ausgeführt, um Aad Connect auszuführen (falls Sie noch nicht über einen verfügen – was sich vor der Zeit lohnt). Bei der [Einrichtung von Aad Connect, dem Thema Express Way,](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) erfahren Sie, wie Sie Ihre Konten lokal und Azure AD mit Aad Connect einrichten und synchronisieren.

Bevor Sie diese Aufgabe ausführen, stellen Sie sicher, dass [Sie die Voraussetzungen erfüllen](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites), und wählen Sie [den Installationstyp aus](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation). Der frühere Link ist zu einem kurzen Artikel für Express-Installationen. Sie können auch Artikel zu [benutzerdefinierten Installationen](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)oder zur [Pass-Through-Authentifizierung](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) finden, wenn Sie benötigt werden.

> [!IMPORTANT]
> Wenn Sie den Konfigurationsassistent für Azure Active Directory-Synchronisierungstool abschließen, wird in Ihrer Active Directory-Gesamtstruktur das Konto **MSOL_AD_SYNC** erstellt. Dieses Konto wird zum Lesen und Synchronisieren der lokalen Active Directory-Informationen verwendet. Damit die Verzeichnissynchronisierung ordnungsgemäß ausgeführt wird, müssen Sie sicherstellen, dass TCP 443 auf dem lokalen Verzeichnissynchronisierungsserver geöffnet ist.

Vergewissern Sie sich nach dem Konfigurieren der Synchronisierung, dass EoP ordnungsgemäß synchronisiert wird. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Kontakte**, und vergewissern Sie sich, dass die Liste der Benutzer in Ihrer lokalen Umgebung korrekt synchronisiert wird.

## <a name="use-the-eac-to-manage-mail-users"></a>Verwalten von E-Mail-Benutzern über die Exchange Admin Center

In diesem Abschnitt finden Sie Informationen über das Hinzufügen und Verwalten von E-Mail-Benutzern direkt in der Exchange Admin Center.
  
### <a name="use-the-eac-to-add-a-mail-user"></a>Hinzufügen eines e-Mail-Benutzers mithilfe der Exchange-Verwaltungskonsole

1. Erstellen Sie einen E-Mail-Benutzer, indem Sie in der Verwaltungskonsole **Empfänger** \> **Kontakte** aufrufen und dann auf **Neu +** klicken.

2. Geben Sie auf der Seite **Neuer E-Mail-Benutzer** die folgenden Benutzerinformationen ein: 

   ****

   |**E-Mail-Benutzereigenschaft**|**Beschreibung**|
   |:-----|:-----|
   |**Vorname**, **Initialen**, **Nachname**|Geben Sie den vollständigen Benutzernamen in die entsprechenden Felder ein.|
   |**Anzeigename**|Geben Sie einen Namen mit bis zu 64 Zeichen ein. Dieses Feld wird automatisch mit den Namen aufgefüllt, die Sie in den Feldern **Vorname**, **Initialen** und **Nachname** eingegeben haben. Der Anzeigename ist erforderlich.  |
   |**Alias**|Geben Sie einen eindeutigen Alias mit bis zu 64 Zeichen für den Benutzer ein. Der Aliasname ist erforderlich.|
   |**Externe E-Mail-Adresse**|Geben Sie die externe E-Mail-Adresse des Benutzers ein.|
   |**Benutzer-ID**|Geben Sie den Namen ein, den der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Der Anmeldename des Benutzers setzt sich aus einem Benutzernamen auf der linken Seite des at-Zeichens (@) und einem Suffix auf der rechten Seite zusammen. Normalerweise ist das Suffix der Name der Domäne, in der sich das Benutzerkonto befindet.|
   |**Neues Kennwort**|Geben Sie das Kennwort ein, das der E-Mail-Benutzer verwenden soll, um sich beim Dienst anzumelden. Stellen Sie sicher, dass das angegebene Kennwort den Anforderungen hinsichtlich Länge, Komplexität und Verlauf der Domäne entspricht, in der Sie das Benutzerkonto erstellen.|
   |**Kennwort bestätigen**|Geben Sie das Kennwort zur Bestätigung erneut ein.|

3. Klicken Sie auf **Speichern**, um den neuen E-Mail-Benutzer zu erstellen. Der neue Benutzer sollte in der Benutzerliste angezeigt werden.

### <a name="use-the-eac-to-edit-or-remove-a-mail-user"></a>Bearbeiten oder Entfernen eines e-Mail-Benutzers mithilfe der Exchange-Verwaltungskonsole

- Navigieren Sie in der Exchange Admin Center zu **Empfänger** \> **Kontakte**. Klicken Sie in der Liste der Benutzer auf den Benutzer, den Sie anzeigen oder ändern möchten, und wählen **** ![Sie dann Bearbeitungs](../media/ITPro-EAC-EditIcon.gif) Symbol bearbeiten aus, um die Benutzereinstellungen nach Bedarf zu aktualisieren. Sie können den Benutzernamen, Aliasnamen oder die Kontaktinformationen ändern, und Sie können ausführliche Informationen zur Benutzerrolle in der Organisation eingeben. Sie können auch einen Benutzer auswählen und dann Remove **** ![-Symbol](../media/ITPro-EAC-RemoveIcon.gif) entfernen auswählen, um es zu löschen. 

## <a name="use-exchange-online-protection-powershell-to-manage-mail-users"></a>Verwenden von Exchange Online Protection PowerShell zum Verwalten von e-Mail-Benutzern

In diesem Abschnitt finden Sie Informationen dazu, wie Sie E-Mail-Benutzer mithilfe der Windows Remote-PowerShell hinzufügen und verwalten.
  
### <a name="use-eop-powershell-to-add-a-mail-user"></a>Verwenden von EoP PowerShell zum Hinzufügen eines e-Mail-Benutzers
  
In diesem Beispiel wird anhand des [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser)-Cmdlets für Jeffrey Zeng ein E-Mail-aktiviertes Benutzerkonto mit den folgenden Angaben erstellt:
  
- Der Vorname ist "Jeffrey" und der Nachname ist "Zeng".

- Der Name ist "Jeffrey", und der Anzeigename ist "Jeffrey Zeng".

- Der Alias ist "jeffreyz".

- Die externe E-Mail-Adresse ist "jzeng@tailspintoys.com".

- Der Office 365-Anmeldename ist "jeffreyz@contoso.onmicrosoft.com".

- Das Kennwort lautet "Pa$$word1".

```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

Um zu überprüfen, ob dies funktioniert hat, führen Sie den folgenden Befehl aus, um Informationen über den neuen e-Mail-Benutzer Jeffrey Zeng anzuzeigen:
  
```Powershell
Get-User -Identity "Jeffrey Zeng"
```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user).

### <a name="use-eop-powershell-to-edit-the-properties-of-a-mail-user"></a>Verwenden von EoP PowerShell zum Bearbeiten der Eigenschaften eines e-Mail-Benutzers
  
Verwenden Sie die Cmdlets [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) und [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser), um Eigenschaften für E-Mail-Benutzer anzuzeigen oder zu ändern.
  
In diesem Beispiel wird die externe E-Mail-Adresse für Pilar Pinella festgelegt.
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

In diesem Beispiel wird die Eigenschaft "Company" für alle E-Mail-Benutzer in "Contoso" geändert.
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```
  
Um zu überprüfen, ob dies funktioniert hat, verwenden Sie das [Get-Recipient-](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) Cmdlet, um die Änderungen zu überprüfen. (Beachten Sie, dass Sie für mehrere E-Mail-Kontakte mehrere Eigenschaften anzeigen können.)
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List
```

Führen Sie für das vorherige Beispiel, in dem die Eigenschaft "Company" für alle E-Mail-Benutzer auf "Contoso" festgelegt wurde, den folgenden Befehl aus, um die Änderungen zu überprüfen:
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.
  
### <a name="use-eop-powershell-to-remove-a-mail-user"></a>Verwenden von EoP PowerShell zum Entfernen eines e-Mail-Benutzers
  
In diesem Beispiel wird das [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser)-Cmdlet verwendet, um den Benutzer Jeffrey Zeng zu löschen:
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 **So stellen Sie sicher, dass es funktioniert hat**
  
Führen Sie das Cmdlet [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) aus, um zu überprüfen, ob der e-Mail-Benutzer nicht mehr vorhanden ist.
  
```Powershell
Get-Recipient Jeffrey | Format-List
```

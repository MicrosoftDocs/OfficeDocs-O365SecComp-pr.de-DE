---
title: Gewähren von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Benutzern müssen Berechtigungen im Office 365 Security &amp; Compliance Center zugewiesen werden, bevor Sie Ihre Sicherheits-oder Compliance-Funktionen verwalten können.
ms.openlocfilehash: 0a3f0d1ddde7d269a0f8f9596c5c3de14e94429d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216305"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Gewähren von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center

Benutzern müssen Berechtigungen im Office 365 Security &amp; Compliance Center zugewiesen werden, bevor Sie Ihre Sicherheits-oder Compliance-Funktionen verwalten können. Als globaler Office 365-Administrator oder Mitglied der Rollengruppe Rolle OrganizationManagement anzuzeigen im Security &amp; Compliance Center können Sie diese Berechtigungen Benutzern erteilen. Benutzer können nur die Sicherheits-oder Compliance-Funktionen verwalten, auf die Sie Zugriff haben. 
  
Weitere Informationen zu den verschiedenen Berechtigungen, die Sie Benutzern im Security &amp; Compliance Center erteilen können, finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Um die Schritte in diesem Artikel ausführen zu können, müssen Sie ein Office 365-globaler Administrator oder ein Mitglied &amp; der Rollengruppe Rolle OrganizationManagement anzuzeigen im Security Compliance Center sein.
    
- Rollengruppen für das Security &amp; Compliance Center haben möglicherweise ähnliche Namen wie die Rollengruppen in Exchange Online, sind aber nicht identisch. 
    
- Rollengruppenmitgliedschaften werden zwischen Exchange Online und dem Security &amp; Compliance Center nicht freigegeben.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden des Office 365 Admin Center, um einem anderen Benutzer Zugriff auf das &amp; Security Compliance Center zu gewähren

1. [Melden Sie sich bei Office 365 an, und wechseln Sie zum Admin Center](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
2. Öffnen Sie im Office 365 Admin Center **Admin** Center, und klicken Sie dann auf **Sicherheits &amp; Konformität**. 
    
3. Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.
    
4. Wählen Sie in der Liste die Rollengruppe aus, der Sie den Benutzer hinzufügen möchten, **** ![und klicken Sie](media/O365_MDM_CreatePolicy_EditIcon.gif)auf Bearbeitungssymbol bearbeiten.
    
5. Klicken Sie auf der Eigenschaftenseite der Rollengruppe unter **Mitglieder**auf ****![Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, und wählen Sie den Namen des Benutzers aus, den Sie hinzufügen möchten. 
    
6. Wenn Sie alle Benutzer ausgewählt haben, die Sie der Rollengruppe hinzufügen möchten, klicken Sie auf **hinzu\> fügen-** und dann auf **OK**.
    
7. Klicken Sie auf **Speichern**, um die Änderungen an der Rollengruppe zu speichern. 
    
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

1. Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.
    
2. Wählen Sie in der Liste die Rollengruppe aus, um die Mitglieder anzuzeigen.
    
3. Auf der rechten Seite in den Rollengruppen Details können Sie die Mitglieder der Rollengruppe anzeigen.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden von PowerShell, um einem anderen Benutzer Zugriff auf &amp; das Security Compliance Center zu gewähren

1. Stellen [Sie eine Verbindung mit Office 365 Security _AMP_ Compliance Center PowerShell her](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).
    
2. Verwenden Sie den Befehl **Add-RoleGroupMember** zum Hinzufügen eines Benutzers zur Rolle "Organisationsverwaltung", wie im folgenden Beispiel gezeigt. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Parameter**
  
- _-Identity_ ist die Rollengruppe, zu der ein Mitglied hinzugefügt werden soll. 
    
- _Member_ ist das Postfach, die universelle Sicherheitsgruppe (USG) oder der Computer, der der Rollengruppe hinzugefügt werden soll. Sie können jeweils nur ein Element angeben. 
    
Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um zu überprüfen, ob Sie Benutzern Zugriff auf das &amp; Security Compliance Center gewährt haben, verwenden Sie das Cmdlet **Get-RoleGroupMember** , um die Mitglieder in der Rollengruppe Organisationsverwaltung anzuzeigen, wie im folgenden Beispiel gezeigt. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  


---
title: Erteilen von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
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
description: Benutzer müssen Berechtigungen im Office 365 Security &amp; Compliance Center erhalten, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können.
ms.openlocfilehash: aa0d1e9af6eb547bbb145d06cabfc431028ec4f0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154297"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Erteilen von Benutzern Zugriff auf das Office 365 &amp; Security Compliance Center

Benutzer müssen Berechtigungen im Office 365 Security &amp; Compliance Center erhalten, bevor Sie alle Sicherheits-und Kompatibilitätsfeatures verwalten können. Als Office 365 globaler Administrator oder Mitglied der Mitglied-Rollengruppe im Security &amp; Compliance Center können Sie diese Berechtigungen Benutzern erteilen. Benutzer können nur die Sicherheits-oder Kompatibilitätsfeatures verwalten, auf die Sie Zugriff haben. 
  
Weitere Informationen zu den verschiedenen Berechtigungen, die Sie Benutzern im Security &amp; Compliance Center erteilen können, finden Sie unter [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Sie müssen ein Office 365 globaler Administrator oder ein Mitglied der Rollengruppe Mitglied im Security &amp; Compliance Center sein, um die Schritte in diesem Artikel ausführen zu können.
    
- Rollengruppen für das Security &amp; Compliance Center haben möglicherweise ähnliche Namen wie die Rollengruppen in Exchange Online, sind aber nicht identisch. 
    
- Rollengruppenmitgliedschaften werden nicht zwischen Exchange Online und dem Security &amp; Compliance Center freigegeben.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden des Office 365 admin Centers, um einem anderen Benutzer Zugriff auf &amp; das Security Compliance Center zu gewähren

1. [Melden Sie sich bei Office 365 an, und wechseln Sie zum Admin Center](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
2. Öffnen Sie im Office 365 Admin Center **Admin** Center, und klicken Sie dann auf **Sicherheits &amp; Kompatibilität**. 
    
3. Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.
    
4. Wählen Sie in der Liste die Rollengruppe aus, der Sie den Benutzer hinzufügen möchten, **** ![und klicken Sie](media/O365_MDM_CreatePolicy_EditIcon.gif)auf Bearbeitungssymbol bearbeiten.
    
5. Klicken Sie auf der Eigenschaftenseite der Rollengruppe unter **Mitglieder**auf Add-](media/ITPro-EAC-AddIcon.gif) Symbol **Hinzufügen**![, und wählen Sie den Namen des Benutzers (oder der Benutzer) aus, den Sie hinzufügen möchten. 
    
6. Wenn Sie alle Benutzer ausgewählt haben, die Sie der Rollengruppe hinzufügen möchten, klicken Sie auf **hinzu\> fügen** und dann auf **OK**.
    
7. Klicken Sie auf **Speichern**, um die Änderungen an der Rollengruppe zu speichern. 
    
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

1. Wechseln Sie im &amp; Security Compliance Center zu **Berechtigungen**.
    
2. Wählen Sie in der Liste die Rollengruppe aus, um die Mitglieder anzuzeigen.
    
3. Auf der rechten Seite in den Rollengruppen Details können Sie die Mitglieder der Rollengruppe anzeigen.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden von PowerShell, um einem anderen Benutzer Zugriff auf &amp; das Security Compliance Center zu gewähren

1. Stellen [Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).
    
2. Verwenden Sie den Befehl **Add-RoleGroupMember** , um einen Benutzer zur Rolle "Organisationsverwaltung" hinzuzufügen, wie im folgenden Beispiel dargestellt. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Parameter**
  
- _-Identity_ ist die Rollengruppe, der Sie ein Mitglied hinzufügen möchten. 
    
- _Mitglied_ ist das Postfach, die universelle Sicherheitsgruppe (Universal Security Group, USG) oder der Computer, der der Rollengruppe hinzugefügt werden soll. Sie können immer nur ein Element angeben. 
    
Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um zu überprüfen, ob Sie Benutzern Zugriff auf das &amp; Security Compliance Center gegeben haben, verwenden Sie das Cmdlet **Get-RoleGroupMember** , um die Mitglieder in der Rollengruppe Organisationsverwaltung anzuzeigen, wie im folgenden Beispiel dargestellt. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  


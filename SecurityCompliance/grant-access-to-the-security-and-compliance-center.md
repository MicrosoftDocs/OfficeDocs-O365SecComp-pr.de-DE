---
title: Gewähren des Benutzerzugriffs auf die Office 365-Sicherheit &amp; Compliance Center
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Benutzer müssen in der Office 365-Sicherheit Berechtigungen zugewiesen werden &amp; Compliance Center, bevor sie die Sicherheits- oder kompatibilitätsanforderungen Features des verwalten können.
ms.openlocfilehash: c612c99f7d72b19d072d728eb4851532d4012414
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013799"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Gewähren des Benutzerzugriffs auf die Office 365-Sicherheit &amp; Compliance Center

Benutzer müssen in der Office 365-Sicherheit Berechtigungen zugewiesen werden &amp; Compliance Center, bevor sie die Sicherheits- oder kompatibilitätsanforderungen Features des verwalten können. Als globaler Office 365-Administrator oder Mitglied der Rollengruppe in das Wertpapier OrganizationManagement &amp; Compliance Center, Sie können diesen Benutzern Berechtigungen erteilen. Benutzer können nur die Sicherheit und Compliance-Features verwalten, mit denen Sie Zugriff auf erhalten. 
  
Weitere Informationen zu den verschiedenen Berechtigungen können Sie erteilen für Benutzer in das Wertpapier &amp; Compliance Center, Auschecken [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Sie müssen ein globaler Office 365-Administrator oder ein Mitglied der Rollengruppe OrganizationManagement in das Wertpapier sein &amp; Compliance Center, um die Schritte in diesem Artikel auszuführen.
    
- Rollengruppen für die Sicherheit &amp; Compliance Center möglicherweise ähnliche Namen der Rollengruppe in Exchange Online, aber sie sind nicht identisch. 
    
- Rolle Gruppenmitgliedschaften werden nicht zwischen Exchange Online und die Sicherheit shared &amp; Compliance Center.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden Sie das Office 365 Administrationscenter zu einem anderen Benutzerzugriff auf der Sicherheit ermöglichen &amp; Compliance Center

1. [Anmelden bei Office 365 und im Administrationscenter zu wechseln](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
<<<<<<< HEAD
2. **Admin zentriert** öffnen Sie in Office 365 Admin Center, und klicken Sie dann auf **Security &amp; Compliance**. 
=======
2. **Admin zentriert** öffnen Sie in der Office 365-Verwaltungskonsole, und klicken Sie dann auf **Security &amp; Compliance**. 
>>>>>>> master
    
3. In das Wertpapier &amp; Compliance Center, **Berechtigungen**zu wechseln.
    
4. Wählen Sie aus der Liste die Rollengruppe, die Sie verwenden möchten, fügen Sie den Benutzer an, und klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
5. Klicken Sie auf der Eigenschaftenseite unter **Mitglieder**der Rollengruppe **Hinzufügen**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) und wählen Sie den Namen des Benutzers (oder Benutzer) Sie hinzufügen möchten. 
    
6. Wenn Sie alle Benutzer, die Sie verwenden möchten, der Rollengruppe hinzufügen, klicken Sie auf ausgewählt haben **Hinzufügen-\> ** , und klicken Sie dann **OK**.
    
7. Klicken Sie auf **Speichern**, um die Änderungen an der Rollengruppe zu speichern. 
    
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

1. In das Wertpapier &amp; Compliance Center, **Berechtigungen**zu wechseln.
    
2. Wählen Sie aus der Liste der Rollengruppe aus, um die Mitglieder anzuzeigen.
    
3. Auf der rechten Seite können Sie in den Details der Rolle, die Mitglieder der Rollengruppe anzeigen.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Verwenden von PowerShell zu einem anderen Benutzerzugriff auf der Sicherheit ermöglichen &amp; Compliance Center

1. [Verbinden auf die Office 365-Sicherheit &amp; Compliance Center mit remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).
    
2. Verwenden Sie den Befehl **Add-RoleGroupMember** zum Hinzufügen eines Benutzers zur Rolle "Organisationsverwaltung", wie im folgenden Beispiel gezeigt. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Parameter**
  
-  _-Identity_ ist die Rollengruppe, zu der ein Mitglied hinzugefügt werden soll. 
    
- - _Member_ ist das Postfach, universelle Sicherheitsgruppe (USG) oder Computer der Rollengruppe hinzufügen. Sie können jeweils nur ein Element angeben. 
    
Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um sicherzustellen, dass Sie Benutzern Zugriff auf die Sicherheit erteilt haben &amp; Compliance Center, verwenden Sie das Cmdlet **Get-RoleGroupMember** zum Anzeigen der Elemente in der Rollengruppe "Organisationsverwaltung", wie im folgenden Beispiel dargestellt. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  


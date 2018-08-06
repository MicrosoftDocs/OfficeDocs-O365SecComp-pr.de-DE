---
title: Verwalten der Berechtigungen der Administratorrollen-Gruppenberechtigungen in EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: In Microsoft Exchange Online Protection (EOP) können Sie die Exchange-Verwaltungskonsole verwenden, um einen Benutzer als Mitglied zu einer oder mehreren Rollengruppen hinzuzufügen, sodass er die Berechtigungen für bestimmte Verwaltungsaufgaben erhält. Darüber hinaus können Sie einen Benutzer über die Exchange-Verwaltungskonsole aus Rollengruppen entfernen.
ms.openlocfilehash: 5d50c77c97f2c345aa3994e7fa3ecd2eea93a13a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026662"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a>Verwalten der Berechtigungen der Administratorrollen-Gruppenberechtigungen in EOP
  
In Microsoft Exchange Online Protection (EOP) können Sie die Exchange-Verwaltungskonsole verwenden, um einen Benutzer als Mitglied zu einer oder mehreren Rollengruppen hinzuzufügen, sodass er die Berechtigungen für bestimmte Verwaltungsaufgaben erhält. Darüber hinaus können Sie einen Benutzer über die Exchange-Verwaltungskonsole aus Rollengruppen entfernen.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5-10 Minuten
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Benutzer, Kontakte und Rollengruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md). 
    
- Bestimmte Berechtigungen in Office 365 entsprechen Berechtigungen der Administratorrollengruppen in EOP. Weitere Informationen finden Sie in der Spalte "Rolle in Exchange Online" im Abschnitt "Für welche Dienste gelten meine Office 365-Berechtigungen?" unter [Zuweisen von Adminrollen](https://go.microsoft.com/fwlink/p/?LinkId=286708).
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="what-do-you-want-to-do"></a>Was möchten Sie machen?

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a>Zuweisen von Mitgliedern zu Administratorrollengruppen mithilfe der Exchange-Verwaltungskonsole

1. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Berechtigungen** \> **Administratorrollen**, klicken Sie auf die Rollengruppe, zu der Benutzer hinzugefügt werden sollen, und klicken Sie anschließend auf **Bearbeiten**![Bearbeitungssymbol](../media/ITPro-EAC-EditIcon.png).
    
2. Klicken Sie unter **Mitglieder** auf Hinzufügen ![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.png). Das Fenster zur Auswahl von Mitgliedern wird angezeigt.
    
3. Suchen Sie nach den Benutzern, die hinzugefügt werden sollen, oder wählen Sie die Benutzer aus der Liste aus.
    
4. Wenn Sie die Benutzer ausgewählt haben, die hinzugefügt werden sollen, klicken Sie auf **Hinzufügen** und anschließend auf **OK**. Das Fenster zur Auswahl von Mitgliedern wird geschlossen.
    
5. Wie Sie sehen, wurde der Benutzer zum Fenster **Mitglieder** hinzugefügt. Klicken Sie auf **Speichern**.
    
    > [!NOTE]
    > Nachdem Sie Mitglieder hinzugefügt oder aus der Rollengruppe entfernt haben, müssen sich die betroffenen Benutzer möglicherweise abmelden und dann erneut anmelden, um die Änderung ihrer Administratorrechten zu sehen. 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a>Entfernen von Mitgliedern aus Administratorrollengruppen mithilfe der Exchange-Verwaltungskonsole

1. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Berechtigungen** \> **Administratorrollen**, klicken Sie auf die Rollengruppe, aus der Benutzer entfernt werden sollen, und klicken Sie anschließend auf **Bearbeiten**![Bearbeitungssymbol](../media/ITPro-EAC-EditIcon.png).
    
2. Wählen Sie unterhalb von **Mitglieder** die Benutzer aus, die entfernt werden sollen, und klicken Sie auf Entfernen ![Entfernen (Symbol)](../media/ITPro-EAC-RemoveIcon.png).
    
3. Klicken Sie auf **Speichern**, um die Änderung an der Rollengruppe zu speichern und zur Seite **Administratorrollen** zurückzukehren. Überprüfen Sie im Detailfenster für die ausgewählte Rollengruppe, ob das Mitglied nicht länger unter Mitglieder aufgeführt wird, um sicherzustellen, dass der Benutzer erfolgreich aus der Administratorrollengruppe entfernt wurde. 
    
    > [!NOTE]
    > Nachdem Sie Mitglieder hinzugefügt oder aus der Rollengruppe entfernt haben, müssen sich die betroffenen Benutzer möglicherweise abmelden und dann erneut anmelden, um die Änderung ihrer Administratorrechten zu sehen. 
  
## <a name="for-more-information"></a>Weitere Informationen

[Featureberechtigungen in EOP](feature-permissions-in-eop.md)
  


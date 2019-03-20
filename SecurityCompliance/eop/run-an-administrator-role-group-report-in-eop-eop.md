---
title: 'Ausführen eines Administrator-Rollengruppenberichts in EOP '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Wenn ein Administrator Mitglieder zu Administratorrollengruppen hinzufügt oder daraus entfernt, protokolliert Microsoft Exchange Online Protection (EOP) jedes Vorkommen.
ms.openlocfilehash: 752def771d95fcfbb3f7cbe0bc86a33b3967716d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692714"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a>Ausführen eines Administrator-Rollengruppenberichts in EOP 

 Wenn ein Administrator Mitglieder zu Administratorrollengruppen hinzufügt bzw. aus diesen entfernt, protokolliert Microsoft Exchange Online Protection (EOP) jede dieser Aktionen. Wenn Sie einen Administrator-Rollengruppenbericht in der Exchange-Verwaltungskonsole ausführen, werden die Einträge als Suchergebnisse angezeigt. Diese umfassen die betroffenen Rollengruppen, den Benutzer, der die Mitgliedschaft der Rollengruppe geändert hat, wann diese Änderung vorgenommen wurde, und welche Aktualisierungen der Mitgliedschaften erfolgt sind. Mithilfe dieses Berichts können Sie Änderungen an den Administratorberechtigungen überwachen, die den Benutzern in der Organisation zugewiesen sind.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Berichte" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md). 
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a>Ausführen eines Administrator-Rollengruppenberichts mithilfe der Exchange-Verwaltungskonsole

Führen Sie den Administrator-Rollengruppenbericht aus, um die Änderungen an Verwaltungsrollengruppen in Ihrer Organisation innerhalb eines bestimmten Zeitraums zu ermitteln.
  
1. Wählen Sie in der Exchange-Verwaltungskonsole **Verwaltung der Richtlinientreue** \> **Überwachung** aus, und klicken Sie anschließend auf **Administrator-Rollengruppenbericht ausführen**.
    
2. Legen Sie **Startdatum** und **Enddatum** fest. Standardmäßig sucht der Bericht nach Änderungen, die innerhalb der letzten zwei Wochen an Administratorrollengruppen vorgenommen wurden.
    
3. Um die Änderungen für eine bestimmte Rollengruppe anzuzeigen, klicken Sie auf **Rollengruppen auswählen**. Wählen Sie im nachfolgenden Dialogfeld die Rollengruppe (oder -gruppen) aus, und klicken Sie auf **OK**. Sie können das Feld auch leer lassen, um nach allen geänderten Rollengruppen zu suchen.
    
4. Klicken Sie auf **Suchen**.
    
Wenn Änderungen gefunden werden, die mit den angegebenen Kriterien übereinstimmen, werden sie im Ergebnisbereich angezeigt. Klicken Sie auf eine Rollengruppe in den Suchergebnissen, um die Änderungen im Detailbereich anzuzeigen.
  
## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Wenn Sie einen Administrator-Rollengruppenbericht erfolgreich ausgeführt haben, werden die Rollengruppen, die innerhalb des Datumsbereichs geändert wurden, im Suchergebnisbereich angezeigt. Wenn keine Ergebnisse angezeigt werden, wurden im angegebenen Datumsbereich keine Änderungen an Rollengruppen vorgenommen. Wenn Sie davon ausgehen, dass Ergebnisse angezeigt werden sollten, ändern Sie den Datumsbereich, und führen Sie den Bericht erneut aus.
  
## <a name="monitor-changes-to-role-group-membership"></a>Überwachen von Änderungen an der Rollengruppenmitgliedschaft

Wenn einer Rollengruppe Mitglieder hinzugefügt oder daraus entfernt werden, wird in den im Detailbereich angezeigten Suchergebnissen angegeben, dass die Rollengruppenmitgliedschaft aktualisiert wurde, und die aktuellen Mitglieder werden aufgelistet. In den Ergebnissen ist nicht angegeben, welcher Benutzer hinzugefügt oder entfernt wurde.
  
Wenn Sie ermitteln möchten, ob ein Benutzer hinzugefügt oder entfernt wurde, müssen zwei separate Einträge im Bericht verglichen werden. Sehen Sie sich beispielsweise die folgenden Protokolleinträge für die Rollengruppe **HelpDesk** an: 
  
 **27.01.2013 16:43:00 Uhr**
  
 **Administrator**
  
 **Aktualisierte Mitglieder: Administrator;annb,florencef;pilarp**
  
 **06.02.2013 10:09:00 Uhr**
  
 **Administrator**
  
 **Aktualisierte Mitglieder: Administrator;annb;florencef;pilarp;tonip**
  
 **19.02.2013 14:12 Uhr**
  
 **Administrator**
  
 **Aktualisierte Mitglieder: Administrator;annb;florencef;tonip**
  
In diesem Beispiel wurden mit dem Administratorbenutzerkonto folgende Änderungen vorgenommen:
  
- Am 06.02.2013 wurde der Benutzer "tonip" hinzugefügt.
    
- Am 19.02.2013 wurde der Benutzer "pilarp" entfernt.
    


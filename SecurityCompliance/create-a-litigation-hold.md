---
title: Erstellen eines Rechtsstreits in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218655"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Erstellen eines Rechtsstreits in Office 365

Sie können ein Postfach für die Aufbewahrung von Rechtsstreitigkeiten platzieren, um alle Postfachinhalte beizubehalten, einschließlich gelöschter Elemente und der ursprünglichen Versionen geänderter Elemente. Wenn Sie ein Benutzerpostfach für die Beweissicherung festlegen, werden Inhalte im Archivpostfach des Benutzers (falls aktiviert) ebenfalls beibehalten. Wenn Sie einen Haltestatus erstellen, können Sie eine Aufbewahrungsdauer (auch als *zeitbasierte Aufbewahrung*bezeichnet) angeben, sodass gelöschte und geänderte Elemente für einen bestimmten Zeitraum aufbewahrt und dann endgültig aus dem Postfach gelöscht werden. Oder Sie können Inhalte auf unbestimmte Zeit aufbewahren (so genannte *unendliche Haltestatus*) oder bis die Beweissicherung entfernt wird. Wenn Sie einen Zeitraum für die Aufbewahrungsdauer angeben, wird er ab dem Datum berechnet, an dem eine Nachricht empfangen oder ein Postfachelement erstellt wird. 
  
Hier erfahren Sie, was passiert, wenn Sie einen Rechtsstreit halten.
  
- Elemente, die vom Benutzer dauerhaft gelöscht werden, werden für die Dauer des haltebereichs im Ordner "Wiederherstellbare Elemente" im Postfach des Benutzers aufbewahrt.
    
- Elemente, die vom Benutzer aus dem Ordner "Wiederherstellbare Elemente" gelöscht werden, werden für die Dauer des haltebereichs beibehalten.
    
- Das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" wurde von 30 GB auf 110 GB erhöht.
    
- Elemente in den primären und archivpostfächern des Benutzers werden beibehalten
    
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um ein Exchange Online-Postfach für die Aufbewahrung von Rechtsstreitigkeiten zu aktivieren, muss ihm eine Exchange Online-Plan 2-Lizenz zugewiesen sein. Wenn einem Postfach eine Exchange Online-Plan 1-Lizenz zugewiesen ist, müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, um es in der Warteschleife zu platzieren.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>AufbewahrungsPflicht für ein Postfach im Office 365 Admin Center

Im folgenden finden Sie die Schritte, mit denen Sie mit dem Office 365 Admin Center ein maibox in den Prozess halten können.

1. Wechseln Sie https://portal.office.com/adminportal/home zu, und melden Sie sich mit ihrem globalen Administratorkonto an.
2. Klicken Sie im linken Navigationsbereich auf**aktive Benutzer Benutzer** . **** > 
3. Wählen Sie den Benutzer aus, dessen Postfach Sie bei der Beweissicherung platzieren möchten.
4. Klicken Sie auf der Seite "Fly-Out" auf **e-Mail-Einstellungen**, und klicken Sie dann neben **rechtsStreit anhalten**auf **Bearbeiten** .
5. Klicken Sie auf der Seite für die **Beweis** Sicherung auf die Umschaltfläche, um das Verfahren für die Aufbewahrung zu aktivieren, und füllen Sie die folgenden optionalen Einstellungen aus:
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    a. **Hold-Dauer (Tage)** – verwenden Sie dieses Feld, um einen zeitbasierten Haltebereich zu erstellen, und geben Sie an, wie lange Postfachelemente aufbewahrt werden, wenn das Postfach in den Rechtsstreit versetzt wird. Die Dauer wird anhand des Datums berechnet, an dem ein Postfachelement empfangen oder erstellt wird. Wenn Sie dieses Feld leer lassen, werden Elemente dauerhaft oder bis zum Entfernen des haltebereichs aufbewahrt. Verwenden Sie Days, um die Dauer anzugeben.
    
    b. **Hinweis** : Verwenden Sie dieses Feld, um dem Benutzer mitzuteilen, dass sein Postfach in einem Rechtsstreit gehalten wird. Der Hinweis wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn er Outlook 2010 oder höher verwendet. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.
     
    c. **Webseite** – verwenden Sie dieses Feld, um den Benutzer zu einer Website zu leiten, um weitere Informationen zur Aufbewahrung von Rechtsstreitigkeiten zu erhalten. Diese URL wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn Sie Outlook 2010 oder höher verwenden. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.
 
6. Klicken Sie auf speichern, um die Beweis **Sicherung** zu erstellen.

Nachdem Sie den Haltebereich erstellt haben, wird in den e-Mail-Einstellungen auf der Seite "Fly-Out" angezeigt, dass für den ausgewählten Benutzer die Option "Beweissicherung" aktiviert ist.

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

Weitere Informationen zum Erstellen und Verwalten von Rechtsstreitigkeiten und zum Verwenden von Exchange Online PowerShell zum Massen Erstellen von Rechtsstreitigkeiten finden Sie unter [platzieren eines Postfachs in der Beweis](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold)Sicherung.

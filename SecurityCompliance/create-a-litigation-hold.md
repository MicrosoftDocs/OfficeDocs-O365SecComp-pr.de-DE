---
title: Erstellen Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037958"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Erstellen Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten in Office 365

Sie können ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten, die beibehalten werden alle Inhalt von Postfächern, einschließlich der gelöschten Elemente und der ursprünglichen Versionen geänderter Objekte platzieren. Wenn Sie ein Benutzerpostfach beweissicherungsverfahrens einleiten, wird Inhalt im Archivpostfach des Benutzers (falls aktiviert) auch beibehalten. Wenn Sie einen Haltestatus erstellen, können Sie eine Warteschleife Dauer (auch als *zeitbasierte Aufbewahrung*bezeichnet) angeben, sodass gelöscht und geänderte Elemente für einen bestimmten Zeitraum aufbewahrt und dauerhaft aus dem Postfach gelöscht werden. Oder Sie können nur Inhalt auf unbestimmte Zeit beibehalten (eine *unendliche Warteschleife*genannt) oder bis die Aufbewahrung für eventuelle Rechtsstreitigkeiten entfernt wird. Wenn Sie einen Haltestatus Dauer angeben, wird ab dem Datum berechnet eine Nachricht empfangen oder ein Postfach-Element erstellt wird. 
  
Hier ist, was geschieht, wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten erstellen.
  
- Elemente, die vom Benutzer endgültig gelöscht werden, werden im Ordner "wiederherstellbare Elemente" im Postfach des Benutzers für die Dauer des Haltestatus beibehalten.
    
- Elemente, die vom Benutzer aus dem Ordner wiederherstellbare Elemente gelöscht werden, werden für die Dauer des Haltestatus beibehalten.
    
- Das Speicherkontingent für "wiederherstellbare Elemente" wird von 30 GB auf 110 GB erhöht.
    
- Elemente des Benutzers primärer und die archivpostfächer werden beibehalten.
    
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um ein Exchange Online-Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten zu platzieren, müssen sie eine Lizenz für Exchange Online – Plan 2 zugewiesen werden. Wenn ein Postfach eine Exchange Online – Plan 1-Lizenz zugewiesen ist, müssten Sie weisen Sie ihr eine separate Lizenz der Exchange Online-Archivierung auf platziert halten.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Platzieren eines Postfachs Aufbewahrung für eventuelle Rechtsstreitigkeiten im Office 365 Administrationscenter

Hier sind die Schritte, um eine Maibox auf Aufbewahrung für eventuelle Rechtsstreitigkeiten im Office 365 Admin Center zu platzieren.

1. Wechseln Sie zu https://portal.office.com/adminportal/home und melden Sie sich über das globale Administratorkonto.
2. Klicken Sie auf **Benutzer** > **aktive Benutzer** im linken Navigationsbereich.
3. Wählen Sie den Benutzer, deren Postfach Sie beweissicherungsverfahrens platzieren möchten.
4. Klicken Sie auf der Seite hinausfliegenden klicken Sie auf **E-Mail-Einstellungen**, und klicken Sie dann auf **Bearbeiten** , neben **Aufbewahrung für eventuelle Rechtsstreitigkeiten**.
5. Klicken Sie auf der Seite **Aufbewahrung für eventuelle Rechtsstreitigkeiten** auf die Umschaltfläche, um Aufbewahrung für eventuelle Rechtsstreitigkeiten zu aktivieren, und schließen Sie die folgenden optionalen Einstellungen, die angezeigt werden:
 
    ![O365_LitigationHold1.PNG](media/O365-LitigationHold1.png)

    a. **halten Dauer (in Tagen)** -verwenden Sie dieses Feld zum Erstellen einer zeitbasierte Aufbewahrung und angeben, wie lange Postfachelemente gehalten werden, wenn das Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird. Ein Element Postfach empfangen oder erstellt wird, wird die Dauer ab dem Datum berechnet. Wenn Sie dieses Feld leer lassen, werden Elemente aufrechterhalten, auf unbestimmte Zeit oder, bis die Sperre entfernt wurde. Verwenden von Tagen die Dauer angeben.
    
    b. **Hinweis** - verwenden Sie dieses Feld informiert den Benutzer, den ihr Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten ist. Die Notiz wird auf der Seite Kontoinformationen in das Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. Zugriff auf dieser Seite können Benutzer die **Datei** in Outlook klicken.
     
    c. **Webseite** - verwenden Sie dieses Feld, um den Benutzer auf eine Website für Weitere Informationen zur Aufbewahrung für eventuelle Rechtsstreitigkeiten zu leiten. Diese URL wird auf der Seite Kontoinformationen in das Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. Zugriff auf dieser Seite können Benutzer die **Datei** in Outlook klicken.
 
6. Klicken Sie auf **Speichern** , um die Aufbewahrung für eventuelle Rechtsstreitigkeiten erstellen.

Nachdem Sie den Haltestatus erstellen, die e-Mail-Einstellungen auf der Seite hinausfliegenden zeigt an, Aufbewahrung für eventuelle Rechtsstreitigkeiten für den ausgewählten Benutzer aktiviert ist.

![O365_LitigationHold2.PNG](media/O365-LitigationHold2.png)

Weitere Informationen zum Erstellen und Verwalten von Rechtsstreitigkeiten enthält und erstellen mithilfe von Exchange Online PowerShell Massen-Aufbewahrung für eventuelle enthält finden Sie unter [Place ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).

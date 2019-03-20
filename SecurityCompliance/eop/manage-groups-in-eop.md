---
title: Verwalten von Gruppen in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Sie können Exchange Online Protection (EOP) zur Erstellung E-Mail-aktivierter Gruppen für eine Exchange-Organisation verwenden. Sie können EOP auch verwenden, um Gruppeneigenschaften zu definieren oder zu aktualisieren, über die Mitgliedschaften, E-Mail-Adressen und andere Aspekte von Gruppen festgelegt werden.
ms.openlocfilehash: db649e4fd955d13e50e96007e8e38fe2c1de5b4d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693301"
---
# <a name="manage-groups-in-eop"></a>Verwalten von Gruppen in EOP

 Sie können Exchange Online Protection (EOP) zur Erstellung E-Mail-aktivierter Gruppen für eine Exchange-Organisation verwenden. Sie können EOP auch verwenden, um Gruppeneigenschaften zu definieren oder zu aktualisieren, über die Mitgliedschaften, E-Mail-Adressen und andere Aspekte von Gruppen festgelegt werden. Sie können je nach Bedarf Verteiler- oder Sicherheitsgruppen anlegen. Diese Gruppen können mithilfe des Exchange Admin Center (EAC) oder über Windows Remote-PowerShell erstellt werden. 
  
## <a name="types-of-mail-enabled-groups"></a>Arten von E-Mail-aktivierten Gruppen

Sie können für Ihre Exchange-Organisation zwei Arten von Gruppen erstellen:
  
- [Erstellen einer Gruppe im EAC](manage-groups-in-eop.md) (auch als Verteilergruppen bezeichnet) sind Sammlungen von E-Mail-Benutzern, z. B. Teams oder andere spontan gebildete Gruppen, die E-Mails zu einem gemeinsamen Thema senden oder empfangen müssen. Verteilergruppen sind exklusiv für die Verteilung von E-Mail-Nachrichten vorgesehen. In EOP wird mit dem Begriff "Verteilergruppe" jede E-Mail-aktivierte Gruppe bezeichnet, egal, ob sie sich in einem Sicherheitskontext befindet oder nicht.
    
- [Bearbeiten oder Entfernen einer Gruppe im EAC](manage-groups-in-eop.md) (auch als Sicherheitsgruppen bezeichnet) sind Sammlungen von E-Mail-Benutzern, die Zugangsberechtigungen für Administratorrollen benötigen. Sie könnten z. B. bestimmten Gruppen von Benutzern Berechtigungen für Administratorrollen gewähren, sodass diese Benutzer dann Anti-Span- und Anti-Malware-Einstellungen konfigurieren können.
    
    > [!NOTE]
    > Standardmäßig ist für alle neuen E-Mail-aktivierten Sicherheitsgruppen die Authentifizierung aller Absender erforderlich. Auf diese Weise wird verhindert, dass externe Absender Nachrichten an E-Mail-aktivierte Sicherheitsgruppen senden können. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter Eintrag "Verteilergruppen und Sicherheitsgruppen" im Thema [Featureberechtigungen in EOP](feature-permissions-in-eop.md). 
    
- Beachten Sie, dass beim Erstellen und Verwalten von Gruppen mithilfe von Remote-PowerShell-Cmdlets eine Drosselung auftreten kann.
    
- Dieses Cmdlet verwendet eine Batchverarbeitungsmethode, die zu einer Laufzeitverzögerung von wenigen Minuten führt, bevor die Ergebnisse des Cmdlets sichtbar sind.
    
- Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online Protection mithilfe der Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).
    
- Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Liegt ein Problem vor? Bitten Sie in den Exchange-Foren um Hilfe. Besuchen Sie die Foren unter [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) oder [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="create-a-group-in-the-eac"></a>Erstellen einer Gruppe im EAC

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Gruppen**.
    
2. Klicken Sie auf **Neu**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif) und anschließend je nach Bedarf auf **Verteilergruppe** oder auf **Sicherheitsgruppe**. Zur Unterscheidung siehe [Arten von E-Mail-aktivierten Gruppen](manage-groups-in-eop.md). 
    
3. Füllen Sie auf der Seite **Neue Verteilergruppe** oder **Neue Sicherheitsgruppe** die folgenden Felder aus: 
    
  - **Anzeigename** Geben Sie einen Anzeigenamen ein, der in Ihrer Organisation eindeutig ist und für die EOP-Benutzer einen Sinn ergibt. Der Anzeigename ist erforderlich. 
    
  - **Alias** Geben Sie einen Gruppenalias mit einer Länge von bis zu 64 Zeichen ein, der in Ihrer Organisation eindeutig ist. Wenn ein EOP-Benutzer diesen Alias in die Zeile An: einer E-Mail eingibt, wird er in den Anzeigenamen der Gruppe aufgelöst. Wenn Sie den Alias ändern, wird die primäre SMTP-Adresse für die Gruppe ebenfalls geändert und enthält dann den neuen Alias. Der Alias ist erforderlich. 
    
  - **Beschreibung** Geben Sie eine Beschreibung der Gruppe ein, sodass der Zweck der Gruppe erkennbar ist. 
    
  - **Besitzer** Standardmäßig ist die Person, die eine Gruppe erstellt, der Besitzer. Sie können Besitzer hinzufügen, indem Sie auf **Hinzufügen**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif) klicken. Jede Gruppe muss mindestens einen Besitzer aufweisen.
    
    > [!NOTE]
    > Besitzer von Gruppen müssen kein Mitglied der jeweiligen Gruppe sein. 
  
  - **Mitglieder** Verwenden Sie diesen Abschnitt zum Hinzufügen von Mitgliedern und um anzugeben, ob eine Genehmigung erforderlich ist, damit Personen der Gruppe beitreten bzw. diese verlassen können. Klicken Sie zum Hinzufügen von Mitgliedern zur Gruppe auf **Hinzufügen**![Hinzufügen (Symbol)](../media/ITPro-EAC-AddIcon.gif).
    
4. Klicken Sie auf **OK**, um zur Ursprungsseite zurückzukehren. 
    
5. Wenn Sie fertig sind, klicken Sie auf **Speichern**, um die Gruppe zu erstellen. Die neue Gruppe sollte in der Liste der Gruppen angezeigt werden. 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a>Bearbeiten oder Entfernen einer Gruppe im EAC

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Gruppen**.
    
2. Führen Sie einen der folgenden Schritte aus:
    
  - So bearbeiten Sie eine Gruppe: Klicken Sie in der Liste der Gruppen auf die Verteiler-oder Sicherheitsgruppe, die Sie anzeigen oder ändern möchten, **** ![und klicken Sie](../media/ITPro-EAC-EditIcon.gif)dann auf Bearbeitungssymbol bearbeiten. Sie können je nach Bedarf allgemeine Einstellungen aktualisieren sowie Gruppenbesitzer oder Gruppenmitglieder hinzufügen oder entfernen.
    
  - So entfernen Sie eine Gruppe Markieren Sie die Gruppe, und klicken Sie auf **Entfernen**![Entfernen (Symbol)](../media/ITPro-EAC-RemoveIcon.gif).
    
3. Wenn Sie die Änderungen vorgenommen haben, klicken Sie auf **Speichern**.
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>Erstellen, Bearbeiten oder Entfernen einer Gruppe mithilfe von Windows Remote-PowerShell

Diese Abschnitt enthält Informationen zum Erstellen von Gruppen und Ändern der Eigenschaften der Gruppen mithilfe von Windows Remote-PowerShell. Es wird außerdem gezeigt, wie eine vorhandene Gruppe entfernt wird. 
  
 **So erstellen Sie eine Gruppe mithilfe von Windows Remote-PowerShell**
  
In diesem Beispiel wird das [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx)-Cmdlet verwendet, um eine Verteilergruppe mit dem Alias "itadmin" und dem Namen "IT Administrators" zu erstellen. Außerdem werden Benutzer als Mitglieder der Gruppe hinzugefügt. 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

Wenn Sie statt einer Verteilergruppe eine Sicherheitsgruppe erstellen möchten, geben Sie stattdessen  `-Type "Security"` an. 
  
Um zu überprüfen, ob die Gruppe "IT Administrators" erfolgreich erstellt wurde, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet aus, um Informationen über die neue Gruppe anzuzeigen: 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

Um eine Liste der Mitglieder in der Gruppe anzuzeigen, führen Sie das [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx)-Cmdlet wie folgt aus: 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

Um eine vollständige Liste aller Ihrer Gruppen anzuzeigen, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus: 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 **So ändern Sie die Eigenschaften einer Gruppe mithilfe von Windows Remote-PowerShell**
  
Verwenden Sie die Cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) und [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx), um Eigenschaften für Gruppen anzuzeigen und zu ändern. Ein Vorteil der Verwendung von Remote-PowerShell gegenüber dem EAC ist, dass damit Eigenschaften für mehrere Gruppe geändert werden können. 
  
Hier einige Beispiele für die Verwendung von Windows Remote-PowerShell zur Änderung von Gruppeneigenschaften.
  
In diesem Beispiel wird das [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx)-Cmdlet verwendet, um die primäre SMTP-Adresse (auch als die Antwortadresse bezeichnet) für die Gruppe "Seattle Employees" in "sea.employees@contoso.com" zu ändern. 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

Um zu prüfen, ob Sie die Eigenschaften einer Gruppe erfolgreich geändert haben, überprüfen Sie die Änderungen mithilfe des [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlets. Ein Vorteil der Verwendung von Remote-PowerShell besteht darin, dass Sie mehrere Eigenschaften für mehrere Gruppen anzeigen können. Führen Sie im obigen Beispiel, in dem die primäre SMTP-Adressgruppe geändert wurde, folgenden Befehl aus, um den neuen Wert zu überprüfen: 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

In diesem Beispiel wird das [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx)-Cmdlet verwendet, um alle Mitglieder der Gruppe "Seattle Employees" zu aktualisieren. Verwenden Sie ein Komma, um alle Mitglieder voneinander zu trennen. 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

Um eine Liste aller Mitglieder in der Gruppe "Seattle Employees" abzurufen, verwenden Sie wie folgt das [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx)-Cmdlet: 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 **So entfernen Sie eine Gruppe mithilfe von Windows Remote-PowerShell**
  
In diesem Beispiel wird das [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx)-Cmdlet verwendet, um eine Verteilergruppe mit dem Namen "IT Administrators" zu entfernen. 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

Um zu überprüfen, ob die Gruppe entfernt wurde, führen Sie das [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx)-Cmdlet wie folgt aus, und überprüfen Sie, ob die Gruppe (in diesem Fall ("IT Administrators") gelöscht wurde. 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```



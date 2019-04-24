---
title: Erstellen eines Beweissicherungsverfahrens
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
ms.openlocfilehash: e4cb614167f89cb6e99d96aa94027ba90d86543e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258368"
---
# <a name="create-a-litigation-hold"></a>Erstellen eines Beweissicherungsverfahrens

Sie können ein Postfach für die Aufbewahrung von Rechtsstreitigkeiten platzieren, um alle Postfachinhalte beizubehalten, einschließlich gelöschter Elemente und der ursprünglichen Versionen geänderter Elemente. Wenn Sie ein Benutzerpostfach für die Beweissicherung festlegen, werden Inhalte im Archivpostfach des Benutzers (falls aktiviert) ebenfalls beibehalten. Wenn Sie einen Haltestatus erstellen, können Sie eine Aufbewahrungsdauer (auch als *zeitbasierte Aufbewahrung*bezeichnet) angeben, sodass gelöschte und geänderte Elemente für einen bestimmten Zeitraum aufbewahrt und dann endgültig aus dem Postfach gelöscht werden. Oder Sie können Inhalte auf unbestimmte Zeit aufbewahren (so genannte *unendliche Haltestatus*) oder bis die Beweissicherung entfernt wird. Wenn Sie einen Zeitraum für die Aufbewahrungsdauer angeben, wird er ab dem Datum berechnet, an dem eine Nachricht empfangen oder ein Postfachelement erstellt wird. 
  
Hier erfahren Sie, was passiert, wenn Sie einen Rechtsstreit halten.
  
- Elemente, die vom Benutzer dauerhaft gelöscht werden, werden für die Dauer des haltebereichs im Ordner "Wiederherstellbare Elemente" im Postfach des Benutzers aufbewahrt.
    
- Elemente, die vom Benutzer aus dem Ordner "Wiederherstellbare Elemente" gelöscht werden, werden für die Dauer des haltebereichs beibehalten.
    
- Das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" wurde von 30 GB auf 110 GB erhöht.
    
- Elemente in den primären und archivpostfächern des Benutzers werden beibehalten
    
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um ein Exchange Online-Postfach für die Aufbewahrung von Rechtsstreitigkeiten zu aktivieren, muss ihm eine Exchange Online-Plan 2-Lizenz zugewiesen sein. Wenn einem Postfach eine Exchange Online-Plan 1-Lizenz zugewiesen ist, müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, um es in der Warteschleife zu platzieren.
    

## <a name="place-a-mailbox-on-litigation-hold"></a>Aktivieren des Beweissicherungsverfahrens für ein Postfach

Im folgenden finden Sie die Schritte, mit denen Sie ein Postfach mithilfe der Exchange-Verwaltungskonsole in einem Rechtsstreit halten können.

1. Wechseln Sie [https://outlook.office.com/ecp](https://outlook.office.com/ecp) zu, und melden Sie sich mit ihrem globalen Administratorkonto an.

2. Klicken Sie im linken Navigationsbereich auf **Empfänger _GT_ Postfächer** .

3. Wählen Sie das Postfach aus, das Sie für die Beweissicherung festlegen möchten, und klicken Sie dann auf **Bearbeiten**.

4. Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen**.
    
5. Klicken Sie unter **Beweissicherungsverfahren: Deaktiviert** auf **Aktivieren**, um für das Postfach das Beweissicherungsverfahren zu aktivieren.
    
6. Geben Sie auf der Seite **Litigation Hold** die folgenden optionalen Informationen ein: 
    
    - **Dauer der Streitbeilegung (Tage)** – verwenden Sie dieses Feld, um einen zeitbasierten Haltebereich zu erstellen, und geben Sie an, wie lange Postfachelemente aufbewahrt werden sollen, wenn das Postfach in den Rechtsstreit versetzt wird. Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde. Wenn die Aufbewahrungsdauer für ein bestimmtes Element abgelaufen ist, wird das Element nicht mehr beibehalten. Wenn Sie dieses Feld leer lassen, werden Elemente unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird. Geben Sie die Dauer in Tagen an.
    
    - **Hinweis** : Verwenden Sie dieses Feld, um den Benutzer darüber zu informieren, dass das Postfach in einem Rechtsstreit gehalten wird. Der Hinweis wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn er Outlook 2010 oder höher verwendet. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.
    
    - **URL** -verwenden Sie dieses Feld, um den Benutzer zu einer Website zu leiten, um weitere Informationen zur Aufbewahrung von Rechtsstreitigkeiten zu erhalten. Diese URL wird auf der Seite Kontoinformationen im Postfach des Benutzers angezeigt, wenn Sie Outlook 2010 oder höher verwenden. Um auf diese Seite zuzugreifen, können Benutzer in Outlook auf **Datei** klicken.

7. Klicken Sie auf der Seite für die **Beweis** **Sicherung auf Speichern** , und klicken Sie dann auf der Eigenschaftenseite des Postfachs auf **Speichern** .

### <a name="create-a-litigation-hold-using-powershell"></a>Erstellen einer Beweissicherung mithilfe von PowerShell

Sie können auch eine Beweissicherung erstellen, indem Sie den folgenden Befehl in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)ausführen:

```
Set-Mailbox <username> -LitigationHoldEnabled $true
```

Der vorherige Befehl behält Elemente unbegrenzt bei, da die Aufbewahrungsdauer nicht angegeben wird. So erstellen Sie eine zeitbasierte Aufbewahrung mit dem folgenden Befehl:

```
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

Weitere Informationen finden Sie unter [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox).

## <a name="how-does-litigation-hold-work"></a>Wie funktioniert das Beweissicherungsverfahren?

Beim normalen Löschworkflow wird ein dauerhaft gelöschtes (UMSCHALT+ENTF) oder aus dem Ordner „Gelöschte Elemente" gelöschtes Postfachelement in den Unterordner „Löschvorgänge" des Ordners „Wiederherstellbare Elemente" verschoben. Beim Anwenden einer Löschrichtlinie (hierbei handelt es sich um ein Aufbewahrungstag mit einer konfigurierten Aufbewahrungsaktion) werden Elemente auch nach Ablauf des Aufbewahrungszeitraums in den Unterordner „Löschvorgänge" verschoben. Beim dauerhaften Löschen eines Elements im Ordner „Wiederherstellbare Elemente" durch einen Benutzer oder nach Ablauf der Aufbewahrungsdauer wird das Element in den Unterordner „Endgültige Löschvorgänge" des Ordners „Wiederherstellbare Elemente" verschoben und zum endgültigen Löschen markiert. Das Element wird beim nächsten Verarbeiten des Postfachs vom Assistenten für verwalteten Ordner aus Exchange dauerhaft gelöscht.

Ist für das Postfach das Beweissicherungsverfahren aktiviert, werden die Elemente im Unterordner „Endgültige Löschvorgänge" für die für das Beweissicherungsverfahren angegebene Aufbewahrungsdauer aufbewahrt. Die Aufbewahrungsdauer wird anhand des ursprünglichen Datums berechnet,an dem ein Element empfangen oder erstellt wurde und legt fest, wie lange die Elemente im Unterordner „Endgültige Löschvorgänge" aufbewahrt werden. Wenn die Aufbewahrungsdauer für ein Element im Unterordner „Endgültige Löschvorgänge" abläuft, wird das Element zum endgültigen Löschen vorgemerkt und beim nächsten Verarbeiten des Postfachs vom Assistenten für verwalteten Ordner dauerhaft aus Exchange gelöscht. Wenn die dauerhafte Aufbewahrung für ein Postfach aktiviert ist, werden die Elemente nicht aus dem Unterordner „Endgültige Löschvorgänge" gelöscht.

Die folgende Abbildung zeigt die Unterordner in den Ordnern „Wiederherstellbare Elemente" und den Aufbewahrungsworkflowprozess.

![Lebenszyklus](media/LitigationHoldLifeCycle.png)

> [!NOTE]
> Wenn ein mit einem eDiscovery-Fall verbundener Haltebereich auf ein Postfach gesetzt wird, werden die gelöschten Elemente aus dem Unterordner "Löschvorgänge" in den Unterordner DiscoveryHolds verschoben und bleiben erhalten, bis das Postfach aus dem eDiscovery-Speicher freigegeben wird.
  
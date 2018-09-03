---
title: Aktivieren Sie die uneingeschränkte Archivierung in Office 365 - Admin-Hilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: 'Für Administratoren: enthält Informationen zum Aktivieren der Archivierung automatisch erweitert, in Office 365, die Ihre Benutzer für ihre Exchange Online-Postfächer mit unbegrenzte Speicher bereitstellt. Sie können die Archivierung automatisch erweitert, für die gesamte Organisation oder nur für bestimmte Benutzer aktivieren.'
ms.openlocfilehash: ede3e75a021d750160268ccf06ac4fe1637d219a
ms.sourcegitcommit: 81c2fd5cd940c51bc43ac7858c7bdfa207ce401a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2018
ms.locfileid: "23809700"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Aktivieren Sie die uneingeschränkte Archivierung in Office 365 - Admin-Hilfe

Das Exchange Online-Archivierung erweiterbares Feature können in Office 365 Sie um unbegrenzte Speicherplatz für archivpostfächer zu aktivieren. Wenn die Archivierung erweiterbares aktiviert ist, ist zusätzlicher Speicherplatz, wenn sie den Speichergrenzwert Ansätze Archivpostfach des Benutzers automatisch hinzugefügt. Das Ergebnis ist die Speicherkapazität unbegrenzte Mailbox. Sie können aktivieren erweiterbares Archivierung für alle Benutzer in Ihrer Organisation oder nur für bestimmte Benutzer. Weitere Informationen zum Erweitern von automatischen Archivierung, finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md).

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein globaler Administrator in Office 365-Organisation oder ein Mitglied der Rollengruppe "Organisationsverwaltung" in Ihrer Exchange Online-Organisation zum Aktivieren der Archivierung automatisch erweitert, für die gesamte Organisation oder für bestimmte Benutzer sein. Alternativ müssen Sie Mitglied einer Rollengruppe sein, die den E-Mail-Empfänger Role erweiterbares Archivierung für bestimmte Benutzer aktivieren zugewiesen hat.
    
- Archivpostfach des Benutzers muss aktiviert sein, bevor Sie automatisch erweitert Archivierung aktivieren können. Ein Benutzer muss eine Lizenz Exchange Online – Plan 2 So aktivieren Sie das Archivpostfach zugewiesen werden. Wenn ein Benutzer eine Lizenz für Exchange Online – Plan 1 zugewiesen ist, müssten Sie diese eine separate Exchange Online-Archivierung Lizenz deren Archivpostfach aktivieren zuordnen. Finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md).
    
- Sie können auch PowerShell verwenden, um archivpostfächer zu aktivieren. Finden Sie im Abschnitt [Weitere Informationen](#more-information) für ein Beispiel für den PowerShell-Befehl, mit denen Sie archivpostfächer für alle Benutzer in Ihrer Organisation zu aktivieren. 
    
- Erweiterbares auch Archivierung unterstützt freigegebene Postfächer. Um das Archiv für ein freigegebenes Postfach zu aktivieren, ist eine Lizenz für Exchange Online – Plan 2 oder eine Lizenz Exchange Online – Plan 1 mit Exchange Online-Archivierung-Lizenz erforderlich.
    
- Kann nicht verwendet werden, die Exchange-Verwaltungskonsole oder die Sicherheit &amp; Compliance Center, um die Aktivierung der Archivierung automatisch erweitert. Sie müssen Exchange Online PowerShell verwenden. Zum Verbinden mit remote-PowerShell mit Ihrer Exchange Online-Organisation finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>Erweiterbares Archivierung für die gesamte Organisation aktiviert werden?

Sie können die erweiterbares Archivierung für die gesamte Organisation aktivieren. Nachdem Sie es aktivieren, wird automatisch erweitert Archivierung aktiviert werden für vorhandene Benutzerpostfächer und für neue Benutzerpostfächer, die erstellt werden. Wenn Sie neue Benutzerpostfächer erstellen, müssen Sie Hauptfenster Archivpostfach des Benutzers zu aktivieren, damit das erweiterbares Archivierung Feature für die neue Postfach des Benutzers verwendet wird.
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
2. Führen Sie den folgenden Befehl in Exchange Online PowerShell-Skripte zur Archivierung automatisch erweitert, für die gesamte Organisation aktiviert werden.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>Erweiterbares Archivierung für bestimmte Benutzer aktivieren

Anstelle der erweiterbares Archivierung für alle Benutzer in Ihrer Organisation können Sie nur für bestimmte Benutzer aktivieren. Dies ist sinnvoll, da nur einige Benutzer möglicherweise die Notwendigkeit einer sehr großen Archivspeicher müssen.
  
Wenn Sie die erweiterbares Archivierung für einen bestimmten Benutzer aktivieren und das Postfach des Benutzers in auf halten oder eine Aufbewahrungsrichtlinie für Office 365 zugewiesen, werden die folgenden beiden Konfigurationen Änderungen vorgenommen:
  
- 10 GB (von 100 GB auf 110 GB) wird das Speicherkontingent für primäre Archivpostfach des Benutzers erhöht. 10 GB (von 90 GB auf 100 GB) wird auch die Kontingentgrenzwert erhöht.
    
- 10 GB (auch von 100 GB auf 110 GB) wird das Speicherkontingent für den Ordner wiederherstellbare Elemente im primären Postfach des Benutzers erhöht. Die wiederherstellbare Elemente Warnung wird auch von 10 GB (von 90 GB auf 100 GB) erhöht. Diese Änderungen gelten nur, wenn das Postfach im auf halten oder eine Aufbewahrungsrichtlinie für Office 365 zugewiesen.
    
Diese zusätzliche Speicherplatz wird hinzugefügt um Probleme Speicher zu verhindern, die auftreten können, bevor das Archiv erweiterbares bereitgestellt wird. Beachten Sie, zusätzlicher Speicher Speicherplatz *ist nicht* hinzugefügt, wenn Sie die Archivierung automatisch erweitert, für die gesamte Organisation, gemäß der Beschreibung im vorherigen Abschnitt aktivieren. 
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
2. Führen Sie den folgenden Befehl in Exchange Online PowerShell um erweiterbares Archivierung für einen bestimmten Benutzer zu aktivieren. Wie bereits erklärt muss Archivpostfach des Benutzers (Hauptfenster Archiv) aktiviert sein, bevor Sie automatisch erweitert Archivierung für diesen Benutzer aktivieren können.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> In einer Exchange-hybridbereitstellung Sie können nicht mithilfe des Befehls **Enable-Mailbox AutoExpandingArchive** aktivieren erweiterbares Archivierung für bestimmte eines Benutzers, dessen Hauptpostfach lokal ist, und deren Archivpostfach ist Cloud-basierten. Zum Aktivieren der automatischen Erweitern Archivierung für cloudbasierte archivpostfächer in einer Exchange-hybridbereitstellung müssen Sie den Befehl **Set-OrganizationConfig AutoExpandingArchive** in Exchange Online PowerShell zum Aktivieren der automatischen Erweitern für Archivierung ausgeführt die gesamte Organisation. Wenn ein Benutzer der primären und cloudbasierte archivpostfächer sind, klicken Sie dann können den Befehl **Enable-Mailbox-AutoExpandingArchive** Sie erweiterbares für diesen Benutzer bestimmte Archivierung aktiviert werden. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>Stellen Sie sicher, dass erweiterbares Archivierung aktiviert ist

Um sicherzustellen, dass für Ihre Organisation die Archivierung erweiterbares aktiviert ist, führen Sie den folgenden Befehl in Exchange Online PowerShell aus.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

Der Wert `True` gibt an, dass automatisch erweitert Archivierung für die Organisation aktiviert ist. 
  
Führen Sie den folgenden Befehl um zu überprüfen, dass erweiterbares Archivierung aktivieren für einen bestimmten Benutzer ist, in Exchange Online PowerShell.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
Der Wert `True` gibt an, dass automatisch erweitert Archivierung für den Benutzer aktiviert ist. 
  
Nach dem Aktivieren der Archivierung automatisch erweitert, beachten Sie Folgendes beachten:
  
- Wenn Sie den Befehl **Set-OrganizationConfig AutoExpandingArchive** erweiterbares Archivierung für Ihre Organisation aktivieren ausführen, müssen Sie die **Enable-Mailbox-AutoExpandingArchive** für einzelne Postfächer ausführen. Beachten Sie, mit dem Cmdlet **Set-OrganizationConfig** erweiterbares Archivierung für Ihre Organisation die *AutoExpandingArchiveEnabled* -Eigenschaft auf Benutzerpostfächer zu ändern, nicht aktiviert `True`.
    
- In ähnlicher Weise werden nicht die Werte für die Postfacheigenschaften *ArchiveQuota* und *ArchiveWarningQuota* geändert, wenn Sie automatisch erweitert Archivierung zu aktivieren. Tatsächlich, wenn Sie automatisch erweitert für ein Benutzerpostfach Archivierung aktiviert werden und die *AutoExpandingArchiveEnabled* -Eigenschaft ist auf `True`, werden nur die Eigenschaften *ArchiveQuota* und *ArchiveWarningQuota* ignoriert. Es folgt ein Beispiel dieser Eigenschaften Postfach nach erweiterbares Archivierung für ein Benutzerpostfach aktiviert ist. 
    
    ![ArchiveQuota und ArchiveWarningQuota Eigenschaften werden ignoriert, nachdem Sie die Archivierung erweiterbares aktiviert](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>Weitere Informationen

- Sie können auch PowerShell verwenden, um archivpostfächer zu aktivieren. Beispielsweise können Sie den folgenden Befehl in Exchange führen Online PowerShell, um archivpostfächer für alle Benutzer zu aktivieren, deren Archivpostfach nicht bereits aktiviert ist.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- Nachdem Sie erweiterbares Archivierung für Ihre Organisation oder für einen bestimmten Benutzer einschalten, wird ein Archivpostfach in ein Archiv automatisch erweitert konvertiert, wenn das Archivpostfach (einschließlich des Ordners wiederherstellbare Elemente) 90 GB erreicht. Es kann bis zu 30 Tage für den zusätzlichen Speicherplatz bereitgestellt werden.
    
- Nachdem Sie erweiterbares Archivierung einschalten, kann nicht deaktiviert werden..
    
- Erweiterbares Archivierung wird für cloudbasierte archivpostfächer in einer Exchange-hybridbereitstellung für Benutzer unterstützt, die über einen lokalen primären Postfach verfügen. Jedoch nach erweiterbares Archivierung für ein cloudbasiertes Archivpostfach aktiviert ist, Sie können nicht deaktiviert-, Archivpostfach wieder auf den lokalen Exchange-Organisation Board.
    
- Eine Liste der Outlook-Clients, mit denen Benutzer Elemente im Bereich zusätzlicher Speicher in ihre Archivpostfach zugreifen, finden Sie im Anforderungsabschnitt "Outlook-für den Zugriff auf Elemente in einem Archiv automatisch erweitert" [Übersicht über unbegrenzte](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) Archivierung in Office 365 .
    
- Wie bereits erläutert, das Speicherkontingent des primären Archivpostfach des Benutzers 10 GB hinzugefügt wird (und in den Ordner wiederherstellbare Elemente, wenn das Postfach befindet sich auf halten) Wenn Sie **Enable-Mailbox AutoExpandingArchive** führen den Befehl aus. Dadurch wird zusätzlichen Speicher, bis der automatische erweitert Speicherplatz bereitgestellt wird (der bis zu 30 Tage dauern kann). Diese zusätzlichen Speicherplatz wird nicht hinzugefügt, wenn Sie das **Set-OrganizationConfig AutoExpandingArchive** zum Aktivieren der Archivierung automatisch erweitert, für alle Postfächer in Ihrer Organisation ausführen. Wenn Sie automatisch erweitert Archivierung für die gesamte Organisation aktiviert, jedoch die zusätzliche 10 GB Speicherplatz für einen bestimmten Benutzer hinzufügen müssen, können Sie den Befehl **Enable-Mailbox-AutoExpandingArchive** für dieses Postfach ausführen. Beachten Sie, dass eine besagt Fehlermeldung wird, dass die Archivierung automatisch erweitert wurde bereits aktiviert, doch der zusätzlichen Speicherplatz wird an das Postfach hinzugefügt werden. 

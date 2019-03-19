---
title: Aktivieren der unbegrenzten Archivierung in Office 365 – Administratorhilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: 'Für Administratoren: erfahren Sie, wie Sie die automatische Erweiterung der Archivierung in Office 365 aktivieren, sodass Ihre Benutzer unbegrenzten Speicherplatz für Ihre Exchange Online-Postfächer bereitstellen können. Sie können die automatische Erweiterung der Archivierung für Ihre gesamte Organisation oder nur für bestimmte Benutzer aktivieren.'
ms.openlocfilehash: 634807a687a8ccbb764a54300f338263f876b604
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670620"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Aktivieren der unbegrenzten Archivierung in Office 365 – Administratorhilfe

Sie können das Feature für die automatische Erweiterung der Exchange Online-Archivierung in Office 365 verwenden, um unbegrenzten Speicherplatz für Archivpostfächer zu aktivieren. Wenn die automatische Vergrößerung der Archivierung aktiviert ist, wird dem Archivpostfach eines Benutzers automatisch zusätzlicher Speicherplatz hinzugefügt, wenn der Speichergrenzwert erreicht wird. Das Ergebnis ist unbegrenzte Speicherkapazität für Postfächer. Sie können die automatische Erweiterung der Archivierung für alle Personen in Ihrer Organisation oder nur für bestimmte Benutzer aktivieren. Weitere Informationen zur automatischen Erweiterung der Archivierung finden Sie unter [Übersicht über die unbegrenzte Archivierung in Office 365](unlimited-archiving.md).

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation oder ein Mitglied der Rollengruppe "Organisationsverwaltung" in Ihrer Exchange Online-Organisation sein, um die automatische Erweiterung der Archivierung für Ihre gesamte Organisation oder für bestimmte Benutzer zu aktivieren. Alternativ müssen Sie Mitglied einer Rollengruppe sein, der die Rolle e-Mail-Empfänger zugewiesen ist, um die automatische Erweiterung der Archivierung für bestimmte Benutzer zu aktivieren.
    
- Das Archivpostfach eines Benutzers muss aktiviert sein, bevor Sie die automatische Erweiterung der Archivierung aktivieren können. Einem Benutzer muss eine Exchange Online-Plan 2-Lizenz zugewiesen sein, um das Archivpostfach zu aktivieren. Wenn einem Benutzer eine Exchange Online-Plan 1-Lizenz zugewiesen ist, müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, um das Archivpostfach zu aktivieren. Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md).
    
- Sie können auch PowerShell verwenden, um Archivpostfächer zu aktivieren. Im Abschnitt [Weitere Informationen](#more-information) finden Sie ein Beispiel für den PowerShell-Befehl, mit dem Sie Archivpostfächer für alle Benutzer in Ihrer Organisation aktivieren können. 
    
- Die Archivierung mit automatischer Erweiterung unterstützt auch freigegebene Postfächer. Zum Aktivieren des Archivs für ein freigegebenes Postfach ist eine Exchange Online-Lizenz für den Plan 2 oder eine Exchange Online-Plan 1-Lizenz mit einer Exchange Online-Archivierungslizenz erforderlich.
    
- Sie können das Exchange Admin Center oder das Security &amp; Compliance Center nicht verwenden, um die automatische Erweiterung der Archivierung zu aktivieren. Sie müssen Exchange Online PowerShell verwenden. Informationen zum Herstellen einer Verbindung mit Ihrer Exchange Online-Organisation mithilfe von Remote-PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>Aktivieren der automatischen Erweiterung der Archivierung für Ihre gesamte Organisation

Sie können die automatische Erweiterung der Archivierung für Ihre gesamte Organisation aktivieren. Nachdem Sie es aktiviert haben, wird die automatische Vergrößerung der Archivierung für vorhandene Benutzerpostfächer und für neue Benutzerpostfächer, die erstellt werden. Wenn Sie neue Benutzerpostfächer erstellen, müssen Sie unbedingt das Hauptarchiv Postfach des Benutzers aktivieren, damit das Feature für die automatische Erweiterung der Archivierung für das neue Benutzerpostfach funktioniert.
  
1. [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um die automatische Erweiterung der Archivierung für Ihre gesamte Organisation zu aktivieren.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>Aktivieren der automatischen Erweiterung der Archivierung für bestimmte Benutzer

Anstatt die automatische Erweiterung der Archivierung für alle Benutzer in Ihrer Organisation zu aktivieren, können Sie Sie nur für bestimmte Benutzer zulassen. Sie können dies tun, da nur einige Benutzer möglicherweise einen sehr großen Archivspeicher benötigen.
  
Wenn Sie die automatische Erweiterung der Archivierung für einen bestimmten Benutzer aktivieren und das Postfach des Benutzers im Wartestatus oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen sind, werden die folgenden beiden Konfigurationsänderungen vorgenommen:
  
- Das Speicherkontingent für das primäre Archivpostfach des Benutzers wird um 10 GB (von 100 GB auf 110 GB) erhöht. Das Kontingent für die Archiv Warnung wird ebenfalls um 10 GB (von 90 GB auf 100 GB) erhöht.
    
- Das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers wird um 10 GB (auch von 100 GB auf 110 GB) erhöht. Das Kontingent "Wiederherstellbare Elemente" wird ebenfalls um 10 GB (von 90 GB auf 100 GB) erhöht. Diese Änderungen gelten nur, wenn das Postfach in der Warteschleife oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen ist.
    
Dieser zusätzliche Speicherplatz wird hinzugefügt, um Speicherprobleme zu vermeiden, die auftreten können, bevor das automatisch expandierende Archiv bereitgestellt wird. Beachten Sie, dass zusätzlicher Speicherplatz nicht hinzugefügt *wird* , wenn Sie die automatische Erweiterung der Archivierung für Ihre gesamte Organisation aktivieren, wie im vorherigen Abschnitt beschrieben. 
  
1. [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um die automatische Erweiterung der Archivierung für einen bestimmten Benutzer zu aktivieren. Wie bereits erläutert, muss das Archivpostfach des Benutzers (Hauptarchiv) aktiviert sein, bevor Sie die automatische Erweiterung der Archivierung für diesen Benutzer aktivieren können.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> In einer Exchange-hybridbereitstellung können Sie den Befehl **Enable-Mailbox-AutoExpandingArchive** nicht verwenden, um die automatische Erweiterung der Archivierung für einen bestimmten Benutzer zu aktivieren, dessen primäres Postfach lokal ist und dessen Archivpostfach Cloud-basiert ist. Um die automatische Erweiterung der Archivierung für Cloud-basierte Archivpostfächer in einer Exchange-hybridbereitstellung zu aktivieren, müssen Sie den Befehl **Set-OrganizationConfig-AutoExpandingArchive** in Exchange Online PowerShell ausführen, um die automatische Erweiterung der Archivierung für die gesamte Organisation. Wenn die primären und Archivpostfächer eines Benutzers Cloud-basiert sind, können Sie den Befehl **Enable-Mailbox-AutoExpandingArchive** verwenden, um die automatische Erweiterung der Archivierung für diesen bestimmten Benutzer zu aktivieren. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>Sicherstellen, dass die automatische Erweiterung der Archivierung aktiviert ist

Führen Sie in Exchange Online PowerShell den folgenden Befehl aus, um zu überprüfen, ob die automatische Erweiterung der Archivierung für Ihre Organisation aktiviert ist.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

Ein Wert von `True` gibt an, dass die automatische Erweiterung der Archivierung für die Organisation aktiviert ist. 
  
Führen Sie in Exchange Online PowerShell den folgenden Befehl aus, um zu überprüfen, ob die automatische Erweiterung der Archivierung für einen bestimmten Benutzer aktiviert ist.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
Ein Wert von `True` gibt an, dass die automatische Erweiterung der Archivierung für den Benutzer aktiviert ist. 
  
Halten Sie die folgenden Dinge im Hinterkopf, nachdem Sie die automatische Erweiterung der Archivierung aktiviert haben:
  
- Wenn Sie den Befehl **Set-OrganizationConfig-AutoExpandingArchive** ausführen, um die automatische Erweiterung der Archivierung für Ihre Organisation zu aktivieren, müssen Sie das **Enable-Mailbox-AutoExpandingArchive** für einzelne Postfächer nicht ausführen. Beachten Sie, dass die *AutoExpandingArchiveEnabled* -Eigenschaft für Benutzerpostfächer in nicht geändert wird, wenn Sie das Cmdlet **Set-OrganizationConfig** ausführen, um `True`die automatische Erweiterung der Archivierung für Ihre Organisation zu aktivieren.
    
- Entsprechend werden die Werte für die *ArchiveQuota* -und *ArchiveWarningQuota* -Postfacheigenschaften nicht geändert, wenn Sie die automatische Erweiterung der Archivierung aktivieren. Wenn Sie die automatische Erweiterung der Archivierung für ein Benutzerpostfach aktivieren und die *AutoExpandingArchiveEnabled* `True`-Eigenschaft auf festgelegt ist, werden die Eigenschaften *ArchiveQuota* und *ArchiveWarningQuota* einfach ignoriert. Nachfolgend finden Sie ein Beispiel für diese Postfacheigenschaften, nachdem die automatische Erweiterung der Archivierung für das Postfach eines Benutzers aktiviert wurde. 
    
    ![ArchiveQuota-und ArchiveWarningQuota-Eigenschaften werden ignoriert, nachdem Sie die automatische Erweiterung der Archivierung aktiviert haben.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>Weitere Informationen

- Sie können auch PowerShell verwenden, um Archivpostfächer zu aktivieren. Sie können beispielsweise den folgenden Befehl in Exchange Online PowerShell ausführen, um Archivpostfächer für alle Benutzer zu aktivieren, deren Archivpostfach noch nicht aktiviert ist.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- Nachdem Sie die automatische Erweiterung der Archivierung für Ihre Organisation oder für einen bestimmten Benutzer aktiviert haben, wird ein Archivpostfach in ein automatisch erweiterbares Archiv konvertiert, wenn das Archivpostfach (einschließlich des Ordners "Wiederherstellbare Elemente") 90 GB erreicht. Es kann bis zu 30 Tage dauern, bis der zusätzliche Speicherplatz zur Verfügung steht.
    
- Nachdem Sie die automatische Erweiterung der Archivierung aktiviert haben, kann Sie nicht deaktiviert werden.
    
- Die automatische Erweiterung der Archivierung wird für Cloud-basierte Archivpostfächer in einer Exchange-hybridbereitstellung für Benutzer unterstützt, die über ein lokales primäres Postfach verfügen. Nachdem die automatische Erweiterung der Archivierung für ein cloudbasierten Archivpostfach aktiviert wurde, können Sie dieses Archivpostfach jedoch nicht mehr an die lokale Exchange-Organisation zurücksenden. Beachten Sie, dass die automatische Erweiterung der Archivierung für lokale Postfächer in Exchange Server 2010 nicht unterstützt wird.
    
- Eine Liste der Outlook-Clients, die Benutzer für den Zugriff auf Elemente im zusätzlichen Speicherbereich in Ihrem Archivpostfach verwenden können, finden Sie im Abschnitt "Outlook-Anforderungen für den Zugriff auf Elemente in einem automatisch erweiterten Archiv" unter [Übersicht über unbegrenzte Archivierung in Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) .
    
- Wie bereits erläutert, werden 10 GB dem Speicherkontingent des primären Archivpostfachs des Benutzers (und dem Ordner "Wiederherstellbare Elemente", wenn das Postfach in der Warteschleife ist) hinzugefügt, wenn Sie den Befehl **Enable-Mailbox-AutoExpandingArchive** ausführen. Dies bietet zusätzlichen Speicher, bis der automatisch erweiterte Speicherplatz bereitgestellt wird (Dies kann bis zu 30 Tage dauern). Dieser zusätzliche Speicherplatz wird nicht hinzugefügt, wenn Sie das **Set-OrganizationConfig-AutoExpandingArchive** ausführen, um die automatische Erweiterung der Archivierung für alle Postfächer in Ihrer Organisation zu aktivieren. Wenn Sie die automatische Erweiterung der Archivierung für die gesamte Organisation aktiviert haben, aber die zusätzlichen 10 GB Speicherplatz für einen bestimmten Benutzer hinzufügen müssen, können Sie den Befehl **Enable-Mailbox-AutoExpandingArchive** für dieses Postfach ausführen. Beachten Sie, dass Sie eine Fehlermeldung erhalten, dass die automatische Erweiterung der Archivierung bereits aktiviert wurde, der zusätzliche Speicherplatz dem Postfach jedoch hinzugefügt wird. 

- Administratoren können das Speicherkontingent nicht anpassen.

> [!IMPORTANT]
> Die automatische Erweiterung der Archivierung wird nur für Postfächer unterstützt, die für einzelne Benutzer oder freigegebene Postfächer mit einer Wachstumsrate verwendet werden, die 1 GB pro Tag nicht überschreitet. Das Verwenden von Journaling, Transportregeln oder Regeln für die automatische Weiterleitung zum Kopieren von Nachrichten in ein Archivpostfach zum Zwecke der Archivierung ist nicht zulässig. Das Archivpostfach eines Benutzers ist nur für diesen Benutzer vorgesehen. Microsoft behält sich das Recht vor, die uneingeschränkte Archivierung dann zu verweigern, wenn das Archivpostfach eines Benutzers zum Speichern von Archivdaten für andere Benutzer verwendet wird.

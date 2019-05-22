---
title: Aktivieren von Archivpostfächern im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Im Security & Compliance Center in Office 365 können Sie Archivpostfächer aktivieren, um den Anforderungen Ihrer Organisation hinsichtlich Nachrichtenarchivierung, eDiscovery und Aufbewahrung gerecht zu werden.
ms.openlocfilehash: 5cf399b311b6c342aff2d84477edaa945f8e0cd4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153287"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a>Aktivieren von Archivpostfächern im Security & Compliance Center
  
Durch die Archivierung in Office 365 (auch In-Situ-Archivierung genannt) erhalten Benutzer zusätzlichen Speicherplatz im Postfach. Nach Aktivierung der Archivpostfächer können Benutzer über Microsoft Outlook und Outlook im Web (früher als Outlook Web App bezeichnet) auf Nachrichten in ihren Archivpostfächern zugreifen und sie dort speichern. Benutzer können auch Nachrichten zwischen dem primären Postfach und dem Archivpostfach kopieren oder verschieben. Mit der Wiederherstellung gelöschter Elemente können die Benutzer darüber hinaus gelöschte Elemente aus dem Ordner „Gelöschte Elemente“ in ihrem Archivpostfach wiederherstellen. 
  
> [!TIP]
> Office 365 bietet mit dem automatisch erweiternden Archiv eine unbegrenzte Menge an Archivspeicher. Wenn das automatisch erweiternde Archiv aktiviert ist und das anfängliche Speicherkontingent im Archivpostfach eines Benutzers erreicht wird, fügt Office 365 automatisch weiteren Speicherplatz hinzu. Dies bedeutet, dass den Benutzern niemals der Postfachspeicherplatz ausgeht und Sie im Grunde nichts weiter tun müssen, nachdem Sie das Archivpostfach eingerichtet und die automatische Erweiterung für Ihre Organisation aktiviert haben. Weitere Informationen finden Sie unter [Übersicht zur unbeschränkten Archivierung in Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Ihnen muss die Rolle "E-Mail-Empfänger" in Exchange Online zugewiesen sein, damit Sie Archivpostfächer aktivieren oder deaktivieren können. Standardmäßig ist diese Rolle den Rollengruppen "Empfängerverwaltung" und "Organisationsverwaltung" auf der Seite **Berechtigungen** im Exchange Admin Center zugewiesen. Wenn die Seite **Archiv** im Security & Compliance Center nicht angezeigt wird, bitten Sie Ihren Administrator, Ihnen die notwendigen Berechtigungen zuzuweisen. 
  
## <a name="enable-an-archive-mailbox"></a>Aktivieren eines Archivpostfachs
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Geschäfts- oder Schul-/Unikonto bei Office 365 an.
    
3. Klicken Sie im Security & Compliance Center im linken Bereich auf **Data Governance** \> **Archiv**.
    
    Die Seite **Archiv** wird angezeigt. In der Spalte **Archivpostfach** ist angegeben, ob für den jeweiligen Benutzer ein Archivpostfach aktiviert bzw. deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie aktivieren möchten.
    
    ![Klicken Sie im Detailbereich des ausgewählten Benutzers auf "Aktivieren", um das Archivpostfach zu aktivieren](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Klicken Sie im Detailbereich des ausgewählten Benutzers auf **Aktivieren**. 
    
    Es wird eine Warnung angezeigt, dass bei einer Aktivierung des Archivpostfachs Elemente im Postfach des Benutzers, die älter sind, als es in der dem Postfach zugewiesenen Archivierungsrichtlinie festgelegt ist, in das neue Archivpostfach verschoben werden. Durch die Standardarchivierungsrichtlinie, die Teil der den Exchange Online-Postfächern zugewiesenen Aufbewahrungsrichtlinie ist, werden Elemente zwei Jahre nach dem Datum, an dem sie an das Postfach übermittelt oder vom Benutzer erstellt wurden, in das Archivpostfach verschoben werden. Weitere Informationen finden Sie im Abschnitt **Weitere Informationen** dieses Artikels. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu aktivieren. 
    
    Das Erstellen des Archivpostfachs kann eine kurze Zeit dauern. Nachdem das Archivpostfach erstellt wurde, wird im Detailbereich für den ausgewählten Benutzer **Archivpostfach: Aktiviert** angezeigt. Sie müssen möglicherweise auf **Aktualisieren** ![Aktualisieren-Symbol](media/O365-MDM-Policy-RefreshIcon.gif) klicken, um die Informationen im Detailbereich zu aktualisieren. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig aktivieren, indem Sie mehrere Benutzer mit deaktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Aktivieren**. 
  
## <a name="disable-an-archive-mailbox"></a>Deaktivieren eines Archivpostfachs
  
Sie können auch die Seite **Archiv** im Security & Compliance Center verwenden, um das Archivpostfach eines Benutzers zu deaktivieren. Nachdem Sie ein Archivpostfach deaktiviert haben, können Sie es innerhalb von 30 Tagen nach der Deaktivierung wieder mit dem primären Postfach des Benutzers verbinden. In diesem Fall wird der ursprüngliche Inhalt des Archivpostfachs wiederhergestellt. Nach Ablauf von 30 Tagen wird der Inhalt des ursprünglichen Archivpostfachs endgültig gelöscht und kann nicht wiederhergestellt werden. Wenn Sie das Archiv also erst nach über 30 Tagen erneut aktivieren, nachdem Sie es deaktiviert haben, wird ein neues Archivpostfach erstellt. 
  
Beachten Sie, dass Elemente aufgrund der Standardarchivierungsrichtlinie für Benutzerpostfächer zwei Jahre nach ihrem Empfang in das Archivpostfach verschoben werden. Wenn Sie das Archivpostfach eines Benutzers deaktivieren, wird keine Aktion mit den Postfachelementen durchgeführt, und diese verbleiben im primären Postfach des Benutzers.
  
So deaktivieren Sie ein Archivpostfach:
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Geschäfts- oder Schul-/Unikonto bei Office 365 an.
    
3. Klicken Sie im Security & Compliance Center im linken Bereich auf **Data Governance** \> **Archiv**.
    
    Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie deaktivieren möchten.
    
5. Klicken Sie im Detailbereich auf **Deaktivieren**. 
    
    Es wird eine Warnung angezeigt, die darauf hinweist, dass Sie 30 Tage Zeit haben, das Archivpostfach wieder zu aktivieren und dass nach 30 Tagen sämtliche Informationen im Archiv dauerhaft gelöscht werden. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu deaktivieren. 
    
    Das Deaktivieren des Archivpostfachs kann eine kurze Zeit dauern. Nachdem das Archivpostfach deaktiviert wurde, wird im Detailbereich für den ausgewählten Benutzer **Archivpostfach: Deaktiviert** angezeigt. Sie müssen möglicherweise auf **Aktualisieren** ![Aktualisieren-Symbol](media/O365-MDM-Policy-RefreshIcon.gif) klicken, um die Informationen im Detailbereich zu aktualisieren. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig deaktivieren, indem Sie mehrere Benutzer mit aktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Deaktivieren**. 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Verwenden von Exchange Online PowerShell zum Aktivieren oder Deaktivieren von Archivpostfächern

Alternativ können Sie Archivpostfächer auch mithilfe von Exchange Online PowerShell aktivieren. Der Hauptgrund für die Verwendung von PowerShell besteht darin, dass Sie schnell das Archivpostfach für alle Benutzer in Ihrer Organisation aktivieren können.

Im ersten Schritt müssen Sie eine Verbindung mit Exchange Online PowerShell herstellen. Anleitungen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

Nachdem Sie eine Verbindung mit Exchange Online hergestellt haben, können Sie die Befehle in den folgenden Abschnitten ausführen, um Archivpostfächer zu aktivieren bzw. zu deaktivieren.

### <a name="enable-archive-mailboxes"></a>Aktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu aktivieren.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu aktivieren, deren Archivpostfach aktuell nicht aktiviert ist.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>Deaktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu deaktivieren.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um die Archivpostfächer aller Benutzer in Ihrer Organisation zu deaktivieren (deren Archivpostfach aktuell aktiviert ist).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>Weitere Informationen
  
- Mit aktiviertem Archivpostfach können Benutzer Nachrichten in ihrem Archivpostfach speichern. Die Benutzer können mit Microsoft Outlook und Outlook im Web auf ihre Archivpostfächer zugreifen. Durch Verwendung einer dieser Clientanwendungen können die Benutzer Nachrichten in ihrem Archivpostfach anzeigen und zwischen ihrem primären Postfach und dem Archivpostfach kopieren oder verschieben. Mit der Wiederherstellung gelöschter Elemente können die Benutzer darüber hinaus gelöschte Elemente aus dem Ordner „Gelöschte Elemente“ in ihrem Archivpostfach wiederherstellen.

   Eine Liste der Outlook-Lizenzen, die In-Situ-Archivierung unterstützen, finden Sie unter [Outlook-Lizenzanforderungen für Exchange-Features](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).

- Archivpostfächer unterstützen Sie und Ihre Benutzer auch bei der Erfüllung der Anforderungen Ihrer Organisation hinsichtlich Aufbewahrung, eDiscovery und Archivierung. Sie können beispielsweise die Exchange-Aufbewahrungsrichtlinie Ihrer Organisation dazu verwenden, Postfachinhalte in das Archivpostfach eines Benutzers zu verschieben. Wenn Sie das Tool für die Inhaltssuche im Security & Compliance Center verwenden, um das Postfach eines Benutzers nach bestimmten Inhalten zu durchsuchen, wird auch das Archivpostfach des Benutzers durchsucht. Wenn Sie die Aufbewahrung für eventuelle Rechtsstreitigkeiten aktivieren oder eine Office 365-Aufbewahrungsrichtlinie auf das Postfach eines Benutzers anwenden, werden die Elemente im Archivpostfach ebenfalls aufbewahrt.
  
- Sind die Archivpostfächer aktiviert, kann Ihre Organisation die standardmäßige Exchange-Aufbewahrungsrichtlinie (auch als Richtlinie zur Verwaltung von Nachrichtendatensätzen bezeichnet) nutzen, die jedem Postfach automatisch zugewiesen wird. Wenn ein Archivpostfach aktiviert ist, führt die standardmäßige Exchange-Aufbewahrungsrichtlinie automatisch Folgendes aus: 
  
    - Verschieben von Elementen, die 2 Jahre alt oder älter sind, aus dem primären Postfach eines Benutzers in dessen Archivpostfach 
    
    - Verschieben von Elementen, die 14 Tage alt oder älter sind, aus dem Ordner „Wiederherstellbare Elemente“ im primären Postfach des Benutzers zum Ordner „Wiederherstellbare Elemente“ im Archivpostfach .
    
- Weitere Informationen zu Archivpostfächern und Exchange-Aufbewahrungsrichtlinien finden Sie hier:
    
  - [Aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Standardaufbewahrungsrichtlinie in Exchange Online ](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Einrichten einer Archivierungs- und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation](set-up-an-archive-and-deletion-policy-for-mailboxes.md)

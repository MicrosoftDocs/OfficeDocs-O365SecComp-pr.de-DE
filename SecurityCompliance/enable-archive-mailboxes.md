---
title: Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Verwenden Sie die Office 365-Sicherheit &amp; Compliance Center um archivpostfächer zur Unterstützung Ihrer Organisation, Beibehaltung von eDiscovery, und halten Sie Anforderungen zu aktivieren.
ms.openlocfilehash: 1c290cf19b396221dac702efd1395911e8a51631
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327097"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a>Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center
  
Archivierung in Office 365 (auch als Compliance-Archivierung bezeichnet) bietet Benutzern zusätzliche Postfach Speicherplatz. Nachdem Sie archivpostfächer aktivieren, Benutzer zugreifen und Speichern von Nachrichten in ihren archivpostfächern mithilfe von Microsoft Outlook und Outlook Web App-Benutzer können auch verschieben oder Kopieren von Nachrichten zwischen ihren primären Postfachs und deren Archivpostfach. Sie können auch aus dem Ordner wiederherstellbare Elemente in ihrem Archivpostfach gelöschte Elemente wiederherstellen, mit dem Tool gelöschte Elemente wiederherstellen. 
  
> [!TIP]
> Office 365 bietet eine unbegrenzte Zeitspanne Archivspeicher mit dem erweiterbares Archivierung Feature. Wenn erweiterbares Archivierung aktiviert ist, und klicken Sie dann das anfängliche Speicherkontingent im Archivpostfach des Benutzers erreicht ist, fügt zusätzlichen Speicherplatz automatisch von Office 365 hinzu. Dies bedeutet, die Benutzer werden nicht ausgeführt, nicht genügend Speicherplatz Postfach und Sie müssen nicht alles zunächst nach der verwalten aktivieren das Archivpostfach und schalten Sie erweiterbares Archivierung für Ihre Organisation. Weitere Informationen finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen:

Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zu aktivieren oder Deaktivieren von archivpostfächern zugewiesen werden. Standardmäßig wird diese Rolle Rollengruppen "Recipient Management" und "Organisationsverwaltung" auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole zugewiesen. Wenn Sie die Seite **Archiv** in das Wertpapier sehen &amp; Compliance Center, bitten Sie Ihren Administrator, um Sie über die erforderlichen Berechtigungen zuweisen. 
  
## <a name="enable-an-archive-mailbox"></a>Aktivieren eines Archivpostfachs
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Archiv**.
    
    Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie aktivieren möchten.
    
    ![Klicken Sie im Detailbereich des ausgewählten Benutzers an das Archivpostfach aktivieren auf Aktivieren](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Klicken Sie im Detailbereich für den ausgewählten Benutzer auf **Aktivieren**. 
    
    Eine Warnung wird angezeigt, die besagt, dass Elemente im Postfach des Benutzers, die älter sind als die Archivierungsrichtlinie Postfach zugeordnet sind, wenn Sie das Archivpostfach aktivieren, in das neue Archivpostfach verschoben werden sollen. Die Standardrichtlinie für das Archivieren, die Teil der Aufbewahrungsrichtlinie zu Exchange Online-Postfächern zugewiesen ist Verschiebt Elemente in das Archivpostfach zwei Jahre nach dem Datum, das der Artikel an das Postfach zugestellt oder vom Benutzer erstellt wurde. Weitere Informationen finden Sie im Abschnitt **Weitere Informationen** in diesem Artikel. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu aktivieren. 
    
    Es kann einen Moment, erstellen Sie das Archivpostfach dauern. Bei der Erstellung, **Archivpostfach: aktiviert** wird im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie auf **Aktualisieren** klicken ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig aktivieren, indem Sie mehrere Benutzer mit deaktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Aktivieren**. 
  
## <a name="disable-an-archive-mailbox"></a>Deaktivieren eines Archivpostfachs
  
Sie können auch die Seite **Archiv** in das Wertpapier &amp; Compliance Center Archivpostfach des Benutzers zu deaktivieren. Wenn Sie ein Archivpostfach deaktiviert haben, können Sie sie zum primären Postfach des Benutzers innerhalb von 30 Tagen deaktivieren sie wieder herstellen. In diesem Fall werden der ursprüngliche Inhalt des archivpostfachs wiederhergestellt. Nach 30 Tagen wird der Inhalt des ursprünglichen archivpostfachs werden dauerhaft gelöscht und können nicht wiederhergestellt werden. Damit wird Sie das Archiv mehr als 30 Tage nach dem Deaktivieren wieder zu aktivieren, eine neue Archivpostfach erstellt. 
  
Beachten Sie, dass die Standardrichtlinie für die Archivierung, den Postfächern der Benutzer verschiebt Elemente in das Archivpostfach zwei Jahre nach dem Datum das Element zugewiesen wird übermittelt. Wenn Sie dem Postfach eines Benutzers archivieren deaktivieren, auf Postfachelemente wird keine Aktion ausgeführt werden, und bleiben sie in der primären Postfach des Benutzers.
  
Um ein Archivpostfach zu deaktivieren:
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Archiv**.
    
    Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie deaktivieren möchten.
    
5. Klicken Sie im Detailbereich auf **Deaktivieren**. 
    
    Eine Warnmeldung wird angezeigt, sagen, dass Sie 30 Tage bis das Archivpostfach erneut aktivieren müssen, und nach 30 Tagen alle Informationen in das Archiv dauerhaft gelöscht werden. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu deaktivieren. 
    
    Es kann einen Moment, deaktivieren Sie das Archivpostfach dauern. Wenn es deaktiviert ist, **Archivpostfach: deaktiviert** wird im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie auf **Aktualisieren** klicken ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig deaktivieren, indem Sie mehrere Benutzer mit aktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Deaktivieren**. 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Verwenden von Exchange Online PowerShell aktivieren oder Deaktivieren von archivpostfächern

Sie können auch Exchange Online PowerShell verwenden, um archivpostfächer zu aktivieren. Der Hauptgrund-PowerShell verwendet wird, dass Sie schnell das Archivpostfach für alle Benutzer in Ihrer Organisation aktivieren können.

Der erste Schritt besteht Verbindung mit Exchange Online PowerShell. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

Nachdem Sie Exchange Online verbunden sind, können Sie die Befehle in den folgenden Abschnitten zum Aktivieren oder Deaktivieren von archivpostfächern ausführen.

### <a name="enable-archive-mailboxes"></a>Aktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu aktivieren.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu aktivieren (, deren Archivpostfach derzeit nicht aktiviert ist).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>Deaktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu deaktivieren.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu deaktivieren (, deren Archivpostfach derzeit aktiviert ist).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>Weitere Informationen
  
- Archivpostfächer helfen Ihnen und den Benutzern Ihrer Organisation Aufbewahrung, eDiscovery, erfüllen und halten Sie Anforderungen. Beispielsweise können Sie Ihrer Organisation Exchange Aufbewahrungsrichtlinie Inhalt von Postfächern in der Benutzer Archivpostfach verschieben. Bei Verwendung der Suchfunktion von Inhalten in das Wertpapier &amp; Compliance Center zum Suchen des Postfachs eines Benutzers nach bestimmten Inhalten, Archivpostfach des Benutzers wird auch durchsucht werden. Und wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren oder eine Office 365-Aufbewahrungsrichtlinie auf dem Postfach eines Benutzers anwenden, werden auch Elemente in das Archivpostfach beibehalten.
  
- Wenn ein Archivpostfach aktiviert ist, können Benutzer Nachrichten in ihrem Archivpostfach speichern. Benutzer können auf ihre archivpostfächer zugreifen mithilfe von Microsoft Outlook und Outlook Web App verwenden eine der folgenden Clientanwendungen, die Benutzer können Nachrichten in ihren Archivpostfach anzuzeigen und verschieben oder Kopieren von Nachrichten zwischen ihren primären Postfachs und deren Archivpostfach. Benutzer können auch gelöschte Elemente aus dem Ordner wiederherstellbare Elemente in ihrem Archivpostfach wiederherstellen, mit dem Tool gelöschte Elemente wiederherstellen. 
  
- Nach dem Archivieren Sie die Postfächer aktiviert sind, kann Ihre Organisation Exchange Standardaufbewahrungsrichtlinie (Messaging Records Management oder MRM-Richtlinie auch genannt) nutzen, die automatisch auf jedes Postfach zugeordnet ist. Wenn ein Archivpostfach aktiviert ist, führt der Exchange-Standardaufbewahrungsrichtlinie automatisch Folgendes aus: 
  
    - Verschieben von Elementen, die 2 Jahre alt oder älter sind, aus dem primären Postfach eines Benutzers in dessen Archivpostfach 
    
    - Verschieben von Elementen, die 14 Tage alt oder älter sind, aus dem Ordner „Wiederherstellbare Elemente" im primären Postfach des Benutzers zum Ordner „Wiederherstellbare Elemente" im Archivpostfach .
    
- Weitere Informationen zu archivpostfächer und Exchange-Aufbewahrungsrichtlinien finden Sie unter:
  
    
  - [Aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Default Aufbewahrungsrichtlinien in Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Richten Sie ein Archiv und Löschung Richtlinie für Postfächer in Ihrer Organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md)

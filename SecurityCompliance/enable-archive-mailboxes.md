---
title: Aktivieren von archivpostfächern im Office 365 &amp; Security Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Verwenden Sie das Office 365 &amp; Security Compliance Center, um Archivpostfächer zu aktivieren, um die Nachrichten Aufbewahrungs-, eDiscovery-und halte Anforderungen Ihrer Organisation zu unterstützen.
ms.openlocfilehash: 10e20d09c531d6758d8011030aea64a6c30cdf9b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217285"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a>Aktivieren von archivpostfächern im Office 365 &amp; Security Compliance Center
  
Die Archivierung in Office 365 (auch als in-Place-Archivierung bezeichnet) bietet Benutzern zusätzlichen Speicherplatz für Postfächer. Nachdem Sie Archivpostfächer aktiviert haben, können Benutzer mithilfe von Microsoft Outlook und Outlook im Web (früher als Outlook Web App bezeichnet) auf Nachrichten in ihren archivpostfächern zugreifen und diese speichern. Benutzer können auch Nachrichten zwischen Ihrem primären Postfach und Ihrem Archivpostfach verschieben oder kopieren. Sie können auch gelöschte Elemente aus dem Ordner "Wiederherstellbare Elemente" im Archivpostfach wiederherstellen, indem Sie das Tool "Gelöschte Elemente" verwenden. 
  
> [!TIP]
> Office 365 bietet eine unbegrenzte Menge an Archivspeicher mit der automatisch expandierenden Archivierungsfunktion. Wenn die automatische Erweiterung der Archivierung aktiviert ist und dann das anfängliche Speicherkontingent im Archivpostfach eines Benutzers erreicht wird, fügt Office 365 automatisch zusätzlichen Speicherplatz hinzu. Dies führt dazu, dass für die Benutzer kein Speicherplatz mehr zur Verfügung steht und Sie nach der anfänglichen Aktivierung des Archivpostfachs und der automatischen Erweiterung der Archivierung für Ihre Organisation nichts verwalten müssen. Weitere Informationen finden Sie unter [Übersicht über unbegrenzte Archivierung in Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden, um Archivpostfächer zu aktivieren oder zu deaktivieren. Diese Rolle wird standardmäßig den Rollengruppen "Empfängerverwaltung" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Wenn die Seite **Archiv** im Security &amp; Compliance Center nicht angezeigt wird, bitten Sie den Administrator, Ihnen die erforderlichen Berechtigungen zuzuweisen. 
  
## <a name="enable-an-archive-mailbox"></a>Aktivieren eines Archivpostfachs
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> **Archive**.
    
    Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie aktivieren möchten.
    
    ![Klicken Sie im Detailbereich des ausgewählten Benutzers auf aktivieren, um das Archivpostfach zu aktivieren.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Klicken Sie im Detailbereich für den ausgewählten Benutzer auf **aktivieren**. 
    
    Es wird eine Warnung angezeigt, dass beim Aktivieren des Archivpostfachs Elemente im Postfach des Benutzers, die älter als die dem Postfach zugewiesene Archivierungsrichtlinie sind, in das neue Archivpostfach verschoben werden. Die Standardarchiv Richtlinie, die Teil der Aufbewahrungsrichtlinie ist, die Exchange Online-Postfächern zugewiesen ist, verschiebt Elemente zwei Jahre nach dem Datum, an dem das Element an das Postfach zugestellt oder vom Benutzer erstellt wurde, in das Archivpostfach. Weitere Informationen finden Sie im Abschnitt **Weitere Informationen** in diesem Artikel. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu aktivieren. 
    
    Es kann einen Moment dauern, bis das Archivpostfach erstellt wurde. Wenn es erstellt wird, wird **Archivpostfach: aktiviert** im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie **** ![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Informationen im Detailbereich zu aktualisieren. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig aktivieren, indem Sie mehrere Benutzer mit deaktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Aktivieren**. 
  
## <a name="disable-an-archive-mailbox"></a>Deaktivieren eines Archivpostfachs
  
Sie können auch die Seite **Archiv** im Security &amp; Compliance Center verwenden, um das Archivpostfach eines Benutzers zu deaktivieren. Nachdem Sie ein Archivpostfach deaktiviert haben, können Sie es innerhalb von 30 Tagen nach der Deaktivierung wieder mit dem primären Postfach des Benutzers verbinden. In diesem Fall werden die ursprünglichen Inhalte des Archivpostfachs wiederhergestellt. Nach 30 Tagen werden die Inhalte des ursprünglichen Archivpostfachs dauerhaft gelöscht und können nicht wiederhergestellt werden. Wenn Sie das Archiv also mehr als 30 Tage nach dem Deaktivieren erneut aktivieren, wird ein neues Archivpostfach erstellt. 
  
Beachten Sie, dass die standardmäßigen archivrichtlinien, die den Postfächern von Benutzern zugewiesen sind, zwei Jahre nach dem Datum, an dem das Element zugestellt wurde, Elemente in das Archivpostfach verschieben Wenn Sie das Archivpostfach eines Benutzers deaktivieren, werden keine Aktionen für Postfachelemente durchgeführt, und Sie verbleiben im primären Postfach des Benutzers.
  
So deaktivieren Sie ein Archivpostfach
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> **Archive**.
    
    Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie deaktivieren möchten.
    
5. Klicken Sie im Detailbereich auf **Deaktivieren**. 
    
    Eine Warnmeldung wird angezeigt, die besagt, dass Sie 30 Tage Zeit haben, um das Archivpostfach wieder zu aktivieren, und dass nach 30 Tagen alle Informationen im Archiv dauerhaft gelöscht werden. 
    
6. Klicken Sie auf **Ja**, um das Archivpostfach zu deaktivieren. 
    
    Es kann einen Moment dauern, bis das Archivpostfach deaktiviert wurde. Wenn es deaktiviert ist, wird **Archivpostfach: deaktiviert** im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie **** ![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Informationen im Detailbereich zu aktualisieren. 
    
> [!TIP]
> Sie können auch mehrere Archivpostfächer gleichzeitig deaktivieren, indem Sie mehrere Benutzer mit aktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Deaktivieren**. 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Verwenden von Exchange Online PowerShell zum Aktivieren oder Deaktivieren von archivpostfächern

Sie können auch Exchange Online PowerShell verwenden, um Archivpostfächer zu aktivieren. Der Hauptgrund für die Verwendung von PowerShell besteht darin, dass Sie das Archivpostfach für alle Benutzer in Ihrer Organisation schnell aktivieren können.

Der erste Schritt besteht darin, eine Verbindung mit Exchange Online PowerShell herzustellen. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

Nachdem Sie eine Verbindung mit Exchange Online hergestellt haben, können Sie die Befehle in den folgenden Abschnitten ausführen, um Archivpostfächer zu aktivieren oder zu deaktivieren.

### <a name="enable-archive-mailboxes"></a>Aktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu aktivieren.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu aktivieren (deren Archivpostfach derzeit nicht aktiviert ist).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>Deaktivieren von Archivpostfächern

Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu deaktivieren.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu deaktivieren (deren Archivpostfach derzeit aktiviert ist).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>Weitere Informationen
  
- Archivpostfächer helfen Ihnen und ihren Benutzern, die Aufbewahrungs-, eDiscovery-und halte Anforderungen Ihrer Organisation zu erfüllen. Sie können beispielsweise die Exchange-Aufbewahrungsrichtlinie Ihrer Organisation verwenden, um Postfachinhalte in das Archivpostfach der Benutzer zu verschieben. Wenn Sie das Inhaltssuche-Tool im Security &amp; Compliance Center verwenden, um das Postfach eines Benutzers nach bestimmten Inhalten zu durchsuchen, wird auch das Archivpostfach des Benutzers durchsucht. Außerdem werden Elemente im Archivpostfach beibehalten, wenn Sie eine Aufbewahrungsrichtlinie für Office 365 auf das Postfach eines Benutzers anwenden.
  
- Wenn ein Archivpostfach aktiviert ist, können Benutzer Nachrichten in Ihrem Archivpostfach speichern. Benutzer können mithilfe von Microsoft Outlook und Outlook im Web auf Ihre Archivpostfächer zugreifen. Mithilfe einer dieser Clientanwendungen können Benutzer Nachrichten in Ihrem Archivpostfach anzeigen und Nachrichten zwischen Ihrem primären Postfach und Ihrem Archivpostfach verschieben oder kopieren. Benutzer können auch gelöschte Elemente aus dem Ordner "Wiederherstellbare Elemente" im Archivpostfach wiederherstellen, indem Sie das Tool "Gelöschte Elemente" verwenden. 
  
- Nachdem Archivpostfächer aktiviert wurden, kann Ihre Organisation die standardmäßige Exchange-Aufbewahrungsrichtlinie nutzen (auch als Messaging Records Management oder MRM Policy bezeichnet), die jedem Postfach automatisch zugewiesen wird. Wenn ein Archivpostfach aktiviert ist, führt die Exchange-Standardaufbewahrungsrichtlinie automatisch folgende Aktionen aus: 
  
    - Verschieben von Elementen, die 2 Jahre alt oder älter sind, aus dem primären Postfach eines Benutzers in dessen Archivpostfach 
    
    - Verschieben von Elementen, die 14 Tage alt oder älter sind, aus dem Ordner „Wiederherstellbare Elemente" im primären Postfach des Benutzers zum Ordner „Wiederherstellbare Elemente" im Archivpostfach .
    
- Weitere Informationen zu archivpostfächern und Exchange-Aufbewahrungsrichtlinien finden Sie unter:
  
    
  - [Aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Standardmäßige AufbewahrungsRichtlinie in Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Einrichten einer Archivierungs-und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation](set-up-an-archive-and-deletion-policy-for-mailboxes.md)

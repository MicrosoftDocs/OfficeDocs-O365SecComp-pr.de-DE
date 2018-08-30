---
title: Suchen und Löschen von e-Mail-Nachrichten in Ihrer Organisation für Office 365 - Admin-Hilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Verwenden Sie die Suche und leeren Feature in die Office 365-Sicherheit &amp; Compliance Center zu suchen und löschen eine e-Mail-Nachricht von alle Postfächer in Ihrer Organisation.
ms.openlocfilehash: 8bba4be473977afc229f64dfba6fd1514b86ecd2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529256"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Suchen und Löschen von e-Mail-Nachrichten in Ihrer Organisation für Office 365 - Admin-Hilfe

**Dieser Artikel ist für Administratoren. Versuchen Sie, um Elemente in Ihrem Postfach zu finden, die Sie löschen möchten? Finden Sie unter [Suchen einer Nachricht oder ein Element mit der Sofortsuche](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Sie können das Inhaltssuche-Feature in Office 365 verwenden, suchen und löschen eine e-Mail-Nachricht aus alle Postfächer in Ihrer Organisation. Dies kann Ihnen suchen und Entfernen von potenziell schädliche oder hohem e-Mails, z. B.:
  
- Nachrichten, die gefährliche Anlagen oder Viren enthalten.
    
- Phishing-Nachrichten
    
- Nachrichten, die vertrauliche Daten enthalten.
    
> [!CAUTION]
> Suchen und löschen ist ein leistungsfähiges Feature, das alle Benutzer ermöglicht, das die erforderlichen Berechtigungen zum Löschen von e-Mail-Nachrichten aus Postfächer in Ihrer Organisation zugewiesen ist. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Zum Erstellen und Ausführen einer Inhaltssuche, müssen Sie Mitglied der Rollengruppe **eDiscovery-Manager** oder die Verwaltungsrolle **Compliance Suche** zugewiesen werden. Um Nachrichten zu löschen, müssen Sie Mitglied der Rollengruppe " **Organisationsverwaltung** " oder die Verwaltungsrolle **Suchen und löschen** zugewiesen werden. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Gewähren des Zugriffs auf die Office 365-Sicherheit &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Sie müssen Sicherheit verwenden &amp; Compliance Center PowerShell Nachrichten löschen. Weitere Informationen zum Herstellen einer Verbindung finden Sie in [Schritt2](#step-2-connect-to-security-amp-compliance-center-powershell) .
    
- Maximal 10 Elemente pro Postfach kann gleichzeitig entfernt werden. Da die Möglichkeit zum Suchen und Entfernen von Nachrichten ein Tool Vorfall-Antwort sein soll, kann dieser Grenzwert mit dem sichergestellt werden, dass Nachrichten aus Postfächern schnell entfernt werden. Dieses Feature ist nicht für die direkte Verwendung von Benutzerpostfächern bereinigen. Um mehr als 10 Elemente löschen, können Sie den Befehl **Search-Mailbox-DeleteContent** in Exchange Online PowerShell verwenden. Finden Sie unter [Suchen und Löschen von Nachrichten - Admin-Hilfe](search-for-and-delete-messagesadmin-help.md).
    
- Die maximale Anzahl von Postfächern in eine Inhaltssuche, Aktion löschen und Löschen von Elementen in einer Suche können ist 50.000. Die Löschaktion (, die Sie in Schritt 3 erstellen) schlägt fehl, wenn die Inhaltssuche (die in [Schritt 1](#step-1-create-a-content-search-to-find-the-message-to-delete)erstellten) mehr als 50.000 Quellpostfächer aufweist. Finden Sie im Abschnitt [Weitere Informationen](#more-information) für einen Hinweis für das Durchführen einer Suche und löschen Sie Vorgang für mehr als 50.000 Postfächer zu. 
    
- Das Verfahren in diesem Artikel kann nur verwendet werden, um Elemente in Exchange Online-Postfächern und öffentlichen Ordnern zu löschen. Sie können sie um Inhalte aus SharePoint oder OneDrive for Business-Websites zu löschen.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Schritt 1: Erstellen Sie eine Inhaltssuche, um die zu löschende Nachricht zu suchen

Der erste Schritt besteht erstellen und Ausführen einer Inhaltssuche, um die Nachricht zu suchen, die Sie aus der Postfächer in Ihrer Organisation entfernen möchten. Sie können die Suche mithilfe der Sicherheits erstellen &amp; Compliance Center oder durch die Cmdlets **New-ComplianceSearch** und **Start-ComplianceSearch** ausführen. Die Nachrichten, die die Abfrage für diese Suche entsprechen werden durch Ausführen des **New-ComplianceSearchAction** -Cmdlets in [Schritt 3](#step-3-delete-the-message)gelöscht. Informationen zum Erstellen einer Inhaltssuche und Konfigurieren von Suchabfragen finden Sie unter den folgenden Themen: 
  
- [Content-Suche in Office 365](content-search.md)
    
- [Stichwortabfragen für Inhaltssuche](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Die Speicherorte für Inhalte, die in die Suche Inhalte durchsucht werden, die Sie in diesem Schritt erstellen können keine SharePoint oder OneDrive for Business-Websites enthalten. Sie können nur Öffentliche Ordner und Postfächer in einer Inhaltssuche einschließen, die e-Mail-Nachrichten verwendet wird. Wenn die Inhaltssuche Websites enthält, erhalten Sie einen Fehler in Schritt 3, wenn Sie das Cmdlet **New-ComplianceSearchAction** ausführen. 
  
### <a name="tips-for-finding-messages-to-remove"></a>Tipps für die Suche nach Nachrichten entfernen

Das Ziel der Suchabfrage ist es, die Ergebnisse der Suche auf die Nachricht oder Nachrichten einzuschränken, die Sie entfernen möchten. Hier finden Sie einige Tipps:
  
- Wenn Sie den genauen Text oder mit dem Ausdruck in der Betreffzeile der Nachricht kennen, verwenden Sie die **Subject** -Eigenschaft in der Suchabfrage. 
    
- Wenn Sie das genaue Datum (oder den Datumsbereich) der Nachricht kennen, nehmen Sie die **Received**-Eigenschaft in die Suchabfrage auf. 
    
- Wenn Sie wissen, wer die Nachricht gesendet hat, nehmen Sie die **From**-Eigenschaft in die Suchabfrage auf. 
    
- Vorschau der Suchergebnisse, um sicherzustellen, dass die Suche nur die Nachricht (Nachrichten) zurückgegeben, die Sie löschen möchten.
    
- Verwenden Sie die Schätzung Suchstatistik (angezeigt im Detailbereich der Suche in das Wertpapier &amp; Compliance Center oder mit dem Cmdlet [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ) um eine Anzahl von die Gesamtzahl der Ergebnisse abzurufen. 
    
Nachfolgend finden Sie zwei Beispiele für Abfragen, um verdächtige E-Mail-Nachrichten zu suchen.
  
- Diese Abfrage gibt Nachrichten zurück, die von Benutzern zwischen dem 13. April 2016 und dem 14. April 2016 empfangen wurden und die Wörter „action“ und „required“ in der Betreffzeile enthalten.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Diese Abfrage gibt Nachrichten zurück, die von chatsuwloginsset12345@outlook.com gesendet wurden und die den exakten Ausdruck „Update your account information“ in der Betreffzeile enthalten.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security-amp-compliance-center-powershell"></a>Schritt 2: Verbinden mit Sicherheit &amp; Compliance Center PowerShell

Im nächsten Schritt wird die Verbindung mit der Sicherheit &amp; Compliance Center PowerShell für Ihre Organisation. Schrittweise Anweisungen finden Sie unter [Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Wenn Ihre Office 365-Konto Multi-Factor Authentication (mehrstufiger Authentifizierung das) oder Verbundauthentifizierung verwendet wird, kann nicht die Anweisungen im vorherigen Thema zum Herstellen einer Verbindung mit der Sicherheit verwenden &amp; Compliance Center PowerShell. Lesen Sie stattdessen die Anweisungen im Thema [Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell mehrstufige Authentifizierung mit](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).
  
## <a name="step-3-delete-the-message"></a>Schritt 3: Löschen der Nachricht

Nachdem Sie erstellt und ein Inhaltssuche, um die Nachricht zurückzugeben, die Sie entfernen möchten, und die Sicherheit verbunden sind eingeschränkt haben &amp; Compliance Center PowerShell der letzte Schritt ist das Cmdlet **New-ComplianceSearchAction** zum Löschen der Nachricht ausführen. Gelöschte Nachrichten werden in den Ordner eines Benutzers wiederherstellbare Elemente verschoben. 
  
Im folgenden Beispiel löscht der Befehl die Suchergebnisse, die von einer Inhaltssuche mit der Bezeichnung „Remove Phishing Message“ zurückgegeben wurde. 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```
  
Die Suche durch den *SearchName* -Parameter angegeben ist, die Content-Suche, die Sie in Schritt 1 erstellt haben. 
  
Weitere Informationen finden Sie unter [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).
  

## <a name="more-information"></a>Weitere Informationen

- **Wie Sie Abrufen des Status der Suche und entfernen Vorgang?**

    Führen Sie das **Get-ComplianceSearchAction** , um den Status des Löschvorgangs abzurufen. Beachten Sie, dass das Objekt, das erstellt wird, wenn Sie das Cmdlet **New-ComplianceSearchAction** ausführen mithilfe dieses Format lautet: `<name of Content Search>_Purge`. 
    
- **Was geschieht nach dem Löschen einer Nachricht?**

    Eine Nachricht, die mithilfe von gelöscht ist die `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` Befehl wird in den Ordner Löschvorgänge in den Ordner des Benutzers wiederherstellbare Elemente verschoben. Es ist nicht vom Office 365 sofort gelöscht. Der Benutzer kann Nachrichten in den Ordner Gelöschte Objekte für die Dauer basierend auf der Aufbewahrungszeit für das Postfach konfiguriert wiederherstellen. Nach Ablauf dieses (oder wenn der Benutzer die Nachricht vor dem Löscht ein abläuft), wird die Nachricht wird in den Ordner Benutzerkontenverwaltung verschoben und nicht mehr vom Benutzer zugegriffen werden kann. Einmal wird in den Ordner bereinigt die Nachricht erneut beibehalten, für die Dauer basierend auf der Aufbewahrungszeit für das Postfach konfiguriert werden, wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist. (Sie in Office 365 ist Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird.) Nach Ablauf die Aufbewahrungszeit für gelöschte die Nachricht wird aus endgültig gekennzeichnet und wird bereinigt werden von Office 365 das nächste Mal an, dem das Postfach von der Assistent für verwaltete Ordner verarbeitet wird. 
    
- **Woher wissen Sie, dass Nachrichten gelöscht und in der Benutzer wiederherstellbare Elemente Ordner verschoben werden?**

    Wenn Sie die gleichen Inhaltssuche ausführen, nachdem Sie eine Nachricht gelöscht, Sie werden weiterhin die gleiche Anzahl von Suchergebnissen angezeigt (und möglicherweise wird davon ausgegangen, dass die Nachricht nicht aus Benutzerpostfächern gelöscht). Dies ist, da eine Inhaltssuche des Ordners wiederherstellbare Elemente durchsucht wird, in dem die gelöschte Nachricht in verschoben wird, nach dem Ausführen der `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` Befehl. Um sicherzustellen, dass Nachrichten, in denen in den Ordner wiederherstellbare Elemente verschoben, können Sie eine Compliance-eDiscovery-Suche (mit dem gleichen Quellpostfächer und Suchkriterien wie die Inhaltssuche in Schritt 1 erstellten) und die Kopie der Suchergebnisse ausführen, Discovery-Postfach. Klicken Sie dann können die Suchergebnisse in das discoverypostfach anzeigen und stellen Sie sicher, dass die Nachrichten in den Ordner wiederherstellbare Elemente verschoben wurde. Ausführliche Informationen zum Erstellen einer Compliance-eDiscovery-Suche, die die Liste der Quellpostfächer und Suchabfrage aus einer Inhaltssuche verwendet finden Sie unter [Verwendung Inhaltssuche in Ihrem Workflow eDiscovery](use-content-search-in-ediscovery.md) . 
    
- **Was geschieht, wenn Sie eine Nachricht von mehr als 50.000 Postfächern löschen müssen?**

    Wie bereits zuvor erwähnt können Sie eine Suche ausführen und Vorgang auf maximal 50.000 Postfächer zu löschen. Wenn Sie zum Suchen und leeren Vorgang für mehr als 50.000 Postfächer verfügen, sollten Sie erstellen temporäre Berechtigungen Suchfilter, die die Anzahl der Postfächer, die auf weniger als 50.000 Postfächer durchsucht werden würde beeinträchtigen würde. Wenn Ihre Organisation Postfächer in anderen Abteilungen, Status oder Ländern enthält, können Sie einen Postfach Suchfilter Berechtigungen basierend auf diesen Postfacheigenschaften suchen einen Teil der Postfächer in Ihrer Organisation erstellen. Nach der Erstellung des Suchfilters Berechtigungen für die Suche (in Schritt 1 beschrieben) erstellen und löschen Sie dann die Nachricht (in Schritt 3 beschrieben). Anschließend können Sie den Filter zum Suchen und Löschen von Nachrichten in einen anderen Satz von Postfächern bearbeiten. Weitere Informationen zum Erstellen von Berechtigungen Suchfilter finden Sie unter [Konfigurieren von Berechtigungen für Inhaltssuche Filtern](permissions-filtering-for-content-search.md).
    
- **Werden in den Suchergebnissen enthalten nicht indizierter Elemente werden gelöscht?**

    Nein, die `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` Befehl nicht indizierten Elemente löschen. 
    
- **Was passiert, wenn eine Nachricht aus dem Postfach gelöscht werden, die auf Compliance-Archiv oder Aufbewahrung für eventuelle Rechtsstreitigkeiten versetzt wurde, oder eine Aufbewahrungsrichtlinie für Office 365 zugewiesen wird?**

    Nach die Nachricht (vom Benutzer oder nach Ablauf die Aufbewahrungszeit für gelöschte) gelöscht wird, wird die Nachricht beibehalten, bis die Dauer halten läuft ab. Wenn die Dauer halten unbegrenzte ist, werden Elemente beibehalten, bis die Sperre entfernt wurde, oder die Dauer halten geändert wird.
    
- **Warum ist der Workflow suchen und entfernen aufgeteilt auf verschiedene Sicherheit &amp; Compliance Center Rollengruppen?**

    Wie bereits erklärt muss eine Person werden Mitglied der Gruppe der eDiscovery-Manager-Rolle oder die Verwaltungsrolle Compliance-Suche suchen Sie Postfächer zugewiesen werden. Um Nachrichten zu löschen, muss eine Person werden Mitglied der Rollengruppe "Organisationsverwaltung" oder die Verwaltungsrolle suchen und Löschen zugewiesen werden. Dadurch können steuern können, die Postfächer in der Organisation suchen und wer Nachrichten löschen können. 

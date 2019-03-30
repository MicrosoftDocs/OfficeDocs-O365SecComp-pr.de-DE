---
title: Suchen und Löschen von e-Mail-Nachrichten in Ihrer Office 365-Organisation-Administratorhilfe
ms.author: markjjo
author: markjjo
manager: laurawi
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
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Verwenden Sie die Such-und Löschfunktion im Security & Compliance Center in Office 365, um eine e-Mail-Nachricht von allen Postfächern in Ihrer Organisation zu suchen und zu löschen.
ms.openlocfilehash: c6fa0d09852016b918375dbff5a19468886d86b3
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000268"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Suchen und Löschen von e-Mail-Nachrichten in Ihrer Office 365-Organisation-Administratorhilfe

**Dieser Artikel richtet sich an Administratoren. Versuchen Sie, Elemente in Ihrem Postfach zu finden, die Sie löschen möchten? Siehe [Suchen nach Nachrichten oder Elementen mit Sofortsuche](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Sie können die Inhaltssuche in Office 365 verwenden, um eine e-Mail-Nachricht von allen Postfächern in Ihrer Organisation zu suchen und zu löschen. Dies kann Ihnen dabei helfen, potenziell schädliche oder risikoreiche e-Mails zu finden und zu entfernen, beispielsweise:
  
- Nachrichten, die gefährliche Anlagen oder Viren enthalten
    
- Phishing-Nachrichten
    
- Nachrichten, die vertrauliche Daten enthalten.
    
> [!CAUTION]
> Suchen und löschen ist eine leistungsstarke Funktion, mit der allen Benutzern, die über die erforderlichen Berechtigungen verfügen, e-Mail-Nachrichten aus Postfächern in Ihrer Organisation gelöscht werden können. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Zum Erstellen und Ausführen einer Inhaltssuche müssen Sie Mitglied der **EDiscovery-Manager-** Rollengruppe sein oder der **Compliance-Such** Verwaltungsrolle zugewiesen sein. Zum Löschen von Nachrichten müssen Sie Mitglied der Rollengruppe " **Organisationsverwaltung** " sein oder der verwaltungsRolle " **Suchen und bereinigen** " zugewiesen sein. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Gewähren von Benutzern Zugriff auf das Security and Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Sie müssen die Security & Compliance Center PowerShell verwenden, um Nachrichten zu löschen. Informationen zum Herstellen einer Verbindung finden Sie in [Schritt 2](#step-2-connect-to-security--compliance-center-powershell) .
    
- Maximal 10 Elemente pro Postfach können gleichzeitig entfernt werden. Da die Funktion zum Suchen und Entfernen von Nachrichten ein Tool zur Reaktion auf Vorfälle sein soll, stellt dieser Höchstwert sicher, dass Nachrichten schnell aus Postfächern entfernt werden können. Dieses Feature ist nicht vorgesehen, um Postfächer zu bereinigen. Wenn Sie mehr als 10 Elemente löschen möchten, können Sie den Befehl **Search-Mailbox-deletecontent** in Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Suchen nach und Löschen von Nachrichten-Administratorhilfe](search-for-and-delete-messagesadmin-help.md).
    
- Die maximale Anzahl von Postfächern in einer Inhaltssuche, in der Sie Elemente löschen können, indem Sie eine Such-und Löschaktion ausführen, ist 50.000. Wenn die Inhaltssuche (die Sie in [Schritt 1](#step-1-create-a-content-search-to-find-the-message-to-delete)erstellen) mehr als 50.000 Quellpostfächer enthält, schlägt die Löschaktion (die Sie in Schritt 3 erstellen) fehl. Im Abschnitt [Weitere Informationen](#more-information) finden Sie einen Tipp zum Durchführen eines Such-und Löschvorgangs auf mehr als 50.000 Postfächern. 
    
- Das Verfahren in diesem Artikel kann nur zum Löschen von Elementen in Exchange Online-Postfächern und öffentlichen Ordnern verwendet werden. Sie können nicht zum Löschen von Inhalten aus SharePoint-oder OneDrive for Business-Websites verwendet werden.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Schritt 1: Erstellen Sie eine Inhaltssuche, um die zu löschende Nachricht zu suchen

Als ersten Schritt müssen Sie eine Inhaltssuche erstellen und ausführen, um die Nachricht zu finden, die Sie aus den Postfächern in der Organisation löschen möchten. Sie können die Suche mithilfe des Security & Compliance Center oder durch Ausführen der Cmdlets **New-ComplianceSearch** und **Start-ComplianceSearch** erstellen. Die Nachrichten, die mit der Abfrage für diese Suche übereinstimmen, werden durch Ausführen des Befehls **New-ComplianceSearchAction-Purge** in [Schritt 3](#step-3-delete-the-message)gelöscht. Informationen zum Erstellen einer Inhaltssuche und Konfigurieren von Suchabfragen finden Sie in den folgenden Themen: 
  
- [Inhaltssuche in Office 365](content-search.md)
    
- [Stichwortabfragen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Die inhaltsspeicherorte, die in der Inhaltssuche durchsucht werden, die Sie in diesem Schritt erstellen, können SharePoint oder OneDrive for Business-Websites nicht einbeziehen. Sie können nur Postfächer und öffentliche Ordner in eine Inhaltssuche einbeziehen, die für e-Mail-Nachrichten verwendet wird. Wenn die Inhaltssuche Websites enthält, erhalten Sie in Schritt 3 eine Fehlermeldung, wenn Sie das Cmdlet **New-ComplianceSearchAction** ausführen. 
  
### <a name="tips-for-finding-messages-to-remove"></a>Tipps zum Suchen nach Nachrichten, die entfernt werden sollen

Das Ziel der Suchabfrage ist es, die Ergebnisse der Suche auf die Nachricht oder Nachrichten einzuschränken, die Sie entfernen möchten. Hier finden Sie einige Tipps:
  
- Wenn Sie den genauen Text oder Ausdruck kennen, der in der Betreffzeile der Nachricht verwendet wird, verwenden Sie die **Subject** -Eigenschaft in der Suchabfrage. 
    
- Wenn Sie das genaue Datum (oder den Datumsbereich) der Nachricht kennen, nehmen Sie die **Received**-Eigenschaft in die Suchabfrage auf. 
    
- Wenn Sie wissen, wer die Nachricht gesendet hat, nehmen Sie die **From**-Eigenschaft in die Suchabfrage auf. 
    
- Zeigen Sie eine Vorschau der Suchergebnisse an, um sicherzustellen, dass die Suche nur die Nachricht (oder Nachrichten) zurückgegeben hat, die Sie löschen möchten.
    
- Verwenden Sie die Such Vorkalkulations Statistik (angezeigt im Detailbereich der Suche im Security & Compliance Center oder mithilfe des Cmdlets [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ), um die Gesamtzahl der Ergebnisse zu ermitteln. 
    
Nachfolgend finden Sie zwei Beispiele für Abfragen, um verdächtige E-Mail-Nachrichten zu suchen.
  
- Diese Abfrage gibt Nachrichten zurück, die von Benutzern zwischen dem 13. April 2016 und dem 14. April 2016 empfangen wurden und die Wörter „action“ und „required“ in der Betreffzeile enthalten.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Diese Abfrage gibt Nachrichten zurück, die von chatsuwloginsset12345@outlook.com gesendet wurden und die den exakten Ausdruck „Update your account information“ in der Betreffzeile enthalten.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Schritt 2: Herstellen einer Verbindung mit Security & Compliance Center PowerShell

Der nächste Schritt besteht darin, eine Verbindung zur Security & Compliance Center-PowerShell für Ihre Organisation herzustellen. Schrittweise Anleitungen finden Sie unter [Connect to Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Wenn Ihr Office 365-Konto eine mehrstufige Authentifizierung (MFA) oder eine Verbundauthentifizierung verwendet, können Sie die Anweisungen im vorherigen Thema zur Verbindung mit Security & Compliance Center PowerShell nicht verwenden. Lesen Sie stattdessen die Anweisungen im Thema [Connect to Security _AMP_ Compliance Center PowerShell using Multi-Factor Authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).
  
## <a name="step-3-delete-the-message"></a>Schritt 3: Löschen der Nachricht

Nachdem Sie eine Inhaltssuche erstellt und verfeinert haben, um die Nachricht zurückzugeben, die Sie entfernen möchten und die mit Security & Compliance Center PowerShell verbunden sind, müssen Sie **** den letzten Schritt ausführen, um die Nachricht zu löschen. Sie können die Nachricht Soft-oder hart löschen. Eine weiche gelöschte Nachricht wird in den Ordner "Wiederherstellbare Elemente" eines Benutzers verschoben und bis zum Ablauf der Aufbewahrungszeit für gelöschte Elemente aufbewahrt. Fest gelöschte Nachrichten sind für eine dauerhafte Entfernung aus dem Postfach gekennzeichnet und werden bei der nächsten Verarbeitung des Postfachs durch den Assistenten für verwaltete Ordner endgültig entfernt. Wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist, werden endgültig gelöschte Elemente nach Ablauf des Aufbewahrungszeitraums für gelöschte Elemente dauerhaft entfernt. Wenn ein Postfach in der Warteschleife gehalten wird, bleiben gelöschte Nachrichten erhalten, bis die Aufbewahrungsdauer für das Element abläuft oder bis der Haltebereich aus dem Postfach entfernt wird.
  
Im folgenden Beispiel löscht der Befehl die Suchergebnisse, die von einer Inhaltssuche mit dem Namen "Remove Phishing Message" zurückgegeben werden. 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Führen Sie den folgenden Befehl aus, um die von der Inhaltssuche für das Entfernen von Phishing-nachRichten zurückgegebenen Elemente zu löschen:

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Beachten Sie, dass beim Ausführen des vorherigen Befehls für das weiche oder harte Löschen von Nachrichten die durch den Parameter *searchName* angegebene Suche die Inhaltssuche ist, die Sie in Schritt 1 erstellt haben. 
  
Weitere Informationen finden Sie unter [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Weitere Informationen

- **Wie erhalten Sie Status beim Suchen und entfernen?**

    Führen Sie **Get-ComplianceSearchAction** aus, um den Status des Löschvorgangs abzurufen. Beachten Sie, dass das Objekt, das beim Ausführen des **New-ComplianceSearchAction-** Cmdlets erstellt wird, mit `<name of Content Search>_Purge`folgendem Format benannt wird:. 
    
- **Was geschieht, nachdem Sie eine Nachricht gelöscht haben?**

   Eine Nachricht, die mit dem `New-ComplianceSearchAction -Purge -PurgeType HardDelete` Befehl gelöscht wird, wird in den Ordner "Säuberungs" verschoben und kann vom Benutzer nicht zugegriffen werden. Nachdem die Nachricht in den Ordner "Purges" verschoben wurde, wird die Nachricht für die Dauer des Aufbewahrungszeitraums für gelöschte Elemente aufbewahrt, wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist. (In Office 365 ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird.) Nach Ablauf der Aufbewahrungszeit für gelöschte Elemente wird die Nachricht für eine dauerhafte Löschung markiert und aus Office 365 gelöscht, wenn das Postfach das nächste Mal vom Assistenten für verwaltete Ordner verarbeitet wird. 

   Wenn Sie den `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` Befehl verwenden, werden Nachrichten in den Ordner "Löschungen" im Ordner "Wiederherstellbare Elemente" des Benutzers verschoben. Es wird nicht sofort aus Office 365 gelöscht. Der Benutzer kann Nachrichten im Ordner „Gelöschte Elemente“ so lange wiederherstellen, bis die für das Postfach konfigurierte Aufbewahrungsfrist abgelaufen ist. Nach Ablauf dieser Aufbewahrungsfrist (oder wenn der Benutzer die Nachricht vor Ablauf dauerhaft löscht) wird die Nachricht in den Ordner „Endgültige Löschvorgänge“ verschoben, und der Benutzer kann nicht mehr darauf zugreifen. Sobald Sie sich im Ordner "Purges" befinden, wird die Nachricht für die Dauer basierend auf dem Aufbewahrungszeitraum für gelöschte Elemente aufbewahrt, der für das Postfach konfiguriert ist, wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist. (In Office 365 ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird.) Nach Ablauf der Aufbewahrungszeit für gelöschte Elemente wird die Nachricht für eine dauerhafte Löschung markiert und aus Office 365 gelöscht, wenn das Postfach das nächste Mal vom Assistenten für verwaltete Ordner verarbeitet wird. 
    
- **Was geschieht, wenn Sie eine Nachricht aus mehr als 50.000 Postfächern löschen müssen?**

    Wie bereits erwähnt, können Sie einen Such-und Löschvorgang mit maximal 50.000 Postfächern ausführen. Wenn Sie einen Such-und Bereinigungsvorgang für mehr als 50.000 Postfächer durchführen müssen, erwägen Sie das Erstellen von temporären Such Berechtigungs filtern, mit denen die Anzahl der Postfächer reduziert würde, die nach weniger als 50.000 Postfächern durchsucht werden würden. Wenn Ihre Organisation beispielsweise Postfächer in unterschiedlichen Abteilungen, Staaten oder Ländern enthält, können Sie einen Filter für die Postfachsuche erstellen, der auf einer dieser Postfacheigenschaften basiert, um eine Teilmenge der Postfächer in Ihrer Organisation zu durchsuchen. Nach dem Erstellen des Such Berechtigungs Filters würden Sie die Suche (in Schritt 1 beschrieben) erstellen und dann die Nachricht löschen (beschrieben in Schritt 3). Anschließend können Sie den Filter bearbeiten, um Nachrichten in einem anderen Satz von Postfächern zu suchen und zu löschen. Weitere Informationen zum Erstellen von Such Berechtigungs Filtern finden Sie unter [configure Permissions Filtering for Content Search](permissions-filtering-for-content-search.md).
    
- **Werden nicht indizierte Elemente, die in den Suchergebnissen enthalten sind, gelöscht?**

    Nein, der Befehl ' New-ComplianceSearchAction-Purge ' löscht nicht indizierte Elemente. 
    
- **Was geschieht, wenn eine Nachricht aus einem Postfach gelöscht wird, für das ein in-situ-Aufbewahrungs-oder Rechtsschutzverfahren festgelegt wurde oder das einer Office 365-Speicherrichtlinie zugeordnet ist?**

    Nachdem die Nachricht gelöscht und in den Ordner "Purges" verschoben wurde, wird die Nachricht beibehalten, bis die Aufbewahrungsdauer abgelaufen ist. Wenn die Aufbewahrungsdauer unbegrenzt ist, werden die Elemente beibehalten, bis der Haltebereich entfernt oder die Aufbewahrungsdauer geändert wird.
    
- **Warum ist der Workflow für suchen und entfernen unter verschiedenen Rollengruppen im Security and Compliance Center aufgeteilt?**

    Wie bereits weiter oben erwähnt, muss ein Benutzer Mitglied der eDiscovery-Manager-Rollengruppe sein, oder ihm muss die Compliancesuche-Verwaltungsrolle zugewiesen sein, damit er Postfächer durchsuchen kann. Um Nachrichten löschen zu können, muss der Benutzer Mitglied der Rollengruppe „Organisationsverwaltung“ sein, oder ihm muss die Verwaltungsrolle zum Suchen und Löschen zugewiesen sein. Auf diese Weise kann geregelt werden, wer Postfächer in der Organisation durchsuchen und wer Nachrichten löschen kann. 

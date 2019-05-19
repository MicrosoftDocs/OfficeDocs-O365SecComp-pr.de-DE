---
title: Suchen nach und Löschen von e-Mail-Nachrichten in Ihrer Office 365 Organisation – Administratorhilfe
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
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
description: Verwenden Sie die Such-und Säuberungsfunktion im Security & Compliance Center in Office 365, um eine e-Mail-Nachricht von allen Postfächern in Ihrer Organisation zu suchen und zu löschen.
ms.openlocfilehash: f654b643a5f1e4feac6e32a67843b2a6a9563bd0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158477"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Suchen nach und Löschen von e-Mail-Nachrichten in Ihrer Office 365 Organisation – Administratorhilfe

**Dieser Artikel richtet sich an Administratoren. Versuchen Sie, nach Elementen in Ihrem Postfach zu suchen, die Sie löschen möchten? Siehe [Suchen nach Nachrichten oder Elementen mit der Sofortsuche](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Sie können das Feature für die Inhaltssuche in Office 365 verwenden, um eine e-Mail-Nachricht aus allen Postfächern in Ihrer Organisation zu suchen und zu löschen. Dies kann Ihnen helfen, potenziell schädliche oder risikoreiche e-Mails zu finden und zu entfernen, beispielsweise:
  
- Nachrichten, die gefährliche Anlagen oder Viren enthalten
    
- Phishing-Nachrichten
    
- Nachrichten, die vertrauliche Daten enthalten.
    
> [!CAUTION]
> Suchen und löschen ist eine leistungsstarke Funktion, die allen Benutzern, denen die erforderlichen Berechtigungen zum Löschen von e-Mail-Nachrichten aus Postfächern in Ihrer Organisation zugewiesen sind, ermöglicht wird. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Zum Erstellen und Ausführen einer Inhaltssuche müssen Sie Mitglied der Rollengruppe " **eDiscovery-Manager** " sein oder der **Compliance Search** -Verwaltungsrolle zugewiesen sein. Zum Löschen von Nachrichten müssen Sie Mitglied der Rollengruppe " **Organisationsverwaltung** " sein oder der Rolle " **Such-und Lösch** Verwaltung" zugewiesen sein. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Gewähren von Benutzern Zugriff auf das Security and Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Sie müssen die Security & Compliance Center PowerShell verwenden, um Nachrichten zu löschen. In [Schritt 2](#step-2-connect-to-security--compliance-center-powershell) finden Sie Anweisungen zum Herstellen einer Verbindung.
    
- Es können maximal 10 Elemente pro Postfach auf einmal entfernt werden. Da die Funktion zum Suchen und Entfernen von Nachrichten ein Tool zur Reaktion auf Vorfälle sein soll, stellt dieser Höchstwert sicher, dass Nachrichten schnell aus Postfächern entfernt werden können. Dieses Feature ist nicht vorgesehen, um Postfächer zu bereinigen. Wenn Sie mehr als 10 Elemente löschen möchten, können Sie den Befehl **Search-Mailbox-Option deletecontent** in Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Suchen nach und Löschen von Nachrichten-Administratorhilfe](search-for-and-delete-messagesadmin-help.md).
    
- Die maximale Anzahl von Postfächern in einer Inhaltssuche, in der Sie Elemente löschen können, indem Sie eine Such-und Löschaktion ausführen, lautet 50.000. Wenn die Inhaltssuche (die Sie in [Schritt 1](#step-1-create-a-content-search-to-find-the-message-to-delete)erstellen) über mehr als 50.000 Quellpostfächer verfügt, tritt bei der Löschaktion (die Sie in Schritt 3 erstellen) ein Fehler auf. Im Abschnitt [Weitere Informationen](#more-information) finden Sie einen Tipp zum Ausführen eines Such-und Löschvorgangs für mehr als 50.000 Postfächer. 
    
- Das Verfahren in diesem Artikel kann nur verwendet werden, um Elemente in Exchange Online Postfächern und öffentlichen Ordnern zu löschen. Sie können ihn nicht zum Löschen von Inhalten aus SharePoint-oder OneDrive für Unternehmen-Websites verwenden.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Schritt 1: Erstellen Sie eine Inhaltssuche, um die zu löschende Nachricht zu suchen

Als ersten Schritt müssen Sie eine Inhaltssuche erstellen und ausführen, um die Nachricht zu finden, die Sie aus den Postfächern in der Organisation löschen möchten. Sie können die Suche mithilfe des Security & Compliance Center oder durch Ausführen der Cmdlets **New-ComplianceSearch** und **Start-ComplianceSearch** erstellen. Die Nachrichten, die mit der Abfrage für diese Suche übereinstimmen, werden durch Ausführen des Befehls **New-ComplianceSearchAction-Purge** in [Schritt 3](#step-3-delete-the-message)gelöscht. Informationen zum Erstellen einer Inhaltssuche und Konfigurieren von Suchabfragen finden Sie in den folgenden Themen: 
  
- [Inhaltssuche in Office 365](content-search.md)
    
- [Stichwortabfragen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Die inhaltsspeicherorte, die in der Inhaltssuche durchsucht werden, die Sie in diesem Schritt erstellen, können keine SharePoint-oder OneDrive für Unternehmen-Websites enthalten. Sie können nur Postfächer und öffentliche Ordner in eine Inhaltssuche einschließen, die für e-Mail-Nachrichten verwendet wird. Wenn die Inhaltssuche Websites enthält, erhalten Sie in Schritt 3 eine Fehlermeldung, wenn Sie das Cmdlet **New-ComplianceSearchAction** ausführen. 
  
### <a name="tips-for-finding-messages-to-remove"></a>Tipps zum Auffinden von zu entfernenden Nachrichten

Das Ziel der Suchabfrage ist es, die Ergebnisse der Suche auf die Nachricht oder Nachrichten einzuschränken, die Sie entfernen möchten. Hier finden Sie einige Tipps:
  
- Wenn Sie den exakten Text oder den genauen Ausdruck kennen, der in der Betreffzeile der Nachricht verwendet wird, verwenden Sie die **Subject** -Eigenschaft in der Suchabfrage. 
    
- Wenn Sie das genaue Datum (oder den Datumsbereich) der Nachricht kennen, nehmen Sie die **Received**-Eigenschaft in die Suchabfrage auf. 
    
- Wenn Sie wissen, wer die Nachricht gesendet hat, nehmen Sie die **From**-Eigenschaft in die Suchabfrage auf. 
    
- Zeigen Sie eine Vorschau der Suchergebnisse an, um zu überprüfen, ob die Suche nur die Nachricht (oder Nachrichten) zurückgegeben hat, die Sie löschen möchten.
    
- Verwenden Sie die Such schätzungs Statistiken (werden im Detailbereich der Suche im Security & Compliance Center oder mithilfe des Cmdlets [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) angezeigt), um die Gesamtanzahl der Ergebnisse abzurufen. 
    
Nachfolgend finden Sie zwei Beispiele für Abfragen, um verdächtige E-Mail-Nachrichten zu suchen.
  
- Diese Abfrage gibt Nachrichten zurück, die von Benutzern zwischen dem 13. April 2016 und dem 14. April 2016 empfangen wurden und die Wörter „action“ und „required“ in der Betreffzeile enthalten.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Diese Abfrage gibt Nachrichten zurück, die von chatsuwloginsset12345@outlook.com gesendet wurden und die den exakten Ausdruck „Update your account information“ in der Betreffzeile enthalten.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Schritt 2: Herstellen einer Verbindung mit der Security & Compliance Center PowerShell

Im nächsten Schritt stellen Sie eine Verbindung mit der Security & Compliance Center PowerShell für Ihre Organisation her. Eine Schritt-für-Schritt-Anleitung finden Sie unter [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Wenn Ihr Office 365 Konto mehrstufige Authentifizierung (MFA) oder Verbundauthentifizierung verwendet, können Sie die Anweisungen im vorherigen Thema nicht zum Herstellen einer Verbindung mit Security & Compliance Center PowerShell verwenden. Lesen Sie stattdessen die Anweisungen im Thema verbinden mit dem [Security & Compliance Center PowerShell mithilfe der mehr](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell)stufigen Authentifizierung.
  
## <a name="step-3-delete-the-message"></a>Schritt 3: Löschen der Nachricht

Nachdem Sie eine Inhaltssuche erstellt und verfeinert haben, um die Nachricht zurückzugeben, die Sie entfernen möchten, und mit der Security & Compliance Center-PowerShell verbunden sind, besteht der letzte Schritt darin, das Cmdlet **New-ComplianceSearchAction** auszuführen, um die Nachricht zu löschen. Sie können die Nachricht Soft-oder hart löschen. Eine vorläufig gelöschte Nachricht wird in den Ordner "Wiederherstellbare Elemente" des Benutzers verschoben und so lange aufbewahrt, bis der Aufbewahrungszeitraum für gelöschte Elemente abläuft. Hart gelöschte Nachrichten werden für die dauerhafte Entfernung aus dem Postfach markiert und werden beim nächsten verarbeiten des Postfachs durch den Assistenten für verwaltete Ordner endgültig entfernt. Wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist, werden endgültig gelöschte Elemente nach Ablauf des Aufbewahrungszeitraums für gelöschte Elemente dauerhaft entfernt. Wenn ein Postfach aufbewahrt wird, werden gelöschte Nachrichten beibehalten, bis die Aufbewahrungsdauer für das Element abläuft oder bis der Haltebereich aus dem Postfach entfernt wird.
  
Im folgenden Beispiel löscht der Befehl die Suchergebnisse, die von einer Inhaltssuche namens "Remove Phishing Message" zurückgegeben werden. 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Wenn Sie die Elemente, die von der Inhaltssuche "Remove Phishing Message" zurückgegeben werden, hart löschen möchten, führen Sie den folgenden Befehl aus:

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Beachten Sie, dass beim Ausführen des vorherigen Befehls für Nachrichten mit Soft-oder Hard-Delete die durch den *searchName* -Parameter angegebene Suche die Inhaltssuche ist, die Sie in Schritt 1 erstellt haben. 
  
Weitere Informationen finden Sie unter [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Weitere Informationen

- **Wie erhalten Sie den Status für den Such-und Entfernungsvorgang?**

    Führen Sie **Get-ComplianceSearchAction** aus, um den Status des Löschvorgangs abzurufen. Beachten Sie, dass das Objekt, das beim Ausführen des **New-ComplianceSearchAction-** Cmdlets erstellt wird, mit `<name of Content Search>_Purge`folgendem Format benannt wird:. 
    
- **Was geschieht, nachdem Sie eine Nachricht gelöscht haben?**

   Eine Nachricht, die mit dem `New-ComplianceSearchAction -Purge -PurgeType HardDelete` Befehl gelöscht wird, wird in den Ordner "Säuberungen" verschoben, und der Benutzer kann nicht darauf zugreifen. Nachdem die Nachricht in den Ordner "Säuberungen" verschoben wurde, wird die Nachricht für die Dauer des Aufbewahrungszeitraums für gelöschte Elemente aufbewahrt, wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist. (In Office 365 ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird.) Nach Ablauf des Aufbewahrungszeitraums für gelöschte Elemente wird die Nachricht als dauerhafter Löschvorgang markiert und wird aus Office 365 gelöscht, wenn das Postfach das nächste Mal vom Assistenten für verwaltete Ordner verarbeitet wird. 

   Wenn Sie den `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` Befehl verwenden, werden Nachrichten in den Ordner "Löschungen" im Ordner "refundable Items" des Benutzers verschoben. Er wird nicht sofort aus Office 365 gelöscht. Der Benutzer kann Nachrichten im Ordner „Gelöschte Elemente“ so lange wiederherstellen, bis die für das Postfach konfigurierte Aufbewahrungsfrist abgelaufen ist. Nach Ablauf dieser Aufbewahrungsfrist (oder wenn der Benutzer die Nachricht vor Ablauf dauerhaft löscht) wird die Nachricht in den Ordner „Endgültige Löschvorgänge“ verschoben, und der Benutzer kann nicht mehr darauf zugreifen. Im Ordner "Säuberungen" wird die Nachricht für die Dauer aufbewahrt, die auf dem Aufbewahrungszeitraum für gelöschte Elemente basiert, der für das Postfach konfiguriert wurde, wenn die Wiederherstellung einzelner Elemente für das Postfach aktiviert ist. (In Office 365 ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird.) Nach Ablauf des Aufbewahrungszeitraums für gelöschte Elemente wird die Nachricht als dauerhafter Löschvorgang markiert und von Office 365 beim nächsten verarbeiten des Postfachs durch den Assistenten für verwaltete Ordner gelöscht. 
    
- **Was ist, wenn Sie eine Nachricht aus mehr als 50.000 Postfächern löschen müssen?**

    Wie bereits erwähnt, können Sie einen Such-und Aufräumvorgang für maximal 50.000 Postfächer durchführen. Wenn Sie einen Such-und Aufräumvorgang für mehr als 50.000 Postfächer durchführen müssen, sollten Sie die Erstellung von Berechtigungs Filtern für temporäre Suchvorgänge in Frage stellen, mit denen die Anzahl der Postfächer reduziert würde, die auf weniger als 50.000 Postfächer durchsucht würden. Wenn Ihre Organisation beispielsweise Postfächer in unterschiedlichen Abteilungen, Staaten oder Ländern enthält, können Sie einen Filter für die Post Fach Suchberechtigungen basierend auf einer dieser Postfacheigenschaften erstellen, um eine Teilmenge von Postfächern in Ihrer Organisation zu durchsuchen. Nachdem Sie den Filter für die Suchberechtigungen erstellt haben, würden Sie die Suche (in Schritt 1 beschrieben) erstellen und dann die Nachricht löschen (in Schritt 3 beschrieben). Anschließend können Sie den Filter bearbeiten, um Nachrichten in einer anderen Gruppe von Postfächern zu suchen und zu löschen. Weitere Informationen zum Erstellen von Such Berechtigungs Filtern finden Sie unter [Konfigurieren der Berechtigungs Filterung für die Inhaltssuche](permissions-filtering-for-content-search.md).
    
- **Werden nicht indizierte Elemente, die in den Suchergebnissen enthalten sind, gelöscht?**

    Nein, der Befehl "New-ComplianceSearchAction-Purge" löscht keine nicht indizierten Elemente. 
    
- **Was passiert, wenn eine Nachricht aus einem Postfach gelöscht wird, das in einem Compliance-Archiv oder einem Beweissicherungsverfahren gespeichert oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde?**

    Nachdem die Nachricht gelöscht und in den Ordner "Säuberungen" verschoben wurde, wird die Nachricht beibehalten, bis die Aufbewahrungsdauer abgelaufen ist. Wenn die Aufbewahrungsdauer unbegrenzt ist, werden die Elemente beibehalten, bis der Haltebereich entfernt oder die Aufbewahrungsdauer geändert wird.
    
- **Warum ist der Workflow "suchen und entfernen" zwischen verschiedenen Sicherheits-und Compliance Center-Rollengruppen aufgeteilt?**

    Wie bereits weiter oben erwähnt, muss ein Benutzer Mitglied der eDiscovery-Manager-Rollengruppe sein, oder ihm muss die Compliancesuche-Verwaltungsrolle zugewiesen sein, damit er Postfächer durchsuchen kann. Um Nachrichten löschen zu können, muss der Benutzer Mitglied der Rollengruppe „Organisationsverwaltung“ sein, oder ihm muss die Verwaltungsrolle zum Suchen und Löschen zugewiesen sein. Auf diese Weise kann geregelt werden, wer Postfächer in der Organisation durchsuchen und wer Nachrichten löschen kann. 

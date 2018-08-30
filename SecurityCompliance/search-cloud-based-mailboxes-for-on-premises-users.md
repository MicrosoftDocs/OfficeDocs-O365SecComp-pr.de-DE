---
title: Suchen von Cloud-basierten Postfächern für lokale Benutzer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Verwenden Sie das Tool Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center zum Suchen nach und exportieren Sie MicrosoftTeams chatdaten (1xN Chats genannt) für den lokalen Benutzer in einer Exchange-hybridbereitstellung.
ms.openlocfilehash: a504dfcf4c82bec036137b90312c01a0b2326ccc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529260"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Suchen von Cloud-basierten Postfächern für lokale Benutzer in Office 365

Wenn Ihre Organisation verfügt über eine hybride Exchange-Bereitstellung und Microsoft-Teams aktiviert hat, können Benutzer die Anwendung des Teams Chat für instant messaging verwenden. Für den Benutzer Cloud-basierten werden die Teams chatdaten (auch als 1xN Chats bezeichnet) auf ihre Cloud-basierten Hauptpostfach gespeichert. Wenn ein lokale Benutzer die Team-Chat-Anwendung verwendet wird, ist das primäre Postfach lokale befindet. Wenn Sie diese Einschränkung umgehen, hat Microsoft ein neues Feature veröffentlicht, wo ein Cloud-basierten Speicherbereich (einem cloudbasierten Postfach für lokale Benutzer genannt) zum Speichern von Teams chatdaten für lokale Benutzer erstellt wird. Auf diese Weise können Sie die Verwendung des Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center zum Suchen und Exportieren von Teams chatdaten für lokale Benutzer. 
  
Hier sind die Anforderungen und Einschränkung zum Einrichten und zum Einrichten und cloudbasierten Postfächer für lokale Benutzer zu suchen:
  
- Die Benutzerkonten in Ihrer lokalen Verzeichnisdienst (Active Directory) müssen mit Azure Active Directory, den Verzeichnisdienst in Office 365 synchronisiert werden. Dies bedeutet, dass ein e-Mail-Benutzerkonto in Office 365 erstellt wird und einem Benutzer, deren primäres Postfach sich in der lokalen Organisation befindet, zugeordnet ist.
    
- Cloud-basierte Postfach für lokale Benutzer ist verwendeten nur Store Teams chatdaten. Ein lokale Benutzer nicht anmelden, um das cloudbasierten Postfach oder keinerlei Zugriff auf. Es kann nicht zum Senden oder Empfangen von e-Mail-Nachrichten verwendet werden. 
    
- Sie müssen eine Anforderung an den Microsoft-Support zur Ihrer Organisation Teams chatdaten in die Cloud-basierten Postfächer für lokale Benutzer suchen aktivieren. Finden Sie unter [eine Anforderung zum Aktivieren dieser Funktion in das Wertpapier mit Microsoft-Supportmitarbeiter ablegen &amp; Compliance Center](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) in diesem Artikel. 
    
 **Hinweis:** Teams Channel Unterhaltungen werden immer in der Cloud-basierte Postfach gespeichert, die mit dem Team zugeordnet ist. Dies bedeutet, dass Sie Inhaltssuche Suche Kanal verwenden können, Unterhaltungen ohne eine Anfrage müssen. Weitere Informationen zum Suchen von Teams channel Unterhaltungen, finden Sie unter [Microsoft-Teams, Suche und Office 365-Gruppen](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Funktionsweise

Wenn ein Microsoft-Teams-aktivierter Benutzer verfügt über ein lokales Postfach und ihre Benutzeridentität/Konto in der Cloud synchronisiert wurden hat, erstellt Microsoft ein Cloud-basierte Postfach um 1xN Teams chatdaten zu speichern. Nachdem die Teams chatdaten in der Cloud-basierte Postfach gespeichert ist, wird es für die Suche indiziert. Auf diese Weise können Sie Inhaltssuche verwenden (und Suchvorgänge eDiscovery-Fälle zugeordnet), um zu suchen, eine Vorschau anzeigen und Exportieren von Teams chatdaten für lokale Benutzer. Sie können auch ** \*ComplianceSearch** -Cmdlets in die Office 365-Sicherheit &amp; Compliance Center PowerShell für Teams chatdaten für lokale Benutzer suchen. 
  
Die folgende Abbildung zeigt, dass der Workflow von wie Teams Daten für lokale Benutzer chat steht zu suchen und eine Vorschau exportieren.
  
![Cloud-basierten Speicher für lokale Benutzer in Microsoft-Teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
Neben dieser neuen Funktionalität weiterhin können Sie Inhalte Suche suchen, eine Vorschau anzeigen und Exportieren von Inhalt in der Cloud-basierte SharePoint-Website und die Exchange-Postfach mit jedem Microsoft-Teams und 1xN Teams chatdaten in der Exchange Online-Postfach für zugewiesene Teams Cloud-basierten Benutzer.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a>Eine Anforderung zum Aktivieren dieser Funktion in das Wertpapier mit Microsoft-Supportmitarbeiter ablegen &amp; Compliance Center

Sie müssen eine Anforderung mit Microsoft-Supportmitarbeiter zum Aktivieren der Organisation verwenden die grafische Benutzeroberfläche in das Wertpapier Datei &amp; Compliance Center Teams chatdaten in die Cloud-basierten Postfächer für lokale Benutzer suchen. Beachten Sie, dass dieses Feature verfügbar in Office 365-Sicherheit ist &amp; Compliance Center PowerShell. Sie müssen nicht übermitteln eine Supportanfrage an PowerShell verwenden, um für Teams chatdaten für lokale Benutzer suchen. 
  
Schließen Sie die folgende Informationen, wenn die Anforderung an den Support von Microsoft zu übermitteln:
  
- Die Standard-Domänenname des Office 365-Organisation.
    
- Der Name des Mandanten und die Mandanten-ID der Office 365-Organisation. Sie finden diese im Azure Active Directory-Portal (unter **Verwalten** \> **Eigenschaften**). Finden Sie [Hier finden Sie Ihre Office 365-Mandanten-ID](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b)aus.
    
- Die folgenden Titel oder die Beschreibung des Zwecks der Anforderung Unterstützung: "Application Inhaltssuche für lokale Benutzer aktivieren". Dadurch wird die Anforderung an den Office 365 eDiscovery engineering Team weitergeleitet, die die Anforderung implementiert. 
    
Nachdem die engineering Änderung erfolgt ist, wird Microsoft Support ein Bereitstellungsdatum geschätzte senden. Beachten Sie, dass der Bereitstellungsprozess in der Regel 2 bis 3 Wochen nach der Supportanfrage zu übermitteln. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>Was geschieht nach dem dieses Feature aktiviert ist?

Nachdem dieses Feature in Office 365-Organisation bereitgestellt wird, die folgenden Änderungen werden in Inhaltssuche vorgenommen und in Zusammenhang mit einer eDiscovery Suchvorgängen case in das Wertpapier &amp; Compliance Center:
  
- Das Kontrollkästchen **Office hinzufügen app Inhalte für lokale Benutzer** wird unter den **Speicherorten** in den Inhalten suchen hinzugefügt. 
    
    ![Die Inhalte der Benutzeroberfläche wird das Kontrollkästchen "Office app Inhalte für lokale Benutzer hinzufügen" hinzugefügt.](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Lokale Benutzer werden im Auswahltool Speicherorte für Inhalte angezeigt, mit denen Sie wählen Sie Benutzerpostfächer zu suchen. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Suchen nach Teams Chat Content in cloudbasierten Postfächer für lokale Benutzer

Nachdem das Feature aktiviert wurde, können Sie Inhaltssuche verwenden, in das Wertpapier &amp; Compliance Center Teams chatdaten in die Cloud-basierten Postfächer für lokale Benutzer suchen. 
  
1. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**
    
2. Klicken Sie auf der Seite **Suche** auf ![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**.
    
    Wie bereits erklärt wird das **Hinzufügen von Office-app-Inhalte für lokale Benutzer** aktivieren klicken Sie unter **Speicherorte**angezeigt. Beachten Sie, dass es in der Standardeinstellung aktiviert ist.
    
3. Erstellen Sie der Stichwortabfrage und fügen Sie Bedingungen zur Suchabfrage, falls erforderlich. Nur die Suche für Team-chats Daten, können Sie die folgende Abfrage in das Feld **Schlüsselwörter** hinzufügen: 
    
    ```
    kind:im
    ``` 

4. Zu diesem Zeitpunkt können Sie eine der folgenden Optionen unter **Speicherorte**wählen:
    
    - **Alle Speicherorte** - wählen Sie diese Option, um die Postfächer aller Benutzer in Ihrer Organisation zu suchen. Wenn das Kontrollkästchen aktiviert ist, werden auch alle cloudbasierte Postfächer für lokale Benutzer gesucht werden soll. 
    
    - **Bestimmte Orte** - wählen Sie diese Option aus, und klicken Sie dann auf **Ändern** \> wählen Sie Benutzer, Gruppen oder Teams, um bestimmte Postfächer zu suchen. Wie bereits erklärt lässt das Auswahltool Speicherorte für lokale Benutzer zu suchen. 
    
5. Speichern Sie, und führen Sie die Suche. Keine Suchergebnisse aus der Cloud-basierten Postfächern für lokale Benutzer können wie alle anderen Suchergebnisse Vorschau angezeigt werden. Darüber hinaus können Sie die Suchergebnisse (einschließlich Teams chatdaten) können in eine PST-Datei exportieren. Weitere Informationen finden Sie unter: 
    
    - [Erstellen Sie eine neue Suche](content-search.md#create-a-new-search)
    
    - [Vorschau auf Suchergebnisse anzeigen](content-search.md#preview-search-results)
    
    - [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Mithilfe von PowerShell für Teams chatdaten im cloudbasierten Postfächer für lokale Benutzer suchen

Sie können die Cmdlets **New-ComplianceSearch** und **Set-ComplianceSearch** in die Office 365-Sicherheit &amp; Compliance Center PowerShell cloudbasierten Postfach für lokale Benutzer zu suchen. Wie bereits erklärt müssen Sie eine Supportanfrage zu PowerShell verwenden, um die Suche nach Teams chatdaten für lokale Benutzer zu übermitteln. 
  
1. [Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Führen Sie die folgenden PowerShell sucht Befehl aus, um einen neuen Inhalt erstellen die cloudbasierten Postfächer von lokalen Benutzern.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    Der Parameter *IncludeUserAppContent* wird verwendet, an die cloudbasierten Postfach für den Benutzer oder Benutzer, die durch den Parameter *ExchangeLocation* angegeben werden. Die *AllowNotFoundExchangeLocationsEnabled* ermöglicht die cloudbasierten Postfächer für lokale Benutzer. Bei Verwendung der `$true` Wert für diesen Parameter, für die Suche nicht versuchen, überprüfen Sie das Vorhandensein des Postfachs, bevor er ausgeführt wird. Dies ist erforderlich, um die cloudbasierten Postfächer für lokale Benutzer zu suchen, da diese Typen von Postfächern als normale Postfächer nicht lösen können. 
    
    Das folgende Beispiel sucht nach Teams Chats (die Sofortnachrichten sind), die Schlüsselwort "Redstone" in der Cloud-basierte Postfach von Sara Davis, lokale Benutzer in der Organisation "Contoso" enthalten.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Nachdem Sie eine neue Suche erstellt haben, müssen Sie unbedingt das **Start-ComplianceSearch** -Cmdlet verwenden, um die Suche auszuführen. 
  
Weitere Informationen zum Verwenden dieser Cmdlets finden Sie unter:
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Bekannte Probleme

- Derzeit können Sie nur Suche, Vorschau und Export Content in cloudbasierten Postfächer für lokale Benutzer. Platzieren eines Postfachs Cloud-basierten für einen lokalen Benutzer einem Haltestatus einer eDiscovery zugeordnet wird Groß-/Kleinschreibung oder Zuweisen einer Aufbewahrungsrichtlinie für Office 365 nicht unterstützt. 
    
- Die Personenauswahl Inhaltsspeicherort für eDiscovery enthält zeigt lokale Benutzer und können Sie diese auswählen. Jedoch wie weiter oben erläutert, dass die Sperre für den lokalen Benutzer nicht angewendet wird.
    
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

 **Wo befinden sich die cloudbasierten Postfächer für lokale Benutzer?**
  
Cloud-basierten Postfächern werden erstellt und im selben Rechenzentrum wie die Office 365-Organisation gespeichert. 
  
 **Gibt es anderen Anforderungen als Übermittlung einer Anforderung Unterstützung?**
  
 Wie bereits erklärt müssen die Identitäten der Benutzer mit Postfächern auf Prem zu Ihrer cloudbasierten Organisation synchronisiert werden, damit ein entsprechendes Benutzerkonto von e-Mail für jedes lokale Benutzerkonto in Office 365 erstellt wird. Darüber hinaus muss die Organisation ein Office 365 Enterprise-Abonnement, wie ein Office 365 Enterprise E1, E3 oder E5-Abonnement besitzen. 
  
 **Gibt es ein Risiko von Datenverlusten der Teams Chat, wenn die lokalen Postfach des Benutzers in die Cloud migriert werden?**
  
Nein. Wenn Sie das primäre Postfach eines lokalen Benutzers zur Cloud migrieren, werden die Teams chatdaten für diesen Benutzer für ihr neues Cloud-basierten primären Postfach migriert.
  
 **Kann ein eDiscovery-Archiv oder Office 365-Aufbewahrungsrichtlinien für lokale Benutzer werden angewendet?**
  
Nein.
  
 **Können Inhaltssuche Find ältere Teams chats für lokale Benutzer vor der Zeit meiner Organisation übermittelt die Anforderung an die dieses Feature aktivieren?**
  
Microsoft gestartet Teams chatdaten für lokale Benutzer auf 31 Januar 2018 gespeichert. So, wenn die Identität eines Benutzers Teams lokalen seit diesem Datum zwischen Active Directory und Azure Active Directory synchronisiert wurde, klicken Sie dann ihre Teams chatdaten werden in einem cloudbasierten Postfach gespeichert und werden durchsuchbar Inhaltssuche verwenden. Microsoft ist auch für das Speichern von Teams chatdaten aus, bevor Sie 31 Januar 2018 in die Cloud-basierten Postfächer für lokale Benutzer arbeiten. Weitere Informationen zu diesem wird bald verfügbar sein.

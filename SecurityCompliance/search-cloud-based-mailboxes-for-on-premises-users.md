---
title: Durchsuchen von cloudbasierten Postfächern für lokale Benutzer in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Verwenden Sie das Inhaltssuche-Tool im Office 365 &amp; Security Compliance Center, um verläuft-Chat Daten (als 1xN-Chats bezeichnet) für lokale Benutzer in einer Exchange-hybridbereitstellung zu suchen und zu exportieren.
ms.openlocfilehash: 148a5766342fcdd52e0505a59729cad3d2993908
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296698"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Durchsuchen von cloudbasierten Postfächern für lokale Benutzer in Office 365

Wenn Ihre Organisation über eine Exchange-hybridbereitstellung verfügt und Microsoft Teams aktiviert hat, können Benutzer die Chat Anwendung Teams für Instant Messaging verwenden. Für den cloudbasierten Benutzer werden die Teams-Chatdaten (auch als 1xN-Chats bezeichnet) in Ihrem primären cloudbasierten Postfach gespeichert. Wenn ein lokale Benutzer die Team Chat Anwendung verwendet, befindet sich Ihr primäres Postfach lokal. Um diese Einschränkung zu umgehen, hat Microsoft ein neues Feature veröffentlicht, bei dem ein Cloud-basierter Speicherbereich (als Cloud-basiertes Postfach für lokale Benutzer bezeichnet) erstellt wird, um Teams-Chatdaten für lokale Benutzer zu speichern. Auf diese Weise können Sie das Inhaltssuche-Tool im Office 365 &amp; Security Compliance Center verwenden, um Teams-Chatdaten für lokale Benutzer zu durchsuchen und zu exportieren. 
  
Hier sind die Anforderungen und Einschränkungen für das Einrichten und einrichten und Durchsuchen von Cloud-basierten Postfächern für lokale Benutzer:
  
- Die Benutzerkonten in Ihrem lokalen Verzeichnisdienst (wie Active Directory) müssen mit Azure Active Directory synchronisiert werden, dem Verzeichnisdienst in Office 365. Dies bedeutet, dass ein e-Mail-Benutzerkonto in Office 365 erstellt wird und einem Benutzer zugeordnet ist, dessen primäres Postfach sich in der lokalen Organisation befindet.
    
- Das Cloud-basierte Postfach für lokale Benutzer wird nur für Speicher Teams-Chat Daten verwendet. Ein lokale Benutzer kann sich nicht bei dem cloudbasierten Postfach oder Zugriff anmelden. Sie kann nicht zum Senden oder empfangen von e-Mail-Nachrichten verwendet werden. 
    
- Sie müssen eine Anforderung an den Microsoft-Support senden, damit Ihre Organisation nach Teams-Chat Daten in den cloudbasierten Postfächern für lokale Benutzer suchen kann. Weitere Informationen finden Sie unter [Einreichen einer Anforderung beim Microsoft-Support, um &amp; diese Funktion im Security Compliance Center](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) in diesem Artikel zu aktivieren. 
    
 **Hinweis:** Teams-Kanal Unterhaltungen werden immer im cloudbasierten Postfach gespeichert, das dem Team zugeordnet ist. Das kann bedeuten, dass Sie die Inhaltssuche verwenden können, um Kanal Unterhaltungen zu durchsuchen, ohne eine Supportanfrage einreichen zu müssen. Weitere Informationen zum Durchsuchen von Teams-Kanal Unterhaltungen finden Sie unter [Suchen von Microsoft Teams und Office 365-Gruppen](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Funktionsweise

Wenn ein Microsoft Teams-aktivierter Benutzer über ein lokales Postfach verfügt und Ihr Benutzerkonto/Ihre Identität mit der Cloud synchronisiert wurde, erstellt Microsoft ein cloudbasierten Postfach zum Speichern von 1xN Teams-Chat Daten. Nachdem die Teams Chat-Daten im cloudbasierten Postfach gespeichert wurden, werden Sie für die Suche indiziert. Dadurch können Sie die Inhaltssuche (und Suchvorgänge im Zusammenhang mit eDiscovery-Fällen) verwenden, um Teams-Chatdaten für lokale Benutzer zu suchen, in der Vorschau anzuzeigen und zu exportieren. sie können auch ** \*ComplianceSearch** -cmdlets im Office 365 Security &amp; Compliance Center PowerShell verwenden, um nach Teams-chat daten für lokale benutzer zu suchen. 
  
Die folgende Grafik zeigt den Workflow, wie Teams Chat-Daten für lokale Benutzer für die Suche, Vorschau und Export verfügbar sind.
  
![Cloud-basierter Speicher für lokale Benutzer in Microsoft Teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
Zusätzlich zu dieser neuen Funktion können Sie die Inhaltssuche weiterhin für die Suche, Vorschau und Export von Teams-Inhalten auf der cloudbasierten SharePoint-Website und im Exchange-Postfach verwenden, die den einzelnen Microsoft Teams-und 1xN Teams-Chatdaten im Exchange Online-Postfach zugeordnet sind. Cloud-basierte Benutzer.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a>Einreichen einer Anforderung beim Microsoft-Support, um diese Funktion im Security &amp; Compliance Center zu aktivieren

Sie müssen eine Anforderung beim Microsoft-Support einreichen, damit Ihre Organisation die grafische Benutzeroberfläche im Security &amp; Compliance Center verwenden kann, um in den cloudbasierten Postfächern für lokale Benutzer nach Teams-Chat Daten zu suchen. Beachten Sie, dass diese Funktion in Office 365 Security &amp; Compliance Center PowerShell verfügbar ist. Sie müssen keine Supportanforderung senden, um PowerShell für die Suche nach Teams-Chat Daten für lokale Benutzer zu verwenden. 
  
Schließen Sie die folgenden Informationen ein, wenn Sie die Anforderung an den Microsoft-Support übermitteln:
  
- Der Standarddomänenname Ihrer Office 365-Organisation.
    
- Der Mandantenname und die Mandanten-ID Ihrer Office 365-Organisation. Sie finden diese im Azure Active Directory-Portal (unter Eigenschaften **Verwalten** \> ****). Weitere Informationen finden Sie unter [Suchen Ihrer Office 365-mandantEN-ID](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).
    
- Der folgende Titel oder eine Beschreibung des Zwecks der Supportanforderung: "Aktivieren der Anwendungsinhalts Suche für lokale Benutzer". Dadurch wird die Anforderung an das Office 365 eDiscovery Engineering-Team weitergeleitet, das die Anforderung implementiert. 
    
Nach der technischen Änderung sendet Ihnen der Microsoft-Support einen geschätzten Bereitstellungstermin zu. Beachten Sie, dass der Bereitstellungsprozess in der Regel 2-3 Wochen dauert, nachdem Sie die Supportanfrage übermittelt haben. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>Was geschieht, wenn dieses Feature aktiviert ist?

Nachdem dieses Feature in Ihrer Office 365-Organisation bereitgestellt wurde, werden die folgenden Änderungen in der Inhaltssuche und in Suchvorgängen vorgenommen, die mit einem &amp; eDiscovery-Fall im Security Compliance Center verknüpft sind:
  
- Das Kontrollkästchen **Office-App-Inhalte für lokale Benutzer hinzufügen** wird unter den **Speicherorten** in der Inhaltssuche hinzugefügt. 
    
    ![Das Kontrollkästchen "Office-App-Inhalte für lokale Benutzer hinzufügen" wird zur Benutzeroberfläche der Inhaltssuche hinzugefügt.](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Lokale Benutzer werden in der Auswahl der inhaltsspeicherorte angezeigt, die Sie verwenden, um die zu durchsuchenden Benutzerpostfächer auszuwählen. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Suchen nach Teams-Chat Inhalten in Cloud-basierten Postfächern für lokale Benutzer

Nachdem das Feature aktiviert wurde, können Sie die Inhaltssuche im Security &amp; Compliance Center verwenden, um nach Teams-Chat Daten in den cloudbasierten Postfächern für lokale Benutzer zu suchen. 
  
1. Wechseln Sie im &amp; Security Compliance Center zu Such **Suche &amp; ** \> - **Inhalts** Suche
    
2. Klicken Sie **** ![auf der Seite suchen auf Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) für **neue Suche**hinzufügen.
    
    Wie bereits erläutert, wird das Kontrollkästchen **Office-App-Inhalte für lokale Benutzer hinzufügen** unter **Speicherorte**angezeigt. Beachten Sie, dass es standardmäßig ausgewählt ist.
    
3. Erstellen Sie die Stichwortabfrage, und fügen Sie der Suchabfrage bei Bedarf Bedingungen hinzu. Wenn Sie nur nach Team Chat Daten suchen möchten, können Sie die folgende Abfrage im Feld **Schlüsselwörter** hinzufügen: 
    
    ```
    kind:im
    ``` 

4. An diesem Punkt können Sie eine der folgenden Optionen unter **Speicherorte**auswählen:
    
    - **Alle Standorte** – wählen Sie diese Option aus, um die Postfächer aller Benutzer in Ihrer Organisation zu durchsuchen. Wenn das Kontrollkästchen aktiviert ist, werden auch alle cloudbasierten Postfächer für lokale Benutzer durchsucht. 
    
    - **Bestimmte Standorte** – wählen Sie diese Option aus, und klicken Sie dann auf **ändern** \> , Benutzer, Gruppen oder Teams auswählen, um bestimmte Postfächer zu durchsuchen. Wie bereits erläutert, können Sie in der Speicherort Auswahl nach lokalen Benutzern suchen. 
    
5. Speichern Sie die Suche, und führen Sie Sie aus. Alle Suchergebnisse aus den cloudbasierten Postfächern für lokale Benutzer können wie alle anderen Suchergebnisse in der Vorschau angezeigt werden. Darüber hinaus können Sie die Suchergebnisse (einschließlich aller Teams Chat-Daten) in eine PST-Datei exportieren. Weitere Informationen finden Sie unter: 
    
    - [Erstellen einer neuen Suche](content-search.md#create-a-new-search)
    
    - [Vorschau auf Suchergebnisse anzeigen](content-search.md#preview-search-results)
    
    - [Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Verwenden von PowerShell zum Suchen nach Teams-Chat Daten in cloudbasierten Postfächern für lokale Benutzer

Sie können die Cmdlets **New-ComplianceSearch** und **Set-ComplianceSearch** im Office 365 Security &amp; Compliance Center PowerShell verwenden, um das Cloud-basierte Postfach für lokale Benutzer zu durchsuchen. Wie bereits erläutert, müssen Sie keine Supportanforderung zur Verwendung von PowerShell für die Suche nach Teams-Chat Daten für lokale Benutzer übermitteln. 
  
1. Stellen [Sie eine Verbindung mit &amp; der Office 365 Security Compliance Center-PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Führen Sie den folgenden PowerShell-Befehl aus, um einen neuen Inhalt zu erstellen durchsucht die cloudbasierten Postfächer von lokalen Benutzern.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    Der Parameter *IncludeUserAppContent* wird verwendet, um das Cloud-basierte Postfach für den Benutzer oder die Benutzer anzugeben, die durch den *ExchangeLocation* -Parameter angegeben werden. Der *AllowNotFoundExchangeLocationsEnabled* ermöglicht Cloud-basierte Postfächer für lokale Benutzer. Wenn Sie den `$true` Wert für diesen Parameter verwenden, versucht die Suche nicht, das vorhanden sein des Postfachs zu überprüfen, bevor es ausgeführt wird. Dies ist erforderlich, um die cloudbasierten Postfächer für lokale Benutzer zu durchsuchen, da diese Typen von Postfächern nicht als reguläre Postfächer aufgelöst werden. 
    
    Das folgende Beispiel sucht nach Teams-Chats (die Sofortnachrichten sind), die das Stichwort "Redstone" im cloudbasierten Postfach von Sara Davis enthalten, das ein lokale Benutzer in der Contoso-Organisation ist.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Nachdem Sie eine neue Suche erstellt haben, müssen Sie das Cmdlet **Start-ComplianceSearch** verwenden, um die Suche auszuführen. 
  
Weitere Informationen zu diesen Cmdlets finden Sie unter:
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Bekannte Probleme

- Derzeit können Sie nur Inhalte in Cloud-basierten Postfächern für lokale Benutzer suchen, in der Vorschau anzeigen und exportieren. Das Platzieren eines cloudbasierten Postfachs für einen lokalen Benutzer in einem mit einem eDiscovery-Fall verknüpften Haltebereich oder das Zuweisen dieser zu einer Office 365-Aufbewahrungsrichtlinie wird nicht unterstützt. 
    
- Die Inhaltsspeicherort Auswahl für eDiscovery-Speicherorte zeigt lokale Benutzer an und lässt Sie Sie auswählen. Wie zuvor erläutert, wird der Speicher jedoch nicht auf den lokalen Benutzer angewendet.
    
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

 **Wo befinden sich Cloud-basierte Postfächer für lokale Benutzer?**
  
Cloud-basierte Postfächer werden im gleichen Rechenzentrum wie Ihre Office 365-Organisation erstellt und gespeichert. 
  
 **Gibt es andere Anforderungen als das Einreichen einer Supportanfrage?**
  
 Wie bereits erläutert, müssen die Identitäten von Benutzern mit in-Prem-Postfächern mit ihrer cloudbasierten Organisation synchronisiert werden, damit für jedes lokale Benutzerkonto in Office 365 ein entsprechendes e-Mail-Benutzerkonto erstellt wird. Darüber hinaus muss Ihre Organisation über ein Office 365 Enterprise-Abonnement verfügen, beispielsweise ein Office 365 Enterprise E1, E3 oder E5-Abonnement. 
  
 **Besteht die Gefahr, dass die Teams-Chat Daten verloren gehen, wenn das lokale Postfach des Benutzers in die Cloud migriert wird?**
  
Nein. Wenn Sie das primäre Postfach eines lokalen Benutzers in die Cloud migrieren, werden die Teams-Chatdaten für diesen Benutzer zu Ihrem neuen cloudbasierten primären Postfach migriert.
  
 **Kann ich ein eDiscovery-Speicher-oder Office 365-Aufbewahrungsrichtlinien auf lokale Benutzer anwenden?**
  
Nein.
  
 **Kann die Inhaltssuche ältere Teams-Chats für lokale Benutzer suchen, bevor meine Organisation die Anforderung zur Aktivierung dieser Funktion eingereicht hat?**
  
Microsoft hat mit dem Speichern der Teams-Chatdaten für lokale Benutzer am 2018. Januar begonnen. Wenn also die Identität eines lokalen Teams-Benutzers seit diesem Datum zwischen Active Directory und Azure Active Directory synchronisiert wurde, werden Ihre Teams-Chat Daten in einem cloudbasierten Postfach gespeichert und können mithilfe der Inhaltssuche durchsucht werden. Microsoft arbeitet auch an der Speicherung von Teams Chat-Daten von vor dem 31. Januar 2018 in der cloudbasierten Postfächer für lokale Benutzer. Weitere Informationen zu diesem Thema werden in Kürze verfügbar sein.

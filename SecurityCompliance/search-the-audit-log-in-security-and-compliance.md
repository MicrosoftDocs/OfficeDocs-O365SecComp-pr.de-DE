---
title: Durchsuchen des Überwachungsprotokolls im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: Verwenden Sie das Security & Compliance Center, um das einheitliche Überwachungsprotokoll zu durchsuchen und Benutzer- und Administratoraktivitäten anzuzeigen, die es in Ihrer Office 365-Organisation gegeben hat.
ms.openlocfilehash: 79309a2145db53f38d5d3c3c29777571d56910ae
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "36165691"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Durchsuchen des Überwachungsprotokolls im Security & Compliance Center

## <a name="introduction"></a>Einführung

Wollen Sie herausfinden, ob ein Benutzer ein bestimmtes Dokument angezeigt oder ein Element aus seinem Postfach gelöscht hat? Wenn ja, verwenden Sie einfach das Office 365 Security and Compliance Center, um das einheitliche Überwachungsprotokoll zu durchsuchen und Benutzer- und Administratoraktivitäten anzuzeigen, die es in Ihrem Office 365-Unternehmen gegeben hat.
 Warum ein einheitliches Überwachungsprotokoll? Weil Sie so nach folgenden Arten von Benutzer- und Administratoraktivitäten in Office 365 suchen können:
  
- Benutzeraktivitäten in SharePoint Online und OneDrive for Business
    
- Benutzeraktivitäten in Exchange Online (Postfachüberwachungsprotokollierung)
  
- Administratoraktivitäten in SharePoint Online
    
- Administratoraktivitäten in Azure Active Directory (dem Verzeichnisdienst für Office 365)
    
- Administratoraktivitäten in Exchange Online (Exchange-Administratorüberwachungsprotokollierung)
    
- Aktivitäten von Benutzern und Administratoren in Sway
    
- eDiscovery-Aktivitäten im Security und Compliance Center
    
- Aktivitäten von Benutzern und Administratoren in Power BI
    
- Aktivitäten von Benutzern und Administratoren in Microsoft Teams

- Aktivitäten von Benutzern und Administratoren in Dynamics 365
    
- Aktivitäten von Benutzern und Administratoren in Yammer
 
- Aktivitäten von Benutzern und Administratoren in Microsoft Flow
    
- Aktivitäten von Benutzern und Administratoren in Microsoft Stream

- Aktivitäten von Analysten und Administratoren in Microsoft Workplace Analytics

- Aktivitäten von Benutzern und Administratoren in Microsoft PowerApps
    
   
## <a name="before-you-begin"></a>Bevor Sie beginnen

Lesen Sie die folgenden Punkte, bevor Sie mit dem Durchsuchen des Überwachungsprotokolls von Office 365 beginnen.
  
- Sie (oder ein anderer Administrator) müssen zuerst die Überwachungsprotokollierung aktivieren, bevor Sie mit dem Durchsuchen des Office 365-Überwachungsprotokolls beginnen können. Zum Aktivieren klicken Sie einfach im Security und Compliance Center auf der Seite **Durchsuchen des Überwachungsprotokolls** auf **Aufzeichnung von Benutzer- und Administratoraktivitäten starten**. (Wenn Sie diesen Link nicht sehen, wurde die Überwachungsprotokollierung für Ihre Organisation bereits aktiviert.) Daraufhin teilt Ihnen eine Meldung mit, dass das Überwachungsprotokoll vorbereitet wird und Sie in ein paar Stunden nach Abschluss der Vorbereitung eine Suche durchführen können. Dieser Vorgang ist nur einmal erforderlich. 
    
    > [!NOTE]
    > Wir sind dabei, die Überwachung standardmäßig zu aktivieren. Bis dahin können Sie diese Option gemäß der obigen Beschreibung aktivieren. 
  
- Ihnen wurde in Exchange Online eine entweder die Rolle „Überwachungsprotokolle nur anzeigen“ oder „Überwachungsprotokolle“ zugewiesen, um das Office 365-Überwachungsprotokoll zu durchsuchen. Standardmäßig sind diese Rollen im Exchange Admin Center zugewiesen den Rollengruppen „Complianceverwaltung“ und „Organisationsverwaltung“ auf der Seite **Berechtigungen**. Bitte beachten Sie, dass globale Administratoren in Office 365 und Microsoft 365 automatisch Mitglieder der Verwaltungsrollengruppe „Organisationsverwaltung“ in Exchange Online sind. Damit ein Benutzer die Möglichkeit hat, das Office 365-Überwachungsprotokoll mit minimalen Rechten zu durchsuchen, können Sie in Exchange Online eine benutzerdefinierte Rollengruppe erstellen, ihr die Rollen "Überwachungsprotokolle nur anzeigen" oder "Überwachungsprotokolle" hinzufügen und den Benutzer dann als Mitglied der neuen Rollengruppe hinzufügen. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Wenn Sie einem Benutzer auf der Seite **Berechtigungen** im Security and Compliance Center die Rolle „Überwachungsprotokolle nur anzeigen“ oder „Überwachungsprotokolle“ zuweisen, kann er das Office 365-Überwachungsprotokoll nicht durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuweisen. Der Grund dafür ist, dass es sich bei dem zugrundeliegenden Cmdlet, das für die Durchsuchung des Überwachungsprotokolls verwendet wird, um ein Exchange Online-Cmdlet handelt. 
  
- Wenn eine überwachte Aktivität von einem Benutzer oder Administrator ausgeführt wird, wird ein Überwachungsdatensatz erstellt und im Office 365-Überwachungsprotokoll Ihrer Organisation gespeichert. Die Zeitdauer, die ein Überwachungsdatensatz aufbewahrt (und im Überwachungsprotokoll durchsuchbar) ist, hängt von Ihrem Office 365-Abonnement und insbesondere vom Lizenztyp ab, der einem bestimmten Benutzer zugewiesen ist.

     - **Office 365 E3:** Überwachungsdatensätze werden 90 Tage lang aufbewahrt. Sie können das Überwachungsprotokoll also nach Aktivitäten durchsuchen, die innerhalb der letzten 90 Tage ausgeführt wurden.

     - **Office 365 E5:** Überwachungsdatensätze werden 90 Tage lang aufbewahrt. Die Möglichkeit zur Aufbewahrung von Überwachungsdatensätzen für ein Jahr kann möglicherweise für E5-Benutzer und Benutzer mit einer E3-Lizenz und einer Office 365 Advanced Compliance-Add-on-Lizenz verfügbar sein.

        > [!NOTE]
        > Das private Preview-Programm für die einjährige Aufbewahrungszeit für Überwachungseinträge für E5-Organisationen (oder für Benutzer in E3-Organisationen, die über erweiterte Compliance-Add-on-Lizenzen verfügen) ist für Neuregistrierungen nicht mehr verfügbar. Dieser Artikel wird aktualisiert, wenn der einjährige Aufbewahrungszeitraum in der öffentlichen Vorschau verfügbar oder zur allgemeinen Verfügbarkeit freigegeben ist.

- Wenn Sie die Überwachungsprotokollsuche in Office 365 für Ihre Organisation deaktivieren möchten, können Sie in der mit Ihrer Exchange Online-Organisation verbundenen Remote-PowerShell den folgenden Befehl ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Um die Überwachungssuche wieder zu aktivieren, können Sie den folgenden Befehl in der Exchange Online-PowerShell ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Weitere Informationen finden Sie unter [Deaktivieren der Überwachungsprotokollsuche in Office 365](turn-audit-log-search-on-or-off.md).
    
- Wie bereits gesagt, handelt es sich bei dem zugrundeliegenden Cmdlet zum Durchsuchen des Überwachungsprotokolls um ein Exchange Online-Cmdlet namens **Search-UnifiedAuditLog**. Das bedeutet, dass Sie anstelle der Seite **Überwachungsprotokollsuche** im Security and Compliance Center dieses Cmdlet zum Durchsuchen des Office 365-Überwachungsprotokolls verwenden können. Sie müssen dieses Cmdlet in der Remote-PowerShell ausführen, die mit Ihrer Exchange Online-Organisation verbunden ist. Weitere Informationen finden Sie unter [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776). 

    Informationen zum Exportieren der vom **Search-UnifiedAuditLog**-Cmdlet zurückgegebenen Suchergebnisse in eine CSV-Datei finden Sie im Abschnitt „Tipps zum Exportieren, konfigurieren und Anzeigen des Überwachungsprotokolls“ in [Exportieren und Anzeigen des Überwachungsprotokolls](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).  

- Wenn Sie programmgesteuert Daten aus dem Office 365-Überwachungsprotokoll herunterladen möchten, empfehlen wir die Verwendung der Office 365-Verwaltungsaktivitäts-API anstelle eines PowerShell-Skripts. Die Office 365-Verwaltungsaktivitäts-API ist ein REST-Webdienst, den Sie beim Entwickeln von Lösungen zur Überwachung von Vorgängen, der Sicherheit und Compliance für Ihre Organisation verwenden können. Weitere Informationen finden Sie in der [Referenz der Office 365-Verwaltungsaktivitäts-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).
    
- Nach dem Auftreten eines Ereignisses kann es bis zu 30 Minuten oder sogar bis zu 24 Stunden dauern, bis der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. Aus der folgenden Tabelle geht die Zeit hervor, die für die unterschiedlichen Dienste in Office 365 benötigt wird.
    
    |**Office 365-Dienste**|**30 Minuten**|**24 Stunden**|
    |:-----|:-----|:-----|
    |Advanced Threat Protection und Threat Intelligence  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (Benutzeranmeldungen)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (Administratorereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |Verhinderung von Datenverlust  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
    |Dynamics 365 CRM <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |eDiscovery  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Teams  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Security & Compliance Center  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |SharePoint Online und OneDrive for Business  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (Azure AD) ist der Verzeichnisdienst von Office 365. Das vereinheitlichte Überwachungsprotokoll enthält Benutzer-, Gruppen-, Anwendungs-, Domänen- und Verzeichnisaktivitäten, die im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal ausgeführt wurden. Eine vollständige Liste der Azure AD-Ereignisse finden Sie unter [Azure Active Directory-Überwachungsberichtsereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Die Überwachungsprotokollierung für Power BI ist standardmäßig nicht aktiviert. Wenn Sie im Office 365-Überwachungsprotokoll nach Power BI-Aktivitäten suchen möchten, müssen Sie die Überwachung für das Power BI-Verwaltungsportal aktivieren. Anweisungen hierzu finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI-Verwaltungsportal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
    
    
## <a name="search-the-audit-log"></a>Durchsuchen des Überwachungsprotokolls

Nachfolgend ist der Prozess zum Durchsuchen des Überwachungsprotokolls in Office 365 dargestellt. 
  
[Schritt 1: Durchführen einer Überwachungsprotokollsuche](#step-1-run-an-audit-log-search)
  
[Schritt 2: Anzeigen der Suchergebnisse](#step-2-view-the-search-results)

[Schritt 3: Filtern der Suchergebnisse](#step-3-filter-the-search-results)

[Schritt 4: Exportieren der Suchergebnisse in eine Datei](#step-4-export-the-search-results-to-a-file)



  
### <a name="step-1-run-an-audit-log-search"></a>Schritt 1: Durchführen einer Überwachungsprotokollsuche

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Verwenden Sie eine private Browsersitzung (keine gewöhnliche Sitzung) für den Zugriff auf das Security and Compliance Center, weil dadurch die Verwendung Ihrer Anmeldeinformationen verhindert wird. Um ein InPrivate-Browserfenster in Internet Explorer oder in Microsoft Edge zu öffnen, drücken Sie einfach STRG+UMSCHALT+P. Drücken Sie STRG+UMSCHALT+N, um eine private Browsersitzung in Google Chrome (ein sogenanntes „Inkognito-Fenster“) zu öffnen. 
  
2. Melden Sie sich mit Ihrem Geschäfts-, Schul- oder Unikonto bei Office 365 an.
    
3. Klicken Sie im Security & Compliance Center im linken links auf **Suchen** und dann auf **Überwachungsprotokollsuche**.
    
    Die Seite **Überwachungsprotokollsuche** wird angezeigt. 
    
    ![Konfigurieren Sie die Suchkriterien, und klicken Sie dann auf „Suchen“, um den Bericht auszuführen.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Sie müssen zuerst die Überwachungsprotokollierung aktivieren, bevor Sie eine Überwachungsprotokollsuche durchführen können. Wenn der Link zu **Aufzeichnung von Benutzer- und Administratoraktivitäten starten** angezeigt wird, klicken Sie darauf, um die Überwachung zu aktivieren. Wird dieser Link nicht angezeigt, wurde die Überprüfung für Ihre Organisation bereits aktiviert. 
  
4. Konfigurieren Sie die folgenden Suchkriterien: 
    
    a. **Aktivitäten** Klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Benutzer- und Administratoraktivitäten sind in Gruppen verwandter Aktivitäten angeordnet. Sie können bestimmte Aktivitäten auswählen oder auf den Namen der Aktivitätsgruppe klicken, um alle Aktivitäten in der Gruppe auszuwählen. Sie können auch auf eine ausgewählte Aktivität klicken, um die Auswahl aufzuheben. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungsprotokolleinträge für die ausgewählten Aktivitäten angezeigt. Durch Auswahl von **Ergebnisse für alle Aktivitäten anzeigen** werden Ergebnisse für alle Aktivitäten angezeigt, die von dem ausgewählten Benutzer oder der ausgewählten Benutzergruppe ausgeführt wurden. 
    
    Es werden mehr als 100 Benutzer- und Administratoraktivitäten im Office 365-Überwachungsprotokoll erfasst. Klicken Sie beim Thema dieses Artikels auf die Registerkarte **Überwachte Aktivitäten**, um die Beschreibungen der einzelnen Aktivitäten in den verschiedenen Office 365-Diensten anzuzeigen. 
    
    b. **Startdatum** und **Enddatum** Standardmäßig sind die letzten sieben Tage ausgewählt. Wählen Sie einen Datums- und Uhrzeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Das Datum und die Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Datumsbereich, den Sie angeben können, umfasst 90 Tage. Es wird ein Fehler angezeigt, wenn der ausgewählte Datumsbereich mehr als 90 Tage umfasst. 
    
    > [!TIP]
    > Wenn Sie den maximalen Datumsbereich von 90 Tagen verwenden, wählen Sie den aktuellen Zeitpunkt für das **Startdatum** aus. Andernfalls wird eine Fehlermeldung angezeigt, in der mitgeteilt wird, dass das Startdatum vor dem Enddatum liegt. Wenn Sie die Überwachung innerhalb der letzten 90 Tage aktiviert haben, kann der maximale Datumsbereich nicht vor dem Datum beginnen, an dem die Überwachung aktiviert wurde. 
  
    c. **Benutzer** Klicken Sie in dieses Feld, und wählen Sie dann einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. In der Liste der Ergebnisse werden die Überwachungsprotokolleinträge für die ausgewählte Aktivität angezeigt, die von den Benutzern ausgeführt wurde, die Sie in diesem Feld ausgewählt haben. Lassen Sie dieses Feld leer, um die Einträge für alle Benutzer (und Dienstkonten) in Ihrer Organisation zurückzugeben. 
    
    d. **Datei, Ordner oder Website** Geben Sie einen Datei- oder Ordnernamen ganz oder teilweise ein, um nach Aktivitäten für die Datei oder den Ordner zu suchen, die bzw. der das angegebene Schlüsselwort enthält. Sie können auch die URL einer Datei oder eines Ordners verwenden. Wenn Sie eine URL verwenden wollen, geben Sie unbedingt den vollständigen URL-Pfad ein. Falls Sie nur einen Teil der URL eingeben, verwenden Sie bitte keine Sonder- oder Leerzeichen. 
    
    Lassen Sie dieses Feld leer, um Einträge für alle Dateien und Ordner in Ihrer Organisation zurückzugeben.
    
   **TIPPS**

   - Wenn Sie nach allen Aktivitäten im Zusammenhang mit einer **Website** suchen, fügen Sie das Platzhaltersymbol (\*) hinter die URL ein, um alle Einträge für diese Website zurückzugeben, z. b. **„https://contoso-my.sharepoint.com/personal/*“**.

   - Wenn Sie nach allen Aktivitäten im Zusammenhang mit einer **Datei** suchen, fügen Sie das Platzhaltersymbol (\*) vor dem Dateinamen ein, um alle Einträge für diese Datei zurückzugeben, z. b. **„*Customer_Profitability_Sample.csv“**.
    

    
5. Klicken Sie auf **Suchen**, um die Suche anhand der Suchkriterien auszuführen.  
    
    Die Suchergebnisse werden geladen und nach wenigen Augenblicken unter **Ergebnisse** angezeigt. Nach Abschluss der Suche wird die Anzahl der gefundenen Ergebnisse angezeigt. Im Bereich **Ergebnisse** werden maximal 5.000 Ereignisse in Schritten von jeweils 150 Ereignissen angezeigt. Wenn mehr als 5.000 Ereignisse die Suchkriterien erfüllen, werden die aktuellsten 5.000 Ereignisse angezeigt. 
    
    ![Die Anzahl der Ergebnisse wird nach Abschluss der Suche angezeigt.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Tipps zum Suchen im Überwachungsprotokoll

- Durch Klicken auf den Aktivitätsnamen können Sie bestimmte Aktivitäten auswählen, nach denen gesucht werden soll. Sie können auch auf den Gruppennamen klicken, um nach allen Aktivitäten in einer Gruppe (z. B. **Datei- und Ordneraktivitäten**) zu suchen. Wenn eine Aktivität ausgewählt ist, können Sie darauf klicken, um die Auswahl aufzuheben. Sie können auch das Suchfeld verwenden, um die Aktivitäten anzuzeigen, die das von Ihnen eingegebene Schlüsselwort enthalten.
    
    ![Klicken Sie auf den Namen der Aktivitätsgruppe, um alle Aktivitäten auszuwählen.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Sie müssen **Ergebnisse für alle Aktivitäten anzeigen** in der Liste **Aktivitäten** auswählen, um Einträge aus dem Exchange-Administrator-Überwachungsprotokoll anzuzeigen. Bei Ereignissen aus diesem Überwachungsprotokoll wird der Name eines Cmdlets (z. B. **Set-Mailbox**) in der Spalte **Aktivität** unter den Ergebnissen angezeigt. Um weitere Informationen zu erhalten, klicken Sie auf die Registerkarte **überwachte Aktivitäten** in diesem Thema, und dann auf **Exchange-Administratoraktivitäten**.
    
    Ebenso gibt es einige Überwachungsaktivitäten, für die in der Liste **Aktivitäten** kein entsprechendes Element enthalten ist. Wenn Sie den Namen des Vorgangs für diese Aktivitäten kennen, können Sie nach allen Aktivitäten suchen und die Ergebnisse dann filtern, indem Sie den Vorgangsnamen in das Feld für die Spalte **Aktivität** eingeben. Weitere Informationen zum Filtern der Ergebnisse finden Sie unter [Schritt 3: Suchergebnisse filtern](#step-3-filter-the-search-results). 
    
- Klicken Sie auf **Auswahl aufheben**, um die aktuelle Auswahl von Suchkriterien aufzuheben. Der Datumsbereich wird auf die Standardeinstellung für die letzten sieben Tage zurückgesetzt. Sie können auch auf **Gesamte Auswahl aufheben, um Ergebnisse für alle Aktivitäten anzuzeigen** klicken, um die getroffene Auswahl von Aktivitäten aufzuheben. 
    
- Wenn 5,000 Ergebnisse gefunden werden, können Sie wahrscheinlich davon ausgehen, dass mehr als 5.000 Ereignisse die Suchkriterien erfüllen. Sie können entweder die Suchkriterien verfeinern und die Suche erneut durchführen, damit weniger Ergebnisse zurückgegeben werden, oder Sie können alle Suchergebnisse exportieren, indem Sie **Ergebnisse exportieren** \> **Alle Ergebnisse herunterladen** auswählen.

  
### <a name="step-2-view-the-search-results"></a>Schritt 2: Anzeigen der Suchergebnisse

Die Ergebnisse einer Überwachungsprotokollsuche werden unter **Ergebnisse** auf der Seite **Überwachungsprotokollsuche** angezeigt. Wie bereits erwähnt werden maximal 5.000 Ereignisse (ggf. die 5.000 neuesten Ereignisse) in Schritten von 150 Ereignissen angezeigt. Zum Anzeigen weiterer Ereignisse können Sie die Bildlaufleiste im Bereich **Ergebnisse** verwenden oder **UMSCHALT+ENDE** drücken, um die nächsten 150 Ereignisse anzuzeigen. 
  
Die Ergebnisse enthalten die folgenden Informationen zu den einzelnen Ereignissen, die bei der Suche zurückgegeben werden.
  
- **Datum:** Das Datum und die Uhrzeit (im UTC-Format), zu der das Ereignis auftrat. 
    
- **IP-Adresse:** Die IP-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. Die IP-Adresse wird im Adressformat IPv4 oder IPv6 angezeigt. 
    
- **Benutzer:** Der Benutzer (oder das Dienstkonto), der die Aktion ausführte, durch die das Ereignis ausgelöst wurde. 
    
- **Aktivität:** Die vom Benutzer ausgeführte Aktivität. Dieser Wert entspricht den Aktivitäten, die Sie in der Dropdownliste **Aktivitäten** ausgewählt haben. Bei einem Ereignis aus dem Exchange-Administratorüberwachungsprotokoll ist der Wert in dieser Spalte ein Exchange-Cmdlet. 
    
- **Element:** Das Objekt, das als Ergebnis der entsprechenden Aktivität erstellt oder geändert wurde. Dies kann z. B. die Datei sein, die angezeigt oder geändert wurde, oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben in dieser Spalte einen Wert. 
    
- **Detail:** Zusätzliche Informationen zu einer Aktivität. Auch hier weisen nicht alle Aktivitäten einen Wert auf. 
    
> [!TIP]
> Klicken Sie unter **Ergebnisse** auf eine Spaltenüberschrift, um die Ergebnisse zu sortieren. Sie können die Ergebnisse aufsteigend (von A nach Z) oder absteigend (von Z nach A) sortieren. Klicken Sie auf die Überschrift **Datum**, um die Ergebnisse vom ältesten zum neuesten oder vom neuesten zum ältesten zu sortieren. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Anzeigen der Details zu einem bestimmten Ereignis

Sie können weitere Details zu einem Ereignis anzeigen, indem Sie in der Liste der Suchergebnisse auf den Ereigniseintrag klicken. Daraufhin wird die Seite **Details** mit detaillierten Eigenschaften des Ereigniseintrags angezeigt. Die angezeigten Eigenschaften sind von dem Office 365-Dienst abhängig, in dem das Ereignis auftritt. Zum Anzeigen weiterer Details klicken Sie auf **Weitere Informationen**. Beschreibungen finden Sie in [Detaillierte Eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
![Klicken Sie auf „Weitere Informationen“, um die genauen Eigenschaften des Datensatzes für das Überwachungsprotokollereignis anzuzeigen.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern der Suchergebnisse

Zusätzlich zur Sortierung können Sie die Ergebnisse einer Überwachungsprotokollsuche auch filtern. Dies ist eine sehr hilfreiche Funktion, mit der Sie schnell die Ergebnisse für einen bestimmten Benutzer oder eine bestimmte Aktivität filtern können. Sie können zuerst eine breite Suche erstellen und dann die Ergebnisse schnell filtern, um nur bestimmte Ereignisse anzuzeigen. Anschließend können Sie die Suchkriterien einschränken und die Suche erneut durchführen, um eine kleinere, kompaktere Gruppe von Ergebnissen zurückzugeben.
  
So filtern Sie die Ergebnisse:
  
1. Führen Sie eine Überwachungsprotokollsuche aus.
    
2. Sobald die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse filtern**.
    
    Unter den einzelnen Spaltenüberschriften werden Felder für Schlüsselwörter angezeigt.
    
3. Klicken Sie auf eines der Felder unter einer Spaltenüberschrift, und geben Sie abhängig von der Spalte ein Wort oder einen Ausdruck ein, nach dem Sie filtern möchten. Die Ergebnisse werden dynamisch angepasst und die Ereignisse angezeigt, die den Filterkriterien entsprechen.
    
    ![Geben Sie unter „Filtern“ ein Wort ein, um Ereignisse anzuzeigen, die dem Filter entsprechen.](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Zum Löschen eines Filters klicken Sie auf das **X** im Filterfeld oder auf **Filterung ausblenden**.
    
> [!TIP]
> Zum Anzeigen von Ereignissen aus dem Exchange-Administratorüberwachungsprotokoll geben Sie einen Bindestrich (**-**) in das Filterfeld **Aktivität** ein. Dadurch werden Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Administratorereignisse angegeben sind. Anschließend können Sie die Cmdlet-Namen alphabetisch sortieren. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Schritt 4: Exportieren der Suchergebnisse in eine Datei

Sie können die Ergebnisse einer Überwachungsprotokollsuche in eine Datei mit kommagetrennten Werten (CSV) auf Ihren lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und Funktionen wie das Suchen, Sortieren, Filtern und Teilen einer einzelnen Spalte (die Zellen mit mehreren Eigenschaften enthält) in mehrere Spalten verwenden.
  
1. Führen Sie eine Überwachungsprotokollsuche aus, und bearbeiten Sie dann die Suchkriterien, bis Sie die gewünschten Ergebnisse erhalten.
    
2. Klicken Sie auf **Ergebnisse exportieren**, und wählen Sie eine der folgenden Optionen aus: 
    
     - **Geladene Ergebnisse speichern:** Wählen Sie diese Option aus, um nur die Einträge zu exportieren, die unter **Ergebnisse** auf der Seite **Überwachungsprotokollsuche** angezeigt werden. Die heruntergeladene CSV-Datei enthält dieselben Spalten (und Daten), die auch auf der Seite angezeigt werden (Datum, Benutzer, Aktivität, Element und Details). Eine zusätzliche Spalte (mit dem Namen **Mehr**) wird in die CSV-Datei aufgenommen und enthält weitere Informationen aus dem Überwachungsprotokolleintrag. Da Sie dieselben Ergebnisse exportieren, die auf der Seite **Überwachungsprotokollsuche** geladen werden (und angezeigt werden können), werden maximal 5.000 Einträge exportiert. 
    
     - **Alle Ergebnisse herunterladen:** Wählen Sie diese Option aus, um alle Einträge aus dem Office 365-Überwachungsprotokoll zu exportieren, die den Suchkriterien entsprechen. Wenn Sie eine große Menge von Suchergebnissen exportieren möchten, wählen Sie diese Option aus, um zusätzlich zu den 5.000 Ergebnissen, die auf der Seite **Überwachungsprotokollsuche** angezeigt werden können, alle Einträge aus dem Überwachungsprotokoll herunterzuladen. Mit dieser Option werden die unformatierten Daten aus dem Überwachungsprotokoll in eine CSV-Datei heruntergeladen, und es sind zusätzliche Informationen aus dem Überwachungsprotokolleintrag in einer Spalte mit dem Namen **AuditData** enthalten. Bei Auswahl dieser Exportoption kann das Herunterladen der Datei etwas länger dauern, da die Datei möglicherweise wesentlich größer als diejenige ist, die bei Auswahl einer anderen Option heruntergeladen wird.
    
       > [!IMPORTANT]
       > Aus seiner einzigen Suche in einer Protokolldatei können Sie maximal 50.000 Einträge in eine CSV-Datei herunterladen. Wenn 50.000 Einträge in die CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass mehr als 50.000 Ereignisse die Suchkriterien erfüllen. Wenn Sie mehr als diesen Grenzwert exportieren möchten, versuchen Sie es mit einem Datenbereich, um die Anzahl der Einträge im Überwachungsprotokoll zu verringern. Möglicherweise müssen Sie mehrere Suchläufe mit kleineren Datumsbereichen durchführen, um mehr als 50.000 Einträge zu exportieren. 
  
3. Nachdem Sie eine Exportoption ausgewählt haben, wird eine Meldung am unteren Rand des Fensters angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen, sie im Ordner "Downloads" oder in einem bestimmten Ordner zu speichern.
 
#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>Weitere Informationen zum Exportieren von Ergebnissen der Überwachungsprotokollsuche

- Wenn Sie alle Suchergebnisse herunterladen, enthält die CSV-Datei eine Spalte mit dem Namen **AuditData**, die zusätzliche Informationen zu jedem Ereignis enthält. Die Daten in dieser Spalte bestehen aus einem JSON-Objekt, das mehrere Eigenschaften aus den Überwachungsprotokolldaten enthält. Jedes *Eigenschaft:Wert*-Paar im JSON-Objekt wird durch ein Komma getrennt. Sie können das JSON-Transformationstool im Power Query-Editor in Excel verwenden, um die Spalte **AuditData** in mehrere Spalten aufzuteilen, sodass jede Eigenschaft im JSON-Objekt eine eigene Spalte besitzt. Dadurch können Sie nach einer oder mehreren dieser Eigenschaften sortieren und filtern. Schrittweise Anleitungen zum Transformieren des JSON-Objekts mit dem Power Query-Editor finden Sie unter [Exportieren, konfigurieren und Anzeigen von Überwachungsprotokolldaten](export-view-audit-log-records.md).
    
    Nachdem Sie die Spalte **AuditData** aufgeteilt haben, können Sie die Spalte **Aktionen** filtern, um die detaillierten Eigenschaften eines bestimmten Aktivitätstyps anzuzeigen. 
    
- Mit der Option **Alle Ergebnisse herunterladen** werden die unformatierten Daten aus dem Office 365-Überwachungsprotokoll in eine CSV-Datei heruntergeladen. Diese Datei enthält andere Spaltennamen (CreationDate, UserIds, Operation, AuditData) als die Datei, die bei Auswahl der Option **Geladene Ergebnisse speichern** heruntergeladen wird. Die Werte in den beiden CSV-Dateien können für dieselbe Aktivität ebenfalls unterschiedlich sein. So kann die Aktivität in der Spalte **Aktion** in der CSV-Datei einen anderen Wert als die „benutzerfreundliche“ Version aufweisen, die in der Spalte **Aktivität** auf der Seite **Überwachungsprotokollsuche** angezeigt wird. Ein Beispiel wäre „MailboxLogin“ im Vergleich zu „am Postfach angemeldeter Benutzer“.

- Wenn Sie alle Ergebnisse einer Suchabfrage herunterladen, die Ereignisse aus verschiedenen Office 365-Diensten umfasst, enthält die Spalte **AuditData** in der CSV-Datei unterschiedliche Eigenschaften, je nachdem, in welchem Dienst die Aktion ausgeführt wurde. Beispielsweise umfassen Einträge aus Azure AD-Überwachungsprotokollen eine Eigenschaft namens **ResultStatus**, die angibt, ob die Aktion erfolgreich war. Diese Eigenschaft ist bei Ereignissen in SharePoint nicht enthalten. SharePoint-Ereignisse weisen hingegen eine Eigenschaft auf, die die Website-URL für Aktivitäten im Zusammenhang mit Dateien und Ordnern angibt. Um diese Abweichungen möglichst gering zu halten, sollten Sie verschiedene Suchen verwenden, um die Ergebnisse für Aktivitäten aus einzelnen Diensten zu exportieren. 
    
    Eine Beschreibung vieler Eigenschaften, die in der Spalte **AuditData** in der CSV-Datei aufgelistet sind, wenn Sie alle Ergebnisse herunterladen, sowie Informationen zu den Diensten, bei denen die einzelnen Eigenschaften verwendet werden, finden Sie unter [Detaillierte Eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Überwachte Aktivitäten

In den Tabellen in diesem Abschnitt sind die Aktivitäten beschrieben, die in Office 365 überwacht werden. Sie können nach diesen Ereignissen suchen, indem Sie das Überwachungsprotokoll im Security and Compliance Center durchsuchen.
  
In diesen Tabellengruppen werden verwandte Aktivitäten oder die Aktivitäten eines bestimmten Office 365-Diensts gruppiert. Die Tabellen enthalten den „benutzerfreundlichen“ Anzeigenamen, der in der Dropdownliste **Aktivitäten** angezeigt wird, sowie den Namen des zugehörigen Vorgangs, der in den Detailinformationen eines Überwachungsdatensatzes und in der CSV-Datei erscheint, wenn Sie Ihre Suchergebnisse exportieren. Beschreibungen der Detailinformationen finden Sie in [Detaillierte Eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
Klicken Sie auf einen der folgenden Links, um zu einer bestimmten Tabelle zu gelangen.
  
||||
|:-----|:-----|:-----|
|[Datei- und Seitenaktivitäten](#file-and-page-activities)<br/> |[Ordneraktivitäten](#folder-activities)<br/> |[SharePoint-Listen Aktivitäten](#sharepoint-list-activities)<br/>|
|[Freigabe- und Zugriffsanforderungsaktivitäten](#sharing-and-access-request-activities)<br/> |[Synchronisierungsaktivitäten](#synchronization-activities)<br/> |[Websiteberechtigungsaktivitäten](#site-permissions-activities)<br/> |
|[Websiteverwaltungsaktivitäten](#site-administration-activities)<br/> |[Exchange-Postfachaktivitäten](#exchange-mailbox-activities)<br/> |[Sway-Aktivitäten](#sway-activities) <br/> |
|[Benutzerverwaltungsaktivitäten](#user-administration-activities) <br/> |[Azure AD-Gruppenverwaltungsaktivitäten](#azure-ad-group-administration-activities) <br/> |[Anwendungsverwaltungsaktivitäten](#application-administration-activities) <br/> |
|[Rollenverwaltungsaktivitäten](#role-administration-activities) <br/> |[Verzeichnisverwaltungsaktivitäten](#directory-administration-activities) <br/>|[eDiscovery-Aktivitäten](#ediscovery-activities) <br/> |
|[Advanced eDiscovery-Aktivitäten](#advanced-ediscovery-activities)<br/> |[Power BI-Aktivitäten](#power-bi-activities) <br/> |[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)<br/>|
|[Microsoft Teams-Aktivitäten](#microsoft-teams-activities) <br/> |[Yammer-Aktivitäten](#yammer-activities) <br/> |[Microsoft Flow-Aktivitäten für Abläufe](#microsoft-flow-activities) <br/>|
|[Microsoft PowerApps-Aktivitäten](#microsoft-powerapps)<br/>|[Microsoft Stream-Aktivitäten](#microsoft-stream-activities) <br/>|[Exchange-Administratoraktivitäten](#exchange-admin-audit-log)<br/>|
||||
  
### <a name="file-and-page-activities"></a>Datei- und Seitenaktivitäten
  
In der folgenden Tabelle sind die Datei- und Seitenaktivitäten in SharePoint Online und OneDrive for Business beschrieben.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Dateizugriff  <br/> |FileAccessed  <br/> |Der Benutzer oder das Systemkonto greift auf eine Datei zu.  <br/> |
|(kein)  <br/> |FileAccessedExtended  <br/> |Dies bezieht sich auf die Aktivität "Dateizugriff" (FileAccessed). Wenn dieselbe Person während eines längeren Zeitraums (bis zu drei Stunden) ständig auf eine Datei zugreift, wird ein FileAccessedExtended-Ereignis protokolliert. Die Protokollierung von FileAccessedExtended-Ereignissen dient dazu, die Anzahl von FileAccessed-Ereignissen zu verringern, die beim ständigen Zugriff auf eine Datei protokolliert werden. Auf diese Weise lässt sich der Stördatenverkehr von mehreren FileAccessed-Einträgen besser reduzieren, bei denen die Benutzeraktivität im Wesentlichen identisch ist, sodass Sie sich auf das ursprüngliche (und wichtigere) FileAccessed-Ereignis konzentrieren können.  <br/> |
|Konformitätsrichtlinienbezeichnung geändert<br/> |ComplianceSettingChanged<br/> |Eine Aufbewahrungsbezeichnung wurde auf ein Dokument angewendet oder daraus entfernt. Dieses Ereignis wird ausgelöst, wenn eine Aufbewahrungsbezeichnung manuell oder automatisch auf eine Nachricht angewendet wird.<br/> |
|Datensatzstatus in "gesperrt" geändert<br/> |LockRecord<br/> |Der Datensatzstatus einer Aufbewahrungsbezeichnung, die ein Dokument als Datensatz klassifiziert, wurde gesperrt. Dies bedeutet, dass das Dokument nicht geändert oder gelöscht werden kann. Nur Benutzer, denen mindestens die Berechtigung „Mitwirkender“ für eine Website zugewiesen ist, können den Datensatzstatus eines Dokuments ändern.<br/> |
|Datensatzstatus in "nicht gesperrt" geändert<br/> |UnlockRecord<br/> |Der Datensatzstatus einer Aufbewahrungsbezeichnung, die ein Dokument als Datensatz klassifiziert, wurde entsperrt. Dies bedeutet, dass das Dokument geändert oder gelöscht werden kann. Nur Benutzer, denen mindestens die Berechtigung „Mitwirkender“ für eine Website zugewiesen ist, können den Datensatzstatus eines Dokuments ändern.<br/><br/> |
|Datei eingecheckt  <br/> |FileCheckedIn  <br/> |Der Benutzer checkt ein Dokument ein, das er aus einer Dokumentbibliothek ausgecheckt hat.  <br/> |
|Datei ausgecheckt  <br/> |FileCheckedOut  <br/> |Der Benutzer checkt ein Dokument aus, das sich in einer Dokumentbibliothek befindet. Benutzer können alle Dokumente, die für sie freigegeben wurden, auschecken oder ändern.  <br/> |
|Datei kopiert  <br/> |FileCopied  <br/> |Der Benutzer kopiert ein Dokument von einer Website. Die kopierte Datei kann in einem anderen Ordner auf der Website gespeichert werden.  <br/> |
|Datei gelöscht  <br/> |FileDeleted  <br/> |Der Benutzer löscht ein Dokument von einer Website.  <br/> |
|Datei aus Papierkorb gelöscht  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem Papierkorb einer Website.  <br/> |
|Datei aus endgültigem Papierkorb gelöscht  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem endgültigen Papierkorb einer Website.  <br/> |
|Konformitätsrichtlinienbezeichnung gelöscht<br/> |ComplianceRecordDelete<br/> |Ein Dokument, das als Datensatz klassifiziert wurde, wurde gelöscht. Ein Dokument wird als Datensatz betrachtet, wenn eine Aufbewahrungsbezeichnung, die Inhalte als Datensatz klassifiziert, auf das Dokument angewendet wird. <br/> |
|Konflikt in Bezug auf die Vertraulichkeitskennzeichnung eines Dokuments <br/>|DocumentSensitivityMismatchDetected<br/>|Der Benutzer lädt ein Dokument hoch, das mit einer Vertraulichkeitskennzeichnung klassifiziert wurde, die eine höhere Priorität hat als der die Vertraulichkeitskennzeichnung, die auf die Website angewendet wird, auf die das Dokument hochgeladen wird. Dieses Ereignis wird nicht ausgelöst, wenn die auf eine Website angewendete Vertraulichkeitskennzeichnung eine höhere Priorität hat als die auf ein Dokument, das auf die Website hochgeladen wurde, angewendete Vertraulichkeitskennzeichnung. Weitere Informationen zur Priorität von Vertraulichkeitskennzeichnungen finden Sie im Abschnitt „Prioritäten von Kennzeichen in [Übersicht über Vertraulichkeitsbezeichnungen](sensitivity-labels.md#label-priority-order-matters).<br/>|
|Malware in einer Datei erkannt  <br/> |FileMalwareDetected  <br/> |Der SharePoint-Virenschutz erkennt Schadsoftware in einer Datei.  <br/> |
|Auschecken einer Datei verworfen  <br/> |FileCheckOutDiscarded  <br/> |Der Benutzer verwirft eine ausgecheckte Datei. Das bedeutet, dass alle Änderungen, die an der Datei vorgenommen wurden, während sie ausgecheckt war, verworfen und nicht in der Version des Dokuments in der Dokumentbibliothek gespeichert werden.  <br/> |
|Datei heruntergeladen  <br/> |FileDownloaded  <br/> |Der Benutzer lädt ein Dokument von einer Website herunter.  <br/> |
|Datei geändert  <br/> |FileModified  <br/> |Der Benutzer oder das Systemkonto ändert den Inhalt oder die Eigenschaften eines Dokuments auf einer Website.  <br/> |
|(keine)  <br/> |FileModifiedExtended  <br/> |Dies bezieht sich auf die Aktivität "Datei geändert" (FileModified). Wenn dieselbe Person während eines längeren Zeitraums (bis zu 3 Stunden) eine Datei ständig ändert, wird ein FileModifiedExtended-Ereignis protokolliert. Die Protokollierung von FileModifiedExtended-Ereignissen dient dazu, die Anzahl von FileModified-Ereignissen zu verringern, die bei ständiger Änderung einer Datei protokolliert werden. Auf diese Weise lässt sich der Stördatenverkehr von mehreren FileModified-Einträgen besser reduzieren, bei denen die Benutzeraktivität im Wesentlichen identisch ist, sodass Sie sich auf das ursprüngliche (und wichtigere) FileModified-Ereignis konzentrieren können.  <br/> |
|Datei verschoben  <br/> |FileMoved  <br/> |Der Benutzer verschiebt ein Dokument von seinem aktuellen Speicherort auf einer Website an einen neuen Speicherort.  <br/> |
|(keine)  <br/> |FilePreviewed  <br/> |Ein Benutzer zeigt eine Vorschau einer Datei auf einer SharePoint- oder OneDrive for Business-Website an. Diese Ereignisse treten in der Regel in großem Umfang basierend auf einer einzelnen Aktivität auf, z. B. der Anzeige einer Bildergalerie.  <br/> |
|Alle Nebenversionen einer Datei in den Papierkorb verschoben  <br/> |FileVersionsAllMinorsRecycled  <br/> |Benutzer löscht alle Nebenversionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Alle Versionen der Datei in den Papierkorb  <br/> |FileVersionsAllRecycled  <br/> |Benutzer löscht alle Versionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Dateiversion in den Papierkorb  <br/> |FileVersionRecycled  <br/> |Benutzer löscht eine Version aus dem Versionsverlauf einer Datei. Die gelöschte Version wird in den Papierkorb der Website verschoben.  <br/> |
|Datei umbenannt  <br/> |FileRenamed  <br/> |Der Benutzer benennt ein Dokument auf einer Website um.  <br/> |
|Datei wiederhergestellt  <br/> |FileRestored  <br/> |Der Benutzer stellt ein Dokument aus dem Papierkorb einer Website wieder her.  <br/> |
|Datei hochgeladen  <br/> |FileUploaded  <br/> |Der Benutzer lädt ein Dokument in einen Ordner auf einer Website hoch.  <br/> |
|Seite angezeigt  <br/> |PageViewed  <br/> |Der Benutzer zeigt eine Seite auf einer Website an. Dieser Vorgang schließt nicht das Verwenden eines Webbrowsers zum Anzeigen von in Dokumentbibliotheken gespeicherten Dateien ein.  <br/> |
|(keine)  <br/> |PageViewedExtended  <br/> |Dies bezieht sich auf die Aktivität "Seite angezeigt" (PageViewed). Wenn dieselbe Person während eines längeren Zeitraums (bis zu 3 Stunden) eine Webseite ständig anzeigt, wird ein PageViewedExtended-Ereignis protokolliert. Die Protokollierung von PageViewedExtended-Ereignissen dient dazu, die Anzahl von PageViewed-Ereignissen zu verringern, die beim ständigen Anzeigen einer Seite protokolliert werden. Auf diese Weise lässt sich der Stördatenverkehr von mehreren PageViewed-Einträgen besser reduzieren, bei denen die Benutzeraktivität im Wesentlichen identisch ist, sodass Sie sich auf das ursprüngliche (und wichtigere) PageViewed-Ereignis konzentrieren können.  <br/> |
|Aufruf wird vom Client signalisiert <br/>|ClientViewSignaled<br/>|Ein Benutzerclient (z. b. eine Website oder einer mobile App) hat signalisiert, dass die angegebene Seite vom Benutzer aufgerufen wurde. Diese Aktivität wird häufig nach einem PagePrefetched-Ereignis für eine Seite protokolliert. <br/><br/>**Hinweis**: Da ClientViewSignaled-Ereignisse vom Client und nicht vom Server signalisiert werden, ist es möglich, dass das Ereignis nicht vom Server protokolliert wird und daher im Überwachungsprotokoll nicht auftaucht. Es ist auch möglich, dass die Informationen im Überwachungsdatensatz möglicherweise nicht zuverlässig sind. Da die Identität des Benutzers aber durch das Token überprüft wird, mit dem das Signal erstellt wurde, ist die im entsprechenden Überwachungsdatensatz aufgelistete Identität des Benutzers korrekt. |
|(keine) <br/>|PagePrefetched<br/>|Der Client eines Benutzers (beispielsweise eine Website oder eine Mobile App) hat die angegebene Seite angefordert, um die Leistung zu verbessern, wenn der Benutzer zu ihr navigiert. Dieses Ereignis wird protokolliert, um anzugeben, dass der Seiteninhalt für den Client des Benutzers bereitgestellt wurden. Dieses Ereignis ist kein definitiver Hinweis darauf, dass der Benutzer zu der Seite navigiert ist. Wenn der Seiteninhalt vom Client (gemäß der Anforderung des Benutzers) gerendert wird, sollte ein ClientViewSignaled-Ereignis generiert werden. Nicht alle Clients unterstützen Prefetches, und daher werden einige möglicherweise stattdessen als PageViewed-Ereignisse protokolliert.<br/>|
||||
  
### <a name="folder-activities"></a>Ordneraktivitäten
  
In der folgenden Tabelle sind die Ordneraktivitäten in SharePoint Online und OneDrive for Business beschrieben.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Ordner kopiert  <br/> |FolderCopied  <br/> |Ein Benutzer in SharePoint oder OneDrive for Business kopiert einen Ordner von einer Website zu einer anderen.  <br/> |
|Ordner erstellt  <br/> |FolderCreated  <br/> |Der Benutzer erstellt einen Ordner auf einer Website.  <br/> |
|Ordner gelöscht  <br/> |FolderDeleted  <br/> |Der Benutzer löscht einen Ordner von einer Website.  <br/> |
|Ordner aus Papierkorb gelöscht  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Der Benutzer löscht einen Ordner aus dem Papierkorb auf einer Website.  <br/> |
|Ordner aus endgültigem Papierkorb gelöscht  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Der Benutzer löscht einen Ordner aus dem endgültigen Papierkorb auf einer Website.  <br/> |
|Ordner geändert  <br/> |FolderModified  <br/> |Der Benutzer ändert einen Ordner auf einer Website. Dies schließt das Ändern der Ordnermetadaten, beispielsweise das Ändern von Tags und Eigenschaften, ein.  <br/> |
|Ordner verschoben  <br/> |FolderMoved  <br/> |Der Benutzer verschiebt einen Ordner an eine andere Position auf einer Website.  <br/> |
|Ordner umbenannt  <br/> |FolderRenamed  <br/> |Der Benutzer benennt einen Ordner auf einer Website um.  <br/> |
|Ordner wiederhergestellt  <br/> |FolderRestored  <br/> |Der Benutzer stellt einen gelöschten Ordner aus dem Papierkorb auf einer Website wieder her.  <br/> |
||||
  
### <a name="sharepoint-list-activities"></a>SharePoint-Listen Aktivitäten
  
In der folgenden Tabelle sind die Aktivitäten im Zusammenhang mit der Interaktion zwischen Benutzern und Listenelementen in SharePoint Online beschrieben.

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
| Liste erstellt              | ListCreated              | Ein Benutzer hat eine SharePoint-Liste erstellt.|
| Listenspalte erstellt       | ListColumnCreated        | Ein Benutzer hat eine Listenspalte in einer SharePoint-Liste erstellt. Eine Listenspalte ist eine Spalte, die mit einer oder mehreren SharePoint-Listen verbunden ist. |
| Listeninhaltstyp erstellt | ListContentTypeCreated   | Ein Benutzer hat einen Listeninhaltstyp erstellt. Eine Listeninhaltstyp ist ein Inhaltstyp, der mit einer oder mehreren SharePoint-Listen verbunden ist.|
| Listenelement erstellt         | ListItemCreated          | Ein Benutzer hat ein Element in einer vorhandenen SharePoint-Liste erstellt.|
| Websitespalte erstellt       | SiteColumnCreated        | Ein Benutzer hat eine Websitespalte in einer SharePoint-Liste erstellt. Eine Websitespalte ist eine Spalte, die keiner Liste angefügt ist. Eine Websitespalte ist auch eine Metadatenstruktur, die von jeder Liste in einem bestimmten Web verwendet werden kann.|
| Websiteinhaltstyp erstellt | Site ContentTypeCreated | Ein Benutzer hat einen Websiteinhaltstyp erstellt. Bei einem Websiteinhaltstyp handelt es sich um einen Inhaltstyp, der mit der übergeordneten Website verknüpft ist.|
| Liste gelöscht              | ListDeleted              | Ein Benutzer hat eine SharePoint-Liste gelöscht.|
| Listenspalte gelöscht       | ListColumnDeleted      | Ein Benutzer hat eine SharePoint-Listenspalte gelöscht.|
| Listeninhaltstyp gelöscht | ListContentTypeDeleted   | Ein Benutzer hat einen Listeninhaltstyp gelöscht. |
| Listenelement gelöscht         | ListItemDeleted        | Ein Benutzer hat ein Listenelement einer SharePoint-Liste gelöscht.|
| Websitespalte gelöscht       | SiteColumnDeleted        | Ein Benutzer hat eine Websitespalte in einer SharePoint-Liste gelöscht. |
| Websiteinhaltstyp gelöscht | SiteContentTypeDeleted   | Ein Benutzer hat einen Websiteinhaltstyp gelöscht.|
| Listenelement in den Papierkorb verschoben        | ListItemRecycled         | Ein Benutzer hat ein SharePoint-Listenelement in den Papierkorb verschoben.|
| Liste wiederhergestellt             | ListRestored             | Ein Benutzer hat eine SharePoint-Liste aus dem Papierkorb wiederhergestellt.|
| Listenelement wiederhergestellt        | ListItemRestored         | Ein Benutzer hat ein SharePoint-Listenelement aus dem Papierkorb wiederhergestellt.|
| Liste aktualisiert              | ListUpdated              | Ein Benutzer hat eine SharePoint-Liste aktualisiert, indem er eine oder mehrere Eigenschaften geändert hat.|
| Listenspalte aktualisiert       | ListColumnUpdated        | Ein Benutzer hat eine SharePoint-Listenspalte durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
| Listeninhaltstyp aktualisiert | ListContentTypeUpdated   | Ein Benutzer hat einen Listeninhaltstyp aktualisiert, indem er eine oder mehrere Eigenschaften geändert hat.|
| Listenelement aktualisiert         | ListItemUpdated          | Ein Benutzer hat ein SharePoint-Listenelement aktualisiert, indem er eine oder mehrere Eigenschaften geändert hat.|  
| Websitespalte aktualisiert       | SiteColumnUpdated        | Ein Benutzer hat eine SharePoint-Websitespalte durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
| Websiteinhaltstyp aktualisiert | SiteContentTypeUpdated   | Ein Benutzer hat einen Websiteinhaltstyp aktualisiert, indem er eine oder mehrere Eigenschaften geändert hat.|
||||

### <a name="sharing-and-access-request-activities"></a>Freigabe- und Zugriffsanforderungsaktivitäten 
  
In der folgenden Tabelle sind die Freigabe- und Zugriffsanforderungsaktivitäten in SharePoint Online und OneDrive for Business beschrieben. Bei Freigabeereignissen gibt die Spalte **Details** unter **Ergebnisse** den Namen des Benutzers oder der Gruppe an, für den oder die das Element freigegeben wurde. Außerdem wird angegeben, ob dieser Benutzer oder diese Gruppe Mitglied oder Gast in Ihrer Organisation ist. Weitere Informationen finden Sie unter [Verwenden der Freigabeüberwachung im Office 365-Überwachungsprotokoll](use-sharing-auditing.md).
  
> [!NOTE]
> Benutzer können je nach der Eigenschaft „UserType“ des Benutzerobjekts entweder *Mitglieder* oder *Gäste* sein. Ein Mitglied ist normalerweise ein Mitarbeiter, ein Gast ist ein Kooperationspartner außerhalb der Organisation. Wenn ein Benutzer eine Freigabeeinladung akzeptiert (und nicht bereits Mitglied Ihrer Organisation ist), wird im Verzeichnis Ihrer Organisation ein Gastkonto für diesen Benutzer erstellt. Nachdem der Gastbenutzer über ein Konto in Ihrem Verzeichnis verfügt, können Ressourcen unmittelbar mit ihm geteilt werden (ohne vorherige Einladung). 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Berechtigungsstufe zu Websitesammlung hinzugefügt  <br/> |PermissionLevelAdded  <br/> |Eine Berechtigungsstufe wurde zu einer Websitesammlung hinzugefügt.  <br/> |
|Zugriffsanforderung akzeptiert  <br/> |AccessRequestAccepted  <br/> |Eine Zugriffsanforderung für eine Website, einen Ordner oder ein Dokument wurde akzeptiert, und dem anfordernden Benutzer wurde der Zugriff gewährt.  <br/> |
|Akzeptierte Freigabeeinladung  <br/> |SharingInvitationAccepted  <br/> |Der Benutzer (Mitglied oder Gast) hat eine Freigabeeinladung akzeptiert, und der Zugriff auf die Ressource wurde gewährt. Dieses Ereignis enthält Informationen zu dem eingeladenen Benutzer sowie die E-Mail-Adresse, die für die Annahme der Einladung verwendet wurde (bei Adressen können unterschiedlich sein). Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, das beschreibt, in welcher Weise dem Benutzer der Zugriff auf die Ressource gewährt wurde, beispielsweise in dem der Benutzer einer Gruppe hinzugefügt wurde, die Zugriff auf die Ressource hat.  <br/> |
|Freigabeeinladung gesperrt  <br/> |SharingInvitationBlocked  <br/> | Eine von einem Benutzer in Ihrer Organisation gesendete Freigabeeinladung wird aufgrund einer Richtlinie für externe Freigabe blockiert, die die externe Freigabe auf Basis der Domäne des Empfängers zulässt oder verweigert. In diesem Fall wurde die Freigabeeinladung blockiert, weil:  <br/>  Die Domäne des Zielbenutzers nicht in der Liste der zulässigen Domänen enthalten ist.  <br/>  Oder:  <br/>  Die Domäne des Zielbenutzers in der Liste der blockierten Domänen enthalten ist.  <br/>  Weitere Informationen zum Zulassen oder Blockieren externer Freigaben basierend auf Domänen finden Sie unter [Eingeschränkte Domänenfreigabe in SharePoint Online und OneDrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Zugriffsanforderung erstellt  <br/> |AccessRequestCreated  <br/> |Der Benutzer fordert Zugriff auf eine Website, einen Ordner oder ein Dokument an, für deren Zugriff er über keine Berechtigungen verfügt.  <br/> |
|Unternehmensweit teilbarer Link erstellt   <br/> |CompanyLinkCreated  <br/> |Ein Benutzer hat einen unternehmensweit teilbaren Link zu einer Ressource erstellt. Unternehmensweite Links können nur von Mitgliedern Ihrer Organisation verwendet werden. Sie können nicht von Gästen genutzt werden.  <br/> |
|Anonymer Link erstellt  <br/> |AnonymousLinkCreated  <br/> |Ein Benutzer hat einen anonymen Link zu eine Ressource erstellt. Jeder, der über diesen Link verfügt, kann auf die Ressource zugreifen, ohne sich authentifizieren zu müssen.  <br/> |
|Sicherer Link erstellt  <br/> |SecureLinkCreated  <br/> |Für dieses Element wurde ein sicherer Freigabelink erstellt.  <br/> |
|Freigabeeinladung erstellt  <br/> |SharingInvitationCreated  <br/> |Ein Benutzer hat eine Ressource in SharePoint Online oder OneDrive for Business mit einem Benutzer geteilt, der sich nicht im Verzeichnis Ihrer Organisation befindet.  <br/> |
|Sicherer Link gelöscht  <br/> |SecureLinkDeleted  <br/> |Ein sicherer Freigabelink wurde gelöscht.  <br/> |
|Zugriffsanforderung verweigert   <br/> |AccessRequestDenied  <br/> |Eine Zugriffsanforderung auf eine Website, einen Ordner oder ein Dokument wurde verweigert.  <br/> |
|Unternehmensweit teilbarer Link entfernt  <br/> |CompanyLinkRemoved  <br/> |Ein Benutzer hat einen unternehmensweit teilbaren zu einer Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Anonymer Link entfernt  <br/> |AnonymousLinkRemoved  <br/> |Ein Benutzer hat einen anonymen Link zu eine Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Datei, Ordner oder Website freigegeben  <br/> |SharingSet  <br/> |Ein Benutzer (Mitglied oder Gast) hat eine Datei, einen Ordner oder eine Website in SharePoint oder OneDrive for Business mit einem Benutzer im Verzeichnis Ihrer Organisation geteilt. Der Wert in der Spalte **Detail** für diese Aktivität gibt den Namen des Benutzers an, mit dem die Ressource geteilt wurde, und ob es sich bei diesem Benutzer um ein Mitglied oder einen Gast handelt. Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, das beschreibt, in welcher Weise dem Benutzer der Zugriff auf die Ressource gewährt wurde. So kann beispielsweise der Benutzer einer Gruppe hinzugefügt werden, die Zugriff auf die Ressource hat.  <br/> |
|Zugriffsanforderung aktualisiert  <br/> |AccessRequestUpdated  <br/> |Eine Zugriffsanforderung für ein Element wurde aktualisiert.  <br/> |
|Anonymer Link aktualisiert   <br/> |AnonymousLinkUpdated  <br/> |Ein Benutzer hat einen anonymen Link zu eine Ressource aktualisiert. Das aktualisierte Feld wird beim Exportieren der Suchergebnisse in die EventData-Eigenschaft eingeschlossen.  <br/> |
|Freigabeeinladung aktualisiert  <br/> |SharingInvitationUpdated  <br/> |Eine externe Freigabeeinladung wurde aktualisiert.  <br/> |
|Anonymer Link verwendet  <br/> |AnonymousLinkUsed  <br/> |Ein anonymer Benutzer hat über einen anonymen Link auf eine Ressource zugegriffen. Die Identität des Benutzers ist möglicherweise nicht bekannt, Sie können jedoch andere Details wie die IP-Adresse des Benutzers anzeigen.  <br/> |
|Freigabe von Datei, Ordner oder Website aufgehoben  <br/> |SharingRevoked  <br/> |Ein Benutzer (Mitglied oder Gast) hat die Freigabe einer Datei, eines Ordners oder einer Website aufgehoben, die oder der zuvor mit einem anderen Benutzer geteilt wurde.  <br/> |
|Unternehmensweit teilbarer Link verwendet  <br/> |CompanyLinkUsed  <br/> |Ein Benutzer hat über einen unternehmensweit teilbaren Link auf eine Ressource zugegriffen.  <br/> |
|Sicherer Link verwendet  <br/> |SecureLinkUsed  <br/> |Ein Benutzer hat einen sicheren Link verwendet.  <br/> |
|Benutzer zu sicherem Link hinzugefügt  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die einen sicheren Freigabelink verwenden können.  <br/> |
|Benutzer wurde aus „sicherer Link“ entfernt  <br/> |RemovedFromSecureLink  <br/> |Ein Benutzer wurde von der Liste der Entitäten entfernt, die einen sicheren Freigabelink verwenden können.  <br/> |
|Freigabeeinladung zurückgezogen  <br/> |SharingInvitationRevoked  <br/> |Ein Benutzer hat eine Freigabeeinladung zu einer Ressource zurückgezogen.   <br/> |
||||
  
### <a name="synchronization-activities"></a>Synchronisierungsaktivitäten
  
In der folgenden Tabelle sind die Dateisychronisierungsaktivitäten in SharePoint Online und OneDrive for Business beschrieben.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Computer zum Synchronisieren von Dateien zugelassen  <br/> |ManagedSyncClientAllowed  <br/> |Der Benutzer richtet erfolgreich eine Synchronisierungsbeziehung mit einer Website ein. Die Synchronisierungsbeziehung ist erfolgreich, da der Computer des Benutzers Mitglied einer Domäne ist, die zur Liste der Domänen, die in Ihrer Organisation auf Dokumentbibliotheken zugreifen können (auch *Liste der sicheren Empfänger* genannt), hinzugefügt wurde.  <br/> Weitere Informationen zu dieser Funktion finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die in der Liste der sicheren Empfänger enthalten sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Computer für Synchronisieren von Dateien blockiert  <br/> |UnmanagedSyncClientBlocked  <br/> |Der Benutzer versucht, eine Synchronisierungsbeziehung mit einer Website von einem Computer aus einzurichten, der kein Mitglied der Domäne Ihrer Organisation ist oder ein Mitglied einer Domäne ist, die nicht zur Liste der Domänen (auch *Liste der sicheren Empfänger* genannt), die auf Dokumentbibliotheken in Ihrer Organisation zugreifen können, hinzugefügt wurde. Die Synchronisierungsbeziehung ist nicht zulässig, und der Computer des Benutzers ist für das Synchronisieren, Herunterladen oder Hochladen von Dateien der Dokumentbibliothek gesperrt.  <br/> Informationen zu dieser Funktion finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die in der Liste der sicheren Empfänger enthalten sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Dateien auf Computer heruntergeladen  <br/> |FileSyncDownloadedFull  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung ein und lädt zum ersten Mal erfolgreich Dateien aus einer Dokumentbibliothek auf seinen Computer herunter.  <br/> |
|Dateiänderungen auf Computer heruntergeladen  <br/> |FileSyncDownloadedPartial  <br/> |Der Benutzer lädt erfolgreich alle Änderungen an Dateien aus der Dokumentbibliothek herunter. Diese Aktivität gibt an, dass alle Änderungen, die an Dateien in der Dokumentbibliothek vorgenommen wurden, auf den Computer des Benutzers heruntergeladen wurden. Es wurden nur Änderungen heruntergeladen, da die Dokumentbibliothek zuvor vom Benutzer heruntergeladen wurde (wie durch die Aktivität **Dateien auf Computer heruntergeladen** angegeben).  <br/> |
|Dateien in Dokumentbibliothek hochgeladen  <br/> |FileSyncUploadedFull  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung ein und lädt zum ersten Mal erfolgreich Dateien von seinem Computer in eine Dokumentbibliothek hoch.  <br/> |
|Dateiänderungen in Dokumentbibliothek hochgeladen  <br/> |FileSyncUploadedPartial  <br/> |Der Benutzer lädt erfolgreich Änderungen an Dateien in eine Dokumentbibliothek hoch. Dieses Ereignis gibt an, dass alle Änderungen, die an der lokalen Version einer Datei aus einer Dokumentbibliothek vorgenommen wurden, erfolgreich in die Dokumentbibliothek geladen werden. Es werden nur Änderungen hochgeladen, da diese Dateien zuvor vom Benutzer hochgeladen wurden (wie durch die Aktivität **Dateien in Dokumentbibliothek hochgeladen** angegeben).  <br/> |
||||

### <a name="site-permissions-activities"></a>Websiteberechtigungsaktivitäten

In der folgenden Tabelle sind die Ereignisse im Zusammenhang mit dem Zuweisen von Berechtigungen in SharePoint und der Verwendung von Gruppen zum Gewähren (und Widerrufen) des Zugriffs auf Websites aufgelistet.

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Websitesammlungsadministrator hinzugefügt  <br/> |SiteCollectionAdminAdded  <br/> |Der Websitesammlungsadministrator oder -besitzer fügt eine Person als Websitesammlungsadministrator für eine Website hinzu. Websitesammlungsadministratoren verfügen über Vollzugriff für die Websitesammlung und alle Unterwebsites. Diese Aktivität wird ebenfalls protokolliert, wenn ein Administrator sich selbst Zugriff auf das OneDrive-Konto eines Benutzers gewährt (durch Bearbeiten des Benutzerprofils im SharePoint Admin Center oder [mithilfe des Microsoft 365 Admin Centers](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)). <br/> |
|Benutzer oder Gruppe zu SharePoint-Gruppe hinzugefügt  <br/> |AddedToGroup  <br/> |Ein Benutzer hat ein Mitglied oder einen Gast zu einer SharePoint-Gruppe hinzugefügt. Dies kann eine beabsichtigte Aktion oder das Ergebnis einer anderen Aktivität wie eines Freigabeereignisses gewesen sein.  <br/> |
|Vererbung der Berechtigungsstufe unterbrochen  <br/> |PermissionLevelsInheritanceBroken  <br/> |Ein Element wurde geändert, sodass es die Berechtigungsstufen nicht mehr vom übergeordneten Element erbt.  <br/> |
|Vererbung der Freigabe unterbrochen  <br/> |SharingInheritanceBroken  <br/> |Ein Element wurde geändert, sodass es die Freigabeberechtigung nicht mehr vom übergeordneten Element erbt.  <br/> |
|Gruppe erstellt  <br/> |GroupAdded  <br/> |Der Websiteadministrator oder -besitzer erstellt eine Gruppe für eine Website oder führt eine Aufgabe aus, die zur Erstellung einer Gruppe führt. Wenn ein Benutzer beispielsweise zum ersten Mal einen Link zum Freigeben einer Datei erstellt, wird eine Systemgruppe zur OneDrive for Business-Website hinzugefügt. Dieses Ereignis kann auch dadurch entstehen, dass ein Benutzer einen Link mit Bearbeitungsberechtigungen für eine freigegebene Datei erstellt.  <br/> |
|Gruppe gelöscht  <br/> |GroupRemoved  <br/> |Der Benutzer löscht eine Gruppe von einer Website.  <br/> |
|Zugriffsanforderungseinstellungen geändert  <br/> |WebRequestAccessModified  <br/> |Die Einstellungen für die Zugriffsanforderungseinstellungen wurden auf einer-Website geändert.  <br/> |
|Einstellung „Mitglieder können teilen“ geändert  <br/> |WebMembersCanShareModified  <br/> |Die Einstellung **Mitglieder können freigeben** wurde auf einer Website geändert.  <br/> |
|Berechtigungsstufe in Websitesammlung geändert  <br/> |PermissionLevelModified  <br/> |Eine Berechtigungsstufe in einer Websitesammlung wurde geändert.  <br/> |
|Websiteberechtigungen geändert  <br/> |SitePermissionsModified  <br/> |Der Websiteadministrator oder -besitzer (oder das Systemkonto) ändert die Berechtigungsstufe, die einer Gruppe auf einer Website zugeordnet ist. Diese Aktivität wird ebenfalls protokolliert, wenn alle Berechtigungen für eine Gruppe entfernt werden.  <br/><br/> **Hinweis:** Dieser Vorgang ist in SharePoint Online veraltet. Um verwandte Ereignisse zu finden, können Sie nach anderen Aktivitäten im Zusammenhang mit Berechtigungen suchen, z. B. **Websitesammlungsadministrator hinzugefügt**, **Benutzer oder Gruppe zu SharePoint-Gruppe hinzugefügt**, **Benutzer darf Gruppen erstellen**, **Gruppe erstellt** oder **Gruppe gelöscht**.|
|Berechtigungsstufe aus einer Websitesammlung gelöscht  <br/> |PermissionLevelRemoved  <br/> |Eine Berechtigungsstufe wurde aus einer Websitesammlung gelöscht.  <br/> |
|Websitesammlungsadministrator entfernt  <br/> |SiteCollectionAdminRemoved <br/> |Der Websitesammlungsadministrator oder -besitzer entfernt eine Person als Websitesammlungsadministrator für eine Website. Diese Aktivität wird ebenfalls protokolliert, wenn ein Administrator sich selbst von der Liste der Websitesammlungsadministratoren eines OneDrive-Kontos eines Benutzers entfernt (durch Bearbeiten des Benutzerprofils im SharePoint Admin Center).  Um diese Aktivität in den Suchergebnissen des Überwachungsprotokolls zurückzugeben, müssen Sie nach allen Aktivitäten suchen. <br/> |
|Benutzer oder Gruppe aus SharePoint-Gruppe entfernt  <br/> |RemovedFromGroup  <br/> |Ein Benutzer hat ein Mitglied oder einen Gast aus einer SharePoint-Gruppe entfernt. Dies kann eine beabsichtigte Aktion oder das Ergebnis einer anderen Aktivität wie dem Aufheben einer Freigabe gewesen sein.  <br/> |
|Website-Administratorberechtigungen angefordert  <br/> |SiteAdminChangeRequest  <br/> |Der Benutzer fordert an, als Websitesammlungsadministrator für eine Websitesammlung hinzugefügt zu werden. Websitesammlungsadministratoren verfügen über Vollzugriff für die Websitesammlung und alle Unterwebsites.  <br/> |
|Vererbung der Freigabe wiederhergestellt  <br/> |SharingInheritanceReset  <br/> |Eine Änderung wurde vorgenommen, sodass ein Element die Freigabeberechtigung vom übergeordneten Element erbt.  <br/> |
|Gruppe aktualisiert  <br/> |GroupUpdated  <br/> |Der Websiteadministrator oder -besitzer ändert die Einstellungen einer Gruppe für eine Website. Dazu kann das Ändern des Gruppennamens, das Anzeigen oder Bearbeiten der Gruppenmitgliedschaft und die Art der Verarbeitung von Mitgliedsanträgen gehören.  <br/> |
||||

  
### <a name="site-administration-activities"></a>Websiteverwaltungsaktivitäten
  
Die folgende Tabelle enthält die Ereignisse, die aus Websiteverwaltungsaufgaben in SharePoint Online resultieren.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Zulässigen Datenspeicherort festgelegt<br/>|AllowedDataLocationAdded|Ein SharePoint- oder globaler Administrator hat einen zulässigen Datenspeicherort in einer Multi-Geo-Umgebung hinzugefügt. <br/>|
|Ausgenommener Benutzer-Agent hinzugefügt  <br/> |ExemptUserAgentSet  <br/> |Ein SharePoint- oder globaler Administrator hat einen Benutzer-Agent zu der Liste der ausgenommenen Benutzer-Agents im SharePoint Admin Center hinzugefügt.  <br/> |
|Geografischer Standort-Administrator hinzugefügt<br/>|GeoAdminAdded<br/>|Ein SharePoint- oder globaler Administrator hat einen Benutzer als Geo-Administrator eines Standorts hinzugefügt. <br/>|
|Benutzer das Erstellen von Gruppen gestattet  <br/> |AllowGroupCreationSet  <br/> |Der Websiteadministrator oder -besitzer fügt eine Berechtigungsstufe zu einer Website hinzu, die einem Benutzer, dem diese Berechtigung zugewiesen wird, das Erstellen einer Gruppe für diese Website gestattet.   <br/> |
|Verschiebung der Websitegeografie abgebrochen  <br/> |SiteGeoMoveCancelled  <br/> |Ein SharePoint- oder globaler Administrator bricht erfolgreich eine Verschiebung der SharePoint-oder OneDrive-Websitegeografie ab. Mit der Multi-Geo-Funktion kann eine Office 365-Organisation mehrere Office 365-Rechenzentrumsregionen umfassen, die als „Geos“ bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Freigaberichtlinie geändert  <br/> |SharingPolicyChanged  <br/> |Ein SharePoint- oder globaler Administrator hat eine SharePoint-Freigaberichtlinie mithilfe des Office 365 Admin-Portals, des SharePoint Admin Portals oder der SharePoint Online Management Shell geändert. Alle Änderungen an den Einstellungen der Freigaberichtlinie in Ihrer Organisation werden protokolliert. Die geänderte Richtlinie wird im Feld **ModifiedProperties** in den Detailinformationen des Ereignisdatensatzes aufgeführt.  <br/> |
|Zugriffsrichtlinie des Geräts geändert  <br/> |DeviceAccessPolicyChanged  <br/> |Ein SharePoint- oder globaler Administrator hat die Richtlinie für nicht verwaltete Geräte in Ihrer Organisation geändert. Diese Richtlinie steuert den Zugriff auf SharePoint, OneDrive und Office 365 von Geräten, die Ihrer Organisation nicht beigetreten sind. Zum Konfigurieren dieser Richtlinie ist ein Enterprise Mobility + Security-Abonnement erforderlich. Weitere Informationen finden Sie unter [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).  <br/> |
|Ausgenommene Benutzer-Agents geändert  <br/> |CustomizeExemptUsers  <br/> |Ein SharePoint- oder globaler Administrator hat die Liste der ausgenommenen Benutzer-Agents im SharePoint Admin Center angepasst. Sie können festlegen, welche Benutzer-Agents vom Empfangen einer gesamten Webseite zum Indizieren ausgenommen werden sollen. Dies bedeutet: Wenn ein Benutzer-Agent, den Sie als ausgenommen Benutzer festgelegt haben, auf ein InfoPath-Formular stößt, wird das Formular als XML-Datei und nicht als komplette Webseite zurückgegeben. Dadurch wird die Indizierung von InfoPath-Formularen beschleunigt.  <br/> |
|Netzwerkzugriffsrichtlinie geändert  <br/> |NetworkAccessPolicyChanged  <br/> |Ein SharePoint- oder globaler Administrator hat die standortbasierte Zugriffsrichtlinie (auch als „Grenze des vertrauenswürdigen Netzwerks“ bezeichnet) im SharePoint Admin Center oder mithilfe der SharePoint PowerShell geändert. Dieser Richtlinientyp steuert, wer basierend auf von Ihnen festgelegten autorisierten IP-Adressbereichen Zugriff auf SharePoint- und OneDrive-Ressourcen in Ihrer Organisation hat. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf SharePoint Online- und OneDrive-Daten auf der Grundlage von definierten Netzwerkspeicherorten](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).  <br/> |
|Verschiebung der Websitegeografie abgeschlossen  <br/> |SiteGeoMoveCompleted  <br/> |Eine von einem globalen Administrator in Ihrer Organisation angesetzte Verschiebung der Websitegeografie wurde erfolgreich abgeschlossen. Mit der Multi-Geo-Funktion kann eine Office 365-Organisation mehrere Office 365-Rechenzentrumsregionen umfassen, die als „Geos“ bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Senden-an-Verbindung erstellt  <br/> |SendToConnectionAdded  <br/> |Ein SharePoint- oder globaler Administrator erstellt eine neue Senden-an-Verbindung auf der Verwaltungsseite für Datensätze im SharePoint Admin Center. Mit einer Senden-an-Verbindung werden die Einstellungen für ein Dokumentrepository oder ein Datenarchiv festgelegt. Wenn Sie eine Senden-an-Verbindung erstellen, kann eine Inhaltsorganisation Dokumente an den angegebenen Speicherort übermitteln.  <br/> |
|Websitesammlung erstellt  <br/> |SiteCollectionCreated  <br/> |Ein SharePoint- oder globaler Administrator erstellt eine Websitesammlung in Ihrer SharePoint Online-Organisation, oder ein Benutzer stellt seine OneDrive for Business-Website bereit.  <br/> |
|Verwaiste Hub-Website gelöscht<br/>|HubSiteOrphanHubDeleted<br/>|Ein SharePoint- oder globaler Administrator hat eine verwaiste Hub-Website gelöscht. Es handelt sich dabei um eine Hub-Website, der keine Websites zugeordnet sind. Ein verwaister Hub ist wahrscheinlich durch den Löschvorgang der ursprünglichen Hub-Website entstanden. <br/>|
|Senden-an-Verbindung gelöscht  <br/> |SendToConnectionRemoved  <br/> |Ein SharePoint- oder globaler Administrator löscht eine Senden-an-Verbindung auf der Verwaltungsseite für Datensätze im SharePoint Admin Center.  <br/> |
|Website gelöscht  <br/> |SiteDeleted  <br/> |Der Websiteadministrator löscht eine Website.  <br/> |
|Dokumentvorschau aktiviert  <br/> |PreviewModeEnabledSet  <br/> |Der Websiteadministrator aktiviert die Dokumentvorschau für eine Website.  <br/> |
|Älterer Workflow aktiviert  <br/> |LegacyWorkflowEnabledSet  <br/> |Der Websiteadministrator oder -besitzer fügt den SharePoint 2013-Workflowaufgaben-Inhaltstyp zur Website hinzu. Globale Administratoren können ebenfalls Workflows für die gesamte Organisation im SharePoint Admin Center aktivieren.  <br/> |
|Office on Demand aktiviert  <br/> |OfficeOnDemandSet  <br/> |Der Websiteadministrator aktiviert Office on Demand, wodurch Benutzer auf die neueste Version von Office-Desktopanwendungen zugreifen können. Office on Demand wird im SharePoint Admin Center aktiviert und erfordert ein Office 365-Abonnement, bei dem alle Office-Anwendungen installiert werden.  <br/> |
|Ergebnisquelle für Personensuchen aktiviert<br/>|PeopleResultsScopeSet<br/>|Der Websiteadministrator erstellt die Ergebnisquelle für Personensuchen für eine Website.<br/>|
|RSS-Feeds aktiviert  <br/> |NewsFeedEnabledSet  <br/> |Der Websiteadministrator oder -besitzer aktiviert RSS-Feeds für eine Website. Globale Administratoren können RSS-Feeds für die gesamte Organisation im SharePoint Admin Center aktivieren.  <br/> |
|Website mit Hub-Website verbunden<br/>|HubSiteJoined<br/>|Der Besitzer einer Website verknüpft seine Website mit einer Hub-Website.<br/>|
|Hub-Website registriert<br/>|HubSiteRegistered<br/>|Ein SharePoint- oder globaler Administrator erstellt eine Hub-Website. Das Ergebnis: Die Website ist als Hub-Website registriert. <br/>|
|Zulässigen Datenspeicherort entfernt<br/>|AllowedDataLocationDeleted<br/>|Ein SharePoint- oder globaler Administrator hat einen zulässigen Datenspeicherort aus einer Multi-Geo-Umgebung entfernt.<br/>|
|Geografischer Standort-Administrator entfernt<br/>|GeoAdminDeleted<br/>|Ein SharePoint- oder globaler Administrator hat einen Benutzer als Geo-Administrator eines Standorts entfernt.<br/>|
|Website umbenannt  <br/> |SiteRenamed  <br/> |Der Websiteadministrator oder -besitzer benennt eine Website um.  <br/> |
|Verschiebung der Websitegeografie geplant  <br/> |SiteGeoMoveScheduled  <br/> |Ein SharePoint- oder globaler Administrator plant erfolgreich eine Verschiebung der SharePoint-oder OneDrive-Websitegeografie. Mit der Multi-Geo-Funktion kann eine Office 365-Organisation mehrere Office 365-Rechenzentrumsregionen umfassen, die als „Geos“ bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Hostwebsite festgelegt  <br/> |HostSiteSet  <br/> |Ein SharePoint- oder globaler Administrator ändert die vorgesehene Website zum Hosten persönlicher oder OneDrive for Business-Websites.  <br/> |
|Ein Speicherkontingent für einen geografischen Standort wurde konfiguriert  <br/> |GeoQuotaAllocated<br/> |Ein SharePoint- oder globaler Administrator hat einen zulässigen Datenspeicherort in einer Multi-Geo-Umgebung konfiguriert.<br/> |
|Website von der Hub-Website gelöst<br/>|HubSiteUnjoined<br/>|Der Besitzer einer Website löst seine Website von einer Hub-Website.<br/>|
|Registrierung einer Hub-Website entfernt<br/>|HubSiteUnregistered<br/>|Ein SharePoint- oder globaler Administrator hat die Registrierung seiner Website als Hub-Website entfernt. Wenn die Registrierung einer Hub-Website aufgehoben wird, funktioniert sie nicht mehr als Hub-Website. <br/>|
||||
  
### <a name="exchange-mailbox-activities"></a>Exchange-Postfachaktivitäten
  
In der folgenden Tabelle sind die Aktivitäten aufgelistet, die von der Postfachüberwachungsprotokollierung erfasst werden können. Postfachaktivitäten, die vom Besitzer des Postfachs, einem delegierten Benutzer oder einem Administrator ausgeführt werden, werden automatisch 90 Tage lang im Office 365 Überwachungsprotokoll protokolliert. Ein Administrator kann die Postfachüberwachungsprotokollierung für alle Benutzer in Ihrer Organisation deaktivieren. In diesem Fall werden für alle Benutzer Postfachaktivitäten nicht protokolliert. Weitere Informationen finden Sie unter [Postfachüberwachungen verwalten](enable-mailbox-auditing.md).

 Sie können auch mithilfe des Cmdlets [Search-MailboxAuditLog in Exchange Online PowerShell](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) nach Postfachaktivitäten suchen. 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Postfachberechtigungen für Stellvertretung hinzugefügt  <br/> |AddMailboxPermissionsAddMailboxPermissions  <br/> |Ein Administrator hat einem Benutzer die Postfachberechtigung „FullAccess“ für das Postfach einer anderen Person zugewiesen (auch „Stellvertretung“ genannt). Die Berechtigung "FullAccess" erlaubt der Stellvertretung, das Postfach der anderen Person zu öffnen sowie den Inhalt des Postfachs zu lesen und zu verwalten.  <br/> |
|Benutzer mit Stellvertretungszugriff auf den Kalenderordner hinzugefügt oder entfernt<br/> |UpdateCalendarDelegation<br/> |Ein Benutzer wurde als Stellvertretung für den Kalender eines anderen Benutzers hinzugefügt oder entfernt. Der Stellvertretungszugriff gibt anderen Personen in der gleichen Organisation die Berechtigung zum Verwalten des Kalenders des Postfachbesitzers. <br/> |
|Berechtigungen für Ordner hinzugefügt<br/> |AddFolderPermissions<br/> |Eine Ordnerberechtigung wurde hinzugefügt. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach zugreifen können und welche Nachrichten sich in diesen Ordnern befinden.<br/> |
|Nachrichten in anderen Ordner kopiert  <br/> |Copy  <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |
|Erstelltes Postfachelement  <br/> |Erstellen  <br/> |Ein Element wird im „Kalender“, in den „Kontakten“, den „Notizen“ oder im „Aufgabenordner“ des Postfachs erstellt. Ein Beispiel: Es wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, Senden oder Empfangen einer Nachricht nicht überwacht wird. Auch das Erstellen eines Postfachordners wird nicht überwacht.  <br/> |
|Neue Posteingangsregel in der Outlook Web App erstellt  <br/> |NewInboxRule<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat in der Outlook Web App eine Posteingangsregel erstellt.<br/> |
|Nachrichten aus Ordner „Gelöschte Elemente“ gelöscht  <br/> |SoftDelete  <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Diese Elemente werden in den Ordner "Wiederherstellbare Elemente" verschoben. Nachrichten werden auch in den Ordner „Wiederherstellbare Elemente“ verschoben, wenn ein Benutzer diese auswählt und**UMSCHALT+ENTF** drückt.  <br/> |
|Nachricht als Datensatz klassifiziert  <br/> |ApplyRecordLabel<br/> |Eine Nachricht wurde als Datensatz klassifiziert. Dies geschieht, wenn eine Aufbewahrungsbezeichnung, die Inhalte als Datensatz klassifiziert, manuell oder automatisch auf eine Nachricht angewendet wird.<br/> |
|Nachrichten in anderen Ordner verschoben  <br/> |Move  <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |
|Nachrichten in Ordner "Gelöschte Elemente" verschoben  <br/> |MoveToDeletedItems  <br/> |Eine Nachricht wurde gelöscht und in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
|Ordnerberechtigung geändert  <br/> |UpdateFolderPermissions  <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Postfachordner und die Nachrichten in diesen Ordnern zugreifen können.  <br/> |
|Posteingangsregel in Outlook Web App geändert<br/> |SetInboxRule<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat in der Outlook Web App eine Posteingangsregel geändert.<br/> |
|Nachrichten aus Postfach gelöscht  <br/> |HardDelete  <br/> |Eine Nachricht wurde aus dem Ordner "Wiederherstellbare Elemente" gelöscht (dauerhaft aus dem Postfach entfernt).  <br/> |
|Postfachberechtigungen für Stellvertretung entfernt  <br/> |Remove-MailboxPermission  <br/> |Ein Administrator hat die Berechtigung „FullAccess“ (die einer Stellvertretung zugewiesen wurde) aus dem Postfach einer Person entfernt. Nachdem die Berechtigung „FullAccess“ entfernt wurde, kann die Stellvertretung das Postfach der anderen Person nicht mehr öffnen und nicht mehr auf Inhalte in dem Postfach zugreifen.  <br/> |
|Ordnerberechtigung entfernt<br/> |RemoveFolderPermissions<br/> |Eine Ordnerberechtigung wurde entfernt. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach zugreifen können und welche Nachrichten sich in diesen Ordnern befinden.<br/> |
|Nachricht mit Berechtigungen vom Typ "Senden als" gesendet  <br/> |SendAs  <br/> |Eine Nachricht wurde unter Verwendung der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |
|Nachricht mit Berechtigungen vom Typ "Senden im Auftrag von" gesendet  <br/> |SendOnBehalf  <br/> |Eine Nachricht wurde unter Verwendung der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Bei der Nachricht ist für den Empfänger angegeben, in wessen Auftrag die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |
|Posteingangsregeln des Outlook-Clients aktualisiert<br/> |UpdateInboxRules<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat im Outlook-Client eine Posteingangsregel geändert.<br/> |
|Nachricht aktualisiert  <br/> |Update  <br/> |Eine Nachricht oder ihre Eigenschaften wurden geändert.  <br/> |
|Benutzer am Postfach angemeldet  <br/> |MailboxLogin  <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |
||||

### <a name="sway-activities"></a>Sway-Aktivitäten
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in Sway aufgelistet. Sway ist eine Office 365-App, die Benutzer beim Sammeln, Formatieren und Teilen von Ideen, Geschichten und Präsentationen in einem interaktiven, webbasierten Zeichenbereich unterstützt. Weitere Informationen finden Sie unter [Häufig gestellte Fragen zu Sway – Hilfe für Administratoren](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Sway-Freigabestufe geändert  <br/> |SwayChangeShareLevel  <br/> |Ein Benutzer ändert die Freigabestufe eines Sways. Mit diesem Ereignis wird ein Benutzer erfasst, der den Umfang einer mit einem Sway verknüpften Freigabe geändert hat, beispielsweise von „Öffentlich“ zu „Innerhalb der Organisation“.  <br/> |
|Sway erstellt  <br/> |SwayCreate  <br/> |Der Benutzer erstellt ein Sway.  <br/> |
|Sway gelöscht  <br/> |SwayDelete  <br/> |Der Benutzer löscht ein Sway.  <br/> |
|Sway-Duplizierung deaktiviert  <br/> |SwayDisableDuplication  <br/> |Ein Benutzer hat die Duplizierung eines Sways deaktiviert.  <br/> |
|Sway dupliziert  <br/> |SwayDuplicate  <br/> |Der Benutzer dupliziert ein Sway.  <br/> |
|Sway bearbeitet   <br/> |SwayEdit  <br/> |Der Benutzer bearbeitet ein Sway.  <br/> |
|Sway-Duplizierung aktiviert  <br/> |EnableDuplication  <br/> |Ein Benutzer hat die Duplizierung eines Sways aktiviert. Die Fähigkeit eines Benutzers zum Aktivieren der Duplizierung eines Sways ist standardmäßig aktiviert.  <br/> |
|Sway-Freigabe widerrufen  <br/> |SwayRevokeShare  <br/> |Der Benutzer stoppt die Freigabe eines Sways, indem er den Zugriff widerruft. Wenn der Zugriff widerrufen wird, ändern sich die dem Sway zugeordneten Verknüpfungen.  <br/> |
|Sway freigegeben  <br/> |SwayShare  <br/> |Ein Benutzer plant, ein Sway freizugeben. Mit diesem Ereignis wird die Benutzeraktion des Klickens auf ein bestimmtes Freigabeziel im Freigabemenü des Sways erfasst. Das Ereignis gibt nicht an, ob der Benutzer die Freigabeaktion abgeschlossen hat.  <br/> |
|Externen Freigabe von Sway deaktiviert  <br/> |SwayExternalSharingOff  <br/> |Ein Administrator deaktiviert die externe Sway-Freigabe für die gesamte Organisation im Microsoft 365 Admin Center.  <br/> |
|Externe Freigabe von Sway aktiviert  <br/> |SwayExternalSharingOn  <br/> |Ein Administrator aktiviert die externe Sway-Freigabe für die gesamte Organisation im Microsoft 365 Admin Center.  <br/> |
|Sway-Dienst deaktiviert  <br/> |SwayServiceOff  <br/> |Ein Administrator deaktiviert Sway für die gesamte Organisation im Microsoft 365 Admin Center.  <br/> |
|Sway-Dienst aktiviert  <br/> |SwayServiceOn  <br/> |Ein Administrator aktiviert Sway für die gesamte Organisation im Microsoft 365 Admin Center (der Sway-Dienst ist standardmäßig aktiviert).  <br/> |
|Angezeigtes Sway  <br/> |SwayView  <br/> |Der Benutzer zeigt ein Sway an.  <br/> |
||||

  
### <a name="user-administration-activities"></a>Benutzerverwaltungsaktivitäten
  
In der folgenden Tabelle sind Benutzerverwaltungsaktivitäten aufgelistet, die protokolliert werden, wenn ein Administrator ein Benutzerkonto über das Microsoft 365 Admin Center oder das Azure-Verwaltungsportal hinzufügt oder ändert.
  
|**Aktivität**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Benutzer hinzugefügt  <br/> |Benutzer hinzufügen  <br/> |Ein Office 365-Benutzerkonto wurde erstellt.  <br/> |
|Benutzerlizenz geändert  <br/> |Benutzerlizenz ändern  <br/> |Die einem Benutzer zugewiesene Lizenz wurde geändert. Wenn Sie feststellen möchten, welche Lizenzen geändert wurden, sehen Sie sich die entsprechende Aktivität **Benutzer aktualisiert** an.  <br/> |
|Benutzerkennwort geändert  <br/> |Benutzerkennwort ändern  <br/> |Der Administrator hat das Kennwort für einen Benutzer geändert.  <br/> |
|Benutzer gelöscht  <br/> |Benutzer löschen  <br/> |Ein Office 365-Benutzerkonto wurde gelöscht.  <br/> |
|Benutzerkennwort zurücksetzen  <br/> |Benutzerkennwort zurücksetzen  <br/> |Der Administrator hat das Kennwort eines Benutzers zurückgesetzt.  <br/> |
|Eigenschaft festgelegt, die einen Benutzer zur Kennwortänderung zwingt  <br/> |Erzwungene Änderung des Benutzerkennworts festgelegt  <br/> |Der Administrator hat die Eigenschaft festgelegt, die einen Benutzer dazu zwingt, sein Kennwort bei der nächsten Anmeldung bei Office 365 zu ändern.  <br/> |
|Lizenzeigenschaften festgelegt  <br/> |Lizenzeigenschaften festgelegt  <br/> |Der Administrator ändert die Eigenschaften einer Lizenz, die einem Benutzer zugewiesen ist.  <br/> |
|Benutzer aktualisiert  <br/> |Benutzer aktualisieren  <br/> |Ein Administrator ändert eine oder mehrere Eigenschaften eines Benutzerkontos. Eine Liste der Benutzereigenschaften, die aktualisiert werden können, finden Sie im Abschnitt "Aktualisieren von Benutzerattributen" unter [Azure Active Directory-Überwachungsberichtsereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Azure Active Directory-Gruppenverwaltungsaktivitäten
  
In der nachstehenden Tabelle werden die Gruppenverwaltungsaktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator oder ein Benutzer eine Office 365-Gruppe erstellt oder ändert, oder aber wenn ein Administrator eine Sicherheitsgruppe über das Microsoft 365 Admin Center oder das Azure-Verwaltungsportal erstellt.  Weitere Informationen zu Gruppen in Office 365 finden Sie unter [Anzeigen, Erstellen und Löschen von Gruppen im Office 365 Admin Center](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Gruppe hinzugefügt  <br/> |Gruppe hinzufügen  <br/> |Eine Gruppe wurde erstellt.  <br/> |
|Mitglied zur Gruppe hinzugefügt  <br/> |Mitglied zu Gruppe hinzufügen  <br/> |Ein Mitglied wurde zu einer Gruppe hinzugefügt.  <br/> |
|Gruppe gelöscht  <br/> |Gruppe löschen  <br/> |Eine Gruppe wurde gelöscht.  <br/> |
|Mitglied aus Gruppe entfernt  <br/> |Mitglied aus Gruppe entfernen  <br/> |Ein Mitglied wurde aus einer Gruppe entfernt.  <br/> |
|Gruppe aktualisiert  <br/> |Gruppe aktualisieren  <br/> |Eine Eigenschaft einer Gruppe wurde geändert.  <br/> |
||||
   
### <a name="application-administration-activities"></a>Anwendungsverwaltungsaktivitäten
  
In der folgenden Tabelle sind Anwendungsverwaltungsaktivitäten aufgelistet, die protokolliert werden, wenn ein Administrator eine in Azure AD registrierte Anwendung hinzufügt oder ändert. Jede Anwendung, die Azure AD zur Authentifizierung verwendet, muss im Verzeichnis registriert sein.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Delegierungseintrag hinzugefügt  <br/> |Delegierungseintrag hinzufügen  <br/> |Eine Authentifizierungsberechtigung für eine Anwendung in Azure AD wurde erstellt/gewährt.  <br/> |
|Dienstprinzipal hinzugefügt  <br/> |Dienstprinzipal hinzufügen  <br/> |Eine Anwendung wurde in Azure AD registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Anmeldeinformationen für einen Dienstprinzipal hinzugefügt   <br/> |Dienstprinzipal-Anmeldeinformationen hinzufügen  <br/> |Anmeldeinformationen für einen Dienstprinzipal in Azure AD wurden hinzugefügt. Ein Dienstprinzipal stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Delegierungseintrag entfernt  <br/> |Delegierungseintrag entfernen  <br/> |Eine Authentifizierungsberechtigung für eine Anwendung in Azure AD wurde entfernt.  <br/> |
|Dienstprinzipal aus dem Verzeichnis entfernt  <br/> |Dienstprinzipal entfernen  <br/> |Eine Anwendung wurde aus Azure AD gelöscht oder ihre Registrierung aufgehoben. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Anmeldeinformationen aus einem Dienstprinzipal entfernt   <br/> |Dienstprinzipal-Anmeldeinformationen entfernen  <br/> |Anmeldeinformationen für einen Dienstprinzipal in Azure AD wurden entfernt. Ein Dienstprinzipal stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Delegierungseintrag festgelegt  <br/> |Delegierungseintrag festgelegt  <br/> |Eine Authentifizierungsberechtigung für eine Anwendung in Azure AD wurde aktualisiert.  <br/> |
||||

### <a name="role-administration-activities"></a>Rollenverwaltungsaktivitäten
  
In der folgenden Tabelle sind Azure AD-Rollenverwaltungsaktivitäten aufgelistet, die protokolliert werden, wenn ein Administrator Administratorrollen im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Mitglied zu Rolle hinzugefügt  <br/> |Rollenmitglied zu Rolle hinzufügen  <br/> |Ein Benutzer wurde einer Administratorrolle in Office 365 hinzugefügt.  <br/> |
|Benutzer aus einer Directory-Rolle entfernt  <br/> |Rollenmitglied aus Rolle entfernen  <br/> |Ein Benutzer wurde aus einer Administratorrolle in Office 365 entfernt.  <br/> |
|Kontaktinformationen für Unternehmen festgelegt  <br/> |Kontaktinformationen für Unternehmen festgelegt  <br/> |Die Kontakteinstellungen auf Unternehmensebene für Ihre Office 365-Organisation wurden aktualisiert. Dies umfasst E-Mail-Adressen für Nachrichten in Bezug auf Abonnements, die von Office 365 gesendet werden, sowie technische Benachrichtigungen zu Office 365-Diensten.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>Verzeichnisverwaltungsaktivitäten
  
In der folgenden Tabelle sind Aktivitäten in Bezug auf Verzeichnisse und Domänen in Azure AD aufgelistet, die protokolliert werden, wenn ein Administrator seine Office 365-Organisation im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Domäne zu Unternehmen hinzugefügt  <br/> |Domäne zu Unternehmen hinzufügen  <br/> |Eine Domäne wurde Ihrer Office 365-Organisation hinzugefügt.  <br/> |
|Partner zum Verzeichnis hinzugefügt  <br/> |Partner zu Unternehmen hinzufügen  <br/> |Es wurde ein Partner (delegierter Administrator) zu Ihrer Office 365-Organisation hinzugefügt.  <br/> |
|Domäne aus Unternehmen entfernt  <br/> |Domäne aus Unternehmen entfernen  <br/> |Es wurde eine Domäne aus Ihrer Office 365-Organisation entfernt.  <br/> |
|Partner aus dem Verzeichnis entfernt  <br/> |Partner aus Unternehmen entfernen  <br/> |Es wurde ein Partner (delegierter Administrator) aus Ihrer Office 365-Organisation entfernt.  <br/> |
|Unternehmensinformationen festgelegt  <br/> |Unternehmensinformationen festgelegen  <br/> |Die Unternehmensinformationen für Ihre Office 365-Organisation wurden aktualisiert. Dies umfasst E-Mail-Adressen für Nachrichten in Bezug auf Abonnements, die von Office 365 gesendet werden, sowie technische Benachrichtigungen zu Office 365-Diensten.  <br/> |
|Domänenauthentifizierung festgelegt  <br/> |Domänenauthentifizierung festgelegen  <br/> |Die Einstellungen der Domänenauthentifizierung für Ihre Office 365-Organisation wurde geändert.  <br/> |
|Verbundeinstellungen für eine Domäne aktualisiert  <br/> |Verbundeinstellungen für Domäne festlegen  <br/> |Die Verbundeinstellungen (externe Freigabe) für Ihre Office 365-Organisation wurden geändert.  <br/> |
|Kennwortrichtlinie festgelegt  <br/> |Kennwortrichtlinie festlegen  <br/> |Die Längen- und Zeicheneinschränkungen für Benutzerkennwörter in Ihrer Office 365-Organisation wurden geändert.  <br/> |
|Azure AD-Synchronisierung aktiviert  <br/> |DirSyncEnabled-Flag für Unternehmen festlegen  <br/> |Die Eigenschaft, die ein Verzeichnis für die Azure AD-Synchronisierungsdienste aktiviert, wurde festgelegt.  <br/> |
|Domäne aktualisiert  <br/> |Domäne aktualisieren  <br/> |Die Einstellungen einer Domäne in Ihrer Office 365-Organisation wurden aktualisiert.  <br/> |
|Domäne überprüft  <br/> |Domäne überprüfen  <br/> |Es wurde überprüft, ob Ihre Organisation der Besitzer der Domäne ist.  <br/> |
|Domäne mit E-Mail-Prüfung überprüft  <br/> |Domäne mit E-Mail-Prüfung überprüfen  <br/> |Es wurde eine E-Mail-Prüfung verwendet, um zu überprüfen, ob Ihre Organisation der Besitzer der Domäne ist.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten
  
Inhaltssuche und mit eDiscovery zusammenhängende Aktivitäten, die im Security and Compliance Center oder durch Ausführen der entsprechenden PowerShell-Cmdlets durchgeführt werden, werden im Überwachungsprotokoll protokolliert. Hierzu gehören unter anderem folgende Aktivitäten:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, Starten und Bearbeiten von Inhaltssuchen
    
- Durchführen von Aktionen bei der Inhaltssuche, wie Vorschau, Exportieren und Löschen von Suchergebnissen
    
- Konfigurieren von Berechtigungsfiltern für die Inhaltssuche
    
- Verwalten der eDiscovery-Administratorrolle
    
Eine Liste und eine detaillierte Beschreibung der eDiscovery-Aktivitäten, die protokolliert werden, finden Sie unter [Suchen nach eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Es dauert bis zu 30 Minuten, bis die Ereignisse, die aus den unter **eDiscovery-Aktivitäten** in der Dropdownliste **Aktivitäten** aufgeführten Aktivitäten resultieren, in den Suchergebnissen angezeigt werden. Im Gegensatz dazu dauert es bis zu 24 Stunden, bis die entsprechenden Ereignisse aus eDiscovery-Cmdlet-Aktivitäten in der Liste der Suchergebnisse angezeigt werden. 
  
### <a name="advanced-ediscovery-activities"></a>Advanced eDiscovery-Aktivitäten

In der folgenden Tabelle sind Aktivitäten aufgeführt, die sich ergeben, wenn IT-Spezialisten und Juristen Aufgaben in Advanced eDiscovery in Microsoft 365 ausführen. Weitere Informationen finden Sie unter [Übersicht über die Advanced eDiscovery-Lösung in Microsoft 365](compliance20/overview-ediscovery-20.md).

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
| Daten zu einem anderen Prüfdateisatz hinzugefügt<br/>         | AddWorkingSetQueryToWorkingSet<br/>  |  Der Benutzer hat Dokumente eines Prüfdateisatzes einem anderen hinzugefügt.<br/>|
| Daten zu einem Prüfdateisatz hinzugefügt <br/>                | AddQueryToWorkingSet<br/>            |  Der Benutzer hat die Suchergebnisse einer Inhaltssuche, die einem Advanced eDiscovery-Fall zugeordnet sind, einem Prüfdateisatz zugeordnet.<br/>|
| Nicht-Office 365-Daten einem Prüfdateisatz hinzugefügt<br/>  | AddNonOffice365DataToWorkingSet<br/> |  Der Benutzer hat Nicht-Office 365-Daten einem Prüfdateisatz hinzugefügt.<br/>|
| Wiederhergestellte Dokumente zu Prüfdateisatz hinzugefügt<br/> | AddRemediatedData<br/>               |  Der Benutzer lädt Dokumente hoch, bei denen Indizierungsfehler aufgetreten sind, die in einem Prüfdateisatz festgehalten worden sind.<br/>|
| Daten im Prüfdateisatz analysiert <br/>             | RunAlgo<br/>                         |  Der Benutzer hat eine Analyse der Dokumente in einem Prüfdateisatz durchgeführt. <br/>|
| Dokument im Prüfdateisatz kommentiert <br/>        | AnnotateDocument<br/>                |  Ein Benutzer hat ein Dokument in einem Prüfdateisatz kommentiert. „Kommentieren“ umfasst auch das Bearbeiten/Redigieren des Dokuments. <br/>|
| Ladesätze verglichen <br/>                      | LoadComparisonJob<br/>               |Der Benutzer hat zwei verschiedene Ladesätze in einem Prüfdateisatz verglichen. Unter Ladesatz versteht man, dass Daten aus einer Inhaltssuche, die einem Fall zugeordnet sind, einem Prüfdateisatz hinzugefügt werden.  <br/>|
| Dokumente in PDF-Dateien konvertiert<br/>      | BurnJob<br/>                         |Der Benutzer hat alle redigierten Dokumente in einem Prüfdateisatz in PDF-Dateien konvertiert.<br/>|
| Prüfdateisatz erstellt<br/>                       | CreateWorkingSet<br/>                |Der Benutzer hat einen Prüfdateisatz erstellt.<br/>|
| Prüfdateisatzsuche erstellt<br/>                | CreateWorkingSetSearch<br/>          |Der Benutzer hat eine Suchabfrage erstellt, die die Dokumente in einem Prüfdateisatz durchsuchen. <br/>|
| Tag erstellt<br/>                              | CreateTag<br/>                       |Ein Benutzer hat eine Tag-Gruppe in einem Prüfdateisatz erstellt. Eine Tag-Gruppe kann ein oder mehrere untergeordnete Tags enthalten. Diese Tags werden dann zum Taggen von Dokumenten im Prüfdateisatz verwendet.<br/>|
| Prüfdateisatzsuche gelöscht <br/>               | DeleteWorkingSetSearch<br/>          |Ein Benutzer hat eine Suchabfrage in einem Prüfdateisatz gelöscht.<br/>|
| Tag gelöscht<br/>                              | DeleteTag<br/>                       |Ein Benutzer hat ein Tag oder eine Tag-Gruppe in einem Prüfdateisatz gelöscht.<br/>|
| Heruntergeladenes Dokument<br/>                      | DownloadDocument<br/>                |Ein Benutzer hat ein Dokument aus einem Prüfdateisatz heruntergeladen.<br/>|
| Tag bearbeitet <br/>                              | DownloadDocument<br/>                |Ein Benutzer hat ein Tag in einem Prüfdateisatz geändert.<br/>|
| Dokumente aus einem Prüfdateisatz exportiert <br/>      | ExportJob<br/>                       |Der Benutzer hat Dokumente aus einem Prüfdateisatz exportiert.<br/>|
| Falleinstellungen geändert <br/>                   | UpdateCaseSettings<br/>              | Der Benutzer hat die Einstellungen für einen Fall geändert. Die Falleinstellungen umfassen Fallinformationen, Zugriffsberechtigungen und Einstellungen, mit denen das Such- und Analyseverhalten gesteuert werden.<br/>|
| Prüfdateisatzsuche geändert<br/>               | UpdateWorkingSetSearch<br/>          |  Ein Benutzer hat eine Suchabfrage in einem Prüfdateisatz geändert.<br/>|
| Vorschau einer Prüfdateisatzsuche angezeigt <br/>             | PreviewWorkingSetSearch<br/>         |  Der Benutzer hat die Ergebnisse einer Suchabfrage in einem Prüfdateisatz in einer Vorschau angezeigt.<br/>|
| Fehler in Dokumenten behoben <br/>              | ErrorRemediationJob<br/>             |  Der Benutzer behebt Dateien mit Indizierungsfehlern. <br/>|
| Dokument getaggt<br/>                          | TagFiles<br/>                        |  Ein Benutzer hat ein Dokument in einem Prüfdateisatz mit Tags versehen.<br/>|
| Ergebnisse einer Abfrage getaggt<br/>                | TagJob<br/>                          |  Ein Benutzer hat alle Dokumente getaggt, die den Kriterien einer Suchabfrage in einem Prüfdateisatz entsprechen.<br/>|
| Dokument im Prüfdateisatz angezeigt<br/>            | ViewDocument<br/>                    |  Ein Benutzer hat ein Dokument in einem Prüfdateisatz angezeigt.<br/>|
|||

### <a name="power-bi-activities"></a>Power BI-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Power BI durchsuchen. Informationen zu Power BI-Aktivitäten finden Sie im Abschnitt „durch Power BI-Aktivitäten überwachte Aktivitäten“ unter [Verwenden der Überwachung innerhalb Ihrer Organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
Die Überwachungsprotokollierung für Power BI ist standardmäßig nicht aktiviert. Wenn Sie im Office 365-Überwachungsprotokoll nach Power BI-Aktivitäten suchen möchten, müssen Sie die Überwachung für das Power BI-Verwaltungsportal aktivieren. Anweisungen hierzu finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI-Verwaltungsportal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
  
### <a name="microsoft-workplace-analytics-activities"></a>Microsoft Workplace Analytics-Aktivitäten

Workplace Analytics bietet einen Einblick in die Zusammenarbeit von Gruppen innerhalb Office 365-Organisation. In der folgenden Tabelle sind die Aktivitäten aufgeführt, die von Benutzern ausgeführt wurden, denen die Administrator- oder Analystenrolle in Workplace Analytics zugeordnet ist. Benutzern, denen die Rolle des Analysten zugewiesen ist, haben Vollzugriff auf alle Dienstfunktionen und können das Produkt für Analysen verwenden. Benutzer, denen die Administratorrolle zugewiesen wurde, können Datenschutzeinstellungen und Systemstandardwerte konfigurieren sowie Organisationsdaten in Workplace Analytics vorbereiten, hochladen und überprüfen. Weitere Informationen finden Sie unter [Workplace Analytics](https://docs.microsoft.com/de-DE/workplace-analytics/index-orig).

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Auf OData-Link zugegriffen <br/> |AccessedOdataLink <br/> |Analyst hat auf für eine Abfrage auf den OData-Link zugegriffen.|
|Abfrage abgebrochen <br/> |CanceledQuery <br/> |Ein Analyst hat eine laufende Abfrage abgebrochen.|
|Besprechungsausschluss erstellt <br/> |MeetingExclusionCreated <br/> |Ein Analytiker hat eine Ausschlussregel Besprechungen erstellt.|
|Ergebnis gelöscht <br/> |DeletedResult <br/> |Ein Analyst hat ein Abfrageergebnis gelöscht.|
|Bericht heruntergeladen <br/> |DownloadedReport <br/> |Ein Analyst hat eine Abfrageergebnisdatei heruntergeladen.|
|Abfrage ausgeführt <br/> |ExecutedQuery <br/> |Ein Analyst hat eine Abfrage ausgeführt.|
|Datenzugriffseinstellungen aktualisiert <br/> |UpdatedDataAccessSetting <br/> |Ein Administrator hat die Datenzugriffseinstellungen aktualisiert.|
|Datenschutzeinstellung aktualisiert <br/> |UpdatedPrivacySetting <br/> |Ein Administrator hat die Datenschutzeinstellungen aktualisiert, z. B. die minimale Gruppengröße.|
|Organisationsdaten hochgeladen <br/> |UploadedOrgData <br/> |Ein Administrator hat eine Organisationsdatendatei hochgeladen.|
|Explore angezeigt <br/> |ViewedExplore <br/> |Ein Analyst hat Visualisierungen in einer oder mehreren Explore-Registerkarten angezeigt.|
||||

### <a name="microsoft-teams-activities"></a>Microsoft Teams-Aktivitäten
  
In der folgenden Tabelle sind die in Microsoft Teams von Benutzern und Administratoren ausgeführten Aktivitäten aufgelistet, die im Office 365-Überwachungsprotokoll protokolliert werden. Microsoft Teams ist ein Arbeitsbereich in Office 365, der das Chatten ermöglicht. Hier werden die Unterhaltungen, Besprechungen, Dateien und Notizen eines Teams an einem Ort zusammengeführt. Weitere Informationen und Links zu Hilfethemen finden Sie unter:
  
- [Häufig gestellte Fragen zu Microsoft Teams – Administratorhilfe](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Hilfe zu Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Bot zum Team hinzugefügt  <br/> |BotAddedToTeam  <br/> |Ein Benutzer fügt einem Team einen Bot hinzu.  <br/> |
|Kanal hinzugefügt  <br/> |ChannelAdded  <br/> |Ein Benutzer fügt einem Team einen Kanal hinzu.  <br/> |
|Connector hinzugefügt  <br/> |ConnectorAdded  <br/> |Ein Benutzer fügt einen Connector zu einem Kanal hinzu.  <br/> |
|Mitglieder zum Team hinzugefügt  <br/> |MemberAdded  <br/> |Ein Teambesitzer fügt Mitglieder zu einem Team hinzu.  <br/> |
|Registerkarte hinzugefügt  <br/> |TabAdded  <br/> |Ein Benutzer fügt einem Kanal eine Registerkarte hinzu.  <br/> |
|Kanaleinstellung geändert  <br/> |ChannelSettingChanged  <br/> | Der Vorgang "ChannelSettingChanged" wird protokolliert, wenn die folgenden Aktivitäten von einem Teammitglied ausgeführt werden. Für jede dieser Aktivitäten wird in den Suchergebnissen für das Überwachungsprotokoll in der Spalte **Element** eine Beschreibung der geänderten Einstellung (nachstehend in Klammern gesetzt) angezeigt.  <br/> <br/>- Ändert den Namen eines Teamkanals (**Kanalname**).  <br/>  <br/>- Ändert die Beschreibung eines Teamkanals (**Kanalbeschreibung**).  <br/> |
|Organisationseinstellung geändert  <br/> |TeamsTenantSettingChanged  <br/> | Der Vorgang "TeamsTenantSettingChanged" wird protokolliert, wenn die folgenden Aktivitäten von einem globalen Administrator (über das Microsoft 365 Admin Center) ausgeführt werden. Beachten Sie, dass sich diese Aktivitäten auf die organisationsweiten Microsoft Teams-Einstellungen auswirken. Weitere Informationen finden Sie unter [Administratoreinstellungen für Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).  <br/>  Für jede dieser Aktivitäten wird in den Suchergebnissen für das Überwachungsprotokoll in der Spalte **Element** eine Beschreibung der geänderten Einstellung (nachstehend in Klammern gesetzt) angezeigt.  <br/><br/>- Aktiviert bzw. deaktiviert Microsoft Teams für die Organisation (**Microsoft Teams**).  <br/><br/>- Aktiviert bzw. deaktiviert die Interoperabilität zwischen Microsoft Teams und Skype for Business für die Organisation (**Skype for Business Interoperability**).<br/><br/>- Aktiviert oder deaktiviert die Organigrammansicht in Microsoft Teams-Clients (Organigrammansicht **). <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, private Besprechungen zu planen (** private Besprechung planen **). <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Kanalbesprechungen zu planen (Kanalbesprechungsplanung**).   <br/><br/>- Aktiviert oder deaktiviert Videoanrufe in Teambesprechungen (Video für Skype-Besprechungen **).  <br/><br/>- Aktiviert oder deaktiviert die Bildschirmfreigabe in Microsoft Teams-Meetups für die Organisation (** Bildschirmfreigabe für Skype-Besprechungen **). <br/><br/> - Aktiviert oder deaktiviert die Möglichkeit, animierte Bilder (so genannte Giphys) zu Teamunterhaltungen hinzuzufügen (animierte Bilder**).    <br/><br/>- Ändert die Inhaltsbewertungseinstellung für die Organisation (**Inhaltsbewertung**). Die Inhaltsbewertung beschränkt, welche Arten animierter Bilder in Unterhaltungen angezeigt werden können.  <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, anpassbare Bilder (so genannte benutzerdefinierte Memes) aus dem Internet zu Teamunterhaltungen hinzuzufügen (anpassbare Bilder aus dem Internet **). <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, bearbeitbare Bilder (so genannte Aufkleber) zu Teamunterhaltungen hinzuzufügen (** bearbeitbare Bilder **). <br/><br/> -Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Bots in den Chats und Kanälen von Microsoft Teams zu verwenden (organisationsweite Bots**). <br/><br/>- Aktiviert bestimmte Bots für Microsoft Teams. Davon ausgenommen ist der Teams-Hilfebot „T-Bot“, der verfügbar ist, wenn Bots für die Organisation aktiviert sind (**Einzelne Bots**).  <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Erweiterungen oder Registerkarten hinzuzufügen (**Erweiterungen oder Registerkarten**).  <br/><br/>- Aktiviert oder deaktiviert das Sideloading proprietärer Bots für Microsoft Teams (**Sideloading von Bots**).  <br/><br/>- Aktiviert oder deaktiviert die Möglichkeit für Benutzer, E-Mail-Nachrichten an einen Microsoft Teams-Kanal zu senden (**Kanal-E-Mail**).  <br/> |
|Rolle von Mitgliedern im Team geändert  <br/> |MemberRoleChanged  <br/> |Ein Teambesitzer ändert die Rolle der Mitglieder in einem Team. Die folgenden Werte geben den Rollentyp an, der dem Benutzer zugewiesen wurde.  <br/><br/><br/> **1** - Zeigt die Rolle des Besitzers an.<br/>**2** - Zeigt die Rolle des Mitglieds an. <br/>**3** - Zeigt die Rolle des Gastes an. <br/>Die Eigenschaft „Mitglieder“ enthält auch den Namen Ihrer Organisation und die E-Mail-Adresse des Mitglieds.  <br/> |
|Teameinstellung geändert  <br/> |TeamSettingChanged  <br/> | Der Vorgang "TeamSettingChanged" wird protokolliert, wenn die folgenden Aktivitäten von einem Teambesitzer ausgeführt werden. Für jede dieser Aktivitäten wird in den Suchergebnissen für das Überwachungsprotokoll in der Spalte **Element** eine Beschreibung der geänderten Einstellung (nachstehend in Klammern gesetzt) angezeigt.  <br/><br/>- Ändert die Art des Zugriffs für ein Team. Teams können als „Privat“ oder „Öffentlich" festgelegt werden (**Art des Teamzugriffs**). Wenn ein Team privat ist (Standardeinstellung), haben Benutzer nur nach Einladung Zugriff auf das Team. Wenn ein Team öffentlich ist, kann es von allen Benutzern gefunden werden.  <br/><br/>- Ändert die Informationsklassifizierung eines Teams (**Teamklassifizierung**).  <br/>  Teamdaten können beispielsweise als mit hohen, mittleren oder niedrigen geschäftlichen Auswirkungen klassifiziert werden.<br/><br/>- Ändert den Namen eines Teams (**Teamname**).  <br/><br/>- Ändert die Beschreibung eines Teams (Teambeschreibung). <br/><br/>- Änderungen von Einstellungen für das Team. Ein Teambesitzer kann in einem Teams-Client auf diese Einstellungen zugreifen, indem er mit der rechten Maustaste auf ein Team klickt, anschließend auf **Team verwalten** klickt und dann die Registerkarte **Einstellungen** auswählt. Für diese Aktivitäten wird in den Suchergebnissen für das Überwachungsprotokoll in der Spalte **Element** der Name der geänderten Einstellung angezeigt.  <br/> |
|Team erstellt  <br/> |TeamCreated  <br/> |Ein Benutzer erstellt ein Team.  <br/> |
|Kanal gelöscht  <br/> |ChannelDeleted  <br/> |Ein Benutzer löscht einen Kanal aus einem Team.  <br/> |
|Team gelöscht  <br/> |TeamDeleted  <br/> |Ein Teambesitzer löscht ein Team.  <br/> |
|Bot aus Team entfernt  <br/> |BotRemovedFromTeam  <br/> |Ein Benutzer entfernt einen Bot aus einem Team.  <br/> |
|Connector entfernt  <br/> |ConnectorRemoved  <br/> |Ein Benutzer entfernt einen Connector aus einem Kanal.  <br/> |
|Mitglieder aus Team entfernt  <br/> |MemberRemoved  <br/> |Ein Teambesitzer entfernt Mitglieder aus einem Team.  <br/> |
|Registerkarte entfernt  <br/> |TabRemoved  <br/> |Ein Benutzer entfernt eine Registerkarte aus einem Kanal.  <br/> |
|Connector aktualisiert  <br/> |ConnectorUpdated  <br/> |Ein Benutzer hat in einem Kanal einen Connector geändert.  <br/> |
|Registerkarte aktualisiert  <br/> |TabUpdated  <br/> |Ein Benutzer hat in einem Kanal eine Registerkarte geändert.  <br/> |
|Benutzer bei Teams angemeldet  <br/> |TeamsSessionStarted  <br/> |Ein Benutzer meldet sich bei einem Microsoft Teams-Client an.  <br/> |
||||

### <a name="yammer-activities"></a>Yammer-Aktivitäten
  
In der folgenden Tabelle sind die in Yammer von Benutzern und Administratoren ausgeführten Aktivitäten aufgelistet, die im Office 365-Überwachungsprotokoll protokolliert werden. Zur Rückgabe von Yammer-Aktivitäten aus dem Office 365-Überwachungsprotokoll müssen Sie in der Liste **Aktivitäten** den Eintrag **Ergebnisse für alle Aktivitäten anzeigen** auswählen. Verwenden Sie die Datumsbereichsfelder und die Liste **Benutzer**, um die Suchergebnisse einzuschränken. 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Datenaufbewahrungsrichtlinie geändert  <br/> |SoftDeleteSettingsUpdated  <br/> |Ein bestätigter Administrator ändert die Einstellung der Aufbewahrungsrichtlinie für Netzwerkdaten in "Endgültig Löschen" oder "Vorläufig Löschen". Dieser Vorgang kann nur von bestätigten Administratoren ausgeführt werden.  <br/> |
|Netzwerkkonfiguration geändert  <br/> |NetworkConfigurationUpdated  <br/> |Ein Netzwerk- oder bestätigter Administrator ändert die Konfiguration des Yammer-Netzwerks. Dies schließt das Festlegen des Intervalls zum Exportieren von Daten und das Aktivieren von Chats ein.  <br/> |
|Netzwerkprofileinstellungen geändert  <br/> |ProcessProfileFields  <br/> |Ein Netzwerk- oder bestätigter Administrator ändert die Informationen, die für die Netzwerkbenutzer in den Mitgliedsprofilen angezeigt werden.  <br/> |
|Modus für private Inhalte geändert  <br/> |SupervisorAdminToggled  <br/> |Ein bestätigter Administrator aktiviert oder deaktiviert den *Modus "Privater Inhalt"*. In diesem Modus kann ein Administrator die Beiträge in privaten Gruppen und die zwischen einzelnen Benutzern (oder Benutzergruppen) ausgetauschten privaten Nachrichten anzeigen. Dieser Vorgang kann nur von bestätigten Administratoren ausgeführt werden.  <br/> |
|Sicherheitskonfiguration geändert  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Ein bestätigter Administrator aktualisiert die Sicherheitskonfiguration des Yammer-Netzwerks. Dies schließt das Festlegen von Kennwortablaufrichtlinien und Einschränkungen für IP-Adressen ein. Dieser Vorgang kann nur von bestätigten Administratoren ausgeführt werden.  <br/> |
|Datei erstellt  <br/> |FileCreated  <br/> |Ein Benutzer lädt eine Datei hoch.  <br/> |
|Gruppe erstellt  <br/> |GroupCreation  <br/> |Der Benutzer erstellt eine Gruppe.  <br/> |
|Gruppe gelöscht  <br/> |GroupDeletion  <br/> |Eine Gruppe wird in Yammer gelöscht.  <br/> |
|Nachricht gelöscht  <br/> |MessageDeleted  <br/> |Ein Benutzer löscht eine Nachricht.  <br/> |
|Datei heruntergeladen  <br/> |FileDownloaded  <br/> |Ein Benutzer lädt eine Datei herunter.  <br/> |
|Daten exportiert  <br/> |DataExport  <br/> |Ein bestätigter Administrator exportiert Yammer-Netzwerkdaten. Dieser Vorgang kann nur von bestätigten Administratoren ausgeführt werden.  <br/> |
|Datei freigegeben  <br/> |FileShared  <br/> |Ein Benutzer gibt eine Datei für einen anderen Benutzer frei.  <br/> |
|Netzwerkbenutzer gesperrt  <br/> |NetworkUserSuspended  <br/> |Ein Netzwerk- oder bestätigter Administrator sperrt (deaktiviert) einen Benutzer in Yammer.  <br/> |
|Benutzer gesperrt  <br/> |UserSuspension  <br/> |Ein Benutzerkonto wird gesperrt (deaktiviert).  <br/> |
|Dateibeschreibung aktualisiert  <br/> |FileUpdateDescription  <br/> |Ein Benutzer ändert die Beschreibung einer Datei.  <br/> |
|Dateiname aktualisiert  <br/> |FileUpdateName  <br/> |Ein Benutzer ändert den Namen einer Datei.  <br/> |
|Datei angezeigt  <br/> |FileVisited  <br/> |Ein Benutzer zeigt eine Datei an.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Microsoft Flow-Aktivitäten

Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Flow durchsuchen. Diese Aktivitäten umfassen das Erstellen, Bearbeiten und Löschen von Flows sowie das Ändern von Flow-Berechtigungen. Informationen zum Überwachen von Flow-Aktivitäten finden Sie im Blog [Microsoft Flow-Überwachungsereignissen jetzt im Security and Compliance Center verfügbar](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft PowerApps durchsuchen. Diese Aktivitäten umfassen das Erstellen, Starten und Veröffentlichen einer App. Das Zuweisen von Berechtigungen zu Apps wird ebenfalls überwacht. Eine Beschreibung aller PowerApps-Aktivitäten finden Sie unter [Aktivitätsprotokollierung für PowerApps](https://docs.microsoft.com/de-DE/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Microsoft Stream-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Stream durchsuchen. Diese Aktivitäten umfassen Videoaktivitäten, die von Benutzern ausgeführt werden, Gruppenkanalaktivitäten und Administratoraktivitäten, beispielsweisedas Verwalten von Benutzern und Organisationseinstellungen sowie das Exportieren von Berichten. Eine Beschreibung dieser Aktivitäten finden Sie im Abschnitt „Aktivitäten, die in Microsoft Stream protokolliert werden“ in den [Überwachungsprotokollen in Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Exchange-Administratorüberwachungsprotokoll
  
Mit der Exchange-Administratorüberwachungsprotokollierung, die in Office 365 standardmäßig aktiviert ist, wird ein Ereignis im Office 365--Überwachungsprotokoll erfasst, wenn ein Administrator (oder ein Benutzer, dem Administratorrechte zugewiesen wurden) eine Änderung in Ihrer Exchange Online-Organisation vornimmt. Änderungen, die im Exchange Admin Center oder durch Ausführen eines Cmdlets in der Exchange Online PowerShell vorgenommen werden, werden im Exchange-Administratorüberwachungsprotokoll erfasst. Cmdlets, die mit den Verben **Get-**, **Search-** oder **Test-** beginnen, werden nicht im Office 365-Überwachungsprotokoll protokolliert. Ausführlichere Informationen zur Administratorüberwachungsprotokollierung in Exchange finden Sie unter [Administratorüberwachungsprotokollierung](https://go.microsoft.com/fwlink/p/?LinkID=619225).

> [!IMPORTANT]
> Einige Exchange Online-Cmdlets, die nicht im Exchange-administratorüberwachungsprotokoll (oder im Office 365-Überwachungsprotokoll) protokolliert sind. Viele dieser Cmdlets beziehen sich auf die Verwaltung des Exchange Online-Diensts und werden vom Personal des Microsoft-Rechenzentrums oder Dienstkonten ausgeführt. Diese Cmdlets werden nicht protokolliert, weil die große Anzahl von Überwachungsereignissen zu großem „Rauschen“ führen würde. Wenn ein Exchange Online-Cmdlet vorhanden ist, das nicht überwacht wird, senden Sie uns bitte einen Vorschlag an das [Office 365 Security & Compliance User Voice-Forum](https://office365.uservoice.com/forums/289138-office-365-security-compliance), und fordern Sie an, dass es für die Überwachung aktiviert wird. Sie können auch einen Desing Change Request (DCR) an den Microsoft-Support senden.
  
Nachfolgend finden Sie einige Tipps für die Suche nach Exchange-Administratoraktivitäten beim Durchsuchen des Office 365-Überwachungsprotokolls:
  
- Zur Rückgabe von Einträgen aus dem Exchange-Administratorüberwachungsprotokoll müssen Sie **Ergebnisse für alle Aktivitäten anzeigen** in der Liste **Aktivitäten** auswählen. Verwenden Sie die Felder für Datumsbereiche und die Liste **Benutzer**, um die Suchergebnisse auf Cmdlets zu begrenzen, die von einem bestimmten Exchange-Administrator innerhalb eines bestimmten Zeitraums ausgeführt wurden. 
    
- Zum Anzeigen von Ereignissen aus dem Exchange-Administratorüberwachungsprotokoll filtern Sie die Suchergebnisse, und geben Sie einen Bindestrich (**--**) in das Filterfeld **Aktivität** ein. Dadurch werden Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Administratorereignisse angegeben sind. Anschließend können Sie die Cmdlet-Namen alphabetisch sortieren. 
    
    ![Geben Sie einen Bindestrich in das Feld "Aktivitäten" ein, um Exchange-Administratorereignisse zu filtern.](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Um Informationen darüber zu erhalten, welches Cmdlet ausgeführt wurde, welche Parameter und Parameterwerte verwendet wurden und welche Objekte betroffen waren, können Sie die Suchergebnisse exportieren, indem Sie die Option **Alle Ergebnisse herunterladen** auswählen. Weiter Informationen findn Sie unter[Exportieren, Konfigurieren und Anzeigen von Überwachungsprotokoll-Datensätzen](export-view-audit-log-records.md). 

- Sie können auch den Befehl `Search-UnifiedAuditLog -RecordType ExchangeAdmin` in der Exchange Online PowerShell verwenden, um nur Überwachungsdatensätze aus dem Exchange-Administratorüberwachungsprotokoll zurückzugeben. Nach der Ausführung eines Exchange-Cmdlet kann es bis zu 30 Minuten dauern, bis der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen zurückgegeben wird. Weitere Informationen finden Sie unter [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog). Informationen zum Exportieren der vom **Search-UnifiedAuditLog**-Cmdlet zurückgegebenen Suchergebnisse in eine CSV-Datei finden Sie im Abschnitt „Tipps zum Exportieren, konfigurieren und Anzeigen des Überwachungsprotokolls“ in [Exportieren und Anzeigen des Überwachungsprotokolls](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Sie können Ereignisse auch im Exchange Admin Center anzeigen, oder durch Ausführen von **Search-AdminAuditLog** in der Exchange Online PowerShell. Dies ist eine gute Möglichkeit, um gezielt nach Aktivitäten zu suchen, die von Exchange Online-Administratoren durchgeführt wurden. Weitere Anweisungen finden Sie in:
   
   - [Anzeigen des Administratorüberwachungsprotokolls](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx) 
   
   -  [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-adminauditlog)
   
   Bitte denken Sie daran, dass dieselben Exchange-Administratoraktivitäten sowohl im Exchange-Administratorüberwachungsprotokoll als auch im Office 365-Überwachungsprotokoll protokolliert werden.
  
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wo finde ich Informationen zu den Funktionen, die der Überwachungsdienst in Office 365 bietet?**

Weitere Informationen zu den Funktionen für Überwachung und Berichterstellung in Office 365 finden Sie unter [Überwachung und Berichterstellung in Office 365](office-365-auditing-and-reporting-overview.md). 

**Welche verschiedenen Office 365-Dienste werden zur Zeit überwacht?**

Die am häufigsten verwendeten Office 365-Dienste wie Exchange Online, SharePoint Online, OneDrive for Business, Azure Active Directory, Microsoft Teams, Dynamics 365, Advanced Threat Protection und Power BI werden überwacht. Eine Liste der Dienste mit Überwachung finden Sie [am Anfang dieses Artikels ](search-the-audit-log-in-security-and-compliance.md).

**Welche Aktivitäten werden vom Überwachungsdienst in Office 365 überwacht?**

Im Abschnitt [überwachte Aktivitäten](#audited-activities) in diesem Artikel finden Sie eine Liste inklusive Beschreibung der in Office 365 geprüften Aktivitäten.

**Wie lange dauert es, bis ein Überwachungsdatensatz nach einem Ereignis verfügbar ist?**

Die meisten Überwachungsdaten sind innerhalb von 30 Minuten verfügbar, aber es kann bis zu 24 Stunden nach einem Ereignis dauern, bis der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. Sehen Sie sich die Tabelle im Abschnitt [Bevor Sie beginnen](#before-you-begin) dieses Artikels an, in der die Zeit angezeigt wird, die für die Verfügbarkeit von Ereignissen in den verschiedenen Office 365-Diensten benötigt wird.

**Wie lange werden die Überwachungseinträge aufbewahrt?**

Wie zuvor erläutert, hängt der Aufbewahrungszeitraum für Überwachungseinträge vom Office 365-Abonnement Ihrer Organisation ab.  

- **Office 365 E3:** Überwachungsdatensätze werden 90 Tage lang aufbewahrt.

- **Office 365 E5:** Überwachungsdatensätze werden 90 Tage lang aufbewahrt. Die Möglichkeit zur Aufbewahrung von Überwachungsdatensätzen für ein Jahr kann möglicherweise für E5-Benutzer und Benutzer mit einer E3-Lizenz und einer Office 365 Advanced Compliance-Add-on-Lizenz verfügbar sein.

     > [!NOTE]
     > Wie zuvor erläutert, ist das private Vorschauprogramm für die einjährige Aufbewahrungszeit für Überwachungseinträge für E5-Organisationen (oder für Benutzer in E3-Organisationen, die über erweiterte Compliance-Add-on-Lizenzen verfügen) für Neuregistrierungen nicht mehr verfügbar. Dieser Artikel wird aktualisiert, wenn der einjährige Aufbewahrungszeitraum in der öffentlichen Vorschau verfügbar oder zur allgemeinen Verfügbarkeit freigegeben ist.

Beachten Sie auch, dass die Dauer des Aufbewahrungszeitraums für Überwachungsdatensätze auf der Lizenzierung pro Benutzer basiert. Wenn z. b. einem Benutzer in Ihrer Organisation eine Office 365 E3-oder E5-Lizenz zugewiesen worden ist, werden die Überwachungseinträge für von diesem Benutzer ausgeführte Aktivitäten 90 Tage lang aufbewahrt.

**Kann ich programmgesteuert auf die Überwachungsdaten zugreifen?**

Ja. Die Office 365-Verwaltungsaktivitäts-API dient zum programmgesteuerten Abrufen der Überwachungsprotokolle.  Informationen zum Einstieg finden Sie unter [Erste Schritte mit der Office 365-Verwaltungsaktivitäts-API](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Gibt es andere Möglichkeiten zum Abrufen von Überwachungsprotokollen außer der Verwendung des Security and Compliance Centers oder der Office 365-Verwaltungsaktivitäts-API?**

Nein. Dies sind die einzigen beiden Möglichkeiten zum Abrufen von Daten aus dem Office 365-Überwachungsdienst. 

**Muss ich die Überwachung in jedem Dienst, für den ich Überwachungsprotokolle erfassen möchte, einzeln aktivieren?**

In den meisten Office 365-Diensten ist die Überwachung standardmäßig aktiviert, nachdem Sie die Überwachung für Ihre Office 365-Organisation aktiviert haben (wie im Abschnitt [Bevor Sie beginnen](#before-you-begin) in diesem Artikel beschrieben wird).

**Unterstützt der Office 365-Überwachungsdienst die Deduplizierung von Datensätzen?**

Nein. Die Überwachungsdienst-Pipeline arbeitet nahezu in Echtzeit und kann daher keine Deduplizierung unterstützen.
 
**Wird der Datenaustausch von Office 365 über alle Regionen hinweg überwacht?**

Nein. Zurzeit stellen wir Audit-Pipelines in den Regionen NA (Nordamerika), EMEA (Europa, Naher Osten und Afrika) und APAC (Asien-Pazifik) bereit. Es kann jedoch vorkommen, dass die Daten zum Lastenausgleich und nur während Livesite-Problemen zwischen den Regionen übertragen werden. Bei solchen Aktivitäten werden die Daten bei der Übertragung verschlüsselt.   
 
**Sind die Überwachungsdaten verschlüsselt?**

Überwachungsdaten werden in Exchange-Postfächern (ruhende Daten) in derselben Region gespeichert, in der die Überwachungspipeline bereitgestellt wird. Diese Daten sind nicht verschlüsselt. Zu übertragende Daten werden jedoch immer verschlüsselt. 

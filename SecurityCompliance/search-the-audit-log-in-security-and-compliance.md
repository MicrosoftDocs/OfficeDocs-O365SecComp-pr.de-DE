---
title: 'Durchsuchen des Überwachungsprotokolls im Security #a0 Compliance Center'
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
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Verwenden Sie das Security #a0 Compliance Center, um das einheitliche Überwachungsprotokoll zu durchsuchen, um Benutzer-und Administratoraktivitäten in Ihrer Office 365 Organisation anzuzeigen. '
ms.openlocfilehash: 656bb3a82c11308e8596c0eb71972ead5dfed620
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435225"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Durchsuchen des Überwachungsprotokolls im Security #a0 Compliance Center

## <a name="introduction"></a>Einführung

Sie müssen herausfinden, ob ein Benutzer ein bestimmtes Dokument gesehen oder ein Element aus seinem Postfach gelöscht hat? Wenn dies der Fall ist, können Sie das &amp; Office 365 Security Compliance Center verwenden, um das einheitliche Überwachungsprotokoll zu durchsuchen, um Benutzer-und Administratoraktivitäten in Ihrer Office 365 Organisation anzuzeigen. Warum ein einheitliches Überwachungsprotokoll? Da Sie in Office 365 nach den folgenden Arten von Benutzer-und Administratoraktivitäten suchen können:
  
- Benutzeraktivität in SharePoint Online und OneDrive für Unternehmen
    
- Benutzeraktivität in Exchange Online (Exchange-postfachüberwachungsprotokollierung)
  
- Administrator Aktivität in SharePoint Online
    
- Administrator Aktivität in Azure Active Directory (Verzeichnisdienst für Office 365)
    
- Administrator Aktivität in Exchange Online (Exchange Admin Audit Logging)
    
- Benutzer-und Administrator Aktivität in Sway
    
- eDiscovery-Aktivitäten im Security and Compliance Center
    
- Benutzer-und Administrator Aktivität in Power BI
    
- Benutzer-und Administratoraktivitäten in Microsoft Teams

- Benutzer-und Administrator Aktivität in Dynamics 365
    
- Benutzer-und Administrator Aktivität in "jammern"
 
- Benutzer-und Administrator Aktivität in Microsoft Flow
    
- Benutzer-und Administrator Aktivität in Microsoft Stream

- Analysten-und Administratoraktivitäten in Microsoft Workplace Analytics

- Benutzer-und Administratoraktivitäten in Microsoft PowerApps
    
   
## <a name="before-you-begin"></a>Bevor Sie beginnen

Lesen Sie unbedingt die folgenden Elemente, bevor Sie mit der Suche im Office 365 Überwachungsprotokoll beginnen.
  
- Sie (oder ein anderer Administrator) müssen zuerst die Überwachungsprotokollierung aktivieren, bevor Sie mit der Suche im Office 365 Überwachungsprotokoll beginnen können. Klicken Sie zum Aktivieren auf der Seite **Überwachungsprotokoll Suche** im Security #a0 Compliance Center auf **Aufzeichnung von Benutzer-und Administratoraktivitäten starten** . (Wenn dieser Link nicht angezeigt wird, wurde die Überwachung für Ihre Organisation bereits aktiviert.) Nachdem Sie es aktiviert haben, wird eine Meldung angezeigt, die besagt, dass das Überwachungsprotokoll vorbereitet wird und dass Sie eine Suche in einigen Stunden nach Abschluss der Vorbereitung ausführen können. Sie müssen dies nur einmal tun. 
    
    > [!NOTE]
    > Wir sind gerade dabei, die Überwachung standardmäßig zu aktivieren. Bis dahin können Sie Sie wie oben beschrieben aktivieren. 
  
- Sie müssen in Exchange Online die Rolle "nur Ansichts Überwachungsprotokolle" oder "Überwachungsprotokolle" zugewiesen sein, um das Office 365 Überwachungsprotokoll durchsuchen zu können. Diese Rollen werden standardmäßig den Rollengruppen Compliance Management und Organisationsverwaltung auf der Seite **Berechtigungen** im Exchange Admin Center zugewiesen. Beachten Sie, dass globale Administratoren in Office 365 und Microsoft 365 automatisch als Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt werden. Um einem Benutzer die Möglichkeit zu geben, das Office 365 Überwachungsprotokoll mit der minimalen Berechtigungsstufe zu durchsuchen, können Sie eine benutzerdefinierte Rollengruppe in Exchange Online erstellen, die nur-Ansicht-Überwachungsprotokolle oder die Rolle "Überwachungsprotokolle" hinzufügen und dann den Benutzer als Mitglied der neuen Rollengruppe hinzufügen. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Wenn Sie einem Benutzer die Rolle "nur Ansichts Überwachungsprotokolle" oder "Überwachungsprotokolle" auf der Seite **Berechtigungen** im Security #a0 Compliance Center zuweisen, kann er das Office 365 Überwachungsprotokoll nicht durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuweisen. Dies liegt daran, dass das zugrunde liegende Cmdlet, das zum Durchsuchen des Überwachungsprotokolls verwendet wird, ein Exchange Online-Cmdlet ist. 
  
- Wenn eine überwachte Aktivität von einem Benutzer oder Administrator ausgeführt wird, wird ein Überwachungseintrag generiert und im Office 365 Überwachungsprotokoll für Ihre Organisation gespeichert. Die Zeitdauer, für die ein Überwachungsdatensatz aufbewahrt wird (und im Überwachungsprotokoll durchsuchbar), hängt von Ihrem Office 365-Abonnement und insbesondere vom Typ der Lizenz ab, die einem bestimmten Benutzer zugewiesen ist.

     - **Office 365 E3** -Überwachungseinträge werden für 90 Tage aufbewahrt. Das bedeutet, dass Sie das Überwachungsprotokoll nach Aktivitäten durchsuchen können, die in den letzten 90 Tagen ausgeführt wurden.

     - **Office 365 E5** -Überwachungseinträge werden auch für 90 Tage aufbewahrt. Das Aufbewahren von Überwachungsdatensätzen für ein Jahr ist möglicherweise für E5-Benutzer und-Benutzer mit einer E3-Lizenz und einer Add-on-Lizenz für Office 365 Advanced Compliance verfügbar.

        > [!NOTE]
        > Das private Preview-Programm für die einjährige Aufbewahrungszeit für Überwachungsdatensätze für E5-Organisationen (oder für Benutzer in E3-Organisationen mit erweiterten Compliance-Add-on-Lizenzen) ist für die neue Registrierung geschlossen. Dieser Artikel wird aktualisiert, wenn der Aufbewahrungszeitraum für ein Jahr in der öffentlichen Vorschau verfügbar oder für allgemeine Verfügbarkeit freigegeben ist.

- Wenn Sie die Überwachungsprotokoll Suche in Office 365 für Ihre Organisation deaktivieren möchten, können Sie den folgenden Befehl in der Remote-PowerShell ausführen, die mit Ihrer Exchange Online Organisation verbunden ist:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Um die Überwachungs Suche erneut zu aktivieren, können Sie den folgenden Befehl in Exchange Online PowerShell ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Weitere Informationen finden Sie unter [Deaktivieren der Überwachungsprotokoll Suche in Office 365](turn-audit-log-search-on-or-off.md).
    
- Wie bereits erwähnt, ist das zugrunde liegende Cmdlet, das zum Durchsuchen des Überwachungsprotokolls verwendet wird, ein Exchange Online-Cmdlet, das **Such UnifiedAuditLog**ist. Das bedeutet, dass Sie dieses Cmdlet verwenden können, um das Office 365 Überwachungsprotokoll zu durchsuchen, anstatt die Seite **Überwachungsprotokoll Suche** im Security #a0 Compliance Center zu verwenden. Sie müssen dieses Cmdlet in der Remote-PowerShell ausführen, die mit Ihrer Exchange Online Organisation verbunden ist. Weitere Informationen finden Sie unter [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Wenn Sie Daten programmgesteuert aus dem Office 365 Überwachungsprotokoll herunterladen möchten, sollten Sie die API für die Office 365 Verwaltungsaktivität anstelle eines PowerShell-Skripts verwenden. Die Office 365-Verwaltungs Aktivitäts-API ist ein Rest-Webdienst, mit dem Sie Betriebs-, Sicherheits-und Compliance-Überwachungslösungen für Ihre Organisation entwickeln können. Weitere Informationen finden Sie unter [API-Referenz zur Office 365-Verwaltungsaktivität](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).
    
- Es kann bis zu 30 Minuten oder bis zu 24 Stunden dauern, bis ein Ereignis eintritt, damit der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. In der folgenden Tabelle ist die für die verschiedenen Dienste in Office 365 benötigte Zeit dargestellt.
    
    |**Office 365-Dienste**|**30 Minuten**|**24 Stunden**|
    |:-----|:-----|:-----|
    |Advanced Threat Protection und Threat Intelligence  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure-Active Directory (Benutzeranmelde Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure-Active Directory (admin-Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
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
    |SharePoint Online und OneDrive for Business  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (Azure AD) ist der Verzeichnisdienst für Office 365. Das einheitliche Überwachungsprotokoll enthält Aktivitäten von Benutzern, Gruppen, Anwendungen, Domänen und Verzeichnissen, die im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal ausgeführt werden. Eine vollständige Liste der Azure AD Ereignisse finden Sie unter [Azure Active Directory Audit Report Events](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Exchange Online Überwachungsprotokolle bestehen aus zwei Arten von Ereignissen: Exchange-Administrator Ereignisse (von Administratoren ausgeführte Aktionen) und Post Fach Ereignisse (Aktionen, die von Benutzern in Postfächern ausgeführt werden). Beachten Sie, dass die postfachüberwachung nicht standardmäßig aktiviert ist. Es muss für jedes Benutzerpostfach aktiviert sein, bevor Post Fach Ereignisse im Office 365 Überwachungsprotokoll gesucht werden können. Weitere Informationen zur postfachüberwachung und den protokollierten Post Fach Überwachungsaktionen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md).
    
- Die Überwachungsprotokollierung für Power BI ist standardmäßig nicht aktiviert. Um im Office 365 Überwachungsprotokoll nach Power BI-Aktivitäten zu suchen, müssen Sie die Überwachung im Power BI-Verwaltungsportal aktivieren. Anweisungen finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI-Verwaltungsportal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
    
    
## <a name="search-the-audit-log"></a>Durchsuchen des Überwachungsprotokolls

Hier ist der Vorgang zum Durchsuchen des Überwachungsprotokolls in Office 365.
  
[Schritt 1: Ausführen einer Überwachungsprotokoll Suche](#step-1-run-an-audit-log-search)
  
[Schritt 2: Anzeigen der Suchergebnisse](#step-2-view-the-search-results)

[Schritt 3: Filtern der Suchergebnisse](#step-3-filter-the-search-results)

[Schritt 4: Exportieren der Suchergebnisse in eine Datei](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Schritt 1: Ausführen einer Überwachungsprotokoll Suche

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Verwenden Sie eine private Browsersitzung (keine reguläre Sitzung), um auf das Security #a0 Compliance Center zuzugreifen, da dadurch verhindert wird, dass die Anmeldeinformationen, mit denen Sie derzeit angemeldet sind, verwendet werden. Drücken Sie zum Öffnen einer InPrivate-Browsersitzung in Internet Explorer oder Microsoft Edge einfach STRG + UMSCHALT + P. Drücken Sie STRG + UMSCHALT + N, um eine private Browsersitzung in Google Chrome (als inkognito-Fenster bezeichnet) zu öffnen. 
  
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security #a0 Compliance Center auf **Suchen**, und klicken Sie dann auf **Überwachungsprotokoll Suche**.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
    ![Konfigurieren Sie Kriterien, und klicken Sie dann auf suchen, um den Bericht auszuführen](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Sie müssen zunächst die Überwachungsprotokollierung aktivieren, bevor Sie eine Überwachungsprotokoll Suche ausführen können. Wenn der Link **Recording User und admin Activity starten** angezeigt wird, klicken Sie darauf, um die Überwachung zu aktivieren. Wenn dieser Link nicht angezeigt wird, wurde die Überwachung für Ihre Organisation bereits aktiviert. 
  
4. Konfigurieren Sie die folgenden Suchkriterien:
    
    a. **Aktivitäten** Klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Benutzer-und Administratoraktivitäten werden in Gruppen verwandter Aktivitäten organisiert. Sie können bestimmte Aktivitäten auswählen oder auf den Namen der Aktivitätsgruppe klicken, um alle Aktivitäten in der Gruppe auszuwählen. Sie können auch auf eine ausgewählte Aktivität klicken, um die Auswahl zu löschen. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungsprotokolleinträge für die ausgewählten Aktivitäten angezeigt. Wenn Sie **Ergebnisse für alle Aktivitäten anzeigen** auswählen, werden die Ergebnisse für alle Aktivitäten angezeigt, die von dem ausgewählten Benutzer oder der Gruppe von Benutzern ausgeführt werden. 
    
    Über 100 Benutzer-und Administratoraktivitäten werden im Office 365 Überwachungsprotokoll protokolliert. Klicken Sie auf die Registerkarte über **wachte Aktivitäten** im Thema dieses Artikels, um die Beschreibungen aller Aktivitäten in den verschiedenen Office 365 Diensten anzuzeigen. 
    
    b. **Start Datum** und **Enddatum** die letzten sieben Tage sind standardmäßig ausgewählt. Wählen Sie einen Datums-und Zeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Das Datum und die Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Datumsbereich, den Sie angeben können, ist 90 Tage. Wenn der ausgewählte Datumsbereich größer als 90 Tage ist, wird ein Fehler angezeigt. 
    
    > [!TIP]
    > Wenn Sie den maximalen Datumsbereich von 90 Tagen verwenden, wählen Sie die aktuelle Uhrzeit für das **Start Datum**aus. Andernfalls wird eine Fehlermeldung angezeigt, die besagt, dass das Startdatum vor dem Enddatum liegt. Wenn Sie die Überwachung in den letzten 90 Tagen aktiviert haben, kann der maximale Datumsbereich nicht vor dem Datum beginnen, an dem die Überwachung aktiviert wurde. 
  
    c. **Benutzer** Klicken Sie in dieses Feld, und wählen Sie einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. Die Überwachungsprotokolleinträge für die ausgewählte Aktivität, die von den Benutzern ausgeführt werden, die Sie in diesem Feld ausgewählt haben, werden in der Ergebnisliste angezeigt. Lassen Sie dieses Feld leer, um Einträge für alle Benutzer (und Dienstkonten) in Ihrer Organisation zurückzugeben. 
    
    d. **Datei, Ordner oder Website** Geben Sie einen oder alle Datei-oder Ordnernamen ein, um nach Aktivitäten im Zusammenhang mit der Datei des Ordners zu suchen, die das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Wenn Sie eine URL verwenden, müssen Sie sicherstellen, dass Sie den vollständigen URL-Pfad eingeben oder nur einen Teil der URL eingeben, wobei keine Sonderzeichen oder Leerzeichen enthalten sind. 
    
    Lassen Sie dieses Feld leer, um Einträge für alle Dateien und Ordner in Ihrer Organisation zurückzugeben.
    
   **Tipps**

   - Wenn Sie alle Aktivitäten im Zusammenhang mit einer **Website**suchen, fügen Sie das Platzhalter\*Symbol () nach der URL hinzu, um alle Einträge für diese Website zurückzugeben. Beispiel: **https://contoso-my.sharepoint.com/personal/"*"**.

   - Wenn Sie alle Aktivitäten im Zusammenhang mit einer **Datei**suchen, fügen Sie das Platzhalter\*Symbol () vor dem Dateinamen hinzu, um alle Einträge für diese Datei zurückzugeben. Beispiel: **"* Customer_Profitability_Sample. csv"**.
    

    
5. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 
    
    Die Suchergebnisse werden geladen, und nach ein paar Momenten werden Sie unter **Ergebnisse**angezeigt. Wenn die Suche abgeschlossen ist, wird die Anzahl der gefundenen Ergebnisse angezeigt. Beachten Sie, dass im **Ergebnis** Bereich maximal 5.000 Ereignisse in Schritten von 150 Ereignissen angezeigt werden. Wenn mehr als 5.000 Ereignisse den Suchkriterien entsprechen, werden die neuesten 5.000-Ereignisse angezeigt. 
    
    ![Die Anzahl der Ergebnisse, die nach Abschluss der Suche angezeigt werden](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Tipps zum Durchsuchen des Überwachungsprotokolls

- Sie können bestimmte Aktivitäten für die Suche auswählen, indem Sie auf den Namen der Aktivität klicken. Sie können auch nach allen Aktivitäten in einer Gruppe (beispielsweise **Datei-und Ordner Aktivitäten**) suchen, indem Sie auf den Namen der Gruppe klicken. Wenn eine Aktivität ausgewählt ist, können Sie darauf klicken, um die Auswahl abzubrechen. Sie können auch das Suchfeld verwenden, um die Aktivitäten anzuzeigen, die das von Ihnen eingegebene Schlüsselwort enthalten.
    
    ![Klicken Sie auf Aktivitätsgruppen Name, um alle Aktivitäten auszuwählen.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Sie müssen die Option **Ergebnisse für alle Aktivitäten** in der Liste **Aktivitäten** anzeigen auswählen, um Ereignisse aus dem Exchange Admin-Überwachungsprotokoll anzuzeigen. Ereignisse aus diesem Überwachungsprotokoll zeigen einen Cmdlet-Namen (beispielsweise " **festgelegt-Postfach** ") in der Spalte " **Aktivität** " in den Ergebnissen an. Weitere Informationen erhalten Sie, indem Sie auf die Registerkarte über **wachte Aktivitäten** in diesem Thema klicken und dann auf **Exchange-Verwaltungsaktivitäten**klicken.
    
    Ebenso gibt es einige Überwachungsaktivitäten, die nicht über ein entsprechendes Element in der Liste **Aktivitäten** verfügen. Wenn Sie den Namen des Vorgangs für diese Aktivitäten kennen, können Sie nach allen Aktivitäten suchen und dann die Ergebnisse filtern, indem Sie den Namen des Vorgangs in das Feld für die Spalte " **Aktivität** " eingeben. Weitere Informationen zum Filtern der Ergebnisse finden Sie unter [Schritt 3: Filtern der Suchergebnisse](#step-3-filter-the-search-results) . 
    
- Klicken Sie auf **Löschen** , um die aktuellen Suchkriterien zu löschen. Der Datumsbereich kehrt auf den Standardwert der letzten sieben Tage zurück. Sie können auch auf **Alle löschen klicken, um die Ergebnisse aller Aktivitäten anzuzeigen** , um alle ausgewählten Aktivitäten abzubrechen. 
    
- Wenn 5.000 Ergebnisse gefunden werden, können Sie wahrscheinlich davon ausgehen, dass es mehr als 5.000 Ereignisse gibt, die die Suchkriterien erfüllt haben. Sie können entweder die Suchkriterien verfeinern und die Suche erneut ausführen, um weniger Ergebnisse zurückzugeben, oder Sie können alle Suchergebnisse exportieren, indem Sie **Ergebnisse** \> exportieren **alle Ergebnisse herunterladen**auswählen.

  
### <a name="step-2-view-the-search-results"></a>Schritt 2: Anzeigen der Suchergebnisse

Die Ergebnisse einer Überwachungsprotokoll Suche werden unter **Ergebnisse** auf der Seite **Überwachungsprotokoll Suche** angezeigt. Wie bereits erwähnt, werden maximal 5.000 (neueste) Ereignisse in Schritten von 150 Ereignissen angezeigt. Um weitere Ereignisse anzuzeigen, können Sie die Bildlaufleiste im **Ergebnis** Bereich verwenden, oder Sie können **Umschalt + Ende** drücken, um die nächsten 150-Ereignisse anzuzeigen. 
  
Die Ergebnisse enthalten die folgenden Informationen zu jedem Ereignis, das von der Suche zurückgegeben wird.
  
- **Datum:** Das Datum und die Uhrzeit (im UTC-Format), als das Ereignis aufgetreten ist. 
    
- **IP-Adresse:** Die IP-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. Die IP-Adresse wird im Adressformat IPv4 oder IPv6 angezeigt. 
    
- **Benutzer:** Der Benutzer (oder das Dienstkonto), der die Aktion ausgeführt hat, die das Ereignis ausgelöst hat. 
    
- **Aktivität:** Die vom Benutzer ausgeführte Aktivität. Dieser Wert entspricht den Aktivitäten, die Sie in der Dropdownliste **Aktivitäten** ausgewählt haben. Bei einem Ereignis aus dem Exchange-administratorüberwachungsprotokoll handelt es sich bei dem Wert in dieser Spalte um ein Exchange-Cmdlet. 
    
- **Element:** Das Objekt, das als Ergebnis der entsprechenden Aktivität erstellt oder geändert wurde. Beispielsweise die Datei, die angezeigt oder geändert wurde, oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben einen Wert in dieser Spalte. 
    
- **Details:** Weitere Details zu einer Aktivität. Auch hier haben nicht alle Aktivitäten einen Wert. 
    
> [!TIP]
> Klicken Sie unter **Ergebnisse** auf eine Spaltenüberschrift, um die Ergebnisse zu sortieren. Sie können die Ergebnisse von a bis z oder z in a sortieren. Klicken Sie auf die **Datums** Kopfzeile, um die Ergebnisse von der ältesten bis neuesten oder neuesten in die älteste zu sortieren. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Anzeigen der Details für ein bestimmtes Ereignis

Sie können weitere Details zu einem Ereignis anzeigen, indem Sie auf den Ereigniseintrag in der Liste der Suchergebnisse klicken. Eine **Detail** Seite wird angezeigt, die die detaillierten Eigenschaften aus dem Ereigniseintrag enthält. Die angezeigten Eigenschaften hängen vom Office 365 Dienst ab, in dem das Ereignis auftritt. Klicken Sie zum Anzeigen dieser Details auf **Weitere Informationen**. Beschreibungen finden Sie unter [detaillierte Eigenschaften im Office 365 Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
![Klicken Sie auf Weitere Informationen, um die detaillierten Eigenschaften des Überwachungsprotokoll-Ereignisdatensatzes anzuzeigen.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern der Suchergebnisse

Neben der Sortierung können Sie auch die Ergebnisse einer Überwachungsprotokoll Suche filtern. Dieses Feature eignet sich hervorragend, um die Ergebnisse für einen bestimmten Benutzer oder eine bestimmte Aktivität schnell Filtern zu können. Sie können anfänglich eine breite Suche erstellen und dann die Ergebnisse schnell filtern, um bestimmte Ereignisse anzuzeigen. Anschließend können Sie die Suchkriterien eingrenzen und die Suche erneut ausführen, um einen kleineren, prägnanteren Ergebnissatz zurückzugeben.
  
So filtern Sie die Ergebnisse:
  
1. Führen Sie eine Überwachungsprotokoll Suche aus.
    
2. Wenn die Ergebnisse angezeigt werden, klicken Sie auf **Filter Ergebnisse**.
    
    Stichwort Felder werden unter jeder Spaltenüberschrift angezeigt.
    
3. Klicken Sie auf eines der Felder unter einer Spaltenüberschrift, und geben Sie je nach der Spalte, nach der Sie filtern, ein Wort oder einen Ausdruck ein. Die Ergebnisse werden dynamisch angepasst, um die Ereignisse anzuzeigen, die mit Ihrem Filter übereinstimmen.
    
    ![Geben Sie ein Wort in Filter ein, um Ereignisse anzuzeigen, die dem Filter entsprechen.](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Wenn Sie einen Filter löschen möchten, klicken Sie im Feld Filter auf das **X** , oder klicken Sie einfach auf **Filter ausblenden**.
    
> [!TIP]
> Geben Sie zum Anzeigen von Ereignissen aus dem Exchange-Administrator Überwachungs **-** Protokoll im Feld **Aktivitäts** Filter einen (Bindestrich) ein. Dadurch werden Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Verwaltungsereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortieren. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Schritt 4: Exportieren der Suchergebnisse in eine Datei

Sie können die Ergebnisse einer Überwachungsprotokoll Suche in eine CSV-Datei (Comma Separated Value) auf Ihrem lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und Features wie das suchen, sortieren, Filtern und Teilen einer einzelnen Spalte (die mehrere Eigenschaften enthält) in mehrere Spalten verwenden.
  
1. Führen Sie eine Überwachungsprotokoll Suche aus, und überprüfen Sie dann die Suchkriterien, bis Sie die gewünschten Ergebnisse erhalten haben.
    
2. Klicken Sie auf **Ergebnisse exportieren** , und wählen Sie eine der folgenden Optionen aus: 
    
     - **Geladene Ergebnisse speichern** – wählen Sie diese Option aus, um nur die Einträge zu exportieren, die unter **Ergebnisse** auf der Seite **Überwachungsprotokoll Suche** angezeigt werden. Die heruntergeladene CSV-Datei enthält dieselben Spalten (und Daten), die auf der Seite angezeigt werden (Datum, Benutzer, Aktivität, Element und Details). Eine zusätzliche Spalte (mit dem Namen **more**) ist in der CSV-Datei enthalten, die weitere Informationen aus dem Überwachungsprotokolleintrag enthält. Da Sie dieselben Ergebnisse exportieren, die auf der Seite **Überwachungsprotokoll Suche** geladen (und sichtbar) werden, werden maximal 5.000 Einträge exportiert. 
    
     - **Alle Ergebnisse herunterladen** – wählen Sie diese Option aus, um alle Einträge aus dem Office 365 Überwachungsprotokoll zu exportieren, die die Suchkriterien erfüllen. Für eine große Gruppe von Suchergebnissen wählen Sie diese Option aus, um alle Einträge zusätzlich zu den 5.000-Überwachungseinträgen aus dem Überwachungsprotokoll herunterzuladen, die auf der Seite **Überwachungsprotokoll Suche** angezeigt werden können. Mit dieser Option werden die Rohdaten aus dem Überwachungsprotokoll in eine CSV-Datei heruntergeladen, und es werden zusätzliche Informationen aus dem Überwachungsprotokolleintrag in einer Spalte namens **Auditdata**. Das Herunterladen der Datei kann länger dauern, wenn Sie diese Exportoption auswählen, da die Datei viel größer sein kann als diejenige, die heruntergeladen wurde, wenn Sie die Option andere auswählen.
    
       > [!IMPORTANT]
       > Sie können maximal 50.000 Einträge aus einer einzigen Überwachungsprotokoll Suche in eine CSV-Datei herunterladen. Wenn 50.000-Einträge in die CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass es mehr als 50.000 Ereignisse gibt, die die Suchkriterien erfüllt haben. Um mehr als diesen Grenzwert zu exportieren, verwenden Sie einen Datumsbereich, um die Anzahl der Überwachungsprotokolleinträge zu verringern. Möglicherweise müssen Sie mehrere Suchvorgänge mit kleineren Datumsbereichen ausführen, um mehr als 50.000 Einträge zu exportieren. 
  
3. Nachdem Sie eine Exportoption ausgewählt haben, wird am unteren Rand des Fensters eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen, Sie im Ordner "Downloads" zu speichern oder in einem bestimmten Ordner zu speichern.
 
#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>Weitere Informationen zum Exportieren und Anzeigen von Suchergebnissen für Überwachungsprotokolle

- Wenn Sie alle Suchergebnisse herunterladen, enthält die CSV-Datei eine Spalte mit dem Namen **Auditdata**, die zusätzliche Informationen zu den einzelnen Ereignissen enthält. Die Daten in dieser Spalte bestehen aus einem JSON-Objekt, das mehrere Eigenschaften aus dem Überwachungsprotokolleintrag enthält. Jedes *Property: Value-* Paar im JSON-Objekt wird durch ein Komma getrennt. Sie können das JSON-Transformations Tool im Power Query-Editor in Excel verwenden, um die **Auditdata** -Spalte in mehrere Spalten aufzuteilen, sodass jede Eigenschaft im JSON-Objekt über eine eigene Spalte verfügt. Auf diese Weise können Sie eine oder mehrere dieser Eigenschaften sortieren und filtern. Eine Schritt-für-Schritt-Anleitung zum Transformieren des JSON-Objekts mithilfe des Power Query-Editors finden Sie unter [exportieren, konfigurieren und Anzeigen von Überwachungsprotokolldaten Sätzen](export-view-audit-log-records.md).
    
    Nachdem Sie die Spalte **Auditdata** geteilt haben, können Sie in der Spalte **Vorgänge** filtern, um die detaillierten Eigenschaften für einen bestimmten Aktivitätstyp anzuzeigen. 
    
- Die Option **alle Ergebnisse herunterladen** lädt die Rohdaten aus dem Office 365 Überwachungsprotokoll in eine CSV-Datei herunter. Diese Datei enthält unterschiedliche Spaltennamen (CreationDate, userids, Operation, Auditdata) als die Datei, die heruntergeladen wurde, wenn Sie die Option geladene **Ergebnisse speichern** auswählen. Die Werte in den zwei unterschiedlichen CSV-Dateien für dieselbe Aktivität können ebenfalls unterschiedlich sein. Beispielsweise kann die Aktivität in der Spalte **Aktion** in der CSV-Datei einen anderen Wert als den "benutzerfreundlichen" Namen haben, der in der Spalte " **Aktivität** " auf der Seite " **Überwachungsprotokoll Suche** " angezeigt wird. Beispiel: Mailbox Login: vs. User angemeldet bei Mailbox.

- Wenn Sie alle Ergebnisse aus einer Suchabfrage herunterladen, die Ereignisse aus unterschiedlichen Office 365 Diensten enthält, enthält die **Auditdata** -Spalte in der CSV-Datei je nach Dienst, in dem die Aktion ausgeführt wurde, unterschiedliche Eigenschaften. Beispielsweise enthalten Einträge aus Exchange-und Azure AD-Überwachungsprotokollen eine Eigenschaft mit dem Namen **ResultStatus** , die angibt, ob die Aktion erfolgreich war oder nicht. Diese Eigenschaft ist für Ereignisse in SharePoint nicht enthalten. In ähnlicher Weise verfügen SharePoint-Ereignisse über eine Eigenschaft, die die Website-URL für Aktivitäten im Zusammenhang mit Dateien und Ordnern identifiziert. Um dieses Verhalten zu verringern, sollten Sie verschiedene Suchvorgänge verwenden, um die Ergebnisse für Aktivitäten aus einem einzelnen Dienst zu exportieren. 
    
    Eine Beschreibung vieler Eigenschaften, die in der **Auditdata** -Spalte in der CSV-Datei aufgelistet werden, wenn Sie alle Ergebnisse herunterladen, und der Dienst, auf den sich jeder bezieht, finden Sie unter [detaillierte Eigenschaften im Office 365 Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Überwachte Aktivitäten

In den Tabellen in diesem Abschnitt werden die Aktivitäten beschrieben, die in Office 365 überwacht werden. Sie können nach diesen Ereignissen suchen, indem Sie das Überwachungsprotokoll im Security and Compliance Center durchsuchen.
  
In diesen Tabellen werden verwandte Aktivitäten oder Aktivitäten aus einem bestimmten Office 365 Dienst gruppiert. Die Tabellen enthalten den Anzeigenamen, der in der Dropdownliste **Aktivitäten** angezeigt wird, und den Namen des entsprechenden Vorgangs, der in den detaillierten Informationen eines Überwachungsdatensatzes und in der CSV-Datei angezeigt wird, wenn Sie die Suchergebnisse exportieren. Beschreibungen der detaillierten Informationen finden Sie unter [detaillierte Eigenschaften im Office 365 Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
Klicken Sie auf einen der folgenden Links, um zu einer bestimmten Tabelle zu wechseln.
  
||||
|:-----|:-----|:-----|
|[Datei-und Seiten Aktivitäten](#file-and-page-activities)<br/> |[Ordner Aktivitäten](#folder-activities)<br/> |[SharePoint-Listen Aktivitäten](#sharepoint-list-activities)<br/>|
|[Freigabe-und Zugriffs Anforderungs Aktivitäten](#sharing-and-access-request-activities)<br/> |[Synchronisierungsaktivitäten](#synchronization-activities)<br/> |[Aktivitäten für Websiteberechtigungen](#site-permissions-activities)<br/> |
|[Website Verwaltungsaktivitäten](#site-administration-activities)<br/> |[Exchange-Postfachaktivitäten](#exchange-mailbox-activities)<br/> |[Sway-Aktivitäten](#sway-activities) <br/> |
|[Benutzer Verwaltungsaktivitäten](#user-administration-activities) <br/> |[Azure Ad Gruppen Verwaltungsaktivitäten](#azure-ad-group-administration-activities) <br/> |[Anwendungs Verwaltungsaktivitäten](#application-administration-activities) <br/> |
|[Aktivitäten für die Rollenverwaltung](#role-administration-activities) <br/> |[Aktivitäten der Verzeichnisverwaltung](#directory-administration-activities) <br/>|[eDiscovery-Aktivitäten](#ediscovery-activities) <br/> |
|[Erweiterte eDiscovery-Aktivitäten](#advanced-ediscovery-activities)<br/> |[Power BI-Aktivitäten](#power-bi-activities) <br/> |[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)<br/>|
|[Microsoft Teams-Aktivitäten](#microsoft-teams-activities) <br/> |[Jammern von Aktivitäten](#yammer-activities) <br/> |[Microsoft Flow-Aktivitäten](#microsoft-flow-activities) <br/>|
|[Microsoft PowerApps-Aktivitäten](#microsoft-powerapps)<br/>|[Microsoft Stream-Aktivitäten](#microsoft-stream-activities) <br/>|[Exchange-Administratoraktivitäten](#exchange-admin-audit-log)<br/>|
||||
  
### <a name="file-and-page-activities"></a>Datei-und Seiten Aktivitäten
  
In der folgenden Tabelle werden die Datei-und Seiten Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Datei wird aufgerufen  <br/> |FileAccessed  <br/> |Ein Benutzer- oder Systemkonto greift auf eine Datei zu.  <br/> |
|keine  <br/> |FileAccessedExtended  <br/> |Dies bezieht sich auf die "accessed file"-Aktivität (fileaccessed). Ein FileAccessedExtended-Ereignis wird protokolliert, wenn dieselbe Person während eines längeren Zeitraums (bis zu 3 Stunden) ständig auf eine Datei zugreift. Der Zweck der Protokollierung von FileAccessedExtended-Ereignissen besteht darin, die Anzahl der fileaccessed-Ereignisse zu verringern, die protokolliert werden, wenn ständig auf eine Datei zugegriffen wird. Dadurch wird das Rauschen mehrerer fileaccessed-Datensätze für die im Wesentlichen dieselbe Benutzeraktivität reduziert, und Sie können sich auf das anfängliche (und wichtigere) fileaccessed-Ereignis konzentrieren.  <br/> |
|Geänderte Konformitätsrichtlinien Bezeichnung<br/> |ComplianceSettingChanged<br/> |Eine Aufbewahrungs Bezeichnung wurde auf ein Dokument angewendet oder daraus entfernt. Dieses Ereignis wird ausgelöst, wenn eine Aufbewahrungs Bezeichnung manuell oder automatisch auf eine Nachricht angewendet wird.<br/> |
|Datensatzstatus in gesperrt geändert<br/> |LockRecord<br/> |Der Datensatzstatus einer Aufbewahrungs Bezeichnung, die ein Dokument als Datensatz klassifiziert, wurde gesperrt. Dies bedeutet, dass das Dokument nicht geändert oder gelöscht werden kann. Nur Benutzer, denen mindestens die Berechtigung Teilnehmer für eine Website zugewiesen ist, können den Datensatzstatus eines Dokuments ändern.<br/> |
|Geänderter Datensatzstatus in entsperrt<br/> |UnlockRecord<br/> |Der Datensatzstatus einer Aufbewahrungs Bezeichnung, die ein Dokument als Datensatz klassifiziert, wurde entsperrt. Dies bedeutet, dass das Dokument geändert oder gelöscht werden kann. Nur Benutzer, denen mindestens die Berechtigung Teilnehmer für eine Website zugewiesen ist, können den Datensatzstatus eines Dokuments ändern.<br/><br/> |
|Datei eingecheckt  <br/> |Filecheckedin  <br/> |Benutzer checkt ein Dokument ein, das aus einer Dokumentbibliothek ausgecheckt wurde.  <br/> |
|Ausgecheckte Datei  <br/> |FileCheck out  <br/> |Ein Benutzer checkt ein Dokument aus, das sich in einer Dokumentbibliothek befindet. Benutzer können alle Dokumente, die für sie freigegeben wurden, auschecken oder ändern.  <br/> |
|Kopierte Datei  <br/> |FileCopied  <br/> |Ein Benutzer kopiert ein Dokument von einer Website. Die kopierte Datei kann in einem anderen Ordner auf der Website gespeichert werden.  <br/> |
|Gelöschte Datei  <br/> |FileDeleted  <br/> |Ein Benutzer löscht ein Dokument von einer Website.  <br/> |
|Gelöschte Datei aus dem Papierkorb  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem Papierkorb einer Website.  <br/> |
|Gelöschte Datei aus dem endgültigen Papierkorb  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem endgültigen Papierkorb einer Website.  <br/> |
|Konformitätsrichtlinien Bezeichnung für den gelöschten Datensatz<br/> |ComplianceRecordDelete<br/> |Ein Dokument, das als Datensatz klassifiziert wurde, wurde gelöscht. Ein Dokument wird als Datensatz betrachtet, wenn eine Aufbewahrungs Bezeichnung, die Inhalte als Datensatz klassifiziert, auf das Dokument angewendet wird. <br/> |
|Konflikt bei erkannter Dokument Sensitivität <br/>|DocumentSensitivityMismatchDetected<br/>|Der Benutzer lädt ein Dokument hoch, das mit einer Vertraulichkeits Bezeichnung klassifiziert wurde, die eine höhere Priorität aufweist als die Vertraulichkeits Bezeichnung, die auf die Website angewendet wird, in die das Dokument hochgeladen wird. Hinweis Dieses Ereignis wird nicht ausgelöst, wenn die auf eine Website angewendete Vertraulichkeits Bezeichnung eine höhere Priorität aufweist als die Vertraulichkeits Bezeichnung, die auf ein Dokument angewendet wird, das auf die Website hochgeladen wird. Weitere Informationen zur Priorität "Sensitivitäts Bezeichnung" finden Sie im Abschnitt "Bezeichnungs Priorität" in [Übersicht über Sensitivitäts Bezeichnungen](sensitivity-labels.md#label-priority-order-matters).<br/>|
|Erkannte Schadsoftware in Datei  <br/> |FileMalwareDetected  <br/> |SharePoint-Antivirus-Engine erkennt Schadsoftware in einer Datei.  <br/> |
|Auschecken der Datei verworfen  <br/> |FileCheckOutDiscarded  <br/> |Der Benutzer verwirft eine ausgecheckte Datei. Das bedeutet, dass alle Änderungen, die an der Datei vorgenommen wurden, während sie ausgecheckt war, verworfen und nicht in der Version des Dokuments in der Dokumentbibliothek gespeichert werden.  <br/> |
|Heruntergeladene Datei  <br/> |FileDownloaded  <br/> |Ein Benutzer lädt ein Dokument von einer Website herunter.  <br/> |
|Geänderte Datei  <br/> |FileModified  <br/> |Das Benutzer-oder Systemkonto ändert den Inhalt oder die Eigenschaften eines Dokuments, das sich auf einer Website befindet.  <br/> |
|keine  <br/> |FileModifiedExtended  <br/> |Dies bezieht sich auf die "geänderte Datei" (File modified)-Aktivität. Ein FileModifiedExtended-Ereignis wird protokolliert, wenn dieselbe Person eine Datei kontinuierlich für einen längeren Zeitraum (bis zu 3 Stunden) ändert. Der Zweck der Protokollierung von FileModifiedExtended-Ereignissen besteht darin, die Anzahl von filemodified-Ereignissen zu verringern, die protokolliert werden, wenn eine Datei ständig geändert wird. Dadurch wird das Rauschen mehrerer filemodified-Datensätze für die im Wesentlichen dieselbe Benutzeraktivität reduziert, und Sie können sich auf das anfängliche (und wichtigere) filemodified-Ereignis konzentrieren.  <br/> |
|Verschobene Datei  <br/> |FileMoved  <br/> |Der Benutzer verschiebt ein Dokument von seinem aktuellen Speicherort auf einer Website an einen neuen Speicherort.  <br/> |
|Alle Nebenversionen der Datei wieder verwendet  <br/> |FileVersionsAllMinorsRecycled  <br/> |Der Benutzer löscht alle Nebenversionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Alle Versionen der Datei wieder verwendet  <br/> |FileVersionsAllRecycled  <br/> |Der Benutzer löscht alle Versionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Recycelte Version der Datei  <br/> |FileVersionRecycled  <br/> |Der Benutzer löscht eine Version aus dem Versionsverlauf einer Datei. Die gelöschte Version wird in den Papierkorb der Website verschoben.  <br/> |
|Umbenannte Datei  <br/> |FileRenamed  <br/> |Benutzer benennt ein Dokument auf einer Website um.  <br/> |
|Wiederhergestellte Datei  <br/> |FileRestored  <br/> |Ein Benutzer stellt ein Dokument aus dem Papierkorb einer Website wieder her.  <br/> |
|Hochgeladene Datei  <br/> |FileUploaded  <br/> |Ein Benutzer lädt ein Dokument in einen Ordner auf einer Website hoch.  <br/> |
|Angezeigte Seite  <br/> |PageViewed  <br/> |Der Benutzer zeigt eine Seite auf einer Website an. Dies umfasst nicht die Verwendung eines Webbrowsers zum Anzeigen von Dateien, die sich in einer Dokumentbibliothek befinden.  <br/> |
|keine  <br/> |PageViewedExtended  <br/> |Dies bezieht sich auf die Aktivität "betrachtete Seite" (mit Zugriff). Ein PageViewedExtended-Ereignis wird protokolliert, wenn dieselbe Person eine Webseite kontinuierlich für einen längeren Zeitraum (bis zu 3 Stunden) anzeigt. Der Zweck der Protokollierung von PageViewedExtended-Ereignissen besteht darin, die Anzahl von Ereignis Anteilen zu reduzieren, die protokolliert werden, wenn eine Seite kontinuierlich angezeigt wird. Auf diese Weise wird das Rauschen mehrerer Datensätze mit Seitenzugriff für die im Wesentlichen dieselbe Benutzeraktivität reduziert, und Sie können sich auf das anfängliche (und wichtigere) Zugriff-Ereignis konzentrieren.  <br/> |
|Vom Client signalisiert anzeigen <br/>|ClientViewSignaled<br/>|Der Client eines Benutzers (beispielsweise Website oder Mobile App) hat signalisiert, dass die angegebene Seite vom Benutzer angezeigt wurde. Diese Aktivität wird häufig nach einem PagePrefetched-Ereignis für eine Seite protokolliert. <br/><br/>**Hinweis**: da ClientViewSignaled-Ereignisse vom Client anstelle des Servers signalisiert werden, kann es sein, dass das Ereignis möglicherweise nicht vom Server protokolliert wird und daher möglicherweise nicht im Überwachungsprotokoll angezeigt wird. Es ist auch möglich, dass die Informationen im Überwachungseintrag möglicherweise nicht vertrauenswürdig sind. Da die Identität des Benutzers jedoch durch das Token überprüft wird, das zum Erstellen des Signals verwendet wird, ist die Identität des Benutzers, der im entsprechenden Überwachungseintrag aufgeführt ist, korrekt. |
|keine <br/>|PagePrefetched<br/>|Der Client eines Benutzers (beispielsweise Website oder Mobile App) hat die angegebene Seite angefordert, um die Leistung zu verbessern, wenn der Benutzer zu ihm navigiert. Dieses Ereignis wird protokolliert, um anzugeben, dass der Seiteninhalt dem Client des Benutzers zugestellt wurde; Dieses Ereignis ist kein definitiver Hinweis darauf, dass der Benutzer tatsächlich zu der Seite navigiert ist. Wenn der Seiteninhalt vom Client gerendert wird (gemäß der Anforderung des Benutzers), sollte ein ClientViewSignaled-Ereignis generiert werden. Beachten Sie, dass nicht alle Clients die Angabe eines Pre-Fetch unterstützen, weshalb einige vorab abgerufene Aktivitäten stattdessen möglicherweise als geteilte Ereignisse protokolliert werden.<br/>|
||||
  
### <a name="folder-activities"></a>Ordner Aktivitäten
  
In der folgenden Tabelle werden die Ordner Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Kopierter Ordner  <br/> |FolderCopied  <br/> |Der Benutzer kopiert einen Ordner von einer Website an einen anderen Speicherort in SharePoint oder OneDrive für Unternehmen.  <br/> |
|Erstellter Ordner  <br/> |FolderCreated  <br/> |Der Benutzer erstellt einen Ordner auf einer Website.  <br/> |
|Gelöschter Ordner  <br/> |FolderDeleted  <br/> |Ein Benutzer löscht einen Ordner von einer Website.  <br/> |
|Gelöschter Ordner aus dem Papierkorb  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Ein Benutzer löscht einen Ordner aus dem Papierkorb einer Website.  <br/> |
|Gelöschter Ordner aus dem endgültigen Papierkorb  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Ein Benutzer löscht einen Ordner aus dem endgültigen Papierkorb einer Website.  <br/> |
|Geänderter Ordner  <br/> |FolderModified  <br/> |Der Benutzer ändert einen Ordner auf einer Website. Dies umfasst das Ändern der Ordnermetadaten, beispielsweise das Ändern von Tags und Eigenschaften.  <br/> |
|Verschobener Ordner  <br/> |FolderMoved  <br/> |Der Benutzer verschiebt einen Ordner an einen anderen Speicherort auf einer Website.  <br/> |
|Umbenannter Ordner  <br/> |FolderRenamed  <br/> |Der Benutzer benennt einen Ordner auf einer Website um.  <br/> |
|Wiederhergestellter Ordner  <br/> |FolderRestored  <br/> |Der Benutzer stellt einen gelöschten Ordner aus dem Papierkorb einer Website wieder her.  <br/> |
||||
  
### <a name="sharepoint-list-activities"></a>SharePoint-Listen Aktivitäten
  
In der folgenden Tabelle werden Aktivitäten im Zusammenhang mit der Interaktion von Benutzern mit Listen und Listenelementen in SharePoint Online beschrieben.

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
| Erstellte Liste              | ListCreated              | Ein Benutzer hat eine neue SharePoint-Liste erstellt.|
| Erstellte Listenspalte       | ListColumnCreated        | Ein Benutzer hat eine neue SharePoint-Listenspalte erstellt. Eine Listenspalte ist eine Spalte, die an eine oder mehrere SharePoint-Listen angefügt ist. |
| Erstellter Listeninhaltstyp | ListContentTypeCreated   | Ein Benutzer hat einen neuen Listeninhaltstyp erstellt. Ein Listeninhaltstyp ist ein Inhaltstyp, der an eine oder mehrere SharePoint-Listen angefügt ist.|
| Erstelltes Listenelement         | ListItemCreated          | Ein Benutzer hat ein neues Element in einer vorhandenen SharePoint-Liste erstellt.|
| Erstellte Websitespalte       | SiteColumnCreated        | Ein Benutzer hat eine neue SharePoint-Websitespalte erstellt. Eine Websitespalte ist eine Spalte, die nicht an eine Liste angefügt ist. Eine Websitespalte ist auch eine Metadatenstruktur, die von einer beliebigen Liste in einem bestimmten Web verwendet werden kann.|
| Erstellter Websiteinhaltstyp | Erstellter Website-ContentType | Ein Benutzer hat einen neuen Websiteinhaltstyp erstellt. Bei einem Websiteinhaltstyp handelt es sich um einen Inhaltstyp, der an die übergeordnete Website angefügt ist.|
| Gelöschte Liste              | ListDeleted              | Ein Benutzer hat eine SharePoint-Liste gelöscht.|
| Gelöschte Listenspalte       | Listenspalte gelöscht      | Ein Benutzer hat eine SharePoint-Listenspalte gelöscht.|
| Gelöschter Listeninhaltstyp | ListContentTypeDeleted   | Ein Benutzer hat einen Listeninhaltstyp gelöscht. |
| Gelöschtes Listenelement         | Listenelement gelöscht        | Ein Benutzer hat ein SharePoint-Listenelement gelöscht.|
| Spalte "Gelöschte Websites"       | SiteColumnDeleted        | Ein Benutzer hat eine SharePoint-Websitespalte gelöscht. |
| Gelöschter Websiteinhaltstyp | SiteContentTypeDeleted   | Ein Benutzer hat einen Websiteinhaltstyp gelöscht.|
| Aufbereitetes Listenelement        | ListItemRecycled         | Ein Benutzer hat ein SharePoint-Listenelement in den Papierkorb verschoben.|
| Wiederhergestellte Liste             | ListRestored             | Ein Benutzer hat eine SharePoint-Liste aus dem Papierkorb wiederhergestellt.|
| Wieder hergestelltes Listenelement        | ListItemRestored         | Ein Benutzer hat ein SharePoint-Listenelement aus dem Papierkorb wiederhergestellt.|
| Aktualisierte Liste              | ListUpdated              | Ein Benutzer hat eine SharePoint-Liste aktualisiert, indem er eine oder mehrere Eigenschaften ändert.|
| Aktualisierte Listenspalte       | ListColumnUpdated        | Ein Benutzer hat eine SharePoint-Listenspalte durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
| Aktualisierter Listeninhaltstyp | ListContentTypeUpdated   | Ein Benutzer hat einen Listeninhaltstyp durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
| Aktualisiertes Listenelement         | ListItemUpdated          | Ein Benutzer hat ein SharePoint-Listenelement aktualisiert, indem eine oder mehrere Eigenschaften geändert wurden.|  
| Aktualisierte Websitespalte       | SiteColumnUpdated        | Ein Benutzer hat eine SharePoint-Websitespalte durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
| Aktualisierter Websiteinhaltstyp | SiteContentTypeUpdated   | Ein Benutzer hat einen Websiteinhaltstyp durch Ändern einer oder mehrerer Eigenschaften aktualisiert.|
||||

### <a name="sharing-and-access-request-activities"></a>Freigabe-und Zugriffs Anforderungs Aktivitäten
  
In der folgenden Tabelle werden die Benutzer Freigabe-und Zugriffs Anforderungs Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben. Bei Freigabe Ereignissen identifiziert die **Detail** Spalte unter **Ergebnisse** den Namen des Benutzers oder der Gruppe, für die das Element freigegeben wurde, und ob dieser Benutzer oder diese Gruppe ein Mitglied oder Gast in Ihrer Organisation ist. Weitere Informationen finden Sie unter [Use Sharing Auditing in the Office 365 Audit Log](use-sharing-auditing.md).
  
> [!NOTE]
> Benutzer können entweder *Mitglieder* oder *Gäste* sein, die auf der usertype-Eigenschaft des User-Objekts basieren. Ein Mitglied ist normalerweise ein Mitarbeiter, und ein Gast ist normalerweise ein Mitarbeiter außerhalb Ihrer Organisation. Wenn ein Benutzer eine Freigabeeinladung akzeptiert (und nicht bereits Teil Ihrer Organisation ist), wird ein Gastkonto für Sie im Verzeichnis Ihrer Organisation erstellt. Wenn der Gastbenutzer über ein Konto in Ihrem Verzeichnis verfügt, werden Ressourcen möglicherweise direkt für Sie freigegeben (ohne eine Einladung erforderlich). 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Berechtigungsstufe zur Websitesammlung hinzugefügt  <br/> |PermissionLevelAdded  <br/> |Eine Berechtigungsstufe wurde einer Websitesammlung hinzugefügt.  <br/> |
|Akzeptierte Zugriffsanforderung  <br/> |AccessRequestAccepted  <br/> |Eine Zugriffsanforderung für eine Website, einen Ordner oder ein Dokument wurde akzeptiert, und dem anfordernden Benutzer wurde Zugriff erteilt.  <br/> |
|Einladung zur Freigabe angenommen  <br/> |SharingInvitationAccepted  <br/> |Benutzer (Mitglied oder Gast) akzeptierten eine Freigabeeinladung und erhielten Zugriff auf eine Ressource. Dieses Ereignis enthält Informationen über den Benutzer, der eingeladen wurde, und die e-Mail-Adresse, die zum Annehmen der Einladung verwendet wurde (Sie können unterschiedlich sein). Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, in dem beschrieben wird, wie dem Benutzer der Zugriff auf die Ressource gewährt wurde, beispielsweise das Hinzufügen des Benutzers zu einer Gruppe, die Zugriff auf die Ressource hat.  <br/> |
|Blockierte Freigabeeinladung  <br/> |SharingInvitationBlocked  <br/> | Eine von einem Benutzer in Ihrer Organisation gesendete Freigabeeinladung wird aufgrund einer Richtlinie für externe Freigaben blockiert, die die externe Freigabe basierend auf der Domäne des Zielbenutzers zulässt oder ablehnt. In diesem Fall wurde die Freigabeeinladung blockiert, weil:  <br/>  Die Domäne des Zielbenutzers ist nicht in der Liste der zulässigen Domänen enthalten.  <br/>  Oder  <br/>  Die Domäne des Zielbenutzers ist in der Liste der blockierten Domänen enthalten.  <br/>  Weitere Informationen zum Zulassen oder Blockieren der externen Freigabe basierend auf Domänen finden Sie unter [restricted Domains Sharing in SharePoint Online and OneDrive für Unternehmen](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Erstellte Zugriffsanforderung  <br/> |AccessRequestCreated  <br/> |Benutzer fordert Zugriff auf eine Website, einen Ordner oder ein Dokument an, für die Sie keine Zugriffsberechtigungen haben.  <br/> |
|Erstellen eines Unternehmens-freigegebenen Links  <br/> |CompanyLinkCreated  <br/> |Der Benutzer hat einen unternehmensweiten Link zu einer Ressource erstellt. unternehmensweite Links können nur von Mitgliedern in Ihrer Organisation verwendet werden. Sie können nicht von Gästen verwendet werden.  <br/> |
|Anonyme Verknüpfung erstellt  <br/> |AnonymousLinkCreated  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource erstellt. Jeder, der über diesen Link verfügt, kann auf die Ressource zugreifen, ohne authentifiziert werden zu müssen.  <br/> |
|Erstellter sicherer Link  <br/> |SecureLinkCreated  <br/> |Für dieses Element wurde ein sicherer Freigabe Link erstellt.  <br/> |
|Erstellte Freigabeeinladung  <br/> |SharingInvitationCreated  <br/> |Der Benutzer hat eine Ressource in SharePoint Online oder OneDrive für Unternehmen mit einem Benutzer freigegeben, der sich nicht im Verzeichnis Ihrer Organisation befindet.  <br/> |
|Gelöschte sichere Verbindung  <br/> |SecureLinkDeleted  <br/> |Eine sichere Freigabe Verbindung wurde gelöscht.  <br/> |
|Verweigerte Zugriffsanforderung  <br/> |AccessRequestDenied  <br/> |Eine Zugriffsanforderung für eine Website, einen Ordner oder ein Dokument wurde abgelehnt.  <br/> |
|Ein Unternehmen mit freigegebener Verbindung entfernt  <br/> |CompanyLinkRemoved  <br/> |Ein Benutzer hat einen unternehmensweiten Link zu einer Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Entfernen eines anonymen Links  <br/> |AnonymousLinkRemoved  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Freigegebene Datei, Ordner oder Website  <br/> |SharingSet  <br/> |Benutzer (Mitglied oder Gast) haben eine Datei, einen Ordner oder eine Website in SharePoint freigegeben oder OneDrive für Unternehmen mit einem Benutzer im Verzeichnis Ihrer Organisation. Der Wert in der Spalte **Detail** für diese Aktivität gibt den Namen des Benutzers an, für den die Ressource freigegeben wurde, und gibt an, ob dieser Benutzer ein Mitglied oder ein Gast ist. Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, in dem beschrieben wird, wie dem Benutzer der Zugriff auf die Ressource gewährt wurde. beispielsweise das Hinzufügen des Benutzers zu einer Gruppe, die Zugriff auf die Ressource hat.  <br/> |
|Aktualisierte Zugriffsanforderung  <br/> |AccessRequestUpdated  <br/> |Eine Zugriffsanforderung für ein Element wurde aktualisiert.  <br/> |
|Anonymer Link aktualisiert  <br/> |AnonymousLinkUpdated  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource aktualisiert. Das aktualisierte Feld ist in der EventData-Eigenschaft enthalten, wenn Sie die Suchergebnisse exportieren.  <br/> |
|Aktualisierte Freigabeeinladung  <br/> |SharingInvitationUpdated  <br/> |Eine externe Freigabeeinladung wurde aktualisiert.  <br/> |
|Anonyme Verknüpfung verwendet  <br/> |AnonymousLinkUsed  <br/> |Ein anonymer Benutzer hat über einen anonymen Link auf eine Ressource zugegriffen. Die Identität des Benutzers ist möglicherweise unbekannt, aber Sie können andere Details wie die IP-Adresse des Benutzers abrufen.  <br/> |
|Nicht freigegebene Datei, Ordner oder Website  <br/> |SharingRevoked  <br/> |Der Benutzer (Mitglied oder Gast) hat eine Datei, einen Ordner oder eine Website, die zuvor für einen anderen Benutzer freigegeben wurde, nicht freigegeben.  <br/> |
|Verwendet einen Unternehmens-Link mit Freigabe  <br/> |CompanyLinkUsed  <br/> |Der Benutzer hat über einen unternehmensweiten Link auf eine Ressource zugegriffen.  <br/> |
|Verwendeter sicherer Link  <br/> |SecureLinkUsed  <br/> |Ein Benutzer hat eine sichere Verbindung verwendet.  <br/> |
|Zu sicherer Link hinzugefügter Benutzer  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die einen Link zur sicheren Freigabe verwenden können.  <br/> |
|Benutzer wurde aus einem sicheren Link entfernt  <br/> |RemovedFromSecureLink  <br/> |Ein Benutzer wurde aus der Liste der Entitäten entfernt, die einen Link zur sicheren Freigabe verwenden können.  <br/> |
|Freigabeeinladung zurückgezogen  <br/> |SharingInvitationRevoked  <br/> |Der Benutzer hat eine Freigabeeinladung zu einer Ressource zurückgezogen.  <br/> |
||||
  
### <a name="synchronization-activities"></a>Synchronisierungsaktivitäten
  
In der folgenden Tabelle werden die Datei Synchronisierungsaktivitäten in SharePoint Online und OneDrive für Unternehmen aufgeführt.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Zulässiger Computer zum Synchronisieren von Dateien  <br/> |ManagedSyncClientAllowed  <br/> |Benutzer erstellt erfolgreich eine Synchronisierungsbeziehung mit einer Website. Die Synchronisierungsbeziehung ist erfolgreich, da der Computer des Benutzers Mitglied einer Domäne ist, die der Liste der Domänen hinzugefügt wurde (die als *sichere Empfängerliste* bezeichnet wird), die auf Dokumentbibliotheken in Ihrer Organisation zugreifen kann.  <br/> Weitere Informationen zu dieser Funktion finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die in der Liste der sicheren Empfänger enthalten sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Blockierter Computer für das Synchronisieren von Dateien  <br/> |UnmanagedSyncClientBlocked  <br/> |Der Benutzer versucht, eine Synchronisierungsbeziehung mit einer Website von einem Computer aus herzustellen, der nicht Mitglied der Domäne Ihrer Organisation ist oder Mitglied einer Domäne ist, die nicht der Liste der Domänen hinzugefügt wurde (so genannte *Liste sicherer Empfänger)* , die auf Dokument zugreifen kann. Bibliotheken in Ihrer Organisation. Die Synchronisierungsbeziehung ist nicht zulässig, und der Computer des Benutzers ist für das Synchronisieren, Herunterladen oder Hochladen von Dateien der Dokumentbibliothek gesperrt.  <br/> Informationen zu dieser Funktion finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die in der Liste der sicheren Empfänger enthalten sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Heruntergeladene Dateien auf Computer  <br/> |FileSyncDownloadedFull  <br/> |Benutzer richtet eine Synchronisierungsbeziehung ein und downloadet erfolgreich Dateien erstmalig auf Ihren Computer aus einer Dokumentbibliothek.  <br/> |
|Heruntergeladene Dateiänderungen auf Computer  <br/> |FileSyncDownloadedPartial  <br/> |Benutzer lädt erfolgreich alle Änderungen an Dateien aus einer Dokumentbibliothek herunter. Diese Aktivität gibt an, dass alle Änderungen, die an Dateien in der Dokumentbibliothek vorgenommen wurden, auf den Computer des Benutzers heruntergeladen wurden. Nur Änderungen wurden heruntergeladen, da die Dokumentbibliothek zuvor vom Benutzer heruntergeladen wurde (wie von den **heruntergeladenen Dateien in die Computer** Aktivität angezeigt).  <br/> |
|Hochgeladene Dateien in die Dokumentbibliothek  <br/> |FileSyncUploadedFull  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung ein und lädt die Dateien zum ersten Mal erfolgreich von Ihrem Computer in eine Dokumentbibliothek hoch.  <br/> |
|Hochgeladene Dateiänderungen an Dokumentbibliothek  <br/> |FileSyncUploadedPartial  <br/> |Der Benutzer lädt erfolgreich Änderungen an Dateien in einer Dokumentbibliothek hoch. Dieses Ereignis gibt an, dass alle Änderungen, die an der lokalen Version einer Datei aus einer Dokumentbibliothek vorgenommen wurden, erfolgreich in die Dokumentbibliothek geladen werden. Nur Änderungen werden hochgeladen, da diese Dateien zuvor vom Benutzer hochgeladen wurden (wie von den **hochgeladenen Dateien in die Dokument Bibliotheks** Aktivität angezeigt).  <br/> |
||||

### <a name="site-permissions-activities"></a>Aktivitäten für Websiteberechtigungen

Die folgende Tabelle enthält Ereignisse im Zusammenhang mit dem Zuweisen von Berechtigungen in SharePoint und der Verwendung von Gruppen zum erteilen (und widerrufen) des Zugriffs auf Websites.

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Websitesammlungsadministrator hinzugefügt  <br/> |SiteCollectionAdminAdded  <br/> |Websitesammlungsadministrator oder-Besitzer fügt eine Person als Websitesammlungsadministrator für eine Website hinzu. Websitesammlungsadministratoren verfügen über Vollzugriff für die Websitesammlung und alle Unterwebsites. Diese Aktivität wird auch protokolliert, wenn ein Administrator selbst Zugriff auf das OneDrive-Konto eines Benutzers gewährt (durch Bearbeiten des Benutzerprofils im SharePoint Admin Center oder [mithilfe des Microsoft 365 admin Centers](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)). <br/> |
|Benutzer oder Gruppe zur SharePoint-Gruppe hinzugefügt  <br/> |AddedToGroup  <br/> |Der Benutzer hat einer SharePoint-Gruppe ein Mitglied oder einen Gast hinzugefügt. Dies ist möglicherweise eine absichtliche Aktion oder das Ergebnis einer anderen Aktivität, beispielsweiseeines Freigabe Ereignisses.  <br/> |
|Vererbung von Berechtigungsebenen abgebrochen  <br/> |PermissionLevelsInheritanceBroken  <br/> |Ein Element wurde so geändert, dass es nicht mehr Berechtigungsstufen von seinem übergeordneten Element erbt.  <br/> |
|Freigabe Vererbung abgebrochen  <br/> |SharingInheritanceBroken  <br/> |Ein Element wurde so geändert, dass es keine Freigabeberechtigungen mehr von seinem übergeordneten Element erbt.  <br/> |
|Erstellte Gruppe  <br/> |GroupAdded  <br/> |Websiteadministrator oder Besitzer erstellen eine Gruppe für eine Website oder führen eine Aufgabe aus, die dazu führt, dass eine Gruppe erstellt wird. Wenn ein Benutzer beispielsweise zum ersten Mal einen Link zum Freigeben einer Datei erstellt, wird eine Systemgruppe zur OneDrive for Business-Website hinzugefügt. Dieses Ereignis kann auch dadurch entstehen, dass ein Benutzer einen Link mit Bearbeitungsberechtigungen für eine freigegebene Datei erstellt.  <br/> |
|Gelöschte Gruppe  <br/> |GroupRemoved  <br/> |Benutzer löscht eine Gruppe von einer Website.  <br/> |
|Geänderte Zugriffs Anforderungs Einstellung  <br/> |WebRequestAccessModified  <br/> |Die Einstellungen für die Zugriffsanforderung wurden auf einer Website geändert.  <br/> |
|Geänderte Einstellung "Mitglieder können freigeben"  <br/> |WebMembersCanShareModified  <br/> |Die Einstellung " **Mitglieder können freigeben** " wurde auf einer Website geändert.  <br/> |
|Geänderte Berechtigungsstufe für Websitesammlung  <br/> |PermissionLevelModified  <br/> |Eine Berechtigungsstufe wurde in einer Websitesammlung geändert.  <br/> |
|Geänderte Websiteberechtigungen  <br/> |SitePermissionsModified  <br/> |Der Websiteadministrator oder Besitzer (oder Systemkonto) ändert die Berechtigungsstufe, die einer Gruppe auf einer Website zugewiesen ist. Diese Aktivität wird auch protokolliert, wenn alle Berechtigungen aus einer Gruppe entfernt werden.  <br/><br/> **Hinweis**: dieser Vorgang ist in SharePoint Online veraltet. Um verwandte Ereignisse zu finden, können Sie nach anderen Berechtigungs bezogenen Aktivitäten wie dem **hinzugefügten Websitesammlungsadministrator**, dem **hinzugefügten Benutzer oder der Gruppe zur SharePoint-Gruppe**, dem zulässigen **Benutzer zum Erstellen von Gruppen, der** **erstellten Gruppe**und dem Löschen suchen. ** Gruppe aus.**|
|Entfernte Berechtigungsstufe aus Websitesammlung  <br/> |PermissionLevelRemoved  <br/> |Eine Berechtigungsstufe wurde aus einer Websitesammlung entfernt.  <br/> |
|Websitesammlungsadministrator entfernt  <br/> |SiteCollectionAdminRemoved <br/> |Websitesammlungsadministrator oder-Besitzer entfernt eine Person als Websitesammlungsadministrator für eine Website. Diese Aktivität wird auch protokolliert, wenn ein Administrator sich selbst aus der Liste der Websitesammlungsadministratoren für das OneDrive-Konto eines Benutzers entfernt (durch Bearbeiten des Benutzerprofils im SharePoint Admin Center).  Beachten Sie, dass Sie nach allen Aktivitäten suchen müssen, um diese Aktivität in den Überwachungsprotokoll-Suchergebnissen zurückzugeben. <br/> |
|Entfernter Benutzer oder eine Gruppe aus der SharePoint-Gruppe  <br/> |RemovedFromGroup  <br/> |Ein Benutzer hat ein Mitglied oder einen Gast aus einer SharePoint-Gruppe entfernt. Möglicherweise handelt es sich um eine vorsätzliche Aktion oder das Ergebnis einer anderen Aktivität, beispielsweise ein Freigabe Ereignis.  <br/> |
|Angeforderte Websiteadministrator Berechtigungen  <br/> |SiteAdminChangeRequest  <br/> |Benutzeranforderungen, die als Websitesammlungsadministrator für eine Websitesammlung hinzugefügt werden sollen. Websitesammlungsadministratoren verfügen über Vollzugriff für die Websitesammlung und alle Unterwebsites.  <br/> |
|Wiederhergestellte Freigabe Vererbung  <br/> |SharingInheritanceReset  <br/> |Es wurde eine Änderung vorgenommen, sodass ein Element Freigabeberechtigungen von seinem übergeordneten Element erbt.  <br/> |
|Aktualisierte Gruppe  <br/> |GroupUpdated  <br/> |Der Websiteadministrator oder Besitzer ändert die Einstellungen einer Gruppe für eine Website. Dazu kann das Ändern des Gruppennamens, das Anzeigen oder Bearbeiten der Gruppenmitgliedschaft und die Art der Verarbeitung von Mitgliedsanträgen gehören.  <br/> |
||||

  
### <a name="site-administration-activities"></a>Website Verwaltungsaktivitäten
  
In der folgenden Tabelle sind die Ereignisse aufgeführt, die aus Websiteverwaltungsaufgaben in SharePoint Online resultieren.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Zugelassener Datenspeicherort hinzugefügt<br/>|AllowedDataLocationAdded|Ein SharePoint-oder globaler Administrator hat einen zulässigen Datenspeicherort in einer Multi-Geo-Umgebung hinzugefügt. <br/>|
|Ausnahme Benutzer-Agent hinzugefügt  <br/> |ExemptUserAgentSet  <br/> |Ein SharePoint-oder globaler Administrator hat einen Benutzer-Agent zur Liste der freigestellten Benutzer-Agents im SharePoint Admin Center hinzugefügt.  <br/> |
|Geo-Standort-Administrator hinzugefügt<br/>|GeoAdminAdded<br/>|Ein SharePoint-oder globaler Administrator hat einen Benutzer als Geo-Administrator eines Standorts hinzugefügt. <br/>|
|Zulässiger Benutzer zum Erstellen von Gruppen  <br/> |AllowGroupCreationSet  <br/> |Websiteadministrator oder Besitzer fügt eine Berechtigungsstufe zu einer Website hinzu, die es einem Benutzer, dem diese Berechtigung zugewiesen wurde, ermöglicht, eine Gruppe für diese Website zu erstellen.  <br/> |
|Abgebrochener Standort-Geo-Wechsel  <br/> |SiteGeoMoveCancelled  <br/> |Ein SharePoint-oder globaler Administrator hat eine SharePoint-oder OneDrive-Website-geografische Verlagerung erfolgreich abgebrochen. Die Multi-Geo-Funktion ermöglicht eine Office 365 Organisation, die sich über mehrere Office 365 Rechenzentrums-Regionen erstreckt, die als GEOS bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Änderung einer Freigaberichtlinie  <br/> |SharingPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat eine SharePoint-Freigaberichtlinie mithilfe des Office 365 Administrator Portals, des SharePoint-Verwaltungsportals oder der SharePoint Online Verwaltungsshell geändert. Änderungen an den Einstellungen in der Freigaberichtlinie in Ihrer Organisation werden protokolliert. Die geänderte Richtlinie wird im Feld **ModifiedProperties** in den detaillierten Eigenschaften des Ereignisdatensatzes identifiziert.  <br/> |
|Geänderte Gerätezugriffs Richtlinie  <br/> |DeviceAccessPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat die Richtlinie für nicht verwaltete Geräte für Ihre Organisation geändert. Diese Richtlinie steuert den Zugriff auf SharePoint, OneDrive und Office 365 von Geräten, die nicht mit Ihrer Organisation verbunden sind. Zum Konfigurieren dieser Richtlinie ist ein Enterprise Mobility +-Sicherheitsabonnement erforderlich. Weitere Informationen finden Sie unter [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).  <br/> |
|Geänderte freigestellte Benutzer-Agents  <br/> |CustomizeExemptUsers  <br/> |Ein SharePoint-oder globaler Administrator hat die Liste der freigestellten Benutzer-Agents im SharePoint Admin Center angepasst. Sie können angeben, welche Benutzer-Agents vom Anzeigen einer vollständigen zu indizierenden Webseite ausgenommen werden sollen. Wenn ein von Ihnen als "freigegebener" bezeichneter Benutzer-Agent auf ein InfoPath-Formular stößt, wird das Formular anstelle einer ganzen Webseite als XML-Datei zurückgegeben. Dadurch wird die Indizierung von InfoPath-Formularen beschleunigt.  <br/> |
|Geänderte Netzwerkzugriffsrichtlinie  <br/> |NetworkAccessPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat die standortbasierte Zugriffsrichtlinie (auch als vertrauenswürdige Netzwerkgrenze bezeichnet) im SharePoint Admin Center oder mithilfe von SharePoint Online PowerShell geändert. Diese Art von Richtlinie steuert, wer auf SharePoint-und OneDrive-Ressourcen in Ihrer Organisation basierend auf autorisierten IP-Adressbereichen zugreifen kann, die Sie angeben. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf SharePoint Online-und OneDrive-Daten basierend auf dem Netzwerkspeicherort](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).  <br/> |
|Abgeschlossener Standort-geografischer Wechsel  <br/> |SiteGeoMoveCompleted  <br/> |Ein geografischer Standortwechsel, der von einem globalen Administrator in Ihrer Organisation geplant wurde, wurde erfolgreich abgeschlossen. Die Multi-Geo-Funktion ermöglicht eine Office 365 Organisation, die sich über mehrere Office 365 Rechenzentrums-Regionen erstreckt, die als GEOS bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Erstellt an-Verbindung gesendet  <br/> |SendToConnectionAdded  <br/> |Ein SharePoint-oder globaler Administrator erstellt auf der Seite Datensatzverwaltung im SharePoint Admin Center eine neue Verbindung senden an. Mit einer Senden-an-Verbindung werden die Einstellungen für ein Dokumentrepository oder ein Datenarchiv festgelegt. Wenn Sie eine Senden-an-Verbindung erstellen, kann die Inhaltsorganisation Dokumente an den angegebenen Speicherort übermitteln.  <br/> |
|Erstellte Websitesammlung  <br/> |SiteCollectionCreated  <br/> |Ein SharePoint-oder globaler Administrator erstellt eine neue Websitesammlung in Ihrer SharePoint Online Organisation, oder ein Benutzer stellt seine OneDrive für Unternehmen Website bereit.  <br/> |
|Gelöschter verwaister Hub-Standort<br/>|HubSiteOrphanHubDeleted<br/>|Ein SharePoint-oder globaler Administrator hat einen verwaisten Hub-Standort gelöscht, bei dem es sich um einen Hub-Standort handelt, dem keine Websites zugeordnet sind. Ein verwaister Hub wird wahrscheinlich durch das Löschen des ursprünglichen Hub-Standorts verursacht. <br/>|
|Gelöscht an Verbindung gesendet  <br/> |SendToConnectionRemoved  <br/> |Ein SharePoint-oder globaler Administrator löscht eine senden-an-Verbindung auf der Seite "Datensatzverwaltung" im SharePoint Admin Center.  <br/> |
|Gelöschte Website  <br/> |SiteDeleted  <br/> |Websiteadministrator löscht eine Website.  <br/> |
|Aktivierte Dokumentvorschau  <br/> |PreviewModeEnabledSet  <br/> |Websiteadministrator aktiviert die Dokumentvorschau für eine Website.  <br/> |
|Aktivierter älterer Workflow  <br/> |LegacyWorkflowEnabledSet  <br/> |Websiteadministrator oder Besitzer fügt der Website den Inhaltstyp für SharePoint 2013-Workflowtask hinzu. Globale Administratoren können auch im SharePoint Admin Center Workflows für die gesamte Organisation aktivieren.  <br/> |
|Office on Demand aktiviert  <br/> |OfficeOnDemandSet  <br/> |Der Websiteadministrator aktiviert Office on Demand, wodurch Benutzer auf die neueste Version von Office-Desktopanwendungen zugreifen können. Office on Demand wird im SharePoint Admin Center aktiviert und erfordert ein Office 365-Abonnement, bei dem alle Office-Anwendungen installiert werden.  <br/> |
|Aktivierte ergebnisquelle für Personen Suchvorgänge<br/>|PeopleResultsScopeSet<br/>|Der Websiteadministrator erstellt die ergebnisquelle für Personen Suchvorgänge für eine Website.<br/>|
|Aktivierte RSS-Feeds  <br/> |NewsFeedEnabledSet  <br/> |Der Websiteadministrator oder Besitzer aktiviert RSS-Feeds für eine Website. Globale Administratoren können RSS-Feeds für die gesamte Organisation im SharePoint Admin Center aktivieren.  <br/> |
|Verbundener Standort mit Hub-Standort<br/>|HubSiteJoined<br/>|Ein Websitebesitzer ordnet seine Website einem Hub-Standort zu.<br/>|
|Registrierter Hub-Standort<br/>|HubSiteRegistered<br/>|Ein SharePoint-oder globaler Administrator erstellt einen Hub-Standort. Das Ergebnis ist, dass die Website als Hub-Standort registriert ist. <br/>|
|Speicherort für zulässige Daten entfernt<br/>|AllowedDataLocationDeleted<br/>|Ein SharePoint-oder globaler Administrator hat einen zulässigen Datenspeicherort in einer Multi-Geo-Umgebung entfernt.<br/>|
|Geo-Standort-Administrator entfernt<br/>|GeoAdminDeleted<br/>|Ein SharePoint-oder globaler Administrator hat einen Benutzer als Geo-Administrator eines Standorts entfernt.<br/>|
|Umbenannter Standort  <br/> |SiteRenamed  <br/> |Websiteadministrator oder Besitzer benennt eine Website um  <br/> |
|Geplanter geografischer Standortwechsel  <br/> |SiteGeoMoveScheduled  <br/> |Ein SharePoint-oder globaler Administrator plant eine SharePoint-oder OneDrive-Website-geografische Verlagerung erfolgreich. Die Multi-Geo-Funktion ermöglicht eine Office 365 Organisation, die sich über mehrere Office 365 Rechenzentrums-Regionen erstreckt, die als GEOS bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Hostwebsite festlegen  <br/> |HostSiteSet  <br/> |Ein SharePoint-oder globaler Administrator ändert die festgelegte Website, um persönliche oder OneDrive für Unternehmen Websites zu hosten.  <br/> |
|Festlegen des Speicherkontingents für den geografischen Standort  <br/> |GeoQuotaAllocated<br/> |Ein SharePoint-oder globaler Administrator hat das Speicherkontingent für einen geografischen Standort in einer Multi-Geo-Umgebung konfiguriert.<br/> |
|Nicht verbundener Standort von Hub-Standort<br/>|HubSiteUnjoined<br/>|Ein Websitebesitzer trennt seine Website von einem Hub-Standort.<br/>|
|Nicht registrierter Hub-Standort<br/>|HubSiteUnregistered<br/>|Ein SharePoint-oder globaler Administrator hebt die Registrierung eines Standorts als Hub-Standort auf. Wenn ein Hub-Standort nicht registriert ist, funktioniert er nicht mehr als Hub-Standort. <br/>|
||||
  
### <a name="exchange-mailbox-activities"></a>Exchange-Postfachaktivitäten
  
In der folgenden Tabelle sind die Aktivitäten aufgeführt, die von der postfachüberwachungsprotokollierung protokolliert werden können. Postfachaktivitäten, die vom Postfachbesitzer, einem Delegierten Benutzer oder einem Administrator ausgeführt werden, werden im Office 365 Überwachungsprotokoll für bis zu 90 Tage automatisch angemeldet. Beachten Sie, dass es für einen Administrator möglich ist, die postfachüberwachungsprotokollierung für alle Benutzer in Ihrem organizatin zu deaktivieren. In diesem Fall werden keine Postfachaktionen für einen Benutzer protokolliert. Weitere Informationen finden Sie unter [Verwalten der postfachüberwachung](enable-mailbox-auditing.md).

 Sie können auch mithilfe des Cmdlets [Search-Mailbox auditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) in Exchange Online PowerShell nach Postfachaktivitäten suchen. 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Berechtigungen für Stellvertretungs Postfächer hinzugefügt  <br/> |AddMailboxPermissions  <br/> |Ein Administrator hat dem Postfach einer anderen Person die Berechtigung FullAccess Postfach für einen Benutzer (als Stellvertreter bezeichnet) zugewiesen. Die FullAccess-Berechtigung ermöglicht es der Stellvertretung, das Postfach der anderen Person zu öffnen und den Inhalt des Postfachs zu lesen und zu verwalten.  <br/> |
|Benutzer mit Stellvertreter Zugriff auf Kalenderordner hinzugefügt oder entfernt<br/> |UpdateCalendarDelegation<br/> |Ein Benutzer wurde dem Kalender des Postfachs eines anderen Benutzers als Stellvertreter hinzugefügt oder daraus entfernt. Mit der Kalender Delegierung kann ein anderer Benutzer in derselben Organisation Berechtigungen zum Verwalten des Kalenders des Postfachbesitzers erhalten. <br/> |
|Berechtigungen zum Ordner hinzugefügt<br/> |AddFolderPermissions<br/> |Eine Ordnerberechtigung wurde hinzugefügt. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach und die in diesen Ordnern befindlichen Nachrichten zugreifen können.<br/> |
|Nachrichten in einen anderen Ordner kopiert  <br/> |Kopieren  <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |
|Erstelltes Postfachelement  <br/> |Erstellen  <br/> |Ein Element wird im Ordner "Kalender", "Kontakte", "Notizen" oder "Aufgaben" im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht nicht überwacht wird. Außerdem wird das Erstellen eines Postfachordners nicht überwacht.  <br/> |
|Neue Posteingangsregel in Outlook-Webanwendung erstellt  <br/> |NewInboxRule<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat eine neue Posteingangsregel in der Outlook-Webanwendung erstellt.<br/> |
|Gelöschte Nachrichten aus dem Ordner "Gelöschte Elemente"  <br/> |SoftDelete  <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Diese Elemente werden in den Ordner "refundable Items" verschoben. Nachrichten werden auch in den Ordner "Wiederherstellbare Elemente" verschoben, wenn ein Benutzer Sie auswählt und **UMSCHALT + ENTF**drückt.  <br/> |
|Nachricht als Datensatz bezeichnet  <br/> |ApplyRecordLabel<br/> |Eine Nachricht wurde als Datensatz klassifiziert. Dies tritt auf, wenn eine Aufbewahrungs Bezeichnung, die Inhalte als Datensatz klassifiziert, manuell oder automatisch auf eine Nachricht angewendet wird.<br/> |
|Nachrichten in einen anderen Ordner verschoben  <br/> |Move  <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |
|Verschobene Nachrichten in den Ordner "Gelöschte Elemente"  <br/> |MoveToDeletedItems  <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |
|Berechtigung "Geänderter Ordner"  <br/> |UpdateFolderPermissions  <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Postfachordner und die Nachrichten im Ordner zugreifen können.  <br/> |
|Geänderte Posteingangsregel aus Outlook-Webanwendung<br/> |SetInboxRule<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat eine Posteingangsregel mithilfe der Outlook-Webanwendung geändert.<br/> |
|Bereinigte Nachrichten aus dem Postfach  <br/> |HardDelete  <br/> |Eine Nachricht wurde aus dem Ordner "refundable Items" gelöscht (endgültig aus dem Postfach gelöscht).  <br/> |
|Berechtigungen für Stellvertretungs Postfächer entfernt  <br/> |Remove-MailboxPermission  <br/> |Ein Administrator hat die FullAccess-Berechtigung (die einer Stellvertretung zugewiesen wurde) aus dem Postfach einer Person entfernt. Nachdem die FullAccess-Berechtigung entfernt wurde, kann die Stellvertretung das Postfach der anderen Person nicht öffnen oder auf Inhalte darauf zugreifen.  <br/> |
|Berechtigungen aus Ordner entfernt<br/> |RemoveFolderPermissions<br/> |Eine Ordnerberechtigung wurde entfernt. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach und die in diesen Ordnern befindlichen Nachrichten zugreifen können.<br/> |
|Gesendete Nachricht mit "Senden als"-Berechtigungen  <br/> |SendAs  <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |
|Gesendete Nachricht mit Berechtigungen "Senden im Auftrag von"  <br/> |SendOnBehalf  <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |
|Aktualisierte Posteingangsregeln aus dem Outlook-Client<br/> |UpdateInboxRules<br/> |Ein Postfachbesitzer oder ein anderer Benutzer mit Zugriff auf das Postfach hat eine Posteingangsregel im Outlook-Client geändert.<br/> |
|Aktualisierte Nachricht  <br/> |Aktualisieren  <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |
|Benutzer, der bei einem Postfach angemeldet ist  <br/> |Mailbox Login:  <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |
||||

### <a name="sway-activities"></a>Sway-Aktivitäten
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in Sway aufgeführt. Sway ist eine Office 365-APP, mit der Benutzer Ideen, Geschichten und Präsentationen in einer interaktiven, webbasierten Leinwand sammeln, formatieren und freigeben können. Weitere Informationen finden Sie unter [häufig gestellte Fragen zur Sway-Admin-Hilfe](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Sway-Freigabeebene  <br/> |SwayChangeShareLevel  <br/> |Der Benutzer ändert die Freigabeebene eines Sway. Dieses Ereignis erfasst den Benutzer, der den Bereich der mit einer Sway verbundenen Freigabe ändert. beispielsweise Public versus innerhalb der Organisation.  <br/> |
|Erstellt Sway  <br/> |SwayCreate  <br/> |Der Benutzer erstellt einen Sway.  <br/> |
|Gelöschter Sway  <br/> |SwayDelete  <br/> |Ein Benutzer löscht einen Sway.  <br/> |
|Deaktivierte Sway-Duplizierung  <br/> |SwayDisableDuplication  <br/> |Der Benutzer deaktiviert die Duplizierung eines Sways.  <br/> |
|Doppelter Sway  <br/> |SwayDuplicate  <br/> |Benutzer dupliziert einen Sway.  <br/> |
|Bearbeitete Sway  <br/> |SwayEdit  <br/> |Der Benutzer bearbeitet einen Sway.  <br/> |
|Aktivierte Sway-Duplizierung  <br/> |EnableDuplication  <br/> |Der Benutzer ermöglicht die Duplizierung eines Sways; die Möglichkeit für einen Benutzer, die Duplizierung einer Sway zu aktivieren, ist standardmäßig aktiviert.  <br/> |
|Aufgehobene Sway-Freigabe  <br/> |SwayRevokeShare  <br/> |Der Benutzer stoppt die Freigabe eines Sways, indem er den Zugriff auf ihn widerruft. Wenn der Zugriff widerrufen wird, ändern sich die dem Sway zugeordneten Verknüpfungen.  <br/> |
|Freigegebener Sway  <br/> |SwayShare  <br/> |Der Benutzer beabsichtigt, einen Sway zu teilen. Dieses Ereignis erfasst die Benutzeraktion des Klickens auf ein bestimmtes freigabeziel im Menü Sway share. Das Ereignis gibt nicht an, ob der Benutzer die Freigabe Aktion abgeschlossen hat.  <br/> |
|Externe Freigabe von Sway deaktiviert  <br/> |SwayExternalSharingOff  <br/> |Der Administrator deaktiviert die externe Sway-Freigabe für die gesamte Organisation mithilfe des Microsoft 365 Admin Center.  <br/> |
|Aktivierte externe Freigabe von Sway  <br/> |SwayExternalSharingOn  <br/> |Der Administrator aktiviert die externe Sway-Freigabe für die gesamte Organisation mithilfe des Microsoft 365 Admin Center.  <br/> |
|Ausgeschalteter Sway-Dienst  <br/> |SwayServiceOff  <br/> |Der Administrator deaktiviert Sway für die gesamte Organisation mithilfe des Microsoft 365 Admin Center.  <br/> |
|Aktivierter Sway-Dienst  <br/> |SwayServiceOn  <br/> |Der Administrator aktiviert Sway für die gesamte Organisation mithilfe des Microsoft 365 Admin Center (Sway-Dienst ist standardmäßig aktiviert).  <br/> |
|Sway ansehen  <br/> |SwayView  <br/> |Benutzeransichten ein Sway.  <br/> |
||||

  
### <a name="user-administration-activities"></a>Benutzer Verwaltungsaktivitäten
  
In der folgenden Tabelle sind die Benutzer Verwaltungsaktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator ein Benutzerkonto mithilfe des Microsoft 365 Admin Center oder des Azure-Verwaltungsportals hinzufügt oder ändert.
  
|**Aktivität**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Benutzer hinzugefügt  <br/> |Benutzer hinzufügen  <br/> |Ein Office 365 Benutzerkonto wurde erstellt.  <br/> |
|Geänderte Benutzerlizenz  <br/> |Ändern der Benutzerlizenz  <br/> |Die Lizenz, die einem Benutzer zugewiesen wurde, was geändert wurde. Informationen zu den geänderten Lizenzen finden Sie in der entsprechenden **aktualisierten Benutzer** Aktivität.  <br/> |
|Geändertes Benutzerkennwort  <br/> |Benutzerkennwort ändern  <br/> |Der Administrator hat das Kennwort für einen Benutzer geändert.  <br/> |
|Gelöschter Benutzer  <br/> |Benutzer löschen  <br/> |Ein Office 365 Benutzerkonto wurde gelöscht.  <br/> |
|Benutzerkennwort zurücksetzen  <br/> |Benutzerkennwort zurücksetzen  <br/> |Der Administrator hat das Kennwort für einen Benutzer zurückgesetzt.  <br/> |
|Festlegen einer Eigenschaft, die den Benutzer zum Ändern des Kennworts zwingt  <br/> |Erzwingen der Änderung des Benutzerkennworts festlegen  <br/> |Administrator legen Sie die Eigenschaft fest, die es einem Benutzer erzwingt, sein Kennwort zu ändern, wenn sich der Benutzer das nächste Mal bei Office 365 anmeldet.  <br/> |
|Festlegen von Lizenzeigenschaften  <br/> |Festlegen von Lizenzeigenschaften  <br/> |Der Administrator ändert die Eigenschaften einer Lizenz, die einem Benutzer zugewiesen ist.  <br/> |
|Aktualisierter Benutzer  <br/> |Benutzer aktualisieren  <br/> |Administrator ändert eine oder mehrere Eigenschaften eines Benutzerkontos. Eine Liste der Benutzereigenschaften, die aktualisiert werden können, finden Sie im Abschnitt "Aktualisieren von Benutzerattributen" in [Azure Active Directory Überwachungsberichts Ereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Azure Ad Gruppen Verwaltungsaktivitäten
  
In der folgenden Tabelle sind Gruppen Verwaltungsaktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator oder ein Benutzer eine Office 365 Gruppe erstellt oder ändert oder wenn ein Administrator eine Sicherheitsgruppe mithilfe des Microsoft 365 Admin Center oder des Azure-Verwaltungsportals erstellt. Weitere Informationen zu Gruppen in Office 365 finden Sie unter [anzeigen, erstellen und Löschen von Gruppen im Microsoft 365 Admin Center](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Gruppe hinzugefügt  <br/> |Gruppe hinzufügen  <br/> |Eine Gruppe wurde erstellt.  <br/> |
|Mitglied zu Gruppe hinzugefügt  <br/> |Mitglied zur Gruppe hinzufügen  <br/> |Ein Mitglied wurde einer Gruppe hinzugefügt.  <br/> |
|Gelöschte Gruppe  <br/> |Gruppe löschen  <br/> |Eine Gruppe wurde gelöscht.  <br/> |
|Element aus Gruppe entfernt  <br/> |Element aus Gruppe entfernen  <br/> |Ein Mitglied wurde aus einer Gruppe entfernt.  <br/> |
|Aktualisierte Gruppe  <br/> |Gruppe aktualisieren  <br/> |Eine Eigenschaft einer Gruppe wurde geändert.  <br/> |
||||
   
### <a name="application-administration-activities"></a>Anwendungs Verwaltungsaktivitäten
  
In der folgenden Tabelle sind Anwendungsadministrator Aktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator eine Anwendung hinzufügt oder ändert, die in Azure AD registriert ist. Jede Anwendung, die Azure AD für die Authentifizierung verwendet, muss im Verzeichnis registriert sein.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Delegierungs Eintrag hinzugefügt  <br/> |Stellvertretungs Eintrag hinzufügen  <br/> |Eine Authentifizierungs Berechtigung wurde für eine Anwendung in Azure AD erstellt/erteilt.  <br/> |
|Dienstprinzipal hinzugefügt  <br/> |Dienstprinzipal hinzufügen  <br/> |Eine Anwendung wurde in Azure AD registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Anmeldeinformationen zu einem Dienstprinzipal hinzugefügt  <br/> |Hinzufügen von Anmeldeinformationen für Dienst Prinzipale  <br/> |Anmeldeinformationen wurden einem Dienstprinzipal in Azure AD hinzugefügt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Delegierungs Eintrag entfernt  <br/> |Delegierungs Eintrag entfernen  <br/> |In Azure AD wurde eine Authentifizierungs Berechtigung aus einer Anwendung entfernt.  <br/> |
|Dienstprinzipal aus dem Verzeichnis entfernt  <br/> |Dienstprinzipal entfernen  <br/> |Eine Anwendung wurde aus Azure AD gelöscht/aufgehoben. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Anmeldeinformationen aus einem Dienstprinzipal entfernt  <br/> |Entfernen von Anmeldeinformationen für den Dienstprinzipal  <br/> |Anmeldeinformationen wurden in Azure AD aus einem Dienstprinzipal entfernt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Festlegen des Delegierungs Eintrags  <br/> |Festlegen des Delegierungs Eintrags  <br/> |Eine Authentifizierungs Berechtigung wurde für eine Anwendung in Azure AD aktualisiert.  <br/> |
||||

### <a name="role-administration-activities"></a>Aktivitäten für die Rollenverwaltung
  
In der folgenden Tabelle werden Azure AD Rollen Verwaltungsaktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator Administratorrollen im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Mitglied zu Rolle hinzufügen  <br/> |Rollenmitglied zur Rolle hinzufügen  <br/> |Benutzer wurde in Office 365 zu einer Administratorrolle hinzugefügt.  <br/> |
|Entfernen eines Benutzers aus einer Verzeichnis Rolle  <br/> |Rollenelement aus Rolle entfernen  <br/> |Ein Benutzer wurde aus einer Administratorrolle in Office 365 entfernt.  <br/> |
|Unternehmenskontakt Informationen festlegen  <br/> |Unternehmenskontakt Informationen festlegen  <br/> |Die Kontakteinstellungen auf Unternehmensebene für Ihre Office 365 Organisation wurden aktualisiert. Dies umfasst e-Mail-Adressen für von Office 365 gesendete abonnementbezogene e-Mails sowie technische Benachrichtigungen zu Office 365 Diensten.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>Aktivitäten der Verzeichnisverwaltung
  
In der folgenden Tabelle werden Azure AD Verzeichnis-und domänenbezogenen Aktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator seine Office 365 Organisation im Microsoft 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Domäne zu Firma hinzugefügt  <br/> |Domäne zu Firma hinzufügen  <br/> |Domäne zu Ihrer Office 365 Organisation hinzugefügt.  <br/> |
|Partner zum Verzeichnis hinzugefügt  <br/> |Partner zu Firma hinzufügen  <br/> |Partner (Delegierter Administrator) zu Ihrer Office 365 Organisation hinzugefügt.  <br/> |
|Entfernte Domäne aus dem Unternehmen  <br/> |Domäne aus Firma entfernen  <br/> |Eine Domäne wurde aus Ihrer Office 365 Organisation entfernt.  <br/> |
|Partner aus dem Verzeichnis entfernt  <br/> |Partner aus Firma entfernen  <br/> |Partner (Delegierter Administrator) aus Ihrer Office 365 Organisation entfernt.  <br/> |
|Unternehmensinformationen festlegen  <br/> |Unternehmensinformationen festlegen  <br/> |Die Unternehmensinformationen für Ihre Office 365 Organisation wurden aktualisiert. Dies umfasst e-Mail-Adressen für von Office 365 gesendete abonnementbezogene e-Mails sowie technische Benachrichtigungen zu Office 365 Diensten.  <br/> |
|Festlegen der Domänenauthentifizierung  <br/> |Festlegen der Domänenauthentifizierung  <br/> |Die Domänen Authentifizierungseinstellung für Ihre Office 365 Organisation wurde geändert.  <br/> |
|Die Verbund Einstellungen für eine Domäne wurden aktualisiert.  <br/> |Festlegen von Verbund Einstellungen für die Domäne  <br/> |Die Einstellungen für den Verbund (externe Freigabe) für Ihre Office 365 Organisation wurden geändert.  <br/> |
|Festlegen der Kennwortrichtlinie  <br/> |Festlegen der Kennwortrichtlinie  <br/> |Die Längen-und Zeicheneinschränkungen für Benutzerkennwörter in Ihrer Office 365 Organisation wurden geändert.  <br/> |
|Aktivierte Azure AD Synchronisierung  <br/> |DirSyncEnabled-Flag für Unternehmen festlegen  <br/> |Legen Sie die Eigenschaft fest, die ein Verzeichnis für Azure AD Synchronisierung aktiviert.  <br/> |
|Aktualisierte Domäne  <br/> |Domäne aktualisieren  <br/> |Die Einstellungen einer Domäne in Ihrer Office 365 Organisation wurden aktualisiert.  <br/> |
|Verifizierte Domäne  <br/> |Überprüfen der Domäne  <br/> |Überprüft, ob Ihre Organisation der Besitzer einer Domäne ist.  <br/> |
|Verifizierte e-Mail-Domäne überprüft  <br/> |Überprüfen der bestätigten e-Mail-Domäne  <br/> |Verwenden Sie die e-Mail-Überprüfung, um zu überprüfen, ob Ihre Organisation der Besitzer einer Domäne ist.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten
  
Inhaltssuche und eDiscovery-bezogene Aktivitäten, die im Security and Compliance Center oder durch Ausführen der entsprechenden PowerShell-Cmdlets ausgeführt werden, werden im Überwachungsprotokoll protokolliert. Dies umfasst die folgenden Aktivitäten:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, starten und Bearbeiten von Inhalts suchen
    
- Ausführen von Inhalts Suchaktionen wie Vorschau, Export und Löschen von Suchergebnissen
    
- Konfigurieren der Berechtigungs Filterung für die Inhaltssuche
    
- Verwalten der eDiscovery-Administrator Rolle
    
Eine Liste und eine ausführliche Beschreibung der protokollierten eDiscovery-Aktivitäten finden Sie unter [Suchen nach eDiscovery-Aktivitäten im Office 365 Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Es dauert bis zu 30 Minuten für Ereignisse, die sich aus den unter **eDiscovery-Aktivitäten** aufgeführten Aktivitäten in der Dropdownliste **Aktivitäten** ergeben, die in den Suchergebnissen angezeigt werden sollen. Umgekehrt kann es bis zu 24 Stunden dauern, bis die entsprechenden Ereignisse aus eDiscovery-Cmdlet-Aktivitäten in den Suchergebnissen angezeigt werden. 
  
### <a name="advanced-ediscovery-activities"></a>Erweiterte eDiscovery-Aktivitäten

In der folgenden Tabelle sind Aktivitäten aufgeführt, die von IT-Experten und Juristen durchgeführt werden, die Aufgaben in Advanced eDiscovery in Microsoft 365 ausführen. Weitere Informationen finden Sie unter [Übersicht über die erweiterte eDiscovery-Lösung in Microsoft 365](compliance20/overview-ediscovery-20.md).

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
| Hinzufügen von Daten zu einem anderen Überprüfungs Satzes<br/>         | AddWorkingSetQueryToWorkingSet<br/>  |  Benutzer haben Dokumente aus einer Überprüfungsgruppe zu einem anderen Überprüfungs Sätze hinzugefügt.<br/>|
| Hinzugefügte Daten zu Überprüfungs Sätzen <br/>                | AddQueryToWorkingSet<br/>            |  Der Benutzer hat die Suchergebnisse aus einer Inhaltssuche, die einem erweiterten eDiscovery-Fall zugeordnet ist, einem Überprüfungs Satzes hinzugefügt.<br/>|
| Nicht Office 365E Daten zu Überprüfungs Sätzen hinzugefügt.<br/>  | AddNonOffice365DataToWorkingSet<br/> |  Benutzer hat einem Überprüfungs Satzes nicht Office 365 Daten hinzugefügt.<br/>|
| Korrigierte Dokumente zu Überprüfungs Sätzen hinzugefügt<br/> | AddRemediatedData<br/>               |  Benutzer lädt Dokumente mit Indizierungs Fehlern hoch, die an einem Überprüfungs Satz fixiert wurden.<br/>|
| Analysierte Daten in der Überprüfungsgruppe <br/>             | RunAlgo<br/>                         |  Der Benutzer hat Analysen für die Dokumente in einem Überprüfungs Satzes ausgeführt. <br/>|
| Dokument mit Anmerkungen in der Überprüfungsgruppe <br/>        | AnnotateDocument<br/>                |  Ein Benutzer hat ein Dokument in einem Überprüfungs Satzes kommentiert. Annotation enthält einen Text, der in einem Dokument agiert. <br/>|
| Vergleich von Lastsätzen <br/>                      | LoadComparisonJob<br/>               |Der Benutzer hat zwei verschiedene lastgruppen in einem Überprüfungs Satz verglichen. Ein Lastsatz ist, wenn Daten aus einer Inhaltssuche, die dem Fall zugeordnet sind, einem Überprüfungs Satzes hinzugefügt werden.  <br/>|
| Konvertierte behandelte Dokumente in PDF<br/>      | BurnJob<br/>                         |Der Benutzer hat alle in einem Überprüfungs Dokument festgelegten Dokumente in PDF-Dateien konvertiert.<br/>|
| Überprüfungsgruppe erstellt<br/>                       | Createworkingset<br/>                |Der Benutzer hat einen Überprüfungs Sätze erstellt.<br/>|
| Erstellte Überprüfungs Sätze suchen<br/>                | CreateWorkingSetSearch<br/>          |Der Benutzer hat eine Suchabfrage erstellt, die die Dokumente in einem Überprüfungs Sätze durchsucht. <br/>|
| Erstelltes Tag<br/>                              | CreateTag<br/>                       |Benutzer hat eine Tag-Gruppe in einem Überprüfungs Satzes erstellt. Eine Transpondergruppe kann ein oder mehrere untergeordnete Tags enthalten. Diese Tags werden dann zum Markieren von Dokumenten in der Überprüfungsgruppe verwendet.<br/>|
| Suche nach gelöschten Überprüfungs Sätzen <br/>               | DeleteWorkingSetSearch<br/>          |Benutzer hat eine Suchabfrage in einem Überprüfungs Satzes gelöscht.<br/>|
| Gelöschtes Tag<br/>                              | DeleteTag<br/>                       |Ein Benutzer hat ein Tag oder eine Tag-Gruppe in einem Überprüfungs Satzes gelöscht.<br/>|
| Heruntergeladenes Dokument<br/>                      | DownloadDocument<br/>                |Ein Benutzer hat ein Dokument aus einer Überprüfungsgruppe heruntergeladen.<br/>|
| Bearbeitetes Tag <br/>                              | DownloadDocument<br/>                |Der Benutzer hat ein Tag in einem Überprüfungs Satzes geändert.<br/>|
| Exportierte Dokumente aus der Überprüfungsgruppe <br/>      | ExportJob<br/>                       |Benutzer hat Dokumente aus einem Überprüfungs Satzes exportiert.<br/>|
| Geänderte Fall Einstellung <br/>                   | UpdateCaseSettings<br/>              | Der Benutzer hat die Einstellungen für einen Fall geändert. Zu den Fall Einstellungen gehören Fall Informationen, Zugriffsberechtigungen und Einstellungen, mit denen Such-und Analyseverhalten gesteuert werden.<br/>|
| Suche für geänderte Überprüfungs Sätze<br/>               | UpdateWorkingSetSearch<br/>          |  Der Benutzer hat eine Suchabfrage in einem Überprüfungs Satzes bearbeitet.<br/>|
| Vorschau der Überprüfungs Sätze suchen <br/>             | PreviewWorkingSetSearch<br/>         |  Der Benutzer hat eine Vorschau der Ergebnisse einer Suchabfrage in einem Überprüfungs Satzes angezeigt.<br/>|
| Behobene Fehlerdokumente <br/>              | ErrorRemediationJob<br/>             |  Benutzer behebt Dateien, die Indizierungsfehler enthielten. <br/>|
| Markiertes Dokument<br/>                          | TagFiles<br/>                        |  Ein Benutzer Kenn schreibt ein Dokument in einem Überprüfungs Satzes.<br/>|
| Getaggte Ergebnisse einer Abfrage<br/>                | TagJob<br/>                          |  Benutzer Tags alle Dokumente, die den Kriterien der Suchabfrage in einem Überprüfungs Satzes entsprechen.<br/>|
| Angezeigtes Dokument in Überprüfungsgruppe<br/>            | ViewDocument<br/>                    |  Ein Benutzer hat ein Dokument in einem Überprüfungs Satzes angezeigt.<br/>|
|||

### <a name="power-bi-activities"></a>Power BI-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Power BI durchsuchen. Informationen zu Power BI-Aktivitäten finden Sie im Abschnitt "von Power Power BI geprüfte Aktivitäten" unter [Verwenden der Überwachung in Ihrer Organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
Beachten Sie, dass die Überwachungsprotokollierung für Power BI standardmäßig nicht aktiviert ist. Um im Office 365 Überwachungsprotokoll nach Power BI-Aktivitäten zu suchen, müssen Sie die Überwachung im Power BI-Verwaltungsportal aktivieren. Anweisungen finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI-Verwaltungsportal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
  
### <a name="microsoft-workplace-analytics-activities"></a>Microsoft Workplace Analytics-Aktivitäten

Die Arbeitsplatzanalyse bietet Einblicke in die Zusammenarbeit von Gruppen in Ihrer Office 365 Organisation. In der folgenden Tabelle sind die Aktivitäten aufgeführt, die von Benutzern ausgeführt werden, denen die Rolle "Administrator" oder "Analyst Roles in Workplace Analytics" zugewiesen ist. Benutzer, denen die Analysten Rolle zugewiesen ist, haben Vollzugriff auf alle Dienstfunktionen und verwenden das Produkt für die Analyse. Benutzer, denen die Administrator Rolle zugewiesen ist, können Datenschutzeinstellungen und Systemstandards konfigurieren und Organisationsdaten in der Arbeitsplatzanalyse vorbereiten, hochladen und überprüfen. Weitere Informationen finden Sie unter [Workplace Analytics](https://docs.microsoft.com/en-us/workplace-analytics/index-orig).

|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Zugriff auf OData-Link <br/> |AccessedOdataLink <br/> |Analyst hat auf den OData-Link für eine Abfrage zugegriffen.|
|Abgebrochene Abfrage <br/> |CanceledQuery <br/> |Analyst hat eine laufende Abfrage abgebrochen.|
|Erstellter Besprechungs Ausschluss <br/> |MeetingExclusionCreated <br/> |Analyst hat eine neue Besprechungs Ausschlussregel erstellt.|
|Gelöschtes Ergebnis <br/> |DeletedResult <br/> |Analyst hat ein Abfrageergebnis gelöscht.|
|Heruntergeladener Bericht <br/> |DownloadedReport <br/> |Analyst hat eine Abfrageergebnis Datei heruntergeladen.|
|Ausgeführte Abfrage <br/> |ExecutedQuery <br/> |Analyst hat eine Abfrage ausgeführt.|
|Aktualisierte Datenzugriffs Einstellung <br/> |UpdatedDataAccessSetting <br/> |Administrator aktualisierte Datenzugriffs Einstellungen.|
|Aktualisierte Datenschutzeinstellung <br/> |UpdatedPrivacySetting <br/> |Administrator aktualisierte Datenschutzeinstellungen; Beispiel: minimale Gruppengröße.|
|Hochgeladene Organisationsdaten <br/> |UploadedOrgData <br/> |Administrator hochgeladene Organisationsdaten Datei.|
|Explore anzeigen <br/> |ViewedExplore <br/> |Von Analysten betrachtete Visualisierungen in einem oder mehreren Registerkarten für Durchsuchen von Seiten.|
||||

### <a name="microsoft-teams-activities"></a>Microsoft Teams-Aktivitäten
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in Microsoft Teams aufgeführt, die im Office 365 Überwachungsprotokoll protokolliert werden. Microsoft Teams ist ein Chat zentrierter Arbeitsbereich in Office 365. Es bringt die Unterhaltungen, Besprechungen, Dateien und Notizen eines Teams an einem zentralen Ort zusammen. Weitere Informationen und Links zu Hilfethemen finden Sie unter:
  
- [Häufig gestellte Fragen zu Microsoft Teams – Administratorhilfe](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Hilfe zu Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Bot zum Team hinzugefügt  <br/> |BotAddedToTeam  <br/> |Ein Benutzer fügt einem Team einen bot hinzu.  <br/> |
|Kanal hinzugefügt  <br/> |ChannelAdded  <br/> |Ein Benutzer fügt einem Team einen Kanal hinzu.  <br/> |
|Connector hinzugefügt  <br/> |ConnectorAdded  <br/> |Ein Benutzer fügt einem Kanal einen Verbinder hinzu.  <br/> |
|Mitglieder zu Team hinzugefügt  <br/> |MemberAdded  <br/> |Ein Teambesitzer fügt einem Teammitglied (en) hinzu.  <br/> |
|Registerkarte hinzugefügt  <br/> |TabAdded  <br/> |Ein Benutzer fügt einem Kanal eine Registerkarte hinzu.  <br/> |
|Geänderte Kanaleinstellung  <br/> |ChannelSettingChanged  <br/> | Der ChannelSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem Teammitglied ausgeführt werden. Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (unten in Klammern dargestellt) in der Spalte **Element** in den Überwachungsprotokoll-Suchergebnissen angezeigt.  <br/> <br/>– Ändert den Namen eines Team Kanals ( **Kanal Name**).  <br/>  <br/>– Ändert die Beschreibung eines Team Kanals ( **Kanalbeschreibung**).  <br/> |
|Geänderte Organisations Einstellung  <br/> |TeamsTenantSettingChanged  <br/> | Der TeamsTenantSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem globalen Administrator ausgeführt werden (mithilfe des Microsoft 365 admin Centers); Beachten Sie, dass diese Aktivitäten sich auf organisationsweite Microsoft Teams-Einstellungen auswirken. Weitere Informationen finden Sie unter [Administrator Einstellungen für Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).  <br/>  Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (unten in Klammern dargestellt) in der Spalte **Element** in den Überwachungsprotokoll-Suchergebnissen angezeigt.  <br/><br/>– Aktiviert oder deaktiviert Microsoft Teams für die Organisation ( **Microsoft Teams**).  <br/><br/>– Aktiviert oder deaktiviert die Interoperabilität zwischen Microsoft Teams und Skype for Business für die Organisation ( **Skype for Business Interoperabilität**).<br/><br/>– Aktiviert oder deaktiviert die Ansicht Organisationsdiagramm in Microsoft Teams-Clients (Organigramm- **Ansicht**).  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, private Besprechungen ( **private Besprechungsplanung**) zu planen.  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Kanal Besprechungen ( **Kanal Konferenzplanung**) zu planen.  <br/><br/>– Aktiviert oder deaktiviert Videoanrufe in Microsoft Teams-Besprechungen ( **Video für Skype**-Besprechungen).  <br/><br/>– Aktiviert oder deaktiviert die Bildschirmfreigabe in Microsoft Teams-Meetups für die Organisation ( **Bildschirmfreigabe für Skype**-Besprechungen).  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit, animierte Bilder ("Giphys") zu Microsoft Teams-Unterhaltungen ( **animierte Bilder**) hinzuzufügen.  <br/><br/>– Ändert die Einstellung für die Inhaltsbewertung für die Organisation ( **Inhaltsbewertung**). Die Inhaltsbewertung schränkt den Typ des animierten Bilds ein, das in Unterhaltungen angezeigt werden kann.  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, anpassbare Bilder (so genannte benutzerdefinierte Meme) aus dem Internet zu Team Unterhaltungen ( **anpassbare Bilder aus dem Internet**) hinzuzufügen.  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, bearbeitbare Bilder (als Aufkleber bezeichnet) zu Team Unterhaltungen ( **bearbeitbare Bilder**) hinzuzufügen.<br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Bots in Microsoft Teams-Chats und-Kanälen ( **org-Wide Bots**) zu verwenden.<br/><br/>-Aktiviert spezifische Bots für Microsoft Teams; Dies beinhaltet nicht den t-bot, der Microsoft Teams-Hilfe bot, der verfügbar ist, wenn Bots für die Organisation aktiviert sind ( **einzelne Bots**).  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Erweiterungen oder Registerkarten ( **Erweiterungen oder Registerkarten**) hinzuzufügen.  <br/><br/>– Aktiviert oder deaktiviert das Seiten Laden von proprietären Bots für Microsoft Teams ( **Seiten Laden von Bots**).  <br/><br/>– Aktiviert oder deaktiviert die Möglichkeit für Benutzer, e-Mail-Nachrichten an einen Microsoft Teams-Kanal ( **Kanal-e-Mail**) zu senden.  <br/> |
|Geänderte Rolle von Mitgliedern im Team  <br/> |MemberRoleChanged  <br/> |Ein Teambesitzer ändert die Rolle von Mitgliedern in einem Team. Die folgenden Werte geben den Rollentyp an, der dem Benutzer zugewiesen ist.  <br/><br/><br/> **1** – gibt die Besitzerrolle an.<br/>**2** – gibt die Mitglieder Rolle an. <br/>**3** – gibt die Gast Rolle an. <br/>Die Members-Eigenschaft enthält auch den Namen Ihrer Organisation und die e-Mail-Adresse des Mitglieds.  <br/> |
|Geänderte Team Einstellung  <br/> |TeamSettingChanged  <br/> | Der TeamSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem Teambesitzer ausgeführt werden. Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (unten in Klammern dargestellt) in der Spalte **Element** in den Überwachungsprotokoll-Suchergebnissen angezeigt.  <br/><br/>– Ändert den Zugriffstyp für ein Team. Teams können als private oder Public ( **Team Zugriffstyp**) festgelegt werden. Wenn ein Team privat ist (Standardeinstellung), können Benutzer nur per Einladung auf das Team zugreifen. Wenn ein Team öffentlich ist, kann es von jedem Benutzer erkannt werden.  <br/><br/>– Ändert die Informationsklassifizierung eines Teams ( **Team Klassifizierung**).  <br/>  Beispielsweise können Team Daten als hohe geschäftliche Auswirkung, mittlere geschäftliche Auswirkungen oder geringe geschäftliche Auswirkungen klassifiziert werden.<br/><br/>– Ändert den Namen eines Teams ( **Teamname**).  <br/><br/>– Ändert die Team Beschreibung ( **Team Beschreibung**). <br/><br/>– Änderungen, die an den Team Einstellungen vorgenommen wurden. Ein Teambesitzer kann auf diese Einstellungen in einem Teams-Client zugreifen, indem er mit der rechten Maustaste auf ein Team klickt, auf **Team verwalten**klickt und dann auf die Registerkarte **Einstellungen** klickt. Für diese Aktivitäten wird der Name der geänderten Einstellung in der Spalte **Element** in den Überwachungsprotokoll-Suchergebnissen angezeigt.  <br/> |
|Erstelltes Team  <br/> |TeamCreated  <br/> |Ein Benutzer erstellt ein neues Team.  <br/> |
|Gelöschter Kanal  <br/> |ChannelDeleted  <br/> |Ein Benutzer löscht einen Kanal aus einem Team.  <br/> |
|Gelöschtes Team  <br/> |TeamDeleted  <br/> |Ein Teambesitzer löscht ein Team.  <br/> |
|Bot aus dem Team entfernt  <br/> |BotRemovedFromTeam  <br/> |Ein Benutzer entfernt einen bot aus einem Team.  <br/> |
|Connector entfernt  <br/> |ConnectorRemoved  <br/> |Ein Benutzer entfernt den Connector aus einem Kanal.  <br/> |
|Mitglieder aus Team entfernt  <br/> |MemberRemoved  <br/> |Ein Teambesitzer entfernt Mitglieder aus einem Team.  <br/> |
|Registerkarte entfernt  <br/> |TabRemoved  <br/> |Ein Benutzer entfernt eine Registerkarte aus einem Kanal.  <br/> |
|Aktualisierter Connector  <br/> |ConnectorUpdated  <br/> |Ein Benutzer hat einen Konnektor in einem Kanal geändert.  <br/> |
|Aktualisierte Registerkarte  <br/> |TabUpdated  <br/> |Ein Benutzer hat eine Registerkarte in einem Kanal geändert.  <br/> |
|Benutzer, der sich bei Teams angemeldet hat  <br/> |TeamsSessionStarted  <br/> |Ein Benutzer meldet sich bei einem Microsoft Teams-Client an.  <br/> |
||||

### <a name="yammer-activities"></a>Jammern von Aktivitäten
  
In der folgenden Tabelle werden die Benutzer-und Administratoraktivitäten in "jammern" aufgelistet, die im Office 365 Überwachungsprotokoll protokolliert werden. Wenn Sie Aktivitäten im Zusammenhang mit jammern aus dem Office 365-Überwachungsprotokoll zurückgeben möchten, müssen Sie die Option **Ergebnisse für alle Aktivitäten** in der Liste **Aktivitäten** anzeigen auswählen. Verwenden Sie die Datumsbereichsfelder und die **Benutzer** Liste, um die Suchergebnisse einzuschränken. 
  
|**Anzeigename**|**Vorgang**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Datenaufbewahrungsrichtlinie  <br/> |SoftDeleteSettingsUpdated  <br/> |Der verifizierte Administrator aktualisiert die Einstellung für die Netzwerkdaten Aufbewahrungsrichtlinie entweder auf Hard Delete oder auf Soft Delete. Dieser Vorgang kann nur von überprüften Administratoren ausgeführt werden.  <br/> |
|Geänderte Netzwerkkonfiguration  <br/> |NetworkConfigurationUpdated  <br/> |Netzwerk oder überprüfter Administrator ändert die Konfiguration des Jammer Netzwerks. Dies umfasst das Festlegen des Intervalls für das Exportieren von Daten und das Aktivieren von Chat.  <br/> |
|Geänderte Netzwerkprofil Einstellungen  <br/> |ProcessProfileFields  <br/> |Netzwerk oder überprüfter Administrator ändert die Informationen, die in den Mitglieds Profilen für Netzwerkbenutzer Netzwerk angezeigt werden.  <br/> |
|Geänderter privater Inhalts Modus  <br/> |SupervisorAdminToggled  <br/> |Der verifizierte Administrator aktiviert oder deaktiviert den *privaten Inhalts Modus* . In diesem Modus können Administratoren Beiträge in privaten Gruppen anzeigen und private Nachrichten zwischen einzelnen Benutzern (oder Gruppen von Benutzern) anzeigen. Nur verifizierte Administratoren können diesen Vorgang nur ausführen.  <br/> |
|Geänderte Sicherheitskonfiguration  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Der verifizierte Administrator aktualisiert die Sicherheitskonfiguration des Jammer Netzwerks. Dies umfasst das Festlegen von Richtlinien für Kennwortablauf und Einschränkungen für IP-Adressen. Dieser Vorgang kann nur von überprüften Administratoren ausgeführt werden.  <br/> |
|Erstellte Datei  <br/> |Filecreated  <br/> |Der Benutzer lädt eine Datei hoch.  <br/> |
|Erstellte Gruppe  <br/> |GroupCreation  <br/> |Der Benutzer erstellt eine neue Gruppe.  <br/> |
|Gelöschte Gruppe  <br/> |GroupDeletion  <br/> |Eine Gruppe wird aus jammern gelöscht.  <br/> |
|Gelöschte Nachricht  <br/> |MessageDeleted  <br/> |Der Benutzer löscht eine Nachricht.  <br/> |
|Heruntergeladene Datei  <br/> |FileDownloaded  <br/> |Der Benutzer lädt eine Datei herunter.  <br/> |
|Exportierte Daten  <br/> |DataExport  <br/> |Überprüft Administrator exportiert jammern von Netzwerkdaten. Dieser Vorgang kann nur von überprüften Administratoren ausgeführt werden.  <br/> |
|Freigegebene Datei  <br/> |Filesharing  <br/> |Der Benutzer teilt eine Datei mit einem anderen Benutzer.  <br/> |
|Unterbrochener Netzwerkbenutzer  <br/> |NetworkUserSuspended  <br/> |"Netzwerk" oder "Verifizierter Administrator" hält einen Benutzer von "jammern" suspendiert (deaktiviert).  <br/> |
|Angeh ALTENER Benutzer  <br/> |UserSuspension  <br/> |Das Benutzerkonto ist angehalten (deaktiviert).  <br/> |
|Aktualisierte Dateibeschreibung  <br/> |FileUpdateDescription  <br/> |Der Benutzer ändert die Beschreibung einer Datei.  <br/> |
|Name der aktualisierten Datei  <br/> |Fileupdatename  <br/> |Der Benutzer ändert den Namen einer Datei.  <br/> |
|Betrachtete Datei  <br/> |Filevisited  <br/> |Der Benutzer sieht eine Datei an.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Microsoft Flow-Aktivitäten

Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Flow durchsuchen. Diese Aktivitäten umfassen das Erstellen, bearbeiten und Löschen von Flows sowie das Ändern von Fluss Berechtigungen. Informationen zur Überwachung von Fluss Aktivitäten finden Sie im Blog [Microsoft Flow Audit-Ereignisse jetzt verfügbar in Security #a0 Compliance Center](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Sie können das Überwachungsprotokoll für App-bezogene Aktivitäten in PowerApps durchsuchen. Diese Aktivitäten umfassen das Erstellen, starten und Veröffentlichen einer App. Das Zuweisen von Berechtigungen zu apps wird ebenfalls überwacht. Eine Beschreibung aller PowerApps-Aktivitäten finden Sie unter [Aktivitätsprotokollierung für PowerApps](https://docs.microsoft.com/en-us/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Microsoft Stream-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Stream durchsuchen. Zu diesen Aktivitäten gehören Video Aktivitäten, die von Benutzern durchgeführt werden, Gruppenkanal Aktivitäten und Administratoraktivitäten wie das Verwalten von Benutzern, das Verwalten von Organisationseinstellungen und das Exportieren von Berichten. Eine Beschreibung dieser Aktivitäten finden Sie im Abschnitt "protokollierte Aktivitäten in Microsoft Stream" in [Überwachungsprotokollen in Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Exchange-Administrator-Überwachungsprotokoll
  
Exchange Administrator-Überwachungsprotokollierung – die standardmäßig in Office 365 aktiviert ist – protokolliert ein Ereignis im Office 365 Überwachungsprotokoll, wenn ein Administrator (oder ein Benutzer, dem Administratorrechte zugewiesen wurden) eine Änderung in Ihrer Exchange Online Organisation vornimmt. Änderungen, die mithilfe des Exchange Admin Center oder durch Ausführen eines Cmdlets in Windows PowerShell vorgenommen werden, werden im Exchange-administratorüberwachungsprotokoll protokolliert. Ausführlichere Informationen zur Administrator-Überwachungsprotokollierung in Exchange finden Sie unter [Administrator-Überwachungsprotokollierung](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Hier finden Sie einige Tipps für die Suche nach Aktivitäten im Exchange Admin-Überwachungsprotokoll:
  
- Wenn Sie Einträge aus dem Exchange Admin-Überwachungsprotokoll zurückgeben möchten, müssen Sie die Option **Ergebnisse für alle Aktivitäten** in der Liste **Aktivitäten** anzeigen auswählen. Verwenden Sie die Datumsbereichsfelder und die **Benutzer** Liste, um die Suchergebnisse für Cmdlets einzuschränken, die von einem bestimmten Exchange-Administrator innerhalb eines bestimmten Datumsbereichs ausgeführt werden. 
    
- Wenn Sie Ereignisse aus dem Exchange-administratorüberwachungsprotokoll anzeigen möchten, Filtern Sie die Such **-** Ergebnisse, und geben Sie im Feld **Aktivitäts** Filter einen (Bindestrich) ein. Dadurch werden Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Verwaltungsereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortieren. 
    
    ![Geben Sie im feldaktivitäten einen Bindestrich ein, um Exchange-Administrator Ereignisse zu filtern.](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Wenn Sie Informationen dazu erhalten möchten, welches Cmdlet ausgeführt wurde, welche Parameter und Parameterwerte verwendet wurden und welche Objekte betroffen sind, müssen Sie die Suchergebnisse exportieren und die Option **alle Ergebnisse herunterladen** auswählen. 
    
- Sie können auch Ereignisse im Exchange Admin-Überwachungsprotokoll anzeigen, indem Sie das Exchange Admin Center verwenden. Anweisungen finden Sie unter [View the Administrator Audit Log](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wo finde ich die Features, die der Überwachungsdienst in Office 365 bietet?**

Weitere Informationen zu den in Office 365 verfügbaren Überwachungs-und Berichtsfunktionen finden Sie unter [Auditing and Reporting in Office 365](office-365-auditing-and-reporting-overview.md). 

**Was sind unterschiedliche Office 365 Dienste, die derzeit überwacht werden?**

Die am häufigsten verwendeten Office 365 Dienste wie Exchange Online, SharePoint Online, OneDrive für Unternehmen, Azure Active Directory, Microsoft Teams, Dynamics 365, Advanced Threat Protection und Power BI werden überwacht. Unter dem [Anfang dieses Artikels](search-the-audit-log-in-security-and-compliance.md) finden Sie eine Liste der überwachten Dienste.

**Welche Aktivitäten werden vom Überwachungsdienst in Office 365 überwacht?**

Eine Liste und eine Beschreibung der Aktivitäten, die in Office 365 überwacht werden, finden Sie im Abschnitt über [wachte Aktivitäten](#audited-activities) in diesem Artikel.

**Wie lange dauert es, bis ein Überwachungsdatensatz verfügbar ist, nachdem ein Ereignis aufgetreten ist?**

Die meisten Überwachungsdaten sind innerhalb von 30 Minuten verfügbar, es kann jedoch bis zu 24 Stunden dauern, bis ein Ereignis eintritt, damit der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. Sehen Sie sich die Tabelle im Abschnitt [bevor Sie beginnen](#before-you-begin) dieses Artikels an, in dem die Zeit angezeigt wird, die für die Verfügbarkeit von Ereignissen in den verschiedenen Office 365 Diensten benötigt wird.

**Wie lange werden die Überwachungsdatensätze aufbewahrt?**

Wie bereits erläutert, hängt der Aufbewahrungszeitraum für Überwachungseinträge vom Office 365 Abonnement Ihrer Organisation ab.  

- **Office 365 E3** -Überwachungseinträge werden für 90 Tage aufbewahrt.

- **Office 365 E5** -Überwachungseinträge werden auch für 90 Tage aufbewahrt. Das Aufbewahren von Überwachungsdatensätzen für ein Jahr ist möglicherweise für E5-Benutzer und-Benutzer mit einer E3-Lizenz und einer Add-on-Lizenz für Office 365 Advanced Compliance verfügbar.

     > [!NOTE]
     > Wie bereits erläutert, ist das private Vorschau Programm für die einjährige Aufbewahrungszeit für Überwachungsdatensätze für E5-Organisationen (oder E3-Organisationen mit erweiterten Compliance-Add-on-Lizenzen) für die neue Registrierung geschlossen. Dieser Artikel wird aktualisiert, wenn der Aufbewahrungszeitraum für ein Jahr in der öffentlichen Vorschau verfügbar oder für allgemeine Verfügbarkeit freigegeben ist.

Beachten Sie außerdem, dass die Dauer des Aufbewahrungszeitraums für Überwachungsdatensätze auf der pro-Benutzer-Lizenzierung basiert. Wenn beispielsweise einem Benutzer in Ihrer Organisation eine Office 365 E3-oder E5-Lizenz zugewiesen ist, werden die Überwachungseinträge für von diesem Benutzer ausgeführte Aktivitäten für 90 Tage aufbewahrt.

**Kann ich die Überwachungsdaten programmgesteuert aufrufen?**

Ja. Die Office 365 Verwaltungs Aktivitäts-API wird zum programmgesteuerten Abrufen der Überwachungsprotokolle verwendet.  Die ersten Schritte finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Gibt es andere Möglichkeiten zum Abrufen von Überwachungsprotokollen als die Verwendung des Security and Compliance Centers oder der API für die Office 365-Verwaltungsaktivität?**

Nein. Dies sind die einzigen beiden Methoden zum Abrufen von Daten aus dem Office 365-Überwachungsdienst. 

**Muss die Überwachung in jedem Dienst, für den Überwachungsprotokolle erfasst werden sollen, einzeln aktiviert werden?**

In den meisten Office 365 Diensten ist die Überwachung standardmäßig aktiviert, nachdem Sie zunächst die Überwachung für Ihre Office 365 Organisation aktiviert haben (wie im Abschnitt [bevor Sie beginnen](#before-you-begin) in diesem Artikel beschrieben). Sie müssen jedoch die postfachüberwachung in Exchange Online für jedes Postfach aktivieren, das Sie überwachen möchten.   Wir arbeiten daran, die postfachüberwachung standardmäßig für alle Postfächer in einer Office 365 Organisation zu aktivieren. Weitere Informationen finden Sie unter „Exchange-Postfachüberwachung wird standardmäßig aktiviert“ im [Microsoft-Blog für Sicherheit, Datenschutz und Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171).

**Unterstützt der Office 365 Überwachungsdienst die Deduplizierung von Datensätzen?**

Nein. Die Überwachungsdienst Pipeline ist nahezu in Echtzeit und kann daher keine Deduplizierung unterstützen.
 
**Fließt Office 365-Überwachungsdaten in Geographien?**

Nein. Derzeit gibt es Überwachungs Pipeline Bereitstellungen in den Regionen na (Nordamerika), EMEA (Europa, Mittlerer Osten und Afrika) und APAC (asiatisch-Pazifik). Es kann jedoch vorkommen, dass die Daten in diesen Regionen für den Lastenausgleich und nur bei Problemen mit der Live-Website fließen. Wenn wir diese Aktivitäten ausführen, werden die Daten in der Übertragung verschlüsselt.   
 
**Werden Überwachungsdaten verschlüsselt?**

Überwachungsdaten werden in Exchange-Postfächern (Daten im Ruhezustand) in derselben Region gespeichert, in der die Überwachungs Pipeline bereitgestellt wird. Diese Daten werden nicht verschlüsselt. Daten während der Übertragung werden jedoch immer verschlüsselt. 

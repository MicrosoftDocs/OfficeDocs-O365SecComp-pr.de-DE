---
title: Durchsuchen des Überwachungsprotokolls im Office 365 Security &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Verwenden Sie die Office 365-Sicherheit und Compliance Center, um das unified Überwachungsprotokoll zum Anzeigen von Benutzer- und Administrator-Aktivität in Office 365-Organisation zu suchen. '
ms.openlocfilehash: 39b3d6438d4680fe7a50f831bbd2d5667c4acffe
ms.sourcegitcommit: a138cf89095ab0d2bd07caf82b3d48149002c1fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2018
ms.locfileid: "26626151"
---
# <a name="search-the-audit-log-in-the-office-365-security--compliance-center"></a>Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit und Compliance Center

Erforderlich, um zu ermitteln, ob ein Benutzer ein bestimmtes Dokument angezeigt oder ein Element aus dem Postfach gelöscht? Wenn also die Sicherheit der Office 365 verwendbare &amp; Compliance Center, um das unified Überwachungsprotokoll zum Anzeigen von Benutzer- und Administrator-Aktivität in Office 365-Organisation durchsuchen. Warum einer einheitlichen Audit protokolliert? Da Sie für die folgenden Typen von Benutzer- und Admin Aktivität in Office 365 suchen können:
  
- Benutzeraktivität in SharePoint Online und OneDrive für Unternehmen
    
- Benutzeraktivität in Exchange Online (Exchange-Postfach postfachüberwachungsprotokollierung)
    
    > [!IMPORTANT]
    > Mailbox Audit Logging muss aktiviert werden für jedes Benutzerpostfach bevor Benutzeraktivität in Exchange Online protokolliert werden. Weitere Informationen finden Sie unter [Aktivieren der Überwachung in Office 365 Postfach](enable-mailbox-auditing.md).
  
- Admin-Aktivität in SharePoint Online
    
- Admin-Aktivität in Azure Active Directory (Verzeichnisdienst für Office 365)
    
- Admin-Aktivität in Exchange Online (Exchange Admin postfachüberwachungsprotokollierung)
    
- Benutzer- und Admin-Aktivität im Schlingern
    
- eDiscovery-Aktivitäten im Compliance Center & Sicherheit in Office 365
    
- Benutzer- und Admin Aktivität in Power BI
    
- Benutzer- und Admin-Aktivität in Microsoft-Teams

- Benutzer- und Admin Aktivität in Dynamics 365
    
- Benutzer- und Admin Aktivität in Yammer
 
- Benutzer- und Admin-Aktivität in Microsoft Flow
    
- Benutzer- und Admin-Aktivität in Microsoft Stream
    
   
## <a name="before-you-begin"></a>Bevor Sie beginnen:

Stellen Sie sicher, dass die folgenden Elemente, bevor Sie beginnen, suchen die Office 365 in das Überwachungsprotokoll lesen.
  
- Sie (oder ein anderes Admin) muss zunächst auf die Protokollierung, bevor Sie beginnen können, suchen das Office 365-Überwachungsprotokoll aktivieren. Um sie zu aktivieren, klicken Sie einfach auf **die Benutzer- und Admin Aktivität Aufzeichnung starten** auf der Seite **Audit Log Suche** in das Wertpapier &amp; Compliance Center. (Wenn Sie diese Verknüpfung nicht angezeigt wird, wurde die Überwachung bereits für Ihre Organisation aktiviert.) Nachdem Sie es aktivieren, wird eine Meldung angezeigt, die besagt, das Überwachungsprotokoll vorbereitet wird und dass Sie eine Suche, in ein paar Stunden ausführen können nach Abschluss die Vorbereitung. Sie müssen nur einmal erforderlich. 
    
    > [!NOTE]
    > Wir sind während der Aktivierung der Überwachung in der Standardeinstellung. Bis zu diesem Zeitpunkt können Sie es aktivieren wie weiter oben beschrieben. 
  
- Sie müssen die Rolle des Kontaktobjekts überwachen Protokolle oder Protokolle überwachen im Exchange Online um das Office 365-Überwachungsprotokoll durchsuchen zugewiesen werden. Standardmäßig werden die Verwaltung der Richtlinientreue und Organization Management Rollengruppen auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole dieser Rollen zugewiesen. Wenn einem Benutzer die Möglichkeit, die das Überwachungsprotokoll Office 365 mit der Mindestmaß an Privilegien durchsuchen übergeben möchten, können Sie erstellen eine benutzerdefinierte Rollengruppe in Exchange Online, Kontaktobjekts überwachen Protokolle oder Protokolle überwachen-Rolle hinzufügen, und fügen Sie den Benutzer als Mitglied der neuen Rollengruppe. Weitere Informationen finden Sie unter [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Wenn Sie einem Benutzer die Rolle Kontaktobjekts überwachen Protokolle oder Protokolle überwachen auf der Seite **Berechtigungen** in das Wertpapier zuweisen &amp; Compliance Center, sie nicht möglich, das Office 365-Überwachungsprotokoll durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuzuweisen. Dies ist, da das zugrunde liegende-Cmdlet verwendet, um das Überwachungsprotokoll durchsuchen Exchange Online-Cmdlet ist. 
  
- Wenn eine überwachte Aktivität durch einen Benutzer oder Administrator ausgeführt wird, ein Audit-Datensatz erstellt und im Überwachungsprotokoll Office 365 für Ihre Organisation gespeichert. Die Zeitdauer, die ein Datensatz Audit aufbewahrt werden (und in das Überwachungsprotokoll durchsuchbar) ist, hängt davon ab Ihres Office 365-Abonnements und ausdrücklich den Typ der Lizenz, die das einen bestimmten Benutzer zugeordnet ist.

     - **Office 365 E3** - Audit Datensätze 90 Tage lang aufbewahrt werden. Dies bedeutet, dass Sie das Überwachungsprotokoll Aktivitäten suchen können, die innerhalb der letzten 90 Tage durchgeführt wurden.

     - **Office 365 E5** - Audit 365 Tage (ein Jahr) Datensätze aufbewahrt werden. Dies bedeutet, dass Sie das Überwachungsprotokoll Aktivitäten suchen können, die innerhalb des letzten Jahres ausgeführt wurden. Aufbewahren von Audit-Datensätze für ein Jahr ist auch für Benutzer, die eine E3/Exchange Online – Plan 1-Lizenz zugewiesen sind, und haben eine zusätzliche Lizenz für Office 365 erweiterte Compliance verfügbar.

        > [!NOTE]
        > Die einjährige Aufbewahrungsdauer für Audit-Datensätze für E5 (oder E3 Organisationen, die erweiterte Compliance Add-on Lizenzen haben) ist derzeit nur als Teil eines Programms private Preview. In diesem Vorschauprogramm zu registrieren, um Bitte Datei eine Anforderung mit [Microsoft-Support](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) und als Beschreibung der Sie Hilfe benötigen, sind: "Langfristige Office 365 Audit Log private Preview".

- Wenn Sie die Audit Log-Suche in Office 365 für Ihre Organisation zu deaktivieren möchten, können Sie den folgenden Befehl in remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Um Audit Suche erneut aktivieren, können Sie in Exchange Online PowerShell den folgenden Befehl ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Weitere Informationen finden Sie unter [Audit Log Suche in Office 365 deaktivieren](turn-audit-log-search-on-or-off.md).
    
- Wie bereits zuvor erwähnt ist das zugrunde liegende-Cmdlet verwendet, um das Überwachungsprotokoll Durchsuchen einer Exchange Online-Cmdlet **Search-UnifiedAuditLog**. Verwenden Sie dieses Cmdlet, um das Office 365-Überwachungsprotokoll statt der Seite **Protokoll Such-** in das Wertpapier durchsuchen bedeutet &amp; Compliance Center. Sie müssen zum Ausführen dieses Cmdlet in remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden ist. Weitere Informationen finden Sie unter [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Wenn Sie Daten aus dem Office 365-Überwachungsprotokoll programmgesteuert herunterladen möchten, sollten Sie die Office 365-Verwaltungs-Aktivität API statt eines PowerShell-Skripts verwenden. Die Office 365-Verwaltungs-Aktivität-API ist eine REST-Webdienst, den Sie zum Entwickeln von Operationen, Sicherheit und Compliance-monitoring-Lösungen für Ihre Organisation verwenden können. Weitere Informationen finden Sie unter [Office 365 Management Aktivität-API-Referenz](https://go.microsoft.com/fwlink/?linkid=852309).
    
- Es kann bis zu 30 Minuten dauern oder von 24 Stunden nach Ereignis tritt ein, die der entsprechenden Überwachungsprotokolleintrag in den Suchergebnissen angezeigt werden. Die folgende Tabelle zeigt den Zeitaufwand für die verschiedenen Dienste in Office 365.
    
    |**Office 365-Dienste**|**30 Minuten**|**24 Stunden**|
    |:-----|:-----|:-----|
    |Erweiterte Schutz und Bedrohungsanalyse  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (Benutzer Anmeldung Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (Admin Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |Azure Active Directory (Benutzer Anmeldung Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Verhinderung von Datenverlust  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Dynamics 365 CRM <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |eDiscovery  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Forms  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Teams  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Security &amp; Compliance Center  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |SharePoint Online und OneDrive for Business  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Yammer  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (AD Azure) ist der Verzeichnisdienst für Office 365. Unified Überwachungsprotokoll enthält Benutzer, Gruppe, Anwendung, Domäne und Directory Aktivitäten ausgeführt in Office 365 Administrationscenter oder in der in Azure-Verwaltungsportal. Eine vollständige Liste der Azure AD-Ereignisse finden Sie unter [Azure Active Directory Bericht Überwachungsereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Exchange Online Überwachungsprotokolle bestehen aus zwei Arten von Ereignissen: Exchange Admin-Ereignisse (von Administratoren ausgeführten Aktionen) und Postfach-Ereignisse (von Benutzern für Postfächer ausgeführte Aktionen). Beachten Sie, dass die Überwachung von Postfächern in der Standardeinstellung nicht aktiviert ist. Es muss für jedes Benutzerpostfach aktivieren, bevor der Postfach-Ereignisse im Überwachungsprotokoll Office 365 für durchsucht werden können. Weitere Informationen zur Überwachung von Postfächern und die postfachüberwachung für Aktionen, die angemeldet sind, finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](enable-mailbox-auditing.md).
    
- Überwachungsprotokollierung für Power BI ist nicht standardmäßig aktiviert. Zum Suchen von Power BI-Aktivitäten im Überwachungsprotokoll Office 365 müssen Sie zum Aktivieren der Überwachung in Power BI-Admin-Portal. Eine Anleitung finden Sie im Abschnitt "Überwachungsprotokolle" [Power BI](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)-Verwaltungsportal.
    
    
## <a name="search-the-audit-log"></a>Durchsuchen des Überwachungsprotokolls

Hier ist der Prozess für die Suche im Überwachungsprotokolls in Office 365.
  
[Schritt 1: Führen Sie eine Audit Log-Suche](#step-1-run-an-audit-log-search)
  
[Schritt 2: Anzeigen der Suchergebnisse](#step-2-view-the-search-results)

[Schritt 3: Filtern von Suchergebnissen](#step-3-filter-the-search-results)

[Schritt 4: Exportieren Sie die Suchergebnisse in eine Datei.](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Schritt 1: Führen Sie eine Audit Log-Suche

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Verwenden eine private Browsersitzung (nicht regulären Sitzung) greifen Sie auf die Office 365-Sicherheit &amp; Compliance Center, da dies die Anmeldeinformationen verhindert wird, die Sie derzeit mit angemeldet sind verwendet werden. Um eine Sitzung InPrivate-Browsen in Internet Explorer oder Microsoft Edge zu öffnen, drücken Sie STRG + UMSCHALT + P. Um eine private Browsersitzung Google Chrome (als ein incognito Fenster bezeichnet) zu öffnen, drücken Sie STRG + UMSCHALT + N. 
  
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung**, und klicken Sie auf **Audit Log suchen**.
    
    **Audit Log** Suchseite wird angezeigt. 
    
    ![Konfigurieren von Kriterien, und klicken Sie dann auf Suchen, um den Bericht ausführen](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Sie müssen überwachungsprotokollierung vor dem Ausführen einer Audit Log-Suche zum ersten Mal einschalten. Wenn die Verknüpfung **Benutzer- und Admin Aktivität Aufzeichnung starten** angezeigt wird, klicken Sie auf, um die Überwachung einzuschalten. Wenn Sie diese Verknüpfung nicht angezeigt wird, wurde die Überwachung bereits für Ihre Organisation aktiviert. 
  
4. Konfigurieren Sie die folgenden Suchkriterien:
    
    a. **Aktivitäten** klicken Sie auf die Dropdown-Liste die Aktivitäten angezeigt werden sollen, denen Sie für suchen können. Benutzer- und Admin Aktivitäten sind an eine Gruppe von Aktivitäten in organisiert. Sie können bestimmte Aktivitäten auswählen, oder Sie können den Gruppennamen Aktivität alle Aktivitäten in der Gruppe auswählen auf. Klicken Sie auf einen ausgewählten Aktivität zum Aufheben der Auswahl. Nachdem Sie die Suche ausführen werden nur die Überwachungsprotokolleinträge für den ausgewählten Aktivitäten angezeigt. **Ergebnisse für alle Aktivitäten anzeigen** auswählen zeigt die Ergebnisse für alle Aktivitäten, die von den ausgewählten Benutzer oder die Gruppe von Benutzern durchgeführt. 
    
    Mehr als 100 Benutzer und Admin Aktivitäten werden im Überwachungsprotokoll Office 365 protokolliert. Klicken Sie auf der Registerkarte **Löschvorgänge Aktivitäten** im Thema dieses Artikels finden in den Beschreibungen jeder Aktivität in jeder der verschiedenen Office 365-Dienste. 
    
    b. **Startdatum** und **Enddatum** den letzten sieben Tagen sind standardmäßig aktiviert. Wählen Sie einen Bereich für Datum und Uhrzeit der Ereignisse angezeigt, die innerhalb dieses Zeitraums aufgetreten sind. Datum und Uhrzeit werden in koordinierter Weltzeit (UTC) Format angezeigt. Der maximale Zeitraum, den Sie angeben können, ist 90 Tage. Ein Fehler wird angezeigt, wenn des ausgewählten Datumsbereichs älter als 90 Tage ist. 
    
    > [!TIP]
    > Wenn Sie den maximale Datumsbereich der 90 Tage verwenden, wählen Sie die aktuelle Zeit für das **Startdatum**an. Andernfalls erhalten Sie eine Fehlermeldung ausgegeben, die das Startdatum einer älteren Version als das Enddatum ist. Wenn Sie innerhalb der letzten 90 Tage Überwachung aktiviert haben, kann nicht der maximalen Zeitraum vor dem Datum gestartet, die Überwachung aktiviert wurde. 
  
    c-Ergebnis für **Benutzer** klicken Sie in dieses Feld ein und wählen Sie einen oder mehrere Benutzer, um die Suche angezeigt werden. Die Überwachungsprotokolleinträge für die ausgewählten Aktivitäten, die von den Benutzern, die Sie in dieses Feld auswählen, werden in der Liste der Ergebnisse angezeigt. Lassen Sie dieses Feld leer, Zurückgeben von Einträgen für alle Benutzer (und Dienstkonten) in Ihrer Organisation. 
    
    d. **File- oder Folder** Geben Sie einige oder alle ein File- oder Folder Name für die Suche nach Aktivitäten im Zusammenhang mit der Datei des Ordners, der das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Enthalten Sie Wenn Sie eine URL verwenden, sicherzustellen, dass der Typ der vollständige URL-Pfad sein oder wenn Sie nur einen Teil der URL eingeben nicht keine Sonderzeichen oder Leerzeichen. 
    
    Lassen Sie dieses Feld leer, Zurückgeben von Einträgen für alle Dateien und Ordner in Ihrer Organisation.
    
5. Klicken Sie auf **Suche** zum Ausführen der Suche mit den Suchkriterien. 
    
    Die Suchergebnisse werden geladen, und nach einigen Augenblicken sie unter **Ergebnisse**angezeigt werden. Wenn die Suche abgeschlossen ist, wird die Anzahl der gefundenen Ergebnisse angezeigt. Beachten Sie, dass maximal 5.000 Ereignisse in Schritten von 150 Ereignisse im **Ergebnisbereich** angezeigt wird. Wenn mehr als 5.000 Ereignisse den Suchkriterien entsprechen, werden die neuesten 5.000 Ereignisse angezeigt. 
    
    ![Die Anzahl der Ergebnisse werden angezeigt, nachdem die Suche abgeschlossen ist](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Tipps für die Suche im Überwachungsprotokolls

- Sie können bestimmte Aktivitäten zu suchenden, indem Sie auf den Namen der Aktivität auswählen. Oder Sie können für alle Aktivitäten in einer Gruppe (beispielsweise **Datei- und Aktivitäten**), indem Sie auf den Namen der Gruppe suchen. Wenn eine Aktivität ausgewählt ist, können Sie darauf, um die Auswahl Abbrechen klicken. Das Suchfeld können auch die Aktivitäten anzuzeigen, die das Schlüsselwort enthalten, das Sie eingeben.
    
    ![Klicken Sie auf Aktivität Gruppennamen, wählen Sie alle Aktivitäten](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Sie müssen **Ergebnisse für alle Aktivitäten anzeigen** wählen Sie in der Liste **Aktivitäten** Ereignisse aus dem Exchange Admin-Überwachungsprotokoll angezeigt. Ereignisse aus dieser Überwachungsprotokoll einen Cmdlet-Namen (beispielsweise " **Set-Mailbox** ") in der **Aktivität** -Spalte in den Ergebnissen angezeigt. Weitere Informationen klicken Sie auf der Registerkarte **Aktivitäten Löschvorgänge** in diesem Thema aus, und klicken Sie dann auf **Exchange-Admin-Aktivitäten**.
    
    In ähnlicher Weise werden einige auditing Aktivitäten, die nicht über ein entsprechendes Element in der Liste **Aktivitäten** verfügen. Wenn Sie den Namen des Vorgangs für das Rollout kennen, können Sie für alle Aktivitäten zu suchen und dann die Ergebnisse filtern, indem Sie im Feld für die **Aktivität** Spalte den Namen des Vorgangs eingeben. Finden Sie unter [Schritt 3: Filtern von Suchergebnissen](#step-3-filter-the-search-results) Weitere Informationen zum Filtern der Ergebnisse. 
    
- Klicken Sie auf **Deaktivieren** , um die aktuellen Suchkriterien zu löschen. Der Datumsbereich gibt den letzten sieben Tagen wird der Standardwert zurück. Sie können auch **alle zum Anzeigen der Ergebnisse für alle Aktivitäten löschen** , um alle ausgewählten Aktivitäten Abbrechen klicken. 
    
- Wenn 5000 Ergebnisse gefunden werden, können Sie wahrscheinlich davon ausgehen, dass es sind mehr als 5.000 Ereignisse, die die Suchkriterien erfüllen. Können Sie die Suchkriterien verfeinern und führen Sie die Suche zum Zurückgeben von Ergebnissen aus weniger erneut aus, oder alle der Suchergebnisse zu exportieren, indem Sie die **Ergebnisse exportieren** auswählen \> **alle Ergebnisse herunterladen**.

  
### <a name="step-2-view-the-search-results"></a>Schritt 2: Anzeigen der Suchergebnisse

Die Ergebnisse einer Audit Log Suche werden auf der Seite **Protokoll Such-** unter **Ergebnisse** angezeigt. Wie bereits erwähnt, maximal 5.000 (neu) Ereignisse in Schritten von 150 Ereignisse angezeigt werden. Zum Anzeigen von mehr Ereignisse können Sie im **Ergebnisbereich** die Bildlaufleiste oder drücken Sie **UMSCHALT + Ende** der nächsten 150 Ereignisse angezeigt. 
  
Die Ergebnisse enthalten die folgende Informationen zu jedem Ereignis, das von der Suche zurückgegebenen.
  
- **Datum:** Datum und Uhrzeit (in UTC-Format), die das Ereignis auftrat. 
    
- **IP-Adresse:** Die IP-Adresse des Geräts, das verwendet wurde, wenn die Aktivität protokolliert wurde. Die IP-Adresse wird in ein IPv4 oder IPv6-Adressformat angezeigt. 
    
- **Benutzer:** Der Benutzer (oder ein Dienstkonto), die die Aktion, die das Ereignis ausgelöst hat ausgeführt. 
    
- **Aktivität:** Die Aktivitäten des Benutzers. Dieser Wert entspricht der Aktivitäten, die Sie in der Dropdownliste **Aktivitäten** ausgewählt haben. Für ein Ereignis aus dem Exchange Admin-Überwachungsprotokoll ist der Wert in dieser Spalte ein Exchange-Cmdlet. 
    
- **Element:** Das Objekt, das erstellt oder als Ergebnis der entsprechenden Aktivität geändert wurde. Die Datei, die angezeigt oder geändert wurde oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben einen Wert in dieser Spalte. 
    
- **Detail:** Weitere Informationen zur Aktivität. In diesem Fall müssen nicht alle Aktivitäten einen Wert. 
    
> [!TIP]
> Klicken Sie auf eine Spaltenüberschrift unter **Ergebnisse** zum Sortieren der Ergebnisse. Sie können die Ergebnisse von A bis Z oder Z sortieren, um A. Klicken Sie auf der **Date** -Header zum Sortieren der Ergebnisse vom ältesten zu neuesten oder Absteigend. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Zeigen Sie die Details für ein bestimmtes Ereignis

Sie können weitere Details zu einem Ereignis anzeigen, indem Sie auf der Ereignisprotokolleintrag in der Liste der Suchergebnisse. Eine Seite **Details** angezeigt, die die detaillierten Eigenschaften aus dem Ereignisdatensatz enthält. Die Eigenschaften, die angezeigt werden, abhängig von der Office 365-Dienst, in dem das Ereignis tritt auf, ab. Um diese Details anzuzeigen, klicken Sie auf **Weitere Informationen**. Beschreibungen finden Sie unter [Detailangaben zu den Eigenschaften in der Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
![Klicken Sie auf Weitere Informationen zum Anzeigen der detaillierten Eigenschaften des Datensatzes Audit log](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern von Suchergebnissen

Zusätzlich zum Sortieren, können Sie auch die Ergebnisse einer Audit Log Suche filtern. Dies ist ein hervorragendes Feature, mit denen Sie die Ergebnisse für einen bestimmten Benutzer oder eine Aktivität schnell filtern kann. Sie können zunächst eine Breite Suche erstellen und dann schnell Filtern der Ergebnisse, um bestimmte Ereignisse finden Sie unter. Klicken Sie dann können Sie die Suchkriterien eingrenzen und führen Sie die Suche zum Zurückgeben von einer kleineren, kürzeren Gruppe von Ergebnissen erneut aus.
  
Um die Ergebnisse zu filtern:
  
1. Führen Sie eine Audit Log-Suche.
    
2. Wenn die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse filtern**.
    
    Schlüsselwort-Felder werden unter jeder Spaltenüberschrift angezeigt.
    
3. Klicken Sie auf eines der Felder unter eine Spaltenüberschrift, und geben Sie ein Wort oder Ausdruck, je nach der Spalte, der Sie filtern möchten. Die Ergebnisse werden dynamisch textlichen, um die Ereignisse anzuzeigen, die den Filter entsprechen.
    
    ![Geben Sie ein Wort im angegebenen Ereignisse angezeigt, die dem Filter entsprechen](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Um einen Filter zu löschen, klicken Sie auf das **X** im Filterfeld, oder klicken Sie einfach auf **Filtern ausblenden**.
    
> [!TIP]
> Geben Sie zum Anzeigen von Ereignissen aus dem Exchange Admin-Überwachungsprotokoll ein **-** (Strich) im Filterfeld **Aktivität** . Dadurch wird die Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange Admin-Ereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortiert werden. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Schritt 4: Exportieren Sie die Suchergebnisse in eine Datei.

Sie können die Ergebnisse einer Audit Log-Suche in einer durch Trennzeichen getrennten Werten (CSV)-Datei auf Ihrem lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und verwenden Features wie beispielsweise die Suche, sortieren, Filtern und Aufteilen einer einzelnen Spalteninhalts (die Zellen mit mehreren Werte enthält) in mehreren Spalten.
  
1. Führen Sie eine Audit Log-Suche, und Überarbeiten Sie die Suchkriterien, bis Sie die gewünschten Ergebnisse haben.
    
2. Klicken Sie auf **Ergebnisse exportieren** , und wählen Sie eine der folgenden Optionen aus: 
    
  - **Geladenen Ergebnisse speichern** Wählen Sie diese Option, um nur die Einträge zu exportieren, der unter **Ergebnisse** angezeigt werden, auf die ** Audit Log Suche ** Seite. Die CSV-Datei, die heruntergeladen wird enthält dieselben Spalten (und Daten) angezeigt, auf der Seite (Datum, Benutzer, Aktivität, Artikel und Details). Eine weitere Spalte ( **Weitere**Namens) ist in der CSV-Datei enthalten, die Informationen aus dem Überwachungseintrag Protokoll enthält. Da Sie die gleichen Ergebnisse exportieren, die geladen (und angezeigt werden können) sind auf der Seite **Audit Log Suche** maximal 5.000 Einträge werden exportiert. 
    
  - **Laden Sie alle Ergebnisse** Wählen Sie diese Option, um alle Einträge aus dem Office 365-Überwachungsprotokoll, die die Suchkriterien erfüllen exportieren. Wählen Sie für eine große Gruppe von Suchergebnissen diese Option, um alle Einträge aus dem Überwachungsprotokoll zusätzlich zu den 5000 Ergebnisse herunterladen, die auf der Seite **Protokoll Such-** angezeigt werden kann. Diese Option wird die Rohdaten in eine CSV-Datei aus dem Überwachungsprotokoll herunterladen und enthält zusätzliche Informationen aus dem Überwachungseintrag melden Sie sich in einer Spalte mit dem Namen **AuditData**. Länger kann dauern, die Datei herunterzuladen, wenn Sie diese Exportoption auswählen, da die Datei wesentlich größer als der sein kann, die heruntergeladen wird, wenn Sie die Option andere ausgewählt.
    
    > [!IMPORTANT]
    > Sie können maximal 50.000 Einträge aus einer einzigen Audit Log-Suche in einer CSV-Datei herunterladen. Wenn 50.000 Einträge in der CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass es sind mehr als 50.000 Ereignisse, die die Suchkriterien erfüllen. Wenn mehr als diese Grenze exportieren möchten, verwenden Sie einen Datumsbereich zur Reduzierung der Anzahl von Überwachungsprotokolleinträgen. Möglicherweise müssen Sie mehrere Suchvorgänge mit kleineren Datumsbereiche für mehr als 50.000 Einträge exportieren durchgeführt werden. 
  
3. Nachdem Sie eine Exportoption ausgewählt haben, wird eine Meldung am unteren Rand des Fensters angezeigt, die aufgefordert, öffnen Sie die CSV-Datei, speichern Sie die Downloads-Ordner oder in einen bestimmten Ordner zu speichern.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>Weitere Informationen zum Exportieren von Audit Log-Suchergebnisse

- Die Option **alle Ergebnisse laden** lädt die Rohdaten aus der Office 365-Überwachungsprotokoll in eine CSV-Datei. Diese Datei enthält verschiedene Spaltennamen (CreationDate, Benutzer-IDs, Vorgang, AuditData) als die Datei, die heruntergeladen wird, wenn Sie die Option **Speichern geladenen Ergebnisse** auswählen. Die Werte in zwei verschiedenen CSV-Dateien für die gleiche Aktivität können auch anders lauten. Beispielsweise die Aktivität in der Spalte **Aktion** in der CSV-Datei und weist möglicherweise einen anderen Wert als die "benutzerfreundlichen" Version, die in der Spalte **Aktivität** auf der Seite **Audit Log Suche** ; angezeigt wird Beispielsweise können Sie MailboxLogin im Vergleich zu Benutzer in Postfach angemeldet.
    
- Wenn Sie alle Ergebnisse herunterladen, enthält die CSV-Datei eine Spalte mit dem Namen **AuditData**, die zusätzliche Informationen zu jedem Ereignis enthält. Wie bereits erwähnt enthält diese Spalte eine mehrwertige Eigenschaft für mehrere Eigenschaften aus dem Audit Log Datensatz. Jede **Eigenschaft-Wert** -Paare im dieses mehrwertige Eigenschaften werden durch ein Komma getrennt. Sie können die Power-Abfrage in Excel verwenden, mehrere Spalten in dieser Spalte aufgeteilt werden, damit jede Eigenschaft eine eigenen Spalte verwendet werden. Dadurch können Sie sortieren und Filtern für ein oder mehrere dieser Eigenschaften. Finden Sie Informationen hierzu finden Sie im Abschnitt "Teilen einer Spalte durch Trennzeichen" Split [Text (Power Query) in einer Spalte](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662).
    
    Nachdem Sie die Spalte **AuditData** geteilt, können Sie in der Spalte **Vorgänge** zum Anzeigen der detaillierten Eigenschaften für einen bestimmten Objekttyp Aktivität filtern. 
    
- Es besteht ein 3,060 Zeichen-Grenzwert für die Daten, die im Feld **AuditData** für einen Audit-Eintrag angezeigt wird. Die 3,060-Zeichen überschritten wird, werden die Daten in diesem Feld abgeschnitten. 
    
- Wenn Sie alle Ergebnisse aus einer Suchabfrage, die Ereignisse aus verschiedenen Office 365-Dienste enthält herunterladen, enthält die **AuditData** -Spalte in der CSV-Datei verschiedene Eigenschaften, je nachdem, denen was in Service die Aktion ausgeführt wurde. Beispielsweise enthalten Einträge aus Exchange und Azure AD Überwachungsprotokolle eine Eigenschaft mit dem Namen **ResultStatus** , die angibt, ob die Aktion erfolgreich war. Diese Eigenschaft ist nicht mit inbegriffen für Ereignisse in SharePoint. In ähnlicher Weise SharePoint-Ereignisse haben eine Eigenschaft identifiziert die Website URL für Dateien und Ordner-bezogene Aktivitäten. Um dieses Verhalten zu verringern, sollten Sie in Betracht ziehen, unterschiedliche Suchen durchführen So exportieren Sie die Ergebnisse für Aktivitäten aus einem einzelnen Dienst zu verwenden. 
    
    Eine Beschreibung der Eigenschaften, die in der Spalte **AuditData** in der CSV-Datei aufgelistet sind, wenn Sie alle Ergebnisse und den Dienst jedes Herunterladen einer betrifft, finden Sie unter [Detailangaben zu den Eigenschaften in der Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Überwachten Aktivitäten

Die Tabellen in diesem Abschnitt beschreiben die Aktivitäten, die in Office 365 überwacht werden. Sie können für diese Ereignisse durch Suchen der Überwachungsprotokolle in das Wertpapier protokollieren suchen &amp; Compliance Center. Klicken Sie auf die Registerkarte **Suchen im Überwachungsprotokoll** für eine schrittweise Anleitung. 
  
Diese Tabellen Gruppieren verwandter Aktivitäten oder die Aktivitäten aus einem bestimmten Office 365-Dienst. Die Tabellen enthalten den Anzeigenamen, der in der Dropdown-Liste von **Aktivitäten** angezeigt wird und den Namen der entsprechenden Vorgang, der angezeigt wird, in die detaillierten Informationen eines Datensatzes Audit und in der CSV-Datei, wenn Sie die Suchergebnisse exportieren. Beschreibung der ausführliche Informationen finden Sie unter [Detailangaben zu den Eigenschaften in der Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
Klicken Sie auf eine der folgenden Links, um zu einer bestimmten Tabelle zu wechseln.
  
||||
|:-----|:-----|:-----|
|[Datei und Seite Aktivitäten](#file-and-page-activities)<br/> |[Ordner Aktivitäten](#folder-activities)<br/> |[Freigabe und Access Anforderung Aktivitäten](#sharing-and-access-request-activities)<br/> |
|[Synchronisierung Aktivitäten](#synchronization-activities)<br/> |[Site-Verwaltungsaktivitäten](#site-administration-activities)<br/> |[Exchange-Postfach-Aktivitäten](#exchange-mailbox-activities)<br/> |
|[Sway Aktivitäten](#sway-activities) <br/> |[Die Verwaltung Benutzeraktivitäten](#user-administration-activities) <br/> |[Azure Active Directory-Gruppe Administration Aktivitäten](#azure-ad-group-administration-activities) <br/> |
|[Anwendung Administration Aktivitäten](#application-administration-activities) <br/> |[Rolle Administration Aktivitäten](#role-administration-activities) <br/> |[Directory Administration Aktivitäten](#directory-administration-activities) <br/> |
|[eDiscovery-Aktivitäten](#ediscovery-activities) <br/> |[Power BI-Aktivitäten](#power-bi-activities) <br/> |[Microsoft-Teams, Aktivitäten](#microsoft-teams-activities) <br/> |
|[Yammer-Aktivitäten](#yammer-activities) <br/> |[Microsoft Flow](#microsoft-flow) <br/> |[Microsoft Stream](#microsoft-stream) <br/>|
|[Exchange-Administrator-Überwachungsprotokoll](#exchange-admin-audit-log) <br/> |
   
  
### <a name="file-and-page-activities"></a>Datei und Seite Aktivitäten
  
In der folgenden Tabelle werden die Datei und Seite Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Geöffneten Datei  <br/> |FileAccessed  <br/> |Benutzer- oder Systemkonto greift auf eine Datei.  <br/> |
|(kein Rahmen)  <br/> |FileAccessedExtended  <br/> |Dies bezieht sich auf die Datei"Zugriff" Aktivität (FileAccessed). Wenn die gleiche Person ständig eine Datei für einen längeren Zeitraum (bis zu 3 Stunden) zugreift, wird ein FileAccessedExtended-Ereignis protokolliert. Protokollieren von Ereignissen FileAccessedExtended dient zum Verringern der Anzahl FileAccessed Ereignisse, die protokolliert werden, wenn eine Datei ständig zugegriffen wird. Dies hilft bei der Rauschen von mehrere FileAccessed-Datensätzen für was im Wesentlichen ist Benutzeraktivität und Sie sich auf das erste (und wichtiger) FileAccessed Ereignis konzentrieren können.  <br/> |
|Datei eingecheckt  <br/> |FileCheckedIn  <br/> |Benutzerprüfungen in einem Dokument, das sie aus einer Dokumentbibliothek ausgecheckt.  <br/> |
|Datei ausgecheckt  <br/> |FileCheckedOut  <br/> |Benutzer checkt ein Dokument befindet sich in einer Dokumentbibliothek aus. Benutzer können Auschecken und vornehmen von Änderungen an Dokumenten, die mit diesen freigegeben wurden.  <br/> |
|Kopierte Datei  <br/> |FileCopied  <br/> |Benutzer kopiert ein Dokument aus einer Website. Die kopierte Datei kann in einen anderen Ordner auf der Website gespeichert werden.  <br/> |
|Gelöschte Datei  <br/> |FileDeleted  <br/> |Benutzer löscht ein Dokument aus einer Website.  <br/> |
|Gelöschte Datei aus dem Papierkorb  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Benutzer löscht eine Datei aus dem Papierkorb einer Website.  <br/> |
|Gelöschte Datei aus dem endgültigen Papierkorb  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Benutzer löscht eine Datei aus dem endgültigen Papierkorb einer Website.  <br/> |
|Erkannte Schadsoftware in Datei  <br/> |FileMalwareDetected  <br/> |SharePoint-Antivirus-Modul erkennt schädlichen Code in einer Datei.  <br/> |
|Verworfene Auscheckvorgang  <br/> |FileCheckOutDiscarded  <br/> |Benutzer verwirft eine ausgecheckte Datei, oder macht dies rückgängig. Alle Änderungen, die an der Datei vorgenommen wurden, als sie ausgecheckt war, werden verworfen und nicht in der Dokumentversion in der Dokumentbibliothek gespeichert.  <br/> |
|Heruntergeladene Datei  <br/> |FileDownloaded  <br/> |Benutzer lädt ein Dokument aus einer Website.  <br/> |
|Geänderte Datei  <br/> |FileModified  <br/> |Benutzer oder Systemkonto ändert den Inhalt oder die Eigenschaften eines Dokuments auf einer Website befindet.  <br/> |
|(kein Rahmen)  <br/> |FileModifiedExtended  <br/> |Dies bezieht sich auf die Datei"Modified" Aktivität (FileModified). Ein Ereignis FileModifiedExtended wird protokolliert, wenn die gleiche Person ständig eine Datei für einen längeren Zeitraum (bis zu 3 Stunden) ändert. Protokollieren von Ereignissen FileModifiedExtended dient zum Verringern der Anzahl FileModified Ereignisse, die protokolliert werden, wenn eine Datei ständig geändert wird. Dies hilft bei der Rauschen von mehrere FileModified-Datensätzen für was im Wesentlichen ist Benutzeraktivität und Sie sich auf das erste (und wichtiger) FileModified Ereignis konzentrieren können.  <br/> |
|Verschobene Datei  <br/> |FileMoved  <br/> |Benutzer verschoben ein Dokument von seinem aktuellen Speicherort auf einer Website an einen neuen Speicherort.  <br/> |
|Alle Nebenversionen der Datei im Papierkorb  <br/> |FileVersionsAllMinorsRecycled  <br/> |Benutzer löscht alle Nebenversionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Alle Versionen der Datei im Papierkorb  <br/> |FileVersionsAllRecycled  <br/> |Benutzer löscht alle Versionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Wiederverwendeten Version der Datei  <br/> |FileVersionRecycled  <br/> |Benutzer löscht eine Version aus dem Versionsverlauf einer Datei. Die gelöschte Version wird in den Papierkorb der Website verschoben.  <br/> |
|Umbenannte Datei  <br/> |FileRenamed  <br/> |Ein Dokument auf einer Website umbenannt wird.  <br/> |
|Wiederhergestellten Datei  <br/> |FileRestored  <br/> |Benutzer wiederherstellen ein Dokuments aus dem Papierkorb einer Website.  <br/> |
|Hochgeladene Datei  <br/> |FileUploaded  <br/> |Benutzer hochgeladen ein Dokument in einen Ordner auf einer Website.  <br/> |
|Angezeigte Seite  <br/> |PageViewed  <br/> |Benutzer zeigt eine Seite auf einer Website. Dies umfasst nicht mit einem Webbrowser anzeigen von Dateien in einer Dokumentbibliothek befinden.  <br/> |
|(kein Rahmen)  <br/> |PageViewedExtended  <br/> |Dies bezieht sich auf der Seite"Ansicht" Aktivitäten (PageViewed). Ein PageViewedExtended-Ereignis wird protokolliert, wenn die gleiche Person ständig eine Webseite für einen längeren Zeitraum (bis zu 3 Stunden) anzeigt. Protokollieren von Ereignissen PageViewedExtended dient zum Verringern der Anzahl PageViewed Ereignisse, die protokolliert werden, wenn eine Seite ständig angezeigt wird. Dies hilft bei der Rauschen von mehrere PageViewed-Datensätzen für was im Wesentlichen ist Benutzeraktivität und Sie sich auf das erste (und wichtiger) PageViewed Ereignis konzentrieren können.  <br/> |
  
### <a name="folder-activities"></a>Ordner Aktivitäten
  
In der folgenden Tabelle werden die Ordner Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Kopierte Ordner  <br/> |FolderCopied  <br/> |Benutzer kopiert einen Ordner aus einer Website in eine andere Position in SharePoint oder OneDrive für Unternehmen.  <br/> |
|Erstellte Ordner  <br/> |FolderCreated  <br/> |Benutzer erstellt einen Ordner auf einer Website.  <br/> |
|Gelöschte Ordner  <br/> |FolderDeleted  <br/> |Benutzer löscht einen Ordner aus einer Website.  <br/> |
|Gelöschte Ordner aus dem Papierkorb  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Benutzer löscht einen Ordner aus dem Papierkorb auf einer Website.  <br/> |
|Gelöschte Ordner aus im endgültigen Papierkorb  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Benutzer löscht einen Ordner aus dem endgültigen Papierkorb auf einer Website.  <br/> |
|Geänderte Ordner  <br/> |FolderModified  <br/> |Benutzer ändert einen Ordner auf einer Website. Dazu gehört das Ändern der Ordnermetadaten, wie Kategorien und Eigenschaften ändern.  <br/> |
|Verschobene Ordner  <br/> |FolderMoved  <br/> |Benutzer Verschiebt einen Ordner an einen anderen Ort auf einer Website.  <br/> |
|Umbenannte Ordner  <br/> |FolderRenamed  <br/> |Einen Ordner auf einer Website umbenannt wird.  <br/> |
|Wiederhergestellte Ordner  <br/> |FolderRestored  <br/> |Benutzer wiederherstellen ein gelöschtes Ordners aus dem Papierkorb auf einer Website.  <br/> |
  
### <a name="sharing-and-access-request-activities"></a>Freigabe und Access Anforderung Aktivitäten
  
In der folgenden Tabelle werden die Benutzer Freigabe und Access Anforderung Aktivitäten in SharePoint Online und OneDrive für Unternehmen beschrieben. Für die Freigabe von Ereignissen, die Spalte **Details** unter **Ergebnisse** identifiziert den Namen des Benutzers oder der Gruppe, die für das Element freigegeben wurde, und gibt an, ob Benutzer oder die Gruppe ist ein Element oder Gast in Ihrer Organisation. Weitere Informationen finden Sie unter [Überwachung in das Überwachungsprotokoll Office 365 Freigabe verwenden](use-sharing-auditing.md).
  
> [!NOTE]
> Benutzer können *Mitglieder* oder *Gäste* auf Basis der UserType-Eigenschaft des User-Objekts sein. Ein Element wird in der Regel ein Mitarbeiter und Gast ist in der Regel ein Collaborator außerhalb Ihrer Organisation. Wenn ein Benutzer eine Einladung zur Freigabe akzeptiert (und noch nicht Teil der Organisation), wird im Verzeichnis Ihrer Organisation ein Gastkonto erstellt. Sobald der Gastbenutzer ein Konto in Ihrem Verzeichnis verfügt, können Ressourcen (ohne eine Einladung) direkt mit freigegeben werden. 
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Access-Anforderung akzeptiert  <br/> |AccessRequestAccepted  <br/> |Eine Access-Anforderung an eine Website, Ordner oder Dokument wurde angenommen und der anfordernde Benutzer Zugriff gewährt wurde.  <br/> |
|Akzeptiert eine freigabeeinladung  <br/> |SharingInvitationAccepted  <br/> |Benutzer (Mitglied oder Gast) akzeptiert eine Einladung zur Freigabe, und Zugriff auf eine Ressource erteilt wurde. Dieses Ereignis enthält Informationen zu den Benutzer, die eingeladen wurde und die e-Mail-Adresse, die verwendet wurde, um die Einladung anzunehmen (sie können unterschiedliche sein). Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, die beschreibt, wie der Benutzer erteilt wurde Zugriff auf die Ressource hinzufügen des Benutzers zu einer Gruppe, die Zugriff auf die Ressource hat.  <br/> |
|Hinzugefügte Berechtigungsstufe für Websitesammlung  <br/> |PermissionLevelAdded  <br/> |Eine Berechtigungsstufe wurde in eine Websitesammlung hinzugefügt.  <br/> |
|Benutzer, die sichere Verbindung  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die diese Freigabe sichere Verbindung verwenden können.  <br/> |
|Einladung zur Freigabe blockiert  <br/> |SharingInvitationBlocked  <br/> | Eine Einladung zur Freigabe von einem Benutzer in Ihrer Organisation gesendet wird aufgrund eines externen Freigaberichtlinie blockiert, die erteilt oder verweigert externe Freigabe auf Basis der Domäne des Zielbenutzers. In diesem Fall wurde die Einladung zur Freigabe, da blockiert:<br/>  Domäne des Zielbenutzers ist nicht in der Liste der zugelassenen Domänen enthalten.  <br/>  Oder  <br/>  Domäne des Zielbenutzers ist in der Liste der blockierten Domänen enthalten.  <br/>  Weitere Informationen zum Zulassen oder Sperren externe Freigabe basierend auf Domänen finden Sie unter [eingeschränkten Freigabe in SharePoint Online und OneDrive für Unternehmen Domänen](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Eingestellt wurde Ebene Vererbung von Berechtigungen  <br/> |PermissionLevelsInheritanceBroken  <br/> |Ein Element wurde geändert, sodass es nicht mehr Berechtigungsstufen von der übergeordneten Website erbt.  <br/> |
|Freigeben von Vererbung eingestellt wurde  <br/> |SharingInheritanceBroken  <br/> |Ein Element wurde geändert, sodass es nicht mehr Freigabeberechtigungen von der übergeordneten Website erbt.  <br/> |
|Erstellung eines Unternehmens freigebbare links  <br/> |CompanyLinkCreated  <br/> |Der Benutzer erstellt einen unternehmensweite Link zu einer Ressource. unternehmensweite Links kann nur von Mitgliedern in Ihrer Organisation verwendet werden. Sie können nicht von Gästen verwendet werden.  <br/> |
|Access-Anforderung erstellt  <br/> |AccessRequestCreated  <br/> |Benutzer fordert den Zugriff auf eine Website, Ordner, oder sie nicht über Berechtigungen zum Zugriff auf verfügen.  <br/> |
|Erstellt einen anonymen link  <br/> |AnonymousLinkCreated  <br/> |Der Benutzer erstellt einen anonymen Link zu einer Ressource. Jeder Benutzer mit diesen Link kann die Ressource zugreifen, ohne authentifiziert werden.  <br/> |
|Sichere Verbindung erstellt  <br/> |SecureLinkCreated  <br/> |Auf dieses Element wurde als sichere Verbindung für die Freigabe erstellt.  <br/> |
|Einladung zur Freigabe erstellt  <br/> |SharingInvitationCreated  <br/> |Benutzer freigegebene Ressource in SharePoint Online oder OneDrive für Unternehmen mit einem Benutzer, die nicht im Verzeichnis Ihrer Organisation befindet.  <br/> |
|Gelöschte sichere Verbindung  <br/> |SecureLinkDeleted  <br/> |Eine sichere Freigabe Verknüpfung wurde gelöscht.  <br/> |
|Access-Anforderung abgelehnt  <br/> |AccessRequestDenied  <br/> |Eine Access-Anforderung an eine Website, Ordner oder Dokument wurde verweigert.  <br/> |
|Geänderte Berechtigungsstufe in der Websitesammlung  <br/> |PermissionLevelModified  <br/> |Eine Berechtigungsstufe wurde für eine Websitesammlung geändert.  <br/> |
|Entfernt einen Unternehmen freigebbare link  <br/> |CompanyLinkRemoved  <br/> |Benutzer entfernt einen unternehmensweite Link zu einer Ressource. Die Verknüpfung kann nicht mehr verwendet werden, Zugriff auf die Ressource.  <br/> |
|Entfernt einen anonymen link  <br/> |AnonymousLinkRemoved  <br/> |Benutzer entfernt einen anonymen Link zu einer Ressource. Die Verknüpfung kann nicht mehr verwendet werden, Zugriff auf die Ressource.  <br/> |
|Berechtigungsstufe aus der Websitesammlung entfernt  <br/> |PermissionLevelRemoved  <br/> |Eine Berechtigungsstufe wurde aus der Websitesammlung entfernt.  <br/> |
|Freigeben von Vererbung wiederhergestellt  <br/> |SharingInheritanceReset  <br/> |Es wurde eine Änderung vorgenommen, so, dass ein Element Freigabeberechtigungen von der übergeordneten Website erbt.  <br/> |
|Freigegebene Datei, Ordner oder site  <br/> |SharingSet  <br/> |Benutzer (Mitglied oder Gast) freigegebene Dateien, Ordner oder einer Website in SharePoint oder OneDrive für Unternehmen mit einem Benutzer in das Verzeichnis der Organisation. Der Wert in der Spalte **Details** für diese Aktivität gibt den Namen des Benutzers, den für die Ressource freigegeben wurde und ob dieser Benutzer Mitglied oder Gast ist. Diese Aktivität wird häufig von einem zweiten Ereignis begleitet, die beschreibt, wie der Benutzer Zugriff auf die Ressource gewährt wurde; Angenommen, hinzufügen den Benutzer zu einer Gruppe, die Zugriff auf die Ressource hat.<br/> |
|Aktualisierte zugriffsanforderung  <br/> |AccessRequestUpdated  <br/> |Eine zugriffsanforderung auf ein Element aktualisiert wurde.  <br/> |
|Aktualisiert einen anonymen link  <br/> |AnonymousLinkUpdated  <br/> |Benutzer aktualisiert einen anonymen Link auf eine Ressource. Das aktualisierte Feld ist in der EventData-Eigenschaft enthalten, wenn Sie die Suchergebnisse exportieren.  <br/> |
|Aktualisiert eine freigabeeinladung  <br/> |SharingInvitationUpdated  <br/> |Eine externe freigabeeinladung wurde aktualisiert.  <br/> |
|Verwendet einen anonymen link  <br/> |AnonymousLinkUsed  <br/> |Anonymer Benutzer auf eine Ressource mithilfe einer Verknüpfung auf der anonymen zugegriffen. Die Identität des Benutzers ist möglicherweise nicht bekannt, aber Sie können andere Informationen wie IP-Adresse des Benutzers abrufen.  <br/> |
|Datei nicht freigegeben, Ordner oder site  <br/> |SharingRevoked  <br/> |Benutzer (Mitglied oder Gast) nicht freigegeben, Dateien, Ordner oder Website, die zuvor mit einem anderen Benutzer freigegeben wurde.  <br/> |
|Einen Unternehmen freigebbare Link verwendet  <br/> |CompanyLinkUsed  <br/> |Benutzer Zugriff auf eine Ressource über eine unternehmensweite Verknüpfung.  <br/> |
|Sichere Verbindung verwendet  <br/> |SecureLinkUsed  <br/> |Ein Benutzer verwendet eine sichere Verbindung.  <br/> |
|Benutzer, die sichere Verbindung  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die als sharing sichere Verbindung verwenden können.  <br/> |
|Benutzer von sichere Verbindung entfernt  <br/> |RemovedFromSecureLink  <br/> |Ein Benutzer wurde aus der Liste der Entitäten entfernt, die als sharing sichere Verbindung verwenden können.  <br/> |
|Einstellten Einladung zur Freigabe  <br/> |SharingInvitationRevoked  <br/> |Benutzer einstellten eine Einladung zur Freigabe auf eine Ressource.  <br/> |
  
### <a name="synchronization-activities"></a>Synchronisierung Aktivitäten
  
Die folgende Tabelle enthält die Datei Synchronisierung Aktivitäten in SharePoint Online und OneDrive für Unternehmen.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Computer zum Synchronisieren von Dateien zulässig  <br/> |ManagedSyncClientAllowed  <br/> |Benutzer richtet erfolgreich eine Sync-Beziehung mit einer Website. Die Sync-Beziehung ist erfolgreich, da es sich bei dem Computer des Benutzers ein Mitglied einer Domäne ist, die die Liste der Domänen (mit der Bezeichnung der *Liste sicherer Empfänger* ) hinzugefügt wurden, die Dokumentbibliotheken in Ihrer Organisation zugreifen können.<br/> Weitere Informationen zu diesem Feature finden Sie unter [Use Windows PowerShell-Cmdlets zum OneDrive-Synchronisierung für Domänen aktivieren, die in der Liste sicherer Empfänger sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Blockierte Computer aus der Synchronisierung von Dateien  <br/> |UnmanagedSyncClientBlocked  <br/> |Benutzer versucht, eine Synchronisierung Beziehung mit einer Website von einem Computer herstellen, der nicht Mitglied einer Domäne Ihrer Organisation ist, oder ist ein Mitglied einer Domäne, die nicht in die Liste der Domänen hinzugefügt wurde (aufgerufen, die *Liste sicherer Empfänger)* , die auf Dokument zugreifen können Bibliotheken in Ihrer Organisation. Die Sync-Beziehung ist nicht zulässig, und dem Computer des Benutzers synchronisiert wird, herunterladen oder Hochladen von Dateien in einer Dokumentbibliothek blockiert ist.<br/> Informationen zu diesem Feature finden Sie unter [Use Windows PowerShell-Cmdlets zum OneDrive-Synchronisierung für Domänen aktivieren, die in der Liste sicherer Empfänger sind](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Heruntergeladenen Dateien auf dem computer  <br/> |FileSyncDownloadedFull  <br/> |Benutzer richtet eine Beziehung Sync und downloads erfolgreich Dateien zum ersten Mal auf Ihrem jeweiligen Computer aus einer Dokumentbibliothek.  <br/> |
|Heruntergeladene Datei Änderungen an computer  <br/> |FileSyncDownloadedPartial  <br/> |Benutzer herunterlädt Änderungen an Dateien erfolgreich aus einer Dokumentbibliothek. Diese Aktivität gibt an, dass alle Änderungen, die in der Dokumentbibliothek Dateien vorgenommen wurden auf dem Computer des Benutzers heruntergeladen wurden. Nur Änderungen wurden heruntergeladen, da die Dokumentbibliothek vom Benutzer zuvor heruntergeladen wurde (wie die **Dateien auf Computer heruntergeladen** Aktivität angegeben).<br/> |
|Hochgeladenen Dateien in Dokumentbibliothek  <br/> |FileSyncUploadedFull  <br/> |Benutzer richtet eine Beziehung Sync und erfolgreich Dateien zum ersten Mal von ihrem Computer in einer Dokumentbibliothek hochgeladen.  <br/> |
|Hochgeladene Datei Änderungen an einer Dokumentbibliothek  <br/> |FileSyncUploadedPartial  <br/> |Benutzer werden die Änderungen erfolgreich in Dateien in einer Dokumentbibliothek hochgeladen. Dieses Ereignis gibt an, dass alle an der lokalen Version einer Datei aus einer Dokumentbibliothek vorgenommenen Änderungen erfolgreich in die Dokumentbibliothek hochgeladen werden. Nur Änderungen entladen werden, da diese Dateien vom Benutzer bereits hochgeladen wurden (durch die ** Dateien in die Dokumentbibliothek hochgeladen ** Aktivität).  <br/> |
  
### <a name="site-administration-activities"></a>Site-Verwaltungsaktivitäten
  
Die folgende Tabelle enthält die Ereignisse, die von Site-Administrationsaufgaben in SharePoint Online.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Ausgenommene Benutzer-Agent hinzugefügt  <br/> |ExemptUserAgentSet  <br/> |Eine SharePoint oder globaler Administrator Fügt einen Benutzer-Agent zur Liste der ausgenommene Benutzer-Agents in der SharePoint-Verwaltungskonsole.  <br/> |
|Hinzugefügte Websitesammlungs-Administrator  <br/> |SiteCollectionAdminAdded  <br/> |Websitesammlungs-Administrator oder Besitzer eine Person, die als ein Websitesammlungsadministrator für eine Website hinzugefügt werden. Websitesammlungsadministratoren haben Vollzugriff-Berechtigungen für die Websitesammlung und aller Unterwebsites.  <br/> |
|Hinzugefügte Benutzer oder Gruppen zu SharePoint-Gruppe  <br/> |AddedToGroup  <br/> |Benutzer werden ein Element oder Gast zu einer SharePoint-Gruppe hinzugefügt. Dies möglicherweise eine beabsichtigte Aktion oder das Ergebnis einer anderen Aktivität, wie ein Ereignis sharing wurden.  <br/> |
|Zulässige Benutzer zum Erstellen von Gruppen  <br/> |AllowGroupCreationSet  <br/> |Websiteadministrator oder Besitzer Fügt eine Berechtigungsstufe auf einer Website, die einem Benutzer ermöglicht, die Berechtigung zum Erstellen einer Gruppe für diesen Standort zugewiesen.  <br/> |
|Geo abgebrochen Website verschieben  <br/> |SiteGeoMoveCancelled  <br/> |Eine SharePoint oder globaler Administrator hebt erfolgreich eine SharePoint oder OneDrive Website Geo verschoben werden. Die Multi-Geo-Funktion können eine Office 365-Organisation mehrere Regionen für die Office 365-Datacenter, umfassen die Geos bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Geändert von einer Freigaberichtlinie  <br/> |SharingPolicyChanged  <br/> |Eine SharePoint globaler Administrator geändert oder eine SharePoint Freigaberichtlinie mithilfe der Office 365-Verwaltungsportal, SharePoint-Admin-Portal oder SharePoint Online-Verwaltungsshell. Jede Änderung an den Einstellungen in die Freigaberichtlinie in Ihrer Organisation wird angemeldet sein. Die Richtlinie, die geändert wurde, wird im Feld **geänderte Eigenschaften** in die Detailangaben zu den Eigenschaften des Datensatzes identifiziert.<br/> |
|Gerät Zugriffsrichtlinie geändert  <br/> |DeviceAccessPolicyChanged  <br/> |Eine SharePoint oder der globale Administrator hat die nicht verwalteten Geräten-Richtlinie für Ihre Organisation geändert. Diese Richtlinie steuert den Zugriff auf SharePoint, OneDrive und Office 365 von Geräten, die Ihre Organisation verknüpft werden. Konfigurieren diese Richtlinie erfordert eine Enterprise-Mobilität + Security-Abonnement. Weitere Informationen finden Sie unter [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).<br/> |
|Geänderte ausgenommene Benutzer-agents  <br/> |CustomizeExemptUsers  <br/> |Eine SharePoint oder globaler Administrator angepasst die Liste der ausgenommene Benutzer-Agents in der SharePoint-Verwaltungskonsole. Sie können die Benutzer-Agents zu erhalten, eine gesamte Webseite Index ausgenommen angeben. Dies bedeutet, dass wenn eine Benutzer-Agent, der Sie ein InfoPath-Formular als ausgenommen stößt angegeben haben, wird das Formular als XML-Datei, anstatt eine gesamte Webseite zurückgegeben werden soll. Dies beschleunigt Indizierung InfoPath-Formularen.  <br/> |
|Netzwerk-Zugriffsrichtlinie geändert  <br/> |NetworkAccessPolicyChanged  <br/> |Ein SharePoint oder globaler Administrator sich die standortbasierte Zugriffsrichtlinie (auch als eine vertrauenswürdige Netzwerkgrenze bezeichnet) in der SharePoint-Verwaltungskonsole oder mithilfe von SharePoint Online-PowerShell geändert. Dieser Typ der Richtlinie-Steuerelemente, die SharePoint- und OneDrive Ressourcen in einer Organisation anhand von autorisierten IP-Adressbereiche, die Sie angeben zugreifen können. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf SharePoint Online und OneDrive Daten basierend auf Speicherort im Netzwerk](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).<br/> |
|Abgeschlossene Website Geo verschieben  <br/> |SiteGeoMoveCompleted  <br/> |Eine Website Geo Verschiebung, die durch ein globaler Administrator in Ihrer Organisation geplant wurde wurde erfolgreich abgeschlossen. Die Multi-Geo-Funktion können eine Office 365-Organisation mehrere Regionen für die Office 365-Datacenter, umfassen die Geos bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Erstellte Gruppe  <br/> |GroupAdded  <br/> |Websiteadministrator oder Besitzer erstellt eine Gruppe für eine Website oder führt eine Aufgabe, die Ergebnisse in einer Gruppe erstellt wird. Beispielsweise wird erstmals ein Benutzer einen Link, um eine Dateifreigabe erstellt, eine Systemgruppe OneDrive for Business-Standort des Benutzers hinzugefügt. Dieses Ereignis kann auch ein Ergebnis eines Benutzers erstellen eine Verknüpfung mit Berechtigungen für eine freigegebene Datei bearbeiten.  <br/> |
|Erstellte Verbindung senden an  <br/> |SendToConnectionAdded  <br/> |Eine SharePoint oder globaler Administrator erstellt eine neue Verbindung senden an auf der Seite Records Management in der SharePoint-Verwaltungskonsole. Eine Verbindung zum Senden an gibt die Einstellungen für einem Dokumentrepository oder einem Datenarchiv. Wenn Sie eine Verbindung zum Senden an erstellen, können die Inhaltsorganisation Dokumente an der angegebenen Position übermitteln.  <br/> |
|Erstellten Websitesammlung  <br/> |SiteCollectionCreated  <br/> |Eine SharePoint oder globaler Administrator erstellt eine neue Websitesammlung in die SharePoint Online-Organisation oder ein Benutzer bereitgestellt wird, ihre OneDrive for Business-Site.  <br/> |
|Gelöschte Gruppe  <br/> |GroupRemoved  <br/> |Benutzer löscht eine Gruppe aus einer Website.  <br/> |
|Gelöschte Verbindung senden an  <br/> |SendToConnectionRemoved  <br/> |Eine SharePoint oder globaler Administrator Löscht eine Verbindung senden an auf der Seite Records Management in der SharePoint-Verwaltungskonsole.  <br/> |
|Gelöschte Website  <br/> |SiteDeleted  <br/> |Websiteadministrator eine Website gelöscht.  <br/> |
|Dokumentvorschau aktiviert  <br/> |PreviewModeEnabledSet  <br/> |Websiteadministrator kann Dokumentvorschau für eine Website.  <br/> |
|Legacy-Workflow aktiviert  <br/> |LegacyWorkflowEnabledSet  <br/> |Websiteadministrator oder Besitzer fügt der Website den Inhaltstyp für SharePoint 2013-Workflowtask hinzu. Globale Administratoren können auch im SharePoint Admin Center Workflows für die gesamte Organisation aktivieren.  <br/> |
|Aktiviert Office on Demand  <br/> |OfficeOnDemandSet  <br/> |Websiteadministrator ermöglicht Office on Demand, dem Benutzer die neueste Version des Office-desktopanwendungen zugreifen kann. Office on Demand ist aktiviert, in der SharePoint-Verwaltungskonsole und erfordert ein Office 365-Abonnement, die vollständige, installierte Office-Clientanwendungen enthält.  <br/> |
|Aktivierte RSS-feeds  <br/> |NewsFeedEnabledSet  <br/> |Websiteadministrator oder Besitzer können RSS-Feeds für eine Website. Globale Administratoren können RSS-Feeds für die gesamte Organisation im SharePoint Administrationscenter aktivieren.  <br/> |
|Geänderte zugriffsanforderung festlegen  <br/> |WebRequestAccessModified  <br/> |Die Einstellungen für die Anforderung wurden auf einer Website geändert.  <br/> |
|Geänderte Elemente können freigeben-Einstellung  <br/> |WebMembersCanShareModified  <br/> |Die Einstellung **Mitglieder können freigeben** wurde auf einer Website geändert.  <br/> |
|Geänderte Projektwebsite-Berechtigungen  <br/> |SitePermissionsModified  <br/> |Websiteadministrator oder Besitzer (oder Systemkonto) ändert sich die Berechtigungsstufe, die eine Gruppe auf einer Website zugeordnet sind. Diese Aktivität wird auch protokolliert, wenn alle Berechtigungen aus einer Gruppe entfernt werden.<br/> > [!NOTE]> Dieser Vorgang wurde in SharePoint Online verworfen. Damit Ereignisse ermittelt wird, können Sie für andere Aktivitäten Berechtigungen in Zusammenhang stehen, wie **Websitesammlungsadministrator hinzugefügt**, **Es wurden Benutzer oder eine Gruppe zu SharePoint-Gruppe**, **Zugelassene Benutzer zum Erstellen von Gruppen**, **Gruppe erstellt**und **Deleted suchen Gruppe.**         |
|Benutzer oder eine Gruppe von SharePoint-Gruppe entfernt.  <br/> |RemovedFromGroup  <br/> |Benutzer entfernt ein Element oder Gast aus einer SharePoint-Gruppe an. Dies kann eine beabsichtigte Aktion oder das Ergebnis einer anderen Aktivität, wie ein Ereignis Sperren wurden.  <br/> |
|Umbenannte Website  <br/> |SiteRenamed  <br/> |Benennt Websiteadministrator oder Besitzer eine Website  <br/> |
|Administratorberechtigungen für die angeforderte Website  <br/> |SiteAdminChangeRequest  <br/> |Benutzeranfragen als ein Websitesammlungsadministrator für eine Websitesammlung hinzugefügt werden soll. Websitesammlungsadministratoren haben Vollzugriff-Berechtigungen für die Websitesammlung und aller Unterwebsites.  <br/> |
|Geo geplanten Website verschieben  <br/> |SiteGeoMoveScheduled  <br/> |Eine SharePoint oder globaler Administrator plant erfolgreich eine SharePoint oder OneDrive Website Geo verschoben werden. Die Multi-Geo-Funktion können eine Office 365-Organisation mehrere Regionen für die Office 365-Datacenter, umfassen die Geos bezeichnet werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Set-Hostwebsite  <br/> |HostSiteSet  <br/> |Eine SharePoint oder globaler Administrator festgelegte Website zum Hosten von persönlichen oder OneDrive für Websites mit Geschäftsdaten geändert.  <br/> |
|Aktualisierte Gruppe  <br/> |GroupUpdated  <br/> |Websiteadministrator oder Besitzer die Einstellungen einer Gruppe für eine Website geändert. Dazu kann gehören, ändern den Namen der Gruppe, anzeigen oder Bearbeiten der Gruppenmitgliedschaft und wie Mitgliedschaft Anforderungen behandelt werden kann.  <br/> |
  
### <a name="exchange-mailbox-activities"></a>Exchange-Postfach-Aktivitäten
  
Die folgende Tabelle enthält die Aktivitäten, die vom Postfach protokolliert werden können postfachüberwachungsprotokollierung. Postfach Aktivitäten von den Besitzer des Postfachs, ein delegierte Benutzer oder Administrator angemeldet sind. Standardmäßig ist nicht Überwachung von Postfächern in Office 365 aktiviert. Mailbox Audit Logging muss aktiviert werden für jedes Postfach vor dem Postfach Aktivität protokolliert werden. Weitere Informationen finden Sie unter [Aktivieren der Überwachung in Office 365 Postfach](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Hinzugefügten Stellvertretung Postfachberechtigungen  <br/> |Add-MailboxPermission  <br/> |Ein Administrator hat die Berechtigung FullAccess Postfach an einen Benutzer (als Stellvertreter bezeichnet) an eine andere Person Postfach festgelegt. Die Berechtigung FullAccess ermöglicht es der Stellvertretung zum Öffnen des anderen Teilnehmers Postfach, und lesen und den Inhalt des Postfachs verwalten.  <br/> |
|Die kopierten Nachrichten in einen anderen Ordner  <br/> |Kopieren  <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |
|Erstellte Postfach-Element  <br/> |Erstellen  <br/> |Ein Element wird in den Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht wird nicht überwacht. Erstellen einen Postfachordner wird auch nicht überwacht.  <br/> |
|Gelöschte Nachrichten aus dem Ordner Gelöschte Elemente  <br/> |SoftDelete  <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner Gelöschte Elemente gelöscht. Diese Elemente werden in den Ordner "wiederherstellbare Elemente" verschoben. Nachrichten werden auch in den Ordner wiederherstellbare Elemente verschoben, wenn ein Benutzer wählt sie aus, und drücken **UMSCHALT + ENTF**.<br/> |
|Nachrichten in einen anderen Ordner verschoben  <br/> |Verschieben  <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |
|Nachrichten in Ordner Gelöschte Elemente verschoben  <br/> |MoveToDeletedItems  <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |
|Geänderte Ordnerberechtigungen  <br/> |UpdateFolderPermissions  <br/> |Eine Ordnerberechtigung wurde geändert. Ordner Berechtigungen-steuern, welche Benutzer in Ihrer Organisation Postfachordner und die Nachrichten im Ordner zugreifen können.  <br/> |
|Gelöschten Nachrichten aus dem Postfach  <br/> |HardDelete  <br/> |Eine Nachricht wurde aus "wiederherstellbare Elemente" (dauerhaft aus dem Postfach gelöscht) gelöscht.  <br/> |
|Entfernte Delegat Postfachberechtigungen  <br/> |Remove-MailboxPermission  <br/> |Ein Administrator entfernt die Berechtigung FullAccess (die Stellvertreter zugewiesen wurde) aus einer Person Postfach. Nachdem die Berechtigung FullAccess entfernt wurde, kann nicht die Stellvertretung Öffnen des anderen Teilnehmers Postfach oder Zugriff auf alle Inhalte darin.  <br/> |
|Gesendete Nachricht mit der Berechtigung Senden als  <br/> |"SendAs"  <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |
|Nachricht gesendet Senden im Auftrag von Berechtigungen  <br/> |Sendonbehalf werden standardmäßig  <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |
|Aktualisierte Delegieren des Zugriffs auf Kalenderordner  <br/> |UpdateCalendarDelegation  <br/> |Eine kalenderdelegierung wurde eines Postfachs zugewiesen. Kalenderdelegierung ermöglicht eine andere Person in der gleichen Organisationsberechtigungen zum Verwalten des Postfachbesitzers Kalenders.  <br/> |
|Aktualisierte Nachricht  <br/> |Aktualisieren  <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |
|Benutzer, die im Postfach angemeldet  <br/> |MailboxLogin  <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |
|(kein Rahmen)  <br/> |UpdateInboxRules  <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. Posteingangsregeln dienen zum Verarbeiten von Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen und Aktionen, wenn die Bedingung einer Regel erfüllt sind, wie eine Nachricht in einen bestimmten Ordner verschieben oder Löschen einer Nachricht.<br/> Zum Zurückgeben von Einträgen für Posteingang Regel Aktivitäten, müssen Sie **Ergebnisse für alle Aktivitäten** in der Liste der **Aktivitäten** aus. Verwenden Sie den Bereich Datumsfeldern und **der Benutzerliste** , um die Suchergebnisse einzuschränken.<br/> |
  
### <a name="sway-activities"></a>Sway Aktivitäten
  
Die folgende Tabelle enthält die Benutzer- und Admin Aktivitäten in Schlingern. Schlingern ist eine Office 365-app, die Benutzer zu erfassen, formatieren und Freigeben von Ideen, Textabschnitte und Präsentationen auf eine interaktive, webbasierte Zeichenbereich helfen. Weitere Informationen finden Sie unter [häufig gestellte Fragen zu Schlingern - Admin-Hilfe](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Schlingern Freigabe-Ebene  <br/> |SwayChangeShareLevel  <br/> |Benutzer, die Zugriffsebene Freigeben einer Schlingern ändert. Dieses Ereignis erfasst den Benutzer ändern den Bereich der Freigabe einer Schlingern zugeordnet. beispielsweise Öffentliche im Vergleich zu innerhalb der Organisation.  <br/> |
|Erstellte Schlingern  <br/> |SwayCreate  <br/> |Benutzer erstellt eine Schlingern.  <br/> |
|Gelöschte Schlingern  <br/> |SwayDelete  <br/> |Benutzer löscht eine Schlingern.  <br/> |
|Deaktivierte Schlingern Duplizierung  <br/> |SwayDisableDuplication  <br/> |Benutzer wird die Duplizierung von einer Schlingern deaktiviert.  <br/> |
|Duplizierte Schlingern  <br/> |SwayDuplicate  <br/> |Benutzer dupliziert eine Schlingern.  <br/> |
|Bearbeitete Schlingern  <br/> |SwayEdit  <br/> |Benutzer bearbeitet ein Schlingern.  <br/> |
|Aktivierte Schlingern Duplizierung  <br/> |EnableDuplication  <br/> |Benutzer kann die Duplizierung von einer Schlingern. die Möglichkeit, um die Duplizierung von einem Schlingern zu ermöglichen, ist standardmäßig aktiviert.  <br/> |
|Gesperrte Schlingern Freigabe  <br/> |SwayRevokeShare  <br/> |Freigeben einer Schlingern durch Aufheben der Zugriff darauf beendet. Widerrufen des Zugriffs ändert die Links eine Schlingern zugeordnet.  <br/> |
|Freigegebene Schlingern  <br/> |SwayShare  <br/> |Benutzer beabsichtigt, eine Schlingern freigeben. Dieses Ereignis erfasst die Aktion des Benutzers auf bestimmte Freigabeziel in das Menü Schlingern freigeben. Das Ereignis gibt nicht an, ob der Benutzer die Freigabe Aktion ausgeführt.  <br/> |
|Externe Freigabe von Schlingern deaktiviert  <br/> |SwayExternalSharingOff  <br/> |Administrator deaktiviert externe Schlingern Freigabe für die gesamte Organisation mithilfe der Office 365-Verwaltungskonsole.  <br/> |
|Externe Freigabe von Schlingern aktiviert  <br/> |SwayExternalSharingOn  <br/> |Administrator kann externe Schlingern Freigabe für die gesamte Organisation mithilfe der Office 365-Verwaltungskonsole.  <br/> |
|Schlingern Service deaktiviert  <br/> |SwayServiceOff  <br/> |Administrator deaktiviert Schlingern für die gesamte Organisation mithilfe der Office 365-Verwaltungskonsole.  <br/> |
|Schlingern Service aktiviert  <br/> |SwayServiceOn  <br/> |Administrator kann Schlingern für die gesamte Organisation mithilfe des Office 365 Administrationscenter (Schlingern Dienst in der Standardeinstellung aktiviert ist).  <br/> |
|Angezeigte Schlingern  <br/> |SwayView  <br/> |Benutzer zeigt eine Schlingern.  <br/> |

  
### <a name="user-administration-activities"></a>Die Verwaltung Benutzeraktivitäten
  
Die folgende Tabelle enthält die Administration Benutzeraktivitäten, die protokolliert werden, wenn ein Administrator hinzufügen oder ändern ein Benutzerkonto mithilfe von Office 365 Administrationscenter oder dem Azure-Verwaltungsportal.
  
|**Aktivität**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Benutzer wurde hinzugefügt.  <br/> |Benutzer hinzufügen  <br/> |Ein Office 365-Benutzerkonto erstellt wurde.  <br/> |
|Geänderte Benutzerlizenz  <br/> |Change-Benutzerlizenz  <br/> |Die Lizenz zugewiesen, die einem Benutzer, was sich geändert hat. Um herauszufinden, welche Lizenzen Änderungen wurden, finden Sie unter den entsprechenden Benutzeraktivität **aktualisiert** .<br/> |
|Geänderte Benutzerkennwort  <br/> |Benutzerkennwort ändern  <br/> |Administrator geändert, das Kennwort das Kennwort für einen Benutzer.  <br/> |
|Gelöschter Benutzer  <br/> |Löschen eines Benutzers  <br/> |Ein Office 365-Benutzerkonto wurde gelöscht.  <br/> |
|Benutzerkennwort zurücksetzen  <br/> |Benutzerkennwort zurücksetzen  <br/> |Administrator Zurücksetzen des Kennworts für einen Benutzer.  <br/> |
|Legen Sie-Eigenschaft, die erzwingt, dass Benutzer das Kennwort ändern  <br/> |Set-Force-Benutzerkennwort ändern  <br/> |Administrator festlegen die Eigenschaft, die einen Benutzer das Ändern ihres Kennworts, das das nächste Mal Benutzer anmelden bei Office 365, erzwingt.  <br/> |
|Lizenz-Eigenschaften festlegen  <br/> |Lizenz-Eigenschaften festlegen  <br/> |Administrator ändert die Eigenschaften einer lizenzierten einem Benutzer zugewiesen.  <br/> |
|Aktualisierte Benutzer  <br/> |Benutzer aktualisieren  <br/> |Administrator ändert eine oder mehrere Eigenschaften eines Benutzerkontos ein. Eine Liste mit den Benutzereigenschaften, die aktualisiert werden können, finden Sie im Abschnitt "Benutzerattribute aktualisieren" in [Azure Active Directory Bericht Überwachungsereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).<br/> |
  
### <a name="azure-ad-group-administration-activities"></a>Azure Active Directory-Gruppe Administration Aktivitäten
  
Die folgende Tabelle enthält die Gruppe Verwaltung der Aktivitäten, die protokolliert werden, wenn ein Administrator oder von einem Benutzer erstellt oder eine Office 365-Gruppe ändert oder ein Administrator eine Sicherheitsgruppe mithilfe von Office 365 Administrationscenter oder dem Azure-Verwaltungsportal erstellt. Weitere Informationen zu Gruppen in Office 365 finden Sie unter [anzeigen, erstellen und Löschen von Gruppen in Office 365 Administrationscenter](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Hinzugefügte Gruppe  <br/> |Gruppe hinzufügen  <br/> |Eine Gruppe erstellt wurde.  <br/> |
|Mitglied der Gruppe hinzugefügt  <br/> |Mitglied der Gruppe hinzufügen  <br/> |Ein Mitglied wurde zu einer Gruppe hinzugefügt.  <br/> |
|Gelöschte Gruppe  <br/> |Gruppe löschen  <br/> |Eine Gruppe wurde gelöscht.  <br/> |
|Entfernte Mitglied aus Gruppe  <br/> |Mitglied aus Gruppe entfernen  <br/> |Es wurde ein Mitglied aus einer Gruppe entfernt.  <br/> |
|Aktualisierte Gruppe  <br/> |Aktualisierungsgruppe  <br/> |Eine Eigenschaft einer Gruppe wurde geändert.  <br/> |
   
### <a name="application-administration-activities"></a>Anwendung Administration Aktivitäten
  
Die folgende Tabelle enthält die Anwendung Admin Aktivitäten, die protokolliert werden, wenn ein Administrator hinzufügen oder ändern eine Anwendung, die in Azure Active Directory registriert ist. Eine beliebige Anwendung, die Azure AD für die Authentifizierung verwendet, muss in das Verzeichnis registriert werden.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Hinzugefügte Delegierung-Eintrag  <br/> |Fügen Sie Delegierung Eintrag hinzu  <br/> |Eine Berechtigung für die Authentifizierung war zu einer Anwendung in Azure Active Directory erstellt/erteilt.  <br/> |
|Hinzugefügte Dienstprinzipalnamen  <br/> |Hinzufügen von Dienstprinzipalnamen  <br/> |Eine Anwendung wurde in Azure Active Directory registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Hinzugefügte Anmeldeinformationen eines Prinzipals service  <br/> |Hinzufügen von Anmeldeinformationen für den Prinzipal Dienst  <br/> |Anmeldeinformationen wurden mit einem Prinzipal in Azure Active Directory-Dienst hinzugefügt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Entfernte Delegierung-Eintrag  <br/> |Delegierung Eintrag entfernen  <br/> |Eine Authentifizierung Berechtigung wurde von einer Anwendung in Azure Active Directory entfernt.  <br/> |
|Entfernt einen Dienstprinzipal aus dem Verzeichnis  <br/> |Entfernen von Dienstprinzipalnamen  <br/> |Eine Anwendung wurde aus dem Azure Active Directory gelöscht/nicht registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Entfernte Anmeldeinformationen aus einem Dienst Prinzipal  <br/> |Principal Dienstanmeldeinformationen entfernen  <br/> |Anmeldeinformationen wurden aus einem Dienst in Azure AD principal entfernt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Set-Delegierung-Eintrag  <br/> |Set-Delegierung-Eintrag  <br/> |Eine Authentifizierung Berechtigung wurde für eine Anwendung in Azure Active Directory aktualisiert.  <br/> |

### <a name="role-administration-activities"></a>Rolle Administration Aktivitäten
  
Die folgende Tabelle enthält die Azure AD-Rolle Administration Aktivitäten protokolliert werden, wenn ein Administrator Administratorrollen in Office 365 Administrationscenter oder in der Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Mitglied der Rolle hinzufügen  <br/> |Fügen Sie der Rolle Rolle  <br/> |Einen Benutzer hinzugefügt zu einer Administratorrolle im Office 365.  <br/> |
|Entfernt einen Benutzer aus einer Rolle directory  <br/> |Mitglied der Rolle von Rolle entfernen  <br/> |Entfernt einen Benutzer aus einer Administratorrolle in Office 365.  <br/> |
|Legen Sie die Kontaktinformationen für Unternehmen  <br/> |Legen Sie die Kontaktinformationen für Unternehmen  <br/> |Aktualisiert die Unternehmensebene Kontakten Vorgaben für Office 365-Organisation. Dazu gehören e-Mail-Adressen für Abonnement-bezogene e-Mail vom Office 365 sowie technische Benachrichtigungen zu Office 365-Dienste gesendet.  <br/> |
   
### <a name="directory-administration-activities"></a>Directory Administration Aktivitäten
  
Die folgende Tabelle listet Azure Active Directory Directory und Domänen-bezogenen Aktivitäten, die protokolliert werden, wenn ein Administrator ihre Office 365-Organisation in Office 365 Administrationscenter oder in der Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Hinzugefügte Domäne für Unternehmen  <br/> |Hinzufügen einer Domäne zu Unternehmen  <br/> |Eine Domäne hinzugefügt zu Office 365-Organisation.  <br/> |
|Einen Partner hinzugefügt zum Verzeichnis.  <br/> |Hinzufügen von Partnern für Unternehmen  <br/> |Partner (delegierte Administrator) hinzugefügt zu Office 365-Organisation.  <br/> |
|Entfernte Domäne in Unternehmen  <br/> |Entfernen von Domänen in Unternehmen  <br/> |Entfernt eine Domäne aus Office 365-Organisation.  <br/> |
|Einen Partner entfernt aus dem Verzeichnis.  <br/> |Entfernen Sie Partner in Unternehmen  <br/> |Partner (delegierte Administrator) entfernt von Office 365-Organisation.  <br/> |
|Set-Firmeninformationen  <br/> |Set-Firmeninformationen  <br/> |Aktualisiert die Firmeninformationen für Office 365-Organisation. Dazu gehören e-Mail-Adressen für Abonnement-bezogene e-Mail vom Office 365 sowie technische Benachrichtigungen zu Office 365-Dienste gesendet.  <br/> |
|Festlegen der Domänenauthentifizierung  <br/> |Festlegen der Domänenauthentifizierung  <br/> |Die Einstellung für die Authentifizierung für Office 365-Organisation geändert.  <br/> |
|Aktualisiert die verbundeinstellungen für eine Domäne  <br/> |Festlegen von verbundeinstellungen für Domäne  <br/> |Geändert (externe Freigabe) verbundeinstellungen für Office 365-Organisation.  <br/> |
|Set-Kennwortrichtlinie  <br/> |Set-Kennwortrichtlinie  <br/> |Die Pfadlängen- und Einschränkungen für Benutzerkennwörter in Office 365-Organisation geändert.  <br/> |
|Azure AD-Synchronisierung – aktiviert  <br/> |Festlegen von DirSyncEnabled Flag für Unternehmen  <br/> |Legen Sie die Eigenschaft, die ein Verzeichnis für Azure AD-Synchronisierung – ermöglicht.  <br/> |
|Aktualisierte Domäne  <br/> |Domäne aktualisieren  <br/> |Aktualisiert die Einstellungen einer Domäne in Office 365-Organisation.  <br/> |
|Überprüften Domäne  <br/> |Überprüfen der Domäne  <br/> |Sichergestellt, dass Ihre Organisation den Besitzer einer Domäne ist.  <br/> |
|Überprüften e-Mail überprüften Domäne  <br/> |Überprüfen von e-Mail-überprüften Domäne  <br/> |Verwendeten e-Mail-Überprüfung, um sicherzustellen, dass Ihre Organisation den Besitzer einer Domäne ist.  <br/> |
   
### <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten
  
Content-Suche und eDiscovery-bezogene Aktivitäten, die in Office 365-Sicherheit ausgeführt werden &amp; Compliance Center oder durch Ausführen der entsprechenden Windows PowerShell-Cmdlets im Überwachungsprotokoll Office 365 angemeldet sind. Dazu gehören die folgenden Aktivitäten:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, starten und Bearbeiten von Content-Suche
    
- Ausführen Inhaltssuche Aktionen, beispielsweise das Anzeigen einer Vorschau, führt zu ausführenden und Löschen von Suche
    
- Konfigurieren von Berechtigungen für die Inhaltssuche filtern
    
- Verwalten von eDiscovery-Administratorrolle
    
Eine Liste und eine detaillierte Beschreibung der eDiscovery-Aktivitäten, die protokolliert werden, finden Sie unter [Suchen für eDiscovery-Aktivitäten in der Office 365 in das Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Es dauert bis zu 30 Minuten für Ereignisse, die aus den Aktivitäten aufgeführt, die unter dem **eDiscovery-Aktivitäten** in der Dropdownliste **Aktivitäten** , die in den Suchergebnissen angezeigt werden. Dagegen dauert bis zu 24 Stunden für die entsprechenden Ereignisse aus eDiscovery Cmdlet Aktivitäten aus, die in den Suchergebnissen angezeigt werden. 
  
### <a name="power-bi-activities"></a>Power BI-Aktivitäten
  
Sie können das Überwachungsprotokoll Aktivitäten in Power BI suchen. Informationen zu Power BI-Aktivitäten finden Sie im Abschnitt "Vorgänge überwacht von Power Power BI" unter [Using Überwachung innerhalb Ihrer Organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
Beachten Sie, dass die überwachungsprotokollierung für Power BI standardmäßig nicht aktiviert ist. Zum Suchen von Power BI-Aktivitäten im Überwachungsprotokoll Office 365 müssen Sie zum Aktivieren der Überwachung in Power BI-Admin-Portal. Eine Anleitung finden Sie im Abschnitt "Überwachungsprotokolle" [Power BI](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)-Verwaltungsportal.
  
### <a name="microsoft-teams-activities"></a>Microsoft-Teams, Aktivitäten
  
Die folgende Tabelle enthält den Benutzer und Überwachungsprotokoll Admin Aktivitäten in Microsoft-Teams, die in der Office 365 angemeldet sind. Microsoft-Teams, ist ein Chat zentriert Arbeitsbereich in Office 365. Es vereint Unterhaltungen, Besprechungen, Dateien und Notizen ein Team in einem einzigen Speicherort. Weitere Informationen und Links zu Themen können finden Sie unter:
  
- [Häufig gestellte Fragen zu Microsoft-Teams - Admin-Hilfe](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Hilfe für Microsoft-Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Hinzugefügte Bot an das team  <br/> |BotAddedToTeam  <br/> |Ein Benutzer hinzugefügt ein Team einen Bot.  <br/> |
|DDE-Kanal hinzugefügt  <br/> |ChannelAdded  <br/> |Ein Benutzer hinzugefügt ein Team einen Kanal.  <br/> |
|Hinzugefügte connector  <br/> |ConnectorAdded  <br/> |Ein Benutzer hinzugefügt eine Verbindung zu einem Kanal.  <br/> |
|Hinzugefügte Elemente an das team  <br/> |MemberAdded  <br/> |Der Teambesitzer einer hinzugefügt ein Team Mitglieder.  <br/> |
|Hinzugefügte Registerkarte  <br/> |TabAdded  <br/> |Ein Benutzer hinzugefügt einen Kanal eine Registerkarte.  <br/> |
|Kanal-Einstellung geändert  <br/> |ChannelSettingChanged  <br/> | Der Vorgang ChannelSettingChanged wird protokolliert, wenn die folgenden Aktivitäten von einem Teammitglied ausgeführt werden. Eine Beschreibung der Einstellung, die geändert wurde (siehe unten Klammer) wird für jede dieser Aktivitäten in der Spalte **Element** in den Suchergebnissen für Audit Log angezeigt.<br/> <br/>-Der Name des einer Team-Kanal ( **DDE-Kanalname**) geändert.  <br/>  <br/>-Die Beschreibung des einer Team-Kanal ( **DDE-Kanal Beschreibung**) geändert.  <br/> |
|Organisation Einstellung geändert  <br/> |TeamsTenantSettingChanged  <br/> | Der Vorgang TeamsTenantSettingChanged wird protokolliert, wenn die folgenden Aktivitäten ausgeführt werden, durch den ein globaler Administrator (mithilfe des Office 365 Administrationscenter). Beachten Sie, dass diese Aktivitäten organisationsweiten Microsoft-Teams Einstellungen auswirken. Weitere Informationen finden Sie unter [Administrator-Einstellungen für Microsoft-Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).<br/>  Eine Beschreibung der Einstellung, die geändert wurde (siehe unten Klammer) wird für jede dieser Aktivitäten in der Spalte **Element** in den Suchergebnissen für Audit Log angezeigt.  <br/><br/>-Aktiviert oder deaktiviert Microsoft-Teams für die Organisation ( **Microsoft-Teams**).  <br/><br/>-Aktiviert oder deaktiviert die Interoperabilität zwischen Microsoft-Teams und Skype für Unternehmen für die Organisation ( **Skype für die Interoperabilität Business**).<br/><br/>-Aktiviert oder deaktiviert die Organigramms Ansicht im Microsoft-Teams, Clients ( **Org Diagrammansicht**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder private Besprechungstermine ( **Private Besprechung planen**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder Besprechungstermine DDE-Kanal ( **DDE-Kanal auf Besprechung planen**).  <br/><br/>-Aktiviert oder deaktiviert video Aufrufen in Teams Besprechungen ( **Video für Skype Besprechungen**).  <br/><br/>-Aktiviert oder deaktiviert die Bildschirmfreigabe in Microsoft-Teams, Meetups für die Organisation ( **Bildschirmfreigabe Skype-Besprechungen**).  <br/><br/>-Aktiviert oder deaktiviert diese Möglichkeit zum Hinzufügen von animierte Bilder (als Giphys bezeichnet) auf Teams Unterhaltungen ( **animierter Bilder**).  <br/><br/>-Die Inhalte zur Bewertung der Einstellung für die Organisation ( **zum Bewerten**) ändert. Zum Bewerten der schränkt des Typs der Animation, die in Unterhaltungen angezeigt werden kann.<br/><br/>-Aktiviert, oder deaktiviert die Option für Teammitgliedern zum Hinzufügen von anpassbarer Bildern (benutzerdefinierte Memes genannt) aus dem Internet auf Team Unterhaltungen ( **anpassbar Bilder aus dem Internet**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit von Teammitgliedern zum Hinzufügen von bearbeitbaren Bildern (Aufkleber genannt) Team Unterhaltungen ( **bearbeitbare Bilder**).<br/><br/>-Aktiviert oder deaktiviert diese Möglichkeit für Teammitglieder Bots in Microsoft-Teams, Chats und Kanäle ( **Org geltende Bots**) verwenden.<br/><br/>-Können bestimmte Bots für Microsoft-Teams. Dies umfasst nicht den T-Bot, also die Hilfe Bot Teams, die verfügbar ist, wenn für die Organisation ( **einzelne Bots**) Bots aktiviert sind.  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder Extensions oder Registerkarten ( **Extensions oder Registerkarten**) hinzufügen.  <br/><br/>-Aktiviert oder deaktiviert das Laden Seite proprietäre Bots für Microsoft-Teams ( **Seite Laden von Programmen**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Benutzer zum Senden von e-Mail-Nachrichten an einen Microsoft-Teams-Kanal ( **DDE-Kanal e-Mail**).  <br/> |
|Geänderte Rolle von Mitgliedern in team  <br/> |MemberRoleChanged  <br/> |Ein Teambesitzer ändert die Rolle des Mitglieder in einem Team. Die folgenden Werte geben Sie an, die dem Benutzer zugewiesene Rollentyp.<br/><br/><br/> **1** – gibt die Rolle des Eigentümers an.<br/>**2** – gibt die Rolle an. <br/>**3** – gibt an, die Guest-Rolle. <br/>Members-Eigenschaft enthält auch den Namen Ihrer Organisation und e-Mail-Adresse des Mitglieds.  <br/> |
|Team Einstellung geändert  <br/> |TeamSettingChanged  <br/> | Der Vorgang TeamSettingChanged wird protokolliert, wenn von einer Teambesitzer die folgenden Aktivitäten ausgeführt werden. Eine Beschreibung der Einstellung, die geändert wurde (siehe unten Klammer) wird für jede dieser Aktivitäten in der Spalte **Element** in den Suchergebnissen für Audit Log angezeigt.<br/><br/>-Ändert den Zugriffstyp für ein Team. Teams können als privat oder öffentlich ( **Team Zugriffstyp**) liegen. Wenn ein Team ist privat (Standardeinstellung) Benutzer können nur über eine Einladung das Team zugreifen. Wenn ein Team öffentlich ist, ist es von jedem Benutzer sichtbar.<br/><br/>-Die Klassifizierung Informationen eines Teams ( **Team Klassifizierung**) ändert.  <br/>  Beispielsweise können Teams Daten als hohe geschäftliche Relevanz, mittlere geschäftliche Relevanz oder niedrig geschäftliche Relevanz klassifiziert werden.<br/><br/>-Der Name eines Teams ( **Teamname**) geändert.  <br/><br/>-Ändert die Beschreibung eines Teams ( **Team Beschreibung**). <br/><br/>-Änderungen an das Team-Einstellungen. Ein Teambesitzer kann diese Einstellungen in einer Clientdatenbank Teams indem Sie mit der rechten Maustaste ein Team, auf **Team verwalten**, und klicken Sie dann auf die Registerkarte **Einstellungen** zugreifen. Für das Rollout wird der Name der Einstellung, die geändert wurde in der Spalte **Element** in den Suchergebnissen für Audit Log angezeigt.<br/> |
|Erstellte team  <br/> |TeamCreated  <br/> |Ein Benutzer erstellt ein neues Team.  <br/> |
|Gelöschte DDE-Kanal  <br/> |ChannelDeleted  <br/> |Ein Benutzer löscht einen Kanal aus einem Team.  <br/> |
|Gelöschte team  <br/> |TeamDeleted  <br/> |Der Teambesitzer einer Löscht ein Team.  <br/> |
|Entfernte Bot-Teams  <br/> |BotRemovedFromTeam  <br/> |Ein Benutzer entfernt ein Bot aus einem Team.  <br/> |
|Entfernte connector  <br/> |ConnectorRemoved  <br/> |Ein Benutzer entfernt Connector aus einem Kanal.  <br/> |
|Entfernte Elemente-Teams  <br/> |MemberRemoved  <br/> |Ein Teambesitzer entfernt Mitglieder aus einem Team.  <br/> |
|Entfernte Registerkarte  <br/> |TabRemoved  <br/> |Ein Benutzer entfernt eine Registerkarte aus einem Kanal.  <br/> |
|Aktualisierte connector  <br/> |ConnectorUpdated  <br/> |Ein Benutzer eine Verbindung in einem Kanal geändert hat.  <br/> |
|Aktualisierte Registerkarte  <br/> |TabUpdated  <br/> |Ein Benutzer eine Registerkarte in einem Kanal geändert hat.  <br/> |
|Benutzer angemeldet Teams  <br/> |TeamsSessionStarted  <br/> |Ein Benutzer anmeldet an einen Microsoft-Teams, Client.  <br/> |

### <a name="yammer-activities"></a>Yammer-Aktivitäten
  
Die folgende Tabelle enthält den Benutzer und Überwachungsprotokoll Admin Aktivitäten in Yammer, die in der Office 365 angemeldet sind. Wenn zurückgeben möchten, dass in das Überwachungsprotokoll Yammer-bezogene Aktivitäten aus der Office 365, müssen Sie **Ergebnisse für alle Aktivitäten** in der Liste der **Aktivitäten** aus. Verwenden Sie den Bereich Datumsfeldern und **der Benutzerliste** , um die Suchergebnisse einzuschränken. 
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Datenaufbewahrungsrichtlinie  <br/> |SoftDeleteSettingsUpdated  <br/> |Überprüften Admin aktualisiert die Einstellung für das Netzwerk Daten Aufbewahrungsrichtlinie auf Festplatte löschen oder weiche löschen. Dieser Vorgang kann nur überprüften-Admins ausgeführt werden.  <br/> |
|Geänderte Netzwerkkonfiguration  <br/> |NetworkConfigurationUpdated  <br/> |Netzwerk- oder überprüften Admin ändert den Yammer-Netzwerk Konfiguration. Dazu gehört das Intervall für das Exportieren von Daten und Aktivieren von Chat festlegen.  <br/> |
|Geänderte Netzwerk-profileinstellungen  <br/> |ProcessProfileFields  <br/> |Netzwerk- oder überprüften Admin ändert die angezeigten Informationen auf Member Profile für Benutzer Netzwerk-Netzwerk.  <br/> |
|Private Modus Inhalt geändert  <br/> |SupervisorAdminToggled  <br/> |Überprüften Admin schaltet *Private Inhalte-Modus* oder aus. In diesem Modus können Beiträge Sicht Admin im privaten Gruppen und Anzeigen von private Nachrichten zwischen den einzelnen Benutzer (oder Gruppen von Benutzern). Dieser Vorgang kann nur überprüften-Admins nur ausgeführt werden.<br/> |
|Geänderte Sicherheitskonfiguration  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Überprüften Admin aktualisiert die Yammer-Netzwerk-Sicherheitskonfiguration. Dazu gehören Richtlinien für den Kennwortablauf Einstellung und Einschränkungen für IP-Adressen. Dieser Vorgang kann nur überprüften-Admins ausgeführt werden.  <br/> |
|Erstellte Datei  <br/> |FileCreated  <br/> |Benutzer hochlädt eine Datei.  <br/> |
|Erstellte Gruppe  <br/> |GroupCreation  <br/> |Benutzer erstellt eine neue Gruppe.  <br/> |
|Gelöschte Gruppe  <br/> |GroupDeletion  <br/> |Eine Gruppe wird aus Yammer gelöscht.  <br/> |
|Gelöschte Nachricht  <br/> |MessageDeleted  <br/> |Benutzer wird eine Nachricht gelöscht.  <br/> |
|Heruntergeladene Datei  <br/> |FileDownloaded  <br/> |Benutzer herunterlädt eine Datei.  <br/> |
|Exportierten Daten  <br/> |Datenexport  <br/> |Überprüften Admin exportiert Daten für Yammer-Netzwerk. Dieser Vorgang kann nur überprüften-Admins ausgeführt werden.  <br/> |
|Freigegebene Datei  <br/> |FileShared  <br/> |Benutzer kann eine Datei mit einem anderen Benutzer freigeben.  <br/> |
|Angehaltenen Netzwerkbenutzer  <br/> |NetworkUserSuspended  <br/> |Hält die Netzwerk- oder überprüften Admin (deaktiviert) eines Benutzers von Yammer.  <br/> |
|Gesperrte Mitglied  <br/> |UserSuspension  <br/> |Benutzerkonto wird angehalten (deaktiviert).  <br/> |
|Aktualisierte DateiBeschreibung  <br/> |FileUpdateDescription  <br/> |Benutzer, ändert die Beschreibung einer Datei.  <br/> |
|Aktualisierter Dateiname  <br/> |FileUpdateName  <br/> |Benutzer ändert den Namen einer Datei.  <br/> |
|Angezeigten Datei  <br/> |FileVisited  <br/> |Benutzer zeigt eine Datei.  <br/> |
   
### <a name="microsoft-flow"></a>Microsoft Flow

Sie können das Überwachungsprotokoll Aktivitäten in Microsoft Flow suchen. Hierzu zählen erstellen, bearbeiten und Löschen von fließt und Ändern der Berechtigungen für den Nachrichtenfluss. Informationen zur Überwachung für Workflowaktivitäten finden Sie im Blogbeitrag [Microsoft Fluss Überwachen von Ereignissen, die nun in Office 365-Sicherheit und Compliance Center verfügbar sind](https://flow.microsoft.com/blog/security-and-compliance-center).


### <a name="microsoft-stream"></a>Microsoft Stream
  
Sie können das Überwachungsprotokoll Aktivitäten in Microsoft Stream suchen. Hierzu zählen video Aktivitäten von Benutzer, Gruppe Channel Aktivitäten und Admin Aktivitäten wie Verwalten von Benutzern, Verwalten von Einstellungen der Organisation und Exportieren von Berichten. Eine Beschreibung dieser Aktivitäten finden Sie im Abschnitt "Aktivitäten protokolliert in Stream Microsoft" in [Überwachungsprotokollen in Microsoft Stream-Objekt](https://docs.microsoft.com/stream/audit-logs).
  
### <a name="exchange-admin-audit-log"></a>Exchange-Administrator-Überwachungsprotokoll
  
Exchange-Administrator-überwachungsprotokollierung – aktiviert, die standardmäßig in Office 365 – zeichnet ein Ereignis in das Überwachungsprotokoll Office 365, wenn ein Administrator (oder ein Benutzer mit Administratorberechtigungen zugewiesen wurde) in Ihrer Exchange Online-Organisation eine Änderung vornimmt. Mithilfe der Exchange-Verwaltungskonsole oder durch Ausführen eines Cmdlets in Windows PowerShell vorgenommenen Änderungen werden im Exchange Admin Audit Log protokolliert. Ausführlichere Informationen zu Admin überwachen Sie die Protokollierung in Exchange finden Sie [administratorüberwachungsprotokollierung](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Hier sind einige Tipps für die Suche nach Aktivität im Exchange Admin-Überwachungsprotokoll ein:
  
- Zum Zurückgeben von Einträgen aus dem Exchange Admin-Überwachungsprotokoll, müssen Sie **Ergebnisse für alle Aktivitäten** in der Liste der **Aktivitäten** aus. Verwenden Sie den Bereich Datumsfeldern und **der Benutzerliste** die Suchergebnisse für Cmdlets, die von einem bestimmten Exchange-Administrator innerhalb eines bestimmten Zeitraums ausgeführt werden können. 
    
- Zum Anzeigen von Ereignissen aus dem Exchange Admin-Überwachungsprotokoll Filtern der Suchergebnisse und Typ einen **-** (Strich) im Filterfeld **Aktivität** . Dadurch wird die Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange Admin-Ereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortiert werden. 
    
    ![Geben Sie einen Bindestrich im Aktivitäten zum Filtern von Exchange Admin-Ereignisse](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Zum Abrufen von Informationen über welche Cmdlet ausgeführt wurde, welche Parameter und Parameterwerte verwendet wurden und welche Objekte betroffen sind, müssen Sie die Suchergebnisse exportieren, und wählen Sie die Option **alle Ergebnisse herunterladen** . 
    
- Sie können Ereignisse auch mithilfe der Exchange-Verwaltungskonsole in der Exchange-administratorüberwachungsprotokoll anzeigen. Anweisungen finden Sie unter [administratorüberwachungsprotokoll anzeigen](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wo finde ich über die Features, die von der Überwachung in Office 365-Dienst angeboten?**

Weitere Informationen über die Überwachung und reporting Features in Office 365 finden Sie unter [Überwachung und Berichterstellung in Office 365](office-365-auditing-and-reporting-overview.md). 

**Was sind die verschiedenen Office 365-Dienste, die derzeit überwacht werden?**

Die am häufigsten verwendeten Office 365-Dienste wie Exchange Online, SharePoint, OneDrive, Azure Active Directory, Microsoft-Teams, CRM, erweiterte Threat Protection und Data Loss Prevention überwacht werden sollen. Siehe Abschnitt [Einführung](#search-the-audit-log-in-the-office-365-security-amp-compliance-center) in diesem Artikel finden Sie eine vollständige Liste.

**Welche Aktivitäten überwacht werden durch die Überwachung der Dienst in Office 365?**

Siehe Abschnitt [Löschvorgänge Aktivitäten](#audited-activities) in diesem Artikel finden Sie eine Liste und Beschreibung der Aktivitäten, die in Office 365 überwacht werden.

**Wie lange dauert es für einen auditing-Eintrag zur Verfügung stehen, nachdem ein Ereignis aufgetreten ist?**

Die meisten Überwachung von Daten innerhalb von 30 Minuten ist verfügbar, aber nach dem Auftreten eines Ereignisses für das entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt werden bis zu 24 Stunden dauern. Finden Sie in der Tabelle im Abschnitt [vor Beginn](#before-you-begin) dieses Artikels, die die Zeit anzeigt, die für Ereignisse in den verschiedenen Office 365-Diensten benötigt verfügbar sein soll.

**Wie lange werden für das Überwachungsprotokoll Datensätze beibehalten?**

Wie bereits erklärt hängt von der Aufbewahrungszeitraum für Audit Datensätze Office 365-Abonnement Ihrer Organisation.  

- **Office 365 E3** - Audit Datensätze 90 Tage lang aufbewahrt werden.

- **Office 365 E5** - Audit 365 Tage (ein Jahr) Datensätze aufbewahrt werden. Aufbewahren von Audit-Datensätze für ein Jahr ist auch für Organisationen, die ein Abonnement E3 und ein Office 365 erweiterte Compliance Add-on-Abonnement verfügen verfügbar.

     > [!NOTE]
     > Wie bereits erläutert, die einjährige Aufbewahrungsdauer für Audit-Datensätze für E5 (oder E3 Organisationen, die erweiterte Compliance Add-on Lizenzen haben) ist derzeit nur als Teil eines Programms private Preview. In diesem Vorschauprogramm zu registrieren, um Bitte Datei eine Anforderung mit [Microsoft-Support](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) und als Beschreibung der Sie Hilfe benötigen, sind: "Langfristige Office 365 Audit Log private Preview".

Beachten Sie außerdem, dass die Dauer des Aufbewahrungszeitraums für Audit Datensätze auf Benutzerebene Lizenzierung basiert. Beispielsweise wenn ein Benutzer in Ihrer Organisation eine Lizenz für Office 365 E3 zugewiesen ist, werden dann die Überwachungseinträge für Aktivitäten, die ausgeführt werden, die von diesem Benutzer 90 Tage lang aufbewahrt. Wenn ein anderer Benutzer eine Lizenz für Office 365 E5 zugewiesen ist, werden ihre Überwachungseinträge für ein Jahr beibehalten. 

**Kann ich die Überwachung von Daten programmgesteuert zugreifen?**

Ja. Die Office 365-Verwaltungs-Aktivität-API wird verwendet, um die Überwachungsprotokolle programmgesteuert abgerufen.  Zum Einstieg finden Sie unter [Erste Schritte mit Office 365-Management-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Gibt es andere Methoden, um die Protokolle an die Office 365-Sicherheit & Compliance Center oder die Office 365-Verwaltungs-Aktivität API Überwachung abrufen?**

Nein. Dies sind die nur zwei Methoden zum Abrufen von Daten aus dem Office 365-Überwachung-Dienst. 

**Müssen einzeln Aktivieren der Überwachung in alle Dienste, die ich für Überwachungsprotokolle erfassen möchten?**

In den meisten Office 365-Diensten ist standardmäßig aktiviert, nachdem Sie anfänglich Überwachung für Office 365-Organisation (wie im Abschnitt [bevor Sie beginnen:](#before-you-begin) in diesem Artikel beschrieben) aktivieren. Allerdings müssen Sie aktivieren Postfach Überwachung in Exchange Online für jedes Postfach, das Sie überwachen möchten.   Wir arbeiten zum Aktivieren der Überwachung von Postfächern in der Standardeinstellung für alle Postfächer in einer Office 365-Organisation. Weitere Informationen finden Sie unter "Überwachung von Exchange-Postfächern in der Standardeinstellung im [Blog des Microsoft Security, Privatsphäre und Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171)aktiviert wird".

**Deduplizierung der Office 365-Überwachung Servicesupport von Datensätzen?**

Nein. Pipeline für die Überwachung Service ist nahezu in Echtzeit und kann daher nicht Deduplizierung unterstützen.
 
**Werden Office 365 Überwachung von Daten werden über Landesgrenzen übergeben?**

Nein. Wir haben gerade Überwachung Pipeline Bereitstellungen NA (Nordamerika), EMEA (Europa, Naher Osten und Afrika) und "APAC" (Asien-Pazifik) Regionen. Jedoch können wir die Daten über diese Bereiche für den Lastenausgleich und nur während der live-Site Probleme übergeben. Wenn wir diese Aktivitäten ausführen, werden die Daten während der Übertragung verschlüsselt.   
 
**Ist die verschlüsselten Daten Überwachung?**

Überwachen von Daten wird in Exchange-Postfächern (Daten im Ruhezustand) im selben Bereich gespeichert, in der Pipeline für die Überwachung bereitgestellt wird. Diese Daten werden nicht verschlüsselt. Allerdings werden immer Daten während der Übertragung verschlüsselt. 













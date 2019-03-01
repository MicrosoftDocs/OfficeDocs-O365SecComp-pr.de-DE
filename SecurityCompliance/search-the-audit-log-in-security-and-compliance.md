---
title: Durchsuchen des Überwachungsprotokolls im Office 365 Security &amp; Compliance Center
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
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Verwenden Sie das Office 365 Security & Compliance Center, um das einheitliche Überwachungsprotokoll durchsuchen, um die Benutzer-und Administratoraktivitäten in Ihrer Office 365-Organisation anzuzeigen. '
ms.openlocfilehash: ac4ded889b913b2a090e4002f917ec06485948e1
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341776"
---
# <a name="search-the-audit-log-in-the-office-365-security--compliance-center"></a>Durchsuchen des Überwachungsprotokolls im Office 365 Security & Compliance Center

Sie müssen herausfinden, ob ein Benutzer ein bestimmtes Dokument angezeigt oder ein Element aus seinem Postfach gelöscht hat? In diesem Fall können Sie das Office 365 Security &amp; Compliance Center verwenden, um das einheitliche Überwachungsprotokoll durchsuchen, um die Benutzer-und Administratoraktivitäten in ihrer Office 365-Organisation anzuzeigen. Warum ein einheitliches Überwachungsprotokoll? Da Sie für die folgenden Arten von Benutzer-und Administratoraktivitäten in Office 365 suchen können:
  
- Benutzeraktivität in SharePoint Online und OneDrive for Business
    
- Benutzeraktivität in Exchange Online (Exchange-postfachüberwachungsprotokollierung)
    
    > [!IMPORTANT]
    > Die postfachüberwachungsprotokollierung muss für jedes Benutzerpostfach aktiviert sein, bevor die Benutzeraktivität in Exchange Online protokolliert wird. Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md).
  
- Administrator Aktivität in SharePoint Online
    
- Administrator Aktivität in Azure Active Directory (der Verzeichnisdienst für Office 365)
    
- Administrator Aktivität in Exchange Online (Exchange-Administrator-Überwachungsprotokollierung)
    
- Benutzer-und Administrator Aktivität in Sway
    
- eDiscovery-Aktivitäten im Office 365 Security & Compliance Center
    
- Benutzer-und Administrator Aktivität in Power BI
    
- Benutzer-und Administratoraktivitäten in Microsoft Teams

- Benutzer-und Administrator Aktivität in Dynamics 365
    
- Benutzer-und Administrator Aktivität in jammern
 
- Benutzer-und Administratoraktivitäten in Microsoft Flow
    
- Benutzer-und Administrator Aktivität in Microsoft Stream

- Analysten-und Administratoraktivitäten in Microsoft Workplace Analytics

- Benutzer-und Administrator Aktivität in PowerApps
    
   
## <a name="before-you-begin"></a>Bevor Sie beginnen

Lesen Sie unbedingt die folgenden Elemente, bevor Sie mit der Durchsuchung des Office 365-Überwachungsprotokolls beginnen.
  
- Sie (oder ein anderer Administrator) müssen zunächst die Überwachungsprotokollierung aktivieren, bevor Sie mit der Durchsuchung des Office 365-Überwachungsprotokolls beginnen können. Klicken Sie zum Aktivieren auf der Seite **Überwachungsprotokoll Suche** im Security &amp; Compliance Center auf **Aufzeichnung von Benutzer-und Administratoraktivitäten starten** . (Wenn dieser Link nicht angezeigt wird, wurde die Überwachung für Ihre Organisation aktiviert.) Nachdem Sie es aktiviert haben, wird eine Meldung angezeigt, die besagt, dass das Überwachungsprotokoll vorbereitet wird, und dass Sie eine Suche in ein paar Stunden nach Abschluss der Vorbereitung ausführen können. Sie müssen dies nur einmal tun. 
    
    > [!NOTE]
    > Wir sind dabei, die Überwachung standardmäßig zu aktivieren. Bis zu diesem Zeitpunkt können Sie ihn wie zuvor beschrieben aktivieren. 
  
- Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" verfügen, um das Office 365-Überwachungsprotokoll durchsuchen zu können. Diese Rollen werden standardmäßig den Rollengruppen "Compliance-Verwaltung" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Um einem Benutzer die Möglichkeit zu geben, das Office 365-Überwachungsprotokoll mit den Mindestberechtigungen zu durchsuchen, können Sie eine benutzerdefinierte Rollengruppe in Exchange Online erstellen, die Überwachungsprotokolle oder Überwachungsprotokoll Rollen der Ansicht hinzufügen und dann den Benutzer als Mitglied der neuen Rollengruppe hinzufügen. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Wenn Sie einem Benutzer die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" auf der Seite " **Berechtigungen** " im &amp; Security Compliance Center zuweisen, können Sie das Office 365-Überwachungsprotokoll nicht durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuweisen. Dies liegt daran, dass das zugrunde liegende Cmdlet zum Durchsuchen des Überwachungsprotokolls ein Exchange Online-Cmdlet ist. 
  
- Wenn eine überwachte Aktivität von einem Benutzer oder Administrator ausgeführt wird, wird ein Überwachungsdatensatz generiert und im Office 365-Überwachungsprotokoll für Ihre Organisation gespeichert. Die Dauer, die ein Überwachungsdatensatz aufbewahrt wird (und im Überwachungsprotokoll durchsuchbar ist), hängt von Ihrem Office 365-Abonnement und insbesondere vom Typ der Lizenz ab, die einem bestimmten Benutzer zugewiesen ist.

     - **Office 365 E3** -Überwachungsdatensätze werden für 90 Tage aufbewahrt. Das führt dazu, dass Sie das Überwachungsprotokoll nach Aktivitäten durchsuchen können, die innerhalb der letzten 90 Tage durchgeführt wurden.

     - **Office 365 E5** -Überwachungsdatensätze werden für 365 Tage (ein Jahr) aufbewahrt. Das führt dazu, dass Sie das Überwachungsprotokoll nach Aktivitäten durchsuchen können, die im letzten Jahr durchgeführt wurden. Das aufBewahren von Überwachungsdatensätzen für ein Jahr ist auch für Benutzer verfügbar, denen eine E3/Exchange Online-Plan 1-Lizenz zugewiesen ist und die über eine Office 365 Advanced Compliance-Add-on-Lizenz verfügt.

        > [!NOTE]
        > Die einjährige Aufbewahrungsdauer für Überwachungsdatensätze für E5-Organisationen (oder E3-Organisationen mit erweiterten Compliance-Add-on-Lizenzen) ist derzeit nur im Rahmen eines privaten Vorschau Programms verfügbar. Wenn Sie sich für dieses Vorschau Programm anmelden möchten, geben Sie eine Anforderung beim [Microsoft-Support](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) ein, und fügen Sie Folgendes als Beschreibung der benötigten Hilfe zu: "Long-term Office 365 Audit Log private Preview".

- Wenn Sie die Überwachungsprotokoll Suche in Office 365 für Ihre Organisation deaktivieren möchten, können Sie den folgenden Befehl in Remote-PowerShell ausführen, die mit Ihrer Exchange Online-Organisation verbunden ist:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Wenn Sie die Überwachungs Suche erneut aktivieren möchten, können Sie den folgenden Befehl in Exchange Online PowerShell ausführen:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Weitere Informationen finden Sie unter [Deaktivieren der Suche in einem Überwachungsprotokoll in Office 365](turn-audit-log-search-on-or-off.md).
    
- Wie bereits erwähnt, ist das zugrunde liegende Cmdlet, das zum Durchsuchen des Überwachungsprotokolls verwendet wird, ein Exchange Online-Cmdlet, das **Search-UnifiedAuditLog**ist. Daher können Sie dieses Cmdlet verwenden, um das Office 365-Überwachungsprotokoll zu durchsuchen, statt die Seite **Überwachungsprotokoll Suche** im &amp; Security Compliance Center zu verwenden. Sie müssen dieses Cmdlet in einer Remote-PowerShell ausführen, die mit Ihrer Exchange Online-Organisation verbunden ist. Weitere Informationen finden Sie unter [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Wenn Sie Daten programmgesteuert aus dem Office 365-Überwachungsprotokoll herunterladen möchten, wird empfohlen, die Office 365-Verwaltungs Aktivitäts-API anstelle eines PowerShell-Skripts zu verwenden. Die Office 365-Verwaltungs Aktivitäts-API ist ein REST-Webdienst, den Sie zum Entwickeln von Betriebs-, Sicherheits-und Compliance-Überwachungslösungen für Ihre Organisation verwenden können. Weitere Informationen finden Sie unter [Office 365 Management Activity API Reference](https://go.microsoft.com/fwlink/?linkid=852309).
    
- Es kann bis zu 30 Minuten oder bis zu 24 Stunden dauern, bis ein Ereignis eintritt, damit der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. Die folgende Tabelle zeigt die Zeit, die für die verschiedenen Dienste in Office 365 benötigt wird.
    
    |**Office 365-Dienste**|**30 Minuten**|**24 Stunden**|
    |:-----|:-----|:-----|
    |Advanced Threat Protection und Threat Intelligence  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (Benutzeranmelde Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (admin-Ereignisse)  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |Verhinderung von Datenverlust  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
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
    |SharePoint Online und OneDrive for Business  <br/> |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Yammer  <br/> ||![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (Azure AD) ist der Verzeichnisdienst für Office 365. Das vereinheitlichte Überwachungsprotokoll enthält Benutzer-, Gruppen-, Anwendungs-, Domänen-und Verzeichnis Aktivitäten, die im Office 365 Admin Center oder im Azure-Verwaltungsportal durchgeführt werden. Eine vollständige Liste der Azure AD-Ereignisse finden Sie unter [Azure Active Directory-Überwachungsbericht Ereignisse](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Exchange Online-Überwachungsprotokolle bestehen aus zwei Arten von Ereignissen: Exchange-Verwaltungsereignisse (von Administratoren ausgeführte Aktionen) und Post Fach Ereignisse (Aktionen, die von Benutzern in Postfächern ausgeführt werden). Beachten Sie, dass die postfachüberwachung nicht standardmäßig aktiviert ist. Sie muss für jedes Benutzerpostfach aktiviert werden, bevor nach Post Fach Ereignissen im Office 365-Überwachungsprotokoll gesucht werden kann. Weitere Informationen zur postfachüberwachung und zu den protokollierten Post Fach Überwachungsaktionen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md).
    
- Die Überwachungsprotokollierung für Power BI ist nicht standardmäßig aktiviert. Um nach Power BI-Aktivitäten im Office 365-Überwachungsprotokoll zu suchen, müssen Sie die Überwachung im Power BI Admin-Portal aktivieren. Anweisungen finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI Admin Portal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
    
    
## <a name="search-the-audit-log"></a>Durchsuchen des Überwachungsprotokolls

Hier finden Sie den Prozess zum Durchsuchen des Überwachungsprotokolls in Office 365.
  
[Schritt 1: Ausführen einer Überwachungsprotokoll Suche](#step-1-run-an-audit-log-search)
  
[Schritt 2: Anzeigen der Suchergebnisse](#step-2-view-the-search-results)

[Schritt 3: Filtern der Suchergebnisse](#step-3-filter-the-search-results)

[Schritt 4: Exportieren der Suchergebnisse in eine Datei](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Schritt 1: Ausführen einer Überwachungsprotokoll Suche

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Verwenden Sie eine private Browsersitzung (keine reguläre Sitzung) für den Zugriff auf das Office &amp; 365 Security Compliance Center, da dadurch die Anmeldeinformationen, mit denen Sie derzeit angemeldet sind, nicht verwendet werden. Drücken Sie STRG + UMSCHALT + P, um eine inPrivate-Browsing-Sitzung in Internet Explorer oder Microsoft Edge zu öffnen. Drücken Sie STRG + UMSCHALT + N, um eine private Browsersitzung in Google Chrome (als inkognito-Fenster bezeichnet) zu öffnen. 
  
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Such &amp; Prüfung**, und klicken Sie dann auf **Überwachungsprotokoll Suche**.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
    ![Konfigurieren Sie Kriterien, und klicken Sie dann auf suchen, um Bericht auszuführen.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Sie müssen zuerst die Überwachungsprotokollierung aktivieren, bevor Sie eine Überwachungsprotokoll Suche ausführen können. Wenn der Link **Benutzer-und Administrator Aktivität starten** angezeigt wird, klicken Sie darauf, um die Überwachung zu aktivieren. Wenn dieser Link nicht angezeigt wird, wurde die Überwachung für Ihre Organisation aktiviert. 
  
4. Konfigurieren Sie die folgenden Suchkriterien:
    
    a. **Aktivitäten** klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Benutzer-und Administratoraktivitäten sind in Gruppen verwandter Aktivitäten organisiert. Sie können bestimmte Aktivitäten auswählen oder auf den Namen der Aktivitätsgruppe klicken, um alle Aktivitäten in der Gruppe auszuwählen. Sie können auch auf eine ausgewählte Aktivität klicken, um die Auswahl zu löschen. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungsprotokolleinträge für die ausgewählten Aktivitäten angezeigt. Wenn Sie **Ergebnisse für alle Aktivitäten anzeigen** auswählen, werden die Ergebnisse für alle Aktivitäten angezeigt, die vom ausgewählten Benutzer oder einer Benutzergruppe ausgeführt werden. 
    
    Mehr als 100 Benutzer-und Administratoraktivitäten werden im Office 365-Überwachungsprotokoll protokolliert. Klicken Sie zum Thema dieses Artikels auf die Registerkarte "über **wachte Aktivitäten** ", um die Beschreibungen jeder Aktivität in den verschiedenen Office 365-Diensten anzuzeigen. 
    
    b. **Start Datum** und **Enddatum** die letzten sieben Tage sind standardmäßig ausgewählt. Wählen Sie einen Datums-und Uhrzeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Datum und Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Zeitraum, den Sie angeben können, beträgt 90 Tage. Wenn der ausgewählte Datumszeitraum größer als 90 Tage ist, wird ein Fehler angezeigt. 
    
    > [!TIP]
    > Wenn Sie den maximalen Datumswert von 90 Tagen verwenden, wählen Sie die aktuelle Uhrzeit für das **Start Datum**aus. Andernfalls erhalten Sie eine Fehlermeldung, dass das Startdatum vor dem Enddatum liegt. Wenn Sie die Überwachung innerhalb der letzten 90 Tage aktiviert haben, kann der maximale Datumsbereich nicht vor dem Datum beginnen, an dem die Überwachung aktiviert wurde. 
  
    c. **Benutzer** klicken in dieses Feld und wählen dann einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. Die Überwachungsprotokolleinträge für die ausgewählte Aktivität, die von den Benutzern, die Sie in diesem Feld ausgewählt haben, ausgeführt werden, werden in der Ergebnisliste angezeigt. Lassen Sie dieses Feld leer, um Einträge für alle Benutzer (und Dienstkonten) in Ihrer Organisation zurückzugeben. 
    
    d. **Datei, Ordner oder Website** geben Sie einen oder alle Datei-oder Ordnernamen ein, um nach Aktivitäten im Zusammenhang mit der Ordner Datei zu suchen, die das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Wenn Sie eine URL verwenden, stellen Sie sicher, dass Sie den vollständigen URL-Pfad eingeben, oder geben Sie nur einen Teil der URL ein, und schließen Sie keine Sonderzeichen oder Leerzeichen ein. 
    
    Lassen Sie dieses Feld leer, um Einträge für alle Dateien und Ordner in Ihrer Organisation zurückzugeben.
    
    > [!TIP]
    > Wenn Sie nach allen Aktivitäten im Zusammenhang mit einer **Website**suchen, fügen Sie das Platz\*Halter Symbol () nach der URL hinzu, um alle Einträge für diese Website zurückzugeben. Beispiel: **https://contoso-my.sharepoint.com/personal/"*"**.
    
5. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 
    
    Die Suchergebnisse werden geladen, und nach ein paar Augenblicken werden Sie unter **Ergebnisse**angezeigt. Wenn die Suche abgeschlossen ist, wird die Anzahl der gefundenen Ergebnisse angezeigt. Beachten Sie, dass im **Ergebnis** Bereich in schritten von 150 ereignissen maximal 5.000 Ereignisse angezeigt werden. Wenn mehr als 5.000 Ereignisse den Suchkriterien entsprechen, werden die neuesten 5.000-Ereignisse angezeigt. 
    
    ![Die Anzahl der Ergebnisse wird angezeigt, nachdem die Suche abgeschlossen ist.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Tipps zum Durchsuchen des Überwachungsprotokolls

- Sie können bestimmte Aktivitäten auswählen, nach denen Sie suchen möchten, indem Sie auf den Aktivitätsnamen klicken. Sie können auch nach allen Aktivitäten in einer Gruppe (beispielsweise **Datei-und Ordner Aktivitäten**) suchen, indem Sie auf den Gruppennamen klicken. Wenn eine Aktivität ausgewählt ist, können Sie darauf klicken, um die Auswahl abzubrechen. Sie können auch das Suchfeld verwenden, um die Aktivitäten anzuzeigen, die das von Ihnen eingegebene Stichwort enthalten.
    
    ![Klicken Sie auf Aktivitätsgruppen Name, um alle Aktivitäten auszuwählen.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Sie müssen in der Liste **Aktivitäten** die Option **Ergebnisse für alle Aktivitäten anzeigen** auswählen, um Ereignisse aus dem Exchange-administratorüberwachungsprotokoll anzuzeigen. Ereignisse in diesem Überwachungsprotokoll zeigen einen Cmdlet-Namen (beispielsweise **Set-Mailbox** ) in der Spalte **Activity** in den Ergebnissen an. Weitere Informationen finden Sie, wenn Sie auf die Registerkarte über **wachte Aktivitäten** in diesem Thema klicken und dann auf **Exchange-Verwaltungsaktivitäten**klicken.
    
    Entsprechend gibt es einige Überwachungsaktivitäten, die kein entsprechendes Element in der Liste **Aktivitäten** enthalten. Wenn Sie den Namen des Vorgangs für diese Aktivitäten kennen, können Sie nach allen Aktivitäten suchen und dann die Ergebnisse filtern, indem Sie den Namen des Vorgangs in das Feld für die Spalte **Aktivität** eingeben. Weitere Informationen zum Filtern der Ergebnisse finden Sie unter [Schritt 3: Filtern der Suchergebnisse](#step-3-filter-the-search-results) . 
    
- Klicken Sie auf **Löschen** , um die aktuellen Suchkriterien zu löschen. Der Datumsbereiche gibt den Standardwert der letzten sieben Tage zurück. Sie können auch auf **Alle löschen klicken, um die Ergebnisse für alle Aktivitäten anzuzeigen** , um alle ausgewählten Aktivitäten abzubrechen. 
    
- Wenn 5.000 Ergebnisse gefunden werden, können Sie wahrscheinlich davon ausgehen, dass es mehr als 5.000 Ereignisse gibt, die den Suchkriterien entsprechen. Sie können entweder die Suchkriterien verfeinern und die Suche erneut ausführen, um weniger Ergebnisse zurückzugeben, oder Sie können alle Suchergebnisse exportieren, indem Sie die Option **Ergebnisse** \> **herunterladen alle Ergebnisse**auswählen.

  
### <a name="step-2-view-the-search-results"></a>Schritt 2: Anzeigen der Suchergebnisse

Die Ergebnisse einer Überwachungsprotokoll Suche werden unter **Ergebnisse** auf der Seite **Überwachungsprotokoll Suche** angezeigt. Wie bereits erwähnt, werden maximal 5.000 (neueste) Ereignisse in Schritten von 150 Ereignissen angezeigt. Um weitere Ereignisse anzuzeigen, können Sie die Bildlaufleiste im **Ergebnis** Bereich verwenden, oder Sie können **Umschalt + Ende** drücken, um die nächsten 150-Ereignisse anzuzeigen. 
  
Die Ergebnisse enthalten die folgenden Informationen zu jedem von der Suche zurückgegebenen Ereignis.
  
- **Date:** Das Datum und die Uhrzeit (im UTC-Format), als das Ereignis aufgetreten ist. 
    
- **IP-Adresse:** Die IP-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. Die IP-Adresse wird in einem IPv4-oder IPv6-Adressformat angezeigt. 
    
- **Benutzer:** Der Benutzer (oder das Dienstkonto), der die Aktion ausgeführt hat, die das Ereignis ausgelöst hat. 
    
- **Aktivität:** Die vom Benutzer ausgeführte Aktivität. Dieser Wert entspricht den Aktivitäten, die Sie in der Dropdownliste **Aktivitäten** ausgewählt haben. Bei einem Ereignis aus dem Exchange-administratorüberwachungsprotokoll ist der Wert in dieser Spalte ein Exchange-Cmdlet. 
    
- **Element:** Das Objekt, das als Ergebnis der entsprechenden Aktivität erstellt oder geändert wurde. Beispielsweise die Datei, die angezeigt oder geändert wurde, oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben einen Wert in dieser Spalte. 
    
- **Detail:** Weitere Details zu einer Aktivität. Auch hier haben nicht alle Aktivitäten einen Wert. 
    
> [!TIP]
> Klicken Sie unter **Ergebnisse** auf eine Spaltenüberschrift, um die Ergebnisse zu sortieren. Sie können die Ergebnisse von A bis Z oder Z in A sortieren. Klicken Sie auf die Kopfzeile **Datum** , um die Ergebnisse von der ältesten nach neuesten oder neuesten in die älteste zu sortieren. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Anzeigen der Details für ein bestimmtes Ereignis

Sie können weitere Details zu einem Ereignis anzeigen, indem Sie in der Liste der Suchergebnisse auf den Ereigniseintrag klicken. Es wird eine **Detail** Seite mit detaillierten Eigenschaften aus dem Ereignisdatensatz angezeigt. Welche Eigenschaften angezeigt werden, hängt vom Office 365-Dienst ab, in dem das Ereignis auftritt. Klicken Sie auf **Weitere Informationen**, um diese Details anzuzeigen. Beschreibungen finden Sie unter [detaillierte Eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
![Klicken Sie auf Weitere Informationen, um die detaillierten Eigenschaften des Überwachungsprotokoll-Ereignisdatensatzes anzuzeigen.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern der Suchergebnisse

Zusätzlich zur Sortierung können Sie auch die Ergebnisse einer Überwachungsprotokoll Suche filtern. Dies ist eine hervorragende Funktion, mit der Sie die Ergebnisse für einen bestimmten Benutzer oder eine bestimmte Aktivität schnell filtern können. Sie können zunächst eine breite Suche erstellen und dann schnell die Ergebnisse filtern, um bestimmte Ereignisse anzuzeigen. Dann können Sie die Suchkriterien einschränken und die Suche erneut ausführen, um eine kleinere, übersichtlichere Ergebnismenge zurückzugeben.
  
So filtern Sie die Ergebnisse
  
1. Führen Sie eine Überwachungsprotokoll Suche aus.
    
2. Wenn die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse filtern**.
    
    Stichwort Felder werden unter jeder Spaltenüberschrift angezeigt.
    
3. Klicken Sie auf eines der Felder unter einer Spaltenüberschrift, und geben Sie je nach der Spalte, nach der gefiltert werden soll, ein Wort oder einen Ausdruck ein. Die Ergebnisse werden dynamisch angepasst, um die Ereignisse anzuzeigen, die dem Filter entsprechen.
    
    ![Geben Sie ein Wort in Filter ein, um die Ereignisse anzuzeigen, die dem Filter entsprechen.](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Wenn Sie einen Filter löschen möchten, klicken Sie im Feld Filter auf das **X** , oder klicken Sie einfach auf **Filterung ausblenden**.
    
> [!TIP]
> Zum Anzeigen von Ereignissen aus dem Exchange-Administrator-Überwachungsprotokoll **-** geben Sie im Feld **Aktivitäts** Filter einen (Strich) ein. Dadurch werden die Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Verwaltungsereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortieren. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Schritt 4: Exportieren der Suchergebnisse in eine Datei

Sie können die Ergebnisse einer Überwachungsprotokoll Suche in eine CSV-Datei (Comma Separated Value) auf Ihrem lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und Features wie suchen, sortieren, Filtern und Aufteilen einer einzelnen Spalte (die mehrwertige Zellen enthält) in mehrere Spalten verwenden.
  
1. Führen Sie eine Überwachungsprotokoll Suche aus, und überprüfen Sie dann die Suchkriterien, bis Sie die gewünschten Ergebnisse erhalten haben.
    
2. Klicken Sie auf **Ergebnisse exportieren** , und wählen Sie eine der folgenden Optionen aus: 
    
  - **Geladene Ergebnisse speichern** Wählen Sie diese Option aus, um nur die Einträge zu exportieren, die unter **Ergebnisse** auf der Seite * * Überwachungsprotokoll Suche * * angezeigt werden. Die heruntergeladene CSV-Datei enthält die gleichen Spalten (und Daten), die auf der Seite angezeigt werden (Datum, Benutzer, Aktivität, Element und Details). In der CSV-Datei ist eine zusätzliche Spalte mit dem Namen **more**enthalten, die weitere Informationen aus dem Überwachungsprotokolleintrag enthält. Da Sie die gleichen Ergebnisse exportieren, die auf der Seite **Überwachungsprotokoll Suche** geladen (und angezeigt) werden, werden maximal 5.000 Einträge exportiert. 
    
  - **Alle Ergebnisse herunterladen** Wählen Sie diese Option aus, um alle Einträge aus dem Office 365-Überwachungsprotokoll zu exportieren, die den Suchkriterien entsprechen. Wählen Sie diese Option aus, um alle Einträge aus dem Überwachungsprotokoll neben den 5.000-Ergebnissen herunterzuladen, die auf der Seite für die **Überwachungsprotokoll Suche** angezeigt werden können. Mit dieser Option werden die Rohdaten aus dem Überwachungsprotokoll in eine CSV-Datei heruntergeladen und zusätzliche Informationen aus dem Überwachungsprotokolleintrag in einer Spalte mit dem Namen **Auditdata**. Es kann länger dauern, bis Sie die Datei herunterladen, wenn Sie diese Exportoption wählen, da die Datei viel größer sein kann als diejenige, die heruntergeladen wird, wenn Sie die Option andere auswählen.
    
    > [!IMPORTANT]
    > Sie können maximal 50.000 Einträge in eine CSV-Datei aus einer einzelnen Überwachungsprotokoll Suche herunterladen. Wenn 50.000-Einträge in die CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass es mehr als 50.000 Ereignisse gibt, die die Suchkriterien erfüllen. Wenn Sie mehr als diesen Grenzwert exportieren möchten, verwenden Sie einen Datumsbereich, um die Anzahl der Überwachungsprotokolleinträge zu reduzieren. Möglicherweise müssen Sie mehrere Suchvorgänge mit kleineren Datumsbereichen ausführen, um mehr als 50.000 Einträge zu exportieren. 
  
3. Nachdem Sie eine Exportoption ausgewählt haben, wird unten im Fenster eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen, im Ordner "Downloads" zu speichern oder in einem bestimmten Ordner zu speichern.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>Weitere Informationen zum Exportieren von Überwachungsprotokoll-Suchergebnissen

- Die Option **alle Ergebnisse herunterladen** downloadet die Rohdaten aus dem Office 365-Überwachungsprotokoll in eine CSV-Datei. Diese Datei enthält unterschiedliche Spaltennamen (CreationDate, UserIds, Operation, AuditData) als die Datei, die heruntergeladen wird, wenn Sie die Option geladene **Ergebnisse speichern** auswählen. Die Werte in den beiden unterschiedlichen CSV-Dateien für dieselbe Aktivität können ebenfalls unterschiedlich sein. Beispiel: die Aktivität in der Spalte " **Aktion** " in der CSV-Datei und möglicherweise einen anderen Wert als die benutzerfreundliche Version, die in der Spalte " **Aktivität** " auf der Suchseite für das **Überwachungsprotokoll** angezeigt wird; Beispiel: Mailbox Login: vs. User angemeldet bei Mailbox.
    
- Wenn Sie alle Ergebnisse herunterladen, enthält die CSV-Datei eine Spalte mit dem Namen **Auditdata**, die zusätzliche Informationen zu den einzelnen Ereignissen enthält. Wie bereits erwähnt, enthält diese Spalte eine mehrwertige Eigenschaft für mehrere Eigenschaften aus dem Überwachungsprotokolldaten Satz. Jedes der **Property: Value** -Paare in dieser mehrwertigen Eigenschaft werden durch ein Komma getrennt. Sie können die Power-Abfrage in Excel verwenden, um diese Spalte in mehrere Spalten aufzuteilen, sodass jede Eigenschaft eine eigene Spalte hat. Auf diese Weise können Sie eine oder mehrere dieser Eigenschaften sortieren und filtern. Weitere Informationen hierzu finden Sie im Abschnitt "Split a Column by Delimiter" unter [Split a Column of Text (Power Query)](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662).
    
    Nachdem Sie die **Auditdata** -Spalte geteilt haben, können Sie nach der Spalte **Vorgänge** filtern, um die detaillierten Eigenschaften für einen bestimmten Aktivitätstyp anzuzeigen. 
    
- Es gibt eine 3.060-Zeichen Grenze für die Daten, die im Feld **Auditdata** für einen Überwachungsdatensatz angezeigt werden. Wenn die 3.060-Zeichen Grenze überschritten wird, werden die Daten in diesem Feld abgeschnitten. 
    
- Wenn Sie alle Ergebnisse aus einer Suchabfrage herunterladen, die Ereignisse aus verschiedenen Office 365-Diensten enthält, enthält die Spalte **Auditdata** in der CSV-Datei unterschiedliche Eigenschaften, je nachdem, in welchem Dienst die Aktion ausgeführt wurde. Beispielsweise enthält Einträge aus Exchange-und Azure AD-Überwachungsprotokollen eine Eigenschaft mit dem Namen **ResultStatus** , die angibt, ob die Aktion erfolgreich war oder nicht. Diese Eigenschaft ist für Ereignisse in SharePoint nicht enthalten. Entsprechend verfügen SharePoint-Ereignisse über eine Eigenschaft, die die Website-URL für Datei-und Ordner bezogene Aktivitäten identifiziert. Um dieses Verhalten zu verringern, sollten Sie verschiedene Suchvorgänge verwenden, um die Ergebnisse für Aktivitäten aus einem einzelnen Dienst zu exportieren. 
    
    Eine Beschreibung der Eigenschaften, die in der **Auditdata** -Spalte in der CSV-Datei aufgeführt sind, wenn Sie alle Ergebnisse herunterladen, und der jeweilige Dienst gilt, finden Sie unter [detaillierte eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>ÜberWachte Aktivitäten

In den Tabellen in diesem Abschnitt werden die in Office 365 überwachten Aktivitäten beschrieben. Sie können nach diesen Ereignissen suchen, indem Sie das Überwachungsprotokoll im Security & Compliance Center durchsuchen.
  
Diese Tabellen Gruppieren verwandte Aktivitäten oder Aktivitäten von einem bestimmten Office 365-Dienst. Die Tabellen enthalten den Anzeigenamen, der in der Dropdownliste **Aktivitäten** angezeigt wird, sowie den Namen des entsprechenden Vorgangs, der in den detaillierten Informationen eines Überwachungsdatensatzes und in der CSV-Datei angezeigt wird, wenn Sie die Suchergebnisse exportieren. Beschreibungen der detaillierten Informationen finden Sie unter [detaillierte Eigenschaften im Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).
  
Klicken Sie auf einen der folgenden Links, um zu einer bestimmten Tabelle zu wechseln.
  
||||
|:-----|:-----|:-----|
|[Datei-und Seiten Aktivitäten](#file-and-page-activities)<br/> |[Ordner Aktivitäten](#folder-activities)<br/> |[Freigabe-und Zugriffs Anforderungs Aktivitäten](#sharing-and-access-request-activities)<br/> |
|[Synchronisierungsaktivitäten](#synchronization-activities)<br/> |[Aktivitäten der Websiteverwaltung](#site-administration-activities)<br/> |[Exchange-Postfachaktivitäten](#exchange-mailbox-activities)<br/> |
|[Aufbewahrungsrichtlinie und Bezeichnungs Aktivitäten](#retention-policy-and-label-activities) <br/>|[Sway-Aktivitäten](#sway-activities) <br/> |[Benutzer Verwaltungsaktivitäten](#user-administration-activities) <br/> 
|[Verwaltungsaktivitäten der Azure AD-Gruppe](#azure-ad-group-administration-activities) <br/> |[Aktivitäten der Anwendungsverwaltung](#application-administration-activities) <br/> |[Rollen Verwaltungsaktivitäten](#role-administration-activities) <br/> |
|[Aktivitäten der Verzeichnisverwaltung](#directory-administration-activities) <br/> |[eDiscovery-Aktivitäten](#ediscovery-activities) <br/> |[Power BI-Aktivitäten](#power-bi-activities) <br/> |
|[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)<br/>|[Microsoft Teams-Aktivitäten](#microsoft-teams-activities) <br/> |[Aktivitäten mit jammern](#yammer-activities) <br/> |
[Microsoft Flow](#microsoft-flow) <br/> |[Microsoft PowerApps](#microsoft-powerapps)<br/>|[Microsoft Stream](#microsoft-stream) <br/>|
|[Exchange-Verwaltungsaktivitäten](#exchange-admin-audit-log)<br/>
||||
   
  
### <a name="file-and-page-activities"></a>Datei-und Seiten Aktivitäten
  
In der folgenden Tabelle werden die Datei-und Seiten Aktivitäten in SharePoint Online und OneDrive for Business beschrieben.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Datei mit Zugriff  <br/> |FileAccessed  <br/> |Benutzer-oder Systemkonto greift auf eine Datei zu.  <br/> |
|keine  <br/> |FileAccessedExtended  <br/> |Dies bezieht sich auf die Aktivität "Zugriff auf Datei" (fileAccessed). Ein FileAccessedExtended-Ereignis wird protokolliert, wenn dieselbe Person ständig auf eine Datei über einen längeren Zeitraum (bis zu 3 Stunden) zugreift. Der Zweck der Protokollierung von FileAccessedExtended-Ereignissen besteht darin, die Anzahl von fileAccessed-Ereignissen zu verringern, die protokolliert werden, wenn auf eine Datei ständig zugegriffen wird. Dadurch wird das Rauschen mehrerer fileAccessed-Datensätze für die im Wesentlichen dieselbe Benutzeraktivität reduziert, und Sie können sich auf das anfängliche (und noch wichtigere) fileAccessed-Ereignis konzentrieren.  <br/> |
|Eingecheckt  <br/> |FileCheckedin  <br/> |Der Benutzer checkt ein Dokument ein, das er aus einer Dokumentbibliothek ausgecheckt hat.  <br/> |
|Ausgecheckte Datei  <br/> |FileChecked  <br/> |Der Benutzer checkt ein Dokument aus einer Dokumentbibliothek aus. Benutzer können Dokumente auschecken und ändern, die für Sie freigegeben wurden.  <br/> |
|Kopierte Datei  <br/> |FileCopied  <br/> |Ein Benutzer kopiert ein Dokument von einer Website. Die kopierte Datei kann in einem anderen Ordner auf der Website gespeichert werden.  <br/> |
|Gelöschte Datei  <br/> |FileDeleted  <br/> |Ein Benutzer löscht ein Dokument von einer Website.  <br/> |
|Gelöschte Datei aus dem Papierkorb  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem Papierkorb einer Website.  <br/> |
|Gelöschte Datei aus dem endgültigen Papierkorb  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Der Benutzer löscht eine Datei aus dem endgültigen Papierkorb einer Website.  <br/> |
|Erkannte Schadsoftware in der Datei  <br/> |FileMalwareDetected  <br/> |Das SharePoint-Antivirus-Modul erkennt Schadsoftware in einer Datei.  <br/> |
|Auschecken verworfener Dateien  <br/> |FileCheckOutDiscarded  <br/> |Benutzer verwirft eine ausgecheckte Datei, oder macht dies rückgängig. Alle Änderungen, die an der Datei vorgenommen wurden, als sie ausgecheckt war, werden verworfen und nicht in der Dokumentversion in der Dokumentbibliothek gespeichert.  <br/> |
|HeruntergeLadene Datei  <br/> |FileDownloaded  <br/> |Ein Benutzer lädt ein Dokument von einer Website herunter.  <br/> |
|Geänderte Datei  <br/> |FileModified  <br/> |Benutzer-oder Systemkonto ändert den Inhalt oder die Eigenschaften eines Dokuments, das sich auf einer Website befindet.  <br/> |
|keine  <br/> |FileModifiedExtended  <br/> |Dies bezieht sich auf die "geänderte Datei" (fileModified)-Aktivität. Ein FileModifiedExtended-Ereignis wird protokolliert, wenn dieselbe Person ständig eine Datei für einen längeren Zeitraum (bis zu 3 Stunden) ändert. Der Zweck der Protokollierung von FileModifiedExtended-Ereignissen besteht darin, die Anzahl der fileModified-Ereignisse zu verringern, die protokolliert werden, wenn eine Datei ständig geändert wird. Dadurch wird das Rauschen mehrerer fileModified-Datensätze für die im Wesentlichen dieselbe Benutzeraktivität reduziert, und Sie können sich auf das anfängliche (und noch wichtigere) fileModified-Ereignis konzentrieren.  <br/> |
|Verschobene Datei  <br/> |FileMoved  <br/> |Ein Benutzer verschiebt ein Dokument von seinem aktuellen Speicherort auf einer Website an einen neuen Speicherort.  <br/> |
|Alle Nebenversionen der Datei werden wieder verwendet.  <br/> |FileVersionsAllMinorsRecycled  <br/> |Der Benutzer löscht alle Nebenversionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Alle Dateiversionen wurden recycelt  <br/> |FileVersionsAllRecycled  <br/> |Der Benutzer löscht alle Versionen aus dem Versionsverlauf einer Datei. Die gelöschten Versionen werden in den Papierkorb der Website verschoben.  <br/> |
|Recycelte Version der Datei  <br/> |FileVersionRecycled  <br/> |Der Benutzer löscht eine Version aus dem Versionsverlauf einer Datei. Die gelöschte Version wird in den Papierkorb der Website verschoben.  <br/> |
|UmBenannte Datei  <br/> |FileRenamed  <br/> |Der Benutzer benennt ein Dokument auf einer Website um.  <br/> |
|Wiederhergestellte Datei  <br/> |FileRestored  <br/> |Der Benutzer stellt ein Dokument aus dem Papierkorb einer Website wieder her.  <br/> |
|HochgeLadene Datei  <br/> |File uploaded  <br/> |Ein Benutzer lädt ein Dokument in einen Ordner auf einer Website hoch.  <br/> |
|Angezeigte Seite  <br/> |Seitenzugriffe  <br/> |Benutzer zeigt eine Seite auf einer Website an. Hierzu gehört nicht die Verwendung eines Webbrowsers zum Anzeigen von Dateien in einer Dokumentbibliothek.  <br/> |
|keine  <br/> |PageViewedExtended  <br/> |Dies bezieht sich auf die "viewed page"-Aktivität. Ein PageViewedExtended-Ereignis wird protokolliert, wenn dieselbe Person ständig eine Webseite für einen längeren Zeitraum (bis zu 3 Stunden) anzeigt. Der Zweck der Protokollierung von PageViewedExtended-Ereignissen besteht darin, die Anzahl der aufgetretenen Ereignisse zu verringern, die protokolliert werden, wenn eine Seite ständig angezeigt wird. Dies trägt dazu bei, das Rauschen von mehreren aufgegebenen Datensätzen für die im Wesentlichen dieselbe Benutzeraktivität zu reduzieren, und Sie können sich auf das anfängliche (und noch wichtigere) geteilte Ereignis konzentrieren.  <br/> |
||||
  
### <a name="folder-activities"></a>Ordner Aktivitäten
  
In der folgenden Tabelle werden die Ordner Aktivitäten in SharePoint Online und OneDrive for Business beschrieben.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Kopierter Ordner  <br/> |FolderCopied  <br/> |Der Benutzer kopiert einen Ordner von einer Website an einen anderen Speicherort in SharePoint oder OneDrive for Business.  <br/> |
|Erstellter Ordner  <br/> |FolderCreated  <br/> |Der Benutzer erstellt einen Ordner auf einer Website.  <br/> |
|Gelöschter Ordner  <br/> |FolderDeleted  <br/> |Ein Benutzer löscht einen Ordner von einer Website.  <br/> |
|Gelöschter Ordner aus dem Papierkorb  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Ein Benutzer löscht einen Ordner aus dem Papierkorb auf einer Website.  <br/> |
|Gelöschter Ordner aus dem endgültigen Papierkorb  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Ein Benutzer löscht einen Ordner aus dem endgültigen Papierkorb auf einer Website.  <br/> |
|Geänderter Ordner  <br/> |FolderModified  <br/> |Der Benutzer ändert einen Ordner auf einer Website. Dazu gehört das Ändern der Ordnermetadaten wie das Ändern von Tags und Eigenschaften.  <br/> |
|Verschobener Ordner  <br/> |FolderMoved  <br/> |Der Benutzer verschiebt einen Ordner an einen anderen Speicherort auf einer Website.  <br/> |
|UmBenannter Ordner  <br/> |FolderRenamed  <br/> |Der Benutzer benennt einen Ordner auf einer Website um.  <br/> |
|Wiederhergestellter Ordner  <br/> |FolderRestored  <br/> |Der Benutzer stellt einen gelöschten Ordner aus dem Papierkorb auf einer Website wieder her.  <br/> |
||||
  
### <a name="sharing-and-access-request-activities"></a>Freigabe-und Zugriffs Anforderungs Aktivitäten
  
In der folgenden Tabelle werden die Benutzer Freigabe-und Zugriffs Anforderungs Aktivitäten in SharePoint Online und OneDrive for Business beschrieben. Bei Freigabe Ereignissen identifiziert die **Detail** Spalte unter **Ergebnisse** den Namen des Benutzers oder der Gruppe, für die das Element freigegeben wurde, und gibt an, ob dieser Benutzer oder diese Gruppe Mitglied oder Gast in Ihrer Organisation ist. Weitere Informationen finden Sie unter [Verwenden der Freigabe Überwachung im Office 365-Überwachungsprotokoll](use-sharing-auditing.md).
  
> [!NOTE]
> Benutzer können auf Basis der usertype-Eigenschaft des User-Objekts entweder *Mitglieder* oder *Gäste* sein. Bei einem Mitglied handelt es sich normalerweise um einen Mitarbeiter, und ein Gast ist normalerweise außerhalb Ihres Unternehmens ein Mitarbeiter. Wenn ein Benutzer eine Freigabeeinladung akzeptiert (und nicht bereits Teil Ihrer Organisation ist), wird im Verzeichnis Ihrer Organisation ein Gastkonto erstellt. Sobald der Gastbenutzer über ein Konto in Ihrem Verzeichnis verfügt, können Ressourcen direkt mit diesen freigegeben werden (ohne dass eine Einladung erforderlich ist). 
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Akzeptierte Zugriffsanforderungen  <br/> |AccessRequestAccepted  <br/> |Eine Zugriffsanforderung für eine Website, einen Ordner oder ein Dokument wurde akzeptiert, und dem anfordernden Benutzer wurde der Zugriff erteilt.  <br/> |
|Akzeptierte Freigabeeinladung  <br/> |SharingInvitationAccepted  <br/> |Benutzer (Mitglied oder Gast) akzeptierte eine Freigabeeinladung und erhielt Zugriff auf eine Ressource. Dieses Ereignis enthält Informationen über den Benutzer, der eingeladen wurde, und die e-Mail-Adresse, die zum Annehmen der Einladung verwendet wurde (Sie können unterschiedlich sein). Diese Aktivität wird häufig durch ein zweites Ereignis begleitet, das beschreibt, wie dem Benutzer der Zugriff auf die Ressource gewährt wurde, beispielsweise das Hinzufügen des Benutzers zu einer Gruppe, die Zugriff auf die Ressource hat.  <br/> |
|Berechtigungsstufe zur Websitesammlung HinzugeFügt  <br/> |PermissionLevelAdded  <br/> |Einer Websitesammlung wurde eine Berechtigungsstufe hinzugefügt.  <br/> |
|Benutzer zu Secure Link hinzugefügt  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die diesen sicheren Freigabe Link verwenden können.  <br/> |
|Blockierte Freigabeeinladung  <br/> |SharingInvitationBlocked  <br/> | Eine Freigabeeinladung, die von einem Benutzer in Ihrer Organisation gesendet wurde, wird aufgrund einer externen Freigaberichtlinie blockiert, durch die die externe Freigabe basierend auf der Domäne des Zielbenutzers zugelassen oder verweigert wird. In diesem Fall wurde die Freigabeeinladung blockiert, weil:<br/>  Die Domäne des Zielbenutzers ist nicht in der Liste der zulässigen Domänen enthalten.  <br/>  Oder  <br/>  Die Domäne des Zielbenutzers ist in der Liste der blockierten Domänen enthalten.  <br/>  Weitere Informationen zum Zulassen oder Blockieren von externer Freigabe auf Domänenbasis finden Sie unter [restricted Domains Sharing in SharePoint Online und OneDrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Vererbung der Berechtigungen für "Broke"  <br/> |PermissionLevelsInheritanceBroken  <br/> |Ein Element wurde so geändert, dass es keine Berechtigungsstufen mehr von seinem übergeordneten Objekt erbt.  <br/> |
|Freigabe Vererbung abgebrochen  <br/> |SharingInheritanceBroken  <br/> |Ein Element wurde so geändert, dass es keine Freigabeberechtigungen mehr von seinem übergeordneten Objekt erbt.  <br/> |
|Unternehmens Freigabe Link erstellt  <br/> |CompanyLinkCreated  <br/> |Der Benutzer hat einen unternehmensweiten Link zu einer Ressource erstellt. unternehmensweite Links können nur von Mitgliedern in Ihrer Organisation verwendet werden. Sie können nicht von Gästen verwendet werden.  <br/> |
|Erstellte Zugriffsanforderung  <br/> |AccessRequestCreated  <br/> |Benutzer fordert Zugriff auf eine Website, einen Ordner oder ein Dokument an, für die Sie keine Zugriffsberechtigungen haben.  <br/> |
|Anonyme Verknüpfung erstellt  <br/> |AnonymousLinkCreated  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource erstellt. Jeder Benutzer mit diesem Link kann auf die Ressource zugreifen, ohne authentifiziert werden zu müssen.  <br/> |
|Erstellter sicherer Link  <br/> |SecureLinkCreated  <br/> |Ein sicherer Freigabe Link wurde für dieses Element erstellt.  <br/> |
|Freigabeeinladung erstellt  <br/> |SharingInvitationCreated  <br/> |Der Benutzer hat eine Ressource in SharePoint Online oder OneDrive für Unternehmen mit einem Benutzer freigegeben, der sich nicht im Verzeichnis Ihrer Organisation befindet.  <br/> |
|Gelöschte sichere Verbindung  <br/> |SecureLinkDeleted  <br/> |Ein sicherer Freigabe Link wurde gelöscht.  <br/> |
|Verweigerte Zugriffsanforderung  <br/> |AccessRequestDenied  <br/> |Eine Zugriffsanforderung für eine Website, einen Ordner oder ein Dokument wurde verweigert.  <br/> |
|Geänderte Berechtigungsstufe für die Websitesammlung  <br/> |PermissionLevelModified  <br/> |Eine Berechtigungsstufe wurde für eine Websitesammlung geändert.  <br/> |
|Entfernen eines Unternehmens Freigabelinks  <br/> |CompanyLinkRemoved  <br/> |Der Benutzer hat einen unternehmensweiten Link zu einer Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Anonymer Link entfernt  <br/> |AnonymousLinkRemoved  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource entfernt. Der Link kann nicht mehr für den Zugriff auf die Ressource verwendet werden.  <br/> |
|Berechtigungsstufe aus Websitesammlung entfernt  <br/> |PermissionLevelRemoved  <br/> |Eine Berechtigungsstufe wurde aus einer Websitesammlung entfernt.  <br/> |
|Wiederhergestellte Freigabe Vererbung  <br/> |SharingInheritanceReset  <br/> |Es wurde eine Änderung vorgenommen, sodass ein Element Freigabeberechtigungen von seinem übergeordneten Objekt erbt.  <br/> |
|FreigeGebene Datei, Ordner oder Website  <br/> |SharingSet  <br/> |Benutzer (Mitglied oder Gast) haben eine Datei, einen Ordner oder eine Website in SharePoint oder OneDrive für Unternehmen mit einem Benutzer im Verzeichnis Ihrer Organisation freigegeben. Der Wert in der **Detail** Spalte für diese Aktivität identifiziert den Namen des Benutzers, für den die Ressource freigegeben wurde, und gibt an, ob dieser Benutzer ein Mitglied oder ein Gast ist. Diese Aktivität wird häufig durch ein zweites Ereignis begleitet, das beschreibt, wie dem Benutzer der Zugriff auf die Ressource gewährt wurde. Beispielsweise wird der Benutzer zu einer Gruppe hinzugefügt, die Zugriff auf die Ressource hat.<br/> |
|Aktualisierte Zugriffsanforderung  <br/> |AccessRequestUpdated  <br/> |Eine Zugriffsanforderung für ein Element wurde aktualisiert.  <br/> |
|Anonymer Link wurde aktualisiert  <br/> |AnonymousLinkUpdated  <br/> |Der Benutzer hat einen anonymen Link zu einer Ressource aktualisiert. Das aktualisierte Feld ist in der EventData-Eigenschaft enthalten, wenn Sie die Suchergebnisse exportieren.  <br/> |
|Aktualisierte Freigabeeinladung  <br/> |SharingInvitationUpdated  <br/> |Eine externe Freigabeeinladung wurde aktualisiert.  <br/> |
|Verwendet einen anonymen Link  <br/> |AnonymousLinkUsed  <br/> |Ein anonymer Benutzer hat auf eine Ressource über einen anonymen Link zugegriffen. Die Identität des Benutzers ist möglicherweise unbekannt, aber Sie können weitere Details wie die IP-Adresse des Benutzers abrufen.  <br/> |
|Nicht freigegebene Datei, Ordner oder Website  <br/> |SharingRevoked  <br/> |Benutzer (Mitglied oder Gast) die Freigabe einer Datei, eines Ordners oder einer Website, die zuvor für einen anderen Benutzer freigegeben wurde.  <br/> |
|Verwendeter Link zu einem Unternehmen  <br/> |CompanyLinkUsed  <br/> |Der Benutzer hat auf eine Ressource über einen unternehmensweiten Link zugegriffen.  <br/> |
|Verwendeter sicherer Link  <br/> |SecureLinkUsed  <br/> |Ein Benutzer hat einen sicheren Link verwendet.  <br/> |
|Benutzer zu Secure Link hinzugefügt  <br/> |AddedToSecureLink  <br/> |Ein Benutzer wurde der Liste der Entitäten hinzugefügt, die einen sicheren Freigabe Link verwenden können.  <br/> |
|Benutzer wurde aus "Secure Link" entfernt  <br/> |RemovedFromSecureLink  <br/> |Ein Benutzer wurde aus der Liste der Entitäten entfernt, die einen sicheren Freigabe Link verwenden können.  <br/> |
|Einladung zur Freigabe wurde zurückgezogen  <br/> |SharingInvitationRevoked  <br/> |Der Benutzer hat eine Freigabeeinladung zu einer Ressource zurückgezogen.  <br/> |
||||
  
### <a name="synchronization-activities"></a>Synchronisierungsaktivitäten
  
In der folgenden Tabelle sind die Datei Synchronisierungsaktivitäten in SharePoint Online und OneDrive for Business aufgeführt.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Zulässiger Computer zum Synchronisieren von Dateien  <br/> |ManagedSyncClientAllowed  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung mit einer Website erfolgreich ein. Die Synchronisierungsbeziehung ist erfolgreich, da der Computer des Benutzers Mitglied einer Domäne ist, die der Liste der Domänen (als *Liste sicherer Empfänger* bezeichnet) hinzugefügt wurde, die auf Dokumentbibliotheken in Ihrer Organisation zugreifen kann.<br/> Weitere Informationen zu dieser Funktion finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die sich in der Liste der sicheren Empfänger befinden](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Blockierte Computer aus der Synchronisierung von Dateien  <br/> |UnmanagedSyncClientBlocked  <br/> |Der Benutzer versucht, eine Synchronisierungsbeziehung mit einer Website von einem Computer aus einzurichten, der kein Mitglied der Domäne Ihrer Organisation ist oder Mitglied einer Domäne ist, die der Liste der Domänen (als *sichere Empfängerliste bezeichnet)* nicht hinzugefügt wurde, die auf das Dokument zugreifen kann. Bibliotheken in Ihrer Organisation. Die Synchronisierungsbeziehung ist nicht zulässig, und der Computer des Benutzers ist für das Synchronisieren, herunterladen oder Hochladen von Dateien in einer Dokumentbibliothek gesperrt.<br/> Informationen zu diesem Feature finden Sie unter [Verwenden von Windows PowerShell-Cmdlets zum Aktivieren der OneDrive-Synchronisierung für Domänen, die sich in der Liste sicherer Empfänger befinden](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|HeruntergeLadene Dateien auf den Computer  <br/> |FileSyncDownloadedFull  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung ein und lädt Dateien zum ersten Mal aus einer Dokumentbibliothek auf Ihren Computer herunter.  <br/> |
|HeruntergeLadene Dateiänderungen am Computer  <br/> |FileSyncDownloadedPartial  <br/> |Der Benutzer lädt erfolgreich alle Änderungen an Dateien aus einer Dokumentbibliothek herunter. Diese Aktivität weist darauf hin, dass alle Änderungen an Dateien in der Dokumentbibliothek auf den Computer des Benutzers heruntergeladen wurden. Nur Änderungen wurden heruntergeladen, da die Dokumentbibliothek zuvor vom Benutzer heruntergeladen wurde (wie durch die **herunterGeladenen Dateien auf Computer** Aktivität angegeben).<br/> |
|HochgeLadene Dateien in die Dokumentbibliothek  <br/> |FileSyncUploadedFull  <br/> |Der Benutzer richtet eine Synchronisierungsbeziehung ein und lädt Dateien zum ersten Mal vom Computer in eine Dokumentbibliothek hoch.  <br/> |
|HochgeLadene Dateiänderungen an der Dokumentbibliothek  <br/> |FileSyncUploadedPartial  <br/> |Der Benutzer lädt Änderungen an Dateien in einer Dokumentbibliothek erfolgreich hoch. Dieses Ereignis gibt an, dass alle Änderungen, die an der lokalen Version einer Datei aus einer Dokumentbibliothek vorgenommen wurden, erfolgreich in die Dokumentbibliothek hochgeladen werden. Nur Änderungen werden entladen, da diese Dateien zuvor vom Benutzer hochgeladen wurden (wie in der * * uploaded files to Document Library * * Activity angegeben).  <br/> |
||||
  
### <a name="site-administration-activities"></a>Aktivitäten der Websiteverwaltung
  
In der folgenden Tabelle sind die Ereignisse aufgeführt, die sich aus Websiteverwaltungsaufgaben in SharePoint Online ergeben.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Freigestellter Benutzer-Agent HinzugeFügt  <br/> |ExemptUserAgentSet  <br/> |Ein SharePoint-oder globaler Administrator fügt einen Benutzer-Agent zur Liste der ausgenommenen Benutzer-Agents im SharePoint Admin Center hinzu.  <br/> |
|Websitesammlungsadministrator HinzugeFügt  <br/> |SiteCollectionAdminAdded  <br/> |Der Websitesammlungsadministrator oder-Besitzer fügt eine Person als Websitesammlungsadministrator für eine Website hinzu. Websitesammlungsadministratoren verfügen über Vollzugriffsberechtigungen für die Websitesammlung und alle Unterwebsites. Diese Aktivität wird auch protokolliert, wenn ein Administrator sich selbst Zugriff auf das OneDrive-Konto eines Benutzers gewährt (indem er das Benutzerprofil im SharePoint Admin Center oder [mithilfe des Office 365 admin Centers](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)bearbeitet).<br/> |
|keine  <br/> |SiteCollectionAdminRemoved <br/> |Der Websitesammlungsadministrator oder-Besitzer entfernt eine Person als Websitesammlungsadministrator für eine Website. Diese Aktivität wird auch protokolliert, wenn ein Administrator sich selbst aus der Liste der Websitesammlungsadministratoren für das OneDrive-Konto eines Benutzers entfernt (durch Bearbeiten des Benutzerprofils im SharePoint Admin Center).  Beachten Sie, dass Sie nach allen Aktivitäten suchen müssen, um diese Aktivität in den Suchergebnissen des Überwachungsprotokolls zurückzugeben. <br/> |
|Benutzer oder Gruppe zu SharePoint-Gruppe HinzugeFügt  <br/> |AddedToGroup  <br/> |Der Benutzer hat ein Mitglied oder einen Gast zu einer SharePoint-Gruppe hinzugefügt. Dies ist möglicherweise eine absichtliche Aktion oder das Ergebnis einer anderen Aktivität, wie etwa ein Freigabe Ereignis.  <br/> |
|Berechtigte Benutzer zum Erstellen von Gruppen  <br/> |AllowGroupCreationSet  <br/> |Der Websiteadministrator oder-Besitzer fügt eine Berechtigungsstufe zu einer Website hinzu, die es einem Benutzer ermöglicht, die Berechtigung zum Erstellen einer Gruppe für diese Website zuzuweisen.  <br/> |
|Gelöschte Website Geo-Verschiebung  <br/> |SiteGeoMoveCancelled  <br/> |Ein SharePoint-oder globaler Administrator bricht erfolgreich eine SharePoint-oder OneDrive Site Geo-Verschiebung ab. Die Multi-Geo-Funktion ermöglicht eine Office 365-Organisation, die mehrere Office 365-Datencenter-geographies umfasst, die GEOS genannt werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Ändern einer Freigaberichtlinie  <br/> |SharingPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat eine SharePoint-Freigaberichtlinie mithilfe des Office 365-Verwaltungsportals, des SharePoint-Verwaltungsportals oder der SharePoint Online-Verwaltungsshell geändert. Jede Änderung an den Einstellungen in der Freigaberichtlinie in Ihrer Organisation wird protokolliert. Die geänderte Richtlinie wird im Feld **ModifiedProperties** in den detaillierten Eigenschaften des Ereignisdatensatzes identifiziert.<br/> |
|Geänderte Gerätezugriffs Richtlinie  <br/> |DeviceAccessPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat die Richtlinie für nicht verwaltete Geräte für Ihre Organisation geändert. Diese Richtlinie steuert den Zugriff auf SharePoint, OneDrive und Office 365 von Geräten, die nicht mit Ihrer Organisation verbunden sind. Zum Konfigurieren dieser Richtlinie ist ein Enterprise Mobility +-Sicherheitsabonnement erforderlich. Weitere Informationen finden Sie unter [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).<br/> |
|Geänderte Ausgeschlossene Benutzer-Agents  <br/> |CustomizeExemptUsers  <br/> |Ein SharePoint-oder globaler Administrator hat die Liste der ausgenommenen Benutzer-Agents im SharePoint Admin Center angepasst. Sie können angeben, welche Benutzer-Agents vom Empfang einer vollständigen Webseite zu indizieren sind. Wenn ein Benutzer-Agent, den Sie als ausgenommen angegeben haben, ein InfoPath-Formular findet, wird das Formular anstelle einer gesamten Webseite als XML-Datei zurückgegeben. Dadurch wird die Indizierung von InfoPath-Formularen beschleunigt.  <br/> |
|Geänderte Netzwerkzugriffsrichtlinie  <br/> |NetworkAccessPolicyChanged  <br/> |Ein SharePoint-oder globaler Administrator hat die standortbasierte Zugriffsrichtlinie (auch als vertrauenswürdige Netzwerkgrenze bezeichnet) im SharePoint Admin Center oder mithilfe von SharePoint Online PowerShell geändert. Dieser Richtlinientyp steuert, wer auf SharePoint-und OneDrive-Ressourcen in Ihrer Organisation basierend auf autorisierten IP-Adressbereichen zugreifen kann, die Sie angeben. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf SharePoint Online-und OneDrive-Daten basierend auf dem Netzwerkspeicherort](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).<br/> |
|Abgeschlossene Website Geo-Verschiebung  <br/> |SiteGeoMoveCompleted  <br/> |Eine Standort Geo-Verschiebung, die von einem globalen Administrator in Ihrer Organisation geplant wurde, wurde erfolgreich abgeschlossen. Die Multi-Geo-Funktion ermöglicht eine Office 365-Organisation, die mehrere Office 365-Datencenter-geographies umfasst, die GEOS genannt werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Erstellte Gruppe  <br/> |GroupAdded  <br/> |Der Websiteadministrator oder-Besitzer erstellt eine Gruppe für eine Website oder führt eine Aufgabe aus, die dazu führt, dass eine Gruppe erstellt wird. Wenn ein Benutzer zum ersten Mal einen Link zum Freigeben einer Datei erstellt, wird eine Systemgruppe zur OneDrive für Business-Website des Benutzers hinzugefügt. Dieses Ereignis kann auch darauf hinweisen, dass ein Benutzer eine Verknüpfung mit Bearbeitungsberechtigungen für eine freigegebene Datei erstellt.  <br/> |
|Erstellt an Connection  <br/> |SendToConnectionAdded  <br/> |Ein SharePoint-oder globaler Administrator erstellt eine neue Verbindung senden an auf der Seite Datensatzverwaltung im SharePoint Admin Center. Eine Sende-an-Verbindung gibt Einstellungen für ein Dokument-Repository oder ein Datenarchiv an. Wenn Sie eine senden-an-Verbindung erstellen, kann ein Inhalts Organisator Dokumente an den angegebenen Speicherort übermitteln.  <br/> |
|Erstellte Websitesammlung  <br/> |SiteCollectionCreated  <br/> |Ein SharePoint-oder globaler Administrator erstellt eine neue Websitesammlung in Ihrer SharePoint Online-Organisation, oder ein Benutzer stellt die OneDrive for Business-Website bereit.  <br/> |
|Gelöschte Gruppe  <br/> |GroupRemoved  <br/> |Der Benutzer löscht eine Gruppe aus einer Website.  <br/> |
|Gelöscht an Verbindung gesendet  <br/> |SendToConnectionRemoved  <br/> |Ein SharePoint-oder globaler Administrator löscht eine senden-an-Verbindung auf der Seite Datensatzverwaltung im SharePoint Admin Center.  <br/> |
|Gelöschte Website  <br/> |SiteDeleted  <br/> |Websiteadministrator löscht eine Website.  <br/> |
|Aktivierte Dokumentvorschau  <br/> |PreviewModeEnabledSet  <br/> |Der Websiteadministrator aktiviert die Dokumentvorschau für eine Website.  <br/> |
|Aktivierter Legacy Workflow  <br/> |LegacyWorkflowEnabledSet  <br/> |Websiteadministrator oder Besitzer fügt der Website den Inhaltstyp für SharePoint 2013-Workflowtask hinzu. Globale Administratoren können auch im SharePoint Admin Center Workflows für die gesamte Organisation aktivieren.  <br/> |
|Aktivieren von Office bei Bedarf  <br/> |OfficeOnDemandSet  <br/> |Der Websiteadministrator aktiviert Office on Demand, sodass Benutzer auf die neueste Version von Office-Desktopanwendungen zugreifen können. Office on Demand ist im SharePoint Admin Center aktiviert und erfordert ein Office 365-Abonnement, das vollständige, installierte Office-Anwendungen enthält.  <br/> |
|Aktivierte RSS-Feeds  <br/> |NewsFeedEnabledSet  <br/> |Der Websiteadministrator oder-Besitzer aktiviert RSS-Feeds für eine Website. Globale Administratoren können RSS-Feeds für die gesamte Organisation im SharePoint Admin Center aktivieren.  <br/> |
|Geänderte Zugriffs Anforderungs Einstellung  <br/> |WebRequestAccessModified  <br/> |Die Einstellungen für die Zugriffsanforderung wurden auf einer Website geändert.  <br/> |
|Geänderte Elemente können die Einstellung freigeben  <br/> |WebMembersCanShareModified  <br/> |Die Einstellung der **Mitglieder kann** auf einer Website geändert werden.  <br/> |
|Geänderte Websiteberechtigungen  <br/> |SitePermissionsModified  <br/> |Websiteadministrator oder Besitzer (oder Systemkonto) ändert die Berechtigungsstufe, die einer Gruppe auf einer Website zugewiesen ist. Diese Aktivität wird auch protokolliert, wenn alle Berechtigungen aus einer Gruppe entfernt werden.<br/> > [!NOTE]> dieser Vorgang ist in SharePoint Online veraltet. Zum Suchen nach verwandten Ereignissen können Sie nach anderen Berechtigungs bezogenen Aktivitäten wie **Hinzufügen des Websitesammlungsadministrators**, **Hinzufügen von Benutzer oder Gruppen zu SharePoint-Gruppen**, Benutzer **Gruppen erstellen**, **erstellte Gruppe**und gelöscht suchen. ** Group.**         |
|Benutzer oder Gruppe aus SharePoint-Gruppe entfernt  <br/> |RemovedFromGroup  <br/> |Der Benutzer hat ein Mitglied oder einen Gast aus einer SharePoint-Gruppe entfernt. Dies ist möglicherweise eine absichtliche Aktion oder das Ergebnis einer anderen Aktivität, beispielsweiseeines Unsharing-Ereignisses.  <br/> |
|UmBenannte Website  <br/> |SiteRenamed  <br/> |Websiteadministrator oder Besitzer benennt eine Website um  <br/> |
|Angeforderte Websiteadministrator Berechtigungen  <br/> |SiteAdminChangeRequest  <br/> |Benutzeranforderungen, die als Websitesammlungsadministrator für eine Websitesammlung hinzugefügt werden sollen. Websitesammlungsadministratoren verfügen über Vollzugriffsberechtigungen für die Websitesammlung und alle Unterwebsites.  <br/> |
|Geplante Standort Geo-Verschiebung  <br/> |SiteGeoMoveScheduled  <br/> |Ein SharePoint-oder globaler Administrator plant erfolgreich eine SharePoint-oder OneDrive Site Geo-Verschiebung. Die Multi-Geo-Funktion ermöglicht eine Office 365-Organisation, die mehrere Office 365-Datencenter-geographies umfasst, die GEOS genannt werden. Weitere Informationen finden Sie unter [Multi-Geo-Funktionen in OneDrive und SharePoint Online in Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Festlegen der Hostwebsite  <br/> |HostSiteSet  <br/> |Ein SharePoint-oder globaler Administrator ändert die designierte Website, um persönliche oder OneDrive for Business-Websites zu hosten.  <br/> |
|Aktualisierte Gruppe  <br/> |GroupUpdated  <br/> |Der Websiteadministrator oder Besitzer ändert die Einstellungen einer Gruppe für eine Website. Dazu gehört das Ändern des Gruppennamens, der die Gruppenmitgliedschaft anzeigen oder bearbeiten kann und wie Mitgliedschaftsanfragen behandelt werden.  <br/> |
||||
  
### <a name="exchange-mailbox-activities"></a>Exchange-Postfachaktivitäten
  
In der folgenden Tabelle sind die Aktivitäten aufgeführt, die von der postfachüberwachungsprotokollierung protokolliert werden können. Postfachaktivitäten, die vom Postfachbesitzer, einem Delegierten Benutzer oder einem Administrator ausgeführt werden, werden protokolliert. Die postfachüberwachung in Office 365 ist standardmäßig nicht aktiviert. Die postfachüberwachungsprotokollierung muss für jedes Postfach aktiviert sein, bevor die Post Fach Aktivität protokolliert wird. Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Stellvertretungs-Postfachberechtigungen HinzugeFügt  <br/> |Add-MailboxPermission  <br/> |Ein Administrator hat dem Postfach einer anderen Person die Berechtigung FullAccess-Postfach für einen Benutzer (als Stellvertretung bezeichnet) zugewiesen. Die FullAccess-Berechtigung ermöglicht es der Stellvertretung, das Postfach der anderen Person zu öffnen und den Inhalt des Postfachs zu lesen und zu verwalten.  <br/> |
|Klassifizierte Nachricht als Datensatz  <br/> |ApplyRecordLabel<br/> |Eine Nachricht wurde als Datensatz klassifiziert. Dies tritt auf, wenn eine Aufbewahrungs Bezeichnung, die Inhalte als Datensatz klassifiziert, manuell oder automatisch auf eine Nachricht angewendet wird.<br/> |
|Nachrichten in einen anderen Ordner kopiert  <br/> |Kopieren  <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |
|Erstelltes Postfachelement  <br/> |Erstellen  <br/> |Ein Element wird im Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht nicht überwacht wird. Außerdem wird das Erstellen eines Postfachordners nicht überwacht.  <br/> |
|Neue Posteingangsregel in Outlook Web App erstellt  <br/> |NewInboxRule<br/> |<br/> |
|Gelöschte Nachrichten aus Ordner "Gelöschte Elemente"  <br/> |SoftDelete  <br/> |Eine Nachricht wurde dauerhaft aus dem Ordner "Gelöschte Elemente" gelöscht oder gelöscht. Diese Elemente werden in den Ordner "Wiederherstellbare Elemente" verschoben. Nachrichten werden auch in den Ordner "Wiederherstellbare Elemente" verschoben, wenn ein Benutzer Sie auswählt und **UMSCHALT + ENTF**drückt.<br/> |
|Nachrichten in einen anderen Ordner verschoben  <br/> |Verschieben  <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |
|Nachrichten in Ordner "Gelöschte Elemente" verschoben  <br/> |MoveToDeletedItems  <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |
|Berechtigung für geänderte Ordner  <br/> |UpdateFolderPermissions  <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Postfachordner und die Nachrichten im Ordner zugreifen können.  <br/> |
|Gelöschte Nachrichten aus dem Postfach  <br/> |HardDelete  <br/> |Eine Nachricht wurde aus dem Ordner "Wiederherstellbare Elemente" entfernt (dauerhaft aus dem Postfach gelöscht).  <br/> |
|Berechtigungen für Stellvertreter Postfächer entfernt  <br/> |Remove-MailboxPermission  <br/> |Ein Administrator hat die FullAccess-Berechtigung (die einem Stellvertreter zugewiesen wurde) aus dem Postfach einer Person entfernt. Nachdem die FullAccess-Berechtigung entfernt wurde, kann die Stellvertretung das Postfach der anderen Person nicht öffnen oder auf Inhalte zugreifen.  <br/> |
|Gesendete Nachricht unter Verwendung der Berechtigung "Senden als"  <br/> |SendAs  <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |
|Gesendete Nachricht mithilfe von "Senden im Auftrag von"-Berechtigungen  <br/> |SendOnBehalf  <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |
|Aktualisierter Stellvertretungszugriff auf Kalenderordner  <br/> |UpdateCalendarDelegation  <br/> |Einem Postfach wurde eine Kalender Delegierung zugewiesen. Die Kalender Delegierung erteilt anderen Benutzern in derselben Organisation Berechtigungen zum Verwalten des Kalenders des Postfachbesitzers.  <br/> |
|Aktualisierte Nachricht  <br/> |Aktualisieren  <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |
|Benutzer bei Postfach angemeldet  <br/> |Mailbox Login:  <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |
|keine  <br/> |UpdateInboxRules  <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. PostEingangsregeln werden verwendet, um Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen zu verarbeiten und Aktionen auszuführen, wenn die Bedingungen einer Regel erfüllt sind, beispielsweise das Verschieben einer Nachricht in einen bestimmten Ordner oder das Löschen einer Nachricht.<br/> Wenn Sie Einträge für Posteingangsregel Aktivitäten zurückgeben möchten, müssen Sie in der Liste **Aktivitäten** die Option **Ergebnisse für alle Aktivitäten anzeigen** auswählen. Verwenden Sie die Felder Datumsbereiche und **Benutzer** , um die Suchergebnisse einzuschränken.<br/> |
||||
  
### <a name="retention-policy-and-label-activities"></a>Aufbewahrungsrichtlinie und Bezeichnungs Aktivitäten

In der folgenden Tabelle werden die Aktivitäten im Zusammenhang mit Office 365-Aufbewahrungsrichtlinien und Office 365-Aufbewahrungs Bezeichnungen beschrieben.

- [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md)
- [Übersicht über Aufbewahrungsbezeichnungen](labels.md)
<br/>

|**Aktivität**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
| Erstellte Aufbewahrungs Konfiguration für eine Aufbewahrungsrichtlinie<br/> |NewRetentionComplianceRule<br/> |Der Administrator konfiguriert die Aufbewahrungseinstellungen für eine neue Aufbewahrungsrichtlinie. Aufbewahrungseinstellungen umfassen, wie lange Elemente aufbewahrt werden, und was mit Elementen passiert, wenn der Aufbewahrungszeitraum abgelaufen ist (beispielsweise Löschen von Elementen, beibehalten von Elementen oder beibehalten und dann löschen). Diese Aktivität entspricht auch der Verwendung des [New-RetentionComplianceRule-](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancerule) Cmdlets.<br/>|
| Erstellte Aufbewahrungs Bezeichnung <br/> |NewComplianceTag<br/>  |Der Administrator erstellt eine neue Aufbewahrungs Bezeichnung.<br/> |
| Erstellte Aufbewahrungsrichtlinie<br/> |NewRetentionCompliancePolicy<br/> |Der Administrator erstellt eine neue Aufbewahrungsrichtlinie.<br/>  |
| Gelöschte Aufbewahrungs Konfiguration für eine Aufbewahrungsrichtlinie<br/> | RemoveRetentionComplianceRule<br/>| Der Administrator löscht die Konfigurationseinstellungen einer Aufbewahrungsrichtlinie. Diese Aktivität wird wahrscheinlich protokolliert, wenn ein Administrator eine Aufbewahrungsrichtlinie löscht oder das Cmdlet **Remove-RetentionComplianceRule** ausführt.<br/> |
| Gelöschte Aufbewahrungs Bezeichnung <br/> |RemoveComplianceTag<br/>  | Der Administrator löscht eine Aufbewahrungs Bezeichnung.<br/>|
| Gelöschte Aufbewahrungsrichtlinie<br/> |RemoveRetentionCompliancePolicy<br/> |Der Administrator löscht eine Aufbewahrungsrichtlinie. <br/>  |
| Aktivieren von Compliance-Features<br/> |SetRestrictiveRetentionUI<br/> |Der Administrator aktiviert Compliance-Funktionen, indem er das Cmdlet **Set-RegulatoryComplianceUI** ausführt. Nachdem dieses Cmdlet ausgeführt wurde, können Administratoren eine Aufbewahrungsrichtlinie Sperren und mithilfe der Benutzeroberfläche Security & Compliance Center eine Aufbewahrungs Bezeichnung als behördlichen Daten Satz angeben. Bis eine Organisation das Cmdlet **Set-RegulatoryComplianceUI** verwendet, um diese Features zu aktivieren, kann das Sperren einer Aufbewahrungsrichtlinie und das Erstellen einer gesetzlichen Aufbewahrungs Bezeichnung nur mithilfe von PowerShell erfolgen.<br/>|
| Aktualisierte Aufbewahrungs Konfiguration für eine Aufbewahrungsrichtlinie<br/> | SetRetentionComplianceRule<br/>| Der Administrator ändert die Aufbewahrungseinstellungen für eine vorhandene Aufbewahrungsrichtlinie. Aufbewahrungseinstellungen umfassen, wie lange Elemente aufbewahrt werden, und was mit Elementen passiert, wenn der Aufbewahrungszeitraum abgelaufen ist (beispielsweise Löschen von Elementen, beibehalten von Elementen oder beibehalten und dann löschen). Diese Aktivität entspricht auch der Verwendung des Cmdlets [Set-RetentionComplianceRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/set-retentioncompliancerule) .<br/>|
| Aktualisierte Aufbewahrungs Bezeichnung <br/> |SetComplianceTag<br/>  | Der Administrator aktualisiert eine vorhandene Aufbewahrungs Bezeichnung.<br/>|
| Aktualisierte Aufbewahrungsrichtlinie<br/> |SetRetentionCompliancePolicy <br/>|Der Administrator aktualisiert eine vorhandene Aufbewahrungsrichtlinie. Zu den Updates, die dieses Ereignis auslösen, gehört das Hinzufügen oder Ausschließen von Inhaltsspeicherorten, auf die die Aufbewahrungsrichtlinie angewendet wird.<br/>|
||||

### <a name="sway-activities"></a>Sway-Aktivitäten
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in Sway aufgeführt. Sway ist eine Office 365-APP, die Benutzern hilft, Ideen, Geschichten und Präsentationen auf einer interaktiven, webbasierten Leinwand zu sammeln, zu formatieren und zu teilen. Weitere Informationen finden Sie unter [häufig gestellte Fragen zu Sway-Admin-Hilfe](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Sway-Freigabestufe  <br/> |SwayChangeShareLevel  <br/> |Der Benutzer ändert die Freigabeebene eines Sway. Dieses Ereignis erfasst den Benutzer, der den Bereich der Freigabe ändert, die mit einem Sway verbunden ist; beispielsweise Public versus innerhalb der Organisation.  <br/> |
|Erstellt Sway  <br/> |SwayCreate  <br/> |Der Benutzer erstellt eine Sway.  <br/> |
|Gelöschte Sway  <br/> |SwayDelete  <br/> |Der Benutzer löscht eine Sway.  <br/> |
|DeAktivierte Sway-Duplizierung  <br/> |SwayDisableDuplication  <br/> |Der Benutzer deaktiviert die Duplizierung eines Sway.  <br/> |
|Duplizierte Sway  <br/> |SwayDuplicate  <br/> |Der Benutzer dupliziert eine Sway.  <br/> |
|Bearbeitet Sway  <br/> |SwayEdit  <br/> |Benutzer bearbeitet eine Sway.  <br/> |
|Aktivierte Sway-Duplizierung  <br/> |EnableDuplication  <br/> |Der Benutzer ermöglicht die Duplizierung einer Sway; die Möglichkeit für einen Benutzer, die Duplizierung einer Sway zu aktivieren, ist standardmäßig aktiviert.  <br/> |
|Widerrufen der Sway-Freigabe  <br/> |SwayRevokeShare  <br/> |Der Benutzer beendet die Freigabe eines Sway durch widerrufen des Zugriffs. Beim widerrufen des Zugriffs werden die mit einem Sway verknüpften Links geändert.  <br/> |
|Gemeinsame Sway  <br/> |SwayShare  <br/> |Der Benutzer beabsichtigt, eine Sway zu teilen. Dieses Ereignis erfasst die Benutzeraktion des Klickens auf ein bestimmtes freigabeziel im Sway-Freigabe Menü. Das Ereignis gibt nicht an, ob der Benutzer die Freigabe Aktion abgeschlossen hat.  <br/> |
|Externe Freigabe von Sway deaktiviert  <br/> |SwayExternalSharingOff  <br/> |Der Administrator deaktiviert die externe Sway-Freigabe für die gesamte Organisation mithilfe des Office 365 Admin Center.  <br/> |
|Aktivierte externe Freigabe von Sway  <br/> |SwayExternalSharingOn  <br/> |Der Administrator aktiviert die externe Sway-Freigabe für die gesamte Organisation mithilfe des Office 365 Admin Center.  <br/> |
|Turned off Sway Service  <br/> |SwayServiceOff  <br/> |Der Administrator deaktiviert Sway für die gesamte Organisation mithilfe des Office 365 Admin Center.  <br/> |
|Turned on Sway Service  <br/> |SwayServiceOn  <br/> |Der Administrator aktiviert die Sway für die gesamte Organisation mithilfe des Office 365 Admin Center (der Sway-Dienst ist standardmäßig aktiviert).  <br/> |
|Sway  <br/> |SwayView  <br/> |Benutzeransicht ein Sway.  <br/> |
||||

  
### <a name="user-administration-activities"></a>Benutzer Verwaltungsaktivitäten
  
In der folgenden Tabelle werden die Aktivitäten der Benutzerverwaltung aufgelistet, die protokolliert werden, wenn ein Benutzerkonto mithilfe des Office 365 admin Centers oder des Azure-Verwaltungsportals hinzugefügt oder geändert wird.
  
|**Aktivität**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Benutzer HinzugeFügt  <br/> |Benutzer hinzufügen  <br/> |Ein Office 365-Benutzerkonto wurde erstellt.  <br/> |
|Geänderte Benutzerlizenz  <br/> |Ändern der Benutzerlizenz  <br/> |Die einem Benutzer zugewiesene Lizenz, was geändert wurde. Informationen dazu, welche Lizenzen geändert wurden, finden Sie in der entsprechenden **aktualisierten Benutzer** Aktivität.<br/> |
|Geändertes Benutzerkennwort  <br/> |Benutzerkennwort ändern  <br/> |Der Administrator hat das Kennwort als Kennwort für einen Benutzer geändert.  <br/> |
|Gelöschter Benutzer  <br/> |Löschen eines Benutzers  <br/> |Ein Office 365-Benutzerkonto wurde gelöscht.  <br/> |
|Benutzerkennwort zurücksetzen  <br/> |Benutzerkennwort zurücksetzen  <br/> |Der Administrator hat das Kennwort für einen Benutzer zurückgesetzt.  <br/> |
|Eigenschaft festlegen, die den Benutzer zum Ändern des Kennworts zwingt  <br/> |Erzwingen der Änderung des Benutzerkennworts  <br/> |Administrator legen Sie die Eigenschaft fest, die es einem Benutzer erzwingt, sein Kennwort zu ändern, wenn sich der Benutzer das nächste Mal bei Office 365 anmeldet.  <br/> |
|Festlegen von Lizenzeigenschaften  <br/> |Festlegen von Lizenzeigenschaften  <br/> |Der Administrator ändert die Eigenschaften einer einem Benutzer zugewiesenen Lizenz.  <br/> |
|Aktualisierter Benutzer  <br/> |Benutzer aktualisieren  <br/> |Der Administrator ändert eine oder mehrere Eigenschaften eines Benutzerkontos. Eine Liste der Benutzereigenschaften, die aktualisiert werden können, finden Sie im Abschnitt "Aktualisieren von Benutzerattributen" in [Azure Active Directory-Überwachungsbericht Ereignissen](https://go.microsoft.com/fwlink/p/?LinkID=616549).<br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Verwaltungsaktivitäten der Azure AD-Gruppe
  
In der folgenden Tabelle sind die Aktivitäten der Gruppenverwaltung aufgeführt, die protokolliert werden, wenn ein Administrator oder ein Benutzer eine Office 365-Gruppe erstellt oder ändert oder wenn ein Administrator eine Sicherheitsgruppe mithilfe des Office 365 admin Centers oder des Azure-Verwaltungsportals erstellt. Weitere Informationen zu Gruppen in Office 365 finden Sie unter [anzeigen, erstellen und Löschen von Gruppen im office 365 Admin Center](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Gruppe HinzugeFügt  <br/> |Gruppe hinzufügen  <br/> |Eine Gruppe wurde erstellt.  <br/> |
|Mitglied zu Gruppe HinzugeFügt  <br/> |Mitglied zu Gruppe hinzufügen  <br/> |Ein Mitglied wurde einer Gruppe hinzugefügt.  <br/> |
|Gelöschte Gruppe  <br/> |Gruppe löschen  <br/> |Eine Gruppe wurde gelöscht.  <br/> |
|Element aus Gruppe entfernt  <br/> |Element aus Gruppe entfernen  <br/> |Ein Mitglied wurde aus einer Gruppe entfernt.  <br/> |
|Aktualisierte Gruppe  <br/> |Gruppe aktualisieren  <br/> |Eine Eigenschaft einer Gruppe wurde geändert.  <br/> |
||||
   
### <a name="application-administration-activities"></a>Aktivitäten der Anwendungsverwaltung
  
In der folgenden Tabelle sind die Anwendungsadministrator Aktivitäten aufgeführt, die protokolliert werden, wenn ein Administrator eine in Azure AD registrierte Anwendung hinzufügt oder ändert. Alle Anwendungen, die Azure AD für die Authentifizierung benötigen, müssen im Verzeichnis registriert sein.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Delegierungs Eintrag HinzugeFügt  <br/> |Delegierungs Eintrag hinzufügen  <br/> |Eine Authentifizierungs Berechtigung wurde für eine Anwendung in Azure AD erstellt/erteilt.  <br/> |
|Dienstprinzipal HinzugeFügt  <br/> |Hinzufügen eines Dienst Prinzipals  <br/> |Eine Anwendung wurde in Azure AD registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Anmeldeinformationen zu einem Dienstprinzipal HinzugeFügt  <br/> |Hinzufügen von Dienstprinzipal Anmeldeinformationen  <br/> |Anmeldeinformationen wurden einem Dienstprinzipal in Azure AD hinzugefügt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Delegierungs Eintrag entfernt  <br/> |Delegierungs Eintrag entfernen  <br/> |Eine Authentifizierungs Berechtigung wurde aus einer Anwendung in Azure AD entfernt.  <br/> |
|Ein Dienstprinzipal wurde aus dem Verzeichnis entfernt.  <br/> |Dienstprinzipal entfernen  <br/> |Eine Anwendung wurde aus Azure AD gelöscht/nicht registriert. Eine Anwendung wird durch einen Dienstprinzipal im Verzeichnis dargestellt.  <br/> |
|Die Anmeldeinformationen wurden aus einem Dienstprinzipal entfernt.  <br/> |Entfernen von Dienstprinzipal Anmeldeinformationen  <br/> |Anmeldeinformationen wurden aus einem Dienstprinzipal in Azure AD entfernt. Ein Dienst Prinzip stellt eine Anwendung im Verzeichnis dar.  <br/> |
|Festlegen des Delegierungs Eintrags  <br/> |Festlegen des Delegierungs Eintrags  <br/> |Eine Authentifizierungs Berechtigung wurde für eine Anwendung in Azure AD aktualisiert.  <br/> |
||||

### <a name="role-administration-activities"></a>Rollen Verwaltungsaktivitäten
  
Die folgende Tabelle enthält eine Liste der Azure AD Role Administration-Aktivitäten, die protokolliert werden, wenn ein Administrator Administratorrollen im Office 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Mitglied zu Rolle hinzufügen  <br/> |Rollenmitglied zu Rolle hinzufügen  <br/> |Benutzer zu einer Administratorrolle in Office 365 HinzugeFügt.  <br/> |
|Entfernen eines Benutzers aus einer Verzeichnis Rolle  <br/> |Rollenelement aus Rolle entfernen  <br/> |Ein Benutzer wurde aus einer Administratorrolle in Office 365 entfernt.  <br/> |
|Unternehmenskontakt Informationen festlegen  <br/> |Unternehmenskontakt Informationen festlegen  <br/> |Die Kontakteinstellungen auf Unternehmensebene für Ihre Office 365-Organisation wurden aktualisiert. Dazu gehören e-Mail-Adressen für abonnementbezogene e-Mails, die von Office 365 gesendet werden, sowie technische Benachrichtigungen zu Office 365-Diensten.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>Aktivitäten der Verzeichnisverwaltung
  
In der folgenden Tabelle werden die Azure AD-Verzeichnis-und domänenbezogenen Aktivitäten aufgelistet, die protokolliert werden, wenn ein Administrator die Office 365-Organisation im Office 365 Admin Center oder im Azure-Verwaltungsportal verwaltet.
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Domäne zu Firma HinzugeFügt  <br/> |Hinzufügen einer Domäne zu Firma  <br/> |Domäne zu Ihrer Office 365-Organisation HinzugeFügt.  <br/> |
|Partner zum Verzeichnis HinzugeFügt  <br/> |Hinzufügen eines Partners zu Unternehmen  <br/> |Partner (Delegierter Administrator) zu Ihrer Office 365-Organisation HinzugeFügt.  <br/> |
|Domäne aus Firma entfernt  <br/> |Domäne aus Firma entfernen  <br/> |Eine Domäne aus Ihrer Office 365-Organisation entfernt.  <br/> |
|Partner aus dem Verzeichnis entfernt  <br/> |Partner aus Firma entfernen  <br/> |Ein Partner (Delegierter Administrator) wurde aus Ihrer Office 365-Organisation entfernt.  <br/> |
|Unternehmensinformationen festlegen  <br/> |Unternehmensinformationen festlegen  <br/> |Unternehmensinformationen für Ihre Office 365-Organisation aktualisiert. Dazu gehören e-Mail-Adressen für abonnementbezogene e-Mails, die von Office 365 gesendet werden, sowie technische Benachrichtigungen zu Office 365-Diensten.  <br/> |
|Festlegen der Domänenauthentifizierung  <br/> |Festlegen der Domänenauthentifizierung  <br/> |Die Domänen Authentifizierungseinstellung für Ihre Office 365-Organisation wurde geändert.  <br/> |
|Die Verbund Einstellungen für eine Domäne wurden aktualisiert.  <br/> |Festlegen von Verbund Einstellungen für die Domäne  <br/> |Die Einstellungen für den Verbund (externe Freigabe) für Ihre Office 365-Organisation wurden geändert.  <br/> |
|Festlegen der Kennwortrichtlinie  <br/> |Festlegen der Kennwortrichtlinie  <br/> |Die Längen-und Zeicheneinschränkungen für Benutzerkennwörter in Ihrer Office 365-Organisation wurden geändert.  <br/> |
|Azure AD-Synchronisierung aktiviert  <br/> |DirSyncEnabled-Flag für Unternehmen festlegen  <br/> |Legen Sie die Eigenschaft fest, die ein Verzeichnis für die Azure AD-Synchronisierung aktiviert.  <br/> |
|Aktualisierte Domäne  <br/> |Domäne aktualisieren  <br/> |Die Einstellungen einer Domäne in Ihrer Office 365-Organisation wurden aktualisiert.  <br/> |
|Verifizierte Domäne  <br/> |Domäne überprüfen  <br/> |Überprüft, ob Ihre Organisation der Besitzer einer Domäne ist.  <br/> |
|Verifizierte e-Mail verifizierte Domäne  <br/> |Überprüfen der e-Mail verifizierte Domäne  <br/> |Verwenden Sie die e-Mail-Überprüfung, um sicherzustellen, dass Ihre Organisation der Besitzer einer Domäne ist.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>eDiscovery-Aktivitäten
  
Inhaltssuche und eDiscovery-bezogene Aktivitäten, die im Office 365 Security & Compliance Center oder durch Ausführen der entsprechenden Windows PowerShell-Cmdlets ausgeführt werden, werden im Office 365-Überwachungsprotokoll protokolliert. Hierzu gehören die folgenden Aktivitäten:
  
- Erstellen und Verwalten von eDiscovery-Fällen
    
- Erstellen, starten und Bearbeiten von Inhalts suchen
    
- Ausführen von Inhalts Suchaktionen wie Vorschau, exportieren und Löschen von Suchergebnissen
    
- Konfigurieren der Filterung von Berechtigungen für die Inhaltssuche
    
- Verwalten der eDiscovery-Administrator Rolle
    
Eine Liste und eine detaillierte Beschreibung der zu protokollierenden eDiscovery-Aktivitäten finden Sie unter [Suchen nach eDiscovery-Aktivitäten im Office 365-Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Es dauert bis zu 30 Minuten für Ereignisse, die sich aus den unter **eDiscovery-Aktivitäten** aufgeführten Aktivitäten in der Dropdownliste **Aktivitäten** ergeben, die in den Suchergebnissen angezeigt werden sollen. Umgekehrt kann es bis zu 24 Stunden dauern, bis die entsprechenden Ereignisse aus eDiscovery-Cmdlet-Aktivitäten in den Suchergebnissen angezeigt werden. 
  
### <a name="power-bi-activities"></a>Power BI-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Power BI durchsuchen. Informationen zu Power BI-Aktivitäten finden Sie im Abschnitt "Aktivitäten, die von Power Power BI überwacht werden" unter [Verwenden der Überwachung in Ihrer Organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
Beachten Sie, dass die Überwachungsprotokollierung für Power BI standardmäßig nicht aktiviert ist. Um nach Power BI-Aktivitäten im Office 365-Überwachungsprotokoll zu suchen, müssen Sie die Überwachung im Power BI Admin-Portal aktivieren. Anweisungen finden Sie im Abschnitt "Überwachungsprotokolle" im [Power BI Admin Portal](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
  
### <a name="microsoft-workplace-analytics-activities"></a>Microsoft Workplace Analytics-Aktivitäten

Workplace Analytics bietet einen Einblick in die Zusammenarbeit von Gruppen in Ihrer Office 365-Organisation. In der folgenden Tabelle werden die Aktivitäten aufgeführt, die von Benutzern ausgeführt werden, denen die Rolle Administrator oder Analyst in Workplace Analytics zugewiesen wurde. Benutzer, denen die Rolle "Analyst" zugewiesen ist, haben vollständigen Zugriff auf alle Dienstfunktionen und verwenden das Produkt für die Analyse. Benutzer, denen die Administrator Rolle zugewiesen ist, können Datenschutzeinstellungen und Systemstandardwerte konfigurieren und Organisationsdaten in der Workplace Analytics vorbereiten, hochladen und überprüfen. Weitere Informationen finden Sie unter [Workplace Analytics](https://docs.microsoft.com/en-us/workplace-analytics/index-orig).

|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Zugriff auf OData-Link <br/> |AccessedOdataLink <br/> |Der Analytiker hat auf den OData-Link für eine Abfrage zugegriffen.|
|Abgebrochene Abfrage <br/> |CanceledQuery <br/> |Analyst hat eine laufende Abfrage abgebrochen.|
|Erstellter Besprechungs Ausschluss <br/> |MeetingExclusionCreated <br/> |Der Analytiker hat eine neue Ausschlussregel für Besprechungen erstellt.|
|Gelöschtes Ergebnis <br/> |DeletedResult <br/> |Der Analytiker hat ein Abfrageergebnis gelöscht.|
|HeruntergeLadener Bericht <br/> |DownloadedReport <br/> |Analyst hat eine Abfrageergebnis Datei heruntergeladen.|
|Ausgeführte Abfrage <br/> |ExecutedQuery <br/> |Eine Abfrage wurde vom Analysten ausgeführt.|
|Aktualisierte Datenzugriffs Einstellung <br/> |UpdatedDataAccessSetting <br/> |Admin hat Datenzugriffs Einstellungen aktualisiert.|
|Aktualisierte Datenschutzeinstellung <br/> |UpdatedPrivacySetting <br/> |Admin aktualisierte Datenschutzeinstellungen; Beispiel: minimale Gruppengröße.|
|HochgeLadene Organisationsdaten <br/> |UploadedOrgData <br/> |Admin-hochgeladene Organisations Datendatei.|
|Viewed Explore <br/> |ViewedExplore <br/> |Von Analysten angezeigte Visualisierungen auf einer oder mehreren Registerkarten der Seite "Durchsuchen".|
||||

### <a name="microsoft-teams-activities"></a>Microsoft Teams-Aktivitäten
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in Microsoft Teams aufgeführt, die im Office 365-Überwachungsprotokoll protokolliert werden. Microsoft Teams ist ein Chat-zentrierter Arbeitsbereich in Office 365. Die Unterhaltungen, Besprechungen, Dateien und Notizen eines Teams werden an einem zentralen Ort zusammengeführt. Weitere Informationen und Links zu Hilfethemen finden Sie unter:
  
- [Häufig gestellte Fragen zu Microsoft Teams-Administratorhilfe](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Microsoft Teams-Hilfe](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Bot zu Team HinzugeFügt  <br/> |BotAddedToTeam  <br/> |Ein Benutzer fügt einem Team einen bot hinzu.  <br/> |
|Kanal HinzugeFügt  <br/> |ChannelAdded  <br/> |Ein Benutzer fügt einem Team einen Kanal hinzu.  <br/> |
|Connector HinzugeFügt  <br/> |ConnectorAdded  <br/> |Ein Benutzer fügt einem Kanal einen Konnektor hinzu.  <br/> |
|Mitglieder zu Team HinzugeFügt  <br/> |MemberAdded  <br/> |Ein Teambesitzer fügt einem Teammitglieder hinzu.  <br/> |
|Registerkarte HinzugeFügt  <br/> |TabAdded  <br/> |Ein Benutzer fügt einem Kanal eine Registerkarte hinzu.  <br/> |
|Geänderte Kanaleinstellung  <br/> |ChannelSettingChanged  <br/> | Der ChannelSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem Teammitglied ausgeführt werden. Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (in Klammern unten) in der Spalte **Element** in den Suchergebnissen des Überwachungsprotokolls angezeigt.<br/> <br/>-Ändert den Namen eines Team Kanals ( **Kanalname**).  <br/>  <br/>-Ändert die Beschreibung eines Team Kanals ( **Kanalbeschreibung**).  <br/> |
|Geänderte Organisations Einstellung  <br/> |TeamsTenantSettingChanged  <br/> | Der TeamsTenantSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem globalen Administrator (mit dem Office 365 Admin Center) ausgeführt werden. Beachten Sie, dass sich diese Aktivitäten auf organisationsweite Microsoft Teams-Einstellungen auswirken. Weitere Informationen finden Sie unter [Administrator Einstellungen für Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).<br/>  Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (in Klammern unten) in der Spalte **Element** in den Suchergebnissen des Überwachungsprotokolls angezeigt.  <br/><br/>– Aktiviert oder deaktiviert Microsoft Teams für die Organisation ( **Microsoft Teams**).  <br/><br/>– Aktiviert oder deaktiviert die Interoperabilität zwischen Microsoft Teams und Skype for Business für die Organisation ( **Skype for Business-Interoperabilität**).<br/><br/>– Aktiviert oder deaktiviert die Ansicht Organisationsdiagramm in Microsoft Teams-Clients (Organigramm- **Ansicht**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, private Besprechungen (private Termin **Planung**) zu planen.  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Kanal Besprechungen ( **Kanal Besprechungsplanung**) einzuplanen.  <br/><br/>-Aktiviert oder deaktiviert Videoanrufe in Teams-Besprechungen ( **Video für Skype**-Besprechungen).  <br/><br/>-Aktiviert oder deaktiviert die Bildschirmfreigabe in Microsoft Teams-Meetups für die Organisation ( **Bildschirmfreigabe für Skype**-Besprechungen).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit, animierte Bilder (als Giphys bezeichnet) zu Teams-Unterhaltungen ( **animierte Bilder**) hinzuzufügen.  <br/><br/>-Ändert die Einstellung der Inhaltsbewertung für die Organisation ( **Inhaltsbewertung**). Die Inhaltsbewertung schränkt den Typ des animierten Bilds ein, das in Unterhaltungen angezeigt werden kann.<br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, anpassbare Bilder (als benutzerdefinierte Meme bezeichnet) aus dem Internet zu Team Unterhaltungen hinzuzufügen ( **anpassbare Bilder aus dem Internet**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, bearbeitbare Bilder (als Aufkleber bezeichnet) zu Team Unterhaltungen hinzuzufügen ( **bearbeitbare Bilder**).<br/><br/>-Aktiviert oder deaktiviert diese Fähigkeit für Teammitglieder, Bots in Microsoft Teams-Chats und-Kanälen ( **org-weite Bots**) zu verwenden.<br/><br/>-Aktiviert bestimmte Bots für Microsoft Teams; Dies beinhaltet nicht den T-bot, der Teams-Hilfe-bot, der verfügbar ist, wenn Bots für die Organisation aktiviert sind ( **einzelne Bots**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Teammitglieder, Erweiterungen oder Registerkarten ( **Erweiterungen oder Registerkarten**) hinzuzufügen.  <br/><br/>-Aktiviert oder deaktiviert das Side-Loading von proprietären Bots für Microsoft Teams ( **Side loading of Bots**).  <br/><br/>-Aktiviert oder deaktiviert die Möglichkeit für Benutzer, e-Mail-Nachrichten an einen Microsoft Teams-Kanal ( **Kanal-e-Mail**) zu senden.  <br/> |
|Geänderte Rolle der Mitglieder im Team  <br/> |MemberRoleChanged  <br/> |Ein Teambesitzer ändert die Rolle von Mitgliedern in einem Team. Die folgenden Werte geben den dem Benutzer zugewiesenen Rollentyp an.<br/><br/><br/> **1** – gibt die Rolle des Besitzers an.<br/>**2** – gibt die Rolle des Mitglieds an. <br/>**3** -gibt die Gastrolle an. <br/>Die Members-Eigenschaft enthält auch den Namen Ihrer Organisation und die e-Mail-Adresse des Mitglieds.  <br/> |
|Einstellung für das geänderte Team  <br/> |TeamSettingChanged  <br/> | Der TeamSettingChanged-Vorgang wird protokolliert, wenn die folgenden Aktivitäten von einem Teambesitzer ausgeführt werden. Für jede dieser Aktivitäten wird eine Beschreibung der geänderten Einstellung (in Klammern unten) in der Spalte **Element** in den Suchergebnissen des Überwachungsprotokolls angezeigt.<br/><br/>-Ändert den Zugriffstyp für ein Team. Teams können als privat oder öffentlich festgelegt werden ( **Team Zugriffstyp**). Wenn ein Team privat ist (Standardeinstellung), können Benutzer nur auf Einladung auf das Team zugreifen. Wenn ein Team öffentlich ist, kann es von allen Benutzern ermittelt werden.<br/><br/>-Ändert die Klassifikation der Informationen eines Teams ( **Team Klassifizierung**).  <br/>  Team Daten können beispielsweise als hohe geschäftliche Auswirkungen, mittlere geschäftliche Auswirkungen oder geringe geschäftliche Auswirkungen klassifiziert werden.<br/><br/>-Ändert den Namen eines Teams ( **Teamname**).  <br/><br/>-Ändert die Team Beschreibung ( **Team Description**). <br/><br/>-Änderungen an den Team Einstellungen. Ein Teambesitzer kann auf diese Einstellungen in einem Teams-Client zugreifen, indem er mit der rechten Maustaste auf ein Team klickt, auf **Team verwalten**klickt und dann auf die Registerkarte **Einstellungen** klickt. Für diese Aktivitäten wird der Name der geänderten Einstellung in der Spalte **Element** in den Suchergebnissen des Überwachungsprotokolls angezeigt.<br/> |
|Erstelltes Team  <br/> |TeamCreated  <br/> |Ein Benutzer erstellt ein neues Team.  <br/> |
|Gelöschter Kanal  <br/> |ChannelDeleted  <br/> |Ein Benutzer löscht einen Kanal aus einem Team.  <br/> |
|Gelöschtes Team  <br/> |TeamDeleted  <br/> |Ein Teambesitzer löscht ein Team.  <br/> |
|Entfernte bot aus dem Team  <br/> |BotRemovedFromTeam  <br/> |Ein Benutzer entfernt einen bot aus einem Team.  <br/> |
|Entfernter Connector  <br/> |ConnectorRemoved  <br/> |Ein Benutzer entfernt den Konnektor aus einem Kanal.  <br/> |
|Mitglieder aus Team entfernt  <br/> |MemberRemoved  <br/> |Ein Teambesitzer entfernt Mitglieder aus einem Team.  <br/> |
|Entfernte Registerkarte  <br/> |TabRemoved  <br/> |Ein Benutzer entfernt eine Registerkarte aus einem Kanal.  <br/> |
|Aktualisierter Connector  <br/> |ConnectorUpdated  <br/> |Ein Benutzer hat einen Konnektor in einem Kanal geändert.  <br/> |
|Aktualisierte Registerkarte  <br/> |TabUpdated  <br/> |Ein Benutzer hat eine Registerkarte in einem Kanal geändert.  <br/> |
|Benutzer angemeldet bei Teams  <br/> |TeamsSessionStarted  <br/> |Ein Benutzer meldet sich bei einem Microsoft Teams-Client an.  <br/> |
||||

### <a name="yammer-activities"></a>Aktivitäten mit jammern
  
In der folgenden Tabelle sind die Benutzer-und Administratoraktivitäten in jammern aufgeführt, die im Office 365-Überwachungsprotokoll protokolliert werden. Wenn Sie Aktivitäten im Zusammenhang mit dem Office 365-Überwachungsprotokoll zurückgeben möchten, müssen Sie in der Liste **Aktivitäten** die Option **Ergebnisse für alle Aktivitäten anzeigen** auswählen. Verwenden Sie die Felder Datumsbereiche und **Benutzer** , um die Suchergebnisse einzuschränken. 
  
|**Anzeigename**|**Operation**|**Beschreibung**|
|:-----|:-----|:-----|
|Geänderte Datenaufbewahrungsrichtlinie  <br/> |SoftDeleteSettingsUpdated  <br/> |Verifizierte Administrator aktualisiert die Einstellung für die Richtlinie zur Netzwerkdaten Aufbewahrung entweder auf Hard Delete oder auf Weiche Löschung. Nur verifizierte Administratoren können diesen Vorgang ausführen.  <br/> |
|Geänderte Netzwerkkonfiguration  <br/> |NetworkConfigurationUpdated  <br/> |Netzwerk oder überprüfter Administrator ändert die Konfiguration des Jammer-Netzwerks. Dazu gehört das Festlegen des Intervalls für den Export von Daten und Aktivieren des Chats.  <br/> |
|Geänderte Netzwerkprofil Einstellungen  <br/> |ProcessProfileFields  <br/> |Netzwerk-oder verifizierte Administratoren ändern die Informationen, die in Mitglieds Profilen für Netzwerkbenutzer Netzwerk angezeigt werden.  <br/> |
|Privater Inhalts Modus geändert  <br/> |SupervisorAdminToggled  <br/> |Verifizierter Administrator aktiviert oder deaktiviert den *privaten Inhalts Modus* . In diesem Modus können Administratoren Beiträge in privaten Gruppen anzeigen und private Nachrichten zwischen einzelnen Benutzern (oder Benutzergruppen) anzeigen. Nur verifizierte Administratoren können diesen Vorgang nur ausführen.<br/> |
|Geänderte Sicherheitskonfiguration  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Verifizierte Administrator aktualisiert die Sicherheitskonfiguration des Jammer-Netzwerks. Hierzu gehören das Festlegen von Kennwortablauf Richtlinien und Einschränkungen für IP-Adressen. Nur verifizierte Administratoren können diesen Vorgang ausführen.  <br/> |
|Erstellte Datei  <br/> |FileCreated  <br/> |Ein Benutzer lädt eine Datei hoch.  <br/> |
|Erstellte Gruppe  <br/> |GroupCreation  <br/> |Der Benutzer erstellt eine neue Gruppe.  <br/> |
|Gelöschte Gruppe  <br/> |GroupDeletion  <br/> |Eine Gruppe wird aus jammern gelöscht.  <br/> |
|Gelöschte Nachricht  <br/> |MessageDeleted  <br/> |Der Benutzer löscht eine Nachricht.  <br/> |
|HeruntergeLadene Datei  <br/> |FileDownloaded  <br/> |Der Benutzer lädt eine Datei herunter.  <br/> |
|Exportierte Daten  <br/> |DataExport  <br/> |Verifizierte admin exportiert Jammer Netzwerkdaten. Nur verifizierte Administratoren können diesen Vorgang ausführen.  <br/> |
|FreigeGebene Datei  <br/> |FileSharing  <br/> |Der Benutzer teilt eine Datei mit einem anderen Benutzer.  <br/> |
|Gesperrter Netzwerkbenutzer  <br/> |NetworkUserSuspended  <br/> |Das Netzwerk oder der verifizierte Administrator suspendiert (deaktiviert) einen Benutzer aus jammern.  <br/> |
|Angehaltene Benutzer  <br/> |UserSuspension  <br/> |Das Benutzerkonto ist angehalten (deaktiviert).  <br/> |
|Aktualisierte Dateibeschreibung  <br/> |FileUpdateDescription  <br/> |Der Benutzer ändert die Beschreibung einer Datei.  <br/> |
|Dateiname aktualisiert  <br/> |FileUpdatename  <br/> |Der Benutzer ändert den Namen einer Datei.  <br/> |
|Angezeigte Datei  <br/> |FileVisited  <br/> |Benutzer zeigt eine Datei an.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Microsoft Flow-Aktivitäten

Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Flow durchsuchen. Zu diesen Aktivitäten gehört das Erstellen, bearbeiten und Löschen von Flows sowie das Ändern von Flow-Berechtigungen. Informationen zur Überwachung von Flow-Aktivitäten finden Sie in den Blog- [Microsoft Flow-Überwachungsereignissen, die jetzt im Office 365 Security _AMP_ Compliance Center verfügbar sind](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Sie können das Überwachungsprotokoll nach App-bezogenen Aktivitäten in PowerApps durchsuchen. Zu diesen Aktivitäten gehört das Erstellen, starten und Veröffentlichen einer App. das Zuweisen von Berechtigungen zu apps wird ebenfalls überwacht. Eine Beschreibung aller PowerApps-Aktivitäten finden Sie unter [Aktivitätsprotokollierung für PowerApps](https://docs.microsoft.com/en-us/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Microsoft Stream-Aktivitäten
  
Sie können das Überwachungsprotokoll nach Aktivitäten in Microsoft Stream durchsuchen. Zu diesen Aktivitäten gehört das Ausführen von Video Aktivitäten durch Benutzer, Gruppenkanal Aktivitäten und Administratoraktivitäten wie das Verwalten von Benutzern, das Verwalten von Organisationseinstellungen und das Exportieren von Berichten. Eine Beschreibung dieser Aktivitäten finden Sie im Abschnitt "Aktivitäten, die in Microsoft Stream protokolliert werden" in [Überwachungsprotokollen in Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Exchange-Administrator-Überwachungsprotokoll
  
Die Exchange-Administrator-Überwachungsprotokollierung, die standardmäßig in Office 365 aktiviert ist, protokolliert ein Ereignis im Office 365-Überwachungsprotokoll, wenn ein Administrator (oder ein Benutzer, dem Administratorberechtigungen zugewiesen wurden) eine Änderung in Ihrer Exchange Online-Organisation vorgenommen hat. Änderungen, die mithilfe der Exchange-Verwaltungskonsole oder durch Ausführen eines Cmdlets in Windows PowerShell vorgenommen wurden, werden im Exchange-administratorüberwachungsprotokoll protokolliert. Detailliertere Informationen zur Administrator-Überwachungsprotokollierung in Exchange finden Sie unter [Administrator-Überwachungsprotokollierung](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Im folgenden finden Sie einige Tipps zum Suchen von Aktivitäten im Exchange-Administrator-Überwachungsprotokoll:
  
- Wenn Sie Einträge aus dem Exchange-Administrator-Überwachungsprotokoll zurückgeben möchten, müssen Sie in der Liste **Aktivitäten** die Option **Ergebnisse für alle Aktivitäten anzeigen** auswählen. Verwenden Sie die Felder Datumsbereich und **Benutzer** , um die Suchergebnisse für Cmdlets einzuschränken, die von einem bestimmten Exchange-Administrator innerhalb eines bestimmten Datumsintervalls ausgeführt werden. 
    
- Um Ereignisse aus dem Exchange-administratorüberwachungsprotokoll anzuzeigen, Filtern Sie die Suchergebnisse, **-** und geben Sie im Feld **Aktivitäts** Filter einen (Strich) ein. Dadurch werden die Cmdlet-Namen angezeigt, die in der Spalte **Aktivität** für Exchange-Verwaltungsereignisse angezeigt werden. Anschließend können Sie die Cmdlet-Namen in alphabetischer Reihenfolge sortieren. 
    
    ![Geben Sie im feldaktivitäten einen Strich ein, um die Exchange-Verwaltungsereignisse zu filtern](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Um Informationen darüber zu erhalten, welches Cmdlet ausgeführt wurde, welche Parameter und Parameterwerte verwendet wurden und welche Objekte betroffen waren, müssen Sie die Suchergebnisse exportieren und die Option **alle Ergebnisse herunterladen** auswählen. 
    
- Sie können Ereignisse auch im Exchange Admin-Überwachungsprotokoll anzeigen, indem Sie das Exchange Admin Center verwenden. Weitere Informationen finden Sie unter [Anzeigen des administratorüberwachungsprotokolls](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wo finde ich Informationen zu den Features, die der Überwachungsdienst in Office 365 bietet?**

Weitere Informationen zu den in Office 365 verfügbaren Überwachungs-und Berichterstattungsfunktionen finden Sie unter [Überwachung und Berichterstellung in office 365](office-365-auditing-and-reporting-overview.md). 

**Was sind unterschiedliche Office 365-Dienste, die derzeit überwacht werden?**

Die am häufigsten verwendeten Office 365-Dienste wie Exchange Online, SharePoint, OneDrive, Azure Active Directory, Microsoft Teams, CRM, erweiterter BedrohungsSchutz und verHinderung von Datenverlust werden überwacht. Eine vollständige Liste finden Sie im [Intro](#search-the-audit-log-in-the-office-365-security-amp-compliance-center) -Abschnitt in diesem Artikel.

**Welche Aktivitäten werden vom Überwachungsdienst in Office 365 überwacht?**

Eine Liste und Beschreibung der in Office 365 überwachten Aktivitäten finden Sie im Abschnitt über [wachte Aktivitäten](#audited-activities) in diesem Artikel.

**Wie lange dauert es, bis ein Überwachungsdatensatz verfügbar ist, nachdem ein Ereignis aufgetreten ist?**

Die meisten Überwachungsdaten sind innerhalb von 30 Minuten verfügbar, es kann jedoch bis zu 24 Stunden dauern, bis der entsprechende Überwachungsprotokolleintrag in den Suchergebnissen angezeigt wird. In der Tabelle im Abschnitt [bevor Sie beginnen](#before-you-begin) dieses Artikels wird gezeigt, wie lange es dauert, bis Ereignisse in den verschiedenen Office 365-Diensten verfügbar sind.

**Wie lange werden die Überwachungseinträge aufbewahrt?**

Wie bereits erläutert, hängt die Aufbewahrungsdauer für Überwachungsdatensätze vom Office 365-Abonnement Ihrer Organisation ab.  

- **Office 365 E3** -Überwachungsdatensätze werden für 90 Tage aufbewahrt.

- **Office 365 E5** -Überwachungsdatensätze werden für 365 Tage (ein Jahr) aufbewahrt. Das aufBewahren von Überwachungsdatensätzen für ein Jahr steht auch für Organisationen zur Verfügung, die über ein E3-Abonnement und ein Office 365 Advanced Compliance-Add-on-Abonnement verfügen.

     > [!NOTE]
     > Wie bereits erläutert, ist die Aufbewahrungsdauer für ein Jahr für die Überwachungsdatensätze für E5-Organisationen (oder E3-Organisationen mit erweiterten Compliance-Add-on-Lizenzen) derzeit nur als Teil eines privaten Vorschau Programms verfügbar. Wenn Sie sich für dieses Vorschau Programm anmelden möchten, geben Sie eine Anforderung beim [Microsoft-Support](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) ein, und fügen Sie Folgendes als Beschreibung der benötigten Hilfe zu: "Long-term Office 365 Audit Log private Preview".

Beachten Sie, dass die Dauer des Aufbewahrungszeitraums für Überwachungsdatensätze auf der benutzerbasierten Lizenzierung basiert. Wenn beispielsweise einem Benutzer in Ihrer Organisation eine Office 365 E3-Lizenz zugewiesen ist, werden die Überwachungsdatensätze für die von diesem Benutzer ausgeführten Aktivitäten für 90 Tage aufbewahrt. Wenn einem anderen Benutzer eine Office 365 E5-Lizenz zugewiesen ist, werden die Überwachungsdatensätze für ein Jahr aufbewahrt. 

**Kann ich programmgesteuert auf die Überwachungsdaten zugreifen?**

Ja. Die Office 365-Verwaltungs Aktivitäts-API wird zum programmgesteuerten Abrufen der Überwachungsprotokolle verwendet.  Informationen zu den ersten Schritten finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Gibt es andere Möglichkeiten zum Abrufen von Überwachungsprotokollen außer der Verwendung des Office 365 Security & Compliance Centers oder der Office 365-Verwaltungs Aktivitäts-API?**

Nein. Dies sind die einzigen beiden Möglichkeiten zum Abrufen von Daten aus dem Office 365-Überwachungsdienst. 

**Muss die Überwachung in jedem Dienst, für den Überwachungsprotokolle erfasst werden sollen, einzeln aktiviert werden?**

In den meisten Office 365-Diensten ist die Überwachung standardmäßig aktiviert, nachdem Sie die Überwachung für Ihre Office 365-Organisation (wie im Abschnitt [bevor Sie beginnen](#before-you-begin) in diesem Artikel beschrieben) aktivieren. Sie müssen jedoch die postfachüberwachung in Exchange Online für jedes Postfach aktivieren, das Sie überwachen möchten.   Wir arbeiten daran, die postfachüberwachung standardmäßig für alle Postfächer in einer Office 365-Organisation zu aktivieren. Weitere Informationen finden Sie unter "Exchange-postfachüberwachung wird standardmäßig aktiviert" im [Microsoft-Blog für Sicherheit, Datenschutz und Kompatibilität](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171).

**Unterstützt der Office 365-Überwachungsdienst die Deduplizierung von Datensätzen?**

Nein. Die Überwachungsdienst-Pipeline ist nahezu in Echtzeit und kann daher keine Deduplizierung unterstützen.
 
**Wird in Office 365 der Datenfluss über geographies hinweg überwacht?**

Nein. Derzeit haben wir Überwachungs Pipeline-Bereitstellungen in den Regionen NA (Nordamerika), EMEA (Europa, Mittlerer Osten und Afrika) und APAC (Asia Pacific). Allerdings können wir die Daten in diesen Regionen für den Lastenausgleich und nur während der Live-Website-Probleme übertragen. Wenn wir diese Aktivitäten ausführen, werden die Daten in Transit verschlüsselt.   
 
**Werden Überwachungsdaten verschlüsselt?**

Überwachungsdaten werden in Exchange-Postfächern (Rest-Daten) in derselben Region gespeichert, in der die Überwachungs Pipeline bereitgestellt wird. Diese Daten werden nicht verschlüsselt. Daten werden jedoch immer verschlüsselt. 













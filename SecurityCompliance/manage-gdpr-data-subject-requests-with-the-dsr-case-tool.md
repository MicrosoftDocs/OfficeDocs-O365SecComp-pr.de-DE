---
title: Verwalten von DSGVO-Datensubjekt Anforderungen mit dem DSR Case Tool im Office 365 &amp; Security Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/25/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: Der DSGVO gibt EU-Bürgern (als betroffene Personen bezeichnet) spezifische Rechte für Ihre persönlichen Daten; zu diesen Rechten gehört das Abrufen von Kopien davon, das Anfordern von Änderungen, das Einschränken der Verarbeitung, das Löschen oder das empfangen in einem elektronischen Format. Eine formelle Anforderung durch eine betroffene Person, eine Aktion zu Ihren personenbezogenen Daten durchführen zu können, wird als Datensubjekt Anforderung oder DSR bezeichnet. Sie können DSR-Fälle im Office 365 Security &amp; Compliance Center verwenden, um die DSR-Untersuchungen Ihrer Organisation zu verwalten.
ms.openlocfilehash: 8338ca2eed4f5120571f642a1cbb4408ce36e2c3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213495"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-office-365-security-amp-compliance-center"></a>Verwalten von DSGVO-Datensubjekt Anforderungen mit dem DSR Case Tool im Office 365 &amp; Security Compliance Center

Bei der EU-allgemeinen Datenschutzverordnung (DSGVO) geht es um den Schutz und die Aktivierung der Datenschutz Rechte der einzelnen Personen innerhalb der Europäischen Union (EU). Das DSGVO gibt Personen in der Europäischen Union (als betroffene bezeichnet) das Recht, Ihre personenbezogenen Daten zu öffnen, abzurufen, zu korrigieren, zu löschen und zu verbieten. Personenbezogene Daten sind unter dem DSGVO alle Informationen, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Eine formelle Anfrage einer Person an Ihre Organisation, eine Aktion zu Ihren personenbezogenen Daten durchführen zu können, wird als Datensubjekt Anforderung oder DSR bezeichnet. Ausführliche Informationen zur Reaktion auf DSRs für Daten in Office 365 finden Sie unter [office 365 Data Subject Request Guide](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Um Untersuchungen als Reaktion auf einen von einer Person in Ihrer Organisation übermittelten DSR zu verwalten, können Sie das DSR Case Tool im &amp; Office 365 Security Compliance Center verwenden, um Inhalte zu finden, die in gespeichert sind:
  
- Jedes Benutzerpostfach in Ihrer Organisation. Dazu gehören Skype for Business-Unterhaltungen und eins-zu-eins-Chats in Microsoft Teams.
    
- Alle Postfächer, die einer Office 365-Gruppe und allen Team Postfächern in Microsoft Teams zugeordnet sind
    
- Alle SharePoint Online-Websites und OneDrive for Business-Konten in Ihrer Organisation
    
- Alle Teams-Websites und Office 365-Gruppen Websites in Ihrer Organisation
    
- Alle öffentlichen Ordner in Exchange Online
    
Mit dem DSR Case Tool können Sie Folgendes tun:
  
- Erstellen Sie eine separate Anfrage für jede Untersuchung einer Anforderung einer betroffenen Person.
    
- Steuern, wer Zugriff auf den DSR-Fall hat, indem Personen als Mitglieder des Falls hinzugefügt werden; nur Mitglieder können auf den Fall zugreifen und können ihre Fälle nur in der Liste der Fälle auf der Seite mit den **DSR** -Fällen &amp; im Security Compliance Center anzeigen. Darüber hinaus können Sie verschiedenen Mitgliedern des gleichen falls unterschiedliche Berechtigungen zuweisen. Sie können beispielsweise zulassen, dass einige Mitglieder nur die Groß-/Kleinschreibung und Suchergebnisse anzeigen und anderen Mitgliedern die Suche und den Export von Suchergebnissen gestatten. 
    
- Verwenden Sie die integrierte Suche, um nach allen Inhalten zu suchen, die von einem bestimmten Datensubjekt erstellt oder hochgeladen wurden.
    
- Überprüfen Sie optional die integrierte Suchabfrage, und führen Sie die Suche erneut aus, um die Suchergebnisse einzuschränken.
    
- Fügen Sie zusätzliche Inhalts Suchvorgänge hinzu, die mit dem DSR-Fall verbunden sind. Hierzu gehören das Erstellen von Suchvorgängen, die teilweise indizierte Elemente und vom System generierte Protokolle aus My Analytics und dem Office-Roamingdienst zurückgeben.
    
- Exportieren von Daten als Reaktion auf eine DSR-Access-oder Exportanforderung.
    
- Löschen von Fällen, wenn der DSR-Ermittlungsprozess abgeschlossen ist; Dadurch werden alle Suchvorgänge und Exportaufträge für den Fall entfernt.
    
Hier ist der allgemeine Prozess für die Verwendung des DSR-Fall Tools zur Verwaltung von DSR-Untersuchungen:
  
[Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Schritt 2: Erstellen eines DSR-Falls und Hinzufügen von Mitgliedern](#step-2-create-a-dsr-case-and-add-members)

[Schritt 3: Ausführen der Suchabfrage](#step-3-run-the-search-query)

[Schritt 4: Exportieren der Daten](#step-4-export-the-data)

[Optional Schritt 5: überArbeiten der integrierten Suchabfrage](#optional-step-5-revise-the-built-in-search-query)

[Weitere Informationen zur Verwendung des DSR Case-Tools](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Unsere Tools helfen Administratoren bei der Durchführung von Anforderungen an den DSR-Zugriff oder-Export, indem Sie die integrierte Such-und Exportfunktionalität des DSR Case-Tools nutzen können. Das Tool hilft bei der Erleichterung einer Best-Effort-Methode, um Daten zu exportieren, die für eine von einer betroffenen Person übermittelte DSR-Anforderung relevant sind. Es ist jedoch wichtig zu beachten, dass die Suchergebnisse abhängig von der betroffenen Person oder den ausgeführten Verwaltungsaktionen variieren können, die sich auswirken können, ob ein Element zu Export Zwecken als "personenbezogene Daten" angesehen wird. Wenn die betroffene Person beispielsweise zuletzt eine Datei geändert hat, die Sie nicht erstellt haben, wird die Datei möglicherweise nicht in den Suchergebnissen zurückgegeben. Auf ähnliche Weise kann ein Administrator Daten exportieren, ohne teilweise indizierte Elemente oder alle Versionen von SharePoint-Dokumenten einzuschließen. Daher können die bereitgestellten Tools den Zugriff und den Export von Datenanforderungen erleichtern. die Ergebnisse unterliegen jedoch bestimmten Nutzungsszenarien für Administratoren und betroffene. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern

Standardmäßig kann ein globaler Office 365-Administrator im Security &amp; Compliance Center auf das DSR Case-Tool zugreifen. Andere Benutzer wie ein Datenschutzbeauftragter, ein Personalleiter oder andere an den DSR-Untersuchungen beteiligte Personen haben keinen Zugriff auf das DSR-Fall Tool und müssen über die entsprechenden Berechtigungen für den Zugriff auf das Tool verfügen. Am einfachsten können Sie dies tun, indem Sie zur Seite **Berechtigungen** im Security &amp; Compliance Center wechseln und Benutzer zur eDiscovery-Manager-Rollengruppe hinzufügen. Beachten Sie, dass Sie diese Berechtigungen auch zuweisen müssen, damit Sie als Mitglieder des in Schritt 2 erstellten DSR-Falls hinzugefügt werden können. 
  
Schrittweise Anleitungen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 &amp; Security Compliance Center](assign-ediscovery-permissions.md).
  
> [!NOTE]
> Standardmäßig verfügen ein globaler Office 365-Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" im &amp; Security Compliance Center nicht über die erforderlichen Berechtigungen zum Exportieren von Inhalts Suchergebnissen (siehe Schritt 4 in diesem Artikel). Um dies zu beheben, kann ein Administrator sich selbst als Mitglied der eDiscovery-Manager-Rollengruppe hinzufügen. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Schritt 2: Erstellen eines DSR-Falls und Hinzufügen von Mitgliedern

Der nächste Schritt besteht darin, einen DSR-Fall zu erstellen. Wenn Sie einen Fall erstellen, können Sie die integrierte Suche starten, oder Sie können den Fall erstellen, ohne die Suche zu starten. Im folgenden Verfahren werden Sie aufgefordert, den Fall zu erstellen, ohne die Suche zu starten, und dann zu zeigen, wie Sie der Groß-/Kleinschreibung Mitglieder hinzufügen.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich bei Office 365 mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Klicken Sie im &amp; Security Compliance Center auf **Datenschutz** \> **Antragsteller Anforderungen**, und klicken ![Sie dann](media/ITPro-EAC-AddIcon.gif) auf Symbol hinzufügen **neuer DSR-Fall**.
    
3. Geben Sie auf der Seite **Neues DSR-Fall** Flyout den Fall einen Namen ein, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **weiter**. Beachten Sie, dass der Name des Falls in Ihrer Organisation eindeutig sein muss.
    
    > [!TIP]
    > Erwägen Sie, den Namen der Person hinzuzufügen, die die DSR-Anfrage übermittelt hat, die Sie im Namen und/oder der Beschreibung des neuen Falls untersuchen. Beachten Sie, dass nur Mitglieder dieses Falls (und eDiscovery-Administratoren) den Fall in der Liste der Fälle auf der Seite **Datensubjekt Anforderungen** sehen können. 
  
4. Wählen Sie auf der Seite **Anforderungsdetails** unter **Datensubjekt (die Person, die diese Anforderung eingereicht hat)** die Person aus, für die Sie Daten suchen und exportieren möchten, und klicken Sie dann auf **weiter**.
    
5. Auf der Seite " **Ihre Fall Einstellungen bestätigen** " können Sie den Fallnamen und die Beschreibung ändern und einen anderen Betreff auswählen. Klicken Sie andernfalls einfach auf **Speichern**.
    
    Es wird eine Seite angezeigt, die bestätigt, dass der neue DSR-Fall erstellt wurde.
    
    ![Die Suche starten oder einfach die neue DSR-fallseite abschließen](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    Zu diesem Zeitpunkt können Sie eine der folgenden Aktionen ausführen:
    
    a. durch Klicken auf **Zeige mir Suchergebnisse** wird die Suche gestartet. Dies ist die Standardauswahl. Die integrierte Suche, die ausgeführt wird, wenn Sie diese Option auswählen, und die zurückgegebenen Ergebnisse werden in Schritt 3 erläutert.
    
    b. Wenn Sie auf **Fertig stellen** klicken, wird der neue DSR-Fall geschlossen, ohne die integrierte Suche zu starten. Wenn Sie diese Option auswählen, wird der neue DSR-Fall auf der Seite **Datensubjekt Anforderungen** angezeigt.
    
6. Klicken Sie auf **Fertig stellen** , um zum neuen DSR-Fall zu wechseln und Mitglieder hinzuzufügen. 
    
7. Klicken Sie auf der Seite **Datensubjekt Anforderungen** auf den Namen des soeben erstellten DSR-Falls. 
    
8. Klicken Sie auf der Seite **dieses Fall Flyout verwalten** unter **Mitglieder verwalten**auf **Hinzufügen**. 
    
    Unter **Benutzer**wird eine Liste der Personen angezeigt, denen die entsprechenden eDiscovery-Berechtigungen zugewiesen wurden. Beachten Sie, dass die Personen, denen Sie in Schritt 1 eDiscovery-Berechtigungen zugewiesen haben, in dieser Liste angezeigt werden. 
    
9. Wählen Sie die Personen aus, die als Mitglieder des DSR-Falls hinzugefügt werden sollen, klicken Sie auf **Hinzufügen**, und speichern Sie die Änderungen.
    
    Beachten Sie, dass Sie auch Rollengruppen als Mitglieder der DSR-Groß-/Kleinschreibung hinzufügen können, indem Sie unter **Rollengruppen verwalten**auf **Hinzufügen** klicken. 
    
## <a name="step-3-run-the-search-query"></a>Schritt 3: Ausführen der Suchabfrage

Nachdem Sie einen DSR-Fall erstellt und Mitglieder hinzugefügt haben, besteht der nächste Schritt darin, die integrierte Suche auszuführen, die dem Fall zugeordnet ist. Diese Standardsuch Abfrage führt die folgenden Aktionen aus:
  
- DurchSucht alle Postfächer in Ihrer Organisation nach allen e-Mail-Elementen, die von der betroffenen Person gesendet oder empfangen wurden. Dies geschieht mithilfe der e-Mail-Eigenschaft der *Teilnehmer* , die in allen Personen Feldern in einer e-Mail-Nachricht nach der betroffenen Person sucht. Diese Eigenschaft gibt Elemente zurück, in denen sich der betroffene in den Feldern **from**, **to**, **CC**und **Bcc** befindet. Öffentliche Ordner in Exchange Online werden auch nach Nachrichten durchsucht, die von der betroffenen Person gesendet oder empfangen wurden. 
    
- DurchSucht alle Websites in Ihrer Organisation nach Dokumenten und Elementen, die von der betroffenen Person erstellt oder hochgeladen wurden. Hierzu werden die folgenden Websiteeigenschaften verwendet:
    
  - Die *Author* -Eigenschaft gibt Elemente zurück, bei denen die betroffene Person im Feld Autor in Office-Dokumenten aufgeführt wird. Dieser Wert bleibt auch dann erhalten, wenn das Dokument von einer anderen Person kopiert und hochgeladen wird. 
    
  - Die *CreatedBy* -Eigenschaft gibt Elemente zurück, die von der betroffenen Person erstellt oder hochgeladen wurden. 
    
Hier sehen Sie, wie die Stichwortabfrage für die integrierte Suche aussieht, die automatisch erstellt wird, wenn Sie einen DSR-Fall erstellen.
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Wenn beispielsweise der Name der betroffenen Person Ina Leonte ist, würde die Stichwortabfrage wie folgt aussehen:
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **So führen Sie die integrierte Suche nach einem DSR-Fall aus:**
  
1. Klicken Sie im &amp; Security Compliance Center auf **Datenschutz** \> **Antragsteller-Anforderungen**, und klicken Sie dann neben dem in Schritt 2 erstellten DSR-Fall auf **Öffnen** . 
    
    Klicken Sie oben auf der Seite auf die Registerkarte **Suchen** , und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des neuen DSR-Falls erstellt wurde. Hinweis die Suche hat den gleichen Namen wie der DSR-Fall. 
    
2. Klicken Sie auf der Seite Such Flyout auf **Abfrage öffnen**.
    
    Wenn Sie die Abfrage öffnen, wird die Suche gestartet und in wenigen Momenten abgeschlossen. 
    
3. Klicken Sie nach Abschluss der Suche auf **Ergebnisse anzeigen** , um eine Vorschau der Suchergebnisse anzuzeigen. Weitere Informationen finden Sie unter [Vorschau der Suchergebnisse](content-search.md#preview-search-results).
    
    > [!TIP]
    > Sie können auch die Suchabfrage Statistik anzeigen, um die Anzahl der von der Suche zurückgegebenen Post Fach-und Websiteelemente sowie die wichtigsten inhaltsspeicherorte anzuzeigen, die Elemente enthalten, die mit der Suchabfrage übereinstimmen. Weitere Informationen finden Sie unter [Anzeigen von Informationen und Statistiken zu einer Suche](content-search.md#view-information-and-statistics-about-a-search). 
  
Sie können die integrierte Suchabfrage bearbeiten, die durchsuchten inhaltsspeicherorte ändern und dann die Suche erneut ausführen. Weitere Informationen finden Sie in [Schritt 5](#optional-step-5-revise-the-built-in-search-query) . 
  
## <a name="step-4-export-the-data"></a>Schritt 4: Exportieren der Daten

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie die Suchergebnisse exportieren. Alternativ können Sie, bevor Sie die Daten exportieren, die Abfrage überarbeiten, um die Anzahl der Suchergebnisse zu reduzieren. Weitere Informationen zum Einschränken der Suchergebnisse finden Sie in Schritt 5.
  
Wenn Sie Suchergebnisse exportieren, können Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen werden. Wenn Sie Inhalte aus SharePoint-und OneDrive-Konten exportieren, werden Kopien von systemeigenen Office-Dokumenten und anderen Dokumenten exportiert. Eine Ergebnisdatei, die Informationen zu jedem exportierten Element enthält, ist auch in den Suchergebnissen enthalten. Ausführlichere Informationen zum Exportieren finden Sie unter [Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md).
  
> [!NOTE]
> Standardmäßig verfügen ein globaler Office 365-Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" im &amp; Security Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Inhalts Suchergebnissen. Um dies zu beheben, kann ein Administrator sich selbst als Mitglied der eDiscovery-Manager-Rollengruppe hinzufügen. 
  
Der Computer, den Sie zum Exportieren von Daten verwenden, muss die folgenden Systemanforderungen erfüllen:
  
- 32- oder 64-Bit-Versionen von Windows 7 und höher
    
- Microsoft .NET Framework 4,7
    
- Einen unterstützten Browser:
    
  - Microsoft Edge
    
    Oder
    
  - Microsoft Internet Explorer 10 und höhere Versionen
    
    > [!NOTE]
    > Microsoft stellt keine Drittanbietererweiterungen oder Add-ons für ClickOnce-Anwendungen her. Das Exportieren von Daten mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder Add-ons wird nicht unterstützt. 
  
 **So exportieren Sie Daten aus der integrierten Suche in einem DSR-Fall:**
  
1. Klicken Sie im &amp; Security Compliance Center auf **Datenschutz** \> **Antragsteller-Anforderungen**, und klicken Sie dann neben dem DSR-Fall, für den Sie Daten exportieren möchten, auf **Öffnen** . 
    
2. Klicken Sie oben auf der Seite auf die Registerkarte **Suchen** , und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des DSR-Falls erstellt wurde. Oder klicken Sie auf eine andere Suche, um Daten aus dieser Suche zu exportieren. 
    
3. Klicken Sie ![auf der Seite Such Flyout auf Suchergebnis Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mehr**exportieren, und wählen Sie dann **Ergebnisse** aus der Dropdownliste aus. 
    
4. Wählen Sie auf der Seite **Ergebnisse exportieren** die folgenden empfohlenen Optionen für DSR-Exportanforderungen aus. 
    
    ![Konfigurieren der Exporteinstellungen](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. Wählen Sie unter **Ausgabeoptionen**die erste Option aus ( **alle Elemente, ausgenommen solche, die über ein unbekanntes Format verfügen, verschlüsselt oder aus anderen Gründen nicht indiziert**wurden), um nur indizierte Elemente zu exportieren. Der Grund, warum Sie nicht teilweise indizierte Elemente aus der integrierten Suche exportieren möchten, liegt darin, dass teilweise indizierte Elemente von anderen Benutzern exportiert werden. Wenn Sie nur die teilweise indizierten Elemente für die betroffene Person exportieren möchten, wird empfohlen, eine separate Suche zu erstellen. Weitere Informationen finden Sie unter [exportieren teilweise indizierter Elemente](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) im Abschnitt "Weitere Informationen zur Verwendung des DSR Case-Tools".
    
    b. Wählen Sie unter **Exchange-Inhalt exportieren als**die dritte Option aus, **eine PST-Datei, die alle Nachrichten in einem einzelnen Ordner enthält**. Da einige der Ergebnisse möglicherweise für Elemente vorhanden sind, die aus dem Postfach eines anderen Benutzers stammen, wird diese Option nur das Element in einem einzelnen Ordner aufgelistet, ohne das tatsächliche Postfach anzugeben, und ist die beste Option, die Sie verwenden können, wenn Sie die im nächsten Artikel empfohlenen Ergebnisse deaktivieren. . Diese Option ermöglicht es der betroffenen Person auch, Elemente in chronologischer Reihenfolge zu überarbeiten (Elemente werden nach gesendetem Datum sortiert), ohne dass Sie in der ursprünglichen Postfachordnerstruktur für jedes Element navigieren müssen.
    
    c. Wählen Sie Deduplizierung **aktivieren** aus, um doppelte e-Mail-Nachrichten auszuschließen. Diese Option wird empfohlen, da durch die integrierte Suche alle Postfächer in Ihrer Organisation durchsucht werden. Wenn also mehrere Kopien derselben Nachricht in den Postfächern gefunden werden, die durchsucht wurden, wird mit dieser Option nur eine Kopie einer Nachricht exportiert. Diese Option führt zusammen mit dem Exportieren von Nachrichten in einer PST-Datei in einem einzelnen Ordner zu einer optimalen Benutzererfahrung für Anforderungen an die DSR-Exportanforderung. Beachten Sie, dass im Bericht results. CSV Export alle Speicherorte aufgeführt werden, an denen doppelte Nachrichten gefunden wurden.
    
    Optional können Sie die Option **Versionen für SharePoint-Dokumente einbeziehen** auswählen, um alle Versionen von SharePoint-und OneDrive-Dokumenten zu exportieren. Dies erfordert, dass die Versionsverwaltung für Dokumentbibliotheken aktiviert ist. Mit dieser Option können Sie sicherstellen, dass alle relevanten Daten exportiert werden.
    
5. Klicken Sie nach Auswahl der Exporteinstellungen auf **exportieren**.
    
    Die Suchergebnisse werden zum Herunterladen bereitgestellt, sodass Sie in den Azure-Speicherbereich für Ihre Organisation in der Microsoft-Cloud hochgeladen werden. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
6. Klicken Sie auf die Registerkarte **Export** , um den soeben erstellten Exportauftrag anzuzeigen. Beachten Sie, dass Exportaufträge den gleichen Namen wie die entsprechende Suche mit **_Export** haben, die am Ende des Suchnamens angehängt ist. 
    
7. Klicken Sie auf den soeben erstellten Exportauftrag, um die Seite zum Exportieren des Flyouts anzuzeigen. Auf dieser Seite werden Informationen zur Suche angezeigt, beispielsweise die Größe und die Gesamtzahl der zu exportierenden Elemente sowie der Prozentsatz der Elemente, die in einen Azure-Speicherbereich übertragen wurden. Klicken Sie auf **Aktualisieren** , um die Informationen zum Uploadstatus zu aktualisieren. 
    
8. Klicken Sie unter **Schlüssel exportieren**auf **in Zwischenablage kopieren**. Sie werden diesen Schlüssel in Schritt 11 verwenden, um die Suchergebnisse herunterzuladen.
    
9. Klicken ![Sie oben auf der](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) Seite zum Exportieren des Flyouts auf Suchergebnis Symbol- **Download Ergebnisse** exportieren. 
    
10. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen** , um das **Microsoft Office 365 EDiscovery-Export Tool**zu öffnen. Das **eDiscovery-Export Tool** wird beim ersten herunterladen der Suchergebnisse installiert. 
    
11. Fügen Sie im **eDiscovery-Export Tool**den Exportschlüssel, den Sie in Schritt 8 kopiert haben, in das entsprechende Feld ein.
    
12. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese-und Schreibvorgänge) sollten Sie die Suchergebnisse auf ein lokales Laufwerk herunterladen. Laden Sie Sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
13. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Export Tool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und der Größe) der verbleibenden zu ladenden Elemente. Nach Abschluss des Exportvorgangs können Sie auf die Dateien am Speicherort zugreifen, an dem Sie heruntergeladen wurden. Weitere Informationen zu den Berichten, die beim Herunterladen von Inhalts Suchergebnissen enthalten sind, finden Sie im Abschnitt " [Weitere Informationen](export-search-results.md#more-information) unter" Exportieren von Inhalts Suchergebnissen &amp; aus dem Office 365 Security Compliance Center ". 
    
Nachdem die Daten exportiert wurden, befinden sich die Suchergebnisse und Export Berichte in einem Ordner mit dem Namen des DSR-Falls. Die PST-Dateien, die Postfachelemente enthalten, befinden sich in einem Unterordner mit dem Namen **Exchange**. Dokumente und andere Elemente aus Websites befinden sich in einem Unterordner mit dem Namen **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>Optional Schritt 5: überArbeiten der integrierten Suchabfrage

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie Sie überarbeiten, um den Bereich so einzugrenzen, dass weniger Suchergebnisse zurückgegeben werden. Hierzu fügen Sie der Abfragebedingungen hinzu. Eine Bedingung ist logisch mit der Schlüsselwortabfrage vom **and-** Operator verbunden. Das muss in den Suchergebnissen zurückgegeben werden, Elemente müssen sowohl die Stichwortabfrage als auch alle hinzugefügten Bedingungen erfüllen. Auf diese Weise können Sie die Ergebnisse einschränken. Wenn Sie zwei oder mehr eindeutige Bedingungen zu einer Suchabfrage hinzufügen (Bedingungen, die verschiedene Eigenschaften angeben), werden diese Bedingungen logisch mit dem **and-** Operator verbunden. Dies führt dazu, dass nur Elemente zurückgegeben werden, die alle Bedingungen (zusätzlich zur Stichwortabfrage) erfüllen. Wenn Sie mehrere Werte (durch Kommas oder Semikolons getrennt) einer einzelnen Bedingung hinzufügen, werden diese Werte durch den **or** -Operator verbunden. Das Ergebnis ist, dass Elemente zurückgegeben werden, wenn Sie einen der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
  
Im folgenden finden Sie einige Beispiele für die Bedingungen, die Sie der integrierten Suchabfrage eines DSR-Gehäuses hinzufügen können. Der Name der tatsächlichen Eigenschaft, die in einer Suchabfrage verwendet wird, wird in Klammern angezeigt.
  
- **Dateityp ( `filetype`)** : gibt die Erweiterung eines Dokuments oder einer Datei an. Verwenden Sie diese Bedingung, um nach Dokumenten und Dateien zu suchen, die von bestimmten Office-Anwendungen wie Word, Excel und OneNote erstellt wurden. 
    
- **Nachrichtentyp ( `kind`)** : gibt den Typ des e-Mail-Elements an, nach dem gesucht werden soll. Sie können die Syntax `kind:email OR kind:im` beispielsweise verwenden, um nur e-Mail-Nachrichten und Skype for Business-Unterhaltungen oder 1:1-Chats in Microsoft Teams zurückzugeben. 
    
- **Compliance-Tag`compliancetag`()** – gibt eine Bezeichnung an, die einer e-Mail-Nachricht oder einem Dokument zugewiesen ist. Diese Bedingung gibt Elemente zurück, die mit einer bestimmten Bezeichnung klassifiziert wurden. Bezeichnungen werden zum Klassifizieren von e-Mails und Dokumenten für die Datensteuerung und zum Erzwingen von Aufbewahrungsregeln basierend auf der Klassifizierung verwendet, die von der Bezeichnung definiert wird. Dies ist eine nützliche Bedingung für DSR-Untersuchungen, da Ihre Organisation möglicherweise Bezeichnungen verwendet, um Inhalte im Zusammenhang mit Datenschutz zu klassifizieren oder personenbezogene Daten oder vertrauliche Informationen enthalten. Verwenden Sie für den Wert dieser Bedingung den vollständigen Bezeichnungsnamen oder den ersten Teil des Bezeichnungsnamens mit einem Platzhalter. Weitere Informationen finden Sie unter [Overview of Labels in Office 365](labels.md).
    
Eine Liste und eine Beschreibung aller im DSR Case Tool verfügbaren Bedingungen finden Sie unter [Suchbedingungen](keyword-queries-and-search-conditions.md#search-conditions) im Artikel "Stichwortabfragen und Suchbedingungen für die Inhaltssuche". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Ändern der durchsuchten inhaltsspeicherorte

Zusätzlich zur Überarbeitung der integrierten Suche für einen DSR-Fall können Sie auch die durchsuchten inhaltsspeicherorte ändern. Wie bereits erläutert, durchsucht die integrierte Suche jedes Postfach und jede Website in der Organisation und alle öffentlichen Exchange Online-Ordner. Beispielsweisekönnten Sie die Suche einschränken, um nur das Postfach und das OneDrive-Konto des betroffenen und ausgewählte SharePoint-Websites zu durchsuchen. Wenn Sie bestimmte Websites durchsuchen möchten, müssen Sie jede Website hinzufügen, die Sie durchsuchen möchten.
  
So ändern Sie die inhaltsspeicherorte für die Suche:
  
1. Öffnen Sie die integrierte Suche, für die Sie die inhaltsspeicherorte ändern möchten.
    
2. Klicken Sie in der Suchabfrage unter **Speicherorte**neben der Option **bestimmte Speicherorte** auf **ändern** . 
    
    ![Klicken Sie auf ändern, um die inhaltsspeicherorte der integrierten Suchabfrage zu ändern.](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Die Seite **Speicherort ändern** -Flyout wird angezeigt. Hier finden Sie eine Beschreibung der inhaltsspeicherorte in der integrierten Suche sowie einige Informationen zum Ändern der durchsuchten Speicherorte. 
    
    ![Flyout-Seite "Speicherorte ändern"](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. die Umschaltfläche **Wählen Sie unter alles** in Postfach auswählen oben auf der Seite Flyout aus, wodurch angegeben wird, dass alle Postfächer durchsucht werden. Klicken Sie zum Einschränken des Suchbereichs auf die Umschaltfläche, um die Auswahl zu deaktivieren, und klicken Sie dann auf **Benutzer, Gruppen oder Teams auswählen** , und wählen Sie bestimmte Postfächer für die Suche aus.
    
    b. die Umschaltfläche **Wählen Sie unter Alle auswählen** im Abschnitt Websites in der Mitte der Seite Flyout aus, wodurch angegeben wird, dass alle Websites durchsucht werden. Wenn Sie die Suche auf ausgewählte Websites einschränken möchten, heben Sie die Auswahl der Umschaltfläche auf, und klicken Sie dann auf **Websites auswählen**. Sie müssen jede bestimmte Website hinzufügen, die Sie durchsuchen möchten, einschließlich des OneDrive-Kontos des betroffenen.
    
    c. die Umschaltfläche im Abschnitt Öffentliche Exchange-Ordner wird ausgewählt, was bedeutet, dass alle öffentlichen Exchange-Ordner durchsucht werden. Beachten Sie, dass Sie nur alle öffentlichen Exchange-Ordner oder keine dieser Dateien durchsuchen können. Sie können keine bestimmten suchen.
    
3. Wenn Sie die inhaltsspeicherorte in der integrierten Suche ändern, klicken Sie **auf &amp; ausführen** , um die Suche erneut zu starten. 
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Weitere Informationen zur Verwendung des DSR Case-Tools

In den folgenden Abschnitten finden Sie weitere Informationen zur Verwendung des DSR-Fall Tools zur Reaktion auf Anforderungen an die DSR-Exportanforderung.
  
[Exportieren von Daten aus myAnalytics und dem Office-Roamingdienst](#exporting-data-from-myanalytics-and-the-office-roaming-service)

[Exportieren teilweise indizierter Elemente](#exporting-partially-indexed-items)

[Suchen und Exportieren von Daten aus Microsoft Teams und Office 365-Gruppen](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[DurchSuchen von öffentlichen Exchange-Ordnern](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-myanalytics-and-the-office-roaming-service"></a>Exportieren von Daten aus myAnalytics und dem Office-Roamingdienst

Sie können das DSR Case Tool verwenden, um Verwendungsdaten zu suchen und zu exportieren, die von myAnalytics und dem Office-Roamingdienst generiert werden. Hier finden Sie eine Beschreibung, was diese Dienste tun:
  
- **MyAnalytics** – bietet Benutzern Einblicke darüber, wie Sie Ihre Zeit basierend auf den e-Mails und Kalenderdaten in Ihrem Postfach verbringen. Alle myAnalytics-Einblicke werden von e-Mail-und Besprechungs Kopfzeilen im Postfach des Benutzers abgeleitet. Benutzer, denen eine myAnalytics-Lizenz zugewiesen ist, können sich bei Office 365 anmelden und zum myAnalytics-Dashboard wechseln, um die Einblicke in Ihre Zeit zu sehen. (Benutzer können diese Einblicke als Reaktion auf eine DSR-Zugriffsanforderung abbilden). Die integrierte Suche in einem DSR-Fall exportiert die Daten, die zum Generieren von myAnalytics-Einblicken verwendet werden. 
    
- Bei **Office** -Roamingdienst-Roaming handelt es sich um einen Dienst, der Office-bezogene Einstellungen wie Office-Design, Benutzerwörterbuch, Spracheinstellungen, Entwicklermodus und automatische Korrektur speichert. 
    
Die Daten aus myAnalytics und dem Office-Roamingdienst werden im Postfach einer Daten Antragstellerin in ausgeblendeten Ordnern gespeichert, die sich in einer nicht-zwischenmenschlichen Nachricht (nicht-IPM) von Exchange Online-Postfächern befinden. Das bedeutet, dass die Daten aus der Benutzeransicht ausgeblendet werden, wenn Sie Outlook oder andere e-Mail-Clients verwenden, um auf Ihr Postfach zuzugreifen. Weitere Informationen zu ausgeblendeten Ordnern finden Sie unter [MAPI hiddEn Folders](https://go.microsoft.com/fwlink/?linkid=872758).
  
Sie können eine separate Inhaltssuche erstellen (und Sie einem DSR-Fall zuordnen), die die Nutzungsdaten myAnalytics und des Office-Roaming-Diensts im Postfach der betroffenen Personen zurückgibt. Diese Daten sind nicht in der Suchstatistik enthalten und stehen nicht für die Vorschau zur Verfügung. Sie können es aber exportieren und dann als Reaktion auf eine DSR-Exportanforderung an die betroffene Person übergeben.
  
Wenn Sie Daten aus myAnalytics und dem Office Server-Roaming-Dienst exportieren, werden die Daten in einem separaten Ordner für jede Anwendung gespeichert, die sich im Ordner **ApplicationDataRoot** befindet, der sich unter einem Ordner befindet, der mit der e-Mail-Adresse des Datensubjekts benannt ist. Diese Daten werden als JSON-Dateien exportiert, bei denen es sich um lesbare Textdateien handelt, die den XML-oder TXT-Dateien ähneln, die an e-Mail-Nachrichten angefügt sind. Derzeit werden diese Ordner mit einem Globally Unique Identifier (GUID) benannt, der myAnalytics und dem Office-Roamingdienst zugewiesen ist, die in der folgenden Tabelle aufgeführt sind. In zukünftigen Versionen des DSR Case-Tools wird die GUID durch den Namen der tatsächlichen Anwendung ersetzt. 
  
|**Anwendung**|**GUID/Ordnername**|
|:-----|:-----|
|MyAnalytics  <br/> |3c896ded-22c5-450F-91f6-3d1ef0848f6e  <br/> |
|Office-Roamingdienst  <br/> |1caee58f-eb14-4a6b-9339-1fe2ddf6692b  <br/> |
   
 **So suchen und exportieren Sie die Daten von myAnalytics und Office-Roamingdienst:**
  
1. Klicken Sie im &amp; Security Compliance Center auf **Datenschutz** \> **Antragsteller-Anforderungen**, und klicken Sie dann neben dem DSR-Fall für die betroffene Person, für die Sie Verwendungsdaten exportieren möchten, auf **Öffnen** . 
    
2. Klicken Sie oben auf der Seite auf die Registerkarte **Suchen** , und klicken ![Sie dann](media/ITPro-EAC-AddIcon.gif) auf Symbol **gesteuerte Suche**hinzufügen.
    
3. Klicken Sie auf der Seite **Ihre Suche benennen** auf **Abbrechen** . 
    
4. Aktivieren Sie unter **Suchabfrage**in der Bedingung **Typ** die Kontrollkästchen neben myAnalytics **** und **Office Roaming Service**. 
    
    ![Aktivieren Sie die Kontrollkästchen myAnalytics und Office-Roamingdienst, um Verwendungsdaten zu exportieren.](media/3dacbc7a-c314-492c-828c-6757fda84963.png)
  
    Beachten Sie, **** dass die typbedingung (e-Mail-Nachrichtenklassen) das einzige Element in der Suchabfrage sein sollte. Sie können das Feld **Schlüsselwörter** löschen oder es leer lassen. 
    
5. Stellen Sie sicher, dass unter **Speicherorte** **bestimmte Speicherorte** ausgewählt ist, und klicken Sie dann auf **ändern**.
    
6. Klicken Sie im oberen Bereich der Seite **Speicherorte ändern** (Postfach) auf **Benutzer, Gruppen oder Teams auswählen**.
    
7. Klicken Sie auf der Seite **Speicherorte bearbeiten** auf **Benutzer, Gruppen oder Teams auswählen**, wählen Sie das Postfach der betroffenen Person aus, und speichern Sie dann Ihre Auswahl. 
    
8. Klicken Sie auf ** &amp; ausführen**, und benennen Sie die Suche, und speichern Sie Sie.
    
    Die Suche wird gestartet.
    
 **So exportieren Sie die Daten von myAnalytics und des Office-Roaming-Diensts:**
  
1. Wenn die im vorherigen Schritt erstellte Suche abgeschlossen ist, klicken Sie oben auf der Seite auf die Registerkarte **Suchen** , und klicken Sie dann auf das Kontrollkästchen neben der Suche. Möglicherweise müssen Sie ![auf](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **** aktualisieren Aktualisieren klicken, um die Suche anzuzeigen. 
    
2. Klicken Sie ![auf der Seite Such Flyout auf Suchergebnis Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mehr**exportieren, und wählen Sie dann **Ergebnisse** aus der Dropdownliste aus. 
    
3. Wählen Sie auf der Seite **Ergebnisse exportieren** die folgenden empfohlenen Optionen aus, um Verwendungsdaten zu exportieren. 
    
    ![Exportoptionen beim Exportieren von myAnalytics-und Office Roaming-Dienst Nutzungsdaten](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. Wählen Sie unter **Ausgabeoptionen**die erste Option aus ( **alle Elemente, ausgenommen solche, die über ein unbekanntes Format verfügen, verschlüsselt oder aus anderen Gründen nicht indiziert**wurden), um nur indizierte Elemente zu exportieren.
    
    b. Wählen Sie unter **Exchange-Inhalt exportieren als**die zweite Option aus, **eine PST-Datei, die alle Nachrichten enthält**.
    
    c. lassen Sie die restlichen Exportoptionen nicht ausgewählt.
    
4. Klicken Sie nach Auswahl der Exporteinstellungen auf **exportieren**.
    
    Die Suchergebnisse werden zum Herunterladen bereitgestellt, sodass Sie in den Azure-Speicherbereich für Ihre Organisation in der Microsoft-Cloud hochgeladen werden. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
5. Klicken Sie auf die Registerkarte **Export** , um den soeben erstellten Exportauftrag anzuzeigen. Beachten Sie, dass Exportaufträge den gleichen Namen wie die entsprechende Suche mit **_Export** haben, die am Ende des Suchnamens angehängt ist. 
    
6. Klicken Sie auf den soeben erstellten Exportauftrag, um die Seite zum Exportieren des Flyouts anzuzeigen. 
    
7. Klicken Sie unter **Schlüssel exportieren**auf **in Zwischenablage kopieren**. Sie verwenden diesen Schlüssel in Schritt 10, um die Suchergebnisse herunterzuladen.
    
8. Klicken ![Sie oben auf der](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) Seite zum Exportieren des Flyouts auf Suchergebnis Symbol- **Download Ergebnisse** exportieren. 
    
9. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen** , um das **Microsoft Office 365 EDiscovery-Export Tool**zu öffnen. Das **eDiscovery-Export Tool** wird beim ersten herunterladen der Suchergebnisse installiert. 
    
10. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 7 kopiert haben, in das entsprechende Feld ein.
    
11. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese-und Schreibvorgänge) sollten Sie die Suchergebnisse auf ein lokales Laufwerk herunterladen. Laden Sie Sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
12. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Export Tool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und der Größe) der verbleibenden zu ladenden Elemente. Nach Abschluss des Exportvorgangs können Sie die Exchange-PST-Datei in Outlook öffnen und dann zum Ordner **ApplicationDataRoot** wechseln, um auf die Unterordner von myAnalytics und Roamingdienst zuzugreifen. 
    
    Wie bereits erläutert, werden die JSON-Dateien, die Verwendungsdaten enthalten, an Nachrichten angefügt. Klicken Sie zum Anzeigen einer JSON-Datei auf eine Nachricht, und öffnen Sie dann die angefügte JSON-Datei. 
  
### <a name="exporting-partially-indexed-items"></a>Exportieren teilweise indizierter Elemente

Es wird empfohlen, dass Sie nicht teilweise indizierte Elemente (auch als nicht indizierte Elemente bezeichnet) aus der integrierten Suche exportieren, die erstellt wird, wenn Sie einen neuen DSR-Fall erstellen. Das liegt daran, dass die Suchergebnisse mehr als wahrscheinlich teilweise indizierte Elemente für andere Benutzer in Ihrer Organisation und nicht nur teilweise indizierte Elemente für die betroffene Person enthalten. Stattdessen wird empfohlen, eine separate Inhaltssuche zu erstellen, die dem DSR-Fall zugeordnet ist, der nur die teilweise indizierten Elemente im Zusammenhang mit der betroffenen Person exportieren soll. 
  
Hier ist ein allgemeiner Prozess zum Exportieren teilweise indizierter Elemente. Nachdem Sie exportiert wurden, können Sie Sie überprüfen, um zu ermitteln, ob ein Element auf eine DSR-Access-oder Exportanforderung reagiert.
  
1. Öffnen Sie den DSR-Fall, und erstellen Sie eine neue Suche auf der Seite **Suchen** . 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren der Suchabfrage und der inhaltsspeicherorte für die Suche:
    
    - Verwenden Sie eine leere/leere Stichwortabfrage. Dadurch werden alle Elemente in den Inhaltsspeicherorten zurückgegeben, die durchsucht werden.
    
    - Durchsuchen Sie nur das Exchange Online-Postfach der betroffenen Person und Ihr OneDrive-Konto.
    
3. Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse exportieren und herunterladen (wie in [Schritt 4](#step-4-export-the-data)beschrieben). Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
    
    - Wählen Sie unter **Ausgabeoptionen**die dritte Option aus ( **nur Elemente, die ein unbekanntes Format aufweisen, verschlüsselt oder aus anderen Gründen nicht indiziert wurden**), um nur teilweise indizierte Elemente zu exportieren.
    
    - Unter **Exchange-Inhalt exportieren als**können Sie eine beliebige Option basierend auf Ihren Einstellungen auswählen. 
    
    - Wenn Sie die Option **Versionen für SharePoint-Dokumente einbeziehen** aktivieren, werden Versionen von Dokumenten exportiert, wenn eine Version teilweise indiziert ist. 
    
Weitere Informationen zu teilweise indizierten Elementen finden Sie unter: 
  
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md)

- [Exportieren teilweise indizierter Elemente](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a>Suchen und Exportieren von Daten aus Microsoft Teams und Office 365-Gruppen

UnterHaltungen, die Teil der Chat-Liste in Microsoft Teams (als teamchats oder 1:1-Chats bezeichnet) sind, werden im Exchange Online-Postfach der Benutzer gespeichert, die an den Chats teilnehmen. Außerdem werden die Dateien, die eine Person in einem eins-zu-eins-Chat teilt, im OneDrive-Konto der Person gespeichert, die die Datei freigibt. Da durch die integrierte Suche alle Postfächer und OneDrive-Konten in der Organisation durchsucht werden, werden Team-Chats und Dokumente, die in einer Chatsitzung freigegeben sind (die die betroffene Person erstellt oder hochgeladen hat) von der integrierten Suche in einem DSR-Fall zurückgegeben.
  
Alternativ werden Unterhaltungen, die Teil eines Teams-Kanals sind (auch als Kanal Nachrichten bezeichnet) in dem Postfach gespeichert, das einem Team zugeordnet ist. Diese Arten von Unterhaltungen, an denen die betroffene Person teilgenommen hat, werden auch von der integrierten Suche zurückgegeben, da alle Microsoft Teams zugeordneten Postfächer durchsucht werden. Darüber hinaus werden Kacheln, die eine betroffene Person in einem Teams-Kanal freigegeben haben, auf der SharePoint-Website des Teams gespeichert. Dateien, die erstellt oder uploadedby werden, werden von der integrierten Suche in einem DSR-Fall zurückgegeben, da Websites, die Microsoft Teams zugeordnet sind, in die Suche einbezogen werden.
  
Entsprechend sind auch Postfächer und SharePoint-Websites, die einer Office 365-Gruppe entsprechen, in der integrierten Suche enthalten. Dies führt dazu, dass e-Mail-Nachrichten, die von der betroffenen Person gesendet oder empfangen werden, und Dateien zurückgegeben werden. 
  
Weitere Informationen zur Verwendung der Inhaltssuche zum Suchen nach Elementen in Microsoft Teams und Office 365-Gruppen oder zum Abrufen einer Liste von Mitgliedern finden Sie im Abschnitt "Durchsuchen von Microsoft Teams und Office 365-Gruppen" unter [Inhaltssuche in Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>DurchSuchen von öffentlichen Exchange-Ordnern

Bei der integrierten Suche in einem DSR-Fall werden nur e-Mail-Nachrichten zurückgegeben, die von der betroffenen Person an einen e-Mail-aktivierten Öffentlichen Ordner gesendet wurden, oder Nachrichten, die von einem anderen Benutzer an einen öffentlichen Ordner gesendet und auch die betroffene Person kopiert wurden. Es wird keine Nachricht zurückgegeben, die der betroffene betroffene möglicherweise an einen öffentlichen Ordner gesendet hat. Um nach Elementen zu suchen, die von der betroffenen Person in einem öffentlichen Ordner bereitgestellt wurden, können Sie eine separate Erstellung einer separaten Inhaltssuche erstellen, die nach jedem Element sucht, das von der betroffenen Person an einen öffentlichen Ordner gesendet wurde.
  
Hier finden Sie eine allgemeine Vorgehensweise zum Suchen nach Elementen, die der betroffene in einem öffentlichen Ordner bereitgestellt hat. 
  
1. Öffnen Sie den DSR-Fall, und erstellen Sie eine neue Suche auf der Seite **Suchen** . 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren der Suchabfrage und der inhaltsspeicherorte für die Suche:
    
  - Verwenden Sie im Feld **Schlüsselwörter** die folgende Suchabfrage: 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Durchsuchen aller öffentlichen Exchange-Ordner
    
  - Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse exportieren und herunterladen (wie in [Schritt 4](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)beschrieben). Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 

---
title: Ausführen einer Inhaltssuche im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: 'Verwenden Sie die Inhaltssuche im Security & Compliance Center, um Postfächer, SharePoint Online-Websites und OneDrive für Geschäftsstandorte zu durchsuchen. '
ms.openlocfilehash: 4c3d9cc024a495ff8464e1117d5f46c13c1b9a08
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261738"
---
# <a name="run-a-content-search-in-the-security--compliance-center"></a>Ausführen einer Inhaltssuche im Security & Compliance Center

Sie können das eDiscovery-Tool für die Inhaltssuche im Security & Compliance Center verwenden, um nach Elementen wie e-Mails, Dokumenten und Chatnachrichten in Ihrer Office 365-Organisation zu suchen. Verwenden Sie dieses Tool, um nach Elementen in diesen Office 365-Diensten zu suchen:
  
- Exchange Online-Postfächer und öffentliche Ordner
    
- SharePoint Online-und OneDrive for Business-Websites
    
- Skype for Business-Unterhaltungen
    
- Microsoft Teams 
    
- Office 365-Gruppen
    
Die Inhaltssuche ist ein neues eDiscovery-Such Tool mit neuen und verbesserten Skalierungs-und Leistungsfunktionen. Verwenden Sie die Inhaltssuche, um sehr große eDiscovery-Suchen durchzuführen. Sie können in einer einzelnen Inhaltssuche alle Postfächer, alle öffentlichen Exchange-Ordner und alle SharePoint Online-Websites und OneDrive für Business-Konten durchsuchen. Die Anzahl der inhaltsspeicherorte, die Sie durchsuchen können, ist unbegrenzt. Außerdem gibt es keine Begrenzung für die Anzahl der Suchvorgänge, die gleichzeitig ausgeführt werden können. Nachdem Sie eine Inhaltssuche ausgeführt haben, wird die Anzahl der inhaltsspeicherorte und eine geschätzte Anzahl von Suchergebnissen im Detailbereich auf der Seite **Inhaltssuche** angezeigt. Nachdem Sie eine Suche ausgeführt haben, können Sie eine Vorschau der Ergebnisse anzeigen, Schlüsselwort Statistiken für eine oder mehrere Suchvorgänge abrufen, Inhaltssuche massenweise bearbeiten und die Ergebnisse auf einen lokalen Computer exportieren. 
  
 **Inhalt**
  
[Create a search](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[Exportieren der Suchergebnisse](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[Preview search results](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[Update search results](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[Edit a search](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[Retry a search](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Informationen und Anleitungen zum Erstellen von Suchabfragen und Verwenden von booleschen Suchoperatoren finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md). Dieser Artikel enthält auch Informationen zum Suchen nach vertraulichen Informationstypen und zum Suchen nach Inhalten, die für Personen innerhalb und außerhalb Ihrer Organisation freigegeben sind.
    
- Damit Sie Zugriff auf die Seite " **Inhaltssuche** " haben, um Suchergebnisse und eine Vorschau zu durchsuchen und zu exportieren, muss ein Administrator, Compliance Officer oder eDiscovery-Manager Mitglied der rollenGruppe "eDiscovery Manager" im Security _AMP_ Compliance Center sein. Sie müssen in Exchange Online, SharePoint Online oder für OneDrive für Unternehmen-Websites keine zusätzlichen Suchberechtigungen zuweisen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 Security _AMP_ Compliance Center](assign-ediscovery-permissions.md).
    
- Für die Inhaltssuche gelten Grenzwerte, um die Integrität und Qualität der Dienste für Office 365-Organisationen zu gewährleisten. In den meisten Fällen können diese Grenzwerte nicht geändert werden, Sie sollten die Werte jedoch beachten, damit Sie die Grenzen bei der Planung, beim Ausführen und bei der Problembehandlung von Suchvorgängen berücksichtigen können. Weitere Informationen finden Sie unter [Grenzwerte für die Suche im Security _AMP_ Compliance Center](limits-for-content-search.md).
    
- Weitere Informationen finden Sie im Abschnitt Geschätzte Suchzeiten basierend auf der Anzahl der Postfächer, die in einer einzelnen Inhaltssuche durchsucht werden. 
    
- Wie bereits erwähnt, können Sie die Inhaltssuche verwenden, um in Office 365-Gruppen und Microsoft Teams nach Inhalten zu suchen. Dies führt dazu, dass Sie das Gruppenpostfach, den freigegebenen Kalender und die SharePoint-Websites durchsuchen können, die einer Office 365-Gruppe und einem Microsoft-Team zugeordnet sind. Darüber hinaus können Sie die Kanal Unterhaltungen in einem Microsoft-Team durchsuchen. Weitere Informationen zu Office 365-Gruppen und Microsoft Teams finden Sie unter:
    
  - [Informationen zu Office 365-Gruppen](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [Microsoft Teams-Hilfe](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Im Abschnitt finden Sie Tipps zur Suche nach Inhalten in Office 365-Gruppen und Microsoft Teams. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>Create a search
<a name="create"> </a>

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security & Compliance Centers auf **Suche** \> **Inhaltssuche**.
    
4. Klicken Sie auf **Neu**![Hinzufügen (Symbol)](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
5. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. Dieser Name muss in der Organisation eindeutig sein. 
    
6. Wählen Sie die inhaltsspeicherorte aus, die Sie durchsuchen möchten. Sie können Postfächer, Websites und öffentliche Ordner in derselben Suche durchsuchen.
    
    ![Auswählen der inhaltsspeicherorte, die Sie durchsuchen möchten](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **Überall suchen** Wählen Sie diese Option aus, um alle inhaltsspeicherorte in Ihrer Organisation zu durchsuchen. Wenn Sie diese Option auswählen, können Sie alle Postfächer durchsuchen (einschließlich inaktiven Postfächern und Postfächern für alle Office 365-Gruppen und Microsoft Teams), alle SharePoint-und OneDrive for Business-Websites (dazu gehören die Websites für alle Office 365-Gruppen und Microsoft Teams) und alle öffentlichen Ordner.
    
    ![Klicken Sie auf die Option Such Everywhere, um alle inhaltsspeicherorte zu durchsuchen.](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **Auswahl für benutzerdefinierte Standorte** Wählen Sie diese Option aus, um die Postfächer und Websites auszuwählen, die Sie durchsuchen möchten. Wenn Sie diese Option auswählen, haben Sie die Flexibilität, alle inhaltsspeicherorte für einen bestimmten Dienst (beispielsweisedurch Suchen aller Exchange-Postfächer) zu durchsuchen, oder Sie können bestimmte inhaltsspeicherorte für einen Office 365-Dienst durchsuchen.
    
    Beachten Sie beim Hinzufügen von Inhaltsspeicherorten für die Suche Folgendes:
    
    **Postfächer**
    
  - Wenn Sie auf ****![hinzufügen klicken](media/ITPro-EAC-AddIcon.gif) , um die zu durchsuchenden Postfächer anzugeben, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie dieser Liste Empfänger hinzufügen möchten, geben Sie in das Suchfeld einen Namen (mindestens 3 Zeichen) ein, ****![und klicken Sie](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)auf Suchsymbol suchen.
    
  - Sie können inaktive Postfächer und Verteilergruppen zur Liste der zu durchsuchenden Postfächer hinzufügen. Für Verteilergruppen werden die Postfächer der Gruppenmitglieder durchsucht. Beachten Sie, dass dynamische Verteilergruppen nicht unterstützt werden.
    
  - Führen Sie den Befehl `Get-Mailbox -InactiveMailboxOnly` in Exchange Online PowerShell aus, um eine Liste der inaktiven Postfächer in Ihrer Organisation zu erhalten. Alternativ können Sie im Security & Compliance Center zu **Data Governance** \> **Retention** wechseln und dann auf **Weitere**![Navigationsleisten Ellipsen](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **inaktive Postfächer**klicken.
    
  - Sie können auch das Postfach hinzufügen, das einer Office 365-Gruppe oder einem Microsoft-Team zugeordnet ist. In diesem Fall wird nur das Postfach der Gruppe oder des Teams durchsucht; die Postfächer der Gruppe oder Teammitglieder wurden nicht durchsucht. Um Sie durchsuchen zu können, müssen Sie Sie der Suche ausdrücklich hinzufügen.
    
  - Wenn Sie keine Postfächer in die Suche aufnehmen möchten, wählen Sie **bestimmte Postfächer für die Suche**auswählen, fügen Sie der Liste jedoch kein Postfach hinzu.
    
    **Websites**
    
  - Klicken Sie auf hinzu](media/ITPro-EAC-AddIcon.gif) fügen, um der Suche Websites hinzuzufügen. ****![ Geben Sie die URL für jede Website ein, die Sie durchsuchen möchten. Das Inhaltssuche-Tool überprüft die URL und fügt Sie der Liste der zu durchsuchenden Websites hinzu. 
    
  - Sie können die SharePoint hinzufügen, die einer Office 365-Gruppe oder einem Microsoft-Team zugeordnet ist. Im Abschnitt finden Sie Anleitungen zur Suche nach der URL für die Gruppe oder das Team. 
    
  - Wenn Sie keine Websites in eine Suche einbeziehen möchten, wählen Sie **bestimmte Websites für die Suche**auswählen, aber fügen Sie der Liste keine Website hinzu.
    
    **Öffentliche Ordner**
    
    Bei öffentlichen Ordnern können Sie alle öffentlichen Ordner in Ihrer Exchange Online-Organisation durchsuchen oder keine öffentlichen Ordner durchsuchen.
    
7. Klicken Sie dann auf **Weiter**.
    
8. Auf der Seite **Neue Suche** können Sie Schlüsselwörter und Bedingungen zum Erstellen der Suchabfrage hinzufügen. 
    
    ![Erstellen einer Suchabfrage mit Schlüsselwörtern und Bedingungen](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. Geben Sie im Feld unter **Wonach sollen wir für Sie suchen?** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**, **near**oder **ONEAR**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen. 
    
2. Sie können auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch den **or** -Operator in der erstellten Suchabfrage verbunden. 
    
    ![Sie können ein Stichwort oder eine Stichwort Phase in eine Zeile in der Stichwörter Liste eingeben.](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [View Keyword Statistics for Content Search results](view-keyword-statistics-for-content-search.md).
    
    Informationen zur Verwendung der Stichwortliste finden Sie im Abschnitt. 
    
3. Klicken Sie auf **Abfrage für Tippfehler über** prüfen, um die Abfrage auf nicht unterstützte Zeichen und boolesche Operatoren zu überprüfen, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden oft ausgeblendet und verursachen in der Regel einen Suchfehler oder geben unbeabsichtigte Ergebnisse zurück. Weitere Informationen zu den nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Überprüfen der Inhalts Suchabfrage auf Fehler](check-your-content-search-query-for-errors.md).
    
4. Fügen Sie unter **Bedingungen**einer Suchabfrage Bedingungen hinzu, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt eine Klausel zu der KQL-Suchabfrage hinzu, die beim Starten der Suche erstellt und ausgeführt wird. Eine Bedingung ist durch **AND**-Operator logisch mit der (im Schlüsselwortfeld angegebenen) Schlüsselwortabfrage verbunden. Dies bedeutet, dass Elemente sowohl die Schlüsselwortabfrage als auch die Bedingung erfüllen muss, damit sie in die Suchergebnisse aufgenommen werden. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. 
    
||
|:-----|
|Weitere Informationen zum Erstellen einer Suchabfrage und zum Verwenden von Bedingungen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche ](keyword-queries-and-search-conditions.md). |
   
9. Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten. 
    
    Die Suche wird gestartet. Wenn die Suche abgeschlossen ist, werden im Detailbereich die folgenden Informationen angezeigt.
    
    ![Suchstatistiken werden im Detailbereich der ausgewählten Inhaltssuche angezeigt](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. Datum und Uhrzeit der letzten Ausführung der Suche.
    
2. Die Anzahl (und Gesamtgröße) der gefundenen Elemente, die mit der Suchabfrage übereinstimmen. Beispiele für Elementtypen sind e-Mail-Nachrichten, Kalenderelemente und Dokumente. Wenn ein Element mehrere Instanzen eines Schlüsselwortes enthält, nach dem gesucht wird, wird es nur einmal in der Gesamtanzahl der Elemente gezählt. Wenn Sie beispielsweise nach Wörtern "Stock" oder "Tip" suchen und eine e-Mail-Nachricht drei Instanzen des Wortes "Stock" enthält, wird Sie nur einmal in das Feld **Items** gezählt. 
    
3. Die Anzahl und Gesamtgröße von nicht indizierten Elementen in den Inhaltsspeicherorten, die durchsucht wurden. Die Anzahl nicht indizierter Elemente, die den Suchkriterien nicht entsprechen, werden in die Suchstatistiken einbezogen, die im Detailbereich angezeigt werden. Wenn ein nicht indiziertes Element mit der Suchabfrage übereinstimmt (da andere Nachrichten-oder Dokumenteigenschaften den Suchkriterien entsprechen), wird es nicht in der geschätzten Anzahl von nicht indizierten Elementen eingeschlossen. Wenn jedoch ein nicht indiziertes Element von den Suchkriterien ausgeschlossen wird, wird es nicht in die Schätzung der nicht indizierten Elemente eingeschlossen.
    
4. Die Anzahl der einzelnen Inhaltsspeicher Typen, die durchsucht wurden. Beachten Sie bei Postfächern, dass Archivpostfächer in der Gesamtanzahl der durchsuchten Postfächer enthalten sind. Im vorherigen Beispiel wurden vier Benutzerpostfächer durchsucht, und das Archivpostfach für jeden dieser Benutzer ist aktiviert. Daher werden in der Suchstatistik acht Postfächer zitiert.
    
5. Links zum Anzeigen einer Vorschau der Suchergebnisse oder zum erneuten Ausführen der Suche, um die Suchstatistiken zu aktualisieren.
    
    Klicken Sie bei Bedarf ****![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren, um die Informationen im Detailbereich für die ausgewählte Suche zu aktualisieren. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>Exportieren der Suchergebnisse
<a name="export"> </a>

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie E-Mail-Ergebnisse exportieren, werden diese als PST-Dateien auf Ihren Computer heruntergeladen. Wenn Sie Inhalte aus SharePoint und OneDrive for Business-Websites exportieren, werden Kopien von systemeigenen Office-Dokumenten exportiert. Es gibt auch zusätzliche Dokumente und Berichte, die in den exportierten Suchergebnissen enthalten sind. Weitere Informationen finden Sie unter [Exportieren von Suchergebnissen aus dem Security _AMP_ Compliance Center](export-search-results.md).
  
## <a name="preview-search-results"></a>Suchergebnisse in der Vorschau anzeigen
<a name="preview"> </a>

Nachdem die Suche erfolgreich abgeschlossen wurde, können Sie eine Vorschau der Suchergebnisse anzeigen. Im Zusammenhang mit dem Anzeigen von Inhaltssuchergebnissen in der Vorschau gibt es einige Einschränkungen. Weitere Informationen finden Sie unter [Grenzwerte für die Suche im Security _AMP_ Compliance Center](limits-for-content-search.md). Beachten Sie, dass nicht indizierte Elemente für die Vorschau nicht verfügbar sind.
  
1. Wählen Sie auf der Seite **Inhaltssuche** eine Suche aus. 
    
2. Klicken Sie im Detailbereich unter **Ergebnisse** auf **Vorschau der Suchergebnisse anzeigen**. Die Seite **Vorschau der Suchergebnisse anzeigen** wird geöffnet und enthält eine Liste der Suchergebnisse. 
    
    Sie können auf eine Spaltenüberschrift klicken, um die Ergebnisse basierend auf Betreff, Typ, Absender oder dem Datum zu sortieren, an dem ein Element im Quellpostfach empfangen wurde.
    
3. Klicken Sie auf ein Element, das angezeigt werden soll.
    
    Das Element wird im Vorschaufenster geöffnet.
    
4. Wenn ein Dateityp für die Vorschau nicht unterstützt wird oder eine Kopie eines Dokuments heruntergeladen wird, können Sie auf **Originaldatei herunter** laden klicken, um Sie auf Ihren lokalen Computer herunterzuladen. Für aspx-Webseiten ist die URL für die Seite enthalten, obwohl Sie möglicherweise nicht über die Berechtigungen für den Zugriff auf die Seite verfügen. 
    
> [!NOTE]
> Wenn Sie die Suchergebnisse einer Suche, die vor mehr als sieben Tagen ausgeführt wurde, in der Vorschau anzeigen, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. Die Suche wird erneut ausgeführt, um die aktuellen Ergebnisse abzurufen, die der Suchabfrage entsprechen. 
  
### <a name="file-types-that-can-be-previewed"></a>Dateitypen, die in der Vorschau angezeigt werden können

Im Vorschaubereich können Sie eine Vorschau der unterstützten Dateitypen anzeigen. Wenn ein Dateityp nicht unterstützt wird, müssen Sie eine Kopie der Datei auf den lokalen Computer herunterladen, um Sie anzuzeigen. Die folgenden Dateitypen werden unterstützt und können auf der Seite Vorschau der **Suchergebnisse** angezeigt werden. 
  
- . txt,. html,. MHTML
    
- . eml
    
- . doc,. docx,. docm
    
- . pptm, PPTX
    
- PDF
    
Darüber hinaus werden die folgenden Dateicontainer Typen unterstützt. Sie können die Liste der Dateien im Container im Vorschaubereich anzeigen.
  
- . zip
    
- . gzip
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>Aktualisieren von Suchergebnissen
<a name="restart"> </a>

Wenn Sie die Ergebnisse einer vorhandenen Inhaltssuche aktualisieren, wird die Suchabfrage an allen angegebenen Inhaltsspeicherorten erneut ausgeführt. Der offensichtliche Grund zum Aktualisieren der Suchergebnisse besteht darin, die neuesten Daten abzurufen.
  
1. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, für die Sie die Ergebnisse aktualisieren möchten. 
    
2. Klicken Sie im Detailbereich unter **Ergebnisse** auf **Suchergebnisse aktualisieren**.
    
    Es wird eine Statusmeldung angezeigt, dass die Ergebnisse abgerufen werden. Wenn die Suche abgeschlossen ist, werden die aktualisierten Informationen unter **Ergebnisse** im Detailbereich angezeigt. Beachten Sie, dass das Datum im Feld **Durchsucht am** im Detailbereich auf das aktuelle Datum und die Uhrzeit aktualisiert wird. Klicken Sie ****![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif)aktualisieren, um die Informationen in der Liste der Inhalts Suchvorgänge zu aktualisieren.
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>Bearbeiten einer Suche
<a name="edit"> </a>

Sie können die Quellpostfächer und die Suchabfrage für eine vorhandene Inhaltssuche ändern.
  
1. Wählen Sie auf der Seite **Inhaltssuche** eine Suche aus. 
    
2. Klicken Sie im Detailbereich unter **Abfrage** auf **Suche bearbeiten**.
    
3. Auf der Seite **Speicherorte** können Sie die Suche nach Postfächern, Gruppen, SharePoint-Websites oder OneDrive für Business-Websites ändern. Sie können auch wählen (oder deaktivieren), um alle öffentlichen Ordner in Exchange zu durchsuchen. 
    
4. Auf der Seite **Abfrage** können Sie die Suchabfrage bearbeiten. 
    
5. Klicken Sie auf der Seite **Quellen** oder **Speicherorte** auf **Suchen** , um die überarbeitete Suche zu starten. 
    
    Die überarbeitete Suche wird gestartet. Wenn die Suche abgeschlossen ist, werden die geschätzten Ergebnisse für die überarbeitete Suche im Detailbereich angezeigt.
    
## <a name="retry-a-search"></a>Erneutes Ausführen einer Suche
<a name="retry"> </a>

Wenn bei einer Suche Fehler zurückgegeben werden, müssen Sie nicht alle inhaltsspeicherorte erneut durchsuchen. Sie können die Suche erneut ausführen, sodass nur die fehlerhaften inhaltsspeicherorte der Suche erneut durchsucht werden. Wenn Sie alle inhaltsspeicherorte erneut durchsuchen möchten, können Sie die Suchergebnisse aktualisieren.
  
1. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, die die inhaltsspeicherorte enthält, die Sie erneut durchsuchen möchten. 
    
2. Klicken Sie im Detailbereich unter **Fehler** auf **Suche wiederholen**.
    
    Es wird eine Statusmeldung angezeigt, dass die Ergebnisse abgerufen werden. Wenn die Suche abgeschlossen ist, werden im Detailbereich unter **Ergebnisse** die aktualisierten Informationen angezeigt. Beachten Sie, dass das Datum im Feld **Durchsucht am** im Detailbereich auf das aktuelle Datum und die Uhrzeit aktualisiert wird. Um die Informationen in der Liste der Suchvorgänge zu aktualisieren ****![, klicken Sie](media/O365-MDM-Policy-RefreshIcon.gif)auf Aktualisierungssymbol aktualisieren.
    
[Nach oben](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

Hier finden Sie weitere Informationen zur Inhaltssuche.
  
[Grenzen und Leistung](#limits-and-performance)
  
[Nicht indizierte Elemente](#unindexed-items) 
 
[Microsoft Teams und Office 365-Gruppen](#microsoft-teams-and-office-365-groups)
  

  [OneDrive for Business](#onedrive-for-business)
  
[Suchabfragen](#search-queries)
  
[DurchSuchen inaktiver Postfächer](#searching-inactive-mailboxes)
  
[Sonstiges](#miscellaneous)
  
[Return to top](#before-you-begin)
  
### <a name="limits-and-performance"></a>Grenzen und Leistung
  
- Eine Beschreibung der Grenzwerte für die Inhaltssuche finden Sie unter [Grenzwerte für die Suche im Security _AMP_ Compliance Center](limits-for-content-search.md).
    
- Microsoft sammelt Leistungsinformationen für Inhaltssuche, die von allen Office 365-Organisationen ausgeführt werden. Während sich die Komplexität der Suchabfrage auf die Suchzeiten auswirken kann, ist der größte Faktor für die Dauer der Suche die Anzahl der durchsuchten Postfächer. Obwohl Microsoft keine Vereinbarung zum Service Level für Suchzeiten bereitstellt, werden in der folgenden Tabelle die durchschnittlichen Suchzeiten für eine Inhaltssuche basierend auf der Anzahl der Postfächer aufgeführt, die in der Suche enthalten sind.
    
|**Anzahl der Postfächer**|**Durchschnittliche Suchzeit**|
|:-----|:-----|
|100  <br/> |30 Sekunden  <br/> |
|1,000  <br/> |45 Sekunden  <br/> |
|10,000  <br/> |4 Minuten  <br/> |
|25.000  <br/> |10 Minuten  <br/> |
|50.000  <br/> |20 Minuten  <br/> |
|100,000  <br/> |25 Minuten  <br/> |
   
  
### <a name="unindexed-items"></a>Nicht indizierte Elemente
  
- Wie bereits erläutert, sind nicht indizierte Elemente an Inhaltsspeicherorten, die durchsucht werden, in den geschätzten Suchergebnissen enthalten. Wenn ein nicht indiziertes Element mit der Suchabfrage übereinstimmt (da andere Nachrichten-oder Dokumenteigenschaften den Suchkriterien entsprechen), wird es nicht in der geschätzten Anzahl von nicht indizierten Elementen eingeschlossen. Wenn ein nicht indiziertes Element durch die Suchkriterien ausgeschlossen wird, wird es auch nicht in der geschätzten Anzahl von nicht indizierten Elementen eingeschlossen. Weitere Informationen finden Sie unter [unindizierte Elemente in der Inhaltssuche](https://go.microsoft.com/fwlink/p/?LinkId=780739).
    

  
### <a name="microsoft-teams-and-office-365-groups"></a>Microsoft Teams und Office 365-Gruppen
  
- Microsoft Teams basieren auf Office 365-Gruppen. Daher ist die Suche nach diesen sehr ähnlich. Beachten Sie bei der Suche nach Inhalten in Microsoft Teams-und Office 365-Gruppen die folgenden Aspekte.
    
  - Zum Suchen nach Inhalten in Microsoft Teams-und Office 365-Gruppen müssen Sie das Postfach und die SharePoint-Website angeben, die einem Team oder einer Gruppe zugeordnet sind.
    
  - Führen Sie das Cmdlet **Get-Unifiedgroup** in Exchange Online aus, um die Eigenschaften für ein Microsoft-Team oder eine Office 365-Gruppe anzuzeigen. Dies ist eine gute Möglichkeit, die URL für die Website abzurufen, die einem Team oder einer Gruppe zugeordnet ist. Mit dem folgenden Befehl werden beispielsweise ausgewählte Eigenschaften für eine Office 365-Gruppe mit dem Namen "Senior Leadership Team" angezeigt: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-Unifiedgroup** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
  - Wenn das Postfach eines Benutzers durchsucht wird, wird jede Microsoft-Team-oder Office 365-Gruppe, der der Benutzer angehört, nicht durchsucht. Auf ähnliche Weise wird beim Durchsuchen eines Microsoft-Teams oder einer Office 365-Gruppe nur das Gruppenpostfach und die von Ihnen angegebene Gruppen Website durchsucht; die Postfächer und OneDrive für Geschäftskonten von Gruppenmitgliedern werden nicht durchsucht, es sei denn, Sie fügen Sie der Suche explizit hinzu.
    
  - Wenn Sie eine Liste der Mitglieder eines Microsoft-Teams oder einer Office 365-Gruppe abrufen möchten, können Sie die Eigenschaften auf der Seite **Start \> gruppen** im Microsoft 365 Admin Center anzeigen. Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-UnifiedGroupLinks** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
  - Unterhaltungen, die Teil eines Microsoft Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Microsoft-Team zugeordnet ist. Entsprechend werden Dateien, die Teammitglieder in einem Kanal freigeben, auf der SharePoint-Website des Teams gespeichert. Daher müssen Sie das Microsoft Team-Postfach und die SharePoint-Website als Inhaltsspeicherort hinzufügen, um Unterhaltungen und Dateien in einem Kanal zu durchsuchen.
    
  - 
    
    Alternativ werden Unterhaltungen, die Teil der Chat Liste in Microsoft Teams sind, im Exchange Online-Postfach der Benutzer gespeichert, die am Chat teilnehmen. Und Dateien, die ein Benutzer in Chat Unterhaltungen freigibt, werden im OneDrive for Business-Konto des Benutzers gespeichert, der die Datei freigibt. Daher müssen Sie die einzelnen Benutzerpostfächer und OneDrive für Geschäftskonten als inhaltsspeicherorte hinzufügen, um Unterhaltungen und Dateien in der Chat Liste zu durchsuchen.
    
    > [!NOTE]
    > Benutzer, die an Unterhaltungen teilnehmen, die in der Chat Liste in Microsoft Teams enthalten sind, müssen über ein Exchange Online-Postfach (Cloud-basiert) verfügen, um Chat Unterhaltungen durchsuchen zu können. Das liegt daran, dass Konversationen, die Teil der Chat Liste sind, in den cloudbasierten Postfächern der Chat Teilnehmer gespeichert werden. Wenn ein Chat Teilnehmer kein Exchange Online-Postfach hat, können Sie keine Chat Unterhaltungen durchsuchen. Beispielsweise können Benutzer mit einem lokalen Postfach in einer Exchange-hybridbereitstellung an Unterhaltungen teilnehmen, die in der Chat Liste in Microsoft Teams enthalten sind. In diesem Fall sind jedoch Inhalte dieser Unterhaltung nicht durchsuchbar, da die Benutzer keine Cloud-basierten Postfächer besitzen. 
  
  - Jeder Microsoft-Team-oder Team Kanal enthält ein wiki für Notizen und Zusammenarbeit. Der wiki-Inhalt wird automatisch in einer Datei mit dem MHT-Format gespeichert. Diese Datei wird in der Microsoft Teams-wiki-Datendokument Bibliothek auf der SharePoint-Website des Teams gespeichert. Sie können das Inhaltssuche-Tool verwenden, um das Wiki zu durchsuchen, indem Sie die SharePoint-Website des Teams als den zu durchsuchenden Inhaltsspeicherort angeben. 
    
    > [!NOTE]
    > Die Möglichkeit zum Durchsuchen des Wikis nach einem Microsoft-Team oder-Kanal (beim Durchsuchen der SharePoint-Website des Teams) wurde am 2017 veröffentlicht. Wiki-Seiten, die an diesem oder nach dem Datum gespeichert oder aktualisiert wurden, können durchsucht werden. Wiki-Seiten, die zuletzt gespeichert oder vor diesem Datum aktualisiert wurden, sind nicht für die Suche verfügbar. 
  
### <a name="onedrive-for-business"></a>OneDrive for Business
  
- Informationen zum Erfassen einer Liste der URLs für die OneDrive für Business-Websites in Ihrer Organisation finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Das Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive für Business-Websites enthält. Um dieses Skript ausführen zu können, müssen Sie die SharePoint Online-Verwaltungsshell installieren und verwenden. Stellen Sie sicher, dass Sie die URL der mysite-Domäne Ihrer Organisation an jede OneDrive für Unternehmen-Website anfügen, die Sie durchsuchen möchten. Dies ist die Domäne, die alle Ihre OneDrive für Unternehmen enthält; Beispiel: `https://contoso-my.sharepoint.com`. NachFolgend finden Sie ein Beispiel für eine URL für die OneDrive für die Business- `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`Website eines Benutzers:.
    

### <a name="search-queries"></a>Suchabfragen
  
- Beachten Sie bei der Verwendung der Stichwortliste zum Erstellen einer Suchabfrage die folgenden Aspekte.
    
  - Sie müssen das Kontrollkästchen **Keyword-Liste anzeigen** aktivieren und dann jedes Schlüsselwort in eine separate Zeile eingeben, um eine Suchabfrage zu erstellen, in der die Schlüsselwörter (oder Stichwort Ausdrücke) in jeder Zeile durch den **or** -Operator verbunden werden. Wenn Sie nur eine Liste mit Stichwörtern in das Stichwortfeld einfügen oder die **Eingabe** Taste drücken, nachdem Sie ein Schlüsselwort eingegeben haben, werden Sie nicht durch den **or** -Operator verbunden. Hier sind falsch und richtig Beispiel für das Hinzufügen einer Liste von Schlüsselwörtern. 
    
    **Falsch**
    
    ![Die falsche Methode zum Formatieren einer Schlüsselwortliste (durch Einfügen der Liste in das Stichwortfeld)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Richtig**
    
    ![Die richtige Methode zum Formatieren einer Stichwortliste (durch Auswahl von CheckBox und dann Einfügen einer Liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - Sie können auch eine Liste von Schlüsselwörtern oder Keyword-Phrasen in einer Excel-Datei oder in einer nur-Text-Datei vorbereiten und dann Ihre Liste in die Stichwortliste kopieren und einfügen. Hierzu müssen Sie das Kontrollkästchen **Keyword-Liste anzeigen** aktivieren. Klicken Sie dann auf die erste Zeile in der Stichwortliste, und fügen Sie Ihre Liste ein. Jede Zeile aus der Excel-oder Textdatei wird in eine separate Zeile in der Stichwortliste eingefügt. 
    
  - Nachdem Sie eine Abfrage mithilfe der Stichwortliste erstellt haben, empfiehlt es sich, die Suchabfrage Syntax zu überprüfen (im Detailbereich der ausgewählten Suche), um die gewünschte Suchabfrage zu erstellen. In der Suchabfrage, die im Detailbereich unter **Query** angezeigt wird, werden die Schlüsselwörter durch den Text **(c:s)** getrennt. Dies gibt an, dass die Schlüsselwörter durch den **or** -Operator verbunden werden. Wenn Ihre Suchabfrage Bedingungen enthält, werden die Schlüsselwörter und die Bedingungen entsprechend durch den Text **(c:c)** getrennt. Dies gibt an, dass die Schlüsselwörter mit den Bedingungen vom **and-** Operator verbunden sind. Nachfolgend finden Sie ein Beispiel für die Suchabfrage (wird im Detailbereich angezeigt), die bei Verwendung der Stichwortliste und einer Bedingung resultiert. 
    
    ![Beispiel für die Abfrage, die erstellt wird, wenn die Stichwortliste und eine Bedingung verwendet wird](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - Wenn Sie über eine Suchabfrage mit Schlüsselwörtern für nicht englische Zeichen (beispielsweise chinesische Zeichen) verfügen, müssen Sie möglicherweise das Cmdlet **Set-ComplianceSearch** verwenden, um die Language-Eigenschaft für die Inhaltssuche zu konfigurieren. Wenn Sie eine Inhaltssuche mithilfe der GUI im Security & Compliance Center erstellen, ist die Standardsprache neutral. 
    
    Wie können Sie feststellen, ob die Spracheinstellung für eine Inhaltssuche geändert werden muss? Wenn Sie bestimmte inhaltsspeicherorte die nicht-englischen Zeichen enthalten, die Sie suchen, aber die Suche keine Ergebnisse zurückgibt, kann die Spracheinstellung die Ursache sein.
    
    Führen Sie den folgenden Befehl in Security & Compliance Center PowerShell aus, um die Spracheinstellung für eine vorhandene Inhaltssuche zu ändern:
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    Wenn Sie beispielsweise die Spracheinstellung in Chinesisch ändern möchten, verwenden `zh-CN` Sie den Wert für Kulturcode. Nachdem Sie die Spracheinstellung geändert haben, müssen Sie die Suche erneut ausführen. Eine Liste der möglichen Werte für Kulturcode finden Sie unter [CultureInfo-Klasse](https://go.microsoft.com/fwlink/p/?LinkID=184859). Es wird empfohlen, für die Inhaltssuche zwei teilige Kulturcodes für den Wert der Spracheinstellung zu verwenden. Beispiel: `ja-JP` und nicht `ja`.
    

### <a name="searching-inactive-mailboxes"></a>DurchSuchen inaktiver Postfächer
  
Wie bereits erwähnt, können Sie in einer Inhaltssuche inaktive Postfächer durchsuchen. Im folgenden finden Sie einige Punkte, die Sie beachten sollten, wenn Sie inaktive Postfächer durchsuchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv ist, wird die Inhaltssuche weiterhin das inaktive Postfach durchsuchen, wenn Sie die Suche erneut ausführen, nachdem Sie inaktiv wurde.
    
- In einigen Fällen kann ein Benutzer über ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse verfügen. In diesem Fall wird nur das bestimmte Postfach, das Sie als Speicherort für eine Inhaltssuche auswählen, durchsucht. Anders ausgedrückt: Wenn Sie ein Benutzerpostfach zu einer Suche hinzufügen, können Sie nicht davon ausgehen, dass sowohl Ihre aktiven als auch die inaktiven Postfächer durchsucht werden. nur das Postfach, das Sie der Suche explizit hinzufügen, wird durchsucht.
    
- Es wird dringend empfohlen, ein aktives Postfach und ein inaktives Postfach mit derselben SMTP-Adresse zu vermeiden. Wenn Sie die SMTP-Adresse, die derzeit einem inaktiven Postfach zugewiesen ist, wieder verwenden müssen, sollten Sie das inaktive Postfach wiederherstellen oder den Inhalt eines inaktiven Postfachs in einem aktiven Postfach (oder im Archiv eines aktiven Postfachs) wiederherstellen und dann den inaktives Postfach. Weitere Informationen finden Sie in einem der folgenden Themen:
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)
    
  - [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)
    
### <a name="miscellaneous"></a>Sonstiges
  
- Inhalts Suchvorgänge, die auf der Seite " **Inhaltssuche** " im Security _AMP_ Compliance Center erstellt wurden, werden nicht auf der Seite **in-situ &amp; -eDiscovery** in der Exchange-Verwaltungskonsole angezeigt. Der Grund ist, dass die Architektur der Inhaltssuche und die im Security & Compliance Center erstellten Suchobjekte vollständig von der in-Place-eDiscovery-Funktion in Exchange Online unterschiedlich sind. 
    
    Aus demselben Grund werden Suchvorgänge, die auf der Seite für die **Inhaltssuche** erstellt wurden, nicht auf der Seite **Suchen** eines EDiscovery-Falls im Security & Compliance Center angezeigt. 
    
- Was ist der Unterschied zwischen dem Neustarten einer Suche und dem Wiederholen einer Suche? Wenn Sie eine Suche neu starten, werden alle in der Suche angegebenen inhaltsspeicherorte in einer neuen Vorschau Suche erneut durchsucht. Wenn Sie jedoch eine Suche wiederholen, werden nur die inhaltsspeicherorte durchsucht, die beim letzten Ausführen der Suche fehlgeschlagen sind.
   


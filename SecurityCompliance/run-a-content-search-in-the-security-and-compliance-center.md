---
title: 'Ausführen einer Inhaltssuche im Office 365 Security &amp; Compliance Center '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: 'Verwenden Sie Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center Postfächer, SharePoint Online-Websites und OneDrive for Business-Standorte zu suchen. '
ms.openlocfilehash: d480579db1c39d51d4fa8b0931106f135c5339d2
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038318"
---
# <a name="run-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Ausführen einer Inhaltssuche im Office 365 Security &amp; Compliance Center 

Sie können das Inhaltssuche eDiscovery-Tool verwenden, in die Office 365-Sicherheit &amp; Compliance Center für Elemente wie e-Mails, Dokumente und Sofortnachrichtenunterhaltungen führen in Office 365-Organisation zu suchen. Verwenden Sie dieses Tool, um die Suche nach Elementen in diese Office 365-Dienste:
  
- Öffentliche Ordner und Exchange Online-Postfächern
    
- SharePoint Online und OneDrive for Business-Websites
    
- Skype für Business Unterhaltungen
    
- Microsoft Teams 
    
- Office 365-Gruppen
    
Inhaltssuche ist ein neues eDiscovery-Suche-Tool mit neuen und verbesserten Funktionen für Leistung und Skalierung. Verwenden Sie Inhaltssuche sehr große eDiscovery-suchen ausgeführt. Sie können alle Postfächer, alle öffentlichen Exchange-Ordner und alle SharePoint Online-Websites und OneDrive für Unternehmen Konten in einer einzelnen Inhaltssuche suchen. Es gibt keine Grenzwerte für die Anzahl der Speicherorte für Inhalte, die durchsucht werden. Es gibt auch keine Grenzwerte für die Anzahl der Suchvorgänge, die gleichzeitig ausgeführt werden können. Nachdem Sie eine Suche Inhalte, die Anzahl der Speicherorte für Inhalte ausführen und eine geschätzte Anzahl der Suchergebnisse im Detailbereich auf der Seite für die **Inhaltssuche** angezeigt werden. Nach der Ausführung einer Suche können Sie eine Vorschau der Ergebnisse, rufen Sie schlüsselwortstatistiken für eine oder mehrere Suchvorgänge per Massenvorgang bearbeiten Content-Suche und Exportieren der Ergebnisse in einem lokalen Computer. 
  
 **Inhalt**
  
[Erstellen Sie eine Suche](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[Exportieren der Suchergebnisse](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[Vorschau auf Suchergebnisse anzeigen](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[Aktualisieren von Suchergebnissen](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[Bearbeiten einer Suche](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[Erneutes Ausführen einer Suche](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Informationen und Richtlinien zum Erstellen von Suchabfragen und boolesche Suchoperatoren mit finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md). Dieser Artikel enthält auch Informationen zum Suchen nach Typen vertraulicher Informationen und die Suche nach Inhalten, die gemeinsam mit Personen innerhalb und außerhalb Ihrer Organisation verwendet wird.
    
- Um den Zugriff auf die Seite **Inhaltssuche** zu durchsuchen und Vorschau Exportieren von Suchergebnissen haben, ein Administrator, Compliance-beauftragte oder eDiscovery-Manager muss ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier &amp; Compliance Zentriert. Sie müssen weitere Berechtigungen in Exchange Online, SharePoint Online, oder für OneDrive für Websites mit Geschäftsdaten zuweisen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
- Es gibt Grenzwerte auf Inhaltssuche zur Aufrechterhaltung der Integrität und die Qualität der Office 365-Organisationen bereitgestellten Dienste angewendet. In den meisten Fällen diese Grenzwerte können nicht geändert werden, aber beachten Sie diese, damit diese Grenzwerte bei der Planung, Ausführung und Problembehandlung für Suchvorgänge berücksichtigt werden können. Weitere Informationen finden Sie unter [Grenzwerte für die Suche in der Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md).
    
- Finden Sie im Abschnitt Geschätzte Suche Zeiten basierend auf der Anzahl der Postfächer, die in einer einzelnen Inhaltssuche durchsucht werden. 
    
- Wie bereits zuvor erwähnt können Sie Inhalte Suche zum Suchen nach Inhalten in Office 365-Gruppen und Microsoft-Teams. Dies bedeutet, dass Sie die Gruppe Postfach-, freigegebenen Kalender und SharePoint-Websites, die ein Office 365-Gruppe und ein Microsoft-Team zugeordnet suchen können. Darüber hinaus können Sie in einem Microsoft-Team Channel Unterhaltungen suchen. Informationen zu Office 365-Gruppen und Microsoft-Teams, finden Sie unter:
    
  - [Informieren Sie sich über Office 365-Gruppen](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [Hilfe für Microsoft-Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Finden Sie im Abschnitt Tipps zur Suche nach Inhalten in Office 365-Gruppen und Microsoft-Teams. 
    
[Zurück zum Seitenanfang](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>Erstellen Sie eine Suche
<a name="create"> </a>

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
4. Klicken Sie auf **Neu**![Hinzufügen (Symbol)](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
5. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. Dieser Name muss in der Organisation eindeutig sein. 
    
6. Wählen Sie die Speicherorte für Inhalte, die Sie suchen möchten. Sie können die Postfächer, Websites und Öffentliche Ordner in derselben Suche suchen.
    
    ![Wählen Sie die Speicherorte für Inhalte, die Sie suchen möchten](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **Suche überall** Wählen Sie diese Option, um alle Speicherorte für Inhalte in Ihrer Organisation zu suchen. Wenn Sie diese Option auswählen, können Sie auswählen, um alle Postfächer (einschließlich inaktiver Postfächer und die Postfächer für alle Office 365-Gruppen und Microsoft-Teams), suchen alle SharePoint und OneDrive for Business-Websites (einschließlich der Websites für alle Office 365-Gruppen und Microsoft-Teams), und alle öffentlichen Ordner.
    
    ![Klicken Sie auf die Suche überall Option, um alle Speicherorte für Inhalte durchsuchen](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **Benutzerdefinierte Position Auswahl** Wählen Sie diese Option auswählen, die Postfächer und die Websites, die Sie suchen möchten. Wenn Sie diese Option auswählen, haben Sie Flexibilität, um alle Speicherorte für Inhalte für einen bestimmten Dienst (beispielsweise Durchsuchen aller Exchange-Postfächer) zu suchen, oder Sie können bestimmte Speicherorte für Inhalte für Office 365-Dienst suchen.
    
    Behalten Sie Folgendes beachten Sie beim Hinzufügen von Speicherorte für Inhalte zu suchen:
    
    **Postfächer**
    
  - Wenn Sie auf **Hinzufügen klicken**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) zum Angeben von Postfächern zu suchen die Postfach-Auswahl, die angezeigt wird, ist leer. Dies ist entwurfsbedingt zur Verbesserung der Leistung. Um diese Liste Empfänger hinzuzufügen, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld, und klicken Sie auf **Suche**![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif).
    
  - Sie können die Liste der Postfächer Suchen inaktiver Postfächer und Verteilergruppen hinzufügen. Für Verteilergruppen werden die Postfächer von Gruppenmitgliedern durchsucht. Beachten Sie, dass die dynamische Verteilergruppen nicht unterstützt werden.
    
  - Wenn Sie eine Liste mit den inaktiver Postfächer in Ihrer Organisation erhalten möchten, führen Sie den Befehl `Get-Mailbox -InactiveMailboxOnly` in Exchange Online PowerShell. Alternativ können Sie zu **Daten Governance** wechseln \> **Aufbewahrung** in das Wertpapier &amp; Compliance Center, und klicken Sie dann auf **Weitere**![Navigationsleiste Ellipsen](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **inaktiver Postfächer**.
    
  - Sie können auch das Postfach hinzufügen, das ein Office 365-Gruppe oder ein Microsoft-Team zugeordnet ist. In diesem Fall wird nur das Gruppe oder ein Team Postfach gesucht. die Postfächer der Gruppe oder ein Team Elemente werden nicht durchsucht. Wenn sie suchen möchten, müssen Sie speziell für die Suche hinzufügen.
    
  - Wenn Sie keine Postfächer in die Suche einschließen möchten, aktivieren Sie **Wählen Sie bestimmte Postfächer zu suchen**, jedoch fügen Sie kein Postfachs in die Liste hinzu.
    
    **Websites**
    
  - Klicken Sie auf **Hinzufügen**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) Websites für die Suche hinzufügen. Geben Sie die URL für die einzelnen Standorte, die Sie suchen möchten. Das Tool für die Inhaltssuche wird prüfen Sie die URL, und fügen Sie es der Liste der Websites zu suchen. 
    
  - Sie können die SharePoint hinzufügen, die ein Office 365-Gruppe oder ein Microsoft-Team zugeordnet ist. Finden Sie im Abschnitt Hinweise dazu, wie Sie die URL für die Gruppe oder ein Team zu suchen. 
    
  - Wenn Sie keine Websites in einer Suche einschließen möchten, **Wählen Sie bestimmte Websites suchen**auswählen, aber nicht Hinzufügen einer Website zu der Liste.
    
    **Öffentliche Ordner**
    
    Für Öffentliche Ordner können Sie alle öffentlichen Ordner in Exchange Online-Organisation zu suchen oder nicht öffentliche Ordner suchen.
    
7. Klicken Sie auf **Weiter**.
    
8. Auf der Seite **Neue Suche** können Sie Schlüsselwörter und Bedingungen zum Erstellen der Suchabfrage hinzufügen. 
    
    ![Erstellen einer Suchabfrage mit Schlüsselwörtern und Bedingungen](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. Im Feld unter **Was möchten Sie uns suchen?**, geben Sie in das Feld eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Sie können eine komplexere Abfragen verwenden, die einen booleschen Operators, wie **und**, **oder**, **nicht**, **NEAR**oder **ONEAR**verwenden. Sie können auch suchen für vertrauliche Informationen (wie Sozialversicherungsnummern) in Dokumenten, oder suchen Sie nach Dokumenten, die extern freigegeben haben. Wenn Sie das Schlüsselwort Feld leer lassen, werden alle Inhalte, die in der angegebenen Speicherorte für Inhalte befindet sich in den Suchergebnissen enthalten sein. 
    
2. Sie können das Kontrollkästchen **Schlüsselwortliste anzeigen** und den Typ ein Schlüsselworts in jede Zeile klicken. Wenn Sie dies tun, werden die Schlüsselwörter für jede Zeile der **oder** -Operator in der Suchabfrage vorhanden, die erstellt wird. 
    
    ![Sie können ein Schlüsselwort oder Schlüsselwort Phase in einer Zeile in der Liste Schlüsselwörter eingeben.](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    Gründe für die Verwendung der Schlüsselwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort überein. Dadurch können Sie schnell erkennen, welche Schlüsselwörter der am häufigsten (und mindestens) wirksam werden. Sie können auch eine Stichwortbegriff (in Klammern eingeschlossen sind) in einer Zeile. Weitere Informationen zu Suchstatistik finden Sie unter [schlüsselwortstatistiken für die Inhaltssuche Ergebnisse anzeigen](view-keyword-statistics-for-content-search.md).
    
    Finden Sie im Abschnitt Hinweise zur Verwendung der Schlüsselwortliste aus. 
    
3. Klicken Sie auf **Abfrage für Tippfehler überprüfen** , überprüfen Sie Ihre Abfrage für nicht unterstützte Zeichen und boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden häufig ausgeblendet und in der Regel verursacht einen Fehler beim Suchen oder unbeabsichtigte Ergebnisse zurückzugeben. Weitere Informationen zu nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Content Suchabfrage Fehler überprüfen](check-your-content-search-query-for-errors.md).
    
4. Fügen Sie unter **Conditions**Bedingungen auf eine Suchabfrage aus, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben. Jede Bedingung hinzugefügt der KQL Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch den **AND** -Operator verbunden. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und die Bedingung, die in den Ergebnissen enthalten sein müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. 
    
||
|:-----|
|Weitere Informationen zum Erstellen einer Suchabfrage und Bedingungen verwenden finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche ](keyword-queries-and-search-conditions.md). |
   
9. Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten. 
    
    Die Suche wird gestartet. Wenn die Suche abgeschlossen ist, wird die folgende Informationen im Detailfenster angezeigt.
    
    ![Suchstatistik werden im Detailbereich der ausgewählten Content Suche angezeigt.](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. Das Datum und die Uhrzeit der letzten Ausführung die Suche.
    
2. Die Anzahl (und die Gesamtgröße der) der Elemente, die, die gefunden wurden, abgeglichen die Suchabfrage. Beispiele für Elementtypen sind e-Mail-Nachrichten, Kalenderelemente und Dokumenten. Wenn ein Element mehrere Instanzen eines Stichworts, die enthält nach dem gesucht wird, wird er nur einmal in die Gesamtanzahl der Elemente gezählt. Beispielsweise wird übereinstimmenden Wörter "Stock" oder "Tip" und eine e-Mail-Nachricht enthält drei Vorkommen des Worts "Stock", er nur einmal im Feld **Elemente** gezählt. 
    
3. Die Anzahl und die Gesamtgröße der nicht indizierten Elemente in die Speicherorte für Inhalte, die durchsucht wurden. In die Suchstatistik im Detailbereich angezeigt wird die Anzahl der nicht-indizierten Elemente, die den Suchkriterien entsprechen nicht enthalten sein. Wenn ein nicht-indizierten Element entspricht die Suche Abfragen (da es sich um eine andere Nachricht oder ein Dokument Eigenschaften den Suchkriterien entsprechen), werden nicht es in die geschätzte Anzahl der nicht-indizierten Elementen enthalten sein. Jedoch ein nicht-indizierten Element durch die Suchkriterien ausgeschlossen wird, nicht es in die Schätzung des nicht-indizierten Elementen berücksichtigt.
    
4. Die Anzahl der einzelnen Typen von Inhaltsspeicherort, die durchsucht wurde. Beachten Sie für Postfächer, dass archivpostfächern in die Gesamtzahl der Postfächer enthalten sind, die durchsucht wurden. Im vorherigen Beispiel wurden vier Benutzerpostfächer gesucht, und das Archivpostfach für jeden Benutzer aktiviert ist. Deshalb acht Postfächer in die Suchstatistik zitiert werden.
    
5. Links zu den Suchvorschau führt oder führen Sie die Suche erneut aus, um die Statistik für die Suche zu aktualisieren.
    
    Klicken Sie auf **Aktualisieren**, falls erforderlich,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich für die ausgewählte Suche. 
    
[Zurück zum Seitenanfang](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>Exportieren der Suchergebnisse
<a name="export"> </a>

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, sind sie als PST-Dateien auf Ihren Computer heruntergeladen. Beim Exportieren von Inhalt aus SharePoint und OneDrive for Business-Websites werden Kopien der systemeigenen Office-Dokumente exportiert. Es gibt auch zusätzliche Dokumente und Berichte, die mit der exportierten Suchergebnisse enthalten sind. Weitere Informationen finden Sie unter [Export-Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md).
  
## <a name="preview-search-results"></a>Suchergebnisse in der Vorschau anzeigen
<a name="preview"> </a>

Nachdem eine Suche erfolgreich abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzuzeigen. Es gibt eine Reihe von Einschränkungen im Zusammenhang mit Vorschau der Suchergebnisse. Weitere Informationen finden Sie unter [Grenzwerte für die Suche in der Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md). Beachten Sie, dass nicht indizierter Elemente nicht für die Vorschau von verfügbar sind.
  
1. Wählen Sie auf der Seite **Inhaltssuche** eine Suche ein. 
    
2. Klicken Sie im Detailbereich unter **Ergebnisse** auf **Vorschau der Suchergebnisse anzeigen**. Die Seite **Vorschau der Suchergebnisse anzeigen** wird geöffnet und enthält eine Liste der Suchergebnisse. 
    
    Klicken Sie auf eine Spaltenüberschrift zum Sortieren der Ergebnisse basierend auf Betreff, Typ, Absender oder das Datum, an das ein Element im Quellpostfach empfangen wurde.
    
3. Klicken Sie auf ein Element in der Vorschau anzeigen.
    
    Das Element wird im Vorschaubereich geöffnet.
    
4. Wenn Sie ein Dateityp für die Vorschau oder Herunterladen eine Kopie eines Dokuments nicht unterstützt wird, können Sie die **ursprüngliche Datei herunterladen** , um sie auf dem lokalen Computer herunterladen klicken. Für .aspx Webseiten ist die URL für die Seite enthalten, obwohl Sie keinen Zugriff auf die Seite Berechtigungen können. 
    
> [!NOTE]
> Wenn Sie die Suchergebnisse für eine Suche in der Vorschau, die mehr als 7 Tage vor dem letzten Ausführen anzeigen, werden Sie aufgefordert, so aktualisieren Sie die Suchergebnisse. Die Suche wird erneut ausführen, um die aktuellen Ergebnisse zu erhalten, die die Suchabfrage erfüllen. 
  
### <a name="file-types-that-can-be-previewed"></a>Dateitypen, die eine Vorschau angezeigt werden kann

Sie können unterstützte Dateitypen in der Vorschau anzeigen. Wenn Sie ein Dateityp nicht unterstützt wird, müssen Sie herunterladen eine Kopie der Datei auf Ihrem lokalen Computer an. Die folgenden Dateitypen werden unterstützt und können auf der Seite **Vorschau der Suchergebnisse** angezeigt werden. 
  
- TXT, HTML, MHTML
    
- EML
    
- doc, DOCX, DOCM
    
- pptm, PPTX-Format
    
- PDF
    
Darüber hinaus werden die folgenden Dateitypen Container unterstützt. Sie können die Liste der Dateien im Container in der Vorschau anzeigen.
  
- ZIP
    
- .gzip
    
[Zurück zum Seitenanfang](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>Aktualisieren von Suchergebnissen
<a name="restart"> </a>

Wenn Sie die Ergebnisse einer Suche für vorhandene Inhalte aktualisieren, wird die Suchabfrage auf alle angegebenen Speicherorte für Inhalte erneut ausführen. Aktualisieren der Suchergebnisse werden offensichtlich stets aktuellen Daten abgerufen.
  
1. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, für die Sie die Ergebnisse aktualisieren möchten. 
    
2. Klicken Sie im Detailbereich unter **Ergebnisse** auf **Suchergebnisse aktualisieren**.
    
    Wird ein Statusnachrichten angezeigt besagt, dass die Ergebnisse abgerufen werden. Wenn die Suche abgeschlossen ist, wird die aktualisierter Informationen im Detailbereich unter **Ergebnisse** angezeigt. Beachten Sie, dass das Datum im Feld **durchsucht** im Detailbereich auf das aktuelle Datum und die Uhrzeit aktualisiert wurde. Klicken Sie auf **Aktualisieren**, um die Informationen in der Liste der Content-Suche zu aktualisieren,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Zurück zum Seitenanfang](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>Bearbeiten einer Suche
<a name="edit"> </a>

Sie können die Quellpostfächer und die Suchabfrage für eine vorhandene Inhaltssuche ändern.
  
1. Wählen Sie auf der Seite **Inhaltssuche** eine Suche ein. 
    
2. Klicken Sie im Detailbereich unter **Abfrage** auf **Suche bearbeiten**.
    
3. Auf der Seite **Speicherorte** können Sie die Postfächer, Gruppen, SharePoint-Websites oder OneDrive for Business-Websites suchen ändern. Sie können auch auswählen (oder deaktivieren Sie) alle öffentlichen Ordner in Exchange zu durchsuchen. 
    
4. Klicken Sie auf der Seite **Abfrage** können Sie die Suchabfrage bearbeiten. 
    
5. Um die überarbeitete Suche zu starten, klicken Sie auf die **Quellen** oder **Speicherorte** Seite **Suchen** . 
    
    Die überarbeitete Suche wird gestartet. Wenn die Suche abgeschlossen ist, werden die geschätzten Ergebnisse für die überarbeitete Suche im Detailbereich angezeigt.
    
## <a name="retry-a-search"></a>Erneutes Ausführen einer Suche
<a name="retry"> </a>

Wenn eine Suche Fehler zurückgibt, müssen Sie alle die Speicherorte für Inhalte erneut zu durchsuchen. Sie können die Suche, damit nur die Speicherorte für Inhalte, die nicht die Suche wieder sind erneut ausführen. Um alle Speicherorte für Inhalte neu zu suchen, können Sie die Suchergebnisse aktualisieren.
  
1. Wählen Sie die Suche, die die Speicherorte für Inhalte enthält, die Sie erneut suchen möchten, auf der Seite **Durchsuchen von Inhalten** . 
    
2. Klicken Sie im Detailbereich unter **Fehler** auf **Suche wiederholen**.
    
    Wird ein Statusnachrichten angezeigt besagt, dass die Ergebnisse abgerufen werden. Wenn die Suche abgeschlossen ist, wird die aktualisierter Informationen im Detailbereich unter **Ergebnisse** angezeigt. Beachten Sie, dass das Datum im Feld **durchsucht** im Detailbereich auf das aktuelle Datum und die Uhrzeit aktualisiert wurde. Klicken Sie auf **Aktualisieren**, um die Informationen in der Liste der Suchvorgänge zu aktualisieren,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Zurück zum Seitenanfang](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

Nachfolgend finden Sie weitere Informationen zum Content-Suche.
  
[Grenzwerte und Leistung](run-a-content-search-in-the-security-and-compliance-center.md#limits)
  
[Nicht indizierte Elemente](run-a-content-search-in-the-security-and-compliance-center.md#unindexeditems)
  
[Microsoft-Teams und Office 365-Gruppen](run-a-content-search-in-the-security-and-compliance-center.md#teams)
  
[OneDrive for Business](run-a-content-search-in-the-security-and-compliance-center.md#onedrive)
  
[Suchabfragen](run-a-content-search-in-the-security-and-compliance-center.md#queries)
  
[Suchen inaktive Postfächer](run-a-content-search-in-the-security-and-compliance-center.md#inactivemailboxes)
  
[Verschiedenes](run-a-content-search-in-the-security-and-compliance-center.md#misc)
  
[(Zurück zum Seitenanfang)](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
 **Grenzwerte und Leistung**
  
- Eine Beschreibung der die Grenzwerte, die zu dem Feature für die Inhaltssuche angewendet werden, finden Sie unter [Grenzwerte für die Suche in der Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md).
    
- Microsoft sammelt Leistungsinformationen für Content-Suche ausführen, indem Sie alle Office 365-Organisationen. Während die Komplexität der Suchabfrage Suche Zeiten beeinflussen kann, durchsucht der größte Faktor, der bestimmt, wie lange Suchvorgänge nehmen die Anzahl von Postfächern. Zwar Microsoft ein Service Level Agreement für Suche Zeiten keine, wie oft die durchschnittliche Suche für ein Inhaltssuche basierend auf der Anzahl der Postfächer, die die Suche von der folgenden Tabelle aufgeführt.
    
|**Anzahl von Postfächern**|**Durchschnittliche Suche Zeit**|
|:-----|:-----|
|100  <br/> |30 Sekunden  <br/> |
|1,000  <br/> |45 Sekunden  <br/> |
|10,000  <br/> |4 Minuten  <br/> |
|25.000  <br/> |10 Minuten  <br/> |
|50.000  <br/> |20 Minuten  <br/> |
|100,000  <br/> |25 Minuten  <br/> |
   

  
 **Nicht indizierte Elemente**
  
- Wie bereits erklärt, nicht-indizierten Elementen in Speicherorte für Inhalte, die durchsucht werden in der geschätzten Suchergebnisse enthalten. Wenn ein nicht-indizierten Element entspricht die Suche Abfragen (da es sich um eine andere Nachricht oder ein Dokument Eigenschaften den Suchkriterien entsprechen), werden nicht es in die geschätzte Anzahl der nicht-indizierten Elementen enthalten sein. Wenn ein nicht-indizierten Element durch die Suchkriterien ausgeschlossen wird, werden nicht in die geschätzte Anzahl der nicht-indizierten Elementen eingeschlossen werden. Weitere Informationen finden Sie unter [nicht-indizierten Elementen in Inhaltssuche](https://go.microsoft.com/fwlink/p/?LinkId=780739).
    

  
 **Microsoft-Teams und Office 365-Gruppen**
  
- Microsoft-Teams, basieren auf Office 365-Gruppen. Suchen sie ist daher sehr ähnlich. Behalten Sie die folgenden Punkte berücksichtigen, bei der Suche nach Inhalten in Office 365-Gruppen und Microsoft-Teams.
    
  - Zum Suchen nach Inhalt befindet sich im Microsoft-Teams und Office 365 Gruppen müssen Sie angeben, das Postfach und die SharePoint-Website, die ein Team oder eine Gruppe zugeordnet sind.
    
  - Führen Sie das Cmdlet **Get-UnifiedGroup** in Exchange Online zum Anzeigen von Eigenschaften für ein Microsoft-Team oder eine Office 365-Gruppe. Dies ist eine empfehlenswerte Methode zum Abrufen der URL für die Website, die ein Team oder eine Gruppe zugeordnet ist. Beispielsweise wird mit der folgende Befehl ausgewählte Eigenschaften für ein Office 365-Gruppe mit dem Namen Senior führende Team angezeigt: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroup** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
  - Wenn dem Postfach eines Benutzers durchsucht wird, werden keine Microsoft-Teams oder Office 365-Gruppe, die der Benutzer Mitglied ist gesucht werden soll. Auf ähnliche Weise, wenn Sie ein Microsoft-Team oder eine Office 365-Gruppe, nur auf die Gruppenpostfach und Gruppe Website, die Sie angeben suchen werden durchsucht; Postfächer und OneDrive for Business-Konten Gruppenmitglieder werden nicht durchsucht, wenn Sie explizit auf die Suche hinzufügen.
    
  - Wenn Sie eine Liste der Elemente von einem Microsoft-Team oder eine Office 365-Gruppe erhalten möchten, können Sie die Eigenschaften anzeigen, auf die **Home \> Gruppen** Seite im Office 365 Administrationscenter. Alternativ können Sie in Exchange Online PowerShell den folgenden Befehl ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroupLinks** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
  - Unterhaltungen, die Teil eines Microsoft-Teams Kanals sind werden im Postfach gespeichert, die mit dem Microsoft-Team zugeordnet ist. In ähnlicher Weise werden Dateien, die in einem Kanal Teammitglieder freigeben auf das Team SharePoint-Website gespeichert. Daher müssen Sie das Microsoft-Teams Postfach und die SharePoint-Website als einen Inhaltsspeicherort, Gespräche und Dateien in einem Kanal durchsuchen hinzuzufügen.
    
  - 
    
    Alternativ werden Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams, sind in der Exchange Online-Postfach der Benutzer gespeichert, die im Chat teilnehmen. Und Dateien, die ein Benutzer in Chat Unterhaltungen gemeinsam in die OneDrive for Business-Konto des Benutzers, der die Dateifreigaben gespeichert werden. Aus diesem Grund müssen Sie die einzelnen Benutzerpostfächer und OneDrive for Business-Konten als Speicherorte für Inhalte, Gespräche und Dateien in der Liste Chat zu durchsuchen hinzufügen.
    
    > [!NOTE]
    > Benutzer, die Unterhaltungen teilnehmen, die Teil der Liste der Chat in Microsoft-Teams, benötigen ein Exchange Online (Cloud-basierten) Postfach in der Reihenfolge für Chat Unterhaltungen suchen. Dies liegt daran Unterhaltungen, die Teil der Liste der Chat sind in der Cloud-basierten Postfächern Chat Teilnehmer gespeichert sind. Wenn ein Teilnehmer Chat ein Exchange Online-Postfach besitzt, wird nicht Sie Chat Unterhaltungen suchen können. Beispielsweise können in einer Exchange-hybridbereitstellung Benutzer mit einem lokalen Postfach möglicherweise zur Teilnahme an Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams sind. Jedoch in diesem Fall-Inhalten in dieser Unterhaltung nicht durchsucht werden, da der Benutzer nicht über cloudbasierten Postfächer verfügen. 
  
  - Jede Microsoft-Teams oder ein Team Kanal enthält ein Wiki für Notizen und die Zusammenarbeit. Der Wiki-Inhalt wird automatisch in eine Datei mit einem MHT-Format gespeichert. Diese Datei ist in der Dokumentbibliothek Teams Wiki-Daten auf SharePoint-Teamwebsite gespeichert. Inhalt Such-Tool können Sie das Wiki suchen, indem Sie SharePoint-Teamwebsite als Content Speicherort zu suchen. 
    
    > [!NOTE]
    > Die Möglichkeit zum Suchen von Wiki für ein Microsoft-Team oder DDE-Kanal (bei der SharePoint-Teamwebsite Suche) wurde am 22 Juni 2017 veröffentlicht. Wiki-Seiten, die gespeichert oder auf aktualisiert wurden, die Datum oder nachdem verfügbar sind, gesucht werden soll. Zuletzt gespeichert oder vor diesem Datum aktualisiert Wiki-Seiten sind nicht verfügbar für die Suche. 
  

  
 **OneDrive for Business **
  
- Um eine Liste der URLs für die OneDrive for Business-Websites in Ihrer Organisation zu sammeln, finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Das Skript in diesem Artikel erstellt eine Textdatei, die eine Liste mit allen OneDrive for Business-Websites enthält. Wenn Sie dieses Skript ausführen, müssen Sie zum Installieren und Verwenden von SharePoint Online-Verwaltungsshell. Achten Sie darauf, dass Sie die URL für die MySite Domäne Ihrer Organisation zu jedem OneDrive for Business-Site anzufügen, von dem Sie suchen möchten. Dies ist die Domäne, die Ihre OneDrive for Business enthält. beispielsweise `https://contoso-my.sharepoint.com`. Es folgt ein Beispiel für eine URL für einen Benutzer OneDrive for Business-Website: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    

  
 **Suchabfragen**
  
- Halten die folgenden Punkte berücksichtigen, wenn die diese Schlüsselwortliste verwenden, um eine Suchabfrage zu erstellen.
    
  - Sie haben, aktivieren Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** , und geben Sie dann jedes Schlüsselwort in einer separaten Zeile um eine Suchabfrage zu erstellen, in dem die Keywords (oder Schlüsselwort Ausdrücke) in jeder Zeile über der **OR** -Operator verbunden. Wenn Sie nur eine Liste von Schlüsselwörtern in das Feld Stichwort einfügen oder drücken Sie **die EINGABETASTE** nach Eingabe eines Stichworts, werden nicht sie durch den **oder** -Operator verbunden werden. Hier sind falsch und richtig Beispiel für eine Liste der Schlüsselwörter hinzufügen. 
    
    **Falsche**
    
    ![Die falsche Möglichkeit, um ein Schlüsselwort Listenformat (von der Liste in das Feld Schlüsselwort einfügen)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Richtig**
    
    ![Die ordnungsgemäße ein Schlüsselwort Listenformat (durch auswählen das Kontrollkästchen und klicken Sie dann auf einfügen Liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - Sie können auch eine Liste der Schlüsselwörter oder Ausdrücke in einer Excel-Datei oder eine Klartextdatei Schlüsselwort vorbereiten und klicken Sie dann kopieren und fügen Sie Ihrer Liste in der Liste Schlüsselwort. Zu diesem Zweck müssen Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** . Klicken Sie auf der ersten Zeile in der Schlüsselwortliste, und fügen Sie Ihrer Liste. Jede Zeile aus der Datei Excel- oder Text wird in Zeile in der Schlüsselwortliste trennen eingefügt werden soll. 
    
  - Nach der Erstellung einer Abfrage mithilfe der Schlüsselwortliste ist es ratsam, überprüfen Sie, ob die Abfrage Suchsyntax (im Detailbereich der ausgewählten Suche), stellen Sie die Suche Abfrage ist wie gewünscht. Die Schlüsselwörter werden in der Suchabfrage, die im Detailbereich unter **Abfrage** angezeigt wird, durch den Text **(C:s)** getrennt. Dies weist darauf hin, dass die Schlüsselwörter mithilfe der **OR** -Operator verbunden sind. In ähnlicher Weise enthält die Suchabfrage Bedingungen, die Schlüsselwörter und die Bedingungen sind getrennt durch den Text **(c: c)**. Dies weist darauf hin, dass die Schlüsselwörter, die Bedingungen durch den **AND** -Operator verbunden sind. Hier ist ein Beispiel für die Suchabfrage (im Bereich Details angezeigt), die bei der Verwendung der Schlüsselwortliste und eine Bedingung ergibt. 
    
    ![Beispiel für die Abfrage, die bei der Verwendung der Schlüsselwortliste und eine Bedingung erstellt wird](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - Wenn Sie eine Suchabfrage verfügen, die Schlüsselwörter für nicht englische Zeichen (beispielsweise chinesischen Schriftzeichen) enthält, müssen Sie möglicherweise das **Set-ComplianceSearch** -Cmdlet verwenden, um die Language-Eigenschaft für die Inhaltssuche konfigurieren. Beim Erstellen einer über die Benutzeroberfläche in das Wertpapier Inhaltssuche &amp; Compliance Center, die Standardsprache ist neutral. 
    
    Wie können Sie feststellen, wenn Sie die Einstellung für die Sprache für ein Inhaltssuche ändern müssen? Wenn Sie auf bestimmte Speicherorte für Inhalte enthalten, die nicht englische Zeichen an, denen Sie suchen, aber die Suche gibt keine Ergebnisse zurück sind, kann die Language-Einstellung die Ursache sein.
    
    Wenn die Einstellung für die Sprache für eine vorhandene Inhaltssuche ändern möchten, führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell:
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    Angenommen, um die Spracheinstellung Chinesisch (vereinfacht) ändern, verwenden Sie `zh-CN` für die Kultur Codewert. Nachdem Sie die Spracheinstellung ändern, müssen Sie die Suche erneut auszuführen. Eine Liste der Werte für mögliche Kultur finden Sie unter [CultureInfo--Klasse](https://go.microsoft.com/fwlink/p/?LinkID=184859). Content-Suche wird empfohlen, dass Sie zweiteiligen Kultur-Codes für den Wert der Spracheinstellung verwenden; beispielsweise `ja-JP` und nicht `ja`.
    

  
 **Suchen inaktive Postfächer**
  
Wie bereits zuvor erwähnt können Sie inaktiver Postfächer in einer Inhaltssuche suchen. Hier sind einige Dinge im Hinterkopf behalten, inaktiver Postfächer zu suchen.
  
- Wenn eine Inhaltssuche ein Benutzerpostfach enthält und das Postfach dann inaktiv erfolgt, wird die Inhaltssuche weiterhin inaktive Postfach suchen, wenn die Suche erneut ausführen, nachdem es deaktiviert wurde.
    
- In einigen Fällen kann ein Benutzer einer aktiven Postfach- und eines inaktiven Postfachs, die der gleichen SMTP-Adresse verfügen. In diesem Fall wird nur das spezifische Postfach, das Sie als Speicherort für ein Inhaltssuche auswählen gesucht werden soll. Anders ausgedrückt, wenn Sie dem Postfach eines Benutzers zu einer Suche hinzufügen, nicht davon ausgehen, dass ihre aktive und inaktive Postfächer durchsucht werden; Es wird nur das Postfach, das Sie für die Suche explizit hinzu gesucht werden soll.
    
- Es wird dringend empfohlen, dass Sie vermeiden, dass eine aktive Postfach- und inaktiven Postfachs mit der gleichen SMTP-Adresse. Wenn Sie müssen die SMTP-Adresse wiederverwenden, die aktuell eines inaktiven Postfachs zugewiesen ist, wird empfohlen, das inaktive Postfach wiederherstellen oder des Inhalts eines inaktiven Postfachs zu einem aktiven Postfach (oder das Archiv eines aktiven Postfachs wiederherstellen), und Sie löschen die Inaktives Postfach. Weitere Informationen finden Sie in den folgenden Themen:
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md)
    
  - [Wiederherstellen eines inaktiven Postfachs in Office 365](restore-an-inactive-mailbox.md)
    
  - [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)
    

  
 **Verschiedenes**
  
- Erweiterte Suche auf der Seite **Inhaltssuche** in das Wertpapier Content &amp; Compliance Center werden nicht angezeigt, klicken Sie auf der **Compliance-eDiscovery &amp; halten** Seite in der Exchange-Verwaltungskonsole. Dies ist, da die Architektur für die Inhaltssuche und die Search-Objekte in das Wertpapier erstellt &amp; Compliance Center unterscheiden sich grundlegend als das Compliance-eDiscovery-Feature in Exchange Online. 
    
    Die gleichen Grund-Suchvorgänge auf der Seite für die **Inhaltssuche** erstellt werden nicht angezeigt, auf der Seite **sucht** , der einem eDiscovery-Fall in das Wertpapier &amp; Compliance Center. 
    
- Was ist der Unterschied zwischen neu gestartet und eine Suche wiederholen? Wenn Sie eine Suche neu starten, werden alle Speicherorte für Inhalte, die in der Suche angegeben werden erneut in eine neue Preview-Suche durchsucht. Wenn Sie eine Suche wiederholen, werden nur die Speicherorte für Inhalte, die nicht bei der letzten der Suche Ausführung jedoch erneut durchsucht.
   


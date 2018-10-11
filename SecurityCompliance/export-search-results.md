---
title: 'Exportieren der Inhaltssuchergebnisse aus dem Office 365 Security &amp; Compliance Center '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: 'Exportieren Sie die Suchergebnisse aus einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center auf einen lokalen Computer. Emaill e-Mail-Ergebnisse werden als PST-Dateien exportiert. Inhalte aus SharePoint und OneDrive for Business-Websites als systemeigene Office-Dokumente exportiert werden. '
ms.openlocfilehash: 739d2c162dac938d593e0b65ebca3bf2101ec469
ms.sourcegitcommit: 87a3ca55b6e9cf7e9ccf73e64013dc78dd7660f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2018
ms.locfileid: "25494066"
---
# <a name="export-content-search-results-from-the-office-365-security-amp-compliance-center"></a>Exportieren der Inhaltssuchergebnisse aus dem Office 365 Security &amp; Compliance Center 

Nachdem eine Inhaltssuche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, sind sie als PST-Dateien auf Ihren Computer heruntergeladen. Beim Exportieren von Inhalt aus SharePoint und OneDrive for Business-Websites werden Kopien der systemeigenen Office-Dokumente exportiert. Es sind weitere Dokumente und Berichte, die mit der exportierten Suchergebnisse enthalten sind.
  
Darüber hinaus werden alle RMS-verschlüsselten e-Mail-Nachrichten, die in den Ergebnissen einer Inhaltssuche enthalten sind entschlüsselt werden beim Exportieren (als einzelne Nachrichten). Diese Funktion Entschlüsselung ist standardmäßig für Mitglieder der Gruppe der eDiscovery-Manager-Rolle aktiviert. Dies ist, da die Verwaltungsrolle RMS Entschlüsseln dieser Rollengruppe zugewiesen ist. Finden Sie [Weitere Informationen](#more-information) im Abschnitt Weitere Informationen zum RMS-entschlüsselungs, beim Exportieren von Suchergebnissen. 
  
Exportieren Sie die Ergebnisse einer Suche Content umfasst die Ergebnisse vorbereiten, und klicken Sie dann auf einen lokalen Computer herunterladen.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um die Suchergebnisse zu exportieren, müssen Sie die Verwaltungsrolle "Export" in die Office 365-Sicherheit zugewiesen werden &amp; Compliance Center. Die integrierten eDiscovery-Manager-Rollengruppe wird diese Rolle zugewiesen. Es ist nicht in der Standardeinstellung der Rollengruppe "Organisationsverwaltung" zugewiesen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
- Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:


    
  - 32- oder 64-Bit-Versionen von Windows 7 und höher
    
  - Microsoft .NET Framework 4.7
    
  - Einen unterstützten Browser:
    
     - Microsoft Edge
    
        OR
    
     - Microsoft Internet Explorer 10 und höhere Versionen
    
    **Hinweis:** Microsoft herstellen nicht Drittanbieter-Erweiterungen oder Add-ons für ClickOnce-Anwendungen. Exportieren von Suchergebnissen mithilfe von einem nicht unterstützten Browser mit Drittanbieter-Erweiterungen oder Add-ons wird nicht unterstützt. 
    
- Wenn Sie die Suchergebnisse (in Schritt2 beschrieben) herunterladen, können Sie Geschwindigkeit für den Download erhöhen, durch eine Einstellung für die Windows-Registrierung konfigurieren, auf dem Computer, den Sie verwenden, um die Suchergebnisse zu exportieren. Weitere Informationen finden Sie unter [erhöhen die Geschwindigkeit Download beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
    
- Wenn Sie Suchergebnisse exportieren, werden die Daten vorübergehend in einem eindeutigen Microsoft Azure-Speicherort in der Microsoft-Cloud gespeichert, bevor sie sich an Ihren lokalen Computer heruntergeladen wird. Achten Sie darauf Ihrer Organisation kann an den Endpunkt in Azure, ist eine Verbindung herstellen ** \*. blob.core.windows.net** (der Platzhalter stellt einen eindeutigen Bezeichner für Ihren Export). Suche Ergebnisse werden die Daten aus dem Speicherort der Azure-Speicher gelöscht zwei Wochen, nachdem er erstellt wurde. 
    
- Wenn Ihre Organisation einen Proxyserver verwendet, um eine Kommunikation mit dem Internet, müssen Sie die Proxyeinstellungen für den Server auf dem Computer zu definieren, mit denen Sie die Suchergebnisse exportieren (also die Exporttool von Proxy-Server authentifiziert werden kann). Öffnen Sie hierzu die Datei *"Machine.config"* an der Stelle, die mit Ihrer Version von Windows übereinstimmt. 
    
  - **32-bit** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
    
  - **64-bit** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
    
    Fügen Sie die folgenden Zeilen der Datei *machine.config* irgendwo zwischen den `<configuration>` und `</configuration>` Tags. Ersetzen Sie unbedingt `ProxyServer` und `Port` mit den richtigen Werten für Ihre Organisation; beispielsweise `proxy01.contoso.com:80` . 
    
    ```
    <system.net>
       <defaultProxy enabled="true" useDefaultCredentials="true">
         <proxy proxyaddress="http://ProxyServer :Port " 
                usesystemdefault="False" 
                bypassonlocal="True" 
                autoDetect="False" />
       </defaultProxy>
    </system.net>
    ```

- Finden Sie im Abschnitt für eine Beschreibung für die Grenzwerte für Suchergebnisse exportieren. 
    
- Die maximale Größe einer PST-Datei, die exportiert werden kann beträgt 10 GB. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, mit denen Sie die Suchergebnisse exportieren. [Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse](change-the-size-of-pst-files-when-exporting-results.md)angezeigt.
    
## <a name="step-1-prepare-search-results-for-export"></a>Schritt 1: Vorbereiten der Suchergebnisse für Export

Der erste Schritt besteht darin, die Suchergebnisse für den Export vorzubereiten. Beim Vorbereiten der Ergebnisse werden in der Microsoft-Cloud ein Azure Speicherort hochgeladen werden. Notiz, die Inhalte von Postfächern und Websites wird die maximale Datenübertragungsrate 2 GB pro Stunde hochgeladen.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
4. Wählen Sie auf der Seite **Inhaltssuche** eine Suche ein. 
    
5. Klicken Sie im Detailbereich unter **Ergebnisse auf einem Computer exportieren** auf **Export starten**. 
    
    > [!NOTE]
    > Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. Brechen Sie in diesem Fall den Export ab, klicken Sie im Detailbereich für die ausgewählte Suche auf **Suchergebnisse aktualisieren** und starten Sie dann den Export erneut, nachdem die Ergebnisse aktualisiert wurden.  
  
6. Wählen Sie auf der Seite **der Suchergebnisse exportieren** unter **diese Einträge aus der Suche einschließen**eine der folgenden Optionen aus:
    
    - Nur indizierte Elemente exportieren
    
    - Export indiziert und teilweise indizierte Elemente
    
    - Exportieren Sie nur teilweise indizierte Elemente
    
    Finden Sie im Abschnitt [Weitere Informationen](#more-information) für eine Beschreibung dazu wie teilweise indizierte Elemente werden exportiert. Weitere Informationen zu teilweise indizierte Elemente finden Sie unter [teilweise indizierte Elemente in Inhaltssuche](partially-indexed-items-in-content-search.md).
    
7. Wählen Sie unter **Exportieren von Exchange-Inhalte als**eine der folgenden Optionen aus:
    
    - **Eine PST-Datei für jedes Postfach** - exportiert eine PST-Datei für jedes Postfach des Benutzers, die Suchergebnisse enthält. In der gleichen PST-Datei sind alle Ergebnisse aus Archivpostfach des Benutzers enthalten. Beachten Sie, dass diese Option die Postfachordnerstruktur aus dem Quellpostfach wird. 
    
    - **Eine PST-Datei, die alle Nachrichten** - exportiert eine einzelne PST-Datei (mit dem Namen *Exchange.pst* ), die die Suchergebnisse aus alle Quellpostfächer die Suche enthält. Beachten Sie, dass diese Option die Postfachordnerstruktur für jede Nachricht wird. 
    
    - **Eine PST-Datei, die alle Nachrichten in einem gemeinsamen Ordner enthält** - Exporte Suchergebnisse, die eine einzelne PST-Datei, in dem alle Nachrichten, in einem einzigen, auf oberster Ebene Ordner befinden. Mit dieser Option können Bearbeiter überprüfen Sie Elemente in chronologischer Reihenfolge (Absendedatum werden Elemente sortiert) ohne die ursprünglichen Postfachordnerstruktur für jedes Element zu navigieren. 
    
    - **Einzelne Nachrichten** - Exporte Suchergebnisse die als einzelne e-Mail-Nachrichten mit dem MSG-Format. Wenn Sie diese Option auswählen, werden e-Mail-Suchergebnisse in einen Ordner im Dateisystem exportiert. Pfad des Ordners für einzelne Nachrichten ist identisch mit demjenigen, der verwendet wird, wenn Sie die Ergebnisse in PST-Dateien exportiert. 
    
      > [!IMPORTANT]
      > Um die RMS-verschlüsselten Nachrichten entschlüsselt werden, wenn sie exportiert haben, müssen Sie e-Mail-Suchergebnissen als einzelne Nachrichten exportieren. Verschlüsselte Nachrichten bleibt verschlüsselt, wenn Sie die Suchergebnisse als eine PST-Datei exportieren. 
  
8. Klicken Sie auf das Kontrollkästchen **Deduplizierung aktivieren** , um doppelte Nachrichten ausschließen. Diese Option ist nur dann, wenn die Inhaltsquellen der Suche Exchange-Postfächer oder Öffentliche Ordner enthält. 
    
    Wenn Sie diese Option auswählen, wird nur eine Kopie einer Nachricht exportiert werden, auch wenn mehrere Kopien der gleichen Nachricht in die Postfächer gefunden werden, die durchsucht wurden. Der Export-Ergebnisbericht (Results.csv) enthält eine Zeile für jede Kopie von doppelte Nachrichten, damit Sie die Postfächer (oder Öffentliche Ordner) erkennen können, die eine Kopie der doppelten Nachricht enthalten. Weitere Informationen zu Deduplizierung und wie doppelte Elemente erkannt werden, finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md).
    
9. Klicken Sie auf das Kontrollkästchen **Versionen für SharePoint-Dokumente einschließen** , um alle Versionen von SharePoint-Dokumenten zu exportieren. Diese Option ist nur dann, wenn die Inhaltsquellen der Suche umfasst SharePoint oder OneDrive for Business-Websites. 
    
10. Klicken Sie auf das Kontrollkästchen **Exportieren von Dateien in einem komprimierten Ordner (ZIP)** , um die Suchergebnisse in komprimierten Ordner zu exportieren. Diese Option ist verfügbar, nur Exchange-Elemente als einzelne Nachrichten exportiert werden soll, wenn die Suchergebnisse SharePoint oder OneDrive Dokumente enthalten. Diese Option wird in erster Linie den Grenzwert 260 Zeichen in Windows Dateipfadnamen umgehen, wenn Elemente exportiert werden. Finden Sie die "Dateinamen der exportierten Elemente" im Abschnitt [Weitere Informationen](#more-information) . 
    
11. Klicken Sie auf **Export starten**.
    
    Die Suchergebnisse werden vorbereitet für das Herunterladen, was bedeutet, dass sie in der Azure Speicherort in der Microsoft-Cloud hochgeladen haben. Wenn die Suchergebnisse zum Download bereit sind, wird der Link **Download exportiert Ergebnisse** im Detailbereich unter **Exportieren Sie die Ergebnisse auf einem Computer** angezeigt. 
  
## <a name="step-2-download-the-search-results"></a>Schritt 2: Herunterladen der Suchergebnisse

Im nächste Schritt werden die Suchergebnisse aus dem Speicherort der Azure-Speicher auf dem lokalen Computer herunterladen.
  
Wie bereits erklärt können Sie die Download-Geschwindigkeit erhöhen, durch eine Einstellung für die Windows-Registrierung konfigurieren, auf dem Computer, den Sie verwenden, um die Suchergebnisse zu exportieren. Weitere Informationen finden Sie unter [erhöhen die Geschwindigkeit Download beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Klicken Sie auf **Download exportiert Ergebnisse**, klicken Sie im Detailbereich für die Suche, dass Sie den Export für, unter **Exportieren Sie die Ergebnisse auf einem Computer**gestartet.
    
    Das Fenster **Download Ergebnisse exportiert** wird angezeigt und enthält die folgende Informationen zu den Suchergebnissen, die auf Ihrem Computer heruntergeladen werden. 
    
    - Die Anzahl der Elemente, die heruntergeladen werden.
    
    - Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.
    
    - Ob indiziert oder nicht-indizierten exportiert werden. Nicht indizierte Elemente sind Elemente, die ein bekanntes Format haben, werden verschlüsselt oder aus anderen Gründen indiziert wurden nicht. Weitere Informationen finden Sie unter [nicht-indizierten Elementen in Inhaltssuche](partially-indexed-items-in-content-search.md).
    
    - Unabhängig davon, ob Versionen von SharePoint-Dokumente heruntergeladen werden.
    
    - Der Status des Exportvorgangs Vorbereitung. Sie können die Suchergebnisse herunterladen, selbst wenn die Vorbereitung der Daten abgeschlossen ist, nicht starten.
    
2. Klicken Sie unter **Schlüssel exportieren**auf **in die Zwischenablage kopieren**. Sie werden dieser Schlüssel in Schritt 5 verwenden, um die Suchergebnisse herunterzuladen.
    
    > [!NOTE]
    > Da jeder kann installieren und das eDiscovery-Export-Tool starten und dann diesen Schlüssel verwenden, um die Suchergebnisse herunterzuladen, müssen Sie unbedingt müssen Sie Vorsichtsmaßnahmen gegen dieser Schlüssel schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen. 
  
3. Klicken Sie auf **Ergebnisse herunterladen**.
    
4. Wenn Sie aufgefordert werden, installieren Sie **MicrosoftOffice 365 eDiscovery-Exporttool**, klicken Sie auf **Installieren**.
    
5. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.
    
6. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der großen Menge von Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie Suchergebnisse auf einem lokalen Laufwerk herunterladen. nicht auf ein Netzlaufwerk oder anderen Speicherort im Netzwerk herunterladen. 
  
1. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Die **eDiscovery-Exporttool** zeigt Statusinformationen über den Exportvorgang, einschließlich eine Schätzung der Anzahl (und Größe) der verbleibenden Elemente heruntergeladen werden. Wenn der Exportvorgang abgeschlossen ist, können Sie die Dateien in den Speicherort zugreifen, in dem sie heruntergeladen wurden. 
    

  
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

Nachfolgend finden Sie weitere Informationen zum Exportieren von Suchergebnissen.
  
[Export-Grenzwerte](export-search-results.md#export-limits)
  
[Exportieren von Berichten](export-search-results.md#export-reports)
  
[Exportieren von teilweise indizierte Elemente](#exporting-partially-indexed-items)
  
[Exportieren einzelne Nachrichten oder PST-Dateien](export-search-results.md#Exporting-individual-messages-or-PST-files)
  
[Entschlüsseln von RMS-verschlüsselten Nachrichten](export-search-results.md#Decrypting-RMS-encrypted-messages)
  
[Dateinamen der exportierten Elemente](export-search-results.md#Filenames-of-exported-items)
  
[Verschiedenes](export-search-results.md#miscellaneous)
  
 ### <a name="export-limits"></a>Export-Grenzwerte
  
- Exportieren von Suchergebnissen aus der Sicherheit &amp; Compliance Center hat die folgenden Einschränkungen:
    
  - Sie können bis zu 2 TB Daten aus einer einzelnen Inhaltssuche exportieren. Wenn die Suchergebnisse größer als 2 TB sind, erwägen Sie Datumsbereiche oder andere Typen von Filtern zum Verringern Sie der Gesamtgröße der Suchergebnisse.
    
  - Ihre Organisation kann bis zu 2 TB Daten während eines Tages exportieren.
    
  - Sie können maximal 10 Exporte zur selben Zeit innerhalb Ihrer Organisation ausgeführt haben.
    
  - Ein einzelner Benutzer kann maximal drei Exporte zur selben Zeit ausführen.
    
  - Exportieren von Berichten Inhaltssuche zählt keine gegen einen der Export Grenzwerte. 
    
- Wie bereits erwähnt, werden Suchergebnisse aus Postfächern und Websites auf den Azure Speicherort hochgeladen (gemäß [Schritt 1: Vorbereiten der Suchergebnisse für den Export](export-search-results.md#step1)) die maximale Datenübertragungsrate 2 GB pro Stunde.
    
- Die maximale Größe einer PST-Datei, die exportiert werden kann beträgt 10 GB standardmäßig. Das bedeutet, wenn die Suchergebnisse aus dem Postfach eines Benutzers größer als 10 GB sind, die Suchergebnisse für das Postfach in zwei (oder mehrere) separaten PST-Dateien exportiert werden sollen. Darüber hinaus alle Suchergebnisse in eine einzelne PST-Datei exportiert werden soll, wird die PST-Datei in zusätzliche PST-Dateien trennen werden, wenn die Gesamtgröße der Suchergebnisse größer als 10 GB ist. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, mit denen Sie die Suchergebnisse exportieren. [Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse](change-the-size-of-pst-files-when-exporting-results.md)angezeigt.
    
    Darüber hinaus wird nicht die Suchergebnisse aus einem bestimmten Postfach in mehreren PST-Dateien aufgeteilt werden, es sei denn, die Inhalte aus ein einzelnes Postfach mehr als 10 GB sind. Wenn Sie entschieden haben, um die Suchergebnisse exportieren in eine PST-Datei für, die alle Nachrichten in einem gemeinsamen Ordner enthält und die Suchergebnisse sind größer als 10 GB, die Elemente sind weiterhin in chronologischer Reihenfolge organisiert, damit sie in zusätzliche PST-Dateien, die basierend auf der gesendeten d trennen werden wird Datum.
     
 ### <a name="export-reports"></a>Exportieren von Berichten
  
- Wenn Sie die Suchergebnisse exportieren, sind die folgenden Berichte zusätzlich zu den Suchergebnissen enthalten.
    
  - **Zusammenfassung exportieren** Ein Excel-Dokument, eine Zusammenfassung des Exports enthält. Hierzu zählen Informationen wie die Anzahl der Inhaltsquellen, die durchsucht wurden, die geschätzten und heruntergeladenen Größen der Suchergebnisse und der geschätzten und heruntergeladenen Anzahl von Elementen, die exportiert wurden. 
    
  - **Manifest** Eine Manifestdatei (im XML-Format), die Informationen über jedes Element in den Suchergebnissen enthalten enthält. 
    
  - **Ergebnisse** Ein Excel-Dokument, das Informationen über jedes Element enthält, die als Suchergebnis Download ist. Für e-Mails die, das Ergebnis-Protokoll enthält Informationen zu jeder Nachricht, einschließlich: 
    
      - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
        
      - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
        
      - Die Betreffzeile der Nachricht.
        
      - Absender und Empfänger der Nachricht.
        
      - Gibt an, ob die Nachricht eine doppelte Nachricht ist, wenn Sie die Option Deduplizierung aktiviert, wenn Sie die Suchergebnisse exportieren. Doppelte Nachrichten müssen einen Wert in der Spalte **doppelte Element** , die die Nachricht als ein Duplikat identifiziert. Der Wert in der Spalte **doppelte Element** enthält die Elementidentität der Nachricht, die exportiert wurde. Weitere Informationen finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md).
        
      Für Dokumente aus SharePoint und OneDrive for Business-Websites, das Ergebnis-Protokoll enthält Informationen zu den einzelnen Dokumenten, einschließlich:
        
      - Die URL für das Dokument.
        
      - Die URL für die Websitesammlung, in dem das Dokument gespeichert ist.
        
      - Das Datum, das das Dokument zuletzt geändert wurde.
        
      - Der Name des Dokuments (der in der Spalte Betreff im Protokoll Ergebnis befindet).
    
  - **Nicht indizierte Elemente** Ein Excel-Dokument, das Informationen über alle teilweise indizierte Elemente enthält, die in den Suchergebnissen enthalten sein wird. Wenn Sie beim Erstellen des Berichts der Suchergebnisse teilweise indizierte Elemente einschließen, in diesem Bericht wird weiterhin heruntergeladen werden, aber leer. 
    
  - **Fehler und Warnungen** Enthält Fehler und Warnungen für Dateien, die während des Exports aufgetreten ist. Finden Sie unter der Spalte Fehlerdetails spezifische Informationen für jeden einzelnen Fehler oder eine Warnung. 
    
  - **Elemente übersprungen** Beim Exportieren von Suchergebnissen aus SharePoint und OneDrive for Business-Websites wird der Exportvorgang in der Regel ein übersprungene Elemente-Bericht (SkippedItems.csv) enthalten. In diesem Bericht zitiert Elemente sind in der Regel Elemente, die heruntergeladen werden nicht, wie beispielsweise einen Ordner oder ein Dokument festgelegt. Nicht exportieren dieser Elementtypen ist entwurfsbedingt. Für andere Elemente, die übersprungen wurden, Anzeigen der 'Fehlertyp' und 'Fehlerdetails' Feld im Bericht übersprungene Elemente der Grund dafür das Element wurde übersprungen, und nicht mit den anderen Suchergebnissen Download war. 
    
  - **Ablaufverfolgungsprotokoll** Enthält detaillierte Informationen über den Exportvorgang anzeigt und Probleme während des Exports aufdecken helfen. 
    
    > [!NOTE]
    > Sie können diese Dokumente nur exportieren, ohne die eigentlichen Suchergebnisse exportieren. Finden Sie unter [Exportieren eines Berichts Inhaltssuche](export-a-content-search-report.md). 
  
 ### <a name="exporting-partially-indexed-items"></a>Exportieren von teilweise indizierte Elemente
  
- Wenn Sie Postfachelemente aus einer Inhaltssuche exportieren, der alle Postfachelemente in den Suchergebnissen zurückgibt (, da keine Schlüsselwörter in der Suchabfrage enthalten), teilweise indizierte Elemente werden nicht kopiert werden, in die PST-Datei, die nicht-indizierten Elemente enthält. Dies ist, da alle Elemente, einschließlich teilweise indizierte Elemente, automatisch in den regulären Suchergebnissen enthalten sind. Dies bedeutet, dass teilweise indizierte Elemente eingeschlossen werden in eine PST-Datei (oder als einzelne Nachrichten), die andere, indizierte Elemente enthält.
    
    Darüber hinaus wird, wenn Sie die indiziert und teilweise indizierte Elemente exportieren oder wenn Sie nur die indizierte Elemente aus einer Inhaltssuche exportieren, die alle Elemente zurückgibt, die gleiche Anzahl von Elementen heruntergeladen. In diesem Fall, auch wenn der geschätzten für die Inhaltssuche Suchergebnisse (angezeigt in die Suchstatistik in das Wertpapier &amp; Compliance Center) umfassen weiterhin eine separate Schätzung für die Anzahl der teilweise indizierte Elemente. Nehmen wir beispielsweise an, für die Suche, die alle Elemente (keine Schlüsselwörter in der Suchabfrage) enthält die Schätzung für das zeigt, dass 1.000 Elemente gefunden wurden und 200 teilweise indizierte Elemente auch gefunden wurden. In diesem Fall umfassen die 1.000 Elemente die teilweise indizierte Elemente, da die Suche alle Elemente zurückgibt. Anders ausgedrückt, stehen 1.000 Elemente (gesamt) von der Suche und nicht 1.200 Elemente (wie erwartet) zurückgegeben. Wenn Sie die Ergebnisse dieser Suche exportieren, und wählen Sie auf Export indiziert und teilweise indizierte Elemente (oder nur indizierte Elemente), und klicken Sie dann 1.000 Elemente werden heruntergeladen. In diesem Fall liegt dies daran teilweise indizierte Elemente sind in der regulären (indizierte) Ergebnisse enthalten, wenn Sie eine leere Search-Abfrage verwenden, um alle Elemente zurückzugeben. In diesem Beispiel wenn Sie nur teilweise indizierte Elemente, exportieren würde dann die 200 nicht indizierter Elemente heruntergeladen werden.
    
    Beachten Sie, dass im vorherigen Beispiel (Wenn Sie indiziert und teilweise indizierte Elemente oder exportieren Sie exportieren nur indizierte Elemente) der Lieferumfang der exportierten Suchergebnisse **Exportieren** Zusammenfassungsbericht 1.000 Elemente geschätzte Elemente und 1.000 heruntergeladen aufgelistet würde Elemente für den gleichen Gründen wie weiter oben beschrieben. 
    
- Wenn die Suche, der Sie exportieren Ergebnisse aus einer Suche nach bestimmten Speicherorte für Inhalte oder alle Speicherorte für Inhalte in Ihrer Organisation war, werden nur die teilweise Elemente Speicherorte für Inhalte, die Elemente enthält, die den Suchkriterien entsprechen, exportiert. Anders ausgedrückt, wenn keine Suchergebnisse in einem Postfach oder Website gefunden werden, klicken Sie dann alle Elemente in diesem Postfach teilweise indiziert oder Website werden nicht exportiert werden. Der Grund dafür ist, dass die Wahrscheinlichkeit der Export Fehler erhöhen und die lange es, die dauert erhöhen zu exportieren, und Laden Sie die Suchergebnisse, möglicherweise exportieren teilweise indizierte Elemente aus vielen Standorten in der Organisation.
    
    Um teilweise indizierte Elemente aus allen Speicherorte für Inhalte für die Suche zu exportieren, Konfigurieren der Suche zum Zurückgeben von allen Elementen (durch Entfernen von Schlüsselwörter vom Search-Abfrage), und anschließend nur teilweise indizierte Elemente zu exportieren, wenn Sie die Suchergebnisse exportieren.
    
    ![Verwenden Sie die Thrid Export-Option zum Exportieren von nur nicht-indizierten Elementen](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- Beim Exportieren von Suchergebnissen aus SharePoint oder OneDrive for Business-Websites hängt die Möglichkeit zum Exportieren von nicht-indizierten Elementen auch die Export-Option, die Sie auswählen und gibt an, ob eine Website, die durchsucht wurde einem indizierten Element enthält, die den Suchkriterien entspricht. Beispielsweise werden Wenn Sie bestimmte SharePoint oder OneDrive for Business-Websites suchen und keine Suchergebnisse gefunden werden, klicken Sie dann keine nicht indizierten Elemente aus dieser Websites exportiert werden, wenn Sie die zweite Exportoption zum Exportieren von indizierter und nicht indizierter Elementen wählen. Wenn einem indizierten Element aus einer Website die Suchkriterien übereinstimmt, werden alle nicht-indizierten Elemente aus dieser Website exportiert beim Exportieren von indizierter und nicht indizierter Elementen. In der folgenden Abbildung sind die Exportoptionen, die basierend auf unabhängig davon, ob eine Website einem indizierten Element enthält, die den Suchkriterien entspricht.
    
    ![Wählen Sie die Exportoption basierend auf unabhängig davon, ob eine Website einem indizierten Element enthält, die den Suchkriterien entspricht](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    A – nur indizierte Elemente, die den Suchkriterien entspricht, werden exportiert. Keine teilweise indizierte Elemente werden exportiert.
    
    B – wenn keine indizierte Elemente aus einer Website, die den Suchkriterien entsprechen, werden nicht teilweise indizierte Elemente aus derselben Website exportiert. Wenn indizierte Elemente aus einer Website in den Suchergebnissen zurückgegeben werden, werden die teilweise indizierte Elemente aus dieser Website exportiert. Anders ausgedrückt, werden nur die teilweise indizierte Elemente von Websites, die Elemente enthält, die den Suchkriterien entsprechen, exportiert.
    
    C – alle teilweise indizierte Elemente aus allen Websites in der Suche werden exportiert, unabhängig davon, ob eine Website Elemente enthält, die den Suchkriterien entsprechen.
    
    Wenn Sie teilweise indizierte Elemente exportieren, werden teilweise indizierten Postfachelemente in einer separaten PST-Datei, unabhängig von der Option exportiert, die Sie unter **Exchange exportieren Inhalte als**auswählen.

- Wenn die Suche teilweise indizierte Elemente zurückgegeben werden Ergebnisse (, da die anderen Eigenschaften einer teilweise indizierter Elemente den Suchkriterien), und klicken Sie dann mit den Suchergebnissen regulären diese teilweise indizierten exportiert werden. Daher, wenn Sie indizierte Elemente und teilweise indizierte Elemente exportieren (durch Auswählen der Exportoption **alle Elemente, einschließlich Schriftarten, die unbekanntes Format haben, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht** ), exportiert die teilweise indizierte Elemente mit dem regulären Ergebnis werden im Bericht Results.csv aufgeführt. Sie werden nicht in den Bericht nicht indizierten items.csv aufgeführt werden.
    
 ### <a name="exporting-individual-messages-or-pst-files"></a>Exportieren einzelne Nachrichten oder PST-Dateien
  
- Wenn der Dateiname der Pfad einer Nachricht die maximale Anzahl von Zeichen für Windows überschreitet, wird der Dateiname der Pfad gekürzt. Aber den Namen der Originaldatei Pfad wird im Manifest und ResultsLog angezeigt werden.
    
- Wie bereits erklärt e-Mail-Suche, die Ergebnisse in einen Ordner im Dateisystem exportiert werden. Pfad des Ordners für einzelne Nachrichten würde den Ordnerpfad in das Postfach des Benutzers zu replizieren. Beispiel für eine Suche mit dem Namen "ContosoCase101" Nachrichten im Posteingang des Benutzers würde werden befindet sich im Pfad Ordners `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`. 
    
- Wenn Sie e-Mail-Nachrichten in eine PST-Datei, die alle Nachrichten in einem gemeinsamen Ordner exportieren, sind in den Ordner der obersten Ebene einen Ordner **Gelöschte Elemente** und Ordner ein **Suchordner** enthalten. Dieser Ordner werden leer sein. 
  
 ### <a name="decrypting-rms-encrypted-messages"></a>Entschlüsseln von RMS-verschlüsselten Nachrichten
  
- Wie bereits erklärt müssen zum RMS-verschlüsselten Nachrichten entschlüsselt werden, wenn Sie diese, exportieren Sie die Suchergebnisse als einzelne Nachrichten exportieren. Wenn Sie die Suchergebnisse in eine PST-Datei exportieren, bleibt RMS-verschlüsselten Nachrichten verschlüsselt.
    
- Das Feature des RMS-Entschlüsselung in Inhaltssuche nicht entschlüsselt werden Nachrichten, die mit Office 365 Message Encryption (OME) verschlüsselt, wenn Sie Suchergebnisse exportieren. Wenn eine mit OME verschlüsselte Nachricht von einem Benutzer in Ihrer Organisation gesendet wird, die Kopie der Nachricht in den Ordner des Benutzers gesendet wird nicht verschlüsselt und werden sichtbar, nachdem er exportiert wird. Jedoch, wenn verschlüsselte Nachrichten mit OME von Benutzern in Ihrer Organisation empfangen werden, werden nicht sie entschlüsselt werden, nachdem sie exportiert haben. Weitere Informationen zu OME finden Sie unter [Office 365 Message Encryption](https://go.microsoft.com/fwlink/p/?linkid=844966).
    
- Nachrichten, die nicht entschlüsselt werden, werden im Bericht **ResultsLog** gekennzeichnet. Dieser Bericht enthält die Spalte **Status decodieren**und ein Wert in dieser Spalte der **decodiert** identifiziert die Nachrichten, die wurden entschlüsselt. 
    
- Diese Funktion Entschlüsselung umfasst derzeit nicht verschlüsselte Inhalte aus SharePoint und OneDrive for Business-Websites. Nur RMS-verschlüsselten e-Mail-Nachrichten werden entschlüsselt werden, wenn Sie sie exportieren.
    
- Wenn eine RMS-verschlüsselten e-Mail-Nachricht eine Anlage (beispielsweise ein Dokument oder eine andere e-Mail-Nachricht), die auch verschlüsselt ist enthält, wird nur die obersten Ebene e-Mail-Nachricht entschlüsselt.
    
- Eine RMS-verschlüsselten e-Mail-Nachricht nicht als Vorschau angezeigt. Um eine verschlüsselte Nachricht anzuzeigen, müssen Sie diese exportieren.
    
- Wenn Sie jemanden entschlüsseln RMS-verschlüsselten Nachrichten müssen, müssen Sie zum Erstellen einer benutzerdefinierten Rollengruppe (durch Kopieren der integrierten eDiscovery Rollengruppe Manager), und entfernen Sie die Verwaltungsrolle RMS entschlüsseln aus die benutzerdefinierte Rollengruppe. Fügen Sie die Person, die Sie nicht als Mitglied der Gruppe benutzerdefinierte Rolle Nachrichten entschlüsseln möchten.
  
 ### <a name="filenames-of-exported-items"></a>Dateinamen der exportierten Elemente
  
- Es ist eine 260 Zeichen-Limit (vom Betriebssystem) für den vollständigen Pfadnamen für e-Mail-Nachrichten und websitedokumente auf Ihrem lokalen Computer exportiert. Der vollständigen Pfadnamen für exportierte Elemente enthält das Element ursprünglichen Speicherort und den Speicherort des Ordners auf dem lokalen Computer, auf dem die Suchergebnisse auf heruntergeladen werden. Wenn Sie angeben, dass die Suchergebnisse auf herunterladen beispielsweise `C:\Users\Admin\Desktop\SearchResults` in das eDiscovery-Export-Tool, klicken Sie dann der vollständige Pfadnamen für ein heruntergeladenen e-Mail-Element wäre `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`.
    
    Die 260 Zeichen überschritten wird, wird der vollständige Pfadname für ein Element abgeschnitten.
    
  - Wenn Sie der vollständigen Pfadnamen länger als 260 Zeichen ist, wird der Dateiname verkürzt zum Abrufen der Grenzwert; Beachten Sie, dass der abgeschnittene Dateinamen (mit Ausnahme der Erweiterungs) nicht kleiner als 8 Zeichen werden.
    
  - Wenn der vollständige Pfadname nach den Dateinamen verkürzen weiterhin zu lang ist, wird das Element von seinem aktuellen Speicherort zum übergeordneten Ordner verschoben. Wenn der Pfadname weiterhin zu lang, wird der Prozess wird wiederholt: kürzen Sie den Dateinamen, und wenn es sich bei Bedarf erneut in dem übergeordneten Ordner zu verschieben. Dieser Prozess wird wiederholt, bis Sie der vollständige Pfadnamen der Grenzwert 260 Zeichen ist.
    
  - Wenn ein abgeschnittene vollständigen Pfadnamen bereits vorhanden ist, wird am Ende des Dateinamens eine Versionsnummer hinzugefügt; beispielsweise `statusmessage(2).msg`.
    
    Um dieses Problem zu verringern, sollten Sie Suchergebnisse an einen Speicherort mit einem kurzen Pfadnamen herunterladen. Herunterladen von Suchergebnissen beispielsweise in einen Ordner namens `C:\Results` fügen Sie weniger Zeichen in die Pfadnamen der exportierten Elemente als herunterladen auf einen Ordner namens `C:\Users\Admin\Desktop\Results`.
    
- Beim Exportieren von Dokumenten Site ist es auch möglich, dass der ursprüngliche Dateiname eines Dokuments geändert wird. In diesem Fall speziell für Dokumente, die aus einer SharePoint oder OneDrive for Business-Website gelöscht wurden, die in die Warteschleife gestellt worden ist. Nachdem ein Dokument, das auf einer Website befindet, in der Warteschleife ist, gelöscht wurde, ist gelöschten Dokuments automatisch in der Bibliothek permanentes halten für die Website verschoben (die erstellt wurde, wenn die Website in die Warteschleife gestellt wurde). Wenn gelöschten Dokuments in die Bibliothek permanentes Archiv verschoben wird, wird eine zufällig generiert und eindeutige ID an den ursprünglichen Namen des Dokuments angefügt. Wenn der Dateiname für ein Dokument ist beispielsweise `FY2017Budget.xlsx` und dieses Dokument später gelöscht und in die Bibliothek permanentes Archiv verschoben wird der Dateiname des Dokuments, der in der Bibliothek permanentes Archiv verschoben wird in etwa wie folgt geändert `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`. Wenn ein Dokument in der Bibliothek permanentes halten der Abfrage eine Inhaltssuche entspricht und exportieren Sie die Ergebnisse dieser Suche, ist die exportierte Datei den geänderten Dateinamen. In diesem Beispiel wird der Dateiname des exportierten Dokuments wäre `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.
    
    Darüber hinaus wird bei der Änderung in einem Dokument befindet sich auf einer Website, die in der Warteschleife ist (und versionsverwaltung für die Dokumentbibliothek auf der Website aktiviert wurde), eine Kopie der Datei automatisch in der Bibliothek permanentes halten erstellt. In diesem Fall wird eine zufällig generiert und eindeutige ID auch auf den Dateinamen des Dokuments angefügt, die in der Bibliothek permanentes halten kopiert wird.
    
    Der Grund, warum Dateinamen von Dokumenten, die verschoben oder kopiert haben, in die Bibliothek permanentes halten ist um miteinander in Konflikt stehende Dateinamen zu verhindern. Weitere Informationen über das Platzieren von eines Haltestatus für Websites und die Bibliothek permanentes halten finden Sie unter [Übersicht über die Compliance - Archiv im SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).
    
 ### <a name="miscellaneous"></a>Verschiedenes
  
- Alle Suchergebnisse und die Exportieren von Berichten in einem Ordner mit dem gleichen Namen wie die Inhaltssuche enthalten sind. Die e-Mail-Nachrichten, die exportiert wurden befinden sich in einem Ordner mit dem Namen **Exchange**. Dokumente befinden sich in einen Ordner namens **SharePoint**. 
    
- Die Dateisystem-Metadaten für Dokumente in SharePoint, und OneDrive for Business-Websites wird beibehalten, wenn Dokumente auf Ihrem lokalen Computer exportiert werden. Die Dokumenteigenschaften bedeutet, wie etwa erstellt und Datum der letzten Änderung, werden nicht geändert, wenn Dokumente exportiert werden.
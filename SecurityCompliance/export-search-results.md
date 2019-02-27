---
title: Exportieren von Inhalts Suchergebnissen aus dem Office 365 Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: 'Exportieren Sie die Suchergebnisse aus einer Inhaltssuche im Office 365 Security & Compliance Center auf einen lokalen Computer. E-Mail-Ergebnisse werden als PST-Dateien exportiert. Inhalte aus SharePoint und OneDrive for Business-Websites werden als systemeigene Office-Dokumente exportiert. '
ms.openlocfilehash: 1a94a7ed948de06bfc8f3f9a2dc9c8a5d26ca653
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296568"
---
# <a name="export-content-search-results-from-the-office-365-security--compliance-center"></a>Exportieren von Inhalts Suchergebnissen aus dem Office 365 Security & Compliance Center

Nachdem eine Inhaltssuche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse auf einen lokalen Computer exportieren. Wenn Sie e-Mail-Ergebnisse exportieren, werden Sie als PST-Dateien auf Ihren Computer heruntergeladen. Wenn Sie Inhalte aus SharePoint und OneDrive for Business-Websites exportieren, werden Kopien von systemeigenen Office-Dokumenten exportiert. Die exportierten Suchergebnisse enthalten zusätzliche Dokumente und Berichte.
  
Darüber hinaus werden alle RMS-verschlüsselten e-Mail-Nachrichten, die in den Ergebnissen einer Inhaltssuche enthalten sind, entschlüsselt, wenn Sie Sie exportieren (als einzelne Nachrichten). Diese Entschlüsselungsfunktion ist standardmäßig für Mitglieder der eDiscovery-Manager-Rollengruppe aktiviert. Der Grund ist, dass die Verwaltungsrolle "RMS Decrypt" dieser Rollengruppe zugewiesen ist. Im Abschnitt [Weitere Informationen](#more-information) finden Sie ausführliche Informationen zur RMS-Entschlüsselung beim Exportieren von Suchergebnissen. 
  
Das Exportieren der Ergebnisse einer Inhaltssuche umfasst das Vorbereiten der Ergebnisse und das anschließende herunterladen auf einen lokalen Computer.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um Suchergebnisse zu exportieren, muss Ihnen die Rolle Exportverwaltung im Office 365 Security &amp; Compliance Center zugewiesen sein. Diese Rolle wird der integrierten eDiscovery-Manager-Rollengruppe zugewiesen. Sie wird der Rollengruppe Organisationsverwaltung nicht standardmäßig zugewiesen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 &amp; Security Compliance Center](assign-ediscovery-permissions.md).
    
- Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:


    
  - 32- oder 64-Bit-Versionen von Windows 7 und höher
    
  - Microsoft .NET Framework 4,7
    
  - Einen unterstützten Browser:
    
     - Microsoft Edge
    
        ODER
    
     - Microsoft Internet Explorer 10 und höhere Versionen
    
    **Hinweis:** Microsoft stellt keine Drittanbietererweiterungen oder Add-ons für ClickOnce-Anwendungen her. Das Exportieren von Suchergebnissen mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder Add-ons wird nicht unterstützt. 
    
- Wenn Sie Suchergebnisse herunterladen (beschrieben in Schritt 2), können Sie die Downloadgeschwindigkeit verlängern, indem Sie auf dem Computer, den Sie zum Exportieren der Suchergebnisse verwenden, eine Windows-Registrierungseinstellung konfigurieren. Weitere Informationen finden Sie unter [höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
    
- Wenn Sie Suchergebnisse exportieren, werden die Daten vorübergehend an einem eindeutigen Microsoft Azure-Speicherort in der Microsoft-Cloud gespeichert, bevor Sie auf Ihren lokalen Computer heruntergeladen werden. stellen sie sicher, dass ihre organisation eine verbindung mit dem endpunkt in Azure herstellen kann, nämlich ** \*. blob.core.windows.net** (der platzhalter stellt einen eindeutigen bezeichner für den export dar). Die Suchergebnis Daten werden zwei Wochen nach der Erstellung vom Azure-Speicherort gelöscht. 
    
- Wenn Ihre Organisation einen Proxy Server für die Kommunikation mit dem Internet verwendet, müssen Sie die Proxyservereinstellungen auf dem Computer definieren, den Sie zum Exportieren der Suchergebnisse verwenden (damit das Export Tool von Ihrem Proxy Server authentifiziert werden kann). Öffnen Sie dazu die Datei *Machine. config* an dem Speicherort, der mit Ihrer Windows-Version übereinstimmt. 
    
  - **32-Bit** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
    
  - **64-Bit** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
    
    Fügen Sie die folgenden Zeilen der Datei *Machine. config* zwischen den `<configuration>` Tags und `</configuration>` hinzu. Stellen Sie sicher, `ProxyServer` dass `Port` Sie und die richtigen Werte für Ihre Organisation ersetzen. Beispiel: `proxy01.contoso.com:80` . 
    
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
    
## <a name="step-1-prepare-search-results-for-export"></a>Schritt 1: Vorbereiten der Suchergebnisse für Export

Der erste Schritt besteht darin, die Suchergebnisse für den Export vorzubereiten. Wenn Sie Ergebnisse vorbereiten, werden Sie an einen Azure-Speicherort in der Microsoft-Cloud hochgeladen. Beachten Sie, dass Inhalte von Postfächern und Websites mit einer maximalen Rate von 2 GB pro Stunde hochgeladen werden.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
4. Wählen Sie auf der Seite **Inhaltssuche** eine Suche aus. 
    
5. Klicken Sie im Detailbereich unter **Ergebnisse auf einem Computer exportieren** auf **Export starten**. 
    
    > [!NOTE]
    > Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren. Brechen Sie in diesem Fall den Export ab, klicken Sie im Detailbereich für die ausgewählte Suche auf **Suchergebnisse aktualisieren** und starten Sie dann den Export erneut, nachdem die Ergebnisse aktualisiert wurden.  
  
6. Wählen Sie auf der Seite **Suchergebnisse exportieren** unter **Ausgabeoptionen**eine der folgenden Optionen aus:
    
    - Alle Elemente, ausgenommen solche, die unbekanntes Format aufweisen, werden verschlüsselt oder aus anderen Gründen nicht indiziert.
    
    - Alle Elemente, einschließlich derjenigen, die unbekanntes Format aufweisen, werden verschlüsselt oder aus anderen Gründen nicht indiziert.
    
    - Nur Elemente, die ein unbekanntes Format aufweisen, verschlüsselt oder aus anderen Gründen nicht indiziert wurden
    
    Im Abschnitt [Weitere Informationen](#more-information) finden Sie eine Beschreibung dazu, wie teilweise indizierte Elemente exportiert werden. Weitere Informationen zu teilweise indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche](partially-indexed-items-in-content-search.md).
    
7. Wählen Sie unter **Exchange-Inhalt exportieren als**eine der folgenden Optionen aus:
    
    - **Eine PST-Datei für jedes Postfach** – exportiert eine PST-Datei für jedes Benutzerpostfach, das Suchergebnisse enthält. Alle Ergebnisse aus dem Archivpostfach des Benutzers sind in derselben PST-Datei enthalten. Beachten Sie, dass mit dieser Option die Postfachordnerstruktur aus dem Quellpostfach wiederhergestellt wird. 
    
    - **Eine PST-Datei mit allen Nachrichten** -exportiert eine einzelne PST-Datei (mit dem Namen *Exchange. PST* ), die die Suchergebnisse aus allen in der Suche enthaltenen Quellpostfächern enthält. Beachten Sie, dass mit dieser Option die Postfachordnerstruktur für jede Nachricht wiedergegeben wird. 
    
    - **Eine PST-Datei, die alle Nachrichten in einem einzelnen Ordner enthält** – exportiert Suchergebnisse in eine einzelne PST-Datei, in der sich alle Nachrichten in einem einzelnen Ordner auf oberster Ebene befinden. Mit dieser Option können Prüfer Elemente in chronologischer Reihenfolge überarbeiten (Elemente werden nach gesendetem Datum sortiert), ohne dass Sie in der ursprünglichen Postfachordnerstruktur für jedes Element navigieren müssen. 
    
    - **Einzelne Nachrichten** -exportiert Suchergebnisse als einzelne e-Mail-Nachrichten im MSG-Format. Wenn Sie diese Option auswählen, werden die e-Mail-Suchergebnisse in einen Ordner im Dateisystem exportiert. Der Ordnerpfad für einzelne Nachrichten ist derselbe wie beim Exportieren der Ergebnisse in PST-Dateien. 
    
      > [!IMPORTANT]
      > Um RMS-verschlüsselte Nachrichten beim Exportieren zu entschlüsseln, müssen Sie die e-Mail-Suchergebnisse als einzelne Nachrichten exportieren. VerSchlüsselte Nachrichten bleiben verschlüsselt, wenn Sie die Suchergebnisse als PST-Datei exportieren. 
  
8. Klicken Sie auf das Kontrollkästchen Deduplizierung **aktivieren** , um doppelte Nachrichten auszuschließen. Diese Option wird nur angezeigt, wenn die Inhaltsquellen der Suche Exchange-Postfächer oder öffentliche Ordner enthalten. 
    
    Wenn Sie diese Option auswählen, wird nur eine Kopie einer Nachricht exportiert, auch wenn mehrere Kopien derselben Nachricht in den durchsuchten Postfächern gefunden wurden. Der Exportergebnis Bericht (results. CSV) enthält eine Zeile für jede Kopie einer doppelten Nachricht, sodass Sie die Postfächer (oder öffentliche Ordner) identifizieren können, die eine Kopie der doppelten Nachricht enthalten. Weitere Informationen zur Deduplizierung und zur Identifizierung doppelter Elemente finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md).
    
9. Aktivieren Sie das Kontrollkästchen **Versionen für SharePoint-Dokumente einbeziehen** , um alle Versionen von SharePoint-Dokumenten zu exportieren. Diese Option wird nur angezeigt, wenn die Inhaltsquellen der Suche SharePoint oder OneDrive for Business-Websites enthalten. 
    
10. Aktivieren Sie das Kontrollkästchen **Dateien in einem komprimierten Ordner exportieren (gezippt)** , um Suchergebnisse in komprimierte Ordner zu exportieren. Diese Option ist nur verfügbar, wenn Sie Exchange-Elemente als einzelne Nachrichten exportieren und wenn die Suchergebnisse SharePoint-oder OneDrive-Dokumente sind. Diese Option wird hauptsächlich verwendet, um den 260-Zeichen Grenzwert in Windows-Datei Pfad Namen zu umgehen, wenn Elemente exportiert werden. Siehe "Dateinamen der exportierten Elemente" im Abschnitt [Weitere Informationen](#more-information) . 
    
11. Klicken Sie auf **Export starten**.
    
    Die Suchergebnisse werden zum Herunterladen vorbereitet, d. h., Sie werden an den Azure-Speicherort in der Microsoft-Cloud hochgeladen. Wenn die Suchergebnisse zum Herunterladen bereit sind, wird der Link zum **Herunterladen von exportierten Ergebnissen** unter **Ergebnisse auf einem Computer exportieren** im Detailbereich angezeigt. 
  
## <a name="step-2-download-the-search-results"></a>Schritt 2: Herunterladen der Suchergebnisse

Im nächsten Schritt werden die Suchergebnisse vom Azure-Speicherort auf Ihren lokalen Computer heruntergeladen.
  
Wie bereits erläutert, können Sie die Downloadgeschwindigkeit verlängern, indem Sie auf dem Computer, den Sie zum Exportieren der Suchergebnisse verwenden, eine Windows-Registrierungseinstellung konfigurieren. Weitere Informationen finden Sie unter [höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Klicken Sie im Detailbereich für die Suche, für die Sie den Export gestartet haben, unter **Ergebnisse auf Computer exportieren**auf **exportierte Ergebnisse herunterladen**.
    
    Das Fenster **exportierte Ergebnisse herunterladen** wird angezeigt und enthält die folgenden Informationen zu den Suchergebnissen, die auf Ihren Computer heruntergeladen werden. 
    
    - Die Anzahl der Elemente, die heruntergeladen werden.
    
    - Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.
    
    - Ob indiziert oder nicht indiziert wird exportiert. Nicht indizierte Elemente sind Elemente, die ein erkanntes Format aufweisen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden. Weitere Informationen finden Sie unter [unindizierte Elemente in der Inhaltssuche](partially-indexed-items-in-content-search.md).
    
    - Gibt an, ob Versionen von SharePoint-Dokumenten heruntergeladen werden.
    
    - Der Status des Export Vorbereitungs Vorgangs. Sie können mit dem Herunterladen von Suchergebnissen beginnen, auch wenn die Vorbereitung der Daten nicht abgeschlossen ist.
    
2. Klicken Sie unter **Schlüssel exportieren**auf **in Zwischenablage kopieren**. Sie verwenden diesen Schlüssel in Schritt 5, um die Suchergebnisse herunterzuladen.
    
    > [!NOTE]
    > Da jeder das eDiscovery-Export Tool installieren und starten und dann diesen Schlüssel zum Herunterladen der Suchergebnisse verwenden kann, müssen Sie Vorkehrungen treffen, um diesen Schlüssel genau so zu schützen, als würden Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen. 
  
3. Klicken Sie auf **Ergebnisse herunterladen**.
    
4. Wenn Sie aufgefordert werden, das **microsoft office 365 eDiscovery-Export Tool**zu installieren, klicken Sie auf **Installieren**.
    
5. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.
    
6. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese-und Schreibvorgänge) sollten Sie die Suchergebnisse auf ein lokales Laufwerk herunterladen. Laden Sie Sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
1. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Export Tool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und der Größe) der verbleibenden zu ladenden Elemente. Nach Abschluss des Exportvorgangs können Sie auf die Dateien am Speicherort zugreifen, an dem Sie heruntergeladen wurden. 
    

  
## <a name="more-information"></a>Weitere Informationen

Hier finden Sie weitere Informationen zum Exportieren von Suchergebnissen.
  
[Exportgrenzwerte](#export-limits)
  
[Berichte exportieren](#export-reports)
  
[Exportieren teilweise indizierter Elemente](#exporting-partially-indexed-items)

[Exportieren einzelner Nachrichten oder PST-Dateien](#exporting-individual-messages-or-pst-files)
  
[EntSchlüsseln von RMS-verschlüsselten Nachrichten](#decrypting-rms-encrypted-messages)

[Dateinamen der exportierten Elemente](#filenames-of-exported-items)  
  
[Verschiedenes](#miscellaneous)
  
 ### <a name="export-limits"></a>Exportgrenzwerte
  
- Beim Exportieren von Suchergebnissen aus &amp; dem Security Compliance Center gelten die folgenden Grenzwerte:
    
  - Sie können maximal 2 TB Daten aus einer einzelnen Inhaltssuche exportieren. Wenn die Suchergebnisse größer als 2 TB sind, erwägen Sie die Verwendung von Datumsbereichen oder anderen Filtertypen, um die Gesamtgröße der Suchergebnisse zu verringern.
    
  - Ihre Organisation kann maximal 2 TB Daten an einem Tag exportieren.
    
  - Sie können maximal 10 Exporte gleichzeitig in Ihrer Organisation ausführen.
    
  - Ein einzelner Benutzer kann maximal drei Exporte gleichzeitig ausführen.

  > [!NOTE]
  > Das Exportieren der Berichte aus einer Inhaltssuche gilt auch für die Anzahl der gleichzeitig ausgeführten Exporte und die Anzahl der Exporte, die ein einzelner Benutzer ausführen kann.
    
- Wie bereits erwähnt, werden Suchergebnisse von Postfächern und Websites an den Azure-Speicherort hochgeladen (wie in [Schritt 1: Vorbereiten der Suchergebnisse für den Export](#step-1-prepare-search-results-for-export)beschrieben) mit einer maximalen Rate von 2 GB pro Stunde.
    
- Die maximale Größe einer PST-Datei, die exportiert werden kann, ist standardmäßig 10 GB. Das Ergebnis ist, dass die Suchergebnisse für das Postfach in zwei (oder mehr) separaten PST-Dateien exportiert werden, wenn die Suchergebnisse aus dem Postfach eines Benutzers größer als 10 GB sind. Wenn Sie außerdem alle Suchergebnisse in einer einzelnen PST-Datei exportieren möchten, wird die PST-Datei in zusätzliche PST-Dateien aufgeteilt, wenn die Gesamtgröße der Suchergebnisse größer als 10 GB ist. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, den Sie zum Exportieren der Suchergebnisse verwenden. Weitere Informationen finden Sie unter [Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen](change-the-size-of-pst-files-when-exporting-results.md).
    
    Darüber hinaus werden die Suchergebnisse eines bestimmten Postfachs nicht unter mehrere PST-Dateien aufgeteilt, es sei denn, der Inhalt eines einzelnen Postfachs beträgt mehr als 10 GB. Wenn Sie die Suchergebnisse in eine PST-Datei exportieren möchten, für die alle Nachrichten in einem einzelnen Ordner enthalten sind und die Suchergebnisse größer als 10 GB sind, werden die Elemente immer noch in chronologischer Reihenfolge organisiert, sodass Sie in zusätzliche PST-Dateien basierend auf dem gesendeten d aß.
     
 ### <a name="export-reports"></a>Berichte exportieren
  
- Wenn Sie Suchergebnisse exportieren, werden zusätzlich zu den Suchergebnissen die folgenden Berichte hinzugefügt.
    
  - **Zusammenfassung exportieren** Ein Excel-Dokument, das eine Zusammenfassung des Exports enthält. Hierzu gehören Informationen wie die Anzahl der durchsuchten Inhaltsquellen, die geschätzten und heruntergeladenen Größen der Suchergebnisse sowie die geschätzte und heruntergeladene Anzahl von Elementen, die exportiert wurden. 
    
  - **Manifest** Eine Manifestdatei (im XML-Format), die Informationen zu jedem in den Suchergebnissen enthaltenen Element enthält. 
    
  - **Ergebnisse** Ein Excel-Dokument, das Informationen zu jedem Element enthält, das als Suchergebnis heruntergeladen wird. Für e-Mails enthält das Ergebnisprotokoll Informationen zu den einzelnen Nachrichten, einschließlich: 
    
      - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
        
      - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
        
      - Die Betreffzeile der Nachricht.
        
      - Absender und Empfänger der Nachricht.
        
      - Gibt an, ob es sich bei der Nachricht um eine doppelte Nachricht handelt, wenn Sie beim Exportieren der Suchergebnisse die Option Deduplizierung aktiviert haben. Doppelte Nachrichten haben einen Wert in der Spalte **Duplicate to Item** , der die Nachricht als Duplikat identifiziert. Der Wert in der Spalte duplizieren in **Element** enthält die Element Identität der Nachricht, die exportiert wurde. Weitere Informationen finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md).
        
      Für Dokumente aus SharePoint und OneDrive for Business-Websites enthält das Ergebnisprotokoll Informationen zu jedem Dokument, einschließlich:
        
      - Die URL für das Dokument.
        
      - Die URL für die Websitesammlung, in der sich das Dokument befindet.
        
      - Das Datum, an dem das Dokument zuletzt geändert wurde.
        
      - Der Name des Dokuments (das sich in der Spalte Betreff im Ergebnisprotokoll befindet).
    
  - Nicht **indizierte Elemente** Ein Excel-Dokument mit Informationen zu teilweise indizierten Elementen, die in die Suchergebnisse eingeschlossen werden würden. Wenn Sie beim Generieren des Suchergebnis Berichts keine Teil indizierten Elemente hinzufügen, wird der Bericht weiterhin heruntergeladen, ist jedoch leer. 
    
  - **Fehler und Warnungen** Enthält Fehler und Warnungen für Dateien, die während des Exports gefunden wurden. Informationen zu den einzelnen Fehlern oder Warnungen finden Sie in der Spalte Fehler Details. 
    
  - **ÜbersprungEne Elemente** Wenn Sie Suchergebnisse aus SharePoint-und OneDrive für Business-Websites exportieren, enthält der Export in der Regel einen Bericht mit übersprungenen Elementen (SkippedItems. CSV). Bei den in diesem Bericht zitierten Elementen handelt es sich in der Regel um Elemente, die nicht heruntergeladen werden, beispielsweise einen Ordner oder eine Dokumentenmappe. Dieser Elementtyp wird nicht exportiert. Für andere Elemente, die übersprungen wurden, zeigt das Feld "Fehlertyp" und "Fehler Details" im Bericht "übersprungene Elemente" den Grund, warum das Element übersprungen wurde und nicht mit anderen Suchergebnissen heruntergeladen wurde. 
    
  - **Ablaufverfolgungsprotokoll** Enthält detaillierte Protokollierungsinformationen zum Exportvorgang und kann beim Exportprobleme entdecken. 
    
    > [!NOTE]
    > Sie können diese Dokumente nur exportieren, ohne die tatsächlichen Suchergebnisse exportieren zu müssen. Weitere Informationen finden Sie unter [Exportieren eines Inhalts Suchberichts](export-a-content-search-report.md). 
  
 ### <a name="exporting-partially-indexed-items"></a>Exportieren teilweise indizierter Elemente
  
- Wenn Sie Postfachelemente aus einer Inhaltssuche exportieren, die alle Postfachelemente in den Suchergebnissen zurückgibt (da keine Schlüsselwörter in der Suchabfrage enthalten sind), werden teilweise indizierte Elemente nicht in die PST-Datei kopiert, die die nicht indizierten Elemente enthält. Der Grund dafür ist, dass alle Elemente, einschließlich aller teilweise indizierten Elemente, automatisch in die regulären Suchergebnisse eingeschlossen werden. Dies heißt, dass teilweise indizierte Elemente in einer PST-Datei (oder als einzelne Nachrichten) enthalten sind, die die anderen, indizierten Elemente enthält.
    
    Wenn Sie sowohl die indizierten als auch teilweise indizierten Elemente exportieren oder nur die indizierten Elemente aus einer Inhaltssuche exportieren, die alle Elemente zurückgibt, wird die gleiche Anzahl von Elementen heruntergeladen. Dies geschieht auch dann, wenn die geschätzten Suchergebnisse für die Inhaltssuche (in der Suchstatistik im &amp; Security Compliance Center angezeigt) weiterhin eine separate Schätzung für die Anzahl der teilweise indizierten Elemente aufweisen. Nehmen wir beispielsweise an, dass die Schätzung für eine Suche, die alle Elemente (keine Schlüsselwörter in der Suchabfrage) enthält, zeigt, dass 1.000 Elemente gefunden wurden und 200 teilweise indizierte Elemente ebenfalls gefunden wurden. In diesem Fall schließen die 1.000-Elemente die teilweise indizierten Elemente ein, da die Suche alle Elemente zurückgibt. Anders ausgedrückt gibt es 1.000 Gesamtelemente, die von der Suche zurückgegeben werden, und nicht 1.200 Elemente (wie Sie vielleicht erwarten). Wenn Sie die Ergebnisse dieser Suche exportieren und indizierte und teilweise indizierte Elemente (oder nur indizierte Elemente) exportieren möchten, werden 1.000-Elemente heruntergeladen. Auch dies liegt daran, dass teilweise indizierte Elemente in den regulären (indizierten) Ergebnissen enthalten sind, wenn Sie eine leere Suchabfrage verwenden, um alle Elemente zurückzugeben. Wenn Sie in diesem Beispiel nur teilweise indizierte Elemente exportieren möchten, würden nur die 200 nicht indizierten Elemente heruntergeladen.
    
    Beachten Sie, dass im vorherigen Beispiel (wenn Sie indizierte und teilweise indizierte Elemente exportieren oder nur indizierte Elemente exportieren) der **Export Zusammenfassungs** Bericht, der in den exportierten Suchergebnissen enthalten ist, Listen 1.000 Elemente geschätzte elemente und 1.000 heruntergeladen Elemente aus denselben Gründen wie zuvor beschrieben. 
    
- Wenn die Suche, aus der Sie Ergebnisse exportieren, eine Suche nach bestimmten Inhaltsspeicherorten oder allen Inhaltsspeicherorten in Ihrer Organisation war, werden nur die teilweise Elemente aus Inhaltsspeicherorten exportiert, die Elemente enthalten, die den Suchkriterien entsprechen. Anders ausgedrückt: Wenn in einem Postfach oder einer Website keine Suchergebnisse gefunden werden, werden teilweise indizierte Elemente in diesem Postfach oder in der Website nicht exportiert. Der Grund dafür ist, dass das Exportieren teilweise indizierter Elemente aus vielen Standorten in der Organisation möglicherweise die Wahrscheinlichkeit von Exportfehlern erhöht und die Zeitdauer erhöht, die zum Exportieren und Herunterladen der Suchergebnisse benötigt wird.
    
    Wenn Sie teilweise indizierte Elemente aus allen Inhaltsspeicherorten für eine Suche exportieren möchten, konfigurieren Sie die Suche so, dass alle Elemente (durch Entfernen von Schlüsselwörtern aus der Suchabfrage) zurückgegeben werden, und exportieren Sie dann nur teilweise indizierte Elemente, wenn Sie die Suchergebnisse exportieren.
    
    ![Verwenden der dritten-Exportoption zum Exportieren nur nicht indizierter Elemente](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- Beim Exportieren von Suchergebnissen aus SharePoint-oder OneDrive für Business-Websites hängt die Möglichkeit zum Exportieren von nicht indizierten Elementen auch von der ausgewählten Exportoption ab, und ob eine gesuchte Website ein indiziertes Element enthält, das den Suchkriterien entspricht. Wenn Sie beispielsweise bestimmte SharePoint-oder OneDrive für Unternehmen-Websites durchsuchen und keine Suchergebnisse gefunden werden, werden keine nicht indizierten Elemente dieser Websites exportiert, wenn Sie die zweite Exportoption zum Exportieren von indizierten und nicht indizierten Elementen auswählen. Wenn ein indiziertes Element von einer Website mit den Suchkriterien übereinstimmt, werden alle nicht indizierten Elemente dieser Website exportiert, wenn sowohl indizierte als auch unindizierte Elemente exportieren. In der folgenden Abbildung werden die Exportoptionen beschrieben, die davon ausgehen, ob eine Website ein indiziertes Element enthält, das den Suchkriterien entspricht.
    
    ![Wählen Sie die Option Exportieren basierend darauf aus, ob eine Website ein indiziertes Element enthält, das den Suchkriterien entspricht.](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    A – nur indizierte Elemente, die den Suchkriterien entsprechen, werden exportiert. Es werden keine teilweise indizierten Elemente exportiert.
    
    B-Wenn keine indizierten Elemente einer Website den Suchkriterien entsprechen, werden teilweise indizierte Elemente aus derselben Website nicht exportiert. Wenn indizierte Elemente aus einer Website in den Suchergebnissen zurückgegeben werden, werden die teilweise indizierten Elemente dieser Website exportiert. Anders ausgedrückt, werden nur die teilweise indizierten Elemente aus Websites exportiert, die Elemente enthalten, die den Suchkriterien entsprechen.
    
    C – alle teilweise indizierten Elemente aus allen Websites in der Suche werden exportiert, unabhängig davon, ob eine Websiteelemente enthält, die den Suchkriterien entsprechen.
    
    Wenn Sie teilweise indizierte Elemente exportieren möchten, werden teilweise indizierte Postfachelemente in eine separate PST-Datei exportiert, unabhängig von der Option, die Sie unter **Exchange-Inhalte exportieren als**auswählen.

- Wenn in den Suchergebnissen teilweise indizierte Elemente zurückgegeben werden (da andere Eigenschaften einer teilweise indizierten Elemente mit den Suchkriterien übereinstimmen), werden diese teilweise indiziert und mit den regulären Suchergebnissen exportiert. Wenn Sie also sowohl indizierte Elemente als auch teilweise indizierte Elemente exportieren möchten (indem Sie **alle Elemente auswählen, einschließlich derer, die nicht erkannt wurden, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden** ), werden die teilweise indizierten Elemente exportiert. die regulären Ergebnisse werden im Bericht results. CSV aufgeführt. Sie werden nicht im Bericht "nicht indizierte Elemente. csv" aufgelistet.
    
 ### <a name="exporting-individual-messages-or-pst-files"></a>Exportieren einzelner Nachrichten oder PST-Dateien
  
- Wenn der Dateiname einer Nachricht den maximalen Zeichen Grenzwert für Windows überschreitet, wird der Dateipfad abgeschnitten. Der ursprüngliche Dateiname wird jedoch im Manifest und in ResultsLog aufgelistet.
    
- Wie bereits erläutert, werden e-Mail-Suchergebnisse in einen Ordner im Dateisystem exportiert. Der Ordnerpfad für einzelne Nachrichten würde den Ordnerpfad im Postfach des Benutzers replizieren. Beispielsweise würde für eine Suche mit dem Namen "ContosoCase101" Nachrichten im Posteingang eines Benutzers im Ordnerpfad `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`befinden. 
    
- Wenn Sie e-Mail-Nachrichten in einer PST-Datei mit allen Nachrichten in einem einzelnen Ordner exportieren möchten, sind ein Ordner " **Gelöschte Elemente** " und ein Ordner " **Suchordner** " auf der obersten Ebene des PST-Ordners enthalten. Diese Ordner sind leer. 
  
 ### <a name="decrypting-rms-encrypted-messages"></a>EntSchlüsseln von RMS-verschlüsselten Nachrichten
  
- Wie bereits erläutert, müssen Sie die Suchergebnisse als einzelne Nachrichten exportieren, um RMS-verschlüsselte Nachrichten beim Exportieren zu entschlüsseln. Wenn Sie Suchergebnisse in eine PST-Datei exportieren, bleiben RMS-verschlüsselte Nachrichten verschlüsselt.
    
- Bei der RMS-Entschlüsselungsfunktion in der Inhaltssuche werden Nachrichten, die mit Office 365-Nachrichtenverschlüsselung (OM) verschlüsselt sind, beim Exportieren von Suchergebnissen nicht entschlüsselt. Wenn jedoch eine mit OM verschlüsselte Nachricht von einem Benutzer in Ihrer Organisation gesendet wird, wird die Kopie der Nachricht im gesendeten Ordner des Benutzers nicht verschlüsselt und kann nach dem Exportieren angezeigt werden. Wenn Nachrichten, die mit OM verschlüsselt wurden, jedoch von Benutzern in Ihrer Organisation empfangen werden, werden Sie nicht entschlüsselt, nachdem Sie exportiert wurden. Weitere Informationen zu OM finden Sie unter [Office 365-Nachrichtenverschlüsselung](https://go.microsoft.com/fwlink/p/?linkid=844966).
    
- Nachrichten, die entschlüsselt werden, werden im **ResultsLog** -Bericht identifiziert. Dieser Bericht enthält eine Spalte mit dem Namen **Decode Status**, und der **** Wert decodiert in dieser Spalte identifiziert die Nachrichten, die entschlüsselt wurden. 
    
- Derzeit enthält diese Entschlüsselungsfunktion keine verschlüsselten Inhalte aus SharePoint-und OneDrive für Business-Websites. Nur RMS-verschlüsselte e-Mail-Nachrichten werden entschlüsselt, wenn Sie Sie exportieren.
    
- Wenn eine RMS-verschlüsselte e-Mail-Nachricht eine Anlage hat (beispielsweise ein Dokument oder eine andere e-Mail-Nachricht), die ebenfalls verschlüsselt ist, wird nur die e-Mail-Nachricht der obersten Ebene entschlüsselt.
    
- Sie können keine Vorschau einer RMS-verschlüsselten e-Mail-Nachricht anzeigen. Um eine verschlüsselte Nachricht anzuzeigen, müssen Sie Sie exportieren.
    
- Wenn Sie verhindern möchten, dass eine Person RMS-verschlüsselte Nachrichten entschlüsselt, müssen Sie eine benutzerdefinierte Rollengruppe erstellen (indem Sie die integrierte eDiscovery-Manager-Rollengruppe kopieren) und dann die Verwaltungsrolle RMS Decrypt aus der benutzerdefinierten Rollengruppe entfernen. Fügen Sie dann die Person, die Sie nicht möchten, Nachrichten als Mitglied der benutzerdefinierten Rollengruppe zu entschlüsseln.
  
 ### <a name="filenames-of-exported-items"></a>Dateinamen der exportierten Elemente
  
- Der vollständige Pfadname für e-Mail-Nachrichten und Website Dokumente, die auf Ihren lokalen Computer exportiert werden, besteht aus einem Grenzwert von 260 Zeichen (vom Betriebssystem auferlegt). Der vollständige Pfadname für exportierte Elemente enthält den ursprünglichen Speicherort des Elements und den Ordnerspeicherort auf dem lokalen Computer, in den die Suchergebnisse heruntergeladen werden. Wenn Sie beispielsweise angeben, dass die Suchergebnisse `C:\Users\Admin\Desktop\SearchResults` in das EDiscovery-Export Tool heruntergeladen werden `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`sollen, wäre der vollständige Pfadname für ein heruntergeladenes e-Mail-Element.
    
    Wenn der Grenzwert von 260 Zeichen überschritten wird, wird der vollständige Pfadname für ein Element abgeschnitten.
    
  - Wenn der vollständige Pfadname länger als 260 Zeichen ist, wird der Dateiname gekürzt, um die Grenze zu erreichen. Beachten Sie, dass der gekürzte Dateiname (ohne die Dateierweiterung) nicht kleiner als 8 Zeichen sein darf.
    
  - Wenn der vollständige Pfadname nach der Kürzung des Datei namens noch zu lang ist, wird das Element von seinem aktuellen Speicherort in den übergeordneten Ordner verschoben. Wenn der Pfadname noch zu lang ist, wird der Vorgang wiederholt: kürzen Sie den Dateinamen, und verschieben Sie bei Bedarf erneut zu dem übergeordneten Ordner. Dieser Vorgang wird wiederholt, bis sich der vollständige Pfadname unter dem Grenzwert von 260 Zeichen befindet.
    
  - Wenn bereits ein gekürzter vollständiger Pfadname vorhanden ist, wird eine Versionsnummer am Ende des Datei namens hinzugefügt. Beispiel: `statusmessage(2).msg`.
    
    Um dieses Problem zu vermeiden, sollten Sie die Suchergebnisse an einen Speicherort mit einem kurzen Pfadnamen herunterladen. beispielsweise `C:\Results` würde das Herunterladen von Suchergebnissen in einen Ordner mit dem Namen weniger Zeichen zu den Pfadnamen der exportierten Elemente hinzufügen, `C:\Users\Admin\Desktop\Results`als Sie in einen Ordner mit dem Namen herunterzuladen.
    
- Beim Exportieren von Website Dokumenten kann auch der ursprüngliche Dateiname eines Dokuments geändert werden. Dies geschieht speziell für Dokumente, die von einer SharePoint-oder OneDrive for Business-Website gelöscht wurden, die in den Wartebereich gestellt wurde. Nachdem ein Dokument, das sich auf einer Warteposition befindet, gelöscht wird, wird das gelöschte Dokument automatisch in die Bibliothek für die Aufbewahrungszeit für die Website verschoben (die beim Anhalten der Website erstellt wurde). Wenn das gelöschte Dokument in die Bibliothek zur Aufbewahrungszeit verschoben wird, wird eine zufällig generierte und eindeutige ID an den ursprünglichen Dateinamen des Dokuments angehängt. Wenn beispielsweise der Dateiname für ein Dokument lautet `FY2017Budget.xlsx` und dieses Dokument später gelöscht und in die Bibliothek für die Aufbewahrungsdauer verschoben wird, wird der Dateiname des Dokuments, das in die Bibliothek für die Aufbewahrungszeit verschoben `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`wird, in ungefähr geändert. Wenn ein Dokument in der Bibliothek zur Aufbewahrungsdauer mit der Abfrage einer Inhaltssuche übereinstimmt und Sie die Ergebnisse dieser Suche exportieren, weist die exportierte Datei den geänderten Dateiname auf. in diesem Beispiel wäre der Dateiname des exportierten Dokuments `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.
    
    Wenn ein Dokument auf einer Warte Website geändert wird (und die Versionsverwaltung für die Dokumentbibliothek auf der Website aktiviert wurde), wird darüber hinaus automatisch eine Kopie der Datei in der Bibliothek für die Aufbewahrungszeit erstellt. In diesem Fall wird auch eine zufällig generierte und eindeutige ID an den Dateinamen des Dokuments angehängt, das in die Bibliothek zur Konservierungs Aufbewahrung kopiert wurde.
    
    Der Grund, warum Dateinamen von Dokumenten, die in die Bibliothek für die Konservierungs Aufbewahrung verschoben oder kopiert werden, ist, Konflikt verursachende Dateinamen zu verhindern. Weitere Informationen zum Aufbewahren von Websites und zur Aufbewahrungs Bibliothek finden Sie unter Übersicht über den [in-situ-Speicher in SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).
    
 ### <a name="miscellaneous"></a>Verschiedenes
  
- Alle Suchergebnisse und die Export Berichte sind in einem Ordner mit dem gleichen Namen wie die Inhaltssuche enthalten. Die e-Mail-Nachrichten, die exportiert wurden, befinden sich in einem Ordner mit dem Namen **Exchange**. Dokumente befinden sich in einem Ordner mit dem Namen **SharePoint**. 
    
- Die Dateisystemmetadaten für Dokumente in SharePoint und OneDrive for Business-Websites werden beibehalten, wenn Dokumente auf Ihren lokalen Computer exportiert werden. Das führt dazu, dass Dokumenteigenschaften wie Erstellungs-und Datum der letzten Änderung beim Exportieren von Dokumenten nicht geändert werden.

- Wenn Ihre Suchergebnisse ein Listenelement aus SharePoint aufweisen, das mit der Suchabfrage übereinstimmt, werden alle Zeilen in der Liste zusätzlich zu dem Element exportiert, das mit der Suchabfrage übereinstimmt. Hierzu gehören alle Anlagen in der Liste. Der Grund dafür ist, einen Kontext für Listenelemente bereitzustellen, die in den Suchergebnissen zurückgegeben werden. Beachten Sie, dass sich die Anzahl der exportierten Elemente möglicherweise von den zusätzlichen Listenelementen und Anlagen unterscheidet, als die ursprüngliche Schätzung der Suchergebnisse.

---
title: Verwenden Sie das Tool PST-Auflistung zu suchen, kopieren und Löschen von PST-Dateien in Ihrer Organisation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Verwenden Sie das Microsoft PST-Auflistung-Tool zum Suchen des Netzwerks Ihrer Organisation, um eine Inventur der PST-Dateien abrufen, die in der gesamten Organisation verteilt sind. Wenn Sie PST-Dateien gefunden haben, können Sie die PST-Auflistung Tool verwenden, um zu kopieren Sie sie an einem zentralen Ort aus, damit Sie sie in Office 365 importieren können.
ms.openlocfilehash: 0537a65a32fa25704045bd587cb20f9eee13f628
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038128"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>Verwenden Sie das Tool PST-Auflistung zu suchen, kopieren und Löschen von PST-Dateien in Ihrer Organisation

Das Tool Microsoft PST-Auflistung können Sie Suchen des Netzwerks Ihrer Organisation für PST-Dateien. Das Tool können Sie eine Inventur der PST-Dateien abrufen, die in der gesamten Organisation verteilt sind. Wenn Sie PST-Dateien gefunden haben, können Sie das Tool PST-Auflistung verwenden, an einem zentralen Speicherort kopieren. Müssen PST-Dateien an einem Ort ein, und klicken Sie dann ermöglicht es Ihnen, sie zu Exchange Online-Postfächer (oder ein einzelnes Exchange Online-Postfach) zu importieren, klicken Sie dann den umfassenden Satz von Compliance-Funktionen in Office 365 angewendet werden kann. Dies umfasst das Importieren von PST-Dateien Benutzer archivieren Sie die Postfächer, Suchen nach bestimmten Nachrichten in die PST-Dateien, die Sie importiert haben mithilfe von Suchtools eDiscovery, Beibehaltung von Nachrichten mithilfe von eDiscovery-Archive und Aufbewahrungsrichtlinien für Office 365 und Verwalten von während der Lebensdauer Diese Nachrichten mit der messaging-Zyklus zeichnet auf Management-Features in Exchange Online. Nachdem Sie davon überzeugt sind, dass die PST-Dateien, die Sie gesammelt zu Office 365 erfolgreich importiert wurden, können Sie das Tool verwenden, um sie von ihrem ursprünglichen Speicherort in Ihrem Netzwerk zu löschen. 
  
Haben Sie mit dem Tool PST-Auflistung ist verhindern, dass Benutzer neue PST-Dateien erstellen und Ändern von vorhandenen PST-Dateien, die Sie in Ihrem Netzwerk zu finden. Diese Funktionen "Block" können Sie suchen, zu sammeln, und importieren Sie eine bekannte Gruppe von PST-Dateien in Office 365 und zu verhindern, dass die zukünftige Verbreitung von PST-Dateien in Ihrer Organisation. 
  
## <a name="how-the-pst-collection-tool-works"></a>Funktionsweise des Tools PST-Auflistung

Nachfolgend finden Sie ein schnellen Überblick über den Prozess der Verwendung des Tools PST-Auflistung zum Suchen, steuern, erfassen und Löschen von PST-Dateien in Ihrer Organisation.
  
![Übersicht über den Prozess der PST-Auflistung-tool](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[Schritt 1: Hier finden Sie die PST-Dateien in Ihrem Netzwerk](#step-1-find-pst-files-on-your-network)** – Wenn Sie das Tool zum Suchen von PST-Dateien ausgeführt, Sie geben Sie einen Speicherort, wie etwa eine Organisationseinheit, die Active Directory-Objekte für die Client-und Server enthalten. Sie können auch bestimmte Computer oder Netzwerk-Dateifreigaben suchen. Wenn Sie das Tool ausführen, wird eine "lightweight" Auflistung-Agent auf den Zielcomputern installiert. Dieser Agent sucht den Zielcomputer für PST-Dateien und sendet dann wieder in das Tool PST-Auflistung zu einer beliebigen PST-Datei gefundenen Informationen. Das Tool erstellt Protokolldateien, die Informationen zu den PST-Dateien enthält, die an den angegebenen Speicherorten gefunden wurden. Diese Dateien werden beim Ausführen des Tools in den späteren Schritten verwendet. 
    
2. **[(Optional) Schritt2: Steuern des Zugriffs auf PST-Dateien](#optional-step-2-control-access-to-pst-files)** -das Tool wird ein Gruppenrichtlinienobjekt (GPO) mit Einstellungen, die verhindern, dass Benutzer erstellen oder Ändern von PST-Dateien erstellt. Diese GPO gilt für alle Benutzer in Ihrer Domäne. In diesem optionale Schritt können Sie die "Sperren" PST-Dateien, die in Schritt 1 gefunden wurden, sodass Sie sammeln, importieren und ohne neue erstellte PST-Dateien zu löschen oder die vorhandenen PST-Dateien geändert. 
    
3. **[Schritt 3: Kopieren Sie die PST-Dateien an einen Speicherort für die Auflistung](#step-3-copy-the-pst-files-to-a-collection-location)** – auf diese Weise können Sie die PST-Dateien an einem Ort sammeln, damit Sie sie mithilfe des Office 365 importieren-Diensts in Schritt 4 in Exchange Online-Postfächern importieren können. Wenn Sie das Tool im Modus "sammeln" ausführen, kopiert jeder Agent-Auflistung die PST-Dateien aus dem Zielcomputer aus, die, den an den Speicherort für die Auflistung der Agent installiert ist. 
    
4. **[Schritt 4: Importieren von PST-Dateien in Office 365](#step-4-import-the-pst-files-to-office-365)** -Nachdem Sie die PST-Dateien an einem Speicherort kopiert haben, sind Sie bereit, sie zu Exchange Online-Postfächer zu importieren. 
    
5. **[Schritt 5: löschen die PST-Dateien in Ihrem Netzwerk gefunden](#step-5-delete-the-pst-files-found-on-your-network)** – nach der PST-Dateien, dass gefunden und gesammelt wurden in Exchange Online-Postfächern in Office 365 importiert, können Sie das Tool PST-Auflistung verwenden, um die PST-Dateien aus den ursprünglichen Speicherorten zu löschen, in dem sie in Schritt 1 wurden gefunden. 

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Führen Sie die folgenden Schritte aus, um das Tool PST-Auflistung mit dem lokalen Computer herunterzuladen. 
    
    1. [Laden Sie das Tool PST-Auflistung](https://aka.ms/pstcollectiontool).
    
    2. Klicken Sie auf **Speichern** , klicken Sie im Popupfenster \> zum Speichern der PSTCollectionTool.zip-Datei in einen Ordner auf Ihrem lokalen Computer **Speichern** . 
    
    3. Extrahieren Sie die Datei PSTCollectionTool.zip in einen Ordner auf Ihrem lokalen Computer. der Name des Standardordners ist PSTCollectionTool.
    
- Wenn das Tool PST-Auflistung in einem beliebigen Modus (suchen, blockieren, kopieren oder löschen) ausgeführt werden soll, müssen Sie Mitglied der Gruppen Domänen-Admins in Active Directory-Domäne sein. 

## <a name="step-1-find-pst-files-on-your-network"></a>Schritt 1: Hier finden Sie die PST-Dateien in Ihrem Netzwerk

Der erste Schritt ist zum Ausführen des Tools PST-Auflistung, um die PST-Dateien in Ihrer Organisation zu suchen. Das Tool können Sie um die folgenden Arten von Speicherorten zu suchen. 
  
- Organisationseinheiten (OUs) in einer lokalen Active Directory-Domäne. Das Tool sucht in der angegebenen Organisationseinheit allen Computern, die enthalten sind. 
    
- Client und Server-Computern. Das Tool sucht die angegebenen Computer. 
    
- Netzwerk-Dateifreigaben. Das Tool sucht die angegebene Netzwerk-Dateifreigaben. 
    
Finden Sie in der Beschreibung der `Locations` Parameter in der Tabelle in der folgenden Prozedur Beispiele für die Syntax für jede dieser Speicherort Typen verwenden. 
  
> [!IMPORTANT]
> Sie müssen das Führen Sie das Tool PST-Auflistung in der Find-Modus vor dem Ausführen von anderen Aktionen wie blockieren, erfassen oder Löschen von PST-Dateien. 
  
1. Öffnen Sie ein Eingabeaufforderungsfenster (als Administrator ausführen) auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Ordner PSTCollectionTool (oder dem Ordner, dem Sie die Datei PSTCollectionTool.zip extrahiert haben).
    
3. Wechseln Sie zum Verzeichnis DataCollectorMaster.
    
4. Führen Sie den folgenden Befehl zum Suchen von PST-Dateien in einer angegebenen Position ein.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    In der folgenden Tabelle beschreibt die Parameter und deren Werte erforderlich, beim Ausführen des Befehls DataCollectorMaster.exe, PST-Dateien zu erhalten. 
    
    |Parameter ***|****Beschreibung****|Beispiele für ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ des zu suchenden Daten. Derzeit können Sie das Tool PST-Auflistung um zu suchenden PST-Dateien.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt den Typ des Vorgangs, mit denen das Tool ausgeführt wird. Verwenden Sie den Wert `Find` zum Suchen von PST-Dateien in den angegebenen Ordnern. Beachten Sie, dass das Tool suchen und Abrufen von Informationen zu PST-Dateien, die geöffnet in Outlook und PST-Dateien sind, die mit Outlook-Profilen verbunden werden kann.<br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |Gibt den Namen des Auftrags PST-Auflistung. Verwenden Sie diesen Auftragsnamen, wenn führen Sie das Tool PST-Auflistung zu blockieren, erfassen und Löschen von PST-Dateien, die beim Ausführen des Tools zum Suchen von PST-Dateien gefunden wurden. Name des Auftrags wird auch die Protokoll- und Konfiguration Dateinamen hinzugefügt werden.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | Gibt einen oder mehrere Speicherorte zu suchenden PST-Dateien an. Wenn Sie mehr als einem Standort angeben, verwenden Sie ein Semikolon (;), um einzelne Speicherorte zu trennen. Achten Sie darauf, um die einzelnen Werte dieses Parameters mit doppelte Anführungszeichen umgeben ("").<br/><br/>   Hier wird das Format für erforderliche Identität Wert für die Typen der Speicherorte, die durchsucht werden.  <br/><br/>        **Organisationseinheiten** - verwenden Sie den distinguished Name (DN), um Organisationseinheiten identifizieren; Zum Beispiel:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> Sie können keine integrierten Container Computer angeben (beispielsweise CN = Computers, DC = Contoso, DC = com "), da es eine Organisationseinheit nicht.<br/> <br/> **Computer** - Verwendung der DN oder den vollqualifizierten Domänennamen (FQDN), um Client und Server-Computern in Ihrem Netzwerk zu identifizieren; Zum Beispiel:  <br/>  DN:`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  Oder  <br/>  FQDN:`"FILESERVER01.contoso.com"` <br/><br/>  **Netzwerk-Dateifreigaben** - Verwendung einen UNC-Namen zum Identifizieren der Netzwerk-Dateifreigaben; Zum Beispiel`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, dem in die Protokolldateien kopiert werden. Wenn der Ordner nicht vorhanden ist, wird sie beim Ausführen des Tools erstellt.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, dem die XML-Konfigurationsdatei auf kopiert werden. Diese Datei enthält Informationen zu jeder PST-Datei, die beim Ausführen des Tools gefunden wird. Führen Sie das Tool im Schritt 3 zum Kopieren von PST-Dateien, die gefunden werden, wird diese Datei verwendet werden.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |Dieser optionale Parameter gibt Speicherorte während eines Suchvorgangs überspringen. Sie können bestimmte Organisationseinheiten, Computer und Netzwerkfreigaben ausschließen. Angenommen, Sie konnte Ausschließen von Computern, wie beispielsweise Computer als SQLServer (oder andere Arten von Anwendungsservern) konfiguriert, dass Benutzer keinen Zugriff haben. Wenn Sie mehr als einem Standort auszuschließende angeben, verwenden Sie ein Semikolon (;), um einzelne Speicherorte zu trennen. Achten Sie darauf, um die einzelnen Werte dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |Diese optionale Befehlszeilenoption können Sie das Tool im Modus für einen vorhandenen PST-Auflistung Auftrag Suchen ausführen. Bei Verwendung der `ForceRestart` wechseln, die Ergebnisse aus der vorherigen Suchvorgang für der Auftrag wird verworfen, und das Tool neu bestimmten Positionen durchsucht und Erstellen neuer Dateien von Protokoll- und Konfiguration.<br/> | `-ForceRestart` <br/> |
   
    Es folgt ein Beispiel für die Syntax für den DataCollectorMaster.exe-Befehl mit der tatsächlichen Werte für jeden Parameter:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    Nachdem Sie den Befehl ausführen, werden Ausführliche Statusnachrichten angezeigt, die den Fortschritt der Suchen von PST-Dateien in den angegebenen Ordnern anzuzeigen. Nach einer gewissen zeigt eine abschließende Statusnachricht an die Gesamtzahl der PST-Dateien, die gefunden wurden, gibt an, ob der Auftrag abgeschlossen wurde, und wenn Fehler aufgetreten sind. Die gleiche Statusnachrichten werden in der Datei .log kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>Ergebnisse der Ausführung von DataCollectorMaster.exe in der Find-Modus

Nachdem Sie erfolgreich dem Tool PST-Auflistung den Find-Modus ausgeführt, die folgenden Dateien erstellt und in die von angegebenen Ordner gespeichert werden die `LogLocation` und `ConfigurationLocation` Parameter. 
  
- **\<Auftragsname\>_Suchen_\<DateTimeStamp\>.log** -die Protokolldatei enthält die Statusnachrichten, die angezeigt wurden. Diese Datei wird erstellt, in den Ordner in der `LogLocation` Parameter. 
    
- **\<Auftragsname\>_Suchen_\<DateTimeStamp\>CSV** -der CSV-Datei enthält eine Zeile für jede PST-Datei, die gefunden wurde. Die Informationen für jede PST-Datei enthält den Computer, auf dem die PST-Datei gefunden wurde, den vollständigen Pfad der PST-Datei, die Besitzer der PST-Datei und die Größe der PST-Datei (in KB, KB-Artikel). Diese Datei wird erstellt, in den Ordner in der `LogLocation` Parameter. 
    
    > [!TIP]
    > Verwenden Sie das Tool AutoSum in Excel zum Berechnen der Gesamtgröße (in KB) aller PST-Dateien, die in der CSV-Datei aufgelistet. Klicken Sie dann können Sie einen Konvertierung Rechner verwenden, um die Gesamtgröße in Megabyte (MB) oder Gigabyte (GB) zu konvertieren. 
  
- **\<Auftragsname\>_Suchen_\<DateTimeStamp\>.xml** -die XML-Datei enthält Informationen über der Parameter Werte, wobei verwendet, wenn Sie das Tool im Modus suchen ausgeführt haben. Diese Datei enthält auch Informationen zu jeder PST-Datei, die gefunden wurde. Die Daten in dieser Datei wird beim Ausführen von erneut ausführen des Tools für den gleichen Auftrags sammeln, blockieren, oder löschen Sie die PST-Dateien, die gefunden wurden. Diese Datei wird erstellt, in den Ordner in der `ConfigurationLocation` Parameter. 
    
    > [!IMPORTANT]
    > Nicht umbenennen Sie, ändern Sie oder verschieben Sie diese Datei. Es wird von dem Tool PST-Auflistung verwendet, führen Sie das Tool erneut aus, in den Block, kopieren, oder Löschen von Modus für den gleichen Auftrag. 

## <a name="optional-step-2-control-access-to-pst-files"></a>(Optional) Schritt 2: Steuern des Zugriffs auf PST-Dateien

Optionaler Schritt können Sie "PST-Dateien, die in Schritt 1 gefunden wurden, damit Sie sammeln und importieren Sie eine bekannte Gruppe von PST-Dateien in Office 365 können Sperren". Wenn Sie das Tool PST-Auflistung in der Blockmodus ausführen, geschieht Folgendes: 
  
- Das Tool erstellt ein Gruppenrichtlinienobjekt (GPO) mit dem Namen *PST Usage Steuerelemente* . In diesem Gruppenrichtlinienobjekt mit Ihrer Domäne verknüpft ist, und gilt für alle authentifizierten Benutzer in Ihrer Organisation. 
    
- Die PST-Verwendung Steuerelemente Gruppenrichtlinienobjekt erstellt Registrierungseinträge auf Computern in Ihrer Organisation. Je nach der Parameter, den Sie verwenden, können Sie einen Registrierungseintrag, um zu verhindern, dass Benutzer Erstellen neuer PST-Dateien und eine Einstellung in der Registrierung, die verhindert, dass Benutzer ändern vorhandene PST-Dateien erstellen.
    
> [!NOTE]
> Steuern des Zugriffs auf PST-Dateien für Ihre Organisation zu störende ist, sollten Sie diesen Schritt überspringen und Schritt 3 zum Kopieren von PST-Dateien an einem zentralen Speicherort ausführen. Und Sie für den gleichen Auftrag wiederholen Schritt 1 Sie können (mithilfe der `ForceRestart` Parameter), zusätzliche PST-Dateien zu erhalten, die erstellt wurden, nachdem Sie PST-Dateien an die Auflistung Speicherort kopiert. Wenn neue PST-Dateien gefunden werden, können Sie sie an die Auflistung Speicherort kopieren. Bei Verwendung der `ForceRestart` Parameter, wenn Sie das Tool im Modus suchen erneut ausführen, die Ergebnisse aus der vorherigen Suchvorgang für einen Auftrag verworfen werden und das Tool die angegebenen Speicherorten erneut scannt. 

So blockieren Sie den Zugriff auf PST-Dateien:

1. Öffnen Sie ein Eingabeaufforderungsfenster (als Administrator ausführen) auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool PST-Auflistung heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl zum Blockieren des Zugriffs auf die PST-Dateien in Schritt 1 gefunden.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben, beim Ausführen des Befehls DataCollectorMaster.exe das Erstellen und Ändern von PST-Dateien blockieren. 
    
    |Parameter ***|****Beschreibung****|Beispiele für ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ des zu suchenden Daten. Derzeit können Sie das Tool PST-Auflistung um zu suchenden PST-Dateien.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt den Typ des Vorgangs, mit denen das Tool ausgeführt wird. Verwenden Sie den Wert `Block` hindert Benutzer am Erstellen neuer PST-Dateien und Durchführen von Änderungen an vorhandenen PST-Dateien.<br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |Gibt den Namen eines Auftrags für den vorhandenen PST-Auflistung. Sie müssen diesen Auftragsnamen verwenden, die Sie beim Ausführen des Tools im Modus finden Sie in Schritt 1 verwendet. Dieser Auftragsname wird auch auf den Namen der Protokolldatei hinzugefügt, die beim Ausführen des Tools in der Blockmodus erstellt wird.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Gibt an, dass der Ordner die XML-Konfigurationsdatei enthält, die beim Ausführen des Tools in der Find-Modus erstellt wurde. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 1 verwendet.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, dem in die Protokolldatei für den Zugriffsschutz Vorgang kopiert werden. Dies ist ein optionaler Parameter. Wenn Sie nicht enthalten, wird die Protokolldatei in den Ordner kopiert, in dem Sie das Tool PST-Auflistung heruntergeladen haben. Erwägen Sie den gleichen Speicherort, den Sie verwendet, wenn Sie das Tool im Modus finden Sie in Schritt 1 ausgeführt haben, damit die Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |Verwenden Sie diese Option, um Benutzer daran zu hindern, eine PST-Datei zu ändern. Wenn Sie diese Option verwenden, wird der folgende Registrierungseintrag erstellt: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` und der Wert auf 1 festgelegt ist. Diese Einstellung in der Registrierung wird auf den Computern in Ihrer Organisation, die dem Gruppenrichtlinienobjekt erstellt, die beim Ausführen des Tools PST-Auflistung in der Blockmodus erstellt wird.<br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |Verwenden Sie diese Option verhindert, dass Benutzer neue PST-Dateien zu erstellen, öffnen und PST-Dateien in Outlook importieren und Exportieren von PST-Dateien aus Outlook. Wenn Sie diese Option verwenden, wird der folgende Registrierungseintrag erstellt: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` und der Wert auf 1 festgelegt ist. Diese Einstellung in der Registrierung wird auf den Computern in Ihrer Organisation, die dem Gruppenrichtlinienobjekt erstellt, die beim Ausführen des Tools PST-Auflistung in der Blockmodus erstellt wird.<br/> | `-BlockNewFiles` <br/> |
   
    Es folgt ein Beispiel für die Syntax für den DataCollectorMaster.exe-Befehl mit der tatsächlichen Werte für jeden Parameter:

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    Sie werden aufgefordert, zu bestätigen, dass Sie neue PST-Dateien oder Änderungen an vorhandenen PST-Dateien blockieren möchten. Bestätigen Sie, dass Sie den Vorgang fortsetzen möchten, und der Befehl erfolgreich ausgeführt wird, wird eine Meldung angezeigt, dass ein neues Gruppenrichtlinienobjekt, mit dem Namen "PST Usage Steuerelemente" erstellt wurde.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>Schritt 3: Kopieren Sie die PST-Dateien an einen Speicherort für die Auflistung

Im nächsten Schritt wird, kopieren Sie die PST-Dateien, die gefunden, in dem das Tool PST-Auflistung in der Find-Modus ausgeführt. Auf diese Weise können Sie die PST-Dateien an einem Ort zu sammeln, damit Sie später zu Office 365 importieren können. Bevor Sie die PST-Dateien in der Auflistung Speicherort kopieren, sollten Sie die Ermittlung die Gesamtmenge des Speicherplatzes, der erforderlich ist. Sie können dazu die CSV-Datei, die in Schritt 1 berechnet die Gesamtgröße aller PST-Dateien erstellt wurde.
  
> [!NOTE]
> Nachdem Sie die PST-Dateien in Office 365 importiert und aus dem ursprünglichen Speicherort gelöscht haben, sollten Sie diese aus dem Speicherort der Auflistung zu löschen, die sie in diesem Schritt kopiert wurde. 
  
1. Öffnen Sie ein Eingabeaufforderungsfenster (als Administrator ausführen) auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool PST-Auflistung heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl zum Kopieren von PST-Dateien an einem angegebenen Speicherort.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    Die folgende Tabelle beschreibt die Parameter und deren Werte erforderlich beim Ausführen des Befehls DataCollectorMaster.exe zum Kopieren von PST-Dateien. 
    
    |Parameter ***|****Beschreibung****|Beispiele für ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ des zu suchenden Daten. Derzeit können Sie das Tool PST-Auflistung um zu suchenden PST-Dateien.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt den Typ des Vorgangs, mit denen das Tool ausgeführt wird. Verwenden Sie den Wert `Collect` zu kopieren, PST-Dateien gefunden Wenn Sie das Tool im Modus suchen ausgeführt haben. Beachten Sie, dass das Tool können Kopie von PST-Dateien, die in Outlook geöffnet sind, und kopieren Sie die PST-Dateien, die mit Outlook-Profilen verbunden sind.<br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |Gibt den Namen eines Auftrags für den vorhandenen PST-Auflistung. Sie müssen diesen Auftragsnamen verwenden, die Sie beim Ausführen des Tools im Modus finden Sie in Schritt 1 verwendet. Dieser Auftragsname wird auch auf den Namen der Protokolldatei hinzugefügt, die beim Ausführen des Tools im erfassen Modus erstellt wird.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |Verwenden Sie den gleichen Wert, den Sie für verwendet die `Locations` Parameter in Schritt 1. Sie haben diese Parameter einschließen, wenn Sie das Tool im Modus erfassen ausführen, wenn Sie das Tool zum Löschen der PST-Dateien aus ihrem Quellspeicherort in Schritt 5 erneut ausführen möchten.<br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, der die XML-Konfigurationsdatei enthält, die beim Ausführen des Tools in der Find-Modus erstellt wurde. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 1 verwendet.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |Gibt die Auflistung Position, wo Sie die PST-Dateien kopieren möchten. Sie können Dateien in einem Dateiserver, eine Netzwerkdateifreigabe oder einer Festplatte kopieren. Der Speicherort muss vor dem Ausführen des Tools im Modus erfassen vorhanden sein. Das Tool nicht erstellen Sie den Speicherort und liefert eine Fehlermeldung ausgegeben, dass er nicht vorhanden ist.  <br/> Darüber hinaus müssen Sie Berechtigungen in den von diesem Parameter angegebenen Auflistung Speicherort zu schreiben.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, dem in die Protokolldatei für den erfassen Modus kopiert werden. Dies ist ein optionaler Parameter. Wenn Sie nicht enthalten, wird die Protokolldatei in den Ordner kopiert, in dem Sie das Tool PST-Auflistung heruntergeladen haben. Erwägen Sie den gleichen Speicherort, den Sie verwendet, wenn Sie das Tool im Modus finden Sie in Schritt 1 ausgeführt haben, damit die Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Diese optionale Befehlszeilenoption können Sie das Tool im Modus Auflistung für eine vorhandene Auflistung von PST-Auftrag erneut ausführen. Wenn Sie zuvor das Tool im Modus erfassen ausgeführt, aber ausgeführt wurde das Tool erneut in die Find-Modus mit der `ForceRestart` wechseln, um Speicherorte für PST-Dateien erneut zu überprüfen, verwenden Sie diese Option erneut führen das Tool im Modus Auflistung und kopieren Sie die PST-Dateien gefunden wurden erneut Ihre die Speicherorte erneut gescannt. Bei Verwendung der `ForceRestart` Switch im Modus der Auflistung, das Tool alle vorherigen Vorgänge an Websitesammlungen ignoriert und versucht, kopieren Sie die PST-Dateien von Grund auf neu.<br/> | `-ForceRestart` <br/> |
   
    Es folgt ein Beispiel für die Syntax für das DataCollectorMaster.exe-Tool mit der tatsächlichen Werte für jeden Parameter:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    Nachdem Sie den Befehl ausführen werden Ausführliche Statusnachrichten angezeigt, die zeigen den Fortschritt der Erfassung der PST-Dateien, die in Schritt 1 gefunden wurden. Nach einer gewissen zeigt eine abschließende Statusnachricht an, wenn alle Fehler und den Speicherort an, dem das Protokoll zum kopiert werden. Die gleiche Statusnachrichten werden in der Datei .log kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>Ergebnisse der Ausführung von DataCollectorMaster.exe im Modus sammeln

Nachdem DataCollectorMaster.exe im Modus erfassen erfolgreich ausgeführt wurde, die folgenden Dateien erstellt und in die von angegebenen Ordner gespeichert werden die `LogLocation` und `ConfigurationLocation` Parameter. 
  
- **\<Auftragsname\>_Sammeln_\<DateTimeStamp\>.log** -die Protokolldatei enthält die Statusnachrichten, die angezeigt wurden. Diese Datei wird erstellt, in den Ordner in der `LogLocation` Parameter. 
    
- **\<Auftragsname\>_Sammeln_\<DateTimeStamp\>.xml** -die XML-Datei enthält nur Informationen zum Parameterwerte, wobei von verwendet das Tool im Modus erfassen ausgeführt wurde. Die Daten in dieser Datei wird bei der Ausführung erneut ausführen des DataCollectorMaster.exe-Tools zum Löschen von PST-Dateien finden Sie unter [Schritt 5](#step-5-delete-the-pst-files-found-on-your-network).
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>Schritt 4: Importieren von PST-Dateien in Office 365

Nachdem Sie die PST-Dateien gefunden, die in Schritt 1 gesammelt haben, besteht der nächste Schritt auf Postfächer in Office 365 importieren. Als Teil oder den Importvorgang müssen Sie eine CSV-Datei zur Zuordnung zu erstellen, die eine Zeile jeder PST-Datei enthält, die Sie importieren möchten. Informationen in jeder Zeile gibt den Namen der PST-Datei, e-Mail-Adresse des Benutzers, und, ob Sie dem Benutzer die PST-Datei importieren möchten, der primären oder Postfach zu archivieren. Verwenden Sie die Informationen in der **Auftragsname\>_Suchen_\<DateTimeStamp.csv** (in Schritt erstellten) Datei 1 beim Erstellen der CSV-Datei zur Zuordnung. 
  
Eine schrittweise Anleitung zum Importieren von PST-Dateien nach Office 365 finden Sie in den folgenden Themen:
  
- [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
    
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>Schritt 5: Löschen Sie die PST-Dateien in Ihrem Netzwerk gefunden

Nach Exchange Online-Postfächern in Office 365 PST-Dateien, die gefunden und erfasst importiert wurden, können Sie das Tool PST-Auflistung verwenden, um die PST-Dateien aus der ursprünglichen Speicherorte für Datenquellen zu löschen, in dem sie in Schritt 1 gefunden wurden. 
  
1. Öffnen Sie ein Eingabeaufforderungsfenster (als Administrator ausführen) auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool PST-Auflistung heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl aus, um die PST-Dateien zu löschen.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben, beim Ausführen des Befehls DataCollectorMaster.exe PST-Dateien zu löschen. 
    
    |Parameter ***|****Beschreibung****|Beispiele für ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ des zu suchenden Daten. Derzeit können Sie das Tool PST-Auflistung um zu suchenden PST-Dateien. ![Abstandhalter](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt den Typ des Vorgangs, mit denen das Tool ausgeführt wird. Verwenden Sie den Wert `Delete` löschen, PST-Dateien gefunden Wenn Sie das Tool im Modus suchen ausgeführt haben.<br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |Gibt den Namen eines Auftrags für den vorhandenen PST-Auflistung. Sie müssen diesen Auftragsnamen verwenden, die Sie beim Ausführen des Tools im das Suchen und die in Schritt 1 und Schritt 3 erfassen Modus verwendet. Dieser Auftragsname wird auch auf den Namen der Protokolldatei hinzugefügt, die erstellt wird, wenn Sie das Tool im Modus löschen ausführen.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, der die XML-Konfigurationsdatei, die erstellt wurde enthält, wenn Sie das Tool im Modus erfassen ausgeführt haben. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 3 verwendet.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, dem in die Protokolldatei für die Löschmodus kopiert werden. Dies ist ein optionaler Parameter. Wenn Sie nicht enthalten, wird die Protokolldatei in den Ordner kopiert, in dem Sie das Tool PST-Auflistung heruntergeladen haben. Erwägen Sie den gleichen Speicherort, den Sie verwendet, wenn Sie das Tool im suchen und sammeln Modi in Schritt 1 und Schritt 3 ausgeführt haben, damit die Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Diese optionale Befehlszeilenoption können Sie das Tool im Modus für einen vorhandenen Auftrag PST-Auflistung löschen erneut ausführen. Wenn Sie das Tool im Modus löschen zuvor ausgeführt, aber ausgeführt wurde das Tool erneut in die Find-Modus mit der `ForceRestart` wechseln, um Speicherorte für PST-Dateien erneut zu überprüfen, können Sie diese Option verwenden, führen Sie das Tool im Löschmodus erneut aus, und löschen die PST-Dateien gefunden wurden Ihre Re-Sca Nned die Speicherorte. Bei Verwendung der `ForceRestart` Switch im Löschmodus, das Tool alle vorherigen Löschvorgänge ignoriert und versucht, die PST-Dateien erneut zu löschen.<br/> | `-ForceRestart` <br/> 

    Es folgt ein Beispiel für die Syntax für das DataCollectorMaster.exe-Tool mit der tatsächlichen Werte für jeden Parameter:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    Nach der Ausführung des Befehls werden Ausführliche Statusnachrichten angezeigt, die zeigen den Fortschritt des Löschens von PST-Dateien, die in Schritt 1 gefunden und in Schritt 3 erfasst wurden. Nach einer gewissen zeigt eine abschließende Statusnachricht an, wenn alle Fehler und den Speicherort an, dem das Protokoll zum kopiert werden. Die gleiche Statusnachrichten werden in der Datei .log kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>Ergebnisse der Ausführung von DataCollectorMaster.exe im Modus löschen

Nachdem DataCollectorMaster.exe im Modus löschen erfolgreich ausgeführt wurde, werden die folgenden Dateien erstellt und gespeichert im Ordner angegeben wird, durch die `LogLocation` und `ConfigurationLocation` Parameter. 
  
- **\<Auftragsname\>_Löschen_\<DateTimeStamp\>.log** -die Protokolldatei enthält die Statusnachrichten, die angezeigt wurden. Diese Datei wird erstellt, in den Ordner in der `LogLocation` Parameter. 
    
- **\<Auftragsname\>_Löschen_\<DateTimeStamp\>.xml** -die XML-Datei enthält nur Informationen zum Parameterwerte, wobei von verwendet das Tool im Modus löschen ausgeführt wurde. Enthält den Namen und den Dateipfad der einzelnen PST-Dateien, die gelöscht wurde. Diese Datei wird erstellt, in den Ordner in der `ConfigurationLocation` Parameter. 

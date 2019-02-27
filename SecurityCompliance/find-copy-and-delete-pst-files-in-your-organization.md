---
title: Verwenden des PST-Sammlungs Tools zum Suchen, kopieren und Löschen von PST-Dateien in Ihrer Organisation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Verwenden Sie das Microsoft-PST-Sammlungs Tool, um das Netzwerk Ihrer Organisation zu durchsuchen, um eine Bestandsaufnahme der PST-Dateien zu erhalten, die in Ihrer Organisation verstreut sind. Nachdem Sie PST-Dateien gefunden haben, können Sie das PST-Sammlungs Tool verwenden, um Sie an einem zentralen Speicherort zu kopieren, damit Sie Sie in Office 365 importieren können.
ms.openlocfilehash: 87e13ec8a4c58f848ac2ff7a430a7532942ece74
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296958"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>Verwenden des PST-Sammlungs Tools zum Suchen, kopieren und Löschen von PST-Dateien in Ihrer Organisation

> [!IMPORTANT]
> Das in diesem Artikel beschriebene PST-Sammlungs Tool wird unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt. Das Tool wird ohne Gewähr bereitgestellt. Microsoft lehnt weiterhin alle impliziten Garantien ab, einschließlich der impliziten Garantien der Marktgängigkeit oder der Eignung für einen bestimmten Zweck. Das gesamte Risiko, das sich aus der Nutzung oder Leistung des Tools und der Dokumentation ergibt, liegt bei Ihnen. In keinem Fall sind Microsoft, seine Autoren oder andere Personen, die an der Erstellung, Produktion oder Bereitstellung des Tools beteiligt sind, haftbar für Schäden jeglicher Art (einschließlich, ohne Einschränkung, Schäden für Verlust von Geschäftsgewinnen, Betriebsunterbrechung, Verlust von geschäftliche Informationen oder sonstige Vermögensschäden, die sich aus der Verwendung oder der Unfähigkeit zur Verwendung des Tools oder der Dokumentation ergeben, auch wenn Microsoft über die Möglichkeit solcher Schäden informiert wurde.

Sie können das Microsoft-PST-Sammlungs Tool verwenden, um das Netzwerk Ihrer Organisation nach PST-Dateien zu durchsuchen. Mit dem Tool erhalten Sie eine Bestandsaufnahme der PST-Dateien, die in Ihrer Organisation verstreut sind. Nachdem Sie PST-Dateien gefunden haben, können Sie das PST-Sammlungs Tool verwenden, um Sie an einem zentralen Speicherort zu kopieren. Wenn Sie PST an einem zentralen Ort haben, können Sie Sie in Exchange Online-Postfächer importieren (oder ein einzelnes Exchange Online-Postfach), in dem Sie die umfangreichen Compliance-Features in Office 365 anwenden können. Dazu gehört das Importieren von PST in Archivpostfächer der Benutzer, das Suchen nach bestimmten Nachrichten in den PST-Dateien, die Sie mithilfe von eDiscovery-Such Tools importiert haben, das Speichern von Nachrichten mithilfe von eDiscovery-Haltebereichen und Office 365-Aufbewahrungsrichtlinien sowie die Verwaltung der Lebensdauer Zyklus dieser Nachrichten mithilfe der Funktionen zur Verwaltung von Nachrichtendatensätzen in Exchange Online. Nachdem Sie sicher sind, dass die von Ihnen gesammelten PST-Dateien erfolgreich in Office 365 importiert wurden, können Sie das Tool verwenden, um Sie von Ihrem ursprünglichen Speicherort in Ihrem Netzwerk zu löschen. 
  
Sie können auch das PST-Sammlungs Tool verwenden, um zu verhindern, dass Benutzer neue PST-Dateien erstellen und die vorhandenen PST-Dateien ändern, die Sie in Ihrem Netzwerk finden. Mit diesen "blockieren"-Funktionen können Sie bekannte PST-Dateien in Office 365 finden, sammeln und importieren und die zukünftige Proliferation von PST-Dateien in Ihrer Organisation verhindern. 
  
## <a name="how-the-pst-collection-tool-works"></a>Funktionsweise des PST-Sammlungs Tools

Hier finden Sie einen kurzen Überblick über den Prozess der Verwendung des PST-Sammlungs Tools zum Suchen, Steuern, sammeln und Löschen von PST-Dateien in Ihrer Organisation.
  
![Übersicht über den Prozess des PST-Sammlungs Tools](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[Schritt 1: Suchen von PST-Dateien in Ihrem Netzwerk](#step-1-find-pst-files-on-your-network)** -Wenn Sie das Tool ausführen, um PST-Dateien zu finden, geben Sie einen Speicherort an, beispielsweise eine Organisationseinheit, die Active Directory-Objekte für Client-und Server Computer enthält. Sie können auch bestimmte Computer oder Netzwerkdateifreigaben durchsuchen. Wenn Sie das Tool ausführen, wird auf den Zielcomputern ein "Lightweight"-Sammlungs-Agent installiert. Dieser Agent durchsucht den Zielcomputer nach PST-Dateien und sendet dann Informationen zu jeder gefundenen PST-Datei zurück an das PST-Sammlungs Tool. Das Tool erstellt Protokolldateien, die Informationen zu den PST-Dateien enthalten, die an den angegebenen Speicherorten gefunden wurden. Diese Dateien werden verwendet, wenn Sie das Tool in späteren Schritten ausführen. 
    
2. **[(Optional) Schritt 2: Steuern des Zugriffs auf PST-Dateien](#optional-step-2-control-access-to-pst-files)** – das Tool erstellt ein Gruppenrichtlinienobjekt (GPO) mit Einstellungen, mit denen verhindert werden soll, dass Benutzer PST-Dateien erstellen oder ändern. Dieses GPO wird auf alle Benutzer in Ihrer Domäne angewendet. Dieser optionale Schritt hilft Ihnen bei der "Sperrung" der PST-Dateien, die in Schritt 1 gefunden wurden, sodass Sie Sie sammeln, importieren und löschen können, ohne dass neue PST-Dateien erstellt oder die vorhandenen PST-Dateien geändert wurden. 
    
3. **[Schritt 3: Kopieren der PST-Dateien in einen Sammel Speicherort](#step-3-copy-the-pst-files-to-a-collection-location)** – mit dieser Option können Sie die PST-Dateien an einem Speicherort sammeln, sodass Sie Sie mithilfe des Office 365-Import Diensts in Schritt 4 in Exchange Online-Postfächer importieren. Wenn Sie das Tool im Modus "sammeln" ausführen, kopiert jeder Sammlungs-Agent die PST-Dateien vom Zielcomputer, auf dem der Agent installiert ist, an den Speicherort der Sammlung. 
    
4. **[Schritt 4: Importieren der PST-Dateien in Office 365](#step-4-import-the-pst-files-to-office-365)** – nachdem Sie die PST-Dateien an einen Speicherort kopiert haben, können Sie Sie in Exchange Online-Postfächer importieren. 
    
5. **[Schritt 5: Löschen der PST-Dateien, die in Ihrem Netzwerk gefunden](#step-5-delete-the-pst-files-found-on-your-network)** wurden-nachdem die PST-Dateien, die Sie gefunden und gesammelt haben, in Exchange Online-Postfächer in Office 365 importiert wurden, können Sie das PST-Sammlungs Tool verwenden, um die PST-Dateien von den ursprünglichen Speicherorten zu löschen, an denen Sie wurden in Schritt 1 gefunden. 

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Führen Sie die folgenden Schritte aus, um das PST-Sammlungs Tool auf Ihren lokalen Computer herunterzuladen. 
    
    1. [Laden Sie das PST-Sammlungs Tool herunter](https://aka.ms/pstcollectiontool).
    
    2. Klicken Sie **** \> **** im Popupfenster auf Speichern unter, um die Datei PSTCollectionTool. zip in einem Ordner auf dem lokalen Computer zu speichern. 
    
    3. Extrahieren Sie die Datei PSTCollectionTool. zip in einen Ordner auf Ihrem lokalen Computer. der standardmäßige Ordnername ist PSTCollectionTool.
    
- Sie müssen Mitglied der Gruppe "Domänenadministratoren" in Ihrer Active Directory-Domäne sein, um das PST-Sammlungs Tool in einem beliebigen Modus (suchen, blockieren, kopieren oder löschen) ausführen zu können. 

## <a name="step-1-find-pst-files-on-your-network"></a>Schritt 1: Suchen von PST-Dateien in Ihrem Netzwerk

Der erste Schritt besteht darin, das PST-Sammlungs Tool auszuführen, um PST-Dateien in Ihrer Organisation zu finden. Sie können das Tool verwenden, um die folgenden Arten von Speicherorten zu durchsuchen. 
  
- Organisationseinheiten (Organizational Units, OUs) in einer lokalen Active Directory-Domäne. Das Tool sucht alle Computer, die in der angegebenen Organisationseinheit enthalten sind. 
    
- Client-und Server Computer. Das Tool durchsucht die angegebenen Computer. 
    
- Netzwerkdateifreigaben. Das Tool durchsucht die angegebenen Netzwerkdateifreigaben. 
    
Beispiele für die Syntax, `Locations` die für jeden dieser Speicherort Typen verwendet werden, finden Sie in der Beschreibung des Parameters in der Tabelle in der folgenden Vorgehensweise. 
  
> [!IMPORTANT]
> Sie müssen das Tool zum Ausführen der PST-Auflistung im Such Modus aktivieren, bevor Sie andere Aktionen wie das blockieren, sammeln oder Löschen von PST-Dateien ausführen können. 
  
1. Öffnen Sie auf dem lokalen Computer eine EingabeaufForderungen (als Administrator ausführen).
    
2. Wechseln Sie zum Ordner PSTCollectionTool (oder den Ordner, in den Sie die Datei PSTCollectionTool. zip extrahiert haben).
    
3. Wechseln Sie in das DataCollectorMaster-Verzeichnis.
    
4. Führen Sie den folgenden Befehl aus, um PST-Dateien an einem angegebenen Speicherort zu finden.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    In der folgenden Tabelle werden die Parameter und die erforderlichen Werte beschrieben, wenn Sie den Befehl DataCollectorMaster. exe ausführen, um PST-Dateien zu finden. 
    
    |Parameter * * * *|****Beschreibung****|Beispiele * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ der zu suchenden Daten an. Derzeit können Sie das PST-Sammlungs Tool verwenden, um nach PST-Dateien zu suchen.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt die Art der Operation an, die vom Tool ausgeführt wird. Verwenden Sie den `Find` Wert, um PST-Dateien an den angegebenen Speicherorten zu suchen. Beachten Sie, dass das Tool Informationen zu PST-Dateien finden und abrufen kann, die in Outlook-und PST-Dateien geöffnet sind, die mit Outlook-Profilen verbunden sind.<br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |Gibt den Namen des PST-Sammlungs Auftrags an. Sie verwenden denselben Auftragsnamen, wenn Sie das PST-Sammlungs Tool ausführen, um die PST-Dateien zu blockieren, zu sammeln und zu löschen, die gefunden werden, wenn Sie das Tool ausführen, um PST-Dateien zu finden. Der Auftragsname wird auch den Namen der Protokoll-und Konfigurationsdateien hinzugefügt.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | Gibt einen oder mehrere Speicherorte für die Suche nach PST-Dateien an. Wenn Sie mehrere Standorte angeben, verwenden Sie ein Semikolon (;) Trennen einzelner Standorte. Stellen Sie sicher, dass Sie die einzelnen Werte dieses Parameters mit doppelten Anführungszeichen ("") umgeben.<br/><br/>   Hier ist das erforderliche Identitätswert Format für die Typen von Speicherorten, die Sie durchsuchen können.  <br/><br/>        **OUs** – verwenden Sie den Distinguished Name (DN), um Organisationseinheiten zu identifizieren. Zum Beispiel:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> Sie können den integrierten Computer Container (beispielsweise CN = Computers, DC = contoso, DC = com) nicht angeben, da es sich nicht um eine Organisationseinheit handelt.<br/> <br/> **Computer** – verwenden Sie den DN oder den vollqualifizierten Domänennamen (FQDN), um Client-und Server Computer in Ihrem Netzwerk zu identifizieren. Zum Beispiel:  <br/>  DN`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  Oder  <br/>  FQDN`"FILESERVER01.contoso.com"` <br/><br/>  **Netzwerkdateifreigaben** : Verwenden Sie einen UNC-Namen, um Netzwerkdateifreigaben zu identifizieren. Zum Beispiel`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, in den die Protokolldateien kopiert werden. Wenn der Ordner nicht vorhanden ist, wird er erstellt, wenn Sie das Tool ausführen.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, in den die XML-Konfigurationsdatei kopiert wird. Diese Datei enthält Informationen zu jeder PST-Datei, die gefunden wird, wenn Sie das Tool ausführen. Diese Datei wird verwendet, wenn Sie das Tool in Schritt 3 ausführen, um die gefundenen PST-Dateien zu kopieren.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |Dieser optionale Parameter gibt an, welche Positionen während eines Suchvorgangs übersprungen werden sollen. Sie können bestimmte Organisationseinheiten, Computer und Netzwerkdateifreigaben ausschließen. Beispielsweisekönnten Sie Computer ausschließen, wie Computer, die als SQL Server (oder andere Arten von Anwendungsservern) konfiguriert sind, auf die Benutzer keinen Zugriff haben. Wenn Sie mehr als einen auszuschließenden Standort angeben, verwenden Sie ein Semikolon (;) Trennen einzelner Standorte. Stellen Sie sicher, dass Sie die einzelnen Werte dieses Parameters mit doppelten Anführungszeichen ("") umgeben.  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |Mit dieser optionalen Option können Sie das Tool im Suchmodus für einen vorhandenen PST-Sammelauftrag ausführen. Wenn Sie die `ForceRestart` Option verwenden, werden die Ergebnisse des vorherigen Suchvorgangs für den Auftrag verworfen, und das Tool überprüft die angegebenen Speicherorte erneut und erstellt neue Protokoll-und Konfigurationsdateien.<br/> | `-ForceRestart` <br/> |
   
    NachFolgend finden Sie ein Beispiel für die Syntax für den Befehl DataCollectorMaster. exe, indem Sie die tatsächlichen Werte für jeden Parameter verwenden:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    Nachdem Sie den Befehl ausgeführt haben, werden detaillierte Statusmeldungen angezeigt, die den Fortschritt der Suche nach PST-Dateien an den angegebenen Speicherorten anzeigen. Nach einer Weile wird die Gesamtzahl der gefundenen PST-Dateien angezeigt, unabhängig davon, ob der Auftrag abgeschlossen wurde und ob Fehler aufgetreten sind. Die gleichen Statusmeldungen werden in die Log-Datei kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>Ergebnisse der Verwendung von DataCollectorMaster. exe im Suchmodus

Nachdem Sie das PST-Sammlungs Tool im Suchmodus erfolgreich ausgeführt haben, werden die folgenden Dateien in den Ordnern erstellt und gespeichert `LogLocation` , `ConfigurationLocation` die durch die Parameter und angegeben werden. 
  
- **\<Jobname\>__ Find\<DateTimeStamp\>. log** – die Protokolldatei enthält die Statusmeldungen, die angezeigt wurden. Diese Datei wird in dem durch den `LogLocation` -Parameter angegebenen Ordner erstellt. 
    
- **\<Jobname\>__ Find\<DateTimeStamp\>. CSV** – die CSV-Datei enthält eine Zeile für jede gefundene PST-Datei. Die Informationen für die einzelnen PST-Dateien enthalten den Computer, auf dem die PST-Datei gefunden wurde, den vollständigen Pfad der PST-Datei, den Besitzer der PST-Datei und die Größe (in Kilobytes, KBs) der PST-Datei. Diese Datei wird in dem durch den `LogLocation` -Parameter angegebenen Ordner erstellt. 
    
    > [!TIP]
    > Verwenden Sie das AutoSumme-Tool in Excel, um die Gesamtgröße (in KB) aller in der CSV-Datei aufgeführten PST-Dateien zu berechnen. Anschließend können Sie einen Konvertierungs Rechner verwenden, um die Gesamtgröße in Megabyte (MB) oder Gigabyte (GB) umzuwandeln. 
  
- **\<Jobname\>__ Find\<DateTimeStamp\>. XML** – die XML-Datei enthält Informationen zu den Parameterwerten, die beim Ausführen des Tools im Suchmodus verwendet wurden. Diese Datei enthält auch Informationen zu jeder PST-Datei, die gefunden wurde. Die Daten in dieser Datei werden verwendet, wenn Sie das Tool erneut ausführen, um die gefundenen PST-Dateien zu blockieren, zu sammeln oder zu löschen. Diese Datei wird in dem durch den `ConfigurationLocation` -Parameter angegebenen Ordner erstellt. 
    
    > [!IMPORTANT]
    > Umbenennen, ändern oder verschieben Sie diese Datei nicht. Sie wird vom PST-Sammlungs Tool verwendet, wenn Sie das Tool im Block-, Kopier-oder Löschmodus für denselben Auftrag erneut ausführen. 

## <a name="optional-step-2-control-access-to-pst-files"></a>Optional Schritt 2: Steuern des Zugriffs auf PST-Dateien

In diesem optionalen Schritt können Sie die PST-Dateien, die in Schritt 1 gefunden wurden, "Sperren", sodass Sie eine bekannte Gruppe von PST-Dateien in Office 365 sammeln und importieren können. Wenn Sie das PST-Sammlungs Tool im Block Modus ausführen, geschieht Folgendes: 
  
- Das Tool erstellt ein Gruppenrichtlinienobjekt (GPO) mit dem Namen *PST-Verwendungs Steuerung* . Dieses GPO ist mit Ihrer Domäne verknüpft und gilt für alle authentifizierten Benutzer in Ihrer Organisation. 
    
- Das GPO für PST-Verwendungs Steuerelemente erstellt Registrierungseinstellungen für Computer in Ihrer Organisation. Je nach verwendetem Parameter können Sie eine Registrierungseinstellung erstellen, um zu verhindern, dass Benutzer neue PST-Dateien erstellen, und eine Registrierungseinstellung, die verhindert, dass Benutzer vorhandene PST-Dateien ändern.
    
> [!NOTE]
> Wenn die Steuerung des Zugriffs auf PST-Dateien für Ihre Organisation zu störend ist, sollten Sie diesen Schritt überspringen und Schritt 3 ausführen, um PST-Dateien an einen zentralen Speicherort zu kopieren. Dann können Sie Schritt 1 für denselben Auftrag wiederholen (mithilfe des `ForceRestart` -Parameters), um weitere PST-Dateien zu finden, die erstellt wurden, nachdem Sie PST-Dateien an den Speicherort der Sammlung kopiert haben. Wenn neue PST-Dateien gefunden werden, können Sie Sie an den Speicherort der Sammlung kopieren. Wenn Sie den `ForceRestart` Parameter beim erneuten Ausführen des Tools im Suchmodus verwenden, werden die Ergebnisse des vorherigen Suchvorgangs für einen Auftrag verworfen, und das Tool überprüft die angegebenen Speicherorte erneut. 

So blockieren Sie den Zugriff auf PST-Dateien

1. Öffnen Sie auf dem lokalen Computer eine EingabeaufForderungen (als Administrator ausführen).
    
2. Wechseln Sie zu dem Verzeichnis, in das Sie das PST-Sammlungs Tool heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl aus, um den Zugriff auf die in Schritt 1 gefundenen PST-Dateien zu blockieren.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    In der folgenden Tabelle werden die Parameter und die erforderlichen Werte beschrieben, wenn Sie den Befehl DataCollectorMaster. exe ausführen, um das Erstellen und Ändern von PST-Dateien zu blockieren. 
    
    |Parameter * * * *|****Beschreibung****|Beispiele * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ der zu suchenden Daten an. Derzeit können Sie das PST-Sammlungs Tool verwenden, um nach PST-Dateien zu suchen.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt die Art der Operation an, die vom Tool ausgeführt wird. Verwenden Sie den `Block` Wert, um zu verhindern, dass Benutzer neue PST-Dateien erstellen und Änderungen an vorhandenen PST-Dateien vornehmen.<br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |Gibt den Namen eines vorhandenen PST-Sammlungs Auftrags an. Sie müssen denselben Auftragsnamen verwenden, den Sie beim Ausführen des Tools im Suchmodus in Schritt 1 verwendet haben. Dieser Auftragsname wird auch dem Namen der Protokolldatei hinzugefügt, die erstellt wird, wenn Sie das Tool im Blockmodus ausführen.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Gibt an, dass der Ordner die XML-Konfigurationsdatei enthält, die beim Ausführen des Tools im Suchmodus erstellt wurde. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 1 verwendet haben.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, in den die Protokolldatei für den Block Vorgang kopiert wird. Dies ist ein optionaler Parameter. Wenn Sie Sie nicht hinzufügen, wird die Protokolldatei in den Ordner kopiert, in den Sie das PST-Sammlungs Tool heruntergeladen haben. Erwägen Sie die Verwendung desselben Protokollspeicherorts, den Sie beim Ausführen des Tools im Such Modus in Schritt 1 verwendet haben, damit alle Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |Verwenden Sie diese Option, um zu verhindern, dass Benutzer eine PST-Datei ändern. Wenn Sie diese Option verwenden, wird der folgende Registrierungseintrag erstellt: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` und der Datenwert ist auf 1 festgelegt. Diese Registrierungseinstellung wird auf den Computern in Ihrer Organisation durch das Gruppenrichtlinienobjekt erstellt, das erstellt wird, wenn Sie das PST-Sammlungs Tool im Blockmodus ausführen.<br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |Verwenden Sie diese Option, um zu verhindern, dass Benutzer neue PST-Dateien erstellen, PST-Dateien in Outlook öffnen und importieren und PST-Dateien aus Outlook exportieren. Wenn Sie diese Option verwenden, wird der folgende Registrierungseintrag erstellt: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` und der Datenwert ist auf 1 festgelegt. Diese Registrierungseinstellung wird auf den Computern in Ihrer Organisation durch das Gruppenrichtlinienobjekt erstellt, das erstellt wird, wenn Sie das PST-Sammlungs Tool im Blockmodus ausführen.<br/> | `-BlockNewFiles` <br/> |
   
    NachFolgend finden Sie ein Beispiel für die Syntax für den Befehl DataCollectorMaster. exe, indem Sie die tatsächlichen Werte für jeden Parameter verwenden:

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    Sie werden aufgefordert zu bestätigen, dass Sie neue PST-Dateien oder Änderungen an vorhandenen PST-Dateien blockieren möchten. Nachdem Sie sichergestellt haben, dass Sie den Vorgang fortsetzen möchten und der Befehl erfolgreich ausgeführt wird, wird eine Meldung angezeigt, die besagt, dass ein neues GPO mit dem Namen "PST-Verwendungs Steuerung" erstellt wurde.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>Schritt 3: Kopieren der PST-Dateien in einen Sammlungs Speicherort

Der nächste Schritt besteht darin, die PST-Dateien zu kopieren, die gefunden wurden, als Sie das PST-Sammlungs Tool im Suchmodus ausgeführt haben. Auf diese Weise können Sie die PST-Dateien an einem Ort sammeln, damit Sie Sie später in Office 365 importieren. Bevor Sie die PST-Dateien in den Abhol Speicherort kopieren, sollten Sie die Gesamtmenge an Speicherplatz ermitteln, die erforderlich ist. Verwenden Sie dazu die CSV-Datei, die in Schritt 1 erstellt wurde, um die Gesamtgröße aller PST-Dateien zu berechnen.
  
> [!NOTE]
> Nachdem Sie die PST-Dateien in Office 365 importiert und am ursprünglichen Speicherort gelöscht haben, können Sie Sie in diesem Schritt aus dem Sammlungs Speicherort löschen, in den Sie Sie kopiert haben. 
  
1. Öffnen Sie auf dem lokalen Computer eine EingabeaufForderungen (als Administrator ausführen).
    
2. Wechseln Sie zu dem Verzeichnis, in das Sie das PST-Sammlungs Tool heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl aus, um die PST-Dateien an einen angegebenen Speicherort zu kopieren.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    In der folgenden Tabelle werden die Parameter und die erforderlichen Werte beschrieben, wenn Sie den Befehl DataCollectorMaster. exe ausführen, um PST-Dateien zu kopieren. 
    
    |Parameter * * * *|****Beschreibung****|Beispiele * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ der zu suchenden Daten an. Derzeit können Sie das PST-Sammlungs Tool verwenden, um nach PST-Dateien zu suchen.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt die Art der Operation an, die vom Tool ausgeführt wird. Verwenden Sie den `Collect` Wert, um die PST-Dateien zu kopieren, die beim Ausführen des Tools im Suchmodus gefunden wurden. Beachten Sie, dass das Tool in der Lage ist, PST-Dateien zu kopieren, die in Outlook geöffnet sind, und PST-Dateien kopieren, die mit Outlook-Profilen verbunden sind.<br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |Gibt den Namen eines vorhandenen PST-Sammlungs Auftrags an. Sie müssen denselben Auftragsnamen verwenden, den Sie beim Ausführen des Tools im Suchmodus in Schritt 1 verwendet haben. Dieser Auftragsname wird auch dem Namen der Protokolldatei hinzugefügt, die erstellt wird, wenn Sie das Tool im Sammlungsmodus ausführen.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |Verwenden Sie den gleichen Wert, den Sie für `Locations` den Parameter in Schritt 1 verwendet haben. Sie verwenden diesen Parameter, wenn Sie das Tool im Sammlungsmodus ausführen, wenn Sie das Tool erneut ausführen möchten, um die PST-Dateien aus dem Quellspeicherort in Schritt 5 zu löschen.<br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, der die XML-Konfigurationsdatei enthält, die beim Ausführen des Tools im Suchmodus erstellt wurde. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 1 verwendet haben.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |Gibt den Abhol Speicherort an, an den Sie die PST-Dateien kopieren möchten. Sie können Dateien auf einen Dateiserver, eine Netzwerkdateifreigabe oder eine Festplatte kopieren. Der Speicherort muss vorhanden sein, bevor Sie das Tool im Sammlungsmodus ausführen. Das Tool erstellt den Speicherort nicht und gibt einen Fehler zurück, der besagt, dass er nicht vorhanden ist.  <br/> Außerdem müssen Sie Berechtigungen für den durch diesen Parameter angegebenen Sammlungs Speicherort schreiben.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, in den die Protokolldatei für den Sammlungsmodus kopiert wird. Dies ist ein optionaler Parameter. Wenn Sie Sie nicht hinzufügen, wird die Protokolldatei in den Ordner kopiert, in den Sie das PST-Sammlungs Tool heruntergeladen haben. Erwägen Sie die Verwendung desselben Protokollspeicherorts, den Sie beim Ausführen des Tools im Such Modus in Schritt 1 verwendet haben, damit alle Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Mit dieser optionalen Option können Sie das Tool im Sammlungsmodus für einen vorhandenen PST-Sammelauftrag erneut ausführen. Wenn Sie das Tool zuvor im Sammlungsmodus ausgeführt, aber das Tool dann erneut im Suchmodus ausgeführt haben und die `ForceRestart` Option zum erneuten Scannen von Speicherorten für PST-Dateien verwendet haben, können Sie diese Option verwenden, um das Tool erneut im Sammelmodus auszuführen und die PST-Dateien erneut zu kopieren, die gefunden wurden, als Ihr die Speicherorte wurden erneut gescannt. Wenn Sie die `ForceRestart` Option im Sammlungsmodus verwenden, ignoriert das Tool alle vorherigen Sammlungsvorgänge und versucht, die PST-Dateien von Grund auf zu kopieren.<br/> | `-ForceRestart` <br/> |
   
    NachFolgend finden Sie ein Beispiel für die Syntax für das DataCollectorMaster. exe-Tool, das die tatsächlichen Werte für jeden Parameter verwendet:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    Nachdem Sie den Befehl ausgeführt haben, werden detaillierte Statusmeldungen angezeigt, die den Fortschritt der Sammlung der PST-Dateien anzeigen, die in Schritt 1 gefunden wurden. Nach einer Weile wird eine endgültige Statusmeldung angezeigt, wenn Fehler aufgetreten sind und der Speicherort, in den das Protokoll kopiert wird. Die gleichen Statusmeldungen werden in die Log-Datei kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>Ergebnisse der Verwendung von DataCollectorMaster. exe im Sammlungsmodus

Nachdem Sie DataCollectorMaster. exe erfolgreich im Sammlungsmodus ausgeführt haben, werden die folgenden Dateien in den Ordnern erstellt und gespeichert, die `LogLocation` durch `ConfigurationLocation` die Parameter und angegeben werden. 
  
- **\<Jobname\>__ Collect\<DateTimeStamp\>. log** -die Protokolldatei enthält die Statusmeldungen, die angezeigt wurden. Diese Datei wird in dem durch den `LogLocation` -Parameter angegebenen Ordner erstellt. 
    
- **\<Jobname\>__ Collect\<DateTimeStamp\>. XML** – die XML-Datei enthält nur Informationen zu den Parameterwerten, die von dem Tool im Sammlungsmodus verwendet wurden. Die Daten in dieser Datei werden verwendet, wenn Sie das DataCollectorMaster. exe-Tool ausführen, um PST-Dateien zu löschen. siehe [Schritt 5](#step-5-delete-the-pst-files-found-on-your-network).
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>Schritt 4: Importieren der PST-Dateien in Office 365

Nachdem Sie die in Schritt 1 gefundenen PST-Dateien gesammelt haben, besteht der nächste Schritt darin, Sie in Postfächer in Office 365 zu importieren. Als Teil oder der Importvorgang müssen Sie eine CSV-Zuordnungsdatei erstellen, die eine Zeile jeder PST-Datei enthält, die Sie importieren möchten. Die Informationen in jeder Zeile geben den Namen der PST-Datei, die e-Mail-Adresse des Benutzers und die Frage an, ob die PST-Datei in das primäre oder Archivpostfach des Benutzers importiert werden soll. Verwenden Sie die Informationen in der Datei **Jobname\>_Find_\<DateTimeStamp. CSV** (created in Step) 1, um die CSV-Zuordnungsdatei zu erstellen. 
  
Schrittweise Anleitungen zum Importieren von PST-Dateien in Office 365 finden Sie in einem der folgenden Themen:
  
- [Verwenden des Netzwerkuploads zum Importieren von PST-Dateien in Office 365](use-network-upload-to-import-pst-files.md)
    
- [Verwenden des Laufwerkversands zum Importieren von PST-Dateien in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>Schritt 5: Löschen der PST-Dateien, die in Ihrem Netzwerk gefunden wurden

Nachdem die PST-Dateien, die Sie gefunden und gesammelt haben, in Exchange Online-Postfächer in Office 365 importiert wurden, können Sie das PST-Sammlungs Tool verwenden, um die PST-Dateien aus den ursprünglichen Quellspeicherorten zu löschen, an denen Sie in Schritt 1 gefunden wurden. 
  
1. Öffnen Sie auf dem lokalen Computer eine EingabeaufForderungen (als Administrator ausführen).
    
2. Wechseln Sie zu dem Verzeichnis, in das Sie das PST-Sammlungs Tool heruntergeladen haben.
    
3. Führen Sie den folgenden Befehl aus, um die PST-Dateien zu löschen.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    In der folgenden Tabelle werden die Parameter und die erforderlichen Werte beschrieben, wenn Sie den Befehl DataCollectorMaster. exe ausführen, um PST-Dateien zu löschen. 
    
    |Parameter * * * *|****Beschreibung****|Beispiele * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Gibt den Typ der zu suchenden Daten an. Derzeit können Sie das PST-Sammlungs Tool verwenden, um nach PST-Dateien zu suchen. ![um](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Gibt die Art der Operation an, die vom Tool ausgeführt wird. Verwenden Sie den `Delete` Wert, um die PST-Dateien zu löschen, die beim Ausführen des Tools im Suchmodus gefunden wurden.<br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |Gibt den Namen eines vorhandenen PST-Sammlungs Auftrags an. Sie müssen denselben Auftragsnamen verwenden, den Sie beim Ausführen des Tools im Suchmodus und im Sammlungsmodus in Schritt 1 und Schritt 3 verwendet haben. Dieser Auftragsname wird auch dem Namen der Protokolldatei hinzugefügt, die erstellt wird, wenn Sie das Tool im Löschmodus ausführen.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Gibt den Ordner an, der die XML-Konfigurationsdatei enthält, die beim Ausführen des Tools im Sammlungsmodus erstellt wurde. Verwenden Sie den gleichen Wert, den Sie für diesen Parameter in Schritt 3 verwendet haben.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Gibt den Ordner an, in den die Protokolldatei für den Löschmodus kopiert wird. Dies ist ein optionaler Parameter. Wenn Sie Sie nicht hinzufügen, wird die Protokolldatei in den Ordner kopiert, in den Sie das PST-Sammlungs Tool heruntergeladen haben. Erwägen Sie die Verwendung desselben Protokollspeicherorts, den Sie beim Ausführen des Tools in den Modi suchen und erfassen in Schritt 1 und Schritt 3 verwendet haben, damit alle Protokolldateien im selben Ordner gespeichert werden.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Mit dieser optionalen Option können Sie das Tool im Löschmodus für einen vorhandenen PST-Sammelauftrag erneut ausführen. Wenn Sie das Tool zuvor im Löschmodus ausgeführt, aber das Tool dann erneut im Suchmodus ausgeführt haben und die `ForceRestart` Option zum erneuten Scannen von Speicherorten für PST-Dateien verwendet haben, können Sie diese Option verwenden, um das Tool im Löschmodus erneut auszuführen und die PST-Dateien zu löschen, die gefunden wurden, als Ihr re-SCA nned die Standorte. Wenn Sie die `ForceRestart` Option im Löschmodus verwenden, ignoriert das Tool alle vorherigen Löschvorgänge und versucht erneut, die PST-Dateien zu löschen.<br/> | `-ForceRestart` <br/> 

    NachFolgend finden Sie ein Beispiel für die Syntax für das DataCollectorMaster. exe-Tool, das die tatsächlichen Werte für jeden Parameter verwendet:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    Nachdem Sie den Befehl ausgeführt haben, werden detaillierte Statusmeldungen angezeigt, die den Fortschritt des Löschens der PST-Dateien anzeigen, die in Schritt 1 gefunden und in Schritt 3 gesammelt wurden. Nach einer Weile wird eine endgültige Statusmeldung angezeigt, wenn Fehler aufgetreten sind und der Speicherort, in den das Protokoll kopiert wird. Die gleichen Statusmeldungen werden in die Log-Datei kopiert.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>Ergebnisse der DataCollectorMaster. exe im Löschmodus

Nachdem Sie DataCollectorMaster. exe erfolgreich im Löschmodus ausgeführt haben, werden die folgenden Dateien in dem durch die `LogLocation` Parameter und `ConfigurationLocation` angegebenen Ordner gespeichert. 
  
- **\<Jobname\>__ DELETE\<DateTimeStamp\>. log** – die Protokolldatei enthält die Statusmeldungen, die angezeigt wurden. Diese Datei wird in dem durch den `LogLocation` -Parameter angegebenen Ordner erstellt. 
    
- **\<Jobname\>__ DELETE\<DateTimeStamp\>. XML** – die XML-Datei enthält nur Informationen zu den Parameterwerten, die von dem Tool im Löschmodus verwendet wurden. Außerdem werden der Name und der Dateipfad jeder gelöschten PST-Datei aufgelistet. Diese Datei wird in dem durch den `ConfigurationLocation` -Parameter angegebenen Ordner erstellt. 

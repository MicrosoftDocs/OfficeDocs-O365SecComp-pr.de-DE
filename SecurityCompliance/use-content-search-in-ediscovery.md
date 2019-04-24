---
title: Verwenden der Inhaltssuche im eDiscovery-Workflow
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Verwenden Sie ein PowerShell-Skript, um eine in-Place-eDiscovery-Suche in Exchange Online basierend auf einer im Security & Compliance Center erstellten Suche zu erstellen. '
ms.openlocfilehash: 2e4f1b3570ce2400472a0b2a9ddee886ffc4bab3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263797"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a>Verwenden der Inhaltssuche im eDiscovery-Workflow

Mit der Inhaltssuche im Security & Compliance Center können Sie alle Postfächer in Ihrer Organisation durchsuchen. Im Gegensatz zu in-Place eDiscovery in Exchange Online (wo Sie bis zu 10.000 Postfächer durchsuchen können), gibt es keine Begrenzung für die Anzahl von Ziel Postfächern in einer einzelnen Suche. Für Szenarien, in denen organisationsweite Suchen erforderlich sind, können Sie die Inhaltssuche zum Durchsuchen aller Postfächer verwenden. Anschließend können Sie die Workflowfeatures von in-situ-eDiscovery verwenden, um andere eDiscovery-bezogene Aufgaben auszuführen, wie das Speichern von Postfächern und das Exportieren von Suchergebnissen. Angenommen, Sie müssen alle Postfächer durchsuchen, um bestimmte Verwalter zu identifizieren, die auf einen Rechtsfall reagieren. Sie können die Inhaltssuche im Security & Compliance Center verwenden, um alle Postfächer in Ihrer Organisation zu durchsuchen, um diejenigen zu identifizieren, die auf den Fall reagieren. Dann können Sie diese Liste der Depot Postfächer als Quellpostfächer für eine in-Place-eDiscovery-Suche in Exchange Online verwenden. Mithilfe von in-situ-eDiscovery können Sie auch diese Quellpostfächer einhalten, Suchergebnisse in ein Discovery-Postfach kopieren und die Suchergebnisse exportieren.
  
Dieses Thema enthält ein Skript, das Sie zum Erstellen einer in-Place-eDiscovery-Suche in Exchange Online ausführen können, indem Sie die Liste der Quellpostfächer und die Suchabfrage aus einer im Security & Compliance Center erstellten Suche verwenden. Im Folgenden finden Sie eine Übersicht über den Vorgang:
  
[Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfach in Ihrer Organisation](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[Schritt 2: Herstellen einer Verbindung mit \& dem Security Compliance Center und Exchange Online in einer einzigen Remote-PowerShell-Sitzung](#step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[Step 4: Start the In-Place eDiscovery search](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a>Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation

Der erste Schritt besteht darin, das Security & Compliance Center (oder Security & Compliance Center PowerShell) zum Erstellen einer Inhaltssuche zu verwenden, die alle Postfächer in Ihrer Organisation durchsucht. Es gibt keine Begrenzung für die Anzahl der Postfächer für eine einzelne Inhaltssuche. Geben Sie eine geeignete Stichwortabfrage (oder eine Abfrage für vertrauliche Informationstypen) an, damit die Suche nur die Quellpostfächer zurückgibt, die für Ihre Untersuchung relevant sind. Verfeinern Sie bei Bedarf die Suchabfrage, um den Umfang der zurückgegebenen Suchergebnisse und Quellpostfächer einzuschränken.
  
> [!NOTE]
> Wenn die Quellinhaltssuche keine Ergebnisse liefert, wird In-Situ-eDiscovery nicht erstellt, wenn Sie das Skript in Schritt 3 ausführen. Sie müssen die Suchabfrage möglicherweise überarbeiten und die Inhaltssuche erneut ausführen, damit Suchergebnisse zurückgegeben werden. 
  
### <a name="use-the-security--compliance-center-to-search-all-mailboxes"></a>Verwenden des Security & Compliance Center zum Durchsuchen aller Postfächer

1. [Wechseln Sie zum Security _AMP_ Compliance Center](go-to-the-securitycompliance-center.md). 
    
2. Klicken Sie auf **Such** > **Inhaltssuche**, und klicken Sie dann auf](media/O365-MDM-CreatePolicy-AddIcon.gif) **Neues Such** ![Symbol hinzufügen.
    
3. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. 
    
4. Klicken Sie unter **Wo sollen wir suchen?** auf **Alle Postfächer durchsuchen**, und klicken Sie dann auf **Weiter**.
    
5. Geben Sie im Feld unter **Wonach sollen wir für Sie suchen?** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise AND, OR, NOT oder NEAR, oder Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Nachrichten suchen. Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
6. Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten. 
    
    Eine Schätzung der Suchergebnisse, die im Detailbereich angezeigt werden. Dieser umfasst die Gesamtgröße und die Gesamtanzahl der in den Suchergebnissen zurückgegebenen Elemente. Wenn die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzeigen. Klicken Sie ****![gegebenenfalls auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren, um die Informationen im Detailbereich zu aktualisieren. 
    
7.  Verfeinern Sie ggf. die Suchabfrage, um die Suchergebnisse einzugrenzen, und starten Sie die Suche neu. 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a>Verwenden der Security & Compliance Center-PowerShell zum Durchsuchen aller Postfächer

Sie können auch das **New-ComplianceSearch**-Cmdlet zum Durchsuchen aller Postfächer in Ihrer Organisation verwenden. Der erste Schritt besteht darin, [eine Verbindung mit Security _AMP_ Compliance Center PowerShell herzustellen](https://go.microsoft.com/fwlink/p/?LinkID=627084).
  
NachFolgend finden Sie ein Beispiel für die Verwendung von PowerShell zum Durchsuchen aller Postfächer in Ihrer Organisation. Die Suchabfrage gibt alle zwischen dem 1. Januar 2015 und dem 30. Juni 2015 gesendeten Nachrichten zurück, die den Ausdruck "Finanzbericht" in der Betreffzeile enthalten. Der erste Befehl erstellt die Suche, und der zweite Befehl führt die Suche aus. 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

Weitere Informationen finden Sie unter [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a>Überprüfen der Anzahl der Quellpostfächer in der Inhaltssuche

Eine Inhaltssuche gibt maximal 1.000 Quellpostfächer zurück, die Suchergebnisse enthalten. Wenn es mehr als 1.000 Postfächer gibt, die Inhalte enthalten, die mit der Suchabfrage übereinstimmen, sind nur die Top 1.000-Postfächer mit den meisten Suchergebnissen in der Inhaltssuche enthalten, die Sie im vorherigen Schritt erstellt haben. Wenn also mehr als 1.000 Postfächer Suchergebnisse enthalten, werden einige dieser Postfächer nicht in die Liste der Quellpostfächer aufgenommen, die in die in Schritt 3 erstellte neue in-Place-eDiscovery-Suche kopiert wurden. 
  
Führen Sie die folgenden Schritte aus, um eine Inhaltssuche mit nicht mehr als 1.000 Quellpostfächern zu erstellen, um ein Skript mit der Anzahl der Quellpostfächer (die Suchergebnisse enthalten) anzuzeigen, die von der Inhaltssuche zurückgegeben werden, die Sie in Schritt 1 erstellt haben. 
  
1. Speichern Sie den folgenden Text in einer PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Sie können Sie beispielsweise in einer Datei mit dem Namen `SourceMailboxes.ps1`speichern.
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
                  "Please wait until the search finishes.";
                  break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
                  "The Content Search " + $SearchName + " didn't return any useful results.";
                  break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  "Number of mailboxes that have search hits: " + $mailboxes.Count
  ```

2. Wechseln Sie in Security & Compliance Center PowerShell zu dem Ordner, in dem sich das im vorherigen Schritt erstellte Skript befindet, und führen Sie das Skript aus; Zum Beispiel:
    
    ```
    .\SourceMailboxes.ps1
    ```

3. Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, die in Schritt 1 erstellte Inhaltssuche ein.
    
    Das Skript zeigt die Anzahl der Quellpostfächer, die Suchergebnisse enthalten.
    
Wenn mehr als 1.000 Quellpostfächer vorhanden sind, versuchen Sie, zwei (oder mehr) Inhalts suchVorgänge zu erstellen. Suchen Sie beispielsweise die Hälfte der Postfächer Ihrer Organisation in einer Inhaltssuche und die andere Hälfte in einer anderen Inhaltssuche. Sie können auch die Suchkriterien ändern, um die Anzahl der Postfächer zu verringern, die Suchergebnisse enthalten. Sie können beispielsweise einen Datums Umfang einbeziehen oder die Stichwortabfrage verfeinern.
  
## <a name="step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Schritt 2: Herstellen einer Verbindung mit \& dem Security Compliance Center und Exchange Online in einer einzigen Remote-PowerShell-Sitzung

Der nächste Schritt besteht darin, Windows PowerShell sowohl mit dem Security & Compliance Center als auch mit Ihrer Exchange Online-Organisation zu verbinden. Dies ist erforderlich, da das Skript, das Sie in Schritt 3 ausführen, Zugriff auf die Cmdlets für die Inhaltssuche im Security & Compliance Center und in den in-Place eDiscovery-Cmdlets in Exchange Online benötigt.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamensuffixes „.ps1". Sie können Sie beispielsweise in einer Datei mit dem Namen `ConnectEXO-CC.ps1`speichern.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:
    
    ```
    .\ConnectEXO-CC.ps1
    ```

Woher wissen Sie, dass dieses Verfahren erfolgreich war? Nachdem Sie das Skript ausgeführt haben, werden Cmdlets aus dem Security & Compliance Center und Exchange Online in Ihre lokale PowerShell-Sitzung importiert. Wenn Sie keine Fehlermeldungen erhalten, wurde die Verbindung erfolgreich hergestellt. Ein kurzer Test ist die Ausführung eines Security & Compliance Center-Cmdlets, beispielsweise **install-UnifiedCompliancePrerequisite** und eines Exchange Online-Cmdlets wie **Get-Mailbox**. 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a>Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche

Nachdem Sie die duale PowerShell-Sitzung in Schritt 2 erstellt haben, besteht der nächste Schritt darin, ein Skript auszuführen, das eine vorhandene Inhaltssuche in eine in-Place-eDiscovery-Suche konvertiert. Das Skript führt Folgendes aus:
  
- Es fordert Sie auf, den Namen der zu konvertierenden Inhaltssuche anzugeben.
    
- Es stellt sicher, dass die Inhaltssuche abgeschlossen wird. Wenn die Compliancesuche keine Ergebnisse zurückgibt, wird In-Situ-eDiscovery nicht erstellt.
    
- Speichert eine Liste der Quellpostfächer aus der Inhaltssuche mit den Suchergebnissen in einer Variablen.
    
- Erstellt eine neue In-Situ-eDiscovery-Suche mit den folgenden Eigenschaften. Beachten Sie, dass die neue Suche noch nicht gestartet wurde. Sie werden diese in Schritt 4 starten.
    
  - **Name** -der Name der neuen Suche verwendet dieses Format: \<Name der Inhaltssuche\>_MBSearch1. Wenn Sie das Skript erneut ausführen und dieselbe Quellinhalts Suche verwenden, wird die Suche mit \<dem Namen Name der Inhaltssuche\>_MBSearch2.
    
  - **Quellpostfächer** – alle Postfächer aus der Inhaltssuche, die Suchergebnisse enthalten. 
    
  - **Suchabfrage** : die neue Suche verwendet die Suchabfrage aus der Inhaltssuche. Berücksichtigt die Inhaltssuche alle Inhalte (leere Suchabfrage), so ist in der neuen Suche die Suchabfrage leer und es werden alle in den Quellpostfächern enthaltenen Inhalte berücksichtigt. 
    
  - **Suche nur schätzen** -die neue Suche wird als reine schätzungs Suche gekennzeichnet. Die Suchergebnisse werden nicht in ein Discoverypostfach kopiert, nachdem Sie es starten. 
    
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamensuffixes „.ps1". Sie können Sie beispielsweise in einer Datei mit dem Namen `CreateMBSearchFromComplianceSearch.ps1`speichern.
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName,
      [switch]$original,
      [switch]$restoreOriginal
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
    "Please wait until the search finishes";
    break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
    "The Content Search " + $SearchName + " didn't return any useful results";
    "A mailbox search object wasn't created";
    break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  $msPrefix = $SearchName + "_MBSearch";
  $I = 1;
  $mbSearches = Get-MailboxSearch;
  while ($true)
  {
      $found = $false;
      $mbsName = "$msPrefix$I";
      foreach ($mbs in $mbSearches)
      {
          if ($mbs.Name -eq $mbsName)
          {
              $found = $true;
              break;
          }
      }
      if (!$found)
      {
          break;
      }
      $I++;
  }
  $query = $search.KeywordQuery;
  if ([string]::IsNullOrWhiteSpace($query))
  {
      $query = $search.ContentMatchQuery;
  }
  if ([string]::IsNullOrWhiteSpace($query))
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -EstimateOnly;
  }
  else
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -SearchQuery $query -EstimateOnly;
  }
  
  ```

2. Wechseln Sie in der Windows PowerShell-Sitzung, die Sie in Schritt 2 erstellt haben, zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, den Namen der Inhaltssuche ein, die Sie für eine in-Place-eDiscovery-Suche (beispielsweise die in Schritt 1 erstellte Suche) erfassen möchten, und drücken Sie dann die **Eingabe**Taste.
    
    Wenn das Skript erfolgreich ausgeführt wird, wird eine neue In-Situ-eDiscovery-Suche mit dem Status **NotStarted** erstellt. Führen Sie den Befehl  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` aus, um die Eigenschaften der neuen Suche anzuzeigen. 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a>Schritt 4: Starten der In-Situ-eDiscovery-Suche

Das Skript, das Sie in Schritt 3 ausführen, erstellt eine neue Compliance-eDiscovery-Suche, startet diese aber nicht. Der nächste Schritt ist das Starten der Suche, damit Sie eine Schätzung der Suchergebnisse abrufen können.
  
1. Navigieren Sie in Exchange-Verwaltungskonsole (EAC) zu **Verwaltung der Compliance** \> **Compliance-eDiscovery &amp; Compliance-Archive**.
    
2. Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.
    
3. ![Klicken **** Sie auf Such](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> Suchsymbol, um die Suchergebnisse zu **schätzen** , um die Suche zu starten und eine Schätzung der Gesamtgröße und Anzahl der von der Suche zurückgegebenen Elemente zurückzugeben. 
    
    Die Schätzungen werden im Detailbereich angezeigt. Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Informationen im Detailbereich zu aktualisieren. **** ![ 
    
4. Um eine Vorschau der Ergebnisse anzuzeigen, nachdem die Suche abgeschlossen ist, klicken Sie im Detailbereich auf **Vorschau der Suchergebnisse anzeigen**.
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a>Nächste Schritte nach dem Erstellen und Ausführen der In-Situ-eDiscovery-Suche

Nach dem Erstellen und Starten der In-Situ-eDiscovery-Suche, die mit dem Skript in Schritt 3 erstellt wurde, können Sie den normalen In-Situ-eDiscovery-Workflow zum Durchführen verschiedener eDiscovery-Aktionen an den Suchergebnissen verwenden.
  
### <a name="create-an-in-place-hold"></a>Erstellen eines In-Situ-Archivs

1. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Wählen Sie in der Listenansicht die in-Place-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt **** ![haben, und](media/O365_MDM_CreatePolicy_EditIcon.gif)klicken Sie dann auf Bearbeitungssymbol bearbeiten.
    
3. Aktivieren Sie auf der Seite **Compliance-Archive** das Kontrollkästchen **Inhalt, der in ausgewählten Postfächern mit der Suchabfrage übereinstimmt, aufbewahren**, und wählen Sie eine der folgenden Optionen: 
    
  - **Unbegrenzt halten** – wählen Sie diese Option aus, um von der Suche zurückgegebene Elemente unbegrenzt zu speichern. Aufbewahrte Elemente werden solange beibehalten, bis Sie das Postfach aus der Suche entfernt oder die Suche entfernt haben. 
    
  - **Geben Sie die Anzahl von Tagen an, die Elemente im Verhältnis zu Ihrem Empfangsdatum enthalten** sollen: Wählen Sie diese Option aus, um Elemente für einen bestimmten Zeitraum aufzubewahren. Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde. 
    
4. Klicken Sie auf **Speichern**, um das Compliance-Archiv zu erstellen und die Suche neu zu starten. 
    
[Return to top](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a>Kopieren der Suchergebnisse

1. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Wählen Sie in der Listenansicht die In-Situ-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.
    
3. Klicken **** ![Sie auf Such](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)Suchsymbol suchen, und klicken Sie dann in der Dropdownliste auf **Suchergebnisse kopieren** . 
    
4. Wählen Sie unter **Suchergebnisse kopieren** aus den folgenden Optionen:
    
    - Nicht durch **Such Bare Elemente einbeziehen** – aktivieren Sie dieses Kontrollkästchen, um Postfachelemente einzuschließen, die nicht durchsucht werden konnten (beispielsweise Nachrichten mit Anlagen von Dateitypen, die nicht von der Exchange-Suche indiziert werden konnten). 
    
    - **DeduplizierUng aktivieren** -aktivieren Sie dieses Kontrollkästchen, um doppelte Nachrichten auszuschließen. Es wird nur eine einzelne Instanz einer Nachricht in das Discovery-Postfach kopiert. 
    
    - **Vollständige Protokollierung aktivieren** : Aktivieren Sie dieses Kontrollkästchen, um ein vollständiges Protokoll in die Suchergebnisse einzuschließen. 
    
    - E-Mail nach **Abschluss des kopierVorgangs senden** – aktivieren Sie dieses Kontrollkästchen, um eine e-Mail-Benachrichtigung zu erhalten, wenn die Suche abgeschlossen ist. 
    
    - **Ergebnisse in dieses Discovery-Postfach kopieren** – klicken Sie auf **Durchsuchen** , um das Ermittlungspostfach auszuwählen, in das die Suchergebnisse kopiert werden sollen. 
    
5. Klicken Sie auf **Kopieren**, um den Prozess zum Kopieren der Suchergebnisse in das angegebene Discoverypostfach zu starten. 
    
6. Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Informationen über den Kopierstatus zu aktualisieren, die im Detailbereich angezeigt werden. **** ![ 
    
7. Wenn der Kopiervorgang abgeschlossen ist, klicken Sie auf **Öffnen**, um das Discoverypostfach zu öffnen und die Suchergebnisse anzuzeigen. 
  
### <a name="export-the-search-results"></a>Exportieren der Suchergebnisse

1. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
2. Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben, und klicken Sie anschließend auf **In eine PST-Datei exportieren**.
    
3. Gehen Sie im Fenster **eDiscovery-PST-Exporttool** folgendermaßen vor: 
    
    - Klicken Sie auf **Durchsuchen**, und geben Sie das Verzeichnis an, in das die PST-Datei heruntergeladen werden soll. 
    
    - Klicken Sie auf das Kontrollkästchen **Entfernung von Duplikaten aktivieren**, um doppelte Nachrichten auszuschließen. Es wird nur eine einzelne Instanz einer Nachricht in die PST-Datei aufgenommen. 
    
    - Wählen Sie das Kontrollkästchen **Nicht durchsuchbare Elemente einschließen** aus, um Postfachelemente zu berücksichtigen, die nicht durchsucht werden konnten (z. B. Nachrichten mit Anhängen, die Dateitypen enthalten, die von der Exchange-Suche nicht indiziert werden konnten). Nicht durchsuchbare Elemente werden in eine separate PST-Datei exportiert. 
    
4. Klicken Sie auf **Start**, um die Suchergebnisse in eine PST-Datei zu exportieren. 
    
    Es wird ein Fenster angezeigt, das Statusinformationen über den Exportvorgang anzeigt.

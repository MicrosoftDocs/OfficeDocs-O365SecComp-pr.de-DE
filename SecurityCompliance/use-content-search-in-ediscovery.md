---
title: Verwenden der Inhaltssuche im eDiscovery-Workflow
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Verwenden Sie ein PowerShell-Skript zum Erstellen einer Compliance-eDiscovery-Suche in Exchange Online basierend auf einer Suche in der Office 365-Sicherheit erstellten &amp; Compliance Center. '
ms.openlocfilehash: d2f4f845e8c819eed67c3a234bff208a11fb571c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529513"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a>Verwenden der Inhaltssuche im eDiscovery-Workflow

Das Inhaltssuche-Feature in die Office 365-Sicherheit &amp; Compliance Center können Sie alle Postfächer in Ihrer Organisation zu suchen. Im Gegensatz zu Compliance-eDiscovery in Exchange Online (in dem Sie bis zu 10.000 Postfächer suchen können), gibt es keine Grenzwerte für die Anzahl der Postfächer in einem einzelnen Suchvorgang Ziel. Für Szenarien, die Sie organisationsweiten Suchvorgänge ausführen müssen, können Sie Inhaltssuche verwenden, um alle Postfächer zu suchen. Anschließend können Sie die Workflowfeatures von Compliance-eDiscovery für andere eDiscovery-bezogene, Aufgaben wie das Platzieren Postfächer auf halten und ausführenden Suchergebnisse verwenden. Nehmen wir beispielsweise an, mit denen Sie suchen, um bestimmte Verwalter zu ermitteln, die auf eine rechtliche Anfrage reagieren, sind alle Postfächer. Sie können Inhaltssuche in das Wertpapier &amp; Compliance Center, um alle Postfächer in Ihrer Organisation, die identifizieren, die auf die Groß-/Kleinschreibung reagieren, werden zu suchen. Klicken Sie dann können Sie dieser Liste der Postfächer Verwaltungsberechtigter als die Quellpostfächer für eine Compliance-eDiscovery-Suche in Exchange Online verwenden. Verwenden von Compliance-eDiscovery hinaus können Sie diese Quellpostfächer zurückstellen, Suchergebnisse in ein discoverypostfach kopieren und die Suchergebnisse exportieren.
  
Dieses Thema enthält ein Skript, das Sie zum Erstellen einer Compliance-eDiscovery-Suche in Exchange Online mithilfe der Liste der Quellpostfächer und Suchabfrage aus einer Suche in das Wertpapier erstellt ausführen können &amp; Compliance Center. Es folgt eine Übersicht über den Prozess:
  
[Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[Schritt 2: Verbinden mit der Sicherheit &amp; Compliance Center und Exchange Online in einer einzigen remote-PowerShell-Sitzung](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[Schritt 4: Starten der In-Situ-eDiscovery-Suche](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a>Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation

Der erste Schritt besteht, verwenden Sie die Sicherheit &amp; Compliance Center (oder Sicherheit & Compliance Center PowerShell) eine Inhaltssuche erstellen, das alle Postfächer in Ihrer Organisation durchsucht. Es gibt keine Beschränkung für die Anzahl von Postfächern für eine einzelne Inhaltssuche. Geben Sie eine entsprechende Schlüsselwort-Abfrage (oder eine Abfrage nach vertraulichen Informationstypen), sodass die Suche nur diese Quellpostfächer zurückgibt, die für Ihre Untersuchung relevant sind. Optimieren Sie bei Bedarf die Suchabfrage zum Einschränken des Bereichs der Suchergebnisse und Quellpostfächer, die zurückgegeben werden.
  
> [!NOTE]
> Wenn die Quellinhaltssuche keine Ergebnisse liefert, wird In-Situ-eDiscovery nicht erstellt, wenn Sie das Skript in Schritt 3 ausführen. Sie müssen die Suchabfrage möglicherweise überarbeiten und die Inhaltssuche erneut ausführen, damit Suchergebnisse zurückgegeben werden. 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a>Verwenden Sie die Sicherheit &amp; Compliance Center, um alle Postfächer zu suchen.

1. [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md). 
    
2. Klicken Sie auf **Suche &amp; Untersuchung**, klicken Sie auf **Inhaltssuche**und klicken Sie dann auf **New** ![Symbol hinzufügen](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
3. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. 
    
4. Klicken Sie unter **Wo sollen wir suchen?** auf **Alle Postfächer durchsuchen**, und klicken Sie dann auf **Weiter**.
    
5. Im Feld unter **Was möchten Sie uns suchen?**, geben Sie in das Feld eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Können Sie eine komplexere Abfragen, die einen booleschen Operators, wie AND, OR nicht verwenden oder in der Nähe, oder Sie können auch in Nachrichten vertrauliche Informationen (wie Sozialversicherungsnummern) suchen. Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Stichwortabfragen Content-Suche](keyword-queries-and-search-conditions.md).
    
6. Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten. 
    
    Nach einer gewissen eine Schätzung der Suchergebnisse im Detailfenster angezeigt. Die Schätzung für das enthält die Gesamtgröße und-Anzahl der Objekte für die Suchergebnisse an. Nachdem die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzuzeigen. Klicken Sie auf **Aktualisieren**, falls erforderlich,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich. 
    
7.  Verfeinern Sie ggf. die Suchabfrage, um die Suchergebnisse einzugrenzen, und starten Sie die Suche neu. 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a>Verwenden Sie Sicherheit und Compliance Center PowerShell, um alle Postfächer suchen

Sie können auch das Cmdlet " **New-ComplianceSearch** " verwenden, um alle Postfächer in Ihrer Organisation zu suchen. Der erste Schritt besteht darin, [Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).
  
Es folgt ein Beispiel der Verwendung von PowerShell um alle Postfächer in Ihrer Organisation zu suchen. Die Suchabfrage zurückgibt, dass alle Nachrichten, die zwischen dem 1. Januar 2015 und 30 Juni 2015 gesendet und, die den Ausdruck "finanzielle Report" in der Betreffzeile enthalten. Der erste Befehl erstellt die Suche, und im zweite Befehl wird die Suche ausgeführt. 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

Weitere Informationen finden Sie unter [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a>Überprüfen der Anzahl der Quellpostfächer in der Inhaltssuche

Eine Inhaltssuche gibt maximal 1.000 Quellpostfächer, die Suchergebnisse enthalten. Wenn mehr als 1.000 Postfächer, die Inhalte enthalten, die die Suchabfrage entspricht vorhanden sind, sind nur die oberen 1.000 Postfächer mit den meisten Suchergebnissen in die Suche Inhalte enthalten, die Sie im vorherigen Schritt erstellt haben. So mehr als 1000 Postfächer Suchergebnisse enthalten, nicht einige dieser Postfächer in der Liste der in die neue Compliance-eDiscovery-Suche in Schritt 3 erstellte kopiert Quellpostfächer berücksichtigt. 
  
Zum Ausführen eines Skripts, das zeigt die Anzahl der Quellpostfächer (die Suchergebnisse enthalten) zurückgegeben, die für die Inhaltssuche, die Sie in Schritt 1 erstellten folgendermaßen Sie vor, um Sie beim Erstellen einer Inhaltssuche mit nicht mehr als 1.000 Quellpostfächer unterstützen. 
  
1. Speichern Sie den folgenden Text in einer PowerShell-Skriptdatei mithilfe von Filename Suffix. ps1. Angenommen, Sie konnte speichern in eine Datei namens `SourceMailboxes.ps1`.
    
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

2. Sicherheit und Compliance Center PowerShell wechseln Sie zu dem Ordner, in dem das Skript im vorherigen Schritt erstellten befindet, und führen Sie das Skript; Zum Beispiel:
    
    ```
    .\SourceMailboxes.ps1
    ```

3. Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, die in Schritt 1 erstellte Inhaltssuche ein.
    
    Das Skript zeigt die Anzahl der Quellpostfächer, die Suchergebnisse enthalten.
    
Wenn mehr als 1.000 Quellpostfächer vorhanden sind, versuchen Sie zwei (oder mehrere) Content-Suche zu erstellen. Suchen Sie beispielsweise die Hälfte der Postfächer Ihrer Organisation in eine Inhaltssuche und die andere Hälfte in einem anderen Inhaltssuche. Sie könnten auch zur Verringerung der Anzahl von Postfächern, die Suchergebnisse enthalten die Suchkriterien ändern. Beispielsweise können Sie einen Datumsbereich ein- oder verfeinern der Stichwortabfrage.
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Schritt 2: Verbinden mit der Sicherheit &amp; Compliance Center und Exchange Online in einer einzigen remote-PowerShell-Sitzung

Im nächsten Schritt wird Windows PowerShell sowohl die Sicherheit Verbindung &amp; Compliance Center und Ihre Exchange Online-Organisation. Dies ist erforderlich, da das Skript, das Sie in Schritt 3 ausführen, Zugriff auf die Inhaltssuche-Cmdlets in das Wertpapier erfordert &amp; Compliance Center und die Compliance-eDiscovery-Cmdlets in Exchange Online.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe von Filename Suffix. ps1. Angenommen, Sie konnte speichern in eine Datei namens `ConnectEXO-CC.ps1`.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript; Zum Beispiel:
    
    ```
    .\ConnectEXO-CC.ps1
    ```

Woher wissen Sie, ob dies funktioniert? Nach dem Ausführen des Skripts,-Cmdlets auf die Sicherheit &amp; Compliance Center und Exchange Online in Ihre lokale PowerShell-Sitzung importiert werden. Wenn Sie keine Fehler erhalten, verbunden Sie erfolgreich. Ein schnelles Test ist zum Ausführen eines Wertpapiers &amp; Compliance Center-Cmdlet – beispielsweise **Install-UnifiedCompliancePrerequisite** – und einer Exchange Online-Cmdlets wie **Get-Mailbox**. 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a>Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche

Nachdem die duale PowerShell-Sitzung in Schritt2 erstellt wurde, besteht der nächste Schritt das Ausführen eines Skripts, das in einer Compliance-eDiscovery-Suche eine vorhandene Inhaltssuche konvertiert wird. Hier wird die Funktionsweise des Skripts:
  
- Es fordert Sie auf, den Namen der zu konvertierenden Inhaltssuche anzugeben.
    
- Es stellt sicher, dass die Inhaltssuche abgeschlossen wird. Wenn die Compliancesuche keine Ergebnisse zurückgibt, wird In-Situ-eDiscovery nicht erstellt.
    
- Speichert eine Liste der Quellpostfächer aus der Inhaltssuche mit den Suchergebnissen in einer Variablen.
    
- Erstellt eine neue In-Situ-eDiscovery-Suche mit den folgenden Eigenschaften. Beachten Sie, dass die neue Suche noch nicht gestartet wurde. Sie werden diese in Schritt 4 starten.
    
  - **Name** – der Name der neuen Suche verwendet dieses Format: \<Name des Inhaltssuche\>_MBSearch1. Wenn Sie das Skript erneut ausführen und die gleiche Quelle Inhaltssuche verwenden, wird die Suche namens \<Name des Inhaltssuche\>_MBSearch2.
    
  - **Quellpostfächer** - alle Postfächer aus der Inhaltssuche, die Suchergebnisse enthalten. 
    
  - **Suchabfrage** - neue Suche wird die Suchabfrage aus der Inhaltssuche verwendet. Enthält Inhalt für die Suche alle Inhalte (, die die Suchabfrage leer ist) wird die neue Suche müssen auch eine leere Search-Abfrage und enthält alle Inhalte, die in der Quellpostfächer gefunden. 
    
  - **Schätzen Sie nur Search** - neue Suche ist mit einer Suche Estimate-only gekennzeichnet. Es wird nicht Suchergebnisse in ein discoverypostfach kopieren, nachdem Sie den Workflow starten. 
    
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe von Filename Suffix ps1. Angenommen, Sie konnte speichern in eine Datei namens `CreateMBSearchFromComplianceSearch.ps1`.
    
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

2. In der Windows PowerShell-Sitzung, die Sie in Schritt2 erstellt haben, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript. Zum Beispiel:
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. Bei Aufforderung durch das Skript Geben Sie den Namen des Content-Suche, die Sie konvertieren zu einer Compliance-eDiscovery-Suche (beispielsweise die Suche, die Sie in Schritt 1 erstellt) möchten, und drücken Sie die **EINGABETASTE**.
    
    Wenn das Skript erfolgreich ausgeführt wird, wird eine neue In-Situ-eDiscovery-Suche mit dem Status **NotStarted** erstellt. Führen Sie den Befehl  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` aus, um die Eigenschaften der neuen Suche anzuzeigen. 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a>Schritt 4: Starten der In-Situ-eDiscovery-Suche

Mit dem Skript, das Sie in Schritt 3 ausführen, wird eine neue In-Situ-eDiscovery-Suche erstellt, jedoch nicht gestartet. Im nächsten Schritt wird die Suche gestartet, damit Sie eine Schätzung der Suchergebnisse abrufen können.
  
1. Navigieren Sie in Exchange-Verwaltungskonsole (EAC) zu **Verwaltung der Compliance** \> **Compliance-eDiscovery &amp; Compliance-Archive**.
    
2. Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.
    
3. Klicken Sie auf **Suche** ![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Schätzung der Suchergebnisse** auf die Suche starten und eine Schätzung der Gesamtgröße und Anzahl der Elemente, die von der Suche zurückgegebenen zurückzugeben. 
    
    Die Schätzungen werden im Detailfenster angezeigt. Klicken Sie auf **Aktualisieren** ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich angezeigt. 
    
4. Um eine Vorschau der Ergebnisse anzuzeigen, nachdem die Suche abgeschlossen ist, klicken Sie im Detailbereich auf **Vorschau der Suchergebnisse anzeigen**.
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a>Nächste Schritte nach dem Erstellen und Ausführen der In-Situ-eDiscovery-Suche

Nach dem Erstellen und Starten der In-Situ-eDiscovery-Suche, die mit dem Skript in Schritt 3 erstellt wurde, können Sie den normalen In-Situ-eDiscovery-Workflow zum Durchführen verschiedener eDiscovery-Aktionen an den Suchergebnissen verwenden.
  
### <a name="create-an-in-place-hold"></a>Erstellen eines In-Situ-Archivs

1. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
2. In der Listenansicht, wählen Sie die Compliance-eDiscovery-Suche, die Sie in Schritt 3 erstellt haben, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
3. Aktivieren Sie auf der Seite **Compliance-Archive** das Kontrollkästchen **Inhalt, der in ausgewählten Postfächern mit der Suchabfrage übereinstimmt, aufbewahren**, und wählen Sie eine der folgenden Optionen: 
    
  - **In einer Warteschleife verbleibt** - wählen Sie diese Option, um auf eine aufzubewahren von der Suche zurückgegebenen Elemente zu platzieren. Elemente in der Warteschleife bleiben, bis Sie des Postfachs aus der Suche entfernen oder entfernen die Suche erhalten. 
    
  - **Geben Sie Anzahl der Tage speichern Elemente relativ zu ihrer Empfangsdatum** – wählen Sie diese Option, um Elemente für einen bestimmten Zeitraum zu halten. Ein Element Postfach empfangen oder erstellt wird, wird die Dauer ab dem Datum berechnet. 
    
4. Klicken Sie auf **Speichern**, um das Compliance-Archiv zu erstellen und die Suche neu zu starten. 
    
[Zurück zum Seitenanfang](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a>Kopieren der Suchergebnisse

1. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
2. Wählen Sie in der Listenansicht die In-Situ-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.
    
3. Klicken Sie auf **Suche** ![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), und klicken Sie dann auf **Kopieren der Suchergebnisse** aus der Dropdown-Liste. 
    
4. Wählen Sie unter **Suchergebnisse kopieren** aus den folgenden Optionen:
    
    - **Nicht durchsuchbare Elemente einschließen** – aktivieren Sie dieses Kontrollkästchen, Postfachelemente enthalten, die (beispielsweise Nachrichten mit Anlagen mit Dateitypen, die von der Exchange-Suche indiziert werden konnten) konnte nicht durchsucht werden. 
    
    - **Deduplizierung aktivieren** – aktivieren Sie dieses Kontrollkästchen, um doppelte Nachrichten ausschließen. Nur eine einzige Instanz einer Nachricht wird in das discoverypostfach kopiert. 
    
    - **Vollständige Protokollierung aktivieren** – aktivieren Sie dieses Kontrollkästchen, um eine vollständige Protokolldatei in Suchergebnisse einschließen. 
    
    - **Mich bei der Kopiervorgang abgeschlossen ist e-Mail senden** – aktivieren Sie dieses Kontrollkästchen, um eine e-Mail-Benachrichtigung zu erhalten, wenn die Suche abgeschlossen ist. 
    
    - **Ergebnisse in dieser discoverypostfach kopieren** - klicken Sie auf **Durchsuchen** , um das discoverypostfach auszuwählen, die Suchergebnisse angezeigt werden sollen kopiert. 
    
5. Klicken Sie auf **Kopieren**, um den Prozess zum Kopieren der Suchergebnisse in das angegebene Discoverypostfach zu starten. 
    
6. Klicken Sie auf **Aktualisieren** ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) , die Informationen zu den kopieren Status aktualisieren, die im Detailbereich angezeigt wird. 
    
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

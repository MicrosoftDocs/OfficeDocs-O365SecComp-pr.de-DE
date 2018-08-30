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
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="47c08-103">Verwenden der Inhaltssuche im eDiscovery-Workflow</span><span class="sxs-lookup"><span data-stu-id="47c08-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="47c08-p101">Das Inhaltssuche-Feature in die Office 365-Sicherheit &amp; Compliance Center können Sie alle Postfächer in Ihrer Organisation zu suchen. Im Gegensatz zu Compliance-eDiscovery in Exchange Online (in dem Sie bis zu 10.000 Postfächer suchen können), gibt es keine Grenzwerte für die Anzahl der Postfächer in einem einzelnen Suchvorgang Ziel. Für Szenarien, die Sie organisationsweiten Suchvorgänge ausführen müssen, können Sie Inhaltssuche verwenden, um alle Postfächer zu suchen. Anschließend können Sie die Workflowfeatures von Compliance-eDiscovery für andere eDiscovery-bezogene, Aufgaben wie das Platzieren Postfächer auf halten und ausführenden Suchergebnisse verwenden. Nehmen wir beispielsweise an, mit denen Sie suchen, um bestimmte Verwalter zu ermitteln, die auf eine rechtliche Anfrage reagieren, sind alle Postfächer. Sie können Inhaltssuche in das Wertpapier &amp; Compliance Center, um alle Postfächer in Ihrer Organisation, die identifizieren, die auf die Groß-/Kleinschreibung reagieren, werden zu suchen. Klicken Sie dann können Sie dieser Liste der Postfächer Verwaltungsberechtigter als die Quellpostfächer für eine Compliance-eDiscovery-Suche in Exchange Online verwenden. Verwenden von Compliance-eDiscovery hinaus können Sie diese Quellpostfächer zurückstellen, Suchergebnisse in ein discoverypostfach kopieren und die Suchergebnisse exportieren.</span><span class="sxs-lookup"><span data-stu-id="47c08-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="47c08-p102">Dieses Thema enthält ein Skript, das Sie zum Erstellen einer Compliance-eDiscovery-Suche in Exchange Online mithilfe der Liste der Quellpostfächer und Suchabfrage aus einer Suche in das Wertpapier erstellt ausführen können &amp; Compliance Center. Es folgt eine Übersicht über den Prozess:</span><span class="sxs-lookup"><span data-stu-id="47c08-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="47c08-114">Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="47c08-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="47c08-115">Schritt 2: Verbinden mit der Sicherheit &amp; Compliance Center und Exchange Online in einer einzigen remote-PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="47c08-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="47c08-116">Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="47c08-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="47c08-117">Schritt 4: Starten der In-Situ-eDiscovery-Suche</span><span class="sxs-lookup"><span data-stu-id="47c08-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="47c08-118">Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="47c08-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="47c08-p103">Der erste Schritt besteht, verwenden Sie die Sicherheit &amp; Compliance Center (oder Sicherheit & Compliance Center PowerShell) eine Inhaltssuche erstellen, das alle Postfächer in Ihrer Organisation durchsucht. Es gibt keine Beschränkung für die Anzahl von Postfächern für eine einzelne Inhaltssuche. Geben Sie eine entsprechende Schlüsselwort-Abfrage (oder eine Abfrage nach vertraulichen Informationstypen), sodass die Suche nur diese Quellpostfächer zurückgibt, die für Ihre Untersuchung relevant sind. Optimieren Sie bei Bedarf die Suchabfrage zum Einschränken des Bereichs der Suchergebnisse und Quellpostfächer, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="47c08-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="47c08-p104">Wenn die Quellinhaltssuche keine Ergebnisse liefert, wird In-Situ-eDiscovery nicht erstellt, wenn Sie das Skript in Schritt 3 ausführen. Sie müssen die Suchabfrage möglicherweise überarbeiten und die Inhaltssuche erneut ausführen, damit Suchergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="47c08-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="47c08-125">Verwenden Sie die Sicherheit &amp; Compliance Center, um alle Postfächer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="47c08-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="47c08-126">[Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="47c08-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="47c08-127">Klicken Sie auf **Suche &amp; Untersuchung**, klicken Sie auf **Inhaltssuche**und klicken Sie dann auf **New** ![Symbol hinzufügen](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="47c08-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="47c08-128">Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein.</span><span class="sxs-lookup"><span data-stu-id="47c08-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="47c08-129">Klicken Sie unter **Wo sollen wir suchen?** auf **Alle Postfächer durchsuchen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="47c08-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="47c08-p105">Im Feld unter **Was möchten Sie uns suchen?**, geben Sie in das Feld eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Können Sie eine komplexere Abfragen, die einen booleschen Operators, wie AND, OR nicht verwenden oder in der Nähe, oder Sie können auch in Nachrichten vertrauliche Informationen (wie Sozialversicherungsnummern) suchen. Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Stichwortabfragen Content-Suche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="47c08-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="47c08-134">Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="47c08-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="47c08-p106">Nach einer gewissen eine Schätzung der Suchergebnisse im Detailfenster angezeigt. Die Schätzung für das enthält die Gesamtgröße und-Anzahl der Objekte für die Suchergebnisse an. Nachdem die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzuzeigen. Klicken Sie auf **Aktualisieren**, falls erforderlich,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich.</span><span class="sxs-lookup"><span data-stu-id="47c08-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="47c08-139">Verfeinern Sie ggf. die Suchabfrage, um die Suchergebnisse einzugrenzen, und starten Sie die Suche neu.</span><span class="sxs-lookup"><span data-stu-id="47c08-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="47c08-140">Verwenden Sie Sicherheit und Compliance Center PowerShell, um alle Postfächer suchen</span><span class="sxs-lookup"><span data-stu-id="47c08-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="47c08-p107">Sie können auch das Cmdlet " **New-ComplianceSearch** " verwenden, um alle Postfächer in Ihrer Organisation zu suchen. Der erste Schritt besteht darin, [Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="47c08-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="47c08-p108">Es folgt ein Beispiel der Verwendung von PowerShell um alle Postfächer in Ihrer Organisation zu suchen. Die Suchabfrage zurückgibt, dass alle Nachrichten, die zwischen dem 1. Januar 2015 und 30 Juni 2015 gesendet und, die den Ausdruck "finanzielle Report" in der Betreffzeile enthalten. Der erste Befehl erstellt die Suche, und im zweite Befehl wird die Suche ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47c08-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="47c08-146">Weitere Informationen finden Sie unter [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="47c08-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="47c08-147">Überprüfen der Anzahl der Quellpostfächer in der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="47c08-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="47c08-p109">Eine Inhaltssuche gibt maximal 1.000 Quellpostfächer, die Suchergebnisse enthalten. Wenn mehr als 1.000 Postfächer, die Inhalte enthalten, die die Suchabfrage entspricht vorhanden sind, sind nur die oberen 1.000 Postfächer mit den meisten Suchergebnissen in die Suche Inhalte enthalten, die Sie im vorherigen Schritt erstellt haben. So mehr als 1000 Postfächer Suchergebnisse enthalten, nicht einige dieser Postfächer in der Liste der in die neue Compliance-eDiscovery-Suche in Schritt 3 erstellte kopiert Quellpostfächer berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="47c08-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="47c08-151">Zum Ausführen eines Skripts, das zeigt die Anzahl der Quellpostfächer (die Suchergebnisse enthalten) zurückgegeben, die für die Inhaltssuche, die Sie in Schritt 1 erstellten folgendermaßen Sie vor, um Sie beim Erstellen einer Inhaltssuche mit nicht mehr als 1.000 Quellpostfächer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="47c08-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="47c08-p110">Speichern Sie den folgenden Text in einer PowerShell-Skriptdatei mithilfe von Filename Suffix. ps1. Angenommen, Sie konnte speichern in eine Datei namens `SourceMailboxes.ps1`.</span><span class="sxs-lookup"><span data-stu-id="47c08-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
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

2. <span data-ttu-id="47c08-154">Sicherheit und Compliance Center PowerShell wechseln Sie zu dem Ordner, in dem das Skript im vorherigen Schritt erstellten befindet, und führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47c08-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="47c08-155">Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, die in Schritt 1 erstellte Inhaltssuche ein.</span><span class="sxs-lookup"><span data-stu-id="47c08-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="47c08-156">Das Skript zeigt die Anzahl der Quellpostfächer, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="47c08-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="47c08-p111">Wenn mehr als 1.000 Quellpostfächer vorhanden sind, versuchen Sie zwei (oder mehrere) Content-Suche zu erstellen. Suchen Sie beispielsweise die Hälfte der Postfächer Ihrer Organisation in eine Inhaltssuche und die andere Hälfte in einem anderen Inhaltssuche. Sie könnten auch zur Verringerung der Anzahl von Postfächern, die Suchergebnisse enthalten die Suchkriterien ändern. Beispielsweise können Sie einen Datumsbereich ein- oder verfeinern der Stichwortabfrage.</span><span class="sxs-lookup"><span data-stu-id="47c08-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="47c08-161">Schritt 2: Verbinden mit der Sicherheit &amp; Compliance Center und Exchange Online in einer einzigen remote-PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="47c08-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="47c08-p112">Im nächsten Schritt wird Windows PowerShell sowohl die Sicherheit Verbindung &amp; Compliance Center und Ihre Exchange Online-Organisation. Dies ist erforderlich, da das Skript, das Sie in Schritt 3 ausführen, Zugriff auf die Inhaltssuche-Cmdlets in das Wertpapier erfordert &amp; Compliance Center und die Compliance-eDiscovery-Cmdlets in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="47c08-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="47c08-p113">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe von Filename Suffix. ps1. Angenommen, Sie konnte speichern in eine Datei namens `ConnectEXO-CC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="47c08-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="47c08-166">Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47c08-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="47c08-p114">Woher wissen Sie, ob dies funktioniert? Nach dem Ausführen des Skripts,-Cmdlets auf die Sicherheit &amp; Compliance Center und Exchange Online in Ihre lokale PowerShell-Sitzung importiert werden. Wenn Sie keine Fehler erhalten, verbunden Sie erfolgreich. Ein schnelles Test ist zum Ausführen eines Wertpapiers &amp; Compliance Center-Cmdlet – beispielsweise **Install-UnifiedCompliancePrerequisite** – und einer Exchange Online-Cmdlets wie **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="47c08-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="47c08-171">Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="47c08-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="47c08-p115">Nachdem die duale PowerShell-Sitzung in Schritt2 erstellt wurde, besteht der nächste Schritt das Ausführen eines Skripts, das in einer Compliance-eDiscovery-Suche eine vorhandene Inhaltssuche konvertiert wird. Hier wird die Funktionsweise des Skripts:</span><span class="sxs-lookup"><span data-stu-id="47c08-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="47c08-174">Es fordert Sie auf, den Namen der zu konvertierenden Inhaltssuche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="47c08-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="47c08-p116">Es stellt sicher, dass die Inhaltssuche abgeschlossen wird. Wenn die Compliancesuche keine Ergebnisse zurückgibt, wird In-Situ-eDiscovery nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="47c08-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="47c08-177">Speichert eine Liste der Quellpostfächer aus der Inhaltssuche mit den Suchergebnissen in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="47c08-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="47c08-p117">Erstellt eine neue In-Situ-eDiscovery-Suche mit den folgenden Eigenschaften. Beachten Sie, dass die neue Suche noch nicht gestartet wurde. Sie werden diese in Schritt 4 starten.</span><span class="sxs-lookup"><span data-stu-id="47c08-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="47c08-p118">**Name** – der Name der neuen Suche verwendet dieses Format: \<Name des Inhaltssuche\>_MBSearch1. Wenn Sie das Skript erneut ausführen und die gleiche Quelle Inhaltssuche verwenden, wird die Suche namens \<Name des Inhaltssuche\>_MBSearch2.</span><span class="sxs-lookup"><span data-stu-id="47c08-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="47c08-183">**Quellpostfächer** - alle Postfächer aus der Inhaltssuche, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="47c08-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="47c08-p119">**Suchabfrage** - neue Suche wird die Suchabfrage aus der Inhaltssuche verwendet. Enthält Inhalt für die Suche alle Inhalte (, die die Suchabfrage leer ist) wird die neue Suche müssen auch eine leere Search-Abfrage und enthält alle Inhalte, die in der Quellpostfächer gefunden.</span><span class="sxs-lookup"><span data-stu-id="47c08-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="47c08-p120">**Schätzen Sie nur Search** - neue Suche ist mit einer Suche Estimate-only gekennzeichnet. Es wird nicht Suchergebnisse in ein discoverypostfach kopieren, nachdem Sie den Workflow starten.</span><span class="sxs-lookup"><span data-stu-id="47c08-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="47c08-p121">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe von Filename Suffix ps1. Angenommen, Sie konnte speichern in eine Datei namens `CreateMBSearchFromComplianceSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="47c08-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="47c08-190">In der Windows PowerShell-Sitzung, die Sie in Schritt2 erstellt haben, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47c08-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="47c08-191">Bei Aufforderung durch das Skript Geben Sie den Namen des Content-Suche, die Sie konvertieren zu einer Compliance-eDiscovery-Suche (beispielsweise die Suche, die Sie in Schritt 1 erstellt) möchten, und drücken Sie die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="47c08-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="47c08-p122">Wenn das Skript erfolgreich ausgeführt wird, wird eine neue In-Situ-eDiscovery-Suche mit dem Status **NotStarted** erstellt. Führen Sie den Befehl  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` aus, um die Eigenschaften der neuen Suche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="47c08-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="47c08-194">Schritt 4: Starten der In-Situ-eDiscovery-Suche</span><span class="sxs-lookup"><span data-stu-id="47c08-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="47c08-p123">Mit dem Skript, das Sie in Schritt 3 ausführen, wird eine neue In-Situ-eDiscovery-Suche erstellt, jedoch nicht gestartet. Im nächsten Schritt wird die Suche gestartet, damit Sie eine Schätzung der Suchergebnisse abrufen können.</span><span class="sxs-lookup"><span data-stu-id="47c08-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="47c08-197">Navigieren Sie in Exchange-Verwaltungskonsole (EAC) zu **Verwaltung der Compliance** \> **Compliance-eDiscovery &amp; Compliance-Archive**.</span><span class="sxs-lookup"><span data-stu-id="47c08-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="47c08-198">Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="47c08-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="47c08-199">Klicken Sie auf **Suche** ![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Schätzung der Suchergebnisse** auf die Suche starten und eine Schätzung der Gesamtgröße und Anzahl der Elemente, die von der Suche zurückgegebenen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="47c08-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="47c08-p124">Die Schätzungen werden im Detailfenster angezeigt. Klicken Sie auf **Aktualisieren** ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47c08-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="47c08-202">Um eine Vorschau der Ergebnisse anzuzeigen, nachdem die Suche abgeschlossen ist, klicken Sie im Detailbereich auf **Vorschau der Suchergebnisse anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="47c08-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="47c08-203">Nächste Schritte nach dem Erstellen und Ausführen der In-Situ-eDiscovery-Suche</span><span class="sxs-lookup"><span data-stu-id="47c08-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="47c08-204">Nach dem Erstellen und Starten der In-Situ-eDiscovery-Suche, die mit dem Skript in Schritt 3 erstellt wurde, können Sie den normalen In-Situ-eDiscovery-Workflow zum Durchführen verschiedener eDiscovery-Aktionen an den Suchergebnissen verwenden.</span><span class="sxs-lookup"><span data-stu-id="47c08-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="47c08-205">Erstellen eines In-Situ-Archivs</span><span class="sxs-lookup"><span data-stu-id="47c08-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="47c08-206">Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.</span><span class="sxs-lookup"><span data-stu-id="47c08-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="47c08-207">In der Listenansicht, wählen Sie die Compliance-eDiscovery-Suche, die Sie in Schritt 3 erstellt haben, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="47c08-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="47c08-208">Aktivieren Sie auf der Seite **Compliance-Archive** das Kontrollkästchen **Inhalt, der in ausgewählten Postfächern mit der Suchabfrage übereinstimmt, aufbewahren**, und wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="47c08-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="47c08-p125">**In einer Warteschleife verbleibt** - wählen Sie diese Option, um auf eine aufzubewahren von der Suche zurückgegebenen Elemente zu platzieren. Elemente in der Warteschleife bleiben, bis Sie des Postfachs aus der Suche entfernen oder entfernen die Suche erhalten.</span><span class="sxs-lookup"><span data-stu-id="47c08-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="47c08-p126">**Geben Sie Anzahl der Tage speichern Elemente relativ zu ihrer Empfangsdatum** – wählen Sie diese Option, um Elemente für einen bestimmten Zeitraum zu halten. Ein Element Postfach empfangen oder erstellt wird, wird die Dauer ab dem Datum berechnet.</span><span class="sxs-lookup"><span data-stu-id="47c08-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="47c08-213">Klicken Sie auf **Speichern**, um das Compliance-Archiv zu erstellen und die Suche neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="47c08-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="47c08-214">Zurück zum Seitenanfang</span><span class="sxs-lookup"><span data-stu-id="47c08-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="47c08-215">Kopieren der Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="47c08-215">Copy the search results</span></span>

1. <span data-ttu-id="47c08-216">Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.</span><span class="sxs-lookup"><span data-stu-id="47c08-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="47c08-217">Wählen Sie in der Listenansicht die In-Situ-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="47c08-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="47c08-218">Klicken Sie auf **Suche** ![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), und klicken Sie dann auf **Kopieren der Suchergebnisse** aus der Dropdown-Liste.</span><span class="sxs-lookup"><span data-stu-id="47c08-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="47c08-219">Wählen Sie unter **Suchergebnisse kopieren** aus den folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="47c08-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="47c08-220">**Nicht durchsuchbare Elemente einschließen** – aktivieren Sie dieses Kontrollkästchen, Postfachelemente enthalten, die (beispielsweise Nachrichten mit Anlagen mit Dateitypen, die von der Exchange-Suche indiziert werden konnten) konnte nicht durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="47c08-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="47c08-p127">**Deduplizierung aktivieren** – aktivieren Sie dieses Kontrollkästchen, um doppelte Nachrichten ausschließen. Nur eine einzige Instanz einer Nachricht wird in das discoverypostfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="47c08-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="47c08-223">**Vollständige Protokollierung aktivieren** – aktivieren Sie dieses Kontrollkästchen, um eine vollständige Protokolldatei in Suchergebnisse einschließen.</span><span class="sxs-lookup"><span data-stu-id="47c08-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="47c08-224">**Mich bei der Kopiervorgang abgeschlossen ist e-Mail senden** – aktivieren Sie dieses Kontrollkästchen, um eine e-Mail-Benachrichtigung zu erhalten, wenn die Suche abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="47c08-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="47c08-225">**Ergebnisse in dieser discoverypostfach kopieren** - klicken Sie auf **Durchsuchen** , um das discoverypostfach auszuwählen, die Suchergebnisse angezeigt werden sollen kopiert.</span><span class="sxs-lookup"><span data-stu-id="47c08-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="47c08-226">Klicken Sie auf **Kopieren**, um den Prozess zum Kopieren der Suchergebnisse in das angegebene Discoverypostfach zu starten.</span><span class="sxs-lookup"><span data-stu-id="47c08-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="47c08-227">Klicken Sie auf **Aktualisieren** ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) , die Informationen zu den kopieren Status aktualisieren, die im Detailbereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="47c08-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="47c08-228">Wenn der Kopiervorgang abgeschlossen ist, klicken Sie auf **Öffnen**, um das Discoverypostfach zu öffnen und die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="47c08-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="47c08-229">Exportieren der Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="47c08-229">Export the search results</span></span>

1. <span data-ttu-id="47c08-230">Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.</span><span class="sxs-lookup"><span data-stu-id="47c08-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="47c08-231">Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben, und klicken Sie anschließend auf **In eine PST-Datei exportieren**.</span><span class="sxs-lookup"><span data-stu-id="47c08-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="47c08-232">Gehen Sie im Fenster **eDiscovery-PST-Exporttool** folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="47c08-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="47c08-233">Klicken Sie auf **Durchsuchen**, und geben Sie das Verzeichnis an, in das die PST-Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47c08-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="47c08-p128">Klicken Sie auf das Kontrollkästchen **Entfernung von Duplikaten aktivieren**, um doppelte Nachrichten auszuschließen. Es wird nur eine einzelne Instanz einer Nachricht in die PST-Datei aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="47c08-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="47c08-p129">Wählen Sie das Kontrollkästchen **Nicht durchsuchbare Elemente einschließen** aus, um Postfachelemente zu berücksichtigen, die nicht durchsucht werden konnten (z. B. Nachrichten mit Anhängen, die Dateitypen enthalten, die von der Exchange-Suche nicht indiziert werden konnten). Nicht durchsuchbare Elemente werden in eine separate PST-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="47c08-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="47c08-238">Klicken Sie auf **Start**, um die Suchergebnisse in eine PST-Datei zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="47c08-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="47c08-239">Es wird ein Fenster angezeigt, das Statusinformationen über den Exportvorgang anzeigt.</span><span class="sxs-lookup"><span data-stu-id="47c08-239">A window is displayed that contains status information about the export process.</span></span>

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
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="4a77e-103">Verwenden der Inhaltssuche im eDiscovery-Workflow</span><span class="sxs-lookup"><span data-stu-id="4a77e-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="4a77e-104">Mit der Inhaltssuche im Security & Compliance Center können Sie alle Postfächer in Ihrer Organisation durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-104">The Content Search feature in the Security & Compliance Center allows you to search all mailboxes in your organization.</span></span> <span data-ttu-id="4a77e-105">Im Gegensatz zu in-Place eDiscovery in Exchange Online (wo Sie bis zu 10.000 Postfächer durchsuchen können), gibt es keine Begrenzung für die Anzahl von Ziel Postfächern in einer einzelnen Suche.</span><span class="sxs-lookup"><span data-stu-id="4a77e-105">Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search.</span></span> <span data-ttu-id="4a77e-106">Für Szenarien, in denen organisationsweite Suchen erforderlich sind, können Sie die Inhaltssuche zum Durchsuchen aller Postfächer verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-106">For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes.</span></span> <span data-ttu-id="4a77e-107">Anschließend können Sie die Workflowfeatures von in-situ-eDiscovery verwenden, um andere eDiscovery-bezogene Aufgaben auszuführen, wie das Speichern von Postfächern und das Exportieren von Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-107">Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results.</span></span> <span data-ttu-id="4a77e-108">Angenommen, Sie müssen alle Postfächer durchsuchen, um bestimmte Verwalter zu identifizieren, die auf einen Rechtsfall reagieren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-108">For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case.</span></span> <span data-ttu-id="4a77e-109">Sie können die Inhaltssuche im Security & Compliance Center verwenden, um alle Postfächer in Ihrer Organisation zu durchsuchen, um diejenigen zu identifizieren, die auf den Fall reagieren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-109">You can use Content Search in the Security & Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case.</span></span> <span data-ttu-id="4a77e-110">Dann können Sie diese Liste der Depot Postfächer als Quellpostfächer für eine in-Place-eDiscovery-Suche in Exchange Online verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-110">Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online.</span></span> <span data-ttu-id="4a77e-111">Mithilfe von in-situ-eDiscovery können Sie auch diese Quellpostfächer einhalten, Suchergebnisse in ein Discovery-Postfach kopieren und die Suchergebnisse exportieren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-111">Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="4a77e-112">Dieses Thema enthält ein Skript, das Sie zum Erstellen einer in-Place-eDiscovery-Suche in Exchange Online ausführen können, indem Sie die Liste der Quellpostfächer und die Suchabfrage aus einer im Security & Compliance Center erstellten Suche verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-112">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security & Compliance Center.</span></span> <span data-ttu-id="4a77e-113">Im Folgenden finden Sie eine Übersicht über den Vorgang:</span><span class="sxs-lookup"><span data-stu-id="4a77e-113">Here's an overview of the process:</span></span>
  
[<span data-ttu-id="4a77e-114">Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfach in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="4a77e-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="4a77e-115">Schritt 2: Herstellen einer Verbindung mit \& dem Security Compliance Center und Exchange Online in einer einzigen Remote-PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="4a77e-115">Step 2: Connect to the Security \& Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="4a77e-116">Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="4a77e-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="4a77e-117">Step 4: Start the In-Place eDiscovery search</span><span class="sxs-lookup"><span data-stu-id="4a77e-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="4a77e-118">Schritt 1: Erstellen einer Inhaltssuche zum Durchsuchen aller Postfächer in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="4a77e-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="4a77e-119">Der erste Schritt besteht darin, das Security & Compliance Center (oder Security & Compliance Center PowerShell) zum Erstellen einer Inhaltssuche zu verwenden, die alle Postfächer in Ihrer Organisation durchsucht.</span><span class="sxs-lookup"><span data-stu-id="4a77e-119">The first step is to use the Security & Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization.</span></span> <span data-ttu-id="4a77e-120">Es gibt keine Begrenzung für die Anzahl der Postfächer für eine einzelne Inhaltssuche.</span><span class="sxs-lookup"><span data-stu-id="4a77e-120">There's no limit for the number of mailboxes for a single Content Search.</span></span> <span data-ttu-id="4a77e-121">Geben Sie eine geeignete Stichwortabfrage (oder eine Abfrage für vertrauliche Informationstypen) an, damit die Suche nur die Quellpostfächer zurückgibt, die für Ihre Untersuchung relevant sind.</span><span class="sxs-lookup"><span data-stu-id="4a77e-121">Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation.</span></span> <span data-ttu-id="4a77e-122">Verfeinern Sie bei Bedarf die Suchabfrage, um den Umfang der zurückgegebenen Suchergebnisse und Quellpostfächer einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="4a77e-122">If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4a77e-p104">Wenn die Quellinhaltssuche keine Ergebnisse liefert, wird In-Situ-eDiscovery nicht erstellt, wenn Sie das Skript in Schritt 3 ausführen. Sie müssen die Suchabfrage möglicherweise überarbeiten und die Inhaltssuche erneut ausführen, damit Suchergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security--compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="4a77e-125">Verwenden des Security & Compliance Center zum Durchsuchen aller Postfächer</span><span class="sxs-lookup"><span data-stu-id="4a77e-125">Use the Security & Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="4a77e-126">[Wechseln Sie zum Security _AMP_ Compliance Center](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4a77e-126">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="4a77e-127">Klicken Sie auf **Such** > **Inhaltssuche**, und klicken Sie dann auf](media/O365-MDM-CreatePolicy-AddIcon.gif) **Neues Such** ![Symbol hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-127">Click **Search** > **Content search**, and then click **New search** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="4a77e-128">Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein.</span><span class="sxs-lookup"><span data-stu-id="4a77e-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="4a77e-129">Klicken Sie unter **Wo sollen wir suchen?** auf **Alle Postfächer durchsuchen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="4a77e-130">Geben Sie im Feld unter **Wonach sollen wir für Sie suchen?** eine Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="4a77e-130">In the box under **What do you want us to look for?**, type a search query in the box.</span></span> <span data-ttu-id="4a77e-131">Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung.</span><span class="sxs-lookup"><span data-stu-id="4a77e-131">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="4a77e-132">Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise AND, OR, NOT oder NEAR, oder Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-132">You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages.</span></span> <span data-ttu-id="4a77e-133">Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="4a77e-133">For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="4a77e-134">Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="4a77e-135">Eine Schätzung der Suchergebnisse, die im Detailbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-135">After a while, an estimate of the search results displayed in the details pane.</span></span> <span data-ttu-id="4a77e-136">Dieser umfasst die Gesamtgröße und die Gesamtanzahl der in den Suchergebnissen zurückgegebenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="4a77e-136">The estimate includes the total size and number of items for the search results.</span></span> <span data-ttu-id="4a77e-137">Wenn die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-137">After the search is completed, you can preview the search results.</span></span> <span data-ttu-id="4a77e-138">Klicken Sie \*\*\*\*![gegebenenfalls auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren, um die Informationen im Detailbereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-138">If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="4a77e-139">Verfeinern Sie ggf. die Suchabfrage, um die Suchergebnisse einzugrenzen, und starten Sie die Suche neu.</span><span class="sxs-lookup"><span data-stu-id="4a77e-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="4a77e-140">Verwenden der Security & Compliance Center-PowerShell zum Durchsuchen aller Postfächer</span><span class="sxs-lookup"><span data-stu-id="4a77e-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="4a77e-141">Sie können auch das **New-ComplianceSearch**-Cmdlet zum Durchsuchen aller Postfächer in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-141">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization.</span></span> <span data-ttu-id="4a77e-142">Der erste Schritt besteht darin, [eine Verbindung mit Security _AMP_ Compliance Center PowerShell herzustellen](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="4a77e-142">The first step is to [Connect to Security & Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="4a77e-143">NachFolgend finden Sie ein Beispiel für die Verwendung von PowerShell zum Durchsuchen aller Postfächer in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="4a77e-143">Here's an example of using PowerShell to search all mailboxes in your organization.</span></span> <span data-ttu-id="4a77e-144">Die Suchabfrage gibt alle zwischen dem 1. Januar 2015 und dem 30. Juni 2015 gesendeten Nachrichten zurück, die den Ausdruck "Finanzbericht" in der Betreffzeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-144">The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line.</span></span> <span data-ttu-id="4a77e-145">Der erste Befehl erstellt die Suche, und der zweite Befehl führt die Suche aus.</span><span class="sxs-lookup"><span data-stu-id="4a77e-145">The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="4a77e-146">Weitere Informationen finden Sie unter [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="4a77e-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="4a77e-147">Überprüfen der Anzahl der Quellpostfächer in der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="4a77e-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="4a77e-148">Eine Inhaltssuche gibt maximal 1.000 Quellpostfächer zurück, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-148">A Content Search returns a maximum of 1,000 source mailboxes that contain search results.</span></span> <span data-ttu-id="4a77e-149">Wenn es mehr als 1.000 Postfächer gibt, die Inhalte enthalten, die mit der Suchabfrage übereinstimmen, sind nur die Top 1.000-Postfächer mit den meisten Suchergebnissen in der Inhaltssuche enthalten, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-149">If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step.</span></span> <span data-ttu-id="4a77e-150">Wenn also mehr als 1.000 Postfächer Suchergebnisse enthalten, werden einige dieser Postfächer nicht in die Liste der Quellpostfächer aufgenommen, die in die in Schritt 3 erstellte neue in-Place-eDiscovery-Suche kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-150">So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="4a77e-151">Führen Sie die folgenden Schritte aus, um eine Inhaltssuche mit nicht mehr als 1.000 Quellpostfächern zu erstellen, um ein Skript mit der Anzahl der Quellpostfächer (die Suchergebnisse enthalten) anzuzeigen, die von der Inhaltssuche zurückgegeben werden, die Sie in Schritt 1 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="4a77e-152">Speichern Sie den folgenden Text in einer PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1".</span><span class="sxs-lookup"><span data-stu-id="4a77e-152">Save the following text to a PowerShell script file by using a filename suffix of .ps1.</span></span> <span data-ttu-id="4a77e-153">Sie können Sie beispielsweise in einer Datei mit dem Namen `SourceMailboxes.ps1`speichern.</span><span class="sxs-lookup"><span data-stu-id="4a77e-153">For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
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

2. <span data-ttu-id="4a77e-154">Wechseln Sie in Security & Compliance Center PowerShell zu dem Ordner, in dem sich das im vorherigen Schritt erstellte Skript befindet, und führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4a77e-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="4a77e-155">Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, die in Schritt 1 erstellte Inhaltssuche ein.</span><span class="sxs-lookup"><span data-stu-id="4a77e-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="4a77e-156">Das Skript zeigt die Anzahl der Quellpostfächer, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="4a77e-157">Wenn mehr als 1.000 Quellpostfächer vorhanden sind, versuchen Sie, zwei (oder mehr) Inhalts suchVorgänge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-157">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches.</span></span> <span data-ttu-id="4a77e-158">Suchen Sie beispielsweise die Hälfte der Postfächer Ihrer Organisation in einer Inhaltssuche und die andere Hälfte in einer anderen Inhaltssuche.</span><span class="sxs-lookup"><span data-stu-id="4a77e-158">For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search.</span></span> <span data-ttu-id="4a77e-159">Sie können auch die Suchkriterien ändern, um die Anzahl der Postfächer zu verringern, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-159">You could also change the search criteria to reduce the number of mailboxes that contain search results.</span></span> <span data-ttu-id="4a77e-160">Sie können beispielsweise einen Datums Umfang einbeziehen oder die Stichwortabfrage verfeinern.</span><span class="sxs-lookup"><span data-stu-id="4a77e-160">For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="4a77e-161">Schritt 2: Herstellen einer Verbindung mit \& dem Security Compliance Center und Exchange Online in einer einzigen Remote-PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="4a77e-161">Step 2: Connect to the Security \& Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="4a77e-162">Der nächste Schritt besteht darin, Windows PowerShell sowohl mit dem Security & Compliance Center als auch mit Ihrer Exchange Online-Organisation zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-162">The next step is to connect Windows PowerShell to both the Security & Compliance Center and to your Exchange Online organization.</span></span> <span data-ttu-id="4a77e-163">Dies ist erforderlich, da das Skript, das Sie in Schritt 3 ausführen, Zugriff auf die Cmdlets für die Inhaltssuche im Security & Compliance Center und in den in-Place eDiscovery-Cmdlets in Exchange Online benötigt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-163">This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security & Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="4a77e-164">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamensuffixes „.ps1".</span><span class="sxs-lookup"><span data-stu-id="4a77e-164">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1.</span></span> <span data-ttu-id="4a77e-165">Sie können Sie beispielsweise in einer Datei mit dem Namen `ConnectEXO-CC.ps1`speichern.</span><span class="sxs-lookup"><span data-stu-id="4a77e-165">For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="4a77e-166">Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4a77e-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="4a77e-167">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="4a77e-167">How do you know if this worked?</span></span> <span data-ttu-id="4a77e-168">Nachdem Sie das Skript ausgeführt haben, werden Cmdlets aus dem Security & Compliance Center und Exchange Online in Ihre lokale PowerShell-Sitzung importiert.</span><span class="sxs-lookup"><span data-stu-id="4a77e-168">After you run the script, cmdlets from the Security & Compliance Center and Exchange Online are imported into your local PowerShell session.</span></span> <span data-ttu-id="4a77e-169">Wenn Sie keine Fehlermeldungen erhalten, wurde die Verbindung erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-169">If you don't receive any errors, you connected successfully.</span></span> <span data-ttu-id="4a77e-170">Ein kurzer Test ist die Ausführung eines Security & Compliance Center-Cmdlets, beispielsweise **install-UnifiedCompliancePrerequisite** und eines Exchange Online-Cmdlets wie **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-170">A quick test is to run a Security & Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="4a77e-171">Schritt 3: Ausführen des Skripts zum Erstellen einer In-Situ-eDiscovery-Suche aus der Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="4a77e-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="4a77e-172">Nachdem Sie die duale PowerShell-Sitzung in Schritt 2 erstellt haben, besteht der nächste Schritt darin, ein Skript auszuführen, das eine vorhandene Inhaltssuche in eine in-Place-eDiscovery-Suche konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4a77e-172">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search.</span></span> <span data-ttu-id="4a77e-173">Das Skript führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="4a77e-173">Here's what the script does:</span></span>
  
- <span data-ttu-id="4a77e-174">Es fordert Sie auf, den Namen der zu konvertierenden Inhaltssuche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="4a77e-p116">Es stellt sicher, dass die Inhaltssuche abgeschlossen wird. Wenn die Compliancesuche keine Ergebnisse zurückgibt, wird In-Situ-eDiscovery nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="4a77e-177">Speichert eine Liste der Quellpostfächer aus der Inhaltssuche mit den Suchergebnissen in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="4a77e-p117">Erstellt eine neue In-Situ-eDiscovery-Suche mit den folgenden Eigenschaften. Beachten Sie, dass die neue Suche noch nicht gestartet wurde. Sie werden diese in Schritt 4 starten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="4a77e-181">**Name** -der Name der neuen Suche verwendet dieses Format: \<Name der Inhaltssuche\>_MBSearch1.</span><span class="sxs-lookup"><span data-stu-id="4a77e-181">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1.</span></span> <span data-ttu-id="4a77e-182">Wenn Sie das Skript erneut ausführen und dieselbe Quellinhalts Suche verwenden, wird die Suche mit \<dem Namen Name der Inhaltssuche\>_MBSearch2.</span><span class="sxs-lookup"><span data-stu-id="4a77e-182">If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="4a77e-183">**Quellpostfächer** – alle Postfächer aus der Inhaltssuche, die Suchergebnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="4a77e-184">**Suchabfrage** : die neue Suche verwendet die Suchabfrage aus der Inhaltssuche.</span><span class="sxs-lookup"><span data-stu-id="4a77e-184">**Search query** - The new search uses the search query from the Content Search.</span></span> <span data-ttu-id="4a77e-185">Berücksichtigt die Inhaltssuche alle Inhalte (leere Suchabfrage), so ist in der neuen Suche die Suchabfrage leer und es werden alle in den Quellpostfächern enthaltenen Inhalte berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-185">If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="4a77e-186">**Suche nur schätzen** -die neue Suche wird als reine schätzungs Suche gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4a77e-186">**Estimate only search** - The new search is marked as an estimate-only search.</span></span> <span data-ttu-id="4a77e-187">Die Suchergebnisse werden nicht in ein Discoverypostfach kopiert, nachdem Sie es starten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-187">It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="4a77e-188">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamensuffixes „.ps1".</span><span class="sxs-lookup"><span data-stu-id="4a77e-188">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1.</span></span> <span data-ttu-id="4a77e-189">Sie können Sie beispielsweise in einer Datei mit dem Namen `CreateMBSearchFromComplianceSearch.ps1`speichern.</span><span class="sxs-lookup"><span data-stu-id="4a77e-189">For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="4a77e-190">Wechseln Sie in der Windows PowerShell-Sitzung, die Sie in Schritt 2 erstellt haben, zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4a77e-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="4a77e-191">Geben Sie, wenn Sie vom Skript dazu aufgefordert werden, den Namen der Inhaltssuche ein, die Sie für eine in-Place-eDiscovery-Suche (beispielsweise die in Schritt 1 erstellte Suche) erfassen möchten, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="4a77e-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="4a77e-p122">Wenn das Skript erfolgreich ausgeführt wird, wird eine neue In-Situ-eDiscovery-Suche mit dem Status **NotStarted** erstellt. Führen Sie den Befehl  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` aus, um die Eigenschaften der neuen Suche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="4a77e-194">Schritt 4: Starten der In-Situ-eDiscovery-Suche</span><span class="sxs-lookup"><span data-stu-id="4a77e-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="4a77e-p123">Das Skript, das Sie in Schritt 3 ausführen, erstellt eine neue Compliance-eDiscovery-Suche, startet diese aber nicht. Der nächste Schritt ist das Starten der Suche, damit Sie eine Schätzung der Suchergebnisse abrufen können.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="4a77e-197">Navigieren Sie in Exchange-Verwaltungskonsole (EAC) zu **Verwaltung der Compliance** \> **Compliance-eDiscovery &amp; Compliance-Archive**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="4a77e-198">Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="4a77e-199">![Klicken **** Sie auf Such](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> Suchsymbol, um die Suchergebnisse zu **schätzen** , um die Suche zu starten und eine Schätzung der Gesamtgröße und Anzahl der von der Suche zurückgegebenen Elemente zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="4a77e-200">Die Schätzungen werden im Detailbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-200">The estimates are displayed in the details pane.</span></span> <span data-ttu-id="4a77e-201">Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Informationen im Detailbereich zu aktualisieren. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="4a77e-201">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="4a77e-202">Um eine Vorschau der Ergebnisse anzuzeigen, nachdem die Suche abgeschlossen ist, klicken Sie im Detailbereich auf **Vorschau der Suchergebnisse anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="4a77e-203">Nächste Schritte nach dem Erstellen und Ausführen der In-Situ-eDiscovery-Suche</span><span class="sxs-lookup"><span data-stu-id="4a77e-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="4a77e-204">Nach dem Erstellen und Starten der In-Situ-eDiscovery-Suche, die mit dem Skript in Schritt 3 erstellt wurde, können Sie den normalen In-Situ-eDiscovery-Workflow zum Durchführen verschiedener eDiscovery-Aktionen an den Suchergebnissen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77e-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="4a77e-205">Erstellen eines In-Situ-Archivs</span><span class="sxs-lookup"><span data-stu-id="4a77e-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="4a77e-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="4a77e-207">Wählen Sie in der Listenansicht die in-Place-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt \*\*\*\* ![haben, und](media/O365_MDM_CreatePolicy_EditIcon.gif)klicken Sie dann auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="4a77e-208">Aktivieren Sie auf der Seite **Compliance-Archive** das Kontrollkästchen **Inhalt, der in ausgewählten Postfächern mit der Suchabfrage übereinstimmt, aufbewahren**, und wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="4a77e-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="4a77e-209">**Unbegrenzt halten** – wählen Sie diese Option aus, um von der Suche zurückgegebene Elemente unbegrenzt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4a77e-209">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold.</span></span> <span data-ttu-id="4a77e-210">Aufbewahrte Elemente werden solange beibehalten, bis Sie das Postfach aus der Suche entfernt oder die Suche entfernt haben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-210">Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="4a77e-211">**Geben Sie die Anzahl von Tagen an, die Elemente im Verhältnis zu Ihrem Empfangsdatum enthalten** sollen: Wählen Sie diese Option aus, um Elemente für einen bestimmten Zeitraum aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-211">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period.</span></span> <span data-ttu-id="4a77e-212">Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a77e-212">The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="4a77e-213">Klicken Sie auf **Speichern**, um das Compliance-Archiv zu erstellen und die Suche neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="4a77e-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="4a77e-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="4a77e-215">Kopieren der Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="4a77e-215">Copy the search results</span></span>

1. <span data-ttu-id="4a77e-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="4a77e-217">Wählen Sie in der Listenansicht die In-Situ-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4a77e-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="4a77e-218">Klicken \*\*\*\* ![Sie auf Such](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)Suchsymbol suchen, und klicken Sie dann in der Dropdownliste auf **Suchergebnisse kopieren** .</span><span class="sxs-lookup"><span data-stu-id="4a77e-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="4a77e-219">Wählen Sie unter **Suchergebnisse kopieren** aus den folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="4a77e-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="4a77e-220">Nicht durch **Such Bare Elemente einbeziehen** – aktivieren Sie dieses Kontrollkästchen, um Postfachelemente einzuschließen, die nicht durchsucht werden konnten (beispielsweise Nachrichten mit Anlagen von Dateitypen, die nicht von der Exchange-Suche indiziert werden konnten).</span><span class="sxs-lookup"><span data-stu-id="4a77e-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="4a77e-221">**DeduplizierUng aktivieren** -aktivieren Sie dieses Kontrollkästchen, um doppelte Nachrichten auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-221">**Enable de-duplication** - Select this check box to exclude duplicate messages.</span></span> <span data-ttu-id="4a77e-222">Es wird nur eine einzelne Instanz einer Nachricht in das Discovery-Postfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="4a77e-222">Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="4a77e-223">**Vollständige Protokollierung aktivieren** : Aktivieren Sie dieses Kontrollkästchen, um ein vollständiges Protokoll in die Suchergebnisse einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="4a77e-224">E-Mail nach **Abschluss des kopierVorgangs senden** – aktivieren Sie dieses Kontrollkästchen, um eine e-Mail-Benachrichtigung zu erhalten, wenn die Suche abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4a77e-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="4a77e-225">**Ergebnisse in dieses Discovery-Postfach kopieren** – klicken Sie auf **Durchsuchen** , um das Ermittlungspostfach auszuwählen, in das die Suchergebnisse kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="4a77e-226">Klicken Sie auf **Kopieren**, um den Prozess zum Kopieren der Suchergebnisse in das angegebene Discoverypostfach zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a77e-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="4a77e-227">Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Informationen über den Kopierstatus zu aktualisieren, die im Detailbereich angezeigt werden. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="4a77e-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="4a77e-228">Wenn der Kopiervorgang abgeschlossen ist, klicken Sie auf **Öffnen**, um das Discoverypostfach zu öffnen und die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="4a77e-229">Exportieren der Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="4a77e-229">Export the search results</span></span>

1. <span data-ttu-id="4a77e-230">Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="4a77e-231">Wählen Sie in der Listenansicht die Compliance-eDiscovery-Suche aus, die Sie in Schritt 3 erstellt haben, und klicken Sie anschließend auf **In eine PST-Datei exportieren**.</span><span class="sxs-lookup"><span data-stu-id="4a77e-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="4a77e-232">Gehen Sie im Fenster **eDiscovery-PST-Exporttool** folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="4a77e-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="4a77e-233">Klicken Sie auf **Durchsuchen**, und geben Sie das Verzeichnis an, in das die PST-Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a77e-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="4a77e-p128">Klicken Sie auf das Kontrollkästchen **Entfernung von Duplikaten aktivieren**, um doppelte Nachrichten auszuschließen. Es wird nur eine einzelne Instanz einer Nachricht in die PST-Datei aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="4a77e-p129">Wählen Sie das Kontrollkästchen **Nicht durchsuchbare Elemente einschließen** aus, um Postfachelemente zu berücksichtigen, die nicht durchsucht werden konnten (z. B. Nachrichten mit Anhängen, die Dateitypen enthalten, die von der Exchange-Suche nicht indiziert werden konnten). Nicht durchsuchbare Elemente werden in eine separate PST-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="4a77e-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="4a77e-238">Klicken Sie auf **Start**, um die Suchergebnisse in eine PST-Datei zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="4a77e-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="4a77e-239">Es wird ein Fenster angezeigt, das Statusinformationen über den Exportvorgang anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4a77e-239">A window is displayed that contains status information about the export process.</span></span>

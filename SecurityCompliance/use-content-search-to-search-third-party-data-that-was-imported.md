---
title: Verwenden Sie Inhaltssuche, um Daten von Dritten zu suchen, die in Office 365 importiert wurde
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Verwenden Sie das Inhaltssuche eDiscovery-Tool nach Elementen gesucht, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage aus, um alle importierten Elemente suchen oder erstellen Sie eine Abfrage zum Suchen nach bestimmten von Drittanbieter-Datentypen erstellen. In diesem Artikel werden die Werte, die Sie in einer schlüsselwortabfrage verwenden können, um die Datentypen von Drittanbietern suchen, die auf Office 365 importiert werden kann.
ms.openlocfilehash: 6829e894ba687fb09184c32201f76394e37bbbf8
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037968"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="6ffeb-105">Verwenden Sie Inhaltssuche, um Daten von Dritten zu suchen, die in Office 365 importiert wurde</span><span class="sxs-lookup"><span data-stu-id="6ffeb-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="6ffeb-p102">Sie können das [Inhaltssuche eDiscovery-Tool](content-search.md) verwenden, in die Office 365-Sicherheit &amp; Compliance Center, um die Suche nach Elementen, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage aus, um alle importierten von Drittanbieter-Datenelementen gesucht werden soll erstellen, oder Sie können eine Abfrage an die Suche nur bestimmte Drittanbieter-Datenelemente erstellen. Darüber hinaus können Sie auch eine abfragebasierte Aufbewahrung Richtlinie erstellen oder einer eDiscovery-Abfrage-basierte halten Drittanbieter-Daten in Office 365 erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ffeb-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="6ffeb-109">Weitere Informationen zum Importieren von Drittanbieter-Daten und eine Liste der Drittanbieter-Datentypen, die in Office 365 importiert werden können, finden Sie unter [Archivierung Drittanbieter - Daten in Office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="6ffeb-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="6ffeb-110">Erstellen einer Abfrage zum Suchen von Daten für alle von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="6ffeb-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="6ffeb-p103">Suche (oder direkt in der Warteschleife) jede Art von Drittanbieter-Daten, die Sie in Office 365 importiert haben, können Sie Sie können die `kind:externaldata` Meldung Eigenschaft-Wert-Paar in das Feld Stichwort für ein Inhaltssuche oder beim Erstellen einer abfragebasierte Aufbewahrung. Um die Suche nach Elementen, die aus einer beliebigen Drittanbieter-Datenquelle importiert wurden, und das Wort "Contoso" in die Subject-Eigenschaft des importierten Elements enthalten sein, verwenden Sie beispielsweise die folgende Abfrage:</span><span class="sxs-lookup"><span data-stu-id="6ffeb-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="6ffeb-p104">Im vorherigen Beispiel der Schlüsselwort-Abfrage enthält die Subject-Eigenschaft. Eine Liste mit anderen Eigenschaften für Drittanbieter-Datenelemente, die in einer schlüsselwortabfrage enthalten, finden Sie im Abschnitt "Weitere Informationen" in der [Drittanbieter - Archivierungsdaten in Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="6ffeb-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="6ffeb-p105">Beim Erstellen von Abfragen zum Durchsuchen und halten von Drittanbieter-Daten, können Sie auch Bedingungen verwenden, um die Suchergebnisse einzuschränken. Weitere Informationen zum Erstellen von Suchabfragen finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="6ffeb-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="6ffeb-117">Erstellen einer Abfrage, um bestimmte Arten von Drittanbieter-Daten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6ffeb-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="6ffeb-118">Nicht alle Arten von Drittanbieter-Daten durchsuchen, sondern können Sie Abfragen für ein Drittanbieter-Datentyp angeben, dass nur die Suche erstellen, mithilfe der folgenden Nachricht Eigenschaft-Wert-Paar in das Feld Stichwort für ein Inhaltssuche:</span><span class="sxs-lookup"><span data-stu-id="6ffeb-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="6ffeb-119">Um nur Facebook Daten zu suchen, die das Wort "Contoso" in die Subject-Eigenschaft enthält, würden Sie beispielsweise die folgende Abfrage verwenden:</span><span class="sxs-lookup"><span data-stu-id="6ffeb-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="6ffeb-p106">Die folgende Tabelle enthält die Drittanbieter-Datentypen, die durchsucht werden, und der Wert für die `itemclass:` message-Eigenschaft, wie nach speziell für diese Art von Drittanbieter-Daten. Beachten Sie, dass die Abfragesyntax Groß-/Kleinschreibung nicht.</span><span class="sxs-lookup"><span data-stu-id="6ffeb-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="6ffeb-122">**Drittanbieter-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="6ffeb-122">**Third-party data type**</span></span>|<span data-ttu-id="6ffeb-123">**Wert für `itemclass:` -Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="6ffeb-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ffeb-124">AIM</span><span class="sxs-lookup"><span data-stu-id="6ffeb-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="6ffeb-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="6ffeb-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="6ffeb-126">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="6ffeb-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="6ffeb-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="6ffeb-128">Ares</span><span class="sxs-lookup"><span data-stu-id="6ffeb-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="6ffeb-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="6ffeb-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="6ffeb-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="6ffeb-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="6ffeb-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="6ffeb-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="6ffeb-132">Platzhalter für AX</span><span class="sxs-lookup"><span data-stu-id="6ffeb-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="6ffeb-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="6ffeb-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="6ffeb-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="6ffeb-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="6ffeb-135">Bearshare</span><span class="sxs-lookup"><span data-stu-id="6ffeb-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="6ffeb-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="6ffeb-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="6ffeb-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6ffeb-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="6ffeb-138">BlackBerry mithilfe von Anruflisten</span><span class="sxs-lookup"><span data-stu-id="6ffeb-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="6ffeb-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="6ffeb-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="6ffeb-140">BlackBerry-PIN</span><span class="sxs-lookup"><span data-stu-id="6ffeb-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="6ffeb-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="6ffeb-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="6ffeb-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="6ffeb-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="6ffeb-143">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="6ffeb-144">Bloomberg Messaging</span><span class="sxs-lookup"><span data-stu-id="6ffeb-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="6ffeb-145">Box
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="6ffeb-146">Cisco Sofortnachrichten &amp; Anwesenheitsserver</span><span class="sxs-lookup"><span data-stu-id="6ffeb-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="6ffeb-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="6ffeb-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="6ffeb-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6ffeb-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="6ffeb-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="6ffeb-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="6ffeb-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="6ffeb-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="6ffeb-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="6ffeb-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="6ffeb-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="6ffeb-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="6ffeb-153">Flickr
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="6ffeb-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="6ffeb-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="6ffeb-155">Google+
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="6ffeb-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="6ffeb-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="6ffeb-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="6ffeb-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="6ffeb-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="6ffeb-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="6ffeb-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="6ffeb-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="6ffeb-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="6ffeb-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="6ffeb-161">IBM-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="6ffeb-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="6ffeb-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="6ffeb-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="6ffeb-163">ICE Chat</span><span class="sxs-lookup"><span data-stu-id="6ffeb-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="6ffeb-164">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="6ffeb-165">Instagram
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="6ffeb-166">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="6ffeb-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="6ffeb-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="6ffeb-168">IRC</span><span class="sxs-lookup"><span data-stu-id="6ffeb-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="6ffeb-169">Jive
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="6ffeb-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="6ffeb-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="6ffeb-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="6ffeb-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="6ffeb-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6ffeb-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="6ffeb-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="6ffeb-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="6ffeb-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="6ffeb-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="6ffeb-175">Beachten Sie ausrichten</span><span class="sxs-lookup"><span data-stu-id="6ffeb-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="6ffeb-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="6ffeb-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="6ffeb-177">MSN</span><span class="sxs-lookup"><span data-stu-id="6ffeb-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="6ffeb-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="6ffeb-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="6ffeb-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="6ffeb-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="6ffeb-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="6ffeb-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="6ffeb-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="6ffeb-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="6ffeb-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="6ffeb-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="6ffeb-183">QQ</span><span class="sxs-lookup"><span data-stu-id="6ffeb-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="6ffeb-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="6ffeb-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="6ffeb-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6ffeb-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="6ffeb-186">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="6ffeb-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="6ffeb-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="6ffeb-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="6ffeb-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="6ffeb-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="6ffeb-189">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="6ffeb-190">Symphony
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="6ffeb-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="6ffeb-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="6ffeb-192">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="6ffeb-193">Tor</span><span class="sxs-lookup"><span data-stu-id="6ffeb-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="6ffeb-194">TTT</span><span class="sxs-lookup"><span data-stu-id="6ffeb-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="6ffeb-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="6ffeb-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="6ffeb-196">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="6ffeb-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="6ffeb-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="6ffeb-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="6ffeb-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="6ffeb-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="6ffeb-199">Winny</span><span class="sxs-lookup"><span data-stu-id="6ffeb-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="6ffeb-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="6ffeb-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="6ffeb-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="6ffeb-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="6ffeb-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="6ffeb-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="6ffeb-203">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="6ffeb-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |

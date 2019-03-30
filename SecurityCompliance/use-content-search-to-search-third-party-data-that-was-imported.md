---
title: Verwenden der Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Verwenden Sie das eDiscovery-Tool für die Inhaltssuche, um nach Elementen zu suchen, die in Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Sie können eine Abfrage erstellen, um nach allen importierten Elementen zu suchen, oder eine Abfrage erstellen, um nach bestimmten Drittanbieter Datentypen zu suchen. In diesem Artikel werden die Werte aufgelistet, die Sie in einer Stichwortabfrage verwenden können, um die Drittanbieter-Datentypen zu durchsuchen, die in Office 365 importiert werden können.
ms.openlocfilehash: 361ead435d397464452c5b58ecf251a7322ced05
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999708"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="53330-105">Verwenden der Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden</span><span class="sxs-lookup"><span data-stu-id="53330-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="53330-106">Sie können das eDiscovery-Tool für die [Inhaltssuche](content-search.md) im Security _AMP_ Compliance Center verwenden, um nach Elementen zu suchen, die in Postfächern in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="53330-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="53330-107">Sie können eine Abfrage zum Durchsuchen aller importierten drittanbieterdaten Elemente erstellen, oder Sie können eine Abfrage erstellen, um nur bestimmte Drittanbieter-Datenelemente zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="53330-107">You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items.</span></span> <span data-ttu-id="53330-108">Darüber hinaus können Sie auch eine abfragebasierte AufbewahrungsRichtlinie oder einen abfragebasierten eDiscovery-Speicher erstellen, um drittanbieterdaten in Office 365 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53330-108">Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="53330-109">Weitere Informationen zum Importieren von drittanbieterdaten und eine Liste der Drittanbieter Datentypen, die in Office 365 importiert werden können, finden Sie unter [Archivierung von drittanbieterdaten in office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="53330-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="53330-110">Erstellen einer Abfrage zum Durchsuchen aller drittanbieterdaten</span><span class="sxs-lookup"><span data-stu-id="53330-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="53330-111">Wenn Sie alle Typen von drittanbieterdaten, die Sie in Office 365 importiert haben, Durchsuchen (oder im Wartebereich platzieren) möchten, können `kind:externaldata` Sie das Nachrichteneigenschaft-Wert-Paar im Stichwortfeld für eine Inhaltssuche oder beim Erstellen eines abfragebasierten haltebereichs verwenden.</span><span class="sxs-lookup"><span data-stu-id="53330-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="53330-112">Wenn Sie beispielsweise nach Elementen suchen möchten, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in der Subject-Eigenschaft des importierten Elements enthalten, würden Sie die folgende Abfrage verwenden:</span><span class="sxs-lookup"><span data-stu-id="53330-112">For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="53330-113">Das vorherige Keyword Query-Beispiel enthält die Subject-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="53330-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="53330-114">Eine Liste anderer Eigenschaften von drittanbieterdaten Elementen, die in eine Stichwortabfrage aufgenommen werden können, finden Sie im Abschnitt "Weitere Informationen" unter [Archivieren von drittanbieterdaten in Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="53330-114">For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="53330-115">Beim Erstellen von Abfragen zum Durchsuchen und Speichern von drittanbieterdaten können Sie auch Bedingungen verwenden, um die Suchergebnisse einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="53330-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="53330-116">Weitere Informationen zum Erstellen von Inhalts Suchabfragen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="53330-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="53330-117">Erstellen einer Abfrage zum Durchsuchen bestimmter Typen von drittanbieterdaten</span><span class="sxs-lookup"><span data-stu-id="53330-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="53330-118">Anstatt alle Typen von drittanbieterdaten zu durchsuchen, können Sie Abfragen erstellen, die nur nach einem angegebenen Typ von drittanbieterdaten suchen, indem Sie im Stichwortfeld für eine Inhaltssuche das folgende Nachrichten Eigenschaftswert-paar verwenden:</span><span class="sxs-lookup"><span data-stu-id="53330-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="53330-119">Wenn Sie beispielsweise nur Facebook-Daten durchsuchen möchten, die das Wort "Contoso" in der Subject-Eigenschaft enthalten, würden Sie die folgende Abfrage verwenden:</span><span class="sxs-lookup"><span data-stu-id="53330-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="53330-120">In der folgenden Tabelle sind die Drittanbieter-Datentypen aufgeführt, die Sie durchsuchen können, und der Wert `itemclass:` , der für die Message-Eigenschaft verwendet werden soll, um gezielt nach diesem Typ von drittanbieterdaten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="53330-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="53330-121">Beachten Sie, dass bei der Abfragesyntax die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="53330-121">Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="53330-122">**Drittanbieter-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="53330-122">**Third-party data type**</span></span>|<span data-ttu-id="53330-123">**Wert für `itemclass:` Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="53330-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53330-124">VERSUCHEN</span><span class="sxs-lookup"><span data-stu-id="53330-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="53330-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="53330-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="53330-126">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="53330-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="53330-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="53330-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="53330-128">Ares</span><span class="sxs-lookup"><span data-stu-id="53330-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="53330-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="53330-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="53330-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="53330-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="53330-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="53330-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="53330-132">AXS-Platzhalter</span><span class="sxs-lookup"><span data-stu-id="53330-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="53330-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="53330-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="53330-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="53330-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="53330-135">BearShare</span><span class="sxs-lookup"><span data-stu-id="53330-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="53330-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="53330-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="53330-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="53330-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="53330-138">BlackBerry-Anrufprotokolle</span><span class="sxs-lookup"><span data-stu-id="53330-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="53330-139">BlackBerry-Messenger</span><span class="sxs-lookup"><span data-stu-id="53330-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="53330-140">BlackBerry-PIN</span><span class="sxs-lookup"><span data-stu-id="53330-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="53330-141">BlackBerry-SMS</span><span class="sxs-lookup"><span data-stu-id="53330-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="53330-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="53330-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="53330-143">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="53330-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="53330-144">Bloomberg-Messaging</span><span class="sxs-lookup"><span data-stu-id="53330-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="53330-145">Box</span><span class="sxs-lookup"><span data-stu-id="53330-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="53330-146">Cisco- &amp; Sofortnachrichten-Anwesenheits Server</span><span class="sxs-lookup"><span data-stu-id="53330-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="53330-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="53330-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="53330-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="53330-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="53330-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="53330-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="53330-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="53330-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="53330-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="53330-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="53330-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="53330-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="53330-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="53330-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="53330-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="53330-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="53330-155">Google +</span><span class="sxs-lookup"><span data-stu-id="53330-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="53330-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="53330-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="53330-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="53330-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="53330-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="53330-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="53330-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="53330-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="53330-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="53330-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="53330-161">IBM-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="53330-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="53330-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="53330-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="53330-163">ICE-Chat</span><span class="sxs-lookup"><span data-stu-id="53330-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="53330-164">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="53330-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="53330-165">Instagram</span><span class="sxs-lookup"><span data-stu-id="53330-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="53330-166">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="53330-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="53330-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="53330-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="53330-168">IRC</span><span class="sxs-lookup"><span data-stu-id="53330-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="53330-169">Jive</span><span class="sxs-lookup"><span data-stu-id="53330-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="53330-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="53330-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="53330-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="53330-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="53330-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="53330-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="53330-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="53330-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="53330-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="53330-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="53330-175">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="53330-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="53330-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="53330-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="53330-177">MSN</span><span class="sxs-lookup"><span data-stu-id="53330-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="53330-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="53330-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="53330-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="53330-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="53330-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="53330-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="53330-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="53330-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="53330-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="53330-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="53330-183">QQ</span><span class="sxs-lookup"><span data-stu-id="53330-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="53330-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="53330-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="53330-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="53330-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="53330-186">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="53330-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="53330-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="53330-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="53330-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="53330-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="53330-189">Squawker</span><span class="sxs-lookup"><span data-stu-id="53330-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="53330-190">Symphonie</span><span class="sxs-lookup"><span data-stu-id="53330-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="53330-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="53330-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="53330-192">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="53330-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="53330-193">Tor</span><span class="sxs-lookup"><span data-stu-id="53330-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="53330-194">TTT</span><span class="sxs-lookup"><span data-stu-id="53330-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="53330-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="53330-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="53330-196">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="53330-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="53330-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="53330-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="53330-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="53330-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="53330-199">Winny</span><span class="sxs-lookup"><span data-stu-id="53330-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="53330-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="53330-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="53330-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="53330-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="53330-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="53330-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="53330-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="53330-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |

---
title: Archivieren von Drittanbieter-Daten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können drittanbieterdaten aus sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen in Postfächer in Ihrer Office 365-Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und Datenquellen in Office 365 archivieren. Anschließend können Sie Office 365-Kompatibilitätsfeatures (wie rechtliche Aufbewahrung, Inhaltssuche und Aufbewahrungsrichtlinien) an drittanbieterdaten appply.
ms.openlocfilehash: 37811fdbee52cf956c6371deea53a242c2a3c550
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218495"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="26130-105">Archivieren von Drittanbieter-Daten in Office 365</span><span class="sxs-lookup"><span data-stu-id="26130-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="26130-p102">Office 365 ermöglicht Administratoren das Importieren und Archivieren von drittanbieterdaten von sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen zu Postfächern in Ihrer Office 365-Organisation. Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können, sind folgende:</span><span class="sxs-lookup"><span data-stu-id="26130-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="26130-108">**Social** -Twitter, Facebook, jammern und LinkedIn</span><span class="sxs-lookup"><span data-stu-id="26130-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="26130-109">**Instant Messaging** -Yahoo Messenger, GoogleTalk und Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="26130-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="26130-110">**Dokument Zusammenarbeit** und Dropbox</span><span class="sxs-lookup"><span data-stu-id="26130-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="26130-111">**Vertikale Branchen** – Customer Relationship Management (wie Salesforce Chatter) und Financials (wie Thomson Reuters und Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="26130-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="26130-112">**SMS/Textnachrichten** -BlackBerry</span><span class="sxs-lookup"><span data-stu-id="26130-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="26130-p103">Nachdem drittanbieterdaten importiert wurden, können Sie die Office 365-Compliance-Funktionen wie das Aufheben von Rechtsstreitigkeiten, Inhaltssuche, in-situ-Archivierung,-Überwachung und Office 365-Aufbewahrungsrichtlinien auf diese Daten anwenden. Wenn beispielsweise ein Postfach in den Rechtsstreit versetzt wird, werden Daten von Drittanbietern beibehalten. Mithilfe der Inhaltssuche können Sie drittanbieterdaten durchsuchen. Sie können auch Archivierungs-und Aufbewahrungsrichtlinien auf drittanbieterdaten anwenden, genau wie für Microsoft-Daten. Kurz gesagt, die Archivierung von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien kompatibel bleibt.</span><span class="sxs-lookup"><span data-stu-id="26130-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="26130-118">Im folgenden finden Sie eine Übersicht über den Prozess und die erforderlichen Schritte zum Importieren von drittanbieterdaten in Office 365.</span><span class="sxs-lookup"><span data-stu-id="26130-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="26130-119">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="26130-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="26130-120">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="26130-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="26130-121">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="26130-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="26130-122">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="26130-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="26130-123">Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="26130-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="26130-124">Works> des Drittanbieters für den Datenimport</span><span class="sxs-lookup"><span data-stu-id="26130-124">How the third-party data import process works></span></span>

<span data-ttu-id="26130-125">Die folgende Abbildung und die Beschreibung erläutern, wie der Prozess zum Importieren von Drittanbieterdaten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="26130-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="26130-127">Der Kunde arbeitet mit seinem bevorzugten Partner zusammen, um einen Connector zu konfigurieren, der Elemente aus der Drittanbieter-Datenquelle extrahiert und diese Elemente dann in Office 365 importiert.</span><span class="sxs-lookup"><span data-stu-id="26130-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="26130-p104">Der Partner-Connector stellt über eine Drittanbieter-API (auf einer festgelegten oder konfigurierten Basis) eine Verbindung zu drittanbieterdaten Quellen her und extrahiert Elemente aus der Datenquelle. Der Partner-Konnektor wandelt den Inhalt eines Elements in ein e-Mail-Nachrichtenformat um. Im Abschnitt [Weitere Informationen](#more-information) finden Sie eine Beschreibung des Nachrichtenformat Schemas.</span><span class="sxs-lookup"><span data-stu-id="26130-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="26130-131">Der Partner-Connector stellt mithilfe des Exchange-webDiensts (EWS) über einen bekannten Endpunkt eine Verbindung mit dem Azure-Dienst in Office 365 her.</span><span class="sxs-lookup"><span data-stu-id="26130-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="26130-p105">Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:</span><span class="sxs-lookup"><span data-stu-id="26130-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="26130-p106">a. **Elemente mit einer Benutzer-ID, die einem office 365-Benutzerkonto entspricht** – wenn der Partner-Konnektor die Benutzer-ID des Elements in der Drittanbieter-Datenquelle einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in \*\*\*\* den Ordner "purges" des Benutzers Ordner "Wiederherstellbare Elemente". Benutzer können nicht auf Elemente im Ordner "Purge" zugreifen. Sie können jedoch Office 365 eDiscovery-Tools verwenden, um im Ordner "Purges" nach Elementen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="26130-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="26130-p107">b. **Elemente, die nicht über eine Benutzer-ID verfügen, die einem office 365-Benutzerkonto entspricht** – wenn der Partner-Konnektor die Benutzer-ID eines Elements nicht einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in den Ordner " **Posteingang** " des Drittanbieter-Daten Postfachs kopiert. Durch das Importieren von Elementen in den Posteingang können Sie oder eine Person in Ihrer Organisation sich beim Drittanbieter Postfach anmelden, um diese Elemente anzuzeigen und zu verwalten, und feststellen, ob Anpassungen in der Konfiguration des Partner-Connectors vorgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="26130-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="26130-141">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="26130-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="26130-p108">Eine wichtige Komponente für die Archivierung von drittanbieterdaten in Office 365 ist die Suche und Zusammenarbeit mit einem Microsoft-Partner, der sich auf die Erfassung von Daten aus einer Drittanbieter-Datenquelle und deren Import in Office 365 spezialisiert hat. Nachdem die Daten importiert wurden, können Sie zusammen mit den anderen Microsoft-Daten Ihrer Organisation archiviert und aufbewahrt werden, wie beispielsweise e-Mails von Exchange und Dokumenten aus SharePoint und OneDrive for Business. Ein Partner erstellt einen Connector, der Daten aus drittanbieterdaten Quellen Ihrer Organisation extrahiert (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächer als e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="26130-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="26130-145">In den folgenden Abschnitten werden die Microsoft-Partner und die von Ihnen unterstützten Drittanbieter-Datenquellen aufgeführt, die am Programm zur Archivierung von drittanbieterdaten in Office 365 teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="26130-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="26130-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="26130-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="26130-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="26130-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="26130-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="26130-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="26130-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="26130-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="26130-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="26130-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="26130-151">Verba</span><span class="sxs-lookup"><span data-stu-id="26130-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="26130-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="26130-152">17a-4 LLC</span></span>

<span data-ttu-id="26130-153">17a-4 LLC unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="26130-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="26130-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="26130-154">BlackBerry</span></span>
    
- <span data-ttu-id="26130-155">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="26130-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="26130-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="26130-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="26130-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="26130-157">FactSet</span></span>
    
- <span data-ttu-id="26130-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="26130-158">HipChat</span></span>
    
- <span data-ttu-id="26130-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="26130-159">InvestEdge</span></span>
    
- <span data-ttu-id="26130-160">Schwätzchen</span><span class="sxs-lookup"><span data-stu-id="26130-160">LivePerson</span></span>
    
- <span data-ttu-id="26130-161">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="26130-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="26130-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="26130-162">OpenText</span></span>
    
- <span data-ttu-id="26130-163">Live-Hilfe für Oracle/ATG 'click-to-call'
</span><span class="sxs-lookup"><span data-stu-id="26130-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="26130-164">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="26130-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="26130-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="26130-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="26130-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="26130-166">MindAlign</span></span>
    
- <span data-ttu-id="26130-167">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="26130-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="26130-168">
Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="26130-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="26130-169">
Skype for Business Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="26130-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="26130-170">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="26130-170">SQL Databases</span></span>
    
- <span data-ttu-id="26130-171">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="26130-171">Squawker</span></span>
    
- <span data-ttu-id="26130-172">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="26130-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="26130-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="26130-173">Actiance</span></span>

<span data-ttu-id="26130-174">[Actiance](https://www.actiance.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="26130-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="26130-175">AIM</span><span class="sxs-lookup"><span data-stu-id="26130-175">AIM</span></span>
    
- <span data-ttu-id="26130-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="26130-176">American Idol</span></span>
    
- <span data-ttu-id="26130-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="26130-177">Apple Juice</span></span>
    
- <span data-ttu-id="26130-178">
AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="26130-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="26130-179">Ares</span><span class="sxs-lookup"><span data-stu-id="26130-179">Ares</span></span>
    
- <span data-ttu-id="26130-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="26130-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="26130-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="26130-181">Bear Share</span></span>
    
- <span data-ttu-id="26130-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="26130-182">Bit Torrent</span></span>
    
- <span data-ttu-id="26130-183">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="26130-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-184">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-185">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-186">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-187">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="26130-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="26130-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="26130-188">CellTrust</span></span>
    
- <span data-ttu-id="26130-189">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="26130-189">Chat Import</span></span>
    
- <span data-ttu-id="26130-190">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="26130-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="26130-191">Chatter
</span><span class="sxs-lookup"><span data-stu-id="26130-191">Chatter</span></span>
    
- <span data-ttu-id="26130-192">Cisco IM &amp; Presence Server (v 9.0.1, v 9.1, v 9.1.1 SU1, V10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="26130-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="26130-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="26130-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="26130-194">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="26130-194">Collaboration Import</span></span>
    
- <span data-ttu-id="26130-195">Echtzeitprotokollierung für Zusammenarbeit
</span><span class="sxs-lookup"><span data-stu-id="26130-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="26130-196">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="26130-196">Direct Connect</span></span>
    
- <span data-ttu-id="26130-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="26130-197">Facebook</span></span>
    
- <span data-ttu-id="26130-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="26130-198">FactSet</span></span>
    
- <span data-ttu-id="26130-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="26130-199">FastTrack</span></span>
    
- <span data-ttu-id="26130-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="26130-200">Gnutella</span></span>
    
- <span data-ttu-id="26130-201">Google+
</span><span class="sxs-lookup"><span data-stu-id="26130-201">Google+</span></span>
    
- <span data-ttu-id="26130-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="26130-202">GoToMyPC</span></span>
    
- <span data-ttu-id="26130-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="26130-203">Hopster</span></span>
    
- <span data-ttu-id="26130-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="26130-204">HubConnex</span></span>
    
- <span data-ttu-id="26130-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="26130-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="26130-206">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="26130-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="26130-207">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="26130-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="26130-208">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="26130-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="26130-209">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="26130-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="26130-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="26130-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="26130-211">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="26130-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="26130-212">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="26130-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="26130-213">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="26130-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="26130-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="26130-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="26130-215">Chat-Import
</span><span class="sxs-lookup"><span data-stu-id="26130-215">IM Import</span></span>
    
- <span data-ttu-id="26130-216">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="26130-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="26130-217">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="26130-217">Indii Messenger</span></span>
    
- <span data-ttu-id="26130-218">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="26130-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="26130-219">IRC</span><span class="sxs-lookup"><span data-stu-id="26130-219">IRC</span></span>
    
- <span data-ttu-id="26130-220">Jive
</span><span class="sxs-lookup"><span data-stu-id="26130-220">Jive</span></span>
    
- <span data-ttu-id="26130-221">Jive 6 Real Time Logging (v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="26130-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="26130-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="26130-222">Jive Import</span></span>
    
- <span data-ttu-id="26130-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="26130-223">JXTA</span></span>
    
- <span data-ttu-id="26130-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="26130-224">LinkedIn</span></span>
    
- <span data-ttu-id="26130-225">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="26130-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="26130-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="26130-226">MFTP</span></span>
    
- <span data-ttu-id="26130-227">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="26130-228">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="26130-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="26130-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="26130-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="26130-230">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="26130-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="26130-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="26130-231">MindAlign</span></span>
    
- <span data-ttu-id="26130-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="26130-232">Mobile Guard</span></span>
    
- <span data-ttu-id="26130-233">MSN</span><span class="sxs-lookup"><span data-stu-id="26130-233">MSN</span></span>
    
- <span data-ttu-id="26130-234">My Space</span><span class="sxs-lookup"><span data-stu-id="26130-234">My Space</span></span>
    
- <span data-ttu-id="26130-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="26130-235">NEONetwork</span></span>
    
- <span data-ttu-id="26130-236">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="26130-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="26130-237">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="26130-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="26130-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="26130-238">Pinterest</span></span>
    
- <span data-ttu-id="26130-239">Pivot</span><span class="sxs-lookup"><span data-stu-id="26130-239">Pivot</span></span>
    
- <span data-ttu-id="26130-240">QQ</span><span class="sxs-lookup"><span data-stu-id="26130-240">QQ</span></span>
    
- <span data-ttu-id="26130-241">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="26130-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="26130-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="26130-242">SoftEther</span></span>
    
- <span data-ttu-id="26130-243">Symphony
</span><span class="sxs-lookup"><span data-stu-id="26130-243">Symphony</span></span>
    
- <span data-ttu-id="26130-244">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="26130-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="26130-245">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="26130-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="26130-246">Tor</span><span class="sxs-lookup"><span data-stu-id="26130-246">Tor</span></span>
    
- <span data-ttu-id="26130-247">TTT</span><span class="sxs-lookup"><span data-stu-id="26130-247">TTT</span></span>
    
- <span data-ttu-id="26130-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="26130-248">Twitter</span></span>
    
- <span data-ttu-id="26130-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="26130-249">WinMX</span></span>
    
- <span data-ttu-id="26130-250">Winny</span><span class="sxs-lookup"><span data-stu-id="26130-250">Winny</span></span>
    
- <span data-ttu-id="26130-251">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="26130-251">Yahoo</span></span>
    
- <span data-ttu-id="26130-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="26130-252">Yammer</span></span>
    
- <span data-ttu-id="26130-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="26130-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="26130-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="26130-254">ArchiveSocial</span></span>

<span data-ttu-id="26130-255">[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="26130-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="26130-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="26130-256">Facebook</span></span>
    
- <span data-ttu-id="26130-257">Flickr
</span><span class="sxs-lookup"><span data-stu-id="26130-257">Flickr</span></span>
    
- <span data-ttu-id="26130-258">Instagram
</span><span class="sxs-lookup"><span data-stu-id="26130-258">Instagram</span></span>
    
- <span data-ttu-id="26130-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="26130-259">LinkedIn</span></span>
    
- <span data-ttu-id="26130-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="26130-260">Pinterest</span></span>
    
- <span data-ttu-id="26130-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="26130-261">Twitter</span></span>
    
- <span data-ttu-id="26130-262">YouTube</span><span class="sxs-lookup"><span data-stu-id="26130-262">YouTube</span></span>
    
- <span data-ttu-id="26130-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="26130-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="26130-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="26130-264">Globanet</span></span>

<span data-ttu-id="26130-265">[Globanet](https://www.globanet.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="26130-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="26130-266">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="26130-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="26130-267">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="26130-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-268">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-269">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-270">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="26130-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="26130-271">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="26130-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="26130-272">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="26130-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="26130-273">Box</span><span class="sxs-lookup"><span data-stu-id="26130-273">Box</span></span>
    
- <span data-ttu-id="26130-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="26130-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="26130-275">Cisco IM &amp; Presence Server (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="26130-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="26130-276">Cisco WebEx-Teams</span><span class="sxs-lookup"><span data-stu-id="26130-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="26130-277">Freigabe für &amp; Citrix Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="26130-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="26130-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="26130-278">CrowdCompass</span></span>

- <span data-ttu-id="26130-279">Durch Trennzeichen getrennte, benutzerdefinierte Textdateien
</span><span class="sxs-lookup"><span data-stu-id="26130-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="26130-280">Benutzerdefinierte XML-Dateien
</span><span class="sxs-lookup"><span data-stu-id="26130-280">Custom XML files</span></span>
    
- <span data-ttu-id="26130-281">Facebook (Seiten)</span><span class="sxs-lookup"><span data-stu-id="26130-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="26130-282">Factset
</span><span class="sxs-lookup"><span data-stu-id="26130-282">Factset</span></span>
    
- <span data-ttu-id="26130-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="26130-283">FXConnect</span></span>
    
- <span data-ttu-id="26130-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="26130-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="26130-285">Jive
</span><span class="sxs-lookup"><span data-stu-id="26130-285">Jive</span></span>
    
- <span data-ttu-id="26130-286">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="26130-286">Macgregor XIP</span></span>

- <span data-ttu-id="26130-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="26130-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="26130-288">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="26130-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="26130-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="26130-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="26130-290">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="26130-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="26130-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="26130-291">Mobile Guard</span></span>
    
- <span data-ttu-id="26130-292">Pivot</span><span class="sxs-lookup"><span data-stu-id="26130-292">Pivot</span></span>
    
- <span data-ttu-id="26130-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="26130-293">Salesforce Chatter</span></span>

- <span data-ttu-id="26130-294">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="26130-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="26130-295">Skype for Business, Versionen 2007 R2 - 2016 (lokal)
</span><span class="sxs-lookup"><span data-stu-id="26130-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="26130-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="26130-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="26130-297">Symphony
</span><span class="sxs-lookup"><span data-stu-id="26130-297">Symphony</span></span>
    
- <span data-ttu-id="26130-298">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="26130-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="26130-299">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="26130-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="26130-300">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="26130-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="26130-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="26130-301">Twitter</span></span>
    
- <span data-ttu-id="26130-302">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="26130-302">UBS Chat</span></span>
    
- <span data-ttu-id="26130-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="26130-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="26130-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="26130-304">OpenText</span></span>

<span data-ttu-id="26130-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="26130-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="26130-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="26130-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="26130-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="26130-307">Axs Exchange</span></span>
    
- <span data-ttu-id="26130-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="26130-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="26130-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="26130-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="26130-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="26130-310">Axs Signed</span></span>
    
- <span data-ttu-id="26130-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="26130-311">Bloomberg</span></span>
    
- <span data-ttu-id="26130-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="26130-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="26130-313">Verba</span><span class="sxs-lookup"><span data-stu-id="26130-313">Verba</span></span>

<span data-ttu-id="26130-314">[Verba](https://www.verba.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="26130-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="26130-315">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="26130-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="26130-316">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="26130-317">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="26130-317">Avtec Radio</span></span>
    
- <span data-ttu-id="26130-318">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="26130-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="26130-319">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="26130-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="26130-320">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="26130-321">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-321">Centile Voice</span></span>
    
- <span data-ttu-id="26130-322">Chatnachricht in Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="26130-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="26130-323">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="26130-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="26130-324">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="26130-325">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="26130-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="26130-326">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="26130-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="26130-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="26130-327">ESChat Radio</span></span>
    
- <span data-ttu-id="26130-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="26130-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="26130-329">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="26130-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="26130-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="26130-331">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="26130-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="26130-332">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="26130-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="26130-333">Oracle/Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="26130-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="26130-334">Oracle/Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="26130-335">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="26130-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="26130-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="26130-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="26130-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="26130-338">Chatnachricht in Skype for Business/Lync
</span><span class="sxs-lookup"><span data-stu-id="26130-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="26130-339">Skype for Business/Lync Video
</span><span class="sxs-lookup"><span data-stu-id="26130-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="26130-340">Skype for Business/Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="26130-341">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="26130-342">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="26130-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="26130-343">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="26130-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="26130-344">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="26130-344">Truphone Voice</span></span>
    
- <span data-ttu-id="26130-345">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="26130-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="26130-346">Windows Desktop-Computerbildschirm 
</span><span class="sxs-lookup"><span data-stu-id="26130-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="26130-347">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="26130-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="26130-p109">Hier finden Sie die Schritte zum Erstellen und Konfigurieren eines Drittanbieter-Daten Postfachs zum Importieren von Daten in Office 365. Wie bereits erläutert, werden Elemente in dieses Postfach importiert, wenn der Partner-Konnektor die Benutzer-ID des Elements nicht einem Office 365-Benutzerkonto zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="26130-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="26130-350">**Führen Sie diese Aufgaben im Office 365 Admin Center aus.**</span><span class="sxs-lookup"><span data-stu-id="26130-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="26130-p110">Erstellen Sie ein neues Benutzerkonto in Office 365, und weisen Sie ihm eine Exchange Online-Plan 2-Lizenz zu. Weitere Informationen finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Eine Plan 2-Lizenz ist erforderlich, um für das Postfach ein aufbewahrungsVerfahren durchzuführen oder ein Archivpostfach mit einem unbegrenzten Speicherkontingent zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="26130-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="26130-353">Fügen Sie das Benutzerkonto für das Drittanbieter-Daten Postfach der **Exchange-Administrator** Rolle in Office 365 hinzu. Weitere Informationen finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="26130-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="26130-p111">Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto. Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="26130-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="26130-356">**Ausführen dieser Aufgaben im Exchange Admin Center**</span><span class="sxs-lookup"><span data-stu-id="26130-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="26130-p112">Ausblenden des Drittanbieter-Daten Postfachs aus dem Adressbuch und anderen Adresslisten in Ihrer Organisation; Weitere Informationen finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternativ können Sie den folgenden PowerShell-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="26130-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="26130-359">Weisen Sie dem Drittanbieter-Daten Postfach die Berechtigung **FullAccess** zu, damit Administratoren oder Compliance Officers das Drittanbieter-Daten Postfach im Outlook-Desktop Client öffnen können. Weitere Informationen finden Sie unter [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="26130-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="26130-360">Aktivieren Sie die folgenden kompatibilitätsbezogenen Office 365-Features für das Drittanbieter-Daten Postfach:</span><span class="sxs-lookup"><span data-stu-id="26130-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="26130-p113">Aktivieren Sie das Archivpostfach. Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [Archivierung in Office 365](enable-unlimited-archiving.md). Auf diese Weise können Sie Speicherplatz im primären Postfach freigeben, indem Sie eine Archivrichtlinie einrichten, mit der Drittanbieter-Datenelemente in das Archivpostfach verschoben werden. Dadurch erhalten Sie unbegrenzten Speicherplatz für drittanbieterdaten.</span><span class="sxs-lookup"><span data-stu-id="26130-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="26130-p114">Platzieren Sie das Drittanbieter-Daten Postfach in einem Rechtsstreit. Sie können auch eine Office 365-Aufbewahrungsrichtlinie im Office 365 Security &amp; Compliance Center anwenden. Wenn Sie dieses Postfach anhalten, werden Datenelemente von Drittanbietern (auf unbestimmte Zeit oder für eine bestimmte Dauer) aufbewahrt und verhindert, dass Sie aus dem Postfach gelöscht werden. Lesen Sie eines der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="26130-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="26130-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="26130-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="26130-369">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="26130-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="26130-p115">Aktivieren der postfachüberwachungsprotokollierung für Besitzer-, Stellvertreter-und Administratorzugriff auf das Drittanbieter-Daten Postfach Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md). Auf diese Weise können Sie alle Aktivitäten überwachen, die von jedem Benutzer ausgeführt werden, der Zugriff auf das Drittanbieter-Daten Postfach hat.</span><span class="sxs-lookup"><span data-stu-id="26130-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="26130-372">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="26130-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="26130-p116">Im nächsten Schritt werden Benutzerpostfächer für die Unterstützung von drittanbieterdaten konfiguriert. Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="26130-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="26130-375">Aktivieren Sie das Archivpostfach für jeden Benutzer; Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [Archivierung in Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="26130-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="26130-376">Platzieren von Benutzerpostfächern für die Aufbewahrung von Rechtsstreitigkeiten oder Anwenden einer Office 365-Archivierungsrichtlinie Lesen Sie eines der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="26130-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="26130-377">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="26130-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="26130-378">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="26130-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="26130-379">Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26130-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="26130-380">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="26130-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="26130-381">Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren.</span><span class="sxs-lookup"><span data-stu-id="26130-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="26130-382">Der Endpunkt, der zum Herstellen einer Verbindung mit dem Azure-Dienst in Office 365 verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="26130-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="26130-p117">Die Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) des Drittanbieter-Daten Postfachs, das Sie in Schritt 2 erstellt haben. Diese Anmeldeinformationen sind erforderlich, damit der Partner-Connector auf Elemente zugreifen und diese in Benutzerpostfächer und das Drittanbieter-Daten Postfach importieren kann.</span><span class="sxs-lookup"><span data-stu-id="26130-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="26130-385">Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="26130-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="26130-p118">Ab dem 30. September 2018 beginnt der Azure-Dienst in Office 365 mit der Verwendung der modernen Authentifizierung in Exchange Online, um Drittanbieter-Datenkonnektoren zu authentifizieren, die versuchen, eine Verbindung mit Ihrer Office 365-Organisation herzustellen, um Daten zu importieren. Der Grund für diese Änderung besteht darin, dass die moderne Authentifizierung mehr Sicherheit bietet als die aktuelle Methode, die auf dem Whitelisting von Drittanbieter-Connectors basiert, die den zuvor beschriebenen Endpunkt zum Herstellen einer Verbindung mit dem Azure-Dienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="26130-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="26130-p119">Damit ein Drittanbieter-Datenkonnektor mit der neuen modernen Authentifizierungsmethode eine Verbindung mit Office 365 herstellen kann, muss ein Administrator in Ihrer Office 365-Organisation mit der Registrierung des Connectors als vertrauenswürdige Dienstanwendung in Azure Active Directory einverstanden sein. Hierzu wird eine Berechtigungsanforderung akzeptiert, damit der Connector auf die Daten Ihrer Organisation in Azure Active Directory zugreifen kann. Nachdem Sie diese Anforderung angenommen haben, wird der Drittanbieter-Datenkonnektor als Unternehmensanwendung zu Azure Active Directory hinzugefügt und als Dienstprinzipal dargestellt. Weitere Informationen zum Zustimmungsprozess finden Sie unter [mandantEnadministrator-Einwilligung](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="26130-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="26130-392">Hier sind die Schritte zum Zugreifen auf und akzeptieren der Anforderung zur Registrierung des Connectors:</span><span class="sxs-lookup"><span data-stu-id="26130-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="26130-393">Wechseln Sie zu [dieser Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) , und melden Sie sich mit den Anmeldeinformationen eines globalen Office 365-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="26130-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="26130-p120">Das folgende Dialogfeld wird angezeigt. Sie können die "Carets" erweitern, um die Berechtigungen zu überarbeiten, die dem Connector zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="26130-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="26130-396">![Das Dialogfeld Berechtigungsanforderung wird angezeigt.](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="26130-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="26130-397">Klicken Sie auf **annehmen**.</span><span class="sxs-lookup"><span data-stu-id="26130-397">Click **Accept**.</span></span>

<span data-ttu-id="26130-p121">Nachdem Sie die Anforderung akzeptiert haben, wird das [Azure-Portal](https://portal.azure.com) angezeigt. Klicken Sie auf **Azure Active Directory** > -**Unternehmensanwendungen**, um die Liste der Anwendungen für Ihre Organisation anzuzeigen. Der Office 365-Drittanbieter-Daten-Konnektor ist auf dem Blade **Enterprise-Anwendungen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="26130-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26130-p122">Nach dem 30. September 2018 werden drittanbieterdaten nicht mehr in Postfächer in Ihrer Organisation importiert, wenn Sie keinen Drittanbieter-Daten-Konnektor in Azure Active Directory registrieren. Hinweis vorhandene Drittanbieter-Datenkonnektoren (die vor dem 30. September 2018 erstellt wurden) müssen auch in Azure Active Directory registriert werden, indem Sie das Verfahren in Schritt 5 befolgen.</span><span class="sxs-lookup"><span data-stu-id="26130-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="26130-403">Widerrufen der Zustimmung für einen Drittanbieter-Daten-Konnektor</span><span class="sxs-lookup"><span data-stu-id="26130-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="26130-p123">Nachdem Ihre Organisation der Berechtigungsanforderung zur Registrierung eines Drittanbieter-Daten-Konnektors in Azure Active Directory zugestimmt hat, kann Ihre Organisation diese Einwilligung jederzeit widerrufen. Das Widerrufen der Zustimmung für einen Connector bedeutet jedoch, dass Daten aus der Drittanbieter-Datenquelle nicht mehr in Office 365 importiert werden.</span><span class="sxs-lookup"><span data-stu-id="26130-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="26130-p124">Um die Einwilligung für einen Drittanbieter-Datenkonnektor zu widerrufen, können Sie die Anwendung (durch Löschen des entsprechenden Dienst Prinzipals) aus Azure Active Directory mithilfe des Blades " **Enterprise-Anwendungen** " im Azure-Portal oder mithilfe der [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Sie können auch das Cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) in Azure Active Directory PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="26130-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="26130-408">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26130-408">More information</span></span>

- <span data-ttu-id="26130-p125">Wie bereits erläutert, werden Elemente aus drittanbieterdaten Quellen als e-Mail-Nachrichten in Exchange-Postfächer importiert. Der Partner-Konnektor importiert das Element mithilfe eines für die Office 365-API erforderlichen Schemas. In der folgenden Tabelle werden die Nachrichteneigenschaften eines Elements aus einer Drittanbieter-Datenquelle beschrieben, nachdem es in ein Exchange-Postfach als e-Mail-Nachricht importiert wurde. Die Tabelle gibt auch an, ob die Message-Eigenschaft obligatorisch ist. Obligatorische Eigenschaften müssen aufgefüllt werden. Wenn für ein Element eine obligatorische Eigenschaft fehlt, wird es nicht in Office 365 importiert. Der Importprozess gibt eine Fehlermeldung zurück, die erklärt, warum ein Element nicht importiert wurde und welche Eigenschaft fehlt.</span><span class="sxs-lookup"><span data-stu-id="26130-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="26130-416">**Nachrichteneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="26130-416">**Message property**</span></span>|<span data-ttu-id="26130-417">**Obligatorisch?**</span><span class="sxs-lookup"><span data-stu-id="26130-417">**Mandatory?**</span></span>|<span data-ttu-id="26130-418">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26130-418">**Description**</span></span>|<span data-ttu-id="26130-419">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="26130-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="26130-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="26130-420">**FROM**</span></span> <br/> |<span data-ttu-id="26130-421">Ja</span><span class="sxs-lookup"><span data-stu-id="26130-421">Yes</span></span>  <br/> |<span data-ttu-id="26130-p126">Der Benutzer, der das Element ursprünglich erstellt oder in der Drittanbieter-Datenquelle gesendet hat. Der Partner-Konnektor versucht, die Benutzer-ID aus dem Quellelement (beispielsweise einem Twitter-handle) einem Office 365-Benutzerkonto für alle Teilnehmer (Benutzer in den Feldern von und bis) zuzuordnen. Eine Kopie der Nachricht wird in das Postfach jedes Teilnehmers importiert. Wenn keiner der Teilnehmer des Elements einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element in das Archivierungs Postfach eines Drittanbieters in Office 365 importiert.</span><span class="sxs-lookup"><span data-stu-id="26130-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="26130-p127">Der Teilnehmer, der als Absender des Elements identifiziert wird, muss über ein aktives Postfach in der Office 365-Organisation verfügen, in das das Element importiert wird. Wenn der Absender nicht über ein aktives Postfach verfügt, wird der folgende Fehler zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="26130-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="26130-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="26130-428">**TO**</span></span> <br/> |<span data-ttu-id="26130-429">Ja</span><span class="sxs-lookup"><span data-stu-id="26130-429">Yes</span></span>  <br/> |<span data-ttu-id="26130-430">Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).</span><span class="sxs-lookup"><span data-stu-id="26130-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="26130-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="26130-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="26130-432">Nein</span><span class="sxs-lookup"><span data-stu-id="26130-432">No</span></span>  <br/> |<span data-ttu-id="26130-433">Der Betreff des Quellelements.</span><span class="sxs-lookup"><span data-stu-id="26130-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="26130-434">**Datum**</span><span class="sxs-lookup"><span data-stu-id="26130-434">**DATE**</span></span> <br/> |<span data-ttu-id="26130-435">Ja</span><span class="sxs-lookup"><span data-stu-id="26130-435">Yes</span></span>  <br/> |<span data-ttu-id="26130-436">Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.</span><span class="sxs-lookup"><span data-stu-id="26130-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="26130-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="26130-437">**BODY**</span></span> <br/> |<span data-ttu-id="26130-438">Nein</span><span class="sxs-lookup"><span data-stu-id="26130-438">No</span></span>  <br/> |<span data-ttu-id="26130-p128">Der Inhalt der Nachricht oder des Beitrags. Bei einigen Datenquellen kann der Inhalt dieser Eigenschaft mit dem Inhalt der **Subject** -Eigenschaft identisch sein. Während des Importvorgangs versucht der Partner-Konnektor, die vollständige Originaltreue aus der Inhaltsquelle zu erhalten. Wenn möglich, Dateien, Grafiken oder andere Inhalte aus dem Text des Quellelements in dieser Eigenschaft enthalten sind. Andernfalls wird der Inhalt des Quellelements in die **Attachment** -Eigenschaft eingeschlossen. Der Inhalt dieser Eigenschaft hängt vom Partner-Konnektor und von der Funktion der QuellPlattform ab.</span><span class="sxs-lookup"><span data-stu-id="26130-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="26130-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="26130-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="26130-446">Nein</span><span class="sxs-lookup"><span data-stu-id="26130-446">No</span></span>  <br/> |<span data-ttu-id="26130-p129">Wenn ein Element in der Datenquelle (beispielsweise ein tweet in Twitter oder eine Sofortnachrichtenunterhaltung) über eine angefügte Datei verfügt oder Bilder enthält, versucht der Partner Connect zunächst, Anlagen in die **Body** -Eigenschaft einzuschließen. Wenn dies nicht möglich ist, wird Sie der \* \* ATTACHMENT \* \*-Eigenschaft hinzugefügt. Weitere Beispiele für Anlagen sind likes in Facebook, Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder einen Beitrag.</span><span class="sxs-lookup"><span data-stu-id="26130-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="26130-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="26130-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="26130-451">Ja</span><span class="sxs-lookup"><span data-stu-id="26130-451">Yes</span></span>  <br/> | <span data-ttu-id="26130-p130">Hierbei handelt es sich um eine mehrwertige Eigenschaft, die vom Partner-Konnektor erstellt und aufgefüllt wird. Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`. (Diese Eigenschaft muss mit `IPM.NOTE`beginnen; dieses Format ähnelt der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="26130-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="26130-455">`Source`-Gibt die Datenquelle eines Drittanbieters an. beispielsweise Twitter, Facebook oder BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="26130-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="26130-p131">`Event`-Gibt die Art der Aktivität an, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erstellt hat; zum Beispiel ein tweet in Twitter oder ein Beitrag in Facebook. Ereignisse sind spezifisch für die Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="26130-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="26130-p132">Ein Zweck dieser Eigenschaft besteht darin, bestimmte Elemente basierend auf der Datenquelle zu filtern, von der ein Element stammt oder auf dem Typ des Ereignisses basiert. In einer eDiscovery-Suche können Sie beispielsweise eine Suchabfrage erstellen, um alle Tweets zu finden, die von einem bestimmten Benutzer gepostet wurden.</span><span class="sxs-lookup"><span data-stu-id="26130-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="26130-p133">Wenn Elemente erfolgreich in Postfächer in Office 365 importiert werden, wird ein eindeutiger Bezeichner als Teil der HTTP-Antwort an den Aufrufer zurückgegeben. Dieser Bezeichner – genannt `x-IngestionCorrelationID`– kann für nachfolgende Problembehandlungszwecke von Partnern für die End-to-End-Nachverfolgung von Elementen verwendet werden. Es wird empfohlen, dass Partner diese Informationen erfassen und am Ende entsprechend protokollieren. Nachfolgend finden Sie ein Beispiel für eine HTTP-Antwort mit diesem Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="26130-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="26130-p134">Sie können das Inhaltssuche-Tool im Office 365 Security &amp; Compliance Center verwenden, um nach Elementen zu suchen, die in Postfächern in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Wenn Sie speziell nach diesen importierten Elementen suchen möchten, können Sie die folgenden Nachrichten Eigenschaftswert-Paare im Stichwortfeld für eine Inhaltssuche verwenden. .</span><span class="sxs-lookup"><span data-stu-id="26130-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="26130-p135">**`kind:externaldata`**-Verwenden Sie dieses Eigenschaft-Wert-Paar zum Durchsuchen aller Drittanbieter-Datentypen. Wenn Sie beispielsweise nach Elementen suchen möchten, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in der Subject-Eigenschaft des importierten Elements enthalten haben, würden Sie `kind:externaldata AND subject:contoso`die Stichwortabfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="26130-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="26130-p136">**`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses Eigenschaft-Wert-Paar nur, um einen angegebenen Typ von drittanbieterdaten zu durchsuchen. Wenn Sie beispielsweise nur Facebook-Daten durchsuchen möchten, die das Wort "Contoso" in der Subject-Eigenschaft enthalten, würden `itemclass:ipm.externaldata.Facebook* AND subject:contoso`Sie die Stichwortabfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="26130-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="26130-471">Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` Eigenschaft finden Sie unter Verwenden der [Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden](use-content-search-to-search-third-party-data-that-was-imported.md) .</span><span class="sxs-lookup"><span data-stu-id="26130-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="26130-472">Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="26130-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="26130-473">Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="26130-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="26130-474">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="26130-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 

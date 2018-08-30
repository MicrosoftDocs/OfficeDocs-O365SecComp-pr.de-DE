---
title: Archivieren von Drittanbieter-Daten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können Drittanbieter-Daten aus soziale Medien Plattformen, instant messaging-Plattformen und Dokument für die Zusammenarbeit Plattformen auf Postfächer in Office 365-Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und Datenquellen in Office 365 zu archivieren. Anschließend können Sie Appply Office 365 Compliance-Features (wie rechtliche Aufbewahrungspflicht, Inhaltssuche und Aufbewahrungsrichtlinien) auf Drittanbieter-Daten.
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230037"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="ce3b3-105">Archivieren von Drittanbieter-Daten in Office 365</span><span class="sxs-lookup"><span data-stu-id="ce3b3-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="ce3b3-p102">Office 365 ermöglicht Administratoren importieren und Archivieren von Drittanbieter-Daten von Plattformen soziale Medien, instant messaging-Plattformen und Collaboration-Plattformen Dokument auf Postfächer in Office 365-Organisation. Die folgenden: Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="ce3b3-108">**Social** - Twitter, Facebook, LinkedIn und Yammer</span><span class="sxs-lookup"><span data-stu-id="ce3b3-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="ce3b3-109">**Instant messaging** - Yahoo Messenger, GoogleTalk und Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="ce3b3-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="ce3b3-110">**Zusammenarbeit an Dokumenten** - Feld und Ablage</span><span class="sxs-lookup"><span data-stu-id="ce3b3-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="ce3b3-111">**Vertikale Branchen** - Customer Relationship Management (beispielsweise Vertriebs Anwendungsstörgeräusche) und Finanzen (wie Thomson Reuters und Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="ce3b3-112">**SMS-Text messaging** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ce3b3-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="ce3b3-p103">Nach dem Import Drittanbieter-Daten können Sie Office 365 Compliance-Features anwenden – beispielsweise Aufbewahrung für eventuelle Rechtsstreitigkeiten, Inhaltssuche, Compliance-Archivierung, Überwachung und Office 365 Aufbewahrungsrichtlinien – auf diese Daten. Wenn ein Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird, werden angenommen, Drittanbieter-Daten beibehalten. Sie können Drittanbieter-Daten mithilfe von Inhaltssuche suchen. Oder Sie können anwenden, Archivierung und Aufbewahrungsrichtlinien auf Drittanbieter-Daten wie für Microsoft Data. Kurz gesagt, helfen Archivierung von Drittanbieter-Daten in Office 365 Ihrer Organisation, die Einhaltung der behördlichen und behördlichen Richtlinien bleiben.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="ce3b3-118">Hier ist eine Übersicht über den Prozess und die Schritte zum Importieren von Drittanbieter-Daten zu Office 365 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="ce3b3-119">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="ce3b3-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="ce3b3-120">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ce3b3-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="ce3b3-121">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ce3b3-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="ce3b3-122">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="ce3b3-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="ce3b3-123">Funktioniert wie die Daten von Drittanbieter-Prozess Importieren ></span><span class="sxs-lookup"><span data-stu-id="ce3b3-123">How the third-party data import process works></span></span>

<span data-ttu-id="ce3b3-124">Die folgende Abbildung und die Beschreibung erläutern, wie der Prozess zum Importieren von Drittanbieterdaten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-124">The following illustration and description explain how the third-party data import process works.</span></span>
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="ce3b3-126">Kunden arbeitet mit Partner Wahl eine Verbindung konfigurieren, die Elemente aus der Drittanbieter-Datenquelle extrahiert und dann diese Elemente zu Office 365 importieren.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-126">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="ce3b3-p104">Der Partner-Connector Drittanbieter-Datenquellen über einen Drittanbieter-API (auf Basis geplant oder als konfiguriert) her und extrahiert Elemente aus der Datenquelle. Der Partner Connector konvertiert den Inhalt eines Elements in einer e-Mail-Format. Finden Sie [Weitere Informationen](#more-information) im Abschnitt für eine Beschreibung des Message-Format-Schemas.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="ce3b3-130">Partner-Connector stellt eine Verbindung mit dem Azure-Dienst in Office 365 mithilfe von Dienst (Exchange Web Services, EWS) über eine bekannte Endpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-130">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="ce3b3-p105">Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="ce3b3-p106">a **Elemente verfügen, die eine Benutzer-ID, die ein Benutzerkonto für Office 365 entspricht** -Wenn Sie der Connector Partner die Benutzer-ID des Elements in der Drittanbieter-Datenquelle für einen bestimmten Benutzer zugeordnet werden kann, die in den Ordner **Löscht ein** , in des Benutzers-ID in Office 365, das Element kopiert werden. Ordner "wiederherstellbare Elemente". Benutzer können keine Elemente im Ordner Benutzerkontenverwaltung zugreifen. EDiscovery-Tools für Office 365 können Sie jedoch um für Elemente im Ordner Benutzerkontenverwaltung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="ce3b3-p107">b. **Elemente, die eine Benutzer-ID besitzen, die ein Office 365-Benutzerkonto entspricht** – Falls der Partner-Connector die Benutzer-ID eines Elements zu einem bestimmten Benutzer zuordnen kann nicht-ID in Office 365, das Element in den Ordner **Posteingang** des Postfachs Drittanbieter-Daten kopiert werden. Importieren von Elementen in den Posteingang können Sie oder eine Person in Ihrer Organisation So melden Sie sich an das Postfach von Drittanbietern zum Anzeigen und Verwalten von dieser Elemente sowie überprüfen, ob alle Korrekturen in der Connectorkonfiguration Partner getroffen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="ce3b3-140">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="ce3b3-140">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="ce3b3-p108">Eine wichtige Komponente für die Archivierung von Drittanbieter-Daten in Office 365 ist Suchen von und Arbeiten mit einem Microsoft-Partner, die sich auf in Sammeln von Daten aus einer Drittanbieter-Datenquelle und importieren es in Office 365. Nachdem die Daten importiert werden, es kann archiviert und beibehalten zusammen mit Ihrer Organisation des anderen Microsoft-Daten, wie beispielsweise e-Mail-Nachrichten von Exchange und Dokumente aus SharePoint und OneDrive für Unternehmen. Ein Partner erstellt einen Connector, der Daten aus Ihrer Organisation Drittanbieter-Datenquellen (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) extrahiert und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächern als importiert e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="ce3b3-144">In den folgenden Abschnitten aufgelistet, die Microsoft-Partner – und Drittanbieter-Datenquellen, die sie unterstützen –, die die Anwendung für die Archivierung von Drittanbieter-Daten in Office 365 beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-144">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="ce3b3-145">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="ce3b3-145">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="ce3b3-146">Actiance</span><span class="sxs-lookup"><span data-stu-id="ce3b3-146">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="ce3b3-147">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="ce3b3-147">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="ce3b3-148">Globanet</span><span class="sxs-lookup"><span data-stu-id="ce3b3-148">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="ce3b3-149">OpenText</span><span class="sxs-lookup"><span data-stu-id="ce3b3-149">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="ce3b3-150">Verba</span><span class="sxs-lookup"><span data-stu-id="ce3b3-150">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="ce3b3-151">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="ce3b3-151">17a-4 LLC</span></span>

<span data-ttu-id="ce3b3-152">17a-4 LLC unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-152">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="ce3b3-153">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ce3b3-153">BlackBerry</span></span>
    
- <span data-ttu-id="ce3b3-154">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="ce3b3-154">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="ce3b3-155">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="ce3b3-155">Cisco Jabber</span></span>
    
- <span data-ttu-id="ce3b3-156">FactSet</span><span class="sxs-lookup"><span data-stu-id="ce3b3-156">FactSet</span></span>
    
- <span data-ttu-id="ce3b3-157">HipChat</span><span class="sxs-lookup"><span data-stu-id="ce3b3-157">HipChat</span></span>
    
- <span data-ttu-id="ce3b3-158">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="ce3b3-158">InvestEdge</span></span>
    
- <span data-ttu-id="ce3b3-159">LivePerson</span><span class="sxs-lookup"><span data-stu-id="ce3b3-159">LivePerson</span></span>
    
- <span data-ttu-id="ce3b3-160">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-160">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="ce3b3-161">OpenText</span><span class="sxs-lookup"><span data-stu-id="ce3b3-161">OpenText</span></span>
    
- <span data-ttu-id="ce3b3-162">Live-Hilfe für Oracle/ATG 'click-to-call'
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-162">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="ce3b3-163">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-163">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="ce3b3-164">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce3b3-164">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="ce3b3-165">MindAlign</span><span class="sxs-lookup"><span data-stu-id="ce3b3-165">MindAlign</span></span>
    
- <span data-ttu-id="ce3b3-166">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-166">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="ce3b3-167">
Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-167">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="ce3b3-168">
Skype for Business Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-168">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="ce3b3-169">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ce3b3-169">SQL Databases</span></span>
    
- <span data-ttu-id="ce3b3-170">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-170">Squawker</span></span>
    
- <span data-ttu-id="ce3b3-171">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-171">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="ce3b3-172">Actiance</span><span class="sxs-lookup"><span data-stu-id="ce3b3-172">Actiance</span></span>

<span data-ttu-id="ce3b3-173">[Actiance](https://www.actiance.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-173">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="ce3b3-174">AIM</span><span class="sxs-lookup"><span data-stu-id="ce3b3-174">AIM</span></span>
    
- <span data-ttu-id="ce3b3-175">American Idol</span><span class="sxs-lookup"><span data-stu-id="ce3b3-175">American Idol</span></span>
    
- <span data-ttu-id="ce3b3-176">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="ce3b3-176">Apple Juice</span></span>
    
- <span data-ttu-id="ce3b3-177">
AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-177">AOL with Pivot client</span></span>
    
- <span data-ttu-id="ce3b3-178">Ares</span><span class="sxs-lookup"><span data-stu-id="ce3b3-178">Ares</span></span>
    
- <span data-ttu-id="ce3b3-179">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="ce3b3-179">Bazaar Voice</span></span>
    
- <span data-ttu-id="ce3b3-180">Bear Share</span><span class="sxs-lookup"><span data-stu-id="ce3b3-180">Bear Share</span></span>
    
- <span data-ttu-id="ce3b3-181">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="ce3b3-181">Bit Torrent</span></span>
    
- <span data-ttu-id="ce3b3-182">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-182">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-183">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-183">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-184">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-184">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-185">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-185">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-186">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-186">Bloomberg Mail</span></span>
    
- <span data-ttu-id="ce3b3-187">CellTrust</span><span class="sxs-lookup"><span data-stu-id="ce3b3-187">CellTrust</span></span>
    
- <span data-ttu-id="ce3b3-188">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-188">Chat Import</span></span>
    
- <span data-ttu-id="ce3b3-189">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-189">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="ce3b3-190">Chatter
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-190">Chatter</span></span>
    
- <span data-ttu-id="ce3b3-191">Cisco Sofortnachrichten &amp; Anwesenheitsserver (v9.0.1, 9.1, v9.1.1 SU1, v10 v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-191">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="ce3b3-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="ce3b3-193">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-193">Collaboration Import</span></span>
    
- <span data-ttu-id="ce3b3-194">Echtzeitprotokollierung für Zusammenarbeit
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-194">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="ce3b3-195">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="ce3b3-195">Direct Connect</span></span>
    
- <span data-ttu-id="ce3b3-196">Facebook</span><span class="sxs-lookup"><span data-stu-id="ce3b3-196">Facebook</span></span>
    
- <span data-ttu-id="ce3b3-197">FactSet</span><span class="sxs-lookup"><span data-stu-id="ce3b3-197">FactSet</span></span>
    
- <span data-ttu-id="ce3b3-198">FastTrack</span><span class="sxs-lookup"><span data-stu-id="ce3b3-198">FastTrack</span></span>
    
- <span data-ttu-id="ce3b3-199">Gnutella</span><span class="sxs-lookup"><span data-stu-id="ce3b3-199">Gnutella</span></span>
    
- <span data-ttu-id="ce3b3-200">Google+
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-200">Google+</span></span>
    
- <span data-ttu-id="ce3b3-201">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="ce3b3-201">GoToMyPC</span></span>
    
- <span data-ttu-id="ce3b3-202">Hopster</span><span class="sxs-lookup"><span data-stu-id="ce3b3-202">Hopster</span></span>
    
- <span data-ttu-id="ce3b3-203">HubConnex</span><span class="sxs-lookup"><span data-stu-id="ce3b3-203">HubConnex</span></span>
    
- <span data-ttu-id="ce3b3-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="ce3b3-205">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-205">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="ce3b3-206">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-206">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="ce3b3-207">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-207">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="ce3b3-208">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-208">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="ce3b3-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="ce3b3-210">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-210">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="ce3b3-211">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-211">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="ce3b3-212">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-212">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="ce3b3-213">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="ce3b3-213">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="ce3b3-214">Chat-Import
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-214">IM Import</span></span>
    
- <span data-ttu-id="ce3b3-215">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-215">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="ce3b3-216">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-216">Indii Messenger</span></span>
    
- <span data-ttu-id="ce3b3-217">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-217">Instant Bloomberg</span></span>
    
- <span data-ttu-id="ce3b3-218">IRC</span><span class="sxs-lookup"><span data-stu-id="ce3b3-218">IRC</span></span>
    
- <span data-ttu-id="ce3b3-219">Jive
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-219">Jive</span></span>
    
- <span data-ttu-id="ce3b3-220">Jive 6 Real Time Logging (v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-220">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="ce3b3-221">Jive Import</span><span class="sxs-lookup"><span data-stu-id="ce3b3-221">Jive Import</span></span>
    
- <span data-ttu-id="ce3b3-222">JXTA</span><span class="sxs-lookup"><span data-stu-id="ce3b3-222">JXTA</span></span>
    
- <span data-ttu-id="ce3b3-223">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="ce3b3-223">LinkedIn</span></span>
    
- <span data-ttu-id="ce3b3-224">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-224">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="ce3b3-225">MFTP</span><span class="sxs-lookup"><span data-stu-id="ce3b3-225">MFTP</span></span>
    
- <span data-ttu-id="ce3b3-226">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-226">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="ce3b3-227">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-227">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="ce3b3-228">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ce3b3-228">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="ce3b3-229">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-229">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="ce3b3-230">MindAlign</span><span class="sxs-lookup"><span data-stu-id="ce3b3-230">MindAlign</span></span>
    
- <span data-ttu-id="ce3b3-231">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="ce3b3-231">Mobile Guard</span></span>
    
- <span data-ttu-id="ce3b3-232">MSN</span><span class="sxs-lookup"><span data-stu-id="ce3b3-232">MSN</span></span>
    
- <span data-ttu-id="ce3b3-233">My Space</span><span class="sxs-lookup"><span data-stu-id="ce3b3-233">My Space</span></span>
    
- <span data-ttu-id="ce3b3-234">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="ce3b3-234">NEONetwork</span></span>
    
- <span data-ttu-id="ce3b3-235">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-235">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="ce3b3-236">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-236">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="ce3b3-237">Pinterest</span><span class="sxs-lookup"><span data-stu-id="ce3b3-237">Pinterest</span></span>
    
- <span data-ttu-id="ce3b3-238">Pivot</span><span class="sxs-lookup"><span data-stu-id="ce3b3-238">Pivot</span></span>
    
- <span data-ttu-id="ce3b3-239">QQ</span><span class="sxs-lookup"><span data-stu-id="ce3b3-239">QQ</span></span>
    
- <span data-ttu-id="ce3b3-240">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="ce3b3-240">Skype for Business 2015</span></span>
    
- <span data-ttu-id="ce3b3-241">SoftEther</span><span class="sxs-lookup"><span data-stu-id="ce3b3-241">SoftEther</span></span>
    
- <span data-ttu-id="ce3b3-242">Symphony
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-242">Symphony</span></span>
    
- <span data-ttu-id="ce3b3-243">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-243">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="ce3b3-244">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-244">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="ce3b3-245">Tor</span><span class="sxs-lookup"><span data-stu-id="ce3b3-245">Tor</span></span>
    
- <span data-ttu-id="ce3b3-246">TTT</span><span class="sxs-lookup"><span data-stu-id="ce3b3-246">TTT</span></span>
    
- <span data-ttu-id="ce3b3-247">Twitter</span><span class="sxs-lookup"><span data-stu-id="ce3b3-247">Twitter</span></span>
    
- <span data-ttu-id="ce3b3-248">WinMX</span><span class="sxs-lookup"><span data-stu-id="ce3b3-248">WinMX</span></span>
    
- <span data-ttu-id="ce3b3-249">Winny</span><span class="sxs-lookup"><span data-stu-id="ce3b3-249">Winny</span></span>
    
- <span data-ttu-id="ce3b3-250">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-250">Yahoo</span></span>
    
- <span data-ttu-id="ce3b3-251">Yammer</span><span class="sxs-lookup"><span data-stu-id="ce3b3-251">Yammer</span></span>
    
- <span data-ttu-id="ce3b3-252">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-252">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="ce3b3-253">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="ce3b3-253">ArchiveSocial</span></span>

<span data-ttu-id="ce3b3-254">[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-254">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="ce3b3-255">Facebook</span><span class="sxs-lookup"><span data-stu-id="ce3b3-255">Facebook</span></span>
    
- <span data-ttu-id="ce3b3-256">Flickr
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-256">Flickr</span></span>
    
- <span data-ttu-id="ce3b3-257">Instagram
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-257">Instagram</span></span>
    
- <span data-ttu-id="ce3b3-258">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="ce3b3-258">LinkedIn</span></span>
    
- <span data-ttu-id="ce3b3-259">Pinterest</span><span class="sxs-lookup"><span data-stu-id="ce3b3-259">Pinterest</span></span>
    
- <span data-ttu-id="ce3b3-260">Twitter</span><span class="sxs-lookup"><span data-stu-id="ce3b3-260">Twitter</span></span>
    
- <span data-ttu-id="ce3b3-261">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-261">YouTube</span></span>
    
- <span data-ttu-id="ce3b3-262">Vimeo</span><span class="sxs-lookup"><span data-stu-id="ce3b3-262">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="ce3b3-263">Globanet</span><span class="sxs-lookup"><span data-stu-id="ce3b3-263">Globanet</span></span>

<span data-ttu-id="ce3b3-264">[Globanet](https://www.globanet.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-264">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="ce3b3-265">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-265">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="ce3b3-266">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-266">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-267">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-267">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-268">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-268">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-269">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-269">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="ce3b3-270">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-270">Bloomberg Chat</span></span>
    
- <span data-ttu-id="ce3b3-271">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-271">Bloomberg Mail</span></span>
    
- <span data-ttu-id="ce3b3-272">Box
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-272">Box</span></span>
    
- <span data-ttu-id="ce3b3-273">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="ce3b3-273">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="ce3b3-274">Cisco Sofortnachrichten &amp; Anwesenheitsserver (V11. v10 v10.5.1 SU1, 0, "v11.5 SU2")</span><span class="sxs-lookup"><span data-stu-id="ce3b3-274">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="ce3b3-275">Cisco Webex Teams</span><span class="sxs-lookup"><span data-stu-id="ce3b3-275">Cisco Webex Teams</span></span>

- <span data-ttu-id="ce3b3-276">Citrix Workspace &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="ce3b3-276">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="ce3b3-277">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="ce3b3-277">CrowdCompass</span></span>

- <span data-ttu-id="ce3b3-278">Durch Trennzeichen getrennte, benutzerdefinierte Textdateien
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-278">Custom delimited text files</span></span>
    
- <span data-ttu-id="ce3b3-279">Benutzerdefinierte XML-Dateien
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-279">Custom XML files</span></span>
    
- <span data-ttu-id="ce3b3-280">Facebook (Seiten)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-280">Facebook (Pages)</span></span>
    
- <span data-ttu-id="ce3b3-281">Factset
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-281">Factset</span></span>
    
- <span data-ttu-id="ce3b3-282">FXConnect</span><span class="sxs-lookup"><span data-stu-id="ce3b3-282">FXConnect</span></span>
    
- <span data-ttu-id="ce3b3-283">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="ce3b3-283">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="ce3b3-284">Jive
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-284">Jive</span></span>
    
- <span data-ttu-id="ce3b3-285">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-285">Macgregor XIP</span></span>

- <span data-ttu-id="ce3b3-286">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="ce3b3-286">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="ce3b3-287">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="ce3b3-287">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="ce3b3-288">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ce3b3-288">Microsoft Teams</span></span>
       
- <span data-ttu-id="ce3b3-289">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-289">Microsoft Yammer</span></span>
    
- <span data-ttu-id="ce3b3-290">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="ce3b3-290">Mobile Guard</span></span>
    
- <span data-ttu-id="ce3b3-291">Pivot</span><span class="sxs-lookup"><span data-stu-id="ce3b3-291">Pivot</span></span>
    
- <span data-ttu-id="ce3b3-292">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="ce3b3-292">Salesforce Chatter</span></span>

- <span data-ttu-id="ce3b3-293">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="ce3b3-293">Skype for Business Online</span></span>
    
- <span data-ttu-id="ce3b3-294">Skype for Business, Versionen 2007 R2 - 2016 (lokal)
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-294">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="ce3b3-295">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="ce3b3-295">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="ce3b3-296">Symphony
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-296">Symphony</span></span>
    
- <span data-ttu-id="ce3b3-297">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-297">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="ce3b3-298">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-298">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="ce3b3-299">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-299">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="ce3b3-300">Twitter</span><span class="sxs-lookup"><span data-stu-id="ce3b3-300">Twitter</span></span>
    
- <span data-ttu-id="ce3b3-301">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-301">UBS Chat</span></span>
    
- <span data-ttu-id="ce3b3-302">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-302">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="ce3b3-303">OpenText</span><span class="sxs-lookup"><span data-stu-id="ce3b3-303">OpenText</span></span>

<span data-ttu-id="ce3b3-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="ce3b3-305">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="ce3b3-305">Axs Encrypted</span></span>
    
- <span data-ttu-id="ce3b3-306">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="ce3b3-306">Axs Exchange</span></span>
    
- <span data-ttu-id="ce3b3-307">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="ce3b3-307">Axs Local Archive</span></span>
    
- <span data-ttu-id="ce3b3-308">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="ce3b3-308">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="ce3b3-309">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="ce3b3-309">Axs Signed</span></span>
    
- <span data-ttu-id="ce3b3-310">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="ce3b3-310">Bloomberg</span></span>
    
- <span data-ttu-id="ce3b3-311">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="ce3b3-311">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="ce3b3-312">Verba</span><span class="sxs-lookup"><span data-stu-id="ce3b3-312">Verba</span></span>

<span data-ttu-id="ce3b3-313">[Verba](https://www.verba.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-313">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="ce3b3-314">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-314">Avaya Aura Video</span></span>
    
- <span data-ttu-id="ce3b3-315">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-315">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="ce3b3-316">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-316">Avtec Radio</span></span>
    
- <span data-ttu-id="ce3b3-317">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-317">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="ce3b3-318">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-318">BroadSoft Video</span></span>
    
- <span data-ttu-id="ce3b3-319">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-319">BroadSoft Voice</span></span>
    
- <span data-ttu-id="ce3b3-320">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-320">Centile Voice</span></span>
    
- <span data-ttu-id="ce3b3-321">Chatnachricht in Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="ce3b3-321">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="ce3b3-322">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-322">Cisco UC Video</span></span>
    
- <span data-ttu-id="ce3b3-323">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-323">Cisco UC Voice</span></span>
    
- <span data-ttu-id="ce3b3-324">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="ce3b3-324">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="ce3b3-325">Cisco UCCX/UCCE VoIP</span><span class="sxs-lookup"><span data-stu-id="ce3b3-325">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="ce3b3-326">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="ce3b3-326">ESChat Radio</span></span>
    
- <span data-ttu-id="ce3b3-327">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="ce3b3-327">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="ce3b3-328">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-328">IP Trade Voice</span></span>
    
- <span data-ttu-id="ce3b3-329">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="ce3b3-329">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="ce3b3-330">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-330">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="ce3b3-331">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-331">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="ce3b3-332">Oracle/Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-332">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="ce3b3-333">Oracle/Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-333">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="ce3b3-334">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-334">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="ce3b3-335">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="ce3b3-335">SIPREC Video</span></span>
    
-  <span data-ttu-id="ce3b3-336">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="ce3b3-336">SIPREC Voice</span></span> 
    
- <span data-ttu-id="ce3b3-337">Chatnachricht in Skype for Business/Lync
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-337">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="ce3b3-338">Skype for Business/Lync Video
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-338">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="ce3b3-339">Skype for Business/Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-339">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="ce3b3-340">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-340">Speakerbus Voice</span></span>
    
- <span data-ttu-id="ce3b3-341">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-341">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="ce3b3-342">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-342">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="ce3b3-343">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-343">Truphone Voice</span></span>
    
- <span data-ttu-id="ce3b3-344">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-344">TwistedPair Radio</span></span>
    
- <span data-ttu-id="ce3b3-345">Windows Desktop-Computerbildschirm 
</span><span class="sxs-lookup"><span data-stu-id="ce3b3-345">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="ce3b3-346">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ce3b3-346">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="ce3b3-p109">Hier sind die Schritte zum Erstellen und Konfigurieren eines Postfachs Drittanbieter-Daten für das Importieren von Daten in Office 365. Wie vorherige erläutert, Elemente auf dieses Postfach importiert werden, wenn der Partner-Connector die Benutzer-ID des Elements ein Benutzerkonto für Office 365 zugeordnet ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="ce3b3-349">**Führen Sie diese Aufgaben in Office 365 Administrationscenter**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-349">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="ce3b3-p110">Erstellen eines neuen Benutzerkontos in Office 365, und weisen Sie es mit einer Lizenzvertrags für Exchange Online – Plan 2; finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). So platzieren das Postfach in die Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Aktivieren eines archivpostfachs, das eine unbegrenzte Speicherkontingent hat, ist eine Plan 2-Lizenz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="ce3b3-352">Fügen Sie das Benutzerkonto für das Postfach von Drittanbieter-Daten für die **Exchange-Administrator** -Admin-Rolle in Office 365; finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="ce3b3-352">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="ce3b3-p111">Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto. Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="ce3b3-355">**Führen Sie diese Aufgaben in der Exchange-Verwaltungskonsole**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-355">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="ce3b3-p112">Ausblenden des Postfachs Drittanbieter-Daten aus dem Adressbuch und andere Adresslisten in Ihrer Organisation; finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternativ können Sie den folgenden PowerShell-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="ce3b3-358">Weisen Sie die Berechtigung **FullAccess** das Postfach von Drittanbieter-Daten, damit Administratoren oder Compliance Officer das Postfach von Drittanbietern Daten im Outlook-Desktopclient geöffnet werden können; finden Sie unter [Verwalten von Berechtigungen für Empfänger](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="ce3b3-358">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="ce3b3-359">Aktivieren Sie die folgenden Compliance-bezogene Office 365-Features für das Postfach von Drittanbieter-Daten:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-359">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="ce3b3-p113">Aktivieren Sie das Archivpostfach; finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md). Auf diese Weise können Sie frei bis Speicherplatz in das primäre Postfach durch Einrichten einer Archivrichtlinie, die Elemente von Drittanbieter-Daten in das Archivpostfach verschoben. Dies stellt Sie unbegrenzte Speicher für Drittanbieter-Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="ce3b3-p114">Platzieren Sie das Postfach von Drittanbieter-Daten in die Aufbewahrung für eventuelle Rechtsstreitigkeiten. Sie können auch anwenden eine Aufbewahrungsrichtlinie Office 365 in die Office 365-Sicherheit &amp; Compliance Center. Platzieren dieses Postfach in der Warteschleife wird aufbewahren von von Drittanbieter-Datenelementen (auf unbestimmte Zeit oder für eine angegebene Dauer) und zu verhindern, aus dem Postfach gelöscht werden. Finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="ce3b3-367">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="ce3b3-367">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="ce3b3-368">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="ce3b3-368">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="ce3b3-p115">Aktivieren Sie die postfachüberwachungsprotokollierung für den Besitzer, Delegaten und Admin-Zugriff auf das Postfach von Drittanbietern Daten; finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](enable-mailbox-auditing.md). Dadurch können Sie alle Aktivitäten, die von jedem Benutzer mit Zugriff auf das Postfach von Drittanbietern Daten überwachen.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="ce3b3-371">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ce3b3-371">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="ce3b3-p116">Der nächste Schritt besteht darin Benutzerpostfächer zur Unterstützung von Drittanbieter-Daten konfigurieren. Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="ce3b3-374">Aktivieren Sie das Archivpostfach für jeden Benutzer. finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="ce3b3-374">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="ce3b3-375">Platzieren von Benutzerpostfächern in Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Anwenden einer Aufbewahrungsrichtlinie für Office 365. finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-375">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="ce3b3-376">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="ce3b3-376">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="ce3b3-377">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="ce3b3-377">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="ce3b3-378">Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-378">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="ce3b3-379">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="ce3b3-379">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="ce3b3-380">Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-380">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="ce3b3-381">Der Endpunkt für die Verbindung mit dem Azure-Dienst in Office 365 verwendet:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-381">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="ce3b3-p117">Die Anmeldung Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) für das Postfach von Drittanbieter-Daten, das Sie in Schritt2 erstellt haben. Diese Anmeldeinformationen sind erforderlich, damit der Partner-Connector zugreifen und Elemente für Benutzerpostfächer und an das Postfach von Drittanbietern Daten importieren kann.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
    

  
## <a name="more-information"></a><span data-ttu-id="ce3b3-384">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce3b3-384">More information</span></span>

- <span data-ttu-id="ce3b3-p118">Wie vorherige erläutert, Elemente von Drittanbieter-Daten, die in Exchange-Postfächern als e-Mail-Nachrichten Quellen importiert werden. Der Partner-Connector importiert das Element mit einem Schema, das von der Office 365-API erforderlich. In der folgenden Tabelle werden die Eigenschaften eines Elements aus einer Drittanbieter-Datenquelle beschrieben, nach dem Import auf einem Exchange-Postfach als e-Mail-Nachricht ist. Die Tabelle zeigt auch an, ob die Message-Eigenschaft zwingend erforderlich ist. Erforderliche Eigenschaften müssen aufgefüllt werden. Wenn ein Element eine erforderliche Eigenschaft nicht angezeigt wird, werden nicht es zu Office 365 importiert werden. Der Importvorgang wird eine Fehlermeldung angezeigt, die erklärt, warum ein Element wurde nicht importiert und welche Eigenschaft fehlt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p118">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="ce3b3-392">**Nachrichteneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-392">**Message property**</span></span>|<span data-ttu-id="ce3b3-393">**Zwingend erforderlich?**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-393">**Mandatory?**</span></span>|<span data-ttu-id="ce3b3-394">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-394">**Description**</span></span>|<span data-ttu-id="ce3b3-395">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-395">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="ce3b3-396">**FROM**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-396">**FROM**</span></span> <br/> |<span data-ttu-id="ce3b3-397">Ja</span><span class="sxs-lookup"><span data-stu-id="ce3b3-397">Yes</span></span>  <br/> |<span data-ttu-id="ce3b3-p119">Der Benutzer, die ursprünglich erstellt oder das Element in der Drittanbieter-Datenquelle gesendet. Der Partner-Verbindung versucht, die Benutzer-ID aus dem Quellelement (beispielsweise ein Handle Twitter) ein Benutzerkonto für Office 365 für alle Teilnehmer (Benutzer in die Felder FROM und TO) zuordnen. Eine Kopie der Nachricht wird an das Postfach von jedem Teilnehmer importiert werden. Wenn keines der Teilnehmer aus dem Element zu einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element auf das Postfach der Drittanbieter-Archivierung in Office 365 importiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p119">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="ce3b3-p120">Der Teilnehmer, der als Absender des Elements identifiziert wird benötigen kein active-Postfach in der Office 365-Organisation, die auf das Element importiert wird. Wenn der Absender eine aktive Postfach besitzt, wird die folgende Fehlermeldung zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p120">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="ce3b3-404">**TO**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-404">**TO**</span></span> <br/> |<span data-ttu-id="ce3b3-405">Ja</span><span class="sxs-lookup"><span data-stu-id="ce3b3-405">Yes</span></span>  <br/> |<span data-ttu-id="ce3b3-406">Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).</span><span class="sxs-lookup"><span data-stu-id="ce3b3-406">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="ce3b3-407">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-407">**SUBJECT**</span></span> <br/> |<span data-ttu-id="ce3b3-408">Nein</span><span class="sxs-lookup"><span data-stu-id="ce3b3-408">No</span></span>  <br/> |<span data-ttu-id="ce3b3-409">Der Betreff des Quellelements.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-409">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="ce3b3-410">**DATUM**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-410">**DATE**</span></span> <br/> |<span data-ttu-id="ce3b3-411">Ja</span><span class="sxs-lookup"><span data-stu-id="ce3b3-411">Yes</span></span>  <br/> |<span data-ttu-id="ce3b3-412">Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-412">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="ce3b3-413">**BODY**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-413">**BODY**</span></span> <br/> |<span data-ttu-id="ce3b3-414">Nein</span><span class="sxs-lookup"><span data-stu-id="ce3b3-414">No</span></span>  <br/> |<span data-ttu-id="ce3b3-p121">Der Inhalt der Nachricht oder des Beitrags. Für einige Datenquellen können den Inhalt dieser Eigenschaft des Inhalts für die **SUBJECT** -Eigenschaft identisch sein. Während des Importvorgangs versucht der Partner Connector originalgetreue aus der Inhaltsquelle wie möglich beizubehalten. Wenn möglich ist in dieser Eigenschaft Dateien, Grafiken oder andere Inhalte aus dem Textkörper des Quellelements enthalten. Andernfalls ist in der **Anlage** -Eigenschaft Inhalte aus dem Quellelement enthalten. Der Inhalt dieser Eigenschaft werden für den Connector Partner und für die Funktionalität der Source-Plattform abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p121">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="ce3b3-421">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-421">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="ce3b3-422">Nein</span><span class="sxs-lookup"><span data-stu-id="ce3b3-422">No</span></span>  <br/> |<span data-ttu-id="ce3b3-p122">Wenn ein Element in der Datenquelle (beispielsweise einen Tweet in Twitter oder einer Unterhaltung über Sofortnachrichten) hat eine angefügte Datei oder fügen Sie Bilder, Verbinden des Partners wird ersten Versuch zum Einschließen von Anlagen in die **BODY** -Eigenschaft. Wenn das ist nicht möglich, wird diese hinzugefügt der ** Anlage ** Eigenschaft. Weitere Beispiele für Anlagen sind "gefällt mir" in Facebook Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder ein Beitrag.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p122">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="ce3b3-426">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="ce3b3-426">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="ce3b3-427">Ja</span><span class="sxs-lookup"><span data-stu-id="ce3b3-427">Yes</span></span>  <br/> | <span data-ttu-id="ce3b3-p123">Dies ist eine mehrwertige-Eigenschaft, die erstellt und durch Partner Connector aufgefüllt wird. Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`. (Diese Eigenschaft muss zunächst `IPM.NOTE`; dieses Format ist vergleichbar mit der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p123">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="ce3b3-431">`Source`-Gibt die Drittanbieter-Datenquelle an. beispielsweise Twitter, Facebook oder BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-431">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="ce3b3-p124">`Event`-Gibt den Typ der Aktivität, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erzeugt an. beispielsweise einen Tweet in Twitter oder ein Beitrag in Facebook. Ereignisse sind für die Datenquelle spezifisch.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p124">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="ce3b3-p125">Ein Zweck von dieser Eigenschaft wird zum Filtern von bestimmter Elementen basierend auf die Datenquelle, an dem ein Element stammt oder basierend auf den Typ des Ereignisses. Beispielsweise können in einer eDiscovery-Suche Sie erstellen eine Suchabfrage aus, um alle Tweets zu suchen, die von einem bestimmten Benutzer veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p125">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="ce3b3-p126">Wenn Elemente auf Postfächer in Office 365 erfolgreich importiert wurden, wird eine eindeutige ID wieder an den Aufrufer als Teil der HTTP-Antwort zurückgegeben. Dieser Bezeichner – aufgerufen `x-IngestionCorrelationID`– aus Gründen nachfolgende zur Problembehandlung von Partnern für eine End-to-End-Überwachung von Elementen verwendet werden kann. Es wird empfohlen, dass Partner diese Informationen erfassen und melden Sie es entsprechend geleitet. Es folgt ein Beispiel für eine HTTP-Antwort, die mit diesem Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p126">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="ce3b3-p127">Sie können das Tool für die Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, um die Suche nach Elementen, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Um speziell für diese importierte Elemente zu suchen, können Sie die folgende Meldung-Wert-Paare im Schlüsselwort für ein Inhaltssuche verwenden. .</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p127">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="ce3b3-p128">**`kind:externaldata`**-Verwenden Sie diese Eigenschaft-Wert-Paar, um alle Arten von Drittanbietern suchen. Verwenden Sie beispielsweise, um die Suche nach Elementen, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in die Subject-Eigenschaft des importierten Elements enthalten die Stichwortabfrage `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p128">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="ce3b3-p129">**`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses-Eigenschaft-Wert-Paar nur Suche eines Datentyps Drittanbieter-angeben. Um nur Facebook Daten zu suchen, die das Wort "Contoso" in die Subject-Eigenschaft enthält, verwenden Sie beispielsweise die Stichwortabfrage `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="ce3b3-p129">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="ce3b3-447">Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` -Eigenschaft, finden Sie unter [Inhaltssuche verwenden, um Daten von Dritten zu suchen, die in Office 365 importiert wurde,](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="ce3b3-447">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="ce3b3-448">Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ce3b3-448">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="ce3b3-449">Content-Suche in Office 365</span><span class="sxs-lookup"><span data-stu-id="ce3b3-449">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="ce3b3-450">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="ce3b3-450">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 

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
ms.openlocfilehash: 7af88338333e90bd208d693fbfd5bb691d44b538
ms.sourcegitcommit: 4c6c937ec51e8b754332e4c1c8d286e73e197e2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2018
ms.locfileid: "23827089"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="6cf82-105">Archivieren von Drittanbieter-Daten in Office 365</span><span class="sxs-lookup"><span data-stu-id="6cf82-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="6cf82-p102">Office 365 ermöglicht Administratoren importieren und Archivieren von Drittanbieter-Daten von Plattformen soziale Medien, instant messaging-Plattformen und Collaboration-Plattformen Dokument auf Postfächer in Office 365-Organisation. Die folgenden: Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können</span><span class="sxs-lookup"><span data-stu-id="6cf82-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="6cf82-108">**Social** - Twitter, Facebook, LinkedIn und Yammer</span><span class="sxs-lookup"><span data-stu-id="6cf82-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="6cf82-109">**Instant messaging** - Yahoo Messenger, GoogleTalk und Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="6cf82-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="6cf82-110">**Zusammenarbeit an Dokumenten** - Feld und Ablage</span><span class="sxs-lookup"><span data-stu-id="6cf82-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="6cf82-111">**Vertikale Branchen** - Customer Relationship Management (beispielsweise Vertriebs Anwendungsstörgeräusche) und Finanzen (wie Thomson Reuters und Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="6cf82-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="6cf82-112">**SMS-Text messaging** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6cf82-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="6cf82-p103">Nach dem Import Drittanbieter-Daten können Sie Office 365 Compliance-Features anwenden – beispielsweise Aufbewahrung für eventuelle Rechtsstreitigkeiten, Inhaltssuche, Compliance-Archivierung, Überwachung und Office 365 Aufbewahrungsrichtlinien – auf diese Daten. Wenn ein Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird, werden angenommen, Drittanbieter-Daten beibehalten. Sie können Drittanbieter-Daten mithilfe von Inhaltssuche suchen. Oder Sie können anwenden, Archivierung und Aufbewahrungsrichtlinien auf Drittanbieter-Daten wie für Microsoft Data. Kurz gesagt, helfen Archivierung von Drittanbieter-Daten in Office 365 Ihrer Organisation, die Einhaltung der behördlichen und behördlichen Richtlinien bleiben.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="6cf82-118">Hier ist eine Übersicht über den Prozess und die Schritte zum Importieren von Drittanbieter-Daten zu Office 365 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6cf82-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="6cf82-119">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="6cf82-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="6cf82-120">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6cf82-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="6cf82-121">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6cf82-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="6cf82-122">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="6cf82-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="6cf82-123">Schritt 5: Registrieren Sie den Connector Drittanbieter-Daten in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6cf82-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="6cf82-124">Funktioniert wie die Daten von Drittanbieter-Prozess Importieren ></span><span class="sxs-lookup"><span data-stu-id="6cf82-124">How the third-party data import process works></span></span>

<span data-ttu-id="6cf82-125">Die folgende Abbildung und die Beschreibung erläutern, wie der Prozess zum Importieren von Drittanbieterdaten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6cf82-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="6cf82-127">Kunden arbeitet mit Partner Wahl eine Verbindung konfigurieren, die Elemente aus der Drittanbieter-Datenquelle extrahiert und dann diese Elemente zu Office 365 importieren.</span><span class="sxs-lookup"><span data-stu-id="6cf82-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="6cf82-p104">Der Partner-Connector Drittanbieter-Datenquellen über einen Drittanbieter-API (auf Basis geplant oder als konfiguriert) her und extrahiert Elemente aus der Datenquelle. Der Partner Connector konvertiert den Inhalt eines Elements in einer e-Mail-Format. Finden Sie [Weitere Informationen](#more-information) im Abschnitt für eine Beschreibung des Message-Format-Schemas.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="6cf82-131">Partner-Connector stellt eine Verbindung mit dem Azure-Dienst in Office 365 mithilfe von Dienst (Exchange Web Services, EWS) über eine bekannte Endpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="6cf82-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="6cf82-p105">Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="6cf82-p106">a **Elemente verfügen, die eine Benutzer-ID, die ein Benutzerkonto für Office 365 entspricht** -Wenn Sie der Connector Partner die Benutzer-ID des Elements in der Drittanbieter-Datenquelle für einen bestimmten Benutzer zugeordnet werden kann, die in den Ordner **Löscht ein** , in des Benutzers-ID in Office 365, das Element kopiert werden. Ordner "wiederherstellbare Elemente". Benutzer können keine Elemente im Ordner Benutzerkontenverwaltung zugreifen. EDiscovery-Tools für Office 365 können Sie jedoch um für Elemente im Ordner Benutzerkontenverwaltung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="6cf82-p107">b. **Elemente, die eine Benutzer-ID besitzen, die ein Office 365-Benutzerkonto entspricht** – Falls der Partner-Connector die Benutzer-ID eines Elements zu einem bestimmten Benutzer zuordnen kann nicht-ID in Office 365, das Element in den Ordner **Posteingang** des Postfachs Drittanbieter-Daten kopiert werden. Importieren von Elementen in den Posteingang können Sie oder eine Person in Ihrer Organisation So melden Sie sich an das Postfach von Drittanbietern zum Anzeigen und Verwalten von dieser Elemente sowie überprüfen, ob alle Korrekturen in der Connectorkonfiguration Partner getroffen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="6cf82-141">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="6cf82-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="6cf82-p108">Eine wichtige Komponente für die Archivierung von Drittanbieter-Daten in Office 365 ist Suchen von und Arbeiten mit einem Microsoft-Partner, die sich auf in Sammeln von Daten aus einer Drittanbieter-Datenquelle und importieren es in Office 365. Nachdem die Daten importiert werden, es kann archiviert und beibehalten zusammen mit Ihrer Organisation des anderen Microsoft-Daten, wie beispielsweise e-Mail-Nachrichten von Exchange und Dokumente aus SharePoint und OneDrive für Unternehmen. Ein Partner erstellt einen Connector, der Daten aus Ihrer Organisation Drittanbieter-Datenquellen (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) extrahiert und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächern als importiert e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="6cf82-145">In den folgenden Abschnitten aufgelistet, die Microsoft-Partner – und Drittanbieter-Datenquellen, die sie unterstützen –, die die Anwendung für die Archivierung von Drittanbieter-Daten in Office 365 beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="6cf82-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="6cf82-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="6cf82-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="6cf82-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="6cf82-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="6cf82-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="6cf82-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="6cf82-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="6cf82-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="6cf82-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="6cf82-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="6cf82-151">Verba</span><span class="sxs-lookup"><span data-stu-id="6cf82-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="6cf82-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="6cf82-152">17a-4 LLC</span></span>

<span data-ttu-id="6cf82-153">17a-4 LLC unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="6cf82-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6cf82-154">BlackBerry</span></span>
    
- <span data-ttu-id="6cf82-155">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="6cf82-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="6cf82-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="6cf82-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="6cf82-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="6cf82-157">FactSet</span></span>
    
- <span data-ttu-id="6cf82-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="6cf82-158">HipChat</span></span>
    
- <span data-ttu-id="6cf82-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="6cf82-159">InvestEdge</span></span>
    
- <span data-ttu-id="6cf82-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="6cf82-160">LivePerson</span></span>
    
- <span data-ttu-id="6cf82-161">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="6cf82-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="6cf82-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="6cf82-162">OpenText</span></span>
    
- <span data-ttu-id="6cf82-163">Live-Hilfe für Oracle/ATG 'click-to-call'
</span><span class="sxs-lookup"><span data-stu-id="6cf82-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="6cf82-164">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="6cf82-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="6cf82-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="6cf82-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="6cf82-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="6cf82-166">MindAlign</span></span>
    
- <span data-ttu-id="6cf82-167">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="6cf82-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="6cf82-168">
Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="6cf82-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="6cf82-169">
Skype for Business Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="6cf82-170">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="6cf82-170">SQL Databases</span></span>
    
- <span data-ttu-id="6cf82-171">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="6cf82-171">Squawker</span></span>
    
- <span data-ttu-id="6cf82-172">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="6cf82-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="6cf82-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="6cf82-173">Actiance</span></span>

<span data-ttu-id="6cf82-174">[Actiance](https://www.actiance.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6cf82-175">AIM</span><span class="sxs-lookup"><span data-stu-id="6cf82-175">AIM</span></span>
    
- <span data-ttu-id="6cf82-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="6cf82-176">American Idol</span></span>
    
- <span data-ttu-id="6cf82-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="6cf82-177">Apple Juice</span></span>
    
- <span data-ttu-id="6cf82-178">
AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="6cf82-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="6cf82-179">Ares</span><span class="sxs-lookup"><span data-stu-id="6cf82-179">Ares</span></span>
    
- <span data-ttu-id="6cf82-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="6cf82-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="6cf82-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="6cf82-181">Bear Share</span></span>
    
- <span data-ttu-id="6cf82-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="6cf82-182">Bit Torrent</span></span>
    
- <span data-ttu-id="6cf82-183">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-184">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-185">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-186">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-187">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="6cf82-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="6cf82-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="6cf82-188">CellTrust</span></span>
    
- <span data-ttu-id="6cf82-189">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="6cf82-189">Chat Import</span></span>
    
- <span data-ttu-id="6cf82-190">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="6cf82-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="6cf82-191">Chatter
</span><span class="sxs-lookup"><span data-stu-id="6cf82-191">Chatter</span></span>
    
- <span data-ttu-id="6cf82-192">Cisco Sofortnachrichten &amp; Anwesenheitsserver (v9.0.1, 9.1, v9.1.1 SU1, v10 v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="6cf82-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="6cf82-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="6cf82-194">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="6cf82-194">Collaboration Import</span></span>
    
- <span data-ttu-id="6cf82-195">Echtzeitprotokollierung für Zusammenarbeit
</span><span class="sxs-lookup"><span data-stu-id="6cf82-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="6cf82-196">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="6cf82-196">Direct Connect</span></span>
    
- <span data-ttu-id="6cf82-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="6cf82-197">Facebook</span></span>
    
- <span data-ttu-id="6cf82-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="6cf82-198">FactSet</span></span>
    
- <span data-ttu-id="6cf82-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="6cf82-199">FastTrack</span></span>
    
- <span data-ttu-id="6cf82-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="6cf82-200">Gnutella</span></span>
    
- <span data-ttu-id="6cf82-201">Google+
</span><span class="sxs-lookup"><span data-stu-id="6cf82-201">Google+</span></span>
    
- <span data-ttu-id="6cf82-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="6cf82-202">GoToMyPC</span></span>
    
- <span data-ttu-id="6cf82-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="6cf82-203">Hopster</span></span>
    
- <span data-ttu-id="6cf82-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="6cf82-204">HubConnex</span></span>
    
- <span data-ttu-id="6cf82-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="6cf82-206">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="6cf82-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="6cf82-207">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="6cf82-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="6cf82-208">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="6cf82-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="6cf82-209">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="6cf82-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="6cf82-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="6cf82-211">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="6cf82-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="6cf82-212">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="6cf82-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="6cf82-213">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="6cf82-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="6cf82-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="6cf82-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="6cf82-215">Chat-Import
</span><span class="sxs-lookup"><span data-stu-id="6cf82-215">IM Import</span></span>
    
- <span data-ttu-id="6cf82-216">Echtzeitprotokollierung und -richtinie für Chat
</span><span class="sxs-lookup"><span data-stu-id="6cf82-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="6cf82-217">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="6cf82-217">Indii Messenger</span></span>
    
- <span data-ttu-id="6cf82-218">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="6cf82-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="6cf82-219">IRC</span><span class="sxs-lookup"><span data-stu-id="6cf82-219">IRC</span></span>
    
- <span data-ttu-id="6cf82-220">Jive
</span><span class="sxs-lookup"><span data-stu-id="6cf82-220">Jive</span></span>
    
- <span data-ttu-id="6cf82-221">Jive 6 Real Time Logging (v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="6cf82-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="6cf82-222">Jive Import</span></span>
    
- <span data-ttu-id="6cf82-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="6cf82-223">JXTA</span></span>
    
- <span data-ttu-id="6cf82-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6cf82-224">LinkedIn</span></span>
    
- <span data-ttu-id="6cf82-225">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="6cf82-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="6cf82-226">MFTP</span></span>
    
- <span data-ttu-id="6cf82-227">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="6cf82-228">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="6cf82-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6cf82-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="6cf82-230">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="6cf82-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="6cf82-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="6cf82-231">MindAlign</span></span>
    
- <span data-ttu-id="6cf82-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="6cf82-232">Mobile Guard</span></span>
    
- <span data-ttu-id="6cf82-233">MSN</span><span class="sxs-lookup"><span data-stu-id="6cf82-233">MSN</span></span>
    
- <span data-ttu-id="6cf82-234">My Space</span><span class="sxs-lookup"><span data-stu-id="6cf82-234">My Space</span></span>
    
- <span data-ttu-id="6cf82-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="6cf82-235">NEONetwork</span></span>
    
- <span data-ttu-id="6cf82-236">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="6cf82-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="6cf82-237">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="6cf82-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="6cf82-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="6cf82-238">Pinterest</span></span>
    
- <span data-ttu-id="6cf82-239">Pivot</span><span class="sxs-lookup"><span data-stu-id="6cf82-239">Pivot</span></span>
    
- <span data-ttu-id="6cf82-240">QQ</span><span class="sxs-lookup"><span data-stu-id="6cf82-240">QQ</span></span>
    
- <span data-ttu-id="6cf82-241">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="6cf82-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="6cf82-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="6cf82-242">SoftEther</span></span>
    
- <span data-ttu-id="6cf82-243">Symphony
</span><span class="sxs-lookup"><span data-stu-id="6cf82-243">Symphony</span></span>
    
- <span data-ttu-id="6cf82-244">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="6cf82-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="6cf82-245">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="6cf82-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="6cf82-246">Tor</span><span class="sxs-lookup"><span data-stu-id="6cf82-246">Tor</span></span>
    
- <span data-ttu-id="6cf82-247">TTT</span><span class="sxs-lookup"><span data-stu-id="6cf82-247">TTT</span></span>
    
- <span data-ttu-id="6cf82-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="6cf82-248">Twitter</span></span>
    
- <span data-ttu-id="6cf82-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="6cf82-249">WinMX</span></span>
    
- <span data-ttu-id="6cf82-250">Winny</span><span class="sxs-lookup"><span data-stu-id="6cf82-250">Winny</span></span>
    
- <span data-ttu-id="6cf82-251">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="6cf82-251">Yahoo</span></span>
    
- <span data-ttu-id="6cf82-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="6cf82-252">Yammer</span></span>
    
- <span data-ttu-id="6cf82-253">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="6cf82-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="6cf82-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="6cf82-254">ArchiveSocial</span></span>

<span data-ttu-id="6cf82-255">[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6cf82-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="6cf82-256">Facebook</span></span>
    
- <span data-ttu-id="6cf82-257">Flickr
</span><span class="sxs-lookup"><span data-stu-id="6cf82-257">Flickr</span></span>
    
- <span data-ttu-id="6cf82-258">Instagram
</span><span class="sxs-lookup"><span data-stu-id="6cf82-258">Instagram</span></span>
    
- <span data-ttu-id="6cf82-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6cf82-259">LinkedIn</span></span>
    
- <span data-ttu-id="6cf82-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="6cf82-260">Pinterest</span></span>
    
- <span data-ttu-id="6cf82-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="6cf82-261">Twitter</span></span>
    
- <span data-ttu-id="6cf82-262">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="6cf82-262">YouTube</span></span>
    
- <span data-ttu-id="6cf82-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="6cf82-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="6cf82-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="6cf82-264">Globanet</span></span>

<span data-ttu-id="6cf82-265">[Globanet](https://www.globanet.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6cf82-266">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="6cf82-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="6cf82-267">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-268">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-269">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-270">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6cf82-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6cf82-271">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="6cf82-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="6cf82-272">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="6cf82-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="6cf82-273">Box
</span><span class="sxs-lookup"><span data-stu-id="6cf82-273">Box</span></span>
    
- <span data-ttu-id="6cf82-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6cf82-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="6cf82-275">Cisco Sofortnachrichten &amp; Anwesenheitsserver (V11. v10 v10.5.1 SU1, 0, "v11.5 SU2")</span><span class="sxs-lookup"><span data-stu-id="6cf82-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="6cf82-276">Cisco Webex Teams</span><span class="sxs-lookup"><span data-stu-id="6cf82-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="6cf82-277">Citrix Workspace &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="6cf82-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="6cf82-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="6cf82-278">CrowdCompass</span></span>

- <span data-ttu-id="6cf82-279">Durch Trennzeichen getrennte, benutzerdefinierte Textdateien
</span><span class="sxs-lookup"><span data-stu-id="6cf82-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="6cf82-280">Benutzerdefinierte XML-Dateien
</span><span class="sxs-lookup"><span data-stu-id="6cf82-280">Custom XML files</span></span>
    
- <span data-ttu-id="6cf82-281">Facebook (Seiten)</span><span class="sxs-lookup"><span data-stu-id="6cf82-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="6cf82-282">Factset
</span><span class="sxs-lookup"><span data-stu-id="6cf82-282">Factset</span></span>
    
- <span data-ttu-id="6cf82-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="6cf82-283">FXConnect</span></span>
    
- <span data-ttu-id="6cf82-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="6cf82-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="6cf82-285">Jive
</span><span class="sxs-lookup"><span data-stu-id="6cf82-285">Jive</span></span>
    
- <span data-ttu-id="6cf82-286">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="6cf82-286">Macgregor XIP</span></span>

- <span data-ttu-id="6cf82-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="6cf82-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="6cf82-288">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="6cf82-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="6cf82-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6cf82-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="6cf82-290">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="6cf82-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="6cf82-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="6cf82-291">Mobile Guard</span></span>
    
- <span data-ttu-id="6cf82-292">Pivot</span><span class="sxs-lookup"><span data-stu-id="6cf82-292">Pivot</span></span>
    
- <span data-ttu-id="6cf82-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6cf82-293">Salesforce Chatter</span></span>

- <span data-ttu-id="6cf82-294">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="6cf82-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="6cf82-295">Skype for Business, Versionen 2007 R2 - 2016 (lokal)
</span><span class="sxs-lookup"><span data-stu-id="6cf82-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="6cf82-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="6cf82-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="6cf82-297">Symphony
</span><span class="sxs-lookup"><span data-stu-id="6cf82-297">Symphony</span></span>
    
- <span data-ttu-id="6cf82-298">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="6cf82-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="6cf82-299">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="6cf82-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="6cf82-300">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="6cf82-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="6cf82-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="6cf82-301">Twitter</span></span>
    
- <span data-ttu-id="6cf82-302">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="6cf82-302">UBS Chat</span></span>
    
- <span data-ttu-id="6cf82-303">YouTube (engl.)</span><span class="sxs-lookup"><span data-stu-id="6cf82-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="6cf82-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="6cf82-304">OpenText</span></span>

<span data-ttu-id="6cf82-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6cf82-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="6cf82-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="6cf82-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="6cf82-307">Axs Exchange</span></span>
    
- <span data-ttu-id="6cf82-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="6cf82-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="6cf82-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="6cf82-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="6cf82-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="6cf82-310">Axs Signed</span></span>
    
- <span data-ttu-id="6cf82-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="6cf82-311">Bloomberg</span></span>
    
- <span data-ttu-id="6cf82-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="6cf82-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="6cf82-313">Verba</span><span class="sxs-lookup"><span data-stu-id="6cf82-313">Verba</span></span>

<span data-ttu-id="6cf82-314">[Verba](https://www.verba.com) unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6cf82-315">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="6cf82-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="6cf82-316">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="6cf82-317">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="6cf82-317">Avtec Radio</span></span>
    
- <span data-ttu-id="6cf82-318">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="6cf82-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="6cf82-319">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="6cf82-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="6cf82-320">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="6cf82-321">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-321">Centile Voice</span></span>
    
- <span data-ttu-id="6cf82-322">Chatnachricht in Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="6cf82-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="6cf82-323">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="6cf82-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="6cf82-324">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="6cf82-325">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="6cf82-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="6cf82-326">Cisco UCCX/UCCE VoIP</span><span class="sxs-lookup"><span data-stu-id="6cf82-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="6cf82-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="6cf82-327">ESChat Radio</span></span>
    
- <span data-ttu-id="6cf82-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="6cf82-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="6cf82-329">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="6cf82-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="6cf82-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="6cf82-331">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="6cf82-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="6cf82-332">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="6cf82-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="6cf82-333">Oracle/Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="6cf82-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="6cf82-334">Oracle/Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="6cf82-335">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="6cf82-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="6cf82-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="6cf82-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="6cf82-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="6cf82-338">Chatnachricht in Skype for Business/Lync
</span><span class="sxs-lookup"><span data-stu-id="6cf82-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="6cf82-339">Skype for Business/Lync Video
</span><span class="sxs-lookup"><span data-stu-id="6cf82-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="6cf82-340">Skype for Business/Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="6cf82-341">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="6cf82-342">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="6cf82-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="6cf82-343">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="6cf82-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="6cf82-344">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="6cf82-344">Truphone Voice</span></span>
    
- <span data-ttu-id="6cf82-345">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="6cf82-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="6cf82-346">Windows Desktop-Computerbildschirm 
</span><span class="sxs-lookup"><span data-stu-id="6cf82-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="6cf82-347">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6cf82-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="6cf82-p109">Hier sind die Schritte zum Erstellen und Konfigurieren eines Postfachs Drittanbieter-Daten für das Importieren von Daten in Office 365. Wie vorherige erläutert, Elemente auf dieses Postfach importiert werden, wenn der Partner-Connector die Benutzer-ID des Elements ein Benutzerkonto für Office 365 zugeordnet ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="6cf82-350">**Führen Sie diese Aufgaben in Office 365 Administrationscenter**</span><span class="sxs-lookup"><span data-stu-id="6cf82-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="6cf82-p110">Erstellen eines neuen Benutzerkontos in Office 365, und weisen Sie es mit einer Lizenzvertrags für Exchange Online – Plan 2; finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). So platzieren das Postfach in die Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Aktivieren eines archivpostfachs, das eine unbegrenzte Speicherkontingent hat, ist eine Plan 2-Lizenz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="6cf82-353">Fügen Sie das Benutzerkonto für das Postfach von Drittanbieter-Daten für die **Exchange-Administrator** -Admin-Rolle in Office 365; finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="6cf82-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="6cf82-p111">Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto. Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="6cf82-356">**Führen Sie diese Aufgaben in der Exchange-Verwaltungskonsole**</span><span class="sxs-lookup"><span data-stu-id="6cf82-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="6cf82-p112">Ausblenden des Postfachs Drittanbieter-Daten aus dem Adressbuch und andere Adresslisten in Ihrer Organisation; finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternativ können Sie den folgenden PowerShell-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="6cf82-359">Weisen Sie die Berechtigung **FullAccess** das Postfach von Drittanbieter-Daten, damit Administratoren oder Compliance Officer das Postfach von Drittanbietern Daten im Outlook-Desktopclient geöffnet werden können; finden Sie unter [Verwalten von Berechtigungen für Empfänger](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="6cf82-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="6cf82-360">Aktivieren Sie die folgenden Compliance-bezogene Office 365-Features für das Postfach von Drittanbieter-Daten:</span><span class="sxs-lookup"><span data-stu-id="6cf82-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="6cf82-p113">Aktivieren Sie das Archivpostfach; finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md). Auf diese Weise können Sie frei bis Speicherplatz in das primäre Postfach durch Einrichten einer Archivrichtlinie, die Elemente von Drittanbieter-Daten in das Archivpostfach verschoben. Dies stellt Sie unbegrenzte Speicher für Drittanbieter-Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="6cf82-p114">Platzieren Sie das Postfach von Drittanbieter-Daten in die Aufbewahrung für eventuelle Rechtsstreitigkeiten. Sie können auch anwenden eine Aufbewahrungsrichtlinie Office 365 in die Office 365-Sicherheit &amp; Compliance Center. Platzieren dieses Postfach in der Warteschleife wird aufbewahren von von Drittanbieter-Datenelementen (auf unbestimmte Zeit oder für eine angegebene Dauer) und zu verhindern, aus dem Postfach gelöscht werden. Finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="6cf82-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="6cf82-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="6cf82-369">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="6cf82-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="6cf82-p115">Aktivieren Sie die postfachüberwachungsprotokollierung für den Besitzer, Delegaten und Admin-Zugriff auf das Postfach von Drittanbietern Daten; finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](enable-mailbox-auditing.md). Dadurch können Sie alle Aktivitäten, die von jedem Benutzer mit Zugriff auf das Postfach von Drittanbietern Daten überwachen.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="6cf82-372">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6cf82-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="6cf82-p116">Der nächste Schritt besteht darin Benutzerpostfächer zur Unterstützung von Drittanbieter-Daten konfigurieren. Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="6cf82-375">Aktivieren Sie das Archivpostfach für jeden Benutzer. finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="6cf82-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="6cf82-376">Platzieren von Benutzerpostfächern in Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Anwenden einer Aufbewahrungsrichtlinie für Office 365. finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="6cf82-377">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="6cf82-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="6cf82-378">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="6cf82-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="6cf82-379">Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cf82-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="6cf82-380">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="6cf82-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="6cf82-381">Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren.</span><span class="sxs-lookup"><span data-stu-id="6cf82-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="6cf82-382">Der Endpunkt für die Verbindung mit dem Azure-Dienst in Office 365 verwendet:</span><span class="sxs-lookup"><span data-stu-id="6cf82-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="6cf82-p117">Die Anmeldung Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) für das Postfach von Drittanbieter-Daten, das Sie in Schritt2 erstellt haben. Diese Anmeldeinformationen sind erforderlich, damit der Partner-Connector zugreifen und Elemente für Benutzerpostfächer und an das Postfach von Drittanbietern Daten importieren kann.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="6cf82-385">Schritt 5: Registrieren Sie den Connector Drittanbieter-Daten in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6cf82-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="6cf82-p118">30 September 2018 starten, beginnt der Azure-Dienst in Office 365 verwenden moderne Authentifizierung in Exchange Online zum Authentifizieren von Drittanbieter-datenkonnektoren, die versuchen, eine Verbindung mit Office 365-Organisation zum Importieren der Daten. Der Grund für diese Änderung ist die moderne Authentifizierung sicherer als die aktuelle-Methode enthält, die mithilfe von Drittanbietern Connectors basiert, die mit den zuvor beschriebenen Endpunkt mit dem Azure-Dienst hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="6cf82-p119">Um einen Drittanbieter-Daten Connector Verbindung mit Office 365 mit der neuen modernen Authentifizierungsmethode zu aktivieren, muss ein Administrator in Office 365-Organisation Ihr Einverständnis der Connector als vertrauenswürdigen Dienst-Anwendung in Azure Active Directory registrieren. Dies erfolgt eine Anforderung Berechtigungen, um den Connector Zugriff auf Daten in Azure Active Directory Ihrer Organisation zu ermöglichen und zu übernehmen. Nachdem Sie diese Einladung annehmen, ist der Connector Drittanbieter-Daten als eine Enterprise-Anwendung mit Azure Active Directory hinzugefügt und als einen Dienstprinzipal dargestellt. Weitere Informationen zu den Prozess Zustimmung finden Sie unter [Mandanten Admin stimmen](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="6cf82-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="6cf82-392">Hier sind die Schritte zum zugreifen, und akzeptieren Sie die Anforderung an den Connector registrieren:</span><span class="sxs-lookup"><span data-stu-id="6cf82-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="6cf82-393">Besuchen Sie [Diese Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) , und melden Sie sich mit den Anmeldeinformationen des ein globaler Office 365-Administrator.</span><span class="sxs-lookup"><span data-stu-id="6cf82-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="6cf82-p120">Das folgende Dialogfeld wird angezeigt. Erweitern Sie die Caretzeichen zur Überprüfung der Berechtigungen, die an den Konnektor zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="6cf82-396">![Das Anforderung Berechtigungsdialogfeld wird angezeigt.](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="6cf82-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="6cf82-397">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="6cf82-397">Click **Accept**.</span></span>

<span data-ttu-id="6cf82-p121">Nachdem Sie die Anfrage zu akzeptieren, wird der [Azure-Portal](https://portal.azure.com) angezeigt. Klicken Sie zum Anzeigen der Liste der Programme für Ihre Organisation **Azure Active Directory** > **unternehmensanwendungen**. Der Office 365-Drittanbieter-Daten-Connector wird auf das Blade **unternehmensanwendungen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cf82-p122">Nach 30 September 2018 werden der Drittanbieter-Daten nicht mehr in Postfächer in Ihrer Organisation importiert werden, wenn Sie einen Connector Drittanbieter-Daten in Azure Active Directory registrieren nicht. Das Verfahren in Schritt 5 muss einer vorhandenen Drittanbieter-datenkonnektoren (die vor dem 30 September 2018 erstellt) Hinweis auch in Azure Active Directory registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="6cf82-403">Das Aufheben von Zustimmung für einen Connector Drittanbieter-Daten</span><span class="sxs-lookup"><span data-stu-id="6cf82-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="6cf82-p123">Nach Ihrer Organisation auf die Anforderung Berechtigungen zum Registrieren eines Drittanbieter-Daten-Connectors in Azure Active Directory zustimmt, kann Ihre Organisation dieses Consent jederzeit widerrufen. Das Aufheben der Zustimmung für einen Connector wird jedoch bedeuten, dass Daten aus der Drittanbieter-Datenquelle nicht mehr in Office 365 importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="6cf82-p124">Um Zustimmung für einen Connector Drittanbieter-Daten entziehen möchten, können Sie die Anwendung zu löschen (durch den entsprechenden Dienstprinzipal löschen) von Azure Active Directory mit dem **unternehmensanwendungen** Blade im Azure-Portal oder mithilfe der [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Sie können auch das Cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) in Azure Active Directory PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="6cf82-408">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6cf82-408">More information</span></span>

- <span data-ttu-id="6cf82-p125">Wie vorherige erläutert, Elemente von Drittanbieter-Daten, die in Exchange-Postfächern als e-Mail-Nachrichten Quellen importiert werden. Der Partner-Connector importiert das Element mit einem Schema, das von der Office 365-API erforderlich. In der folgenden Tabelle werden die Eigenschaften eines Elements aus einer Drittanbieter-Datenquelle beschrieben, nach dem Import auf einem Exchange-Postfach als e-Mail-Nachricht ist. Die Tabelle zeigt auch an, ob die Message-Eigenschaft zwingend erforderlich ist. Erforderliche Eigenschaften müssen aufgefüllt werden. Wenn ein Element eine erforderliche Eigenschaft nicht angezeigt wird, werden nicht es zu Office 365 importiert werden. Der Importvorgang wird eine Fehlermeldung angezeigt, die erklärt, warum ein Element wurde nicht importiert und welche Eigenschaft fehlt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="6cf82-416">**Nachrichteneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="6cf82-416">**Message property**</span></span>|<span data-ttu-id="6cf82-417">**Zwingend erforderlich?**</span><span class="sxs-lookup"><span data-stu-id="6cf82-417">**Mandatory?**</span></span>|<span data-ttu-id="6cf82-418">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6cf82-418">**Description**</span></span>|<span data-ttu-id="6cf82-419">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="6cf82-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6cf82-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="6cf82-420">**FROM**</span></span> <br/> |<span data-ttu-id="6cf82-421">Ja</span><span class="sxs-lookup"><span data-stu-id="6cf82-421">Yes</span></span>  <br/> |<span data-ttu-id="6cf82-p126">Der Benutzer, die ursprünglich erstellt oder das Element in der Drittanbieter-Datenquelle gesendet. Der Partner-Verbindung versucht, die Benutzer-ID aus dem Quellelement (beispielsweise ein Handle Twitter) ein Benutzerkonto für Office 365 für alle Teilnehmer (Benutzer in die Felder FROM und TO) zuordnen. Eine Kopie der Nachricht wird an das Postfach von jedem Teilnehmer importiert werden. Wenn keines der Teilnehmer aus dem Element zu einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element auf das Postfach der Drittanbieter-Archivierung in Office 365 importiert werden.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="6cf82-p127">Der Teilnehmer, der als Absender des Elements identifiziert wird benötigen kein active-Postfach in der Office 365-Organisation, die auf das Element importiert wird. Wenn der Absender eine aktive Postfach besitzt, wird die folgende Fehlermeldung zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="6cf82-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="6cf82-428">**TO**</span></span> <br/> |<span data-ttu-id="6cf82-429">Ja</span><span class="sxs-lookup"><span data-stu-id="6cf82-429">Yes</span></span>  <br/> |<span data-ttu-id="6cf82-430">Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).</span><span class="sxs-lookup"><span data-stu-id="6cf82-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="6cf82-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="6cf82-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="6cf82-432">Nein</span><span class="sxs-lookup"><span data-stu-id="6cf82-432">No</span></span>  <br/> |<span data-ttu-id="6cf82-433">Der Betreff des Quellelements.</span><span class="sxs-lookup"><span data-stu-id="6cf82-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="6cf82-434">**DATUM**</span><span class="sxs-lookup"><span data-stu-id="6cf82-434">**DATE**</span></span> <br/> |<span data-ttu-id="6cf82-435">Ja</span><span class="sxs-lookup"><span data-stu-id="6cf82-435">Yes</span></span>  <br/> |<span data-ttu-id="6cf82-436">Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.</span><span class="sxs-lookup"><span data-stu-id="6cf82-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="6cf82-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="6cf82-437">**BODY**</span></span> <br/> |<span data-ttu-id="6cf82-438">Nein</span><span class="sxs-lookup"><span data-stu-id="6cf82-438">No</span></span>  <br/> |<span data-ttu-id="6cf82-p128">Der Inhalt der Nachricht oder des Beitrags. Für einige Datenquellen können den Inhalt dieser Eigenschaft des Inhalts für die **SUBJECT** -Eigenschaft identisch sein. Während des Importvorgangs versucht der Partner Connector originalgetreue aus der Inhaltsquelle wie möglich beizubehalten. Wenn möglich ist in dieser Eigenschaft Dateien, Grafiken oder andere Inhalte aus dem Textkörper des Quellelements enthalten. Andernfalls ist in der **Anlage** -Eigenschaft Inhalte aus dem Quellelement enthalten. Der Inhalt dieser Eigenschaft werden für den Connector Partner und für die Funktionalität der Source-Plattform abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="6cf82-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="6cf82-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="6cf82-446">Nein</span><span class="sxs-lookup"><span data-stu-id="6cf82-446">No</span></span>  <br/> |<span data-ttu-id="6cf82-p129">Wenn ein Element in der Datenquelle (beispielsweise einen Tweet in Twitter oder einer Unterhaltung über Sofortnachrichten) hat eine angefügte Datei oder fügen Sie Bilder, Verbinden des Partners wird ersten Versuch zum Einschließen von Anlagen in die **BODY** -Eigenschaft. Wenn das ist nicht möglich, wird diese hinzugefügt der ** Anlage ** Eigenschaft. Weitere Beispiele für Anlagen sind "gefällt mir" in Facebook Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder ein Beitrag.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="6cf82-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="6cf82-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="6cf82-451">Ja</span><span class="sxs-lookup"><span data-stu-id="6cf82-451">Yes</span></span>  <br/> | <span data-ttu-id="6cf82-p130">Dies ist eine mehrwertige-Eigenschaft, die erstellt und durch Partner Connector aufgefüllt wird. Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`. (Diese Eigenschaft muss zunächst `IPM.NOTE`; dieses Format ist vergleichbar mit der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="6cf82-455">`Source`-Gibt die Drittanbieter-Datenquelle an. beispielsweise Twitter, Facebook oder BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="6cf82-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="6cf82-p131">`Event`-Gibt den Typ der Aktivität, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erzeugt an. beispielsweise einen Tweet in Twitter oder ein Beitrag in Facebook. Ereignisse sind für die Datenquelle spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="6cf82-p132">Ein Zweck von dieser Eigenschaft wird zum Filtern von bestimmter Elementen basierend auf die Datenquelle, an dem ein Element stammt oder basierend auf den Typ des Ereignisses. Beispielsweise können in einer eDiscovery-Suche Sie erstellen eine Suchabfrage aus, um alle Tweets zu suchen, die von einem bestimmten Benutzer veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="6cf82-p133">Wenn Elemente auf Postfächer in Office 365 erfolgreich importiert wurden, wird eine eindeutige ID wieder an den Aufrufer als Teil der HTTP-Antwort zurückgegeben. Dieser Bezeichner – aufgerufen `x-IngestionCorrelationID`– aus Gründen nachfolgende zur Problembehandlung von Partnern für eine End-to-End-Überwachung von Elementen verwendet werden kann. Es wird empfohlen, dass Partner diese Informationen erfassen und melden Sie es entsprechend geleitet. Es folgt ein Beispiel für eine HTTP-Antwort, die mit diesem Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6cf82-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="6cf82-p134">Sie können das Tool für die Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, um die Suche nach Elementen, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Um speziell für diese importierte Elemente zu suchen, können Sie die folgende Meldung-Wert-Paare im Schlüsselwort für ein Inhaltssuche verwenden. .</span><span class="sxs-lookup"><span data-stu-id="6cf82-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="6cf82-p135">**`kind:externaldata`**-Verwenden Sie diese Eigenschaft-Wert-Paar, um alle Arten von Drittanbietern suchen. Verwenden Sie beispielsweise, um die Suche nach Elementen, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in die Subject-Eigenschaft des importierten Elements enthalten die Stichwortabfrage `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="6cf82-p136">**`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses-Eigenschaft-Wert-Paar nur Suche eines Datentyps Drittanbieter-angeben. Um nur Facebook Daten zu suchen, die das Wort "Contoso" in die Subject-Eigenschaft enthält, verwenden Sie beispielsweise die Stichwortabfrage `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="6cf82-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="6cf82-471">Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` -Eigenschaft, finden Sie unter [Inhaltssuche verwenden, um Daten von Dritten zu suchen, die in Office 365 importiert wurde,](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="6cf82-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="6cf82-472">Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6cf82-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="6cf82-473">Content-Suche in Office 365</span><span class="sxs-lookup"><span data-stu-id="6cf82-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="6cf82-474">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="6cf82-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 

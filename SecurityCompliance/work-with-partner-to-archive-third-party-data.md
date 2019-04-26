---
title: Arbeiten mit einem Partner zum Archivieren von drittanbieterdaten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Ihre Organisation kann mit einem Microsoft-Partner zusammenarbeiten, um einen benutzerdefinierten Connector einzurichten, um drittanbieterdaten aus Datenquellen wie Salesforce Chatter, Yahoo Messenger oder jammern zu importieren. Auf diese Weise können Sie Daten von Drittanbieter-Datenquellen in Office 365 archivieren, damit Sie die Office 365-Compliance-Funktionen wie rechtliche Aufbewahrung, Inhaltssuche und Aufbewahrungsrichtlinien zum Verwalten der Steuerung der drittanbieterdaten Ihrer Organisation verwenden.
ms.openlocfilehash: dce015438c9764f66e98936df9454cba73fd8472
ms.sourcegitcommit: 63a10dc5ffa9d709fac437d3fc9e554b1bcd826f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2019
ms.locfileid: "33307953"
---
# <a name="work-with-a-partner-to-archive-third-party-data-in-office-365"></a><span data-ttu-id="315f1-104">Arbeiten mit einem Partner zum Archivieren von drittanbieterdaten in Office 365</span><span class="sxs-lookup"><span data-stu-id="315f1-104">Work with a partner to archive third-party data in Office 365</span></span>

<span data-ttu-id="315f1-105">Sie können mit einem Microsoft-Partner zusammenarbeiten, um Daten aus einer Drittanbieter-Datenquelle in Office 365 zu importieren und zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-105">You can work with a Microsoft Partner to import and archive data from a third-party data source to Office 365.</span></span> <span data-ttu-id="315f1-106">Ein Partner kann Ihnen einen benutzerdefinierten Connector bereitstellen, der so konfiguriert ist, dass Elemente aus der Drittanbieter-Datenquelle (regelmäßig) extrahiert werden und diese Elemente dann in Office 365 importiert werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-106">A partner can provide you with an custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items to Office 365.</span></span> <span data-ttu-id="315f1-107">Der Partner-Konnektor wandelt den Inhalt eines Elements aus der Datenquelle in ein e-Mail-Nachrichtenformat um und speichert dann die Elemente in Postfächern in Office 365.</span><span class="sxs-lookup"><span data-stu-id="315f1-107">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes in Office 365.</span></span> <span data-ttu-id="315f1-108">Nachdem drittanbieterdaten importiert wurden, können Sie die Office 365-Compliance-Funktionen wie das Aufheben von Rechtsstreitigkeiten, Inhaltssuche, in-situ-Archivierung,-Überwachung und Office 365-Aufbewahrungsrichtlinien auf diese Daten anwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-108">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data.</span></span>
  
<span data-ttu-id="315f1-109">Im folgenden finden Sie eine Übersicht über den Prozess und die erforderlichen Schritte für die Zusammenarbeit mit einem Microsoft-Partner zum Importieren von drittanbieterdaten in Office 365.</span><span class="sxs-lookup"><span data-stu-id="315f1-109">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data to Office 365.</span></span>

[<span data-ttu-id="315f1-110">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="315f1-110">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="315f1-111">Step 2: Create and configure a third-party data mailbox in Office 365</span><span class="sxs-lookup"><span data-stu-id="315f1-111">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="315f1-112">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="315f1-112">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="315f1-113">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="315f1-113">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="315f1-114">Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="315f1-114">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="315f1-115">So funktioniert der Prozess zum Importieren von Drittanbieterdaten</span><span class="sxs-lookup"><span data-stu-id="315f1-115">How the third-party data import process works</span></span>

<span data-ttu-id="315f1-116">In der folgenden Abbildung und Beschreibung wird erläutert, wie der Drittanbieter-Datenimport Prozess bei der Arbeit mit einem Partner funktioniert.</span><span class="sxs-lookup"><span data-stu-id="315f1-116">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="315f1-118">Der Kunde arbeitet mit seinem bevorzugten Partner zusammen, um einen Connector zu konfigurieren, der Elemente aus der Drittanbieter-Datenquelle extrahiert und diese Elemente dann in Office 365 importiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-118">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="315f1-119">Der Partner-Connector stellt über eine Drittanbieter-API (auf einer festgelegten oder konfigurierten Basis) eine Verbindung zu drittanbieterdaten Quellen her und extrahiert Elemente aus der Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="315f1-119">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="315f1-120">Der Partnerconnector konvertiert den Inhalt eines Elements in ein E-Mail-Format.</span><span class="sxs-lookup"><span data-stu-id="315f1-120">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="315f1-121">Im Abschnitt [More information](#more-information) finden Sie eine Beschreibung des Nachrichtenformatschemas.</span><span class="sxs-lookup"><span data-stu-id="315f1-121">See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="315f1-122">Der Partner-Connector stellt mithilfe des Exchange-webDiensts (EWS) über einen bekannten Endpunkt eine Verbindung mit dem Azure-Dienst in Office 365 her.</span><span class="sxs-lookup"><span data-stu-id="315f1-122">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="315f1-p104">Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:</span><span class="sxs-lookup"><span data-stu-id="315f1-p104">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="315f1-125">a.</span><span class="sxs-lookup"><span data-stu-id="315f1-125">a.</span></span> <span data-ttu-id="315f1-126">**Elemente mit einer Benutzer-ID, die einem office 365-Benutzerkonto entsprechen** – wenn der Partner-Konnektor die Benutzer-ID des Elements in der Drittanbieter-Datenquelle einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in \*\*\*\* den Ordner "purges" im REC des Benutzers kopiert. Ordner "überable Items".</span><span class="sxs-lookup"><span data-stu-id="315f1-126">**Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="315f1-127">Benutzer können nicht auf Elemente im Ordner „Endgültige Löschvorgänge“ zugreifen.</span><span class="sxs-lookup"><span data-stu-id="315f1-127">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="315f1-128">Sie können jedoch Office 365 eDiscovery-Tools verwenden, um im Ordner "Purges" nach Elementen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="315f1-128">However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="315f1-129">b.</span><span class="sxs-lookup"><span data-stu-id="315f1-129">b.</span></span> <span data-ttu-id="315f1-130">**Elemente, die nicht über eine Benutzer-ID verfügen, die einem office 365-Benutzerkonto entspricht** – wenn der Partner-Konnektor die Benutzer-ID eines Elements nicht einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in den Ordner " **Posteingang** " des Drittanbieter-Daten Postfachs kopiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-130">**Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="315f1-131">Das Importieren von Elementen in den Posteingang ermöglicht Ihnen oder einem anderen Benutzer in Ihrer Organisation, sich beim Drittanbieter-Postfach anzumelden und diese Elemente zu verwalten und zu sehen, ob Anpassungen an der Partnerconnectorkonfiguration vorgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="315f1-131">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="315f1-132">Schritt 1: Partner für Drittanbieterdaten suchen</span><span class="sxs-lookup"><span data-stu-id="315f1-132">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="315f1-133">Eine wichtige Komponente für die Archivierung von drittanbieterdaten in Office 365 ist die Suche und Zusammenarbeit mit einem Microsoft-Partner, der sich auf die Erfassung von Daten aus einer Drittanbieter-Datenquelle und deren Import in Office 365 spezialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="315f1-133">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365.</span></span> <span data-ttu-id="315f1-134">Nachdem die Daten importiert wurden, können Sie zusammen mit den anderen Microsoft-Daten Ihrer Organisation archiviert und aufbewahrt werden, wie beispielsweise e-Mails von Exchange und Dokumenten aus SharePoint und OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="315f1-134">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="315f1-135">Ein Partner erstellt einen Connector, der Daten aus drittanbieterdaten Quellen Ihrer Organisation extrahiert (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächer als e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="315f1-135">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="315f1-136">In den folgenden Abschnitten werden die Microsoft-Partner und die von Ihnen unterstützten Drittanbieter-Datenquellen aufgeführt, die am Programm zur Archivierung von drittanbieterdaten in Office 365 teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="315f1-136">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="315f1-137">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="315f1-137">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="315f1-138">Actiance</span><span class="sxs-lookup"><span data-stu-id="315f1-138">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="315f1-139">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="315f1-139">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="315f1-140">Globanet</span><span class="sxs-lookup"><span data-stu-id="315f1-140">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="315f1-141">OpenText</span><span class="sxs-lookup"><span data-stu-id="315f1-141">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="315f1-142">Verba</span><span class="sxs-lookup"><span data-stu-id="315f1-142">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="315f1-143">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="315f1-143">17a-4 LLC</span></span>

<span data-ttu-id="315f1-144">17a-4 LLC unterstützt die folgenden Drittanbieter-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-144">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="315f1-145">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="315f1-145">BlackBerry</span></span>
    
- <span data-ttu-id="315f1-146">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="315f1-146">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="315f1-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="315f1-147">Cisco Jabber</span></span>
    
- <span data-ttu-id="315f1-148">FactSet</span><span class="sxs-lookup"><span data-stu-id="315f1-148">FactSet</span></span>
    
- <span data-ttu-id="315f1-149">HipChat</span><span class="sxs-lookup"><span data-stu-id="315f1-149">HipChat</span></span>
    
- <span data-ttu-id="315f1-150">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="315f1-150">InvestEdge</span></span>
    
- <span data-ttu-id="315f1-151">Schwätzchen</span><span class="sxs-lookup"><span data-stu-id="315f1-151">LivePerson</span></span>
    
- <span data-ttu-id="315f1-152">MessageLabs Data Streams</span><span class="sxs-lookup"><span data-stu-id="315f1-152">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="315f1-153">OpenText</span><span class="sxs-lookup"><span data-stu-id="315f1-153">OpenText</span></span>
    
- <span data-ttu-id="315f1-154">Live-Hilfe für Oracle/ATG 'click-to-call'</span><span class="sxs-lookup"><span data-stu-id="315f1-154">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="315f1-155">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="315f1-155">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="315f1-156">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="315f1-156">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="315f1-157">MindAlign</span><span class="sxs-lookup"><span data-stu-id="315f1-157">MindAlign</span></span>
    
- <span data-ttu-id="315f1-158">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="315f1-158">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="315f1-159">Skype for Business (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="315f1-159">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="315f1-160">Skype for Business Online (Lync Online)</span><span class="sxs-lookup"><span data-stu-id="315f1-160">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="315f1-161">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="315f1-161">SQL Databases</span></span>
    
- <span data-ttu-id="315f1-162">Squawker</span><span class="sxs-lookup"><span data-stu-id="315f1-162">Squawker</span></span>
    
- <span data-ttu-id="315f1-163">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="315f1-163">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="315f1-164">Actiance</span><span class="sxs-lookup"><span data-stu-id="315f1-164">Actiance</span></span>

<span data-ttu-id="315f1-165">[Actiance](https://www.actiance.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-165">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="315f1-166">VERSUCHEN</span><span class="sxs-lookup"><span data-stu-id="315f1-166">AIM</span></span>
    
- <span data-ttu-id="315f1-167">American Idol</span><span class="sxs-lookup"><span data-stu-id="315f1-167">American Idol</span></span>
    
- <span data-ttu-id="315f1-168">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="315f1-168">Apple Juice</span></span>
    
- <span data-ttu-id="315f1-169">AOL mit Pivot-Client</span><span class="sxs-lookup"><span data-stu-id="315f1-169">AOL with Pivot client</span></span>
    
- <span data-ttu-id="315f1-170">Ares</span><span class="sxs-lookup"><span data-stu-id="315f1-170">Ares</span></span>
    
- <span data-ttu-id="315f1-171">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-171">Bazaar Voice</span></span>
    
- <span data-ttu-id="315f1-172">Bear Share</span><span class="sxs-lookup"><span data-stu-id="315f1-172">Bear Share</span></span>
    
- <span data-ttu-id="315f1-173">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="315f1-173">Bit Torrent</span></span>
    
- <span data-ttu-id="315f1-174">BlackBerry-Anrufprotokolle (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-174">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-175">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-175">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-176">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-176">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-177">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-177">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-178">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="315f1-178">Bloomberg Mail</span></span>
    
- <span data-ttu-id="315f1-179">CellTrust</span><span class="sxs-lookup"><span data-stu-id="315f1-179">CellTrust</span></span>
    
- <span data-ttu-id="315f1-180">Chat Import</span><span class="sxs-lookup"><span data-stu-id="315f1-180">Chat Import</span></span>
    
- <span data-ttu-id="315f1-181">Echtzeitprotokollierung und -richtinie für Chat</span><span class="sxs-lookup"><span data-stu-id="315f1-181">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="315f1-182">Geschwätz</span><span class="sxs-lookup"><span data-stu-id="315f1-182">Chatter</span></span>
    
- <span data-ttu-id="315f1-183">Cisco IM &amp; Presence Server (v 9.0.1, v 9.1, v 9.1.1 SU1, V10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="315f1-183">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="315f1-184">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="315f1-184">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="315f1-185">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="315f1-185">Collaboration Import</span></span>
    
- <span data-ttu-id="315f1-186">Echtzeitprotokollierung für Zusammenarbeit</span><span class="sxs-lookup"><span data-stu-id="315f1-186">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="315f1-187">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="315f1-187">Direct Connect</span></span>
    
- <span data-ttu-id="315f1-188">Facebook</span><span class="sxs-lookup"><span data-stu-id="315f1-188">Facebook</span></span>
    
- <span data-ttu-id="315f1-189">FactSet</span><span class="sxs-lookup"><span data-stu-id="315f1-189">FactSet</span></span>
    
- <span data-ttu-id="315f1-190">FastTrack</span><span class="sxs-lookup"><span data-stu-id="315f1-190">FastTrack</span></span>
    
- <span data-ttu-id="315f1-191">Gnutella</span><span class="sxs-lookup"><span data-stu-id="315f1-191">Gnutella</span></span>
    
- <span data-ttu-id="315f1-192">Google +</span><span class="sxs-lookup"><span data-stu-id="315f1-192">Google+</span></span>
    
- <span data-ttu-id="315f1-193">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="315f1-193">GoToMyPC</span></span>
    
- <span data-ttu-id="315f1-194">Hopster</span><span class="sxs-lookup"><span data-stu-id="315f1-194">Hopster</span></span>
    
- <span data-ttu-id="315f1-195">HubConnex</span><span class="sxs-lookup"><span data-stu-id="315f1-195">HubConnex</span></span>
    
- <span data-ttu-id="315f1-196">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span><span class="sxs-lookup"><span data-stu-id="315f1-196">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="315f1-197">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="315f1-197">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="315f1-198">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="315f1-198">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="315f1-199">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="315f1-199">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="315f1-200">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="315f1-200">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="315f1-201">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span><span class="sxs-lookup"><span data-stu-id="315f1-201">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="315f1-202">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="315f1-202">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="315f1-203">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="315f1-203">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="315f1-204">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="315f1-204">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="315f1-205">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="315f1-205">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="315f1-206">Chat-Import</span><span class="sxs-lookup"><span data-stu-id="315f1-206">IM Import</span></span>
    
- <span data-ttu-id="315f1-207">Echtzeitprotokollierung und -richtinie für Chat</span><span class="sxs-lookup"><span data-stu-id="315f1-207">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="315f1-208">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="315f1-208">Indii Messenger</span></span>
    
- <span data-ttu-id="315f1-209">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="315f1-209">Instant Bloomberg</span></span>
    
- <span data-ttu-id="315f1-210">IRC</span><span class="sxs-lookup"><span data-stu-id="315f1-210">IRC</span></span>
    
- <span data-ttu-id="315f1-211">Jive</span><span class="sxs-lookup"><span data-stu-id="315f1-211">Jive</span></span>
    
- <span data-ttu-id="315f1-212">Jive 6 Real Time Logging (v6, v7)</span><span class="sxs-lookup"><span data-stu-id="315f1-212">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="315f1-213">Jive Import</span><span class="sxs-lookup"><span data-stu-id="315f1-213">Jive Import</span></span>
    
- <span data-ttu-id="315f1-214">JXTA</span><span class="sxs-lookup"><span data-stu-id="315f1-214">JXTA</span></span>
    
- <span data-ttu-id="315f1-215">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="315f1-215">LinkedIn</span></span>
    
- <span data-ttu-id="315f1-216">Microsoft Lync (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="315f1-216">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="315f1-217">MFTP</span><span class="sxs-lookup"><span data-stu-id="315f1-217">MFTP</span></span>
    
- <span data-ttu-id="315f1-218">Microsoft Lync 2013 Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-218">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="315f1-219">Microsoft SharePoint (2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="315f1-219">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="315f1-220">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="315f1-220">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="315f1-221">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="315f1-221">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="315f1-222">MindAlign</span><span class="sxs-lookup"><span data-stu-id="315f1-222">MindAlign</span></span>
    
- <span data-ttu-id="315f1-223">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="315f1-223">Mobile Guard</span></span>
    
- <span data-ttu-id="315f1-224">MSN</span><span class="sxs-lookup"><span data-stu-id="315f1-224">MSN</span></span>
    
- <span data-ttu-id="315f1-225">My Space</span><span class="sxs-lookup"><span data-stu-id="315f1-225">My Space</span></span>
    
- <span data-ttu-id="315f1-226">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="315f1-226">NEONetwork</span></span>
    
- <span data-ttu-id="315f1-227">Office 365 Lync Dedicated</span><span class="sxs-lookup"><span data-stu-id="315f1-227">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="315f1-228">Office 365 Shared IM</span><span class="sxs-lookup"><span data-stu-id="315f1-228">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="315f1-229">Pinterest</span><span class="sxs-lookup"><span data-stu-id="315f1-229">Pinterest</span></span>
    
- <span data-ttu-id="315f1-230">Pivot</span><span class="sxs-lookup"><span data-stu-id="315f1-230">Pivot</span></span>
    
- <span data-ttu-id="315f1-231">QQ</span><span class="sxs-lookup"><span data-stu-id="315f1-231">QQ</span></span>
    
- <span data-ttu-id="315f1-232">Skype for Business 2015</span><span class="sxs-lookup"><span data-stu-id="315f1-232">Skype for Business 2015</span></span>
    
- <span data-ttu-id="315f1-233">SoftEther</span><span class="sxs-lookup"><span data-stu-id="315f1-233">SoftEther</span></span>
    
- <span data-ttu-id="315f1-234">Symphonie</span><span class="sxs-lookup"><span data-stu-id="315f1-234">Symphony</span></span>
    
- <span data-ttu-id="315f1-235">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="315f1-235">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="315f1-236">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="315f1-236">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="315f1-237">Tor</span><span class="sxs-lookup"><span data-stu-id="315f1-237">Tor</span></span>
    
- <span data-ttu-id="315f1-238">TTT</span><span class="sxs-lookup"><span data-stu-id="315f1-238">TTT</span></span>
    
- <span data-ttu-id="315f1-239">Twitter</span><span class="sxs-lookup"><span data-stu-id="315f1-239">Twitter</span></span>
    
- <span data-ttu-id="315f1-240">WinMX</span><span class="sxs-lookup"><span data-stu-id="315f1-240">WinMX</span></span>
    
- <span data-ttu-id="315f1-241">Winny</span><span class="sxs-lookup"><span data-stu-id="315f1-241">Winny</span></span>
    
- <span data-ttu-id="315f1-242">Yahoo</span><span class="sxs-lookup"><span data-stu-id="315f1-242">Yahoo</span></span>
    
- <span data-ttu-id="315f1-243">Yammer</span><span class="sxs-lookup"><span data-stu-id="315f1-243">Yammer</span></span>
    
- <span data-ttu-id="315f1-244">YouTube</span><span class="sxs-lookup"><span data-stu-id="315f1-244">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="315f1-245">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="315f1-245">ArchiveSocial</span></span>

<span data-ttu-id="315f1-246">[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-246">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="315f1-247">Facebook</span><span class="sxs-lookup"><span data-stu-id="315f1-247">Facebook</span></span>
    
- <span data-ttu-id="315f1-248">Flickr</span><span class="sxs-lookup"><span data-stu-id="315f1-248">Flickr</span></span>
    
- <span data-ttu-id="315f1-249">Instagram</span><span class="sxs-lookup"><span data-stu-id="315f1-249">Instagram</span></span>
    
- <span data-ttu-id="315f1-250">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="315f1-250">LinkedIn</span></span>
    
- <span data-ttu-id="315f1-251">Pinterest</span><span class="sxs-lookup"><span data-stu-id="315f1-251">Pinterest</span></span>
    
- <span data-ttu-id="315f1-252">Twitter</span><span class="sxs-lookup"><span data-stu-id="315f1-252">Twitter</span></span>
    
- <span data-ttu-id="315f1-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="315f1-253">YouTube</span></span>
    
- <span data-ttu-id="315f1-254">Vimeo</span><span class="sxs-lookup"><span data-stu-id="315f1-254">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="315f1-255">Globanet</span><span class="sxs-lookup"><span data-stu-id="315f1-255">Globanet</span></span>

<span data-ttu-id="315f1-256">[Globanet](https://www.globanet.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-256">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="315f1-257">AOL mit Pivot-Client
</span><span class="sxs-lookup"><span data-stu-id="315f1-257">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="315f1-258">BlackBerry-Anrufprotokolle (v5, v10, v12)
</span><span class="sxs-lookup"><span data-stu-id="315f1-258">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-259">BlackBerry Messenger (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-259">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-260">BlackBerry PIN (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-260">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-261">BlackBerry SMS (v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="315f1-261">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="315f1-262">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="315f1-262">Bloomberg Chat</span></span>
    
- <span data-ttu-id="315f1-263">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="315f1-263">Bloomberg Mail</span></span>
    
- <span data-ttu-id="315f1-264">Box</span><span class="sxs-lookup"><span data-stu-id="315f1-264">Box</span></span>
    
- <span data-ttu-id="315f1-265">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="315f1-265">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="315f1-266">Cisco IM &amp; Presence Server (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="315f1-266">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="315f1-267">Cisco WebEx-Teams</span><span class="sxs-lookup"><span data-stu-id="315f1-267">Cisco Webex Teams</span></span>

- <span data-ttu-id="315f1-268">Freigabe für &amp; Citrix Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="315f1-268">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="315f1-269">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="315f1-269">CrowdCompass</span></span>

- <span data-ttu-id="315f1-270">Durch Trennzeichen getrennte, benutzerdefinierte Textdateien</span><span class="sxs-lookup"><span data-stu-id="315f1-270">Custom delimited text files</span></span>
    
- <span data-ttu-id="315f1-271">Benutzerdefinierte XML-Dateien</span><span class="sxs-lookup"><span data-stu-id="315f1-271">Custom XML files</span></span>
    
- <span data-ttu-id="315f1-272">Facebook (Seiten)</span><span class="sxs-lookup"><span data-stu-id="315f1-272">Facebook (Pages)</span></span>
    
- <span data-ttu-id="315f1-273">FactSet</span><span class="sxs-lookup"><span data-stu-id="315f1-273">Factset</span></span>
    
- <span data-ttu-id="315f1-274">FXConnect</span><span class="sxs-lookup"><span data-stu-id="315f1-274">FXConnect</span></span>
    
- <span data-ttu-id="315f1-275">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="315f1-275">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="315f1-276">Jive</span><span class="sxs-lookup"><span data-stu-id="315f1-276">Jive</span></span>
    
- <span data-ttu-id="315f1-277">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="315f1-277">Macgregor XIP</span></span>

- <span data-ttu-id="315f1-278">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="315f1-278">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="315f1-279">Microsoft OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="315f1-279">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="315f1-280">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="315f1-280">Microsoft Teams</span></span>
       
- <span data-ttu-id="315f1-281">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="315f1-281">Microsoft Yammer</span></span>
    
- <span data-ttu-id="315f1-282">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="315f1-282">Mobile Guard</span></span>
    
- <span data-ttu-id="315f1-283">Pivot</span><span class="sxs-lookup"><span data-stu-id="315f1-283">Pivot</span></span>
    
- <span data-ttu-id="315f1-284">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="315f1-284">Salesforce Chatter</span></span>

- <span data-ttu-id="315f1-285">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="315f1-285">Skype for Business Online</span></span>
    
- <span data-ttu-id="315f1-286">Skype for Business, Versionen 2007 R2 - 2016 (lokal)</span><span class="sxs-lookup"><span data-stu-id="315f1-286">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="315f1-287">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="315f1-287">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="315f1-288">Symphonie</span><span class="sxs-lookup"><span data-stu-id="315f1-288">Symphony</span></span>
    
- <span data-ttu-id="315f1-289">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="315f1-289">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="315f1-290">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="315f1-290">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="315f1-291">Thomson Reuters Dealings 3000 / FX Trading</span><span class="sxs-lookup"><span data-stu-id="315f1-291">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="315f1-292">Twitter</span><span class="sxs-lookup"><span data-stu-id="315f1-292">Twitter</span></span>
    
- <span data-ttu-id="315f1-293">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="315f1-293">UBS Chat</span></span>
    
- <span data-ttu-id="315f1-294">YouTube</span><span class="sxs-lookup"><span data-stu-id="315f1-294">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="315f1-295">OpenText</span><span class="sxs-lookup"><span data-stu-id="315f1-295">OpenText</span></span>

<span data-ttu-id="315f1-296">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-296">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="315f1-297">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="315f1-297">Axs Encrypted</span></span>
    
- <span data-ttu-id="315f1-298">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="315f1-298">Axs Exchange</span></span>
    
- <span data-ttu-id="315f1-299">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="315f1-299">Axs Local Archive</span></span>
    
- <span data-ttu-id="315f1-300">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="315f1-300">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="315f1-301">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="315f1-301">Axs Signed</span></span>
    
- <span data-ttu-id="315f1-302">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="315f1-302">Bloomberg</span></span>
    
- <span data-ttu-id="315f1-303">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="315f1-303">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="315f1-304">Verba</span><span class="sxs-lookup"><span data-stu-id="315f1-304">Verba</span></span>

<span data-ttu-id="315f1-305">[Verba](https://www.verba.com) unterstützt die folgenden drittanbieterdaten Quellen:</span><span class="sxs-lookup"><span data-stu-id="315f1-305">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="315f1-306">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="315f1-306">Avaya Aura Video</span></span>
    
- <span data-ttu-id="315f1-307">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-307">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="315f1-308">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="315f1-308">Avtec Radio</span></span>
    
- <span data-ttu-id="315f1-309">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="315f1-309">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="315f1-310">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="315f1-310">BroadSoft Video</span></span>
    
- <span data-ttu-id="315f1-311">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-311">BroadSoft Voice</span></span>
    
- <span data-ttu-id="315f1-312">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-312">Centile Voice</span></span>
    
- <span data-ttu-id="315f1-313">Chatnachricht in Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="315f1-313">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="315f1-314">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="315f1-314">Cisco UC Video</span></span>
    
- <span data-ttu-id="315f1-315">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-315">Cisco UC Voice</span></span>
    
- <span data-ttu-id="315f1-316">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="315f1-316">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="315f1-317">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-317">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="315f1-318">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="315f1-318">ESChat Radio</span></span>
    
- <span data-ttu-id="315f1-319">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="315f1-319">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="315f1-320">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-320">IP Trade Voice</span></span>
    
- <span data-ttu-id="315f1-321">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="315f1-321">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="315f1-322">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="315f1-322">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="315f1-323">Mitel MiContact Center for Lync (prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="315f1-323">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="315f1-324">Oracle/Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="315f1-324">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="315f1-325">Oracle/Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-325">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="315f1-326">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-326">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="315f1-327">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="315f1-327">SIPREC Video</span></span>
    
-  <span data-ttu-id="315f1-328">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-328">SIPREC Voice</span></span> 
    
- <span data-ttu-id="315f1-329">Chatnachricht in Skype for Business/Lync</span><span class="sxs-lookup"><span data-stu-id="315f1-329">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="315f1-330">Skype for Business/Lync Video</span><span class="sxs-lookup"><span data-stu-id="315f1-330">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="315f1-331">Skype for Business/Lync Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-331">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="315f1-332">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-332">Speakerbus Voice</span></span>
    
- <span data-ttu-id="315f1-333">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="315f1-333">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="315f1-334">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-334">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="315f1-335">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="315f1-335">Truphone Voice</span></span>
    
- <span data-ttu-id="315f1-336">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="315f1-336">TwistedPair Radio</span></span>
    
- <span data-ttu-id="315f1-337">Windows Desktop-Computerbildschirm</span><span class="sxs-lookup"><span data-stu-id="315f1-337">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="315f1-338">Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="315f1-338">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="315f1-339">Hier finden Sie die Schritte zum Erstellen und Konfigurieren eines Drittanbieter-Daten Postfachs zum Importieren von Daten in Office 365.</span><span class="sxs-lookup"><span data-stu-id="315f1-339">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365.</span></span> <span data-ttu-id="315f1-340">Wie bereits erläutert, werden Elemente in dieses Postfach importiert, wenn der Partner-Konnektor die Benutzer-ID des Elements nicht einem Office 365-Benutzerkonto zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="315f1-340">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="315f1-341">**Führen Sie diese Aufgaben im Microsoft 365 Admin Center aus.**</span><span class="sxs-lookup"><span data-stu-id="315f1-341">**Complete these tasks in the Microsoft 365 admin center**</span></span>
  
1. <span data-ttu-id="315f1-342">Erstellen Sie ein neues Benutzerkonto in Office 365, und weisen Sie ihm eine Exchange Online-Plan 2-Lizenz zu. Weitere Informationen finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span><span class="sxs-lookup"><span data-stu-id="315f1-342">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="315f1-343">Eine Plan 2-Lizenz ist erforderlich, um für das Postfach ein aufbewahrungsVerfahren durchzuführen oder ein Archivpostfach mit einem unbegrenzten Speicherkontingent zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-343">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="315f1-344">Fügen Sie das Benutzerkonto für das Drittanbieter-Daten Postfach der **Exchange-Administrator** Rolle in Office 365 hinzu. Weitere Informationen finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="315f1-344">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="315f1-345">Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="315f1-345">Write down the credentials for this user account.</span></span> <span data-ttu-id="315f1-346">Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="315f1-346">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="315f1-347">**Ausführen dieser Aufgaben im Exchange Admin Center**</span><span class="sxs-lookup"><span data-stu-id="315f1-347">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="315f1-348">Ausblenden des Drittanbieter-Daten Postfachs aus dem Adressbuch und anderen Adresslisten in Ihrer Organisation; Weitere Informationen finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span><span class="sxs-lookup"><span data-stu-id="315f1-348">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="315f1-349">Alternativ können Sie den folgenden PowerShell-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="315f1-349">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="315f1-350">Weisen Sie dem Drittanbieter-Daten Postfach die Berechtigung **FullAccess** zu, damit Administratoren oder Compliance Officers das Drittanbieter-Daten Postfach im Outlook-Desktop Client öffnen können. Weitere Informationen finden Sie unter [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="315f1-350">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="315f1-351">Aktivieren Sie die folgenden kompatibilitätsbezogenen Office 365-Features für das Drittanbieter-Daten Postfach:</span><span class="sxs-lookup"><span data-stu-id="315f1-351">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="315f1-352">Aktivieren Sie das Archivpostfach. siehe [Aktivieren von archivpostfächern](enable-archive-mailboxes.md) und Aktivieren der unbegrenzten [Archivierung](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-352">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="315f1-353">Auf diese Weise können Sie Speicherplatz im primären Postfach freigeben, indem Sie eine Archivrichtlinie einrichten, mit der Drittanbieter-Datenelemente in das Archivpostfach verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-353">This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="315f1-354">Dadurch erhalten Sie unbegrenzten Speicherplatz für drittanbieterdaten.</span><span class="sxs-lookup"><span data-stu-id="315f1-354">This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="315f1-355">Aktivieren Sie für das Drittanbieterdaten-Postfach das Beweissicherungsverfahren.</span><span class="sxs-lookup"><span data-stu-id="315f1-355">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="315f1-356">Sie können auch eine Office 365-Aufbewahrungsrichtlinie im Security and Compliance Center anwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-356">You can also apply an Office 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="315f1-357">Wenn Sie dieses Postfach anhalten, werden Datenelemente von Drittanbietern (auf unbestimmte Zeit oder für eine bestimmte Dauer) aufbewahrt und verhindert, dass Sie aus dem Postfach gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-357">Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="315f1-358">Lesen Sie eines der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="315f1-358">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="315f1-359">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="315f1-359">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="315f1-360">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="315f1-360">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="315f1-361">Aktivieren der postfachüberwachungsprotokollierung für Besitzer-, Stellvertreter-und Administratorzugriff auf das Drittanbieter-Daten Postfach Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-361">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="315f1-362">Auf diese Weise können Sie alle Aktivitäten überwachen, die von jedem Benutzer ausgeführt werden, der Zugriff auf das Drittanbieter-Daten Postfach hat.</span><span class="sxs-lookup"><span data-stu-id="315f1-362">This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="315f1-363">Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="315f1-363">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="315f1-364">Als Nächstes müssen Sie die Benutzerpostfächer für die Unterstützung von Drittanbieterdaten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-364">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="315f1-365">Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="315f1-365">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="315f1-366">Aktivieren Sie das Archivpostfach für jeden Benutzer; siehe [Aktivieren von archivpostfächern](enable-archive-mailboxes.md) und Aktivieren der unbegrenzten [Archivierung](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-366">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="315f1-367">Platzieren von Benutzerpostfächern für die Aufbewahrung von Rechtsstreitigkeiten oder Anwenden einer Office 365-Archivierungsrichtlinie Lesen Sie eines der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="315f1-367">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="315f1-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="315f1-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="315f1-369">Übersicht über Aufbewahrungsrichtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="315f1-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="315f1-370">Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="315f1-370">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="315f1-371">Schritt 4: Bereitstellen von Informationen für Ihren Partner</span><span class="sxs-lookup"><span data-stu-id="315f1-371">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="315f1-372">Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-372">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="315f1-373">Der Endpunkt, der zum Herstellen einer Verbindung mit dem Azure-Dienst in Office 365 verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="315f1-373">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="315f1-374">Die Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) des Drittanbieter-Daten Postfachs, das Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="315f1-374">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="315f1-375">Diese Anmeldeinformationen sind erforderlich, damit der Partnerconnector auf Elemente zugreifen und sie in das Drittanbieterdaten-Postfach importieren kann.</span><span class="sxs-lookup"><span data-stu-id="315f1-375">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="315f1-376">Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="315f1-376">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="315f1-377">Ab dem 30. September 2018 beginnt der Azure-Dienst in Office 365 mit der Verwendung der modernen Authentifizierung in Exchange Online, um Drittanbieter-Datenkonnektoren zu authentifizieren, die versuchen, eine Verbindung mit Ihrer Office 365-Organisation herzustellen, um Daten zu importieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-377">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data.</span></span> <span data-ttu-id="315f1-378">Der Grund für diese Änderung besteht darin, dass die moderne Authentifizierung mehr Sicherheit bietet als die aktuelle Methode, die auf dem Whitelisting von Drittanbieter-Connectors basiert, die den zuvor beschriebenen Endpunkt zum Herstellen einer Verbindung mit dem Azure-Dienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-378">The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="315f1-379">Damit ein Drittanbieter-Datenkonnektor mit der neuen modernen Authentifizierungsmethode eine Verbindung mit Office 365 herstellen kann, muss ein Administrator in Ihrer Office 365-Organisation mit der Registrierung des Connectors als vertrauenswürdige Dienstanwendung in Azure Active Directory einverstanden sein.</span><span class="sxs-lookup"><span data-stu-id="315f1-379">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="315f1-380">Hierzu wird eine Berechtigungsanforderung akzeptiert, damit der Connector auf die Daten Ihrer Organisation in Azure Active Directory zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="315f1-380">This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="315f1-381">Nachdem Sie diese Anforderung angenommen haben, wird der Drittanbieter-Datenkonnektor als Unternehmensanwendung zu Azure Active Directory hinzugefügt und als Dienstprinzipal dargestellt.</span><span class="sxs-lookup"><span data-stu-id="315f1-381">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="315f1-382">Weitere Informationen zum Zustimmungsprozess finden Sie unter [mandantEnadministrator-Einwilligung](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="315f1-382">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="315f1-383">Hier sind die Schritte zum Zugreifen auf und akzeptieren der Anforderung zur Registrierung des Connectors:</span><span class="sxs-lookup"><span data-stu-id="315f1-383">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="315f1-384">Wechseln Sie zu [dieser Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) , und melden Sie sich mit den Anmeldeinformationen eines globalen Office 365-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="315f1-384">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="315f1-385">Das folgende Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="315f1-385">The following dialog box is displayed.</span></span> <span data-ttu-id="315f1-386">Sie können die "Carets" erweitern, um die Berechtigungen zu überarbeiten, die dem Connector zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-386">You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="315f1-387">![Das Dialogfeld Berechtigungsanforderung wird angezeigt.](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="315f1-387">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="315f1-388">Klicken Sie auf **Annehmen**.</span><span class="sxs-lookup"><span data-stu-id="315f1-388">Click **Accept**.</span></span>

<span data-ttu-id="315f1-389">Nachdem Sie die Anforderung akzeptiert haben, wird das [Azure-Portal](https://portal.azure.com) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="315f1-389">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="315f1-390">Klicken Sie auf **Azure Active Directory** > -**Unternehmensanwendungen**, um die Liste der Anwendungen für Ihre Organisation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="315f1-390">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="315f1-391">Der Office 365-Drittanbieter-Daten-Konnektor ist auf dem Blade **Enterprise-Anwendungen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="315f1-391">The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="315f1-392">Nach dem 30. September 2018 werden drittanbieterdaten nicht mehr in Postfächer in Ihrer Organisation importiert, wenn Sie keinen Drittanbieter-Daten-Konnektor in Azure Active Directory registrieren.</span><span class="sxs-lookup"><span data-stu-id="315f1-392">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="315f1-393">Hinweis vorhandene Drittanbieter-Datenkonnektoren (die vor dem 30. September 2018 erstellt wurden) müssen auch in Azure Active Directory registriert werden, indem Sie das Verfahren in Schritt 5 befolgen.</span><span class="sxs-lookup"><span data-stu-id="315f1-393">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="315f1-394">Widerrufen der Zustimmung für einen Drittanbieter-Daten-Konnektor</span><span class="sxs-lookup"><span data-stu-id="315f1-394">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="315f1-395">Nachdem Ihre Organisation der Berechtigungsanforderung zur Registrierung eines Drittanbieter-Daten-Konnektors in Azure Active Directory zugestimmt hat, kann Ihre Organisation diese Einwilligung jederzeit widerrufen.</span><span class="sxs-lookup"><span data-stu-id="315f1-395">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="315f1-396">Das Widerrufen der Zustimmung für einen Connector bedeutet jedoch, dass Daten aus der Drittanbieter-Datenquelle nicht mehr in Office 365 importiert werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-396">However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="315f1-397">Um die Einwilligung für einen Drittanbieter-Datenkonnektor zu widerrufen, können Sie die Anwendung (durch Löschen des entsprechenden Dienst Prinzipals) aus Azure Active Directory mithilfe des Blades " **Enterprise-Anwendungen** " im Azure-Portal oder mithilfe der [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="315f1-397">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span></span> <span data-ttu-id="315f1-398">Sie können auch das Cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) in Azure Active Directory PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-398">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="315f1-399">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="315f1-399">More information</span></span>

- <span data-ttu-id="315f1-400">Wie bereits weiter oben erläutert, werden Elemente aus Drittanbieter-Datenquellen als E-Mail-Nachrichten in Exchange-Postfächer importiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-400">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="315f1-401">Der Partner-Konnektor importiert das Element mithilfe eines für die Office 365-API erforderlichen Schemas.</span><span class="sxs-lookup"><span data-stu-id="315f1-401">The partner connector imports the item using a schema required by the Office 365 API.</span></span> <span data-ttu-id="315f1-402">Die folgende Tabelle beschreibt die Nachrichteneigenschaften eines Elements aus einer Drittanbieter-Datenquelle, nachdem es als E-Mail-Nachricht in ein Exchange-Postfach importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="315f1-402">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="315f1-403">Zudem ist angegeben, wenn die Nachrichteneigenschaft zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="315f1-403">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="315f1-404">Erforderliche Eigenschaften müssen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-404">Mandatory properties must be populated.</span></span> <span data-ttu-id="315f1-405">Wenn für ein Element eine obligatorische Eigenschaft fehlt, wird es nicht in Office 365 importiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-405">If an item is missing a mandatory property, it won't be imported to Office 365.</span></span> <span data-ttu-id="315f1-406">Der Importvorgang gibt eine Fehlermeldung zurück, in der erklärt wird, warum ein Element nicht importiert wurde und welche Eigenschaft fehlt.</span><span class="sxs-lookup"><span data-stu-id="315f1-406">The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="315f1-407">**Nachrichteneigenschaft**</span><span class="sxs-lookup"><span data-stu-id="315f1-407">**Message property**</span></span>|<span data-ttu-id="315f1-408">**Erforderlich?**</span><span class="sxs-lookup"><span data-stu-id="315f1-408">**Mandatory?**</span></span>|<span data-ttu-id="315f1-409">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="315f1-409">**Description**</span></span>|<span data-ttu-id="315f1-410">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="315f1-410">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="315f1-411">**FROM**</span><span class="sxs-lookup"><span data-stu-id="315f1-411">**FROM**</span></span> <br/> |<span data-ttu-id="315f1-412">Ja</span><span class="sxs-lookup"><span data-stu-id="315f1-412">Yes</span></span>  <br/> |<span data-ttu-id="315f1-413">Der Benutzer, der das Element in der Drittanbieter-Datenquelle ursprünglich erstellt oder gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="315f1-413">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="315f1-414">Der Partner-Konnektor versucht, die Benutzer-ID aus dem Quellelement (beispielsweise einem Twitter-handle) einem Office 365-Benutzerkonto für alle Teilnehmer (Benutzer in den Feldern von und bis) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="315f1-414">The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="315f1-415">Eine Kopie der Nachricht wird in das Postfach jedes Teilnehmers importiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-415">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="315f1-416">Wenn keiner der Teilnehmer des Elements einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element in das Archivierungs Postfach eines Drittanbieters in Office 365 importiert.</span><span class="sxs-lookup"><span data-stu-id="315f1-416">If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.</span></span>  <br/> <br/> <span data-ttu-id="315f1-417">Der Teilnehmer, der als Absender des Elements identifiziert wird, muss über ein aktives Postfach in der Office 365-Organisation verfügen, in das das Element importiert wird.</span><span class="sxs-lookup"><span data-stu-id="315f1-417">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to.</span></span> <span data-ttu-id="315f1-418">Wenn der Absender nicht über ein aktives Postfach verfügt, wird der folgende Fehler zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="315f1-418">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="315f1-419">**TO**</span><span class="sxs-lookup"><span data-stu-id="315f1-419">**TO**</span></span> <br/> |<span data-ttu-id="315f1-420">Ja</span><span class="sxs-lookup"><span data-stu-id="315f1-420">Yes</span></span>  <br/> |<span data-ttu-id="315f1-421">Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).</span><span class="sxs-lookup"><span data-stu-id="315f1-421">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="315f1-422">**Betreff**</span><span class="sxs-lookup"><span data-stu-id="315f1-422">**SUBJECT**</span></span> <br/> |<span data-ttu-id="315f1-423">Nein</span><span class="sxs-lookup"><span data-stu-id="315f1-423">No</span></span>  <br/> |<span data-ttu-id="315f1-424">Der Betreff des Quellelements.</span><span class="sxs-lookup"><span data-stu-id="315f1-424">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="315f1-425">**Datum**</span><span class="sxs-lookup"><span data-stu-id="315f1-425">**DATE**</span></span> <br/> |<span data-ttu-id="315f1-426">Ja</span><span class="sxs-lookup"><span data-stu-id="315f1-426">Yes</span></span>  <br/> |<span data-ttu-id="315f1-427">Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.</span><span class="sxs-lookup"><span data-stu-id="315f1-427">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="315f1-428">**Text**</span><span class="sxs-lookup"><span data-stu-id="315f1-428">**BODY**</span></span> <br/> |<span data-ttu-id="315f1-429">Nein</span><span class="sxs-lookup"><span data-stu-id="315f1-429">No</span></span>  <br/> |<span data-ttu-id="315f1-430">Der Inhalt der Nachricht oder des Beitrags.</span><span class="sxs-lookup"><span data-stu-id="315f1-430">The contents of the message or post.</span></span> <span data-ttu-id="315f1-431">Bei einigen Datenquellen kann der Inhalt dieser Eigenschaft mit dem Inhalt der Eigenschaft **SUBJECT** identisch sein.</span><span class="sxs-lookup"><span data-stu-id="315f1-431">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="315f1-432">Während des Importvorgangs versucht der Partnerconnector, die Inhaltsquelle so originalgetreu wie möglich beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="315f1-432">During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="315f1-433">Soweit möglich, werden Dateien, Grafiken oder andere Inhalte aus dem Textkörper des Quellelements in diese Eigenschaft einbezogen.</span><span class="sxs-lookup"><span data-stu-id="315f1-433">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="315f1-434">Andernfalls wird der Inhalt aus dem Quellelement in die Eigenschaft **ATTACHMENT** einbezogen.</span><span class="sxs-lookup"><span data-stu-id="315f1-434">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="315f1-435">Der Inhalt dieser Eigenschaft hängt vom Partner-Konnektor und von der Funktion der QuellPlattform ab.</span><span class="sxs-lookup"><span data-stu-id="315f1-435">The contents of this property will depend on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="315f1-436">**Anlage**</span><span class="sxs-lookup"><span data-stu-id="315f1-436">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="315f1-437">Nein</span><span class="sxs-lookup"><span data-stu-id="315f1-437">No</span></span>  <br/> |<span data-ttu-id="315f1-438">Wenn ein Element in der Datenquelle (beispielsweise ein tweet in Twitter oder eine Sofortnachrichtenunterhaltung) über eine angefügte Datei verfügt oder Bilder enthält, versucht der Partner Connect zunächst, Anlagen in die **Body** -Eigenschaft einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="315f1-438">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="315f1-439">Wenn dies nicht möglich ist, wird Sie der \* \* ATTACHMENT \* \*-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="315f1-439">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="315f1-440">Weitere Beispiele für Anlagen sind „Gefällt mir“-Angaben in Facebook, Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder einen Beitrag.</span><span class="sxs-lookup"><span data-stu-id="315f1-440">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="315f1-441">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="315f1-441">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="315f1-442">Ja</span><span class="sxs-lookup"><span data-stu-id="315f1-442">Yes</span></span>  <br/> | <span data-ttu-id="315f1-443">Dies ist eine Eigenschaft mit mehreren Werten, die vom Partnerconnector erstellt und mit Werten gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="315f1-443">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="315f1-444">Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`.</span><span class="sxs-lookup"><span data-stu-id="315f1-444">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="315f1-445">(Diese Eigenschaft muss mit `IPM.NOTE`beginnen; dieses Format ähnelt der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="315f1-445">(This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="315f1-446">`Source`-Gibt die Datenquelle eines Drittanbieters an. beispielsweise Twitter, Facebook oder BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="315f1-446">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="315f1-447">`Event`-Gibt die Art der Aktivität an, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erstellt hat; zum Beispiel ein tweet in Twitter oder ein Beitrag in Facebook.</span><span class="sxs-lookup"><span data-stu-id="315f1-447">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="315f1-448">Ereignisse sind für die jeweilige Datenquelle spezifisch.</span><span class="sxs-lookup"><span data-stu-id="315f1-448">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="315f1-449">Ein Zweck dieser Eigenschaft ist es zum Beispiel, bestimmte Elemente basierend auf der Datenquelle zu filtern, aus der ein Element stammt, oder basierend auf dem Typ des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="315f1-449">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="315f1-450">So könnten Sie in einer eDiscovery-Suche zum Beispiel eine Suchabfrage erstellen, um alle Tweets zu finden, die von einem bestimmten Benutzer gepostet wurden.</span><span class="sxs-lookup"><span data-stu-id="315f1-450">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="315f1-451">Wenn Elemente erfolgreich in Postfächer in Office 365 importiert werden, wird ein eindeutiger Bezeichner als Teil der HTTP-Antwort an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="315f1-451">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="315f1-452">Dieser Bezeichner – genannt `x-IngestionCorrelationID`– kann für nachfolgende Problembehandlungszwecke von Partnern für die End-to-End-Nachverfolgung von Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="315f1-452">This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="315f1-453">Es wird empfohlen, dass Partner diese Informationen entsprechend erfassen und sammeln.</span><span class="sxs-lookup"><span data-stu-id="315f1-453">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="315f1-454">Im Folgenden ist ein Beispiel einer HTTP-Antwort mit diesem Bezeichner aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="315f1-454">Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="315f1-455">Sie können das Inhaltssuche-Tool im Security and Compliance Center verwenden, um nach Elementen zu suchen, die in Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="315f1-455">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="315f1-456">Wenn Sie speziell nach diesen importierten Elementen suchen möchten, können Sie die folgenden Nachrichten Eigenschaftswert-Paare im Stichwortfeld für eine Inhaltssuche verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-456">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="315f1-457">**`kind:externaldata`**-Verwenden Sie dieses Eigenschaft-Wert-Paar zum Durchsuchen aller Drittanbieter-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="315f1-457">**`kind:externaldata`** - Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="315f1-458">Wenn Sie beispielsweise nach Elementen suchen möchten, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in der Subject-Eigenschaft des importierten Elements enthalten haben, würden Sie `kind:externaldata AND subject:contoso`die Stichwortabfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-458">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="315f1-459">**`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses Eigenschaft-Wert-Paar nur, um einen angegebenen Typ von drittanbieterdaten zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="315f1-459">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="315f1-460">Wenn Sie beispielsweise nur Facebook-Daten durchsuchen möchten, die das Wort "Contoso" in der Subject-Eigenschaft enthalten, würden `itemclass:ipm.externaldata.Facebook* AND subject:contoso`Sie die Stichwortabfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="315f1-460">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="315f1-461">Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` Eigenschaft finden Sie unter Verwenden der [Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden](use-content-search-to-search-third-party-data-that-was-imported.md) .</span><span class="sxs-lookup"><span data-stu-id="315f1-461">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="315f1-462">Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="315f1-462">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="315f1-463">Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="315f1-463">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="315f1-464">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="315f1-464">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 

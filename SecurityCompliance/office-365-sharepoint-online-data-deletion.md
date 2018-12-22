---
title: Office 365 SharePoint Online-Daten löschen
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Erläuterung der Löschung von Daten in SharePoint Online.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411161"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="5e1f4-103">SharePoint Online-Daten löschen in Office 365</span><span class="sxs-lookup"><span data-stu-id="5e1f4-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="5e1f4-p101">SharePoint Online werden Objekte als abstrahiert Code in Datenbanken gespeichert. Wenn ein Benutzer eine Datei mit SharePoint Online hochgeladen wird, wird diese Datei zerlegt und in der Anwendungscode übersetzt und in mehreren Tabellen in mehreren Datenbanken gespeichert. Alle Inhalte, die ein Kunde hochlädt ist in SharePoint Online-Segmenten verschlüsselt (potenziell mit mehreren AES 256-Bit-Schlüssel), aufgeschlüsselt und Datencenter verteilt. Ausführliche Informationen zum Prozess Segmentierung und Verschlüsselung finden Sie unter [Verschlüsselung in der Microsoft-Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5e1f4-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="5e1f4-p102">In SharePoint Online – werden Elemente für 93 Tagen ab dem Zeitpunkt beibehalten, die Sie sie aus dem ursprünglichen Speicherort löschen. Sie bleiben im Papierkorb der Website die gesamte Zeit, es sei denn, ein Benutzer löscht diese dann von dort aus oder, Papierkorb Leert. In diesem Fall werden die Elemente der Websitesammlung Papierkorb, wobei sie für den Rest der 93 Tage bleiben. Informationen zum Wiederherstellen von gelöschten Elementen finden Sie unter [Wiederherstellen von Elementen im Papierkorb der SharePoint-Website](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Die Aufbewahrungszeit Recycle Bin ist nicht konfigurierbar in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="5e1f4-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="5e1f4-113">Wenn Sie eine Websitesammlung löschen, sind Sie auch die Hierarchie der Websites in der Auflistung und alle Inhalte zu löschen:</span><span class="sxs-lookup"><span data-stu-id="5e1f4-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="5e1f4-114">Dokumente und Dokumentbibliotheken</span><span class="sxs-lookup"><span data-stu-id="5e1f4-114">Documents and document libraries</span></span>
- <span data-ttu-id="5e1f4-115">Listen und Listendaten</span><span class="sxs-lookup"><span data-stu-id="5e1f4-115">Lists and list data</span></span>
- <span data-ttu-id="5e1f4-116">Einstellungen für die Websitekonfiguration</span><span class="sxs-lookup"><span data-stu-id="5e1f4-116">Site configuration settings</span></span>
- <span data-ttu-id="5e1f4-117">Rolle und Sicherheitsinformationen Informationen, die auf der Website oder Unterwebsites zusammenhängt</span><span class="sxs-lookup"><span data-stu-id="5e1f4-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="5e1f4-118">Unterwebsites der Website, deren Inhalt und Benutzer auf oberster Ebene Informationen</span><span class="sxs-lookup"><span data-stu-id="5e1f4-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="5e1f4-119">Wenn Sie eine Websitesammlung versehentlich gelöscht haben, können sie durch ein globaler oder SharePoint wiederhergestellt Admin mit der SharePoint-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="5e1f4-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="5e1f4-p103">Festplatte Löschvorgang tritt auf, wenn ein Benutzer gelöschte Elemente aus der Websitesammlung des Papierkorbs löscht, wenn die Archivierung und Sicherung Perioden ablaufen oder ein Administrator eine Websitesammlung mit dem [Remove-SPODeletedSite-Cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)dauerhaft gelöscht. Wenn ein harte Benutzer löscht (dauerhaft gelöscht oder löscht) Inhalte aus SharePoint Online, alle Verschlüsselungsschlüssel für die gelöschten Blöcke werden ebenfalls gelöscht. Die Blöcke auf den Datenträgern, die die gelöschten Blöcke zuvor gespeichert werden als nicht verwendete und bereit zur Wiederverwendung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5e1f4-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>

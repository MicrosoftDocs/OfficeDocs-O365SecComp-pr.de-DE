---
title: Office 365 SharePoint Online-Datenlöschung
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Erklärung zum Löschen von Daten in SharePoint Online.
ms.openlocfilehash: 6d4989bc4b503309ba50237a164bffebaff1e7af
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218425"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="4c4d0-103">Löschen von SharePoint Online-Daten in Office 365</span><span class="sxs-lookup"><span data-stu-id="4c4d0-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="4c4d0-p101">SharePoint Online speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer eine Datei in SharePoint Online hochlädt, wird diese Datei zerlegt und in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken gespeichert. In SharePoint Online werden alle Inhalte, die ein Kunde hochlädt, in Abschnitte unterteilt, verschlüsselt (potenziell mit mehreren AES 256-Bit-Schlüsseln) und über das Datencenter verteilt. Ausführliche Informationen zum Chunking-und Verschlüsselungsprozess finden Sie unter [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4c4d0-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="4c4d0-p102">In SharePoint Online werden Elemente 93 Tage lang aufbewahrt, ab dem Zeitpunkt, zu dem Sie Sie vom ursprünglichen Speicherort gelöscht haben. Sie bleiben die gesamte Zeit im Papierkorb der Website, es sei denn, Sie werden von dort gelöscht oder geleert. In diesem Fall gehen die Elemente in den Papierkorb der Websitesammlung, in dem Sie für den Rest der 93 Tage verbleiben. Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter [Wiederherstellen von Elementen im Papierkorb einer SharePoint-Website](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Die Aufbewahrungszeit des Papierkorbs kann in SharePoint Online nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4c4d0-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="4c4d0-113">Wenn Sie eine Websitesammlung löschen, löschen Sie auch die Hierarchie der Websites in der Auflistung und alle darin enthaltenen Inhalte:</span><span class="sxs-lookup"><span data-stu-id="4c4d0-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="4c4d0-114">Dokumente und Dokumentbibliotheken</span><span class="sxs-lookup"><span data-stu-id="4c4d0-114">Documents and document libraries</span></span>
- <span data-ttu-id="4c4d0-115">Listen und Auflisten von Daten</span><span class="sxs-lookup"><span data-stu-id="4c4d0-115">Lists and list data</span></span>
- <span data-ttu-id="4c4d0-116">Website Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="4c4d0-116">Site configuration settings</span></span>
- <span data-ttu-id="4c4d0-117">Rollen-und Sicherheitsinformationen im Zusammenhang mit der Website oder ihren Unterwebsites</span><span class="sxs-lookup"><span data-stu-id="4c4d0-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="4c4d0-118">Unterwebsites der Website auf höchster Ebene, deren Inhalte und Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="4c4d0-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="4c4d0-119">Wenn Sie eine Websitesammlung versehentlich löschen, kann Sie von einem globalen oder SharePoint-Administrator mithilfe des SharePoint admin Centers wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4c4d0-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="4c4d0-p103">Das harte löschen tritt auf, wenn ein Benutzer gelöschte Elemente aus dem Papierkorb der Websitesammlung löscht, wenn die Aufbewahrungs-und Sicherungs Zeiträume abgelaufen sind oder wenn ein Administrator eine Websitesammlung mithilfe des [Remove-SPODeletedSite-Cmdlets](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)dauerhaft gelöscht. Wenn ein Benutzer Inhalte aus SharePoint Online löscht (dauerhaft gelöscht oder löscht), werden auch alle Verschlüsselungsschlüssel für die gelöschten Chunks gelöscht. Die Blöcke auf den Datenträgern, die zuvor die gelöschten Chunks gespeichert haben, werden als nicht verwendet markiert und können wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c4d0-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>

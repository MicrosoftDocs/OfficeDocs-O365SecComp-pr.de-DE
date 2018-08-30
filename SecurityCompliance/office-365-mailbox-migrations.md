---
title: Office 365-Postfachmigration
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine kurze Zusammenfassung der Cmdlets für Office 365-Postfachmigrationen verwendet.
ms.openlocfilehash: 86896d956072b5c11e3b3292363bb32312ff1187
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529705"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="99cef-103">Office 365-Postfachmigration</span><span class="sxs-lookup"><span data-stu-id="99cef-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="99cef-p101">Kunden können mit einer Exchange-basierte hybridbereitstellung lokalen Exchange-Postfächern zu [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) -Organisation verschieben oder Exchange Online-Postfächern für eine [lokale Exchange -](https://docs.microsoft.com/Exchange/exchange-server) Organisation verschieben. Migrationsbatches werden beim Verschieben von Postfächern zwischen lokalen und Exchange Online-Organisationen verwendet. Kunden können Statistiken und andere Informationen zu Postfachmigrationen mit den folgenden Cmdlets überprüfen:</span><span class="sxs-lookup"><span data-stu-id="99cef-p101">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization. Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations. Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="99cef-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - bietet standardstatistiken für ein Benutzerpostfach, einschließlich der Status, die Postfachgröße, archivieren Postfachgröße "und" Prozent abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="99cef-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="99cef-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - bietet eine Übersichtsliste Postfachobjekte und-Attribute in der Organisation.</span><span class="sxs-lookup"><span data-stu-id="99cef-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="99cef-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - enthält eine Liste der vorhandenen e-Mail-aktivierte Objekte wie Postfächer, e-Mail-Benutzer, Kontakte und Verteilergruppen.</span><span class="sxs-lookup"><span data-stu-id="99cef-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="99cef-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - bietet einen detaillierten Status einer laufenden Postfachmigration.</span><span class="sxs-lookup"><span data-stu-id="99cef-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="99cef-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - enthält Informationen über das Postfach verschiebungs- und migrationsbenutzern.</span><span class="sxs-lookup"><span data-stu-id="99cef-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="99cef-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - enthält Informationen zu den Status des aktuellen migrationsbatch.</span><span class="sxs-lookup"><span data-stu-id="99cef-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="99cef-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - enthält ausführliche Informationen zum Migrationsstatus für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="99cef-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="99cef-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - bietet Informationen zu Postfächern, wie Größe, die Anzahl der Nachrichten und den Zeitpunkt des letzten Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="99cef-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="99cef-115">Weitere Informationen zu zusätzlichen Cmdlets finden Sie unter [Verschiebungs- und Migrations-Cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="99cef-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>

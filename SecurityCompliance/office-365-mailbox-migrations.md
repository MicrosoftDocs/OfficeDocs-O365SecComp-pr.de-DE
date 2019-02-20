---
title: Office 365-Postfachmigrationen
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine kurze Zusammenfassung der Cmdlets für die Migration von Office 365-Postfächern.
ms.openlocfilehash: 195497d94ab434c66a176e37fb84f6cd1da48baa
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090777"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="025a2-103">Office 365-Postfachmigrationen</span><span class="sxs-lookup"><span data-stu-id="025a2-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="025a2-p101">Bei einer Exchange-basierten hybridbereitstellung können Kunden wahlweise lokale Exchange-Postfächer in eine [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) -Organisation verschieben oder Exchange Online-Postfächer in eine [lokale Exchange](https://docs.microsoft.com/Exchange/exchange-server) -Organisation verschieben. Migrationsbatches werden beim Verschieben von Postfächern zwischen lokalen und Exchange Online-Organisationen verwendet. Kunden können Statistiken und weitere Informationen zu Postfachmigrationen mithilfe der folgenden Cmdlets überarbeiten:</span><span class="sxs-lookup"><span data-stu-id="025a2-p101">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization. Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations. Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="025a2-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) – stellt Standardstatistiken für ein Benutzerpostfach bereit, das den Status, die Postfachgröße, die Größe des Archivpostfachs und den abgeschlossenen Prozentsatz umfasst.</span><span class="sxs-lookup"><span data-stu-id="025a2-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="025a2-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) – enthält eine Zusammenfassungsliste der Postfachobjekte und-Attribute in der Organisation.</span><span class="sxs-lookup"><span data-stu-id="025a2-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="025a2-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) – enthält eine Liste vorhandener e-Mail-aktivierter Objekte wie Postfächer, e-Mail-Benutzer, Kontakte und Verteilergruppen.</span><span class="sxs-lookup"><span data-stu-id="025a2-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="025a2-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) – liefert einen detaillierten Status einer laufenden Postfachmigration.</span><span class="sxs-lookup"><span data-stu-id="025a2-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="025a2-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) – enthält Informationen zu den Benutzern für die Postfachverschiebung und-Migration.</span><span class="sxs-lookup"><span data-stu-id="025a2-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="025a2-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) – enthält Informationen zum Status des aktuellen Migrationsbatches.</span><span class="sxs-lookup"><span data-stu-id="025a2-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="025a2-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) – enthält detaillierte Informationen zum Migrationsstatus für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="025a2-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="025a2-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) – enthält Informationen zu Postfächern wie Größe, Anzahl der Nachrichten und Uhrzeit des letzten Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="025a2-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="025a2-115">Weitere Informationen zu zusätzlichen Cmdlets finden Sie unter [Move and Migration Cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="025a2-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>

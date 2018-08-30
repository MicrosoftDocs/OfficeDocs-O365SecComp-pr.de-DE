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
# <a name="office-365-mailbox-migrations"></a>Office 365-Postfachmigration
Kunden können mit einer Exchange-basierte hybridbereitstellung lokalen Exchange-Postfächern zu [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) -Organisation verschieben oder Exchange Online-Postfächern für eine [lokale Exchange -](https://docs.microsoft.com/Exchange/exchange-server) Organisation verschieben. Migrationsbatches werden beim Verschieben von Postfächern zwischen lokalen und Exchange Online-Organisationen verwendet. Kunden können Statistiken und andere Informationen zu Postfachmigrationen mit den folgenden Cmdlets überprüfen:

- [Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - bietet standardstatistiken für ein Benutzerpostfach, einschließlich der Status, die Postfachgröße, archivieren Postfachgröße "und" Prozent abgeschlossen.
- [Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - bietet eine Übersichtsliste Postfachobjekte und-Attribute in der Organisation.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - enthält eine Liste der vorhandenen e-Mail-aktivierte Objekte wie Postfächer, e-Mail-Benutzer, Kontakte und Verteilergruppen.
- [Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - bietet einen detaillierten Status einer laufenden Postfachmigration.
- [Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - enthält Informationen über das Postfach verschiebungs- und migrationsbenutzern.
- [Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - enthält Informationen zu den Status des aktuellen migrationsbatch.
- [Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - enthält ausführliche Informationen zum Migrationsstatus für einen bestimmten Benutzer.
- [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - bietet Informationen zu Postfächern, wie Größe, die Anzahl der Nachrichten und den Zeitpunkt des letzten Zugriffs.

Weitere Informationen zu zusätzlichen Cmdlets finden Sie unter [Verschiebungs- und Migrations-Cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).

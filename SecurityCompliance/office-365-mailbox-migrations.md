---
title: Office 365-Postfachmigrationen
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine kurze Zusammenfassung der Cmdlets für die Migration von Office 365-Postfächern.
ms.openlocfilehash: f21462b1f4a1838ee617e0d429ba73f01ca2db90
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262577"
---
# <a name="office-365-mailbox-migrations"></a>Office 365-Postfachmigrationen
Bei einer Exchange-basierten hybridbereitstellung können Kunden wahlweise lokale Exchange-Postfächer in eine [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) -Organisation verschieben oder Exchange Online-Postfächer in eine [lokale Exchange](https://docs.microsoft.com/Exchange/exchange-server) -Organisation verschieben. Migrationsbatches werden beim Verschieben von Postfächern zwischen lokalen und Exchange Online-Organisationen verwendet. Kunden können Statistiken und weitere Informationen zu Postfachmigrationen mithilfe der folgenden Cmdlets überarbeiten:

- [Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) – stellt Standardstatistiken für ein Benutzerpostfach bereit, das den Status, die Postfachgröße, die Größe des Archivpostfachs und den abgeschlossenen Prozentsatz umfasst.
- [Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) – enthält eine Zusammenfassungsliste der Postfachobjekte und-Attribute in der Organisation.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) – enthält eine Liste vorhandener e-Mail-aktivierter Objekte wie Postfächer, e-Mail-Benutzer, Kontakte und Verteilergruppen.
- [Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) – liefert einen detaillierten Status einer laufenden Postfachmigration.
- [Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) – enthält Informationen zu den Benutzern für die Postfachverschiebung und-Migration.
- [Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) – enthält Informationen zum Status des aktuellen Migrationsbatches.
- [Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) – enthält detaillierte Informationen zum Migrationsstatus für einen bestimmten Benutzer.
- [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) – enthält Informationen zu Postfächern wie Größe, Anzahl der Nachrichten und Uhrzeit des letzten Zugriffs.

Weitere Informationen zu zusätzlichen Cmdlets finden Sie unter [Move and Migration Cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).

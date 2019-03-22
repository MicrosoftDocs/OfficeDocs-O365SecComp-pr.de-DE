---
title: Übersicht über die Nachrichtenflussstatus der oberen Domäne
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren können sich über den Status des Nachrichtenflusses im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center informieren.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 04aa986982465a4c66fbf99f517fb34622d65e19
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722885"
---
# <a name="top-domain-mail-flow-status-insight"></a>Übersicht über die Nachrichtenflussstatus der oberen Domäne

> [!NOTE]
> Die in diesem Thema beschriebenen Features wurden nicht für alle Office 365-Organisationen bereitgestellt und können geändert werden.

Die **Nachrichtenflussstatus-** Einblicke der oberen Domänen bieten Ihnen den aktuellen Status der Domänen Ihrer Organisation im Hinblick auf den Nachrichtenfluss. Diese Einblicke helfen Ihnen bei der Identifizierung und Problembehandlung von Domänen, die Auswirkungen auf die ***Nachrichtenübermittlung*** haben (beispielsweise können keine externen e-Mails empfangen werden), insbesondere Domänen Ablauf oder Domänen mit falschen MX-Einträgen.

![Die obere Domänen-Fluss Status Einblicke im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/domain-mail-flow-status-selected.png)

Wenn Sie im Insight auf **Details anzeigen** klicken, wird ein Flyout angezeigt, in dem Sie weitere Details zum Status jeder Domäne sehen.

Ein grünes Häkchen für eine Domäne gibt den aktuellen MX-Eintrag an (wenn Sie zum Dashboard für Nachrichtenfluss Einblicke navigieren) entspricht dem Wert, den wir im Datensatz haben, und dass die Domäne während der letzten zwei Stunden e-Mails empfangen hat.

Ein rotes x für eine Domäne gibt an, dass der MX-Eintrag geändert wurde und dass die Domäne während der letzten 6 Stunden keine e-Mails erhalten hat. Dies weist darauf hin, dass Ihre Domäne abgelaufen ist oder dass der MX-Eintrag falsch aktualisiert wurde. Erkundigen Sie sich bei Ihrer Domänenregistrierungsstelle oder Ihrem DNS-Hostingdienst, ob die Domäne abgelaufen ist oder ob der MX-Eintrag der Domäne falsch ist.

![Das Detail Flyout im oberen Domänen-Fluss Status Einblicke](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights-v2.md).

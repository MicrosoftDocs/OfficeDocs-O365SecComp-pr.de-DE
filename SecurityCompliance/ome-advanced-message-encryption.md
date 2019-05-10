---
title: Erweiterte Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Die erweiterte Nachrichtenverschlüsselung in Office 365 hilft Organisationen bei der Erfüllung Ihrer Compliance-Verpflichtungen, indem Administratoren das ablaufen und den Zugriff über ein Office 365-Webportal auf verschlüsselte e-Mails verweigern.
ms.openlocfilehash: 5559a2bca4cd804cfcfdf547146eeb416252ca5f
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834904"
---
# <a name="office-365-advanced-message-encryption"></a>Erweiterte Office 365-Nachrichtenverschlüsselung

Office 365 erweiterte Nachrichtenverschlüsselung steht über die Office 365-Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung. Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht die erweiterte Nachrichtenverschlüsselung von Office 365 enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Konformität der Advanced Compliance-SKU erwerben.

Erweiterte Nachrichtenverschlüsselung in Office 365 hilft Kunden bei der Einhaltung von Compliance-Verpflichtungen, die eine flexiblere Kontrolle über externe Empfänger und Ihren Zugriff auf verschlüsselte e-Mails erfordern. Mit der erweiterten Nachrichtenverschlüsselung in Office 365 können Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, mit automatischen Richtlinien steuern. Sie können diese Richtlinien so konfigurieren, dass vertrauliche Informationstypen wie PII, finanzielle oder Integritäts-IDs identifiziert werden, oder Sie verwenden Stichwörter, um den Schutz zu verbessern. Nachdem Sie die Richtlinien konfiguriert haben, koppeln Sie Richtlinien mit benutzerdefinierten e-Mail-Vorlagen und fügen dann ein Ablaufdatum für eine zusätzliche Kontrolle von e-Mails hinzu, die der Richtlinie entsprechen. Außerdem können Administratoren verschlüsselte e-Mails, auf die extern über ein sicheres Webportal zugegriffen wird, weiter steuern, indem Sie den Zugriff auf die e-Mails jederzeit widerrufen.

Sie können nur ein Ablaufdatum für e-Mails, die an externe Empfänger gesendet werden, widerrufen und festlegen.

Wenn Sie eine benutzerdefinierte Branding-Vorlage anwenden, wendet Office 365 mit der erweiterten Nachrichtenverschlüsselung von Office 365 einen Wrapper auf e-Mails an, der der e-Mail-Fluss Regel entspricht, auf die Sie die Vorlage anwenden. Sie können nur Nachrichten widerrufen und Ablaufdatum auf Nachrichten anwenden, die Benutzer über das Portal erhalten. Anders ausgedrückt: e-Mails, auf die eine benutzerdefinierte Branding-Vorlage angewendet wurde.

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Erste Schritte mit Office 365 erweiterte Nachrichtenverschlüsselung

In den folgenden Themen wird beschrieben, wie Sie erweiterte Nachrichtenverschlüsselung einrichten und verwenden.

Ihre Organisation muss über ein Abonnement verfügen, das die erweiterte Nachrichtenverschlüsselung von Office 365 enthält. Ausführliche Informationen zu unterstützten Abonnements finden Sie in der [Nachrichten Richtlinie und im Compliance-Dienst](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).

Wenn Sie keine Office 365-Nachrichtenverschlüsselung eingerichtet haben, finden Sie weitere Informationen unter [Einrichten neuer Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).

[Legen Sie ein Ablaufdatum für e-Mail-Verschlüsseln von Office 365 Advanced Message Encryption fest](ome-advanced-expiration.md). Steuern Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, mit automatischen Richtlinien, die den Schutz erhöhen, indem Sie den Zugriff über ein sicheres Webportal zu verschlüsselten e-Mails verlaufen

[Widerrufen von e-Mails, die von Office 365 verschlüsselt wurden erweiterte Nachrichtenverschlüsselung](revoke-ome-encrypted-mail.md). Steuern Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, und erhöhen Sie den Schutz, indem Sie den Zugriff über ein sicheres Webportal zu verschlüsselten e-Mails widerrufen.  
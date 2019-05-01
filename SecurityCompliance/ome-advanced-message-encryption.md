---
title: Office 365 erweiterte Nachrichtenverschlüsselung
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
ms.openlocfilehash: a775803a8d2678441f319c0145e96e7d19c26f7e
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506719"
---
# <a name="office-365-advanced-message-encryption"></a>Office 365 erweiterte Nachrichtenverschlüsselung

Office 365 erweiterte Nachrichtenverschlüsselung steht über die Office 365-Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung. Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht die erweiterte Nachrichtenverschlüsselung von Office 365 enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Konformität der Advanced Compliance-SKU erwerben.

Dieser Artikel ist Teil einer größeren Artikelreihe zur [Nachrichtenverschlüsselung von Office 365](ome.md).

Erweiterte Nachrichtenverschlüsselung in Office 365 hilft Kunden bei der Einhaltung von Compliance-Verpflichtungen, die eine flexiblere Kontrolle über externe Empfänger und Ihren Zugriff auf verschlüsselte e-Mails erfordern. Mit der erweiterten Nachrichtenverschlüsselung in Office 365 können Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, mit automatischen Richtlinien steuern. Sie können diese Richtlinien so konfigurieren, dass vertrauliche Informationstypen wie PII, finanzielle oder Integritäts-IDs identifiziert werden, oder Sie verwenden Stichwörter, um den Schutz zu verbessern. Nachdem Sie die Richtlinien konfiguriert haben, Paaren Sie Richtlinien mit einer benutzerdefinierten e-Mail-Vorlage und fügen dann ein Ablaufdatum für zusätzliche Steuerelemente für e-Mails hinzu, die der Richtlinie entsprechen. Darüber hinaus können Administratoren verschlüsselte e-Mails, auf die extern über ein sicheres Webportal zugegriffen wird, weiter steuern, indem Sie den Zugriff auf die e-Mails jederzeit widerrufen.

Sie können nur einen Ablauf für und widerrufen von e-Mails festlegen, die an externe Empfänger gesendet werden.

Mit der erweiterten Nachrichtenverschlüsselung von Office 365 wendet das Office 365 jedes Mal, wenn Sie ein benutzerdefiniertes Branding anwenden, den Wrapper auf e-Mails an, die der Nachrichtenfluss Regel entsprechen, auf die Sie die Vorlage anwenden. Außerdem kann das Ablaufdatum nur verwendet werden, wenn benutzerdefiniertes Branding verwendet wird. Sie können nur Nachrichten widerrufen, die über das Portal empfangen werden.

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Erste Schritte mit Office 365 erweiterte Nachrichtenverschlüsselung

In den folgenden Themen wird beschrieben, wie Sie erweiterte Nachrichtenverschlüsselung einrichten und verwenden.

Ihre Organisation muss über ein Abonnement verfügen, das die erweiterte Nachrichtenverschlüsselung von Office 365 enthält. Ausführliche Informationen zu unterstützten Abonnements finden Sie in der [Nachrichten Richtlinie und im Compliance-Dienst](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).

Richten Sie die neuen Office 365-Nachrichten Verschlüsselungsfunktionen ein, wenn Sie noch nicht für die Nutzung erweiterter Nachrichten Verschlüsselungsfunktionen eingerichtet sind, die zusätzlich zu verschlüsselten Nachrichten, die extern freigegeben werden, zusätzlichen Schutz bieten. Wenn Sie keine Office 365-Nachrichtenverschlüsselung eingerichtet haben, finden Sie weitere Informationen unter [Einrichten neuer office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).

[Legen Sie ein Ablaufdatum für e-Mail-Verschlüsseln von Office 365 Advanced Message Encryption fest](ome-advanced-expiration.md). Steuern Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, mit automatischen Richtlinien, die den Schutz erhöhen, indem Sie den Zugriff über ein sicheres Webportal zu verschlüsselten e-Mails verlaufen

[Widerrufen von e-Mails, die von Office 365 verschlüsselt wurden erweiterte Nachrichtenverschlüsselung](revoke-ome-encrypted-mail.md). Steuern Sie vertrauliche e-Mails, die außerhalb der Organisation freigegeben werden, und erhöhen Sie den Schutz, indem Sie den Zugriff über ein sicheres Webportal zu verschlüsselten e-Mails widerrufen.  
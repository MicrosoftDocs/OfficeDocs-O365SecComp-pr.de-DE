---
title: Festlegen eines Ablaufdatums für e-Mail, die von Office 365 verschlüsselt wurde erweiterte Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Mit Office 365 erweiterte Nachrichten Verschlüsselungsfunktionen am Anfang der Office 365-Nachrichtenverschlüsselung (OM) können Sie Ihre e-Mail-Sicherheit erweitern, indem Sie ein Ablaufdatum für e-Mails über eine benutzerdefinierte Marken Vorlage festlegen.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506718"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a>Festlegen eines Ablaufdatums für e-Mail, die von Office 365 verschlüsselt wurde erweiterte Nachrichtenverschlüsselung

Office 365 erweiterte Nachrichtenverschlüsselung steht über die Office 365-Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung. Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht die erweiterte Nachrichtenverschlüsselung von Office 365 enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Konformität der Advanced Compliance-SKU erwerben.

Sie können den Nachrichtenablauf für e-Mails verwenden, die Ihre Benutzer an externe Empfänger senden, die das OM-Portal verwenden, um auf verschlüsselte e-Mails zuzugreifen. Sie erzwingen, dass die Empfänger das OM-Portal verwenden, um verschlüsselte e-Mails anzuzeigen und zu beantworten, die von Ihrer Organisation mithilfe einer benutzerdefinierten Branding-Vorlage gesendet wurden, die ein Ablaufdatum in Windows PowerShell angibt.

Wenn Sie als globaler O365-Administrator Ihr Unternehmensbranding anwenden, um das Erscheinungsbild der e-Mail-Nachrichten Ihrer Office 365-Organisation anzupassen, können Sie auch ein Ablaufdatum für diese e-Mail-Nachrichten angeben. Mit der erweiterten Nachrichtenverschlüsselung von Office 365 können Sie mehrere Vorlagen für verschlüsselte e-Mails aus Ihrer Organisation erstellen. Mithilfe einer Vorlage können Sie steuern, wie lange Empfänger auf e-Mails zugreifen, die von Ihren Benutzern gesendet werden.

Wenn ein Endbenutzer e-Mails mit einem Ablaufdatum erhält, sieht der Benutzer das Ablaufdatum in der Wrapper-e-Mail. Wenn ein Benutzer versucht, eine abgelaufene e-Mail zu öffnen, wird im OM-Portal ein Fehler angezeigt.

Nur e-Mails an externe Empfänger sind abgelaufen.

Mit der erweiterten Nachrichtenverschlüsselung von Office 365 wendet das Office 365 jedes Mal, wenn Sie ein benutzerdefiniertes Branding anwenden, den Wrapper auf e-Mails an, die der Nachrichtenfluss Regel entsprechen, auf die Sie die Vorlage anwenden. Außerdem kann das Ablaufdatum nur verwendet werden, wenn benutzerdefiniertes Branding verwendet wird.

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a>Erstellen einer benutzerdefinierten Branding-Vorlage zum Erzwingen des Ablaufs von e-Mails mithilfe von PowerShell

1. Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.

2. Führen Sie das Cmdlet New-OMEConfiguration aus.

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

Wobei Folgendes gilt:

- Identity ist der Name der benutzerdefinierten Vorlage.

- ExternalMailExpiryInDays gibt an, wie viele Tage e-Mails von Empfängern aufbewahrt werden sollen, bevor Sie ablaufen. Sie können einen beliebigen Wert zwischen 1 und 730 Tage verwenden.

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Weitere Informationen zu Office 365 erweiterte Nachrichtenverschlüsselung

- [Office 365 erweiterte Nachrichtenverschlüsselung](ome-advanced-message-encryption.md)

- [Widerrufen von e-Mails, die von Office 365 verschlüsselt wurden erweiterte Nachrichtenverschlüsselung](revoke-ome-encrypted-mail.md)

- [Beschreibung des Nachrichtenrichtlinien-und Konformitäts Diensts](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
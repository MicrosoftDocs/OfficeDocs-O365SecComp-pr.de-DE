---
title: Widerrufen von E-Mails, die von der Office 365-Nachrichtenverschlüsselung verschlüsselt wurden
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/29/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Als Office 365-Administrator können Sie bestimmte-e-Mails widerrufen, die mit Office 365-Nachrichtenverschlüsselung verschlüsselt wurden.
ms.openlocfilehash: a3f5c08d2c8660e56c378fc5fa7a850ff2c12eb5
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614389"
---
# <a name="office-365-message-encryption-email-revocation"></a>Office 365 Message Encryption e-Mail-Sperrung

Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur [Office 365 Message Encryption](ome.md). Moment, verschlüsselte e-Mail-Sperrung ist in der Vorschau. Erwarten Sie Updates und Änderungen an das Feature und die Inhalte, wie wir weiter unser Angebot zu verbessern.

Möglicherweise ist es erforderlich sind, um eine e-Mail zu sperren, die bereits gesendet wurde. Wenn die e-Mail-Nachricht wurde mit Office 365-Nachrichtenverschlüsselung verschlüsselt, und Sie ein Office 365-Administrator sind, können Sie diese e-Mail unter bestimmten Umständen Schritte durchführen. In diesem Artikel wird beschrieben, unter welchen Umständen dies möglich ist und wie es.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Verschlüsselte e-Mails, die Sie sperren können

Sie können verschlüsselte e-Mails sperren, wenn der Empfänger ein Link-basierte Branding verschlüsselten e-Mail erhalten. Wenn der Empfänger eine systemeigene Inline-Erfahrung in einen unterstützten Outlook-Client erhalten, und klicken Sie dann diese e-Mails nicht gesperrt werden können.

Ob ein Empfänger ein Link-basierte Erlebnis erhält oder eine Inline wünschen hängt von dem Empfänger Identitätstyp: Office 365 und Microsoft Account Empfänger (beispielsweise outlook.com Benutzer) erhalten eine Inline wünschen in unterstützten Outlook-Clients. Alle anderen Empfängertypen wie Google Mail-Empfänger, rufen Sie ein Link-basierte wünschen.

In Kürze müssen Organisationen, eine Link-basierte Erfahrung unabhängig von der Empfänger Identität zu erzwingen. Auf diese Weise alle Empfänger eine e-Mail mit Branding mit einem Link zu Office 365 Message Encryption-Portal erhalten, in dem sie werden können lesen und Beantworten von verschlüsselten e-Mail-Nachrichten. Alle solchen verschlüsselte e-Mails werden widerrufbare.
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Empfänger Erfahrung für widerrufenen verschlüsselte e-Mails

Nachdem eine e-Mail-Nachricht gesperrt wurde, erhalten der Empfänger eine Fehlermeldung beim Versuch, die verschlüsselte e-Mail über das Office 365 Message Encryption Portal zugreifen: "die Nachricht wurde vom Absender gesperrt".

![Screenshot, der einen widerrufenen verschlüsselte e-Mails anzeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>Wie Sie eine verschlüsselte e-Mail widerrufen

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Schritt 1. Die Nachrichten-ID der e-Mail erhalten

Vor dem Sperren Sie eine verschlüsselte e-Mail-Nachrichten müssen Sie die Nachrichten-ID, die e-Mail zu erfassen. Die MessageId hat normalerweise das Format:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Es gibt mehrere Methoden, die Nachrichten-ID der e-Mail erhalten, die Sie sperren möchten. In diesem Abschnitt werden einige Optionen, aber Sie können jede Methode, die die ID bietet verwenden

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>Die Nachrichten-ID der e-Mail identifizieren Sie mithilfe von Message Trace in das Wertpapier widerrufen möchten &amp; Compliance Center

1. Suchen Sie nach der e-Mail vom Absender oder Empfänger über [Neue Message Trace in Office 365-Sicherheit & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).
2. Wenn Sie gefunden haben die e-Mail-Nachricht wählen Sie sie aus, um die **Nachricht Trace** Detailbereich aufzurufen. Erweitern Sie **Weitere Informationen** zum Suchen der Nachricht-ID.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>Die Nachrichten-ID der e-Mail identifizieren Sie mithilfe von Office Message Encryption Berichte in das Wertpapier widerrufen möchten &amp; Compliance Center

1. In das Wertpapier &amp; Compliance Center, navigieren Sie zu der **Nachrichtenverschlüsselung Bericht**.
2. Wählen Sie die Tabelle **Details anzeigen** , und identifizieren Sie die Nachricht, die Sie sperren möchten.
3. Doppelklicken Sie auf die Nachricht zum Anzeigen von Details, die die Nachricht-ID enthalten

### <a name="step-2-revoke-the-mail"></a>Schritt 2. Die e-Mail-Nachricht widerrufen  

Wenn Sie die e-Mail-Nachrichten-ID, den, die Sie aufheben möchten kennen, können Sie die e-Mail-Nachricht mit dem Cmdlet Set-OMEMessageRevocation widerrufen.

1. [Verbindung mit Exchange Online mit Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

2. Führen Sie das Cmdlet Set-OMEMessageRevocation wie folgt aus:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. Um zu überprüfen, ob die e-Mail-Nachricht gesperrt wurde, führen Sie das Cmdlet Get-OMEMessageStatus wie folgt aus:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | fl Revoked
    ```  
    Wenn OCSP erfolgreich war, gibt das Cmdlet das folgende Ergebnis zurück:  

    `Revoked: True`

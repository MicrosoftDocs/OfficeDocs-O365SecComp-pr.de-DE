---
title: Widerrufen von E-Mails, die von der erweiterten Office 365-Nachrichtenverschlüsselung verschlüsselt wurden
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Als Office 365 Administrator können Sie bestimmte e-Mails widerrufen, die mit Office 365 erweiterter Nachrichtenverschlüsselung verschlüsselt wurden.
ms.openlocfilehash: 098ce50791152c8bbb4e4692d6fb85e4c2c7cb58
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156787"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a>Widerrufen von E-Mails, die von der erweiterten Office 365-Nachrichtenverschlüsselung verschlüsselt wurden

Die e-Mail-Sperrung wird im Rahmen Office 365 erweiterten Nachrichtenverschlüsselung angeboten. Office 365 erweiterte Nachrichtenverschlüsselung steht über Office 365 Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung. Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten. Wenn Ihre Organisation über ein Office 365es Abonnement verfügt, das nicht Office 365 erweiterte Nachrichtenverschlüsselung enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Kompatibilität der Advanced Compliance-SKU erwerben.

Dieser Artikel ist Teil einer größeren Reihe von Artikeln über [Office 365 Nachrichtenverschlüsselung](ome.md).

Möglicherweise ist es erforderlich, eine e-Mail zu widerrufen, die bereits gesendet wurde. Wenn die e-Mail mit Office 365 erweiterten Nachrichtenverschlüsselung verschlüsselt wurde und Sie ein Office 365 Administrator sind, können Sie dies unter bestimmten Bedingungen für e-Mails tun. In diesem Artikel wird beschrieben, unter welchen Umständen und wie dies möglich ist.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Verschlüsselte e-Mails, die Sie widerrufen können

Sie können verschlüsselte e-Mails widerrufen, wenn der Empfänger eine Linkbasierte, eingebrannte verschlüsselte e-Mail erhalten hat. Wenn der Empfänger eine systemeigene Inline Erfahrung in einem unterstützten Outlook-Client empfangen hat, können diese e-Mails nicht widerrufen werden.

Ob ein Empfänger eine Linkbasierte Erfahrung oder eine Inline-Erfahrung erhält, hängt vom Typ der Empfänger Identität ab: Office 365-und Microsoft-Konto Empfänger (beispielsweise Outlook.com-Benutzer) erhalten eine Inline-Erfahrung in unterstützten Outlook-Clients. Alle anderen Empfängertypen, wie etwa Gmail-Empfänger, erhalten eine Linkbasierte Benutzeroberfläche.

## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Empfänger Erfahrung für gesperrte verschlüsselte e-Mails

Sobald eine e-Mail widerrufen wurde, erhält der Empfänger eine Fehlermeldung, wenn er versucht, über das Office 365 Nachrichten Verschlüsselungs Portal auf die verschlüsselte e-Mail zuzugreifen: "die Nachricht wurde vom Absender widerrufen".

![Screenshot, der eine widerrufene verschlüsselte e-Mail zeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>Vorgehensweise widerrufen einer verschlüsselten e-Mail

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Schritt 1: Abrufen der Nachrichten-ID der e-Mail

Bevor Sie eine verschlüsselte e-Mail widerrufen können, müssen Sie die Nachrichten-ID der e-Mail erfassen. Die MessageId weist normalerweise das folgende Format auf:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Es gibt mehrere Möglichkeiten, die Nachrichten-ID der e-Mail zu finden, die Sie widerrufen möchten. In diesem Abschnitt werden einige Optionen beschrieben, aber Sie können eine beliebige Methode verwenden, die die ID bereitstellt.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>So identifizieren Sie die Nachrichten-ID der e-Mail, die Sie mithilfe der Nachrichtenablaufverfolgung im Security &amp; Compliance Center widerrufen möchten

1. Suchen Sie nach der e-Mail nach Absender oder Empfänger mithilfe der [neuen Nachrichtenablaufverfolgung im Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).

2. Nachdem Sie die e-Mail-Adresse gefunden haben, wählen Sie Sie aus, um den Bereich **Nachrichtenablauf Verfolgungs Details** aufzurufen. Erweitern Sie **Weitere Informationen** , um nach der Nachrichten-ID zu suchen.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>So identifizieren Sie die Nachrichten-ID der e-Mail, die Sie mithilfe von Office-Nachrichten Verschlüsselungs Berichten im &amp; Security Compliance Center widerrufen möchten

1. Navigieren Sie im &amp; Security Compliance Center zum **Nachrichten Verschlüsselungs Bericht**.

2. Wählen Sie die Tabelle **Details anzeigen** aus, und identifizieren Sie die Nachricht, die Sie widerrufen möchten.

3. Doppelklicken Sie auf die Nachricht, um Details anzuzeigen, die die Nachrichten-ID enthalten.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>Schritt 2: Sicherstellen, dass die e-Mail widerruflich ist

Um zu überprüfen, ob Sie eine bestimmte e-Mail-Nachricht widerrufen können, überprüfen Sie, **** ob das Feld Sperr Status &amp; in der Tabelle Details im Security Compliance Center angezeigt wird.

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Sie eine bestimmte e-Mail-Nachricht mithilfe von Windows PowerShell widerrufen können.

1. Verwenden Sie ein Arbeits-oder Schulkonto, das über globale Administratorberechtigungen in Ihrer Office 365 Organisation verfügt, starten Sie eine Windows PowerShell Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet "OMEMessageStatus" wie folgt aus:

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   Gibt den Betreff der Nachricht zurück und gibt an, ob die Nachricht widerruflich ist. For example,

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a>Schritt 3: E-Mail widerrufen  

Sobald Sie die Nachrichten-ID der e-Mail kennen, die Sie widerrufen möchten, und Sie sichergestellt haben, dass die Nachricht widerruflich ist, können Sie die e-Mail widerrufen.

Um die e-Mail im Security &amp; Compliance Center zu widerrufen, wählen Sie in der Tabelle **Details** die Option **widerrufen**aus.

Sie können eine e-Mail mithilfe von Windows PowerShell widerrufen, indem Sie das Cmdlet "OMEMessageRevocation" verwenden.

1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet "OMEMessageRevocation" wie folgt aus:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. Um zu überprüfen, ob die e-Mail widerrufen wurde, führen Sie das Get-OMEMessageStatus-Cmdlet wie folgt aus:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    Wenn die Sperrung erfolgreich war, gibt das Cmdlet das folgende Ergebnis zurück:  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Weitere Informationen zu Office 365 erweiterte Nachrichtenverschlüsselung

- [Erweiterte Office 365-Nachrichtenverschlüsselung](ome-advanced-message-encryption.md)

- [Office 365 erweiterte Nachrichtenverschlüsselung – e-Mail-Ablauf](ome-advanced-expiration.md)

- [Beschreibung des Nachrichtenrichtlinien-und Kompatibilitätsdiensts](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
---
title: Widerrufen von E-Mails, die von der Office 365-Nachrichtenverschlüsselung verschlüsselt wurden
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Als Office 365-Administrator können Sie bestimmte e-Mails, die mit der Office 365-Nachrichtenverschlüsselung verschlüsselt wurden, widerrufen.
ms.openlocfilehash: 75b5e46e25f447ddac0de5a7911d0df8385da6b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214895"
---
# <a name="office-365-message-encryption-email-revocation"></a>E-Mail-Sperrung für Office 365-Nachrichtenverschlüsselung

Dieser Artikel ist Teil einer größeren Artikelreihe zur [Nachrichtenverschlüsselung von Office 365](ome.md). Im Moment befindet sich die verschlüsselte e-Mail-Sperrung in der Vorschau. Erwarten Sie Updates und Änderungen an der Funktion und den Inhalten, während wir unser Angebot weiter verbessern.

Möglicherweise ist es erforderlich, eine bereits gesendete e-Mail zu widerrufen. Wenn die e-Mail mit der Office 365-Nachrichtenverschlüsselung verschlüsselt wurde und Sie ein Office 365-Administrator sind, können Sie dies unter bestimmten Umständen für e-Mails tun. In diesem Artikel wird beschrieben, unter welchen Umständen dies möglich und wie es geht.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>VerSchlüsselte e-Mails, die Sie widerrufen können

Sie können verschlüsselte e-Mails widerrufen, wenn der Empfänger eine verschlüsselte e-Mail-Nachricht auf linkbasis erhalten hat. Wenn der Empfänger eine native Inline-Erfahrung in einem unterstützten Outlook-Client erhalten hat, können diese e-Mails nicht widerrufen werden.

Ob ein Empfänger eine Linkbasierte Erfahrung oder eine Inline Erfahrung erhält, hängt vom Empfänger Identitätstyp ab: Office 365-und Microsoft-Konto Empfänger (beispielsweise outlook.com-Benutzer) erhalten eine Inline Erfahrung in unterstützten Outlook-Clients. Alle anderen Empfängertypen, wie etwa Gmail-Empfänger, erhalten eine Linkbasierte Benutzeroberfläche.

In Kürze können Organisationen unabhängig von der Empfänger Identität eine Linkbasierte Benutzeroberfläche erzwingen. Auf diese Weise erhalten alle Empfänger eine Branded-e-Mail mit einem Link zum Office 365-Nachrichten Verschlüsselungs Portal, in dem Sie verschlüsselte e-Mails lesen und beantworten können. Alle diese verschlüsselten e-Mails sind widerruflich.
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Empfänger Erfahrung für gesperrte verschlüsselte e-Mails

Sobald eine e-Mail gesperrt wurde, erhält der Empfänger beim Versuch, über das Office 365-Nachrichten Verschlüsselungs Portal auf die verschlüsselten e-Mails zuzugreifen, eine Fehlermeldung: "die Nachricht wurde vom Absender widerrufen."

![Screenshot, der eine gesperrte verschlüsselte e-Mail anzeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>So widerrufen Sie eine verschlüsselte e-Mail

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Schritt 1. Abrufen der Nachrichten-ID der e-Mail

Bevor Sie eine verschlüsselte e-Mail widerrufen können, müssen Sie die Nachrichten-ID der e-Mail sammeln. Die MessageId hat normalerweise das folgende Format:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Es gibt mehrere Möglichkeiten, die Nachrichten-ID der e-Mail zu finden, die Sie widerrufen möchten. In diesem Abschnitt werden einige Optionen beschrieben, aber Sie können eine beliebige Methode verwenden, die die ID bereitstellt.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>So identifizieren Sie die nachRichten-ID der e-Mail, die Sie mithilfe der Nachrichtenablaufverfolgung im &amp; Security Compliance Center widerrufen möchten

1. Suchen Sie nach der e-Mail nach Absender oder Empfänger mithilfe der [neuen Nachrichtenablaufverfolgung im Office 365 Security _AMP_ Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).
2. Nachdem Sie die e-Mail gefunden haben, wählen Sie Sie aus, um den Bereich **Nachrichtenablauf Verfolgungs Details** anzuzeigen. Erweitern Sie **Weitere Informationen** , um nach der Nachrichten-ID zu suchen.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>So identifizieren Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, mithilfe von Office- &amp; Nachrichten Verschlüsselungs Berichten im Security Compliance Center

1. Navigieren Sie im &amp; Security Compliance Center zum Bericht zur **Nachrichtenverschlüsselung**.
2. Wählen Sie die Tabelle **Details anzeigen** aus, und identifizieren Sie die Nachricht, die Sie widerrufen möchten.
3. Doppelklicken Sie auf die Nachricht, um Details anzuzeigen, die die nachRichten-ID aufweisen.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>Schritt 2. Überprüfen, ob die e-Mail widerruflich ist

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob eine bestimmte e-Mail-Nachricht widerrufen werden kann.

1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-OMEMessageStatus wie folgt aus:
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   Dieser gibt den Betreff der Nachricht zurück und gibt an, ob die Nachricht widerruflich ist. Zum Beispiel

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a>Schritt 3. Widerrufen der e-Mail  

Nachdem Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, kennen und sichergestellt haben, dass die Nachricht widerruflich ist, können Sie die e-Mail mithilfe des Cmdlets Set-OMEMessageRevocation widerrufen.

1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-OMEMessageRevocation wie folgt aus:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. Führen Sie das Cmdlet Get-OMEMessageStatus wie folgt aus, um zu überprüfen, ob die e-Mail widerrufen wurde:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    Wenn die Sperrung erfolgreich war, gibt das Cmdlet folgendes Ergebnis zurück:  

    `Revoked: True`

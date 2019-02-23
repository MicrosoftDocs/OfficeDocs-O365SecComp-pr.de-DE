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
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="9e23c-103">E-Mail-Sperrung für Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="9e23c-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="9e23c-p101">Dieser Artikel ist Teil einer größeren Artikelreihe zur [Nachrichtenverschlüsselung von Office 365](ome.md). Im Moment befindet sich die verschlüsselte e-Mail-Sperrung in der Vorschau. Erwarten Sie Updates und Änderungen an der Funktion und den Inhalten, während wir unser Angebot weiter verbessern.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="9e23c-p102">Möglicherweise ist es erforderlich, eine bereits gesendete e-Mail zu widerrufen. Wenn die e-Mail mit der Office 365-Nachrichtenverschlüsselung verschlüsselt wurde und Sie ein Office 365-Administrator sind, können Sie dies unter bestimmten Umständen für e-Mails tun. In diesem Artikel wird beschrieben, unter welchen Umständen dies möglich und wie es geht.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="9e23c-110">VerSchlüsselte e-Mails, die Sie widerrufen können</span><span class="sxs-lookup"><span data-stu-id="9e23c-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="9e23c-p103">Sie können verschlüsselte e-Mails widerrufen, wenn der Empfänger eine verschlüsselte e-Mail-Nachricht auf linkbasis erhalten hat. Wenn der Empfänger eine native Inline-Erfahrung in einem unterstützten Outlook-Client erhalten hat, können diese e-Mails nicht widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="9e23c-p104">Ob ein Empfänger eine Linkbasierte Erfahrung oder eine Inline Erfahrung erhält, hängt vom Empfänger Identitätstyp ab: Office 365-und Microsoft-Konto Empfänger (beispielsweise outlook.com-Benutzer) erhalten eine Inline Erfahrung in unterstützten Outlook-Clients. Alle anderen Empfängertypen, wie etwa Gmail-Empfänger, erhalten eine Linkbasierte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="9e23c-p105">In Kürze können Organisationen unabhängig von der Empfänger Identität eine Linkbasierte Benutzeroberfläche erzwingen. Auf diese Weise erhalten alle Empfänger eine Branded-e-Mail mit einem Link zum Office 365-Nachrichten Verschlüsselungs Portal, in dem Sie verschlüsselte e-Mails lesen und beantworten können. Alle diese verschlüsselten e-Mails sind widerruflich.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="9e23c-118">Empfänger Erfahrung für gesperrte verschlüsselte e-Mails</span><span class="sxs-lookup"><span data-stu-id="9e23c-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="9e23c-119">Sobald eine e-Mail gesperrt wurde, erhält der Empfänger beim Versuch, über das Office 365-Nachrichten Verschlüsselungs Portal auf die verschlüsselten e-Mails zuzugreifen, eine Fehlermeldung: "die Nachricht wurde vom Absender widerrufen."</span><span class="sxs-lookup"><span data-stu-id="9e23c-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Screenshot, der eine gesperrte verschlüsselte e-Mail anzeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="9e23c-121">So widerrufen Sie eine verschlüsselte e-Mail</span><span class="sxs-lookup"><span data-stu-id="9e23c-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="9e23c-p106">Schritt 1. Abrufen der Nachrichten-ID der e-Mail</span><span class="sxs-lookup"><span data-stu-id="9e23c-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="9e23c-p107">Bevor Sie eine verschlüsselte e-Mail widerrufen können, müssen Sie die Nachrichten-ID der e-Mail sammeln. Die MessageId hat normalerweise das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9e23c-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="9e23c-p108">Es gibt mehrere Möglichkeiten, die Nachrichten-ID der e-Mail zu finden, die Sie widerrufen möchten. In diesem Abschnitt werden einige Optionen beschrieben, aber Sie können eine beliebige Methode verwenden, die die ID bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="9e23c-128">So identifizieren Sie die nachRichten-ID der e-Mail, die Sie mithilfe der Nachrichtenablaufverfolgung im &amp; Security Compliance Center widerrufen möchten</span><span class="sxs-lookup"><span data-stu-id="9e23c-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="9e23c-129">Suchen Sie nach der e-Mail nach Absender oder Empfänger mithilfe der [neuen Nachrichtenablaufverfolgung im Office 365 Security _AMP_ Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="9e23c-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="9e23c-p109">Nachdem Sie die e-Mail gefunden haben, wählen Sie Sie aus, um den Bereich **Nachrichtenablauf Verfolgungs Details** anzuzeigen. Erweitern Sie **Weitere Informationen** , um nach der Nachrichten-ID zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9e23c-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="9e23c-132">So identifizieren Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, mithilfe von Office- &amp; Nachrichten Verschlüsselungs Berichten im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="9e23c-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="9e23c-133">Navigieren Sie im &amp; Security Compliance Center zum Bericht zur **Nachrichtenverschlüsselung**.</span><span class="sxs-lookup"><span data-stu-id="9e23c-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="9e23c-134">Wählen Sie die Tabelle **Details anzeigen** aus, und identifizieren Sie die Nachricht, die Sie widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9e23c-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="9e23c-135">Doppelklicken Sie auf die Nachricht, um Details anzuzeigen, die die nachRichten-ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9e23c-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="9e23c-p110">Schritt 2. Überprüfen, ob die e-Mail widerruflich ist</span><span class="sxs-lookup"><span data-stu-id="9e23c-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="9e23c-138">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob eine bestimmte e-Mail-Nachricht widerrufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e23c-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="9e23c-p111">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="9e23c-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="9e23c-141">Führen Sie das Cmdlet Set-OMEMessageStatus wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9e23c-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="9e23c-p112">Dieser gibt den Betreff der Nachricht zurück und gibt an, ob die Nachricht widerruflich ist. Zum Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e23c-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="9e23c-p113">Schritt 3. Widerrufen der e-Mail</span><span class="sxs-lookup"><span data-stu-id="9e23c-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="9e23c-146">Nachdem Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, kennen und sichergestellt haben, dass die Nachricht widerruflich ist, können Sie die e-Mail mithilfe des Cmdlets Set-OMEMessageRevocation widerrufen.</span><span class="sxs-lookup"><span data-stu-id="9e23c-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="9e23c-147">[Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="9e23c-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="9e23c-148">Führen Sie das Cmdlet Set-OMEMessageRevocation wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9e23c-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="9e23c-149">Führen Sie das Cmdlet Get-OMEMessageStatus wie folgt aus, um zu überprüfen, ob die e-Mail widerrufen wurde:</span><span class="sxs-lookup"><span data-stu-id="9e23c-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="9e23c-150">Wenn die Sperrung erfolgreich war, gibt das Cmdlet folgendes Ergebnis zurück:</span><span class="sxs-lookup"><span data-stu-id="9e23c-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`

---
title: Widerrufen Sie e-Mail von Office 365-Nachrichtenverschlüsselung verschlüsselt
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Als Office 365-Administrator können Sie bestimmte-e-Mails widerrufen, die mit Office 365-Nachrichtenverschlüsselung verschlüsselt wurden.
ms.openlocfilehash: 19eb874fa15a21c29a9eb2823829e81ff244a555
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2018
ms.locfileid: "25011821"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="618d6-103">Office 365 Message Encryption e-Mail-Sperrung</span><span class="sxs-lookup"><span data-stu-id="618d6-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="618d6-p101">Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur [Office 365 Message Encryption](ome.md). Moment, verschlüsselte e-Mail-Sperrung ist in der Vorschau. Erwarten Sie Updates und Änderungen an das Feature und die Inhalte, wie wir weiter unser Angebot zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="618d6-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="618d6-p102">Möglicherweise ist es erforderlich sind, um eine e-Mail zu sperren, die bereits gesendet wurde. Wenn die e-Mail-Nachricht wurde mit Office 365-Nachrichtenverschlüsselung verschlüsselt, und Sie ein Office 365-Administrator sind, können Sie diese e-Mail unter bestimmten Umständen Schritte durchführen. In diesem Artikel wird beschrieben, unter welchen Umständen dies möglich ist und wie es.</span><span class="sxs-lookup"><span data-stu-id="618d6-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="618d6-110">Verschlüsselte e-Mails, die Sie sperren können</span><span class="sxs-lookup"><span data-stu-id="618d6-110">Encrypted emails that you can revoke</span></span>
<span data-ttu-id="618d6-p103">Sie können verschlüsselte e-Mails sperren, wenn der Empfänger ein Link-basierte Branding verschlüsselten e-Mail erhalten. Wenn der Empfänger eine systemeigene Inline-Erfahrung in einen unterstützten Outlook-Client erhalten, und klicken Sie dann diese e-Mails nicht gesperrt werden können.</span><span class="sxs-lookup"><span data-stu-id="618d6-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="618d6-113">Ob ein Empfänger ein Link-basierte Erlebnis erhält oder eine Inline wünschen hängt von dem Empfänger Identitätstyp: Office 365 und Microsoft Account Empfänger (beispielsweise outlook.com Benutzer) erhalten eine Inline wünschen in unterstützten Outlook-Clients.</span><span class="sxs-lookup"><span data-stu-id="618d6-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span>  
<span data-ttu-id="618d6-114">Alle anderen Empfängertypen wie Google Mail-Empfänger, rufen Sie ein Link-basierte wünschen.</span><span class="sxs-lookup"><span data-stu-id="618d6-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span> 

<span data-ttu-id="618d6-p104">In Kürze müssen Organisationen, eine Link-basierte Erfahrung unabhängig von der Empfänger Identität zu erzwingen. Auf diese Weise alle Empfänger eine e-Mail mit Branding mit einem Link zu Office 365 Message Encryption-Portal erhalten, in dem sie werden können lesen und Beantworten von verschlüsselten e-Mail-Nachrichten. Alle solchen verschlüsselte e-Mails werden widerrufbare.</span><span class="sxs-lookup"><span data-stu-id="618d6-p104">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span> 
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="618d6-118">Empfänger Erfahrung für widerrufenen verschlüsselte e-Mails</span><span class="sxs-lookup"><span data-stu-id="618d6-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="618d6-119">Nachdem eine e-Mail-Nachricht gesperrt wurde, erhalten der Empfänger eine Fehlermeldung beim Versuch, die verschlüsselte e-Mail über das Office 365 Message Encryption Portal zugreifen: "die Nachricht wurde vom Absender gesperrt".</span><span class="sxs-lookup"><span data-stu-id="618d6-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Screenshot, der einen widerrufenen verschlüsselte e-Mails anzeigt.](media/revoked-encrypted-email.png)
    
## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="618d6-121">Wie Sie eine verschlüsselte e-Mail widerrufen</span><span class="sxs-lookup"><span data-stu-id="618d6-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="618d6-p105">Schritt 1. Die Nachrichten-ID der e-Mail erhalten</span><span class="sxs-lookup"><span data-stu-id="618d6-p105">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="618d6-p106">Vor dem Sperren Sie eine verschlüsselte e-Mail-Nachrichten müssen Sie die Nachrichten-ID, die e-Mail zu erfassen. Die MessageId hat normalerweise das Format:</span><span class="sxs-lookup"><span data-stu-id="618d6-p106">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="618d6-p107">Es gibt mehrere Methoden, die Nachrichten-ID der e-Mail erhalten, die Sie sperren möchten. In diesem Abschnitt werden einige Optionen, aber Sie können jede Methode, die die ID bietet verwenden</span><span class="sxs-lookup"><span data-stu-id="618d6-p107">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="618d6-128">Die Nachrichten-ID der e-Mail identifizieren Sie mithilfe von Message Trace in das Wertpapier widerrufen möchten &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="618d6-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="618d6-129">Suchen Sie nach der e-Mail vom Absender oder Empfänger über [Neue Message Trace in Office 365-Sicherheit und Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="618d6-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="618d6-p108">Wenn Sie gefunden haben die e-Mail-Nachricht wählen Sie sie aus, um die **Nachricht Trace** Detailbereich aufzurufen. Erweitern Sie **Weitere Informationen** zum Suchen der Nachricht-ID.</span><span class="sxs-lookup"><span data-stu-id="618d6-p108">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

  #### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="618d6-132">Die Nachrichten-ID der e-Mail identifizieren Sie mithilfe von Office Message Encryption Berichte in das Wertpapier widerrufen möchten &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="618d6-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>
1. <span data-ttu-id="618d6-133">In das Wertpapier &amp; Compliance Center, navigieren Sie zu der **Nachrichtenverschlüsselung Bericht**.</span><span class="sxs-lookup"><span data-stu-id="618d6-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="618d6-134">Wählen Sie die Tabelle **Details anzeigen** , und identifizieren Sie die Nachricht, die Sie sperren möchten.</span><span class="sxs-lookup"><span data-stu-id="618d6-134">Choose the **View details** table and identify the message that you want to revoke.</span></span> 
3. <span data-ttu-id="618d6-135">Doppelklicken Sie auf die Nachricht zum Anzeigen von Details, die die Nachricht-ID enthalten</span><span class="sxs-lookup"><span data-stu-id="618d6-135">Double-click the message to view details that include the Message ID.</span></span> 

### <a name="step-2-revoke-the-mail"></a><span data-ttu-id="618d6-p109">Schritt 2. Die e-Mail-Nachricht widerrufen</span><span class="sxs-lookup"><span data-stu-id="618d6-p109">Step 2. Revoke the mail</span></span>  

<span data-ttu-id="618d6-138">Wenn Sie die e-Mail-Nachrichten-ID, den, die Sie aufheben möchten kennen, können Sie die e-Mail-Nachricht mit dem Cmdlet Set-OMEMessageRevocation widerrufen.</span><span class="sxs-lookup"><span data-stu-id="618d6-138">Once you know the Message ID of the email you want to revoke, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span> 

1. <span data-ttu-id="618d6-139">[Verbindung mit Exchange Online mit Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="618d6-139">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="618d6-140">Führen Sie das Cmdlet Set-OMEMessageRevocation wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="618d6-140">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>
    
    ```
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. <span data-ttu-id="618d6-141">Um zu überprüfen, ob die e-Mail-Nachricht gesperrt wurde, führen Sie das Cmdlet Get-OMEMessageStatus wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="618d6-141">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>
    
    ```
    Get-OMEMessageStatus -MessageId "<messageId>"
    ```  
    <span data-ttu-id="618d6-142">Wenn OCSP erfolgreich war, gibt das Cmdlet das folgende Ergebnis zurück:</span><span class="sxs-lookup"><span data-stu-id="618d6-142">If revocation was successful, the cmdlet returns the following result:</span></span>  

    ```The encrypted email with the subject "<subject>" and Message ID "<messageId>" was successfully revoked.```

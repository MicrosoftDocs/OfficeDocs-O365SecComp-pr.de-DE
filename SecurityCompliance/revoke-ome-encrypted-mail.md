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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264822"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="be345-103">E-Mail-Sperrung für Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="be345-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="be345-104">Dieser Artikel ist Teil einer größeren Artikelreihe zur [Nachrichtenverschlüsselung von Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="be345-104">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span> <span data-ttu-id="be345-105">Im Moment befindet sich die verschlüsselte e-Mail-Sperrung in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="be345-105">Right now, encrypted email revocation is in preview.</span></span> <span data-ttu-id="be345-106">Erwarten Sie Updates und Änderungen an der Funktion und den Inhalten, während wir unser Angebot weiter verbessern.</span><span class="sxs-lookup"><span data-stu-id="be345-106">Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="be345-107">Möglicherweise ist es erforderlich, eine bereits gesendete e-Mail zu widerrufen.</span><span class="sxs-lookup"><span data-stu-id="be345-107">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="be345-108">Wenn die e-Mail mit der Office 365-Nachrichtenverschlüsselung verschlüsselt wurde und Sie ein Office 365-Administrator sind, können Sie dies unter bestimmten Umständen für e-Mails tun.</span><span class="sxs-lookup"><span data-stu-id="be345-108">If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="be345-109">In diesem Artikel wird beschrieben, unter welchen Umständen dies möglich und wie es geht.</span><span class="sxs-lookup"><span data-stu-id="be345-109">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="be345-110">VerSchlüsselte e-Mails, die Sie widerrufen können</span><span class="sxs-lookup"><span data-stu-id="be345-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="be345-111">Sie können verschlüsselte e-Mails widerrufen, wenn der Empfänger eine verschlüsselte e-Mail-Nachricht auf linkbasis erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="be345-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="be345-112">Wenn der Empfänger eine native Inline-Erfahrung in einem unterstützten Outlook-Client erhalten hat, können diese e-Mails nicht widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="be345-112">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="be345-113">Ob ein Empfänger eine Linkbasierte Erfahrung oder eine Inline Erfahrung erhält, hängt vom Empfänger Identitätstyp ab: Office 365-und Microsoft-Konto Empfänger (beispielsweise outlook.com-Benutzer) erhalten eine Inline Erfahrung in unterstützten Outlook-Clients.</span><span class="sxs-lookup"><span data-stu-id="be345-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="be345-114">Alle anderen Empfängertypen, wie etwa Gmail-Empfänger, erhalten eine Linkbasierte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="be345-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="be345-115">In Kürze können Organisationen unabhängig von der Empfänger Identität eine Linkbasierte Benutzeroberfläche erzwingen.</span><span class="sxs-lookup"><span data-stu-id="be345-115">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity.</span></span> <span data-ttu-id="be345-116">Auf diese Weise erhalten alle Empfänger eine Branded-e-Mail mit einem Link zum Office 365-Nachrichten Verschlüsselungs Portal, in dem Sie verschlüsselte e-Mails lesen und beantworten können.</span><span class="sxs-lookup"><span data-stu-id="be345-116">This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails.</span></span> <span data-ttu-id="be345-117">Alle diese verschlüsselten e-Mails sind widerruflich.</span><span class="sxs-lookup"><span data-stu-id="be345-117">All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="be345-118">Empfänger Erfahrung für gesperrte verschlüsselte e-Mails</span><span class="sxs-lookup"><span data-stu-id="be345-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="be345-119">Sobald eine e-Mail gesperrt wurde, erhält der Empfänger beim Versuch, über das Office 365-Nachrichten Verschlüsselungs Portal auf die verschlüsselten e-Mails zuzugreifen, eine Fehlermeldung: "die Nachricht wurde vom Absender widerrufen."</span><span class="sxs-lookup"><span data-stu-id="be345-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Screenshot, der eine gesperrte verschlüsselte e-Mail anzeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="be345-121">So widerrufen Sie eine verschlüsselte e-Mail</span><span class="sxs-lookup"><span data-stu-id="be345-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="be345-122">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="be345-122">Step 1.</span></span> <span data-ttu-id="be345-123">Abrufen der Nachrichten-ID der e-Mail</span><span class="sxs-lookup"><span data-stu-id="be345-123">Obtain the Message ID of the email</span></span>

<span data-ttu-id="be345-124">Bevor Sie eine verschlüsselte e-Mail widerrufen können, müssen Sie die Nachrichten-ID der e-Mail sammeln.</span><span class="sxs-lookup"><span data-stu-id="be345-124">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="be345-125">Die MessageId hat normalerweise das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="be345-125">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="be345-126">Es gibt mehrere Möglichkeiten, die Nachrichten-ID der e-Mail zu finden, die Sie widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="be345-126">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="be345-127">In diesem Abschnitt werden einige Optionen beschrieben, aber Sie können eine beliebige Methode verwenden, die die ID bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="be345-127">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="be345-128">So identifizieren Sie die nachRichten-ID der e-Mail, die Sie mithilfe der Nachrichtenablaufverfolgung im &amp; Security Compliance Center widerrufen möchten</span><span class="sxs-lookup"><span data-stu-id="be345-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="be345-129">Suchen Sie nach der e-Mail nach Absender oder Empfänger mithilfe der [neuen Nachrichtenablaufverfolgung im Office 365 Security _AMP_ Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="be345-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="be345-130">Nachdem Sie die e-Mail gefunden haben, wählen Sie Sie aus, um den Bereich **Nachrichtenablauf Verfolgungs Details** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be345-130">Once you've located the email select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="be345-131">Erweitern Sie **Weitere Informationen** , um nach der Nachrichten-ID zu suchen.</span><span class="sxs-lookup"><span data-stu-id="be345-131">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="be345-132">So identifizieren Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, mithilfe von Office- &amp; Nachrichten Verschlüsselungs Berichten im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="be345-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="be345-133">Navigieren Sie im &amp; Security Compliance Center zum Bericht zur **Nachrichtenverschlüsselung**.</span><span class="sxs-lookup"><span data-stu-id="be345-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="be345-134">Wählen Sie die Tabelle **Details anzeigen** aus, und identifizieren Sie die Nachricht, die Sie widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="be345-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="be345-135">Doppelklicken Sie auf die Nachricht, um Details anzuzeigen, die die nachRichten-ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="be345-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="be345-136">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="be345-136">Step 2.</span></span> <span data-ttu-id="be345-137">Überprüfen, ob die e-Mail widerruflich ist</span><span class="sxs-lookup"><span data-stu-id="be345-137">Verify that the mail is revocable</span></span>

<span data-ttu-id="be345-138">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob eine bestimmte e-Mail-Nachricht widerrufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="be345-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="be345-139">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="be345-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="be345-140">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="be345-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="be345-141">Führen Sie das Cmdlet Set-OMEMessageStatus wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="be345-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="be345-142">Dieser gibt den Betreff der Nachricht zurück und gibt an, ob die Nachricht widerruflich ist.</span><span class="sxs-lookup"><span data-stu-id="be345-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="be345-143">For example,</span><span class="sxs-lookup"><span data-stu-id="be345-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="be345-144">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="be345-144">Step 3.</span></span> <span data-ttu-id="be345-145">Widerrufen der e-Mail</span><span class="sxs-lookup"><span data-stu-id="be345-145">Revoke the mail</span></span>  

<span data-ttu-id="be345-146">Nachdem Sie die nachRichten-ID der e-Mail, die Sie widerrufen möchten, kennen und sichergestellt haben, dass die Nachricht widerruflich ist, können Sie die e-Mail mithilfe des Cmdlets Set-OMEMessageRevocation widerrufen.</span><span class="sxs-lookup"><span data-stu-id="be345-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="be345-147">[Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="be345-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="be345-148">Führen Sie das Cmdlet Set-OMEMessageRevocation wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="be345-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="be345-149">Führen Sie das Cmdlet Get-OMEMessageStatus wie folgt aus, um zu überprüfen, ob die e-Mail widerrufen wurde:</span><span class="sxs-lookup"><span data-stu-id="be345-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="be345-150">Wenn die Sperrung erfolgreich war, gibt das Cmdlet folgendes Ergebnis zurück:</span><span class="sxs-lookup"><span data-stu-id="be345-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`

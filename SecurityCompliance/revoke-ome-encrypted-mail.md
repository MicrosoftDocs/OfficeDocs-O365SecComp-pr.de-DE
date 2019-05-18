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
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="c69bf-103">Widerrufen von E-Mails, die von der erweiterten Office 365-Nachrichtenverschlüsselung verschlüsselt wurden</span><span class="sxs-lookup"><span data-stu-id="c69bf-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="c69bf-104">Die e-Mail-Sperrung wird im Rahmen Office 365 erweiterten Nachrichtenverschlüsselung angeboten.</span><span class="sxs-lookup"><span data-stu-id="c69bf-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="c69bf-105">Office 365 erweiterte Nachrichtenverschlüsselung steht über Office 365 Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c69bf-105">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="c69bf-106">Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c69bf-106">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="c69bf-107">Wenn Ihre Organisation über ein Office 365es Abonnement verfügt, das nicht Office 365 erweiterte Nachrichtenverschlüsselung enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Kompatibilität der Advanced Compliance-SKU erwerben.</span><span class="sxs-lookup"><span data-stu-id="c69bf-107">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="c69bf-108">Dieser Artikel ist Teil einer größeren Reihe von Artikeln über [Office 365 Nachrichtenverschlüsselung](ome.md).</span><span class="sxs-lookup"><span data-stu-id="c69bf-108">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="c69bf-109">Möglicherweise ist es erforderlich, eine e-Mail zu widerrufen, die bereits gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c69bf-109">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="c69bf-110">Wenn die e-Mail mit Office 365 erweiterten Nachrichtenverschlüsselung verschlüsselt wurde und Sie ein Office 365 Administrator sind, können Sie dies unter bestimmten Bedingungen für e-Mails tun.</span><span class="sxs-lookup"><span data-stu-id="c69bf-110">If the email was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="c69bf-111">In diesem Artikel wird beschrieben, unter welchen Umständen und wie dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c69bf-111">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="c69bf-112">Verschlüsselte e-Mails, die Sie widerrufen können</span><span class="sxs-lookup"><span data-stu-id="c69bf-112">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="c69bf-113">Sie können verschlüsselte e-Mails widerrufen, wenn der Empfänger eine Linkbasierte, eingebrannte verschlüsselte e-Mail erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="c69bf-113">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="c69bf-114">Wenn der Empfänger eine systemeigene Inline Erfahrung in einem unterstützten Outlook-Client empfangen hat, können diese e-Mails nicht widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="c69bf-114">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="c69bf-115">Ob ein Empfänger eine Linkbasierte Erfahrung oder eine Inline-Erfahrung erhält, hängt vom Typ der Empfänger Identität ab: Office 365-und Microsoft-Konto Empfänger (beispielsweise Outlook.com-Benutzer) erhalten eine Inline-Erfahrung in unterstützten Outlook-Clients.</span><span class="sxs-lookup"><span data-stu-id="c69bf-115">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="c69bf-116">Alle anderen Empfängertypen, wie etwa Gmail-Empfänger, erhalten eine Linkbasierte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c69bf-116">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="c69bf-117">Empfänger Erfahrung für gesperrte verschlüsselte e-Mails</span><span class="sxs-lookup"><span data-stu-id="c69bf-117">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="c69bf-118">Sobald eine e-Mail widerrufen wurde, erhält der Empfänger eine Fehlermeldung, wenn er versucht, über das Office 365 Nachrichten Verschlüsselungs Portal auf die verschlüsselte e-Mail zuzugreifen: "die Nachricht wurde vom Absender widerrufen".</span><span class="sxs-lookup"><span data-stu-id="c69bf-118">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Screenshot, der eine widerrufene verschlüsselte e-Mail zeigt.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="c69bf-120">Vorgehensweise widerrufen einer verschlüsselten e-Mail</span><span class="sxs-lookup"><span data-stu-id="c69bf-120">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="c69bf-121">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="c69bf-121">Step 1.</span></span> <span data-ttu-id="c69bf-122">Abrufen der Nachrichten-ID der e-Mail</span><span class="sxs-lookup"><span data-stu-id="c69bf-122">Obtain the Message ID of the email</span></span>

<span data-ttu-id="c69bf-123">Bevor Sie eine verschlüsselte e-Mail widerrufen können, müssen Sie die Nachrichten-ID der e-Mail erfassen.</span><span class="sxs-lookup"><span data-stu-id="c69bf-123">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="c69bf-124">Die MessageId weist normalerweise das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="c69bf-124">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="c69bf-125">Es gibt mehrere Möglichkeiten, die Nachrichten-ID der e-Mail zu finden, die Sie widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c69bf-125">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="c69bf-126">In diesem Abschnitt werden einige Optionen beschrieben, aber Sie können eine beliebige Methode verwenden, die die ID bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c69bf-126">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="c69bf-127">So identifizieren Sie die Nachrichten-ID der e-Mail, die Sie mithilfe der Nachrichtenablaufverfolgung im Security &amp; Compliance Center widerrufen möchten</span><span class="sxs-lookup"><span data-stu-id="c69bf-127">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c69bf-128">Suchen Sie nach der e-Mail nach Absender oder Empfänger mithilfe der [neuen Nachrichtenablaufverfolgung im Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="c69bf-128">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="c69bf-129">Nachdem Sie die e-Mail-Adresse gefunden haben, wählen Sie Sie aus, um den Bereich **Nachrichtenablauf Verfolgungs Details** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c69bf-129">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="c69bf-130">Erweitern Sie **Weitere Informationen** , um nach der Nachrichten-ID zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c69bf-130">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="c69bf-131">So identifizieren Sie die Nachrichten-ID der e-Mail, die Sie mithilfe von Office-Nachrichten Verschlüsselungs Berichten im &amp; Security Compliance Center widerrufen möchten</span><span class="sxs-lookup"><span data-stu-id="c69bf-131">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c69bf-132">Navigieren Sie im &amp; Security Compliance Center zum **Nachrichten Verschlüsselungs Bericht**.</span><span class="sxs-lookup"><span data-stu-id="c69bf-132">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>

2. <span data-ttu-id="c69bf-133">Wählen Sie die Tabelle **Details anzeigen** aus, und identifizieren Sie die Nachricht, die Sie widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c69bf-133">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="c69bf-134">Doppelklicken Sie auf die Nachricht, um Details anzuzeigen, die die Nachrichten-ID enthalten.</span><span class="sxs-lookup"><span data-stu-id="c69bf-134">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="c69bf-135">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="c69bf-135">Step 2.</span></span> <span data-ttu-id="c69bf-136">Sicherstellen, dass die e-Mail widerruflich ist</span><span class="sxs-lookup"><span data-stu-id="c69bf-136">Verify that the mail is revocable</span></span>

<span data-ttu-id="c69bf-137">Um zu überprüfen, ob Sie eine bestimmte e-Mail-Nachricht widerrufen können, überprüfen Sie, \*\*\*\* ob das Feld Sperr Status &amp; in der Tabelle Details im Security Compliance Center angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c69bf-137">To verify whether you can revoke a particular email message, check whether the Revocation Status field is visible in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="c69bf-138">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Sie eine bestimmte e-Mail-Nachricht mithilfe von Windows PowerShell widerrufen können.</span><span class="sxs-lookup"><span data-stu-id="c69bf-138">To verify whether or not you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="c69bf-139">Verwenden Sie ein Arbeits-oder Schulkonto, das über globale Administratorberechtigungen in Ihrer Office 365 Organisation verfügt, starten Sie eine Windows PowerShell Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="c69bf-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c69bf-140">Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c69bf-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c69bf-141">Führen Sie das Cmdlet "OMEMessageStatus" wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c69bf-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="c69bf-142">Gibt den Betreff der Nachricht zurück und gibt an, ob die Nachricht widerruflich ist.</span><span class="sxs-lookup"><span data-stu-id="c69bf-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="c69bf-143">For example,</span><span class="sxs-lookup"><span data-stu-id="c69bf-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="c69bf-144">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="c69bf-144">Step 3.</span></span> <span data-ttu-id="c69bf-145">E-Mail widerrufen</span><span class="sxs-lookup"><span data-stu-id="c69bf-145">Revoke the mail</span></span>  

<span data-ttu-id="c69bf-146">Sobald Sie die Nachrichten-ID der e-Mail kennen, die Sie widerrufen möchten, und Sie sichergestellt haben, dass die Nachricht widerruflich ist, können Sie die e-Mail widerrufen.</span><span class="sxs-lookup"><span data-stu-id="c69bf-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email.</span></span>

<span data-ttu-id="c69bf-147">Um die e-Mail im Security &amp; Compliance Center zu widerrufen, wählen Sie in der Tabelle **Details** die Option **widerrufen**aus.</span><span class="sxs-lookup"><span data-stu-id="c69bf-147">To revoke the email in the Security &amp; Compliance Center, in the **Details** table, choose **Revoke**.</span></span>

<span data-ttu-id="c69bf-148">Sie können eine e-Mail mithilfe von Windows PowerShell widerrufen, indem Sie das Cmdlet "OMEMessageRevocation" verwenden.</span><span class="sxs-lookup"><span data-stu-id="c69bf-148">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="c69bf-149">[Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c69bf-149">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c69bf-150">Führen Sie das Cmdlet "OMEMessageRevocation" wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c69bf-150">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="c69bf-151">Um zu überprüfen, ob die e-Mail widerrufen wurde, führen Sie das Get-OMEMessageStatus-Cmdlet wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c69bf-151">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="c69bf-152">Wenn die Sperrung erfolgreich war, gibt das Cmdlet das folgende Ergebnis zurück:</span><span class="sxs-lookup"><span data-stu-id="c69bf-152">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="c69bf-153">Weitere Informationen zu Office 365 erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="c69bf-153">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="c69bf-154">Erweiterte Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="c69bf-154">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="c69bf-155">Office 365 erweiterte Nachrichtenverschlüsselung – e-Mail-Ablauf</span><span class="sxs-lookup"><span data-stu-id="c69bf-155">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="c69bf-156">Beschreibung des Nachrichtenrichtlinien-und Kompatibilitätsdiensts</span><span class="sxs-lookup"><span data-stu-id="c69bf-156">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
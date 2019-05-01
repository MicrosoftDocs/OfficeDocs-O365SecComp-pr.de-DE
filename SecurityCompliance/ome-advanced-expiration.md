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
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="ebf24-103">Festlegen eines Ablaufdatums für e-Mail, die von Office 365 verschlüsselt wurde erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="ebf24-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="ebf24-104">Office 365 erweiterte Nachrichtenverschlüsselung steht über die Office 365-Nachrichtenverschlüsselung in bestimmten Abonnements zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ebf24-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="ebf24-105">Die erweiterte Nachrichtenverschlüsselung ist in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 und Office 365 Education A5 enthalten.</span><span class="sxs-lookup"><span data-stu-id="ebf24-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="ebf24-106">Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht die erweiterte Nachrichtenverschlüsselung von Office 365 enthält, können Sie erweiterte Nachrichtenverschlüsselung als Add-on mit E5-Konformität der Advanced Compliance-SKU erwerben.</span><span class="sxs-lookup"><span data-stu-id="ebf24-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="ebf24-107">Sie können den Nachrichtenablauf für e-Mails verwenden, die Ihre Benutzer an externe Empfänger senden, die das OM-Portal verwenden, um auf verschlüsselte e-Mails zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ebf24-107">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="ebf24-108">Sie erzwingen, dass die Empfänger das OM-Portal verwenden, um verschlüsselte e-Mails anzuzeigen und zu beantworten, die von Ihrer Organisation mithilfe einer benutzerdefinierten Branding-Vorlage gesendet wurden, die ein Ablaufdatum in Windows PowerShell angibt.</span><span class="sxs-lookup"><span data-stu-id="ebf24-108">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows Powershell.</span></span>

<span data-ttu-id="ebf24-109">Wenn Sie als globaler O365-Administrator Ihr Unternehmensbranding anwenden, um das Erscheinungsbild der e-Mail-Nachrichten Ihrer Office 365-Organisation anzupassen, können Sie auch ein Ablaufdatum für diese e-Mail-Nachrichten angeben.</span><span class="sxs-lookup"><span data-stu-id="ebf24-109">As an O365 global administrator, when you apply your company branding to customize the look of your Office 365 organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="ebf24-110">Mit der erweiterten Nachrichtenverschlüsselung von Office 365 können Sie mehrere Vorlagen für verschlüsselte e-Mails aus Ihrer Organisation erstellen.</span><span class="sxs-lookup"><span data-stu-id="ebf24-110">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="ebf24-111">Mithilfe einer Vorlage können Sie steuern, wie lange Empfänger auf e-Mails zugreifen, die von Ihren Benutzern gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebf24-111">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="ebf24-112">Wenn ein Endbenutzer e-Mails mit einem Ablaufdatum erhält, sieht der Benutzer das Ablaufdatum in der Wrapper-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="ebf24-112">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="ebf24-113">Wenn ein Benutzer versucht, eine abgelaufene e-Mail zu öffnen, wird im OM-Portal ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebf24-113">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="ebf24-114">Nur e-Mails an externe Empfänger sind abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ebf24-114">Only emails to external recipients are expirable.</span></span>

<span data-ttu-id="ebf24-115">Mit der erweiterten Nachrichtenverschlüsselung von Office 365 wendet das Office 365 jedes Mal, wenn Sie ein benutzerdefiniertes Branding anwenden, den Wrapper auf e-Mails an, die der Nachrichtenfluss Regel entsprechen, auf die Sie die Vorlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="ebf24-115">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="ebf24-116">Außerdem kann das Ablaufdatum nur verwendet werden, wenn benutzerdefiniertes Branding verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebf24-116">In addition, expiration can only be used if custom branding is used.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="ebf24-117">Erstellen einer benutzerdefinierten Branding-Vorlage zum Erzwingen des Ablaufs von e-Mails mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebf24-117">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="ebf24-118">Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ebf24-118">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="ebf24-119">Führen Sie das Cmdlet New-OMEConfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="ebf24-119">Run the New-OMEConfiguration cmdlet.</span></span>

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

<span data-ttu-id="ebf24-120">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="ebf24-120">Where:</span></span>

- <span data-ttu-id="ebf24-121">Identity ist der Name der benutzerdefinierten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="ebf24-121">Identity is the name of the custom template.</span></span>

- <span data-ttu-id="ebf24-122">ExternalMailExpiryInDays gibt an, wie viele Tage e-Mails von Empfängern aufbewahrt werden sollen, bevor Sie ablaufen.</span><span class="sxs-lookup"><span data-stu-id="ebf24-122">ExternalMailExpiryInDays identifies the number of days you want recipients to be able to keep mail before it expires.</span></span> <span data-ttu-id="ebf24-123">Sie können einen beliebigen Wert zwischen 1 und 730 Tage verwenden.</span><span class="sxs-lookup"><span data-stu-id="ebf24-123">You can use any value between 1 to 730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="ebf24-124">Weitere Informationen zu Office 365 erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="ebf24-124">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="ebf24-125">Office 365 erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="ebf24-125">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="ebf24-126">Widerrufen von e-Mails, die von Office 365 verschlüsselt wurden erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="ebf24-126">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="ebf24-127">Beschreibung des Nachrichtenrichtlinien-und Konformitäts Diensts</span><span class="sxs-lookup"><span data-stu-id="ebf24-127">Message policy and compliance service description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
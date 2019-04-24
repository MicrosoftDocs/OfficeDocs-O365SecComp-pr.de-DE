---
title: Konfigurieren von S/MIME-Einstellungen in Exchange Online für Outlook im Web
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Eine kurze Beschreibung, was Exchange Online-Administratoren tun müssen, um die S/MIME-Einstellungen in Outlook im Web in Exchange Online anzuzeigen und zu konfigurieren.
ms.openlocfilehash: d890b7f39d16d8c0f3866d5ff0024fe31160af6b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258993"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a><span data-ttu-id="910a6-103">Konfigurieren von S/MIME-Einstellungen in Exchange Online für Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="910a6-103">Configure S/MIME settings in Exchange Online for Outlook on the web</span></span>

<span data-ttu-id="910a6-104">Als Administrator für Exchange Online können Sie Outlook im Web (früher als Outlook Web App bezeichnet) einrichten, um das Senden und empfangen von S/MIME-geschützten Nachrichten zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="910a6-104">As an admin for Exchange Online, you can set up Outlook on the web (formerly known as Outlook Web App) to allow sending and receiving S/MIME-protected messages.</span></span> <span data-ttu-id="910a6-105">Verwenden Sie die Cmdlets **Get-SmimeConfig** und **Set-SmimeConfig** , um dieses Feature in Exchange Online PowerShell anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="910a6-105">Use the **Get-SmimeConfig** and **Set-SmimeConfig** cmdlets to view and manage this feature in Exchange Online PowerShell.</span></span> <span data-ttu-id="910a6-106">Wie Sie eine Verbindung mit Exchange Online PowerShell herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="910a6-106">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

<span data-ttu-id="910a6-107">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) und [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span><span class="sxs-lookup"><span data-stu-id="910a6-107">For detailed syntax and parameter information, see [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span></span>

## <a name="considerations-for-chrome"></a><span data-ttu-id="910a6-108">Überlegungen zu Chrome</span><span class="sxs-lookup"><span data-stu-id="910a6-108">Considerations for Chrome</span></span>

<span data-ttu-id="910a6-109">Wenn Sie S/MIME in Outlook im Web im Google Chrome-Webbrowser verwenden möchten, müssen Sie (oder ein anderer Administrator) die Chrom Richtlinie namens **ExtensionInstallForcelist** festlegen und konfigurieren, um die Microsoft S/MIME-Erweiterung in Chrome zu installieren.</span><span class="sxs-lookup"><span data-stu-id="910a6-109">To use S/MIME in Outlook on the web in the Google Chrome web browser, you (or another admin) must set and configure the Chromium policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in Chrome.</span></span> <span data-ttu-id="910a6-110">Die Richtlinie sollte die Syntax verwenden `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` : zum Beispiel `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`:.</span><span class="sxs-lookup"><span data-stu-id="910a6-110">The policy should use the syntax: `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` For example: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span></span> <span data-ttu-id="910a6-111">Beachten Sie, dass die Anwendung dieser Richtlinie Computer mit einer Domäne erfordert, sodass die Verwendung von S/MIME in Chrom effektiv Computer mit einer Domäne erfordert.</span><span class="sxs-lookup"><span data-stu-id="910a6-111">And note that applying this policy requires domain-joined computers, so using S/MIME in Chrome effectively requires domain-joined computers.</span></span>

<span data-ttu-id="910a6-112">Dieser Schritt ist eine Voraussetzung für die Verwendung von Chrome; Es ersetzt nicht das S/MIME-Steuerelement, das von Benutzern installiert wird.</span><span class="sxs-lookup"><span data-stu-id="910a6-112">This step is a prerequisite for using Chrome; it does not replace the S/MIME control that's installed by users.</span></span> <span data-ttu-id="910a6-113">Ausführliche Informationen zur **ExtensionInstallForcelist** -Richtlinie finden Sie unter [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span><span class="sxs-lookup"><span data-stu-id="910a6-113">For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span></span>

## <a name="for-more-information"></a><span data-ttu-id="910a6-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="910a6-114">For more information</span></span>

[<span data-ttu-id="910a6-115">S/MIME für die Nachrichtensignierung und -verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="910a6-115">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

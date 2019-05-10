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
ms.openlocfilehash: 41ec5b675284b2040a11f9e076ccef4afcda561a
ms.sourcegitcommit: d24f50347c671cf5d2d8afec2f80d37d18af8b5d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33867828"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a><span data-ttu-id="b16ca-103">Konfigurieren von S/MIME-Einstellungen in Exchange Online für Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="b16ca-103">Configure S/MIME settings in Exchange Online for Outlook on the web</span></span>

<span data-ttu-id="b16ca-104">Als Administrator für Exchange Online können Sie Outlook im Web (früher als Outlook Web App bezeichnet) einrichten, um das Senden und empfangen von S/MIME-geschützten Nachrichten zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="b16ca-104">As an admin for Exchange Online, you can set up Outlook on the web (formerly known as Outlook Web App) to allow sending and receiving S/MIME-protected messages.</span></span> <span data-ttu-id="b16ca-105">Verwenden Sie die Cmdlets **Get-SmimeConfig** und **Set-SmimeConfig** , um dieses Feature in Exchange Online PowerShell anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b16ca-105">Use the **Get-SmimeConfig** and **Set-SmimeConfig** cmdlets to view and manage this feature in Exchange Online PowerShell.</span></span> <span data-ttu-id="b16ca-106">Wie Sie eine Verbindung mit Exchange Online PowerShell herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="b16ca-106">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

<span data-ttu-id="b16ca-107">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) und [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span><span class="sxs-lookup"><span data-stu-id="b16ca-107">For detailed syntax and parameter information, see [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span></span>

## <a name="considerations-for-chrome"></a><span data-ttu-id="b16ca-108">Überlegungen zu Chrome</span><span class="sxs-lookup"><span data-stu-id="b16ca-108">Considerations for Chrome</span></span>

<span data-ttu-id="b16ca-109">Wenn Sie s/MIME in Outlook im Web im Google Chrome-Webbrowser verwenden möchten, müssen Sie (oder ein anderer Administrator) die Chrom Richtlinie namens **ExtensionInstallForcelist** festlegen und konfigurieren, um die Microsoft S/MIME-Erweiterung in Chrome zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b16ca-109">To use S/MIME in Outlook on the web in the Google Chrome web browser, you (or another admin) must set and configure the Chromium policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in Chrome.</span></span> <span data-ttu-id="b16ca-110">Der Richtlinienwert lautet `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span><span class="sxs-lookup"><span data-stu-id="b16ca-110">The policy value is `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span></span> <span data-ttu-id="b16ca-111">Beachten Sie, dass die Anwendung dieser Richtlinie Computer mit einer Domäne erfordert, sodass die Verwendung von S/MIME in Chrom effektiv Computer mit einer Domäne erfordert.</span><span class="sxs-lookup"><span data-stu-id="b16ca-111">And note that applying this policy requires domain-joined computers, so using S/MIME in Chrome effectively requires domain-joined computers.</span></span>

<span data-ttu-id="b16ca-112">Ausführliche Informationen zur **ExtensionInstallForcelist** -Richtlinie finden Sie unter [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span><span class="sxs-lookup"><span data-stu-id="b16ca-112">For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span></span>

<span data-ttu-id="b16ca-113">Dieser Schritt ist eine Voraussetzung für die Verwendung von Chrome; Es ersetzt nicht das S/MIME-Steuerelement, das von Benutzern installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b16ca-113">This step is a prerequisite for using Chrome; it does not replace the S/MIME control that's installed by users.</span></span> <span data-ttu-id="b16ca-114">Benutzer werden aufgefordert, das s/MIME-Steuerelement in Outlook im Web während der ersten Verwendung von s/MIME herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b16ca-114">Users are prompted to download and install the S/MIME control in Outlook on the web during their first use of S/MIME.</span></span> <span data-ttu-id="b16ca-115">Oder Benutzer können proaktiv zu **S/MIME** im Outlook im Web-Einstellungen wechseln, um den Download-Link für das Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b16ca-115">Or, users can proactively go to **S/MIME** in their Outlook on the web settings to get the download link for the control.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="b16ca-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b16ca-116">For more information</span></span>

[<span data-ttu-id="b16ca-117">S/MIME für die Nachrichtensignierung und -verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b16ca-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

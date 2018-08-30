---
title: Problembehandlung bei Gerät Registrierung mit MDM für Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Wenn Sie Probleme arbeiten, wenn Sie versuchen, ein Gerät in das Mobile Gerät Management (MDM) für Office 365 registrieren, versuchen Sie die Schritte, die hier aufgeführten, um das Problem zu verfolgen. Wenn die allgemeinen Schritte das Problem nicht beheben, finden Sie in den nachfolgenden Abschnitten mit bestimmten Schritten für Ihren Gerätetyp.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272110"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a><span data-ttu-id="f11dc-104">Problembehandlung bei Gerät Registrierung mit MDM für Office 365</span><span class="sxs-lookup"><span data-stu-id="f11dc-104">Troubleshoot device enrollment with MDM for Office 365</span></span>

<span data-ttu-id="f11dc-p102">Wenn Sie Probleme arbeiten, wenn Sie versuchen, ein Gerät in das Mobile Gerät Management (MDM) für Office 365 registrieren, versuchen Sie die Schritte, die hier aufgeführten, um das Problem zu verfolgen. Wenn die allgemeinen Schritte das Problem nicht beheben, finden Sie in den nachfolgenden Abschnitten mit bestimmten Schritten für Ihren Gerätetyp.</span><span class="sxs-lookup"><span data-stu-id="f11dc-p102">If you're running into issues when you try to enroll a device in Mobile Device Management (MDM) for Office 365, try the steps listed here to track down the problem. If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>
  
## <a name="steps-to-try-first"></a><span data-ttu-id="f11dc-107">Schritte zum zuerst versuchen.</span><span class="sxs-lookup"><span data-stu-id="f11dc-107">Steps to try first</span></span>

<span data-ttu-id="f11dc-108">Überprüfen Sie die folgenden Schritte aus, um zu starten:</span><span class="sxs-lookup"><span data-stu-id="f11dc-108">To start, check the following:</span></span>
  
- <span data-ttu-id="f11dc-109">Stellen Sie sicher, dass das Gerät nicht bereits mit einem anderen mobilen Gerät Management Anbieter wie etwa Intune registriert ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-109">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>
    
- <span data-ttu-id="f11dc-110">Stellen Sie sicher, dass das Gerät auf das richtige Datum und die Uhrzeit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-110">Make sure that the device is set to the correct date and time.</span></span>
    
- <span data-ttu-id="f11dc-111">Wechseln Sie zu einer anderen Wi-Fi oder Mobilfunknetz auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f11dc-111">Switch to a different Wi-Fi or cellular network on the device.</span></span>
    
- <span data-ttu-id="f11dc-112">Deinstallieren Sie für Android oder iOS-Geräte die app Intune Unternehmensportal auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f11dc-112">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span>
    
## <a name="ios-phone-or-tablet"></a><span data-ttu-id="f11dc-113">iOS-Telefon oder tablet</span><span class="sxs-lookup"><span data-stu-id="f11dc-113">iOS phone or tablet</span></span>

- <span data-ttu-id="f11dc-114">Stellen Sie sicher, dass [Sie ein Zertifikat APNs eingerichtet](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7)haben.</span><span class="sxs-lookup"><span data-stu-id="f11dc-114">Make sure that you've [set up an APNs certificate](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span></span>
    
- <span data-ttu-id="f11dc-p103">In den **Einstellungen** \> **Allgemeine** \> **Profil** (oder **Gerätemanagement**), stellen Sie sicher, dass ein **Management-Profil** nicht bereits installiert ist. Wenn dies der Fall, entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="f11dc-p103">In **Settings** \> **General** \> **Profile** (or **Device Management**), make sure that a **Management Profile** is not already installed. If it is, remove it.</span></span> 
    
- <span data-ttu-id="f11dc-117">Wenn Sie die Fehlermeldung sehen "Fehler beim Geräts zu registrieren" Melden Sie sich bei Office 365 und stellen Sie sicher, dass eine Lizenz, die Exchange Online enthält, die dem Benutzer zugewiesen wurde, die an das Gerät angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-117">If you see the error message, "Device failed to enroll," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="f11dc-118">Wenn Sie sehen die Fehlermeldung "Profil konnte nicht installiert werden," führen Sie eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="f11dc-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>
    
  - <span data-ttu-id="f11dc-119">Stellen Sie sicher, dass Safari als Standardbrowser auf dem Gerät ist und dass Cookies nicht deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="f11dc-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>
    
  - <span data-ttu-id="f11dc-120">Starten Sie das Gerät neu, und klicken Sie dann navigieren Sie zu portal.manage.microsoft.com, melden Sie sich mit Ihrem Office 365-Benutzer-ID und das Kennwort, und versuchen Sie, das Profil manuell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f11dc-120">Reboot the device, then navigate to portal.manage.microsoft.com, sign in with your Office 365 user ID and password, and attempt to install the profile manually.</span></span>
    
## <a name="windows-rt-tablet"></a><span data-ttu-id="f11dc-121">Windows RT-tablet</span><span class="sxs-lookup"><span data-stu-id="f11dc-121">Windows RT tablet</span></span>

- <span data-ttu-id="f11dc-122">Stellen Sie sicher, dass Ihre Domäne [in Office 365 MDM entwickelt eingerichtet](set-up-mobile-device-management.md)ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-122">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="f11dc-123">Stellen Sie sicher, dass der Benutzer ist **Turn On** auswählen, anstatt auswählen **teilnehmen**.</span><span class="sxs-lookup"><span data-stu-id="f11dc-123">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>
    
## <a name="windows-phone"></a><span data-ttu-id="f11dc-124">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="f11dc-124">Windows Phone</span></span>

- <span data-ttu-id="f11dc-125">Stellen Sie sicher, dass Ihre Domäne [in Office 365 MDM entwickelt eingerichtet](set-up-mobile-device-management.md)ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-125">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="f11dc-126">Stellen Sie sicher, dass das Gerät Windows 8.1 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f11dc-126">Make sure the device is running Windows 8.1 or later.</span></span>
    
## <a name="android-phone-or-tablet"></a><span data-ttu-id="f11dc-127">Android-Telefon oder tablet</span><span class="sxs-lookup"><span data-stu-id="f11dc-127">Android phone or tablet</span></span>

- <span data-ttu-id="f11dc-128">Stellen Sie sicher, dass das Gerät Android 4.0 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f11dc-128">Make sure the device is running Android 4.0 or later.</span></span>
    
- <span data-ttu-id="f11dc-129">Wenn Sie die Fehlermeldung sehen "Es konnte nicht dieses Gerät registrieren" Melden Sie sich bei Office 365, und stellen Sie sicher, dass eine Lizenz, die Exchange Online enthält, die dem Benutzer zugewiesen wurde, die an das Gerät angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="f11dc-129">If you see the error message, "We couldn't enroll this device," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="f11dc-130">Überprüfen Sie im **Infobereich** auf dem Gerät zu sehen, ob alle erforderlichen Endbenutzeraktionen ausstehen, und wenn Ja, führen Sie die Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f11dc-130">Check the **Notification Area** on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span> 
    


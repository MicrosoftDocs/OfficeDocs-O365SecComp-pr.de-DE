---
title: Registrieren Sie Ihr mobile Gerät in Office 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
ms.assetid: c8ac722d-dcaf-4135-8345-3e6327f5d3c5
description: Bevor Sie Office 365-Diensten über das Gerät verwenden können, müssen Sie in Verwaltung mobiler Geräte für Office 365 (MDM) registrieren, um diese Schritte zu befolgen. Sie tun, wenn Sie Ihre Arbeit hinzuzufügen oder Schule e-Mail-Konto auf Ihrem Gerät zum ersten Mal.
ms.openlocfilehash: 63e4052d42007d97928f158a704beb9721758a44
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272300"
---
# <a name="enroll-your-mobile-device-in-office-365"></a><span data-ttu-id="79f59-104">Registrieren Sie Ihr mobile Gerät in Office 365</span><span class="sxs-lookup"><span data-stu-id="79f59-104">Enroll your mobile device in Office 365</span></span>

<span data-ttu-id="79f59-p102">Verwenden Ihr Telefon, Tablet und andere mobile Geräte für die Arbeit ist eine hervorragende Möglichkeit zum bleiben darüber informiert und Business-Projekten arbeiten, während Sie sich nicht im Büro sind. Bevor Sie Office 365-Diensten über das Gerät verwenden können, müssen Sie zuerst es Verwaltung mobiler Geräte für Office 365 (MDM) mithilfe von Microsoft Intune Unternehmensportal registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79f59-p102">Using your phone, tablet, and other mobile devices for work is a great way to stay informed and work on business projects while you're away from the office. Before you can use Office 365 services with your device, you may need to first enroll it in Mobile Device Management for Office 365 (MDM) using Microsoft Intune Company Portal.</span></span>
  
<span data-ttu-id="79f59-p103">Organisationen entscheiden MDM, sodass Mitarbeiter ihren mobilen Geräten verwenden können, um sicheren Zugriff auf Arbeit e-Mail, Kalender und Dokumente, während das Unternehmen wichtige Daten schützt und ihre Compliance-Anforderungen erfüllt. [Erfahren Sie mehr über MDM in Office 365](https://go.microsoft.com/fwlink/?LinkId=615142).</span><span class="sxs-lookup"><span data-stu-id="79f59-p103">Organizations choose MDM so that employees can use their mobile devices to securely access work email, calendars, and documents while the business secures important data and meets their compliance requirements. [Learn about MDM in Office 365](https://go.microsoft.com/fwlink/?LinkId=615142).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="79f59-p104">Wenn Sie Ihr Gerät in MDM für Office 365 registrieren, müssen Sie möglicherweise ein Kennwort, zusammen mit zulassen die Option für Ihre Organisation Arbeit auf das Gerät Wischen einrichten. Bereinigung von einem Gerät kann (von Office 365 Administrationscenter) beispielsweise ausgeführt werden, um alle Daten vom Gerät zu entfernen, wenn das Kennwort zu oft falsch eingegeben wird oder wenn Nutzungsbedingungen unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="79f59-p104">When you enroll your device in MDM for Office 365, you might be required to set up a password, together with allowing the option for your work organization to wipe the device. A device wipe can be performed (from the Office 365 admin center), for example, to remove all data from the device if the password is entered incorrectly too many times or if usage terms are broken.</span></span> 
  
 <span data-ttu-id="79f59-111">**Unterstützte Geräte**</span><span class="sxs-lookup"><span data-stu-id="79f59-111">**Supported devices**</span></span>
  
<span data-ttu-id="79f59-p105">MDM und InTune funktioniert bei den meisten, jedoch nicht alle mobilen Geräten. Die folgenden werden mit MDM für Office 365 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79f59-p105">MDM and InTune works with most, but not all, mobile devices. The following are supported with MDM for Office 365.</span></span>
  
- <span data-ttu-id="79f59-114">iOS 7.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="79f59-114">iOS 7.1 or later</span></span>
    
- <span data-ttu-id="79f59-115">Android 4 oder höher</span><span class="sxs-lookup"><span data-stu-id="79f59-115">Android 4 or later</span></span>
    
- <span data-ttu-id="79f59-116">Windows 8.1 (Telefon und PC) und höher mit Windows 10 einschließen</span><span class="sxs-lookup"><span data-stu-id="79f59-116">Windows 8.1 (Phone and PC) and later to include Windows 10</span></span>
    
- <span data-ttu-id="79f59-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="79f59-117">Windows 10</span></span>
    
<span data-ttu-id="79f59-118">Wenn Ihr Gerät nicht aufgeführte, und Sie mit MDM und Intune verwendet werden müssen, wenden Sie sich an den Systemadministrator arbeiten oder Schule.</span><span class="sxs-lookup"><span data-stu-id="79f59-118">If your device is not listed above, and you need to use it with MDM and Intune, contact your work or school administrator.</span></span>
  
> [!TIP]
> <span data-ttu-id="79f59-119">Wenn Sie das Gerät zum Registrieren von Probleme haben, finden Sie unter: [Troubleshoot Gerät Registrierung mit MDM für Office 365](troubleshoot-mdm.md).</span><span class="sxs-lookup"><span data-stu-id="79f59-119">If you're having trouble enrolling your device, see: [Troubleshoot device enrollment with MDM for Office 365](troubleshoot-mdm.md).</span></span> 
  
## <a name="set-up-your-mobile-device-with-intune-and-mdm-for-office-365"></a><span data-ttu-id="79f59-120">Einrichten von Ihrem mobilen Gerät mit Intune und MDM für Office 365</span><span class="sxs-lookup"><span data-stu-id="79f59-120">Set up your mobile device with Intune and MDM for Office 365</span></span>

<span data-ttu-id="79f59-121">Aktiviert ein Gerät von Office 365 und MDM verwaltet werden, die Intune Unternehmensportal</span><span class="sxs-lookup"><span data-stu-id="79f59-121">The Intune Company Portal enables a device to be managed by Office 365 and MDM.</span></span>
  
### <a name="iphone-or-ipad"></a><span data-ttu-id="79f59-122">iPhone oder iPad</span><span class="sxs-lookup"><span data-stu-id="79f59-122">iPhone or iPad</span></span>

> [!TIP]
> <span data-ttu-id="79f59-123">Nicht möglich, e-Mails senden und empfangen, bis Sie diesen Schritt ausführen.</span><span class="sxs-lookup"><span data-stu-id="79f59-123">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="79f59-124">Wechseln Sie auf der Apple App Store herunterladen und Intune Unternehmensportal installieren.</span><span class="sxs-lookup"><span data-stu-id="79f59-124">Go to the Apple App Store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="79f59-125">[Befolgen Sie diese Schritte zum Konfigurieren und verbinden](https://go.microsoft.com/fwlink/?linkid=875316) Ihrer iOS-Telefon oder Tablet mit dem Unternehmensportal zu Office 365.</span><span class="sxs-lookup"><span data-stu-id="79f59-125">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875316) your iOS phone or tablet with the Company portal to Office 365.</span></span> 
    
### <a name="android-phone-or-tablet"></a><span data-ttu-id="79f59-126">Android-Telefon oder tablet</span><span class="sxs-lookup"><span data-stu-id="79f59-126">Android phone or tablet</span></span>

> [!TIP]
> <span data-ttu-id="79f59-127">Nicht möglich, e-Mails senden und empfangen, bis Sie diesen Schritt ausführen.</span><span class="sxs-lookup"><span data-stu-id="79f59-127">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="79f59-128">Wechseln Sie an den Store Google wiedergeben herunterladen und Installieren von Intune Unternehmensportal.</span><span class="sxs-lookup"><span data-stu-id="79f59-128">Go to the Google Play store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="79f59-129">[Befolgen Sie diese Schritte zum Konfigurieren und verbinden](https://go.microsoft.com/fwlink/?linkid=875317) Ihrer Android-Telefon oder Tablet mit dem Unternehmensportal zu Office 365.</span><span class="sxs-lookup"><span data-stu-id="79f59-129">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875317) your Android phone or tablet with the Company portal to Office 365.</span></span> 
    
## <a name="whats-next"></a><span data-ttu-id="79f59-130">Was kommt als nächstes</span><span class="sxs-lookup"><span data-stu-id="79f59-130">What's next</span></span>

<span data-ttu-id="79f59-131">Nachdem das Gerät MDM für Office 365 registriert ist, können Sie mithilfe von Office-apps auf Ihrem Gerät e-Mail, Kalender, Kontakte und Dokumente entwickelt starten.</span><span class="sxs-lookup"><span data-stu-id="79f59-131">After your device is enrolled in MDM for Office 365, you can start using Office apps on your device to work with email, calendar, contacts, and documents.</span></span>
  


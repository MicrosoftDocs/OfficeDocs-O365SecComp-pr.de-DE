---
title: Löschen eines mobilen Geräts in Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Verwaltung für Office 365 integrierten mobiler Geräte können eine selektive Remotegerätzurücksetzung nur Informationen der Organisation zu entfernen, oder eine vollständige Remotegerätzurücksetzung alle Daten von einem mobilen Gerät löschen und Wiederherstellen auf ihre Factory Einstellungen.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272500"
---
# <a name="wipe-a-mobile-device-in-office-365"></a><span data-ttu-id="cdd79-103">Löschen eines mobilen Geräts in Office 365</span><span class="sxs-lookup"><span data-stu-id="cdd79-103">Wipe a mobile device in Office 365</span></span>
  
<span data-ttu-id="cdd79-104">Verwaltung für Office 365 integrierten mobiler Geräte können eine selektive Remotegerätzurücksetzung nur Informationen der Organisation zu entfernen, oder eine vollständige Remotegerätzurücksetzung alle Daten von einem mobilen Gerät löschen und Wiederherstellen auf ihre Factory Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="cdd79-104">You can use built-in mobile device management for Office 365 to do a selective wipe to remove only organizational information, or a full wipe to delete all information from a mobile device and restore it to its factory settings.</span></span>
  
## <a name="what-to-know-before-you-begin"></a><span data-ttu-id="cdd79-105">Was Sie wissen, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="cdd79-105">What to know before you begin</span></span>

- <span data-ttu-id="cdd79-p101">Mobile Geräte können vertrauliche Organisationsinformationen gespeichert und gewähren Sie Zugriff auf Office 365-Ressourcen Ihrer Organisation. Zum Schutz Ihrer Organisation Informationen können Sie eine vollständige Remotegerätzurücksetzung oder eine selektive Wischen ausführen:</span><span class="sxs-lookup"><span data-stu-id="cdd79-p101">Mobile devices can store sensitive organizational information and provide access to your organization's Office 365 resources. To help protect your organization's information, you can do a full wipe or a selective wipe:</span></span>
    
  - <span data-ttu-id="cdd79-p102">**Vollständige Remotegerätzurücksetzung**: Löscht alle Daten auf dem Mobilgerät eines Benutzers, einschließlich der installierten Programme, Fotos und persönliche Informationen. Wenn der Löschvorgang abgeschlossen ist, wird das Gerät auf ihre Einstellungen Factory wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-p102">**Full wipe**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information. When the wipe is complete, the device is restored to its factory settings.</span></span> 
    
  - <span data-ttu-id="cdd79-110">**Selektive Wischen**: Unternehmensdaten und Blätter installiert Applications, Fotos und persönlichen Informationen auf dem mobilen Gerät des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-110">**Selective wipe**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span> 
    
- <span data-ttu-id="cdd79-111">Wenn ein Gerät (vollständige Remotegerätzurücksetzung oder selektive Remotegerätzurücksetzung) gelöscht wird, wird das Gerät aus der Liste der verwalteten Geräten entfernt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-111">When a device is wiped (full wipe or selective wipe), the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="cdd79-p103">Sie können richten Sie eine Richtlinie zur Verwaltung von mobilen Gerät, die automatisch (vollständige Wischen) Löscht ein Gerät, nachdem der Benutzer erfolglos versucht, das Gerät Kennwort eingeben eine bestimmte Anzahl von Malen. Führen Sie die Schritte in [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cdd79-p103">You can set up a mobile device management policy that automatically wipes (full wipe) a device after the user unsuccessfully tries to enter the device's password a specific number of times. Follow the steps in [Create and deploy device security policies](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="cdd79-114">Wenn Sie wissen, was ein Benutzer treten, wenn Sie ihr Gerät Wischen möchten, finden Sie unter [Was ist der Benutzer und Gerät Auswirkungen?](wipe-a-mobile-device.md#BKMK_Impact).</span><span class="sxs-lookup"><span data-stu-id="cdd79-114">If you want to know what a user will experience when you wipe their device, see [What's the user and device impact?](wipe-a-mobile-device.md#BKMK_Impact).</span></span>
    
## <a name="wipe-a-mobile-device"></a><span data-ttu-id="cdd79-115">Löschen eines mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="cdd79-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="cdd79-116">Wechseln Sie zu der [ ![klicken Sie hier, um zu Office 365 Administrationscenter zu wechseln.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span><span class="sxs-lookup"><span data-stu-id="cdd79-116">Go to the [![Click here to go to the Office 365 admin center.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span></span>

2. <span data-ttu-id="cdd79-117">Wechseln Sie zu [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **Verhinderung von Datenverlust** \> **Gerätemanagement**.</span><span class="sxs-lookup"><span data-stu-id="cdd79-117">Go to [Go to the Office 365 Security &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)\> **Data loss prevention** \> **Device management**.</span></span>
    
3. <span data-ttu-id="cdd79-118">Wählen Sie das Gerät, den, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="cdd79-118">Select the device you want to wipe.</span></span>
    
4. <span data-ttu-id="cdd79-119">Wählen Sie den Typ des Remotezurücksetzung Sie tun möchten.</span><span class="sxs-lookup"><span data-stu-id="cdd79-119">Select the type of remote wipe you want to do.</span></span>
    
  - <span data-ttu-id="cdd79-120">Führen Sie eine selektive Remotegerätzurücksetzung und Löschen nur Office 365-Organisation die Informationen im rechten Bereich, wählen Sie **selektive Wischen**.</span><span class="sxs-lookup"><span data-stu-id="cdd79-120">To do a selective wipe and delete only Office 365 organization information, in the right pane, select **Selective wipe**.</span></span>
    
  - <span data-ttu-id="cdd79-121">Wählen Sie zum Ausführen einer vollständigen Remotegerätzurücksetzung und Wiederherstellen von das Gerät auf ihre Factory Einstellungen, die im rechten Bereich in **vollständige Remotegerätzurücksetzung**aus.</span><span class="sxs-lookup"><span data-stu-id="cdd79-121">To do a full wipe and restore the device to its factory settings, in the right pane, select **Full wipe**.</span></span>
    
![Wählen Sie ein Gerät, und wählen Sie dann die Remotegerätzurücksetzung ausführen.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. <span data-ttu-id="cdd79-123">Wählen Sie **Ja,** um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="cdd79-123">Select **Yes** to confirm.</span></span> 
    
<span data-ttu-id="cdd79-124">Bis der Löschvorgang abgeschlossen ist, wird der **Status des** als **RetirePending** oder **RetireIssued**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-124">Until the wipe finishes, the **Device status** will show as **RetirePending** or **RetireIssued**.</span></span>
  
### <a name="how-do-i-know-it-worked"></a><span data-ttu-id="cdd79-125">Wissen ich, dass es funktioniert?</span><span class="sxs-lookup"><span data-stu-id="cdd79-125">How do I know it worked?</span></span>

<span data-ttu-id="cdd79-126">Das mobile Gerät in der Liste der verwalteten Geräten wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-126">You'll no longer see the mobile device in the list of managed devices.</span></span>
  
## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="cdd79-127">Warum sollten Sie ein Gerät Wischen?</span><span class="sxs-lookup"><span data-stu-id="cdd79-127">Why would you want to wipe a device?</span></span>

<span data-ttu-id="cdd79-128">Es gibt verschiedene Gründe für verlorener Geräte:</span><span class="sxs-lookup"><span data-stu-id="cdd79-128">There are several reasons for wiping devices:</span></span>
  
- <span data-ttu-id="cdd79-p104">Mobile Geräte wie Smartphones und Tablets werden Funktionsumfang immer immer. Dies bedeutet, dass für Ihre Benutzer zum Speichern von vertraulichen Unternehmensinformationen (beispielsweise persönliche Identifikationsnummer oder vertraulich Communications) und darauf zugreifen, unterwegs ist es einfacher. Wenn eines dieser mobilen Geräte Verlust oder Diebstahl, kann das Gerät sofort verlorener Hilfe verhindern, dass Ihre Organisation Informationen beziehen, die in die falschen Hände.</span><span class="sxs-lookup"><span data-stu-id="cdd79-p104">Mobile devices like smartphones and tablets are becoming more full-featured all the time. This means it's easier for your users to store sensitive corporate information (such as personal identification or confidential communications) and access it on the go. If one of these mobile devices is lost or stolen, wiping the device immediately can help prevent your organization's information from ending up in the wrong hands.</span></span>
    
- <span data-ttu-id="cdd79-132">Wenn ein Benutzer die Organisation mit einem persönlichen Gerät die MDM für Office 365 registriert ist verlässt, helfen Ihnen Organisationsinformationen aus mit diesen Benutzern wechseln, indem Sie wie folgt eine selektive Remotegerätzurücksetzung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="cdd79-132">When a user leaves the organization with a personal device that is enrolled in MDM for Office 365, you can help prevent organizational information from going with that user by doing a selective wipe.</span></span>
    
- <span data-ttu-id="cdd79-p105">Wenn Ihre Organisation mobile Geräte für Benutzer bereitstellt, müssen Sie möglicherweise von Zeit zu Zeit zuzuweisende Geräte. Ausführen einer vollständigen Remotegerätzurücksetzung auf einem Gerät vor der Zuweisung zu einem neuen Benutzer unterstützt wird sichergestellt, dass vertraulicher Informationen aus der vorherigen Besitzer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="cdd79-p105">If your organization provides mobile devices to users, you might need to reassign devices from time to time. Doing a full wipe on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>
    
## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="cdd79-135">Was ist der Benutzer und die Auswirkungen Gerät?</span><span class="sxs-lookup"><span data-stu-id="cdd79-135">What's the user and device impact?</span></span>

<span data-ttu-id="cdd79-p106">Der Löschvorgang wird sofort an das mobile Gerät gesendet. Das Gerät wird auch als nicht kompatibel in AAD gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cdd79-p106">The wipe is sent immediately to the mobile device. The device is also marked as not compliant in AAD.</span></span>
  
<span data-ttu-id="cdd79-138">In der folgenden Tabelle wird beschrieben, welche Inhalte für jede Art von Gerät entfernt wird, wenn ein Gerät selektiv Kennworteingaben gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="cdd79-138">The following table describes what content is removed for each device type when a device is selectively wiped.</span></span>
  
|<span data-ttu-id="cdd79-139">**Inhalte Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="cdd79-139">**Content impact**</span></span>|<span data-ttu-id="cdd79-140">**Windows Phone 8.1**</span><span class="sxs-lookup"><span data-stu-id="cdd79-140">**Windows Phone 8.1**</span></span>|<span data-ttu-id="cdd79-141">**iOS 7.1+**</span><span class="sxs-lookup"><span data-stu-id="cdd79-141">**iOS 7.1+**</span></span>|<span data-ttu-id="cdd79-142">**Android 4 und höher**</span><span class="sxs-lookup"><span data-stu-id="cdd79-142">**Android 4+**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cdd79-143">Unternehmen Portal app\* wird deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="cdd79-143">Company Portal app\* is uninstalled.</span></span>  <br/> |<span data-ttu-id="cdd79-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cdd79-144">N/A</span></span>  <br/> |<span data-ttu-id="cdd79-145">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-145">✔</span></span>  <br/> |<span data-ttu-id="cdd79-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cdd79-146">N/A</span></span>  <br/> |
|<span data-ttu-id="cdd79-p107">Office 365-app-Daten von apps, in dem Steuerung des Zugriffs von MDM für Office 365 unterstützt wird, gehostet werden entfernt (derzeit Outlook und OneDrive für Unternehmen). Die apps werden nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="cdd79-p107">Office 365 app data hosted by apps where access control is supported by MDM for Office 365 is removed (currently Outlook and OneDrive for Business). The apps are not removed.</span></span>  <br/> <span data-ttu-id="cdd79-149">Outlook für Android werden zwischengespeicherten-e-Mails nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cdd79-149">Outlook for Android does not remove cached emails.</span></span>  <br/> |<span data-ttu-id="cdd79-150">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-150">✔</span></span>  <br/> |<span data-ttu-id="cdd79-151">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-151">✔</span></span>  <br/> |<span data-ttu-id="cdd79-152">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-152">✔</span></span>  <br/> |
|<span data-ttu-id="cdd79-153">Aufgeführt, die von MDM für Office 365 für Geräte angewendet wurden, werden nicht mehr auf dem Gerät erzwungen, und Benutzer können die Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="cdd79-153">Policy settings that were applied by MDM for Office 365 to devices are no longer enforced on the device and users can change the settings.</span></span>  <br/> |<span data-ttu-id="cdd79-154">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-154">✔</span></span>  <br/> |<span data-ttu-id="cdd79-155">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-155">✔</span></span>  <br/> |<span data-ttu-id="cdd79-156">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-156">✔</span></span>  <br/> |
|<span data-ttu-id="cdd79-157">E-Mail-Profile von MDM für Office 365 werden entfernt, und zwischengespeicherte e-Mail auf dem Gerät wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cdd79-157">Email profiles created by MDM for Office 365 are removed and cached email on the device is deleted.</span></span>  <br/> |<span data-ttu-id="cdd79-158">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cdd79-158">N/A</span></span>  <br/> |<span data-ttu-id="cdd79-159">✔</span><span class="sxs-lookup"><span data-stu-id="cdd79-159">✔</span></span>  <br/> |<span data-ttu-id="cdd79-160">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cdd79-160">N/A</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="cdd79-161">\*Unternehmen Portal app ist im App Store für iOS und die Wiedergabe-Speichers für Android-Geräte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cdd79-161">\* Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="cdd79-162">Verwandte Inhalte</span><span class="sxs-lookup"><span data-stu-id="cdd79-162">Related content</span></span>

[<span data-ttu-id="cdd79-163">Verwalten von mobilen Geräten in Office 365</span><span class="sxs-lookup"><span data-stu-id="cdd79-163">Manage mobile devices in Office 365</span></span>](set-up-mobile-device-management.md)
  


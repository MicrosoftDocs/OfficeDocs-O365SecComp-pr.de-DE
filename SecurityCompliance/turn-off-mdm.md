---
title: Zum Deaktivieren der Verwaltung mobiler Geräte in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Führen Sie diese Schritte, um beenden MDM Richtlinien für mobile Geräte in Office 365-Organisation erzwungen wird.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272220"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a><span data-ttu-id="c19ea-103">Zum Deaktivieren der Verwaltung mobiler Geräte in Office 365</span><span class="sxs-lookup"><span data-stu-id="c19ea-103">How to turn off Mobile Device Management in Office 365</span></span>

<span data-ttu-id="c19ea-104">Um effektiv MDM für Office 365 deaktivieren, Personengruppen (definiert durch Sicherheitsgruppen) aus der Informationsverwaltungsrichtlinien Gerät entfernen oder die Richtlinien selbst zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c19ea-104">To effectively turn off MDM for Office 365, you remove groups of people (defined by security groups) from the device management policies, or remove the policies themselves.</span></span> 
  
- <span data-ttu-id="c19ea-105">Entfernen Sie Gruppen von Benutzern durch Entfernen von Benutzersicherheitsgruppen aus der Richtlinien für Geräte, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c19ea-105">Remove groups of users by removing user security groups from the device policies you've created.</span></span> 
    
- <span data-ttu-id="c19ea-106">Deaktivieren Sie MDM für alle Benutzer, indem Sie alle MDM Geräterichtlinien entfernen.</span><span class="sxs-lookup"><span data-stu-id="c19ea-106">Disable MDM for everyone by removing all MDM device policies.</span></span> 
    
<span data-ttu-id="c19ea-p101">Diese Optionen werden MDM Erzwingung für Geräte in Ihrer Organisation entfernt. Leider können nicht Sie einfach "aufheben" MDM für Office 365 Nachdem Sie es eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="c19ea-p101">These options will remove MDM enforcement for devices in your organization. Unfortunately, you can't simply "unprovision" MDM for Office 365 after you've set it up.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c19ea-p102">Achten Sie auf die Auswirkung auf Benutzercomputern, wenn Sie Benutzersicherheitsgruppen aus Richtlinien entfernen oder die Richtlinien selbst zu entfernen. Beispielsweise e-Mail-Profile und Cache-e-Mails können entfernt werden je nach dem Gerät. Weitere Informationen: [Was ist die Auswirkung von Sicherheitsrichtlinien auf anderes Gerätetypen?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span><span class="sxs-lookup"><span data-stu-id="c19ea-p102">Be aware of the impact on users' devices when you remove user security groups from policies or remove the policies themselves. For example, email profiles and cached emails may be removed, depending on the device. See: [What is the impact of security policies on different device types?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span></span>
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a><span data-ttu-id="c19ea-112">Entfernen von Benutzersicherheitsgruppen aus MDM Geräterichtlinien</span><span class="sxs-lookup"><span data-stu-id="c19ea-112">Remove user security groups from MDM device policies</span></span>

1. <span data-ttu-id="c19ea-113">Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Verhinderung von Datenverlust** \> **Gerät Sicherheitsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-113">Go to **Security &amp; Compliance Center**\> **Data loss prevention** \> **Device security polices**.</span></span>
    
2. <span data-ttu-id="c19ea-114">Wählen Sie eine Richtlinie für Geräte aus, und klicken Sie auf ![Bearbeitungssymbol](media/O365-MDM-CreatePolicy-EditIcon.gif) **Richtlinie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-114">Select a device policy, and click ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif) **Edit policy**.</span></span>
    
3. <span data-ttu-id="c19ea-115">Klicken Sie unter **Bereitstellung**auf **- Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-115">Under **Deployment**, click **- Remove**.</span></span>
    
    <span data-ttu-id="c19ea-116">Wählen Sie unter **Gruppen**die eine Sicherheitsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="c19ea-116">Under **Groups**, select a security group.</span></span>
    
4.  <span data-ttu-id="c19ea-117">Klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-117">Click **Remove**.</span></span>
    
5. <span data-ttu-id="c19ea-118">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-118">Click **Save**.</span></span>
    
## <a name="remove-mdm-device-policies"></a><span data-ttu-id="c19ea-119">Entfernen von MDM Geräterichtlinien</span><span class="sxs-lookup"><span data-stu-id="c19ea-119">Remove MDM device policies</span></span>

1. <span data-ttu-id="c19ea-120">Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Sicherheitsrichtlinien für Geräte**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-120">Go to **Security &amp; Compliance Center**\> **Security policies** \> **Device security policies**.</span></span>
    
2. <span data-ttu-id="c19ea-p103">Wählen Sie eine Richtlinie für Geräte aus, und klicken Sie dann auf ![Bild von den Papierkorb können Symbol. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Richtlinie zu löschen**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-p103">Select a device policy, and then click ![Image of the trash can icon.](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Delete policy**.</span></span>
    
3. <span data-ttu-id="c19ea-123">Klicken Sie im Dialogfeld **Warnung** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c19ea-123">In the **Warning** dialog, click **Yes**.</span></span> 
    


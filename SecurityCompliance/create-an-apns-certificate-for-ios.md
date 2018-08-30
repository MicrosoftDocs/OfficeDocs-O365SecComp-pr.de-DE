---
title: Erstellen Sie ein Zertifikat APNs für iOS-Geräte
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Zum Verwalten von iOS-Geräte wie iPad und iPhones in Verwaltung mobiler Geräte für Office 365 folgendermaßen Sie vor, um ein Zertifikat APNs zuerst zu erstellen.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272050"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="d8d6e-103">Erstellen Sie ein Zertifikat APNs für iOS-Geräte</span><span class="sxs-lookup"><span data-stu-id="d8d6e-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="d8d6e-104">Zum Verwalten von iOS-Geräte wie iPad und iPhones in Verwaltung mobiler Geräte für Office 365 müssen Sie ein Zertifikat APNs erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="d8d6e-p101">Zu diesem Zweck führen Sie die Schritte auf der Seite Verwaltungsportals über den Link **Einrichten** . (Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Gerätemanagement** \> **Einstellungen verwalten**.)</span><span class="sxs-lookup"><span data-stu-id="d8d6e-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Richten Sie die Verwaltung von mobilen Geräten erforderlich und empfohlene Schritte](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="d8d6e-108">Wählen Sie neben **Konfigurieren eines Zertifikats APNs für iOS-Geräte** **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="d8d6e-109">Wählen Sie **die CSR-Datei herunterladen** und speichern Sie die zertifikatanforderung für den signierenden um an einer Stelle auf dem Computer, den Sie problemlos wiederfinden.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Im Dialogfeld APN Zertifikat installieren](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="d8d6e-111">Wählen Sie **Weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="d8d6e-112">Erstellen Sie ein Zertifikat APN.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="d8d6e-113">Wählen Sie **Apple APNS Portal** , um die Apple-Push Zertifikate Portal zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Installieren von APN Cert Benachrichtigungsdialogfeld mit Apple APNS Portal ausgewählt](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="d8d6e-115">Melden Sie sich mit einem Apple-ID.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="d8d6e-p102">Verwenden Sie ein Unternehmen, der ein e-Mail-Konto Apple-ID, die mit Ihrer Organisation bleiben zugeordnet, selbst wenn der Benutzer, der das Konto verwaltet verlässt. Speichern Sie diese ID, da Sie müssen die gleiche-ID verwenden, wird das Zertifikat zu erneuern.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="d8d6e-118">Wählen Sie **ein Zertifikat erstellen** aus, und akzeptieren Sie die **Rechtlichen Hinweisen**.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="d8d6e-119">**Navigieren** Sie zu signierenden Zertifikat anfordern, dass Sie von Office 365 an Ihren Computer heruntergeladen haben, und wählen Sie die **Hochladen**.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="d8d6e-120">**Laden Sie** erstellt das Zertifikat APN Apple Push Zertifikat Portal an Ihren Computer.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="d8d6e-121">Wenn Sie das Zertifikat herunterladen Probleme haben, aktualisieren Sie den Browser.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="d8d6e-122">Gehen Sie zurück zu Office 365, und wählen Sie **Weiter** , um die Seite **Hochladen APNS Zertifikat** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="d8d6e-123">Navigieren Sie zu der APN-Zertifikat, das Sie über das Apple-Push Zertifikate Portal heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Klicken Sie auf die Schaltfläche Durchsuchen, um APNS Zertifikat auszuwählen, die Sie von Apple heruntergeladen haben](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="d8d6e-125">Wählen Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-125">Select **Finish**.</span></span>
    
<span data-ttu-id="d8d6e-126">Wechseln Sie wieder zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Gerätemanagement** \> **Einstellungen verwalten** , um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d8d6e-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  


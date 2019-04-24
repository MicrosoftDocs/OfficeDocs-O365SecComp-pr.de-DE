---
title: Erstellen eines APNs-Zertifikats für iOS-Geräte
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Um iOS-Geräte wie iPad und iPhones in der Verwaltung mobiler Geräte für Office 365 zu verwalten, führen Sie die folgenden Schritte aus, um zuerst ein APNs-Zertifikat zu erstellen.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258623"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Erstellen eines APNs-Zertifikats für iOS-Geräte

 Um iOS-Geräte wie iPad und iPhones in der Verwaltung mobiler Geräte für Office 365 zu verwalten, müssen Sie ein APNs-Zertifikat erstellen. 
  
Führen Sie dazu die Schritte aus dem Link **Einrichten** auf der Portalseite aus. (Gehen Sie **zu &amp; Security Compliance Center** \> - **Sicherheitsrichtlinien** \> **Geräteverwaltung** \> **Einstellungen verwalten**.)
  
![Einrichten der erforderlichen und empfohlenen Schritte für die Verwaltung mobiler Geräte](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.
    
2. Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember. 
    
    ![Installieren des APN-Zertifikats (Dialogfeld)](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3.  Select **Next**. 
    
4.  Create an APN certificate.
    
  - Select **Apple APNS Portal** to open the Apple Push Certificates Portal.  
    
    ![Installieren des APN-Benachrichtigungs-CERT-Dialogs mit ausgewähltem Apple APNS-Portal](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Sign in with an Apple ID.
    
    > [!IMPORTANT]
    > Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate. 
  
  - Select **Create a Certificate** and accept the **Terms of Use**.
    
  - **Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.
    
  - **Download** the APN certificate created by the Apple Push Certificate Portal to your computer. 
    
    > [!TIP]
    > If you're having trouble downloading the certificate, refresh your browser. 
  
5. Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page. 
    
6.  Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.
    
    ![Klicken Sie auf die Schaltfläche Durchsuchen, um APNS CERT auszuwählen, das Sie von Apple heruntergeladen haben](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Select **Finish**.
    
Gehen Sie zurück zu Security ** &amp; Compliance Center** \> **Security Policies** \> **Device Management** \> **Manage Settings** , um das Setup abzuschließen. 
  


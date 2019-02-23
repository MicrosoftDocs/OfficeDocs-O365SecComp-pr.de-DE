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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220455"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Erstellen eines APNs-Zertifikats für iOS-Geräte

 Um iOS-Geräte wie iPad und iPhones in der Verwaltung mobiler Geräte für Office 365 zu verwalten, müssen Sie ein APNs-Zertifikat erstellen. 
  
Führen Sie dazu die Schritte aus dem Link **Einrichten** auf der Portalseite aus. (Gehen Sie **zu &amp; Security Compliance Center** \> - **Sicherheitsrichtlinien** \> **Geräteverwaltung** \> **Einstellungen verwalten**.)
  
![Einrichten der erforderlichen und empfohlenen Schritte für die Verwaltung mobiler Geräte](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Wählen Sie neben **Konfigurieren eines APNs-Zertifikats für IOS-Geräte**die Option **Einrichten**aus.
    
2. Wählen Sie **CSR-Datei herunterladen** aus, und speichern Sie die Zertifikatsignaturanforderung auf einem Speicherort auf Ihrem Computer, den Sie sich merken werden. 
    
    ![Installieren des APN-Zertifikats (Dialogfeld)](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Wählen Sie **Weiter** aus.
    
4. Erstellen Sie ein APN-Zertifikat.
    
  - Wählen Sie **Apple APNS-Portal** aus, um das Apple Push Certificates-Portal zu öffnen. 
    
    ![Installieren des APN-Benachrichtigungs-CERT-Dialogs mit ausgewähltem Apple APNS-Portal](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Melden Sie sich mit einer Apple-ID an.
    
    > [!IMPORTANT]
    > Verwenden Sie eine Unternehmens Apple-ID, die einem e-Mail-Konto zugeordnet ist, das in Ihrer Organisation verbleiben soll, auch wenn der Benutzer, der das Konto verwaltet, verlässt. Speichern Sie diese ID, da Sie beim Erneuern des Zertifikats dieselbe ID verwenden müssen. 
  
  - Wählen Sie **Zertifikat erstellen** und die **Nutzungsbedingungen**akzeptieren aus.
    
  - **Wechseln** Sie zur zertifikatsignieranforderung, die Sie von Office 365 auf Ihren Computer heruntergeladen haben, und wählen Sie **hochladen**aus.
    
  - **Laden** Sie das vom Apple Push Certificate Portal erstellte APN-Zertifikat auf Ihren Computer herunter. 
    
    > [!TIP]
    > Wenn Sie Probleme beim Herunterladen des Zertifikats haben, aktualisieren Sie Ihren Browser. 
  
5. Wechseln Sie zurück zu Office 365, und wählen Sie **weiter** , um zur Seite **APNS-Zertifikat hochladen** zu gelangen. 
    
6. Navigieren Sie zum APN-Zertifikat, das Sie aus dem Apple Push Certificates-Portal heruntergeladen haben.
    
    ![Klicken Sie auf die Schaltfläche Durchsuchen, um APNS CERT auszuwählen, das Sie von Apple heruntergeladen haben](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Wählen Sie **Fertig stellen**aus.
    
Gehen Sie zurück zu Security ** &amp; Compliance Center** \> **Security Policies** \> **Device Management** \> **Manage Settings** , um das Setup abzuschließen. 
  


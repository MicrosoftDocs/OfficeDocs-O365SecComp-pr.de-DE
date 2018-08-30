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
# <a name="create-an-apns-certificate-for-ios-devices"></a>Erstellen Sie ein Zertifikat APNs für iOS-Geräte

 Zum Verwalten von iOS-Geräte wie iPad und iPhones in Verwaltung mobiler Geräte für Office 365 müssen Sie ein Zertifikat APNs erstellen. 
  
Zu diesem Zweck führen Sie die Schritte auf der Seite Verwaltungsportals über den Link **Einrichten** . (Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Gerätemanagement** \> **Einstellungen verwalten**.)
  
![Richten Sie die Verwaltung von mobilen Geräten erforderlich und empfohlene Schritte](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Wählen Sie neben **Konfigurieren eines Zertifikats APNs für iOS-Geräte** **Einrichten**.
    
2. Wählen Sie **die CSR-Datei herunterladen** und speichern Sie die zertifikatanforderung für den signierenden um an einer Stelle auf dem Computer, den Sie problemlos wiederfinden. 
    
    ![Im Dialogfeld APN Zertifikat installieren](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Wählen Sie **Weiter**aus.
    
4. Erstellen Sie ein Zertifikat APN.
    
  - Wählen Sie **Apple APNS Portal** , um die Apple-Push Zertifikate Portal zu öffnen. 
    
    ![Installieren von APN Cert Benachrichtigungsdialogfeld mit Apple APNS Portal ausgewählt](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Melden Sie sich mit einem Apple-ID.
    
    > [!IMPORTANT]
    > Verwenden Sie ein Unternehmen, der ein e-Mail-Konto Apple-ID, die mit Ihrer Organisation bleiben zugeordnet, selbst wenn der Benutzer, der das Konto verwaltet verlässt. Speichern Sie diese ID, da Sie müssen die gleiche-ID verwenden, wird das Zertifikat zu erneuern. 
  
  - Wählen Sie **ein Zertifikat erstellen** aus, und akzeptieren Sie die **Rechtlichen Hinweisen**.
    
  - **Navigieren** Sie zu signierenden Zertifikat anfordern, dass Sie von Office 365 an Ihren Computer heruntergeladen haben, und wählen Sie die **Hochladen**.
    
  - **Laden Sie** erstellt das Zertifikat APN Apple Push Zertifikat Portal an Ihren Computer. 
    
    > [!TIP]
    > Wenn Sie das Zertifikat herunterladen Probleme haben, aktualisieren Sie den Browser. 
  
5. Gehen Sie zurück zu Office 365, und wählen Sie **Weiter** , um die Seite **Hochladen APNS Zertifikat** abzurufen. 
    
6. Navigieren Sie zu der APN-Zertifikat, das Sie über das Apple-Push Zertifikate Portal heruntergeladen haben.
    
    ![Klicken Sie auf die Schaltfläche Durchsuchen, um APNS Zertifikat auszuwählen, die Sie von Apple heruntergeladen haben](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Wählen Sie auf **Fertig stellen**.
    
Wechseln Sie wieder zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Gerätemanagement** \> **Einstellungen verwalten** , um die Installation abzuschließen. 
  


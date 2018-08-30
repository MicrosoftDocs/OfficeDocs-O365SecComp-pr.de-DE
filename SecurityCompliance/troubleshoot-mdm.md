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
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a>Problembehandlung bei Gerät Registrierung mit MDM für Office 365

Wenn Sie Probleme arbeiten, wenn Sie versuchen, ein Gerät in das Mobile Gerät Management (MDM) für Office 365 registrieren, versuchen Sie die Schritte, die hier aufgeführten, um das Problem zu verfolgen. Wenn die allgemeinen Schritte das Problem nicht beheben, finden Sie in den nachfolgenden Abschnitten mit bestimmten Schritten für Ihren Gerätetyp.
  
## <a name="steps-to-try-first"></a>Schritte zum zuerst versuchen.

Überprüfen Sie die folgenden Schritte aus, um zu starten:
  
- Stellen Sie sicher, dass das Gerät nicht bereits mit einem anderen mobilen Gerät Management Anbieter wie etwa Intune registriert ist.
    
- Stellen Sie sicher, dass das Gerät auf das richtige Datum und die Uhrzeit festgelegt ist.
    
- Wechseln Sie zu einer anderen Wi-Fi oder Mobilfunknetz auf dem Gerät.
    
- Deinstallieren Sie für Android oder iOS-Geräte die app Intune Unternehmensportal auf dem Gerät.
    
## <a name="ios-phone-or-tablet"></a>iOS-Telefon oder tablet

- Stellen Sie sicher, dass [Sie ein Zertifikat APNs eingerichtet](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7)haben.
    
- In den **Einstellungen** \> **Allgemeine** \> **Profil** (oder **Gerätemanagement**), stellen Sie sicher, dass ein **Management-Profil** nicht bereits installiert ist. Wenn dies der Fall, entfernen Sie es. 
    
- Wenn Sie die Fehlermeldung sehen "Fehler beim Geräts zu registrieren" Melden Sie sich bei Office 365 und stellen Sie sicher, dass eine Lizenz, die Exchange Online enthält, die dem Benutzer zugewiesen wurde, die an das Gerät angemeldet ist.
    
- Wenn Sie sehen die Fehlermeldung "Profil konnte nicht installiert werden," führen Sie eine der folgenden:
    
  - Stellen Sie sicher, dass Safari als Standardbrowser auf dem Gerät ist und dass Cookies nicht deaktiviert sind.
    
  - Starten Sie das Gerät neu, und klicken Sie dann navigieren Sie zu portal.manage.microsoft.com, melden Sie sich mit Ihrem Office 365-Benutzer-ID und das Kennwort, und versuchen Sie, das Profil manuell zu installieren.
    
## <a name="windows-rt-tablet"></a>Windows RT-tablet

- Stellen Sie sicher, dass Ihre Domäne [in Office 365 MDM entwickelt eingerichtet](set-up-mobile-device-management.md)ist.
    
- Stellen Sie sicher, dass der Benutzer ist **Turn On** auswählen, anstatt auswählen **teilnehmen**.
    
## <a name="windows-phone"></a>Windows Phone

- Stellen Sie sicher, dass Ihre Domäne [in Office 365 MDM entwickelt eingerichtet](set-up-mobile-device-management.md)ist.
    
- Stellen Sie sicher, dass das Gerät Windows 8.1 oder höher ausgeführt wird.
    
## <a name="android-phone-or-tablet"></a>Android-Telefon oder tablet

- Stellen Sie sicher, dass das Gerät Android 4.0 oder höher ausgeführt wird.
    
- Wenn Sie die Fehlermeldung sehen "Es konnte nicht dieses Gerät registrieren" Melden Sie sich bei Office 365, und stellen Sie sicher, dass eine Lizenz, die Exchange Online enthält, die dem Benutzer zugewiesen wurde, die an das Gerät angemeldet ist.
    
- Überprüfen Sie im **Infobereich** auf dem Gerät zu sehen, ob alle erforderlichen Endbenutzeraktionen ausstehen, und wenn Ja, führen Sie die Aktionen. 
    


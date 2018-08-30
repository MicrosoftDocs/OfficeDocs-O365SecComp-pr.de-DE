---
title: Übersicht über die Verwaltung von mobilen Geräten (MDM) für Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: Sie können verwalten und mobile Geräten secure, wenn sie mit Office 365-Organisation verbunden sind, mithilfe der Verwaltung mobiler Geräte für Office 365. Mobile Geräte wie Smartphones und Tablets, mit denen Arbeit e-Mail, Kalender, Kontakte zugreifen und Dokumente dafür sorgen, dass die Mitarbeiter ihre Arbeit unabhängig vom Standort jederzeit und überall, erhalten eine wichtige Rolle spielen. Daher ist es wichtig, dass Sie Ihrer Organisation Informationen schützen Wenn Personen-Geräte verwenden. Sie können MDM für Office 365 verwenden, um gerätesicherheit Richtlinien und Zugriffsregeln festzulegen und mobile Geräte zu löschen, wenn sie verlorenen oder gestohlenen.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272490"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a>Übersicht über die Verwaltung von mobilen Geräten (MDM) für Office 365

Sie können verwalten und mobile Geräten secure, wenn sie mit Office 365-Organisation verbunden sind, mithilfe der Verwaltung mobiler Geräte für Office 365. Mobile Geräte wie Smartphones und Tablets, mit denen Arbeit e-Mail, Kalender, Kontakte zugreifen und Dokumente dafür sorgen, dass die Mitarbeiter ihre Arbeit unabhängig vom Standort jederzeit und überall, erhalten eine wichtige Rolle spielen. Daher ist es wichtig, dass Sie Ihrer Organisation Informationen schützen Wenn Personen-Geräte verwenden. Sie können MDM für Office 365 verwenden, um gerätesicherheit Richtlinien und Zugriffsregeln festzulegen und mobile Geräte zu löschen, wenn sie verlorenen oder gestohlenen.
  
![MDM auf Android-Telefon](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a>Welche Arten von Geräten können Sie verwalten?

MDM für Office 365 können viele Arten von mobilen Geräten wie Windows Phone, Android, iPhone und iPad verwalten. Zum Verwalten von mobiler Geräten, die von Personen in Ihrer Organisation verwendeten muss jede Person eine entsprechende Office 365-Lizenz und ihr Gerät in MDM für Office 365 registriert werden muss. 
  
Um herauszufinden, was MDM für Office 365 für jede Art von Gerät unterstützt wird, finden Sie unter [Funktionen der Verwaltung mobiler Geräte für Office 365](capabilities-of-mobile-device-management.md).
  
## <a name="setup-steps-for-mdm"></a>Einrichtungsschritte für MDM

Ein Office 365 globaler Administrator müssen die folgenden Schritte aus, um zu aktivieren und MDM für Office 365 einrichten. Befolgen Sie die Anleitung unter dem Thema auf [MDM für Office 365 einrichten](set-up-mobile-device-management.md) , um ausführliche Schritte finden Sie unter. Hier ist eine schnelle Zusammenfassung: 
  
> Schritt 1: Aktivieren Sie MDM für Office 365, indem Sie die folgenden Schritte in das [Festlegen von Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md).
    
> Schritt 2: Einrichten von MDM für Office 365, beispielsweise ein APNs Zertifikat zum Verwalten von iOS-Geräte zu erstellen und Hinzufügen eines Datensatzes Domain Name System (DNS) für Ihre Domäne zur Unterstützung von Windows-Telefonen.
    
> Schritt 3: Erstellen von Geräterichtlinien und Benutzergruppen zuweisen. Wenn Sie dies tun, erhalten die Benutzer eine [e-Mail auf dem Gerät](enroll-your-mobile-device.md). Und wenn sie die Registrierung abgeschlossen haben, wird ihre Geräte eingeschränkt durch die Richtlinien, die Sie für diese eingerichtet haben.
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a>Geräteverwaltungsaufgaben

Nach dem haben Sie MDM für Office 365 einrichten und Ihre Benutzer ihren Geräten registriert haben, können Sie die Geräte verwalten, blockieren Sie den Zugriff oder ein Gerät Wischen, falls erforderlich. Erfahren Sie mehr über [einige allgemeine Verwaltungsaufgaben für Geräte](manage-devices-in-mdm.md), einschließlich, wo Sie die Aufgaben ausgeführt werden.
  
## <a name="other-ways-to-manage-devices-and-apps"></a>Andere Möglichkeiten zum Verwalten von Geräten und apps

Wenn Sie benötigen umfasst mehr Funktionen bereit als MDM für Office 365, sehen Sie sich diesen [Vergleich der Features MDM und Microsoft Intune](choose-between-mdm-and-intune.md) um festzustellen, ob ein Abonnement Intune Anforderungen Ihrer Organisation gerecht werden. 
  
Wenn Sie nur mobile app-Verwaltung (MAM) benötigen, bietet die vielleicht für Personen, die Aktualisierung Arbeit Projekte auf ihren eigenen Geräten Intune eine andere Option zusätzlich zu registrieren und Verwalten von Geräten. Ein Abonnement Intune können Sie MAM Richtlinien eingerichtet mithilfe des Azure-Portals, selbst wenn Personen Geräte Intune registriert werden nicht. Finden Sie unter [Protect app-Daten mithilfe von MAM Richtlinien](https://go.microsoft.com/fwlink/?LinkId=825439). 
  
## <a name="see-also"></a>Siehe auch

[Abrufen von Informationen zu Geräten von MDM verwaltet werden](get-details-about-mdm-managed-devices.md)

[Einrichten von MDM für Office 365](set-up-mobile-device-management.md)
  
[Registrieren von mobilen Geräten in MDM](enroll-your-mobile-device.md)
  
[Verwalten von Geräten in MDM registriert](manage-devices-in-mdm.md)


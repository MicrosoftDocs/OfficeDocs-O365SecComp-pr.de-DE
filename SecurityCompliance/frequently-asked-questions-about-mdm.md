---
title: Häufig gestellte Fragen zur Verwaltung mobiler Geräte für Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 3871f99c-c9db-4a23-86f9-902c1b02f58d
description: Dieser Artikel enthält häufig gestellte Fragen zu Mobile Device Management (MDM) für Office 365, ein Feature, das Unterstützung bei der Verwaltung und Sicherung von mobilen Geräten in Office 365.
ms.openlocfilehash: 6c4a5b3603d392b3d83769cd0f17450ce70565be
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272270"
---
# <a name="frequently-asked-questions-about-mobile-device-management-for-office-365"></a>Häufig gestellte Fragen zur Verwaltung mobiler Geräte für Office 365

Dieser Artikel enthält häufig gestellte Fragen zu Mobile Device Management (MDM) für Office 365, ein Feature, das Unterstützung bei der Verwaltung und Sicherung von mobilen Geräten in Office 365.
  
## <a name="faqs"></a>FAQ

- [Wie finde ich MDM für Office 365? Ich nicht in der Office 365-Verwaltungskonsole angezeigt wird](#how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center)
    
- [Wie kann ich Gerätemanagement in MDM Einstieg](#how-can-i-get-started-with-device-management-in-mdm)
    
- [Ich möchte MDM einrichten, aber es scheint unterbrochene. Die Office 365-Dienststatus hat "Bereitstellung" für eine Weile angezeigt wurde. Was kann ich tun?](#im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do)
    
- [Was kann ich tun, wenn Gerät Registrierung ein Fehler auftritt?](#what-can-i-do-if-device-enrollment-fails)
    
- [Was ist der Unterschied zwischen Intune und MDM für Office 365?](#whats-the-difference-between-intune-and-mdm-for-office-365)
    
- [Wie funktionieren Richtlinien für MDM? Wie einrichten kann ich sie? Deaktivieren sie?](#how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them)
    
- [Kann ich von der Verwaltung von Exchange ActiveSync-Geräten zur MDM für Office 365 wechseln?](#can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365)
    
- [Ich MDM einrichten, aber es entfernt werden soll. Was sind die Schritte?](#i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps)
    
- [Benötigen Sie weitere Hilfe](#still-need-help)
    
## <a name="how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center"></a>Wie finde ich MDM für Office 365? Ich nicht in der Office 365-Verwaltungskonsole angezeigt wird

Wir haben die Einführung dieses Feature bei Office 365-Kunden abgeschlossen. Suchen Sie nach der Registerkarte **Verwaltung von Geräten** in der [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Wenn es nicht angezeigt wird, informieren Sie uns. Finden Sie unter [benötigen Sie weitere Hilfe?](#still-need-help), und wir helfen Ihnen den Einstieg. 
  
## <a name="how-can-i-get-started-with-device-management-in-mdm"></a>Wie kann ich Gerätemanagement in MDM Einstieg

Es gibt vier Schritte zum Einstieg in MDM für Office 365 (erfahren Sie Details in [Set up Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md)):
  
1. **MDM aktivieren** Wechseln Sie zu der [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) , und wählen Sie die **Verwaltung von Geräten**. Klicken Sie auf zum Deaktivieren der Aktivierungsprozess loszulegen **steigen** . 
    
2. **Konfiguration für MDM abzuschließen**. Dies möglicherweise APNs Zertifikatkonfiguration und Updates für DNS-Einträge für Ihre Domäne erforderlich. 
    
3. **Erstellen von Richtlinien**. Erstellen von Informationsverwaltungsrichtlinien Gerät, und anwenden auf Gruppen von Benutzern, die [in Sicherheitsgruppen eingerichtet](create-device-security-policies.md)sind. Es wird empfohlen, dass Sie starten, indem Sie die Richtlinien für eine kleine Testgruppe bereitstellen. In das Wertpapier &amp; Compliance Center, wählen Sie **Sicherheitsrichtlinien für Geräte**.
    
4. **Benutzer registrieren Geräte.** Benutzer, die eine Richtlinie angewendet wurde, werden auf [ihren Geräten registrieren](enroll-your-mobile-device.md) aufgefordert, wenn sie versuchen, Office 365 Daten zugreifen (z. B. mit ihren e-Mail-Client). 
    
## <a name="im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do"></a>Ich möchte MDM einrichten, aber es scheint unterbrochene. Die Office 365-Dienststatus hat "Bereitstellung" für eine Weile angezeigt wurde. Was kann ich tun?

Es kann einige Zeit in der Dienst Sie sich vorzubereiten worden ist. Wenn die Bereitstellung abgeschlossen ist, sehen Sie die Verwaltung mobiler Geräte für Office 365-Seite. Wenn Sie 24 Stunden gewartet haben, und der Status weiterhin **Provisioning ist**, finden Sie [benötigen Sie weitere Hilfe?](#still-need-help) und wir helfen herauszufinden, was das Problem ist. 
  
## <a name="what-can-i-do-if-device-enrollment-fails"></a>Was kann ich tun, wenn Gerät Registrierung ein Fehler auftritt?

Wenn Sie Probleme beim Abrufen eines Geräts registriert haben, versuchen Sie zunächst, überprüfen Folgendes:
  
- Stellen Sie sicher, dass das Gerät nicht bereits mit einem anderen mobilen Gerät Management Anbieter wie etwa Intune registriert ist.
    
- Stellen Sie sicher, dass das Gerät auf das richtige Datum und die Uhrzeit festgelegt ist.
    
- Wechseln Sie zu einer anderen Wi-Fi oder Mobilfunknetz auf dem Gerät.
    
- Deinstallieren Sie für Android oder iOS-Geräte die app Intune Unternehmensportal auf dem Gerät.
    
Wenn Registrierung immer noch funktioniert nicht, [versuchen Sie diese zusätzlichen Schritte zur Problembehandlung](troubleshoot-mdm.md).
  
## <a name="whats-the-difference-between-intune-and-mdm-for-office-365"></a>Was ist der Unterschied zwischen Intune und MDM für Office 365?

Beide MDM für Office 365 und Intune bieten Cloud-basierte Lösungen zum Verwalten von Geräten in Ihrer Organisation. Verwenden Sie diesen [nebeneinander Vergleich](choose-between-mdm-and-intune.md) von zwei Diensten, mit denen Sie entscheiden, ob mit Intune oder MDM für Office 365 für Sie optimiert ist. 
  
## <a name="how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them"></a>Wie funktionieren Richtlinien für MDM? Wie einrichten kann ich sie? Deaktivieren sie?

Nach Abschluss der anfänglichen Installation für MDM für Office 365, Sie [Richtlinien erstellen, und wenden Sie diese an eine Gruppe von Benutzern](create-device-security-policies.md) in [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Für die Benutzer, denen für die Richtlinien gelten, erfordern Richtlinien für die Benutzer, ihren Geräten in MDM für Office 365 registrieren, bevor das Gerät Zugriff auf Office 365-Daten verwendet werden kann. Die Richtlinien, die Sie einrichten Bestimmen der Einstellungen für mobile Geräte, z. B., wie oft Kennwörter zurückgesetzt werden müssen oder gibt an, ob die Verschlüsselung erforderlich ist. 
  
Wir stellen Schritt-für-Schritt-Anleitung zum [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](create-device-security-policies.md). Erstellen Sie die Richtlinien in das Wertpapier &amp; Compliance Center, und Sie können eine oder mehrere Richtlinien deaktivieren, indem Rückgabe an die Sicherheit &amp; Compliance Center und Bearbeitung der Richtlinie die angewendete Gruppe zu entfernen. Oder Sie können auch nicht die Richtlinie vollständig zu entfernen.
  
Wenn Sie, dass eine bestimmte Gruppe von Benutzern durch Richtlinien beeinträchtigt wird verhindern möchten, können Sie eine Gruppe der Ausschluss-Gruppe hinzufügen. In das Wertpapier &amp; Compliance Center auf der Registerkarte **Geräte** wählen Sie **Device Access-Einstellungen verwalten**aus, und fügen Sie der Gruppe sein, um die **gibt es Sicherheitsgruppen, die Steuerung des Zugriffs ausgeschlossen werden soll?** Abschnitt. 
  
## <a name="can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365"></a>Kann ich von der Verwaltung von Exchange ActiveSync-Geräten zur MDM für Office 365 wechseln?

Wenn Sie bereits [Exchange ActiveSync-Richtlinien](https://go.microsoft.com/fwlink/?LinkId=615145) zum Verwalten von mobiler Geräten verwenden, können Sie die Schritte zum [Festlegen von Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md)mit MDM für Office 365 starten.
  
Wenn Sie die Richtlinien, die Sie in MDM für Office 365 für Benutzergruppen erstellen anwenden, überschreiben diese Richtlinien Exchange ActiveSync-Postfachrichtlinien für mobile Geräte und gerätezugriffsregeln, die Sie in der Exchange-Verwaltungskonsole für die Benutzer erstellt haben. 
  
Nachdem ein Gerät für Office 365, alle Exchange ActiveSync-Postfachrichtlinie Mobilgerät MDM registriert ist oder gerätezugriffsregel angewendet auf das Gerät wird ignoriert.
  
## <a name="i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps"></a>Ich MDM einrichten, aber es entfernt werden soll. Was sind die Schritte?

Leider können nicht Sie einfach "aufheben" MDM für Office 365 Nachdem Sie es eingerichtet haben. Jedoch können Sie es für Gruppen von Benutzern durch Entfernen von Benutzersicherheitsgruppen aus der die von die Ihnen erstellten Geräterichtlinien entfernen. Oder es für alle Benutzer deaktivieren, indem Sie die Richtlinien für Geräte entfernen, damit sie nicht vorhanden sind und nicht erzwungen. Finden Sie unter [Verwaltung mobiler Geräte in Office 365 zu deaktivieren](turn-off-mdm.md).
  
## <a name="still-need-help"></a>Benötigen Sie weitere Hilfe?

[![Erhalten von Hilfe in den Communityforen von Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administratoren: Anmelden und Serviceanfrage erstellen](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administratoren: Support kontaktieren](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

  


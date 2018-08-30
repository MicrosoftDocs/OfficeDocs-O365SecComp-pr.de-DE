---
title: Funktionen der integrierten mobilen Geräteverwaltung für Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.DevicePolicySupportedDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: a1da44e5-7475-4992-be91-9ccec25905b0
description: Mobile Device Management für Office 365 helfen Ihnen beim schützen und Verwalten von mobilen Geräten wie iPhones, iPads, sonst noch und Windows-Telefonen in Ihrer Organisation verwendeten. Erstellen Sie Mobilgerät Informationsverwaltungsrichtlinien mit Einstellungen, die den Zugriff auf Office 365-e-Mail und Dokumente auf unterstützten mobilen Geräten und apps Ihrer Organisation ein, und lassen Sie ein Gerät Remote Wischen, wenn es Diebstahl Steuerelement helfen kann.
ms.openlocfilehash: b7200eee3b50c2fc6d3e0ea0920236d71837a88b
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272600"
---
# <a name="capabilities-of-built-in-mobile-device-management-for-office-365"></a>Funktionen der integrierten mobilen Geräteverwaltung für Office 365

Mobile Device Management für Office 365 helfen Ihnen beim schützen und Verwalten von mobilen Geräten wie iPhones, iPads, sonst noch und Windows-Telefonen von lizenzierten Office 365-Benutzer in Ihrer Organisation verwendet. Sie können Richtlinien für mobile Geräte Management mit Einstellungen erstellen, die Steuern des Zugriffs auf Ihre Organisation Office 365-e-Mail und Dokumente für unterstützten mobilen Geräten und apps helfen kann. Wenn ein Gerät verlorenen oder gestohlenen, können Sie das Gerät zum Entfernen von vertraulichen Organisationsinformationen Remote Wischen.
    
Benötigen Sie weitere Funktionen als in MDM für Office 365 enthalten ist? Festzustellen, ob Microsoft Intune wurde, was Sie benötigen: [Wählen Sie zwischen MDM für Office 365 und Microsoft Intune](choose-between-mdm-and-intune.md).
  
## <a name="supported-devices"></a>Unterstützte Geräte

Sie können die MDM für Office 365 zu schützen und verwalten die folgenden Arten von Geräten verwenden.
  
- Windows Phone 8.1 +
    
- iOS 7.1 oder höher
    
- Android 4 oder höher
    
- Windows 8.1\*
    
- Windows 8.1 RT\*
    
- Windows-10\*\*
    
- 10 Windows Mobile\*\*
    
\*Steuerung des Zugriffs für Geräte mit Windows 8.1 und Windows 8.1 RT ist auf Exchange ActiveSync beschränkt.
  
\*\*Erfordert das Gerät zu Azure Active Directory hinzugefügt werden und im mobilen Gerät-Verwaltungsdienst Ihrer Organisation registriert werden.
  
Wenn Personen in Ihrer Organisation auf mobilen Geräten, die durch die Verwaltung mobiler Geräte für Office 365 unterstützt werden verwenden, können Sie Exchange ActiveSync-app-Zugriff auf Office 365-e-Mail für diese Geräte zu Ihrer Organisation Daten sicherer machen blockieren möchten. Schritte für das Blockieren von Exchange ActiveSync: finden Sie unter [Device Access-Einstellungen verwalten](manage-device-access-settings.md).
  
## <a name="access-control-for-office-365-email-and-documents"></a>Zugriffssteuerung für Office 365-E-Mails und -Dokumente

Für die verschiedenen Typen von mobilen Geräten in der folgenden Tabelle die unterstützten apps fordert den Benutzer MDM für Office 365 anmelden, wobei es wird eine neue Mobilgerät-Management-Richtlinie, die auf das Gerät des Benutzers angewendet wird und der Benutzer noch nicht zuvor registriert das Gerät. Wenn das Gerät des Benutzers eine Richtlinie nicht erfüllen, je nachdem, wie Sie die Richtlinie eingerichtet, kann ein Benutzer den Zugriff auf Office 365-Ressourcen in diesen apps werden blockiert werden oder haben sie möglicherweise Zugriff, aber Office 365 meldet eine Richtlinie Verletzung.
  
||**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|
|:-----|:-----|:-----|:-----|
|**Exchange** <br/> Exchange ActiveSync umfasst integrierte e-Mail- und Drittanbieter-apps an, wie TouchDown, die Exchange ActiveSync-Version 14,1 oder höher verwenden.  <br/> |![Exchange ActiveSync-Symbol](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Exchange Mail Mobile (Symbol)](media/5b5312b4-3bfb-4fc7-84ff-d7ab21227c10.png)Exchange Mail  <br/> |![Exchange ActiveSync-Symbol](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![iPhone Mail Mobile (Symbol)](media/888bdc7a-8354-4013-a0b2-0d4432a9a92e.png)E-Mails  <br/> |![Exchange ActiveSync-Symbol](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Android-E-Mail (Symbol)](media/20b48492-4adc-40ce-99cf-1b47bd2b389d.png)E-Mail  <br/> |
|**Office** und **OneDrive for Business** <br/> |Keine unterstützte Apps  <br/> |![iPhone Outlook Mobile (Symbol)](media/6c63112d-c10c-4040-85cc-feeccc3dd424.png)Outlook  <br/> ![iPhone OneDrive Mobile (Symbol)](media/560ec187-82d9-4793-b72f-7ba595972bdc.png)OneDrive  <br/> ![iPhone Word Mobile (Symbol)](media/63a3a749-1f98-402f-b211-e46b9224b655.png)Word  <br/> ![iPhone Excel Mobile (Symbol)](media/5b8f62c0-96aa-4602-9ed8-f837bbf5fa9e.png)Excel  <br/> ![iPhone PowerPoint Mobile (Symbol)](media/17c02dca-f60a-4d13-a610-00d576a40943.png)PowerPoint  <br/> |**Auf Telefonen und Tablets** <br/> ![Android-Telefon und Tablet Outlook mobile-Symbol](media/ed2a813d-f481-46e0-acc9-6422f0d16072.png)Outlook  <br/> ![Android-Telefon OneDrive-mobile-Symbol](media/64855d02-1684-4795-b4c5-863860f18722.png)OneDrive  <br/> ![Android Word mobile-Symbol](media/f618fe83-b163-4680-b924-fcedc06ab4ba.png)Word  <br/> ![Android Excel mobile-Symbol](media/659c7a5f-5797-4b47-a776-4a0c8f784c89.png)Excel  <br/> ![Android PowerPoint mobile-Symbol](media/35b98bce-d7cb-40ce-87e3-07b9764207b1.png)PowerPoint  <br/> **Nur auf Telefonen:** <br/> ![Office Mobile-mobile-Symbol](media/1aa9e978-6eb2-40aa-82da-62fb79cee313.png)Office Mobile  <br/> |
   
> [!NOTE]
>  Unterstützung für iOS 7.1 und höheren Versionen umfasst iPhone und iPad-Geräten. > Verwaltung von BlackBerry-Geräte wird durch Verwaltung mobiler Geräte für Office 365 nicht unterstützt. Verwenden Sie BlackBerry Business Cloud Services (BBCS) von BlackBerry zum Verwalten von BlackBerry-Geräte. > Benutzer werden nicht aufgefordert, registrieren und wird nicht blockiert oder Verletzung der Richtlinie gemeldet, wenn sie Office 365 SharePoint-Websites, Dokumente in Office Online, oder e-Mail in Outlook Web App Zugriff auf den mobilen Browser verwenden. 
  
Das folgende Diagramm zeigt, was geschieht, wenn ein Benutzer durch ein neues Gerät zu einer app anmeldet, unterstützt für Office 365-Steuerelement mit MDM zugreifen. Der Benutzer wird verhindert, dass Sie den Zugriff auf Office 365-Ressourcen in der app, bis sie ihr Gerät registrieren.
  
![Zeigt Registrierungsvorgang für neue Geräte.](media/O365-MDM-Capabilities-EnrollmentExample.png)
  
> [!NOTE]
> Richtlinien und Zugriffsregeln für Office 365 in MDM erstellt werden Exchange ActiveSync-Postfachrichtlinien für mobile Geräte und in der Exchange-Verwaltungskonsole erstellt gerätezugriffsregeln außer Kraft setzen. Nachdem ein Gerät für Office 365, alle Exchange ActiveSync-Postfachrichtlinie Mobilgerät MDM registriert ist oder gerätezugriffsregel angewendet auf das Gerät wird ignoriert. Weitere Informationen zu Exchange ActiveSync finden Sie unter [Exchange ActiveSync in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="policy-settings-for-mobile-devices"></a>Richtlinieneinstellungen für mobile Geräte

Wenn Sie eine Richtlinie zum Blockieren des Zugriffs mit bestimmten Einstellungen eingeschaltet erstellen, werden Benutzer blockiert den Zugriff auf Office 365-Ressourcen, wenn Sie eine unterstützte app verwenden, die in der [Steuerung des Zugriffs für Office 365-e-Mail und Dokumente](#access-control-for-office-365-email-and-documents)aufgeführt wird. Die Einstellungen, die Benutzern den Zugriff auf Office 365-Ressourcen blockieren sind in den folgenden Abschnitten:
  
- Sicherheit
    
- Verschlüsselung
    
- Jailbroken
    
- Verwaltetes E-Mail-Profil
    
Im folgende Diagramm wird beispielsweise was geschieht, wenn ein Benutzer mit einem registrierten Gerät kompatibel mit einer sicherheitseinstellung in eine Richtlinie zur Verwaltung von mobilen Gerät nicht zur Verfügung, die auf ihrem Gerät angewendet wird. Der Benutzer meldet sich bei einer app unterstützt für Office 365-Steuerelement mit MDM zugreifen. Sie werden blockiert den Zugriff auf Office 365-Ressourcen in der app, bis ihr Gerät die Sicherheitsstufe entspricht.
  
![Zeigt an, dass Benutzer blockiert wird, wenn Gerät nicht kompatibel ist.](media/O365-MDM-Capabilities-ComplianceExample.png)
  
In den folgenden Abschnitten werden die aufgeführt, die Sie verwenden können, hausärzten und Verwaltung von mobilen Geräten, die mit Office 365-Ressourcen Ihrer Organisation verbunden. 
  
### <a name="security-settings"></a>Sicherheitseinstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Kennwort anfordern  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Einfaches Kennwort verhindern  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Alphanumerisches Kennwort anfordern  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Minimale Kennwortlänge  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Anzahl von Anmeldefehlern, bevor die Gerätedaten gelöscht werden  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Minuten der Inaktivität, bevor das Gerät gesperrt wird  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Kennwortablauf (Tage)  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Kennwortverlauf verfolgen und Wiederverwendung verhindern  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="encryption-settings"></a>Verschlüsselungseinstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Datenverschlüsselung auf Geräten anfordern  <br/> |Windows Phone 8.1 ist bereits verschlüsselt, und die Verschlüsselung kann nicht rückgängig gemacht werden.  <br/> |✖  <br/> |✔  <br/> |✔\*  <br/> |
   
\*Mit Samsung Knox können Sie auch auf Speicherkarten Verschlüsselung aus.
  
### <a name="jail-broken-setting"></a>Jailbroken-Einstellung

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Gerät muss ohne Jailbreak und ohne Rootzugriff sein  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="managed-email-profile-option"></a>Verwaltetes E-Mail-Profil

Die folgende Option kann blockieren, Benutzern den Zugriff auf ihre Office 365-e-Mail, wenn sie einer manuell erstellten e-Mail-Profil verwenden. Benutzer auf iOS-Geräte müssen ihre manuell erstellten e-Mail-Profil löschen, bevor sie ihre e-Mails zugreifen können. Nachdem sie das Profil gelöscht haben, wird ein neues Profil automatisch auf dem Gerät erstellt werden.
  
|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|E-Mail-Profil wird verwaltet  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="cloud-settings"></a>Cloud-Einstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Verschlüsselte Sicherung anfordern  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Cloudsicherung blockieren  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Dokumentsynchronisierung blockieren  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Fotosynchronisierung blockieren  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Google Sicherung  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |✖  <br/> |✔  <br/> |
|Google-Konto automatische Synchronisierung zulassen  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="system-settings"></a>Systemeinstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Screenshots blockieren  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Senden von Diagnosedaten vom Gerät aus blockieren  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="application-settings"></a>Anwendungseinstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Videokonferenzen auf Gerät blockieren  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Zugriff auf Anwendungsspeicher blockieren  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Kennwort beim Zugriff auf Anwendungsspeicher anfordern  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="device-capabilities-settings"></a>Gerätefunktionseinstellungen

|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 und höher**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Verbindung mit Wechselmedien blockieren  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|Bluetooth-Verbindung blockieren  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="additional-settings"></a>Zusätzliche Einstellungen

Sie können die folgenden zusätzlichen Richtlinieneinstellungen mithilfe von PowerShell-Cmdlets festlegen. Weitere Informationen finden Sie unter [Sicherheit in Office 365 &amp; Compliance Center Cmdlets](https://go.microsoft.com/fwlink/p/?LinkId=827804).
  
|**Name der Einstellung**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 + (einschließlich Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|CameraEnabled  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|RegionRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MoviesRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|TVShowsRating  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AppsRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceDialing  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceAssistant  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowAssistantWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowPassbookWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MaxPasswordGracePeriod  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|PasswordQuality  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|SystemSecurityTLS  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|WLANEnabled  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="settings-supported-by-windows"></a>Einstellungen von Windows unterstützt werden

Sie können Windows 8.1 und Windows 10 Geräte Registrieren von als mobilen Geräten verwalten. Nach der Bereitstellung einer Richtlinie für den entsprechenden Benutzer mit Windows 8.1 RT und Windows 10 RT-Geräte müssen Sie registrieren bei MDM für Office 365 beim ersten sie die integrierte-e-Mail-app verwenden, um ihre Office 365-e-Mail zuzugreifen. 
  
Die folgenden Einstellungen sind für Windows 8.1 und Windows-10-Geräte unterstützt, die als mobile Geräte registriert sind. Diese Einstellung blockieren nicht Benutzern den Zugriff auf Office 365-Ressourcen.
  
 **Sicherheitseinstellungen**
  
- Alphanumerisches Kennwort anfordern
    
- Minimale Kennwortlänge
    
- Anzahl von Anmeldefehlern, bevor die Gerätedaten gelöscht werden
    
- Minuten der Inaktivität, bevor das Gerät gesperrt wird
    
- Kennwortablauf (Tage)
    
- Kennwortverlauf verfolgen und Wiederverwendung verhindern
    
 **Systemeinstellungen**
  
Senden von Diagnosedaten vom Gerät aus blockieren
  
 **Zusätzliche Einstellungen**
  
Sie können die folgenden zusätzlichen Richtlinieneinstellungen mithilfe von PowerShell-Cmdlets festlegen:
  
- AllowConvenienceLogon
    
- UserAccountControlStatus
    
- FirewallStatus
    
- AutoUpdateStatus
    
- AntiVirusStatus
    
- AntiVirusSignatureStatus
    
- SmartScreenEnabled
    
- WorkFoldersSyncUrl
    
## <a name="remotely-wipe-a-mobile-device"></a>Mobiles Gerät per Remotezugriff zurücksetzen

 Ist ein Gerät verlorenen oder gestohlenen, entfernen Sie vertrauliche Unternehmensdaten und Zugriff auf Office 365-Ressourcen Ihrer Organisation zu verhindern, indem Sie wie folgt eine Bereinigung aus **Sicherheit Hilfe &amp; Compliance Center\>Verhinderung von Datenverlust\>Gerät Management**. Sie können eine selektive Remotegerätzurücksetzung nur Unternehmensdaten entfernen oder eine vollständige Remotegerätzurücksetzung alle Daten von einem Gerät löschen und Wiederherstellen auf ihre Factory Einstellungen vornehmen.
  
Weitere Informationen finden Sie unter [Löschen ein mobiles Geräts in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518157).
  
## <a name="see-also"></a>Siehe auch

[Übersicht der mobilen Geräteverwaltung für Office 365](overview-of-mdm.md)
  
[Erstellen und Bereitstellen von Gerätesicherheitsrichtlinien](create-device-security-policies.md)


---
title: Festlegen von Mobile Device Management (MDM) in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: Die integrierte Verwaltung mobiler Geräte für Office 365 erleichtert die Sicherung und Verwaltung von mobilen Geräten wie iPhones, iPads, sonst noch, der Ihre Benutzer und Windows-Telefonen. Sie zunächst folgendermaßen Sie vor, um zu aktivieren und Verwaltung mobiler Geräte für Office 365 einrichten.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272360"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a>Festlegen von Mobile Device Management (MDM) in Office 365

Die integrierte Mobile Device Management (MDM) für Office 365 erleichtert die Sicherung und Verwaltung von mobilen Geräten wie iPhones, iPads, sonst noch, der Ihre Benutzer und Windows-Telefonen. Sie können erstellen und Verwalten von Sicherheitsrichtlinien für Geräte, Remote ein Gerät und detaillierte Device Berichte anzeigen.
  
Haben Sie Fragen? Wir haben [eine – häufig gestellte Fragen zu häufig gestellten Fragen Adresse](frequently-asked-questions-about-mdm.md)zusammengestellt. Beachten Sie, dass Sie nicht verwenden können eine [Partner: Angebot delegierte Administration](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) Verwaltung mobiler Geräte für Office 365 verwalten. 
  
Gerätemanagement ist Bestandteil der Sicherheit &amp; Compliance Center, Sie es Gehe um zu deaktiviert MDM Setup zu starten müssen.
  
Um die Verwaltung mobiler Geräte für Office 365 Sie einrichten müssen:
  
1. [Aktivieren Sie den Mobile Gerät-Verwaltungsdienst](#activate-the-mobile-device-management-service)  
2. [Einrichten von Verwaltung mobiler Geräte](#set-up-mobile-device-management)
3. [Stellen Sie sicher, dass Benutzer ihren Geräten registrieren](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a>Aktivieren Sie den Mobile Gerät-Verwaltungsdienst

1. Melden Sie sich mit Ihrem Geschäfts- oder Schulkonto bei Office 365 an. 
    
2. Wechseln Sie zu [Sicherheit &amp; Compliance Center](https://protection.office.com).
    
3. Navigieren Sie zur **Verhinderung von Datenverlust** \> **Gerätemanagement** und klicken Sie auf zum Deaktivieren der Aktivierungsprozess loszulegen **steigen** . 
    
    ![Verwaltung mobiler Geräte für Office 365 einrichten](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. Wir erstellt eine Standardsicherheitsrichtlinie für Sie, die Ihnen den Einstieg zu unterstützen. Aktualisieren Sie den Namen der Codezugriffssicherheits-Richtlinie auf dieser Seite, und klicken Sie dann auf **Setup zu starten**.
    
    ![Verwaltung mobiler Geräte Codezugriffssicherheits-Richtlinie festlegen](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. Der Setup-Bildschirm wird angezeigt, die Fortschritt anzeigt, auf den Dienst einrichten.
    
    ![Status der MDM-Installation](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> Sie können auch **MDM Setup** per Suche suchen. Im Office 365 Administrationscenter \> **Homepage der Verwaltung von mobilen Geräten Typ in das Feld **Suchen** ** . > ![Suche für die Verwaltung von mobilen Geräten in der Verwaltungskonsole](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)
  
Kann es einige Zeit zum Aktivieren der Verwaltung mobiler Geräte für Office 365 dauern, aber wenn er abgeschlossen ist, erhalten Sie eine e-Mail, die die nächsten Schritte erläutert.
  
## <a name="set-up-mobile-device-management"></a>Einrichten von Verwaltung mobiler Geräte

Wenn der Dienst bereit ist, führen Sie die folgenden vier Schritte aus, um das Setup abzuschließen. Möglicherweise müssen Sie [Einstellungen verwalten](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) klicken Sie auf der Seite **Verwaltung von Geräten** in die Sicherheit auf &amp; Compliance Center, um die folgenden Einstellungen finden Sie unter. 
  
![Richten Sie die Verwaltung von mobilen Geräten erforderlich und empfohlene Schritte](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a>Schritt 1: (Erforderlich) Configure Domänen für MDM

Wenn Sie nicht über eine benutzerdefinierte Domäne ist, die mit Office 365 verfügen oder wenn Sie keine Windows-Geräte verwalten, können Sie diesen Abschnitt überspringen. Andernfalls müssen Sie die DNS-Einträge für die Domäne an Ihrem DNS-Host hinzufügen. Wenn Sie die Datensätze im Rahmen der Einrichtung Ihrer Domäne mit Office 365 bereits hinzugefügt haben, sind Sie alle festlegen. Nach dem Sie Datensätze hinzufügen, werden Office 365-Benutzer in Ihrer Organisation, die auf ihrem Windows-Gerät mit einer e-Mail-Adresse anmelden, die Ihre benutzerdefinierte Domäne verwendet, um in MDM für Office 365 registrieren umgeleitet.
  
Benötigen Sie Hilfe beim Einrichten der Datensätze? Suchen Sie nach Ihrer domänenregistrierungsstelle in der Liste [Erstellen von DNS-Einträge für Office 365 beim Verwalten Ihrer DNS-Einträge](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) , und wählen Sie den Namen der Registrierungsstelle fahren Sie mit Schritt für Schritt Hilfe zum Erstellen von DNS-Einträgen. Verwenden Sie diese Anweisungen, um die folgenden beiden Einträge hinzuzufügen: 
  
|**Hostname**|**Eintragstyp**|**Adresse**|**TTL**|
|:-----|:-----|:-----|:-----|
|EnterpriseEnrollment  <br/> |CNAME  <br/> |EnterpriseEnrollment.manage.microsoft.com  <br/> |3600  <br/> |
|EnterpriseRegistration  <br/> |CNAME  <br/> |EnterpriseRegistration.windows.net  <br/> |3600  <br/> |
   
Nachdem Sie die beiden Datensätze hinzugefügt haben, gehen Sie zurück, für die Sicherheit &amp; Compliance Center und navigieren Sie zur **Verwaltung von Geräten** \> **Einstellungen verwalten** für die Durchführung den nächsten Schritt. 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a>Schritt 2: (Erforderlich) Konfigurieren eines Zertifikats APNs für iOS-Geräte

Zum Verwalten von iOS-Geräte wie iPad und iPhones müssen Sie ein Zertifikat APNs erstellen.
  
Zu diesem Zweck führen Sie die Schritte über das **Einrichten von** Links auf der **Setup-Verwaltungsseite mobilen Gerät**.
  
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
    
APN Zertifikat hinzugefügt haben, gehen Sie zurück, um die Sicherheit &amp; Compliance Center und navigieren Sie zur **Verwaltung von Geräten** \> **Einstellungen verwalten** für die Durchführung den nächsten Schritt. 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a>Schritt 3: (Empfohlen) richten Sie mehrstufige Authentifizierung

Wenn Sie mehrstufige Authentifizierung (mehrstufiger Authentifizierung das) unter **empfohlene Schritte**nicht angezeigt wird, können Sie diesen Abschnitt überspringen. Wenn diese Option aufgeführt ist, wird empfohlen, dass Sie mehrstufiger Authentifizierung das im Azure AD-Portal auf die Sicherheit der Verwaltung mobiler Geräte für Office 365-Registrierungsprozess zu aktivieren. Es ist standardmäßig deaktiviert.
  
Mehrstufiger Authentifizierung das hilft bei der Anmeldung an Office 365 für die Registrierung des mobilen Geräts zu sichern, indem Sie eine zweite Form der Authentifizierung erfordern. Benutzer werden benötigt, um ein Telefonanruf, eine Textnachricht oder eine app-Benachrichtigung auf ihrem mobilen Gerät nach dem eingeben ordnungsgemäß ihre Arbeit Kontokennwort zu bestätigen. Sie können ihr Gerät nur registrieren, nach diesem zweiten Form der Authentifizierung abgeschlossen ist. Nachdem in Verwaltung mobiler Geräte Geräten der Benutzer für Office 365 registriert sind, können Benutzer Office 365-Ressourcen mit nur ihre Arbeit-Konto zugreifen.
  
Wählen Sie neben die **mehrstufige Authentifizierung eingerichtet haben** **Einrichten**. Um erfahren Sie, wie Sie mehrstufiger Authentifizierung das im Azure AD-Portal aktivieren, finden Sie unter [Einrichten von Multi-Factor Authentication](https://go.microsoft.com/fwlink/p/?LinkId=519255).
  
Nachdem Sie mehrstufiger Authentifizierung das eingerichtet haben, gehen Sie zurück, für die Sicherheit &amp; Compliance Center und navigieren Sie zur **Verwaltung von Geräten** \> **Einstellungen verwalten** für die Durchführung den nächsten Schritt. 
  
### <a name="step-4-recommended-manage-device-security-policies"></a>Schritt 4: Verwalten (empfohlen) Sicherheitsrichtlinien für Geräte

Im nächste Schritt wird das Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte zum Schutz von Daten der Office 365-Organisation. Sie können beispielsweise zur Verhinderung von Datenverlust, wenn ein Benutzer ihr Gerät durch Erstellen einer Richtlinie für die Geräte sperren nach 5 Minuten der Inaktivität verliert und Geräten nach 3 Fehlschlägen Kennworteingaben gelöscht.
  
In der **Sicherheit &amp; Compliance Center**, wechseln Sie zu **Sicherheitsrichtlinien** \> **Sicherheitsrichtlinien für Geräte** erstellen Gerät Sicherheitsrichtlinien und Zugriffsregeln. 
  
![Fügen Sie eine Gerät Codezugriffssicherheits-Richtlinie](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
Schritt-für-Schritt-Anleitung zum Erstellen einer neuen Richtlinie, finden Sie unter [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](create-device-security-policies.md).
  
> [!TIP]
>  Wenn Sie eine neue Richtlinie erstellen, können Sie Zugriff und Bericht Richtlinie Verletzung ermöglichen, auf dem eines Benutzers ist Gerät nicht kompatibel mit der Richtlinie für die Richtlinie festlegen möchten. Auf diese Weise können Sie sehen, wie viele mobile Geräte durch die Richtlinie ohne Blockieren des Zugriffs auf Office 365 auswirkt. > Bevor Sie eine neue Richtlinie für alle Benutzer in Ihrer Organisation bereitstellen, wird empfohlen, dass Sie auch auf die von einer kleinen Anzahl von Benutzern verwendeten Geräte testen. > Vor der Bereitstellung von Richtlinien können Sie darüber hinaus Ihre Organisation die potenziellen Auswirkungen Registrieren eines Geräts in MDM für Office 365 kennen. Je nachdem, wie Sie die Richtlinien einrichten konnte Geräte, die mit diesen (nicht kompatible Geräte) entsprechen nicht verhindert werden, dass Sie den Zugriff auf Office 365. Nicht kompatible Geräte möglicherweise auch apps installiert, Fotos und andere persönliche Informationen, die auf einem Gerät registrierten, wenn das Gerät bereinigt wird gelöscht werden konnte. Weitere Informationen: [Löschen ein mobiles Geräts in Office 365](wipe-a-mobile-device.md). 
  
## <a name="make-sure-users-enroll-their-devices"></a>Stellen Sie sicher, dass Benutzer ihren Geräten registrieren

Nachdem Sie erstellt und eine Richtlinie zur Verwaltung von mobilen Gerät bereitgestellt haben, erhält jeden lizenzierter Office 365-Benutzer in Ihrer Organisation, die für die Geräterichtlinie gilt eine e-Mail das nächste Mal, den, das Sie bei Office 365 auf ihrem mobilen Gerät anmelden. Sie müssen die Registrierung und Aktivierung Schritte ausführen, bevor sie Office 365-e-Mails und Dokumente zugreifen können. Finden Sie unter [Ihrem mobilen Gerät für die Arbeit oder Schule registrieren](enroll-your-mobile-device.md).
  
> [!IMPORTANT]
> Wenn die bevorzugte Sprache des Benutzers von der Registrierungsprozess nicht unterstützt wird, erhalten Benutzer Registrierung Benachrichtigung und Schritte auf ihren mobilen Geräten in einer anderen Sprache. Nicht alle Sprachen in Office 365 unterstützt werden derzeit für den Registrierungsprozess auf mobilen Geräten unterstützt. 
  
Benutzer mit Android oder iOS-Geräte sind so installieren Sie die app Unternehmensportal im Rahmen der Registrierung erforderlich.
  
## <a name="related-topics"></a>Verwandte Themen

[Funktionen der Verwaltung von mobilen Geräten](capabilities-of-mobile-device-management.md)
  
[Erstellen und Bereitstellen von Gerätesicherheitsrichtlinien](create-device-security-policies.md)
  


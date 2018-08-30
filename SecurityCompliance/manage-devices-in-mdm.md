---
title: Verwalten von Geräten in Verwaltung mobiler Geräte in Office 365 registriert
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
- MBS150
- MET150
ms.assetid: 28dd276b-beeb-4c5b-8b22-7551186127fe
description: Führen Sie diese Schritte zum Festlegen von Mobile Device Management (MDM) in Office 365.
ms.openlocfilehash: 3a84b6904b866e07eb4efabe0f39041b282d0ba9
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272310"
---
# <a name="manage-devices-enrolled-in-mobile-device-management-in-office-365"></a>Verwalten von Geräten in Verwaltung mobiler Geräte in Office 365 registriert

Die integrierte Verwaltung mobiler Geräte für Office 365 erleichtert die Sicherung und Verwaltung von mobilen Geräten wie iPhones, iPads, sonst noch, der Ihre Benutzer und Windows-Telefonen. Der erste Schritt besteht darin zu Office 365 und [Einrichten von MDM für Office 365](set-up-mobile-device-management.md)anmelden. 
  
Nachdem Sie es, die Personen in Ihrer Organisation eingerichtet haben müssen im Dienst [ihren Geräten zu registrieren](enroll-your-mobile-device.md) . Anschließend können Sie MDM für Office 365 verwenden, zur Verwaltung der Geräte in Ihrer Organisation. Beispielsweise können Sie Sicherheitsrichtlinien für Geräte zu beschränken, e-Mail-Zugriff oder andere Dienste, Geräte Berichte anzeigen und Remote Wischen ein Gerät verwenden. Gehen Sie in der Regel auf der [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) für diese Aufgaben. 
  
## <a name="device-management-tasks"></a>Geräteverwaltungsaufgaben

Gehen Sie folgendermaßen vor, um das Gerät VA anzuzeigen. 
  
1. Navigieren Sie zum Office 365 Admin Center.
    
2. Geben Sie Verwaltung mobiler Geräte in das Suchfeld ein, und wählen Sie **Verwaltung mobiler Geräte** aus der Liste der Ergebnisse. 
    
    ![Typ Mobile Geräte-Manager in der Office 365-Suchfeld](media/e2e2f1c0-e543-431a-959b-e26c2ba328a7.png)
  
Nachdem Sie MDM für Office 365 eingerichtet haben, wird hier wie Sie die mobilen Geräte in Ihrer Organisation verwalten können. 
  
|**Hierzu...**|**Aktion...**|
|:-----|:-----|
|Zurücksetzen eines Geräts  <br/> |Wählen Sie in der Systemsteuerung Gerätemanagement *Gerätename* , dann **vollständige Remotegerätzurücksetzung** zum Löschen aller Informationen oder **selektive Wischen** , um nur Organisationsinformationen auf dem Gerät zu löschen.  <br/> Finden Sie [ein Gerät in Office 365](wipe-a-mobile-device.md).  <br/> |
|Blockieren des Zugriffs auf Exchange-E-Mail für nicht unterstützte Geräte unter Verwendung von Exchange ActiveSync  <br/> |Wählen Sie in der Systemsteuerung Gerätemanagement **Block**.  <br/> |
|Einrichten von Richtlinien für Geräte wie kennwortanforderungen und Sicherheitseinstellungen  <br/> |Klicken Sie in der Systemsteuerung Gerätemanagement auf \> **Sicherheitsrichtlinien für Geräte** \> **Hinzufügen +**.  <br/> Finden Sie unter [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](create-device-security-policies.md).  <br/> |
|Anzeigen des Liste blockierter Geräte  <br/> |Wählen Sie in der Systemsteuerung Gerätemanagement unter **Wählen Sie eine Ansicht** **blockiert**aus.  <br/> ||
|Entsperren eines nicht kompatiblen oder nicht unterstützten Geräts für einen Benutzer oder eine Benutzergruppe  <br/> | Nicht kompatible Geräte auf unterschiedliche Weise entsperren Sie je nach Ihrer Situation. Wählen Sie eine der folgenden:<br/>  Entfernen Sie den oder die Benutzer aus der Sicherheitsgruppe, die, der auf die Richtlinie angewendet wurde. Wechseln Sie zu **Office 365 Administrationscenter** \> **Gruppen**, und wählen Sie dann * Gruppenname *. Klicken Sie auf **Bearbeiten, Elemente und Administratoren**.<br/>  Entfernen der Sicherheitsgruppe, die die Benutzer ein Mitglied aus der Geräterichtlinie sind. Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Sicherheitsrichtlinien für Geräte**. Wählen Sie * Richtlinie Gerätename *, klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **Bereitstellung**.<br/>  Aufheben der Blockierung von allen nicht konformer Geräten für eine Geräterichtlinie. Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Sicherheitsrichtlinien für Geräte**. Wählen Sie *Richtlinie Gerätenamen* , und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **für Access**. Wählen Sie **Access und Bericht Verletzung zulassen**.<br/>  Wechseln Sie zum Aufheben der Blockierung von einem Gerät nicht konformer oder nicht unterstützte für einen Benutzer oder eine Gruppe von Benutzern auf Gehe zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Gerätemanagement** \> **Gerätezugriffs verwalten-Einstellungen **. Fügen Sie eine Sicherheitsgruppe mit den Mitgliedern, den, die Sie ausschließen verhindern möchten, den Zugriff auf Office 365 blockiert. Finden Sie unter [erstellen, bearbeiten oder Löschen einer Sicherheitsgruppe in Office 365 Administrationscenter](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> |
|Anzeigen von Details zu den Geräten in Ihrer Organisation  <br/> |Befolgen Sie die Schritte in [erhalten Sie Informationen zu Geräten von MDM verwaltet werden](get-details-about-mdm-managed-devices.md), um Details zu erhalten, beispielsweise, die welche Geräte registrierten und Einhaltung der Sicherheitsrichtlinien für Geräte wurden.  <br/> |
|Entfernen von Benutzern, damit ihre Geräte von MDM nicht mehr verwaltet werden  <br/> |Bearbeiten der Sicherheitsgruppe über Gerät Informationsverwaltungsrichtlinien für MDM an den Benutzer zu entfernen. Finden Sie unter [erstellen, bearbeiten oder Löschen einer Sicherheitsgruppe in Office 365 Administrationscenter](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> Um MDM aus Ihrer Office 365-Benutzer zu entfernen, finden Sie unter [Verwaltung mobiler Geräte in Office 365 deaktivieren](turn-off-mdm.md).  <br/> |
   


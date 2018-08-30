---
title: Zum Deaktivieren der Verwaltung mobiler Geräte in Office 365
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
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Führen Sie diese Schritte, um beenden MDM Richtlinien für mobile Geräte in Office 365-Organisation erzwungen wird.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272220"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a>Zum Deaktivieren der Verwaltung mobiler Geräte in Office 365

Um effektiv MDM für Office 365 deaktivieren, Personengruppen (definiert durch Sicherheitsgruppen) aus der Informationsverwaltungsrichtlinien Gerät entfernen oder die Richtlinien selbst zu entfernen. 
  
- Entfernen Sie Gruppen von Benutzern durch Entfernen von Benutzersicherheitsgruppen aus der Richtlinien für Geräte, die Sie erstellt haben. 
    
- Deaktivieren Sie MDM für alle Benutzer, indem Sie alle MDM Geräterichtlinien entfernen. 
    
Diese Optionen werden MDM Erzwingung für Geräte in Ihrer Organisation entfernt. Leider können nicht Sie einfach "aufheben" MDM für Office 365 Nachdem Sie es eingerichtet haben.
  
> [!IMPORTANT]
> Achten Sie auf die Auswirkung auf Benutzercomputern, wenn Sie Benutzersicherheitsgruppen aus Richtlinien entfernen oder die Richtlinien selbst zu entfernen. Beispielsweise e-Mail-Profile und Cache-e-Mails können entfernt werden je nach dem Gerät. Weitere Informationen: [Was ist die Auswirkung von Sicherheitsrichtlinien auf anderes Gerätetypen?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a>Entfernen von Benutzersicherheitsgruppen aus MDM Geräterichtlinien

1. Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Verhinderung von Datenverlust** \> **Gerät Sicherheitsrichtlinien**.
    
2. Wählen Sie eine Richtlinie für Geräte aus, und klicken Sie auf ![Bearbeitungssymbol](media/O365-MDM-CreatePolicy-EditIcon.gif) **Richtlinie bearbeiten**.
    
3. Klicken Sie unter **Bereitstellung**auf **- Entfernen**.
    
    Wählen Sie unter **Gruppen**die eine Sicherheitsgruppe aus.
    
4.  Klicken Sie auf **Entfernen**.
    
5. Klicken Sie auf **Speichern**.
    
## <a name="remove-mdm-device-policies"></a>Entfernen von MDM Geräterichtlinien

1. Wechseln Sie zu **Sicherheit &amp; Compliance Center** \> **Sicherheitsrichtlinien** \> **Sicherheitsrichtlinien für Geräte**.
    
2. Wählen Sie eine Richtlinie für Geräte aus, und klicken Sie dann auf ![Bild von den Papierkorb können Symbol. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Richtlinie zu löschen**.
    
3. Klicken Sie im Dialogfeld **Warnung** auf **Ja**. 
    


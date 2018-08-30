---
title: Löschen eines mobilen Geräts in Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Verwaltung für Office 365 integrierten mobiler Geräte können eine selektive Remotegerätzurücksetzung nur Informationen der Organisation zu entfernen, oder eine vollständige Remotegerätzurücksetzung alle Daten von einem mobilen Gerät löschen und Wiederherstellen auf ihre Factory Einstellungen.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272500"
---
# <a name="wipe-a-mobile-device-in-office-365"></a>Löschen eines mobilen Geräts in Office 365
  
Verwaltung für Office 365 integrierten mobiler Geräte können eine selektive Remotegerätzurücksetzung nur Informationen der Organisation zu entfernen, oder eine vollständige Remotegerätzurücksetzung alle Daten von einem mobilen Gerät löschen und Wiederherstellen auf ihre Factory Einstellungen.
  
## <a name="what-to-know-before-you-begin"></a>Was Sie wissen, bevor Sie beginnen

- Mobile Geräte können vertrauliche Organisationsinformationen gespeichert und gewähren Sie Zugriff auf Office 365-Ressourcen Ihrer Organisation. Zum Schutz Ihrer Organisation Informationen können Sie eine vollständige Remotegerätzurücksetzung oder eine selektive Wischen ausführen:
    
  - **Vollständige Remotegerätzurücksetzung**: Löscht alle Daten auf dem Mobilgerät eines Benutzers, einschließlich der installierten Programme, Fotos und persönliche Informationen. Wenn der Löschvorgang abgeschlossen ist, wird das Gerät auf ihre Einstellungen Factory wiederhergestellt. 
    
  - **Selektive Wischen**: Unternehmensdaten und Blätter installiert Applications, Fotos und persönlichen Informationen auf dem mobilen Gerät des Benutzers entfernt. 
    
- Wenn ein Gerät (vollständige Remotegerätzurücksetzung oder selektive Remotegerätzurücksetzung) gelöscht wird, wird das Gerät aus der Liste der verwalteten Geräten entfernt.
    
- Sie können richten Sie eine Richtlinie zur Verwaltung von mobilen Gerät, die automatisch (vollständige Wischen) Löscht ein Gerät, nachdem der Benutzer erfolglos versucht, das Gerät Kennwort eingeben eine bestimmte Anzahl von Malen. Führen Sie die Schritte in [Erstellen und Bereitstellen von Sicherheitsrichtlinien für Geräte](create-device-security-policies.md).
    
- Wenn Sie wissen, was ein Benutzer treten, wenn Sie ihr Gerät Wischen möchten, finden Sie unter [Was ist der Benutzer und Gerät Auswirkungen?](wipe-a-mobile-device.md#BKMK_Impact).
    
## <a name="wipe-a-mobile-device"></a>Löschen eines mobilen Geräts

1. Wechseln Sie zu der [ ![klicken Sie hier, um zu Office 365 Administrationscenter zu wechseln.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).

2. Wechseln Sie zu [Wechseln Sie zu der Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **Verhinderung von Datenverlust** \> **Gerätemanagement**.
    
3. Wählen Sie das Gerät, den, das Sie löschen möchten.
    
4. Wählen Sie den Typ des Remotezurücksetzung Sie tun möchten.
    
  - Führen Sie eine selektive Remotegerätzurücksetzung und Löschen nur Office 365-Organisation die Informationen im rechten Bereich, wählen Sie **selektive Wischen**.
    
  - Wählen Sie zum Ausführen einer vollständigen Remotegerätzurücksetzung und Wiederherstellen von das Gerät auf ihre Factory Einstellungen, die im rechten Bereich in **vollständige Remotegerätzurücksetzung**aus.
    
![Wählen Sie ein Gerät, und wählen Sie dann die Remotegerätzurücksetzung ausführen.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. Wählen Sie **Ja,** um zu bestätigen. 
    
Bis der Löschvorgang abgeschlossen ist, wird der **Status des** als **RetirePending** oder **RetireIssued**angezeigt.
  
### <a name="how-do-i-know-it-worked"></a>Wissen ich, dass es funktioniert?

Das mobile Gerät in der Liste der verwalteten Geräten wird nicht mehr angezeigt.
  
## <a name="why-would-you-want-to-wipe-a-device"></a>Warum sollten Sie ein Gerät Wischen?

Es gibt verschiedene Gründe für verlorener Geräte:
  
- Mobile Geräte wie Smartphones und Tablets werden Funktionsumfang immer immer. Dies bedeutet, dass für Ihre Benutzer zum Speichern von vertraulichen Unternehmensinformationen (beispielsweise persönliche Identifikationsnummer oder vertraulich Communications) und darauf zugreifen, unterwegs ist es einfacher. Wenn eines dieser mobilen Geräte Verlust oder Diebstahl, kann das Gerät sofort verlorener Hilfe verhindern, dass Ihre Organisation Informationen beziehen, die in die falschen Hände.
    
- Wenn ein Benutzer die Organisation mit einem persönlichen Gerät die MDM für Office 365 registriert ist verlässt, helfen Ihnen Organisationsinformationen aus mit diesen Benutzern wechseln, indem Sie wie folgt eine selektive Remotegerätzurücksetzung zu verhindern.
    
- Wenn Ihre Organisation mobile Geräte für Benutzer bereitstellt, müssen Sie möglicherweise von Zeit zu Zeit zuzuweisende Geräte. Ausführen einer vollständigen Remotegerätzurücksetzung auf einem Gerät vor der Zuweisung zu einem neuen Benutzer unterstützt wird sichergestellt, dass vertraulicher Informationen aus der vorherigen Besitzer gelöscht wird.
    
## <a name="whats-the-user-and-device-impact"></a>Was ist der Benutzer und die Auswirkungen Gerät?

Der Löschvorgang wird sofort an das mobile Gerät gesendet. Das Gerät wird auch als nicht kompatibel in AAD gekennzeichnet.
  
In der folgenden Tabelle wird beschrieben, welche Inhalte für jede Art von Gerät entfernt wird, wenn ein Gerät selektiv Kennworteingaben gelöscht wird.
  
|**Inhalte Auswirkungen**|**Windows Phone 8.1**|**iOS 7.1+**|**Android 4 und höher**|
|:-----|:-----|:-----|:-----|
|Unternehmen Portal app\* wird deinstalliert.  <br/> |Nicht zutreffend  <br/> |✔  <br/> |Nicht zutreffend  <br/> |
|Office 365-app-Daten von apps, in dem Steuerung des Zugriffs von MDM für Office 365 unterstützt wird, gehostet werden entfernt (derzeit Outlook und OneDrive für Unternehmen). Die apps werden nicht entfernt.  <br/> Outlook für Android werden zwischengespeicherten-e-Mails nicht entfernt werden.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Aufgeführt, die von MDM für Office 365 für Geräte angewendet wurden, werden nicht mehr auf dem Gerät erzwungen, und Benutzer können die Einstellungen ändern.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|E-Mail-Profile von MDM für Office 365 werden entfernt, und zwischengespeicherte e-Mail auf dem Gerät wird gelöscht.  <br/> |Nicht zutreffend  <br/> |✔  <br/> |Nicht zutreffend  <br/> |
   
> [!NOTE]
> \*Unternehmen Portal app ist im App Store für iOS und die Wiedergabe-Speichers für Android-Geräte verfügbar. 
  
## <a name="related-content"></a>Verwandte Inhalte

[Verwalten von mobilen Geräten in Office 365](set-up-mobile-device-management.md)
  


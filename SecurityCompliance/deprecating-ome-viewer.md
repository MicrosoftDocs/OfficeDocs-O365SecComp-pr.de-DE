---
title: VerAltete Office 365 Message Encryption Viewer-App
ms.author: krowley
author: kccross
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6336cabb-b06e-402f-9e85-8bb9eb4ce68f
ms.collection:
- M365-security-compliance
description: Am 15. August 2018 werden wir die Office 365 Message Encryption (OM) Viewer Mobile App aus Android und Apple Stores entfernen. Die Mobile App für den Office 365-Nachrichten Verschlüsselungs Betrachter war zum Lesen von e-Mail-Nachrichten und Anlagen erforderlich, die mit der vorherigen Version von OM auf Apple-und Android-Telefonen verschlüsselt wurden. Abgesehen vom Entfernen der OM Viewer-App führen wir keine weiteren Änderungen an der vorherigen Version von OM aus.
ms.openlocfilehash: 82f28249e6b9911faea866f5a3574b635e45156c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256973"
---
# <a name="deprecating-office-365-message-encryption-viewer-app"></a>VerAltete Office 365 Message Encryption Viewer-App

Am 15. August 2018 entfernten wir die Office 365 Message Encryption (OM) Viewer Mobile App aus Android und Apple Stores. Die Mobile App für den Office 365-Nachrichten Verschlüsselungs Betrachter war zum Lesen von e-Mail-Nachrichten und Anlagen erforderlich, die mit der vorherigen Version von OM auf Apple-und Android-Telefonen verschlüsselt wurden. Abgesehen vom Entfernen der OM Viewer-App führen wir keine weiteren Änderungen an der vorherigen Version von OM aus.
  
## <a name="changes-from-august-2018"></a>Änderungen vom August 2018

Wie im September 2017 angekündigt, haben wir eine neue Version der [Office 365-Nachrichtenverschlüsselung](https://aka.ms/ome2017) veröffentlicht, damit Benutzer verschlüsselte und geschützte Nachrichten innerhalb oder außerhalb der Organisation senden können, ohne dass die Mobile App erforderlich ist. Seither wurden zusätzliche Funktionen hinzugefügt:
  
- [Nur verSchlüsselte Vorlage](https://aka.ms/encryptonly)

- [Steuerelement zum Entschlüsseln von Anlagen](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Admin-control-for-attachments-now-available-in-Office-365/ba-p/204007)
    
Mit dieser Änderung können Benutzer ab dem 1. August die Mobile App für den Office 365-Nachrichten Verschlüsselungs Betrachter nicht mehr herunterladen. Daher können e-Mail-Empfänger Nachrichten, die mit der vorherigen Version von OM verschlüsselt wurden, auf einigen Android-und Apple Mobile-Geräten möglicherweise nicht lesen. Sie können diese Nachrichten jedoch weiterhin auf PCs lesen (über Desktop Browser). Benutzer, die die APP bereits heruntergeladen haben, können Sie weiterhin verwenden.
  
## <a name="why-this-change-was-made"></a>Gründe für diese Änderung

Die neue Version von OM benötigt keine Mobile App mehr zum Lesen geschützter e-Mail-Nachrichten und Anlagen. Office 365-Kunden, die die neuen OM-Funktionen verwenden, können die geschützte Nachricht in Outlook Mobile-und nicht-Office 365-Kunden anzeigen, die geschützte Nachrichten in einem Browser anzeigen können.
  
Wenn Benutzer eine mobile app herunterladen müssen, ist dies eine weitere Hürde für Kunden zum Anzeigen geschützter Nachrichten. Die neuen Nachrichten Verschlüsselungsfunktionen von Office 365 bieten eine bessere mobile Umgebung.
  
## <a name="can-i-still-use-the-previous-version-of-office-365-message-encryption"></a>Kann ich weiterhin die frühere Version von Office 365-Nachrichtenverschlüsselung verwenden

Die frühere Version von Office 365 Nachrichtenverschlüsselung ist zu diesem Zeitpunkt nicht veraltet, jedoch haben wir wesentliche Verbesserungen an der neuen Version von Office 365-Nachrichtenverschlüsselung vorgenommen, die das Verschlüsseln und schützen von vertraulichen Daten für alle Benutzer vereinfacht. und auf jedem Gerät, einschließlich der Möglichkeit für Office 365-Benutzer, geschützte Nachrichten direkt in Outlook (Desktop, Mobil und Web) zu lesen. 
  
## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>Was muss ich tun, um diese Änderung vorzubereiten?

Wenn Ihre Organisation derzeit verschlüsselte Anlagen an Empfänger sendet, die die OM Viewer-App benötigen, sollten Sie Ihre Dokumentations-und Schulungsressourcen aktualisieren.
  
Es wird empfohlen, vorhandene Exchange-Nachrichtenfluss Regeln zu aktualisieren, um die aktuelle Version von OM zu verwenden, damit Ihre Organisation die neuen und verbesserten Funktionen nutzen kann. Nachdem Sie die neuen OM-Funktionen eingerichtet haben, benötigt der Empfänger die APP zum Lesen verschlüsselter Nachrichten auf mobilen Geräten nicht.
  
Microsoft empfiehlt, einen Plan für die Umstellung auf die neuen Funktionen von OM zu erstellen, sobald es für Ihre Organisation sinnvoll ist. Weitere Informationen finden Sie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md). Wenn Sie mehr über die Funktionsweise der neuen Funktionen erfahren möchten, lesen Sie [Office 365-Nachrichtenverschlüsselung](ome.md).
  


---
title: Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Damit S/MIME-geschützte Nachrichten versendet werden können, müssen die entsprechenden Zertifikate eingerichtet werden. Zum Senden von verschlüsselten Nachrichten über Exchange Online verwendet das E-Mail-Programm das öffentliche Zertifikat des Empfängers, um die Nachricht zu verschlüsseln. Dieses öffentliche X.509-Zertifikat muss in Office 365 veröffentlicht werden.
ms.openlocfilehash: 452b538b4515bdbcd5fcbdedad17f0450c04207a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002376"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME

Damit S/MIME-geschützte Nachrichten versendet werden können, müssen die entsprechenden Zertifikate eingerichtet werden. Zum Senden von verschlüsselten Nachrichten über Exchange Online verwendet das E-Mail-Programm das öffentliche Zertifikat des Empfängers, um die Nachricht zu verschlüsseln. Dieses öffentliche X.509-Zertifikat muss in Office 365 veröffentlicht werden.
  
## <a name="to-sync-certificates-that-support-smime"></a>So synchronisieren Sie Zertifikate, die S/MIME unterstützen

Richten Sie S/MIME ein, indem Sie Zertifikate ausgeben und diese in Ihrem lokalen Active Directory-Domänendienst veröffentlichen. Weitere Informationen zum Verwalten von Zertifikaten in Exchange 2013 finden Sie unter [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).
  
Nachdem Ihre Zertifikate veröffentlicht wurden, verwenden Sie Azure Active Directory-Synchronisierungstool, um Benutzerdaten aus der lokalen Exchange-Umgebung mit Office 365 zu synchronisieren. Weitere Informationen zu diesem Prozess finden Sie unter [DirSync: Versionsverlauf für das Verzeichnissynchronisierungstool](https://go.microsoft.com/fwlink/p/?LinkId=392587).
  
Zusammen mit anderen Verzeichnisdaten synchronisiert das Tool für S/MIME-Zwecke die Attribute  `userCertificate` und  `userSMIMECertificate` für jedes Benutzerobjekt, sodass die Daten verwendet werden können, um Nachrichten zu signieren und zu verschlüsseln. 
  
## <a name="more-information"></a>Weitere Informationen

[S/MIME für die Nachrichtensignierung und -verschlüsselung](s-mime-for-message-signing-and-encryption.md)
  
[Azure Active Directory-Synchronisierungstool](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  


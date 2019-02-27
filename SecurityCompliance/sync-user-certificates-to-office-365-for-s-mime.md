---
title: Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME
ms.author: chrisda
author: chrisda
manager: Serdars
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
ms.openlocfilehash: 35de3ba34be48a8553c7034f646576e4fca8b870
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30294998"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME

Bevor jeder S/MIME-geschützte Nachrichten in Exchange Online senden kann, müssen die entsprechenden Zertifikate eingerichtet werden. Um verschlüsselte Nachrichten über Exchange Online zu senden, verwendet die e-Mail-App des Absenders das öffentliche Zertifikat des Empfängers, um die Nachricht zu verschlüsseln. Dieses öffentliche X. 509-Zertifikat muss in Office 365 veröffentlicht werden.

## <a name="to-sync-certificates-that-support-smime"></a>So synchronisieren Sie Zertifikate, die S/MIME unterstützen

Beginnen Sie mit dem Einrichten von S/MIME, indem Sie Zertifikate ausgeben und Sie in Ihrem lokalen Active Directory-Domänendienst veröffentlichen. Weitere Informationen zum Verwalten von Zertifikaten in Exchange Server finden Sie unter [digitale Zertifikate und SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).

Nachdem Ihre Zertifikate veröffentlicht wurden, verwenden Sie Azure Active Directory-Synchronisierungstool, um Benutzerdaten aus der lokalen Exchange-Umgebung mit Office 365 zu synchronisieren. Weitere Informationen zu diesem Prozess finden Sie unter [DirSync: Versionsverlauf für das Verzeichnissynchronisierungstool](https://go.microsoft.com/fwlink/p/?LinkId=392587).

Zusammen mit der Synchronisierung anderer Verzeichnisdaten wird das Tool für S/MIME-Zwecke die Attribute **userCertificate** und **userSMIMECertificate** für jedes Benutzerobjekt synchronisieren, damit die Daten zum Signieren und Verschlüsseln von Nachrichten verwendet werden können.

## <a name="more-information"></a>Weitere Informationen

[S/MIME für die Nachrichtensignierung und -verschlüsselung](s-mime-for-message-signing-and-encryption.md)

[Azure Active Directory-Synchronisierungstool](https://go.microsoft.com/fwlink/p/?LinkId=392587)

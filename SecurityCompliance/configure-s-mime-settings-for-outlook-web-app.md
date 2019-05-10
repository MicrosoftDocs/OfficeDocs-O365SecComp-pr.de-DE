---
title: Konfigurieren von S/MIME-Einstellungen in Exchange Online für Outlook im Web
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Eine kurze Beschreibung, was Exchange Online-Administratoren tun müssen, um die S/MIME-Einstellungen in Outlook im Web in Exchange Online anzuzeigen und zu konfigurieren.
ms.openlocfilehash: 41ec5b675284b2040a11f9e076ccef4afcda561a
ms.sourcegitcommit: d24f50347c671cf5d2d8afec2f80d37d18af8b5d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33867828"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a>Konfigurieren von S/MIME-Einstellungen in Exchange Online für Outlook im Web

Als Administrator für Exchange Online können Sie Outlook im Web (früher als Outlook Web App bezeichnet) einrichten, um das Senden und empfangen von S/MIME-geschützten Nachrichten zuzulassen. Verwenden Sie die Cmdlets **Get-SmimeConfig** und **Set-SmimeConfig** , um dieses Feature in Exchange Online PowerShell anzuzeigen und zu verwalten. Wie Sie eine Verbindung mit Exchange Online PowerShell herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) und [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).

## <a name="considerations-for-chrome"></a>Überlegungen zu Chrome

Wenn Sie s/MIME in Outlook im Web im Google Chrome-Webbrowser verwenden möchten, müssen Sie (oder ein anderer Administrator) die Chrom Richtlinie namens **ExtensionInstallForcelist** festlegen und konfigurieren, um die Microsoft S/MIME-Erweiterung in Chrome zu installieren. Der Richtlinienwert lautet `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`. Beachten Sie, dass die Anwendung dieser Richtlinie Computer mit einer Domäne erfordert, sodass die Verwendung von S/MIME in Chrom effektiv Computer mit einer Domäne erfordert.

Ausführliche Informationen zur **ExtensionInstallForcelist** -Richtlinie finden Sie unter [ExtensionInstallForcelist](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).

Dieser Schritt ist eine Voraussetzung für die Verwendung von Chrome; Es ersetzt nicht das S/MIME-Steuerelement, das von Benutzern installiert wird. Benutzer werden aufgefordert, das s/MIME-Steuerelement in Outlook im Web während der ersten Verwendung von s/MIME herunterzuladen und zu installieren. Oder Benutzer können proaktiv zu **S/MIME** im Outlook im Web-Einstellungen wechseln, um den Download-Link für das Steuerelement abzurufen.

## <a name="for-more-information"></a>Weitere Informationen

[S/MIME für die Nachrichtensignierung und -verschlüsselung](s-mime-for-message-signing-and-encryption.md)

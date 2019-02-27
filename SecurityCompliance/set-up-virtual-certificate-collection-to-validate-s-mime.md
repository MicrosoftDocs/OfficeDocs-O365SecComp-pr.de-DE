---
title: Einrichten einer virtuellen Zertifikat Sammlung in Exchange Online zum Überprüfen von S/MIME
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: Administratoren erfahren, wie Sie eine virtuelle Zertifikat Sammlung erstellen, die zum Überprüfen von S/MIME-Zertifikaten in Exchange Online verwendet wird.
ms.openlocfilehash: 2aa6e529f5ca374af6fe6d80a403058a8b6e468a
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296948"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a>Einrichten einer virtuellen Zertifikat Sammlung in Exchange Online zum Überprüfen von S/MIME

Als Administrator müssen Sie eine virtuelle Zertifikat Sammlung in Exchange Online konfigurieren, die zum Überprüfen von S/MIME-Zertifikaten verwendet wird. Diese virtuelle Zertifikats Sammlung ist als Zertifikatspeicher mit einer Dateinamenerweiterung SST eingerichtet. Die SST-Datei enthält alle Stamm-und Zwischenzertifikate, die beim Überprüfen eines S/MIME-Zertifikats verwendet werden.

## <a name="create-and-save-an-sst"></a>Erstellen und Speichern einer SST-Datei

Sie können diese SST-Zertifikatspeicher Datei erstellen, indem Sie die Zertifikate von einem vertrauenswürdigen Computer mithilfe des Cmdlets **Export-Certificate** in __ Windows PowerShell exportieren und den Typwert als sst angeben. Weitere Informationen finden Sie unter [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).

Nachdem Sie die SST-Zertifikatspeicher Datei verwendet haben, verwenden Sie die folgende Syntax in Exchange Online PowerShell, um den Inhalt der SST-Datei im virtuellen Exchange Online-Zertifikatspeicher zu speichern. Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

In diesem Beispiel wird die SST-Datei C:\My Documents\Exported Certificate Store. sst importiert.

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).

## <a name="ensuring-a-certificate-is-valid"></a>Sicherstellen der Gültigkeit eines Zertifikats

In Exchange Online wird nur der SST für die Zertifikatüberprüfung verwendet.

## <a name="more-information"></a>Weitere Informationen

[S/MIME für die Nachrichtensignierung und -verschlüsselung](s-mime-for-message-signing-and-encryption.md)

[Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)

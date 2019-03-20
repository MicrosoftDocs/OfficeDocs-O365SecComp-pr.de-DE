---
title: Einrichten einer virtuellen Zertifikat Sammlung in Exchange Online zum Überprüfen von S/MIME
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: Administratoren erfahren, wie Sie eine virtuelle Zertifikat Sammlung erstellen, die zum Überprüfen von S/MIME-Zertifikaten in Exchange Online verwendet wird.
ms.openlocfilehash: 15998bce1971952286d8dd4401a92f1e9e47c25d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693554"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a><span data-ttu-id="f74cb-103">Einrichten einer virtuellen Zertifikat Sammlung in Exchange Online zum Überprüfen von S/MIME</span><span class="sxs-lookup"><span data-stu-id="f74cb-103">Set up virtual certificate collection in Exchange Online to validate S/MIME</span></span>

<span data-ttu-id="f74cb-104">Als Administrator müssen Sie eine virtuelle Zertifikat Sammlung in Exchange Online konfigurieren, die zum Überprüfen von S/MIME-Zertifikaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f74cb-104">As an admin, you will need to configure a virtual certificate collection in Exchange Online that will be used to validate S/MIME certificates.</span></span> <span data-ttu-id="f74cb-105">Diese virtuelle Zertifikats Sammlung ist als Zertifikatspeicher mit einer Dateinamenerweiterung SST eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f74cb-105">This virtual certificate collection is set up as a certificate store with an SST filename extension.</span></span> <span data-ttu-id="f74cb-106">Die SST-Datei enthält alle Stamm- und Zwischenzertifikate, die bei der Überprüfung eines S/MIME-Zertifikats verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f74cb-106">The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>

## <a name="create-and-save-an-sst"></a><span data-ttu-id="f74cb-107">Erstellen und Speichern einer SST-Datei</span><span class="sxs-lookup"><span data-stu-id="f74cb-107">Create and save an SST</span></span>

<span data-ttu-id="f74cb-108">Sie können diese SST-Zertifikatspeicher Datei erstellen, indem Sie die Zertifikate von einem vertrauenswürdigen Computer mithilfe des Cmdlets **Export-Certificate** in __ Windows PowerShell exportieren und den Typwert als sst angeben.</span><span class="sxs-lookup"><span data-stu-id="f74cb-108">You can create this SST certificate store file by exporting the certificates from a trusted machine using the **Export-Certificate** cmdlet in Windows PowerShell and specifying the _Type_ value as SST.</span></span> <span data-ttu-id="f74cb-109">Weitere Informationen finden Sie unter [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span><span class="sxs-lookup"><span data-stu-id="f74cb-109">For instructions, see [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span></span>

<span data-ttu-id="f74cb-110">Nachdem Sie die SST-Zertifikatspeicher Datei verwendet haben, verwenden Sie die folgende Syntax in Exchange Online PowerShell, um den Inhalt der SST-Datei im virtuellen Exchange Online-Zertifikatspeicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f74cb-110">Once you have the SST certificate store file, use the following syntax in Exchange Online PowerShell to save the SST file contents in the Exchange Online virtual certificate store.</span></span> <span data-ttu-id="f74cb-111">Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="f74cb-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

<span data-ttu-id="f74cb-112">In diesem Beispiel wird die SST-Datei C:\My Documents\Exported Certificate Store. sst importiert.</span><span class="sxs-lookup"><span data-stu-id="f74cb-112">This example imports the SST file C:\My Documents\Exported Certificate Store.sst.</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

<span data-ttu-id="f74cb-113">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span><span class="sxs-lookup"><span data-stu-id="f74cb-113">For detailed syntax and parameter information, see [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span></span>

## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="f74cb-114">Sicherstellen der Gültigkeit eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f74cb-114">Ensuring a certificate is valid</span></span>

<span data-ttu-id="f74cb-115">In Exchange Online wird nur der SST für die Zertifikatüberprüfung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f74cb-115">In Exchange Online, only the SST is used for certificate validation.</span></span>

## <a name="more-information"></a><span data-ttu-id="f74cb-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f74cb-116">More Information</span></span>

[<span data-ttu-id="f74cb-117">S/MIME für die Nachrichtensignierung und -verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="f74cb-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="f74cb-118">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="f74cb-118">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)

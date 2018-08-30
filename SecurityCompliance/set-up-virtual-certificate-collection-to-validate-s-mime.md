---
title: Einrichten einer virtuellen Zertifikatauflistung für die Überprüfung von S/MIME
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
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: s mandantenadministrator müssen Sie eine Auflistung der virtuellen Zertifikate konfigurieren, die zur Überprüfung von S/MIME-Zertifikaten verwendet werden.
ms.openlocfilehash: 88d12b3c1d5f36c58f278cf304237a569a8b92c4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003034"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a><span data-ttu-id="98e24-103">Einrichten einer virtuellen Zertifikatauflistung für die Überprüfung von S/MIME</span><span class="sxs-lookup"><span data-stu-id="98e24-103">Set up virtual certificate collection to validate S/MIME</span></span>

<span data-ttu-id="98e24-p101">Als Mandantenadministrator müssen Sie eine virtuelle Zertifikatauflistung konfigurieren, die zur Überprüfung von S/MIME-Zertifikaten verwendet wird. Die virtuelle Zertifikatauflistung wird als Datei vom Typ Zertifikatspeicher mit der Dateinamenerweiterung SST eingerichtet. Die SST-Datei enthält alle Stamm- und Zwischenzertifikate, die bei der Überprüfung eines S/MIME-Zertifikats verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98e24-p101">As a tenant administrator you will need to configure a virtual certificate collection that will be used to validate S/MIME certificates. This virtual certificate collection is set up as a certificate store file type with an SST filename extension. The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>
  
## <a name="create-and-save-an-sst"></a><span data-ttu-id="98e24-107">Erstellen und Speichern einer SST-Datei</span><span class="sxs-lookup"><span data-stu-id="98e24-107">Create and save an SST</span></span>
<span data-ttu-id="98e24-108"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="98e24-108"></span></span>

<span data-ttu-id="98e24-p102">Die Shell kann nur für diesen Vorgang verwendet werden. Wie eine Exchange-Verwaltungsshell in Ihrer lokalen Exchange-Organisation geöffnet wird, erfahren Sie unter **Open the Shell**. Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.</span><span class="sxs-lookup"><span data-stu-id="98e24-p102">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
<span data-ttu-id="98e24-p103">Als Administrator können Sie diese SST-Datei erstellen, indem Sie die Zertifikate mit dem Cmdlet  `Export-Certificate` von einem vertrauenswürdigen Computer exportieren und den Typ als SST angeben. Weitere Informationen zum Cmdlet  `Export-Certificate` finden Sie im Referenzthema zu [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx).</span><span class="sxs-lookup"><span data-stu-id="98e24-p103">As an administrator, you can create this SST file by exporting the certificates from a trusted machine using the  `Export-Certificate` cmdlet and specifying the type as SST. For more information the  `Export-Certificate` cmdlet, see the [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx) reference topic.</span></span> 
  
<span data-ttu-id="98e24-p104">Nachdem die SST-Datei generiert wurde, speichern Sie sie mit dem Cmdlet  `Set-Smimeconfig` mit dem Parameter  _-SMIMECertificateIssuingCA_ im virtuellen Zertifikatspeicher. Beispiel:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span><span class="sxs-lookup"><span data-stu-id="98e24-p104">Once the SST file is generated, use the  `Set-Smimeconfig` cmdlet to save it in the virtual certificate store by using the  _-SMIMECertificateIssuingCA_ parameter. For example:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span></span>
  
## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="98e24-116">Sicherstellen der Gültigkeit eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="98e24-116">Ensuring a certificate is valid</span></span>
<span data-ttu-id="98e24-117"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="98e24-117"></span></span>

<span data-ttu-id="98e24-p105">Zunächst sucht Exchange 2013 SP1 nach der SST-Datei und überprüft das Zertifikat. Liefert die Überprüfung einen Fehler, wird im Zertifikatspeicher des lokalen Computers gesucht, um das Zertifikat zu überprüfen. Dieses Verhalten ist neu in Exchange 2013 SP1 und unterscheidet sich von früheren Versionen von Exchange. In Exchange Online wird nur die SST-Datei zur Überprüfung verwendet.</span><span class="sxs-lookup"><span data-stu-id="98e24-p105">Exchange 2013 SP1 first checks for the SST file and validates the certificate. If the validation fails, it will look at the local machine certificate store to validate the certificate. This behavior is new for Exchange 2013 SP1 and different from prior versions of Exchange. In Exchange Online only the SST will be used for validation.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="98e24-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98e24-122">More Information</span></span>
<span data-ttu-id="98e24-123"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="98e24-123"></span></span>

[<span data-ttu-id="98e24-124">S/MIME für die Nachrichtensignierung und -verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="98e24-124">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="98e24-125">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="98e24-125">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  


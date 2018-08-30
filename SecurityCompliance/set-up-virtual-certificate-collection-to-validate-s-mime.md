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
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a>Einrichten einer virtuellen Zertifikatauflistung für die Überprüfung von S/MIME

Als Mandantenadministrator müssen Sie eine virtuelle Zertifikatauflistung konfigurieren, die zur Überprüfung von S/MIME-Zertifikaten verwendet wird. Die virtuelle Zertifikatauflistung wird als Datei vom Typ Zertifikatspeicher mit der Dateinamenerweiterung SST eingerichtet. Die SST-Datei enthält alle Stamm- und Zwischenzertifikate, die bei der Überprüfung eines S/MIME-Zertifikats verwendet werden.
  
## <a name="create-and-save-an-sst"></a>Erstellen und Speichern einer SST-Datei
<a name="sectionSection0"> </a>

Die Shell kann nur für diesen Vorgang verwendet werden. Wie eine Exchange-Verwaltungsshell in Ihrer lokalen Exchange-Organisation geöffnet wird, erfahren Sie unter **Open the Shell**. Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.
  
Als Administrator können Sie diese SST-Datei erstellen, indem Sie die Zertifikate mit dem Cmdlet  `Export-Certificate` von einem vertrauenswürdigen Computer exportieren und den Typ als SST angeben. Weitere Informationen zum Cmdlet  `Export-Certificate` finden Sie im Referenzthema zu [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx). 
  
Nachdem die SST-Datei generiert wurde, speichern Sie sie mit dem Cmdlet  `Set-Smimeconfig` mit dem Parameter  _-SMIMECertificateIssuingCA_ im virtuellen Zertifikatspeicher. Beispiel:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`
  
## <a name="ensuring-a-certificate-is-valid"></a>Sicherstellen der Gültigkeit eines Zertifikats
<a name="sectionSection1"> </a>

Zunächst sucht Exchange 2013 SP1 nach der SST-Datei und überprüft das Zertifikat. Liefert die Überprüfung einen Fehler, wird im Zertifikatspeicher des lokalen Computers gesucht, um das Zertifikat zu überprüfen. Dieses Verhalten ist neu in Exchange 2013 SP1 und unterscheidet sich von früheren Versionen von Exchange. In Exchange Online wird nur die SST-Datei zur Überprüfung verwendet.
  
## <a name="more-information"></a>Weitere Informationen
<a name="sectionSection2"> </a>

[S/MIME für die Nachrichtensignierung und -verschlüsselung](s-mime-for-message-signing-and-encryption.md)
  
[Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  


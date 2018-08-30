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
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="ad2af-105">Synchronisierung von Benutzerzertifikaten nach Office 365 für S/MIME</span><span class="sxs-lookup"><span data-stu-id="ad2af-105">Sync user certificates to Office 365 for S/MIME</span></span>

<span data-ttu-id="ad2af-p102">Damit S/MIME-geschützte Nachrichten versendet werden können, müssen die entsprechenden Zertifikate eingerichtet werden. Zum Senden von verschlüsselten Nachrichten über Exchange Online verwendet das E-Mail-Programm das öffentliche Zertifikat des Empfängers, um die Nachricht zu verschlüsseln. Dieses öffentliche X.509-Zertifikat muss in Office 365 veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="ad2af-p102">Before anyone can send S/MIME-protected messages, the appropriate certificates must be set up. In order to send encrypted messages through Exchange Online, the sender's email program uses the public certificate of the recipient to encrypt the message. This public X.509 certificate has to be published to Office 365.</span></span>
  
## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="ad2af-109">So synchronisieren Sie Zertifikate, die S/MIME unterstützen</span><span class="sxs-lookup"><span data-stu-id="ad2af-109">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="ad2af-p103">Richten Sie S/MIME ein, indem Sie Zertifikate ausgeben und diese in Ihrem lokalen Active Directory-Domänendienst veröffentlichen. Weitere Informationen zum Verwalten von Zertifikaten in Exchange 2013 finden Sie unter [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad2af-p103">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service. For more information about managing certificates in Exchange 2013, see [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span></span>
  
<span data-ttu-id="ad2af-p104">Nachdem Ihre Zertifikate veröffentlicht wurden, verwenden Sie Azure Active Directory-Synchronisierungstool, um Benutzerdaten aus der lokalen Exchange-Umgebung mit Office 365 zu synchronisieren. Weitere Informationen zu diesem Prozess finden Sie unter [DirSync: Versionsverlauf für das Verzeichnissynchronisierungstool](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span><span class="sxs-lookup"><span data-stu-id="ad2af-p104">After your certificates are published, use the Azure Active Directory Sync tool to synchronize user data from your on-premises Exchange environment to Office 365. For more information on this process, see [DirSync: Directory Sync Tool Version Release History](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span></span>
  
<span data-ttu-id="ad2af-114">Zusammen mit anderen Verzeichnisdaten synchronisiert das Tool für S/MIME-Zwecke die Attribute  `userCertificate` und  `userSMIMECertificate` für jedes Benutzerobjekt, sodass die Daten verwendet werden können, um Nachrichten zu signieren und zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="ad2af-114">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  `userCertificate` and  `userSMIMECertificate` attributes for each user object so the data can be used to sign and encrypt messages.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="ad2af-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad2af-115">More Information</span></span>

[<span data-ttu-id="ad2af-116">S/MIME für die Nachrichtensignierung und -verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="ad2af-116">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="ad2af-117">Azure Active Directory-Synchronisierungstool</span><span class="sxs-lookup"><span data-stu-id="ad2af-117">Azure Active Directory Sync tool</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  


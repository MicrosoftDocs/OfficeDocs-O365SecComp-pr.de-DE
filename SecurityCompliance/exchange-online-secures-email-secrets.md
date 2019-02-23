---
title: Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Zusätzlich zum Office 365 Trust Center, das Sicherheits-, Datenschutz-und Kompatibilitätsinformationen für Office 365 bereitstellt, möchten Sie vielleicht wissen, wie Office 365 die von Ihnen bereitgestellten vertraulichen Daten in den Rechenzentren schützt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
ms.openlocfilehash: ba4c661899273f5e07c2468631298f5500d0e32f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218075"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="b7be9-104">Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b7be9-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="b7be9-105">In diesem Artikel wird beschrieben, wie Microsoft Ihre geheimen E-Mail-Daten in seinen Datencentern sichert.</span><span class="sxs-lookup"><span data-stu-id="b7be9-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="b7be9-106">Wie sichern wir geheime Informationen, die von Ihnen bereitgestellt werden?</span><span class="sxs-lookup"><span data-stu-id="b7be9-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="b7be9-p102">Zusätzlich zum Office 365 Trust Center, das [Sicherheits-, Datenschutz-und Kompatibilitätsinformationen für office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, möchten Sie vielleicht wissen, wie Office 365 die von Ihnen bereitgestellten vertraulichen Daten in den Rechenzentren schützt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).</span><span class="sxs-lookup"><span data-stu-id="b7be9-p102">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters. We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="b7be9-p103">Die verteilte Schlüsselverwaltung (DKM) ist eine clientseitige Funktionalität, die eine Reihe von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet. Nur Mitglieder einer bestimmten Sicherheitsgruppe in Active Directory-Domänendiensten können auf diese Schlüssel zugreifen, um die Daten zu entschlüsseln, die von DKM verschlüsselt wurden. In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe. Zum Standardverfahren im Datencenter gehört es, dass kein Benutzer Anmeldeinformationen erhält, die Teil dieser Sicherheitsgruppe sind. Daher hat keine Person Zugriff auf die Schlüssel, mit denen diese geheimen Daten entschlüsselt werden können.</span><span class="sxs-lookup"><span data-stu-id="b7be9-p103">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information. Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM. In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group. As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="b7be9-p104">Zu Debugging-, Problembehandlungs- oder Überwachungszwecken muss ein Datencenteradministrator erhöhte Rechte anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind. Dieser Vorgang erfordert mehrere Stufen rechtlicher Genehmigungen. Wenn der Zugriff gewährt wird, werden alle Aktivitäten protokolliert und überwacht. Darüber hinaus wird der Zugriff nur für einen bestimmten Zeitraum gewährt, danach läuft er automatisch ab.</span><span class="sxs-lookup"><span data-stu-id="b7be9-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="b7be9-p105">Als zusätzliche Schutzmaßnahme umfasst die DKM-Technologie einen automatisierten Schlüsselrollover sowie automatische Archivierung. Dadurch wird sichergestellt, dass Sie weiterhin auf Ihre älteren Inhalte zugreifen können, ohne dabei auf unbestimmte Zeit den gleichen Schlüssel zu verwenden.
</span><span class="sxs-lookup"><span data-stu-id="b7be9-p105">For extra protection, DKM technology includes automated key rollover and archiving. This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="b7be9-119">Wo wird DKM bei Exchange Online eingesetzt?</span><span class="sxs-lookup"><span data-stu-id="b7be9-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="b7be9-p106">Microsoft verwendet DKM, um Ihre geheimen Daten in Exchange Online-Datencentern zu verschlüsseln. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b7be9-p106">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters. For example:</span></span>
  
- <span data-ttu-id="b7be9-p107">Anmeldeinformationen für E-Mail-Konten für verbundene Konten. Verbundene Konten sind Drittanbieterkonten wie Hotmail-, Gmail- und Yahoo!-E-Mail-Konten.</span><span class="sxs-lookup"><span data-stu-id="b7be9-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>
    
- <span data-ttu-id="b7be9-p108">RMS-Stammschlüssel. Dabei handelt es sich um Kundenschlüssel, die entweder aus Azure RMS oder aus der lokalen Active Directory-Domänendienste-Bereitstellungen des Kunden importiert werden, die zum Verschlüsseln und Entschlüsseln von e-Mails mit RMS oder Office 365 Message Encryption (OM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7be9-p108">Rights Management service (RMS) root keys. These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="b7be9-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b7be9-127">Related topics</span></span>

[<span data-ttu-id="b7be9-128">Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="b7be9-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="b7be9-129">Technische Details zur Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="b7be9-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="b7be9-130">Dienstsicherheit im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="b7be9-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  


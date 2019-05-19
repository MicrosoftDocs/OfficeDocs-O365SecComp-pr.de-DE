---
title: Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Neben dem Office 365 Trust Center, das Informationen zu Sicherheit, Datenschutz und Compliance für Office 365 bereitstellt, sollten Sie wissen, wie Office 365 zum Schutz von in den Rechenzentren bereitgestellten Geheimnissen beiträgt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
ms.openlocfilehash: 609d59b6e4da779e0fa663b40fdbf26036753669
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154587"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="344d4-104">Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online</span><span class="sxs-lookup"><span data-stu-id="344d4-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="344d4-105">In diesem Artikel wird beschrieben, wie Microsoft Ihre e-Mail-Geheimnisse in ihren Rechenzentren sichert.</span><span class="sxs-lookup"><span data-stu-id="344d4-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="344d4-106">Wie sichern wir geheime Informationen, die von Ihnen bereitgestellt werden?</span><span class="sxs-lookup"><span data-stu-id="344d4-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="344d4-107">Neben dem Office 365 Trust Center, das Informationen zu [Sicherheit, Datenschutz und Compliance für Office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, sollten Sie wissen, wie Office 365 zum Schutz von in den Rechenzentren bereitgestellten Geheimnissen beiträgt.</span><span class="sxs-lookup"><span data-stu-id="344d4-107">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters.</span></span> <span data-ttu-id="344d4-108">Wir verwenden eine Technologie namens Distributed Key Manager (DKM).</span><span class="sxs-lookup"><span data-stu-id="344d4-108">We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="344d4-109">Distributed Key Manager (DKM) ist eine clientseitige Funktionalität, die eine Reihe von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="344d4-109">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information.</span></span> <span data-ttu-id="344d4-110">Nur Mitglieder einer bestimmten Sicherheitsgruppe in Active Directory-Domänendienste können auf diese Schlüssel zugreifen, um die von DKM verschlüsselten Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="344d4-110">Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM.</span></span> <span data-ttu-id="344d4-111">In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="344d4-111">In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group.</span></span> <span data-ttu-id="344d4-112">Im Rahmen des standardmäßigen betriebsverfahrens im Rechenzentrum werden keinem Menschen Anmeldeinformationen zugewiesen, die Teil dieser Sicherheitsgruppe sind, und daher hat kein Mensch Zugriff auf die Schlüssel, die diese Geheimnisse entschlüsseln können.</span><span class="sxs-lookup"><span data-stu-id="344d4-112">As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="344d4-113">Zum Debuggen, zur Problembehandlung oder zu Überwachungszwecken muss ein Rechenzentrums Administrator erhöhten Zugriff anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind.</span><span class="sxs-lookup"><span data-stu-id="344d4-113">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group.</span></span> <span data-ttu-id="344d4-114">Für diesen Prozess sind mehrere Ebenen der rechtlichen Genehmigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="344d4-114">This process requires multiple levels of legal approval.</span></span> <span data-ttu-id="344d4-115">Wenn der Zugriff gewährt wird, werden alle Aktivitäten protokolliert und überwacht.</span><span class="sxs-lookup"><span data-stu-id="344d4-115">If access is granted, all activity is logged and audited.</span></span> <span data-ttu-id="344d4-116">Darüber hinaus wird der Zugriff nur für ein festgelegtes Zeitintervall gewährt, nach dem es automatisch abläuft.</span><span class="sxs-lookup"><span data-stu-id="344d4-116">In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="344d4-117">Für zusätzlichen Schutz umfasst die DKM-Technologie einen automatisierten Schlüssel Rollover und eine Archivierung.</span><span class="sxs-lookup"><span data-stu-id="344d4-117">For extra protection, DKM technology includes automated key rollover and archiving.</span></span> <span data-ttu-id="344d4-118">Dadurch wird auch sichergestellt, dass Sie weiterhin auf Ihre älteren Inhalte zugreifen können, ohne sich auf unbestimmte Zeit auf denselben Schlüssel verlassen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="344d4-118">This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="344d4-119">Wo verwendet Exchange Online DKM?</span><span class="sxs-lookup"><span data-stu-id="344d4-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="344d4-120">Microsoft verwendet DKM, um ihre Geheimnisse in Exchange Online-Rechenzentren zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="344d4-120">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters.</span></span> <span data-ttu-id="344d4-121">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="344d4-121">For example:</span></span>
  
- <span data-ttu-id="344d4-122">E-Mail-Kontoanmeldeinformationen für verbundene Konten.</span><span class="sxs-lookup"><span data-stu-id="344d4-122">Email account credentials for connected accounts.</span></span> <span data-ttu-id="344d4-123">Verbundene Konten sind Drittanbieter Konten wie Hotmail, Gmail und Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="344d4-123">Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo!</span></span> <span data-ttu-id="344d4-124">e-Mail-Konten.</span><span class="sxs-lookup"><span data-stu-id="344d4-124">mail accounts.</span></span>
    
- <span data-ttu-id="344d4-125">RMS-Stammschlüssel (Rights Management Service, Rechteverwaltungsdienst).</span><span class="sxs-lookup"><span data-stu-id="344d4-125">Rights Management service (RMS) root keys.</span></span> <span data-ttu-id="344d4-126">Hierbei handelt es sich um Kundenschlüssel, die entweder aus Azure RMS oder aus lokalen Active Directory-Domänendienste RMS-Bereitstellungen von Kunden importiert werden, die zum Verschlüsseln und Entschlüsseln von e-Mails mit RMS-oder Office 365-Nachrichtenverschlüsselung (OM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="344d4-126">These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="344d4-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="344d4-127">Related topics</span></span>

[<span data-ttu-id="344d4-128">Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="344d4-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="344d4-129">Technische Details zur Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="344d4-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="344d4-130">Dienst Assurance im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="344d4-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  


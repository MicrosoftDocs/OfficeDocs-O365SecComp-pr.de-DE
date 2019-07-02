---
title: Office 365 jammern von Unternehmens Zugriffs Steuerelementen
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine kurze Zusammenfassung über das Jammern von Enterprise-Zugriffs Steuerelementen in der Produktionsumgebung.'
ms.openlocfilehash: ec1a5767495b6b183ceda2af558cbec0c479e956
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622315"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="90601-103">Yammer Enterprise-Zugriffssteuerungen</span><span class="sxs-lookup"><span data-stu-id="90601-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="90601-104">Der physische und logische Zugriff auf die Produktionsumgebung jammern ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="90601-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="90601-105">Wie bei anderen Office 365-Ingenieuren haben Jammer Techniker keinen ständigen Zugriff auf Kundendaten.</span><span class="sxs-lookup"><span data-stu-id="90601-105">As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data.</span></span> <span data-ttu-id="90601-106">Der Zugriff muss mithilfe eines Genehmigungs basierten Just-in-Time-Zugriffs Steuerungssystems angefordert werden, ähnlich wie Lockbox mit einer begrenzten Anzahl von genehmigenden Personen.</span><span class="sxs-lookup"><span data-stu-id="90601-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="90601-107">Genehmigende Personen überprüfen die Anforderung (beispielsweise überprüfen, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Zeit usw. legitim ist), und genehmigen oder verweigern die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="90601-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="90601-108">Wenn die Anforderung genehmigt wird, wird der JIT-Zugriff für eine definierte und beschränkte Zeit gewährt.</span><span class="sxs-lookup"><span data-stu-id="90601-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="90601-109">Nach Überschreiten der Zugriffszeit läuft der Zugriff automatisch ab.</span><span class="sxs-lookup"><span data-stu-id="90601-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="90601-110">Wie bei anderen Office 365 Diensten verwendet jeder Zugriff auf die Produktionsumgebung für jammern die mehrstufige Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="90601-110">As with other Office 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="90601-111">Der gesamte Zugriffs-und Befehlsverlauf wird einem Benutzer zugeschrieben und regelmäßig vom Sicherheitsteam "jammern" protokolliert und überprüft.</span><span class="sxs-lookup"><span data-stu-id="90601-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="90601-112">Weitere Informationen zur Verwaltung und Verwaltung von jammern finden Sie unter jammern der [Administratorhilfe](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="90601-112">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>
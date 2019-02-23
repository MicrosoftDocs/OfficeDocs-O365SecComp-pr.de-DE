---
title: Office 365 jammern Enterprise-Zugriffssteuerungen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine kurze Zusammenfassung zu jammern von Enterprise-Zugriffssteuerungen in der Produktionsumgebung.'
ms.openlocfilehash: 76b62e7ea026a52d822e5a213461e930b1d595e3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217885"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="0d19f-103">Yammer Enterprise-Zugriffssteuerungen</span><span class="sxs-lookup"><span data-stu-id="0d19f-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="0d19f-p101">Sowohl der physische als auch der logische Zugriff auf die Produktionsumgebung jammern ist auf eine sehr kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Office 365-Ingenieuren haben Jammer Ingenieure keinen Zugriff auf Kundendaten. Der Zugriff muss über ein Genehmigungs basiertes Just-in-Time-Zugriffs Steuerungssystem wie Lockbox angefordert werden, und es gibt eine begrenzte Anzahl von genehmigenden Personen. Genehmigende Personen überprüfen die Anforderung (beispielsweise überprüfen Sie, ob die Anforderung aufgrund der Anforderungen, des Geschäftsfalls, der Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird der JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt, nach dem er automatisch abläuft.</span><span class="sxs-lookup"><span data-stu-id="0d19f-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="0d19f-p102">Wie bei anderen Office 365-Diensten nutzt der gesamte Zugriff auf die Produktionsumgebung jammern die mehrstufige Authentifizierung. Der gesamte Zugriff und der Befehlsverlauf werden einem Benutzer zugeordnet und vom Jammer Sicherheitsteam regelmäßig protokolliert und überprüft.</span><span class="sxs-lookup"><span data-stu-id="0d19f-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="0d19f-111">Weitere Informationen zur Verwaltung und Verwaltung von jammern finden Sie unter [Hilfe](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US)zu jammern.</span><span class="sxs-lookup"><span data-stu-id="0d19f-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>
---
title: Office 365 jammern Enterprise-Zugriffssteuerungen
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
description: 'Zusammenfassung: eine kurze Zusammenfassung zu jammern von Enterprise-Zugriffssteuerungen in der Produktionsumgebung.'
ms.openlocfilehash: 61598235a010aaa1c578c449cb054073212a41f9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262347"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Enterprise-Zugriffssteuerungen 

Sowohl der physische als auch der logische Zugriff auf die Produktionsumgebung jammern ist auf eine sehr kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Office 365-Ingenieuren haben Jammer Ingenieure keinen Zugriff auf Kundendaten. Der Zugriff muss über ein Genehmigungs basiertes Just-in-Time-Zugriffs Steuerungssystem wie Lockbox angefordert werden, und es gibt eine begrenzte Anzahl von genehmigenden Personen. Genehmigende Personen überprüfen die Anforderung (beispielsweise überprüfen Sie, ob die Anforderung aufgrund der Anforderungen, des Geschäftsfalls, der Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird der JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt, nach dem er automatisch abläuft. 

Wie bei anderen Office 365-Diensten nutzt der gesamte Zugriff auf die Produktionsumgebung jammern die mehrstufige Authentifizierung. Der gesamte Zugriff und der Befehlsverlauf werden einem Benutzer zugeordnet und vom Jammer Sicherheitsteam regelmäßig protokolliert und überprüft.

Weitere Informationen zur Verwaltung und Verwaltung von jammern finden Sie unter [Hilfe](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US)zu jammern.
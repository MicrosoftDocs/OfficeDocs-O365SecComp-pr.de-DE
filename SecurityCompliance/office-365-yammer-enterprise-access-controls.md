---
title: Office 365 jammern Enterprise-Zugriffssteuerungen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine kurze Zusammenfassung zu jammern von Enterprise-Zugriffssteuerungen in der Produktionsumgebung.'
ms.openlocfilehash: 33126ee6acf42a97148c12917855535a8578e8cf
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090727"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Enterprise-Zugriffssteuerungen 

Sowohl der physische als auch der logische Zugriff auf die Produktionsumgebung jammern ist auf eine sehr kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Office 365-Ingenieuren haben Jammer Ingenieure keinen Zugriff auf Kundendaten. Der Zugriff muss über ein Genehmigungs basiertes Just-in-Time-Zugriffs Steuerungssystem wie Lockbox angefordert werden, und es gibt eine begrenzte Anzahl von genehmigenden Personen. Genehmigende Personen überprüfen die Anforderung (beispielsweise überprüfen Sie, ob die Anforderung aufgrund der Anforderungen, des Geschäftsfalls, der Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird der JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt, nach dem er automatisch abläuft. 

Wie bei anderen Office 365-Diensten nutzt der gesamte Zugriff auf die Produktionsumgebung jammern die mehrstufige Authentifizierung. Der gesamte Zugriff und der Befehlsverlauf werden einem Benutzer zugeordnet und vom Jammer Sicherheitsteam regelmäßig protokolliert und überprüft.

Weitere Informationen zur Verwaltung und Verwaltung von jammern finden Sie unter [Hilfe](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US)zu jammern.
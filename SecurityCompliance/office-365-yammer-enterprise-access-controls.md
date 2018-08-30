---
title: Zugreifen auf Steuerelemente von Office 365 Yammer Enterprise
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
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Eine kurze Zusammenfassung zur Yammer Enterprise zugreifen auf Steuerelemente in der produktionsumgebung.'
ms.openlocfilehash: 3f51e63c16022353e743b57d8e977f2ea2e6a835
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529972"
---
# <a name="yammer-enterprise-access-controls"></a>Zugreifen auf Steuerelemente von Yammer Enterprise 

Physische und logische Zugriff auf die Yammer-produktionsumgebung ist auf eine sehr kleine Gruppe von Personen (Infrastruktur und Vorgänge) beschränkt. Wie andere Ingenieure Office 365 haben Yammer Ingenieure NULL stehende Zugriff auf Kundendaten. Access muss ein Zugriff auf Genehmigung-Basis Just-in-Time-Verwaltungssystem Lockbox ähnelt mit angefordert werden, und es ist eine begrenzte Anzahl von genehmigende Personen. Genehmigende Personen überprüfen, ob die Anforderung (z. B. sie überprüfen, ob die Anforderung legitime basierend auf Notwendigkeit, Geschäftsfall, Zeit usw. wird), und klicken Sie dann genehmigen oder ablehnen. Wenn die Anforderung genehmigt wird, JIT für einen Zeitraum definiert ist und begrenzt erhält Zugriff nach dem sie automatisch abläuft. 

Wie bei anderen Office 365-Dienste nutzt alle Zugriff auf die produktionsumgebung Yammer mehrstufige Authentifizierung. Alle Access und Befehl Verlauf Ergebnisarray als Attribut zugewiesen, die ein Benutzer und protokolliert und Teams Sicherheit für Yammer regelmäßig überprüft.

Weitere Informationen zu Yammer Administration und Verwaltung finden Sie unter [Yammer Admin-Hilfe](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).
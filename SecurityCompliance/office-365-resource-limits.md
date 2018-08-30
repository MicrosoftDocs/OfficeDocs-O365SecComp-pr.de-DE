---
title: Grenzwerte für Office 365-Ressource
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
description: 'Zusammenfassung: Informationen zu Ressourcen für die verschiedenen Komponenten von Office 365 beschränkt.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530116"
---
# <a name="resource-limits"></a>Ressourcengrenzen

Verwenden von Kontingenten (Grenzwerte) und der Einschränkung ist Ressourcengrenzen durchgesetzt. Azure Active Directory und der einzelnen Office 365-Dienste verwenden beide. Grenzwerte für dienstspezifische werden und mit der Zeit ändern, wie die neuen Funktionen hinzugefügt werden. Ausführliche auf die aktuellen Grenzwerte für die verschiedenen Dienste finden Sie unter den folgenden Themen:
- [Azure Active Directory Service Grenzen und Einschränkungen](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [Exchange Online-Begrenzungen](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [Beschränkungen von Exchange Online Protection](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [SharePoint Online softwarebeschränkungen und-Grenzen](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype für Business-Grenzwerte](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [Yammer-REST-API und Rate-Grenzwerte](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Maximale Dateigröße in Schlingern](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Zusätzlich zu diesen Grenzwerten werden mehrere einschränkungsmechanismen in der gesamten Azure Active Directory und Office 365 verwendet. Innerhalb des Dienstes Einschränkung ist besonders wichtig, wenn die Ressourcen des Umkreisnetzwerks in Microsoft Rechenzentren für die Breite Palette von Kunden optimiert sind, die die Dienste zu verwenden. Einschränkungsmechanismen umfassen:
- Azure Active Directory und Office 365-Features auf Benutzerebene Einschränkung, die die Anzahl der Transaktionen oder gleichzeitige Anrufe (durch Code- oder Skriptblock), die von einem einzelnen Benutzer ausgeführt werden können.
- Jeder Mandant bei der Erstellung des Mandanten wird eine standardmäßige Einschränkungsrichtlinie PowerShell zugewiesen. Diese Einstellungen wirken sich auf anderen Elementen, wie die maximale Anzahl von gleichzeitigen PowerShell-Sitzungen, die von einem Administrator der einzelnen geöffnet werden können.
- Jeder Exchange Online-Kunden ist eine Standardrichtlinie für die Exchange-Webdienste (EWS), die für EWS-Client-Vorgänge optimiert ist, und, die Einschränkung gilt für alle Outlook-Clients.

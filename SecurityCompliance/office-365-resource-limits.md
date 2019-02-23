---
title: Office 365-Ressourcengrenzwerte
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
description: 'Zusammenfassung: Informationen zu Ressourcen Grenzwerten für die verschiedenen Anwendungen in Office 365.'
ms.openlocfilehash: ee44bde8bd93d3628ed3f31f5bbbce024a3056b5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220215"
---
# <a name="resource-limits"></a>Ressourcenbeschränkungen

Ressourcengrenzwerte werden mithilfe von Kontingenten (Limits) und Einschränkung erzwungen. Azure Active Directory und die einzelnen Office 365-Dienste verwenden beides. Grenzwertesind Dienst spezifisch und ändern sich im Lauf der Zeit, wenn neue Funktionen hinzugefügt werden. Details zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:
- [Grenzwerte und Einschränkungen des Azure Active Directory-Diensts](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [Exchange Online-Begrenzungen](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [Beschränkungen von Exchange Online Protection](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [Grenzen und Grenzen von SharePoint Online-Software](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business-Grenzwerte](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [Jammern-REST-API und Raten Begrenzungen](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Dateigrößenbeschränkungen in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Zusätzlich zu diesen Grenzwerten werden in Azure Active Directory und Office 365 mehrere Einschränkungs Mechanismen verwendet. Die Einschränkung innerhalb des Diensts ist besonders wichtig, da die Netzwerkressourcen in Microsoft-Rechenzentren für die breite Palette von Kunden optimiert sind, die die Dienste nutzen. Zu den Einschränkungs Mechanismen gehört Folgendes:
- Azure Active Directory und Office 365 verfügen über Einschränkungen auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen anrufen (durch Skripts oder Code) begrenzen, die von einem einzelnen Benutzer ausgeführt werden können.
- Jedem Mandanten wird bei der Mandanten Erstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen. Diese Einstellungen wirken sich auf andere Elemente aus, wie beispielsweise die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.
- Jeder Exchange Online-Kunde verfügt über eine Standardrichtlinie für Exchange-webDienste (EWS), die für EWS-Client Vorgänge optimiert ist, sowie eine Drosselung, die für alle Outlook-Clients gilt.

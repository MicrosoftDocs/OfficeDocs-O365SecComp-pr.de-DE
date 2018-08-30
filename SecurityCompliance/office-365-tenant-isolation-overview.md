---
title: Mandantenisolation in Office 365
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
description: Eine Übersicht darüber, wie Microsoft mandantenisolation für Office 365 erzwingt.
ms.openlocfilehash: fcf66ee65c2a4cfdf73ae0eac77f54bd555d059d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529514"
---
# <a name="tenant-isolation-in-office-365"></a>Mandantenisolation in Office 365

Einer der wichtigsten Vorteile von Cloud computing Konzept einer freigegebenen, allgemeine Infrastruktur gleichzeitig über zahlreiche Kunden ist, was zu Größenvorteile. Dieses Konzept ist *mehrmandantenfähigkeit*bezeichnet. Microsoft versucht kontinuierlich stellen Sie sicher, dass die Architekturen mit mehreren Mandanten unsere Cloud-Dienste auf Unternehmensebene Sicherheit, Vertraulichkeit, Datenschutz, Integrität und Verfügbarkeit Standards unterstützen.

Basierend auf das erhebliche Investitionen und die Erfahrung von [Trustworthy Computing](https://www.microsoft.com/en-us/twc/default.aspx) und dem [Security Development Lifecycle](http://www.microsoft.com/security/sdl/default.aspx)gesammelt, wurden Microsoft Cloud Services unter der Annahme entwickelt, dass alle Mandanten für alle potenziell schädlichen sind andere Mandanten, und wir haben Sicherheitsmaßnahmen, um zu verhindern, dass die Aktionen von einem Mandanten aus Beeinträchtigung der Sicherheit oder einen anderen Mandanten-Dienst oder den Zugriff auf die Inhalte von einer anderen Mandanten implementiert.

Zwei Hauptziele der Verwaltung der mandantenisolation in einer Umgebung mit mehreren Mandanten sind:
1.  Verhindern von Informationsverlusten oder nicht autorisierten Zugriff an Kunden Inhalte konstant; und
2.  Verhindert, dass die Aktionen des Mandanten eine Beeinträchtigung des Diensts für einen anderen Mandanten

Mehrere Formulare Schutz es wurden in Office 365 ein, um zu verhindern, dass Kunden aus Kompromisse bei Office 365-Diensten oder Anwendungen oder nicht autorisierten Zugriff auf die Informationen von anderen Mandanten oder das Office 365-System selbst, einschließlich der gesamten implementiert:
- Logischer Isolierung von Kunden von Inhalten innerhalb jeder Mandant für Office 365-Dienste wird durch die Azure Active Directory-Autorisierung und rollenbasierte Zugriffssteuerung erreicht.
- SharePoint Online bietet Daten Isolation Mechanismen auf Speicherebene.
- Microsoft verwendet strenge physische Sicherheit, Hintergrund und einer Verschlüsselungsstrategie für die mehrstufige, um die Vertraulichkeit und Integrität des Inhalts von Kunden zu schützen. Alle Office 365-Rechenzentren haben biometrische zugreifen auf Steuerelemente, mit der am häufigsten erfordern Palm druckt, physischen zuzugreifen. Darüber hinaus müssen alle US-basierten Microsoft-Mitarbeiter eine Prüfung standard Hintergrund als Teil der Einstellungsprozess erfolgreich abgeschlossen. Weitere Informationen zu den Steuerelementen für administrativen Zugriff in Office 365 verwendet finden Sie unter [Office 365 Administrative zugreifen auf Steuerelemente](office-365-administrative-access-controls-overview.md).
- Office 365 verwendet dienstseitige Technologien, mit denen Kunden Inhalte im Ruhezustand und bei der Übertragung, einschließlich BitLocker pro Datei-Verschlüsselung verschlüsselt Transport Layer Security (TLS) und Internet Protocol Security (IPsec). Ausführliche Informationen zur Verschlüsselung in Office 365 finden Sie unter [Data Encryption Technologies in Office 365](office-365-encryption-in-the-microsoft-cloud-overview.md).

Zusammen bilden die oben aufgelisteten Schutzebenen robuste logischen Isolierung Steuerelemente, die Schutz und zur Risikominderung entspricht, die durch die physische Isolation allein bereitgestellt.

## <a name="related-links"></a>Verwandte Links
- [Die Isolierung und Steuerung des Zugriffs in Azure Active Directory](office-365-isolation-in-azure-active-directory.md)
- [Mandanten Isolation im Büro Diagramm und eingegangen](office-365-isolation-in-graph-and-delve.md)
- [Mandantenisolation in Office 365-Suche](office-365-isolation-in-office-365-search.md)
- [Mandantenisolation in Office 365-Videos](office-365-isolation-in-office-365-video.md)
- [Ressourcengrenzen](office-365-resource-limits.md)
- [Überwachen und Testen von Mandanten Grenzen](office-365-monitoring-and-testing.md)
- [Die Isolierung und Steuerung des Zugriffs in Office 365](office-365-isolation-in-office-365.md)
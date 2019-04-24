---
title: Mandanten Isolation in Office 365
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
description: Eine Übersicht darüber, wie Microsoft die Mandanten Isolierung für Office 365 erzwingt.
ms.openlocfilehash: 87fd8cddce830ef58bcaa08462d6bcb120d1e05f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262377"
---
# <a name="tenant-isolation-in-office-365"></a>Mandanten Isolation in Office 365

Einer der Hauptvorteile von Cloud Computing ist das Konzept einer gemeinsam genutzten, gemeinsamen Infrastruktur für zahlreiche Kunden gleichzeitig, was zu Größenvorteilen führt. Dieses Konzept heißt *mehr Mandanten*Fähigkeit. Microsoft arbeitet kontinuierlich daran, sicherzustellen, dass die Multi-Mandanten-Architekturen unserer Cloud-Dienste unternehmensweite Sicherheits-, Vertraulichkeits-, Datenschutz-, Integritäts-und Verfügbarkeitsstandards unterstützen.

Basierend auf den erheblichen Investitionen und Erfahrungen aus [Trustworthy Computing](https://www.microsoft.com/en-us/twc/default.aspx) und dem [Sicherheits Entwicklungslebenszyklus](http://www.microsoft.com/security/sdl/default.aspx)wurden Microsoft Cloud Services mit der Annahme entworfen, dass alle Mandanten potenziell feindlich für alle sind. andere Mandanten, und wir haben Sicherheitsmaßnahmen ergriffen, um zu verhindern, dass die Aktionen eines Mandanten die Sicherheit oder den Dienst eines anderen Mandanten beeinträchtigen oder auf den Inhalt eines anderen Mandanten zugreifen.

Die beiden Hauptziele der Verwaltung der Mandanten Isolierung in einer Umgebung mit mehreren Mandanten sind:
1.  Verhindern des Auslaufens oder unbefugten Zugriffs auf Kunden Inhalte über Mandanten hinweg; und
2.  Verhindern, dass die Aktionen eines Mandanten sich negativ auf den Dienst für einen anderen Mandanten auswirken

In Office 365 wurden mehrere Schutzformen implementiert, um zu verhindern, dass Kunden Office 365-Dienste oder-Anwendungen kompromittieren oder nicht autorisierten Zugriff auf die Informationen anderer Mandanten oder des Office 365-Systems selbst erlangt haben, einschließlich:
- Die logische Isolierung von Kundeninhalten innerhalb der einzelnen Mandanten für Office 365-Dienste wird über die Azure Active Directory-Autorisierung und die rollenbasierte Zugriffssteuerung erreicht.
- SharePoint Online bietet Daten Isolationsmechanismen auf Speicherebene.
- Microsoft verwendet strenge physische Sicherheit, Hintergrundprüfung und eine mehrschichtige Verschlüsselungsstrategie, um die Vertraulichkeit und Integrität von Kundeninhalten zu schützen. Alle Office 365-Rechenzentren verfügen über biometrische Zugriffssteuerungen, wobei die meisten Palm-Drucke benötigen, um physischen Zugriff zu erhalten. Darüber hinaus sind alle US-amerikanischen Microsoft-Mitarbeiter verpflichtet, eine standardmäßige Hintergrundüberprüfung im Rahmen des Einstellungsprozesses erfolgreich abzuschließen. Weitere Informationen zu den Steuerelementen, die für den administrativen Zugriff in Office 365 verwendet werden, finden Sie unter [office 365 administrative Access Controls](office-365-administrative-access-controls-overview.md).
- In Office 365 werden Service seitige Technologien verwendet, die Kunden Inhalte auf Rest-und Transit Ebene verschlüsseln, einschließlich BitLocker, Dateiverschlüsselung, Transport Layer Security (TLS) und IPsec (Internet Protocol Security). Genauere Informationen zur Verschlüsselung in Office 365 finden Sie unter [Data Encryption Technologies in office 365](office-365-encryption-in-the-microsoft-cloud-overview.md).

Zusammenstellen die oben aufgeführten Schutzmechanismen zuverlässige Isolierungs Steuerelemente zur Verfügung, die den Schutz und die Minderung von Bedrohungen, die der physischen Isolierung dienen, gewährleisten.

## <a name="related-links"></a>Links zu verwandten Themen
- [Isolierung und Zugriffssteuerung in Azure Active Directory](office-365-isolation-in-azure-active-directory.md)
- [Mandantenisolation in Office Graph und Delve](office-365-isolation-in-graph-and-delve.md)
- [Mandantenisolation in der Office 365-Suche](office-365-isolation-in-office-365-search.md)
- [Mandantenisolation in Office 365 Video](office-365-isolation-in-office-365-video.md)
- [Ressourcenbeschränkungen](office-365-resource-limits.md)
- [Überwachen und Testen von Mandantengrenzen](office-365-monitoring-and-testing.md)
- [Isolierung und Zugriffskontrolle in Office 365](office-365-isolation-in-office-365.md)
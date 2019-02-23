---
title: Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Zusätzlich zum Office 365 Trust Center, das Sicherheits-, Datenschutz-und Kompatibilitätsinformationen für Office 365 bereitstellt, möchten Sie vielleicht wissen, wie Office 365 die von Ihnen bereitgestellten vertraulichen Daten in den Rechenzentren schützt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
ms.openlocfilehash: ba4c661899273f5e07c2468631298f5500d0e32f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218075"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online

In diesem Artikel wird beschrieben, wie Microsoft Ihre geheimen E-Mail-Daten in seinen Datencentern sichert.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Wie sichern wir geheime Informationen, die von Ihnen bereitgestellt werden?

Zusätzlich zum Office 365 Trust Center, das [Sicherheits-, Datenschutz-und Kompatibilitätsinformationen für office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, möchten Sie vielleicht wissen, wie Office 365 die von Ihnen bereitgestellten vertraulichen Daten in den Rechenzentren schützt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
  
Die verteilte Schlüsselverwaltung (DKM) ist eine clientseitige Funktionalität, die eine Reihe von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet. Nur Mitglieder einer bestimmten Sicherheitsgruppe in Active Directory-Domänendiensten können auf diese Schlüssel zugreifen, um die Daten zu entschlüsseln, die von DKM verschlüsselt wurden. In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe. Zum Standardverfahren im Datencenter gehört es, dass kein Benutzer Anmeldeinformationen erhält, die Teil dieser Sicherheitsgruppe sind. Daher hat keine Person Zugriff auf die Schlüssel, mit denen diese geheimen Daten entschlüsselt werden können.
  
Zu Debugging-, Problembehandlungs- oder Überwachungszwecken muss ein Datencenteradministrator erhöhte Rechte anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind. Dieser Vorgang erfordert mehrere Stufen rechtlicher Genehmigungen. Wenn der Zugriff gewährt wird, werden alle Aktivitäten protokolliert und überwacht. Darüber hinaus wird der Zugriff nur für einen bestimmten Zeitraum gewährt, danach läuft er automatisch ab.
  
Als zusätzliche Schutzmaßnahme umfasst die DKM-Technologie einen automatisierten Schlüsselrollover sowie automatische Archivierung. Dadurch wird sichergestellt, dass Sie weiterhin auf Ihre älteren Inhalte zugreifen können, ohne dabei auf unbestimmte Zeit den gleichen Schlüssel zu verwenden.

  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Wo wird DKM bei Exchange Online eingesetzt?

Microsoft verwendet DKM, um Ihre geheimen Daten in Exchange Online-Datencentern zu verschlüsseln. Beispiel:
  
- Anmeldeinformationen für E-Mail-Konten für verbundene Konten. Verbundene Konten sind Drittanbieterkonten wie Hotmail-, Gmail- und Yahoo!-E-Mail-Konten.
    
- RMS-Stammschlüssel. Dabei handelt es sich um Kundenschlüssel, die entweder aus Azure RMS oder aus der lokalen Active Directory-Domänendienste-Bereitstellungen des Kunden importiert werden, die zum Verschlüsseln und Entschlüsseln von e-Mails mit RMS oder Office 365 Message Encryption (OM) verwendet werden.
    
## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Details zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Dienstsicherheit im Office 365 Security &amp; Compliance Center](https://go.microsoft.com/fwlink/?linkid=874645)
  


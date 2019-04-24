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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255483"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online

In diesem Artikel wird beschrieben, wie Microsoft Ihre e-Mail-Geheimnisse in den Rechenzentren sichert.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Wie sichern wir geheime Informationen, die Ihnen zur Verfügung gestellt werden?

Zusätzlich zum Office 365 Trust Center, das [Sicherheits-, Datenschutz-und Kompatibilitätsinformationen für office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, möchten Sie vielleicht wissen, wie Office 365 die von Ihnen bereitgestellten vertraulichen Daten in den Rechenzentren schützt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
  
Distributed Key Manager (DKM) ist eine clientseitige Funktionalität, die einen Satz von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet. Nur Mitglieder einer bestimmten Sicherheitsgruppe in den Active Directory-Domänendiensten können auf diese Schlüssel zugreifen, um die mit DKM verschlüsselten Daten zu entschlüsseln. In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe. Als Teil der standardmäßigen Betriebs Prozedur im Datencenter erhält kein Mensch die Anmeldeinformationen, die Teil dieser Sicherheitsgruppe sind, und daher hat kein Mensch Zugriff auf die Schlüssel, die diese Geheimnisse entschlüsseln können.
  
Für Debugging-, Problem Behandlungs-oder Überwachungszwecke muss ein Datencenter-Administrator den erhöhten Zugriff anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind. Dieser Prozess erfordert mehrere rechtliche Genehmigungsstufen. Wenn der Zugriff erteilt wird, wird die gesamte Aktivität protokolliert und überwacht. Darüber hinaus wird der Zugriff nur für ein festgelegtes Zeitintervall gewährt, nach dem es automatisch abläuft.
  
Für zusätzlichen Schutz bietet die DKM-Technologie eine automatische Tasten Überschreitung und Archivierung. Dadurch wird auch sichergestellt, dass Sie weiterhin auf Ihren älteren Inhalt zugreifen können, ohne auf den gleichen Schlüssel unbegrenzt verlassen zu müssen.
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Wo verwendet Exchange Online DKM?

Microsoft verwendet DKM, um ihre Geheimnisse in Exchange Online-Rechenzentren zu verschlüsseln. Beispiel:
  
- E-Mail-Kontoanmeldeinformationen für verbundene Konten. Verbundene Konten sind Drittanbieter Konten wie Hotmail, Gmail und Yahoo!. e-Mail-Konten.
    
- RMS-Stammschlüssel. Dabei handelt es sich um Kundenschlüssel, die entweder aus Azure RMS oder aus der lokalen Active Directory-Domänendienste-Bereitstellungen des Kunden importiert werden, die zum Verschlüsseln und Entschlüsseln von e-Mails mit RMS oder Office 365 Message Encryption (OM) verwendet werden.
    
## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Details zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Dienstsicherheit im Office 365 Security &amp; Compliance Center](https://go.microsoft.com/fwlink/?linkid=874645)
  


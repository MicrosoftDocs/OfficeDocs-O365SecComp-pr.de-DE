---
title: Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Neben dem Office 365 Trust Center, das Informationen zu Sicherheit, Datenschutz und Compliance für Office 365 bereitstellt, sollten Sie wissen, wie Office 365 zum Schutz von in den Rechenzentren bereitgestellten Geheimnissen beiträgt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
ms.openlocfilehash: 609d59b6e4da779e0fa663b40fdbf26036753669
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154587"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online

In diesem Artikel wird beschrieben, wie Microsoft Ihre e-Mail-Geheimnisse in ihren Rechenzentren sichert.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Wie sichern wir geheime Informationen, die von Ihnen bereitgestellt werden?

Neben dem Office 365 Trust Center, das Informationen zu [Sicherheit, Datenschutz und Compliance für Office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, sollten Sie wissen, wie Office 365 zum Schutz von in den Rechenzentren bereitgestellten Geheimnissen beiträgt. Wir verwenden eine Technologie namens Distributed Key Manager (DKM).
  
Distributed Key Manager (DKM) ist eine clientseitige Funktionalität, die eine Reihe von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet. Nur Mitglieder einer bestimmten Sicherheitsgruppe in Active Directory-Domänendienste können auf diese Schlüssel zugreifen, um die von DKM verschlüsselten Daten zu entschlüsseln. In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe. Im Rahmen des standardmäßigen betriebsverfahrens im Rechenzentrum werden keinem Menschen Anmeldeinformationen zugewiesen, die Teil dieser Sicherheitsgruppe sind, und daher hat kein Mensch Zugriff auf die Schlüssel, die diese Geheimnisse entschlüsseln können.
  
Zum Debuggen, zur Problembehandlung oder zu Überwachungszwecken muss ein Rechenzentrums Administrator erhöhten Zugriff anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind. Für diesen Prozess sind mehrere Ebenen der rechtlichen Genehmigung erforderlich. Wenn der Zugriff gewährt wird, werden alle Aktivitäten protokolliert und überwacht. Darüber hinaus wird der Zugriff nur für ein festgelegtes Zeitintervall gewährt, nach dem es automatisch abläuft.
  
Für zusätzlichen Schutz umfasst die DKM-Technologie einen automatisierten Schlüssel Rollover und eine Archivierung. Dadurch wird auch sichergestellt, dass Sie weiterhin auf Ihre älteren Inhalte zugreifen können, ohne sich auf unbestimmte Zeit auf denselben Schlüssel verlassen zu müssen.
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Wo verwendet Exchange Online DKM?

Microsoft verwendet DKM, um ihre Geheimnisse in Exchange Online-Rechenzentren zu verschlüsseln. Zum Beispiel:
  
- E-Mail-Kontoanmeldeinformationen für verbundene Konten. Verbundene Konten sind Drittanbieter Konten wie Hotmail, Gmail und Yahoo!. e-Mail-Konten.
    
- RMS-Stammschlüssel (Rights Management Service, Rechteverwaltungsdienst). Hierbei handelt es sich um Kundenschlüssel, die entweder aus Azure RMS oder aus lokalen Active Directory-Domänendienste RMS-Bereitstellungen von Kunden importiert werden, die zum Verschlüsseln und Entschlüsseln von e-Mails mit RMS-oder Office 365-Nachrichtenverschlüsselung (OM) verwendet werden.
    
## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Details zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Dienst Assurance im Office 365 Security &amp; Compliance Center](https://go.microsoft.com/fwlink/?linkid=874645)
  


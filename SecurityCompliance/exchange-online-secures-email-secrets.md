---
title: Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
description: Zusätzlich zu Office 365 Trust Center die Sicherheit, Datenschutz und Kompatibilitätsdaten für Office 365 bereitstellt, ist möglicherweise möchten Sie wissen, Schutzmechanismen in Office 365 schützt Secrets, die Sie in den Datencentern bereitstellen. Wir verwenden eine Technologie namens verteilten Schlüssel Manager (DKM).
ms.openlocfilehash: a8fe1a2c9393958a391ec69a9a476a06de8c7576
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529975"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Schützen von vertraulichen Inhalten in E-Mails mit Exchange Online

In diesem Artikel wird beschrieben, wie Microsoft Ihre geheimen E-Mail-Daten in seinen Datencentern sichert.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Wie sichern wir geheime Informationen, die von Ihnen bereitgestellt werden?

Zusätzlich zu Office 365 Trust Center die [Sicherheit, Datenschutz und Kompatibilitätsdaten für Office 365](https://go.microsoft.com/fwlink/?linkid=874644)bereitstellt, ist möglicherweise möchten Sie wissen, Schutzmechanismen in Office 365 schützt Secrets, die Sie in den Datencentern bereitstellen. Wir verwenden eine Technologie namens verteilten Schlüssel Manager (DKM).
  
Die verteilte Schlüsselverwaltung (DKM) ist eine clientseitige Funktionalität, die eine Reihe von geheimen Schlüsseln zum Verschlüsseln und Entschlüsseln von Informationen verwendet. Nur Mitglieder einer bestimmten Sicherheitsgruppe in Active Directory-Domänendiensten können auf diese Schlüssel zugreifen, um die Daten zu entschlüsseln, die von DKM verschlüsselt wurden. In Exchange Online sind nur bestimmte Dienstkonten, unter denen die Exchange-Prozesse ausgeführt werden, Teil dieser Sicherheitsgruppe. Zum Standardverfahren im Datencenter gehört es, dass kein Benutzer Anmeldeinformationen erhält, die Teil dieser Sicherheitsgruppe sind. Daher hat keine Person Zugriff auf die Schlüssel, mit denen diese geheimen Daten entschlüsselt werden können.
  
Zu Debugging-, Problembehandlungs- oder Überwachungszwecken muss ein Datencenteradministrator erhöhte Rechte anfordern, um temporäre Anmeldeinformationen zu erhalten, die Teil der Sicherheitsgruppe sind. Dieser Vorgang erfordert mehrere Stufen rechtlicher Genehmigungen. Wenn der Zugriff gewährt wird, werden alle Aktivitäten protokolliert und überwacht. Darüber hinaus wird der Zugriff nur für einen bestimmten Zeitraum gewährt, danach läuft er automatisch ab.
  
Als zusätzliche Schutzmaßnahme umfasst die DKM-Technologie einen automatisierten Schlüsselrollover sowie automatische Archivierung. Dadurch wird sichergestellt, dass Sie weiterhin auf Ihre älteren Inhalte zugreifen können, ohne dabei auf unbestimmte Zeit den gleichen Schlüssel zu verwenden.

  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Wo wird DKM bei Exchange Online eingesetzt?

Microsoft verwendet DKM, um Ihre geheimen Daten in Exchange Online-Datencentern zu verschlüsseln. Beispiel:
  
- Anmeldeinformationen für E-Mail-Konten für verbundene Konten. Verbundene Konten sind Drittanbieterkonten wie Hotmail-, Gmail- und Yahoo!-E-Mail-Konten.
    
- Rights Management Service (RMS) Stammschlüssel. Dies sind die Kundenschlüssel, die entweder importiert von Azure RMS oder des Kunden lokale Active Directory Domain Services, RMS-Bereitstellungen, die zum Verschlüsseln und Entschlüsseln von e-Mail-Nachrichten mit RMS oder Office 365 Message Encryption (OME) verwendet werden.
    
## <a name="related-topics"></a>Verwandte Themen

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Referenz Details über die Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Service Assurance in die Office 365-Sicherheit &amp; Compliance Center](https://go.microsoft.com/fwlink/?linkid=874645)
  


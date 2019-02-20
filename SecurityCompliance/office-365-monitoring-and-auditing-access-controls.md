---
title: Office 365-Überwachungs-und-Überwachungs Zugriffssteuerungen
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
description: 'Zusammenfassung: eine Zusammenfassung der verschiedenen Überwachungs-und Überwachungs Zugriffssteuerelemente in Office 365.'
ms.openlocfilehash: 7a7023f61a72bd1368bb25754b33e40581a403b9
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090907"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>ÜberWachen und Überwachen von Zugriffssteuerungen in Office 365

Microsoft führt eine umfassende Überwachung und Überwachung aller Delegierung, aller Verwendung von Berechtigungen und aller Vorgänge in Office 365 aus. Die Office 365-Zugriffssteuerung ist ein automatisierter Prozess, der auf dem Prinzip der geringsten Rechte basiert und Datenzugriffs Steuerungen und-Prüfungen einbindet:
- Der gesamte zulässige Zugriff ist für einen eindeutigen Benutzer rückverfolgbar, sodass Administratoren für die Behandlung von Kundeninhalten verantwortlich sind.
- Zugriffssteuerungsanforderungen, Genehmigungen und administrative Betriebsprotokolle werden zur Analyse von Sicherheits Einblicken und bösartigen Ereignissen erfasst.
- Zugriffsebenen werden basierend auf der Mitgliedschaft in der Sicherheitsgruppe in nahezu Echtzeit überprüft, um sicherzustellen, dass nur Benutzer, die über autorisierte geschäftliche Gründe verfügen und die Berechtigungsanforderungen erfüllen, Zugriff auf die Systeme haben.
- Office 365, die Zugriffssteuerung und die unterstützenden Dienste, einschließlich Azure Active Directory und unserer physikalischen Datencenter, werden regelmäßig von unabhängigen Drittparteien für die Einhaltung von [ISO/iec 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [iso/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC)überwacht. [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)und andere [Standards](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Office 365-Ingenieure sind verpflichtet, jährliche Sicherheitsschulungen über die bewährten Methoden und Risiken für den erweiterten Zugriff zu Unternehmen und die Sicherheits-und Datenschutzrichtlinien von Microsoft anzuerkennen, um Ihre Ansprüche an den Dienst beizubehalten.

Automatisierte Warnungen werden ausgelöst, wenn verdächtige Aktivitäten erkannt werden, wie etwa mehrere fehlgeschlagene Anmeldungen innerhalb kurzer Zeit. Das Office 365 Security Response-Team verwendet Maschinelles Lernen und große Datenanalysen, um Aktivitäten für unregelmäßige Zugriffsmuster zu überprüfen und zu analysieren und proaktiv auf anomale und illegale Aktivitäten zu reagieren. Microsoft verwendet außerdem ein dediziertes Team von Penetrations Testern und engagiert sich in regelmäßigen Übungen mit roten Teams und blauen Teams, um Sicherheits-und Zugriffssteuerungsprobleme im Dienst zu finden. Kunden können die Effektivität der Zugriffs Steuerungssysteme auch überprüfen, indem Sie Überwachungsberichte und die von Office 365 bereitgestellte Verwaltungs Aktivitäts-API verwenden. 

Weitere Informationen finden Sie unter [office 365 Management Activity API Reference](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) and [Auditing and Reporting in Office 365](office-365-auditing-and-reporting-overview.md).

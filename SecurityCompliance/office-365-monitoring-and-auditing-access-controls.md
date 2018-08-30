---
title: Office 365 Überwachung und Prüfung zugreifen auf Steuerelemente
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
description: 'Zusammenfassung: Eine Zusammenfassung der verschiedenen Überwachung und Überwachung zugreifen auf Steuerelemente in Office 365 verfügbar.'
ms.openlocfilehash: 7ef25d62ce3c4fa320dd0b164183c6f67be7d76d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529971"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>Überwachung und Prüfung zugreifen auf Steuerelemente in Office 365

Microsoft führt umfassende Überwachung und Überprüfung von allen Delegierung, alle Verwendung von Berechtigungen und alle Vorgänge, die in Office 365 auftreten. Office 365 Access Steuerelement ist ein automatisierter Prozess auf dem Prinzip der geringsten Rechte und Zugreifen auf Steuerelemente von Daten und Überwachungen eingebunden erstellt:
- Alle zulässiger Zugriff lässt sich auf eine eindeutige Benutzer, die Administratoren für die Behandlung von Kunden Inhalt verantwortlich machen.
- Zugriffsanforderungen-Steuerelement, Genehmigungen und administrative Vorgänge protokolliert werden für die Analyse von Fakten zum Thema Sicherheit und bösartige Ereignisse erfasst.
- Zugriffsebenen werden in nahezu in Echtzeit basierend auf Sicherheitsgruppen-Mitgliedschaft um sicherzustellen, dass nur Benutzer, die Business Nachweise autorisiert haben und die Berechtigung erfüllen Zugriff auf den Systemen haben überprüft.
- Office 365, dessen zugreifen auf Steuerelemente und unterstützende Dienste, einschließlich Azure Active Directory und unsere physischen Rechenzentren, werden von unabhängigen Drittanbietern für die Einhaltung von [ISO/IEC 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC)regelmäßig überwacht, [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)und andere [Standards](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Office 365 Ingenieure sind erforderlich, jährliche-Schulung überprüfen mit erhöhten Rechten Access best Practices und Risiken und Microsofts Sicherheits- und Datenschutzauflagen beizubehalten, deren Berechtigungen für den Dienst zu bestätigen.

Automatisierte Benachrichtigungen werden ausgelöst, wenn verdächtiger Aktivitäten, wie mehrere fehlerhafte Anmeldungen innerhalb einer kurzen erkannt wird. Das Office 365 Security Response-Team verwendet Computer Lern- und big Datenanalyse überprüfen und Analysieren der Aktivität für unregelmäßige Access Muster und proaktiv auf abweichenden und unerlaubte Aktivitäten reagieren. Microsoft arbeitet ein engagierten Team von Durchdringungstester auch und abwickelt in regelmäßigen Rot Team und Blau Team Übungen finden Sicherheit und Kontrolle Probleme im Dienst zugreifen. Kunden können die Effektivität des Access-Verwaltungssysteme auch mithilfe von Überwachungsberichten und die Aktivität Management API von Office 365 überprüfen. 

Weitere Informationen finden Sie unter [Office 365 Management Aktivität-API-Referenz](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) und [Überwachung und Berichterstellung in Office 365](office-365-auditing-and-reporting-overview.md).

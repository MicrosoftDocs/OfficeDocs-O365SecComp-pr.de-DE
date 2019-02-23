---
title: Office 365 Umgang mit Datenbeschädigung
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
description: Eine Erläuterung der Datenbeschädigung in Office 365 und der Anstrengungen von Microsoft zur Vorbeugung und Wiederherstellung.
ms.openlocfilehash: d33cb298c432db45d560e4c2876d9ac34ab9d6f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216545"
---
# <a name="dealing-with-data-corruption-in-office-365"></a>Umgang mit Datenbeschädigungen in Office 365

Einer der herausfordernden Aspekte bei der Durchführung eines großen Cloud-Diensts ist die Handhabung von Datenbeschädigungen aufgrund der großen Datenmengen und unabhängigen Systeme. Datenbeschädigungen können durch folgende Ursachen verursacht werden:
- Anwendungs-oder Infrastrukturfehler, die teilweise oder vollständig den Anwendungsstatus korrumpieren 
- Hardware Probleme, die dazu führen, dass Daten verloren gehen oder Daten nicht gelesen werden können 
- Menschliche Betriebsfehler 
- Böswillige Hacker und verärgerte Mitarbeiter 
- VorFälle in externen Diensten, die zu einem Verlust von Daten führen 

Da eine höhere Ausfallsicherheit bei der Datenintegrität zu weniger Datenbeschädigungen führt, hat Microsoft in Office 365-Schutzmechanismen integriert, um eine Beschädigung zu vermeiden, sowie Systeme und Prozesse, die es uns ermöglichen, Daten wiederherzustellen, wenn dies der Fall ist. ÜberPrüfungen und Prozesse innerhalb der verschiedenen Phasen des Entwicklungsprozesses können Sie die Ausfallsicherheit bei Datenbeschädigungen verbessern, einschließlich:
- System Entwurf
- Code Organisation und-Struktur 
- Code Überprüfung 
- Komponententests, Integrationstests und Systemtests
- Test/Gates für Trip Wires 

In Office 365-Produktionsumgebungen stellt die Peer Replikation zwischen Rechenzentren sicher, dass immer mehrere Live Kopien von Daten vorhanden sind. Standard Bilder und Skripts werden zum Wiederherstellen verlorener Server verwendet, und replizierte Daten werden zum Wiederherstellen von Kundendaten verwendet. Aufgrund der integrierten Überprüfungen und Prozesse von Datenausfall Sicherheit verwaltet Microsoft nur die Dokumentation zu Office 365 Information System (einschließlich sicherheitsbezogener Dokumentation), wobei die integrierte Replikation in SharePoint Online und der interne Code verwendet werden. Repository-Tool, Quell Depot. Die Systemdokumentation wird in SharePoint Online gespeichert, und das Quell Depot enthält System-und Anwendungsabbilder. Sowohl SharePoint Online als auch Source Depot verwenden Versionsverwaltung und werden nahezu in Echtzeit repliziert. 
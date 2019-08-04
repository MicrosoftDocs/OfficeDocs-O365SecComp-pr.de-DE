---
title: Office 365 Umgang mit Datenbeschädigung
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
description: Eine Erläuterung der Datenbeschädigung in Office 365 und der Bemühungen von Microsoft um Verhinderung und Wiederherstellung.
ms.openlocfilehash: 4997ec0efb60d4e62e3a385af8bbd1a610c5290a
ms.sourcegitcommit: f0d23e57b00f07cef5b1b2d366eaeeeacda37e3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2019
ms.locfileid: "35786700"
---
# <a name="dealing-with-data-corruption-in-office-365"></a>Umgang mit Datenbeschädigung in Office 365

Einer der Herausforderungen bei der Ausführung eines umfangreichen Cloud-Diensts besteht darin, dass angesichts der großen Datenmengen und unabhängigen Systeme Datenbeschädigungen umgangen werden. Die Beschädigung von Daten kann durch folgende Ursachen verursacht werden:

- Anwendungs-oder Infrastrukturfehler, die einen oder alle Anwendungszustände beschädigen
- Hardware Probleme, die zu Datenverlusten oder zum Lesen von Daten führen können
- Menschliche Betriebsfehler
- Böswillige Hacker und verärgerte Mitarbeiter
- Vorfälle in externen Diensten, die zu einem Datenverlust führen

Da höhere Ausfallsicherheit in der Datenintegrität weniger Daten Beschädigungs Vorfälle bedeutet, hat Microsoft in Office 365 Schutzmechanismen integriert, um zu verhindern, dass eine Beschädigung stattfindet, sowie von Systemen und Prozessen, mit denen Daten wiederhergestellt werden können, wenn dies der Fall ist. Checks and Processes sind in den verschiedenen Phasen des Engineering-Release-Prozesses vorhanden, um die Ausfallsicherheit bei Datenbeschädigung zu verbessern, einschließlich:

- System Design
- Code Organisation und-Struktur
- Code Überprüfung
- Komponententests, Integrationstests und Systemtests
- Trip Wires-Tests/Tore

In Office 365 Produktionsumgebungen stellt die Peer Replikation zwischen Rechenzentren sicher, dass es immer mehrere Live Kopien aller Daten gibt. Standard Bilder und-Skripts werden verwendet, um verloren gegangene Server wiederherzustellen, und replizierte Daten werden verwendet, um Kundendaten wiederherzustellen. Aufgrund der integrierten Tests und Prozesse für die Ausfallsicherheit von Daten hält Microsoft Sicherungen nur von Office 365 Dokumentation zum Informationssystem (einschließlich sicherheitsbezogener Dokumentation) mit integrierter Replikation in SharePoint Online und unserem internen Code. Repository-Tool, Quell Depot. Die Systemdokumentation wird in SharePoint Online gespeichert, und das Quell Depot enthält System-und Anwendungsbilder. Sowohl SharePoint Online als auch das Quell Depot verwenden die Versionsverwaltung und werden nahezu in Echtzeit repliziert.

---
title: Office 365 Umgang mit beschädigte Daten
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
description: Eine Erläuterung der Beschädigung in Office 365 und seinen anstrengungen, der von Datenverlust und Wiederherstellung von Daten.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529543"
---
# <a name="dealing-with-data-corruption-in-office-365"></a>Umgang mit Beschädigung der Daten im Office 365

Einer der Herausforderung Aspekte der Ausführung eines umfangreichen Cloud-Diensts ist wie eine Beschädigung von Daten behandelt die große Menge von Daten und unabhängige Systeme angegeben. Beschädigte Daten kann folgende Ursachen haben:
- Anwendung oder Infrastruktur Bugs, zu beschädigen einige oder alle der Zustand der Anwendung 
- Hardware Probleme zur Folge verloren gegangene Daten oder ein Fehler beim Lesen von Daten 
- Human Ausführungsfehler 
- Hacker und unzufriedenen Mitarbeitern 
- Vorfälle in externe Dienste, die gewisser Datenverlust führen 

Da größere Flexibilität Datenintegrität weniger Daten Beschädigung Vorfälle bedeutet, hat Microsoft in Office 365 Schutzmechanismen zu verhindern, dass eine Beschädigung aus, um dies als auch Systemen und Prozessen, mit denen uns Daten wiederherstellen, wenn dies der Fall ist integriert. Prüfungen und Prozesse vorhanden innerhalb der verschiedenen Phasen des der engineering Freigabeprozess erhöhen Resiliency vor Beschädigung der Daten, einschließlich:
- Systementwurfs
- Code-Organisation und Struktur 
- Überprüfung des Codes 
- Komponententests Integrationstests und Systemtests
- Roundtrip verbindet Tests/gates 

In Office 365 produktionsumgebungen wird Peer-Replikation zwischen Rechenzentren, sind immer mehrere live Kopien der Daten sichergestellt. Standardgrafiken und Skripts dienen zum verloren Server wiederherzustellen, und replizierte Daten werden verwendet, um die Kundendaten wiederherstellen. Aufgrund der integrierten Daten Resiliency Prüfungen und Prozesse verwaltet Microsoft Sicherungen nur über Office 365 Informationen System-Dokumentation (einschließlich Sicherheits-Dokumentation), mit der integrierten Replikation in SharePoint Online und unsere internen code Repository Tool Quelldepot. Systemdokumentation ist in SharePoint Online gespeichert und Quelldepot System- und Bilder enthält. SharePoint Online und Quelldepot versionsverwaltung und nahezu in Echtzeit repliziert werden. 
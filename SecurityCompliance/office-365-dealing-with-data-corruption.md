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
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="6c199-103">Umgang mit Beschädigung der Daten im Office 365</span><span class="sxs-lookup"><span data-stu-id="6c199-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="6c199-p101">Einer der Herausforderung Aspekte der Ausführung eines umfangreichen Cloud-Diensts ist wie eine Beschädigung von Daten behandelt die große Menge von Daten und unabhängige Systeme angegeben. Beschädigte Daten kann folgende Ursachen haben:</span><span class="sxs-lookup"><span data-stu-id="6c199-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="6c199-106">Anwendung oder Infrastruktur Bugs, zu beschädigen einige oder alle der Zustand der Anwendung</span><span class="sxs-lookup"><span data-stu-id="6c199-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="6c199-107">Hardware Probleme zur Folge verloren gegangene Daten oder ein Fehler beim Lesen von Daten</span><span class="sxs-lookup"><span data-stu-id="6c199-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="6c199-108">Human Ausführungsfehler</span><span class="sxs-lookup"><span data-stu-id="6c199-108">Human operational errors</span></span> 
- <span data-ttu-id="6c199-109">Hacker und unzufriedenen Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="6c199-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="6c199-110">Vorfälle in externe Dienste, die gewisser Datenverlust führen</span><span class="sxs-lookup"><span data-stu-id="6c199-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="6c199-p102">Da größere Flexibilität Datenintegrität weniger Daten Beschädigung Vorfälle bedeutet, hat Microsoft in Office 365 Schutzmechanismen zu verhindern, dass eine Beschädigung aus, um dies als auch Systemen und Prozessen, mit denen uns Daten wiederherstellen, wenn dies der Fall ist integriert. Prüfungen und Prozesse vorhanden innerhalb der verschiedenen Phasen des der engineering Freigabeprozess erhöhen Resiliency vor Beschädigung der Daten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="6c199-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="6c199-113">Systementwurfs</span><span class="sxs-lookup"><span data-stu-id="6c199-113">System Design</span></span>
- <span data-ttu-id="6c199-114">Code-Organisation und Struktur</span><span class="sxs-lookup"><span data-stu-id="6c199-114">Code organization and structure</span></span> 
- <span data-ttu-id="6c199-115">Überprüfung des Codes</span><span class="sxs-lookup"><span data-stu-id="6c199-115">Code review</span></span> 
- <span data-ttu-id="6c199-116">Komponententests Integrationstests und Systemtests</span><span class="sxs-lookup"><span data-stu-id="6c199-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="6c199-117">Roundtrip verbindet Tests/gates</span><span class="sxs-lookup"><span data-stu-id="6c199-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="6c199-p103">In Office 365 produktionsumgebungen wird Peer-Replikation zwischen Rechenzentren, sind immer mehrere live Kopien der Daten sichergestellt. Standardgrafiken und Skripts dienen zum verloren Server wiederherzustellen, und replizierte Daten werden verwendet, um die Kundendaten wiederherstellen. Aufgrund der integrierten Daten Resiliency Prüfungen und Prozesse verwaltet Microsoft Sicherungen nur über Office 365 Informationen System-Dokumentation (einschließlich Sicherheits-Dokumentation), mit der integrierten Replikation in SharePoint Online und unsere internen code Repository Tool Quelldepot. Systemdokumentation ist in SharePoint Online gespeichert und Quelldepot System- und Bilder enthält. SharePoint Online und Quelldepot versionsverwaltung und nahezu in Echtzeit repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="6c199-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 
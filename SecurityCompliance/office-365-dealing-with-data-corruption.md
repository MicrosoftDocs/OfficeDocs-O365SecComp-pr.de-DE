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
description: Eine Erläuterung der Datenbeschädigung in Office 365 und der Anstrengungen von Microsoft zur Vorbeugung und Wiederherstellung.
ms.openlocfilehash: 9bf55243399ecd9f01f736e2da70d7c07231fa63
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262827"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="45566-103">Umgang mit Datenbeschädigungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="45566-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="45566-104">Einer der herausfordernden Aspekte bei der Durchführung eines großen Cloud-Diensts ist die Handhabung von Datenbeschädigungen aufgrund der großen Datenmengen und unabhängigen Systeme.</span><span class="sxs-lookup"><span data-stu-id="45566-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="45566-105">Datenbeschädigungen können durch folgende Ursachen verursacht werden:</span><span class="sxs-lookup"><span data-stu-id="45566-105">Data corruption can be caused by:</span></span>
- <span data-ttu-id="45566-106">Anwendungs-oder Infrastrukturfehler, die teilweise oder vollständig den Anwendungsstatus korrumpieren</span><span class="sxs-lookup"><span data-stu-id="45566-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="45566-107">Hardware Probleme, die dazu führen, dass Daten verloren gehen oder Daten nicht gelesen werden können</span><span class="sxs-lookup"><span data-stu-id="45566-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="45566-108">Menschliche Betriebsfehler</span><span class="sxs-lookup"><span data-stu-id="45566-108">Human operational errors</span></span> 
- <span data-ttu-id="45566-109">Böswillige Hacker und verärgerte Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="45566-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="45566-110">VorFälle in externen Diensten, die zu einem Verlust von Daten führen</span><span class="sxs-lookup"><span data-stu-id="45566-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="45566-111">Da eine höhere Ausfallsicherheit bei der Datenintegrität zu weniger Datenbeschädigungen führt, hat Microsoft in Office 365-Schutzmechanismen integriert, um eine Beschädigung zu vermeiden, sowie Systeme und Prozesse, die es uns ermöglichen, Daten wiederherzustellen, wenn dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="45566-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="45566-112">ÜberPrüfungen und Prozesse innerhalb der verschiedenen Phasen des Entwicklungsprozesses können Sie die Ausfallsicherheit bei Datenbeschädigungen verbessern, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="45566-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="45566-113">System Entwurf</span><span class="sxs-lookup"><span data-stu-id="45566-113">System Design</span></span>
- <span data-ttu-id="45566-114">Code Organisation und-Struktur</span><span class="sxs-lookup"><span data-stu-id="45566-114">Code organization and structure</span></span> 
- <span data-ttu-id="45566-115">Code Überprüfung</span><span class="sxs-lookup"><span data-stu-id="45566-115">Code review</span></span> 
- <span data-ttu-id="45566-116">Komponententests, Integrationstests und Systemtests</span><span class="sxs-lookup"><span data-stu-id="45566-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="45566-117">Test/Gates für Trip Wires</span><span class="sxs-lookup"><span data-stu-id="45566-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="45566-118">In Office 365-Produktionsumgebungen stellt die Peer Replikation zwischen Rechenzentren sicher, dass immer mehrere Live Kopien von Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="45566-118">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="45566-119">Standard Bilder und Skripts werden zum Wiederherstellen verlorener Server verwendet, und replizierte Daten werden zum Wiederherstellen von Kundendaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="45566-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="45566-120">Aufgrund der integrierten Überprüfungen und Prozesse von Datenausfall Sicherheit verwaltet Microsoft nur die Dokumentation zu Office 365 Information System (einschließlich sicherheitsbezogener Dokumentation), wobei die integrierte Replikation in SharePoint Online und der interne Code verwendet werden. Repository-Tool, Quell Depot.</span><span class="sxs-lookup"><span data-stu-id="45566-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="45566-121">Die Systemdokumentation wird in SharePoint Online gespeichert, und das Quell Depot enthält System-und Anwendungsabbilder.</span><span class="sxs-lookup"><span data-stu-id="45566-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="45566-122">Sowohl SharePoint Online als auch Source Depot verwenden Versionsverwaltung und werden nahezu in Echtzeit repliziert.</span><span class="sxs-lookup"><span data-stu-id="45566-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 
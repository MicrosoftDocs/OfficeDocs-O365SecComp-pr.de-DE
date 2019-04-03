---
title: Überwachen und melden des Sicherheitsstatus im Microsoft 365 Security Center
description: Beschreibt, wie das Microsoft 365 Security Center eine Zusammenfassung des Schutzes und des Sicherheitsstatus bietet.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Sicherheitscenter, Überwachung, Bericht, Status
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 0a0bcbde7daa79aabda30013fca2560384545feb
ms.sourcegitcommit: 8213c353954b92f5c3979bee4aa049da0fd28a18
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2019
ms.locfileid: "31043216"
---
# <a name="monitor-and-report-security-status-in-microsoft-365-security-center"></a><span data-ttu-id="36459-104">Überwachen und melden des Sicherheitsstatus im Microsoft 365 Security Center</span><span class="sxs-lookup"><span data-stu-id="36459-104">Monitor and report security status in Microsoft 365 security center</span></span>

<span data-ttu-id="36459-105">Das Microsoft 365-Sicherheitscenter bietet eine Übersicht über den Schutz-und Sicherheitsstatus in Ihrer Microsoft 365-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="36459-105">The Microsoft 365 security center provides at a glance summary of protection and security status across your Microsoft 365 environment.</span></span>

<span data-ttu-id="36459-106">Das Sicherheitscenter enthält einen Abschnitt zur **Überwachung von &-Berichten** mit zahlreichen Karten, die eine Vielzahl von Bereichen abdecken, die Sicherheitsanalysten und Administratoren als Teil ihres täglichen Betriebs verfolgen.</span><span class="sxs-lookup"><span data-stu-id="36459-106">The security center includes a **Monitoring & reports** section which features a host of cards covering a variety of areas that security analysts and administrators track as part of their day-to-day operations.</span></span> <span data-ttu-id="36459-107">Beim Drilldown bieten Karten detaillierte Berichte und in einigen Fällen Verwaltungsoptionen an.</span><span class="sxs-lookup"><span data-stu-id="36459-107">On drill-down, cards provide detailed reports and, in some cases, management options.</span></span>

## <a name="customize-views"></a><span data-ttu-id="36459-108">Anpassen von Ansichten</span><span class="sxs-lookup"><span data-stu-id="36459-108">Customize views</span></span>

<span data-ttu-id="36459-109">Überwachungs-und Berichts Karten werden standardmäßig in die folgenden Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="36459-109">By default, monitoring and report cards are grouped into these categories:</span></span>
  
* <span data-ttu-id="36459-110">[Identitäten](monitor-and-report-identities.md) – Benutzerkonten und Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="36459-110">[Identities](monitor-and-report-identities.md) – user accounts and credentials</span></span>
* <span data-ttu-id="36459-111">[Daten](monitor-data.md) – e-Mail-und Dokumentinhalte</span><span class="sxs-lookup"><span data-stu-id="36459-111">[Data](monitor-data.md) – email and document contents</span></span>
* <span data-ttu-id="36459-112">[Geräte](monitor-devices.md) – Computer, Mobiltelefone und andere Geräte</span><span class="sxs-lookup"><span data-stu-id="36459-112">[Devices](monitor-devices.md) – computers, mobile phones, and other devices</span></span>
* <span data-ttu-id="36459-113">[Apps](monitor-apps.md) – Programme und angeschlossene Onlinedienste</span><span class="sxs-lookup"><span data-stu-id="36459-113">[Apps](monitor-apps.md) – programs and attached online services</span></span>

<span data-ttu-id="36459-114">Wechseln Sie zu **Gruppieren nach Thema**, um die Karten neu anzuordnen und gruppieren Sie Sie wie folgt:</span><span class="sxs-lookup"><span data-stu-id="36459-114">Switch to **Group by topic**, to rearrange the cards and group them into the following:</span></span>

* <span data-ttu-id="36459-115">**Risiko** – Karten, die Entitäten wie Konten und Geräte hervorheben, die möglicherweise gefährdet sind.</span><span class="sxs-lookup"><span data-stu-id="36459-115">**Risk** – cards that highlight entities, such as accounts and devices, that might be at risk.</span></span> <span data-ttu-id="36459-116">Diese Karten stellen auch mögliche Risikoquellen hervor, beispielsweise neue Bedrohungs Kampagnen und privilegierte Cloud-apps.</span><span class="sxs-lookup"><span data-stu-id="36459-116">These cards also highlight possible sources of risk, such as new threat campaigns and privileged cloud apps</span></span>  
* <span data-ttu-id="36459-117">**Erkennungs Trends** – Karten, die neue Bedrohungserkennungen, Anomalien und Richtlinienverstöße hervorheben</span><span class="sxs-lookup"><span data-stu-id="36459-117">**Detection trends** – cards that highlight new threat detections, anomalies, and policy violations</span></span>
* <span data-ttu-id="36459-118">**Konfiguration und Integrität** – Karten, die die Konfiguration und Bereitstellung von Sicherheitskontrollen umfassen, einschließlich Geräte-Onboarding-Status für Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="36459-118">**Configuration and health** – cards that cover the configuration and deployment of security controls, including device onboarding states to management services</span></span>
* <span data-ttu-id="36459-119">**Sonstiges** – alle anderen Karten, die nicht unter andere Themen kategorisiert werden</span><span class="sxs-lookup"><span data-stu-id="36459-119">**Other** – all other cards not categorized under other topics</span></span>

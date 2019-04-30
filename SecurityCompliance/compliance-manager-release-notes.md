---
title: Microsoft Compliance Manager – Versionshinweise
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473090"
---
# <a name="release-notes-for-compliance-manager-preview"></a><span data-ttu-id="51b66-104">Versionshinweise für Compliance-Manager (Preview)</span><span class="sxs-lookup"><span data-stu-id="51b66-104">Release Notes for Compliance Manager (Preview)</span></span>

<span data-ttu-id="51b66-105">Mit der öffentlichen Vorschau des Compliance-Managers erhalten Sie frühzeitigen Zugriff auf bevorstehende Funktionen und Updates.</span><span class="sxs-lookup"><span data-stu-id="51b66-105">The public preview of Compliance Manager provides you with early access to upcoming functionality and updates.</span></span>

<span data-ttu-id="51b66-106">Sie können das aktualisierte [Compliance-Manager-](https://servicetrust.microsoft.com/ComplianceManager) Tool im [Service Trust Portal](https://servicetrust.microsoft.com) verwenden, um behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachzuverfolgen, zuzuweisen und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="51b66-106">You can use the updated [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) tool on the [Service Trust Portal](https://servicetrust.microsoft.com) to track, assign, and verify regulatory compliance activities related to Microsoft cloud services.</span></span>

## <a name="whats-new-in-compliance-manager-preview"></a><span data-ttu-id="51b66-107">Neuigkeiten im Compliance-Manager (Preview)</span><span class="sxs-lookup"><span data-stu-id="51b66-107">What’s new in Compliance Manager (Preview)</span></span>

- <span data-ttu-id="51b66-108">**Integration in Microsoft Secure Score:** Compliance-Manager unterstützt die Integration in [Microsoft Secure Score](microsoft-secure-score.md) , indem Kunden verwaltete Aktionen auf mehr als 50 Secure Score-Aktionen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="51b66-108">**Integration with Microsoft Secure Score:** Compliance Manager supports integration with [Microsoft Secure Score](microsoft-secure-score.md) by mapping customer-managed Actions to more than 50 Secure Score actions.</span></span> <span data-ttu-id="51b66-109">Wenn Sie eine zugeordnete Aktion in Secure Score ausführen, wird die entsprechende Compliance-Manager-Aktion automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="51b66-109">When you complete a mapped action in Secure Score, the corresponding Compliance Manager Action is automatically updated.</span></span>

- <span data-ttu-id="51b66-110">**Importieren von benutzerdefinierten Bewertungen:** Zusätzlich zu den integrierten Bewertungen unterstützt Compliance Manager jetzt das Importieren von benutzerdefinierten Vorlagen, sodass Sie benutzerdefinierte Bewertungen für ein beliebiges Produkt oder einen Dienst sowie alle Standard-oder Regulierungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="51b66-110">**Import custom Assessments:** In addition to built-in Assessments, Compliance Manager now supports importing custom Templates, enabling you to create custom Assessments for any product or service and any standard or regulation.</span></span>

- <span data-ttu-id="51b66-111">**Aktionselemente:** Aktionselemente sind jetzt einzelne Elemente, und viele enthalten Telemetrie-Sammlung von der Microsoft Secure Score Graph-API.</span><span class="sxs-lookup"><span data-stu-id="51b66-111">**Actions Items:** Action Items are now individual items and many include telemetry collection from the Microsoft Secure Score Graph API.</span></span> <span data-ttu-id="51b66-112">Soweit möglich, haben die Empfehlungen für Technische Aktionen jetzt Links zur entsprechenden Konfigurationsseite im Office 365-Dienst.</span><span class="sxs-lookup"><span data-stu-id="51b66-112">Where possible, technical action recommendations now have links to the applicable configuration page in the Office 365 service.</span></span>

- <span data-ttu-id="51b66-113">**Mandantenverwaltung:** Neue Schnittstelle zum Verwalten neuer Datenelemente im Compliance-Manager (Preview):</span><span class="sxs-lookup"><span data-stu-id="51b66-113">**Tenant Management:** New interface for managing new data elements in Compliance Manager (Preview):</span></span>
    - <span data-ttu-id="51b66-114">**Dimensionen:** Anzeigen, hinzufügen und Anpassen von Metadaten für Vorlagen, BEWERTUNGEN und Aktionselemente, mit denen Sie benutzerdefinierte Pivots für Filter erstellen können.</span><span class="sxs-lookup"><span data-stu-id="51b66-114">**Dimensions:** View, add and customize metadata for Templates, Assessments, and Action Items that allow you to create custom pivots for filters.</span></span>
    - <span data-ttu-id="51b66-115">**Besitzer:** Geben Sie einen Besitzer für jedes Aktionselement an.</span><span class="sxs-lookup"><span data-stu-id="51b66-115">**Owners:** Specify an owner for each Action Item.</span></span>
    - <span data-ttu-id="51b66-116">**Kundenaktionen:** Verwalten der vollständigen Liste der im Compliance-Manager (Preview) enthaltenen Aktionen und aktivieren/deaktivieren der Überwachung der sicheren Bewertung für Aktionselemente, die mit Secure Score integriert sind.</span><span class="sxs-lookup"><span data-stu-id="51b66-116">**Customer Actions:** Manage the complete list of Actions Items included in Compliance Manager (Preview) and enable/disable Secure Score monitoring for Action Items that are integrated with Secure Score.</span></span>

- <span data-ttu-id="51b66-117">**Aktualisierte Kompatibilitätsbewertung**: die Methodik wurde geändert, um die Synchronisierung mit Microsoft Secure Score zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51b66-117">**Updated Compliance Score**: The methodology has changed to support syncing with Microsoft Secure Score.</span></span> <span data-ttu-id="51b66-118">Das scoringsystem entfernt die von Microsoft verwalteten Steuerelemente und konzentriert sich ausschließlich auf den Abschluss von vom Kunden verwalteten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="51b66-118">The scoring system removes the Microsoft-managed control credits and focuses solely on the completion of customer-managed controls.</span></span>

## <a name="known-issues-in-compliance-manager-preview"></a><span data-ttu-id="51b66-119">Bekannte Probleme im Compliance-Manager (Preview)</span><span class="sxs-lookup"><span data-stu-id="51b66-119">Known issues in Compliance Manager (Preview)</span></span>

<span data-ttu-id="51b66-120">In den folgenden Abschnitten werden bekannte Probleme behandelt, die in kommenden Versionen von Compliance-Manager behoben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51b66-120">The following sections cover known issues to be resolved in upcoming releases of Compliance Manager.</span></span>

### <a name="compliance-score"></a><span data-ttu-id="51b66-121">KonformitätsBewertung</span><span class="sxs-lookup"><span data-stu-id="51b66-121">Compliance Score</span></span>

- <span data-ttu-id="51b66-122">Wenn Aktionselemente als **nicht im Bereich**gekennzeichnet sind, wird die dem Aktionselement zugewiesene Bewertung nicht aus der Berechnung der Kompatibilitätsbewertung ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51b66-122">When Action Items are marked as **Not in Scope**, the score assigned to the Action Item is not excluded from the Compliance Score calculation.</span></span> <span data-ttu-id="51b66-123">Aktionselemente, die **nicht im Bereich** markiert sind, sollten ihre Konformitätsbewertung nicht verlängern.</span><span class="sxs-lookup"><span data-stu-id="51b66-123">Action Items marked **Not in Scope** should not increase your Compliance Score.</span></span>

### <a name="microsoft-managed-controls"></a><span data-ttu-id="51b66-124">Von Microsoft verwaltete Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="51b66-124">Microsoft-managed Controls</span></span>

- <span data-ttu-id="51b66-125">Das Test Datum für von Microsoft verwaltete Steuerelemente wird nicht auf der Benutzeroberfläche angezeigt, selbst wenn diese in die Bewertung einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="51b66-125">The test date for Microsoft-managed controls is not appearing in the UI, even when included in the Assessment.</span></span> <span data-ttu-id="51b66-126">Zum Anzeigen von Informationen zum Test Datum müssen Sie die Bewertung exportieren.</span><span class="sxs-lookup"><span data-stu-id="51b66-126">To see test date information, you must export the Assessment.</span></span>

### <a name="customization"></a><span data-ttu-id="51b66-127">Anpassung</span><span class="sxs-lookup"><span data-stu-id="51b66-127">Customization</span></span>

- <span data-ttu-id="51b66-128">Durch das Hinzufügen von benutzerdefinierten Steuerelementen kann ein neues Steuerelement zu einer vorhandenen Steuerelement Familie hinzugefügt werden, es ist jedoch nicht möglich, eine neue Steuerelement Familie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="51b66-128">Adding custom Controls enables adding a new control to an existing control family, but it does not allow you to add a new Control Family.</span></span>
- <span data-ttu-id="51b66-129">Diese Release unterstützt keine Verknüpfung von Aktionselementen oder Hinzufügen von Aktionen Elemente oder Steuerelemente zu einer Bewertung.</span><span class="sxs-lookup"><span data-stu-id="51b66-129">This release does not support linking Action Items or adding Actions Items or Controls to an Assessment.</span></span>
- <span data-ttu-id="51b66-130">Wenn Sie eine benutzerdefinierte Aktion erstellen, können Sie Sie nicht bearbeiten oder löschen.</span><span class="sxs-lookup"><span data-stu-id="51b66-130">If you create a custom Action, you cannot edit or delete it.</span></span>

### <a name="control-families-not-shown-in-assessments"></a><span data-ttu-id="51b66-131">Steuern von Familien, die nicht in Bewertungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="51b66-131">Control Families Not Shown in Assessments</span></span>

- <span data-ttu-id="51b66-132">Wenn Sie eine Vorlage importieren, reflektieren alle auf dieser Vorlage basierenden Bewertungen alle Steuerelementfamilien, die Teil der Vorlage sind.</span><span class="sxs-lookup"><span data-stu-id="51b66-132">When you import a Template, all Assessments based on that Template will reflect all Control Families that are part of the Template.</span></span> <span data-ttu-id="51b66-133">Wenn Sie jedoch der Vorlage neue Steuerelementfamilien hinzufügen, werden die Änderungen durch vorhandene Bewertungen nicht widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="51b66-133">But if you add new Control Families to the Template, any existing Assessments will not reflect the changes.</span></span> <span data-ttu-id="51b66-134">Nur neue Bewertungen, die aus der aktualisierten Vorlage erstellt wurden, spiegeln die Änderungen wider.</span><span class="sxs-lookup"><span data-stu-id="51b66-134">Only new Assessments created off the updated Template will reflect the changes.</span></span>

### <a name="filters"></a><span data-ttu-id="51b66-135">Filter</span><span class="sxs-lookup"><span data-stu-id="51b66-135">Filters</span></span>

- <span data-ttu-id="51b66-136">Das Filtern von Aktionselementen oder Steuerelementen führt nicht konsistent zu korrekten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="51b66-136">Filtering on Action Items or Controls does not consistently produce correct results.</span></span>

### <a name="templates"></a><span data-ttu-id="51b66-137">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="51b66-137">Templates</span></span>

- <span data-ttu-id="51b66-138">Archivierte Vorlagen können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="51b66-138">Archived templates are editable and they should not be editable.</span></span>
- <span data-ttu-id="51b66-139">Gesperrte Vorlagen ermöglichen die Erstellung von Bewertungen, wenn Sie dies nicht tun sollten.</span><span class="sxs-lookup"><span data-stu-id="51b66-139">Locked templates allow for Assessment creation when they should not.</span></span> <span data-ttu-id="51b66-140">Das Sperren einer Vorlage soll verhindern, dass Sie zum Erstellen von Bewertungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51b66-140">Locking a Template is meant to prevent it from being used to create Assessments.</span></span>

### <a name="export"></a><span data-ttu-id="51b66-141">Exportieren</span><span class="sxs-lookup"><span data-stu-id="51b66-141">Export</span></span>

- <span data-ttu-id="51b66-142">Der Vorlagenexport in JSON schlägt fehl, wenn der Vorlagenstatus auf " **importiert** " oder "Ausstehend" festgelegt ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="51b66-142">Template export to JSON fails when the template status is set to **Imported** or **Pending Approval**.</span></span>

### <a name="supported-browsers"></a><span data-ttu-id="51b66-143">Unterstützte Browser</span><span class="sxs-lookup"><span data-stu-id="51b66-143">Supported browsers</span></span>

- <span data-ttu-id="51b66-144">Die neuesten Versionen von Microsoft Edge, Chrome und Safari werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51b66-144">The latest versions of Microsoft Edge, Chrome, and Safari are supported.</span></span>
- <span data-ttu-id="51b66-145">Es kann vorkommen, dass aktualisierte Daten erst angezeigt werden, wenn Ihr Browser aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="51b66-145">There may be instances where updated data does not appear until your browser is refreshed.</span></span>
- <span data-ttu-id="51b66-146">Die Vorschauversion von Microsoft Edge wird nicht unterstützt, hat aber keine bekannten Probleme.</span><span class="sxs-lookup"><span data-stu-id="51b66-146">The preview version of Microsoft Edge is not supported but has no known issues.</span></span>
- <span data-ttu-id="51b66-147">Internet Explorer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51b66-147">Internet Explorer is not supported.</span></span>

### <a name="session-timeout"></a><span data-ttu-id="51b66-148">Sitzungstimeout</span><span class="sxs-lookup"><span data-stu-id="51b66-148">Session timeout</span></span>

- <span data-ttu-id="51b66-149">Wenn eine Sitzung ausläuft, wird möglicherweise ein Fehler "etwas schief gelaufen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51b66-149">When a session times out, a “Something went wrong” error may appear.</span></span> <span data-ttu-id="51b66-150">Wechseln Sie zur Lösung des [Kompatibilitäts-Managers](https://servicetrust.microsoft.com/ComplianceManager) , und melden Sie sich erneut an.</span><span class="sxs-lookup"><span data-stu-id="51b66-150">To resolve, go to [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) and log in again.</span></span>
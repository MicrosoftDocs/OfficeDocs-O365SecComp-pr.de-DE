---
title: Übersicht über den Dateiplan-Manager
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen, Aufbewahrungsbezeichnungsrichtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.
ms.openlocfilehash: b7d80ff6a7f78e592462fe2723a87383e046015f
ms.sourcegitcommit: 6eb51931242d07abde2e37f1bd57d13bc724f0de
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34547970"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="24d66-103">Übersicht über den Dateiplan-Manager</span><span class="sxs-lookup"><span data-stu-id="24d66-103">Overview of file plan manager</span></span>

<span data-ttu-id="24d66-104">Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen, Aufbewahrungsbezeichnungsrichtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.</span><span class="sxs-lookup"><span data-stu-id="24d66-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Dateiplanseite](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="24d66-106">Zugriff auf den Dateiplan-Manager</span><span class="sxs-lookup"><span data-stu-id="24d66-106">Accessing file plan manager</span></span>

<span data-ttu-id="24d66-107">Es gibt die folgenden beiden Anforderungen für den Zugriff auf den Dateiplan-Manager:</span><span class="sxs-lookup"><span data-stu-id="24d66-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="24d66-108">Ein Office 365 Enterprise E5-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24d66-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="24d66-109">Der Benutzer wurde einer der folgenden Rollen des Security &amp; Compliance Centers zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="24d66-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="24d66-110">Aufbewahrungs-Manager</span><span class="sxs-lookup"><span data-stu-id="24d66-110">Retention Manager</span></span>
    - <span data-ttu-id="24d66-111">Aufbewahrungs-Manager (schreibgeschützt)</span><span class="sxs-lookup"><span data-stu-id="24d66-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="24d66-112">Standardmäßige Aufbewahrungsbezeichnung und Bezeichnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="24d66-112">Default retention labels and label policy</span></span>

<span data-ttu-id="24d66-113">Wenn keine Aufbewahrungsbezeichnungen im Security & Compliance Center vorhanden sind, wird, wenn Sie im linken Navigationsbereich **Dateiplan** auswählen, eine Bezeichnungsrichtlinie mit dem Namen **Standardmäßige Veröffentlichungsrichtlinie für Datengovernance** erstellt.</span><span class="sxs-lookup"><span data-stu-id="24d66-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="24d66-114">Diese Bezeichnungsrichtlinie enthält drei Aufbewahrungsbezeichnungen:</span><span class="sxs-lookup"><span data-stu-id="24d66-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="24d66-115">**Operative Prozesse**</span><span class="sxs-lookup"><span data-stu-id="24d66-115">**Operational procedure**</span></span>
- <span data-ttu-id="24d66-116">**Allgemeines Geschäft**</span><span class="sxs-lookup"><span data-stu-id="24d66-116">**Business general**</span></span>
- <span data-ttu-id="24d66-117">**Vertragliche Vereinbarung**</span><span class="sxs-lookup"><span data-stu-id="24d66-117">**Contract agreement**</span></span>

<span data-ttu-id="24d66-118">Diese Aufbewahrungsbezeichnungen sind so konfiguriert, dass Inhalte nur aufbewahrt, aber nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="24d66-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="24d66-119">Diese Bezeichnungsrichtlinie wird in der gesamten Organisation veröffentlicht und kann deaktiviert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="24d66-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="24d66-120">Sie können feststellen, wer den Dateiplan-Manager geöffnet und den Eindruck beim ersten Ausführen gestartet hat, indem Sie das Überwachungsprotokoll für die Aktivitäten **Erstellte Aufbewahrungsrichtlinie** und **Erstellte Konfiguration für eine Aufbewahrungsrichtlinie** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="24d66-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="24d66-121">Aufgrund von Kundenfeedback haben wir dieses Feature entfernt, durch das die standardmäßigen Aufbewahrungsbezeichnungen und die oben genannte Aufbewahrungsbezeichnungsrichtlinie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24d66-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="24d66-122">Diese Aufbewahrungsbezeichnungen und Aufbewahrungsbezeichnungsrichtlinien werden Ihnen nur dann angezeigt, wenn Sie den Datei-Plan-Manager vor dem 11. April 2019 geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="24d66-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="24d66-123">Navigieren in Ihrem Dateiplan</span><span class="sxs-lookup"><span data-stu-id="24d66-123">Navigating your file plan</span></span>

<span data-ttu-id="24d66-124">Mit dem Dateiplan-Manager können Sie leichter die Einstellungen aller Aufbewahrungsbezeichnungen und Richtlinien aus einer Ansicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="24d66-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="24d66-125">Beachten Sie, dass Aufbewahrungsbezeichnungen, die außerhalb des Dateiplans erstellt wurden, im Dateiplan verfügbar sind und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="24d66-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="24d66-126">Auf den Registerkarten für die **Dateiplanbezeichnungen** sind die folgenden zusätzlichen Informationen und Funktionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="24d66-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="24d66-127">Spalten mit Bezeichnungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="24d66-127">Label settings columns</span></span>

- <span data-ttu-id="24d66-p103">**Basierend auf** gibt den Typ des Auslösers an, der den Aufbewahrungszeitraum starten kann. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24d66-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="24d66-130">Ereignis</span><span class="sxs-lookup"><span data-stu-id="24d66-130">Event</span></span>
    - <span data-ttu-id="24d66-131">Zeitpunkt der Erstellung</span><span class="sxs-lookup"><span data-stu-id="24d66-131">When created</span></span>
    - <span data-ttu-id="24d66-132">Zeitpunkt der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="24d66-132">When last modified</span></span>
    - <span data-ttu-id="24d66-133">Zeitpunkt der Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="24d66-133">When labeled</span></span>
- <span data-ttu-id="24d66-p104">**Datensatz** gibt an, ob das Element ein deklarierter Datensatz werden kann, wenn die Bezeichnung angewendet wurde. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24d66-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="24d66-136">Nein</span><span class="sxs-lookup"><span data-stu-id="24d66-136">No</span></span>
    - <span data-ttu-id="24d66-137">Ja</span><span class="sxs-lookup"><span data-stu-id="24d66-137">Yes</span></span>
    - <span data-ttu-id="24d66-138">Yes (Vorgeschrieben)</span><span class="sxs-lookup"><span data-stu-id="24d66-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="24d66-p105">**Aufbewahrung** gibt den Aufbewahrungstyp an. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24d66-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="24d66-141">Beibehalten</span><span class="sxs-lookup"><span data-stu-id="24d66-141">Keep</span></span>
    - <span data-ttu-id="24d66-142">Beibehalten und löschen</span><span class="sxs-lookup"><span data-stu-id="24d66-142">Keep and delete</span></span>
    - <span data-ttu-id="24d66-143">Löschen</span><span class="sxs-lookup"><span data-stu-id="24d66-143">Delete</span></span>
- <span data-ttu-id="24d66-p106">**Disposition** gibt an, was mit dem Inhalt am Ende des Aufbewahrungszeitraums geschieht. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24d66-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="24d66-146">Null</span><span class="sxs-lookup"><span data-stu-id="24d66-146">null</span></span>
    - <span data-ttu-id="24d66-147">Keine Aktion</span><span class="sxs-lookup"><span data-stu-id="24d66-147">No action</span></span>
    - <span data-ttu-id="24d66-148">Automatisch löschen</span><span class="sxs-lookup"><span data-stu-id="24d66-148">Auto-delete</span></span>
    - <span data-ttu-id="24d66-149">Überprüfung erforderlich (auch bezeichnet als Dispositionsprüfung)</span><span class="sxs-lookup"><span data-stu-id="24d66-149">Review required (aka Disposition review)</span></span>

![Bezeichnungseinstellungen im Dateiplan](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a><span data-ttu-id="24d66-151">Spalten mit Dateiplanbeschreibungen für Aufbewahrungsbezeichnungen</span><span class="sxs-lookup"><span data-stu-id="24d66-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="24d66-p107">Sie können nun mehr Informationen in die Konfiguration Ihrer Aufbewahrungsbezeichnungen einschließen. Durch Einfügen von Dateiplanbeschreibungen in Aufbewahrungsbezeichnungen können Sie die Verwaltbarkeit und Organisation Ihres Dateiplans verbessern.</span><span class="sxs-lookup"><span data-stu-id="24d66-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="24d66-p108">Für den Einstieg stellt Dateiplan-Manager einige einsatzbereite Werte für Folgendes bereit: Funktion/Abteilung, Kategorie, Autoritätstyp und Bereitstellung. Sie können neue Werte für die Dateiplanbeschreibung hinzufügen, wenn Sie eine Aufbewahrungsbezeichnung erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="24d66-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="24d66-156">Nachfolgend finden Sie eine Übersicht der Dateiplanbeschreibungen beim Erstellen oder Bearbeiten einer Aufbewahrungsbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="24d66-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Dateiplanbeschreibungen](media/file-plan-descriptors.png)

<span data-ttu-id="24d66-158">Nachfolgend finden Sie eine Übersicht über die Spalten mit Dateiplanbeschreibungen auf der Registerkarte „Bezeichnungen“ des Dateiplan-Managers.</span><span class="sxs-lookup"><span data-stu-id="24d66-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a><span data-ttu-id="24d66-160">Exportieren aller vorhandenen Aufbewahrungsbezeichnungen zum Analysieren und/oder Durchführen von Offline Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="24d66-160">Export all existing retention labels to analyze and/or perform offline reviews</span></span>

<span data-ttu-id="24d66-161">Aus dem Dateiplan-Manager können Sie die Details aller Aufbewahrungsbezeichnungen in eine CSV-Datei exportieren, mit deren Hilfe Sie regelmäßige Complianceüberprüfungen mit den Beteiligten an der Datengovernance in Ihrer Organisation durchführen können.</span><span class="sxs-lookup"><span data-stu-id="24d66-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="24d66-162">Um alle Aufbewahrungsbezeichnungen zu exportieren, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen exportieren**.</span><span class="sxs-lookup"><span data-stu-id="24d66-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Option zum Exportieren des Dateiplans](media/file-plan-export-labels-option.png)

<span data-ttu-id="24d66-164">Es wird eine CSV-Datei mit allen vorhandenen Aufbewahrungsbeschriftungen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="24d66-164">A \*.csv file containing all existing retention labels will open.</span></span>

![CSV-Datei, in der alle Aufbewahrungsbeschriftungen angezeigt werden](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a><span data-ttu-id="24d66-166">Importieren von Aufbewahrungsbezeichnungen in Ihren Dateiplan</span><span class="sxs-lookup"><span data-stu-id="24d66-166">Import labels into your file plan</span></span>

<span data-ttu-id="24d66-167">Aus dem Dateiplan-Manager können Sie neue Aufbewahrungsbezeichnungen massenimportieren und vorhandene Aufbewahrungsbezeichnungen ändern.</span><span class="sxs-lookup"><span data-stu-id="24d66-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="24d66-168">Zum Importieren von neuen Aufbewahrungsbeschriftungen und zum Aktualisieren von vorhandenen Aufbewahrungsbezeichnungen gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen importieren**.</span><span class="sxs-lookup"><span data-stu-id="24d66-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Option zum Importieren des Dateiplans](media/file-plan-import-labels-option.png)

![Option zum Herunterladen einer leeren Vorlage für den Dateiplan](media/file-plan-blank-template-option.png)

<span data-ttu-id="24d66-171">Laden Sie eine leere Vorlage herunter (oder beginnen Sie mit einem Export Ihres aktuellen Dateiplans).</span><span class="sxs-lookup"><span data-stu-id="24d66-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Leere Vorlage eines Dateiplans, geöffnet in Excel](media/file-plan-blank-template.png)

<span data-ttu-id="24d66-173">Füllen Sie die Vorlage aus (in Kürze verfügbar: Referenzinformationen zu gültigen Wertkombinationen für ein einzelne Aufbewahrungsbezeichnung).</span><span class="sxs-lookup"><span data-stu-id="24d66-173">Fill-out the template (coming soon: reference information about valid value combinations for a single retention label).</span></span>

![Dateiplanvorlage mit ausgefüllten Informationen](media/file-plan-filled-out-template.png)

<span data-ttu-id="24d66-175">Laden Sie die ausgefüllte Vorlage hoch; die Einträge werden dann vom Dateiplan-Manager überprüft, und es werden Importstatistiken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24d66-175">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Dateiplan-Importstatistiken](media/file-plan-import-statistics.png)

<span data-ttu-id="24d66-177">Für den Fall, dass ein Überprüfungsfehler vorliegt, überprüft der Dateiplanimport weiterhin jeden Eintrag in der Importdatei und zeigt alle Fehler an, wobei er die Zeilen-/Reihennummern in der Importdatei referenziert und die angezeigten Fehlerergebnisse kopiert, damit Sie einfach zur Importdatei zurückkehren und die Fehler korrigieren können.</span><span class="sxs-lookup"><span data-stu-id="24d66-177">In the event there is a validation error, file plan import will continue to validate every entry in the import file and display all errors referencing line/row numbers in the import file, copy the displayed error results so that you can easilly return to the import file and correct the errors.</span></span> 

<span data-ttu-id="24d66-178">Wenn der Importvorgang abgeschlossen ist, kehren Sie zum Dateiplan-Manager zurück, um neuen oder vorhandenen Aufbewahrungsbezeichnungsrichtlinien neue Aufbewahrungsbezeichnungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="24d66-178">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Option zum Veröffentlichen von Bezeichnungen](media/file-plan-publish-labels-option.png)


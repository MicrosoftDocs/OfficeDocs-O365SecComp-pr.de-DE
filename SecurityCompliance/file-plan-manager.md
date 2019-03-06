---
title: Übersicht über den Dateiplan-Manager
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen und Richtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.
ms.openlocfilehash: 328b8f1aeed3e25fb0ab5eb651fb3846b123747c
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410520"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="49aa8-103">Übersicht über den Dateiplan-Manager</span><span class="sxs-lookup"><span data-stu-id="49aa8-103">Overview of file plan manager</span></span>

<span data-ttu-id="49aa8-104">Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen und Richtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.</span><span class="sxs-lookup"><span data-stu-id="49aa8-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Dateiplanseite](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="49aa8-106">Zugriff auf den Dateiplan-Manager</span><span class="sxs-lookup"><span data-stu-id="49aa8-106">Accessing file plan manager</span></span>

<span data-ttu-id="49aa8-107">Es gibt die folgenden beiden Anforderungen für den Zugriff auf den Dateiplan-Manager:</span><span class="sxs-lookup"><span data-stu-id="49aa8-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="49aa8-108">Ein Office 365 Enterprise E5-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49aa8-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="49aa8-109">Der Benutzer wurde einer der folgenden Rollen des Security &amp; Compliance Centers zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="49aa8-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="49aa8-110">Aufbewahrungs-Manager</span><span class="sxs-lookup"><span data-stu-id="49aa8-110">Retention Manager</span></span>
    - <span data-ttu-id="49aa8-111">Aufbewahrungs-Manager (schreibgeschützt)</span><span class="sxs-lookup"><span data-stu-id="49aa8-111">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="49aa8-112">Navigieren in Ihrem Dateiplan</span><span class="sxs-lookup"><span data-stu-id="49aa8-112">Navigating your file plan</span></span>

<span data-ttu-id="49aa8-113">Mit dem Dateiplan-Manager können Sie leichter die Einstellungen aller Aufbewahrungsbezeichnungen und Richtlinien aus einer Ansicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="49aa8-113">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="49aa8-114">Beachten Sie, dass Aufbewahrungsbezeichnungen, die außerhalb des Dateiplans erstellt wurden, im Dateiplan verfügbar sind und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="49aa8-114">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="49aa8-115">Auf den Registerkarten für die **Dateiplanbezeichnungen** sind die folgenden zusätzlichen Informationen und Funktionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="49aa8-115">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="49aa8-116">Spalten mit Bezeichnungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="49aa8-116">Label settings columns</span></span>
 
- <span data-ttu-id="49aa8-p101">**Basierend auf** gibt den Typ des Auslösers an, der den Aufbewahrungszeitraum starten kann. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49aa8-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="49aa8-119">Ereignis</span><span class="sxs-lookup"><span data-stu-id="49aa8-119">Event</span></span>
    - <span data-ttu-id="49aa8-120">Zeitpunkt der Erstellung</span><span class="sxs-lookup"><span data-stu-id="49aa8-120">When created</span></span>
    - <span data-ttu-id="49aa8-121">Zeitpunkt der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="49aa8-121">When last modified</span></span>
    - <span data-ttu-id="49aa8-122">Zeitpunkt der Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="49aa8-122">When labeled</span></span>
- <span data-ttu-id="49aa8-p102">**Datensatz** gibt an, ob das Element ein deklarierter Datensatz werden kann, wenn die Bezeichnung angewendet wurde. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49aa8-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="49aa8-125">Nein</span><span class="sxs-lookup"><span data-stu-id="49aa8-125">No</span></span>
    - <span data-ttu-id="49aa8-126">Ja</span><span class="sxs-lookup"><span data-stu-id="49aa8-126">Yes</span></span>
    - <span data-ttu-id="49aa8-127">Yes (Vorgeschrieben)</span><span class="sxs-lookup"><span data-stu-id="49aa8-127">Yes(Regulatory)</span></span>
- <span data-ttu-id="49aa8-p103">**Aufbewahrung** gibt den Aufbewahrungstyp an. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49aa8-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="49aa8-130">Beibehalten</span><span class="sxs-lookup"><span data-stu-id="49aa8-130">Keep</span></span>
    - <span data-ttu-id="49aa8-131">Beibehalten und löschen</span><span class="sxs-lookup"><span data-stu-id="49aa8-131">Keep and delete</span></span>
    - <span data-ttu-id="49aa8-132">Löschen</span><span class="sxs-lookup"><span data-stu-id="49aa8-132">Delete</span></span>
- <span data-ttu-id="49aa8-p104">**Disposition** gibt an, was mit dem Inhalt am Ende des Aufbewahrungszeitraums geschieht. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="49aa8-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="49aa8-135">Null</span><span class="sxs-lookup"><span data-stu-id="49aa8-135">null</span></span>
    - <span data-ttu-id="49aa8-136">Keine Aktion</span><span class="sxs-lookup"><span data-stu-id="49aa8-136">No action</span></span>
    - <span data-ttu-id="49aa8-137">Automatisch löschen</span><span class="sxs-lookup"><span data-stu-id="49aa8-137">Auto-delete</span></span>
    - <span data-ttu-id="49aa8-138">Überprüfung erforderlich (auch bezeichnet als Dispositionsprüfung)</span><span class="sxs-lookup"><span data-stu-id="49aa8-138">Review required (aka Disposition review)</span></span>

![Bezeichnungseinstellungen im Dateiplan](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="49aa8-140">Spalten mit Dateiplanbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="49aa8-140">Label file plan descriptors columns</span></span>

<span data-ttu-id="49aa8-p105">Sie können nun mehr Informationen in die Konfiguration Ihrer Aufbewahrungsbezeichnungen einschließen. Durch Einfügen von Dateiplanbeschreibungen in Bezeichnungen können Sie die Verwaltbarkeit und Organisation Ihres Dateiplans verbessern.</span><span class="sxs-lookup"><span data-stu-id="49aa8-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="49aa8-p106">Für den Einstieg stellt Dateiplan-Manager einige einsatzbereite Werte für Folgendes bereit: Funktion/Abteilung, Kategorie, Autoritätstyp und Bereitstellung. Sie können neue Werte für die Dateiplanbeschreibung hinzufügen, wenn Sie eine Aufbewahrungsbezeichnung erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="49aa8-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="49aa8-145">Nachfolgend finden Sie eine Übersicht der Dateiplanbeschreibungen beim Erstellen oder Bearbeiten einer Aufbewahrungsbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="49aa8-145">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Dateiplanbeschreibungen](media/file-plan-descriptors.png)

<span data-ttu-id="49aa8-147">Nachfolgend finden Sie eine Übersicht über die Spalten mit Dateiplanbeschreibungen auf der Registerkarte „Bezeichnungen“ des Dateiplan-Managers.</span><span class="sxs-lookup"><span data-stu-id="49aa8-147">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="49aa8-149">Exportieren von Bezeichnungen Ihres Dateiplans</span><span class="sxs-lookup"><span data-stu-id="49aa8-149">Export labels out of your file plan</span></span>

<span data-ttu-id="49aa8-150">Aus dem Dateiplan-Manager können Sie die Details aller Aufbewahrungsbezeichnungen in eine CSV-Datei exportieren, mit deren Hilfe Sie regelmäßige Complianceüberprüfungen mit den Beteiligten an der Datengovernance in Ihrer Organisation durchführen können.</span><span class="sxs-lookup"><span data-stu-id="49aa8-150">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="49aa8-151">Um alle Aufbewahrungsbezeichnungen zu exportieren, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen exportieren**.</span><span class="sxs-lookup"><span data-stu-id="49aa8-151">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Option zum Exportieren des Dateiplans](media/file-plan-export-labels-option.png)

<span data-ttu-id="49aa8-153">Es wird eine CSV-Datei mit allen vorhandenen Aufbewahrungsbeschriftungen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="49aa8-153">A \*.csv file containing all existing retention labels will open.</span></span>

![CSV-Datei, in der alle Aufbewahrungsbeschriftungen angezeigt werden](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="49aa8-155">Importieren von Bezeichnungen in Ihren Dateiplan</span><span class="sxs-lookup"><span data-stu-id="49aa8-155">Import labels into your file plan</span></span>

<span data-ttu-id="49aa8-156">Aus dem Dateiplan-Manager können Sie neue Bezeichnungen massenimportieren und vorhandenen Aufbewahrungsbezeichnungen ändern.</span><span class="sxs-lookup"><span data-stu-id="49aa8-156">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="49aa8-157">Zum Importieren von neuen Aufbewahrungsbeschriftungen und zum Aktualisieren von vorhandenen Aufbewahrungsbezeichnungen vornehmen, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen importieren**.</span><span class="sxs-lookup"><span data-stu-id="49aa8-157">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Option zum Importieren des Dateiplans](media/file-plan-import-labels-option.png)

![Option zum Herunterladen einer leeren Vorlage für den Dateiplan](media/file-plan-blank-template-option.png)

<span data-ttu-id="49aa8-160">Laden Sie eine leere Vorlage herunter (oder beginnen Sie mit einem Export Ihres aktuellen Dateiplans).</span><span class="sxs-lookup"><span data-stu-id="49aa8-160">Download a blank template (or start from an export of your current file plan).</span></span>

![Leere Vorlage eines Dateiplans, geöffnet in Excel](media/file-plan-blank-template.png)

<span data-ttu-id="49aa8-162">Füllen Sie die Vorlage aus (Referenzinformationen zu gültigen Werte für Einträge sind in Kürze verfügbar).</span><span class="sxs-lookup"><span data-stu-id="49aa8-162">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Dateiplanvorlage mit ausgefüllten Informationen](media/file-plan-filled-out-template.png)

<span data-ttu-id="49aa8-164">Laden Sie die ausgefüllte Vorlage hoch; die Einträge werden dann vom Dateiplan-Manager überprüft, und es werden Importstatistiken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49aa8-164">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Dateiplan-Importstatistiken](media/file-plan-import-statistics.png)

<span data-ttu-id="49aa8-166">Wenn der Importvorgang abgeschlossen ist, kehren Sie zum Dateiplan-Manager zurück, um neuen oder vorhandenen Richtlinien neue Bezeichnungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="49aa8-166">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Option zum Veröffentlichen von Bezeichnungen](media/file-plan-publish-labels-option.png)


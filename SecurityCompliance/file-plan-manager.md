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
# <a name="overview-of-file-plan-manager"></a>Übersicht über den Dateiplan-Manager

Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen, Aufbewahrungsbezeichnungsrichtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.

![Dateiplanseite](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a>Zugriff auf den Dateiplan-Manager

Es gibt die folgenden beiden Anforderungen für den Zugriff auf den Dateiplan-Manager:
- Ein Office 365 Enterprise E5-Abonnement.
- Der Benutzer wurde einer der folgenden Rollen des Security &amp; Compliance Centers zugewiesen:
    - Aufbewahrungs-Manager
    - Aufbewahrungs-Manager (schreibgeschützt)

## <a name="default-retention-labels-and-label-policy"></a>Standardmäßige Aufbewahrungsbezeichnung und Bezeichnungsrichtlinie

Wenn keine Aufbewahrungsbezeichnungen im Security & Compliance Center vorhanden sind, wird, wenn Sie im linken Navigationsbereich **Dateiplan** auswählen, eine Bezeichnungsrichtlinie mit dem Namen **Standardmäßige Veröffentlichungsrichtlinie für Datengovernance** erstellt. 

Diese Bezeichnungsrichtlinie enthält drei Aufbewahrungsbezeichnungen:

- **Operative Prozesse**
- **Allgemeines Geschäft**
- **Vertragliche Vereinbarung**

Diese Aufbewahrungsbezeichnungen sind so konfiguriert, dass Inhalte nur aufbewahrt, aber nicht gelöscht werden. Diese Bezeichnungsrichtlinie wird in der gesamten Organisation veröffentlicht und kann deaktiviert oder entfernt werden. 

Sie können feststellen, wer den Dateiplan-Manager geöffnet und den Eindruck beim ersten Ausführen gestartet hat, indem Sie das Überwachungsprotokoll für die Aktivitäten **Erstellte Aufbewahrungsrichtlinie** und **Erstellte Konfiguration für eine Aufbewahrungsrichtlinie** überprüfen.

> [!NOTE]
> Aufgrund von Kundenfeedback haben wir dieses Feature entfernt, durch das die standardmäßigen Aufbewahrungsbezeichnungen und die oben genannte Aufbewahrungsbezeichnungsrichtlinie erstellt wurden. Diese Aufbewahrungsbezeichnungen und Aufbewahrungsbezeichnungsrichtlinien werden Ihnen nur dann angezeigt, wenn Sie den Datei-Plan-Manager vor dem 11. April 2019 geöffnet haben.

## <a name="navigating-your-file-plan"></a>Navigieren in Ihrem Dateiplan

Mit dem Dateiplan-Manager können Sie leichter die Einstellungen aller Aufbewahrungsbezeichnungen und Richtlinien aus einer Ansicht anzeigen.

Beachten Sie, dass Aufbewahrungsbezeichnungen, die außerhalb des Dateiplans erstellt wurden, im Dateiplan verfügbar sind und umgekehrt.

Auf den Registerkarten für die **Dateiplanbezeichnungen** sind die folgenden zusätzlichen Informationen und Funktionen verfügbar:

### <a name="label-settings-columns"></a>Spalten mit Bezeichnungseinstellungen

- **Basierend auf** gibt den Typ des Auslösers an, der den Aufbewahrungszeitraum starten kann. Gültige Werte sind:
    - Ereignis
    - Zeitpunkt der Erstellung
    - Zeitpunkt der letzten Änderung
    - Zeitpunkt der Bezeichnung
- **Datensatz** gibt an, ob das Element ein deklarierter Datensatz werden kann, wenn die Bezeichnung angewendet wurde. Gültige Werte sind:
    - Nein
    - Ja
    - Yes (Vorgeschrieben)
- **Aufbewahrung** gibt den Aufbewahrungstyp an. Gültige Werte sind:
    - Beibehalten
    - Beibehalten und löschen
    - Löschen
- **Disposition** gibt an, was mit dem Inhalt am Ende des Aufbewahrungszeitraums geschieht. Gültige Werte sind:
    - Null
    - Keine Aktion
    - Automatisch löschen
    - Überprüfung erforderlich (auch bezeichnet als Dispositionsprüfung)

![Bezeichnungseinstellungen im Dateiplan](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a>Spalten mit Dateiplanbeschreibungen für Aufbewahrungsbezeichnungen

Sie können nun mehr Informationen in die Konfiguration Ihrer Aufbewahrungsbezeichnungen einschließen. Durch Einfügen von Dateiplanbeschreibungen in Aufbewahrungsbezeichnungen können Sie die Verwaltbarkeit und Organisation Ihres Dateiplans verbessern.

Für den Einstieg stellt Dateiplan-Manager einige einsatzbereite Werte für Folgendes bereit: Funktion/Abteilung, Kategorie, Autoritätstyp und Bereitstellung. Sie können neue Werte für die Dateiplanbeschreibung hinzufügen, wenn Sie eine Aufbewahrungsbezeichnung erstellen oder bearbeiten.

Nachfolgend finden Sie eine Übersicht der Dateiplanbeschreibungen beim Erstellen oder Bearbeiten einer Aufbewahrungsbezeichnung.

![Dateiplanbeschreibungen](media/file-plan-descriptors.png)

Nachfolgend finden Sie eine Übersicht über die Spalten mit Dateiplanbeschreibungen auf der Registerkarte „Bezeichnungen“ des Dateiplan-Managers.

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a>Exportieren aller vorhandenen Aufbewahrungsbezeichnungen zum Analysieren und/oder Durchführen von Offline Überprüfungen

Aus dem Dateiplan-Manager können Sie die Details aller Aufbewahrungsbezeichnungen in eine CSV-Datei exportieren, mit deren Hilfe Sie regelmäßige Complianceüberprüfungen mit den Beteiligten an der Datengovernance in Ihrer Organisation durchführen können.

Um alle Aufbewahrungsbezeichnungen zu exportieren, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen exportieren**.

![Option zum Exportieren des Dateiplans](media/file-plan-export-labels-option.png)

Es wird eine CSV-Datei mit allen vorhandenen Aufbewahrungsbeschriftungen geöffnet.

![CSV-Datei, in der alle Aufbewahrungsbeschriftungen angezeigt werden](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a>Importieren von Aufbewahrungsbezeichnungen in Ihren Dateiplan

Aus dem Dateiplan-Manager können Sie neue Aufbewahrungsbezeichnungen massenimportieren und vorhandene Aufbewahrungsbezeichnungen ändern.

Zum Importieren von neuen Aufbewahrungsbeschriftungen und zum Aktualisieren von vorhandenen Aufbewahrungsbezeichnungen gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen importieren**.

![Option zum Importieren des Dateiplans](media/file-plan-import-labels-option.png)

![Option zum Herunterladen einer leeren Vorlage für den Dateiplan](media/file-plan-blank-template-option.png)

Laden Sie eine leere Vorlage herunter (oder beginnen Sie mit einem Export Ihres aktuellen Dateiplans).

![Leere Vorlage eines Dateiplans, geöffnet in Excel](media/file-plan-blank-template.png)

Füllen Sie die Vorlage aus (in Kürze verfügbar: Referenzinformationen zu gültigen Wertkombinationen für ein einzelne Aufbewahrungsbezeichnung).

![Dateiplanvorlage mit ausgefüllten Informationen](media/file-plan-filled-out-template.png)

Laden Sie die ausgefüllte Vorlage hoch; die Einträge werden dann vom Dateiplan-Manager überprüft, und es werden Importstatistiken angezeigt.

![Dateiplan-Importstatistiken](media/file-plan-import-statistics.png)

Für den Fall, dass ein Überprüfungsfehler vorliegt, überprüft der Dateiplanimport weiterhin jeden Eintrag in der Importdatei und zeigt alle Fehler an, wobei er die Zeilen-/Reihennummern in der Importdatei referenziert und die angezeigten Fehlerergebnisse kopiert, damit Sie einfach zur Importdatei zurückkehren und die Fehler korrigieren können. 

Wenn der Importvorgang abgeschlossen ist, kehren Sie zum Dateiplan-Manager zurück, um neuen oder vorhandenen Aufbewahrungsbezeichnungsrichtlinien neue Aufbewahrungsbezeichnungen zuzuweisen.

![Option zum Veröffentlichen von Bezeichnungen](media/file-plan-publish-labels-option.png)


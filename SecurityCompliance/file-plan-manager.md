---
title: Übersicht über den Dateiplan-Manager
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen und Richtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.
ms.openlocfilehash: 4feacf20444591f6da2d55a928a81e86b56c5d9a
ms.sourcegitcommit: 9f34ace6bbe3d5e07e24ebaae96613750869cddf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2018
ms.locfileid: "25019276"
---
# <a name="overview-of-file-plan-manager"></a>Übersicht über den Dateiplan-Manager

Der Dateiplan-Manager bietet erweiterte Verwaltungsfunktionen für Aufbewahrungsbezeichnungen und Richtlinien und bietet eine integrierte Möglichkeit, Bezeichnungen und Bezeichnung-zu-Inhalt-Aktivitäten in Ihrem gesamten Inhaltslebenszyklus zu durchlaufen – von der Erstellung über die Zusammenarbeit, die Datensatzdeklaration, die Aufbewahrung hin zur Disposition.

![Dateiplanseite](media/file-plan-page.png)

## <a name="important-this-feature-is-currently-available-only-as-part-of-the-office-365-preview-program"></a>Wichtig: Dieses Feature ist derzeit nur als Teil des Office 365 Preview-Programms verfügbar.

Dieses Feature wird in Ihrem Mandanten nur angezeigt, wenn Ihre Organisation sich beim Office 365 Preview-Programm registriert hat.

## <a name="accessing-file-plan-manager"></a>Zugriff auf den Dateiplan-Manager

Es gibt die folgenden beiden Anforderungen für den Zugriff auf den Dateiplan-Manager:
- Ein Office 365 Enterprise E5-Abonnement.
- Der Benutzer wurde einer der folgenden Rollen des Security &amp; Compliance Centers zugewiesen: 
    - Aufbewahrungs-Manager
    - Aufbewahrungs-Manager (schreibgeschützt)

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

### <a name="label-file-plan-descriptors-columns"></a>Spalten mit Dateiplanbeschreibungen

Sie können nun mehr Informationen in die Konfiguration Ihrer Aufbewahrungsbezeichnungen einschließen. Durch Einfügen von Dateiplanbeschreibungen in Bezeichnungen können Sie die Verwaltbarkeit und Organisation Ihres Dateiplans verbessern.

Für den Einstieg stellt Dateiplan-Manager einige einsatzbereite Werte für Folgendes bereit: Funktion/Abteilung, Kategorie, Autoritätstyp und Bereitstellung. Sie können neue Werte für die Dateiplanbeschreibung hinzufügen, wenn Sie eine Aufbewahrungsbezeichnung erstellen oder bearbeiten.

Nachfolgend finden Sie eine Übersicht der Dateiplanbeschreibungen beim Erstellen oder Bearbeiten einer Aufbewahrungsbezeichnung.

![Dateiplanbeschreibungen](media/file-plan-descriptors.png)

Nachfolgend finden Sie eine Übersicht über die Spalten mit Dateiplanbeschreibungen auf der Registerkarte „Bezeichnungen“ des Dateiplan-Managers.

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a>Exportieren von Bezeichnungen Ihres Dateiplans

Aus dem Dateiplan-Manager können Sie die Details aller Aufbewahrungsbezeichnungen in eine CSV-Datei exportieren, mit deren Hilfe Sie regelmäßige Complianceüberprüfungen mit den Beteiligten an der Datengovernance in Ihrer Organisation durchführen können.

Um alle Aufbewahrungsbezeichnungen zu exportieren, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen exportieren**.

![Option zum Exportieren des Dateiplans](media/file-plan-export-labels-option.png)

Es wird eine CSV-Datei mit allen vorhandenen Aufbewahrungsbeschriftungen geöffnet.

![CSV-Datei, in der alle Aufbewahrungsbeschriftungen angezeigt werden](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a>Importieren von Bezeichnungen in Ihren Dateiplan

Aus dem Dateiplan-Manager können Sie neue Bezeichnungen massenimportieren und vorhandenen Aufbewahrungsbezeichnungen ändern.

Zum Importieren von neuen Aufbewahrungsbeschriftungen und zum Aktualisieren von vorhandenen Aufbewahrungsbezeichnungen vornehmen, gehen Sie zu **Dateiplan-Manager** \> **Dateiplanaktionen** \> **Bezeichnungen importieren**.

![Option zum Importieren des Dateiplans](media/file-plan-import-labels-option.png)

![Option zum Herunterladen einer leeren Vorlage für den Dateiplan](media/file-plan-blank-template-option.png)

Laden Sie eine leere Vorlage herunter (oder beginnen Sie mit einem Export Ihres aktuellen Dateiplans).

![Leere Vorlage eines Dateiplans, geöffnet in Excel](media/file-plan-blank-template.png)

Füllen Sie die Vorlage aus (Referenzinformationen zu gültigen Werte für Einträge sind in Kürze verfügbar).

![Dateiplanvorlage mit ausgefüllten Informationen](media/file-plan-filled-out-template.png)

Laden Sie die ausgefüllte Vorlage hoch; die Einträge werden dann vom Dateiplan-Manager überprüft, und es werden Importstatistiken angezeigt.

![Dateiplan-Importstatistiken](media/file-plan-import-statistics.png)

Wenn der Importvorgang abgeschlossen ist, kehren Sie zum Dateiplan-Manager zurück, um neuen oder vorhandenen Richtlinien neue Bezeichnungen zuzuweisen.

![Option zum Veröffentlichen von Bezeichnungen](media/file-plan-publish-labels-option.png)


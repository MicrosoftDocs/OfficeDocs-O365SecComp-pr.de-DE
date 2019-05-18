---
title: Verwalten von Aufträgen in Daten Untersuchungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 12b86f3e63d69fbd64304f1ed46cff25daffa8ff
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150767"
---
# <a name="manage-jobs-in-data-investigations-preview"></a>Verwalten von Aufträgen in Daten Untersuchungen (Vorschau)

Im folgenden finden Sie eine Liste der Aufträge (in der Regel langwierige Prozesse), die auf der Registerkarte **Aufträge** einer Untersuchung in Data Investigations (Preview) nachverfolgt werden. Diese Aufträge werden durch Benutzeraktionen bei der Verwendung und Verwaltung von Untersuchungen ausgelöst.

| Auftragstyp           | Beschreibung     |
| :----------------- | :----------     |
|Hinzufügen von Daten zu einem Beweissatzes | Ein Benutzer fügt die Ergebnisse einer Suche zu einem Beweissatz hinzu.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). |
|Hinzufügen von Daten zu einem anderen Beweissatzes | Ein Benutzer fügt Dokumente aus einem Beweissatz in demselben Fall in einen anderen Beweissatz ein.|
|Hinzufügen von nicht Office 365-Daten zu einem Beweissatzes | Ein Benutzer lädt nicht Office 365 Daten in einen Beweissatz hoch. Die Daten werden auch während dieses Prozesses indiziert. Beispielsweise werden Dateien von einem lokalen Dateiserver oder einem Clientcomputer in einen Beweissatz hochgeladen. Weitere Informationen finden Sie unter [Laden von nicht Office 365 Daten in Beweise](load-non-office365-data.md).| 
|Hinzufügen von korrigierten Daten zu einem Evidence-Datensatz | Daten mit Verarbeitungsfehlern werden wiederhergestellt und in einen Beweissatz zurückgeladen. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten für eine Untersuchung](error-remediation.md). | 
|Vergleichen von Lastsätzen | Ein Benutzer prüft die Unterschiede zwischen verschiedenen Lastsätzen in einem Beweissatz. Bei einem Lastsatz handelt es sich um eine Instanz des Hinzufügens von Daten zu einem Beweissatz. Wenn Sie beispielsweise die Ergebnisse zweier unterschiedlicher Suchvorgänge dem gleichen Beweissatz hinzufügen, würde jeder einen Lastsatz darstellen. Weitere Informationen finden Sie unter [Manage Last Sets](manage-load-sets.md). |
|Konvertieren von behandelten Dokumenten in PDF|Nachdem ein Benutzer ein Dokument in einem Beweissatz kommentiert und einen Teil davon verarbeitet hat, kann er das in eine PDF-Datei konvertierte Dokument auswählen. Dadurch wird sichergestellt, dass der behandelte Teil nicht sichtbar ist, wenn das Dokument zur Präsentation exportiert wird. Weitere Informationen finden Sie unter [Überprüfen von Daten in Evidence](review-data-in-evidence.md). |
|Schätzen von Suchergebnissen | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), durchsucht das Such Tool den Index nach Elementen, die mit der Suchabfrage übereinstimmen, und bereitet eine Schätzung vor, die die Anzahl und die Gesamtgröße aller Elemente durch die Suche sowie die Anzahl der Datenquellen enthält. Sea rched.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). | 
|Vorbereiten von Daten für den Export | Ein Benutzer exportiert Dokumente aus einem Evidence-Datensatz. Wenn der Exportvorgang abgeschlossen ist, können Sie die exportierten Daten auf einen lokalen Computer herunterladen. Weitere Informationen finden Sie unter [Exportieren von Daten aus einer Untersuchung](export-data.md). | 
|Vorbereiten der Fehlerbehebung |Wenn ein Benutzer eine Datei auswählt und eine neue Fehlerkorrektur in der Fehleransicht auf der Registerkarte **Verarbeitung** einer Untersuchung erstellt, besteht der erste Schritt im Prozess darin, die Datei mit dem Verarbeitungsfehler an einen Azure-Speicherort in der Microsoft-Cloud hochzuladen. Dieser Auftrag verfolgt den Fortschritt des Upload-Prozesses. Weitere Informationen zum Fehlerkorrektur-Workflow finden Sie unter [Fehlerbehebung bei der Verarbeitung von Daten für eine Untersuchung](error-remediation.md).| 
|Vorbereiten der Suchvorschau | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), bereitet das Such Tool eine Beispiel Teilmenge von Elementen vor, die mit der Suchabfrage übereinstimmen, die in der Vorschau angezeigt werden kann. Die Vorschau der Suchergebnisse kann Ihnen helfen, die Effektivität der Suche zu ermitteln.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). | 
|Erneutes Indizieren von Daten von interessanten Personen | Wenn Sie eine Person von Interesse zu einer Untersuchung hinzufügen, werden alle teilweise indizierten Elemente in der Person von Interesse ausgewählte Datenquellen durch einen Prozess namens *Erweiterte Indizierung*neu indiziert. Dieser Auftrag wird auch ausgelöst, wenn Sie auf der Registerkarte **Verarbeitung** einer Untersuchung auf **Indexansicht aktualisieren** klicken. Weitere Informationen finden Sie unter [Erweiterte Indizierung von Daten für eine Untersuchung](index-data-people-of-interest.md).
|Durchführen von Analysen | Ein Benutzer analysiert Daten in einem Beweissatz, indem er Analysetools wie etwa doppelte Erkennung, e-Mail-Threading Analyse und Design Analyse ausführt. Weitere Informationen finden Sie unter [Ausführen von Analysen, um schneller zu untersuchen](run-analytics-to-investigate-faster.md). | 
|Markieren von Dokumenten | Dieser Auftrag wird ausgelöst, wenn ein Benutzer beim Überprüfen von Dokumenten in einem Beweismittel im taggingbereich auf " **Tagging-Auftrag starten** **"** klickt. Ein Benutzer kann diesen Auftrag starten, nachdem er Dokumente in einem Beweissatz markiert und diese dann im Dokument Panel anzeigen massenhaft ausgewählt hat. Weitere Informationen finden Sie unter [Tag Documents in Evidence](tag-documents.md). | 
|||

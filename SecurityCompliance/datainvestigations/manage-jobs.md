---
title: Verwalten von Aufträgen in Daten Untersuchungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3b144fbf5f00f3dbb017ac176c75677970f2f7f2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258183"
---
# <a name="manage-jobs-in-data-investigations-preview"></a>Verwalten von Aufträgen in Daten Untersuchungen (Vorschau)

Nachfolgend finden Sie eine Liste der Aufträge (in der Regel lang andauernde Prozesse), die auf der Registerkarte **Aufträge** einer Untersuchung in Daten Untersuchungen (Preview) nachverfolgt werden. Diese Aufträge werden durch Benutzeraktionen bei der Verwendung und Verwaltung von Untersuchungen ausgelöst.

| Auftragstyp           | Beschreibung     |
| :----------------- | :----------     |
|Hinzufügen von Daten zu einem Beweissatz | Ein Benutzer fügt die Ergebnisse einer Suche einem Evidence-Satz hinzu.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). |
|Hinzufügen von Daten zu einem anderen nachweissatz | Ein Benutzer fügt Dokumente aus einem Evidence-Satz zu einem anderen Evidence-Satz in demselben Fall hinzu.|
|Hinzufügen von nicht-Office 365-Daten zu einem Evidence-Satz | Ein Benutzer lädt nicht-Office 365-Daten in einen Evidence-Satz hoch. Die Daten werden auch während dieses Prozesses indiziert. Beispielsweise werden Dateien von einem lokalen Dateiserver oder einem Clientcomputer in einen Evidence-Satz hochgeladen. Weitere Informationen finden Sie unter [Laden von nicht-Office 365-Daten in Beweise](load-non-office365-data.md).| 
|Hinzufügen von remediationd Data zu einem Evidence Set | Daten mit Verarbeitungsfehlern werden wiederhergestellt und in einen Evidence-Satz zurückgeladen. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten für eine Untersuchung](error-remediation.md). | 
|Vergleichen von Auslastungs Sätzen | Ein Benutzer betrachtet die Unterschiede zwischen verschiedenen Auslastungs Sätzen in einem Evidence-Satz. Ein Auslastungs Satz ist eine Instanz des Hinzufügens von Daten zu einem Evidence-Satz. Wenn Sie beispielsweise die Ergebnisse von zwei unterschiedlichen Suchvorgängen zum gleichen Beweissatz hinzufügen, würde jeder einen Lasten Satz darstellen. Weitere Informationen finden Sie unter [Manage Auslastung Sets](manage-load-sets.md). |
|Konvertieren von gehandelten Dokumenten in PDF|Nachdem ein Benutzer ein Dokument mit Anmerkungen versehen und einen Teil davon bearbeitet hat, können Sie das Dokument in eine PDF-Datei konvertieren. Dadurch wird sichergestellt, dass der behandelte Teil nicht sichtbar ist, wenn das Dokument für die Präsentation exportiert wird. Weitere Informationen finden Sie unter [Überprüfen von Daten in Evidence](review-data-in-evidence.md). |
|Schätzen von Suchergebnissen | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), durchsucht das Such Tool den Index nach Elementen, die mit der Suchabfrage übereinstimmen, und bereitet eine Schätzung vor, die die Anzahl und Gesamtgröße aller Elemente durch die Suche und die Anzahl der Datenquellen Sea rched.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). | 
|Vorbereiten von Daten für den Export | Ein Benutzer exportiert Dokumente aus einem Evidence-Satz. Nach Abschluss des Exportvorgangs können die exportierten Daten auf einen lokalen Computer heruntergeladen werden. Weitere Informationen finden Sie unter [Exportieren von Daten aus einer Untersuchung](export-data.md). | 
|Vorbereiten auf die Fehlerbehebung |Wenn ein Benutzer eine Datei auswählt und eine neue Fehlerkorrektur in der Fehleransicht auf der Registerkarte **Verarbeitung** einer Untersuchung erstellt, besteht der erste Schritt in diesem Prozess darin, die Datei mit dem Verarbeitungsfehler an einen Azure-Speicherort in der Microsoft-Cloud hochzuladen. Dieser Auftrag verfolgt den Fortschritt des Uploads. Weitere Informationen zum Fehlerkorrektur-Workflow finden Sie unter [Fehlerbehebung bei der Verarbeitung von Daten für eine Untersuchung](error-remediation.md).| 
|Vorbereiten der Suchvorschau | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), bereitet das Such Tool eine Beispiel Teilmenge der Elemente (die mit der Suchabfrage übereinstimmen) vor, die in der Vorschau angezeigt werden können. Die Vorschau der Suchergebnisse hilft Ihnen bei der Bestimmung der Effektivität der Suche.  Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md). | 
|Erneutes Indizieren von personenbezogenen Daten | Wenn Sie eine Person von Interesse zu einer Untersuchung hinzufügen, werden alle teilweise indizierten Elemente in den ausgewählten Datenquellen der Person von Interest durch einen Prozess mit dem Namen *Advanced Indexing*neu indiziert. Dieser Auftrag wird auch ausgelöst, wenn Sie auf der Registerkarte **Verarbeitung** einer Untersuchung auf **Index aktualisieren** in der Indexansicht klicken. Weitere Informationen finden Sie unter [Erweiterte Indizierung von Daten für eine Untersuchung](index-data-people-of-interest.md).
|Running Analytics | Ein Benutzer analysiert Daten in einem Beweissatz, indem er Analysetools wie near Duplicate Detection, e-Mail-Threading-Analyse und Design Analyse ausführt. Weitere Informationen finden Sie unter [Run Analytics to untersuchen schneller](run-analytics-to-investigate-faster.md). | 
|Markieren von Dokumenten | Dieser Auftrag wird ausgelöst, wenn ein Benutzer beim Überprüfen von Dokumenten in **** einem Beweissatz auf **Tagging-Auftrag starten** klickt. Ein Benutzer kann diesen Auftrag nach dem Markieren von Dokumenten in einem Evidence-Satz starten und diese dann im Dokumentbereich für die Massenauswahl auswählen. Weitere Informationen finden Sie unter [Tag Documents in Evidence](tag-documents.md). | 
|||

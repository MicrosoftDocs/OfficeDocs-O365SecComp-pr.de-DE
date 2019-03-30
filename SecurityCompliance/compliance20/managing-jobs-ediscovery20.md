---
title: Verwalten von Aufträgen in Advanced eDiscovery (Preview)
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
ms.openlocfilehash: a5b9975803e0243f873bdd5f538dbc5e62907327
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997051"
---
# <a name="manage-jobs-in-advanced-ediscovery-preview"></a>Verwalten von Aufträgen in Advanced eDiscovery (Preview)

Hier finden Sie eine Liste der Aufträge (bei denen es sich in der Regel um lang andauernde Prozesse handelt), die auf der Registerkarte **Aufträge** eines Falls in Advanced EDiscovery (Preview) nachverfolgt werden. Diese Aufträge werden durch Benutzeraktionen ausgelöst, wenn Fälle verwendet und verwaltet werden.

| Auftragstyp           | Beschreibung     |
| :----------------- | :----------     |
|Hinzufügen von Daten zu einem Workingset | Ein Benutzer fügt die Ergebnisse einer Suche zu einem Workingset hinzu.  Weitere Informationen finden Sie unter [Hinzufügen von Suchergebnissen zu einem Arbeitssatz](add-data-to-working-set.md). |
|Hinzufügen von Daten zu einem anderen Arbeitssatz | Ein Benutzer fügt Dokumente aus einem Arbeitssatz in demselben Fall zu einem anderen Arbeitssatz hinzu.|
|Hinzufügen von nicht-Office 365-Daten zu einem Workingset | Ein Benutzer lädt nicht-Office 365-Daten in einen Arbeitssatz hoch. Die Daten werden auch während dieses Prozesses indiziert. Beispielsweise werden Dateien von einem lokalen Dateiserver oder einem Clientcomputer in einen Arbeitssatz hochgeladen. Weitere Informationen finden Sie unter [Laden von nicht-Office 365-Daten in eine Arbeitsmappe](load-non-office365-data.md).| 
|Hinzufügen von vermittelten Daten zu einem Workingset | Daten mit Verarbeitungsfehlern werden wiederhergestellt und in eine Arbeitsmappe zurückgeladen. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md). | 
|Vergleichen von Auslastungs Sätzen | Ein Benutzer betrachtet die Unterschiede zwischen verschiedenen Auslastungs Sätzen in einer Arbeitsmappe. Ein Auslastungs Satz ist eine Instanz des Hinzufügens von Daten zu einem Workingset. Wenn Sie beispielsweise die Ergebnisse von zwei unterschiedlichen Suchvorgängen zum gleichen Arbeitssatz hinzufügen, würde jeder eine Auslastungs Gruppe darstellen. Weitere Informationen finden Sie unter [Manage Auslastung Sets](manage-load-sets.md). |
|Konvertieren von gehandelten Dokumenten in PDF|Nachdem ein Benutzer ein Dokument in einem Arbeitssatz mit Anmerkungen versehen und einen Teil davon bearbeitet hat, können Sie das Dokument in eine PDF-Datei konvertieren. Dadurch wird sichergestellt, dass der behandelte Teil nicht sichtbar ist, wenn das Dokument zur Präsentation exportiert wird. Weitere Informationen finden Sie unter [Anzeigen von Dokumenten in einem Arbeitssatz](annotating-and-redacting-documents.md). |
|Schätzen von Suchergebnissen | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), sucht das Such Tool den Index nach Elementen, die mit der Suchabfrage übereinstimmen, und bereitet eine Schätzung vor, die die Anzahl und Gesamtgröße aller Elemente bei der Suche und die Anzahl der Datenquellen anbraten Ched.  Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall](collecting-data-for-ediscovery.md). | 
|Vorbereiten von Daten für den Export | Ein Benutzer exportiert Dokumente feom a aus einem Arbeitssatz. Nach Abschluss des Exportvorgangs können die exportierten Daten auf einen lokalen Computer heruntergeladen werden. Weitere Informationen finden Sie unter [exportieren](exporting-data-ediscover20.md)von Falldaten. | 
|Vorbereiten auf die Fehlerbehebung |Wenn ein Benutzer eine Datei auswählt und eine neue Fehlerkorrektur in der Fehleransicht auf der Registerkarte **Verarbeitung** eines Falls erstellt, besteht der erste Schritt in diesem Prozess darin, die Datei mit dem Verarbeitungsfehler an einen Azure-Speicherort in der Microsoft-Cloud hochzuladen. Dieser Auftrag verfolgt den Fortschritt des Uploads. Weitere Informationen zum Fehlerkorrektur-Workflow finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md). | 
|Vorbereiten der Suchvorschau | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), bereitet das Such Tool eine Beispiel Teilmenge der Elemente (die mit der Suchabfrage übereinstimmen) vor, die in der Vorschau angezeigt werden können. Die Vorschau der Suchergebnisse hilft Ihnen bei der Bestimmung der Effektivität der Suche.  Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall](collecting-data-for-ediscovery.md#view-search-results-and-statistics). | 
|Erneutes Indizieren von Depotdaten | Wenn Sie einen Verwalter zu einem Fall hinzufügen, werden alle teilweise indizierten Elemente in den ausgewählten Datenquellen der Depotbank durch einen Prozess namens *Advanced Indexing*neu indiziert. Dieser Auftrag wird auch ausgelöst, wenn Sie auf der Registerkarte **Verarbeitung** eines Falls auf Index **Aktualisieren** in der Indexansicht klicken. Weitere Informationen finden Sie unter [Erweiterte Indizierung von Depotbank-Daten](indexing-custodian-data.md).
|Running Analytics | Ein Benutzer analysiert Daten in einem Arbeitssatz, indem er erweiterte eDiscovery Analytics-Tools wie near Duplicate Detection, e-Mail-Threading-Analyse und Design Analyse ausführt. Weitere Informationen finden Sie unter [Analysieren von Daten in einem Arbeitssatz](analyzing-data-in-working-set.md). | 
|Markieren von Dokumenten | Dieser Auftrag wird ausgelöst, wenn ein Benutzer beim Überprüfen von Dokumenten in **** einem Arbeitssatz auf **Tagging-Auftrag starten** klickt. Ein Benutzer kann diesen Auftrag nach dem Markieren von Dokumenten in einem Arbeitssatz und anschließendem Massen auswählen im Dokumentbereich starten. Weitere Informationen finden Sie unter [Tag Documents in a Working Set](tagging-documents.md). | 
|||

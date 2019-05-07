---
title: Verwalten von Aufträgen in Advanced eDiscovery
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
ms.openlocfilehash: 4d306f6f1a37fad0aa5e3f92cafdb29b1ea37d1c
ms.sourcegitcommit: 25595bc8fae96bc23b7b6d7102a22f37878987c0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "33641611"
---
# <a name="manage-jobs-in-advanced-ediscovery"></a>Verwalten von Aufträgen in Advanced eDiscovery

Hier finden Sie eine Liste der Aufträge (in der Regel lang andauernde Prozesse), die auf der Registerkarte **Aufträge** eines Falls in Advanced eDiscovery nachverfolgt werden. Diese Aufträge werden durch Benutzeraktionen ausgelöst, wenn Fälle verwendet und verwaltet werden.

| Auftragstyp           | Beschreibung     |
| :----------------- | :----------     |
|Hinzufügen von Daten zu einem Übersichts Satz | Ein Benutzer fügt die Ergebnisse einer Suche zu einem Übersichts Satz hinzu. Dieser Auftrag besteht aus zwei Unteraufträgen: </br> </br>• **GatheringItems** – eine Liste von Elementen, die mit der Suchabfrage übereinstimmen (und der Office 365-Datenquelle, in der Sie sich befinden) wird generiert. </br>• **Einnahme & Indizierung** – die Elemente, die mit der Suchabfrage übereinstimmen, werden an einen Azure-Speicherort (in einem ** Prozess namens "Ingestion") kopiert, und anschließend werden diese Elemente im Azure-Speicher Speicherort erneut indiziert. Dieser neue Index wird beim Abfragen und Analysieren von Elementen im DataSet verwendet. </br></br>Weitere Informationen finden Sie unter [Hinzufügen von Suchergebnissen zu einem](add-data-to-review-set.md)Übersichts Satz. |
|Hinzufügen von Daten zu einem anderen Übersichts Satz | Ein Benutzer fügt in demselben Fall Dokumente aus einem Übersichts Satz zu einem anderen überprüfungssatz hinzu. Weitere Informationen finden Sie unter [Hinzufügen von Daten zu einem Übersichts Satz aus einem anderen](add-data-to-review-set-from-another-review-set.md)Übersichts Satz.|
|Hinzufügen von nicht-Office 365-Daten zu einem Übersichts Satz | Ein Benutzer lädt nicht-Office 365-Daten in einen Übersichts Satz hoch. Die Daten werden auch während dieses Prozesses indiziert. Beispielsweise werden Dateien von einem lokalen Dateiserver oder einem Clientcomputer in einen Übersichts Satz hochgeladen. Weitere Informationen finden Sie unter [Laden von nicht-Office 365-Daten in einen](load-non-office365-data.md)Übersichts Satz.| 
|Hinzufügen von wiederhergestellten Daten zu einem Übersichts Satz | Daten mit Verarbeitungsfehlern werden wiederhergestellt und in einen Übersichts Satz zurückgeladen. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md). | 
|Vergleichen von Auslastungs Sätzen | Ein Benutzer betrachtet die Unterschiede zwischen verschiedenen Auslastungs Sätzen in einem Übersichts Satz. Ein Auslastungs Satz ist eine Instanz des Hinzufügens von Daten zu einem Übersichts Satz. Wenn Sie beispielsweise die Ergebnisse von zwei verschiedenen Suchvorgängen zu demselben Übersichts Satz hinzufügen, würde jeder einen Lasten Satz darstellen. Weitere Informationen finden Sie unter [Manage Auslastung Sets](manage-load-sets.md). |
|Konvertieren von gehandelten Dokumenten in PDF|Nachdem ein Benutzer ein Dokument in einem Übersichts Satz mit Anmerkungen versehen und einen Teil davon bearbeitet hat, können Sie das Dokument in eine PDF-Datei konvertieren. Dadurch wird sichergestellt, dass der behandelte Teil nicht sichtbar ist, wenn das Dokument zur Präsentation exportiert wird. Weitere Informationen finden Sie unter [Anzeigen von Dokumenten in einem Übersichts Satz](annotating-and-redacting-documents.md). |
|Schätzen von Suchergebnissen | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), sucht das Such Tool den Index nach Elementen, die mit der Suchabfrage übereinstimmen, und bereitet eine Schätzung vor, die die Anzahl und Gesamtgröße aller Elemente bei der Suche und die Anzahl der Datenquellen anbraten Ched.  Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall](collecting-data-for-ediscovery.md). | 
|Vorbereiten von Daten für den Export | Ein Benutzer exportiert Dokumente aus einem Übersichts Satz aus einem. Nach Abschluss des Exportvorgangs können die exportierten Daten auf einen lokalen Computer heruntergeladen werden. Weitere Informationen finden Sie unter [exportieren](exporting-data-ediscover20.md)von Falldaten. | 
|Vorbereiten auf die Fehlerbehebung |Wenn ein Benutzer eine Datei auswählt und eine neue Fehlerkorrektur in der Fehleransicht auf der Registerkarte **Verarbeitung** eines Falls erstellt, besteht der erste Schritt in diesem Prozess darin, die Datei mit dem Verarbeitungsfehler an einen Azure-Speicherort in der Microsoft-Cloud hochzuladen. Dieser Auftrag verfolgt den Fortschritt des Uploads. Weitere Informationen zum Fehlerkorrektur-Workflow finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md). | 
|Vorbereiten der Suchvorschau | Nachdem ein Benutzer eine neue Suche erstellt und ausgeführt hat (oder eine vorhandene Suche erneut ausführt), bereitet das Such Tool eine Beispiel Teilmenge der Elemente (die mit der Suchabfrage übereinstimmen) vor, die in der Vorschau angezeigt werden können. Die Vorschau der Suchergebnisse hilft Ihnen bei der Bestimmung der Effektivität der Suche.  Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall](collecting-data-for-ediscovery.md#view-search-results-and-statistics). | 
|Erneutes Indizieren von Depotdaten | Wenn Sie einen Verwalter zu einem Fall hinzufügen, werden alle teilweise indizierten Elemente in den ausgewählten Datenquellen der Depotbank durch einen Prozess namens *Advanced Indexing*neu indiziert. Dieser Auftrag wird auch ausgelöst, wenn Sie auf der Registerkarte **Verarbeitung** eines Falls auf Index **Aktualisieren** in der Indexansicht klicken. Weitere Informationen finden Sie unter [Erweiterte Indizierung von Depotbank-Daten](indexing-custodian-data.md).
|Running Analytics | Ein Benutzer analysiert Daten in einem Überprüfungs Satz, indem er erweiterte eDiscovery Analytics-Tools wie near Duplicate Detection, e-Mail-Threading-Analyse und Design Analyse ausführt. Weitere Informationen finden Sie unter [Analysieren von Daten in einem](analyzing-data-in-review-set.md)Übersichts Satz. | 
|Markieren von Dokumenten | Dieser Auftrag wird ausgelöst, wenn ein Benutzer beim Überprüfen von Dokumenten in **** einem Überprüfungs Satz auf **Tagging-Auftrag starten** klickt. Ein Benutzer kann diesen Auftrag nach dem Markieren von Dokumenten in einem Übersichts Satz starten und diese dann im Dokumentbereich anzeigen massenweise auswählen. Weitere Informationen finden Sie unter [Tag Documents in a Review Set](tagging-documents.md). | 
|||


## <a name="job-status"></a>Auftragsstatus

In der folgenden Tabelle werden die verschiedenen Statuszustände für Aufträge beschrieben.

| Status           | Beschreibung     |
| :----------------- | :----------     |
| Übermittelt | Ein neuer Auftrag wurde erstellt.  Das Datum und die Uhrzeit, zu der der Auftrag übermittelt wurde, werden in der Spalte **erstellt** auf der Registerkarte **Aufträge** angezeigt. |
| Fehler bei Übermittlung | Fehler bei der Auftragsübermittlung.  Sie sollten versuchen, die Aktion, die den Auftrag ausgelöst hat, erneut auszuführen. |
| In Arbeit | Der Auftrag ausgeführt wird, können Sie den Fortschritt des Auftrags auf der Registerkarte **Aufträge** überwachen. |
| Erfolgreiche | Der Auftrag wurde erfolgreich abgeschlossen. Das Datum und die Uhrzeit, zu der der Auftrag abgeschlossen ist, wird in der Spalte **abgeschlossen** auf der Registerkarte **Aufträge** angezeigt. |
| Teilweise erfolgreich | Der Auftrag war teilweise erfolgreich. |
| Failed | Fehler beim Auftrag.  Sie sollten versuchen, die Aktion, die den Auftrag ausgelöst hat, erneut auszuführen. Wenn der Auftrag ein zweites Mal fehlschlägt, empfehlen wir, dass Sie sich an den Microsoft-Support wenden und die Supportinformationen aus dem Auftrag bereitstellen. |

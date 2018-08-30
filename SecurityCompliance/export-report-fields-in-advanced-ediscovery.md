---
title: Exportieren von Berichtsfeldern in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: Beschreibt die Felder, die in das Exportieren von Berichten für erweiterte eDiscovery enthalten sind.
ms.openlocfilehash: a578523098248bcfa16ea8ba97d756d97ba060fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529138"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Exportieren von Berichtsfeldern in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema werden die erweiterten eDiscovery-Export Berichtsfelder für die Standard- und alle Vorlagen.
  
## <a name="export-report-fields"></a>Exportieren von Berichtsfeldern

In der folgenden Tabelle werden die Felder für jede Vorlage exportieren.
  
|**Name des Felds exportieren**|**Gruppe**|**Beschreibung**|**Verfügbar in den Standard-Vorlage**|**Verfügbar in allen Vorlage**|
|:-----|:-----|:-----|:-----|:-----|
|Soll  <br/> |Allgemein  <br/> |Nummer der Zeile.  <br/> |Ja  <br/> |Ja  <br/> |
|File_ID  <br/> |Allgemein  <br/> |Datei-ID.  <br/> |Ja  <br/> |Ja  <br/> |
|File_class  <br/> |Verarbeitung  <br/> |File-Klasse.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_ID  <br/> |Verarbeitung  <br/> |Numerische Kennung, die zum Gruppieren der Dateien (in der Regel e-Mail-Instanz und die zugehörigen Anlagen) verwendet wird.  <br/> |Ja  <br/> |Ja  <br/> |
|For_review  <br/> |Verarbeitung  <br/> |Flag, um anzugeben, dass das Feld in Export zur Überprüfung einbezogen werden.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_file_name  <br/> |Verarbeitung  <br/> |Systemeigene Dateiname, ohne zu verweisen, Ordner und Erweiterung.  <br/> |Ja  <br/> |Ja  <br/> |
|Verwalter  <br/> |Allgemein  <br/> |Verwaltungsberechtigter der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Set_ID  <br/> |Analyse  <br/> |"Festlegen von ND" oder "E-Mail-Gruppe" Id.  <br/> |Ja  <br/> |Ja  <br/> |
|Inclusive_type  <br/> |E-Mail  <br/> |Gibt an, ob die Datei einschließlich wird gemäß der folgenden Werte: 0 - nicht inklusive 1 - einschließlich 2 - minus 3 - inklusive Kopie inklusive.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_pivot  <br/> |NEAR Duplikate  <br/> |Gibt an, ob die Datei eine Pivot ist.  <br/> |Ja  <br/> |Ja  <br/> |
|Similarity_percent  <br/> |NEAR Duplikate  <br/> |Prozentsatz der Ähnlichkeit relativ zu der PivotTable.  <br/> |Ja  <br/> |Ja  <br/> |
|Duplicate_subset  <br/> |NEAR Duplikate  <br/> |Eindeutiger Bezeichner der doppelten Teilmenge. Gibt an, ob die Datei Text genaue Duplikate hat.  <br/> |Ja  <br/> |Ja  <br/> |
|Datum  <br/> |Allgemein  <br/> |Datum der Datei (hängt Dateityp - e-Mail: Absendedatum; Dokument: Änderungsdatum).  <br/> |Ja  <br/> |Ja  <br/> |
|Dominant_theme  <br/> |Analyse  <br/> |Primäre Design der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Themes_list  <br/> |Designs  <br/> |Liste der Designnamen.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Eindeutiger Bezeichner der numerischen Nearduplicate aus einem Satz.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_set  <br/> |E-Mail  <br/> |Legen Sie eindeutige Identifikationsnummer einer e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_thread  <br/> |E-Mail  <br/> |Beschreibt die Position der e-Mail innerhalb des e-Mail-besteht aus allen Knoten-IDs aus dem Stammverzeichnis auf aktuelle e-Mail, getrennt durch Punkte festgelegt.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_Betreff  <br/> |E-Mail  <br/> |Betreff der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_date_sent  <br/> |E-Mail  <br/> |Datum, an dem die e-Mail-Nachricht gesendet wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_participants  <br/> |E-Mail  <br/> |E-Mail-Adressen von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Links.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_participant_domains  <br/> |E-Mail  <br/> |Domänen von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Verknüpfung.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_sender  <br/> |E-Mail  <br/> |Name des e-Mail-Absenders und/oder Adresse.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_sender_domain  <br/> |E-Mail  <br/> |E-Mail-Domäne des Absenders.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_to  <br/> |E-Mail  <br/> |An die Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_cc  <br/> |E-Mail  <br/> |CC-Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_bcc  <br/> |E-Mail  <br/> |BCC-Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_recipient_domains  <br/> |E-Mail  <br/> |E-Mail-Empfänger (an, CC und BCC) Domänen.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_date_received  <br/> |E-Mail  <br/> |Datum, an dem e-Mail empfangen wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_action  <br/> |E-Mail  <br/> |Werte: Entsprechend der E-Mail-Betreff: "Weiterleiten" (für "Firmware:"), "Antwort" (für "RE:") oder "Andere" (andere Betrefftext).  <br/> |Ja  <br/> |Ja  <br/> |
|Meeting_Start_Date/Uhrzeit  <br/> ||Datum und Uhrzeit, an dem ein Besprechungselement gestartet.  <br/> |Ja  <br/> |Ja  <br/> |
|Meeting_End_Date/Uhrzeit  <br/> ||Datum und Uhrzeit, an dem ein Besprechungselement beendet wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|File_relevance_score  <br/> |Relevanz  <br/> |Relevanz Faktor (0 bis 100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_relevance_score  <br/> |Relevanz  <br/> |Max-Produktfamilie Relevanz Faktor (0 bis 100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_tag  <br/> |Relevanz  <br/> |Markieren der Datei, wenn die Datei manuell in Relevanz markiert wurde. Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_load_group  <br/> |Relevanz  <br/> |Relevanz Gruppe laden, für die angegebene Datei mit einem Feld pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Normalized_relevance_score  <br/> |Relevanz  <br/> |(0 bis 100) Faktor normalisierte Relevanz, die zwischen Probleme und lädt vergleichbar ist.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_seed  <br/> |Relevanz  <br/> |Markieren der Datei, wenn diese Liste festgelegt wurde, werden als Ausgangswert-Datei in Relevanz pro/Problemkategorie.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_pre markiert  <br/> |Relevanz  <br/> |Markieren der Datei, wenn es als vor dem markierten in Relevanz pro Problem/Kategorie festgelegt wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_status_description  <br/> |Relevanz  <br/> |Beschreibung des Relevanz Status.  <br/> |Ja  <br/> |Ja  <br/> |
|Kommentar  <br/> |Allgemein  <br/> |Vom Benutzer eingegebene Kommentar.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_input_path  <br/> |Verarbeitung  <br/> |Exportieren Sie input Pfad.  <br/> |Ja  <br/> |Ja  <br/> |
|Pivot_ID  <br/> |NEAR Duplikate  <br/> |Pivot-ID der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_size  <br/> |Verarbeitung  <br/> |Anzahl von Dateien in einer Familie.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_type  <br/> |Verarbeitung  <br/> |Systemeigene Dateityp. Arbeitsblatt oder Präsentation.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_MD5  <br/> |Verarbeitung  <br/> |MD5-Hashwert der systemeigenen Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_size  <br/> |Verarbeitung  <br/> |Systemeigene Dateigröße.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_extension  <br/> |Verarbeitung  <br/> |Systemeigene Erweiterung.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_date_modified  <br/> |Dokumenteigenschaften  <br/> |Datum, die systemeigene Datei übernommen aus der Datei Metadaten geändert wurde, an.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_date_created  <br/> |Dokumenteigenschaften  <br/> |Systemeigene Datumsdatei wurde, stammt aus den Metadaten der Datei erstellt.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_modified_by  <br/> |Dokumenteigenschaften  <br/> |Benutzer, die systemeigene Datei, übernommen aus der Datei Metadaten geändert wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_date_modified  <br/> |Dokumenteigenschaften  <br/> |Systemeigene Datumsdatei wurde übernommen aus den Feldern SharePoint oder Exchange, geändert.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_date_created  <br/> |Dokumenteigenschaften  <br/> |Systemeigene Datumsdatei wurde SharePoint oder Exchange Felder entnommen, erstellt.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_modified_by  <br/> |Dokumenteigenschaften  <br/> |Benutzer, die zuletzt geändert systemeigene Datei entnommen SharePoint oder Exchange-Felder.  <br/> |Ja  <br/> |Ja  <br/> |
|Compound_path  <br/> |Verarbeitung  <br/> |Systemeigene Dateipfad, einschließlich der zusammengesetzten Quelle.  <br/> |Ja  <br/> |Ja  <br/> |
|Input_path  <br/> |Verarbeitung  <br/> |Pfad der Eingabedatei.  <br/> |Ja  <br/> |Ja  <br/> |
|Input_date_modified  <br/> |Verarbeitung  <br/> |Eingabedatei Datum der letzten Änderung.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_ET_sort_excl_attach  <br/> |Analyse  <br/> |Verkettung von E-Mails und ND festgelegt zur Überprüfung. Hatte ' wird hinzugefügt, wie e-Mail-Ssets ND Sets und "E" Präfix hinzugefügt wird.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_ET_sort_incl_attach  <br/> |Analyse  <br/> |Verkettung von E-Mails festlegen und würde ND zur Prüfung festlegen ' wird hinzugefügt, sobald ein Präfix an ND Sets und "E" hinzugefügt wird auf E-Mail wird. Darüber hinaus wird jede e-Mail innerhalb einer Email_set ihre entsprechenden Anhänge folgen.  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_custodians  <br/> |Allgemein  <br/> |Verwalter von Aufhebung der täuschen-Dateien  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_file_IDs  <br/> |Allgemein  <br/> |IDs der Aufhebung der täuschen-Dateien  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_paths  <br/> |Allgemein  <br/> |Pfade der Aufhebung der täuschen-Dateien  <br/> |Ja  <br/> |Ja  <br/> |
|File_key  <br/> |Allgemein  <br/> |Interner Bezeichner für die zukünftige Verwendung.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_native_path  <br/> |Verarbeitung  <br/> |Pfad der systemeigenen Datei im Exportpaket.  <br/> |Ja  <br/> |Ja  <br/> |
|Extracted_text_path  <br/> |Verarbeitung  <br/> |Pfad der extrahierten Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_batch  <br/> |Verarbeitung  <br/> |Batch-ID für Batch importieren.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_status_ID  <br/> |Verarbeitung  <br/> |Bezeichner darstellen Phase Prozessstatus.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_status_description  <br/> |Verarbeitung  <br/> |Beschreibung der Phase Status verarbeiten: erfolgreich oder fehlerbeschreibung.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_status_ID  <br/> |Verarbeitung  <br/> |ID des Exportstatus.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_status_description  <br/> |Verarbeitung  <br/> |Beschreibung des Exportstatus; erfolgreich oder fehlerbeschreibung.  <br/> |Ja  <br/> |Ja  <br/> |
|Read_percent  <br/> |Relevanz  <br/> |Lesen Sie % (0 bis 100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_author  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Autor.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_comments  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Kommentare.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_keywords  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Schlüsselwörter.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_last_saved_by  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: zuletzt gespeichert von.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_revision  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Revisionsnummer.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_subject  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Betreff.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_template  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Vorlage.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_title  <br/> |Dokumenteigenschaften  <br/> |Dokumenteigenschaften: Titel.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_has_attachment  <br/> |E-Mail  <br/> |Gibt an, ob die e-Mail eine oder mehrere Anlagen hat.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_importance  <br/> |E-Mail  <br/> |E-Mail-Importance-Eigenschaft.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_level  <br/> |E-Mail  <br/> |Gibt an, der e-Mail-Ebene innerhalb der e-Mail-Thread. Für den Wert der angefügten e-Mail-Anlagen.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_recipients  <br/> |E-Mail  <br/> |E-Mail-Empfänger Namen und/oder Adressen (an, CC und BCC).  <br/> |Nein  <br/> |Ja  <br/> |
|Email_security  <br/> |E-Mail  <br/> |E-Mail-Sicherheit-Eigenschaft.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_sensitivity  <br/> |E-Mail  <br/> |E-Mail-Sensitivity-Eigenschaft.  <br/> |Nein  <br/> |Ja  <br/> |
|Export_batch  <br/> |Verarbeitung  <br/> |Den letzten Export Batch Dateinamen.  <br/> |Nein  <br/> |Ja  <br/> |
|Export_session  <br/> |Verarbeitung  <br/> |Datei des letzten Export Sitzung Id einschließlich Datum.  <br/> |Nein  <br/> |Ja  <br/> |
|Extracted_text_length  <br/> |Verarbeitung  <br/> |Länge der Textdatei extrahierter.  <br/> |Nein  <br/> |Ja  <br/> |
|Family_duplicate_set  <br/> |Verarbeitung  <br/> |Numerische Kennung für Familien, die genaue Text Duplikate voneinander sind (alle Familienangehörige sind jeweils - genaue Duplikate).  <br/> |Nein  <br/> |Ja  <br/> |
|Has_Text  <br/> |Verarbeitung  <br/> |Gibt an, ob ein Text in der Datei vorhanden ist: 0 – keine; 1 – Ja.  <br/> |Nein  <br/> |Ja  <br/> |
|Input_file_ID  <br/> |Verarbeitung  <br/> |ID der Input-Datei aus der Datei aus extrahiert wurde.  <br/> |Nein  <br/> |Ja  <br/> |
|Native_SHA_256  <br/> |Verarbeitung  <br/> |SHA-256 Hashwert der systemeigenen Datei.  <br/> |Nein  <br/> |Ja  <br/> |
|O365_authors  <br/> |Dokumenteigenschaften  <br/> |Benutzer, die systemeigene Datei, übernommen aus SharePoint oder Exchange Felder geändert wurde.  <br/> |Nein  <br/> |Ja  <br/> |
|O365_created_by  <br/> |Dokumenteigenschaften  <br/> |Benutzer, die systemeigene Datei entnommen SharePoint oder Exchange Felder erstellt hat.  <br/> |Nein  <br/> |Ja  <br/> |
|Parent_node  <br/> |E-Mail  <br/> |Bezieht sich einen Knoten in einer e-Mail-Thread auf dem nächsten übergeordneten Knoten, der keiner fehlenden Verknüpfung ist.  <br/> |Nein  <br/> |Ja  <br/> |
|Set_order_inclusives_first  <br/> |E-Mail  <br/> |E-Mail-Nachrichten und Anlagen: Zähler chronologischen Reihenfolge (Inclusives ersten). Dokumente: um dreht Tür und andere nach Ähnlichkeit Faktor, absteigend.  <br/> |Nein  <br/> |Ja  <br/> |
|Tagged_By  <br/> |Relevanz  <br/> |Benutzer, der die Datei für die bestimmten Problem in Relevanz markiert.  <br/> |Nein  <br/> |Ja  <br/> |
|Word_count  <br/> |Analyse  <br/> |Anzahl der Wörter im Dokument.  <br/> |Nein  <br/> |Ja  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Exportieren von Groß-/Kleinschreibung Daten mit erweiterten eDiscovery](export-case-data-in-advanced-ediscovery.md)
  
[Exportieren Sie Ergebnisse](export-results-in-advanced-ediscovery.md)
  
[Anzeigen des Verlaufs Batch und ältere Ergebnisse exportieren](view-batch-history-and-export-past-results.md)
  


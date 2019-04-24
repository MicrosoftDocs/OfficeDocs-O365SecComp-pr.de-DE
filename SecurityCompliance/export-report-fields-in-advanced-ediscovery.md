---
title: Exportieren von Berichtfeldern in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: Beschreibt alle Felder, die in den Export Berichten für Advanced eDiscovery enthalten sind.
ms.openlocfilehash: 36443f6aac70392603acfe6702bcc4fe7a4f4bf3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255463"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Exportieren von Berichtfeldern in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema werden die erweiterten eDiscovery-Export Bericht Felder für die Standard-und alle-Vorlagen beschrieben.
  
## <a name="export-report-fields"></a>Exportieren von Berichtsfeldern

In der folgenden Tabelle sind die Felder für jede Exportvorlage aufgeführt.
  
|**Name des Export Felds**|**Group**|**Beschreibung**|**Verfügbar in Standard Vorlage**|**Verfügbar in allen Vorlagen**|
|:-----|:-----|:-----|:-----|:-----|
|ROW_NUMBER  <br/> |Allgemein  <br/> |Zeilennummer.  <br/> |Ja  <br/> |Ja  <br/> |
|File_ID  <br/> |Allgemein  <br/> |Datei-ID.  <br/> |Ja  <br/> |Ja  <br/> |
|File_class  <br/> |Verarbeitung  <br/> |File-Klasse.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_ID  <br/> |Verarbeitung  <br/> |Numerischer Bezeichner, der zum Gruppieren von Dateien verwendet wird (in der Regel e-Mail-Instanz und zugehörige Anlagen).  <br/> |Ja  <br/> |Ja  <br/> |
|For_review  <br/> |Verarbeitung  <br/> |Flag, das angibt, dass das Feld zur Überarbeitung in den Export eingeschlossen werden soll.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_file_name  <br/> |Verarbeitung  <br/> |Systemeigener Dateiname ohne Verweis auf Ordner und Erweiterung.  <br/> |Ja  <br/> |Ja  <br/> |
|Hüter  <br/> |Allgemein  <br/> |Verwalter der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Set_ID  <br/> |Analysieren  <br/> |"ND-Satz" oder "e-Mail-Satz"-ID.  <br/> |Ja  <br/> |Ja  <br/> |
|Inclusive_type  <br/> |E-Mail  <br/> |Gibt an, ob die Datei inklusiv ist, entsprechend den folgenden Werten: 0-nicht inklusive, 1-Inclusive, 2-inklusive minus, 3-inclusive-Kopie.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_pivot  <br/> |Duplikate in der Nähe  <br/> |Gibt an, ob es sich bei der Datei um eine Pivot handelt.  <br/> |Ja  <br/> |Ja  <br/> |
|Similarity_percent  <br/> |Duplikate in der Nähe  <br/> |Prozentualer Anteil der Ähnlichkeit relativ zum Drehpunkt.  <br/> |Ja  <br/> |Ja  <br/> |
|Duplicate_subset  <br/> |Duplikate in der Nähe  <br/> |Eindeutiger Bezeichner der doppelten Teilmenge. Gibt an, ob die Datei exakte Text Duplikate enthält.  <br/> |Ja  <br/> |Ja  <br/> |
|Datum  <br/> |Allgemein  <br/> |Datum der Datei (abhängig vom Dateityp – e-Mail: Sendedatum; Dokument: Datum geändert).  <br/> |Ja  <br/> |Ja  <br/> |
|Dominant_theme  <br/> |Analysieren  <br/> |Primäres Design der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Themes_list  <br/> |Designs  <br/> |Liste der Designnamen.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Eindeutiger numerischer Bezeichner eines Nearduplicate-Satzes.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_set  <br/> |E-Mail  <br/> |Eindeutiger numerischer Bezeichner eines e-Mail-Satzes.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_thread  <br/> |E-Mail  <br/> |Beschreibt die Position der e-Mail innerhalb des e-Mail-Satzes besteht aus allen Knoten-IDs vom Stamm zur aktuellen e-Mail, getrennt durch Punkte.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_subject  <br/> |E-Mail  <br/> |Betreff der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_date_sent  <br/> |E-Mail  <br/> |Datum, an dem die e-Mail gesendet wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_participants  <br/> |E-Mail  <br/> |E-Mail-Adressen aller Teilnehmer in einem e-Mail-Thread, einschließlich fehlender Links.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_participant_domains  <br/> |E-Mail  <br/> |Domänen aller Teilnehmer in einem e-Mail-Thread, einschließlich fehlender Links.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_sender  <br/> |E-Mail  <br/> |E-Mail-Absender Name und/oder-Adresse.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_sender_domain  <br/> |E-Mail  <br/> |Die Domäne des Absenders.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_to  <br/> |E-Mail  <br/> |An den Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_cc  <br/> |E-Mail  <br/> |CC-Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_bcc  <br/> |E-Mail  <br/> |BCC-Empfänger der e-Mail.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_recipient_domains  <br/> |E-Mail  <br/> |E-Mail-Empfängerdomänen (an, CC und BCC).  <br/> |Ja  <br/> |Ja  <br/> |
|Email_date_received  <br/> |E-Mail  <br/> |Datum, an dem e-Mails empfangen wurden.  <br/> |Ja  <br/> |Ja  <br/> |
|Email_action  <br/> |E-Mail  <br/> |Werte: gemäß e-Mail-Betreff: "Forward" (für "FW:"), "Reply" (für "RE:") oder "Other" (anderer Betrefftext).  <br/> |Ja  <br/> |Ja  <br/> |
|Meeting_Start_Date/Zeit  <br/> ||Das Datum und die Uhrzeit, zu denen ein Besprechungselement gestartet wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Meeting_End_Date/Zeit  <br/> ||Das Datum und die Uhrzeit, zu denen ein Besprechungselement beendet wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|File_relevance_score  <br/> |Relevanz  <br/> |Relevance Score (0-100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_relevance_score  <br/> |Relevanz  <br/> |Maximale Familien Relevanz (0-100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_tag  <br/> |Relevanz  <br/> |Tagging der Datei, wenn die Datei manuell in Relevanz markiert wurde. Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_load_group  <br/> |Relevanz  <br/> |Relevanz laden Gruppe der angegebenen Datei mit einem Feld pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Normalized_relevance_score  <br/> |Relevanz  <br/> |Normalisierte Relevanz (0-100), die zwischen Problemen und Lasten vergleichbar ist.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_seed  <br/> |Relevanz  <br/> |Tagging der Datei, wenn Sie als eine seeddatei in Relevanz pro Problem/Kategorie festgelegt wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Marked_as_pre-Tagged  <br/> |Relevanz  <br/> |Tagging der Datei, wenn Sie in Relevanz pro Problem/Kategorie als Pre-Tagged festgelegt wurde.  <br/> |Ja  <br/> |Ja  <br/> |
|Relevance_status_description  <br/> |Relevanz  <br/> |Beschreibung des relevanzstatus.  <br/> |Ja  <br/> |Ja  <br/> |
|Kommentar  <br/> |Allgemein  <br/> |Vom Benutzer eingegebene Kommentar.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_input_path  <br/> |Verarbeitung  <br/> |Eingabepfad exportieren.  <br/> |Ja  <br/> |Ja  <br/> |
|Pivot_ID  <br/> |Duplikate in der Nähe  <br/> |Pivot-ID der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Family_size  <br/> |Verarbeitung  <br/> |Anzahl der Dateien in einer Familie.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_type  <br/> |Verarbeitung  <br/> |Systemeigener Dateityp. Beispielsweise Tabellenkalkulation oder Präsentation.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_MD5  <br/> |Verarbeitung  <br/> |MD5-Hashwert der systemeigenen Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_size  <br/> |Verarbeitung  <br/> |Systemeigene Dateigröße.  <br/> |Ja  <br/> |Ja  <br/> |
|Native_extension  <br/> |Verarbeitung  <br/> |Native Dateierweiterung.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_date_modified  <br/> |Dokumenteigenschaften  <br/> |Datum systemeigene Datei wurde geändert, entnommen aus den Metadaten der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_date_created  <br/> |Dokumenteigenschaften  <br/> |Datum systemeigene Datei wurde erstellt, entnommen aus den Metadaten der Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_modified_by  <br/> |Dokumenteigenschaften  <br/> |Benutzer, der die systemeigene Datei aus den Metadaten der Datei geändert hat.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_date_modified  <br/> |Dokumenteigenschaften  <br/> |Das Datum, an dem die systemeigene Datei geändert wurde, stammt aus den Feldern SharePoint oder Exchange.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_date_created  <br/> |Dokumenteigenschaften  <br/> |Die systemeigene Datei wurde aus SharePoint-oder Exchange-Feldern erstellt.  <br/> |Ja  <br/> |Ja  <br/> |
|O365_modified_by  <br/> |Dokumenteigenschaften  <br/> |Benutzer, der die systemeigene Datei zuletzt aus SharePoint-oder Exchange-Feldern geändert hat.  <br/> |Ja  <br/> |Ja  <br/> |
|Compound_path  <br/> |Verarbeitung  <br/> |Systemeigener Dateipfad, einschließlich der zusammengesetzten Quelle.  <br/> |Ja  <br/> |Ja  <br/> |
|Input_path  <br/> |Verarbeitung  <br/> |Pfad der Eingabedatei.  <br/> |Ja  <br/> |Ja  <br/> |
|Input_date_modified  <br/> |Verarbeitung  <br/> |Datum Eingabedatei wurde zuletzt geändert.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_ET_sort_excl_attach  <br/> |Analysieren  <br/> |Verkettung von e-Mail-Satz und ND-Satz zur Überprüfungen. 'D ' wird als Präfix zu ND-Sätzen hinzugefügt, und "E" wird e-Mail-ssets hinzugefügt.  <br/> |Ja  <br/> |Ja  <br/> |
|ND_ET_sort_incl_attach  <br/> |Analysieren  <br/> |Die Verkettung von e-Mail-Satz und ND-Satz für Übersetzung 'D ' wird als Präfix zu ND-Sätzen hinzugefügt, und "E" wird e-Mail-Sätzen hinzugefügt. Darüber hinaus werden jeder e-Mail innerhalb einer Email_set die entsprechenden Anhänge gefolgt.  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_custodians  <br/> |Allgemein  <br/> |Verwalter von deduped files  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_file_IDs  <br/> |Allgemein  <br/> |IDs von debetrogenen Dateien  <br/> |Ja  <br/> |Ja  <br/> |
|Deduped_paths  <br/> |Allgemein  <br/> |Pfade von deduped files  <br/> |Ja  <br/> |Ja  <br/> |
|File_key  <br/> |Allgemein  <br/> |Interner Bezeichner für zukünftige Verwendung.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_native_path  <br/> |Verarbeitung  <br/> |Pfad der systemeigenen Datei im Exportpaket.  <br/> |Ja  <br/> |Ja  <br/> |
|Extracted_text_path  <br/> |Verarbeitung  <br/> |Pfad der extrahierten Datei.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_batch  <br/> |Verarbeitung  <br/> |Batch Bezeichner für Import Batch.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_status_ID  <br/> |Verarbeitung  <br/> |Bezeichner, der den Status der Prozessstufe darstellt.  <br/> |Ja  <br/> |Ja  <br/> |
|Process_status_description  <br/> |Verarbeitung  <br/> |Prozessstatus Beschreibung: erfolgreich oder Fehlerbeschreibung.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_status_ID  <br/> |Verarbeitung  <br/> |ID des Exportstatus.  <br/> |Ja  <br/> |Ja  <br/> |
|Export_status_description  <br/> |Verarbeitung  <br/> |Beschreibung des Exportstatus; erfolgreiche oder Fehlerbeschreibung.  <br/> |Ja  <br/> |Ja  <br/> |
|Read_percent  <br/> |Relevanz  <br/> |Lesen Sie% (0-100). Pro Problem.  <br/> |Ja  <br/> |Ja  <br/> |
|Doc_author  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Author.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_comments  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Kommentare.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_keywords  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Schlüsselwörter.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_last_saved_by  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: zuletzt gespeichert von.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_revision  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Revisionsnummer.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_subject  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Betreff.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_template  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Vorlage.  <br/> |Nein  <br/> |Ja  <br/> |
|Doc_title  <br/> |Document-Eigenschaften  <br/> |Dokumenteigenschaften: Title.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_has_attachment  <br/> |E-Mail  <br/> |Gibt an, ob die e-Mail eine oder mehrere Anlagen enthält.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_importance  <br/> |E-Mail  <br/> |Eigenschaft für e-Mail-Wichtigkeit.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_level  <br/> |E-Mail  <br/> |Gibt die e-Mail-Ebene im e-Mail-Thread an. Für Anlagen der Wert der angefügten e-Mail.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_recipients  <br/> |E-Mail  <br/> |E-Mail-Empfänger Name und/oder Adressen (an, CC und BCC).  <br/> |Nein  <br/> |Ja  <br/> |
|Email_security  <br/> |E-Mail  <br/> |E-Mail-Sicherheitseigenschaft.  <br/> |Nein  <br/> |Ja  <br/> |
|Email_sensitivity  <br/> |E-Mail  <br/> |Eigenschaft für die e-Mail-Vertraulichkeit.  <br/> |Nein  <br/> |Ja  <br/> |
|Export_batch  <br/> |Verarbeitung  <br/> |Der letzte Export Batch Name der Datei.  <br/> |Nein  <br/> |Ja  <br/> |
|Export_session  <br/> |Verarbeitung  <br/> |Die letzte Export Sitzungs-ID der Datei, einschließlich Datum.  <br/> |Nein  <br/> |Ja  <br/> |
|Extracted_text_length  <br/> |Verarbeitung  <br/> |Die Zeichen Länge der extrahierten Textdatei.  <br/> |Nein  <br/> |Ja  <br/> |
|Family_duplicate_set  <br/> |Verarbeitung  <br/> |Numerischer Bezeichner für Familien, die exakte Text Duplikate voneinander sind (beziehungsweise-alle Mitglieder der Familien sind exakte Duplikate).  <br/> |Nein  <br/> |Ja  <br/> |
|Has_Text  <br/> |Verarbeitung  <br/> |Gibt an, ob ein Text in der Datei vorhanden ist: 0-Nein; 1-ja.  <br/> |Nein  <br/> |Ja  <br/> |
|Input_file_ID  <br/> |Verarbeitung  <br/> |ID der Eingabedatei, aus der die Datei extrahiert wurde.  <br/> |Nein  <br/> |Ja  <br/> |
|Native_SHA_256  <br/> |Verarbeitung  <br/> |SHA-256-Hashwert der systemeigenen Datei.  <br/> |Nein  <br/> |Ja  <br/> |
|O365_authors  <br/> |Document-Eigenschaften  <br/> |Benutzer, die systemeigene Dateien aus SharePoint-oder Exchange-Feldern geändert haben.  <br/> |Nein  <br/> |Ja  <br/> |
|O365_created_by  <br/> |Document-Eigenschaften  <br/> |Benutzer, der systemeigene Dateien erstellt hat, die aus SharePoint-oder Exchange-Feldern entnommen wurden.  <br/> |Nein  <br/> |Ja  <br/> |
|Parent_node  <br/> |E-Mail  <br/> |Verknüpft einen Knoten in einem e-Mail-Thread mit dem nächstgelegenen übergeordneten Knoten, der kein fehlender Link ist.  <br/> |Nein  <br/> |Ja  <br/> |
|Set_order_inclusives_first  <br/> |E-Mail  <br/> |E-Mails und Anhänge: Zähler chronologische Reihenfolge (einschließlich zuerst). Documents: pivotiert zuerst und der Rest nach Ähnlichkeits Bewertung absteigend.  <br/> |Nein  <br/> |Ja  <br/> |
|Tagged_By  <br/> |Relevanz  <br/> |Der Benutzer, der die Datei für das jeweilige Problem relevant markiert hat.  <br/> |Nein  <br/> |Ja  <br/> |
|Word_count  <br/> |Analysieren  <br/> |Die Anzahl der Wörter im Dokument.  <br/> |Nein  <br/> |Ja  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Exportieren von Falldaten mit Advanced eDiscovery](export-case-data-in-advanced-ediscovery.md)
  
[Exportieren von Ergebnissen](export-results-in-advanced-ediscovery.md)
  
[Anzeigen des Batch Verlaufs und exportieren vergangener Ergebnisse](view-batch-history-and-export-past-results.md)
  


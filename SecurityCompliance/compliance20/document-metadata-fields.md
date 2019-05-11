---
title: Dokument-Metadatenfelder in Advanced eDiscovery
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
ms.openlocfilehash: e45400726537a3b1ebadcc3d828d9cb8110e2100
ms.sourcegitcommit: 09fd88272187f82b6e635af83edabea08c2cc49c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2019
ms.locfileid: "33884753"
---
# <a name="document-metadata-fields-in-advanced-ediscovery"></a>Dokument-Metadatenfelder in Advanced eDiscovery

In der folgenden Tabelle sind die Metadatenfelder für Dokumente in einem Übersichts Satz in einem Fall in Advanced eDiscovery aufgeführt. Die Tabelle gibt den Namen des Metadatenfelds an, ob das Feld durchsucht werden kann, wenn eine Abfrage in einem Übersichts Satz läuft, ob das Feld vorhanden ist, wenn die Datei Metadaten eines ausgewählten Dokuments in einem Übersichts Satz angezeigt werden, und ob das Feld bei Dokumenten ein erneut exportiert.

| Feldname | Durchsuchbarer Feldname | Exportierter Feldname | Anzeige Feldname | Beschreibung |
| :- |  :- |  :- |  :- |  :- |
| Anlageninhalts-ID | AttachmentContentId |  | Anlageninhalts-ID | Anlageninhalts-ID des Elements. |
| Anlagennamen | AttachmentNames | Attachment_Names | Anlagennamen | Liste der Namen von Anlagen. |
| Anwalts-Client-Berechtigungs Bewertung | AttorneyClientPrivilegeScore |  | Anwalts-Client-Berechtigungs Bewertung | Attorney-Client-Berechtigungsmodell – Inhaltsbewertung. |
| Ursprung | Ursprung | Doc_authors | Ursprung | Autor aus den Dokumentmetadaten. |
| BCC | Bcc | Email_bcc | BCC | BCC-Feld für für Nachrichtentypen.  Format ist **Display \<Name SMTPAddress>**. |
| CC | Cc | Email_cc | CC | Feld CC für für Nachrichtentypen.  Format ist **Display \<Name SMTPAddress>**. |
| Konformitäts Bezeichnungen | ComplianceLabels | Compliance_labels | Konformitäts Bezeichnungen | Konformitäts Bezeichnungen in Office 365. |
| Zusammengesetzter Pfad | CompoundPath | Compound_path | Zusammengesetzter Pfad | Menschlich lesbarer Pfad, der die Quelle des Elements beschreibt. |
| Inhalt | Inhalt |  |  | Extrahierter Text des Elements. |
| Unterhaltungs Text | Unterhaltungs Text |  | Unterhaltungs Text | Unterhaltungs Text des Elements. |
| Unterhaltungsthema | Unterhaltungsthema |  | Unterhaltungsthema | Unterhaltungsthema des Elements. |
| Unterhaltungs-ID | ConversationId | Conversation_ID | Unterhaltungs-ID | Unterhaltungs-ID aus der Nachricht. |
| Unterhaltungs Index |  | Conversation_index | Unterhaltungs Index | Konversations Index aus der Nachricht. |
| Unterhaltungs-PDF-Zeit | ConversationPdfTime |  | Unterhaltungs-PDF-Zeit | Datum, an dem die PDF-Version der Unterhaltung erstellt wurde. |
| Unterhaltungs-Bearbeitungszeit | ConversationRedactionBurnTime |  | Unterhaltungs-Bearbeitungszeit | Datum, an dem die PDF-Version der Unterhaltung für den Chat erstellt wurde. |
| Dokument Erstellungsdatum | CreatedTime | Doc_date_created | Dokument Erstellungsdatum | Erstelldatum aus Dokumentmetadaten. |
| Custodian | Custodian | Custodian | Custodian | Name der Depotbank, der das Element zugeordnet wurde. |
| Datum | Datum | Datum | Datum | Date ist ein berechnetes Feld, das vom Dateityp abhängt.<br />**E-Mail**: Datum gesendet<br />**E-Mail-Anlagen**: Datum der letzten Änderung des Dokuments, falls nicht verfügbar, das gesendete Datum des übergeordneten Elements<br />**Eingebettete Dokumente**: Datum der letzten Änderung des Dokuments, falls nicht verfügbar, das Datum der letzten Änderung des übergeordneten Elements.<br />**SPO-Dokumente (einschließlich moderner Anhänge)**: SharePoint-Datum der letzten Änderung, falls nicht verfügbar, das Datum der letzten Änderung von Dokumenten<br />**Nicht-Office-Dokumente**: Datum der letzten Änderung<br />**Besprechungen**: Startdatum der Besprechung<br />**Voicemail**: Datum gesendet<br />**Sofortnachrichten**: gesendet am. |
| Andere Pfade | Dedupedcompoundpath | Deduped_compound_path | Andere Pfade | Liste der zusammengesetzten Pfade von Dokumenten, bei denen es sich um exakte Duplikate handelt (e-Mail: basierend auf Inhalt, Dokumente: basierend auf Hash). |
| Andere Verwalter | DedupedCustodians | Deduped_custodians | Andere Verwalter | Liste der Verwalter von Dokumenten, die exakte Duplikate sind (für e-Mails: basierend auf Inhalten; für Dokumente: basiert auf Hash). |
| Weitere Datei-IDs | DedupedFileIds | Deduped_file_IDs | Weitere Datei-IDs | Liste der Datei-IDs von Dokumenten, bei denen es sich um exakte Duplikate handelt (für e-Mails: basierend auf Inhalten; für Dokumente: basiert auf Hash). |
| Dokument Kommentare | DocComments | Doc_comments | Dokument Kommentare | Kommentare aus den Dokumentmetadaten. |
| Dokument Firma |  | Doc_company | Dokument Firma | Unternehmen aus den Dokumentmetadaten. |
| DocIndex |  |  |  | Der Index in der Familie. -1 oder 0 bedeutet, dass es sich um den Stamm handelt. |
| Dokument Schlüsselwörter |  | Doc_keywords | Dokument Schlüsselwörter | Schlüsselwörter aus den Dokumentmetadaten. |
| Dokument geändert von |  | Doc_modified_by | Dokument geändert von | Datum der letzten Änderung von Dokumentmetadaten. |
| Dokumentüberarbeitung |  | Doc_revision | Dokumentüberarbeitung | Revision aus den Dokumentmetadaten. |
| Dokument Betreff |  | Doc_subject | Dokument Betreff | Betreff aus den Dokumentmetadaten. |
| Dokumentvorlage |  | Doc_template | Dokumentvorlage | Vorlage aus den Dokumentmetadaten. |
| Dominantes Design | DominantTheme | Dominant_theme | Dominantes Design | Für Analysen berechnetes dominantes Design. |
| Doppelte Teilmenge |  | Duplicate_subset | Doppelte Teilmenge | Gruppen-ID für exakte Duplikate. |
| E-Mail-Adresse |  | Email_action |  | None, reply, Forward basierend auf der Betreffzeile einer Nachricht. |
| Bestätigung für e-Mail-Zustellung |  | Email_delivery_receipt | Bestätigung für e-Mail-Zustellung | E-Mail-Adresse, die in Internet Kopfzeilen zur Zustellungsbestätigung bereitgestellt wird |
| Importance | EmailImportance | Email_importance | Importance | Wichtigkeit der Nachricht: **0**: niedrig; **1**: normal; **2**: hoch |
| EmailLevel |  | Email_level |  | Gibt die Ebene einer Nachricht innerhalb des e-Mail-Threads an, zu dem Sie gehört; Anlagen erben den Wert der übergeordneten Nachricht. |
| E-Mail-Nachrichten-ID |  | Email_message_ID | E-Mail-Nachrichten-ID | Die Internet Nachrichten-ID aus der Nachricht. |
| EmailReadReceipt |  | Email_read_receipt |  | E-Mail-Adresse in Internet Kopfzeilen für Lesebestätigung. |
| E-Mail-Sicherheit | EmailSecurity | Email_security | E-Mail-Sicherheit | Sicherheitseinstellung der Nachricht: **0**: None; **1**: signiert; **2**: verschlüsselt; **3**: verschlüsselt und signiert. |
| E-Mail-Vertraulichkeit | EmailSensitivity | email_sensitivity | E-Mail-Vertraulichkeit | Empfindlichkeitseinstellung der Nachricht: **0**: None; **1**: persönlich; **2**: privat; **3**: CompanyConfidential. |
| E-Mail-Satz | Emailset | Email_set | E-Mail-Satz | Gruppen-ID für alle Nachrichten im gleichen e-Mail-Satz. |
| EmailThread |  | Email_thread |  | Die Position der Nachricht innerhalb des e-Mail-Satzes; besteht aus allen Knoten-IDs vom Stamm bis zur aktuellen Nachricht, Punkt getrennt. |
| Extrahierter Inhaltstyp |  | Extracted_content_type | Extrahierter Inhaltstyp | Extrahierter Inhaltstyp in Form von MIME-Typ; Beispiel: Image/JPEG. |
| ExtractedTextLength |  | Extracted_text_length |  | Anzahl der Zeichen im extrahierten Text. |
| Familien Relevanz-Ergebnis Fall 1 |  | Family_relevance_score_case_issue_1 |  | Familien Relevanz bei Ausgabe 1 von Relevanz. |
| FamilyDuplicateSet |  | Family_duplicate_set |  | Numerischer Bezeichner für Familien, die exakte Duplikate voneinander sind (derselbe Inhalt und alle gleichen Anlagen). |
| Familien-ID | FamilyID | Family_ID | Familien-ID | Familien-ID gruppiert alle Elemente; für e-Mails umfasst dies die Nachricht und alle Anlagen; für Dokumente sind dies das Dokument und alle eingebetteten Elemente. |
| Größe der Familie |  | Family_size | Größe der Familie | Anzahl der Dokumente in der Familie. |
| Datei Relevanz-Ergebnis Fall 1 |  | File_relevance_score_case_issue_1 |  | Datei Relevanz, Fall Issue 1 von Relevanz. |
| File-Klasse | Fileclass | File_class | File-Klasse | Für Inhalte aus SharePoint und OneDrive: **Document**; für Inhalte von Exchange: **e-Mail**oder **Anlage**. |
| Datei-ID | FileId | File_ID | Datei-ID | Dokumentbezeichner innerhalb der Groß-/Kleinschreibung eindeutig.|
| Dateisystem-Erstellungsdatum |  | File_system_date_created | Dateisystem-Erstellungsdatum | Erstellungsdatum aus Dateisystem (gilt nur für nicht-Office 365-Daten). |
| Dateisystem Datum geändert |  | File_system_date_modified | Dateisystem Datum geändert | Änderungsdatum vom Dateisystem (gilt nur für nicht-Office 365-Daten). |
| Dateityp | FileType |  | Dateityp | Dateityp des Elements basierend auf der Dateierweiterung. |
| Hat Anlage | HasAttachment | Email_has_attachment | Hat Anlage | Gibt an, ob die Nachricht Anlagen enthält. |
| Hat Anwalt | HasAttorney |  | Hat Anwalt | True, wenn mindestens einer der Teilnehmer in der Liste der Rechtsanwälte gefunden wird; Andernfalls ist der Wert false. |
| HasText |  | Has_text |  | Gibt an, ob das Element Text enthält, mögliche Werte sind true und false. |
| Unveränderliche ID | Unveränderliche | Immutable_ID | Unveränderliche ID | Unveränderliche ID, wie in Office 365 gespeichert. |
| Inklusivtyp | Inklusivtype | Inclusive_type | Inklusivtyp | Für Analysen berechneter inklusivtyp: **0** -not inclusive; **1** -inklusive; **2** inklusive minus; **3** -inclusive-Kopie. |
| In reply to ID |  | In_reply_to_ID | In reply to ID | In Antwort auf ID aus der Nachricht. |
| Ist repräsentativ | Isrepresentative | Is_representative | Ist repräsentativ | Ein Dokument in jedem Satz exakter Duplikate wird als Representative gekennzeichnet. |
| Elementklasse | ItemClass | Item_class | Elementklasse | Von Exchange Server bereitgestellte Elementklasse; beispielsweise **IPM. Hinweis** |
| Datum der letzten Änderung | LastModifiedDate | Doc_date_modified | Datum der letzten Änderung | Datum der letzten Änderung aus Dokumentmetadaten. |
| Lade-ID | Lade-Nr. | Load_ID | Lade-ID | Lade-ID, in der das Element in einen überprüfungssatz geladen wurde. |
| Standort | Standort | Standort | Standort | Eine Zeichenfolge, die den Speicherort angibt, von dem Dokumente bezogen wurden;<br />Nicht-O365-> importierte Daten<br />Teams – > Teams<br />Exo-> Exchange<br />SPO-> SharePoint<br />OneDrive for Business-> OneDrive |
| Standortname | LocationName | Location_name | Standortname | Zeichenfolge, die die Quelle des Elements identifiziert.  Für Exchange ist dies die SMTP-Adresse des Postfachs.  Für SharePoint und OneDrive die URL der Websitesammlung. |
| Als Vertreter gekennzeichnet | MarkAsRepresentative |  | Als Vertreter gekennzeichnet | Ein Dokument aus jeder Gruppe von exakten Duplikaten wird als Repräsentanten gekennzeichnet. |
| Gekennzeichnet als Pre-Tagged Case Issue 1 |  | Marked_as_pre_tagged_Case_issue_1 |  | Als Pre-Tagged Case Issue 1 von Relevanz gekennzeichnet. |
| Markiert als Seed Case Issue 1 |  | Marked_as_seed_Case_issue_1 |  | Als Seed Case Issue 1 (Relevanz) gekennzeichnet. |
| Enddatum der Besprechung | MeetingEndDate | Meeting_end_date | Enddatum der Besprechung | Sitzungs Enddatum für Besprechungen. |
| Start Datum der Besprechung | MeetingStartDate | Meeting_start_date | Start Datum der Besprechung | Besprechungs Startdatum für Besprechungen. |
| Nachrichtentyp | MessageKind | Message_kind | Nachrichtentyp | Der Typ der zu suchenden Nachricht.<br />Mögliche Werte: <br />contacts <br />docs <br />email <br />externaldata <br />faxes <br />im <br />journals <br />meetings <br />verläuft (gibt Elemente aus Chats, Besprechungen und anrufen in Microsoft Teams zurück) <br />notes <br />posts <br />rssfeeds <br />tasks <br />voicemail |
| Systemeigene Erweiterung | NativeExtension | Native_extension | Systemeigene Erweiterung | Systemeigene Erweiterung des Elements. |
| Systemeigener Dateiname | NativeFileName | Native_file_name | Systemeigener Dateiname | Systemeigener Dateiname des Elements. |
| NativeMD5 |  | Native_MD5 |  | MD5-Hash des Dateistreams. |
| ND/et Sort: ohne Anlagen | NdEtSortExclAttach | ND_ET_sort_excl_attach | ND/et Sort: ohne Anlagen | Verkettung von e-Mail-Sätzen und ND-Sätzen zur effizienten Sortierung zur Zeit der Überprüfungen; D wird als Präfix zu ND-Sätzen hinzugefügt und e zu e-Mail-Sätzen hinzugefügt. |
| ND/et Sort: einschließlich Attachments | NdEtSortInclAttach | ND_ET_sort_incl_attach | ND/et Sort: einschließlich Attachments | Verkettung von e-Mail-Sätzen und ND-Sätzen zur effizienten Sortierung zur Zeit der Überprüfungen; D wird als Präfix zu ND-Sätzen hinzugefügt und e zu e-Mail-Sätzen hinzugefügt. Jeder e-Mail innerhalb eines e-Mail-Satzes werden die entsprechenden Anhänge gefolgt. |
| Normalisierte Relevanz-Bewertung, Fall 1 |  | Normalized_relevance_score_case_issue_1 |  | Normalisierte Relevanz-Bewertung bei Ausgabe 1 von Relevanz. |
| O365 Autoren |  | O365_authors | O365 Autoren | Autor aus SharePoint. |
| O365 erstellt von |  | O365_created_by | O365 erstellt von | Erstellt von aus SharePoint. |
| O365-Erstellungsdatum |  | O365_date_created | O365-Erstellungsdatum | Erstellungsdatum aus SharePoint. |
| O365 Datum geändert |  | O365_date_modified | O365 Datum geändert | Datum der letzten Änderung in SharePoint. |
| O365 geändert von |  | O365_modified_by | O365 geändert von | Geändert von von SharePoint. |
| Übergeordnete ID | ParentId | Parent_ID | Übergeordnete ID | ID des übergeordneten Elements. |
| ParentNode |  | Parent_node |  | Die nächste vorhergehende e-Mail-Nachricht im e-Mail-Thread. |
| Übergeordneter Pfad | ParentPath | Parent_path | Übergeordneter Pfad | Zusammengesetzter Pfad des direkten übergeordneten Objekts des Elements. |
| Teilnehmer Domänen | ParticipantDomains | Email_participant_domains | Teilnehmer Domänen | Liste aller Domänen der Teilnehmer einer Nachricht. |
| Participants | Participants | Email_participants | Participants | Liste aller Teilnehmer einer Nachricht; Beispiel: Absender, an, CC, BCC. |
| Pivot-ID | Pivot-Achse | Pivot_ID | Pivot-ID | Die ID eines Pivots. |
| Potenziell privilegierte | PotentiallyPrivileged | Potentially_privileged | Potenziell privilegierte | True, wenn das Dokument mit dem Anwalts-und Berechtigungs Erkennungs Modell potenziell privilegiert wird |
| Verarbeitungsstatus | ProcessingStatus | Error_code | Verarbeitungsstatus | Verarbeitungsstatus, nachdem das Element einem Übersichts Satz hinzugefügt wurde. |
| Prozent Fall Ausgabe 1 lesen |  | Read_percent_Case_issue_1 |  | Lesen Sie percent Case Issue 1 von Relevanz. |
| Quantil lesen | ReadPercentile |  | Quantil lesen | Lesen Sie Perzentil für das Dokument basierend auf Relevanz. |
| Empfängeranzahl |  | Recipient_count | Empfängeranzahl | Die Anzahl der Empfänger in der Nachricht. |
| Empfängerdomänen | RecipientDomains | Email_recipient_domains | Empfängerdomänen | Liste aller Domänen von Empfängern einer Nachricht. |
| Empfänger | Empfänger | Email_recipients | Empfänger | Liste aller Empfänger einer Nachricht (an, CC, BCC). |
| Relevanz für Auslastungs Gruppen Fall 1 |  | Relevance_load_group_case_issue_1 |  | Relevanz belastungsgruppe Fall Issue 1 von Relevanz. |
| Relevanzstatus Beschreibung Case Issue 1 |  | Relevance_status_description_Case_issue_1 |  | Relevanzstatus Beschreibung Case Issue 1 from Relevance. |
| Relevanz-Tag-Fall-Problem 1 |  | Relevance_tag_case_issue_1 |  | Relevanztag Case Issue 1 von Relevanz. |
| Relevanz-Kommentar |  | Relevance_comment | Relevanz-Kommentar | Kommentarfeld aus Relevanz. |
| Relevanz-Bewertung | RelevanceScore |  | Relevanz-Bewertung | Relevanz des Dokuments anhand der Relevanz. |
| Relevance-Tag | RelevanceTag |  | Relevance-Tag | Relevanz des Dokuments anhand der Relevanz. |
| Vertreter-ID | Repräsentative-Nr. |  | Vertreter-ID | Numerischer Bezeichner der einzelnen Duplikate. |
| Absender | Absender | Email_sender | Absender | Absenderfeld für Nachrichtentypen.  Format ist **Display \<Name SmtpAddress>**. |
| Absender/Autor | SenderAuthor |  | Absender/Autor | Berechnetes Feld des Absenders oder Autors des Elements. |
| Absenderdomäne | SenderDomain | Email_sender_domain | Absenderdomäne | Die Domäne des Absenders. |
| Gesendet | Gesendet | Email_date_sent | Gesendet | Sendedatum der Nachricht. |
| Reihenfolge: inklusive zuerst | SetOrderInclusivesFirst | Set_order_inclusives_first | Set Order: Inclusive First. | Sortierfeld-e-Mail und Anhänge: Counter-chronologisch, Dokumente: Pivot zuerst dann nach Ähnlichkeits Bewertung, absteigend. |
| SimilarityPercent |  | Similarity_percent |  | Gibt an, wie ähnlich ein Dokument dem Drehpunkt des in der Nähe vorhandenen Duplikats entspricht. |
| Systemeigene Dateigröße | Größe | Native_size | Systemeigene Dateigröße | Die Anzahl der Bytes des systemeigenen Elements. |
| Betreff | Betreff | Email_subject | Betreff | Betreff der Nachricht. |
| Betreff/Titel | Betreff erstellt |  | Betreff/Titel | Berechnetes Feld des Betreffs oder Titels des Elements. |
| Tagged by Case Issue 1 |  | Tagged_by_Case_issue_1 |  | Benutzer, der dieses Dokument für Case Issue 1 in Relevanz markiert hat. |
| Tags | Tags | Tags | Tags | In einem Übersichts Satz angewendete Tags. |
| Design Liste | Themesliste | Themes_list | Design Liste | Für Analysen berechnete Design Liste. |
| Titel | Titel | Doc_title | Titel | Titel aus den Dokumentmetadaten. |
| An | An | Email_to | An | To-Feld für für Nachrichtentypen.  Format ist **Display\<Name SmtpAddress>** |
| Eindeutig in e-Mail-Satz | UniqueInEmailSet |  | Eindeutig in e-Mail-Satz | False, wenn ein Duplikat der Anlage im e-Mail-Satz vorhanden ist. |
| Wurde korrigiert | WasRemediated | Was_Remediated | Wurde korrigiert | True, wenn das Element korrigiert wurde, andernfalls false. |
| Wörter zählen | WordCount | Word_count | Wörter zählen | Die Anzahl der Wörter im Element. |
||||||

  > [!NOTE]
  > Weitere Informationen zu durchsuchbaren Feldern bei der Suche direkt für Office 365 finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](https://docs.microsoft.com/en-us/office365/securitycompliance/keyword-queries-and-search-conditions)
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
ms.openlocfilehash: 75550d48a474fc6429a780d0a03d28745e20e1f7
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835055"
---
# <a name="document-metadata-fields-in-advanced-ediscovery"></a>Dokument-Metadatenfelder in Advanced eDiscovery

Die Tabelle in diesem Artikel listet die Metadatenfelder für Dokumente in einem Übersichts Satz in einem Fall in Advanced eDiscovery auf. Die Tabelle gibt den Namen des Metadatenfelds an, ob das Feld durchsucht werden kann, wenn eine Abfrage in einem Übersichts Satz läuft, ob das Feld vorhanden ist, wenn die Datei Metadaten eines ausgewählten Dokuments in einem Übersichts Satz angezeigt werden, und ob das Feld bei Dokumenten ein erneut exportiert. 

> [!NOTE]
> Die Werte in Klammern in der Spalte **Searchable in Review Set** sind der Name der Eigenschaft, nach der Sie suchen können. Die Werte in Klammern in der Spalte **sichtbar in Datei Metadaten** sind der Name der Eigenschaft, die angezeigt wird, wenn Sie die Datei Metadaten anzeigen.

|**Feldname** </br>|**Durchsuchbar im Übersichts Satz** |**Sichtbar in Datei Metadaten** |**Exportiert** |
|:-------------------------- |:---------------------------------------- |:------------------------|:------------------|
|Case-Tags                  | Ja (Tags)                                      |                         | Ja         |
|Konformitäts Bezeichnungen          |                                                 |                         | Ja         |
|Zusammengesetzter Pfad              |                                                 |                         | Ja         |
|Container-ID               |                                                 |                         | Ja         |
|Unterhaltungsindex         |                                                 |                         | Ja         |
|Custodian                  | Ja (Depotbank)                                 |   Ja (Depotbank)       | Ja         |
|Datenquelle                | Ja (Quelle)                                    |   Ja (Arbeitslast)          | Ja         |
|Datum                       | Ja (Datum)                                      |   Ja (Datum UTC)        | Ja         |
|Deduplizierte zusammengesetzter Pfad      |                                                 |                         | Ja         |
|Deduped Verwalter         |                                                 |                         | Ja         |
|Deduplizierte Datei-IDs           |                                                 |                         | Ja         |
|Dokumentautoren                | Ja (Autor) *                                   |    Ja (Autor)         | Ja         |
|Doc-Kommentare               | Ja (Kommentare)                                  |                         | Ja         |
|Doc-Firma                |                                                 |                         | Ja         |
|Dokument Erstellungsdatum           | Ja (erstellt) *                              |    Ja (erstellte Zeit)   | Ja         |
|Dokumentdatum geändert          | Ja (lastModifiedDate) *                         |                         | Ja         |
|Doc-Schlüsselwörter               |                                                 |                         | Ja         |
|Dokument zuletzt gespeichert von          |                                                 |                         | Ja         |
|Dokument geändert von            |                                                 |                         | Ja         |
|Dokument Betreff                |                                                 |  Ja (Betreff/Titel)    | Ja         |
|Dokumentvorlage               |                                                 |                         | Ja         |
|Dokumenttitel                  | Ja (Title)                                     |  Ja (Title)            | Ja         |
|Dokumentversion                |                                                 |                         | Ja         |
|Dominantes Design             | Ja (dominantTheme)                             |  Ja (dominantes Design)   | Ja         |
|Doppelte Teilmenge           |                                                 |                         | Ja         |
|E-Mail-Aktion               |                                                 |                         | Ja         |
|E-Mail-BCC                  | Ja (BCC)                                       |                         | Ja         |
|E-Mail-CC                   | Ja (CC)                                        |                         | Ja         |
|E-Mail-Unterhaltungs-ID      |                                                 |                         | Ja         |
|E-Mail-Empfangsdatum        | Ja (empfangen)                                  |   Ja (empfangen)        | Ja         |
|Gesendetes e-Mail-Datum            | Ja (gesendet)                                      |   Ja (gesendet)            | Ja         |
|E-Mail hat Anlage       |                                                 |                         | Ja         |
|E-Mail-Wichtigkeit           |                                                 |                         | Ja         |
|E-Mail-Internetkopfzeilen     |                                                 |                         | Ja         |
|E-Mail-Ebene                |                                                 |                         | Ja         |
|E-Mail-Nachrichten-ID           |                                                 |                         | Ja         |
|E-Mail-Teilnehmer Domänen  | Ja (participantDomains)                        |                         | Ja         |
|E-Mail-Teilnehmer         | Ja (Teilnehmer)                              |                         | Ja         |
|E-Mail-Empfängerdomänen    | Ja (recipientDomains)                          |                         | Ja         |
|E-Mail-Empfänger           | Ja (Empfänger)                                |                         | Ja         |
|E-Mail-Sicherheit             |                                                 |                         | Ja         |
|E-Mail-Absender               | Ja (Absender)                                    |   Ja (Absender)          | Ja         |
|E-Mail-Absenderdomäne        | Ja (senderDomain)                              |                         | Ja         |
|E-Mail-Vertraulichkeit          |                                                 |                         | Ja         |
|E-Mail-Satz                  | Ja (emailSetId)                                |   Ja (EmailSetID)      | Ja         |
|E-Mail-Betreff              | Ja (Betreff)                                   |   Ja (Betreff/Titel)   | Ja         |
|E-Mail-Thread               |                                                 |                         | Ja         |
|E-Mail an                   | Ja (an)                                        |                         | Ja         |
|Fehlercode                 | Ja (processingStatus)                          |                         | Ja         |
|Systemeigenen Pfad exportieren         |                                                 |                         | Ja         |
|Extrahierte Text Länge      |                                                 |                         | Ja         |
|Extrahierter Textpfad        |                                                 |                         | Ja         |
|Familien-ID                  | Ja (Family-ID)                                  |   Ja (Family-ID)        | Ja         |
|Größe der Familie                |                                                 |                         | Ja         |
|File-Klasse                 | Ja (fileclass)                                 |   Ja (File-Klasse)      | Ja         |
|Datei-ID                    | Ja (Datei-Nr.)                                    |   Ja (ID)              | Ja         |
|Hat Text                   |                                                 |                         | Ja         |
|Inklusivtyp             | Ja (inklusivtype)                             |   Ja (inklusive Typ)  | Ja         |
|Eingabedatum geändert        |                                                 |                         | Ja         |
|Eingabedatei-ID              |                                                 |                         | Ja         |
|Eingabepfad                 |                                                 |                         | Ja         |
|Internetnachrichten-ID        |                                                 |                         | Ja         |
|Ist repräsentativ          | Ja (markAsRepresentative)                      |                         | Ja         |
|Elementklasse                 |                                                 |                         | Ja         |
|Lade-ID                    | Ja (Lade-Nr.)                                    |                         | Ja         |
|Standortname              |                                                 |                         | Ja         |
|Markiert als Pivot            | Ja (markAsPivot)                               |   Ja (als Pivot gekennzeichnet) | Ja         |
|Nachrichtentyp               | Ja (messageKind)                               |                         | Ja         |
|Systemeigene Erweiterung           |                                                 |                         | Ja         |
|Systemeigener Dateiname           |                                                 |    Ja (Dateiname)      | Ja         |
|Natives MD5                 |                                                 |                         | Ja         |
|Native SHA 256             |                                                 |                         | Ja         |
|Systemeigene Größe                | Ja (Größe)                                      |   Ja (NativeSize)     | Ja         |
|Systemeigener Typ                | Ja (filetype)                                  |   Ja (Dateityp)       | Ja         |
|ND et Sort exkl. Attach     |                                                 |                         | Ja         |
|ND et Sort incl. Attach     |                                                 |                         | Ja         |
|ND-Satz                     |                                                 |                         | Ja         |
|O365 Autoren               | Ja (Autor) *                                   |   Ja (Absender/Autor)   | Ja         |
|O365 erstellt von            |                                                 |                         | Ja         |
|O365-Erstellungsdatum          | Ja (erstellt) *                              |                         | Ja         |
|O365 Datum geändert         | Ja (lastModifiedDate) *                         |   Ja (Datum der letzten Änderung) | Ja      |
|O365 geändert von           |                                                 |                         | Ja         |
|Übergeordneter Knoten                |                                                 |                         | Ja         |
|Pivot-ID                   | Ja (pivotable)                                   |  Ja (pivotable)          | Ja         |
|Empfängeranzahl            |                                                 |                         | Ja         |
|Zeilennummer                 |                                                 |                         | Ja         |
|ID festlegen                     |                                                 |                         | Ja         |
|Zuerst Order inclusive festlegen |                                                 |                         | Ja         |
|Ähnlichkeit prozentual         |                                                 |                         | Ja         |
|Design Liste                | Ja (designlist)                                | Ja (Design Liste)       | Ja         |
|Word count                 | Ja (WordCount)                                 |                         | Ja         |
|Relevanz (Problem)    | Ja (relevanceScore_issueNum)                   |                         | Ja           |
|Quantil lesen (Problem)    | Ja (readPercentile_issueNum)                   |                         | Ja          |
|Relevance-Tag (Problem)      | Ja (relevanceTag_issueNum)                     |                         | Ja           |
|||||

  \*Wenn in einem Dokument eingebettete Werte vorhanden sind, priorisiert die Suche diese Werte für diese Felder. Andernfalls wird versucht, den Wert aus Office 365 anzuzeigen.
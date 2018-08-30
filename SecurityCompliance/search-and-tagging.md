---
title: Suche und Kategorien
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529531"
---
# <a name="search-and-tagging"></a>Suche und Kategorien

In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Suchen Sie die Dokumente in Ihrem Fall

Nachdem Sie Dokumente in erweiterten eDiscovery verarbeitet und optional das Modul Analyse oder der Relevanz-Modul ausgeführt werden, Sie suchen können und Verwenden von Kategorien, die Dokumente im Fall durchsuchen und Organisieren Case-spezifische Tags. Sie können Definieren von Abfragen mit dem angegebenen Bedingung Karten oder über eine KQL-ähnliche Abfragesprache in den Schlüsselwörtern Bedingung Karte. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR(n) sind die unterstützten sowie nachstehende mehrere Zeichen Platzhalterzeichen (*). Diese Eigenschaften werden in der Abfrage-Eigenschaftenname unterstützt:

- Caselabel: Tags erstellt/angewendet in der Suche und Kategorien für diesen Fall 
- Verwalter: im Fall - eingeschränkt zugewiesen Verwalter
- Datum: Datum für e-Mail gesendet, Änderungsdatum für Dokumente
- FileID: Datei mit der ID innerhalb der Groß-/Kleinschreibung
- FileType: systemeigene Erweiterung
- Fileclass: e-Mail, Dokument oder Anlage
- Senderauthor: Absender-e-Mails, Autor für Dokumente
- Größe: Größe der Datei in KB
- Betreff: Betreff für e-Mails, Titel für Dokumente
- bcc
- cc
- Teilnehmer: e-Mail-Adressen von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Links
- empfangen: Empfangsdatum
- Empfänger: e-Mail-Namen der Empfänger oder Adressen (an, cc, Bcc)
- sender
- LastModifiedDate: letzte Änderung eines Dokuments
- gesendet: Datum der eine e-Mail gesendet
- bis
- Autor: Autor einer e-Mail
- Title: Titel eines Dokuments
- Dominanttheme: dominanten Design eines Elements\*
- Themeslist: Designs, die einem Element zugeordnet sind.\*
- Readpercentile_ [Issuenum]: Lesen Quantil eines Elements für Problem [Issuenum]\*\*
- Relevancescore_ [Issuenum]: Relevanz Bewertung eines Elements für Problem [Issuenum]\*\*
- Relevancetag_ [Issuenum]: Wenn ein Element manuell für Relevanz, dessen Tag für [Issuenum] markiert wurde.\*\*

\*Nur verfügbar, wenn das Modul Designs ausgeführt wurde \* \* nur verfügbar, wenn das Modul Relevanz ausgeführt wurde
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)


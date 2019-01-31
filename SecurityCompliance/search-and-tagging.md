---
title: Suche und Kategorien
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666145"
---
# <a name="search-and-tagging"></a>Suche und Kategorien

In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta. Eine kurze Demo der Suche und Kategorien finden Sie unter das [Verwalten von Daten mit erweiterten eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) -Video.

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Suchen Sie die Dokumente in Ihrem Fall

Nachdem Sie verarbeitet Dokumente in einem erweiterten eDiscovery-Fall (und optional das Modul Analyze oder Relevanz ausgeführt), können Sie die Such- und Tagging Dokumente durchsuchen, und ordnen Sie diese dann durch Anwenden von Groß-/Kleinschreibung-spezifischen Tags (auch als Etiketten bezeichnet). Sie können eine Suchabfrage mithilfe der angegebenen Bedingung Karten definiert oder mithilfe einer KQL-ähnliche Abfragesprache in den Schlüsselwörtern Bedingung Karte. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR(n) sind die unterstützten sowie nachstehende mehrere Zeichen Platzhalterzeichen (*). 

Die folgende Tabelle enthält die Eigenschaften, die Sie für die Verwendung einer KQL-Abfrage-Schlüsselwort suchen können. Alternativ können Sie eine Bedingung (für ausgewählte Eigenschaften) auf eine Suchabfrage hinzufügen eine Bedingung-Karte finden Sie in der erweiterten eDiscovery Such-Tool verwenden.

|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**caselabel** <br/> | Der Name des Tags erstellt/angewendet, wenn ein Dokument markiert ist. <br/> |
|**Verwaltungsberechtigter** <br/> | Der Verwaltungsberechtigte mit einem Dokument verknüpften; eingeschränkt. <br/> |
|**Datum** <br/> | Datum für e-Mail gesendet. das Änderungsdatum für websitedokumente. <br/> |
|**"FileID"** <br/> | Die Datei-ID in der Groß-/Kleinschreibung. <br/> |
|**FileType** <br/> | Die systemeigene Erweiterung. <br/> |
|**fileclass** <br/> | E-Mail, Dokument oder Anlage. <br/> |
|**senderauthor** <br/> | Der Absender für e-Mail; der Autor für websitedokumente. <br/> |
|**Größe** <br/> | Die Größe der Datei in KB. <br/> |
|**Betreff** <br/> | Der Betreff der e-Mail; der Titel für die websitedokumente. <br/> |
|**bcc** <br/> | Das Feld Bcc der e-Mail. <br/> |
|**cc** <br/> | Das Feld Cc der e-Mail. <br/> |
|**Teilnehmer** <br/> | Die e-Mail-Adresse von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Links. <br/> |
|**empfangen** <br/> | Das Datum, an das eine e-Mail-Nachricht empfangen wurde. <br/> |
|**Empfänger** <br/> | Empfänger einer e-Mail, die auf an, Cc oder Bcc Felder enthalten. <br/> |
|**sender** <br/> | Der Absender der e-Mail. <br/> |
|**LastModifiedDate** <br/> | Datum der ein Dokument auf der Website wird von der letzten Änderung. <br/> |
|**gesendet** <br/> | Das Absendedatum der e-Mail. <br/> |
|**An** <br/> | Der Empfänger in das Feld an der eine e-Mail-Nachricht aufgeführt. <br/> |
|**Autor** <br/> | Der Autor des ein Dokument auf der Website. <br/> |
|**title** <br/> | Der Titel eines Dokuments für die Website. <br/> |
|**dominanttheme**\* <br/> | Das dominante Design eines Elements. <br/> |
|**themeslist**\* <br/> | Designs, die einem Element zugeordnet sind. <br/> |
|**Readpercentile_ [Issuenum]**\*\* <br/> | Das Lesen Quantil eines Elements, für das Problem durch [Issuenum] definiert. <br/> |
|**Relevancescore_ [Issuenum]**\*\* <br/> | Die Relevanz Bewertung eines Elements, für das Problem durch [Issuenum] definiert. <br/> |
|**Relevancetag_ [Tagname]**\*\* <br/> | Wenn ein Element wurde markiert wurde manuell für Relevanz, das Tag durch [Tagname] definiert. <br/> |
|||

\*Nur verfügbar, wenn das Modul Designs ausgeführt wurde.

\*\*Nur verfügbar, wenn das Modul Relevanz ausgeführt wurde.

Alternativ können Sie eine Karte Bedingung in der erweiterten eDiscovery Such-Tool verwenden, so eine Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzu. Der folgende Screenshot zeigt die Bedingungen, die einer Abfrage hinzugefügt werden können. Die **Gruppe** -Spalte gibt an, ob die Eigenschaft auf e-Mail, Dokumente oder beides (angegeben durch den Wert *Allgemeine*) angewendet wird. Diese Spalte identifiziert auch die durchsuchbaren Eigenschaften, die nach dem Ausführen des Relevanz Moduls verfügbar sind.

![Suchkriterien im erweiterten eDiscovery Such-tool](media/AeDSearchConditions.png)

Weitere Informationen zu durchsuchbare Eigenschaften finden Sie unter [Stichwortabfragen und Suchkriterien](keyword-queries-and-search-conditions.md).
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)


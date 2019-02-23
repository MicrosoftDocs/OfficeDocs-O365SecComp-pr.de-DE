---
title: Suche und Tagging
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In Advanced eDiscovery können Sie mithilfe des Such-und Markierungs Moduls die Dokumente in Ihrem Fall suchen, in der Vorschau anzeigen und organisieren. Dieses Modul befindet sich derzeit in der Beta Version.
ms.openlocfilehash: 58913a01f30b4169470592f5fc271e3ce785ac5d
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222964"
---
# <a name="search-and-tagging"></a>Suche und Tagging

In Advanced eDiscovery können Sie mithilfe des Such-und Markierungs Moduls die Dokumente in Ihrem Fall suchen, in der Vorschau anzeigen und organisieren. Dieses Modul befindet sich derzeit in der Beta Version. Eine kurze Übersicht über das Suchen und markieren finden Sie unter [Verwalten von Daten mit erweitertem eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) -Video.

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Durchsuchen der Dokumente in Ihrem Fall

Nachdem Sie Dokumente in einem erweiterten eDiscovery-Fall verarbeitet haben (und optional das Modul Analyze oder Relevance ausführen), können Sie die Suche und das Tagging verwenden, um Dokumente zu durchsuchen und Sie dann zu organisieren, indem Sie fallspezifische Tags (auch als Bezeichnungen bezeichnet) anwenden. Sie können eine Suchabfrage mithilfe der bereitgestellten Bedingungs Karten oder mithilfe einer KQL-artigen Abfragesprache in der Schlüsselwort-Bedingungs Karte definieren. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR (n) werden unterstützt, ebenso wie nachgestellte mehrstellige Platzhalterzeichen (*). 

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Sie mithilfe einer KQL-Schlüsselwortabfrage suchen können. Alternativ können Sie eine Bedingungs Karte für im Advanced eDiscovery Search Tool verwenden, um einer Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzuzufügen.

|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**caselabel** <br/> | Der Name des Tags, das erstellt/angewendet wird, wenn ein Dokument markiert wird. <br/> |
|**Custodian** <br/> | Die einem Dokument zugeordnete Depotbank; Einschränkungen vorbehalten. <br/> |
|**Datum** <br/> | Sendedatum für e-Mail; das geänderte Datum für Website Dokumente. <br/> |
|**FileID** <br/> | Die Datei-ID innerhalb der Anfrage. <br/> |
|**filetype** <br/> | Die systemeigene Dateierweiterung. <br/> |
|**fileclass** <br/> | E-Mail, Dokument oder Anlage. <br/> |
|**senderauthor** <br/> | Der Absender für e-Mail; der Autor für Website Dokumente. <br/> |
|**Größe** <br/> | Die Größe der Datei in KB. <br/> |
|**Betreff erstellt** <br/> | Betreff für e-Mail; der Titel für Website Dokumente. <br/> |
|**bcc** <br/> | Das Feld Bcc einer e-Mail. <br/> |
|**cc** <br/> | Das Feld Cc einer e-Mail. <br/> |
|**Teilnehmer** <br/> | Die e-Mail-Adresse aller Teilnehmer in einem e-Mail-Thread, einschließlich fehlender Links. <br/> |
|**empfangen** <br/> | Das Datum, an dem eine e-Mail empfangen wurde. <br/> |
|**Empfänger** <br/> | Empfänger einer e-Mail, die in den Feldern "an", "CC" oder "Bcc" enthalten sind. <br/> |
|**sender** <br/> | Der Absender einer e-Mail. <br/> |
|**LastModifiedDate** <br/> | Das Datum der letzten Änderung eines Website Dokuments. <br/> |
|**gesendet** <br/> | Das gesendete Datum einer e-Mail. <br/> |
|**An** <br/> | Der Empfänger, der im Feld "an" einer e-Mail aufgeführt wird. <br/> |
|**Autor** <br/> | Der Autor eines Website Dokuments. <br/> |
|**title** <br/> | Der Titel eines Website Dokuments. <br/> |
|**dominanttheme**\* <br/> | Das vorherrschende Design eines Elements. <br/> |
|**themesliste**\* <br/> | Designs, die einem Element zugeordnet sind. <br/> |
|**readpercentile_ [issuenum]**\*\* <br/> | Das Lese-Perzentil eines Elements für das von [issuenum] definierte Problem. <br/> |
|**relevancescore_ [issuenum]**\*\* <br/> | Die Relevanz eines Elements für das von [issuenum] definierte Problem. <br/> |
|**relevancetag_ [Tagname]**\*\* <br/> | Wenn ein Element für die Relevanz manuell markiert wurde, wird es durch [Tagname] definiert. <br/> |
|||

\*Nur verfügbar, wenn das Designmodul ausgeführt wurde.

\*\*Nur verfügbar, wenn das Relevance-Modul ausgeführt wurde.

Alternativ können Sie eine Bedingungs Karte im Tool für die erweiterte eDiscovery-Suche verwenden, um einer Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzuzufügen. Der folgende Screenshot zeigt die Bedingungen, die einer Abfrage hinzugefügt werden können. Die Spalte **Group** gibt an, ob die Eigenschaft auf e-Mails, Website Dokumente oder beides angewendet wird (angegeben durch den *allgemeinen*Wert). In dieser Spalte werden auch die durchsuchbaren Eigenschaften identifiziert, die nach der Ausführung des Relevance-Moduls verfügbar sind.

![Suchbedingungen im Tool für die erweiterte eDiscovery-Suche](media/AeDSearchConditions.png)

Weitere Informationen zu durchsuchbaren Eigenschaften finden Sie unter [Stichwortabfragen und Suchbedingungen](keyword-queries-and-search-conditions.md).
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)


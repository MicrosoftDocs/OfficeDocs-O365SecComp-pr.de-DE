---
title: Verwalten von rechtlichen Untersuchungen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: Verwenden Sie eDiscovery-Fälle im Security & Compliance Center in Office 365, um die rechtlichen Untersuchungen Ihrer Organisation zu verwalten. Wenn Sie über ein E5-Abonnement verfügen, können Sie die Falldaten mithilfe der Funktionen Textanalyse, Maschinelles Lernen und Vorhersage Codierung von Advanced eDiscovery weiter analysieren.
ms.openlocfilehash: 5bfa4719f2bb065a7064e7dc9d02778a4d032da8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252093"
---
# <a name="manage-legal-investigations-in-office-365"></a>Verwalten von rechtlichen Untersuchungen in Office 365

Organisationen haben viele Gründe, auf einen Rechtsstreit mit bestimmten Führungskräften oder anderen Mitarbeitern in Ihrer Organisation zu reagieren. Dies kann dazu führen, dass Sie weitere Untersuchungen in e-Mails, Dokumenten, Sofortnachrichtenunterhaltungen und anderen Inhaltsspeicherorten, die von Personen in ihren täglichen Arbeitsaufgaben verwendet werden, schnell finden und behalten. Sie können diese und viele andere ähnliche Aktivitäten mithilfe der eDiscovery Case Tools im Security & Compliance Center ausführen.
  
[Verwalten von rechtlichen Untersuchungen mit eDiscovery-Fällen](#manage-legal-investigations-with-ediscovery-cases)
  
[Analysieren von Falldaten mit Office 365 Advanced eDiscovery](#analyze-case-data-using-office-365-advanced-ediscovery)
  
**Möchten Sie wissen, wie Microsoft eDiscovery-Untersuchungen verwaltet?** Hier ist ein [Technisches Whitepaper](https://go.microsoft.com/fwlink/?linkid=852161) , das Sie herunterladen können, das erklärt, wie wir dieselben Office 365-Such-und-Untersuchungs Tools verwenden, um unseren internen eDiscovery-Workflow zu verwalten.
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>Verwalten von rechtlichen Untersuchungen mit eDiscovery-Fällen

mit eDiscovery-Fällen können Sie steuern, wer eDiscovery-Fälle in Ihrer Organisation erstellen, darauf zugreifen und verwalten kann. Verwenden Sie Fälle, um Mitglieder hinzuzufügen und zu steuern, welche Arten von Aktionen Sie ausführen können, halten Sie die für einen Rechtsstreit relevanten inhaltsspeicherorte fest, und verwenden Sie das Inhaltssuche-Tool, um die Speicherorte für Inhalte zu durchsuchen, die möglicherweise auf Ihren Fall reagieren. Anschließend können Sie diese Ergebnisse für weitere Untersuchungen durch externe Prüfer exportieren und herunterladen. Wenn Ihre Office 365-Organisation über ein E5-Abonnement verfügt, können Sie auch Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten.
  
- [Verwalten Sie Ihren eDiscovery-Workflow](ediscovery-cases.md) durch Erstellen und Verwenden von eDiscovery-Fällen für jede juristische Untersuchung, die Ihre Organisation ausführen muss. 
    
- [Zuweisen von eDiscovery-Berechtigungen](assign-ediscovery-permissions.md) zum Steuern, wer eDiscovery-Fälle in Ihrer Organisation erstellen und verwalten kann 
    
- [Einrichten von Konformitäts Grenzen](set-up-compliance-boundaries.md) zur Steuerung der Benutzerinhalts Speicherorte, die eDiscovery-Manager durchsuchen können 
    
- [Suchen nach Inhalten](search-for-content.md) in Ihrer Organisation 
    
- [Vorbereiten von Case-Inhalten für Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md) , damit Sie Analysen mit den leistungsfähigen analyseTools von Advanced eDiscovery wie optische Zeichenerkennung, e-Mail-Threading und Vorhersage Codierung ausführen können 
    
### <a name="use-scripts-for-advanced-scenarios"></a>Verwenden von Skripts für erweiterte Szenarien

Wie im vorherigen Abschnitt, in dem Skripts für die Inhaltssuche aufgeführt wurden, haben wir auch einige PowerShell-Skripts für Security & Compliance Center erstellt, die Sie bei der Verwaltung von eDiscovery-Fällen unterstützen.
  
- [Erstellen Sie einen eDiscovery-Aufbewahrungsbericht](create-a-report-on-holds-in-ediscovery-cases.md) mit Informationen zu allen mit eDiscovery-Fällen in Ihrer Organisation verknüpften Haltebereichen. 
    
- [Hinzufügen von Postfächern und OneDrive-Standorten](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) für eine Liste von Benutzern zu einem eDiscovery-Speicher 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a>Analysieren von Falldaten mit Office 365 Advanced eDiscovery

Office 365 Advanced eDiscovery baut auf den in den vorherigen Abschnitten beschriebenen Inhaltssuche-und eDiscovery-Funktionen auf. Nachdem Sie einen eDiscovery-Fall erstellt haben, die Aufbewahrungsorte in die Warteschleife gestellt und Daten gesammelt haben, die möglicherweise auf den Fall reagieren, können Sie die Daten mithilfe der Funktionen "Textanalyse", "Maschinelles Lernen" und "Predictive Coding capabilities of Advanced" weiter analysieren. eDiscovery. Dadurch kann Ihre Organisation Tausende von e-Mail-Nachrichten, Dokumenten und anderen Arten von Daten schnell verarbeiten, um die Elemente zu finden, die für einen bestimmten Fall wahrscheinlich relevant sind. Und wir haben Unified Case Management und Advanced eDiscovery, damit Sie den gleichen Fall innerhalb des Security & Compliance Center nahtlos verwalten können.
  
> [!NOTE]
> Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden. Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden. Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz. 
  
### <a name="get-started"></a>Erste Schritte

Am schnellsten können Sie mit Advanced eDiscovery beginnen, einen Fall zu erstellen und die Suchergebnisse im Security & Compliance Center vorzubereiten, die Ergebnisse in Advanced eDiscovery zu laden und dann die Express Analyse auszuführen, um die Falldaten zu analysieren und dann die Ergebnisse zu exportieren. für externe Überprüfungen.
  
- [Schnellübersicht](quick-setup-for-advanced-ediscovery.md) über den erweiterten eDiscovery-Workflow 
    
- [Einrichten von Benutzern und Fällen](set-up-users-and-cases-in-advanced-ediscovery.md) für Advanced eDiscovery durch Erstellen eines Falls, Zuweisen von eDiscovery-Berechtigungen und Hinzufügen von Fall Mitgliedern, alle mithilfe des Security _AMP_ Compliance Center 
    
- [Vorbereiten und Laden von Such Daten](prepare-data-for-advanced-ediscovery.md) in den Fall in Advanced eDiscovery 
    
- [Laden von nicht-Office 365-Daten](import-non-office-365-data-into-advanced-ediscovery.md) in einen Fall zur Analyse in Advanced eDiscovery 
    
- [Verwenden Sie die Express Analyse](use-express-analysis-in-advanced-ediscovery.md) , um die Daten in einem Fall schnell zu analysieren und dann einfach die Ergebnisse zu exportieren. 
    
### <a name="analyze-data"></a>Analysieren von Daten

Nachdem die Such Daten in Advanced eDiscovery in den Fall geladen wurden, verwenden Sie das Analysemodul, um mit der Analyse zu beginnen. Der erste Teil des Analyseprozesses besteht darin, Dateien in Gruppen von eindeutigen Dateien, Duplikaten und beinahe-Duplikaten zu organisieren (auch als Dokument Ähnlichkeit bekannt). Dann organisieren Sie die Daten erneut in hierarchisch strukturierten Gruppen von e-Mail-Threads und-Designs und legen optional Textfilter ignorieren fest, um bestimmten Text aus der Analyse auszuschließen. Anschließend führen Sie die Analyse aus und zeigen die Ergebnisse an.
  
- Informationen zur [Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md) bei der Vorbereitung der Analyse von Daten in Advanced eDiscovery 
    
- [Richten Sie die Optionen](set-analyze-options-in-advanced-ediscovery.md) für Near-Duplicates, Designs und e-Mail-Threading ein, und führen Sie dann das Analysemodul aus. 
    
- [Einrichten von Text filtern ignorieren](set-ignore-text-in-advanced-ediscovery.md) , damit Text und Textzeichenfolgen nicht analysiert werden können Diese Filter ignorieren auch Text, wenn Sie die Relevanz-Analyse ausführen. 
    
- [Anzeigen der Ergebnisse](view-analyze-results-in-advanced-ediscovery.md) des Analyseprozesses 
    
- [Konfigurieren erweiterter Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md) für den Analyseprozess 
    
### <a name="set-up-relevance-training"></a>Einrichten der Relevanzschulung

PreDictive Coding (called Relevance) in Advanced eDiscovery ermöglicht Ihnen, das System auf das zu trainieren, wonach Sie suchen, indem Sie Entscheidungen treffen (um zu entscheiden, ob etwas relevant ist).
  
- Informationen [zum Einrichten von Relevanz-Schulungen](manage-relevance-setup-in-advanced-ediscovery.md) , zum Markieren von Dateien, die für einen Fall relevant sind, und zum Definieren von Fall Problemen 
    
- [Definieren von Fall Problemen](define-issues-and-assign-users.md) und Zuweisen jedes Problems zu einem Benutzer, der die Dateien ausbildet 
    
- [Hinzufügen von importierten Dateien zu aktueller oder neuer Auslastung](set-up-loads-to-add-imported-files.md) , die der Relevanz-Schulung hinzugefügt wird; eine Auslastung ist ein neuer Batch von Dateien, die zu einem Fall hinzugefügt werden und dann für Relevanz-Schulung verwendet werden. 
    
- [Definieren Sie hervorgehobene Schlüsselwörter](define-highlighted-keywords-and-advanced-options.md) , die der Relevanz-Schulung hinzugefügt werden können. auf diese Weise können Sie Dateien, die für einen Fall relevant sind, besser identifizieren. 
    
### <a name="run-the-relevance-module"></a>Ausführen des Relevance-Moduls

Nachdem Sie die Schulung eingerichtet haben, können Sie das Relevanz-Modul ausführen und die Effektivität der Schulungs Einstellungen bewerten, die zu einer Relevanz-Rangfolge führen, mit der Sie entscheiden können, ob Sie zusätzliche Schulungen durchführen müssen, oder ob Sie bereit sind, mit dem Tagging von Dateien zu beginnen. relevant für Ihren Fall.
  
- [Erfahren Sie mehr über den relevanzprozess](use-relevance-in-advanced-ediscovery.md) und den iterativen Prozess der Bewertung, des Tagging, der Nachverfolgung und des Umschulungs Vorgangs basierend auf einem Beispielsatz von Dateien 
    
- [Erfahren Sie mehr über die Bewertung](assessment-in-relevance-in-advanced-ediscovery.md) , bei der ein Experte, der mit dem Fall vertraut ist, eine Reihe von Fall Dateien prüft und die effektivItät der Relevanz-Schulung bestimmt. 
    
- [Bewerten Sie die Fall Dateien](tagging-and-assessment-in-advanced-ediscovery.md) , um die Effektivität (so genannte *Reichhaltigkeit* ) von Trainingseinstellungen zu berechnen, und markieren Sie dann Dateien als relevant oder nicht relevant für Ihren Fall. auf diese Weise können Sie ermitteln, ob die aktuelle Schulung ausreicht oder ob Sie die Trainingseinstellungen anpassen sollten. 
    
- Führen Sie nach Abschluss [der Bewertung die Relevanz-Schulung aus](tagging-and-relevance-training-in-advanced-ediscovery.md) , und markieren Sie dann erneut Dateien als relevant oder nicht relevant für die Probleme, die Sie für den Fall definiert haben. 
    
- [Verfolgen Sie den Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md) Prozess, um festzustellen, ob die Relevanz-Schulung Ihr Bewertungs Ziel erreicht hat (als *stabiler Ausbildungsstatus* bezeichnet) oder ob mehr Schulungen erforderlich sind. Sie können auch die Relevanz-Ergebnisse für jedes Fall Problem anzeigen 
    
- [Entscheidungen basierend auf der Relevanz-Analyse treffen](decision-based-on-the-results-in-advanced-ediscovery.md) , um die Größe der sich ergebenden Fall Dateien zu bestimmen, die zur Überprüfung exportiert werden können 
    
- [Testen der Qualität der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md) , um die während des Relevanz-Vorgangs getroffenen Entscheidungen zu überprüfen 
    
### <a name="export-results"></a>Ergebnisse exportieren

Der letzte Schritt bei der Analyse von Falldaten in Advanced eDiscovery ist das Exportieren der Ergebnisse der Analyse für die externe Überprüfung.
  
- [Informationen zum Exportieren von Falldaten](export-case-data-in-advanced-ediscovery.md)
    
- [Exportieren von Falldaten](export-results-in-advanced-ediscovery.md)
    
- [Anzeigen des Batchverlaufs und Exportieren vergangener Ergebnisse](view-batch-history-and-export-past-results.md)
    
- [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a>Weitere Erweiterte eDiscovery-Tools

Advanced eDiscovery bietet zusätzliche Tools und Funktionen, die über die Analyse von Falldaten, die Relevanz-Analyse und den Export von Daten hinausgehen.
  
- [Ausführen erweiterter eDiscovery-Berichte](run-reports-in-advanced-ediscovery.md)
    
- [Definieren von Groß-/Kleinschreibung und Mandanten Einstellungen](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [Erweiterte eDiscovery-Dienstprogramme](use-advanced-ediscovery-utilities.md)

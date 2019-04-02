---
title: Übersicht über Daten Untersuchungen in Microsoft 365
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
description: In diesem Artikel wird das neue Tool für Daten Untersuchungen (Preview) in Microsoft 365 beschrieben.
ms.openlocfilehash: 11ba4d0870461695d327577396ccd535ac4340e1
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030157"
---
# <a name="overview-of-data-investigations-preview-in-microsoft-365"></a>Übersicht über Daten Untersuchungen in Microsoft 365

Ein Datenüberlauf tritt auf, wenn ein Dokument mit vertraulichen, vertraulichen oder böswilligen Inhalten in einer nicht vertrauenswürdigen Umgebung veröffentlicht wird. Wenn ein Datenüberlauf erkannt wird, ist es wichtig, schnell die Umgebung zu enthalten, die Größe und die Speicherorte des Ausfalls zu ermitteln, die Benutzeraktivitäten zu untersuchen und dann die verschütteten Daten aus dem Dienst zu löschen. Mit dem neuen Tool für Daten Untersuchungen (Preview) können Sie nach vertraulichen, böswilligen oder verlegten Daten in Office 365 suchen, untersuchen, was passiert ist, und die entsprechenden Maßnahmen ergreifen, um das Verschütten zu beheben.  

In diesem Artikel wird beschrieben, wie Sie mithilfe der Funktionen im Tool neue Daten Untersuchungen (Vorschau) ein Szenario für Daten verschütten behandeln.

## <a name="data-investigations-preview-workflow"></a>Daten unterSuchungen (Vorschau)-Workflow 

In den folgenden Abschnitten werden die einzelnen Schritte im integrierten Workflow in Daten Untersuchungen (Preview) beschrieben. Der folgende Screenshot zeigt die Registerkarte " **Start** " einer Untersuchung mit dem Namen " *High Risk: Finance Documents Leak*". 

![Workflow im Daten Ermittlungs Tool](../media/DataInvestigationsWorkflow.png)

## <a name="search-for-sensitive-malicious-or-misplaced-data"></a>Suchen nach vertraulichen, böswilligen oder verlegten Daten

Verwenden Sie die Registerkarte **Durchsuchen** , um Suchvorgänge zu erstellen, um die Office 365 für Daten zu suchen, die Sie korrigieren möchten. Sie können abfragebasierte suchen erstellen und ausführen, um eine festgelegte e-Mail-Nachricht und Dokumente zu identifizieren, die verschüttete Daten enthalten können, und diese dann als zu überprüfende und zu analysierende Beweise sammeln. Darüber hinaus können Sie das Such Tool verwenden, um eine Vorschau der Beispiel Dokumente und Suchstatistiken anzuzeigen, die Ihnen helfen, die Suchergebnisse zu verfeinern und zu verbessern. Wenn Sie festgestellt haben, dass die Suchergebnisse alle für die Untersuchung relevanten Daten enthalten, fügen Sie die Suchergebnisse dem nachweissatz hinzu, der zur weiteren Überprüfung, zur Folgenabschätzung und ggf. zur Durchführung von Korrekturmaßnahmen erforderlich ist. Weitere Informationen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md).

## <a name="review-and-investigate-evidence"></a>Überprüfen und untersuchen von beweisen

Verwenden Sie die Registerkarte **Evidence** , um die Daten zu untersuchen, die Sie im Live-Dienst gesammelt haben, in diesem fall Office 365. Die Daten im Evidence Set sind eine Momentaufnahme der Suchergebnisse, die Sie gesammelt haben. Wenn Sie Suchergebnisse als Nachweis hinzufügen, wird ein Prozess ausgelöst, um Dateien, Metadaten und Text zu extrahieren. Wenn dieser Prozess abgeschlossen ist, erstellt das Daten Ermittlungs Tool einen neuen Index aller Daten und fügt ihn einem Evidence-Satz hinzu. Für zeitkritische Untersuchungen können Sie dadurch schnell die Umgebung enthalten, indem Sie Daten löschen, die sich in den ursprünglichen Inhaltsspeicherorten (im Live-Dienst) befinden, während Sie den Nachweis untersuchen, den Sie in einer isolierten Umgebung gesammelt haben. Nachdem Sie Beweise gesammelt haben, können Sie zusätzliche Abfragen ausführen, um die Daten nach Zeitspanne, Dateitypen, Datenbesitzern und anderen Arten von Bedingungen einzugrenzen. Beispielsweise können Sie mithilfe der Bedingungen für den Autor, den Absender und den Empfänger schnell erkennen, welche Personen am datenspill beteiligt waren, und ob eine der verschütteten Daten für Benutzer außerhalb Ihrer Organisation freigegeben wurde.

Sie können auch erweiterte Analysen zu den gesammelten beweisen ausführen. Auf diese Weise können Sie allgemeine Designs bereitstellen und Nachweise durch e-Mail-Threads, exakte Duplikate und beinahe-Duplikate organisieren, um die Untersuchung zu erleichtern. Sie können Dokumente in der extrahierten Textansicht oder im systemeigenen Dateiformat überprüfen und Sie mit Untersuchungsergebnissen versehen. Weitere Informationen finden Sie unter:

  - [Über Prüfdaten in Evidence](review-data-in-evidence.md)

  - [Führen Sie Analysen aus, um schneller zu untersuchen](run-analytics-to-investigate-faster.md)


## <a name="managing-people-of-interest"></a>Verwalten von Personen mit Interesse

Verwenden Sie die Registerkarte **Personen von Interesse** , um die Personen hinzuzufügen und zu verwalten, die Sie während der Untersuchung des nach Weisens als Interessen Personen identifiziert haben. Wenn Sie Personen mit Interesse hinzufügen, werden Ihre Datenquellen, wie das Postfach und das OneDrive-Konto, identifiziert und zugeordnet. Dann können Sie zusätzliche Suchvorgänge durchsuchen, indem Sie nur die inhaltsspeicherorte dieser Personen. Wenn der Bereich von Personen von Interesse ist, sind die Suchvorgänge effizienter und präziser, da das Tool alle nicht indizierten Daten wie Bilder oder nicht unterstützte Dateitypen erneut verarbeitet. Auf der Registerkarte **People of Interest** können Sie auch die Überwachungsprotokoll Aktivität dieser Personen anzeigen und Durchsuchen, um die Untersuchung weiter zu unterstützen. Sie können während der Untersuchung weitere Personen hinzufügen. Weitere Informationen finden Sie unter [Verwalten von Personen von Interesse eine Untersuchung](manage-people-of-interest.md).

## <a name="indexing-the-data-of-people-of-interest"></a>Indizieren der Daten von interessierten Personen

Durch das Hinzufügen einer Person, die für eine Untersuchung von Interesse ist, werden alle teilweise indizierten Elemente aus den Datenquellen der Person neu indiziert. Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet. Die erweiterte Indizierung verarbeitet Daten wie Bilder und nicht unterstützte Dateitypen erneut, damit diese Daten vollständig auffindbar sind, wenn Sie Suchvorgänge ausführen, um Daten für eine Untersuchung zu erfassen. Verwenden Sie die Registerkarte **Verarbeitung** , um den Status der erweiterten Indizierung zu überwachen und alle Verarbeitungsfehler zu beheben, die mit einem Prozess namens *Fehlerbehebung*auftreten können. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten für eine Untersuchung](error-remediation.md).

## <a name="exporting-data"></a>Exportieren von Daten

Wenn Sie Daten exportieren möchten, verwenden Sie die **** Registerkarte Exporte, um einen Exportauftrag zu verwalten und Daten aus dem nachweissatz herunterzuladen. Wenn Sie Nachweise exportieren, werden die Daten an einen Azure-Speicherort hochgeladen und können dann auf einen lokalen Computer heruntergeladen werden. Auf der **** Registerkarte Exports können Sie die Azure-speicherORTS-URL und den Speicher Bewertungsschlüssel abrufen, die beide zum Herunterladen der exportierten Daten erforderlich sind. Weitere Informationen finden Sie unter [Exportieren von Daten aus einer Untersuchung](export-data.md).

## <a name="managing-jobs"></a>Verwalten der Aufträge

Auf der Registerkarte **Aufträge** können Sie die lang andauernden Prozesse für Aufgaben im Zusammenhang mit der Untersuchung überwachen. Hierzu gehören Aufträge zum Ausführen von Suchvorgängen, zum Hinzufügen von Daten zu einem Evidence-Set, zum erneuten Indizieren von Daten und zum Exportieren von nachweisen. Sie können beispielsweise eine neue Suche auf der Registerkarte **Suchvorgänge** erstellen, die eine Vielzahl von Datenquellen enthält. Der Status dieses Suchvorgangs wird auf der Registerkarte **Aufträge** angezeigt. Weitere Informationen finden Sie unter [Verwalten von Aufträgen in einer Datenermittlung](manage-jobs.md).

## <a name="configuring-investigation-settings"></a>Konfigurieren von Untersuchungseinstellungen

Auf der Registerkarte **Einstellungen** können Sie die Einstellungen für die Untersuchung konfigurieren. Dazu gehört das Hinzufügen von Mitgliedern zu einer Untersuchung, schließen oder Löschen einer Untersuchung und Konfigurieren des Such-und Analyse Verhaltens. Weitere Informationen finden Sie unter [Configure Settings in Data Investigations (Preview)](configure-settings-datainvestigations.md).

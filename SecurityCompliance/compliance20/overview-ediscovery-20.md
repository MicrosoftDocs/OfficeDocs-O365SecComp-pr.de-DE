---
title: Übersicht über Advanced eDiscovery (Preview) in Microsoft 365
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
description: In diesem Artikel wird die neue Version von Advanced eDiscovery (Preview) in Microsoft 365 beschrieben.
ms.openlocfilehash: 2296f4ee1867cacc90eada9e5f12888a8ea0d242
ms.sourcegitcommit: 13c601ea11ce6a3c71036fdafda059061c6998d0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2019
ms.locfileid: "30313151"
---
# <a name="overview-of-advanced-ediscovery-preview-in-microsoft-365"></a>Übersicht über Advanced eDiscovery (Preview) in Microsoft 365

Microsoft hat soeben eine Vorschauversion des aktualisierten erweiterten eDiscovery-Tools veröffentlicht, die auf den vorhandenen eDiscovery-Funktionen in Office 365 basiert. Diese Preview-Version mit dem Namen *Advanced eDiscovery (Preview)* bietet einen End-to-End-Workflow zum beibehalten, erfassen, überprüfen, analysieren und Exportieren von Inhalten, die auf interne und externe Untersuchungen Ihrer Organisation reagieren. 

## <a name="alignment-with-edrm"></a>Ausrichtung mit EDRM

Der integrierte Workflow von Advanced eDiscovery (Preview) richtet sich nach dem eDiscovery-Prozess, der vom Electronic Discovery Reference Model (EDRM) beschrieben wird. 

![Das elektronische Discovery-Referenzmodell (EDRM)](../media/EDRMv1.png)

(Bildquelle mit freundlicher Genehmigung von edrm.net. Das Quellbild wurde unter Creative Commons Attribution 3,0 unportierte Lizenz zur Verfügung gestellt.

Auf hoher Ebene unterstützt die erweiterte eDiscovery (Preview) den EDRM-Workflow:

- **Identification** -nachdem Sie potenzielle Personen identifiziert haben, die für eine Untersuchung von Interesse sind, können Sie diese als Verwalter hinzufügen (auch als *Datenverwalter*bezeichnet, da Sie möglicherweise über Informationen verfügen, die für die Untersuchung relevant sind) für eine erweiterte eDiscovery (Preview)-Fall. Nachdem Benutzer als Verwalter hinzugefügt wurden, ist es einfach, Depot Dokumente aufzubewahren, zu sammeln und zu überarbeiten.

- **Konservierung** – um Daten zu erhalten und zu schützen, die für eine Untersuchung relevant sind, können Sie mit Advanced EDiscovery (Preview) die Datenquellen, die den depotbanks zugeordnet sind, in einem Fall legal halten. Sie können auch keine Daten im Gewahrsam halten. Darüber hinaus verfügt Advanced eDiscovery (Preview) über einen integrierten Kommunikations-Workflow, mit dem Sie Benachrichtigungen an Verwalter übermitteln und Ihre Bestätigungen nachverfolgen können.

- **Sammlung** – nachdem Sie die für die Untersuchung relevanten Datenquellen identifiziert (und beibehalten haben), können Sie das integrierte Such Tool in Advanced EDiscovery (Preview) verwenden, um Livedaten aus den Datenquellen für den Freiheitsentzug (und ohne Freiheitsentzug) zu suchen und zu sammeln. Datenquellen, sofern zutreffend), die für den Fall relevant sein können.

- **Verarbeitung** – nachdem Sie alle für den Fall relevanten Daten erfasst haben, wird der nächste Schritt zur weiteren Überprüfung und Analyse verarbeitet. In Advanced eDiscovery (Preview) bedeutet dies, dass die in der Sammlungsphase identifizierten in-Place-Daten in einen Azure-Speicherort kopiert werden (als *Arbeitssatz*bezeichnet), der eine statische Ansicht der Falldaten bereitstellt. 
 
- **Review** -nachdem Daten einer Arbeitsmappe hinzugefügt wurden, können Sie bestimmte Dokumente anzeigen und zusätzliche Abfragen ausführen, um die Daten auf das zu reduzieren, was für den Fall am relevantesten ist. Darüber hinaus können Sie bestimmte Dokumente mit Anmerkungen versehen und markieren.
 
- **Analysis** -Advanced EDiscovery (Preview) bietet integrierte Analysetools, mit denen Sie Daten aus dem Arbeitssatz, den Sie bestimmen, nicht relevant für die Untersuchung sind. Zusätzlich zur Reduzierung des Volumens relevanter Daten hilft Ihnen Advance eDiscovery (Preview) auch, die Kosten für rechtliche Überprüfungen zu speichern, indem Sie Inhalte organisieren, um den Übersichts Prozess zu vereinfachen und effizienter zu gestalten.

- **Produktion** und **Präsentation** – Wenn Sie bereit sind, können Sie Dokumente aus einem Arbeitssatz zur rechtlichen Überprüfungen exportieren. Sie können Dokumente im eigenen Format oder in einem EDRM Format exportieren, damit Sie in Übersichts Anwendungen von Drittanbietern importiert werden können.

## <a name="advanced-ediscovery-preview-workflow"></a>Advanced eDiscovery (Preview)-Workflow

In den folgenden Abschnitten werden die einzelnen Schritte im integrierten Workflow in Advanced eDiscovery (Preview) beschrieben. Der folgende Screenshot zeigt die Registerkarte **Start** eines Falls namens *Product Liability 2019002*. Hinweis die Workflow-Registerkarten am oberen Rand der Seite werden so sequenziert, dass Sie am EDRM-Prozess ausgerichtet werden. 

Weitere Informationen zum End-to-End-Workflow in Advanced eDiscovery (Preview) finden Sie in diesem [Microsoft-Mechanik-Video](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Registerkarten in Advanced eDiscovery (Preview) folgen dem EDRM-Workflow](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Verwalten von Verwaltungsberechtigten

Verwenden Sie die Registerkarte **Hüter** , um die Personen hinzuzufügen und zu verwalten, die Sie im Fall als Personen von Interesse identifiziert haben. Wenn Sie Verwalter hinzufügen, können Sie schnell Depot bezogene Aktionen durchführen, wie beispielsweise die Aufbewahrungszeit für Depotbank-Datenquellen wie das Postfach und das OneDrive-Konto, die Kommunikation mit den Bewahrern und das Durchsuchen von Depotdaten Quellen zum Sammeln von Inhalten. , der für den Fall relevant ist. Wenn der Fall fortgeschritten ist, können Sie ganz einfach neue Verwalter hinzufügen oder Verwalter aus dem Fall freigeben. Weitere Informationen finden Sie unter [Arbeiten mit Verwaltern in Advanced eDiscovery (Preview)](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Verwalten von Benachrichtigungen über zugelassene Aufbewahrungszeiträume

Verwenden Sie **** die Registerkarte Kommunikationen, um den Prozess der Kommunikation mit den Verwaltern in dem Fall zu verwalten. In einem gesetzlichen Aufbewahrungs Vermerk werden Verwalter angewiesen, alle Inhalte, die für den Fall relevant sein können, aufzubewahren. Juristische Teams müssen in der Lage sein, diese Nachrichten zu verfolgen, die von Verwaltern empfangen, gelesen und anerkannt wurden. Der Kommunikations Workflow in Advanced eDiscovery (Preview) ermöglicht Ihnen das Erstellen und Senden von anfänglichen Benachrichtigungen, Erinnerungen, Freigabe Benachrichtigungen und Eskalationen, wenn Verwalter eine Hold-Benachrichtigung nicht bestätigen. Weitere Informationen finden Sie unter [Arbeiten mit Kommunikation in Advanced eDiscovery (Preview)](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Verwalten der Inhalts Aufbewahrung

Wenn Sie einem Fall einen Verwalter hinzufügen, haben Sie die Möglichkeit, Depotdaten aufzubewahren. Verwenden Sie die Registerkarte halte **Status** , um den beim Hinzufügen von Bewahrern erstellten Speicher zu verwalten und zusätzliche gesetzliche Aufbewahrungspflichten zu verwalten, die mit dem Fall verbunden sind (Sie können beispielsweise nicht-Datenquellen für den Freiheitsentzug identifizieren und einhalten). Sie können auch alle Haltestatus in der Groß-/Kleinschreibung bearbeiten und Sie als abfragebasierte Aufbewahrungsdauer festlegen, sodass nur der Inhalt, der mit der Abfrage übereinstimmt, gehalten wird. Sie können beispielsweise einen Datumsbereich zur Aufbewahrung hinzufügen, sodass nur Inhalte, die innerhalb eines bestimmten Datums erstellt wurden, beibehalten werden. Sie können auch Statistiken zu Inhalten abrufen, die in der Warteschleife enthalten sind, den Haltebereich entfernen, nachdem er für den Fall nicht mehr relevant ist, oder ihn löschen. Weitere Informationen finden Sie unter [Manage Holds in Advanced eDiscovery (Preview)](managing-holds.md).

## <a name="indexing-custodian-data"></a>Indizierung von Depotdaten

Wenn Sie einen Depot und die dazugehörigen Datenquellen zu einem Fall hinzufügen, wird jedes teilweise indizierte Element aus einer Depotbank-Datenquelle erneut indiziert (durch einen Prozess namens *Advanced Indexing*). Dadurch können Freiheitsentzug-Inhalte wie Bilder, nicht unterstützte Dateitypen und andere potenziell nicht indizierte Inhalte vollständig durchsuchbar werden, wenn Sie Suchvorgänge ausführen, um Daten für den Fall zu erfassen. Verwenden Sie die Registerkarte **Verarbeitung** , um den Status der erweiterten Indizierung zu überwachen und Verarbeitungsfehler zu beheben (mit einem Prozess namens *Fehler*Korrektur). Weitere Informationen finden Sie unter [Beheben von Verarbeitungsfehlern in Advanced eDiscovery (Preview)](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Erfassen von Falldaten

Verwenden Sie die Registerkarte **Suchvorgänge** , um Suchvorgänge durchzuführen, um die in-Place-und nicht-Pfleger-Datenquellen in Office 365 nach für den Fall relevanten Inhalten zu durchsuchen. Sie können abfragebasierte Suchvorgänge (mithilfe von Schlüsselwörtern und Bedingungen) erstellen und ausführen, um eine Reihe von e-Mail-Nachrichten und Dokumenten zu identifizieren, die für den Fall relevant sind und die Sie in den folgenden Schritten im eDiscovery-Workflow weiter überprüfen und analysieren möchten. Sie können eine oder mehrere Suchvorgänge erstellen, die mit der Anfrage verknüpft sind. Darüber hinaus können Sie das Such Tool verwenden, um eine Vorschau der Beispiel Dokumente und Suchstatistiken anzuzeigen, mit denen Sie die Suchergebnisse verfeinern und verbessern können. Wenn Sie festgestellt haben, dass die Suchergebnisse alle für den Fall relevanten Daten enthalten, fügen Sie die Suchergebnisse einem Workingset zur weiteren Überprüfung, Analyse und gegebenenfalls zum Culling hinzu. Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall in Advanced eDiscovery (Preview)](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>ÜberPrüfen und Analysieren von Falldaten

Verwenden Sie die Registerkarte **Working Sets** , um die Inhalte zu überprüfen und zu analysieren, die Sie vom Live-System gesammelt und einem Arbeitssatz hinzugefügt haben. Bei ** einem Workingset handelt es sich um eine statische Sammlung dieser Daten (d. h. eine Offlinekopie von Daten) von freiheitsentziehenden Daten (und ggf. Daten ohne Freiheitsentzug), die Sie in der vorherigen Phase des eDiscovery-Workflows gesammelt haben. Wenn Sie Suchergebnisse zu einem Arbeitssatz hinzufügen, wird ein Prozess ausgelöst, der Dateien aus Containern extrahiert, Metadaten extrahiert und Text extrahiert. Wenn dieser Prozess abgeschlossen ist, erstellt das System einen neuen Index aller Daten, die von Depotbanken gesammelt und dem Arbeitssatz hinzugefügt wurden. Nachdem die Daten der Arbeitsmappe hinzugefügt wurden, können Sie zusätzliche Abfragen ausführen, um die Falldaten einzuschränken, Daten als Text oder im systemeigenen Dateiformat anzuzeigen und Dokumente im Arbeitssatz mit Anmerkungen versehen, redact und zu markieren. Darüber hinaus können Sie erweiterte Analysen wie Dokument Duplizierung, e-Mail-Threading und Designs durchführen. Nachdem Sie die Daten nur auf das, was für den Fall relevant ist, abgeschlachtet haben, können Sie Dokumente direkt herunterladen oder zusammen mit Datei Metadaten, Anmerkungen und beliebigen Tags exportieren. Weitere Informationen finden Sie unter:

  - [Überprüfen von Falldaten in Advanced eDiscovery (Preview)](reviewing-data-in-working-set.md)
  - [Analysieren von Daten in einem Arbeitssatz in Advanced eDiscovery (Preview)](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportieren von Daten zur Überarbeitung und Präsentation

Nachdem Sie die Daten aus einem Arbeitssatz exportiert haben, verwenden **** Sie die Registerkarte Exporte, um einen Exportauftrag zu verwalten und Daten aus einem Arbeitssatz herunterzuladen. Wenn Sie eine Arbeitsmappe exportieren, werden die Daten an einen Azure-Speicherort hochgeladen und können dann auf einen lokalen Computer heruntergeladen werden. Sie können den Speicherort und den Speicher Bewertungsschlüssel abrufen, der zum Herunterladen der exportierten Daten auf der Registerkarte **Exports** erforderlich ist. Weitere Informationen finden Sie unter [Exportieren von Falldaten in Advanced eDiscovery (Preview)](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Verwalten der Aufträge

Auf der Registerkarte **Aufträge** können Sie lang andauernde Prozesse für von Ihnen initiierte fallbezogene Aufgaben überwachen. Beispiele für Aufträge sind die im Zusammenhang mit Re-Indizierung, suchen und Exporte. Sie können beispielsweise eine neue Suche auf der Registerkarte **Suchvorgänge** erstellen, die eine Vielzahl von Datenquellen enthält. Der Status dieses Suchvorgangs wird auf der Registerkarte **Aufträge** angezeigt. Weitere Informationen finden Sie unter [Manage Jobs in Advanced eDiscovery (Preview)](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Konfigurieren von Falleinstellungen

Auf der Registerkarte **Einstellungen** können Sie die Groß-/Kleinschreibung konfigurieren. Dazu gehört das Hinzufügen von Mitgliedern zu einem Fall, schließen oder Löschen eines Falls und Konfigurieren des Such-und Analyse Verhaltens. Weitere Informationen finden Sie unter [Konfigurieren von Fall Einstellungen in Advanced eDiscovery (Preview)](configuring-case-settings-ediscovery20.md).

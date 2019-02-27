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
ms.openlocfilehash: e2d89c2b8499c8818bececc4414182a6db689fb6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297018"
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

- **Verarbeitung** – nachdem Sie alle für den Fall relevanten Daten erfasst haben, wird der nächste Schritt zur weiteren Überprüfung und Analyse verarbeitet. In Advanced eDiscovery (Preview) bedeutet dies, dass die in der Sammlungsphase identifizierten in-Place-Daten in den Azure-Speicher Speicherort (als *Arbeitsgruppe*bezeichnet) kopiert werden, sodass Sie eine statische Ansicht der Falldaten erhalten. 
 
- **Review** -nachdem einer Arbeitsmappe Daten hinzugefügt wurden, können Sie bestimmte Dokumente anzeigen und zusätzliche Abfragen ausführen, um  
 
- **Analysis** -Advanced EDiscovery (Preview) bietet integrierte Analysetools, mit denen Sie Daten aus dem von Ihnen festgelegten Arbeitssatz ausmerzen können, der für die Untersuchung nicht relevant ist. Zusätzlich zur Reduzierung des Volumens relevanter Daten hilft Ihnen Advance eDiscovery (Preview) auch, die Kosten für rechtliche Überprüfungen zu speichern, indem Sie Inhalte organisieren, um den Übersichts Prozess zu vereinfachen und effizienter zu gestalten.

- **Produktion** und **Präsentation** – Wenn Sie bereit sind, können Sie Dokumente aus einem Arbeitssatz zur rechtlichen Überprüfungen exportieren. Sie können Dokumente im eigenen Format oder in einem EDRM Format exportieren, damit Sie in Übersichts Anwendungen von Drittanbietern importiert werden können.

## <a name="advanced-ediscovery-preview-workflow"></a>Advanced eDiscovery (Preview)-Workflow

In den folgenden Abschnitten werden die einzelnen Schritte im integrierten Workflow in Advanced eDiscovery (Preview) beschrieben. Der folgende Screenshot zeigt die Registerkarte **Start** eines Falls namens *Product Liability 2019002*. Hinweis die Workflow-Registerkarten am oberen Rand der Seite werden so sequenziert, dass Sie am EDRM-Prozess ausgerichtet werden. 

Weitere Informationen zum End-to-End-Workflow in Advanced eDiscovery (Preview) finden Sie in diesem [Microsoft-Mechanik-Video](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Registerkarten in Advanced eDiscovery (Preview) folgen dem EDRM-Workflow](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Verwalten von Verwaltungsberechtigten

Verwenden Sie die Registerkarte **Hüter** , um die Personen hinzuzufügen und zu verwalten, die Sie im Fall als Personen von Interesse identifiziert haben. Wenn Sie Verwalter hinzufügen, können Sie schnell Depotbank-bezogene Aktionen wie das Platzieren einer legalen Vorgehensweise für Depotbank-Datenquellen wie das Postfach und das OneDrive-Konto, die Kommunikation mit den Bewahrern und das Durchsuchen von Depotdaten Quellen zum Sammeln von Inhalten ausführen. , der für den Fall relevant ist. Wie bei den Fortschritten ist es ganz einfach, neue Verwalter hinzuzufügen oder Verwalter aus dem Fall zu entbinden. Weitere Informationen finden Sie unter [Arbeiten mit Verwaltern in Advanced eDiscovery (Preview)](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Verwalten von Benachrichtigungen über zugelassene Aufbewahrungszeiträume

Verwenden Sie **** die Registerkarte Kommunikationen, um den Prozess der Kommunikation mit den Verwaltern in dem Fall zu verwalten. In einem gesetzlichen Aufbewahrungs Vermerk werden Verwalter angewiesen, alle Inhalte, die für den Fall relevant sein können, aufzubewahren. Juristische Teams müssen in der Lage sein, diese Nachrichten zu verfolgen, die von Verwaltern empfangen, gelesen und anerkannt wurden. Der Kommunikations Workflow in Advanced eDiscovery (Preview) ermöglicht Ihnen das Erstellen und Senden von anfänglichen Benachrichtigungen, Erinnerungen, Freigabe Benachrichtigungen und Eskalationen, wenn Verwalter eine Hold-Benachrichtigung nicht bestätigen. Weitere Informationen finden Sie unter [Arbeiten mit Kommunikation in Advanced eDiscovery (Preview)](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Verwalten der Inhalts Aufbewahrung

Wenn Sie einem Fall einen Verwalter hinzufügen, haben Sie die Möglichkeit, Depotdaten aufzubewahren. Verwenden Sie die Registerkarte halte **Status** , um den beim Hinzufügen von Verwaltern erstellten Speicher zu verwalten und zusätzliche gesetzliche aufbewahrungsbereiche für den Fall zu verwalten. Sie können beispielsweise Datenquellen ohne Freiheitsentzug identifizieren und aufbewahren. Sie können auch alle Haltestatus in der Groß-/Kleinschreibung bearbeiten und Sie als abfragebasierte Aufbewahrungsdauer festlegen, sodass nur der Inhalt, der mit der Abfrage übereinstimmt, gespeichert wird. Sie können beispielsweise einen Datumsbereich zur Aufbewahrung hinzufügen, sodass nur Inhalte, die innerhalb eines bestimmten Datums erstellt wurden, beibehalten wurden. Sie können auch Statistiken zu Inhalten abrufen, die in der Warteschleife enthalten sind, den Haltestatus nach dem Zeitpunkt entfernen, zu dem er nicht mehr relevant ist, oder löschen. Weitere Informationen finden Sie unter [Manage Holds in Advanced eDiscovery (Preview)](managing-holds.md).

## <a name="indexing-custodian-data"></a>Indizierung von Depotdaten

Wenn Sie einen Depot und die dazugehörigen Datenquellen zu einem Fall hinzufügen, wird jedes teilweise indizierte Element aus einer Depotbank-Datenquelle erneut indiziert (durch einen Prozess namens *Advanced Indexing*). Auf diese Weise können Freiheitsentzug-Inhalte wie Bilder, nicht unterstützte Dateitypen und andere potenziell nicht indizierte Inhalte vollständig durchsuchbar werden, um Daten zu sammeln, die für den Fall relevant sind. Verwenden Sie die Registerkarte **Verarbeitung** , um den Status der erweiterten Indizierung zu überwachen und Verarbeitungsfehler zu beheben (mithilfe einer Process Calle- *Fehler*Korrektur.) Weitere Informationen finden Sie unter [Beheben von Verarbeitungsfehlern in Advanced eDiscovery (Preview)](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Erfassen von Falldaten

Verwenden Sie die Registerkarte **Suchvorgänge** , um Suchvorgänge zum Durchsuchen der in-Place-und nicht-Pfleger-Datenquellen in Office 365 für Inhalte zu erstellen, die für den Fall relevant sind. Sie können abfragebasierte Suchvorgänge (mithilfe von Schlüsselwörtern und Bedingungen) erstellen und ausführen, um eine festgelegte e-Mail-Nachricht und Dokumente zu identifizieren, die für den Fall relevant sind, und die Sie in den folgenden Schritten im eDiscovery-Workflow weiter prüfen und analysieren möchten. Sie können eine oder mehrere Suchvorgänge erstellen, die mit der Anfrage verknüpft sind. Darüber hinaus können Sie das Such Tool verwenden, um eine Vorschau der Beispiel Dokumente und Suchstatistiken anzuzeigen, die dazu beitragen können, die Suchergebnisse zu verfeinern und zu verbessern. Wenn Sie festgestellt haben, dass die Suchergebnisse alle für den Fall relevanten Daten enthalten, fügen Sie die Suchergebnisse einem Workingset zur weiteren Überprüfung, Analyse und gegebenenfalls zum Culling hinzu. Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall in Advanced eDiscovery (Preview)](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>ÜberPrüfen und Analysieren von Falldaten

Verwenden Sie die Registerkarte **Working Sets** , oder überprüfen und analysieren Sie die Inhalte, die Sie im Live-System gesammelt und einem Arbeitssatz hinzugefügt haben. Bei ** einem Workingset handelt es sich um eine statische Sammlung (also eine Offlinekopie von DAT) von freiheitsentziehenden Daten (und ggf. Daten ohne Freiheitsentzug), die Sie in der vorherigen Phase des eDiscovery-Workflows gesammelt haben. Wenn Sie Suchergebnisse zu einem Arbeitssatz hinzufügen, wird ein Prozess ausgelöst, der Dateien aus Containern extrahiert, Metadaten extrahiert und Text extrahiert. Wenn dieser Prozess abgeschlossen ist, erstellt das System einen neuen Index aller Daten, die von Depotbanken gesammelt und dem Arbeitssatz hinzugefügt wurden. Nachdem die Daten der Arbeitsmappe hinzugefügt wurden, können Sie zusätzliche Abfragen ausführen, um die Falldaten einzuschränken, Daten als Text oder im systemeigenen Dateiformat anzuzeigen und Dokumente im Arbeitssatz mit Anmerkungen versehen, redact und zu markieren. Darüber hinaus können Sie erweiterte Analysen wie Dokument Duplizierung, e-Mail-Threading und Designs durchführen. Nachdem Sie die Daten nur auf das, was für den Fall relevant ist, gekeult haben, können Sie entweder Download Dokumente direkt herunterladen oder Sie zusammen mit Datei Metadaten, Anmerkungen und beliebigen Tags exportieren. Weitere Informationen finden Sie unter:

  - [Überprüfen von Falldaten in Advanced eDiscovery (Preview)](reviewing-data-in-working-set.md)
  - [Analysieren von Daten in einem Arbeitssatz in Advanced eDiscovery (Preview)](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportieren von Daten zur Überarbeitung und Präsentation

Nachdem Sie die Daten aus einem Arbeitssatz exportiert haben, verwenden **** Sie die Registerkarte Exporte, um einen Exportauftrag zu verwalten und Daten aus einem Arbeitssatz herunterzuladen. Wenn Sie eine Arbeitsmappe exportieren, werden die Daten an einen Azure-Speicherort hochgeladen und können dann auf einen lokalen Computer heruntergeladen werden. Sie können den Speicherort und den Speicher Bewertungsschlüssel abrufen, der zum Herunterladen der exportierten Daten auf der Registerkarte **Exports** erforderlich ist. Weitere Informationen finden Sie unter [Exportieren von Falldaten in Advanced eDiscovery (Preview)](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Verwalten der Aufträge

Überwachen Sie auf der Registerkarte **Aufträge** lang andauernde Prozesse für von Ihnen initiierte fallbezogene Aufgaben, suchen Sie nach Neuindizierung, suchen und exportieren. Sie können beispielsweise eine neue Suche auf der Registerkarte **Suchvorgänge** erstellen, die eine Vielzahl von Datenquellen enthält. Der Status dieses Suchvorgangs wird auf der Registerkarte **Aufträge** angezeigt. Weitere Informationen finden Sie unter [Manage Jobs in Advanced eDiscovery (Preview)](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Konfigurieren von Falleinstellungen

Auf der Registerkarte **Einstellungen** können Sie die Groß-/Kleinschreibung konfigurieren. Dazu gehört das Hinzufügen von Mitgliedern zu einem Fall, schließen oder Löschen eines Falls und Konfigurieren des Such-und Analyse Verhaltens. Weitere Informationen finden Sie unter [Konfigurieren von Fall Einstellungen in Advanced eDiscovery (Preview)](configuring-case-settings-ediscovery20.md).


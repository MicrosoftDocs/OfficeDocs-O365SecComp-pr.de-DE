---
title: Übersicht über die erweiterte eDiscovery-Lösung in Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: In diesem Artikel wird die neue Version von Advanced eDiscovery in Microsoft 365 beschrieben.
ms.openlocfilehash: a29e156cee9af1f5bf4ef3339614a1db52254d6c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154997"
---
# <a name="overview-of-the-advanced-ediscovery-solution-in-microsoft-365"></a>Übersicht über die erweiterte eDiscovery-Lösung in Microsoft 365

Die erweiterte eDiscovery-Lösung in Microsoft 365 baut auf den vorhandenen eDiscovery-und Analysefunktionen in Office 365 auf. Diese neue Lösung, die als *Erweiterte eDiscovery*bezeichnet wird, bietet einen End-to-End-Workflow zum aufbewahren, sammeln, überprüfen, analysieren und Exportieren von Inhalten, die auf interne und externe Untersuchungen in Ihrer Organisation reagieren. Außerdem können Legal Teams den gesamten Workflow für rechtliche Aufbewahrungs Benachrichtigungen verwalten, um mit in einem Fall beteiligten Verwaltern zu kommunizieren. 

## <a name="alignment-with-edrm"></a>Ausrichtung mit EDRM

Der integrierte Workflow von Advanced eDiscovery richtet sich an den eDiscovery-Prozess, der durch das Electronic Discovery Reference Model (EDRM) beschrieben wird. 

![Das elektronische Discovery Reference Model (EDRM)](../media/EDRMv1.png)

(Bildquelle mit freundlicher Genehmigung von EDRM.net. Das Quellbild wurde unter Creative Commons Attribution 3,0 Unported License zur Verfügung gestellt.)

Hier erfahren Sie, wie Advanced eDiscovery den EDRM-Workflow auf hohem Niveau unterstützt:

- **Identifikation** – nachdem Sie potenzielle Personen für eine Untersuchung identifiziert haben, können Sie Sie als Verwalter (auch als *Datenverwalter*bezeichnet) hinzufügen, da diese möglicherweise Informationen enthalten, die für die Untersuchung relevant sind. eDiscovery-Fall. Nachdem Benutzer als Verwalter hinzugefügt wurden, ist es ganz einfach, Depot Dokumente aufzubewahren, zu sammeln und zu überprüfen.

- **Bewahrung** – um Daten, die für eine Untersuchung relevant sind, beizubehalten und zu schützen, können Sie mit Advanced eDiscovery die Datenquellen, die den Depot Betreuern zugeordnet sind, in einem Fall legal halten. Sie können auch Daten für nicht-Freiheitsentzug speichern. Darüber hinaus verfügt Advanced eDiscovery über einen integrierten Kommunikations Workflow, sodass Sie Benachrichtigungen für rechtliche Aufbewahrungen an Verwalter senden und deren Bestätigungen nachverfolgen können.

- **Collection** – nachdem Sie die für die Untersuchung relevanten Datenquellen identifiziert (und aufbewahrt) haben, können Sie das integrierte Such Tool in der erweiterten eDiscovery-Suche für und Sammeln von Livedaten aus den Freiheits Datenquellen (und Datenquellen ohne Freiheitsentzug) verwenden. (falls zutreffend), die für den Fall relevant sein können.

- **Processing** – nachdem Sie alle für den Fall relevanten Daten gesammelt haben, ist der nächste Schritt der Prozess für die weitere Überprüfung und Analyse. In Advanced eDiscovery bedeutet dies, dass die in der Sammlungsphase identifizierten in-Place-Daten in einen Azure-Speicherort (als Überprüfungs *Gruppe*bezeichnet) kopiert werden, der eine statische Ansicht der Falldaten bereitstellt. 
 
- **Review** – nachdem Daten zu einem Überprüfungs Satzes hinzugefügt wurden, können Sie bestimmte Dokumente anzeigen und zusätzliche Abfragen ausführen, um die Daten auf die für den Fall relevantesten zu reduzieren. Außerdem können Sie bestimmte Dokumente mit Anmerkungen versehen und kennzeichnen.
 
- **Analyse** – Advanced eDiscovery stellt integrierte Analysetools bereit, mit denen Sie weitere Daten aus dem Überprüfungs Sätzen ausmerzen können, die Sie für die Untersuchung nicht relevant finden. Zusätzlich zur Verringerung der Menge relevanter Daten hilft Ihnen Advance eDiscovery (Preview) auch, rechtliche Überprüfungskosten zu sparen, indem Sie Inhalte organisieren, um den Überprüfungsprozess einfacher und effizienter zu gestalten.

- **Produktion** und **Präsentation** – Wenn Sie dazu in der Lage sind, können Sie Dokumente aus einem Überprüfungs Satzes für die juristische Überprüfung exportieren. Sie können Dokumente in ihrem systemeigenen Format oder in einem von EDRM angegebenen Format exportieren, sodass Sie in Überprüfung-Anwendungen von Drittanbietern importiert werden können.

## <a name="advanced-ediscovery-workflow"></a>Erweiterter eDiscovery-Workflow

In den folgenden Abschnitten werden die einzelnen Schritte des integrierten End-to-End-Workflows in Advanced eDiscovery beschrieben. Der folgende Screenshot zeigt die Registerkarte **Start** eines Falls mit dem Namen *Product Liability 2019002*. Hinweis die Workflow Registerkarten oben auf der Seite werden sequenziert, um Sie mit dem EDRM-Prozess auszurichten. 

Weitere Informationen zum End-to-End-Workflow in Advanced eDiscovery finden Sie in diesem [Microsoft Mechanics-Video](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Registerkarten in Advanced eDiscovery entsprechen dem EDRM-Workflow](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Verwalten von Verwaltungsberechtigten

Verwenden Sie die Registerkarte **depotverwalter** , um Personen hinzuzufügen und zu verwalten, die Sie im Fall als interessierte Personen identifiziert haben. Wenn Sie Verwalter hinzufügen, können Sie schnell Depot bezogene Aktionen durchführen, beispielsweise das Festlegen einer Aufbewahrungspflicht für Depotdaten Quellen, wie das Postfach und das OneDrive-Konto, die Kommunikation mit den Verwaltern und das Durchsuchen von Depotdaten Quellen zum Sammeln von Inhalten. Das ist für den Fall relevant. Wenn der Fall fortschreitet, können Sie ganz einfach neue Depotbanken oder Ersetzungs Verwalter aus dem Fall hinzufügen. Weitere Informationen finden Sie unter [Arbeiten mit Verwaltern in Advanced eDiscovery](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Verwalten von Benachrichtigungen über zugelassene Aufbewahrungszeit

Verwenden Sie **** die Registerkarte Kommunikationen, um den Prozess der Kommunikation mit den Depotbanken im Fall zu verwalten. Ein rechtlicher Aufbewahrungs Bescheid weist Verwalter an, alle Inhalte zu bewahren, die für den Fall relevant sein können. Zugelassene Teams müssen in der Lage sein, nachzuverfolgen, dass Benachrichtigungen empfangen, gelesen und von den Verwaltern bestätigt wurden. Der Kommunikations Workflow in Advanced eDiscovery ermöglicht Ihnen das Erstellen und Senden von anfänglichen Benachrichtigungen, Erinnerungen, Freigabe Benachrichtigungen und Eskalationen, wenn Verwalter eine Aufbewahrungs Benachrichtigung nicht bestätigen. Weitere Informationen finden Sie unter [Arbeiten mit Kommunikationen in Advanced eDiscovery](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Verwalten der Inhalts Aufbewahrung

Wenn Sie eine Depotbank zu einem Fall hinzufügen, haben Sie die Möglichkeit, Aufbewahrungsdaten aufzubewahren. Verwenden Sie die Registerkarte halte **Status** , um den beim Hinzufügen von Depotstellen erstellten Aufbewahrungsplatz zu verwalten und zusätzliche Rechtliche Aufbewahrungspflicht zu verwalten, die dem Fall zugeordnet sind (beispielsweise können Sie Datenquellen ohne Freiheitsentzug identifizieren und aufbewahren). Sie können auch jeden Haltebereich für den Fall bearbeiten und als Abfrage basiert halten, sodass nur der Inhalt, der mit der Abfrage übereinstimmt, gespeichert wird. Sie können beispielsweise einen Datumsbereich zum Haltestatus hinzufügen, sodass nur Inhalte, die innerhalb eines bestimmten Datums erstellt wurden, in beibehalten gespeichert wurden. Sie können auch Statistiken zu Inhalten abrufen, die in der Warteschleife gespeichert sind, den Haltebereich entfernen, nachdem er für den Fall nicht mehr relevant ist, oder ihn löschen. Weitere Informationen finden Sie unter [Manage Holds in Advanced eDiscovery](managing-holds.md).

## <a name="indexing-custodian-data"></a>Indexieren von Depotdaten

Wenn Sie einem Fall eine Depotstelle und die entsprechenden Datenquellen für den Freiheitsentzug hinzufügen, wird jedes teilweise indizierte Element aus einer Depotbank-Datenquelle neu indiziert (durch einen Prozess namens *Advanced Indexing*). Dadurch können Freiheits geschützte Inhalte wie Bilder, nicht unterstützte Dateitypen und andere potenziell nicht indizierte Inhalte vollständig durchsucht werden, wenn Sie Suchvorgänge ausführen, um Daten für den Fall zu sammeln. Verwenden Sie die Registerkarte **Verarbeitung** , um den Status der erweiterten Indizierung zu überwachen und Verarbeitungsfehler zu beheben (mithilfe eines Prozesses namens *Fehlerbehebung*). Weitere Informationen finden Sie unter [Beheben von Verarbeitungsfehlern in Advanced eDiscovery](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Erfassen von Falldaten

Verwenden Sie die Registerkarte **Suchen** , um Suchvorgänge für in-Place-Freiheitsentzug-und nicht-Freiheitsentzug-Datenquellen in Office 365 für für den Fall relevante Inhalte zu erstellen. Sie können abfragebasierte Suchvorgänge erstellen und ausführen (unter Verwendung von Schlüsselwörtern und Bedingungen), um eine Gruppe von e-Mail-Nachrichten und Dokumenten zu identifizieren, die für den Fall relevant sind und die Sie in den folgenden Schritten im eDiscovery-Workflow weiter überprüfen und analysieren möchten. Sie können eine oder mehrere Suchvorgänge erstellen, die mit der Anfrage verknüpft sind. Darüber hinaus können Sie das Such Tool verwenden, um eine Vorschau von Beispiel Dokumenten anzuzeigen und Suchstatistiken anzuzeigen, die Ihnen helfen können, die Suchergebnisse zu verfeinern und zu verbessern. Nachdem Sie sichergestellt haben, dass die Suchergebnisse alle für den Fall relevanten Daten enthalten, fügen Sie die Suchergebnisse zu einem Überprüfungs Satzes hinzu, um die weitere Überprüfung, Analyse und ggf. das ausmerzen zu erhalten. Weitere Informationen finden Sie unter [Sammeln von Daten für einen Fall in Advanced eDiscovery](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>Überprüfen und Analysieren von Case-Daten

Auf der Registerkarte Überprüfungs **Sätze** können Sie die Inhalte, die Sie im Live-System gesammelt und einem Überprüfungs Satz hinzugefügt haben, überprüfen und analysieren. Ein *Überprüfungs Satz* ist eine statische Sammlung dieser Daten (mit anderen Worten: eine Offlinekopie von Daten) von Daten für den Freiheitsentzug (und, falls zutreffend, Daten ohne Freiheitsentzug), die Sie in der vorherigen Phase des eDiscovery-Workflows gesammelt haben. Wenn Sie einer Überprüfungsgruppe Suchergebnisse hinzufügen, wird ein Prozess ausgelöst, der Dateien aus Containern extrahiert, Metadaten extrahiert und Text extrahiert. Wenn dieser Vorgang abgeschlossen ist, erstellt das System einen neuen Index aller Daten, die von Verwaltern gesammelt und dem Überprüfungs Satzes hinzugefügt wurden. Nachdem die Daten dem Überprüfungs Sätzen hinzugefügt wurden, können Sie zusätzliche Abfragen ausführen, um die Falldaten einzuschränken, Daten als Text oder im systemeigenen Dateiformat anzuzeigen und Dokumente in der Überprüfungsgruppe mit Anmerkungen, redact und Tags zu versehen. Darüber hinaus können Sie erweiterte Analysen durchführen, beispielsweise das Identifizieren von Dokument Duplikaten, e-Mail-Threads und Designs. Nachdem Sie die Daten nur auf das, was für den Fall relevant ist, abgeschlachtet haben, können Sie Dokumente entweder direkt herunterladen oder zusammen mit Datei Metadaten, Anmerkungen und Tags exportieren. Weitere Informationen finden Sie unter:

  - [Überprüfen von Case-Daten in Advanced eDiscovery](reviewing-data-in-review-set.md)
  - [Analysieren von Daten in einer Überprüfungsgruppe in Advanced eDiscovery](analyzing-data-in-review-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportieren von Daten zur Überprüfung und Präsentation

Nachdem Sie die Daten aus einem Überprüfungs Satzes exportiert haben **** , verwenden Sie die Registerkarte Exports, um einen Exportauftrag zu verwalten und Daten aus einem Überprüfungspaket herunterzuladen. Beim Exportieren eines Überprüfungs Satzes werden die Daten in einen Azure-Speicherort hochgeladen und stehen dann auf einem lokalen Computer heruntergeladen werden. Sie können den erforderlichen Standort-und Speicher Bewertungsschlüssel abrufen, um die exportierten Daten **** auf der Registerkarte "Exports" herunterzuladen. Weitere Informationen finden Sie unter [Exportieren von Case-Daten in Advanced eDiscovery](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Verwalten der Aufträge

Verwenden Sie die Registerkarte **Aufträge** , um langwierige Prozesse für bereits initiierte fallbezogene Aufgaben zu überwachen. Beispiele für Aufträge sind die im Zusammenhang mit der erneuten Indizierung, der Suche und dem Export von Case-Daten. Beispielsweise können Sie eine neue Suche auf der Registerkarte **Suchen** erstellen, die eine große Anzahl von Datenquellen enthält. Der Status dieses Suchvorgangs wird auf der Registerkarte **Aufträge** angezeigt. Weitere Informationen finden Sie unter [Manage Jobs in Advanced eDiscovery](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Konfigurieren von Falleinstellungen

Verwenden Sie die Registerkarte **Einstellungen** , um Einstellungen für Groß-/Kleinschreibung zu konfigurieren. Dies umfasst das Hinzufügen von Mitgliedern zu einem Fall, das Schließen oder Löschen eines Falls und das Konfigurieren des Such-und Analyse Verhaltens. Weitere Informationen finden Sie unter [Konfigurieren von Fall Einstellungen in Advanced eDiscovery](configuring-case-settings-ediscovery20.md).

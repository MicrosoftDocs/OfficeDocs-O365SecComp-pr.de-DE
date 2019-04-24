---
title: Überprüfen von Nachweisdaten
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
ms.openlocfilehash: e84f05fa1a7356952b62f2f4adc3b7d0f1ddc94e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258043"
---
# <a name="review-the-data-in-evidence"></a>Überprüfen von Nachweisdaten

Bei den Daten in einem Evidence-Satz in einer Daten Untersuchung handelt es sich um eine Momentaufnahme der Suchergebnisse, die Sie gesammelt und dem Evidence-Satz hinzugefügt haben. Wenn Sie Suchergebnisse zu beweisen hinzufügen, wird ein Prozess ausgelöst, um Dateien, Metadaten und Text aus den von der Suche zurückgegebenen Elementen zu extrahieren. Dann erstellt das Tool für Daten Untersuchungen (Vorschau) einen neuen Index (durch einen Prozess namens *Advanced Indexing*) aller Daten und fügt einen auf der Registerkarte **Evidence** festgelegten Nachweis hinzu. 

Bei zeitabhängigen Untersuchungen können Sie dadurch schnell die Umgebung eindämmen, indem Sie die tatsächlich verschütteten oder bösartigen Daten, die sich in der ursprünglichen Datenquelle befinden, löschen und gleichzeitig den erneut erstellten Beweis in einem isolierte Umgebung, in diesem Fall werden die Daten in den Evidence-Satz kopiert. Nachdem der Beweis gesammelt und dem Evidence-Satz hinzugefügt wurde, können Sie einzelne Dokumente im nativen Format, im Text Format oder in einem nahezu systemeigenen Format überarbeiten, mit dem Sie Dokumente mit Anmerkungen versehen und redact können. Darüber hinaus können Sie Abfragen ausführen, um die Datensätze nach Zeitspanne, Dateitypen, Datenbesitzern und vielen anderen Eigenschaften und Suchbedingungen einzugrenzen. Beispielsweise können Sie mithilfe der Bedingungen Autor, Absender oder Empfänger schnell erkennen, welche Personen an dem Vorfall beteiligt sind und ob Daten aus Ihrer Organisation für externe Benutzer freigegeben wurden. Weitere Informationen zum Durchsuchen von Daten in einem Evidence-Satz finden Sie unter [Query the data in Evidence](evidence-query.md).

Um Dokumente zu gruppieren und weitere Unterstützung für Ihre Überprüfungen zu erhalten, wählen Sie auf der Registerkarte **Evidence** einen Evidence-Satz aus, und klicken Sie dann auf **Evidence verwalten**. Klicken Sie in der **Analytics** -Kachel auf **Analyse für den gesamten Satz neu erstellen**. Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt. Anschließend können Sie die allgemeinen Themen der Daten sehen und auch Dokumente per e-Mail-Threads, in der Nähe von Duplikaten und exakte Duplikate organisieren, um Ihre Untersuchung zu unterstützen. Weitere Informationen finden Sie unter [Run Analytics to untersuchen schneller](run-analytics-to-investigate-faster.md).

## <a name="view-documents-in-evidence"></a>Dokumente als Beweis anzeigen

Daten Untersuchungen (Preview) ermöglicht die Anzeige von Inhalten in mehreren verschiedenen Viewern, wobei jeder Betrachter einen anderen Zweck hat. Diese Zuschauer sind:

- Datei Metadaten
- Systemeigene Ansicht
- Text Ansicht
- Ansicht mit Anmerkungen

Wenn Sie auf einen dieser Viewer zugreifen möchten, wählen Sie ein Dokument in einem Evidence-Set aus.

## <a name="file-metadata"></a>Datei Metadaten

In dieser Ansicht werden verschiedene Metadaten-Eigenschaften angezeigt, die dem ausgewählten Dokument zugeordnet sind. Sie können diese Ansicht ein-und ausschalten, indem Sie auf **Datei Metadaten**klicken. Beim Überprüfen eines Dokuments können Sie die Datei Metadaten anzeigen und trotzdem zwischen den verschiedenen Viewern wechseln.

Im folgenden finden Sie ein Beispiel für die Datei Metadaten für ein Dokument. Weitere Informationen zu den Metadatenfeldern finden Sie unter [Document Metadata fields in Data Investigations (Preview)](document-metadata-fields.md).

![Datei-Metadatenbereich](../media/Reviewimage2.png)

## <a name="native-view"></a>Systemeigene Ansicht

Der systemeigene Viewer zeigt die genaueste Ansicht eines Dokuments im systemeigenen Format an. Die systemeigene Ansicht wird für Hunderte von Dateitypen unterstützt und soll Dokumente in der größtmöglichen nativen Umgebung anzeigen. Für Microsoft Office-Dateien verwendet der systemeigene Viewer Office Online. Auf diese Weise können Sie Inhalte wie Kommentare in verschiedenen Office-Dokumenten, Formeln und ausgeblendeten Zeilen/Spalten in Excel und die Notizenansicht in PowerPoint anzeigen.

![Systemeigene Ansicht
](../media/Reviewimage3.png)

## <a name="text-view"></a>Text Ansicht

Der Text Betrachter bietet eine Ansicht des extrahierten Texts einer Datei. Eingebettete Bilder und Formatierungen werden ignoriert, aber diese Ansicht ist sehr nützlich, wenn Sie versuchen, die Inhalte in einem Dokument schnell zu überprüfen und zu verstehen. Die Text Ansicht umfasst auch die folgenden Features:

  - Ein Linien Zähler, der das referenzieren bestimmter Teile eines Dokuments erleichtert.

  - Hervorheben von Suchtreffern, die Ausdrücke im Dokument sowie auf der Bildlaufleiste hervorheben

  - Eine diff-Ansicht bietet eine Vergleichsansicht, in der die Textunterschiede beim Anzeigen von Dokumenten mit dem Panel **near Duplicates** hervorgehoben werden.

**Beispiel für Linien Zähler und Suchtreffer Hervorhebung in Text und ScrollBar**

![Text Ansicht
](../media/Reviewimage4.png)

**Beispiel für die diff-Ansicht**

![Ansicht "diff"
](../media/Reviewimage5.png)

## <a name="annotate-view"></a>Ansicht mit Anmerkungen

In der Ansicht mit Anmerkungen werden Features bereitgestellt, mit denen Sie während des überarbeits Vorgangs Markups für ein Dokument anwenden können. Hierzu gehören die folgenden Tools:

  - **Flächen-Aktionen** – Sie können ein deckendes Feld im Dokument zeichnen, das vertrauliche Inhalte ausgeblendet.

  - **Bleistift** – Sie können ein Dokument Freihandzeichnen, um auf bestimmte Teile des Inhalts zu achten.

  - **Anmerkungen auswählen** – Sie können Anmerkungen in einem Dokument auswählen und löschen.

  - **Anmerkungs Transparenz umschalten** – Sie können die Transparenz von Anmerkungen (zwischen deckend und halbtransparent) so umschalten, dass der Inhalt hinter der Anmerkung angezeigt wird. Dazu gehört das Umschalten der Transparenz von Bleistift Anmerkungen und-Aktionen.

Die Ansicht mit Anmerkungen stellt auch die folgenden Navigationsfunktionen bereit:

  - **Vorherige Seite**, **Nächste Seite**, und **Navigieren Sie zu** Steuerelementen für die Seiten Navigation für mehrseitige Dokumente.

  - **Zoom** – erhöht oder verkleinert die Größe von Dokumenten in der Ansicht mit Anmerkungen.

  - **Rotate** – Dokumente im Uhrzeigersinn drehen.

  - **Suche** – suchen Sie nach Schlüsselwörtern in einem Dokument, und verwenden Sie dann die vorherigen und nächsten Steuerelemente, um die Treffer (die hervorgehoben werden) innerhalb des Dokuments anzuzeigen.

**Beispiel für eine Ansicht mit Anmerkungen**

![Ansicht mit Anmerkungen](../media/Reviewimage1.png)

> [!NOTE]
> Anmerkungen werden auf eine Kopie des Dokuments angewendet, das dem Evidence-Satz hinzugefügt wurde. Die Originaldokumente im Live-Dienst werden nicht mit Anmerkungen versehen.

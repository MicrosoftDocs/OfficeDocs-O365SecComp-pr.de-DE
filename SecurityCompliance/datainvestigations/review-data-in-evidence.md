---
title: Über Prüfdaten in Evidence
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
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030148"
---
# <a name="review-data-in-evidence"></a>Über Prüfdaten in Evidence

**Evidence** ist eine Momentaufnahme der Suchergebnisse, die Sie gesammelt haben. Wenn Sie Suchergebnisse zu beweisen hinzufügen, wird ein Prozess ausgelöst, um Dateien, Metadaten und Text zu extrahieren. Anschließend erstellt das System einen neuen Index aller Daten und fügt den Nachweise hinzu ****. 

Bei zeitabhängigen Vorfällen können Sie dadurch schnell die Umgebung eindämmen, indem Sie Daten an ursprünglichen Speicherorten löschen und erneut erstellte Nachweise in einer isolierten Umgebung untersuchen. Nach dem Sammeln von beweisen können Sie einzelne Dokumente im nativen Format, im Text Format oder in einem nahezu systemeigenen Format überarbeiten. Darüber hinaus können Sie Abfragen ausführen, um die Daten nach Zeitspanne, Dateitypen, Datenbesitzern und vielen anderen Bedingungs Karten einzugrenzen. Mit Autor/Absender/Empfänger-Bedingungs Karten können Sie schnell untersuchen, wer am Spill beteiligt ist und ob externe Freigaben vorhanden sind. Weitere Informationen finden Sie unter:

  - [Abfragen der Daten nach belegen](evidence-query.md)

Klicken Sie auf **Beweise verwalten**, um Dokumente zu gruppieren und weitere Unterstützung für Ihre Überprüfungen zu erhalten. Klicken Sie in der **Analytics** -Kachel auf **analysieren**. Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt. Anschließend können Sie die allgemeinen Themen der Daten sehen und auch Dokumente per e-Mail-Threads, exakte Duplikate und beinahe-Duplikate organisieren, um Ihre Untersuchung zu erleichtern. Weitere Informationen finden Sie unter:

  - [Führen Sie Analysen aus, um schneller zu untersuchen](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a>Dokumente als Beweis anzeigen

Data Investigation (Preview) zeigt Inhalte über mehrere Betrachter an, die jeweils unterschiedlichen Zwecken dienen. Die verschiedenen Betrachter können verwendet werden, indem Sie auf ein beliebiges Dokument in **Evidence**klicken. Die derzeit bereitgestellten Viewer sind:

- Datei Metadaten
- Systemeigene Ansicht
- Text Ansicht
- Ansicht mit Anmerkungen
- Konvertierte Ansicht

## <a name="file-metadata"></a>Datei Metadaten

Dieses Panel kann ein-oder ausgeschaltet werden, um verschiedene Metadaten anzuzeigen, die mit dem Dokument verknüpft sind. Auch wenn das Suchergebnis Raster angepasst werden kann, um bestimmte Metadaten anzuzeigen, gibt es Fälle, in denen horizontaler Bildlauf beim Überprüfen von Daten schwierig sein kann. Der Datei-Metadatenbereich ermöglicht es einem Benutzer, eine Ansicht innerhalb des Viewers einzuschalten.

![Datei-Metadatenbereich
](../media/Reviewimage2.png)

## <a name="native-view"></a>Systemeigene Ansicht

Der systemeigene Viewer zeigt die umfangreichste Ansicht eines Dokuments an. Es unterstützt Hunderte von Dateitypen und soll eine möglichst Native Erfahrung darstellen. Für Microsoft Office-Dateien nutzt der Viewer beispielsweise Office Online, um Inhalte wie Dokument Kommentare, Excel-Formeln, ausgeblendete Zeilen/Spalten, PowerPoint-Notizen usw. anzuzeigen. Weitere Informationen zu den Office Online-Viewern finden Sie \[hier need Link\]

![Systemeigene Ansicht
](../media/Reviewimage3.png)

## <a name="text-view"></a>Text Ansicht

Der Text Betrachter bietet eine Ansicht des extrahierten Texts einer Datei. Eingebettete Bilder und Formatierungen werden ignoriert, aber eine sehr leistungsfähigere Ansicht, wenn ein Benutzer versucht, den Inhalt schnell zu verstehen. Die Text Ansicht umfasst auch andere Features:

  - Linien Zähler erleichtert das verweisen auf bestimmte Teile eines Dokuments

  - Hervorhebung von Suchtreffern, die Ausdrücke innerhalb des Dokuments sowie die Bildlaufleiste hervorheben

  - Die Ansicht diff bietet eine Vergleichsansicht, in der Textunterschiede beim Anzeigen von nahezu doppelt vorhandenen Dokumenten hervorgehoben werden.

![Text Ansicht
](../media/Reviewimage4.png)

![Ansicht "diff"
](../media/Reviewimage5.png)

## <a name="annotate-view"></a>Ansicht mit Anmerkungen

In der Ansicht mit Anmerkungen werden Features bereitgestellt, mit denen Benutzer während der Untersuchung Markups für ein Dokument anwenden können, einschließlich:

  - Flächen-Aktionen – Benutzer können ein Feld in das Dokument ziehen, um vertrauliche Inhalte zu verstecken.

  - Bleistift – Benutzer können ein Dokument Freihandzeichnen, um die Aufmerksamkeit auf bestimmte Teile eines Dokuments zu lenken.

  - Anmerkungen auswählen – Benutzer können Anmerkungen in einem Dokument auswählen, um Sie zu löschen

  - UmSchalten der Anmerkungs Transparenz – macht Anmerkungen halbtransparent, um den Inhalt hinter der Anmerkung anzuzeigen

  - Vorherige Seite – navigiert zur vorherigen Seite

  - Nächste Seite – navigiert zur nächsten Seite

  - Gehe zu Seite – der Benutzer kann eine bestimmte Seitenzahl eingeben, zu der navigiert werden soll.

  - Zoom – Zoomebene für Ansicht mit Anmerkungen festlegen

  - Rotate – Benutzer kann Dokument im Uhrzeigersinn drehen

  - Suche – der Benutzer kann in einem Dokument suchen und zu den verschiedenen Treffern innerhalb des Dokuments navigieren.
    
    ![Ansicht mit Anmerkungen
    ](../media/Reviewimage1.png)

Beachten Sie, dass diese Anmerkungen auf Daten, die als Beweise gesammelt werden, nicht an seinem ursprünglichen Speicherort in Live System gespeichert werden. 

## <a name="more-information"></a>Weitere Informationen

In der folgenden Tabelle sind die Grenzwerte für Beweise in Daten Untersuchungen (Preview) aufgeführt.  Alle Elemente, die die maximale Anzahl der einzelnen Dateien überschreiten, werden als Verarbeitungsfehler angezeigt.
    
  |**Beschreibung der Beschränkung**|**Grenzwert**|
  |:-----|:-----|
  |Maximale Anzahl von Evidence-Auflistungen  <br/> |50  <br/> |
  |Gesamtanzahl der Dokumente, die in einen Fall aufgenommen werden können (für alle Evidence-Auflistungen in der Untersuchung)  <br/> |1 Million  <br/> |
  |Gesamtgröße der Datei pro Ladevorgang  <br/> |100 GB  <br/> |
  |Maximale Größe einer einzelnen Datei   <br/> |100 MB  <br/> |
  |Maximale Anzahl von Zeichen, die aus einer einzelnen Datei extrahiert wurden.  <br/> |10 Millionen  <br/> |
  |Tiefe der eingebetteten Elemente in einem Dokument  <br/> |25  <br/> |
  
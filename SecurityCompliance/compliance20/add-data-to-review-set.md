---
title: Hinzufügen von Suchergebnissen zu einem Übersichts Satz
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
ms.openlocfilehash: fc32836026d1a2c449e73a28eafc2f5a631a1705
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527187"
---
# <a name="add-search-results-to-a-review-set"></a>Hinzufügen von Suchergebnissen zu einem Übersichts Satz

Wenn Sie mit den Ergebnissen einer Suche zufrieden sind und Sie bereit sind, diese Suchergebnisse zu überprüfen und zu analysieren, können Sie Sie zu einem Übersichts Satz hinzufügen. Das Kopieren der ursprünglichen Daten in den Überprüfungs Satz erleichtert auch den Überprüfungs-und Analyseprozess, indem Sie erweiterte Analysetools wie die Erkennung von Designs, die Erkennung nahezu doppelter Informationen und die Identifizierung von e-Mail-Threads bereitstellt. Sie können auch Daten aus nicht-Office 365-Datenquellen zu einem Übersichts Satz hinzufügen, damit Sie diese Daten zusätzlich zu den von Office 365 gesammelten Daten überarbeiten können.

Wenn Sie die Ergebnisse einer Suche zu einem Übersichts Satz hinzufügen (Übersichts Sätze befinden sich auf der Registerkarte Übersichts **Sätze** des Falls), treten die folgenden beiden Vorgänge auf:

- Alle Elemente in den Suchergebnissen werden aus der ursprünglichen Datenquelle in den Live Office 365-Diensten kopiert und an einen sicheren Azure-Speicherort in der Microsoft-Cloud kopiert.

- Alle Elemente (einschließlich des Inhalts und der Metadaten) werden neu indiziert, sodass alle Daten im Übersichts Satz während der Überprüfungen der Falldaten vollständig durchsuchbar sind. Die erneute Indizierung der Daten führt zu gründlichen und sehr schnellen Suchvorgängen, wenn Sie die Daten im Überprüfungs Satz während der Fall Ermittlung durchsuchen.

Wenn Sie einem Übersichts Satz Daten hinzufügen möchten, klicken Sie auf der Registerkarte **Suchvorgänge** auf eine Suche, und klicken Sie dann auf der Seite Flyout auf **zu überprüfende Ergebnisse hinzufügen** .

![Hinzufügen von Daten zu einem Übersichts Satz](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

Beachten Sie, dass Sie einem vorhandenen überprüfungssatz hinzufügen oder einen neuen Übersichts Satz erstellen können.  Wenn Sie zu einem neuen Übersichts Satz hinzufügen, geben Sie den Namen an, und klicken Sie dann auf **Hinzufügen**.

![Auswählen eines Übersichts Satzes](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

Das Hinzufügen von Daten zu einem Übersichts Satz ist ein langwieriger Prozess. Dieser Prozess umfasst das Erfassen von Elementen aus den ursprünglichen Datenquellen in Office 365 (beispielsweise von Postfächern und Websites), das Kopieren dieser Elemente in den Azure-Speicherort (dieser Kopiervorgang wird auch als *Einnahme*bezeichnet) und das anschließende erneute Indizieren der Elemente. Sie können den Fortschritt auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchvorgänge** nachverfolgen, indem Sie den Status in der Spalte **hinzugefügte Daten zur Überprüfung festlegen** überwachen. Klicken Sie nach Abschluss der Überarbeitungs Satzverarbeitung im Fall auf die Registerkarte Überprüfungs **Sätze** , und klicken Sie dann auf den Überprüfungs Satz, um das Filtern, überprüfen, taggen und Exportieren von Daten im Überprüfungs Satz zu starten.

## <a name="add-a-sample-to-a-review-set"></a>Hinzufügen eines Beispiels zu einem Übersichts Satz

Wenn Sie die Ergebnisse einer Suche gründlich überprüfen möchten, bevor Sie Sie zu einem Überprüfungs Satz hinzufügen, können Sie ein Beispiel der Suchergebnisse einem Überprüfungs Satz hinzufügen, statt alles hinzuzufügen.

Wenn Sie einem Übersichts Satz ein Beispiel hinzufügen möchten, klicken Sie auf der Registerkarte Such **Vorgänge** auf eine Suche, und klicken Sie dann auf der Seite Flyout auf **Sample** . Wählen Sie **** auf der Seite samplingparameter eine der folgenden Optionen aus:

- **Konfidenzniveau%** und **Konfidenzintervall%** -die dem überprüfungssatz hinzugefügten Elemente werden durch die festgelegten statistischen Parameter bestimmt. Wenn Sie normalerweise eine Zuverlässigkeitsstufe und ein Intervall beim Sampling von Ergebnissen verwenden, geben Sie diese in den Dropdownfeldern an. Verwenden Sie andernfalls die Standardeinstellungen.

- **Zufallsstichprobe%** -die dem überprüfungssatz hinzugefügten Elemente basieren auf einer Zufallsauswahl des angegebenen Prozentsatzes der Gesamtanzahl der von der Suche zurückgegebenen Elemente.

Nachdem Sie eine der vorherigen Optionen ausgewählt und konfiguriert haben, wählen Sie einen vorhandenen überprüfungssatz aus, um das Beispiel hinzuzufügen, und klicken Sie dann auf **senden**. Sie können den Fortschritt auch auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchvorgänge** nachverfolgen, indem Sie den Status in der Spalte **hinzugefügte Daten zur Überprüfung festlegen** überwachen.
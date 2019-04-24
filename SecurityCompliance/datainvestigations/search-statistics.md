---
title: Suchstatistiken
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
ms.openlocfilehash: 986c3f3cbb19cd0f66b18db274e68a3bf8414952
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258103"
---
# <a name="search-statistics"></a>Suchstatistiken

Eine effektive Möglichkeit zum Überprüfen der Suchergebnisse bei der Untersuchung eines Daten Vorfalls, um die Statistiken über Ihre Suchergebnisse anzuzeigen, um sicherzustellen, dass Sie Ihren Erwartungen entsprechen. Wenn eine Suche ausgeführt wird, werden die folgenden allgemeinen Statistiken unter **Status** auf der Seite Suchdetails-Flyout angezeigt:

![Such statisics auf Suchdetails-Flyout-Seite](../media/SearchDetailsFlyout.png)

- Die geschätzte Anzahl und Größe der Elemente, die den Suchkriterien entsprechen.

- Die Anzahl und Größe von teilweise indizierten Elementen (auch als nicht indizierte *Elemente*bezeichnet), die nicht durchsuchbar sind, aber in den Inhaltsspeicherorten gefunden wurden, die in der Suche enthalten waren.

- Die Anzahl der Postfächer und Websites, die durchsucht wurden.

Wenn Sie detailliertere Statistiken anzeigen möchten, klicken Sie auf der Seite Suchdetails-Flyout auf **Statistiken** . Auf der Seite **Suchstatistiken** können Sie die Suchzusammenfassung, den Top-Speicherort mit Elementen, die mit den Suchergebnissen übereinstimmen, sowie detaillierte Statistiken zur Suchabfrage anzeigen.

![Dropdownliste für Suchstatistiken](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a>Zusammenfassung

In der **Zusammenfassungs** Ansicht können die Suchergebnisse nach Standorttyp aufgeschlüsselt angezeigt werden (beispielsweise sind Speicherorte Exchange-Postfächer und SharePoint-Websites). Die folgenden Informationen werden für jeden Standorttyp angezeigt:

- Die Anzahl der Standorte mit Elementen, die den Suchkriterien entsprechen.

- Die Gesamtzahl der Elemente aus jedem Speicherorttyp, die den Suchkriterien entsprechen.

- Die Gesamtgröße der Elemente aus jedem Speicherorttyp, die den Suchkriterien entsprechen.

## <a name="top-locations"></a>Top-Standorte

In der Ansicht der **oberen Speicherorte** werden die einzelnen inhaltsspeicherorte mit den meisten Elementen angezeigt, die den Suchkriterien entsprechen. Für jeden Inhaltsspeicherort werden die folgenden Informationen angezeigt:

- Der Name des Speicherorts; die e-Mail-Adresse für Postfächer und die URL für SharePoint-Websites

- Der Speicherorttyp

- Anzahl der Elemente, die den Suchkriterien entsprechen

- Die Gesamtgröße aller Elemente, die den Suchkriterien entsprechen.

## <a name="queries"></a>Abfragen

In der Ansicht **Abfragen** können Sie detaillierte Statistiken für jede Komponente der Suchabfrage anzeigen. Wenn Sie die Stichwortliste in der Suchabfrage verwendet haben, können Sie in der Ansicht **Abfragen** Erweiterte Statistiken anzeigen, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern oder Schlüsselwörtern übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Teile der Abfrage am meisten (und am wenigsten) effektiv sind. 

Die folgenden Informationen werden in der Ansicht **Abfragen** angezeigt:

 - **Speicherorttyp** – der Typ des Inhaltsspeicherorts für die in der Zeile angezeigten Statistiken.

- **Teil-in** dieser Spalte wird einer der folgenden Werte angezeigt: **Primary** oder **Keyword**. **Primary** bedeutet, dass die Zeile Statistiken über die gesamte Abfrage darstellt. **Stichwort** : die Statistiken in der Zeile gelten für eine der Abfragekomponenten.

- **Condition** – die tatsächliche Abfragekomponente der Suchabfrage, auf die sich die Zeile bezieht. Wenn der Wert in der Spalte **Teilen** **primär**ist, werden die Statistiken für die gesamte Suchabfrage angezeigt; Wenn der Wert **Schlüsselwort**ist, wird die Statistik für die Komponente der Abfrage angezeigt, die in der Spalte **Abfrage** angezeigt wird. Wenn beispielsweise die Stichwortliste verwendet wurde, wird die Statistik eines der Schlüsselwörter angezeigt.

  Im folgenden finden Sie weitere Informationen zu den in der Spalte **Abfragen** angezeigten Statistiken:
  
  - Wenn Sie nach allen Inhalten in Postfächern suchen (indem Sie keine Schlüsselwörter angeben), lautet die tatsächliche Abfrage **(Größe > = 0)** , sodass alle Elemente zurückgegeben werden.
  
  - Beim Durchsuchen von SharePoint-und OneDrive-Websites werden der Suchabfrage die beiden folgenden Komponenten hinzugefügt:
    
    **Nicht IsExternalContent: 1** -Dies schließt Inhalte aus einer lokalen SharePoint-Organisation aus.
    
    **Nicht isOneNotePage: 1** -Dies schließt alle OneNote-Dateien aus, da es sich dabei um Duplikate eines Dokuments handeln würde, das mit der Suchabfrage übereinstimmt.

- **Standorte in der Suche** Die Anzahl der inhaltsspeicherorte mit Elementen, die mit der Suchabfrage für die in der Zeile angezeigte Komponente/Bedingung übereinstimmen. Beachten Sie, dass Archivpostfächer als separater Speicherort gezählt werden, wenn Sie Elemente enthalten, die den Suchkriterien entsprechen.

- **Items** – die Gesamtzahl der Elemente, die mit den Suchkriterien für die in der Zeile angezeigte Komponente/Bedingung übereinstimmen.

- **Size** – die Gesamtzahl der Elemente, die mit den Suchkriterien für die in der Zeile angezeigte Komponente/Bedingung übereinstimmten.
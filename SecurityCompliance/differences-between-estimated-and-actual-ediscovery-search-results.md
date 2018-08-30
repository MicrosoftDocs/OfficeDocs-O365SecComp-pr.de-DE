---
title: Unterschiede zwischen geschätzten und tatsächlichen eDiscovery-Suchergebnissen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/13/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 8f20ca4f-a908-46ec-99e6-9890d269ecf2
description: 'Verstehen Sie, warum geschätzten und tatsächlichen Suchergebnisse in Suchvorgängen, die mit den eDiscovery-Tools in Office 365 variieren. '
ms.openlocfilehash: 15fd34fc4b2f7edaa4020043d3dd7ffc21d643ad
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528874"
---
# <a name="differences-between-estimated-and-actual-ediscovery-search-results-in-office-365"></a>Unterschiede zwischen geschätzten und tatsächlichen eDiscovery-Suchergebnissen in Office 365

Dieses Thema bezieht sich auf Suchvorgänge, die mit einer der folgenden Microsoft eDiscovery Tools ausgeführt werden können:  <br/>  
- Content-Suche in der Office 365-Sicherheit &amp; Compliance Center  <br/>  
- Compliance-eDiscovery in der Exchange-Verwaltungskonsole (EAC)  <br/>  
- Das eDiscovery Center in SharePoint Online  <br/> 
   
Wenn Sie eine eDiscovery-Suche ausführen, wird das Tool verwendeten eine Schätzung der die Anzahl der Elemente (und deren Gesamtgröße), die die Suchkriterien erfüllen zurück. Beispielsweise beim Ausführen einer Suche in das Wertpapier &amp; Compliance Center, die geschätzte Suche Ergebnisse im Detailbereich für die ausgewählte Suche angezeigt werden.
  
![Schätzung der Ergebnisse wird im Detailbereich der ausgewählten Suche angezeigt](media/74e4ce83-40be-41a9-b60f-5ad447e79fe4.png)
  
Dies ist die gleiche Schätzung der Gesamtgröße und-Anzahl der Objekte, die angezeigt wird, in die eDiscovery-Exportprogramm beim Exportieren von Ergebnissen in einem lokalen Computer und im Bericht Summary exportieren, der mit den Suchergebnissen heruntergeladen wird.
  
**Geschätzte Ergebnisse in der eDiscovery-Exportprogramm**

![Geschätzte Ergebnisse im eDiscovery-Exporttool](media/d34312a5-0ee6-49aa-9460-7ea0015a6e66.png)
  
**Geschätzte Ergebnisse im Zusammenfassungsbericht exportieren**

![Geschätzte Suchergebnisse sind im Exportzusammenfassungsbericht enthalten.](media/44b579da-86c2-4f33-81b5-84d604003eda.png)
  
Wie Sie in der vorherigen Screenshot des Berichts exportieren Zusammenfassung bemerken werden, unterscheiden sich jedoch die Größe und Anzahl der eigentlichen Suchergebnisse, die tatsächlich heruntergeladen werden als die Größe und Anzahl der geschätzten Suchergebnisse. 
  
![Unterschied zwischen geschätzten und heruntergeladenen Suchergebnissen](media/84aef318-230f-430d-9d9e-02f21342d364.png)
  
Es folgen einige Gründe für die folgenden Unterschiede:
  
- **Die Anzeige von Ergebnissen werden geschätzt** - eine Schätzung der Suchergebnisse sind genau das, eine Schätzung (und keine Zählung) der Elemente, die die Abfrage Suchkriterien erfüllen. Um die Schätzung des Exchange-Elementen kompiliert werden sollen, wird eine Liste der IDs, die den Suchkriterien entsprechen-Nachricht aus der Exchange-Datenbank vom Tool eDiscovery angefordert verwendeten. Aber wenn Sie die Suchergebnisse exportieren, Erneutes Ausführen der Suche und die tatsächlichen Nachrichten aus der Exchange-Datenbank abgerufen werden. Diese Unterschiede also möglicherweise aufgrund wie die geschätzte Anzahl der Elemente und die tatsächliche Anzahl von Elementen festgelegt werden. 
    
- **Änderungen, die zwischen dem Zeitpunkt vorkommen, wenn schätzen und Exportieren von Suchergebnissen** - Wenn Sie Suchergebnisse exportieren, wird die Suche neu gestartet, um diese neuesten Elemente im Suchindex zu erfassen, die die Suchkriterien erfüllen. Es ist möglich, es sind weitere Elemente erstellt wurden, Ihren gesendeten oder empfangenen, die Suchkriterien erfüllen, die in der Zeit zwischen Wenn der geschätzten Suchergebnisse gesammelt wurden, und wenn die Suchergebnisse exportiert wurden. Es ist außerdem möglich, dass Elemente, die im Suchindex waren, wenn die Suchergebnisse geschätzt wurden nicht mehr verfügbar sind, da sie von der Inhaltsspeicherort gelöscht wurden, bevor die Suchergebnisse exportiert werden. Eine Möglichkeit, dieses Problem ist ein Datumsbereich für eine eDiscovery-Suche an. Eine weitere Möglichkeit ist einen Haltestatus auf Speicherorte für Inhalte zu platzieren, sodass Elemente beibehalten werden und nicht gelöscht werden. 
    
- **Nicht-indizierten Elementen** - Elemente, die für die Suche nicht indizierten sind können Unterschiede zwischen geschätzten und tatsächlichen Suchergebnisse verursachen. Beispielsweise enthalten In-Place eDiscovery in Exchange und das eDiscovery Center in SharePoint nicht indizierten Elemente (, die den Suchkriterien entsprechen nicht) beim Ausführen einer Suche auf die Suchergebnisse schätzen. Aber Sie können nicht indizierter Elemente einschließen, wenn Sie die Suchergebnisse exportieren. Wenn Sie beim Exportieren von Suchergebnissen nicht indizierter Elemente einschließen, liegt möglicherweise weitere Elemente, die exportiert werden. Dadurch wird einen Unterschied zwischen den geschätzten und exportierten Suchergebnisse. 
    
    Wenn Sie das Tool für die Inhaltssuche in das Wertpapier verwenden &amp; Compliance Center, Sie haben die Möglichkeit, nicht-indizierten Elemente in die Schätzung für das Search enthalten. Die Anzahl von nicht-indizierten Elementen, die von der Suche zurückgegebenen wird im Detailbereich zusammen mit der geschätzten Suchergebnisse aufgeführt. Alle nicht-indizierten Elementen würde auch in die Gesamtgröße der geschätzten Suchergebnisse enthalten sein. Wenn Sie die Suchergebnisse exportieren, müssen Sie die Option zum ein- oder nicht indizierten Elemente einschließen. Wie Sie diese Optionen konfigurieren können dazu führen, Unterschiede zwischen geschätzt und die eigentlichen Suchergebnisse werden heruntergeladen. 
    
- **Exportieren Sie die Ergebnisse der Suche Inhalte, die alle Speicherorte für Inhalte enthält** – Wenn die Suche, der Sie Ergebnisse aus exportieren war eine Suche alle Speicherorte für Inhalte in Ihrer Organisation, und klicken Sie dann auf nur nicht-indizierten Elementen Speicherorte für Inhalte, die enthalten Elemente, die den Suchkriterien entsprechen, werden exportiert. Anders ausgedrückt, wenn keine Suchergebnisse in einem Postfach oder Website gefunden werden, wird nicht klicken Sie dann alle nicht-indizierten Elemente in diesem Postfach oder Website exportiert werden. Nicht-indizierten Elemente aus allen Speicherorte für Inhalte (auch die, die keine Elemente enthalten, die die Suchabfrage entsprechen) werden jedoch in der geschätzten Suchergebnisse enthalten sein. 
    
    Alternativ, wenn die Suche, der Sie Ergebnisse aus exportieren auf bestimmte Speicherorte für Inhalte enthalten, werden dann nicht indizierter Elemente (, die durch die Suchkriterien ausgeschlossen werden nicht) aus alle die Speicherorte für Inhalte in der Suche angegebenen exportiert. In diesem Fall sollte die geschätzte Anzahl der nicht-indizierten Elemente und die Anzahl der nicht-indizierten tatsächlich exportierte Elemente identisch sein.
    
    Der Grund für das Exportieren von nicht indizierten Elementen von jedem Standort in der Organisation ist, da es möglicherweise die Wahrscheinlichkeit der Export Fehler erhöhen und, die lange es, die dauert erhöhen zu exportieren, und Laden Sie die Suchergebnisse.
    
- **Roh-Dateiformate im Vergleich zu exportierten Dateien in Dateiformaten** – für Exchange-Elementen, die geschätzte Größe der Suchergebnisse wird mithilfe der rohen Exchange Nachrichtengrößen berechnet. E-Mail-Nachrichten werden jedoch exportiert in eine PST-Datei oder als einzelne Nachrichten (die als EML-Dateien formatiert sind). Beide der folgenden Export Optionen verwenden einer anderen Datei formatieren, unformatierte Exchange-Nachrichten, die in die Gesamtgröße der exportierten Dateigröße wird anders als die geschätzte Dateigröße erzeugt. 
    
- **Dokumentversionen** – für SharePoint-Dokumente, mehrere Versionen eines Dokuments werden nicht in der geschätzten Suchergebnisse enthalten. Aber Sie haben die Möglichkeit, alle Dokumentversionen einschließen aus, wenn Sie die Suchergebnisse exportieren, die tatsächliche Anzahl (und der Gesamtgröße) der exportierten Dokumente erhöht wird. 
    
- **Deduplizierung** - Elemente für Exchange, Deduplizierung verringert die Anzahl der Elemente, die exportiert werden. Sie haben die Möglichkeit, die Suchergebnisse Deduplizierung, wenn Sie sie exportieren. Für Exchange-Nachrichten bedeutet dies, dass nur eine einzige Instanz einer Nachricht exportiert wurde, obwohl dieser Nachricht in mehreren Postfächern gefunden werden kann. Der geschätzten Suchergebnisse einschließen jede Instanz einer Nachricht. Damit Sie die Option Deduplizierung beim Exportieren von Suchergebnissen auswählen, die tatsächliche Anzahl von Elementen, die exportiert werden erheblich kleiner als die geschätzte Anzahl der Elemente werden könnte. 
    
    Im Hinterkopf behalten, wenn die Option Deduplizierung ausgewählt ist, dass alle Exchange-Elemente in einer einzigen PST-Datei exportiert werden und die Ordnerstruktur aus der Quellpostfächer wird nicht beibehalten. Die exportierte PST-Datei enthält nur die e-Mail-Elemente. Ein Bericht der Suchergebnisse enthält jedoch einen Eintrag für jede exportierte Nachricht, die das Quellpostfach identifiziert, wo sich die Nachricht befindet. Dadurch werden alle Postfächer zu identifizieren, die eine doppelte Nachricht enthalten. Wenn Sie nicht Deduplizierung aktivieren, wird für jedes Postfach in der Suche enthalten eine separate PST-Datei exportiert. 
    
## <a name="exporting-unindexed-items-from-the-ediscovery-center-in-sharepoint-online"></a>Exportieren von nicht-indizierten Elementen aus dem eDiscovery Center in SharePoint Online

In der eDiscovery Center in SharePoint Online, haben Sie die Option zum Einschließen von nicht-indizierten Inhalt (von Exchange und SharePoint) beim Exportieren Sie die Ergebnisse einer eDiscovery-Suche. Zu diesem Zweck auswählen der Option **Elemente einschließen, die verschlüsselt werden, oder ein unbekanntes Format besitzen** . Nicht indizierte Elemente (auch als uncrawlable in SharePoint bezeichnet) sind Elemente in Exchange und SharePoint, die aus irgendeinem Grund für die Suche indiziert wurden nicht. Nicht-indizierten Exchange-Elemente werden im Bericht **Exchange Indexfehler** aufgeführt, die beim Exportieren von Suchergebnissen enthalten ist. In ähnlicher Weise werden nicht indizierten SharePoint-Elemente in **SharePoint Indexfehler** Bericht aufgeführt. Wenn Sie nicht-indizierten Elementen exportieren, sind sie in einen Ordner namens **Uncrawlable**heruntergeladen. Nicht-indizierten Exchange-Elemente sind in eine PST-Datei enthalten; jedes nicht indizierten Dokument von SharePoint wird zu heruntergeladen. Die Anzahl der nicht-indizierten Elemente (sofern vorhanden) werden in jeder Index Fehler Bericht aufgeführt. Die Anzahl von nicht-indizierten Elementen in den Berichten sollte die Anzahl von nicht-indizierten Elementen entsprechen, die heruntergeladen werden. 
  
 **Was einige Gründe aufgeführt sind, wenn die Anzahl der exportierten nicht indizierter Elemente die Anzahl von Elementen im Index Fehlerbericht nicht übereinstimmen?** Wie bereits erklärt ist es möglich, dass Elemente gelöscht wurden von Office 365 zwischen dem Zeitpunkt der Ausführung der Suche Estimate und Zeitpunkt, zu dem die Suchergebnisse exportiert wurden. Eine ähnliche Abweichung kann für nicht-indizierten Elementen auftreten. Beispielsweise möglicherweise der Suchindex out-Datum sein, wenn Suchergebnisse exportiert werden. Dies bedeutet, dass ein nicht-indizierten Element, das mit den Suchergebnissen exportiert wurde nicht im Index Fehler Bericht aufgeführt sind, da das Element zur Zeit indiziert wurde nicht die Ergebnisse der exportiert wurden. Dies führt zu mehr nicht indizierten Elementen Export wird, als im Index Fehlerbericht aufgeführt sind. In ähnlicher Weise konnte ein nicht-indizierten Element in den Fehlerbericht Index aufgeführten von Office 365 gelöscht wurden vor der Suchindex aktualisiert wurde. Dies führt zu weniger nicht indizierten Elementen Export wird, als im Index Fehlerbericht aufgeführt sind. 
  
> [!NOTE]
> Wenn Sie nicht auswählen die Option **Elemente einschließen, die verschlüsselt sind oder ein unbekanntes Format,** beim Exportieren Suchergebnisse oder die Berichte nur herunterladen, die Index-Fehlerberichte heruntergeladen werden dabei jedoch keine Einträge. Dies bedeutet nicht, dass keine Indizierung Fehler vorhanden sind. Es also nur nicht-indizierten Elementen in den Export berücksichtigt wurden. 
  


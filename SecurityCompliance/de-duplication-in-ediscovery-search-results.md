---
title: Deduplizierung in eDiscovery-Suchergebnissen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: Sie haben die Möglichkeit, eDiscovery-Suchergebnissen Entfernung von Duplikaten, die exportiert werden, sodass nur eine Kopie einer e-Mail-Nachricht exportiert werden, auch wenn mehrere Instanzen derselben Nachricht in verschiedenen Postfächern möglicherweise gefunden wurden.
ms.openlocfilehash: 5e54f0e5841fdbd29d1ab8b6b9509ff06e827920
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038008"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>Deduplizierung in eDiscovery-Suchergebnissen

Dieser Artikel beschreibt die Funktionsweise von eDiscovery-Suchergebnissen Deduplizierung und erläutert die Einschränkungen des Algorithmus Deduplizierung.
  
Wenn Sie eDiscovery-Tools für Office 365 mit der Ergebnisse einer eDiscovery-Suche exportiert werden, müssen Sie die Option aus, um die Ergebnisse Entfernung von Duplikaten, die exportiert werden. Was bedeutet das? Wenn Sie die Deduplizierung aktivieren (standardmäßig Deduplizierung ist nicht aktiviert), nur eine Kopie einer e-Mail-Nachricht wird exportiert, auch wenn mehrere Instanzen derselben Nachricht Postfächer gefunden wurden möglicherweise, die durchsucht wurden. Deduplizierung können Sie die Zeitersparnis durch Verringern der Anzahl der Elemente, die Sie überprüfen und analysieren, nachdem die Suchergebnisse exportiert werden müssen. Aber es ist wichtig, zu verstehen, wie Deduplizierung und beachten Sie, dass sind Einschränkungen des Algorithmus, die ein eindeutiges Element als ein Duplikat gekennzeichnet werden, während des Exportvorgangs verursachen können.
  
## <a name="how-duplicate-messages-are-identified"></a>Wie doppelte Nachrichten identifiziert werden

Office 365 eDiscovery Tools verwenden eine Kombination der folgenden e-Mail-Eigenschaften bestimmt, ob eine Nachricht ein Duplikat ist:
  
- **InternetMessageId** - diese Eigenschaft gibt die Internetnachricht-ID einer e-Mail-Nachricht, die einen global eindeutigen Bezeichner ist, der auf eine bestimmte Version von einer bestimmten Nachricht verweist. Diese ID wird generiert, indem der Adresse des Absenders e-Mail-Clientprogramm oder Host-e-Mail-System, die die Nachricht sendet. Wenn eine Person eine Nachricht an mehrere Empfänger sendet, wird die Internetnachrichten-ID für jede Instanz der Nachricht identisch sein. Nachfolgende Überarbeitungen auf die ursprüngliche Nachricht erhalten einen andere Meldung-Bezeichner. 
    
- **ConversationTopic** - Eigenschaftswert gibt den Betreff des Unterhaltungsthreads einer Nachricht an. Der Wert der **ConversationTopic** -Eigenschaft ist die Zeichenfolge, die im allgemeine Thema der Unterhaltung beschreibt. Eine Erhaltung umfasst eine anfängliche Nachricht und alle Nachrichten, die in der Antwort auf die ursprüngliche Nachricht gesendet. Nachrichten innerhalb der gleichen Unterhaltung haben den gleichen Wert für die **ConversationTopic** -Eigenschaft. Der Wert dieser Eigenschaft ist in der Regel die Betreffzeile aus der ursprünglichen Nachricht, die die Unterhaltung erzeugt. 
    
- **BodyTagInfo** - Dies ist eine interne Exchange-Speicher-Eigenschaft. Der Wert dieser Eigenschaft wird durch die Überprüfung auf verschiedene Attribute im Textkörper der Nachricht berechnet. Diese Eigenschaft wird verwendet, um Unterschiede im Textkörper der Nachrichten zu identifizieren. 
    
Während des Exportvorgangs eDiscovery werden diese drei Eigenschaften für jede Nachricht verglichen, die den Suchkriterien entspricht. Wenn diese Eigenschaften für zwei (oder mehrere) Nachrichten identisch sind, werden diese Nachrichten werden Duplikate bestimmt und das Ergebnis ist, dass nur eine Kopie der Nachricht exportiert werden sollen, wenn die Deduplizierung aktiviert ist. Die Nachricht, die exportiert wird, wird als "Quellelement" bezeichnet. Informationen zu doppelten Nachrichten ist in der **Results.csv** und die **Datei Manifest.xml** Berichte enthalten, die mit der exportierten Suchergebnisse enthalten sind. In der Datei **Results.csv** wird eine doppelte Nachricht durch einen Wert in der Spalte **doppelte Element** identifiziert. Der Wert in dieser Spalte entspricht dem Wert in der Spalte **Elementidentität** für die Nachricht, die exportiert wurde. 
  
In der folgenden Grafik anzeigen wie doppelte Nachrichten werden in den **Results.csv** und die **Datei Manifest.xml** -Berichten, die mit den Suchergebnissen exportiert werden angezeigt. Diese Berichte umfassen keine e-Mail-Eigenschaften, die zuvor beschrieben, die in der Deduplizierung-Algorithmus verwendet werden. Stattdessen können die Berichte die **Element-Identity** -Eigenschaft, die vom Exchange-Informationsspeicher Elementen zugewiesen ist. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Results.csv Bericht (in Excel angezeigt)
  
![Anzeigen von Informationen zu doppelten Elementen, die im Bericht Results.csv](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Manifest.XML-Bericht (in Excel angezeigt)
  
![Anzeigen von Informationen zu doppelten Elementen, die im Bericht "Manifest.xml"](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
Darüber hinaus sind andere Eigenschaften von doppelten Nachrichten in der Export-Berichte enthalten. Dazu gehört das Postfach-doppelte Nachrichten in, befindet sich, ob die Nachricht an eine Verteilergruppe gesendet wurde und ob die Nachricht war, würde der Cc oder Bcc'd an einen anderen Benutzer.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>Einschränkungen des Algorithmus Deduplizierung

Es gibt einige bekannten Einschränkungen des Algorithmus Deduplizierung, der eindeutige Elemente als Duplikate gekennzeichnet abrufen verursachen können. Es ist wichtig, diese Grenzen verstehen, sodass Sie entscheiden können, ob das optionale Deduplizierung-Feature verwenden.
  
Es gibt eine Situation, in dem das Feature Deduplizierung möglicherweise versehentlich Identifizieren einer Nachricht als ein Duplikat und nicht zu exportieren (jedoch nennen es weiterhin als Duplikat in den Export-Berichten). Hierbei handelt es sich um Nachrichten, die ein Benutzer bearbeitet, aber nicht senden. Nehmen wir beispielsweise an einen Benutzer wählt eine Nachricht in Outlook, kopiert den Inhalt der Nachricht und fügt sie anschließend in einer neuen Nachricht. Ändert sich der Benutzer eine Kopien durch Entfernen oder Hinzufügen einer Anlage oder ändern die Betreffzeile oder dem Nachrichtentext selbst. Wenn die beiden Nachrichten der Abfrage einer eDiscovery-Suche übereinstimmen, wird nur eine der Nachrichten exportiert werden, wenn Deduplizierung aktiviert wird, wenn die Suchergebnisse exportiert werden. Also, obwohl die ursprüngliche Nachricht oder die kopierte Nachricht geändert wurde, keines der überarbeiteten Nachrichten gesendet wurden und daher die Werte der Eigenschaften **InternetMessageId**, **ConversationTopic** und **BodyTagInfo** waren nicht aktualisiert. Aber wie bereits erklärt, werden beide Nachrichten in den Export-Berichten angezeigt werden 
  
Beachten Sie, dass eindeutige Nachrichten auch als Duplikate gekennzeichnet werden können, wenn das Kopie bei Schreibvorgang Seite Protection-Feature aktiviert ist, wie die Groß-/Kleinschreibung eines Postfachs, Beweissicherungsverfahren oder Compliance-Archiv. Das Feature Kopie bei Schreibvorgang kopiert die ursprüngliche Nachricht (und speichert ihn im Ordner Versionen des Benutzerordner wiederherstellbare Elemente), bevor die Überarbeitung ursprünglichen Element gespeichert wird. In diesem Fall der überarbeiteten Kopie und der ursprünglichen Nachricht (im Ordner "wiederherstellbare Elemente") als doppelte Nachrichten betrachtet werden können, und daher nur eine von ihnen exportiert werden würde.
  
> [!IMPORTANT]
> Wenn die Einschränkungen des Algorithmus Deduplizierung für die Qualität Ihrer Suchergebnisse beeinträchtigen könnten, sollte nicht Sie beim Exportieren Deduplizierung aktivieren. Wenn Sie die in diesem Abschnitt beschriebenen Situationen sind wahrscheinlich keinen Faktor in den Suchergebnissen angezeigt werden, und die Anzahl der Elemente, die am ehesten Duplikate reduziert werden soll, sollten Sie erwägen, Deduplizierung aktivieren. 
  
## <a name="more-information"></a>Weitere Informationen

- Die Informationen in diesem Artikel gilt beim Exportieren von Suchergebnissen mithilfe eines der folgenden eDiscovery-Tools:
    
  - Content-Suche in der Office 365-Sicherheit &amp; Compliance Center
    
  - Compliance-eDiscovery in Exchange Online
    
  - Das eDiscovery Center in SharePoint Online
    
- Weitere Informationen zum Exportieren von Suchergebnissen finden Sie unter:
    
  - [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
  - [Exportieren ein Berichts Inhaltssuche aus der Office 365-Sicherheit &amp; Compliance Center](export-a-content-search-report.md)
    
  - [Exportieren von Compliance-eDiscovery-Suchergebnisse in eine PST-Datei](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [Exportieren von Inhalten und Erstellen von Berichten im eDiscovery Center](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)

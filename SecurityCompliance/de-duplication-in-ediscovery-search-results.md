---
title: Deduplizierung in eDiscovery-Suchergebnissen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: Sie haben die Möglichkeit, eDiscovery-Suchergebnisse zu deduplizieren, die exportiert werden, damit nur eine Kopie einer e-Mail-Nachricht exportiert wird, obwohl mehrere Instanzen derselben Nachricht in unterschiedlichen Postfächern gefunden wurden.
ms.openlocfilehash: a8615a1a6504bd9eb4848af89eb3bf1aec52cad2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220385"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>Deduplizierung in eDiscovery-Suchergebnissen

In diesem Artikel wird beschrieben, wie die Deduplizierung von eDiscovery-Suchergebnissen funktioniert und wie die Einschränkungen des Algorithmus für die Deduplizierung erläutert werden.
  
Wenn Sie die Ergebnisse einer eDiscovery-Suche mithilfe von Office 365 eDiscovery-Tools exportieren, haben Sie die Möglichkeit, die exportierten Ergebnisse zu deduplizieren. Was bedeutet das? Wenn Sie Deduplizierung aktivieren (Deduplizierung ist standardmäßig nicht aktiviert), wird nur eine Kopie einer e-Mail-Nachricht exportiert, obwohl in den durchsuchten Postfächern möglicherweise mehrere Instanzen derselben Nachricht gefunden wurden. Durch die Deduplizierung können Sie Zeit sparen, indem Sie die Anzahl der Elemente verringern, die Sie nach dem Export der Suchergebnisse überprüfen und analysieren müssen. Es ist jedoch wichtig zu verstehen, wie Deduplizierung funktioniert, und dass es Einschränkungen für den Algorithmus gibt, die dazu führen können, dass ein eindeutiges Element während des Exportvorgangs als Duplikat gekennzeichnet wird.
  
## <a name="how-duplicate-messages-are-identified"></a>Identifizieren von doppelten Nachrichten

Office 365 eDiscovery-Tools verwenden Sie eine Kombination der folgenden e-Mail-Eigenschaften, um zu bestimmen, ob eine Nachricht ein Duplikat ist:
  
- **InternetMessageId** -diese Eigenschaft gibt die Internet Nachrichten-ID einer e-Mail-Nachricht an, bei der es sich um eine global eindeutige ID handelt, die auf eine bestimmte Version einer bestimmten Nachricht verweist. Diese ID wird vom e-Mail-Programm des Absenders oder vom Host-e-Mail-System generiert, das die Nachricht sendet. Wenn eine Person eine Nachricht an mehrere Empfänger sendet, ist die Internet Nachrichten-ID für jede Instanz der Nachricht identisch. Nachfolgende Überarbeitungen an der ursprünglichen Nachricht erhalten einen anderen Nachrichtenbezeichner. 
    
- **ConversationTopic** -seine Eigenschaft gibt den Betreff des Konversations Threads einer Nachricht an. Der Wert der **ConversationTopic** -Eigenschaft ist die Zeichenfolge, die das allgemeine Thema der Unterhaltung beschreibt. Eine Konservierung besteht aus einer anfänglichen Nachricht und allen Nachrichten, die als Antwort auf die ursprüngliche Nachricht gesendet wurden. Nachrichten innerhalb der gleichen Unterhaltung haben den gleichen Wert für die **ConversationTopic** -Eigenschaft. Der Wert dieser Eigenschaft ist in der Regel die Betreffzeile der ersten Nachricht, die die Unterhaltung hervorgebracht hat. 
    
- **BodyTagInfo** – hierbei handelt es sich um eine interne Exchange-Speichereigenschaft. Der Wert dieser Eigenschaft wird berechnet, indem verschiedene Attribute im Textkörper der Nachricht überprüft werden. Diese Eigenschaft wird verwendet, um Unterschiede im Nachrichtentext zu identifizieren. 
    
Während des eDiscovery-Exportvorgangs werden diese drei Eigenschaften für jede Nachricht verglichen, die den Suchkriterien entspricht. Wenn diese Eigenschaften für zwei (oder mehr) Nachrichten identisch sind, werden diese Nachrichten als Duplikate festgelegt, und das Ergebnis ist, dass nur eine Kopie der Nachricht exportiert wird, wenn Deduplizierung aktiviert ist. Die exportierte Nachricht wird als "Quellelement" bezeichnet. Informationen zu doppelten Nachrichten sind in den Berichten **results. CSV** und **Manifest. XML** enthalten, die in den exportierten Suchergebnissen enthalten sind. In der Datei **results. CSV** wird eine doppelte Nachricht durch einen Wert in der Spalte Duplikat in **Element** identifiziert. Der Wert in dieser Spalte entspricht dem Wert in der Spalte **Element Identität** für die Nachricht, die exportiert wurde. 
  
Die folgende Grafik zeigt, wie doppelte Nachrichten in den Berichten **results. CSV** und **Manifest. XML** angezeigt werden, die mit den Suchergebnissen exportiert werden. Diese Berichte beziehen sich nicht auf die zuvor beschriebenen e-Mail-Eigenschaften, die im Deduplizierungs-Algorithmus verwendet werden. Stattdessen enthält die Berichte die **Element Identitäts** Eigenschaft, die Elementen vom Exchange-Speicher zugewiesen wird. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Results. CSV-Bericht (in Excel angezeigt)
  
![Anzeigen von Informationen zu doppelten Elementen im Bericht "results. csv"](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Manifest. XML-Bericht (in Excel angezeigt)
  
![Anzeigen von Informationen zu doppelten Elementen im Manifest. XML-Bericht](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
Darüber hinaus sind andere Eigenschaften aus doppelten Nachrichten in den Export Berichten enthalten. Dies umfasst das Postfach, in dem sich die doppelte Nachricht befindet, ob die Nachricht an eine Verteilergruppe gesendet wurde und ob die Nachricht von CC 'd oder Bcc an einen anderen Benutzer übermittelt wurde.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>Einschränkungen des Deduplizierungs-Algorithmus

Es gibt einige bekannte Einschränkungen des Deduplizierungs-Algorithmus, die dazu führen können, dass eindeutige Elemente als Duplikate gekennzeichnet werden. Es ist wichtig, diese Einschränkungen zu verstehen, damit Sie entscheiden können, ob die optionale Deduplizierung verwendet werden soll.
  
Es gibt eine Situation, in der die Deduplizierung eine Nachricht fälschlicherweise als Duplikat identifiziert und nicht exportiert (aber Sie als Duplikat in den Export Berichten zitiert). Hierbei handelt es sich um Nachrichten, die ein Benutzer bearbeitet, aber nicht sendet. Angenommen, ein Benutzer wählt in Outlook eine Nachricht aus, kopiert den Inhalt der Nachricht und fügt Sie dann in eine neue Nachricht ein. Dann ändert der Benutzer eine der Kopien durch Entfernen oder Hinzufügen einer Anlage oder Ändern der Betreffzeile oder des Texts selbst. Wenn diese beiden Nachrichten mit der Abfrage einer eDiscovery-Suche übereinstimmen, wird nur eine der Nachrichten exportiert, wenn Deduplizierung aktiviert ist, wenn die Suchergebnisse exportiert werden. Obwohl also die ursprüngliche Nachricht oder die kopierte Nachricht geändert wurde, wurden keine der überarbeiteten Nachrichten gesendet, und daher wurden die Werte der Eigenschaften **InternetMessageId**, **ConversationTopic** und **BodyTagInfo** nicht aktualisiert. Wie bereits erläutert, werden beide Nachrichten in den Export Berichten aufgeführt. 
  
Beachten Sie, dass eindeutige Nachrichten auch dann als Duplikate gekennzeichnet werden können, wenn die Kopierschutz Funktion aktiviert ist, wie im Fall, dass ein Postfach in einem Rechtsstreit gehalten wird oder in der Lage ist. Die Copy-on-Write-Funktion kopiert die ursprüngliche Nachricht (und speichert Sie im Ordner "Versionen" des Ordners "Wiederherstellbare Elemente" des Benutzers), bevor die Revision des ursprünglichen Elements gespeichert wird. In diesem Fall können die überarbeitete Kopie und die ursprüngliche Nachricht (im Ordner "Wiederherstellbare Elemente") als doppelte Nachrichten betrachtet werden, und daher würde nur einer davon exportiert.
  
> [!IMPORTANT]
> Wenn sich die Einschränkungen des Algorithmus für die Deduplizierung möglicherweise auf die Qualität Ihrer Suchergebnisse auswirken, sollten Sie keine Deduplizierung aktivieren, wenn Sie Elemente exportieren. Wenn die in diesem Abschnitt beschriebenen Situationen wahrscheinlich nicht in ihren Suchergebnissen einen Faktor darstellen und Sie die Anzahl der Elemente verringern möchten, die am ehesten doppelt vorhanden sind, sollten Sie die Deduplizierung aktivieren. 
  
## <a name="more-information"></a>Weitere Informationen

- Die Informationen in diesem Artikel gelten für den Export von Suchergebnissen mithilfe eines der folgenden eDiscovery-Tools:
    
  - Inhaltssuche im Office 365 Security &amp; Compliance Center
    
  - Compliance-eDiscovery in Exchange Online
    
  - Das eDiscovery Center in SharePoint Online
    
- Weitere Informationen zum Exportieren von Suchergebnissen finden Sie unter:
    
  - [Exportieren von Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
  - [Exportieren eines Inhalts Suchberichts aus dem Office 365 Security &amp; Compliance Center](export-a-content-search-report.md)
    
  - [Exportieren von in-Place eDiscovery-Suchergebnissen in eine PST-Datei](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [Exportieren von Inhalten und Erstellen von Berichten im eDiscovery Center](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)

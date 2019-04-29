---
title: Archivieren von drittanbieterdaten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können drittanbieterdaten aus sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen in Postfächer in Ihrer Office 365-Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und anderen drittanbieterdaten Quellen in Office 365 archivieren. Anschließend können Sie die Office 365-Kompatibilitätsfeatures (wie rechtliche Aufbewahrung, eDiscovery, in-situ-Archivierung und Aufbewahrungsrichtlinien) für drittanbieterdaten verwenden und anwenden.
ms.openlocfilehash: b96c4852c3c9226219120a1be014ea3988cf91a2
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402913"
---
# <a name="archive-third-party-data-in-office-365"></a>Archivieren von drittanbieterdaten in Office 365

Office 365 ermöglicht Administratoren das Importieren und Archivieren von drittanbieterdaten von sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen zu Postfächern in Ihrer Office 365-Organisation. Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können, sind folgende: 
  
- **Social** -Twitter, Facebook, jammern und LinkedIn 
    
- **Instant Messaging** -Yahoo Messenger, GoogleTalk und Cisco Jabber 
    
- **Dokument Zusammenarbeit** und Dropbox 
    
- **Vertikale Branchen** -Kundenbeziehungsverwaltung (wie Salesforce Chatter) und Finanzdienstleistungen (wie Bloomberg und Thomson Reuters) 
    
- **SMS/Textnachrichten** -BlackBerry 
    
Nachdem drittanbieterdaten importiert wurden, können Sie diese Daten über die Office 365-Kompatibilitätsfeatures (beispielsweise Rechtsstreit, eDiscovery, in-situ-Archivierung, Überwachung, Überwachung und Office 365-Aufbewahrungsrichtlinien) anwenden. Wenn ein Postfach zum Beispiel dem Beweissicherungsverfahren unterliegt, werden Drittanbieterdaten beibehalten. Mithilfe von Microsoft eDiscovery-Tools können Sie drittanbieterdaten durchsuchen. Oder Sie können (genau wie bei Microsoft-Daten) Archivierungs- und Aufbewahrungsrichtlinien auf Drittanbieterdaten anwenden. Kurz gesagt, die Archivierung von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien kompatibel bleibt.

Es gibt zwei Möglichkeiten zum Importieren und Archivieren von drittanbieterdaten in Office 365:

- **Verwenden eines Drittanbieter-datenkonnektors im Security _AMP_ Compliance Center** – verwenden Sie einen benutzerdefinierten Datenkonnektor, der im Security _AMP_ Compliance Center in Office 365 verfügbar ist. Nachdem Sie den Connector eingerichtet und konfiguriert haben, stellt er eine Verbindung mit der Drittanbieter-Datenquelle her, konvertiert den Inhalt eines Elements in ein e-Mail-Nachrichtenformat und importiert das Element in ein Postfach in Office 365. Informationen zu den von diesen Konnektoren unterstützten drittanbieterdaten Quellen und dem schrittweisen Verfahren zum Einrichten eines Connectors finden Sie unter [use Sample Connectors to Archiv Third-Party Data in Office 365 (Preview)](archive-third-party-data-with-sample-connector.md).

- **Arbeiten mit einem Microsoft-Partner** – Ihre Organisation arbeitet mit einem Microsoft-Partner zusammen, der einen benutzerdefinierten Connector bereitstellt, der zum Extrahieren von Elementen aus der Drittanbieter-Datenquelle konfiguriert wird (in regelmäßigen Abständen) und dann eine Verbindung mit der Microsoft-Cloud über eine API eines Drittanbieters und importieren Sie diese Elemente in Office 365. Der Partner-Konnektor wandelt auch den Inhalt eines Elements aus der Drittanbieter-Datenquelle in eine e-Mail-Nachricht um und importiert Sie dann in ein Postfach in Office 365. Eine Liste der Partner, mit denen Sie arbeiten können, und der schrittweise Prozess für diese Methode finden Sie unter [Arbeiten mit einem Partner zum Archivieren von drittanbieterdaten in Office 365](work-with-partner-to-archive-third-party-data.md).
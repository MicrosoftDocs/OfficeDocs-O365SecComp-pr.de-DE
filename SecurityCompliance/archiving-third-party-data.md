---
title: Archivieren von Drittanbieterdaten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können Daten von Drittanbietern aus Social Media-Plattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen zu Postfächern in Ihrer Office 365 Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und anderen Datenquellen von Drittanbietern in Office 365 archivieren. Anschließend können Sie Office 365 Compliance-Features (wie Legal Hold, eDiscovery, in-situ-Archivierung und Aufbewahrungsrichtlinien) für drittanbieterdaten verwenden und anwenden.
ms.openlocfilehash: 33ce9c0d648d0c247abcaac8838e351d413a1990
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152081"
---
# <a name="archive-third-party-data-in-office-365"></a>Archivieren von Drittanbieterdaten in Office 365

Office 365 können Administratoren drittanbieterdaten aus Social Media-Plattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen in Postfächern in Ihrer Office 365 Organisation importieren und archivieren. Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können, umfassen Folgendes: 
  
- **Social** -Twitter, Facebook, jammern und LinkedIn 
    
- **Instant Messaging** – Yahoo Messenger, GoogleTalk und Cisco Jabber 
    
- **Dokument Zusammenarbeit** -Box und Dropbox 
    
- **Vertikale Branchen** -Kunden Beziehungs Management (beispielsweise Salesforce Chatter) und Finanzdienstleistungen (wie Bloomberg und Thomson Reuters) 
    
- **SMS/Textnachrichten** -BlackBerry 
    
Nachdem Sie Daten von Drittanbietern importiert haben, können Sie Office 365 Compliance-Features wie Beweissicherungsverfahren, eDiscovery, in-situ-Archivierung, Überwachung, Überwachung und Office 365 Aufbewahrungsrichtlinien auf diese Daten anwenden. Wenn ein Postfach zum Beispiel dem Beweissicherungsverfahren unterliegt, werden Drittanbieterdaten beibehalten. Sie können drittanbieterdaten mithilfe von Microsoft eDiscovery-Tools durchsuchen. Oder Sie können (genau wie bei Microsoft-Daten) Archivierungs- und Aufbewahrungsrichtlinien auf Drittanbieterdaten anwenden. Kurz gesagt: das Archivieren von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien konform bleibt.

Es gibt zwei Möglichkeiten zum Importieren und Archivieren von drittanbieterdaten in Office 365:

- **Verwenden Sie einen Drittanbieter-Daten Konnektor im Security & Compliance Center** – verwenden Sie einen benutzerdefinierten Daten Konnektor, der im Security & Compliance Center in Office 365 verfügbar ist. Nachdem Sie den Connector eingerichtet und konfiguriert haben, stellt er eine Verbindung mit der Drittanbieter-Datenquelle her, wandelt den Inhalt eines Elements in ein e-Mail-Nachrichtenformat um und importiert dann das Element in ein Postfach in Office 365. Derzeit können Sie Beispiel-Konnektoren implementieren, um Daten aus Facebook-Geschäfts Seiten und Twitter zu importieren und zu archivieren. Die Schritt-für-Schritt-Anleitung zum Einrichten eines Connectors finden Sie unter:
   
   - **Facebook** - [verwendet einen Beispiel-Konnektor zum Archivieren von Facebook-Daten in Office 365 (Vorschau)](archive-facebook-data-with-sample-connector.md)
  
   - **Twitter** - [Verwenden eines Beispiel-Konnektors zum Archivieren von Twitter-Daten in Office 365 (Vorschau)](archive-twitter-data-with-sample-connector.md)

- **Arbeiten mit einem Microsoft-Partner** – Ihre Organisation arbeitet mit einem Microsoft-Partner zusammen, der einen benutzerdefinierten Connector bereitstellt, der zum Extrahieren von Elementen aus der Drittanbieter-Datenquelle konfiguriert wird (regelmäßig) und dann über eine Verbindung mit der Microsoft-Cloud hergestellt wird. Drittanbieter-API und importieren Sie diese Elemente in Office 365. Der Partner Connector wandelt auch den Inhalt eines Elements aus der Drittanbieter-Datenquelle in eine e-Mail-Nachricht um und importiert diese dann in ein Postfach in Office 365. Eine Liste der Partner, mit denen Sie zusammenarbeiten und den schrittweisen Prozess für diese Methode ausführen können, finden Sie unter [Arbeiten mit einem Partner zum Archivieren von drittanbieterdaten in Office 365](work-with-partner-to-archive-third-party-data.md).
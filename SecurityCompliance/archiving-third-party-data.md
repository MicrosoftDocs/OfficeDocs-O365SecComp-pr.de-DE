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
ms.openlocfilehash: 796ad0314374dca60d1ff5f6b9317be491b757a1
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2019
ms.locfileid: "35014604"
---
# <a name="archive-third-party-data-in-office-365"></a>Archivieren von Drittanbieterdaten in Office 365

Office 365 können Administratoren drittanbieterdaten aus Social Media-Plattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen in Postfächern in Ihrer Office 365 Organisation importieren und archivieren. Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können, umfassen die folgenden Dienste: 
  
- **Social** – Facebook, LinkedIn, Twitter und jammern 
    
- **Instant Messaging** – Yahoo Messenger, GoogleTalk und Cisco Jabber 
    
- **Dokument Zusammenarbeit** – Box und Dropbox 
    
- **Vertikale Branchen** – Kunden Beziehungs Management (beispielsweise Salesforce Chatter) und Finanzdienste (wie Bloomberg und Thomson Reuters) 
    
- **SMS/Textnachrichten** – BlackBerry 
    
Nachdem Sie Daten von Drittanbietern importiert haben, können Sie Office 365 Compliance-Features wie Beweissicherungsverfahren, eDiscovery, in-situ-Archivierung, Überwachung, Überwachung und Office 365 Aufbewahrungsrichtlinien auf diese Daten anwenden. Wenn ein Postfach zum Beispiel dem Beweissicherungsverfahren unterliegt, werden Drittanbieterdaten beibehalten. Sie können drittanbieterdaten mithilfe von Microsoft eDiscovery-Tools durchsuchen. Oder Sie können (genau wie bei Microsoft-Daten) Archivierungs- und Aufbewahrungsrichtlinien auf Drittanbieterdaten anwenden. Kurz gesagt: das Archivieren von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien konform bleibt.

Es gibt zwei Möglichkeiten zum Importieren und Archivieren von drittanbieterdaten in Office 365:

- **Verwenden Sie einen Drittanbieter-Daten Konnektor im Security #a0 Compliance Center** – verwenden Sie einen benutzerdefinierten Daten Konnektor, der im Security #a1 Compliance Center in Office 365 zur Verfügung steht. Nachdem Sie den Connector eingerichtet und konfiguriert haben, stellt er eine Verbindung mit der Drittanbieter-Datenquelle her, wandelt den Inhalt eines Elements in ein e-Mail-Nachrichtenformat um und importiert dann das Element in ein Postfach in Office 365. Zu diesem Zeitpunkt können Sie Connectors zum Importieren und Archivieren von Daten von Facebook-Geschäfts Seiten, Unternehmens Twitter-Konten, Instant Bloomberg und LinkedIn implementieren. Die Schritt-für-Schritt-Anleitung zum Einrichten eines Connectors finden Sie unter:
   
   - **Facebook** – [verwenden Sie einen Beispiel-Konnektor, um Facebook-Daten in Office 365 zu archivieren](archive-facebook-data-with-sample-connector.md) .
  
   - **Twitter** – [verwenden Sie einen Beispiel-Konnektor zum Archivieren von Twitter-Daten in Office 365](archive-twitter-data-with-sample-connector.md)
    
   - **LinkedIn** – [Einrichten eines Connectors zum Archivieren von LinkedIn Daten in Office 365](archive-linkedin-data.md)

- **Arbeiten mit einem Microsoft-Partner** – Ihre Organisation arbeitet mit einem Microsoft-Partner zusammen, der einen benutzerdefinierten Connector zur Verfügung stellt, der zum Extrahieren von Elementen aus der Drittanbieter-Datenquelle konfiguriert wird (regelmäßig) und dann über eine Verbindung mit der Microsoft-Cloud hergestellt wird. Drittanbieter-API und importieren Sie diese Elemente in Office 365. Der Partner Connector wandelt auch den Inhalt eines Elements aus der Drittanbieter-Datenquelle in eine e-Mail-Nachricht um und importiert diese dann in ein Postfach in Office 365. Eine Liste der Partner, mit denen Sie zusammenarbeiten und den schrittweisen Prozess für diese Methode ausführen können, finden Sie unter [Arbeiten mit einem Partner zum Archivieren von drittanbieterdaten in Office 365](work-with-partner-to-archive-third-party-data.md).
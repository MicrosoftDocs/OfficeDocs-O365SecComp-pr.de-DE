---
title: Erweiterte Indizierung von Daten für eine Untersuchung
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
ms.openlocfilehash: 9537cf743b89da7167ce3a37a5915027f4eb717a
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030158"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a>Erweiterte Indizierung von Daten für eine Untersuchung

Der Inhalt des Live-Systems kann aus einer Reihe von Gründen teilweise indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen. Wenn Sie mit hohem Risikodaten Überlauf arbeiten, möchten Sie sicherstellen, dass die Suche alle Daten erfasst, die Sie untersuchen möchten. Wenn eine betroffene Person zu einer Datenermittlung hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind. Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet. 

Weitere Informationen zur Verarbeitungsunterstützung in Office 365 und teilweise indizierten Elementen finden Sie unter:

- [Unterstützte Dateitypen in Daten Untersuchungen](supported-filetypes-datainvestigations.md)

- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)

- [Von der Exchange-Suche indizierte Dateiformate](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [Standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Anzeigen erweiterter Indizierungs Ergebnisse

Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.  In der Ansicht Interessen Indizes werden alle Elemente aufgelistet, die dem *Hybrid Index*hinzugefügt wurden.  Der Hybrid Index enthält Daten Untersuchungen (Preview), in denen der erneut verarbeitete Inhalt gespeichert wird.

Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).

## <a name="updating-advanced-indexes-for-people-of-interest"></a>Aktualisieren erweiterter Indizes für Personen von Interesse

Wenn eine Person von Interesse zu einer Datenermittlung hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet. Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.

> [!NOTE]
> Das Aktualisieren von Personen mit interessanten Indizes ist ein langwieriger Prozess. Es wird empfohlen, dass Sie Indizes nicht mehr als einmal pro Tag in einer Untersuchung aktualisieren.

---
title: Erweiterte Indizierung der Daten von Verwaltungsberechtigten
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
ms.openlocfilehash: 1521aadca42c8119ae341065865b227fb16ffcf3
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295028"
---
# <a name="advanced-indexing-of-custodian-data"></a>Erweiterte Indizierung der Daten von Verwaltungsberechtigten

Wenn eine Depotbank zu einem Advanced eDiscovery (Preview)-Fall hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind.  Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet. Inhalte können teilweise aus verschiedenen Gründen indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen.

Weitere Informationen zur Verarbeitungsunterstützung in Office 365 und teilweise indizierten Elementen finden Sie unter:

- [Unterstützte Dateitypen in Advanced eDiscovery](supported-filetypes-ediscovery20.md)
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [Von der Exchange-Suche indizierte Dateiformate](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [Standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Anzeigen erweiterter Indizierungs Ergebnisse

Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.  In der Ansicht Depot Indizierung werden alle dem *Hybrid Index*hinzugefügten Elemente aufgelistet.  Im Hybrid Index werden die neu verarbeiteten Inhalte von Advanced eDiscovery (Preview) gespeichert.

Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Aktualisieren erweiterter Indizes für Verwalter

Wenn einem erweiterten eDiscovery-Fall (Preview) ein Depot hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet. Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.

> [!NOTE]
> Das Aktualisieren von Depot Indizes ist ein langwieriger Prozess. Es wird empfohlen, die Indizes in einem Fall nicht mehr als einmal pro Tag zu aktualisieren.

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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218665"
---
# <a name="advanced-indexing-of-custodian-data"></a>Erweiterte Indizierung der Daten von Verwaltungsberechtigten

Wenn eine Depotbank zu einem Advanced eDiscovery (Preview)-Fall hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind.  Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet. Inhalte können teilweise aus verschiedenen Gründen indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen.  Weitere Informationen zu teilweise indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Anzeigen erweiterter Indizierungs Ergebnisse

Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.  In der Ansicht Depot Indizierung werden alle dem *Hybrid Index*hinzugefügten Elemente aufgelistet.  Im Hybrid Index werden die neu verarbeiteten Inhalte von Advanced eDiscovery (Preview) gespeichert.

Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Aktualisieren erweiterter Indizes für Verwalter

Wenn einem erweiterten eDiscovery-Fall (Preview) ein Depot hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet. Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.

> [!NOTE]
> Das Aktualisieren von Depot Indizes ist ein langwieriger Prozess. Es wird empfohlen, die Indizes in einem Fall nicht mehr als einmal pro Tag zu aktualisieren.

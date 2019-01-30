---
title: Erweiterte Indizierung von Verwaltungsberechtigten Daten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607762"
---
# <a name="advanced-indexing-of-custodian-data"></a>Erweiterte Indizierung von Verwaltungsberechtigten Daten

Wenn ein Verwaltungsberechtigter zu einem Fall erweiterte eDiscovery (Preview) hinzugefügt wird, ist keine Inhalte in Office 365, die als gilt als wurde teilweise indiziert erneut verarbeiteten vollständig durchsuchbare machen.  Dieser Vorgang wird als *erweiterte Indizierung*bezeichnet. Inhalte kann teilweise für eine Reihe von Gründe für das Vorhandensein von Bildern, nicht unterstützte Dateitypen oder bei Auftreten von Indizierung maximale Dateigröße indiziert werden.  Weitere Informationen zum teilweise indizierte Elemente finden Sie unter [teilweise indizierte Elemente in Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Anzeigen von Ergebnissen der erweiterte Indizierung

Nachdem der erweiterte Indizierung abgeschlossen ist, können Sie einen Überblick über die Effektivität des erneute Verarbeitung abrufen.  In der Ansicht Verwaltungsberechtigter Indizierung enthält das Diagramm alle Elemente auf den *Hybriden Index*hinzugefügt.  Der Hybrid-Index ist, wo den Inhalt erneut verarbeiteten auf Erweiterte eDiscovery (Preview) gespeichert werden.

Das Diagramm enthält auch die Anzahl der Elemente, die Remediation erfordern und eine andere Grafik von Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Error Remediation beim Verarbeiten von Daten](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Aktualisieren von erweiterten Indizes für Verwalter

Wenn ein Verwaltungsberechtigter zu einem Fall erweiterte eDiscovery (Preview) hinzugefügt wird, werden alle teilweise indizierte Elemente erneut verarbeitet. Mit der Zeit können mehr teilweise indizierte Elemente Postfach oder OneDrive-Konto des Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.

> [!NOTE]
> Aktualisieren von Indizes Verwaltungsberechtigter ist ein langer Prozess. Es wird empfohlen, dass Sie Indizes nur einmal pro Tag in dem Fall nicht aktualisieren.

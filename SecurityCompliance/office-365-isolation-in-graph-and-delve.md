---
title: Office 365-Mandantenisolation im Büro Diagramm und eingegangen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Eine Erläuterung der mandantenisolation in das Office-Diagramm und Delve.'
ms.openlocfilehash: bdc0f34d558f25ec139861c9a91261a72418f18a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529289"
---
# <a name="tenant-isolation-in-the-office-graph-and-delve"></a>Mandanten Isolation im Büro Diagramm und eingegangen

## <a name="tenant-isolation-in-the-office-graph"></a>Mandantenisolation im Office-Diagramm
Die [Office-Diagramm](https://dev.office.com/officegraph) Modelle Aktivität in Office 365-Dienste, einschließlich Exchange Online, SharePoint Online, Yammer, Skype für Unternehmen, Azure Active Directory und weitere, und externe Dienste, wie andere Microsoft-Dienste oder Drittanbieter-Dienste. Office-Diagramm-Komponenten werden in der gesamten Office 365 verwendet. Das Office-Diagramm stellt eine Auflistung von Inhalt und Aktivitäten und die Beziehungen zwischen ihnen, die über die gesamte Office Suite auftreten. Anspruchsvolle Techniken erlernen Computer verwendet, um Personen mit der relevante Inhalte, Gespräche und Mitarbeiter um verbinden. Beispielsweise der Mandanten Index in SharePoint Online verfügt über den Office-Diagramm Index, mit dem Delve Abfragen dienen, dem Analysemodul Processing in SharePoint Online wird verwendet, um speichern Signale und Insights berechnen und Exchange Online berechnet des Benutzers Empfängercache als Eingabe für Mandanten Analytics.

Das Office-Diagramm enthält Informationen zu Enterprise-Objekten, wie Personen und Dokumenten, als auch die Beziehungen und Interaktionen zwischen diesen Objekten. Die Beziehungen und Interaktionen werden als *Kanten*dargestellt. Im Office-Diagramm ist nach Mandant segmentierte, sodass Kanten nur zwischen *Knoten* in der gleichen Instanz vorhanden sein können. Ein *Knoten* ist eine Entität mit Uniform Resource Identifier (URI), Knotentyp, Zugriffssteuerungsliste und eine Reihe von Facetten, *Metadaten* und Kanten enthält. Jeder Knoten sind Metadaten und Kanten, angeordnet in *Facetten* wie in der allgemeinen Knowledge Modell zugeordnet. *Metadaten* sind benannte Eigenschaften gespeichert, die auf einem Knoten die für die Suche, filtern oder Analyse innerhalb des Office-Diagramms verwendet werden kann. Ein *Aspekt* ist eine logische Sammlung von Metadaten und Ränder auf einen Knoten. Jede Facetten beschreibt einen Aspekt eines Knotens an. 

Das Office-Diagramm bringt nicht alle Daten in einem Repository; Vielmehr speichert sie Metadaten und Beziehungen zu Daten, die an anderer Stelle befindet. Im Office-Diagramm besteht aus mehreren Datenspeichern und Verarbeitungskomponenten:
- Die Mandanten Diagramm Store bietet die Bulk-Speicher für effiziente Analytics optimiert.
- Die aktiven Cache-Inhalt enthält zufällige schnell aktiven Knoten und Kanten auf Laufwerk Benutzererlebnis.
- Der Eingabe Router benachrichtigt Komponenten internen und externen über Änderungen an einem Diagramm Mandanten.

Analytics innerhalb jeder Arbeitslast Einblicke in die gesamte Mandanten Berechnungen für die Überprüfung relevante ableiten, und drücken sie an einem Diagramm Mandanten. Mandanten über alle Aktivitäten eines Mandanten Analytics Gründe für Einblicke in Verhalten, das Muster zu erstellen. Exchange Online wird beispielsweise die Empfängercache für jeden Benutzer mit Analysen, die über das Postfach des Benutzers effizient Grund berechnet. Diese Analytics pro Benutzer erzeugen eine Reihe von *RecipientCache Kanten* auf jede Person, die wiederum dem Mandanten Diagramm abgelegt. Auf diese Weise wird die wie viel die Analytics processing erreicht bald wie möglich die Quelldaten.

## <a name="tenant-isolation-in-delve"></a>Mandantenisolation in ausführlicher behandelt.
Wie bereits erwähnt, das Office-Diagramm eignet sich ideal für Erfahrungen, mit deren Hilfe Benutzer ermitteln und Zusammenarbeit auf aktuellen Aktivitäten in ihrem Unternehmen und bietet eine Entität-centric Plattform für Analytics auf Grund über Inhalt und Aktivität Arbeitslasten und über Office 365. Eingegangen ist der erste solche Erfahrung verfügt über das Office-Diagramm. Eingegangen ist eine Office 365 Web wünschen, die Inhalte von Office 365 und Yammer Enterprise zu Office 365-Benutzer über das Office-Diagramm Flächen. Für die Webbenutzeroberfläche zeigt Daten als unterschiedliche bewertungseinrichtungen, jeweils mit einem bestimmten Thema wie *Trending um mich* oder *geändert von mir*. Jedes Board umfasst mehrere Karten Dokument die Anzeige von zusammengefassten Texts und ein Bild aus dem Dokument. Die Karte kann Benutzer Aktionen wie das Dokument oder eine Seite Yammer für das Dokument zu öffnen. Es ist eine Seite für jede Person in einer Office 365-Mandanten, in dem die zutreffenden Dokumente für diese Person angezeigt und Symbole, die Exchange Online oder Skype für Unternehmen für die Interaktion mit dieser Person aufrufen können. Da Delve auf der Office-Diagramm-API basiert, wird durch die Mandanten-basierte Isolation diese API gebunden.
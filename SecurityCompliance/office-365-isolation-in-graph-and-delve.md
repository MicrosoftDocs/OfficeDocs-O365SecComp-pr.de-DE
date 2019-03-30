---
title: Office 365-Mandanten Isolierung im Office-Diagramm
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine Erläuterung der Mandanten Isolierung im Office-Diagramm und in "einTauchen".'
ms.openlocfilehash: 22bcf581c26ea4e334539a81861ff4dee68967ef
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004202"
---
# <a name="tenant-isolation-in-the-office-graph-and-delve"></a>Mandantenisolation in Office Graph und Delve

## <a name="tenant-isolation-in-the-office-graph"></a>Mandanten Isolierung im Office-Diagramm
Die [Office Graph](https://dev.office.com/officegraph) -Modell Aktivitäten in Office 365-Diensten, einschließlich Exchange Online, SharePoint Online, jammern, Skype for Business, Azure Active Directory und mehr, und in externen Diensten wie anderen Microsoft-Diensten oder Drittanbieterdiensten. Office Graph-Komponenten werden in Office 365 verwendet. Das Office Graph stellt eine Sammlung von Inhalten und Aktivitäten sowie die Beziehungen zwischen diesen dar, die in der gesamten Office-Suite stattfinden. Es verwendet ausgefeilte Techniken des maschinellen Lernens, um Personen mit den relevanten Inhalten, Unterhaltungen und Personen zu verbinden. Beispielsweise verfügt der Mandanten Index in SharePoint Online über einen Office Graph-Index, der für vertiefte Abfragen verwendet wird, das Analyse Verarbeitungsmodul in SharePoint Online dient zum Speichern von Signalen und Berechnen von Einblicken, und Exchange Online berechnet die einzelnen Benutzer Empfängercache als Eingabe in Mandanten Analyse.

Das Office Graph enthält Informationen zu Unternehmens Objekten wie Personen und Dokumenten sowie zu den Beziehungen und Interaktionen zwischen diesen Objekten. Die Beziehungen und Interaktionen werden als *Kanten*dargestellt. Das Office-Diagramm wird nach Mandanten segmentiert, sodass Kanten nur zwischen *Knoten* in derselben Mandantschaft vorhanden sein können. Ein *Knoten* ist eine Entität mit einem URI (Uniform Resource Identifier), Knotentyp, Zugriffssteuerungsliste und einer Gruppe von Facets, die *Metadaten* und Ränder enthalten. Jeder Knoten hat Metadaten und Kanten zugeordnet, die in *Facets* wie im allgemeinen Wissens Modell angeordnet sind. *Metadaten* sind benannte Eigenschaften, die in einem Knoten gespeichert sind, der zum Suchen, Filtern oder analysieren innerhalb des Office-Diagramms verwendet werden kann. Ein *Facet* ist eine logische Sammlung von Metadaten und Rändern auf einem Knoten. Jedes facet beschreibt einen Aspekt eines Knotens. 

Das Office-Diagramm bringt nicht alle Daten in ein einzelnes Repository; Stattdessen werden Metadaten und Beziehungen zu Daten gespeichert, die an anderer Stelle Leben. Das Office-Diagramm besteht aus mehreren Daten speichern und Verarbeitungskomponenten:
- Der Mandanten Diagrammspeicher bietet Massenspeicher, der für effiziente Analysen optimiert ist.
- Der aktive Inhalts Cache ermöglicht den schnellen Zufallszugriff auf aktive Knoten und Edges, um die Benutzerfreundlichkeit zu steigern.
- Der Eingabe Router benachrichtigt interne und externe Komponenten über Änderungen am Mandanten Diagramm.

Analysen innerhalb jeder Arbeitslast leiten Erkenntnisse, die für die Mandanten weiten Berechnungen relevant sind, und führen Sie an das Mandanten Diagramm weiter. Mandanten Analyse Gründe für alle Aktivitäten in einem Mandanten, um Einblicke in Verhaltensmuster zu erzielen. Exchange Online berechnet beispielsweise den Empfängercache für jeden Benutzer mit Analysen, die für das Postfach der einzelnen Benutzer effizient sind. Diese pro-Benutzer-Analyse erzeugt eine Reihe von *RecipientCache-Kanten* für jede Person, die wiederum an das Mandanten Diagramm geschoben werden. Dadurch wird die Verarbeitung der Analyse so weit wie möglich bei den Quelldaten beibehalten.

## <a name="tenant-isolation-in-delve"></a>Mandanten Isolierung in verTiefen
Wie bereits erwähnt, macht der Office Graph Erfahrungen, die Personen bei der Ermittlung und Zusammenarbeit an aktuellen Aktivitäten in Ihrem Unternehmen helfen, und bietet eine Entitäts zentrierte Plattform für Analysen, um die Inhalte und Aktivitäten über Arbeitslasten hinweg zu überdenken und Beyond Office 365. VerTiefen ist die erste solche Erfahrung, die von der Office-Grafik unterstützt wird.
VerTiefen ist eine Office 365-Web-Erfahrung, die Inhalte aus Office 365 und jammert Enterprise zu Office 365-Benutzer über das Office-Diagramm. Die Webumgebung zeigt Daten als unterschiedliche Bretter an, die jeweils ein bestimmtes Thema aufweisen, wie etwa *Trending um mich herum* oder *von mir geändert*. Jedes Board besteht aus mehreren Dokumentkarten, in denen Zusammenfassender Text und ein Bild aus dem Dokument angezeigt werden. Die Karte ermöglicht es Benutzern, das Dokument oder eine Jammer Seite für das Dokument zu öffnen. Für jede Person in einem Office 365-Mandanten gibt es eine Seite, die die relevantesten Dokumente für diese Person anzeigt, sowie Symbole, die Exchange Online oder Skype for Business für die Interaktion mit dieser Person aufrufen können. Da Sie auf der Office Graph-API basieren, ist Sie an die Mandanten basierte Isolierung dieser API gebunden.
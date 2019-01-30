---
title: Hinzufügen der Verwalter zu einem Fall erweiterte eDiscovery (Preview)
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
ms.openlocfilehash: d9a7dc6b1c2eeffdcd49be64d1d09d4a2bda782b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607805"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Hinzufügen einer erweiterten eDiscovery (Preview) Verwalter Case

Erweiterte eDiscovery (Preview) können Sie das integrierte Verwaltungsberechtigter-Verwaltungstool, um Ihre Workflows Verwalten von Verwalter und identifizieren relevant, freiheitsentziehenden Datenquellen in einer Anfrage koordinieren nutzen. Wenn Sie ein Verwaltungsberechtigter hinzufügen, das System automatisch erkennen und Place-Haltebereiche auf ihre primäres Exchange-Postfach und OneDrive for Business-Site. Wie Sie Ihre Suche durchführen, möglicherweise auch aufdecken und ordnen Sie zusätzliche Postfächer oder Websites, die ein Verwaltungsberechtigter in der Vergangenheit oder Teams zugegriffen werden, dass ein Verwaltungsberechtigter heute gehört.

Verwenden Sie den folgenden Workflow hinzufügen und Verwalten der Verwalter in Fällen innerhalb der & Security Compliance Center erweiterte eDiscovery (Preview). 

## <a name="step-1-identify-potential-custodians"></a>Schritt 1: Identifizieren Sie potenzieller Verwalter

Der erste Schritt besteht, um die entsprechenden Verwalter für Ihre Frage zu identifizieren. Um eine Anfrage Verwalter hinzuzufügen, müssen Sie ein Mitglied der eDiscovery-Manager oder Rollengruppe für eDiscovery-Admins sein.   

Um eine vorhandene erweiterte eDiscovery (Preview) Anfrage Verwalter hinzuzufügen:

1. Wechseln Sie auf der Seite **Erweiterte eDiscovery (Preview)** für diesen Fall.
 
2. Nachdem Sie eine Anfrage ausgewählt haben, wechseln Sie zur Registerkarte **Verwalter** , und klicken Sie auf **+ Verwaltungsberechtigter hinzufügen**. 
 
3. Wählen Sie die Verwalter, die Sie die Groß-/Kleinschreibung hinzufügen möchten. Sie können durch Eingabe suchen, und wählen Sie die Benutzer aus Ihrer Organisation Azure Active Directory starten.
 
4. Nachdem Sie die Liste der Verwalter abgeschlossen haben, klicken Sie auf **Weiter** um Identifizieren potenzieller Datenquellen zu beginnen. 
   
## <a name="optional-step-2-select-custodian-data-sources"></a>(Optional) Schritt 2: Wählen Sie Verwaltungsberechtigter-Datenquellen aus

Nachdem Sie eine Anfrage Verwalter hinzugefügt haben, können Sie Office 365 zur einfacheren Identifizieren und Beibehalten der primären Verwaltungsberechtigter Datenquellen nutzen. Im nächste Schritt in diesem Workflow ist, wählen Sie die Besitz der Verwalter in Schritt 1 angegebenen Datenquellen. 

Um Verwaltungsberechtigte Datenquellen zu ermitteln: 

1. Wählen Sie für jede Verwaltungsberechtigter **Exchange** , wenn das System automatisch identifizieren und der Verwaltungsberechtigte primäre Exchange-Postfach hinzufügen möchten. 
 
2. Wählen Sie für jede Verwaltungsberechtigter **OneDrive** , wenn das System automatisch identifizieren und der Verwaltungsberechtigte primäre OneDrive URL hinzufügen möchten. 

    Nachdem Sie Ihre Auswahl getroffen haben sie System wird automatisch versucht, die Datenquellen identifizieren und Ihren Fall hinzugefügt werden.
 
4. Klicken Sie auf **Weiter** , um Ihre Verwaltungsberechtigter zusätzliche Datenquellen zuordnen beginnen.

## <a name="optional-step-3-map-additional-data-sources"></a>(Optional) Schritt 3: Ordnen Sie zusätzliche Datenquellen

Je nach Ihren Fall Sie möglicherweise auch Postfächer hinzufügen möchten, die ein bestimmtes Verwaltungsberechtigter in der Vergangenheit verwendet haben möglicherweise gruppiert, in dem ein Verwaltungsberechtigter ist derzeit ein Element oder Websites, die ein Verwaltungsberechtigter Zugriff auf in der Vergangenheit waren. Zusätzlich zu den primären Verwaltungsberechtigter-Datenquellen können Sie zusätzliche Office 365-Datenquellen ein Verwaltungsberechtigter hinzufügen oder Nutzung von Office 365, um potenziell relevante Datenquellen zu identifizieren. 

So ordnen Sie Postfächer, Websites oder Teams zu einem bestimmten Verwaltungsberechtigter
1. Wählen Sie **Update** Speicherorte für Inhalte, wie Postfächer, Websites und Teams, ein bestimmtes Verwaltungsberechtigter zugewiesen. 

2. Geben Sie in der flyoutmenü Folgendes ein:
   
  -  **Exchange-Postfächern** - klicken Sie auf **Wählen Sie Benutzer, Gruppen oder Teams** und klicken Sie dann auf **Wählen Sie Benutzer, Gruppen oder Teams** erneut. Um Postfächer zum Zuweisen der ausgewählten Verwaltungsberechtigte anzugeben, verwenden Sie das Suchfeld Benutzerpostfächer und Verteilergruppen suchen. Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder einem Microsoft-Team zuweisen. Wählen Sie die Benutzer, die Gruppe, die Kontrollkästchen Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.

      > [!NOTE]
      > Wenn Sie Benutzer, Gruppen oder Teams auswählen, zum Angeben der Postfächer klicken, ist das Postfach Auswahltool, das angezeigt wird leer. Dies ist entwurfsbedingt zur Verbesserung der Leistung. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld.
     
   - **SharePoint-Websites** - auf **Choose Sites** , und klicken Sie dann auf **Choose Websites** erneut aus, um zusätzliche SharePoint und OneDrive for Business-Websites angeben, die Sie der ausgewählten Verwaltungsberechtigte zuweisen möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder einem Microsoft-Team hinzufügen. Geben Sie die URL für die einzelnen Standorte, die Sie zuweisen möchten. Klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
   - **Microsoft-Teams** – auf **Teams auswählen** und dann auf **Teams wählen Sie** erneut aus, um eine Liste der Microsoft-Teams, Gruppen, dass der Verwaltungsberechtigte heute gehört anzeigen. Wählen Sie die Teams, die Sie Ihrer Verwaltungsberechtigter hinzufügen möchten. Die ausgewählte erkennt das System automatisch & auswählen, die diesem Microsoft Team zugeordneten SharePoint-Website und Gruppenpostfach zugeordnet. Klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
        
      > [!NOTE]
      > Um weitere Microsoft-Teams hinzuzufügen, müssen Sie das Postfach und die SharePoint-Website wie oben gezeigt einzeln hinzufügen.

Nachdem Sie die Zuordnung von Quellen abgeschlossen haben, können Sie die Gesamtanzahl von Postfächern, Websites und Teams für die Verwalter anzeigen, die Sie soeben hinzugefügt haben. Wenn Sie die entsprechenden Datenquellen für eine bestimmte Verwaltungsberechtigter abgeschlossen haben, werden diese Zuordnung verwaltet und die eDiscovery-Auflistung, Verarbeitung und Überprüfungsworkflows erweitert. 

## <a name="optional-step-4-place-custodians-on-hold"></a>(Optional) Schritt 4: Platzieren Verwalter auf

 Nachdem Sie die Verwalter und Datenquellen, die Sie hinzufügen, zu der Fall möchten abgeschlossen haben, können Sie optional einige tätigen oder aller Ihrer Verwalter auf halten. Wenn Sie in der Warteschleife ein Verwaltungsberechtigter einleiten, wird der Inhalt dieser Benutzer zugeordnet gespeichert, bis Sie der Verwaltungsberechtigte aus der Groß-/Kleinschreibung oder freigeben, bis Sie den Haltestatus löschen. In einigen Fällen können Sie einen Case ohne ordnen sie in der Warteschleife Verwalter hinzufügen möchten. 

Halten zum Platzieren die ausgewählten Verwalter und Datenquellen auf:

1. Überprüfen Sie Ihre Auswahl Verwaltungsberechtigter, und wählen Sie die Checkox jedes Verwaltungsberechtigter in der Warteschleife platziert. Nachdem ein Verwaltungsberechtigter in der Warteschleife platziert wurde, wird eine Verwaltungsberechtigter Aufbewahrungsrichtlinie, alle freiheitsentziehenden Datenquellen enthält automatisch erstellt. Wenn die Option nicht aktiviert ist, die Verwaltungsberechtigter ausgewählt &-Datenquellen werden die Groß-/Kleinschreibung hinzugefügt werden, aber der Inhalt wird nicht beibehalten.

2. Wechseln Sie zur Registerkarte **enthält** , und wählen Sie die **Verwaltungsberechtigter halten Richtlinie**. 

3. Klicken Sie auf **Bearbeiten** , um alle ausgewählten Verwaltungsberechtigter Datenquellen anzeigen.

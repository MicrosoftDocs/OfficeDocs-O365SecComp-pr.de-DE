---
title: Hinzufügen von Bewahrern zu einem Advanced eDiscovery (Preview)-Fall
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
ms.openlocfilehash: 730e1fe40756bcb38f3b071137828072f4e2dcb5
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296718"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Hinzufügen von Bewahrern zu einem Advanced eDiscovery (Preview)-Fall

Mit Advanced eDiscovery (Preview) können Sie das integrierte Depot Verwaltungstool nutzen, um Ihre Workflows rund um die Verwaltung von Verwaltern und die Identifizierung relevanter, Freiheits enthaltener Datenquellen in einem Fall zu koordinieren. Wenn Sie eine Depotbank hinzufügen, kann das System die primären Exchange-Postfächer und die OneDrive for Business-Website automatisch identifizieren. Wenn Sie Ihre Ermittlung durchführen, können Sie auch zusätzliche Postfächer oder Websites aufdecken und zuordnen, auf die ein Verwalter in der Vergangenheit oder Teams zugegriffen hat, von denen ein Verwalter heute Mitglied ist.

Verwenden Sie den folgenden Workflow, um Verwalter in Advanced eDiscovery (Preview)-Fällen im Security & Compliance Center hinzuzufügen und zu verwalten. 

![Registerkarte Depotverwaltung](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a>Schritt 1: Identifizieren potenzieller Verwalter

Der erste Schritt besteht darin, die geeigneten Verwalter für Ihre Angelegenheit zu identifizieren. Um einem Fall Verwalter hinzuzufügen, müssen Sie Mitglied der Rollengruppe "eDiscovery-Manager" oder "eDiscovery-Admins" sein.   

![Identifizieren potenzieller Verwalter](../media/AddCustodianStep1.png)

So fügen Sie einem vorhandenen Advanced eDiscovery (Preview)-Fall Verwalter hinzu:

1. Wechseln Sie auf der Seite **Advanced eDiscovery (Preview)** zu Ihrem Fall.
 
2. Nachdem Sie einen Fall ausgewählt haben, wechseln Sie zur **** Registerkarte depotbanks, und klicken Sie auf **+ Depotbank hinzufügen**. 
 
3. Wählen Sie die Verwalter aus, die Sie der Anfrage hinzufügen möchten. Sie können zunächst eingeben, um die Benutzer aus Azure Active Directory Ihrer Organisation zu suchen und auszuwählen.
 
4. Nachdem Sie die Liste der Verwalter abgeschlossen haben, klicken Sie auf **weiter** , um mit der Identifizierung potenzieller Datenquellen zu beginnen. 
  
## <a name="optional-step-2-select-custodian-data-sources"></a>Optional Schritt 2: Auswählen von Depotbank-Datenquellen

Nachdem Sie einem Fall Verwalter hinzugefügt haben, können Sie Office 365 für die Identifizierung und Aufbewahrung der primären Depotbank-Datenquellen nutzen. Im nächsten Schritt dieses Workflows werden die Datenquellen ausgewählt, die den in Schritt 1 angegebenen depotbanks gehören. 

![Wählen Sie Datenquellen für FreiheitsEntzug aus](../media/AddCustodianStep2.png)

So identifizieren Sie Depotbank-Datenquellen: 

1. Wählen Sie für jede Depotbank **Exchange** aus, wenn das primäre Exchange-Postfach des Depot Systems automatisch ermittelt und hinzugefügt werden soll. 
 
2. Wählen Sie für jede Depotbank **OneDrive** aus, wenn Sie möchten, dass das System die primäre ONEDRIVE-URL der Depotbank automatisch identifiziert und hinzufügt. 

    Nachdem Sie Ihre Auswahl getroffen haben, versucht das System automatisch, die Datenquellen zu identifizieren und zu Ihrem Fall hinzuzufügen.
 
4. Klicken Sie auf **weiter** , um mit dem Zuordnen zusätzlicher Datenquellen zur Depotbank zu beginnen.

## <a name="optional-step-3-map-additional-data-sources"></a>Optional Schritt 3: Zuordnen zusätzlicher Datenquellen

Je nach Fall möchten Sie möglicherweise auch Postfächer hinzufügen, die ein bestimmter Depotbank in der Vergangenheit verwendet haben kann, Gruppen, in denen ein Depotbank derzeit Mitglied ist, oder Websites, auf die ein Verwalter in der Vergangenheit Zugriff hatte. Zusätzlich zu den primären Depotbank-Datenquellen können Sie zusätzliche Office 365-Datenquellen einem depotverwalter hinzufügen oder Office 365 nutzen, um potenziell relevante Datenquellen zu identifizieren. 

![Zuordnen zusätzlicher Datenquellen](../media/AddCustodianStep3.PNG)

Zuordnen von Postfächern, Websites oder Teams zu einem bestimmten Depot:

1. Wählen Sie **Aktualisieren** aus, um einem bestimmten Verwalter inhaltsspeicherorte wie Postfächer, Websites und Teams zuzuweisen. 

2. Geben Sie im Flyout Folgendes an:
   
    -  **Exchange-Postfächer** – klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** . Zum Angeben von Postfächern, die dem ausgewählten depotverwalter zugewiesen werden sollen, verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen. Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder ein Microsoft-Team zuweisen. Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.

        > [!NOTE]
        > Wenn Sie auf Benutzer, Gruppen oder Teams zum Angeben von Postfächern klicken, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein.
     
     - **SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um zusätzliche SharePoint-und OneDrive für Business-Websites anzugeben, die Sie dem ausgewählten depotverwalter zuweisen möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen. Geben Sie die URL für jede Website ein, die Sie zuweisen möchten. Klicken Sie auf **auswählen**und dann auf **Fertig**.
     - **Microsoft Teams** – klicken Sie auf **Teams auswählen** , und klicken Sie dann erneut auf **Teams auswählen** , um eine Liste der Microsoft-Team Gruppen anzuzeigen, von denen die Depotbank heute Mitglied ist. Wählen Sie die Teams aus, die Sie Ihrem depotverwalter hinzufügen möchten. Nach der Auswahl identifiziert das System automatisch & wählen Sie die zugeordnete SharePoint-Website und das Gruppenpostfach aus, die diesem Microsoft-Team zugeordnet sind. Klicken Sie auf **auswählen**und dann auf **Fertig**.
        
      > [!NOTE]
      > Um zusätzliche Microsoft Teams hinzuzufügen, müssen Sie das Postfach und die SharePoint-Website, wie oben dargestellt, separat hinzufügen.

Nachdem Sie die Zuordnung Ihrer Quellen abgeschlossen haben, können Sie die Gesamtanzahl der Postfächer, Websites und Teams für die Verwalter anzeigen, die Sie soeben hinzugefügt haben. Wenn Sie die für einen bestimmten Verwalter relevanten Datenquellen finalisiert haben, wird diese Zuordnung verwaltet und auf die eDiscovery-Sammlung, Verarbeitung und Überprüfung von Workflows ausgedehnt. 

## <a name="optional-step-4-place-custodians-on-hold"></a>Optional Schritt 4: Platzieren Sie Verwalter in der Warteschleife

Nachdem Sie die Verwalter und Datenquellen, die Sie zu Ihrem Fall hinzufügen möchten, abgeschlossen haben, können Sie optional einige oder alle Ihre Verwalter aufbewahren. Wenn Sie eine Aufbewahrungsstelle aufbewahren, werden die diesem Benutzer zugeordneten Inhalte aufbewahrt, bis Sie die Depotbank aus dem Fall freigeben oder den Haltestatus löschen. In einigen Fällen möchten Sie möglicherweise Verwalter zu einem Fall hinzufügen, ohne Sie zu halten. 

So platzieren Sie die ausgewählten Verwalter und Datenquellen in der Warteschleife:

1. Überprüfen Sie Ihre Depot Auswahl, und aktivieren Sie das Kontrollkästchen, um die Aufbewahrungszeit für jede Depotbank zu platzieren. Nachdem eine Depotbank in der Warteschleife gehalten wurde, wird automatisch eine Depotbank-Aufbewahrungsrichtlinie erstellt, die alle Depot Quellen enthält. Wenn die Option nicht aktiviert ist, werden die Depotbank und die ausgewählten Datenquellen dem Fall hinzugefügt, aber der Inhalt wird nicht beibehalten.

2. Wechseln Sie zur Registerkarte halte **Status** , und wählen Sie die **Aufbewahrungsrichtlinie**aus. 

3. Klicken Sie auf **Bearbeiten** , um alle ausgewählten Depotbank-Datenquellen anzuzeigen.

    ![Platz](../media/AddCustodianStep4.PNG)

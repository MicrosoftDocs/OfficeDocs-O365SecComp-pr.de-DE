---
title: Anzeigen der Depotbank-Überwachungsaktivität
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
ms.openlocfilehash: defc89f1d54238e62f947fd197e7a866380ee601
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241032"
---
# <a name="view-custodian-audit-activity"></a>Anzeigen der Depotbank-Überwachungsaktivität

Sie müssen herausfinden, ob ein Benutzer ein bestimmtes Dokument angezeigt oder ein Element aus seinem Postfach gelöscht hat? Advanced eDiscovery (Preview) ist jetzt in das vorhandene Überwachungsprotokoll-Such Tool im Security & Compliance Center integriert. Mithilfe dieser eingebetteten Benutzeroberfläche können Sie das Tool für die Verwaltung der erweiterten eDiscovery-Daten (Vorschau) verwenden, um Ihre Untersuchung zu erleichtern, indem Sie einfach auf die Aktivitäten für Verwalter in Ihrem Fall zugreifen und diese durchsuchen.

## <a name="before-you-begin"></a>Bevor Sie beginnen

Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" verfügen, um das Office 365-Überwachungsprotokoll durchsuchen zu können. Diese Rollen werden standardmäßig den Rollengruppen "Compliance-Verwaltung" und "Organisationsverwaltung" auf der Seite "Berechtigungen" im Exchange Admin Center zugewiesen. Um einem Benutzer die Möglichkeit zu geben, das erweiterte eDiscovery (Preview)-Überwachungsprotokoll mit den Mindestberechtigungen zu durchsuchen, können Sie eine benutzerdefinierte Rollengruppe in Exchange Online erstellen, die Überwachungsprotokolle oder Überwachungsprotokoll Rollen hinzufügen und den Benutzer dann als Mitglied der neuen Rolle GR hinzufügen. OUP. Weitere Informationen finden Sie unter Verwalten von Rollengruppen in Exchange Online.

> [!IMPORTANT]
> Wenn Sie einem Benutzer die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" auf der Seite "Berechtigungen" im Security & Compliance Center zuweisen, können Sie das Office 365-Überwachungsprotokoll nicht durchsuchen. Sie müssen die Berechtigungen in Exchange Online zuweisen. Dies liegt daran, dass das zugrunde liegende Cmdlet zum Durchsuchen des Überwachungsprotokolls ein Exchange Online-Cmdlet ist.

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a>Schritt 1: Erstellen einer erweiterten eDiscovery (Preview)-Überwachungsprotokoll Suche

   1. Wählen Sie im **Security _AMP_ Compliance Center _GT_ Advanced eDiscovery (Preview)** einen vorhandenen Fall aus.
   
   2. Navigieren Sie zur Registerkarte **Depotverwalter** , und wählen Sie eine Depotbank aus.
   
   3. Nachdem Sie eine Depotbank ausgewählt haben, klicken Sie auf  ![Anzeigen der Depotbank-Aktivität](../media/ViewCustodianActivity.PNG)  im Detailbereich.
   
   4. Konfigurieren Sie die folgenden Suchkriterien:
      
      a. **Aktivitäten** -klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungsdatensätze für die ausgewählten Aktivitäten angezeigt. Wenn Sie **Ergebnisse für alle Aktivitäten anzeigen** auswählen, werden Ergebnisse für alle Aktivitäten angezeigt, die den anderen Suchkriterien entsprechen.

      ![Liste der Aktivitäten](../media/CustodianActivityAudit.PNG)
      
      b. **Start-und Enddatum** – wählen Sie einen Datums-und Uhrzeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Die letzten sieben Tage sind standardmäßig ausgewählt. Datum und Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Zeitraum, den Sie angeben können, beträgt ein Jahr.
      
      c. **Verwalter** – klicken Sie in dieses Feld, und wählen Sie dann einen bestimmten Verwalter aus, für den Suchergebnisse angezeigt werden sollen. Überwachungsdatensätze für die ausgewählte Aktivität, die von den Benutzern, die Sie in diesem Feld ausgewählt haben, ausgeführt werden, werden in der Ergebnisliste angezeigt.
      
   5. Click   ![Schaltfläche "suchen"](../media/SearchButton.PNG)  , um die Suche mit Ihren Suchkriterien auszuführen. Die Suchergebnisse werden geladen, und nach ein paar Augenblicken werden Sie unter Ergebnisse auf der Such Seite der Depotbank-Aktivitäten angezeigt. 

## <a name="step-2-view-the-audit-log-search-results"></a>Schritt 2: Anzeigen der Suchergebnisse des Überwachungsprotokolls

Die Ergebnisse einer Überwachungsprotokoll Suche werden unter Ergebnisse auf der Seite Depot Überwachungsprotokoll angezeigt. Maximal 5.000 (neueste) Ereignisse werden in Schritten von 150 Ereignissen angezeigt. Um weitere Ereignisse anzuzeigen, können Sie die Bildlaufleiste im Ergebnisbereich verwenden, oder Sie können Umschalt + Ende drücken, um die nächsten 150-Ereignisse anzuzeigen.

Die Ergebnisse enthalten die folgenden Informationen zu jedem von der Suche zurückgegebenen Ereignis.
- **Datum**: das Datum und die Uhrzeit (im UTC-Format), als das Ereignis aufgetreten ist.

- **IP-Adresse**: die IP-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. Die IP-Adresse wird im Adressformat IPv4 oder IPv6 angezeigt.

- **Benutzer**: der Benutzer (oder das Dienstkonto), der die Aktion ausgeführt hat, die das Ereignis ausgelöst hat.

- **Activity**: die vom Benutzer ausgeführte Aktivität. Dieser Wert entspricht den Aktivitäten, die Sie in der Dropdownliste Aktivitäten ausgewählt haben. Bei einem Ereignis aus dem Exchange-administratorüberwachungsprotokoll ist der Wert in dieser Spalte ein Exchange-Cmdlet.

- **Item**: das Objekt, das als Ergebnis der entsprechenden Aktivität erstellt oder geändert wurde. Beispielsweise die Datei, die angezeigt oder geändert wurde, oder das Benutzerkonto, das aktualisiert wurde. Nicht alle Aktivitäten haben einen Wert in dieser Spalte.

- **Detail**: Weitere Details zu einer Aktivität. Auch hier haben nicht alle Aktivitäten einen Wert.

## <a name="step-3-filter-the-search-results"></a>Schritt 3: Filtern der Suchergebnisse

Zusätzlich zur Sortierung können Sie auch die Ergebnisse einer Überwachungsprotokoll Suche filtern. Auf diese Weise können Sie die Ergebnisse für einen bestimmten Benutzer oder eine bestimmte Aktivität schnell filtern. 

So filtern Sie die Ergebnisse

 1. Erstellen und Ausführen einer Überwachungsprotokoll Suche.
  
2. Wenn die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse filtern**.
 
3. Stichwort Felder werden unter jeder Spaltenüberschrift angezeigt.
  
4. Klicken Sie auf eines der Felder unter einer Spaltenüberschrift, und geben Sie je nach der Spalte, nach der gefiltert werden soll, ein Wort oder einen Ausdruck ein. Die Ergebnisse werden dynamisch angepasst, um die Ereignisse anzuzeigen, die dem Filter entsprechen.
  
5. Wenn Sie einen Filter löschen möchten, klicken Sie im Feld Filter auf das **X** , oder klicken Sie einfach auf **Filterung ausblenden**.

## <a name="export-the-search-results-to-a-file"></a>Exportieren der Suchergebnisse in eine Datei

Sie können die Ergebnisse einer Überwachungsprotokoll Suche in eine CSV-Datei (Comma Separated Value) auf Ihrem lokalen Computer exportieren. Sie können diese Datei in Microsoft Excel öffnen und Features wie suchen, sortieren, Filtern und Aufteilen einer einzelnen Spalte (die mehrwertige Zellen enthält) in mehrere Spalten verwenden.

1. Führen Sie eine Überwachungsprotokoll Suche aus, und überprüfen Sie dann die Suchkriterien, bis Sie die gewünschten Ergebnisse erhalten haben.
  
2. Klicken Sie auf Ergebnisse exportieren, und wählen Sie eine der folgenden Optionen aus:

    - **Gespeicherte Ergebnisse speichern:** Wählen Sie diese Option aus, um nur die Einträge zu exportieren, die auf der Suchseite des **Depot Überwachungsprotokolls** unter **Ergebnisse** angezeigt werden. Die heruntergeladene CSV-Datei enthält die gleichen Spalten (und Daten), die auf der Seite angezeigt werden (Datum, Benutzer, Aktivität, Element und Details). Eine weitere Spalte ( **mehr**Titel) ist in der CSV-Datei enthalten, die weitere Informationen aus dem Überwachungsprotokolleintrag enthält. Da Sie die gleichen Ergebnisse exportieren, die auf der Seite Überwachungsprotokoll Suche geladen (und angezeigt) werden, werden maximal 5.000 Einträge exportiert.
        
    - **Alle Ergebnisse herunterladen:** Wählen Sie diese Option aus, um alle Einträge aus dem Office 365-Überwachungsprotokoll zu exportieren, die den Suchkriterien entsprechen. Wählen Sie diese Option aus, um eine Vielzahl von Suchergebnissen aus dem Überwachungsprotokoll herunterzuladen, zusätzlich zu den 5.000-Ergebnissen, die auf der Suchseite des **Depot Überwachungsprotokolls** angezeigt werden können. Mit dieser Option werden die Rohdaten aus dem Überwachungsprotokoll in eine CSV-Datei heruntergeladen und zusätzliche Informationen aus dem Überwachungsprotokolleintrag in einer Spalte mit dem Namen AuditData. Es kann länger dauern, bis Sie die Datei herunterladen, wenn Sie diese Exportoption wählen, da die Datei viel größer sein kann als diejenige, die heruntergeladen wird, wenn Sie die Option andere auswählen.
    
      > [!IMPORTANT]
      > Sie können maximal 50.000 Einträge in eine CSV-Datei aus einer einzelnen Überwachungsprotokoll Suche herunterladen. Wenn 50.000-Einträge in die CSV-Datei heruntergeladen werden, können Sie wahrscheinlich davon ausgehen, dass es mehr als 50.000 Ereignisse gibt, die die Suchkriterien erfüllen. Wenn Sie mehr als diesen Grenzwert exportieren möchten, verwenden Sie einen Datumsbereich, um die Anzahl der Überwachungsprotokolleinträge zu reduzieren. Möglicherweise müssen Sie mehrere Suchvorgänge mit kleineren Datumsbereichen ausführen, um mehr als 50.000 Einträge zu exportieren.
        

3. Nachdem Sie eine Exportoption ausgewählt haben, wird unten im Fenster eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen, im Ordner "Downloads" zu speichern oder in einem bestimmten Ordner zu speichern.

Weitere Informationen zum Anzeigen, Filtern oder Exportieren von Überwachungsprotokoll-Suchergebnissen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 Security _AMP_ Compliance Center](../search-the-audit-log-in-security-and-compliance.md).

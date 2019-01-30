---
title: Verwalten von Haltestatus in erweiterten eDiscovery (Preview)
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
ms.openlocfilehash: 861b8fb8c0595f4ede0327d7426650d21046eba3
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607817"
---
# <a name="managing-holds-in-advanced-ediscovery-preview"></a>Verwalten von Haltestatus in erweiterten eDiscovery (Preview)

Erweiterte eDiscovery (Preview)-Fällen können zum Erstellen von Haltestatus, um Inhalte zu erhalten, die möglicherweise für Ihr Fall relevant. Verwenden die erweiterte eDiscovery (Preview) Funktionen halten, können Sie Haltebereiche Platzieren auf Verwalter und deren Datenquellen. Darüber hinaus können Sie einen Haltestatus freiheitsentziehenden auf Postfächer und OneDrive for Business-Websites platzieren. Sie können auch einen Haltestatus auf die Gruppe Postfach-, SharePoint-Website und OneDrive for Business-Site für eine Office 365-Gruppe platzieren. In ähnlicher Weise können Sie einen Haltestatus platzieren, auf das Postfach und die Website, die Microsoft-Teams zugeordnet sind. Wenn Sie die Speicherorte für Inhalte in der Warteschleife einleiten, wird Inhalt gespeichert, bis Sie der Verwaltungsberechtigte Version, entfernen einen spezifischen Standort oder die Aufbewahrungsrichtlinie vollständig löschen.

## <a name="manage-custodian-based-holds"></a>Verwalten von Haltestatus Verwaltungsberechtigter-basierte

In einigen Fällen müssen Sie möglicherweise eine Reihe von Verwalter von Daten, die Sie angegeben haben und entschieden, die beibehalten. Erweiterte eDiscovery (Preview) Wenn diese Verwalter sich in der Warteschleife befinden, halten in der Benutzer und die ausgewählten Daten werden Quellen ein Verwaltungsberechtigter automatisch hinzugefügt Richtlinie. 

Die Aufbewahrungsrichtlinie Verwaltungsberechtigter folgendermaßen angezeigt:

1. Klicken Sie auf die **Sicherheit & Compliance Center**, **eDiscovery > erweiterte eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.
   
2. Wechseln Sie zur Registerkarte **Verwalter** Verwalter innerhalb Ihrer Fall hinzufügen. Informationen zum Hinzufügen und platzieren in der Warteschleife in einem erweiterten eDiscovery (Preview)-Fall Verwalter finden Sie unter [Verwalter hinzufügen, um eine erweiterte eDiscovery (Preview) Fall](add-custodians-to-case.md). Wenn Sie bereits Verwalter hinzugefügt und diese in die Warteschleife gestellt, fahren Sie mit Schritt 3 fort.
   
3. Wechseln Sie zur Registerkarte **enthält** , und wählen Sie die Richtlinie"Verwaltungsberechtigter'.
   
4. In der Dropdown-Seite können Sie sehen Statistiken für die Richtlinie zu halten. Sie können auch Aktionen wie Ihre Verwaltungsberechtigter basierende Sperre eine Abfrage gilt ausführen. Weitere Informationen zum Erstellen einer Abfrage halten und Verwenden von Bedingungen finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](../keyword-queries-and-search-conditions.md).
 
## <a name="manage-non-custodial-holds"></a>Verwalten von nicht-freiheitsentziehenden Haltestatus

Wenn Sie einen Haltestatus erstellen, müssen Sie die folgenden Optionen aus, um den Inhalt zu begrenzen, der in der angegebenen Speicherorte für Inhalte gehalten wird:

  - Sie erstellen eine unendliche halten, in dem alle Inhalte in der Warteschleife platziert wird. Alternativ können Sie eine abfragebasierte Aufbewahrung erstellen, in dem nur auf Inhalte, die eine Suchabfrage entspricht in der Warteschleife platziert wird.
  - Sie können angeben, einen Datumsbereich nur die Inhalte enthalten, die gesendet, empfangen oder innerhalb des Datumsbereichs erstellt wurde. Alternativ können Sie alle Inhalte unabhängig davon Wenn es gesendet, empfangen oder erstellt wurde, halten.

Zum Erstellen eines Haltestatus für einen Fall erweiterte eDiscovery (Preview):

1. Klicken Sie auf die **Sicherheit & Compliance Center**, **eDiscovery > erweiterte eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.
  
2. Klicken Sie auf **Öffnen** neben der Groß-/Kleinschreibung, die Sie dem Haltestatus in erstellen möchten.
  
3. Klicken Sie auf der Registerkarte **enthält** , auf der Startseite für die Groß-/Kleinschreibung.
  
4. Klicken Sie auf **Erstellen**, klicken Sie auf der Registerkarte **enthält** .
  
5. Benennen Sie auf der Seite **Name der Warteschleife** dem Haltestatus. Der Name des Haltestatus muss in Ihrer Organisation eindeutig sein.
 
6. (Optional) Fügen Sie in das Feld **Beschreibung** eine Beschreibung des Haltestatus hinzu.
  
7. Klicken Sie auf **Weiter**.
  
8. Wählen Sie halten Sie die Speicherorte für Inhalte, denen Sie einfügen möchten. Sie können die Postfächer, Websites und Öffentliche Ordner in der Warteschleife platzieren.

   a: **Exchange-e-Mail** - klicken Sie auf **Wählen Sie Benutzer, Gruppen oder Teams** und klicken Sie dann auf **Wählen Sie Benutzer, Gruppen oder Teams** erneut aus, um anzugeben, dass Postfächer auf halten. Verwenden Sie das Suchfeld, um die Benutzerpostfächer und Verteilergruppen (in einem Haltestatus auf die Postfächer von Gruppenmitgliedern platzieren) Hier finden Sie in der Warteschleife platziert. Sie können auch einen Haltestatus auf das zugeordnete Postfach für eine Office 365-Gruppe oder ein Team Microsoft platzieren. Wählen Sie die Benutzer, die Gruppe, die Kontrollkästchen Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
 
    > [!NOTE]
    > Wenn Sie **Wählen Sie Benutzer, Gruppen oder Teams** an Postfächer in die Warteschleife stellen klicken, wird das Postfach Auswahltool, das angezeigt wird leer. Dies ist entwurfsbedingt zur Verbesserung der Leistung. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld.

    b. **SharePoint-Websites** - klicken Sie auf **Websites auswählen** und dann auf **Choose Websites** erneut aus, um anzugeben, dass SharePoint und OneDrive for Business-Websites auf halten. Geben Sie die URL für die einzelnen Standorte, die Sie in die Warteschleife stellen möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder einem Microsoft-Team hinzufügen. Klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
    
     Finden Sie im Abschnitt **häufig gestellte Fragen zu** Tipps für die Office 365-Gruppen und Microsoft-Teams, in der Warteschleife an.

    > [!NOTE]
    > In seltenen Fällen einer Person für Benutzerprinzipalnamen (UPN) geändert wurde, wird auch die URL für ihre OneDrive-Konto, um den neuen UPN integrieren geändert werden. In diesem Fall müssen Sie den Haltestatus zu ändern, indem Sie neue OneDrive-URL des Benutzers hinzufügen und Entfernen von der alte Datenbankserver.

     c. **Öffentliche Ordner von Exchange** - verschieben Sie die Umschaltfläche auf alle Position, platzieren Sie alle öffentlichen Ordner in Ihrer Exchange Online Organisation auf halten. Notiz, die Sie bestimmte Öffentliche Ordner zu hinzufügen auswählen können nicht halten. Lassen Sie die Umschaltfläche auf **keine** festgelegt, wenn Sie nicht, um einem Haltestatus für Öffentliche Ordner zu platzieren möchten.

9. Wenn Sie dem Haltestatus hinzufügen Inhaltsspeicherorte fertig sind, klicken Sie auf **Weiter**.
  
10. Führen Sie die folgenden Schritte aus, um eine abfragebasierte Aufbewahrung mit Bedingungen zu erstellen. Andernfalls, klicken Sie einfach auf **Weiter**.
    
    - Unter im Feld **Stichwörter**eine Suchabfrage im Feld Typ, sodass nur die Inhalte, die die Suchkriterien erfüllt platziert ist halten. Sie können Schlüsselwörter, Nachrichteneigenschaften oder Dokumenteigenschaften, wie Dateinamen angeben. Sie können auch komplexere Abfragen, die einen booleschen Operators, wie AND, OR oder nicht verwenden. Wenn Sie lassen halten Sie das Schlüsselwort Feld leer ist, und klicken Sie dann auf alle Inhalte befindet sich in der angegebenen Speicherorte für Inhalte platziert wird.

    - Klicken Sie auf **Add** Bedingungen an einen oder mehrere Bedingungen einschränken die Suchabfrage für den Haltestatus hinzuzufügen. Jede Bedingung hinzugefügt der KQL Search-Abfrage, die erstellt und ausgeführt, wenn Sie den Haltestatus erstellen eine-Klausel. Beispielsweise können Sie einen Datumsbereich angeben, sodass e-Mail oder Website Dokumente, die in dem Bereich Datum erstellt wurden, in die Warteschleife gestellt werden. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) von der AND-Operator verbunden. Das bedeutet, die Elemente beide erfüllen müssen halten die Stichwortabfrage und die Bedingung auf platziert werden.

     Weitere Informationen zum Erstellen einer Suchabfrage und Bedingungen verwenden finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

12. Halten Sie nach der Konfiguration einer abfragebasierte, und klicken Sie auf **Weiter**.
 
13. Überprüfen Sie die Einstellungen, und klicken Sie dann auf **diesem Haltestatus erstellen**.


## <a name="view-hold-statistics"></a>Anzeigen von Statistiken Haltestatus

Informationen zu den neuen Haltestatus wird nach einiger Zeit im Detailbereich auf der Registerkarte **enthält** , für die ausgewählte Warteschleife angezeigt. Hierzu gehören die Anzahl von Postfächern Websites auf halten, und halten Sie Statistiken zu den Inhalt, der auf getätigt wurde, wie die gesamte Anzahl und Größe der Elemente in der Warteschleife platziert und der letzten Ausführung den Haltestatus, die Statistik berechnet wurden. Diese Dateien enthalten Statistiken Hilfe, die Sie ermitteln, wie viel Inhalt, die auf den eDiscovery-Fall zusammenhängt gehalten wird.

Beachten Sie die folgenden Punkte berücksichtigen zu halten Statistiken:

- Die Gesamtzahl der Elemente in der Warteschleife gibt die Anzahl von Elementen aus allen Inhaltsquellen, die in der Warteschleife platziert werden. Wenn Sie erstellt haben halten eine abfragebasierte, diese Statistik gibt die Anzahl der Elemente an, die mit die Abfrage übereinstimmen.
  
- Die Anzahl der Elemente in der Warteschleife enthält auch nicht indizierten Elemente in die Speicherorte für Inhalte gefunden. Beachten Sie, wenn Sie eine abfragebasierte Aufbewahrung erstellen, werden alle nicht-indizierten Elemente in die Speicherorte für Inhalte in die Warteschleife gestellt. Dazu gehören nicht indizierten Elementen, die nicht die Suchkriterien des eine abfragebasierte Aufbewahrung entsprechen und nicht-indizierten Elementen, die außerhalb von Bereich Bedingung Datum liegen möglicherweise. Dies unterscheidet sich was geschieht, wenn Sie eine Inhaltssuche ausführen, in dem nicht indizierte Elementen, die die Suchabfrage stimmen nicht überein oder durch eine Datum Bereich Bedingung ausgeschlossen werden in den Suchergebnissen enthalten sind. Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in Inhaltssuche in Office 365](../partially-indexed-items-in-content-search.md). 

- Sie können die neuesten Haltestatus Statistiken abrufen, indem Sie auf Update Statistik eine Schätzung Suche erneut ausführen, die die aktuelle Anzahl von Elementen in der Warteschleife berechnet.

- Falls erforderlich, klicken Sie auf aktualisieren, in der Symbolleiste auf die Warteschleife Statistiken im Detailbereich zu aktualisieren.

- Normal für die Anzahl der Elemente auf halten über einen Zeitraum zu erhöhen, da Benutzer, dessen Postfach oder Website in der Warteschleife ist, in der Regel senden oder Empfangen von neuen e-Mail-Nachricht und erstellen neue SharePoint- und OneDrive für Geschäftsdokumente.

- Wenn eine SharePoint-Website oder OneDrive-Konto zu einem anderen Bereich in einer Umgebung mit mehreren geografisch verschoben wurde, nicht die Statistiken für diese Website in die Warteschleife Statistik berücksichtigt. Die Inhalte der Website werden jedoch weiterhin in der Warteschleife. Darüber hinaus wird eine Website in einer anderen Region verschoben wird die URL, die in der Warteschleife angezeigt wird nicht aktualisiert werden. Sie müssen den Haltestatus bearbeiten und aktualisieren Sie die URL.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

- **Wie ich ein Verwaltungsberechtigter eine zusätzliche Office 365 Gruppen oder Teams Microsoft-Website zugeordnet sind? Und wie sieht es aus einer nicht freiheitsentziehenden Platzieren auf Office 365-Gruppen und Microsoft-Teams, halten Sie?** Microsoft-Teams, basieren auf Office 365-Gruppen. Ordnen sie in der Warteschleife in einem eDiscovery-Fall ist daher sehr ähnlich. Berücksichtigen Sie die folgenden Punkte berücksichtigen, bei der platzieren Office 365-Gruppen und Microsoft-Teams auf halten.
  - Um Inhalt befindet sich im Office 365-Gruppen und Microsoft-Teams, in der Warteschleife zu platzieren, müssen Sie das Postfach angeben und SharePoint-Website, die eine Gruppe oder ein Team zugeordnet.
  
  - Führen Sie das Cmdlet **Get-UnifiedGroup** in Exchange Online zum Anzeigen von Eigenschaften für ein Office 365-Gruppe oder ein Team von Microsoft. Dies ist eine empfehlenswerte Methode zum Abrufen der URL für die Website, die ein Office 365-Gruppe oder ein Microsoft-Team zugeordnet ist. Beispielsweise wird mit der folgende Befehl ausgewählte Eigenschaften für ein Office 365-Gruppe mit dem Namen Senior führende Team angezeigt:


    ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > Um das Cmdlet Get-UnifiedGroup ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen.

 - Wenn dem Postfach eines Benutzers durchsucht wird, werden keine Office 365-Gruppe oder der Microsoft-Teams, die der Benutzer Mitglied ist gesucht werden soll. Wenn Sie eine Office 365-Gruppe platzieren oder Microsoft Team halten, nur die Gruppenpostfach und Gruppenseite platziert werden auf ähnliche Weise, halten Sie; Postfächer und OneDrive for Business-Websites Gruppenmitglieder werden nicht in die Warteschleife gestellt, es sei denn, Sie explizit als Verwalter hinzufügen oder ihre Datenquellen halten. Daher, wenn Sie ein Office 365-Gruppe oder Microsoft-Teams auf platzieren müssen für eine bestimmte Verwaltungsberechtigter halten, sollten Sie der Verwaltungsberechtigte (finden Sie unter Verwalten von Verwalter in erweiterten eDiscovery (Preview)) die Gruppe Website und Gruppenpostfach zuordnen. Wenn die Office 365-Gruppe oder ein Microsoft-Team nicht auf ein einzelnes Verwaltungsberechtigter zurückzuführen ist, sollten Sie halten die Quelle an, ein nicht freiheitsentziehenden hinzufügen. 
 
 - Wenn Sie eine Liste der Mitglieder einer Gruppe von Office 365 oder Microsoft-Teams erhalten möchten, können Sie die Eigenschaften auf der Homepage für die Gruppen von > im Office 365 Administrationscenter anzeigen. Alternativ können Sie in Exchange Online PowerShell den folgenden Befehl ausführen:

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroupLinks** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen.

- Kanal-Unterhaltungen, die Teil eines Microsoft-Teams Kanals sind werden im Postfach gespeichert, die mit dem Team zugeordnet ist. In ähnlicher Weise werden Dateien, die in einem Kanal Teammitglieder freigeben auf das Team SharePoint-Website gespeichert. Daher müssen Sie das Microsoft-Teams Postfach platzieren und SharePoint-Website auf halten, um Unterhaltungen und Dateien in einem Kanal beibehalten werden.
  
- Alternativ werden Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams, sind in das Postfach des Benutzers, die im Chat teilnehmen gespeichert.  Dateien, die ein Benutzer in Chat Unterhaltungen gemeinsam werden in die OneDrive for Business-Website des Benutzers gespeichert, die die Dateifreigaben. Daher müssen Sie die einzelnen Benutzerpostfächer platzieren und OneDrive for Business-Websites auf halten, um Unterhaltungen und Dateien in der Liste Chat beibehalten werden. 
  
- Jede Microsoft-Teams oder ein Team Kanal enthält ein Wiki für Notizen und die Zusammenarbeit. Der Wiki-Inhalt wird automatisch in eine Datei mit einem MHT-Format gespeichert. Diese Datei ist in der Dokumentbibliothek Teams Wiki-Daten auf SharePoint-Teamwebsite gespeichert. Sie können den Inhalt im Wiki in der Warteschleife tätigen, indem Sie das Team SharePoint-Website in der Warteschleife platziert.

  > [!NOTE]
  > Die Möglichkeit zum Beibehalten von Wiki-Inhalten für einen Microsoft-Teams oder ein Team-Kanal (Wenn Sie das Team SharePoint-Website in die Warteschleife stellen) wurde am 22 Juni 2017 veröffentlicht. Wenn auf eine Teamwebsite ist halten Sie, das Wiki Inhalte an diesem Datum starten aufbewahrt werden. Jedoch wurde Wenn eine Teamwebsite in der Warteschleife wird und die Wiki-Inhalte vor dem 22 Juni 2017 gelöscht wurde nicht der Inhalt Wiki beibehalten.

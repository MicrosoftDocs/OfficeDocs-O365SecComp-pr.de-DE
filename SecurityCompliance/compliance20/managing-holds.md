---
title: Verwalten von Haltebereichen in Advanced eDiscovery (Preview)
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
ms.openlocfilehash: fe6ab3a1e1108e9ab2e4fc201357b72a77453d38
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295718"
---
# <a name="manage-holds-in-advanced-ediscovery-preview"></a>Verwalten von Haltebereichen in Advanced eDiscovery (Preview)

Sie können einen erweiterten eDiscovery (Preview)-Fall verwenden, um haltebereiche zu erstellen, die für Ihren Fall relevant sind. Mithilfe der erweiterten eDiscovery-Funktionen (Preview) können Sie haltebereiche für Verwalter und deren Datenquellen platzieren. Darüber hinaus können Sie Postfächer und OneDrive für Business-Websites nicht sperren. Sie können auch das Gruppenpostfach, die SharePoint-Website und die OneDrive for Business-Website für eine Office 365-Gruppe einhalten. Entsprechend können Sie auch das Postfach und die Website, die Microsoft Teams zugeordnet sind, einhalten. Wenn Sie inhaltsspeicherorte in der Warteschleife platzieren, werden Inhalte aufbewahrt, bis Sie die Depotbank freigeben, einen bestimmten Datenspeicherort entfernen oder die halte Richtlinie vollständig löschen.

## <a name="manage-custodian-based-holds"></a>Verwalten von Depot basierten Haltebereichen

In einigen Fällen verfügen Sie möglicherweise über eine Reihe von Datenverwalter, die Sie identifiziert haben und die Sie beibehalten möchten. In Advanced eDiscovery (Preview) werden die Benutzer und Ihre ausgewählten Datenquellen automatisch einer Aufbewahrungsrichtlinie hinzugefügt, wenn diese Verwalter in der Warteschleife gespeichert werden. 

So zeigen Sie die Aufbewahrungsrichtlinie an:

1. Klicken Sie im **Security _AMP_ Compliance Center**auf **eDiscovery > Advanced eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.
   
2. Wechseln Sie zur Registerkarte **depotverwalter** , um Verwalter in Ihrem Fall hinzuzufügen. Informationen dazu, wie Sie Verwalter in einem Advanced eDiscovery (Preview)-Fall hinzufügen und platzieren können, finden Sie unter Hinzufügen von Bewahrern [zu einem Advanced eDiscovery (Preview)-Fall](add-custodians-to-case.md). Wenn Sie bereits Verwalter hinzugefügt und in die Warteschleife gestellt haben, fahren Sie mit Schritt 3 fort.
   
3. Wechseln Sie zur Registerkarte halte **Status** , und wählen Sie die Option "Depotbank" aus.
   
4. Auf der Flyout-Seite können Sie die Statistiken für die Richtlinie halten. Sie können auch Aktionen wie das Anwenden einer Abfrage auf Ihren Depot basierten Haltebereich ausführen. Weitere Informationen zum Erstellen einer Hold-Abfrage und zum Verwenden von Bedingungen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md).
 
## <a name="manage-non-custodial-holds"></a>Verwalten von Freiheitsentzug

Wenn Sie einen Haltestatus erstellen, haben Sie die folgenden Optionen, um den Inhalt an den angegebenen Inhaltsspeicherorten zu bereichern:

  - Sie erstellen eine unendliche Halteposition, an der der gesamte Inhalt gehalten wird. Alternativ können Sie eine abfragebasierte Aufbewahrung erstellen, in der nur Inhalte gespeichert werden, die mit einer Suchabfrage übereinstimmen.
  - Sie können einen Datumsbereich angeben, der nur den Inhalt enthalten soll, der innerhalb dieses Datumsbereichs gesendet, empfangen oder erstellt wurde. Alternativ können Sie alle Inhalte unabhängig davon speichern, wann Sie gesendet, empfangen oder erstellt wurden.

So erstellen Sie einen Speicher für einen erweiterten eDiscovery (Preview)-Fall:

1. Klicken Sie im **Security _AMP_ Compliance Center**auf **eDiscovery > Advanced eDiscovery (Preview)** , um die Liste der Fälle in Ihrer Organisation anzuzeigen.
  
2. Klicken Sie neben dem Fall, in dem Sie den Haltestatus erstellen möchten, auf **Öffnen** .
  
3. Klicken Sie auf der Startseite für den Fall auf die Registerkarte halte **Status** .
  
4. Klicken Sie auf der Registerkarte halte **Status** auf **Erstellen**.
  
5. Geben Sie auf der Seite " **halten Sie den Namen** " einen Namen ein. Der Name des haltebereichs muss in Ihrer Organisation eindeutig sein.
 
6. Optional Fügen Sie im Feld **Beschreibung** eine Beschreibung des haltebereichs hinzu.
  
7. Klicken Sie auf **Weiter**.
  
8. Wählen Sie die inhaltsspeicherorte aus, die Sie für den Aufbewahrungsort aktivieren möchten. Sie können Postfächer, Websites und öffentliche Ordner in der Warteschleife platzieren.

   a. **Exchange e-Mail** -klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** , um die Aufbewahrungszeit für Postfächer anzugeben. Verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen (um die Postfächer der Gruppenmitglieder einzuhalten). Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder ein Microsoft-Team einhalten. Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
 
    > [!NOTE]
    > Wenn Sie auf **Benutzer, Gruppen oder Teams auswählen** klicken, um die Postfächer anzugeben, die in der Warteschleife platziert werden sollen, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein.

    b. **SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um SharePoint-und OneDrive für Business-Websites für die Aufbewahrung anzugeben. Geben Sie die URL für jede Website ein, die Sie in der Warteschleife platzieren möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen. Klicken Sie auf **auswählen**und dann auf **Fertig**.
    
     Weitere Informationen finden Sie im Abschnitt " **FAQ** ", in dem Sie sich über das Speichern von Office 365-Gruppen und Microsoft Teams unterhalten.

    > [!NOTE]
    > In den seltenen Fällen, in denen sich der Benutzerprinzipalname (UPN) einer Person geändert hat, wird auch die URL für Ihr OneDrive-Konto geändert, um den neuen UPN zu integrieren. In diesem Fall müssen Sie den Haltestatus ändern, indem Sie die neue OneDrive-URL des Benutzers hinzufügen und den alten entfernen.

     c. **Öffentliche Ordner in Exchange** : Verschieben Sie den UMSCHALT Schalter in die alle-Position, um alle öffentlichen Ordner in Ihrer Exchange Online-Organisation aufzubewahren. Beachten Sie, dass Sie bestimmte öffentliche Ordner nicht für die Aufbewahrung auswählen können. Lassen Sie den UMSCHALT Schalter auf **None** festgelegt, wenn Sie keine öffentlichen Ordner einhalten möchten.

9. Wenn Sie mit dem Hinzufügen von Inhaltsspeicherorten zum Haltebereich fertig sind, klicken Sie auf **weiter**.
  
10. Führen Sie die folgenden Schritte aus, um eine abfragebasierte Aufbewahrung mit Bedingungen zu erstellen. Klicken Sie andernfalls einfach auf **weiter**.
    
    - Geben Sie im Feld unter **Schlüsselwörter**eine Suchabfrage in das Feld ein, sodass nur der Inhalt, der den Suchkriterien entspricht, in der Warteschleife gespeichert wird. Sie können Schlüsselwörter, Nachrichteneigenschaften oder Dokumenteigenschaften wie Dateinamen angeben. Sie können auch komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise AND, OR oder NOT. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in der Warteschleife platziert.

    - Klicken Sie auf Bedingungen **Hinzufügen** , um eine oder mehrere Bedingungen hinzuzufügen, um die Suchabfrage für den Haltebereich einzuschränken. Jede Bedingung fügt der KQL-Suchabfrage, die beim Erstellen des haltebereichs erstellt und ausgeführt wird, eine Klausel hinzu. Sie können beispielsweise einen Datumsbereich angeben, sodass e-Mails oder Website Dokumente, die innerhalb des Datumsbereichs erstellt wurden, gehalten werden. Eine Bedingung ist logisch mit der Schlüsselwortabfrage (angegeben im Stichwortfeld) durch den AND-Operator verbunden. Das hat zur Folge, dass Elemente sowohl die Stichwortabfrage als auch die Bedingung erfüllen müssen, die in den Haltestatus versetzt werden soll.

     Weitere Informationen zum Erstellen einer Suchabfrage und zum Verwenden von Bedingungen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

12. Klicken Sie nach dem Konfigurieren einer abfragebasierten Aufbewahrung auf **weiter**.
 
13. Überdenken Sie Ihre Einstellungen, und klicken Sie dann auf **diesen halteBereich erstellen**.


## <a name="view-hold-statistics"></a>Hold-Statistiken anzeigen

Nach einiger Zeit werden Informationen über den neuen Haltestatus im Detailbereich auf der Registerkarte halte **Status** für den ausgewählten Halt angezeigt. Zu diesen Informationen gehören die Anzahl der Postfächer und Websites, die in der Warteschleife gespeichert wurden, sowie Statistiken zu den Inhalten, die in den Warteschlangen gehalten wurden, wie die Gesamtanzahl und die Größe der in der Warteschleife befindlichen Elemente und der Zeitpunkt der letzten Berechnung der Aufbewahrungs Statistiken. Anhand dieser Statistiken können Sie ermitteln, wie viele Inhalte im Zusammenhang mit dem eDiscovery-Fall stehen.

Beachten Sie die folgenden Aspekte im Hinblick auf Hold Statistics:

- Die Gesamtanzahl der in der Warteschleife enthaltenen Elemente gibt die Anzahl der Elemente aus allen Inhaltsquellen an, die in der Warteschleife gespeichert werden. Wenn Sie eine abfragebasierte Aufbewahrung erstellt haben, gibt diese Statistik die Anzahl der Elemente an, die der Abfrage entsprechen.
  
- Die Anzahl der in der Warteschleife enthaltenen Elemente enthält auch nicht indizierte Elemente, die sich in den Inhaltsspeicherorten befinden. Beachten Sie, dass beim Erstellen einer abfragebasierten Aufbewahrung alle nicht indizierten Elemente in den Inhaltsspeicherorten gehalten werden. Dies umfasst nicht indizierte Elemente, die nicht mit den Suchkriterien einer abfragebasierten Aufbewahrung übereinstimmen, und nicht indizierte Elemente, die möglicherweise außerhalb einer Datumsbereichs Bedingung liegen. Dies unterscheidet sich von dem, was passiert, wenn Sie eine Inhaltssuche ausführen, in der nicht indizierte Elemente, die nicht mit der Suchabfrage übereinstimmen oder von einer Bedingung für den Datumswert ausgeschlossen werden, nicht in den Suchergebnissen enthalten sind. Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](../partially-indexed-items-in-content-search.md). 

- Sie können die neueste Hold-Statistik abrufen, indem Sie auf Statistik aktualisieren klicken, um eine Such Schätzung erneut auszuführen, die die aktuelle Anzahl der zu speichernden Elemente berechnet.

- Klicken Sie gegebenenfalls in der Symbolleiste auf aktualisieren, um die Aufbewahrungs Statistiken im Detailbereich zu aktualisieren.

- Es ist normal, dass die Anzahl der zu haltenden Elemente im Laufe der Zeit ansteigt, da Benutzer, deren Postfach oder Website in Betrieb ist, normalerweise neue e-Mail-Nachrichten senden oder empfangen und neue SharePoint-und OneDrive für Geschäftsdokumente erstellen.

- Wenn ein SharePoint-oder OneDrive-Konto in eine andere Region in einer Multi-Geo-Umgebung verschoben wird, werden die Statistiken für diese Website nicht in die Aufbewahrungs Statistik aufgenommen. Die Inhalte auf der Website bleiben jedoch weiterhin in der Warteschleife. Wenn eine Website in einen anderen Bereich verschoben wird, wird auch die URL, die in der Warteschleife angezeigt wird, nicht aktualisiert. Sie müssen den Haltebereich bearbeiten und die URL aktualisieren.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

- **Wie kann ich eine zusätzliche Office 365-Gruppe oder Microsoft Teams-Website einem depotverwalter zuordnen? Und wie sieht es mit einem nicht FreiheitsEntzug für Office 365-Gruppen und Microsoft Teams aus?** Microsoft Teams basieren auf Office 365-Gruppen. Daher ist es sehr ähnlich, Sie in einem eDiscovery-Fall aufzubewahren. Beachten Sie beim Platzieren von Office 365-Gruppen und Microsoft Teams die folgenden Aspekte.
  - Wenn Sie Inhalte in Office 365-Gruppen und Microsoft Teams platzieren möchten, müssen Sie das Postfach und die SharePoint-Website angeben, die einer Gruppe oder einem Team zugeordnet ist.
  
  - Führen Sie das Cmdlet **Get-Unifiedgroup** in Exchange Online aus, um die Eigenschaften einer Office 365-Gruppe oder eines Microsoft Teams anzuzeigen. Dies ist eine gute Möglichkeit, die URL für die Website abzurufen, die einer Office 365-Gruppe oder einem Microsoft-Team zugeordnet ist. Mit dem folgenden Befehl werden beispielsweise ausgewählte Eigenschaften für eine Office 365-Gruppe mit dem Namen "Senior Leadership Team" angezeigt:


    ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > Damit Sie das Cmdlet Get-Unifiedgroup ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist.

 - Wenn das Postfach eines Benutzers durchsucht wird, werden alle Office 365-Gruppen oder Microsoft-Teams, in denen der Benutzer Mitglied ist, nicht durchsucht. Entsprechend werden beim Platzieren einer Office 365-Gruppe oder eines Microsoft Teams nur das Gruppenpostfach und die Gruppen Website in der Warteschleife platziert. die Postfächer und OneDrive für Business-Websites von Gruppenmitgliedern werden nicht in die Warteschleife gestellt, es sei denn, Sie fügen Sie explizit als Verwalter hinzu oder platzieren Ihre Datenquellen in der Warteschleife. Wenn Sie daher eine Office 365-Gruppe oder ein Microsoft-Team für eine bestimmte Depotbank in der Warteschleife platzieren müssen, sollten Sie die Gruppen Website und das Gruppenpostfach der Depotbank zuordnen (siehe Managing Custodys in Advanced eDiscovery (Preview)). Wenn die Office 365-Gruppe oder das Microsoft-Team nicht auf einen einzigen Verwalter zurückzuführen ist, sollten Sie erwägen, die Quelle in einem Depot ohne Freiheitsentzug hinzuzufügen. 
 
 - Wenn Sie eine Liste der Mitglieder einer Office 365-Gruppe oder eines Microsoft Teams abrufen möchten, können Sie die Eigenschaften auf der Seite >-Gruppen für Office 365 anzeigen. Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen:

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-UnifiedGroupLinks** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist.

- Kanal Unterhaltungen, die Teil eines Microsoft Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Team zugeordnet ist. Entsprechend werden Dateien, die Teammitglieder in einem Kanal freigeben, auf der SharePoint-Website des Teams gespeichert. Daher müssen Sie das Microsoft Team-Postfach und die SharePoint-Website anhalten, um Unterhaltungen und Dateien in einem Kanal beizubehalten.
  
- Alternativ werden Unterhaltungen, die Teil der Chat-Liste in Microsoft Teams sind, im Postfach des Benutzers gespeichert, der am Chat teilnimmt.  Dateien, die ein Benutzer in Chat Unterhaltungen freigibt, werden auf der OneDrive for Business-Website des Benutzers gespeichert, der die Datei freigibt. Daher müssen Sie die einzelnen Benutzerpostfächer und OneDrive für Business-Websites in der Warteschleife platzieren, um Unterhaltungen und Dateien in der Chat-Liste beizubehalten. 
  
- Jeder Microsoft-Team-oder Team Kanal enthält ein wiki für Notizen und Zusammenarbeit. Der wiki-Inhalt wird automatisch in einer Datei mit dem MHT-Format gespeichert. Diese Datei wird in der Microsoft Teams-wiki-Datendokument Bibliothek auf der SharePoint-Website des Teams gespeichert. Sie können die Inhalte im wiki halten, indem Sie die SharePoint-Website des Teams in der Warteschleife platzieren.

  > [!NOTE]
  > Die Möglichkeit, wiki-Inhalte für ein Microsoft-Team oder einen Team Kanal beizubehalten (wenn Sie die SharePoint-Website des Teams in der Warteschleife platzieren) wurde am 2017 veröffentlicht. Wenn eine Teamwebsite in der Warteschleife steht, wird der wiki-Inhalt ab diesem Datum aufbewahrt. Wenn jedoch eine Teamwebsite gehalten wird und der Inhalt des Wikis vor dem 22. Juni 2017 gelöscht wurde, wurde der wiki-Inhalt nicht beibehalten.

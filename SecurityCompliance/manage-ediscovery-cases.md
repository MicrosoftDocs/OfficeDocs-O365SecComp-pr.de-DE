---
title: Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9a00b9ea-33fd-4772-8ea6-9d3c65e829e6
description: Verwenden Sie die Office 365-Sicherheit &amp; Compliance Center zum Erstellen von eDiscovery-Haltestatus sowie zum zugreifen und Verwalten von eDiscovery-Fälle in Ihrer Organisation.
ms.openlocfilehash: 5be66419e19f9703be5dde3fad82837bda249b72
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529436"
---
# <a name="manage-ediscovery-cases-in-the-office-365-security-amp-compliance-center"></a>Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center

Sie können die eDiscovery-Fälle verwenden, in die Office 365-Sicherheit &amp; Compliance Center steuern, wer erstellen, Zugriff und eDiscovery-Fälle in Ihrer Organisation verwalten können. Wenn Ihre Organisation ein E5 für Office 365-Abonnement umfasst, können Sie auch eDiscovery-Fälle zum Analysieren von Suchergebnissen mithilfe von Office 365 erweiterte eDiscovery verwenden.
  
EDiscovery-Fall können Sie zum Hinzufügen von Mitgliedern zu einer Anfrage, die steuern, welche Arten von Aktionen, dass bestimmte Groß-/Kleinschreibung Mitglieder durchführen, platzieren Sie einen Haltestatus auf Speicherorte für Inhalte in eine rechtliche Anfrage relevant und ordnen Sie einen einzelnen Case mehrere Inhalten suchen können. Sie können auch Exportieren der Suchergebnisse in Content, die eine Anfrage zugeordnet ist oder Vorbereiten von Suchergebnissen für die Analyse in erweiterten eDiscovery. eDiscovery-Fälle sind eine empfehlenswerte Methode zum einschränken, wer Zugriff auf Content-Suche und die Suchergebnisse für eine bestimmte rechtliche Anfrage in Ihrer Organisation hat.
  
Verwenden Sie den folgenden Workflow zum Einrichten und Verwenden von eDiscovery-Fälle in das Wertpapier &amp; eDiscovery Compliance Center und erweitert.
  
[Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern](manage-ediscovery-cases.md#step1_1)
  
[Schritt 2: Erstellen einer neuen Anfrage](manage-ediscovery-cases.md#step2_1)
  
[Schritt 3: Hinzufügen von Mitgliedern zu einer Anfrage](manage-ediscovery-cases.md#step2a_1)
  
[Schritt 4: Platzieren Speicherorte für Inhalte auf](manage-ediscovery-cases.md#step3_1)
  
[Schritt 5: Erstellen Sie und führen Sie einer eine Anfrage zugeordnete Inhaltssuche aus](manage-ediscovery-cases.md#step4_1)
  
[Schritt 6: Exportieren Sie die Ergebnisse einer Inhaltssuche eine Anfrage zugeordnete](manage-ediscovery-cases.md#step5_1)
  
[Schritt 7: Vorbereiten der Suchergebnisse für erweiterte eDiscovery](manage-ediscovery-cases.md#step7_1)
  
[Schritt 8: Wechseln Sie zu der erweiterten eDiscovery-Fall](manage-ediscovery-cases.md#gotoAeD_1)
  
[(Optional) Schritt 9: Schließen Sie eine Anfrage](manage-ediscovery-cases.md#closecase_1)
  
[(Optional) Schritt 10: Eine geschlossene Anfrage erneut öffnen](manage-ediscovery-cases.md#reopencase_1)
  
[Weitere Informationen](manage-ediscovery-cases.md#moreinfo_1)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern
<a name="step1_1"> </a>

Der erste Schritt besteht die entsprechenden Berechtigungen eDiscovery-bezogene an Personen zuweisen, damit Sie sie zu einem eDiscovery-Fall in Schritt2 hinzufügen können. Sie müssen ein Mitglied der Rollengruppe "Organisationsverwaltung" (oder die Verwaltungsrolle Rolle zugewiesen werden) in die Office 365-Sicherheit &amp; Compliance Center, eDiscovery-Berechtigungen zuzuweisen. Die folgende Liste beschreibt die eDiscovery-bezogene Rollengruppen in das Wertpapier &amp; Compliance Center.
  
- **Prüfer** Dieser Rollengruppe hat die restriktivsten eDiscovery-bezogene Berechtigungen. Mitglieder dieser Gruppe können nur finden und öffnen Sie die Liste der auf der Seite **eDiscovery** -Fälle in das Wertpapier &amp; Compliance Center, die sie Mitglieder sind. Hinzufügen von Mitgliedern zu einer Anfrage Fällen erstellt werden kann, Haltestatus erstellen, erstellen Sie gesucht, Exportieren von Suchergebnissen oder Ergebnisse für erweiterte eDiscovery vorbereiten. Mitglieder können jedoch Fällen in erweiterten eDiscovery Analysis Aufgaben zugreifen. 
    
- **eDiscovery-Manager** Mitglieder dieser Rollengruppe können erstellen und Verwalten von eDiscovery-Fälle. Sie können hinzufügen und Entfernen von Mitgliedern, platzieren Sie Inhalte Speicherorte auf halten, erstellen und bearbeiten eine Anfrage zugeordnete Inhalte durchsucht, exportieren Sie die Ergebnisse einer Suche Inhalte und Vorbereiten von Suchergebnissen für die Analyse in erweiterten eDiscovery. Es gibt zwei Untergruppen in dieser Rollengruppe. Der Unterschied zwischen diesen Untergruppen basiert auf Bereich.
    
  - **eDiscovery-Manager** Anzeigen und verwalten sie erstellen oder ein Mitglied der eDiscovery-Fälle. Eine andere eDiscovery-Manager erstellt eine Anfrage, jedoch keine zweite eDiscovery-Manager als Mitglied in diesem Fall hinzufügen, die zweite eDiscovery-Manager nicht möglich, anzeigen oder öffnen die Groß-/Kleinschreibung auf der Seite **eDiscovery** in das Wertpapier &amp; Compliance Center. eDiscovery-Manager kann auch ihre Fällen in erweiterten eDiscovery Analysis Aufgaben zugreifen. 
    
  - **eDiscovery-Administrator** Kann alle Fallmanagement Aufgaben, bei denen eine eDiscovery-Manager tun kann. Darüber hinaus können eine eDiscovery-Administrator:
    
  - Anzeigen aller Fälle, die auf der Seite **eDiscovery-Fälle** aufgeführt sind. 
    
  - Verwaltet alle eDiscovery-Fall in der Organisation werden, nachdem sie sich als Mitglied der Groß-/Kleinschreibung hinzufügen.
    
  - Ausführen von Verwaltungsaufgaben in erweiterten eDiscovery, wie Verarbeiten von Groß-/Kleinschreibung Daten zur Analyse, Konfigurieren von Groß-/Kleinschreibung und Exportieren von Daten aus der erweiterten eDiscovery. Dies ist, da eine Person einer eDiscovery-Administrator in das Wertpapier &amp; Compliance Center wird automatisch als Administrator in erweiterten eDiscovery hinzugefügt.
    
    Überlegungen dazu, warum Sie ggf. einen eDiscovery-Administrator in Ihrer Organisation benötigen, finden Sie im Abschnitt [More information](manage-ediscovery-cases.md#moreinfo_1). 
    
> [!IMPORTANT]
> Wenn eine Person kein Mitglied einer dieser eDiscovery-bezogene Rollengruppen ist oder ist kein Mitglied einer Rollengruppe, die die Prüfer-Rolle zugewiesen hat, können nicht Sie sie als Mitglied einer eDiscovery-Fall hinzufügen. 
  
 **So weisen Sie eDiscovery-Berechtigungen zu**
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Berechtigungen**, und führen Sie dann eine der folgenden basierend auf den eDiscovery-Berechtigungen, die Sie zuweisen möchten.
    
  - Leseberechtigungen zuweisen, indem Sie wählen Sie aus der Rollengruppe " **Reviewer** ", und klicken Sie dann neben **Mitglieder** auf **Bearbeiten**. Klicken Sie auf **Elemente auswählen**, klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Hinzufügen** , wählen Sie den Benutzer, die Sie an der Rollengruppe Reviewer hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**.
    
  - EDiscovery-Manager-Berechtigungen zuweisen, indem Sie wählen Sie aus der Rollengruppe **eDiscovery-Manager** , und klicken Sie neben **eDiscovery-Manager**, klicken Sie dann auf **Bearbeiten**. Klicken Sie auf **auswählen, eDiscovery-Manager**, klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) ** hinzufügen **, wählen Sie den Benutzer, die Sie als ein eDiscovery-Manager hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**.
    
  - EDiscovery-Administratorberechtigungen zuweisen, indem Sie wählen Sie aus der Rollengruppe **eDiscovery-Manager** , und klicken Sie neben **eDiscovery-Administrator**, klicken Sie dann auf **Bearbeiten**. Klicken Sie auf **Choose eDiscovery-Administrator**, klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Hinzufügen**, wählen Sie den Benutzer, die Sie als einer eDiscovery-Administrator hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**.
    
4. Nachdem Sie alle Benutzer hinzugefügt haben, klicken Sie auf **Fertig**, klicken Sie auf **Speichern** , um die Änderungen an der Rollengruppe zu speichern, und klicken Sie dann auf **Schließen**.
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-2-create-a-new-case"></a>Schritt 2: Erstellen einer neuen Anfrage
<a name="step2_1"> </a>

Im nächste Schritt ist erstellen Sie einen neue eDiscovery-Fall. Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager zum Erstellen von eDiscovery-Fälle sein. Wie bereits erläutert, nach dem Erstellen eines neuen Vorgangs in das Wertpapier &amp; Compliance Center, Sie (und Mitgliedern der Groß-/Kleinschreibung) sein, dass dieselbe Groß-/Kleinschreibung im erweiterten eDiscovery, wenn Sie die Organisation sind ein Abonnement von Office 365 E5 hat zugreifen können.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery**, und klicken Sie dann auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Erstellen einer Anfrage**.
    
4. Benennen Sie auf der Seite **Neue Anfrage** der Groß-/Kleinschreibung, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **Speichern**. Beachten Sie, dass die Groß-/Kleinschreibung Name in Ihrer Organisation eindeutig sein muss.
    
    ![Neue Seite Groß-/Kleinschreibung](media/538f66b8-eb6e-4c4c-83d8-7154fd85883a.png)
  
    Die neue Groß-/Kleinschreibung wird in der Liste der Anfragen auf der Seite **eDiscovery** angezeigt. Beachten Sie, dass Sie den Cursor über einen Groß-/Kleinschreibung Namen zum Anzeigen von Informationen über die Groß-/Kleinschreibung, einschließlich des Status der Anfrage ( **aktiv** oder **geschlossen**), bewegen können die Beschreibung der die Groß-/Kleinschreibung (die im vorherigen Schritt erstellt wurde), und wenn die Groß-/Kleinschreibung zuletzt geändert wurde und Wer es geändert.
    
    > [!TIP]
    > Nachdem Sie einen neuen Vorgang erstellen, können Sie sie jederzeit umbenennen. Klicken Sie einfach auf den Namen der Anfrage auf der Seite **eDiscovery** . Klicken Sie auf der Seite flyoutmenü **Verwalten in diesem Fall** ändern Sie den Namen in das Feld unter **Name**angezeigt, und speichern Sie die Änderung. 
  
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-3-add-members-to-a-case"></a>Schritt 3: Hinzufügen von Mitgliedern zu einer Anfrage
<a name="step2a_1"> </a>

Nachdem Sie eine neue Anfrage erstellt haben, besteht der nächste Schritt, um die Groß-/Kleinschreibung Mitglieder hinzuzufügen. Wie vorherige erläutert, nur Benutzer, die Mitglieder des Bearbeiters sind oder eDiscovery-Manager Rollengruppen hinzugefügt werden können, als Mitglied der Groß-/Kleinschreibung. Beachten Sie, dass die eDiscovery-Manager, die die Groß-/Kleinschreibung erstellt automatisch als Mitglied hinzugefügt wird.
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der Anfrage, der Sie Mitglieder hinzufügen möchten.
    
    Seite flyoutmenü **Verwalten in diesem Fall** wird angezeigt. 
    
    ![Klicken Sie auf die Groß-/Kleinschreibung Namen zum Verwalten dieser Groß-/Kleinschreibung Seite anzeigen](media/2364dc08-a3dc-4724-acf4-7a68c8588e6f.png)
  
3. Klicken Sie unter **Manage Mitglieder**, klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Hinzufügen** , um die Groß-/Kleinschreibung Mitglieder hinzuzufügen. 
    
4. Aktivieren Sie in der Liste der Personen, die als Mitglied der Groß-/Kleinschreibung hinzugefügt werden können das Kontrollkästchen neben dem Namen der Personen ein, den, die Sie der Anfrage hinzufügen möchten.
    
    > [!TIP]
    > Wenn Sie haben eine umfangreiche Liste mit Personen, die Sie als Mitglieder hinzugefügt werden, verwenden Sie das Feld **Suchen** nach einer bestimmten Person in der Liste suchen. 
  
5. Nachdem Sie die Personen als Mitglieder der Gruppe hinzufügen ausgewählt haben, klicken Sie auf **Hinzufügen**.
    
    Klicken Sie in **diesem Fall verwalten**auf **Speichern** , um die neue Liste der Groß-/Kleinschreibung Elemente zu speichern. 
    
6. Klicken Sie auf **Speichern** , um die neue Liste der Groß-/Kleinschreibung Elemente zu speichern. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-4-place-content-locations-on-hold"></a>Schritt 4: Platzieren Speicherorte für Inhalte auf
<a name="step3_1"> </a>

EDiscovery-Fall können zum Erstellen von Haltestatus, um Inhalte zu erhalten, die für die Groß-/Kleinschreibung relevant sein könnten. Sie können einen Haltestatus auf Postfächer und OneDrive für Websites mit Geschäftsdaten von Personen tätigen, die in der Groß-/Kleinschreibung Verwalter sind. Sie können auch einen Haltestatus auf die Gruppe Postfach-, SharePoint-Website und OneDrive for Business-Site für eine Office 365-Gruppe platzieren. In ähnlicher Weise können Sie einen Haltestatus platzieren, auf das Postfach und die Website, die Microsoft-Teams zugeordnet sind. Wenn Sie die Speicherorte für Inhalte in der Warteschleife einleiten, wird Inhalt gespeichert, bis aus der Inhaltsspeicherort oder, bis Sie den Haltestatus löschen, entfernen den Haltestatus.
  
Wenn Sie einen Haltestatus erstellen, müssen Sie die folgenden Optionen aus, um den Inhalt zu begrenzen, der in der angegebenen Speicherorte für Inhalte gehalten wird:
  
- Sie erstellen eine unendliche halten, in dem alle Inhalte in der Warteschleife platziert wird. Alternativ können Sie eine abfragebasierte Aufbewahrung erstellen, in dem nur auf Inhalte, die eine Suchabfrage entspricht in der Warteschleife platziert wird.
    
- Sie können angeben, einen Datumsbereich nur die Inhalte enthalten, die gesendet, empfangen oder innerhalb des Datumsbereichs erstellt wurde. Alternativ können Sie alle Inhalte unabhängig davon Wenn es gesendet, empfangen oder erstellt wurde, halten.
    
> [!NOTE]
> Sie können maximal 10.000 Richtlinien halten Sie über alle eDiscovery-Fälle in Ihrer Organisation haben. 
  
Zum Erstellen eines Haltestatus für einen eDiscovery-Fall:
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf **Öffnen** neben der Groß-/Kleinschreibung, die Sie dem Haltestatus in erstellen möchten. 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **halten**.
    
    ![Klicken Sie auf halten, um die Groß-/Kleinschreibung Haltestatus Seite anzuzeigen.](media/25c0300a-bd33-4443-a121-d595b1a3e00f.png)
  
4. Klicken Sie auf der Seite **halten** **New**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).
    
5. Benennen Sie auf der Seite **erstellen einen neuen Haltestatus** dem Haltestatus. Der Name des Haltestatus muss in Ihrer Organisation eindeutig sein. 
    
6. Wählen Sie halten Sie die Speicherorte für Inhalte, denen Sie einfügen möchten. Sie können die Postfächer, Websites und Öffentliche Ordner in der Warteschleife platzieren.
    
    ![Wählen Sie Inhaltsspeicherorte aus, die im Haltebereich platziert werden sollen.](media/a00c952c-f91f-4708-b5a4-6213e4c413c7.png)
  
1. **Postfächer** Klicken Sie auf **Hinzufügen**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) an Postfächer in der Warteschleife platziert. Verwenden Sie das Suchfeld, um die Benutzerpostfächer und Verteilergruppen (in einem Haltestatus auf die Postfächer von Gruppenmitgliedern platzieren) Hier finden Sie in der Warteschleife platziert. Sie können auch einen Haltestatus auf das zugeordnete Postfach für eine Office 365-Gruppe oder ein Team Microsoft platzieren. 
    
    > [!NOTE]
    > Wenn Sie auf **Hinzufügen klicken**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) Postfächer im Archiv zu platzieren Sie zum angeben die Postfach-Auswahl, die angezeigt wird leer ist. Dies ist entwurfsbedingt zur Verbesserung der Leistung. Um Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld, und klicken Sie auf **Suche**![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif). 
  
2. **Websites** Klicken Sie auf **Hinzufügen**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) an SharePoint und OneDrive for Business-Websites in der Warteschleife platziert. Geben Sie die URL für die einzelnen Standorte, die Sie in die Warteschleife stellen möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder einem Microsoft-Team hinzufügen. 
    
<<<<<<< HEAD finden Sie unter der [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da#moreinfo_1) Abschnitt Tipps zur Office 365-Gruppen und Microsoft-Teams, in der Warteschleife an. === Finden Sie [Weitere Informationen](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da.aspx#moreinfo_1) im Abschnitt Tipps zur Office 365-Gruppen und Microsoft-Teams, in der Warteschleife an. 
>>>>>>> Deniseb-Konvertierung
    
    > [!NOTE]
    > In the rare case that a person's user principal name (UPN) is changed, the URL for their OneDrive account will also be changed to incorporate the new UPN. If this happens, you'll have to modify the hold by adding the user's new OneDrive URL and removing the old one. 
  
3. **Öffentliche Ordner** Klicken Sie auf **alle öffentlichen Ordner halten** , um alle öffentlichen Ordner in Ihrer Exchange Online-Organisation auf Archiv zu platzieren. Notiz, die Sie bestimmte Öffentliche Ordner zu hinzufügen auswählen können nicht halten. Lassen Sie die Option **nicht halten Sie Öffentliche Ordner** ausgewählt, wenn Sie keinen Haltestatus für Öffentliche Ordner aufnehmen möchten. 
    
7. Wenn Sie dem Haltestatus hinzufügen Inhaltsspeicherorte fertig sind, klicken Sie auf **Weiter**.
    
8. Führen Sie die folgenden Schritte aus, um eine abfragebasierte Aufbewahrung mit Bedingungen zu erstellen. Andernfalls, klicken Sie einfach auf **Fertig stellen** , um alle Inhalte enthalten. 
    
    ![Erstellen Sie eine abfragebasierte Aufbewahrung durch Angeben von Schlüsselwörtern und Bedingungen](media/a5bb802e-2e96-4f12-8b33-1ddd671638e4.png)
  
    Weitere Informationen zum Erstellen einer Suchabfrage und Bedingungen verwenden finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).
    
1. Im Feld unter **Was möchten Sie uns suchen?**, geben Sie eine Suchabfrage im, sodass nur die Inhalte, die die Suchkriterien entspricht in der Warteschleife platziert wird. Sie können Schlüsselwörter, Nachrichteneigenschaften oder Dokumenteigenschaften, wie Dateinamen angeben. Sie können auch komplexere Abfragen, die einen booleschen Operators, wie **AND**, **OR**oder **nicht**verwenden. Wenn Sie lassen halten Sie das Schlüsselwort Feld leer ist, und klicken Sie dann auf alle Inhalte befindet sich in der angegebenen Speicherorte für Inhalte platziert wird. 
    
2. Klicken Sie unter **Umständen**auf **Bedingung hinzufügen** , um eine oder mehrere Bedingungen einschränken die Suchabfrage für den Haltestatus hinzuzufügen. Jede Bedingung hinzugefügt der KQL Search-Abfrage, die erstellt und ausgeführt, wenn Sie den Haltestatus erstellen eine-Klausel. Beispielsweise können Sie einen Datumsbereich angeben, sodass e-Mail oder Website Dokumente, die in dem Bereich Datum erstellt wurden, in die Warteschleife gestellt werden. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch den **AND** -Operator verbunden. Das bedeutet, die Elemente beide erfüllen müssen halten die Stichwortabfrage und die Bedingung auf platziert werden. 
    
9. Halten Sie nach der Konfiguration einer abfragebasierte, und klicken Sie auf **Fertig stellen** , um den Haltestatus zu erstellen. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
### <a name="hold-statistics"></a>Halten Sie Statistiken

Informationen zu den neuen Haltestatus wird nach einer gewissen im Detailbereich auf der Seite **enthält** , für die ausgewählte Warteschleife angezeigt. Hierzu gehören die Anzahl von Postfächern Websites auf halten, und halten Sie Statistiken zu den Inhalt, der auf getätigt wurde, wie die gesamte Anzahl und Größe der Elemente in der Warteschleife platziert und der letzten Ausführung den Haltestatus, die Statistik berechnet wurden. Diese Dateien enthalten Statistiken Hilfe, die Sie ermitteln, wie viel Inhalt, die auf den eDiscovery-Fall zusammenhängt gehalten wird. 
  
![Halten Sie, dass im Detailbereich zum ausgewählten Haltebereich Statistiken angezeigt werden](media/e46359a3-cba1-4771-bbf5-bc53b4a2cb14.png)
  
Beachten Sie die folgenden Punkte berücksichtigen zu halten Statistiken:
  
- Die Gesamtzahl der Elemente in der Warteschleife gibt die Anzahl von Elementen aus allen Inhaltsquellen, die in der Warteschleife platziert werden. Wenn Sie erstellt haben halten eine abfragebasierte, diese Statistik gibt die Anzahl der Elemente an, die mit die Abfrage übereinstimmen.
    
- Die Anzahl der Elemente in der Warteschleife enthält auch nicht indizierten Elemente in die Speicherorte für Inhalte gefunden. Beachten Sie, wenn Sie eine abfragebasierte Aufbewahrung erstellen, werden alle nicht-indizierten Elemente in die Speicherorte für Inhalte in die Warteschleife gestellt. Dazu gehören nicht indizierten Elementen, die nicht die Suchkriterien des eine abfragebasierte Aufbewahrung entsprechen und nicht-indizierten Elementen, die außerhalb von Bereich Bedingung Datum liegen möglicherweise. Dies unterscheidet sich was geschieht, wenn Sie eine Inhaltssuche ausführen, in dem nicht indizierte Elementen, die die Suchabfrage stimmen nicht überein oder durch eine Datum Bereich Bedingung ausgeschlossen werden in den Suchergebnissen enthalten sind. Weitere Informationen zu nicht indizierten Elementen finden Sie unter [nicht-indizierten Elementen in Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md).
    
- Sie können die neuesten abrufen halten, schätzen Sie Statistiken, indem Sie auf eine Suche erneut ausführen, um **Statistiken zu aktualisieren** , die die aktuelle Anzahl von Elementen in der Warteschleife berechnet. Klicken Sie auf **Aktualisieren**, falls erforderlich,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) in der Symbolleiste auf die Warteschleife Statistiken im Detailbereich zu aktualisieren. 
    
- Normal für die Anzahl der Elemente auf halten über einen Zeitraum zu erhöhen, da Benutzer, dessen Postfach oder Website in der Warteschleife ist, in der Regel senden oder Empfangen von neuen e-Mail-Nachricht und erstellen neue SharePoint- und OneDrive für Geschäftsdokumente.
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>Schritt 5: Erstellen Sie und führen Sie einer eine Anfrage zugeordnete Inhaltssuche aus
<a name="step4_1"> </a>

Nach ein eDiscovery-Fall erstellt wird und alle Verwalter im Zusammenhang mit der Groß-/Kleinschreibung in die Warteschleife gestellt werden, können Sie erstellen und Ausführen von mindestens einen Content-Suche, die die Groß-/Kleinschreibung zugeordnet sind. Sucht eine Anfrage zugeordnet werden nicht angezeigt, auf **der Seite in das Wertpapier** Content &amp; Compliance Center. Dies bedeutet, die eine Anfrage Content-Suche zugeordnet kann nur von Groß-/Kleinschreibung Membern zugegriffen werden, die auch Mitglieder der Rollengruppe eDiscovery-Manager sind. 
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, die Sie erstellen eine Inhaltssuche in möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **Suchen**.
    
    ![Klicken Sie auf der Homepage der die Groß-/Kleinschreibung Suche](media/bd358eb3-12d4-4f0c-8317-d192286813d0.png)
  
4. Klicken Sie auf der Seite **Suche** auf **neu**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).
    
5. Geben Sie auf der Seite **neue Suche** einen Namen für die Suche ein. Content-Suche eine Anfrage zugeordnete müssen Namen aufweisen, die in Office 365-Organisation eindeutig sind. 
    
6. Wählen Sie die Speicherorte für Inhalte, die Sie suchen möchten. Sie können die Postfächer, Websites und Öffentliche Ordner in derselben Suche suchen.
    
    ![Suchen Sie Groß-/Kleinschreibung Inhaltsspeicherorte Speicherorte für alle Inhalte, oder wählen Sie bestimmte Speicherorte für Inhalte](media/08c523dc-cba8-4fce-aee6-f86251204393.png)
  
1. **Alle Inhalte Groß-/Kleinschreibung** Wählen Sie diese Option, um alle Speicherorte für die Inhalte zu suchen, die in der Warteschleife im Fall erteilt wurden. Wenn die Groß-/Kleinschreibung mehrere enthält enthält, den Inhalt, den Speicherorten alle Haltestatus durchsucht werden, wenn Sie diese Option auswählen. Darüber hinaus wurde auf eine abfragebasierte Aufbewahrung ein Inhaltsspeicherort eingefügt, werden nur die Elemente, die in der Warteschleife sind durchsucht, wenn Sie die Inhaltssuche ausführen, die Sie in diesem Schritt erstellen. Wenn ein Benutzer abfragebasierter Groß-/Kleinschreibung gehalten wurde, die Elemente beibehält, die gesendet oder vor einem bestimmten Datum erstellt wurden, würde beispielsweise nur die Elemente durchsucht werden mithilfe von die Suchkriterien für die Inhaltssuche. Dies geschieht durch Herstellen einer Verbindung mit der Groß-/Kleinschreibung Haltestatus Abfrage und die Inhaltssuche Abfrage nach einem **AND** -Operator. Finden Sie [Weitere Informationen](manage-ediscovery-cases.md#moreinfo_1) im Abschnitt am Ende dieses Artikels ausführliche Informationen zum Suchen von Inhalten Groß-/Kleinschreibung. 
    
2. **Suche überall** Wählen Sie diese Option, um alle Speicherorte für Inhalte in Ihrer Organisation zu suchen. Wenn Sie diese Option auswählen, Sie können festlegen, dass alle Exchange-Postfächer gesucht (enthält auch die Postfächer für alle Office 365-Gruppen und Microsoft-Teams), alle SharePoint und OneDrive for Business-Websites (einschließlich der Websites für alle Office 365-Gruppen und Microsoft Teams), und alle öffentlichen Ordner.
    
3. **Benutzerdefinierte Position Auswahl** Wählen Sie diese Option auswählen, die Postfächer und die Websites, die Sie suchen möchten. Wenn Sie diese Option auswählen, wird die Liste der Postfächer und Websites bereits ausgefüllte, mit dem Inhalt, die die Standorte, die platziert werden innerhalb der Groß-/Kleinschreibung enthalten. Sie können auch auswählen, um alle öffentlichen Ordner in Ihrer Organisation zu suchen.
    
    ![Durchsuchen Sie alle Groß-/Kleinschreibung Inhalt, suchen Sie alle Speicherorte oder suchen einen benutzerdefinierten Speicherort zu](media/7ca97ab4-52d5-46a5-9e24-e3a4d1001595.png)
  
    Wenn Sie wählen Sie diese Option aus, und suchen Sie alle Inhaltsspeicherort, in der ist enthalten jedoch, eine Abfrage aus einer Groß-/Kleinschreibung abfragebasierte Aufbewahrung wird nicht zur Suchabfrage angewendet werden. Anders ausgedrückt, alle Inhalte an einem Speicherort wird durchsucht, nicht nur die Inhalte, die von einer Groß-/Kleinschreibung abfragebasierte Aufbewahrung beibehalten wird.
    
    Sie können das bereits ausgefüllte Groß-/Kleinschreibung Speicherorte für Inhalte zu entfernen oder neue hinzufügen. Wenn Sie diese Option auswählen, müssen Sie auch Flexibilität, um alle Speicherorte für Inhalte für einen bestimmten Dienst (beispielsweise Durchsuchen aller Exchange-Postfächer) zu suchen, oder Sie können bestimmte Speicherorte für Inhalte für einen Dienst suchen. Sie können auch auswählen, ob er die öffentlichen Ordner in Ihrer Organisation zu suchen.
    
    Beachten Sie folgende Punkte beachten Sie beim Hinzufügen von Speicherorte für Inhalte zu suchen:
    
  - Wenn Sie auf **Hinzufügen klicken**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) zum Angeben von Postfächern zu suchen die Postfach-Auswahl, die angezeigt wird, ist leer. Dies ist entwurfsbedingt zur Verbesserung der Leistung. Um diese Liste Empfänger hinzuzufügen, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld, und klicken Sie auf **Suche**![Suchsymbol](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif).
    
  - Sie können die Liste der Postfächer Suchen inaktiver Postfächer, Gruppen von Office 365, Microsoft-Teams und Verteilergruppen hinzufügen. Dynamische Verteilergruppen werden nicht unterstützt. Wenn Sie Office 365 Gruppen oder Microsoft-Teams, hinzufügen, wird das Postfach Gruppe oder ein Team durchsucht; die Postfächer der Mitglieder der Gruppe werden nicht durchsucht.
    
  - Wenn Sie nicht in einer Suche keine Postfächer oder Websites einschließen möchten, wählen Sie **bestimmte Postfächer auswählen, um zu suchen** oder **Auswählen bestimmter Websites suchen**, aber fügen Sie nicht zur Liste Postfächer oder Websites hinzu.
    
  - Websites, klicken Sie auf **Hinzufügen**hinzufügen![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) und geben Sie die URL für die einzelnen Standorte, die Sie suchen möchten. Sie können auch die URL für die SharePoint-Website für Office 365-Gruppen und Microsoft-Teams hinzufügen. 
    
7. Ausgewählt, nachdem Sie die Speicherorte für Inhalte zu suchen, klicken Sie auf **Weiter**.
    
8. Auf der Seite **Neue Suche** können Sie Schlüsselwörter und Bedingungen zum Erstellen der Suchabfrage hinzufügen. 
    
    ![Suchkriterien und Bedingungen](media/9064147e-feac-4090-bbf6-2298ad7622c6.png)
  
1. Im Feld unter **Was möchten Sie uns suchen?**, geben Sie in das Feld eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Sie können eine komplexere Abfragen verwenden, die einen booleschen Operators, wie **und**, **oder**, **nicht**, **NEAR**oder **ONEAR**verwenden. Sie können auch suchen für vertrauliche Informationen (wie Sozialversicherungsnummern) in Dokumenten, oder suchen Sie nach Dokumenten, die extern freigegeben haben. Wenn Sie das Schlüsselwort Feld leer lassen, werden alle Inhalte, die in der angegebenen Speicherorte für Inhalte befindet sich in den Suchergebnissen enthalten sein. 
    
2. Sie können das Kontrollkästchen **Schlüsselwortliste anzeigen** und den Typ ein Schlüsselworts in jede Zeile klicken. Wenn Sie dies tun, werden die Schlüsselwörter für jede Zeile der **oder** -Operator in der Suchabfrage vorhanden, die erstellt wird. 
    
    ![Schlüsselwörter für die Suche](media/c3ef511a-e0a3-4b5d-9779-36803270a193.png)
  
    Gründe für die Verwendung der Schlüsselwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort überein. Dadurch können Sie schnell erkennen, welche Schlüsselwörter der am häufigsten (und mindestens) wirksam werden. Sie können auch eine Stichwortbegriff (in Klammern eingeschlossen sind) in einer Zeile. Weitere Informationen zu Suchstatistik finden Sie unter [schlüsselwortstatistiken für die Inhaltssuche Ergebnisse anzeigen](view-keyword-statistics-for-content-search.md).
    
    [Weitere Informationen](run-a-content-search-in-the-security-and-compliance-center.md#moreinfo)finden Sie weitere Informationen zur Verwendung der Liste Schlüsselwörter.
    
3. Klicken Sie auf **Abfrage für Tippfehler überprüfen** , überprüfen Sie Ihre Abfrage für nicht unterstützte Zeichen und boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Nicht unterstützte Zeichen werden häufig ausgeblendet und in der Regel verursacht einen Fehler beim Suchen oder unbeabsichtigte Ergebnisse zurückzugeben. Weitere Informationen zu nicht unterstützten Zeichen, die überprüft werden, finden Sie unter [Content Suchabfrage Fehler überprüfen](check-your-content-search-query-for-errors.md).
    
4. Fügen Sie unter **Conditions**Bedingungen auf eine Suchabfrage aus, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben. Jede Bedingung hinzugefügt der KQL Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch den **AND** -Operator verbunden. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und die Bedingung, die in den Ergebnissen enthalten sein müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. 
    
    Weitere Informationen zum Erstellen einer Suchabfrage sowie zur Verwendung von Bedingungen finden Sie unter [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
9. Klicken Sie auf **Suche**, um die Sucheinstellungen zu speichern und die Suche zu starten. 
    
    Die Suche wird gestartet. Nach einer gewissen wird eine Schätzung der Suchergebnisse im Detailfenster angezeigt. Die Schätzung für das enthält die Gesamtgröße und die Anzahl der Elemente, die die Suchkriterien entsprechen. Die Schätzung für das Search enthält auch die Anzahl der nicht-indizierten Elemente in die Speicherorte für Inhalte, die durchsucht wurden. In die Suchstatistik im Detailbereich angezeigt wird die Anzahl der nicht-indizierten Elemente, die den Suchkriterien entsprechen nicht enthalten sein. Wenn ein nicht-indizierten Element entspricht die Suche Abfragen (da es sich um eine andere Nachricht oder ein Dokument Eigenschaften den Suchkriterien entsprechen), werden nicht es in die geschätzte Anzahl der nicht-indizierten Elementen enthalten sein. Wenn ein nicht-indizierten Element durch die Suchkriterien ausgeschlossen wird, wird nicht in die Schätzung des nicht-indizierten Elementen eingeschlossen werden.
    
    Nachdem die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzuzeigen. Klicken Sie auf **Aktualisieren**, falls erforderlich,![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>Schritt 6: Exportieren Sie die Ergebnisse einer Inhaltssuche eine Anfrage zugeordnete
<a name="step5_1"> </a>

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse exportieren. Beim Exportieren von Suchergebnissen werden Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen. Beim Exportieren von Inhalt aus SharePoint und OneDrive for Business-Websites werden Kopien der systemeigenen Office-Dokumente und andere Dokumente exportiert. Eine Manifestdatei (im XML-Format), die Informationen über jedes Suchergebnis enthält, wird auch exportiert.
  
Sie können die Ergebnisse einer [Exportieren Sie die Ergebnisse von einem einzelnen Suchvorgang eine Anfrage zugeordnete](manage-ediscovery-cases.md#singlesearch_1) exportieren, oder Sie können die Ergebnisse der [Exportieren Sie die Ergebnisse von mehreren Suchvorgängen eine Anfrage zugeordnete](manage-ediscovery-cases.md#multiplesearches_1)exportieren.
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>Exportieren Sie die Ergebnisse einer einzelnen zugeordneten Suche dem Fall
<a name="singlesearch_1"> </a>

1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, der Sie Exportieren von durchsuchen möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **Suchen**.
    
4. Klicken Sie auf die Suche, die Sie Exportieren von Suchergebnissen aus, klicken Sie auf **Exportieren**möchten, in der Liste der Suche für die Groß-/Kleinschreibung,![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png), und klicken Sie dann auf **Exportieren Sie die Ergebnisse**.
    
    Die Seite " **Suchergebnisse" Export** "wird angezeigt. Der Workflow So exportieren Sie die Ergebnisse aus einer Inhaltssuche zugeordnet sind Fall exportieren die Suchergebnisse für eine Suche auf der Seite für die **Inhaltssuche** identisch ist. Schrittweise Anweisungen finden Sie unter [Export-Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md).
    
    > [!NOTE]
    > Wenn Sie die Suchergebnisse exportieren, müssen Sie die Option zum Deduplizierung aktivieren, sodass nur eine Kopie einer e-Mail-Nachricht exportiert werden, auch wenn mehrere Instanzen derselben Nachricht Postfächer gefunden wurden möglicherweise, die durchsucht wurden. Weitere Informationen zu Deduplizierung und wie doppelte Elemente erkannt werden, finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md). 
  
5. Nachdem Sie den Export starten, klicken Sie auf **Exportieren** , um die Liste der Exportaufträge anzuzeigen, die für diese Anfrage vorhanden sind. 
    
    ![Klicken Sie auf exportieren, um eine Liste der Exportaufträge anzuzeigen](media/b7b95bf7-134e-471e-961e-f86c1bb633eb.png)
  
    Möglicherweise müssen Sie auf **Aktualisieren**klicken![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) so aktualisieren Sie die Liste der Aufträge exportieren, um den Exportauftrag anzuzeigen, die Sie gerade erstellt haben. Beachten Sie, dass Exportaufträge denselben Namen wie die entsprechenden Inhalte suchen mit **_Export** bis zum Ende des Suchbegriff angefügt haben. 
    
6. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um Statusinformationen im Detailbereich anzuzeigen. Hierzu gehören den Prozentsatz der Elemente, die in einen Bereich Azure-Speicher in der Microsoft-Cloud übertragen wurden.
    
    Nachdem alle Elemente übertragen worden sind, klicken Sie auf **Download exportiert Ergebnisse** , um die Suchergebnisse auf den lokalen Computer herunterzuladen. Weitere Informationen finden Sie unter Schritt2 im [Export-Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>Exportieren Sie die Ergebnisse von mehreren Suchvorgängen Fall zugeordnet
<a name="multiplesearches_1"> </a>

Als Alternative zum Exportieren Sie die Ergebnisse einer einzelnen Content Suche eine Anfrage zugeordnet sind, können Sie die Ergebnisse von mehreren Suchvorgängen aus die gleiche Groß-/Kleinschreibung in einem einzelnen Export exportieren. Exportieren Sie die Ergebnisse von mehreren Suchvorgängen ist schneller und einfacher, als die Ergebnisse einer Suche zu einem Zeitpunkt exportieren.
  
> [!NOTE]
> Sie können nicht die Ergebnisse von mehreren Suchvorgängen zu exportieren, wenn eine die Suchvorgänge konfiguriert wurde, um alle Inhalte Groß-/Kleinschreibung zu suchen. Exportieren Sie nur die Ergebnisse von mehreren Suchvorgängen für Suchvorgänge, die einem eDiscovery-Fall zugeordnet sind. Können nicht exportiert werden die Ergebnisse von mehreren Suchvorgängen auf der Seite **Inhaltssuche** in das Wertpapier aufgeführten &amp; Compliance Center. 
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, der Sie Exportieren von durchsuchen möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **Suchen**.
    
4. Wählen Sie in der Liste der Suche für die Groß-/Kleinschreibung zwei oder mehr Suchvorgänge an, denen Sie von Suchergebnissen aus exportieren möchten.
    
    > [!NOTE]
    > Um mehrere Suchvorgänge auszuwählen, drücken Sie **STRG** , während Sie jeder Suche klicken. Oder Sie können mehrere benachbarte Suchvorgänge auswählen, indem auf der ersten suchen Sie **die UMSCHALTTASTE** gedrückt halten und dann auf die zuletzt durchgeführte Suche. 
  
5. Nachdem Sie die Suche ausgewählt haben, klicken Sie auf **Exportieren**![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png), und klicken Sie dann auf **Exportieren Sie die Ergebnisse**.
    
6. Die ** exportieren Sie die Suchergebnisse für Suchvorgänge *n* ** Seite angezeigt, wobei *n* die Anzahl der Suchvorgänge ist, die Sie Ergebnisse für exportieren. Beachten Sie, dass Sie dem Exportauftrag einen Namen geben müssen. 
    
    Der Workflow So exportieren Sie die Ergebnisse aus mehreren Content-Suche eine Anfrage zugeordnet ist dieselbe wie die Suchergebnisse für einen einzelnen Suchvorgang exportieren. Schrittweise Anweisungen finden Sie unter [Export-Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md).
    
    > [!NOTE]
    > Beim Exportieren von Suchergebnissen aus mehreren Suchvorgängen Fall zugeordnet haben Sie auch die Option zum Deduplizierung aktivieren, sodass nur eine Kopie einer e-Mail-Nachricht exportiert werden, auch wenn mehrere Instanzen derselben Nachricht gefunden wurden möglicherweise die Postfächer, die in einem oder mehreren der Suchvorgänge durchsucht wurden. Weitere Informationen zu Deduplizierung und wie doppelte Elemente erkannt werden, finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md). 
  
7. Nachdem Sie den Export starten, klicken Sie auf **Exportieren** , um die Liste der Export anzuzeigen, die für diese Anfrage Aufträge. 
    
    ![Klicken Sie auf exportieren, um eine Liste der Exportaufträge anzuzeigen](media/b7b95bf7-134e-471e-961e-f86c1bb633eb.png)
  
    Möglicherweise müssen Sie auf **Aktualisieren**klicken![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) so aktualisieren Sie die Liste der Aufträge exportieren, um den Exportauftrag anzuzeigen, die Sie gerade erstellt haben. Beachten Sie, dass die suchen, die in den Exportauftrag enthalten waren in der Spalte **Suchvorgänge** aufgeführt sind. 
    
8. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um Statusinformationen im Detailbereich anzuzeigen. Hierzu gehören den Prozentsatz der Elemente, die in einen Bereich Azure-Speicher in der Microsoft-Cloud übertragen wurden.
    
9. Nachdem alle Elemente übertragen worden sind, klicken Sie auf **Download exportiert Ergebnisse** , um die Suchergebnisse auf den lokalen Computer herunterzuladen. Weitere Informationen finden Sie unter Schritt2 im [Export-Suchergebnisse aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>Weitere Informationen zum Exportieren die Ergebnisse von mehreren Suchvorgängen

- Wenn Sie die Ergebnisse von mehreren Suchvorgängen exportieren, die Suchabfragen aus allen Suchvorgängen mithilfe von **oder** -Operatoren kombiniert werden, und klicken Sie dann die Kombinierte Suche gestartet wird. Die geschätzte kombinierte Suchergebnisse werden im Detailbereich des Auftrags für ausgewählte Export angezeigt. Die Suchergebnisse werden in der Azure-Speicher-Bereich in der Microsoft-Cloud übertragen. Der Status der Übertragung wird auch im Detailbereich angezeigt. Wie bereits zuvor erwähnt nachdem die Suchergebnisse übertragen worden sind, können Sie diese auf den lokalen Computer herunterladen. 
    
- Die maximale Anzahl von Stichwörtern aus der Suchabfragen für alle Suchvorgänge, die Sie exportieren möchten, beträgt 500. (Dies ist die gleiche Grenzwert für eine einzelne Inhaltssuche). Dies liegt daran des Exportvorgangs die Suchabfragen mithilfe des Operators **OR** kombiniert. Wenn Sie diesen Grenzwert überschreiten, wird ein Fehler zurückgegeben. In diesem Fall müssen Sie die Ergebnisse aus weniger Suchvorgänge exportieren oder vereinfachen die Suchabfragen der Suchvorgänge, die Sie exportieren möchten. 
    
- Die Suchergebnisse, die exportiert werden sind von der Inhaltsquelle organisiert, die, denen in das Element gefunden wurde. Dies bedeutet, dass eine Inhaltsquelle in die Exportergebnisse möglicherweise mit anderen Suche zurückgegebenen Elemente muss. Angenommen, wenn Sie e-Mail-Nachrichten in eine PST-Datei für jedes Postfach exportieren möchten, haben die PST-Datei Ergebnisse aus mehreren Suchvorgänge.
    
- Wenn das gleiche e-Mail-Element oder Dokument aus der gleichen Speicherort des Inhalts von mehr als einer der Suchvorgänge, die Sie exportieren zurückgegeben wird, wird nur eine Kopie des Elements exportiert werden.
    
- Sie können für mehrere Suchvorgänge nach exportieren nach ihrer Erstellung nicht bearbeiten. Sie können nicht beispielsweise hinzufügen oder Entfernen von Suchvorgänge vom Export. Sie müssen zum Erstellen eines neuen Auftrags Export zum Ändern der Suchergebnisse exportiert werden. Nach dem Erstellen eines Auftrags exportieren können Sie nur die Ergebnisse auf einen Computer herunterladen, starten den Export oder Löschen des Exportvorgangs.
    
- Wenn Sie den Export neu starten, werden nicht Änderungen an der Abfragen der Suchvorgänge, die den Exportauftrag bilden die Suchergebnisse, die abgerufen werden sollen. Wenn Sie einen Export neu starten, werden der gleichen kombinierten Search-Abfrage Auftrag, der ausgeführt wurde, bei der Erstellung des Exportvorgangs erneut ausgeführt.
    
- Wenn Sie einen Export aus der Seite **Exporte** in einem eDiscovery-Fall neu starten, werden die Suchergebnisse, die in den Bereich der Azure-Speicher übertragen werden die vorherigen Ergebnisse überschrieben; die vorherigen Ergebnisse gab es übertragen nicht verfügbar heruntergeladen werden. 
    
- Die Ergebnisse von mehreren Suchvorgängen für die Analyse in erweiterten eDiscovery vorbereitet ist nicht verfügbar. Sie können nur die Ergebnisse von einem einzelnen Suchvorgang für die Analyse in erweiterten eDiscovery vorbereiten.
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>Schritt 7: Vorbereiten der Suchergebnisse für erweiterte eDiscovery
<a name="step7_1"> </a>

Wenn Ihre Organisation ein E5 für Office 365-Abonnement umfasst, können Sie die Ergebnisse der Content-Suche eine Anfrage für die Analyse in erweiterten eDiscovery zugeordnete vorbereiten. Nachdem Sie die Suchergebnisse vorbereitet haben, können Sie zu erweiterten eDiscovery wechseln (finden Sie unter [Schritt 8: Wechseln Sie zu der erweiterten eDiscovery-Fall](manage-ediscovery-cases.md#gotoAeD_1)) und die Suche Ergebnisdaten zur weiteren Analyse in erweiterten eDiscovery verarbeiten können.
  
Wenn Sie die Suchergebnisse für erweiterte eDiscovery vorbereiten, extrahiert optischen zeichenerkennung (OCR)-Funktionalität Text automatisch von Bildern. OCR wird unterstützt für lose Dateien, e-Mail-Anlagen und eingebettete Bilder. Dadurch können Sie die Text-Analysefunktionen der erweiterten eDiscovery (in der Nähe Duplikate, e-Mail-threading, Designs und vorhersehbare codieren) auf Text, der im Bilddateien anwenden.
  
> [!NOTE]
> Um eine erweiterte eDiscovery mit Benutzerdaten zu analysieren, muss der Benutzer (der Verwaltungsberechtigte der Daten) eine Lizenz für Office 365 E5 zugewiesen werden. Alternativ können der Benutzer mit einer Lizenz für Office 365 E1 oder E3 eine erweiterte eDiscovery eigenständige Lizenz zugewiesen werden. Administratoren und Compliance Officer, die zugewiesenen Fällen und erweiterte eDiscovery verwenden, um Daten zu analysieren erforderlich keine E5-Lizenz. 
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, die Sie Suchergebnisse für die Analyse in erweiterten eDiscovery vorbereiten möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** auf **Suchen**, und wählen Sie dann Suche aus.
    
4. Klicken Sie im Detailbereich unter **Analyze Ergebnisse mit erweiterten eDiscovery**auf **Prepare-Ergebnisse für die Analyse**.
    
5. Gehen Sie auf der Seite **Ergebnisse für Analyse vorbereiten** folgendermaßen vor:  
    
  - Verhindern Sie, dass indizierte Elemente, indiziert und nicht-indizierten Elemente oder nur nicht-indizierten Elemente für die Analyse in erweiterten eDiscovery vorzubereiten.
    
  - Wählen Sie, ob alle Versionen von Dokumenten in SharePoint, die die Suchkriterien erfüllen gefunden werden sollen. Diese Option ist nur dann, wenn die Inhaltsquellen für die Suche umfasst Websites.
    
  - Geben Sie an, ob eine Benachrichtigung gesendet (oder kopiert) an eine Person aus, wenn die Vorbereitung abgeschlossen ist und die Daten ist bereit, die im erweiterten eDiscovery verarbeitet werden soll.
    
6. Klicken Sie auf **Vorbereiten**.
    
    Die Suchergebnisse sind für die Analyse mit erweiterten eDiscovery vorbereitet.
    
7. Klicken Sie im Detailbereich auf **Überprüfen Vorbereitung Status** zum Anzeigen von Informationen über den Prozess zur Vorbereitung. Wenn die Vorbereitung abgeschlossen ist, navigieren Sie zu der Groß-/Kleinschreibung im erweiterten eDiscovery zum Verarbeiten der Daten für die Analyse. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>Schritt 8: Wechseln Sie zu der erweiterten eDiscovery-Fall
<a name="gotoAeD_1"> </a>

Nach dem Erstellen einer Anfrage in das Wertpapier &amp; Compliance Center, können Sie auf die gleiche Groß-/Kleinschreibung im erweiterten eDiscovery wechseln.
  
Wechseln Sie zu einer erweiterten eDiscovery-Fall:
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben die Groß-/Kleinschreibung, die Sie in der erweiterten eDiscovery wechseln möchten **Öffnen** . 
    
3. Klicken Sie auf **der Homepage für den Fall** **Schalter, mit dem erweiterten eDiscovery**auf.
    
    ![Klicken Sie auf Wechseln zu erweiterten eDiscovery So öffnen Sie die Groß-/Kleinschreibung in erweiterten eDiscovery](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    **Herstellen einer Verbindung mit erweiterten eDiscovery** Statusanzeige wird angezeigt. Wenn Sie erweiterte eDiscovery verbunden sind, wird eine Liste der Container auf der Seite angezeigt. 
    
    ![Die Groß-/Kleinschreibung wird in erweiterten eDiscovery angezeigt.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
    Diese Container darstellen der Suchergebnisse, die Sie für die Analyse in erweiterten eDiscovery in Schritt 7 vorbereitet haben. Beachten Sie, dass der Name des Containers den gleichen Namen wie Inhaltssuche im Fall in das Wertpapier hat &amp; Compliance Center. Der Container in der Liste sind diejenigen aus, denen Sie vorbereitet haben. Wenn ein anderer Benutzer die Suchergebnisse für die erweiterte eDiscovery vorbereitet, wird nicht die entsprechenden Container in der Liste enthalten.
    
4. Wählen Sie einen Container, und klicken Sie auf **Fortsetzen**, um die Suche Ergebnisdaten aus einem Container zu der erweiterten eDiscovery-Fall zu laden.
    
    Informationen zum Prozess Containern finden Sie unter [Ausführen des Moduls Prozess und Laden von Daten in Office 365 erweiterte eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md).
    
> [!TIP]
> Klicken Sie auf **Schalter, mit dem eDiscovery** , um die gleiche Groß-/Kleinschreibung in das Wertpapier wieder zu &amp; Compliance Center. 
  
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="optional-step-9-close-a-case"></a>(Optional) Schritt 9: Schließen Sie eine Anfrage
<a name="closecase_1"> </a>

Wenn der Fall, rechtliche oder von einem eDiscovery-Fall unterstützt Untersuchung abgeschlossen ist, können Sie die Groß-/Kleinschreibung schließen. Hier ist, was geschieht, wenn Sie eine Anfrage abschließen:
  
- Wenn die Groß-/Kleinschreibung alle Speicherorte für Inhalte in der Warteschleife enthält, werden dieser Aufbewahrungspflichten deaktiviert werden. Content wird dadurch kann dauerhaft gelöscht oder bereinigt, durch den Benutzer oder durch ein automatisierter Prozess, wie eine Richtlinie löschen.
    
- Schließen nur eine Anfrage wird deaktiviert den Haltestatus an, die diesem Vorgang zugeordnet sind. Wenn andere Aufbewahrungen auf einen Inhaltsspeicherort (beispielsweise eine Aufbewahrung für eventuelle Haltestatus. eine Beibehaltung der Richtlinie oder für ein Archiv aus einem anderen eDiscovery-Fall) sind, werden dieser Aufbewahrungspflichten weiterhin verwaltet werden.
    
- Die Groß-/Kleinschreibung wird weiterhin auf der Seite eDiscovery in das Wertpapier aufgeführt &amp; Compliance Center. Die Details, Haltestatus, Suchvorgänge und Mitglieder der Fall geschlossen werden beibehalten.
    
- Sie können eine Anfrage bearbeiten, nachdem er geschlossen wurde. Beispielsweise können Sie hinzufügen oder beim Entfernen von Mitgliedern Suchvorgänge erstellen, Exportieren von Suchergebnissen und Analysen in erweiterten eDiscovery Suchergebnis vorbereiten. Der Hauptunterschied zwischen aktiven und geschlossenen Fällen ist, dass Haltestatus deaktiviert sind, wenn eine Anfrage geschlossen wird.
    
So schließen Sie eine Anfrage:
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der Anfrage, die Sie löschen möchten.
    
    Seite flyoutmenü **Verwalten in diesem Fall** wird angezeigt. 
    
3. Klicken Sie unter **Manage Anfragestatus**auf ![Entfernen der Schaltfläche Blick](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) **Fall schließen**.
    
4. Klicken Sie auf der Seite **Details** auf **Fall schließen**.
    
    Eine Warnung besagt, dass die Aufbewahrungspflichten zugeordnete die Groß-/Kleinschreibung deaktiviert angezeigt.
    
5. Klicken Sie auf **Ja,** um die Groß-/Kleinschreibung zu schließen. 
    
    Der Status auf der Seite **Verwalten in diesem Fall** flyoutmenü wird von **aktiv** in **geschlossen**geändert.
    
6. **In diesem Fall verwalten**zu schließen.
    
7. Klicken Sie auf der Seite **eDiscovery** auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren des Status von den geschlossenen Fall **Aktualisieren** . Es kann bis zu 60 Minuten für die Durchführung der Schließvorgang dauern. 
    
    Wenn der Vorgang abgeschlossen ist, wird der Status der Anfrage in **Schließen** auf der Seite **eDiscovery** geändert. Klicken Sie auf den Namen der Groß-/Kleinschreibung erneut aus, um die Seite **Verwalten in diesem Fall** flyoutmenü anzuzeigen, die Informationen zu enthält die Groß-/Kleinschreibung geschlossen wurde und, die es geschlossen. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="optional-step-10-re-open-a-closed-case"></a>(Optional) Schritt 10: Eine geschlossene Anfrage erneut öffnen
<a name="reopencase_1"> </a>

Wenn Sie eine Anfrage erneut öffnen, werden nicht automatisch alle Haltestatus an, die vorhanden waren, wenn die Groß-/Kleinschreibung geschlossen wurde reaktiviert werden. Nachdem die Groß-/Kleinschreibung erneut geöffnet ist, müssen Sie wechseln Sie zur Seite **halten** , und aktivieren Sie in der vorherigen enthalten sind. Um einem Haltestatus zu aktivieren, wählen Sie sie aus, und klicken Sie im Detailbereich auf **schalten Sie es** . 
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der Anfrage, die Sie erneut öffnen möchten.
    
    Seite flyoutmenü **Verwalten in diesem Fall** wird angezeigt. 
    
3. Klicken Sie unter **Verwalten von Anfragestatus**klicken Sie auf **Fall erneut zu öffnen**.
    
    Eine Warnung besagt, dass der Haltestatus an, die beim Schließen war die Groß-/Kleinschreibung zugeordnet waren automatisch aktiviert werden nicht angezeigt.
    
4. Klicken Sie auf **Ja,** um die Groß-/Kleinschreibung erneut zu öffnen. 
    
    Der Status auf der Seite **Verwalten in diesem Fall** flyoutmenü wird von **geschlossen** in **aktiv**geändert.
    
5. **In diesem Fall verwalten**zu schließen.
    
6. Klicken Sie auf der Seite **eDiscovery** auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** zum Aktualisieren des Status der Anfrage erneut geöffnet. Es kann bis zu 60 Minuten für den Prozess erneut öffnen, für die Durchführung dauern. 
    
    Wenn der Vorgang abgeschlossen ist, wird der Status der Anfrage auf der Seite **eDiscovery** in **aktiv** geändert. 
    
[Zurück zum Seitenanfang](manage-ediscovery-cases.md#top)
  
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo_1"> </a>

- **Gibt es Grenzwerte für eDiscovery-Fälle oder enthält, die einem eDiscovery-Fall zugeordnet?** Die folgende Tabelle enthält die Grenzwerte für eDiscovery-Fälle und Groß-/Kleinschreibung enthält.
    
|**Beschreibung der Beschränkung**|**Grenzwert**|
|:-----|:-----|
|Maximale Anzahl von Fällen für eine Organisation  <br/> |Keine Begrenzung  <br/> |
|Maximale Anzahl der Fall enthält für eine Organisation  <br/> |10,000  <br/> |
|Maximale Anzahl von Postfächern in einem einzelnen Groß-/Kleinschreibung Haltestatus  <br/> |1,000  <br/> |
|Maximale Anzahl von SharePoint- und OneDrive for Business-Websites in einem einzigen Groß-/Kleinschreibung Haltestatus  <br/> |100  <br/> |
   
- **Wie sieht Anfragen, die auf der Seite Fallmanagement in erweiterten eDiscovery erstellten?** Sie können eine Liste der älteren erweiterte eDiscovery-Fälle zugreifen, indem Sie auf den Link klicken Sie unten auf der Seite **eDiscovery** in das Wertpapier &amp; Compliance Center. Klicken Sie dazu sämtliche Ressourcen in einem älteren Fall müssen Sie jedoch Kontaktieren des Supports für Office 365 und anfordern, dass die Groß-/Kleinschreibung zu einer neuen eDiscovery-Fall in das Wertpapier verschoben werden &amp; Compliance Center. 
    
- **Gründe für das Erstellen einer eDiscovery-Administrator?** Wie bereits erläutert, eine eDiscovery, den Administrator Mitglied der Gruppe der eDiscovery-Manager-Rolle ist, anzeigen und alle eDiscovery-Fälle in Ihrer Organisation zugreifen kann. Diese Möglichkeit zum Zugriff auf die eDiscovery-Fälle hat zwei wichtige Funktionen:
    
  - Wenn eine Person, die das einzige Mitglied einer eDiscovery-Fall ist Ihre Organisation verlässt, kann niemand (einschließlich Mitglieder der Rollengruppe "Organisationsverwaltung" oder ein anderes Mitglied der Rollengruppe eDiscovery-Manager), eDiscovery-Fall zugreifen, da der Mitglied sind nicht der Fall. In diesem Fall würde keine Möglichkeit, den Zugriff auf die Groß-/Kleinschreibung vorhanden sein. Da eine eDiscovery-Administrator alle eDiscovery-Fälle, in der Organisation zugreifen kann, können sie die Groß-/Kleinschreibung in das Wertpapier anzeigen, aber &amp; Compliance Center und Hinzufügen von sich selbst oder einem anderen eDiscovery-Manager als Mitglied der Groß-/Kleinschreibung.
    
  - Da eine eDiscovery-Administrator kann anzeigen und Zugriff auf alle eDiscovery-Fälle, können sie überwachen und überwachen alle Anfragen und zugehörige Content-Suche. Dies hilft um Missbrauch des Content-Suche oder eDiscovery-Fälle zu verhindern. Und da eDiscovery Administratoren möglicherweise vertraulichen Informationen in den Ergebnissen einer Inhaltssuche zugreifen kann, sollten Sie die Anzahl der Personen, die eDiscovery-Administratoren sind beschränken.
    
    Schließlich wie vorherige erläutert, eDiscovery-Administratoren in das Wertpapier &amp; Compliance Center werden automatisch als Administratoren in erweiterten eDiscovery hinzugefügt. Dies bedeutet, dass eine Person, die einer eDiscovery-Administrator ist in erweiterten eDiscovery, wie Einrichten von Benutzern, Erstellen von Fällen und Hinzufügen von Daten zu Fällen administrative Aufgaben ausführen kann.
    
<<<<<<< HEAD
- **Was lizenzierungsanforderungen Speicherorte für Inhalte in der Warteschleife platziert werden?** Im Allgemeinen Organisationen benötigen ein Abonnement von Office 365 E3 oder höher, um die Speicherorte für Inhalte in die Warteschleife stellen. Eine Lizenz für Exchange Online – Plan 2 ist erforderlich, um Postfächer im Archiv zu platzieren. Weitere Informationen finden Sie unter diesem [FAQ zu eDiscovery](https://support.office.com/article/9d1a29ae-b7b4-4a27-9c8c-84289023dcae#Q5). =======
- **Was lizenzierungsanforderungen Speicherorte für Inhalte in der Warteschleife platziert werden?** Im Allgemeinen Organisationen benötigen ein Abonnement von Office 365 E3 oder höher, um die Speicherorte für Inhalte in die Warteschleife stellen. Eine Lizenz für Exchange Online – Plan 2 ist erforderlich, um Postfächer im Archiv zu platzieren. Weitere Informationen finden Sie unter diese [– häufig gestellte Fragen](https://support.office.com/article/9d1a29ae-b7b4-4a27-9c8c-84289023dcae.aspx#Q5).
>>>>>>> Deniseb-Konvertierung
    
- **Was sollten Sie wissen, zur Suche alle Groß-/Kleinschreibung Inhalte in Schritt 5?** Wie bereits erklärt, suchen Sie die halten Sie die Speicherorte für Inhalte, die für erteilt wurden in die Groß-/Kleinschreibung. Wenn Sie dies tun, wird nur die Inhalte, die den Haltestatus Kriterien entspricht suchen. Ist keine Haltekriterien, wird alle Inhalte durchsucht. Wenn Inhalt auf eine abfragebasierte halten, nur die Inhalte, halten Sie beide Übereinstimmungen Kriterien (aus dem Haltestatus platziert in Schritt 4), und die Suchkriterien (von der Suche in Schritt 5) wird mit den Suchergebnissen zurückgegeben.
    
    Es folgen einige andere Dinge im Hinterkopf behalten, alle Inhalte Groß-/Kleinschreibung zu suchen:
    
  - Wenn ein Inhaltsspeicherort Teil der verschiedenen Archiven innerhalb der gleichen Fall ist, werden die Warteschleife Abfragen durch einen Operator **oder** kombiniert bei der Suche, mit der alle Groß-/Kleinschreibung Content Option Inhaltsspeicherort. In ähnlicher Weise ein Inhaltsspeicherort ist Teil zwei enthält verschiedene, in dem eine abfragebasierte ist und der andere eine unendliche Warteschleife (wobei alle Inhalte in die Warteschleife gestellt wird), und klicken Sie dann alle Inhalte aufgrund unendlichen Haltebereich Suche durchgeführt wird. 
    
  - Wenn eine Inhaltssuche für eine Anfrage ist und konfiguriert haben, um alle Inhalte Groß-/Kleinschreibung zu suchen, und ändern Sie einen Haltestatus (durch Hinzufügen oder entfernen einen Inhaltsspeicherort oder Ändern der Abfrage Haltestatus), wird die Konfiguration mit diesen Änderungen aktualisiert. Sie müssen jedoch erneut ausführen der Suche nach der Haltebereich geändert wird, um die Suchergebnisse zu aktualisieren.
    
  - Wenn mehrere Groß-/Kleinschreibung Haltestatus auf einen Inhaltsspeicherort in einem eDiscovery-Fall platziert werden und Sie auswählen, dass um alle Inhalte Groß-/Kleinschreibung zu suchen, ist die maximale Anzahl von Stichwörtern für diese Suchabfrage 500. Dies liegt daran die Inhaltssuche alle abfragebasierter Haltestatus mithilfe des Operators **OR** kombiniert. Wenn vorhanden, dass mehr als 500 Schlüsselwörter in der kombinierten Abfragen und die Abfrage für die Inhaltssuche halten sind, enthält klicken Sie dann im Postfach alle Inhalte durchsucht wird, nicht nur, dass Inhalte, die mit einer abfragebasierte Groß-/Kleinschreibung übereinstimmt. 
    
  - Weist ein Groß-/Kleinschreibung Haltestatus Status **Einschalten**, können Sie weiterhin die Groß-/Kleinschreibung Speicherorte für Inhalte durchsuchen zwar der Haltestatus eingeschaltet.
    
  - Wie bereits erwähnt, wenn eine Suche konfiguriert ist, um alle Inhalte zu diesem Fall, suchen Sie, dass die Suche aufnehmen können nicht, wenn Sie die Ergebnisse von mehreren Suchvorgängen exportieren möchten. Wenn eine Suche konfiguriert ist, um alle Inhalte Groß-/Kleinschreibung zu suchen, müssen Sie die Ergebnisse dieser einzelnen Suche exportiert werden.
    
- **Wie sieht es aus einen Haltestatus auf Office 365-Gruppen und Microsoft-Teams, platzieren?** Microsoft-Teams, basieren auf Office 365-Gruppen. Ordnen sie in der Warteschleife in einem eDiscovery-Fall ist daher sehr ähnlich. Berücksichtigen Sie die folgenden Punkte berücksichtigen, bei der platzieren Office 365-Gruppen und Microsoft-Teams auf halten. 
    
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
    > Um das Cmdlet **Get-UnifiedGroup** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
  - Wenn dem Postfach eines Benutzers durchsucht wird, werden keine Office 365-Gruppe oder der Microsoft-Teams, die der Benutzer Mitglied ist gesucht werden soll. Wenn Sie eine Office 365-Gruppe platzieren oder Microsoft Team halten, nur die Gruppenpostfach und Gruppenseite platziert werden auf ähnliche Weise, halten Sie; Postfächer und OneDrive for Business-Websites Gruppenmitglieder werden nicht in die Warteschleife gestellt, es sei denn, Sie explizit dem Haltestatus hinzufügen. Wenn Sie die Notwendigkeit, setzen Sie ein Office 365-Gruppe oder der Microsoft-Teams auf halten rechtlichen Gründen sollten Sie Postfächer und OneDrive for Business-Websites für Gruppe und Team Mitglieder auf demselben hinzufügen daher zu halten.
    
  - Wenn Sie eine Liste der Mitglieder einer Gruppe von Office 365 oder Microsoft-Teams erhalten möchten, können Sie die Eigenschaften anzeigen, auf die **Home \> Gruppen** Seite im Office 365 Administrationscenter. Alternativ können Sie in Exchange Online PowerShell den folgenden Befehl ausführen: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Um das Cmdlet **Get-UnifiedGroupLinks** ausführen, müssen Sie die Rolle des Kontaktobjekts Empfänger in Exchange Online zugewiesen werden, oder ein Mitglied einer Rollengruppe sein hat, die die Rolle des Kontaktobjekts Empfänger zugewiesen. 
  
  - Unterhaltungen, die Teil eines Microsoft-Teams Kanals sind werden im Postfach gespeichert, die mit dem Microsoft-Team zugeordnet ist. In ähnlicher Weise werden Dateien, die in einem Kanal Teammitglieder freigeben auf das Team SharePoint-Website gespeichert. Daher müssen Sie das Microsoft-Teams Postfach platzieren und SharePoint-Website auf halten, um Unterhaltungen und Dateien in einem Kanal beibehalten werden.
    
    Alternativ werden Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams, sind in das Postfach des Benutzers, die im Chat teilnehmen gespeichert. Und Dateien, die ein Benutzer in Chat Unterhaltungen gemeinsam in die OneDrive for Business-Website des Benutzers, der die Dateifreigaben gespeichert werden. Daher müssen Sie die einzelnen Benutzerpostfächer platzieren und OneDrive for Business-Websites auf halten, um Unterhaltungen und Dateien in der Liste Chat beibehalten werden. Deshalb ist es ratsam, eine Aufbewahrung legen Sie für die Postfächer der Elemente von einem Microsoft-Team zusätzlich zum Platzieren der teampostfächer (und die Website) in der Warteschleife ist.
    
    > [!IMPORTANT]
    > Exchange Online (Cloud-basierten)-Postfach benötigen Benutzer, die Unterhaltungen teilnehmen, die Teil der Liste der Chat in Microsoft-Teams sind, um Chat Unterhaltungen beibehalten, wenn das Postfach eine eDiscovery gehalten wird. Dies liegt daran Unterhaltungen, die Teil der Liste der Chat sind in der Cloud-basierten Postfächern Chat Teilnehmer gespeichert sind. Wenn ein Teilnehmer Chat ein Exchange Online-Postfach besitzt, werden Sie kann nicht Chat Unterhaltungen beibehalten. Beispielsweise können in einer Exchange-hybridbereitstellung Benutzer mit einem lokalen Postfach möglicherweise zur Teilnahme an Unterhaltungen, die Teil der Liste der Chat in Microsoft-Teams sind. Jedoch kann nicht in diesem Fall-Inhalten in dieser Unterhaltung beibehalten, da der Benutzer nicht über cloudbasierten Postfächer verfügen. 
  
  - Jede Microsoft-Teams oder ein Team Kanal enthält ein Wiki für Notizen und die Zusammenarbeit. Der Wiki-Inhalt wird automatisch in eine Datei mit einem MHT-Format gespeichert. Diese Datei ist in der Dokumentbibliothek Teams Wiki-Daten auf SharePoint-Teamwebsite gespeichert. Sie können den Inhalt im Wiki in der Warteschleife tätigen, indem Sie das Team SharePoint-Website in der Warteschleife platziert.
    
    > [!NOTE]
    > Die Möglichkeit zum Beibehalten von Wiki-Inhalten für einen Microsoft-Teams oder ein Team-Kanal (Wenn Sie das Team SharePoint-Website in die Warteschleife stellen) wurde am 22 Juni 2017 veröffentlicht. Wenn auf eine Teamwebsite ist halten Sie, das Wiki Inhalte an diesem Datum starten aufbewahrt werden. Jedoch wurde Wenn eine Teamwebsite in der Warteschleife wird und die Wiki-Inhalte vor dem 22 Juni 2017 gelöscht wurde nicht der Inhalt Wiki beibehalten. 
  
- **Wie finde ich heraus die URL für OneDrive for Business-Websites?** Eine Liste der URLs von Websites mit Geschäftsdaten in Ihrer Organisation, sodass Sie diese einem Haltebereich hinzufügen oder suchen können mit einem eDiscovery-Fall verknüpften finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)für die OneDrive erfassen möchten. Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Wenn Sie dieses Skript ausführen, müssen Sie zum Installieren und Verwenden von SharePoint Online-Verwaltungsshell. Achten Sie darauf, dass Sie die URL für die MySite Domäne Ihrer Organisation an jedem Standort OneDrive angefügt werden soll, die Sie suchen möchten. Dies ist die Domäne, die alle Ihre OneDrive enthält. beispielsweise `https://contoso-my.sharepoint.com`. Es folgt ein Beispiel für die URL der Website eines Benutzers OneDrive: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.

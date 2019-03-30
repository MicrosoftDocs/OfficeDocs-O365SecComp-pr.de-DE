---
title: eDiscovery-Fälle im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 8dd335ab-29d0-41c3-8dd8-9f7c7481e60c
description: Verwenden Sie das Security & Compliance Center, um eDiscovery-Fälle in Ihrer Organisation zu erstellen und zu verwalten. Sie können dem Fall Mitglieder zuweisen, inhaltsspeicherorte in der Warteschleife platzieren, mit dem Fall verknüpfte Inhalts suchVorgänge ausführen und die Suchergebnisse exportieren. Sie können Falldaten auch für die weitere Analyse in Advanced eDiscovery vorbereiten.
ms.openlocfilehash: 3c3d3fb6d4e2244554059e731b4585dd546ff52b
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000728"
---
# <a name="ediscovery-cases-in-the-security--compliance-center"></a>eDiscovery-Fälle im Security & Compliance Center

Sie können eDiscovery-Fälle im Compliance Center in Office 365 und Microsoft 365 verwenden, um zu steuern, wer eDiscovery-Fälle in Ihrer Organisation erstellen, darauf zugreifen und verwalten kann. Wenn Ihre Organisation über ein Office 365 E5-Abonnement verfügt, können Sie auch mithilfe von eDiscovery-Fällen Suchergebnisse mithilfe von Office 365 Advanced eDiscovery analysieren.
  
Ein eDiscovery-Fall ermöglicht Ihnen das Hinzufügen von Mitgliedern zu einem Fall, die Steuerung der Aktionen, die von bestimmten Fall Mitgliedern ausgeführt werden können, die Aufbewahrung der für einen Rechtsstreit relevanten inhaltsspeicherorte und das Zuordnen mehrerer Inhalts suchVorgänge zu einem einzelnen Fall. Sie können auch die Ergebnisse der Inhaltssuche exportieren, die mit einem Fall verknüpft ist, oder die Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten. eDiscovery-Fälle sind eine gute Möglichkeit, um zu beschränken, wer Zugriff auf Inhaltssuchen und Suchergebnisse für einen bestimmten Rechtsfall in Ihrer Organisation hat.
  
Verwenden Sie den folgenden Workflow, um eDiscovery-Fälle im Security & Compliance Center und Advanced eDiscovery einzurichten und zu verwenden.

[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Schritt 2: Erstellen eines neuen Falls](#step-2-create-a-new-case)

[Schritt 3: Hinzufügen von Mitgliedern zu einem Fall](#step-3-add-members-to-a-case)

[Schritt 4: Speichern der inhaltsspeicherorte](#step-4-place-content-locations-on-hold)

[Schritt 5: Erstellen und Ausführen einer Inhaltssuche, die mit einem Fall verknüpft ist](#step-5-create-and-run-a-content-search-associated-with-a-case)

[Schritt 6: Exportieren der Ergebnisse einer Inhaltssuche, die mit einem Fall verknüpft ist](#step-6-export-the-results-of-a-content-search-associated-with-a-case)

[Schritt 7: Vorbereiten der Suchergebnisse für erweiterte eDiscovery](#step-7-prepare-search-results-for-advanced-ediscovery)

[Schritt 8: Wechseln Sie zu dem Fall in Advanced eDiscovery](#step-8-go-to-the-case-in-advanced-ediscovery)

[Optional Schritt 9: Abschließen einer Groß-/Kleinschreibung](#optional-step-9-close-a-case)

[Optional Schritt 10: Erneutes Öffnen eines Closed Case](#optional-step-10-re-open-a-closed-case)

[Weitere Informationen](#more-information)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern

Der erste Schritt besteht darin, den Benutzern die entsprechenden eDiscovery-bezogenen Berechtigungen zuzuweisen, damit Sie Sie zu einem eDiscovery-Fall in Schritt 2 hinzufügen können. Sie müssen Mitglied der Rollengruppe "Organisationsverwaltung" sein (oder der Rolle "Rollenverwaltung" zugewiesen sein) im Security & Compliance Center, um eDiscovery-Berechtigungen zuzuweisen. In der folgenden Liste werden die eDiscovery-bezogenen Rollengruppen im Security & Compliance Center beschrieben. 
  
- **Prüfer** – diese Rollengruppe verfügt über die restriktivsten eDiscovery-bezogenen Berechtigungen. Der primäre Zweck dieser Rollengruppe besteht darin, Mitgliedern das Anzeigen und Zugreifen auf Falldaten in Office 365 Advanced eDiscovery zu ermöglichen. Mitglieder dieser Gruppe können nur die Liste der Fälle auf der **eDiscovery** -Seite im Security _AMP_ Compliance Center sehen und öffnen, von denen Sie Mitglieder sind. Nachdem der Benutzer auf einen Fall im Security and Compliance Center zugegriffen hat, können Sie auf **zu Advanced eDiscovery wechseln** , um auf die Falldaten in Advanced eDiscovery zuzugreifen und Sie zu analysieren. Sie können keine Fälle erstellen, Mitglieder zu einem Fall hinzufügen, haltebereiche erstellen, suchen erstellen, Suchergebnisse anzeigen, Suchergebnisse exportieren oder Ergebnisse für erweiterte eDiscovery vorbereiten. 
    
- **eDiscovery-Manager** : Mitglieder dieser Rollengruppe können eDiscovery-Fälle erstellen und verwalten. Sie können Mitglieder hinzufügen und entfernen, inhaltsspeicherorte halten, Inhalts suchen erstellen und bearbeiten, die mit einem Fall verknüpft sind, die Ergebnisse einer Inhaltssuche exportieren und Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten. Diese Rollengruppe enthält zwei Untergruppen. Die Differenz zwischen diesen Untergruppen basiert auf dem Bereich.
    
  - **eDiscovery Manager** – kann die eDiscovery-Fälle anzeigen und verwalten, die Sie erstellen oder Mitglied sind. Wenn ein anderer eDiscovery-Manager einen Fall erstellt, aber keinen zweiten eDiscovery-Manager als Mitglied dieses Falls hinzufügt, kann der zweite eDiscovery-Manager den Fall auf der **eDiscovery** -Seite im Security _AMP_ Compliance Center nicht anzeigen oder öffnen. eDiscovery-Manager können auch auf ihre Fälle in Advanced eDiscovery zugreifen, um Analyseaufgaben auszuführen. 
    
  - **eDiscovery-Administrator** – kann alle Fall Verwaltungsaufgaben durchführen, die ein eDiscovery-Manager ausführen kann. Darüber hinaus können eDiscovery-Administratoren folgende Aktionen durchführen:
    
    - Anzeigen aller Fälle, die auf der Seite **eDiscovery-Fälle** aufgeführt sind. 
    
    - Verwalten Sie alle Fälle in der Organisation, nachdem Sie sich selbst als Mitglied der Anfrage hinzugefügt haben.
    
    - Zugriffs Fall Daten in Advanced eDiscovery für jeden Fall in der Organisation.
    
    Überlegungen dazu, warum Sie ggf. einen eDiscovery-Administrator in Ihrer Organisation benötigen, finden Sie im Abschnitt [More information](#more-information). 
    
> [!IMPORTANT]
> Wenn eine Person nicht Mitglied einer dieser eDiscovery-bezogenen Rollengruppen ist oder nicht Mitglied einer Rollengruppe ist, der die Prüferrolle zugewiesen wurde, können Sie Sie nicht als Mitglied eines eDiscovery-Falls hinzufügen. 

Weitere Informationen zu eDiscovery-Berechtigungen finden Sie unter [assign eDiscovery Permissions](assign-ediscovery-permissions.md).
  
 **So weisen Sie eDiscovery-Berechtigungen zu**
  
1. Wechseln Sie zu [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Security & Compliance Center auf **Berechtigungen**, und führen Sie dann eine der folgenden Aktionen basierend auf den eDiscovery-Berechtigungen aus, die Sie zuweisen möchten.
    
    - Wenn Sie Berechtigungen für Prüfer zuweisen möchten, wählen Sie die Rollengruppe **Prüfer** aus, und klicken Sie dann neben **Mitglieder**auf **Bearbeiten**. Klicken Sie auf **Mitglieder auswählen**, klicken Sie ![auf **Bearbeiten**, klicken Sie auf Symbol](media/ITPro-EAC-AddIcon.gif) **** hinzufügen, wählen Sie den Benutzer aus, der der Rollengruppe Prüfer hinzugefügt werden soll, und klicken Sie dann auf **hinzu**fügen.
    
    - Um eDiscovery-Manager-Berechtigungen zuzuweisen, wählen Sie die Rollengruppe " **eDiscovery-Manager** " aus, und klicken Sie dann neben **eDiscovery-Manager**auf **Bearbeiten**. Klicken Sie auf **eDiscovery-Manager auswählen**, klicken ![Sie auf](media/ITPro-EAC-AddIcon.gif) **Bearbeiten**, klicken Sie auf Symbol hinzufügen * * Add * *, wählen Sie den Benutzer aus, den Sie als eDiscovery-Manager hinzufügen möchten, und klicken Sie dann auf **Hinzufügen**.
    
    - Um eDiscovery-Administratorberechtigungen zuzuweisen, wählen Sie die Rollengruppe " **eDiscovery-Manager** " aus, und klicken Sie dann neben **eDiscovery-Administrator**auf **Bearbeiten**. Klicken Sie auf **eDiscovery-Administrator auswählen**, klicken ![Sie auf](media/ITPro-EAC-AddIcon.gif) **** **Bearbeiten**, klicken Sie auf Symbol hinzufügen, wählen Sie den Benutzer aus, den Sie als eDiscovery-Administrator hinzufügen möchten, und klicken Sie dann auf **hinzu**fügen.
    
4. Nachdem Sie alle Benutzer hinzugefügt haben, klicken Sie auf **Fertig**, klicken Sie auf **Speichern** , um die Änderungen an der Rollengruppe zu speichern, und klicken Sie dann auf **Schließen**.

## <a name="step-2-create-a-new-case"></a>Schritt 2: Erstellen eines neuen Falls

Im nächsten Schritt erstellen Sie einen neuen eDiscovery-Fall. Sie müssen Mitglied der Rollengruppe „eDiscovery-Manager“ sein, um eDiscovery-Fälle zu erstellen. Wie bereits erläutert, können Sie, nachdem Sie im Security & Compliance Center einen neuen Fall erstellt haben, auf diesen Fall in Advanced eDiscovery zugreifen, wenn Sie ein Office 365 E5-Abonnement haben.
  
1. Wechseln Sie zu [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery**, und klicken Sie ![dann auf](media/ITPro-EAC-AddIcon.gif) Symbol hinzufügen, **um eine Groß-/Kleinschreibung zu erstellen**.
    
4. Geben Sie auf der Seite **neuer Fall** den Fall einen Namen ein, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **Speichern**. Beachten Sie, dass der Fallname in Ihrer Organisation eindeutig sein muss.
    
    ![Erstellen eines neuen Falls](media/7f78f83b-1525-4c77-9888-4b6bda1e148d.png)
  
    Der neue Fall wird in der Liste der Fälle auf der **eDiscovery** -Seite angezeigt. Beachten Sie, dass Sie den Mauszeiger über einen Fallnamen bewegen können, um Informationen über den Fall anzuzeigen, einschließlich des Status der Groß-/Kleinschreibung ( **aktiv** oder **geschlossen**), der Beschreibung des Falls (die im vorherigen Schritt erstellt wurde) und wann die Anfrage zuletzt geändert wurde. Wer hat es geändert.
    
    > [!TIP]
    > Nachdem Sie einen neuen Fall erstellt haben, können Sie ihn jederzeit umbenennen. Klicken Sie auf der **eDiscovery** -Seite einfach auf den Namen der Anfrage. Ändern Sie auf der Seite **dieses Fall Flyout verwalten** den Namen, der im Feld unter **Name**angezeigt wird, und speichern Sie die Änderung. 
  
## <a name="step-3-add-members-to-a-case"></a>Schritt 3: Hinzufügen von Mitgliedern zu einem Fall

Nachdem Sie einen neuen Fall erstellt haben, besteht der nächste Schritt darin, dem Fall Mitglieder hinzuzufügen. Wie bereits zuvor erläutert, können nur Benutzer, die Mitglied der Rollengruppen Prüfer oder eDiscovery-Manager sind, als Mitglieder des Falls hinzugefügt werden. Beachten Sie, dass der eDiscovery-Manager, der den Fall erstellt hat, automatisch als Mitglied hinzugefügt wird.
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der Groß-/Kleinschreibung, der Sie Mitglieder hinzufügen möchten.
    
    Die Seite **dieses Fall Flyout verwalten** wird angezeigt. 
    
    ![Verwalten einer Fall Flyout-Seite](media/11f35ceb-6c98-4580-a3bc-ad688e9c7af9.png)
  
3. Klicken Sie ![unter **Mitglieder verwalten**auf Symbol](media/ITPro-EAC-AddIcon.gif) **** hinzufügen, um der Anfrage Mitglieder hinzuzufügen. 
    
    Sie können der Groß-/Kleinschreibung auch eine Rollengruppe hinzufügen. Klicken Sie unter **Rollengruppen verwalten**auf ![Symbol](media/ITPro-EAC-AddIcon.gif) **hinzu**fügen.
    
    > [!NOTE]
    > Rollengruppen steuern, wer einem eDiscovery-Fall Mitglieder zuweisen kann. Das kann bedeuten, dass Sie den Rollengruppen, denen Sie angehören, eine Groß-/Kleinschreibung zuweisen.
    
4. Klicken Sie in der Liste der Personen oder Rollengruppen, die als Mitglieder des Falls hinzugefügt werden können, auf das Kontrollkästchen neben den Namen der Personen oder Rollengruppen, die Sie hinzufügen möchten.
    
    > [!TIP]
    > Wenn Sie eine umfangreiche Liste von Personen haben, die als Mitglieder hinzugefügt werden können, verwenden Sie das **Suchfeld** , um nach einer bestimmten Person in der Liste zu suchen. 
  
5. Nachdem Sie die Personen oder Rollengruppen ausgewählt haben, die als Mitglieder der Gruppe hinzugefügt werden sollen, klicken Sie auf **Hinzufügen**.
    
    Klicken Sie in **diesem Fall verwalten**auf **Speichern** , um die neue Liste der Fall Mitglieder zu speichern. 
    
6. Klicken Sie auf **Speichern** , um die neue Liste der Fall Mitglieder zu speichern. 
  
## <a name="step-4-place-content-locations-on-hold"></a>Schritt 4: Speichern der inhaltsspeicherorte

Sie können einen eDiscovery-Fall zum Erstellen von Haltebereichen verwenden, um Inhalte beizubehalten, die möglicherweise für den Fall relevant sind. Sie können die Postfächer und OneDrive für Business-Websites von Personen, die in diesem Fall Verwalter sind, einhalten. Sie können auch das Gruppenpostfach, die SharePoint-Website und die OneDrive for Business-Website für eine Office 365-Gruppe einhalten. Entsprechend können Sie auch das Postfach und die Website, die Microsoft Teams zugeordnet sind, einhalten. Wenn Sie inhaltsspeicherorte in der Warteschleife platzieren, werden Inhalte aufbewahrt, bis Sie den Haltebereich vom Inhaltsspeicherort entfernen oder den Haltebereich löschen.

> [!NOTE]
> Nachdem Sie einen Inhaltsspeicher Platz gedrückt haben, dauert es bis zu 24 Stunden, bis die Sperre wirksam wird. 
>   
Wenn Sie einen Haltestatus erstellen, haben Sie die folgenden Optionen, um den Inhalt an den angegebenen Inhaltsspeicherorten zu bereichern:
  
- Sie erstellen eine unendliche Halteposition, an der der gesamte Inhalt gehalten wird. Alternativ können Sie eine abfragebasierte Aufbewahrung erstellen, in der nur Inhalte gespeichert werden, die mit einer Suchabfrage übereinstimmen.
    
- Sie können einen Datumsbereich angeben, der nur den Inhalt enthalten soll, der innerhalb dieses Datumsbereichs gesendet, empfangen oder erstellt wurde. Alternativ können Sie alle Inhalte unabhängig davon speichern, wann Sie gesendet, empfangen oder erstellt wurden.
    
> [!NOTE]
> Sie können maximal 10.000-Speicherrichtlinien für alle eDiscovery-Fälle in Ihrer Organisation einhalten. 
  
So erstellen Sie einen Aufbewahrungs Status für einen eDiscovery-Fall:
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, in dem Sie den Haltestatus erstellen möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf die Registerkarte **halten** . 
    
    ![Klicken Sie auf die Registerkarte halten](media/3fef2db4-36de-4517-a34d-82f47b82d9bf.png)
  
4. Klicken Sie **** ![auf der Seite halten auf Symbol](media/ITPro-EAC-AddIcon.gif) **Erstellen**hinzufügen.
    
5. Geben Sie auf der Seite " **halten Sie den Namen** " einen Namen ein. Der Name des haltebereichs muss in Ihrer Organisation eindeutig sein. 
    
    ![Geben Sie einen eindeutigen Namen für ihre Aufbewahrung ein.](media/7e15ea63-abd1-4f14-a29c-7ecfb9571d2c.png)
  
6. Optional Fügen Sie im Feld **Beschreibung** eine Beschreibung des haltebereichs hinzu. 
    
7. Klicken Sie auf **Weiter**.
    
8. Wählen Sie die inhaltsspeicherorte aus, die Sie für den Aufbewahrungsort aktivieren möchten. Sie können Postfächer, Websites und öffentliche Ordner in der Warteschleife platzieren.
    
    ![Wählen Sie Inhaltsspeicherorte aus, die im Haltebereich platziert werden sollen.](media/a59e4265-9151-4dbf-913f-6a4ab8db06b4.png)
  
   a. **Exchange-e-Mail** -klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** . Angeben von Postfächern für die Aufbewahrung. Verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen (um die Postfächer der Gruppenmitglieder einzuhalten). Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder ein Microsoft-Team einhalten. Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.
    
    > [!NOTE]
    > Wenn Sie auf **Benutzer, Gruppen oder Teams auswählen** klicken, um die Postfächer anzugeben, die in der Warteschleife platziert werden sollen, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein. 
  
   b. **SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um SharePoint-und OneDrive für Business-Websites für die Aufbewahrung anzugeben. Geben Sie die URL für jede Website ein, die Sie in der Warteschleife platzieren möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen. Klicken Sie auf **auswählen**und dann auf **Fertig**.
    
    Im Abschnitt [Weitere Informationen](#more-information) finden Sie Tipps für die Aufbewahrung von Office 365-Gruppen und Microsoft Teams. 
    
    > [!NOTE]
    > In dem seltenen Fall, dass der Benutzerprinzipalname (UPN) einer Person geändert wird, wird auch die URL für Ihr OneDrive-Konto geändert, um den neuen UPN zu integrieren. In diesem Fall müssen Sie den Haltestatus ändern, indem Sie die neue OneDrive-URL des Benutzers hinzufügen und den alten entfernen. 
  
   c. **Öffentliche Exchange-Ordner** – verschieben Sie das ![Umschaltflächen](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) -Steuerelement Umschaltfläche in die **alle** -Position, um alle öffentlichen Ordner in Ihrer Exchange Online-Organisation aufzubewahren. Beachten Sie, dass Sie bestimmte öffentliche Ordner nicht für die Aufbewahrung auswählen können. Lassen Sie den UMSCHALT Schalter auf **None** festgelegt, wenn Sie keine öffentlichen Ordner einhalten möchten.
    
9. Wenn Sie mit dem Hinzufügen von Inhaltsspeicherorten zum Haltebereich fertig sind, klicken Sie auf **weiter**.
    
10. Führen Sie die folgenden Schritte aus, um eine abfragebasierte Aufbewahrung mit Bedingungen zu erstellen. Klicken Sie andernfalls einfach auf **weiter** .
    
    ![Erstellen einer abfragebasierten Aufbewahrung mit Bedingungen](media/d587b58e-d05c-4ac0-b0fe-09019e4f1063.png)
  
    
       a. Geben Sie im Feld unter **Schlüsselwörter**eine Suchabfrage in das Feld ein, sodass nur der Inhalt, der den Suchkriterien entspricht, in der Warteschleife gespeichert wird. Sie können Schlüsselwörter, Nachrichteneigenschaften oder Dokumenteigenschaften wie Dateinamen angeben. Sie können auch komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**oder **Not**. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in der Warteschleife platziert.
    
    b. Klicken ![Sie auf](media/ITPro-EAC-AddIcon.gif) **** Symbol hinzufügen, um eine oder mehrere Bedingungen hinzuzufügen, um die Suchabfrage für den Haltebereich einzuschränken. Jede Bedingung fügt der KQL-Suchabfrage, die beim Erstellen des haltebereichs erstellt und ausgeführt wird, eine Klausel hinzu. Sie können beispielsweise einen Datumsbereich angeben, sodass e-Mails oder Website Dokumente, die innerhalb des Datumsbereichs erstellt wurden, gehalten werden. Eine Bedingung ist durch **AND**-Operator logisch mit der (im Schlüsselwortfeld angegebenen) Schlüsselwortabfrage verbunden. Das hat zur Folge, dass Elemente sowohl die Stichwortabfrage als auch die Bedingung erfüllen müssen, die in den Haltestatus versetzt werden soll.

    Weitere Informationen zum Erstellen einer Suchabfrage und zum Verwenden von Bedingungen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).
    
11. Klicken Sie nach dem Konfigurieren einer abfragebasierten Aufbewahrung auf **weiter**.
    
12. Überdenken Sie Ihre Einstellungen, und klicken Sie dann auf **diesen halteBereich erstellen**.
    
### <a name="hold-statistics"></a>Aufbewahrungs Statistiken

Nach einer Weile werden Informationen über den neuen Haltestatus im Detailbereich auf der halte **Status** Seite für den ausgewählten Speicher angezeigt. Zu diesen Informationen gehören die Anzahl der Postfächer und Websites, die in der Warteschleife gespeichert wurden, sowie Statistiken zu den Inhalten, die in den Warteschlangen gehalten wurden, wie die Gesamtanzahl und die Größe der in der Warteschleife befindlichen Elemente und der Zeitpunkt der letzten Berechnung der Aufbewahrungs Statistiken. Anhand dieser Statistiken können Sie ermitteln, wie viele Inhalte im Zusammenhang mit dem eDiscovery-Fall stehen. 
  
![Aufbewahrungs Statistiken](media/575cfe0a-9210-4ae4-8df8-65665d66712e.png)
  
Beachten Sie die folgenden Aspekte im Hinblick auf Hold Statistics:
  
- Die Gesamtanzahl der in der Warteschleife enthaltenen Elemente gibt die Anzahl der Elemente aus allen Inhaltsquellen an, die in der Warteschleife gespeichert werden. Wenn Sie eine abfragebasierte Aufbewahrung erstellt haben, gibt diese Statistik die Anzahl der Elemente an, die der Abfrage entsprechen.
    
- Die Anzahl der in der Warteschleife enthaltenen Elemente enthält auch nicht indizierte Elemente, die sich in den Inhaltsspeicherorten befinden. Beachten Sie, dass beim Erstellen einer abfragebasierten Aufbewahrung alle nicht indizierten Elemente in den Inhaltsspeicherorten gehalten werden. Dies umfasst nicht indizierte Elemente, die nicht mit den Suchkriterien einer abfragebasierten Aufbewahrung übereinstimmen, und nicht indizierte Elemente, die möglicherweise außerhalb einer Datumsbereichs Bedingung liegen. Dies unterscheidet sich von dem, was passiert, wenn Sie eine Inhaltssuche ausführen, in der nicht indizierte Elemente, die nicht mit der Suchabfrage übereinstimmen oder von einer Bedingung für den Datumswert ausgeschlossen werden, nicht in den Suchergebnissen enthalten sind. Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md).
    
- Sie können die neueste Hold-Statistik abrufen, indem Sie auf **Statistik aktualisieren** klicken, um eine Such Schätzung erneut auszuführen, die die aktuelle Anzahl der zu speichernden Elemente berechnet. Klicken Sie ****![gegebenenfalls auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren in der Symbolleiste, um die Aufbewahrungs Statistiken im Detailbereich zu aktualisieren. 
    
- Es ist normal, dass die Anzahl der zu haltenden Elemente im Laufe der Zeit ansteigt, da Benutzer, deren Postfach oder Website in Betrieb ist, normalerweise neue e-Mail-Nachrichten senden oder empfangen und neue SharePoint-und OneDrive für Geschäftsdokumente erstellen.
    
> [!NOTE]
> Wenn ein SharePoint-oder OneDrive-Konto in eine andere Region in einer Multi-Geo-Umgebung verschoben wird, werden die Statistiken für diese Website nicht in die Aufbewahrungs Statistik aufgenommen. Die Inhalte auf der Website bleiben jedoch weiterhin in der Warteschleife. Wenn eine Website in einen anderen Bereich verschoben wird, wird auch die URL, die in der Warteschleife angezeigt wird, nicht aktualisiert. Sie müssen den Haltebereich bearbeiten und die URL aktualisieren. 
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>Schritt 5: Erstellen und Ausführen einer Inhaltssuche, die mit einem Fall verknüpft ist

Nachdem ein eDiscovery-Fall erstellt wurde und alle Depotstellen im Zusammenhang mit dem Fall gespeichert werden, können Sie eine oder mehrere Inhalts suchVorgänge erstellen und ausführen, die dem Fall zugeordnet sind. Inhalts suchVorgänge, die mit einem Fall verknüpft sind, werden nicht auf der Seite **Suchen** im Security _AMP_ Compliance Center aufgeführt. Dies führt dazu, dass der Zugriff auf Inhalts suchen, die einem Fall zugeordnet sind, nur von Fall Mitgliedern erfolgen kann, die auch Mitglieder der eDiscovery-Manager-Rollengruppe sind. 
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, in dem Sie eine Inhaltssuche erstellen möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf die Registerkarte **Suchen** . 
    
    ![Suchregisterkarte](media/2e15fe32-1a2e-4588-ad0b-5d96f77cece9.png)
  
4. Klicken Sie **** ![auf der Seite suchen auf Symbol](media/ITPro-EAC-AddIcon.gif) für **neue Suche**hinzufügen. 
    
5. Auf der Seite **Neue Suche** können Sie Schlüsselwörter und Bedingungen zum Erstellen der Suchabfrage hinzufügen. 
    
    ![Neue Suche](media/0e9954e7-c0ea-4e05-820b-e4b81dc5f81d.png)
  
6. Sie können Schlüsselwörter, Nachrichteneigenschaften wie gesendete und empfangene Datumsangaben oder Dokumenteigenschaften angeben, beispielsweise Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**, **near**oder **ONEAR**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen. 
    
7. Sie können auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch den **or** -Operator in der erstellten Suchabfrage verbunden. 
    
    ![Stichwortliste](media/29cceb5d-2817-4fc4-b91a-ced1c5824a17.png)
  
    Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [View Keyword Statistics for Content Search results](view-keyword-statistics-for-content-search.md).
    
    Weitere Informationen zur Verwendung der Stichwörter Liste finden Sie unter [Erstellen einer Suchabfrage](content-search.md#building-a-search-query).
    
8. Fügen Sie unter **Bedingungen**einer Suchabfrage Bedingungen hinzu, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt eine Klausel zu der KQL-Suchabfrage hinzu, die beim Starten der Suche erstellt und ausgeführt wird. Eine Bedingung ist durch **AND**-Operator logisch mit der (im Schlüsselwortfeld angegebenen) Schlüsselwortabfrage verbunden. Dies bedeutet, dass Elemente sowohl die Schlüsselwortabfrage als auch die Bedingung erfüllen muss, damit sie in die Suchergebnisse aufgenommen werden. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. 
    
    Weitere Informationen zum Erstellen einer Suchabfrage sowie zur Verwendung von Bedingungen finden Sie unter [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
9. Wählen Sie unter **Speicherorte: Aufbewahrungsort**die inhaltsspeicherorte aus, die Sie durchsuchen möchten. Sie können Postfächer, Websites und öffentliche Ordner in derselben Suche durchsuchen.
    
    ![Speicherorte, Speicherorte](media/d56398aa-0b20-4500-8e26-494eab92a99f.png)
  
    - **Alle Standorte** – wählen Sie diese Option aus, um alle inhaltsspeicherorte in Ihrer Organisation zu durchsuchen. Wenn Sie diese Option auswählen, können Sie alle Exchange-Postfächer durchsuchen (einschließlich der Postfächer für alle Office 365-Gruppen und Microsoft Teams), alle SharePoint-und OneDrive für Business-Websites (einschließlich der Websites für alle Office 365-Gruppen und Microsoft Teams) und alle öffentlichen Ordner.
    
    - **Alle Speicherorte** – wählen Sie diese Option aus, um alle inhaltsspeicherorte zu durchsuchen, die in der Groß-/Kleinschreibung gehalten wurden. Wenn die Groß-/Kleinschreibung mehrere haltebereiche enthält, werden die inhaltsspeicherorte aus allen speichern durchsucht, wenn Sie diese Option auswählen. Wenn ein Inhaltsspeicherort auf eine abfragebasierte Aufbewahrungsstelle gesetzt wurde, werden außerdem nur die Warteschlangenelemente durchsucht, wenn Sie die Inhaltssuche ausführen, die Sie in diesem Schritt erstellen. Wenn beispielsweise ein Benutzer in einer abfragebasierten Groß-/Kleinschreibung gehalten wurde, die Elemente beibehält, die vor einem bestimmten Datum gesendet oder erstellt wurden, würden nur diese Elemente mithilfe der Suchkriterien der Inhaltssuche durchsucht. Dies wird erreicht, indem die Case-Hold-Abfrage und die Inhalts Suchabfrage durch einen **and-** Operator verbunden werden. Im Abschnitt [Weitere Informationen](#more-information) am Ende dieses Artikels finden Sie weitere Informationen zum Suchen von Fall Inhalten. 
    
    - **Bestimmte Speicherorte** – wählen Sie diese Option aus, um die Postfächer und Websites auszuwählen, die Sie durchsuchen möchten. Wenn Sie diese Option auswählen und auf **ändern**klicken, wird eine Liste mit Speicherorten angezeigt. Sie können auswählen, ob Sie alle Benutzer, Gruppen, Teams oder Website Standorte durchsuchen möchten.
    
      ![Auswählen bestimmter Standorte](media/97469b15-7be1-4aee-be27-f8343636152c.png)
  
      Sie können auch alle öffentlichen Ordner in Ihrer Organisation durchsuchen, aber wenn Sie diese Option auswählen und einen beliebigen Inhaltsspeicherort in der Warteschleife durchsuchen, wird keine Abfrage aus einem abfragebasierten Groß-/Kleinschreibung auf die Suchabfrage angewendet. Mit anderen Worten: alle Inhalte an einem Speicherort werden durchsucht, nicht nur der Inhalt, der von einem abfragebasierten Gehäuse aufbewahrt wird.
    
      Sie können die vordefinierten Fall inhaltsspeicherorte entfernen oder neue hinzufügen. Wenn Sie diese Option auswählen, haben Sie auch die Flexibilität, alle inhaltsspeicherorte für einen bestimmten Dienst (beispielsweisedurch Suchen aller Exchange-Postfächer) zu durchsuchen, oder Sie können bestimmte inhaltsspeicherorte für einen Dienst durchsuchen. Sie können auch auswählen, ob die öffentlichen Ordner in Ihrer Organisation durchsucht werden sollen.
    
      Beachten Sie diese Aspekte beim Hinzufügen von Inhaltsspeicherorten für die Suche:
    
      - Wenn Sie auf **Benutzer, Gruppen oder Teams auswählen** klicken, um die zu durchsuchenden Postfächer anzugeben, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Um dieser Liste Empfänger hinzuzufügen, klicken Sie auf **Benutzer, Gruppen oder Teams auswählen**, geben Sie im Suchfeld einen Namen (mindestens 3 Zeichen) ein, aktivieren Sie das Kontrollkästchen neben dem Namen, und klicken Sie dann auf **auswählen**. 
    
      - Sie können inaktive Postfächer, Office 365-Gruppen, Microsoft Teams und Verteilergruppen zur Liste der zu durchsuchenden Postfächer hinzufügen. Dynamische Verteilergruppen werden nicht unterstützt. Wenn Sie Office 365-Gruppen oder Microsoft Teams hinzufügen, wird das Gruppen-oder Team Postfach durchsucht; die Postfächer der Gruppenmitglieder wurden nicht durchsucht.
    
      - Klicken Sie zum Hinzufügen von Websites auf **Websites auswählen**, klicken Sie erneut auf **Websites auswählen** , und geben Sie die URL für jede Website ein, die Sie durchsuchen möchten. Sie können auch die URL für die SharePoint-Website für Office 365-Gruppen und Microsoft Teams hinzufügen. 
    
10. Nachdem Sie die zu durchsuchenden inhaltsspeicherorte ausgewählt haben, klicken Sie auf **Fertig** und dann auf **Speichern**.
    
11. Klicken Sie auf der Seite **neue Suche** auf **Speichern** , und geben Sie einen Namen für die Suche ein. Inhalts suchVorgänge, die mit einem Fall verknüpft sind, müssen Namen haben, die innerhalb Ihrer Office 365-Organisation eindeutig sind. 
    
12. Klicken Sie auf **Run speichern &amp; ** , um die Sucheinstellungen zu speichern. 
    
13. Geben Sie einen eindeutigen Namen für die Suche ein, und klicken Sie auf **Speichern** , um die Suche zu starten. 
    
    Die Suche beginnt. Nach einer Weile wird eine Schätzung der Suchergebnisse im Detailbereich angezeigt. Die Schätzung umfasst die Gesamtgröße und die Anzahl der Elemente, die den Suchkriterien entsprechen. Die Such Schätzung enthält auch die Anzahl der nicht indizierten Elemente in den Inhaltsspeicherorten, die durchsucht wurden. Die Anzahl nicht indizierter Elemente, die den Suchkriterien nicht entsprechen, werden in die Suchstatistiken einbezogen, die im Detailbereich angezeigt werden. Wenn ein nicht indiziertes Element mit der Suchabfrage übereinstimmt (da andere Nachrichten-oder Dokumenteigenschaften den Suchkriterien entsprechen), wird es nicht in der geschätzten Anzahl von nicht indizierten Elementen eingeschlossen. Wenn ein nicht indiziertes Element von den Suchkriterien ausgeschlossen wird, wird es auch nicht in die Schätzung der nicht indizierten Elemente eingeschlossen.
    
  Wenn die Suche abgeschlossen ist, können Sie eine Vorschau der Suchergebnisse anzeigen. Klicken Sie ****![gegebenenfalls auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren, um die Informationen im Detailbereich zu aktualisieren. 
    
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>Schritt 6: Exportieren der Ergebnisse einer Inhaltssuche, die mit einem Fall verknüpft ist

Nachdem eine Suche erfolgreich ausgeführt wurde, können Sie die Suchergebnisse exportieren. Wenn Sie Suchergebnisse exportieren, werden Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen. Wenn Sie Inhalte aus SharePoint-und OneDrive für Business-Websites exportieren, werden Kopien von systemeigenen Office-Dokumenten und anderen Dokumenten exportiert. Eine Manifestdatei (im XML-Format), die Informationen zu jedem Suchergebnis enthält, wird ebenfalls exportiert.
  
Sie können die Ergebnisse einer einzelnen Suche exportieren, die [mit einem Fall verknüpft](#export-the-results-of-a-single-search-associated-with-a-case) ist, oder Sie können die Ergebnisse [mehrerer Suchvorgänge exportieren, die mit einem Fall verknüpft sind](#export-the-results-of-multiple-searches-associated-with-a-case).
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>Exportieren der Ergebnisse einer einzelnen Suche, die mit einem Fall verknüpft ist

1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, aus dem Sie die Suche exportieren möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf **Suchen**.
    
4. Klicken Sie in der Liste der Suchvorgänge auf die Suche, aus der Sie Suchergebnisse exportieren möchten, klicken Sie ![auf Suchergebnis Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mehr**exportieren, und wählen Sie dann **Ergebnisse** aus der Dropdownliste aus. 
    
    Die Seite **Ergebnisse exportieren** wird angezeigt. 
    
    ![Ergebnisseite exportieren](media/ab0bb46d-310b-4374-8644-717146df6676.png)
  
    Der Workflow zum Exportieren der Ergebnisse aus einer Inhaltssuche, die mit einem Fall verknüpft ist, entspricht dem Exportieren der Suchergebnisse für eine Suche auf der Seite **Inhaltssuche** . Schrittweise Anleitungen finden Sie unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md).
    
    > [!NOTE]
    > Wenn Sie Suchergebnisse exportieren, haben Sie die Möglichkeit, die Deduplizierung zu aktivieren, sodass nur eine Kopie einer e-Mail-Nachricht exportiert wird, obwohl in den durchsuchten Postfächern möglicherweise mehrere Instanzen derselben Nachricht gefunden wurden. Weitere Informationen zur Deduplizierung und zur Identifizierung doppelter Elemente finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md). 
  
5. Klicken Sie auf die Registerkarte **Export** , um die Liste der Exportaufträge anzuzeigen, die für diesen Fall vorhanden sind. 
    
    ![Registerkarte "Exportieren"](media/1b84c45e-4ec9-4ecd-9e07-eaf8fc4cc307.png)
  
    Möglicherweise müssen Sie ****![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Liste der Exportaufträge so zu aktualisieren, dass der soeben erstellte Exportauftrag angezeigt wird. Beachten Sie, dass Exportaufträge den gleichen Namen wie die entsprechende Inhaltssuche aufweisen, wobei **_Export** an das Ende des Such namens angefügt wird. 
    
6. Klicken Sie auf den soeben erstellten Exportauftrag, um Statusinformationen im Detailbereich anzuzeigen. Diese Informationen enthalten den Prozentsatz der Elemente, die in einen Azure-Speicherbereich in der Microsoft-Cloud übertragen wurden.
    
    Klicken Sie nach der Übertragung aller Elemente auf **Ergebnisse herunterladen** , um die Suchergebnisse auf Ihren lokalen Computer herunterzuladen. Weitere Informationen finden Sie unter Schritt 2 unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md) .
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>Exportieren der Ergebnisse mehrerer Suchvorgänge, die mit einem Fall verknüpft sind

Als Alternative zum Exportieren der Ergebnisse einer einzelnen Inhaltssuche, die mit einem Fall verknüpft ist, können Sie die Ergebnisse mehrerer Suchvorgänge aus demselben Fall in einen einzelnen Export exportieren. Das Exportieren der Ergebnisse mehrerer Suchvorgänge ist schneller und einfacher als das Exportieren der Suchergebnisse.
  
> [!NOTE]
> Sie können die Ergebnisse mehrerer Suchvorgänge nicht exportieren, wenn eine dieser Suchvorgänge so konfiguriert wurde, dass alle Case-Inhalte durchsucht werden. Exportieren Sie nur die Ergebnisse mehrerer Suchvorgänge für Suchvorgänge, die einem eDiscovery-Fall zugeordnet sind. Sie können die Ergebnisse mehrerer suchen, die auf der Seite für die **Inhaltssuche** im Security _AMP_ Compliance Center aufgeführt sind, nicht exportieren. 
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, aus dem Sie Suchergebnisse exportieren möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf **Suchen**.
    
4. Wählen Sie in der Liste der Suchvorgänge für den Fall mindestens zwei Suchvorgänge aus, für die Sie Suchergebnisse exportieren möchten.
    
    > [!NOTE]
    > Drücken Sie die STRG-Taste, um mehrere Suchvorgänge auszuwählen. Sie können auch mehrere benachbarte Suchvorgänge auswählen, indem Sie auf die erste Suche klicken, die UMSCHALTTASTE gedrückt halten und dann auf die letzte Suche klicken. 
  
5. Nachdem Sie die Suchvorgänge ausgewählt haben, wird die Seite **Massenaktionen** angezeigt. 
    
    ![Klicken Sie auf der Seite Massenaktionen auf Ergebnisse exportieren.](media/f34e3707-a9c1-494f-91a4-da1165aa730a.png)
  
    
6. Klicken ![Sie auf Export](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Ergebnisse**für Suchergebnisse-Symbol exportieren.

7. Geben Sie auf der Seite **Ergebnisse exportieren** einen eindeutigen Namen für den Export ein, wählen Sie Ausgabeoptionen aus, und wählen Sie aus, wie der Inhalt exportiert werden soll. Klicken Sie auf **Exportieren**.
    
    Der Workflow zum Exportieren der Ergebnisse aus mehreren Inhalts Suchvorgängen, die mit einem Fall verknüpft sind, entspricht dem Exportieren der Suchergebnisse für eine einzelne Suche. Schrittweise Anleitungen finden Sie unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md).
    
    > [!NOTE]
    > Wenn Sie Suchergebnisse aus mehreren Suchvorgängen exportieren, die mit einem Fall verknüpft sind, haben Sie auch die Möglichkeit, die Deduplizierung zu aktivieren, sodass nur eine Kopie einer e-Mail-Nachricht exportiert wird, obwohl mehrere Instanzen derselben Nachricht möglicherweise im Postfächer, die in einer oder mehreren Suchvorgängen durchsucht wurden. Weitere Informationen zur Deduplizierung und zur Identifizierung doppelter Elemente finden Sie unter [Deduplizierung in eDiscovery-Suchergebnissen](de-duplication-in-ediscovery-search-results.md). 
  
8. Nachdem Sie den Export gestartet haben, klicken Sie auf die Registerkarte **exportieren** , um die Liste der Exportaufträge für diesen Fall anzuzeigen. 
    
    ![Registerkarte "Exportieren", mehrfach Suche](media/b9505e1b-559f-4a8c-96b3-a3f734753926.png)
  
    Möglicherweise müssen Sie **** ![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Liste der Exportaufträge zu aktualisieren, um den soeben erstellten Exportauftrag anzuzeigen. Beachten Sie, dass die Suchvorgänge, die im Exportauftrag enthalten waren, in der Spalte **Suchen** aufgelistet werden. 
    
8. Klicken Sie auf den soeben erstellten Exportauftrag, um Statusinformationen im Detailbereich anzuzeigen. Diese Informationen enthalten den Prozentsatz der Elemente, die in einen Azure-Speicherbereich in der Microsoft-Cloud übertragen wurden.
    
9. Klicken Sie nach der Übertragung aller Elemente auf **Ergebnisse herunterladen** , um die Suchergebnisse auf Ihren lokalen Computer herunterzuladen. Weitere Informationen finden Sie unter Schritt 2 unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md).
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>Weitere Informationen zum Exportieren der Ergebnisse mehrerer Suchvorgänge

- Wenn Sie die Ergebnisse mehrerer Suchvorgänge exportieren, werden die Suchabfragen von allen Suchvorgängen mithilfe von **oder** -Operatoren kombiniert, und dann wird die kombinierte Suche gestartet. Die geschätzten Ergebnisse der kombinierten Suche werden im Detailbereich des ausgewählten Exportauftrags angezeigt. Die Suchergebnisse werden dann in den Azure-Speicherbereich in der Microsoft-Cloud übertragen. Der Status der Übertragung wird auch im Detailbereich angezeigt. Nachdem alle Suchergebnisse übertragen wurden, können Sie diese auf Ihren lokalen Computer herunterladen. 
    
- Die maximale Anzahl von Stichwörtern aus den Suchabfragen für alle Suchvorgänge, die Sie exportieren möchten, ist 500. (Dies ist derselbe Grenzwert für eine einzelne Inhaltssuche). Der Grund dafür ist, dass der Exportauftrag alle Suchabfragen mit dem **or** -Operator kombiniert. Wenn Sie diesen Grenzwert überschreiten, wird ein Fehler zurückgegeben. In diesem Fall müssen Sie die Ergebnisse aus weniger Suchvorgängen exportieren oder die Suchabfragen der Suchvorgänge vereinfachen, die Sie exportieren möchten. 
    
- Die exportierten Suchergebnisse werden nach der Inhaltsquelle organisiert, in der das Element gefunden wurde. Das führt dazu, dass eine Inhaltsquelle in den Export Ergebnissen Elemente enthalten kann, die von verschiedenen Suchvorgängen zurückgegeben werden. Wenn Sie beispielsweise die Option zum Exportieren von e-Mail-Nachrichten in einer PST-Datei für jedes Postfach ausgewählt haben, kann die PST-Datei Ergebnisse aus mehreren Suchvorgängen aufweisen.
    
- Wenn dasselbe e-Mail-Element oder Dokument aus demselben Inhaltsspeicherort von mehr als einer der Suchvorgänge zurückgegeben wird, die Sie exportieren, wird nur eine Kopie des Elements exportiert.
    
- Sie können einen Export nicht für mehrere Suchvorgänge nach dem erstellen bearbeiten. Sie können beispielsweise keine Suchvorgänge aus dem Export hinzufügen oder entfernen. Sie müssen einen neuen Exportauftrag erstellen, um zu ändern, welche Suchergebnisse exportiert werden. Nachdem ein Exportauftrag erstellt wurde, können Sie die Ergebnisse nur auf einen Computer herunterladen, den Export neu starten oder den Exportauftrag löschen.
    
- Wenn Sie den Export erneut starten, wirken sich Änderungen an den Abfragen der Suchvorgänge, aus denen der Exportauftrag besteht, nicht auf die Suchergebnisse aus, die abgerufen werden. Wenn Sie einen Export neu starten, wird derselbe kombinierte Suchabfrage Auftrag ausgeführt, der beim Erstellen des Exportauftrags ausgeführt wurde.
    
- Wenn Sie einen Export aus der Seite **Exporte** in einem eDiscovery-Fall neu starten, überschreiben die Suchergebnisse, die an den Azure-Speicherbereich übertragen werden, die vorherigen Ergebnisse. die zuvor übermittelten Ergebnisse stehen nicht zum Herunterladen zur Verfügung. 
    
- Das Vorbereiten der Ergebnisse mehrerer Suchvorgänge für die Analyse in Advanced eDiscovery ist nicht verfügbar. Sie können nur die Ergebnisse einer einzelnen Suche für die Analyse in Advanced eDiscovery vorbereiten.

## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>Schritt 7: Vorbereiten der Suchergebnisse für erweiterte eDiscovery

Wenn Ihre Organisation über ein Office 365 E5-Abonnement verfügt, können Sie die Ergebnisse der Inhaltssuche vorbereiten, die mit einem Fall zur Analyse in Advanced eDiscovery verknüpft sind. Nachdem Sie die Suchergebnisse vorbereitet haben, können Sie auf Advanced eDiscovery (siehe [Schritt 8: Wechseln Sie zum Fall in Advanced eDiscovery](#step-8-go-to-the-case-in-advanced-ediscovery)) wechseln und die Suchergebnis Daten zur weiteren Analyse in Advanced eDiscovery verarbeiten.
  
Wenn Sie Suchergebnisse für erweiterte eDiscovery vorbereiten, extrahiert die Optical Character Recognition (OCR)-Funktionalität automatisch Text aus Bildern. OCR wird für lose Dateien, e-Mail-Anlagen und eingebettete Bilder unterstützt. Auf diese Weise können Sie die Textanalyse Funktionen von Advanced eDiscovery (Near-Duplikate, e-Mail-Threading, Designs und Vorhersage Codierung) auf Text in Bilddateien anwenden.
  
> [!NOTE]
> Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden. Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden. Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz. 
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, dass Sie Suchergebnisse für die Analyse in Advanced eDiscovery vorbereiten möchten, auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf **Suchen**, und wählen Sie dann die Suche aus.
    
4. Klicken Sie im Detailbereich auf ![Suchergebnis Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **mehr**exportieren, und klicken Sie dann auf **für erweiterte eDiscovery vorbereiten**.
    
    ![Vorbereiten der Ergebnisse für Advanced eDiscovery](media/b6548ff0-a6e9-42b1-9ae4-5c15146f5690.png)
  
5. Wählen Sie auf der Seite **Prepare for Advanced eDiscovery** eine der folgenden Optionen aus: 
    
    - Alle Elemente, ausgenommen Personen mit unbekanntem Format, werden verschlüsselt oder aus anderen Gründen nicht indiziert.
    
    - Alle Elemente, einschließlich derer, die nicht erkannt wurden, werden verschlüsselt oder aus anderen Gründen nicht indiziert.
    
    - Nur Elemente, die ein nicht erkennbares Format aufweisen, werden verschlüsselt oder aus anderen Gründen nicht indiziert.
    
6. Optional Aktivieren Sie das Kontrollkästchen **Versionen für SharePoint-Dateien einbeziehen** . 
    
7. Klicken Sie auf **Vorbereiten**.
    
    Die Suchergebnisse werden für die Analyse mit Advanced eDiscovery vorbereitet.
    
8. Klicken Sie auf **Beenden** , um den Detailbereich zu beenden. 
    
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>Schritt 8: Wechseln Sie zu dem Fall in Advanced eDiscovery

Nachdem Sie im Security & Compliance Center einen Fall erstellt haben, können Sie den gleichen Fall in Advanced eDiscovery aufrufen.
  
So navigieren Sie zu einem Fall in Advanced eDiscovery:
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie neben dem Fall, zu dem Sie wechseln möchten, in Advanced eDiscovery auf **Öffnen** . 
    
3. Klicken Sie auf der **Start** Seite für den Fall auf **zu Advanced eDiscovery wechseln**.
    
    ![Wählen Sie wechseln zu Advanced eDiscovery](media/d7e31558-e79c-4782-b841-2b735568a576.png)
  
    Die Statusleiste **Verbinden mit Advanced eDiscovery** wird angezeigt. Wenn Sie mit Advanced eDiscovery verbunden sind, wird auf der Seite eine Liste mit Containern angezeigt. 
    
    ![Erweiterte eDiscorvery-Statusanzeige](media/4a84273d-765b-44b8-9006-c20e810ea393.png)
  
    Diese Container stellen die Suchergebnisse dar, die Sie in Schritt 7 für die Analyse in Advanced eDiscovery vorbereitet haben. Beachten Sie, dass der Name des Containers den gleichen Namen wie die Inhaltssuche in dem Fall im Security & Compliance Center hat. Die Container in der Liste sind diejenigen, die Sie vorbereitet haben. Wenn ein anderer Benutzer Suchergebnisse für Advanced eDiscovery vorbereitet hat, werden die entsprechenden Container nicht in die Liste aufgenommen.
    
4. Wenn Sie die Suchergebnis Daten aus einem Container in den Fall in Advanced eDiscovery laden möchten, wählen Sie einen Container aus, und klicken Sie auf **verarbeiten**.
    
    Weitere Informationen zum Verarbeiten von Containern finden Sie unter [Ausführen des Process-Moduls und Laden von Daten in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md).
    
> [!TIP]
> Klicken Sie auf **zu EDiscovery wechseln** , um zu diesem Fall im Security _AMP_ Compliance Center zurückzukehren. 
  
## <a name="optional-step-9-close-a-case"></a>Optional Schritt 9: Abschließen einer Groß-/Kleinschreibung

Wenn der von einem eDiscovery-Fall unterstützte Rechtsfall oder die Untersuchung abgeschlossen ist, können Sie den Fall abschließen. Hier sehen Sie, was passiert, wenn Sie einen Fall abschließen:
  
- Wenn die Groß-/Kleinschreibung inhaltsspeicherorte enthält, wird diese Sperre deaktiviert. Dies kann dazu führen, dass Inhalte dauerhaft gelöscht oder entfernt werden, entweder durch den Benutzer oder durch einen automatisierten Prozess wie eine Löschrichtlinie.
    
- Durch das Schließen einer Groß-/Kleinschreibung werden nur die haltebereiche deaktiviert, die diesem Fall zugeordnet sind. Wenn andere Haltebereiche an einem Inhaltsspeicherort platziert werden (beispielsweise in einem Rechtsstreit. eine erHaltungs Richtlinie oder eine Aufbewahrungspflicht aus einem anderen eDiscovery-Fall) Diese gilt weiterhin.
    
- Der Fall wird weiterhin auf der eDiscovery-Seite im Security & Compliance Center aufgeführt. Die Details, Haltestatus, suchen und Elemente einer geschlossenen Groß-/Kleinschreibung werden beibehalten.
    
- Sie können einen Fall nach dem Schließen bearbeiten. Beispielsweise können Sie Mitglieder hinzufügen oder entfernen, suchen erstellen, Suchergebnisse exportieren und das Suchergebnis für die Analyse in Advanced eDiscovery vorbereiten. Der Hauptunterschied zwischen aktiven und geschlossenen Fällen besteht darin, dass haltebereiche deaktiviert sind, wenn ein Fall geschlossen wird.
    
So können Sie eine Groß-/Kleinschreibung abschließen:
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der zu schließenden Groß-/Kleinschreibung.
    
    Die Seite **dieses Fall Flyout verwalten** wird angezeigt. 
    
3. Klicken Sie unter **Fall Status verwalten**auf ![die Schaltfläche](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) Peek-Taste **abschließen**.
    
    Es wird eine Warnung angezeigt, die besagt, dass die mit der Anfrage verknüpften haltebereiche deaktiviert werden.
    
4. Klicken Sie auf **Ja** , um den Fall zu beenden. 
    
    Der Status auf der Seite " **dieses Fall Flyout verwalten** " wird von " **aktiv** " in " **Closing**" geändert.
    
5. Beenden Sie die Seite " **diesen Fall verwalten** ". 
    
6. Klicken Sie **** ![auf der Seite eDiscovery auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol **Aktualisieren** , um den Status der geschlossenen Groß-/Kleinschreibung zu aktualisieren. Es kann bis zu 60 Minuten dauern, bis der Schließvorgang abgeschlossen ist. 
    
    Nach Abschluss des Vorgangs wird der Status der Anfrage auf der **eDiscovery** -Seite in **geschlossen** geändert. Klicken Sie erneut auf den Namen des Falls, um die Seite **dieses Fall Flyout verwalten** anzuzeigen, die Informationen dazu enthält, wann der Fall geschlossen wurde und wer ihn geschlossen hat. 
     
## <a name="optional-step-10-re-open-a-closed-case"></a>Optional Schritt 10: Erneutes Öffnen eines Closed Case

Wenn Sie einen Fall erneut öffnen, werden alle haltebereiche, die vorhanden waren, als der Fall geschlossen wurde, nicht automatisch wiederhergestellt. Nachdem der Fall erneut geöffnet wurde, müssen Sie zur Seite "halten" wechseln und die vorherigen **halte** Status aktivieren. Wenn Sie einen Haltestatus aktivieren möchten, wählen Sie ihn aus, und klicken Sie im Detailbereich auf **aktivieren** . 
  
1. Klicken Sie im Security & Compliance Center auf **eDiscovery** \> **eDiscovery** , um die Liste der Fälle in Ihrer Organisation anzuzeigen. 
    
2. Klicken Sie auf den Namen der Anfrage, die Sie erneut öffnen möchten.
    
    Die Seite **dieses Fall Flyout verwalten** wird angezeigt. 
    
3. Klicken Sie unter **Fall Status verwalten**auf **Fall erneut öffnen**.
    
    Es wird eine Warnung angezeigt, die besagt, dass die haltebereiche, die mit dem Fall verbunden waren, nicht automatisch aktiviert werden.
    
4. Klicken Sie auf **Ja** , um den Fall erneut zu öffnen. 
    
    Der Status auf der Seite " **dieses Fall Flyout verwalten** " wird von " **geschlossen** " in " **aktiv**" geändert.
    
5. Beenden Sie die Seite " **diesen Fall verwalten** ". 
    
6. Klicken Sie **** ![auf der Seite eDiscovery auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol **Aktualisieren** , um den Status des neu geöffneten Falls zu aktualisieren. Es kann bis zu 60 Minuten dauern, bis der Vorgang abgeschlossen ist. 
    
    Nach Abschluss des Vorgangs wird der Status des Falls auf der **eDiscovery** -Seite in **aktiv** geändert. 
  
## <a name="more-information"></a>Weitere Informationen

- **Gelten für eDiscovery-Fälle oder für einen eDiscovery-Fall zugeordnete Aufbewahrungs Grenzen?** In der folgenden Tabelle sind die Grenzwerte für eDiscovery-Fälle und Case Holds aufgeführt.
    
  |**Beschreibung der Beschränkung**|**Grenzwert**|
  |:-----|:-----|
  |Maximale Anzahl von Fällen für eine Organisation  <br/> |Keine Begrenzung  <br/> |
  |Maximale Anzahl von Fall Haltebereichen für eine Organisation  <br/> |10,000  <br/> |
  |Maximale Anzahl von Postfächern in einem einzelnen Fall  <br/> |1,000  <br/> |
  |Maximale Anzahl von SharePoint-und OneDrive für Business-Websites in einem einzelnen Fall  <br/> |100  <br/> |
   
- **Was ist mit Fällen, die auf der Seite Fallverwaltung in Advanced eDiscovery erstellt wurden?** Sie können auf eine Liste älterer erweiterter eDiscovery-Fälle zugreifen, indem Sie unten auf der **eDiscovery** -Seite im Security _AMP_ Compliance Center auf den Link klicken. Wenn Sie jedoch in einem älteren Fall arbeiten möchten, müssen Sie sich an den Office 365-Support wenden und den Fall in einen neuen eDiscovery-Fall im Security & Compliance Center verschieben. 
    
- **Gründe für das Festlegen eines eDiscovery-Administrators** Wie bereits erwähnt, ist ein eDiscovery-Administrator Mitglied der Rollengruppe „eDiscovery-Manager“, die alle eDiscovery-Fälle in Ihrer Organisation anzeigen und auf diese zugreifen kann. Dieser Zugriff auf alle eDiscovery-Fälle dient zwei wichtigen Zwecken:
    
  - Wenn eine Person, die das einzige Mitglied eines eDiscovery-Falls ist, die Organisation verlässt, kann niemand (einschließlich Mitglieder der Rollengruppe „Organisationsverwaltung“ oder andere Mitglieder der Rollengruppe „eDiscovery-Manager“) auf diesen eDiscovery-Fall zugreifen, da diese Personen keine Fallmitglieder sind. In diesem Fall gäbe es keine Möglichkeit, auf die Daten in dem Fall zuzugreifen. Da ein eDiscovery-Administrator jedoch auf alle eDiscovery-Fälle in der Organisation zugreifen kann, können Sie den Fall im Security & Compliance Center anzeigen und sich selbst oder einen anderen eDiscovery-Manager als Mitglied der Anfrage hinzufügen.
    
  - Da ein eDiscovery-Administrator alle eDiscovery-Fälle anzeigen und darauf zugreifen kann, können Sie alle Fälle und zugehörige Inhalts suchVorgänge überwachen und überwachen. So kann der Missbrauch von Inhaltssuchen oder anderen eDiscovery-Fällen verhindert werden. Und da eDiscovery-Administratoren potenziell vertrauliche Informationen in den Ergebnissen einer Inhaltssuche zugreifen können, sollten Sie die Anzahl von Personen, die eDiscovery-Administratoren sind, begrenzen.
    
    Schließlich werden, wie bereits zuvor erläutert, eDiscovery-Administratoren im Security & Compliance Center automatisch als Administratoren in Advanced eDiscovery hinzugefügt. Das bedeutet, dass eine Person, die ein eDiscovery-Administrator ist, administrative Aufgaben in Advanced eDiscovery ausführen kann, wie das Einrichten von Benutzern, das Erstellen von Fällen und das Hinzufügen von Daten zu Fällen.
    
- **Welche Lizenzierungsanforderungen müssen erfüllt sein, damit die inhaltsspeicherorte aufbewahrt werden können?** Im Allgemeinen benötigen Organisationen ein Office 365 E3-Abonnement oder höher, um die Aufbewahrung von Inhaltsspeicherorten zu aktivieren. Zur Aufbewahrung von Postfächern ist eine Exchange Online-Plan 2-Lizenz für das Postfach erforderlich, das Sie anhalten möchten.
    
- **Was sollten Sie sonst noch über das Durchsuchen aller Case-Inhalte in Schritt 5 wissen?** Wie bereits erläutert, können Sie die inhaltsspeicherorte durchsuchen, die in der Groß-/Kleinschreibung gehalten wurden. Wenn Sie dies tun, wird nur der Inhalt gesucht, der mit den halte Kriterien übereinstimmt. Wenn es keine Aufbewahrungs Kriterien gibt, wird der gesamte Inhalt durchsucht. Wenn sich Inhalte auf einer abfragebasierten Aufbewahrung befinden, wird nur der Inhalt zurückgegeben, der beiden halte Kriterien entspricht (aus dem in Schritt 4 gehaltenen Haltebereich) und den Suchkriterien (aus der Suche in Schritt 5).
    
    Im folgenden finden Sie einige Punkte, die Sie beachten sollten, wenn Sie alle Case-Inhalte durchsuchen:
    
  - Wenn ein Inhaltsspeicherort Teil mehrerer haltebereiche innerhalb desselben Falls ist, werden die Hold-Abfragen von einem **or** -Operator kombiniert, wenn Sie diesen Inhaltsspeicherort mithilfe der Option "alle Groß-/Kleinschreibung" Durchsuchen. Wenn ein Inhaltsspeicherort Teil von zwei verschiedenen Haltebereichen ist, wobei der eine abfragebasierte und der andere ein unendlicher Halt ist (bei dem der gesamte Inhalt in der Warteschleife gehalten wird), werden alle Inhalte aufgrund des unendlichen Speichers durchsucht. 
    
  - Wenn eine Inhaltssuche für einen Fall ist und Sie Sie so konfiguriert haben, dass alle Case-Inhalte durchsucht werden und Sie dann einen Haltestatus ändern (durch Hinzufügen oder Entfernen eines Inhaltsspeicherorts oder Ändern der Hold-Abfrage), wird die Suchkonfiguration mit diesen Änderungen aktualisiert. Sie müssen jedoch die Suche erneut ausführen, nachdem der Haltebereich geändert wurde, um die Suchergebnisse zu aktualisieren.
    
  - Wenn in einem eDiscovery-Fall mehrere Case-haltebereiche an einem Inhaltsspeicherort gespeichert werden und Sie alle Case-Inhalte durchsuchen möchten, beträgt die maximale Anzahl von Schlüsselwörtern für diese Suchabfrage 500. Der Grund dafür ist, dass die Inhaltssuche alle abfragebasierten haltebereiche mithilfe des **or** -Operators kombiniert. Wenn in den kombinierten Warte-und Inhalts Suchabfragen mehr als 500 Schlüsselwörter vorhanden sind, wird der gesamte Inhalt des Postfachs durchsucht, nicht nur die Inhalte, die mit dem abfragebasierten Case übereinstimmen. 
    
  - Wenn eine Groß-/Kleinschreibung den Status " **aktivieren**" aufweist, können Sie die Anfragen-inhaltsspeicherorte weiterhin durchsuchen, während der Haltebereich aktiviert wird.
    
  - Wenn eine Suche so konfiguriert ist, dass alle Case-Inhalte durchsucht werden, können Sie die Suche nicht einbeziehen, wenn Sie die Ergebnisse mehrerer Suchvorgänge exportieren möchten. Wenn eine Suche so konfiguriert ist, dass alle Case-Inhalte durchsucht werden, müssen Sie die Ergebnisse dieser einzelnen Suche exportieren.
    
- **Wenn ein Postfach, eine SharePoint-Website oder ein OneDrive-Konto, das in der Warteschleife gespeichert ist, in eine andere Region in einer Multi-Geo-Umgebung verschoben wird, gilt der Aufbewahrungs Status weiterhin?** In allen Fällen werden die Inhalte in einem Postfach-, Website-oder OneDrive-Konto weiterhin beibehalten. Die Aufbewahrungs Statistik enthält jedoch keine Elemente mehr aus einem Inhaltsspeicherort, der in eine andere Region verschoben wurde. Um die Aufbewahrungs Statistik für einen verschobenen Inhaltsspeicherort einzuschließen, müssen Sie den Haltebereich bearbeiten und die URL (oder die SMTP-Adresse eines Postfachs) so aktualisieren, dass der Speicherort des Inhalts erneut in der halte Statistik enthalten ist. 
    
- **Was ist mit dem Aufbewahren von Office 365-Gruppen und Microsoft Teams?** Microsoft Teams basieren auf Office 365-Gruppen. Daher ist es sehr ähnlich, Sie in einem eDiscovery-Fall aufzubewahren. Beachten Sie beim Platzieren von Office 365-Gruppen und Microsoft Teams die folgenden Aspekte. 
    
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
    > Damit Sie das Cmdlet **Get-Unifiedgroup** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
  - Wenn das Postfach eines Benutzers durchsucht wird, werden alle Office 365-Gruppen oder Microsoft-Teams, in denen der Benutzer Mitglied ist, nicht durchsucht. Entsprechend werden beim Platzieren einer Office 365-Gruppe oder eines Microsoft Teams nur das Gruppenpostfach und die Gruppen Website in der Warteschleife platziert. die Postfächer und OneDrive für Business-Websites von Gruppenmitgliedern werden nicht in die Warteschleife aufgenommen, es sei denn, Sie fügen Sie explizit dem Haltestatus hinzu. Wenn Sie daher eine Office 365-Gruppe oder ein Microsoft-Team aus rechtlichen Gründen in Betrieb nehmen müssen, sollten Sie die Postfächer und OneDrive für Business-Websites für Gruppen-und Teammitglieder in derselben Warteschleife hinzufügen.
    
  - Um eine Liste der Mitglieder einer Office 365-Gruppe oder eines Microsoft Teams abzurufen, können Sie die Eigenschaften auf der Seite **" \> Startgruppen** " im Microsoft 365 Admin Center anzeigen. Alternativ können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
    
      ```
      Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
      ```

    > [!NOTE]
    > Damit Sie das Cmdlet **Get-UnifiedGroupLinks** ausführen können, müssen Sie die Rolle "nur anzeigen" in Exchange Online oder Mitglied einer Rollengruppe haben, der die Rolle "nur anzeigen" zugewiesen ist. 
  
  - Unterhaltungen, die Teil eines Microsoft Teams-Kanals sind, werden in dem Postfach gespeichert, das dem Microsoft-Team zugeordnet ist. Entsprechend werden Dateien, die Teammitglieder in einem Kanal freigeben, auf der SharePoint-Website des Teams gespeichert. Daher müssen Sie das Microsoft Team-Postfach und die SharePoint-Website anhalten, um Unterhaltungen und Dateien in einem Kanal beizubehalten.
    
    Alternativ werden Unterhaltungen, die Teil der Chat-Liste in Microsoft Teams sind, im Postfach des Benutzers gespeichert, der am Chat teilnimmt. Und Dateien, die ein Benutzer in Chat Unterhaltungen freigibt, werden auf der OneDrive for Business-Website des Benutzers gespeichert, der die Datei frei gibt. Daher müssen Sie die einzelnen Benutzerpostfächer und OneDrive für Business-Websites in der Warteschleife platzieren, um Unterhaltungen und Dateien in der Chat-Liste beizubehalten. Daher empfiehlt es sich, die Postfächer der Mitglieder eines Microsoft-Teams zusätzlich zu halten, um das Team Postfach (und die Website) zu halten.
    
    > [!IMPORTANT]
    > Benutzer, die an Unterhaltungen teilnehmen, die Mitglied der Chat Liste in Microsoft Teams sind, müssen über ein Exchange Online-(Cloud-basiertes) Postfach verfügen, um Chat Unterhaltungen beizubehalten, wenn das Postfach in den eDiscovery-Speicher gestellt wird. Das liegt daran, dass Konversationen, die Teil der Chat Liste sind, in den cloudbasierten Postfächern der Chat Teilnehmer gespeichert werden. Wenn ein Chat Teilnehmer kein Exchange Online-Postfach hat, können Sie keine Chat Unterhaltungen mehr aufbewahren. Beispielsweise können Benutzer mit einem lokalen Postfach in einer Exchange-hybridbereitstellung an Unterhaltungen teilnehmen, die in der Chat Liste in Microsoft Teams enthalten sind. In diesem Fall können Inhalte aus dieser Unterhaltung nicht beibehalten werden, da die Benutzer keine Cloud-basierten Postfächer besitzen. 
  
  - Jeder Microsoft-Team-oder Team Kanal enthält ein wiki für Notizen und Zusammenarbeit. Der wiki-Inhalt wird automatisch in einer Datei mit dem MHT-Format gespeichert. Diese Datei wird in der Microsoft Teams-wiki-Datendokument Bibliothek auf der SharePoint-Website des Teams gespeichert. Sie können die Inhalte im wiki halten, indem Sie die SharePoint-Website des Teams in der Warteschleife platzieren.
    
    > [!NOTE]
    > Die Möglichkeit, wiki-Inhalte für ein Microsoft-Team oder einen Team Kanal beizubehalten (wenn Sie die SharePoint-Website des Teams in der Warteschleife platzieren) wurde am 2017 veröffentlicht. Wenn eine Teamwebsite in der Warteschleife steht, wird der wiki-Inhalt ab diesem Datum aufbewahrt. Wenn jedoch eine Teamwebsite gehalten wird und der Inhalt des Wikis vor dem 22. Juni 2017 gelöscht wurde, wurde der wiki-Inhalt nicht beibehalten. 
  
- **Wie finde ich die URL für OneDrive for Business-Websites?** Informationen zum Erfassen einer Liste der URLs für die OneDrive für Business-Websites in Ihrer Organisation, damit Sie Sie zu einem Haltebereich oder einer Suche, die mit einem eDiscovery-Fall verknüpft ist, hinzufügen können, finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Um dieses Skript ausführen zu können, müssen Sie die SharePoint Online-Verwaltungsshell installieren und verwenden. Fügen Sie die URL der mysite-Domäne Ihrer Organisation jeder OneDrive-Website, die Sie durchsuchen möchten, hinzu. Dies ist die Domäne, die alle Ihre OneDrive enthält. Beispiel: `https://contoso-my.sharepoint.com`. Nachfolgend finden Sie ein Beispiel für eine URL für die OneDrive-Website `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`eines Benutzers:.

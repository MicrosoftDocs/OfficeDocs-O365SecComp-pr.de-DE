---
title: eDiscovery Solution Series Data Spilling Scenario-Suche und Säuberung
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Verwenden Sie Office 365 eDiscovery und Such Tools, um einen Vorfall mit Datenausfällen in Ihrer Organisation zu verwalten und darauf zu reagieren.
ms.openlocfilehash: 50078e3f22ede8a1af2a252a7a6f75710534c062
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258938"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>eDiscovery-Lösungsreihe: Szenario für Daten verschütten – suchen und löschen

 **Was geschieht bei Daten verschütten?** Bei Daten verschütten wird ein vertrauliches Dokument in einer nicht vertrauenswürdigen Umgebung veröffentlicht. Wenn ein Vorfall mit Daten verschütten erkannt wird, ist es wichtig, schnell die Größe und die Speicherorte des Ausfalls zu ermitteln, die Benutzeraktivitäten zu untersuchen und dann die verschütteten Daten dauerhaft aus dem System zu entfernen. 
  
## <a name="data-spillage-scenario"></a>Szenario für Daten verschütten

Sie sind Lead Information Security Officer bei Contoso. Sie werden über eine Daten verschüttende Situation informiert, in der ein Mitarbeiter unwissentlich ein streng vertrauliches Dokument mit mehreren Personen per e-Mail geteilt hat. Sie möchten schnell bewerten, wer dieses Dokument intern und extern erhalten hat. Nachdem Sie identifiziert wurden, möchten Sie die Fall Ergebnisse mit anderen Ermittlern teilen, um Sie zu überprüfen und die Daten dann endgültig aus Office 365 zu entfernen. Nachdem die Untersuchung abgeschlossen ist, möchten Sie einen Bericht mit den Nachweise für die dauerhafte Entfernung und weitere Details zu jedem späteren Zeitpunkt generieren.
  
### <a name="scope-of-this-article"></a>Bereich dieses Artikels

Dieses Dokument enthält eine Liste mit Anweisungen dazu, wie Sie eine Nachricht aus Office 365 dauerhaft entfernen, damit Sie nicht zugänglich oder wiederhergestellt werden kann. Informationen zum Löschen einer Nachricht und zur Wiederherstellung bis zum Ablauf der Aufbewahrungszeit für gelöschte Elemente finden Sie unter [Suchen nach und Löschen von e-Mail-Nachrichten in Ihrer Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md).
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>Workflow für die Verwaltung von Datenüberlauf Ereignissen

Hier finden Sie eine Vorgehensweise zum Verwalten eines Daten verschüttenden Vorfalls:

![Der 8-stufige Workflow für die Verwaltung von Daten verschüttender Vorfälle](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[Optional Schritt 1: Verwalten der Benutzer, die auf den Fall zugreifen können, und Festlegen von Konformitäts Grenzen](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[Schritt 2: Erstellen eines eDiscovery-Falls](#step-2-create-an-ediscovery-case)<br/>
[Schritt 3: Suchen nach verschütteten Daten](#step-3-search-for-the-spilled-data)<br/>
[Schritt 4: überprüfen und Überprüfen der Fall Ergebnisse](#step-4-review-and-validate-case-findings)<br/>
[Schritt 5: Verwenden des Nachrichtenablauf Verfolgungsprotokolls zum Überprüfen der Freigabe von verschütteten Daten](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[Schritt 6: Vorbereiten der Postfächer](#step-6-prepare-the-mailboxes)<br/>
[Schritt 7: Dauerhaftes Löschen der verschütteten Daten](#step-7-permanently-delete-the-spilled-data)<br/>
[Schritt 8: überprüfen, einen Nachweis für das Löschen und überwachen](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>Wissenswertes vor dem Start

- Wenn ein Postfach aufbewahrt wird, verbleibt eine gelöschte Nachricht im Ordner "Wiederherstellbare Elemente", bis der Aufbewahrungszeitraum abgelaufen ist oder der Haltestatus aufgehoben wird. In [Schritt 6](#step-6-prepare-the-mailboxes) wird beschrieben, wie Sie die Aufbewahrung aus den Postfächern entfernen. Erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen des haltebereichs. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat. 
    
- Um zu steuern, welche Benutzerpostfächer ein Daten verschütteter Prüfer durchsuchen und verwalten kann, wer auf den Fall zugreifen kann, können Sie Compliance-Grenzen einrichten und eine benutzerdefinierte Rollengruppe erstellen, die in [Schritt 1](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)beschrieben wird. Zu diesem Zweck müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" sein oder der Rolle "Rollenverwaltung" zugewiesen sein. Wenn Sie oder der Administrator in Ihrer Organisation bereits Kompatibilitäts Grenzen festgelegt haben, können Sie Schritt 1 überspringen.
    
- Zum Erstellen einer Groß-/Kleinschreibung müssen Sie Mitglied der eDiscovery-Manager-Rollengruppe sein oder Mitglied einer benutzerdefinierten Rollengruppe sein, der die Rolle "Fallverwaltung" zugewiesen ist. Wenn Sie kein Mitglied sind, bitten Sie einen Office 365-Administrator, [Sie der Rollengruppe "eDiscovery-Manager" hinzuzufügen](assign-ediscovery-permissions.md).
    
- Zum Löschen von Daten, die in Ihrer Organisation verschüttet wurden, müssen Sie den Befehl [Search-Mailbox-deletecontent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) in Exchange Online PowerShell verwenden. Außerdem müssen Sie zur Verwendung des *deletecontent* -Parameters auch Mitglied einer Rollengruppe in Exchange Online sein, der die Rolle "Post Fach Import-Export" zugewiesen ist. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" unter [Verwalten von Rollengruppen](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx).
    
- So durchsuchen Sie die eDiscovery-Aktivitäten des Office 365-Überwachungsprotokolls in Schritt 8 muss die Überwachung für Ihre Organisation aktiviert sein. Sie können nach Aktivitäten suchen, die innerhalb der letzten 90 Tage durchgeführt wurden. Weitere Informationen zum Aktivieren und Verwenden der Überwachung finden Sie im Abschnitt überprüfen [des datenspill-Ermittlungsprozesses](#auditing-the-data-spillage-investigation-process) in Schritt 8. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>Optional Schritt 1: Verwalten der Benutzer, die auf den Fall zugreifen können, und Festlegen von Konformitäts Grenzen

Je nach ihrer Organisationspraxis müssen Sie steuern, wer auf den eDiscovery-Fall zugreifen kann, der zur Untersuchung eines Daten verschütteten Ereignisses verwendet wird, und die Konformitäts Grenzen einrichten. Am einfachsten können Sie dies tun, indem Sie Ermittler als Mitglieder einer vorhandenen Rollengruppe im Security & Compliance Center hinzufügen und die Rollengruppe dann als Mitglied des eDiscovery-Falls hinzufügen. Informationen zu den integrierten eDiscovery-Rollengruppen und zum Hinzufügen von Mitgliedern zu einem eDiscovery-Fall finden Sie unter [assign eDiscovery Permissions](assign-ediscovery-permissions.md).
  
Sie können auch eine neue Rollengruppe erstellen, die Ihren organisatorischen Anforderungen entspricht. Sie können beispielsweise eine Gruppe von Daten verschütteten Ermittlern in der Organisation für den Zugriff auf und die Zusammenarbeit an allen Daten, die verschüttet werden müssen. Hierzu können Sie die Rollengruppe "Data Spill Investigator" erstellen, die entsprechenden Rollen zuweisen (Export, RMS entSchlüsseln, überprüfen, Vorschau, Konformitäts Suche und Fallverwaltung), die Daten verschütteten Ermittler zur Rollengruppe hinzufügen und dann die Rollengruppe als Mitglied des Daten verschüttenden eDiscovery-Falls. Detaillierte Anweisungen dazu finden Sie unter [Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365](set-up-compliance-boundaries.md) . 
  
## <a name="step-2-create-an-ediscovery-case"></a>Schritt 2: Erstellen eines eDiscovery-Falls

Ein eDiscovery-Fall bietet eine effektive Möglichkeit zum Verwalten der Untersuchung von Daten verschütten. Sie können der Rollengruppe, die Sie in Schritt 1 erstellt haben, Mitglieder hinzufügen, die Rollengruppe als Mitglied eines neuen eDiscovery-Falls hinzufügen, iterative suchen ausführen, um die verschütteten Daten zu finden, einen Bericht zur Freigabe zu exportieren, den Status des Falls nachzuverfolgen und dann auf die Details des c ASE, falls erforderlich. Erwägen Sie, eine Benennungskonvention für eDiscovery-Fälle einzurichten, die für Daten verschüttete Vorfälle verwendet werden, und geben Sie so viele Informationen wie möglich im Fallname und in der Beschreibung an, damit Sie in Zukunft gegebenenfalls suchen und darauf verweisen können.
  
Um einen neuen Fall zu erstellen, können Sie eDiscovery im Security and Compliance Center verwenden. Weitere Informationen finden Sie unter "Erstellen eines neuen Falls" in [eDiscovery-Fällen](ediscovery-cases.md#step-2-create-a-new-case).
  
## <a name="step-3-search-for-the-spilled-data"></a>Schritt 3: Suchen nach verschütteten Daten

Nachdem Sie einen Fall und verwalteten Zugriff erstellt haben, können Sie den Fall verwenden, um iterativ nach den verschütteten Daten zu suchen und die Postfächer zu identifizieren, die die verschütteten Daten enthalten. Sie verwenden die gleiche Suchabfrage, die Sie zum Auffinden der e-Mail-Nachrichten verwendet haben, um diese Nachrichten in [Schritt 7](#step-7-permanently-delete-the-spilled-data)zu löschen.
  
Informationen zum Erstellen einer Inhaltssuche, die mit einem eDiscovery-Fall verknüpft ist, finden Sie unter "erstellen und Ausführen einer mit einem Fall verknüpften Inhaltssuche" in [eDiscovery-Fällen](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case).
  
 **Wichtig:** Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, enthalten möglicherweise die tatsächlich verschütteten Daten, nach denen Sie suchen. Wenn Sie beispielsweise nach Dokumenten suchen, die eine Sozialversicherungsnummer enthalten, und das Schlüsselwort IT as Search verwenden, müssen Sie die Abfrage später löschen, um weiteres verschütten zu vermeiden. Weitere Informationen finden Sie unter [Löschen der Suchabfrage](#deleting-the-search-query) in Schritt 8. 
  
## <a name="step-4-review-and-validate-case-findings"></a>Schritt 4: überprüfen und Überprüfen der Fall Ergebnisse

Nachdem Sie eine Inhaltssuche erstellt haben, müssen Sie die Suchergebnisse überprüfen und überprüfen und sicherstellen, dass Sie nur aus den e-Mail-Nachrichten bestehen, die gelöscht werden müssen. In einer Inhaltssuche können Sie eine Vorschau einer Zufallsstichprobe von 1.000-e-Mail-Nachrichten anzeigen, ohne die Suchergebnisse zu exportieren, um weitere Daten zu vermeiden. Weitere Informationen zu den Einschränkungen für die Vorschau finden Sie unter [Limits for Content Search](limits-for-content-search.md).
  
Wenn Sie mehr als 1.000 Postfächer oder mehr als 100 e-Mail-Nachrichten pro Postfach überarbeiten, können Sie die anfängliche Suche in mehrere Suchvorgänge unterteilen, indem Sie zusätzliche Schlüsselwörter oder Bedingungen wie Datumsbereich oder Absender/Empfänger verwenden und die Ergebnisse jeder Suche überarbeiten. individuell. Notieren Sie sich alle Suchabfragen, die beim Löschen von Nachrichten in [Schritt 7](#step-7-permanently-delete-the-spilled-data)verwendet werden sollen.

Wenn einem Verwalter oder Endbenutzer eine Office 36 E5-Lizenz zugewiesen ist, können Sie bis zu 10.000 Suchergebnisse gleichzeitig mit Office 365 Advanced eDiscovery überprüfen. Wenn mehr als 10.000 e-Mail-Nachrichten überprüft werden sollen, können Sie die Suchabfrage nach Datumsbereich teilen und jedes Ergebnis einzeln überarbeiten, da Suchergebnisse nach Datum sortiert werden. In Advanced eDiscovery können Sie Suchergebnisse mit der **Bezeichnung als** -Funktion im Vorschaufenster kennzeichnen und das Suchergebnis anhand der Beschriftung Filtern. Dies ist hilfreich, wenn Sie mit einem sekundären Prüfer zusammenarbeiten. Mithilfe zusätzlicher Analysetools in Advanced eDiscovery, wie beispielsweise der optischen Zeichenerkennung, des e-Mail-Threadings und der Predictive-Codierung, können Sie Tausende von Nachrichten schnell verarbeiten und überarbeiten und Sie zur weiteren Überprüfungen kennzeichnen. Siehe [Quick Setup für Office 365 Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md).

Wenn Sie eine e-Mail-Nachricht mit verschütteten Daten finden, überprüfen Sie die Empfänger der Nachricht, um festzustellen, ob Sie extern freigegeben wurde. Wenn Sie eine Nachricht weiter verfolgen möchten, können Sie die Absenderinformationen und den Zeitraum erfassen, sodass Sie die in [Schritt 5](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)beschriebenen Nachrichtenablauf Protokolle verwenden können.

Nachdem Sie die Suchergebnisse überprüft haben, können Sie Ihre Ergebnisse mit anderen Benutzern für eine sekundäre Überprüfung freigeben. Personen, die Sie dem Fall in Schritt 1 zugeordnet haben, können den Fall Inhalt sowohl in eDiscovery als auch in Advanced eDiscovery überarbeiten und die Fall Ergebnisse genehmigen. Sie können auch einen Bericht generieren, ohne den tatsächlichen Inhalt zu exportieren. Sie können diesen Bericht auch als einen Lösch Nachweis verwenden, der in [Schritt 8](#step-8-verify-provide-a-proof-of-deletion-and-audit)beschrieben wird.
  
 **So generieren Sie einen statistischen Bericht**
  
1. Wechseln Sie im eDiscovery-Fall zur Seite **Suchen** , und klicken Sie auf die Suche, für die Sie einen Bericht generieren möchten. 
    
2. Klicken Sie auf der Seite Flyout auf **Weitere >-Export Bericht**.
 
      Die Seite Bericht exportieren wird angezeigt.

    ![Wählen Sie die Suche aus, und klicken Sie dann auf der Seite Flyout auf weitere >-Export Bericht.](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. Wählen Sie **alle Elemente aus, einschließlich derer, die nicht erkannt wurden, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden** , und klicken Sie dann auf **Bericht generieren**.

4. Klicken Sie im eDiscovery-Fall auf **exportieren** , um die Liste der Exportaufträge anzuzeigen. Möglicherweise müssen Sie auf **Aktualisieren** klicken, um die Liste zu aktualisieren, um den soeben erstellten Exportauftrag anzuzeigen.

5. Klicken Sie auf den Auftrag exportieren, und klicken Sie dann auf der Seite Flyout auf Bericht **herunterladen** .
 
    ![Klicken Sie auf der Seite exportieren auf den Export, und klicken Sie dann auf "Bericht herunterladen".](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

Der **Zusammenfassungsbericht exportieren** enthält die Anzahl der gefundenen Speicherorte und die Größe der Suchergebnisse. Sie können dies verwenden, um mit dem Bericht zu vergleichen, der nach dem Löschen generiert wurde, und als Beweis für das Löschen angeben. Der **Ergebnis** Bericht enthält eine detailliertere Zusammenfassung der Suchergebnisse, einschließlich Betreff, Absender, Empfänger, wenn die e-Mail gelesen wurde, Daten und Größe der einzelnen Nachrichten. Wenn eines der Details in diesem Bericht die tatsächlich verschütteten Daten enthält, müssen Sie die Datei "results. csv" nach Abschluss der Untersuchung dauerhaft löschen.

Weitere Informationen zum Exportieren von Berichten finden Sie unter [Exportieren eines Inhalts Suchberichts](export-a-content-search-report.md).
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>Schritt 5: Verwenden des Nachrichtenablauf Verfolgungsprotokolls zum Überprüfen der Freigabe von verschütteten Daten

Um zu untersuchen, ob e-Mails mit verschütteten Daten freigegeben wurden, können Sie optional die Nachrichtenablauf Protokolle mit den Absenderinformationen und den Datumsbereichen Abfragen, die Sie in Schritt 4 gesammelt haben. Beachten Sie, dass der Aufbewahrungszeitraum für die Nachrichtenablaufverfolgung 30 Tage für Echtzeitdaten und 90 Tage für Verlaufsdaten beträgt.
  
Sie können die Nachrichtenablaufverfolgung im Security and Compliance Center verwenden oder die entsprechenden Cmdlets in Exchange Online PowerShell verwenden. Beachten Sie, dass die Nachrichtenablaufverfolgung keine vollständigen Garantien für die Vollständigkeit der zurückgegebenen Daten bietet. Weitere Informationen zur Verwendung der Nachrichtenablaufverfolgung finden Sie unter: 
  
- [Nachrichtenablaufverfolgung im Security & Compliance Center](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Neue Nachrichtenablaufverfolgung im Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>Schritt 6: Vorbereiten der Postfächer

Nachdem Sie überprüft und überprüft haben, ob die Suchergebnisse nur die Nachrichten enthalten, die gelöscht werden müssen, müssen Sie eine Liste der e-Mail-Adressen der betroffenen Postfächer sammeln, die Sie in Schritt 7 beim Ausführen des Befehls **Search-Mailbox-deletecontent** verwenden müssen. Möglicherweise müssen Sie auch die Postfächer vorbereiten, bevor Sie e-Mail-Nachrichten dauerhaft löschen können, je nachdem, ob die Wiederherstellung einzelner Elemente in den Postfächern aktiviert ist, die die verschütteten Daten enthalten, oder ob eines dieser Postfächer in der Warteschleife ist.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>Abrufen einer Liste von Adressen von Postfächern mit verschütteten Daten

Es gibt zwei Möglichkeiten, um eine Liste der e-Mail-Adressen von Postfächern mit verschütteten Daten zu sammeln.

**Option 1: Abrufen einer Liste von Adressen von Postfächern mit verschütteten Daten**

1. Öffnen Sie den eDiscovery-Fall, wechseln Sie zur Seite **Suchen** , und wählen Sie die entsprechende Inhaltssuche aus. 
    
2. Klicken Sie auf der Seite Flyout auf **Ergebnisse anzeigen**.
    
3. Klicken Sie in der Dropdownliste **Einzelergebnisse** auf **Suchstatistiken**.
    
4. Klicken Sie in der Dropdownliste **Typ** auf **oberster Speicherort**.
    
    ![Abrufen einer Liste von Postfächern, die Suchergebnisse enthalten, auf der Seite "Top-Speicherorte" in der Suchstatistik](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    Eine Liste mit Postfächern, die Suchergebnisse enthalten, wird angezeigt. Die Anzahl der Elemente in jedem Postfach, die mit der Suchabfrage übereinstimmen, wird ebenfalls angezeigt.
    
5. Kopieren Sie die Informationen in der Liste, speichern Sie Sie in einer Datei, oder klicken Sie auf **herunterladen** , um die Informationen in eine CSV-Datei herunterzuladen. 
    
**Option 2: Abrufen von Postfachspeicher Orten aus dem Exportbericht**

Öffnen Sie den zusammenfassenden Bericht exportieren, den Sie in [Schritt 4](#step-4-review-and-validate-case-findings)heruntergeladen haben. In der ersten Spalte des Berichts wird die e-Mail-Adresse jedes Postfachs unter **Speicherorte**aufgeführt.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>Vorbereiten der Postfächer, damit die verschütteten Daten gelöscht werden können

Wenn die Wiederherstellung einzelner Elemente aktiviert ist oder ein Postfach in der Warteschleife gespeichert wird, wird eine dauerhaft gelöschte Nachricht im Ordner "Wiederherstellbare Elemente" aufbewahrt. Bevor Sie verschüttete Daten löschen können, müssen Sie daher die vorhandenen Postfachkonfigurationen überprüfen und die Wiederherstellung einzelner Elemente deaktivieren und alle Aufbewahrungs-oder Office 365-Speicherrichtlinien entfernen. Denken Sie daran, dass Sie ein Postfach gleichzeitig vorbereiten können, und führen Sie dann denselben Befehl für verschiedene Postfächer aus, oder erstellen Sie ein PowerShell-Skript, um mehrere Postfächer gleichzeitig vorzubereiten.

- Weitere Informationen dazu, wie Sie überprüfen können, ob die Wiederherstellung einzelner Elemente aktiviert ist, oder ob das Postfach in den Speicher verschoben wird, oder dass es einem Benutzer zugewiesen ist, finden Sie unter "Schritt 1: Sammeln von Information über das Postfach" unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) " in "Aufbewahrung". Aufbewahrungsrichtlinie. 
    
- Weitere Informationen zum Deaktivieren der Wiederherstellung einzelner Elemente finden Sie unter "Schritt 2: Vorbereiten des Postfachs" unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von cloudbasierten Postfächern in der Warteschleife](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) . 
    
- Weitere Informationen dazu, wie Sie einen Haltebereich oder eine Aufbewahrungsrichtlinie aus einem Postfach entfernen, finden Sie unter "Schritt 3: alle haltebereiche aus dem Postfach entfernen" unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von Cloud-basierten Postfächern](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) . 

- Weitere Informationen finden Sie unter "Schritt 4: Entfernen der Verzögerungsdauer aus dem Postfach" unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" für Cloud-basierte Postfächer in der Warteschleife](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) .
    
 **Wichtig:** Erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen einer Aufbewahrungs-oder Archivierungsrichtlinie. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat. 
  
Stellen Sie sicher, dass Sie das Postfach auf vorherige Konfigurationen zurücksetzen, nachdem Sie sichergestellt haben, dass die verschütteten Daten dauerhaft gelöscht wurden. Details finden Sie in [Schritt 7](#step-7-permanently-delete-the-spilled-data).

## <a name="step-7-permanently-delete-the-spilled-data"></a>Schritt 7: Dauerhaftes Löschen der verschütteten Daten

Mithilfe der Postfachspeicher Orte, die Sie in Schritt 6 gesammelt und vorbereitet haben, und der in Schritt 3 erstellten und verfeinerten Suchabfrage, um e-Mail-Nachrichten mit den verschütteten Daten zu finden, können Sie die verschütteten Daten jetzt endgültig löschen. Wie bereits erläutert, muss Ihnen die Rolle "Post Fach Import-Export" in Exchange Online zugewiesen werden, um Nachrichten mithilfe des folgenden Verfahrens zu löschen.
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. Führen Sie den folgenden Befehl aus:
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Führen Sie den vorherigen Befehl für jedes Postfach, das die verschütteten Daten enthält, erneut aus, indem Sie den Wert für den Parameter Identity ersetzen. Zum Beispiel:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
Wie bereits erwähnt, können Sie auch ein [PowerShell-Skript](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) erstellen und es mit einer Liste von Postfächern ausführen, damit das Skript die verschütteten Daten in jedem Postfach löscht.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>Schritt 8: überprüfen, einen Nachweis für das Löschen und überwachen

Der letzte Schritt im Workflow zum Verwalten eines Daten verschüttenden Vorfalls besteht darin, zu überprüfen, ob die verschütteten Daten dauerhaft aus dem Postfach entfernt wurden, indem Sie zum eDiscovery-Fall wechseln und dieselbe Suchabfrage erneut ausführen, die zum Löschen dieser Daten verwendet wurde, um zu bestätigen, dass keine Ergebnisse AR e zurückgegeben. Nachdem Sie sichergestellt haben, dass die verschütteten Daten dauerhaft entfernt wurden, können Sie einen Bericht exportieren und ihn (zusammen mit dem ursprünglichen Bericht) als Beweis für das Löschen einbinden. Dann können Sie [den Fall schließen, der](ediscovery-cases.md#optional-step-9-close-a-case)es Ihnen ermöglicht, es erneut zu öffnen, wenn Sie in Zukunft darauf verweisen. Darüber hinaus können Sie Postfächer auch in den vorherigen Zustand zurücksetzen, die Suchabfrage zum Auffinden der verschütteten Daten löschen und nach Überwachungsdatensätzen der ausgeführten Aufgaben suchen, wenn Sie den Vorfall zur Daten Auslagen Verwaltung ausführen. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>Zurücksetzen der Postfächer in den vorherigen Zustand

Wenn Sie in Schritt 6 eine Postfachkonfiguration geändert haben, um die Postfächer vorzubereiten, bevor die verschütteten Daten gelöscht wurden, müssen Sie Sie in den vorherigen Zustand zurücksetzen. Weitere Informationen finden Sie unter "Schritt 6: Zurücksetzen des Postfachs in den vorherigen Status" unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von cloudbasierten Postfächern in der Warteschleife](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state).
  
### <a name="deleting-the-search-query"></a>Löschen der Suchabfrage

Wenn die Schlüsselwörter in der Suchabfrage, die Sie in Schritt 3 erstellt und verwendet haben, einige der tatsächlich verschütteten Daten enthalten, sollten Sie die Suchabfrage löschen, um zu verhindern, dass weitere Daten verschüttet werden.
  
1. Öffnen Sie im Security and Compliance Center den eDiscovery-Fall, wechseln Sie zur Seite **Suchen** , und wählen Sie die entsprechende Inhaltssuche aus.
    
2. Klicken Sie auf der Seite Flyout auf **Löschen**.

    ![Wählen Sie die Suche aus, und klicken Sie dann auf der Seite Flyout auf Löschen.](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>ÜberWachen des Ermittlungsprozesses für Daten ausschütten

Sie können im Office 365-Überwachungsprotokoll nach den eDiscovery-Aktivitäten suchen, die während der Untersuchung durchgeführt wurden. Sie können auch das Überwachungsprotokoll durchsuchen, um die Überwachungsdatensätze zurückzugeben, die beim Ausführen des Befehls **Search-Mailbox-deletecontent** erstellt wurden, um die verschütteten Daten zu löschen. Weitere Informationen finden Sie unter:

- [Durchsuchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md)

- [Suchen nach eDiscovery-Aktivitäten im Überwachungsprotokoll](search-for-ediscovery-activities-in-the-audit-log.md)

- Informationen zum Suchen nach Überwachungsdatensätzen im Zusammenhang mit ausgeführten Cmdlets in Exchange Online finden Sie im Abschnitt "überwachte Aktivitäten-Exchange-administratorüberwachungsprotokoll" im [Überwachungsprotokoll durchsuchen](search-the-audit-log-in-security-and-compliance.md#audited-activities) .
  


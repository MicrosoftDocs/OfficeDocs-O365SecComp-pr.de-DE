---
title: eDiscovery-Lösung Datenreihe Daten stellen-Szenario – suchen und löschen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Verwenden Sie eDiscovery, und suchen Sie Office 365-Tools zum Verwalten und reagieren auf eine Daten stellen Vorfall in Ihrer Organisation.
ms.openlocfilehash: d2c5a0a6efcc75a38df97c7c597503e5642f83eb
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575349"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>eDiscovery-Lösung Series: Daten stellen Szenario - suchen und löschen

 **Daten stellen Neuigkeiten und warum sollte Sie das interessieren?** Daten stellen ist, wenn ein vertrauliches Dokument in einer nicht vertrauenswürdigen Umgebung freigegeben ist. Wenn ein Daten stellen Vorfall erkannt wird, ist es wichtig, schnell Bewerten der Größe und Standorte von der Stellen, untersuchen Sie die Benutzeraktivitäten herum und verschütteten Daten dann dauerhaft aus dem System löschen. 
  
## <a name="data-spillage-scenario"></a>Daten stellen Szenario

Sie können eine Lead Information Security Officer bei Contoso. Sie sind für eine Situation, stellen Daten darüber informiert, in dem ein Mitarbeiter unwissentlich ein streng vertrauliches Dokument mit mehreren Personen per e-Mail gemeinsam genutzt. Möchten Sie schnell bewerten, die in diesem Dokument intern und extern empfangen. Sobald identifiziert, möchten Sie Groß-/Kleinschreibung Ergebnisse mit anderen Prüfer, um zu prüfen, und entfernen Sie die Daten endgültig aus Office 365 freigeben. Nach Abschluss die Untersuchung, erstellen Sie einen Bericht mit dem Beweis des endgültig zu löschen und andere Groß-/Kleinschreibung Details für alle zukünftigen werden soll.
  
### <a name="scope-of-this-article"></a>Themenbereich dieses Artikels

Dieses Dokument enthält eine Liste von Anweisungen zum dauerhaft entfernen einer Nachricht aus Office 365, damit nicht zugänglich oder wiederhergestellt ist. Zum Löschen einer Nachricht, und machen es wiederherstellbare, bis die Aufbewahrungszeit für gelöschte abläuft, finden Sie unter [Suchen und Löschen von e-Mail-Nachrichten in Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md).
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>Workflows zum Verwalten von Daten stellen Vorfälle

Wie sieht einen Daten stellen Vorfall verwalten:

![Schritt 8 Workflows zum Verwalten von Daten stellen Vorfälle](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[(Optional) Schritt 1: Verwalten Sie können, wer Zugriff auf die Groß-/Kleinschreibung und Compliance-Grenzen festlegen](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[Schritt 2: Erstellen Sie einen eDiscovery-Fall](#step-2-create-an-ediscovery-case)<br/>
[Schritt 3: Suchen nach die verschütteten Daten](#step-3-search-for-the-spilled-data)<br/>
[Schritt 4: Überprüfen Sie, und überprüfen Sie die Groß-/Kleinschreibung Ergebnisse](#step-4-review-and-validate-case-findings)<br/>
[Schritt 5: Verwendung Nachricht Ablaufverfolgungsprotokoll wie verschütteten Daten überprüft wurde freigegeben.](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[Schritt 6: Vorbereiten der Postfächer](#step-6-prepare-the-mailboxes)<br/>
[Schritt 7: Die verschütteten Daten endgültig löschen](#step-7-permanently-delete-the-spilled-data)<br/>
[Schritt 8: Stellen Sie sicher, nachweisen des Löschens und überwachen](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>Wichtige Informationen, bevor Sie beginnen

- Wenn ein Postfach in der Warteschleife ist, bleibt eine gelöschte Nachricht im Ordner "wiederherstellbare Elemente", bis der Aufbewahrungszeitraum abgelaufen ist oder die Aufbewahrungsrichtlinie deaktiviert wird. [Schritt 6](#step-6-prepare-the-mailboxes) wird beschrieben, wie die Postfächer Halten aufheben. Wenden Sie sich die Verwaltung von Datensätzen und rechtliche Abteilungen vor dem Haltebereich zu entfernen. Ihre Organisation möglicherweise eine Richtlinie, die definiert, ob ein Postfach auf halten oder ein Daten stellen Vorfall Vorrang. 
    
- Um zu steuern, welche Benutzerpostfächer ein Daten stellen Prüfer kann suchen und verwalten, die die Groß-/Kleinschreibung zugreifen können, können Sie Compliance-Grenzen einrichten und erstellen eine benutzerdefinierten Rollengruppe, die in [Schritt 1](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)beschrieben ist. Zu diesem Zweck müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" oder die Verwaltungsrolle Rolle zugewiesen werden. Wenn Sie oder in Administrator in Ihrer Organisation bereits Set Compliance Grenzen hat, können Sie Schritt 1 überspringen.
    
- Um eine Anfrage zu erstellen, müssen Sie Mitglied der Gruppe der eDiscovery-Manager-Rolle sein oder ein Mitglied einer benutzerdefinierten Rollengruppe, die die Groß-/Kleinschreibung Verwaltungsrolle zugewiesen hat. Wenn Sie kein Mitglied sind, bitten Sie einen Office 365-Administrator, [Fügen Sie der Gruppe eDiscovery-Manager-Rolle hinzu](assign-ediscovery-permissions.md).
    
- Zum Löschen von Daten, die in Ihrer Organisation verschüttet ist, müssen Sie den Befehl [Search-Mailbox-DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) in Exchange Online PowerShell verwenden. Wenn Sie den Parameter *DeleteContent* verwenden, müssen Sie darüber hinaus auch ein Mitglied einer Rollengruppe in Exchange Online sein, die die Postfach Import/Export-Rolle zugewiesen hat. Finden Sie im Abschnitt "Hinzufügen eine Rolle zu einer Rollengruppe" [Rollengruppen verwalten](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx).
    
- Um die Office 365 Audit Log eDiscovery Aktivitäten in Schritt 8 zu suchen, muss die Überwachung für Ihre Organisation aktiviert werden. Sie können nach Aktivitäten suchen, die innerhalb der letzten 90 Tage durchgeführt wurden. Finden Sie weitere Informationen zum Aktivieren und mithilfe der Überwachung finden Sie im Abschnitt [Überwachung stellen Untersuchung von Daten](#auditing-the-data-spillage-investigation-process) in Schritt 8 ein. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>(Optional) Schritt 1: Verwalten Sie können, wer Zugriff auf die Groß-/Kleinschreibung und Compliance-Grenzen festlegen

Je nach Ihrer Organisation praktischen müssen Sie steuern, wer die eDiscovery-Fall verwendet, um eine Daten stellen Vorfall untersuchen und Einrichten von Compliance-Grenzen zugreifen kann. Die einfachste Möglichkeit hierzu ist Prüfer als Mitglieder von einer vorhandenen Rollengruppe im Compliance Center & Sicherheit in Office 365 hinzufügen und anschließend die Rollengruppe als Mitglied der eDiscovery-Fall hinzugefügt. Informationen zu integrierten eDiscovery Rollengruppen und Hinzufügen von Mitgliedern zu einer eDiscovery-Fall finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
  
Sie können auch eine neue Rollengruppe erstellen, die mit Ihrer Anforderungen in der Organisation abschließt. Beispielsweise sollten Sie eine Gruppe von Daten stellen Prüfer in der Organisation für den Zugriff und auf allen Daten stellen Fällen zusammenarbeiten. Sie können hierzu eine Rollengruppe "Daten stellen Prüfer" erstellen, zuweisen die entsprechenden Rollen (Export, RMS entschlüsseln, überprüfen, Preview, Compliance-Suche und Case Management), die Daten stellen Prüfer der Rollengruppe hinzufügen und klicken Sie dann Hinzufügen der Rollengruppe als Mitglied der Daten stellen eDiscovery-Fall. Informationen dazu finden Sie unter [Einrichten von Compliance-Grenzen für eDiscovery Untersuchungen in Office 365](set-up-compliance-boundaries.md) . 
  
## <a name="step-2-create-an-ediscovery-case"></a>Schritt 2: Erstellen Sie einen eDiscovery-Fall

EDiscovery-Fall bietet eine effiziente Möglichkeit, Ihre Daten stellen Untersuchung verwalten. Sie können Hinzufügen von Mitgliedern der Rollengruppe, die Sie in Schritt 1 erstellt haben, hinzufügen die Rollengruppe als Mitglied der neuen eDiscovery-Fall, iterative Suchvorgänge die verschütteten Daten suchen, das Exportieren eines Berichts für die Freigabe Nachverfolgen des Status von der Groß-/Kleinschreibung durchführen und dann wieder auf die Details der c verweisen ASE, falls erforderlich. Festlegen einer Namenskonvention für eDiscovery-Fälle verwendet für Daten stellen Vorfälle berücksichtigen und können in Groß-/Kleinschreibung Name und Beschreibung können Suchen und finden Sie in der Zukunft bei Bedarf Informationen bereit.
  
Um einen neuen Vorgang erstellen, können Sie eDiscovery in das Wertpapier &amp; Compliance Center. Finden Sie unter "Erstellen eines neuen Vorgangs in [eDiscovery-Fälle im Compliance Center & Sicherheit in Office 365"](ediscovery-cases.md#step-2-create-a-new-case).
  
## <a name="step-3-search-for-the-spilled-data"></a>Schritt 3: Suchen nach die verschütteten Daten

Nun, dass Sie eine Anfrage und verwalteten Zugriff erstellt haben, können Sie die Groß-/Kleinschreibung, bei der Suche iterativ die verschütteten Daten suchen und identifizieren die Postfächer, die die verschütteten Daten enthalten. Sie verwenden die gleichen Search-Abfrage, mit der Sie die e-Mail-Nachrichten an die gleichen Nachrichten im [Schritt 7](#step-7-permanently-delete-the-spilled-data)löschen finden.
  
So erstellen Sie einen Inhalt Suchvorgänge mit einem eDiscovery-Fall verknüpft ist, finden Sie unter "Erstellen und ausführen, der eine Anfrage eine Inhaltssuche zugeordnet" in [eDiscovery-Fälle, in der Office 365-Sicherheit und Compliance Center](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case).
  
 **Wichtig:** Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, können die tatsächlichen verschütteten Daten enthalten, denen Sie suchen. Wenn Sie die Suche nach Dokumenten mit einer Sozialversicherungsnummer und Sie die It als Suchbegriff in die Suche verwenden, müssen Sie die Abfrage anschließend zur Vermeidung von weiteren stellen löschen. Finden Sie in Schritt 8 [Löschen der Suchabfrage](#deleting-the-search-query) . 
  
## <a name="step-4-review-and-validate-case-findings"></a>Schritt 4: Überprüfen Sie, und überprüfen Sie die Groß-/Kleinschreibung Ergebnisse

Nachdem Sie eine Inhaltssuche erstellt haben, müssen Sie überprüfen, und überprüfen Sie, ob die Suche führt zu, und stellen Sie sicher, dass sie nur aus der e-Mail-Nachrichten bestehen, die gelöscht werden müssen. In einer Inhaltssuche können Sie eine Stichproben von 1.000 e-Mails Vorschau anzeigen, ohne die Suchergebnisse zur Vermeidung von weiteren stellen Daten exportieren. Lesen Sie mehr zu den Einschränkungen Preview unter [Grenzwerte für die Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center](limits-for-content-search.md).
  
Wenn Sie Postfächer mehr als 1.000 oder mehr als 100 e-Mail-Nachrichten pro Postfach, um zu prüfen verfügen, können Sie mehrere Suchvorgänge zusätzliche Schlüsselwörter oder Bedingungen wie Datumsbereich oder Absender/Empfänger mithilfe die erste Suche unterteilen und überprüfen Sie die Ergebnisse jeder Suche einzeln. Stellen Sie sicher, dass Sie notieren Sie alle von Suchabfragen verwenden, wenn Sie in [Schritt 7](#step-7-permanently-delete-the-spilled-data)Nachrichten löschen.

Wenn ein Verwaltungsberechtigter oder Endbenutzer eine Office 36 E5 Lizenz zugewiesen ist, können Sie bis zu 10.000 Suchergebnisse, die gleichzeitig mit Office 365 erweiterte eDiscovery überprüfen. Wenn mehr als 10.000 e-Mail-Nachrichten überprüfen vorhanden sind, können Sie teilen Sie die Suchabfrage durch Datumsbereich und überprüfen jedes Ergebnis einzeln als suchen, die Ergebnisse nach Datum sortiert werden. Im erweiterten eDiscovery können Suchergebnisse mit der **Bezeichnung als** Feature im Vorschaufenster markieren und filtern, indem Sie das Tag, das Sie mit der Bezeichnung das Suchergebnis. Dies ist hilfreich, wenn Sie mit einer sekundären Reviewer zusammenarbeiten. Mit zusätzlichen Analytics Tools in erweiterten eDiscovery, wie optische zeichenerkennung, e-Mail-threading und vorhersehbare codieren, können Sie schnell zu verarbeiten und Tausende von Nachrichten überprüfen und markieren sie zur späteren Überprüfung. Finden Sie [Schnelles Setup für Office 365 erweiterte eDiscovery](quick-setup-for-advanced-ediscovery.md).

Wenn Sie eine e-Mail-Nachricht, die verschütteten Daten enthält gefunden, überprüfen Sie die Empfänger der Nachricht zu ermitteln, ob sie extern freigegeben wurde. Weitere verfolgen können eine Nachricht Sie sammeln Absenderinformationen und Datumsbereich, sodass Sie die Ablaufverfolgungsprotokolle Nachricht verwenden können, die in [Schritt 5](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)beschrieben wird.

Afer Sie die Suchergebnisse überprüft haben, sollten Sie Ihre Ergebnisse für eine sekundäre Überprüfung für andere Benutzer freizugeben. Personen, die Sie in Schritt 1 der Fall zugewiesen haben können die Groß-/Kleinschreibung Inhalte in eDiscovery und erweiterte eDiscovery überprüfen und Genehmigen von Groß-/Kleinschreibung Ergebnisse. Sie können auch einen Bericht generieren, ohne die tatsächlichen Inhalte zu exportieren. Sie können auch in demselben Bericht als Beweis für löschen, die in [Schritt 8](#step-8-verify-provide-a-proof-of-deletion-and-audit)beschrieben wird.
  
 **Einen Bericht statistische:**
  
1. Wechseln Sie zu der Seite **Suchen** in der eDiscovery-Fall, und klicken Sie auf die Suche, der Sie für einen Bericht erstellen möchten. 
    
2. Klicken Sie auf der Seite flyoutmenü auf **mehr > Exportieren Bericht**.
 
      Die Export-Bericht angezeigt wird.

    ![Wählen Sie die Suche, und klicken Sie auf Weiter > Exportieren Bericht auf der Seite flyoutmenü](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. Wählen Sie **alle Elemente, einschließlich Schriftarten, die unbekanntes Format haben, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht** aus, und klicken Sie dann auf **Bericht generieren**.

4. Klicken Sie in der eDiscovery-Fall auf **Exportieren** , um die Liste der Exportaufträge anzuzeigen. Möglicherweise müssen Sie auf **Aktualisieren** , zum Aktualisieren der Liste, um den Exportauftrag anzuzeigen, den Sie gerade erstellt haben.

5. Klicken Sie auf den Exportauftrag aus, und klicken Sie dann auf Bericht auf der Seite flyoutmenü **herunterladen** .
 
    ![Klicken Sie auf der Seite exportieren auf die exportieren, und klicken Sie dann auf "Bericht herunterladen"](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

Der **Exportieren zusammenfassenden** Bericht enthält die Anzahl der Standorte gefunden, deren Ergebnisse und die Größe der Suchergebnisse. Hiermit können Sie mit dem Bericht generiert nach Löschvorgang vergleichen und als Beweis des Löschens bereitstellen. Der Bericht der **Suchergebnisse** enthält eine ausführlichere Zusammenfassung der Suchergebnisse, einschließlich der Betreff, Absender, Empfänger, wenn die Nachricht gelesen wurde, Datumsangaben und Größe der einzelnen Nachrichten. Wenn alle Details in diesem Bericht enthält die tatsächlichen verschütteten Daten, müssen Sie unbedingt die Datei Results.csv dauerhaft zu löschen, wenn die Untersuchung abgeschlossen wurde.

Weitere Informationen zum Exportieren von Berichten finden Sie unter [Exportieren eines Berichts Inhaltssuche](export-a-content-search-report.md).
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>Schritt 5: Verwendung Nachricht Ablaufverfolgungsprotokoll wie verschütteten Daten überprüft wurde freigegeben.

Um weitere untersuchen, wenn e-Mail mit verschütteten Daten freigegeben wurde, können Sie optional die Ablaufverfolgungsprotokolle Nachricht mit der Absenderinformationen und die Informationen zu Datumsbereich, die Sie in Schritt 4 gesammelt Abfragen. Beachten Sie, dass der Aufbewahrungszeitraum für nachrichtenablaufverfolgung 30 Tage für Echtzeitdaten und 90 Tage Verlaufsdaten ist.
  
Sie können die nachrichtenablaufverfolgung im Compliance Center & Sicherheit verwenden oder verwenden Sie die entsprechenden Cmdlets in Exchange Online PowerShell. Es ist wichtig, beachten Sie, dass nachrichtenablaufverfolgung vollständige Garantien für die Vollständigkeit der zurückgegebenen Daten nicht angeboten wird. Weitere Informationen zur Verwendung von nachrichtenablaufverfolgung finden Sie unter: 
  
- [Nachricht Trace in die Office 365-Sicherheit &amp; Compliance Center](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Neue Message Trace in Office 365-Sicherheit &amp; Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>Schritt 6: Vorbereiten der Postfächer

Nachdem Sie überprüfen, und überprüfen, dass die Suchergebnisse enthält nur die Nachrichten, die gelöscht werden müssen, müssen Sie eine Liste der e-Mail-Adressen der betroffenen Postfächer verwenden Sie in Schritt 7 beim Ausführen des Befehls **Search-Mailbox-DeleteContent** sammeln. Sie müssen auch die Postfächer vorbereiten, bevor Sie endgültig löschen, können e-Mail-Nachrichten, abhängig davon, ob der Wiederherstellung einzelner Elemente auf die Postfächer, die die verschütteten Daten enthalten, oder aktiviert ist wenn eines dieser Postfächer auf halten.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>Abrufen einer Liste von Adressen der Postfächer mit verschütteten Daten

Es gibt zwei Methoden, um eine Liste der e-Mail-Adressen von Postfächern mit verschütteten Daten erfassen.

**Option 1: Abrufen einer Liste von Adressen der Postfächer mit verschütteten Daten**

1. Öffnen Sie die eDiscovery-Fall, wechseln Sie zu **der Seite** , und wählen Sie den entsprechenden Inhalten suchen. 
    
2. Klicken Sie auf der Seite flyoutmenü auf **Ergebnisse anzeigen**.
    
3. Klicken Sie in der Dropdownliste **einzelne Ergebnisse** auf **Suchstatistik**.
    
4. Klicken Sie in der Dropdownliste **Typ** auf **oberen Speicherorte**.
    
    ![Abrufen einer Liste der Postfächer, die Suchergebnisse auf der Seite Leiste Speicherorte in die Suchstatistik enthalten](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    Eine Liste der Postfächer, die Suchergebnisse enthalten wird angezeigt. Die Anzahl der Elemente in den einzelnen Postfächern, die die Suchabfrage entsprechen wird auch angezeigt.
    
5. Kopieren Sie die Informationen in der Liste und in eine Datei zu speichern Sie, oder klicken Sie auf **herunterladen** , um die Informationen in eine CSV-Datei herunterladen. 
    
**Option 2: Get-Postfach Speicherorte aus dem Bericht exportieren**

Öffnen Sie in [Schritt 4](#step-4-review-and-validate-case-findings)der Zusammenfassungsbericht exportieren, die Sie heruntergeladen haben. Die e-Mail-Adresse der einzelnen Postfächer wird in der ersten Spalte im Bericht klicken Sie unter **Speicherorte**aufgeführt.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>Vorbereiten der Postfächer, damit können Sie die verschütteten Daten löschen

Wenn die Wiederherstellung einzelner Elemente aktiviert ist, oder wenn ein Postfach in die Warteschleife gestellt wird, wird eine endgültig gelöschte (Zeitfenster) Nachricht im Ordner wiederherstellbare Elemente aufbewahrt werden. Bevor Sie verschütteten Daten endgültig löschen können, müssen Sie so überprüfen die vorhandenen Postfachkonfigurationen und Wiederherstellung einzelner Elemente deaktivieren und entfernen Sie alle Haltestatus oder Office 365-Aufbewahrungsrichtlinie. Lassen Sie beachten Sie, dass Sie können ein Postfach zu einem Zeitpunkt vorbereiten und führen Sie den gleichen Befehl auf verschiedene Postfächer, oder ein PowerShell-Skripts erstellen, um mehrere Postfächer gleichzeitig vorzubereiten.

- Finden Sie unter "Schritt 1: Sammeln von Informationen über das Postfach" in Anweisungen zu überprüfen, ob die Wiederherstellung einzelner Elemente aktiviert ist oder wenn das Postfach befindet Archiv oder zugeordnet ist, zum [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) einer Aufbewahrungsrichtlinie. 
    
- Finden Sie unter "Schritt 2: Vorbereiten des Postfachs" in eine Anleitung zum Deaktivieren der Wiederherstellung einzelner Elemente [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) . 
    
- Finden Sie unter "Schritt 3: Entfernen Sie alle Haltestatus aus dem Postfach" in eine Anleitung zum Entfernen eine Richtlinie halten oder die Aufbewahrung von ein Postfach [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) . 

- Finden Sie unter "Schritt 4: entfernen, halten Sie die Verzögerung aus dem Postfach" in das [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) Anweisungen zum Entfernen der Verzögerung halten, die für das Postfach befindet, nachdem alle Arten von Haltestatus entfernt wurde.
    
 **Wichtig:** Mit der datensatzverwaltung oder der rechtlichen Abteilungen vor dem Entfernen einer Richtlinie halten oder die Aufbewahrung prüfen. Ihrer Organisation möglicherweise eine Richtlinie, die definiert, ob ein Postfach auf halten, oder ein Daten stellen Vorfall Vorrang. 
  
Achten Sie darauf, dass das vorherigen Konfigurationen für das Postfach wiederherzustellen, nachdem Sie überprüft haben, dass die verschütteten Daten dauerhaft gelöscht wurde. Finden Sie die Details in [Schritt 7](#step-7-permanently-delete-the-spilled-data).

## <a name="step-7-permanently-delete-the-spilled-data"></a>Schritt 7: Die verschütteten Daten endgültig löschen

Verwenden die Postfach-Speicherorte, die gesammelt und in Schritt 6 und die Suchabfrage, die erstellt wurde und in Schritt 3, um e-Mail-Nachrichten suchen, die die verschütteten Daten enthalten eingeschränkt vorbereitet haben, können Sie jetzt dauerhaft verschütteten Daten löschen. Wie bereits erklärt müssen Sie die Rolle Postfach Import/Export in Exchange Online zum Löschen von Nachrichten anhand des folgenden Verfahrens zugewiesen werden.
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. Führen Sie den folgenden Befehl aus:
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Führen Sie den vorherigen Befehl für jedes Postfach mit den verschütteten Daten, indem Sie den Wert für den Parameter Identity ersetzen erneut aus; Zum Beispiel:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
Wie bereits zuvor erwähnt können auch ein [Powershell-Skript](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) erstellen und ausführen, gegen eine Liste der Postfächer, dass das Skript die verschütteten Daten in jedem Postfach gelöscht.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>Schritt 8: Stellen Sie sicher, nachweisen des Löschens und überwachen

Der letzte Schritt des Workflows zum Verwalten von eines Daten stellen Vorfalls ist, um sicherzustellen, dass die verschütteten Daten dauerhaft aus dem Postfach entfernt wurde zu eDiscovery-Fall und erneutes Ausführen der gleichen Search-Abfrage, die verwendet wurde, um den Daten, um sicherzustellen, dass keine Ergebnisse Ar löschen e zurückgegeben. Nach dem Sie, dass die verschütteten Daten dauerhaft entfernt wurde bestätigen, können Sie Exportieren eines Berichts und (zusammen mit den ursprünglichen Bericht) als einen Nachweis des Löschens einzuschließen. Anschließend können Sie [die Groß-/Kleinschreibung schließen](ediscovery-cases.md#optional-step-9-close-a-case), denen Sie es erneut öffnen, wenn Sie haben darauf verweisen in der Zukunft können. Darüber hinaus können Sie auch Postfächer zurückkehren löschen Sie den vorherigen Zustand, die die Suchabfrage verwendet, um die verschütteten Daten suchen, und suchen für die Überwachung von Datensätzen Aufgaben beim Verwalten des Daten stellen Vorfalls ausgeführt. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>Die Postfächer in den vorherigen Zustand zurücksetzen

Wenn Sie geändert Konfiguration für Postfächer in Schritt 6 haben, um die Postfächer vorzubereiten, bevor die verschütteten Daten gelöscht wurde, müssen Sie sie in den vorherigen Zustand zurückgesetzt. Finden Sie unter "Schritt 6: das Postfach in den vorherigen Zustand zurückgesetzt" in das [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state).
  
### <a name="deleting-the-search-query"></a>Löschen der Suchabfrage

Wenn die Schlüsselwörter in der Suchabfrage, die Sie erstellt und verwendet in Schritt 3 enthält einige oder alle der tatsächlichen verschütteten Daten, sollten Sie die Search-Abfrage aus, um weitere stellen Daten zu verhindern löschen.
  
1. Öffnen Sie im Compliance Center & Sicherheit die eDiscovery-Fall, wechseln Sie zu **der Seite** , und wählen Sie die entsprechenden Inhaltssuche.
    
2. Klicken Sie auf der Seite flyoutmenü auf **Löschen**.

    ![Wählen Sie die Suche, und klicken Sie dann auf Löschen klicken Sie auf der Seite flyoutmenü](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>Überwachung stellen Untersuchung von Daten

Sie können das Office 365-Überwachungsprotokoll für die eDiscovery-Aktivitäten suchen, die während der Untersuchung ausgeführt wurden. Sie können auch suchen im Überwachungsprotokoll Rückgabe der Audit-Einträge, die erstellt wurden, wenn Sie den Befehl **Search-Mailbox-DeleteContent** zum Löschen der Daten verschütteten ausgeführt haben. Weitere Informationen finden Sie unter:

- [Durchsuchen des Überwachungsprotokolls im Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md)

- [Suchen Sie nach eDiscovery-Aktivitäten im Überwachungsprotokoll Office 365](search-for-ediscovery-activities-in-the-audit-log.md)

- Finden Sie im Abschnitt "Überwacht Aktivitäten - Exchange-Administrator-Überwachungsprotokoll" bei der [Suche der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities) Hinweise zum Suchen nach Audit Datensätze im Zusammenhang mit der Ausführung des Cmdlets in Exchange Online.
  


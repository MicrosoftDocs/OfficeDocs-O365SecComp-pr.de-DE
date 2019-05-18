---
title: Verwalten eines Ereignisses zur Verschütten von Daten in Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: In diesem Artikel wird beschrieben, wie Sie mit dem Tool für neue Daten Untersuchungen (Vorschau) im Security & Compliance Center einen Vorfall zur Verschütten von Daten verwalten.
ms.openlocfilehash: 7aada296566bb5312ab56680485798323d0ab096
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150747"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Verwalten eines Ereignisses zur Verschütten von Daten in Microsoft 365

Das Verschütten von Daten erfolgt, wenn ein Dokument mit vertraulichen, vertraulichen oder bösartigen Informationen in einer nicht vertrauenswürdigen Umgebung freigegeben wird. Wenn ein Vorfall mit Datenüberlauf erkannt wird, ist es wichtig, dass die Umgebung schnell enthalten ist, die Größe und die Standorte des Verfalls bewertet, die Benutzeraktivitäten um Sie herum überprüft und dann die verschütteten Daten aus dem Dienst gelöscht werden. Mithilfe des Tools zur Datenermittlung (Preview) können Sie nach vertraulichen, böswilligen oder veralteten Daten in Office 365 suchen, um herauszufinden, was passiert ist, und dann entsprechende Aktionen durchführen.  

## <a name="scope-of-this-article"></a>Umfang dieses Artikels

Dieser Artikel enthält eine Liste mit Anweisungen zum endgültigen Löschen von Elementen aus Office 365 Postfächern, damit Sie nicht mehr zugänglich sind oder von Benutzern oder Administratoren wiederhergestellt werden können. 

> [!NOTE]
> Wenn Sie Elemente löschen, die sich in einer SharePoint-oder OneDrive für Unternehmen-Website befinden, werden Sie für 93 Tage ab dem Zeitpunkt aufbewahrt, zu dem Sie Sie aus Ihrem ursprünglichen Speicherort löschen.

## <a name="scenario"></a>Szenario

Sie werden über einen Vorfall mit Datenüberlauf informiert, bei dem ein Mitarbeiter unwissentlich ein streng vertrauliches Dokument mit mehreren Personen per e-Mail freigegeben hat. Sie möchten schnell beurteilen, wer dieses Dokument empfangen hat, sowohl innerhalb als auch außerhalb Ihrer Organisation. Nachdem Sie den Vorfall untersucht haben, planen Sie, ihre Ergebnisse mit anderen Ermittlern zu überprüfen und die verschütteten Daten dann endgültig aus Ihrer Office 365 Organisation zu entfernen. Nach Abschluss der Untersuchung möchten Sie alle Beweise entfernen. 

> [!IMPORTANT]
> Während Sie die verschütteten Daten in ihrer eigenen Organisation dauerhaft entfernen können, können alle Daten, die außerhalb Ihrer Organisation verschüttet werden, mit diesen Funktionen nicht entfernt werden.

## <a name="workflow"></a>Workflow

Im folgenden finden Sie den Workflow für die Verwendung von Daten Untersuchungen (Preview) zum Verwalten eines Ereignisses zur Verschütten von Daten:

1.  Erstellen Sie eine Daten Untersuchung.

2.  Suchen Sie nach vertraulichen, böswilligen oder verlegten Daten, und sammeln Sie Sie als Beweis.

3.  Überprüfen und untersuchen Sie die Beweise.

4.  Löschen Sie die verschütteten Daten endgültig.

5.  Schließen oder löschen Sie die Untersuchung.


## <a name="before-you-begin"></a>Bevor Sie beginnen

- Mit dem Tool zur Datenermittlung (Preview) im Security & Compliance Center können Sie eine Untersuchung durchführen, nach den verschütteten Daten suchen und diese überprüfen und analysieren. Anschließend verwenden Sie die Security & Compliance Center PowerShell, um die verschütteten Daten endgültig aus Office 365 zu löschen. 

- Um eine Untersuchung durchführen zu können, müssen Sie Mitglied der Rollengruppe Compliance Administrator im Security & Compliance Center sein.

- Zum Löschen von Nachrichten müssen Sie Mitglied einer Rollengruppe im Security & Compliance Center sein, dem die Rolle "suchen" und "Löschen" zugewiesen ist. Diese Rolle wird standardmäßig der Rollengruppe "Organisationsverwaltung" zugewiesen. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Permissions in the Security & Compliance Center](../permissions-in-the-security-and-compliance-center.md). 

- Um zu steuern, welche Benutzerpostfächer und OneDrive-Konten ein Prüfer durchsuchen kann, kann Ihre Organisation Compliance-Grenzen einrichten. Weitere Informationen erhalten Sie, indem [Sie Compliance-Grenzen für eDiscovery](../set-up-compliance-boundaries.md)-Untersuchungen einrichten. 

## <a name="step-1-create-a-data-investigation"></a>Schritt 1: Erstellen einer Daten Untersuchung

So erstellen Sie eine Untersuchung im Tool zur Datenanalyse (Vorschau):

1. Wechseln Sie zu [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Compliance Center auf **Daten**Untersuchungen.
 
4. Klicken Sie auf der Seite **Daten Ermittlungen (Vorschau)** auf **neue Untersuchung erstellen**.
    
5. Geben Sie auf der Seite **neue Daten Ermittlungs** Flyout der Untersuchung einen Namen (erforderlich), und geben Sie dann eine optionale unter Suchnummer und eine Beschreibung ein. Beachten Sie, dass der Name in Ihrer Organisation eindeutig sein muss.

6. Führen **Sie unter möchten Sie zusätzliche Einstellungen nach dem Erstellen dieser Untersuchung konfigurieren?** eine der folgenden Aktionen aus:

    - Klicken Sie auf **Ja** , um die Untersuchung zu erstellen, und zeigen Sie die Seite **Einstellungen** im neuen Fall an. Auf diese Weise können Sie der Untersuchung Mitglieder hinzufügen.
    
    - Klicken Sie auf **Nein** , um die Untersuchung nur zu erstellen und in der Liste der Fälle auf der Seite **Daten Ermittlungen (Vorschau)** anzuzeigen. Wenn Sie diese Option auswählen, werden Sie als einziges Mitglied der Untersuchung hinzugefügt, und die Standardeinstellungen für Suche und Analyse werden verwendet. Sie können nach Erstellung der Untersuchung jederzeit Mitglieder hinzufügen oder Einstellungen ändern.

7. Klicken Sie auf **Speichern** , um die Untersuchung zu erstellen.

    Die neue Untersuchung wird in der Liste auf der Seite **Daten Ermittlungen (Vorschau)** angezeigt. 

8. Klicken Sie zum Öffnen einer Untersuchung auf den Namen der Untersuchung. 

    Die Registerkarte **Start** für die Untersuchung wird angezeigt. 

> [!TIP]
> Erstellen Sie eine Benennungskonvention für Untersuchungen, und geben Sie so viele Informationen wie möglich in den Namen und die Beschreibung ein, damit Sie in Zukunft bei Bedarf suchen und auf Sie zugreifen können.
 
## <a name="step-2-search-for-the-spilled-data"></a>Schritt 2: Suchen nach den verschütteten Daten 
 
Wenn Sie wissen, welche Benutzer Sie nach verschütteten Daten durchsuchen möchten, können Sie diese als interessante Personen hinzufügen, um Ihre Datenquellen der Untersuchung zuzuordnen und Ihr Postfach und Ihr OneDrive-Konto schnell zu durchsuchen. Klicken Sie zum Hinzufügen von Personen, die für die Untersuchung interessant sind, auf **interessante**Personen, und klicken Sie dann auf interessante Personen **Hinzufügen**. Weitere Informationen finden Sie unter [Verwalten von Personen mit Interesse](manage-people-of-interest.md).

Auf der Registerkarte **Suchen** können Sie Suchvorgänge erstellen, um die verschütteten Daten zu finden. Sie verwenden dieselbe Suchabfrage, die Sie zum Auffinden der verschütteten Daten verwendet haben, um die gleichen Nachrichten in [Schritt 4](#step-4-delete-the-spilled-data)zu löschen. Weitere Informationen zum Erstellen von Suchvorgängen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md).

Nachdem Sie die Suche ausgeführt haben, können Sie eine Vorschau der Suchergebnisse anzeigen und Suchstatistiken anzeigen, um die Effektivität Ihrer Suchabfrage auszuwerten. Nachdem Sie die Elemente identifiziert haben, die Sie aus Office 365 löschen möchten, können Sie auf die Registerkarte **Beweise** klicken und dann einen Beweissatz erstellen und Suchergebnisse hinzufügen, die diese Elemente enthalten. 

Klicken Sie dazu auf die Suche, die Sie untersuchen möchten. Klicken Sie auf der Seite Flyout auf **Ergebnisse zu Beweismitteln hinzufügen** , und befolgen Sie die Anweisungen. Anschließend können Sie mit dem Nachweis einzelne Dokumente überprüfen, ermitteln, wer Zugriff auf Dokumente hat, und die Dokumente exportieren. Wenn Sie die Dokumente einfach löschen möchten, statt sie zu überprüfen, fahren Sie mit [Schritt 4](#step-4-delete-the-spilled-data)fort. 

> [!IMPORTANT]
> Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, enthalten möglicherweise die tatsächlich verschütteten Daten, die Sie suchen. Wenn Sie beispielsweise nach Dokumenten suchen, die eine Sozialversicherungsnummer enthalten, und Sie Sie als Stichwort in der Suchabfrage verwenden, müssen Sie die Abfrage anschließend löschen, um weiteres auslaufen zu vermeiden. Sie können die Suche löschen oder die gesamte Untersuchung in [Schritt 5](#step-5-close-or-delete-the-investigation)löschen. 

## <a name="step-3-review-and-investigate"></a>Schritt 3: überprüfen und untersuchen 

Wechseln Sie in der Untersuchung zur Registerkarte **Beweise** , und klicken Sie auf den Beweissatz, den Sie im vorherigen Schritt erstellt haben. Nachdem der Verarbeitungsauftrag abgeschlossen wurde und die Suchergebnisse dem Beweis hinzugefügt wurden, können Sie einzelne Dokumente in ihrem systemeigenen Format, im Text Format oder im nahezu systemeigenen Format überprüfen. Sie können zusätzliche Abfragen erstellen, um die Liste der Dokumente einzuschränken und Dokumente zu markieren, um die Ergebnisse ihrer Untersuchung anzugeben. Weitere Informationen finden Sie unter [Überprüfen von Daten in Evidence](review-data-in-evidence.md) .

Klicken Sie auf **Beweise verwalten**, um Dokumente zu gruppieren und weitere Unterstützung für Ihre Überprüfung zu erhalten. Klicken Sie in der **Analyse** Kachel auf **analysieren**. Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt. Weitere Informationen finden Sie unter:

- [Durchführen von Analysen zur schnelleren Untersuchung](run-analytics-to-investigate-faster.md)
- [Erkennen von Quasiduplikaten](near-duplicates.md)
- [E-Mail-Threading](email-threading.md)
- [Designs](themes.md)

Um zu ermitteln, welche Benutzer am Datenüberlauf beteiligt sind, können Sie eine neue Abfrage im Beweissatz erstellen und dann die Bedingungen Absender/Autor und Empfänger verwenden. Dadurch wird eine Liste aller Absender, Empfänger und Autoren erstellt, die in gesammelten Daten gefunden wurden, die dem Nachweis hinzugefügt wurden. Stellen Sie sicher, dass Sie die Liste untersuchen, um festzustellen, ob externe Benutzer vorhanden sind. Weitere Informationen zum Einschränken von Suchergebnissen mithilfe von Bedingungen finden Sie unter [Suchbedingungen](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-delete-the-spilled-data"></a>Schritt 4: Löschen der verschütteten Daten

### <a name="deleting-mailbox-items"></a>Löschen von Postfachelementen

Nachdem Sie überprüft und überprüft haben, dass die Suchergebnisse nur die e-Mail-Nachrichten enthalten, die gelöscht werden müssen, können Sie sie dauerhaft löschen, indem Sie den Befehl **New-ComplianceSearchAction-Purge-purgetype HardDelete** in Security & Compliance ausführen. Center-PowerShell. Anweisungen finden Sie unter [Suchen nach und Löschen von e-Mail-Nachrichten](../search-for-and-delete-messages-in-your-organization.md). 

Wenn die Wiederherstellung einzelner Elemente für Postfächer in Ihrer Organisation aktiviert ist, werden endgültig gelöschte Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers (und für Administratoren zugänglich) aufbewahrt, bis der Aufbewahrungszeitraum für gelöschte Elemente endet (der Standardwert ist 14 Tage). Wenn ein Postfach, das verschüttete Daten enthält, darüber hinaus in einer Aufbewahrungsrichtlinie gespeichert ist oder einer Aufbewahrungsrichtlinie zugewiesen ist, werden bereinigte Nachrichten im Ordner "Wiederherstellbare Elemente" aufbewahrt, bis die Aufbewahrungsdauer für das Element abläuft. Um Nachrichten sofort zu löschen, müssen Sie zusätzliche Aufgaben durchführen. Anweisungen finden Sie unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von cloudbasierten Postfächern in der Warteschleife](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Erkundigen Sie sich bei der Datensatzverwaltung oder den Rechtsabteilungen, bevor Sie eine Aufbewahrungsrichtlinie entfernen. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein aufbewahrtes Postfach oder ein Vorfall mit Datenüberlauf Vorrang hat. 

### <a name="deleting-site-items"></a>Löschen von Websiteelementen

Wenn Sie ein Dokument dauerhaft aus einer SharePoint-Website oder einem OneDrive-Konto löschen möchten, müssen Sie das Dokument löschen und dann aus dem Papierkorb der Website löschen und dann aus dem Papierkorb der Websitesammlung löschen. Weitere Informationen finden Sie unter [Delete Documents in SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Alternativ können Sie eine gesamte Websitesammlung löschen, die möglicherweise verschüttete Daten enthält. Anweisungen finden Sie unter [Löschen einer Websitesammlung](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Schritt 5: schließen oder Löschen der Untersuchung

Nachdem Sie Dokumente in den Quellinhalts Speicherorten (Postfächern oder Websites) im Live-Dienst gelöscht haben, verfügen Sie weiterhin über Kopien dieser Dokumente, die Sie im Rahmen der Untersuchung zum Beweis hinzugefügt haben. Um weitere Datenüberlauf zu vermeiden, sollten Sie das Löschen der Untersuchung selbst in Betracht ziehen.

So löschen Sie eine Untersuchung:

1. Klicken Sie auf der Registerkarte **Einstellungen** auf **Ermittlungsinformationen**.

2. Klicken Sie auf **Untersuchung löschen**. 

Wenn Sie die Untersuchung nicht löschen müssen oder wenn Sie die Informationen speichern möchten, die Sie während der Untersuchung gesammelt haben, können Sie auf **Fall schließen**klicken. Dann können Sie zu einem späteren Zeitpunkt abgeschlossene Untersuchungen erneut öffnen.

---
title: Verwalten eines Daten verschüttenden Vorfalls in Microsoft 365
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
description: In diesem Artikel wird beschrieben, wie Sie mit dem Tool "neue Daten Untersuchungen (Vorschau)" im Security & Compliance Center einen Vorfall mit Datenausfällen verwalten können.
ms.openlocfilehash: 93a98a4e01df011b789ba2453734f093ad8c19d6
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030159"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Verwalten eines Daten verschüttenden Vorfalls in Microsoft 365

Bei Daten verschütten wird ein Dokument mit vertraulichen, vertraulichen oder bösartigen Informationen in einer nicht vertrauenswürdigen Umgebung veröffentlicht. Wenn ein Vorfall mit Daten verschütten erkannt wird, ist es wichtig, schnell die Umgebung zu enthalten, die Größe und die Speicherorte des Ausfalls zu prüfen, die Benutzeraktivitäten zu untersuchen und dann die verschütteten Daten aus dem Dienst zu löschen. Mit dem Tool Daten Untersuchungen (Preview) können Sie nach vertraulichen, böswilligen oder verlegten Daten in Office 365 suchen, um herauszufinden, was passiert ist, und dann entsprechende Aktionen ausführen.  

## <a name="scope-of-this-article"></a>Bereich dieses Artikels

Dieser Artikel enthält eine Liste mit Anweisungen zum endgültigen Löschen von Elementen aus Office 365-Postfächern, damit diese nicht mehr von Benutzern oder Administratoren wiederhergestellt werden können. 

> [!NOTE]
> Wenn Sie Elemente in einer SharePoint-oder OneDrive for Business-Website löschen, werden diese 93 Tage lang aufbewahrt, ab dem Zeitpunkt, zu dem Sie Sie am ursprünglichen Speicherort gelöscht haben.

## <a name="scenario"></a>Szenario

Sie werden über einen Vorfall bei Datenübertragung informiert, bei dem ein Mitarbeiter unwissentlich ein streng vertrauliches Dokument mit mehreren Personen per e-Mail geteilt hat. Sie möchten schnell bewerten, wer dieses Dokument sowohl innerhalb als auch außerhalb Ihrer Organisation erhalten hat. Nachdem Sie den Vorfall untersucht haben, planen Sie, ihre Ergebnisse für andere Prüfer zu überprüfen und die verschütteten Daten dann endgültig aus Office 365 zu entfernen. Nach Abschluss der Untersuchung möchten Sie alle Nachweise entfernen. 

## <a name="workflow"></a>Workflow

Im folgenden finden Sie den Workflow für die Verwendung von Daten Untersuchungen (Preview) zum Verwalten eines Datenausfalls:

1.  Erstellen Sie eine Datenermittlung.

2.  Suchen Sie nach vertraulichen, böswilligen oder verlegten Daten, und sammeln Sie Sie als Beweis.

3.  Überprüfen und untersuchen der Beweise.

4.  Löschen Sie die verschütteten Daten endgültig.

5.  Beenden oder löschen Sie die Untersuchung.


## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie verwenden das Tool Daten Untersuchungen (Vorschau) im Security & Compliance Center, um eine Untersuchung zu erstellen, nach verschütteten Daten zu suchen und diese zu überprüfen und zu analysieren. Anschließend verwenden Sie die Security & Compliance Center PowerShell, um die verschütteten Daten endgültig aus Office 365 zu löschen. 

- Zum Erstellen einer Untersuchung müssen Sie Mitglied der Rollengruppe "Compliance-Administrator" im Security & Compliance Center sein.

- Zum Löschen von Nachrichten müssen Sie Mitglied einer Rollengruppe im Security & Compliance Center sein, dem die Rolle "suchen und löschen" zugewiesen ist. Diese Rolle wird standardmäßig der Rollengruppe "Organisationsverwaltung" zugewiesen. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Permissions in the Security _AMP_ Compliance Center](../permissions-in-the-security-and-compliance-center.md). 

- Um zu steuern, welche Benutzerpostfächer und OneDrive-Konten ein Prüfer durchsuchen kann, kann Ihre Organisation Konformitäts Grenzen einrichten. Um weitere Informationen zu erhalten, [richten Sie Compliance-Grenzen für eDiscovery](../set-up-compliance-boundaries.md)-Untersuchungen ein. 

## <a name="step-1-create-a-data-investigation"></a>Schritt 1: Erstellen einer Datenermittlung

So erstellen Sie eine Untersuchung im Tool für Daten Untersuchungen (Vorschau):

1. Wechseln Sie zu [https://compliance.microsoft.com](https://compliance.microsoft.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Compliance Center auf **Daten Untersuchungen**.
 
4. Klicken Sie auf der Seite **Daten Untersuchungen (Vorschau)** auf **neue Untersuchung erstellen**.
    
5. Geben Sie auf der Seite **Neues Daten Ermittlungs** Flyout der Untersuchung einen Namen (erforderlich) ein, und geben Sie dann eine optionale Untersuchungs Nummer und eine Beschreibung ein. Beachten Sie, dass der Name in Ihrer Organisation eindeutig sein muss.

6. Führen **Sie unter möchten Sie nach dem Erstellen dieser Untersuchung zusätzliche Einstellungen konfigurieren?** eine der folgenden Aktionen aus:

    - Klicken Sie auf **Ja** , um die Untersuchung zu erstellen, und zeigen Sie die Seite **Einstellungen** im neuen Fall an. Dies ermöglicht Ihnen das Hinzufügen von Mitgliedern zur Untersuchung.
    
    - Klicken Sie auf **Nein** , um die Untersuchung zu erstellen und in der Liste der Fälle auf der Seite **Daten Untersuchungen (Vorschau)** anzuzeigen. Wenn Sie diese Option auswählen, werden Sie als einziges Mitglied der Untersuchung hinzugefügt, und die Standardeinstellungen für Suche und Analyse werden verwendet. Sie können jederzeit nach der Erstellung der Untersuchung Mitglieder hinzufügen oder Einstellungen ändern.

7. Klicken Sie auf **Speichern** , um die Untersuchung zu erstellen.

    Die neue Untersuchung wird in der Liste auf der Seite **Daten Untersuchungen (Preview)** angezeigt. 

8. Klicken Sie auf den Namen der Untersuchung, um eine Untersuchung zu öffnen. 

    Die Registerkarte **Start** für die Untersuchung wird angezeigt. 

> [!TIP]
> Erwägen Sie, eine Benennungskonvention für Untersuchungen einzurichten, und geben Sie so viele Informationen wie möglich in den Namen und die Beschreibung ein, damit Sie in Zukunft gegebenenfalls suchen und darauf verweisen können.
 
## <a name="step-2-search-for-the-spilled-data"></a>Schritt 2: Suchen nach verschütteten Daten 
 
Wenn Sie wissen, welche Benutzer Sie nach verschütteten Daten durchsuchen möchten, können Sie diese als interessante Personen hinzufügen, um Ihre Datenquellen der Untersuchung zuzuordnen und Ihr Postfach und Ihr OneDrive-Konto schnell zu durchsuchen. Klicken Sie zum Hinzufügen von Personen, die für die Untersuchung von Interesse sind, auf **Personen**von Interesse, und klicken Sie dann auf **interessante Personen hinzufügen**. Weitere Informationen finden Sie unter [Verwalten von Personen von Interesse](manage-people-of-interest.md).

Auf der Registerkarte **Suchvorgänge** können Sie suchen erstellen, um die verschütteten Daten zu finden. Sie verwenden die gleiche Suchabfrage, die Sie zum Auffinden der verschütteten Daten verwendet haben, um diese Nachrichten in [Schritt 4](#step-4-delete-the-spilled-data)zu löschen. Weitere Informationen zum Erstellen von Suchvorgängen finden Sie unter [Suchen nach Daten in einer Untersuchung](search-for-data.md).

Nachdem Sie die Suche ausgeführt haben, können Sie eine Vorschau der Suchergebnisse anzeigen und Suchstatistiken ansehen, um die Effektivität Ihrer Suchabfrage zu bewerten. Nachdem Sie die Elemente identifiziert haben, die Sie aus Office 365 löschen möchten, können Sie auf die Registerkarte **Evidence** klicken und dann einen Evidence-Satz erstellen und Suchergebnisse hinzufügen, die diese Elemente enthalten. 

Klicken Sie dazu auf die Suche, die Sie untersuchen möchten. Klicken Sie auf der Seite Flyout auf **Ergebnisse zu beweisen hinzufügen** , und folgen Sie den Anweisungen. Anschließend können Sie in den Nachweise einzelne Dokumente überprüfen, den Zugriff auf Dokumente untersuchen und die Dokumente exportieren. Um die Dokumente einfach zu löschen, anstatt Sie zu überprüfen, fahren Sie mit [Schritt 4](#step-4-delete-the-spilled-data)fort. 

> [!IMPORTANT]
> Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, enthalten möglicherweise die tatsächlich verschütteten Daten, nach denen Sie suchen. Wenn Sie beispielsweise nach Dokumenten suchen, die eine Sozialversicherungsnummer enthalten, und Sie in der Suchabfrage als Schlüsselwort verwenden, müssen Sie die Abfrage löschen, um weiteres verschütten zu vermeiden. Sie können die Suche löschen oder die gesamte Untersuchung in [Schritt 5](#step-5-close-or-delete-the-investigation)löschen. 

## <a name="step-3-review-and-investigate"></a>Schritt 3: überprüfen und untersuchen 

Wechseln Sie in der Untersuchung zu **Evidence** , und klicken Sie auf den im vorherigen Schritt erstellten Evidence-Satz. Nachdem der Verarbeitungsauftrag abgeschlossen ist und die Suchergebnisse dem Beweis hinzugefügt wurden, können Sie einzelne Dokumente im nativen Format, im Text Format oder in einem nahezu systemeigenen Format überarbeiten. Sie können zusätzliche Abfragen erstellen, um die Liste der Dokumente einzuschränken und Dokumente zu markieren, um die Ergebnisse ihrer Untersuchung anzugeben. Weitere Informationen finden Sie unter [Überprüfen von Daten in Evidence](review-data-in-evidence.md)

Klicken Sie auf **Beweise verwalten**, um Dokumente zu gruppieren und weitere Unterstützung für Ihre Überprüfungen zu erhalten. Klicken Sie in der **Analytics** -Kachel auf **analysieren**. Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt. Weitere Informationen finden Sie unter:

- [Führen Sie Analysen aus, um schneller zu untersuchen](run-analytics-to-investigate-faster.md)
- [Erkennen von Quasiduplikaten](near-duplicates.md)
- [E-Mail-Threading](email-threading.md)
- [Designs](themes.md)

Um zu ermitteln, welche Benutzer am Datenüberlauf beteiligt sind, können Sie eine neue Abfrage im Beweissatz erstellen und dann die Bedingungen Absender/Autor und Empfänger verwenden. Dadurch wird eine Liste aller Absender, Empfänger und Autoren erstellt, die in gesammelten Daten gefunden wurden, die dem Beweis hinzugefügt wurden. Stellen Sie sicher, dass Sie die Liste überprüfen, um festzustellen, ob externe Benutzer vorhanden sind. Weitere Informationen zur Verwendung von Bedingungen, um Suchergebnisse einzuschränken, finden Sie unter [Suchbedingungen](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-delete-the-spilled-data"></a>Schritt 4: Löschen der verschütteten Daten

### <a name="deleting-mailbox-items"></a>Löschen von Postfachelementen

Nachdem Sie überprüft und überprüft haben, dass die Suchergebnisse nur die e-Mail-Nachrichten enthalten, die gelöscht werden müssen, können Sie sie dauerhaft löschen, indem Sie den Befehl **New-ComplianceSearchAction-Purge-purgeType HardDelete** in Security & Compliance ausführen. Center PowerShell. Anweisungen finden Sie unter [Suchen nach und Löschen von e-Mail-Nachrichten](../search-for-and-delete-messages-in-your-organization.md). 

Wenn die Wiederherstellung einzelner Elemente für Postfächer in Ihrer Organisation aktiviert ist, werden dauerhaft gelöschte Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers gespeichert (und für Administratoren zugänglich), bis der Aufbewahrungszeitraum für gelöschte Elemente endet (der Standardwert beträgt 14 Tage). Wenn jedoch ein Postfach, das verschüttete Daten enthält, über eine gesetzliche Aufbewahrungspflicht verfügt oder einer Beibehaltungsrichtlinie zugewiesen ist, werden bereinigte Nachrichten im Ordner "Wiederherstellbare Elemente" aufbewahrt, bis die Haltedauer für das Element abläuft. Wenn Sie Nachrichten sofort löschen möchten, müssen Sie zusätzliche Aufgaben ausführen. Anweisungen hierzu finden Sie unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von cloudbasierten Postfächern in der Warteschleife](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen einer Aufbewahrungs-oder Archivierungsrichtlinie. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat. 

### <a name="deleting-site-items"></a>Löschen von Websiteelementen

Um ein Dokument dauerhaft aus einem SharePoint-Website-oder OneDrive-Konto zu löschen, müssen Sie das Dokument löschen und dann aus dem Papierkorb der Website löschen und es dann aus dem Papierkorb der Websitesammlung löschen. Weitere Informationen finden Sie unter [Löschen von Dokumenten in SharePoint und OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Alternativ können Sie eine gesamte Websitesammlung löschen, die verschüttete Daten enthalten könnte. Anweisungen finden Sie unter [Löschen einer Websitesammlung](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Schritt 5: beenden oder Löschen der Untersuchung

Nachdem Sie Dokumente in den Quellinhalts Speicherorten (Postfächer oder Websites) im Live-Dienst gelöscht haben, verfügen Sie weiterhin über Kopien dieser Dokumente, die Sie im Rahmen ihrer Untersuchung zu Beweismitteln hinzugefügt haben. Um weitere Daten zu vermeiden, sollten Sie die Untersuchung selbst löschen.

So löschen Sie eine Untersuchung:

1. Klicken Sie auf der Registerkarte **Einstellungen** auf **Ermittlungsinformationen**.

2. Klicken Sie auf **untersuchUng löschen**. 

Wenn Sie die Untersuchung nicht löschen müssen oder wenn Sie die während der Untersuchung gesammelten Informationen speichern möchten, klicken Sie auf **Fall abschließen**. Dann können Sie zu einem späteren Zeitpunkt geschlossene Untersuchungen erneut öffnen.
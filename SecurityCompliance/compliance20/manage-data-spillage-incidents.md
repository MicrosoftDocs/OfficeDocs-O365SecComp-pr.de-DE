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
ms.collection: M365-security-compliance M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: In diesem Artikel wird beschrieben, wie Sie mit dem Tool "neue Daten Untersuchungen (Vorschau)" im Office 365 Security & Compliance Center einen Vorfall mit Datenausfällen verwalten können.
ms.openlocfilehash: 33943ee4367e01f413cfa7840c796d5197323185
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862557"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Verwalten eines Daten verschüttenden Vorfalls in Microsoft 365 

Bei Daten verschütten wird ein vertrauliches Dokument in einer nicht vertrauenswürdigen Umgebung veröffentlicht. Wenn ein Vorfall mit Daten verschütten erkannt wird, ist es wichtig, schnell die Größe und die Speicherorte des Ausfalls zu ermitteln, die Benutzeraktivitäten zu untersuchen und dann die verschütteten Daten dauerhaft aus dem System zu entfernen.

## <a name="scope-of-this-article"></a>Bereich dieses Artikels

Dieser Artikel enthält eine Liste mit Anweisungen zum dauerhaften Entfernen von Elementen aus Office 365-Postfächern, damit diese nicht mehr von Benutzern oder Administratoren wiederhergestellt werden können. 

> [!NOTE]
> Wenn Sie Elemente in einer SharePoint-oder OneDrive for Business-Website löschen, werden diese 93 Tage lang aufbewahrt, ab dem Zeitpunkt, zu dem Sie Sie am ursprünglichen Speicherort gelöscht haben.

## <a name="scenario"></a>Szenario

Sie werden über einen Vorfall bei Datenübertragung informiert, bei dem ein Mitarbeiter unwissentlich ein streng vertrauliches Dokument mit mehreren Personen per e-Mail geteilt hat. Sie möchten schnell bewerten, wer dieses Dokument sowohl innerhalb als auch außerhalb Ihrer Organisation erhalten hat. Nachdem Sie den Vorfall untersucht haben, planen Sie, ihre Ergebnisse für andere Prüfer zu überprüfen und die verschütteten Daten dann endgültig aus Office 365 zu entfernen. Nach Abschluss der Untersuchung möchten Sie alle Nachweise entfernen. 

## <a name="workflow"></a>Workflow

Im folgenden finden Sie den Workflow für die Verwendung von Daten Untersuchungen (Preview) zum Verwalten eines Datenausfalls:

1.  Erstellen Sie eine Datenermittlung.

2.  Suchen Sie nach verschütteten Daten.

3.  Überprüfen und untersuchen des Vorfalls.

4.  Löschen Sie die verschütteten Daten endgültig.

5.  Beenden oder löschen Sie die Untersuchung.


## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie verwenden das Tool Daten Untersuchungen (Vorschau) im Office 365 Security & Compliance Center, um eine Untersuchung zu erstellen, nach verschütteten Daten zu suchen und diese zu überprüfen und zu analysieren. Anschließend verwenden Sie die Security & Compliance Center PowerShell, um die verschütteten Daten endgültig aus Office 365 zu löschen. 

- Zum Erstellen einer Untersuchung müssen Sie Mitglied der Rollengruppe "Compliance-Administrator" im Security & Compliance Center sein.

- Zum Löschen von Nachrichten müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" im Security & Compliance Center sein oder der Rolle "suchen und löschen" zugewiesen sein. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [Gewähren von Benutzern Zugriff auf das Security _AMP_ Compliance Center](../grant-access-to-the-security-and-compliance-center.md). 

- Um zu steuern, welche Benutzerpostfächer und OneDrive-Konten ein Prüfer durchsuchen kann, kann Ihre Organisation Konformitäts Grenzen einrichten. Um weitere Informationen zu erhalten, [richten Sie Compliance-Grenzen für eDiscovery](../set-up-compliance-boundaries.md)-Untersuchungen ein. 

## <a name="step-1-create-a-data-investigation"></a>Schritt 1: Erstellen einer Datenermittlung

So erstellen Sie eine Datenuntersuchung:

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Security & Compliance Center auf **Daten Untersuchungen**.
 
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
 
Wenn Sie wissen, welche Benutzer Sie nach verschütteten Daten durchsuchen möchten, können Sie diese als interessante Personen hinzufügen, um Ihre Datenquellen der Untersuchung zuzuordnen und Ihr Postfach und Ihr OneDrive-Konto schnell zu durchsuchen. Klicken Sie zum Hinzufügen von Personen, die für die Untersuchung von Interesse sind, auf **Personen**von Interesse, und klicken Sie dann auf **interessante Personen hinzufügen**. 

Auf der Registerkarte **Suchvorgänge** können Sie suchen erstellen, um die verschütteten Daten zu finden. Sie verwenden die gleiche Suchabfrage, die Sie zum Auffinden der verschütteten Daten verwendet haben, um diese Nachrichten in [Schritt 4](#step-4-permanently-delete-the-spilled-data)zu löschen. Weitere Informationen zum Erstellen von Suchvorgängen finden Sie unter [Erstellen einer Suche zum Sammeln von Daten](create-search-to-collect-data.md).

Nachdem Sie die Suche ausgeführt haben, können Sie eine Vorschau der Suchergebnisse anzeigen und Suchstatistiken ansehen, um die Effektivität Ihrer Suchabfrage zu bewerten. Nachdem Sie die Elemente identifiziert haben, die Sie aus Office 365 löschen möchten, können Sie auf **** die Registerkarte Incidents klicken und dann einen Vorfall erstellen und Suchergebnisse hinzufügen, die diese Elemente enthalten. 

Klicken Sie dazu auf die Suche, die Sie untersuchen möchten. Klicken Sie auf der Seite Flyout auf **Ergebnisse zu Vorfall hinzufügen** , und folgen Sie den Anweisungen. Dann können Sie im Vorfall einzelne Dokumente überprüfen, den Zugriff auf Dokumente untersuchen und die Dokumente exportieren. Um die Dokumente einfach zu löschen, anstatt Sie zu überprüfen, fahren Sie mit [Schritt 4](#step-4-permanently-delete-the-spilled-data)fort. 

> [!IMPORTANT]
> Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, enthalten möglicherweise die tatsächlich verschütteten Daten, nach denen Sie suchen. Wenn Sie beispielsweise nach Dokumenten suchen, die eine Sozialversicherungsnummer enthalten, und Sie in der Suchabfrage als Schlüsselwort verwenden, müssen Sie die Abfrage löschen, um weiteres verschütten zu vermeiden. Sie können die Suche löschen oder die gesamte Untersuchung in [Schritt 5](#step-5-close-or-delete-the-investigation)löschen. 

## <a name="step-3-review-and-investigate"></a>Schritt 3: überprüfen und untersuchen 

Wechseln Sie in der Untersuchung zur Registerkarte **Incidents** , und klicken Sie auf den Vorfall, den Sie im vorherigen Schritt erstellt haben. Nachdem der Verarbeitungsauftrag abgeschlossen ist und die Suchergebnisse dem Vorfall hinzugefügt wurden, können Sie einzelne Dokumente im systemeigenen Format, im Text Format oder in einem nahezu systemeigenen Format überarbeiten. Sie können zusätzliche Abfragen erstellen, um die Liste der Dokumente weiter einzuschränken und Dokumente zu markieren, um die Ergebnisse ihrer Untersuchung anzugeben.

Klicken Sie auf **Vorfall verwalten**, um Dokumente zu gruppieren und weitere Unterstützung zu erhalten. Klicken Sie in der **Analytics** -Kachel auf **analysieren**. Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt. Weitere Informationen finden Sie unter:

- [Erkennen von Quasiduplikaten](near-duplicates.md)
- [E-Mail-Threading](email-threading.md)
- [Designs](themes.md)

Um zu ermitteln, welche Benutzer am Datenüberlauf beteiligt sind, können Sie eine neue Abfrage im Vorfall erstellen und dann die Bedingungen Absender/Autor und Empfänger verwenden. Dadurch wird eine Liste aller Absender, Empfänger und Autoren erstellt, die in gesammelten Daten gefunden wurden, die dem Vorfall hinzugefügt wurden. Überprüfen Sie unbedingt die Liste, um festzustellen, ob externe Benutzer in der Liste vorhanden sind. Weitere Informationen finden Sie unter [Suchbedingungen](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-permanently-delete-the-spilled-data"></a>Schritt 4: Dauerhaftes Löschen der verschütteten Daten

### <a name="deleting-mailbox-items"></a>Löschen von Postfachelementen

Nachdem Sie überprüft und überprüft haben, dass die Suchergebnisse nur die e-Mail-Nachrichten enthalten, die gelöscht werden müssen, können Sie sie dauerhaft löschen, indem Sie den Befehl **New-ComplianceSearchAction-Purge-purgeType HardDelete** in Security & Compliance ausführen. Center PowerShell. Anweisungen finden Sie unter [Suchen nach und Löschen von e-Mail-Nachrichten](../search-for-and-delete-messages-in-your-organization.md). 

Beachten Sie, dass, wenn die Wiederherstellung einzelner Elemente für Postfächer in Ihrer Organisation aktiviert ist, dauerhaft gelöschte Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers aufbewahrt werden (und von Administratoren zugänglich sind), bis der Aufbewahrungszeitraum für gelöschte Elemente endet (Standard ist 14 Tage). Wenn eines der Postfächer, die verschüttete Daten enthalten, über eine gesetzliche Aufbewahrungspflicht verfügt oder einer Beibehaltungsrichtlinie zugewiesen ist, wird die bereinigte Nachricht weiterhin im Ordner "Wiederherstellbare Elemente" aufbewahrt, bis die Aufbewahrung entfernt oder das Postfach nicht mehr in den Speicherrichtlinien eingeschlossen ist. Wenn Sie Nachrichten sofort löschen möchten, müssen Sie zusätzliche Aufgaben ausführen. Anweisungen hierzu finden Sie unter [Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von cloudbasierten Postfächern in der Warteschleife ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen einer Aufbewahrungs-oder Archivierungsrichtlinie. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat. 

### <a name="deleting-site-items"></a>Löschen von Websiteelementen

Um ein Dokument dauerhaft aus einer SharePoint-Website oder einem OneDrive for Business-Konto zu löschen, müssen Sie es löschen und es dann aus dem Papierkorb der Websitesammlung löschen. Anweisungen hierzu finden Sie unter [Löschen von Dokumenten in SharePoint und OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Alternativ können Sie eine gesamte Websitesammlung löschen, die verschüttete Daten enthalten könnte. Anweisungen finden Sie unter [Löschen einer Websitesammlung](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Schritt 5: beenden oder Löschen der Untersuchung

Nachdem Sie Dokumente in den Quellinhalts Speicherorten (Postfächer oder Websites) gelöscht haben, verfügen Sie weiterhin über Kopien dieser Dokumente, die Sie bei der Untersuchung Vorfällen hinzugefügt haben. Um weitere Daten zu vermeiden, sollten Sie die Untersuchung löschen.

So löschen Sie eine Untersuchung:

1. Klicken Sie auf der Registerkarte **Einstellungen** auf **Ermittlungsinformationen**.

2. Klicken Sie auf **Fall löschen**. 

Wenn Sie die Untersuchung nicht löschen müssen oder wenn Sie die während der Untersuchung gesammelten Informationen speichern möchten, klicken Sie auf **Fall abschließen**. Zu einem späteren Zeitpunkt können geschlossene Untersuchungen erneut geöffnet werden.
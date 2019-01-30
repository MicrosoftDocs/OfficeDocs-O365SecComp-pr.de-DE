---
title: Verwalten von einem Daten stellen Vorfall in Microsoft 365
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
description: In diesem Artikel wird beschrieben, mit dem neuen Daten-Untersuchungen (Preview)-Tool in der Office 365-Sicherheit & Compliance Center zum Verwalten von eines Daten stellen Vorfalls.
ms.openlocfilehash: d863d87cc667b9695f9bf619c35575715dfa144e
ms.sourcegitcommit: 98ec28932ae20e848f9f489c3c78e4a7edab6d18
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "29636622"
---
# <a name="managing-a-data-spillage-incident-in-microsoft-365"></a>Verwalten von einem Daten stellen Vorfall in Microsoft 365 

Daten stellen ist, wenn ein vertrauliches Dokument in einer nicht vertrauenswürdigen Umgebung freigegeben ist. Wenn ein Daten stellen Vorfall erkannt wird, ist es wichtig, schnell Bewerten der Größe und Standorte von der Stellen, untersuchen Sie die Benutzeraktivitäten herum und verschütteten Daten dann dauerhaft aus dem System löschen.

## <a name="scope-of-this-article"></a>Themenbereich dieses Artikels

Dieser Artikel enthält eine Liste von Anweisungen zum Entfernen von Elementen dauerhaft in Office 365-Postfächer, sodass sie nicht mehr verfügbar oder durch Benutzer oder Administratoren wiederhergestellt werden. 

> [!NOTE]
> Beim Löschen von Elementen in einem SharePoint oder OneDrive for Business-Site befinden werden für 93 Tagen ab dem Zeitpunkt beibehalten, die Sie sie aus dem ursprünglichen Speicherort löschen.

## <a name="scenario"></a>Szenario

Sie haben eine Daten stellen Vorfall darüber informiert, in dem ein Mitarbeiter unwissentlich ein streng vertraulich Dokument mit mehreren Personen per e-Mail gemeinsam genutzt. Möchten Sie schnell bewerten, die dieses Dokument, sowohl innerhalb als auch außerhalb Ihrer Organisation empfangen. Nachdem Sie haben den Vorfall untersuchen, Planen Sie Ihre Ergebnisse mit anderen Prüfer, um zu prüfen, und entfernen Sie die verschütteten Daten endgültig aus Office 365 freigeben. Nach Abschluss die Untersuchung möchten Sie alle Spuren entfernen. 

## <a name="workflow"></a>Workflow

Hier wird der Workflow für die Verwendung von Daten Untersuchungen (Preview) einen Daten stellen Vorfall verwalten:

1.  Erstellen Sie eine Untersuchung von Daten.

2.  Suchen Sie nach der verschütteten Daten.

3.  Überprüfen Sie und untersuchen Sie des Vorfalls.

4.  Löschen Sie die verschütteten Daten endgültig.

5.  Schließen oder die Untersuchung löschen.


## <a name="before-you-begin"></a>Bevor Sie beginnen:

- Verwenden Sie das Tool Daten Untersuchungen (Preview) in die Sicherheit in Office 365 Compliance Center & eine Untersuchung erstellen, suchen Sie nach der verschütteten Daten, und überprüfen und analysieren. Sicherheit & Compliance Center PowerShell verwenden Sie dann die verschütteten Daten aus Office 365 endgültig löschen. 

- Um eine Untersuchung zu erstellen, müssen Sie Mitglied der Rollengruppe in der & Security Compliance Center Compliance-Administrator sein.

- Um Nachrichten zu löschen, müssen Sie Mitglied der Rollengruppe "Organisationsverwaltung" in der & Security Compliance Center oder die Rolle suchen und löschen. Informationen zum Hinzufügen von Benutzern zu einer Rollengruppe finden Sie unter [gewähren Sie Benutzerzugriff auf die Sicherheit & Compliance Center](../grant-access-to-the-security-and-compliance-center.md). 

- Um zu steuern, welche Benutzerpostfächer und OneDrive-Konten ein Prüfer suchen kann, kann Compliance-Grenzen Ihrer Organisation einrichten. Weitere Informationen, [Compliance-Grenzen für eDiscovery Untersuchungen einrichten](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Schritt 1: Erstellen einer Untersuchung von Daten

So erstellen Sie eine Untersuchung von Daten:

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie in der & Security Compliance Center auf **Daten Untersuchungen**.
 
4. Klicken Sie auf **Erstellen einer neuen Untersuchung**, auf der Seite **Daten Untersuchungen (Preview)** .
    
5. Benennen Sie auf der Seite **neue Daten Untersuchung** flyoutmenü der Untersuchung (erforderlich), und geben Sie eine Nummer optional Untersuchung und eine Beschreibung ein. Beachten Sie, dass der Name muss in Ihrer Organisation eindeutig sein.

6. Klicken Sie unter **möchten Sie zusätzliche Einstellungen konfigurieren, nach dem Erstellen dieser Untersuchung?**, eine der folgenden Aktionen aus:

    - Klicken Sie auf **Ja,** um die Untersuchung zu erstellen und Anzeigen der Seite **Einstellungen** in der neuen Groß-/Kleinschreibung. Dadurch können Sie die Untersuchung Mitglieder hinzu.
    
    - Klicken Sie auf **Nein** , um nur die Untersuchung erstellen und anzeigen in der Liste der Anfragen auf der Seite **Daten Untersuchungen (Preview)** . Wenn Sie diese Option auswählen, werden Sie hinzugefügt werden, wie das einzige Mitglied die Untersuchung und die Standardeinstellungen für Suche und-Analyse verwendet wird. Sie können Mitglieder hinzufügen oder ändern, jederzeit nach die Untersuchung erstellt wird.

7. Klicken Sie auf **Speichern** , um die Untersuchung zu erstellen.

    Die neue Untersuchung wird in der Liste auf der Seite **Daten Untersuchungen (Preview)** angezeigt. 

8. Um eine Untersuchung zu öffnen, klicken Sie auf den Namen der Untersuchung. 

    Für die Untersuchung die Registerkarte **Start** wird angezeigt. 

> [!TIP]
> Berücksichtigen Sie festlegen einer Namenskonvention für Untersuchungen, und geben Sie so viele Informationen wie können Sie in den Namen und die Beschreibung, sodass Sie suchen und finden Sie in der Zukunft bei Bedarf.
 
## <a name="step-2-search-for-the-spilled-data"></a>Schritt 2:-Suche für die verschütteten Daten 
 
Wenn Sie die Benutzer verschütteten Daten suchen möchten kennen, können Sie sie als Personen von Interesse zum Zuordnen von deren Datenquellen für die Untersuchung und schnelles Suchen, deren Postfach und OneDrive-Konto hinzufügen. Um die Untersuchung interessante Menschen hinzuzufügen, klicken Sie auf **Personen von Interesse**, und klicken Sie dann auf **Hinzufügen von Personen von Interesse**. 

Klicken Sie auf der Registerkarte **Suchen** können Sie einer Suche zum Suchen Sie die verschütteten Daten erstellen. Sie werden die gleichen Suchabfrage verwenden, die Sie verwendet verschütteten So löschen Sie die gleichen Nachrichten in [Schritt 4](##step-4:-permanently-delete-the-spilled-data)zu finden. Weitere Informationen zum Erstellen von sucht finden Sie unter [Erstellen einer Suche zum Sammeln von Daten](create-search-to-collect-data.md).

Nach dem Ausführen die Suche können Sie eine Vorschau anzeigen Beispiele für Suchergebnisse und Ansicht Suchstatistik für die Effektivität der Suchabfrage ausgewertet werden soll. Nachdem Sie die Elemente zu, die Sie aus Office 365 löschen möchten identifizieren, können Suchergebnisse, die diese Elemente enthalten Sie klicken Sie auf der Registerkarte **Vorfälle** und klicken Sie dann einen Vorfall erstellen und hinzufügen. 

Klicken Sie hierzu auf die Suche, die Sie untersuchen möchten. Klicken Sie auf der Seite flyoutmenü klicken Sie auf **Add Ergebnisse auf Vorfall** , und befolgen Sie die Anweisungen. Klicken Sie dann in den Vorfall können Sie einzelne Dokumente zu überprüfen, untersuchen, die Zugriff auf Dokumente hatte, und exportieren die Dokumente. Um die Dokumente anstelle von hierfür, einfach zu löschen, fahren Sie mit [Schritt 4](##step-4:-permanently-delete-the-spilled-data). 

> [!IMPORTANT]
> Die Schlüsselwörter, die Sie in der Suchabfrage verwenden, können die tatsächlichen verschütteten Daten enthalten, denen Sie suchen. Wenn Sie die Suche nach Dokumenten mit einer Sozialversicherungsnummer und Sie als ein Schlüsselwort in der Suchabfrage verwenden, müssen Sie die Abfrage anschließend zur Vermeidung von weiteren stellen löschen. Sie können löschen suchen oder die gesamte Untersuchung in [Schritt 5](##step-5:-close-or-delete-investigation). 

## <a name="step-3-review-and-investigate"></a>Schritt 3: Überprüfen und untersuchen 

In der Untersuchung wechseln Sie zur Registerkarte **Vorfälle** , und klicken Sie auf der Vorfall, den Sie im vorherigen Schritt erstellt haben. Nach der Verarbeitung der Auftrag abgeschlossen ist, und die Suchergebnisse des Vorfalls hinzugefügt werden, können Sie einzelne Dokumente im systemeigenen Format, Text-Format oder ein in der Nähe systemeigenen Format überprüfen. Sie können zusätzliche Abfragen zur weiteren Einschränkung der Liste von Dokumenten und Kennzeichnen von Dokumenten an, dass die Ergebnisse aus der Prüfung erstellen.

Klicken Sie zum Gruppieren von Dokumenten, und erhalten Sie weitere Unterstützung für die Überprüfung, auf **Vorfall verwalten**. Klicken Sie in die Kachel **Analytics** auf **Analysieren**. Dadurch wird die erweiterte Analytics wie Erkennung von Duplikaten, e-Mail-threading und Design Analyse ausgeführt. Weitere Informationen finden Sie unter:

- [Erkennung von Duplikaten in Ihrer Nähe.](near-duplicates.md)
- [Threading-e-Mail](email-threading.md)
- [Designs](themes.md)

Um zu bestimmen, welche Benutzer an die Daten stellen beteiligt sind, können Sie Erstellen einer neuen Abfrage in der Vorfall und verwenden Sie die/Author Absender und Empfänger Bedingungen. Dadurch wird eine Liste aller Absender, Empfänger und Autoren gefunden in gesammelten Daten, die den Vorfall hinzugefügt wurde, erstellt. Achten Sie darauf, untersuchen Sie die Liste, um festzustellen, ob externe Benutzer in der Liste vorhanden sind. Weitere Informationen finden Sie unter [Search Conditions](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-permanently-delete-the-spilled-data"></a>Schritt 4: Die verschütteten Daten endgültig löschen

### <a name="deleting-mailbox-items"></a>Löschen von postfachelementen

Nachdem Sie überprüfen, und überprüfen Sie, ob die Suchergebnisse nur die e-Mail-Nachrichten enthalten, die gelöscht werden müssen, Sie dauerhaft löschen durch Ausführen der **New-ComplianceSearchAction-löschen - PurgeType HardDelete** Command in Security & Compliance Center PowerShell. Anweisungen finden Sie unter [Suchen und Löschen von e-Mail-Nachrichten](../search-for-and-delete-messages-in-your-organization.md). 

Beachten Sie, die Wiederherstellung einzelner Elemente für Postfächer in Ihrer Organisation aktiviert ist dauerhaft Objekte gelöschte werden in den Ordner des Benutzers wiederherstellbare Elemente aufbewahrt werden (und von Administratoren verfügbar) bis gelöschter Elemente Aufbewahrung Ende der (Standardeinstellung ist 14 Tage). Darüber hinaus der Postfächer, die verschütteten Daten enthalten sind, eine rechtliche Aufbewahrungspflicht oder eine Aufbewahrungsrichtlinie zugewiesen, wird Zeitfenster Nachricht beibehalten werden im Ordner "wiederherstellbare Elemente", bis die Sperre entfernt wurde, oder das Postfach von Aufbewahrungsrichtlinien ausgeschlossen wird. Auf der Festplatte löschen von Nachrichten müssen Sie sofort Addition Aufgaben ausführen. Anweisungen finden Sie unter [Löschen von Elementen im Ordner des cloudbasierten Postfächer auf halten wiederherstellbaren Elementen ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Mit der datensatzverwaltung oder der rechtlichen Abteilungen vor dem Entfernen einer Richtlinie halten oder die Aufbewahrung prüfen. Ihrer Organisation möglicherweise eine Richtlinie, die definiert, ob ein Postfach auf halten, oder ein Daten stellen Vorfall Vorrang. 

### <a name="deleting-site-items"></a>Löschen von Website-Elementen

Zum dauerhaft löschen eines Dokuments aus einer SharePoint-Website oder OneDrive for Business-Konto, haben Sie von der Website löschen, und löschen Sie ihn aus der Websitesammlung Papierkorb und Sie haben, ihn zu löschen. Anweisungen finden Sie unter [Löschen von Dokumenten in SharePoint und OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Alternativ können Sie eine komplette Websitesammlung, der verschütteten Daten enthalten möglicherweise löschen. Anweisungen finden Sie unter [Löschen einer Websitesammlung](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Schritt 5: Schließen Sie oder löschen Sie die Untersuchung

Nachdem Sie Dokumente in der quellspeicherorte für Inhalte (Postfächer oder Websites) zu löschen, müssen Sie dennoch Kopien dieser Dokumente, die im Rahmen Ihrer Untersuchung Vorfälle hinzugefügt. Um weitere stellen Daten zu vermeiden, sollten Sie die Untersuchung löschen.

So löschen Sie eine Untersuchung:

1. Klicken Sie auf der Registerkarte **Einstellungen** auf **Untersuchung Informationen**.
2. Klicken Sie auf die **Anfrage zu löschen**. 

Wenn Sie nicht die Untersuchung löschen müssen oder speichern Sie die Informationen, die Sie bei der Untersuchung erfasst werden sollen, können Sie den **Fall schließen**klicken. Zu einem späteren Zeitpunkt können Sie geschlossene Untersuchungen erneut öffnen.
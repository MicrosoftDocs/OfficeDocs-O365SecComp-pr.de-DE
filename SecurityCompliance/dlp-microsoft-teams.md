---
title: Schutz vor Datenverlust und Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/26/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Sie können jetzt DLP-Richtlinien auf Microsoft Teams-Chats und-Kanäle anwenden. Lesen Sie diesen Artikel, um mehr über die Funktionsweise zu erfahren.
ms.openlocfilehash: 712729972942d98afb5b3898ad357114ce1a6bae
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "33367244"
---
# <a name="data-loss-prevention-and-microsoft-teams"></a>Schutz vor Datenverlust und Microsoft Teams

## <a name="overview-of-dlp-for-microsoft-teams"></a>Übersicht über DLP für Microsoft Teams

Vor kurzem wurden die DLP-Funktionen ( [Data Loss Prevention](data-loss-prevention-policies.md) ) auf Microsoft Teams ausgedehnt. Wenn Ihre Organisation DLP besitzt, können Sie jetzt Richtlinien definieren, die verhindern, dass Personen vertrauliche Informationen in einem Microsoft Teams-Kanal oder einer Chatsitzung freigeben. Hier einige Beispiele für die Funktionsweise dieses Schutzes:

- **Beispiel 1: Schützen vertraulicher Informationen in Nachrichten**. Angenommen, jemand versucht, vertrauliche Informationen in einem Teams-Chat oder-Kanal mit Gästen (externe Benutzer) zu teilen. Wenn Sie eine DLP-Richtlinie definiert haben, um dies zu verhindern, werden Nachrichten mit vertraulichen Informationen, die an externe Benutzer gesendet werden, gelöscht. Dies geschieht automatisch und innerhalb von Sekunden, je nachdem, wie ihre DLP-Richtlinie konfiguriert ist.

- **Beispiel 2: Schützen vertraulicher Informationen in Dokumenten**. Angenommen, jemand versucht, ein Dokument mit Gästen in einem Microsoft Teams-Kanal oder-Chat freizugeben, und das Dokument enthält vertrauliche Informationen. Wenn Sie eine DLP-Richtlinie definiert haben, um dies zu verhindern, wird das Dokument für diese Benutzer nicht geöffnet. Beachten Sie, dass in diesem Fall ihre DLP-Richtlinie SharePoint und OneDrive aufweisen muss, damit Schutz vorhanden ist.

## <a name="policy-tips-help-educate-users"></a>Richtlinien Tipps helfen bei der Schulung von Benutzern

Ähnlich wie DLP in [Exchange, Outlook und Outlook im Web](data-loss-prevention-policies.md#policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web), [SharePoint-und OneDrive for Business-Websites](data-loss-prevention-policies.md#policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites)und Office- [Desktop Clients](data-loss-prevention-policies.md#policy-evaluation-in-the-office-desktop-programs), werden Richtlinien Tipps angezeigt, wenn eine Aktion mit einer DLP-Richtlinie in Konflikt steht. Hier sehen Sie ein Beispiel für einen richtlinientipp:

![Benachrichtigung über blockierte Nachrichten in Teams](media/dlp-teams-blockedmessage-notification.png)

In diesem Fall hat der Absender versucht, eine Sozialversicherungsnummer in einem Microsoft Teams-Kanal freizugeben. **Was kann ich tun?** Link öffnet ein Dialogfeld, das Optionen für den Absender zur Lösung des Problems bereitstellt. Beachten Sie, dass in diesem Fall der Absender sich entscheiden kann, die Richtlinie zu überschreiben, oder einen Administrator benachrichtigen, dass er Sie überarbeiten und beheben muss.

![Optionen zum Auflösen blockierter Nachrichten](media/dlp-teams-blockedmessage-possibleactions.png)

In Ihrer Organisation können Sie auswählen, ob Benutzer eine DLP-Richtlinie außer Kraft setzen dürfen oder nicht. Und wenn Sie Ihre DLP-Richtlinien konfigurieren, können Sie die Standardrichtlinien Tipps verwenden oder [Richtlinien Tipps](#to-customize-policy-tips) für Ihre Organisation anpassen. 

Zurück zu unserem Beispiel, in dem ein Absender eine Sozialversicherungsnummer in einem Teams-Kanal freigegeben hat:

![Nachricht blockiert](media/dlp-teams-blockedmessage-notification-to-user.png)

The **What es this?** Link öffnet einen [Artikel](data-loss-prevention-policies.md) über DLP-Richtlinien, der erläutert, warum die Nachricht blockiert wurde.

### <a name="to-customize-policy-tips"></a>So passen Sie Richtlinien Tipps an

Um diese Aufgabe ausführen zu können, muss Ihnen eine Rolle zugewiesen sein, die über Berechtigungen zum Bearbeiten von DLP-Richtlinien verfügt. Weitere Informationen finden Sie unter [Permissions](data-loss-prevention-policies.md#permissions).

1. Wechseln Sie zum Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), und melden Sie sich an.

2. Wählen Sie > **Richtlinie**zur Verhinderung von **Datenverlust**. 

3. Wählen Sie eine Richtlinie aus, und wählen Sie neben **Richtlinieneinstellungen**die Option **Bearbeiten**aus.

4. Erstellen Sie entweder eine neue Regel, oder bearbeiten Sie eine vorhandene Regel für die Richtlinie.<br/>![Bearbeiten einer Regel für eine Richtlinie](media/dlp-teams-editrule.png)<br/>

5. Wählen Sie auf der Registerkarte **Benutzer Benachrichtigungen** die Option **e-Mail-Text anpassen** und/oder **die richtlinientipp-Textoptionen anpassen** aus.<br/>![Anpassen von Benutzer Benachrichtigungen und Richtlinien Tipps](media/dlp-teams-editrule-usernotifications.png)<br/>  

6. Geben Sie den Text an, der für e-Mail-Benachrichtigungen und/oder Richtlinien Tipps verwendet werden soll, und klicken Sie dann auf **Speichern**. 

7. Klicken Sie auf der Registerkarte **Richtlinieneinstellungen** auf **Speichern**.

Lassen Sie ungefähr eine Stunde dauern, bis sich Ihre Änderungen im Rechenzentrum durchlaufen haben, und synchronisieren Sie mit Benutzerkonten.
 
## <a name="add-microsoft-teams-as-a-location-to-existing-dlp-policies"></a>Hinzufügen von Microsoft Teams als Standort zu vorhandenen DLP-Richtlinien

Um diese Aufgabe ausführen zu können, muss Ihnen eine Rolle zugewiesen sein, die über Berechtigungen zum Bearbeiten von DLP-Richtlinien verfügt. Weitere Informationen finden Sie unter [Permissions](data-loss-prevention-policies.md#permissions).

1. Wechseln Sie zum Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), und melden Sie sich an.

2. Wählen Sie > **Richtlinie**zur Verhinderung von **Datenverlust**. 

3. Wählen Sie eine Richtlinie aus, und überprüfen Sie die Werte unter **Speicherorte**. Wenn Sie **Teams Chat und Channel-Nachrichten**sehen, sind Sie vollständig eingestellt. Klicken Sie andernfalls auf **Bearbeiten**.<br/>![Standorte für vorhandene Richtlinie](media/dlp-teams-editexistingpolicy.png)<br/>

4. Aktivieren Sie in der Spalte **Status** die Richtlinie für **Teams-Chat-und Kanal Nachrichten**.<br/>![DLP für Teams-Chats und-Kanäle](media/dlp-teams-addteamschatschannels.png)<br/>

5. Behalten Sie die Standardeinstellungen für alle Konten bei, oder geben Sie an, welche Konten hinzugefügt oder ausgeschlossen werden sollen.

6. Klicken Sie auf **Speichern**.

Lassen Sie ungefähr eine Stunde dauern, bis sich Ihre Änderungen im Rechenzentrum durchlaufen haben, und synchronisieren Sie mit Benutzerkonten.

## <a name="define-a-new-dlp-policy-for-microsoft-teams"></a>Definieren einer neuen DLP-Richtlinie für Microsoft Teams

Um diese Aufgabe ausführen zu können, muss Ihnen eine Rolle zugewiesen sein, die über Berechtigungen zum Bearbeiten von DLP-Richtlinien verfügt. Weitere Informationen finden Sie unter [Permissions](data-loss-prevention-policies.md#permissions).

1. Wechseln Sie zum Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), und melden Sie sich an.

2. Wählen Sie **Data Loss Prevention** > **Policy** > **+ Create a Policy**aus. 

3. Wählen Sie eine [Vorlage](data-loss-prevention-policies.md#dlp-policy-templates)aus, und klicken Sie dann auf **weiter**.<br/>In unserem Beispiel haben wir die US-amerikanische personenbezogene Informationsdaten Vorlage ausgewählt.<br/>![Datenschutz Vorlage für DLP-Richtlinie](media/dlp-teams-createnewpolicy-template.png)<br/>

4. Geben Sie auf der Registerkarte **Richtlinie benennen** einen Namen und eine Beschreibung für die Richtlinie ein, und klicken Sie dann auf **weiter**. 

5. Behalten Sie auf der Registerkarte **Speicherorte auswählen** die Standardeinstellung für alle Standorte bei, oder wählen Sie **bestimmte Speicher**Orte auswählen, und klicken Sie dann auf **weiter**.<br/>Wenn Sie bestimmte Standorte ausgewählt haben, wählen Sie die Speicherorte für ihre DLP-Richtlinie aus, und wählen Sie dann **weiter**aus.<br/>![DLP-Richtlinienspeicher Orte](media/dlp-teams-selectlocationsnewpolicy.png)<br/>
    > [!NOTE]
    > Wenn Sie sicherstellen möchten, dass Dokumente, die vertrauliche Informationen enthalten, nicht ungeeignet freigegeben werden, stellen Sie sicher, dass **SharePoint-Websites** und **OneDrive-Konten** zusammen mit **Teams-Chat-und Kanal Nachrichten**aktiviert sind.
<br/>

6. Behalten Sie auf der Registerkarte **Richtlinieneinstellungen** unter **Anpassen des zu schützenden Inhaltstyps**die standardmäßigen einfachen Einstellungen bei, oder wählen Sie **Erweiterte Einstellungen verwenden**aus, und klicken Sie dann auf **weiter**. Wenn Sie erweiterte Einstellungen auswählen, können Sie Regeln für die Richtlinie erstellen oder bearbeiten. (Weitere Informationen hierzu finden Sie unter [einfache Einstellungen im Vergleich zu erweiterten Einstellungen](data-loss-prevention-policies.md#simple-settings-vs-advanced-settings).)

7.  Überprüfen Sie auf der Registerkarte **Richtlinieneinstellungen** unter **Was möchten Sie tun, wenn vertrauliche Informationen ermittelt werden?** die Einstellungen. (Hier können Sie die Standard [Richtlinien Tipps und e-Mail-Benachrichtigungen](use-notifications-and-policy-tips.md)beibehalten oder anpassen.)<br/>![DLP-Richtlinieneinstellungen mit Tipps und Benachrichtigungen](media/dlp-teams-policysettings-tipsemails.png)<br/>Wenn Sie die Überprüfung oder Bearbeitung der Einstellungen abgeschlossen haben, klicken Sie auf **weiter**.

8. Wählen Sie auf der Registerkarte **Richtlinieneinstellungen** unter möchten **Sie die Richtlinie aktivieren oder die Dinge zuerst testen?** aus, ob die Richtlinie aktiviert, [zuerst getestet](data-loss-prevention-policies.md#roll-out-dlp-policies-gradually-with-test-mode)oder deaktiviert bleiben soll, und wählen Sie dann **weiter**aus.<br/>![Angeben, ob die Richtlinie aktiviert werden soll](media/dlp-teams-policysettings-turnonnow.png)<br/>

9. Überarbeiten Sie auf der Registerkarte **Überprüfungen** der Einstellungen die Einstellungen für die neue Richtlinie. Wählen Sie **Bearbeiten** aus, um Änderungen vorzunehmen. Wenn Sie fertig sind, wählen Sie **Erstellen**aus. 

Lassen Sie ungefähr eine Stunde zu, bis sich Ihre neue Richtlinie durch Ihr Rechenzentrum und mit Benutzerkonten synchronisiert.

## <a name="related-articles"></a>Verwandte Artikel

[Erstellen, Testen und Optimieren einer DLP-Richtlinie](create-test-tune-dlp-policy.md)

[Senden von E-Mail-Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien](use-notifications-and-policy-tips.md)

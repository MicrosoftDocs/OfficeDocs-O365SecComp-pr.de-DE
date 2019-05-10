---
title: Kunden-Lockbox-Anfragen in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
search.appverid:
- BCS160
- MET150
- MOE150
description: Erfahren Sie mehr über Kunden-Lockbox-Anfragen, mit denen Sie steuern können, wie ein Microsoft-Supporttechniker auf Ihre Daten zugreifen kann, wenn Sie ein Problem ausführen.
ms.openlocfilehash: 3a86f3333114f3015b85d8066298f9834737f127
ms.sourcegitcommit: 000548aa269ad775f20af5acd6aa726ac340c793
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "33661421"
---
# <a name="customer-lockbox-in-office-365"></a>Kunden-Lockbox in Office 365

> [!NOTE]
> Dieser Artikel bietet Bereitstellungs-und Konfigurationsanleitungen für ein Feature, das derzeit nur für Organisationen mit Microsoft 365 E5, Office 365 E5, Information Protection and Compliance oder Advanced Compliance-Add-on-Abonnement zur Verfügung steht.

Kunden-Lockbox stellt sicher, dass Microsoft nicht auf Ihre Inhalte zugreifen kann, um einen Dienstvorgang ohne Ihre ausdrückliche Genehmigung durchzuführen. Kunden-Lockbox bringt Sie zum Genehmigungsworkflow für Anforderungen für den Zugriff auf Ihre Inhalte.

Gelegentlich helfen Microsoft-Ingenieure bei der Problembehandlung und bei der Behebung von Kunden gemeldeten Problemen im Support Prozess. In der Regel werden Probleme durch umfangreiche Telemetrie-und Debugging-Tools behoben, die Microsoft für seine Dienste eingerichtet hat. In einigen Fällen muss ein Microsoft-Techniker jedoch auf Kunden Inhalte zugreifen, um die Ursache zu ermitteln und das Problem zu beheben. Kunden-Lockbox erfordert, dass der Techniker den Zugriff vom Kunden als letzten Schritt im Genehmigungsworkflow anfordert. Auf diese Weise können Organisationen diese Anforderungen genehmigen oder verweigern und dem Kunden eine direkte Zugriffssteuerung bieten.

### <a name="customer-lockbox-overview-video"></a>Kunden-Lockbox-Übersichtsvideo

> [!VIDEO https://www.microsoft.com/videoplayer/embed/8fecf10b-1f03-4849-8b67-76d3d2a43f26?autoplay=false]

> [!NOTE]
> Kunden-Lockbox unterstützt Anforderungen für den Zugriff auf Daten in Exchange Online, SharePoint Online und OneDrive for Business. Wenn Sie die Unterstützung für andere Office 365-Dienste empfehlen möchten, senden Sie eine Anfrage an [Office 365 UserVoice](https://office365.uservoice.com/).

## <a name="customer-lockbox-workflow"></a>Kunden-Lockbox-Workflow

Die folgenden Schritte beschreiben den typischen Workflow, wenn eine Kunden-Lockbox-Anforderung von einem Microsoft-Techniker initiiert wird:

1. Jemand in einer Organisation hat ein Problem mit seinem Office 365-Postfach.

2. Nachdem der Benutzer das Problem behoben, aber nicht beheben kann, wird eine Supportanfrage beim Microsoft-Support geöffnet.

3. Ein Supporttechniker prüft die Serviceanfrage und legt fest, dass der Zugriff auf die Exchange Online-Inhalte des Kunden erforderlich ist, um das Problem zu beheben.

4. Der Supporttechniker meldet sich beim Kunden-Lockbox-Anforderungs Tool an und führt eine Datenzugriffsanforderung aus, indem er den Mandantennamen, die Dienstanforderungsnummer des Kunden und die geschätzte Dauer angibt, für die der Zugriff auf die Daten erforderlich ist.

5. Nachdem ein Microsoft Support Manager die Anforderung genehmigt hat, sendet die Kunden-Lockbox die designierte genehmigende Person in der Organisation des Kunden eine e-Mail-Benachrichtigung über die ausstehende Zugriffsanforderung von Microsoft.

    ![Beispiel einer Kunden-Lockbox-e-Mail-Benachrichtigung](media/CustomerLockbox1.png)

   > [!NOTE]
   > Jeder, der die Rolle " [Kunden](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) -Lockbox-Administrator" im Microsoft 365 Admin Center zugewiesen ist, kann Kunden-Lockbox-Anfragen genehmigen.

7. Die genehmigende Person meldet sich beim Microsoft 365 Admin Center an und genehmigt die Anforderung. Dieser Schritt löst die Erstellung eines Überwachungsdatensatzes aus, der durch Durchsuchen des Office 365-Überwachungsprotokolls verfügbar ist. Weitere Informationen finden Sie im Abschnitt [Auditing Customer Lockbox](#auditing-customer-lockbox-requests) Requests.

   Wenn der Kunde die Anforderung ablehnt oder die Anforderung nicht innerhalb von 12 Stunden genehmigt wurde, läuft die Anforderung ab, und dem Microsoft-Techniker wird kein Zugriff erteilt.

   > [!IMPORTANT]
   > Microsoft enthält keine Links in Kunden-Lockbox-e-Mail-Benachrichtigungen, in denen Sie sich bei Office 365 anmelden müssen.

8. Nachdem der Kunde die Anforderung genehmigt hat, erhält der Microsoft-Techniker die Genehmigungsnachricht, meldet sich bei Exchange Online an und behebt das Problem des Kunden. Microsoft-Techniker haben die angeforderte Dauer, um das Problem zu beheben, nach dem der Zugriff automatisch widerrufen wird.

> [!NOTE]
> Alle von einem Microsoft-Techniker ausgeführten Aktionen werden im Office 365-Überwachungsprotokoll protokolliert. Sie können nach diesen Überwachungsdatensätzen suchen und diese überprüfen, und Sie können nach und überprüft werden.

## <a name="turn-customer-lockbox-requests-on-or-off"></a>Aktivieren oder Deaktivieren von Kunden-Lockbox-Anfragen

Ein Office 365-Administrator kann Kunden-Lockbox-Steuerelemente im Microsoft 365 Admin Center aktivieren. Wenn die Lockbox des Kunden aktiviert ist, muss Microsoft die Genehmigung einer Organisation erhalten, bevor auf Inhalte zugegriffen wird.

> [!NOTE]
> Um das folgende Verfahren ausführen zu können, müssen Sie ein globaler Administrator in Ihrer Microsoft 365-oder Office 365-Organisation sein, oder die Rolle " **kundensperre für den Zugriff auf genehmigende Person** " wird zugewiesen.

1. Wechseln Sie [https://admin.microsoft.com](https://admin.microsoft.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.

2. Klicken Sie auf **Einstellungen > Sicherheit & Datenschutz**.

    ![Bearbeiten der Einstellungen für Kunden-Lockbox im Admin Center](media/CustomerLockbox2.png)

3. Klicken Sie auf der Kachel des **Kunden** -Lockbox auf **Bearbeiten**und dann auf **ein** oder **aus** , um das Feature zu aktivieren oder zu deaktivieren.

    ![Require approval for Customer Lockbox](media/CustomerLockbox4.png)

## <a name="approve-or-deny-a-customer-lockbox-request"></a>Genehmigen oder Verweigern einer Kunden-Lockbox-Anfrage

> [!NOTE]
> Um das folgende Verfahren ausführen zu können, müssen Sie ein globaler Administrator in Ihrer Microsoft 365-oder Office 365-Organisation sein, oder die Rolle " **kundensperre für den Zugriff auf genehmigende Person** " wird zugewiesen.

1. Wechseln Sie [https://admin.microsoft.com](https://admin.microsoft.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.

2. Klicken Sie auf **> Kunden-Lockbox-Anfragen unterstützen**.

    ![Klicken Sie auf Support, und klicken Sie dann auf Kunden-Lockbox-Anfragen](media/CustomerLockbox5.png)

    Eine Liste von Kunden-Lockbox-Anfragen wird angezeigt.

    ![Liste der Kunden-Lockbox-Anfragen](media/CustomerLockbox6.png)

3. Wählen Sie eine Kunden-Lockbox-Anforderung aus **** , und klicken Sie dann auf genehmigen oder **verweigern**.

    ![Genehmigen oder Verweigern von Kunden-Lockbox-Anfragen](media/CustomerLockbox7.png)

    Es wird eine Bestätigungsmeldung zur Genehmigung der Kunden-Lockbox-Anfrage angezeigt.

    ![Genehmigen oder Verweigern von Kunden-Lockbox-Anfragen](media/CustomerLockbox8.png)

## <a name="auditing-customer-lockbox-requests"></a>Überwachen von Kunden-Lockbox-Anfragen 

Überwachungsdatensätze, die den Kunden-Lockbox-Anforderungen entsprechen, werden im Office 365-Überwachungsprotokoll protokolliert und können mithilfe des [Überwachungsprotokoll-Such Tools](https://docs.microsoft.com/office365/securitycompliance/search-the-audit-log-in-security-and-compliance) im Office 365 Security & Compliance Center aufgerufen werden. Aktionen im Zusammenhang mit einem Kunden, der eine Kunden-Lockbox-Anforderung akzeptiert oder ablehnt, und von Microsoft-Ingenieuren durchgeführte Aktionen (wenn Zugriffsanforderungen genehmigt werden) werden im Office 365-Überwachungsprotokoll protokolliert. Sie können diese Überwachungsdatensätze suchen und überprüfen.

> [!NOTE]
> Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" verfügen, um das Office 365-Überwachungsprotokoll durchsuchen zu können. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls im Office 365 Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/search-the-audit-log-in-security-and-compliance#before-you-begin).

### <a name="search-the-audit-log-for-activity-related-to-customer-lockbox-requests"></a>Durchsuchen des Überwachungsprotokolls nach Aktivitäten im Zusammenhang mit Kunden-Lockbox-Anfragen

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage erstellen, um Überwachungsdatensätze für Kunden-Lockbox zurückzugeben:

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
  
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.

3. Klicken Sie im linken Bereich des Security & Compliance Centers auf **Search & Investigation** > **Audit Log Search**.

    Die Seite **Überwachungsprotokoll Suche** wird angezeigt.

    ![Überwachungsprotokoll Suche (Seite)](media/auditlogsearch1.png)
  
4. Konfigurieren Sie die folgenden Suchkriterien:

    a. **Aktivitäten** – lassen Sie dieses Feld leer, damit die Suche Überwachungsdatensätze für alle Aktivitäten zurückgibt. Dies ist erforderlich, um Überwachungsdatensätze zurückzugeben, die sich auf Kunden Lockbox-Anfragen und entsprechende Aktivitäten beziehen, die von Microsoft-Ingenieuren ausgeführt werden.

    b. **Start** -und **Enddatum** – wählen Sie einen Datums-und Uhrzeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind.

    c. **Benutzer** – lassen Sie dieses Feld leer.

    d. **Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

5. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 

    Die Suchergebnisse werden geladen, und nach ein paar Augenblicken werden Sie unter **Ergebnisse** auf der Such Seite des **Überwachungsprotokolls** angezeigt.

6. Klicken Sie auf der Suchergebnisseite auf **Ergebnisse filtern** , und führen Sie eine der folgenden Aktionen aus:

   - Zum Anzeigen von Überwachungsdatensätzen im Zusammenhang mit einer genehmigenden Person in Ihrer Organisation, die eine Kunden-Lockbox-Anforderung genehmigt oder ablehnt: Geben Sie im Feld unter der Spalte **Aktivität** den Namen **Set-AccessToCustomerDataRequest**ein.

   - Zum Anzeigen von Überwachungsdatensätzen im Zusammenhang mit einem Microsoft-Techniker, der als Reaktion auf eine genehmigte Kunden-Lockbox-Anforderung Aktionen ausführt: Geben Sie im Feld unter der Spalte **Benutzer** den Namen **Microsoft-Operator**ein. Beachten Sie, dass die vom Techniker ausgeführte Aktion in der Spalte **Activity** angezeigt wird.

      ![Filter für "Microsoft-Operator" zum Anzeigen von Überwachungsdatensätzen](media/CustomerLockbox10.png)

7. Klicken Sie in der Ergebnisliste auf einen Überwachungsdatensatz, um ihn anzuzeigen.

### <a name="audit-record-for-a-customer-lockbox-access-request"></a>Überwachungsdatensatz für eine Kunden-Lockbox-Zugriffsanforderung

Wenn eine Person in Ihrer Organisation eine Kunden-Lockbox-Anfrage genehmigt oder ablehnt, wird im Office 365-Überwachungsprotokoll ein Überwachungsdatensatz protokolliert. Dieser Datensatz enthält die folgenden Informationen. 

| Überwachungsdatensatz Eigenschaft| Beschreibung|
|:---------- |:----------|
| Datum       | Datum und Uhrzeit der Genehmigung oder Ablehnung der Kunden-Lockbox-Anforderung.
| IP-Adresse | Die IP-Adresse des Computers, den die genehmigende Person verwendet hat, um eine Anforderung zu genehmigen oder abzulehnen. |
| Benutzer       | Das Dienstkonto BOXServiceAccount @\[customerforest\]. Prod.Outlook.com.            |
| Aktivität   | Set-AccessToCustomerDataRequest; Dies ist die Überwachungsaktivität, die protokolliert wird, wenn Sie eine Kunden-Lockbox-Anforderung genehmigen oder verweigern.                                |
| Element       | Die GUID der Kunden-Lockbox-Anforderung                             |

Der folgende Screenshot zeigt ein Beispiel für einen Überwachungsprotokolleintrag, der einer genehmigten Kunden-Lockbox-Anforderung entspricht. Wenn eine Kunden-Lockbox-Anforderung abgelehnt wurde, wäre der Wert des **ApprovalDecision** -Parameters **Deny**.

![Überwachungsdatensatz für eine genehmigte Kunden-Lockbox-Anforderung](media/CustomerLockbox9.png)

> [!TIP]
> Klicken Sie auf **Weitere Informationen**, um detailliertere Informationen in einem Überwachungsdatensatz anzuzeigen.

### <a name="audit-record-for-an-action-performed-by-a-microsoft-engineer"></a>Überwachungsdatensatz für eine von einem Microsoft-Techniker ausgeführte Aktion

Wie bereits erläutert, werden die Aktionen, die von einem Microsoft-Techniker ausgeführt werden, nachdem eine Kunden-Lockbox-Anforderung genehmigt wurde (und die zum Zugriff auf Kunden Inhalte führen kann), im Überwachungsprotokoll protokolliert. Diese Einträge enthalten die folgenden Informationen.

| Überwachungsdatensatz Eigenschaft| Beschreibung|
|:---------- |:----------|
| Datum       | Datum, an dem die Aktion ausgeführt wurde. Beachten Sie, dass der Zeitpunkt, zu dem diese Aktion ausgeführt wurde, innerhalb von 4 Stunden nach der Genehmigung der Kunden-Lockbox-Anforderung liegt.              |
| IP-Adresse | Die IP-Adresse des Computers, den Microsoft-Techniker verwendet hat. |
| Benutzer       | Microsoft-Operator; Dieser Wert gibt an, dass dieser Datensatz mit einer Kunden-Lockbox-Anfrage verbunden ist.                                  |
| Aktivität   | Name der vom Microsoft-Techniker ausgeführten Aktivität.|
| Element       | \<leere\>                                             |


## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

#### <a name="which-office-365-services-does-customer-lockbox-apply-to"></a>Auf welche Office 365-Dienste wird die Kunden-Lockbox angewendet?

Kunden-Lockbox wird derzeit in Exchange Online, SharePoint Online und OneDrive for Business unterstützt.

#### <a name="is-customer-lockbox-available-to-all-office-365-customers"></a>Ist die Kunden-Lockbox für alle Office 365-Kunden verfügbar?

Kunden-Lockbox ist in den Microsoft 365-oder Office 365 E5-Abonnements enthalten und kann anderen Plänen mit einem Informationsschutz und einer Compliance oder einem erweiterten Compliance-Add-on-Abonnement hinzugefügt werden. Weitere Informationen finden Sie unter [Pläne und Preise](https://products.office.com/business/office-365-enterprise-e5-business-software) .

#### <a name="what-is-customer-content"></a>Was ist Kunden Inhalt?

Kunden Inhalte sind die Daten, die von Benutzern von Office 365-Diensten und-Anwendungen erstellt werden. Beispiele für Kunden Inhalte:

- E-Mail-Text oder e-Mail-Anlagen

- Inhalte der SharePoint-Website

- Informationen im Textkörper einer SharePoint-Datei

- Skype for Business-Präsentationsdatei

- Sofortnachrichten oder sprach Unterhaltungen

- Vom kundengenerierte BLOB-oder strukturierte Speicherdaten (beispielsweise SQL-Container)

- Sicherheitsinformationen im Kundenbesitz (beispielsweise Zertifikate, Verschlüsselungsschlüssel und Kennwörter)

- Rückschlüsse und alle nachfolgenden Rückschlüsse, wenn der Kunden Inhalt bleibt

Weitere Informationen zu Kundeninhalten in Office 365 finden Sie im [Office 365 Trust Center](https://products.office.com/en-US/business/office-365-trust-center-privacy/).

#### <a name="who-is-notified-when-there-is-a-request-to-access-my-content"></a>Wer wird benachrichtigt, wenn eine Anforderung für den Zugriff auf meine Inhalte besteht?

Globale Administratoren und alle Personen, denen die Administratorrolle "Kunden-Lockbox-Zugriff Genehmiger" zugewiesen ist, werden benachrichtigt. Dies sind auch die gleichen Benutzer, die für Kunden-Lockbox-Anfragen genehmigen können.

#### <a name="who-can-approve-or-reject-these-requests-in-my-organization"></a>Wer kann diese Anforderungen in meiner Organisation genehmigen oder ablehnen?

Globale Administratoren und alle Personen, denen die Administratorrolle "Kunden-Lockbox-Zugriff Genehmiger" zugewiesen ist, können Kunden-Lockbox-Anfragen genehmigen. Kunden steuern diese Rollenzuweisungen in ihren Organisationen.

#### <a name="how-do-i-opt-in-to-customer-lockbox"></a>Wie aktiviere ich eine Kunden-Lockbox?

Ein globaler Administrator kann die Lockbox für Kunden in Microsoft 365 oder Microsoft 365 Admin Center aktivieren und konfigurieren.

#### <a name="if-i-approve-a-customer-lockbox-request-what-can-the-engineer-do-and-how-will-i-know-what-the-microsoft-engineer-did"></a>Wenn ich eine Kunden-Lockbox-Anfrage genehmige, was kann der Techniker tun und wie erfahre ich, was der Microsoft-Techniker getan hat?

Nachdem Sie eine Kunden-Lockbox-Anfrage genehmigt haben, hat der Microsoft-Techniker diese erforderlichen Berechtigungen für den Zugriff auf Kunden Inhalte mithilfe von vorab genehmigten Cmdlets erteilt. Von Microsoft-Ingenieuren als Reaktion auf Kunden Lockbox-Anfragen ausgeführte Aktionen werden im Überwachungsprotokoll im Office 365 Security & Compliance Center protokolliert und können darauf zugreifen.

#### <a name="how-do-i-know-that-microsoft-follows-the-approval-process"></a>Woran erkenne ich, dass Microsoft den Genehmigungsprozess befolgt?

Sie können die e-Mail-Genehmigungsbenachrichtigungen, die an Administratoren und genehmigende Personen in Ihrer Organisation gesendet werden, mit dem Kunden-Lockbox-Anforderungsverlauf im Microsoft 365 Admin Center quer referenzieren.

Kunden-Lockbox ist im aktuellen [SOC 1 SSAE 16-Überwachungsbericht](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports)enthalten. Weitere Informationen finden Sie im [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports).

#### <a name="can-microsoft-modify-the-list-of-approvers-for-my-tenant-if-not-how-is-it-prevented"></a>Kann Microsoft die Liste der genehmigenden Personen für meinen Mandanten ändern? Wenn nicht, wie wird es verhindert?

Nur ein globaler Administrator in Ihrer Organisation kann angeben, wer Kunden-Lockbox-Anfragen genehmigen kann. Das heisst, dass nur die Mitglieder der globalen Administratorgruppe in Azure Active Directory angeben können, wer die Anforderung genehmigen kann. Die Mitgliedschaft in der globalen Administratorgruppe in Azure Active Directory wird nur von Ihrer Organisation verwaltet.

#### <a name="what-if-i-need-more-information-about-a-content-access-request-to-approve-it"></a>Was geschieht, wenn ich weitere Informationen zu einer Inhalts Zugriffsanforderung benötige, um Sie zu genehmigen?

Jede Kunden-Lockbox-Anforderung enthält eine Office 365-Dienstanforderungsnummer. Sie können sich an den Microsoft-Support wenden und auf diese Dienstnummer verweisen, um weitere Informationen zur Anforderung zu erhalten.

#### <a name="when-a-customer-lockbox-request-is-approved-how-long-are-the-permissions-valid"></a>Wie lange sind die Berechtigungen gültig, wenn eine Kunden-Lockbox-Anforderung genehmigt wird?

Derzeit beträgt der maximale Zeitraum für die dem Microsoft-Techniker erteilten Zugriffsberechtigungen 4 Stunden. Der Microsoft-Techniker kann auch einen kürzeren Zeitraum anfordern.

#### <a name="how-can-i-get-a-history-of-all-customer-lockbox-requests"></a>Wie kann ich einen Verlauf aller Kunden-Lockbox-Anfragen erhalten?

Alle Kunden-Lockbox-Anfragen werden im Microsoft 365 Admin Center angezeigt.

#### <a name="how-do-i-correlate-the-content-access-requests-with-the-related-audit-logs"></a>Wie kann ich die Inhalts Zugriffsanforderungen mit den zugehörigen Überwachungsprotokollen korrelieren?

Der Compliance Center-Aktivitäts Feed enthält die Log-Aktivitäten der Kunden-Lockbox. Kunden können die Kunden-Lockbox-Protokoll Aktivitäten über den Aktivitätsfeed für die e-Mail-Anforderung, die Sie erhalten, Querverweisen.

#### <a name="what-happens-when-a-customer-doesnt-respond-to-a-customer-lockbox-request"></a>Was geschieht, wenn ein Kunde nicht auf eine Kunden-Lockbox-Anfrage antwortet?

Kunden-Lockbox-Anfragen haben eine Standarddauer von 12 Stunden. Wenn Sie innerhalb von 12 Stunden keine Antwort auf eine Anforderung senden, läuft die Anforderung ab.

#### <a name="what-does-microsoft-when-a-customer-rejects-a-customer-lockbox-request"></a>Was bewirkt Microsoft, wenn ein Kunde eine Kunden-Lockbox-Anfrage ablehnt?

Wenn ein Kunde eine Kunden-Lockbox-Anfrage ablehnt, tritt kein Zugriff auf Kunden Inhalte auf. Wenn ein Benutzer in Ihrer Organisation weiterhin ein Dienst Problem auftritt, aufgrund dessen Microsoft Zugriff auf Kunden Inhalte benötigt, um das Problem zu beheben, kann das Problem weiterhin auftreten, und Microsoft wird den Benutzer darüber informieren.

#### <a name="does-customer-lockbox-protect-against-data-requests-from-law-enforcement-agencies-or-other-third-parties"></a>Schützt die Kunden-Lockbox gegen Daten Anfragen von Strafverfolgungsbehörden oder anderen Drittanbietern?

Nein. Microsoft übernimmt Drittanbieter Anforderungen für Kundendaten ernst. Als Cloud-Dienstanbieter befürwortet Microsoft stets den Schutz von Kundendaten. Für den Fall, dass eine Vorladung vorliegt, versucht Microsoft immer, den Drittanbieter an den Kunden weiterzuleiten, um die Informationen zu erhalten. (Lesen Sie den Blog von Brad Smith: [Schützen von Kundendaten vor der Regierung Snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen in regelmäßigen Abständen [detaillierte Informationen](https://www.microsoft.com/en-us/corporate-responsibility/lerr) zu den von Microsoft empfangenen Strafverfolgungs Anforderungen.

Weitere Informationen finden Sie im [Microsoft Trust Center](https://www.microsoft.com/en-us/trustcenter/default.aspx) in Bezug auf Datenanforderungen von Drittanbietern und den Abschnitt "Offenlegung von Kundendaten" in den [Online Diensten](https://www.microsoft.com/Licensing/product-licensing/products.aspx) .

#### <a name="how-does-microsoft-ensure-that-a-member-of-its-staff-doesnt-have-standing-access-to-customer-content-in-office-365-applications"></a>Wie stellt Microsoft sicher, dass ein Mitglied seiner Mitarbeiter keinen ständigen Zugriff auf Kunden Inhalte in Office 365-Anwendungen hat?

Microsoft implementiert umfangreiche vorbeugende Maßnahmen durch Zugangskontrollsysteme und ermittelte Maßnahmen, um zu erkennen und zu versuchen, diese Zugriffs Steuerungssysteme zu umgehen. Office 365 arbeitet mit den Prinzipien der geringsten Rechte und des Just-in-Time-Zugriffs. Daher haben keine Microsoft-Mitarbeiter die Berechtigung, ständig auf Kunden Inhalte zuzugreifen. Wenn die Berechtigung erteilt wird, ist Sie für eine begrenzte Dauer. 

Office 365 verwendet ein Zugriffs Steuerungssystem namens *Lockbox* , um Anforderungen für Berechtigungen zu verarbeiten, die das Ausführen von Betriebs-und Verwaltungsfunktionen innerhalb des Diensts ermöglichen. Ein Operator muss den Zugriff auf Kunden Inhalte mit Lockbox anfordern, was dann erforderlich ist, wenn eine zweite Person eine Aktion für die Anforderung (beispielsweise genehmigen) durchführen muss, bevor der Zugriff erteilt wird. Diese zweite Person kann nicht der Anforderer sein und muss als Genehmigung für den Zugriff auf Kunden Inhalte festgelegt werden. Nur wenn die Anforderung genehmigt ist, erhält der Operator temporären Zugriff auf Kunden Inhalte. Nachdem der elevations Zeitraum abgelaufen ist, sperrt Lockbox den Zugriff.

Weitere Informationen zu allgemeinen Sicherheits Vorgehensweisen von Microsoft finden Sie in den [Online-Dienstbedingungen](https://www.microsoft.com/licensing/product-licensing/products) .

#### <a name="under-what-circumstances-do-microsoft-engineers-need-access-to-my-content"></a>Unter welchen Umständen benötigen Microsoft-Techniker Zugriff auf meine Inhalte?

Das häufigste Szenario, in dem Microsoft-Techniker auf Kunden Inhalte zugreifen müssen, ist, wenn der Kunde eine Supportanforderung stellt, die Zugriff für die Problembehandlung erfordert. Ein grundlegendes Prinzip von Office 365 ist, dass der Dienst ohne Microsoft-Zugriff auf Kunden Inhalte funktioniert. Fast alle von Microsoft durchgeführten Dienstvorgänge sind vollständig automatisiert, und die menschliche Einbindung wird in hohem Maße von Kundeninhalten gesteuert und abstrahiert. Das Ziel für Office 365 ist der Zugriff auf Kunden Inhalte zur Unterstützung des Diensts wird erst dann benötigt, wenn der Kunde eine bestimmte Anforderung für Microsoft Access genehmigt.

#### <a name="i-already-thought-my-data-was-secure-with-the-microsoft-cloud-so-why-do-i-need-customer-lockbox"></a>Ich habe bereits gedacht, dass meine Daten mit der Microsoft-Cloud sicher waren, Warum benötige ich dann Kunden-Lockbox?

Kunden-Lockbox bietet eine zusätzliche Steuerungsebene, da Kunden die Möglichkeit bieten, explizite Zugriffsautorisierung für Dienstvorgänge zu erteilen. Durch die Veranschaulichung, dass Verfahren für die explizite Datenzugriffs Autorisierung vorhanden sind, hilft Kunden Lockbox auch Kunden bei der Erfüllung bestimmter Compliance-Verpflichtungen wie HIPAA und FEDRAMP.

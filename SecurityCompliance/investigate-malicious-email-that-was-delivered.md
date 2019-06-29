---
title: Suchen und untersuchen schädlicher e-Mails, die zugestellt wurden (Office 365 Untersuchung und Reaktion auf Bedrohungen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie mithilfe von Bedrohungs Ermittlungs-und-Antwortfunktionen böswillige e-Mails suchen und untersuchen.
ms.openlocfilehash: 5f8c615bed07b75cd3c06ec48f5ba73586f0f6d5
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394290"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>Suchen und untersuchen schädlicher e-Mails, die zugestellt wurden (Office 365 Advanced Threat Protection-Plan 2)

[Office 365 Advanced Threat Protection](office-365-atp.md) können Sie Aktivitäten untersuchen, die Ihre Benutzer gefährden und Maßnahmen zum Schutz Ihrer Organisation ergreifen. Wenn Sie beispielsweise Teil des Sicherheitsteams Ihrer Organisation sind, können Sie nach verdächtigen e-Mail-Nachrichten suchen und diese untersuchen, die Ihren Benutzern zugestellt wurden. Sie können dies mithilfe von [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md)durchführen.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:
  
- Ihre Organisation verfügt über [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 oder Plan 2) und [Lizenzen werden Benutzern zugewiesen](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- [Office 365 Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Organisation aktiviert. 
    
- Ihre Organisation verfügt über Richtlinien, die für Antispam-, Antischadsoftware-und Anti-Phishing-Maßnahmen und so weiter definiert sind. Weitere Informationen finden Sie unter [Protect Against Threats in Office 365](protect-against-threats.md).
    
- Sie sind ein Office 365 globaler Administrator oder haben dem Security &amp; Compliance Center entweder den Sicherheitsadministrator oder die Such-und Säuberungs Rolle zugewiesen. Siehe [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Umgang mit verdächtigen e-Mails

Böswillige Angreifer senden möglicherweise e-Mails an Ihre Benutzer, um zu versuchen, Ihre Anmeldeinformationen zu Phishing und Zugriff auf Ihre Unternehmensgeheimnisse zu erhalten. Um dies zu verhindern, sollten Sie die Threat Protection-Dienste in Office 365 verwenden, einschließlich [Exchange Online Protection](eop/exchange-online-protection-overview.md) und [Advanced Threat Protection](office-365-atp.md). Es gibt jedoch Situationen, in denen ein Angreifer e-Mails an Benutzer senden kann, die eine URL enthalten, und diese URL erst später auf böswilligen Inhalt (Schadsoftware usw.) verweist. Alternativ erkennen Sie möglicherweise zu spät, dass ein Benutzer in Ihrer Organisation kompromittiert wurde, und während dieser Benutzer kompromittiert wurde, hat ein Angreifer dieses Konto verwendet, um e-Mails an andere Benutzer in Ihrem Unternehmen zu senden. Im Rahmen der Bereinigung beider Szenarien möchten Sie möglicherweise e-Mail-Nachrichten von Benutzer Posteingängen entfernen. In solchen Situationen können Sie [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md) nutzen, um diese e-Mail-Nachrichten zu suchen und zu entfernen.

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a>Wo nach dem Ausführen von Aktionen erneut weitergeleitete e-Mails abgelegt werden

Threat Explorer bei der Echtzeiterkennung wurden die Felder Zustellungs Aktion und Zustellungs Speicherort an der Stelle des Zustellungs Status hinzugefügt. Dadurch wird ein vollständigeres Bild davon erzielt, wo Ihre e-Mails landen. Ein Teil des Ziels dieser Änderung besteht darin, die Suche für Sicherheitsleute einfacher zu machen, aber das Ergebnis ist, dass der Speicherort der Problem-e-Mails auf einen Blick zu erkennen ist.

Der Zustellungs Status wird nun in zwei Spalten aufgeteilt:

- **Zustellungs Aktion** – wie lautet der Status dieser e-Mail?
- **Zustellungs Speicherort** – wohin wurde diese e-Mail weitergeleitet?

Zustellungs Aktion ist die Aktion, die aufgrund vorhandener Richtlinien oder Erkennungen auf eine e-Mail angewendet wird. Hier sind die möglichen Aktionen, die eine e-Mail ausführen kann:

1. **Zugestellt** – e-Mails wurden im Posteingang oder Ordner eines Benutzers zugestellt, und der Benutzer kann direkt darauf zugreifen.
2. **Junked** – e-Mails wurden entweder an den Junk-Ordner des Benutzers oder den Ordner "gelöscht" gesendet, und der Benutzer hat Zugriff auf e-Mails in seinem Junk-oder Deleted-Ordner.
3. **Blockiert** – alle e-Mails, die unter Quarantäne gestellt werden, die fehlgeschlagen sind oder gelöscht wurden. Auf diesen Zugriff kann der Benutzer vollständig zugreifen!
4. **Ersetzt** – jede e-Mail-Nachricht, bei der böswillige Anlagen durch txt-Dateien ersetzt werden, in denen der Anhang als böswillig bezeichnet wird.
 
Der Übermittlungsort zeigt die Ergebnisse von Richtlinien und Erkennungen an, die nach der Zustellung ausgeführt werden. Sie ist mit einer Zustellungs Aktion verknüpft. Dieses Feld wurde hinzugefügt, um Einblicke in die Aktion zu geben, die ausgeführt wird, wenn ein Problem mit e-Mails gefunden wird. Im folgenden sind die möglichen Werte für den Zustellungs Speicherort zu finden:

1. **Posteingang oder Ordner** – die e-Mail befindet sich im Posteingang oder in einem Ordner (entsprechend Ihren e-Mail-Regeln).
2. **On-Prem oder External** – das Postfach ist nicht in der Cloud vorhanden, sondern lokal.
3. **Junk-Ordner** – die e-Mail im Ordner Junk eines Benutzers.
4. **Ordner "Gelöschte Elemente"** – die e-Mail im Ordner "Gelöschte Elemente" eines Benutzers.
5. **Quarantine** – die e-Mail-Nachricht in Quarantäne und befindet sich nicht im Postfach eines Benutzers.
6. **Fehler** – die e-Mail konnte das Postfach nicht erreichen.
7. **Fallen gelassen** – die e-Mail wird irgendwo in der Nachrichtenübermittlung verloren.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Suchen und löschen verdächtiger e-Mails, die zugestellt wurden

> [!TIP]
> Threat Explorer (manchmal auch als Explorer bezeichnet) ist ein leistungsfähiger Bericht, der mehrere Zwecke wie das Suchen und Löschen von Nachrichten, das Identifizieren der IP-Adresse eines böswilligen e-Mail-Absenders oder das Starten eines Vorfalls zur weiteren Untersuchung dienen kann. Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mails aus Empfängerpostfächern.

So zeigen Sie die Änderungen am früheren Feld "Zustellungs Status" an (jetzt Zustellungs Aktion und Zustellungs Speicherort): 

1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. Dadurch gelangen Sie zum Security &amp; Compliance Center. 
    
2. Klicken Sie im linken Navigationsbereich auf **Threat Management** \> **Explorer**.

![Screenshot des Bedrohungs-Explorers.](media/Threat Explorer Delivery Action and Delivery Location.PNG)

<!--Comment>
    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection-Plan 2](office-365-ti.md)
  
[Schutz vor Bedrohungen in Office 365](protect-against-threats.md)
  
[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
  


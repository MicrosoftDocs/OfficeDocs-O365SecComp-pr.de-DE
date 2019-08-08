---
title: Suchen und untersuchen schädlicher e-Mails, die in Office 365 bereitgestellt wurden
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 08/07/2019
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
ms.openlocfilehash: 1f558614d77577408a824b3c6181aae22753ab0f
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230559"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-in-office-365"></a>Suchen und untersuchen schädlicher e-Mails, die in Office 365 bereitgestellt wurden

[Office 365 Advanced Threat Protection](office-365-atp.md) ermöglicht es Ihnen, Aktivitäten zu untersuchen, die Ihre Benutzer gefährden und Maßnahmen zum Schutz Ihrer Organisation ergreifen. Wenn Sie beispielsweise Teil des Sicherheitsteams Ihrer Organisation sind, können Sie nach verdächtigen e-Mail-Nachrichten suchen und diese untersuchen, die Ihren Benutzern zugestellt wurden. Sie können dies mithilfe von [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md)durchführen.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:
  
- Ihre Organisation verfügt über [Office 365 erweiterte Bedrohungsschutz](office-365-atp.md) und [Lizenzen werden Benutzern zugewiesen](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
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

- **Zugestellt** – e-Mails wurden im Posteingang oder Ordner eines Benutzers zugestellt, und der Benutzer kann direkt darauf zugreifen.
- **Junked** – e-Mails wurden entweder an den Junk-Ordner des Benutzers oder den Ordner "gelöscht" gesendet, und der Benutzer hat Zugriff auf e-Mails in seinem Junk-oder Deleted-Ordner.
- **Blockiert** – alle e-Mails, die unter Quarantäne gestellt werden, die fehlgeschlagen sind oder gelöscht wurden. Auf diesen Zugriff kann der Benutzer vollständig zugreifen!
- **Ersetzt** – jede e-Mail-Nachricht, bei der böswillige Anlagen durch txt-Dateien ersetzt werden, in denen der Anhang als böswillig bezeichnet wird.
 
Der Übermittlungsort zeigt die Ergebnisse von Richtlinien und Erkennungen an, die nach der Zustellung ausgeführt werden. Sie ist mit einer Zustellungs Aktion verknüpft. Dieses Feld wurde hinzugefügt, um Einblicke in die Aktion zu geben, die ausgeführt wird, wenn ein Problem mit e-Mails gefunden wird. Im folgenden sind die möglichen Werte für den Zustellungs Speicherort zu finden:

- **Posteingang oder Ordner** – die e-Mail befindet sich im Posteingang oder in einem Ordner (entsprechend Ihren e-Mail-Regeln).
- **On-Prem oder External** – das Postfach ist nicht in der Cloud vorhanden, sondern lokal.
- **Junk-Ordner** – die e-Mail im Ordner Junk eines Benutzers.
- **Ordner "Gelöschte Elemente"** – die e-Mail im Ordner "Gelöschte Elemente" eines Benutzers.
- **Quarantine** – die e-Mail-Nachricht in Quarantäne und befindet sich nicht im Postfach eines Benutzers.
- **Fehler** – die e-Mail konnte das Postfach nicht erreichen.
- **Fallen gelassen** – die e-Mail wird irgendwo in der Nachrichtenübermittlung verloren.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Suchen und löschen verdächtiger e-Mails, die zugestellt wurden

> [!TIP]
> Threat Explorer (manchmal auch als Explorer bezeichnet) ist ein leistungsfähiger Bericht, der mehrere Zwecke wie das Suchen und Löschen von Nachrichten, das Identifizieren der IP-Adresse eines böswilligen e-Mail-Absenders oder das Starten eines Vorfalls zur weiteren Untersuchung dienen kann. Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mails aus Empfängerpostfächern.

So zeigen Sie die Änderungen am früheren Feld "Zustellungs Status" an (jetzt Zustellungs Aktion und Zustellungs Speicherort): 

1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. Dadurch gelangen Sie zum Security &amp; Compliance Center. 
    
2. Klicken Sie im linken Navigationsbereich auf **Threat Management** \> **Explorer**.


![Threat Explorer mit Feldern Zustellungs Aktion und Zustellungs Speicherort.](media/ThreatExFields.PNG)

In dieser Grafik wird möglicherweise die neue Spalte spezielle Aktionen feststellen. Dieses Feature zielt darauf ab, den Administratoren das Ergebnis der Verarbeitung einer e-Mail mitzuteilen. Spezielle Aktionen können am Ende der *e-Mail-Zeitachse*des Threat Explorers aktualisiert werden, ein neues Feature, mit dem die Jagd Erfahrung für Administratoren besser gemacht werden soll.

E-Mail-Zeitachse schneidet nach dem Zufallsprinzip aus, da es bei der Überprüfung verschiedener Standorte kürzer ist, um zu versuchen, Ereignisse zu verstehen, die seit dem Eintreffen der e-Mail geschehen sind. Wenn mehrere Ereignisse bei oder nahe gleichzeitig in einer e-Mail auftreten, werden diese Ereignisse in einer Zeitachsenansicht angezeigt. Einige Ereignisse, die nach der Zustellung an Ihre e-Mails geschehen, werden in der Spalte "spezielle Aktionen" erfasst. Durch die Kombination der Informationen aus der *e-* Mail-Zeitachse dieser e-Mail mit den *speziellen Aktionen* , die bei der e-Mail-Zustellung vorgenommen werden, erhalten Administratoren einen Einblick in die Funktionsweise Ihrer Richtlinien, wo die e-Mail schließlich weitergeleitet wurde und in einigen Fällen, was die endgültige Bewertung war. Auf die Spalte spezielle Aktionen kann an derselben Stelle wie Zustellungs Aktion und Zustellungs Speicherort zugegriffen werden, aber um eine e-Mail-Zeitachse anzuzeigen:

1. Klicken Sie auf den Betreff der e-Mail.
2. Klicken Sie im angezeigten Bereich auf *e-Mail-Zeitachse*. (Sie wird unter anderen Überschriften wie "Zusammenfassung" oder "Details", usw. angezeigt.)

Nachdem Sie die e-Mail-Zeitachse geöffnet haben, sollten Sie eine Tabelle sehen, in der Ihnen die Ereignisse nach der Zustellung für diese e-Mail mitgeteilt werden, oder im Fall von keine weiteren Ereignisse für die e-Mail ein einzelnes Ereignis für die ursprüngliche Zustellung angezeigt wird, das ein Ergebnis wie " *Blockierte* " angibt. mit einem Urteil wie *Phishing*. Die Registerkarte hat auch die Möglichkeit, die gesamte e-Mail-Zeitachse zu exportieren, und dadurch werden alle Details auf der Registerkarte und Details in der e-Mail exportiert (Dinge wie Betreff, Absender, Empfänger, Netzwerk und Nachrichten-ID).

3. Wählen Sie im Menü Ansicht die Option **alle e-Mails**aus.<br/>![Verwenden des Menüs "Ansicht" zum Auswählen zwischen e-Mail-und Inhalts Berichten](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Beachten Sie die Bezeichnungen, die im Bericht angezeigt werden, **** beispielsweise zugestellt, **unbekannt**oder **an Junk gesendet**.<br/>![Threat Explorer mit Daten für alle e-Mails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Abhängig von den Aktionen, die für e-Mail-Nachrichten für Ihre Organisation durchgeführt wurden, werden möglicherweise zusätzliche Bezeichnungen wie " **blockiert** " oder " **ersetzt**" angezeigt.)
    
5. Wählen Sie im Bericht **zugestellt** aus, um nur e-Mails anzuzeigen, die in den Posteingängen von Benutzern landeten.<br/>![Durch Klicken auf "an Junk zugestellt" werden die Daten aus der Ansicht entfernt.](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Überprüfen Sie unter dem Diagramm die **e-Mail-** Liste unter dem Diagramm.<br/>![Zeigen Sie unter dem Diagramm eine Liste der gefundenen e-Mail-Nachrichten an.](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Wählen Sie in der Liste ein Element aus, um weitere Details zu dieser e-Mail-Nachricht anzuzeigen. Beispielsweise können Sie auf die Betreffzeile klicken, um Informationen über den Absender, Empfänger, Anlagen und ähnliche e-Mail-Nachrichten anzuzeigen.<br/>![Sie können zusätzliche Informationen zu einem Element anzeigen, einschließlich Details und Anlagen](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Nachdem Sie Informationen zu e-Mail-Nachrichten angezeigt haben, wählen Sie ein oder mehrere Elemente in der Liste aus, um **+-Aktionen**zu aktivieren.
    
9. Verwenden Sie die Liste **+ Aktionen** , um eine Aktion anzuwenden, beispielsweise " **zu gelöschten Elementen navigieren** ". Dadurch werden die ausgewählten Nachrichten aus den Postfächern der Empfänger gelöscht.<br/>![Wenn Sie eine oder mehrere e-Mail-Nachrichten auswählen, können Sie aus mehreren verfügbaren Aktionen auswählen.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection-Plan 2](office-365-ti.md)
  
[Schutz vor Bedrohungen in Office 365](protect-against-threats.md)
  
[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
  


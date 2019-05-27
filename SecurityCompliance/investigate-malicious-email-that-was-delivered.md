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
ms.openlocfilehash: 7e2cef742339e54c094cfb0c3b32fbf596896a3d
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408300"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>Suchen und untersuchen schädlicher e-Mails, die zugestellt wurden (Office 365 Advanced Threat Protection-Plan 2)

[Office 365 Advanced Threat Protection](office-365-atp.md) ermöglicht es Ihnen, Aktivitäten zu untersuchen, die Ihre Benutzer gefährden und Maßnahmen zum Schutz Ihrer Organisation ergreifen. Wenn Sie beispielsweise Teil des Sicherheitsteams Ihrer Organisation sind, können Sie nach verdächtigen e-Mail-Nachrichten suchen und diese untersuchen, die Ihren Benutzern zugestellt wurden. Sie können dies mithilfe von [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md)durchführen.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:
  
- Ihre Organisation verfügt über [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 oder Plan 2) und [Lizenzen werden Benutzern zugewiesen](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- [Office 365 Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Organisation aktiviert. 
    
- Ihre Organisation verfügt über Richtlinien, die für Antispam-, Antischadsoftware-und Anti-Phishing-Maßnahmen und so weiter definiert sind. Weitere Informationen finden Sie unter [Protect Against Threats in Office 365](protect-against-threats.md).
    
- Sie sind ein Office 365 globaler Administrator oder haben dem Security &amp; Compliance Center entweder den Sicherheitsadministrator oder die Such-und Säuberungs Rolle zugewiesen. Siehe [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Umgang mit verdächtigen e-Mails

Böswillige Angreifer senden möglicherweise e-Mails an Ihre Benutzer, um zu versuchen, Ihre Anmeldeinformationen zu Phishing und Zugriff auf Ihre Unternehmensgeheimnisse zu erhalten. Um dies zu verhindern, sollten Sie die von Office 365 angebotenen Bedrohungsschutz Dienste verwenden, einschließlich [Exchange Online Schutz](eop/exchange-online-protection-overview.md) und [erweitertem Bedrohungsschutz](office-365-atp.md). Es gibt jedoch Situationen, in denen ein Angreifer e-Mails an Benutzer senden kann, die eine URL enthalten, und diese URL erst später auf böswilligen Inhalt (Schadsoftware usw.) verweist. Alternativ erkennen Sie möglicherweise zu spät, dass ein Benutzer in Ihrer Organisation kompromittiert wurde, und während dieser Benutzer kompromittiert wurde, hat ein Angreifer dieses Konto verwendet, um e-Mails an andere Benutzer in Ihrem Unternehmen zu senden. Im Rahmen der Bereinigung beider Szenarien möchten Sie möglicherweise e-Mail-Nachrichten von Benutzer Posteingängen entfernen. In solchen Situationen können Sie [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md) nutzen, um diese e-Mail-Nachrichten zu suchen und zu entfernen.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Suchen und löschen verdächtiger e-Mails, die zugestellt wurden

> [!TIP]
> Threat Explorer (auch als Explorer bezeichnet) ist ein leistungsfähiger Bericht, der mehrere Zwecke wie das Suchen und Löschen von Nachrichten, das Identifizieren der IP-Adresse eines böswilligen e-Mail-Absenders oder das Starten eines Vorfalls zur weiteren Untersuchung dienen kann. Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mails aus Empfängerpostfächern. 
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. Dadurch gelangen Sie zum Security &amp; Compliance Center. 
    
2. Klicken Sie im linken Navigationsbereich auf **Threat Management** \> **Explorer**.
    
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
  


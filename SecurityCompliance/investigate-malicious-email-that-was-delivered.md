---
title: Suchen und untersuchen von gelieferten Schad-e-Mails (Office 365 Threat Intelligence)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection: M365-security-compliance
description: Erfahren Sie, wie Sie mithilfe von Bedrohungs Nachrichten nach bösartigen e-Mails suchen und diese untersuchen.
ms.openlocfilehash: adf4066b5119f131b90dc88b99be4011582931c2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215495"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Suchen und untersuchen von gelieferten Schad-e-Mails (Office 365 Threat Intelligence)

Mit [Office 365 Threat Intelligence](office-365-ti.md) können Sie Aktivitäten untersuchen, die Ihre Benutzer gefährden und Maßnahmen zum Schutz Ihrer Organisation ergreifen. Wenn Sie beispielsweise Teil des Sicherheitsteams Ihrer Organisation sind, finden und untersuchen Sie verdächtige e-Mail-Nachrichten, die an Ihre Benutzer übermittelt wurden. Verwenden Sie dazu den [Threat Explorer](get-started-with-ti.md#threat-explorer).
  
> [!IMPORTANT]
> Beginnend im Februar 2019 und über die nächsten Monate hinaus wird Office 365 Threat Intelligence zu Office 365 Advanced Threat Protection Plan 2 mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:
  
- Ihre Organisation verfügt über [office 365 Threat Intelligence](office-365-ti.md) und [weist benutzern in Office 365 for Business Lizenzen zu](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- [Office 365 die Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Organisation aktiviert. 
    
- Ihre Organisation verfügt über Richtlinien, die für Antispam-, Antischadsoftware-und Antiphishingfunktionen definiert sind. Siehe [Threat Management im Office 365 Security &amp; Compliance Center](threat-management.md).
    
- Sie sind ein globaler Office 365-Administrator, oder Sie haben entweder den Sicherheitsadministrator oder die Rolle "suchen und löschen" im &amp; Security Compliance Center zugewiesen. Weitere Informationen finden Sie unter [Permissions &amp; in the Office 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Umgang mit verdächtigen e-Mails

Böswillige Angreifer können e-Mails an Ihre Benutzer senden, um Ihre Anmeldeinformationen zu testen und Ihren Zugriff auf Ihre Unternehmensgeheimnisse zu erhalten. Um dies zu verhindern, sollten Sie die von Office 365 angebotenen Threat Protection-Dienste verwenden, einschließlich Exchange Online Protection und Advanced Threat Protection. Es gibt jedoch Situationen, in denen ein Angreifer e-Mails an Benutzer senden kann, die eine URL enthalten, und diese URL dann später auf bösartige Inhalte (Schadsoftware usw.) verweisen. Alternativ können Sie zu spät erkennen, dass ein Benutzer in Ihrer Organisation kompromittiert wurde, und während dieser Benutzer kompromittiert wurde, hat ein Angreifer dieses Konto verwendet, um e-Mails an andere Benutzer in Ihrem Unternehmen zu senden. Im Rahmen der Bereinigung beider Szenarien möchten Sie möglicherweise e-Mail-Nachrichten von Benutzer Postfächern entfernen. In solchen Situationen können Sie den Bedrohungs-Explorer nutzen, um diese e-Mail-Nachrichten zu finden und zu entfernen.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Suchen und löschen verdächtiger e-Mails, die übermittelt wurden

> [!TIP]
> [Bedrohungs-Explorer](get-started-with-ti.md#threat-explorer) (auch als Explorer bezeichnet) ist ein leistungsstarker Bericht, der mehrere Zwecke erfüllen kann, beispielsweise das Suchen und Löschen von Nachrichten, die Identifizierung der IP-Adresse eines böswilligen e-Mail-Absenders oder das Starten eines Vorfalls zur weiteren Untersuchung. Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mails aus Empfängerpostfächern. 
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. Dadurch gelangen Sie zum Security &amp; Compliance Center. 
    
2. Klicken Sie im linken Navigationsbereich auf **Threat Management** \> **Explorer**.
    
3. Wählen Sie im Menü Ansicht die Option **alle e-Mails**aus.<br/>![Verwenden des Menüs "Ansicht" zur Auswahl zwischen E-Mails und Inhalts Berichten](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Beachten Sie die Beschriftungen, die im Bericht angezeigt werden, **** beispielsweise "Delivered", " **Unknown**" oder " **an Junk geliefert**".<br/>![Bedrohungs-Explorer mit Daten für alle e-Mails](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Abhängig von den Aktionen, die für e-Mail-Nachrichten für Ihre Organisation durchgeführt wurden, werden möglicherweise zusätzliche Bezeichnungen angezeigt, wie **blockiert** oder **ersetzt**.)
    
5. Wählen Sie im Bericht **geliefert** aus, um nur e-Mails anzuzeigen, die in den Posteingängen der Benutzer landeten.<br/>![Durch Klicken auf "an Junk geliefert" werden die Daten aus der Ansicht entfernt.](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Überarbeiten Sie unterhalb des Diagramms die **e-Mail-** Liste unterhalb des Diagramms.<br/>![Zeigen Sie unterhalb des Diagramms eine Liste der erkannten e-Mail-Nachrichten an.](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Wählen Sie in der Liste ein Element aus, um weitere Details zu dieser e-Mail-Nachricht anzuzeigen. Sie können beispielsweise auf die Betreffzeile klicken, um Informationen zum Absender, zu Empfängern, Anlagen und anderen ähnlichen e-Mail-Nachrichten anzuzeigen.<br/>![Sie können zusätzliche Informationen zu einem Element anzeigen, einschließlich Details und Anlagen](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Nachdem Sie Informationen zu e-Mail-Nachrichten angezeigt haben, wählen Sie ein oder mehrere Elemente in der Liste aus, um **+-Aktionen**zu aktivieren.
    
9. Verwenden Sie die Liste **+-Aktionen** , um eine Aktion wie **Verschieben in gelöschte** Elemente anzuwenden. Dadurch werden die ausgewählten Nachrichten aus den Postfächern der Empfänger gelöscht.<br/>![Wenn Sie eine oder mehrere e-Mail-Nachrichten auswählen, können Sie aus verschiedenen verfügbaren Aktionen auswählen.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  
[Schutz vor Bedrohungen in Office 365](protect-against-threats.md)
  
[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
  


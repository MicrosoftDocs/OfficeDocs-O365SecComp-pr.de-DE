---
title: Finden und Untersuchen von böswilligen e-Mail, die (Office 365 Bedrohungsanalyse) übermittelt wurde
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/6/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
description: Erfahren Sie, wie Bedrohungsanalyse zu finden und Untersuchen von böswilligen e-Mail verwenden.
ms.openlocfilehash: b6d4f8a5d1fcfce4461b91796b1264f94d1eb4d1
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014917"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Finden und Untersuchen von böswilligen e-Mail, die (Office 365 Bedrohungsanalyse) übermittelt wurde

[Office 365 Bedrohungsanalyse](office-365-ti.md) können Sie Aktivitäten zu untersuchen, die Ihre Benutzer gefährden und Ausführen einer Aktion zum Schutz Ihrer Organisation. Wenn Sie in Ihrer Organisation Security Team sind, können Sie beispielsweise suchen und untersuchen verdächtigen e-Mails, die an die Benutzer übermittelt wurden. Diese Schritte können Sie mithilfe von [Explorer Bedrohung](get-started-with-ti.md#threat-explorer)durchführen.
  
> [!NOTE]
> Office 365 Bedrohungsanalyse ist in Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann Office 365 Bedrohungsanalyse als Add-on erworben werden. (Als ein globaler Administrator in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen...

Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:
  
- Ihre Organisation verfügt über [Office 365 Bedrohungsanalyse](office-365-ti.md) und [Zuweisen von Lizenzen für Benutzer in Office 365 für Unternehmen](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- [Office 365-Protokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Organisation aktiviert. 
    
- Ihre Organisation enthält Richtlinien für Anti-Spam-, Anti-Malware, Anti-Phishing und So weiter definiert. Finden Sie unter [Bedrohung Management in die Office 365-Sicherheit &amp; Compliance Center](threat-management.md).
    
- Sie sind Administrator für Office 365 globaler oder Sie haben die Sicherheitsadministrator oder Rolle suchen und Löschen in das Wertpapier &amp; Compliance Center. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Umgang mit verdächtigen e-Mails

Angreifer möglicherweise Senden von Nachrichten an Ihre Benutzer zu testen und Phishing ihre Anmeldeinformationen und Zugriff auf Ihre Kennwörter im Unternehmen! Um dies zu vermeiden, sollten Sie die Bedrohung Protection Dienste von Office 365, einschließlich Exchange Online Protection und erweiterte Threat Protection verwenden. Es gibt jedoch Zeiten, wenn ein Angreifer senden Sie eine e-Mail an die Benutzer, die eine URL enthält kann, und nehmen Sie nur höher auf diesem Zeitpunkt URL schädlichem Inhalt (Malware usw.). Alternativ können Sie zu spät bewusst, dass ein Benutzer in Ihrer Organisation gefährdet und während der Benutzer gefährdet wurde, ein Angreifer dieses Kontos verwendet Senden von e-Mails an andere Benutzer in Ihrem Unternehmen. Als Teil des beide Szenarien bereinigen können Sie e-Mail-Nachrichten aus Posteingänge der Benutzer entfernen möchten. In solchen Situationen können Sie Threat Explorer zum Suchen und entfernen diese e-Mail-Nachrichten nutzen!
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Suchen und Löschen von verdächtigen e-Mails, die übermittelt wurde

> [!TIP]
> [Threat Explorer](get-started-with-ti.md#threat-explorer) (auch als Explorer bezeichnet), ist ein leistungsstarker Bericht, der verschiedene Zwecke wie Suchen und Löschen von Nachrichten, identifizieren die IP-Adresse des e-Mail-Absender oder starten einen Vorfall zur weiteren Untersuchung dienen kann. Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mail-Postfächern der Empfänger. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center. 
    
2. Wählen Sie im linken Navigationsbereich **Threat Management** \> **Explorer**.
    
3. Wählen Sie im Menü Ansicht **Alle e-Mails**.<br/>![Verwenden Sie im Menü Ansicht zwischen e-Mail- und Content-Berichte](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Beachten Sie die Beschriftungen, die im Bericht wie **übermittelte**, **unbekannt**oder **den Junk-e-zugestellt**angezeigt werden.<br/>![Anzeigen von Daten für alle e-Mails Threat Explorer](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Je nach den Aktionen, die für e-Mail-Nachrichten für Ihre Organisation erstellt wurden, möglicherweise zusätzliche Bezeichnungen, beispielsweise **blockiert** oder **ersetzt**angezeigt werden.)
    
5. Wählen Sie im Bericht **gesendet** , um nur e-Mails anzuzeigen, die im Posteingang der Benutzer am Ende aus.<br/>![Durch Klicken auf "An Junk übermittelt" entfernt diese Daten aus der Ansicht](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Überprüfen Sie die **E-Mail** -Liste unterhalb des Diagramms, unterhalb des Diagramms.<br/>![Unterhalb des Diagramms Anzeigen einer Liste von e-Mail-Nachrichten, die erkannt wurden](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Wählen Sie in der Liste ein Element, um weitere Informationen zu dieser e-Mail-Nachricht anzeigen aus. Beispielsweise können Sie die Betreffzeile zum Anzeigen von Informationen über den Absender, Empfänger, Anlagen und andere ähnliche e-Mail-Nachrichten klicken.<br/>![Sie können zusätzliche Informationen zu einem Element, einschließlich Details und alle Anlagen anzeigen.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Nach dem Anzeigen von Informationen zu e-Mail-Nachrichten, wählen Sie ein oder mehrere Elemente in der Liste **+ Aktionen**zu aktivieren.
    
9. Verwenden Sie die Liste **+ Aktionen** , um eine Aktion wie etwa **Verschieben auf gelöschte** Elemente anzuwenden. Dadurch werden die ausgewählten Nachrichten aus den Postfächern der Empfänger gelöscht.<br/>![Wenn Sie einen oder mehrere e-Mail-Nachrichten auswählen, können Sie mehrere verfügbaren Aktionen auswählen](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  
[Schutz vor Bedrohungen in Office 365](protect-against-threats.md)
  
[Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)
  


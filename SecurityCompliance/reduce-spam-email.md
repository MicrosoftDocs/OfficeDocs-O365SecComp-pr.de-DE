---
title: Reduzieren von Spam-E-Mails in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
description: Erfahren Sie mehr über die am häufigsten verwendeten Verfahren zur Reduzierung von Spam und Junk-E-Mails in Office 365.
ms.openlocfilehash: fc7181333b9914673c9919d7132af99fec294773
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219925"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Reduzieren von Spam-E-Mails in Office 365

 **Erhalten Sie zu viel Spam in Office 365? Hier ist die Lösung.**
  
Viele Probleme bezüglich Spam in Office 365 können gelöst werden, indem Sie die [Kopfzeilen von E-Mail-Nachrichten anzeigen](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) und bestimmen, wo der Fehler liegt. Sie müssen nach einer Kopfzeile mit dem Namen X-Forefront-Antispam-Report suchen.

  Wenn diese die Zeichenfolge SFV:NSPM enthält, bedeutet dies, dass Exchange Online Protection (EOP) die Nachricht durchsucht und nicht als Spam bewertet hat. Wenn Sie damit nicht einverstanden sind, wird dies als false negative bezeichnet und es wird dringend empfohlen, dass Sie [das Add-in zum Melden von Nachricht verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2), um uns bei der Verbesserung unserer Filter zu helfen.

  Wenn dieser Wert in den Kopfzeilen nicht angezeigt wird, bedeutet dies möglicherweise entweder, dass die E-Mail den Spam-Scan nicht passiert hat oder dass die Nachricht aufgrund eines Konfigurationsproblems ignoriert wurde. Ziehen Sie in diesem Fall die nachfolgenden Informationen zu Rate. 
  
Weitere Informationen zu [Antispam-Nachrichtenkopfzeilen](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).

## <a name="solutions-to-common-causes-of-getting-too-much-spam"></a>Lösungen für häufige Ursachen von zu viel Spam

Um Sie vor zu viel Spam zu schützen, müssen Administratoren in Exchange Online Protection (EOP) ein paar Aufgaben ausführen. Wenn Sie nicht der Administrator für Ihren Office 365-Mandanten sind und zu viel Spam erhalten, sollten Sie diese Aufgaben zusammen mit Ihrem Administrator ausführen. Andernfalls können Sie mit dem Abschnitt für Benutzer fortfahren.
  
### <a name="for-admins"></a>Für Administratoren

- **Ihre DNS-Einträge auf Office 365 zeigen lassen** Damit EOP Schutz bietet, müssen Ihre MX-Einträge (Mail Exchange) ausschließlich auf Office 365 verweisen. Lesen Sie die Informationen unter [Erstellen von DNS-Einträgen für Office 365 beim Verwalten von DNS-Einträgen.](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)
    
- **Die Junk-E-Mail-Regel für alle Postfächer aktivieren** Standardmäßig ist die Aktion des Spamfilters auf **Nachricht in den Junk-E-Mail-Ordner verschieben** festgelegt. Wenn dies die bevorzugte und aktuelle Spamrichtlinienaktion ist, so muss für jedes Postfach [auch die Junk-E-Mail-Regel aktiviert sein](https://support.office.com/de-DE/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). Um dies zu überprüfen, können Sie das Cmdlet „Get-MailboxJunkEmailConfiguration“ für ein oder mehrere Postfächer ausführen. Sie können z. B. alle Postfächer überprüfen, indem Sie Folgendes ausführen: Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}
    
    Wenn Sie die Ausgabe anzeigen, sollte die Enable-Eigenschaft auf „True“ festgelegt sein. Wenn sie auf „False“ festgelegt ist, können Sie „Set-MailboxJunkEmailConfiguration“ ausführen, um dies in „True“ zu ändern.
    
- **Nachrichtenflussregeln und Liste sicherer Absender überprüfen** Sehen Sie sich die Nachrichtenkopfzeile für eine Nachricht an, die als Spam hätte markiert werden sollen. Suchen Sie die SCL-Eigenschaft in der Kopfzeile „X-Forefront-Antispam-Report“. Wenn der SCL-Wert -1 lautet, deutet dies darauf hin, dass sich die Nachricht in der Liste sicherer Absender befand und vom EOP-Spamfilter übergangen wurde. Überprüfen Sie die Nachrichtenflussregel, die Listen zulässiger Absender sowie die Liste des Empfängers für zulässige Absender. Im Artikel [Suchen und Beheben von Problemen mit der E-Mail-Zustellung als Office 365 Business-Administrator](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) finden Sie auch hilfreiche Details dazu, warum eine Nachricht einen SCL-Wert von -1 erhält. 
    
- **Nachrichtenflussregeln auf dem lokalen Exchange Server erstellen** Wenn Sie Exchange Online Protection verwenden, Ihre Postfächer sich aber auf dem lokalen Exchange Server befinden, müssen Sie ein paar Nachrichtenflussregeln auf dem lokalen Exchange Server erstellen. Lesen Sie [Anweisungen für EOP](https://technet.microsoft.com/library/ms.exch.eac.EditAntispamPolicy_SpamAction%28EXCHG.150%29.aspx?v=15.20.548.14&amp;l=1&amp;s=BPOS_S_E15_0).
    
- **Massen-E-Mails als Spam kennzeichnen** Bei Massen-E-Mails handelt es sich um E-Mails, für die sich Benutzer vielleicht registriert haben, die aber dennoch unerwünscht sind. Suchen Sie im Nachrichtenkopf die BCL-Eigenschaft (Bulk Complaint Level) in der Kopfzeile „X-Microsoft-Antispam“. Wenn der BCL-Wert niedriger als der im Spamfilter festgelegte Wert ist, können Sie den Schwellenwert so anpassen, dass stattdessen diese Typen von Massen-E-Mails als Spam markiert werden. Unterschiedliche Benutzer haben unterschiedliche Toleranzen und Vorlieben dafür, [wie Massen-E-Mails behandelt werden](https://docs.microsoft.com/de-DE/office365/SecurityCompliance/bulk-complaint-level-values). Sie können unterschiedliche Richtlinien oder Regel für die unterschiedlichen Wünsche der Benutzer erstellen. 
    
- **Einen Absender sofort blockieren** Wenn Sie einen Absender sofort blockieren müssen, können Sie anhand der E-Mail-Adresse, der Domäne oder der IP-Adresse blockieren. Lesen Sie die Informationen unter [Blockieren von Spam-E-Mail mit dem Office 365-Spamfilter, um falsch positive negative Ergebnisse zu verhindern](block-email-spam-to-prevent-false-negatives.md). Ein Eintrag in einer Liste zulässiger Absender eines Benutzers kann eine vom Administrator festgelegte Sperre überschreiben.
    
- **Aktivieren des Add-Ins zum Melden von Nachrichten für Benutzer** Wir raten Ihnen dringend, dass Sie [das Add-In zum Melden von Nachrichten für Benutzer aktivieren](enable-the-report-message-add-in.md). Als Administrator können Sie vielleicht auch das Feedback anzeigen, das Ihre Benutzer abgeben, und beliebige Muster verwenden, um Einstellungen anzupassen, die möglicherweise zu Problemen führen.
    
### <a name="for-users"></a>Für Benutzer

- **Die Junk-E-Mail-Regel aktivieren und die Zulassungsliste überprüfen** Überprüfen Sie, ob die Regel für die Junk-E-Mail-Aktion aktiviert wurde und dass der Absender oder die Domäne des Absenders in Ihrer persönlichen Liste zulässiger Adressen nicht übergangen wird. Die beste Möglichkeit, um auf diese Einstellungen zuzugreifen, ist über [Blockieren oder Zulassen (Junk-E-Mail-Einstellungen)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). An dieser Stelle können Sie auch festlegen, dass die E-Mail-Adresse oder Domäne des Absenders blockiert werden soll.
    
- **Spam an Microsoft melden** Melden Sie Spamnachrichten an Microsoft, indem Sie das [Add-In zum Melden von Nachrichten verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Darüber hinaus können Sie eine Nachricht an junk@office365.microsoft.com senden und eine oder mehrere Nachrichten anfügen, die Sie melden möchten.
    
    **Wichtig** Wenn Sie die Nachrichten nicht als Anlagen weiterleiten, so fehlen uns die Kopfzeilen und wir können den Junk-E-Mail in Office 365 nicht verbessern. 
    
- **Abonnement von Massen-E-Mails kündigen** Wenn Sie sich für die Nachricht registriert haben (Newsletter, Produktankündigungen usw.) und diese einen Link zum Kündigen des Abonnements von einer vertrauenswürdigen Quelle enthält, können Sie das Abonnement einfach kündigen. In Office 365 werden diese Nachrichten in der Regel nicht als Spam behandelt. Sie können auch den Absender blockieren oder Ihren Administrator bitten, eine Änderung vorzunehmen, die bewirkt, dass alle Massen-E-Mails als Spam behandelt werden.

---
title: Verhindern, dass echte E-Mails in Office 365 als Spam gekennzeichnet werden
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 34823bbc-a3e3-4949-ba42-97c73997eeed
description: Erfahren Sie, wie verhindert wird, dass echte E-Mails in Office 365 als Spam gekennzeichnet werden.
ms.openlocfilehash: f7ba560b4eb30abcda4c97617ead883659558bd8
ms.sourcegitcommit: 6d72cdb882b93edf6dfddb5ff2e6d8a16e2fa0bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25596718"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a>Verhindern, dass echte E-Mails in Office 365 als Spam gekennzeichnet werden

 **Werden echte E-Mails in Office 365 als Spam gekennzeichnet? Hier kommt die Lösung.**
  
Exchange Online Protection (EOP) versucht, Spam zu filtern, sodass in Ihren Posteingang keine Inhalte gelangen, die Sie nicht sehen möchten. Manchmal filtert EOP aber auch E-Mails, die Sie erhalten möchten.
  
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a>Ermitteln der Ursache, warum die Nachricht als Spam gekennzeichnet wurde

Viele Probleme mit Spam in Office 365 können gelöst werden, indem [Sie die E-Mail-Kopfzeilen anzeigen](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) und bestimmen, was falsch gelaufen ist. Wenn Sie eine Nachrichtenkopfzeile mit dem Namen „X-Forefront-Antispam-Report“ sehen, die die Zeichenfolge „SFV:NSPM“ enthält, bedeutet dies, dass Exchange Online Protection (EOP) die Nachricht überprüft und sie als Spam klassifiziert hat. In diesem Fall empfehlen wir dringend, dass Sie [das Add-In zum Melden von Nachrichten verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2), um uns bei der Verbesserung unserer Filter zu unterstützen. Wenn dieser Wert nicht in den Kopfzeilen angezeigt wird, könnte dies bedeuten, dass die E-Mail entweder nicht die Spamüberprüfung durchlaufen hat, oder dass es ein Konfigurationsproblem gab, aufgrund dessen die Nachricht fälschlicherweise als Spam klassifiziert wurde. [Hier erfahren Sie mehr über die Antispam-Nachrichtenkopfzeilen](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
Suchen Sie in der Kopfzeile nach den folgenden Überschriften und Werten.
  
### <a name="x-forefront-antispam-report"></a>X-Forefront-Antispam-Report

- **SFV:BLK** Gibt an, dass die Nachricht als Spam gekennzeichnet wurde, da sich die Absenderadresse auf der Liste blockierter Absender befindet. 
    
- **SFV:SKS** Gibt an, dass die Nachricht vor dem Inhaltsfilter als Spam markiert wurde. Dies könnte eine Transportregel umfassen, durch die die Nachricht als Spam gekennzeichnet wird. Führen Sie eine Nachrichtenablaufverfolgung aus, um zu überprüfen, ob eine Transportregel ausgelöst wird, die möglicherweise eine hohe SCL-Bewertung (Spam Confidence Level) festgelegt hat. 
    
- **SFV:SKB** Gibt an, dass die Nachricht als Spam markiert, da sie einer Sperrliste in der Richtlinie für den Spamfilter entsprach. 
    
- **SFV:BULK** Gibt an, dass der BCL-Wert (Bulk Complaint Level) in der Kopfzeile x-microsoft-antispam über dem Schwellenwert für Massen-E-Mails liegt, der für den Inhaltsfilter festgelegt wurde. Bei Massen-E-Mails handelt es sich um E-Mails, für die sich Benutzer vielleicht registriert haben, die aber dennoch unerwünscht sind. Suchen Sie im Nachrichtenkopf die BCL-Eigenschaft (Bulk Complaint Level) in der Kopfzeile „X-Microsoft-Antispam“. Wenn der BCL-Wert niedriger als der im Spamfilter festgelegte Wert ist, können Sie den Schwellenwert so anpassen, dass stattdessen diese Typen von Massen-E-Mails als Spam markiert werden. Unterschiedliche Benutzer haben unterschiedliche Toleranzen und Vorlieben dafür, wie [Massen-E-Mails behandelt werden](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). Sie können unterschiedliche Richtlinien oder Regel für die unterschiedlichen Wünsche der Benutzer erstellen.
    
- **CAT:SPOOF** oder **CAT:PHISH** Gibt an, dass die Nachricht gefälscht zu sein scheint, was bedeutet , dass die Nachrichtenquelle nicht überprüft werden kann und verdächtig sein könnte. Wenn die Nachricht gültig ist, muss der Absender sicherstellen, dass sie über eine korrekte SPF- und DKIM-Konfiguration verfügt. Überprüfen Sie die Kopfzeile „Authentication-Results“, um weitere Informationen zu erhalten. Es ist zwar schwierig, alle Absender dazu zu veranlassen, gültige E-Mail-Authentifizierungsmethoden zu verwenden, werden diese Überprüfungen jedoch übergangen, kann dies eine große Gefahr darstellen. 
    
### <a name="x-customspam"></a>x-customspam

- Das Vorhandensein dieser Kopfzeile gibt an, dass die Nachricht als Spam gekennzeichnet wurde, da eine der [erweiterten Spamoptionen](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx) in Ihrem Spamfilter aktiviert ist. Es wird empfohlen, dass Sie die Standardeinstellungen verwenden, sofern Sie diese Features nicht benötigen. 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a>Lösungen für weitere Ursachen von zu viel Spam

Um effektiv zu arbeiten, müssen Administratoren in Exchange Online Protection (EOP) ein paar Aufgaben ausführen. Wenn Sie nicht der Administrator für Ihren Office 365-Mandanten sind und zu viel Spam erhalten, sollten Sie diese Aufgaben zusammen mit Ihrem Administrator ausführen. Andernfalls können Sie mit dem Abschnitt für Benutzer fortfahren.
  
### <a name="for-admins"></a>Für Administratoren

- **DNS-Einträge auf Office 365 zeigen lassen** Damit EOP Schutz bieten kann, müssen die MX-DNS-Einträge (Mail Exchanger) für alle Domänen ausschließlich auf Office 365 zeigen. Wenn die MX-Einträge nicht auf Office 365 zeigen, bietet EOP keinen Spamfilter für Ihre Benutzer. Wenn Sie einen anderen Dienst oder eine andere Anwendung für den Spamfilter für Ihre Domäne verwenden möchten, sollten Sie den Spamschutz in EOP deaktivieren. Erstellen Sie hierfür eine Transportregel, durch die der SCL-Wert auf -1 festgelegt wird. Wenn Sie sich später entschließen, doch EOP zu verwenden, entfernen Sie diese Transportregel. 
    
- **Deaktivieren des SmartScreen-Filters in Outlook** Wenn Ihre Benutzer den Outlook-Desktopclient verwenden, sollten sie den SmartScreen-Filter deaktivieren, da dieser nicht mehr unterstützt wird. Wenn der SmartScreen-Filter aktiviert ist, kann dies zu falsch positiven Ergebnissen führen. Dies sollte nicht erforderlich sein, wenn ein aktualisierter Outlook-Desktopclient ausgeführt wird. 
    
- **Aktivieren des Add-Ins zum Melden von Nachrichten für Benutzer** Wir raten Ihnen dringend, dass Sie [das Add-In zum Melden von Nachrichten für Benutzer aktivieren](enable-the-report-message-add-in.md). Als Administrator können Sie vielleicht auch das Feedback anzeigen, das Ihre Benutzer abgeben, und beliebige Muster verwenden, um Einstellungen anzupassen, die möglicherweise zu Problemen führen.
    
- **Einen Absender sofort zulassen** Wenn Sie einen Absender unmittelbar zulassen möchten, empfehlen wir, dass Sie **NUR die IP-Adresse eines bestimmten Absenders zulassen**. Alternativ können Sie einen Absender zulassen und auch sicherstellen, dass der Absender eine Authentifizierungsüberprüfung wie SPF oder DKIM durchläuft, indem eine Transportregel erstellt wird, die **sowohl** nach der Absenderdomäne als auch nach einer erfolgreichen Authentication-Results-Kopfzeile sucht. 
    
### <a name="for-users"></a>Für Benutzer

- **Spam an Microsoft melden** Melden Sie Spamnachrichten an Microsoft, indem Sie das [Add-In zum Melden von Nachrichten verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Darüber hinaus können Sie eine Nachricht an junk@office365.microsoft.com senden und eine oder mehrere Nachrichten anfügen, die Sie melden möchten.
    
    **Wichtig** Wenn Sie die Nachrichten nicht als Anlagen weiterleiten, so [fehlen uns die Kopfzeilen und wir können den Junk-E-Mail in Office 365 nicht verbessern.](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) 
    
- **Hinzufügen eines Absenders zur Liste zulässiger Absender** Als letzte Option können Sie [Blockieren oder Zulassen (Junk-E-Einstellungen) verwenden](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). In diesem Fall sollten Sie sich bewusst sein, dass ein gezielter Phishingangriff in Ihren Posteingang gelangen könnte.
    


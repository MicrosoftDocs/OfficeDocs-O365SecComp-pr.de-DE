---
title: Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Sie können eine Exchange-Nachrichtenfluss Regel erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.
ms.openlocfilehash: 3552899c2fb471624234625331492edcd8421da6
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692644"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden

Ihnen stehen verschiedene Möglichkeiten zur Verfügung, falsch positive und falsch negative Nachrichten zur Analyse an Microsoft zu senden. Als Administrator können Sie Nachrichtenflussregeln verwenden, um anzuzeigen, was Ihre Benutzer an Microsoft als Spam, kein Spam und betrügerische Phishing-Versuche melden. Weitere Informationen finden Sie unter [Übermitteln von Spam-, Nicht-Spamnachrichten und Nachrichten, die als betrügerische Phishing-Angriffe angesehen werden, an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Umgekehrt können Sie eine Exchange-Nachrichtenfluss Regel (auch als Transportregel bezeichnet) erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Mail Flow Rules" im Thema [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) and the "Outlook on the Web Mailbox Policies" im Thema [Clients and Mobile Devices Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Verwenden Sie die Exchange-Verwaltungskonsole, um eine Nachrichtenflussregel zu erstellen, um Berichte zu Junk-E-Mails, Phishing und Nicht-Junk-E-Mails anzuzeigen.

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Unter **Diese Regel anwenden, wenn...** können Sie **Empfänger** und anschließend **Adresse enthält eines dieser Wörter** wählen.
    
5. Im Feld **Wörter oder Ausdrücke angeben** müssen Sie folgende Änderungen vornehmen: 
    - Geben `abuse@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch negative Nachrichten an Microsoft zu senden.
    - Geben `phish@office365.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie auf Symbol hinzufügen. Diese E-Mail-Adresse wird verwendet, um verpasste Phishingnachrichten an Microsoft zu senden.
    - Geben `false_positive@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `not_junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch positive Nachrichten an Microsoft zu senden.
    - Klicken Sie auf **OK**.
    
6. Wählen Sie unter **Folgendes ausführen** die Option **Bcc der Nachricht an...** aus, und wählen Sie dann die Postfächer aus, in denen Sie Nachrichten erhalten möchten. 
    
7. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Wir empfehlen, die Regel über eine bestimmte Zeit zu testen, bevor Sie sie erzwingen. Weitere Informationen finden Sie unter [Verfahren für Nachrichtenfluss Regeln](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures). 
    
8. Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt. 
    
Nachdem Sie die Regel erstellt und durchgesetzt haben, werden sämtliche von Ihrer Organisation aus an vorgegebene E-Mail-Adressen gesendeten Nachrichten in das angegebene Postfach kopiert.
  


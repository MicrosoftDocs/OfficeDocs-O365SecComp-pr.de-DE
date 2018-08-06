---
title: Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/23/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Sie können eine Exchange-Transportregel zum verhindern, dass Ihre Benutzer am Senden von e-Mail-Nachrichten an Microsoft zur Analyse und deren Verwendung in Ihrer eigenen Sicherheitsprozesse erstellen
ms.openlocfilehash: f2376668e2a1a16eba9913178a100fc31763b227
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026772"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden

Es gibt mehrere Methoden, die Sie false positive und false negative Nachrichten an Microsoft zur Analyse senden können. E-Mail-Flussregeln können Sie als Administrator finden Sie unter was Ihre Benutzer an Microsoft als Spam, nicht-Spam und Phishing-Angriffen reporting. Weitere Informationen finden Sie unter [Submit Spam, nicht-Spam und Phishing-Betrug Nachrichten an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Im Gegensatz dazu können Sie eine Exchange-Transportregel zum verhindern, dass Ihre Benutzer am Senden von e-Mail-Nachrichten an Microsoft zur Analyse und deren Verwendung in Ihrer eigenen Sicherheitsprozesse erstellen.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unterEintrag „Transportregeln" im Thema [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) und Eintrag „Outlook Web App-Postfachrichtlinien" im Thema [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx). 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Verwenden Sie die Exchange-Verwaltungskonsole, um eine Nachrichtenflussregel zu erstellen, um Berichte zu Junk-E-Mails, Phishing und Nicht-Junk-E-Mails anzuzeigen.
<a name="sectionSection1"> </a>

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Unter **Diese Regel anwenden, wenn...** können Sie **Empfänger** und anschließend **Adresse enthält eines dieser Wörter** wählen.
    
5. Im Feld **Wörter oder Ausdrücke angeben** müssen Sie folgende Änderungen vornehmen: 
    - Geben Sie **abuse@messaging.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Geben Sie anschließend **junk@office365.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adressen werden verwendet, um falsch negative Nachrichten an Microsoft zu übermitteln.
    - Geben Sie **phish@office365.microsoft.com** ein, und klicken Sie dann auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adresse wird verwendet, um verpasste Phishingnachrichten an Microsoft zu senden.
    - Geben Sie **false_positive@messaging.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Geben Sie anschließend **not_junk@office365.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adressen werden verwendet, um falsch positive Nachrichten an Microsoft zu übermitteln.
    - Klicken Sie auf **OK**.
    
6. Wählen Sie unter **Folgendes ausführen** die Option **Bcc der Nachricht an...** aus, und wählen Sie dann die Postfächer aus, in denen Sie Nachrichten erhalten möchten. 
    
7. Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Wir empfehlen, die Regel über eine bestimmte Zeit zu testen, bevor Sie sie erzwingen. Weitere Informationen zu diesen Optionen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx). 
    
8. Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt. 
    
Nachdem Sie die Regel erstellt und durchgesetzt haben, werden sämtliche von Ihrer Organisation aus an vorgegebene E-Mail-Adressen gesendeten Nachrichten in das angegebene Postfach kopiert.
  


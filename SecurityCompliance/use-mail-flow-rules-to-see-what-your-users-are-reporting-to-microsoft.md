---
title: Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Sie können eine Exchange-Nachrichtenfluss Regel erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.
ms.openlocfilehash: e93c90074ad2d143a964b928d8e868bee24acba2
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341166"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden

Es gibt mehrere Möglichkeiten, wie Sie falsch positive und falsch negative Nachrichten zur Analyse an Microsoft senden können. Als Administrator können Sie Nachrichtenfluss Regeln verwenden, um zu sehen, was Ihre Benutzer an Microsoft als Spam-, nicht-Spam-und Phishing-Scams melden. Weitere Informationen finden Sie unter [Submit Spam, Non-Spam, and Phishing Scam messages to Microsoft for Analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Umgekehrt können Sie eine Exchange-Nachrichtenfluss Regel (auch als Transportregel bezeichnet) erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Mail Flow Rules" im Thema [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) and the "Outlook on the Web Mailbox Policies" im Thema [Clients and Mobile Devices Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Verwenden Sie die Exchange-Verwaltungskonsole, um eine Nachrichtenflussregel zu erstellen, um Berichte zu Junk-E-Mails, Phishing und Nicht-Junk-E-Mails anzuzeigen.

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.
    
2. Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.
    
3. Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.
    
4. Unter **Diese Regel anwenden, wenn...** können Sie **Empfänger** und anschließend **Adresse enthält eines dieser Wörter** wählen.
    
5. Im Feld **Wörter oder Ausdrücke angeben** müssen Sie folgende Änderungen vornehmen: 
    - Geben `abuse@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch negative Nachrichten an Microsoft zu senden.
    - Geben `phish@office365.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie auf Symbol hinzufügen. Diese e-Mail-Adresse wird verwendet, um verpasste Phishing-Nachrichten an Microsoft zu senden.
    - Geben `false_positive@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `not_junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch positive Nachrichten an Microsoft zu senden.
    - Klicken Sie auf **OK**.
    
6. Wählen Sie unter **Folgendes ausführen** die Option **Bcc der Nachricht an...** aus, und wählen Sie dann die Postfächer aus, in denen Sie Nachrichten erhalten möchten. 
    
7. Wenn Sie möchten, können Sie eine Auswahl treffen, um die Regel zu überwachen, die Regel zu testen, die Regel während eines bestimmten Zeitraums zu aktivieren und andere Optionen auszuwählen. Es wird empfohlen, die Regel für einen Zeitraum zu testen, bevor Sie Sie erzwingen. Weitere Informationen finden Sie unter [Verfahren für Nachrichtenfluss Regeln](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures). 
    
8. Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt. 
    
Nachdem Sie die Regel erstellt und durchgesetzt haben, werden sämtliche von Ihrer Organisation aus an vorgegebene E-Mail-Adressen gesendeten Nachrichten in das angegebene Postfach kopiert.
  


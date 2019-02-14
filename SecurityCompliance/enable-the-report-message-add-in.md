---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie der Bericht-add-in für Outlook und Outlook im Web, für einzelne Benutzer oder der gesamten Organisation zu aktivieren.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995156"
---
# <a name="enable-the-report-message-add-in"></a>Aktivieren des Berichtsnachrichts-Add-Ins

## <a name="overview"></a>Übersicht

Der Bericht-add-in für Outlook und Outlook im Web ermöglicht Personen auf einfache Weise falsch klassifizierte e-Mail, ob die sichere oder böswilliges, in der Regel für die Analyse Unwichtigstes. Microsoft verwendet diese Informationen, um die Effektivität des e-Mail-Schutz Technologien verbessern. Darüber hinaus Wenn Ihre Organisation [Office 365 erweiterte Threat Protection](office-365-atp.md) oder [Office 365 Bedrohungsanalyse](office-365-ti.md)verwendet wird, enthält das Bericht-add-in Ihrer Organisation Security Team nützliche Informationen, die sie verwenden können, um zu prüfen und aktualisieren Sicherheitsrichtlinien. 

Nehmen wir beispielsweise bei Personen viele Nachrichten als Phishing melden möchten. Diese Informationen Flächen in das [Dashboard Sicherheit](security-dashboard.md) und sonstige Berichte. Security-Team Ihrer Organisation können diese Informationen als eine Angabe, die Anti-Phishing-Richtlinien möglicherweise aktualisiert werden. Oder wenn Personen viele Nachrichten protokolliert werden, die als Junk-e-Mail Junk gekennzeichnet wurden, mithilfe des Bericht-add-Ins, Security-Team Ihrer Organisation müssen möglicherweise passen Sie die [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md). 

Das Add-in Berichtnachricht funktioniert mit Ihrem Office 365-Abonnement und die folgenden Produkte:
 - Outlook im Web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 für Mac
 - Outlook im Lieferumfang von Office 365 ProPlus

> [!NOTE]
> Der Bericht-add-in für Outlook und Outlook im Web ist dasselbe wie die [Junk-e-Mail-Filter für Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)nicht genau über wenngleich beide e-Mail als Junk, keine Junk-e- oder Phishing-Versuch markiert verwendet werden können. Der Bericht-add-in für Outlook und Outlook im Web benachrichtigt Microsoft Informationen zu falsch klassifizierte e-Mail während der Junk-e-Mail-Filter für Outlook zum Organisieren von e-Mail-Nachrichten im Postfach des Benutzers verwendet wird. 
  
Wenn Sie einen einzelnen Benutzer sind, können Sie [den Bericht-add-in für sich selbst zu aktivieren](#get-the-report-message-add-in-for-yourself). 
  
Wenn Sie ein globaler Office 365-Administrator oder Exchange Online-Administrator sind und Exchange so konfiguriert ist, dass OAuth-Authentifizierung verwenden, können Sie [den Bericht-add-in für Ihre Organisation zu aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization). Die Nachricht-Add-In für Berichts ist nun durch [Zentralisierte Bereitstellung](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)verfügbar.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Die Meldung Bericht-add-in für sich selbst

1. Suchen Sie in [Microsoft Elemente verwenden](https://appsource.microsoft.com/marketplace/apps)für den [Bericht-add-in](https://appsource.microsoft.com/product/office/wa104381180).
    
2. Wählen Sie **erhalten IT jetzt**.<br/>![Melden Sie Meldung – jetzt abrufen](media/ReportMessageGETITNOW.png)<br/> 
    
3. Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus. 
    
4. Melden Sie sich bei Office 365 mit Ihrer Arbeit oder Schule Konto (zur Verwendung von Business) oder Ihrem Microsoft-Konto (zur persönlichen Verwendung).
    
Nachdem das Add-in installiert und aktiviert ist, sehen Sie die folgenden Symbole: 

- In Outlook sieht das Symbol: <br/> ![Melden Sie Meldung Add-In-Symbol für Outlook](media/OutlookReportMessageIcon.png)<br/>
- In Outlook Web App (oder in Outlook im Web) sieht das Symbol:<br/>![Outlook auf das Symbol Berichtnachricht-add-ins web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Als nächsten Schritt erfahren Sie, wie Sie zur [Verwendung des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Abrufen und das Bericht-add-in für Ihre Organisation zu aktivieren

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein. Darüber hinaus muss Exchange konfiguriert sein, um OAuth-Authentifizierung zum Weitere Informationen finden Sie unter [Anforderungen an Exchange (zentralisierte Bereitstellung von add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements)zu verwenden. 

1. Wechseln Sie zur [Seite für Dienste &-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der Microsoft-365-Verwaltungskonsole.<br/>![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Wählen Sie **+ -Add-in bereitstellen**.<br/>![Wählen Sie Add-In bereitstellen](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Überprüfen Sie die Informationen im Fenster **Neues Add-In** , und wählen Sie dann auf **Weiter**.<br/>![Neue Add-in-details](media/NewAddInScreen1.png)<br/>
    
4. Wählen Sie **ich ein Add-in aus dem Office Store hinzufügen möchten**, und wählen Sie dann auf **Weiter**.<br/>![Ich möchte eine neue Add-In hinzufügen](media/NewAddInScreen2.png)<br/> 
    
5. Durchsuchen Sie und in der Liste der Ergebnisse, neben dem **Bericht Nachricht-Add-In**für **Berichts-Nachricht**, wählen Sie **Hinzufügen**.<br/>![Bericht-Nachricht gesucht, und wählen Sie dann hinzufügen](media/NewAddInScreen3.png)<br/>
    
6. Überprüfen Sie die Informationen auf dem Bildschirm **Bericht** , und wählen Sie dann auf **Weiter**.<br/>![Bericht Nachrichtendetails](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Geben Sie die Standardeinstellungen für Benutzer für Outlook, und wählen Sie dann auf **Weiter**.<br/>![Melden Sie Meldung Standardeinstellungen für Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Geben Sie wer das Bericht-Add-in, und wählen Sie dann auf **Speichern**. <br/>![Wer die Nachricht Bericht-add-in](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Wir empfehlen [eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet einrichten](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).

Personen in Ihrer Organisation müssen je nachdem, was Sie ausgewählt haben, wenn Sie das Add-in (Schritte 7-8 oben), Einrichten des [Berichtnachricht-Add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) zur Verfügung. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt: 

- In Outlook sieht das Symbol: <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- In Outlook Web App (oder in Outlook im Web) sieht das Symbol:<br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Wenn Sie Benutzer über das Add-in Bericht darüber informieren, fügen Sie einen Hyperlink zum [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Richten Sie eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet

> [!IMPORTANT]
> Sie müssen Exchange Online-Administrator zum Ausführen dieser Aufgabe sein.
  
Sie können eine Regel einrichten, um eine Kopie der e-Mail-Nachrichten von Benutzern in Ihrer Organisation gemeldet abzurufen. Sie führen Sie diesen, nachdem Sie heruntergeladen und des Berichtnachricht-add-Ins für Ihre Organisation aktiviert haben.
  
1. Wählen Sie in der Exchange-Verwaltungskonsole, **e-Mail-Fluss** \> **Regeln**. 
    
2. Wählen Sie **+** \> **neue Regel erstellen**. 
    
3. Geben Sie im Feld **Name** einen Namen, beispielsweise Übermittlungen.
    
4. Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...** aus. 
    
5. Klicken Sie im Bildschirm **Wörter oder Ausdrücke angeben** hinzufügen `junk@office365.microsoft.com` und `phish@office365.microsoft.com`, und klicken Sie dann auf **OK**.<br/>![Geben Sie die Junk-e- und Phishing e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Wählen Sie in der Liste **die folgenden Schritte aus...** **Bcc der Nachricht an...**. 
    
7. Fügen Sie ein globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Leser, die eine Kopie der einzelnen Personen an Microsoft gemeldet e-Mail-Nachricht erhalten sollen, und wählen Sie dann auf **OK**.<br/>![Fügen Sie eine globale oder eine Sicherheitsgruppe Administrator, um eine Kopie jeder gemeldeten Nachricht empfangen hinzu](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Wählen Sie **diese Regel mit Schweregrad**aus, und wählen Sie **Mittel**. 
    
9. Wählen Sie unter **Wählen Sie einen Modus für diese Regel** **erzwingen**.<br/>![Eine Regel richten Sie ein, um eine Kopie jeder Nachricht gemeldeten abzurufen](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Klicken Sie auf **Save**. 
    
Mit dieser Regel vorhanden Wenn eine Person in Ihrer Organisation eine e-Mail-Nachricht mit dem Bericht add-in, meldet erhalten Ihrer globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Reader eine Kopie der Nachricht. Diese Informationen können Sie festlegen oder Richtlinien, wie [Links zu Office 365 ATP sicherer](atp-safe-links.md) Richtlinien oder Ihre [Anti-Spam-](anti-spam-protection.md) Einstellungen anpassen. 

## <a name="learn-how-to-use-the-report-message-add-in"></a>Informationen Sie zur Verwendung des Berichtnachricht-add-Ins

Finden Sie unter [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Überprüfen Sie oder bearbeiten Sie der Einstellungen für den Bericht-add-in

Sie können überprüfen und bearbeiten die Standardeinstellungen für den Bericht-add-in auf der [Seite für Dienste &-Add-Ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns). 

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein.
    
1. Wechseln Sie zur [Seite für Dienste &-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der Microsoft-365-Verwaltungskonsole.<br/>![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Suchen Sie und wählen Sie die Add-in-Bericht.<br/>![Suchen Sie und wählen Sie des Berichtnachricht-add-Ins aus](media/FindReportMessageAddIn.png)<br/> 
    
3. Überprüfen Sie auf dem Bildschirm Berichtnachricht und bearbeiten Sie der Einstellungen entsprechend den Anforderungen Ihrer Organisation.<br/>![Einstellungen für den Bericht-add-in](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a>Verwandte Themen

[Verwenden des Add-Ins Nachricht melden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center](view-email-security-reports.md)

[Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)

[Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center](use-explorer-in-security-and-compliance.md)
  


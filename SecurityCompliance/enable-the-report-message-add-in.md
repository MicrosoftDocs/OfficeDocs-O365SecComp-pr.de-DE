---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/04/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Erfahren Sie, wie der Bericht-add-in für Outlook und Outlook im Web, für einzelne Benutzer oder der gesamten Organisation zu aktivieren.
ms.openlocfilehash: 2eb12bd14f92e2d4ee26fbef817578d32e737b85
ms.sourcegitcommit: e14dec9bed0c0009acbc1f1cb80b4d0794ad5739
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2018
ms.locfileid: "25435092"
---
# <a name="enable-the-report-message-add-in"></a>Aktivieren des Berichtsnachrichts-Add-Ins

Bericht-add-in für Outlook können Personen auf einfache Weise falsch klassifizierte e-Mail, ob die sichere oder böswilliges, in der Regel für die Analyse Unwichtigstes. Microsoft verwendet diese Informationen, um die Effektivität des e-Mail-Schutz Technologien verbessern. Darüber hinaus Wenn Ihre Organisation Microsoft Cloud-Dienste, die [Office 365 erweiterte Threat Protection](office-365-atp.md) oder [Bedrohungsanalyse](office-365-ti.md)enthalten verwendet wird, enthält das Bericht-add-in Ihrer Organisation Security Team nützliche Informationen Sie können Sie überprüfen und Aktualisieren von Sicherheitsrichtlinien. 

Nehmen wir beispielsweise bei Personen viele Nachrichten als Phishing melden möchten. Diese Informationen Flächen in das [Dashboard Sicherheit](security-dashboard.md) und sonstige Berichte. Security-Team Ihrer Organisation können diese Informationen als eine Angabe, die Anti-Phishing-Richtlinien möglicherweise aktualisiert werden. Oder wenn Personen viele Nachrichten protokolliert werden, die als Junk-e-Mail Junk gekennzeichnet wurden, mithilfe des Bericht-add-Ins, Security-Team Ihrer Organisation müssen möglicherweise passen Sie die [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md).  
  
Wenn Sie einen einzelnen Benutzer sind, können Sie [den Bericht-add-in für sich selbst zu aktivieren](#get-the-report-message-add-in-for-yourself). 
  
Wenn Sie Exchange Online-Administrator sind, können Sie [den Bericht-add-in für Ihre Organisation zu aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization).
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Die Meldung Bericht-add-in für sich selbst

1. In [Office zu speichern](https://appsource.microsoft.com/product/office/WA104381180?src=office)die Meldung Bericht-add-in.
    
2. Wählen Sie **erhalten IT jetzt**.<br/>![Melden Sie Meldung – jetzt abrufen](media/ReportMessageGETITNOW.png)<br/> 
    
3. Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus. 
    
4. Melden Sie sich bei Ihrem Office 365-e-Mail mit Ihrer Arbeit oder Schule-Konto (zur Verwendung von Business) oder Ihrem Microsoft-Konto (zur persönlichen Verwendung).
    

Nachdem das Add-in installiert und aktiviert ist, sehen Sie die folgenden Symbole: 

- In Outlook sieht das Symbol: <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- In Outlook Web App sieht das Symbol:<br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

Als nächsten Schritt erfahren Sie, wie Sie zur [Verwendung des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Abrufen und das Bericht-add-in für Ihre Organisation zu aktivieren

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein.

1. Wechseln Sie zu [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie **Admin** , fahren Sie mit der Verwaltungskonsole. 
    
3. Wählen Sie **Admin zentriert** \> **Exchange** fahren Sie mit der Exchange-Verwaltungskonsole (EAC). 
    
4. Wählen Sie die **Organisation** \> **-add-ins**. 
    
5. Wählen Sie **+**  >  **aus dem Office Store hinzufügen**.<br/>![Wählen Sie aus dem Office Store hinzufügen](media/EAC-Org-AddFromOfficeStore.png)<br/>Dadurch wird der Office Store in Ihrem Webbrowser geöffnet.
    
6. Suchen nach einer Berichtnachricht.<br/>![Suchen nach einer Berichtnachricht](media/ReportMessageSearchOfficeStore.png)<br/>
    
7. Wählen Sie in der Liste **Apps** **Berichtnachricht aus**, und wählen Sie dann **Sofort erhalten möchten**.<br/>![Wählen Sie GET IT jetzt](media/ReportMessageGETITNOW.png)<br/> 
    
8. Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus. 
    
    ![Klicken Sie auf Weiter, um die Begriffe und die Datenschutzrichtlinie akzeptieren](media/ReportMessageTermsAndConditions.png)
  
9. Ein Assistent wird geöffnet, mit denen Sie Konfigurieren der Überprüfung der Bericht-add-in die Informationen, und wählen Sie **Weiter** , um den Vorgang fortzusetzen.<br/>![Melden Sie Meldung Add-In-Assistenten für Office 365](media/ReportMessageAdminInstallUI.png)<br/> 

10. Geben Sie die Standardeinstellung, die Sie für den Bericht-add-in Benutzern zugewiesen werden sollen.<br/>![Geben Sie die Standardeinstellungen für den Bericht-add-in](media/ReportMessageUserOptionsAdminsSet.png)<br/>
    
11. Geben Sie an, wer die Berichtnachricht-add-in. <br/>![Geben Sie an, wer die Berichtnachricht-add-in](media/ReportMessageChooseWhoGetsItAdminSettings.png)<br/>

12. Wählen Sie **Speichern**.

Je nachdem, was Sie mit dem Assistenten ausgewählt müssen die Personen in Ihrer Organisation des Berichtnachricht add-Ins zur Verfügung. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt: 

- In Outlook sieht das Symbol: <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- In Outlook Web App sieht das Symbol:<br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>


Als Nächstes erfahren Sie, wie [der Bericht-add-in verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)und Einrichten einer Regel gemeldeten e-Mail-Nachrichten angezeigt.

## <a name="review-or-edit-the-default-settings-for-the-report-message-add-in"></a>Überprüfen Sie oder bearbeiten Sie die Standardeinstellungen für den Bericht-add-in

Sie können überprüfen und bearbeiten die Standardeinstellungen für den Bericht-add-in im Admin Center. 

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein.
    
1. Wenn Sie nur das Bericht-add-in für Ihre Organisation installiert haben, müssen Sie bereits auf der Seite Dienste & -add-ins sein. Andernfalls, fahren Sie [hier](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) und melden Sie sich mit Ihrem arbeiten oder Schule-Konto für Office 365.

2. Suchen Sie **Bericht**zu, und wählen Sie dann aus.<br/>![Dienste und add-ins für Office 365](media/ReportMessage-o365servicesaddins.png)<br/> 
    
3. Ein Bereich wird geöffnet, in dem die Einstellungen angezeigt, die für den Bericht-add-in während der Bereitstellung ausgewählt wurden.<br/>![Einstellungen für den Bericht-add-in](media/ReportMessage-reviewaddinsettings.png)<br/> 

4. Überprüfen Sie und bei Bedarf Bearbeiten der Einstellungen für den Bericht-add-in, und klicken Sie dann Ihre Änderungen zu speichern.
    
  
## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Richten Sie eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet

> [!IMPORTANT]
> Sie müssen Exchange Online-Administrator zum Ausführen dieser Aufgabe sein.
  
Sie können eine Regel einrichten, um eine Kopie der e-Mail-Nachrichten von Benutzern in Ihrer Organisation gemeldet abzurufen. Sie führen Sie diesen, nachdem Sie heruntergeladen und des Berichtnachricht-add-Ins für Ihre Organisation aktiviert haben.
  
1. Wählen Sie in der Exchange-Verwaltungskonsole, **e-Mail-Fluss** \> **Regeln**. 
    
2. Wählen Sie **+** \> **neue Regel erstellen**. 
    
3. Geben Sie im Feld **Name** einen Namen, beispielsweise Übermittlungen.
    
4. Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...** aus. 
    
5. Klicken Sie im Bildschirm **Wörter oder Ausdrücke angeben** fügen Sie junk@office365.microsoft.com und phish@office365.microsoft.com hinzu, und wählen Sie dann auf **OK**. 
    
    ![Geben Sie die Junk-e- und Phishing e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. Wählen Sie in der Liste **die folgenden Schritte aus...** **Bcc der Nachricht an...**. 
    
7. Fügen Sie ein globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Leser, die eine Kopie der einzelnen Personen an Microsoft gemeldet e-Mail-Nachricht erhalten sollen, und wählen Sie dann auf **OK**. 
    
    ![Fügen Sie eine globale oder eine Sicherheitsgruppe Administrator, um eine Kopie jeder gemeldeten Nachricht empfangen hinzu](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. Wählen Sie **diese Regel mit Schweregrad**aus, und wählen Sie **Mittel**. 
    
9. Wählen Sie unter **Wählen Sie einen Modus für diese Regel** **erzwingen**. 
    
    ![Eine Regel richten Sie ein, um eine Kopie jeder Nachricht gemeldeten abzurufen](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. Wählen Sie **Speichern**. 
    
Mit dieser Regel vorhanden Wenn eine Person in Ihrer Organisation eine e-Mail-Nachricht mit dem Bericht add-in, meldet erhalten Ihrer globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Reader eine Kopie der Nachricht. Diese Informationen können Sie festlegen oder Richtlinien, wie [Links zu Office 365 ATP sicherer](atp-safe-links.md) Richtlinien anpassen. 
  
## <a name="related-topics"></a>Verwandte Themen

[Verwenden des Berichtnachricht-add-Ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center](view-email-security-reports.md)

[Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)

[Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center](use-explorer-in-security-and-compliance.md)
  


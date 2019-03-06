---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/05/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie das Berichtnachrichten-Add-in für Outlook und Outlook im Web für einzelne Benutzer oder Ihre gesamte Organisation aktivieren können.
ms.openlocfilehash: aba02855b514f0d631d332623d840f9c65911bd1
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410900"
---
# <a name="enable-the-report-message-add-in"></a>Aktivieren des Berichtsnachrichts-Add-Ins

> [!NOTE]
> Das Berichtnachrichten-Add-in für Outlook und Outlook im Web ist nicht genau dasselbe wie der [Outlook-Junk-e-Mail-Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), obwohl beide verwendet werden können, um e-Mails als Junk, nicht als Junk oder als Phishing-Versuch zu kennzeichnen. Der Unterschied besteht darin, dass das Berichtsnachrichten-Add-in für Outlook und Outlook im Web Microsoft über falsch klassifizierte e-Mails benachrichtigt, während der Outlook-Junk-e-Mail-Filter zum Organisieren von e-Mail-Nachrichten im Postfach eines Benutzers verwendet wird. 

## <a name="overview"></a>Übersicht

Das Berichtnachrichten-Add-in für Outlook und Outlook im Web ermöglicht es Benutzern, problemlos falsch klassifizierte e-Mails, ob sicher oder bösartig, an Microsoft und ihre Partner zur Analyse zu melden. Microsoft verwendet diese Übermittlungen, um die Effektivität von e-Mail-Schutztechnologien zu verbessern. Wenn in Ihrer Organisation [office 365 Advanced Threat Protection](office-365-atp.md) oder [Office 365 Threat Intelligence](office-365-ti.md)verwendet wird, stellt das Add-in "Berichtnachricht" Darüber hinaus für das Sicherheitsteam Ihrer Organisation nützliche Informationen zur Verfügung, die Sie zum überarbeiten und aktualisieren verwenden können. Sicherheitsrichtlinien. 

Nehmen wir beispielsweise an, dass Benutzer viele Nachrichten als Phishing melden. Diese Informations Oberflächen werden im [Sicherheits Dashboard](security-dashboard.md) und in anderen Berichten angezeigt. Das Sicherheitsteam Ihrer Organisation kann diese Informationen als Hinweis dafür verwenden, dass Anti-Phishing-Richtlinien möglicherweise aktualisiert werden müssen. Oder wenn Personen viele Nachrichten melden, die mit dem Add-in "Berichtnachricht" als Junk-e-Mail als nicht-Junk markiert wurden, muss das Sicherheitsteam Ihrer Organisation möglicherweise [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md)anpassen. 

Das Berichtnachrichten-Add-in funktioniert mit Ihrem Office 365-Abonnement und den folgenden Produkten:
 - Outlook im Web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 für Mac
 - Outlook im Lieferumfang von Office 365 proPlus

Der vorhandene Webbrowser sollte ausreichen, damit das Berichtnachrichten-Add-in funktioniert. Wenn Sie jedoch feststellen, dass das Add-in nicht verfügbar ist oder nicht wie erwartet funktioniert, probieren Sie einen anderen Browser aus.
  
Wenn Sie ein einzelner Benutzer sind, können Sie [das Berichtnachrichten-Add-in für sich selbst aktivieren](#get-the-report-message-add-in-for-yourself). 
  
Wenn Sie ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sind und Exchange für die Verwendung der OAuth-Authentifizierung konfiguriert ist, können Sie [das Add-in für die Berichtnachricht für Ihre Organisation aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization). Das Berichtnachrichten-Add-in ist jetzt über eine [zentralisierte Bereitstellung](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)verfügbar.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Abrufen des Berichtsnachrichten-Add-Ins für sich selbst

1. Suchen Sie in [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps)nach dem [Add-in "Berichtnachricht](https://appsource.microsoft.com/product/office/wa104381180)".
    
2. Wählen Sie **get it now**aus.<br/>![Berichtnachricht-get it now](media/ReportMessageGETITNOW.png)<br/> 
    
3. Lesen Sie die Nutzungsbedingungen und Datenschutzrichtlinien. Wählen Sie dann **Continue** aus. 
    
4. Melden Sie sich mit Ihrem Geschäfts-oder Schulkonto (für geschäftliche Zwecke) oder Ihrem Microsoft-Konto (für den persönlichen Gebrauch) bei Office 365 an.
    
Nachdem das Add-in installiert und aktiviert wurde, werden die folgenden Symbole angezeigt: 

- In Outlook sieht das Symbol wie folgt aus: <br/> ![Add-in-Symbol für Berichtnachricht für Outlook](media/OutlookReportMessageIcon.png)<br/>
- In Outlook im Web (früher als Outlook Web App bezeichnet) sieht das Symbol wie folgt aus:<br/>![Add-in-Symbol für Outlook im Web-Bericht](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Als nächsten Schritt erfahren Sie, wie Sie [das Add-in "Berichtnachricht" verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Abrufen und Aktivieren des Berichtsnachrichten-Add-Ins für Ihre Organisation

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sein, um diese Aufgabe ausführen zu können. Darüber hinaus muss Exchange für die Verwendung der OAuth-Authentifizierung konfiguriert werden, um weitere Informationen zu erhalten, siehe [Exchange Requirements (zentralisierte Bereitstellung von Add-Ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements). 

1. Wechseln Sie zur [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) im Microsoft 365 Admin Center.<br/>![Seite "Dienste und Add-Ins" im neuen Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Wählen Sie **+ Add-in bereitstellen**aus.<br/>![Wählen Sie Add-in bereitstellen](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Lesen Sie im **neuen Add-in-** Bildschirm die Informationen, und klicken Sie dann auf **weiter**.<br/>![Neue Add-in-Details](media/NewAddInScreen1.png)<br/>
    
4. Wählen Sie **Ich möchte ein Add-in aus dem Office Store hinzufügen**, und klicken Sie dann auf **weiter**.<br/>![Ich möchte ein neues Add-in hinzufügen](media/NewAddInScreen2.png)<br/> 
    
5. Suchen Sie nach **Bericht Meldung**, und wählen Sie in der Ergebnisliste neben dem **Add-in Berichtnachricht**die Option **Hinzufügen**aus.<br/>![Suchen Sie nach Bericht Meldung, und wählen Sie dann hinzufügen](media/NewAddInScreen3.png)<br/>
    
6. Lesen Sie auf dem Bildschirm **Bericht Meldung** die Informationen, und klicken Sie dann auf **weiter**.<br/>![Berichtnachrichten Details](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Geben Sie die Benutzer Standardeinstellungen für Outlook an, und klicken Sie dann auf **weiter**.<br/>![Berichtsnachrichten-Standardeinstellungen für Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Geben Sie an, wer das Add-in für Berichtnachrichten abrufen soll, und klicken Sie dann auf **Speichern**. <br/>![Wer ruft das Add-in für Berichtnachrichten ab](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Es [wird empfohlen, eine Regel einzurichten, um eine Kopie der von Ihren Benutzern gemeldeten e-Mail-Nachrichten abzurufen](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).

Je nachdem, was Sie beim Einrichten des Add-ins ausgewählt haben (Schritte 7-8 oben), wird den Benutzern in Ihrer Organisation das [Add-in "Berichtnachricht](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) " zur Verfügung gestellt. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt: 

- In Outlook sieht das Symbol wie folgt aus: <br/> ![Add-in-Symbol für Berichtnachricht für Outlook](media/OutlookReportMessageIcon.png)<br/>
- In Outlook im Web sieht das Symbol wie folgt aus:<br/>![Add-in-Symbol für Outlook im Web-Bericht](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Wenn Sie Benutzer über das Berichtnachrichten-Add-in Benachrichtigen, fügen Sie einen Link hinzu, um [das Berichtnachrichten-Add-in zu verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Einrichten einer Regel zum Abrufen einer Kopie von e-Mail-Nachrichten, die von Ihren Benutzern gemeldet werden

> [!IMPORTANT]
> Zum Ausführen dieser Aufgabe müssen Sie Exchange Online-Administrator sein.
  
Sie können eine Regel einrichten, um eine Kopie der von Benutzern in Ihrer Organisation gemeldeten e-Mail-Nachrichten abzurufen. Führen Sie dies aus, nachdem Sie das Add-in Berichtsnachricht für Ihre Organisation heruntergeladen und aktiviert haben.
  
1. Wählen Sie im Exchange Admin Center **Nachrichtenfluss** \> **Regeln**aus. 
    
2. Wählen **+** \> Sie **neue Regel erstellen**aus. 
    
3. Geben Sie in das Feld **Name** einen Namen ein, beispielsweise Übermittlungen.
    
4. Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...**. 
    
5. Fügen Sie im Bildschirm **Wörter oder Ausdrücke angeben den Text** hinzu `junk@office365.microsoft.com` , und `phish@office365.microsoft.com`wählen Sie dann **OK**aus.<br/>![Angeben der Junk-und Phishing-e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Wählen Sie in der Liste **führen Sie die folgenden** aus... **die Meldung Bcc an..**. aus. 
    
7. Fügen Sie einen globalen Administrator, Sicherheitsadministrator und/oder Sicherheits Leser hinzu, der eine Kopie jeder e-Mail erhalten soll, die Personen an Microsoft melden, und klicken Sie dann auf **OK**.<br/>![Hinzufügen eines globalen oder Sicherheitsadministrators zum Empfangen einer Kopie jeder gemeldeten Nachricht](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Wählen Sie **diese Regel mit Schweregrad überwachen**aus, und wählen Sie **Mittel**aus. 
    
9. Wählen Sie unter **Wählen Sie einen Modus für diese Regel**aus die Option **erzwingen**aus.<br/>![Einrichten einer Regel zum Abrufen einer Kopie jeder gemeldeten Nachricht](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Wählen Sie **Speichern**. 
    
Wenn diese Regel gilt, erhalten Benutzer, die in Ihrer Organisation eine e-Mail-Nachricht mit dem Berichtnachrichten-Add-in melden, ihren globalen Administrator, Sicherheitsadministrator und/oder Sicherheits Leser eine Kopie dieser Nachricht. Mit diesen Informationen können Sie Richtlinien wie [Office 365 ATP](atp-safe-links.md) -Richtlinien für sichere Links oder Ihre Antispameinstellungen einrichten [](anti-spam-protection.md) oder anpassen. 

## <a name="learn-how-to-use-the-report-message-add-in"></a>Informationen zur Verwendung des Berichtnachrichten-Add-ins

Weitere Informationen finden Sie unter [Verwenden des Berichtnachrichten-Add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Überarbeiten oder Bearbeiten von Einstellungen für das Berichtnachrichten-Add-in

Sie können die Standardeinstellungen für das Berichtnachrichten-Add-in auf der [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns)überarbeiten und bearbeiten. 

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sein, um diese Aufgabe ausführen zu können.
    
1. Wechseln Sie zur [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) im Microsoft 365 Admin Center.<br/>![Seite "Dienste und Add-Ins" im neuen Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Suchen und wählen Sie das Add-in Berichtnachricht aus.<br/>![Suchen und auswählen des Add-Ins "Berichtnachricht"](media/FindReportMessageAddIn.png)<br/> 
    
3. Überprüfung und Bearbeitung der Einstellungen für Ihre Organisation auf dem Bildschirm Bericht Meldung.<br/>![Einstellungen für das Berichtnachrichten-Add-in](media/EditReportMessageAddIn.png)<br/> 

## <a name="related-topics"></a>Verwandte Themen

[Verwenden des Berichtnachrichten-Add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center](view-email-security-reports.md)

[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)

[Verwenden des Explorers im Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)
  


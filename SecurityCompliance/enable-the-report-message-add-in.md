---
title: Aktivieren des Berichtnachricht-add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Erfahren Sie, wie der Bericht-add-in für Outlook und Outlook im Web, für einzelne Benutzer oder der gesamten Organisation zu aktivieren.
ms.openlocfilehash: 2260f8823132d23e0e1f57a421fd223ea3ab14bd
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229997"
---
# <a name="enable-the-report-message-add-in"></a>Aktivieren des Berichtnachricht-add-Ins

Bericht-add-in für Outlook können Personen auf einfache Weise falsch klassifizierte e-Mail, ob die sichere oder böswilliges, in der Regel für die Analyse Unwichtigstes. Microsoft verwendet diese Informationen, um die Effektivität des e-Mail-Schutz Technologien verbessern.
  
Wenn Sie einen einzelnen Benutzer sind, können Sie den Bericht-add-in für sich selbst. 
  
Wenn Sie Exchange Online-Administrator sind, können Sie die Add-in-Bericht für Ihre Organisation.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Die Meldung Bericht-add-in für sich selbst

1. Wechseln Sie zu [https://store.office.com](https://store.office.com), und suchen Sie nach der Add-in-Bericht.
    
2. Wählen Sie **jetzt beziehen** (oder **Hinzufügen** ). 
    
3. Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus. 
    
4. Melden Sie sich bei Ihrem Office 365-e-Mail mit Ihrer Arbeit oder Schule-Konto (zur Verwendung von Business) oder Ihrem Microsoft-Konto (zur persönlichen Verwendung).
    
Nachdem das Add-in installiert und aktiviert ist, sehen Sie die folgenden Symbole: 

- In Outlook sieht das Symbol: </br> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)</br>
- In Outlook Web App sieht das Symbol:</br>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)</br>

  
Als nächsten Schritt erfahren Sie, wie Sie zur [Verwendung des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Abrufen und das Bericht-add-in für Ihre Organisation zu aktivieren

> [!IMPORTANT]
> Sie müssen Exchange Online-Administrator zum Ausführen dieser Aufgabe sein.
  
1. Wechseln Sie zu [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie **Admin** , fahren Sie mit der Verwaltungskonsole. 
    
3. Wählen Sie **Admin zentriert** \> **Exchange** fahren Sie mit der Exchange-Verwaltungskonsole (EAC). 
    
4. Wählen Sie die **Organisation** \> **-add-ins**. 
    
5. Wählen Sie **+** \> **aus dem Office Store hinzufügen**. 
    
6. Suchen nach einer Berichtnachricht.
    
7. Suchen Sie in der Liste mit den **Suchergebnissen App** **Berichtnachricht**, und wählen Sie dann auf **jetzt beziehen** (oder **Hinzufügen** ). 
    
8. Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus. 
    
    ![Klicken Sie auf Weiter, um die Begriffe und die Datenschutzrichtlinie akzeptieren](media/3c813cd6-1601-4791-97dc-f8edbbd3fb6b.png)
  
9. Wählen Sie **Ja**, auf dem Bestätigungsbildschirm zur. 
    
10. Nachdem Sie das Bericht-add-in installiert haben, müssen Sie es aktivieren. Gehen Sie hierzu folgendermaßen vor:
    
1. Zurück zu der Exchange-Verwaltungskonsole, und aktualisieren Sie das Browserfenster.
    
2. Wählen Sie die **Organisation** \> **-add-ins**. 
    
3. Wählen Sie in der Liste der Add-Ins **Berichtnachricht**aus. 
    
    ![In der Exchange-Verwaltungskonsole können Sie den Bericht-add-in für Outlook](media/b496743c-55fa-4cdb-aa06-0b2a7aec6dab.png)
  
4. Wählen Sie **Bearbeiten**, und wählen Sie eine Option aus, um das Add-in zu aktivieren. 
    
    ![Aktivieren des Berichtnachricht-add-Ins in der Exchange-Verwaltungskonsole](media/578b1b66-3620-4a8a-9819-1c9cc6836f37.png)
  
5. Wählen Sie **Speichern**. 
    
> [!TIP]
> Nachdem das Add-in installiert und aktiviert ist, werden die Personen in Ihrer Organisation die folgenden Symbole angezeigt: 
  
Als Nächstes erfahren Sie, wie [der Bericht-add-in verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)und Einrichten einer Regel gemeldeten e-Mail-Nachrichten angezeigt.
  
### <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Richten Sie eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet

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
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  


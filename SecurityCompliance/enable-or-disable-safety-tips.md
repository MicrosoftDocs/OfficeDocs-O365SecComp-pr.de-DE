---
title: Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
ms.collection:
- M365-security-compliance
description: Informiert Office 365-und EOP-Administratoren über die Aktivierung und Deaktivierung von Sicherheitstipps in e-Mail-Nachrichten.
ms.openlocfilehash: 9be9c4cd7fc8e94208aac2ad8812c93a3465f58b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693434"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365

Exchange Online Protection (EOP) fügt einen Sicherheitstipp für von ihm übermittelte e-Mail-Nachrichten hinzu oder stempelt diesen. Diese Sicherheitstipps bieten den Empfängern eine schnelle und visuelle Möglichkeit, um festzustellen, ob eine Nachricht von einem sicheren, überprüften Absender stammt, wenn die Nachricht von Office 365 als Spam gekennzeichnet wurde, wenn die Nachricht etwas Verdächtiges enthält, beispielsweise einen Phishing-Betrug, oder wenn externe Bilder blockiert. Office 365-und EOP-eigenständige Administratoren können eine Spam Richtlinieneinstellung bearbeiten, um zu aktivieren oder zu deaktivieren, dass Sicherheitstipps in Outlook und anderen Desktop-e-Mail-Clients in e-Mails angezeigt werden. 
  
Office 365 ermöglicht Sicherheitstipps standardmäßig für Ihre Organisation, und es wird empfohlen, dass Sie aktiviert bleiben, um Spam-und Phishing-Angriffe zu bekämpfen. Sie können Sicherheitstipps für Outlook im Web nicht deaktivieren.
  
Beispiele und Informationen zu den in Sicherheitstipps angezeigten Daten finden Sie unter [Sicherheitstipps in e-Mail-Nachrichten in Office 365.](safety-tips-in-office-365.md)
  
Inhalt dieses Themas:
  
- [So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe des Office 365 Security &amp; Compliance Center](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe von PowerShell](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe des Office 365 Security &amp; Compliance Center
<a name="SandCCsafetytip"> </a>

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts, Schul- oder Unikonto an.
    
3. Wählen Sie **Richtlinie**für die **Bedrohungs Verwaltung** \> aus. 
    
4. Wählen Sie auf der Seite **Richtlinie** die Option **Antispam**aus.
    
    ![Dieser Screenshot zeigt, wie Sie im Security &amp; Compliance Center auf die Seite Anti-Spam-Einstellungen gelangen.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. Klicken Sie auf der Seite **Anti-Spam-Einstellungen** auf die Registerkarte **Benutzerdefiniert** . 
    
    ![Dieser Screenshot zeigt den Speicherort der benutzerdefinierten Registerkarte auf der Seite Anti-Spam-Einstellungen im &amp; Security Compliance Center.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. Falls erforderlich, wählen Sie die Option **benutzerdefinierte Einstellungen** aus, um benutzerdefinierte Einstellungen zu aktivieren. Wenn die Option benutzerdefinierte Einstellungen auf **aus**festgelegt ist, können Sie keine Spamfilter Richtlinien ändern.
    
    ![Dieser Screenshot zeigt, dass benutzerdefinierte Anti-Spam-Filterrichtlinien Einstellungen deaktiviert wurden.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. Erweitern Sie die zu ändernde Spam Richtlinie, und wählen Sie dann **Richtlinie bearbeiten**aus. Wählen Sie beispielsweise den Pfeil nach unten neben **Standardrichtlinie für Spamfilter**aus. Sie können auch eine neue Richtlinie erstellen, indem Sie **eine Richtlinie hinzufügen**auswählen.
    
8. Erweitern Sie **Spam-und Massen** Aktionen. 
    
9. Aktivieren Sie zur Aktivierung von Sicherheitstipps unter **Sicherheitstipps**das Kontrollkästchen **ein** . Um Sicherheitstipps zu deaktivieren, deaktivieren Sie das Kontrollkästchen **ein** . 
    
10. Wählen Sie **Speichern** aus.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe von PowerShell
<a name="pshellsafetytip"> </a>

Administratoren können Exchange Online PowerShell verwenden, um Sicherheitstipps zu aktivieren oder zu deaktivieren. Verwenden Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum, um Sicherheitstipps in einer Spamfilter Richtlinie zu aktivieren oder zu deaktivieren.
  
1. Stellen Sie eine Verbindung mit Exchange Online PowerShell her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Führen Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum aus, um Sicherheitstipps zu aktivieren oder zu deaktivieren:
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

Wobei Folgendes gilt:
    
  -  *Richtlinienname* ist der Name der Richtlinie, die Sie ändern möchten, beispielsweise **default**.
    
  -  `$true`aktiviert Sicherheitstipps für die Spamfilter Richtlinie. 
    
  -  `$false`deaktiviert Sicherheitstipps für die Spamfilter Richtlinie. 
    
    Führen Sie beispielsweise den folgenden Befehl aus, um Sicherheitstipps für die standardmäßige Spamfilter Richtlinie zu deaktivieren:
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

Weitere Informationen zu diesem Cmdlet finden Sie unter [Set-hostedcontentfilterpolicy dient zum](https://technet.microsoft.com/library/jj200781.aspx).
    
## <a name="still-need-help"></a>Benötigen Sie weitere Hilfe?
<a name="pshellsafetytip"> </a>

Wenn Sie Sicherheitstipps deaktiviert haben, diese jedoch weiterhin in Ihren e-Mail-Nachrichten angezeigt werden, überprüfen Sie Folgendes:
  
- Sie können Sicherheitstipps für Outlook im Web nicht deaktivieren. Versuchen Sie, dieselbe e-Mail in einem anderen Client wie Outlook anzuzeigen.
    
- Sicherheitstipps sind standardmäßig aktiviert für jeden Benutzer, der EOP verwendet, umfasst dies alle Benutzer von Office 365. Um zu verhindern, dass Sicherheitstipps in e-Mails angezeigt werden, müssen Sie Sie mithilfe einer Spamfilter Richtlinie deaktivieren, wie in diesem Thema beschrieben. Nachdem Sie die Richtlinie eingerichtet haben, stellen Sie sicher, dass Sie aktiviert ist. Informationen zum Aktivieren von Spamfilter Richtlinien finden Sie unter [configure your Spamfilter Policies](https://technet.microsoft.com/library/jj200684.aspx).
    
Weitere Möglichkeiten zum bekämpfen von Spam und Phishing finden Sie unter [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).
  


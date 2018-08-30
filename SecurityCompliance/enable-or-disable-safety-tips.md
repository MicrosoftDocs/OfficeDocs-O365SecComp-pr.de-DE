---
title: Aktivieren Sie oder deaktivieren Sie der Sicherheitstipps in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/6/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Office 365 und EOP-Admins erfahren, wie Sie aktivieren und Deaktivieren der Sicherheitstipps in e-Mail-Nachrichten.
ms.openlocfilehash: 3a8257f9d34ec5def54e2b9c9e919172366d023f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529553"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Aktivieren Sie oder deaktivieren Sie der Sicherheitstipps in Office 365

Fügt der Exchange Online Protection (EOP) oder Stempel, eine Safety Tipp, um e-Mail-Nachrichten, die sie bietet. Absender, Safety Tipps bieten eine schnelle, visuelle Möglichkeit, zu bestimmen, ob eine Nachricht aus einer sicheren Empfänger überprüft werden, wenn die Nachricht als Spam von Office 365, markiert wurde, wenn die Nachricht enthält etwas wie Phishing-Betrug verdächtigen oder externe Bilder haben blockiert wurden. Office 365 und EOP-Standalone-Admins können bearbeiten eine richtlinieneinstellung Spam zum Aktivieren oder Deaktivieren der Sicherheitstipps von e-Mail in Outlook und anderen desktop-e-Mail-Clients angezeigt wird. 
  
Office 365 Safety Tipps für Ihre Organisation standardmäßig aktiviert, und es wird empfohlen, dass Sie diese aktiviert gegen Spam und Phishing-Angriffen zu lassen. Sie können keine Sicherheitstipps für Outlook im Web deaktivieren.
  
Beispiele finden Sie unter und lernen Sie die Informationen im Safety Tipps, finden Sie unter [Sicherheit in e-Mail-Nachrichten in Office 365 Tipps.](safety-tips-in-office-365.md)
  
Inhalt dieses Themas:
  
- [So aktivieren oder Deaktivieren von Safety Tipps mithilfe der Office 365-Sicherheit &amp; Compliance Center](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [Tipps zu aktivieren oder deaktivieren die Sicherheit mithilfe von PowerShell](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>So aktivieren oder Deaktivieren von Safety Tipps mithilfe der Office 365-Sicherheit &amp; Compliance Center
<a name="SandCCsafetytip"> </a>

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Geschäfts- oder Schulkonto bei Office 365 an.
    
3. Wählen Sie **Threat Management** \> **Richtlinie**. 
    
4. Wählen Sie auf der Seite **Richtlinie** **Anti-Spam**aus.
    
    ![Dieser Screenshot zeigt, wie Sie auf der Seite Anti-Spam Settings in das Wertpapier abrufen &amp; Compliance Center.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. Wählen Sie auf der Seite **Anti-Spam Settings** die Registerkarte **Benutzerdefiniert** . 
    
    ![Dieser Screenshot zeigt den Speicherort der benutzerdefinierten Registerkarte auf der Seite Anti-Spam Settings in das Wertpapier &amp; Compliance Center.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. Falls erforderlich, wählen Sie die Option **Benutzerdefinierte Einstellungen** , um benutzerdefinierte Einstellungen zu aktivieren. Wenn die Option Benutzerdefinierte Einstellungen auf **deaktiviert**festgelegt ist, werden Sie kann nicht zum Ändern von Richtlinien für Spam-Filter.
    
    ![Dieser Screenshot zeigt benutzerdefinierten Anti-Spam-Filter Richtlinieneinstellungen deaktiviert.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. Erweitern Sie die Spam-Richtlinie, den, die Sie ändern, und wählen Sie dann auf **Richtlinie bearbeiten**möchten. Wählen Sie beispielsweise den Pfeil nach unten neben der **Standard-Spam-Richtlinie zu filtern**. Oder, wenn Sie möchten, können Sie eine neue Richtlinie erstellen, indem Sie **eine Richtlinie hinzufügen**auswählen.
    
8. Erweitern Sie **Spam und Massen** -Aktionen. 
    
9. Aktivieren Sie das Kontrollkästchen **auf** , um Sicherheitstipps, unter **Safety Tipps**zu aktivieren. Deaktivieren Sie das Kontrollkästchen **auf** , um Sicherheitstipps zu deaktivieren. 
    
10. Wählen Sie **Speichern**.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>Tipps zu aktivieren oder deaktivieren die Sicherheit mithilfe von PowerShell
<a name="pshellsafetytip"> </a>

Administratoren können Exchange Online PowerShell aktivieren oder Deaktivieren der Sicherheitstipps. Verwenden Sie das Cmdlet Set-hostedcontentfilterpolicy dient zum Aktivieren oder Deaktivieren der Sicherheitstipps in einer Spam-Filter-Richtlinie.
  
1. Herstellen einer Verbindung mit Exchange Online PowerShell. Informationen finden Sie unter [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Führen Sie das Cmdlet Set-hostedcontentfilterpolicy dient zum Aktivieren oder Deaktivieren der Sicherheitstipps aus:
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

    Wobei Folgendes gilt:
    
  -  *Richtlinienname* ist der Name der Richtlinie, die Sie ändern beispielsweise **Standard, möchten**.
    
  -  `$true`Sicherheitstipps für die Spam-Filter-Richtlinie aktiviert. 
    
  -  `$false`Sicherheitstipps für die Spam-Filter-Richtlinie deaktiviert. 
    
    Führen Sie beispielsweise den folgenden Befehl, um Sicherheitstipps für die Standardrichtlinie für Spam-Filter zu deaktivieren, aus:
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

    Weitere Informationen zu diesem Cmdlet finden Sie unter [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).
    
## <a name="still-need-help"></a>Benötigen Sie weitere Hilfe?
<a name="pshellsafetytip"> </a>

Wenn Sie Sicherheitstipps deaktiviert, aber sind weiterhin in Ihre e-Mail-Nachrichten, überprüfen Sie Folgendes:
  
- Sie können keine Sicherheitstipps für Outlook im Web deaktivieren. Versuchen Sie die gleiche e-Mail in einem anderen Client wie Outlook anzeigen.
    
- Sicherheitstipps sind standardmäßig für jedes, EOP verwendet, einschließlich jeder, der Office 365. Um die Sicherheitstipps in e-Mail angezeigt deaktiviert haben, müssen Sie sie mithilfe einer Filterrichtlinie für Spam, wie in diesem Thema beschrieben deaktivieren. Nachdem Sie die Richtlinie eingerichtet haben, stellen Sie sicher, dass es aktiviert ist. Informationen zu Richtlinien für Spam-Filter aktivieren finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](https://technet.microsoft.com/library/jj200684.aspx).
    
Weitere Methoden zum Spam und Phishing zu bekämpfen finden Sie unter [Office 365 E-Mail Anti-Spam-Schutz](anti-spam-protection.md).
  


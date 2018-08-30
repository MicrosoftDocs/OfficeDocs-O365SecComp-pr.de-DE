---
title: Installation des Add-Ins „Junk-E-Mail-Berichtsprogramm“ für Microsoft Outlook
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8dcc752f-e22e-44ce-a104-4cc4d7e439f3
description: In diesem ArticleSupported LanguagesInstall die Junk-e-e-Mail-Reporting-Add-InUninstall die Junk-e-Mail-Reporting hinzufügen-an Weitere Informationen
ms.openlocfilehash: 4204c80f298a0756f8e2fde2d0845d07570eaff9
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272320"
---
# <a name="install-the-junk-email-reporting-add-in-for-microsoft-outlook"></a>Installation des Add-Ins „Junk-E-Mail-Berichtsprogramm“ für Microsoft Outlook
  
In diesem Thema wird beschrieben, wie Sie das Microsoft-Add-In „Junk-E-Mail-Berichtsprogramm für Outlook“ auf Clientcomputern in Ihrer Organisation installieren und deinstallieren. Die aktuelle Version des Add-Ins (Januar 2016) umfasst Unterstützung für Outlook 2016, Outlook 2013, Outlook 2010 und Outlook 2007.  
  
Das Add-In (für alle unterstützten Sprachen) ermöglicht es Ihnen, Junk-E-Mails direkt aus dem Outlook-Menüband heraus zu melden. Die englische Version des-Add-Ins enthält zusätzliche Optionen zum Melden von E-Mail-Problemen an Microsoft direkt aus dem Menüband:
  
-   Melden von eingegangenen Phishing-Scam-E-Mails 
    
- Melden von E-Mails, die fälschlicherweise als Junk-E-Mails identifiziert wurden.
    
## <a name="supported-languages"></a>Unterstützte Sprachen
<a name="sectionSection0"> </a>

Die folgenden Sprachen werden von dem Add-In "Junk-E-Mail-Berichtsprogramm" unterstützt: 
  
- Chinesisch (vereinfacht)
    
- Chinesisch (traditionell)
    
- Niederländisch
    
- Englisch
    
- Französisch
    
- Deutsch
    
- Italienisch
    
- Japanisch
    
- Koreanisch
    
- Portugiesisch
    
- Portugiesisch (Brasilien)
    
- Spanisch
    
## <a name="install-the-junk-email-reporting-add-in"></a>Installieren des Add-Ins "Junk-E-Mail-Berichtsprogramm"
<a name="sectionSection1"> </a>

Sie können das Add-Ins „Junk-E-Mail-Berichtsprogramm“ installieren:
  
- Durch Ausführen von Windows Installer-Pakets wie andere MSI-Datei. Wenn Sie das Add-in installieren, wird eine Benutzeroberfläche wird geöffnet und in den Installationsbildschirmen aufgefordert. Weitere Informationen finden Sie unter [der Junk-e-Mail-Reporting-Add-In mit dem Setup-Assistenten installieren](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard). OR
    
- Durch Ausführen einer automatischen Installations, die Benutzeroberfläche wird unterdrückt. Stattdessen geben Sie die Befehlszeilenoptionen, die ein Installationsskript ausgeführt. Wenn Sie das Add-in installieren, stehen zusätzliche Konfigurationsoptionen für die nicht mithilfe der Benutzeroberfläche verfügbar sind. Weitere Informationen finden Sie unter [Installieren der Junk-e-Mail-Reporting-Add-In unbeaufsichtigten Modus verwenden](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode).
    
### <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Installationsvoraussetzungen für das Microsoft-Add-In „Junk-E-Mail-Berichtsprogramm für Microsoft Outlook“:
  
- Eines der folgenden Betriebssysteme: Windows 10, Windows 8.1, Windows 8, Windows 7 Service Pack 1, Windows 10 Server, Windows Server 2012 R2, Windows Server 2012 oder Windows Server 2008 R2
    
- Outlook 2016, Outlook 2013, Outlook 2010 oder Outlook 2007 (Service Pack 2 oder höher)
    
- Primäre Interop-Assemblys für Microsoft Office: 
    
  - Informationen zum Herunterladen der primären Interop-Assemblys für Microsoft Office 2010 oder höher, fahren Sie mit dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=166026).
    
  - Wenn die primären Interop-Assemblys für Microsoft Office 2007 herunterladen möchten, wechseln Sie zum [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=72637).
    
- Microsoft .NET Framework, [Version 2.0](https://go.microsoft.com/fwlink/?LinkID=208706).
    
> [!NOTE]
> Für den Computer, auf dem das Add-In installiert werden soll, sind Administratorrechte erforderlich. 
  
### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a>Installieren des Add-Ins "Junk-E-Mail-Berichtsprogramm" mithilfe des Setup-Assistenten
<a name="BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard"> </a>

1. Schließen Sie Outlook auf Ihrem Computer.
    
2. Klicken Sie auf der Seite Microsoft Download Center für die Microsoft Junk-e-Mail Reporting Add-In für Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkID=147248](https://go.microsoft.com/fwlink/?LinkID=147248) , und Laden Sie die MSI-Datei. 
    
3. Doppelklicken Sie auf die MSI-Datei. 
    
4. Klicken Sie auf der Seite **Willkommen beim Setup des Microsoft-Add-Ins "Junk-E-Mail-Berichtsprogramm"** auf **Weiter**. 
    
5. Lesen Sie den Lizenzvertrag, und wenn Sie mit den Installationsbedingungen einverstanden sind, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags zu** (zum Fortsetzen der Installation erforderlich). Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen. 
    
6. Klicken Sie nach Abschluss des Assistenten auf **Fertig stellen**. 
    
7. Starten Sie Outlook.
    
8. Suchen Sie die **Junk-e-** Schaltfläche auf Ihrem Outlook-Menüband. Sie können jetzt Junk-e-Mails an Microsoft, indem Sie die junk-e-Mail-Nachrichten in Ihrem Posteingang auswählen und klicken auf die Schaltfläche **Bericht Junk** melden. 
    
9. Wählen Sie den Pfeil nach unten neben **Junk** aus, um weitere Optionen anzuzeigen, z. B. **Als betrügerischen Phishing-Versuch melden**, wenn Sie Phishing-Scam-E-Mails an Microsoft melden möchten. In Ihrem Junk-E-Mailordner können Sie auch **Keine Junk-E-Mail** auswählen, wenn eine E-Mail-Nachricht fälschlicherweise als Junk-E-Mail gekennzeichnet wurde. 
    
### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a>Installieren des Add-Ins „Junk-E-Mail-Berichtsprogramm“ im unbeaufsichtigten Modus
<a name="BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode"> </a>

1. Schließen Sie Outlook auf Ihrem Computer.
    
2. Öffnen Sie eine Eingabeaufforderung.
    
3. Falls Sie das Add-In direkt ohne optionale Parameter installieren möchten, geben Sie Folgendes an:
    
  - X86-Computern Outlook:`msiexec /qn /i JunkReportingAdd-in.x86-en.msi`
    
  - X64-Computern Outlook:`msiexec /qn /i JunkReportingAdd-in.x64-en.msi`
    
    Sie können auch die optionalen Parameter "MaxMessageSelection" und "BccEmailAddress" angeben:
    
  - MaxMessageSelection ermöglicht Administratoren, die maximale Anzahl von Nachrichten zu definieren, die von Benutzern für die Übermittlung in einem einzigen Klick ausgewählt werden kann. Der Bereich umfasst 1 bis 50 Nachrichten, und der Standardwert ist 10 Nachrichten.
    
    Beispiel: Wenn Sie die maximale Anzahl von Nachrichten, die von Benutzern für die Übermittlung in einem einzigen Klick an 16 ausgewählt werden können, festlegen möchten, verwenden Sie die folgende Option als Teil des Installationsbefehls:`MaxMessageSelection=16`
    
  - BccEmailAddress kann Administratoren ein Postfach einrichten, um eine Kopie der alle ihre Benutzerübermittlungen erhalten, indem Sie eine e-Mail-Adresse "Bcc" festlegen. Wenn das Postfach, eine Kopie aller übermittelt eingerichtet ist werden an die BccEmailAddress-e-Mails gesendet. Andernfalls ist die Standardeinstellung keine Bcc-e-Mail-Adresse.
    
    Beispiel: Wenn Sie junkReports@contoso.com als die Bcc-e-Mail-Adresse für alle Übermittlungen verwenden möchten, verwenden Sie den folgenden Befehl ein:`BccEmailAddress="junkReports@contoso.com"`
    
    > [!NOTE]
    > Sie können mehrere Bcc e-Mail-Adressen, indem sie mit einem Semikolon als Trennzeichen eingeben festlegen. Beispiel:`BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`
  
    Zum Hinzufügen dieser beiden optionalen Parameter würden Sie gemäß den oben stehenden Beispielen für einen Computer, auf dem x86 Outlook ausgeführt wird, Folgendes eingeben: 
    
  ```
  msiexec /qn /i JunkReportingAdd-in.x86-en.msi. MaxMessageSelection=16 BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"
  ```

4. Nachdem die Installation abgeschlossen ist, starten Sie Outlook.
    
5. Suchen Sie die **Junk-e-** Schaltfläche auf Ihrem Outlook-Menüband. Sie können jetzt Junk-e-Mails an Microsoft, indem Sie die junk-e-Mail-Nachrichten in Ihrem Posteingang auswählen und klicken auf die Schaltfläche **Bericht Junk** melden. 
    
6. Wählen Sie den Pfeil nach unten neben **Junk** aus, um weitere Optionen anzuzeigen, z. B. **Als betrügerischen Phishing-Versuch melden**, wenn Sie Phishing-Scam-E-Mails an Microsoft melden möchten. In Ihrem Junk-E-Mailordner können Sie auch **Keine Junk-E-Mail** auswählen, wenn eine E-Mail-Nachricht fälschlicherweise als Junk-E-Mail gekennzeichnet wurde. 
    
## <a name="uninstall-the-junk-email-reporting-add-in"></a>Deinstallieren des Add-Ins "Junk-E-Mail-Berichtsprogramm"
<a name="sectionSection2"> </a>

Wählen Sie zum Deinstallieren des Add-Ins „Junk-E-Mail-Berichtsprogramm“ eine dieser Optionen aus:
  
- Entfernen Sie das Add-In über die Windows-Systemsteuerung. Weitere Informationen finden Sie unter [Uninstall the Junk Email Reporting Add-in from Control Panel](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel). ODER
    
- Führen Sie das Windows Installer-Paket aus, und wählen Sie die Option "Deinstallieren". Weitere Informationen finden Sie unter [Uninstall the Junk Email Reporting Add-in by Running the Windows Installer Package](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage). ODER
    
- Führen Sie eine automatische Installation mithilfe der Deinstallationsoption aus. Weitere Informationen finden Sie unter [Uninstall the Junk Email Reporting Add-in in Silent Mode](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#MK_UninstalltheJunkEmailReportingAdd-ininSilentMode).
    
> [!NOTE]
> Für den Computer, auf dem das Add-In deinstalliert werden soll, sind Administratorrechte erforderlich. 
  
### <a name="uninstall-the-junk-email-reporting-add-in-from-control-panel"></a>Deinstallieren des Add-Ins "Junk-E-Mail-Berichtsprogramm" über die Systemsteuerung
<a name="BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel"> </a>

1. Schließen Sie Outlook auf Ihrem Computer.
    
2. Wählen Sie im Startmenü des Computers die Option **Systemsteuerung**.
    
3. Wählen Sie **Programme und Funktionen**.
    
4. Wählen Sie **Microsoft-Add-In "Junk-E-Mail-Berichtsprogramm für Microsoft Office Outlook"**.
    
5. Wählen Sie **Deinstallieren**.
    
6. Starten Sie Outlook neu, um sich davon zu überzeugen, dass das Add-In nicht mehr in der Outlook-Menüleiste angezeigt wird.
    
### <a name="uninstall-the-junk-email-reporting-add-in-by-running-the-windows-installer-package"></a>Deinstallieren des Add-Ins "Junk-E-Mail-Berichtsprogramm" durch Ausführen des Windows Installer-Pakets
<a name="BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage"> </a>

1. Schließen Sie Outlook auf Ihrem Computer.
    
    > [!NOTE]
    > Wenn Outlook während des Deinstallationsvorgangs ausgeführt wird, müssen Sie es neu starten, um das Add-In vollständig zu deinstallieren. 
  
2. Führen Sie die MSI-Datei aus, die Sie zuvor ausgeführt haben, um das Add-In zu installieren. 
    
    (Wechseln Sie zur Seite im Microsoft Download Center für die Microsoft Junk-e-Mail Reporting Add-In für Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkId=147248](https://go.microsoft.com/fwlink/?LinkId=147248), laden Sie die MSI-Datei, und doppelklicken Sie dann auf die MSI-Datei.) 
    
3. Folgen Sie den Eingabeaufforderungen, um das Add-In zu deinstallieren.
    
4. Starten Sie Outlook neu, um sich davon zu überzeugen, dass das Add-In nicht mehr in der Outlook-Menüleiste angezeigt wird.
    
### <a name="uninstall-the-junk-email-reporting-add-in-in-silent-mode"></a>Deinstallieren des Add-Ins "Junk-E-Mail-Berichtsprogramm" im unbeaufsichtigten Modus
<a name="MK_UninstalltheJunkEmailReportingAdd-ininSilentMode"> </a>

1. Schließen Sie Outlook auf Ihrem Computer.
    
    > [!NOTE]
    > Wenn Outlook während des Deinstallationsvorgangs ausgeführt wird, müssen Sie es neu starten, um das Add-In vollständig zu deinstallieren. 
  
2. Öffnen Sie eine Eingabeaufforderung.
    
3. Geben Sie die folgenden Befehlszeilenparameter an:
    
    X86-Computern Outlook:`msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
    X64-Computern Outlook:`msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
4. Starten Sie Outlook neu, um sich davon zu überzeugen, dass das Add-In nicht mehr in der Outlook-Menüleiste angezeigt wird.
    
## <a name="for-more-information"></a>Weitere Informationen
<a name="sectionSection3"> </a>

[Melden von Junk-E-Mails an Microsoft](report-junk-email-messages-to-microsoft.md)
  
[Problembehandlung und Supportinformationen](troubleshooting-and-support-information.md)
  


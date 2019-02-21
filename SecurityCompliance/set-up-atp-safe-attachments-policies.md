---
title: Einrichten von Office 365 ATP-Richtlinien für sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
ms.collection: M365-security-compliance
description: Definieren Sie Richtlinien für sichere Anlagen zum Schutz Ihrer Organisation vor schädlichen Dateien in e-Mails.
ms.openlocfilehash: dc3235dc8225a46ee28ea8bd0342721b4d55f4f0
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123936"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Einrichten von Office 365 ATP-Richtlinien für sichere Anlagen

Personen, die regelmäßig Anhänge senden, empfangen und freigeben, wie Dokumente, Präsentationen, Tabellenkalkulationen und vieles mehr. Es ist nicht immer einfach zu erkennen, ob eine Anlage sicher oder bösartig ist, indem Sie sich eine e-Mail-Nachricht ansehen. Und das letzte, was Sie wollen, ist eine Schadsoftware, die Sie durchlaufen und verheerend für Ihre Organisation anrichten können. Glücklicherweise kann [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) helfen. Sie können ATP-Richtlinien für [sichere Anlagen](atp-safe-attachments.md) einrichten, um sicherzustellen, dass Ihre Organisation vor Angriffen durch unsichere e-Mail-Anhänge geschützt ist. 
  
## <a name="what-to-do"></a>Nächste Schritte 
  
1. [Überarbeiten der Voraussetzungen](#review-the-prerequisites)
    
2. [Einrichten einer Richtlinie zu sicheren ATP-Anlagen](#set-up-an-atp-safe-attachments-policy)
    
3. [Informationen zu Richtlinienoptionen für ATP-sichere Anlagen](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>Schritt 1: Überarbeiten der Voraussetzungen

- Stellen Sie sicher, dass Ihre Organisation über [Office 365 Advanced Threat Protection](office-365-atp.md)verfügt.
    
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen. Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben: <br>

    |Rolle  |Wo/wie zugewiesen  |
    |---------|---------|
    |Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
    Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

- Informationen [zu Richtlinienoptionen für ATP-sichere Anlagen](#learn-about-atp-safe-attachments-policy-options) (in diesem Artikel). Einige Optionen, wie beispielsweise die Optionen zum Überwachen oder ersetzen, können zu einer geringfügigen Verzögerung von e-Mails führen, während Anlagen gescannt werden. Um Nachrichten Verzögerungen zu vermeiden, sollten Sie die [dynamische Übermittlung und Vorschau](dynamic-delivery-and-previewing.md)verwenden.
    
- Erlauben Sie bis zu 30 Minuten, bis Ihre neue oder aktualisierte Richtlinie auf alle Office 365-Rechenzentren verteilt ist.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>Schritt 2: einrichten (oder bearbeiten) einer ATP-Richtlinie für sichere Anlagen
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. wählen sie im Office 365 &amp; Security Compliance Center im linken navigationsbereich unter bedrohungs **verwaltung**die option **richtlinie** \> für **sichere anlagen**aus.
    
3. Wenn Sie **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**, wird empfohlen, diese Option auszuwählen. Dadurch wird [office 365 Advanced Threat Protection für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) für ihre Office 365-Umgebung aktiviert. 
    
4. Wählen Sie **neu** aus (die Schaltfläche neu ähnelt einem Plus **+** Zeichen ()), um mit dem Erstellen Ihrer Richtlinie zu beginnen.
    
5. Geben Sie den Namen, die Beschreibung und die Einstellungen für die Richtlinie an.<br/><br/>**Beispiel:** Sie können die folgenden Einstellungen angeben, um eine Richtlinie mit dem Namen "keine Verzögerungen" einzurichten, die alle Nachrichten sofort bereitstellt und dann Anhänge anfügt, nachdem Sie gescannt wurden: 
    
      - Geben Sie im Feld **Name** keine Verzögerungen ein.
    
      - Geben Sie im Feld **Beschreibung** eine Beschreibung ein, die Nachrichten sofort übermittelt und nach der Überprüfung Anhänge anfügt.
    
      - Wählen Sie im Abschnitt Antwort die Option **dynamische Zuschaltung** aus. ([Erfahren Sie mehr über die dynamische bereit-und Vorschau mit sicheren ATP-Anlagen](dynamic-delivery-and-previewing.md).)
    
      - Wählen Sie im Abschnitt umLeitungs **Anlage** die Option Umleitung aktivieren aus, und geben Sie die e-Mail-Adresse des globalen Administrators, Sicherheitsadministrators oder Sicherheitsanalysten ihres Office 365 ein, der böswillige Anlagen untersucht. 
    
      - Wählen Sie im Abschnitt **angewendet** am **die Option Empfängerdomäne ist**aus, und wählen Sie dann Ihre Domäne aus. Klicken Sie auf **Hinzufügen**und dann auf **OK**.
    
6. Klicken Sie auf **Save**.
    
Erwägen Sie das Einrichten mehrerer ATP-Richtlinien für sichere Anlagen für Ihre Organisation. Diese Richtlinien werden in der Reihenfolge angewendet, in der Sie auf der Seite " **sichere Anlagen** " aufgeführt sind. Nachdem eine Richtlinie definiert oder bearbeitet wurde, können die Polizeibehörden mindestens 30 Minuten lang in Microsoft-Rechenzentren wirksam werden. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>Schritt 3: Informationen zu Richtlinien Optionen für ATP Safe Attachments

Bei der Einrichtung Ihrer Richtlinien für sichere ATP-Anlagen wählen Sie aus zahlreichen Optionen, einschließlich Monitor, Block, ersetzen, dynamischer Bereitstellung usw. Wenn Sie sich Fragen, was diese Optionen tun, werden in der folgenden Tabelle die einzelnen und ihre Auswirkungen zusammengefasst.
  
|**Option**|**Effekt**|**Verwenden Sie, wenn Sie Folgendes möchten:**|
|:-----|:-----|:-----|
|**Off** <br/> |Die Anlagen werden nicht auf Schadsoftware überprüft  <br/> Nachrichtenübermittlung wird nicht verzögert  <br/> |Deaktivieren Sie die Überprüfung für interne Absender, Scanner, Faxe oder Smarthosts, die nur bekannte, gute Anlagen senden.  <br/> Vermeiden unnötiger Verzögerungen beim Routing interner e-Mails  <br/> **Diese Option wird für die meisten Benutzer nicht empfohlen. Es ermöglicht Ihnen, die Überprüfung von ATP Safe Attachments für eine kleine Gruppe interner Absender zu aktivieren.**           |
|**Monitor** <br/> |Übermittelte Nachrichten mit Anlagen und verfolgt dann, was mit erkannter Schadsoftware geschieht  <br/> |Siehe wo erkannte Schadsoftware in Ihrer Organisation geht  <br/> |
|**Block** <br/> |Verhindert das Fortsetzen von Nachrichten mit erkannter Schadsoftware  <br/> Sendet Nachrichten mit erkannter Schadsoftware [in Quarantäne in Office 365](manage-quarantined-messages-and-files.md) , in der ein Sicherheitsadministrator oder Analytiker diese Nachrichten überarbeiten und freigeben (oder löschen) kann  <br/> Automatisches Blockieren zukünftiger Nachrichten und Anlagen  <br/> |Schützen Sie Ihre Organisation vor wiederholten Angriffen mit denselben Schadsoftware-Anlagen  <br/> |
|**Ersetzen** <br/> |Entfernt erkannte Schadsoftware-Anlagen  <br/> Benachrichtigt Empfänger, dass Anlagen entfernt wurden.  <br/> Sendet Nachrichten mit erkannter Schadsoftware [in Quarantäne in Office 365](manage-quarantined-messages-and-files.md) , in der ein Sicherheitsadministrator oder Analytiker diese Nachrichten überarbeiten und freigeben (oder löschen) kann  <br/> |Erhöhen der Sichtbarkeit von Empfängern, dass Anlagen aufgrund erkannter Schadsoftware entfernt wurden  <br/> |
|**Dynamische Verteilung** <br/> |Sofortiges übermitteln von Nachrichten  <br/> Ersetzt Anlagen mit einer Platzhalterdatei, bis die Überprüfung abgeschlossen ist, und fügt die Anlagen dann erneut an, wenn keine Schadsoftware erkannt wird.  <br/> Enthält Funktionen für die Vorschau von Anlagen für die meisten PDFs und Office-Dateien während des Scans  <br/> Sendet Nachrichten mit erkannter Schadsoftware in Quarantäne, in der ein Sicherheitsadministrator oder Analytiker diese Nachrichten überarbeiten und freigeben (oder löschen) kann  <br/> [Informationen zur dynamischen bereitstellen und Vorschau mit sicheren ATP-Anlagen](dynamic-delivery-and-previewing.md) <br/> |Vermeiden von Nachrichten Verzögerungen beim Schützen von Empfängern vor schädlichen Dateien  <br/> Empfänger können Anhänge im abgesicherten Modus anzeigen, während die Überprüfung stattfindet  <br/> |
|**Umleitung aktivieren** <br/> |Gilt, wenn die Option Monitor, Block oder ersetzen ausgewählt ist.  <br/> Sendet Anlagen an eine angegebene e-Mail-Adresse, die von Sicherheitsadministratoren oder Analysten untersucht werden kann  <br/> |Aktivieren von Sicherheitsadministratoren und Analysten zur Untersuchung verdächtiger Anlagen  <br/> |
   
## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Ihre ATP-Richtlinien für sichere Anlagen eingerichtet haben, können Sie sehen, wie ATP für Ihre Organisation funktioniert, indem Sie Berichte anzeigen. Weitere Informationen finden Sie in den folgenden Ressourcen:
- [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
- [Verwenden des Explorers im Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)

Bleiben Sie auf dem neuesten Stand der neuen Features für ATP. Besuchen Sie die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) , und erfahren Sie mehr über [neue Features, die ATP hinzugefügt werden](office-365-atp.md#new-features-in-office-365-atp).
 
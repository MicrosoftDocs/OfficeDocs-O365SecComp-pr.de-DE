---
title: Einrichten von Office 365 ATP-Richtlinien für sichere Links
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
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection: M365-security-compliance
description: Einrichten von Richtlinien für sichere Links zum Schutz Ihrer Organisation vor böswilligen Links in Word-, Excel-, PowerPoint-und Visio-Dateien sowie in e-Mail-Nachrichten.
ms.openlocfilehash: ee60b8fa5824b5e7ff478370216b52d17a6dc94f
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123956"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Einrichten von Office 365 ATP-Richtlinien für sichere Links

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden. Wenn Sie ein Benutzer sind, der nach Informationen zu sicheren Links in Outlook sucht, lesen Sie den Thema [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

[ATP-sichere Links](atp-safe-links.md), eine Funktion von [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), können Ihre Organisation vor böswilligen linksschützen, die bei Phishing-und anderen Angriffen verwendet werden. Wenn Sie über die erforderlichen [Berechtigungen für das Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)verfügen, können Sie ATP-Richtlinien für sichere Links einrichten, um sicherzustellen, dass beim Klicken auf Webadressen (URLs) Ihre Organisation geschützt ist. Ihre ATP-Richtlinien für sichere Links können so konfiguriert werden, dass URLs in e-Mails und URLs in Office-Dokumenten gescannt werden.
  
[Den ATP werden ständig neue Features hinzugefügt](office-365-atp.md#new-features-in-office-365-atp). Wenn neue Features hinzugefügt werden, müssen Sie möglicherweise Anpassungen an Ihren vorhandenen ATP-Richtlinien für sichere Links vornehmen.

## <a name="what-to-do"></a>Nächste Schritte 
  
1. [Überarbeiten Sie die voraus](#review-the-prerequisites)setzungen.
    
2. [Überarbeiten Sie die Standardrichtlinie für sichere ATP-Links, die für alle gilt](#define-an-atp-safe-links-policy-that-applies-to-everyone). Sie können beispielsweise [Ihre benutzerdefinierte Liste blockiertEr URLs für sichere ATP-Links einrichten](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Hinzufügen oder Bearbeiten von Richtlinien für bestimmte e-Mail-Empfänger](#add-a-policy-for-specific-email-recipients), einschließlich [der Einrichtung Ihrer benutzerdefinierten Liste "nicht umschreiben" für ATP-sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Weitere Informationen zu den Optionen für sichere Links für ATP](#learn-about-atp-safe-links-policy-options) (in diesem Artikel), einschließlich der Einstellungen für die letzten Änderungen.
    
## <a name="step-1-review-the-prerequisites"></a>Schritt 1: Überarbeiten der Voraussetzungen

- Stellen Sie sicher, dass Ihre Organisation über [Office 365 Advanced Threat Protection](office-365-atp.md)verfügt.
    
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen. Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben: <br>

    |Rolle  |Wo/wie zugewiesen  |
    |---------|---------|
    |Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

    Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

- Stellen Sie sicher, dass die Office-Clients für die Verwendung der [modernen Authentifizierung](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) konfiguriert sind (Dies ist für den Schutz von ATP-Sicherheits Links in Office-Dokumenten).
    
- [Weitere Informationen zu den Optionen für sichere Links für ATP](#learn-about-atp-safe-links-policy-options) (in diesem Artikel). 

- Erlauben Sie bis zu 30 Minuten, bis Ihre neue oder aktualisierte Richtlinie auf alle Office 365-Rechenzentren verteilt ist.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>Schritt 2: definieren (oder überarbeiten) der ATP-Richtlinie für sichere Links, die für jeden gilt

Wenn Sie [Office 365 Advanced Threat Protection](office-365-atp.md)haben, haben Sie eine standardRICHTLINIE für ATP-sichere Links, die für alle Benutzer in Ihrer Organisation gilt. Stellen Sie sicher, dass Sie die Standardrichtlinie überprüfen und gegebenenfalls bearbeiten.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Wählen Sie im linken Navigationsbereich unter **Bedrohungs Verwaltung**die Option **Richt \> Linie** für **sichere Links**aus.
    
3. Wählen Sie in den **Richtlinien für den Abschnitt gesamte Organisation** die Option **Standard**aus, und klicken Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten ähnelt einem Bleistift).<br/>![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für den Schutz sicherer Links zu bearbeiten.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Geben Sie im Abschnitt **folgende URLs blockieren** eine oder mehrere URLs an, die verhindern sollen, dass Personen in Ihrer Organisation einen Besuch abhalten. (Siehe [Einrichten einer benutzerdefinierten Liste blockiertEr URLs mithilfe von ATP-sicheren Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).)
    
5. Wählen Sie im Abschnitt **Einstellungen für Inhalt außer e-Mail** die gewünschten Optionen aus (oder löschen). (Es wird empfohlen, alle Optionen auszuwählen.) 
    
6. Klicken Sie auf **Save**.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>Schritt 3: hinzufügen (oder bearbeiten) ATP-Richtlinien für sichere Links, die für bestimmte e-Mail-Empfänger gelten

Nachdem Sie die standardmäßige ATP-Richtlinie für sichere Links für alle Benutzer überprüft (oder bearbeitet) haben, besteht der nächste Schritt darin, zusätzliche Richtlinien zu definieren, die für bestimmte Empfänger gelten. Sie können beispielsweise Ausnahmen für Ihre Standardrichtlinie angeben, indem Sie eine zusätzliche Richtlinie definieren. 
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. 
    
2. Wählen Sie im linken Navigationsbereich unter **Bedrohungs Verwaltung**die Option **Richtlinie**aus.
    
3. Wählen Sie **sichere Links**aus.
    
4. Klicken Sie im Abschnitt **Richtlinien für bestimmte Empfänger auf** **neu** (die Schaltfläche neu ähnelt einem Pluszeichen ( **+**)).<br/>![Wählen Sie neu aus, um eine Richtlinie zu sicheren Links für bestimmte e-Mail-Empfänger hinzuzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Geben Sie den Namen, die Beschreibung sowie Einstellungen für Ihre Richtlinie an.<br/>**Beispiel:** Um eine Richtlinie mit dem Namen "kein direktes Klicken durch" einzurichten, die Personen in einer bestimmten Gruppe in Ihrer Organisation nicht ermöglicht, durch Klicken auf eine bestimmte Website ohne ATP Safe Links Protection zu navigieren, können Sie die folgenden empfohlenen Einstellungen angeben: 
    
  - Geben Sie im Feld **Name** keinen direkten Mausklick ein.
    
  - Geben Sie in das Feld **Beschreibung** eine Beschreibung wie ein, um zu verhindern, dass Personen in bestimmten Gruppen durch Klicken zu einer Website ohne überPRÜFUNG der ATP-sichere Links zu einer Webseite navigieren.
    
  - Klicken Sie im Abschnitt **Aktion auswählen** **auf ein**.
    
  - Wählen Sie **sichere Anlagen zum Überprüfen von herunterladbaren Inhalten**aus.
    
  - Wenn diese Option verfügbar ist, wählen Sie **sichere Links auf Nachrichten anwenden aus, die innerhalb der Organisation gesendet**werden.
    
  - Aktivieren Sie die Option **Benutzer darf nicht auf die ursprüngliche URL klicken**.
    
  - (Optional) Geben Sie im Abschnitt **folgende URLs nicht umschreiben** eine oder mehrere URLs an, die als sicher für Ihre Organisation gelten. (Siehe [Einrichten einer benutzerdefinierten URLs-Liste "nicht umschreiben" mithilfe von ATP-sicheren Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Wählen Sie im Abschnitt **angewendet** am **den Empfänger ist Mitglied von aus**, und wählen Sie dann die Gruppe (n) aus, die Sie in Ihre Richtlinie aufnehmen möchten. Klicken Sie auf **Hinzufügen**und dann auf **OK**.
    
6. Klicken Sie auf **Save**.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>Schritt 4: Informationen zu den Optionen für die ATP-Sicherheits Links

Wenn Sie Ihre ATP-Richtlinien für sichere Links einrichten oder bearbeiten, stehen Ihnen mehrere Optionen zur Verfügung. Wenn Sie sich Fragen, was diese Optionen sind, wird in der folgenden Tabelle jede und ihre Auswirkung beschrieben. Denken Sie daran, dass es zwei Hauptarten von ATP-Richtlinien für sichere Links gibt, die Sie definieren oder bearbeiten können:
- eine [Standardrichtlinie](#default-policy-options) , die für jeden gilt 
- zusätzliche [Richtlinien, die für bestimmte Empfänger definiert sind](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>Standardrichtlinien Optionen

Standardrichtlinien Optionen gelten für alle Benutzer in Ihrer Organisation.

|Diese Option  |Funktion  |
|---------|---------|
| **Blockieren der folgenden URLs** <br/>    | Ermöglicht Ihrer Organisation eine benutzerdefinierte Liste von URLs, die automatisch blockiert werden. Wenn Benutzer auf eine URL in dieser Liste klicken, werden Sie zu einer [Warnungsseite](atp-safe-links-warning-pages.md) geleitet, die erklärt, warum die URL blockiert ist.<br/> Weitere Informationen finden Sie unter [Einrichten einer benutzerdefinierten Liste blockierter URLs mit sicheren ATP-Links      |
| **Office 365 proPlus, Office für iOS und Android** <br/>    | Wenn diese Option ausgewählt ist, wird der sichere ATP-Links Schutz auf URLs in Dokumenten angewendet, die in Office 365 proPlus (Word, Excel und PowerPoint unter Windows oder Mac OS), Office-Dokumente auf iOS-oder Android-Geräten, Visio 2016 unter Windows und Office Online (Word Online, PowerPoint Online, Excel Online und OneNote Online), sofern der Benutzer sich bei Office 365 angemeldet hat. <br/><br/>Wenn nur **Office 2016 unter Windows**angezeigt wird, haben die Feature-Updates noch nicht ihre Office 365-Umgebung erreicht (und Sie werden bald verfügbar sein). Bis dahin gilt ATP Safe Links Protection für Word 2016, Excel 2016, PowerPoint 2016 oder Visio 2016 unter Windows.            |
| **Nicht nachverfolgen, wenn Benutzer auf ATP-sichere Links klicken** <br/>  | Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in Word, Excel, PowerPoint und Visio-Dokumente wird nicht gespeichert.  <br/> |
|**Nicht zulassen, dass Benutzer auf ATP-sichere Links mit ursprünglicher URL klicken** <br/> |Wenn diese Option aktiviert ist, können Benutzer nicht über eine [Warnungsseite](atp-safe-links-warning-pages.md) an eine URL weitergeleitet werden, die als bösartig festgelegt wurde.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>Richtlinien für bestimmte e-Mail-Empfänger

|Diese Option  |Funktion  |
|---------|---------|
|**Off** <br/> |URLs in e-Mail-Nachrichten werden nicht überprüft.  <br/> Ermöglicht Ihnen das Definieren einer Ausnahmeregel, beispielsweise einer Regel, die URLs in e-Mail-Nachrichten für eine bestimmte Empfängergruppe nicht überprüft.  <br/> |
|**Auf** <br/> |Schreibt URLs neu, um Benutzer über den sicheren ATP-Links Schutz zu leiten, wenn die Benutzer auf URLs in e-Mail-Nachrichten klicken.  <br/> Überprüft eine URL, wenn auf eine Liste blockierter oder bösartiger URLs geklickt wird.  <br/> |
|**Verwenden sicherer Anlagen zum Überprüfen von herunterladbaren Inhalten** <br/> |Wenn diese Option ausgewählt ist, werden URLs, die auf herunterladbare Inhalte verweisen, überprüft.  <br/> |
|**Anwenden sicherer Links auf Nachrichten, die innerhalb der Organisation gesendet werden** <br/> | Wenn diese Option verfügbar und ausgewählt ist, wird der sichere ATP-Links Schutz auf e-Mail-Nachrichten angewendet, die zwischen Personen in Ihrer Organisation gesendet werden, vorausgesetzt, die e-Mail-Konten werden in Office 365 gehostet.  <br/> |
|**Benutzerklicks nicht nachverfolgen** <br/> |Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in e-Mails von externen Absendern wird nicht gespeichert. URL-Click Tracking für Links innerhalb von e-Mails, die innerhalb der Organisation gesendet werden, wird derzeit nicht unterstützt.  <br/> |
|**Benutzer dürfen nicht auf die ursprüngliche URL klicken.** <br/> |Wenn diese Option aktiviert ist, können Benutzer nicht über eine [Warnungsseite](atp-safe-links-warning-pages.md) an eine URL weitergeleitet werden, die als bösartig festgelegt wurde.  <br/> |
|**Die folgenden URLs nicht umschreiben** <br/> |Leaves URLs wie Sie sind. Speichert eine benutzerdefinierte Liste sicherer URLs, die keine Überprüfung für eine bestimmte Gruppe von e-Mail-Empfängern in Ihrer Organisation benötigen.  Weitere Informationen finden Sie unter [Einrichten einer benutzerdefinierten URL-Liste "nicht umschreiben" unter Verwendung von ATP-Sicherheits Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) , einschließlich der letzten Änderungen an der\*Unterstützung von Platzhalter Sternchen ().<br/> |
   
## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Ihre ATP-Richtlinien für sichere Links eingerichtet haben, können Sie sehen, wie ATP für Ihre orgnization funktioniert, indem Sie Berichte anzeigen. Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)

- [Verwenden des Explorers im Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)

Bleiben Sie auf dem neuesten Stand der neuen Features für ATP. Besuchen Sie die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) , und erfahren Sie mehr über [neue Features, die ATP hinzugefügt werden](office-365-atp.md#new-features-in-office-365-atp).
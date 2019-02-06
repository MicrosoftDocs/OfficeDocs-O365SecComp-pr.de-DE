---
title: Einrichten von Richtlinien für Office 365 ATP sichere Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Richten Sie Richtlinien für sichere Links mit Ihrer Organisation vor böswilligen Links in Word, Excel, PowerPoint und Visio-Dateien sowie in e-Mail-Nachrichten zu schützen.
ms.openlocfilehash: 714b3df825272ab182443b31e0b2cf90b64b71b7
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741088"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Einrichten von Richtlinien für Office 365 ATP sichere Links

[ATP sichere Links](atp-safe-links.md), ein Feature von [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP), können Ihre Organisation vor böswilligen Links in Phishing und anderen Angriffen verwendet schützen. Wenn Sie die erforderlichen haben [Berechtigungen für die Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), ATP sichere Links Richtlinien einrichten, um sicherzustellen, dass beim Klicken auf Webadressen (URLs), Ihrer Organisation geschützt ist. Ihrer Richtlinien ATP sichere Links können in e-Mail-URLs und URLs in Office-Dokumenten überprüfen konfiguriert werden.
  
[Neue Features ständig ATP hinzugefügt wird](office-365-atp.md#new-features-are-continually-being-added-to-atp). Neue Features hinzugefügt werden, müssen Sie möglicherweise Ihre vorhandenen ATP sichere Links Richtlinien anpassen.

## <a name="what-to-do"></a>Nächste Schritte 
  
1. [Überprüfen Sie die erforderlichen Komponenten](#review-the-prerequisites).
    
2. [Überprüfen und Bearbeiten der Standardrichtlinie für ATP sichere Links, die für alle Benutzer gilt](#define-an-atp-safe-links-policy-that-applies-to-everyone). Beispielsweise können Sie [die benutzerdefinierten blockierte URLs Liste für sichere Links ATP eingerichtet](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Hinzufügen oder Bearbeiten von Richtlinien für bestimmte e-Mail-Empfänger](#add-a-policy-for-specific-email-recipients), einschließlich der [Einrichtung von Ihrer benutzerdefinierten "Nicht rewrite" URLs Liste für sichere ATP-Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Informieren Sie sich über Richtlinienoptionen ATP sichere Links](#learn-about-atp-safe-links-policy-options) (in diesem Artikel) einschließlich der Einstellungen für kürzlichen Änderungen.
    
## <a name="step-1-review-the-prerequisites"></a>Schritt 1: Überprüfen der erforderlichen Komponenten

- Stellen Sie sicher, dass Ihre Organisation [Office 365 erweiterte Schutz](office-365-atp.md)verfügt.
    
- Stellen Sie sicher, dass Sie die erforderlichen Berechtigungen verfügen. Um ATP Richtlinien definieren (oder bearbeiten), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen zugewiesen werden: <br>

    |Rolle  |WHERE/wie zugewiesen.  |
    |---------|---------|
    |Office 365 globaler Administrator |Die Person, die zum Erwerben von Office 365 angemeldet ist ein globaler Administrator in der Standardeinstellung. (Siehe [zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) , um mehr zu erfahren.)         |
    |Office 365-Sicherheitsadministrator |Administrationscenter ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
    |Verwaltung von Exchange Online-Organisation |Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

- Stellen Sie sicher, dass Office-Clients konfiguriert sind, um [Moderne Authentifizierung](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) zu verwenden (Dies ist für sichere Links ATP Schutz in Office-Dokumente).
    
- [Informieren Sie sich über Richtlinienoptionen ATP sichere Links](#learn-about-atp-safe-links-policy-options) (in diesem Artikel). 

- Können Sie bis zu 30 Minuten für die neue oder aktualisierte Richtlinie in allen Office 365-Rechenzentren verteilen.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>Schritt 2: Die sichere Links ATP-Richtlinie, die für alle Benutzer gilt definieren (oder Lesen)

Wenn Sie [Office 365 erweiterte Threat Protection](office-365-atp.md)haben, müssen Sie eine Standardrichtlinie ATP sichere Links, die für jede Person in Ihrer Organisation gilt. Stellen Sie sicher, um zu prüfen, und bei Bedarf bearbeiten Sie der Standardrichtlinie.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Richtlinie \> ** **Sichere Links**.
    
3. Klicken Sie im Abschnitt **Richtlinien, die für die gesamte Organisation gelten,** **Standard**wählen Sie aus, und wählen Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten hat einen Stift).<br/>![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für sichere Links Protection bearbeiten](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Geben Sie im Abschnitt **die folgenden URLs zu blockieren** eine oder mehrere URLs, die Sie Personen in Ihrer Organisation aus Vorsichtsmaßnahmen verhindern möchten. (Siehe [Richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).)
    
5. Im Abschnitt **Einstellungen, die für Inhalt mit Ausnahme der e-Mail gelten,** aktivieren (oder deaktivieren) die Optionen, die Sie verwenden möchten. (Es wird empfohlen, dass Sie alle Optionen auswählen.) 
    
6. Klicken Sie auf **Save**.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>Schritt 3: Sichere Links ATP-Richtlinien, die auf bestimmte e-Mail-Empfänger anzuwenden hinzufügen (oder bearbeiten)

Nachdem Sie überprüft (bearbeitet die Standardrichtlinie ATP sichere Links oder haben), die für alle Benutzer gilt, besteht der nächste Schritt zusätzliche Richtlinien definieren, die an bestimmte Empfänger anwenden können. Beispielsweise können Sie auf die Standardrichtlinie Ausnahmen angeben, indem Sie eine zusätzliche Richtlinie definieren. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Richtlinie**aus.
    
3. Wählen Sie **sichere Links**aus.
    
4. Wählen Sie im Abschnitt **Richtlinien, die auf bestimmte Empfänger anzuwenden** , **New** (neue Schaltfläche ähnelt ein Pluszeichen ( **+**)).<br/>![Wählen Sie neu aus, um eine sichere Links Richtlinie für bestimmte e-Mail-Empfänger hinzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Geben Sie den Namen, die Beschreibung sowie Einstellungen für Ihre Richtlinie an.<br/>**Beispiel:** Um eine Richtlinie namens "keine direkte Durchklick" eingerichtet, die keine Personen in eine bestimmte Gruppe in Ihrer Organisation auf bis zu einer bestimmten Website ohne ATP sichere Links Schutz zulässt, können Sie Folgendes angeben Einstellungen empfohlen: 
    
  - Geben Sie im Feld **Name den Namen** keine direkte Durchklick.
    
  - Geben Sie im Feld **Beschreibung** eine Beschreibung wie verhindert, dass Personen in bestimmte Gruppen von bis zu einer Website ohne Überprüfung ATP sichere Links auf.
    
  - Wählen Sie im Abschnitt **Wählen Sie die Aktion** **auf**.
    
  - Wählen Sie **Verwenden sichere Anlagen zu überprüfenden Inhalte zum Herunterladen**aus.
    
  - Wenn diese Option verfügbar ist, wählen Sie **Sichere Links zu innerhalb der Organisation gesendeten Nachrichten anwenden**.
    
  - Wählen Sie die **Benutzer über die ursprüngliche URL klicken können nicht**aus.
    
  - (Dieser Schritt ist optional.) Geben Sie im Abschnitt **Schreiben Sie die folgenden URLs nicht** eine oder mehrere URLs, die als sicher für Ihre Organisation gelten. (Siehe [Richten Sie eine benutzerdefinierte "Nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - **Angewendet auf** Sie im Abschnitt wählen Sie **der Empfänger ist Mitglied von**, und wählen Sie dann die Kontaktgruppen, die in der Richtlinie enthalten sein sollen. Wählen Sie **Hinzufügen**, und wählen Sie dann auf **OK**.
    
6. Klicken Sie auf **Save**.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>Schritt 4: Informationen Sie zu Richtlinienoptionen ATP sichere Links

Beim Einrichten oder Ihrer Richtlinien ATP sichere Links bearbeiten und sieht mehrere Optionen zur Verfügung. Für den Fall, dass Sie wissen möchten, was diese Optionen sind, werden in der folgenden Tabelle können Sie jeweils und dessen Effekt beschrieben. Beachten Sie, dass es zwei Hauptarten ATP sichere Links Richtlinien gibt, definieren oder bearbeiten:
- eine [Standardrichtlinie](#default-policy-options) , die für alle Benutzer gilt. 
- zusätzliche [Richtlinien, die für bestimmte Empfänger definiert sind](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>Standardoptionen für die Richtlinie

Standardoptionen für die Richtlinie gelten für alle Benutzer in Ihrer Organisation.

|Diese option  |Funktion  |
|---------|---------|
| **Die folgenden URLs zu blockieren** <br/>    | Ermöglicht Ihrem Unternehmen haben eine benutzerdefinierte Liste von URLs, die automatisch gesperrt sind. Wenn Benutzer eine URL in dieser Liste klicken, werden sie zu einer [Seite Warnung](atp-safe-links-warning-pages.md) weitergeleitet, die erklärt, warum die URL ausgeschlossen wird.<br/> Für Weitere Informationen finden Sie unter [richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links      |
| **Office 365 ProPlus, Office für iOS und Android (engl.)** <br/>    | Wenn diese Option ausgewählt ist, ATP sichere Links öffnen Schutz auf URLs in Dokumenten angewendet wird, die in Office 365 ProPlus (Word, Excel und PowerPoint unter Windows oder Mac OS), Office-Dokumente auf IOS- oder Android-Geräte, Visio 2016 unter Windows und Office Online (Word Online, Online PowerPoint, Excel Online und OneNote Online), sofern der Benutzer in Office 365 angemeldet hat. <br/><br/>Wenn Sie nur **Office 2016 unter Windows**angezeigt wird, klicken Sie dann die Feature-Updates nicht erreicht haben Ihre Office 365-Umgebung noch (und bald sind). Sichere Links ATP Protection betrifft bis zu diesem Zeitpunkt aus Word 2016, 2016 Excel, PowerPoint 2016 oder Visio 2016 unter Windows.            |
| **Verwalten Sie nicht, wenn Benutzer ATP sichere Links klicken** <br/>  | Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in Word, Excel, PowerPoint und Visio-Dokumenten wird nicht gespeichert.  <br/> |
|**Lassen Sie nicht über ATP sichere Links auf die ursprüngliche URL klicken Sie auf Benutzer** <br/> |Wenn diese Option ausgewählt ist, können nicht Benutzer hinter einer [Seite Warnung](atp-safe-links-warning-pages.md) auf eine URL fortgesetzt, die böswilligen werden bestimmt wird.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>Richtlinien, die auf bestimmte e-Mail-Empfänger anzuwenden

|Diese option  |Funktion  |
|---------|---------|
|**Off** <br/> |URLs überprüft in e-Mail-Nachrichten nicht.  <br/> Können Sie eine Ausnahmeregel, wie eine Regel zu definieren, die nicht URLs für eine bestimmte Gruppe von Empfängern in e-Mail-Nachrichten überprüft wird.  <br/> |
|**Klicken Sie auf** <br/> |URLs umschreibt Route Benutzern über ATP sichere Links Protection, wenn der Benutzer URLs in e-Mail-Nachrichten klicken.  <br/> Eine URL mit einer Liste der blockierten oder böswilliges URLs Toolparts überprüft.  <br/> |
|**Verwenden Sie sichere Anlagen um zu überprüfenden Inhalte zum Herunterladen** <br/> |Wenn diese Option ausgewählt ist, werden die URLs, die auf Inhalte zum Herunterladen zeigen überprüft.  <br/> |
|**Wenden Sie sichere Links auf innerhalb der Organisation gesendeten Nachrichten an** <br/> | Wenn diese Option aktiviert ist, wird ATP sichere Links Schutz auf e-Mails angewendet, die Nachrichten zwischen Personen in Ihrer Organisation, die e-Mail-Konten bereitgestellt in Office 365 gehostet werden.  <br/> |
|**Benutzer klickt auf nicht überwacht** <br/> |Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in e-Mail-Nachrichten von externen Absendern wird nicht gespeichert. Klicken Sie auf URL tracking für Links in e-Mail-Nachrichten innerhalb der Organisation gesendet wird derzeit nicht unterstützt.  <br/> |
|**Lassen Sie nicht über die ursprüngliche URL, klicken Sie auf Benutzer** <br/> |Wenn diese Option ausgewählt ist, können nicht Benutzer hinter einer [Seite Warnung](atp-safe-links-warning-pages.md) auf eine URL fortgesetzt, die böswilligen werden bestimmt wird.  <br/> |
|**Schreiben Sie die folgenden URLs nicht** <br/> |Lässt URLs unverändert. Hält eine benutzerdefinierte Liste von sicheren URLs, die keine Überprüfung für eine bestimmte Gruppe von e-Mail-Empfängern in Ihrer Organisation benötigen.  Einzelheiten finden Sie unter [Einrichten einer benutzerdefinierten "Nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) , einschließlich kürzlichen Änderungen an der Unterstützung für Platzhalter Sternchen (\*).<br/> |
   
## <a name="next-steps"></a>Nächste Schritte

Nachdem Ihre ATP sichere Links Richtlinien vorhanden sind, können Sie sehen, wie für Ihre Organisation ATP funktionsfähig ist, indem Sie Berichte anzeigen. Finden Sie in den folgenden Ressourcen, um mehr zu erfahren:

- [Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)

- [Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center](use-explorer-in-security-and-compliance.md)

Neue Features der ATP behalten. Besuchen Sie die [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) , und informieren Sie sich über [neue Features, die ATP hinzugefügt wird](office-365-atp.md#new-features-are-continually-being-added-to-atp).
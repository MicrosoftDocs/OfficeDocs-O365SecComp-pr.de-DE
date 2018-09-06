---
title: Einrichten von Richtlinien für Office 365 ATP sichere Links
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
description: Richten Sie Richtlinien für sichere Links mit Ihrer Organisation vor böswilligen Links in Word, Excel, PowerPoint und Visio-Dateien sowie in e-Mail-Nachrichten zu schützen.
ms.openlocfilehash: a0c88a81503555417c16501ec9283cf2316c6d09
ms.sourcegitcommit: a8884b9675559018e1fddec1c0cc2de0bc3bdde5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839975"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Einrichten von Richtlinien für Office 365 ATP sichere Links

[ATP sichere Links](atp-safe-links.md) , ein Feature von [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP), können Ihre Organisation vor böswilligen Links in Phishing und anderen Angriffen verwendet schützen. Wenn Sie die erforderlichen haben [in die Office 365-Sicherheit zugewiesenen Berechtigungen &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), ATP sichere Links Richtlinien einrichten, um sicherzustellen, dass beim Klicken auf Webadressen (URLs), Ihrer Organisation geschützt ist. Ihrer Richtlinien ATP sichere Links können in e-Mail-URLs und URLs in Office-Dokumenten überprüfen konfiguriert werden.
  
Neue Features werden ständig ATP sichere Links hinzugefügt:
  
- In spät Oktober 2017 ist erweitertem Schutz ATP sichere Links um URLs in e-Mail als auch in Office 365 ProPlus-Dokumenten, beispielsweise Word, Excel, PowerPoint, Windows, iOS und Android-Geräte und Visio-Dateien auf Windows-URLs zu übernehmen.
    
- März 2018 ab, ist sicherer Links ATP Schutz erweitert, um auf zwischen Personen in einer Organisation gesendeten e-Mails anwenden.
    
- Ende März 2018 ab, ist ATP sichere Links erweitertem Schutz um URLs in Office Online (Online Word, Excel Online, Online PowerPoint und OneNote Online) und Office 365 ProPlus unter Mac OS zuzuweisen.
    
- Im Mai 2018 beginnen, werden [Warnung Seiten](atp-safe-links-warning-pages.md) aktualisiert mit ein neues Farbschema, Weitere Informationen und die Möglichkeit, die auf einer Website ungeachtet der angegebenen Empfehlungen fortfahren. 

Neue Features hinzugefügt werden, müssen Sie möglicherweise Ihre vorhandenen ATP sichere Links Richtlinien anpassen.

## <a name="what-to-do"></a>Nächste Schritte 
  
1. [Überprüfen Sie die erforderlichen Komponenten](#review-the-prerequisites).
    
2. [Überprüfen und Bearbeiten der Standardrichtlinie für ATP sichere Links, die für alle Benutzer gilt](#define-an-atp-safe-links-policy-that-applies-to-everyone). Beispielsweise können Sie [die benutzerdefinierten blockierte URLs Liste für sichere Links ATP eingerichtet](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Hinzufügen einer Richtlinie für bestimmte e-Mail-Empfänger](#add-a-policy-for-specific-email-recipients), einschließlich der [Einrichtung von Ihrer benutzerdefinierten "Nicht rewrite" URLs Liste für sichere ATP-Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Informieren Sie sich über Richtlinienoptionen ATP sichere Links](#learn-about-atp-safe-links-policy-options) (in diesem Artikel) einschließlich der Einstellungen für kürzlichen Änderungen
    
## <a name="review-the-prerequisites"></a>Überprüfen Sie die erforderlichen Komponenten

- Stellen Sie sicher, dass Ihre Organisation [Office 365 erweiterte Schutz](office-365-atp.md)verfügt.
    
- Stellen Sie sicher, dass Sie die erforderlichen verfügen [über Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
- [Informieren Sie sich über Richtlinienoptionen ATP sichere Links](#learn-about-atp-safe-links-policy-options) (in diesem Artikel). 
    
- Können Sie bis zu 30 Minuten für die neue oder aktualisierte Richtlinie in allen Office 365-Rechenzentren verteilen.
    
## <a name="define-an-atp-safe-links-policy-that-applies-to-everyone"></a>Definieren einer Richtlinie für den sicheren ATP-Links, die für alle Benutzer gilt

Wenn Sie erweiterte Schutz in Office 365 Enterprise verwenden, müssen Sie eine Standardrichtlinie ATP sichere Links, die für jede Person in Ihrer Organisation gilt. Sie können Ihre Richtlinie in entweder das Wertpapier bearbeiten &amp; Compliance Center oder die Exchange-Verwaltungskonsole. **Es wird empfohlen, die Sicherheit &amp; Compliance Center zu lesen oder bearbeiten eine beliebige Richtlinie ATP**.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Richtlinie \> ** **Sichere Links**.
    
3. Klicken Sie im Abschnitt **Richtlinien, die für die gesamte Organisation gelten,** **Standard**wählen Sie aus, und wählen Sie dann auf **Bearbeiten** (die Schaltfläche Bearbeiten hat einen Stift). 
    
    ![Klicken Sie auf Bearbeiten, um die Standardrichtlinie für sichere Links Protection bearbeiten](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Geben Sie im Abschnitt **die folgenden URLs zu blockieren** eine oder mehrere URLs, die Sie Personen in Ihrer Organisation aus Vorsichtsmaßnahmen verhindern möchten. (Siehe [Richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).)
    
5. Im Abschnitt **Einstellungen, die für Inhalt mit Ausnahme der e-Mail gelten,** aktivieren (oder deaktivieren) die Optionen, die Sie verwenden möchten. (Es wird empfohlen, dass Sie alle Optionen auswählen.) 
    
6. Wählen Sie **Speichern**.
    
## <a name="add-a-policy-for-specific-email-recipients"></a>Hinzufügen einer Richtlinie für bestimmte e-Mail-Empfänger

Nachdem Sie die Richtlinie für alle Benutzer überprüft haben, sollten Sie zusätzliche Richtlinien für bestimmte Gruppen von e-Mail-Empfängern definieren. Dadurch können Sie Ausnahmen für die Standardrichtlinie angeben. Sie können entweder die Sicherheit von Richtlinien hinzufügen &amp; Compliance Center (empfohlen) oder die Exchange-Verwaltungskonsole. **Es wird empfohlen, die Sicherheit &amp; Compliance Center zu lesen oder bearbeiten eine beliebige Richtlinie ATP**.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. Wählen Sie im linken Navigationsbereich, klicken Sie unter **Threat Management** **Richtlinie**aus.
    
3. Wählen Sie **sichere Links**aus.
    
4. Wählen Sie im Abschnitt **Richtlinien, die auf bestimmte Empfänger anzuwenden** , **New** (neue Schaltfläche ähnelt ein Pluszeichen ( **+**)).
    
    ![Wählen Sie neu aus, um eine sichere Links Richtlinie für bestimmte e-Mail-Empfänger hinzufügen](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Geben Sie den Namen, die Beschreibung sowie Einstellungen für Ihre Richtlinie an.
    
    **Beispiel:** Um eine Richtlinie namens "keine direkte Durchklick" eingerichtet, die keine Personen in eine bestimmte Gruppe in Ihrer Organisation auf bis zu einer bestimmten Website ohne ATP sichere Links Schutz zulässt, können Sie Folgendes angeben Einstellungen empfohlen: 
    
  - Geben Sie im Feld **Name den Namen** keine direkte Durchklick.
    
  - Geben Sie im Feld **Beschreibung** eine Beschreibung wie verhindert, dass Personen in bestimmte Gruppen von bis zu einer Website ohne Überprüfung ATP sichere Links auf.
    
  - Wählen Sie im Abschnitt **Wählen Sie die Aktion** **auf**.
    
  - Wählen Sie **Verwenden sichere Anlagen zu überprüfenden Inhalte zum Herunterladen**aus.
    
  - Wenn diese Option verfügbar ist, wählen Sie **Sichere Links zu innerhalb der Organisation gesendeten Nachrichten anwenden**.
    
  - Wählen Sie die **Benutzer über die ursprüngliche URL klicken können nicht**aus.
    
  - (Dieser Schritt ist optional.) Geben Sie im Abschnitt **Schreiben Sie die folgenden URLs nicht** eine oder mehrere URLs, die als sicher für Ihre Organisation gelten. (Siehe [Richten Sie eine benutzerdefinierte "Nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - **Angewendet auf** Sie im Abschnitt wählen Sie **der Empfänger ist Mitglied von**, und wählen Sie dann die Kontaktgruppen, die in der Richtlinie enthalten sein sollen. Wählen Sie **Hinzufügen**, und wählen Sie dann auf **OK**.
    
6. Wählen Sie **Speichern**.
    
## <a name="learn-about-atp-safe-links-policy-options"></a>Erfahren Sie mehr über Richtlinienoptionen ATP sichere Links

Beim Einrichten oder eine Richtlinie für den sicheren Links ATP bearbeiten und sieht mehrere Optionen zur Verfügung. Für den Fall, dass Sie wissen möchten, was diese Optionen sind, werden in der folgenden Tabelle können Sie jeweils und dessen Effekt beschrieben. Beachten Sie, dass es zwei Hauptarten Richtlinien gibt, definieren oder bearbeiten: eine Standardrichtlinie, die für alle Benutzer gilt, und zusätzliche Richtlinien, die für bestimmte Empfänger definiert sind.
  
|**Für diese Richtlinie**|**Diese option**|**Funktion**|
|:-----|:-----|:-----|
|Standard (sobald definiert, die Standardrichtlinie für alle Benutzer in der Organisation)  <br/> |**Die folgenden URLs zu blockieren** <br/> |Ermöglicht Ihrem Unternehmen haben eine benutzerdefinierte Liste von URLs, die automatisch gesperrt sind. Wenn Benutzer eine URL in dieser Liste klicken, werden sie zu einer [Seite Warnung](atp-safe-links-warning-pages.md) weitergeleitet, die erklärt, warum die URL ausgeschlossen wird.<br/> Einzelheiten finden Sie unter [Einrichten einer benutzerdefinierten blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md) , beispielsweise neu hinzugefügte Unterstützung für bis zu drei Platzhalter Sternchen (\*).  <br/> |
|Standard  <br/> |**Office 365 ProPlus, Office für iOS und Android (engl.)** <br/> |Wenn diese Option ausgewählt ist, ATP sichere Links öffnen Schutz auf URLs in Dokumenten angewendet wird, die in Office 365 ProPlus (Word, Excel und PowerPoint unter Windows oder Mac OS), Office-Dokumente auf IOS- oder Android-Geräte, Visio 2016 unter Windows und Office Online (Word Online, Online PowerPoint, Excel Online und OneNote Online), sofern der Benutzer in Office 365 angemeldet hat. </br></br>Wenn Sie nur **Office 2016 unter Windows**angezeigt wird, klicken Sie dann die Feature-Updates nicht erreicht haben Ihre Office 365-Umgebung noch (und bald sind). Sichere Links ATP Protection betrifft bis zu diesem Zeitpunkt aus Word 2016, 2016 Excel, PowerPoint 2016 oder Visio 2016 unter Windows.           |
|Standard  <br/> |**Verwalten Sie nicht, wenn Benutzer ATP sichere Links klicken** <br/> |Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in Word, Excel, PowerPoint und Visio-Dokumenten wird nicht gespeichert.  <br/> |
|Standard  <br/> |**Lassen Sie nicht über ATP sichere Links auf die ursprüngliche URL klicken Sie auf Benutzer** <br/> |Wenn diese Option ausgewählt ist, können nicht Benutzer hinter einer [Seite Warnung](atp-safe-links-warning-pages.md) auf eine URL fortgesetzt, die böswilligen werden bestimmt wird.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Off** <br/> |URLs überprüft in e-Mail-Nachrichten nicht.  <br/> Können Sie eine Ausnahmeregel, wie eine Regel zu definieren, die nicht URLs für eine bestimmte Gruppe von Empfängern in e-Mail-Nachrichten überprüft wird.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Klicken Sie auf** <br/> |URLs umschreibt Route Benutzern über ATP sichere Links Protection, wenn der Benutzer URLs in e-Mail-Nachrichten klicken.  <br/> Eine URL mit einer Liste der blockierten oder böswilliges URLs Toolparts überprüft.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Verwenden Sie sichere Anlagen um zu überprüfenden Inhalte zum Herunterladen** <br/> |Wenn diese Option ausgewählt ist, werden die URLs, die auf Inhalte zum Herunterladen zeigen überprüft.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Wenden Sie sichere Links auf innerhalb der Organisation gesendeten Nachrichten an** <br/> | Wenn diese Option aktiviert ist, wird ATP sichere Links Schutz auf e-Mails angewendet, die Nachrichten zwischen Personen in Ihrer Organisation, die e-Mail-Konten bereitgestellt in Office 365 gehostet werden.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Benutzer klickt auf nicht überwacht** <br/> |Wenn diese Option ausgewählt ist, klicken Sie auf Daten für URLs in e-Mail-Nachrichten von externen Absendern wird nicht gespeichert. Klicken Sie auf URL tracking für Links in e-Mail-Nachrichten innerhalb der Organisation gesendet wird derzeit nicht unterstützt.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Lassen Sie nicht über die ursprüngliche URL, klicken Sie auf Benutzer** <br/> |Wenn diese Option ausgewählt ist, können nicht Benutzer hinter einer [Seite Warnung](atp-safe-links-warning-pages.md) auf eine URL fortgesetzt, die böswilligen werden bestimmt wird.  <br/> |
|Eine Richtlinie für bestimmte e-Mail-Empfänger erstellt  <br/> |**Schreiben Sie die folgenden URLs nicht** <br/> |Lässt URLs unverändert. Hält eine benutzerdefinierte Liste von sicheren URLs, die keine Überprüfung für eine bestimmte Gruppe von e-Mail-Empfängern in Ihrer Organisation benötigen.  Einzelheiten finden Sie unter [Einrichten einer benutzerdefinierten "Nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) , einschließlich kürzlichen Änderungen an der Unterstützung für Platzhalter Sternchen (\*).<br/> |
   
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[ATP sichere Links in Office 365](atp-safe-links.md)
  
[ATP sichere Anlagen in Office 365](atp-safe-attachments.md)
  
[Richten Sie eine benutzerdefinierte blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md)
  
[Richten Sie eine benutzerdefinierte "Nicht rewrite" URLs Liste verwenden ATP sichere Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)

[Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  


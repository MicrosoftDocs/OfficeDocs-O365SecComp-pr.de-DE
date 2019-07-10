---
title: Suchen und Freigeben von isolierten Nachrichten als Benutzer in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 05/19/2018
audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
description: 'Als Office 365 Benutzer können Sie Ihre eigenen Nachrichten mit Spamquarantäne auf zwei Arten verwalten: indem Sie auf Spambenachrichtigungen reagieren, die Sie direkt an Sie gesendet haben (wenn Ihr Administrator diese Funktion eingerichtet hat), oder indem Sie das Feature "Spamquarantäne" in der &amp; Security Compliance verwenden. Center.'
ms.openlocfilehash: 47c17e59f6f54d973eeaf761ecee6a1ac5a3dbba
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599351"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Suchen und Freigeben von isolierten Nachrichten als Benutzer in Office 365

Als Office 365 Benutzer können Sie Nachrichten, die an die Quarantäne gesendet wurden, nicht auf zwei Arten an Sie gesendet, sondern auf eine der folgenden beiden Methoden verwalten: indem Sie [auf Spambenachrichtigungen reagieren, die Sie direkt an Sie gesendet](use-spam-notifications-to-release-and-report-quarantined-messages.md) haben (sofern Ihr Administrator &amp; dies eingerichtet hat), oder indem Sie das Security Compliance Center verwenden. 
  
> [!NOTE]
> Wenn Sie ein Administrator sind, können Sie [isolierte Nachrichten](manage-quarantined-messages-and-files.md) für andere Personen in Ihrer Organisation verwalten. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Anzeigen von Nachrichten, die an die Quarantäne statt an Sie gesendet wurden

1. Melden Sie sich bei Office 365 an, und wechseln Sie mithilfe Ihres geschäftlichen oder Schul Kontos [zum Security and Compliance Center](go-to-the-securitycompliance-center.md) . 
    
2. Erweitern Sie auf der linken Seite **Bedrohungs Verwaltung**, wählen Sie **überprüfen**und dann **Quarantäne**aus.
    
    > [!TIP]
    > Wenn Sie direkt zur **Quarantäne** Seite im Security &amp; Compliance Center wechseln möchten, verwenden Sie die folgende URL: #a0[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Standardmäßig zeigt das Security &amp; Compliance Center alle e-Mail-Nachrichten an, die als Spam isoliert wurden. Die Nachrichten werden basierend auf dem **Datum** , an dem die Nachricht empfangen wurde, von der neuesten bis zur ältesten sortiert. **Absender**, **Betreff**und das Ablaufdatum (unter **Expires** ) werden ebenfalls für jede Nachricht angezeigt. Sie können nach einem Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren. 
  
Sie können eine Liste aller in Quarantäne befindlichen Nachrichten anzeigen, oder Sie können nach bestimmten Nachrichten durch Filtern suchen. Sie können nur Massenvorgänge für bis zu 100 Elemente ausführen, sodass das Filtern auch dazu beitragen kann, Ihr Resultset zu reduzieren, wenn Sie mehr als das haben. Sie können Nachrichten schnell nach einem einzelnen Quarantäne Grund filtern, indem Sie eine Option aus der Dropdownliste auswählen. Zu den Optionen gehören:
  
- Als Spam identifizierte e-Mails. Diese unter Quarantäne gestellten Nachrichten werden standardmäßig angezeigt.
    
- Als Massen-e-Mail bezeichnete e-Mail.
    
Nachdem Sie eine bestimmte isolierte Nachricht gefunden haben, klicken Sie auf die Nachricht, um Details dazu anzuzeigen, und führen Sie Aktionen aus. Sie können die Nachricht in Ihrem Postfach freigeben, die Nachricht in einer Vorschau anzeigen, die Nachricht herunterladen oder die Nachricht sofort aus der Quarantäne löschen.
  
> [!NOTE]
> Sie müssen über Administratorberechtigungen in Office 365 verfügen, damit Sie mit Nachrichten in Quarantäne arbeiten können, die an andere Benutzer gesendet wurden. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>So filtern und suchen Sie Nachrichten in Quarantäne

Wenn Sie viele isolierte Elemente haben, können Sie die Zahl auf eine verwaltbare Menge reduzieren, indem Sie Sie filtern.
  
1. Wählen Sie auf der Seite **Quarantäne** aus, ob Sie **Spam** -oder **Massen** Quarantäne Nachrichten anzeigen möchten. 
    
2. Wählen Sie unter **Ergebnisse sortieren nach**eine beliebige Kombination von Bedingungen aus, indem Sie den entsprechenden Filter oder Filter festlegen (Sie können zu diesem Zeitpunkt keine Platzhalter verwenden). Es gibt mehrere Bedingungen, die Sie auswählen können, einschließlich der folgenden:
    
  - **Nachrichten-ID** Verwenden Sie diese Option, um eine bestimmte Nachricht auszuwählen, wenn Sie die Nachrichten-ID kennen. 
    
    Wenn beispielsweise eine bestimmte Nachricht von einem Benutzer in Ihrer Organisation gesendet oder dafür bestimmt wird, aber nie sein Ziel erreicht hat, können Sie mithilfe einer Nachrichtenablaufverfolgung nach der Nachricht suchen (siehe [Ausführen einer Nachrichtenablaufverfolgung und Anzeigen von Ergebnissen](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht an die Quarantäne gesendet wurde, weil Sie möglicherweise mit einer Nachrichtenfluss Regel übereinstimmt oder als Spam identifiziert wurde, können Sie diese Nachricht dann leicht in der Quarantäne finden, indem Sie die zugehörige Nachrichten-ID angeben. Stellen Sie sicher, dass die vollständige Zeichenfolge der Nachrichten-ID enthalten ist. Dies kann beispielsweise zu Spitzen\<\>Klammern () gehören:
    
    \<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Absender-e-Mail-Adresse** Wählen Sie aus, um nach einer einzelnen Absender-e-Mail-Adresse zu filtern. 
    
  - **E-Mail-Adresse** des Empfängers Wählen Sie aus, um nach einer einzelnen Empfänger-e-Mail-Adresse zu filtern. 
    
  - **Betreff** Geben Sie den Betreff einer e-Mail-Adresse ein, die Sie suchen möchten. 
    
  - **Datumsbereich** Sie können festlegen, dass nach dem Datum gefiltert wird, an dem die Nachricht an die Quarantäne gesendet wurde. Sie können das Datum oder einen Datumsbereich angeben, einschließlich der Uhrzeit. 
    
  - **Ablaufdatum** Um nach Ablaufdatum zu filtern, wählen Sie **Erweiterter Filter**aus. Sie können Nachrichten auswählen, die innerhalb der nächsten 24 Stunden ( **heute**) aus der Quarantäne gelöscht werden, innerhalb der nächsten 48 Stunden ( **nächsten 2 Tage**), innerhalb der nächsten Woche ( **Nächste 7 Tage**), oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.
    
    > [!IMPORTANT]
    > Standardmäßig werden Spam-und Massennachrichten 30 Tage lang in Quarantäne aufbewahrt. Dieser Zeitraum ist jedoch konfigurierbar, und der Administrator hat möglicherweise einen anderen Aufbewahrungszeitraum für die Quarantäne festgelegt. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen. 
  
## <a name="view-details-for-a-specific-message"></a>Anzeigen von Details für eine bestimmte Nachricht

Nachdem Sie eine Nachricht ausgewählt haben, wird eine Zusammenfassung der Nachrichteneigenschaften in einem Bereich auf der rechten Seite angezeigt.
  
- Nach **richten-ID:** Der eindeutige Bezeichner für die Nachricht. 
    
- **Absenderadresse:** Die Person, die die Nachricht gesendet hat. 
    
- **Erhalten:** Das Datum, an dem die Nachricht empfangen wurde. 
    
- **Betreff:** Der Text der Betreffzeile in der Nachricht. 
    
- **Quarantäne Grund:** Zeigt an, ob eine Nachricht als **Spam** oder **Massen**erkannt wurde.
    
- **Ablaufdatum:** Das Datum, an dem die Nachricht aus der Quarantäne gelöscht wird. 
    
- **Veröffentlicht an:** Alle e-Mail-Adressen (falls vorhanden), für die die Nachricht freigegeben wurde. 
    
- **Noch nicht freigegeben an:** Alle e-Mail-Adressen (falls vorhanden), für die die Nachricht nicht freigegeben wurde. Sie können die Option **Release** wählen, wenn Sie die Nachricht für Ihr Postfach freigeben möchten (Weitere Informationen zum Freigeben von Nachrichten im nächsten Abschnitt). 
    
Sie können noch mehr Details zur Nachricht erhalten, indem Sie eine der folgenden Optionen auswählen:
  
- **Nachrichtenkopfzeile anzeigen** Wählen Sie diese Option aus, um den Text der Nachrichtenkopfzeile anzuzeigen. Um die Kopfzeile eingehend zu analysieren, kopieren Sie den Text der Nachrichtenkopfzeile in die Zwischenablage, und wählen Sie dann **Microsoft Message Header Analyzer** aus, um zur Remote Verbindungs Untersuchung zu wechseln (Klicken Sie mit der rechten Maustaste, und wählen Sie in einer neuen Registerkarte öffnen aus, wenn Sie Office 365 nicht verlassen möchten Führen Sie diese Aufgabe aus). Fügen Sie die Kopfzeile der Nachricht auf der Seite im Abschnitt Nachrichtenkopf Analyse ein, und wählen Sie Kopfzeilen analysieren aus. 
    
- **Vorschau Nachricht** Ermöglicht das Anzeigen von Rohdaten-oder HTML-Versionen des Nachrichtentext Texts. In der HTML-Ansicht sind Links deaktiviert. 
    
## <a name="manage-your-quarantined-messages"></a>Verwalten von Nachrichten in Quarantäne

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben, haben Sie mehrere Optionen zum Verwalten von Nachrichten in der Quarantäne.
  
- Keine Aktion ausführen. Wenn Sie nichts tun, wird die Nachricht nach Ablauf von Office 365 automatisch gelöscht. Denken Sie daran, wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen.
    
- **Nachricht freigeben** Freigeben einer isolierten Nachricht (oder eines Satzes von Nachrichten), damit die Nachricht an Ihr Postfach gesendet wird. Wenn Sie eine Nachricht freigeben, haben Sie die Möglichkeit, die Nachricht an Microsoft zur Analyse zu melden. 
    
    Wenn Sie sich entscheiden, eine Nachricht zu melden, die auch als melden einer Nachricht als falsch positives Ergebnis bezeichnet wird, wird die Nachricht an das Microsoft-Spam Analyse Team gemeldet. Das Team bewertet und analysiert falsch positive Nachrichten, und je nach Analyseergebnis können die Filterregeln für den Dienst weiten Spam Inhalt so angepasst werden, dass diese Nachrichten durchlassen.
    
- **Nachricht herunterladen** Hiermit können Sie die Nachricht als EML-Datei herunterladen. Nachdem Sie eine Nachricht heruntergeladen haben, können Sie die EML-Datei überprüfen, indem Sie Ihren e-Mail-Client verwenden, bevor Sie die Nachricht freigeben. 
    
- **Aus Quarantäne entfernen** Löscht die Nachricht sofort aus der Quarantäne, ohne die Nachricht in Ihrem Postfach freizugeben. 
    


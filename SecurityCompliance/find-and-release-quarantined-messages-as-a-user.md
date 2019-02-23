---
title: Suchen und Freigeben von Nachrichten in Quarantäne als Benutzer in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
description: 'Als Office 365-Benutzer können Sie Ihre eigenen Nachrichten in Spamquarantäne auf zweierlei Weise verwalten: durch Antworten auf Spambenachrichtigungen, die Sie direkt an Sie gesendet haben (wenn Ihr Administrator diese Funktion eingerichtet hat) oder mithilfe der Spamquarantäne Funktion im Security &amp; Compliance Center.'
ms.openlocfilehash: acbf862f05a9282a26444b738400d29c03d07f1f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214995"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Suchen und Freigeben von Nachrichten in Quarantäne als Benutzer in Office 365

Als Office 365-Benutzer können Sie Nachrichten, die an die Quarantäne gesendet wurden, nicht auf eine der folgenden Weisen an Sie gesendet, sondern auf eine von zwei Arten verwalten: durch [Antworten auf Spambenachrichtigungen, die Sie direkt an Sie gesendet](use-spam-notifications-to-release-and-report-quarantined-messages.md) haben (wenn Ihr &amp; Administrator dies eingerichtet hat) oder mithilfe des Security Compliance Centers. 
  
> [!NOTE]
> Wenn Sie ein Administrator sind, können Sie [isolierte Nachrichten](manage-quarantined-messages-and-files.md) für andere Personen in Ihrer Organisation verwalten. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Anzeigen von Nachrichten, die an Quarantäne gesendet wurden, statt an Sie

1. Melden Sie sich bei Office 365 an, und wechseln Sie über Ihr Geschäfts-oder Schulkonto [zum Security and Compliance Center](go-to-the-securitycompliance-center.md) . 
    
2. Erweitern Sie im linken Bereich **Bedrohungs Verwaltung**, klicken Sie auf **Überarbeiten**, und wählen Sie dann **Quarantäne**aus.
    
    > [!TIP]
    > Um direkt zur **Quarantäne** Seite im Security &amp; Compliance Center zu wechseln, verwenden Sie die folgende URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Standardmäßig zeigt das Security &amp; Compliance Center alle e-Mail-Nachrichten an, die als Spam isoliert wurden. Die Nachrichten werden basierend auf dem **Datum** , an dem die Nachricht eingegangen ist, vom neuesten zum ältesten sortiert. **Absender**, **Betreff**und Ablaufdatum (unter Expires **** ) werden auch für jede Nachricht angezeigt. Sie können ein Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken. Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren. 
  
Sie können eine Liste aller isolierten Nachrichten anzeigen, oder Sie können nach bestimmten Nachrichten suchen, indem Sie filtern. Sie können nur Massenvorgänge mit bis zu 100 Elementen ausführen, sodass die Filterung auch dazu beitragen kann, Ihr Resultset zu reduzieren, wenn Sie mehr als das haben. Sie können Nachrichten für einen einzelnen Quarantäne Grund schnell filtern, indem Sie eine Option aus der Dropdownliste auswählen. Folgende Optionen sind verfügbar:
  
- Als Spam identifizierte E-Mail. Diese isolierten Nachrichten werden standardmäßig angezeigt.
    
- Als Massenmail identifizierte E-Mail.
    
Nachdem Sie eine bestimmte isolierte Nachricht gefunden haben, klicken Sie auf die Nachricht, um Details dazu anzuzeigen, und führen Sie Aktionen aus. Sie können die Nachricht in Ihrem Postfach freigeben, eine Vorschau der Nachricht anzeigen, die Nachricht herunterladen oder die Nachricht aus der Quarantäne sofort löschen.
  
> [!NOTE]
> Sie benötigen Administratorberechtigungen in Office 365, um mit isolierten Nachrichten zu arbeiten, die an andere Benutzer gesendet wurden. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>So filtern und finden Sie isolierte Nachrichten

Wenn Sie viele isolierte Elemente haben, können Sie die Anzahl auf einen verwaltbaren Satz reduzieren, indem Sie Sie filtern.
  
1. Wählen Sie auf der Seite **Quarantäne** aus, ob **Spam** -oder **Massen** Quarantäne Nachrichten angezeigt werden sollen. 
    
2. Wählen Sie unter **Ergebnisse sortieren nach**eine beliebige Kombination von Bedingungen aus, indem Sie den entsprechenden Filter oder Filter (Sie können derzeit keine Platzhalter verwenden) festlegen. Es gibt verschiedene Bedingungen, die Sie auswählen können, einschließlich der folgenden:
    
  - Nach **richten-ID** Verwenden Sie diese Option, um eine bestimmte Nachricht auszuwählen, wenn Sie die Nachrichten-ID kennen. 
    
    Wenn beispielsweise eine bestimmte Nachricht von einem Benutzer in Ihrer Organisation gesendet oder für diesen vorgesehen ist, aber nie sein Ziel erreicht hat, können Sie mithilfe einer Nachrichtenablaufverfolgung nach der Nachricht suchen (siehe [Ausführen einer Nachrichtenablaufverfolgung und Anzeigen der Ergebnisse](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht an die Quarantäne gesendet wurde, da Sie möglicherweise mit einer Nachrichtenfluss Regel übereinstimmt oder als Spam identifiziert wurde, können Sie diese Nachricht in Quarantäne finden, indem Sie Ihre Nachrichten-ID angeben. Stellen Sie sicher, dass Sie die vollständige Nachricht-ID-Zeichenfolge angeben. Dies kann beispielsweise eine eckige Klammer (\<\>) einschließen:
    
    \<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Absender-e-Mail-Adresse** Wählen Sie aus, um nach einer einzelnen Absender-e-Mail-Adresse zu filtern. 
    
  - **Empfänger-e-Mail-Adresse** Wählen Sie aus, um nach einer einzelnen Empfänger-e-Mail-Adresse zu filtern. 
    
  - **Betreff** Geben Sie den Betreff einer e-Mail-Adresse ein, die Sie suchen möchten. 
    
  - **Datumsintervall** Sie können nach dem Datum filtern, an dem die Nachricht an die Quarantäne gesendet wurde. Sie können das Datum oder einen Datumszeitraum angeben, einschließlich der Uhrzeit. 
    
  - **Ablaufdatum** Um nach Ablaufdatum zu filtern, wählen Sie **Erweiterte Filter**aus. Sie können Nachrichten auswählen, die innerhalb der nächsten 24 Stunden ( **heute**) innerhalb der nächsten 48 Stunden ( **Nächste 2 Tage**), innerhalb der nächsten Woche ( **nächsten 7 Tage**) aus der Quarantäne gelöscht werden sollen, oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.
    
    > [!IMPORTANT]
    > Standardmäßig werden Spam-und Massennachrichten für 30 Tage in Quarantäne aufbewahrt. Dieser Zeitraum ist jedoch konfigurierbar, und Ihr Administrator hat möglicherweise einen anderen Aufbewahrungszeitraum für Quarantäne festgelegt. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht mehr zurück erhalten. 
  
## <a name="view-details-for-a-specific-message"></a>Anzeigen von Details zu einer bestimmten Nachricht

Nachdem Sie eine Nachricht ausgewählt haben, wird eine Zusammenfassung der Nachrichteneigenschaften in einem Bereich auf der rechten Seite angezeigt.
  
- Nach **richten-ID:** Der eindeutige Bezeichner für die Nachricht. 
    
- **Absenderadresse:** Absender der Nachricht. 
    
- **Empfangen:** Das Datum, an dem die Nachricht empfangen wurde. 
    
- **Betreff:** Der Text der Betreffzeile in der Nachricht. 
    
- **Quarantäne Grund:** Zeigt an, ob eine Nachricht als **Spam** oder als **Bulk**identifiziert wurde.
    
- **Expires:** Das Datum, an dem die Nachricht aus der Quarantäne gelöscht wird. 
    
- **Veröffentlicht für:** Alle e-Mail-Adressen (sofern vorhanden), für die die Nachricht freigegeben wurde. 
    
- **Noch nicht freigegeben für:** Alle e-Mail-Adressen (sofern vorhanden), für die die Nachricht nicht freigegeben wurde. Sie können **Release** auswählen, wenn Sie die Nachricht in Ihrem Postfach freigeben möchten (Weitere Informationen zum Freigeben von Nachrichten im nächsten Abschnitt). 
    
Sie können weitere Details zu der Nachricht abrufen, indem Sie eine der folgenden Optionen auswählen:
  
- **Nachrichtenkopfzeile anzeigen** Wählen Sie diese Option aus, um den Nachrichten Kopftext anzuzeigen. Wenn Sie die Kopfzeile eingehend analysieren möchten, kopieren Sie den Text der Nachrichtenkopfzeile in die Zwischenablage, und wählen Sie dann **Microsoft Message Header Analyzer** aus, um zur Remote Verbindungs Untersuchung zu wechseln (Klicken Sie mit der rechten Maustaste, und wählen Sie in einer neuen Registerkarte öffnen aus, wenn Sie nicht möchten, dass Office 365 Führen Sie diese Aufgabe aus). Fügen Sie den Nachrichtenkopf im Abschnitt Nachrichtenkopf Analyse auf der Seite ein, und wählen Sie Kopfzeilen analysieren aus. 
    
- **Vorschau Nachricht** Ermöglicht das Anzeigen von RAW-oder HTML-Versionen des Nachrichtentext Texts. In der HTML-Ansicht sind Links deaktiviert. 
    
## <a name="manage-your-quarantined-messages"></a>Verwalten der isolierten Nachrichten

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben, haben Sie mehrere Optionen für die Verwaltung von Nachrichten in Quarantäne.
  
- Nichts tun. Wenn Sie nichts tun, wird die Nachricht nach Ablauf automatisch von Office 365 gelöscht. Denken Sie daran, wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück erhalten.
    
- **Release-Meldung** Gibt eine isolierte Nachricht (oder einen Satz von Nachrichten) frei, damit die Nachricht an Ihr Postfach gesendet wird. Wenn Sie eine Nachricht freigeben, haben Sie die Möglichkeit, die Nachricht zur Analyse an Microsoft zu melden. 
    
    Wenn Sie eine Nachricht melden, die auch als Meldung als falsch positives Ergebnis bezeichnet wird, wird die Nachricht an das Microsoft-Spam Analyse Team gemeldet. Das Team wertet und analysiert falsch positive Nachrichten, und je nach Ergebnis der Analyse können die Filterregeln des Dienst weiten Spam Inhalts angepasst werden, um diese Nachrichten zu ermöglichen.
    
- **Nachricht herunterladen** Ermöglicht das Herunterladen der Nachricht als EML-Datei. Nachdem Sie eine Nachricht heruntergeladen haben, können Sie die EML-Datei mit Ihrem e-Mail-Client überarbeiten, bevor Sie die Nachricht freigeben. 
    
- **Aus Quarantäne entfernen** Löscht die Nachricht sofort aus der Quarantäne, ohne die Nachricht für Ihr Postfach freizugeben. 
    


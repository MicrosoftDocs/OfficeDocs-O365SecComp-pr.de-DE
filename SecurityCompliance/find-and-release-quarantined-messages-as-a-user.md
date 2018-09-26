---
title: Finden und Freigeben von Nachrichten in Quarantäne als Benutzer in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
description: 'Als Office 365-Benutzer können Sie Ihre eigenen Nachrichten Spam-Quarantäne in einem der folgenden beiden Methoden verwalten: durch die Spam-Benachrichtigungen an Sie gesendeten Antworten (sofern Ihr Administrator diese Funktion eingerichtet hat), oder mithilfe der Spam-Quarantäne-Funktion in das Wertpapier &amp; Compliance Zentriert.'
ms.openlocfilehash: 728273838d9e592e17638638258f481830bc0bbe
ms.sourcegitcommit: f7fff49ae0b1c3056faa58d73c1070cb4e638fbf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018889"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Finden und Freigeben von Nachrichten in Quarantäne als Benutzer in Office 365

Als Office 365-Benutzer können Nachrichten, statt in Quarantäne gesendet, um Sie in einem der folgenden beiden Methoden gesendet wurden, verwaltet: [Reagieren auf Spam-Benachrichtigungen gesendet, um Sie direkt](use-spam-notifications-to-release-and-report-quarantined-messages.md) (sofern Ihr Administrator diese eingerichtet), oder mithilfe der Sicherheits &amp; Compliance Center. 
  
> [!NOTE]
> Wenn Sie ein Administrator sind, können Sie [Nachrichten in Quarantäne verwalten](manage-quarantined-messages-and-files.md) für andere Personen in Ihrer Organisation. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Anzeigen von Nachrichten, die in Quarantäne anstatt an Sie gesendet wurden

1. Melden Sie sich bei Office 365 aus, und [Wechseln Sie zu Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md) mit Ihrem Konto arbeiten oder Schule. 
    
2. Auf der linken Seite erweitern Sie **Threat Management**, wählen Sie **Überprüfen**und wählen Sie dann die **Quarantäne**.
    
    > [!TIP]
    > So rufen direkt an die Seite **Quarantäne** in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Standardmäßig wird die Sicherheit &amp; Compliance Center zeigt alle e-Mail-Nachrichten, die isoliert wurden als Spam. Die Nachrichten werden vom neuesten zum ältesten basierend auf dem **Datum** sortiert, die die Nachricht empfangen wurde. **Absender**, **Betreff**und das Ablaufdatum (unter **Expires** ) sind auch für jede Nachricht angezeigt. Sie können auf ein Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge rückgängig zu machen. 
  
Können Sie eine Liste aller Nachrichten in Quarantäne anzeigen, oder Sie können durch Filtern nach bestimmten Nachrichten suchen. Sie können nur tun Massenvorgänge für bis zu 100 Elemente so filtern auch das Resultset verringern kann, wenn Sie mehr als, haben. Sie können Nachrichten für einen einzelnen Quarantäne Grund schnell filtern, durch Auswählen einer Option in der Dropdown-Liste. Optionen gehören:
  
- E-Mail-Nachrichten, die als Spam identifiziert. Diese Nachrichten in Quarantäne werden standardmäßig angezeigt.
    
- E-Mails, die als Massen-Mail.
    
Wenn Sie eine bestimmte quarantänenachricht gefunden haben, klicken Sie auf die Nachricht an die Details zu ihr anzeigen und Aktionen. Sie können die Nachricht an Ihr Postfach freigeben, eine Vorschau die Nachricht, laden Sie die Nachricht oder Löschen der Nachricht aus der Quarantäne sofort.
  
> [!NOTE]
> Sie benötigen Administratorberechtigungen in Office 365 Nachrichten in Quarantäne entwickelt, die an andere Benutzer gesendet wurden. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Filtern und suchen Sie nach Nachrichten in Quarantäne

Wenn Sie viel ein isoliertes verfügen, können Sie die Anzahl an eine Reihe verwaltbaren durch Filtern reduzieren.
  
1. Wählen Sie auf der Seite **Quarantäne** Quarantäne gibt an, ob Sie **Spam** oder **Bulk** anzeigen möchten. 
    
2. Wählen Sie unter **Ergebnisse wie folgt sortieren**eine beliebige Kombination von Bedingungen durch Festlegen der entsprechenden Filter oder Filter (Platzhalter können zu diesem Zeitpunkt nicht verwendet). Es gibt mehrere Zustände, die Sie auswählen können, einschließlich der folgenden:
    
  - **Nachrichten-ID** Hiermit können Sie eine bestimmte Nachricht auswählen, wenn Sie wissen, dass die Nachrichten-ID. 
    
    Beispielsweise, wenn eine bestimmte Nachricht gesendeten oder für einen Benutzer in Ihrer Organisation vorgesehen ist, jedoch niemals ihr Ziel erreicht, Sie können Suchen für die Nachricht mithilfe einer nachrichtenablaufverfolgung (siehe [Ausführen einer nachrichtenablaufverfolgung und Anzeigen der Ergebnisse](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht gesendet wurde, vielleicht isoliert werden, da es eine e-Mail-Flussregel übereinstimmen oder als Spam identifiziert wurde, klicken Sie dann finden auf einfache Weise diese Nachricht in Quarantäne Sie durch Angeben der Nachricht-ID. Achten Sie darauf, dass die vollständige Nachrichten-ID-Zeichenfolge enthalten. Beispiele spitze Klammern (\<\>), zum Beispiel:
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **E-Mail-Adresse des Absenders** Wählen Sie zum Filtern nach einer einzelnen Absender e-Mail-Adresse. 
    
  - **E-Mail-Adresse des Empfängers** Wählen Sie zum Filtern nach einer einzigen e-Mail-Adresse. 
    
  - **Betreff** Geben Sie den Betreff einer e-Mail-Adresse, den Sie suchen möchten. 
    
  - **Datumsbereich** Sie können auch nach dem Datum zu filtern, die die Nachricht gesendet wurde, isoliert werden. Sie können das Datum oder einen Datumsbereich, einschließlich der Zeit angeben. 
    
  - **Ablaufdatum** Wählen Sie zum Filtern nach Ablaufdatum **Spezialfilter**. Sie können auswählen, Nachrichten, die innerhalb der nächsten 24 Stunden ( **heute**), innerhalb der nächsten 48 Stunden ( **nächsten 2 Tage**), innerhalb der nächsten Woche ( **nächsten 7 Tage**) aus der Quarantäne gelöscht werden, oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.
    
    > [!IMPORTANT]
    > Standardmäßig werden Spam und Massen Nachrichten in Quarantäne 30 Tage lang aufbewahrt. Jedoch in diesem Zeitraum ist konfigurierbar, und Ihre Admin möglicherweise eine unterschiedliche Quarantäne Aufbewahrungsdauer festgelegt haben. Sie können nicht Office 365 eine Nachricht aus der Quarantäne gelöscht, es wieder erhalten. 
  
## <a name="view-details-for-a-specific-message"></a>Anzeigen von Details für eine bestimmte Nachricht

Nachdem Sie eine Nachricht ausgewählt haben, sehen Sie eine Zusammenfassung der Nachrichteneigenschaften in einem Bereich auf der rechten Seite der Seite.
  
- **Nachrichten-ID:** Der eindeutige Bezeichner für die Nachricht. 
    
- **Absenderadresse:** Absender der Nachricht. 
    
- **Empfangen:** Das Datum, an das die Nachricht empfangen wurde. 
    
- **Betreff:** Der Text der Betreffzeile der Nachricht. 
    
- **Isolieren Grund:** Wird angezeigt, wenn eine Nachricht als **Spam** oder **Bulk**identifiziert wurde.
    
- **Läuft ab:** Das Datum, wenn die Nachricht aus der Quarantäne gelöscht werden. 
    
- **Für freigegeben:** Alle e-Mail-Adressen (falls vorhanden), die die Nachricht freigegeben wurde. 
    
- **Noch nicht auf freigegebene:** Alle e-Mail-Adressen (falls vorhanden), die die Nachricht nicht freigegeben wurde. Sie können **Version** auswählen, wenn Sie die Nachricht an Ihr Postfach (mehr über das Freigeben von Nachrichten im nächsten Abschnitt) freigeben möchten. 
    
Sie können noch mehr Details über die Nachricht abrufen, indem Sie eine der folgenden Optionen auswählen:
  
- **Nachrichtenkopf anzeigen** Wählen Sie diese Option, um den Nachrichtentext für die Kopfzeile finden Sie unter. Um die Kopfzeile im Detail zu analysieren, den Nachrichtentext-Header in die Zwischenablage kopieren und anschließend auf **Microsoft Message Headers Analyzer** , fahren Sie mit der Remote Connectivity Analyzer (mit der rechten Maustaste, und wählen Sie in einer neuen Registerkarte öffnen, wenn Sie nicht, lassen Sie Office 365 möchten Führen Sie diese Aufgabe). Fügen Sie die Nachrichtenkopfzeile auf die Seite im Abschnitt Nachricht Kopfzeile Analyzer, und wählen Sie Kopfzeilen analysieren. 
    
- **Meldung zur Vorschau** Ermöglicht die finden Sie unter Rohdaten oder HTML-Versionen der Textkörper der Nachricht. Links sind in der HTML-Ansicht deaktiviert. 
    
## <a name="manage-your-quarantined-messages"></a>Verwalten Sie Ihre Nachrichten in Quarantäne

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben, müssen Sie mehrere Optionen für die Verwaltung von Nachrichten in Quarantäne.
  
- Keine Aktion ausführen. Wenn Sie nichts tun entscheiden, wird die Nachricht von Office 365 automatisch nach Ablauf gelöscht werden. Beachten Sie, dass wenn eine Nachricht von Office 365 löscht aus der Quarantäne, Sie unwiederbringlich.
    
- **Mit Nachricht freigeben** Freigeben einer in Quarantäne verschobenen Nachricht (oder einen Satz von Nachrichten), damit die Nachricht an Ihr Postfach gesendet wird. Wenn Sie eine Nachricht freigeben, müssen Sie die Option aus, um die Nachricht zur Analyse an Microsoft gemeldet. 
    
    Wenn Sie angeben, dass eine Nachricht, auch als bezeichnet reporting einer Nachricht als falsch positives Ergebnis melden wird die Nachricht an den Microsoft-Spamanalyseteam gemeldet. Das Team wertet und analysiert false positive Nachrichten und, abhängig von den Ergebnissen der Analyse, können die Dienst geltende Spam Inhaltsfilterregeln, um diese Nachrichten über ermöglichen angepasst werden.
    
- **Herunterladen der Nachricht** Können Sie die Nachricht als EML-Datei herunterladen. Nachdem Sie eine Nachricht heruntergeladen haben, können Sie die EML-Datei mit Ihrem e-Mail-Client, bevor Sie die Nachricht überprüfen. 
    
- **Entfernen Sie aus der Quarantäne** Löscht die Nachricht sofort aus der Quarantäne ohne die Nachricht an Ihr Postfach freizugeben. 
    


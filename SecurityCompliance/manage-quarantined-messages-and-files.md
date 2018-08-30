---
title: Verwalten von in Quarantäne verschobenen Nachrichten und Dateien als Administrator in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
description: 'Als Administrator können Sie anzeigen, freigeben und melden false positive in Quarantäne verschobenen Nachrichten in Office 365. Sie können Richtlinien festlegen, sodass Office 365 Nachrichten filtert und sendet sie zur aus verschiedenen Gründen in Quarantäne:, da sie als Spam, Massen, Phishing, Schadsoftware erkannt wurden oder sie eine e-Mail-Flussregel übereinstimmen. '
ms.openlocfilehash: f30604da185b3455d89ae7c1206bda2149ef7778
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529502"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a>Verwalten von in Quarantäne verschobenen Nachrichten und Dateien als Administrator in Office 365

Als Administrator können Sie anzeigen, freigeben und Löschen von Nachrichten in Quarantäne und Bericht falsch positive Nachrichten in Quarantäne in Office 365. Sie können auch anzeigen, herunterladen und Löschen von isolierten Dateien von Advance Threat Protection (ATP) für SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams erfasst. Sie können Richtlinien festlegen, sodass Office 365 Nachrichten filtert und sendet sie zur aus verschiedenen Gründen in Quarantäne:, da sie als Spam, Massen-Mail Phishing-Mail, die mit Malware, identifiziert wurden oder da sie eine e-Mail-Flussregel übereinstimmen.
  
In der Standardeinstellung sendet Office 365 Phishing und Nachrichten mit Schadsoftware direkt zu isolieren. Andere gefilterten Nachrichten werden an Benutzer Junk-e-Mail-Ordner gesendet, es sei denn, Sie eine Richtlinie einrichten, die Nachrichten in Quarantäne gesendet.
  
Sie benötigen Administratorberechtigungen in Office 365 Nachrichten in Quarantäne entwickelt, die an andere Benutzer gesendet wurden und zur Arbeit mit Dateien in Quarantäne.
  
> [!IMPORTANT]
> Standardmäßig werden Spam, Massen, Malware, Phishing und Nachrichten, die isoliert wurden, da sie eine e-Mail-Flussregel übereinstimmen in Quarantäne für 30 Tage gespeichert. Sie können die Quarantäne Zeit in Anti-Spam-Einstellungen in das Wertpapier anpassen &amp; Compliance Center. Sie können nicht Office 365 eine Nachricht aus der Quarantäne gelöscht, es wieder erhalten. Wenn Sie möchten, können Sie die Beibehaltungsdauer für Nachrichten in Quarantäne in Ihrer Anti-Spam-Filterrichtlinien ändern. Weitere Informationen finden Sie unter [Festlegen von der Aufbewahrungszeitraum Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
  
## <a name="view-your-organizations-quarantined-messages"></a>Anzeigen von in Quarantäne verschobenen Nachrichten Ihrer Organisation

1. Melden Sie sich einer Arbeit oder Schule Konto, das globale in Ihrer Office-365organization Administratorrechten zu Office 365 und [Wechseln Sie zur Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md).
    
2. In der Liste auf der linken Seite erweitern Sie **Threat Management**, wählen Sie **Überprüfen**und wählen Sie dann die **Quarantäne**.
    
    > [!TIP]
    > So rufen direkt an die Seite **Quarantäne** in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
    Standardmäßig wird die Sicherheit &amp; Compliance Center zeigt alle e-Mail-Nachrichten, die isoliert wurden als Spam. Die Nachrichten werden vom neuesten zum ältesten basierend auf dem **Datum** sortiert, die die Nachricht empfangen wurde. **Absender**, **Betreff**und das Ablaufdatum (unter **Expires** ) sind auch für jede Nachricht angezeigt. Sie können auf ein Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge rückgängig zu machen. 
    
3. Können Sie eine Liste aller Nachrichten in Quarantäne anzeigen, oder Sie können das Resultset durch Filtern reduzieren. Sie können nur tun Massenvorgänge für bis zu 100 Elemente so filtern auch das Resultset verringern kann, wenn Sie mehr als, haben. Sie können Nachrichten für einen einzelnen Quarantäne Grund schnell filtern, durch Auswählen einer Option aus dem Filter am oberen Rand der Seite. Optionen gehören:
    
  - E-Mail als Spam identifiziert
    
  - E-Mail-Nachrichten unter Quarantäne gestellte e-Mails, da es eine Richtlinie festlegen, indem eine e-Mail-Flussregel (auch als Transportregeln bezeichnet) abgeglichen
    
  - E-Mails, die als Massen-mail
    
  - E-Mails, die als Phishing-mail
    
  - E-Mail-Nachrichten unter Quarantäne gestellte e-Mails, da es Schadsoftware enthält
    
Sie können außerdem als Administrator, alle für Ihre Organisation oder nur an Sie gesendeten Nachrichten zu filtern. Beenden der Benutzer kann nur Anzeigen von und Arbeiten mit Nachrichten, die an Sie gesendet.
  
Sie können auch Ihre Ergebnisse, um bestimmte Nachrichten suchen filtern. Tipps finden Sie unter [Filtern von Ergebnissen und hier finden unter Quarantäne gestellte Nachrichten und Dateien](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
Wenn Sie eine bestimmte quarantänenachricht gefunden haben, klicken Sie auf die Nachricht an die Details zu ihr anzeigen, und Aktionen Sie, wie die Nachricht an die Person Posteingang freigeben.
  
## <a name="view-your-organizations-quarantined-files"></a>Anzeigen von in Quarantäne verschobenen Dateien Ihres Unternehmens

1. Melden Sie sich einer Arbeit oder Schule Konto, das globale in Office 365-Organisation Administratorrechten zu Office 365 und [Wechseln Sie zur Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Auf der linken Seite erweitern Sie **Threat Management**, wählen Sie **Überprüfen**und wählen Sie dann die **Quarantäne**. 
    
    > [!TIP]
    > So rufen direkt an die Seite **Quarantäne** in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
3. Die Seite wird standardmäßig unter Quarantäne gestellte e-Mails angezeigt. Um isolierte Dateien anzuzeigen, legen Sie die Filter am oberen Rand der Seite zum Anzeigen von **Dateien**, unter Quarantäne gestellte e-Mails aufgrund von **Schadsoftware**. Sie benötigen Administratorberechtigungen in Office 365 mit isolierten Dateien arbeiten. 
    
4. Die Dateien werden vom neuesten zum ältesten basierend auf das Datum sortiert, die Datei unter Quarantäne gestellt wurde. Der **Benutzer** , der zuletzt geändert hat die Datei, den **Dienst** , der die Datei gebucht wurde und der **Dateiname**, **Speicherort**, **Dateigröße**, und das Ablaufdatum ( **Expires**) werden ebenfalls aufgelistet, für jede Datei. Sie können auf ein Feld sortieren, indem Sie auf eine Kopfzeile; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge rückgängig zu machen.
    
Können Sie eine Liste aller Dateien in Quarantäne anzeigen, oder Sie können bestimmte Dateien nach Filterung suchen. Genau wie Nachrichten nur möglich Massenvorgänge für bis zu 100 Elemente. Derzeit die Sicherheit &amp; Compliance Center können Sie anzeigen und Verwalten von Dateien, die in Quarantäne sind, da sie als mit Malware identifiziert wurden. Tipps finden Sie unter [Filtern von Ergebnissen und hier finden unter Quarantäne gestellte Nachrichten und Dateien](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a>Zum Filtern der Ergebnisse und hier finden unter Quarantäne gestellte Nachrichten und Dateien
<a name="BKMK_AdvSearch"> </a>

Je nach Ihrer Einstellungen möglicherweise viel isolierte Nachrichten und Dateien. Um eine bestimmte Nachricht oder eine Datei oder eine Gruppe von Nachrichten oder Dateien zu suchen, können Sie ein isoliertes basierend auf einer Vielzahl von Zusatzinformationen filtern.
  
1. Stellen Sie sicher, dass die oberste Zeile der Filter zum Anzeigen von Nachrichten oder Dateien entsprechend festgelegt ist, klicken Sie auf der Seite **Quarantäne** : 
    
  - Um für Dateien zu suchen, setzen Sie Filter zum Anzeigen von **Dateien** unter Quarantäne gestellte e-Mails aufgrund von **Schadsoftware**.
    
    Für Dateien unter Quarantäne zeigt die Seite alle isolierte Dateien nicht nur Ihre eigene, unabhängig davon, was Ihnen sagen It angezeigt.
    
  - Legen Sie zum Suchen von Nachrichten in Quarantäne Filter, um **Alle** anzeigen oder **nur meine** **e-Mail**. Für der letzte Filter wählen Sie dem Typ der in Quarantäne verschobenen Nachricht, die Sie gesuchten. Sie können für isolierte Nachrichten suchen, die als **Spam**für Nachrichten identifiziert wurden, die eine e-Mail-Fluss oder **Transportregel**, **Massen** -, **Phishing** Mail oder e-Mail ein, die **Schadsoftware**enthält abgeglichen.
    
2. Wählen Sie unter **Ergebnisse wie folgt sortieren**den oder die Filter, den, die Sie verwenden, um aus dem Dropdown-Listen suchen möchten. Die Optionen abhängig, ob Sie Dateien oder Nachrichten suchen. Platzhalter sind in Suchfelder zu diesem Zeitpunkt nicht unterstützt.
    
    Für Dateien und Nachrichten Sie können auswählen, Filtern nach dem Datum die Nachricht oder Datei in Quarantäne gesendet wurde. Sie können das Datum oder einen Datumsbereich, einschließlich der Zeit angeben. Sie können auch die Suchergebnisse durch das Ablaufdatum filtern, auf dem die Datei oder die Nachricht aus der Quarantäne gelöscht wird oder eine Kombination von Filtern können. Um nach Ablaufdatum suchen, wählen Sie **Erweiterte Filter**. Unter **Expires**können Sie auswählen, Nachrichten, die innerhalb der nächsten 24 Stunden ( **heute**), innerhalb der nächsten 48 Stunden ( **nächsten 2 Tage**), innerhalb der nächsten Woche ( **nächsten 7 Tage**) aus der Quarantäne gelöscht werden, oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.
    
    Für Nachrichten müssen Sie die folgenden zusätzlichen Optionen:
    
  - **Nachrichten-ID**. Hiermit können Sie um eine bestimmte Nachricht zu identifizieren, wenn Sie wissen, dass die Nachrichten-ID. 
    
    Beispielsweise, wenn eine bestimmte Nachricht gesendeten oder für einen Benutzer in Ihrer Organisation vorgesehen ist, jedoch niemals ihr Ziel erreicht, Sie können Suchen für die Nachricht mithilfe einer nachrichtenablaufverfolgung (siehe [Ausführen einer nachrichtenablaufverfolgung und Anzeigen der Ergebnisse](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht gesendet wurde, vielleicht isoliert werden, da es eine e-Mail-Flussregel übereinstimmen oder als Spam identifiziert wurde, klicken Sie dann finden auf einfache Weise diese Nachricht in Quarantäne Sie durch Angeben der Nachrichten-ID Achten Sie darauf, dass Sie die vollständige e-Mail-ID-Zeichenfolge enthalten. Beispiele spitze Klammern (\<\>), zum Beispiel:
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **E-Mail-Adresse des Absenders**. Wählen Sie zum Filtern nach einer einzelnen Absender e-Mail-Adresse. 
    
  - **E-Mail-Adresse des Empfängers**. Wählen Sie zum Filtern nach einer einzigen e-Mail-Adresse. 
    
  - **Betreff**. Geben Sie den Betreff einer e-Mail-Adresse, den Sie suchen möchten. Platzhaltersuche nicht unterstützt wird, müssen Sie den gesamten Betreff der Nachricht für die Suche verwendet, damit die Nachricht in den Ergebnissen zurückgegeben. Die Suche wird nicht beachtet. 
    
## <a name="view-details-about-quarantined-messages-and-files"></a>Anzeigen von Details zu isolierte Nachrichten und Dateien
<a name="BKMK_ViewDetails"> </a>

Bei der Auswahl eines Elements in der Quarantäneliste angezeigt werden, sehen Sie eine Zusammenfassung der seine Eigenschaften im **Detailbereich** auf der rechten Seite des Wertpapiers &amp; Compliance Center. 
  
 **Details für isolierte Nachrichten angezeigt**
  
- **Nachrichten-ID**. Der eindeutige Bezeichner für die Nachricht. 
    
- **Adresse des Absenders**. Absender der Nachricht. 
    
- **Empfangen**. Das Datum und die Zeit, die die Nachricht empfangen wurde. 
    
- **Betreff**. Der Text der Betreffzeile der Nachricht. 
    
- **Typ**. Wird angezeigt, wenn eine Nachricht als **Spam**, **Massen**, **Phishing**, abgeglichen eine Regel für e-Mail-Fluss ( **Transportregel**) oder als mit **Schadsoftware**erkannt wurde identifiziert wurde.
    
- **Läuft ab**. Datum und Uhrzeit, wann die Nachricht automatisch aus der Quarantäne gelöscht werden. 
    
- **Für freigegeben**. Alle e-Mail-Adressen (falls vorhanden), die die Nachricht freigegeben wurde. 
    
- **Für die noch nicht freigegeben**. Alle e-Mail-Adressen (falls vorhanden), die die Nachricht nicht noch freigegeben wurde. 
    
 **Details für isolierte Dateien angezeigt**
  
- **Dateiname** Der Name der Datei in Quarantäne. 
    
- **Websitepfad** URL, die den Speicherort der Datei in Office 365 definiert. 
    
- **Erkannt Datum / Uhrzeit** Das Datum und die Zeit, die die Datei unter Quarantäne gestellt wurde. 
    
- **Läuft ab** Das Datum, wenn die Nachricht aus der Quarantäne gelöscht werden. 
    
- **Erkannte durch** Die Methode zum Erkennen von Schadsoftware in der Datei verwendet. Dies kann ATP (Erweiterter Schutz) oder von Microsoft Anti-Malware Engine sein. 
    
- **Veröffentlicht** Beschreibt, unabhängig davon, ob die Datei freigegeben wurde. 
    
- **Name der Schadsoftware** Familie und der Name der Schadsoftware erkannt wird, in der Datei. 
    
- **Dokument-ID** Ein eindeutiger Bezeichner für das Dokument. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **Organisation** Ihre Organisation die eindeutige ID in Office 365. 
    
- **Geändert von** Das arbeiten oder Schule Konto des Benutzers, der die Datei zuletzt geändert wurde. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **SHA256-Hash** Den Hash der Datei. Sie können dies zum Nachschlagen von anderen Reputation speichern, die möglicherweise oder untersuchen, wo die Datei in Ihrer Umgebung möglicherweise. 
    
## <a name="managing-messages-and-files-in-quarantine"></a>Verwalten von Nachrichten und Dateien in Quarantäne
<a name="BKMK_ManageQuarantinedItem"> </a>

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben Sie mehrere Optionen für die Verwaltung von Nachrichten in Quarantäne.
  
- Keine Aktion ausführen. Wenn Sie nichts tun entscheiden, wird die Nachricht von Office 365 automatisch nach Ablauf gelöscht werden. Standardmäßig werden Spam, Massen, Malware, Phishing und Nachrichten unter Quarantäne gestellte e-Mails, da sie eine e-Mail-Flussregel übereinstimmen in Quarantäne für 30 Tage gespeichert. Sie können nicht Office 365 eine Nachricht aus der Quarantäne gelöscht, es wieder erhalten. Wenn Sie möchten, können Sie die Aufbewahrungsdauer für Nachrichten in Quarantäne ändern, indem Sie die Einstellung **Spam für (Tage) aufbewahren** in Ihrer Anti-Spam-Richtlinien konfigurieren. Weitere Informationen finden Sie unter [Festlegen von der Aufbewahrungszeitraum Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
    
- **Nachrichtenkopf anzeigen** Wählen Sie diesen Link, um den Nachrichtentext für die Kopfzeile finden Sie unter. Um die Kopfzeile im Detail zu analysieren, den Nachrichtentext-Header in die Zwischenablage kopieren und anschließend auf **Microsoft Message Headers Analyzer** , fahren Sie mit der Remote Connectivity Analyzer (mit der rechten Maustaste, und wählen Sie **in einer neuen Registerkarte geöffnet** , wenn Sie nicht, lassen Sie Office möchten 365 zum Abschließen dieser Aufgabe). Fügen Sie die Nachrichtenkopfzeile auf die Seite im Abschnitt Nachricht Kopfzeile Analyzer, und wählen Sie **Kopfzeilen analysieren**.
    
- **Meldung zur Vorschau** Ermöglicht die finden Sie unter Rohdaten oder HTML-Versionen der Textkörper der Nachricht. Links sind in der HTML-Ansicht deaktiviert. 
    
- **Nachricht herunterladen** , oder **Laden Sie die Datei**. Wählen Sie diese Option, um eine Kopie der Nachricht oder eine Datei auf Ihrem lokalen Gerät herunterladen. Sie müssen sicherstellen, dass Sie verstehen die Risiken im Zusammenhang mit Elementen aus der Quarantäne heruntergeladen wurde, bevor Sie dazu berechtigt sind. Nachrichten werden im EML-Format in einem Ordner gespeichert, die von die Ihnen angegebenen. Unter Quarantäne gestellte Dateien werden im Originalformat gespeichert.
    
- **Löschen** Wenn Sie möchten, können Sie sofort eine isolierte Element (oder Satz Elemente) anstelle von Warten auf das Ablaufdatum Festlegen von Office 365 löschen. Zum Löschen einer Nachricht oder Datei in der Quarantäne-Liste, wählen Sie das Element, und wählen Sie dann auf **Löschen**. Um mehrere Elemente gleichzeitig zu löschen, aktivieren Sie das Kontrollkästchen links neben der Elemente in der Quarantäne-Liste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** **ausgewählte Nachrichten löschen** oder **Löschen von ausgewählten Dateien**.
    
- **Version** Freigeben Sie einer isolierten Element (oder einen Satz von Elementen) und die Elemente als fälschlicherweise unter Quarantäne gestellte (falsch positive Ergebnisse) an Microsoft. 
    
    Zum Freigeben und Melden von einer einzelnen Nachricht oder Datei, in der Quarantäneliste wählen Sie des Elements aus, und wählen Sie **Datei** oder **Freigeben Nachricht**. Auf der nächsten Seite stellen Sie sicher, dass **Berichtnachrichten an Microsoft zur Analyse** oder **Berichtsdateien an Microsoft zur Analyse** ausgewählt ist. 
    
    Um mehrere Elemente gleichzeitig freizugeben, aktivieren Sie das Kontrollkästchen links neben der Elemente in der Quarantäne-Liste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** **Release-Dateien** oder **Freigeben von Nachrichten**. Auf der nächsten Seite stellen Sie sicher, dass **Berichtnachrichten an Microsoft zur Analyse** oder **Berichtsdateien an Microsoft zur Analyse** ausgewählt ist. 
    
Wenn Sie Nachrichten freigeben möchten, sollten Sie Folgendes beachten:
  
- Wenn Sie eine Massen-Version von mehrere Nachrichten gleichzeitig ausführen, werden die Nachrichten an alle Empfänger ursprünglich identifizierten freigegeben. Wenn Sie nur Nachrichten nur an bestimmte Empfänger freigeben möchten, müssen Sie die Nachrichten eines zu einem Zeitpunkt freigeben und die Empfänger einzeln zu identifizieren.
    
- Eine Nachricht kann nicht mehr als einmal an den gleichen Empfänger freigegeben werden muss.
    
- Wenn Sie eine Nachricht an mehrere Empfänger freigegeben sind, werden nur Empfänger, die zuvor nicht die Nachricht erhalten haben in der Liste der potenziellen Empfänger angezeigt.
    
- Bei der Auswahl Unwichtigstes falsch positive Ergebnisse, wenn die Nachricht oder Nachrichten, die Sie freigeben, als Spam, Massen, Phishing oder als Benutzer mit Malware isoliert wurden, wird die Nachricht auch die Microsoft-Spamanalyseteam gemeldet werden. Das Team bewerten und analysieren die Nachricht wird, und, abhängig von den Ergebnissen der Analyse, die gesamte Service Spam Inhaltsfilterregeln geändert werden, um die Nachricht über ermöglichen.
    
## <a name="setting-the-quarantine-retention-period"></a>Festlegen der Aufbewahrungszeitraum Quarantäne
<a name="BKMK_ModQuarantineTime"> </a>

Sie können konfigurieren, wie lange Nachrichten und Dateien bleibt in Quarantäne, bevor diese ablaufen. Standardmäßig werden ein isoliertes 30 Tage gespeichert. Sie konfigurieren Sie diese Einstellung für jede Richtlinie, die Sie erstellen. Sie können auch den Wert für die Standardrichtlinie, wie in diesem Artikel beschrieben ändern. 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a>So ändern Sie die Quarantäne Aufbewahrungsdauer für die Standardrichtlinie für Spam-Filter in die Sicherheit und Compliance Center

1. Melden Sie sich einer Arbeit oder Schule Konto, das globale in Office 365-Organisation Administratorrechten zu Office 365 und [Wechseln Sie zur Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Auf der linken Seite erweitern Sie **Threat Management**, wählen Sie **Richtlinie**aus, und wählen Sie dann **Anti-Spam**. 
    
    > [!TIP]
    > So rufen direkt auf der Seite **Anti-Spam** in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)
  
3. Wählen Sie **benutzerdefinierte** zum Anzeigen der Registerkarte **Benutzerdefinierte Einstellungen** . 
    
4. Erweitern Sie die Zeile **Spam-Filter Standardrichtlinie (immer ON)** . 
    
5. Wählen Sie **Richtlinie bearbeiten**. Die Einstellungen für die Standardrichtlinie für Spam-Filter werden in eine neue Seite angezeigt.
    
6. Erweitern Sie **Spam und Massen-Aktionen**.
    
7. Geben Sie unter **Quarantäne**in das Textfeld **beibehalten Spam für (Tage)** die Zeitspanne, die Office 365-Nachrichten und Dateien in Quarantäne beibehalten werden soll. Der Standardwert ist 30 Tage. Dies ist auch das Maximum. 
    
8. Wählen Sie **Speichern**.
    


---
title: Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
description: 'Als Administrator können Sie falsch positiv isolierte Nachrichten in Office 365 anzeigen, freigeben und melden. Sie können Richtlinien so einrichten, dass Office 365 Nachrichten filtert und Sie aus verschiedenen Gründen an die Quarantäne sendet: da Sie als Spam, Massen, Phishing, Schadsoftware oder als Übereinstimmung mit einer Nachrichtenfluss Regel identifiziert wurden. '
ms.openlocfilehash: d62aded09f3560de6ba4485757c1bb5ce3f8cb6d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219195"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a>Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365

Als Administrator können Sie isolierte Nachrichten anzeigen, freigeben und löschen sowie falsch positiv isolierte Nachrichten in Office 365 melden. Sie können auch isolierte Dateien, die von Advance Threat Protection (ATP) für SharePoint Online, OneDrive for Business und Microsoft Teams erfasst wurden, anzeigen, herunterladen und löschen. Sie können Richtlinien so einrichten, dass Office 365 Nachrichten filtert und Sie aus verschiedenen Gründen an die Quarantäne sendet: da Sie als Spam, Massenmail, Phishing-e-Mail, mit Schadsoftware oder mit einer Nachrichtenfluss Regel identifiziert wurden.
  
Standardmäßig sendet Office 365 Phishing-Nachrichten und Nachrichten mit Schadsoftware direkt in Quarantäne. Andere gefilterte Nachrichten werden an den Junk-e-Mail-Ordner der Benutzer gesendet, es sei denn, Sie richten eine Richtlinie für die Quarantäne ein.
  
Sie benötigen globale Administratorberechtigungen (GA) in Office 365, damit Sie mit isolierten Nachrichten arbeiten können, die an andere Benutzer gesendet wurden und mit Quarantänedateien arbeiten.
  
> [!IMPORTANT]
>Spam-, Massen-und Phishing-Nachrichten werden standardmäßig 30 Tage lang in Quarantäne gehalten. Nachrichten, die unter Quarantäne gestellt werden, da Sie einer e-Mail-Fluss Regel entsprechen, werden 7 Tage lang in Quarantäne gehalten. Schadsoftware-Nachrichten werden 15 Tage lang in Quarantäne aufbewahrt. Sie können die Spamquarantäne Zeit in den Antispam-Einstellungen im Security &amp; Compliance Center anpassen. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht mehr zurück erhalten. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten in ihren Anti-Spam-Filterrichtlinien ändern. Weitere Informationen finden Sie unter [Festlegen der Aufbewahrungsdauer für Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
  
## <a name="view-your-organizations-quarantined-messages"></a>Anzeigen der isolierten Nachrichten in Ihrer Organisation

1. Melden Sie sich bei einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365-Organisation bei Office 365 an, und [wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie in der Liste auf der linken Seite **Bedrohungs Verwaltung**, klicken Sie auf **Überarbeiten**, und wählen Sie dann **Quarantäne**aus.
    
    > [!TIP]
    > Um direkt zur **Quarantäne** Seite im Security &amp; Compliance Center zu wechseln, verwenden Sie die folgende URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
    Standardmäßig zeigt das Security &amp; Compliance Center alle e-Mail-Nachrichten an, die als Spam isoliert wurden. Die Nachrichten werden basierend auf dem **Datum** , an dem die Nachricht eingegangen ist, vom neuesten zum ältesten sortiert. **Absender**, **Betreff**und Ablaufdatum (unter Expires **** ) werden auch für jede Nachricht angezeigt. Sie können ein Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken. Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren. 
    
3. Sie können eine Liste aller isolierten Nachrichten anzeigen, oder Sie können das Resultset durch Filterung reduzieren. Sie können nur Massenvorgänge mit bis zu 100 Elementen ausführen, sodass die Filterung auch dazu beitragen kann, Ihr Resultset zu reduzieren, wenn Sie mehr als das haben. Sie können Nachrichten für einen einzelnen Quarantäne Grund schnell filtern, indem Sie eine Option aus dem Filter oben auf der Seite auswählen. Folgende Optionen sind verfügbar:
    
  - Als Spam identifizierte E-Mails
    
  - Isolierte E-Mails, da Sie einer Richtlinie mit einer e-Mail-Fluss Regel (auch als Transportregel bezeichnet) entspricht
    
  - Als Massenmail identifizierte E-Mail
    
  - Als Phishing-e-Mail identifizierte E-Mails
    
  - Isolierte E-Mails, da Sie Schadsoftware enthalten
    
Darüber hinaus können Sie als Administrator auswählen, ob alle Nachrichten für Ihre Organisation oder nur an Sie gesendete Nachrichten gefiltert werden sollen. Endbenutzer können nur Nachrichten anzeigen und daran arbeiten, die an Sie gesendet werden.
  
Sie können Ihre Ergebnisse auch filtern, um nach Nachrichten zu suchen. Tipps finden Sie unter [So filtern Sie Ergebnisse und suchen nach Nachrichten und Dateien in Quarantäne](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
Nachdem Sie eine bestimmte isolierte Nachricht gefunden haben, klicken Sie auf die Nachricht, um Details dazu anzuzeigen, und führen Sie Aktionen aus, wie das Freigeben der Nachricht an das Postfach eines Benutzers.
  
## <a name="view-your-organizations-quarantined-files"></a>Anzeigen der in Quarantäne gestellten Dateien Ihrer Organisation

1. Melden Sie sich bei einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365-Organisation bei Office 365 an, und [wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie im linken Bereich **Bedrohungs Verwaltung**, klicken Sie auf **Überarbeiten**, und wählen Sie dann **Quarantäne**aus. <br/>
    > [!TIP]
    > Um direkt zur **Quarantäne** Seite im Security &amp; Compliance Center zu wechseln, verwenden Sie die folgende URL: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
3. Standardmäßig werden auf der Seite isolierte e-Mail-Nachrichten angezeigt. Zum Anzeigen von isolierten Dateien legen Sie die Filter oben auf der Seite so fest, dass **Dateien**angezeigt werden, die aufgrund von **Schadsoftware**isoliert wurden. Sie benötigen Administratorberechtigungen in Office 365, um mit isolierten Dateien zu arbeiten. 
    
4. Die Dateien werden basierend auf dem Datum, an dem die Datei isoliert wurde, vom neuesten zum ältesten sortiert. Der **Benutzer** , der die Datei zuletzt geändert hat, der **Dienst** , für den die Datei bereitgestellt wurde, der **Dateiname**, der **Speicherort**, die **Dateigröße**und das Ablaufdatum ( **läuft ab**), werden auch für jede Datei aufgelistet. Sie können ein Feld sortieren, indem Sie auf eine Kopfzeile klicken. Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren.
    
Sie können eine Liste aller isolierten Dateien anzeigen, oder Sie können nach bestimmten Dateien suchen, indem Sie filtern. Genau wie Nachrichten können Sie nur Massenvorgänge mit bis zu 100 Elementen ausführen. Derzeit können Sie mit &amp; dem Security Compliance Center Dateien, die sich in Quarantäne befinden, anzeigen und verwalten, da Sie als Schadsoftware identifiziert wurden. Tipps finden Sie unter [So filtern Sie Ergebnisse und suchen nach Nachrichten und Dateien in Quarantäne](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a>So filtern Sie Ergebnisse und finden isolierte Nachrichten und Dateien
<a name="BKMK_AdvSearch"> </a>

Je nach Ihren Einstellungen kann es viele isolierte Nachrichten und Dateien geben. Um nach einer bestimmten Nachricht oder Datei oder einem Satz von Nachrichten oder Dateien zu suchen, können Sie isolierte Elemente basierend auf einer Vielzahl von zusätzlichen Informationen filtern.
  
1. Stellen Sie auf der Seite **Quarantäne** sicher, dass die oberste Filterreihe so festgelegt ist, dass Nachrichten oder Dateien angezeigt werden: 
    
      - Zum Suchen nach Dateien legen Sie die Filter so fest, dass **Dateien** , die **** aufgrund von Schadsoftware isoliert wurden, angezeigt werden.<br/>
    Bei isolierten Dateien werden alle isolierten Dateien angezeigt, nicht nur Ihre eigenen, unabhängig davon, was Sie anzeigen möchten.
    
      - Zum Suchen nach Nachrichten in Quarantäne legen Sie Filter so fest, dass **alle** oder **nur meine** **e-Mails**angezeigt werden. Für den letzten Filter wählen Sie den Typ der Quarantäne Nachricht aus, nach der Sie suchen. Sie können nach Nachrichten, die als **Spam**identifiziert wurden, nach Nachrichten suchen, die mit einer Nachrichtenfluss-oder **Transportregel**, **Massen** Mail, **Phishing** -e-Mails oder **** e-Mails mit Schadsoftware übereinstimmen.
    
2. Wählen Sie unter **Ergebnisse sortieren nach**den Filter aus, den Sie für die Suche verwenden möchten, in den Dropdownlisten. Die Optionen variieren je nachdem, ob Sie nach Dateien oder Nachrichten suchen. Platzhalter werden in Suchfeldern zu diesem Zeitpunkt nicht unterstützt.<br/><br/>Sowohl für Dateien als auch für Nachrichten können Sie nach dem Datum filtern, an dem die Nachricht oder Datei an die Quarantäne gesendet wurde. Sie können das Datum oder einen Datumszeitraum angeben, einschließlich der Uhrzeit. Sie können Ihre Suchergebnisse auch nach dem Ablaufdatum filtern, an dem die Datei oder Nachricht aus der Quarantäne gelöscht wird, oder Sie können eine Kombination aus Filtern verwenden. Wählen Sie **Erweiterter Filter**aus, um nach Ablaufdatum zu suchen. Unter **Expires**können Sie Nachrichten auswählen, die innerhalb der nächsten 24 Stunden ( **heute**), innerhalb der nächsten 48 Stunden ( **Nächste 2 Tage**), innerhalb der nächsten Woche ( **nächsten 7 Tage**) aus der Quarantäne gelöscht werden sollen, oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.<br/><br/>Für Nachrichten haben Sie die folgenden zusätzlichen Optionen:
    
      - Nach **richten-ID**. Verwenden Sie diese, um eine bestimmte Nachricht zu identifizieren, wenn Sie die Nachrichten-ID kennen.<br/><br/>Wenn beispielsweise eine bestimmte Nachricht von einem Benutzer in Ihrer Organisation gesendet oder für diesen vorgesehen ist, aber nie sein Ziel erreicht hat, können Sie mithilfe einer Nachrichtenablaufverfolgung nach der Nachricht suchen (siehe [Ausführen einer Nachrichtenablaufverfolgung und Anzeigen der Ergebnisse](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht an die Quarantäne gesendet wurde, da Sie möglicherweise mit einer Nachrichtenfluss Regel übereinstimmt oder als Spam identifiziert wurde, können Sie diese Nachricht in Quarantäne finden, indem Sie Ihre Nachrichten-ID angeben. Stellen Sie sicher, dass Sie die vollständige Nachricht-ID-Zeichenfolge angeben. Dies kann beispielsweise eine eckige Klammer (\<\>) einschließen:<br/>
    `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`
    
      - **Absender-e-Mail-Adresse**. Wählen Sie aus, um nach einer einzelnen Absender-e-Mail-Adresse zu filtern. 
    
      - **E-Mail-Adresse**des Empfängers. Wählen Sie aus, um nach einer einzelnen Empfänger-e-Mail-Adresse zu filtern. 
    
      - **Betreff**. Geben Sie den Betreff einer e-Mail-Adresse ein, die Sie suchen möchten. Da die Platzhaltersuche nicht unterstützt wird, müssen Sie den gesamten Betreff der Nachricht verwenden, damit die Suche die Nachricht in den Ergebnissen zurückgibt. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet. 
    
## <a name="view-details-about-quarantined-messages-and-files"></a>Anzeigen von Details zu isolierten Nachrichten und Dateien

Wenn Sie ein Element auswählen, das in der Quarantäneliste angezeigt wird, wird im **Detail** Bereich auf der rechten Seite des Security &amp; Compliance Centers eine Zusammenfassung seiner Eigenschaften angezeigt. 
  
**Für isolierte Nachrichten angezeigte Details**
  
- Nach **richten-ID**. Der eindeutige Bezeichner für die Nachricht. 
    
- **Absenderadresse**. Absender der Nachricht. 
    
- **Empfangen**. Datum und Uhrzeit der Übermittlung der Nachricht. 
    
- **Betreff**. Der Text der Betreffzeile der Nachricht. 
    
- **Type**. Zeigt an, ob eine Nachricht als **Spam**, als **Massen**-, **Phishing**-, Übereinstimmung mit einer e-Mail-Fluss Regel ( **Transport Regel**) oder als mit **Schadsoftware**gekennzeichnet erkannt wurde.
    
- **Läuft ab**. Das Datum und die Uhrzeit, zu denen die Nachricht automatisch aus der Quarantäne gelöscht wird. 
    
- **Veröffentlicht an**. Alle e-Mail-Adressen (sofern vorhanden), für die die Nachricht freigegeben wurde. 
    
- **Noch nicht für veröffentlicht**. Alle e-Mail-Adressen (sofern vorhanden), für die die Nachricht noch nicht freigegeben wurde. 
    
 **Details angezeigt für Quarantänedateien**
  
- **Dateiname** Der Name der Datei in Quarantäne. 
    
- **Websitepfad** URL, die den Speicherort der Datei in Office 365 definiert. 
    
- **ErkanntEs Datum/Uhrzeit** Das Datum und die Uhrzeit, zu der die Datei isoliert wurde. 
    
- **Läuft ab** Das Datum, an dem die Nachricht aus der Quarantäne gelöscht wird. 
    
- **Erkannt von** Die Methode zum Auffinden der Schadsoftware in der Datei. Dabei kann es sich entweder um ATP (Advanced Threat Protection) oder um das Antischadsoftware-Modul von Microsoft handeln. 
    
- **Veröffentlicht** Beschreibt, ob die Datei freigegeben wurde. 
    
- **Schadsoftware** Familie und Name der Schadsoftware, die in der Datei erkannt wurde. 
    
- **Dokument-ID** Ein eindeutiger Bezeichner für das Dokument. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **Organisation** Die eindeutige ID Ihrer Organisation in Office 365. 
    
- **Geändert von** Das Arbeits-oder Schulkonto des Benutzers, der die Datei zuletzt geändert hat. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **SHA256-Hash** Der Hash der Datei. Sie können dies verwenden, um andere Reputation Stores zu suchen, die Sie möglicherweise haben, oder um zu untersuchen, wo sich die Datei in Ihrer Umgebung befinden könnte. 
    
## <a name="managing-messages-and-files-in-quarantine"></a>Verwalten von Nachrichten und Dateien in Quarantäne
<a name="BKMK_ManageQuarantinedItem"> </a>

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben, haben Sie mehrere Optionen für die Verwaltung von Nachrichten in Quarantäne.
  
- Nichts tun. Wenn Sie nichts tun, wird die Nachricht nach Ablauf automatisch von Office 365 gelöscht. Spam, Massen, Schadsoftware, Phishing und Nachrichten, die in Quarantäne verschoben wurden, da Sie einer e-Mail-Fluss Regel entsprechen, werden 30 Tage lang in Quarantäne gehalten. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht mehr zurück erhalten. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten ändern, indem Sie die Einstellung **Spam für (Tage)** in ihren Anti-Spam-Richtlinien konfigurieren. Weitere Informationen finden Sie unter [Festlegen der Aufbewahrungsdauer für Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
    
- **Nachrichtenkopfzeile anzeigen** Klicken Sie auf diesen Link, um den Nachrichten Kopftext anzuzeigen. Wenn Sie die Kopfzeile eingehend analysieren möchten, kopieren Sie den Nachrichtenkopf in die Zwischenablage, und wählen Sie dann **Microsoft Message Header Analyzer** aus, um zur Remote Verbindungs Untersuchung zu wechseln (Klicken Sie mit der rechten Maustaste, und wählen Sie **in einer neuen Registerkarte öffnen** aus, wenn Sie Office nicht verlassen möchten. 365 zum Abschließen dieser Aufgabe). Fügen Sie den Nachrichtenkopf im Abschnitt Nachrichtenkopf Analyse auf der Seite ein, und wählen Sie **Kopfzeilen analysieren**aus.
    
- **Vorschau Nachricht** Ermöglicht das Anzeigen von RAW-oder HTML-Versionen des Nachrichtentext Texts. In der HTML-Ansicht sind Links deaktiviert. 
    
- **Herunterladen der Nachricht** oder **herunterladen der Datei**. Wählen Sie diese Option aus, um eine Kopie der Nachricht oder Datei auf Ihr lokales Gerät herunterzuladen. Sie müssen sich vergewissern, dass Sie die Risiken im Zusammenhang mit dem Herunterladen von Elementen aus der Quarantäne verstehen, bevor Sie dazu berechtigt sind. Nachrichten werden im eml-Format in einem von Ihnen angegebenen Ordner gespeichert. Isolierte Dateien werden im ursprünglichen Format gespeichert.
    
- **Löschen** Wenn Sie möchten, können Sie ein isoliertes Element (oder eine Gruppe von Elementen) sofort löschen, statt auf das von Office 365 festgelegte Ablaufdatum zu warten. Wenn Sie eine Nachricht oder Datei löschen möchten, wählen Sie in der Quarantäneliste das Element aus, und wählen Sie dann **Löschen**aus. Wenn Sie mehrere Elemente gleichzeitig löschen möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der daraufhin angezeigten Seite **Massenaktionen** die Option **ausgewählte Nachrichten löschen** oder **ausgewählte Dateien löschen**aus.
    
- **Release** Freigeben eines isolierten Elements (oder einer Gruppe von Elementen) und melden der Elemente als falsch isoliert (falsch positives Ergebnis) an Microsoft. 
    
    Wenn Sie eine einzelne Nachricht oder Datei freigeben und melden möchten, wählen Sie in der Quarantäneliste das Element aus **** , wählen Sie releasedatei oder **Release Message**aus. Stellen Sie sicher, dass auf der nächsten Seite die Option **Berichte an Microsoft für Analysen** oder **Berichtdateien an Microsoft zur Analyse** angezeigt wird. 
    
    Wenn Sie mehrere Elemente gleichzeitig freigeben möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der daraufhin angezeigten Seite **Massenaktionen** die Option **Dateien freigeben** oder **Nachrichten**freigeben aus. Stellen Sie sicher, dass auf der nächsten Seite die Option **Berichte an Microsoft für Analysen** oder **Berichtdateien an Microsoft zur Analyse** angezeigt wird. 
    
Beachten Sie beim Freigeben von Nachrichten Folgendes:
  
- Wenn Sie eine Massenfreigabe mehrerer Nachrichten gleichzeitig durchführen, werden die Nachrichten an alle ursprünglich identifizierten Empfänger freigegeben. Wenn Sie nur Nachrichten nur für bestimmte Empfänger freigeben möchten, müssen Sie die Nachrichten nacheinander freigeben und die Empfänger einzeln identifizieren.
    
- Eine Nachricht kann nicht mehr als einmal an denselben Empfänger freigegeben werden.
    
- Wenn Sie eine Nachricht an mehrere Empfänger freigeben, werden nur Empfänger, die die Nachricht zuvor nicht erhalten haben, in der Liste der potenziellen Empfänger angezeigt.
    
- Wenn Sie sich für die Meldung falsch positiver Ergebnisse entscheiden, wird die Nachricht auch dem Microsoft-Spam Analyse Team gemeldet, wenn die von Ihnen veröffentlichten Nachrichten als Spam, Massen, Phishing oder Schadsoftware isoliert wurden. Das Team bewertet und analysiert die Nachricht, und je nach Ergebnis der Analyse können die Filterregeln des Dienst weiten Spam Inhalts angepasst werden, um die Nachricht zu überprüfen.
    
## <a name="setting-the-quarantine-retention-period"></a>Festlegen der Aufbewahrungsdauer für Quarantäne
<a name="BKMK_ModQuarantineTime"> </a>

Sie können konfigurieren, wie lange Nachrichten und Dateien in Quarantäne bleiben, bevor Sie ablaufen. Standardmäßig werden isolierte Elemente 30 Tage lang aufbewahrt. Sie konfigurieren diese Einstellung für jede Richtlinie, die Sie erstellen. Sie können den Wert für die Standardrichtlinie auch ändern, wie in diesem Artikel beschrieben. 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a>So ändern Sie die Aufbewahrungsdauer für die Quarantäne für die standardmäßige Spamfilter Richtlinie im Security and Compliance Center

1. Melden Sie sich bei einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365-Organisation bei Office 365 an, und [wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie auf der linken Seite **Bedrohungs Verwaltung**, wählen Sie **Richtlinie**aus, und wählen Sie dann **Antispam**aus. <br/>
    > [!TIP]
    > Um direkt zur Seite **Anti-Spam** im Security &amp; Compliance Center zu wechseln, verwenden Sie die folgende URL: >[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)
  
3. Wählen Sie **Benutzerdefiniert** aus, um die Registerkarte **benutzerdefinierte Einstellungen** anzuzeigen. 
    
4. Erweitern Sie die **standardmäßige Spamfilter Richtlinie (Always on)** . 
    
5. Wählen Sie **Richtlinie bearbeiten**aus. Die Einstellungen für die standardmäßige Spamfilter Richtlinie werden auf einer neuen Seite angezeigt.
    
6. Erweitern Sie **Spam-und Massenaktionen**.
    
7. Geben Sie unter **Quarantäne**im Textfeld **Spam für (Tage) aufbewahren** die Zeitdauer ein, für die Office 365 Nachrichten und Dateien in Quarantäne speichern soll. Der Standardwert ist 30 Tage. Dies ist auch die maximale. 
    
8. Klicken Sie auf **Save**.
    


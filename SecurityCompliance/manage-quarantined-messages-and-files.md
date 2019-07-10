---
title: Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 09/05/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
description: 'Als Administrator können Sie in Office 365 falsch positive unter Quarantäne gestellte Nachrichten anzeigen, freigeben und melden. Sie können Richtlinien so einrichten, dass Nachrichten von Office 365 gefiltert und aus verschiedenen Gründen an die Quarantäne gesendet werden: weil Sie als Spam, Massen, Phishing, Schadsoftware oder als Übereinstimmung mit einer Nachrichtenfluss Regel identifiziert wurden. '
ms.openlocfilehash: 245068b7d3ec51cbca887883f791b19ea116731a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598801"
---
# <a name="manage-quarantined-messages-and-files-as-an-administrator-in-office-365"></a>Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365

Als Administrator können Sie in Office 365 unter Quarantäne gestellte Nachrichten anzeigen, freigeben und löschen sowie falsch positive Nachrichten in Quarantäne melden. Sie können auch isolierte Dateien anzeigen, herunterladen und löschen, die von Advance Threat Protection (ATP) für SharePoint Online, OneDrive für Unternehmen und Microsoft Teams erfasst werden. Sie können Richtlinien so einrichten, dass Nachrichten von Office 365 gefiltert und aus mehreren Gründen an die Quarantäne gesendet werden: weil Sie als Spam, Massen-e-Mails, Phishing-e-Mails, Schadsoftware oder aufgrund einer e-Mail-Fluss Regel identifiziert wurden.
  
Standardmäßig sendet Office 365 Phishingnachrichten und Nachrichten mit Schadsoftware direkt in Quarantäne. Andere gefilterte Nachrichten werden an den Junk-e-Mail-Ordner der Benutzer gesendet, es sei denn, Sie richten eine Richtlinie zum Senden an den Quarantänebereich ein.
  
Sie müssen über globale Administratorberechtigungen (GA) in Office 365 oder Sicherheitsadministrator im Security and Compliance Center verfügen, damit Sie mit in Quarantäne gestellten Nachrichten arbeiten können, die an andere Benutzer gesendet wurden, und um mit isolierten Dateien zu arbeiten.
  
> [!IMPORTANT]
>Standardmäßig werden Spam, Massen-und Phishing-Nachrichten 30 Tage lang in Quarantäne aufbewahrt. Nachrichten, die unter Quarantäne gestellt werden, weil Sie einer Nachrichtenfluss Regel entsprechen, werden für 7 Tage in Quarantäne aufbewahrt. Schadsoftware-Nachrichten werden 15 Tage lang in Quarantäne aufbewahrt. Sie können die Spamquarantäne Zeit in den Antispam-Einstellungen im Security &amp; Compliance Center anpassen. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten in ihren Anti-Spam-Filterrichtlinien ändern. Weitere Informationen finden Sie unter [Festlegen des Aufbewahrungszeitraums für die Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
  
## <a name="view-your-organizations-quarantined-messages"></a>Anzeigen der isolierten Nachrichten Ihrer Organisation

1. Melden Sie sich mit einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365 Organisation bei Office 365 [an, und wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie in der Liste auf der linken Seite die Option **Threat Management**, wählen Sie **überprüfen**, und wählen Sie dann **Quarantäne**aus.
    
    > [!TIP]
    > Wenn Sie direkt zur **Quarantäne** Seite im Security &amp; Compliance Center wechseln möchten, verwenden Sie die folgende URL: #a0[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
    Standardmäßig zeigt das Security &amp; Compliance Center alle e-Mail-Nachrichten an, die als Spam isoliert wurden. Die Nachrichten werden basierend auf dem **Datum** , an dem die Nachricht empfangen wurde, von der neuesten bis zur ältesten sortiert. **Absender**, **Betreff**und das Ablaufdatum (unter **Expires** ) werden ebenfalls für jede Nachricht angezeigt. Sie können nach einem Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren. 
    
3. Sie können eine Liste aller in Quarantäne gestellten Nachrichten anzeigen oder das Resultset durch Filterung reduzieren. Sie können nur Massenvorgänge für bis zu 100 Elemente ausführen, sodass das Filtern auch dazu beitragen kann, Ihr Resultset zu reduzieren, wenn Sie mehr als das haben. Sie können Nachrichten schnell nach einem einzelnen Quarantäne Grund filtern, indem Sie eine Option aus dem Filter oben auf der Seite auswählen. Zu den Optionen gehören:
    
  - Als Spam identifizierte e-Mails
    
  - E-Mail-Quarantäne, da Sie mit einer Richtlinie übereinstimmt, die von einer Nachrichtenfluss Regel festgelegt wurde (auch als Transportregel bezeichnet)
    
  - Als Massen-e-Mail bezeichnete e-Mail
    
  - Als Phishing-e-Mails identifizierte e-Mails
    
  - E-Mail-Quarantäne, weil Sie Schadsoftware enthält
    
Darüber hinaus können Sie als Administrator auswählen, dass alle Nachrichten für Ihre Organisation gefiltert werden oder nur an Sie gesendete Nachrichten. Endbenutzer können Nachrichten, die an Sie gesendet werden, nur anzeigen und bearbeiten.
  
Sie können Ihre Ergebnisse auch filtern, um nach bestimmten Nachrichten zu suchen. Tipps finden Sie unter [So filtern Sie Ergebnisse und suchen nach isolierten Nachrichten und Dateien](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
Nachdem Sie eine bestimmte isolierte Nachricht gefunden haben, klicken Sie auf die Nachricht, um Details dazu anzuzeigen und Aktionen durchführen zu können, wie das Freigeben der Nachricht an das Postfach eines anderen Benutzers.
  
## <a name="view-your-organizations-quarantined-files"></a>Anzeigen der isolierten Dateien in Ihrer Organisation

1. Melden Sie sich bei Office 365 mit einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365 Organisation an, und [wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie auf der linken Seite **Bedrohungs Verwaltung**, wählen Sie **überprüfen**und dann **Quarantäne**aus. <br/>
    > [!TIP]
    > Wenn Sie direkt zur **Quarantäne** Seite im Security &amp; Compliance Center wechseln möchten, verwenden Sie die folgende URL: #a0[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
3. Standardmäßig werden in der Seite isolierte e-Mail-Nachrichten angezeigt. Zum Anzeigen von isolierten Dateien legen Sie die Filter oben auf der Seite so fest, dass **Dateien**angezeigt werden, die aufgrund **Schadsoftware**isoliert wurden. Sie benötigen Administratorberechtigungen in Office 365, um mit isolierten Dateien zu arbeiten. 
    
4. Die Dateien werden basierend auf dem Datum, an dem die Datei isoliert wurde, von der neuesten bis zur ältesten sortiert. Der **Benutzer** , der die Datei zuletzt geändert hat, der **Dienst** , auf den die Datei geschrieben wurde, der **Dateiname**, der **Speicherort**, die **Dateigröße**und das **** Ablaufdatum (Expires) werden ebenfalls für jede Datei aufgelistet. Sie können nach einem Feld sortieren, indem Sie auf eine Kopfzeile klicken; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren.
    
Sie können eine Liste aller in Quarantäne befindlichen Dateien anzeigen, oder Sie können nach bestimmten Dateien suchen, indem Sie filtern. Genau wie Nachrichten können Sie nur Massenvorgänge für bis zu 100 Elemente ausführen. Derzeit können Sie mit &amp; dem Security Compliance Center Dateien anzeigen und verwalten, die sich in Quarantäne befinden, da Sie als Schadsoftware erkannt wurden. Tipps finden Sie unter [So filtern Sie Ergebnisse und suchen nach isolierten Nachrichten und Dateien](manage-quarantined-messages-and-files.md#BKMK_AdvSearch) in diesem Artikel. 
  
## <a name="to-filter-results-and-find-quarantined-messages-and-files"></a>So filtern Sie Ergebnisse und finden isolierte Nachrichten und Dateien
<a name="BKMK_AdvSearch"> </a>

Je nach Ihren Einstellungen gibt es möglicherweise viele isolierte Nachrichten und Dateien. Zum Auffinden einer bestimmten Nachricht oder Datei oder eines Satzes von Nachrichten oder Dateien können Sie unter Quarantäne gestellte Elemente basierend auf einer Vielzahl zusätzlicher Informationen filtern.
  
1. Stellen Sie auf der Seite " **Quarantäne** " sicher, dass die oberste Reihe von Filtern so festgelegt ist, dass Nachrichten oder Dateien entsprechend angezeigt werden: 
    
      - Zum Suchen nach Dateien legen Sie die Filter so fest, dass **Dateien** angezeigt werden, die aufgrund von **Schadsoftware**isoliert wurden.<br/>
    Bei isolierten Dateien werden auf der Seite alle isolierten Dateien angezeigt, nicht nur Ihre eigenen, unabhängig davon, was Sie anzeigen möchten.
    
      - Zum Suchen nach isolierten Nachrichten legen Sie Filter so fest, dass **alle** oder **nur meine** **e-Mails**angezeigt werden. Für den letzten Filter wählen Sie den Typ der isolierten Nachricht aus, nach der gesucht werden soll. Sie können nach Nachrichten suchen, die als **Spam**identifiziert wurden, für Nachrichten, die einer e-Mail-Fluss Regel (**Transportregel**), **Massen** Nachrichten, **Phishing** -e-Mails oder e-Mails mit **Schadsoftware**entsprachen.
    
2. Wählen Sie unter **Ergebnisse sortieren nach**die Filter oder Filter aus, die Sie für die Suche in den Dropdownlisten verwenden möchten. Die Optionen variieren je nachdem, ob Sie nach Dateien oder Nachrichten suchen. Platzhalter werden zu diesem Zeitpunkt in Suchfeldern nicht unterstützt.<br/><br/>Für Dateien und Nachrichten können Sie festlegen, dass nach dem Datum gefiltert wird, an dem die Nachricht oder Datei an die Quarantäne gesendet wurde. Sie können das Datum oder einen Datumsbereich angeben, einschließlich der Uhrzeit. Sie können Ihre Suchergebnisse auch nach dem Ablaufdatum filtern, an dem die Datei oder Nachricht aus der Quarantäne gelöscht wird, oder Sie können eine Kombination von Filtern verwenden. Um nach Ablaufdatum zu suchen, wählen Sie **Erweiterter Filter**aus. Unter **Expires**können Sie Nachrichten auswählen, die innerhalb der nächsten 24 Stunden ( **heute**) aus der Quarantäne gelöscht werden, innerhalb der nächsten 48 Stunden ( **nächsten 2 Tage**), innerhalb der nächsten Woche ( **Nächste 7 Tage**), oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.<br/><br/>Für Nachrichten haben Sie die folgenden zusätzlichen Optionen:
    
      - **Nachrichten-ID**. Verwenden Sie diese, um eine bestimmte Nachricht zu identifizieren, wenn Sie die Nachrichten-ID kennen.<br/><br/>
    Wenn beispielsweise eine bestimmte Nachricht von einem Benutzer in Ihrer Organisation gesendet oder dafür bestimmt wird, aber nie sein Ziel erreicht hat, können Sie mithilfe einer Nachrichtenablaufverfolgung nach der Nachricht suchen (siehe [Ausführen einer Nachrichtenablaufverfolgung und Anzeigen von Ergebnissen](https://go.microsoft.com/fwlink/?LinkId=799737)). Wenn Sie feststellen, dass die Nachricht an die Quarantäne gesendet wurde, weil Sie möglicherweise mit einer Nachrichtenfluss Regel übereinstimmt oder als Spam identifiziert wurde, können Sie diese Nachricht dann leicht in der Quarantäne finden, indem Sie die zugehörige Nachrichten-ID angeben. Achten Sie darauf, die vollständige Nachricht-ID-Zeichenfolge einzubeziehen. Dies kann beispielsweise zu Spitzen\<\>Klammern () gehören:<br/>
    `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`
    
      - **Absender-e-Mail-Adresse**. Wählen Sie aus, um nach einer einzelnen Absender-e-Mail-Adresse zu filtern. 
    
      - **E-Mail-Adresse**des Empfängers. Wählen Sie aus, um nach einer einzelnen Empfänger-e-Mail-Adresse zu filtern. 
    
      - **Betreff**. Geben Sie den Betreff einer e-Mail-Adresse ein, die Sie suchen möchten. Da die Suche nach Platzhalter nicht unterstützt wird, müssen Sie den gesamten Betreff der Nachricht verwenden, damit die Nachricht in den Ergebnissen zurückgegeben wird. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet. 
    
## <a name="view-details-about-quarantined-messages-and-files"></a>Anzeigen von Details zu isolierten Nachrichten und Dateien

Wenn Sie ein in der Quarantäneliste angezeigtes Element auswählen, wird im **Detail** Bereich auf der rechten Seite des Security &amp; Compliance Centers eine Zusammenfassung der zugehörigen Eigenschaften angezeigt. 
  
**Für isolierte Nachrichten angezeigte Details**
  
- **Nachrichten-ID**. Der eindeutige Bezeichner für die Nachricht. 
    
- **Absenderadresse**. Die Person, die die Nachricht gesendet hat. 
    
- **Erhalten**. Das Datum und die Uhrzeit, zu der die Nachricht erhalten wurde. 
    
- **Betreff**. Der Text für die Betreffzeile der Nachricht. 
    
- **Geben**Sie ein. Zeigt an, ob eine Nachricht als **Spam**, **Massen**, **Phishing**, Übereinstimmung mit einer e-Mail-Fluss Regel (**Transport Regel**) oder als mit **Schadsoftware**gekennzeichnet identifiziert wurde.
    
- **Läuft ab**. Das Datum und die Uhrzeit, zu der die Nachricht automatisch aus der Quarantäne gelöscht wird. 
    
- **Freigegeben an**. Alle e-Mail-Adressen (falls vorhanden), für die die Nachricht freigegeben wurde. 
    
- **Noch nicht freigegeben**. Alle e-Mail-Adressen (falls vorhanden), für die die Nachricht noch nicht freigegeben wurde. 
    
 **Für isolierte Dateien angezeigte Details**
  
- **Dateiname** Der Name der Datei in Quarantäne. 
    
- **Websitepfad** URL, die den Speicherort der Datei in Office 365 definiert. 
    
- **Erkanntes Datum/Uhrzeit** Das Datum und die Uhrzeit, zu denen die Datei isoliert wurde. 
    
- **Ablaufdatum** Das Datum, an dem die Nachricht aus der Quarantäne gelöscht wird. 
    
- **Erkannt von** Die Methode, mit der die Schadsoftware in der Datei erkannt wird. Dies kann entweder ATP (Advanced Threat Protection) oder das Anti-Malware-Modul von Microsoft sein. 
    
- **Freigegeben** Beschreibt, ob die Datei freigegeben wurde oder nicht. 
    
- **Name** der Schadsoftware Die Familie und der Name der Schadsoftware, die in der Datei erkannt wurde. 
    
- **Dokument-ID** Ein eindeutiger Bezeichner für das Dokument. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **Organisation** Die eindeutige ID Ihrer Organisation in Office 365. 
    
- **Geändert von** Das Arbeits-oder Schulkonto des Benutzers, der die Datei zuletzt geändert hat. 
    
- **Dateigröße** Die Größe der Datei in KB. 
    
- **SHA256-Hash** Der Hash der Datei. Sie können dies verwenden, um nach anderen Reputation Stores zu suchen, die Sie möglicherweise haben, oder um herauszufinden, wo sich die Datei sonst in Ihrer Umgebung befinden könnte. 
    
## <a name="managing-messages-and-files-in-quarantine"></a>Verwalten von Nachrichten und Dateien in der Quarantäne
<a name="BKMK_ManageQuarantinedItem"> </a>

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten ausgewählt haben, haben Sie mehrere Optionen zum Verwalten von Nachrichten in der Quarantäne.
  
- Keine Aktion ausführen. Wenn Sie nichts tun, wird die Nachricht nach Ablauf von Office 365 automatisch gelöscht. Standardmäßig werden Spam, Massen, Schadsoftware, Phishing und Nachrichten, die mit einer e-Mail-Fluss Regel übereinstimmen, in Quarantäne für 30 Tage aufbewahrt. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten ändern, indem Sie die Einstellung **Spam für (Tage)** in ihren Anti-Spam-Richtlinien konfigurieren. Weitere Informationen finden Sie unter [Festlegen des Aufbewahrungszeitraums für die Quarantäne](manage-quarantined-messages-and-files.md#BKMK_ModQuarantineTime) in diesem Artikel. 
    
- **Nachrichtenkopfzeile anzeigen** Klicken Sie auf diesen Link, um den Text der Nachrichtenkopfzeile anzuzeigen. Um die Kopfzeile eingehend zu analysieren, kopieren Sie den Text der Nachrichtenkopfzeile in die Zwischenablage, und wählen Sie dann **Microsoft Message Header Analyzer** aus, um zur Remote Verbindungs Untersuchung zu wechseln (Klicken Sie mit der rechten Maustaste, und wählen Sie **in einer neuen Registerkarte öffnen** aus, wenn Sie Office nicht verlassen möchten. 365, um diese Aufgabe abzuschließen). Fügen Sie die Kopfzeile der Nachricht auf der Seite im Abschnitt Nachrichtenkopf Analyse ein, und wählen Sie **Kopfzeilen analysieren**aus.
    
- **Vorschau Nachricht** Ermöglicht das Anzeigen von Rohdaten-oder HTML-Versionen des Nachrichtentext Texts. In der HTML-Ansicht sind Links deaktiviert. 
    
- **Nachricht herunterladen** oder **Datei herunterladen**. Wählen Sie diese Option aus, um eine Kopie der Nachricht oder Datei auf Ihr lokales Gerät herunterzuladen. Sie müssen sich vergewissern, dass Sie die Risiken im Zusammenhang mit dem Herunterladen von Elementen aus der Quarantäne kennen, bevor Sie dies tun können. Nachrichten werden im eml-Format in einem von Ihnen angegebenen Ordner gespeichert. In Quarantäne befindliche Dateien werden im ursprünglichen Format gespeichert.
    
- **Löschen** Sie Wenn Sie möchten, können Sie sofort ein isoliertes Element (oder eine Gruppe von Elementen) löschen, anstatt auf das von Office 365 festgelegte Ablaufdatum zu warten. Zum Löschen einer Nachricht oder Datei wählen Sie in der Quarantäneliste das Element aus, und klicken Sie dann auf **Löschen**. Wenn Sie mehrere Elemente gleichzeitig löschen möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** die Option **ausgewählte Nachrichten löschen** oder **ausgewählte Dateien löschen**aus.
    
- **Release** Freigeben eines isolierten Elements (oder einer Gruppe von Elementen) und melden der Elemente als falsch isoliert (falsch positive Ergebnisse) an Microsoft. 
    
    Wenn Sie eine einzelne Nachricht oder Datei freigeben und melden möchten, wählen Sie in der Quarantäneliste das Element aus, und wählen Sie **Datei freigeben** oder **Nachricht freigeben**aus. Stellen Sie auf der nächsten Seite sicher, dass **Berichtsmeldungen an Microsoft für Analyse** -oder **Berichtsdateien an Microsoft für Analyse** ausgewählt ist. 
    
    Wenn Sie mehrere Elemente gleichzeitig freigeben möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** die Option **Dateien freigeben** oder **Nachrichten**freigeben aus. Stellen Sie auf der nächsten Seite sicher, dass **Berichtsmeldungen an Microsoft für Analyse** -oder **Berichtsdateien an Microsoft für Analyse** ausgewählt ist. 
    
Beachten Sie beim Freigeben von Nachrichten Folgendes:
  
- Wenn Sie eine Massen Veröffentlichung mehrerer Nachrichten gleichzeitig ausführen, werden die Nachrichten für alle ursprünglich identifizierten Empfänger freigegeben. Wenn Sie nur Nachrichten nur für bestimmte Empfänger freigeben möchten, müssen Sie die Nachrichten nacheinander freigeben und die Empfänger einzeln identifizieren.
    
- Eine Nachricht kann nicht mehrmals an denselben Empfänger freigegeben werden.
    
- Wenn Sie eine Nachricht an mehrere Empfänger freigeben, werden nur Empfänger, die die Nachricht zuvor nicht erhalten haben, in der Liste der potenziellen Empfänger angezeigt.
    
- Wenn Sie sich entscheiden, falsch positive Ergebnisse zu melden, werden die Nachrichten, die Sie freigegeben haben, als Spam, Massen, Phishing oder als enthaltender Schadsoftware isoliert, dann wird die Nachricht auch an das Microsoft-Spam Analyse Team gemeldet. Das Team bewertet und analysiert die Nachricht, und je nach den Ergebnissen der Analyse können die Filterregeln für den Dienst weiten Spam Inhalt so angepasst werden, dass die Nachricht durchlassen wird.
    
## <a name="setting-the-quarantine-retention-period"></a>Festlegen des Aufbewahrungszeitraums für Quarantäne
<a name="BKMK_ModQuarantineTime"> </a>

Sie können konfigurieren, wie lange Nachrichten und Dateien in der Quarantäne verbleiben, bevor Sie ablaufen. Standardmäßig werden isolierte Elemente 30 Tage lang aufbewahrt. Sie konfigurieren diese Einstellung für jede Richtlinie, die Sie erstellen. Sie können den Wert für die Standardrichtlinie auch wie in diesem Artikel beschrieben ändern. 
  
### <a name="to-modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security-and-compliance-center"></a>So ändern Sie den Aufbewahrungszeitraum für Quarantäne für die standardmäßige Spamfilter Richtlinie im Security and Compliance Center

1. Melden Sie sich bei Office 365 mit einem Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365 Organisation an, und [wechseln Sie zum Security and Compliance Center](go-to-the-securitycompliance-center.md).
    
2. Erweitern Sie auf der linken Seite den Knoten **Bedrohungs Verwaltung**, wählen Sie **Richtlinie**aus, und wählen Sie dann **Anti-Spam**aus. <br/>
    > [!TIP]
    > Wenn Sie direkt zur **Antispam-** Seite im Security &amp; Compliance Center wechseln möchten, verwenden Sie die folgende URL: #a0[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)
  
3. Wählen Sie **Benutzerdefiniert** aus, um die Registerkarte **benutzerdefinierte Einstellungen** anzuzeigen. 
    
4. Erweitern Sie die Zeile **Standard-Spamfilter Richtlinie (Always on)** . 
    
5. Wählen Sie **Richtlinie bearbeiten**aus. Die Einstellungen für die standardmäßige Spamfilter Richtlinie werden auf einer neuen Seite angezeigt.
    
6. Erweitern Sie **Spam-und Massenaktionen**.
    
7. Geben Sie unter **Quarantäne**im Textfeld **Spam für (Tage) beibehalten** den Zeitraum ein, in dem Office 365 Nachrichten und Dateien in der Quarantäne aufbewahrt werden sollen. Der Standardwert beträgt 30 Tage. Dies ist auch die maximale. 
    
8. Wählen Sie **Speichern** aus.
    


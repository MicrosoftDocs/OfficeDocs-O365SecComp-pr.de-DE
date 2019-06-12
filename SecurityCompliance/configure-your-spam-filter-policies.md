---
title: Konfigurieren von Spamfilterrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: Zu den grundlegenden spamfiltereinstellungen gehören das Auswählen der Aktion, die für Nachrichten ausgeführt werden soll, die als Spam identifiziert werden.
ms.openlocfilehash: be99c017a5038fbfb431edbcf2d65c877d92388c
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857655"
---
# <a name="configure-your-spam-filter-policies"></a>Konfigurieren von Spamfilterrichtlinien
Zu den spamfiltereinstellungen gehört das Auswählen der Aktion, die für Nachrichten ausgeführt werden soll, die als Spam identifiziert werden. Einstellungen für Spam Filterrichtlinien werden nur für eingehende Nachrichten angewendet, und es gibt zwei Typen:

  - Standard: die standardmäßige Spamfilter Richtlinie wird zum Konfigurieren von unternehmensweiten spamfiltereinstellungen verwendet. Diese Richtlinie kann nicht umbenannt werden und ist immer eingeschaltet.

  - Benutzerdefiniert: benutzerdefinierte Spamfilter Richtlinien können Granular sein und auf bestimmte Benutzer, Gruppen oder Domänen in Ihrer Organisation angewendet werden. Benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Sie können die Reihenfolge ändern, in der Ihre benutzerdefinierten Richtlinien ausgeführt werden, indem Sie die Priorität der einzelnen benutzerdefinierten Richtlinien ändern. Wenn mehrere Richtlinien den festgelegten Kriterien entsprechen, gilt jedoch nur die höchste Priorität (d. h. die am nächsten an 0) liegende Richtlinie.

## <a name="what-you-must-know-before-you-begin"></a>Was Sie wissen müssen, bevor Sie beginnen

Geschätzte Zeit bis zum Abschließen des Vorgangs: 30 Minuten
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter Anti-Spam-Eintrag im [Feature Berechtigungen in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) Thema.

Die Einstellungen für die Spamfilter Richtlinie befinden sich alle im Security #a0 Compliance Center (SCC). Weitere Informationen finden [Sie unter Wechseln zum Office 365 Security #a0 Compliance Center](go-to-the-securitycompliance-center.md). Die Seite Anti-Spam-Einstellungen befindet sich im \> Abschnitt **Anti-Spam** im SCC **Threat Management** \> - **Richtlinie** \> .

## <a name="access-and-create-spam-filter-policies"></a>Zugreifen auf und Erstellen von Spamfilter Richtlinien

Auf der Seite Anti-Spam-Einstellungen können die Standardeinstellungen auf der Registerkarte Standard angezeigt werden. Um diese Einstellungen zu ändern, wechseln Sie zur Registerkarte **Benutzerdefiniert** . Sie können einige der Standardeinstellungen in der standardmäßigen Spamfilter Richtlinie anzeigen und konfigurieren.

Um weitere benutzerdefinierte Einstellungen zu ermöglichen oder benutzerdefinierte Richtlinien hinzuzufügen, ändern Sie die Auswahl für **benutzerdefinierte Einstellungen** in **ein** , um benutzerdefinierte Spamfilter Richtlinien zu aktivieren. Sie können vorhandene benutzerdefinierte Richtlinien anzeigen, indem Sie Sie von hier aus erweitern.

## <a name="configure-custom-spam-filter-policy-settings"></a>Konfigurieren von benutzerdefinierten Einstellungen für Spamfilter Richtlinien

1. Wählen Sie und klicken Sie auf **Richtlinie bearbeiten** , wenn Sie eine Richtlinie bearbeiten; Klicken Sie andernfalls auf **Richtlinie erstellen** .

2. Sie können einen eindeutigen Namen für benutzerdefinierte Richtlinien angeben, aber die Standardrichtlinie kann nicht umbenannt werden. Optional können Sie auch eine ausführlichere Beschreibung für jede Richtlinie angeben.

3. Im Abschnitt **Spam-und Massenaktionen** :

  - Wählen Sie eine Aktion für die **Spam**-, **High Confidence Spam**-, **Phishing-e-Mail**-und **Massen-e-Mail-** Typen aus. Die verfügbaren Werte sind: 

    - **Nachricht in Junk-e-Mail-Ordner umlegen:** Sendet die Nachricht an den Junk-e-Mail-Ordner der angegebenen Empfänger. Dies ist die Standardaktion für Spam, Spam mit hoher Zuverlässigkeit und Massen.<br/><br/>

    > [!NOTE]
    > Damit diese Aktion mit lokalen Postfächern funktioniert, müssen Sie zwei Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Servern konfigurieren, um von EoP hinzugefügte Spam Kopfzeilen zu erkennen. Ausführliche Informationen finden Sie unter so [Stellen Sie sicher, dass Spam an den Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Dieser Schritt ist für eigenständige Kunden mit Exchange Online Protection (EoP) von entscheidender Bedeutung.

    - **X-Header hinzufügen:** Sendet die Nachricht an die angegebenen Empfänger, fügt jedoch dem Nachrichtenkopf X-HeaderText hinzu, um die Nachricht als Spam zu identifizieren. Wenn Sie diesen Text als Bezeichner verwenden, können Sie optional Posteingangsregeln erstellen oder ein Downstream-Gerät verwenden, um die Nachricht zu bearbeiten. Der standardmäßige X-Headertext lautet in etwa **Diese Nachricht ist offenbar Spam**.<br/>Sie können den Text der x-Kopfzeile mithilfe des Texteingabefelds **diese x-Kopfzeile hinzufügen** anpassen. Wenn Sie den Text der X-Kopfzeile anpassen, beachten Sie die folgenden Bedingungen: 
    
      - Wenn \< Sie nur die Kopfzeile im Format- *Header*\>angeben, in der keine Leerzeichen in der \< *Kopfzeile*\>vorhanden sind, wird ein Doppelpunkt an den benutzerdefinierten Text angehängt, gefolgt von dem Standardtext.       Wenn Sie beispielsweise "This-is-My-Custom-Header" angeben, wird der Text der X-Kopfzeile als "This-is-My-Custom-Header: Diese Nachricht scheint Spam" angezeigt. 
        
      - Wenn Sie Leerzeichen innerhalb des benutzerdefinierten Kopfzeilentexts einfügen oder den Doppelpunkt selbst hinzufügen (beispielsweise "x Dies ist mein benutzerdefinierter Header" oder "x-this-is-My-Custom-Header:"), wird der x-HeaderText auf den Standardwert "x-this-is-Spam: Diese Nachricht scheint Spam" zurückgesetzt.
    
      - Sie können den Headertext nicht im Format \< *Header*  \>:\<  *Wert*  \> angeben. Wenn Sie dies tun, werden beide Werte vor und nach dem Doppelpunkt ignoriert, und stattdessen wird der standardmäßige x-Header-Text angezeigt: "x-this-is-Spam: Diese Nachricht scheint Spam zu sein." 
      
      - Beachten Sie, dass e-Mail-Nachrichten mit dieser X-Kopfzeile aufgrund der Post Fach Junk-Konfiguration möglicherweise weiterhin in den Postfachordner Junk-e-Mail verschoben werden Sie können dies ändern, indem Sie dieses Feature mit der Option "MailboxJunkEmailConfiguration" deaktivieren.

    - **Betreff-Zeile wird mit Text voran gestellt:** Sendet die Nachricht an die beabsichtigten Empfänger, stellt jedoch der Betreffzeile den Text voran, den Sie in der **Zeile Präfix Betreff mit diesem Text** Eingabefeld angeben. Wenn Sie diesen Text als Bezeichner verwenden, können Sie optional Regeln erstellen, um die Nachrichten nach Bedarf zu filtern oder weiterzuleiten. 

    - **Nachricht an e-Mail-Adresse umleiten:** Sendet die Nachricht an eine festgelegte e-Mail-Adresse statt an die vorgesehenen Empfänger. Geben Sie im Eingabefeld **Nachricht an E-Mail-Adresse umleiten** die Adresse ein, an die die Umleitung erfolgen soll.

    - **Nachricht löschen:** Löscht die gesamte Nachricht, einschließlich aller Anlagen. 
        
    - **Quarantäne Nachricht:** Sendet die Nachricht an die Quarantäne statt an die vorgesehenen Empfänger. Dies ist die Standardaktion für Phishing. Geben Sie bei Auswahl dieser Option im Eingabefeld **Spamnachrichten aufbewahren für (Tage)** die Anzahl der Tage an, für die die Nachricht in Quarantäne bleiben soll. (Nach Ablauf des angegebenen Zeitraums wird die Nachricht automatisch gelöscht. Der Standardwert ist 30 Tage, was der Maximalwert ist. Der Mindestwert ist 1 Tag.)<br/><br/>Tipp: Informationen dazu, wie Administratoren e-Mail-Nachrichten verwalten können, die sich in der Exchange-Verwaltungskonsole in der Quarantäne befinden, finden Sie unter [Quarantine](quarantine.md) and [Find and Release Quarantined Messages as a Administrator](find-and-release-quarantined-messages-as-an-administrator.md). > Informationen zum Konfigurieren von Spambenachrichtigungen, die an Benutzer gesendet werden sollen, finden Sie unter [configure End-User Spam Notifications in EoP](configure-end-user-spam-notifications-in-eop.md) oder [configure End-User Spam Notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 

  - Konfigurieren **Wählen Sie den Schwellenwert** aus, um festzulegen, wie Massen-e-Mails als Spam behandelt werden sollen, basierend auf der Massen Reklamations Ebene (BCL) der Nachricht. Sie können eine Schwellenwerteinstellung zwischen 1–9 auswählen, wobei 1 die meisten Massensendungen als Spam markiert und 9 die meisten Massensendungen als übermittelbar zulässt. Der Dienst führt dann die konfigurierte Aktion aus, beispielsweise das Senden der Nachricht an den Junk-e-Mail-Ordner des Empfängers. Weitere Informationen finden Sie unter [Bulk Complaint Level values](bulk-complaint-level-values.md) und [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md). 

4. Auf der Seite **Spam Eigenschaften** können Sie die Optionen für den Test Modus für die Richtlinie festlegen, indem Sie Folgendes konfigurieren: 
    
      - **Keine** Es werden keine Testmodusaktionen bezüglich der Nachricht ausgeführt. Hierbei handelt es sich um die Standardeinstellung. 
        
      - **Hinzufügen des standardmäßigen Test-X-Kopfzeilentexts** Wenn Sie diese Option auswählen, wird die Nachricht an die angegebenen Empfänger gesendet, aber auch eine spezielle X-Kopfzeile zur Nachricht hinzugefügt, um Sie so zu identifizieren, dass Sie mit einer bestimmten erweiterten Spamfilter Option übereinstimmt. 
        
      - **Bcc-Nachricht an diese Adresse senden** Wenn Sie diese Option auswählen, wird eine Blindkopie der Nachricht an die e-Mail-Adresse gesendet, die Sie im Eingabefeld angeben. <br/><br/>Weitere Informationen zu den erweiterten Spamfilter Optionen, einschließlich Beschreibungen zu jeder Option und dem jedem einzelnen zugeordneten X-Header-Text, finden Sie unter [Advanced Spam Filtering Options](advanced-spam-filtering-asf-options.md).

5. Klicken Sie für benutzerdefinierte Richtlinien nur auf das Menüelement **anwenden auf** , und erstellen Sie dann eine bedingungsbasierte Regel, um die Benutzer, Gruppen und Domänen anzugeben, auf die diese Richtlinie angewendet werden soll. Sie können mehrere Bedingungen angeben, wenn diese eindeutig sind. 
    
      - Um Benutzer auszuwählen, wählen Sie **Der Empfänger ist** aus. Wählen Sie im folgenden Dialogfeld in der Benutzerauswahlliste den bzw. die Absender in Ihrem Unternehmen aus, und klicken Sie dann auf **Hinzufügen**. Wenn Sie Absender hinzufügen möchten, die nicht in der Liste enthalten sind, geben Sie deren E-Mail-Adressen ein, und klicken Sie auf **Namen überprüfen**. In diesem Feld können Sie auch Platzhalterzeichen für mehrere E-Mail-Adressen verwenden (z. B.: \*@ _domainname_). Wenn Sie Ihre Auswahl getroffen haben, klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Gruppen auszuwählen, wählen Sie **Der Empfänger ist Mitglied von** aus, und wählen Sie dann im folgenden Dialogfeld die Gruppen aus oder geben Sie diese an. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Domänen auszuwählen, wählen Sie **Empfängerdomäne ist** aus, und fügen Sie dann im folgenden Dialogfeld die Domänen hinzu. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren.<br/><br/>Sie können Ausnahmen innerhalb der Regel erstellen. So können Sie beispielsweise Nachrichten aus allen Domänen mit Ausnahme einer bestimmten Domäne filtern. Klicken Sie auf **Ausnahme hinzufügen**, und erstellen Sie dann Ihre Ausnahmebedingungen ähnlich wie die anderen Bedingungen.<br/><br/>Das Anwenden einer Spamrichtlinie auf eine Gruppe wird nur für **E-Mail-aktivierte Sicherheitsgruppen** unterstützt. 
  
6. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Richtlinieneinstellungen angezeigt.

Die Standardrichtlinie kann nicht deaktiviert oder gelöscht werden, und benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Für benutzerdefinierte Richtlinien können Sie die Kontrollkästchen in der Spalte **aktiviert** aktivieren oder deaktivieren. Standardmäßig sind alle Richtlinien aktiviert. Um eine benutzerdefinierte Richtlinie zu löschen, wählen Sie die ![Richtlinie](media/ITPro-EAC-DeleteIcon.gif) **** aus, klicken Sie auf das Symbol Löschen, und bestätigen Sie, dass Sie die Richtlinie löschen möchten.

> [!TIP]
> Sie können die Priorität (Reihenfolge der Ausführung) Ihrer benutzerdefinierten Richtlinien ändern ![, indem Sie](media/ITPro-EAC-UpArrowIcon.gif) auf den Pfeil ![](media/ITPro-EAC-DownArrowIcon.gif) nach oben nach oben und nach unten zeigenden Pfeil nach unten klicken. Die Richtlinie mit der **Priorität** **0** wird zuerst ausgeführt, gefolgt von **1**, dann **2**usw. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Konfigurieren der Richtlinien für die Spamfilterung mit Remote-PowerShell

Sie können auch in PowerShell Richtlinien für die Spamfilterung konfigurieren und anwenden. Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen. Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, können Sie unter [Verbinden mit PowerShell in Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=627290) nachlesen.
  
- [Get-HostedContentFilterPolicy](http://technet.microsoft.com/library/d510471a-dda5-4df7-b3f8-2ee7a1948436.aspx) Dient zum Anzeigen Ihrer Einstellungen für die Spamfilterung. 
    
- [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) Dient zum Bearbeiten Ihrer Einstellungen für die Spamfilterung. 
    
- [New-HostedContentFilterPolicy](http://technet.microsoft.com/library/4d15128d-9e16-42a1-8ac5-36f07d4bbbf0.aspx) Dient zum Erstellen einer neuen benutzerdefinierten Richtlinie für die Spamfilterung. 
    
- [Remove-HostedContentFilterPolicy](http://technet.microsoft.com/library/9fe1fe03-8f83-41e3-9bf5-084a392784d6.aspx) Dient zum Löschen einer benutzerdefinierten Richtlinie für die Spamfilterung. 
    
Zum Anwenden einer benutzerdefinierten Richtlinie für die Spamfilterung auf Benutzer, Gruppen und/oder Domänen verwenden Sie das Cmdlet [New-HostedContentFilterRule](http://technet.microsoft.com/library/2df13ba9-1eb0-4da3-bd72-a79d5fa15e26.aspx) (um eine neue Filterregel zu erstellen, die auf benutzerdefinierte Richtlinien angewendet werden kann) oder das Cmdlet [Set-HostedContentFilterRule](http://technet.microsoft.com/library/ba259260-ffd3-43f3-8ef4-9d8659679d02.aspx) (um eine vorhandene Filterregel zu bearbeiten, die auf benutzerdefinierte Richtlinien angewendet werden kann). Mit dem Cmdlet [Enable-HostedContentFilterRule](http://technet.microsoft.com/library/354ece28-dcde-4b5f-88ed-475115e7ea78.aspx) oder [Disable-HostedContentFilterRule](http://technet.microsoft.com/library/c1f8dafc-ef5d-47e3-b0fb-71a88e145fc5.aspx) können Sie die für die Richtlinie geltende Regel aktivieren oder deaktivieren. 
  
## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um sicherzustellen, dass Spam ordnungsgemäß erkannt und behandelt wird, können Sie über den Dienst eine GTUBE-Nachricht senden. Ähnlich wie die EICAR-Antivirustestdatei, beinhaltet GTUBE einen Test, mit dem Sie überprüfen können, ob der Dienst eingehende Spamnachrichten erkennt. Eine GTUBE-Nachricht sollte vom Spamfilter immer als Spam erkannt werden, und die daraufhin bezüglich der Nachricht ausgeführten Aktionen sollten den Einstellungen entsprechen, die Sie konfiguriert haben.
  
Geben Sie den folgenden GTUBE-Text in eine E-Mail in einer Zeile ohne Leerzeichen und Zeilenumbrüche ein:
  
```
XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
```

## <a name="fine-tuning-your-spam-filter-policy-to-prevent-false-positives-and-false-negatives"></a>Optimieren Ihrer Spamfilterrichtlinie, um falsch positive Ergebnisse und falsch negative Ergebnisse zu verhindern

Sie können erweiterte Spam Filterungstechniken aktivieren, wenn Sie einen aggressiveren Ansatz für die Spamfilterung verfolgen möchten. Allgemeine Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Verwenden einer Liste sicherer Adressen oder anderer Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](reduce-spam-email.md). Diese sind hilfreich, wenn Sie über die Steuerung auf Administratorebene verfügen und wenn Sie falsch positive Ergebnisse oder falsch negative Ergebnisse vermeiden möchten.

## <a name="allowblock-lists"></a>Listen zulassen/blockieren

Es gibt Zeiten, in denen unsere Filter die Nachricht versäumen, oder es dauert Zeit, bis unsere Systeme Sie einholen. In diesen Fällen verfügt die Antispam-Richtlinie über eine allow-und eine Sperrliste, um das aktuelle Urteil außer Kraft zu setzen. Diese Option sollte nur sparsam verwendet werden, da Listen unüberschaubar und vorübergehend sein können, da unser Filter Stapel das tun sollte, was Sie tun sollte.

Sowohl Zulassungs-als auch Sperrlisten werden als Teil einer beliebigen Spam Schutzrichtlinie für Kunden konfiguriert:

1. Im Abschnitt **Zulassungslisten** können Sie Einträge wie Absender oder Domänen angeben, die immer an den Posteingang übermittelt werden. E-Mails von diesen Einträgen werden nicht vom Spamfilter verarbeitet. 
    
      - Fügen Sie der Zulassungsliste für Absender vertrauenswürdige Absender hinzu. Klicken ****![Sie auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol bearbeiten, und fügen Sie dann im Dialogfeldauswahl die Absenderadressen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **Speichern** , um zur Seite **Zulassungslisten** zurückzukehren. 
        
      - Fügen Sie der Zulassungsliste für Domänen vertrauenswürdige Domänen hinzu. Klicken ****![Sie auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol bearbeiten, und fügen Sie dann im Dialogfeldauswahl die Domänen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **Speichern** , um zur Seite **Zulassungslisten** zurückzukehren. 

> [!CAUTION]
> Sie sollten keine akzeptierten Domänen (Domänen, die Sie besitzen) oder allgemeine Domänen wie Microsoft.com, Office.com usw. in einer Zulassungsliste auflisten. Auf diese Weise können Spoofer das Senden von e-Mails uneingeschränkt in Ihre Organisation ermöglichen.

2. Auf der Seite **Sperrlisten** können Sie Einträge, wie z. B. Absender oder Domänen, angeben, die immer als Spam markiert werden. Der Dienst wendet die konfigurierte Spamaktion bei hoher Vertrauenswürdigkeit auf E-Mails an, die diesen Einträgen entsprechen. 
    
      - Fügen Sie der Absendersperrliste unerwünschte Absender hinzu. Klicken ****![Sie auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol bearbeiten, und fügen Sie dann im Dialogfeldauswahl die Absenderadressen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **Speichern** , um zur Seite **Sperrlisten** zurückzukehren. 
        
      - Fügen Sie der Domänensperrliste unerwünschte Domänen hinzu. Klicken ****![Sie auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol bearbeiten, und fügen Sie dann im Dialogfeldauswahl die Domänen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **Speichern** , um zur Seite **Sperrlisten** zurückzukehren.

> [!TIP]
>  Es kann Situationen geben, in denen Ihre Organisation möglicherweise nicht mit dem vom Dienst bereitgestellten Urteil einverstanden ist. In diesem Fall können Sie den Eintrag zulassen oder blockieren dauerhaft beibehalten. Wenn Sie jedoch eine Domäne für einen längeren Zeitraum in die Zulassungsliste einfügen möchten, sollten Sie dem Absender mitteilen, dass seine Domäne authentifiziert und auf DMARC Reject festgelegt wird, falls dies nicht der Fall ist.

## <a name="for-more-information"></a>Weitere Informationen
<a name="sectionSection6"> </a>

[Einrichten Ihrer Domäne für DMARC](use-dmarc-to-validate-email.md)
  
[Quarantine](quarantine.md)
  
[Verwenden von sicheren Listen oder anderen Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](https://go.microsoft.com/fwlink/p/?LinkId=534225)

[SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md)
  


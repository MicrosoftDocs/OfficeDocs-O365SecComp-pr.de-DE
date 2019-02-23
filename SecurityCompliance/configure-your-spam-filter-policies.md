---
title: Konfigurieren von Spamfilterrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: Zu den grundlegenden spamfiltereinstellungen gehört das Auswählen der Aktion für Nachrichten, die als Spam identifiziert werden, und die Auswahl, ob Nachrichten gefiltert werden sollen, die in bestimmten Sprachen geschrieben oder aus bestimmten Ländern oder Regionen gesendet werden.
ms.openlocfilehash: 20c1e60f10b2cdf12bb2a62afa80f56904a7a3f2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216785"
---
# <a name="configure-your-spam-filter-policies"></a>Konfigurieren von Spamfilterrichtlinien
  
Zu den grundlegenden spamfiltereinstellungen gehört das Auswählen der Aktion für Nachrichten, die als Spam identifiziert werden. Einstellungen für Spam Filterrichtlinien werden nur auf eingehende Nachrichten angewendet. Sie können die standardmäßige Spamfilter Richtlinie bearbeiten, um Ihre unternehmensweiten spamfiltereinstellungen zu konfigurieren und benutzerdefinierte Spamfilter Richtlinien zu erstellen und diese dann auf bestimmte Benutzer, Gruppen oder Domänen in Ihrer Organisation anzuwenden. Benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Sie können die Reihenfolge ändern, in der die benutzerdefinierten Richtlinien ausgeführt werden, indem Sie die Priorität der einzelnen benutzerdefinierten Richtlinien ändern. Es gilt jedoch nur die Richtlinie mit der höchsten Priorität, wenn mehrere Richtlinien den festgelegten Kriterien entsprechen. 
  
> [!IMPORTANT]
> Für Kunden der eigenständigen Exchange Online Protection (EOP)-Lösung: Standardmäßig leiten die EOP-Spamfilter als Spam erkannte Nachrichten an den Junk-E-Mail-Ordner der einzelnen Empfänger weiter. Damit die Aktion **Nachricht in Junk-E-Mail-Ordner verschieben** jedoch bei lokalen Postfächern angewendet wird, müssen Sie auf Ihren lokalen Servern Exchange-Transportregeln konfigurieren, um Spamkopfzeilen zu erkennen, die von EOP hinzugefügt wurden. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
## <a name="what-you-must-know-before-you-begin"></a>Was Sie wissen müssen, bevor Sie beginnen

Geschätzte Zeit bis zum Abschließen des Vorgangs: 30 Minuten
  
Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter Anti-Spam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.
  
## <a name="use-the-security--compliance-center-scc-to-configure-spam-filter-policies"></a>Konfigurieren von Spamfilter Richtlinien mithilfe des Security & Compliance Center (SCC)

1. Navigieren Sie im Security & Compliance Center (SCC) zu **Threat Management** \> **Policy** \> **Antispam**.
    
2. Führen Sie auf der Seite **Anti-Spam-Einstellungen** einen der folgenden Schritte aus: 
    
      - Überarbeiten Sie die standardmäßige unternehmensweite Richtlinie unter den Standardeinstellungen.
    
      - Klicken Sie auf die Registerkarte **Benutzerdefiniert** , ändern Sie die **benutzerdefinierte Einstellungs** Auswahl in ein, und![klicken Sie](media/ITPro-EAC-AddIcon.gif) auf die Schaltfläche * * Symbol **Creatge eine Richtlinie** hinzufügen, um eine neue benutzerdefinierte Spamfilter Richtlinie zu erstellen, die auf Benutzer, Gruppen, **** und Domänen in Ihrer Organisation. Sie können auch vorhandene benutzerdefinierte Richtlinien bearbeiten, indem Sie darauf doppelklicken. 
    
3. Geben Sie nur für benutzerdefinierte Richtlinien einen Namen für diese Richtlinie an. Optional können Sie auch eine ausführlichere Beschreibung angeben. Die Standardrichtlinie kann nicht umbenannt werden.<br/><br/>Hinweis: Wenn Sie eine Richtlinie erstellen, werden alle Konfigurationseinstellungen auf einem einzelnen Bildschirm angezeigt. Wenn Sie dagegen eine Richtlinie bearbeiten, müssen Sie durch mehrere Bildschirme navigieren. Die Einstellungen sind in beiden Fällen identisch, aber im restlichen Teil dieses Verfahrens wird beschrieben, wie Sie beim Bearbeiten einer Richtlinie auf diese Einstellungen zugreifen. 
  
4. Wählen Sie auf der Seite **Spam-und Massen-e-Mail-Aktionen** unter **Spam** -und **High-Confidence-Spam**die Aktion aus, die für eingehende Spam-und Massen-e-Mails durchführen Standardmäßig wird **Nachrichten in Junk-e-Mail-Ordner verschieben** ausgewählt. Die anderen möglichen Werte sind: 
    
      - **Nachricht löschen** Löscht die gesamte Nachricht, einschließlich aller Anlagen. 
        
      - **Nachricht in Quarantäne verschieben** Verschiebt die Nachricht in Quarantäne, anstatt sie an die vorgesehenen Empfänger zu senden. Geben Sie bei Auswahl dieser Option im Eingabefeld **Spamnachrichten aufbewahren für (Tage)** die Anzahl der Tage an, für die die Nachricht in Quarantäne bleiben soll. (Nach Ablauf des angegebenen Zeitraums wird die Nachricht automatisch gelöscht. Der Standardwert beträgt 15 Tage, dies ist der Maximalwert. Der Mindestwert ist 1 Tag.)<br/><br/>Tipp: Informationen dazu, wie Administratoren e-Mail-Nachrichten verwalten können, die sich in der Exchange-verwaltungsKONSOLE in Quarantäne befinden, finden Sie unter [Quarantine](quarantine.md) and [Find and Release Quarantined Messages as an Administrator](find-and-release-quarantined-messages-as-an-administrator.md). > Informationen zum Konfigurieren von Spam Benachrichtigungsnachrichten, die an Benutzer gesendet werden sollen, finden Sie unter [configure End-User Spam Notifications in EoP](configure-end-user-spam-notifications-in-eop.md) oder [configure End-User Spam Notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
      - **Nachricht in Junk-E-Mail-Ordner verschieben** Sendet Nachrichten an den Ordner "Junk-E-Mail" der angegebenen Empfänger. Dies ist die Standardaktion für beide Schwellenwerte für die Vertrauenswürdigkeit.<br/><br/>**WICHTIG: für Exchange Online Protection (EOP)-Kunden: damit diese Aktion mit lokalen Postfächern funktioniert, müssen Sie zwei Exchange-Transport Regeln auf Ihren lokalen Servern konfigurieren, um von EOP hinzugefügte Spam Kopfzeilen zu finden. Weitere Informationen finden Sie unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).**
  
      - **Hinzufügen von X-Header** Sendet die Nachricht an die angegebenen Empfänger, fügt jedoch dem Nachrichtenkopf einen X-Header-Text hinzu, um die Nachricht als Spam zu identifizieren. Wenn Sie diesen Text als Bezeichner verwenden, können Sie optional Posteingangsregeln erstellen oder ein Downstream-Gerät verwenden, um die Nachricht zu bearbeiten. Der standardmäßige X-Header-Text ist **Diese Nachricht scheint Spam zu sein**.<br/>Sie können den X-Header-Text anpassen, indem Sie das Kontrollkästchen **diesen x-Kopfzeilentext hinzufügen** verwenden. Wenn Sie den X-Header-Text anpassen, beachten Sie die folgenden Bedingungen: 
    
      - Wenn Sie nur die Kopfzeile in der Format \< *Kopfzeile*\>angeben, in der keine Leerzeichen innerhalb der \< *Kopfzeile*\>vorhanden sind, wird ein Doppelpunkt an den benutzerdefinierten Text angefügt, gefolgt von dem Standardtext. Wenn Sie beispielsweise "dieser-ist-mein-benutzerdefinierter-Header" angeben, wird der X-Header-Text als "dieser-ist-mein-benutzerdefinierter-Header" angezeigt: Diese Nachricht scheint Spam zu sein.       
        
      - Wenn Sie Leerzeichen innerhalb des benutzerdefinierten Kopfzeilentexts einfügen oder den Doppelpunkt selbst hinzufügen (beispielsweise "x Dies ist mein benutzerdefinierter Header" oder "X-dieser-ist-mein-benutzerdefinierter-Header:"), wird der X-Header-Text auf den Standardwert "X-This-is-Spam: Diese Nachricht scheint als Spam" zurückgesetzt
    
      - Sie können den Kopfzeilentext nicht im Format \< *Header*  \>:\<  *value*  \>angeben. Wenn Sie dies tun, werden beide Werte vor und nach dem Doppelpunkt ignoriert, und stattdessen wird der standardmäßige X-Header-Text angezeigt: "X-This-is-Spam: Diese Nachricht ist offenbar Spam." 
      
      - Beachten Sie, dass e-Mail-Nachrichten mit dieser X-Kopfzeile aufgrund der Konfiguration von Post Fach Junk-e-Mail-Nachrichten weiterhin in den Postfachordner verschoben werden. Sie können dies ändern, indem Sie dieses Feature mit Set-MailboxJunkEmailConfiguration deaktivieren.
        
      - Voranstellen der **Betreffzeile mit Text** Sendet die Nachricht an die beabsichtigten Empfänger, stellt jedoch der Betreffzeile den Text voran, den Sie im Feld **Betreff Zeile mit diesem Text** eingeben angeben. Mithilfe dieses Texts als Bezeichner können Sie optional Regeln erstellen, um die Nachrichten nach Bedarf zu filtern oder weiterzuleiten. 
        
      - **Nachricht an E-Mail-Adresse umleiten** Sendet die Nachricht an eine ausgewählte E-Mail-Adresse anstatt an die vorgesehenen Empfänger. Geben Sie im Eingabefeld **Nachricht an E-Mail-Adresse umleiten** die Adresse ein, an die die Umleitung erfolgen soll.<br/><br/>Hinweis: Weitere Informationen zu den SCL-Werten finden Sie unter [Spam Confidence Levels](spam-confidence-levels.md). 
  
5. Unter **Bulk E-Mail** können Sie einen Schwellenwert auswählen, ab dem Massen-E-Mails wie Spam behandelt werden sollen. Dieser Schwellenwert basiert auf dem BCL-Wert (Bulk Complaint Level) der Nachricht. Sie können eine Schwellenwerteinstellung zwischen 1-9 auswählen, wobei 1 die meisten Massensendungen als Spam markiert und 9 die meisten Massensendungen als übermittelbar zulässt. Der Dienst führt dann die konfigurierte Aktion aus, z. B. das Senden der Nachricht in den Junk-E-Mail-Ordner des Empfängers. Weitere Informationen finden Sie unter [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md) und [Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?](what-s-the-difference-between-junk-email-and-bulk-email.md). 
    
6. Auf der Seite **Sperrlisten** können Sie Einträge, wie z. B. Absender oder Domänen, angeben, die immer als Spam markiert werden. Der Dienst wendet die konfigurierte Spamaktion bei hoher Vertrauenswürdigkeit auf E-Mails an, die diesen Einträgen entsprechen. 
    
      - Fügen Sie der Absendersperrliste unerwünschte Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
        
      - Fügen Sie der Domänensperrliste unerwünschte Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren.<br/><br/>**Achtung: Wenn Sie Domänen auf oberster Ebene blockieren, ist es wahrscheinlich, dass e-Mails, die Sie wünschen, als Spam markiert werden.** 
  
7. Auf der Seite **Zulassungslisten** können Sie Einträge angeben, z. B. Absender oder Domänen, die immer an den Posteingang übermittelt werden. E-Mails von diesen Einträgen werden nicht vom Spamfilter verarbeitet. 
    
      - Fügen Sie der Zulassungsliste für Absender vertrauenswürdige Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK", um zur Seite **Zulassungslisten** zurückzukehren. 
        
      - Fügen Sie der Zulassungsliste für Domänen vertrauenswürdige Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK", um zur Seite **Zulassungslisten** zurückzukehren.<br/><br/>**Achtung: Wenn Sie Domänen auf oberster Ebene zulassen, ist es wahrscheinlich, dass e-Mails, die Sie nicht wünschen, an einen Posteingang übermittelt werden.** 
  
8. Auf der Seite **Internationale Spamnachrichten** können Sie nach in bestimmten Sprachen verfassten oder aus spezifischen Ländern oder Regionen gesendeten E-Mails filtern. Es können bis zu 86 Sprachen und 250 Regionen konfiguriert werden. Der Dienst wendet dann die konfigurierte Aktion für Spam mit hoher Vertrauenswürdigkeit an. 
    
9. Aktivieren Sie das Kontrollkästchen **e-Mail-Nachrichten in den folgenden Sprachen filtern** , um diese Funktion zu ermöglichen. Klicken ![Sie auf](media/ITPro-EAC-AddIcon.gif)Symbol hinzufügen, und wählen Sie dann im Dialogfeldauswahl die gewünschten Optionen aus (Multi-Selection wird unterstützt). Wenn Sie beispielsweise auswählen, dass Nachrichten gefiltert werden sollen, die auf Arabisch (AR) geschrieben wurden, und die **Quarantäne Nachricht** ihre konfigurierte Aktion für Spamnachrichten mit hoher Vertrauenswürdigkeit ist, werden alle auf Arabisch geschriebenen Nachrichten in Quarantäne verschoben. Klicken Sie auf **OK** , um zum **internationalen Spam** Bereich zurückzukehren. 
    
10. Aktivieren Sie das Kontrollkästchen **e-Mail-Nachrichten aus den folgenden Ländern oder Regionen Filtern** , um diese Funktion zu ermöglichen. Klicken ![Sie auf](media/ITPro-EAC-AddIcon.gif)Symbol hinzufügen, und wählen Sie dann im Dialogfeldauswahl die gewünschten Optionen aus (Multi-Selection wird unterstützt). Wenn Sie beispielsweise auswählen, dass alle Nachrichten, die aus Australien (AU) gesendet werden, gefiltert werden sollen und die **Quarantäne Nachricht** ihre konfigurierte Aktion für Spamnachrichten mit hoher Vertrauenswürdigkeit ist, werden alle Nachrichten, die aus Australien gesendet werden, unter Quarantäne gestellt. Klicken Sie auf **OK** , um zum **internationalen Spam** Bereich zurückzukehren.<br/><br/>Wenn keine internationalen Spamoptionen ausgewählt sind, wendet der Dienst standardmäßig die normale Spamfilterung auf gesendete Nachrichten in allen Sprachen und aus allen Regionen an. Nachrichten werden untersucht und die konfigurierten Aktionen angewendet, wenn die Nachricht als Spam oder Spam mit hoher Vertrauenswürdigkeit eingestuft wird. 
  
11. Auf der Seite **Erweiterte Optionen** können Sie **Ein**, **Aus** oder **Test** für jede erweiterte Spamfilteroption auswählen. 
    
12. **In** NachRichten werden nach der Regel, die dieser Option zugeordnet ist, aktiv gefiltert. Nachrichten werden entweder als Spam markiert oder Ihre Spam-Bewertungen erhöht, je nachdem, welche Optionen Sie aktivieren. 
    
13. **Aus** Für die Nachrichten, die den Kriterien für Spam entsprechen, wird keine Aktion ausgeführt. Alle Optionen sind standardmäßig deaktiviert. 
    
14. **Test** Für Nachrichten, die den Spamfilter Kriterien entsprechen, wird keine Aktion ausgeführt. Nachrichten können jedoch durch Hinzufügen einer X-Kopfzeile gekennzeichnet werden, bevor Sie an den beabsichtigten Empfänger zugestellt werden. Mit dieser X-Kopfzeile wissen Sie, welche ASF-Option abgeglichen wurde. Wenn Sie **Test** für eine der erweiterten Optionen angegeben haben, können Sie die folgenden Einstellungen für den Testmodus konfigurieren, die angewendet werden sollen, wenn eine Übereinstimmung mit einer Test aktivierten Option hergestellt wird: 
    
      - **Keine** Es werden keine Testmodusaktionen bezüglich der Nachricht ausgeführt. Hierbei handelt es sich um die Standardeinstellung. 
        
      - **Hinzufügen des standardmäßigen Test-X-Header Texts** Wenn Sie diese Option auswählen, wird die Nachricht an die angegebenen Empfänger gesendet, aber außerdem wird der Nachricht ein spezieller X-Header hinzugefügt, um Sie als Übereinstimmung mit einer bestimmten erweiterten Spam Filterungs Option zu identifizieren. 
        
      - **Senden einer Bcc-Nachricht an diese Adresse** Wenn Sie diese Option auswählen, wird eine Kopie der Nachricht an die im Eingabefeld angegebene e-Mail-Adresse gesendet. <br/><br/>Weitere Informationen zu den erweiterten Spamfilter Optionen, einschließlich Beschreibungen zu jeder Option und dem jeweils zugeordneten X-Header-Text, finden Sie unter [Advanced Spam Filtering Options](advanced-spam-filtering-asf-options.md). 
  
15. Klicken Sie nur für benutzerdefinierte Richtlinien auf das Menüelement **übernehmen auf** , und erstellen Sie dann eine bedingungsbasierte Regel, um die Benutzer, Gruppen und Domänen anzugeben, auf die diese Richtlinie angewendet werden soll. Sie können mehrere Bedingungen erstellen, wenn Sie eindeutig sind. 
    
      - Um Benutzer auszuwählen, wählen Sie **Der Empfänger ist** aus. Wählen Sie im folgenden Dialogfeld in der Benutzerauswahlliste den bzw. die Absender in Ihrem Unternehmen aus, und klicken Sie dann auf **Hinzufügen**. Wenn Sie Absender hinzufügen möchten, die nicht in der Liste enthalten sind, geben Sie deren E-Mail-Adressen ein, und klicken Sie auf **Namen überprüfen**. In diesem Feld können Sie auch Platzhalterzeichen für mehrere E-Mail-Adressen verwenden (z. B.: \*@ _domainname_). Wenn Sie Ihre Auswahl getroffen haben, klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Gruppen auszuwählen, wählen Sie **Der Empfänger ist Mitglied von** aus, und wählen Sie dann im folgenden Dialogfeld die Gruppen aus oder geben Sie diese an. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Domänen auszuwählen, wählen Sie **Empfängerdomäne ist** aus, und fügen Sie dann im folgenden Dialogfeld die Domänen hinzu. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren.<br/><br/>Sie können Ausnahmen innerhalb der Regel erstellen. So können Sie beispielsweise Nachrichten aus allen Domänen mit Ausnahme einer bestimmten Domäne filtern. Klicken Sie auf **Ausnahme hinzufügen**, und erstellen Sie dann Ihre Ausnahmebedingungen ähnlich wie die anderen Bedingungen.<br/><br/>Das Anwenden einer Spamrichtlinie auf eine Gruppe wird nur für **E-Mail-aktivierte Sicherheitsgruppen** unterstützt. 
  
16. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Richtlinieneinstellungen angezeigt.

Die Standardrichtlinie kann nicht deaktiviert oder gelöscht werden, und benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Bei benutzerdefinierten Richtlinien können Sie die Kontrollkästchen in der Spalte **aktiviert** aktivieren oder deaktivieren. Standardmäßig sind alle Richtlinien aktiviert. Wenn Sie eine benutzerdefinierte Richtlinie löschen möchten, wählen Sie ![die Richt](media/ITPro-EAC-DeleteIcon.gif) **** Linie aus, klicken Sie auf das Symbol Löschsymbol löschen, und bestätigen Sie, dass Sie die Richtlinie löschen möchten.

> [!TIP]
>  Sie können die Priorität (laufende Reihenfolge) Ihrer benutzerdefinierten Richtlinien ändern, ![indem Sie auf](media/ITPro-EAC-UpArrowIcon.gif) den Pfeil nach ![oben und nach](media/ITPro-EAC-DownArrowIcon.gif) -unten-Symbol nach unten klicken. Die Richtlinie mit der **Priorität** **0** wird zuerst ausgeführt, gefolgt von **1**, dann **2**usw. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Konfigurieren der Richtlinien für die Spamfilterung mit Remote-PowerShell

Sie können in PowerShell auch Spamfilter Richtlinien konfigurieren und anwenden. Informationen zur Verwendung von Windows PowerShell zum Herstellen einer Verbindung mit Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Informationen dazu, wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online Protection herstellen, finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
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

Sie können erweiterte Spamfilteroptionen aktivieren, wenn Sie einen aggressiveren Ansatz für die Spamfilterung verfolgen möchten. Allgemeine Antispameinstellungen, die für die gesamte Organisation gelten, finden Sie unter [Verwenden einer Liste sicherer Adressen oder anderer Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](https://go.microsoft.com/fwlink/p/?LinkId=534224) oder [Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zum Verhindern von falsch negativen Ergebnissen](https://go.microsoft.com/fwlink/p/?LinkId=534225). Diese sind hilfreich, wenn Sie über die Steuerung auf Administratorebene verfügen und wenn Sie falsch positive Ergebnisse oder falsch negative Ergebnisse vermeiden möchten.
   
## <a name="for-more-information"></a>Weitere Informationen
<a name="sectionSection6"> </a>

[Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md)
  
[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  
[Quarantine](quarantine.md)
  
[Verwenden von sicheren Listen oder anderen Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  


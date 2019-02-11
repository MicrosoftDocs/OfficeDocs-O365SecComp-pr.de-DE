---
title: Konfigurieren von Spamfilterrichtlinien
ms.author: krowley
author: kccross
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
description: Grundlegende Spam-filtereinstellungen umfassen auswählen die Aktion, die auf Nachrichten angewendet werden, die als Spam identifiziert werden und auswählen, ob Sie Nachrichten zu filtern, die in bestimmten Sprachen geschrieben oder von bestimmten Ländern oder Regionen gesendet werden.
ms.openlocfilehash: 64b66f53bb56c404acefebd4fa9d211f5458f29f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29614479"
---
# <a name="configure-your-spam-filter-policies"></a>Konfigurieren von Spamfilterrichtlinien
  
Mit einfachen Spamfiltereinstellungen können Sie angeben, wie mit als Spam identifizierten Nachrichten verfahren werden soll, und ob Nachrichten in bestimmten Sprachen oder aus bestimmten Ländern bzw. Regionen herausgefiltert werden sollen. Die Einstellungen für die Spamfilterrichtlinie werden nur auf eingehende Nachrichten angewendet. Sie können die standardmäßige Spamfilterrichtlinie verwenden, um die unternehmensweiten Spamfiltereinstellungen zu konfigurieren und benutzerdefinierte Spamfilterrichtlinien zu erstellen und diese auf bestimmte Benutzer, Gruppen oder Domänen in Ihrer Organisation anwenden. Benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Sie können die Reihenfolge ändern, in der Ihre benutzerdefinierten Richtlinien ausgeführt werden, indem Sie die Priorität der einzelnen benutzerdefinierten Richtlinien ändern.
  
> [!IMPORTANT]
> Für Kunden der eigenständigen Exchange Online Protection (EOP)-Lösung: Standardmäßig leiten die EOP-Spamfilter als Spam erkannte Nachrichten an den Junk-E-Mail-Ordner der einzelnen Empfänger weiter. Damit die Aktion **Nachricht in Junk-E-Mail-Ordner verschieben** jedoch bei lokalen Postfächern angewendet wird, müssen Sie auf Ihren lokalen Servern Exchange-Transportregeln konfigurieren, um Spamkopfzeilen zu erkennen, die von EOP hinzugefügt wurden. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
## <a name="what-you-must-know-before-you-begin"></a>Was Sie wissen müssen, bevor Sie beginnen

Geschätzte Zeit bis zum Abschließen des Vorgangs: 30 Minuten
  
Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter Anti-Spam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-exchange-admin-center-eac-to-configure-spam-filter-policies"></a>Konfigurieren der Richtlinien für die Spamfilterung mit der Exchange-Verwaltungskonsole

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spamfilter**.
    
2. Führen Sie auf der Seite **Allgemein** eine der folgenden Aktionen aus: 
    
      - Doppelklicken Sie auf die Standardrichtlinie, um diese unternehmensweite Richtlinie zu bearbeiten.
    
      - Klicken Sie auf das Symbol für ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) **Neu**, um eine neue benutzerdefinierte Richtlinie für die Spamfilterung zu erstellen, die auf Benutzer, Gruppen und Domänen in Ihrer Organisation angewendet werden kann. Die können auch vorhandene benutzerdefinierte Richtlinien bearbeiten, in dem Sie darauf doppelklicken. 
    
3. Geben Sie für benutzerdefinierte Richtlinien einen Namen für diese Richtlinie. Optional können Sie auch eine ausführlichere Beschreibung angeben. Die Standardrichtlinie kann nicht umbenannt werden.<br/><br/>Hinweis: Wenn Sie eine Richtlinie erstellen, werden alle Konfigurationseinstellungen auf einem einzelnen Bildschirm angezeigt. Wenn Sie eine Richtlinie bearbeiten, müssen Sie dagegen über mehrere Bildschirme navigieren. Die Einstellungen in beiden Fällen gleich sind, aber die restlichen Schritte dieses Verfahrens wird beschrieben, wie diese Einstellungen zugreifen, wenn Sie eine Richtlinie bearbeiten. 
  
4. Wählen Sie auf der Seite **e-Mail-Aktionen, Spam und Massen** unter **Spam** und **Vertrauenswürdige Spam**die durchzuführende für eingehende e-Mails von Spam und Massen. **Verschieben von Nachrichten an den Junk-e-Mail-Ordner** ist standardmäßig aktiviert. Die anderen möglichen Werte sind: 
    
      - **Nachricht löschen** Löscht die gesamte Nachricht, einschließlich aller Anlagen. 
        
      - **Nachricht in Quarantäne verschieben** Verschiebt die Nachricht in Quarantäne, anstatt sie an die vorgesehenen Empfänger zu senden. Geben Sie bei Auswahl dieser Option im Eingabefeld **Spamnachrichten aufbewahren für (Tage)** die Anzahl der Tage an, für die die Nachricht in Quarantäne bleiben soll. (Nach Ablauf des angegebenen Zeitraums wird die Nachricht automatisch gelöscht. Der Standardwert beträgt 15 Tage, dies ist der Maximalwert. Der Mindestwert ist 1 Tag.)<br/><br/>Tipp: Informationen dazu, wie Administratoren e-Mails verwalten können, die sich in der Quarantäne in der Exchange-Verwaltungskonsole befinden, finden Sie unter [Quarantäne](quarantine.md) und [finden und Freigeben von Nachrichten in Quarantäne als Administrator](find-and-release-quarantined-messages-as-an-administrator.md). > Informationen zur Konfiguration von Nachrichten an Benutzer gesendet werden finden Sie unter [Configure End-User Spam Notifications in EOP-](configure-end-user-spam-notifications-in-eop.md) oder [Configure End-User Spam-Benachrichtigungen in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
      - **Nachricht in Junk-E-Mail-Ordner verschieben** Sendet Nachrichten an den Ordner "Junk-E-Mail" der angegebenen Empfänger. Dies ist die Standardaktion für beide Schwellenwerte für die Vertrauenswürdigkeit.<br/><br/>**Wichtig: Für Kunden mit Exchange Online Protection (EOP): In der Reihenfolge für die Aktion zum Arbeiten mit lokalen Postfächern, müssen Sie zwei Exchange-Transportregeln auf Ihren lokalen Servern zum Erkennen von Spam-Headern von EOP hinzugefügte konfigurieren. Weitere Informationen hierzu finden Sie unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).**
  
      - **X-Header hinzufügen** Die Nachricht an die angegebenen Empfänger gesendet, aber der Nachrichtenkopf, um die Nachricht als Spam identifiziert X-Header Text hinzugefügt. Verwenden diesen Text als Bezeichner, können Sie optional Posteingangsregeln erstellen oder ein downstream-Gerät verwendet werden, die für die Nachricht fungiert. Der X-Header Standardtext ist **Diese Meldung wird angezeigt, um Spam handelt**.<br/>Sie können den X-Headertext mithilfe das **Hinzufügen dieser X - Headertext** Eingabefeld anpassen. Wenn Sie den X-Headertext anpassen, beachten Sie Folgendes: 
    
      - Wenn Sie nur die Kopfzeile im Format angeben \< *Header*\>, wobei es keine Leerzeichen innerhalb sind der \< *Header*\>, ein Doppelpunkt wird auf den benutzerdefinierten Text, gefolgt von den Standardtext angefügt werden. Angenommen, wenn Sie "This-ist-meine-Custom-Header" angeben, der X-Header-Text wird angezeigt als "This-ist-meine-Custom-Header: Diese Meldung wird angezeigt, um Spam handelt."       
        
      - Wenn Sie Leerzeichen im benutzerdefinierten Headertext enthalten, oder wenn Sie den Doppelpunkt selbst hinzufügen (z. B. "X Dies ist die benutzerdefinierte Kopfzeile" oder "X-This-is-my-custom-header:"), der X-Header-Text wird wieder auf den Standardwert als "X-dieser-ist-Spam: Diese Meldung wird angezeigt, um Spam handelt."
    
      - Ist nicht möglich, geben Sie den Headertext im Format \< *Header*  \>:\<  *Wert*  \>. Wenn Sie dies tun, beide Werte, die vor und nach der Doppelpunkt ignoriert wird und der Standardtext X-Header stattdessen angezeigt: "X-dieser-ist-Spam: Diese Meldung wird angezeigt, um Spam handelt." 
      
      - Beachten Sie, dass e-Mails mit diesen X-Header weiterhin auf Junk-e-Mail-Postfachordner aufgrund von Junk-e-Konfiguration für Postfächer verschoben werden können. Sie können dies durch Deaktivieren dieser Funktion mit Set-MailboxJunkEmailConfiguration ändern.
        
      - **Prepend Betreffzeile mit text** Sendet die Nachricht an die vorgesehenen Empfänger, aber die Betreffzeile mit dem Text, den Sie in das **Präfix für Betreff mit diesem Text** Eingabefeld angeben voranzustellen. Verwenden diesen Text als Bezeichner, können Sie optional erstellen Regeln zum Filtern und Weiterleiten von Nachrichten nach Bedarf. 
        
      - **Nachricht an E-Mail-Adresse umleiten** Sendet die Nachricht an eine ausgewählte E-Mail-Adresse anstatt an die vorgesehenen Empfänger. Geben Sie im Eingabefeld **Nachricht an E-Mail-Adresse umleiten** die Adresse ein, an die die Umleitung erfolgen soll.<br/><br/>Hinweis: Weitere Informationen zu Spam Confidence Levels, finden Sie unter [Spam Confidence Levels](spam-confidence-levels.md). 
  
5. Unter **Bulk E-Mail** können Sie einen Schwellenwert auswählen, ab dem Massen-E-Mails wie Spam behandelt werden sollen. Dieser Schwellenwert basiert auf dem BCL-Wert (Bulk Complaint Level) der Nachricht. Sie können eine Schwellenwerteinstellung zwischen 1-9 auswählen, wobei 1 die meisten Massensendungen als Spam markiert und 9 die meisten Massensendungen als übermittelbar zulässt. Der Dienst führt dann die konfigurierte Aktion aus, z. B. das Senden der Nachricht in den Junk-E-Mail-Ordner des Empfängers. Weitere Informationen finden Sie unter [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md) und [Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?](what-s-the-difference-between-junk-email-and-bulk-email.md). 
    
6. Auf der Seite **Sperrlisten** können Sie Einträge, wie z. B. Absender oder Domänen, angeben, die immer als Spam markiert werden. Der Dienst wendet die konfigurierte Spamaktion bei hoher Vertrauenswürdigkeit auf E-Mails an, die diesen Einträgen entsprechen. 
    
      - Fügen Sie der Absendersperrliste unerwünschte Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren. 
        
      - Fügen Sie der Domänensperrliste unerwünschte Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie blockieren möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf **OK**, um zur Seite **Sperrlisten** zurückzukehren.<br/><br/>**Vorsicht: Wenn Sie Domänen der obersten Ebene blockieren, ist es wahrscheinlich, dass Sie die gewünschten e-Mail als Spam markiert wird.** 
  
7. Auf der Seite **Zulassungslisten** können Sie Einträge angeben, z. B. Absender oder Domänen, die immer an den Posteingang übermittelt werden. E-Mails von diesen Einträgen werden nicht vom Spamfilter verarbeitet. 
    
      - Fügen Sie der Zulassungsliste für Absender vertrauenswürdige Absender hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Absenderadressen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK", um zur Seite **Zulassungslisten** zurückzukehren. 
        
      - Fügen Sie der Zulassungsliste für Domänen vertrauenswürdige Domänen hinzu. Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und fügen Sie dann im Auswahldialogfeld die Domänen hinzu, die Sie zulassen möchten. Sie können mehrere Einträge mithilfe eines Semikolons oder einer neuen Zeile trennen. Klicken Sie auf „OK", um zur Seite **Zulassungslisten** zurückzukehren.<br/><br/>**Vorsicht: Wenn Sie Domänen der obersten Ebene zulassen, ist es wahrscheinlich, dass e-Mail, die Sie nicht möchten, mit einem Posteingang zugestellt werden.** 
  
8. Auf der Seite **Internationale Spamnachrichten** können Sie nach in bestimmten Sprachen verfassten oder aus spezifischen Ländern oder Regionen gesendeten E-Mails filtern. Es können bis zu 86 Sprachen und 250 Regionen konfiguriert werden. Der Dienst wendet dann die konfigurierte Aktion für Spam mit hoher Vertrauenswürdigkeit an. 
    
9. Aktivieren Sie das Kontrollkästchen **Filter e-Mail-Nachrichten in den folgenden Sprachen geschrieben** , um diese Funktionalität zu aktivieren. Klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann im Dialogfeld Auswahl Stellen Ihrer Auswahl (Mehrfachauswahl wird unterstützt). Beispielsweise werden, wenn Sie zum Filtern von Nachrichten in Arabisch (AR) geschrieben, und **in Quarantäne verschobene Nachricht** die konfigurierten Aktion für vertrauenswürdige Spamnachrichten ist, in Arabisch geschriebenen Nachrichten unter Quarantäne gestellt werden. Klicken Sie auf **ok,** um in den Bereich **International Spam** zurückzugeben. 
    
10. Aktivieren Sie das Kontrollkästchen **Filter e-Mail-Nachrichten aus den folgenden Ländern oder Regionen gesendet** , um diese Funktionalität zu aktivieren. Klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann im Dialogfeld Auswahl Stellen Ihrer Auswahl (Mehrfachauswahl wird unterstützt). Beispielsweise wird Wenn Sie auswählen, dass um alle Nachrichten zu filtern, die aus Australien (AU) gesendet werden, und **in Quarantäne verschobene Nachricht** die konfigurierten Aktion für vertrauenswürdige Spamnachrichten, und klicken Sie dann auf alle Nachrichten, die aus Australien gesendet wird unter Quarantäne gestellt werden. Klicken Sie auf **ok,** um in den Bereich **International Spam** zurückzugeben.<br/><br/>Wenn keine internationalen Spamoptionen ausgewählt sind, wendet der Dienst standardmäßig die normale Spamfilterung auf gesendete Nachrichten in allen Sprachen und aus allen Regionen an. Nachrichten werden untersucht und die konfigurierten Aktionen angewendet, wenn die Nachricht als Spam oder Spam mit hoher Vertrauenswürdigkeit eingestuft wird. 
  
11. Auf der Seite **Erweiterte Optionen** können Sie **Ein**, **Aus** oder **Test** für jede erweiterte Spamfilteroption auswählen. 
    
12. **Klicken Sie auf** Nachrichten werden aktiv gemäß der Regel gefiltert, die die Option zugeordnet ist. Nachrichten werden entweder als Spam markiert oder werden haben ihre Spam-Faktoren erhöht, je nach den, die Optionen, die Sie aktivieren. 
    
13. **Aus** Für die Nachrichten, die den Kriterien für Spam entsprechen, wird keine Aktion ausgeführt. Alle Optionen sind standardmäßig deaktiviert. 
    
14. **Test** Für Nachrichten, die Spam-Filterkriterien erfüllen, wird keine Aktion ausgeführt. Jedoch können Nachrichten von einem X-Header hinzufügen, bevor sie an den Empfänger zugestellt werden markiert werden. Dieser X-Header können Sie feststellen, welche Option ASF Übereinstimmung gefunden wurde. Wenn Sie für die erweiterten Optionen **Testen** angegeben haben, können Sie die folgenden Test Modus Einstellungen angewendet werden soll, wenn eine Übereinstimmung, auf die Option Test aktiviert vorliegt konfigurieren: 
    
      - **Keine** Es werden keine Testmodusaktionen bezüglich der Nachricht ausgeführt. Hierbei handelt es sich um die Standardeinstellung. 
        
      - **Hinzufügen der Standardwert X - Headertext testen** Durch Auswählen dieser Option sendet die Nachricht an die angegebenen Empfänger, aber auch die Nachricht für die Identifizierung als eine bestimmte erweiterte spamfilterungsoption übereinstimmen müssen einen speziellen X-Header hinzugefügt. 
        
      - **Bcc-Nachricht an diese Adresse senden** Durch Auswählen dieser Option sendet eine Blindkopie der Nachricht an die e-Mail-Adresse, die Sie im Eingabefeld angeben. <br/><br/>Weitere Informationen zu den erweiterten spamfilteroptionen, einschließlich Beschreibungen zu jeder Option und die X-Headertext jedem Befehl zugeordnet ist finden Sie unter [Erweiterte Spamfilterung Optionen](advanced-spam-filtering-asf-options.md). 
  
15. Für benutzerdefinierte Richtlinien nur, klicken Sie auf das Menüelement **für übernehmen** , und klicken Sie dann Erstellen einer Bedingung-basierte Regel zum Angeben der Benutzer, Gruppen und Domänen, mit denen diese Richtlinie angewendet werden. Sie können mehrere Bedingungen erstellen, wenn sie eindeutig sind. 
    
      - Um Benutzer auszuwählen, wählen Sie **Der Empfänger ist** aus. Wählen Sie im folgenden Dialogfeld in der Benutzerauswahlliste den bzw. die Absender in Ihrem Unternehmen aus, und klicken Sie dann auf **Hinzufügen**. Wenn Sie Absender hinzufügen möchten, die nicht in der Liste enthalten sind, geben Sie deren E-Mail-Adressen ein, und klicken Sie auf **Namen überprüfen**. In diesem Feld können Sie auch Platzhalterzeichen für mehrere E-Mail-Adressen verwenden (z. B.: \*@ _domainname_). Wenn Sie Ihre Auswahl getroffen haben, klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Gruppen auszuwählen, wählen Sie **Der Empfänger ist Mitglied von** aus, und wählen Sie dann im folgenden Dialogfeld die Gruppen aus oder geben Sie diese an. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren. 
        
      - Um Domänen auszuwählen, wählen Sie **Empfängerdomäne ist** aus, und fügen Sie dann im folgenden Dialogfeld die Domänen hinzu. Klicken Sie auf **OK**, um zum Hauptbildschirm zurückzukehren.<br/><br/>Sie können Ausnahmen innerhalb der Regel erstellen. So können Sie beispielsweise Nachrichten aus allen Domänen mit Ausnahme einer bestimmten Domäne filtern. Klicken Sie auf **Ausnahme hinzufügen**, und erstellen Sie dann Ihre Ausnahmebedingungen ähnlich wie die anderen Bedingungen.<br/><br/>Das Anwenden einer Spamrichtlinie auf eine Gruppe wird nur für **E-Mail-aktivierte Sicherheitsgruppen** unterstützt. 
  
16. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Richtlinieneinstellungen angezeigt.

> [!TIP]
>  Sie können die Kontrollkästchen in der Spalte **AKTIVIERT** aktivieren beziehungsweise deaktivieren, um Ihre benutzerdefinierten Richtlinien zu aktivieren oder zu deaktivieren. Alle Richtlinien sind standardmäßig aktiviert, und die Standardrichtlinie kann nicht deaktiviert werden. >  Um eine benutzerdefinierte Richtlinie zu löschen, wählen Sie die Richtlinie aus, klicken Sie auf das Symbol ![Löschen (Symbol)](media/ITPro-EAC-DeleteIcon.gif) **Löschen**, und bestätigen Sie dann, dass Sie die Richtlinie löschen möchten. Die Standardrichtlinie kann nicht gelöscht werden. >  Benutzerdefinierte Richtlinien haben immer Vorrang vor der Standardrichtlinie. Benutzerdefinierte Richtlinien werden in der umgekehrten Reihenfolge ausgeführt, in der sie von Ihnen erstellt wurden (von der ältesten zur neuesten). Sie können die Priorität (Ausführungsreihenfolge) Ihrer benutzerdefinierten Richtlinien aber ändern, indem Sie auf den Nach-oben-Pfeil ![NACH-OBEN-TASTE (Symbol)](media/ITPro-EAC-UpArrowIcon.gif) bzw. den Nach-unten-Pfeil ![NACH-UNTEN-TASTE (Symbol)](media/ITPro-EAC-DownArrowIcon.gif) klicken. Die Richtlinie mit der **PRIORITÄT** **0** wird zuerst ausgeführt, gefolgt von **1**, dann **2** usw. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Konfigurieren der Richtlinien für die Spamfilterung mit Remote-PowerShell

Sie können auch konfigurieren und Anwenden von Spam-Filter-Richtlinien in PowerShell. So verwenden Sie Windows PowerShell für die Verbindung zu Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Weitere Informationen zu Windows PowerShell verwenden, um die Verbindung mit Exchange Online Protection finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
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
  


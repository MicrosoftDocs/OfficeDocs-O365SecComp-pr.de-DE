---
title: Weitere Informationen zu Spoofing Intelligence
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
description: Verwenden Sie Spoof Intelligence im Security &amp; Compliance Center auf der Seite Anti-Spam-Einstellungen, um alle Absender zu Überprüfung, die entweder Domänen, die Teil Ihrer Organisation sind, Spoofing oder externe Domänen Spoofing. Spoof Intelligence ist als Teil von Office 365 Enterprise E5 oder separat im Rahmen von Advanced Threat Protection und Exchange Online Protection verfügbar.
ms.openlocfilehash: b8c791dc47198fa0da08dec1de6fdab8ebfbdb32
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214825"
---
# <a name="learn-more-about-spoof-intelligence"></a>Weitere Informationen zu Spoofing Intelligence

Verwenden Sie Spoof Intelligence im Security &amp; Compliance Center auf der **Seite Anti-Spam-Einstellungen** , um alle Absender zu Überprüfung, die entweder Domänen, die Teil Ihrer Organisation sind, Spoofing oder externe Domänen Spoofing. Spoof Intelligence ist als Teil von Office 365 Enterprise E5 oder separat im Rahmen von Advanced Threat Protection (ATP) und ab Oktober 2018 Exchange Online Protection (EOP) verfügbar. 
  
## <a name="what-types-of-email-spoofing-can-i-review-and-which-should-i-protect-against-with-spoof-intelligence"></a>Welche Arten von e-Mail-Spoofing kann ich überarbeiten und welche sollte ich gegen Spoof Intelligence schützen?

Für Domänen, die Sie besitzen, können Sie Absender überarbeiten, die Ihre Domäne spoofen, und dann auswählen, ob der Absender den Vorgang fortsetzen oder den Absender blockieren soll. Für externe Domänen können Sie die Absenderdomäne in Kombination mit der sendenden Infrastruktur zulassen, auch wenn es sich nicht um eine einzelne sendende e-Mail-Adresse handelt.
  
Wenn ein Absender eine e-Mail-Adresse gefälscht hat, scheint er e-Mails im Namen eines oder mehrerer Benutzerkonten in einer der Domänen Ihrer Organisation oder einer externen Domäne zu senden, die an Ihre Organisation sendet. Überraschenderweise gibt es einige legitime geschäftliche Gründe für Spoofing. In diesen Fällen würden Sie beispielsweise nicht verhindern, dass der Absender Ihre Domäne manipuliert:
  
- Sie haben Drittanbieter Absender, die Ihre Domäne zum Senden von Massen-e-Mails an Ihre eigenen Mitarbeiter für Unternehmensumfragen verwenden.
    
- Sie haben ein externes Unternehmen angeheuert, um Werbe-oder Produktaktualisierungen in Ihrem Namen zu erstellen und zu senden.
    
- Ein Assistent, der regelmäßig e-Mails für eine andere Person in Ihrer Organisation senden muss.
    
- Eine Anwendung, die so konfiguriert ist, dass Sie Ihre eigene Organisation vortäuscht, um interne Benachrichtigungen per e-Mail zu senden.
    
Externe Domänen senden häufig gefälschte e-Mails, und viele dieser Gründe sind legitim. Hier sind beispielsweise einige legitime Fälle, in denen externe Absender gefälschte e-Mails senden:
  
- Der Absender befindet sich in einer Diskussions-Mailingliste, und in der Mailingliste wird die e-Mail vom ursprünglichen Absender an alle Teilnehmer der Mailingliste weitergeleitet.
    
- Ein externes Unternehmen sendet e-Mails im Namen eines anderen Unternehmens (beispielsweise einen automatisierten Bericht oder ein Software-as-a-Service-Unternehmen).
    
Sie benötigen eine Möglichkeit, um sicherzustellen, dass die von legitimen spoofern gesendeten e-Mails nicht in Spamfilter in Office 365 oder externen e-Mail-Systemen eingehen. In der Regel behandelt Office 365 diese e-Mail-Nachrichten als Spam. Als Office 365-Administrator haben Sie die Möglichkeit, dies zu verhindern, indem Sie Spoof-Filter im Security &amp; Compliance Center einrichten. Wenn Sie die Domäne besitzen, können Sie SPF-, DKIM-und DMARC für diese Absender konfigurieren.
  
Andererseits müssen böswillige Spoofer, die Absender, die Ihre Domäne spoofen, oder externe Domänen zum Senden von Spam-oder Phishing-e-Mails, blockiert werden. Spoofing ist auch eine häufige Möglichkeit für Phisher, Benutzeranmeldeinformationen abzurufen. Office 365 verfügt über integrierten Schutz vor Spoofing, um Ihre Organisation vor Absender dieser böswilligen e-Mails zu schützen. Spoof Protection für die Domänen Ihrer Organisation ist immer für alle Office 365-Kunden aktiviert, und der Schutz externer Domänen ist standardmäßig für Advanced Threat Protection-Kunden und ab Oktober 2018 EOP-Kunden aktiviert. Um diesen Schutz weiter zu verstärken, teilen Sie uns mit, welche Absender autorisiert sind, die Domänen Ihrer Organisation zu fälschen und e-Mails in Ihrem Namen zu senden, und ob externe Domänen Spoofing-Berechtigungen haben. Alle e-Mails, die von einem Absender gesendet werden, den Sie nicht autorisieren, werden von Office 365 als Spam oder Spoofing behandelt. Achten Sie darauf, dass Absender Ihre Domäne spoofen, und helfen Sie uns, spoof Intelligence mithilfe des Security &amp; Compliance Centers zu verbessern.
  
## <a name="managing-spoof-intelligence-in-the-security-amp-compliance-center"></a>Verwalten von Spoof Intelligence im Security &amp; Compliance Center
<a name="Managespooflist"> </a>

Die von Ihnen festgelegte Spoof-Intelligence-Richtlinie wird immer von Office 365 erzwungen. Sie können es nicht deaktivieren, aber Sie k? nnen auswählen, wie viel Sie aktiv verwalten möchten.
  
Sie können die Absender, die Ihre Domäne spoofen, oder externe Domänen überprüfen und dann entscheiden, ob jeder Absender dies mithilfe des Security &amp; Compliance Centers tun darf. Für jedes gefälschte Benutzerkonto, das von einem Absender von Ihrer Domäne oder einer externen Domäne gefälscht wird, können Sie die Informationen in der folgenden Tabelle anzeigen.
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
|Absender  <br/> |Wird auch als wahrer Absender bezeichnet. Dies ist normalerweise die Domäne, von der die Spoof-e-Mail stammt. Office 365 bestimmt die Domäne des Pointer (PTR)-DNS-Eintrags der sendenden IP-Adresse, die Ihre Organisation manipuliert. Wenn keine Domäne gefunden wird, zeigt der Bericht stattdessen die IP-Adresse des Absenders an.  <br/> |
|Gefälschter Benutzer  <br/> |Das Benutzerkonto, das vom Absender gefälscht wird.  <br/> Nur **interne** Registerkarte. Dieses Feld enthält eine einzelne e-Mail-Adresse, oder wenn der Absender mehrere Benutzerkonten vortäuscht, **** enthält er mehrere.<br/> Nur **externe** Registerkarte. Externe Domänen enthalten nur eine sendende Domäne und enthalten keine vollständige e-Mail-Adresse.<br/> **Tipp! Für erweiterte Administratoren.** Der gefälschte Benutzer ist die von (5322. from)-Adresse, die auch die Adresse ist, die vom e-Mail-Client als Absenderadresse angezeigt wird. Dies wird manchmal auch als Kopfzeile. von-Adresse bezeichnet. Die Gültigkeit dieser Adresse wird nicht von SPF überprüft.           |
|Anzahl der Nachrichten  <br/> |Die Anzahl von e-Mail-Nachrichten, die der Absender innerhalb der letzten 30 Tage an Ihre Organisation gesendet hat.  <br/> |
|Anzahl der Benutzer Reklamationen  <br/> |Beschwerden, die von Benutzern in den letzten 30 Tagen gegen diesen Absender von Ihren Benutzern eingereicht wurden. Reklamationen sind in der Regel in Form von Junk-Übermittlungen an Microsoft.  <br/> |
|Authentifizierungsergebnis  <br/> |Dieser Wert wird **übergeben** , wenn der Absender die Exchange Online Protection (EoP)-Authentifizierungsüberprüfung (SPF oder DKIM) **** erfolgreich durchgeführt hat, wenn der Absender EoP-Absender Authentifizierungsprüfungen fehlgeschlagen ist, oder **unbekannt** , ob das Ergebnis dieser Prüfungen nicht bezeichnet.  <br/> |
|Entscheidungssatz durch  <br/> |Zeigt an, ob der Office 365-Administrator oder die Spoof Intelligence-Richtlinie bestimmt hat, ob der Absender den Benutzer spoofen darf.  <br/> |
|Zuletzt gesehen  <br/> |Das letzte Datum, an dem eine Nachricht von diesem Absender im Namen dieses gefälschten Benutzers empfangen wurde.  <br/> |
|Darf gefälscht werden?  <br/> | Zeigt an, ob dieser Absender e-Mails im Namen des gefälschten Benutzers senden darf. Mögliche Werte sind:<br/> **Ja** Alle gefälschten Adressen von diesem Spoofing-Absender können Ihre Organisation fälschen.  <br/> **Nein** Gefälschte Adressen von diesem Spoofing-Absender können Ihre Organisation nicht fälschen. Stattdessen werden Nachrichten von diesem Absender von Office 365 als Spam markiert.<br/> **Einige Benutzer** Wenn ein Absender mehrere Benutzer manipuliert, können einige gefälschte Adressen dieses Absenders Ihre Organisation fälschen, der Rest wird als Spam markiert. Verwenden Sie die Registerkarte **detaillierte** , um die spezifischen Adressen anzuzeigen.<br/> |
|Spoof-Typ  <br/> |Dieser Wert ist **internal** , wenn es sich bei der Domäne um eine der in der Organisation festgestellten Domänen handelt, andernfalls ist der Wert **extern**.  <br/> |
   
 **So verwalten Sie Absender, die Ihre Domäne mithilfe des Security &amp; Compliance Centers spoofen**
  
1. Wechseln Sie zum [Security &amp; Compliance Center](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Geschäfts-oder Schulkonto bei Office 365 an. Ihr Konto benötigt Administratoranmeldeinformationen in Ihrer Office 365-Organisation.
    
3. Erweitern Sie im &amp; Security Compliance Center die Option **Anti-Spam**für die **Threat Management** \> **Policy** \> .  
  
    ![Screenshot mit Zugriff auf die Anti-Spam-Seite](media/0a098e68-5ecf-40d7-984f-d15fcc1f958d.jpg)
  
4. Wählen Sie **** auf der Seite Antispameinstellungen im rechten Bereich die Registerkarte **Benutzerdefiniert** aus, und führen Sie dann einen Bildlauf nach unten durch, und erweitern Sie **Spoof Intelligence Policy**.  
  
    ![Screenshot mit Zugriff auf die benutzerdefinierten Anti-Spam-Einstellungen](media/a5112100-0b37-460f-932d-5b2f98157871.jpg)
  
5. Zum Anzeigen der Liste der Absender, die Ihre Domäne spoofen, wählen Sie **neue Absender überprüfen** und dann die Registerkarte **Domänen** aus. 
    
    Wenn Sie Absender bereits überprüft haben und einige der vorherigen Optionen ändern möchten, können Sie stattdessen die Option **mir bereits überprüfte Absender anzeigen** auswählen. In beiden Fällen wird das folgende Fenster angezeigt.  
  
    ![Screenshot mit Zugriff auf die Registerkarte "gefälschte Absender"](media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)
  
    Jeder gefälschte Benutzer wird in einer separaten Zeile angezeigt, sodass Sie auswählen können, ob der Absender zulassen oder blockieren soll, dass jeder Benutzer einzeln gefälscht wird.  
  
    Wenn Sie einen Absender zur Zulassungsliste für einen Benutzer hinzufügen möchten, wählen Sie in der Spalte **zulässig bis Spoof** die Option **Ja** aus. Wenn Sie einen Absender zur Sperrliste für einen Benutzer hinzufügen möchten, wählen Sie **Nein**aus.
     
    Um die Richtlinie für Domänen festzulegen, die Sie nicht besitzen, wählen Sie die Registerkarte **externe Domänen** aus. ändern Sie einen beliebigen Absender in der Spalte **zulässig zu Spoof** auf **Ja** , damit dieser Absender nicht authentifizierte e-Mails an Ihre Organisation senden kann. Alternativ dazu, wenn Sie der Meinung sind, dass Office 365 einen Fehler gemacht hat, dass der Absender gefälschte e-Mails senden kann, ändern Sie die Spalte **zulässig in Spoof** auf **Nein**.  
  
    ![Screenshot, der angibt, ob ein Absender Spoofing erlaubt](media/5dbef9cf-103f-49cd-9638-4b0083d6baa7.jpg)
  
6. Klicken Sie auf **Speichern** , um alle Änderungen zu speichern. 

Wenn Sie über ein Office 365 Enterprise E5-Abonnement verfügen oder den Advanced Threat Protection als Add-on separat erworben haben, können Sie auch Absender verwalten, die Ihre Domäne über [Spoof Intelligence Insight](https://docs.microsoft.com/en-us/office365/securitycompliance/walkthrough-spoof-intelligence-insight)Spoofing.
    
## <a name="configuring-the-anti-spoofing-policy"></a>Konfigurieren der Richtlinie zum Schutz vor Spoofing
<a name="Managespooflist"> </a>

Zusätzlich zum Zulassen oder Blockieren eines bestimmten Absenders beim Senden von gefälschten e-Mails in Ihre Organisation können Sie auch konfigurieren, wie streng der Filter sein soll und welche Aktion ausgeführt werden soll, wenn eine Spoofing-Nachricht gefunden wird.
  
Schutz vor Spoofing wird auf e-Mails von Absendern von Domänen angewendet, die sich außerhalb Ihrer Office 365-Organisation befinden. Sie können die Richtlinie auf Empfänger anwenden, deren Postfächer für Office 365 Enterprise E5, Advanced Threat Protection und ab Oktober 2018 EOP-Kunden lizenziert sind. Sie verwalten die Richtlinie zum Schutz vor Spoofing zusammen mit den anderen Anti-Phishing-Einstellungen. Weitere Informationen zu Anti-Phishing-Einstellungen finden Sie unter [Einrichten der Office 365-Richtlinien zum Schutz](https://support.office.com/article/set-up-office-365-atp-anti-phishing-policies-5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578?ui=en-US&amp;rs=en-US&amp;ad=US#phishpolicyoptions)vor Phishing.
  
Office 365 enthält standardmäßigen Schutz vor Spoofing, der immer läuft. Dieser Standardschutz ist im Security &amp; Compliance Center nicht sichtbar oder kann über Windows PowerShell-Cmdlets abgerufen werden. Sie können den standardmäßigen Schutz vor Spoofing nicht ändern. Stattdessen können Sie konfigurieren, wie strikt Office 365 den Schutz vor Spoofing in jeder von Ihnen erstellten Anti-Phishing-Richtlinie erzwingt. 
  
Auch wenn die Richtlinie zum Schutz vor Spoofing im Security &amp; Compliance Center unter der Richtlinie zum Schutz vor Phishing angezeigt wird, erbt sie nicht Ihr Standardverhalten von der vorhandenen Phishing-Einstellung unter der Anti-Spam-Konfiguration. Wenn Sie Einstellungen unter **Anti-Spam** \> - **Phishing** haben, die Sie für Antispoofing replizieren möchten, müssen Sie eine Anti-Phishing-Richtlinie erstellen und dann den Spoof-Teil der Anti-Phishing-Richtlinie bearbeiten, um Ihre Spoof-Einstellungen widerzuspiegeln. Im folgenden Abschnitt beschrieben, statt die Standardeinstellungen zu akzeptieren, die im Hintergrund ausgeführt werden. 
  
 **So konfigurieren Sie den Schutz vor Spoofing innerhalb einer Anti-Phishing-Richtlinie mithilfe des &amp; Security Compliance Centers**
  
1. Wechseln Sie zum [Security &amp; Compliance Center](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Geschäfts-oder Schulkonto bei Office 365 an. Ihr Konto benötigt Administratoranmeldeinformationen in Ihrer Office 365-Organisation.
    
3. Erweitern Sie im &amp; Security Compliance Center **Threat Management** \> **Policy** \> **Anti-Phishing**. 
    
4. Wählen Sie auf der Seite **Anti-Phishing** im rechten Bereich die zu konfigurierende Anti-Phishing-Richtlinie aus. 
    
5. Klicken Sie auf der angezeigten Seite in der Zeile **Spoof** auf **Bearbeiten**. 
    
6. Konfigurieren Sie als nächstes die Aktionen, die ausgeführt werden sollen, wenn eine Nachricht als domänenübergreifende Parodie erkannt wird. Das Standardverhalten besteht darin, die Nachricht in den Junk-e-Mail-Ordner des Empfängers zu verschieben. Die andere Option besteht darin, die Nachricht an die Quarantäne zu senden. Weitere Informationen zum Verwalten von Nachrichten, die an die Quarantäne gesendet werden, finden Sie unter Isolieren von [e-Mail-Nachrichten in Office 365](quarantine-email-messages.md).  
  
    ![Screenshot mit Richtlinienbearbeitungsoptionen für das Spoofing](media/7a868dff-2c4b-46b9-88ca-f2d523ca2307.jpg)
  
7. Treffen Sie Ihre Wahl, und wählen Sie dann **Speichern**aus. 
    
## <a name="other-ways-to-manage-spoofing-and-phishing-with-office-365"></a>Weitere Möglichkeiten zum Verwalten von Spoofing und Phishing mit Office 365
<a name="Managespooflist"> </a>

Bemühen Sie sich um Spoofing und Phishingschutz. Hier finden Sie verwandte Methoden zum Überprüfen von Absendern, die Ihre Domäne spoofen, und verhindern, dass Sie Ihre Organisation beschädigen:
  
- Überprüfen Sie den Bericht Exchange Online Protection Spoof-e-Mail als Teil Ihrer Routine. Sie können diesen Bericht häufig verwenden, um gefälschte Absender anzuzeigen und zu verwalten. Weitere Informationen finden Sie unter **Spoof-e-Mail-Bericht** in [use-e-Mail-Schutz berichte in Office 365 zum Anzeigen von Daten über Schadsoftware, Spam und Regel](https://technet.microsoft.com/library/dn500744%28v=exchg.150%29.aspx)Erfassungen.
    
Für fortgeschrittenere Office 365-Administratoren können Sie diese Überprüfungen auch ausführen:
    
    
- Überdenken Sie Ihre SPF-Konfiguration (Sender Policy Framework). Eine kurze Einführung in SPF und eine schnelle Konfiguration finden Sie unter [Set up SPF in Office 365, um Spoofing zu verhindern](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Ein tieferes Verständnis dafür, wie Office 365 SPF verwendet, oder für die Problembehandlung oder nicht standardmäßige Bereitstellungen wie hybridbereitstellungen, beginnen Sie mit der [Verwendung von Sender Policy Framework (SPF) durch office 365, um Spoofing zu verhindern](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).
    
- Überarbeiten Sie Ihre DomainKeys Identified Mail (DKIM)-Konfiguration. Sie sollten DKIM zusätzlich zu SPF und DMARC verwenden, um zu verhindern, dass Spoofer Nachrichten senden, die so aussehen, als würden Sie von Ihrer Domäne kommen. DKIM ermöglicht das Hinzufügen einer digitalen Signatur zu e-Mail-Nachrichten im Nachrichtenkopf. Weitere Informationen finden Sie unter [Verwenden von DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer Domäne in Office 365 gesendet werden](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).
    
- Überprüfung der Konfiguration der domänenbasierten Nachrichtenauthentifizierung,-Berichterstellung und-Konformität (DMARC). Die Implementierung von DMARC mit SPF und DKIM bietet zusätzlichen Schutz vor Spoofing-und Phishing-e-Mails. DMARC unterstützt das Empfangen von e-Mail-Systemen bestimmen, was mit Nachrichten von Ihrer Domäne gesendet wird, die SPF-oder DKIM-Prüfungen nicht durchführen. Weitere Informationen finden Sie unter [Verwenden von DMARC zum Überprüfen von e-Mails in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
- Verwenden Sie das Windows PowerShell [-Cmdlet Get-PhishFilterPolicy](https://technet.microsoft.com/en-us/library/mt735158%28v=exchg.160%29.aspx) , um detaillierte Daten zu gefälschten Absendern zu sammeln, Zulassungs-und Sperrlisten zu generieren und um festzulegen, wie Sie umfassendere SPF-, DKIM-und DMARC-DNS-Einträge generieren können, ohne dass Ihre legitime e-Mails werden in externen Spamfiltern erfasst. Weitere Informationen finden Sie unter [Funktionsweise des Antispoofing-Schutzes in Office 365](https://blogs.msdn.microsoft.com/tzink/2016/02/23/how-antispoofing-protection-works-in-office-365/).
    


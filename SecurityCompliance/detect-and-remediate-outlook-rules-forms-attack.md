---
title: Identifizieren und Beheben von Outlook-Regeln und benutzerdefinierten Formularen Injection-Angriffen in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Erfahren Sie, wie Sie die Outlook-Regeln und benutzerdefinierte Formulare Injections-Angriffe in Office 365 erkennen und beheben können.
ms.openlocfilehash: 59d45e50e15e3709c8a041ead59b8cc6e2a38306
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2019
ms.locfileid: "30656061"
---
# <a name="detect-and-remediate-outlook-rules-and-custom-forms-injections-attacks-in-office-365"></a>Erkennen und Korrigieren von Outlook-Regeln und benutzerdefinierten Formularen für Einschleusungsangriffe in Office 365

**Zusammenfassung** Erfahren Sie, wie Sie die Outlook-Regeln und benutzerdefinierte Formulare Injections-Angriffe in Office 365 erkennen und beheben können.

## <a name="what-is-the-outlook-rules-and-custom-forms-injection-attack"></a>Was ist die Outlook-Regeln und benutzerdefinierte Formulare Injection-Angriff?
Nachdem ein Angreifer ein Konto in Ihrem Mandanten verletzt hat und einsetzt, werden Sie versuchen, eine Möglichkeit einzurichten, um sich wieder einzulassen, nachdem Sie erkannt und entfernt wurden. Dies wird als Einrichten eines Persistenz-Mechanismus bezeichnet. Dies können Sie auf zweiErlei Weise tun, indem Sie Outlook-Regeln ausnutzen oder benutzerdefinierte Formulare in Outlook einfügen.
In beiden Fällen wird die Regel oder das Formular vom Cloud-Dienst bis zum Desktop Client synchronisiert, sodass ein vollständiges Format und eine erneute Installation der Client Software den Injektions Mechanismus nicht eliminiert. Der Grund ist, dass beim erneuten Verbinden der Outlook-Client Software mit dem Postfach in der Cloud die Regeln und Formulare erneut aus der Cloud heruntergeladen werden. Sobald die Regeln und Formulare vorhanden sind, verwendet der Angreifer Sie zum Ausführen von Remote-oder benutzerdefinierten Code, in der Regel zur Installation von Schadsoftware auf dem lokalen Computer. Die Schadsoftware stiehlt dann Anmeldeinformationen erneut oder führt andere illegale Aktivitäten aus. Die gute Nachricht ist, dass Sie bei der Aktualisierung Ihrer Clients auf die neueste Version nicht anfällig für die Bedrohung sind, da die aktuellen Outlook-Client Standardwerte beide Mechanismen blockieren. 

Die Angriffe folgen in der Regel folgenden Mustern:

Die Regel ausNutzung
1. Der Angreifer stiehlt den Benutzernamen und das Kennwort eines Benutzers.
2. Der Angreifer meldet sich dann bei diesem Benutzer-Exchange-Postfach an. Das Postfach kann entweder in Exchange Online oder lokal in Exchange vorhanden sein.
3. Der Angreifer erstellt dann eine Weiterleitungsregel im Postfach, die ausgelöst wird, wenn das Postfach eine e-Mail erhält, die den Kriterien der Regel entspricht. Die Kriterien von Rule und der Inhalt der Trigger-e-Mails sind für jeden anderen maßgeschneidert.
4. Der Angreifer sendet die Trigger-e-Mail an den Benutzer, der sein Postfach normal verwendet.
5. Wenn die e-Mail empfangen wird, wird die Regel ausgelöst. Die Regel besteht darin, eine Anwendung auf einem Remoteserver (WebDAV) zu starten.
6. Die Anwendung installiert normalerweise Schadsoftware wie [PowerShell Empire](https://www.powershellempire.com/)lokal auf dem Computer des Benutzers.
7. Mit der Schadsoftware kann der Angreifer den Benutzernamen und das Kennwort des Benutzers oder andere Anmeldeinformationen vom lokalen Computer erneut stehlen und andere böswillige Aktivitäten ausführen.

Die Formular ausNutzung
1. Der Angreifer stiehlt den Benutzernamen und das Kennwort eines Benutzers.
2. Der Angreifer meldet sich dann bei diesem Benutzer-Exchange-Postfach an. Das Postfach kann entweder in Exchange Online oder lokal in Exchange vorhanden sein.
3. Der Angreifer erstellt dann eine benutzerdefinierte e-Mail-Formularvorlage und fügt Sie in das Postfach des Benutzers ein.  Das benutzerdefinierte Formular wird ausgelöst, wenn das Postfach eine e-Mail empfängt, für die das Postfach das benutzerdefinierte Formular laden muss. Das benutzerdefinierte Formular und das e-Mail-Format sind für jeden anderen maßgeschneidert.
4. Der Angreifer sendet die Trigger-e-Mail an den Benutzer, der sein Postfach normal verwendet.
5. Wenn die e-Mail empfangen wird, wird das Formular geladen. Das Formular startet eine Anwendung auf einem Remoteserver (WebDAV).
6. Die Anwendung installiert normalerweise Schadsoftware wie [PowerShell Empire](https://www.powershellempire.com/)lokal auf dem Computer des Benutzers.
7. Mit der Schadsoftware kann der Angreifer den Benutzernamen und das Kennwort des Benutzers oder andere Anmeldeinformationen vom lokalen Computer erneut stehlen und andere böswillige Aktivitäten ausführen.


## <a name="what-a-rules-and-custom-forms-injection-attack-might-look-like-office-365"></a>Welche Regeln und benutzerdefinierten Formular Injection-Angriffe können wie Office 365 aussehen?

Diese Dauerhaftigkeitsmechanismen werden von Ihren Benutzern wahrscheinlich nicht bemerkt und können in einigen Fällen sogar unsichtbar für Sie sein.  In diesem Artikel erfahren Sie, wie Sie nach einem der folgenden sieben Zeichen (Indikatoren der Gefährdung) suchen. Wenn Sie diese finden, müssen Sie korrekturschritte ausführen.

- Indikatoren für die Kompromiss Regeln
    - Regelaktion ist das Starten einer Anwendung.
    - Regel verweist auf eine EXE, ZIP oder URL.
    - Suchen Sie auf dem lokalen Computer nach neuen Prozessstarts, die aus der Outlook-PID stammen.
- Indikatoren für die Kompromisse bei benutzerdefinierten Formularen 
    - Benutzerdefiniertes Formular wird als eigene Nachrichtenklasse gespeichert.
    - Nachrichtenklasse enthält ausführbaren Code.
    - In der Regel in der Bibliothek für persönliche Formulare oder Posteingang-Ordner gespeichert.
    - Das Formular hat den Namen IPM. Hinweis. [benutzerdefinierter Name].

## <a name="steps-for-finding-signs-of-this-attack-and-confirming-it"></a>Schritte zum Auffinden von Anzeichen für diesen Angriff und zur Bestätigung
Sie können eine der beiden folgenden Methoden verwenden, um den Angriff zu bestätigen.
- Untersuchen Sie die Regeln und Formulare für jedes Postfach mithilfe des Outlook-Clients.  Diese Methode ist gründlich, aber Sie können den Postfachbenutzer nur zu einem Zeitpunkt überprüfen, der sehr zeitaufwändig sein kann, wenn viele Benutzer überprüfen müssen.  Es kann auch zu einem Verstoß gegen den Computer führen, von dem Sie die Prüfung durchführen.
- Verwenden Sie das PowerShell-Skript [Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) , um alle e-Mail-Weiterleitungsregeln und benutzerdefinierten Formulare für alle Benutzer in Ihrem Mandanten automatisch zu dumpen. Dies ist die schnellste und sicherste Methode mit dem geringsten Aufwand.


### <a name="confirm-the-rules-attack-using-the-outlook-client"></a>Bestätigen des anGriffs auf Regeln mithilfe des Outlook-Clients
1. Öffnen Sie den Benutzer Outlook-Client als Benutzer.  Der Benutzer benötigt möglicherweise Ihre Hilfe bei der Untersuchung der Regeln für sein Postfach.
2. Weitere Informationen finden Sie unter [Verwalten von e-Mail-Nachrichten](https://support.office.com/article/manage-email-messages-by-using-rules-c24f5dea-9465-4df4-ad17-a50704d66c59#ID0EAABAAA=2010) mithilfe von Regel Artikeln für die Verfahren zum Öffnen der Regel Schnittstelle in den Versionen 2007, 2010 oder 2013 von Outlook.
3. Suchen Sie nach Regeln, die der Benutzer nicht erstellt hat, oder unerwarteten Regeln oder Regeln mit verdächtigen Namen.
4. Sehen Sie sich die Regelbeschreibung für Regelaktionen an, die gestartet und Anwendung sind, oder verweisen Sie auf. EXE,. ZIP-Datei oder zum Starten einer URL.
5. Suchen Sie nach neuen Prozessen, die mit der Outlook-Prozess-ID beginnen.  Weitere Informationen [finden Sie untersuchen der Prozess-ID](https://docs.microsoft.com/windows-hardware/drivers/debugger/finding-the-process-id).

### <a name="steps-to-confirm-the-forms-attack-using-the-outlook-client"></a>Schritte zum Bestätigen des Formular Angriffs mit dem Outlook-Client
1. Öffnen Sie den Benutzer Outlook-Client als Benutzer.
2. Führen Sie die Schritte in aus, [zeigen Sie die Registerkarte Entwicklertools](https://support.office.com/article/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) für die Benutzerversion von Outlook.
3. Öffnen Sie die Registerkarte jetzt sichtbare Entwickler in Outlook, und klicken Sie auf **Formular entwerfen**.
4. Wählen Sie den **Posteingang** aus der Liste **Suchen in** aus. Suchen Sie nach benutzerdefinierten Formularen.  Benutzerdefinierte Formulare sind selten genug, wenn Sie überhaupt benutzerdefinierte Formulare haben, ist es einen tieferen Blick Wert.
5. Untersuchen Sie alle benutzerdefinierten Formulare, insbesondere die als ausgeblendet gekennzeichnet.
6. Öffnen Sie benutzerdefinierte Formulare, und klicken Sie in der Gruppe **Formular** auf **Code anzeigen** , um zu sehen, was beim Laden des Formulars ausgeführt wird.

### <a name="steps-to-confirm-the-rules-and-forms-attack-using-powershell"></a>Schritte zum Bestätigen der Regeln und des Angriffs von Formularen mithilfe von PowerShell
Am einfachsten können Sie eine Regel oder einen benutzerdefinierten Formular Angriff überprüfen, indem Sie das PowerShell [-Skript Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) ausführen.  Dieses Skript stellt eine Verbindung zu jedem Postfach in Ihrem Mandanten her und gibt alle Regeln und Formulare in zwei CSV-Dateien aus.

#### <a name="pre-requisites"></a>Voraussetzungen
Sie müssen über ein globales Administratorrecht zum Ausführen des Skripts verfügen, da das Skript mit jedem Postfach in der Mandantschaft eine Verbindung herstellt, um die Regeln und Formulare zu lesen.

1. Melden Sie sich bei dem Computer an, von dem Sie das Skript mit lokalen Administratorrechten ausführen.
2. Laden Sie das Get-AllTenantRulesAndForms. ps1-Skript aus GitHub herunter, und kopieren Sie es in einen Ordner, von dem aus Sie es ausführen.  Das Skript erstellt zwei Datums gestempelte Dateien in diesem Ordner, MailboxFormsExport-yyyy-mm-dd. CSV und MailboxRulesExport-yyyy-mm-dd. CSV.
3. Öffnen Sie eine PowerShell-Instanz als Administrator, und öffnen Sie den Ordner, in dem Sie das Skript gespeichert haben.
4. Führen Sie diese PowerShell-Befehlszeile `.\Get-AllTenantRulesAndForms.ps1`wie folgt aus: .\Get-AllTenantRulesAndForms.ps1

#### <a name="interpreting-the-output"></a>Interpretieren der Ausgabe

MailboxRulesExport-*yyyy-mm-dd*. CSV – überprüfen Sie die Regeln (eine pro Zeile) auf Aktionsbedingungen, die Anwendungen oder ausführbare Dateien einbeziehen.
- Action Type (Spalte A) – Wenn der Wert "ID_ACTION_CUSTOM" angezeigt wird, ist die Regel wahrscheinlich bösartig.
- IsPotentiallyMalicious (Spalte D) – Wenn dieser Wert "TRUE" ist, ist die Regel wahrscheinlich bösartig.
- ActionCommand "(Spalte G) – Wenn diese eine Anwendung oder eine Datei mit der exe-, ZIP-Erweiterung oder einem Eintrag auflistet, der auf eine URL verweist, die nicht vorhanden sein soll, ist die Regel wahrscheinlich bösartig.

MailboxFormsExport-*yyyy-mm-dd*. csv – im Allgemeinen ist die Verwendung von benutzerdefinierten Formularen sehr selten.  Wenn Sie in dieser Arbeitsmappe finden, öffnen Sie das Postfach des Benutzers, und überprüfen Sie das Formular selbst.  Wenn Ihre Organisation Sie nicht absichtlich dort abgelegt hat, ist Sie wahrscheinlich bösartig.



## <a name="how-to-stop-and-remediate-the-outlook-rules-and-forms-attack"></a>Beenden und Beheben des Angriffs auf Outlook-Regeln und-Formulare
Wenn Sie einen der beiden folgenden Angriffe nachweisen können, ist die Korrektur einfach, indem Sie einfach die Regel oder das Formular aus dem Postfach löschen. Sie können dies mit dem Outlook-Client oder mit Remote-PowerShell zum Entfernen von Regeln tun.

### <a name="using-outlook"></a>Verwenden von Outlook
1. Identifizieren aller Geräte, die der Benutzer in Outlook verwendet hat.  Sie müssen alle von potentieller Schadsoftware gereinigt werden.  Lassen Sie den Benutzer erst anmelden und e-Mails verwenden, wenn alle Geräte bereinigt wurden.
2. Führen Sie die Schritte unter [Delete a Rule](https://support.office.com/article/Delete-a-rule-2F0E7139-F696-4422-8498-44846DB9067F) for each Device aus.
3. Wenn Sie sich nicht sicher sind, ob andere Schadsoftware vorhanden sind, können Sie die gesamte Software auf dem Gerät formatieren und neu installieren.  Für mobile Geräte können Sie die Schritte des Herstellers ausführen, um das Gerät auf das Factory-Image zurückzusetzen.
4. Installieren Sie die neuesten Versionen von Outlook.  Denken Sie daran, dass die aktuelle Version von Outlook beide Typen dieses Angriffs standardmäßig blockiert.
5. Nachdem alle Offlinekopien des Postfachs entfernt wurden, setzen Sie das Kennwort des Benutzers zurück (verwenden Sie eine hochwertige Kopie), und führen Sie die Schritte unter [Setup Multi-Factor Authentication for Office 365 users](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) aus, wenn MFA noch nicht aktiviert wurde. Dadurch wird sichergestellt, dass die Anmeldeinformationen des Benutzers nicht über andere Mittel (wie Phishing oder Kenn Wort Wiederverwendung) offen gelegt werden.

### <a name="using-powershell"></a>Verwendung von PowerShell
Es gibt zwei Remote-PowerShell-Cmdlets, mit denen Sie gefährliche Regeln entfernen oder deaktivieren können. Führen Sie die folgenden Schritte aus.
 
Schritte für Postfächer auf einem Exchange-Server

1. Stellen Sie mithilfe der Remote-PowerShell eine Verbindung mit dem Exchange-Server her. Führen Sie die Schritte unter [Herstellen einer Verbindung mit Exchange-Servern mithilfe der Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-server/connect-to-exchange-servers-using-remote-powershell?view=exchange-ps)aus.
2. Wenn Sie eine einzelne Regel, mehrere Regeln oder alle Regeln aus einem Postfach vollständig entfernen möchten, verwenden Sie das [Cmdlet Remove-Posteingangsregel ](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps), um eine, mehrere oder alle Regeln aus dem Postfach vollständig zu entfernen.
3. Wenn Sie die Regel und ihren Inhalt für weitere Untersuchungen behalten möchten, verwenden Sie das [Cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

Schritte für Postfächer in Exchange Online
1. Führen Sie die Schritte unter [Herstellen einer Verbindung mit Exchange Online mithilfe von PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)aus.
2.  Wenn Sie eine einzelne Regel, mehrere Regeln oder alle Regeln aus einem Postfach vollständig entfernen möchten, verwenden Sie das [Cmdlet Remove-Posteingangsregel](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps).
3.  Wenn Sie die Regel und ihren Inhalt für weitere Untersuchungen behalten möchten, verwenden Sie das [Cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

## <a name="how-to-minimize-future-attacks"></a>So minimieren Sie zukünftige Angriffe

### <a name="first-protect-your-accounts"></a>First: schützen Sie Ihre Konten

Die Regeln und Formular Angriffe werden nur von Angreifern verwendet, nachdem Sie ein Konto Ihres Benutzers gestohlen oder verletzt haben. Daher besteht der erste Schritt zur Verhinderung der Verwendung dieser Exploits für Ihre Organisation darin, ihre Benutzerkonten aggressiv zu schützen.  Zu den häufigsten Methoden für die Verletzung von Konten gehören Phishing-oder [Kenn Wort Spritzen](http://www.dabcc.com/microsoft-defending-against-password-spray-attacks/) Angriffe.



Die beste Möglichkeit zum Schützen Ihrer Benutzerkonten und insbesondere der Administratorkonten besteht darin, die [mehrstufige Authentifizierung für Office 365-Benutzer](https://support.office.com/article/set-up-multi-factor-authentication-for-office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)einzurichten.  Außerdem sollten Sie Folgendes tun:
<ol>
    <li>Überwachen Sie, wie ihre Benutzerkonten <a href="https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports">zugegriffen und verwendet</a>werden. Sie können die anfängliche Verletzung nicht verhindern, aber Sie werden die Dauer und die Auswirkungen der Verletzung verringern, indem Sie Sie früher erfassen. Sie können diese verwenden: <a href="https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475">Office 365 Cloud App-Sicherheitsrichtlinien</a> zum Überwachen von Konten und Benachrichtigungen über ungewöhnliche Aktivitäten. 
        <ol type="a">
            <li><b>Mehrere fehlgeschlagene Anmeldeversuche</b> Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Benutzer mehrere fehlgeschlagene Anmeldeaktivitäten in einer einzelnen Sitzung im Hinblick auf die erlernte Baseline ausführen, was auf eine versuchte Verletzung hindeuten könnte.</li>
            <li><b>Unmöglich Reisen</b> - Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Aktivitäten von demselben Benutzer an verschiedenen Orten innerhalb eines Zeitraums erkannt werden, der kürzer ist als die erwartete Reisezeit zwischen den beiden Speicherorten. Dies kann darauf hindeuten, dass ein anderer Benutzer die gleichen Anmeldeinformationen verwendet. Das erkennen dieses anormalen Verhaltens erfordert einen anfänglichen Lernzeitraum von sieben Tagen, in dem er das Aktivitätsmuster eines neuen Benutzers erlernt.</li>
            <li><b>Ungewöhnliche imitierte Aktivität (nach Benutzer)</b> - Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Benutzer mehrere imitierte Aktivitäten in einer einzigen Sitzung im Hinblick auf die gelernte Grundlinie ausführen, was auf eine versuchte Verletzung hindeuten könnte.</li>
        </ol>
    </li>
    <li>Nutzen Sie ein Tool wie die <a href="https://securescore.office.com/">Secure Score Office 365</a> , um Konto Sicherheitskonfigurationen und-Verhaltensweisen zu verwalten. 
    </li>
</ol> 

### <a name="second-keep-your-outlook-clients-current"></a>Zweitens: halten Sie Ihre Outlook-Clients auf dem neuesten Stand
Vollständig aktualisierte und gepatchte Versionen von Outlook 2013 und 2016 deaktivieren die Regel/Formularaktion "Anwendung starten" standardmäßig.  Dadurch wird sichergestellt, dass die Regel-und Formularaktionen auch dann blockiert werden, wenn ein Angreifer gegen das Konto verstößt.  Sie können die neuesten Updates und Sicherheitspatches installieren, indem Sie die Schritte unter [Install Office Updates](https://support.office.com/article/Install-Office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)ausführen.

Hier sind die Patch-Versionen für Ihre Outlook 2013-und 2016-Clients:
- Outlook 2013:15.0.4937.1000 oder höher
- Outlook 2016:16.0.4534.1001 oder höher

Weitere Informationen zu den einzelnen Sicherheitspatches finden Sie unter:

- [Sicherheits Patch für Outlook 2013](https://support.microsoft.com/en-us/help/3191938) 
- [Sicherheits Patch für Outlook 2016](https://support.microsoft.com/en-us/help/3191883)

### <a name="third-monitor-your-outlook-clients"></a>Drittens: Überwachen Sie Ihre Outlook-Clients
Beachten Sie, dass ein Angreifer auch bei installierten Patches und Updates die Konfiguration des lokalen Computers ändern kann, um das Verhalten "Start Anwendung" erneut zu aktivieren. Sie können die [Erweiterte Gruppenrichtlinienverwaltung](https://docs.microsoft.com/microsoft-desktop-optimization-pack/agpm/) verwenden, um lokale Computerrichtlinien auf Ihren Clients zu überwachen und zu erzwingen.  
Mithilfe der Informationen unter so [zeigen Sie die Systemregistrierung mithilfe von 64-Bit-Versionen von Windows](https://support.microsoft.com/en-us/help/305097/how-to-view-the-system-registry-by-using-64-bit-versions-of-windows)an, können Sie festzustellen, ob die "Start Anwendung" durch eine Außerkraftsetzung in der Registrierung erneut aktiviert wurde.  Überprüfen Sie die folgenden Unterschlüssel: 

- Outlook 2016: HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Security\
- Outlook 2013: HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Security\

Suchen Sie nach dem Schlüssel EnableUnsafeClientMailRules. Wenn es vorhanden ist und auf 1 festgelegt ist, wurde der Outlook-Sicherheitspatch überschrieben, und der Computer ist anfällig für den Angriffs Formular/Regeln. Wenn der Wert 0 ist, wird die Aktion "Anwendung starten" deaktiviert.  Wenn die aktualisierte und gepatchte Version von Outlook installiert ist und dieser Registrierungsschlüssel nicht vorhanden ist, ist ein System nicht anfällig für diese Angriffe.

Kunden mit lokalen Exchange-Installationen sollten in Erwägung ziehen, ältere Versionen von Outlook zu blockieren, die keine Patches zur Verfügung haben. Details zu diesem Prozess finden Sie im Artikel [configure Outlook Client Blocking](https://technet.microsoft.com/en-us/library/dd335207(v=exchg.150).aspx).

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Secure Office 365 wie ein Cyber pro
Ihr Office 365-Abonnement verfügt über eine Reihe leistungsstarker Sicherheitsfunktionen, die Sie zum Schutz Ihrer Daten und ihrer Benutzer verwenden können.  Verwenden Sie die [office 365 Security Roadmap: die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) , um die empfohlenen bewährten Methoden von Microsoft für die Sicherung ihres Office 365-Mandanten zu implementieren.
- Aufgaben, die in den ersten 30 Tagen erledigt werden müssen.  Diese haben sofortige Auswirkungen und sind für Ihre Benutzer gering.
- Aufgaben in 90 Tagen. Diese benötigen etwas mehr Zeit, um ihre Sicherheitslage zu planen und zu implementieren.
- Über 90 Tage. Diese Verbesserungen werden in den ersten 90-Tagen ausgeführt.

## <a name="see-also"></a>Siehe auch:
- [Böswillige Outlook-Regeln](https://silentbreaksecurity.com/malicious-outlook-rules/) von SilentBreak Security Post about Rules Vector bietet eine detaillierte Übersicht darüber, wie die Outlook-Regeln. 
- [MAPI über HTTP und mailrule Pwnage](https://sensepost.com/blog/2016/mapi-over-http-and-mailrule-pwnage/) auf dem Sensepost-Blog über mailrule Pwnage erörtert ein Tool mit dem Namen Lineal, mit dem Sie Postfächerüber Outlook-Regeln ausnutzen können.
- [Outlook-Formulare und-Shells](https://sensepost.com/blog/2017/outlook-forms-and-shells/) im Sensepost-Blog über Forms Threat Vector. 
- [Lineal-CodeBase](https://github.com/sensepost/ruler)
- [Lineal-Indikatoren für Kompromisse](https://github.com/sensepost/notruler/blob/master/iocs.md)
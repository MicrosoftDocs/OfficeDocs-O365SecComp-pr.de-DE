---
title: Erkennen und Beheben von Outlook-Regeln und benutzerdefinierten Formularen Injektionsangriffe in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/23/2018
audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Erfahren Sie, wie Sie die Outlook-Regeln und Injektionen von benutzerdefinierten Formularen in Office 365 erkennen und beheben können.
ms.openlocfilehash: ef2f08c953b91ccefcadd5947d2d0a9f39683ae2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150257"
---
# <a name="detect-and-remediate-outlook-rules-and-custom-forms-injections-attacks-in-office-365"></a>Erkennen und Korrigieren von Outlook-Regeln und benutzerdefinierten Formularen für Einschleusungsangriffe in Office 365

**Zusammenfassung** Hier erfahren Sie, wie Sie die Outlook-Regeln und Injektionen von benutzerdefinierten Formularen in Office 365 erkennen und beheben können.

## <a name="what-is-the-outlook-rules-and-custom-forms-injection-attack"></a>Was sind die Outlook-Regeln und der Injektions Angriff für benutzerdefinierte Formulare?
Nachdem ein Angreifer ein Konto in Ihrem Mandanten verletzt und eingeht, werden Sie versuchen, eine Möglichkeit einzurichten, in zu bleiben, oder eine Möglichkeit, wieder einzusteigen, nachdem Sie entdeckt und entfernt wurden. Dies wird als Einrichten eines Dauerhaftigkeitsmechanismus bezeichnet. Es gibt zwei Möglichkeiten, dies zu tun, indem Sie Outlook-Regeln ausnutzen oder benutzerdefinierte Formulare in Outlook einfügen.
In beiden Fällen wird die Regel oder das Formular vom clouddienst auf den Desktop Client synchronisiert, sodass ein vollständiges Format und eine erneute Installation der Client Software den Injektions Mechanismus nicht ausschließen. Dies liegt daran, dass beim Wiederherstellen der Verbindung der Outlook-Client Software mit dem Postfach in der Cloud die Regeln und Formulare erneut aus der Cloud heruntergeladen werden. Sobald die Regeln und Formulare vorhanden sind, verwendet der Angreifer Sie, um Remote-oder benutzerdefinierten Code auszuführen, normalerweise zum Installieren von Schadsoftware auf dem lokalen Computer. Die Schadsoftware stiehlt dann die Anmeldeinformationen erneut oder führt andere unerlaubte Aktivitäten aus. Die gute Nachricht hierbei ist, dass Sie, wenn Sie Ihre Clients auf die neueste Version Patchen lassen, nicht anfällig für die Bedrohung sind, da die aktuellen Outlook-Clientstandard Werte beide Mechanismen blockieren. 

Die Angriffe folgen in der Regel diesen Mustern:

Die Regeln ausnutzen
1. Der Angreifer stiehlt den Benutzernamen und das Kennwort eines Ihrer Benutzer.
2. Der Angreifer meldet sich dann beim Exchange-Postfach dieses Benutzers an. Das Postfach kann entweder in Exchange Online oder lokal in Exchange sein.
3. Der Angreifer erstellt dann eine Weiterleitungsregel im Postfach, die ausgelöst wird, wenn das Postfach eine e-Mail empfängt, die den Kriterien der Regel entspricht. Die Kriterien der Regel und der Inhalt der Trigger-e-Mail sind für einander maßgeschneidert.
4. Der Angreifer sendet die Trigger-e-Mail an den Benutzer, der sein Postfach normal verwendet.
5. Wenn die e-Mail empfangen wird, wird die Regel ausgelöst. Die Aktion der Regel besteht in der Regel darin, eine Anwendung auf einem Remoteserver (WebDAV) zu starten.
6. Die Anwendung installiert in der Regel Malware wie [PowerShell Empire](https://www.powershellempire.com/)lokal auf dem Computer des Benutzers.
7. Durch die Schadsoftware kann der Angreifer den Benutzernamen und das Kennwort des Benutzers oder andere Anmeldeinformationen vom lokalen Computer erneut stehlen und andere schädliche Aktivitäten ausführen.

Exploits für Formulare
1. Der Angreifer stiehlt den Benutzernamen und das Kennwort eines Ihrer Benutzer.
2. Der Angreifer meldet sich dann für das Exchange-Postfach dieses Benutzers an. Das Postfach kann entweder in Exchange Online oder lokal in Exchange sein.
3. Der Angreifer erstellt dann eine benutzerdefinierte e-Mail-Formularvorlage und fügt Sie in das Postfach des Benutzers ein.  Das benutzerdefinierte Formular wird ausgelöst, wenn das Postfach eine e-Mail empfängt, die erfordert, dass das Postfach das benutzerdefinierte Formular lädt. Das benutzerdefinierte Formular und das Format der e-Mail sind für einander maßgeschneidert.
4. Der Angreifer sendet die Trigger-e-Mail an den Benutzer, der sein Postfach normal verwendet.
5. Wenn die e-Mail empfangen wird, wird das Formular geladen. Das Formular startet eine Anwendung auf einem Remoteserver (WebDAV).
6. Die Anwendung installiert in der Regel Malware wie [PowerShell Empire](https://www.powershellempire.com/)lokal auf dem Computer des Benutzers.
7. Durch die Schadsoftware kann der Angreifer den Benutzernamen und das Kennwort des Benutzers oder andere Anmeldeinformationen vom lokalen Computer erneut stehlen und andere schädliche Aktivitäten ausführen.


## <a name="what-a-rules-and-custom-forms-injection-attack-might-look-like-office-365"></a>Welche Regeln und benutzerdefinierten Formular Injektionsangriffe können wie Office 365 aussehen?

Diese Dauerhaftigkeitsmechanismen werden von Ihren Benutzern kaum bemerkt und können in einigen Fällen sogar für Sie unsichtbar sein.  In diesem Artikel erfahren Sie, wie Sie nach einem der unten aufgeführten sieben Zeichen (Indikatoren für eine Gefährdung) suchen. Wenn Sie diese finden, müssen Sie korrekturschritte durchführen.

- Indikatoren für den Kompromiss in der Regel
    - Regelaktion ist das Starten einer Anwendung.
    - Regel verweist auf eine exe-, ZIP-oder URL-Adresse.
    - Suchen Sie auf dem lokalen Computer nach neuen Prozessstarts, die aus der Outlook-PID stammen.
- Indikatoren für den Kompromiss mit benutzerdefinierten Formularen 
    - Das benutzerdefinierte Formular wird als eigene Nachrichtenklasse gespeichert.
    - Nachrichtenklasse enthält ausführbaren Code.
    - In der Regel in persönlichen Formularbibliotheken oder Posteingangs Ordnern gespeichert.
    - Das Formular hat den Namen IPM. Hinweis. [benutzerdefinierter Name].

## <a name="steps-for-finding-signs-of-this-attack-and-confirming-it"></a>Schritte zum Auffinden von Anzeichen für diesen Angriff und zur Bestätigung
Sie können eine der beiden folgenden Methoden verwenden, um den Angriff zu bestätigen.
- Untersuchen Sie die Regeln und Formulare für jedes Postfach mithilfe des Outlook-Clients manuell.  Diese Methode ist gründlich, aber Sie können nur den Postfachbenutzer zu einem Zeitpunkt überprüfen, der sehr zeitaufwendig sein kann, wenn Sie viele Benutzer überprüfen müssen.  Dies kann auch zu einem Verstoß gegen den Computer führen, von dem aus Sie den Test durchführen.
- Verwenden Sie das PowerShell-Skript [Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) , um automatisch alle e-Mail-Weiterleitungsregeln und benutzerdefinierten Formulare für alle Benutzer in Ihrem Mandanten zu sichern. Dies ist die schnellste und sicherste Methode mit der geringsten Menge an Aufwand.


### <a name="confirm-the-rules-attack-using-the-outlook-client"></a>Überprüfen des Regel Angriffs mithilfe des Outlook-Clients
1. Öffnen Sie den Outlook-Clientbenutzer als Benutzer.  Der Benutzer benötigt möglicherweise Hilfe bei der Untersuchung der Regeln für sein Postfach.
2. Weitere Informationen finden Sie unter [Verwalten von e-Mail-Nachrichten mithilfe von Regel](https://support.office.com/article/manage-email-messages-by-using-rules-c24f5dea-9465-4df4-ad17-a50704d66c59#ID0EAABAAA=2010) Artikeln für die Verfahren zum Öffnen der Regel Schnittstelle in den Versionen 2007, 2010 oder 2013 von Outlook.
3. Suchen Sie nach Regeln, die der Benutzer nicht erstellt hat, oder an unerwarteten Regeln oder Regeln mit verdächtigen Namen.
4. Suchen Sie in der Regelbeschreibung nach Regelaktionen, die Start und Application oder auf eine. EXE,. ZIP-Datei oder zum Starten einer URL.
5. Suchen Sie nach neuen Prozessen, die mit der Outlook-Prozess-ID beginnen.  Lesen Sie [die Informationen zur Prozess-ID](https://docs.microsoft.com/windows-hardware/drivers/debugger/finding-the-process-id).

### <a name="steps-to-confirm-the-forms-attack-using-the-outlook-client"></a>Schritte zum Bestätigen des Formular Angriffs mit dem Outlook-Client
1. Öffnen Sie den Benutzer Outlook-Client als Benutzer.
2. Führen Sie die Schritte in aus, und [zeigen Sie die Registerkarte Entwickler](https://support.office.com/article/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) für die Outlook-Benutzerversion an.
3. Öffnen Sie die Registerkarte Entwickler jetzt sichtbar in Outlook, und klicken Sie auf **ein Formular entwerfen**.
4. Wählen Sie den **Posteingang** in der Liste **Suchen in** aus. Suchen Sie nach benutzerdefinierten Formularen.  Benutzerdefinierte Formulare sind selten genug, wenn Sie benutzerdefinierte Formulare haben, ist es ein tieferes aussehen Wert.
5. Untersuchen Sie benutzerdefinierte Formulare, insbesondere die als ausgeblendet markierten.
6. Öffnen Sie benutzerdefinierte Formulare, und klicken Sie in der Gruppe **Formular** auf **Code anzeigen** , um zu sehen, was ausgeführt wird, wenn das Formular geladen wird.

### <a name="steps-to-confirm-the-rules-and-forms-attack-using-powershell"></a>Schritte zum Überprüfen der Regeln und Formular Angriffe mithilfe von PowerShell
Die einfachste Möglichkeit, eine Regel oder einen benutzerdefinierten Formular Angriff zu überprüfen, besteht darin, das PowerShell [-Skript Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) auszuführen.  Dieses Skript stellt eine Verbindung mit jedem Postfach in Ihrem Mandanten her und dumpt alle Regeln und Formulare in zwei CSV-Dateien.

#### <a name="pre-requisites"></a>Voraussetzungen
Sie benötigen eine globale Administratorberechtigung zum Ausführen des Skripts, da das Skript eine Verbindung mit jedem Postfach in der Mandantschaft herstellt, um die Regeln und Formulare zu lesen.

1. Melden Sie sich bei dem Computer an, auf dem das Skript mit lokalen Administratorrechten ausgeführt wird.
2. Laden Sie das Get-AllTenantRulesAndForms. ps1-Skript aus GitHub in einen Ordner herunter, aus dem Sie es ausführen möchten, oder kopieren Sie es.  Das Skript erstellt zwei Datums gestempelte Dateien in diesem Ordner, MailboxFormsExport-yyyy-mm-dd. CSV und MailboxRulesExport-yyyy-mm-dd. CSV.
3. Öffnen Sie eine PowerShell-Instanz als Administrator, und öffnen Sie den Ordner, in dem Sie das Skript gespeichert haben.
4. Führen Sie diese PowerShell-Befehlszeile `.\Get-AllTenantRulesAndForms.ps1`wie folgt .\Get-AllTenantRulesAndForms.ps1

#### <a name="interpreting-the-output"></a>Interpretieren der Ausgabe

MailboxRulesExport-*yyyy-mm-dd*. CSV – untersuchen Sie die Regeln (eine pro Zeile) für Aktionsbedingungen, die Anwendungen oder ausführbare Dateien enthalten.
- Action Type (Spalte A) – Wenn der Wert "ID_ACTION_CUSTOM" angezeigt wird, ist die Regel wahrscheinlich bösartig.
- IsPotentiallyMalicious (Spalte D) – Wenn dieser Wert "true" lautet, ist die Regel wahrscheinlich bösartig.
- ActionCommand "(Spalte G) – Wenn dies eine Anwendung oder eine Datei mit einer exe-, ZIP-Erweiterung oder einem Eintrag enthält, der auf eine URL verweist, die nicht vorhanden sein soll, ist die Regel wahrscheinlich bösartig.

MailboxFormsExport-*yyyy-mm-dd*. csv – im Allgemeinen ist die Verwendung von benutzerdefinierten Formularen sehr selten.  Wenn Sie eine in dieser Arbeitsmappe finden, öffnen Sie das Postfach des Benutzers, und überprüfen Sie das Formular selbst.  Wenn Ihre Organisation Sie nicht absichtlich dort abgelegt hat, ist dies wahrscheinlich böswillig.



## <a name="how-to-stop-and-remediate-the-outlook-rules-and-forms-attack"></a>Vorgehensweise beenden und Beheben von Outlook-Regeln und Formular Angriffen
Wenn Sie einen der beiden Angriffs Beweise gefunden haben, ist die Korrektur einfach, löschen Sie einfach die Regel oder das Formular aus dem Postfach. Sie können dies mit dem Outlook-Client oder mithilfe von Remote-PowerShell tun, um Regeln zu entfernen.

### <a name="using-outlook"></a>Verwenden von Outlook
1. Identifizieren Sie alle Geräte, die der Benutzer mit Outlook verwendet hat.  Sie müssen alle von potentiellen Schadsoftware gereinigt werden.  Lassen Sie den Benutzer sich nicht anmelden und e-Mail verwenden, bis alle Geräte bereinigt wurden.
2. Befolgen Sie die Schritte unter [Löschen einer Regel](https://support.office.com/article/Delete-a-rule-2F0E7139-F696-4422-8498-44846DB9067F) für jedes Gerät.
3. Wenn Sie sich über das vorhanden sein anderer Schadsoftware nicht sicher sind, können Sie die gesamte Software auf dem Gerät formatieren und neu installieren.  Für mobile Geräte können Sie den Herstellern Schritte folgen, um das Gerät auf das Factory-Image zurückzusetzen.
4. Installieren Sie die aktuellsten Versionen von Outlook.  Beachten Sie, dass die aktuelle Version von Outlook beide Typen dieses Angriffs standardmäßig blockiert.
5. Nachdem alle Offlinekopien des Postfachs entfernt wurden, setzen Sie das Kennwort des Benutzers zurück (verwenden Sie eine hochwertige), und führen Sie die Schritte unter [Einrichten der mehrstufigen Authentifizierung für Office 365 Benutzer](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) aus, wenn MFA noch nicht aktiviert wurde. Dadurch wird sichergestellt, dass die Anmeldeinformationen des Benutzers nicht auf andere Weise verfügbar gemacht werden (wie Phishing oder Kenn Wort Wiederverwendung).

### <a name="using-powershell"></a>Verwendung von PowerShell
Es gibt zwei Remote-PowerShell-Cmdlets, mit denen Sie gefährliche Regeln entfernen oder deaktivieren können. Führen Sie einfach die folgenden Schritte aus.
 
Schritte für Postfächer auf einem Exchange-Server

1. Stellen Sie mithilfe von Remote-PowerShell eine Verbindung mit dem Exchange-Server her. Führen Sie die Schritte unter [Verbinden mit Exchange-Servern mithilfe von Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-server/connect-to-exchange-servers-using-remote-powershell?view=exchange-ps)aus.
2. Wenn Sie eine einzelne Regel, mehrere Regeln oder alle Regeln aus einem Postfach vollständig entfernen möchten, verwenden Sie das [Cmdlet Remove-Posteingangsregel ](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps)– verwenden Sie diese Option, um eine, mehrere oder alle Regeln aus dem Postfach vollständig zu entfernen.
3. Wenn Sie die Regel und ihren Inhalt für weitere Untersuchungen beibehalten möchten, verwenden Sie das [Cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

Schritte für Postfächer in Exchange Online
1. Führen Sie die Schritte unter [Verbinden mit Exchange Online mithilfe von PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)aus.
2.  Wenn Sie eine einzelne Regel, mehrere Regeln oder alle Regeln aus einem Postfach vollständig entfernen möchten, verwenden Sie das [Cmdlet Remove-Posteingangsregel](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps).
3.  Wenn Sie die Regel und ihren Inhalt für weitere Untersuchungen beibehalten möchten, verwenden Sie das [Cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

## <a name="how-to-minimize-future-attacks"></a>Vorgehensweise minimieren künftiger Angriffe

### <a name="first-protect-your-accounts"></a>Erstens: Schützen Ihrer Konten

Die Regeln und Formular Ausnutzungen werden nur von einem Angreifer verwendet, nachdem er ein Konto des Benutzers gestohlen oder verletzt hat. Der erste Schritt zur Verhinderung der Verwendung dieser Exploits für Ihre Organisation besteht darin, ihre Benutzerkonten aggressiv zu schützen.  Einige der häufigsten Methoden, bei denen Konten verletzt werden, sind Phishing-oder [Kenn Wort Sprüh](http://www.dabcc.com/microsoft-defending-against-password-spray-attacks/) Angriffe.



Die beste Möglichkeit zum Schutz Ihrer Benutzerkonten und insbesondere ihrer Administratorkonten besteht darin, die [mehrstufige Authentifizierung für Office 365 Benutzer](https://support.office.com/article/set-up-multi-factor-authentication-for-office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)einzurichten.  Sie sollten auch Folgendes tun:
<ol>
    <li>Überwachen Sie, wie auf ihre Benutzerkonten <a href="https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports">zugegriffen und verwendet wird</a>. Sie können die anfängliche Verletzung nicht verhindern, aber Sie werden die Dauer und die Auswirkungen der Verletzung verkürzen, indem Sie Sie früher erkennen. Sie können diese verwenden: <a href="https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security">Office 365 Cloud App Security Policies</a> to Monitor Your Accounts und Alert on Unusual activity. 
        <ol type="a">
            <li><b>Mehrere fehlgeschlagene Anmeldeversuche</b> Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Benutzer mehrere fehlgeschlagene Anmeldeaktivitäten in einer einzigen Sitzung im Hinblick auf die gelernte Baseline ausführen, was auf eine versuchte Verletzung hindeuten könnte.</li>
            <li><b>Unmöglich Reisen</b> - Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Aktivitäten vom gleichen Benutzer an unterschiedlichen Orten innerhalb eines Zeitraums erkannt werden, der kürzer ist als die erwartete Reisezeit zwischen den beiden Standorten. Dies kann darauf hindeuten, dass ein anderer Benutzer die gleichen Anmeldeinformationen verwendet. Wenn Sie dieses anomale Verhalten erkennen, ist eine anfängliche Lernphase von sieben Tagen erforderlich, in der das Aktivitätsmuster eines neuen Benutzers erlernt wird.</li>
            <li><b>Ungewöhnliche imitierte Aktivität (nach Benutzer)</b> - Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn Benutzer mehrere imitierte Aktivitäten in einer einzigen Sitzung im Hinblick auf die erlernten Grundlagen ausführen, was auf eine versuchte Verletzung hindeuten könnte.</li>
        </ol>
    </li>
    <li>Nutzen Sie ein Tool wie das <a href="https://securescore.office.com/">Office 365 Secure Score</a> , um Konto Sicherheitskonfigurationen und-Verhalten zu verwalten. 
    </li>
</ol> 

### <a name="second-keep-your-outlook-clients-current"></a>Zweite: beibehalten der aktuellen Outlook-Clients
Vollständig aktualisierte und gepatchte Versionen von Outlook 2013 und 2016 deaktivieren Sie die Regel/Form-Aktion "Anwendung starten" standardmäßig.  Dadurch wird sichergestellt, dass die Regel-und Formularaktionen blockiert werden, selbst wenn ein Angreifer das Konto verletzt.  Sie können die neuesten Updates und Sicherheitspatches installieren, indem Sie die Schritte unter [Installieren von Office-Updates](https://support.office.com/article/Install-Office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)ausführen.

Hier sind die Patch-Versionen für Ihre Outlook 2013-und 2016-Clients:
- Outlook 2013:15.0.4937.1000 oder höher
- Outlook 2016:16.0.4534.1001 oder höher

Weitere Informationen zu den einzelnen Sicherheitspatches finden Sie unter:

- [Outlook 2013 Sicherheits Patch](https://support.microsoft.com/en-us/help/3191938) 
- [Outlook 2016-Sicherheits Patch](https://support.microsoft.com/en-us/help/3191883)

### <a name="third-monitor-your-outlook-clients"></a>Drittens: Überwachen Ihrer Outlook-Clients
Beachten Sie, dass es auch bei installierten Patches und Updates möglich ist, dass ein Angreifer die Konfiguration des lokalen Computers so ändert, dass das Verhalten "Anwendung starten" erneut aktiviert wird. Sie können die [Erweiterte Gruppenrichtlinienverwaltung](https://docs.microsoft.com/microsoft-desktop-optimization-pack/agpm/) verwenden, um lokale Computerrichtlinien auf Ihren Clients zu überwachen und zu erzwingen.  
Sie können sehen, ob "Anwendung starten" durch eine Außerkraftsetzung in der Registrierung erneut aktiviert wurde, indem Sie die Informationen in [How to View the System Registry by using 64-Bit Windows](https://support.microsoft.com/en-us/help/305097/how-to-view-the-system-registry-by-using-64-bit-versions-of-windows)verwenden.  Überprüfen Sie diese Unterschlüssel: 

- Outlook 2016: HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Security\
- Outlook 2013: HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Security\

Suchen Sie nach dem Schlüssel EnableUnsafeClientMailRules. Wenn er vorhanden und auf 1 festgelegt ist, wurde der Outlook-Sicherheitspatch außer Kraft gesetzt, und der Computer ist anfällig für den Angriff auf Form/Regel. Wenn der Wert 0 ist, wird die Aktion "Anwendung starten" deaktiviert.  Wenn die aktualisierte und gepatchte Version von Outlook installiert ist und dieser Registrierungsschlüssel nicht vorhanden ist, ist ein System nicht anfällig für diese Angriffe.

Kunden mit lokalen Exchange-Installationen sollten in Betracht gezogen, ältere Versionen von Outlook zu blockieren, für die keine Patches verfügbar sind. Details zu diesem Prozess finden Sie im Artikel [configure Outlook Client Blocking](https://technet.microsoft.com/en-us/library/dd335207(v=exchg.150).aspx).

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sichern von Office 365 wie ein Profi für Internetsicherheit
Ihr Office 365-Abonnement bietet eine Reihe von leistungsfähigen Funktionen für Sicherheit, die Sie zum Schutz Ihrer Daten und Ihrer Benutzer verwenden können.  Verwenden Sie die [Office 365-Sicherheits-Roadmap: Top-Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) zum Implementieren von empfohlenen Microsoft-Best-Practices für den Schutz Ihres Office 365-Mandanten.
- Aufgaben, die in den ersten 30 Tagen ausgeführt werden sollten.  Diese sind unmittelbar gültig und haben nur geringe Auswirkungen für die Benutzer.
- Aufgaben, die innerhalb von 90 Tagen ausgeführt werden sollten. Diese erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich.
- Über 90 Tage hinaus. Diese Verbesserungen werden in den ersten 90 Tagen Ihrer Arbeit umgesetzt.

## <a name="see-also"></a>Siehe auch:
- [Böswillige Outlook-Regeln](https://silentbreaksecurity.com/malicious-outlook-rules/) durch SilentBreak Security Post about Rules Vector enthält eine ausführliche Übersicht über die Art und Weise, wie die Outlook-Regeln. 
- [MAPI über HTTP und mailrule Pwnage](https://sensepost.com/blog/2016/mapi-over-http-and-mailrule-pwnage/) im Sensepost-Blog über mailrule Pwnage beschreibt ein Tool mit dem Namen Ruler, mit dem Sie Postfächerüber Outlook-Regeln ausnutzen können.
- [Outlook-Formulare und-Shells](https://sensepost.com/blog/2017/outlook-forms-and-shells/) im Sensepost-Blog über Forms Threat Vector. 
- [Lineal-CodeBase](https://github.com/sensepost/ruler)
- [Lineal-Indikatoren für Kompromisse](https://github.com/sensepost/notruler/blob/master/iocs.md)
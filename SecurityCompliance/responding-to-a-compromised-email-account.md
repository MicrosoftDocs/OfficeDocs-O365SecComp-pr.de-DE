---
title: Reagieren auf ein angegriffenes E-Mail-Konto in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.custom: TopSMBIssues
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Informationen zum erkennen und beantworten eines kompromittierten e-Mail-Kontos in Office 365
ms.openlocfilehash: 5598b424c8175fd8cbb173d4b7b96839f64472dd
ms.sourcegitcommit: f6073deec39a18581ed12abef18728417a52cdf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2019
ms.locfileid: "30747551"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Reagieren auf ein angegriffenes E-Mail-Konto in Office 365

**Zusammenfassung** Erfahren Sie, wie Sie ein kompromittiertes e-Mail-Konto in Office 365 erkennen und darauf reagieren.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Was ist ein kompromittiertes e-Mail-Konto in Office 365?
Der Zugriff auf Office 365-Postfächer, Daten und andere Dienste wird über die Verwendung von Anmeldeinformationen gesteuert, beispielsweise einen Benutzernamen und ein Kennwort oder eine PIN. Wenn eine andere Person als der vorgesehene Benutzer diese Anmeldeinformationen stiehlt, gelten die gestohlenen Anmeldeinformationen als kompromittiert. Bei diesen kann sich der Angreifer als ursprünglicher Benutzer anmelden und illegale Aktionen ausführen.
Unter Verwendung der gestohlenen Anmeldeinformationen kann der Angreifer auf das Office 365-Postfach des Benutzers, auf SharePoint-Ordner oder auf Dateien in der OneDrive des Benutzers zugreifen. Eine häufig verwendete Aktion ist, dass der Angreifer e-Mails als ursprünglichen Benutzer an Empfänger sowohl innerhalb als auch außerhalb der Organisation sendet. Wenn der Angreifer Daten an externe Empfänger sendet, wird dies als Datenfilterung bezeichnet.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Symptome eines kompromittierten Office 365-e-Mail-Kontos
Benutzer können ungewöhnliche Aktivitäten in Ihren Office 365-Postfächern bemerken und melden. Es folgen einige häufige Symptome:
- Verdächtige Aktivitäten wie fehlende oder gelöschte e-Mails.
- Andere Benutzer erhalten möglicherweise e-Mails vom kompromittierten Konto, ohne dass die entsprechende e-Mail im Ordner " **Gesendete Elemente** " des Absenders vorhanden ist.
- Das vorhanden sein von Posteingangsregeln, die nicht vom beabsichtigten Benutzer oder vom Administrator erstellt wurden. Diese Regeln können e-Mails automatisch an unbekannte Adressen weiterleiten oder in die Ordner **Notizen**, **Junk-e-Mail**oder **RSS-Abonnements** verschieben.
- Der Anzeigename des Benutzers kann in der globalen Adressliste geändert werden.
- Das Senden von e-Mails ist für das Postfach des Benutzers blockiert.
- Die Ordner "gesendete oder gelöschte Elemente" in Microsoft Outlook oder Outlook im Web (früher als Outlook Web App bezeichnet) enthalten allgemeine Nachrichten mit gehackten Konten, beispielsweise "Ich bin in London fest, sende Geld".
- Ungewöhnliche Profiländerungen wie der Name, die Telefonnummer oder die Postleitzahl wurden aktualisiert.
- Ungewöhnliche Anmeldeinformationen, wie etwa mehrere Kennwortänderungen, sind erforderlich.
- Die e-Mail-Weiterleitung wurde kürzlich hinzugefügt.
- Eine ungewöhnliche Signatur wurde kürzlich hinzugefügt, beispielsweise eine gefälschte Bank Signatur oder eine verschreibungspflichtige Medikamenten Signatur.

Wenn ein Benutzer eines der oben genannten Symptome meldet, sollten Sie weitere Untersuchungen durchführen. Das Office 365 Security & Compliance Center und das Azure-Portal bieten Tools, die Ihnen dabei helfen, die Aktivität eines Benutzerkontos zu untersuchen, das Sie möglicherweise gefährden.
- Office 365 Unified Audit Logs im Security & Compliance Center-überprüfen Sie alle Aktivitäten für das mutmaßliche Konto, indem Sie die Ergebnisse für den Datumsbereich von unmittelbar vor der verdächtigen Aktivität auf das aktuelle Datum filtern. Filtern Sie nicht nach den Aktivitäten während der Suche.
- Verwenden Sie die Azure AD-Anmelde Protokolle und andere Risikoberichte, die im Azure AD-Portal verfügbar sind. ÜberPrüfen Sie die Werte in den folgenden Spalten:
    - Überprüfende IP-Adresse
    - Anmelde Standorte
    - Anmeldezeiten
    - Erfolg oder Fehler bei der Anmeldung

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Sichern und Wiederherstellen der e-Mail-Funktion in einem mutmaßlich kompromittierten Office 365-Konto und-Postfach

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Auch nachdem Sie den Zugriff auf Ihr Konto wiedererlangt haben, hat der Angreifer möglicherweise Back-Door-Einträge hinzugefügt, die es dem Angreifer ermöglichen, die Kontrolle über das Konto wieder aufzunehmen.

Sie müssen alle folgenden Schritte ausführen, um den Zugriff auf Ihr Konto wiederherzustellen, je früher desto besser, um sicherzustellen, dass der Hijacker das Konto nicht mehr steuert. Mit diesen Schritten können Sie alle Back-Door-Einträge entfernen, die der Hijacker Ihrem Konto hinzugefügt hat. Nachdem Sie diese Schritte ausgeführt haben, sollten Sie eine Virenprüfung ausführen, um sicherzustellen, dass Ihr Computer nicht kompromittiert wird.

### <a name="step-1-reset-the-users-password"></a>Schritt 1 Zurücksetzen des Kennworts des Benutzers
> [!WARNING]
> Senden Sie das neue Kennwort nicht per e-Mail an den beabsichtigten Benutzer, da der Angreifer weiterhin Zugriff auf das Postfach hat.

1. Folgen Sie dem Zurücksetzen eines Office 365 Business-Kennworts für eine andere Prozedur in [Administratoren: Zurücksetzen von office 365 Business](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c) passwords

**Hinweise:**
- Stellen Sie sicher, dass das Kennwort stark ist und dass es groß-und Kleinbuchstaben, mindestens eine Zahl und mindestens ein Sonderzeichen enthält. 
- Verwenden Sie keines der letzten fünf Kennwörter. Auch wenn Sie mit der Kennwortverlaufs Anforderung ein jüngeres Kennwort wieder verwenden können, sollten Sie etwas auswählen, das der Angreifer nicht erraten kann.
- Wenn Ihre lokale Identität mit Office 365 verbunden ist, müssen Sie Ihr Kennwort lokal ändern und dann Ihren Administrator über die Gefährdung informieren.

> [!TIP]
> Es wird dringend empfohlen, die mehrstufige Authentifizierung (Multi-Factor Authentication, MFA) zu aktivieren, um eine Gefährdung zu vermeiden, insbesondere für Konten mit Administratorrechten.  Weitere Informationen finden Sie [hier](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Schritt 2 entfernen verdächtiger e-Mail-Weiterleitungsadressen
1. Öffnen Sie das **Office 365 Admin Center _GT_ Active Users**.
2. Suchen Sie nach dem fraglichen Benutzerkonto, und erweitern Sie **e-Mail-Einstellungen**.
3. Klicken Sie für die **e-Mail-Weiterleitung**auf **Bearbeiten**.
4. Entfernen Sie alle verdächtigen Weiterleitungsadressen.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Schritt 3 Deaktivieren aller Verdächtigen Posteingangsregeln
1. Melden Sie sich mit Outlook im Web beim Benutzerpostfach an.
2. Klicken Sie auf das Zahnradsymbol und dann auf **e-Mail**.
3. Klicken Sie auf postEingangs **-und Sweep-Regeln** , und lesen Sie die Regeln.
4. Deaktivieren oder löschen Sie verdächtige Regeln.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Schritt 4 Entsperren des Benutzers zum Senden von e-Mails
Wenn das mutmaßlich kompromittierte Postfach zum Senden von Spam-e-Mails illegal verwendet wurde, ist es wahrscheinlich, dass das Postfach nicht mehr gesendet werden kann.
1. Führen Sie die Verfahren unter [Entfernen eines Benutzers, einer Domäne oder einer IP-Adresse aus einer Sperrliste nach dem Senden von Spam-e-](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )Mails aus, um die Blockierung eines Postfachs vom Senden von e-Mails aufzuheben.

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Schritt 5 optional: Blockieren des Benutzerkontos bei der Anmeldung
> [!IMPORTANT]
> Sie können das mutmaßlich kompromittierte Konto vor der Anmeldung blockieren, bis Sie der Meinung sind, dass der Zugriff erneut aktiviert werden kann.

1. Wechseln Sie zum Office 365 Admin Center.
2. Wählen Sie im Office 365 Admin Center die Option **Benutzer** aus.
3. Wählen Sie den Mitarbeiter aus, den Sie blockieren möchten, und wählen Sie dann **Bearbeiten** neben **Anmeldestatus** im Benutzerbereich
4. Wählen Sie im Bereich **Anmeldestatus** die Option **Anmeldung blockiert** und dann **Speichern** aus. 
5. Erweitern Sie im Office 365 Admin Center im unteren linken Navigationsbereich **Admin Center** , und wählen Sie **Exchange**aus.
6. Navigieren Sie im Exchange Admin Center zu **Empfänger _GT_ Postfächer**.
7. Wählen Sie den Benutzer aus, und klicken Sie auf der Seite Benutzereigenschaften unter **Mobile Geräte**auf **Exchange-ActivcSync deaktivieren** , und deaktivieren Sie **** **OWA für Geräte** , und beantworten Sie beide.
8. **Deaktivieren** Sie unter **e-Mail-Konnektivität**die Option **Ja**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Schritt 6 optional: Entfernen des mutmaßlichen kompromittierten Kontos aus allen administrativen Rollengruppen
> [!NOTE]
> Die Mitgliedschaft in einer Administratorrollengruppe kann wiederhergestellt werden, nachdem das Konto gesichert wurde.

1. Melden Sie sich beim Office 365 Admin Center mit einem globalen Administratorkonto an, und öffnen Sie **aktive Benutzer**.
2. Suchen Sie nach dem mutmaßlich kompromittierten Konto, und überprüfen Sie, ob dem Konto Administratorrollen zugewiesen sind.
3. Öffnen Sie das **Security _AMP_ Compliance Center**.
4. Klicken Sie auf **Berechtigungen**.
5. Überprüfen Sie die Rollengruppen manuell, um festzustellen, ob das mutmaßlich kompromittierte Konto Mitglied einer dieser Benutzer ist.  Wenn dies der Fall ist: a. Klicken Sie auf die Rollengruppe, und klicken Sie auf **Rollengruppe bearbeiten**.
    b. Klicken Sie auf **Mitglieder auswählen** und **Bearbeiten** , um den Benutzer aus der Rollengruppe zu entfernen.
6. Öffnen des **Exchange Admin Center**
7. Klicken Sie auf **Berechtigungen**.
8. Überprüfen Sie die Rollengruppen manuell, um festzustellen, ob das mutmaßlich kompromittierte Konto Mitglied einer dieser Benutzer ist. Wenn dies der Fall ist: a. Klicken Sie auf die Rollengruppe, und klicken Sie auf **Bearbeiten**.
    b. Verwenden Sie den Abschnitt **Members** , um den Benutzer aus der Rollengruppe zu entfernen.

### <a name="step-7-optional-additional-precautionary-steps"></a>Schritt 7 optional: zusätzliche Vorsichtsmaßnahmen
1. Vergewissern Sie sich, dass Sie die gesendeten Elemente überprüft haben. Möglicherweise müssen Sie die Personen in Ihrer Kontaktliste darüber informieren, dass Ihr Konto kompromittiert wurde. Der Angreifer hat Sie möglicherweise um Geld und Spoofing gebeten, beispielsweise, dass Sie in einem anderen Land gestrandet waren und Geld benötigten, oder der Angreifer kann Ihnen einen Virus senden, um auch Ihre Computer zu entführen.
2. Möglicherweise wurden alle anderen Dienste, die dieses Exchange-Konto als alternatives e-Mail-Konto verwendet haben, kompromittiert. Führen Sie zunächst die folgenden Schritte für Ihr Office 365-Abonnement aus, und führen Sie die folgenden Schritte für Ihre anderen Konten aus.
3. Stellen Sie sicher, dass Ihre Kontaktinformationen, wie Telefonnummern und Adressen, korrekt sind.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Secure Office 365 wie ein Cyber pro
Ihr Office 365-Abonnement verfügt über eine Reihe leistungsstarker Sicherheitsfunktionen, die Sie zum Schutz Ihrer Daten und ihrer Benutzer verwenden können.  Verwenden Sie die [office 365 Security Roadmap: die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) , um die empfohlenen bewährten Methoden von Microsoft für die Sicherung ihres Office 365-Mandanten zu implementieren.
- Aufgaben, die in den ersten 30 Tagen erledigt werden müssen.  Diese haben sofortige Auswirkungen und sind für Ihre Benutzer gering.
- Aufgaben in 90 Tagen. Diese benötigen etwas mehr Zeit, um ihre Sicherheitslage zu planen und zu implementieren.
- Über 90 Tage. Diese Verbesserungen werden in den ersten 90-Tagen ausgeführt.

## <a name="see-also"></a>Siehe auch:
- [Bewährte Methoden für die Sicherheit in Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Erkennen und Korrigieren von Outlook-Regeln und benutzerdefinierten Formularen für Einschleusungsangriffe in Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Internet Crime Complaint Center](http://www.ic3.gov/preventiontips.aspx)
- [Wertpapier-und Exchange-Kommission-Betrugsbekämpfung](http://www.sec.gov/investor/pubs/phishing.htm)

---
title: Reagieren auf ein angegriffenes E-Mail-Konto in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Erfahren Sie, wie erkennen und reagieren auf eine kompromittierten e-Mail-Konto in Office 365
ms.openlocfilehash: bf3350da88804639356100fb5be2403c76cbcec6
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977590"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Reagieren auf ein angegriffenes E-Mail-Konto in Office 365

**Zusammenfassung** Informationen Sie zum Erkennen und reagieren auf eine kompromittierten e-Mail-Konto in Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Was ist ein gefährdet e-Mail-Konto in Office 365?
Zugriff auf Office 365-Postfächer, Daten und andere Dienste, die durch die Verwendung von Anmeldeinformationen, beispielsweise ein Benutzername und Kennwort oder eine PIN gesteuert wird. Wenn eine andere Person als der gewünschte Benutzer diese Anmeldeinformationen entwendet, gelten die gestohlenen Anmeldeinformationen möglicherweise gefährdet. Mit diesen kann der Angreifer als der ursprünglichen Benutzer anmelden und unerlaubte Aktionen ausführen. Die gestohlenen Anmeldeinformationen verwenden, kann der Angreifer Office 365-Postfach des Benutzers, SharePoint-Ordner oder Dateien in OneDrive des Benutzers zugreifen. Eine Aktion im Allgemeinen ist der Angreifer e-Mails an Empfänger innerhalb und außerhalb der Organisation als des ursprünglichen Benutzers senden. Wenn der Angreifer Daten an externe Empfänger-e-Mails, wird diese Daten Exfiltration aufgerufen.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Symptome eines kompromittierten Office 365-e-Mail-Kontos
Benutzer möglicherweise beachten und ungewöhnliche Aktivität in ihre Office 365-Postfächer. Im folgenden sind einige häufige Symptome:
- Verdächtige Aktivitäten wie fehlende oder gelöschte-e-Mails.
- Andere Benutzer möglicherweise dieses Konto ohne entsprechende im Ordner " **Gesendete Elemente** " des Absenders einer vorhandenen e-Mail-e-Mails erhalten.
- Das Vorhandensein von Posteingangsregeln, die von der gewünschten Benutzer oder der Administrator erstellt wurden nicht. Diese Regeln möglicherweise automatisch Weiterleiten von e-Mails an unbekannte Adressen oder verschieben Sie sie in den Ordner **Notizen**, **Junk-e-Mail-** oder **RSS-Abonnements** .
- Anzeigename des Benutzers kann in der globalen Adressliste geändert werden.
- Das Postfach des Benutzers wird verhindert, dass das Senden von e-Mails.
- Der Ordner gesendet oder gelöschte Objekte in Microsoft Outlook oder Microsoft Outlook Web App enthalten allgemeine gehackt Konto Nachrichten, wie "Ich in London Geld senden hängen bin."
- Ungewöhnliche Profil ändert, beispielsweise den Namen, die Telefonnummer oder die Postleitzahl wurden aktualisiert.
- Ungewöhnliche Anmeldeinformationen geändert wird, wie mehrere kennwortänderungen sind erforderlich.
- E-Mail-Weiterleitung wurde kürzlich hinzugefügt.
- Eine ungewöhnliche Signatur wurde kürzlich hinzugefügt, wie eine Signatur gefälschten Bankgeschäfte oder eine Aufgabenebene Drug Signatur.

Wenn ein Benutzer die oben genannten Symptome meldet, sollten Sie weiteren Untersuchung durchführen. Die Office 365-Sicherheit und Compliance Center und der Azure-Verwaltungsportal bieten Tools, mit denen Sie die Aktivität eines Benutzerkontos untersuchen, die vermutlich möglicherweise gefährdet ist.
- Office 365 Unified Überwachungsprotokolle im Compliance Center- & Sicherheit überprüfen alle Aktivitäten für das Konto verdächtige Nachrichten durch Filtern der Ergebnisse für das Datum Bereich übergreifende aus unmittelbar vor dem verdächtige Aktivitäten auf das aktuelle Datum ist aufgetreten. Nicht filtern Sie auf die Aktivitäten bei der Suche.
- Verwenden Sie die Protokolle Azure AD-Anmeldung und andere Risikoberichte, die im Azure AD-Portal zur Verfügung stehen. Überprüfen Sie die Werte in den folgenden Spalten:
    - Überprüfen Sie die IP-Adresse
    - Anmeldung Speicherorte
    - -in Zeiten
    - Anmeldung Erfolg oder Fehler



## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Sichern und Wiederherstellen von e-Mail-Funktion in einen verdächtige Nachrichten wie Office 365-Konto und das Postfach gefährdet

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Auch nach dem Sie Zugriff auf Ihr Konto wiederhergestellt haben, hat der Angreifer möglicherweise Back-Tür Einträge hinzugefügt, mit die der Angreifer Steuerelement des Kontos fortsetzen zu können.

Sie müssen alle folgenden Schritte aus, um Zugriff auf Ihr Konto wieder zu übernehmen, stellen Sie sicher, dass die Hijacker fortsetzen nicht besser steuern die früher Ihr Konto ausführen. Diese Schritte können Sie die Back-Tür Einträge zu entfernen, die die Hijacker auf Ihr Konto möglicherweise hinzugefügt. Nachdem Sie diese Schritte ausgeführt haben, wird empfohlen, dass Sie einen VirusScan dafür sorgen, dass Ihr Computer beeinträchtigt wird nicht ausgeführt.

### <a name="step-1-reset-the-users-password"></a>Schritt 1 Zurücksetzen eines Benutzerkennworts
> [!WARNING]
> Senden Sie das neue Kennwort nicht an die vorgesehenen Benutzer per e-Mail, wie der Angreifer weiterhin Zugriff auf das Postfach zu diesem Zeitpunkt hat.

1. Führen Sie das Kennwort zurücksetzen einer Office 365 Business nach einer Person anderen Verfahren in [Admins: Office 365 zurücksetzen Business Kennwörter](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Hinweise:**
- Stellen Sie sicher, dass das Kennwort stark ist und dass sie Groß-und Kleinbuchstaben, mindestens eine Zahl und mindestens ein Sonderzeichen enthält. 
- Wiederverwenden Sie nicht keinem der letzten fünf Kennwörter. Obwohl die Anforderung Verlauf einer neueren Kennwort erneut verwenden kann, sollten Sie etwas auswählen, die der Angreifer ermittelt werden kann.
- Wenn Ihre lokalen Identität mit Office 365 im Verbund befindet, müssen Sie Ihre lokalen Kennwort ändern, und klicken Sie dann müssen Sie den Administrator der Gefährdung benachrichtigen.

> [!TIP]
> Es wird dringend empfohlen, Multi-Factor Authentication (mehrstufiger Authentifizierung das), um zu verhindern, dass Kompromiss, insbesondere für Konten mit Administratorrechte zu aktivieren.  Erfahren Sie mehr [hier](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Schritt 2 Remove verdächtigen e-Mail-Weiterleitung-Adressen
1. Öffnen der **Office 365 Admin Center > aktive Benutzer**.
2. Suchen Sie das betreffende Benutzerkonto aus, und erweitern Sie **E-Mail-Einstellungen**.
3. **Weiterleiten von E-Mail**klicken Sie auf **Bearbeiten**.
4. Alle verdächtigen Weiterleitungsadressen zu entfernen.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Schritt 3 deaktivieren alle verdächtigen Posteingangsregeln
1. Melden Sie sich das Postfach des Benutzers mit Outlook Web App (OWA).
2. Klicken Sie auf das Zahnradsymbol, und klicken Sie auf **Mail**.
3. Klicken Sie auf **Posteingang und Sweep Regeln** , und überprüfen Sie die Regeln.
4. Deaktivieren oder Löschen von verdächtigen Regeln.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Schritt 4 zulassen der Benutzer am Senden von e-Mail
Wenn das verdächtige Nachrichten kompromittierte Postfach zum Senden von Spam-e-Mail-unrechtmäßig verwendet wurde, ist es wahrscheinlich, dass das Postfach senden von Nachrichten blockiert wurde.
1. Zum Aufheben der Blockierung eines Postfachs Senden von Nachrichten, gehen Sie wie unter [Entfernen eines Benutzers, Domäne oder IP-Adresse von einer Sperrliste nach dem Spam-e-Mail zu senden](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Schritt 5-Optional: Blockieren Sie das Benutzerkonto anmelden bei
> [!IMPORTANT]
> Sie können dieses verdächtige Nachrichten Konto aus Anmeldung, bis Sie Ihrer Meinung nach Access wieder aktivieren sicher ist blockieren.

1. Navigieren Sie zum Office 365 Admin Center.
2. Wählen Sie im Office 365 Administrationscenter **Benutzer**.
3. Wählen Sie den Mitarbeiter, den Sie sperren möchten, und wählen Sie dann im Bereich Benutzer neben **Anmeldestatus** **Bearbeiten**
4. Wählen Sie im Bereich **Anmeldestatus** **- Anmeldung blockiert** , und klicken Sie dann auf **Speichern**. 
5. Erweitern Sie in der Office 365-Verwaltungskonsole in der unteren linken Navigationsbereich **Admin Center** - **Exchange**.
6. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger > Postfächer**.
7. Wählen Sie den Benutzer und auf der Seite Benutzer Eigenschaften unter **Mobile Geräte**, klicken Sie auf **Exchange-ActivcSync deaktivieren** und **OWA for Devices deaktivieren** , und beide **Ja** beantworten.
8. Klicken Sie unter **E-Mail-Konnektivität**, **Deaktivieren** und Antwort **Ja**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Schritt 6 Optional: Entfernen Sie dieses Konto verdächtige Nachrichten aus allen Gruppen der Administratorrolle
> [!NOTE]
> Administratorrolle Gruppenmitgliedschaft kann wiederhergestellt werden, nachdem das Konto gesichert wurde.

1. Melden Sie sich bei Office 365 Admin Center mit einem globalen Administratorkonto an, und öffnen Sie **Aktive Benutzer**.
2. Hier finden Sie die verdächtige gefährdet Konto und manuell überprüfen, um festzustellen, ob alle Administratorrollen für das Konto zugewiesen sind.
3. Öffnen Sie die **Sicherheit und Compliance Center**.
4. Klicken Sie auf **Berechtigungen**.
5. Die Rollengruppen, um herauszufinden, wenn die verdächtige gefährdet Konto ein Mitglied eines davon ist manuell zu überprüfen.  Wenn es ist: a klicken Sie auf die Rollengruppe, und klicken Sie auf **Rollengruppe bearbeiten**.  b. Klicken Sie auf **Ausgewählte Mitglieder** und **Bearbeiten** , um den Benutzer aus der Rollengruppe zu entfernen.
6. Öffnen Sie die **Exchange-Verwaltungskonsole**
7. Klicken Sie auf **Berechtigungen**.
8. Die Rollengruppen, um herauszufinden, wenn die verdächtige gefährdet Konto ein Mitglied eines davon ist manuell zu überprüfen. Wenn es ist: a, klicken Sie auf die Rollengruppe, und klicken Sie auf **Bearbeiten**.  b. verwenden Sie Abschnitt **Mitglieder** , um den Benutzer aus der Rollengruppe zu entfernen.

### <a name="step-7-optional-additional-precautionary-steps"></a>Optional Schritt 7: Zusätzliche Vorsichtsmaßnahmen
1. Stellen Sie sicher, dass Sie gesendete Objekte überprüfen. Möglicherweise müssen Sie die Personen in Ihrer Kontaktliste zu informieren, dass Ihr Konto gefährdet wurde. Der Angreifer kann sie nach der Money, gefragt haben spoofing, beispielsweise, dass in einem anderen Land isolierte wurden und benötigt der Money oder der Angreifer möglicherweise Sie ihnen einen Virus senden auf ihren Computern auch unerlaubterweise.
2. Keine anderen Dienste, die diese Exchange-Konto verwendet, wie das alternative e-Mail-Konto möglicherweise beschädigt wurde. Zuerst, führen Sie diese Schritte für Ihr Office 365-Abonnement, und führen Sie diese Schritte für die anderen Konten.
3. Stellen Sie sicher, dass Ihre Kontaktinformationen wie Telefonnummern und Adressen, korrekt ist.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sichern von Office 365 wie eine pro Sicherheit im Internet
Ihr Office 365-Abonnement verfügt über eine leistungsstarke Reihe von Sicherheitsfunktionen, die Sie verwenden können, um Ihre Daten und Ihre Benutzer zu schützen.  Verwendung der [Wegweiser für Office 365-Sicherheit: Top-Prioritäten für den ersten 30 Tagen 90 Tage und darüber hinaus](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) zur Implementierung von Microsoft empfohlene bewährte Methoden zum Sichern Ihrer Office 365-Mandanten.
- Aufgaben in den ersten 30 Tagen ausgeführt.  Diesen sofort einen Einfluss darauf haben und klein sind für die Benutzer.
- Aufgaben in 90 Tage ausgeführt. Diese erfordern etwas mehr Zeit zum Planen und implementieren, aber Ihre Sicherheitsstatus erheblich verbessert.
- Mehr als 90 Tage. Erstellen Sie diese Verbesserungen in Ihrer ersten 90 Tage Arbeit.

## <a name="see-also"></a>Siehe auch:
- [Bewährte Methoden für die Sicherheit in Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Erkennen und Korrigieren von Outlook-Regeln und benutzerdefinierten Formularen für Einschleusungsangriffe in Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Internet Crime kompatibles Center](http://www.ic3.gov/preventiontips.aspx)
- [Sicherheit und Exchange Provision - Betrug "Phishing"](http://www.sec.gov/investor/pubs/phishing.htm)

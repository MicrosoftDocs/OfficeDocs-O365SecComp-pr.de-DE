---
title: Schutz vor Bedrohungen in Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Verwenden Sie diesen Artikel als Leitfaden für die Konfiguration Ihrer Threat Protection-Features.
ms.openlocfilehash: 646ec220bf4649472d4ab885824010bc32ea862c
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402983"
---
# <a name="protect-against-threats-in-office-365"></a>Schutz vor Bedrohungen in Office 365

Office 365 umfasst eine Vielzahl von Funktionen zum Schutz vor Bedrohungen. Hier finden Sie eine Schnellstartanleitung, die Sie als Prüfliste verwenden können, um sicherzustellen, dass Ihre Bedrohungsschutz Funktionen für Ihre Organisation eingerichtet sind. Wenn Sie neue Features für den Schutz vor Bedrohungen in Office 365 haben oder Sie nur nicht sicher sind, wo Sie anfangen sollen, verwenden Sie die folgenden Anweisungen als Ausgangspunkt. 

> [!IMPORTANT]
> Die **anfänglichen empfohlenen Einstellungen sind für jede Art von Richtlinie enthalten; es stehen jedoch viele Optionen zur Verfügung, und Sie können Ihre Einstellungen entsprechend den Anforderungen Ihrer Organisation anpassen**. Lassen Sie ungefähr 30 Minuten zu, bis Ihre Richtlinien oder Änderungen sich im Rechenzentrum durchsetzen.

## <a name="requirements"></a>Anforderungen

### <a name="subscriptions"></a>Abonnements

Threat Protection-Funktionen sind in allen Office 365-Abonnements enthalten; Einige Abonnements bieten jedoch erweiterte Funktionen. In der folgenden Tabelle sind die in diesem Artikel enthaltenen Schutzfunktionen zusammen mit den Mindestanforderungen für das Abonnement aufgeführt.<br/>

|Schutztyp  |Abonnementanforderung  |
|---------|---------|
|Schutz vor Schadsoftware    | [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EoP        |
|Schutz vor schädlichen URLs und Dateien in e-Mails und Office-Dokumenten    | [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)        |
|Antiphishingschutz    | [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)      |
|Erweiterter Schutz vor Phishing    | [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)   |
|Antispamschutz     | [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)       |
|Automatische Bereinigung ohne Uhrzeit (für e-Mail)    | [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EoP        |
|Überwachungsprotokollierung (wird zur Berichterstellung verwendet)    | [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)        |

### <a name="roles-and-permissions"></a>Rollen und Berechtigungen

Sie müssen eine entsprechende Rolle zugewiesen sein, um Richtlinien im [Security _AMP_ Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)zu konfigurieren. Die folgende Tabelle enthält einige Beispiele: 

|Rolle oder Rollengruppe  |Weitere Informationen  |
|---------|---------|
|Office 365 globaler Administrator |[Informationen zu Administratorrollen von Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Sicherheitsadministrator |[Berechtigungen für Administrator Rollen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Exchange Online-Organisationsverwaltung |[Berechtigungen in Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>und<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

## <a name="part-1---anti-malware-protection"></a>Abschnitt 1: Schutz vor Schadsoftware

Der [Schutz](anti-malware-protection.md) vor Schadsoftware ist in Abonnements mit [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EoP) verfügbar. 

1. Wählen Sie im [Security & Compliance Center](https://protection.office.com) **Threat Management** > **Policy** > **Anti-Schadsoftware**aus.

2. Doppelklicken Sie auf die **Standard** Richtlinie, und wählen Sie dann **Einstellungen**aus.

3. Geben Sie die folgenden Einstellungen an:
    
    - Behalten Sie im Abschnitt **Malware Erkennungs Antwort** die Standardeinstellung **Nein**bei.
   
    - Wählen Sie im Abschnitt **Filter für allgemeine Anlagentypen** die Option **ein**aus.

4. Klicken Sie auf **Speichern**.

Weitere Informationen zu Optionen für Antischadsoftware finden Sie unter [configure Anti-Malware Policies](configure-anti-malware-policies.md).

## <a name="part-2---protection-from-malicious-urls-and-files"></a>Part 2: Schutz vor schädlichen URLs und Dateien

Der Schutz vor schädlichen URLs und Dateien in Abonnements mit [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP) ist verfügbar und wird über die Richtlinien für [sichere ATP-Anlagen](atp-safe-attachments.md) und ATP- [Verknüpfungen](atp-safe-links.md) eingerichtet.

### <a name="atp-safe-attachments-policies"></a>Richtlinien für ATP-sichere Anlagen

Zum Einrichten von [ATP Safe Attachments](atp-safe-attachments.md)müssen Sie mindestens eine ATP-Richtlinie für sichere Anlagen definieren. 

1. Wählen Sie im [Security & Compliance Center](https://protection.office.com)" **Threat Management** > **Policy** > **ATP Safe Attachments**" aus.

2. Aktivieren Sie die Option **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**.

3. Klicken Sie im Abschnitt **e-Mail-Anlagen schützen** auf das**+** Pluszeichen ().

4. Geben Sie die folgenden Einstellungen an:

    - Geben `Block malware`Sie in das Feld **Name** ein.

    - Wählen Sie im Abschnitt Antwort die Option **Block**aus.

    - Wählen Sie im Abschnitt **Anlage umleiten** die Option **Umleitung aktivieren**aus, und geben Sie dann die e-Mail-Adresse des Sicherheitsadministrators oder-Operators Ihrer Organisation an, der erkannte Dateien überprüft.

    - Wählen Sie im Abschnitt **angewendet auf** **die Empfängerdomäne ist**aus. Wählen Sie dann Ihre Domäne aus, wählen Sie **Hinzufügen**aus, und klicken Sie dann auf **OK**.

5. Klicken Sie auf **Speichern**.

6. (**Empfohlener zusätzlicher Schritt**) Führen Sie als globaler Administrator oder SharePoint Online-Administrator das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** aus, wobei der Parameter **DisallowInfectedFileDownload** für Ihre Office 365-Umgebung auf *true* festgelegt ist. (Dadurch wird verhindert, dass Benutzer Dateien, die als bösartig erkannt werden, öffnen, bewegen, kopieren oder freigeben.)  

Weitere Informationen finden Sie unter [Einrichten von office 365 ATP Safe Attachments Policies](set-up-atp-safe-attachments-policies.md) und [aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).

### <a name="atp-safe-links-policies"></a>Richtlinien für ATP-sichere Links

Um ATP- [sichere Links](atp-safe-links.md)einzurichten, überarbeiten Sie Ihre Standardrichtlinie und fügen Sie eine Richtlinie für bestimmte Benutzer hinzu.

1. Klicken Sie im [Security & Compliance Center](https://protection.office.com)auf **Threat Management** > **Policy** > **ATP Safe Links**.

2. Doppelklicken Sie auf die **Standard** Richtlinie.

3. Wählen Sie im Abschnitt **sichere Links verwenden in** die option **Office 365 ProPlus, Office für IOS und Android**aus, und klicken Sie dann auf **Speichern**.

4. Klicken Sie im Abschnitt **Richtlinien für bestimmte Empfänger** auf das Pluszeichen (**+**).

5. Geben Sie die folgenden Einstellungen an:

    - Geben Sie in das Feld **Name** einen Namen ein `Safe Links`.

    - Klicken Sie im Abschnitt **Aktion auswählen** **auf ein**.

    - Wählen Sie die folgenden Optionen aus:

        - **Verwenden sicherer Anlagen zum Überprüfen von herunterladbaren Inhalten** 

        - **Anwenden sicherer Links auf innerhalb der Organisation gesendete e-Mail-Nachrichten**

        - **Nicht zulassen, dass Benutzer auf sichere Links mit ursprünglicher URL klicken**

    - Wählen Sie im Abschnitt **angewendet auf** **die Empfängerdomäne ist**aus. Wählen Sie dann Ihre Domäne aus, wählen Sie **Hinzufügen**aus, und klicken Sie dann auf **OK**.

6. Klicken Sie auf **Speichern**.

Weitere Informationen finden Sie unter [Einrichten von Office 365 ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md). 

## <a name="part-3---anti-phishing-protection"></a>Abschnitt 3: Schutz vor Phishing

Der [Schutz vor Phishing](anti-phishing-protection.md) ist in Abonnements mit [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)verfügbar. Advanced Anti-Phishing Protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Im folgenden Verfahren wird beschrieben, wie Sie eine ATP-Richtlinie zum Schutz vor Phishing konfigurieren. Die Schritte sind für die Konfiguration einer Richtlinie zum Schutz vor Phishing (ohne ATP) ähnlich.

1. Wählen Sie im [Security & Compliance Center](https://protection.office.com)die Option **Threat Management** > **Policy** > **ATP Anti-Phishing**aus.

2. Klicken Sie auf **Standardrichtlinie**.

3. Klicken Sie im Abschnitt **Identitätswechsel** auf **Bearbeiten**, und geben Sie dann die folgenden Einstellungen an:

    -  Aktivieren Sie auf der Registerkarte **zu schützende Benutzer hinzufügen** den Schutz. Fügen Sie dann Benutzer wie die Vorstandsmitglieder Ihrer Organisation, ihren CEO, CFO und andere Führungskräfte hinzu. (Sie können eine einzelne e-Mail-Adresse eingeben oder auf klicken, um eine Liste anzuzeigen.)

    - Aktivieren Sie auf der Registerkarte **zu schützende Domänen hinzufügen** **die Option automatisch die Domänen**, denen ich angehört. Wenn Sie über benutzerdefinierte Domänen verfügen, fügen Sie diese ebenfalls hinzu.

    - Wählen Sie auf der Registerkarte **Aktionen** die Option **Nachricht in den Junk-e-Mail-Ordner der Empfänger** sowohl für den imitierten Benutzer als auch für die Identität der Domäne aus, und aktivieren Sie Sicherheitstipps.

    - Stellen Sie auf der Registerkarte **Mailbox Intelligence** sicher, dass die Option Mailbox Intelligence aktiviert ist.

    - Klicken Sie auf der Registerkarte **Überprüfen der Einstellungen** auf **Speichern**, nachdem Sie die Einstellungen überprüft haben.

4. Klicken Sie im Abschnitt **Spoof** auf **Bearbeiten**, und geben Sie dann die folgenden Einstellungen an:

    - Stellen Sie auf der Registerkarte Spoofing- **Filtereinstellungen** sicher, dass der Schutz vor Spoofing aktiviert ist.

    - Klicken Sie auf der Registerkarte **Aktionen** auf Nachricht in die Junk-e-Mail-Ordner der Empfänger verschieben.

    - Klicken Sie auf der Registerkarte **Überprüfen der Einstellungen** auf **Speichern**, nachdem Sie die Einstellungen überprüft haben. (Wenn Sie keine Änderungen vorgenommen haben, klicken Sie auf **Abbrechen**.)

5. Beenden Sie die Seite Standardrichtlinieneinstellungen.

Weitere Informationen zu den Optionen für die Anti-Phishing-Richtlinie finden Sie unter [Einrichten von Richtlinien zum Schutz](set-up-anti-phishing-policies.md)vor Phishing.

## <a name="part-4---anti-spam-protection"></a>Abschnitt 4-Antispamschutz

[](anti-spam-protection.md) Antispamschutz ist in Abonnements mit [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)verfügbar.

1. Wählen Sie im [Security & Compliance Center](https://protection.office.com)**Anti-Spam**für **Threat Management** > **Policy** > aus.

2. Aktivieren Sie auf der Registerkarte **benutzerdefinierte** **Einstellungen** .

3. Erweitern Sie **Standard-Spamfilter Richtlinie**, klicken Sie auf **Richtlinie bearbeiten**, und geben Sie dann die folgenden Einstellungen an:

    - Legen Sie im Abschnitt **Spam-und Massenaktionen** den Schwellenwert auf 5 oder 6 fest.

    - Überarbeiten Sie im Abschnitt **Zulassungslisten** die zulässigen Absender und Domänen, und bearbeiten Sie Sie gegebenenfalls.

4. Klicken Sie auf **Speichern**.

Weitere Informationen zu ihren Antispampolitik-Optionen finden Sie unter [configure the Anti-Spam](configure-the-anti-spam-policies.md)Policys.

## <a name="part-5---additional-settings-to-configure"></a>Abschnitt 5 – zusätzliche Konfigurationseinstellungen

Zusätzlich zum Konfigurieren von Schutz vor Schadsoftware, bösartigen URLs und Dateien, Phishing und Spam wird empfohlen, die Einstellungen für die automatische Bereinigung und die Überwachungsprotokollierung für Null Stunden zu konfigurieren.

### <a name="zero-hour-auto-purge-for-email"></a>Automatische Bereinigung von Null Stunden für e-Mails

[Automatische Bereinigung ohne Uhrzeit](zero-hour-auto-purge.md) (ZAP) ist in Abonnements verfügbar, die [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)enthält. Dieser Schutz ist standardmäßig aktiviert. die folgenden Bedingungen müssen jedoch erfüllt sein, damit der Schutz wirksam wird:

- Spam Aktionen sind so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner verschoben** wird. [](anti-spam-protection.md)

- Benutzer haben Ihre Standard [Einstellungen für Junk-e-Mails](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert.

Weitere Informationen finden Sie unter [Zero-Hour-automatische Bereinigung – Schutz vor Spam und Schadsoftware](zero-hour-auto-purge.md).

### <a name="audit-logging-for-reporting-and-investigation"></a>Überwachungsprotokollierung für Berichterstellung und Untersuchung

Die Überwachungsprotokollierung ist in Abonnements verfügbar, die [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)verwenden. Um Daten in Bedrohungsschutz Berichten wie [Sicherheits Dashboard](security-dashboard.md), [e-Mail-Sicherheitsberichte](view-email-security-reports.md)und [Explorer](use-explorer-in-security-and-compliance.md)anzuzeigen, muss die Überwachungsprotokollierung für Ihre Organisation aktiviert sein. Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).

## <a name="post-setup-tasks"></a>Aufgaben nach der Installation

Nachdem Sie Ihre Bedrohungsschutz-Features konfiguriert haben, stellen Sie sicher, dass Sie überwachen, wie diese Funktionen funktionieren, überprüfen und überarbeiten Sie die Richtlinien nach Bedarf, und achten Sie auf neue Features und dienstupdates.

|Nächste Schritte  |Ressourcen für weitere Informationen  |
|---------|---------|
|Sehen Sie sich an, wie Bedrohungen-Schutzfunktionen für Ihre Organisation funktionieren, indem Sie Berichte anzeigen    |[Sicherheits Dashboard](security-dashboard.md)<br/>[E-Mail-Sicherheitsberichte](view-email-security-reports.md)<br/>[Berichte für Office 365 ATP](view-reports-for-atp.md)<br/>[Sicherheitsrisiken-Explorer](use-explorer-in-security-and-compliance.md)    |
|Regelmäßiges Überprüfen und Überarbeiten der Bedrohungsschutz Richtlinien    |[Secure Score](microsoft-secure-score.md)<br/>[Intelligente Berichte und Einblicke](reports-and-insights-in-security-and-compliance.md)<br/>[Office 365 Threat Investigation and Response Features](keep-users-safe-with-office-365-ti.md)          |
|Überwachen von neuen Features und dienstupdates     |[Standard-und zielGerichtete Release-Optionen](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)<br/>[Nachrichtencenter](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide)<br/>[Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)<br/>[Dienstbeschreibungen](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)         |



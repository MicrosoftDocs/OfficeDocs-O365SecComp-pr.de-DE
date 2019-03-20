---
title: 'Schnell Start: Einrichten von Office 365 Advanced Threat Protection'
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Hier finden Sie eine Schnellstartanleitung, die Sie verwenden können, um sicherzustellen, dass Office 365 Advanced Threat Protection (ATP) für Ihre Organisation eingerichtet und konfiguriert ist.
ms.openlocfilehash: 5aecbdb63f30a620812de44907b29dcae838ba36
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693296"
---
# <a name="quick-start-guide-set-up-office-365-advanced-threat-protection"></a>Schnell Start Handbuch: Einrichten von Office 365 Advanced Threat Protection

Hier finden Sie eine Schnellstartanleitung, die Sie als Prüfliste verwenden können, um sicherzustellen, dass Office 365 Advanced Threat Protection (ATP) für Ihre Organisation eingerichtet ist. Wenn Sie noch nicht mit dem Bedrohungsschutz in Office 365 zu tun haben, oder wenn Sie nicht sicher sind, wo Sie anfangen sollen, verwenden Sie die folgenden Anweisungen als Ausgangspunkt. 

> [!IMPORTANT]
> Die **anfänglichen empfohlenen Einstellungen sind für jede Art von Richtlinie enthalten; es stehen jedoch viele Optionen zur Verfügung, und Sie können Ihre Einstellungen entsprechend den Anforderungen Ihrer Organisation anpassen**. Lassen Sie ungefähr 30 Minuten zu, bis Ihre Richtlinien oder Änderungen sich im Rechenzentrum durchsetzen.

## <a name="prerequisites"></a>Voraussetzungen

- Ihre Organisation muss über ein Abonnement verfügen, das [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) umfasst.

- Sie müssen für den Zugriff auf ATP-Features eine entsprechende Rolle zugewiesen sein. Die folgende Tabelle enthält einige Beispiele: 

    |Rolle oder Rollengruppe  |Weitere Informationen  |
    |---------|---------|
    |Office 365 globaler Administrator |[Informationen zu Administratorrollen von Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
    |Sicherheitsadministrator |[Berechtigungen für Administrator Rollen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
    |Exchange Online-Organisationsverwaltung |[Berechtigungen in Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>und<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

    (Siehe [Berechtigungen im Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).)

## <a name="part-1---anti-malware"></a>Abschnitt 1-Antischadsoftware

1. wählen sie im [Office 365 Security & Compliance Center](https://protection.office.com) **Threat management** > **Policy** > **Anti-schadsoftware**aus.
2. Doppelklicken Sie auf die **Standard** Richtlinie, und wählen Sie dann **Einstellungen**aus.
3. Geben Sie die folgenden Einstellungen an:
    - Behalten Sie im Abschnitt **Malware Erkennungs Antwort** die Standardeinstellung **Nein**bei.
    - Wählen Sie im Abschnitt **Filter für allgemeine Anlagentypen** die Option **ein**aus.
4. Klicken Sie auf **Speichern**.

Weitere Informationen zu Optionen für Antischadsoftware finden Sie unter [configure Anti-Malware Policies](configure-anti-malware-policies.md).

## <a name="part-2---zero-day-protection"></a>Abschnitt 2-Zero-Day-Schutz

Zero-Day Protection ist durch Richtlinien wie ATP-sichere Links und sichere Anlagen Richtlinien eingerichtet.

### <a name="atp-safe-attachments-policies"></a>Richtlinien für ATP-sichere Anlagen

1. wählen sie im [Office 365 Security & Compliance Center](https://protection.office.com)" **Threat management** > **Policy** > **ATP safe attachments**" aus.
2. Aktivieren Sie die Option **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**.
3. Klicken Sie im Abschnitt **e-Mail-Anlagen schützen** auf das**+** Pluszeichen ().
4. Geben Sie die folgenden Einstellungen an:
    - Geben `Block malware`Sie in das Feld **Name** ein.
    - Wählen Sie im Abschnitt Antwort die Option **Block**aus.
    - Wählen Sie im Abschnitt **Anlage umleiten** die Option **Umleitung aktivieren**aus, und geben Sie dann die e-Mail-Adresse des Sicherheitsadministrators oder-Operators Ihrer Organisation an, der erkannte Dateien überprüft.
    - Wählen Sie im Abschnitt **angewendet auf** **die Empfängerdomäne ist**aus. Wählen Sie dann Ihre Domäne aus, wählen Sie **Hinzufügen**aus, und klicken Sie dann auf **OK**.
5. Klicken Sie auf **Speichern**.
6. (Empfohlener zusätzlicher Schritt) Führen Sie als globaler Administrator oder SharePoint Online-Administrator das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** aus, wobei der Parameter **DisallowInfectedFileDownload** für Ihre Office 365-Umgebung auf *true* festgelegt ist. (Dadurch wird verhindert, dass Benutzer Dateien, die als bösartig erkannt werden, öffnen, bewegen, kopieren oder freigeben.)  

Weitere Informationen finden Sie unter [Einrichten von office 365 ATP Safe Attachments Policies](set-up-atp-safe-attachments-policies.md) und [aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).

### <a name="atp-safe-links-policies"></a>Richtlinien für ATP-sichere Links

Um ATP-sichere Links einzurichten, überarbeiten Sie Ihre Standardrichtlinie und fügen eine Richtlinie hinzu.

1. wählen sie im [Office 365 Security & Compliance Center](https://protection.office.com)" **Threat management** > **Policy** > **ATP Safe Links**" aus.
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

## <a name="part-3---anti-phishing"></a>Abschnitt 3-AntiPhishing 

1. wählen sie im [Office 365 Security & Compliance Center](https://protection.office.com)die option **Threat management** > **Policy** > **ATP anti-phishing**aus.
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

Weitere Informationen zu den Optionen für die Anti-Phishing-Richtlinie finden Sie unter [Einrichten von Office 365 ATP-Antiphishing-und Anti-Phishing-Richtlinien](set-up-anti-phishing-policies.md).

## <a name="part-4---anti-spam"></a>Abschnitt 4-Antispam

1. wählen sie im [Office 365 Security & Compliance Center](https://protection.office.com)" **Threat management** > **Policy** > **Anti-spam**" aus.
2. Aktivieren Sie auf der Registerkarte **benutzerdefinierte** **Einstellungen** .
3. Erweitern Sie **Standard-Spamfilter Richtlinie**, klicken Sie auf **Richtlinie bearbeiten**, und geben Sie dann die folgenden Einstellungen an:
    - Legen Sie im Abschnitt **Spam-und Massenaktionen** den Schwellenwert auf 5 oder 6 fest.
    - Überarbeiten Sie im Abschnitt **Zulassungslisten** die zulässigen Absender und Domänen, und bearbeiten Sie Sie gegebenenfalls.
4. Klicken Sie auf **Speichern**.

Weitere Informationen zu ihren Antispampolitik-Optionen finden Sie unter [configure the Anti-Spam](configure-the-anti-spam-policies.md)Policys.

## <a name="part-5---service-wide-settings"></a>Abschnitt 5-dienstweite Einstellungen

### <a name="zero-hour-auto-purge"></a>Automatische Bereinigung ohne Uhrzeit

Automatische Bereinigung von Null Stunden (ZAP) ist standardmäßig aktiviert; die folgenden Bedingungen müssen jedoch erfüllt sein:
- Spam Aktionen sind so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner verschoben** wird.
- Benutzer haben ihre Standardeinstellungen für Junk-e-Mails beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert.

Weitere Informationen finden Sie unter [Zero-Hour-automatische Bereinigung – Schutz vor Spam und Schadsoftware](zero-hour-auto-purge.md).

### <a name="audit-logging"></a>Überwachungsprotokollierung

Zum Anzeigen von Daten in Bedrohungsschutz Berichten wie [Sicherheits Dashboard](security-dashboard.md) und [Explorer](use-explorer-in-security-and-compliance.md)muss die Überwachungsprotokollierung für Ihre Organisation aktiviert sein.

Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).

## <a name="post-setup-tasks"></a>Aufgaben nach der Installation

### <a name="watch-for-new-features-and-service-updates"></a>Überwachen von neuen Features und dienstupdates

- [Besuchen Sie die Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [Siehe Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a>Sehen Sie, wie ATP für Ihre Organisation funktioniert.

- [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)

- [Verwenden des Explorers im Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a>Regelmäßiges Überprüfen und Überarbeiten ihrer ATP-Richtlinien

- [Sicherstellen der Sicherheit Ihrer Office 365-Benutzer mit der Bedrohungsanalyse und-Antwort von Office 365](keep-users-safe-with-office-365-ti.md) 

- [Verwenden der intelligenten Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md) 
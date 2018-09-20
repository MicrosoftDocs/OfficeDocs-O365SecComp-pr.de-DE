---
title: Konfigurieren von Systemzugriff Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Verwenden Sie in diesem Thema, um weitere Informationen zum Konfigurieren der Systemzugriff Management in Office 365
ms.openlocfilehash: 6494505554a02f005df8f45839c9575094acbf1a
ms.sourcegitcommit: d31904e81f81d0fba75309a2bc8bbfb05565a0b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2018
ms.locfileid: "24055250"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>Konfigurieren von Systemzugriff Management in Office 365

> [!IMPORTANT]
> In diesem Thema werden die Hinweise zur Bereitstellung und Konfiguration für derzeit nur in Office 365 E5 und erweiterte Compliance-SKUs verfügbaren Features behandelt.

In diesem Thema führt Sie durch Aktivieren und Konfigurieren von Systemzugriff Management in Office 365-Organisation. Sie können entweder die mit Berechtigungen Zugriff, die Microsoft 365 Admin Center oder Exchange Management PowerShell zum Verwalten und verwenden. 

## <a name="enable-and-configure-privileged-access-management"></a>Aktivieren und Konfigurieren der Verwaltung von Systemzugriff

Führen Sie diese Schritte zum Einrichten und Verwenden von Systemzugriff in Office 365-Organisation aus:

- [Schritt 1: Erstellen einer genehmigenden Person Gruppe](privileged-access-management-configuration.md#step1)

    Bevor Sie mit Berechtigung Access beginnen, bestimmen Sie die Genehmigungsberechtigung für eingehende Anforderungen für den Zugriff auf Aufgaben mit erhöhten Rechten und Berechtigungen besitzen. Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist werden Genehmigen von zugriffsanforderungen. Dies ist aktiviert, indem Sie eine e-Mail-aktivierte Sicherheitsgruppe in Office 365 erstellen.

- [Schritt 2: Aktivieren von Systemzugriff](privileged-access-management-configuration.md#step2)

    Systemzugriff muss explizit aktiviert werden in Office 365 mit der Standardgruppe genehmigende Person und einschließlich einer Reihe von Systemkonten, die Sie aus der Systemzugriff Management Zugriffssteuerung ausgeschlossen werden möchten.

- [Schritt 3: Erstellen einer Richtlinie für den Zugriff](privileged-access-management-configuration.md#step3)

    Erstellen einer Richtlinie für die Genehmigung können Sie die Genehmigung von bestimmten Anforderungen an einzelne Aufgaben bezogenen definieren. Die Typ von Genehmigungsoptionen werden **automatisch** oder **manuell**.

- [Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /](privileged-access-management-configuration.md#step4)

    Aktiviert, privilegierten Zugriff erfordert Genehmigungen für das Ausführen aller Aufgaben, die eine Genehmigung zugeordnete Richtlinie definiert wurde. Benutzer müssen zum Ausführen von Aufgaben, die eine Genehmigung Richtlinie müssen anfordern und zugriffsgenehmigung, um die erforderlichen Berechtigungen zum Ausführen der Aufgabe lassen erteilt werden.

Nachdem die Zustimmung eingeholt wurde, der anfordernde Benutzer kann den beabsichtigten Vorgang ausführen und Systemzugriff autorisieren und Ausführen die Aufgabe im Auftrag eines Benutzers wird. Die Genehmigung bleibt gültig für den angeforderten Dauer (Dauer der Standardwert lautet 4 Stunden), in dem die anfordernde Person die vorgesehene Aufgabe mehrmals führen kann. Alle solchen Ausführungen sind angemeldet und für Sicherheit und Compliance Überwachung zur Verfügung gestellt. 

> [!NOTE]
> Wenn Sie Exchange Management PowerShell zur Aktivierung und Konfiguration Systemzugriff verwenden möchten, führen Sie die Schritte in Verbindung mit Exchange Online PowerShell mit Ihrer Office 365 [Connect to Exchange Online PowerShell mithilfe von Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) Anmeldeinformationen. Sie müssen nicht die mehrstufige Authentifizierung für Office 365-Organisation mit den Schritten um Systemzugriff zu ermöglichen, während eine Verbindung mit Exchange Online PowerShell aktivieren. Herstellen einer Verbindung mit Multi-Factor Authentication erstellt ein OAuth-Token, das vom Systemzugriff für die Anmeldung Ihre Anforderungen verwendet wird.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Schritt 1: Erstellen einer genehmigenden Person Gruppe

1. Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .

2. Wechseln Sie in der Verwaltungskonsole **Gruppen** > **Gruppe hinzufügen**.

3. Wählen Sie die **e-Mail-aktivierte Sicherheitsgruppe** Gruppentyp aus, und führen Sie dann die Felder **Name**, **Gruppe e-Mail-Adresse**und **Beschreibung** für die neue Gruppe.

4. Speichern Sie die Gruppe. Es dauert ein paar Minuten für die Gruppe vollständig konfiguriert werden und in der Office 365-Verwaltungskonsole angezeigt werden.

5. Wählen Sie die neue genehmigende Person aus, und wählen Sie zum Hinzufügen von Benutzern der Gruppe **Bearbeiten** .

6. Speichern Sie die Gruppe.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Schritt 2: Aktivieren von Systemzugriff

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .

2. Wechseln Sie in der Verwaltungskonsole zur **Einstellungen > Sicherheit und Datenschutz** > **Systemzugriff**.

3. Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .

4. Weisen Sie in Schritt 1 als den **Standard-Gruppe der genehmigenden Personen**erstellten Gruppe der genehmigenden Person.

5. **Speichern** und **Schließen**.

### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie den folgenden Befehl in Exchange Online PowerShell Systemzugriff aktivieren und der genehmigenden Person Gruppe zuweisen:
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
Beispiel:
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> Systemkonten, dass das Feature um sicherzustellen, dass bestimmte der Automatisierung innerhalb Ihrer Organisation zur Verfügung gestellt wird ohne Abhängigkeit an Systemzugriff arbeiten können, aber es wird empfohlen, dass solche Ausschlüsse außergewöhnliche werden und die zulässigen genehmigt und überwacht werden sollte Führen Sie regelmäßige.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Schritt 3: Erstellen einer Richtlinie für den Zugriff

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .

2. Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.

3. Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.

4. Wählen Sie **Richtlinien konfigurieren** , und wählen Sie **eine Richtlinie hinzufügen**.

5. Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:
    
    **Richtlinientyp**: Vorgangs-, Rolle oder Rollengruppe

    **Richtlinie auf Benutzerebene**: Exchange oder Office 365

    **Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien

    **Typ der statusgenehmigung**: manuell oder automatisch

    **Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte Gruppe der genehmigenden Personen

6. Wählen Sie **Erstellen** und dann auf **Schließen**. Es kann einige Minuten für die Richtlinie vollständig konfiguriert und aktiviert worden ist.

### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie folgenden Befehl in Exchange Online PowerShell zum Erstellen und eine Genehmigung zu definieren:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Beispiel:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Schritt 4: Genehmigen Sie Systemzugriff Anforderungen übermitteln /

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Elevation-Autorisierung auszuführende Aufgaben privilegierte anfordern

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.

2. Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.

3. Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.

4. Wählen Sie **neue Anforderung**. Wählen Sie aus dem Dropdown-Feldern die entsprechenden Werte für Ihre Organisation:

    **Anforderungstyp**: Vorgangs-, Rolle oder Rollengruppe

    **Bereich anfordern**: Exchange

    **Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien

    **Dauer (in Stunden)**: Anzahl von Stunden für den angeforderten Zugriff

    **Kommentare**: Textfeld für Kommentare im Zusammenhang mit Ihrer Access-Anforderung

5. Wählen Sie **Speichern** und dann auf **Schließen**. Ihre Anforderung wird der genehmigenden Person Gruppe per e-Mail gesendet werden.

#### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie den folgenden Befehl in Exchange Online PowerShell zum Erstellen und senden eine Aufforderung zur Genehmigung an die Gruppe der genehmigenden Person:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Beispiel:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Anzeigen des Status der Elevation-Anforderungen
Nach dem Erstellen einer genehmigungsanforderung Elevation Anforderungsstatus in der Verwaltungskonsole überprüft werden kann oder im Exchange Management PowerShell Anforderung mit der zugeordnete ID.

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.

2. Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.

3. Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.

4. Wählen Sie **Ansicht** zum Filtern von weitergeleiteten Anfragen nach dem Status **ausstehender**, **genehmigt**, **verweigert**oder **Kunden Lockbox** .

#### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Anforderung Genehmigungsstatus für eine bestimmte Anforderung ID anzuzeigen:
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Beispiel:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>Eine Erhöhung Autorisierung Anforderung genehmigen
Wenn eine Aufforderung zur Genehmigung erstellt wird, Mitglied der Gruppe relevanten genehmigende Person erhält eine e-Mail-Benachrichtigung und genehmigen die Anforderung der Anforderung ID zugeordnet werden kann Der Requestor wird die Anforderung zur Genehmigung oder Ablehnung per e-Mail-Nachricht benachrichtigt werden.

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der [Microsoft 365 Admin Center](https://portal.office.com) mit Ihren Anmeldeinformationen.

2. Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.

3. Wählen Sie **Verwalten Zugriffsrichtlinien und Anforderungen**.

4. Wählen Sie eine aufgelistete Anforderung, um die Details anzuzeigen und auszuführende Aktion auf die Anforderung.

5. Wählen Sie **Genehmigen** genehmigen die Anforderung, oder wählen Sie **Verweigern** , um die Anforderung zu verweigern. Zuvor können genehmigte Anforderungen durch Auswählen von **Sperren**widerrufen zugreifen.

#### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung genehmigen:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Beispiel:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Erhöhung Autorisierung Anforderung zu verweigern:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Beispiel:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a>Deaktivieren Sie Systemzugriff in Office 365

Falls erforderlich, können Sie für Ihre Organisation Systemzugriff Management deaktivieren. Deaktivieren von Berechtigungen wird Access keine zugehörigen Genehmigung Richtlinien oder eine genehmigende Person Gruppen gelöscht.

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden das Microsoft 365 Admin Center

1. Melden Sie sich bei der Verwendung von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation [Microsoft 365 Admin Center](https://portal.office.com) .

2. Wechseln Sie in der Verwaltungskonsole auf **Einstellungen** > **Sicherheit und Datenschutz** > **Systemzugriff**.

3. Aktivieren Sie das Steuerelement **Genehmigungen für Systemzugriff erfordern** .

### <a name="using-exchange-management-powershell"></a>Verwenden von PowerShell für Exchange-Verwaltung

Führen Sie den folgenden Befehl in Exchange Online Powershell, um Systemzugriff zu deaktivieren:

```
Disable-ElevatedAccessControl
```
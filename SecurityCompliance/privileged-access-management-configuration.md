---
title: Konfigurieren von privileged Access Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: In diesem Thema erfahren Sie mehr über das Konfigurieren von privileged Access Management in Office 365
ms.openlocfilehash: 3d186998006dd3cc59877b1571f50314af5bbce8
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492824"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>Konfigurieren von privileged Access Management in Office 365

> [!IMPORTANT]
> Dieses Thema enthält Informationen zur Bereitstellung und Konfiguration von Features, die derzeit nur in Office 365 E5 und Advanced Compliance-SKUs verfügbar sind.

In diesem Thema erfahren Sie, wie Sie die privilegierte Zugriffsverwaltung in Ihrer Office 365-Organisation aktivieren und konfigurieren. Sie können entweder das Microsoft 365 Admin Center oder die Exchange-Verwaltungs-PowerShell verwenden, um den privilegierten Zugriff zu verwalten und zu verwenden. 

## <a name="enable-and-configure-privileged-access-management"></a>Aktivieren und Konfigurieren der Verwaltung privilegierter Zugriffsrechte

Führen Sie die folgenden Schritte aus, um den privilegierten Zugriff in Ihrer Office 365-Organisation einzurichten und zu verwenden:

- [Schritt 1: Erstellen der Gruppe einer genehmigenden Person](privileged-access-management-configuration.md#step1)

    Bevor Sie mit dem Verwenden von Berechtigungszugriff beginnen, bestimmen Sie, wer über Genehmigungsautorität für eingehende Anforderungen für den Zugriff auf erhöhte und privilegierte Aufgaben verfügt. Jeder Benutzer, der Teil der Gruppe der genehmigenden Personen ist, kann Zugriffsanforderungen genehmigen. Dies wird durch das Erstellen einer e-Mail-aktivierten Sicherheitsgruppe in Office 365 aktiviert.

- [Schritt 2: Aktivieren des privilegierten Zugriffs](privileged-access-management-configuration.md#step2)

    Privilegierter Zugriff muss explizit in Office 365 mit der standardmäßigen genehmigenden Gruppe aktiviert werden und eine Reihe von Systemkonten enthalten, die Sie aus der Zugriffssteuerung für die privilegierte Zugriffsverwaltung ausschließen möchten.

- [Schritt 3: Erstellen einer Zugriffsrichtlinie](privileged-access-management-configuration.md#step3)

    Durch das Erstellen einer Genehmigungsrichtlinie können Sie die spezifischen Genehmigungsanforderungen für einzelne Aufgaben definieren. Die Optionen für den Genehmigungs sind **automatisch** oder **manuell**.

- [Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen](privileged-access-management-configuration.md#step4)

    Nach der Aktivierung erfordert der privilegierte Zugriff Genehmigungen für die Ausführung von Aufgaben, für die eine zugehörige Genehmigungsrichtlinie definiert ist. Benutzer, die Aufgaben ausführen müssen, die in der Genehmigungsrichtlinie enthalten sind, müssen die Zugriffsgenehmigung anfordern und erhalten, um die zum Ausführen der Aufgabe erforderlichen Berechtigungen zu erhalten.

Nachdem die Genehmigung erteilt wurde, kann der anfordernde Benutzer die vorgesehene Aufgabe ausführen, und der privilegierte Zugriff autorisiert und führt die Aufgabe im Namen der Benutzer aus. Die Genehmigung bleibt für die angeforderte Dauer (Standarddauer 4 Stunden) gültig, während der der anfordernde die vorgesehene Aufgabe mehrmals ausführen kann. Alle derartigen Ausführungen werden protokolliert und für die Sicherheits-und Konformitätsüberwachung zur Verfügung gestellt. 

> [!NOTE]
> Wenn Sie die Exchange-Verwaltungsshell zum Aktivieren und Konfigurieren des privilegierten Zugriffs verwenden möchten, führen Sie die Schritte unter [Herstellen einer Verbindung mit Exchange Online PowerShell mithilfe der mehr](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) stufigen Authentifizierung zum Herstellen einer Verbindung mit Exchange Online PowerShell mit ihrem Office 365 aus. Anmeldeinformationen. Sie müssen die mehrstufige Authentifizierung für Ihre Office 365-Organisation nicht aktivieren, um die Schritte zum Aktivieren des privilegierten Zugriffs beim Herstellen einer Verbindung mit Exchange Online PowerShell zu verwenden. Beim Herstellen einer Verbindung mit mehrstufiger Authentifizierung wird ein OAuth-Token erstellt, das von privilegiertem Zugriff zum Signieren von Anforderungen verwendet wird.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Schritt 1: Erstellen einer Gruppe von genehmigenden Personen

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.

2. Wechseln Sie im Admin Center zu **Gruppen** > **Hinzufügen einer Gruppe**.

3. Wählen Sie den Gruppentyp **e-Mail-aktivierte Sicherheitsgruppe** aus, und füllen Sie dann die Felder **Name**, **Gruppen-e-Mail-Adresse**und **Beschreibung** für die neue Gruppe aus.

4. Speichern Sie die Gruppe. Es kann einige Minuten dauern, bis die Gruppe vollständig konfiguriert ist und im Office 365 Admin Center angezeigt wird.

5. Wählen Sie die Gruppe neuer genehmigender aus, und wählen Sie **Bearbeiten** aus, um Benutzer zur Gruppe hinzuzufügen.

6. Speichern Sie die Gruppe.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Schritt 2: Aktivieren des privilegierten Zugriffs

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.

2. Navigieren Sie im Admin Center zu **Einstellungen > Security & Privacy** > **privileged Access**.

3. Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .

4. Weisen Sie die Gruppe der genehmigenden Personen, die Sie in Schritt 1 erstellt haben, als **Standardgruppe für genehmigende**Personen zu.

5. **Speichern** und **Beenden**.

### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu aktivieren und die Gruppe der genehmigenden Personen zuzuweisen:
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
Beispiel:
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> Das Feature "System Konten" wird bereitgestellt, um sicherzustellen, dass bestimmte Automatisierungen in Ihrer Organisation ohne Abhängigkeit vom privilegierten Zugriff funktionieren können, es wird jedoch empfohlen, dass diese Ausnahmen außergewöhnlich sind und diese zulässig sind. regelmäßig.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Schritt 3: Erstellen einer Zugriffsrichtlinie

Sie können bis zu 30 privilegierte Zugriffsrichtlinien für Ihre Office 365-Organisation erstellen und konfigurieren.

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.

4. Wählen Sie **Richtlinien konfigurieren** aus, und wählen Sie **Richtlinie hinzufügen**aus.

5. Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:
    
    **Richtlinientyp**: Aufgabe, Rolle oder Rollengruppe

    **Richtlinienbereich**: Exchange

    **Richtlinienname**: Wählen Sie aus den verfügbaren Richtlinien aus

    **** Genehmigungs: manuell oder automatisch

    **Genehmigungsgruppe**: Wählen Sie die in Schritt 1 erstellte genehmigende Gruppe aus.

6. Klicken Sie auf **Erstellen** und dann auf **Schließen**. Es kann einige Minuten dauern, bis die Richtlinie vollständig konfiguriert und aktiviert ist.

### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsrichtlinie zu erstellen und zu definieren:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Beispiel:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Schritt 4: überMitteln/genehmigen von privilegierten Zugriffsanforderungen

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Anfordern einer Erhöhungs Autorisierung zum Ausführen privilegierter Aufgaben

Anforderungen für den privilegierten Zugriff sind bis zu 24 Stunden nach der Übermittlung der Anforderung gültig. Wenn diese nicht genehmigt oder verweigert werden, werden die Anforderungen ablaufen, und der Zugriff wird nicht genehmigt.

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.

4. Wählen Sie **neue Anforderung**aus. Wählen Sie in den Dropdownfeldern die entsprechenden Werte für Ihre Organisation aus:

    **Anforderungstyp**: Aufgabe, Rolle oder Rollengruppe

    **Anforderungsbereich**: Exchange

    **Anforderung für**: Wählen Sie aus den verfügbaren Richtlinien

    **Dauer (Stunden)**: Anzahl der Stunden des angeforderten Zugriffs. Es gibt keine Begrenzung für die Anzahl der Stunden, die angefordert werden können.

    **Kommentare**: Textfeld für Kommentare in Bezug auf ihre Zugriffsanforderung

5. Klicken Sie auf **Speichern** und dann auf **Schließen**. Ihre Anfrage wird per e-Mail an die Gruppe der genehmigenden Person gesendet.

#### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Genehmigungsanforderung an die Gruppe der genehmigenden Personen zu erstellen und zu übermitteln:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Beispiel:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Anzeigen des Status von Ansichts Anforderungen
Nachdem eine Genehmigungsanforderung erstellt wurde, kann der Status der Höhen Anforderung im Admin Center oder in der Exchange-Verwaltungs-PowerShell mithilfe der ID der Anforderung zugeordnet werden.

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.

4. Wählen Sie **Ansicht** aus, um übermittelte Anforderungen nach dem Status Ausstehend, **genehmigt**, **verweigert**oder **Kunden** zu filtern. ****

#### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Status einer Genehmigungsanforderung für eine bestimmte Anforderungs-ID anzuzeigen:
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Beispiel:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>Genehmigen einer Elevation-Autorisierungsanforderung
Wenn eine Genehmigungsanforderung erstellt wird, erhalten Mitglieder der entsprechenden genehmigenden Gruppe eine e-Mail-Benachrichtigung und können die Anforderung genehmigen, die der Anforderungs-ID zugeordnet ist. Der Anforderer wird über eine e-Mail-Nachricht über die Genehmigung oder Ablehnung der Anforderung benachrichtigt.

#### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich mit Ihren Anmeldeinformationen beim [Microsoft 365 Admin Center](https://portal.office.com) an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.

4. Wählen Sie eine aufgeführte Anforderung aus, um die Details anzuzeigen und Aktionen für die Anforderung durchführen zu können.

5. Wählen **** Sie genehmigen aus, um die Anforderung zu genehmigen, oder wählen Sie **verweigern** , um die Anforderung zu verweigern. Zuvor genehmigten Anforderungen kann der Zugriff widerrufen werden, indem Sie **REVOKE**auswählen.

#### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Elevation-Autorisierungsanforderung zu genehmigen:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Beispiel:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Elevation-Autorisierungsanforderung zu verweigern:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Beispiel:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Löschen einer Richtlinie für privilegierten Zugriff in Office 365
Sie können eine Richtlinie für den privilegierten Zugriff löschen, wenn Sie in Ihrer Organisation nicht mehr benötigt wird.

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Wählen Sie **Zugriffsrichtlinien und-Anforderungen verwalten**aus.

4. Wählen Sie **Richtlinien konfigurieren**aus.

5. Wählen Sie die Richtlinie aus, die Sie löschen möchten, und wählen Sie dann **Richtlinie entfernen**aus.

6. Wählen Sie **Schließen** aus.

### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine privilegierte Zugriffsrichtlinie zu löschen:

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>Deaktivieren des privilegierten Zugriffs in Office 365

Bei Bedarf können Sie die privilegierte Zugriffsverwaltung für Ihre Organisation deaktivieren. Durch das Deaktivieren des privilegierten Zugriffs werden keine zugehörigen Genehmigungsrichtlinien oder genehmigenden Gruppen gelöscht.

### <a name="using-the-microsoft-365-admin-center"></a>Verwenden des Microsoft 365 Admin Center

1. Melden Sie sich beim [Microsoft 365 Admin Center](https://portal.office.com) mithilfe von Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an.

2. Navigieren Sie im Admin Center zu **Einstellungen** > **Security & Privacy** > **privileged Access**.

3. Aktivieren Sie das Kontrollelement **Genehmigungen für privilegierten Zugriff anfordern** .

### <a name="using-exchange-management-powershell"></a>Verwenden der Exchange-Verwaltungs-PowerShell

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den privilegierten Zugriff zu deaktivieren:

```
Disable-ElevatedAccessControl
```
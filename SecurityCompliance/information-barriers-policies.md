---
title: Definieren von Richtlinien für Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Hier erfahren Sie, wie Sie Richtlinien für Informationsbarrieren in Microsoft Teams definieren.
ms.openlocfilehash: 3ec9d89f22456f00104135013ee6009e8e4824df
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668302"
---
# <a name="define-policies-for-information-barriers-preview"></a>Definieren von Richtlinien für Informationsbarrieren (Vorschau)

Mit Informationsbarrieren können Sie Richtlinien definieren, mit denen verhindert werden soll, dass bestimmte Segmente von Benutzern miteinander kommunizieren, oder dass bestimmte Segmente nur mit bestimmten anderen Segmenten kommunizieren dürfen. Richtlinien für Informationsbarrieren können Ihrem Unternehmen dabei helfen, die Einhaltung relevanter Branchenstandards und-Vorschriften beizubehalten und potenzielle Interessenkonflikte zu vermeiden. Weitere Informationen finden Sie unter [Information Barriers (Preview)](information-barriers.md). 

> [!IMPORTANT]
> In diesem Artikel wird beschrieben, wie Sie Richtlinien für Informationsbarrieren planen, definieren, implementieren und verwalten. Es sind mehrere Schritte beteiligt, und der Arbeitsfluss ist in mehrere Teile unterteilt. Stellen Sie sicher, dass Sie die [voraus](#prerequisites) setzungen und den gesamten Prozess gelesen haben, bevor Sie mit dem definieren (oder bearbeiten) von Informations Sperrrichtlinien beginnen.

## <a name="concepts-of-information-barrier-policies"></a>Konzepte von Richtlinien für Informationsbarrieren

Bevor Sie Informationen Barrier Policies planen, definieren und implementieren, sollten Sie die zugrunde liegenden Konzepte kennen. Mit Informationsbarrieren arbeiten Sie mit Benutzerkonto Attributen, Segmenten, Richtlinien für Informationsbarrieren und einem Richtlinien Anwendungsprozess, der in diesem Artikel beschrieben wird. 

- **Benutzerkontoattribute** werden in Azure Active Directory (oder Exchange Online) definiert. Diese Attribute können Abteilung, Position, Standort, Teamname usw. umfassen. 

- **Segmente** werden im Office 365 Security #a0 Compliance Center mithilfe eines ausgewählten **Benutzerkontoattributs**wie Abteilung, Position, Ort, Teamname oder eines beliebigen [unterstützten Attributs](information-barriers-attributes.md)definiert. Das Definieren von Segmenten wirkt sich nicht auf Benutzer aus. Es wird lediglich die Stufe für die Definition von Informationsschranken Richtlinien festgelegt und dann angewendet.

- **Richtlinien für Informationsbarrieren** werden definiert und **** einzelnen Segmenten zugewiesen. Nicht allen Segmenten wird eine Richtlinie zugewiesen. Darüber hinaus kann keinem einzelnen Segment mehr als eine Richtlinie zugewiesen werden. Wenn Sie Richtlinien definieren, wählen Sie aus zwei Arten von Richtlinien:
    - Richtlinien, die verhindern, dass ein Segment mit einem anderen Segment kommuniziert
    - Richtlinien, mit denen ein Segment nur mit bestimmten anderen Segmenten kommunizieren kann

    Im Idealfall verwenden Sie die Mindestanzahl von Richtlinien, um sicherzustellen, dass Ihre Organisation den rechtlichen und branchenspezifischen Anforderungen entspricht.

- Die **Richtlinienanwendung** wird ausgeführt, nachdem alle Richtlinien für Informationsbarrieren definiert wurden und Sie Sie in Ihrer Organisation anwenden können.

## <a name="the-work-flow-at-a-glance"></a>Der Workflow auf einen Blick

|Phase    |Was ist involviert  |
|---------|---------|
|[Stellen Sie sicher, dass die Voraussetzungen erfüllt sind](#prerequisites)     |-Sicherstellen, dass Ihr Abonnement Informationsbarrieren enthält<br/>-Sicherstellen, dass Sie über die erforderlichen Berechtigungen zum Definieren/Bearbeiten von Segmenten und Richtlinien verfügen<br/>-Stellen Sie sicher, dass Ihre Verzeichnisdaten die Struktur Ihres Unternehmens widerspiegeln.<br/>-Stellen Sie sicher, dass die bereichsbezogene Verzeichnissuche in Microsoft Teams aktiviert ist.<br/>-Stellen Sie sicher, dass die Überwachungsprotokollierung aktiviert ist.<br/>-Verwenden von PowerShell zum Ausführen der Aufgaben in diesem Artikel (Beispiel-Cmdlets werden bereitgestellt)<br/>-Bereitstellen der Zustimmung des Administrators für Informationsbarrieren in Microsoft Teams (Schritte sind enthalten)          |
|[Teil 1: segmentieren aller Benutzer in Ihrer Organisation](#part-1-segment-users)     |-Bestimmen der erforderlichen Richtlinien<br/>-Eine Liste der zu definierenden Segmente erstellen<br/>-Bestimmen der zu verwendenden Attribute<br/>-Definieren von Segmenten in Bezug auf Richtlinienfilter        |
|[Abschnitt 2: Definieren von Richtlinien für Informationsbarrieren](#part-2-define-information-barrier-policies)     |-Definieren Ihrer Richtlinien (noch nicht gültig)<br/>-Auswählen aus zwei Arten (blockieren oder zulassen) |
|[Abschnitt 3: Anwenden von Richtlinien für Informationsbarrieren](#part-3-apply-information-barrier-policies)     |-Festlegen von Richtlinien auf aktiven Status<br/>-Ausführen der Richtlinienanwendung<br/>-Überprüfen des Richtlinienstatus         |
|(Nach Bedarf) [Bearbeiten eines Segments oder einer Richtlinie](#edit-a-segment-or-a-policy)     |-Bearbeiten eines Segments<br/>-Bearbeiten oder Entfernen einer Richtlinie<br/>-Ausführen der Richtlinienanwendung<br/>-Überprüfen des Richtlinienstatus         |
|(Nach Bedarf) [Problembehandlung](information-barriers-troubleshooting.md)|-Maßnahmen ergreifen, wenn Richtlinien nicht wie erwartet funktionieren|

## <a name="prerequisites"></a>Voraussetzungen

**Derzeit befindet sich das Feature "Informations Barriere" in privater Vorschau**. Wenn diese Features allgemein verfügbar sind, werden Sie in Abonnements eingeschlossen, beispielsweise:

- Microsoft 365 E5
- Office 365 E5
- Office 365 Erweiterte Compliance
- Microsoft 365 E5 – Informationsschutz und Compliance

Weitere Informationen finden Sie unter [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).

### <a name="permissions"></a>Berechtigungen

Um Richtlinien für Informationsbarrieren zu definieren oder zu bearbeiten, **muss Ihnen eine entsprechende Rolle zugewiesen sein**, beispielsweise eine der folgenden:
- Microsoft 365 Enterprise-Global-Administrator
- Office 365 globaler Administrator
- Complianceadministrator
- IB-Konformitätsverwaltung (Dies ist eine neue Rolle!)

Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Berechtigungen im Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).
       
### <a name="directory-data"></a>Verzeichnisdaten

**Stellen Sie sicher, dass die Struktur Ihrer Organisation in Verzeichnisdaten widergespiegelt wird**. Stellen Sie dazu sicher, dass die Attribute des Benutzerkontos wie Gruppenmitgliedschaft, Abteilungsname usw. ordnungsgemäß in Azure Active Directory (oder Exchange Online) aufgefüllt werden. Weitere Informationen finden Sie in den folgenden Ressourcen:
- [Attribute für Richtlinien für Informationsbarrieren (Vorschau)](information-barriers-attributes.md)
- [Hinzufügen oder Aktualisieren der Profilinformationen eines Benutzers mithilfe von Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)
- [Konfigurieren von Eigenschaften eines Benutzerkontos mit Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)

### <a name="scoped-directory-search"></a>Suche im bereichsbezogenen Verzeichnis

**Bevor Sie die erste Richtlinie für Informationsbarrieren Ihrer Organisation definieren, müssen Sie die [bereichsbezogene Verzeichnissuche in Microsoft Teams aktivieren](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)**. Warten Sie mindestens 24 Stunden nach dem Aktivieren der bereichsbezogenen Verzeichnissuche, bevor Sie Richtlinien für Informationsbarrieren einrichten oder definieren.

### <a name="audit-logging"></a>Überwachungsprotokollierung

Um den Status einer Richtlinienanwendung nachzuschlagen, muss die Überwachungsprotokollierung aktiviert sein. Dies wird empfohlen, bevor Sie mit dem Definieren von Segmenten oder Richtlinien beginnen. Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren von Office 365 Überwachungsprotokoll Suche](turn-audit-log-search-on-or-off.md).

### <a name="powershell"></a>PowerShell

**Derzeit werden Richtlinien für Informationsbarrieren im Office 365 Security #a0 Compliance Center mithilfe von PowerShell-Cmdlets definiert und verwaltet**. In diesem Artikel werden zwar mehrere Szenarien und Beispiele bereitgestellt, aber Sie müssen mit PowerShell-Cmdlets und-Parametern vertraut sein. 

Stellen [Sie eine Verbindung mit Office 365 Security #a0 Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="provide-admin-consent-for-information-barriers-in-microsoft-teams"></a>Bereitstellen der Zustimmung des Administrators für Informationsbarrieren in Microsoft Teams

Verwenden Sie das folgende Verfahren, um Richtlinien für Informationsbarrieren zu aktivieren, die in Microsoft Teams erwartungsgemäß funktionieren. 

Wenn Ihre Richtlinien beispielsweise vorhanden sind, können Informationsbarrieren Personen aus Chatsitzungen entfernen, in denen Sie sich nicht befinden sollen. Dadurch wird sichergestellt, dass Ihre Organisation mit den Richtlinien und Vorschriften konform bleibt. 

1. Führen Sie die folgenden PowerShell-Cmdlets aus:

    ```
    Login-AzureRmAccount 
    $appId="bcf62038-e005-436d-b970-2a472f8c1982" 
    $sp=Get-AzureRmADServicePrincipal -ServicePrincipalName $appId
    if ($sp -eq $null) { New-AzureRmADServicePrincipal -ApplicationId $appId }
    Start-Process  "https://login.microsoftonline.com/common/adminconsent?client_id=$appId"
    ```

2. Wenn Sie dazu aufgefordert werden, melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.

3. Überprüfen Sie im Dialogfeld **angeforderte Berechtigungen** die Informationen, und wählen Sie dann **akzeptieren**aus.

## <a name="part-1-segment-users"></a>Teil 1: Segment Benutzer

In dieser Phase bestimmen Sie, welche Richtlinien benötigt werden, erstellen eine Liste der zu definierenden Segmente und definieren dann Ihre Segmente.

### <a name="determine-what-policies-are-needed"></a>Bestimmen der erforderlichen Richtlinien

Unter Berücksichtigung gesetzlicher und Branchen rechtlicher bestimmungensind die Gruppen in Ihrer Organisation, die Richtlinien für Informationsbarrieren benötigen? Erstellen Sie eine Liste. Gibt es Gruppen, die daran gehindert werden sollen, mit einer anderen Gruppe zu kommunizieren? Gibt es Gruppen, die nur mit einer oder zwei anderen Gruppen kommunizieren dürfen? Denken Sie an die Richtlinien, die Sie als Zugehörigkeit zu einer von zwei Gruppen benötigen:
- **Blockieren von Richtlinien** , die verhindern, dass eine Gruppe mit einer anderen Gruppe kommuniziert
- **Zulassen von Richtlinien** , mit denen bestimmte Gruppen nur mit bestimmten anderen Gruppen kommunizieren können

Wenn Sie über eine anfängliche Liste von Gruppen und Richtlinien verfügen, fahren Sie mit dem Identifizieren der benötigten Segmente fort.

(Siehe [Beispiel: Contosos Abteilungen und Plan](#contosos-departments-and-plan) in diesem Artikel.)

### <a name="identify-segments"></a>Identifizieren von Segmenten

Erstellen Sie zusätzlich zu Ihrer anfänglichen Richtlinienliste eine Liste der Segmente für Ihre Organisation. Jeder Benutzer in Ihrer Organisation sollte zu einem Segment gehören, und kein Benutzer sollte zu zwei oder mehr Segmenten gehören. Für jedes Segment kann nur eine Informations Sperrrichtlinie angewendet werden. 

Bestimmen Sie, welche Attribute in den Verzeichnisdaten Ihrer Organisation verwendet werden, um Segmente zu definieren. Sie können *Department*, Mitglied ** oder eines der unterstützten Attribute verwenden. Stellen Sie sicher, dass Sie Werte in dem Attribut haben, das Sie für alle Benutzer auswählen. Eine Liste der unterstützten Attribute finden Sie unter [Attribute for Information Barrier Policies (Preview)](information-barriers-attributes.md).

> [!IMPORTANT]
> **Bevor Sie mit dem nächsten Abschnitt fortfahren, stellen Sie sicher, dass Ihre Verzeichnisdaten Werte für Attribute aufweisen, die Sie zum Definieren von Segmenten verwenden können**. Wenn Ihre Verzeichnisdaten keine Werte für die Attribute enthalten, die Sie verwenden möchten, müssen alle Benutzerkonten aktualisiert werden, um diese Informationen einzubeziehen, bevor Sie mit Informationsbarrieren fortfahren. Wenn Sie Hilfe dazu erhalten möchten, lesen Sie die folgenden Ressourcen:<br/>- [Konfigurieren von Eigenschaften von Benutzerkonten mit Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)<br/>- [Hinzufügen oder Aktualisieren der Profilinformationen eines Benutzers mithilfe von Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)

### <a name="define-segments-using-powershell"></a>Definieren von Segmenten mithilfe von PowerShell

> [!IMPORTANT]
> **Stellen Sie sicher, dass sich Ihre Segmente nicht überschneiden**. Jeder Benutzer in Ihrer Organisation sollte zu einem (und nur einem) Segment gehören. Kein Benutzer sollte zu zwei oder mehr Segmenten gehören. Segmente sollten für alle Benutzer in Ihrer Organisation definiert werden. (Siehe [Beispiel: Contosos definierte Segmente](#contosos-defined-segments) in diesem Artikel.)

1. Verwenden Sie zum Definieren eines Organisations Segments das **New-OrganizationSegment-** Cmdlet mit dem **UserGroupFilter** -Parameter, der dem [Attribut](information-barriers-attributes.md) entspricht, das Sie verwenden möchten. 

    Syntax`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`

    Beispiel: `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`

    In diesem Beispiel wird ein Segment namens *HR* mithilfe von *HR*definiert, einem Wert im Department-Attribut.

2. Wiederholen Sie Schritt 1 für jedes Segment, das Sie definieren möchten.

    Nach dem Ausführen jedes Cmdlets sollte eine Liste mit Details zum neuen Segment angezeigt werden. Details umfassen den Typ des Segments, wer es erstellt oder zuletzt geändert hat usw. 

Nachdem Sie Ihre Segmente definiert haben, fahren Sie mit define Information Barrier Policies fort.

## <a name="part-2-define-information-barrier-policies"></a>Abschnitt 2: Definieren von Richtlinien für Informationsbarrieren

Wählen Sie mit der Liste der Benutzersegmente und den Richtlinien für Informationsbarrieren, die Sie definieren möchten, ein Szenario aus, und führen Sie dann die Schritte aus. 

> [!IMPORTANT]
> **Stellen Sie sicher, dass Sie bei der Definition von Richtlinien keinem Segment mehr als eine Richtlinie zuweisen**. Wenn Sie beispielsweise eine Richtlinie für ein Segment mit dem Namen " *Sales*" definieren, definieren Sie keine zusätzliche Richtlinie für den *Vertrieb*. 

Bestimmen Sie, ob Sie die Kommunikation zwischen bestimmten Segmenten verhindern oder die Kommunikation auf bestimmte Segmente beschränken müssen. Wählen Sie zwischen den Szenarien unten aus, um Ihre Richtlinien zu definieren.

- [Szenario 1: Blockieren der Kommunikation zwischen Segmenten](#scenario-1-block-communications-between-segments)
- [Szenario 2: zulassen, dass ein Segment nur mit einem anderen Segment kommuniziert](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)

> [!NOTE]
> Achten Sie beim Definieren von Richtlinien für Informationsbarrieren darauf, diese Richtlinien auf inaktiven Status festzulegen, bis Sie bereit sind, Sie anzuwenden. Das definieren (oder bearbeiten) von Richtlinien wirkt sich erst dann auf Benutzer aus, wenn diese Richtlinien auf aktiver Status festgelegt und dann angewendet wurden.

(Weitere Informationen finden Sie in diesem Artikel unter [Beispiel: Contosos Information Barrier Policies](#contosos-information-barrier-policies) .)

### <a name="scenario-1-block-communications-between-segments"></a>Szenario 1: Blockieren der Kommunikation zwischen Segmenten

Wenn Sie verhindern möchten, dass Segmente miteinander kommunizieren, definieren Sie zwei Richtlinien: eine für jede Richtung. Jede Richtlinie blockiert die Kommunikation nur auf eine Weise.

Nehmen Sie beispielsweise an, dass Sie die Kommunikation zwischen Segment a und Segment B blockieren möchten. In diesem Fall definieren Sie eine Richtlinie, die verhindert, dass Segment a mit Segment b kommuniziert, und dann eine zweite Richtlinie definieren, um zu verhindern, dass Segment b mit Segment A kommuniziert.

1. Verwenden Sie zum Definieren Ihrer ersten Sperrrichtlinie das Cmdlet **New-InformationBarrierPolicy** mit dem Parameter **SegmentsBlocked** . 

    Syntax`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`

    Beispiel: `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`

    In diesem Beispiel haben wir eine Richtlinie mit dem Namen " *Sales-Research* " für ein Segment namens " *Sales*" definiert. Wenn diese Richtlinie aktiv und angewendet wird, wird verhindert, dass Personen im *Vertrieb* mit Personen in einem Segment mit dem Namen *Research*kommunizieren.

2. Verwenden Sie zum Definieren des zweiten Sperr Segments das Cmdlet **New-InformationBarrierPolicy** mit dem Parameter **SegmentsBlocked** erneut, diesmal mit umgekehrten Segmenten.

    Beispiel: `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`

    In diesem Beispiel wurde eine Richtlinie mit dem Namen *Research-Sales* definiert, um zu verhindern, dass die Forschung mit dem Vertrieb kommuniziert.
 
2. Führen Sie einen der folgenden Schritte aus:

   - (Falls erforderlich) [Definieren einer Richtlinie, mit der ein Segment nur mit einem anderen Segment kommunizieren kann](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment) 
   - (Nachdem alle Ihre Richtlinien definiert wurden) [Anwenden von Richtlinien für Informationsbarrieren](#part-3-apply-information-barrier-policies)

### <a name="scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment"></a>Szenario 2: zulassen, dass ein Segment nur mit einem anderen Segment kommuniziert

1. Damit ein Segment nur mit einem anderen Segment kommunizieren kann, verwenden Sie das Cmdlet **New-InformationBarrierPolicy** mit dem Parameter **SegmentsAllowed** . 

    Syntax`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`

    Beispiel: `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    In diesem Beispiel haben wir eine Richtlinie mit dem Namen *Manufacturing-HR* für ein Segment namens *Manufacturing*definiert. Wenn diese Richtlinie aktiv und angewendet wird, können Sie in der *Fertigung* nur Personen in einem Segment namens *HR*kommunizieren. (In diesem Fall kann die Fertigung nicht mit Benutzern kommunizieren, die nicht Teil von HR sind.)

    **Bei Bedarf können Sie mit diesem Cmdlet mehrere Segmente angeben, wie in den folgenden beiden Beispielen dargestellt.**

    Syntax`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`

    **Beispiel 1: Definieren einer Richtlinie, mit der mehrere Segmente mit nur einem anderen Segment kommunizieren können**

    `New-InformationBarrierPolicy -Name "ResearchManufacturing-HR" -AssignedSegment "Research, Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    In diesem Beispiel haben wir eine Richtlinie definiert, die es den *Forschungs* -und *Fertigungs* Segmenten ermöglicht, nur mit *HR*zu kommunizieren.

    **Beispiel 2: Definieren einer Richtlinie, um zu ermöglichen, dass mehrere Segmente nur mit bestimmten anderen Segmenten kommunizieren**    

    `New-InformationBarrierPolicy -Name "SalesMarketing-HRManufacturing" -AssignedSegment "Sales, Marketing" -SegmentsAllowed "HR, Manufacturing" -State Inactive`

    In diesem Beispiel haben wir eine Richtlinie definiert, mit der die Segmente *Vertrieb* und *Marketing* nur mit *HR* und *Manufacturing*kommunizieren können.

    Wiederholen Sie diesen Schritt für jede Richtlinie, die Sie definieren möchten, damit bestimmte Segmente nur mit bestimmten anderen Segmenten kommunizieren können.

2. Führen Sie einen der folgenden Schritte aus:

   - (Falls erforderlich) [Definieren einer Richtlinie zum Blockieren der Kommunikation zwischen Segmenten](#scenario-1-block-communications-between-segments) 
   - (Nachdem alle Ihre Richtlinien definiert wurden) [Anwenden von Richtlinien für Informationsbarrieren](#part-3-apply-information-barrier-policies)

## <a name="part-3-apply-information-barrier-policies"></a>Abschnitt 3: Anwenden von Richtlinien für Informationsbarrieren

Richtlinien für Informationsbarrieren werden erst wirksam, wenn Sie Sie auf aktiver Status festlegen und dann die Richtlinien anwenden.

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der definierten Richtlinien anzuzeigen. Notieren Sie den Status und die Identität (GUID) der einzelnen Richtlinien.

    Syntax`Get-InformationBarrierPolicy`

2. Um eine Richtlinie auf den aktiven Status festzulegen, verwenden Sie das Cmdlet "InformationBarrierPolicy" mit einem **Identity** -Parameter und den **State** **-** Parameter auf " **aktiv**" festgelegt. 

    Syntax`Set-InformationBarrierPolicy -Identity GUID -State Active`

    Beispiel: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`
    
    In diesem Beispiel wird eine Richtlinie für Informationsbarrieren festgelegt, bei der die GUID *43c37853-EA10-4b90-a23d-ab8c93772471* den Status aktiv besitzt.

    Wiederholen Sie diesen Schritt für jede Richtlinie entsprechend.

3. Wenn Sie die Richtlinien für Informationsbarrieren auf den aktiven Status festgesetzt haben, verwenden Sie das Cmdlet **Start-InformationBarrierPoliciesApplication** im Office 365 Security #a0 Compliance Center.

    Syntax`Start-InformationBarrierPoliciesApplication`

    Nach etwa einer halben Stunde werden Richtlinien angewendet, Benutzer nach Benutzer, für Ihre Organisation. Wenn Ihre Organisation groß ist, kann es 24 Stunden (oder mehr) dauern, bis dieser Prozess abgeschlossen ist. (Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.)

## <a name="verify-status-of-user-accounts-segments-policies-or-policy-application"></a>Überprüfen des Status von Benutzerkonten, Segmenten, Richtlinien oder Richtlinien Anwendungen

Mithilfe von PowerShell können Sie den Status von Benutzerkonten, Segmenten, Richtlinien und Richtlinien Anwendungen überprüfen, wie in der folgenden Tabelle aufgeführt.

|So überprüfen Sie dies  |Aktion  |
|---------|---------|
|Benutzerkonten     |Verwenden Sie das Cmdlet **Get-InformationBarrierRecipientStatus** mit Identitäts Parametern. <p>Syntax`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>Sie können einen beliebigen Wert verwenden, der jeden Benutzer eindeutig identifiziert, beispielsweise Name, Alias, Distinguished Name, kanonischer Domänenname, e-Mail-Adresse oder GUID. <p>Beispiel: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>In diesem Beispiel wird auf zwei Benutzerkonten in Office 365 verwiesen: *meganb* für *Megan*und *alexw* für *Alex*. <p>(Sie können dieses Cmdlet auch für einen einzelnen Benutzer verwenden: `Get-InformationBarrierRecipientStatus -Identity <value>`) <p>Dieses Cmdlet gibt Informationen zu Benutzern zurück, beispielsweise Attributwerte und alle angewendeten Richtlinien für Informationsbarrieren.|
|Segmente     |Verwenden Sie das Cmdlet **Get-OrganizationSegment** .<p>Syntax`Get-OrganizationSegment` <p>Dadurch wird eine Liste aller Segmente angezeigt, die für Ihre Organisation definiert sind.         |
|Richtlinien für Informationsbarrieren     |Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** . <p> Syntax`Get-InformationBarrierPolicy` <p>Dadurch wird eine Liste der definierten Richtlinien für Informationsbarrieren angezeigt, die definiert wurden, und deren Status.       |
|Die neueste Informations Barriere-Richtlinienanwendung     | Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** . <p>Syntax`Get-InformationBarrierPoliciesApplicationStatus`<p>    Dadurch werden Informationen darüber angezeigt, ob die Richtlinienanwendung abgeschlossen, ein Fehler aufgetreten ist oder ausgeführt wird.       |
|Alle Informations Barrier Policy-Anwendungen|Verwenden`Get-InformationBarrierPoliciesApplicationStatus -All $true`<p>Dadurch werden Informationen darüber angezeigt, ob die Richtlinienanwendung abgeschlossen, ein Fehler aufgetreten ist oder ausgeführt wird.|

## <a name="stop-a-policy-application"></a>Beenden einer Richtlinienanwendung

Wenn Sie die Anwendung von Richtlinien für Informationsbarrieren gestartet haben und diese Richtlinien nicht mehr angewendet werden sollen, verwenden Sie das folgende Verfahren. Denken Sie daran, dass es ungefähr 30-35 Minuten dauern wird, bis der Prozess beginnt.

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPoliciesApplicationStatus** , um den Status der neuesten Informations Barriere-Richtlinienanwendung anzuzeigen.

    Syntax`Get-InformationBarrierPoliciesApplicationStatus`

    Beachten Sie die GUID der Anwendung.

2. Verwenden Sie das Cmdlet **Stop-InformationBarrierPoliciesApplication** mit einem Identity-Parameter.

    Syntax`Stop-InformationBarrierPoliciesApplication -Identity GUID`

    Beispiel: `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`

## <a name="edit-a-segment-or-a-policy"></a>Bearbeiten eines Segments oder einer Richtlinie

### <a name="edit-a-segment"></a>Bearbeiten eines Segments

1. Verwenden Sie das Cmdlet **Get-OrganizationSegment** , um alle vorhandenen Segmente anzuzeigen.
    
    Syntax`Get-OrganizationSegment`

    Es wird eine Liste mit Segmenten und Details für jede, wie Segmenttyp, den UserGroupFilter-Wert, der erstellt oder zuletzt geändert, Guid, und so weiter angezeigt.

    > [!TIP]
    > Drucken oder speichern Sie die Liste der Segmente als Referenz später. Wenn Sie beispielsweise ein Segment bearbeiten möchten, müssen Sie dessen Namen oder den Wert ermitteln (dieser wird mit dem Parameter Identity verwendet).

2. Verwenden Sie zum Bearbeiten eines Segments das Cmdlet " **OrganizationSegment** " mit dem Parameter " **Identity** " und den relevanten Details. 

    Syntax`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`

    Beispiel: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`

    In diesem Beispiel haben wir für das Segment mit dem GUID- *c96e0837-C232-4a8a-841e-ef45787d8fcd*den Namen der Abteilung in "HRDept" geändert.

Wenn Sie die Bearbeitung von Segmenten für Ihre Organisation abgeschlossen haben, können Sie mit dem [definieren](#part-2-define-information-barrier-policies) oder [Bearbeiten](#edit-a-policy) von Richtlinien für Informationsbarrieren fortfahren.

### <a name="edit-a-policy"></a>Bearbeiten einer Richtlinie

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.

    Syntax`Get-InformationBarrierPolicy`

    Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie ändern möchten. Beachten Sie die GUID und den Namen der Richtlinie.

2. Verwenden Sie das Cmdlet "InformationBarrierPolicy" mit einem **Identity** **-** Parameter, und geben Sie die Änderungen an, die Sie vornehmen möchten.

    Syntax (Blockieren von Segmenten für die Kommunikation mit anderen Segmenten): 

    `Set-InformationBarrierPolicy -Identity GUID -SegmentsBlocked "segmentname, segmentname"` 

    Syntax (Aktivieren von Segmenten zur Kommunikation nur mit bestimmten anderen Segmenten):
    
    ``Set-InformationBarrierPolicy -Identity GUID -SegmentsAllowed "segmentname, segmentname"``

    Beispiel: angenommen, eine Richtlinie wurde definiert, um zu verhindern, dass die Forschung mit Vertrieb und Marketing kommuniziert. Die Richtlinie wurde mithilfe dieses Cmdlets definiert:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`
    
    Angenommen, wir möchten diese ändern, damit Personen in der Forschung nur mit Personen in HR kommunizieren können. Um diese Änderung vorzunehmen, verwenden wir dieses Cmdlet:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`

3. Wenn Sie die Bearbeitung einer Richtlinie abgeschlossen haben, sollten Sie Ihre Änderungen übernehmen. (Weitere Informationen finden Sie unter [Apply Information Barrier Policies](#part-3-apply-information-barrier-policies).)

### <a name="remove-a-policy"></a>Entfernen einer Richtlinie

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.

    Syntax`Get-InformationBarrierPolicy`

    Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie entfernen möchten. Beachten Sie die GUID und den Namen der Richtlinie. Stellen Sie sicher, dass die Richtlinie auf inaktiver Status festgelegt ist.

2. Verwenden Sie das Cmdlet **Remove-InformationBarrierPolicy** mit einem Identity-Parameter.

    Syntax`Remove-InformationBarrierPolicy -Identity GUID`

    Beispiel: nehmen wir an, dass eine Richtlinie mit GUID- *43c37853-EA10-4b90-a23d-ab8c93772471*entfernt werden soll. Zu diesem Zweck verwenden wir dieses Cmdlet:
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    Bestätigen Sie die Änderung, wenn Sie dazu aufgefordert werden.

3. Wiederholen Sie die Schritte 1-2 für jede Richtlinie, die Sie entfernen möchten.

4. Wenn Sie das Entfernen von Richtlinien abgeschlossen haben, wenden Sie die Änderungen an. Verwenden Sie dazu das Cmdlet **Start-InformationBarrierPoliciesApplication** .

    Syntax`Start-InformationBarrierPoliciesApplication`

    Änderungen werden angewendet, Benutzer nach Benutzer, für Ihre Organisation. Wenn Ihre Organisation groß ist, kann es 24 Stunden (oder mehr) dauern, bis dieser Prozess abgeschlossen ist.

### <a name="set-a-policy-to-inactive-status"></a>Festlegen einer Richtlinie auf inaktiver Status

1. Verwenden Sie das Cmdlet **Get-InformationBarrierPolicy** , um eine Liste der aktuellen Information Barrier-Richtlinien anzuzeigen.

    Syntax`Get-InformationBarrierPolicy`

    Identifizieren Sie in der Ergebnisliste die Richtlinie, die Sie ändern möchten (oder entfernen). Beachten Sie die GUID und den Namen der Richtlinie.

2. Um den Status der Richtlinie auf inaktiv festzulegen, verwenden Sie das Cmdlet "InformationBarrierPolicy" mit einem Identity-Parameter und dem State **-** Parameter auf "inaktiv" festgelegt.

    Syntax`Set-InformationBarrierPolicy -Identity GUID -State Inactive`

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    In diesem Beispiel wird eine Richtlinie für Informationsbarrieren festgelegt, die GUID *43c37853-EA10-4b90-a23d-ab8c9377247* in einen inaktiven Status hat.

3. Verwenden Sie das Cmdlet **Start-InformationBarrierPoliciesApplication** , um die Änderungen zu übernehmen.

    Syntax`Start-InformationBarrierPoliciesApplication`

    Änderungen werden angewendet, Benutzer nach Benutzer, für Ihre Organisation. Wenn Ihre Organisation groß ist, kann es 24 Stunden (oder mehr) dauern, bis dieser Prozess abgeschlossen ist. (Als allgemeine Richtlinie dauert es etwa eine Stunde, 5.000-Benutzerkonten zu verarbeiten.)

Zu diesem Zeitpunkt werden mindestens eine Richtlinie für Informationsbarrieren auf inaktiver Status festgelegt. Von hier aus können Sie einen der folgenden Schritte ausführen:
- Lassen Sie es unverändert (eine Richtlinie, die auf inaktiven Status festgelegt ist, hat keine Auswirkungen auf die Benutzer)
- [Bearbeiten einer Richtlinie](#edit-a-policy) 
- [Entfernen einer Richtlinie](#remove-a-policy)

## <a name="example-contosos-departments-segments-and-policies"></a>Beispiel: Abteilungen, Segmente und Richtlinien von Contoso

Um zu sehen, wie sich eine Organisation an das Definieren von Segmenten und Richtlinien wenden kann, betrachten Sie das folgende Beispiel.

### <a name="contosos-departments-and-plan"></a>Abteilungen und Plan von Contoso

Contoso verfügt über fünf Abteilungen: HR, Vertrieb, Marketing, Forschung und Fertigung. Um mit den Branchenrichtlinien konform zu bleiben, sollten Personen in einigen Abteilungen nicht mit anderen Abteilungen kommunizieren, wie in der folgenden Tabelle aufgeführt:

|Segment  |Sprechen kann  |Kann nicht mit  |
|---------|---------|---------|
|HR     |Alle         |(keine Einschränkungen)         |
|Sales     |HR, Marketing, Produktion         |Recherche         |
|Marketing     |Alle         |(keine Einschränkungen)         |
|Recherche     |HR, Marketing, Produktion        |Sales     |
|Fertigung |HR, Marketing |Andere Personen als HR oder Marketing |

In diesem Hinblick umfasst der Plan von Contoso drei Richtlinien für Informationsbarrieren:

1. Eine Richtlinie, die verhindert, dass Verkäufe mit der Forschung kommunizieren (und eine andere Richtlinie, um zu verhindern, dass die Forschung mit dem Vertrieb kommuniziert)
2. Eine Richtlinie, mit der die Fertigung nur mit HR und Marketing kommunizieren kann 

Es ist nicht erforderlich, Richtlinien für HR oder Marketing zu definieren.

### <a name="contosos-defined-segments"></a>Definierte Segmente von Contoso

Contoso wird das Department-Attribut in Azure Active Directory verwenden, um Segmente wie folgt zu definieren:

|Abteilung  |Segment Definition  |
|---------|---------|
|HR     | `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`        |
|Sales     | `New-OrganizationSegment -Name "Sales" -UserGroupFilter "Department -eq 'Sales'"`        |
|Marketing     | `New-OrganizationSegment -Name "Marketing" -UserGroupFilter "Department -eq 'Marketing'"`        |
|Recherche     | `New-OrganizationSegment -Name "Research" -UserGroupFilter "Department -eq 'Research'"`        |
|Fertigung     | `New-OrganizationSegment -Name "Manufacturing" -UserGroupFilter "Department -eq 'Manufacturing'"`        |

Nachdem die Segmente definiert wurden, werden von Contoso Richtlinien definiert. 

### <a name="contosos-information-barrier-policies"></a>Richtlinien für Informationsbarrieren von Contoso

Contoso definiert drei Policen, wie in der folgenden Tabelle beschrieben:

|Richtlinie  |Richtliniendefinition  |
|---------|---------|
|Richtlinie 1: verhindern, dass Verkäufe mit Forschung kommunizieren     | `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p> In diesem Beispiel wird die Richtlinie "Informations Barriere" als " *Sales-Research*" bezeichnet. Wenn diese Richtlinie aktiv ist und angewendet wird, können Benutzer, die sich im Vertriebs Segment befinden, nicht mit Benutzern im Forschungs Segment kommunizieren. Dies ist eine unidirektionale Richtlinie. Damit wird nicht verhindert, dass die Forschung mit dem Vertrieb kommuniziert. Dafür ist Richtlinie 2 erforderlich.      |
|Richtlinie 2: verhindern, dass die Forschung mit dem Vertrieb kommuniziert     | `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p> In diesem Beispiel wird die Richtlinie "Informations Barriere" als " *Research-Sales*" bezeichnet. Wenn diese Richtlinie aktiv ist und angewendet wird, können Benutzer, die sich im Forschungs Segment befinden, nicht mit Benutzern im Vertriebs Segment kommunizieren.       |
|Richtlinie 3: zulassen, dass die Fertigung nur mit HR und Marketing kommuniziert     | `New-InformationBarrierPolicy -Name "Manufacturing-HRMarketing" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR, Marketing" -State Inactive` <p>In diesem Fall wird die Richtlinie "Informations Barriere" als " *Manufacturing-HRMarketing*" bezeichnet. Wenn diese Richtlinie aktiv ist und angewendet wird, kann Manufacturing nur mit HR und Marketing kommunizieren. Beachten Sie, dass HR und Marketing nicht von der Kommunikation mit anderen Segmenten eingeschränkt werden. |

Wenn Segmente und Richtlinien definiert sind, wendet Contoso die Richtlinien durch Ausführen des Cmdlets **Start-InformationBarrierPoliciesApplication** an. 

Wenn dieser Vorgang abgeschlossen ist, entspricht Contoso den rechtlichen und branchenspezifischen Anforderungen.

## <a name="related-articles"></a>Verwandte Artikel

[Hier erhalten Sie einen Überblick über Informationsbarrieren](information-barriers.md)

[Weitere Informationen zu Informationsbarrieren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[Attribute für Richtlinien für Informationsbarrieren (Vorschau)](information-barriers-attributes.md)

[Problembehandlung bei Informationsbarrieren (Vorschau)](information-barriers-troubleshooting.md)

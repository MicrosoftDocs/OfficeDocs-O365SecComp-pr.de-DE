---
title: So identifizieren Sie den Typ der Warteschleife platziert auf einem Exchange Online-Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
ms.openlocfilehash: d24e51bca0e3d290f110b1ab40f3ee9ae7993678
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529717"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>So identifizieren Sie den Typ der Warteschleife platziert auf einem Exchange Online-Postfach

In diesem Artikel wird erläutert, wie in Exchange Online-Postfächern in Office 365 platziert Haltestatus identifiziert.

Office 365 bietet eine Reihe von Methoden, die Ihrer Organisation Inhalt von Postfächern zu verhindern kann dauerhaft gelöscht. Dies ermöglicht der Organisation beibehalten Inhalts Compliance regulären Rubriken im Magazin erfüllen oder für die Dauer der rechtlichen oder anderen Typen von Untersuchungen. Es folgt eine Liste der Aufbewahrung Features (auch gewählte Haltestatus) in Office 365:

- **Aufbewahrung für eventuelle Rechtsstreitigkeiten** - Haltestatus an, die auf Benutzerpostfächer in Exchange Online angewendet werden.

- **halten Sie eDiscovery** - Haltestatus an, die einem eDiscovery-Fall im Compliance Center & Sicherheit zugeordnet sind. eDiscovery-Haltestatus können für Office 365-Gruppen und Microsoft-Teams, auf die Benutzerpostfächer, und klicken Sie auf das entsprechende Postfach angewendet werden.

- **In-Place Hold** - Haltestatus an, die auf die Benutzerpostfächer angewendet werden, mithilfe der In-Place eDiscovery & Hold-Tool in der Exchange-Administrator zentriert im Exchange Online.

- **Aufbewahrungsrichtlinie für Office 365** - Inhalte in Benutzerpostfächern in Exchange Online und in das entsprechende Postfach für Office 365-Gruppen und Microsoft-Teams, behält. Sie können eine Aufbewahrungsrichtlinie erstellen Richtlinie behält Skype für Business Unterhaltungen, die in die Benutzerpostfächer gespeichert sind.

  Es gibt zwei Arten von Office 365-Aufbewahrungsrichtlinien, die Postfächer zugewiesen werden können.

    - **Aufbewahrungsrichtlinien bestimmten Speicherort** - Hierbei handelt es sich um Richtlinien, die die Speicherorte für Inhalte von bestimmten Benutzern zugewiesen sind. Verwenden Sie das Cmdlet Get-Mailbox in Exchange Online PowerShell, Abrufen von Informationen zu Aufbewahrungsrichtlinien auf bestimmte Postfächer zugewiesen.

    - **Aufbewahrungsrichtlinien organisationsweiten** - Hierbei handelt es sich um Richtlinien, die alle Speicherorte für Inhalte in Ihrer Organisation zugewiesen sind. Verwenden Sie das Cmdlet Get-OrganizationConfig in Exchange Online PowerShell, Abrufen von Informationen zu Aufbewahrungsrichtlinien organisationsweiten. Weitere Informationen finden Sie im Abschnitt "Anwenden einer Aufbewahrungsrichtlinie auf eine gesamte Organisation oder bestimmte Orte" in der Übersicht über die Office 365-Aufbewahrungsrichtlinien.

Zum Verwalten von Postfächern in der Warteschleife müssen Sie möglicherweise den Typ des Haltestatus zu identifizieren, die für ein Postfach befindet, sodass Sie Aufgaben wie das Ändern der Dauer halten, vorübergehend oder endgültig den Haltestatus entfernen oder Ausschließen eines Postfachs aus einer Aufbewahrungsrichtlinie für Office 365 ausführen können. In diesen Fällen wird im erste Schritt identifiziert den Typ des Haltestatus für das Postfach platziert. Und da mehrere Haltestatus (und anderen Arten von Haltestatus) auf ein einzelnes Postfach angeordnet werden können, müssen Sie alle Haltestatus für ein Postfach platziert werden, wenn Sie möchten, entfernen oder Ändern dieser Aufbewahrungspflichten zu identifizieren.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Schritt 1: Abrufen von die GUID für den Haltestatus für ein Postfach platziert

Sie können die folgenden zwei Cmdlets ausführen, in Exchange Online PowerShell, um die GUID des Haltestatus abzurufen, die für ein Postfach platziert werden. Nachdem Sie eine GUID abgerufen haben, verwenden Sie es zum Identifizieren des bestimmten Haltebereich in Schritt2 ein. Beachten Sie, dass Rechtsstreitigkeiten enthält nicht von einer GUID identifiziert werden. Rechtsstreitigkeiten sind für ein Postfach entweder aktiviert oder deaktiviert.

- **Get-Mailbox** - verwenden, dieses Cmdlet, um zu bestimmen, ob die Aufbewahrung für eventuelle Rechtsstreitigkeiten für ein Postfach aktiviert ist und die GUIDs für eDiscovery abzurufen enthält, Compliance-Archive und Office 365-Aufbewahrungsrichtlinien, die speziell für ein Postfach zugewiesen sind. Die Ausgabe dieses Cmdlets wird auch angeben, ob ein Postfach aus einer Organisation geltende Aufbewahrungsrichtlinie explizit ausgeschlossen wurde.

- **Get-OrganizationConfig** – verwenden Sie dieses Cmdlet die GUIDs für organisationsweite Aufbewahrungsrichtlinien abrufen.

Zum Verbinden mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Führen Sie den folgenden Befehl zum Abrufen von Informationen zu den Haltestatus und Office 365-Aufbewahrungsrichtlinien an ein Postfach angewendet.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Wenn in der Eigenschaft InPlaceHolds zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jede GUID in einer separaten Zeile angezeigt.

In der folgenden Tabelle wird beschrieben, wie zum Identifizieren der verschiedener Arten von Haltestatus basierend auf den Werten in der *InPlaceHolds* -Eigenschaft, wenn Sie das **Get-Mailbox** -Cmdlet ausführen.


|Haltebereichstyp  |Beispielwert  |So identifizieren Sie den Haltestatus  |
|---------|---------|---------|
|Beweissicherungsverfahren     |    `True`     |     Aufbewahrung für eventuelle Rechtsstreitigkeiten für ein Postfach aktiviert ist, wenn die *LitigationHoldEnabled* -Eigenschaft, um festgelegt ist `True`.    |
|eDiscovery-Archiv     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   Die *InPlaceHolds-Eigenschaft* enthält die GUID der eine Sperre einer eDiscovery-Fall im Compliance Center & Sicherheit zugeordnet. Sie können erkennen, dies ist ein eDiscovery halten, da die GUID mit beginnt die `UniH` Prefix (das Unified halten bezeichnet).      |
|Compliance-Archiv     |     `c0ba3ce811b6432a8751430937152491` <br/> oder <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     Die *InPlaceHolds* -Eigenschaft enthält die GUID der der Compliance-Archivs, das für das Postfach befindet. Sie können erkennen, dies ist eine In-Place Hold, da die GUID nicht entweder mit einem Präfix starten, oder er beginnt mit der `cld` Präfix.     |
|Office 365 Aufbewahrungsrichtlinie explizit an das Postfach angewendet.     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> oder <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     Die InPlaceHolds-Eigenschaft enthält die GUIDs der jede bestimmten Speicherort Aufbewahrungsrichtlinie, die an das Postfach angewendet wird. Sie können Aufbewahrungsrichtlinien identifizieren, weil die GUID mit beginnt die `mbx` oder die `skp` Präfix. Die `skp` Präfix gibt an, dass die Aufbewahrungsrichtlinie auf Skype für Business Unterhaltungen in das Postfach des Benutzers angewendet wird.    |
|Von einer Organisation geltende Office 365-Aufbewahrungsrichtlinie ausgeschlossen     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Wenn ein Postfach aus einer Organisation geltende Office 365-Aufbewahrungsrichtlinie ausgeschlossen wird, die GUID für die Aufbewahrungsrichtlinie wird das Postfach von ausgeschlossen wird angezeigt, in der InPlaceHolds-Eigenschaft und lässt sich durch die `-mbx` Präfix.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Wenn die *InPlaceHolds* -Eigenschaft leer ist, wenn Sie das **Get-Mailbox** -Cmdlet ausführen, gibt es noch möglicherweise einen oder mehrere organisationsweiten Office 365 Aufbewahrungsrichtlinien auf das Postfach angewendet. Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Liste der GUIDs für Office 365-Aufbewahrungsrichtlinien organisationsweiten abrufen.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Wenn in der Eigenschaft InPlaceHolds zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jede GUID in einer separaten Zeile angezeigt.

Die folgende Tabelle beschreibt die verschiedenen Typen von organisationsweiten Haltestatus und So identifizieren Sie jede Type basierend auf die GUIDs in *InPlaceHolds* -Eigenschaft enthalten sind, wenn Sie das Cmdlet **Get-OrganizationConfig** ausführen.


|Haltebereichstyp  |Beispielwert  |Beschreibung  |
|---------|---------|---------|
|Office 365 Aufbewahrungsrichtlinien auf Exchange-Postfächer, öffentliche Exchange-Ordner und Teams Chats angewendet    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Organisationsweite Aufbewahrungsrichtlinien angewendet auf Exchange-Postfächer, öffentliche Exchange-Ordner und 1xN Chats in Microsoft-Teams, werden durch GUIDs, die mit beginnen identifiziert die `mbx` Präfix. Beachten Sie, dass im Postfach der einzelnen Chat Teilnehmer 1xN Chats gespeichert sind.      |
|Office 365 Aufbewahrungsrichtlinie auf Office 365-Gruppen und Teams Channel Nachrichten angewendet     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Organisationsweite Aufbewahrungsrichtlinien auf Office 365-Gruppen und Kanalnachrichten in Microsoft-Teams, DDE-angewendet werden durch GUIDs, die mit beginnen identifiziert die `grp` Präfix. Beachten Sie, dass Channel Nachrichten im Gruppenpostfach gespeichert werden, die einem Microsoft-Team zugeordnet ist.     |

Weitere Informationen-Aufbewahrungsrichtlinien angewendet, die Microsoft-Teams finden Sie unter dem Abschnitt "Teams Speicherort" [Übersicht über die Aufbewahrungsrichtlinien](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Grundlegendes zum Format des Werts InPlaceHolds für Aufbewahrungsrichtlinien

Zusätzlich zu den Präfix (Mbx, Skp oder Gruppe), das ein Element in der InPlaceHolds-Eigenschaft, wie eine Aufbewahrungsrichtlinie für Office 365 identifiziert, enthält den Wert auch ein Suffix, das den Typ der Aufbewahrungsaktion identifiziert, die für die Richtlinie konfiguriert ist. Beispielsweise wird das Suffix Aktion in den folgenden Beispielen fett hervorgehoben:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

In der folgenden Tabelle sind die drei mögliche aufbewahrungsaktionen definiert:

|Wert  |Beschreibung  |
|---------|---------|
|**1**     | Gibt an, dass die Aufbewahrungsrichtlinie konfiguriert ist, um Elemente zu löschen. die Richtlinie nicht Elemente aufbewahrt werden.        |
|**2**    |    Gibt an, dass die Aufbewahrungsrichtlinie konfiguriert ist, um Elemente aufzunehmen. die Richtlinie löschen nicht Elemente, nachdem der Aufbewahrungszeitraum abgelaufen ist.     |
|**3**     |   Gibt an, dass die Aufbewahrungsrichtlinie konfiguriert ist, um halten von Elementen, und löschen Sie sie, nachdem der Aufbewahrungszeitraum abgelaufen ist.      |

Weitere Informationen zu aufbewahrungsaktionen finden Sie im Abschnitt "Content für einen bestimmten Zeitraum Mauer" unter [Overview of Aufbewahrungsrichtlinien](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Schritt 2: Mithilfe der GUID zum Identifizieren der Warteschleife

Nachdem Sie die GUID für einen Haltestatus erhalten haben, die an ein Postfach angewendet wird, besteht der nächste Schritt mit dieser GUID, den Haltestatus identifiziert. Die folgenden Abschnitte zeigen So identifizieren Sie den Namen des Haltestatus (und andere Informationen) mit dem Haltebereich GUID.

### <a name="ediscovery-holds"></a>eDiscovery-Haltestatus

Führen Sie die folgenden Befehle in Sicherheit und Compliance Center PowerShell, eine eDiscovery-Archiv zu identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich das Präfix UniH) für die eDiscovery halten, dass Sie in Schritt 1 identifiziert haben. Der erste Befehl erstellt eine Variable, die Informationen zu den Haltestatus enthält. Diese Variable wird in den anderen Befehlen verwendet. Der zweite Befehl zeigt den Namen des eDiscovery-Fall, der Haltebereich zugeordnet ist. Der dritte Befehl zeigt den Namen des Haltestatus und eine Liste der Postfächer, auf denen der Haltestatus angewendet wird.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Zum Verbinden mit Sicherheits- und Compliance Center PowerShell finden Sie unter [Connect to Office 365-Sicherheit und Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>In-Situ-Speicher

Führen Sie den folgenden Befehl in Exchange Online PowerShell, die In-Place Hold identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID für die Compliance-Archivs, die Sie in Schritt 1 identifiziert. Der Befehl zeigt den Namen des Haltestatus und eine Liste der Postfächer, auf denen der Haltestatus angewendet wird.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Beachten Sie, dass bei die GUID, für die Compliance-Archivs mit beginnt die `cld` Präfix, müssen Sie das Präfix enthalten, beim Ausführen des vorherigen Befehls.

### <a name="office-365-retention-policies"></a>Office 365-Aufbewahrungsrichtlinien

Führen Sie dem folgenden Befehl in Sicherheit und Compliance Center PowerShell für die Identität der Office 365-Aufbewahrungsrichtlinie (organisationsweite oder bestimmte Speicherort), die an das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich der Mbx, Skp oder Gruppe Präfix oder das Suffix Aktion), die Sie in Schritt 1 identifiziert.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="next-steps"></a>Nächste Schritte

Wenn Sie den Haltestatus identifiziert haben, die an ein Postfach angewendet werden, können Sie Aufgaben wie die Dauer des Haltestatus, vorübergehend ändern oder dauerhaft entfernt den Haltestatus oder im Fall von Office 365-Aufbewahrungsrichtlinien, Ausführen ein inaktives Postfachs aus der Richtlinie ausgenommen. Weitere Informationen zum Ausführen von Aufgaben im Zusammenhang mit Haltestatus finden Sie unter eins der folgenden Themen:

- Führen Sie die [Set-RetentionCompliancePolicy - AddExchangeLocationException \<Benutzerpostfach >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) Command in Sicherheit und Compliance Center PowerShell ein Postfach aus einer Organisation geltende Office 365-Aufbewahrungsrichtlinie ausschließen. Beachten Sie, dass dieser Befehl nur für Aufbewahrungsrichtlinien verwendet werden kann, wobei der Wert für die Eigenschaft *ExchangeLocation* entspricht `All`.

- Führen Sie die [Set-Mailbox - ExcludeFromOrgHolds \<halten, GUID ohne Präfix oder Suffix >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) Command in Exchange Online PowerShell ein inaktives Postfachs aus einer Organisation geltende Office 365-Aufbewahrungsrichtlinie ausschließen.

- [Ändern Sie die Dauer halten eines inaktiven Postfachs in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

- [Löschen von Elementen im Ordner "wiederherstellbare Elemente" des cloudbasierten Postfächer in der Warteschleife](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)

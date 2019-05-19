---
title: Identifizieren des Haltebereichs für ein Exchange Online-Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Hier erfahren Sie, wie Sie die verschiedenen Aufbewahrungs Typen identifizieren können, die in einem Office 365 Postfach gespeichert werden können. Zu diesen Aufbewahrungsarten zählen Beweissicherungsverfahren, eDiscovery-Haltestatus und Office 365-Aufbewahrungsrichtlinien. Sie können auch ermitteln, ob ein Benutzer von einer unternehmensweiten Aufbewahrungsrichtlinie ausgeschlossen wurde.
ms.openlocfilehash: 29ae9d7ba8be2bf0064c163605aee9ad8fd5fd07
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154197"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Identifizieren des Haltebereichs für ein Exchange Online-Postfach

In diesem Artikel wird erläutert, wie Sie auf Exchange Online Postfächern in Office 365 angeordnete haltebereiche identifizieren.

Office 365 bietet eine Reihe von Möglichkeiten, mit denen Ihre Organisation verhindern kann, dass Postfachinhalte endgültig gelöscht werden. Auf diese Weise kann Ihre Organisation Inhalte beibehalten, um die Compliance-Regularien oder die Dauer rechtlicher oder anderer Arten von Untersuchungen zu erfüllen. Im folgenden finden Sie eine Liste der Aufbewahrungs Features ( ** auch "Holds" genannt) in Office 365:

- **Beweissicherungsverfahren** , die auf Benutzerpostfächer in Exchange Online angewendet werden.

- **eDiscovery Hold-halte** Status, die einem eDiscovery-Fall im Security and Compliance Center zugeordnet sind. eDiscovery-Haltestatus können auf Benutzerpostfächer und auf das entsprechende Postfach für Office 365 Gruppen und Microsoft Teams angewendet werden.

- **In-** situ-Aufbewahrungsspeicher, die auf Benutzerpostfächer mithilfe des in-situ-eDiscovery-& in der Exchange-Verwaltungskonsole in Exchange Online angewendet werden.

- **Office 365 Aufbewahrungsrichtlinie** : behält Inhalte in Benutzerpostfächern in Exchange Online und im entsprechenden Postfach für Office 365 Gruppen und Microsoft Teams bei. Sie können eine Aufbewahrungsrichtlinie erstellen behält Skype for Business Unterhaltungen bei, die in Benutzerpostfächern gespeichert sind.

  Es gibt zwei Arten von Office 365-Aufbewahrungsrichtlinien, die Postfächern zugewiesen werden können.

    - **Spezifische Aufbewahrungsrichtlinien für Standorte** – Dies sind Richtlinien, die den Inhaltsspeicherorten bestimmter Benutzer zugewiesen sind. Verwenden Sie das Cmdlet **Get-Mailbox** in Exchange Online PowerShell, um Informationen zu Aufbewahrungsrichtlinien abzurufen, die bestimmten Postfächern zugewiesen sind.

    - **Organisationsweite Aufbewahrungsrichtlinien** -Dies sind Richtlinien, die allen Inhaltsspeicherorten in Ihrer Organisation zugewiesen sind. Verwenden Sie das Cmdlet **Get-OrganizationConfig** in Exchange Online PowerShell, um Informationen zu organisationsweiten Aufbewahrungsrichtlinien zu erhalten.
  Weitere Informationen finden Sie im Abschnitt "Anwenden einer Aufbewahrungsrichtlinie auf eine gesamte Organisation oder bestimmte Standorte" in [Overview of Office 365 Retention Policies](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Office 365 Aufbewahrungs Bezeichnungen** : Wenn ein Benutzer eine Office 365 Aufbewahrungs Bezeichnung anwendet (eine, die für die Aufbewahrung von Inhalten oder das aufbewahren ** und Löschen von Inhalten konfiguriert ist) in einem Ordner oder Element in seinem Postfach, wird ein Aufbewahrungsplatz auf das Postfach gesetzt, als ob das Postfach in einem Beweissicherungsverfahren gespeichert oder einer Office 365 Aufbewahrungsrichtlinie zugewiesen. Weitere Informationen finden Sie unter [Identifizieren von Postfächern in der Warteschleife, da eine Aufbewahrungs Bezeichnung auf einen Ordner oder ein Element](#identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item) Abschnitt in diesem Artikel angewendet wurde.

Zum Verwalten von Postfächern müssen Sie möglicherweise den Aufbewahrungs für ein Postfach identifizieren, sodass Sie Aufgaben wie das Ändern der Aufbewahrungsdauer, vorübergehendes oder dauerhaftes Entfernen des haltebereichs oder Ausschließen eines Postfachs aus einer Office 365-Aufbewahrungsrichtlinie ausführen können. In diesen Fällen besteht der erste Schritt darin, den Typ des für das Postfach gelegten Haltestatus zu identifizieren. Da mehrere haltebereiche (und unterschiedliche Aufbewahrungs Typen) in einem einzelnen Postfach gespeichert werden können, müssen Sie alle in einem Postfach enthaltenen haltebereiche identifizieren, wenn Sie diese Sperren entfernen oder ändern möchten.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Schritt 1: Abrufen der GUID für in einem Postfach gelegte Haltestatus

Sie können die folgenden zwei Cmdlets in Exchange Online PowerShell ausführen, um die GUID der Haltestatus abzurufen, die in einem Postfach gespeichert werden. Nachdem Sie eine GUID abgerufen haben, verwenden Sie Sie, um den bestimmten Haltebereich in Schritt 2 zu identifizieren. Beachten Sie, dass Beweissicherungsverfahren nicht durch eine GUID identifiziert werden. Beweissicherungsverfahren sind für ein Postfach entweder aktiviert oder deaktiviert.

- **Get-Mailbox** -verwenden Sie dieses Cmdlet, um festzustellen, ob das Beweissicherungsverfahren für ein Postfach aktiviert ist, und um die GUIDs für eDiscovery Holds, in-situ-Speicher und Office 365 Aufbewahrungsrichtlinien abzurufen, die speziell einem Postfach zugewiesen sind. Die Ausgabe dieses Cmdlets gibt außerdem an, ob ein Postfach explizit von einer Aufbewahrungsrichtlinie für die Organisation ausgeschlossen wurde.

- **Get-OrganizationConfig** -verwenden Sie dieses Cmdlet, um die GUIDs für organisationsweite Aufbewahrungsrichtlinien abzurufen.

Wie Sie eine Verbindung mit Exchange Online PowerShell herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Führen Sie den folgenden Befehl aus, um Informationen zu den Haltebereichen und Office 365 Aufbewahrungsrichtlinien zu erhalten, die auf ein Postfach angewendet werden.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Wenn die InPlaceHolds-Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den Befehl ausführen, um `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` die einzelnen GUIDs in einer separaten Zeile anzuzeigen.

In der folgenden Tabelle wird beschrieben, wie Sie unterschiedliche Aufbewahrungs Typen basierend auf den Werten in der *InPlaceHolds* -Eigenschaft identifizieren, wenn Sie das Cmdlet **Get-Mailbox** ausführen.


|Haltebereichstyp  |Beispielwert  |Vorgehensweise zum Identifizieren des Haltestatus  |
|---------|---------|---------|
|Aufbewahrung für eventuelle Rechtsstreitigkeiten     |    `True`     |     Das Beweissicherungsverfahren ist für ein Postfach aktiviert, wenn die *LitigationHoldEnabled* - `True`Eigenschaft auf festgelegt ist.    |
|eDiscovery-Aufbewahrung     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   Die *InPlaceHolds-Eigenschaft* enthält die GUID aller Halterungen, die einem eDiscovery-Fall im Security and Compliance Center zugeordnet sind. Sie können feststellen, dass es sich um einen eDiscovery-Speicher handelt `UniH` , da die GUID mit dem Präfix beginnt (das einen einheitlichen Haltestatus bezeichnet).      |
|Compliance-Archiv     |     `c0ba3ce811b6432a8751430937152491` <br/> oder <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     Die *InPlaceHolds* -Eigenschaft enthält die GUID des in-situ-Speichers, der im Postfach platziert wird. Sie können feststellen, dass es sich um einen in-situ-Speicher handelt, da die GUID entweder nicht mit einem `cld` Präfix beginnt oder mit dem Präfix beginnt.     |
|Office 365 Aufbewahrungsrichtlinie, die speziell auf das Postfach angewendet wird     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> oder <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     Die InPlaceHolds-Eigenschaft enthält GUIDs einer bestimmten Aufbewahrungsrichtlinie für Standorte, die auf das Postfach angewendet wird. Sie können Aufbewahrungsrichtlinien identifizieren, da die GUID mit `mbx` dem oder `skp` dem Präfix beginnt. Das `skp` Präfix gibt an, dass die Aufbewahrungsrichtlinie auf Skype for Business Unterhaltungen im Postfach des Benutzers angewendet wird.    |
|Von einer organisationsweiten Office 365 Aufbewahrungsrichtlinie ausgeschlossen     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Wenn ein Postfach aus einer organisationsweiten Office 365 Aufbewahrungsrichtlinie ausgeschlossen wird, wird die GUID für die Aufbewahrungsrichtlinie, von der das Postfach ausgeschlossen wird, in der InPlaceHolds-Eigenschaft angezeigt `-mbx` und durch das Präfix identifiziert.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Wenn die *InPlaceHolds* -Eigenschaft beim Ausführen des Cmdlets **Get-Mailbox** leer ist, kann es möglicherweise eine oder mehrere organisationsweite Office 365 Aufbewahrungsrichtlinien auf das Postfach angewendet werden. Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Liste von GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Wenn die InPlaceHolds-Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den Befehl ausführen, um `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` die einzelnen GUIDs in einer separaten Zeile anzuzeigen.

In der folgenden Tabelle werden die unterschiedlichen Typen von organisationsweiten Haltebereichen beschrieben, und Sie können jeden Typ basierend auf den in der *InPlaceHolds* -Eigenschaft enthaltenen GUIDs identifizieren, wenn Sie das Cmdlet **Get-OrganizationConfig** ausführen.


|Haltebereichstyp  |Beispielwert  |Beschreibung  |
|---------|---------|---------|
|Office 365 von Aufbewahrungsrichtlinien, die auf Exchange-Postfächer, öffentliche Exchange-Ordner und Chats von Teams angewendet werden    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer, öffentliche Exchange-Ordner und 1xN-Chats in Microsoft Teams angewendet werden, werden durch `mbx` GUIDs identifiziert, die mit dem Präfix beginnen. Beachten Sie, dass 1xN-Chats im Postfach der einzelnen Chat Teilnehmer gespeichert werden.      |
|Office 365-Aufbewahrungsrichtlinie, die auf Office 365 Gruppen und Teams Kanal Nachrichten angewendet wird     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Organisationsweite Aufbewahrungsrichtlinien, die auf Office 365 Gruppen und Kanal Nachrichten in Microsoft Teams angewendet werden, werden durch GUIDs identifiziert `grp` , die mit dem Präfix beginnen. Beachten Sie, dass Kanal Nachrichten im Gruppenpostfach gespeichert werden, das einem Microsoft-Team zugeordnet ist.     |

Weitere Informationen zu Aufbewahrungsrichtlinien, die auf Microsoft Teams angewendet werden, finden Sie im Abschnitt "Teams-Standort" unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Grundlegendes zum Format des InPlaceHolds-Werts für Aufbewahrungsrichtlinien

Zusätzlich zum Präfix (MBX, SKP oder GRP), das ein Element in der InPlaceHolds-Eigenschaft als Office 365 Aufbewahrungsrichtlinie identifiziert, enthält der Wert auch ein Suffix, das den Typ der Aufbewahrungsaktion identifiziert, die für die Richtlinie konfiguriert ist. Beispielsweise wird das Aktions Suffix in den folgenden Beispielen fett dargestellt:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

In der folgenden Tabelle werden die drei möglichen Aufbewahrungsaktionen definiert:

|Wert  |Beschreibung  |
|---------|---------|
|**1**     | Gibt an, dass die Aufbewahrungsrichtlinie zum Löschen von Elementen konfiguriert ist. die Richtlinie behält keine Elemente bei.        |
|**2**    |    Gibt an, dass die Aufbewahrungsrichtlinie zum Speichern von Elementen konfiguriert ist. die Richtlinie löscht keine Elemente nach Ablauf des Aufbewahrungszeitraums.     |
|**3**     |   Gibt an, dass die Aufbewahrungsrichtlinie so konfiguriert ist, dass Sie Elemente aufbewahrt und anschließend nach Ablauf des Aufbewahrungszeitraums gelöscht wird.      |

Weitere Informationen zu Aufbewahrungsaktionen finden Sie im Abschnitt "Aufbewahrung von Inhalten für einen bestimmten Zeitraum" in Übersicht über [Aufbewahrungsrichtlinien](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Schritt 2: Verwenden der GUID zum Identifizieren des Haltestatus

Nachdem Sie die GUID für einen auf ein Postfach angewendeten Haltestatus abgerufen haben, besteht der nächste Schritt darin, diese GUID zum Identifizieren des Haltestatus zu verwenden. In den folgenden Abschnitten wird gezeigt, wie Sie den Namen des Haltestatus (und andere Informationen) mithilfe der Hold-GUID identifizieren.

### <a name="ediscovery-holds"></a>eDiscovery-Aufbewahrung

Führen Sie die folgenden Befehle in Security & Compliance Center PowerShell aus, um einen eDiscovery-Speicher zu identifizieren, der auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne das UniH-Präfix) für den eDiscovery-Haltebereich, den Sie in Schritt 1 identifiziert haben. Mit dem ersten Befehl wird eine Variable erstellt, die Informationen zum Haltestatus enthält. Diese Variable wird in den anderen Befehlen verwendet. Der zweite Befehl zeigt den Namen des eDiscovery-Falls an, dem der Haltebereich zugeordnet ist. Der dritte Befehl zeigt den Namen des Haltestatus und eine Liste der Postfächer an, für die der Aufbewahrungsplatz gilt.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Informationen zum Herstellen einer Verbindung mit dem Security & Compliance Center PowerShell finden Sie unter [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>In-Situ-Speicher

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den in-situ-Speicher zu identifizieren, der auf das Postfach angewendet wird. Verwenden Sie die GUID für den in-situ-Speicher, den Sie in Schritt 1 identifiziert haben. Der Befehl zeigt den Namen des Haltestatus und eine Liste der Postfächer an, für die der Aufbewahrungsplatz gilt.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Beachten Sie Folgendes: Wenn die GUID für den in-situ-Speicher `cld` mit dem Präfix beginnt, müssen Sie unbedingt das Präfix einschließen, wenn Sie den vorherigen Befehl ausführen.

### <a name="office-365-retention-policies"></a>Office 365 von Aufbewahrungsrichtlinien

Führen Sie den folgenden Befehl in Security & Compliance Center PowerShell aus, um die Office 365 Aufbewahrungsrichtlinie (organisationsweit oder an einem bestimmten Speicherort) zu identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne das in Schritt 1 identifizierte MBX-, SKP-oder GfK-Präfix oder das Aktions Suffix).

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>Identifizieren von Postfächern in der Warteschleife, da eine Aufbewahrungs Bezeichnung auf einen Ordner oder ein Element angewendet wurde

Wenn ein Benutzer eine Aufbewahrungs Bezeichnung anwendet, die so konfiguriert ist, dass Inhalte beibehalten oder beibehalten und anschließend Inhalt in einem beliebigen Ordner oder Element in seinem Postfach gelöscht werden, wird die *ComplianceTagHoldApplied* -Postfacheigenschaft auf **true**festgelegt. In diesem Fall gilt das Postfach als in der Warteschleife, als ob es in einem Beweissicherungsverfahren gespeichert oder einer Office 365 Aufbewahrungsrichtlinie zugewiesen wurde. Wenn die *ComplianceTagHoldApplied* -Eigenschaft auf **true**festgelegt ist, können die folgenden Dinge auftreten:

- Wenn das Postfach oder das Office 365 Benutzerkonto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven [Postfach](inactive-mailboxes-in-office-365.md).
- Sie können das Postfach nicht deaktivieren (entweder das primäre Postfach oder das Archivpostfach, falls es aktiviert ist).
- Elemente im Postfach können länger als erwartet aufbewahrt werden. Dies liegt daran, dass das Postfach in der Warteschleife ist und daher keine Elemente endgültig gelöscht werden (bereinigt).

Um den Wert der *ComplianceTagHoldApplied* -Eigenschaft anzuzeigen, führen Sie den folgenden Befehl in Exchange Online PowerShell aus:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Weitere Informationen zu Aufbewahrungs Bezeichnungen finden Sie unter [Overview of Office 365 Retention Labels](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>Verwalten von Postfächern in Verzögerungs speichern

Nach dem Entfernen eines beliebigen haltebereichs aus einem Postfach wird der Wert der *DelayHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Dies tritt auf, wenn der Assistent für verwaltete Ordner das nächste Mal das Postfach verarbeitet und erkennt, dass ein Haltebereich entfernt wurde. Dies wird als *Verzögerungs* Speicher bezeichnet und bedeutet, dass das tatsächliche Entfernen des Haltestatus für 30 Tage verzögert wird, um zu verhindern, dass Daten endgültig aus dem Postfach gelöscht (bereinigt) werden. Dadurch erhalten Administratoren die Möglichkeit, Postfachelemente zu suchen oder wiederherzustellen, die gelöscht werden, nachdem die Aufbewahrungszeit tatsächlich entfernt wurde. Wenn ein Verzögerungs Speicher auf das Postfach gesetzt wird, wird das Postfach weiterhin für unbegrenzte Dauer aufbewahrt, als ob das Postfach ein Beweissicherungsverfahren aufweist. Nach 30 Tagen läuft die Verzögerungsdauer ab, und Office 365 versucht automatisch, die Verzögerungszeit zu entfernen (indem die *DelayHoldApplied* -Eigenschaft auf **false**festgelegt wird), damit der Haltestatus tatsächlich entfernt wird. Nachdem die *DelayHoldApplied* -Eigenschaft auf **false festgelegt**wurde, werden Elemente, die zum Entfernen markiert sind, beim nächsten verarbeiten des Postfachs vom Assistenten für verwaltete Ordner gelöscht.

Um den Wert für die *DelayHoldApplied* -Eigenschaft für ein Postfach anzuzeigen, führen Sie den folgenden Befehl in Exchange Online PowerShell aus.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Um die Verzögerung zu entfernen, bevor Sie abläuft, können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Beachten Sie, dass Ihnen die Rolle "Legal Hold" in Exchange Online zugewiesen werden muss, um den Parameter *RemoveDelayHoldApplied* verwenden zu können. 

Um die Verzögerung für ein inaktives Postfach zu entfernen, führen Sie den folgenden Befehl in Exchange Online PowerShell aus:

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> Die beste Möglichkeit zum Angeben eines inaktiven Postfachs im vorherigen Befehl ist die Verwendung des Distinguished Name oder Exchange GUID-Werts. Durch Verwenden eines dieser Werte können Sie verhindern, versehentlich das falsche Postfach anzugeben. 

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die auf ein Postfach angewendeten Haltestatus identifiziert haben, können Sie Aufgaben wie das Ändern der Aufbewahrungsdauer, vorübergehendes oder dauerhaftes Entfernen des Haltestatus oder im Fall von Office 365-Aufbewahrungsrichtlinien mit Ausnahme eines inaktiven Postfachs aus der Richtlinie ausführen. Weitere Informationen zum Durchführen von Aufgaben im Zusammenhang mit Holds finden Sie in einem der folgenden Themen:

- Führen Sie den Befehl " [Benutzer mailbox> \<festlegen-RetentionCompliancePolicy-AddExchangeLocationException](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) " in Security & Compliance Center PowerShell aus, um ein Postfach aus einer organisationsweiten Office 365 Aufbewahrungsrichtlinie auszuschließen. Beachten Sie, dass dieser Befehl nur für Aufbewahrungsrichtlinien verwendet werden kann, bei ** denen der Wert `All`für die ExchangeLocation-Eigenschaft gleich ist.

- Führen Sie in Exchange Online PowerShell den Befehl [festlegen-Mailbox-ExcludeFromOrgHolds \<Hold GUID without Prefix oder suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) aus, um ein inaktives Postfach aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie auszuschließen.

- [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

- [Löschen von Elementen im Ordner „Wiederherstellbare Elemente“ für cloudbasierte aufzubewahrende Postfächer](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)

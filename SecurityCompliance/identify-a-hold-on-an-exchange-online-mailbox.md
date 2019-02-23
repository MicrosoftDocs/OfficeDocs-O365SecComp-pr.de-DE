---
title: Identifizieren des Haltebereichs für ein Exchange Online-Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Erfahren Sie, wie Sie die verschiedenen Aufbewahrungsarten identifizieren können, die in einem Office 365-Postfach gespeichert werden dürfen. Zu diesen Aufbewahrungsarten gehört das Litigation Hold, eDiscovery Holds und Office 365 Retention Policies. Sie können auch feststellen, ob ein Benutzer von einer organisationsweiten Aufbewahrungsrichtlinie ausgeschlossen wurde.
ms.openlocfilehash: 9c286ac6303a4d1f85e94e4ae6ca2163081e51b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219105"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Identifizieren des Haltebereichs für ein Exchange Online-Postfach

In diesem Artikel wird erläutert, wie Sie die in Exchange Online-Postfächern in Office 365 enthaltenen aufbewahrungsbereiche identifizieren.

Office 365 bietet eine Reihe von Möglichkeiten, wie Sie verhindern können, dass Postfachinhalte dauerhaft gelöscht werden. Auf diese Weise kann Ihre Organisation Inhalte aufbewahren, um Compliance-Stammdaten oder für die Dauer von rechtlichen oder sonstigen Untersuchungen zu erfüllen. Hier finden Sie eine Liste der Aufbewahrungs Features (auch als halte *Status*bezeichnet) in Office 365:

- In Exchange Online werden die **Aufbewahrungsverfahren** für Benutzerpostfächer angewendet.

- **eDiscovery-halte** Status, die einem eDiscovery-Fall im Security _AMP_ Compliance Center zugeordnet sind. eDiscovery-Speicher können auf Benutzerpostfächer und auf das entsprechende Postfach für Office 365-Gruppen und Microsoft Teams angewendet werden.

- Die **in-** situ-Speicher, die auf Benutzerpostfächer angewendet werden, indem Sie das in-situ-EDiscovery-& in der Exchange-verwaltungsKonsole in Exchange Online verwenden.

- **Office 365-Aufbewahrungsrichtlinie** -behält Inhalte in Benutzerpostfächern in Exchange Online und im entsprechenden Postfach für Office 365-Gruppen und Microsoft Teams bei. Sie können eine Aufbewahrungsrichtlinie erstellen behält Skype for Business-Unterhaltungen bei, die in Benutzerpostfächern gespeichert sind.

  Es gibt zwei Arten von Office 365-Aufbewahrungsrichtlinien, die Postfächern zugewiesen werden können.

    - **Spezifische Aufbewahrungsrichtlinien für Standorte** – Dies sind Richtlinien, die den Inhaltsspeicherorten bestimmter Benutzer zugewiesen sind. Sie verwenden das Cmdlet **Get-Mailbox** in Exchange Online PowerShell, um Informationen zu Aufbewahrungsrichtlinien abzurufen, die bestimmten Postfächern zugewiesen sind.

    - **Organisationsweite Aufbewahrungsrichtlinien** -Dies sind Richtlinien, die allen Inhaltsspeicherorten in Ihrer Organisation zugewiesen sind. Verwenden Sie das Cmdlet **Get-OrganizationConfig** in Exchange Online PowerShell, um Informationen zu organisationsweiten Aufbewahrungsrichtlinien abzurufen. Weitere Informationen finden Sie im Abschnitt "Anwenden einer Aufbewahrungsrichtlinie auf eine gesamte Organisation oder einen bestimmten Standort" unter [Übersicht über Office 365-Aufbewahrungsrichtlinien](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Office 365-Aufbewahrungs Bezeichnungen** -wenn ein Benutzer eine Office 365-Aufbewahrungs Bezeichnung anwendet (eine, die so konfiguriert ist, dass Inhalte beibehalten oder beibehalten und dann Inhalt gelöscht wird), in einem *beliebigen* Ordner oder Element in Ihrem Postfach, wird ein Aufbewahrungszeitraum für das Postfach gespeichert, als ob das Postfach für die Aufbewahrung von Rechtsstreitigkeiten oder für die Zuweisung zu einer Office 365-Speicherrichtlinie. Weitere Informationen finden Sie unter [Identifizieren von Postfächern in der Warteschleife, da eine Aufbewahrungs Bezeichnung auf einen Ordner-oder Element](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) Abschnitt in diesem Artikel angewendet wurde.

um die aufbewahrungszeit von postfächern zu verwalten, müssen sie möglicherweise den aufbewahrungs für ein postfach ermitteln, sodass sie aufgaben wie das ändern der haltedauer, vorübergehendes oder dauerhaftes entfernen des haltebereichs oder das ausschließen eines postfachs aus einer Office 365-speicherrichtlinie ausführen können. In diesen Fällen müssen Sie zunächst den Aufbewahrungs des Postfachs identifizieren. Und da mehrere haltebereiche (und unterschiedliche Aufbewahrungs Typen) für ein einzelnes Postfach gespeichert werden können, müssen Sie alle für ein Postfach festgelegten haltebereiche identifizieren, wenn Sie diese Sperren entfernen oder ändern möchten.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Schritt 1: Abrufen der GUID für haltebereiche, die in einem Postfach gespeichert sind

Sie können die folgenden beiden Cmdlets in Exchange Online PowerShell ausführen, um die GUID der haltebereiche abzurufen, die in einem Postfach gespeichert werden. Nachdem Sie eine GUID abgerufen haben, verwenden Sie diese, um den jeweiligen Haltebereich in Schritt 2 zu identifizieren. Beachten Sie, dass die Beweissicherung nicht durch eine GUID gekennzeichnet wird. Rechtsstreitigkeiten sind für ein Postfach aktiviert oder deaktiviert.

- **Get-Mailbox** -verwenden Sie dieses Cmdlet, um zu bestimmen, ob die Beweissicherung für ein Postfach aktiviert ist, und um die GUIDs für eDiscovery Holds, in-situ-Speicher und Office 365-Aufbewahrungsrichtlinien abzurufen, die speziell einem Postfach zugeordnet sind. Die Ausgabe dieses Cmdlets gibt auch an, ob ein Postfach explizit aus einer organisationsweiten Aufbewahrungsrichtlinie ausgeschlossen wurde.

- **Get-OrganizationConfig** -verwenden Sie dieses Cmdlet, um die GUIDs für organisationsweite Aufbewahrungsrichtlinien abzurufen.

Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Führen Sie den folgenden Befehl aus, um Informationen zu den Haltebereichen und Office 365-Aufbewahrungsrichtlinien für ein Postfach abzurufen.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Wenn die InPlaceHolds-Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den Befehl ausführen, um `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` die einzelnen GUIDs in einer separaten Zeile anzuzeigen.

In der folgenden Tabelle wird beschrieben, wie Sie unterschiedliche Aufbewahrungs Typen basierend auf den Werten in der *InPlaceHolds* -Eigenschaft identifizieren, wenn Sie das Cmdlet **Get-Mailbox** ausführen.


|Haltebereichstyp  |Beispielwert  |So identifizieren Sie den Haltestatus  |
|---------|---------|---------|
|Beweissicherungsverfahren     |    `True`     |     Die Beweissicherung für ein Postfach ist aktiviert, wenn die *LitigationHoldEnabled* -Eigenschaft `True`auf festgelegt ist.    |
|eDiscovery-Haltebereich     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   Die *InPlaceHolds-Eigenschaft* enthält die GUID eines beliebigen haltebereichs, der einem eDiscovery-Fall im Security _AMP_ Compliance Center zugeordnet ist. Sie können feststellen, dass dies ein eDiscovery-Speicher ist, da `UniH` die GUID mit dem Präfix beginnt (das einen einheitlichen Haltebereich bezeichnet).      |
|Compliance-Archiv     |     `c0ba3ce811b6432a8751430937152491` <br/> oder <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     Die *InPlaceHolds* -Eigenschaft enthält die GUID des in-situ-Speichers, der für das Postfach platziert wird. Sie können feststellen, dass es sich um einen in-situ-Speicher handelt, da die GUID entweder nicht mit einem `cld` Präfix beginnt oder mit dem Präfix startet.     |
|Speziell auf das Postfach angewendete Aufbewahrungsrichtlinie für Office 365     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> oder <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     Die InPlaceHolds-Eigenschaft enthält GUIDs einer bestimmten Aufbewahrungsrichtlinie für Standorte, die auf das Postfach angewendet wird. Sie können Aufbewahrungsrichtlinien identifizieren, da die GUID mit `mbx` dem oder `skp` dem Präfix beginnt. Das `skp` Präfix gibt an, dass die Aufbewahrungsrichtlinie auf Skype for Business-Unterhaltungen im Postfach des Benutzers angewendet wird.    |
|Ausgeschlossen von einer organisationsweiten Office 365-Aufbewahrungsrichtlinie     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Wenn ein Postfach aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie ausgeschlossen ist, wird die GUID für die Aufbewahrungsrichtlinie, von der das Postfach ausgeschlossen wird, in der InPlaceHolds-Eigenschaft `-mbx` angezeigt und durch das Präfix gekennzeichnet.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Wenn die *InPlaceHolds* -Eigenschaft beim Ausführen des Cmdlets **Get-Mailbox** leer ist, kann weiterhin eine oder mehrere organisationsweite Office 365-Aufbewahrungsrichtlinien auf das Postfach angewendet werden. Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Liste der GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Wenn die InPlaceHolds-Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den Befehl ausführen, um `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` die einzelnen GUIDs in einer separaten Zeile anzuzeigen.

In der folgenden Tabelle werden die unterschiedlichen organisationsweiten Aufbewahrungsarten und die Identifizierung der einzelnen Typen anhand der GUIDs beschrieben, die in der *InPlaceHolds* -Eigenschaft enthalten sind, wenn Sie das Cmdlet **Get-OrganizationConfig** ausführen.


|Haltebereichstyp  |Beispielwert  |Description  |
|---------|---------|---------|
|Office 365-Aufbewahrungsrichtlinien, die auf Exchange-Postfächer, öffentliche Exchange-Ordner und Teams-Chats angewendet werden    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer, öffentliche Exchange-Ordner und 1xN-Chats in Microsoft Teams angewendet werden, werden durch `mbx` GUIDs identifiziert, die mit dem Präfix beginnen. Beachten Sie, dass 1xN-Chats im Postfach der einzelnen Chat Teilnehmer gespeichert werden.      |
|Office 365-Aufbewahrungsrichtlinie, die auf Office 365-Gruppen und Teams-Kanal Nachrichten angewendet wird     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Organisationsweite Aufbewahrungsrichtlinien, die auf Office 365-Gruppen und Kanal Nachrichten in Microsoft Teams angewendet werden, werden durch GUIDs `grp` identifiziert, die mit dem Präfix beginnen. Beachten Sie, dass Kanal Nachrichten im Gruppenpostfach gespeichert sind, das einem Microsoft-Team zugeordnet ist.     |

Weitere Informationen zu Aufbewahrungsrichtlinien für Microsoft Teams finden Sie im Abschnitt "Standort Teams" im [Überblick über Aufbewahrungsrichtlinien](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Grundlegendes zum Format des InPlaceHolds-Werts für Aufbewahrungsrichtlinien

Zusätzlich zum Präfix (MBX, SKP oder GRP), das ein Element in der InPlaceHolds-Eigenschaft als Office 365-Aufbewahrungsrichtlinie identifiziert, enthält der Wert auch ein Suffix, das den Typ der Aufbewahrungsaktion identifiziert, die für die Richtlinie konfiguriert ist. Das Aktion-Suffix wird beispielsweise in den folgenden Beispielen fett hervorgehoben:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

In der folgenden Tabelle sind die drei möglichen Aufbewahrungsaktionen definiert:

|Wert  |Beschreibung  |
|---------|---------|
|**1**     | Gibt an, dass die Aufbewahrungsrichtlinie zum Löschen von Elementen konfiguriert ist; die Richtlinie behält keine Elemente bei.        |
|**2**    |    Gibt an, dass die Aufbewahrungsrichtlinie so konfiguriert ist, dass Elemente aufbewahrt werden. die Richtlinie löscht keine Elemente nach Ablauf des Aufbewahrungszeitraums.     |
|**3**     |   Gibt an, dass die Aufbewahrungsrichtlinie so konfiguriert ist, dass Elemente aufbewahrt und nach Ablauf des Aufbewahrungszeitraums gelöscht werden.      |

Weitere Informationen zu Aufbewahrungsaktionen finden Sie im Abschnitt "Beibehaltung von Inhalten für einen bestimmten Zeitraum" unter Übersicht über [Aufbewahrungsrichtlinien](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Schritt 2: Verwenden der GUID zum Identifizieren des haltebereichs

Nachdem Sie die GUID für einen Haltebereich abgerufen haben, der auf ein Postfach angewendet wird, besteht der nächste Schritt darin, die GUID zu verwenden, um den Haltestatus zu identifizieren. In den folgenden Abschnitten wird gezeigt, wie der Name des haltebereichs (und andere Informationen) mithilfe der Hold-GUID identifiziert wird.

### <a name="ediscovery-holds"></a>eDiscovery-Aufbewahrung

Führen Sie die folgenden Befehle in Security & Compliance Center PowerShell aus, um einen eDiscovery-Speicher zu identifizieren, der auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne UniH-Präfix) für den eDiscovery-Speicher, den Sie in Schritt 1 identifiziert haben. Der erste Befehl erstellt eine Variable, die Informationen über den Haltebereich enthält; Diese Variable wird in den anderen Befehlen verwendet. Der zweite Befehl zeigt den Namen des eDiscovery-Falls an, dem der Haltebereich zugeordnet ist. Der dritte Befehl zeigt den Haltestatus und eine Liste der Postfächer an, auf die der Haltebereich angewendet wird.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Informationen zum Herstellen einer Verbindung mit der Security & Compliance Center-PowerShell finden Sie unter [Connect to Office 365 Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>In-Situ-Speicher

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den in-situ-Speicher zu identifizieren, der auf das Postfach angewendet wird. Verwenden Sie die GUID für den in-situ-Speicher, den Sie in Schritt 1 identifiziert haben. Der Befehl zeigt den Haltestatus und eine Liste der Postfächer an, auf die der Haltebereich angewendet wird.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Beachten Sie Folgendes: Wenn die GUID für den in-situ-Speicher `cld` mit dem Präfix beginnt, achten Sie darauf, das Präfix beim Ausführen des vorherigen Befehls einzuschließen.

### <a name="office-365-retention-policies"></a>Office 365-Aufbewahrungsrichtlinien

Führen Sie den folgenden Befehl in Security & Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie (organisationsweit oder spezifischer Speicherort) zu identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne das MBX-, SKP-oder GRP-Präfix oder das Aktions Suffix), die Sie in Schritt 1 identifiziert haben.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>Identifizieren von Postfächern in der Warteschleife, da eine Aufbewahrungs Bezeichnung auf einen Ordner oder ein Element angewendet wurde

Wenn ein Benutzer eine Aufbewahrungs Bezeichnung anwendet, die so konfiguriert ist, dass Inhalte beibehalten oder beibehalten und dann Inhalt in einem beliebigen Ordner oder Element in Ihrem Postfach gelöscht wird, wird die *ComplianceTagHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Wenn dies der Fall ist, wird das Postfach als in der Warteschleife gehalten, so als ob es in einem Rechtsstreit gehalten oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde. Wenn die *ComplianceTagHoldApplied* -Eigenschaft auf **true**festgelegt ist, können die folgenden Dinge auftreten:

- Wenn das Postfach oder das Office 365-Benutzerkonto des Benutzers gelöscht wird, wird das Postfach zu einem inaktiven [Postfach](inactive-mailboxes-in-office-365.md).
- Sie können das Postfach nicht deaktivieren (entweder das primäre Postfach oder das Archivpostfach, falls es aktiviert ist).
- Elemente im Postfach können länger aufbewahrt werden als erwartet. Der Grund ist, dass das Postfach in der Warteschleife gespeichert wird und daher keine Elemente endgültig gelöscht werden.

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Wert der *ComplianceTagHoldApplied* -Eigenschaft anzuzeigen:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Weitere Informationen zu Aufbewahrungs Bezeichnungen finden Sie unter [Overview of Office 365 Retention Labels](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>Verwalten von Postfächern bei verzögerter Aufbewahrung

Nachdem ein Aufbewahrungs aus einem Postfach entfernt wurde, wird der Wert der *DelayHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Dies tritt auf, wenn der Assistent für verwaltete Ordner das nächste Mal das Postfach verarbeitet und erkennt, dass ein Haltebereich entfernt wurde. Dies wird als *Verzögerungs Sperre* bezeichnet und bedeutet, dass das tatsächliche Entfernen des Haltestatus für 30 Tage verzögert wird, um zu verhindern, dass Daten dauerhaft aus dem Postfach gelöscht werden. Dies gibt Administratoren die Möglichkeit, nach Postfachelementen zu suchen oder wiederherzustellen, die gelöscht werden, nachdem der Haltebereich tatsächlich entfernt wurde. Wenn ein Verzögerungs Speicher für das Postfach gespeichert wird, wird das Postfach für eine unbegrenzte Dauer nach wie vor als für das Postfach aktiviert gehalten. Nach 30 Tagen wird die Verzögerungsdauer abgelaufen, und Office 365 versucht automatisch, die Verzögerungsdauer zu entfernen (indem Sie die *DelayHoldApplied* -Eigenschaft auf **false**festlegen), sodass der Haltestatus tatsächlich entfernt wird. Nachdem die *DelayHoldApplied* -Eigenschaft auf **false festgelegt**wurde, werden Elemente, die zum Entfernen markiert sind, beim nächsten verarbeiten des Postfachs vom Assistenten für verwaltete Ordner gelöscht.

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Wert für die *DelayHoldApplied* -Eigenschaft für ein Postfach anzuzeigen.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Um die Verzögerungsdauer zu entfernen, bevor Sie abläuft, können Sie den folgenden Befehl in Exchange Online PowerShell ausführen: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Beachten Sie, dass Sie in Exchange Online die Rolle "Gesetzliche Aufbewahrungspflicht" für die Verwendung des Parameters *RemoveDelayHoldApplied* 

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um die Verzögerungsdauer für ein inaktives Postfach zu entfernen:

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> Die beste Möglichkeit zum Angeben eines inaktiven Postfachs im vorherigen Befehl besteht darin, den Distinguished Name oder den Exchange-GUID-Wert zu verwenden. Die Verwendung eines dieser Werte verhindert das versehentliche angeben des falschen Postfachs. 

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die haltebereiche identifiziert haben, die auf ein Postfach angewendet werden, können Sie Aufgaben wie das Ändern der Aufbewahrungsdauer, das vorübergehende oder dauerhafte Entfernen des Speichers, oder im Fall von Office 365-Archivierungsrichtlinien, die ein inaktives Postfach aus der Richtlinie ausschließen, ausführen. Weitere Informationen zum Ausführen von Aufgaben im Zusammenhang mit Haltebereichen finden Sie in den folgenden Themen:

- Führen Sie den Befehl [Set-RetentionCompliancePolicy \<-AddExchangeLocationException User Mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) in Security & Compliance Center PowerShell aus, um ein Postfach aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie auszuschließen. Beachten Sie, dass dieser Befehl nur für Aufbewahrungsrichtlinien verwendet werden kann, bei ** denen der Wert `All`für die ExchangeLocation-Eigenschaft gleich ist.

- Führen Sie die Anweisung [Set-Mailbox \<-ExcludeFromOrgHolds Hold GUID without Prefix oder Suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) in Exchange Online PowerShell aus, um ein inaktives Postfach aus einer organisationsweiten Office 365-Aufbewahrungsrichtlinie auszuschließen.

- [Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Löschen eines inaktiven Postfachs in Office 365](delete-an-inactive-mailbox.md)

- [Löschen von Elementen im Ordner „Wiederherstellbare Elemente“ für cloudbasierte aufzubewahrende Postfächer](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)

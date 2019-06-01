---
title: Attribute für Richtlinien für Informationsbarrieren
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
description: Verwenden Sie diesen Artikel als Referenz für verschiedene Attribute, die Sie in Richtlinien für Informationsbarrieren verwenden können.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668304"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Attribute für Richtlinien für Informationsbarrieren (Vorschau)

Bestimmte Attribute in Azure Active Directory können verwendet werden, um Benutzer zu segmentieren. Segmente werden dann als Filter für Richtlinien für Informationsbarrieren verwendet. Beispielsweise können Sie mithilfe von **Department** Segmente von Benutzern nach Abteilung in Ihrer Organisation definieren (sofern kein einzelner Mitarbeiter gleichzeitig für zwei Abteilungen arbeitet). 

Dieser Artikel enthält eine Liste der Attribute, die verwendet werden können. Wenn Sie mehr über Informationsbarrieren erfahren möchten, lesen Sie die folgenden Ressourcen:
- [Informationsbarrieren (Vorschau)](information-barriers.md)
- [Definieren von Richtlinien für Informationsbarrieren in Microsoft Teams (Vorschau)](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Verwenden von Attributen in Richtlinien für Informationsbarrieren

Die in diesem Artikel aufgeführten Attribute können zum Definieren (oder bearbeiten) von Segmenten von Benutzern verwendet werden. Segmente werden als Parameter (UserGroupFilter) in Richtlinien für Informationsbarrieren verwendet, wie in den folgenden Beispielen dargestellt:

|Beispiel  |Cmdlet  |
|---------|---------|
|Definieren eines Segments namens Segment1 mit dem Department-Attribut     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|Definieren Sie ein Segment, das als segmenta bezeichnet wird, indem Sie das Attribut "Attributs" verwenden (angenommen, dieses Attribut enthält Gruppennamen, beispielsweise "bluegroup").     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|Definieren Sie ein Segment namens Daytrader mit ExtensionAttribute1 (angenommen, dieses Attribut enthält Auftragstitel wie "Daytrader").|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

Wenn Sie Segmente definieren, verwenden Sie für alle Segmente dasselbe Attribut. Wenn Sie beispielsweise einige Segmente mithilfe von *Department*definieren, definieren Sie alle Segmente mithilfe von *Department*. Definieren Sie einige Segmente nicht mithilfe von *Department* und ** anderen mithilfe von "Redefine". Stellen Sie sicher, dass sich Ihre Segmente nicht überschneiden. Jeder Benutzer sollte genau einem Segment zugeordnet werden. 

Weitere Informationen finden Sie unter [define Segments using PowerShell](information-barriers-policies.md#define-segments-using-powershell).

## <a name="reference"></a>Referenz

In der folgenden Tabelle sind die Attribute aufgeführt, die Sie mit Informationsbarrieren verwenden können.

|Azure Active Directory Eigenschaften Name (LDAP-Anzeigename)  |Exchange-Eigenschaftsname  |
|---------|---------|
|Gemeinsame Dokument       | Gemeinsame Dokument        |
|Company     |Company         |
|Abteilung     |Abteilung         |
|ExtensionAttribute1 |CustomAttribute1  |
|ExtensionAttribute2 |CustomAttribute2  |
|ExtensionAttribute3 |CustomAttribute3  |
|ExtensionAttribute4 |Parameter CustomAttribute4  |
|ExtensionAttribute5 |Eigenschaft CustomAttribute5  |
|ExtensionAttribute6 |CustomAttribute6  |
|ExtensionAttribute7 |CustomAttribute7  |
|ExtensionAttribute8 |CustomAttribute8  |
|ExtensionAttribute9 |CustomAttribute9  |
|ExtensionAttribute10 |CustomAttribute10  |
|ExtensionAttribute11 |CustomAttribute11  |
|ExtensionAttribute12 |CustomAttribute12  |
|ExtensionAttribute13 |CustomAttribute13  |
|ExtensionAttribute14 |CustomAttribute14  |
|ExtensionAttribute15 |CustomAttribute15  |
|MSExchExtensionCustomAttribute1 |ExtensionCustomAttribute1 |
|MSExchExtensionCustomAttribute2 |ExtensionCustomAttribute2 |
|MSExchExtensionCustomAttribute3 |ExtensionCustomAttribute3 |
|MSExchExtensionCustomAttribute4 |ExtensionCustomAttribute4 |
|MSExchExtensionCustomAttribute5 |ExtensionCustomAttribute5 |
|MailNickname |Alias |
|PhysicalDeliveryOfficeName |Office |
|PostalCode |PostalCode |
|ProxyAddresses |EmailAddresses |
|StreetAddress |StreetAddress |
|TargetAddress |ExternalEmailAddress |
|UsageLocation |UsageLocation |
|UserPrincipalName  |UserPrincipalName  |
|E-Mail   |WindowsEmailAddress    |
|Beschreibung    |Beschreibung    |
|MemberOf   |MemberOfGroup  |

## <a name="related-topics"></a>Verwandte Themen

[Definieren von Richtlinien für Informationsbarrieren in Microsoft Teams (Vorschau)](information-barriers-policies.md)

[Problembehandlung bei Informationsbarrieren (Vorschau)](information-barriers-troubleshooting.md)

[Informationsbarrieren (Vorschau)](information-barriers.md)




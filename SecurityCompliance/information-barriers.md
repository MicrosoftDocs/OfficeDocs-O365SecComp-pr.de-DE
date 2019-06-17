---
title: Übersicht über Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Verwenden Sie Informationsbarrieren, um die Kommunikation mit Microsoft Teams in Ihrer Organisation sicherzustellen.
ms.openlocfilehash: a2c202d08f1de60f92f13b2ac4c2b9d3c7f900e8
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935937"
---
# <a name="information-barriers-preview"></a>Informationsbarrieren (Vorschau)

## <a name="overview"></a>Übersicht

Microsoft Cloud Services umfassen leistungsstarke Funktionen für Kommunikation und Zusammenarbeit. Angenommen, Sie möchten die Kommunikation zwischen zwei Gruppen einschränken, um zu verhindern, dass in Ihrer Organisation ein Interessenkonflikt auftritt. Oder Sie möchten möglicherweise die Kommunikation zwischen bestimmten Personen innerhalb Ihrer Organisation einschränken, um interne Informationen zu schützen. Microsoft 365 ermöglicht die Kommunikation und Zusammenarbeit zwischen Gruppen und Organisationen, gibt es also eine Möglichkeit, die Kommunikation zwischen bestimmten Benutzergruppen einzuschränken, wenn dies erforderlich ist? Mit Informationsbarrieren, können Sie! 

Informationsbarrieren befinden sich jetzt in der Vorschau, beginnend mit Microsoft Teams. Wenn diese Features für Ihre Organisation verfügbar sind, kann ein Administrator für Compliance-oder Informationsbarrieren Richtlinien definieren, um die Kommunikation zwischen Benutzergruppen in Microsoft Teams zuzulassen oder zu verhindern. Richtlinien für Informationsbarrieren können für Situationen wie diese verwendet werden:

- Ein Day Trader kann keine Person im Marketing Team anrufen
- Finanz Personal, das an vertraulichen Unternehmensinformationen arbeitet, kann keine Anrufe von bestimmten Gruppen innerhalb Ihrer Organisation empfangen.
- Ein internes Team mit Geschäfts geheimem Material kann nicht online mit Personen in bestimmten Gruppen innerhalb Ihrer Organisation anrufen oder chatten.
- Ein Forschungsteam kann nur online mit einem Produktentwicklungsteam anrufen oder chatten

Für alle diese Beispielszenarien (und mehr) können Richtlinien für Informationsbarrieren definiert werden, um die Kommunikation in Microsoft Teams zu verhindern oder zuzulassen. Mithilfe solcher Richtlinien kann verhindert werden, dass Personen Anrufe oder Chats mit Personen durchlaufen, die Sie nicht haben sollten, oder dass Personen nur mit bestimmten Gruppen in Microsoft Teams kommunizieren können. Wenn die Richtlinien für Informationsbarrieren wirksam sind und Benutzer, die von diesen Richtlinien abgedeckt werden, versuchen, mit anderen Personen in Microsoft Teams zu kommunizieren, werden Überprüfungen durchgeführt, um die Kommunikation zu verhindern (oder zulassen) (gemäß den Richtlinien für Informationsbarrieren). Weitere Informationen zur Benutzererfahrung mit Informationsbarrieren finden Sie unter [Information Barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

> [!NOTE]
> Informationsbarrieren gelten nicht für e-Mail-Kommunikationen oder für die Dateifreigabe über SharePoint Online oder OneDrive.

## <a name="required-licenses-and-permissions"></a>Erforderliche Lizenzen und Berechtigungen

**Derzeit befindet sich das Feature "Informations Barriere" in privater Vorschau**. Wenn diese Features allgemein verfügbar sind, werden Sie in Abonnements eingeschlossen, beispielsweise:

- Microsoft 365 E5
- Office 365 E5
- Office 365 Erweiterte Compliance
- Microsoft 365 E5 – Informationsschutz und Compliance

Weitere Informationen finden Sie unter [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).

Um [Richtlinien für Informationsbarrieren zu definieren oder zu bearbeiten](information-barriers-policies.md), muss Ihnen eine der folgenden Rollen zugewiesen sein:

- Microsoft 365 globaler Administrator
- Globaler Office 365-Administrator\ 
- Compliance-Administrator
- Administrator für Informationsbarrieren

Sie müssen mit PowerShell-Cmdlets vertraut sein, um Richtlinien für Informationsbarrieren zu definieren, zu validieren oder zu bearbeiten. Obwohl in den [Gewusst-wie-Informationen](information-barriers-policies.md)mehrere Beispiele für PowerShell-Cmdlets bereitgestellt werden, müssen Sie zusätzliche Details wie Parameter für Ihre Organisation kennen.

## <a name="next-steps"></a>Nächste Schritte

- [Weitere Informationen zu Informationsbarrieren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [Siehe die Attribute, die für Richtlinien für Informationsbarrieren verwendet werden können.](information-barriers-attributes.md)
- [Definieren von Richtlinien für Informationsbarrieren](information-barriers-policies.md) 


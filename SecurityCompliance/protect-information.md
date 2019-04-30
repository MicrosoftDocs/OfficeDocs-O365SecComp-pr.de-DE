---
title: Schützen von Informationen
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/26/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Zielseite zum Schutz von Informationen
ms.openlocfilehash: 1c673c2417b399c57ca7ac7e5c5a7b7351de1edd
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473094"
---
# <a name="protect-information"></a>Schützen von Informationen

Microsoft 365 und Office 365 bieten Funktionen, die auf bestimmte Typen von Daten angewendet werden können, um Informationen zu schützen. 


|**Funktion**|**Weitere Informationen**|
|:-----|:-----|
|[Vertraulichkeitsbezeichnungen](sensitivity-labels.md) <br/> |Mithilfe von Vertraulichkeits Bezeichnungen können Sie Ihre vertraulichen Inhalte klassifizieren und schützen. Schutzoptionen sind Beschriftungen, Wasserzeichen und Verschlüsselung. Vertraulichkeits Bezeichnungen verwenden Azure Information Protection. Wenn Sie Azure Information Protection-Bezeichnungen verwenden, wird im Moment empfohlen, keine neuen Beschriftungen in anderen Verwaltungs Centern zu erstellen, bis Sie die Migration abgeschlossen haben. Siehe [Azure Information Protection Migration](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> [Aufbewahrungs Beschriftungen](retention-policies.md) unterscheiden sich von den Vertraulichkeits Bezeichnungen. Aufbewahrungs Bezeichnungen helfen Ihnen dabei, Inhalte basierend auf von Ihnen definierten Richtlinien beizubehalten oder zu löschen. Diese Hilfe Organisationen erfüllen Branchenvorschriften und interne Richtlinien.|
|Verhinderung von [Datenverlust](data-loss-prevention-policies.md) DLP  <br/> |Mit DLP-Richtlinien können Sie vertrauliche Informationen in Office 365 identifizieren, überwachen und automatisch schützen. Richtlinien zur Verhinderung von Datenverlust können Vertraulichkeits Bezeichnungen und vertrauliche Informationstypen verwenden, um vertrauliche Informationen zu identifizieren. <br/> |
|[Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md)  <br/> |DLP enthält viele Arten von vertraulichen Informationen, die Sie in DLP-Richtlinien verwenden können. Arten von vertraulichen Informationen definieren, wie der automatisierte Prozess bestimmte Informationstypen wie Integritätsdienst Nummern und Kreditkartennummern erkennt.   <br/> |
|[Office 365-Nachrichtenverschlüsselung](ome.md) Ome  <br/> |Mit der Office 365-Nachrichtenverschlüsselung kann Ihre Organisation verschlüsselte e-Mail-Nachrichten zwischen Personen innerhalb und außerhalb Ihrer Organisation senden und empfangen. Die Office 365-Nachrichtenverschlüsselung funktioniert mit Outlook.com, Yahoo!, Gmail und anderen e-Mail-Diensten. Die Verschlüsselung von e-Mail-Nachrichten trägt dazu bei, dass nur vorgesehene Empfänger Nachrichteninhalte anzeigen können.  <br/> |
|[Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Wenn Sie Vertraulichkeits Bezeichnungen oder Office-Nachrichtenverschlüsselung verwenden, verwenden Sie bereits Azure Information Protection. Wenn Sie Azure Information Protection-Bezeichnungen noch nicht in Office 365 migriert haben, können Sie diese in Azure Information Protection weiterhin verwalten.  <br/>Der [Azure Information Protection-Scanner](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) kann lokal ausgeführt werden, um Dateien auf Windows Server-, Netzwerkfreigabe-und SharePoint Server-Websites und-Bibliotheken zu klassifizieren und zu schützen. Dies kann ein erster Schritt zur Identifizierung von Daten für die Migration zu Office 365 sein.
|Azure Information Protection mit BYOK-oder HYOK-Lösungen <br/> |Einige Organisationen verfügen über eine Geschäftsanforderung oder Compliance-Anforderungen, um die Kontrolle über einen Verschlüsselungs-Schlüssel vor Ort oder in der Cloud beizubehalten. Dies ist jedoch nicht die Regel. Weitere Informationen finden Sie unter [halten Sie Ihren eigenen Schlüssel (Hyok) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions) , und [bringen Sie Ihren eigenen Schlüssel (BYOK) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). <br/> |
    


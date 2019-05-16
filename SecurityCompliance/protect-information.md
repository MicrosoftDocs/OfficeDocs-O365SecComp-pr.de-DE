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
ms.openlocfilehash: 696684778604f4259166bdc3059944285833cba1
ms.sourcegitcommit: 4eb4ca899adcf4d86501530f875eb49af8cdaeb7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2019
ms.locfileid: "34083178"
---
# <a name="protect-information"></a>Schützen von Informationen

Microsoft 365 und Office 365 bieten Funktionen, die auf bestimmte Typen von Daten angewendet werden können, um Informationen zu schützen.


|**Funktion**|**Weitere Informationen**|
|:-----|:-----|
|[Vertraulichkeitsbezeichnungen](sensitivity-labels.md) <br/> |Mithilfe von Vertraulichkeits Bezeichnungen können Sie Ihre vertraulichen Inhalte klassifizieren und schützen. Schutzoptionen sind Beschriftungen, Wasserzeichen und Verschlüsselung. Vertraulichkeits Bezeichnungen verwenden Azure Information Protection. Wenn Sie Azure Information Protection-Bezeichnungen verwenden, wird im Moment empfohlen, keine neuen Beschriftungen in anderen Verwaltungs Centern zu erstellen, bis Sie die Migration abgeschlossen haben. Siehe [Azure Information Protection Migration](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> [Aufbewahrungs Beschriftungen](retention-policies.md) unterscheiden sich von den Vertraulichkeits Bezeichnungen. Aufbewahrungs Bezeichnungen helfen Ihnen dabei, Inhalte basierend auf von Ihnen definierten Richtlinien beizubehalten oder zu löschen. Diese Hilfe Organisationen erfüllen Branchenvorschriften und interne Richtlinien.|
|Verhinderung von [Datenverlust](data-loss-prevention-policies.md) DLP  <br/> |Mit DLP-Richtlinien können Sie vertrauliche Informationen in Office 365 identifizieren, überwachen und automatisch schützen. Richtlinien zur Verhinderung von Datenverlust können Vertraulichkeits Bezeichnungen und vertrauliche Informationstypen verwenden, um vertrauliche Informationen zu identifizieren. <br/> |
|[Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md) <br/> |Microsoft 365 enthält viele Arten von vertraulichen Informationen, die für die Verwendung in DLP-Richtlinien und für die automatische Klassifizierung mit Vertraulichkeits-und Aufbewahrungs Bezeichnungen bereit stehen. Vertrauliche Informationstypen können auch mit dem [Azure Information Protection-Scanner](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) verwendet werden, um Dateien in lokalen zu klassifizieren und zu schützen. Arten von vertraulichen Informationen definieren, wie der automatisierte Prozess bestimmte Informationstypen wie Integritätsdienst Nummern und Kreditkartennummern erkennt.   <br/> |
|[Office 365-Nachrichtenverschlüsselung](ome.md) Ome  <br/> |Mit der Office 365-Nachrichtenverschlüsselung kann Ihre Organisation verschlüsselte e-Mail-Nachrichten zwischen Personen innerhalb und außerhalb Ihrer Organisation senden und empfangen. Die Office 365-Nachrichtenverschlüsselung funktioniert mit Outlook.com, Yahoo!, Gmail und anderen e-Mail-Diensten. Die Verschlüsselung von e-Mail-Nachrichten trägt dazu bei, dass nur vorgesehene Empfänger Nachrichteninhalte anzeigen können. <br/> |
|[Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Azure Information Protection (manchmal auch als AIP bezeichnet) hilft einer Organisation, Dokumente und e-Mails zu klassifizieren, zu bezeichnen und optional zu schützen. Administratoren können Bezeichnungen automatisch anwenden, indem Sie Regeln und Bedingungen definieren. Benutzer können Bezeichnungen manuell auf Dateien und e-Mails anwenden. Sie können auch Empfehlungen für Benutzer geben, wann Beschriftungen angewendet werden sollen.<br/> Wenn Sie Vertraulichkeits Bezeichnungen oder Office-Nachrichtenverschlüsselung verwenden, verwenden Sie bereits Klassifizierungs-und Schutzfunktionen. Wenn Sie Azure Information Protection-Bezeichnungen noch nicht in Office 365 migriert haben, können Sie diese in Azure Information Protection weiter verwalten.  <br/>Sie können den [Azure Information Protection-Scanner](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) vor Ort ausführen, um Dateien auf Windows Server-, Netzwerkfreigabe-und SharePoint Server-Websites und-Bibliotheken zu klassifizieren und zu schützen. Dies kann ein erster Schritt zur Identifizierung von Daten für die Migration zu Office 365 sein.
|Azure Information Protection mit vom Kunden verwalteten Verschlüsselungsschlüssel <br/> |Einige Organisationen verfügen über eine Geschäftsanforderung oder Compliance-Anforderungen, um die Kontrolle über einen Verschlüsselungsschlüssel beizubehalten. Dies ist jedoch nicht die Regel. Mit Azure Information Protection können Organisationen ihren eigenen Schlüssel (BYOK) in den Dienst einbinden. Weitere Informationen finden Sie unter [bringen Sie Ihren eigenen Schlüssel (BYOK) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). Eine weitere komplexere Option wird für Kunden angeboten, die eine Anforderung haben, einen Verschlüsselungsschlüssel auf dem lokalen Speicherplatz beizubehalten, der als eigene Schlüssel (Hyok) bezeichnet wird.  Weitere Informationen finden Sie unter [halten Sie Ihren eigenen Schlüssel (Hyok) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions). <br/> |
    


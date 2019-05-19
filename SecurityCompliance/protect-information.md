---
title: Schützen von Informationen
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/26/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Ziel Seite zum Schutz von Informationen
ms.openlocfilehash: 77b4332ae4c5450f7464af660e3cda82ddbe18a5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157237"
---
# <a name="protect-information"></a>Schützen von Informationen

Microsoft 365 und Office 365 umfassen Funktionen, die auf bestimmte Datentypen angewendet werden können, um Informationen zu schützen.


|**Funktion**|**Weitere Informationen**|
|:-----|:-----|
|[Vertraulichkeitsbezeichnungen](sensitivity-labels.md) <br/> |Mit Sensitivitäts Bezeichnungen können Sie klassifizieren und zum Schutz Ihrer vertraulichen Inhalte beitragen. Zu den Schutzoptionen gehören Beschriftungen, Wasserzeichen und Verschlüsselung. Vertraulichkeits Bezeichnungen verwenden Azure Information Protection. Wenn Sie Azure Information Protection-Bezeichnungen verwenden, sollten Sie erst nach Abschluss der Migration die Erstellung neuer Bezeichnungen in anderen Verwaltungs Centern vermeiden. Siehe [Azure Information Protection Migration](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> [Aufbewahrungs Bezeichnungen](retention-policies.md) unterscheiden sich von den Vertraulichkeits Bezeichnungen. Aufbewahrungs Bezeichnungen helfen Ihnen, Inhalte auf der Grundlage von von Ihnen definierten Richtlinien beizubehalten oder zu löschen. Diese unterstützen Organisationen bei der Einhaltung von Branchenvorschriften und internen Richtlinien.|
|Verhinderung von [Datenverlust](data-loss-prevention-policies.md) DLP  <br/> |Mit DLP-Richtlinien können Sie vertrauliche Informationen über Office 365 identifizieren, überwachen und automatisch schützen. Policies zur Verhinderung von Datenverlusten können Vertraulichkeits Bezeichnungen und Typen vertraulicher Informationen verwenden, um vertrauliche Informationen zu identifizieren. <br/> |
|[Typen vertraulicher Informationen](what-the-sensitive-information-types-look-for.md) <br/> |Microsoft 365 enthält zahlreiche vertrauliche Informationstypen, die Sie in DLP-Richtlinien und für die automatische Klassifizierung mit Sensitivitäts-und Aufbewahrungs Bezeichnungen verwenden können. Vertrauliche Informationstypen können auch mit dem [Azure Information Protection-Scanner](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) verwendet werden, um Dateien lokal zu klassifizieren und zu schützen. Typen vertraulicher Informationen definieren, wie der automatisierte Prozess bestimmte Informationstypen wie Integritätsdienst Nummern und Kreditkartennummern erkennt.   <br/> |
|[Office 365 Nachrichtenverschlüsselung](ome.md) Ome  <br/> |Mit Office 365 Nachrichtenverschlüsselung kann Ihre Organisation verschlüsselte e-Mail-Nachrichten zwischen Personen innerhalb und außerhalb Ihrer Organisation senden und empfangen. Office 365 Nachrichtenverschlüsselung funktioniert mit Outlook.com, Yahoo!, Gmail und anderen e-Mail-Diensten. Die e-Mail-Nachrichtenverschlüsselung hilft sicherzustellen, dass nur vorgesehene Empfänger Nachrichteninhalte anzeigen können. <br/> |
|[Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Azure Information Protection (manchmal auch als AIP bezeichnet) hilft einer Organisation, Dokumente und e-Mails zu klassifizieren, zu bezeichnen und optional zu schützen. Administratoren können Bezeichnungen automatisch zuweisen, indem Sie Regeln und Bedingungen definieren. Benutzer können Bezeichnungen manuell auf Dateien und e-Mails anwenden. Sie können Benutzern auch Empfehlungen geben, wann Beschriftungen angewendet werden sollen.<br/> Wenn Sie Sensitivitäts Bezeichnungen oder die Office-Nachrichtenverschlüsselung verwenden, verwenden Sie bereits Klassifizierungs-und Schutzfunktionen. Wenn Sie Azure Information Protection-Bezeichnungen noch nicht in Office 365 migriert haben, sollten Sie diese in Azure Information Protection weiterhin verwalten.  <br/>Sie können den [Azure Information Protection-Scanner](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) lokal ausführen, um Dateien auf Windows Server, Netzwerkfreigaben und SharePoint Server-Websites und-Bibliotheken zu klassifizieren und zu schützen. Dies kann ein erster Schritt in Richtung der Identifizierung von Daten sein, die zu Office 365 migriert werden sollen.
|Azure Information Protection mit vom Kunden verwalteten Verschlüsselungsschlüssel <br/> |Einige Organisationen benötigen eine geschäftliche Anforderung oder Compliance-Anforderung, um die Kontrolle über einen Verschlüsselungsschlüssel beizubehalten. Dies ist jedoch nicht die Regel. Azure Information Protection ermöglicht es Organisationen, ihren eigenen Schlüssel (BYOK) in den Dienst zu integrieren. Weitere Informationen finden Sie unter [holen eines eigenen Schlüssels (BYOK) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). Eine weitere komplexere Option wird für Kunden angeboten, die einen Verschlüsselungsschlüssel lokal aufbewahren müssen, der als "eigenen Schlüssel halten" (Hyok) bezeichnet wird.  Weitere Informationen finden Sie unter [halten eines eigenen Schlüssels (Hyok) für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions). <br/> |
    


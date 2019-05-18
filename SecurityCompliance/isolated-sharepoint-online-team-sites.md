---
title: Isolierte SharePoint Online-Teamwebsites
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 71250a04-fd2d-4c3c-a32b-b8a838b19a54
description: 'Zusammenfassung: Informationen zu Verwendungszwecken für isolierte SharePoint Online-Teamwebsites.'
ms.openlocfilehash: 07f4d84493cdc7c0e153186164824fe8aa1e36bc
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150067"
---
# <a name="isolated-sharepoint-online-team-sites"></a>Isolierte SharePoint Online-Teamwebsites

 **Zusammenfassung:** Informationen zu Verwendungszwecken für isolierte SharePoint Online-Teamwebsites.
  
SharePoint Online-Teamwebsites sind eine einfache Möglichkeit, um schnell einen Ort für die Zusammenarbeit an Notizen, Dokumenten, Artikeln, einem Kalender und anderen Ressourcen in Microsoft Office 365 zu erstellen. SharePoint Online-Teamwebsites basieren auf einer Office 365-Gruppe und haben ein vereinfachtes Verwaltungsmodell, um die offene Zusammenarbeit mit einer privaten Menge von Gruppenmitgliedern oder der gesamten Organisation zu ermöglichen. Über eine standardmäßige SharePoint Online-Teamwebsite können Mitglieder der Office 365-Gruppe andere Benutzer einladen und Berechtigungseinstellungen steuern.
  
In einigen Fällen möchten Sie vielleicht jedoch eine SharePoint Online-Teamwebsite für die Zusammenarbeit erstellen, bei der die Berechtigungen der Website strenger über Gruppenmitgliedschaft und SharePoint Online-Berechtigungsebenen gesteuert werden, die nur von SharePoint-Administratoren verwaltet werden. Wir bezeichnen dies als eine isolierte Website, die auf die Gruppe der Benutzer beschränkt ist, die entweder auf der Website zusammenarbeiten, ihren Inhalt anzeigen oder diese verwalten. Eine isolierte Website kann z. B. in folgenden Fällen erforderlich sein:
  
- Für ein geheimes Projekt innerhalb Ihrer Organisation.
    
- Als Speicherort für das besonders vertrauliche oder wertvolle geistige Eigentum Ihrer Organisation.
    
- Für die Ressourcen im Zusammenhang mit einer Klage, die von Ihrer Organisation erhoben oder die gegen sie geführt wird.
    
- Zum Freigeben eines Office 365-Abonnements für mehrere Organisationen, zwischen denen es zwar einige Überschneidungen gibt, die jedoch größtenteils als eigenständige Geschäftseinheiten existieren.
    
Dies sind die Anforderungen einer isolierten-Website:
  
- Nur SharePoint Online-Administratoren können Aufgaben der Websiteverwaltung ausführen; hierzu gehören die Gruppenmitgliedschaft für den Zugriff auf die Website und das Konfigurieren von benutzerdefinierten Berechtigungen.
    
- Mitglieder der Website können keine anderen Mitglieder zur Teamwebsite einladen.
    
- Benutzer, die kein Mitglied der isolierten Website sind, können keinen Zugriff auf die Website anfordern. Wenn sie versuchen, auf eine der Website zugeordnete URL zuzugreifen, wird eine Webseite mit der Meldung angezeigt, dass der Zugriff verweigert wurde.
    
Der Nachteil beim Anfordern einer zentralen Zugriffssteuerung und von benutzerdefinierten Berechtigungen von SharePoint Online-Administratoren besteht darin, dass die Website isoliert bleibt. Beispielsweise können aktuelle Mitglieder weder absichtlich noch versehentlich andere Benutzer innerhalb des Office 365-Abonnements, die kein Mitglied der Website sein sollten, einladen oder benutzerdefinierte Berechtigungen für diese konfigurieren.
  
Eine isolierte Website kann mit anderen Features wie z. B. den folgenden verwendet werden:
  
- Information Rights Management, um sicherzustellen, dass die Ressourcen auf der Website verschlüsselt bleiben, auch wenn sie lokal heruntergeladen und auf eine andere Website hochgeladen werden, die der gesamten Organisation zur Verfügung steht.
    
- Verhinderung von Datenverlust, um Benutzer daran zu hindern, die Ressourcen der Website (z. B. Dateien) per E-Mail zu senden.
    
## <a name="next-steps"></a>Nächste Schritte

Wenn Sie eine isolierte SharePoint Online-Teamwebsite in einem Testabonnement ausprobieren möchten, finden Sie eine schrittweise Anleitung unter [Isolierte SharePoint Online-Teamwebsite in Ihrer Office 365-Entwicklungs-/Testumgebung](isolated-sharepoint-online-team-site-dev-test-environment.md).
  
Wenn Sie eine isolierte SharePoint Online-Teamwebsite in der Produktion bereitstellen möchten, lesen Sie die schrittweisen Überlegungen zum Entwurf unter [Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Siehe auch

[Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md)
  
[Verwalten einer isolierten SharePoint Online-Teamwebsite](manage-an-isolated-sharepoint-online-team-site.md)

[Bereitstellen einer isolierten SharePoint Online-Teamwebsite](deploy-an-isolated-sharepoint-online-team-site.md)



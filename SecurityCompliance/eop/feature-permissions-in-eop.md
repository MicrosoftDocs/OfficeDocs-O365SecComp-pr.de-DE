---
title: Featureberechtigungen in EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/30/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 34674847-a6b7-4a7e-9eaa-b64f22bc150d
description: Die erforderlichen Berechtigungen zum Ausführung von Verwaltungsaufgaben für Microsoft Exchange Online Protection (EOP) variieren abhängig davon, welche Funktion verwaltet werden soll.
ms.openlocfilehash: fe39403e60664b0340f01070ccec22b674b5bc62
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027472"
---
# <a name="feature-permissions-in-eop"></a>Featureberechtigungen in EOP

Die erforderlichen Berechtigungen zum Ausführung von Verwaltungsaufgaben für Microsoft Exchange Online Protection (EOP) variieren abhängig davon, welche Funktion verwaltet werden soll. 
  
Zum Einrichten von EOP müssen Sie globaler Office 365-Administrator oder Exchange-Unternehmensadministrator (Rollengruppe „Organisationsverwaltung") sein.
  
## <a name="exchange-online-protection-permissions"></a>Exchange Online Protection-Berechtigungen

In der folgenden Tabelle sind die Berechtigungen aufgeführt, die für die Verwaltung der EOP-Funktionen erforderlich sind. Wenn für eine Funktion mehr als eine Rollengruppe aufgelistet wird, muss Ihnen lediglich eine der Rollengruppen zugewiesen sein, um diese Funktion nutzen zu können.
  
|**Feature**|**Erforderliche Berechtigungen**|
|:-----|:-----|
|Antischadsoftware  <br/> |[Organisationsverwaltung](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Antispam  <br/> |[Organisationsverwaltung](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Verwaltung von Nachrichtenschutz](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Nachrichtenflussregeln  <br/> |[Organisationsverwaltung](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Records Management](http://technet.microsoft.com/library/0e0c95ce-6109-4591-b86d-c6cfd44d21f5.aspx) <br/> |
|Domänen  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Erweiterte Threat Protection (ATP)  <br/> |[Organisationsverwaltung](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Verwaltung von Nachrichtenschutz](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Office 365-Connectors  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Nachrichtenablaufverfolgung  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Organisationskonfiguration  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Quarantäne  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Benutzer, Kontakte und Rollengruppen  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Verteilergruppen und Sicherheitsgruppen  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Berichte anzeigen  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) - Benutzer haben Zugriff auf E-Mail-Schutzberichte.  <br/> [View-Only Recipients](http://technet.microsoft.com/library/37e66b92-81d3-412f-b7a9-e1bb8cbeb468.aspx) - Benutzer haben Zugriff auf E-Mail-Schutzberichte.  <br/> [Compliance Management](http://technet.microsoft.com/library/b91b23a4-e9c7-4bd0-9ee3-ec5cb498da15.aspx) - Benutzer haben Zugriff auf E-Mail-Schutzberichte und DLP-Berichte (Data Loss Prevention, Schutz vor Datenverlust), sofern ihr Abonnement über DLP-Funktionen verfügt.  <br/> |
   


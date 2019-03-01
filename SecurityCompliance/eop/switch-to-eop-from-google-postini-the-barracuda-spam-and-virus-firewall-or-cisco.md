---
title: Wechseln zu EOP von Google Postini, Barracuda Spam &amp; Virus Firewall oder Cisco IronPort
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: In diesem Thema wird erläutert, wie Sie das Verfahren für das Wechseln zu Exchange Online Protection (EOP) von einer lokalen e-Mail-Hygiene-Appliance oder einem cloudbasierten Schutzdienst verstehen und Ihnen dann Hilferessourcen für die ersten Schritte zur Verfügung stellen können.
ms.openlocfilehash: a1fa7b63dfc1e6eb193d458545722c4b5331bc48
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30340756"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Wechseln zu EOP von Google Postini, Barracuda Spam &amp; Virus Firewall oder Cisco IronPort

 In diesem Thema wird der Wechsel von einer lokalen E-Mail-Schutzvorrichtung oder einem cloudbasierten Schutzdienst zu Exchange Online Protection (EOP) näher erläutert. Zur Erleichterung des Einstiegs werden hier außerdem einige Hilferessourcen genannt. Es gibt zahlreiche Lösungen zum Filtern von Spam, doch läuft der Wechsel zu EOP in den meisten Fällen ähnlich ab.
  
Wenn Sie EOP noch nicht kennen und sich erst einen Überblick über seine Funktionen verschaffen möchten, bevor Sie sich für einen Wechsel entscheiden, lesen Sie zunächst [Exchange Online Protection im Überblick](exchange-online-protection-overview.md) auf TechNet. 
  
Bevor Sie zu EOP wechseln, sollten Sie zuerst überlegen, ob Sie die EOP-geschützten Postfächer in der Cloud, mit Exchange Online, lokal oder in einem hybriden Szenario hosten möchten. (Bei einem hybriden Szenario werden Postfächer teils lokal und teils mit Exchange Online gehostet.) Jedes dieser Hostingszenarios - cloudbasiert, lokal oder hybrid - ist möglich, wird jedoch u. U. unterschiedlich eingerichtet. Die folgenden Überlegungen sollen Ihnen bei der Wahl der richtigen Bereitstellung helfen:
  
- **EOP-Schutz mit lokalen Postfächern**: Dieses Szenario ist geeignet, wenn Sie eine vorhandene E-Mail-Hostinginfrastruktur verwenden möchten oder die geschäftlichen Anforderungen lokal gehostete Postfächer erforderlich machen und Sie den cloudbasierten E-Mail-Schutz von EOP nutzen möchten. Eine genauere Beschreibung dieses Szenarios finden Sie unter [Wechseln zu EOP als eigenständige Lösung](#BKMK_SwitchStandalone.md). 
    
- **EOP-Schutz mit Exchange Online-Postfächern**: Dieses Szenario ist geeignet, wenn Sie EOP-Schutz nutzen und alle Postfächer in der Cloud hosten möchten. Dadurch verringert sich die Komplexität, da Sie keine lokalen Messagingserver unterhalten müssen. Dieses Szenario wird unter [Wechseln zu Exchange Online](switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco.md#BKMK_SwitchEXO) beschrieben. 
    
- **EOP-Schutz mit hybriden Postfächern**: Vielleicht hätten Sie gerne Postfächer in der Cloud, müssen aber die Postfächer einiger Benutzer lokal hosten. Wählen Sie dieses Szenario, wenn Sie Postfächer teils lokal und teils mit Exchange Online hosten möchten. Dieses Szenario wird unter [Wechseln zu einer Hybridlösung](#BKMK_SwitchHybrid.md) beschrieben. 
    
## <a name="switch-to-eop-standalone"></a>Wechseln zu EOP als eigenständige Lösung
<a name="BKMK_SwitchStandalone"> </a>

Wenn Sie Postfächer derzeit lokal hosten und eine lokale Schutzvorrichtung oder einen cloudbasierten Messagingschutzdienst verwenden, können Sie zu EOP wechseln, um von seinen Schutzfunktionen und seiner Verfügbarkeit zu profitieren. Wenn Sie EOP als eigenständige Lösung einrichten möchten, d. h. mit lokal gehosteten Postfächern und EOP als E-Mail-Schutz, befolgen Sie die Anleitung unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md). Sie umfasst die Schritte zum Einrichten von EOP-Schutz, wie das Anmelden, das Hinzufügen einer Domäne und das Einrichten des Nachrichtenflusses mit Connectors.
  
## <a name="switch-to-exchange-online"></a>Wechseln zu Exchange Online
<a name="BKMK_SwitchEXO"> </a>

Vielleicht haben Sie lokale Postfächer, die von einer lokalen Vorrichtung geschützt werden, und möchten auf cloudgehostete Exchange Online-Postfächer und EOP-Schutz umsteigen, um die Vorteile der cloudbasierten Messaging- und Schutzfunktionen von Office 365 zu nutzen. Als Erstes können Sie sich bei Office 365 anmelden und Ihre Domäne hinzufügen. In diesem Szenario müssen Sie keine Connectors einrichten, da kein Routing an lokale Postfächer erfolgt. Beginnen Sie auf der [Office 365-Anmeldeseite](https://www.microsoft.com/en-us/office365/online-software.aspx). (Unter [Erste Schritte mit Office 365](https://go.microsoft.com/fwlink/p/?LinkId=275407) finden Sie Ressourcen zum Kennenlernen der Funktionen). 
  
Während der Einrichtung von Office 365 erstellen Sie cloudbasierte Postfachbenutzer.
  
## <a name="switch-to-a-hybrid-solution"></a>Wechseln zu einer Hybridlösung
<a name="BKMK_SwitchHybrid"> </a>

Unter Umständen möchten Sie aufgrund geschäftlicher Anforderungen oder aus Vorschriftsgründen nur einen Teil Ihrer Postfächer in die Cloud verschieben. Wenn Sie ein hybrides Szenario bereitstellen, können Sie Postfächer je nach geschäftlichen Anforderungen in die Cloud verschieben. Die Migration zu einem hybriden Szenario mit EOP-Schutz ist zwar komplizierter als die Umstellung auf ein rein cloudbasiertes Szenario, doch bietet Microsoft volle Unterstützung für Hybridlösungen und zahlreiche Ressourcen, um diesen Vorgang zu erleichtern.
  
Wenn Sie eine Hybridbereitstellung in Erwägung ziehen, ist [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx) dafür der beste Ausgangspunkt. Außerdem stehen in einem hybriden Szenario verschiedene Möglichkeiten zum Weiterleiten von E-Mails zur Verfügung, mit denen Sie sich vertraut machen sollten. Unter [Transport Routing in Exchange 2013 Hybrid Deployments](http://technet.microsoft.com/library/36c2cea3-2e2f-40ac-88bd-7e1b6bd27828.aspx) werden diese im Einzelnen erläutert, sodass Sie je nach geschäftlichen Anforderungen das beste Routingszenario auswählen können. 
  
## <a name="migration-planning"></a>Migrationsplanung
<a name="sectionSection3"> </a>

Wenn Sie sich für einen Wechsel zu EOP entscheiden, sollten Sie unbedingt folgenden Bereichen Beachtung schenken:
  
- **Benutzerdefinierte Filterregeln** Wenn Sie über benutzerdefinierte Filter-oder Geschäftsrichtlinien Regeln verfügen, um bestimmte Spam abzufangen, empfiehlt es sich, EOP mit den Standardeinstellungen für einen Zeitraum zu testen, bevor Sie Ihre Regeln migrieren. EOP bietet Spam Schutz auf Unternehmensniveau mit den Standardeinstellungen kann es sein, dass Sie einige ihrer Regeln nicht zu EOP migrieren müssen. Wenn Sie über Regeln verfügen, mit denen bestimmte benutzerdefinierte Geschäftsrichtlinien erzwungen werden, können Sie diese erstellen. [Nachrichtenfluss Regeln (Transportregeln) in Exchange Online Protection](mail-flow-rules-transport-rules-0.md) enthält detaillierte Anweisungen zum Erstellen von Nachrichtenfluss Regeln in EoP. 
    
- **IP-Zulassungslisten und IP-Sperrlisten** Wenn Sie Zulassungslisten und Sperrlisten auf Benutzerbasis haben, lassen Sie die Listen in EOP als Teil des Setupvorgangs kopieren. Weitere Informationen zu IP-Zulassungslisten und IP-Sperrlisten finden Sie unter [configure the Connection Filter Policy](../configure-the-connection-filter-policy.md).
    
- **Sichere Kommunikation**: Wenn Sie Partner haben, die verschlüsseltes Messaging erforderlich machen, sollten Sie dies über die Exchange-Verwaltungskonsole einrichten. Informationen zum Konfigurieren dieses Szenarios finden Sie unter [Create connectors for a secure mail channel using transport layer security (TLS)](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx).
    
> [!TIP]
> Beim Wechsel von einer lokalen Vorrichtung zu EOP können Sie diese oder einen Server weiterhin einsetzen, um Geschäftsregeln zu überprüfen. Wenn von der Vorrichtung beispielsweise benutzerdefinierte Filter auf ausgehende E-Mails angewendet werden und Sie dies auch weiterhin wünschen, können Sie EOP so konfigurieren, dass E-Mails zur zusätzlichen Filterung direkt an die Vorrichtung gesendet werden, bevor sie an das Internet weitergeleitet werden. Unter [Exchange Online Protection Connectors - Outbound Smart Host Scenario](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx) wird gezeigt, wie der Nachrichtenfluss in diesem Fall eingerichtet wird. 
  


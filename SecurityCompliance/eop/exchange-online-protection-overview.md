---
title: Exchange Online Protection im Überblick
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 01/31/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft Exchange Online Protection (EOP) ist ein cloudbasierter Dienst zum Filtern von E-Mails, mit dem Sie Ihre Organisation vor Spam und Schadsoftware schützen können.
ms.openlocfilehash: 16f2f423b6e517cf204e4b4f6a2949baebfd6223
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686364"
---
# <a name="exchange-online-protection-overview"></a>Exchange Online Protection im Überblick

Microsoft Exchange Online Protection (EOP) ist ein cloudbasierter E-Mail-Filterungsdienst, der zum Schutz Ihrer Organisation vor Spamnachrichten und Schadsoftware beiträgt und Funktionen zum Schutz Ihrer Organisation vor Verletzungen von Nachrichtenrichtlinien aufweist. EOP kann die Verwaltung Ihrer Messagingumgebung und viele der beschwerlichen Aufgaben bei der Verwaltung lokaler Hardware und Software vereinfachen.
  
EOP kann in erster Linie über die folgenden Methoden für den Nachrichtenschutz eingesetzt werden:
  
- **In einem eigenständigen Szenario** EOP bietet Cloud-basierte e-Mail-Schutz für Ihre lokale Microsoft Exchange Server 2013-Umgebung, Legacyversionen von Exchange Server oder eine beliebige andere lokale SMTP-e-Mail-Lösung. 
    
- **Als Bestandteil von Microsoft Exchange Online** EOP schützt standardmäßig cloudgehostete Postfächer von Microsoft Exchange Online. 
    
- **In einer Hybridbereitstellung** kann EOP für den Schutz Ihrer Messagingumgebung und für die Steuerung von E-Mail-Routing konfiguriert werden, wenn Sie sowohl über lokale als auch über Cloud-Postfächer verfügen. 
    
## <a name="how-eop-works"></a>Funktionsweise von EOP

Die Funktionsweise von EOP lässt sich am besten an der Verarbeitung eingehender E-Mails veranschaulichen:
  
![EOP-e-Mail-Verarbeitung](../media/EOP-email-processing.png)
  
Eine eingehende Nachricht durchläuft zunächst Verbindungsfilter, die der Sender Reputation überprüft, und untersucht die Meldung für Schadsoftware. Die meisten Spam ist zu diesem Zeitpunkt beendet und von EOP gefiltert werden gelöscht. Nachrichten weiterhin über richtlinienfilterung, wobei Nachrichten für benutzerdefinierte Transportregeln ausgewertet werden, die Sie erstellen oder aus einer Vorlage zu erzwingen. Beispielsweise haben Sie eine Regel, die eine Benachrichtigung an einen Manager, beim Eintreffen von Nachrichten von einem bestimmten Absender sendet. (Data Loss Prevention überprüft auch zu diesem Zeitpunkt bei auftreten, die Funktion; Informationen zur Verfügbarkeit von Features finden Sie in der [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Übergeben Sie im nächsten Schritt Nachrichten über Content-Filterung, auf dem Inhalt für Terminologie oder allgemeine Eigenschaften auf spam überprüft wird. Eine Nachricht festgestellt, dass Spam vom Inhaltsfilter auf Junk-e-Mail-Ordner eines Benutzers oder der Quarantäne unter Weitere Optionen, basierend auf Ihrer Einstellungen gesendet werden kann. Nachdem eine Nachricht alle diese Ebenen Schutz erfolgreich übergibt, wird es an den Empfänger übermittelt.
  
### <a name="eop-datacenters"></a>EOP-Datencenter

EOP wird in einem weltweiten Rechenzentrennetzwerk ausgeführt, das für eine optimale Verfügbarkeit entworfen wurde. Wenn ein Rechenzentrum ausfällt, werden E-Mails ohne jegliche Dienstunterbrechung automatisch an ein anderes Rechenzentrum weitergeleitet. Die Server in den einzelnen Rechenzentren akzeptieren Nachrichten in Ihrem Namen und trennen Ihre Organisation dadurch vom Internet. So wird die Last Ihrer Server gesenkt. Mit diesem hochverfügbaren Netzwerk kann Microsoft sicherstellen, dass E-Mails rasch an Ihre Organisation übermittelt werden. 
  
EOP führt einen Lastenausgleich zwischen Rechenzentren aus, jedoch nur innerhalb einer Region. Wenn Sie über eine Bereitstellung in einer bestimmten Region verfügen, werden alle Nachrichten mit dem E-Mail-Routing für diese Region verarbeitet. Die folgende Liste zeigt, wie regionales E-Mail-Routing für die EOP-Datencenter funktioniert:
  
    
- In Europa, dem Nahen Osten und Afrika (EMEA) befinden sich alle Exchange Online-Postfächer in EMEA-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über EMEA-Rechenzentren geleitet.
    
- In Asien-Pazifik ("APAC"), befinden sich alle Exchange Online-Postfächern in Rechenzentren "APAC", aber Nachrichten derzeit über "APAC" Rechenzentren für EOP-Filterung geleitet werden.
=======
- In der amerikanischen Kontinent befinden sich alle Exchange Online-Postfächern in US-Datencentern, mit Ausnahme von Südamerika, wo Rechenzentren in Brasilien und Chile verwendet werden, und in Kanada, in denen Rechenzentren in Kanada verwendet werden. Alle e-Mail-Nachrichten, einschließlich Nachrichten für Kunden in Südamerika und in Kanada, werden über lokale Rechenzentren für EOP-Filterung weitergeleitet; Quarantäne gestellte e-Mails wird im Datencenter gespeichert, in dem der Mandant befindet.
    
- In Europa, dem Nahen Osten und Afrika (EMEA) befinden sich alle Exchange Online-Postfächer in EMEA-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über EMEA-Rechenzentren geleitet.
    
- In Asien-Pazifik ("APAC"), befinden sich alle Exchange Online-Postfächern in Rechenzentren "APAC", und Nachrichten werden derzeit über "APAC" Rechenzentren für EOP-Filterung weitergeleitet.
    
- Alle Exchange Online-Postfächer für die Government Community Cloud (GCC) befinden sich in US-Rechenzentren, und alle Nachrichten werden zur EOP-Filterung über US-Rechenzentren geleitet.
    
## <a name="eop-plans-and-features"></a>EOP-Dienste und -Funktionen

Die folgenden EOP-Abonnementpläne sind verfügbar:
  
- **EOP als eigenständige Lösung** Hier schützt EOP Ihre lokalen Postfächer. 
    
- **EOP-Funktionen in Exchange Online** Hier schützt EOP Ihre cloudgehosteten Exchange Online-Postfächer. 
    
- **Exchange Enterprise CAL mit Diensten** Hier schützt EOP Ihre lokalen Postfächer wie EOP als eigenständige Lösung. Außerdem sind DLP-Funktionen (Data Loss Prevention, Verhinderung von Datenverlust) und eine Berichterstellung mithilfe von Webdiensten verfügbar. 
    
Weitere Informationen zu Anforderungen, wichtigen Grenzwerten und Verfügbarkeit von Funktionen in allen EOP-Abonnementplänen finden Sie in der [Exchange Online Protection-Dienstbeschreibung](https://go.microsoft.com/fwlink/p/?LinkId=320619).
  
## <a name="setting-up-eop"></a>Einrichten von EOP

EOP-Bereitstellungen können einfach sein. Dies gilt insbesondere für kleine Organisationen mit einer Handvoll Regeln für die Richtlinientreue. Verfügen Sie jedoch über eine große Organisation mit mehreren Domänen, benutzerdefinierten Richtlinienregeln oder Hybridnachrichtenübermittlung, kann die Einrichtung einen höheren Planungs- und Zeitaufwand erfordern.
  
Sollten Sie bereits EOP erworben haben, können Sie mit den Hinweisen unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md) sicherstellen, dass Sie alle für die Konfiguration von EOP zum Schutz Ihrer Nachrichtenumgebung erforderlichen Schritte ausgeführt haben. 
  
## <a name="for-more-information"></a>Weitere Informationen

[EOP-Funktionen](eop-features.md)
  
[Videos für erste Schritte mit EOP](videos-for-getting-started-with-eop.md)
  
[EOP - Allgemeine häufig gestellte Fragen](eop-general-faq.md)
  
[Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten](eop-queued-deferred-and-bounced-messages-faq.md)
  
[Häufig gestellte Fragen zur delegierten Verwaltung](delegated-administration-faq.md)
  
[Verschieben von Domänen und Einstellungen zwischen EOP-Organisationen](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  


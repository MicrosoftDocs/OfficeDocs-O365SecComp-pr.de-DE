---
title: Office 365 verteidigen von Cloud-Diensten vor Denial-of-Service-anGriffen
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Wie Microsoft seine Cloud-Dienste gegen Denial-of-Service-Angriffe (DoS) verteidigt.
ms.openlocfilehash: 784e17d4b80ac990c903c96f92cd6b96f194439b
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004182"
---
# <a name="defending-microsoft-cloud-services-against-denial-of-service-attacks"></a>Schützen von Microsoft Cloud Services vor Denial-of-Service-anGriffen

## <a name="introduction"></a>Einführung
Microsoft-Rechenzentren sind durch umfassende Sicherheitsvorkehrungen geschützt, die das einzäunen von Umzäunung, Videokameras, Sicherheitspersonal und sicheren Eingängen umfassen, die Biometrie, Smartcard und mehrstufige Authentifizierung verwenden. Die mehrstufige Verteidigungs Sicherheit wird über jeden Bereich der Anlage und zu jeder physischen SERVEREINHEIT fortgesetzt. Die [Microsoft Cloud Infrastructure and Operations Group](https://www.microsoft.com/en-us/cloud-platform/global-datacenters) stellt die Kerninfrastruktur und grundlegende Technologien für unsere Cloud-Dienste bereit. Unsere Rechenzentren erfüllen Branchenstandards für physische Sicherheit und Zuverlässigkeit und werden vom Microsoft-Betriebspersonal verwaltet, überwacht und administriert.

Um unsere Cloud-Dienste weiter zu schützen, bietet Microsoft ein DDoS-Abwehrsystem an, das Teil der Prozesse für die kontinuierliche Überwachung und Penetrationstests in Microsoft Azure ist. Das Azure DDoS-Abwehrsystem soll nicht nur Angriffen von außen, sondern auch von anderen Azure-Mandanten widerstehen. Azure verwendet standardmäßige Erkennungs-und Abschwächungs Techniken wie SYN-Cookies, Ratenbegrenzung und Verbindungslimits zum Schutz vor DDoS-Angriffen.

Die Cloud-Dienste von Microsoft unterliegen der Androhung von Angriffen aus mehreren Quellen. Um die unterschiedlichen DoS-Bedrohungen zu verringern und zu schützen, wurde ein hoch skalierbares und dynamisches System zur Erkennung und Abwehr von Bedrohungen auf Azure-Basis entwickelt und implementiert, mit dem primären Ziel des Schutzes der zugrunde liegenden Infrastruktur vor DoS-Angriffen und helfen, Dienstunterbrechungen für Cloud Services-Kunden zu verhindern. Das Azure DoS-Abwehrsystem schützt den eingehenden, ausgehenden und Region-zu-Region-Datenverkehr.

Die meisten DoS-Angriffe wurden für Ziele auf den Netzwerk-(L3)-und Transport (L4)-Ebenen des OSI-Modells ( [Open Systems](https://docs.microsoft.com/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Interconnection) gestartet. Angriffe, die auf die L3-und L4-Ebenen gerichtet sind, sind darauf ausgelegt, eine Netzwerkschnittstelle oder einen Dienst mit Angriffs Datenverkehr zu überschwemmen, um Ressourcen zu überlasten und die Fähigkeit zur Reaktion auf legitimen Datenverkehr Insbesondere versuchen L3-und L4-Angriffe, die Kapazität von Netzwerkverbindungen, Geräten oder Diensten zu sättigen oder die CPUs von Servern oder virtuellen Computern zu überlasten, die eine Anwendung unterstützen.

Um vor L3-und L4-Angriffen zu schützen, hat Microsoft eine Lösung entworfen, entwickelt und bereitgestellt, die speziell darauf abzielt, die Infrastruktur und die Zielvorgaben der Kunden zu schützen, indem diese Schichten geschützt werden. Durch den Schutz der Infrastruktur wird sichergestellt, dass der Angriffs Verkehr für einen Kunden keine Kollateralschäden oder eine verringerte Netzwerkdienst Qualität für andere Kunden verursacht. Die Lösung verwendet Daten vom Datenverarbeitungs Center-Router. Diese Daten werden von einem Netzwerk Überwachungsdienst analysiert, um Angriffe zu identifizieren. Bei der Erkennung eines Angriffs treten automatisierte Schutzmechanismen in Angriff.

## <a name="application-level-defenses"></a>Verteidigung auf Anwendungsebene
Microsoft Engineering Teams befolgen die strengen Standards von [Microsoft operationAl Security Assurance](https://www.microsoft.com/en-us/SDL/OperationalSecurityAssurance) , um Kundendaten zu schützen. Die Cloud-Dienste von Microsoft sind absichtlich für eine sehr hohe Auslastung sowie zum Schutz und zur Minderung von DoS-Angriffen auf Anwendungsebene vorgesehen. Wir haben eine skalierte Architektur implementiert, bei der Dienste über mehrere globale Rechenzentren mit regionalen Isolierungs-und Einschränkungsfunktionen in einigen Arbeitslasten verteilt werden.

Das Land oder die Region jedes Kunden, das der Administrator des Kunden während der Ersteinrichtung der Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden gemäß einer primären/Sicherungsstrategie zwischen redundanten Rechenzentren repliziert. Ein primäres Rechenzentrum hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die in der Software laufen. Ein Sicherungsdatencenter bietet automatisches Failover. Wenn das primäre Rechenzentrum aus irgendeinem Grund nicht mehr funktioniert, werden Anforderungen an die Kopie der Software-und Kundendaten in der Sicherungsdatenbank umgeleitet. Kundendaten können zu einem bestimmten Zeitpunkt entweder im primären oder im Sicherungs Center verarbeitet werden. Das Verteilen von Daten über mehrere Rechenzentren reduziert die betroffene Oberfläche, wenn ein Rechenzentrum angegriffen wird. Darüber hinaus können die Dienste im betroffenen Datencenter als einer der Wiederherstellungsmechanismen schnell an das sekundäre Datencenter umgeleitet werden, und umgekehrt (umgeleitet zurück zum primären Datencenter, nachdem der Dienst wiederhergestellt wurde).

Einzelne Arbeitsauslastungen beinhaltet integrierte Funktionen zur Verwaltung der Ressourcennutzung. Beispielsweise sind die Einschränkungs Mechanismen in Exchange Online und SharePoint Online Teil eines mehrstufigen Ansatzes zur Abwehr von DoS-Angriffen. Die Einschränkung für Exchange Online-Benutzer basiert auf der vom Endbenutzer verwendeten Ressourcenebene, unabhängig davon, ob sich die Ressourcen in Active Directory, im Exchange Online-Informationsspeicher oder an anderer Stelle befinden. Jedem Client wird ein Budget zugewiesen, um die von einem Benutzer verwendeten Ressourcen einzuschränken. Die Exchange Online-Drosselung für Benutzeraktivitäten und Systemkomponenten basiert auf der [Arbeitsauslastungsverwaltung](http://technet.microsoft.com/en-us/library/jj150503(v=exchg.150).aspx). Eine Exchange Online-Arbeitsauslastung ist ein Exchange Online-Feature,-Protokoll oder-Dienst, der explizit für die Exchange Online-Systemressourcenverwaltung definiert wurde. Jede Exchange Online-Arbeitsauslastung erfordert Systemressourcen wie CPU-, Postfachdaten Bankvorgänge oder Active Directory-Anforderungen zum Durchführen von Benutzeranforderungen oder Hintergrund arbeiten. Beispiele für Exchange Online-Arbeitslasten sind Outlook im Web, Exchange ActiveSync, Postfachmigration und Postfach-Assistenten. Mandantenadministratoren können die Einschränkungseinstellungen für die Exchange-workloadverwaltung für Benutzer mit der Exchange-Verwaltungsshell verwalten. Es gibt verschiedene Formen der Drosselung, die in Exchange Online implementiert wurden, einschließlich PowerShell, Exchange-webDienste und POP und IMAP, Exchange ActiveSync, Verbindungen für mobile Geräte, Empfänger und vieles mehr. Während Administratoren von lokalen Exchange-Bereitstellungen Einschränkungsrichtlinien konfigurieren können, können Administratoren keine Einschränkungsrichtlinien für Exchange Online konfigurieren.

Der häufigste Trigger für die Drosselung in SharePoint Online ist der clientseitige Objektmodellcode (CSOM), der zu viele Aktionen mit einer zu hohen Häufigkeit ausführt. Mit CSOM können viele Aktionen mit einer einzelnen Anforderung ausgeführt werden, die die Nutzungs Grenzwerte überschreiten und eine Drosselung pro Benutzer verursachen kann.

Unabhängig von der Aktivität, die zu Einschränkungen führen kann, wenn ein Benutzer Nutzungs Grenzwerte überschreitet, schränkt SharePoint Online alle weiteren Anforderungen von diesem Benutzerkonto ein, normalerweise für einen kurzen Zeitraum. Während eine Benutzer Einschränkung aktiv ist, werden alle Aktionen dieses Benutzers gedrosselt, bis die Drosselung abläuft, gemäß den folgenden Kriterien:
- Bei Anforderungen, die vom Benutzer direkt in einem Browser ausgeführt werden, wird von SharePoint Online zu einer Einschränkungs Informationsseite umgeleitet, und die Anforderungen schlagen fehl.
- Für alle anderen Anforderungen, einschließlich CSOM-Aufrufe, gibt SharePoint Online HTTP-Statuscode 429 ("zu viele Anforderungen") zurück, und die Anforderungen schlagen fehl.

Wenn der säumige Prozess weiterhin Nutzungs Grenzwerte überschreitet, kann SharePoint Online den Prozess vollständig blockieren und den HTTP-Statuscode 503 ("Dienst nicht verfügbar") zurückgeben.

## <a name="vulnerability-and-penetration-testing"></a>Sicherheits-und PenetrationsTests
Microsoft verwendet viele [Sicherheitstechnologien und-Methoden](https://www.microsoft.com/en-us/trustcenter/security/threatmanagement) , um [seine Cloud-Infrastruktur](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) und lokale Netzwerke vor modernen, anspruchsvollen Bedrohungen zu schützen, einschließlich der Verwendung von Antischadsoftware-Komponenten und-Diensten für Cloud-Dienste, virtuelle Computer (VMs) und andere Systeme; Erweiterte BedrohungsAnalyse, die normale Nutzungsmuster für Netzwerke, Systeme und Benutzer überwacht und das Erlernen von Computern verwendet, um alle ungewöhnlichen Verhaltensweisen und regelmäßige Penetrationstests zu kennzeichnen.

Neben der Durchführung eigener Penetrationstests und der Bereitstellung von [Microsoft Cloud Unified Penetration Testing-Programmen](https://technet.microsoft.com/en-us/mt784683)für unsere Kunden engagieren wir uns auch mit Sicherheitsexperten von Drittanbietern, die regelmäßige Sicherheitsrisikobewertungen von und Penetrationstests für unsere Cloud-Dienste. Die Berichte aus diesen Drittanbieter-Sicherheitsrisikobewertungen können vom [Service Trust](https://aka.ms/STP) und den [Service Assurance](https://aka.ms/ServiceAssurance) -Portalen heruntergeladen werden.

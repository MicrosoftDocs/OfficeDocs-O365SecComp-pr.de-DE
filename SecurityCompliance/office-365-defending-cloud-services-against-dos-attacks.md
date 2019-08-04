---
title: Office 365 schützen von Cloud-Diensten vor Denial-of-Service-Angriffen
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
description: Wie Microsoft seine Cloud-Dienste vor Denial-of-Service-Angriffen (DOS) verteidigt.
ms.openlocfilehash: 932e5a4d206a9d91c81e868e353259db954a2452
ms.sourcegitcommit: f0d23e57b00f07cef5b1b2d366eaeeeacda37e3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2019
ms.locfileid: "35786690"
---
# <a name="defending-microsoft-cloud-services-against-denial-of-service-attacks"></a>Schützen von Microsoft Cloud Services vor Denial-of-Service-Angriffen

## <a name="introduction"></a>Einführung
Microsoft-Rechenzentren werden durch umfassende Sicherheitsvorkehrungen geschützt, einschließlich Umkreis Fechten, Videokameras, Sicherheitspersonal und sicheren Eingängen, die Biometrie, Smartcard und mehrstufige Authentifizierung verwenden. Die tiefen Verteidigungs Sicherheit wird durch jeden Bereich der Einrichtung und für jede physische SERVEREINHEIT fortgesetzt. Die [Microsoft Cloud Infrastructure and Operations Group](https://www.microsoft.com/en-us/cloud-platform/global-datacenters) bietet die Kerninfrastruktur und grundlegende Technologien für unsere Cloud-Dienste. Unsere Rechenzentren entsprechen Branchenstandards für physische Sicherheit und Zuverlässigkeit und werden von Microsoft Operationspersonal verwaltet, überwacht und verwaltet.

Um unsere Cloud-Dienste weiter zu schützen, bietet Microsoft ein DDoS-Abwehrsystem an, das Teil der Microsoft Azure kontinuierlichen Überwachungs-und Penetrationstest Prozesse ist. Das Azure DDoS-Abwehrsystem ist nicht nur für Angriffe von außen, sondern auch von anderen Azure-Mandanten ausgelegt. Azure verwendet standardmäßige Erkennungs-und Minderungs Methoden wie SYN-Cookies, raten Begrenzungen und Verbindungs Grenzwerte zum Schutz vor DDoS-Angriffen.

Die Cloud-Dienste von Microsoft unterliegen der Bedrohung durch Angriffe aus mehreren Quellen. Zur Minderung und zum Schutz vor den verschiedenen DOS-Bedrohungen wurde ein hoch skalierbares und dynamisches Azure-basiertes System zur Erkennung und Abwehr von Bedrohungen entwickelt und implementiert, mit dem Hauptziel, die zugrunde liegende Infrastruktur vor DOS zu schützen. Angriffe und Unterstützung bei der Vermeidung von Dienstunterbrechungen für Cloud Services-Kunden. Das Azure DOS-Minderungs System schützt eingehende, ausgehende und Region-zu-Region-Datenverkehr.

Die meisten DOS-Angriffe werden für Ziele auf den Netzwerk-(L3) und Transport Ebenen (L4) des OSI-Modells ( [Open Systems](https://docs.microsoft.com/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Interconnection) gestartet. Angriffe auf die L3-und L4-Layer wurden entwickelt, um eine Netzwerkschnittstelle oder einen Dienst mit Angriffs Datenverkehr hoch zufluten, um Ressourcen zu überlasten und die Fähigkeit zu verweigern, auf legitimen Datenverkehr zu reagieren. Insbesondere L3-und L4-Angriffe versuchen, entweder die Kapazität von Netzwerkverbindungen, Geräten oder Diensten zu sättigen oder die CPUs von Servern oder virtuellen Computern zu überlasten, die eine Anwendung unterstützen.

Zum Schutz vor L3-und L4-Angriffen hat Microsoft eine Lösung entwickelt, entwickelt und bereitgestellt, die speziell darauf abzielt, die Infrastruktur und die Kunden Ziele zu schützen, die durch den Schutz dieser Schichten angegriffen werden. Durch den Schutz der Infrastruktur wird sichergestellt, dass der Angriffs Datenverkehr, der für einen Kunden bestimmt ist, keinen Kollateralschaden oder eine verringerte Netzwerkqualität für andere Kunden zur Folge hat. Die Lösung verwendet Datenverkehrs Samplingdaten von Rechenzentrums Routern. Diese Daten werden von einem Netzwerk Überwachungsdienst analysiert, um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, treten automatisierte Abwehrmechanismen ein.

## <a name="application-level-defenses"></a>Verteidigung auf Anwendungsebene
Microsoft Engineering Teams befolgten die strengen Standards, die von der [Microsoft Operational Security Assurance](https://www.microsoft.com/en-us/SDL/OperationalSecurityAssurance) zum Schutz von Kundendaten festgelegt wurden. Die Cloud-Dienste von Microsoft wurden absichtlich zur Unterstützung einer sehr hohen Last sowie zum Schutz und zur Milderung von DOS-Angriffen auf Anwendungsebene entwickelt. Wir haben eine skalierte Architektur implementiert, in der Dienste über mehrere globale Rechenzentren mit regionaler Isolierung und Einschränkungsfunktionen in einigen Arbeitslasten verteilt werden.

Das Land oder die Region jedes Kunden, das der Administrator des Kunden während der Ersteinrichtung der Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden gemäß einer primären/Sicherungsstrategie zwischen redundanten Rechenzentren repliziert. Ein primäres Rechenzentrum hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf der Software installiert sind. Ein Sicherungsdatencenter bietet ein automatisches Failover. Wenn das primäre Rechenzentrum aus irgendeinem Grund nicht mehr funktionsfähig ist, werden Anforderungen an die Kopie der Software-und Kundendaten im Sicherungsdatencenter umgeleitet. Kundendaten können zu einem bestimmten Zeitpunkt entweder im primären oder im Sicherungsdatencenter verarbeitet werden. Durch die Verteilung von Daten in mehreren Rechenzentren wird die betroffene Oberfläche reduziert, wenn ein Rechenzentrum angegriffen wird. Darüber hinaus können die Dienste im betroffenen Datencenter als einer der Wiederherstellungsmechanismen schnell zum sekundären Datencenter umgeleitet werden und umgekehrt (umgeleitet zurück zum primären Datencenter, sobald der Dienst wiederhergestellt wird).

Zu den einzelnen Arbeitslasten gehören integrierte Features zur Verwaltung der Ressourcennutzung. Beispielsweise sind die Einschränkungs Mechanismen in Exchange Online und SharePoint Online Teil eines mehrschichtigen Ansatzes zur Verteidigung gegen DoS-Angriffe. Die Einschränkung für Exchange Online Benutzer beruht auf der vom Endbenutzer verbrauchten Ressourcenebene, unabhängig davon, ob sich die Ressourcen in Active Directory, im Exchange Online Informationsspeicher oder an einer anderen Position befinden. Jedem Client wird ein Budget zugewiesen, um die von einem Benutzer konsumierten Ressourcen einzuschränken. Exchange Online Einschränkung für Benutzeraktivität und Systemkomponenten basiert auf der [Arbeitsauslastungsverwaltung](http://technet.microsoft.com/en-us/library/jj150503(v=exchg.150).aspx). Bei einer Exchange Online Arbeitsauslastung handelt es sich um ein Exchange Online Feature, Protokoll oder Dienst, das explizit für die Exchange Online Systemressourcenverwaltung definiert wurde. Für jede Exchange Online Arbeitsauslastung sind Systemressourcen wie CPU, Postfachdaten Bankvorgänge oder Active Directory Anforderungen zum Ausführen von Benutzeranforderungen oder Hintergrundarbeit erforderlich. Beispiele für Exchange Online Arbeitslasten sind Outlook im Internet, Exchange ActiveSync, Postfachmigration und Postfach-Assistenten. Mandantenadministratoren können die Einstellungen für die Einschränkung der Exchange-Arbeitsauslastungsverwaltung für Benutzer mit dem Exchange-Verwaltungsshell verwalten. Es gibt verschiedene Formen der Drosselung, die in Exchange Online implementiert wurden, einschließlich PowerShell, Exchange Webdienste und Pop und IMAP, Exchange ActiveSync, Verbindungen mit mobilen Geräten, Empfänger und vieles mehr. Während Administratoren von lokalen Exchange-Bereitstellungen Einschränkungsrichtlinien konfigurieren können, können Administratoren keine Einschränkungsrichtlinien für Exchange Online konfigurieren.

Der häufigste Auslöser für die Drosselung in SharePoint Online ist der clientseitige Objektmodellcode (CSOM), der zu viele Aktionen mit zu hoher Frequenz ausführt. Mit CSOM können zahlreiche Aktionen mit einer einzigen Anforderung durchgeführt werden, die die Verwendungsbeschränkungen überschreiten und die Einschränkung pro Benutzer verursachen kann.

Unabhängig von der Aktivität, die zu einer Drosselung führen kann, wenn ein Benutzer die Verwendungsbeschränkungen überschreitet, SharePoint Online alle weiteren Anforderungen dieses Benutzerkontos in der Regel für einen kurzen Zeitraum drosseln. Während eine Benutzer Drosselung wirksam ist, werden alle Aktionen dieses Benutzers so lange gedrosselt, bis die Drosselung abläuft, gemäß den folgenden Kriterien:
- Für Anforderungen, die vom Benutzer direkt in einem Browser ausgeführt werden, wird SharePoint Online an eine Einschränkungs Informationsseite umgeleitet, und die Anforderungen werden nicht erfüllt.
- Für alle anderen Anforderungen, einschließlich CSOM-Aufrufe, gibt SharePoint Online den HTTP-Statuscode 429 ("zu viele Anforderungen") zurück, und die Anforderungen werden nicht ausgeführt.

Wenn der problematische Prozess weiterhin die Verwendungsbeschränkungen überschreitet, kann SharePoint Online den Prozess vollständig blockieren und den HTTP-Statuscode 503 ("Dienst nicht verfügbar") zurückgeben.

## <a name="vulnerability-and-penetration-testing"></a>Sicherheitsrisiko und Penetrationstests
Microsoft verwendet zahlreiche [Sicherheitstechnologien und-Methoden](https://www.microsoft.com/en-us/trustcenter/security/threatmanagement) zum [Schutz seiner Cloud-Infrastruktur](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) und lokalen Netzwerke vor modernen, ausgeklügelten Bedrohungen, einschließlich der Verwendung von Antischadsoftware-Komponenten und-Diensten für Cloud-Dienste, virtuell Computer (VMS) und andere Systeme. Advanced Threat Analytics, die normale Verwendungsmuster für Netzwerke, Systeme und Benutzer überwacht und das maschinelle Lernen verwendet, um jedes Verhalten zu kennzeichnen, das außergewöhnlich ist, und regelmäßige Penetrationstests.

Neben der Durchführung eigener Penetrationstests und der Bereitstellung von [Microsoft Cloud Unified Penetration-Testprogramm](https://technet.microsoft.com/en-us/mt784683)für unsere Kunden bieten wir auch Sicherheitsexperten von Drittanbietern an, die regelmäßige Schwachstellen Bewertungen durchführen und Penetrationstests für unsere Cloud-Dienste. Wir stellen die Berichte aus diesen Drittanbieter Bewertungen zur Verfügung, die von der [Dienst Vertrauensstellung](https://aka.ms/STP) und den [Dienst Sicherungs](https://aka.ms/ServiceAssurance) Portalen heruntergeladen werden können.

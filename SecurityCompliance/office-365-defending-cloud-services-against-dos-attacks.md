---
title: Office 365 Clouddiensten Schutz vor Denial-of-Service-Angriffen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Wie Microsoft seine Clouddienste vor Denial-of-Service (DoS)-Angriffen schützt.
ms.openlocfilehash: f11a4293a35de4d36fd38fce892a4e59919111cc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529563"
---
# <a name="defending-microsoft-cloud-services-against-denial-of-service-attacks"></a>Verteidigen Microsoft Cloud-Dienste vor Denial-of-Service-Angriffen

## <a name="introduction"></a>Einführung
Microsoft-Rechenzentren werden durch Verteidigung Sicherheit geschützt, die enthält Umkreisnetzwerk Zäune, Videokameras, Sicherheitspersonals und sichere Eingänge, die Biometrik Smartcard und mehrstufige Authentifizierung zu verwenden. Die Verteidigung Sicherheit über jeden Bereich der Einrichtung und an jedem physischen Server Einheit fortgesetzt wird. [Microsoft-Cloud-Infrastruktur und der Gruppe Vorgänge](https://www.microsoft.com/en-us/cloud-platform/global-datacenters) bietet die Hauptinfrastruktur und grundlegenden Technologien für unsere Clouddienste. Unsere Rechenzentren werden Branchenstandards für physische Sicherheit und Zuverlässigkeit einhalten verwaltet, überwacht und verwaltet von Mitarbeitern des Microsoft Operations.

Um unsere Clouddienste weiter zu schützen, bietet Microsoft ein DDoS Defense System, das die Microsoft Azure kontinuierliche Überwachung und Durchdringungstests Prozesse gehört. Das Azure DDoS Defense System dient nicht nur für Angriffe von außen, sondern auch von anderen Azure Mandanten aufnehmen. Azure verwendet standard-Erkennung und einzusetzenden Techniken wie SYN-Cookies, Rate limiting und verbindungseinschränkungen zum Schutz gegen DDoS-Angriffe.

Microsoft Cloud-Dienste unterliegen die Bedrohung Angriff aus mehreren Quellen. Abwehren von und den Schutz gegen die verschiedenen DoS-Angriffen ein extrem skalierbar und dynamische Azure-basierte Erkennung und Risikominderung System entwickelt und implementiert, mit dem primären Ziel die zugrunde liegenden Infrastruktur von DoS-Angriffen zu schützen und eines Problems zu verhindern, dass Dienst unterbrechen für die Cloud services-Kunden. Das Azure DoS Risikominderung System schützt eingehenden, ausgehenden und regional-Datenverkehr.

Die meisten DoS-Angriffe gestartet für Ziele am Netzwerk (L3) und Transport (L4) Ebenen des Modells [Open Systeme Verbund](https://docs.microsoft.com/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI). Angriffe auf den Ebenen L3 und L4 dienen zum flood ein Netzwerkschnittstelle oder einen Dienst mit Angriff Datenverkehr überlastet Ressourcen und verweigern die Möglichkeit, auf legitime Datenverkehr zu reagieren. Insbesondere L3 und L4 Angriffe Versuch Sättigung erhöhen der Kapazität der Netzwerkverbindungen, Geräte und Dienste, oder führen die CPUs von Servern oder virtuelle Computer, der eine Anwendung.

Zum Schutz vor Angriffen L3 und L4 Microsoft entworfen, entwickelt und eine Lösung bereitgestellt wurde mit denen gezielt schützen die Infrastruktur und Kunden Ziele, die unter Angriff geliefert werden, indem diese Ebenen schützen. Schützen der Infrastruktur wird sichergestellt, dass für die direkte Verwendung für einen bestimmten Kunden Angriff Datenverkehr nicht Begleitmaterial Schäden führt oder Netzwerk Quality of Service für andere Kunden beeinträchtigt. Die Lösung verwendet Datenverkehr Samplingdaten von Routern Datacenter. Diese Daten analysiert werden durch ein Netzwerk Überwachungsdiensts um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, starten automatisierter Defense Mechanismen.

## <a name="application-level-defenses"></a>Schutz auf Anwendungsebene
Microsoft Entwicklungsteams führen Sie die strengen Standards zum Schutz von Kundendaten von [Microsoft betriebliche Sicherheit Assurance](https://www.microsoft.com/en-us/SDL/OperationalSecurityAssurance) festgelegt. Microsoft Cloud-Diensten basieren absichtlich zur Unterstützung der sowie einer sehr hohen Auslastung zu schützen und vor auf Anwendungsebene DoS-Angriffen zu verringern. Wir haben eine horizontale Skalierung Architektur implementiert, in dem Services in mehreren globale Rechenzentren mit regionalen Isolation und Features in einigen Arbeitslast Drosselung verteilt sind.

Land oder Region, die der Kunde Administrator während der Installation von den Diensten identifiziert, des Kunden bestimmt den primären Speicherort für diese Daten. Kundendaten werden zwischen redundante Rechenzentren gemäß einer Strategie für die primäre-Sicherung repliziert. Ein primäres Datencenter gehostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf die Software ausgeführt wird. Ein backup Datencenter bietet automatisches Failover. Wenn das primäre Datencenter nicht aus irgendeinem Grund funktioniert mehr, werden Anfragen auf die Kopie der Software und Kunden Daten im backup Datencenter umgeleitet. Zu jedem Zeitpunkt dürfen Kundendaten in die primäre oder die Sicherung Datacenter verarbeitet werden. Verteilen von Daten für mehrere Rechenzentren reduziert die betroffene Oberfläche für den Fall, dass ein Rechenzentrum Angriff ist. Darüber hinaus die Dienste in der betroffenen Datacenter können schnell umgeleitet werden auf dem sekundären Rechenzentrum als eines der Mechanismen für die Wiederherstellung und umgekehrt umgeschaltet (umgeleitet zurück in das primäre Datencenter, nachdem der Dienst wiederhergestellt wird).

Einzelne Arbeitslasten enthalten integrierte Features, die Ressourcenverwendung verwalten. Beispielsweise sind die Einschränkung Mechanismen in Exchange Online und SharePoint Online Bestandteil einer mehrstufigen Ansatz für die Verteidigung gegen DoS-Angriffe. Drosselung für Exchange Online-Benutzern basiert auf der Ebene der Identitätsdaten durch den Endbenutzer-Ressourcen, ob die Ressourcen in Active Directory, Exchange Online Informationsspeicher oder einer anderen Stelle befinden. Ein Budget ist jeder Client begrenzen die Ressourcen verbraucht von einem Benutzer zugewiesen. Exchange Online für Benutzer Aktivität und Systemkomponenten Einschränkung basiert auf [Workload Management](http://technet.microsoft.com/en-us/library/jj150503(v=exchg.150).aspx). Eine Exchange Online-Arbeitslast ist ein Exchange Online-Feature, Protokoll oder Dienst, der aus Gründen der Exchange Online System Ressourcenmanagement explizit definiert wurde. Jeder Exchange Online-Arbeitslast benötigt Systemressourcen wie CPU, Datenbankvorgänge Postfach, oder Active Directory oder Hintergrund Arbeit ausführen Benutzeranfragen anfordert. Beispiele für Exchange Online Arbeitslasten sind Outlook auf dem Web, Exchange ActiveSync, Migration von Postfächern und Postfach-Assistenten. Mandantenadministratoren können die Exchange-arbeitsauslastungsverwaltung begrenzungseinstellungen für Benutzer mit der Exchange-Verwaltungsshell verwalten. Es gibt verschiedene Formen der Einschränkung, die in Exchange Online, einschließlich PowerShell, Exchange-Webdienste und POP und IMAP, Exchange ActiveSync, Mobilgerät Verbindungen, Empfänger und vieles mehr implementiert wurden. Obwohl Administratoren des lokalen Exchange-Bereitstellungen einschränkungsrichtlinien konfigurieren, können Administratoren nicht einschränkungsrichtlinien für Exchange Online konfigurieren.

Der am häufigsten verwendete Trigger für Drosselungen in SharePoint Online ist-Objekt mithilfe der clientseitigen Objektmodell (CSOM) Code, der mit einer hoch Häufigkeit zu viele Aktionen ausführt. Mit CSOM können alle Vorgänge, die mit einer einzelnen Anforderung, die Einschränkungen überschreiten und verursachen Einschränkung pro Benutzer können ausgeführt werden.

Unabhängig von der Aktivität möglicherweise die Einschränkung, wenn ein Benutzer Einschränkungen, SharePoint Online eine weitere Anforderungen von dieses Benutzerkontos in der Regel für einen kurzen Zeitraum Drosselungen überschreitet. Während einer Throttle Benutzer aktiviert ist, werden alle Aktionen, die von diesem Benutzer gedrosselt, bis der Drosselung, gemäß der folgenden Kriterien abläuft:
- Anforderungen, die vom Benutzer direkt im Browser ausgeführt werden SharePoint Online leitet zu einer Informationsseite der Drosselung und die Anforderungen fehl.
- Für alle Anfragen CSOM-Aufrufe, einschließlich SharePoint Online HTTP-Statuscode 429 ("zu viele Anfragen") zurück, und die Anforderungen fehl.

Wenn der problematische Prozess Usage Grenzwerte überschreitet weiterhin, SharePoint Online möglicherweise vollständig blockieren den Prozess und HTTP-Statuscode 503 ("Dienst nicht verfügbar") zurückgegeben.

## <a name="vulnerability-and-penetration-testing"></a>Sicherheitsrisiko und Durchdringungstests
Microsoft verwendet viele [sicherheitstechnologien und Methoden](https://www.microsoft.com/en-us/trustcenter/security/threatmanagement) [zum Schutz der Cloud-Infrastruktur](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) und lokale Netzwerke gegen Bedrohungen für moderne, anspruchsvolle, einschließlich der Verwendung von Modul-Komponenten und Dienste für virtuelle Cloud services Computern (VMs) und anderen Systemen; Erweiterte Threat-Analyse, die überwacht normalen Verwendungsmuster für Netzwerke, Systeme und Benutzer und Computer lernen, wie Sie jedes Verhalten zu kennzeichnen, die die menschliche Stimme und regulären Durchdringungstests ist beschäftigt.

Zusätzlich zu unserer eigenen Penetration Tests durchführen und unsere Kunden ein [Programm Microsoft Cloud Unified Durchdringungstests](https://technet.microsoft.com/en-us/mt784683)anbieten, wir auch zur Kontaktaufnahme mit Drittanbieter-Security-Experten, die regulären bei der Bewertung von ausführen und Durchdringungstests gegen unsere Clouddienste. Wir stellen die Berichte aus dieser Drittanbieter-bei der Bewertung aus dem [Dienst vertrauen](https://aka.ms/STP) und die [Service Assurance](https://aka.ms/ServiceAssurance) Portale zum Download zur Verfügung.

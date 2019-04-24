---
title: Office 365 Datenvernichtung
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
description: Eine Übersicht über die Microsoft-Richtlinien hinsichtlich der Wiederverwendung, Beseitigung oder Zerstörung von Datenträgerlaufwerken und-Servern von Office 365 Datacenter.
ms.openlocfilehash: fec6065434fa9fa555a057c68eca60082225652c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262907"
---
# <a name="office-365-data-destruction"></a>Office 365 Datenvernichtung

## <a name="physical-data-destruction"></a>Physikalische Datenvernichtung

Microsoft verfügt über Standard Richtlinien für die Datenverarbeitung, die die Wiederverwendung und Entsorgung von Festplatten und fehlgeschlagenen oder abruhestands Servern angehen. Vor der Wiederverwendung von Festplattenlaufwerken in Office 365 führt Microsoft eine physikalische Desinfektion aus, die mit dem nationalen Institut für Standard-und technologiespezifische Veröffentlichung 800-88 ([NIST SP 800-88 Guidelines for Media Sanitized](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) ) konsistent ist. ). Alle Festplatten in Office 365 werden mit der BitLocker-Verschlüsselung auf Volume-Ebene verschlüsselt, daher ist in der Praxis das NIST SP 800-88-konforme löschen nicht erforderlich. Dennoch wird es weiterhin von Microsoft ausgeführt.

Fehlerhafte Datenträger, die in Office 365-Rechenzentren verwendet werden, werden physisch zerstört und über den ISO-Prozess überwacht. Die geeigneten Entsorgungsmethoden werden durch den Objekttyp bestimmt. Bei Festplatten, die nicht gelöscht werden können, verwendet Microsoft einen Vernichtungsprozess, der die Medien zerstört (beispielsweise zerfällt, pulverisiert oder verbrennt) und die Wiederherstellung von Informationen unmöglich macht. Microsoft behält auch alle Datensätze der Zerstörung bei. Microsoft führt einen ähnlichen Prozess der Desinfektion auf Servern durch, die in Office 365 wieder verwendet werden. Diese Richtlinien umfassen sowohl elektronische als auch physische Desinfektion.

Festplatten, die nicht wieder verwendet werden können, werden mit einem physischen Vernichtungsprozess verworfen, der im Rechenzentrum mit den zu zerstörten Datenträgern vor Ort ausgeführt wird. Für die Entsorgung vorgesehene Speichermedien werden in sicheren bins platziert, die sich in jedem Bereich des Datencenters befinden. Jede Secure bin-Station wird durch Videoüberwachung überwacht. Sobald ein Entsorgungs Schacht ungefähr 50% der Kapazität erreicht, kontaktiert das Standortdienst Team das physische Sicherheitsteam, um die Entfernung zu koordinieren. Website-Dienstmitarbeiter entfernen dann den Entsorgungs Schacht unter Escort von einem Sicherheitsbeamten, bis er in einem geschützten Speicherbereich befindet, um die Datenvernichtung abzuwarten. Die Richtlinien und Verfahren für die Handhabung von Datenträger Geräten während der Entsorgung werden routinemäßig getestet, einschließlich Verfahren zur Sicherstellung des Zustands der für die Vernichtung zugelassenen Maschinen.

Beim datenzerstörungs Prozess wird der Datenträger zunächst auf eine Weise gelöscht, die mit NIST 800-88 (wenn möglich) kompatibel ist, und dann in einen industriellen Shredder versetzt und physisch abgerissen. Microsoft behält die Verantwortlichkeit für Objekte bei, die das Rechenzentrum mit NIST SP 800-88 konsistente Säuberung/Bereinigung, Zerstörung von Objekten, Verschlüsselung, exakte Inventur, Verfolgung und Schutz der Chain of Custody während des Transports verlassen. Dieser Prozess wird über das Closed-Circuit-Fernsehen überwacht, und nach Abschluss des Verfahrens wird ein Vernichtungs Zertifikat ausgestellt.

Microsoft verwendet Daten Löschungs Einheiten aus dem Bereich [Extreme Protocol Solutions](http://www.enterprisedataerasure.com/) (EPS). EPS-Software unterstützt die NIST-SP 800-88-Anforderungen für die Bereinigung und Bereinigung/sicheres Löschen. Vor der Bereinigung oder Zerstörung wird ein Inventar vom Microsoft Asset Manager erstellt. Wenn ein Lieferant für die Zerstörung verwendet wird, stellt der Lieferant ein Vernichtungs Zertifikat für jedes zerstörte Objekt bereit, das vom Vermögensverwalter validiert wird.

## <a name="virtual-data-destruction"></a>Virtuelle Datenvernichtung

Microsoft verfügt über Richtlinien und Verfahren für die Datenverarbeitung, die auch eine effektive virtuelle Zerstörung von Daten behandeln, um die Möglichkeit zu schützen, dass Daten ungeeignet zwischen Dienst Mandanten freigegeben werden oder nach einem harten löschen im Dienst zugänglich sind. Daten, die in einem Mandanten aus dem Dienst gelöscht werden, können nicht für einen anderen Dienst Mandanten zugänglich sein, auch wenn einige oder alle desselben zugrunde liegenden physikalischen Speichers später erneut zugewiesen werden. Dies ist ein Ergebnis der zusammengestellten Auswirkungen mehrerer Virtualisierungs-und Fragmentierungs Technologien, die zum Skalieren virtueller Umgebungen verwendet werden, die aktiven Löschverhalten von Anwendungen innerhalb der einzelnen Dienst Mandanten (beispielsweise das [unwiderrufliche](https://docs.microsoft.com/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)löschen) und die erforderlichen Medien-und Anwendungsinhalts Verschlüsselungsprozesse.
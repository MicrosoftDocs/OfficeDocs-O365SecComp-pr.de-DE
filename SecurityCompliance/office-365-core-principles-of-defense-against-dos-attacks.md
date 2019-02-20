---
title: Office 365-Grundprinzipien der Verteidigung gegen Denial-of-Service-Angriffe
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Wie Microsoft die Kernprinzipien der Absorption, der Erkennung und der Schadensminimierung bei der Abwehr von DoS-Angriffen (Denial-of-Service) nutzt.
ms.openlocfilehash: 17dc583258cdb4781dbe2a715e1ce153ee769ed3
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091007"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen

Die drei Hauptprinzipien bei der Verteidigung gegen netzwerkbasierte DoS-Angriffe sind Absorption, Erkennung und Minderung. Die Absorption geschieht vor der Erkennung, und die Erkennung geschieht vor der Minderung. Absorption ist die beste Verteidigung gegen DoS-Angriffe. Wenn der Angriff nicht erkannt werden kann, kann er nicht abgemildert werden. Aber wenn auch der kleinste DoS-Angriff nicht absorbiert werden kann, werden die Dienste nicht lange genug überleben, damit der Angriff erkannt wird.

Natürlich ist es für die meisten Organisationen in der Regel nicht praktikabel, die Überkapazitäten zu erwerben, die zur Aufnahme von DoS-Angriffen erforderlich sind, da dies beträchtliche Investitionen in Technologie und technische Fähigkeiten erfordert. Dies weist auf einen der Sicherheitsvorteile der Verwendung von Microsoft Cloud Services hin. die schiere Skala unserer Dienste ermöglicht es uns, unseren Cloud-Kunden einen hohen Netzwerkschutz auf kosteneffektive Weise zu bieten. Doch selbst in unserem Umfang muss es dennoch ein Gleichgewichtzwischen Absorption, Erkennung und Minderung geben. Um diese Balance zu finden, untersuchen wir die Wachstumsrate eines Angriffs, um zu ermitteln, wie viel wir absorbieren müssen.

Erkennung ist ein Katz-und-Maus-Spiel. Sie müssen ständig nach den neuen Methoden suchen, über die Benutzer sie angreifen, oder um Ihre Systeme zu besiegen. Die >-abSchwächung – >->-Minderung usw. ist ein dauerhafter, beständiger Zustand, der unbegrenzt fortgesetzt wird.

## <a name="defending-against-dos-attacks"></a>Abwehr von DoS-anGriffen

Um einen DoS-Angriff erfolgreich zu verteidigen, ist eine frühzeitige Erkennung unerlässlich. Durch das Aufspüren eines Angriffs, bevor das System überlastet ist, können Defenders einen Reaktionsplan ausführen.

Die folgende Formel hilft bei der Annäherung der Zeit bis zur Auswirkung eines DoS-Angriffs:

   **Maximale Kapazität (in Bytes/Sek.)/Wachstums Rate (in Byte/Sek.) = Zeit bis zum Aufprall (in Byte/Sek.)**

Wenn die Zeit-bis-Erkennung nach der Zeit-zu-Auswirkung auftritt, ist es wahrscheinlich, dass der DoS-Angriff erfolgreich ist. Wenn die Zeit-bis-Erkennung vor der Zeit-zu-Auswirkung auftritt, sollten die angegriffenen Dienste online bleiben und zugänglich sein, wenn Minderungsstrategien verwendet werden. Daher gibt es nur zwei Dinge, die zur Abwehr von DoS-Angriffen ausgeführt werden können:
- Erhöhen Sie die Kapazität, um die Obergrenze für die maximale Kapazität zu erhöhen (was wiederum mehr Zeit für die Ermittlung eines Angriffs bietet). oder
- Verringern Sie die Erkennungszeit.

Die Erhöhung der Kapazität hat direkte fiskalische Auswirkungen. Microsoft empfiehlt, dass Kunden mindestens eine grundlegende Absorptionskapazität entwickeln, um sicherzustellen, dass Sie ein gewisses Maß an DoS-Angriffen überstehen können. Die tatsächliche Absorptionskapazität ist von Kunden zu Kunden unterschiedlich, da jeder Kunde eigene Schwellenwerte für Exposition, Risiko und finanziellen Aufwand hat. Aus wirtschaftlichen Gründen sind Investitionen in Forschung und Zeit in der Regel die kostengünstigste Verteidigungsmethode.

---
title: Office 365 Kernprinzipien der Abwehr von Denial-of-Service-Angriffen
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
description: Wie Microsoft die Kernprinzipien der Absorption, Erkennung und Minderung bei der Abwehr von DOS-Angriffen (Denial of Service) verwendet.
ms.openlocfilehash: 48ed52b496a3288d62b0f0c434fe18df8e1ff44b
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622295"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen

Die drei Hauptprinzipien bei der Verteidigung gegen netzwerkbasierte DOS-Angriffe sind Absorption, Erkennung und Minderung. Die Absorption erfolgt vor der Erkennung, und die Erkennung erfolgt vor der Minderung. Absorption ist die beste Verteidigung gegen einen DOS-Angriff. Wenn der Angriff nicht erkannt werden kann, kann er nicht gemindert werden. Wenn aber selbst der kleinste DOS-Angriff nicht absorbiert werden kann, werden Dienste nicht lange genug überleben, damit der Angriff erkannt wird.

Für die meisten Organisationen ist es nicht wirtschaftlich möglich, überschüssige Kapazitäten für die Aufnahme von DOS-Angriffen zu erwerben, da dies erhebliche Investitionen in Technologie und technische Fertigkeiten erfordert. Dies zeigt einen der Sicherheitsvorteile der Verwendung von Microsoft Cloud Services. Die schiere Skalierung von Microsoft-Diensten bietet Cloud-Kunden einen starken Netzwerkschutz auf kosteneffektive Weise. Aber selbst im großen Maßstab muss es ein Gleichgewichtzwischen Absorption, Erkennung und Minderung geben. Um dieses Gleichgewicht zu finden, untersucht Microsoft die Angriffs Raten, um abzuschätzen, wie viel Microsoft absorbieren muss.

Die Erkennung ist ein Katz-und-Maus-Spiel. Sie müssen ständig nach neuen Wegen suchen, die Menschen angreifen und versuchen, ihre Systeme zu besiegen. "Detect-#a0 mindern-#a1 Detect-#a2 mindern usw. ist ein dauerhafter, persistenter Status, der unbegrenzt fortgesetzt wird.

## <a name="defending-against-dos-attacks"></a>Abwehr von DOS-Angriffen

Um eine erfolgreiche Abwehr von DOS-Angriffen zu erhalten, ist eine frühzeitige Erkennung unerlässlich. Wenn ein Angriff erkannt wird, bevor das System überlastet ist, können Verteidiger einen Antwort Plan ausführen.

Die folgende Formel hilft, die Zeit bis zur Auswirkung eines DoS-Angriffs näher zu befolgen:

   **Maximale Kapazität (in Bytes/Sek.)/Zuwachs Rate (in Bytes/s) = Zeit bis zur Auswirkung (in Bytes/s)**

Wenn die Zeit-zu-Erkennung nach einer Zeit-zu-Wirkung auftritt, ist es wahrscheinlich, dass der DOS-Angriff erfolgreich sein wird. Wenn die Zeit-zu-Erkennung vor Zeit-zu-Wirkung auftritt, sollten die angegriffenen Dienste Online und zugänglich bleiben, wenn Minderungsstrategien verwendet werden. Daher gibt es nur zwei Dinge, die zur Abwehr von DOS-Angriffen ausgeführt werden können:

- Erhöhen der Kapazität zur Anhebung der Obergrenze der maximalen Kapazität (was wiederum mehr Zeit zum Erkennen eines Angriffs bietet); oder
- Verringern Sie die zu erkennende Zeit.

Die zunehmende Kapazität hat eine direkte steuerliche Auswirkung. Microsoft empfiehlt, dass Kunden mindestens die grundlegende Absorptionskapazität entwickeln, um sicherzustellen, dass Sie einen gewissen Grad an DOS-Angriffen überleben können. Die tatsächliche Absorptionskapazität variiert von Kunde zu Kunde, da jeder Kunde über eigene Schwellenwerte für Belichtung, Risiko und finanziellen Aufwand verfügt. Aus wirtschaftlichen Gründen sind Investitionen in Forschung und Zeit für Methoden zur Verringerung der Zeit-zu-Erkennung in der Regel die kostengünstigste Verteidigung.

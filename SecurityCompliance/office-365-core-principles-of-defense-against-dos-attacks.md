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
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="357e3-103">Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="357e3-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>

<span data-ttu-id="357e3-p101">Die drei Hauptprinzipien bei der Verteidigung gegen netzwerkbasierte DoS-Angriffe sind Absorption, Erkennung und Minderung. Die Absorption geschieht vor der Erkennung, und die Erkennung geschieht vor der Minderung. Absorption ist die beste Verteidigung gegen DoS-Angriffe. Wenn der Angriff nicht erkannt werden kann, kann er nicht abgemildert werden. Aber wenn auch der kleinste DoS-Angriff nicht absorbiert werden kann, werden die Dienste nicht lange genug überleben, damit der Angriff erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="357e3-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="357e3-p102">Natürlich ist es für die meisten Organisationen in der Regel nicht praktikabel, die Überkapazitäten zu erwerben, die zur Aufnahme von DoS-Angriffen erforderlich sind, da dies beträchtliche Investitionen in Technologie und technische Fähigkeiten erfordert. Dies weist auf einen der Sicherheitsvorteile der Verwendung von Microsoft Cloud Services hin. die schiere Skala unserer Dienste ermöglicht es uns, unseren Cloud-Kunden einen hohen Netzwerkschutz auf kosteneffektive Weise zu bieten. Doch selbst in unserem Umfang muss es dennoch ein Gleichgewichtzwischen Absorption, Erkennung und Minderung geben. Um diese Balance zu finden, untersuchen wir die Wachstumsrate eines Angriffs, um zu ermitteln, wie viel wir absorbieren müssen.</span><span class="sxs-lookup"><span data-stu-id="357e3-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="357e3-p103">Erkennung ist ein Katz-und-Maus-Spiel. Sie müssen ständig nach den neuen Methoden suchen, über die Benutzer sie angreifen, oder um Ihre Systeme zu besiegen. Die >-abSchwächung – >->-Minderung usw. ist ein dauerhafter, beständiger Zustand, der unbegrenzt fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="357e3-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="357e3-116">Abwehr von DoS-anGriffen</span><span class="sxs-lookup"><span data-stu-id="357e3-116">Defending Against DoS Attacks</span></span>

<span data-ttu-id="357e3-p104">Um einen DoS-Angriff erfolgreich zu verteidigen, ist eine frühzeitige Erkennung unerlässlich. Durch das Aufspüren eines Angriffs, bevor das System überlastet ist, können Defenders einen Reaktionsplan ausführen.</span><span class="sxs-lookup"><span data-stu-id="357e3-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="357e3-119">Die folgende Formel hilft bei der Annäherung der Zeit bis zur Auswirkung eines DoS-Angriffs:</span><span class="sxs-lookup"><span data-stu-id="357e3-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="357e3-120">**Maximale Kapazität (in Bytes/Sek.)/Wachstums Rate (in Byte/Sek.) = Zeit bis zum Aufprall (in Byte/Sek.)**</span><span class="sxs-lookup"><span data-stu-id="357e3-120">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in bytes/sec)**</span></span>

<span data-ttu-id="357e3-p105">Wenn die Zeit-bis-Erkennung nach der Zeit-zu-Auswirkung auftritt, ist es wahrscheinlich, dass der DoS-Angriff erfolgreich ist. Wenn die Zeit-bis-Erkennung vor der Zeit-zu-Auswirkung auftritt, sollten die angegriffenen Dienste online bleiben und zugänglich sein, wenn Minderungsstrategien verwendet werden. Daher gibt es nur zwei Dinge, die zur Abwehr von DoS-Angriffen ausgeführt werden können:</span><span class="sxs-lookup"><span data-stu-id="357e3-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="357e3-124">Erhöhen Sie die Kapazität, um die Obergrenze für die maximale Kapazität zu erhöhen (was wiederum mehr Zeit für die Ermittlung eines Angriffs bietet). oder</span><span class="sxs-lookup"><span data-stu-id="357e3-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="357e3-125">Verringern Sie die Erkennungszeit.</span><span class="sxs-lookup"><span data-stu-id="357e3-125">Decrease the time to detect.</span></span>

<span data-ttu-id="357e3-p106">Die Erhöhung der Kapazität hat direkte fiskalische Auswirkungen. Microsoft empfiehlt, dass Kunden mindestens eine grundlegende Absorptionskapazität entwickeln, um sicherzustellen, dass Sie ein gewisses Maß an DoS-Angriffen überstehen können. Die tatsächliche Absorptionskapazität ist von Kunden zu Kunden unterschiedlich, da jeder Kunde eigene Schwellenwerte für Exposition, Risiko und finanziellen Aufwand hat. Aus wirtschaftlichen Gründen sind Investitionen in Forschung und Zeit in der Regel die kostengünstigste Verteidigungsmethode.</span><span class="sxs-lookup"><span data-stu-id="357e3-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>

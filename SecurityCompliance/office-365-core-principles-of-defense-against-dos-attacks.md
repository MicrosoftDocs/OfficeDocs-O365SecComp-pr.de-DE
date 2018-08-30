---
title: Office 365 Core Prinzipien Schutz vor Denial-of-Service-Angriffen
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
description: Microsoft nutzt wie die wesentlichen Prinzipien der Übernahme, Erkennung und Risikominderung in seiner Schutz vor Denial-of-Service (DoS)-Angriffen.
ms.openlocfilehash: 8355a7897c788241092363a23e198423e81c587a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528846"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="e69cf-103">Wesentliche Prinzipien Schutz vor Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="e69cf-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>
<span data-ttu-id="e69cf-p101">Die drei core Prinzipien bei der Verteidigung gegen DoS Netzwerkangriffen Übernahme, Erkennung und Risikominderung sind. Übernahme geschieht vor der Erkennung und Erkennung vor Risikominderung zufällig. Übernahme ist die beste Verteidigung gegen DoS-Angriffe. Wenn der Angriff kann nicht erkannt werden, kann nicht es gemindert werden. Aber wenn der kleinste DoS-Angriff kann nicht aufgenommen werden, klicken Sie dann Dienste sind nicht lange genug für den Angriff erkannt werden überstehen.</span><span class="sxs-lookup"><span data-stu-id="e69cf-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="e69cf-p102">Natürlich ist es im Allgemeinen nicht wirtschaftlich für die meisten Organisationen die überzählige Kapazität erforderlich sind, um kompensieren DoS-Angriffen, wie dies eine bedeutende Investition in Technologie und technische Kenntnisse erfordert erwerben. Dadurch wird hervorgehoben, einer der Vorteile der Verwendung von Microsoft Cloud Services Security; die reine Skala unserer Dienste kann wir starken Schutz des Kunden Cloud kostengünstige Weise bereitstellen. Aber auch in unseren Skalierung jedoch weiterhin muss ein Gleichgewicht zwischen Übernahme, Erkennung und Risikominderung. Um diese Gleichgewicht zu finden, untersuchen wir ein Angriff Wachstum, um wie viel müssen wir kompensieren zu prognostizieren.</span><span class="sxs-lookup"><span data-stu-id="e69cf-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="e69cf-p103">Erkennung ist ein Katz-und-Maus-Spiel. Sie müssen ständig nachsehen für die neue Kommunikationsmethoden der Mitarbeiter sind oder Angriffe auf Sie versuchen, die Systeme überwinden. Erkennen-mindern > erkennen -> -> mindern usw., ist ein unbefristet, permanente Zustand, die unbestimmte Zeit fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e69cf-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="e69cf-116">Verteidigung gegen DoS-Angriffen</span><span class="sxs-lookup"><span data-stu-id="e69cf-116">Defending Against DoS Attacks</span></span>
<span data-ttu-id="e69cf-p104">Um erfolgreich Verteidigung gegen einen DoS-Angriff, unbedingt frühzeitige Erkennung. Angriff erkennen, bevor das System überlastet ist, können Verteidiger ein Reaktionsplans ausführen.</span><span class="sxs-lookup"><span data-stu-id="e69cf-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="e69cf-119">Die folgende Formel hilft ungefähre die Zeit für einen DoS-Angriff auswirken:</span><span class="sxs-lookup"><span data-stu-id="e69cf-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="e69cf-120">**Maximale Kapazität / (bewerten Sie Wachstum der maximalen Kapazität X) = Zeit zu Auswirkung**</span><span class="sxs-lookup"><span data-stu-id="e69cf-120">**Maximum Capacity / (Maximum Capacity X Growth Rate) = Time to Impact**</span></span>

<span data-ttu-id="e69cf-p105">Wenn die Erkennung Zeit nach Zeit Auswirkungen, auftritt, ist es wahrscheinlich wird der DoS-Angriff erfolgreich ist. Erfolgt die Erkennung Zeit vor der Zeit-Auswirkungen, sollte die Dienste angegriffenen bleiben online und zugegriffen werden, wenn Strategien zur Risikominderung verwendet werden. Daher nur zwei Dinge, die ausgeführt werden können, um die Abwehr von DoS-Angriffen:</span><span class="sxs-lookup"><span data-stu-id="e69cf-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="e69cf-124">Erhöhen der Kapazität die Obergrenze der maximalen Kapazität auslösen (die wiederum mehr Zeit zum Erkennen von Angriff bereitstellt); oder</span><span class="sxs-lookup"><span data-stu-id="e69cf-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="e69cf-125">Verringern Sie die Zeit, um zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="e69cf-125">Decrease the time to detect.</span></span>

<span data-ttu-id="e69cf-p106">Erhöhen der Kapazität wirkt sich direkt Geschäftszeiträume. Microsoft empfiehlt, dass Kunden mindestens grundlegende Übernahme entwickeln Kapazität, um sicherzustellen, dass sie gewisse DoS-Angriff überstehen können. Die tatsächlichen Übernahme Kapazität wird Kunden, hängt von jedem Kunden ihre eigenen Schwellenwerte für Risiko, Risiken und finanziellen Lösungsanbieter hat. Letztlich sind wirtschaftlichen Gründen Investitionen von Research und die Uhrzeit auf Weise zum Verringern der Zeit-Erkennung in der Regel die kostengünstigste Verteidigung.</span><span class="sxs-lookup"><span data-stu-id="e69cf-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>

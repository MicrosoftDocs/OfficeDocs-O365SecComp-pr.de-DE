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
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Wesentliche Prinzipien Schutz vor Denial-of-Service-Angriffen
Die drei core Prinzipien bei der Verteidigung gegen DoS Netzwerkangriffen Übernahme, Erkennung und Risikominderung sind. Übernahme geschieht vor der Erkennung und Erkennung vor Risikominderung zufällig. Übernahme ist die beste Verteidigung gegen DoS-Angriffe. Wenn der Angriff kann nicht erkannt werden, kann nicht es gemindert werden. Aber wenn der kleinste DoS-Angriff kann nicht aufgenommen werden, klicken Sie dann Dienste sind nicht lange genug für den Angriff erkannt werden überstehen.

Natürlich ist es im Allgemeinen nicht wirtschaftlich für die meisten Organisationen die überzählige Kapazität erforderlich sind, um kompensieren DoS-Angriffen, wie dies eine bedeutende Investition in Technologie und technische Kenntnisse erfordert erwerben. Dadurch wird hervorgehoben, einer der Vorteile der Verwendung von Microsoft Cloud Services Security; die reine Skala unserer Dienste kann wir starken Schutz des Kunden Cloud kostengünstige Weise bereitstellen. Aber auch in unseren Skalierung jedoch weiterhin muss ein Gleichgewicht zwischen Übernahme, Erkennung und Risikominderung. Um diese Gleichgewicht zu finden, untersuchen wir ein Angriff Wachstum, um wie viel müssen wir kompensieren zu prognostizieren.

Erkennung ist ein Katz-und-Maus-Spiel. Sie müssen ständig nachsehen für die neue Kommunikationsmethoden der Mitarbeiter sind oder Angriffe auf Sie versuchen, die Systeme überwinden. Erkennen-mindern > erkennen -> -> mindern usw., ist ein unbefristet, permanente Zustand, die unbestimmte Zeit fortgesetzt wird.

## <a name="defending-against-dos-attacks"></a>Verteidigung gegen DoS-Angriffen
Um erfolgreich Verteidigung gegen einen DoS-Angriff, unbedingt frühzeitige Erkennung. Angriff erkennen, bevor das System überlastet ist, können Verteidiger ein Reaktionsplans ausführen.

Die folgende Formel hilft ungefähre die Zeit für einen DoS-Angriff auswirken:

   **Maximale Kapazität / (bewerten Sie Wachstum der maximalen Kapazität X) = Zeit zu Auswirkung**

Wenn die Erkennung Zeit nach Zeit Auswirkungen, auftritt, ist es wahrscheinlich wird der DoS-Angriff erfolgreich ist. Erfolgt die Erkennung Zeit vor der Zeit-Auswirkungen, sollte die Dienste angegriffenen bleiben online und zugegriffen werden, wenn Strategien zur Risikominderung verwendet werden. Daher nur zwei Dinge, die ausgeführt werden können, um die Abwehr von DoS-Angriffen:
- Erhöhen der Kapazität die Obergrenze der maximalen Kapazität auslösen (die wiederum mehr Zeit zum Erkennen von Angriff bereitstellt); oder
- Verringern Sie die Zeit, um zu erkennen.

Erhöhen der Kapazität wirkt sich direkt Geschäftszeiträume. Microsoft empfiehlt, dass Kunden mindestens grundlegende Übernahme entwickeln Kapazität, um sicherzustellen, dass sie gewisse DoS-Angriff überstehen können. Die tatsächlichen Übernahme Kapazität wird Kunden, hängt von jedem Kunden ihre eigenen Schwellenwerte für Risiko, Risiken und finanziellen Lösungsanbieter hat. Letztlich sind wirtschaftlichen Gründen Investitionen von Research und die Uhrzeit auf Weise zum Verringern der Zeit-Erkennung in der Regel die kostengünstigste Verteidigung.

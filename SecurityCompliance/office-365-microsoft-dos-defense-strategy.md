---
title: Von Microsoft Office 365 DoS mehrstufigen Strategie
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
description: Eine Übersicht über Microsoft mehrstufigen Strategie für den Umgang mit Denial-of-Service (DoS) Angriffe.
ms.openlocfilehash: f172db5080ef73402c7e9bc61720eb0f87e844ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528854"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Microsoft Defense Denial-of-Service-Strategie

Microsoft Strategie für den Schutz vor Denial-of-Service (DoS) Netzwerkangriffen ist aufgrund von unseren Skalierung und globale etwas eindeutig. Diese Skala kann Microsoft nutzen, Strategien und Techniken, die einige Organisationen (Anbieter oder Kunden Organisationen) entsprechen können. Das Herzstück unserer DoS-Strategie ist unsere globale Präsenz nutzen. Microsoft beauftragt mit Internet-Anbieter, Peers Anbieter (öffentliche und Private) und Private Unternehmen auf der ganzen Welt erteilen uns eine erhebliche Internetpräsenz (die derzeit, um alle 18 Monate verdoppelt). Große Anwesenheitsstatus müssen mit der Microsoft Angriffe über eine sehr umfangreiche Oberfläche kompensieren.

Unsere Einzigartigkeit angegeben, verwendet Microsoft Erkennung und Risikominderung Prozesse, die von denen von großen Unternehmen abweichen. Unsere Strategie basiert auf eine Trennung der Erkennung und Risikominderung sowie globalen, verteilten Risikominderung durch unsere viele Ränder. Viele Unternehmen verwenden Drittanbieterlösungen die erkennen und Abwehren von Angriffen am Rand. Mit der zunehmenden unsere Kapazität Edge wurde, wurde klar, dass die Bedeutung von jeder Angriffen auf einzelne oder bestimmte Kanten sehr niedrig war. Aufgrund von unseren eindeutige Konfiguration haben wir die Erkennung und Risikominderung Komponenten aufgeteilt. Wir haben mehrstufige Erkennung bereitgestellt, die wir näher Angriffe auf ihre Sättigung Punkt Beibehaltung globale Risikominderung am Rand erkennen können. Diese Strategie wird sichergestellt, dass wir mehrere gleichzeitige Angriffe verarbeitet werden können.

Eines der effektiv und kostengünstige Verteidigung angestellt Microsoft DoS-Angriffen ist unsere Angriffsfläche reduziert wird. Auf diese Weise kann wir unerwünschten Datenverkehr am Rand, im Gegensatz zu analysieren, Verarbeitung und bereinigen den Daten Inline ablegen.

An der Schnittstelle mit dem öffentlichen Netzwerk verwendet Microsoft Security spezieller Geräte für Firewall, NAT und IP-Filterung Funktionen. Wir verwenden auch routing globalen gleich-Kosten mit mehreren Pfad (ECMP). Globale ECMP-routing ist ein Netzwerk-Framework, das wird, dass es sind mehrere globale Pfade sichergestellt zu einen Dienst zu erreichen. Dank dieser mehreren Pfaden sein ein Angriff auf den Dienst, um den Bereich aus dem Angriff stammt – andere Regionen sollten von diesem Angriff nicht betroffen sein, wie Endbenutzer andere Pfade zum Erreichen des Dienstes in diesen Regionen verwenden würden. Wir haben auch unsere eigenen interne DoS Korrelation und Erkennung System entwickelt, das Ablauf der Daten, die Leistungsmetriken und andere Informationen verwendet wird. Dies ist eine Hyperscale Cloud-Dienst in Microsoft Azure die auf verschiedenen Stellen in Microsoft-Netzwerken erfasste Daten analysiert ausgeführt und Dienste. Ein Cross-Arbeitslast DoS Vorfällen Team identifiziert die Rollen und Aufgaben für Teams, die Kriterien für eskalieren und die Protokolle für die verschiedenen Teams ansprechender und für den Umgang mit Vorfällen. Diese Lösungen zwischengeschalteter Batterie bietet Schutz vor DoS-Angriffen-basierten Netzwerk.

Schließlich Cloud-basierten Arbeitslasten mit optimierten basierend auf ihren Protokoll Schwellenwerte konfiguriert sind, und Auslastung der Bandbreite benötigt, um diese Arbeitslast eindeutig zu schützen.

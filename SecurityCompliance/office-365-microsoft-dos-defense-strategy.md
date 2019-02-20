---
title: Office 365 Microsoft-DoS-VerteidigungsStrategie
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über die Verteidigungsstrategie von Microsoft für den Umgang mit DoS-Angriffen (Denial-of-Service).
ms.openlocfilehash: 0b0cf20e6282c85ede05edda3979ae5a7295ac78
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090817"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Denial-of-Service-VerteidigungsStrategie von Microsoft

Die Strategie von Microsoft zum Schutz vor netzwerkbasierten Denial-of-Service-Angriffen (DoS) ist aufgrund unseres Umfangs und der globalen Präsenz etwas einzigartig. Mit dieser Skalierung kann Microsoft Strategien und Techniken nutzen, die nur wenige Organisationen (Anbieter oder Kundenorganisationen) abgleichen können. Der Eckpfeiler unserer DoS-Strategie besteht darin, unsere globale Präsenz zu nutzen. Microsoft engagiert sich mit Internetanbietern, Peering-Anbietern (öffentlich und privat) und privaten Unternehmen auf der ganzen Welt und gibt uns eine beträchtliche Internetpräsenz (die ab diesem schreiben alle 18 Monate verdoppelt). Eine solche große Präsenz ermöglicht es Microsoft, Angriffe über eine sehr große Oberfläche zu absorbieren.

Aufgrund unserer Einzigartigkeit verwendet Microsoft Erkennungs-und Minderungs Prozesse, die sich von den von Großunternehmen verwendeten unterscheiden. Unsere Strategie basiert auf einer Trennung von Erkennung und Minderung sowie globaler, verteilter Schadensbegrenzende Maßnahmen durch unsere vielen Edges. Viele Unternehmen verwenden Lösungen von Drittanbietern, mit denen Angriffe am Rande ermittelt und abgefedert werden. Als unsere Edge-Kapazität anwuchs, wurde deutlich, dass die Bedeutung eines Angriffs auf einzelne oder bestimmte Kanten sehr gering war. Aufgrund unserer einzigartigen Konfiguration haben wir die Komponenten zur Erkennung und Schadensminimierung getrennt. Wir haben mehrstufige Erkennung bereitgestellt, die es uns ermöglicht, Angriffen näher an Ihre Sättigungs Punkte zu erkennen und gleichzeitig globale Abschwächung am Rande beizubehalten. Diese Strategie stellt sicher, dass mehrere Angriffe gleichzeitig ausgeführt werden können.

Eine der effektivsten und kostengünstigsten Abwehrmaßnahmen von Microsoft gegen DoS-Angriffe besteht darin, unsere Angriffsfläche zu reduzieren. Auf diese Weise können wir unerwünschten Datenverkehr am Rand ablegen, statt die Daten Inline zu analysieren, zu verarbeiten und zu schrubben.

An der Schnittstelle mit dem öffentlichen Netzwerk verwendet Microsoft spezielle Sicherheitsgeräte für Firewall-, Netzwerkadressübersetzung-und IP-Filterfunktionen. Außerdem wird das globale equal-cost Multi-Path (ECMP)-Routing verwendet. Das globale ECMP-Routing ist ein Netzwerk Framework, das sicherstellt, dass mehrere globale Pfade vorhanden sind, um einen Dienst zu erreichen. Dank dieser mehreren Pfade sollte ein Angriff auf den Dienst auf die Region beschränkt werden, von der aus der Angriff stammt – andere Regionen sollten von diesem Angriff nicht betroffen sein, da Endbenutzer andere Pfade verwenden würden, um den Dienst in diesen Regionen zu erreichen. Außerdem haben wir ein eigenes internes DoS-Korrelations-und-Erkennungssystem entwickelt, das Fluss Daten, Leistungs Metriken und andere Informationen verwendet. Hierbei handelt es sich um einen hoch skalierten clouddienst, der in Microsoft Azure läuft und Daten aus verschiedenen Punkten in Microsoft-Netzwerken und-Diensten analysiert. Ein Aufgabenbereichs übergreifendes DoS-Reaktionsteam identifiziert die Rollen und Verantwortlichkeiten von Teams, die Kriterien für Eskalationen und die Protokolle für die Einbindung verschiedener Teams und für die Vorfallbehandlung. Diese Lösungen bieten netzwerkbasierten Schutz gegen DoS-Angriffe.

Schließlich werden Cloud-basierte Arbeitsauslastungen basierend auf dem Protokoll und der Bandbreitennutzung mit optimierten Schwellenwerten konfiguriert, um diese Arbeitslast eindeutig zu schützen.

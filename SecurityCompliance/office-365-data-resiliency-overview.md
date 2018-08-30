---
title: Ausfallsicherheit von Daten in Office 365
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
description: Grundlegendes zu datenflexibilität in Microsoft Office 365.
ms.openlocfilehash: 7d43c766615ff1520c6529427116c42795da8565
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529727"
---
# <a name="data-resiliency-in-office-365"></a>Ausfallsicherheit von Daten in Office 365

## <a name="introduction"></a>Einführung
Aufgrund die komplexe Natur von Cloud-computing ist Microsoft Beachten Sie, dass es keine Groß-/Kleinschreibung des Falls Dinge Fehler werden, sondern beim. Wir entwickeln unsere Clouddienste Zuverlässigkeit maximieren und minimieren die negativen Folgen für Kunden, wenn falsche Dinge tun. Wir außerhalb der traditionellen Strategie der komplexe physischen Infrastruktur der vertrauenden Seite verschoben haben, und wir haben Redundanz direkt in unsere Cloud Services integriert. Wir verwenden eine Kombination von weniger komplexen physischen Infrastruktur und intelligenter Software, der die ausfallsicherheit von Daten in unseren Services erstellt und liefert hohen Verfügbarkeit für den Kunden. 

## <a name="resiliency-and-recoverability-are-built-in"></a>Höhere Zuverlässigkeit und Wiederherstellbarkeit sind integriert. 
Erstellen von in höhere Zuverlässigkeit und Wiederherstellung beginnt mit der Annahme, die die zugrunde liegende Infrastruktur und Prozesse zu einem bestimmten Zeitpunkt ein Fehler auftritt,: Hardware (Infrastruktur) schlägt fehl, Menschen machen Fehler, und Software sind Fehler. Während es falsch wäre zu sagen, dass Softwareentwickler keine Gedanken folgende Punkte, bevor Sie die Cloud waren, wurde wie diese Probleme in einer normalen IT-Implementierung behandelt wurden sehr unterschiedliche vor der Cloud: 
- Erstens wurden Hardware und die Infrastruktur Schutzebenen erhebliche. Dies bedeutete Rechenzentren mit 99,99 % Zuverlässigkeit erforderlich erhebliche Leistung und Netzwerkredundanz mit und Servern mit hardwarebasierte clustering, zwei Netzteile, zwei Netzwerkschnittstellen und Ähnliches implementiert wurden. 
- Zweitens wurde Prozess bestehender. Betriebsteams verwaltet strenge Prozeduren, ändern, den Windows beschäftigt sind, und die häufig erhebliche Project der Verwaltungsaufwand reduziert ist. 
- Drittens stattgefunden Bereitstellung in einer Eisessig Tempo. Bereitstellen von Code ohne besitzt die Quelle bedeutete warten Patches und Hauptversion frei, Austausch von Beteiligten Hardware und erhebliche Aufwand. Darüber hinaus wurde die einzige Möglichkeit, ein Problem zu beheben, Rollback. Die meisten IT-Organisationen würden daher nur Hauptversionen die Arbeit auf dem neuesten Stand zur Vermeidung von bereitstellen. 
- Schließlich wurde die Skala bereitgestellten Systemen sowie die Ebene der ihre Vernetzung in der Vergangenheit viel kleiner als jetzt ist. 

Heute, Kunden erwarten Engagement von Microsoft ohne Beeinträchtigung der Medienqualität, und dies ist einer der Gründe, warum Microsoft Dienste und Software mit Flexibilität und Wiederherstellung im Hinterkopf erstellt werden. 

## <a name="office-365-data-resiliency-principles"></a>Office 365 Daten Resiliency Prinzipien 
Resiliency bezeichnet die Fähigkeit eines cloudbasierten Diensts aufnehmen bestimmte Arten von Fehlern und noch bleiben voll funktionsfähige aus Sicht des Kunden. Datenflexibilität bedeutet, dass unabhängig davon, welche Fehler in Office 365 auftreten, wichtige Kundendaten intakt und unverändert bleibt bleibt. Zu diesem Zweck entworfen Office 365-Dienste wurden auf fünf bestimmte Resiliency Prinzipien: 
- Kritische und nicht kritische Daten ist vorhanden. In seltenen Ausfallszenarien können (z. B., ob eine Nachricht gelesen wurde), nicht kritischen Daten gelöscht werden. Wichtige Daten (beispielsweise Kundendaten wie e-Mail-Nachrichten) sollte bei extreme Kosten geschützt werden. Als Design Ziel zugestellte e-Mail-Nachrichten sind immer äußerst wichtig, und z. B., ob eine Nachricht gelesen wurde ist nicht kritische. 
- Kopien von Kundendaten in verschiedenen Fehlertoleranz Zonen getrennt werden müssen oder wie viele Domänen wie möglich (z. B. Rechenzentren, zugänglich über Anmeldeinformationen für einmaliges (Prozess, Server oder -Operator)) fault, um fehlerisolierung bereitzustellen. 
- Wichtige Kundendaten müssen überwacht werden, für die einem beliebigen Teil des Unteilbarkeit, Konsistenz, Isolation, Dauerhaftigkeit (und), die Fehler aufweisen. 
- Kundendaten müssen eine Beschädigung geschützt werden. Es muss aktiv überprüften oder überwachten, repariert und wiederherstellbar sein. 
- Die meisten Data Loss Ergebnisse aus Aktionen des Kunden, also können Kunden wiederherstellen zur eigenen Verwendung eine Benutzeroberfläche, mit deren versehentlich gelöschte Elemente wiederherstellen kann. 
 
Durch den Prozess der unsere Cloud-Dienste zu folgenden Prinzipien, zusammen mit robusten testen und Validierung kann Office 365 erfüllen und die Anforderungen der Kunden beim sicherstellen, dass eine Plattform für fortlaufende Innovation und zur Verbesserung der überschreiten. 

## <a name="related-links"></a>Verwandte Links

- [Umgang mit beschädigte Daten](office-365-dealing-with-data-corruption.md)
- [Malware und Ransomware Schutz](office-365-malware-and-ransomware-protection.md)
- [Überwachung und Korrektur](office-365-monitoring-and-self-healing.md)
- [Exchange-Datenflexibilität](office-365-exchange-data-resiliency.md)
- [Ausfallsicherheit von SharePoint-Daten](office-365-sharepoint-data-resiliency.md)
---
title: Überwachen von Office 365 und Fehlerbehebung
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
description: Informationen zur Office 365 Überwachung und Fehlerbehebung.
ms.openlocfilehash: ff9471eaa6117ca3d7761549bca9ab629020fe79
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529051"
---
# <a name="office-365-monitoring-and-self-healing"></a>Überwachen von Office 365 und Fehlerbehebung
Die Skala für Office 365 angegeben, es ist nicht möglich, behalten Sie Kundendaten ausfallsichere und vor Schadsoftware ohne integrierte Überwachung eine umfassende, Warnung, dass intelligent ist und Korrektur, die schnell und zuverlässig. Eine Reihe von Diensten in der Skalierung von Office 365-Überwachung ist ein sehr großes. Neue Einstellung und Methoden eingeführt werden musste und völlig neue Sätze von Technologie benötigt zum betreiben und Verwalten des Diensts in einer verbundenen Umgebung globalen erstellt werden soll. Wir haben aus herkömmlichen Ansatz der Datensammlung Überwachung und Filterung verschoben, Benachrichtigungen an einen Ansatz zu erstellen, die auf Datenanalyse basiert; Nutzen der Signale und Vertrauen in diese Daten erstellen, und klicken Sie dann mithilfe der Automatisierung wiederherstellen oder das Problem beheben. Dieser Ansatz hilft Menschen die Formel Recovery dauern, wodurch wiederum Vorgänge weniger teuren, schneller und weniger Fehler anfällig. 

Grundlegendes zu Office 365 monitoring ist eine Auflistung von Technologien, die unsere Insights Data Engine, umfassen die auf Azure SQL Azure und [Open-Source-streaming datenbanktechnologie](http://cassandra.apache.org/)basiert. Es dient zum Erfassen und Aggregieren von Daten und Schlussfolgerungen zu erreichen. Derzeit mehr als 500 Millionen Ereignisse pro Stunde von mehr als 100.000 Servern (~ 15 TB pro Tag) Dutzende von Rechenzentren in vielen Regionen verteilt verarbeitet, und diese Nummern wachsen. 

Office 365 verwendet *außen monitoring*, umfasst das Erstellen von synthetischer Transaktionen, um alles zu testen, die wichtig sind. Beispielsweise wird in Exchange Online jedes Szenario jeder Datenbank weltweit testen alle fünf Minuten verstreute Weise bereitstellen kontinuierliche Abdeckung aller Elemente, die im System befindet sich in Ihrer Nähe. Von mehreren Standorten unterstützen werden 250 Millionen Test Transaktionen pro Tag ausgeführt, um eine robuste Baseline oder Heartbeat für den Dienst zu erstellen. 

Office 365 verwendet auch das Konzept von *Roten Warnung*, die nach unten alle monitoring Signale aus allen Computern in unseren Rechenzentren etwas von einem Menschen verwaltbaren, verkleinert werden. Das Konzept ist ganz einfach: Wenn Sie über mehrere Signale erweisen, es muss etwas passiert. Es ist nicht über das Erstellen von Vertrauen in ein Signal, Vorteil angemessene Fidelity für jedes Signal, damit Sie höhere Genauigkeit erhalten. Monitoring-System ist so leistungsstark, dass wir nicht sehen Sie sich unsere Monitore 24 x 7 Personal verfügen. Wir haben nur die Maschinen, die reaktiviert, wenn ein Problem Geräte-, in diesem Fall es das entsprechende auf Abruf Personal Seite wird oder mehr häufig der Fall ist, wird nur fahren Sie fort und das Problem zu lösen. Einmal wir beginnen, sammeln Signale und building rote Warnungen deaktiviert werden, wir können beginnen Triangulierung über alle unsere Servicepartitionen. 

Basierend auf einer Kombination aus der Benachrichtigung für Fehler und der roten Benachrichtigungen, diese Warnung gibt an genau welche Komponenten ein Problem aufgetreten sein könnten und schlägt das System zur Behebung des Problems allein durch einen Neustart eines Postfachservers versuchen. 

Zusätzlich zur Fehlerbehebung wie einzelne Seite wiederherstellen, gehören Exchange Online verschiedene Features, die ein Ansatz für die Überwachung und Korrektur konzentriert sich auf den durch den Endbenutzer beibehalten. Gehören die folgenden Features *Verwalteten Verfügbarkeit*, die integrierte Überwachung und Wiederherstellung Aktionen bereitstellt, und autoreseed-Funktion, die Datenbank Redundanz nach einem Datenträgerfehler automatisch wiederhergestellt. 

## <a name="managed-availability"></a>Verwaltete Verfügbarkeit 
Verwalteter Verfügbarkeit bietet eine systemeigene Integrität überprüfen und Recovery-Lösung, die überwacht und schützt die Endbenutzers über Recovery-orientierten Aktionen. Verwalteter Verfügbarkeit ist die Integration der integrierten monitoring und Recovery Aktionen mit der Exchange-Hochverfügbarkeits-Plattform. Es wurde entwickelt, erkennen und Beheben von Problemen, sobald sie auftreten und vom System ermittelt werden. Im Gegensatz zu vorherigen externen monitoring Lösungen und Techniken für Exchange versuchen nicht verwalteter Verfügbarkeit Sie zu identifizieren oder die Ursache des Problems zu kommunizieren. Stattdessen es Wiederherstellung Aspekte konzentriert sich auf das drei wichtige Bereiche der durch den Endbenutzer aufgelistet: 
- **Verfügbarkeit** – können Benutzer den Dienst zugreifen? 
- **Wartezeit** - wie die Benutzeroberfläche für Benutzer ist? 
- **Fehler** : können Benutzer Ihre vorstellungen umsetzen? 

Verwalteter Verfügbarkeit ist ein internes Feature, das auf jedem Office 365-Server mit Exchange Online ausgeführt wird. Es fragt ab und analysiert Hunderten von Health Metriken pro Sekunde. Wenn etwas gefunden wurde, falsch ist, werden in den meisten Fällen wird es automatisch korrigiert. Es jedoch wird immer, dass Probleme, die verwaltete Verfügbarkeit nicht in einem eigenen korrigieren können. In diesen Fällen wird die verwaltete Verfügbarkeit das Problem an das Supportteam für ein Office 365 durch ereignisprotokollierung ausweiten. 

## <a name="autoreseed"></a>AutoReseed 
Exchange Online-Server werden in einer Konfiguration bereitgestellt, die mehrere Datenbanken und deren protokolldatenströmen auf demselben-RAID-Datenträger gespeichert werden. Diese Konfiguration wird häufig als *einfach eine Reihe von Festplatten* (JBOD) bezeichnet, da kein Speicher Redundanz Mechanismen, beispielsweise RAID, um die Daten auf dem Datenträger zu duplizieren verwendet werden. Bei ein Datenträger in einer Umgebung JBOD ein Fehler auftritt, ist die Daten auf dem Datenträger verloren. 

Die angegebene Größe des Exchange Online und die Tatsache, die darin enthaltenen bereitgestellt sind Millionen von Festplatten, Festplattenlaufwerk mit Fehlern regelmäßig vorkommt im Exchange Online. Mehr als 100 fehlschlagen können Sie sogar täglich ausgeführt. Beim Ausfall einer Festplatte in einer lokalen Enterprise-Bereitstellung muss manuell ein Administrator die fehlerhafte Festplatte ersetzen und die betroffenen Daten wiederherstellen. In einer Cloudbereitstellung die Größe von Office 365 ist Operatoren (Cloud-Administratoren) manuell Austauschen von Datenträgern praktische weder wirtschaftlich. 

Automatisches erneutes Seeding oder *AutoReseed*, ist ein Feature, das ist der Ersatz für Was ist normalerweise Operator-gesteuerte Aktion als Antwort auf ein Datenträgerfehler, Datenverluste Datenbank oder andere Problem, das eine Einsaat eine Datenbankkopie erfordert. AutoReseed ist darauf ausgelegt, automatisch Datenbank Redundanz nach einem Datenträgerfehler mithilfe von Reserve Datenträger, auf die bereitgestellt wurden, auf dem System wiederherstellen. Wenn ein Laufwerk ausfällt, werden Datenbankkopien auf dem Datenträger gespeichert automatisch auf einem vorkonfigurierten Reserve Datenträger auf dem Server, wodurch wiederherstellen Redundanz zurückgesetzt. 
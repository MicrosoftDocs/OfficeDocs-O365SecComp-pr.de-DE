---
title: Office 365-Überwachung und Selbstheilung
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Informationen zu den Überwachungs-und Self-Healing-Funktionen von Office 365.
ms.openlocfilehash: 4878ca5889c9b893154e0e7b910cb17c4b36402c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217545"
---
# <a name="office-365-monitoring-and-self-healing"></a>Office 365-Überwachung und Selbstheilung
Angesichts des Umfangs von Office 365 wäre es nicht möglich, Kundendaten widerstandsfähig zu halten und vor Schadsoftware zu schützen, ohne dass eine integrierte Überwachung umfassend, intelligent und schnell und zuverlässig ist. Das überWachen einer Reihe von Diensten auf der Ebene von Office 365 ist sehr schwierig. Es muss eine neue Denkweise und Methodologie eingeführt werden, und es müssen vollständig neue Technologien erstellt werden, um den Dienst in einer verbundenen globalen Umgebung zu betreiben und zu verwalten. Wir haben uns vom herkömmlichen Überwachungsansatz der Datenerfassung und-Filterung entfernt, um Warnungen zu einem Ansatz zu erstellen, der auf der Datenanalyse basiert. Signale zu erstellen und das Vertrauen in diese Daten und dann mithilfe der Automatisierung zu erholen oder das Problem zu beheben. Diese Vorgehensweise hilft den Menschen bei der Wiederherstellungs Gleichung, wodurch Vorgänge kostengünstiger, schneller und weniger fehleranfällig sind. 

Fundamental für Office 365 Monitoring ist eine Sammlung von Technologien, die unser Data inSights-Modul umfassen, das auf Azure, SQL Azure und [Open-Source-Streamingdatenbank-Technologie](http://cassandra.apache.org/)basiert. Es wurde entwickelt, um Daten zu sammeln und zu aggregieren und Schlussfolgerungen zu erzielen. Derzeit werden mehr als 500 Millionen Ereignisse pro Stunde von mehr als 100.000 Servern (~ 15 TB pro Tag) in Dutzenden von Datencentern in vielen Regionen verteilt, und diese Zahlen werden immer größer. 

Office 365 verwendet die *Externe Überwachung*, die das Erstellen synthetischer Transaktionen umfasst, um alles zu testen, was wichtig ist. In Exchange Online wird in jedem Szenario beispielsweise jede Datenbank weltweit alle fünf Minuten getestet, sodass alles, was sich im System befindet, nahezu kontinuierlich abgedeckt wird. Von mehreren Standorten aus werden 250 Millionen-Testtransaktionen pro Tag ausgeführt, um eine robuste Basislinie oder einen Takt für den Dienst zu erstellen. 

Office 365 verwendet auch das Konzept der *roten Warnung*, die alle Überwachungssignale von allen Computern in unseren Rechenzentren auf etwas reduziert, das von einem Menschen verwaltet werden kann. Das Konzept ist ganz einfach: Wenn etwas über mehrere Signale geschieht, muss etwas passieren. Es geht nicht darum, Vertrauen in ein Signal zu schaffen, es geht darum, eine angemessene Treue für jedes Signal zu haben, damit Sie eine höhere Genauigkeit erhalten. Dieses Überwachungssystem ist so leistungsfähig, dass wir nicht rund um die Uhr über unsere Monitore verfügen. alles, was wir haben, ist die Maschinerie, die aufwacht, wenn Sie ein Problem erkennt, in diesem Fall wird das entsprechende On-Call-Personal, oder häufiger, wie es der Fall ist, es wird einfach weiter gehen und das Problem lösen. Sobald wir mit dem Sammeln von Signalen und dem Erstellen von roten Warnungen beginnen, können wir mit der Triangulation aller Dienst Partitionen beginnen. 

Basierend auf der Kombination aus Fehlermeldung und roten Warnungen gibt diese Warnung genau an, welche Komponenten ein Problem aufweisen können, und dass das System versuchen wird, das Problem selbst zu beheben, indem ein Postfachserver neu gestartet wird. 

Neben Self-Healing-Funktionen wie der Wiederherstellung einzelner Seiten umfasst Exchange Online mehrere Features, die einen Ansatz für die Überwachung und die Selbstheilung verfolgen, wobei die Endbenutzerfreundlichkeit im Vordergrund steht. Zu diesen Features gehören die *verwaltete Verfügbarkeit*, die integrierte Überwachungs-und Wiederherstellungsaktionen bereitstellt und AutoReseed, wodurch die Datenbankredundanz nach einem Datenträgerausfall automatisch wiederhergestellt wird. 

## <a name="managed-availability"></a>Verwaltete Verfügbarkeit 
Die verwaltete Verfügbarkeit bietet eine systemeigene Integritätsprüfung und Wiederherstellungslösung, mit der die Benutzererfahrung durch Wiederherstellungs orientierte Aktionen überwacht und geschützt wird. Bei der verwalteten Verfügbarkeit handelt es sich um die Integration integrierter Überwachungs-und Wiederherstellungsaktionen mit der hoch Verfügbarkeits Plattform von Exchange. Sie wurde entwickelt, um Probleme zu erkennen und wiederherzustellen, sobald sie auftreten und vom System erkannt werden. Anders als bei früheren externen Überwachungslösungen und-Techniken für Exchange versucht die verwaltete Verfügbarkeit nicht, die Ursache eines Problems zu identifizieren oder zu kommunizieren. Stattdessen konzentriert er sich auf Wiederherstellungs Aspekte, die drei Hauptbereiche der Endbenutzeroberfläche berücksichtigen: 
- **Verfügbarkeit** – können Benutzer auf den Dienst zugreifen? 
- **Latenz** -wie ist die Benutzererfahrung? 
- **Fehler** – können Benutzer Ihre Wünsche erfüllen? 

Die verwaltete Verfügbarkeit ist ein internes Feature, das auf jedem Office 365-Server mit Exchange Online ausgeführt wird. Jede Sekunde werden hunderte von Integritäts Metriken abgefragt und analysiert. Wenn sich etwas als falsch herausstellt, wird die meiste Zeit automatisch behoben. Es gibt jedoch immer Probleme, die von der verwalteten Verfügbarkeit nicht selbst behoben werden können. In diesen Fällen wird das Problem durch die verwaltete Verfügbarkeit an ein Office 365-Support Team mithilfe der Ereignisprotokollierung eskaliert. 

## <a name="autoreseed"></a>AutoReseed 
Exchange Online-Server werden in einer Konfiguration bereitgestellt, in der mehrere Datenbanken und deren Protokolldatenströme auf demselben nicht-RAID-Datenträger gespeichert werden. Diese Konfiguration wird häufig als *nur eine Gruppe von* Datenträgern (JBOD) bezeichnet, da keine Speicherredundanz Mechanismen wie RAID verwendet werden, um die Daten auf dem Datenträger zu duplizieren. Wenn ein Datenträger in einer JBOD-Umgebung ausfällt, gehen die Daten auf diesem Datenträger verloren. 

Angesichts der Größe von Exchange Online und der Tatsache, dass es sich um Millionen von Festplatten handelt, sind Laufwerksausfälle in Exchange Online ein reguläres vorkommen. Tatsächlich schlagen täglich mehr als 100 fehl. Wenn ein Datenträger in einer lokalen Enterprise-Bereitstellung ausfällt, muss ein Administrator den ausgefallenen Datenträger manuell ersetzen und die betroffenen Dateien wiederherstellen. In einer Cloud-Bereitstellung ist die Größe von Office 365, wenn Betreiber (Cloud-Administratoren) Datenträger manuell ersetzen, weder praktikabel noch wirtschaftlich machbar. 

Automatisches erneutes Seeding oder *AutoReseed*ist ein Feature, das als Ersatz für die normalerweise vom benutzergesteuerte Aktion als Reaktion auf einen Datenträgerfehler, ein Daten Bank Beschädigungs Ereignis oder ein anderes Problem, bei dem ein erneutes Seeding einer Datenbankkopie erforderlich ist. AutoReseed ist darauf ausgelegt, Datenbankredundanz nach einem Datenträgerausfall mithilfe von Ersatz Datenträgern, die auf dem System bereitgestellt wurden, automatisch wiederherzustellen. Wenn ein Datenträger ausfällt, werden die auf diesem Datenträger gespeicherten Datenbankkopien automatisch in einen vorkonfigurierten Ersatzdatenträger auf dem Server erneut seedingt, wodurch Redundanz wiederhergestellt wird. 
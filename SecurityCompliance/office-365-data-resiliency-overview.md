---
title: Datenresilienz in Office 365
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
description: GrundLegendes zur Datensicherheit in Microsoft Office 365.
ms.openlocfilehash: 1e85f431edeec0a4548b1d37b65a4b1a6cbef8eb
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215635"
---
# <a name="data-resiliency-in-office-365"></a>Datenresilienz in Office 365

## <a name="introduction"></a>Einführung
Angesichts des komplexen Charakters des Cloud-Computings ist Microsoft bewusst, dass es nicht der Fall ist, wenn etwas schief geht, sondern wann. Wir entwerfen unsere Cloud-Dienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden zu minimieren, wenn etwas schief geht. Wir haben die herkömmliche Strategie der unter Berufung auf eine komplexe physische Infrastruktur überschritten, und wir haben Redundanz direkt in unsere Cloud-Dienste integriert. Wir verwenden eine Kombination aus weniger komplexer physischer Infrastruktur und intelligenter Software, mit der Datensicherheit in unseren Diensten aufgebaut wird und die hohe Verfügbarkeit für unsere Kunden ermöglicht. 

## <a name="resiliency-and-recoverability-are-built-in"></a>Ausfallsicherheit und Wiederherstellbarkeit sind integriert 
Das Erstellen von Ausfallsicherheit und Wiederherstellung beginnt mit der Annahme, dass die zugrunde liegende Infrastruktur und Prozesse irgendwann fehlschlagen: Hardware (Infrastruktur) schlägt fehl, Menschen machen Fehler und Software hat Fehler. Obwohl es falsch wäre, zu sagen, dass Softwareentwickler vor der Cloud nicht über diese Dinge nachgedacht haben, war es vor der Cloud sehr unterschiedlich, wie diese Probleme in einer typischen IT-Implementierung behandelt wurden: 
- Erstens waren Hardware-und Infrastruktur Schutz erheblich. Dies bedeutet, dass Rechenzentren mit einer Zuverlässigkeit von 99,99% eine beträchtliche Leistungs-und Netzwerkredundanz erfordern, und Server wurden mit hardwarebasiertem Clustering, zwei Netzteilen, dualen Netzwerkschnittstellen usw. implementiert. 
- Zweitens war der Prozess von größter Bedeutung. In den Betriebsteams wurden strenge Verfahren unterhalten, die Fenster wurden geändert, und es kam oft zu einem beträchtlichen Projektmanagementaufwand. 
- Drittens erfolgte die Bereitstellung in einer Eiszeit. Das Bereitstellen von Code ohne die Quelle zu besitzen bedeutete, auf Patch-Releases zu warten, und Major Version-Versionen behandelten Hardwareaustausch und erhebliche Investitionsaufwendungen. Darüber hinaus war die einzige Möglichkeit zum Beheben eines Problems das Rollback. Daher würden die meisten IT-Organisationen nur größere Versionen bereitstellen, um zu verhindern, dass die Arbeit auf dem neuesten Stand ist. 
- Schließlich war die Skalierung der bereitgestellten Systeme und die Ebene ihrer Verbundenheit historisch viel kleiner als jetzt. 

Heute erwarten Kunden von Microsoft kontinuierliche Innovationen ohne Beeinträchtigung der Qualität, und dies ist einer der Gründe dafür, dass die Dienste und Software von Microsoft auf Ausfallsicherheit und Wiederherstellbarkeit ausgelegt werden. 

## <a name="office-365-data-resiliency-principles"></a>Grundsätze der Datensicherheit in Office 365 
Die Ausfallsicherheit bezieht sich auf die Fähigkeit eines cloudbasierten Diensts, bestimmte Typen von Fehlern zu widerstehen und dennoch aus Sicht des Kunden voll funktionsfähig zu bleiben. Datenausfall Sicherheit: unabhängig davon, welche Fehler in Office 365 auftreten, bleiben wichtige Kundendaten intakt und unberührt. Zu diesem Zweck wurden die Office 365-Dienste auf fünf spezifische Ausfallsicherheit-Prinzipien ausgelegt: 
- Es gibt kritische und nicht kritische Daten. Nicht kritische Daten (beispielsweise, ob eine Nachricht gelesen wurde) können in seltenen Fehlerszenarien gelöscht werden. Kritische Daten (beispielsweise Kundendaten wie e-Mail-Nachrichten) sollten zu extremen Kosten geschützt werden. Als Design Ziel sind zugestellte e-Mail-Nachrichten immer kritisch, und Dinge wie die Frage, ob eine Nachricht gelesen wurde, sind nicht kritisch. 
- Kopien von Kundendaten müssen in verschiedene Fehler Zonen oder so viele fehlerdomänen wie möglich aufgeteilt werden (z. b. Rechenzentren, auf die einzelne Anmeldeinformationen (Prozess, Server oder Operator) zugreifen können, um die Fehlerisolierung zu gewährleisten. 
- Kritische Kundendaten müssen überwacht werden, um einen Teil der atomaren, Konsistenz, Isolierung, Dauerhaftigkeit (ACID) nicht zu überwachen. 
- Kundendaten müssen vor Beschädigung geschützt werden. Sie muss aktiv überprüft oder überwacht, repariert und wiederherstellbar sein. 
- Die meisten Datenverluste resultieren aus Kundenaktionen und ermöglichen es Kunden daher, sich selbst über eine GUI zu erholen, die es Ihnen ermöglicht, versehentlich gelöschte Elemente wiederherzustellen. 
 
Durch den Aufbau unserer Cloud-Dienste zu diesen Prinzipien, gepaart mit robustem testen und Überprüfung, ist Office 365 in der Lage, die Anforderungen von Kunden zu erfüllen und zu übertreffen und gleichzeitig eine Plattform für kontinuierliche Innovation und Verbesserung zu bieten. 

## <a name="related-links"></a>Verwandte Links

- [Umgang mit Datenbeschädigung](office-365-dealing-with-data-corruption.md)
- [Schutz vor Schadsoftware und Ransomware](office-365-malware-and-ransomware-protection.md)
- [Überwachung und Selbstreparatur](office-365-monitoring-and-self-healing.md)
- [Exchange-Datensicherheit](office-365-exchange-data-resiliency.md)
- [SharePoint-Datenausfall Sicherheit](office-365-sharepoint-data-resiliency.md)
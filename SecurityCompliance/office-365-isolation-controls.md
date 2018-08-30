---
title: Steuerelemente für Office 365 Isolation
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
description: 'Zusammenfassung: Eine Erläuterung der Isolation Steuerelemente in Office 365.'
ms.openlocfilehash: 3a5c06d0675a4503d9f5e5edd58535688fb9180a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530111"
---
# <a name="office-365-isolation-controls"></a>Steuerelemente für Office 365 Isolation 

Microsoft versucht kontinuierlich, um sicherzustellen, dass die Architektur mit mehreren Mandanten von Office 365 Unternehmensebene Sicherheit, Vertraulichkeit, Datenschutz, Integrität und Verfügbarkeit [Standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)sowie lokale und internationale Standards unterstützt. Wenn die Skalierung und des Umfangs der von Microsoft bereitgestellten Dienste, wäre es schwierig und nicht wirtschaftliche zum Verwalten von Office 365 erhebliche Benutzerinteraktionen erforderlich waren. Office 365-Dienste werden über mehreren weltweit verteilten Rechenzentren in einer Weise hoch automatisiert bereitgestellt, wobei sehr wenige Datacenter Vorgänge erfordern eine human Fingereingabe und sogar weniger Vorgänge benötigen Zugriff auf Inhalte für Kunden. Unsere Mitarbeiter unterstützt diese Dienste und Rechenzentren mit automatisierten Tools und extrem sicheren Remotezugriff. Details zur Verwendung einiger betrieben werden umfangreiche Services in Office 365 finden Sie unter [einem Behind, die Office 365 für IT-Experten im Hintergrund betrachten](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

Office 365 besteht mehrere Dienste, die wichtige geschäftliche Funktionalität und dazu beitragen, für die gesamte Office 365-Funktionen. Jeder dieser Dienste dient unabhängig sein und miteinander zu integrieren. Office 365 ist mit den Prinzipien eine [Service-orientierte Architektur](https://msdn.microsoft.com/library/aa480021.aspx)entwickelt, die als entwerfen und Entwickeln von Software in Form von interoperablen Diensten, die beim Bereitstellen von klar definierten Business-Funktionalität und [betriebliche Sicherheit definiert ist Assurance](http://www.microsoft.com/download/details.aspx?id=40872), ein Rahmen, der die Kenntnisse erlangt über eine Vielzahl von Funktionen, die an Microsoft, einschließlich Microsoft [Security Development Lifecycle](https://www.microsoft.com/sdl/default.aspx), die [Microsoft Security Response Center](https://technet.microsoft.com/library/dn440717.aspx)und intensive eindeutig sind zur Förderung des Bekanntheitsgrads der Bedrohungslandschaft Sicherheit im Internet.

Office 365-Diensten miteinander interagieren, aber entworfen und implementiert, sodass bereitgestellt und als autonome Dienste unabhängig voneinander betrieben werden kann. Microsoft verfügt, Aufgaben und Bereiche der Verantwortung für eine Office 365 zur Reduzierung von Verkaufschancen für nicht autorisierte oder unbeabsichtigte Änderung oder Missbrauch von Ressourcen der Organisation. Office 365-Teams, die im Rahmen einer umfassenden rollenbasierte Zugriff Steuerelement Mechanismus Rollen definiert haben.

## <a name="customer-content-isolation"></a>Inhaltliche Trennung von Kunden
Alle Kunden Inhalte, die zu einem Mandanten gehören wird isoliert von anderen Mandanten und die Vorgänge und Systemen Daten in die Verwaltung von Office 365 verwendet. Mehrere Formulare des Schutzes es wurden in der gesamten Office 365, um das Risiko der Gefährdung keinen Office 365-Dienst oder Anwendung oder eine beliebige erlangen unberechtigte Zugriff auf die Informationen des Mandanten oder die Office 365-System selbst zu minimieren implementiert. Informationen dazu, wie Microsoft logischen Isolierung von Mandantendaten in Office 365 implementiert wird finden Sie unter [Mandantenisolation in Office 365](office-365-tenant-isolation-overview.md).

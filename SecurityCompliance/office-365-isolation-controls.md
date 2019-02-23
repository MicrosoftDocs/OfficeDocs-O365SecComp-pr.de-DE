---
title: Isolierungssteuerungen in Office 365
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
description: 'Zusammenfassung: eine Erläuterung der Isolations Steuerelemente in Office 365.'
ms.openlocfilehash: a6ff2b11ea02334a6c47317cbb77b8d47207b552
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217315"
---
# <a name="office-365-isolation-controls"></a>Isolierungssteuerungen in Office 365 

Microsoft arbeitet ständig daran, sicherzustellen, dass die Architektur mit mehreren Mandanten von Office 365 die Sicherheit, Vertraulichkeit, Datenschutz, Integrität und Verfügbarkeit von [Standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)auf Unternehmensebene sowie lokale und internationale Standards unterstützt. Angesichts des Umfangs und des Umfangs der von Microsoft bereitgestellten Dienste wäre es schwierig und nicht wirtschaftlich, Office 365 zu verwalten, wenn eine erhebliche menschliche Interaktion erforderlich wäre. Office 365-Dienste werden in einer hoch automatisierten Weise über mehrere global verteilte Rechenzentren bereitgestellt, wobei für äußerst wenige Rechenzentrums Vorgänge eine menschliche Note erforderlich ist und noch weniger Vorgänge den Zugriff auf Kunden Inhalte erfordern. Unsere Mitarbeiter unterstützen diese Dienste und Rechenzentren mit automatisierten Tools und hoch sicherem Remotezugriff. Einige Details zur Verwendung von umfangreichen Diensten in Office 365 finden Sie unter ["Behind the Scenes" in office 365 für IT-Experten](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

Office 365 besteht aus mehreren Diensten, die wichtige Geschäftsfunktionen bereitstellen und zur gesamten Office 365-Umgebung beitragen. Jeder dieser Dienste ist eigenständig und kann miteinander integriert werden. Office 365 wurde mit den Prinzipien einer [DienstorientiertEn Architektur](https://msdn.microsoft.com/library/aa480021.aspx)entworfen, die als entwerfen und entwickeln von Software in Form von interoperablen Diensten definiert ist, die eine klar definierte Geschäftsfunktionalität und [Betriebssicherheit bieten. Assurance](http://www.microsoft.com/download/details.aspx?id=40872), ein Framework, das die erworbenen Kenntnisse durch eine Vielzahl von Funktionen umfasst, die für Microsoft einzigartig sind, einschließlich des Microsoft- [Sicherheits Entwicklungslebenszyklus](https://www.microsoft.com/sdl/default.aspx), des [Microsoft Security Response Center](https://technet.microsoft.com/library/dn440717.aspx)und Deep Bewusstsein für die Cyber-Bedrohungslandschaft.

Office 365-Dienste arbeiten miteinander zusammen, sind jedoch so konzipiert und implementiert, dass Sie unabhängig von einander als autonome Dienste bereitgestellt und betrieben werden können. Microsoft trennt Aufgaben und Zuständigkeitsbereiche für Office 365, um die Möglichkeiten für unbefugte oder unbeabsichtigte Änderungen oder Missbrauch der Ressourcen der Organisation zu verringern. Office 365 Teams haben Rollen als Teil einer umfassenden rollenbasierten Zugriffssteuerungsmethode definiert.

## <a name="customer-content-isolation"></a>Kunden-Inhalts Isolierung
Alle Kunden Inhalte, die zu einem Mandanten gehören, werden von anderen Mandanten isoliert und von den Betriebs-und Systemdaten, die bei der Verwaltung von Office 365 verwendet werden. Es wurden mehrere Schutzformen in Office 365 implementiert, um das Risiko einer Gefährdung eines beliebigen Office 365-Diensts oder einer Anwendung zu minimieren, oder um einen unbefugten Zugriff auf die Informationen von Mandanten oder das Office 365-System selbst zu erlangen. Informationen dazu, wie Microsoft die logische Isolierung von Mandantendaten in Office 365 implementiert, finden Sie unter [mandantEn Isolierung in office 365](office-365-tenant-isolation-overview.md).

---
title: Office 365-Isolierung und Zugriffssteuerung in Azure Active Directory
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
description: 'Zusammenfassung: Funktionsweise der Isolations-und Zugriffssteuerung in Azure Active Directory.'
ms.openlocfilehash: 01103361a084d50adbc6c0a8351d9af8311a39fd
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090507"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a>Isolierung und Zugriffssteuerung in Azure Active Directory

Azure Active Directory wurde entwickelt, um mehrere Mandanten auf hochsichere Weise durch die logische Datenisolierung zu hosten. Der Zugriff auf Azure Active Directory erfolgt über eine Autorisierungs Schicht. Azure Active Directory isoliert Kunden, die Mandanten Container verwenden, als Sicherheitsgrenzen, um die Inhalte eines Kunden so zu schützen, dass der Zugriff auf den Inhalt oder die Beeinträchtigung durch die Mitbewohner nicht möglich ist. Es werden drei Prüfungen von der Berechtigungs Schicht von Azure Active Directory durchgeführt:
- Ist der Prinzipal für den Zugriff auf den Azure Active Directory-Mandanten aktiviert?
- Ist der Prinzipal für den Zugriff auf Daten in diesem Mandanten aktiviert?
- Ist die Rolle des Prinzipals in diesem Mandanten für den Typ des angeforderten Datenzugriffs autorisiert?

Kein Anwendungs-, Benutzer-, Server-oder Dienst kann Azure Active Directory ohne die richtige Authentifizierung und das Token oder Zertifikat zugreifen. Anforderungen werden zurückgewiesen, wenn Sie nicht von korrekten Anmeldeinformationen begleitet werden.

Azure Active Directory hostet jeden Mandanten in seinem eigenen geschützten Container, mit Richtlinien und Berechtigungen für und innerhalb des Containers, der nur vom Mandanten verwaltet wird.
 
![Azure-Container](media/office-365-isolation-azure-container.png)

Das Konzept der Mandanten Container ist im Verzeichnisdienst auf allen Ebenen tief verankert, von Portalen bis hin zu permanentem Speicher. Auch wenn mehrere Azure Active Directory-Mandanten Metadaten auf demselben physischen Datenträger gespeichert werden, gibt es keine Beziehung zwischen den Containern, die von dem Verzeichnisdienst definiert werden, der wiederum vom mandantenadministrator diktiert wird. Es kann keine direkte Verbindung zum Azure Active Directory-Speicher von einer anfordernden Anwendung oder einem Dienst ohne vorherige Durchführung der Autorisierungs Schicht geben.

Im Beispiel unten haben Contoso und Fabrikam beide separate dedizierte Container, und obwohl diese Container einige der gleichen zugrunde liegenden Infrastruktur teilen, wie Server und Speicher, bleiben Sie getrennt und voneinander isoliert und werden von Autorisierungs-und Zugriffs Steuerungsebenen
 
![Dedizierte Azure-Container](media/office-365-isolation-azure-dedicated-containers.png)

Darüber hinaus gibt es keine Anwendungskomponenten, die innerhalb von Azure Active Directory ausgeführt werden können, und es ist nicht möglich, dass ein Mandant gewaltsam die Integrität eines anderen Mandanten verletzt, auf Verschlüsselungsschlüssel eines anderen Mandanten zugreift oder Rohdaten vom Server liest.

Standardmäßig werden von Azure Active Directory alle Vorgänge, die von Identitäten in anderen Mandanten ausgegeben werden, nicht zugelassen. Jeder Mandant ist innerhalb von Azure Active Directory über anspruchsbasierte Zugriffssteuerungen logisch isoliert. Lese-und Schreibvorgänge von Verzeichnisdaten sind auf Mandanten Container ausgelegt und werden durch eine interne Abstraktionsschicht und eine rollenbasierte Zugriffs Steuerungsschicht (Role-Based Access Control, RBAC) abgegrenzt, die den Mandanten zusammen als Sicherheitsgrenze erzwingen. Jede Verzeichnisdaten Zugriffsanforderung wird von diesen Schichten verarbeitet, und jede Zugriffsanforderung in Office 365 wird durch die obige Logik überwacht.

Azure Active Directory verfügt über Nordamerika, die US-Regierung, die Europäische Union, Deutschland und die weltweiten Partitionen. Ein Mandant ist in einer einzelnen Partition vorhanden, und Partitionen können mehrere Mandanten enthalten. Partitionsinformationen werden von Benutzern abstrahiert. Eine bestimmte Partition (einschließlich aller darin enthaltenen Mandanten) wird in mehrere Rechenzentren repliziert. Die Partition für einen Mandanten wird basierend auf den Eigenschaften des Mandanten ausgewählt (beispielsweise der Ländercode). Geheimnisse und andere vertrauliche Informationen in jeder Partition werden mit einem dedizierten Schlüssel verschlüsselt. Die Schlüssel werden beim Erstellen einer neuen Partition automatisch generiert.

Azure Active Directory-Systemfunktionen sind eine eindeutige Instanz für jede Benutzersitzung. Darüber hinaus verwendet Azure Active Directory Verschlüsselungstechnologien, um freigegebene Systemressourcen auf Netzwerkebene zu isolieren, um eine unbefugte und unbeabsichtigte Übermittlung von Informationen zu verhindern.

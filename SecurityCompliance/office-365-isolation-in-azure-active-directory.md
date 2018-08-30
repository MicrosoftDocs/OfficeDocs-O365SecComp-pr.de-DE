---
title: Office 365-Isolation und Steuerung des Zugriffs in Azure Active Directory
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
description: 'Zusammenfassung: Wie die Steuerung des Zugriffs und Isolation innerhalb von Azure Active Directory arbeiten.'
ms.openlocfilehash: db4fa0d026c6c608f09252c65bf1e0de5354f68c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529979"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a>Die Isolierung und Steuerung des Zugriffs in Azure Active Directory

Azure Active Directory wurde entwickelt, um auf eine sehr sichere Weise über logische Datenisolation mehrere Mandanten hosten. Zugriff auf Azure Active Directory wird durch eine Ebene Autorisierung abgegrenzten. Azure Active Directory isoliert Kunden mit Mandanten Containern als Sicherheitsgrenzen, um ein Kunde Inhalte zu schützen, damit der Inhalt nicht zugegriffen oder durch gemeinsame Mandanten gefährdet. Drei überprüft werden von Azure Active Directory-Autorisierung Schicht ausgeführt:
- Werden der Prinzipal ist für den Zugriff auf Azure Active Directory-Mandanten aktiviert?
- Werden der Prinzipal ist für den Zugriff auf Daten in diesen Mandanten aktiviert?
- Ist der Prinzipal Rolle in diesen Mandanten für den Typ der Datenzugriff angefordert autorisiert?

Keine Anwendung, Benutzer, Server oder Dienst kann ohne die richtigen Authentifizierung und Token oder Zertifikat Azure Active Directory zugreifen. Anfragen werden zurückgewiesen, wenn sie nicht von der richtigen Anmeldeinformationen begleitet sind.

Azure Active Directory hostet praktisch jeder Mandant in einem eigenen geschützten Container, mit Richtlinien und Berechtigungen auf und innerhalb des Containers ausschließlich gehört und durch die Mandanten verwaltet.
 
![Azure-container](media/office-365-isolation-azure-container.png)

Das Konzept der Mandanten-Container wird im Verzeichnisdienst an alle Ebenen von Portalen ganz nach ein beständiger Speicher tief verinnerlicht. Auch wenn mehrere Azure Active Directory-Mandanten Metadaten auf demselben physischen Datenträger gespeichert ist, besteht keine Beziehung zwischen den Containern als was durch den Verzeichnisdienst definiert ist, die wiederum von der mandantenadministrator vorgegeben ist. In Azure Active Directory-Speicher kann keine direkten Verbindungen vorhanden sein, alle anfordernde Anwendung oder dem Dienst ohne den ersten Umweg über die Autorisierung Ebene.

Im folgenden Beispiel "Contoso" und "Fabrikam" getrennte, dedizierte Container und, obwohl diese Container einige der gleichen zugrunde liegenden-Infrastruktur, wie etwa-Servern und Speicher freigeben können sie bleiben separate und voneinander getrennt, und durch abgegrenzten Ebenen der Autorisierung und Access Control.
 
![Azure dedizierten Container](media/office-365-isolation-azure-dedicated-containers.png)

Darüber hinaus sind keine Anwendungskomponenten, die von in Azure Active Directory ausgeführt werden können, und es ist nicht möglich, für einen Mandanten zum erzwungenen verletzen die Integrität der einen anderen Mandanten, Zugriff auf Verschlüsselungsschlüssel, der einen anderen Mandanten oder unformatierte Daten vom Server lesen.

In der Standardeinstellung lässt Azure Active Directory alle Vorgänge von Identitäten in anderen Mandanten ausgestellt. Jeder Mandant wird logisch isoliert innerhalb von Azure Active Directory über anspruchsbasierte zugreifen auf Steuerelemente. Lese- und Schreibvorgänge von Directory Daten bezogenen Mandanten Containern und in eine interne Abstraktionsebene und in einer rollenbasierten Zugriffssteuerung (RBAC) Ebene zusammen den Mandanten als Sicherheitsgrenze erzwingen abgegrenzten. Jede Directory Data Access Anforderung wird durch diese Ebenen verarbeitet, und jeder Anforderung Access in Office 365 wird von der oben genannten Logik policed.

Azure Active Directory hat Nordamerika, US-Regierung, Europäische Union, Deutschland, und World Wide Partitionen. Ein Mandant in einer einzelnen Partition vorhanden ist, und Partitionen können mehrere Mandanten enthalten. Informationen zur Partition wird Weg vom Benutzer abstrahiert. Eine bestimmte Partition (einschließlich aller Mandanten darin enthaltenen) wird in mehreren Rechenzentren repliziert. Die Partition für einen Mandanten wird anhand der Eigenschaften des Mandanten (z. B. die Landesvorwahl) ausgewählt. Secrets und andere vertrauliche Informationen in jeder Partition mit einem dedizierten Schlüssel verschlüsselt. Die Schlüssel werden automatisch generiert, wenn eine neue Partition erstellt wird.

Azure Active Directory-System-Funktionen sind eine eindeutige Instanz mit einer benutzersitzung. Darüber hinaus verwendet Azure Active Directory-verschlüsselungstechnologien, um die Isolierung von freigegebenen Systemressourcen auf Netzwerkebene zu verhindern, dass nicht autorisierte und unerwünschte Übermittlung Informationen bereitzustellen.

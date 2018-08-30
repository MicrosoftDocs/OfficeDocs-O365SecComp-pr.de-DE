---
title: Office 365-Isolation und Steuerung des Zugriffs in Office 365
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
description: 'Zusammenfassung: Eine Erläuterung der Isolation und Zugriffssteuerung in den verschiedenen Anwendungen von Office 365.'
ms.openlocfilehash: c1989bc546df357740ea963a1a241dfa14557931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530003"
---
# <a name="isolation-and-access-control-in-office-365"></a>Die Isolierung und Steuerung des Zugriffs in Office 365

Azure Active Directory und Office 365 verwenden eine sehr komplexe Datenmodell, die Dienste, Hunderte von Entitäten, die sich auf Zehntausende enthält Tausende von Beziehungen und Zehntausende Attribute (Entitäten, die Beziehungen und Attribute sind oft anwendungsspezifische). Auf allgemeiner Ebene Azure Active Directory und die Verzeichnisse Service sind die Container von Mandanten und Empfänger, und sie sind synchronisiert statusbasierte Replikationsprotokolle verwenden. Zusätzlich zu der Verzeichnisinformationen Transportsystem mit Azure Active Directory jeden der Dienste auch haben einen eigenen Verzeichnisdienst-Infrastruktur (z. B. Verzeichnisdiensten der Exchange Online, SharePoint Online Directory Services usw.). 
 
![Office 365-Mandanten Daten sync](media/office-365-isolation-tenant-data-sync.png)

In diesem Modell ist keine zentrale Quelle Directory-Daten. Jedes einzelne Datenelement ist einem bestimmten System gehören, jedoch keine einzelnen alle Daten enthält. Office 365-Diensten zusammen mit Azure Active Directory Datenmodell zu erkennen. Azure Active Directory ist die "System Wahrheit" für freigegebene Daten in der Regel kleine als auch statische Daten, die von jeder Dienst häufig verwendet werden. Verbundpartner Modell in Office 365 und Azure Active Directory verwendet bietet die freigegebene Ansicht der Daten.

Office 365 verwendet physischen Speicher und Azure-Cloud-Speicher. Exchange Online (einschließlich Exchange Online Protection) und Skype für Unternehmen können Sie ihre eigenen Speicherung für Kundendaten verwenden. SharePoint Online nutzt die SQL Server-Speicher und die Azure-Speicher, die die Notwendigkeit für zusätzliche Isolierung von Kundendaten auf Speicherebene erfordert.

## <a name="exchange-online"></a>Exchange Online
Exchange Online speichert Kundendaten innerhalb von Postfächern, die innerhalb von Postfachdatenbanken aufgerufen Extensible Storage Engine (ESE)-Datenbanken gehostet werden. Dazu gehören Benutzerpostfächer, verknüpfte Postfächer, freigegebene Postfächer und Postfächer für Öffentliche Ordner. Benutzerpostfächer gehören auch gespeicherte Skype für Business-Inhalten, beispielsweise Unterhaltung gespeichert werden soll. Inhalt von Postfächern umfasst-e-Mails und e-Mail-Anlagen, Kalender und Frei/Gebucht-Informationen, Kontakte, Aufgaben, Notizen, Gruppen und Ableitung Daten.

Jede Postfachdatenbank in Exchange Online enthält die Postfächer aus mehreren Mandanten. Alle Postfächer sind durch Autorisierungscode, einschließlich innerhalb eines Mandanten gesichert. Als hat mit einer lokalen Bereitstellung von Exchange, standardmäßig nur der zugewiesene Benutzer Zugriff auf ein Postfach. Die Zugriffssteuerungsliste (ACL), die ein Postfach sichert enthält eine Identität, die von Azure Active Directory auf der Ebene der Mandant authentifiziert wird. Die Postfächer für einen bestimmten Mandanten können nur Identitäten authentifiziert anhand des Mandanten Authentifizierungsanbieter, die diese Mandanten nur Benutzer enthalten. Inhalte, die zu TenantA gehören werden nicht keinerlei von Benutzern in TenantB, ermittelt, es sei denn, die explizit durch TenantA genehmigt.

## <a name="skype-for-business"></a>Skype for Business
Skype für Unternehmen werden Daten in einer Vielzahl von Orten gespeichert:
- Benutzer- und Konto Informationen Verbindungsendpunkte, die Mandanten-IDs, einschließlich Wählpläne, roaming Settings, Anwesenheitsstatus, Kontaktlisten usw., ist in der Skype für Business Active Directory-Server und in verschiedenen Skype für Business-Datenbank gespeichert Server. Kontaktlisten werden in Exchange Online-Postfach des Benutzers gespeichert, wenn der Benutzer für beide Produkte oder auf Skype für Business Server aktiviert ist, wenn der Benutzer nicht befindet. Skype für Datenbankserver Business sind nicht partitionierten pro Mandant, aber mehrmandantenfähigkeit Isolierung von Daten über RBAC erzwungen wird.
- Besprechungsinhalte, wie Inhalt Benutzer während der Skype für Business-Besprechungen Hochladen wird auf DFS-Freigaben gespeichert. Dieser Inhalt kann auch in Exchange Online archiviert werden, sofern die Archivierung aktiviert ist. DFS-Freigaben sind nicht partitionierten pro Mandant aber mit ACLs wird der Inhalt geschützt und mehrmandantenfähigkeit durch RBAC erzwungen wird.
- Kommunikationsdatensätze in der Aktivitätshistorie wie der Anrufliste, IM-Sitzungen, Anwendungsfreigabe, Instant Messaging-Verlauf usw., ist auch in Exchange Online gespeichert werden können, aber die meisten kommunikationsdatensätze vorübergehend auf Call Detail-Eintrag (CDR) Servern gespeichert sind. Inhalt nicht pro Mandant partitioniert ist, sondern mehrmandantenfähigkeit durch RBAC erzwungen wird.

## <a name="sharepoint-online"></a>SharePoint Online
Es gibt mehrere unabhängige Mechanismen für SharePoint Online, die Daten isolieren eindeutig. SharePoint Online werden Objekte als abstrahiert Code in Datenbanken gespeichert. Beispielsweise wenn ein Benutzer eine Datei mit SharePoint Online hochgeladen wird, ist diese Datei zerlegt und in der Anwendungscode übersetzt und in mehreren Tabellen in mehreren Datenbanken gespeichert.

Wenn ein Benutzer direkt den Speicher mit den Daten zugreifen kann, würde die Inhalte nicht an eine Person oder ein System als SharePoint Online Ingenieure. Diese Mechanismen umfassen Sicherheit Steuerung des Zugriffs und Eigenschaften. Wie oben beschrieben, sind alle SharePoint Online-Ressourcen durch den Autorisierungscode und RBAC-Richtlinien, einschließlich innerhalb eines Mandanten gesichert. Die Zugriffssteuerungsliste (ACL), die eine Ressource sichert enthält eine Identität, die auf der Ebene der Mandant authentifiziert wird. Wie bei Exchange Online, SharePoint Online können Daten für einen bestimmten Mandanten nur Identitäten authentifiziert anhand des Mandanten Authentifizierungsanbieter, die diese Mandanten nur Benutzer enthalten.

Zusätzlich zu der ACLs eine Mandanten Level-Eigenschaft, die angibt, den Authentifizierungsanbieter (die Mandanten-spezifischen Azure Active Directory ist), wird einmal geschrieben und kann nicht geändert werden, nach dem festlegen. Nach die Authentifizierung Provider Mandanten-Eigenschaft für einen Mandanten festgelegt wurde, kann es nicht in eine beliebige APIs verfügbar gemacht werden, um einen Mandanten geändert werden.

Eine eindeutige *SubscriptionId* wird auch für jeden Mandanten verwendet. Alle Kundenstandorten gehören einen Mandanten und eine eindeutige *SubscriptionId* den Mandanten zugewiesen sind. Die *SubscriptionId* -Eigenschaft auf einer Website wird einmal geschrieben und kann nicht geändert werden. Nach eine Website einen Mandanten zugewiesen ist, kann es auf einen anderen Mandanten später mit der API Inhaltsspeicher verschoben werden. Die *SubscriptionId* ist auch der Schlüssel, der zum Erstellen des Sicherheitsbereichs für den Authentifizierungsanbieter verwendet wird und auf den Mandanten gebunden ist.

SharePoint Online verwendet den SQL Server und Azure-Speicher für das Speichern von Inhalten. Auf der Ebene SQL ist der Partitionsschlüssel für den Inhaltsspeicher *SiteId*. Wenn Sie eine SQL-Abfrage ausführen, verwendet SharePoint Online eine *SiteId* , der überprüft wurde als Teil der eine Überprüfung auf Mandantenebene *SubscriptionId* .

SharePoint Online speichert Datei binäre Blobs (z. B. die Datei Datenströme) in Microsoft Azure. Jede SharePoint Online Farm weist ein eigene Microsoft Azure-Konto und alle Blobs, die in Azure gespeichert werden einzeln mit einem Schlüssel, der in den SQL-Inhaltsspeicher gespeichert ist verschlüsselt. Der Verschlüsselungsschlüssel nicht direkt an die Endbenutzer verfügbar gemacht, und im Code durch die Ebene des Genehmigung geschützt ist. Schließlich verfügt SharePoint Online direkt zu erkennen, wann eine HTTP-Anforderung liest oder Daten für mehrere Mandanten schreibt Echtzeit zu überwachen. Dies geschieht durch die Ermittlung der *SubscriptionId* der Anforderungsidentität anhand der *SubscriptionId* der Ressource zugegriffen wird. Eine Anforderung, die Zugriff auf Ressourcen von mehreren Mandanten sollte vom Endbenutzer nie eintreten. Es kann jedoch für Serviceanfragen in einer Umgebung mit mehreren Mandanten vorkommen. Der Suchcrawler zieht inhaltlichen Änderungen für eine gesamte Datenbank beispielsweise alle gleichzeitig. Dieser Schritt umfasst in der Regel das Abfragen von Websites für mehrere Mandanten in einer Anforderung Dienst für einmaliges, die aus Gründen der Effizienz ausgeführt wird.

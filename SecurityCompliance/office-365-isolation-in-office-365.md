---
title: Office 365-Isolierung und Zugriffssteuerung in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine Erläuterung der Isolierung und der Zugriffssteuerung in den verschiedenen Anwendungen von Office 365.'
ms.openlocfilehash: 748da21f5b5048bb4ae4c14700ed482fd6d0058c
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402893"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolierung und Zugriffskontrolle in Office 365

Azure Active Directory und Office 365 verwenden ein hoch komplexes Datenmodell, das Dutzende von Diensten, Hunderte von Entitäten, Tausende von Beziehungen und Zehntausende von Attributen umfasst. Auf hoher Ebene sind Azure Active Directory und die Dienst Verzeichnisse die Container von Mandanten und Empfängern, die mithilfe von statusbasierten Replikationsprotokollen synchronisiert werden. Zusätzlich zu den Verzeichnisinformationen, die in Azure Active Directory gespeichert sind, verfügt jede Dienstauslastung über eine eigene Verzeichnisdienstinfrastruktur.
 
![Office 365-Mandantendaten Synchronisierung](media/office-365-isolation-tenant-data-sync.png)

Innerhalb dieses Modells gibt es keine einzige Quelle für Verzeichnisdaten. Bestimmte Systeme besitzen einzelne Daten, aber kein einzelnes System enthält alle Daten. Office 365-Dienste kooperieren mit Azure Active Directory in diesem Datenmodell. Azure Active Directory ist das "System der Wahrheit" für freigegebene Daten, die in der Regel kleine und statische Daten, die von jedem Dienst verwendet werden. Das in Office 365 und Azure Active Directory verwendete Verbundmodell stellt die freigegebene Ansicht der Daten bereit.

Office 365 verwendet sowohl physischen Speicher als auch Azure-cloudspeicher. Exchange Online (einschließlich Exchange Online Protection) und Skype for Business verwenden ihren eigenen Speicher für Kundendaten. SharePoint Online verwendet sowohl SQL Server-Speicher als auch Azure-Speicher und daher die Notwendigkeit einer zusätzlichen Isolierung von Kundendaten auf Speicherebene.

## <a name="exchange-online"></a>Exchange Online

Exchange Online speichert Kundendaten in Postfächern. Postfächer werden in ESE-Datenbanken (Extensible Storage Engine) (Postfachdatenbanken) gehostet. Hierzu gehören Benutzerpostfächer, verknüpfte Postfächer, freigegebene Postfächer und Postfächer für Öffentliche Ordner. Benutzerpostfächer sind gespeicherte Skype for Business-Inhalte wie Unterhaltungs Verläufe.

Zu den Inhalten des Benutzerpostfachs gehören:

- E-Mails und e-Mail-Anhänge
- Kalender-und Frei/Gebucht-Informationen
- Kontakte
- Aufgaben
- Hinweise
- Gruppen
- InFerenz Daten

Jede Postfachdatenbank in Exchange Online enthält Postfächer von mehreren Mandanten. Ein Autorisierungscode sichert jedes Postfach, einschließlich innerhalb eines Mandanten. Standardmäßig hat nur der zugewiesene Benutzer Zugriff auf ein Postfach. Die Zugriffssteuerungsliste (Access Control List, ACL), die ein Postfach sichert, enthält eine von Azure Active Directory auf Mandantenebene authentifizierte Identität. Die Postfächer für jeden Mandanten sind auf Identitäten beschränkt, die mit dem Authentifizierungsanbieter des Mandanten authentifiziert wurden und nur Benutzer von diesem Mandanten enthalten. Inhalte im Mandanten A können von Benutzern in Mandanten B nicht abgerufen werden, es sei denn, Sie werden vom Mandanten A ausdrücklich genehmigt.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business speichert Daten an verschiedenen Stellen:

- Benutzer-und Kontoinformationen, zu denen Verbindungsendpunkte, Mandanten-IDs, Wählpläne, Roamingeinstellungen, Anwesenheitsstatus, Kontaktlisten usw. gehören, werden in den Active Directory-Servern von Skype for Business und in verschiedenen Skype for Business-Datenbankservern gespeichert. Kontaktlisten werden im Exchange Online-Postfach des Benutzers gespeichert, wenn der Benutzer für beide Produkte oder auf Skype for Business-Servern aktiviert ist, wenn der Benutzer dies nicht tut. Skype for Business-Datenbankserver werden nicht pro Mandant partitioniert, aber die mehrinstanzenfähige Isolierung von Daten wird durch die rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC) erzwungen.
- Besprechungsinhalte und hochgeladene Daten werden auf DFS-Freigaben (Distributed File System) gespeichert. Dieser Inhalt kann auch in Exchange Online archiviert werden, wenn diese Option aktiviert ist. Die DFS-Freigaben werden nicht pro Mandant partitioniert. der Inhalt wird mit ACLs gesichert, und Mehrmandantenfähigkeit wird über RBAC erzwungen.
- Anruf Detaildatensätze, die den Aktivitätsverlauf, wie Anrufverlauf, Sofortnachrichtensitzungen, Anwendungsfreigabe, Instant Messaging-Verlauf usw., enthalten, können auch in Exchange Online gespeichert werden, die meisten Datensätze für Anrufdetails werden jedoch vorübergehend auf einem KDS-Server (Call Detail Record) gespeichert. Inhalte werden nicht pro Mandant partitioniert, Mehrmandantenfähigkeit wird jedoch über RBAC erzwungen.

## <a name="sharepoint-online"></a>SharePoint Online

SharePoint Online verfügt über mehrere unabhängige Mechanismen zur Datenisolierung. Sie speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer beispielsweise eine Datei in SharePoint Online hochlädt, wird die Datei zerlegt, in den Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken gespeichert.

Wenn ein Benutzer direkten Zugriff auf den Speicher erhalten kann, der die Daten enthält, kann er nicht für ein anderes System als SharePoint Online interpretiert werden. Zu diesen Mechanismen gehört die Sicherheit Zugriffssteuerung und Eigenschaften. Alle SharePoint Online-Ressourcen werden durch den Autorisierungscode und die RBAC-Richtlinie gesichert, einschließlich innerhalb eines Mandanten. Die Zugriffssteuerungsliste (Access Control List, ACL), die eine Ressource sichert, enthält eine auf Mandantenebene authentifizierte Identität. SharePoint Online-Daten für einen Mandanten sind auf vom Authentifizierungsanbieter für den Mandanten authentifizierte Identitäten beschränkt.

Zusätzlich zu den ACLs wird eine Eigenschaft auf Mandantenebene, die den Authentifizierungsanbieter (der mandantenspezifische Azure Active Directory) angibt, einmal geschrieben und kann nicht mehr geändert werden, nachdem festgelegt. Nachdem die Mandanten Eigenschaft des Authentifizierungsanbieters für einen Mandanten festgelegt wurde, kann Sie nicht mit allen APIs geändert werden, die für einen Mandanten verfügbar gemacht werden.

Für jeden ** Mandanten wird ein eindeutiger Subskriptionswert verwendet. Alle Kunden Websites sind Besitzer eines Mandanten und weisen dem ** Mandanten eine einmalige Subskriptionsnummer zu. Die *Subscription* -Eigenschaft auf einer Website wird einmal geschrieben und ist dauerhaft. Nachdem ein Standort einem Mandanten zugewiesen wurde, kann er nicht in einen anderen Mandanten verschoben werden. Die *Subscription* -Wert ist der Schlüssel, der zum Erstellen des Sicherheitsbereichs für den Authentifizierungsanbieter verwendet wird und an den Mandanten gebunden ist.

SharePoint Online verwendet SQL Server und Azure Storage für die Speicherung von Inhaltsmetadaten. Der Partitionsschlüssel für den Inhaltsspeicher ist *Site* -Nr. in SQL. Beim Durchführen einer SQL-Abfrage verwendet SharePoint Online eine *Website* -Nr, die im Rahmen einer ** Überprüfung auf Mandantenebene überprüft wurde.

SharePoint Online speichert verschlüsselte Dateiinhalte in Microsoft Azure-BLOBs. Jede SharePoint Online-Farm verfügt über ein eigenes Microsoft Azure-Konto, und alle in Azure gespeicherten BLOBs werden einzeln mit einem Schlüssel verschlüsselt, der im SQL-Inhaltsspeicher gespeichert ist. Der Verschlüsselungsschlüssel, der von der Autorisierungs Schicht im Code geschützt und nicht direkt für den Endbenutzer verfügbar gemacht wird. SharePoint Online verfügt über Echtzeitüberwachung, um zu bestimmen, wann eine HTTP-Anforderung Daten für mehrere Mandanten liest oder schreibt. Die *Abonnement* -ID für die Anforderungsidentität wird mit der *Abonnement* Kennung der aufgerufenen Ressource verfolgt. Anforderungen für den Zugriff auf Ressourcen von mehr als einem Mandanten sollten nie von Endbenutzern ausgeführt werden. Dienstanforderungen in einer Umgebung mit mehreren Mandanten sind die einzige Ausnahme. Beispielsweise zieht der Suchcrawler Inhaltsänderungen für eine gesamte Datenbank auf einmal. Dies umfasst in der Regel das Abfragen von Websites mehrerer Mandanten in einer einzigen Serviceanforderung, was aus Effizienzgründen erfolgt.

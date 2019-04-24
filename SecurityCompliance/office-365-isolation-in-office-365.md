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
ms.openlocfilehash: c4328539f8cca5cb7e76c4a3175cfab0a01b42cf
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262622"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolierung und Zugriffskontrolle in Office 365

Azure Active Directory und Office 365 verwenden ein hoch komplexes Datenmodell, das Dutzende von Diensten, Hunderte von Entitäten, Tausende von Beziehungen und Zehntausende von Attributen umfasst (Entitäten, Beziehungen und Attribute sind oft anwendungsspezifisch). Auf hoher Ebene sind Azure Active Directory und die Dienst Verzeichnisse die Container von Mandanten und Empfängern, und Sie werden mit statusbasierten Replikationsprotokollen synchronisiert. Zusätzlich zu den Verzeichnisinformationen in Azure Active Directory verfügt jeder Dienst über eine eigene Verzeichnisdienstinfrastruktur (beispielsweise Exchange Online-Verzeichnisdienste, SharePoint Online-Verzeichnisdienste usw.). 
 
![Office 365-Mandantendaten Synchronisierung](media/office-365-isolation-tenant-data-sync.png)

Innerhalb dieses Modells gibt es keine einzige Quelle für Verzeichnisdaten. Jeder einzelne Datensatz ist im Besitz eines bestimmten Systems, aber kein einzelnes System enthält alle Daten. Office 365-Dienste kooperieren mit Azure Active Directory, um das Datenmodell zu realisieren. Azure Active Directory ist das "System der Wahrheit" für freigegebene Daten, in der Regel kleine und statische Daten, die häufig von jedem Dienst verwendet werden. Das in Office 365 und Azure Active Directory verwendete Verbundmodell stellt die freigegebene Ansicht der Daten bereit.

Office 365 verwendet sowohl physischen Speicher als auch Azure-cloudspeicher. Exchange Online (einschließlich Exchange Online Protection) und Skype for Business verwenden ihren eigenen Speicher für Kundendaten. SharePoint Online nutzt sowohl den SQL Server-Speicher als auch den Azure-Speicher, was die Notwendigkeit einer zusätzlichen Isolierung von Kundendaten auf Speicherebene erfordert.

## <a name="exchange-online"></a>Exchange Online
Exchange Online speichert Kundendaten in Postfächern, die in ESE-Datenbanken (Extensible Storage Engine) als Postfachdatenbanken gehostet werden. Hierzu gehören Benutzerpostfächer, verknüpfte Postfächer, freigegebene Postfächer und Postfächer für Öffentliche Ordner. Benutzerpostfächer können auch gespeicherte Skype for Business-Inhalte wie Unterhaltungs Verläufe aufnehmen. Zu den Inhalten des Benutzerpostfachs Gehören e-Mails und e-Mail-Anhänge, Kalender-und Frei/Gebucht-Informationen, Kontakte, Aufgaben, Notizen, Gruppen und Inferenz Daten.

Jede Postfachdatenbank in Exchange Online enthält Postfächer von mehreren Mandanten. Alle Postfächer werden durch Autorisierungscode gesichert, einschließlich innerhalb eines Mandanten. Wie bei einer lokalen Bereitstellung von Exchange hat nur der zugewiesene Benutzer standardmäßig Zugriff auf ein Postfach. Die Zugriffssteuerungsliste (Access Control List, ACL), die ein Postfach sichert, enthält eine Identität, die von Azure Active Directory auf Mandantenebene authentifiziert wird. Die Postfächer für einen bestimmten Mandanten sind auf Identitäten beschränkt, die für den Authentifizierungsanbieter des Mandanten authentifiziert wurden und nur Benutzer von diesem Mandanten einbeziehen. Inhalte, die zu Tenanta gehören, können von Benutzern in TenantB nicht abgerufen werden, es sei denn, Sie werden von der Mandanta ausdrücklich genehmigt.

## <a name="skype-for-business"></a>Skype for Business
Skype for Business speichert Daten an verschiedenen Stellen:
- Benutzer-und Kontoinformationen, die Verbindungsendpunkte, Mandanten-IDs, Wählpläne, Roamingeinstellungen, Anwesenheitsstatus, Kontaktlisten usw. enthalten, werden in den Active Directory-Servern von Skype for Business sowie in verschiedenen Skype for Business-Datenbanken gespeichert. Server. Kontaktlisten werden im Exchange Online-Postfach des Benutzers gespeichert, wenn der Benutzer für beide Produkte oder auf Skype for Business-Servern aktiviert ist, wenn der Benutzer dies nicht tut. Skype for Business-Datenbankserver werden nicht pro Mandant partitioniert, aber die Mandantenweite Isolierung von Daten wird über RBAC erzwungen.
- Besprechungsinhalte wie Inhalts Benutzer, die während Skype for Business-Besprechungen hochgeladen werden, werden auf verTeilten Datei System Freigaben gespeichert. Dieser Inhalt kann auch in der Exchange Online-Bereitstellung archiviert werden, die für die Archivierung aktiviert ist. Die DFS-Freigaben werden nicht pro Mandant partitioniert, aber der Inhalt wird mit ACLs gesichert, und Mehrmandantenfähigkeit wird über RBAC erzwungen.
- Anruf Detaildatensätze, die den Aktivitätsverlauf, wie Anrufverlauf, Sofortnachrichtensitzungen, Anwendungsfreigabe, Instant Messaging-Verlauf usw., enthalten, können auch in Exchange Online gespeichert werden, die meisten Anruf Detaildatensätze werden jedoch vorübergehend auf einem KDS-Server (Call Detail Record) gespeichert. Inhalte werden nicht pro Mandant partitioniert, Mehrmandantenfähigkeit wird jedoch über RBAC erzwungen.

## <a name="sharepoint-online"></a>SharePoint Online
Es gibt mehrere unabhängige Mechanismen, die für SharePoint Online eindeutig sind und eine Datenisolierung bieten. SharePoint Online speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer beispielsweise eine Datei in SharePoint Online hochlädt, wird diese Datei zerlegt und in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken gespeichert.

Wenn ein Benutzer direkten Zugriff auf den Speicher erhalten kann, der die Daten enthält, wäre der Inhalt nicht für ein menschliches oder ein anderes System als SharePoint Online zu interpretieren. Zu diesen Mechanismen gehört die Sicherheit Zugriffssteuerung und Eigenschaften. Wie oben beschrieben, werden alle SharePoint Online-Ressourcen durch den Autorisierungscode und die RBAC-Richtlinie gesichert, einschließlich innerhalb eines Mandanten. Die Zugriffssteuerungsliste (Access Control List, ACL), die eine Ressource sichert, enthält eine Identität, die auf Mandantenebene authentifiziert wird. Wie bei Exchange Online sind die Daten für einen bestimmten Mandanten in SharePoint Online auf für den Authentifizierungsanbieter des Mandanten authentifizierte Identitäten beschränkt, die nur Benutzer von diesem Mandanten einbeziehen.

Zusätzlich zu den ACLs wird eine Eigenschaft auf Mandantenebene, die den Authentifizierungsanbieter (der mandantenspezifische Azure Active Directory) angibt, einmal geschrieben und kann nicht mehr geändert werden, nachdem festgelegt. Nachdem die Mandanten Eigenschaft des Authentifizierungsanbieters für einen Mandanten festgelegt wurde, kann Sie nicht mit allen APIs geändert werden, die für einen Mandanten verfügbar gemacht werden.

Eine eindeutige *Abonnement* -Nr. wird auch für jeden Mandanten verwendet. Alle Kunden Websites gehören einem Mandanten und werden einem Mandanten ** zugewiesen. Die *Subscription* -Eigenschaft auf einer Website wird einmal geschrieben und kann nicht geändert werden. Sobald eine Website einem Mandanten zugewiesen wurde, kann er später nicht mehr mithilfe der Inhaltsspeicher-API zu einem anderen Mandanten verschoben werden. Die *Subskriptions* -Nr. ist auch der Schlüssel, der zum Erstellen des Sicherheitsbereichs für den Authentifizierungsanbieter verwendet wird und an den Mandanten gebunden ist.

SharePoint Online verwendet SQL Server und Azure Storage zum Speichern von Inhalten. Auf SQL-Ebene ist der Partitionsschlüssel für den Inhaltsspeicher *Site*-Nr. Beim Durchführen einer SQL-Abfrage verwendet SharePoint Online eine *Website* -Nr., die im Rahmen einer Überprüfung ** auf Mandantenebene überprüft wurde.

SharePoint Online speichert binäre BLOBs (beispielsweise die Dateidaten Ströme) in Microsoft Azure. Jede SharePoint Online-Farm verfügt über ein eigenes Microsoft Azure-Konto, und alle in Azure gespeicherten BLOBs werden einzeln mithilfe eines Schlüssels verschlüsselt, der im SQL-Inhaltsspeicher gespeichert ist. Der Verschlüsselungsschlüssel ist nicht direkt für den Endbenutzer verfügbar und wird in Code von der Autorisierungs Schicht geschützt. Schließlich verfügt SharePoint Online über eine Echtzeitüberwachung, um zu bestimmen, wann eine HTTP-Anforderung Daten für mehrere Mandanten liest oder schreibt. Hierzu verfolgt Sie die *Abonnement* -ID der Anforderungsidentität anhand der *Abonnement* Kennung der Ressource, auf die zugegriffen wird. Eine Anforderung für den Zugriff auf Ressourcen von mehr als einem Mandanten sollte nie von Endbenutzern ausgeführt werden. Es kann jedoch für Serviceanforderungen in einer Umgebung mit mehreren Mandanten auftreten. Beispielsweise zieht der Suchcrawler Inhaltsänderungen für eine gesamte Datenbank auf einmal. Dies umfasst in der Regel das Abfragen von Websites mehrerer Mandanten in einer einzigen Serviceanforderung, was aus Effizienzgründen erfolgt.

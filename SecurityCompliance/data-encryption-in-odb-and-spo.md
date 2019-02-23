---
title: Datenverschlüsselung in OneDrive for Business und SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 6501b5ef-6bf7-43df-b60d-f65781847d6c
ms.collection:
- M365-security-compliance
description: Verstehen Sie die grundlegenden Elemente der Verschlüsselung für die Datensicherheit in OneDrive for Business und SharePoint Online.
ms.openlocfilehash: a43db3da6e4663aee4437689ff51276972298872
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223214"
---
# <a name="data-encryption-in-onedrive-for-business-and-sharepoint-online"></a><span data-ttu-id="4a4de-103">Datenverschlüsselung in OneDrive for Business und SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4a4de-103">Data Encryption in OneDrive for Business and SharePoint Online</span></span>

<span data-ttu-id="4a4de-104">Verstehen Sie die grundlegenden Elemente der Verschlüsselung für die Datensicherheit in OneDrive for Business und SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4a4de-104">Understand the basic elements of encryption for data security in OneDrive for Business and SharePoint Online.</span></span>
  
## <a name="overview"></a><span data-ttu-id="4a4de-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4a4de-105">Overview</span></span>

<span data-ttu-id="4a4de-p101">Office 365 ist eine äußerst sichere Umgebung, die umfassenden Schutz auf mehreren Ebenen bietet: physische Sicherheit von Rechenzentren, Netzwerksicherheit, Zugriffssicherheit, Anwendungssicherheit und Datensicherheit. Dieser Artikel befasst sich speziell mit der Verschlüsselung der Datensicherheit während der Übertragung und im Ruhezustand für OneDrive for Business und SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p101">Office 365 is a highly secure environment that offers extensive protection in multiple layers: physical data center security, network security, access security, application security, and data security. This article specifically focuses on the in-transit and at-rest encryption side of data security for OneDrive for Business and SharePoint Online.</span></span>
  
<span data-ttu-id="4a4de-108">Eine Beschreibung der Office 365-Sicherheit als Ganzes finden Sie unter [Security in office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span><span class="sxs-lookup"><span data-stu-id="4a4de-108">For a description of Office 365 security as a whole, see [Security in Office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span></span>
  
<span data-ttu-id="4a4de-109">Sehen Sie sich im folgenden Video an, wie die Datenverschlüsselung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4a4de-109">Watch how data encryption works in the following video.</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/dea0dec4-4077-4095-9a32-19b94ea2da4b?autoplay=false]
  
## <a name="encryption-of-data-in-transit"></a><span data-ttu-id="4a4de-110">Verschlüsselung von Daten während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="4a4de-110">Encryption of data in transit</span></span>

<span data-ttu-id="4a4de-111">In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.</span><span class="sxs-lookup"><span data-stu-id="4a4de-111">In OneDrive for Business and SharePoint Online, there are two scenarios in which data enters and exits the datacenters.</span></span>
  
- <span data-ttu-id="4a4de-p102">**Clientkommunikation mit dem Server** Bei der Kommunikation mit OneDrive for Business über das Internet werden SSL/TLS-Verbindungen verwendet. Alle SSL-Verbindungen werden mit 2048-Bit-Schlüsseln hergestellt.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p102">**Client communication with the server** Communication to OneDrive for Business across the Internet uses SSL/TLS connections. All SSL connections are established using 2048-bit keys.</span></span> 
    
- <span data-ttu-id="4a4de-p103">**Datenverschiebung zwischen Rechenzentren** Der wichtigste Grund zum Verschieben von Daten zwischen Rechenzentren ist die Georeplikation für die Notfallwiederherstellung. Beispielsweise werden SQL Server-Transaktionsprotokolle und BLOB-Speicher-Deltas entlang dieser Pipe übertragen. Während diese Daten bereits über ein privates Netzwerk übertragen werden, werden sie zusätzlich durch branchenbeste Verschlüsselung geschützt.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p103">**Data movement between datacenters** The primary reason to move data between datacenters is for geo-replication to enable disaster recovery. For instance, SQL Server transaction logs and blob storage deltas travel along this pipe. While this data is already transmitted by using a private network, it is further protected with best-in-class encryption.</span></span> 
    
## <a name="encryption-of-data-at-rest"></a><span data-ttu-id="4a4de-117">Verschlüsselung von Daten im Ruhezustand</span><span class="sxs-lookup"><span data-stu-id="4a4de-117">Encryption of data at rest</span></span>

<span data-ttu-id="4a4de-118">Die Verschlüsselung im Ruhezustand enthält zwei Komponenten: BitLocker-Verschlüsselung auf Datenträgerebene und dateispezifische Verschlüsselung von Kundeninhalten.</span><span class="sxs-lookup"><span data-stu-id="4a4de-118">Encryption at rest includes two components: BitLocker disk-level encryption and per-file encryption of customer content.</span></span>
  
<span data-ttu-id="4a4de-p104">BitLocker wird für OneDrive for Business und SharePoint Online im gesamten Dienst bereitgestellt. Die Verschlüsselung per Datei befindet sich auch in OneDrive for Business und SharePoint Online in Office 365 mit mehreren Mandanten und neuen dedizierten Umgebungen, die auf mandantenfähiger Technologie basieren.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p104">BitLocker is deployed for OneDrive for Business and SharePoint Online across the service. Per-file encryption is also in OneDrive for Business and SharePoint Online in Office 365 multi-tenant and new dedicated environments that are built on multi-tenant technology.</span></span>
  
<span data-ttu-id="4a4de-p105">Während alle Daten auf einem Datenträger mit BitLocker verschlüsselt werden, geht die Dateiverschlüsselung sogar noch weiter, indem ein eindeutiger Schlüssel für jede Datei eingeschlossen wird. Darüber hinaus wird jede Aktualisierung jeder Datei mit einem eigenen Schlüssel verschlüsselt. Bevor sie gespeichert werden, werden die Schlüssel für die verschlüsselten Inhalte an einem vom Inhalt separaten Speicherort gespeichert. Jeder Schritt der Verschlüsselung verwendet AES (Advanced Encryption Standard, erweiterter Verschlüsselungsstandard) mit 256-Bit-Schlüsseln und ist zu FIPS 140-2 (Federal Information Processing Standard) kompatibel. Die verschlüsselten Inhalte werden auf einer Reihe von Containern im gesamten Rechenzentrum verteilt, und jeder Container besitzt eindeutige Anmeldeinformationen. Diese Anmeldeinformationen werden in einem vom Inhalt oder den Inhaltsschlüsseln separaten physischen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p105">While BitLocker encrypts all data on a disk, per-file encryption goes even further by including a unique encryption key for each file. Further, every update to every file is encrypted using its own encryption key. Before they're stored, the keys to the encrypted content are stored in a physically separate location from the content. Every step of this encryption uses Advanced Encryption Standard (AES) with 256-bit keys and is Federal Information Processing Standard (FIPS) 140-2 compliant. The encrypted content is distributed across a number of containers throughout the datacenter, and each container has unique credentials. These credentials are stored in a separate physical location from either the content or the content keys.</span></span>
  
<span data-ttu-id="4a4de-127">Weitere Informationen zur FIPS 140-2-Kompatibilität finden Sie unter [fips 140-2 Compliance](https://go.microsoft.com/fwlink/?LinkId=517625).</span><span class="sxs-lookup"><span data-stu-id="4a4de-127">For additional information about FIPS 140-2 compliance, see [FIPS 140-2 Compliance](https://go.microsoft.com/fwlink/?LinkId=517625).</span></span>
  
<span data-ttu-id="4a4de-p106">Die Verschlüsselung auf Dateiebene nutzt den BLOB-Speicher, um nahezu unbegrenzte Speicherkapazität zu schaffen und einen beispiellosen Schutz zu ermöglichen. Alle Kunden Inhalte in OneDrive for Business und SharePoint Onlinewill werden in den BLOB-Speicher migriert. Hier erfahren Sie, wie diese Daten gesichert werden:</span><span class="sxs-lookup"><span data-stu-id="4a4de-p106">File-level encryption at rest takes advantage of blob storage to provide for virtually unlimited storage growth and to enable unprecedented protection. All customer content in OneDrive for Business and SharePoint Onlinewill be migrated to blob storage. Here's how that data is secured:</span></span>
  
1. <span data-ttu-id="4a4de-p107">Alle Inhalte werden, möglicherweise mit mehreren Schlüsseln, verschlüsselt und über Rechenzentren verteilt. Jede zu speichernde Datei wird je nach der Größe in einen oder mehrere Blöcke aufgeteilt. Dann wird jeder Block mit einem eigenen eindeutigen Schlüssel verschlüsselt. Aktualisierungen werden auf ähnliche Weise behandelt: Der Satz von Änderungen oder Deltas, die von einem Benutzer übermittelt werden, wird in Blöcke unterteilt, und jeder wird mit einem eigenen Schlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p107">All content is encrypted, potentially with multiple keys, and distributed across the datacenter. Each file to be stored is broken into one or more chunks, depending its size. Then, each chunk is encrypted using its own unique key. Updates are handled similarly: the set of changes, or deltas, submitted by a user is broken into chunks, and each is encrypted with its own key.</span></span>
    
2. <span data-ttu-id="4a4de-p108">Alle diese Blöcke - Dateien, Teile von Dateien und Aktualisierungsdeltas - werden als BLOBs in unserem BLOB-Speicher gespeichert. Sie werden zudem nach dem Zufallsprinzip auf mehrere BLOB-Container verteilt.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p108">All of these chunks—files, pieces of files, and update deltas—are stored as blobs in our blob store. They also are randomly distributed across multiple blob containers.</span></span>
    
3. <span data-ttu-id="4a4de-137">Die für das erneute Zusammensetzen der Datei aus ihren Komponenten verwendete „Karte" wird in der Inhaltsdatenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a4de-137">The "map" used to re-assemble the file from its components is stored in the Content Database.</span></span>
    
4. <span data-ttu-id="4a4de-p109">Jeder BLOB-Container besitzt eigene eindeutige Anmeldeinformationen pro Zugriffstyp (Lesen, Schreiben, Aufzählen und Löschen). Jeder Satz von Anmeldeinformationen wird im sicheren Schlüsselspeicher aufbewahrt und regelmäßig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p109">Each blob container has its own unique credentials per access type (read, write, enumerate, and delete). Each set of credentials is held in the secure Key Store and is regularly refreshed.</span></span>
    
<span data-ttu-id="4a4de-140">Anders gesagt, sind drei unterschiedliche Arten von Speicher an der Verschlüsselung im Ruhezustand beteiligt, jede mit einer anderen Funktion:</span><span class="sxs-lookup"><span data-stu-id="4a4de-140">In other words, there are three different types of stores involved in per-file encryption at rest, each with a distinct function:</span></span>
  
- <span data-ttu-id="4a4de-p110">Inhalt wird als verschlüsselte BLOBs im BLOB-Speicher gespeichert. Der Schlüssel für jeden Inhaltsblock wird verschlüsselt und separat in der Inhaltsdatenbank gespeichert. Der Inhalt selbst enthält keinen Hinweis darauf, wie er entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p110">Content is stored as encrypted blobs in the blob store. The key to each chunk of content is encrypted and stored separately in the content database. The content itself holds no clue as to how it can be decrypted.</span></span>
    
- <span data-ttu-id="4a4de-p111">Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Sie enthält die Karte zum Suchen und erneuten Zusammensetzen aller Inhalts-BLOBs im BLOB-Speicher sowie die Schlüssel zum Entschlüsseln dieser BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p111">The Content Database is a SQL Server database. It holds the map required to locate and reassemble all of the content blobs held in the blob store as well as the keys needed to decrypt those blobs.</span></span>
    
<span data-ttu-id="4a4de-p112">Jede dieser drei Speicherkomponenten - BLOB-Speicher, Inhaltsdatenbank und Schlüsselspeicher - ist physisch getrennt. Die Informationen in einer der Komponenten sind allein unbrauchbar. Dies bietet eine einzigartige Sicherheitsstufe. Ohne Zugriff auf alle drei ist es unmöglich, die Schlüssel für die Datenblöcke abzurufen, die Schlüssel zu entschlüsseln, um sie verwendbar zu machen, die Schlüssel ihren entsprechenden Datenblöcken zuzuordnen, einen Block zu entschlüsseln oder ein Dokument aus den einzelnen Blöcken zusammenzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4a4de-p112">Each of these three storage components—the blob store, the Content Database, and the Key Store—is physically separate. The information held in any one of the components is unusable on its own. This provides an unprecedented level of security. Without access to all three it is impossible to retrieve the keys to the chunks, decrypt the keys to make them usable, associate the keys with their corresponding chunks, decrypt any chunk, or reconstruct a document from its constituent chunks.</span></span>
  


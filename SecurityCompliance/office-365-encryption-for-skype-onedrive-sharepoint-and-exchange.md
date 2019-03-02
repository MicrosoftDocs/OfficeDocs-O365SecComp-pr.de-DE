---
title: Office 365-Verschlüsselung für Skype, OneDrive, SharePoint und Exchange
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Zusammenfassung: eine Beschreibung der Verschlüsselung für Skype, OneDrive, SharePoint und Exchange Online.'
ms.openlocfilehash: 55141f671e6cb3d7ea837bfcf9701e37a18fb7ba
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357566"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>Office 365-Verschlüsselung für Skype for Business, OneDrive for Business, SharePoint Online und Exchange Online

Office 365 ist eine hochsichere Umgebung, die umfassenden Schutz in mehreren Schichten bietet: physische rechenzentrumssicherheit, Netzwerksicherheit, Zugriffssicherheit, Anwendungssicherheit und Datensicherheit.

## <a name="skype-for-business"></a>Skype for Business

Kundendaten von Skype for Business können im Ruhezustand in Form von Dateien oder Präsentationen gespeichert werden, die von Besprechungsteilnehmern hochgeladen werden. Der Webkonferenzserver verschlüsselt Kundendaten mithilfe von AES mit einem 256-Bit-Schlüssel. Die verschlüsselten Kundendaten werden in einer Dateifreigabe gespeichert. Jeder Teil der Kundendaten wird mit einem anderen zufällig generierten 256-Bit-Schlüssel verschlüsselt. Wenn ein Teil der Kundendaten in einer Konferenz freigegeben wird, weist der Webkonferenzserver die Konferenz Clients an, die verschlüsselten Kundendaten über HTTPS herunterzuladen. Der entsprechende Schlüssel wird an Clients gesendet, damit die Kundendaten entschlüsselt werden können. Der Webkonferenzserver authentifiziert außerdem Konferenz Clients, bevor Clients den Zugriff auf Konferenz Kundendaten ermöglichen. Wenn Sie einer Webkonferenz beitreten, richtet jeder Konferenz Client zunächst ein SIP-Dialogfeld mit der Konferenz Fokus Komponente ein, die auf dem Front-End-Server über TLS läuft. Der Konferenz Fokus übergibt ein vom Webkonferenzserver generiertes Authentifizierungscookie an den Conference-Client. Der Konferenz Client stellt dann eine Verbindung mit dem Webkonferenzserver her, der das Authentifizierungscookie darstellt, das vom Server authentifiziert werden soll.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business

Alle Kundendateien in SharePoint Online werden durch eindeutige, dateispezifische Schlüssel geschützt, die immer exklusiv für einen einzelnen Mandanten sind. Die Schlüssel werden entweder vom SharePoint Online-Dienst erstellt und verwaltet, oder wenn der Kundenschlüssel verwendet, erstellt und von Kunden verwaltet wird. Wenn eine Datei hochgeladen wird, wird die Verschlüsselung von SharePoint Online im Kontext der Upload-Anforderung durchgeführt, bevor Sie an Azure Storage gesendet wird. Wenn eine Datei heruntergeladen wird, ruft SharePoint Online die verschlüsselten Kundendaten anhand der eindeutigen Dokument-ID aus dem Azure-Speicher ab und entschlüsselt die Kundendaten, bevor Sie an den Benutzer gesendet werden. Azure Storage hat keine Möglichkeit, die Kundendaten zu entschlüsseln oder sogar zu identifizieren oder zu verstehen. Alle Verschlüsselung und Entschlüsselung erfolgen in den gleichen Systemen, die die Mandanten Isolierung erzwingen, die Azure Active Directory und SharePoint Online sind.

Mehrere Arbeitsauslastungen in Office 365 speichern Daten in SharePoint Online, einschließlich Microsoft Teams, in dem alle Dateien in SharePoint Online gespeichert sind, und OneDrive for Business, das SharePoint Online für seinen Speicher verwendet. Alle in SharePoint Online gespeicherten Kundendaten werden (mit einem oder mehreren AES 256-Bit-Schlüssel) verschlüsselt und über das Rechenzentrum wie folgt verteilt. (Jeder Schritt dieses Verschlüsselungsvorgangs ist FIPS 140-2 Level 2 validiert. Weitere Informationen zur FIPS 140-2-Kompatibilität finden Sie unter [fips 140-2 Compliance](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)

- Jede Datei wird je nach Dateigröße in einen oder mehrere Abschnitte aufgeteilt. Jeder Chunk wird mit seinem eigenen eindeutigen AES-256-Bit-Schlüssel verschlüsselt.
- Wenn eine Datei aktualisiert wird, wird das Update auf die gleiche Weise behandelt: die Änderung wird in einen oder mehrere Abschnitte aufgeteilt, und jeder Chunk wird mit einem separaten eindeutigen Schlüssel verschlüsselt.
- Diese Chunks – Dateien, Dateien und Update-Deltas – werden als BLOBs im Azure-Speicher gespeichert, die nach dem Zufallsprinzip über mehrere Azure-Speicherkonten verteilt werden.
- Die Verschlüsselungsschlüssel für diese Kundendaten Segmente werden selbst verschlüsselt.

    - Die Schlüssel, die zum Verschlüsseln der Blobs verwendet werden, werden in der SharePoint Online-Inhaltsdatenbank gespeichert.
    - Die Inhaltsdatenbank wird durch Datenbankzugriffs Steuerelemente und Verschlüsselung geschützt. Die Verschlüsselung wird mithilfe der [transparentEn Datenverschlüsselung](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (DSA) in der [Azure SQL-Datenbank](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview)ausgeführt. (Azure SQL Database ist ein universeller relationaler Datenbankdienst in Microsoft Azure, der Strukturen wie relationale Daten, JSON, Spatial und XML unterstützt.) Diese Geheimnisse befinden sich auf Dienstebene für SharePoint Online, nicht auf Mandantenebene. Diese Geheimnisse (auch als Hauptschlüssel bezeichnet) werden in einem separaten sicheren Repository gespeichert, das als Schlüsselspeicher bezeichnet wird. DSA bietet Sicherheit in Ruhe sowohl für die aktive Datenbank als auch für die Datenbanksicherungen und Transaktionsprotokolle.
    - Wenn Kunden den optionalen Schlüssel angeben, wird der Kundenschlüssel in Azure Key Vault gespeichert, und der Dienst verwendet den Schlüssel, um einen Mandanten Schlüssel zu verschlüsseln, der verwendet wird, um einen Website Schlüssel zu verschlüsseln, der dann zum Verschlüsseln der Tasten auf Dateiebene verwendet wird. Im Wesentlichen wird eine neue Schlüsselhierarchie eingeführt, wenn der Kunde einen Schlüssel bereitstellt.
- Die Karte, die zum erneuten zusammensetzen der Datei verwendet wird, wird zusammen mit den verschlüsselten Schlüsseln in der Inhaltsdatenbank gespeichert, getrennt vom Hauptschlüssel, der zum Entschlüsseln erforderlich ist.
- Jedes Azure-Speicherkonto verfügt über eigene eindeutige Anmeldeinformationen pro Zugriffstyp (lesen, schreiben, auflisten und löschen). Jeder Satz von Anmeldeinformationen wird im Secure Key Store aufbewahrt und regelmäßig aktualisiert. Wie oben beschrieben, gibt es drei verschiedene Arten von speichern, die jeweils eine eigene Funktion aufweisen:
    - Kundendaten werden als verschlüsselte BLOBs im Azure-Speicher gespeichert. Der Schlüssel für jeden Kundendaten Block wird in der Inhaltsdatenbank verschlüsselt und separat gespeichert. Die Kundendaten selbst haben keine Ahnung, wie Sie entschlüsselt werden können.
    - Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Die Zuordnung ist erforderlich, um die im Azure-Speicher gespeicherten Kundendaten-BLOBs sowie die Schlüssel zum Verschlüsseln dieser BLOBs zu finden und wieder zusammenzusetzen. Die Schlüssel Gruppe ist jedoch selbst verschlüsselt (wie oben beschrieben) und in einem separaten Schlüsselspeicher gespeichert.
    - Der Schlüsselspeicher ist physisch von der Inhaltsdatenbank und dem Azure-Speicher getrennt. Sie enthält die Anmeldeinformationen für jeden Azure-Speichercontainer und den Hauptschlüssel für die in der Inhaltsdatenbank enthaltenen verschlüsselten Schlüssel.

Jede dieser drei Speicherkomponenten – der Azure-BLOB-Speicher, die Inhaltsdatenbank und der Schlüsselspeicher – ist physisch getrennt. Die Informationen, die in einer der Komponenten aufbewahrt werden, sind nicht verwendbar. Ohne Zugriff auf alle drei ist es unmöglich, die Schlüssel zu den Chunks abzurufen, die Schlüssel zu entschlüsseln, um Sie nutzbar zu machen, die Schlüssel mit ihren entsprechenden Chunks zu verbinden, die einzelnen Abschnitte zu entschlüsseln oder ein Dokument aus den zugehörigen Chunks zu erstellen.

BitLocker-Zertifikate, die die physischen Datenträger auf Computern im Datencenter schützen, werden in einem sicheren Repository (dem SharePoint Online Secret Store) gespeichert, das durch den Farm Schlüssel geschützt ist.

Die DSA-Schlüssel, die die Schlüssel pro BLOB schützen, werden an zwei Speicherorten gespeichert:

- Das Secure Repository, in dem sich die BitLocker-Zertifikate befinden und durch den Farm Schlüssel geschützt sind; und
- In einem sicheren Repository, verwaltet von der Azure SQL-Datenbank.

Die Anmeldeinformationen, die für den Zugriff auf die Azure-Speichercontainer verwendet werden, befinden sich auch in SharePoint Online Secret Store und werden bei Bedarf an jede SharePoint Online-Farm delegiert. Diese Anmeldeinformationen sind Azure Storage SAS-Signaturen, mit getrennten Anmeldeinformationen, die zum Lesen oder Schreiben von Daten verwendet werden, und mit angewendeten Richtlinien, sodass Sie alle 60 Tage automatisch ablaufen. Zum Lesen oder Schreiben von Daten (nicht beide) werden unterschiedliche Anmeldeinformationen verwendet, und SharePoint Online-Farmen erhalten keine Berechtigungen zum auflisten.

> [!NOTE]
> Für Office 365 US Government-Kunden werden Daten-BLOBs in Azure U.S. Government Storage gespeichert. Darüber hinaus ist der Zugriff auf SharePoint Online-Schlüssel in Office 365 U.S. Government auf Office 365-Mitarbeiter beschränkt, die speziell abgeschirmt wurden. Die Mitarbeiter der Azure U.S. Government-Abteilung haben keinen Zugriff auf den SharePoint Online-Schlüsselspeicher, der zum Verschlüsseln von Daten-BLOBs verwendet wird.

Weitere Informationen zur Datenverschlüsselung in SharePoint Online und OneDrive for Business finden Sie unter [Datenverschlüsselung in OneDrive for Business und SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Listenelemente in SharePoint Online

Listenelemente sind kleinere Kundendaten Segmente, die Ad-hoc erstellt werden oder die innerhalb einer Website dynamischer sein können, beispielsweise Zeilen in einer vom Benutzer erstellten Liste, einzelne Beiträge in einem SharePoint Online-Blog oder Einträge in einer SharePoint Online-Wiki-Seite. Listenelemente werden in der Inhaltsdatenbank (Azure SQL-Datenbank) gespeichert und mit DSA geschützt.

## <a name="encryption-of-data-in-transit"></a>Verschlüsselung von Daten während der Übertragung

In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.

- **Die Client Kommunikation mit der Server** -Kommunikation zu OneDrive for Business über das Internet verwendet SSL/TLS-Verbindungen. Alle SSL-Verbindungen werden mit 2048-Bit-Schlüsseln hergestellt.
- **Datenverlagerung zwischen Rechenzentren** – der Hauptgrund für das Verschieben von Daten zwischen Rechenzentren ist die Geo-Replikation zur Aktivierung der Notfallwiederherstellung. Beispielsweise Reisen SQL Server-Transaktionsprotokolle und BLOB-Speicher-Deltas entlang dieser Pipe. Während diese Daten bereits über ein privates Netzwerk übertragen werden, wird Sie durch die erstklassige Verschlüsselung weiter geschützt.

## <a name="exchange-online"></a>Exchange Online

Exchange Online verwendet BitLocker für alle Postfachdaten, und die BitLocker-Konfiguration wird unter [BitLocker for Encryption](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)beschrieben. Verschlüsselung auf Dienstebene verschlüsselt alle Postfachdaten auf Postfachebene. 

Zusätzlich zur Dienst Verschlüsselung unterstützt Office 365 den Kundenschlüssel, der auf der Dienst Verschlüsselung basiert. Der Kundenschlüssel ist eine von Microsoft verwaltete Schlüssel Option für die Exchange Online-Dienst Verschlüsselung, die auch auf der Microsoft-Roadmap steht. Diese Verschlüsselungsmethode bietet erhöhten Schutz, der nicht durch BitLocker gewährt wurde, da Sie eine Trennung der Serveradministratoren und der für die Entschlüsselung von Daten erforderlichen kryptografischen Schlüssel bietet, und weil die Verschlüsselung direkt auf die Daten angewendet wird (in Kontrast mit BitLocker, wodurch die Verschlüsselung auf dem logischen Datenträgervolume angewendet wird) alle von einem Exchange-Server kopierten Kundendaten bleiben verschlüsselt.

Der Bereich für die Exchange Online-Dienst Verschlüsselung besteht aus Kundendaten, die in Exchange Online gespeichert werden. (Skype for Business speichert nahezu alle vom benutzergenerierten Inhalte innerhalb des Exchange Online-Postfachs des Benutzers und erbt daher das Dienst Verschlüsselungsfeature von Exchange Online.)

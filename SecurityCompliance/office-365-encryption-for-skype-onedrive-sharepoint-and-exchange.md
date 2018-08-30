---
title: Office 365-Verschlüsselung für Skype, OneDrive, SharePoint und Exchange
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
description: 'Zusammenfassung: Eine Beschreibung der Verschlüsselung für Skype, OneDrive, SharePoint und Exchange Online.'
ms.openlocfilehash: 5b839b8d290306f2334d3ca3278d0d5dac20a56f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529463"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>Office 365-Verschlüsselung für Skype für Unternehmen, OneDrive für Unternehmen, SharePoint Online und Exchange Online

Office 365 ist eine sehr sicheren Umgebung, die bietet umfassende Schutz in mehreren Ebenen: physischen Rechenzentrums-Sicherheit, Netzwerksicherheit, zugriffssicherheit, anwendungssicherheit und datensicherheit.

## <a name="skype-for-business"></a>Skype for Business
Skype für Geschäftsdaten-Kunden kann gespeichert werden, im Ruhezustand in Form von Dateien oder Präsentationen, die von Besprechungsteilnehmern hochgeladen werden. Der Webkonferenzserver werden Kundendaten mithilfe von mit einem Schlüssel 256-Bit-AES verschlüsselt. Die verschlüsselte Kundendaten werden in einer Dateifreigabe gespeichert. Jedes Datenelement Kunden ist mit einem anderen willkürlich generierten 256-Bit-Schlüssel verschlüsselt. Wenn ein Inhaltselement Kundendaten in einer Konferenz gemeinsam genutzt wird, weist der Webkonferenzserver die Live Meeting-Clients zum Herunterladen der verschlüsselten Kundendaten über HTTPS. Es sendet den entsprechenden Schlüssel für Clients, sodass die Kundendaten entschlüsselt werden können. Der Webkonferenzserver authentifiziert auch Live Meeting-Clients, bevor die Clients Zugriff auf Kundendaten Konferenz können. Bei der Teilnahme an einer Webkonferenz Richtet jede Konferenzclient ein SIP-Dialogfeld mit der Fokus-Komponente innerhalb des Front-End-Servers über TLS zunächst ausführen. Konferenzen der Übergabe des Fokus an den Client Konferenz ein Authentifizierungscookie vom Server Webkonferenzen generiert werden. Anschließend verbindet der Live Meeting-Client mit dem Webkonferenzserver Präsentation das Authentifizierungscookie vom Server authentifiziert werden.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business
Alle Kundendateien in SharePoint Online werden durch eindeutige, pro Datei Schlüssel geschützt, die immer nur für einen einzelnen Mandanten sind. Die Schlüssel erstellt und von der SharePoint Online-Dienst verwaltet werden, oder wenn Kundenschlüssel verwendet wird, erstellt und verwaltet von Kunden. Wenn eine Datei hochgeladen wird, Verschlüsselung von SharePoint Online im Kontext der Anforderung Upload erfolgt vor dem Azure-Speicher an. Beim Herunterladen einer Datei, ruft SharePoint Online verschlüsselten Kunden Daten aus der Azure-Speicher basierend auf der einzigartige Dokument-ID und die Kundendaten entschlüsselt, bevor sie an den Benutzer gesendet. Azure-Speicher hat keine Möglichkeit zur Entschlüsselung, oder sogar identifizieren und verstehen, die Kundendaten. Alle Ver- und Entschlüsselung vorkommen, in den gleichen Systemen, die mandantenisolation erzwingen die Azure Active Directory und SharePoint Online sind.

Mehrere Arbeitslasten in Office 365 speichern Daten in SharePoint Online, einschließlich Microsoft-Teams, die speichert alle Dateien in SharePoint Online und OneDrive für Unternehmen, die SharePoint Online für einen Speicher verwendet. Alle Kundendaten in SharePoint Online gespeicherte (mit mindestens 256 Bit AES-Schlüssel) verschlüsselt und in dem Rechenzentrum wie folgt verteilt. (Jeder Schritt dieses Prozesses Verschlüsselung ist FIPS 140-2 Ebene 2 überprüft. Weitere Informationen zur Kompatibilität mit FIPS 140-2 finden Sie unter [FIPS 140-2-Konformität](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)
- Jede Datei wird in einen oder mehrere Blöcke, je nach Größe der Datei verteilt. Jeder Block wird mit einem eigenen eindeutigen AES 256-Bit-Schlüssel verschlüsselt.
- Wenn eine Datei aktualisiert wird, wird das Update auf die gleiche Weise behandelt: ist die Änderung in einen oder mehrere Abschnitte unterteilt, und jeder Block mit einem separaten eindeutigen Schlüssel verschlüsselt ist.
- Diese Abschnitte – Dateien, Dateien und Update Deltas – werden als Blobs in Azure-Speicher gespeichert, die über mehrere Konten der Azure-Speicher nach dem Zufallsprinzip verteilt werden. 
- Ist der Verschlüsselungsschlüssel für diese Abschnitte des Kundendaten selbst verschlüsselt.
   - Der Schlüssel zum Verschlüsseln der Blobs werden in SharePoint Online-Inhaltsdatenbank gespeichert.
   - Die Inhaltsdatenbank ist durch Zugreifen auf Steuerelemente von Datenbank und Verschlüsselung im Ruhezustand geschützt. Verschlüsselung wird mithilfe von [Transparenten datenverschlüsselung](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) in [Azure SQL-Datenbank](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview)ausgeführt. (Azure SQL-Datenbank ist eine allgemeine relationalen Datenbank-Dienst in Microsoft Azure, die wie relationale Daten, räumliche, JSON und XML-Strukturen unterstützt.) Diese Secrets sind auf Dienstebene für SharePoint Online, nicht auf der Ebene des Mandanten. Dieser geheimen Schlüssel (auch als die Hauptschlüssel bezeichnet) werden in einem separaten sicheren Repository bezeichnet den Schlüssel Store gespeichert. TDE bietet Sicherheit im Ruhezustand für die aktive Datenbank und die datenbanksicherungen und Transaktionsprotokolle. 
   - Wenn Kunden den optionalen Schlüssel angeben müssen, der Customer-Schlüssel wird in Azure Schlüssel Vault gespeichert, und der Dienst verwendet den Schlüssel zum Verschlüsseln von eines Mandanten-Schlüssels, die verwendet wird, zum Verschlüsseln von eines Website-Schlüssels, der dann zum Verschlüsseln der Datei Schlüssel Ebene verwendet wird. Eine neue Hierarchie ist im Wesentlichen eingeführt, wenn der Kunde einen Schlüssel enthält.
- Die Zuordnung verwendet, um die Datei erneut zusammensetzen wird in der Inhaltsdatenbank zusammen mit der verschlüsselte Schlüssel, getrennt von den Hauptschlüssel entschlüsselt musste gespeichert.
- Jedes Azure-Speicher-Konto verfügt über eine eigene eindeutigen Anmeldeinformationen pro Zugriffstyp (Lesen, schreiben, auflisten und löschen). Jeder Satz von Anmeldeinformationen wird in der secure Store-Taste und regelmäßig aktualisiert wird. Wie oben beschrieben, gibt es drei verschiedene Typen von Speicher, jeweils mit einer distinct-Funktion:
- Kundendaten werden als verschlüsselte Blobs in Azure-Speicher gespeichert. Der Schlüssel zu jeder Ausschnitt von Kundendaten verschlüsselt und in der Inhaltsdatenbank getrennt gespeichert werden. Die Kundendaten selbst enthält keinen Hinweis darauf, wie sie entschlüsselt werden kann.
- Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Sie enthält die Zuordnung zum Suchen und Zusammenstellen der Kunde Datenblobs frei, die in Azure-Speicher sowie die Schlüssel zum Verschlüsseln von diesen Blobs benötigt erforderlich sind. Jedoch ist der Satz von Schlüsseln selbst (wie oben beschrieben) verschlüsselt und in einem separaten Schlüssel Speicher gehalten.
- Der Schlüssel Speicher ist physisch getrennte aus der Inhaltsdatenbank und Azure-Speicher. Er enthält die Anmeldeinformationen für jeden Container Azure-Speicher und des Hauptschlüssels für das Festlegen der verschlüsselten Schlüssel in der Inhaltsdatenbank gespeichert.

Diese drei Speicherkomponenten – Azure BLOB-Speichers, der Inhaltsdatenbank und der Schlüssel Store – ist physisch getrennte. Die Informationen in einem der Komponenten jedoch kann nicht auf einem eigenen verwendet werden. Ohne Zugriff auf alle drei ist es nicht möglich, die Tasten, um die Blöcke abgerufen werden, die Schlüssel verwendbar machen, ordnen Sie die entsprechenden Abschnitte der Schlüssel, jede Chunk entschlüsseln oder Wiederherstellen eines Dokuments aus der zugrunde liegenden Abschnitte zu entschlüsseln.

BitLocker-Zertifikate, die die physische Datenträger auf Computern im Rechenzentrum zu schützen, werden in einem sicheren Repository (die SharePoint Online geheimen Store) gespeichert, die durch den Schlüssel Farm geschützt sind.

Die TDE-Schlüssel, die die pro-BLOB-Schlüssel schützen werden an zwei Orten gespeichert:
- Sichere Repository beinhaltet die BitLocker-Zertifikate und von der Farm Schlüssel geschützt ist; und
- In einem sicheren Repository verwaltet von Azure SQL-Datenbank.

Die Anmeldeinformationen verwendet, um Zugriff auf die Container Azure-Speicher werden auch in SharePoint Online geheimen Schlüssel speichern, und jeder SharePoint Online Farm nach Bedarf delegiert aufrechterhalten. Diese Anmeldeinformationen sind Azure-Speicher SAS-Signaturen, mit eigenen Anmeldeinformationen zum Lesen oder Schreiben von Daten verwendet und Richtlinie angewendet, sodass sie automatisch alle 60 Tage entfernt. Andere Anmeldeinformationen werden verwendet, um das Lesen oder Schreiben von Daten (jedoch nicht beide) und SharePoint Online-Farmen keine Berechtigungen zum Aufzählen zugewiesen.

> US-Regierung für Hinweis-für-Office-365-Kunden, Datenblobs werden in Azure US-Regierung Storage gespeichert. Darüber hinaus ist der Zugriff auf SharePoint Online Keys in Office 365 US-Regierung auf Office 365-Mitarbeiter, die speziell überwachten wurde haben beschränkt. US-Regierung Azure Mitarbeiter haben keinen Zugriff an den SharePoint Online wichtige Store, die zum Verschlüsseln von Datenblobs verwendet wird.

Weitere Informationen zur datenverschlüsselung in SharePoint Online und OneDrive für Unternehmen finden Sie unter [Data Encryption in OneDrive für Unternehmen und SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Listenelemente in SharePoint Online
Listenelemente werden kleineren Segmenten Kunden, die Daten, die Ad-hoc- oder, die erstellt werden mehr dynamisch innerhalb einer Website, wie Zeilen in einer Liste von Benutzern erstellte, einzelne Beiträge in einer SharePoint Online-Blog oder Einträge in einer SharePoint Online-Wiki-Seite vorhanden sein können. Listenelemente in der Inhaltsdatenbank (Azure SQL-Datenbank) gespeichert und geschützt mit TDE.

## <a name="encryption-of-data-in-transit"></a>Verschlüsselung von Daten während der Übertragung
In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.
- **Kommunikation mit dem Client mit dem Server** - Kommunikation zu OneDrive for Business über das Internet verwendet SSL/TLS-Verbindungen. Alle SSL-Verbindungen werden hergestellt mit 2048 Bit.
- **Verschieben von Daten zwischen Rechenzentren** - der Hauptgrund zum Verschieben von Daten zwischen Rechenzentren erfolgt Geo-Replikation für Disaster Recovery. Beispielsweise Reisen SQL Server-Transaktionsprotokolle und BLOB-Speicher Deltas entlang dieser Pipe an. Während dieser Daten bereits über ein privates Netzwerk übertragen werden, ist diese weiter mit beste Verschlüsselung geschützt.


## <a name="exchange-online"></a>Exchange Online
Exchange Online arbeitet mit BitLocker für alle Postfachdaten, und die BitLocker-Konfiguration wird im [BitLocker-Verschlüsselung](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)beschrieben. Servicelevel-Verschlüsselung verschlüsselt alle Postfachdaten auf Postfachebene. 

Neben Service-Verschlüsselung unterstützt Office 365 Customer-Schlüssel, der auf der Basis Service-Verschlüsselung erstellt wird. Kundenschlüssel ist eine Microsoft-Mitarbeiter wichtige Option für Exchange Online-Dienst-Verschlüsselung, der auch auf Microsoft Roadmap ist. Diese Methode der Verschlüsselung bietet erhöhten Schutz nicht von BitLocker da Softwareentwicklern Trennung von Serveradministratoren und die kryptografischen Schlüssel für die Entschlüsselung der Daten erforderlich, und die Verschlüsselung direkt auf die Daten (in angewendet wird Kontrast mit BitLocker, die Verschlüsselung auf dem logischer Datenträger gilt) Kundendaten von einem Exchange-Server kopiert bleibt verschlüsselt.

Der Bereich für die Verschlüsselung von Exchange Online-Dienst ist Kundendaten, die im Ruhezustand in Exchange Online gespeichert sind. (Skype für Business fast alle benutzergenerierte Inhalte in Exchange Online-Postfach des Benutzers speichert und daher erbt das Feature von Exchange Online-Verschlüsselung).

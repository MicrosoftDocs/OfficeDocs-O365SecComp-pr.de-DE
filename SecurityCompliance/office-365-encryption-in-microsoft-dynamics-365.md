---
title: Office 365-Verschlüsselung in Microsoft Dynamics 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 5/31/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Grundlegendes zu Verschlüsselung in Microsoft Dynamics 365.'
ms.openlocfilehash: 181db1724f140c86fb1ac1dbf4a4bfb7063d25a3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528851"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Office 365-Verschlüsselung in Microsoft Dynamics 365

Microsoft verwendet die Verschlüsselung zum Schutz von Kundendaten in Dynamics 365 bei Rest in einer Microsoft-Datenbank, und zwar während der Übertragung zwischen Benutzer Geräten und unsere Rechenzentren. Verbindungen zwischen Kunden und Microsoft-Rechenzentren verschlüsselt werden, und alle öffentlichen Endpunkte sind mit Industriestandard TLS geschützt. TLS wird effektiv eine erhöhter Sicherheit Browser-zu-Server-Verbindung zum Datenschutz und Integrität zwischen Desktops und Rechenzentren sicherzustellen. Nachdem-Verschlüsselung aktiviert ist, kann es deaktiviert werden. Weitere Informationen finden Sie unter [datenverschlüsselung Feldebene](https://msdn.microsoft.com/en-us/library/dn481562.aspx).

Dynamics 365 verwendet standard Microsoft SQL Server Zelle Verschlüsselung für einen Satz mit Attributen der Standard-Entität, die vertraulichen Informationen wie Benutzernamen und Kennwörter e-Mail enthalten. Dieses Feature können Organisationen die Auflagen FIPS 140-2 zugeordnet. Datenverschlüsselung Feldebene ist besonders wichtig in Szenarien, in denen der [Microsoft Dynamics CRM-e-Mail-Router](https://technet.microsoft.com/en-us/library/hh699800.aspx)einsetzen, mit dem Benutzernamen und Kennwörter zum Aktivieren der Integration zwischen einer Dynamics 365-Instanz und eine e-Mail-Dienst speichern müssen. 

Alle Instanzen von Dynamics 365 verwenden [Microsoft SQL Server transparente datenverschlüsselung](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE) in Echtzeit Verschlüsselung von Daten beim Schreiben auf Datenträger (im Ruhezustand) ausführen. TDE verschlüsselt SQL Server, Azure SQL-Datenbank und Azure SQL Data Warehouse-Datendateien. In der Standardeinstellung Microsoft speichert und die Datenbankverschlüsselungsschlüssel für Instanzen von Dynamics 365 verwaltet. (Schlüssel, die von Dynamics 365 für Finanzen verwendet werden, werden von der .NET Framework Data Protection-API generiert.) 

Das Feature zum Verwalten Schlüssel in der Dynamics 365-Verwaltungskonsole bietet Administratoren die Möglichkeit, die Datenbankverschlüsselungsschlüssel verwalten selbst, die Instanzen von Dynamics 365 zugeordnet sind. (Self verwaltete Datenbankverschlüsselungsschlüssel stehen nur im Januar 2017 Update für Microsoft Dynamics 365 und möglicherweise nicht zur Verfügung gestellt für höhere Versionen. Weitere Informationen finden Sie unter [Verwalten der Verschlüsselungsschlüssel für die Dynamics 365 (online)-Instanz](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance).) Die wichtigsten Verwaltungsfeature unterstützt PFX- und BYOK Verschlüsselung wichtige Dateien, beispielsweise in einer HSM gespeichert wurden. (Weitere Informationen zu generieren und übertragen einen Schlüssel HSM geschützt über das Internet, finden Sie unter [wie generiert und HSM-geschützten Schlüssel für Azure Schlüssel Vault übertragen](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys).) 

Um die Option hochladen Verschlüsselung Schlüssel verwenden zu können, benötigen Sie den öffentlichen und privaten Verschlüsselungsschlüssel.

Die wichtigsten Management-Funktion nimmt vereinfachen Sie das Management von Verschlüsselungsschlüsseln mithilfe von Azure Schlüssel Vault Verschlüsselungsschlüssel sicher speichern. Azure-Taste Vault hilft optimaler kryptografische Schlüssel und geheime von Cloudanwendungen und Dienste verwendet werden. Die wichtigsten Management-Funktion erforderlich nicht, dass ein Abonnement Azure Schlüssel Vault und in den meisten Fällen besteht keine Notwendigkeit für den Verschlüsselungsschlüssel Dynamics 365 innerhalb der Vault zum Zugriff auf.

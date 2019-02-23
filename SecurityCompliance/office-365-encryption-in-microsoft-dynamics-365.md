---
title: Office 365-Verschlüsselung in Microsoft Dynamics 365
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: grundLegendes zur Verschlüsselung in Microsoft Dynamics 365.'
ms.openlocfilehash: 7c2a352dd712b0db9d2ad623745f854b863dd2e0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219315"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Office 365-Verschlüsselung in Microsoft Dynamics 365

Microsoft verwendet Verschlüsselungstechnologie, um Kundendaten in Dynamics 365 zu schützen, während Sie sich in einer Microsoft-Datenbank befinden und während Sie zwischen Benutzergeräten und unseren Rechenzentren übertragen wird. Verbindungen zwischen Kunden und Microsoft-Datencentern werden verschlüsselt, und alle öffentlichen Endpunkte werden mit Industriestandard-TLS gesichert. TLS stellt effektiv eine Browser-zu-Server-Verbindung mit Sicherheitsinformationen her, um Datenvertraulichkeit und Integrität zwischen Desktops und Rechenzentren sicherzustellen. Nachdem die Datenverschlüsselung aktiviert wurde, kann Sie nicht deaktiviert werden. Weitere Informationen finden Sie unter [Datenverschlüsselung](https://msdn.microsoft.com/en-us/library/dn481562.aspx)auf Feldebene.

Dynamics 365 verwendet standardmäßige Microsoft SQL Server-Verschlüsselung auf Zellenebene für einen Satz von Standard entitätsattributen, die vertrauliche Informationen wie Benutzernamen und e-Mail-Kennwörter enthalten. Mit dieser Funktion können Organisationen die mit FIPS 140-2 verbundenen Compliance-Anforderungen erfüllen. Die Datenverschlüsselung auf Feldebene ist insbesondere in Szenarien wichtig, die den [Microsoft Dynamics CRM-e-Mail-Router](https://technet.microsoft.com/en-us/library/hh699800.aspx)nutzen, der Benutzernamen und Kennwörter speichern muss, um die Integration zwischen einer Dynamics 365-Instanz und einem e-Mail-Dienst zu ermöglichen. 

Alle Instanzen von Dynamics 365 verwenden [Microsoft SQL Server transparent Data Encryption](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (DSA), um Daten in Echtzeit zu verschlüsseln, wenn Sie auf den Datenträger geschrieben werden (im Rest). DSA verschlüsselt SQL Server-, Azure SQL-Datenbank-und Azure SQL Data Warehouse-Datendateien. Standardmäßig speichert und verwaltet Microsoft die Verschlüsselungsschlüssel für Ihre Instanzen von Dynamics 365. (Die von Dynamics 365 für Financials verwendeten Schlüssel werden von der .NET Framework-Datenschutz-API generiert.) 

Mit der Funktion "Schlüssel verwalten" im Dynamics 365 Administration Center können Administratoren die Verschlüsselungsschlüssel der Datenbank, die mit Instanzen von Dynamics 365 verknüpft sind, selbst verwalten. (Self-Managed-Datenbankverschlüsselungsschlüssel sind nur im Januar 2017-Update für Microsoft Dynamics 365 verfügbar und sind möglicherweise nicht für spätere Versionen verfügbar. Weitere Informationen finden Sie unter [Verwalten der Verschlüsselungsschlüssel für Ihre Dynamics 365 (Online)-Instanz](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance).) Das Schlüssel Verwaltungsfeature unterstützt sowohl PFX-als auch BYOK-Verschlüsselungsschlüssel Dateien, wie in einem HSM gespeicherte. (Weitere Informationen zum Generieren und übertragen eines HSM-geschützten Schlüssels über das Internet finden Sie unter vorGehens [Weise: generieren und übertragen von HSM-geschützten Schlüsseln für Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys).) 

Um die Option Verschlüsselungsschlüssel hochladen zu verwenden, benötigen Sie sowohl den öffentlichen als auch den privaten Verschlüsselungsschlüssel.

Die Schlüssel Verwaltungsfunktion nutzt die Komplexität der Verschlüsselungsschlüsselverwaltung mithilfe von Azure Key Vault, um Verschlüsselungsschlüssel sicher zu speichern. Azure Key Vault hilft bei der Sicherung von kryptografischen Schlüsseln und Geheimnissen, die von Cloud-Anwendungen und-Diensten verwendet werden. Für die Schlüssel Verwaltungsfunktion ist kein Azure Key Vault-Abonnement erforderlich, und in den meisten Fällen ist es nicht erforderlich, auf Verschlüsselungsschlüssel zuzugreifen, die für Dynamics 365 innerhalb des Tresors verwendet werden.

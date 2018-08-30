---
title: Verschlüsselung für Office 365-Dienst
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
description: 'Zusammenfassung: Grundlegendes zu datenflexibilität in Microsoft Office 365.'
ms.openlocfilehash: 1273cd5556bf51dcdac9bbde1b3e8003ab818811
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529454"
---
# <a name="office-365-service-encryption"></a>Verschlüsselung für Office 365-Dienst

Verwenden Sie zusätzlich zur Verwendung von Lautstärkepegel Verschlüsselung, Exchange Online Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen auch Service Verschlüsselung zum Verschlüsseln von Kundendaten. Service-Verschlüsselung ermöglicht zwei Schlüsselverwaltungsdienst-Optionen:
- Microsoft verwaltet alle kryptografischen Schlüssel. (Diese Option ist derzeit in SharePoint Online, OneDrive für Unternehmen und Skype für Unternehmen. Es ist derzeit auf der Roadmap für Exchange Online.)
- Der Kunde stellt Stammschlüssel bei der Verschlüsselung Service verwendet, und der Kunde hierüber von Azure Schlüssel Vault verwaltet. Microsoft verwaltet alle anderen Schlüssel. Diese Option wird als Customer-Schlüssel bezeichnet, und es ist derzeit für Exchange Online, SharePoint Online und OneDrive für Unternehmen. (Zuvor als erweiterte Verschlüsselung mit BYOK bezeichnet. Siehe [Verbesserung Transparenz und Kontrolle für Office 365-Kunden](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) für die ursprüngliche Ankündigung.)

Verschlüsselung Service bietet mehrere Vorteile. Es beispielsweise:
- bietet Rechte Features zum Schutz und Verwaltung auf der Basis starke Verschlüsselung Schutz.
- enthält eine Customer Schlüssel-Option, die mit mehreren Mandanten Services pro Mandant Key Management bereitstellen kann.
- Trennung der Windows-Betriebssystem-Administratoren von Zugriff auf Kundendaten gespeichert oder vom Betriebssystem verarbeitet enthält.
- verbessert die Fähigkeit von Office 365, die Notwendigkeit, Kunden zu erfüllen, die Compliance-Bestimmungen Verschlüsselung haben.

## <a name="customer-key"></a>Kundenschlüssel
Kunden-Schlüssel können Sie eigene mithilfe einer lokalen HSM oder Azure Schlüssel Vault kryptografische Schlüssel generieren. Unabhängig davon, wie der Schlüssel generiert wird verwenden Sie Kunden Azure Schlüssel Vault zu steuern und Verwalten von Office 365 verwendeten die kryptografischen Schlüsseln. Nachdem die Schlüssel in Azure Schlüssel Vault gespeichert sind, können sie Arbeitslasten wie Exchange Online und SharePoint Online zugewiesen und verwendet, um als Stamm der Schlüsselsammlung zum Verschlüsseln von Postfächern und Dateien verwendet. Einer der Vorteile der Verwendung von Kundenschlüssel ist die Fähigkeit von Microsoft auf Kundendaten Prozess gesteuert. Diese Funktion vorhanden ist, damit Kunden, der Daten aus der Office 365 (beispielsweise, wenn ein Kunde beendet Dienst mit Microsoft oder entfernt einen Teil der Daten in der Cloud gespeichert) entfernen möchte dazu und Kundenschlüssel als technische Steuerelement verwenden, um sicherzustellen, dass niemand können , einschließlich Microsoft, zugreifen oder die Daten verarbeiten können. Dies ist hinzufügen (und eine Ergänzung) des Kunden Lockbox-Features, die zur Steuerung des Zugriffs auf Kundendaten von Microsoft-Mitarbeitern verwendet werden können.

Kunden-Schlüssel für Office 365 für Exchange Online einrichten Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen, finden Sie unter [Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). Weitere Informationen finden Sie unter [Customer Product Key für die Office 365 – häufig gestellte Fragen](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)und [Verwalten und Steuerelement müssen Ihre Daten zur Einhaltung der Kompatibilität mit Kundenschlüssel](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).

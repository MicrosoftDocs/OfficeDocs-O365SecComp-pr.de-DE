---
title: Office 365-Dienstverschlüsselung
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
description: 'Zusammenfassung: grundLegendes zur Datensicherheit in Microsoft Office 365.'
ms.openlocfilehash: 4e9dd52adbeada92d14db369b386ff1ca7e42fc5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220345"
---
# <a name="office-365-service-encryption"></a>Office 365-Dienstverschlüsselung

Zusätzlich zur Verschlüsselung auf Volumeebene verwenden Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business auch Dienst Verschlüsselung, um Kundendaten zu verschlüsseln. Die Dienst Verschlüsselung ermöglicht zwei wichtige Verwaltungsoptionen:
- Microsoft verwaltet alle kryptografischen Schlüssel. (Diese Option ist derzeit in SharePoint Online, OneDrive for Business und Skype for Business verfügbar. Sie befindet sich derzeit in der Roadmap für Exchange Online.)
- Der Kunde liefert Stammschlüssel, die mit der Dienst Verschlüsselung verwendet werden, und der Kunde verwaltet diese Schlüssel mithilfe von Azure Key Vault. Microsoft verwaltet alle anderen Schlüssel. Diese Option wird als Kundenschlüssel bezeichnet und ist derzeit für Exchange Online, SharePoint Online und OneDrive for Business verfügbar. (Zuvor als erweiterte Verschlüsselung mit BYOK bezeichnet. Weitere Informationen finden Sie unter [Enhancing transparency and Control for Office 365 Customers](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) for the Original Announcement.)

Die Dienst Verschlüsselung bietet mehrere Vorteile. Beispielsweise:
- bietet Rechte Schutz-und Verwaltungsfunktionen auf der Grundlage eines starken Verschlüsselungs Schutzes.
- enthält eine Kundenschlüssel Option, mit der mehrere Mandanten Dienste eine Schlüsselverwaltung per Mandanten bereitstellen können.
- ermöglicht die Trennung von Windows-Betriebssystem Administratoren vom Zugriff auf vom Betriebssystem gespeicherte oder verarbeitete Kundendaten.
- verbessert die Fähigkeit von Office 365, die Anforderungen von Kunden zu erfüllen, die über Compliance-Anforderungen hinsichtlich der Verschlüsselung verfügen.

## <a name="customer-key"></a>Kundenschlüssel
Mit dem Kundenschlüssel können Sie eigene kryptografische Schlüssel mithilfe eines lokalen HSM oder eines Azure Key Vault generieren. Unabhängig davon, wie der Schlüssel generiert wird, verwenden Kunden Azure Key Vault, um die von Office 365 verwendeten kryptografischen Schlüssel zu steuern und zu verwalten. Nachdem Sie Ihre Schlüssel in Azure Key Vault gespeichert haben, können Sie Arbeitsauslastungen wie Exchange Online und SharePoint Online zugewiesen werden und als Stamm des Schlüsselbunds verwendet werden, der zum Verschlüsseln ihrer Postfachdaten und-Dateien verwendet wird. Einer der anderen Vorteile der Verwendung von Kundenschlüssel besteht darin, die Fähigkeit von Microsoft zu steuern, Kundendaten zu verarbeiten. Diese Funktion ist vorhanden, sodass ein Kunde, der Daten aus Office 365 entfernen möchte (beispielsweise wenn ein Kunde den Dienst mit Microsoft beendet oder einen Teil der in der Cloud gespeicherten Daten entfernt), dies tun kann, und den Kundenschlüssel als technische Steuerung verwenden, um sicherzustellen, dass niemand , einschließlich Microsoft, kann auf die Daten zugreifen oder diese verarbeiten. Dies ist zusätzlich (und eine Ergänzung) zur Kunden-Lockbox-Funktion, die verwendet werden kann, um den Zugriff auf Kundendaten durch Microsoft-Mitarbeiter zu steuern.

Informationen zum Einrichten des Kunden Schlüssels für Office 365 für Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business finden Sie unter [Steuern ihrer Daten in office 365 mit Kundenschlüssel](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). Weitere Informationen finden Sie in den häufig gestellten [Fragen zum Kundenschlüssel für Office 365](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)sowie zum [Verwalten und Steuern ihrer Daten zur Erfüllung der Compliance-Anforderungen mit dem Kundenschlüssel](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).

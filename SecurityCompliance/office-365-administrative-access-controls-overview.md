---
title: Administrative zugreifen auf Steuerelemente in Office 365
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
description: 'Zusammenfassung: Eine Übersicht über Office 365 der Administrative Zugriff Steuerelemente und Daten Kategorisierung.'
ms.openlocfilehash: afa15d37aa8542985c59dbd9e3d82368421530e8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529458"
---
# <a name="administrative-access-controls-in-office-365"></a>Administrative zugreifen auf Steuerelemente in Office 365 

## <a name="introduction"></a>Einführung
Microsoft hat stark und entsprechend in Systeme und Steuerelemente, die meisten Office 365-Vorgänge automatisieren und absichtlich Microsofts Zugriff auf Inhalte für Kunden begrenzen Sie gleichzeitig investiert. Menschen Steuern des Diensts, und Software ausgeführt wird, den Dienst. Auf diese Weise können die Microsoft Office 365 in der Skalierung verwalten sowie das Verwalten der Risiken von internen Bedrohungen für Kunden Inhalte wie böswilligen Akteure der Spear-Phishing eines Microsoft Engineer und So weiter.

Standardmäßig haben Microsoft Ingenieure NULL stehende über Administratorrechte und NULL stehende Zugriff auf Inhalte für Kunden in Office 365. Ein Microsoft-Supportmitarbeiter kann beschränkt, überwacht und Zugriff auf ein Kunde Inhalt für eine begrenzte Zeitspanne, aber nur bei Bedarf für Vorgänge des Diensts, und wenn genehmigt durch ein Mitglied der Microsoft senior Management (und für Kunden, die gesichert haben lizenziert für das Feature Kunden Lockbox, der Kunde).

Microsoft bietet online-Dienste, einschließlich Office 365, mithilfe von mehreren Formularen Cloud Übertragungsmedium:

- **Öffentliche Wolken** - enthält mit mehreren Mandanten Versionen von Office 365, Azure und andere Dienste, die in Nordamerika, Südamerika, Europa, Asien, Australien usw. gehostet werden.
- **National Wolken** - umfasst alle unabhängigen und Drittanbieter-betrieben Wolken außerhalb der USA (außer den oben aufgeführten), wie Office 365 in China (das von 21Vianet betrieben wird) und Office 365 in Deutschland (die von Microsoft betrieben wird jedoch Klicken Sie unter ein Modell, in dem eine deutsche Daten vertrauensnehmerdomäne, Deutsche Telekom, steuert und überwacht Microsofts Zugriff auf Kundendaten und Systeme, die Kundendaten enthalten).
- **US-Regierung Wolken** - enthält Office 365 und Azure-Dienste, die US-Regierungskunden zur Verfügung stehen.

Aus Gründen der in diesem Artikel sind Office 365-Dienste [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (einschließlich [OneDrive für Unternehmen](https://docs.microsoft.com/OneDrive/onedrive)) und [Skype für Unternehmen](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online), mit zusätzlichen Informationen Informationen zu einigen [Yammer Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) zugreifen auf Steuerelemente. Andere Office 365-Dienste sind Gegenstand dieses Artikels.

## <a name="office-365-access-controls"></a>Zugreifen auf Steuerelemente von Office 365
Steuerzwecken Access ist Office 365-Daten als Kundendaten oder andere Datentypen kategorisiert. Kundendaten wird alle Daten, die durch oder im Auftrag eines Kunden durch die Verwendung von Office 365-Dienste, wie Inhalte für Kunden (Inhalte direkt erstellt oder hochgeladen Office 365-Benutzer-e-Mails SharePoint Online Content, einschließlich Sofortnachrichten, die Kunden bereitgestellt Kalender-Elemente, Dokumente und Kontakte in Office 365 gespeichert) und Endbenutzer identifizierbare Informationen (EUII) (Daten, die für einen Benutzer eindeutig ist oder, die für einen einzelnen Benutzer verknüpfbares ist enthält jedoch keine Inhalte für Kunden). 

Andere Typen von Daten enthalten (einschließlich der administrative Daten, also die Informationen, die von Administratoren bereitgestellt, wenn sie Anmeldung oder Dienste erwerben und Zahlungsdaten, d. h. Informationen zu Zahlungsinstrumente, wie etwa einer Karte Details) Kontodaten, Organisation identifizierbare Informationen (Daten, die verwendet werden können, um einen Mandanten; zu identifizieren oder Nutzungsdaten; es ist nicht für einen einzelnen Benutzer verknüpfbares und enthält keine Inhalte für Kunden), und Systemmetadaten (einschließlich der Service-Protokolle, die Einstellungen für die Websitekonfiguration enthalten Systemstatus, Microsoft IP-Adressen und technische Informationen zu Abonnements und Mandanten).

Microsoft Access-Steuerelement Mechanismen, um sicherzustellen, dass kein anderer hat eingerichtet hat nicht genehmigte Zugriff auf Kundendaten oder Access Control-Daten (zum Verwalten des Zugriffs auf andere Typen von Daten oder Funktionen innerhalb der Umgebung, einschließlich des Zugriffs auf Kunden Inhalts- oder EUII; es enthält Microsoft Kennwörter, Zertifikate und andere Daten im Zusammenhang mit Authentifizierung) oder nicht genehmigte physische, logische oder remote-Zugriff auf die Office 365-produktionsumgebung.

Das Zugreifen auf Steuerelemente von Microsoft für den Betrieb von Office 365 verwendet können in drei Kategorien unterteilt werden:
- Isolation-Steuerelemente
- Personal-Steuerelemente
- Technologie-Steuerelemente

Zusammen können diese Steuerelemente verhindern und erkennen schädlicher Aktionen in Office 365. Zusätzlich zu den Isolation, Personal und Technologie-Steuerelemente, die von Microsoft verwendet, es ist eine vierte Kategorie von Steuerelementen: die vom Kunden implementiert.

Office 365 können Sie Ihre Daten zu verwalten, die einen Großteil der gleichen Weise Daten in lokalen Umgebungen verwaltet wird. Die Person, die von einer Organisation für Office 365 automatisch signiert wird ein globaler Administrator (Admin). Der globale Administrator kann hat Zugriff auf alle Funktionen in der Verwaltung von Portalen (z. B. Admin Center und remote-PowerShell), und erstellen oder Benutzer bearbeiten, Zuweisen von Administratorrollen an andere Personen, Zurücksetzen von Benutzerkennwörtern, Verwalten von Benutzerlizenzen, Verwalten von Domänen und Kunden Lockbox genehmigen Anforderungen, unter anderem. Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten festzulegen und je nach Größe Ihrer Organisation, Sie sollten mehrere Administratoren festlegt, die verschiedene Funktionen dienen. Informationen zum Zuweisen von administrativen Rollen und Berechtigungen finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) und [Informationen zu Office 365-Administratorrollen](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Verwandte Links

- [Isolation-Steuerelemente](office-365-isolation-controls.md)
- [Personal-Steuerelemente](office-365-personnel-controls.md)
- [Technologie-Steuerelemente](office-365-technology-controls.md)
- [Überwachung und Prüfung zugreifen auf Steuerelemente](office-365-monitoring-and-auditing-access-controls.md)
- [Zugreifen auf Steuerelemente von Yammer Enterprise](office-365-yammer-enterprise-access-controls.md)
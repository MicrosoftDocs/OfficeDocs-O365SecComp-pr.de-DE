---
title: Administrative Zugriffssteuerungen in Office 365
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine Übersicht über administrative Zugriffssteuerungen und Datenkategorisierung von Office 365.'
ms.openlocfilehash: f5cac8b6161ea7eab6ea390e32caec1c5ddb9bac
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091026"
---
# <a name="administrative-access-controls-in-office-365"></a>Administrative Zugriffssteuerungen in Office 365 

## <a name="introduction"></a>Einführung
Microsoft hat stark und dementsprechend in Systeme und Steuerelemente investiert, die die meisten Office 365-Vorgänge automatisieren und den Zugriff von Microsoft auf Kunden Inhalte absichtlich einschränken. Der Dienst wird vom Menschen beherrscht, und die Software betreibt den Dienst. Dadurch kann Microsoft Office 365 im Maßstab verwalten und die Risiken interner Bedrohungen für Kunden Inhalte wie böswillige Akteure, den Speer-Phishing eines Microsoft-Ingenieurs usw. verwalten.

Standardmäßig verfügen Microsoft-Ingenieure über keine ständigen Verwaltungsrechte und keinen Zugriff auf Kunden Inhalte in Office 365. Ein Microsoft-Techniker kann begrenzten, überwachten und gesicherten Zugriff auf die Inhalte eines Kunden für einen begrenzten Zeitraum haben, jedoch nur, wenn dies für Dienstvorgänge erforderlich ist, und nur dann, wenn er von einem Mitglied von Microsoft Senior Management (und für Kunden, die für die Kunden-Lockbox-Funktion, den Kunden, lizenziert.

Microsoft bietet Onlinedienste, einschließlich Office 365, mit mehreren Formen der Cloud-Bereitstellung:

- **Öffentliche Clouds** – umfasst Mandantenübergreifende Versionen von Office 365, Azure und anderen Diensten, die in Nordamerika, Südamerika, Europa, Asien, Australien usw. gehostet werden.
- **National Clouds** -umfasst alle souveränen und Drittanbieter betriebenen Wolken außerhalb der USA (mit Ausnahme der oben genannten), wie Office 365 in China (die von 21Vianet betrieben wird) und Office 365 in Deutschland (das von Microsoft betrieben wird, aber unter einem Modell, in dem ein deutscher Daten Treuhänder, die Deutsche Telekom, den Zugriff von Microsoft auf Kundendaten und-Systeme, die Kundendaten enthalten, steuert und überwacht.
- **Government Clouds** -umfasst Office 365-und Azure-Dienste, die US-Regierungskunden zur Verfügung stehen.

In diesem Artikel umfassen Office 365-Dienste [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (einschließlich [OneDrive for Business](https://docs.microsoft.com/OneDrive/onedrive)) und [Skype for Business](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)mit zusätzlichen Informationen über einige [jammern Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) -Zugriffssteuerungen. Andere Office 365-Dienste liegen außerhalb dieses Artikels.

## <a name="office-365-access-controls"></a>Office 365-Zugriffssteuerung
Für Zugriffs Steuerungszwecke werden Office 365-Daten als Kundendaten oder andere Datentypen kategorisiert. Kundendaten sind alle Daten, die von oder im Auftrag eines Kunden über die Nutzung von Office 365-Diensten durch den Kunden bereitgestellt werden (beispielsweise Kunden Inhalte (direkt von Office 365-Benutzer erstellte oder Hochgeladene Inhalte, einschließlich e-Mails, SharePoint Online-Inhalte, Instant Messages, Kalenderelemente, Dokumente und Kontakte, die in Office 365 gespeichert sind) und Endbenutzer-identifizierbare Informationen (EUII) (Daten, die für einen Benutzer eindeutig sind oder die mit einem einzelnen Benutzer verknüpft sind, jedoch keinen Kunden Inhalt aufweisen). 

Zu anderen Datentypen gehören Kontodaten (einschließlich administrativer Daten, die von Administratoren bei der Registrierung oder beim Kauf von Diensten bereitgestellt werden, sowie Zahlungsdaten, die Informationen zu Zahlungsinstrumenten wie Kreditkartendetails darstellen). organisatorisch identifizierbare Informationen (Daten, die verwendet werden können, um einen Mandanten zu identifizieren, oder Verwendungsdaten, er ist nicht mit einem einzelnen Benutzer verknüpft und enthält keine Kunden Inhalte) und Systemmetadaten (einschließlich Service Protokollen, die Konfigurationseinstellungen enthalten, Systemstatus, Microsoft-IP-Adressen und technische Informationen zu Abonnements und Mandanten).

Microsoft verfügt über Zugriffssteuerungsmechanismen, mit denen sichergestellt werden kann, dass niemand ungenehmigten Zugriff auf Kundendaten oder Zugriffssteuerungsdaten hat (zur Verwaltung des Zugriffs auf andere Typen von Daten oder Funktionen innerhalb der Umgebung, einschließlich des Zugriffs auf Kunden Inhalte oder EUII). enthält Microsoft-Kennwörter, Sicherheitszertifikate und andere Authentifizierungs bezogene Daten) oder nicht genehmigte physische, logische oder Remotezugriffe auf die Office 365-Produktionsumgebung.

Die von Microsoft für den Betrieb von Office 365 verwendeten Zugriffssteuerungen können in drei Kategorien unterteilt werden:
- Isolations Steuerelemente
- Personal Steuerungen
- Technologie Steuerelemente

In Kombination helfen diese Steuerelemente, bösartige Aktionen in Office 365 zu verhindern und zu ermitteln. Zusätzlich zu den von Microsoft verwendeten Isolierungs-, Personal-und Technologie Steuerelementen gibt es eine vierte Kategorie von Steuerelementen: die von Kunden implementierten.

Mit Office 365 können Sie Ihre Daten auf die gleiche Art und Weise verwalten, wie Daten in lokalen Umgebungen verwaltet werden. Die Person, die eine Organisation für Office 365 anmeldet, wird automatisch zu einem globalen Administrator (admin). Der globale Administrator hat Zugriff auf alle Funktionen in den Verwaltungs Portalen (z. b. Admin Center und Remote-PowerShell) und kann Benutzer erstellen oder bearbeiten, anderen Administratorenrollen zuweisen, Benutzerkennwörter zurücksetzen, Benutzerlizenzen verwalten, Domänen verwalten und Kunden-Lockbox genehmigen. Anforderungen unter anderem. Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten festlegt und abhängig von der Größe Ihrer Organisation mehrere Administratoren festlegen möchten, die unterschiedliche Funktionen nutzen. Informationen zum Zuweisen von Administratorrollen und Berechtigungen finden Sie unter [Zuweisen von Administratorrollen in office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) und [zu Office 365-Administratorrollen](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Verwandte Links

- [Isolations Steuerelemente](office-365-isolation-controls.md)
- [Personal Steuerungen](office-365-personnel-controls.md)
- [Technologie Steuerelemente](office-365-technology-controls.md)
- [Überwachung und Überprüfung von Zugriffssteuerungen](office-365-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise-Zugriffssteuerungen](office-365-yammer-enterprise-access-controls.md)
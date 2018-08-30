---
title: Aufbewahrung von Daten, löschen und Vernichtung in Office 365
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
description: Eine Übersicht über Microsoft Richtlinien für Office 365 bezüglich der Aufbewahrung von Daten, löschen und Vernichtung.
ms.openlocfilehash: 4d952058df8d0efb664f23e5495796fdb9e006f2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529210"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Aufbewahrung von Daten, löschen und Vernichtung in Office 365

## <a name="introduction"></a>Einführung
Microsoft hat eine Daten behandeln von Standard-Richtlinie für Office 365, der angibt, wie lange Kundendaten beibehalten werden, nachdem Sie gelöscht. Im Allgemeinen in Office 365 gibt es zwei Szenarien, in denen Kundendaten gelöscht werden:
- **Aktive Löschung** - Benutzer löscht Daten oder Daten, die einem Benutzer private werden gelöscht, nachdem der Benutzer durch den Administrator der einem aktiven Mandanten gelöscht wird.
- **Passive Löschung** - Abonnement endet mit dem Mandanten.

Microsoft Daten behandeln von Standard-Richtlinien für Office 365 gibt an, wie lange Daten in jedem dieser Szenarien aufbewahrt werden sollen. In den folgenden Abschnitten werden die Kategorien von Daten (basierend auf der Microsoft Office 365 Asset-Klassifizierung Standard) und der beibehaltungszeiträume für den aktiven und passiven Löschung Szenarien beschrieben.

## <a name="active-deletion-retention"></a>Aktive Löschung Aufbewahrung

| Datenkategorie | Mindestens beibehalten | Bei den meisten beibehalten |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Zugriffssteuerungsdaten | Nicht zutreffend | Nicht zutreffend |
| Kunden-Inhalte | 7 Tage | 30 Tage |
| Identifizierbare Informationen zu Endbenutzern | 90 Tage | 180 Tage |
| Kontodaten | 1 Jahr | 3 Jahren |
| Organisation identifizierbare Informationen | 90 Tage | 180 Tage |
| Dateisystem-Metadaten | Siehe Sicherheitsprotokolle | Siehe Sicherheitsprotokolle |
| Sicherheitsprotokolle | Min 1 Jahr | Max 1 Jahr |
| Exchange Online-Archivierung-Protokolle | Min 3 Jahren | Max-3 Jahre |

## <a name="passive-deletion-retention"></a>Passive Löschung Aufbewahrung

| Datenkategorie | Mindestens beibehalten | Bei den meisten beibehalten |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Zugriffssteuerungsdaten | 90 Tage (für Content Wiederherstellung) | 180 Tage (für Content Wiederherstellung) |
| Kunden-Inhalte | 90 Tage (Konto Limited-Funktion) | 180 Tage |
| Identifizierbare Informationen zu Endbenutzern | 90 Tage | 180 Tage |
| Kontodaten | 1 Jahr | 3 Jahren |
| Organisation identifizierbare Informationen | 90 Tage | 180 Tage |
| Dateisystem-Metadaten | Siehe Sicherheitsprotokolle | Siehe Sicherheitsprotokolle |
| Sicherheitsprotokolle | Min 1 Jahr | Max 1 Jahr |
| Exchange Online-Archivierung-Protokolle | Min 3 Jahren | Max-3 Jahre |

## <a name="subscription-rentention"></a>Abonnement Rentention

Kunden-Inhalt wird definiert, wie Exchange Online Inhalt von Postfächern (e-Mail-Body, Kalendereinträge und den Inhalt von e-Mail-Anlagen und gegebenenfalls Skype für Geschäftsinhalten), SharePoint Online-Website-Inhalte und die Dateien in Websites und Dateien hochgeladen zu OneDrive for Business oder Skype für Unternehmen.

AT jederzeit während der Laufzeit eines Abonnements, ein-Abonnent zugreifen und Extrahieren von Kundendaten in Office 365 gespeichert. Mit Ausnahme der kostenlose Testversionen und LinkedIn-Dienste behält Microsoft Kundendaten in Office 365 für 90 Tage nach Ablauf oder Kündigung des Abonnements zum Aktivieren des Abonnenten zum Extrahieren der Daten in einem Konto Limited-Funktion gespeichert. (Im Fall von eine kostenlose Testversion, nach Ablauf die Testversion verschiebt ihn in eine Toleranzperiode besserer 30 Tage (für die meisten Versuche, in den meisten Ländern und Regionen) in Office 365 kaufen. Wenn Sie nicht Office 365 kaufen möchten, können Sie Ihre Testversion laufen lassen oder abzubrechen. Nach der 30-Tage-Nachfrist wird Ihren Testkonto Informationen und Daten dauerhaft gelöscht.)

Nach Ablauf der 90-Tage-Aufbewahrungszeitraum Microsoft deaktiviert das Konto und löscht die Kundendaten. Nicht mehr als 180 Tage nach Ablauf oder Beendigung eines Abonnements für Office 365, wird Microsoft deaktivieren Sie das Konto und alle Kundendaten über das Konto löschen. Nachdem die maximale Aufbewahrungsdauer für alle Daten abgelaufen ist, werden die Daten im Handel nicht wiederhergestellt dargestellt.

Microsoft hat auch eine Daten behandeln von Standard-Richtlinie, die das recycling und die Freigabe von Festplatten und fehlerhaften oder Abschaltung-Server-Adressen. Bevor Sie erneut verwenden keine Laufwerke in Office 365, führt Microsoft einen physischen löschen-Prozess, der mit NIST SP 800-88 kompatibel ist. Laufwerke, die wiederverwendet werden kann nicht entfernt, mit einem physischen Vernichtung Prozess, der innerhalb der Datacenter mit den Festplatten gelöscht wird vor Ort ausgeführt wird. Diese Verfahren werden von Microsoft-Cloud-Infrastruktur & Operations (MCIO) ausgeführt. Weitere Informationen finden Sie unter der MCIO Berichte auf der [Service vertrauen Preview](https://aka.ms/STP)überwachen.

## <a name="expedited-deletion"></a>Expedited löschen
AT jederzeit während der Laufzeit eines Abonnements, kann ein-Abonnent Microsoft Support und EF Anforderung Abonnement entziehen wenden. Bei diesem Vorgang alle Benutzerdaten, einschließlich der Daten in SharePoint Online, Exchange-Online, die unter möglicherweise halten oder gelöschte drei Tage nach der Administrator den Sperrung Code von Microsoft bereitgestellten gibt in inaktiver Postfächer gespeichert ist. Weitere Informationen zu expedited aufheben finden Sie unter [Office 365 abzubrechen](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Verwandte Links
- [Exchange Online-Daten löschen](/office365/enterprise/office-365-exchange-online-data-deletion)
- [SharePoint Online-Daten löschen](/office365/enterprise/office-365-sharepoint-online-data-deletion)
- [Skype für Business Daten löschen](/office365/enterprise/office-365-skype-data-deletion)
- [Unveränderbarkeit in Office 365](/office365/enterprise/office-365-data-immutability)
- [Vernichtung von Daten](/office365/enterprise/office-365-data-destruction)
---
title: Office 365 Daten Vernichtung
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
description: Eine Übersicht über Microsoft Richtlinien in Bezug auf recycling, Beseitigung oder Vernichtung Festplattenlaufwerke mit Office 365 Datacenter und Servern.
ms.openlocfilehash: c9950be4919520f2f46badaa4a7d4cfce5c55b45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529193"
---
# <a name="office-365-data-destruction"></a>Office 365 Daten Vernichtung
Microsoft hat sich Daten behandeln Standard Richtlinien, die Recycle und die Freigabe von Festplatten und fehlerhaften oder Abschaltung Server behandelt. Bevor Sie erneut verwenden keine Laufwerke in Office 365, führt Microsoft einen physischen löschen-Prozess, der mit National Institute of Standards und Technologie Special Publication 800-88 ([NIST SP-800-88-Richtlinien für Medien löschen](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) übereinstimmt ). Alle Laufwerke in Office 365 sind mit Ebene BitLocker Volumeverschlüsselung verschlüsselt damit in der Praxis NIST SP-800-88-kompatible Löschung nicht erforderlich ist. Dennoch wird weiterhin von Microsoft durchgeführt.

Fehler bei Datenträger in Office 365 Rechenzentren physisch gelöscht und durch den Prozess ISO überwacht verwendet wird. Das geeignete Mittel Beseitigung wird durch den Asset-Typ bestimmt. Microsoft verwendet für Festplatten, die Kennworteingaben gelöscht werden, ist nicht möglich, einen Vernichtung Prozess, der das Medium löscht (z. B. disintegrates, pulverizes oder incinerates) und die Wiederherstellung der Informationen unmöglich rendert. Microsoft behält auch alle Datensätze löschen. Microsoft führt einen ähnlichen löschen Prozess auf Servern, die in Office 365 wiederverwendet werden. Diese Richtlinien umfassen elektronischen und physischen löschen.

Laufwerke, die wiederverwendet werden kann nicht entfernt, mit einem physischen Vernichtung Prozess, der innerhalb der Datacenter mit den Festplatten gelöscht wird vor Ort ausgeführt wird. Für die Beseitigung festgelegte Speichermedien befinden sichere befindet sich in den einzelnen Bereichen des Datencenters Fächer. Jede sichere Bin Station wird von video-Überwachung überwacht. Nachdem eine Beseitigung Bin etwa 50 % Kapazität erreicht, kontaktiert das Websitedienste Team physische Sicherheit mit das Team seine Entfernung koordinieren. Website Servicepersonal entfernen klicken Sie dann die Beseitigung Bin unter Escort ein Security Officer, bis es in einem Speicher gesicherten Daten Vernichtung erwartet platziert wird. Richtlinien und Verfahren für die Behandlung von Daten mit der Geräte während der Freigabe werden routinemäßig getestet, einschließlich Verfahren aus, um die Bedingung der Maschinen für Vernichtung genehmigt sicherzustellen.

Beim Löschen von Daten der Datenträger wird zuerst in einer Weise, die mit NIST 800-88 (falls möglich) kompatibel ist gelöscht, und anschließend wird in einer gewerblichen Shredder platziert und physisch vermuten. Microsoft behält Accountability für Anlagen verwenden NIST SP 800-88 konsistente bereinigen/Bereinigung, Asset Vernichtung, Verschlüsselung, präzise Bestandsaufnahme, Tracking und Protection Kette Aufbewahrung während des Transports Datencenter zu verlassen. Dieser Prozess wird über geschlossen Netzfrequenz verbringt überwacht und ein Zertifikat Vernichtung abgeschlossene ausgegeben.

Microsoft setzt Daten Löschung Einheiten von [Extreme Protocol-Lösungen](http://www.enterprisedataerasure.com/) (EPS). EPS-Software unterstützt NIST SP 800-88-Anforderungen für cleansing und Löschung/secure Löschung. Vor dem bereinigen oder Vernichtung wird eine Inventur von Microsoft Asset Manager erstellt. Wenn ein Hersteller zur Vernichtung verwendet wird, bietet der Hersteller ein Zertifikat von Vernichtung für jede Anlage gelöscht, die von der Anlage-Manager überprüft wird.
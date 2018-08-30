---
title: Office 365-Mandantenisolation in Office 365-Videos
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
description: 'Zusammenfassung: Eine Erläuterung der mandantenisolation in Office 365-Videos.'
ms.openlocfilehash: 9476047d56161ec2589fdf743d7ee837ea558865
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529715"
---
# <a name="tenant-isolation-in-office-365-video"></a>Mandantenisolation in Office 365-Videos

> [!NOTE]
> Office 365-Video wird von Microsoft Stream ersetzt. Weitere Informationen zu den neuen Enterprise-video-Dienst, die video-Zusammenarbeit Intelligence hinzugefügt, und erfahren Sie mehr über die Planung für den Übergang für aktuelle Video von Office 365-Kunden finden Sie unter [Migrate in Stream-Objekt aus der Office 365-Videos](https://docs.microsoft.com/stream/).

## <a name="introduction"></a>Einführung
Azure-Speicher wird zum Speichern von Daten für mehrere Office 365-Dienste, einschließlich Office 365-Video und Schlingern verwendet. Azure-Speicher enthält BLOB-Speicher, die einen extrem skalierbar, REST-basierte, Cloud-Speicher-Objekt ist, der zum Speichern von unstrukturierte Daten verwendet wird. Azure-Speicher verwendet eine einfache Zugriffssteuerungsmodell. Jede Azure-Abonnement kann eine oder mehrere Storage-Konten erstellen. Jedes Storage-Konto hat einen einzigen geheimen Schlüssel, der zur Steuerung des Zugriffs auf alle Daten in diesem Storage-Konto verwendet wird. Dies unterstützt die Situation, in dem Speicher Applications zugeordnet ist, und diese Anwendungen verfügen über Vollzugriff auf den zugehörigen Daten. beispielsweise Sway Inhalte speichern in Azure-Speicher. Alle Kunden Inhalte für Schlingern wird im freigegebenen Speicher Azure Konten gespeichert. Inhalt des Benutzers befindet sich in einer separaten Verzeichnisstruktur von Blobs in Azure-Speicher.

Die Systeme verwalten des Zugriffs auf Kundenansprüche (z. B. der Azure-Portal, SMAPI usw.) sind in einer vom Microsoft Azure Anwendung isoliert. Dies trennt logisch Infrastruktur für den Kunden aus der Kunden und Speicherebene.

## <a name="tenant-isolation-in-office-365-video"></a>Mandantenisolation in Office 365-Videos
[Video von Office 365](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) ist ein Unternehmensportal, die Organisationen mit einer sehr sicheren, organisationsweite Ziel für bereitstellen, Freigabe und Erkennen von Videoinhalten bereitstellt. In Office 365 Video jeder Mandant Videos isoliert und verschlüsselte in allen Speicherorten und sind nur verfügbar für authentifizierte Benutzer bleiben, die Zugriff und Berechtigungen für die Organisation Videos verfügen. Office 365-Video verwendet eine Kombination von Technologien für diesen Zweck:
- SharePoint Online wird zum Speichern von der Videodatei und Metadaten (Titel des Videos, Beschreibung usw.) verwendet. Es stellt auch die Sicherheit und Compliance-Ebene (einschließlich Authentifizierung), und suchen Sie Features.
- Azure Media-Dienste bietet Umcodierung, adaptive streaming, sichere Bereitstellung (mit AES-Verschlüsselung) und Miniaturansichten Features.

[Azure-Media-Dienste](https://azure.microsoft.com/services/media-services/) ist eine Plattform-as-a-Service, der zur Aktivierung der End-to-End-Medien Workflows in der Cloud anbietet. Die Plattform bietet eine REST-API für hochladen, Codierung, verschlüsseln (mit PlayReady) und die Bereitstellung von Medien über Azure Rechenzentren auf der ganzen Welt.

Tritt auf, alle Uploads für Office 365-Video über HTTPS. Wenn eine Videodatei hochgeladen wird, ist im SharePoint Online gespeichert, und eine Kopie der Datei wird über einen verschlüsselten Kanal an Azure Media-Dienste gesendet. Azure Media-Dienste transcodiert das Video in mehrere Formate, die für die Anzeige von Erfahrung (z. B. mobile und geringer Bandbreite, hoher Bandbreite usw.) optimiert sind. Diese Dateien, die zusammen mit der ursprünglichen Datei, die beim Hochladen erworben werden in Azure BLOB-Speicher gespeichert. Die Dateien werden mit AES-128 pro MPEG allgemeine Packen Verschlüsselungsalgorithmus (oder einer früheren Version von PlayReady) für die Wiedergabe verschlüsselt und mit AES 256 Speicher Verschlüsselung vor in Azure BLOB-Speicher gespeichert wird verschlüsselt. (Mithilfe des Azure Media Services Client SDK können Kunden steuern, welche Verschlüsselung verwendet wird. Beispielsweise könnte ein Kunde Azure Media-Dienste-Speicher-Verschlüsselung (AES 256) auf hochwertige Medien anzuwenden, bevor Hochladen von Azure BLOB-Speicher.)

Azure Media-Dienste generiert auch eine Miniaturansicht des Videos, der es zusammen mit Miniaturansichten Metadaten zu SharePoint Online über einen verschlüsselten Kanal überträgt.

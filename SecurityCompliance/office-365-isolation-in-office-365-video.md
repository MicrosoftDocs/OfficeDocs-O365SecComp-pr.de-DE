---
title: Office 365-Mandanten Isolierung in Office 365 Video
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
description: 'Zusammenfassung: eine Erläuterung der Mandanten Isolierung in Office 365 Video.'
ms.openlocfilehash: e153605a0e8d938ab7bddb92e46d7d54a94f612a
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091047"
---
# <a name="tenant-isolation-in-office-365-video"></a>Mandantenisolation in Office 365 Video

> [!NOTE]
> Office 365 Video wird durch Microsoft Stream ersetzt. Weitere Informationen zum neuen Enterprise-Videodienst, der die Zusammenarbeit bei Videoinformationen und Informationen zu den Übergangsplänen für aktuelle Office 365-Video Kunden hinzufügt, finden Sie unter [migrate to Stream from office 365 Video](https://docs.microsoft.com/stream/).

## <a name="introduction"></a>Einführung
Azure Storage dient zum Speichern von Daten für mehrere Office 365-Dienste, einschließlich Office 365-Videos und Sway. Azure Storage umfasst BLOB-Speicher, ein hoch skalierbarer, REST-basierter Cloud-Objektspeicher, der zum Speichern von unstrukturierten Daten verwendet wird. Azure Storage verwendet ein einfaches Zugriffssteuerungsmodell; jedes Azure-Abonnement kann mindestens ein Speicherkonto erstellen. Jedes Speicherkonto verfügt über einen einzigen geheimen Schlüssel, der zum Steuern des Zugriffs auf alle Daten in diesem Speicherkonto verwendet wird. Dies unterstützt das typische Szenario, in dem Speicher mit Anwendungen verknüpft ist und diese Anwendungen die vollständige Kontrolle über die zugehörigen Daten haben. beispielsweise Sway Speichern von Inhalten in Azure Storage. Alle Kunden Inhalte für Sway werden in freigegebenen Azure-Speicherkonten gespeichert. Die Inhalte der einzelnen Benutzer befinden sich in einer separaten Verzeichnisstruktur von BLOBs im Azure-Speicher.

Die Systeme, die den Zugriff auf Kundenumgebungen verwalten (z. b. das Azure-Portal, SMAPI usw.), werden innerhalb einer Azure-Anwendung von Microsoft isoliert. Dadurch wird die Kundenzugriffs Infrastruktur logisch von den Kundenanwendungen und der Speicherebene getrennt.

## <a name="tenant-isolation-in-office-365-video"></a>Mandantenisolation in Office 365 Video
[Office 365 Video](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) ist ein Unternehmensportal, das Organisationen ein hochsicheres, organisationsweites Ziel für das veröffentlichen, freigeben und entdecken von Videoinhalten bietet. In Office 365 Video werden die Videos jedes Mandanten isoliert und an allen Speicherorten verschlüsselt und stehen nur authentifizierten Benutzern zur Verfügung, die über Zugriff und Berechtigungen für die Videos der Organisation verfügen. Office 365 Video verwendet eine Kombination von Technologien, um dies zu erreichen:
- SharePoint Online dient zum Speichern der Videodatei und der Metadaten (Videotitel, Beschreibung usw.). Außerdem werden die Sicherheits-und Kompatibilitätsebenen (einschließlich Authentifizierung) sowie Suchfeatures bereitgestellt.
- Azure Media Services bietet Transcodierung, adaptives Streaming, sichere Bereitstellung (mit AES-Verschlüsselung) und Miniaturansicht-Features.

[Azure Media Services](https://azure.microsoft.com/services/media-services/) ist ein Plattform-as-a-Service-Angebot zum Aktivieren von End-to-End-Medien Workflows in der Cloud. Die Plattform bietet eine REST-API zum Hochladen, codieren, verschlüsseln (mit PlayReady) und zur Bereitstellung von Medien über Azure-Rechenzentren auf der ganzen Welt.

Alle Uploads für Office 365-Videos erfolgen über HTTPS. Wenn eine Videodatei hochgeladen wird, wird Sie in SharePoint Online gespeichert, und eine Kopie der Datei wird über einen verschlüsselten Kanal an Azure Media Services gesendet. Azure Media Services transcodiert das Video in mehrere Formate, die für die Anzeige optimiert sind (z. b. Mobile, niedrige Bandbreite, hohe Bandbreite usw.). Diese Dateien werden zusammen mit der beim Hochladen erworbenen Originaldatei im Azure-BLOB-Speicher gespeichert. Die Dateien werden mit AES 128 pro dem MPEG-Verschlüsselungsalgorithmus (oder einer früheren PlayReady-Version) für die Wiedergabe verschlüsselt und mithilfe der AES 256-Speicherverschlüsselung verschlüsselt, bevor Sie im Azure-BLOB-Speicher gespeichert werden. (Mithilfe des Azure Media Services-Client-SDK können Kunden steuern, welche Verschlüsselung verwendet wird. Ein Kunde könnte beispielsweise Azure Media Services-Speicherverschlüsselung (AES 256) auf ein hochwertiges Medienobjekt anwenden, bevor es den Azure-BLOB-Speicher hochlädt.)

Azure Media Services generiert außerdem eine Miniaturansicht für das Video, die über einen verschlüsselten Kanal zusammen mit Miniatur Ansichts Metadaten an SharePoint Online übertragen wird.

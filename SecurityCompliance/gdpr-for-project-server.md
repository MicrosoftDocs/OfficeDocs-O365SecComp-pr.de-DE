---
title: DSGVO für Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Erfahren Sie, wie Sie mit DSGVO-Anforderungen in lokalen Project Server-Installationen umgehen.
ms.openlocfilehash: 8fb29c2d383c03c79d619d2c78df75cffb4eab27
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154497"
---
# <a name="gdpr-for-project-server"></a>DSGVO für Project Server

Project Server verwendet benutzerdefinierte Skripts zum Exportieren und Bearbeiten von Benutzerdaten in Project Web App. Die grundlegende Vorgehensweise sieht folgendermaßen aus:

1.  Suchen Sie die Project Web App-Websites in Ihrer Farm.

2.  Suchen Sie auf jeder Website die Projekte, die den Benutzer enthalten.

3.  Exportieren und überprüfen Sie die Arten von Daten, die Sie überprüfen möchten.

4.  Bearbeiten Sie die Daten bei Bedarf.

In den folgenden Artikeln werden diese Schritte ausführlich beschrieben:

- [Exportieren von Benutzerdaten aus Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Löschen von Benutzerdaten aus Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Beachten Sie, dass Project Server auf SharePoint Server aufbaut und Ereignisse in SharePoint-ULS-Protokollen und in der Verwendungsdatenbank protokolliert. Weitere Informationen finden Sie unter [DSGVO für SharePoint Server](gdpr-for-sharepoint-server.md).

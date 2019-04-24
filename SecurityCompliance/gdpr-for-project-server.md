---
title: DSGVO für Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Erfahren Sie, wie Sie mit DSGVO-Anforderungen in lokalen Project Server-Installationen umgehen.
ms.openlocfilehash: 67097cdab4fdab31537cf4b6dd27ce17234c2bdc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255283"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="5204f-103">DSGVO für Project Server</span><span class="sxs-lookup"><span data-stu-id="5204f-103">GDPR for Project Server</span></span>

<span data-ttu-id="5204f-p101">Project Server verwendet benutzerdefinierte Skripts zum Exportieren und Bearbeiten von Benutzerdaten in Project Web App. Die grundlegende Vorgehensweise sieht folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="5204f-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="5204f-106">Suchen Sie die Project Web App-Websites in Ihrer Farm.</span><span class="sxs-lookup"><span data-stu-id="5204f-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="5204f-107">Suchen Sie auf jeder Website die Projekte, die den Benutzer enthalten.</span><span class="sxs-lookup"><span data-stu-id="5204f-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="5204f-108">Exportieren und überprüfen Sie die Arten von Daten, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="5204f-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="5204f-109">Bearbeiten Sie die Daten bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="5204f-109">Redact data as needed.</span></span>

<span data-ttu-id="5204f-110">In den folgenden Artikeln werden diese Schritte ausführlich beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5204f-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="5204f-111">Exportieren von Benutzerdaten aus Project Server</span><span class="sxs-lookup"><span data-stu-id="5204f-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="5204f-112">Löschen von Benutzerdaten aus Project Server</span><span class="sxs-lookup"><span data-stu-id="5204f-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="5204f-p102">Beachten Sie, dass Project Server auf SharePoint Server aufbaut und Ereignisse in SharePoint-ULS-Protokollen und in der Verwendungsdatenbank protokolliert. Weitere Informationen finden Sie unter [DSGVO für SharePoint Server](gdpr-for-sharepoint-server.md).</span><span class="sxs-lookup"><span data-stu-id="5204f-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>

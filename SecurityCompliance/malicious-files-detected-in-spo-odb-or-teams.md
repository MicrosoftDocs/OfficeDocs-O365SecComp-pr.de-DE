---
title: Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wo Sie Informationen zu böswilligen Dateien anzeigen können, die in SharePoint, OneDrive oder Teams erkannt werden, und wie Sie Maßnahmen für diese Dateien ergreifen.
ms.openlocfilehash: f5304f78ddec884748dd7d1090e2a7895044d045
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241897"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="f93f1-103">Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden</span><span class="sxs-lookup"><span data-stu-id="f93f1-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="f93f1-p101">[Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor schädlichen Dateien in Dokumentbibliotheken und Teamwebsites. Wenn eine bösartige Datei erkannt wird, wird diese Datei blockiert, sodass niemand Sie öffnen, kopieren, verschieben oder freigeben kann, bis weitere Aktionen des Sicherheitsteams der Organisation durchgeführt werden. In diesem Artikel erfahren Sie, wie Sie Informationen zu erkannten Dateien und zu ergreifenden Aktionen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="f93f1-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="f93f1-107">Zum Ausführen der in diesem Artikel beschriebenen Aufgaben benötigen Sie die erforderlichen [Berechtigungen für das Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="f93f1-107">In order to perform the tasks described in this article, you must have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="f93f1-108">Anzeigen von Berichten mit Informationen zu erkannten Dateien</span><span class="sxs-lookup"><span data-stu-id="f93f1-108">View reports with information about detected files</span></span>

<span data-ttu-id="f93f1-109">Zum Anzeigen des Status und detaillierter Informationen zu Dateien, die von Office 365 ATP erkannt wurden, können Sie den Statusbericht über den BedrohungsSchutz verwenden.</span><span class="sxs-lookup"><span data-stu-id="f93f1-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="f93f1-110">wählen sie im [Office 365 &amp; Security Compliance Center](https://protection.office.com)die option **berichte** \> - **Dashboard** \> **Threat Protection Status**aus.</span><span class="sxs-lookup"><span data-stu-id="f93f1-110">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="f93f1-111">Klicken Sie in der oberen rechten Ecke des Berichts auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f93f1-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="f93f1-112">Dient zum Anzeigen der Liste der Dateien, die im Bericht erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="f93f1-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="f93f1-113">Wählen Sie ein Element in der Liste aus, um detaillierte Informationen anzuzeigen, einschließlich der ausgeführten Aktionen, des Datei namens, des Dateipfads und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="f93f1-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="f93f1-114">Klicken Sie auf die Registerkarte **Erweiterte Analyse** , um Informationen wie beobachtete Verhaltens-und Analysedetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f93f1-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="f93f1-115">Anzeigen und Ausführen von Aktionen für Dateien in Quarantäne</span><span class="sxs-lookup"><span data-stu-id="f93f1-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="f93f1-116">wählen sie im Office 365 &amp; Security Compliance Center die option **Threat management** \> **Review** \> **quarantine**aus.</span><span class="sxs-lookup"><span data-stu-id="f93f1-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="f93f1-117">Ändern Sie in der oberen linken Ecke den Filter von **e-Mail** in **Inhalt**.</span><span class="sxs-lookup"><span data-stu-id="f93f1-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="f93f1-118">Wählen Sie ein Element in der Liste aus, um detaillierte Informationen, einschließlich der Datei-URL, anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f93f1-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="f93f1-119">Wählen Sie eine verfügbare Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f93f1-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="f93f1-120">Wählen **Sie &amp; Freigabe Bericht** aus, um die Datei aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="f93f1-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="f93f1-121">Wählen Sie **Bericht an Microsoft senden** aus, um die Datei als falsch positives Ergebnis an Microsoft zu melden.</span><span class="sxs-lookup"><span data-stu-id="f93f1-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="f93f1-122">Wählen Sie **Datei herunterladen** , um die Datei weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="f93f1-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="f93f1-p102">Wählen Sie **Löschen** aus, um die Datei aus der Liste der isolierten Elemente zu entfernen. Wenn Sie diese Option auswählen, müssen Sie die Datei auch aus der entsprechenden Bibliothek in SharePoint Online, OneDrive for Business oder Microsoft Teams löschen. Mit dieser Option wird das Öffnen oder Freigeben einer Datei nicht aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="f93f1-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="f93f1-126">Klicken Sie auf **Schließen** , um die Details für ein ausgewähltes Element zu schließen.</span><span class="sxs-lookup"><span data-stu-id="f93f1-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  


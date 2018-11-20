---
title: Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Erfahren Sie, wo Sie zum Anzeigen von Informationen zu schädliche Dateien in SharePoint, OneDrive oder Teams erkannt und wie Sie auf diese Dateien ergreifen.
ms.openlocfilehash: ba1dc3551e66800213a9cb988ebe9fc5e03e31f2
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238507"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="59a7e-103">Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt</span><span class="sxs-lookup"><span data-stu-id="59a7e-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="59a7e-p101">[Office 365 ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor schädliche Dateien in Dokumentbibliotheken und Teamwebsites. Wenn eine solche Datei erkannt wird, wird diese Datei blockiert, damit niemand öffnen, kopieren, verschieben oder freigeben, bis der Organisation Security Team Weitere Aktionen ausgeführt werden. Lesen Sie diesen Artikel, um Hier erfahren, wie Sie Informationen zu erkannten Dateien anzeigen und welche Aktionen vorgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59a7e-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="59a7e-107">Um die in diesem Artikel beschriebenen Aufgaben durchführen zu können, benötigen Sie die erforderlichen [in die Office 365-Sicherheit zugewiesenen Berechtigungen &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="59a7e-107">In order to perform the tasks described in this article, you must have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="59a7e-108">Anzeigen von Berichten mit Informationen zu erkannten Dateien</span><span class="sxs-lookup"><span data-stu-id="59a7e-108">View reports with information about detected files</span></span>

<span data-ttu-id="59a7e-109">Zum Anzeigen von Status und detaillierte Informationen zu Dateien, die von Office 365 ATP erkannt wurden, können Sie den Threat Protection Statusbericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="59a7e-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="59a7e-110">In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie **Berichte** \> **Dashboard** \> **Bedrohung Schutzstatus**.</span><span class="sxs-lookup"><span data-stu-id="59a7e-110">In the Office 365 Security &amp; Compliance Center, choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="59a7e-111">Wählen Sie in der oberen rechten Ecke des Berichts **Ansicht Detailtabelle**aus.</span><span class="sxs-lookup"><span data-stu-id="59a7e-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="59a7e-112">Anzeigen der Liste der Dateien, die im Bericht erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="59a7e-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="59a7e-113">Wählen Sie ein Element in der Liste, um ausführliche Informationen, einschließlich der Aktionen, den Dateinamen, den Dateipfad und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59a7e-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="59a7e-114">Wählen Sie die Registerkarte **Erweiterte Analyse** Informationen wie beobachteten Verhalten und Analysen Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59a7e-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="59a7e-115">Dient zum zeigen Sie an und führen Sie einer Aktion auf Dateien in Quarantäne aus</span><span class="sxs-lookup"><span data-stu-id="59a7e-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="59a7e-116">In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie **Threat Management** \> **Überprüfung** \> **Quarantine**.</span><span class="sxs-lookup"><span data-stu-id="59a7e-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="59a7e-117">Ändern Sie in der oberen linken Ecke des Filters von **E-Mail** auf **Inhalt**.</span><span class="sxs-lookup"><span data-stu-id="59a7e-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="59a7e-118">Wählen Sie ein Element in der Liste aus, um ausführliche Informationen, einschließlich der URL der Datei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="59a7e-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="59a7e-119">Auswählen einer verfügbaren Aktion an.</span><span class="sxs-lookup"><span data-stu-id="59a7e-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="59a7e-120">Wählen Sie **Release &amp; Bericht** für die Datei aufheben.</span><span class="sxs-lookup"><span data-stu-id="59a7e-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="59a7e-121">Wählen Sie auf die Datei als falsch positiv an Microsoft gemeldet **Bericht an Microsoft senden** .</span><span class="sxs-lookup"><span data-stu-id="59a7e-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="59a7e-122">Wählen Sie die **Datei herunterladen** , untersuchen Sie die Datei noch.</span><span class="sxs-lookup"><span data-stu-id="59a7e-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="59a7e-p102">Wählen Sie auf **Löschen** , um die Datei aus der Liste der in Quarantäne verschobenen Elemente zu entfernen. Wenn Sie diese Option auswählen, müssen Sie auch die Datei aus der entsprechenden Dokumentbibliothek in SharePoint Online, OneDrive for Business oder Microsoft-Teams löschen. Diese Option ist eine Datei verhindern oder freigegebenen geöffnete nicht Blockierung aufheben.</span><span class="sxs-lookup"><span data-stu-id="59a7e-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="59a7e-126">Wählen Sie auf **Schließen** , um die Details für ein ausgewähltes Element zu schließen.</span><span class="sxs-lookup"><span data-stu-id="59a7e-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  


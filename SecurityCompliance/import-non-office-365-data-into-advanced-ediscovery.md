---
title: Importieren von Inhalten für die erweiterte eDiscovery Analyse nicht - Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Wie BLOB-Schritten zum Importieren von Inhalt, die nicht in einer Azure in O365 gespeichert ist, damit es mit AeD analysiert werden kann
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530115"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="aec7c-103">Importieren von Inhalten für die erweiterte eDiscovery Analyse nicht - Office 365</span><span class="sxs-lookup"><span data-stu-id="aec7c-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="aec7c-p101">Nicht alle Dokumente, die Sie möglicherweise zur Analyse mit Office 365 erweiterte eDiscovery werden in Office 365 live. Importieren Sie mit dem Inhalt nicht Office 365-Feature in erweiterten eDiscovery Sie Dokumente hochladen können, die nicht in Office 365 (mit Ausnahme von PST-Dateien) in ein Blob Groß-/Kleinschreibung verknüpfte Azure Storage live und mit erweiterten eDiscovery zu analysieren. Dieses Verfahren wird veranschaulicht, wie Sie Ihre nicht - Office 365-Dokumente in erweiterten eDiscovery für die Analyse bringen.</span><span class="sxs-lookup"><span data-stu-id="aec7c-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="aec7c-p102">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="aec7c-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aec7c-p103">Sie können für Ihre nicht - Office 365-Inhalte ein Office 365 erweiterte eDiscovery Daten Speicher Add-on-Abonnement erwerben. Dies ist für Inhalte, die mit erweiterten eDiscovery analysiert werden ausschließlich zur Verfügung. Führen Sie die Schritte in [erwerben oder bearbeiten und Add-on für Office 365 für Unternehmen](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) und erwerben Sie das Office 365 erweiterte eDiscovery Speicher Add-on.</span><span class="sxs-lookup"><span data-stu-id="aec7c-p103">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content. This is exclusively available for content that is to be analyzed with Advanced eDiscovery. Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="aec7c-112">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="aec7c-112">Before you begin</span></span>

<span data-ttu-id="aec7c-113">Verwendung des Upload nicht Office 365-Features, wie in diesem Verfahren beschrieben muss vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="aec7c-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="aec7c-114">Ein Office 365 E3 mit erweiterte Compliance Add-on oder E5 Abonnement</span><span class="sxs-lookup"><span data-stu-id="aec7c-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="aec7c-115">Alle Verwalter, dessen Inhalt nicht - Office 365 hochgeladen werden, müssen mit erweiterte Compliance Add-on oder E5 Lizenzen E3 verfügen.</span><span class="sxs-lookup"><span data-stu-id="aec7c-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="aec7c-116">Eine vorhandene eDiscovery-Fall</span><span class="sxs-lookup"><span data-stu-id="aec7c-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="aec7c-p104">Alle zum Hochladen von Dateien in den Ordner, in dem ein Ordner pro Verwaltungsberechtigter vorhanden ist und die Ordner Name befindet sich in diesem Format *Alias@DomainName,* gesammelt werden. Die *alias@domainname* müssen Office 365-Benutzeralias und die Domäne sein. Sie können alle *alias@domainname* Ordner in einem Stammordner zusammenfassen. Stammordner kann nur die *alias@domainname* Ordner enthalten, es muss keine losen Dateien im Stammordner</span><span class="sxs-lookup"><span data-stu-id="aec7c-p104">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  . The  *alias@domainname*  must be users Office 365 alias and domain. You can collect all the  *alias@domainname*  folders into a root folder. The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="aec7c-121">Ein Konto, das entweder eine eDiscovery-Manager oder eine eDiscovery-Administrator ist</span><span class="sxs-lookup"><span data-stu-id="aec7c-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="aec7c-122">[Microsoft Azure-Speicher-Tools](https://aka.ms/downloadazcopy) auf einem Computer mit Zugriff auf die Struktur des nicht - Office 365 Content-Ordner installiert.</span><span class="sxs-lookup"><span data-stu-id="aec7c-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="aec7c-123">Hochladen Sie nicht - Office 365-Inhalte in erweiterten eDiscovery</span><span class="sxs-lookup"><span data-stu-id="aec7c-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="aec7c-p105">Als eDiscovery-Manager oder eDiscovery-Administrator öffnen Sie **eDiscovery**, und öffnen Sie die Groß-/Kleinschreibung, der die Daten nicht - Office 365 zu hochgeladen werden soll. Wenn Sie eine Anfrage erstellen müssen, finden Sie unter [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](manage-ediscovery-cases.md)</span><span class="sxs-lookup"><span data-stu-id="aec7c-p105">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to. If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="aec7c-126">Klicken Sie auf **Wechseln zu erweiterten eDiscovery**</span><span class="sxs-lookup"><span data-stu-id="aec7c-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="aec7c-127">Wählen Sie unter **Typ der Datenquelle** **nicht Office 365-Daten**.</span><span class="sxs-lookup"><span data-stu-id="aec7c-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="aec7c-p106">Klicken Sie auf **Add Container**. Nennen Sie den Container, und fügen Sie eine Beschreibung hinzu.</span><span class="sxs-lookup"><span data-stu-id="aec7c-p106">Click **Add container**. Name the container and add a description.</span></span>
    
5. <span data-ttu-id="aec7c-130">Wählen Sie den neu hinzugefügten Container aus der Containerliste, und kopieren Sie die URL, die im Detailbereich Container angezeigt wird, und schließen Sie den Bereich</span><span class="sxs-lookup"><span data-stu-id="aec7c-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="aec7c-131">Öffnen Sie ein Eingabeaufforderungsfenster als Administrator, und wechseln Sie zum Verzeichnis zum Ordner, in dem Sie AzCopy installiert haben.</span><span class="sxs-lookup"><span data-stu-id="aec7c-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="aec7c-132">Erstellen Sie die Befehlszeile AzCopy zum Hochladen von Dateien wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aec7c-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="aec7c-p107">AzCopy/Source: " *vollständigen Pfad zum Stammordner auf lokalen Computer* " / dest: " *Container URLs bis, aber nicht einschließlich der?* " /DestSAS: " *Rest der Container-Url aus der? zum Ende* "/ S.</span><span class="sxs-lookup"><span data-stu-id="aec7c-p107">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*  " /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="aec7c-135">Beispielsweise mithilfe der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="aec7c-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="aec7c-136">Stammordner - C:\Collected Daten</span><span class="sxs-lookup"><span data-stu-id="aec7c-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="aec7c-137">Container-Url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;Si NonOfficeData15 = %7 C 0&amp;Sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA % 3D</span><span class="sxs-lookup"><span data-stu-id="aec7c-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="aec7c-138">die Befehlszeilensyntax AzCopy wäre:</span><span class="sxs-lookup"><span data-stu-id="aec7c-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="aec7c-139">Weitere Informationen zu Azcopy Syntax finden Sie unter, [Übertragen von Daten mit der AzCopy auf Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span><span class="sxs-lookup"><span data-stu-id="aec7c-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="aec7c-140">Es muss ein Stammordner pro Benutzer und der Name des Ordners muss im Format *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="aec7c-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="aec7c-p108">Nachdem die Ordner hochladen haben, wechseln Sie wieder zur erweiterten eDiscovery. Der Inhalt in den Ordnern, die Sie hochgeladen haben kann jetzt im erweiterten eDiscovery verarbeitet werden. Wählen Sie den Container, und klicken Sie auf die Schaltfläche Prozess. Weitere Informationen zu erweiterten eDiscovery Verarbeitung finden Sie unter, [Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="aec7c-p108">Once the folders have finished uploading, switch back to Advanced eDiscovery. The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery. Select the container and click the Process button. For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="aec7c-p109">Nachdem Sie der Container in der erweiterten eDiscovery erfolgreich verarbeitet wird, werden Sie nicht mehr, neuen Inhalt hinzuzufügen, um die SAS-Speicher in Azure sein. Wenn Sie zusätzliche Inhalte sammeln und Sie es die Groß-/Kleinschreibung für die erweiterte eDiscovery-Analyse hinzufügen möchten, müssen Sie einen neuen Container **nicht Office 365-Daten** erstellen und wiederholen Sie dieses Verfahren.</span><span class="sxs-lookup"><span data-stu-id="aec7c-p109">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure. If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="aec7c-147">Wenn der Container *verarbeitet nicht erfolgreich aufgrund Ordner naming Probleme* und Sie dann die Probleme beheben, müssen Sie zum Erstellen einer neuen Container und die Verbindung wiederherstellen und hochladen, erneut mit den Verfahren in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="aec7c-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span> 
  


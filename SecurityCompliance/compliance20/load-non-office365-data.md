---
title: Laden von Nicht-Office 365-Daten in einen Arbeitssatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1dad52075303450673e7f48b87e2952e35629a5e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706086"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="dce14-102">Laden von Nicht-Office 365-Daten in einen Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="dce14-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="dce14-p101">Nicht alle Dokumente, die Sie möglicherweise zur Analyse mit Office 365 erweiterte eDiscovery werden in Office 365 live. Importieren Sie mit dem Inhalt nicht Office 365-Feature in erweiterten eDiscovery Sie Dokumente hochladen können, die in Office 365 in einer Arbeitssatz live nicht, damit diese mit erweiterten eDiscovery analysiert werden. Dieses Verfahren wird veranschaulicht, wie Sie Ihre nicht - Office 365-Dokumente in erweiterten eDiscovery für die Analyse bringen.</span><span class="sxs-lookup"><span data-stu-id="dce14-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="dce14-p102">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.</span><span class="sxs-lookup"><span data-stu-id="dce14-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="dce14-108">Bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="dce14-108">Before you begin</span></span>
<span data-ttu-id="dce14-109">Verwendung des Upload nicht Office 365-Features, wie in diesem Verfahren beschrieben muss vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="dce14-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="dce14-110">Ein Office 365 E3 mit erweiterte Compliance Add-on oder E5 Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dce14-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="dce14-111">Alle Verwalter, dessen Inhalt nicht - Office 365 hochgeladen werden soll, müssen E3 mit erweiterte Compliance Add-on oder E5 Lizenzen verfügen.</span><span class="sxs-lookup"><span data-stu-id="dce14-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="dce14-112">Eine vorhandene eDiscovery-Fall.</span><span class="sxs-lookup"><span data-stu-id="dce14-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="dce14-p103">Alle zum Hochladen von Dateien in den Ordner, in dem ein Ordner pro Verwaltungsberechtigter vorhanden ist und die Ordner Name befindet sich in diesem Format *Alias@DomainName,* gesammelt werden. Die *alias@domainname* müssen Office 365-Benutzeralias und die Domäne sein. Sie können alle *alias@domainname* Ordner in einem Stammordner zusammenfassen. Stammordner kann nur die *alias@domainname* Ordner enthalten, es muss keine losen Dateien im Stammordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dce14-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="dce14-117">Ein Konto, das entweder ein eDiscovery-Manager oder eDiscovery Microsoft Azure Storage Administratortools auf einem Computer mit Zugriff auf die Struktur des nicht - Office 365 Content-Ordner installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dce14-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="dce14-118">Installieren Sie AzCopy, was hier möglich:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="dce14-118">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="dce14-119">Hochladen Sie nicht - Office 365-Inhalte in erweiterten eDiscovery</span><span class="sxs-lookup"><span data-stu-id="dce14-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="dce14-p104">Öffnen Sie als ein eDiscovery-Manager oder eine eDiscovery-Administrator erweiterte eDiscovery, und klicken Sie dann auf die Groß-/Kleinschreibung, der die Daten nicht - Office 365 zu hochgeladen werden soll.  Klicken Sie auf der Registerkarte **legt arbeiten** , und wählen Sie dann des Arbeitssatzes, die, dem Sie die Daten nicht-Office 365 zu laden möchten.  Wenn Sie nicht bereits ein Arbeitssatz erstellt haben, können Sie dies jetzt tun.  Klicken Sie abschließend auf **Verwalten Funktionsweise festgelegt** und dann **Uploads anzeigen** im Datenabschnitt nicht Office 365</span><span class="sxs-lookup"><span data-stu-id="dce14-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="dce14-124">Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht-Office 365-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="dce14-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="dce14-p105">Der erste Schritt im Assistenten bereitet einfach einen sicheren Azure Blob für die Dateien hochgeladen werden.  Nach der Vorbereitung Compelted ist, klicken Sie auf die **Weiter: Hochladen von Dateien** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="dce14-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Nicht-Office 365 importieren – vorbereiten](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="dce14-p106">**Hochladen von Dateien** im Schritt geben Sie den **Pfad zum Speicherort der Dateien**, ist dies, in die nicht-Office 365-Daten, die Sie zum Importieren von planen gespeichert ist.  Festlegen des richtigen Speicherorts wird der AzCopy Befehl ordnungsgemäß aktualisiert wird sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="dce14-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="dce14-131">Wenn Sie AzCopy noch nicht installiert haben, können Sie hier dazu:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="dce14-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="dce14-p107">Kopieren Sie den vordefinierten Befehl durch Klicken auf den Link **in die Zwischenablage kopieren** . Starten einer Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden in der sicheren Azure BLOB-Speicher für den nächsten Schritt hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="dce14-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Importieren von nicht-Office 365 - Hochladen von Dateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importieren von nicht-Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="dce14-p108">Schließlich zum der & Security Compliance zurückzukehren, und klicken Sie auf die **Weiter: Dateien verarbeiten** Schaltfläche.  Dies wird initiiert Verarbeitung Extraktion von Text und Indizieren der hochgeladenen Dateien.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** verfolgen.  Sobald abgeschlossen ist, werden die neuen Dateien in den Arbeitsseiten verfügbar sein.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.</span><span class="sxs-lookup"><span data-stu-id="dce14-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Importieren von nicht-Office 365 - Dateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)


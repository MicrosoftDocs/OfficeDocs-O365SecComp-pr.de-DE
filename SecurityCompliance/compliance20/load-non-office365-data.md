---
title: Laden von Nicht-Office 365-Daten in einen Arbeitssatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 50fcf679b5cd17a079765bfca5435088bef4c06e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217685"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="4fa41-102">Laden von Nicht-Office 365-Daten in einen Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="4fa41-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="4fa41-p101">Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, Leben in Office 365. Mit der nicht-Office 365-Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die nicht in Office 365 Leben, in einen Arbeitssatz hochladen, sodass Sie mit Advanced eDiscovery analysiert werden. In diesem Verfahren wird gezeigt, wie Sie Ihre nicht-Office 365-Dokumente in Advanced eDiscovery for Analysis einbinden.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="4fa41-p102">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="4fa41-108">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="4fa41-108">Before you begin</span></span>
<span data-ttu-id="4fa41-109">Für die Verwendung der in diesem Verfahren beschriebenen Funktion zum Hochladen von nicht-Office 365-Funktionen ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="4fa41-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="4fa41-110">Ein Office 365 E3 mit Advanced Compliance-Add-on oder E5-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fa41-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="4fa41-111">Alle Verwalter, deren nicht-Office 365-Inhalte hochgeladen werden, müssen E3 mit Advanced Compliance Add-on oder E5-Lizenzen haben.</span><span class="sxs-lookup"><span data-stu-id="4fa41-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="4fa41-112">Ein vorhandener eDiscovery-Fall.</span><span class="sxs-lookup"><span data-stu-id="4fa41-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="4fa41-p103">Alle Dateien zum Hochladen in Ordner, in denen ein Ordner pro Depotbank vorhanden ist, und der Name der Ordner in diesem Format *Alias @ Domainname* . *Bei dem Alias @ Domain Name* muss es sich um Benutzer von Office 365 Alias und Domäne handeln. Sie können alle *Alias @ Domain Name* -Ordner in einem Stammordner sammeln. Der Stammordner kann nur die *Alias @ Domain Name* -Ordner enthalten, es dürfen keine losen Dateien im Stammordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="4fa41-117">Ein Konto, das entweder ein eDiscovery-Manager oder ein eDiscovery-Administrator ist, Microsoft Azure-Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die nicht-Office 365-Inhaltsordner Struktur hat.</span><span class="sxs-lookup"><span data-stu-id="4fa41-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="4fa41-118">Installieren Sie AzCopy, was Sie hier tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="4fa41-118">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="4fa41-119">Hochladen von nicht-Office 365-Inhalten in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4fa41-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="4fa41-p104">Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, und führen Sie dann den Fall aus, dass die nicht-Office 365-Daten in hochgeladen werden.  Klicken Sie auf die Registerkarte **Working Sets** , und wählen Sie dann den Arbeitssatz aus, in den Sie die nicht-Office 365-Daten laden möchten.  Wenn Sie noch keine Arbeitsmappe erstellt haben, können Sie dies jetzt tun.  Klicken Sie abschließend auf Workings- **Set verwalten** und dann auf **Uploads** im nicht-Office 365-Datenabschnitt</span><span class="sxs-lookup"><span data-stu-id="4fa41-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="4fa41-124">Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht-Office 365-Datenimport-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="4fa41-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="4fa41-p105">Im ersten Schritt des Assistenten wird ein sicheres Azure-BLOB für die hochzuladenden Dateien vorbereitet.  Wenn die Vorbereitung compelted ist, klicken Sie auf die Schaltfläche **Weiter: Dateien hochladen** .</span><span class="sxs-lookup"><span data-stu-id="4fa41-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Nicht-Office 365-Import-Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="4fa41-p106">Geben Sie im Schritt **Dateien hochladen** den **Pfad zum Speicherort von Dateien**an, in dem sich die nicht von Office 365-Daten, die Sie beim Importieren einplanen, befinden.  Durch Festlegen des korrekten Speicherorts wird sichergestellt, dass der AzCopy-Befehl ordnungsgemäß aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="4fa41-131">Wenn Sie AzCopy noch nicht installiert haben, können Sie dies hier tun:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="4fa41-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="4fa41-p107">Kopieren Sie den vordefinierten Befehl, indem Sie auf den Link **in die Zwischenablage kopieren** klicken. Starten Sie eine Windows-Eingabeaufforderungen, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.  Die Dateien werden für den nächsten Schritt in den Secure Azure BLOB-Speicher hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Nicht-Office 365 Import-Uploaddateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Nicht-Office 365-Import-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="4fa41-p108">Kehren Sie schließlich zur Security & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Process files** .  Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.  Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald der Vorgang abgeschlossen ist, sind die neuen Dateien im Arbeitssatz verfügbar.  Nach Abschluss der Verarbeitung können Sie den Assistenten schließen.</span><span class="sxs-lookup"><span data-stu-id="4fa41-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Nicht-Office 365-Import-Prozessdateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)


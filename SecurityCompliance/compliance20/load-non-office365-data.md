---
title: Laden von Nicht-Office 365-Daten in einen Prüfdateisatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 86d858994f95176ea4d415405c4043f7e7c5308e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155007"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="f102b-102">Laden von Nicht-Office 365-Daten in einen Prüfdateisatz</span><span class="sxs-lookup"><span data-stu-id="f102b-102">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="f102b-103">Nicht alle Dokumente, die Sie möglicherweise mit Office 365 Advanced eDiscovery analysieren müssen, werden in Office 365 Live verwendet.</span><span class="sxs-lookup"><span data-stu-id="f102b-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="f102b-104">Mit der nicht Office 365en Inhalts Importfunktion in Advanced eDiscovery können Sie Dokumente, die nicht in Office 365 Leben, in einen Überprüfungs hochladen, damit diese mit Advanced eDiscovery analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="f102b-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a review set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="f102b-105">In diesem Verfahren erfahren Sie, wie Sie Ihre nicht-Office 365-Dokumente zur Analyse in Advanced eDiscovery integrieren.</span><span class="sxs-lookup"><span data-stu-id="f102b-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="f102b-106">Advanced eDiscovery erfordert eine Office 365 E3 mit dem Advanced Compliance-Add-on oder ein E5-Abonnement für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="f102b-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="f102b-107">Wenn Sie diesen Plan nicht haben und Advanced eDiscovery testen möchten, können Sie sich für eine Testversion von Office 365 Enterprise E5 anmelden.</span><span class="sxs-lookup"><span data-stu-id="f102b-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f102b-108">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="f102b-108">Before you begin</span></span>

<span data-ttu-id="f102b-109">Wenn Sie das Feature "nicht Office 365 hochladen" wie in diesem Artikel beschrieben verwenden, müssen Sie über Folgendes verfügen:</span><span class="sxs-lookup"><span data-stu-id="f102b-109">Using the upload Non-Office 365 feature as described in this article requires that you have the following:</span></span>

- <span data-ttu-id="f102b-110">Ein Office 365-oder Microsoft 365 E5-Abonnement oder ein E3-Abonnement mit dem Add-on-Abonnement für erweiterte Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="f102b-110">An Office 365 or Microsoft 365 E5 subscription or an E3 subscription with the Advanced Compliance add-on subscription.</span></span>

- <span data-ttu-id="f102b-111">Alle Verwalter, deren nicht Office 365 Inhalt hochgeladen wird, müssen über eine E3-Lizenz mit einer Add-on-Lizenz für Advanced Compliance verfügen oder über eine E5-Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="f102b-111">All custodians whose non-Office 365 content will be uploaded must have E3 license with an Advanced Compliance add-on license or have an E5 license.</span></span>

- <span data-ttu-id="f102b-112">Ein vorhandener erweiterter eDiscovery-Fall.</span><span class="sxs-lookup"><span data-stu-id="f102b-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="f102b-113">Verwalter müssen dem Fall hinzugefügt werden, bevor Sie die nicht Office 365 Daten hochladen, die Ihnen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f102b-113">Custodians must be added to the case before you upload the non-Office 365 data that's associated to them.</span></span>

- <span data-ttu-id="f102b-114">Alle hochzuladenden Dateien müssen sich in Ordnern befinden, in denen jeder Ordner einer bestimmten Depotbank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f102b-114">All files that will be uploaded must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="f102b-115">Für die Namen dieser Ordner muss das folgende Benennungsformat verwendet werden: *Alias @ Domain*Name.</span><span class="sxs-lookup"><span data-stu-id="f102b-115">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="f102b-116">Der *Alias @ Domain Name* muss der Office 365 Alias und die Domäne des Benutzers sein.</span><span class="sxs-lookup"><span data-stu-id="f102b-116">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="f102b-117">Sie können alle Alias- *@ Domain Name* -Ordner in einem Stammordner sammeln.</span><span class="sxs-lookup"><span data-stu-id="f102b-117">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="f102b-118">Der Stammordner kann nur die Ordner *Alias @ Domain Name* enthalten; Loose-Dateien sind im Stammordner nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f102b-118">The root folder can only contain the *alias@domainname* folders; loose files aren't allowed in the root folder.</span></span>

   <span data-ttu-id="f102b-119">Beispielsweise ähnelt die Ordnerstruktur für die nicht Office 365 Daten, die Sie hochladen möchten, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f102b-119">For example, the folder structure for the non-Office 365 data that you want to upload would be similar to the following:</span></span>

   - <span data-ttu-id="f102b-120">c:\nonO365\abraham.McMahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f102b-120">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="f102b-121">c:\nonO365\jewell.Gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f102b-121">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="f102b-122">c:\nonO365\staci.Gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f102b-122">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="f102b-123">Dabei sind Abraham.McMahon@contoso.com, Jewell.Gordon@contoso.com und Staci.Gonzalez@contoso.com die SMTP-Adressen der Verwalter in dem Fall.</span><span class="sxs-lookup"><span data-stu-id="f102b-123">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Ordnerstruktur für nicht Office 365E Datenuploads](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="f102b-125">Ein Konto, das entweder eDiscovery-Manager oder eDiscovery-Administrator ist</span><span class="sxs-lookup"><span data-stu-id="f102b-125">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>

- <span data-ttu-id="f102b-126">Microsoft Azure Speicher Tools, die auf einem Computer installiert sind, der Zugriff auf die Struktur nicht Office 365 Inhaltsordner hat.</span><span class="sxs-lookup"><span data-stu-id="f102b-126">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="f102b-127">Installieren Sie AzCopy, was Sie von hier aus tun können:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="f102b-127">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="f102b-128">Hochladen nicht Office 365er Inhalte in die erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f102b-128">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="f102b-129">Öffnen Sie als eDiscovery-Manager oder eDiscovery-Administrator Advanced eDiscovery, dann werden die nicht Office 365-Daten hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="f102b-129">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="f102b-130">Klicken Sie auf die Registerkarte Überprüfungs **Sätze** , und wählen Sie dann den Überprüfungs Satz aus, in den Sie die nicht Office 365 Daten laden möchten.</span><span class="sxs-lookup"><span data-stu-id="f102b-130">Click the **review sets** tab, then select the review set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="f102b-131">Wenn Sie noch keinen Überprüfungs Sätze erstellt haben, können Sie dies jetzt tun.</span><span class="sxs-lookup"><span data-stu-id="f102b-131">If you have not already created a review set, you can do so now.</span></span>  <span data-ttu-id="f102b-132">Klicken Sie schließlich auf **Überarbeitungs Gruppe verwalten** , und klicken Sie dann auf **Uploads anzeigen** in der \* \* nicht Office 365 Daten Kachel.</span><span class="sxs-lookup"><span data-stu-id="f102b-132">Finally, click **Manage review set** and then click **View uploads** in the \*\*Non-Office 365 data tile.</span></span>

2. <span data-ttu-id="f102b-133">Klicken Sie auf die Schaltfläche **Dateien hochladen** , um den nicht Office 365 Datenimport-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="f102b-133">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

   ![Hochladen von Dateien](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="f102b-135">Im ersten Schritt des Assistenten wird einfach ein sicheres Azure-BLOB für die zu hochzuladenden Dateien vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="f102b-135">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="f102b-136">Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf die Schaltfläche **Weiter: Dateien hochladen** .</span><span class="sxs-lookup"><span data-stu-id="f102b-136">Once preparation is completed, click the **Next: Upload files** button.</span></span>

   ![Nicht Office 365 Import – Prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="f102b-138">Geben Sie im Schritt **Upload Files** den **Pfad zum Speicherort der Dateien**an, hier befinden sich die nicht Office 365 Daten, die Sie beim Import planen.</span><span class="sxs-lookup"><span data-stu-id="f102b-138">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="f102b-139">Durch Festlegen des richtigen Speicherorts wird sichergestellt, dass der AzCopy-Befehl ordnungsgemäß aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f102b-139">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f102b-140">Wenn Sie AzCopy nicht bereits installiert haben, können Sie dies hier tun:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="f102b-140">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="f102b-141">Kopieren Sie den vordefinierten Befehl, indem Sie auf den Link **in Zwischenablage kopieren** klicken.</span><span class="sxs-lookup"><span data-stu-id="f102b-141">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="f102b-142">Starten Sie eine Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="f102b-142">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="f102b-143">Die Dateien werden in den sicheren Azure-BLOB-Speicher für den nächsten Schritt hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="f102b-143">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

   ![Nicht Office 365 Import-Upload-Dateien](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Nicht Office 365 Import – AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="f102b-146">Wenn der angegebene AzCopy-Befehl fehlschlägt, lesen Sie [Troubleshooting AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="f102b-146">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="f102b-147">Kehren Sie schließlich zur Sicherheit & Compliance zurück, und klicken Sie auf die Schaltfläche **Weiter: Prozessdateien** .</span><span class="sxs-lookup"><span data-stu-id="f102b-147">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="f102b-148">Dadurch wird die Verarbeitung, die Textextraktion und die Indizierung der hochgeladenen Dateien initiiert.</span><span class="sxs-lookup"><span data-stu-id="f102b-148">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="f102b-149">Sie können den Fortschritt der Verarbeitung hier oder auf der Registerkarte **Aufträge** nachverfolgen.  Sobald die neuen Dateien abgeschlossen sind, sind Sie im Überprüfungs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f102b-149">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the review set.</span></span>  <span data-ttu-id="f102b-150">Nachdem die Verarbeitung abgeschlossen ist, können Sie den Assistenten schließen.</span><span class="sxs-lookup"><span data-stu-id="f102b-150">Once processing is complete, you can dismiss the wizard.</span></span>

   ![Nicht Office 365 Import Prozess-Dateien](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)


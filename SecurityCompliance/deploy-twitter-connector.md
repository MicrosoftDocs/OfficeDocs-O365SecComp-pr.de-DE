---
title: Bereitstellen eines Connectors zum Archivieren von Twitter-Daten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Administratoren können einen systemeigenen Connector zum Importieren und Archivieren von Twitter-Daten in Office 365 einrichten. Nachdem diese Daten in Office 365 importiert wurden, können Sie Compliance-Features wie Legal Hold, Inhaltssuche und Aufbewahrungsrichtlinien verwenden, um die Steuerung der Twitter-Daten Ihrer Organisation zu verwalten.
ms.openlocfilehash: 4d3bce8418ef2fa62c40d221549e6e089dee9647
ms.sourcegitcommit: 6c0fcb82178a4ac26375545f328389a6852a81be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2019
ms.locfileid: "34490545"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a><span data-ttu-id="582f2-104">Bereitstellen eines Connectors zum Archivieren von Twitter-Daten in Office 365</span><span class="sxs-lookup"><span data-stu-id="582f2-104">Deploy a connector to archive Twitter data in Office 365</span></span>

<span data-ttu-id="582f2-105">Dieser Artikel enthält den schrittweisen Prozess zur Bereitstellungeines Connectors, der den Office 365 Import Dienst verwendet, um Daten aus dem Twitter-Konto Ihrer Organisation in Office 365 zu importieren.</span><span class="sxs-lookup"><span data-stu-id="582f2-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from your organization's Twitter account to Office 365.</span></span> <span data-ttu-id="582f2-106">Eine allgemeine Übersicht über diesen Prozess und eine Liste der erforderlichen Voraussetzungen für die Bereitstellungeines Twitter-Konnektors finden Sie unter [Verwenden eines Beispiel-Konnektors zum Archivieren von Twitter-Daten in Office 365 (Preview)](archive-twitter-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="582f2-106">For a high-level overview of this process and a list of prerequisites required to deploy a Twitter connector, see [Use a sample connector to archive Twitter data in Office 365 (Preview)](archive-twitter-data-with-sample-connector.md).</span></span> 

## <a name="step-1-download-the-package"></a><span data-ttu-id="582f2-107">Schritt 1: Herunterladen des Pakets</span><span class="sxs-lookup"><span data-stu-id="582f2-107">Step 1: Download the package</span></span>

<span data-ttu-id="582f2-108">Laden Sie das vorgefertigte Paket aus dem Abschnitt Release im GitHub-Repository unter [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)herunter.</span><span class="sxs-lookup"><span data-stu-id="582f2-108">Download the prebuilt package from the Release section in the GitHub repository at [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases).</span></span> <span data-ttu-id="582f2-109">Laden Sie die ZIP-Datei mit dem Namen **SampleConnector. zip**unter der neuesten Version herunter.</span><span class="sxs-lookup"><span data-stu-id="582f2-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="582f2-110">Sie werden diese ZIP-Datei in Schritt 4 in Azure hochladen.</span><span class="sxs-lookup"><span data-stu-id="582f2-110">You will upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="582f2-111">Schritt 2: Erstellen einer APP in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="582f2-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="582f2-112">Wechseln Sie <https://portal.azure.com> zu, und melden Sie sich mit den Anmeldeinformationen eines Office 365 globalen Administratorkontos an.</span><span class="sxs-lookup"><span data-stu-id="582f2-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

   ![](media/TCimage01.png)

2. <span data-ttu-id="582f2-113">Klicken Sie im linken Navigationsbereich auf **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="582f2-113">In the left navigation pane, click **Azure Active Directory**.</span></span>

   ![](media/TCimage02.png)

3. <span data-ttu-id="582f2-114">Klicken Sie im linken Navigationsbereich auf **App-Registrierungen (Vorschau)** , und klicken Sie dann auf **neue Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="582f2-114">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

   ![](media/TCimage03.png)

4. <span data-ttu-id="582f2-115">Registrieren Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="582f2-115">Register the application.</span></span> <span data-ttu-id="582f2-116">Wählen Sie unter Umleitungs- **URI (optional)** in der Dropdownliste Anwendungstyp die <https://portal.azure.com> Option Webseite aus, und geben Sie dann in das Feld für den URI ein.</span><span class="sxs-lookup"><span data-stu-id="582f2-116">Under **Redirect URI (optional)**, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/TCimage04.png)

5. <span data-ttu-id="582f2-117">Kopieren Sie die Anwendungs-ID **(Client) ID** und **Verzeichnis (Mandanten)** , und speichern Sie Sie in einer Textdatei oder an einem anderen sicheren Ort.</span><span class="sxs-lookup"><span data-stu-id="582f2-117">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="582f2-118">Sie verwenden diese IDs in späteren Schritten.</span><span class="sxs-lookup"><span data-stu-id="582f2-118">You’ll use these IDs in later steps.</span></span>

    ![](media/TCimage05.png)

6. <span data-ttu-id="582f2-119">Wechseln Sie zu **Certificates & Secrets for the New App** und unter **Client Secrets** auf **New Client Secret**.</span><span class="sxs-lookup"><span data-stu-id="582f2-119">Go to **Certificates & secrets for the new app** and under **Client secrets** click **New client secret**.</span></span>

   ![](media/TCimage06.png)

7. <span data-ttu-id="582f2-120">Erstellen Sie einen neuen geheimen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="582f2-120">Create a new secret.</span></span> <span data-ttu-id="582f2-121">Geben Sie im Feld Beschreibung den geheimen Schlüssel ein, und wählen Sie dann einen Ablaufzeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="582f2-121">In the description box, type the secret and then choose an expiration period.</span></span> 

   ![](media/TCimage08.png)

8. <span data-ttu-id="582f2-122">Kopieren Sie den Wert des geheimen Schlüssels, und speichern Sie ihn in einer Textdatei oder an einem anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-122">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="582f2-123">Dies ist der geheime Aad-Anwendungsschlüssel, den Sie in späteren Schritten verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="582f2-123">This is the AAD application secret that you will use in later steps.</span></span>

   ![](media/TCimage09.png)

9. <span data-ttu-id="582f2-124">Wechseln Sie zu **Manifest** , und kopieren Sie die identifierUris (die auch als Aad Application URI bezeichnet wird) wie im folgenden Screenshot hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="582f2-124">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="582f2-125">Kopieren Sie den Aad-Anwendungs-URI in eine Textdatei oder einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-125">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="582f2-126">Sie verwenden Sie in Schritt 6.</span><span class="sxs-lookup"><span data-stu-id="582f2-126">You’ll use it in Step 6.</span></span>

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="582f2-127">Schritt 3: Erstellen eines Azure-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="582f2-127">Step 3: Create an Azure storage account</span></span>

1.  <span data-ttu-id="582f2-128">Wechseln Sie zur Azure-Startseite für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="582f2-128">Go to the Azure home page for your organization.</span></span>

    ![](media/TCimage11.png)

2. <span data-ttu-id="582f2-129">Klicken Sie auf **Ressource erstellen** , und geben Sie **Speicherkonto** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="582f2-129">Click **Create a resource** and they type **storage account** in the search box.</span></span>

   ![](media/TCimage12.png)

3. <span data-ttu-id="582f2-130">Klicken Sie auf **Speicher**, und klicken Sie dann auf **Speicherkonto**.</span><span class="sxs-lookup"><span data-stu-id="582f2-130">Click **Storage**, and then click **Storage account**.</span></span>

   ![](media/TCimage13.png)

4. <span data-ttu-id="582f2-131">Wählen Sie auf der Seite **Speicherkonto erstellen** im Feld Abonnement die Option **Pay-as-you-go** oder **﻿Kostenlose Testversion** je nach Typ des Azure-Abonnements aus.</span><span class="sxs-lookup"><span data-stu-id="582f2-131">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> 

   ![](media/TCimage14.png)

5. <span data-ttu-id="582f2-132">Wählen oder erstellen Sie eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="582f2-132">Select or create a resource group.</span></span>

   ![](media/TCimage15.png)

6. <span data-ttu-id="582f2-133">Geben Sie einen Namen für das Speicherkonto ein.</span><span class="sxs-lookup"><span data-stu-id="582f2-133">Type a name for the storage account.</span></span>

   ![](media/TCimage16.png)

7. <span data-ttu-id="582f2-134">Überprüfen Sie, und klicken Sie dann auf **Erstellen** , um das Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="582f2-134">Review and then click **Create** to create the storage account.</span></span>

   ![](media/TCimage17.png)

8. <span data-ttu-id="582f2-135">Klicken Sie nach einigen Momenten auf **Aktualisieren** , und klicken Sie dann auf **Ressource wechseln** , um zum Speicherkonto zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="582f2-135">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

   ![](media/TCimage18.png)

9. <span data-ttu-id="582f2-136">Klicken Sie im linken Navigationsbereich auf **Zugriffstasten** .</span><span class="sxs-lookup"><span data-stu-id="582f2-136">Click **Access keys** in the left navigation pane.</span></span>

   ![](media/TCimage19.png)

10. <span data-ttu-id="582f2-137">Kopieren Sie eine **Verbindungszeichenfolge** , und speichern Sie Sie in einer Textdatei oder an einem anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-137">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="582f2-138">Verwenden Sie diese Option, wenn Sie in Schritt 4 eine Webanwendungs Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="582f2-138">You’ll use this when creating a web app resource in Step 4.</span></span>

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="582f2-139">Schritt 4: Erstellen einer neuen webapp-Ressource in Azure</span><span class="sxs-lookup"><span data-stu-id="582f2-139">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="582f2-140">Klicken Sie auf der **Start** Seite im Azure-Portal auf **Ressource \> : alles \> -Webanwendung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="582f2-140">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="582f2-141">Klicken Sie \*\*\*\* auf der Seite Webanwendung auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="582f2-141">On the **Web app** page, click **Create**.</span></span>

   ![](media/TCimage21.png)

2. <span data-ttu-id="582f2-142">Geben Sie die Details ein (wie unten dargestellt), und erstellen Sie dann die Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="582f2-142">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="582f2-143">Beachten Sie, dass der Name, den Sie in das Feld **App-Name** eingeben, zum Erstellen der Azure-App-Dienst-URL verwendet wird. Beispiel twitterconnector.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="582f2-143">Note that the name that you enter in the **App name** box will be used to create the Azure app service URL; for example twitterconnector.azurewebsites.net.</span></span>

   ![](media/TCimage22.png)

3. <span data-ttu-id="582f2-144">Wechseln Sie zur neu erstellten Webanwendungs-Ressource, und klicken Sie im linken Navigationsbereich auf **Anwendungseinstellungen** .</span><span class="sxs-lookup"><span data-stu-id="582f2-144">Go to the newly created web app resource, click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="582f2-145">Klicken Sie unter **Anwendungseinstellungen**auf **neue Einstellung hinzufügen** , und fügen Sie die folgenden drei Einstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="582f2-145">Under **Application settings**, click **Add new setting** and add the following three settings.</span></span> <span data-ttu-id="582f2-146">Verwenden Sie die Werte (die Sie in die Textdatei aus den vorherigen Schritten kopiert haben):</span><span class="sxs-lookup"><span data-stu-id="582f2-146">Use the values (that you copied to the text file from the previous steps):</span></span> 

    - <span data-ttu-id="582f2-147">**APISecretKey** – Sie können einen beliebigen Wert als geheimen Schlüssel eingeben.</span><span class="sxs-lookup"><span data-stu-id="582f2-147">**APISecretKey** – You can type any value as the secret.</span></span> <span data-ttu-id="582f2-148">Dieser wird für den Zugriff auf die Connector-Webanwendung in Schritt 7 verwendet.</span><span class="sxs-lookup"><span data-stu-id="582f2-148">This will be used to access the connector web app in Step 7.</span></span>

    - <span data-ttu-id="582f2-149">**StorageAccountConnectionString** – der Verbindungszeichenfolgen-URI, den Sie nach dem Erstellen des Azure-speicherkontos in Schritt 3 kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-149">**StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    - <span data-ttu-id="582f2-150">**Mandanten** Kennung – die Mandanten-ID Ihrer Office 365 Organisation, die Sie nach dem Erstellen der Twitter Connector-app in Azure Active Directory in Schritt 2 kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-150">**tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Twitter connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/TCimage23.png)

4. <span data-ttu-id="582f2-151">Klicken Sie unter **Allgemeine Einstellungen**auf neben dem **immer ein**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="582f2-151">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="582f2-152">Klicken Sie oben auf der Seite auf **Speichern** , um die Anwendungseinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="582f2-152">Click **Save** at the top of the page to save the application settings.</span></span>

   ![](media/TCimage24.png)

5. <span data-ttu-id="582f2-153">Der letzte Schritt besteht darin, den Quellcode der Connector-app in Azure hochzuladen, den Sie in Schritt 1 heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-153">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="582f2-154">Wechseln Sie in einem Webbrowser zu https://<AzureAppResourceName>. SCM.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="582f2-154">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="582f2-155">Wenn beispielsweise der Name Ihrer Azure-App-Ressource (die Sie in Schritt 2 in diesem Abschnitt genannt haben) **twitterconnector**lautet, gehen Sie zu https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="582f2-155">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **twitterconnector**, then you would go to https://twitterconnector.scm.azurewebsites.net/ZipDeployUi.</span></span>

6. <span data-ttu-id="582f2-156">Ziehen Sie das SampleConnector. zip-Menü (das Sie in Schritt 1 heruntergeladen haben) auf diese Seite.</span><span class="sxs-lookup"><span data-stu-id="582f2-156">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="582f2-157">Nachdem die Dateien hochgeladen wurden und die Bereitstellung erfolgreich war, sieht die Seite wie im folgenden Screenshot aus.</span><span class="sxs-lookup"><span data-stu-id="582f2-157">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot.</span></span>

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a><span data-ttu-id="582f2-158">Schritt 5: Erstellen der Twitter-APP</span><span class="sxs-lookup"><span data-stu-id="582f2-158">Step 5: Create the Twitter app</span></span>

1. <span data-ttu-id="582f2-159">Wechseln Sie https://developer.twitter.comzu, melden Sie sich mit den Anmeldeinformationen für das Entwicklerkonto für Ihre Organisation an, und klicken Sie dann auf **apps**.</span><span class="sxs-lookup"><span data-stu-id="582f2-159">Go to https://developer.twitter.com, log in using the credentials for the developer account for your organization, and then click **Apps**.</span></span>

   ![TCimage25-5. png](media/TCimage25-5.png)
2. <span data-ttu-id="582f2-161">Klicken Sie auf **app erstellen**.</span><span class="sxs-lookup"><span data-stu-id="582f2-161">Click **Create an app**.</span></span>
   
   ![](media/TCimage26.png)

3. <span data-ttu-id="582f2-162">Fügen Sie unter **App-Details**Informationen zur Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="582f2-162">Under **App details**, add information about the application.</span></span>

   ![](media/TCimage27.png)

4. <span data-ttu-id="582f2-163">Wählen Sie im Twitter Developer Dashboard die soeben erstellte App aus, und kopieren Sie die angezeigte APP-ID, und speichern Sie Sie in einer Textdatei oder an einem anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-163">On the Twitter developer dashboard, select the app that you just created and copy the App ID that's displayed  and save it to a text file or other storage location.</span></span> <span data-ttu-id="582f2-164">Klicken Sie dann auf **Details**.</span><span class="sxs-lookup"><span data-stu-id="582f2-164">Then click **Details**.</span></span>
   
   ![](media/TCimage28.png)

5. <span data-ttu-id="582f2-165">Kopieren Sie auf der Registerkarte **Schlüssel und Token** unter **Consumer-API-Schlüssel** den geheimen Schlüssel der API, und speichern Sie ihn in einer Textdatei oder an einem anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-165">On the **Keys and tokens** tab, under **Consumer API keys** copy the API secret key and save it to a text file or other storage location.</span></span> <span data-ttu-id="582f2-166">Klicken Sie dann auf **Erstellen** , um ein Zugriffstoken und einen Zugriffstoken Schlüssel zu generieren, und kopieren Sie diese in eine Textdatei oder einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-166">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>
   
   ![](media/TCimage29.png)

   <span data-ttu-id="582f2-167">Klicken Sie dann auf **Erstellen** , um ein Zugriffstoken und einen Zugriffstoken Schlüssel zu generieren, und kopieren Sie diese in eine Textdatei oder einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="582f2-167">Then click **Create** to generate an access token and an access token secret, and copy these to a text file or other storage location.</span></span>

6. <span data-ttu-id="582f2-168">Klicken Sie auf die Registerkarte **Berechtigungen** , und konfigurieren Sie die Berechtigungen wie im folgenden Screenshot dargestellt:</span><span class="sxs-lookup"><span data-stu-id="582f2-168">Click the **Permissions** tab and configure the permissions as shown in the following screenshot:</span></span>

   ![](media/TCimage30.png)

7. <span data-ttu-id="582f2-169">Nachdem Sie die Berechtigungseinstellungen gespeichert haben, klicken Sie auf die Registerkarte **App-Details** , und klicken Sie dann auf **> Bearbeiten Details bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="582f2-169">After you save the permission settings, click the **App details** tab, and then click **Edit > Edit details**.</span></span>

   ![](media/TCimage31.png)

8. <span data-ttu-id="582f2-170">Führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="582f2-170">Do the following tasks:</span></span>

   - <span data-ttu-id="582f2-171">Aktivieren Sie das Kontrollkästchen, damit sich die Connector-App bei Twitter anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="582f2-171">Select the checkbox to allow the connector app to sign in to Twitter.</span></span>
   
   - <span data-ttu-id="582f2-172">Fügen Sie den OAuth-Umleitungs-URI mit dem folgenden Format hinzu: \*\* \<connectorserviceuri>/views/TwitterOAuth\*\*, wobei der Wert von *connectorserviceuri* die Azure-App-Dienst-URL für Ihre Organisation ist. zum Beispiel https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span><span class="sxs-lookup"><span data-stu-id="582f2-172">Add the OAuth redirect Uri using the following format: **\<connectorserviceuri>/Views/TwitterOAuth**, where the value of *connectorserviceuri* is the Azure app service URL for your organization; for example https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.</span></span>

   ![](media/TCimage32.png)

<span data-ttu-id="582f2-173">Die Twitter-Entwickler-App ist jetzt einsatzfähig.</span><span class="sxs-lookup"><span data-stu-id="582f2-173">The Twitter developer app is now ready to use.</span></span>

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="582f2-174">Schritt 6: Konfigurieren der Connector-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="582f2-174">Step 6: Configure the connector web app</span></span> 

1. <span data-ttu-id="582f2-175">Wechseln Sie zu\<https://AzureAppResourceName>. azurewebsites. net (wobei **AzureAppResourceName** der Name Ihrer Azure-App-Ressource ist, die Sie in Schritt 4 benannt haben) Wenn beispielsweise der Name **twitterconnector**lautet https://twitterconnector.azurewebsites.net, wechseln Sie zu.</span><span class="sxs-lookup"><span data-stu-id="582f2-175">Go to https://\<AzureAppResourceName>.azurewebsites.net (where **AzureAppResourceName** is the name of your Azure app resource that you named in Step 4) For example, if the name is **twitterconnector**, go to https://twitterconnector.azurewebsites.net.</span></span> <span data-ttu-id="582f2-176">Die Startseite der APP wird wie im folgenden Screenshot dargestellt.</span><span class="sxs-lookup"><span data-stu-id="582f2-176">The home page of the app will look like the following screenshot.</span></span>

   ![](media/FBCimage41.png)

2. <span data-ttu-id="582f2-177">Klicken Sie auf **Konfigurieren** , um eine Anmeldeseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="582f2-177">Click **Configure** to display a sign in page.</span></span>

   ![](media/FBCimage42.png)

3. <span data-ttu-id="582f2-178">Geben Sie in das Feld Mandanten-ID die Mandanten-ID ein, die Sie in Schritt 2 erhalten haben, oder fügen Sie Sie ein.</span><span class="sxs-lookup"><span data-stu-id="582f2-178">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="582f2-179">Geben Sie in das Feld Kennwort den APISecretKey (den Sie in Schritt 2 erhalten haben) ein, oder fügen Sie ihn ein, und klicken Sie dann auf **Konfigurationseinstellungen festlegen** , um die Seite **Konfigurations Details** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="582f2-179">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

   ![](media/TCimage35.png)

4. <span data-ttu-id="582f2-180">Geben Sie unter **Konfigurations Details**die folgenden Konfigurationseinstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="582f2-180">Under **Configuration Details**, enter the following configuration settings</span></span> 

   - <span data-ttu-id="582f2-181">**Twitter API Key** – die APP-ID für die Twitter-Anwendung, die Sie in Schritt 5 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-181">**Twitter Api Key** - The app ID for the Twitter application that you created in Step 5.</span></span>
   - <span data-ttu-id="582f2-182">**Twitter-API** -geheimer Schlüssel-der geheime API-Schlüssel für die Twitter-Anwendung, die Sie in Schritt 5 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-182">**Twitter Api Secret Key** - The API secret key for the Twitter application that you created in Step 5.</span></span>
   - <span data-ttu-id="582f2-183">**Twitter-Zugriffstoken** : das Zugriffstoken, das Sie in Schritt 5 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-183">**Twitter Access Token** - The access token that you created in Step 5.</span></span>
   - <span data-ttu-id="582f2-184">**Twitter-Zugriffstoken Secret** – der geheime Zugriffstoken-Schlüssel, den Sie in Schritt 5 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-184">**Twitter Access Token Secret** - The access token secret that you created in Step 5.</span></span>
   - <span data-ttu-id="582f2-185">**Aad-Anwendungs-ID** – die Anwendungs-ID für die Azure Active Directory-APP, die Sie in Schritt 2 erstellt haben</span><span class="sxs-lookup"><span data-stu-id="582f2-185">**AAD Application ID** - The application ID for the Azure Active Directory app that you created in Step 2</span></span>
   - <span data-ttu-id="582f2-186">**Aad-Anwendungs Geheimnis** – der Wert für den geheimen Schlüssel "APISecretKey", den Sie in Schritt 4 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="582f2-186">**AAD Application Secret** - The value for the APISecretKey secret that you created in Step 4.</span></span>
   - <span data-ttu-id="582f2-187">**Aad-Anwendungs-URI** – der in Schritt 2 abgerufene Aad-Anwendungs-URI; Beispiel: https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span><span class="sxs-lookup"><span data-stu-id="582f2-187">**AAD Application Uri** - The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   - <span data-ttu-id="582f2-188">**App Insights Instrumentation Key** – lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="582f2-188">**App Insights Instrumentation Key** - Leave this box blank.</span></span>

5. <span data-ttu-id="582f2-189">Klicken Sie auf **Speichern** , um die Verbindungseinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="582f2-189">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a><span data-ttu-id="582f2-190">Schritt 7: Einrichten eines benutzerdefinierten Connectors im Security and Compliance Center</span><span class="sxs-lookup"><span data-stu-id="582f2-190">Step 7: Set up a custom connector in the security and compliance center</span></span>

1.  <span data-ttu-id="582f2-191">Wechseln Sie <https://protection.office.com> zu, und klicken Sie dann auf **Data Governance \> Import \> Archivieren von drittanbieterdaten**.</span><span class="sxs-lookup"><span data-stu-id="582f2-191">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

    ![](media/TCimage36.png)

2. <span data-ttu-id="582f2-192">Klicken Sie auf **Connector hinzufügen** , und klicken Sie dann auf **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="582f2-192">Click **Add a connector** and then click **Twitter**.</span></span>

   ![](media/TCimage37.png)

3. <span data-ttu-id="582f2-193">Geben Sie auf der Seite " **Connector-app hinzufügen** " die folgenden Informationen ein, und klicken Sie dann auf **Connector überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="582f2-193">On the **Add Connector App** page, enter the following information and then click **Validate connector**.</span></span>

    - <span data-ttu-id="582f2-194">Geben Sie im ersten Feld einen Namen für den Connector ein, beispielsweise **Twitter**.</span><span class="sxs-lookup"><span data-stu-id="582f2-194">In the first box, type a name for the connector, such as **Twitter**.</span></span>
    - <span data-ttu-id="582f2-195">Geben Sie im zweiten Feld den Wert des APISecretKey ein, den Sie in Schritt 4 hinzugefügt haben, oder fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="582f2-195">In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    - <span data-ttu-id="582f2-196">Geben Sie im dritten Feld die Azure-App-Dienst-URL ein, oder fügen Sie Sie ein. zum Beispiel **https://twitterconnector.azurewebsites.net**.</span><span class="sxs-lookup"><span data-stu-id="582f2-196">In the third box, type or paste the Azure app service URL; for example **https://twitterconnector.azurewebsites.net**.</span></span>

   <span data-ttu-id="582f2-197">Nachdem der Connector erfolgreich überprüft wurde, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="582f2-197">After the connector is successfully validated, click **Next**.</span></span>

   ![](media/TCimage38.png)

4. <span data-ttu-id="582f2-198">Klicken Sie auf **Anmeldung mit der Connector-App**.</span><span class="sxs-lookup"><span data-stu-id="582f2-198">Click **Login with Connector App**.</span></span>

   ![](media/TCimage39.png)

5. <span data-ttu-id="582f2-199">Geben Sie den APISecretKey erneut ein, oder fügen Sie ihn ein, und klicken Sie dann auf **Login to Connector Service**.</span><span class="sxs-lookup"><span data-stu-id="582f2-199">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/TCimage40.png)


6. <span data-ttu-id="582f2-200">Klicken Sie auf **weiter mit Twitter**.</span><span class="sxs-lookup"><span data-stu-id="582f2-200">Click **Continue with Twitter**.</span></span>

7. <span data-ttu-id="582f2-201">Melden Sie sich auf der Twitter-Anmeldeseite mit den Anmeldeinformationen für das Konto für das Twitter-Konto Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="582f2-201">On the Twitter sign in page, sign in using the credentials for the account for your organization’s Twitter account.</span></span>

   ![](media/TCimage42.png)

   <span data-ttu-id="582f2-202">Nachdem Sie sich angemeldet haben, wird auf der Twitter-Seite die folgende Meldung angezeigt: "Twitter Connector-Auftrag erfolgreich eingerichtet."</span><span class="sxs-lookup"><span data-stu-id="582f2-202">After you sign in, the Twitter page will display the following message, "Twitter Connector Job Successfully set up."</span></span>

8. <span data-ttu-id="582f2-203">Klicken Sie auf **Fertig stellen** , um die Einrichtung des Twitter-Konnektors abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="582f2-203">Click **Finish** to complete setting up the Twitter connector.</span></span>

9. <span data-ttu-id="582f2-204">Auf der Seite **Filter festlegen** können Sie einen Filter anwenden, um Elemente zu importieren (und archivieren), die ein bestimmtes Alter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="582f2-204">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="582f2-205">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="582f2-205">Click **Next**.</span></span>

   ![](media/TCimage44.png)

10. <span data-ttu-id="582f2-206">Wählen Sie auf der Seite **Speicherkonto festlegen** das Office 365 Postfach aus, in das die Twitter-Elemente importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="582f2-206">On the **Set Storage Account** page, select the Office 365 mailbox that the Twitter items will be imported to.</span></span>

    ![](media/TCimage45.png)

11. <span data-ttu-id="582f2-207">Überprüfen Sie Ihre Einstellungen, und klicken Sie dann auf **Fertig stellen** , um das Connector-Setup im Security & Compliance Center abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="582f2-207">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. <span data-ttu-id="582f2-208">Wechseln Sie zur Seite Archivieren von **drittanbieterdaten** , um den Fortschritt des Importvorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="582f2-208">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/TCimage48.png)

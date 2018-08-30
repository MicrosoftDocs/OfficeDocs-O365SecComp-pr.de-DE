---
title: Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Erfahren Sie, wie Kundenschlüssel für Office 365 für Exchange Online, Skype für Unternehmen, SharePoint Online und OneDrive für Unternehmen einzurichten. Mit Kundenschlüssel Verschlüsselungsschlüssel Ihrer Organisation steuern und konfigurieren Sie anschließend Office 365, um diese verwenden, um die Daten im Ruhezustand in Microsoft Rechenzentren zu verschlüsseln.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559230"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="503e4-104">Kontrolle über Ihre Daten in Office 365 mit Kunden-Taste</span><span class="sxs-lookup"><span data-stu-id="503e4-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="503e4-p102">Mit Kundenschlüssel Verschlüsselungsschlüssel Ihrer Organisation steuern und konfigurieren Sie anschließend Office 365, um diese verwenden, um die Daten im Ruhezustand in Microsoft Rechenzentren zu verschlüsseln. Daten im Ruhezustand enthält Daten aus Exchange Online und Skype für Unternehmen, die in Dateien, die in SharePoint Online gespeichert sind und Postfächer gespeichert sind und OneDrive für Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="503e4-p103">Sie müssen die Azure einrichten, bevor Sie Kundenschlüssel für Office 365 verwenden können. In diesem Thema werden die Schritte zum Erstellen und konfigurieren die erforderlichen Ressourcen Azure benötigten Schritte beschrieben und dann werden die Schritte zum Einrichten von Kundenschlüssel in Office 365. Nachdem Sie Azure Setup abgeschlossen haben, bestimmen Sie, welche Richtlinie und daher, welche Schlüssel, um Postfächer und Dateien in Ihrer Organisation zuweisen. Postfächer und die Dateien für die Sie eine Richtlinie zuweisen nicht verwendet Verschlüsselungsrichtlinien, die von Microsoft verwaltet und gesteuert. Weitere Informationen zu Kunden-Taste oder eine allgemeine Übersicht finden Sie unter den [Kunden Product Key für die Office 365 – häufig gestellte Fragen](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="503e4-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="503e4-p104">Es wird dringend empfohlen, dass Sie den empfohlenen Vorgehensweisen in diesem Thema beschrieben. Diese werden als **Tipp** und **Wichtig**heraus aufgerufen. Kunden-Taste können Sie über Root Verschlüsselungsschlüssel, deren Bereich so groß wie die gesamte Organisation sein kann. Dies bedeutet, dass gemachte mit hierüber eine umfassende auswirken und können im Dienst unterbrechen oder unwiderruflich Verlust der Daten.</span><span class="sxs-lookup"><span data-stu-id="503e4-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="503e4-116">Vor dem Einrichten von Kunden-Taste</span><span class="sxs-lookup"><span data-stu-id="503e4-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="503e4-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-117"></span></span>

<span data-ttu-id="503e4-p105">Bevor Sie beginnen, müssen Sie unbedingt, dass Sie die entsprechenden Lizenzierung für Ihre Organisation verfügen. Kundenschlüssel in Office 365 wird in Office 365 E5 oder die erweiterte Compliance-SKU angeboten.</span><span class="sxs-lookup"><span data-stu-id="503e4-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="503e4-p106">Klicken Sie dann, sollten Sie zum Verständnis der Konzepte und die Verfahren in diesem Thema die [Azure Schlüssel Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) Dokumentation überprüfen. Darüber hinaus sind mit den in Azure, beispielsweise [Mandanten](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)verwendeten Begriffen vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="503e4-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="503e4-122">Senden Sie Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com, um Feedback auf Kundenschlüssel, einschließlich der Dokumentation zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="503e4-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="503e4-123">Übersicht über das Einrichten von Kundenschlüssel für Office 365</span><span class="sxs-lookup"><span data-stu-id="503e4-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="503e4-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-124"></span></span>

<span data-ttu-id="503e4-p107">Zum Einrichten der Customer-Schlüssel werden diese Aufgaben ausgeführt werden: Der Rest dieses Themas finden Sie ausführliche Anweisungen für jeden Vorgang oder Links, um weitere Informationen für jeden Schritt im Prozess.</span><span class="sxs-lookup"><span data-stu-id="503e4-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="503e4-127">**In Azure und Microsoft schnelle:**</span><span class="sxs-lookup"><span data-stu-id="503e4-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="503e4-p108">Führen Sie die meisten dieser Aufgaben von Azure PowerShell eine Remoteverbindung herstellen. Die besten Ergebnisse erzielen, verwenden Sie Version 4.4.0 oder höher von Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="503e4-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="503e4-130">Erstellen Sie zwei neue Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="503e4-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="503e4-131">Registrieren der Azure-Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden</span><span class="sxs-lookup"><span data-stu-id="503e4-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="503e4-132">Registrierung kann bis zu fünf Business Tage dauern.</span><span class="sxs-lookup"><span data-stu-id="503e4-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="503e4-133">Übermitteln einer Anforderung an Kundenschlüssel für Office 365 aktivieren</span><span class="sxs-lookup"><span data-stu-id="503e4-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="503e4-p109">Nachdem Sie die zwei neue Azure Abonnements erstellt haben, müssen Sie senden Sie die entsprechende Kundenschlüssel Angebot Anforderung anhand von einem Webformular, die im Microsoft FastTrack Portal gehostet wird. Das Team der schnelle bieten nicht mit Kundenschlüssel Unterstützung. Office einfach verwendet das schnelle Portal, die Sie zum Senden des Formulars und helfen, die relevante Angebote für Kundenschlüssel verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="503e4-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key.</span></span>
  
<span data-ttu-id="503e4-p110">Nachdem Sie ein Kundenschlüssel Angebot gesendet haben, wird Microsoft prüft Ihre Anforderung und benachrichtigt, wenn Sie mit dem Rest der Setup-Aufgaben fortfahren können. Dieser Vorgang kann bis zu fünf Business Tage dauern.</span><span class="sxs-lookup"><span data-stu-id="503e4-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="503e4-139">Erstellen Sie eine Premium Azure Schlüssel Vault in jedes Abonnement</span><span class="sxs-lookup"><span data-stu-id="503e4-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="503e4-140">Zuweisen von Berechtigungen zu jeder wichtige vault</span><span class="sxs-lookup"><span data-stu-id="503e4-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="503e4-141">Aktivieren, und klicken Sie dann auf Ihre wichtigsten Depots vorläufiges Löschen bestätigen</span><span class="sxs-lookup"><span data-stu-id="503e4-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="503e4-142">Hinzufügen eines Schlüssels zur jeder wichtige Vault entweder durch Erstellen oder Importieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="503e4-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="503e4-143">Überprüfen der Wiederherstellung Ihren Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="503e4-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="503e4-144">Backup Azure wichtige Vault</span><span class="sxs-lookup"><span data-stu-id="503e4-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="503e4-145">Überprüfen der Azure-Taste Vault-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="503e4-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="503e4-146">Den URI für jeden Schlüssel Azure Schlüssel Vault zu erhalten</span><span class="sxs-lookup"><span data-stu-id="503e4-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="503e4-147">**In Office 365:**</span><span class="sxs-lookup"><span data-stu-id="503e4-147">**In Office 365:**</span></span>
  
<span data-ttu-id="503e4-148">Exchange Online und Skype für Unternehmen:</span><span class="sxs-lookup"><span data-stu-id="503e4-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="503e4-149">Erstellen einer Daten-Verschlüsselung-Richtlinie (DEP) für die Verwendung mit Exchange Online und Skype für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="503e4-150">Zuweisen einer Datenausführungsverhinderung an ein Postfach</span><span class="sxs-lookup"><span data-stu-id="503e4-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="503e4-151">Überprüfen der Postfach-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="503e4-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="503e4-152">SharePoint Online und OneDrive für Unternehmen:</span><span class="sxs-lookup"><span data-stu-id="503e4-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="503e4-153">Erstellen Sie eine Daten-Verschlüsselung-Richtlinie (DEP) für jeden SharePoint Online und OneDrive for Business geo</span><span class="sxs-lookup"><span data-stu-id="503e4-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="503e4-154">Überprüfen Sie die Verschlüsselung der Gruppe Websites, Teamwebsites und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="503e4-155">Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft FastTrack für Kunden-Taste</span><span class="sxs-lookup"><span data-stu-id="503e4-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="503e4-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-156"></span></span>

<span data-ttu-id="503e4-p111">Führen Sie diese Aufgaben in Azure Schlüssel Vault, um Kundenschlüssel für Office 365 einzurichten. Sie müssen diese Schritte unabhängig davon, ob Sie Kundenschlüssel für Exchange Online und Skype für Unternehmen oder SharePoint Online und OneDrive für Unternehmen oder für alle unterstützten Dienste in Office 365 einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="503e4-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="503e4-159">Erstellen Sie zwei neue Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="503e4-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="503e4-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-160"></span></span>

<span data-ttu-id="503e4-p112">Zwei Azure-Abonnements sind erforderlich für Kunden-Taste. Als bewährte Methode empfiehlt es sich, dass Sie neue Azure Abonnements für die Verwendung mit Kundenschlüssel erstellen. Azure-Taste Vault Schlüssel können nur für Applikationen in derselben mandantenorganisation Azure Active Directory (AAD) autorisiert werden, müssen Sie die neue Abonnements mit den gleichen Azure AD-Mandanten mit Office 365-Organisation verwendet werden, in dem die Einzahlgn zugewiesen werden erstellen. Beispielsweise verwenden Ihr Konto arbeiten oder Schule, die globalen in Office 365-Organisation Administratorrechten. Ausführliche Schritte finden Sie unter [Registrieren für Azure als einer Organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="503e4-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="503e4-p113">Kundenschlüssel erfordert zwei Schlüssel für jede Richtlinie für Daten-Verschlüsselung (DEP). Um dies zu erreichen, müssen Sie zwei Azure Abonnements erstellen. Als bewährte Methode empfiehlt es sich, dass Sie separate Mitglieder Ihrer Organisation konfigurieren Sie einen Schlüssel in jedem Abonnement verfügen. Darüber hinaus sollte nur diese Azure Abonnements verwendet werden, Verschlüsselungsschlüssel für Office 365 verwalten. Dies schützt Ihre Organisation Fall, dass eine Ihrer Operatoren versehentlich, absichtlich oder böswilligen Benutzern löscht oder andernfalls mismanages die Schlüssel für die sie verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="503e4-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="503e4-p114">Es wird empfohlen, dass Sie neue Azure Abonnements einrichten, die ausschließlich für die Verwaltung von Azure Schlüssel Vault Ressourcen für die Verwendung mit Kundenschlüssel verwendet werden. Es gibt keine praktische Obergrenze für die Anzahl der Azure-Abonnements, die Sie für Ihre Organisation erstellen können. Diese bewährten Methoden befolgen minimieren die Auswirkungen der Benutzerfehler und gleichzeitig die von Kundenschlüssel verwendeten Ressourcen verwalten.</span><span class="sxs-lookup"><span data-stu-id="503e4-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="503e4-174">Übermitteln einer Anforderung an Kundenschlüssel für Office 365 aktivieren</span><span class="sxs-lookup"><span data-stu-id="503e4-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="503e4-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-175"></span></span>

<span data-ttu-id="503e4-p115">Nachdem Sie die Azure Schritte abgeschlossen haben, müssen Sie eine Anforderung Angebot in [Microsoft schnelle Portal](https://fasttrack.microsoft.com/)übermitteln. Nachdem Sie eine Anforderung über die schnelle Webportal gesendet haben, überprüft Microsoft die Azure-Taste Vault Konfiguration Daten und von Ihnen eingegebenen Informationen. Die Optionen, die in der Form Angebot bezüglich der autorisierten Finanzabteilung Ihrer Organisation ist erforderlich für den Abschluss der Registrierung Customer-Taste. Der Finanzabteilung Ihrer Organisation, die Sie im Formular auswählen werden zum Sicherstellen der Authentizität jeder Anforderung von widerrufen, und löschen Sie alle Schlüssel mit einer Kunden-Schlüssel datenverschlüsselung Richtlinie verwendet werden. Sie müssen diesen Schritt einmal führen Sie zum Aktivieren von Kundenschlüssel für Exchange Online und Skype für Business Abdeckung und ein zweites Mal Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="503e4-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="503e4-181">Führen Sie diese Schritte, um ein Angebot Kunden-Schlüssels zu übermitteln:</span><span class="sxs-lookup"><span data-stu-id="503e4-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="503e4-182">Melden Sie sich mit einem arbeiten oder Schule Konto mit globalen Administratorberechtigungen in Office 365-Organisation, [Microsoft schnelle Portal](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="503e4-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="503e4-183">Sobald Sie angemeldet sind, navigieren Sie zu dem **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="503e4-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="503e4-184">Wählen Sie **bietet**, und überprüfen Sie die Liste der aktuellen Angebote.</span><span class="sxs-lookup"><span data-stu-id="503e4-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="503e4-185">Wählen Sie **Hier erfahren Sie mehr** , für das Angebot, das für Sie gilt:</span><span class="sxs-lookup"><span data-stu-id="503e4-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="503e4-186">**Exchange Online und Skype für Unternehmen:** **Hier erfahren Sie mehr** wählen Sie auf das Angebot **Customer Product Key für Exchange aus** .</span><span class="sxs-lookup"><span data-stu-id="503e4-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="503e4-187">**SharePoint Online und OneDrive für Unternehmen:** **Hier erfahren Sie mehr** auf das Angebot **Customer Product Key für die SharePoint- und OneDrive für Unternehmen** gewählten.</span><span class="sxs-lookup"><span data-stu-id="503e4-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="503e4-188">Wählen Sie auf der Seite **Details bieten** **Anfordern erstellen**.</span><span class="sxs-lookup"><span data-stu-id="503e4-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="503e4-p116">Füllen Sie alle anwendbaren Details und angeforderten Informationen auf dem Angebot Formular. Beachten Sie insbesondere, Ihre Auswahl für die Führungskräfte Ihrer Organisation genehmigen dauerhaft entfernt und nicht rückgängig gemacht werden beim Löschen des Verschlüsselungsschlüssel und Daten autorisiert werden soll. Wenn Sie das Formular abgeschlossen haben, wählen Sie **Submit**.</span><span class="sxs-lookup"><span data-stu-id="503e4-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="503e4-192">Dieser Vorgang kann bis zu fünf Arbeitstagen sobald Microsoft Ihrer Anfrage benachrichtigt wurde dauern.</span><span class="sxs-lookup"><span data-stu-id="503e4-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="503e4-193">Gehen Sie obligatorische Aufbewahrung Period weiter unten im Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="503e4-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="503e4-194">Registrieren der Azure-Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden</span><span class="sxs-lookup"><span data-stu-id="503e4-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="503e4-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-195"></span></span>

<span data-ttu-id="503e4-p117">Die Daten vorübergehende oder endgültig zum Verlust von Verschlüsselungsschlüsseln Stamm kann sehr störende oder sogar katastrophale, des Diensts und Datenverlust führen kann. Aus diesem Grund erfordern die mit Kundenschlüssel verwendeten Ressourcen verstärkte Sicherheit. Die Azure Ressourcen, die mit Kundenschlüssel verwendet werden, bieten Schutzmechanismen über die Standardkonfiguration. Azure-Abonnements können markiert oder in eine Möglichkeit, die sofortige und unwiderruflich Abbruch verhindern registriert werden. Dies wird als registrieren für eine obligatorische Aufbewahrungsdauer bezeichnet. Die erforderlichen Schritte zum Registrieren von Azure-Abonnements für eine obligatorische Aufbewahrungsdauer erfordern für die Zusammenarbeit mit dem Office 365-Team. Dieser Vorgang kann bis zu fünf Business Tage dauern. Bisher war dies manchmal als "Nicht Abbrechen" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="503e4-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="503e4-204">Vor der Kontaktaufnahme mit Office 365-Team, müssen Sie die folgenden Schritte für jede Azure-Abonnement ausführen, die Sie mit Kundenschlüssel verwenden:</span><span class="sxs-lookup"><span data-stu-id="503e4-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="503e4-p118">Melden Sie sich bei Ihrer Azure-Abonnement mit Azure PowerShell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="503e4-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="503e4-207">Führen Sie das Cmdlet Register-AzureRmProviderFeature zum Registrieren Ihrer Abonnements, um eine obligatorische Aufbewahrungsdauer verwenden.</span><span class="sxs-lookup"><span data-stu-id="503e4-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="503e4-p119">Wenden Sie sich an Microsoft, um den Vorgang abgeschlossen haben. Wenden Sie sich an [spock@microsoft.com](mailto:spock@microsoft.com)für SharePoint und OneDrive for Business-Team. Wenden Sie sich an [exock@microsoft.com](mailto:exock@microsoft.com)für Exchange Online und Skype für Unternehmen. Service Level Agreement (SLA) für Abschluss dieses Vorgangs fünf Arbeitstagen ist nach Microsoft benachrichtigt (überprüft, und) Sie haben eine obligatorische Aufbewahrungsdauer verwenden, um Ihre Abonnements registriert. Fügen Sie die folgenden Ihre e-Mail-Adresse:</span><span class="sxs-lookup"><span data-stu-id="503e4-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="503e4-213">**Betreff**: Customer Product Key für die \< *vollqualifizierten Domänennamen Ihres Mandanten*\></span><span class="sxs-lookup"><span data-stu-id="503e4-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="503e4-214">**Body**: Abonnement-IDs für die die obligatorische Aufbewahrung Periode beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="503e4-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="503e4-215">Nachdem Sie von Microsoft benachrichtigt, dass die Registrierung abgeschlossen ist, überprüfen Sie den Status Ihrer Registrierung durch Ausführen von mit dem Cmdlet Get-AzureRmProviderFeature wie folgt:</span><span class="sxs-lookup"><span data-stu-id="503e4-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="503e4-216">Führen Sie nachdem Sie sichergestellt haben, dass die **Registrierung State** -Eigenschaft aus dem Cmdlet Get-AzureRmProviderFeature **Registered**Wert zurückgegeben den folgenden Befehl aus, um den Vorgang abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="503e4-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="503e4-217">Erstellen Sie eine Premium Azure Schlüssel Vault in jedes Abonnement</span><span class="sxs-lookup"><span data-stu-id="503e4-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="503e4-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-218"></span></span>

<span data-ttu-id="503e4-219">Die Schritte zum Erstellen einer wichtige Vault sind in die [Erste Schritte mit Azure Schlüssel Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), dokumentiert, die führt Sie durch das Installieren und Starten von Azure PowerShell, eine Verbindung mit Ihrem Azure-Abonnement, erstellen eine Ressourcengruppe und erstellen eine wichtige Vault, in dem Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="503e4-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="503e4-p120">Wenn Sie einen Schlüssel Vault erstellen, müssen Sie eine SKU auswählen: Standard oder Premium. Der Standard-SKU kann Azure Schlüssel Vault Schlüssel mit Software geschützt werden - ist kein Schutz (Hardware Security Module, HSM) Schlüssel - und der Premium-SKU ermöglicht die Verwendung von HSMs für den Schutz der Schlüssel Vault Schlüssel. Kundenschlüssel akzeptiert wichtige Depots, die entweder SKU verwenden, obwohl Microsoft empfiehlt, dass Sie nur die Premium-SKU verwenden. Die Kosten der Vorgänge mit Schlüsseln des Typs entspricht, damit der einzige Unterschied Kosten die Kosten pro Monat für jeden Schlüssel HSM geschützt ist. Einzelheiten finden Sie in der [Schlüssel Vault Preise](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="503e4-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="503e4-225">Verwenden Sie die wichtigsten Depots Premium SKU und Schlüssel HSM-geschützten für Produktionsdaten und nur verwenden Sie wichtige Depots Standard SKU und Schlüssel für Test- und Validierung.</span><span class="sxs-lookup"><span data-stu-id="503e4-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="503e4-p121">Erstellen Sie für jeden Office 365-Dienst mit dem Sie Kundenschlüssel verwenden möchten eine wichtige Vault in jeder der beiden Azure Abonnements aufgelistet, die Sie erstellt haben. Für Exchange Online und Skype für Geschäftskunden nur und SharePoint Online und OneDrive für Unternehmen nur, beispielsweise erstellen Sie nur ein paar Depots. Um Kundenschlüssel für Exchange Online und SharePoint Online zu aktivieren, erstellen Sie zwei wichtige Depots-Paare.</span><span class="sxs-lookup"><span data-stu-id="503e4-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="503e4-p122">Verwenden Sie eine Namenskonvention für wichtige Depots, die die beabsichtigte Verwendung von der Datenausführungsverhinderung widerspiegelt, die Sie den Depots zuordnen möchten. Finden Sie im Abschnitt Best Practices unter naming Convention Recommendations.</span><span class="sxs-lookup"><span data-stu-id="503e4-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="503e4-p123">Erstellen einer separaten, kombinierte Depots für jede Data Encryption-Richtlinie. Für Exchange Online wird der Bereich einer Daten-Verschlüsselung Richtlinie von Ihnen ausgewählt, wenn Sie die Richtlinie Postfach zuweisen. Ein Postfach kann nur eine Richtlinie zugewiesen haben, und Sie können bis zu 50 Richtlinien erstellen. Für SharePoint Online ist der Bereich einer Richtlinie alle Daten in einer Organisation in einem geografischen Standort oder Geo.</span><span class="sxs-lookup"><span data-stu-id="503e4-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="503e4-p124">Die Erstellung von wichtigen Depots erfordert auch die Erstellung von Azure Ressourcengruppen, da wichtige Depots benötigen die Speicherkapazität (obwohl sehr kleine) und Schlüssel Vault Protokollierung ist aktiviert, auch gespeicherte Daten generiert. Als bewährte Methode empfiehlt Microsoft die Verwendung von separater Administratoren zum Verwalten von einzelnen Ressourcengruppen mit der Verwaltung mit dem Satz von Administratoren, die alle zugehörige Kundenschlüssel Ressourcen verwalten werden ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="503e4-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="503e4-p125">Um die Verfügbarkeit zu maximieren, sollte Ihre wichtigsten Depots Regionen ungefähr in Office 365-Dienst sein. Wenn Ihre Exchange Online-Organisation in Nordamerika ist, platzieren Sie Ihre wichtigsten Depots in Nordamerika fest. Ist Ihre Exchange Online-Organisation in Europa, setzen Sie Ihre wichtigsten Depots in Europa.</span><span class="sxs-lookup"><span data-stu-id="503e4-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="503e4-p126">Verwenden Sie ein gemeinsames Präfix für wichtige Depots und umfassen eine Abkürzung für die Verwendung und Bereich der wichtigsten Vault und Schlüssel (z. B., für der Contoso-SharePoint-Dienst, in dem die Depots sich in Nordamerika, eine mögliche Paar von Namen befinden, Contoso-O365SP-NA-VaultA1 ist und Contoso-O365SP-NA-VaultA2. Vault Namen sind global eindeutigen Zeichenfolgen in Azure, müssen Sie möglicherweise die Namen der gewünschten Varianten versuchen, für den Fall, dass die Namen die gewünschten bereits durch andere Azure Kunden beansprucht werden. Ab Juli 2017 können Vault Namen geändert werden, damit eine bewährte Methode besteht darin einen schriftlichen Plan für die Installation und verwenden Sie eine weitere Person um zu überprüfen, ob der Plan ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="503e4-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="503e4-p127">Erstellen Sie wenn möglich, Ihre Depots Regionen nicht kombiniert. Kombinierte Azure Regionen stellen hohen Verfügbarkeit über Fehlerdomänen Service bereit. Regionale-Paare können daher als Sicherung des jeweils anderen Region betrachtet werden. Dies bedeutet, dass eine Azure-Ressource, die in einer Region platziert wird automatisch Fehlertoleranz durch die kombinierte Region Zustand wechselt. Aus diesem Grund auswählen von Regionen für zwei Depots verwendet in einer Datenausführungsverhinderung, in dem der Bereiche gekoppelten bedeutet, dass nur zwei Regionen aus der Verfügbarkeit insgesamt verwendet wird. Die meisten Regionen müssen nur zwei Regionen aus, damit diese noch nicht möglich, nicht gepaart Regionen ausgewählt ist. Wenn möglich, wählen Sie zwei nicht gepaart Regionen für die zwei Depots mit einer Datenausführungsverhinderung verwendet Profitieren von insgesamt vier Regionen der Verfügbarkeit. Weitere Informationen finden Sie unter [Business Continuity und Disaster Recovery (BCDR): Azure gepaart Regionen](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) für eine aktuelle Liste der regionalen-Paare.</span><span class="sxs-lookup"><span data-stu-id="503e4-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="503e4-252">Zuweisen von Berechtigungen zu jeder wichtige vault</span><span class="sxs-lookup"><span data-stu-id="503e4-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="503e4-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-253"></span></span>

<span data-ttu-id="503e4-p128">Für jeden Schlüssel Vault müssen Sie drei separaten Satz von Berechtigungen für Kundenschlüssel, je nach der Implementierung definieren. Beispielsweise müssen Sie eine Reihe von Berechtigungen für jede der folgenden definieren:</span><span class="sxs-lookup"><span data-stu-id="503e4-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="503e4-p129">**Taste Vault Administratoren** , die über die alltägliche Verwaltung von Ihrer wichtigsten Vault für Ihre Organisation ausführen. Diese Aufgaben umfassen Backup, erstellen, abrufen, importieren, auflisten und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="503e4-p130">Der Satz von Berechtigungen, die wichtige Vault Administratoren zugewiesen umfasst nicht die Berechtigung, um den Schlüssel zu löschen. Dies ist beabsichtigt und eine wichtige Praxis. Löschen von Verschlüsselungsschlüssel in der Regel erfolgt nicht seit wie folgt so dauerhaft Daten verloren gehen. Es empfiehlt sich gewähren Sie keine diese Berechtigung wichtige Vault Administratoren standardmäßig. Stattdessen reservieren Sie dies für wichtige Vault Mitwirkende und nur an einen Administrator für eine einzelne kurzfristig weisen Sie zu, nachdem eine umfassende Kenntnis der folgen verstanden wird.</span><span class="sxs-lookup"><span data-stu-id="503e4-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="503e4-p131">Wenn diese Berechtigungen zu einem Benutzer in Office 365-Organisation zuweisen möchten, melden Sie sich bei Ihrer Azure-Abonnement mit Azure PowerShell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="503e4-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="503e4-265">Führen Sie das Set-AzureRmKeyVaultAccessPolicy-Cmdlet, um die erforderlichen Berechtigungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="503e4-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="503e4-266">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="503e4-p132">**Taste Vault Autoren** , die Berechtigungen für die Azure Schlüssel Vault selbst ändern können. Sie müssen diese Berechtigungen ändern, wie Mitarbeiter lassen oder teilnehmen an Ihr Team oder in der sehr seltene Fall, dass der Schlüssel vault Administratoren bewusst benötigen die Berechtigung zum Löschen oder Wiederherstellen eines Schlüssels. Diese Reihe von wichtigen Vault Mitwirkende muss die Rolle **Mitwirkender** auf Ihre wichtigsten Vault erteilt werden. Sie können diese Rolle zuweisen, mithilfe von Azure Ressourcen-Manager. Ausführliche Schritte finden Sie unter [Use Role-Based Access Control zum Verwalten des Zugriffs auf Ihre Ressourcen Azure-Abonnement](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Der Administrator, der ein Abonnement erstellt hat dieses Zugriff implizit, sowie die Möglichkeit, anderen Administratoren zur Rolle Mitwirkender zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="503e4-p133">Wenn Sie beabsichtigen, Kundenschlüssel mit Exchange Online und Skype für Unternehmen verwenden, müssen Sie zu Office 365, verwenden Sie die wichtigsten Vault im Auftrag von Exchange Online und Skype für Business Berechtigung erteilen. Wenn Sie beabsichtigen, Kundenschlüssel mit SharePoint Online und OneDrive für Unternehmen verwenden, müssen Sie ebenso Berechtigung für die Office 365, verwenden Sie die wichtigsten Vault für SharePoint Online und OneDrive für Unternehmen hinzugefügt. Um zu Office 365 die Berechtigung erteilen, führen Sie das Cmdlet " **Set-AzureRmKeyVaultAccessPolicy** " mithilfe der folgenden Syntax aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="503e4-276">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="503e4-276">Where:</span></span>
    
  - <span data-ttu-id="503e4-277">*Vaultname* ist der Name der der wichtigsten Vault, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="503e4-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="503e4-278">Ersetzen Sie für Exchange Online und Skype für Unternehmen, *Office 365 AppID* mit`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="503e4-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="503e4-279">Ersetzen Sie *Office 365 AppID* mit für SharePoint Online und OneDrive für Unternehmen`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="503e4-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="503e4-280">Beispiel: Festlegen von Berechtigungen für Exchange Online und Skype für Unternehmen:</span><span class="sxs-lookup"><span data-stu-id="503e4-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="503e4-281">Beispiel: Festlegen von Berechtigungen für SharePoint Online und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="503e4-282">Aktivieren, und klicken Sie dann auf Ihre wichtigsten Depots vorläufiges Löschen bestätigen</span><span class="sxs-lookup"><span data-stu-id="503e4-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="503e4-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-283"></span></span>

<span data-ttu-id="503e4-p134">Wenn Sie Ihren Schlüsseln schnell wiederherstellen können, sind Sie mit weitaus geringerer Wahrscheinlichkeit einer längeren Dienstausfall aufgrund von böswilligen Benutzern oder versehentlich gelöschte Schlüssel-Umgebung zu bieten. Sie müssen aktivieren diese Konfiguration, bezeichnet als Soft löschen, bevor Sie Ihren Schlüsseln mit Kundenschlüssel verwenden können. Weiche löschen aktivieren, können Sie innerhalb des Löschens 90 Tage Schlüsseln oder Depots wiederherstellen, ohne sie aus Sicherung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="503e4-287">Um weiche löschen auf Ihre wichtigsten Depots zu aktivieren, führen Sie diese Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="503e4-p135">Melden Sie sich bei Ihrer Azure-Abonnement mit Windows Powershell. Anweisungen finden Sie unter [Melden Sie sich mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="503e4-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="503e4-p136">Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . In diesem Beispiel ist *Vaultname* der Name der dem Schlüssel Vault für das Sie vorläufiges löschen aktivieren:</span><span class="sxs-lookup"><span data-stu-id="503e4-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="503e4-p137">Vergewissern Sie sich, dass vorläufiges löschen für die wichtigsten Vault durch Ausführen des Cmdlets **Get-AzureRmKeyVault** konfiguriert ist. Wenn vorläufiges löschen für die wichtigsten Vault ordnungsgemäß konfiguriert ist, löschen Sie dann die vorläufig aktiviert? -Eigenschaft gibt den Wert **True**zurück:</span><span class="sxs-lookup"><span data-stu-id="503e4-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="503e4-294">Hinzufügen eines Schlüssels zur jeder wichtige Vault entweder durch Erstellen oder Importieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="503e4-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="503e4-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-295"></span></span>

<span data-ttu-id="503e4-p138">Es gibt zwei Methoden, um ein Azure Schlüssel Vault Schlüssel hinzugefügt. Erstellen Sie einen Schlüssel direkt im Schlüssel Vault, oder Sie können einen Schlüssel importieren. Erstellen einen Schlüssel direkt im Schlüssel Vault ist die weniger kompliziert-Methode Importieren eines Schlüssels bietet eine vollständige Kontrolle über wie der Schlüssel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="503e4-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="503e4-298">Um einen Schlüssel direkt in Ihre wichtigsten Vault erstellen möchten, führen Sie das Cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="503e4-299">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="503e4-299">Where:</span></span>
  
-  <span data-ttu-id="503e4-300">*Vaultname* ist der Name der der wichtigsten Vault, in dem Sie den Schlüssel erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="503e4-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="503e4-301">*Schlüsselname* ist der Name des neuen Schlüssels erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="503e4-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="503e4-p139">Nennen Sie die Tasten mit einer ähnlichen Benennungskonvention für wichtige Depots wie oben beschrieben. Auf diese Weise wird in den Tools, mit die nur der Name des Schlüssels angezeigt, die Zeichenfolge Self beschreiben.</span><span class="sxs-lookup"><span data-stu-id="503e4-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="503e4-304">Wenn Sie beabsichtigen, den Schlüssel mit einer HSM zu schützen, stellen Sie sicher, dass Sie geben Sie als Wert des Parameters _Ziel_ **HSM** anderenfalls **Software**angeben.</span><span class="sxs-lookup"><span data-stu-id="503e4-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="503e4-305">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="503e4-306">Um einen Schlüssel direkt in Ihre wichtigsten Vault importieren, müssen Sie eine Thales nShield Hardware Security Module haben.</span><span class="sxs-lookup"><span data-stu-id="503e4-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="503e4-307">Manche Organisationen bevorzugen diese Vorgehensweise zum Einrichten der Herkunft der ihre Schlüssel, und diese Methode bietet außerdem die folgenden:</span><span class="sxs-lookup"><span data-stu-id="503e4-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="503e4-308">Verwendet für den Import Toolset umfasst Bescheinigung Thales, dass der Schlüssel Exchange Schlüssel (KEK), die zum Verschlüsseln, die Sie generieren des Schlüssels verwendet wird nicht exportierbar ist und innerhalb einer echten HSM, die von Thales hergestellt wurde generiert.</span><span class="sxs-lookup"><span data-stu-id="503e4-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="503e4-p140">Das Toolset enthält Bescheinigung Thales, dass die Azure Schlüssel Vault Security World auch auf einer echten HSM von Thales hergestellt generiert wurde. Diese Bescheinigung erweist sich als für Sie, dass Microsoft genuine Thales Hardware auch verwendet.</span><span class="sxs-lookup"><span data-stu-id="503e4-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="503e4-p141">Wenden Sie sich die Sicherheitsgruppe zu ermitteln, ob die oben genannten Datenschutzpolitik erforderlich sind. Ausführliche Schritte zum Erstellen einer wichtige lokalen und in Ihrer wichtigsten Vault importieren finden Sie unter [generieren und HSM-geschützten Schlüssel für Azure Schlüssel Vault übertragen](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Verwenden Sie die Azure Anweisungen, um einen Schlüssel in jeder wichtige Vault zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="503e4-314">Überprüfen der Wiederherstellung Ihren Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="503e4-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="503e4-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-315"></span></span>

<span data-ttu-id="503e4-p142">Office 365 erfordert, dass das Abonnement Azure Schlüssel Vault auf kein Abbrechen festgelegt ist und dass der Schlüssel von Kundenschlüssel verwendet vorläufiges Löschen aktiviert ist. Sie können dies überprüfen, anhand der Ebene der Wiederherstellung auf Ihren Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="503e4-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="503e4-318">Führen Sie das Cmdlet Get-AzureKeyVaultKey wie folgt aus, um die Wiederherstellung Ebene eines Schlüssels, in Azure PowerShell zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="503e4-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="503e4-319">Wenn die _Wiederherstellung Level_ -Eigenschaft einen anderen Wert als Wert **Wiederherstellbaren + ProtectedSubscription**zurückgibt, müssen Sie überprüfen Sie in diesem Thema und stellen Sie sicher, dass Sie alle Schritte, um das Abonnement in der Liste kein Abbrechen platzieren befolgt haben und dass Sie vorläufiges löschen auf jedem Ihrer wichtigsten Depots aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="503e4-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="503e4-320">Backup Azure wichtige Vault</span><span class="sxs-lookup"><span data-stu-id="503e4-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="503e4-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-321"></span></span>

<span data-ttu-id="503e4-p143">Unmittelbar nach Erstellung oder jede Änderung an einem Schlüssel eine Sicherung durchführen und Speichern von Kopien der Sicherung, online und offline. Offline-Kopien sollte nicht mit einem Netzwerk wie in einer physischen Speicher für sichere oder kommerziellen Einrichtung verbunden werden. Mindestens eine Kopie der Sicherung sollten an einem Speicherort gespeichert werden, die in einem Notfall zugegriffen werden. Die Sicherung Blobs werden ausschließlich Schlüsselmaterial sollte ein Schlüssel Vault-Schlüssel werden dauerhaft oder wiederherzustellen gerendert andernfalls nicht funktioniert. Schlüssel, die außerhalb der Azure-Taste Vault sind und in Azure Schlüssel Vault importiert wurden führen Sie als Sicherungskopie nicht geeignet ist, da die Metadaten für Kunden-Taste, um den Schlüssel verwenden, mit dem externen Schlüssel nicht vorhanden ist. Nur eine Sicherung von Azure Schlüssel Vault kann für Wiederherstellungsvorgänge mit Kundenschlüssel verwendet werden. Aus diesem Grund ist es wichtig, dass eine Sicherung der Azure-Taste Vault vorgenommen werden, sobald eine Taste hochgeladen oder erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="503e4-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="503e4-329">Führen Sie das Cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) zum Erstellen einer Sicherung eines Schlüssels Azure Schlüssel Vault wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="503e4-330">Stellen Sie sicher, dass die Ausgabedatei das Suffix verwendet `.backup`.</span><span class="sxs-lookup"><span data-stu-id="503e4-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="503e4-p144">Dieses Cmdlet entsteht Ausgabedatei ist verschlüsselt und kann nicht außerhalb von Azure Schlüssel Vault verwendet werden. Die Sicherung kann nur mit dem Azure-Abonnement wiederhergestellt werden, von dem die Sicherung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="503e4-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="503e4-p145">Wählen Sie eine Kombination von Ihren Vault Namen und Schlüsselname für die Ausgabedatei. Dadurch wird der Name selbst beschreiben. Es stellt auch sicher, dass backup Dateinamen nicht kollidieren.</span><span class="sxs-lookup"><span data-stu-id="503e4-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="503e4-336">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="503e4-337">Überprüfen der Azure-Taste Vault-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="503e4-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="503e4-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-338"></span></span>

<span data-ttu-id="503e4-p146">Ausführen der Überprüfung vor dem Verwenden der Schlüssel in einem Prevention, DEP ist optional, wird jedoch dringend empfohlen. Insbesondere, wenn Sie die Schritte zum Einrichten Ihrer Schlüssel und Depots andere als die in diesem Thema beschriebenen verwenden, sollten Sie überprüfen die Integrität Ihrer Azure Schlüssel Vault Ressourcen vor dem Konfigurieren der Customer-Taste.</span><span class="sxs-lookup"><span data-stu-id="503e4-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="503e4-341">So überprüfen, dass der Schlüssel Get, WrapKey und UnwrapKey Vorgänge aktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="503e4-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="503e4-342">Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="503e4-p147">Suchen Sie in die Ausgabe für die Richtlinie für den Zugriff und die Exchange Online-ID (GUID) oder die SharePoint Online-ID (GUID) nach Bedarf. Alle drei oben aufgeführten Berechtigungen muss unter Berechtigungen Schlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="503e4-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="503e4-345">Wenn Sie Konfiguration der Richtlinie falsch ist, führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="503e4-346">Beispiel für Exchange Online und Skype für Unternehmen:</span><span class="sxs-lookup"><span data-stu-id="503e4-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="503e4-347">Beispiel für SharePoint Online und OneDrive für Unternehmen:</span><span class="sxs-lookup"><span data-stu-id="503e4-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="503e4-348">So überprüfen, dass ein Ablaufdatum für die Schlüssel wie folgt führen Sie das Cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) nicht festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="503e4-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="503e4-p148">Abgelaufener Schlüssel kann nicht durch Kunden Key verwendet werden und Vorgänge mit einem Schlüssel abgelaufene versucht fehl, und der Benutzer möglicherweise in einem Dienstausfall führen. Es wird dringend empfohlen, dass mit Kundenschlüssel verwendeten Schlüssel nicht über ein Ablaufdatum verfügen. Ein Ablaufdatum, sobald festgelegt ist, kann nicht entfernt werden, jedoch können auf ein anderes Datum geändert werden. Wenn Sie ein Schlüssel verwendet werden muss, die ein Ablaufdatum festgelegt hat, ändern Sie den Ablaufwert auf 12/31/9999 fest. Schlüssel mit einem Ablaufdatum festgelegt zu einem Datum werden andere als 12/31/9999 nicht Office 365-Validierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="503e4-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="503e4-354">Um ein Ablaufdatum zu ändern, die auf einen anderen Wert als 12/31/9999 festgelegt wurde, führen Sie das Cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="503e4-355">Festlegen Sie nicht ein Ablaufdatum auf Verschlüsselungsschlüssel für die Verwendung mit Kundenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="503e4-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="503e4-356">Den URI für jeden Schlüssel Azure Schlüssel Vault zu erhalten</span><span class="sxs-lookup"><span data-stu-id="503e4-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="503e4-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-357"></span></span>

<span data-ttu-id="503e4-p149">Sobald Sie alle Schritte in Azure Einrichten Ihrer wichtigsten Depots abgeschlossen und Ihren Schlüsseln hinzugefügt haben, führen Sie den folgenden Befehl aus, um den URI für den Schlüssel in jeder wichtige Vault abzurufen. Sie müssen diese verwenden URIs beim Erstellen und weisen jedem DEP später, so speichern Sie diese Informationen an einem sicheren Ort. Denken Sie daran, diesen Befehl für jeden Schlüssel Vault einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="503e4-361">In Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="503e4-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="503e4-362">Office 365: Einrichten von Kundenschlüssel für Exchange Online und Skype für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="503e4-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-363"></span></span>

<span data-ttu-id="503e4-p150">Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten der Azure-Taste Vault abgeschlossen haben. Informationen finden Sie unter [Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft schnelle für Kunden-Taste](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="503e4-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="503e4-366">Um Kundenschlüssel für Exchange Online und Skype für Unternehmen einzurichten, müssen Sie diese Schritte ausführen, indem zu Exchange Online mit Windows PowerShell eine Remoteverbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="503e4-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="503e4-367">Erstellen einer Daten-Verschlüsselung-Richtlinie (DEP) für die Verwendung mit Exchange Online und Skype für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="503e4-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-368"></span></span>

<span data-ttu-id="503e4-p151">Eine Datenausführungsverhinderung ist einen Satz von Schlüsseln in Azure Schlüssel Vault gespeicherten zugeordnet. Sie weisen eine DEP eines Postfachs in Office 365. Office 365 wird die in der Richtlinie identifiziert Schlüssel verwenden, um das Postfach zu verschlüsseln. Wenn die Datenausführungsverhinderung erstellen möchten, benötigen Sie die Taste Vault-URIs, die Sie zuvor abgerufen. Weitere Informationen finden Sie in [den URI für jeden Schlüssel Azure Schlüssel Vault beziehen](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="503e4-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="503e4-p152">Denken Sie daran! Beim Erstellen einer Datenausführungsverhinderung Geben Sie zwei Tasten, die sich in zwei verschiedenen Azure Schlüssel Depots befinden. Stellen Sie sicher, dass diese Schlüssel in zwei separate Azure Regionen für die Geo-Redundanz befinden.</span><span class="sxs-lookup"><span data-stu-id="503e4-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="503e4-377">Gehen Sie folgendermaßen vor, um die Datenausführungsverhinderung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="503e4-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="503e4-378">Auf dem lokalen Computer mithilfe eines arbeiten oder Schule Kontos, das in Office 365-Organisation, [eine Verbindung mit Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , indem Sie Windows PowerShell öffnen und Ausführen des folgenden Befehls globaler Administrator-Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="503e4-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="503e4-379">Klicken Sie im Dialogfeld Windows PowerShell anmelden Geben Sie Ihre Arbeit oder Schule Kontoinformationen, klicken Sie auf **OK**, und geben Sie den folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="503e4-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="503e4-380">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="503e4-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="503e4-381">Um eine DEP zu erstellen, verwenden Sie das Cmdlet "New-DataEncryptionPolicy" durch den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="503e4-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="503e4-382">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="503e4-382">Where:</span></span>
    
   -  <span data-ttu-id="503e4-p153">*PolicyName* ist der Name, den Sie für die Richtlinie verwenden möchten. Dürfen enthalten keine Leerzeichen. Beispielsweise USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="503e4-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="503e4-p154">*PolicyDescription* ist eine Beschreibung der Richtlinie, mit die Hilfe Sie nicht vergessen, was für die Richtlinie ist. Sie können in der Beschreibung Leerzeichen enthalten. Beispielsweise Root-Schlüssel für Postfächer in den USA und seine Gebieten.</span><span class="sxs-lookup"><span data-stu-id="503e4-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="503e4-p155">*KeyVaultURI1* ist der URI für den ersten Schlüssel in der Richtlinie. Beispielsweise https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="503e4-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="503e4-p156">*KeyVaultURI2* ist der URI für den zweiten Schlüssel in der Richtlinie. Beispielsweise https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Trennen Sie die beiden URIs durch ein Komma und ein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="503e4-394">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="503e4-395">Zuweisen einer Datenausführungsverhinderung an ein Postfach</span><span class="sxs-lookup"><span data-stu-id="503e4-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="503e4-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-396"></span></span>

<span data-ttu-id="503e4-p157">Weisen Sie die Datenausführungsverhinderung an ein Postfach mithilfe des Cmdlets Set-Mailbox. Nachdem Sie die Richtlinie zuweisen, können Office 365 das Postfach mit dem Schlüssel in der Datenausführungsverhinderung festgelegte verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="503e4-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="503e4-p158">Hierbei gibt *MailboxIdParameter* ein Postfachs an. Weitere Informationen zum Set-Mailbox-Cmdlet finden Sie unter [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="503e4-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="503e4-401">Überprüfen der Postfach-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="503e4-401">Validate mailbox encryption</span></span>
<span data-ttu-id="503e4-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-402"></span></span>

<span data-ttu-id="503e4-p159">Verschlüsseln eines Postfachs kann einige Zeit dauern. Erste Mal Richtlinie zugewiesen das Postfach darüber hinaus müssen die Verschiebung aus einer Datenbank in eine andere, bevor das Postfach des Diensts verschlüsselt werden kann. Es wird empfohlen, dass Sie warten, bevor Sie versuchen, Verschlüsselung zu überprüfen, nachdem Sie eine DEP ändern oder beim ersten Sie eine DEP an ein Postfach zuweisen 72 Stunden.</span><span class="sxs-lookup"><span data-stu-id="503e4-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="503e4-406">Verwenden Sie das Cmdlet Get-MailboxStatistics zu ermitteln, ob ein Postfach verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="503e4-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="503e4-407">Die IsEncrypted-Eigenschaft gibt einen Wert **true,** Wenn das Postfach verschlüsselt sind und den Wert **false** , wenn das Postfach nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="503e4-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="503e4-p160">Die Zeit für das Verschieben von Postfächern, hängt von der Anzahl der Postfächer, die Sie eine DEP zum ersten Mal zuweisen, als auch die Größe der Postfächer ab. Wenn die Postfächer nach einer Woche ab dem Zeitpunkt nicht verschlüsselt wurden Sie die Datenausführungsverhinderung zugewiesen, Verschieben eines Postfachs für die unverschlüsselte Postfächer mit dem Cmdlet New-MoveRequest initiiert.</span><span class="sxs-lookup"><span data-stu-id="503e4-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="503e4-410">Office 365: Einrichten von Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="503e4-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-411"></span></span>

<span data-ttu-id="503e4-p161">Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten der Azure-Taste Vault abgeschlossen haben. Informationen finden Sie unter [Ausführen von Aufgaben in Azure Schlüssel Vault und Microsoft schnelle für Kunden-Taste](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="503e4-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="503e4-414">Um Kundenschlüssel für SharePoint Online und OneDrive für Unternehmen einzurichten, müssen Sie diese Schritte ausführen, indem mit SharePoint Online mit Windows PowerShell eine Remoteverbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="503e4-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="503e4-415">Erstellen Sie eine Daten-Verschlüsselung-Richtlinie (DEP) für jeden SharePoint Online und OneDrive for Business geo</span><span class="sxs-lookup"><span data-stu-id="503e4-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="503e4-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-416"></span></span>

<span data-ttu-id="503e4-p162">Eine Datenausführungsverhinderung ist einen Satz von Schlüsseln in Azure Schlüssel Vault gespeicherten zugeordnet. Eine Datenausführungsverhinderung auf alle Ihre Daten in einem geografischen Standort, auch als bezeichnet eine Geo angewendet. Wenn Sie das Multi-Geo-Feature von Office 365 (derzeit in der Vorschau) verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie nicht mit mehreren geografisch verwenden, können Sie eine Datenausführungsverhinderung für die Verwendung mit SharePoint Online und OneDrive for Business in Office 365 erstellen. Office 365 wird die Schlüssel in der Datenausführungsverhinderung identifiziert verwenden, um Ihre Daten in dieser Geo verschlüsseln. Wenn die Datenausführungsverhinderung erstellen möchten, benötigen Sie die Taste Vault-URIs, die Sie zuvor abgerufen. Weitere Informationen finden Sie in [den URI für jeden Schlüssel Azure Schlüssel Vault beziehen](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="503e4-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="503e4-p163">Denken Sie daran! Beim Erstellen einer Datenausführungsverhinderung Geben Sie zwei Tasten, die sich in zwei verschiedenen Azure Schlüssel Depots befinden. Stellen Sie sicher, dass diese Schlüssel in zwei separate Azure Regionen für die Geo-Redundanz befinden.</span><span class="sxs-lookup"><span data-stu-id="503e4-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="503e4-427">Um eine DEP zu erstellen, müssen Sie eine Remoteverbindung herstellen mit SharePoint Online mithilfe von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="503e4-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="503e4-428">Auf dem lokalen Computer mithilfe eines Kontos arbeiten oder Schule, die in Office 365-Organisation, [eine Verbindung mit SharePoint Online-Powershell](https://technet.microsoft.com/library/fp161372.aspx)globaler Administrator-Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="503e4-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="503e4-429">Führen Sie in der Microsoft SharePoint Online-Verwaltungsshell das Cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="503e4-p164">Wenn Sie die Datenausführungsverhinderung registrieren, beginnt die Verschlüsselung auf die Daten in die Geo. Dies kann eine Weile dauern.</span><span class="sxs-lookup"><span data-stu-id="503e4-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="503e4-432">Überprüfen Sie die Verschlüsselung der Gruppe Websites, Teamwebsites und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="503e4-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-433"></span></span>

<span data-ttu-id="503e4-434">Sie können den Status der Verschlüsselung suchen, indem Sie mit dem Cmdlet Get-SPODataEncryptionPolicy wie folgt ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="503e4-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="503e4-435">Die Ausgabe dieses Cmdlets enthält:</span><span class="sxs-lookup"><span data-stu-id="503e4-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="503e4-436">Der URI der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="503e4-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="503e4-437">Der URI des sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="503e4-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="503e4-p165">Der Verschlüsselungsstatus für die Geo. Mögliche Zuständen zählen:</span><span class="sxs-lookup"><span data-stu-id="503e4-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="503e4-440">**Nicht aufgehoben:** Verschlüsselung mit Schlüssel wurde noch nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="503e4-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="503e4-p166">**Registrieren:** Verschlüsselung mit Schlüssel angewendet wurde, und die Dateien, die gerade verschlüsselt sind. Wenn Ihre Geo in diesem Status ist, benötigen Sie auch angezeigt werden Informationen auf wie viel Prozent der Websites in der Geo abgeschlossen sind, sodass Sie Verschlüsselung Fortschritt überwachen können.</span><span class="sxs-lookup"><span data-stu-id="503e4-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="503e4-443">**Registriert:** Verschlüsselung mit Schlüssel angewendet wurde, und alle Dateien in allen Websites verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="503e4-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="503e4-p167">**Parallelen:** Eine wichtige Rolle ist in Bearbeitung. Wenn Ihre Geo in diesem Status ist, können Sie auch angezeigt werden Informationen wie viel Prozent der Websites haben die wichtigsten Roll-Operation abgeschlossen sein, damit Sie den Fortschritt überwachen können.</span><span class="sxs-lookup"><span data-stu-id="503e4-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="503e4-446">Verwalten von Kunden Product Key für die Office 365</span><span class="sxs-lookup"><span data-stu-id="503e4-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="503e4-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-447"></span></span>

<span data-ttu-id="503e4-448">Nachdem Sie Kundenschlüssel für Office 365 eingerichtet haben, können Sie diese zusätzliche Verwaltungsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="503e4-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="503e4-449">Azure-Taste Vault Schlüssel wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="503e4-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="503e4-450">Zurücksetzen oder gedreht einen Schlüssel in Azure Schlüssel Vault, die Sie mit Kundenschlüssel verwenden</span><span class="sxs-lookup"><span data-stu-id="503e4-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="503e4-451">Verwalten von Berechtigungen für wichtige vault</span><span class="sxs-lookup"><span data-stu-id="503e4-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="503e4-452">Bestimmen der Datenausführungsverhinderung zugewiesen an ein Postfach</span><span class="sxs-lookup"><span data-stu-id="503e4-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="503e4-453">Azure-Taste Vault Schlüssel wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="503e4-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="503e4-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-454"></span></span>

<span data-ttu-id="503e4-p168">Verwenden Sie bevor Sie eine Wiederherstellung ausführen die Wiederherstellungsfunktionen von vorläufiges löschen. Alle Schlüssel, die mit Kundenschlüssel verwendet werden, werden benötigt, um vorläufiges Löschen aktiviert haben. Vorläufiges löschen verhält sich wie ein Papierkorb und ermöglicht die Wiederherstellung bis zu 90 Tage ohne wiederherstellen müssen. Wiederherstellung sollten nur unter Umständen extreme oder ungewöhnliche beispielsweise die Taste oder wichtige Vault verloren gegangen ist erforderlich sein. Wenn Sie einen Schlüssel für die Verwendung mit Kunden-Schlüssel wiederherstellen müssen in Azure PowerShell führen Sie das Cmdlet Restore-AzureKeyVaultKey wie folgt:</span><span class="sxs-lookup"><span data-stu-id="503e4-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="503e4-460">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="503e4-p169">Wenn eine Taste mit dem gleichen Namen in der wichtigsten Vault bereits vorhanden ist, schlägt der Restore-Vorgang fehl. Wiederherstellung AzureKeyVaultKey wiederherstellen alle wichtigen Versionen und alle Metadaten für den Schlüssel, einschließlich der Name des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="503e4-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="503e4-463">Zurücksetzen oder gedreht einen Schlüssel in Azure Schlüssel Vault, die Sie mit Kundenschlüssel verwenden</span><span class="sxs-lookup"><span data-stu-id="503e4-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="503e4-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-464"></span></span>

<span data-ttu-id="503e4-p170">Paralleles Schlüssel ist nicht erforderlich, durch entweder Azure Schlüssel Vault oder Kundenschlüssel. Darüber hinaus sind Schlüssel, die mit einer HSM geschützt sind praktisch unmöglich zu gefährden. Auch wenn ein Stammschlüssel im Besitz des einen böswilligen Akteur wäre gibt es keine machbare Möglichkeit der Nutzung zum Entschlüsseln von Daten, da nur Office 365 Code Verwendungsweise weiß. Paralleles eines Schlüssels ist jedoch durch Kunden Key unterstützt.</span><span class="sxs-lookup"><span data-stu-id="503e4-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="503e4-p171">Führen Sie nur einen Verschlüsselungsschlüssel, den Sie mit Kundenschlüssel verwenden, wenn kein deaktivieren technischer Grund vorhanden ist oder eine Compliance-Anforderung so festgelegt ist, müssen Sie den Schlüssel ein Rollback. Darüber hinaus alle Schlüssel, die Richtlinien zugeordnet wurden oder werden nicht gelöscht. Wenn Sie ein der Schlüssel, wird es Rollback werden mit den vorherigen Schlüsseln Inhalte nicht verschlüsselt. Beispielsweise während aktive Postfächer häufig inaktive erneut verschlüsselt werden werden, möglicherweise getrennt und deaktivierten Postfächer weiterhin mit den vorherigen Schlüsseln verschlüsselt werden. SharePoint Online führt, sodass es möglicherweise archivierten Inhalte mithilfe von ältere Schlüssel Sicherung von Inhalten aus Gründen der Wiederherstellung und Recovery.</span><span class="sxs-lookup"><span data-stu-id="503e4-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="503e4-p172">Um die Sicherheit Ihrer Daten zu gewährleisten, SharePoint Online nicht mehr als einen Schlüssel ein Rollback-Operation zu einem Zeitpunkt durchgeführt werden können. Wenn beide der Schlüssel in einem wichtigen Vault begonnen werden soll, müssen Sie warten, bis der erste wichtige Roll Vorgang vollständig abgeschlossen. Unsere Empfehlung ist, Ihre wichtigsten Roll Vorgänge in verschiedenen Intervallen staffeln, damit dies kein Belang ist.</span><span class="sxs-lookup"><span data-stu-id="503e4-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="503e4-p173">Wenn Sie einen Schlüssel wiederherstellen, werden Sie eine neue Version eines vorhandenen Schlüssels anfordern. Um eine neue Version eines vorhandenen Schlüssels anfordern möchten, verwenden Sie das gleiche-Cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), mit derselben Syntax, die Sie zum Erstellen des Schlüssels an erster Stelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="503e4-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="503e4-479">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="503e4-p174">In diesem Beispiel, da ein Schlüssel mit dem Namen **Contoso-O365EX-NA-VaultA1-Key001** bereits in der **Contoso-O365EX-NA-VaultA1** Vault vorhanden ist wird eine neue Version Schlüssel erstellt werden. Der Vorgang fügt eine neue Version des Schlüssels. Dieser Vorgang behält die wichtigsten früheren Versionen im Versionsverlauf der Schlüssel, sodass zuvor mit diesem Schlüssel verschlüsselte Daten weiterhin entschlüsselt werden können. Sobald Sie parallelen eine beliebige Taste, die ein DEP zugeordnet ist abgeschlossen haben, müssen Sie dann eine zusätzliche-Cmdlet, um sicherzustellen, dass Kundenschlüssel beginnt mit dem neuen Schlüssel ausführen.</span><span class="sxs-lookup"><span data-stu-id="503e4-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="503e4-484">Aktivieren Sie einen neuen Schlüssel verwenden, nachdem Sie ein Rollback oder Schlüssel in Azure Schlüssel Vault drehen Exchange Online und Skype für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="503e4-485">Wenn Sie eine der ein Rollback der Azure-Taste Vault eine DEP zugeordnete TAB-mit Exchange Online und Skype für Business, müssen Sie den folgenden Befehl zum Aktualisieren der Datenausführungsverhinderung und Aktivieren von Office 365 zu starten, mit dem neuen Schlüssel ausführen.</span><span class="sxs-lookup"><span data-stu-id="503e4-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="503e4-486">Angewiesen, Kunden-Taste, um den neuen Schlüssel zum Verschlüsseln von Postfächern in Office 365 führen Sie das Set-DataEncryptionPolicy-Cmdlet wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="503e4-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="503e4-p175">Innerhalb von 48 Stunden werden die aktive Postfächer mit dieser Richtlinie verschlüsselt mit dem aktualisierten Schlüssel verknüpft. Führen Sie die Schritte in [Determine die Datenausführungsverhinderung an ein Postfach zugewiesen](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) , um den Wert für die DataEncryptionPolicyID-Eigenschaft für das Postfach einzuchecken. Der Wert für diese Eigenschaft wird geändert, sobald der aktualisierte Schlüssel angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="503e4-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="503e4-490">Aktivieren Sie einen neuen Schlüssel verwenden, nachdem Sie ein Rollback oder Schlüssel in Azure Schlüssel Vault drehen SharePoint Online und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="503e4-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="503e4-491">Wenn Sie eine der ein Rollback müssen die Azure Schlüssel Vault Schlüssel ein DEP mit SharePoint Online und OneDrive für Unternehmen verwendet, Sie das [Update-SPODataEncryptionPolicy-](https://technet.microsoft.com/library/mt843948.aspx) Cmdlet, um die Datenausführungsverhinderung aktualisieren und Aktivieren von Office 365, um mit dem neuen Schlüssel zu starten.</span><span class="sxs-lookup"><span data-stu-id="503e4-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="503e4-p176">Dadurch wird die Schlüssel Roll-Operation für SharePoint Online und OneDrive für Unternehmen gestartet. Diese Aktion ist nicht direkt. Um den Fortschritt des Schlüssels Vorgang ein Rollback angezeigt wird, führen Sie das Cmdlet Get-SPODataEncryptionPolicy wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="503e4-495">Verwalten von Berechtigungen für wichtige vault</span><span class="sxs-lookup"><span data-stu-id="503e4-495">Manage key vault permissions</span></span>
<span data-ttu-id="503e4-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-496"></span></span>

<span data-ttu-id="503e4-p177">Mehrere Cmdlets sind verfügbar, mit denen Sie anzeigen und, falls erforderlich, entfernen wichtige Vault Berechtigungen. Sie müssen möglicherweise Berechtigungen, beispielsweise zu entfernen, wenn ein Mitarbeiter das Team verlässt.</span><span class="sxs-lookup"><span data-stu-id="503e4-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="503e4-499">Um wichtige Vault Berechtigungen anzuzeigen, führen Sie das Cmdlet Get-AzureRmKeyVault aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="503e4-500">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="503e4-501">Wenn ein Administrator Berechtigungen entfernen möchten, führen Sie das Cmdlet Remove-AzureRmKeyVaultAccessPolicy aus:</span><span class="sxs-lookup"><span data-stu-id="503e4-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="503e4-502">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503e4-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="503e4-503">Bestimmen der Datenausführungsverhinderung zugewiesen an ein Postfach</span><span class="sxs-lookup"><span data-stu-id="503e4-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="503e4-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="503e4-504"></span></span>

<span data-ttu-id="503e4-p178">Um die Datenausführungsverhinderung zugewiesen an ein Postfach zu bestimmen, verwenden Sie das Cmdlet Get-MailboxStatistics aus. Das Cmdlet gibt einen eindeutigen Bezeichner (GUID) zurück.</span><span class="sxs-lookup"><span data-stu-id="503e4-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="503e4-p179">Hierbei gibt *GeneralMailboxOrMailUserIdParameter* ein Postfachs an. Weitere Informationen über das Cmdlet Get-MailboxStatistics finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="503e4-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="503e4-509">Verwenden Sie die GUID, um den Anzeigenamen der die Datenausführungsverhinderung zu erhalten, der das Postfach zugewiesen ist, indem Sie das folgende Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="503e4-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="503e4-510">Dabei ist die *GUID* der GUID, die vom Cmdlet Get-MailboxStatistics im vorherigen Schritt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="503e4-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  


---
title: Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie den Kundenschlüssel für Office 365 für Exchange Online, Skype for Business, SharePoint Online und OneDrive for Business einrichten. Mit dem Kundenschlüssel können Sie die Verschlüsselungsschlüssel Ihrer Organisation steuern und dann Office 365 so konfigurieren, dass Sie zum Verschlüsseln Ihrer Daten im Rest in Microsoft-Rechenzentren verwendet werden.
ms.openlocfilehash: a14a213951bc87e4106e150c88c6b1461a5e685e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218755"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="e2188-104">Kontrolle über Daten in Office 365 mithilfe von Kundenschlüsseln</span><span class="sxs-lookup"><span data-stu-id="e2188-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="e2188-p102">Mit dem Kundenschlüssel können Sie die Verschlüsselungsschlüssel Ihrer Organisation steuern und dann Office 365 so konfigurieren, dass Sie zum Verschlüsseln Ihrer Daten im Rest in Microsoft-Rechenzentren verwendet werden. Zu den restlichen Daten gehören Daten aus Exchange Online und Skype for Business, die in Postfächern und Dateien gespeichert sind, die in SharePoint Online und OneDrive for Business gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e2188-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="e2188-p103">Sie müssen Azure einrichten, bevor Sie den Kundenschlüssel für Office 365 verwenden können. In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um die erforderlichen Azure-Ressourcen zu erstellen und zu konfigurieren und dann die Schritte zum Einrichten des Kunden Schlüssels in Office 365. Nachdem Sie das Azure-Setup abgeschlossen haben, legen Sie fest, welche Richtlinie und daher welche Schlüssel den Postfächern und Dateien in Ihrer Organisation zugewiesen werden sollen. Postfächer und Dateien, für die Sie keine Richtlinie zuweisen, verwenden Verschlüsselungsrichtlinien, die von Microsoft gesteuert und verwaltet werden. Weitere Informationen zum Kundenschlüssel oder eine allgemeine Übersicht finden Sie unter [Kundenschlüssel für Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="e2188-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e2188-p104">Es wird dringend empfohlen, dass Sie die bewährten Methoden in diesem Thema befolgen. Diese werden als **Trinkgeld** und **wichtig**bezeichnet. Mit dem Kundenschlüssel können Sie die Stamm Verschlüsselungsschlüssel steuern, deren Bereich so breit wie die gesamte Organisation sein kann. Dies bedeutet, dass Fehler, die mit diesen Schlüsseln vorgenommen werden, eine große Auswirkung haben und zu Dienstunterbrechungen oder unwiderruflichem Verlust Ihrer Daten führen können.</span><span class="sxs-lookup"><span data-stu-id="e2188-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="e2188-116">Bevor Sie mit dem Einrichten des Kunden Schlüssels beginnen</span><span class="sxs-lookup"><span data-stu-id="e2188-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="e2188-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-117"></span></span>

<span data-ttu-id="e2188-p105">Bevor Sie beginnen, sollten Sie sicherstellen, dass Sie über die entsprechenden Lizenzen für Ihre Organisation verfügen. Der Kundenschlüssel in Office 365 wird in Office 365 E5 oder der Advanced Compliance-SKU angeboten.</span><span class="sxs-lookup"><span data-stu-id="e2188-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="e2188-p106">Um die Konzepte und Verfahren in diesem Thema zu verstehen, sollten Sie sich die [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) -Dokumentation ansehen. Sie können sich auch mit den in Azure verwendeten Ausdrücken vertraut machen, Beispiels [](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)Weise mit dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="e2188-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="e2188-122">Um Feedback zum Kundenschlüssel, einschließlich der Dokumentation, zu geben, senden Sie Ihre Ideen, Vorschläge und Perspektiven an customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e2188-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="e2188-123">Übersicht über das Einrichten des Kunden Schlüssels für Office 365</span><span class="sxs-lookup"><span data-stu-id="e2188-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="e2188-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-124"></span></span>

<span data-ttu-id="e2188-p107">Zum Einrichten des Kunden Schlüssels führen Sie diese Aufgaben aus. Im restlichen Teil dieses Themas finden Sie detaillierte Anweisungen für jede Aufgabe oder Links zu weiteren Informationen für jeden Schritt im Prozess.</span><span class="sxs-lookup"><span data-stu-id="e2188-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="e2188-127">**In Azure und Microsoft:**</span><span class="sxs-lookup"><span data-stu-id="e2188-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="e2188-p108">Die meisten dieser Aufgaben werden durch Remoteverbindung mit Azure PowerShell ausgeführt. Verwenden Sie Version 4.4.0 oder höher von Azure PowerShell, um optimale Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="e2188-130">Erstellen zweier neuer Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="e2188-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="e2188-131">Registrieren von Azure-Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums</span><span class="sxs-lookup"><span data-stu-id="e2188-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="e2188-132">Die Registrierung kann zwischen einem und fünf Werktagen dauern.</span><span class="sxs-lookup"><span data-stu-id="e2188-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="e2188-133">Senden einer Anforderung zum Aktivieren des Kunden Schlüssels für Office 365</span><span class="sxs-lookup"><span data-stu-id="e2188-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="e2188-p109">Nachdem Sie die beiden neuen Azure-Abonnements erstellt haben, müssen Sie die entsprechende Anforderung für das Kunden-Key-Angebot übermitteln, indem Sie ein Webformular ausfüllen, das im Microsoft-Portal für den Zugriff gehostet wird. **Das Team für die Zusammenarbeit bietet keine Unterstützung für den Kundenschlüssel. Office verwendet einfach das Portal für den Überblick, mit dem Sie das Formular übermitteln und uns dabei helfen können, die relevanten Angebote für den Kundenschlüssel nachzuverfolgen**.</span><span class="sxs-lookup"><span data-stu-id="e2188-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. **The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key**.</span></span>
  
<span data-ttu-id="e2188-p110">Nachdem Sie ein Kundenschlüssel Angebot eingereicht haben, prüft Microsoft Ihre Anfrage und benachrichtigt Sie, wenn Sie mit den restlichen Setupaufgaben fortfahren können. Dieser Vorgang kann bis zu fünf Arbeitstage dauern.</span><span class="sxs-lookup"><span data-stu-id="e2188-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="e2188-138">Erstellen eines Premium-Azure-Schlüsseldepots in jedem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e2188-138">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="e2188-139">Zuweisen von Berechtigungen zu jedem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="e2188-139">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="e2188-140">Aktivieren und bestätigen des weichen Löschvorganges in ihren Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="e2188-140">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="e2188-141">Hinzufügen eines Schlüssels zu jedem Schlüsseldepot durch Erstellen oder Importieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="e2188-141">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="e2188-142">Überprüfen der Wiederherstellungsebene der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e2188-142">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="e2188-143">Azure-Schlüsseltresor sichern</span><span class="sxs-lookup"><span data-stu-id="e2188-143">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="e2188-144">Validieren von Azure Key Vault-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="e2188-144">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="e2188-145">Abrufen des URIs für jeden Azure Key Vault-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e2188-145">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="e2188-146">**In Office 365:**</span><span class="sxs-lookup"><span data-stu-id="e2188-146">**In Office 365:**</span></span>
  
<span data-ttu-id="e2188-147">Exchange Online und Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="e2188-147">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="e2188-148">Erstellen einer Daten Verschlüsselungsrichtlinie für die Verwendung mit Exchange Online und Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e2188-148">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="e2188-149">Zuweisen einer DEP zu einem Postfach</span><span class="sxs-lookup"><span data-stu-id="e2188-149">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="e2188-150">ÜberPrüfen der Postfachverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="e2188-150">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="e2188-151">SharePoint Online und OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="e2188-151">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="e2188-152">Erstellen Sie eine Daten Verschlüsselungsrichtlinie (DEP) für jede SharePoint Online-und OneDrive for Business-Geo</span><span class="sxs-lookup"><span data-stu-id="e2188-152">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="e2188-153">Überprüfen der Verschlüsselung von Gruppen Websites, Team Websites und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="e2188-153">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="e2188-154">Ausführen von Aufgaben in Azure Key Vault und Microsoft für den Kundenschlüssel</span><span class="sxs-lookup"><span data-stu-id="e2188-154">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="e2188-155"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-155"></span></span>

<span data-ttu-id="e2188-p111">Führen Sie diese Aufgaben in Azure Key Vault aus, um den Kundenschlüssel für Office 365 einzurichten. Sie müssen diese Schritte unabhängig davon ausführen, ob Sie den Kundenschlüssel für Exchange Online und Skype for Business oder SharePoint Online und OneDrive for Business oder für alle unterstützten Dienste in Office 365 einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="e2188-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="e2188-158">Erstellen zweier neuer Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="e2188-158">Create two new Azure subscriptions</span></span>
<span data-ttu-id="e2188-159"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-159"></span></span>

<span data-ttu-id="e2188-p112">Für den Kundenschlüssel sind zwei Azure-Abonnements erforderlich. Als bewährte vorgehensWeise empfiehlt Microsoft, dass Sie neue Azure-Abonnements für die Verwendung mit dem Kundenschlüssel erstellen. Azure Key Vault-Schlüssel können nur für Anwendungen im selben Azure Active Directory-Mandanten (AAD) autorisiert werden, Sie müssen die neuen Abonnements mit demselben Azure AD-Mandanten erstellen, der mit Ihrer Office 365-Organisation verwendet wird, in der die DEPs zugewiesen werden. Verwenden Sie beispielsweise Ihr Arbeits-oder Schulkonto mit globalen Administratorrechten in Ihrer Office 365-Organisation. Weitere Informationen finden Sie unter [registrieren für Azure als Organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="e2188-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e2188-p113">Der Kundenschlüssel erfordert zwei Schlüssel für jede Daten Verschlüsselungsrichtlinie. Um dies zu erreichen, müssen Sie zwei Azure-Abonnements erstellen. Als bewährte Vorgehensweise empfiehlt Microsoft, dass separate Mitglieder Ihrer Organisation einen Schlüssel in jedem Abonnement konfigurieren. Darüber hinaus sollten diese Azure-Abonnements nur für die Verwaltung von Verschlüsselungsschlüsseln für Office 365 verwendet werden. Dies schützt Ihre Organisation, falls eine ihrer Operatoren versehentlich, absichtlich oder in böswilliger Absicht die Schlüssel löscht, für die Sie verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="e2188-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="e2188-p114">Es wird empfohlen, neue Azure-Abonnements einzurichten, die ausschließlich für die Verwaltung von Azure Key Vault-Ressourcen zur Verwendung mit dem Kundenschlüssel verwendet werden. Es gibt keine praktische Grenze für die Anzahl von Azure-Abonnements, die Sie für Ihre Organisation erstellen können. Durch diese bewährte Vorgehensweise werden die Auswirkungen menschlicher Fehler minimiert und gleichzeitig die Ressourcen der Kundenschlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e2188-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="e2188-173">Senden einer Anforderung zum Aktivieren des Kunden Schlüssels für Office 365</span><span class="sxs-lookup"><span data-stu-id="e2188-173">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="e2188-174"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-174"></span></span>

<span data-ttu-id="e2188-p115">Nachdem Sie die Azure-Schritte abgeschlossen haben, müssen Sie eine Angebotsanforderung im [Microsoft-Portal](https://fasttrack.microsoft.com/)für die Übersendung einreichen. Nachdem Sie eine Anforderung über das Web-Portal für die Verbindung gesendet haben, überprüft Microsoft die von Ihnen bereitgestellten Konfigurationsdaten und Kontaktinformationen von Azure Key Vault. Die Auswahl, die Sie im Angebotsformular bezüglich der autorisierten Mitarbeiter Ihrer Organisation treffen, ist kritisch und für die Fertigstellung der Kundenschlüssel Registrierung erforderlich. Die Offiziere Ihrer Organisation, die Sie im Formular auswählen, werden verwendet, um sicherzustellen, dass alle Anforderungen zum widerrufen und zerstören aller Schlüssel, die mit einer Kundenschlüssel-Daten Verschlüsselungsrichtlinie verwendet werden, verschlüsselt werden. Sie müssen diesen Schritt einmal ausführen, um den Kundenschlüssel für Exchange Online und Skype for Business-Abdeckung zu aktivieren, und ein zweites Mal, um den Kundenschlüssel für SharePoint Online und OneDrive for Business zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e2188-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="e2188-180">Führen Sie die folgenden Schritte aus, um ein Angebot zum Aktivieren des Kunden Schlüssels zu übermitteln:</span><span class="sxs-lookup"><span data-stu-id="e2188-180">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="e2188-181">Melden Sie sich unter Verwendung eines Geschäfts-oder Schul Kontos mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation beim [Microsoft-Portal](https://fasttrack.microsoft.com/)an.</span><span class="sxs-lookup"><span data-stu-id="e2188-181">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="e2188-182">Nachdem Sie sich angemeldet haben, navigieren Sie zum **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="e2188-182">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="e2188-183">Wählen Sie **Angebote**aus, und sehen Sie sich die Liste der aktuellen Angebote an.</span><span class="sxs-lookup"><span data-stu-id="e2188-183">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="e2188-184">Wählen Sie **Weitere Informationen** für das Angebot aus, das für Sie gilt:</span><span class="sxs-lookup"><span data-stu-id="e2188-184">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="e2188-185">**Exchange Online und Skype for Business:** Wählen Sie **Weitere Informationen** zum **Kundenschlüssel für das Exchange** -Angebot aus.</span><span class="sxs-lookup"><span data-stu-id="e2188-185">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="e2188-186">**SharePoint Online und OneDrive for Business:** **Weitere Informationen finden Sie** unter **Kundenschlüssel für SharePoint und OneDrive for Business-** Angebot.</span><span class="sxs-lookup"><span data-stu-id="e2188-186">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="e2188-187">Klicken Sie auf der Seite **Angebotsdetails** auf **Anforderung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="e2188-187">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="e2188-p116">Füllen Sie alle relevanten Details und erforderlichen Informationen im Angebotsformular aus. Achten Sie besonders auf Ihre Auswahl für die Mitarbeiter Ihrer Organisation, die die dauerhafte und irreversible Zerstörung von Verschlüsselungsschlüsseln und Daten genehmigen möchten. Nachdem Sie das Formular ausgefüllt haben, \*\*\*\* klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="e2188-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="e2188-191">Dieser Vorgang kann bis zu fünf Werktage dauern, nachdem Microsoft Ihre Anforderung benachrichtigt hat.</span><span class="sxs-lookup"><span data-stu-id="e2188-191">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="e2188-192">Weiter unten im Abschnitt obligatorische Aufbewahrungsdauer.</span><span class="sxs-lookup"><span data-stu-id="e2188-192">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="e2188-193">Registrieren von Azure-Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums</span><span class="sxs-lookup"><span data-stu-id="e2188-193">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="e2188-194"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-194"></span></span>

<span data-ttu-id="e2188-p117">Der vorübergehende oder dauerhafte Verlust von Verschlüsselungsschlüsseln kann sehr störend oder sogar katastrophal für den Dienstvorgang sein und zu Datenverlusten führen. Aus diesem Grund erfordern die mit dem Kundenschlüssel verwendeten Ressourcen einen starken Schutz. Alle Azure-Ressourcen, die mit dem Kundenschlüssel verwendet werden, bieten Schutzmechanismen jenseits der Standardkonfiguration. Azure-Abonnements können auf eine Weise gekennzeichnet oder registriert werden, die eine sofortige und unwiderrufliche Stornierung verhindert. Dies wird als Registrierung für eine obligatorische Aufbewahrungsdauer bezeichnet. Die erforderlichen Schritte zum Registrieren von Azure-Abonnements für einen obligatorischen Aufbewahrungszeitraum erfordern eine Zusammenarbeit mit dem Office 365-Team. Dieser Prozess kann zwischen einem und fünf Werktagen dauern. Zuvor wurde dies auch als "nicht abbrechen" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e2188-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="e2188-203">Bevor Sie sich mit dem Office 365-Team in Verbindung setzen, müssen Sie für jedes Azure-Abonnement, das Sie mit dem Kundenschlüssel verwenden, die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="e2188-203">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="e2188-p118">Melden Sie sich bei Ihrem Azure-Abonnement mit Azure PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="e2188-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="e2188-206">Führen Sie das Cmdlet Register-AzureRmProviderFeature aus, um Ihre Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e2188-206">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="e2188-p119">Wenden Sie sich an Microsoft, um den Prozess abzuschließen. Wenden Sie sich für das SharePoint-und OneDrive for Business-Team an [Spock@microsoft.com](mailto:spock@microsoft.com). Für Exchange Online und Skype for Business wenden Sie sich an [exock@microsoft.com](mailto:exock@microsoft.com). Die Vereinbarung zum Service Level (SLA) für den Abschluss dieses Vorgangs beträgt fünf Werktage, nachdem Microsoft benachrichtigt (und überprüft) wurde, dass Sie Ihre Abonnements für die Verwendung eines obligatorischen Aufbewahrungszeitraums registriert haben. Fügen Sie Folgendes in Ihre e-Mail ein:</span><span class="sxs-lookup"><span data-stu-id="e2188-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="e2188-212">**Betreff**: Kundenschlüssel für \< *den vollqualifizierten Domänennamen Ihres Mandanten*\></span><span class="sxs-lookup"><span data-stu-id="e2188-212">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="e2188-213">**Body**: Abonnement-IDs, für die Sie den obligatorischen Aufbewahrungszeitraum abschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="e2188-213">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="e2188-214">Sobald Sie von Microsoft eine Benachrichtigung erhalten haben, dass die Registrierung abgeschlossen ist, überprüfen Sie den Status Ihrer Registrierung, indem Sie das Cmdlet Get-AzureRmProviderFeature wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="e2188-214">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="e2188-215">Führen Sie den folgenden Befehl aus, um den Vorgang abzuschließen, nachdem Sie sichergestellt haben, dass die Eigenschaft **Registrierungsstatus** des Cmdlets Get-AzureRmProviderFeature den Wert **registered**zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="e2188-215">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="e2188-216">Erstellen eines Premium-Azure-Schlüsseldepots in jedem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e2188-216">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="e2188-217"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-217"></span></span>

<span data-ttu-id="e2188-218">Die Schritte zum Erstellen eines Schlüssel Tresors sind unter [Erste Schritte mit Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/)dokumentiert, in dem Sie die Installation und Einführung von Azure PowerShell, das Herstellen einer Verbindung mit Ihrem Azure-Abonnement, das Erstellen einer Ressourcengruppe und das Erstellen eines Schlüsseldepots in diesem Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2188-218">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="e2188-p120">Wenn Sie einen schlüsseltresor erstellen, müssen Sie eine SKU wählen: entweder Standard oder Premium. Die Standard-SKU ermöglicht das Schützen von Azure Key Vault-Schlüsseln mit Software – es gibt keinen Sicherheitsmodul-Schlüsselschutz (HSM) – und die Premium-SKU ermöglicht die Verwendung von HSMs für den Schutz von Schlüsseltresor Schlüsseln. Der Kundenschlüssel akzeptiert Schlüsseldepots, die entweder SKU verwenden, obwohl Microsoft dringend empfiehlt, nur die Premium-SKU zu verwenden. Die Kosten für Vorgänge mit Schlüsseln beider Typen sind identisch, daher ist der einzige Kostenunterschied die Kosten pro Monat für jeden HSM-geschützten Schlüssel. Details finden Sie unter [Key Vault Pricing](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="e2188-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e2188-224">Verwenden Sie die Premium-SKU-Schlüsseldepots und HSM-Protected-Schlüssel für Produktionsdaten, und verwenden Sie nur Standard-SKU-Schlüsseldepots und-Schlüssel zu Test-und Validierungszwecken.</span><span class="sxs-lookup"><span data-stu-id="e2188-224">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="e2188-p121">Erstellen Sie für jeden Office 365-Dienst, mit dem Sie den Kundenschlüssel verwenden, in jedem der beiden Azure-Abonnements, die Sie erstellt haben, einen schlüsseltresor. Wenn Sie beispielsweise nur für Exchange Online und Skype for Business oder SharePoint Online und OneDrive for Business tätig sind, erstellen Sie nur ein paar von Vaults. Zum Aktivieren des Kunden Schlüssels für Exchange Online und SharePoint Online erstellen Sie zwei schlüsseltresor Paare.</span><span class="sxs-lookup"><span data-stu-id="e2188-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="e2188-p122">Verwenden Sie eine Benennungskonvention für Schlüssel Tresore, die die vorgesehene Verwendung der DEP widerspiegelt, mit der Sie die Tresore verknüpfen möchten. Weitere Informationen finden Sie im Abschnitt bewährte Methoden unter Empfehlungen zur Benennungskonvention.</span><span class="sxs-lookup"><span data-stu-id="e2188-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="e2188-p123">Erstellen Sie eine separate, paarweise Reihe von Vaults für jede Daten Verschlüsselungsrichtlinie. Für Exchange Online wird der Bereich einer Daten Verschlüsselungsrichtlinie von Ihnen ausgewählt, wenn Sie die Richtlinie dem Postfach zuweisen. Einem Postfach kann nur eine Richtlinie zugewiesen werden, und Sie können bis zu 50 Richtlinien erstellen. Für SharePoint Online ist der Bereich einer Richtlinie alle Daten innerhalb einer Organisation an einem geografischen Standort oder Geo.</span><span class="sxs-lookup"><span data-stu-id="e2188-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="e2188-p124">Für die Erstellung von Schlüsseldepots ist außerdem die Erstellung von Azure-Ressourcengruppen erforderlich, da für Schlüsseldepots Speicherkapazität (obwohl sehr klein) erforderlich ist und die Schlüsseldepot Protokollierung, falls aktiviert, auch gespeicherte Daten generiert. Als bewährte Methode empfiehlt Microsoft die Verwendung separater Administratoren zum Verwalten der einzelnen Ressourcengruppen, wobei die Verwaltung mit den Administratoren ausgerichtet ist, die alle zugehörigen Kundenschlüssel Ressourcen verwalten.</span><span class="sxs-lookup"><span data-stu-id="e2188-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e2188-p125">Um die Verfügbarkeit zu maximieren, sollten sich Ihre Schlüsseldepots in Regionen in der Umgebung Ihres Office 365-Diensts befinden. Wenn sich Ihre Exchange Online-Organisation beispielsweise in Nordamerika befindet, platzieren Sie Ihre Schlüsseldepots in Nordamerika. Wenn sich Ihre Exchange Online-Organisation in Europa befindet, legen Sie Ihre Schlüsseldepots in Europa ab.</span><span class="sxs-lookup"><span data-stu-id="e2188-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="e2188-p126">Verwenden Sie ein gemeinsames Präfix für Schlüssel Tresore, und schließen Sie eine Abkürzung für die Verwendung und den Umfang des Schlüssel Tresors und der Schlüssel ein (beispielsweise für den Contoso SharePoint-Dienst, in dem sich die Tresore in Nordamerika befinden werden, ein mögliches paar von Namen ist contoso-O365SP-NA-VaultA1 und Contoso-O365SP-NA-VaultA2. Vault-Namen sind global eindeutige Zeichenfolgen innerhalb von Azure, daher müssen Sie möglicherweise Variationen Ihrer gewünschten Namen ausprobieren, falls die gewünschten Namen bereits von anderen Azure-Kunden beansprucht werden. 2017 Vault-Namen können nicht geändert werden, daher empfiehlt es sich, einen schriftlichen Plan für das Setup zu haben und eine zweite Person zu verwenden, um zu überprüfen, ob der Plan ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2188-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="e2188-p127">Erstellen Sie nach Möglichkeit Ihre Tresore in nicht gepaarten Regionen. Paarweise gePaarte Azure-Regionen bieten eine hohe Verfügbarkeit für Dienst fehlerdomänen. Daher können regionale Paare als Sicherungs Region des jeweils anderen betrachtet werden. Dies bedeutet, dass eine Azure-Ressource, die in einem Bereich eingefügt wird, automatisch eine Fehlertoleranz durch den gepaarten Bereich erlangt. Aus diesem Grund wird durch das Auswählen von Regionen für zwei Tresore, die in einem DEP verwendet werden, in dem die Regionen gekoppelt sind, nur eine Gesamtanzahl von zwei Verfügbarkeits Regionen verwendet. Die meisten Geographen haben nur zwei Regionen, daher ist es noch nicht möglich, nicht gepaarte Regionen auszuwählen. Wählen Sie nach Möglichkeit zwei nicht gepaarte Regionen für die beiden Tresore aus, die mit einem DEP verwendet werden. Dies profitiert von insgesamt vier Verfügbarkeits Regionen. Weitere Informationen finden Sie unter [Business Continuity and Disaster Recovery (BCDR): Azure pairEd Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current List of Regional Pairs.</span><span class="sxs-lookup"><span data-stu-id="e2188-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="e2188-251">Zuweisen von Berechtigungen zu jedem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="e2188-251">Assign permissions to each key vault</span></span>
<span data-ttu-id="e2188-252"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-252"></span></span>

<span data-ttu-id="e2188-p128">Für jeden schlüsseltresor müssen Sie je nach Implementierung drei separate Berechtigungssätze für den Kundenschlüssel definieren. Sie müssen beispielsweise einen Satz von Berechtigungen für jede der folgenden definieren:</span><span class="sxs-lookup"><span data-stu-id="e2188-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="e2188-p129">**Wichtige Vault-Administratoren** , die die tägliche Verwaltung Ihres Schlüsseldepots für Ihre Organisation ausführen. Zu diesen Aufgaben gehört das sichern, erstellen, abrufen, importieren, auflisten und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="e2188-p130">Der Satz von Berechtigungen, die schlüsseltresor-Administratoren zugewiesen sind, enthält nicht die Berechtigung zum Löschen von Schlüsseln. Dies ist beabsichtigt und eine wichtige Vorgehensweise. Das Löschen von Verschlüsselungsschlüsseln erfolgt in der Regel nicht, da Daten dauerhaft gelöscht werden. Als bewährte Methode sollten Sie diese Berechtigung nicht standardmäßig den schlüsseltresor-Administratoren erteilen. Behalten Sie stattdessen diese für wichtige Vault-Mitwirkende bei, und weisen Sie Sie nur kurzfristig einem Administrator zu, wenn ein klares Verständnis der Konsequenzen verstanden wird.</span><span class="sxs-lookup"><span data-stu-id="e2188-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="e2188-p131">Wenn Sie diesen Berechtigungen einem Benutzer in Ihrer Office 365-Organisation zuweisen möchten, melden Sie sich bei Ihrem Azure-Abonnement mit Azure PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="e2188-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="e2188-264">Führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy aus, um die erforderlichen Berechtigungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e2188-264">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="e2188-265">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-265">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="e2188-p132">**Wichtige Vault** -Mitwirkende, die Berechtigungen für den Azure-schlüsseltresor selbst ändern können. Sie müssen diese Berechtigungen ändern, wenn Mitarbeiter verlassen oder Ihrem Team beitreten, oder in der äußerst seltenen Situation, dass die schlüsseltresor-Administratoren berechtigterweise die Berechtigung zum Löschen oder Wiederherstellen eines Schlüssels benötigen. Dieser Gruppe von wichtigen Vault-Mitwirkenden muss die Rolle \*\*\*\* "Mitwirkende" in Ihrem schlüsseltresor erteilt werden. Sie können diese Rolle mithilfe des Azure-Ressourcen-Managers zuweisen. Weitere Informationen finden Sie unter [Verwenden der rollenbasierten Zugriffssteuerung zum Verwalten des Zugriffs auf Ihre Azure-Abonnement Ressourcen](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Der Administrator, der ein Abonnement erstellt, hat diesen Zugriff implizit sowie die Möglichkeit, andere Administratoren der Rolle mitWirkender zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="e2188-p133">Wenn Sie den Kundenschlüssel mit Exchange Online und Skype for Business verwenden möchten, müssen Sie Office 365 die Berechtigung erteilen, das Schlüsseldepot im Namen von Exchange Online und Skype for Business zu verwenden. Wenn Sie den Kundenschlüssel mit SharePoint Online und OneDrive for Business verwenden möchten, müssen Sie entsprechend die Berechtigung für das Office 365 hinzufügen, um das Schlüsseldepot im Namen von SharePoint Online und OneDrive for Business zu verwenden. Führen Sie das Cmdlet **Set-AzureRmKeyVaultAccessPolicy** mit der folgenden Syntax aus, um die Berechtigung für Office 365 zu erteilen:</span><span class="sxs-lookup"><span data-stu-id="e2188-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="e2188-275">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="e2188-275">Where:</span></span>
    
  - <span data-ttu-id="e2188-276">*vaultname* ist der Name des Schlüsseldepots, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e2188-276">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="e2188-277">Ersetzen Sie *Office 365* -ID für Exchange Online und Skype for Business durch`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="e2188-277">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="e2188-278">Ersetzen Sie *Office 365* -ID für SharePoint Online und OneDrive for Business durch`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="e2188-278">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="e2188-279">Beispiel: Festlegen von Berechtigungen für Exchange Online und Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="e2188-279">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="e2188-280">Beispiel: Festlegen von Berechtigungen für SharePoint Online und OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e2188-280">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="e2188-281">Aktivieren und bestätigen des weichen Löschvorganges in ihren Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="e2188-281">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="e2188-282"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-282"></span></span>

<span data-ttu-id="e2188-p134">Wenn Sie Ihre Schlüssel schnell wiederherstellen können, ist die Wahrscheinlichkeit eines erweiterten Dienstausfalls aufgrund versehentlich oder in böswilliger Absicht gelöschter Schlüssel geringer. Sie müssen diese Konfiguration, die als weiche Löschung bezeichnet wird, aktivieren, bevor Sie Ihre Schlüssel mit dem Kundenschlüssel verwenden können. Durch Aktivieren von Soft Delete können Sie Schlüssel oder Depots innerhalb von 90 Tagen nach dem Löschen wiederherstellen, ohne Sie aus der Sicherung wiederherstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="e2188-286">Führen Sie die folgenden Schritte aus, um die weiche Löschung in ihren Schlüsseldepots zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="e2188-286">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="e2188-p135">Melden Sie sich bei Ihrem Azure-Abonnement mit Windows PowerShell an. Weitere Informationen finden Sie unter [Anmelden mit Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="e2188-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="e2188-p136">Führen Sie das Cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) aus. In diesem Beispiel ist *vaultname* der Name des Schlüssel Tresors, für den Sie das weiche löschen aktivieren:</span><span class="sxs-lookup"><span data-stu-id="e2188-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="e2188-p137">Bestätigen Sie, dass die weiche Löschung für das Schlüsseldepot konfiguriert ist, indem Sie das Cmdlet **Get-AzureRmKeyVault** ausführen. Wenn Soft Delete für den schlüsseltresor ordnungsgemäß konfiguriert ist, ist der weiche Löschvorgang aktiviert? -Eigenschaft gibt den Wert **true**zurück:</span><span class="sxs-lookup"><span data-stu-id="e2188-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="e2188-293">Hinzufügen eines Schlüssels zu jedem Schlüsseldepot durch Erstellen oder Importieren eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="e2188-293">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="e2188-294"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-294"></span></span>

<span data-ttu-id="e2188-p138">Es gibt zwei Möglichkeiten, einem Azure-Schlüsseltresor Schlüssel hinzuzufügen. Sie können einen Schlüssel direkt im Key Vault erstellen, oder Sie können einen Schlüssel importieren. Das Erstellen eines Schlüssels direkt im Schlüsseltresor ist die unkompliziertere Methode, während der Import eines Schlüssels die vollständige Kontrolle über die Generierung des Schlüssels bietet.</span><span class="sxs-lookup"><span data-stu-id="e2188-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="e2188-297">Führen Sie das [Add-AzureKeyVaultKey-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) Cmdlet wie folgt aus, um einen Schlüssel direkt in Ihrem schlüsseltresor zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e2188-297">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="e2188-298">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="e2188-298">Where:</span></span>
  
-  <span data-ttu-id="e2188-299">*vaultname* ist der Name des Schlüssel Tresors, in dem Sie den Schlüssel erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e2188-299">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="e2188-300">*keyName* ist der Name, den Sie dem neuen Schlüssel geben möchten.</span><span class="sxs-lookup"><span data-stu-id="e2188-300">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="e2188-p139">Benennen Sie Schlüssel unter Verwendung einer ähnlichen Benennungskonvention wie oben beschrieben für Schlüsseldepots. Auf diese Weise wird in Tools, die nur den Schlüsselnamen anzeigen, die Zeichenfolge selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="e2188-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="e2188-303">Wenn Sie den Schlüssel mit einem HSM schützen möchten, stellen Sie sicher, dass Sie **HSM** als Wert des Parameters _Destination_ angeben, andernfalls geben Sie **Software**an.</span><span class="sxs-lookup"><span data-stu-id="e2188-303">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="e2188-304">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-304">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="e2188-305">Um einen Schlüssel direkt in Ihr Schlüsseldepot zu importieren, benötigen Sie ein Thales nShield-Hardware Sicherheitsmodul.</span><span class="sxs-lookup"><span data-stu-id="e2188-305">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="e2188-306">Einige Organisationen bevorzugen diesen Ansatz, um die Herkunft Ihrer Schlüssel zu bestimmen, und die diese Methode stellt auch Folgendes bereit:</span><span class="sxs-lookup"><span data-stu-id="e2188-306">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="e2188-307">Das für den Import verwendete Toolset umfasst die Bescheinigung von Thales, dass der Schlüsselaustauschschlüssel (KEK), der zum Verschlüsseln des von Ihnen generierten Schlüssels verwendet wird, nicht exportierbar ist und innerhalb eines echten HSM generiert wird, das von Thales hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2188-307">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="e2188-p140">Das Toolset enthält die Bescheinigung von Thales, dass die Azure Key Vault-Sicherheitswelt auch auf einem echten HSM von Thales hergestellt wurde. Diese Bescheinigung weist darauf hin, dass Microsoft auch echte Thales-Hardware verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2188-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="e2188-p141">Erkundigen Sie sich bei ihrer Sicherheitsgruppe, ob die obigen Bescheinigungen erforderlich sind. Ausführliche Schritte zum Erstellen eines lokalen Schlüssels und zum Importieren dieser Schlüssel in ihren schlüsseltresor finden Sie unter [Vorgehensweise: generieren und übertragen von HSM-geschützten Schlüsseln für Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Verwenden Sie die Azure-Anweisungen, um einen Schlüssel in jedem schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="e2188-313">Überprüfen der Wiederherstellungsebene der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e2188-313">Check the recovery level of your keys</span></span>
<span data-ttu-id="e2188-314"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-314"></span></span>

<span data-ttu-id="e2188-p142">Office 365 erfordert, dass das Azure Key Vault-Abonnement auf nicht abbrechen festgelegt ist und dass die vom Kundenschlüssel verwendeten Schlüssel weiche Löschfunktion aktiviert haben. Sie können dies überprüfen, indem Sie sich die Wiederherstellungs Stufe für Ihre Schlüssel ansehen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="e2188-317">Führen Sie zum Überprüfen der Wiederherstellungsebene eines Schlüssels in Azure PowerShell das Cmdlet Get-AzureKeyVaultKey wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-317">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="e2188-318">Wenn die Eigenschaft wiederHerstellungsEbene einen anderen Wert als " _wieder_ **herstellbare + ProtectedSubscription**" zurückgibt, müssen Sie dieses Thema überprüfen und sicherstellen, dass Sie alle Schritte ausgeführt haben, um das Abonnement auf die Liste nicht abbrechen zu setzen und , dass für jedes Schlüsseldepot der Soft Delete aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2188-318">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="e2188-319">Azure-Schlüsseltresor sichern</span><span class="sxs-lookup"><span data-stu-id="e2188-319">Backup Azure Key Vault</span></span>
<span data-ttu-id="e2188-320"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-320"></span></span>

<span data-ttu-id="e2188-p143">Führen Sie sofort nach dem Erstellen oder Ändern eines Schlüssels eine Sicherung aus, und speichern Sie Kopien der Sicherung, sowohl online als auch offline. Offline Kopien sollten nicht mit einem Netzwerk verbunden sein, beispielsweise in einer physischen oder kommerziellen Speicheranlage. Mindestens eine Kopie der Sicherung sollte an einem Speicherort gespeichert werden, auf den bei einem Notfall zugegriffen werden kann. Die Sicherungs BLOBs sind das einzige Mittel zur Wiederherstellung von Schlüsselmaterial, wenn ein Schlüsseltresor dauerhaft zerstört oder anderweitig nicht mehr funktionsfähig ist. Schlüssel, die sich außerhalb von Azure Key Vault befinden und in Azure Key Vault importiert wurden, können nicht als Sicherung verwendet werden, da die Metadaten, die für den Kundenschlüssel erforderlich sind, nicht mit dem externen Schlüssel vorhanden sind. Nur eine Sicherung aus Azure Key Vault kann für Wiederherstellungsvorgänge mit Kundenschlüssel verwendet werden. Daher ist es wichtig, dass eine Sicherung von Azure Key Vault durchgeführt wird, nachdem ein Schlüssel hochgeladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2188-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="e2188-328">Führen Sie das Cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) wie folgt aus, um eine Sicherung eines Azure Key Vault-Schlüssels zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e2188-328">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="e2188-329">Stellen Sie sicher, dass die Ausgabedatei `.backup`das Suffix verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2188-329">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="e2188-p144">Die aus diesem Cmdlet resultierende Ausgabedatei ist verschlüsselt und kann nicht außerhalb von Azure Key Vault verwendet werden. Die Sicherung kann nur für das Azure-Abonnement wiederhergestellt werden, von dem die Sicherung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2188-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="e2188-p145">Wählen Sie für die Ausgabedatei eine Kombination aus Vault-und Schlüsselnamen aus. Dadurch wird der Dateiname selbsterklärend. Außerdem wird sichergestellt, dass die Namen der Sicherungsdateien nicht kollidieren.</span><span class="sxs-lookup"><span data-stu-id="e2188-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="e2188-335">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-335">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="e2188-336">Validieren von Azure Key Vault-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="e2188-336">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="e2188-337"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-337"></span></span>

<span data-ttu-id="e2188-p146">Das Durchführen einer Validierung vor dem Verwenden von Schlüsseln in einer DEP ist optional, wird jedoch dringend empfohlen. Wenn Sie beispielsweise die in diesem Thema beschriebenen Schritte zum Einrichten Ihrer Schlüssel und Tresore verwenden, sollten Sie die Integrität ihrer Azure Key Vault-Ressourcen überprüfen, bevor Sie den Kundenschlüssel konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e2188-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="e2188-340">So überprüfen Sie, ob für die Schlüssel Get-, wrapKey-und unwrapKey-Vorgänge aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="e2188-340">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="e2188-341">Führen [Sie das Get-AzureRmKeyVault-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) Cmdlet wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-341">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="e2188-p147">Suchen Sie in der Ausgabe nach den entsprechenden Zugriffsrichtlinien und der Exchange Online-Identität (GUID) oder der SharePoint Online-Identität (GUID). Alle drei obigen Berechtigungen müssen unter Berechtigungen für Schlüssel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e2188-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="e2188-344">Wenn die Konfiguration der Zugriffsrichtlinie falsch ist, führen Sie das Cmdlet Set-AzureRmKeyVaultAccessPolicy wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-344">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="e2188-345">Beispielsweise für Exchange Online und Skype for Business:</span><span class="sxs-lookup"><span data-stu-id="e2188-345">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="e2188-346">Beispielsweise für SharePoint Online und OneDrive for Business:</span><span class="sxs-lookup"><span data-stu-id="e2188-346">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="e2188-347">Führen Sie das [Get-AzureKeyVaultKey-](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) Cmdlet wie folgt aus, um zu überprüfen, ob ein Ablaufdatum für die Schlüssel festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="e2188-347">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="e2188-p148">Ein abgelaufener Schlüssel kann nicht vom Kundenschlüssel verwendet werden, und Vorgänge, die mit einem abgelaufenen Schlüssel versucht wurden, können fehlschlagen und zu einem Dienstausfall führen. Es wird dringend empfohlen, dass Schlüssel, die mit dem Kundenschlüssel verwendet werden, kein Ablaufdatum aufweisen. Ein Ablaufdatum, einmal festgelegt, kann nicht entfernt werden, kann aber in ein anderes Datum geändert werden. Wenn ein Schlüssel verwendet werden muss, der ein Ablaufdatum festgelegt hat, ändern Sie den Ablaufwert in 12/31/9999. Schlüssel mit einem Ablaufdatum, das auf ein anderes Datum als 12/31/9999 festgelegt ist, führen keine Office 365-Validierung aus.</span><span class="sxs-lookup"><span data-stu-id="e2188-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="e2188-353">Wenn Sie ein Ablaufdatum ändern möchten, das auf einen anderen Wert als 12/31/9999 festgelegt wurde, führen Sie das Cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-353">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="e2188-354">Legen Sie keine Ablaufdaten für Verschlüsselungsschlüssel fest, die Sie mit dem Kundenschlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2188-354">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="e2188-355">Abrufen des URIs für jeden Azure Key Vault-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e2188-355">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="e2188-356"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-356"></span></span>

<span data-ttu-id="e2188-p149">Nachdem Sie alle Schritte in Azure ausgeführt haben, um Ihre Schlüsseldepots einzurichten und Ihre Schlüssel hinzugefügt haben, führen Sie den folgenden Befehl aus, um den URI für den Schlüssel in jedem schlüsseltresor abzurufen. Sie müssen diese URIs verwenden, wenn Sie jede DEP später erstellen und zuweisen, diese Informationen also an einem sicheren Ort speichern. Denken Sie daran, diesen Befehl einmal für jeden schlüsseltresor auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="e2188-360">In Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e2188-360">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="e2188-361">Office 365: Einrichten des Kunden Schlüssels für Exchange Online und Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e2188-361">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="e2188-362"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-362"></span></span>

<span data-ttu-id="e2188-p150">Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten von Azure Key Vault abgeschlossen haben. Weitere Informationen finden Sie unter [Complete Tasks in Azure Key Vault und Microsoft für den Kundenschlüssel](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="e2188-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="e2188-365">Um den Kundenschlüssel für Exchange Online und Skype for Business einzurichten, müssen Sie diese Schritte ausführen, indem Sie Remote eine Verbindung zu Exchange Online mit Windows PowerShell herstellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-365">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="e2188-366">Erstellen einer Daten Verschlüsselungsrichtlinie für die Verwendung mit Exchange Online und Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e2188-366">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="e2188-367"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-367"></span></span>

<span data-ttu-id="e2188-p151">Eine DEP ist mit einem Schlüsselsatz verknüpft, der in Azure Key Vault gespeichert ist. Sie weisen einem Postfach in Office 365 eine DEP zu. Office 365 verwendet dann die in der Richtlinie angegebenen Schlüssel, um das Postfach zu verschlüsseln. Zum Erstellen der datenAUSFÜHRUNGSverHINDERung benötigen Sie die wichtigsten Vault-URIs, die Sie zuvor abgerufen haben. Anweisungen dazu finden Sie unter [Abrufen des URIs für jeden Azure Key Vault-Schlüssel](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="e2188-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="e2188-p152">Denken Sie daran! Wenn Sie eine DEP erstellen, geben Sie zwei Schlüssel an, die sich in zwei verschiedenen Azure-Schlüsseldepots befinden. Stellen Sie sicher, dass sich diese Schlüssel in zwei getrennten Azure-Regionen befinden, um die Geo-Redundanz sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="e2188-376">Führen Sie die folgenden Schritte aus, um die DEP zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e2188-376">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="e2188-377">Stellen Sie auf Ihrem lokalen Computer über ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation eine [Verbindung zu Exchange Online PowerShell her](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , indem Sie Windows PowerShell öffnen und den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2188-377">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="e2188-378">Geben Sie im Dialogfeld für die Windows PowerShell-Anmelde informationsAnforderung Ihre geschäftlichen oder Schulkonto Informationen ein, klicken Sie auf **OK**, und geben Sie den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e2188-378">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="e2188-379">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="e2188-379">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="e2188-380">Verwenden Sie zum Erstellen einer datenAUSFÜHRUNGSverHINDERung das Cmdlet New-DataEncryptionPolicy, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="e2188-380">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="e2188-381">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="e2188-381">Where:</span></span>
    
   -  <span data-ttu-id="e2188-p153">*PolicyName* ist der Name, den Sie für die Richtlinie verwenden möchten. Namen dürfen keine Leerzeichen enthalten. Beispiel: USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="e2188-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="e2188-p154">*PolicyDescription* ist eine benutzerfreundliche Beschreibung der Richtlinie, mit der Sie sich an die Richtlinie erinnern können. Sie können Leerzeichen in die Beschreibung aufnehmen. Beispiel: Stammschlüssel für Postfächer in den USA und dessen Territorien.</span><span class="sxs-lookup"><span data-stu-id="e2188-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="e2188-p155">*KeyVaultURI1* ist der URI für den ersten Schlüssel in der Richtlinie. Beispiel: https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="e2188-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="e2188-p156">*KeyVaultURI2* ist der URI für den zweiten Schlüssel in der Richtlinie. Beispiel: https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Trennen Sie die beiden URIs durch ein Komma und ein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="e2188-393">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-393">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="e2188-394">Zuweisen einer DEP zu einem Postfach</span><span class="sxs-lookup"><span data-stu-id="e2188-394">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="e2188-395"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-395"></span></span>

<span data-ttu-id="e2188-p157">Weisen Sie die DEP mithilfe des Cmdlets Set-Mailbox einem Postfach zu. Nachdem Sie die Richtlinie zugewiesen haben, kann Office 365 das Postfach mit dem in der DEP angegebenen Schlüssel verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e2188-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="e2188-p158">Wobei *MailboxIdParameter* ein Postfach angibt. Weitere Informationen zum Cmdlet Set-Mailbox finden Sie unter [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2188-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="e2188-400">ÜberPrüfen der Postfachverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="e2188-400">Validate mailbox encryption</span></span>
<span data-ttu-id="e2188-401"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-401"></span></span>

<span data-ttu-id="e2188-p159">Das verSchlüsseln eines Postfachs kann einige Zeit in Anspruch nehmen. Bei der erstmaligen Richtlinienzuweisung muss das Postfach die Verschiebung von einer Datenbank in eine andere abschließen, bevor der Dienst das Postfach verschlüsseln kann. Es wird empfohlen, dass Sie 72 Stunden warten, bevor Sie versuchen, die Verschlüsselung zu überprüfen, nachdem Sie eine DEP geändert haben oder wenn Sie eine DEP zum ersten Mal einem Postfach zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="e2188-405">Verwenden Sie das Cmdlet Get-MailboxStatistics, um zu ermitteln, ob ein Postfach verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="e2188-405">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="e2188-406">Die isEncrypted-Eigenschaft gibt den Wert **true** zurück, wenn das Postfach verschlüsselt ist, und der Wert **false** , wenn das Postfach nicht verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="e2188-406">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="e2188-p160">Die Zeit zum Abschließen der Postfachverschiebungen hängt von der Anzahl der Postfächer ab, denen Sie eine datenAUSFÜHRUNGSverHINDERung zum ersten Mal zuweisen, sowie der Größe der Postfächer. Wenn die Postfächer nach einer Woche ab dem Zeitpunkt, zu dem Sie die DEP zugewiesen haben, nicht verschlüsselt wurden, initiieren Sie mithilfe des Cmdlets New-MoveRequest eine Postfachverschiebung für die unverschlüsselten Postfächer.</span><span class="sxs-lookup"><span data-stu-id="e2188-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="e2188-409">Office 365: Einrichten des Kunden Schlüssels für SharePoint Online und OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="e2188-409">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="e2188-410"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-410"></span></span>

<span data-ttu-id="e2188-p161">Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Aufgaben zum Einrichten von Azure Key Vault abgeschlossen haben. Weitere Informationen finden Sie unter [Complete Tasks in Azure Key Vault und Microsoft für den Kundenschlüssel](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="e2188-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="e2188-413">Zum Einrichten des Kunden Schlüssels für SharePoint Online und OneDrive for Business müssen Sie diese Schritte ausführen, indem Sie Remote eine Verbindung mit SharePoint Online mit Windows PowerShell herstellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-413">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="e2188-414">Erstellen Sie eine Daten Verschlüsselungsrichtlinie (DEP) für jede SharePoint Online-und OneDrive for Business-Geo</span><span class="sxs-lookup"><span data-stu-id="e2188-414">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="e2188-415"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-415"></span></span>

<span data-ttu-id="e2188-p162">Eine DEP ist mit einem Schlüsselsatz verknüpft, der in Azure Key Vault gespeichert ist. Sie wenden eine DEP auf alle Daten an einem geografischen Standort an. Wenn Sie das Multi-Geo-Feature von Office 365 (derzeit in der Vorschau) verwenden, können Sie eine DEP pro Geo erstellen. Wenn Sie nicht Multi-Geo verwenden, können Sie eine datenAUSFÜHRUNGSverHINDERung in Office 365 für die Verwendung mit SharePoint Online und OneDrive for Business erstellen. Office 365 verwendet dann die Schlüssel, die in der DEP identifiziert wurden, um Ihre Daten in dieser Geo zu verschlüsseln. Zum Erstellen der datenAUSFÜHRUNGSverHINDERung benötigen Sie die wichtigsten Vault-URIs, die Sie zuvor abgerufen haben. Anweisungen dazu finden Sie unter [Abrufen des URIs für jeden Azure Key Vault-Schlüssel](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="e2188-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="e2188-p163">Denken Sie daran! Wenn Sie eine DEP erstellen, geben Sie zwei Schlüssel an, die sich in zwei verschiedenen Azure-Schlüsseldepots befinden. Stellen Sie sicher, dass sich diese Schlüssel in zwei getrennten Azure-Regionen befinden, um die Geo-Redundanz sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="e2188-426">Zum Erstellen einer datenAUSFÜHRUNGSverHINDERung müssen Sie mithilfe von Windows PowerShell eine Remoteverbindung mit SharePoint Online herstellen.</span><span class="sxs-lookup"><span data-stu-id="e2188-426">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="e2188-427">Stellen Sie auf Ihrem lokalen Computer über ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation eine [Verbindung mit SharePoint Online PowerShell her](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2188-427">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="e2188-428">Führen Sie in der Microsoft SharePoint Online-Verwaltungsshell das Cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-428">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="e2188-p164">Wenn Sie die DEP registrieren, beginnt die Verschlüsselung mit den Daten im Geo. Dies kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="e2188-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="e2188-431">Überprüfen der Verschlüsselung von Gruppen Websites, Team Websites und OneDrive für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="e2188-431">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="e2188-432"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-432"></span></span>

<span data-ttu-id="e2188-433">Sie können den Status der Verschlüsselung überprüfen, indem Sie das Cmdlet Get-SPODataEncryptionPolicy wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="e2188-433">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="e2188-434">Die Ausgabe dieses Cmdlets umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e2188-434">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="e2188-435">Der URI des Primärschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e2188-435">The URI of the primary key.</span></span>
    
- <span data-ttu-id="e2188-436">Der URI des sekundären Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="e2188-436">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="e2188-p165">Der Verschlüsselungsstatus für den Geo. Mögliche Status:</span><span class="sxs-lookup"><span data-stu-id="e2188-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="e2188-439">Nicht **registriert:** Die Kundenschlüssel Verschlüsselung wurde noch nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="e2188-439">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="e2188-p166">**Registrierung:** Die Kundenschlüssel Verschlüsselung wurde angewendet, und Ihre Dateien werden verschlüsselt. Wenn sich Ihr Geo in diesem Zustand befindet, werden Ihnen auch Informationen darüber angezeigt, wie viel Prozent der Websites in der Geo abgeschlossen sind, damit Sie den Verschlüsselungs Fortschritt überwachen können.</span><span class="sxs-lookup"><span data-stu-id="e2188-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="e2188-442">**Registriert:** Die Kundenschlüssel Verschlüsselung wurde angewendet, und alle Dateien in allen Websites wurden verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="e2188-442">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="e2188-p167">**Rolling:** Ein Schlüssel Roll wird ausgeführt. Wenn sich Ihr Geo in diesem Zustand befindet, werden Ihnen auch Informationen darüber angezeigt, wie viel Prozent der Websites den Schlüssel Rollvorgang abgeschlossen haben, damit Sie den Fortschritt überwachen können.</span><span class="sxs-lookup"><span data-stu-id="e2188-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="e2188-445">Verwalten des Kunden Schlüssels für Office 365</span><span class="sxs-lookup"><span data-stu-id="e2188-445">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="e2188-446"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-446"></span></span>

<span data-ttu-id="e2188-447">Nachdem Sie den Kundenschlüssel für Office 365 eingerichtet haben, können Sie diese zusätzlichen Verwaltungsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2188-447">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="e2188-448">Wiederherstellen von Azure Key Vault-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e2188-448">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="e2188-449">Rollen oder Drehen eines Schlüssels im Azure Key Vault, den Sie mit dem Kundenschlüssel verwenden</span><span class="sxs-lookup"><span data-stu-id="e2188-449">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="e2188-450">Verwalten von schlüsseltresor-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e2188-450">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="e2188-451">Bestimmen der einem Postfach zugewiesenen DEP</span><span class="sxs-lookup"><span data-stu-id="e2188-451">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="e2188-452">Wiederherstellen von Azure Key Vault-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e2188-452">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="e2188-453"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-453"></span></span>

<span data-ttu-id="e2188-p168">Verwenden Sie vor dem Ausführen einer Wiederherstellung die von Soft Delete bereitgestellten Wiederherstellungsfunktionen. Für alle Schlüssel, die mit dem Kundenschlüssel verwendet werden, muss das weiche löschen aktiviert sein. Soft Delete fungiert wie ein Papierkorb und ermöglicht die Wiederherstellung bis zu 90 Tage ohne Wiederherstellung. Die Wiederherstellung sollte nur unter extremen oder ungewöhnlichen Umständen erforderlich sein, beispielsweise wenn der Schlüssel-oder schlüsseltresor verloren geht. Wenn Sie einen Schlüssel zur Verwendung mit dem Kundenschlüssel wiederherstellen müssen, führen Sie in Azure PowerShell das Cmdlet Restore-AzureKeyVaultKey wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="e2188-459">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-459">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="e2188-p169">Wenn bereits ein Schlüssel mit demselben Namen im schlüsseltresor vorhanden ist, schlägt der Wiederherstellungsvorgang fehl. Restore-AzureKeyVaultKey stellt alle Schlüssel Versionen und alle Metadaten für den Schlüssel einschließlich des Schlüssel namens wieder her.</span><span class="sxs-lookup"><span data-stu-id="e2188-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="e2188-462">Rollen oder Drehen eines Schlüssels im Azure Key Vault, den Sie mit dem Kundenschlüssel verwenden</span><span class="sxs-lookup"><span data-stu-id="e2188-462">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="e2188-463"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-463"></span></span>

<span data-ttu-id="e2188-p170">Rollende Schlüssel sind weder für Azure Key Vault noch für einen Kundenschlüssel erforderlich. Außerdem sind Schlüssel, die mit einem HSM geschützt sind, nahezu unmöglich zu kompromittieren. Selbst wenn ein Stammschlüssel im Besitz eines böswilligen Akteurs war, gibt es keine Möglichkeit, diese zum Entschlüsseln von Daten zu verwenden, da nur Office 365 Code die Verwendung dieses Schlüssels weiß. Das Rollen eines Schlüssels wird jedoch vom Kundenschlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2188-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="e2188-p171">Rollen Sie nur einen Verschlüsselungsschlüssel, den Sie mit dem Kundenschlüssel verwenden, wenn ein klarer technischer Grund vorliegt oder eine Compliance-Anforderung vorschreibt, dass Sie den Schlüsselrollen müssen. Löschen Sie außerdem keine Schlüssel, die Richtlinien zugeordnet sind oder waren. Wenn Sie Ihre Schlüsselrollen, werden Inhalte mit den vorherigen Schlüsseln verschlüsselt. Wenn beispielsweise aktive Postfächer häufig erneut verschlüsselt werden, können inaktive, getrennte und deaktivierte Postfächer weiterhin mit den vorherigen Schlüsseln verschlüsselt werden. SharePoint Online führt eine Sicherung von Inhalten zu Wiederherstellungs-und Wiederherstellungszwecken aus, sodass archivierte Inhalte möglicherweise weiterhin mithilfe älterer Schlüssel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e2188-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="e2188-p172">Um die Sicherheit Ihrer Daten sicherzustellen, kann SharePoint Online nicht mehr als einen Schlüssel Roll Vorgang ausführen. Wenn Sie beide Schlüssel in einem schlüsseltresor Rollen möchten, müssen Sie warten, bis der erste Schlüssel Rollvorgang abgeschlossen ist. Unsere Empfehlung besteht darin, Ihre Key-Roll-Vorgänge in unterschiedlichen Intervallen zu staffeln, sodass dies kein Problem darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2188-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="e2188-p173">Wenn Sie einen Schlüsselrollen, fordern Sie eine neue Version eines vorhandenen Schlüssels an. Um eine neue Version eines vorhandenen Schlüssels anzufordern, verwenden Sie dasselbe Cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), mit derselben Syntax, die Sie zum Erstellen des Schlüssels verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="e2188-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="e2188-478">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-478">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="e2188-p174">In diesem Beispiel wird eine neue Schlüssel Version erstellt, da bereits ein Schlüssel mit dem Namen " **contoso-O365EX-na-VaultA1-Key001** " im **contoso-O365EX-VaultA1** -Tresor vorhanden ist. Der Vorgang fügt eine neue Schlüssel Version hinzu. Bei diesem Vorgang werden die vorherigen Schlüssel Versionen im Versionsverlauf des Schlüssels beibehalten, sodass Daten, die zuvor mit diesem Schlüssel verschlüsselt wurden, weiterhin entschlüsselt werden können. Nachdem Sie einen beliebigen Schlüssel für eine datenAUSFÜHRUNGSverHINDERung abgeschlossen haben, müssen Sie ein zusätzliches Cmdlet ausführen, um sicherzustellen, dass der Kundenschlüssel mit dem neuen Schlüssel beginnt.</span><span class="sxs-lookup"><span data-stu-id="e2188-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="e2188-483">Aktivieren von Exchange Online und Skype for Business zum Verwenden eines neuen Schlüssels nach dem Rollen oder Drehen von Schlüsseln in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="e2188-483">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="e2188-484">Wenn Sie einen der Azure Key Vault-Schlüssel für eine datenAUSFÜHRUNGSverHINDERung mit Exchange Online und Skype for Business verwenden, müssen Sie den folgenden Befehl ausführen, um die DEP zu aktualisieren und Office 365 zu aktivieren, um mit dem neuen Schlüssel zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e2188-484">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="e2188-485">So weisen Sie den Kundenschlüssel an, den neuen Schlüssel zum Verschlüsseln von Postfächern in Office 365 zu verwenden führen Sie das Cmdlet Set-DataEncryptionPolicy wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-485">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="e2188-p175">Innerhalb von 48 Stunden werden die mit dieser Richtlinie verschlüsselten aktiven Postfächer dem aktualisierten Schlüssel zugeordnet. Gehen Sie folgendermaßen vor, um den Wert für die DataEncryptionPolicyID-Eigenschaft für das Postfach zu überprüfen. [](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) Der Wert für diese Eigenschaft ändert sich, nachdem der aktualisierte Schlüssel angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e2188-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="e2188-489">Aktivieren von SharePoint Online und OneDrive for Business zum Verwenden eines neuen Schlüssels nach dem Rollen oder Drehen von Schlüsseln in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="e2188-489">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="e2188-490">Wenn Sie einen der Azure Key Vault-Schlüssel für eine datenAUSFÜHRUNGSverHINDERung in SharePoint Online und OneDrive for Business verwenden, müssen Sie das [Update-SPODataEncryptionPolicy-](https://technet.microsoft.com/library/mt843948.aspx) Cmdlet ausführen, um die DEP zu aktualisieren und Office 365 zu aktivieren, um mit dem neuen Schlüssel zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e2188-490">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="e2188-p176">Dadurch wird der Schlüssel Roll-Vorgang für SharePoint Online und OneDrive for Business gestartet. Diese Aktion ist nicht sofort. Führen Sie zum Anzeigen des Fortschritts des Schlüssels Roll-Vorgangs das Cmdlet Get-SPODataEncryptionPolicy wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e2188-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="e2188-494">Verwalten von schlüsseltresor-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e2188-494">Manage key vault permissions</span></span>
<span data-ttu-id="e2188-495"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-495"></span></span>

<span data-ttu-id="e2188-p177">Es stehen mehrere Cmdlets zur Verfügung, mit denen Sie wichtige Vault-Berechtigungen anzeigen und gegebenenfalls entfernen können. Möglicherweise müssen Sie Berechtigungen entfernen, beispielsweise wenn ein Mitarbeiter das Team verlässt.</span><span class="sxs-lookup"><span data-stu-id="e2188-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="e2188-498">Führen Sie das Cmdlet Get-AzureRmKeyVault aus, um die schlüsseltresor-Berechtigungen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="e2188-498">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="e2188-499">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-499">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="e2188-500">Führen Sie das Cmdlet Remove-AzureRmKeyVaultAccessPolicy aus, um die Berechtigungen eines Administrators zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="e2188-500">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="e2188-501">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2188-501">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="e2188-502">Bestimmen der einem Postfach zugewiesenen DEP</span><span class="sxs-lookup"><span data-stu-id="e2188-502">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="e2188-503"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="e2188-503"></span></span>

<span data-ttu-id="e2188-p178">Verwenden Sie das Cmdlet Get-MailboxStatistics, um die einem Postfach zugewiesene DEP zu bestimmen. Das Cmdlet gibt einen eindeutigen Bezeichner (GUID) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2188-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="e2188-p179">Wobei *GeneralMailboxOrMailUserIdParameter* ein Postfach angibt. Weitere Informationen zum Cmdlet Get-MailboxStatistics finden Sie unter [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2188-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="e2188-508">Verwenden Sie die GUID, um den Anzeigenamen der DEP zu ermitteln, dem das Postfach zugewiesen wird, indem Sie das folgende Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2188-508">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="e2188-509">Dabei ist *GUID* die GUID, die vom Get-MailboxStatistics-Cmdlet im vorherigen Schritt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e2188-509">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  


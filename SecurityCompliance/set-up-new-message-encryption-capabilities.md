---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Neue Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren, kann Ihre Organisation geschützte e-Mail-Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation verwenden. Die neuen OM-Funktionen funktionieren mit anderen Office 365-Organisationen, Outlook.com, Gmail und anderen e-Mail-Diensten.
ms.openlocfilehash: fd237e537aa1ff961d2d975b3b30f4a51744ba7c
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479651"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="4f1a9-104">Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4f1a9-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="4f1a9-105">Mit den neuen Funktionen von Office 365 Message Encryption (OM) können Organisationen geschützte e-Mails für alle Benutzer auf einem beliebigen Gerät freigeben.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="4f1a9-106">Benutzer können geschützte Nachrichten mit anderen Office 365-Organisationen und nicht-Office 365-Kunden mithilfe von Outlook.com, Gmail und anderen e-Mail-Diensten austauschen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>


>[!NOTE]
><span data-ttu-id="4f1a9-107">Dieser Artikel richtet sich an Administratoren und IT-Experten.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-107">This article is intended for administrators and IT professionals.</span></span> <span data-ttu-id="4f1a9-108">Wenn Sie ein Endbenutzer sind, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) für entsprechende Lösungen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-108">If you're an end-user, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) for appropriate solutions.</span></span>

<span data-ttu-id="4f1a9-109">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die neuen OM-Funktionen in Ihrem Office 365-Mandanten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-109">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 tenant.</span></span>

## <a name="verify-azure-rights-management-arm-is-active"></a><span data-ttu-id="4f1a9-110">Überprüfen der Azure-Rechteverwaltung (ARM) ist aktiv</span><span class="sxs-lookup"><span data-stu-id="4f1a9-110">Verify Azure Rights Management (ARM) is active</span></span>

>[!NOTE]
><span data-ttu-id="4f1a9-111">Die neuen OM-Funktionen nutzen die Schutzfunktionen von [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), die von [Azure Rights Management (Arm)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-111">The new OME capabilities leverage the protection features in [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span></span>

<span data-ttu-id="4f1a9-112">Die einzige Voraussetzung für die Verwendung der neuen OM-Funktionen ist, dass [Azure Rights Management (Arm)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) in ihrem Office 365-Mandanten aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-112">The only prerequisite for using the new OME capabilities is that [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your Office 365 tenant.</span></span> <span data-ttu-id="4f1a9-113">Wenn dies der Fall ist, aktiviert Office 365 die neuen OM-Funktionen automatisch, und Sie müssen nichts tun.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-113">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="4f1a9-114">Der ARM wird auch automatisch für die meisten berechtigten Pläne aktiviert, daher müssen Sie in dieser Hinsicht möglicherweise nichts Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-114">ARM is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="4f1a9-115">Weitere Informationen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-115">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more.</span></span>

>[!IMPORTANT]
><span data-ttu-id="4f1a9-116">Wenn Sie Active Directory-Rechteverwaltungsdienst (AD RMS) mit Exchange Online verwenden, müssen Sie [zu Azure Information Protection migrieren](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , bevor Sie die neuen OM-Funktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-116">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="4f1a9-117">AD RMS ist nicht kompatibel mit ARM.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-117">AD RMS is not compatible with ARM.</span></span>  

<span data-ttu-id="4f1a9-118">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-118">For more, see:</span></span>

- <span data-ttu-id="4f1a9-119">[Welche Abonnements benötige ich, um die neuen OM-Funktionen verwenden zu können?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) um zu überprüfen, ob Ihr Abonnementplan Azure Information Protection (einschließlich ARM) enthält.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-119">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes ARM).</span></span>
- <span data-ttu-id="4f1a9-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) für Informationen zum Erwerb eines berechtigten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-arm"></a><span data-ttu-id="4f1a9-121">Manuelles Aktivieren des Arms</span><span class="sxs-lookup"><span data-stu-id="4f1a9-121">Manually activating ARM</span></span>

<span data-ttu-id="4f1a9-122">Wenn Sie den ARM deaktiviert haben oder er aus irgendeinem Grund nicht automatisch aktiviert wurde, können Sie ihn manuell im folgenden aktivieren:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-122">If you disabled ARM, or if it was not automatically activated for any reason, you can activated it manually in the:</span></span>

- <span data-ttu-id="4f1a9-123">**Office 365 Admin Center**: Informationen zum [Aktivieren der Azure-Rechteverwaltung im Office 365 Admin Center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-123">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="4f1a9-124">**Azure-Portal**: Informationen zum [Aktivieren der Azure-Rechteverwaltung aus dem Azure-Portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-124">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="4f1a9-125">Konfigurieren der Verwaltung Ihres Azure Information Protection-Mandanten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="4f1a9-125">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="4f1a9-126">Der folgende Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-126">This is an optional step.</span></span> <span data-ttu-id="4f1a9-127">Microsoft die Verwaltung des Stammschlüssels für Azure Information Protection ist die Standardeinstellung und empfohlene bewährte Methode für die meisten Office 365-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-127">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="4f1a9-128">Wenn dies der Fall ist, müssen Sie nichts tun.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-128">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="4f1a9-129">Es gibt viele Gründe, beispielsweise Compliance-Anforderungen, die dazu führen können, dass Sie Ihren eigenen Stammschlüssel generieren und verwalten (auch bekannt als bringen Sie Ihren eigenen Schlüssel (BYOK)).</span><span class="sxs-lookup"><span data-stu-id="4f1a9-129">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="4f1a9-130">Wenn dies der Fall ist, empfehlen wir, dass Sie die erforderlichen Schritte ausführen, bevor Sie die neuen OM-Funktionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-130">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="4f1a9-131">Weitere Informationen finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-131">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="4f1a9-132">Überprüfen der neuen OM-Konfiguration in Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f1a9-132">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="4f1a9-133">Sie können überprüfen, ob Ihr Office 365-Mandant ordnungsgemäß für die Verwendung der neuen OM-Funktionen in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-133">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="4f1a9-134">Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-134">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="4f1a9-135">Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-135">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="4f1a9-136">**Beispiel**:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-136">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="4f1a9-137">Das Bereitstelleneiner Absender-e-Mail ist optional, zwingt das System jedoch, zusätzliche Prüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-137">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="4f1a9-138">Verwenden Sie die e-Mail-Adresse eines beliebigen Benutzers in Ihrem Office 365-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-138">Use the email address of any user in your Office 365 tenant.</span></span> 

     <span data-ttu-id="4f1a9-139">Ihre Ergebnisse sollten wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-139">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="4f1a9-140">Der Name Ihrer Office 365-Organisation ersetzt *contoso*.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-140">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="4f1a9-141">Die Standardvorlagen Namen können sich von den oben dargestellten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-141">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="4f1a9-142">Weitere Informationen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-142">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

3. <span data-ttu-id="4f1a9-143">Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rechteverwaltungsdienst zu trennen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-143">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="4f1a9-144">Aktualisieren von Nachrichtenfluss Regeln zur Verwendung neuer OM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4f1a9-144">Update mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="4f1a9-145">Wenn zuvor konfigurierte e- [Mail-Flussregeln zum](define-mail-flow-rules-to-encrypt-email.md) Verschlüsseln von e-Mails in ihrem Office 365-Mandanten konfiguriert sind, müssen Sie diese vorhandenen Regeln aktualisieren, um die neuen OM-Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-145">If there are previously configured [mail flow rules to encrypt email](define-mail-flow-rules-to-encrypt-email.md) in your Office 365 tenant, you need to update these existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="4f1a9-146">Bei neuen Bereitstellungen ist dieser Schritt zu diesem Zeitpunkt nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-146">For new deployments, this step is unnecessary at this stage.</span></span>   

>[!Note]
><span data-ttu-id="4f1a9-147">Nachrichtenfluss Regeln definieren die Bedingungen, unter denen e-Mail-Nachrichten verschlüsselt werden, und wann die Verschlüsselung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-147">Mail flow rules define the conditions under which email messages are encrypted, and when encryption should be removed.</span></span> <span data-ttu-id="4f1a9-148">Weitere Informationen finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1a9-148">See [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md) for more.</span></span>

<span data-ttu-id="4f1a9-149">So aktualisieren Sie vorhandene Regeln, um die neuen OM-Funktionen zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-149">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="4f1a9-150">Wechseln Sie im Office 365 Admin Center zu **Admin Center _GT_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-150">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>

2. <span data-ttu-id="4f1a9-151">Wechseln Sie im Exchange Admin Center zu **Nachrichtenfluss-_GT_-Regeln**.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-151">In the Exchange admin center, go to **Mail flow > Rules**.</span></span> 
3. <span data-ttu-id="4f1a9-152">**Führen Sie**für jede Regel Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="4f1a9-152">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="4f1a9-153">Wählen Sie **Nachrichtensicherheit ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-153">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="4f1a9-154">Wählen Sie **Office 365-Nachrichtenverschlüsselung und-Rechte Schutz anwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-154">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="4f1a9-155">Wählen Sie in der Liste eine RMS-Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-155">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="4f1a9-156">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-156">Select **Save**.</span></span>
    - <span data-ttu-id="4f1a9-157">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-157">Select **OK**.</span></span>
  
>[!IMPORTANT]
><span data-ttu-id="4f1a9-158">Wenn Sie keine vorhandenen Nachrichtenfluss Regeln aktualisieren, erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat verwenden, anstelle der neuen OM-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="4f1a9-158">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new OME capabilities.</span></span>

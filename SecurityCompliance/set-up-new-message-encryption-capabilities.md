---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Neue Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren, kann Ihre Organisation geschützte e-Mail-Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation verwenden. Die neuen OM-Funktionen funktionieren mit anderen Office 365-Organisationen, Outlook.com, Gmail und anderen e-Mail-Diensten.
ms.openlocfilehash: ea8756d08b1c172c433d6cd8ad1752c4c7ad64e9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260753"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="8b7d8-104">Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8b7d8-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="8b7d8-105">Mit den neuen Funktionen von Office 365 Message Encryption (OM) können Organisationen geschützte e-Mails für alle Benutzer auf einem beliebigen Gerät freigeben.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="8b7d8-106">Benutzer können geschützte Nachrichten mit anderen Office 365-Organisationen und nicht-Office 365-Kunden mithilfe von Outlook.com, Gmail und anderen e-Mail-Diensten austauschen.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="8b7d8-107">Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-107">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="8b7d8-108">Dieser Artikel richtet sich an Administratoren und IT-Experten.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-108">This article is intended for administrators and IT Pros.</span></span> <span data-ttu-id="8b7d8-109">Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-109">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

<span data-ttu-id="8b7d8-110">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die neuen OM-Funktionen in Ihrer Office 365-Organisation verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-110">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 organization.</span></span>

## <a name="verify-that-azure-rights-management-is-active"></a><span data-ttu-id="8b7d8-111">Überprüfen, ob die Azure-Rechteverwaltung aktiv ist</span><span class="sxs-lookup"><span data-stu-id="8b7d8-111">Verify that Azure Rights Management is active</span></span>

<span data-ttu-id="8b7d8-112">Die neuen OM-Funktionen nutzen die Schutzfunktionen in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), die von [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) zum Schutz von e-Mails und Dokumenten über Verschlüsselung und Zugriffssteuerung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-112">The new OME capabilities leverage the protection features in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) to protect emails and documents via encryption and access controls.</span></span>

<span data-ttu-id="8b7d8-113">Die einzige Voraussetzung für die Verwendung der neuen OM-Funktionen besteht darin, dass die [Azure-Rechteverwaltung](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) im Mandanten Ihrer Organisation aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-113">The only prerequisite for using the new OME capabilities is that [Azure Rights Management](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your organization's tenant.</span></span> <span data-ttu-id="8b7d8-114">Wenn dies der Fall ist, aktiviert Office 365 die neuen OM-Funktionen automatisch, und Sie müssen nichts tun.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-114">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="8b7d8-115">Azure RMS wird auch automatisch für die meisten berechtigten Pläne aktiviert, daher müssen Sie in dieser Hinsicht möglicherweise keine weiteren Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-115">Azure RMS is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="8b7d8-116">Weitere Informationen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-116">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more information.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8b7d8-117">Wenn Sie Active Directory-Rechteverwaltungsdienst (AD RMS) mit Exchange Online verwenden, müssen Sie [zu Azure Information Protection migrieren](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , bevor Sie die neuen OM-Funktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-117">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="8b7d8-118">OM ist nicht mit AD RMS kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-118">OME is not compatible with AD RMS.</span></span>  

<span data-ttu-id="8b7d8-119">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-119">For more information, see:</span></span>

- <span data-ttu-id="8b7d8-120">[Welche Abonnements benötige ich, um die neuen OM-Funktionen verwenden zu können?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) So überprüfen Sie, ob Ihr Abonnementplan Azure Information Protection (einschließlich Azure RMS-Funktionalität) enthält.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-120">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes Azure RMS functionality).</span></span>
- <span data-ttu-id="8b7d8-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) für Informationen zum Erwerb eines berechtigten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-azure-rights-management"></a><span data-ttu-id="8b7d8-122">Manuelles Aktivieren der Azure-Rechteverwaltung</span><span class="sxs-lookup"><span data-stu-id="8b7d8-122">Manually activating Azure Rights Management</span></span>

<span data-ttu-id="8b7d8-123">Wenn Sie Azure RMS deaktiviert haben oder wenn es aus irgendeinem Grund nicht automatisch aktiviert wurde, können Sie es manuell im folgenden aktivieren:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-123">If you disabled Azure RMS, or if it was not automatically activated for any reason, you can activate it manually in the:</span></span>

- <span data-ttu-id="8b7d8-124">**Office 365 Admin Center**: Informationen zum [Aktivieren der Azure-Rechteverwaltung im Office 365 Admin Center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-124">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="8b7d8-125">**Azure-Portal**: Informationen zum [Aktivieren der Azure-Rechteverwaltung aus dem Azure-Portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-125">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="8b7d8-126">Konfigurieren der Verwaltung Ihres Azure Information Protection-Mandanten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8b7d8-126">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="8b7d8-127">Der folgende Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-127">This is an optional step.</span></span> <span data-ttu-id="8b7d8-128">Microsoft die Verwaltung des Stammschlüssels für Azure Information Protection ist die Standardeinstellung und empfohlene bewährte Methode für die meisten Office 365-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-128">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="8b7d8-129">Wenn dies der Fall ist, müssen Sie nichts tun.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-129">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="8b7d8-130">Es gibt viele Gründe, beispielsweise Compliance-Anforderungen, die dazu führen können, dass Sie Ihren eigenen Stammschlüssel generieren und verwalten (auch bekannt als bringen Sie Ihren eigenen Schlüssel (BYOK)).</span><span class="sxs-lookup"><span data-stu-id="8b7d8-130">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="8b7d8-131">Wenn dies der Fall ist, empfehlen wir, dass Sie die erforderlichen Schritte ausführen, bevor Sie die neuen OM-Funktionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-131">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="8b7d8-132">Weitere Informationen finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-132">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="8b7d8-133">Überprüfen der neuen OM-Konfiguration in Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b7d8-133">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="8b7d8-134">Sie können überprüfen, ob Ihr Office 365-Mandant ordnungsgemäß für die Verwendung der neuen OM-Funktionen in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-134">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="8b7d8-135">Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-135">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="8b7d8-136">Führen Sie das Cmdlet Get-IRMConfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-136">Run the Get-IRMConfiguration cmdlet.</span></span>

     <span data-ttu-id="8b7d8-137">Für den AzureRMSEnabled-Parameter sollte der Wert $True angezeigt werden, der angibt, dass om in Ihrem Mandanten konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-137">You should see a value of $True for the AzureRMSEnabled parameter, which indicates that OME is configured in your tenant.</span></span> <span data-ttu-id="8b7d8-138">Wenn dies nicht der Fall ist, verwenden Sie Set-IRMConfiguration, um den Wert von AzureRMSEnabled auf $True festzulegen, um OM zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-138">If it is not, use Set-IRMConfiguration to set the value of AzureRMSEnabled to $True to enable OME.</span></span>

3. <span data-ttu-id="8b7d8-139">Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-139">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="8b7d8-140">**Beispiel**:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-140">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="8b7d8-141">Das Bereitstelleneiner Absender-e-Mail ist optional, zwingt das System jedoch, zusätzliche Prüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-141">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="8b7d8-142">Verwenden Sie die e-Mail-Adresse eines beliebigen Benutzers in Ihrem Office 365-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-142">Use the email address of any user in your Office 365 tenant.</span></span>

     <span data-ttu-id="8b7d8-143">Ihre Ergebnisse sollten wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-143">Your results should be similar to:</span></span>

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

   - <span data-ttu-id="8b7d8-144">Der Name Ihrer Office 365-Organisation ersetzt *contoso*.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-144">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="8b7d8-145">Die Standardvorlagen Namen können sich von den oben dargestellten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-145">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="8b7d8-146">Weitere Informationen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="8b7d8-146">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

4. <span data-ttu-id="8b7d8-147">Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rechteverwaltungsdienst zu trennen.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-147">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="8b7d8-148">Nächste Schritte: Definieren von Nachrichtenfluss Regeln zur Verwendung neuer OM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8b7d8-148">Next steps: Define mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="8b7d8-149">Wenn zuvor konfigurierte e-Mail-Flussregeln zum Verschlüsseln von e-Mails in Ihrer Office 365-Organisation konfiguriert sind, müssen Sie die vorhandenen Regeln aktualisieren, um die neuen OM-Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-149">If there are previously configured mail flow rules to encrypt email in your Office 365 organization, you need to update the existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="8b7d8-150">Für neue Bereitstellungen müssen Sie neue Nachrichtenfluss Regeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-150">For new deployments, you need to create new mail flow rules.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8b7d8-151">Wenn Sie keine vorhandenen Nachrichtenfluss Regeln aktualisieren, erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat verwenden, anstelle der neuen nahtlosen OM-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-151">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new seamless OME experience.</span></span>

<span data-ttu-id="8b7d8-152">Nachrichtenfluss Regeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden sollen, sowie Bedingungen zum Entfernen dieser Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-152">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption.</span></span> <span data-ttu-id="8b7d8-153">Wenn Sie eine Aktion für eine Regel festlegen, werden alle Nachrichten, die den Regelbedingungen entsprechen, beim Senden verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-153">When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="8b7d8-154">Schritte zum Erstellen von Nachrichtenfluss Regeln für OM finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="8b7d8-154">For steps on creating mail flow rules for OME, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

<span data-ttu-id="8b7d8-155">So aktualisieren Sie vorhandene Regeln, um die neuen OM-Funktionen zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-155">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="8b7d8-156">Wechseln Sie im Office 365 Admin Center zu **Admin Center _GT_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-156">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>
2. <span data-ttu-id="8b7d8-157">Wechseln Sie im Exchange Admin Center zu **Nachrichtenfluss-_GT_-Regeln**.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-157">In the Exchange admin center, go to **Mail flow > Rules**.</span></span>
3. <span data-ttu-id="8b7d8-158">**Führen Sie**für jede Regel Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8b7d8-158">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="8b7d8-159">Wählen Sie **Nachrichtensicherheit ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-159">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="8b7d8-160">Wählen Sie **Office 365-Nachrichtenverschlüsselung und-Rechte Schutz anwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-160">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="8b7d8-161">Wählen Sie in der Liste eine RMS-Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-161">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="8b7d8-162">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-162">Select **Save**.</span></span>
    - <span data-ttu-id="8b7d8-163">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8b7d8-163">Select **OK**.</span></span>

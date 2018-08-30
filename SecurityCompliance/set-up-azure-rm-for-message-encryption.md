---
title: Einrichten der Azure-Rechteverwaltung für Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: 'Office 365 Message Encryption hängt von Microsoft Azure Rights Management (zuvor bekannt als Windows Azure Active Directory Rights Management). '
ms.openlocfilehash: 99c8de49330cf99545d28d81e0c99c2138797356
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529501"
---
# <a name="set-up-azure-rights-management-for-office-365-message-encryption"></a><span data-ttu-id="d7755-103">Einrichten der Azure-Rechteverwaltung für Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d7755-103">Set up Azure Rights Management for Office 365 Message Encryption</span></span>

<span data-ttu-id="d7755-104">In diesem Thema werden die Schritte, die Sie benötigen, denen Sie folgen, um aktivieren, und legen Sie dann von Azure Rights Management (RMS), Teil des Azure Information Protection, für die Verwendung mit Office 365 Message Encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="d7755-104">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with Office 365 Message Encryption (OME).</span></span>
  
## <a name="prerequisites-for-using-office-365-message-encryption"></a><span data-ttu-id="d7755-105">Voraussetzungen für die Verwendung der Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d7755-105">Prerequisites for using Office 365 Message Encryption</span></span>
<span data-ttu-id="d7755-106"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-106"></span></span>

<span data-ttu-id="d7755-p101">Office 365 Message Encryption (OME), einschließlich IRM, hängt von Azure-Rechteverwaltung (RMS Azure). Azure RMS ist die Protection-Technologie von Azure Information Protection verwendet. Um OME verwenden zu können, muss Office 365-Organisation ein Exchange Online oder Exchange Online Protection-Abonnement enthalten, die wiederum eine Azure Rights Management Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="d7755-p101">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="d7755-110">Wenn Sie nicht sicher was Ihr Abonnement umfasst sind, finden Sie in der Exchange Online-dienstbeschreibungen für [Nachrichtenrichtlinien, Wiederherstellung und Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7755-110">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>
    
- <span data-ttu-id="d7755-111">Wenn Sie nicht über die ein RMS Azure-Abonnement für Exchange Online oder Exchange Online Protection verfügen, müssen Sie ein Abonnement erwerben und zuerst zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7755-111">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>
    
    <span data-ttu-id="d7755-p102">Informationen zum Erwerb von ein Abonnement für Azure Rights Management finden Sie unter [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). Im nächste Abschnitt erhalten Sie Informationen zum Aktivieren von Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="d7755-p102">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>
    
- <span data-ttu-id="d7755-114">Wenn Ihnen Azure Rights Management, aber nicht für Exchange Online oder Exchange Online Protection eingerichtet, wird in diesem Artikel erläutert, wie Azure Rights Management aktivieren und dann die beschreibt der besten Möglichkeit zum Einrichten OME Azure Rights Management entwickelt.</span><span class="sxs-lookup"><span data-stu-id="d7755-114">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>
    
- <span data-ttu-id="d7755-p103">Wenn Sie bereits OME eingerichtet haben, arbeiten mit Azure-Rechteverwaltung für Exchange Online oder Exchange Online Protection, je nachdem, wie Sie es, einrichten möglicherweise Sie beginnen, OME und neuen Features sofort nutzen. In diesem Artikel wird erläutert, wie Sie ermitteln, ob Sie OME ordnungsgemäß eingerichtet haben, wie Sie vorgehen, wenn Sie das Setup ändern müssen und was geschieht, wenn Sie nicht die Installation zu ändern. Um die neuen Funktionen verwenden, müssen Sie beispielsweise Azure RMS mit OME verwenden. Sie können nicht mit einer lokalen Active Directory-RMS die neuen Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7755-p103">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>
    
## <a name="activate-azure-rights-management-for-ome-in-office-365"></a><span data-ttu-id="d7755-119">Aktivieren der Azure-Rechteverwaltung für OME in Office 365</span><span class="sxs-lookup"><span data-stu-id="d7755-119">Activate Azure Rights Management for OME in Office 365</span></span>
<span data-ttu-id="d7755-120"><a name="activatewarm"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-120"></span></span>

<span data-ttu-id="d7755-p104">Sie müssen Azure Rights Management aktivieren, damit die Benutzer in Ihrer Organisation gelten Schutz von Informationen für Nachrichten, die sie senden können, und Öffnen von Nachrichten und Dateien, die vom Dienst Azure-Rechteverwaltung geschützt sind. Anweisungen finden Sie unter [Aktivieren von Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Nachdem Sie die Aktivierung abgeschlossen haben, wird dieser Seite zurückkehren, und die Aufgaben in diesem Artikel fort.</span><span class="sxs-lookup"><span data-stu-id="d7755-p104">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="d7755-124">Richten Sie OME Azure RMS durch Vertrauenswürdige Veröffentlichungsdomänen (Vertrauenswürdige Veröffentlichungsdomänen) importieren</span><span class="sxs-lookup"><span data-stu-id="d7755-124">Set up OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>
<span data-ttu-id="d7755-125"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-125"></span></span>

<span data-ttu-id="d7755-p105">Eine vertrauenswürdige Veröffentlichungsdomäne ist eine XML-Datei, die Informationen zu Ihrer Organisation Rights Management Einstellungen enthält. Beispielsweise der TPD enthält Informationen über das lizenzgebende Serverzertifikat (SLC) zum Signieren und Verschlüsseln von Zertifikaten und Lizenzen, die URLs für Lizenzierung und Veröffentlichung verwendet, und so weiter. Importieren Sie die vertrauenswürdige Veröffentlichungsdomäne in Office 365-Organisation, mithilfe von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d7755-p105">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d7755-p106">In früheren Versionen können Sie auswählen, um Vertrauenswürdige Veröffentlichungsdomänen aus dem Active Directory-Rechteverwaltungsdienste-Dienst (AD RMS) in Office 365-Organisation zu importieren. Jedoch auf diese Weise und verhindert, dass Sie die neuen Funktionen von OME wird nicht empfohlen. Wenn Ihre Office 365-Organisation derzeit ist auf diese Weise konfiguriert haben, empfiehlt es sich, dass Sie einen Plan zum Migrieren von Ihrer lokalen Active Directory-RMS zu Cloud-basierten Azure Information Protection erstellen. Weitere Informationen finden Sie unter [Migrieren von AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Sie werden nicht die neuen OME-Funktionen verwenden, bevor Sie die Migration zu Azure Information Protection abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="d7755-p106">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span> 
  
 <span data-ttu-id="d7755-134">**So importieren Sie Vertrauenswürdige Veröffentlichungsdomänen von Azure RMS**</span><span class="sxs-lookup"><span data-stu-id="d7755-134">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="d7755-135">[Verbindung mit Exchange Online mit Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7755-135">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d7755-136">Wählen Sie die Key-sharing-URL, die Ihre Office 365-Organisation geografischen Standort entspricht:</span><span class="sxs-lookup"><span data-stu-id="d7755-136">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>
    
|<span data-ttu-id="d7755-137">**Standort**</span><span class="sxs-lookup"><span data-stu-id="d7755-137">**Location**</span></span>|<span data-ttu-id="d7755-138">**Key-sharing-URL des Speicherorts**</span><span class="sxs-lookup"><span data-stu-id="d7755-138">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7755-139">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="d7755-139">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="d7755-140">Europäische Union</span><span class="sxs-lookup"><span data-stu-id="d7755-140">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="d7755-141">Asien</span><span class="sxs-lookup"><span data-stu-id="d7755-141">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="d7755-142">Südamerika</span><span class="sxs-lookup"><span data-stu-id="d7755-142">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="d7755-143">Office 365 für Behörden (Community-Cloud der US-Regierung)</span><span class="sxs-lookup"><span data-stu-id="d7755-143">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="d7755-144">Diesen RMS-Key-sharing-Speicherort ist für Kunden vorgesehen, die Office 365 für Behörden SKUs erworben haben.</span><span class="sxs-lookup"><span data-stu-id="d7755-144">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="d7755-145">Konfigurieren Sie den Key-sharing-Speicherort, indem Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="d7755-145">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="d7755-146">Wenn Sie beispielsweise die Key-sharing-Location Ihrer Organisation befindet sich in Nordamerika zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="d7755-146">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="d7755-147">Führen Sie das Cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) , mit der Option - RMSOnline für den import der TPD aus Azure Rights Management:</span><span class="sxs-lookup"><span data-stu-id="d7755-147">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="d7755-p107">Wobei *TPDName* der Name ist, die Sie für die vertrauenswürdige Veröffentlichungsdomäne verwenden möchten. Beispielsweise "Contoso TPD Nordamerika".</span><span class="sxs-lookup"><span data-stu-id="d7755-p107">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="d7755-150">Führen Sie das Cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) um zu überprüfen, dass die Verwendung des Diensts Azure Rights Management zum Office 365-Organisation erfolgreich, wie folgt mit der Option - RMSOnline fest:</span><span class="sxs-lookup"><span data-stu-id="d7755-150">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="d7755-151">Dieses Cmdlet unter anderem überprüft die Konnektivität mit dem Dienst Azure Rights Management, downloads der TPD und ihre Gültigkeit überprüft.</span><span class="sxs-lookup"><span data-stu-id="d7755-151">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="d7755-152">Führen Sie das [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) -Cmdlet wie folgt zum Deaktivieren von Azure Rights Management-Vorlagen werden in Outlook im Web und Outlook zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="d7755-152">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="d7755-153">Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt, um Azure-Rechteverwaltung für Ihre Cloud-basierte e-Mail-Organisation aktivieren und Konfigurieren der Verwendung der Azure-Rechteverwaltung für Office 365 Message Encryption aus:</span><span class="sxs-lookup"><span data-stu-id="d7755-153">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="d7755-p108">Um sicherzustellen, dass Sie erfolgreich der TPD importiert und Azure Rights Management aktiviert haben, verwenden Sie das Cmdlet Test-IRMConfiguration, um Azure Rights Management-Funktionen zu testen. Weitere Informationen hierzu finden Sie unter "Beispiel 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7755-p108">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="d7755-156">Ich habe OME mit Active Directory-Rechteverwaltungsdienste nicht Azure Information Protection eingerichtet, was kann ich tun?</span><span class="sxs-lookup"><span data-stu-id="d7755-156">I have OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="d7755-157"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-157"></span></span>

<span data-ttu-id="d7755-p109">Sie können auch weiterhin Ihre vorhandenen Office 365 Message Encryption Mail Flow Regeln mit Active Directory Rights Management verwenden, aber Sie nicht konfigurieren oder verwenden Sie die neuen OME-Funktionen. Stattdessen müssen Sie auf Azure Information Protection migrieren. Informationen zur Migration und für Ihre Organisation Dies bedeutet finden Sie unter [Migrieren von AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="d7755-p109">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="d7755-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d7755-161">Next steps</span></span>
<span data-ttu-id="d7755-162"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-162"></span></span>

<span data-ttu-id="d7755-163">Wenn Sie Azure Rights Management-Setup abgeschlossen haben, sollten Sie die neuen OME-Funktionen zu aktivieren, finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="d7755-163">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="d7755-164">Nachdem Sie Ihre Organisation zum Verwenden der neuen OME-Funktionen eingerichtet haben, können Sie zum [Definieren von e-Mail-Flussregeln zum Schutz von e-Mail-Nachrichten mit neuen OME-Funktionen](define-mail-flow-rules-to-encrypt-email.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="d7755-164">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="d7755-165">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d7755-165">Related topics</span></span>
<span data-ttu-id="d7755-166"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="d7755-166"></span></span>

[<span data-ttu-id="d7755-167">Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="d7755-167">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="d7755-168">Technische Referenz Details über die Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="d7755-168">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="d7755-169">Was ist Azure Rights Management?</span><span class="sxs-lookup"><span data-stu-id="d7755-169">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  


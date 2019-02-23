---
title: Einrichten von Azure Rights Management für die vorherige Version der Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Die frühere Version der Office 365-Nachrichtenverschlüsselung hängt von der Microsoft Azure Rights Management (früher als Windows Azure Active Directory Rights Management bezeichnet) ab.
ms.openlocfilehash: 89b86035f57699457c86fefb49888b8428f4e01c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214375"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="294bf-103">Einrichten von Azure Rights Management für die vorherige Version der Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="294bf-103">Set up Azure Rights Management for the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="294bf-104">In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um die Azure Rights Management (RMS), ein Teil von Azure Information Protection, für die Verwendung mit der vorherigen Version von Office 365 Message Encryption (OM) zu aktivieren und anschließend einzurichten.</span><span class="sxs-lookup"><span data-stu-id="294bf-104">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with the previous version of Office 365 Message Encryption (OME).</span></span>

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a><span data-ttu-id="294bf-105">Dieser Artikel bezieht sich nur auf die frühere Version von OM.</span><span class="sxs-lookup"><span data-stu-id="294bf-105">This article only applies to the previous version of OME</span></span>
<span data-ttu-id="294bf-p101">Wenn Sie Ihre Office 365-Organisation noch nicht in die neuen OM-Funktionen verschoben haben, aber bereits OM bereitgestellt haben, beziehen sich die Informationen in diesem Artikel auf Ihre Organisation. Microsoft empfiehlt, einen Plan für die Umstellung auf die neuen Funktionen von OM zu erstellen, sobald es für Ihre Organisation sinnvoll ist. Weitere Informationen finden Sie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md). Wenn Sie mehr über die Funktionsweise der neuen Funktionen erfahren möchten, lesen Sie [Office 365-Nachrichtenverschlüsselung](ome.md). Der Rest dieses Artikels bezieht sich auf das Verhalten von OM vor der Freigabe der neuen OM-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="294bf-p101">If you haven't yet moved your Office 365 organization to the new OME capabilities, but you have already deployed OME, then the information in this article applies to your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md). If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md). The rest of this article refers to OME behavior before the release of the new OME capabilities.</span></span>

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="294bf-111">VoraussetZungen für die Verwendung der vorherigen Version von Office 365 Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="294bf-111">Prerequisites for using the previous version of Office 365 Message Encryption</span></span>
<span data-ttu-id="294bf-112"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="294bf-112"></span></span>

<span data-ttu-id="294bf-p102">Office 365 Nachrichtenverschlüsselung (OM), einschließlich IRM, hängt von Azure Rights Management (Azure RMS) ab. Azure RMS ist die Schutztechnologie, die von Azure Information Protection verwendet wird. Zur Verwendung von OM muss Ihre Office 365-Organisation ein Exchange Online-oder Exchange Online Protection-Abonnement enthalten, das wiederum ein Azure Rights Management-Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="294bf-p102">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="294bf-116">Wenn Sie nicht sicher sind, was Ihr Abonnement enthält, finden Sie in den Exchange Online-Dienstbeschreibungen für [Nachrichtenrichtlinien, Wiederherstellung und Kompatibilität](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span><span class="sxs-lookup"><span data-stu-id="294bf-116">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>

- <span data-ttu-id="294bf-117">Wenn Sie nicht über ein Azure RMS-Abonnement für Exchange Online oder Exchange Online Protection verfügen, müssen Sie ein Abonnement erwerben und es zuerst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="294bf-117">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>

    <span data-ttu-id="294bf-p103">Informationen zum Erwerb eines Abonnements für die Azure-Rechteverwaltung finden Sie unter [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). Im nächsten Abschnitt erhalten Sie Informationen zum Aktivieren der Azure-Rechteverwaltung.</span><span class="sxs-lookup"><span data-stu-id="294bf-p103">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>

- <span data-ttu-id="294bf-120">Wenn Sie über Azure Rights Management verfügen, es aber nicht für Exchange Online oder Exchange Online Protection eingerichtet ist, wird in diesem Artikel erläutert, wie Sie die Azure-Rechteverwaltung aktivieren und dann die beste Möglichkeit zum Einrichten von OM für die Verwendung der Azure-Rechteverwaltung.</span><span class="sxs-lookup"><span data-stu-id="294bf-120">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>

- <span data-ttu-id="294bf-p104">Wenn Sie bereits OM für die Zusammenarbeit mit Azure Rights Management für Exchange Online oder Exchange Online Protection eingerichtet haben, können Sie, je nachdem, wie Sie es einrichten, möglicherweise sofort mit der Verwendung von OM und den neuen Funktionen beginnen. In diesem Artikel wird erläutert, wie Sie feststellen, ob Sie "OM" ordnungsgemäß eingerichtet haben, was Sie tun müssen, wenn Sie das Setup ändern möchten und was passiert, wenn Sie das Setup nicht ändern möchten. Um die neuen Funktionen verwenden zu können, müssen Sie beispielsweise Azure RMS mit OM verwenden. Die neuen Funktionen können nicht mit einem lokalen Active Directory-RMS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="294bf-p104">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a><span data-ttu-id="294bf-125">Aktivieren der Azure-Rechteverwaltung für die frühere Version von om in Office 365</span><span class="sxs-lookup"><span data-stu-id="294bf-125">Activate Azure Rights Management for  the previous version of OME in Office 365</span></span>

<span data-ttu-id="294bf-p105">Sie müssen die Azure-Rechteverwaltung aktivieren, damit die Benutzer in Ihrer Organisation den Informationsschutz auf Nachrichten anwenden können, die Sie senden, sowie Nachrichten und Dateien öffnen, die durch den Azure Rights Management-Dienst geschützt wurden. Anweisungen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://go.microsoft.com/fwlink/p/?LinkId=525775). Nachdem Sie die Aktivierung abgeschlossen haben, kehren Sie hierhin zurück, und fahren Sie mit den Aufgaben in diesem Artikel fort.</span><span class="sxs-lookup"><span data-stu-id="294bf-p105">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="294bf-129">Einrichten der vorherigen Version von OM zur Verwendung von Azure RMS durch Importieren von vertrauenswürdigen Veröffentlichungsdomänen (vor)</span><span class="sxs-lookup"><span data-stu-id="294bf-129">Set up the previous version of OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>

<span data-ttu-id="294bf-p106">Ein TPD ist eine XML-Datei, die Informationen zu den Einstellungen für die Rechteverwaltung Ihrer Organisation enthält. Beispielsweise enthält das TPD Informationen zum Server-Lizenzgeberzertifikat (SLC), das zum Signieren und Verschlüsseln von Zertifikaten und Lizenzen verwendet wird, zu den URLs, die für die Lizenzierung und Veröffentlichung verwendet werden usw. Sie importieren das TPD mithilfe von Windows PowerShell in Ihre Office 365-Organisation.</span><span class="sxs-lookup"><span data-stu-id="294bf-p106">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="294bf-p107">Zuvor konnten Sie vor aus dem Active Directory-Rechteverwaltungsdienst (AD RMS) in Ihre Office 365-Organisation importieren. Dies verhindert jedoch, dass Sie die neuen OM-Funktionen verwenden und wird nicht empfohlen. Wenn Ihre Office 365-Organisation auf diese Weise konfiguriert ist, empfiehlt Microsoft, einen Plan für die Migration von Ihrem lokalen Active Directory-RMS zu Cloud-basierten Azure Information Protection zu erstellen. Weitere Informationen finden Sie unter [Migrieren von AD RMS zu Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Sie können die neuen OM-Funktionen erst verwenden, nachdem Sie die Migration zu Azure Information Protection abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="294bf-p107">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span>
  
 <span data-ttu-id="294bf-138">**So importieren Sie vor aus Azure RMS**</span><span class="sxs-lookup"><span data-stu-id="294bf-138">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="294bf-139">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="294bf-139">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="294bf-140">Wählen Sie die URL für die Schlüssel Freigabe aus, die dem geografischen Standort Ihrer Office 365-Organisation entspricht:</span><span class="sxs-lookup"><span data-stu-id="294bf-140">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>

|<span data-ttu-id="294bf-141">**Standort**</span><span class="sxs-lookup"><span data-stu-id="294bf-141">**Location**</span></span>|<span data-ttu-id="294bf-142">**URL für die Schlüssel Freigabeadresse**</span><span class="sxs-lookup"><span data-stu-id="294bf-142">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="294bf-143">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="294bf-143">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="294bf-144">Europäische Union</span><span class="sxs-lookup"><span data-stu-id="294bf-144">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="294bf-145">Asien</span><span class="sxs-lookup"><span data-stu-id="294bf-145">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="294bf-146">Südamerika</span><span class="sxs-lookup"><span data-stu-id="294bf-146">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="294bf-147">Office 365 für Behörden (Community-Cloud der US-Regierung)</span><span class="sxs-lookup"><span data-stu-id="294bf-147">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="294bf-148">Dieser RMS-Freigabespeicherort ist für Kunden reserviert, die Office 365 für staatliche SKUs erworben haben.</span><span class="sxs-lookup"><span data-stu-id="294bf-148">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="294bf-149">Konfigurieren Sie den Speicherort für die Schlüssel Freigabe, indem Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="294bf-149">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="294bf-150">Beispielsweise können Sie den Speicherort für die Schlüssel Freigabe konfigurieren, wenn sich Ihre Organisation in Nordamerika befindet:</span><span class="sxs-lookup"><span data-stu-id="294bf-150">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="294bf-151">Führen Sie das Cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) mit der Option-RMSOnline aus, um das TPD aus der Azure-Rechteverwaltung zu importieren:</span><span class="sxs-lookup"><span data-stu-id="294bf-151">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="294bf-p108">Dabei ist *TPDName* der Name, den Sie für die TPD verwenden möchten. Beispiel: "Contoso North American TPD".</span><span class="sxs-lookup"><span data-stu-id="294bf-p108">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="294bf-154">Führen Sie das Cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) mit der Option-RMSOnline wie folgt aus, um zu überprüfen, ob die Office 365-Organisation erfolgreich für die Verwendung des Azure Rights Management-Diensts konfiguriert wurde:</span><span class="sxs-lookup"><span data-stu-id="294bf-154">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="294bf-155">Unter anderem prüft dieses Cmdlet die Konnektivität mit dem Azure-Rechteverwaltungsdienst, lädt das TPD herunter und überprüft die Gültigkeit.</span><span class="sxs-lookup"><span data-stu-id="294bf-155">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="294bf-156">Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt aus, um die Verfügbarkeit von Azure Rights Management-Vorlagen in Outlook im Web und Outlook zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="294bf-156">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="294bf-157">Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt aus, um die Azure-Rechteverwaltung für Ihre Cloud-basierte e-Mail-Organisation zu aktivieren und für die Verwendung der Azure Rights Management für Office 365-Nachrichtenverschlüsselung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="294bf-157">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="294bf-p109">Verwenden Sie das Cmdlet Test-IRMConfiguration, um zu überprüfen, ob Sie die TPD und die Azure-Rechteverwaltung aktiviert haben, um die Azure-Rechte Verwaltungsfunktion zu testen. Weitere Informationen finden Sie unter "Beispiel 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="294bf-p109">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="294bf-160">Ich habe die frühere Version von OM mit der Active Directory-Rechteverwaltung eingerichtet, nicht mit Azure Information Protection, was kann ich tun?</span><span class="sxs-lookup"><span data-stu-id="294bf-160">I have the previous version of OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="294bf-161"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="294bf-161"></span></span>

<span data-ttu-id="294bf-p110">Sie können weiterhin Ihre vorhandenen Office 365-Nachrichten Verschlüsselungsregeln mit der Active Directory-Rechteverwaltung verwenden, aber die neuen OM-Funktionen nicht konfigurieren oder verwenden. Stattdessen müssen Sie zu Azure Information Protection migrieren. Informationen zur Migration und zur Bedeutung für Ihre Organisation finden Sie unter [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="294bf-p110">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="294bf-165">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="294bf-165">Next steps</span></span>
<span data-ttu-id="294bf-166"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="294bf-166"></span></span>

<span data-ttu-id="294bf-167">Wenn Sie das Azure Rights Management-Setup abgeschlossen haben, finden Sie weitere [Informationen unter Einrichten neuer Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="294bf-167">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="294bf-168">Nachdem Sie Ihre Organisation für die Verwendung der neuen OM-Funktionen eingerichtet haben, können Sie [Nachrichtenfluss Regeln definieren, um e-Mail-Nachrichten mit neuen OM-Funktionen zu schützen](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="294bf-168">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="294bf-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="294bf-169">Related topics</span></span>
<span data-ttu-id="294bf-170"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="294bf-170"></span></span>

[<span data-ttu-id="294bf-171">Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="294bf-171">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="294bf-172">Technische Details zur Verschlüsselung in Office 365</span><span class="sxs-lookup"><span data-stu-id="294bf-172">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="294bf-173">Was ist Azure Rights Management?</span><span class="sxs-lookup"><span data-stu-id="294bf-173">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  


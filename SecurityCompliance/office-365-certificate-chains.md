---
title: Office 365 Zertifikatketten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen über die Zertifikate müssen Sie möglicherweise in Ihre eigene Infrastruktur installieren, finden Sie unter Plan für Drittanbieter-SSL-Zertifikate für Office 365. Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.
ms.openlocfilehash: 1dcc2dc38bb8e3239a3be3983791b0c60917dc5e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529334"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="cf88f-106">Office 365 Zertifikatketten</span><span class="sxs-lookup"><span data-stu-id="cf88f-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="cf88f-p102">Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen für die Zertifikate, die Sie in Ihrer eigenen Infrastruktur installieren möchten finden Sie unter [Planen von Drittanbieter - SSL-Zertifikate für Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.</span><span class="sxs-lookup"><span data-stu-id="cf88f-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="cf88f-111">**Zertifikattyp**</span><span class="sxs-lookup"><span data-stu-id="cf88f-111">**Certificate type**</span></span>|<span data-ttu-id="cf88f-112">**P7b-download**</span><span class="sxs-lookup"><span data-stu-id="cf88f-112">**P7b download**</span></span>|<span data-ttu-id="cf88f-113">**CRL-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="cf88f-113">**CRL Endpoints**</span></span>|<span data-ttu-id="cf88f-114">**OCSP-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="cf88f-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="cf88f-115">**AIA-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="cf88f-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cf88f-116">Öffentlich vertrauenswürdige Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="cf88f-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="cf88f-117">Office 365 Root Certificate Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="cf88f-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="cf88f-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="cf88f-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="cf88f-120">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cf88f-120">N/A</span></span>  <br/> |<span data-ttu-id="cf88f-121">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cf88f-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="cf88f-122">Öffentlich vertrauenswürdigen Zertifikate Intermediate</span><span class="sxs-lookup"><span data-stu-id="cf88f-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="cf88f-123">Office 365 Intermediate Zertifikat Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="cf88f-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="cf88f-124">cdp1.Public trust.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="cf88f-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="cf88f-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="cf88f-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="cf88f-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="cf88f-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="cf88f-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="cf88f-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="cf88f-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="cf88f-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="cf88f-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="cf88f-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="cf88f-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="cf88f-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="cf88f-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="cf88f-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="cf88f-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="cf88f-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="cf88f-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="cf88f-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="cf88f-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="cf88f-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="cf88f-144">Stamm-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="cf88f-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="cf88f-145">Root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="cf88f-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="cf88f-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="cf88f-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="cf88f-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="cf88f-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="cf88f-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="cf88f-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="cf88f-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="cf88f-151">Erweitern Sie den Domänenstamm und in intermediate auf Weitere Informationen zu den Zertifikat-Anbietern finden in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="cf88f-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="cf88f-152">Office 365-Stamm Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="cf88f-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="cf88f-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="cf88f-153"></span></span>

 <span data-ttu-id="cf88f-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="cf88f-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="cf88f-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="cf88f-155">|:-----|</span></span>
|<span data-ttu-id="cf88f-156">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="cf88f-157">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-157">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-158">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-158"></span></span>|
|<span data-ttu-id="cf88f-159">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-159">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-160">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-160"></span></span>|
|<span data-ttu-id="cf88f-161">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-162">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-162"></span></span>|
|<span data-ttu-id="cf88f-163">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-164">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-164"></span></span>|
|<span data-ttu-id="cf88f-165">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-165">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-166">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-166"></span></span>|
|<span data-ttu-id="cf88f-167">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-168">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-168"></span></span>|
|<span data-ttu-id="cf88f-169">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-170">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-170"></span></span>|
|<span data-ttu-id="cf88f-171">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-172">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-172"></span></span>|
|<span data-ttu-id="cf88f-173">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-174">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-174"></span></span>|
   
 <span data-ttu-id="cf88f-175">**CNNIC STAMM**</span><span class="sxs-lookup"><span data-stu-id="cf88f-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-176">**Subject**</span></span>|
|<span data-ttu-id="cf88f-177">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-177"></span></span>|
|<span data-ttu-id="cf88f-178">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-178">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-179">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-179"></span></span>|
|<span data-ttu-id="cf88f-180">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-180">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-181">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-181"></span></span>|
|<span data-ttu-id="cf88f-182">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-183">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-183"></span></span>|
|<span data-ttu-id="cf88f-184">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-185">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-185"></span></span>|
|<span data-ttu-id="cf88f-186">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-186">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-187">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-187"></span></span>|
|<span data-ttu-id="cf88f-188">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-189">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-189"></span></span>|
|<span data-ttu-id="cf88f-190">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-191">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-191"></span></span>|
|<span data-ttu-id="cf88f-192">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-193">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-193"></span></span>|
|<span data-ttu-id="cf88f-194">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-195">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-195"></span></span>|
|<span data-ttu-id="cf88f-196">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-197">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-197"></span></span>|
   
 <span data-ttu-id="cf88f-198">**Globale Stammzertifizierungsstelle DigiCert**</span><span class="sxs-lookup"><span data-stu-id="cf88f-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-199">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-199">**Subject**</span></span>|
|<span data-ttu-id="cf88f-200">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-200"></span></span>|
|<span data-ttu-id="cf88f-201">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-201">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-202">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-202"></span></span>|
|<span data-ttu-id="cf88f-203">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-203">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-204">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-204"></span></span>|
|<span data-ttu-id="cf88f-205">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-206">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-206"></span></span>|
|<span data-ttu-id="cf88f-207">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-208">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-208"></span></span>|
|<span data-ttu-id="cf88f-209">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-209">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-210">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-210"></span></span>|
|<span data-ttu-id="cf88f-211">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-212">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-212"></span></span>|
|<span data-ttu-id="cf88f-213">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-214">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-214"></span></span>|
|<span data-ttu-id="cf88f-215">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-216">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-216"></span></span>|
|<span data-ttu-id="cf88f-217">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-218">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-218"></span></span>|
|<span data-ttu-id="cf88f-219">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-220">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-220"></span></span>|
   
 <span data-ttu-id="cf88f-221">**DigiCert besonders Assurance EV Stammzertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="cf88f-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-222">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-222">**Subject**</span></span>|
|<span data-ttu-id="cf88f-223">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-223"></span></span>|
|<span data-ttu-id="cf88f-224">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-224">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-225">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-225"></span></span>|
|<span data-ttu-id="cf88f-226">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-226">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-227">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-227"></span></span>|
|<span data-ttu-id="cf88f-228">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-229">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-229"></span></span>|
|<span data-ttu-id="cf88f-230">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-231">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-231"></span></span>|
|<span data-ttu-id="cf88f-232">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-232">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-233">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-233"></span></span>|
|<span data-ttu-id="cf88f-234">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-235">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-235"></span></span>|
|<span data-ttu-id="cf88f-236">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-237">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-237"></span></span>|
|<span data-ttu-id="cf88f-238">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-239">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-239"></span></span>|
|<span data-ttu-id="cf88f-240">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-241">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-241"></span></span>|
|<span data-ttu-id="cf88f-242">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-243">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-243"></span></span>|
   
 <span data-ttu-id="cf88f-244">**D-TRUST-Klasse 3 Stammzertifizierungsstelle 2 2009**</span><span class="sxs-lookup"><span data-stu-id="cf88f-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-245">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-245">**Subject**</span></span>|
|<span data-ttu-id="cf88f-246">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-246"></span></span>|
|<span data-ttu-id="cf88f-247">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-247">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-248">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-248"></span></span>|
|<span data-ttu-id="cf88f-249">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-249">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-250">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-250"></span></span>|
|<span data-ttu-id="cf88f-251">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-252">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-252"></span></span>|
|<span data-ttu-id="cf88f-253">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-254">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-254"></span></span>|
|<span data-ttu-id="cf88f-255">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-255">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-256">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-256"></span></span>|
|<span data-ttu-id="cf88f-257">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-258">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-258"></span></span>|
|<span data-ttu-id="cf88f-259">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-260">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-260"></span></span>|
|<span data-ttu-id="cf88f-261">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-262">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-262"></span></span>|
|<span data-ttu-id="cf88f-263">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-264">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-264"></span></span>|
|<span data-ttu-id="cf88f-265">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-265">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-266">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-266"></span></span>|
   
 <span data-ttu-id="cf88f-267">**Klasse 3-D VERTRAUENSWÜRDIGE Stammzertifizierungsstelle 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="cf88f-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-268">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-268">**Subject**</span></span>|
|<span data-ttu-id="cf88f-269">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-269"></span></span>|
|<span data-ttu-id="cf88f-270">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-270">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-271">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-271"></span></span>|
|<span data-ttu-id="cf88f-272">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-272">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-273">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-273"></span></span>|
|<span data-ttu-id="cf88f-274">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-275">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-275"></span></span>|
|<span data-ttu-id="cf88f-276">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-277">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-277"></span></span>|
|<span data-ttu-id="cf88f-278">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-278">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-279">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-279"></span></span>|
|<span data-ttu-id="cf88f-280">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-281">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-281"></span></span>|
|<span data-ttu-id="cf88f-282">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-283">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-283"></span></span>|
|<span data-ttu-id="cf88f-284">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-285">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-285"></span></span>|
|<span data-ttu-id="cf88f-286">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-287">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-287"></span></span>|
|<span data-ttu-id="cf88f-288">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-288">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-289">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-289"></span></span>|
   
 <span data-ttu-id="cf88f-290">**Sommerzeit Stammzertifizierungsstelle X3**</span><span class="sxs-lookup"><span data-stu-id="cf88f-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-291">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-291">**Subject**</span></span>|
|<span data-ttu-id="cf88f-292">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-292"></span></span>|
|<span data-ttu-id="cf88f-293">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-293">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-294">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-294"></span></span>|
|<span data-ttu-id="cf88f-295">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-295">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-296">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-296"></span></span>|
|<span data-ttu-id="cf88f-297">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-298">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-298"></span></span>|
|<span data-ttu-id="cf88f-299">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-300">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-300"></span></span>|
|<span data-ttu-id="cf88f-301">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-301">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-302">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-302"></span></span>|
|<span data-ttu-id="cf88f-303">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-304">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-304"></span></span>|
|<span data-ttu-id="cf88f-305">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-306">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-306"></span></span>|
|<span data-ttu-id="cf88f-307">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-308">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-308"></span></span>|
|<span data-ttu-id="cf88f-309">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-310">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-310"></span></span>|
   
 <span data-ttu-id="cf88f-311">**Entrust Stammzertifizierungsstelle - G2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-312">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-312">**Subject**</span></span>|
|<span data-ttu-id="cf88f-313">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-313"></span></span>|
|<span data-ttu-id="cf88f-314">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-314">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-315">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-315"></span></span>|
|<span data-ttu-id="cf88f-316">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-316">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-317">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-317"></span></span>|
|<span data-ttu-id="cf88f-318">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-319">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-319"></span></span>|
|<span data-ttu-id="cf88f-320">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-321">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-321"></span></span>|
|<span data-ttu-id="cf88f-322">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-322">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-323">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-323"></span></span>|
|<span data-ttu-id="cf88f-324">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-325">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-325"></span></span>|
|<span data-ttu-id="cf88f-326">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-327">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-327"></span></span>|
|<span data-ttu-id="cf88f-328">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-329">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-329"></span></span>|
|<span data-ttu-id="cf88f-330">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-331">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-331"></span></span>|
   
 <span data-ttu-id="cf88f-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-333">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-333">**Subject**</span></span>|
|<span data-ttu-id="cf88f-334">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-334"></span></span>|
|<span data-ttu-id="cf88f-335">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-335">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-336">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-336"></span></span>|
|<span data-ttu-id="cf88f-337">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-337">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-338">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-338"></span></span>|
|<span data-ttu-id="cf88f-339">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-340">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-340"></span></span>|
|<span data-ttu-id="cf88f-341">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-342">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-342"></span></span>|
|<span data-ttu-id="cf88f-343">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-343">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-344">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-344"></span></span>|
|<span data-ttu-id="cf88f-345">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-346">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-346"></span></span>|
|<span data-ttu-id="cf88f-347">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-348">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-348"></span></span>|
|<span data-ttu-id="cf88f-349">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-350">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-350"></span></span>|
|<span data-ttu-id="cf88f-351">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-352">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-352"></span></span>|
   
 <span data-ttu-id="cf88f-353">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="cf88f-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-354">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-354">**Subject**</span></span>|
|<span data-ttu-id="cf88f-355">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-355"></span></span>|
|<span data-ttu-id="cf88f-356">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-356">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-357">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-357"></span></span>|
|<span data-ttu-id="cf88f-358">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-358">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-359">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-359"></span></span>|
|<span data-ttu-id="cf88f-360">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-361">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-361"></span></span>|
|<span data-ttu-id="cf88f-362">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-363">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-363"></span></span>|
|<span data-ttu-id="cf88f-364">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-364">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-365">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-365"></span></span>|
|<span data-ttu-id="cf88f-366">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-367">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-367"></span></span>|
|<span data-ttu-id="cf88f-368">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-369">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-369"></span></span>|
|<span data-ttu-id="cf88f-370">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-371">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-371"></span></span>|
|<span data-ttu-id="cf88f-372">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-373">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-373"></span></span>|
|<span data-ttu-id="cf88f-374">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-375">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-375"></span></span>|
|<span data-ttu-id="cf88f-376">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-376">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-377">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-377"></span></span>|
   
 <span data-ttu-id="cf88f-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="cf88f-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-379">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-379">**Subject**</span></span>|
|<span data-ttu-id="cf88f-380">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-380"></span></span>|
|<span data-ttu-id="cf88f-381">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-381">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-382">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-382"></span></span>|
|<span data-ttu-id="cf88f-383">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-383">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-384">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-384"></span></span>|
|<span data-ttu-id="cf88f-385">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-386">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-386"></span></span>|
|<span data-ttu-id="cf88f-387">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-388">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-388"></span></span>|
|<span data-ttu-id="cf88f-389">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-389">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-390">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-390"></span></span>|
|<span data-ttu-id="cf88f-391">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-392">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-392"></span></span>|
|<span data-ttu-id="cf88f-393">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-394">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-394"></span></span>|
|<span data-ttu-id="cf88f-395">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-396">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-396"></span></span>|
|<span data-ttu-id="cf88f-397">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-398">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-398"></span></span>|
   
 <span data-ttu-id="cf88f-399">**Thawte primären Stammzertifizierungsstelle - G3**</span><span class="sxs-lookup"><span data-stu-id="cf88f-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-400">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-400">**Subject**</span></span>|
|<span data-ttu-id="cf88f-401">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-401"></span></span>|
|<span data-ttu-id="cf88f-402">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-402">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-403">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-403"></span></span>|
|<span data-ttu-id="cf88f-404">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-404">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-405">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-405"></span></span>|
|<span data-ttu-id="cf88f-406">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-407">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-407"></span></span>|
|<span data-ttu-id="cf88f-408">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-409">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-409"></span></span>|
|<span data-ttu-id="cf88f-410">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-410">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-411">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-411"></span></span>|
|<span data-ttu-id="cf88f-412">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-413">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-413"></span></span>|
|<span data-ttu-id="cf88f-414">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-415">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-415"></span></span>|
|<span data-ttu-id="cf88f-416">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-417">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-417"></span></span>|
|<span data-ttu-id="cf88f-418">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-419">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-419"></span></span>|
   
 <span data-ttu-id="cf88f-420">**VeriSign Klasse 3 öffentlichen primären Zertifizierungsstelle - G5**</span><span class="sxs-lookup"><span data-stu-id="cf88f-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-421">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-421">**Subject**</span></span>|
|<span data-ttu-id="cf88f-422">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-422"></span></span>|
|<span data-ttu-id="cf88f-423">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-423">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-424">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-424"></span></span>|
|<span data-ttu-id="cf88f-425">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-425">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-426">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-426"></span></span>|
|<span data-ttu-id="cf88f-427">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-428">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-428"></span></span>|
|<span data-ttu-id="cf88f-429">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-430">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-430"></span></span>|
|<span data-ttu-id="cf88f-431">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-431">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-432">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-432"></span></span>|
|<span data-ttu-id="cf88f-433">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-434">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-434"></span></span>|
|<span data-ttu-id="cf88f-435">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-436">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-436"></span></span>|
|<span data-ttu-id="cf88f-437">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-438">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-438"></span></span>|
|<span data-ttu-id="cf88f-439">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-440">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="cf88f-441">Office 365 Intermediate Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="cf88f-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="cf88f-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="cf88f-442"></span></span>

 <span data-ttu-id="cf88f-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="cf88f-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-444">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-444">**Subject**</span></span>|
|<span data-ttu-id="cf88f-445">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-445"></span></span>|
|<span data-ttu-id="cf88f-446">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-446">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-447">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-447"></span></span>|
|<span data-ttu-id="cf88f-448">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-448">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-449">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-449"></span></span>|
|<span data-ttu-id="cf88f-450">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-450">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-451">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-451"></span></span>|
|<span data-ttu-id="cf88f-452">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-453">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-453"></span></span>|
|<span data-ttu-id="cf88f-454">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-455">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-455"></span></span>|
|<span data-ttu-id="cf88f-456">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-456">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-457">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-457"></span></span>|
|<span data-ttu-id="cf88f-458">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-459">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-459"></span></span>|
|<span data-ttu-id="cf88f-460">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-461">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-461"></span></span>|
|<span data-ttu-id="cf88f-462">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-463">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-463"></span></span>|
|<span data-ttu-id="cf88f-464">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-465">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-465"></span></span>|
|<span data-ttu-id="cf88f-466">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-467">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-467"></span></span>|
|<span data-ttu-id="cf88f-468">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-468">**AIA URLs**</span></span>|
|<span data-ttu-id="cf88f-469">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-469"></span></span>|
|<span data-ttu-id="cf88f-470">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-470">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-471">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-471"></span></span>|
|<span data-ttu-id="cf88f-472">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-473">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-473"></span></span>|
   
 <span data-ttu-id="cf88f-474">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 2009**</span><span class="sxs-lookup"><span data-stu-id="cf88f-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-475">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-475">**Subject**</span></span>|
|<span data-ttu-id="cf88f-476">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-476"></span></span>|
|<span data-ttu-id="cf88f-477">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-477">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-478">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-478"></span></span>|
|<span data-ttu-id="cf88f-479">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="cf88f-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="cf88f-480">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-480"></span></span>|
|<span data-ttu-id="cf88f-481">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-481">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-482">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-482"></span></span>|
|<span data-ttu-id="cf88f-483">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-483">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-484">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-484"></span></span>|
|<span data-ttu-id="cf88f-485">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-486">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-486"></span></span>|
|<span data-ttu-id="cf88f-487">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-488">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-488"></span></span>|
|<span data-ttu-id="cf88f-489">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-489">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-490">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-490"></span></span>|
|<span data-ttu-id="cf88f-491">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-492">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-492"></span></span>|
|<span data-ttu-id="cf88f-493">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-494">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-494"></span></span>|
|<span data-ttu-id="cf88f-495">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-496">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-496"></span></span>|
|<span data-ttu-id="cf88f-497">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-498">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-498"></span></span>|
|<span data-ttu-id="cf88f-499">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-500">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-500"></span></span>|
|<span data-ttu-id="cf88f-501">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-501">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-502">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-502"></span></span>|
|<span data-ttu-id="cf88f-503">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-504">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-504"></span></span>|
   
 <span data-ttu-id="cf88f-505">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="cf88f-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-506">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-506">**Subject**</span></span>|
|<span data-ttu-id="cf88f-507">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-507"></span></span>|
|<span data-ttu-id="cf88f-508">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-508">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-509">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-509"></span></span>|
|<span data-ttu-id="cf88f-510">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="cf88f-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="cf88f-511">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-511"></span></span>|
|<span data-ttu-id="cf88f-512">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-512">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-513">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-513"></span></span>|
|<span data-ttu-id="cf88f-514">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-514">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-515">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-515"></span></span>|
|<span data-ttu-id="cf88f-516">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-517">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-517"></span></span>|
|<span data-ttu-id="cf88f-518">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-519">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-519"></span></span>|
|<span data-ttu-id="cf88f-520">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-520">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-521">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-521"></span></span>|
|<span data-ttu-id="cf88f-522">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-523">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-523"></span></span>|
|<span data-ttu-id="cf88f-524">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-525">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-525"></span></span>|
|<span data-ttu-id="cf88f-526">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-527">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-527"></span></span>|
|<span data-ttu-id="cf88f-528">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-529">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-529"></span></span>|
|<span data-ttu-id="cf88f-530">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-531">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-531"></span></span>|
|<span data-ttu-id="cf88f-532">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-532">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-533">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-533"></span></span>|
|<span data-ttu-id="cf88f-534">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-535">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-535"></span></span>|
   
 <span data-ttu-id="cf88f-536">**DigiCert Cloud-Dienste CA-1**</span><span class="sxs-lookup"><span data-stu-id="cf88f-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-537">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-537">**Subject**</span></span>|
|<span data-ttu-id="cf88f-538">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-538"></span></span>|
|<span data-ttu-id="cf88f-539">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-539">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-540">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-540"></span></span>|
|<span data-ttu-id="cf88f-541">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-541">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-542">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-542"></span></span>|
|<span data-ttu-id="cf88f-543">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-543">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-544">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-544"></span></span>|
|<span data-ttu-id="cf88f-545">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-546">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-546"></span></span>|
|<span data-ttu-id="cf88f-547">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-548">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-548"></span></span>|
|<span data-ttu-id="cf88f-549">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-549">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-550">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-550"></span></span>|
|<span data-ttu-id="cf88f-551">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-552">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-552"></span></span>|
|<span data-ttu-id="cf88f-553">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-554">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-554"></span></span>|
|<span data-ttu-id="cf88f-555">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-556">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-556"></span></span>|
|<span data-ttu-id="cf88f-557">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-558">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-558"></span></span>|
|<span data-ttu-id="cf88f-559">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-560">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-560"></span></span>|
|<span data-ttu-id="cf88f-561">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-561">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-562">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-562"></span></span>|
|<span data-ttu-id="cf88f-563">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-564">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-564"></span></span>|
   
 <span data-ttu-id="cf88f-565">**DigiCert SHA2 hohe Assurance Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="cf88f-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-566">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-566">**Subject**</span></span>|
|<span data-ttu-id="cf88f-567">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-567"></span></span>|
|<span data-ttu-id="cf88f-568">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-568">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-569">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-569"></span></span>|
|<span data-ttu-id="cf88f-570">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-570">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-571">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-571"></span></span>|
|<span data-ttu-id="cf88f-572">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-572">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-573">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-573"></span></span>|
|<span data-ttu-id="cf88f-574">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-575">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-575"></span></span>|
|<span data-ttu-id="cf88f-576">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-577">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-577"></span></span>|
|<span data-ttu-id="cf88f-578">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-578">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-579">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-579"></span></span>|
|<span data-ttu-id="cf88f-580">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-581">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-581"></span></span>|
|<span data-ttu-id="cf88f-582">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-583">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-583"></span></span>|
|<span data-ttu-id="cf88f-584">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-585">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-585"></span></span>|
|<span data-ttu-id="cf88f-586">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-587">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-587"></span></span>|
|<span data-ttu-id="cf88f-588">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-589">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-589"></span></span>|
|<span data-ttu-id="cf88f-590">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-590">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-591">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-591"></span></span>|
|<span data-ttu-id="cf88f-592">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-593">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-593"></span></span>|
   
 <span data-ttu-id="cf88f-594">**DigiCert SHA2 sicheren Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="cf88f-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-595">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-595">**Subject**</span></span>|
|<span data-ttu-id="cf88f-596">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-596"></span></span>|
|<span data-ttu-id="cf88f-597">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-597">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-598">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-598"></span></span>|
|<span data-ttu-id="cf88f-599">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-599">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-600">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-600"></span></span>|
|<span data-ttu-id="cf88f-601">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-601">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-602">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-602"></span></span>|
|<span data-ttu-id="cf88f-603">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-604">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-604"></span></span>|
|<span data-ttu-id="cf88f-605">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-606">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-606"></span></span>|
|<span data-ttu-id="cf88f-607">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-607">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-608">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-608"></span></span>|
|<span data-ttu-id="cf88f-609">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-610">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-610"></span></span>|
|<span data-ttu-id="cf88f-611">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-612">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-612"></span></span>|
|<span data-ttu-id="cf88f-613">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-614">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-614"></span></span>|
|<span data-ttu-id="cf88f-615">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-616">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-616"></span></span>|
|<span data-ttu-id="cf88f-617">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-618">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-618"></span></span>|
|<span data-ttu-id="cf88f-619">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-619">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-620">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-620"></span></span>|
|<span data-ttu-id="cf88f-621">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-622">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-622"></span></span>|
   
 <span data-ttu-id="cf88f-623">**Entrust Zertifizierungsstelle - L1C**</span><span class="sxs-lookup"><span data-stu-id="cf88f-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-624">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-624">**Subject**</span></span>|
|<span data-ttu-id="cf88f-625">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-625"></span></span>|
|<span data-ttu-id="cf88f-626">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-626">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-627">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-627"></span></span>|
|<span data-ttu-id="cf88f-628">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-628">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-629">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-629"></span></span>|
|<span data-ttu-id="cf88f-630">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-630">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-631">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-631"></span></span>|
|<span data-ttu-id="cf88f-632">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-633">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-633"></span></span>|
|<span data-ttu-id="cf88f-634">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-635">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-635"></span></span>|
|<span data-ttu-id="cf88f-636">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-636">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-637">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-637"></span></span>|
|<span data-ttu-id="cf88f-638">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-639">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-639"></span></span>|
|<span data-ttu-id="cf88f-640">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-641">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-641"></span></span>|
|<span data-ttu-id="cf88f-642">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-643">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-643"></span></span>|
|<span data-ttu-id="cf88f-644">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-645">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-645"></span></span>|
|<span data-ttu-id="cf88f-646">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-647">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-647"></span></span>|
|<span data-ttu-id="cf88f-648">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-648">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-649">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-649"></span></span>|
|<span data-ttu-id="cf88f-650">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-651">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-651"></span></span>|
   
 <span data-ttu-id="cf88f-652">**Entrust Zertifizierungsstelle - L1K**</span><span class="sxs-lookup"><span data-stu-id="cf88f-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-653">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-653">**Subject**</span></span>|
|<span data-ttu-id="cf88f-654">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-654"></span></span>|
|<span data-ttu-id="cf88f-655">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-655">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-656">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-656"></span></span>|
|<span data-ttu-id="cf88f-657">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-657">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-658">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-658"></span></span>|
|<span data-ttu-id="cf88f-659">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-659">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-660">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-660"></span></span>|
|<span data-ttu-id="cf88f-661">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-662">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-662"></span></span>|
|<span data-ttu-id="cf88f-663">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-664">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-664"></span></span>|
|<span data-ttu-id="cf88f-665">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-665">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-666">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-666"></span></span>|
|<span data-ttu-id="cf88f-667">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-668">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-668"></span></span>|
|<span data-ttu-id="cf88f-669">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-670">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-670"></span></span>|
|<span data-ttu-id="cf88f-671">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-672">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-672"></span></span>|
|<span data-ttu-id="cf88f-673">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-674">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-674"></span></span>|
|<span data-ttu-id="cf88f-675">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-676">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-676"></span></span>|
|<span data-ttu-id="cf88f-677">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-677">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-678">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-678"></span></span>|
|<span data-ttu-id="cf88f-679">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-680">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-680"></span></span>|
   
 <span data-ttu-id="cf88f-681">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="cf88f-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-682">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-682">**Subject**</span></span>|
|<span data-ttu-id="cf88f-683">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-683"></span></span>|
|<span data-ttu-id="cf88f-684">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-684">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-685">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-685"></span></span>|
|<span data-ttu-id="cf88f-686">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-686">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-687">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-687"></span></span>|
|<span data-ttu-id="cf88f-688">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-688">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-689">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-689"></span></span>|
|<span data-ttu-id="cf88f-690">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-691">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-691"></span></span>|
|<span data-ttu-id="cf88f-692">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-693">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-693"></span></span>|
|<span data-ttu-id="cf88f-694">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-694">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-695">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-695"></span></span>|
|<span data-ttu-id="cf88f-696">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-697">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-697"></span></span>|
|<span data-ttu-id="cf88f-698">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-699">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-699"></span></span>|
|<span data-ttu-id="cf88f-700">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-701">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-701"></span></span>|
|<span data-ttu-id="cf88f-702">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-703">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-703"></span></span>|
|<span data-ttu-id="cf88f-704">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-705">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-705"></span></span>|
|<span data-ttu-id="cf88f-706">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-706">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-707">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-707"></span></span>|
|<span data-ttu-id="cf88f-708">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-709">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-709"></span></span>|
   
 <span data-ttu-id="cf88f-710">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G2 Informationen**</span><span class="sxs-lookup"><span data-stu-id="cf88f-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-711">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-711">**Subject**</span></span>|
|<span data-ttu-id="cf88f-712">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-712"></span></span>|
|<span data-ttu-id="cf88f-713">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-713">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-714">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-714"></span></span>|
|<span data-ttu-id="cf88f-715">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-715">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-716">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-716"></span></span>|
|<span data-ttu-id="cf88f-717">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-717">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-718">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-718"></span></span>|
|<span data-ttu-id="cf88f-719">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-720">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-720"></span></span>|
|<span data-ttu-id="cf88f-721">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-722">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-722"></span></span>|
|<span data-ttu-id="cf88f-723">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-723">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-724">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-724"></span></span>|
|<span data-ttu-id="cf88f-725">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-726">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-726"></span></span>|
|<span data-ttu-id="cf88f-727">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-728">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-728"></span></span>|
|<span data-ttu-id="cf88f-729">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-730">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-730"></span></span>|
|<span data-ttu-id="cf88f-731">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-732">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-732"></span></span>|
|<span data-ttu-id="cf88f-733">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-734">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-734"></span></span>|
|<span data-ttu-id="cf88f-735">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-735">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-736">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-736"></span></span>|
|<span data-ttu-id="cf88f-737">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-738">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-738"></span></span>|
   
 <span data-ttu-id="cf88f-739">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G3 Informationen**</span><span class="sxs-lookup"><span data-stu-id="cf88f-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-740">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-740">**Subject**</span></span>|
|<span data-ttu-id="cf88f-741">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-741"></span></span>|
|<span data-ttu-id="cf88f-742">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-742">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-743">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-743"></span></span>|
|<span data-ttu-id="cf88f-744">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-744">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-745">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-745"></span></span>|
|<span data-ttu-id="cf88f-746">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-746">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-747">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-747"></span></span>|
|<span data-ttu-id="cf88f-748">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-749">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-749"></span></span>|
|<span data-ttu-id="cf88f-750">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-751">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-751"></span></span>|
|<span data-ttu-id="cf88f-752">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-752">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-753">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-753"></span></span>|
|<span data-ttu-id="cf88f-754">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-755">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-755"></span></span>|
|<span data-ttu-id="cf88f-756">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-757">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-757"></span></span>|
|<span data-ttu-id="cf88f-758">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-759">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-759"></span></span>|
|<span data-ttu-id="cf88f-760">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-761">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-761"></span></span>|
|<span data-ttu-id="cf88f-762">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-763">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-763"></span></span>|
|<span data-ttu-id="cf88f-764">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-764">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-765">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-765"></span></span>|
|<span data-ttu-id="cf88f-766">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-767">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-767"></span></span>|
   
 <span data-ttu-id="cf88f-768">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-769">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-769">**Subject**</span></span>|
|<span data-ttu-id="cf88f-770">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-770"></span></span>|
|<span data-ttu-id="cf88f-771">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-771">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-772">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-772"></span></span>|
|<span data-ttu-id="cf88f-773">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-773">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-774">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-774"></span></span>|
|<span data-ttu-id="cf88f-775">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-775">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-776">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-776"></span></span>|
|<span data-ttu-id="cf88f-777">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-778">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-778"></span></span>|
|<span data-ttu-id="cf88f-779">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-780">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-780"></span></span>|
|<span data-ttu-id="cf88f-781">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-781">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-782">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-782"></span></span>|
|<span data-ttu-id="cf88f-783">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-784">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-784"></span></span>|
|<span data-ttu-id="cf88f-785">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-786">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-786"></span></span>|
|<span data-ttu-id="cf88f-787">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-788">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-788"></span></span>|
|<span data-ttu-id="cf88f-789">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-790">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-790"></span></span>|
|<span data-ttu-id="cf88f-791">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-792">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-792"></span></span>|
|<span data-ttu-id="cf88f-793">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-793">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-794">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-794"></span></span>|
|<span data-ttu-id="cf88f-795">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-796">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-796"></span></span>|
   
 <span data-ttu-id="cf88f-797">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-798">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-798">**Subject**</span></span>|
|<span data-ttu-id="cf88f-799">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-799"></span></span>|
|<span data-ttu-id="cf88f-800">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-800">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-801">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-801"></span></span>|
|<span data-ttu-id="cf88f-802">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-802">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-803">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-803"></span></span>|
|<span data-ttu-id="cf88f-804">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-804">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-805">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-805"></span></span>|
|<span data-ttu-id="cf88f-806">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-807">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-807"></span></span>|
|<span data-ttu-id="cf88f-808">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-809">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-809"></span></span>|
|<span data-ttu-id="cf88f-810">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-810">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-811">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-811"></span></span>|
|<span data-ttu-id="cf88f-812">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-813">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-813"></span></span>|
|<span data-ttu-id="cf88f-814">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-815">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-815"></span></span>|
|<span data-ttu-id="cf88f-816">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-817">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-817"></span></span>|
|<span data-ttu-id="cf88f-818">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-819">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-819"></span></span>|
|<span data-ttu-id="cf88f-820">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-821">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-821"></span></span>|
|<span data-ttu-id="cf88f-822">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-822">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-823">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-823"></span></span>|
|<span data-ttu-id="cf88f-824">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-825">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-825"></span></span>|
   
 <span data-ttu-id="cf88f-826">**Lassen Sie uns Behörde X3 verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="cf88f-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-827">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-827">**Subject**</span></span>|
|<span data-ttu-id="cf88f-828">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-828"></span></span>|
|<span data-ttu-id="cf88f-829">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-829">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-830">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-830"></span></span>|
|<span data-ttu-id="cf88f-831">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-831">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-832">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-832"></span></span>|
|<span data-ttu-id="cf88f-833">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-833">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-834">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-834"></span></span>|
|<span data-ttu-id="cf88f-835">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-836">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-836"></span></span>|
|<span data-ttu-id="cf88f-837">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-838">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-838"></span></span>|
|<span data-ttu-id="cf88f-839">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-839">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-840">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-840"></span></span>|
|<span data-ttu-id="cf88f-841">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-842">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-842"></span></span>|
|<span data-ttu-id="cf88f-843">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-844">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-844"></span></span>|
|<span data-ttu-id="cf88f-845">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-846">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-846"></span></span>|
|<span data-ttu-id="cf88f-847">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-848">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-848"></span></span>|
|<span data-ttu-id="cf88f-849">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-850">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-850"></span></span>|
|<span data-ttu-id="cf88f-851">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-851">**AIA URLs**</span></span>|
|<span data-ttu-id="cf88f-852">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-852"></span></span>|
|<span data-ttu-id="cf88f-853">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-853">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-854">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-854"></span></span>|
|<span data-ttu-id="cf88f-855">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-856">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-856"></span></span>|
   
 <span data-ttu-id="cf88f-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-858">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-858">**Subject**</span></span>|
|<span data-ttu-id="cf88f-859">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-859"></span></span>|
|<span data-ttu-id="cf88f-860">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-860">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-861">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-861"></span></span>|
|<span data-ttu-id="cf88f-862">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-862">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-863">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-863"></span></span>|
|<span data-ttu-id="cf88f-864">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-864">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-865">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-865"></span></span>|
|<span data-ttu-id="cf88f-866">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-867">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-867"></span></span>|
|<span data-ttu-id="cf88f-868">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-869">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-869"></span></span>|
|<span data-ttu-id="cf88f-870">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-870">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-871">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-871"></span></span>|
|<span data-ttu-id="cf88f-872">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-873">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-873"></span></span>|
|<span data-ttu-id="cf88f-874">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-875">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-875"></span></span>|
|<span data-ttu-id="cf88f-876">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-877">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-877"></span></span>|
|<span data-ttu-id="cf88f-878">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-879">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-879"></span></span>|
|<span data-ttu-id="cf88f-880">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-881">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-881"></span></span>|
|<span data-ttu-id="cf88f-882">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-882">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-883">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-883"></span></span>|
   
 <span data-ttu-id="cf88f-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-885">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-885">**Subject**</span></span>|
|<span data-ttu-id="cf88f-886">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-886"></span></span>|
|<span data-ttu-id="cf88f-887">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-887">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-888">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-888"></span></span>|
|<span data-ttu-id="cf88f-889">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-889">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-890">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-890"></span></span>|
|<span data-ttu-id="cf88f-891">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-891">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-892">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-892"></span></span>|
|<span data-ttu-id="cf88f-893">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-894">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-894"></span></span>|
|<span data-ttu-id="cf88f-895">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-896">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-896"></span></span>|
|<span data-ttu-id="cf88f-897">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-897">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-898">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-898"></span></span>|
|<span data-ttu-id="cf88f-899">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-900">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-900"></span></span>|
|<span data-ttu-id="cf88f-901">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-902">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-902"></span></span>|
|<span data-ttu-id="cf88f-903">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-904">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-904"></span></span>|
|<span data-ttu-id="cf88f-905">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-906">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-906"></span></span>|
|<span data-ttu-id="cf88f-907">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-908">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-908"></span></span>|
|<span data-ttu-id="cf88f-909">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-909">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-910">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-910"></span></span>|
|<span data-ttu-id="cf88f-911">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-912">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-912"></span></span>|
   
 <span data-ttu-id="cf88f-913">**Microsoft IT TLS Zertifizierungsstelle 1**</span><span class="sxs-lookup"><span data-stu-id="cf88f-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-914">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-914">**Subject**</span></span>|
|<span data-ttu-id="cf88f-915">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-915"></span></span>|
|<span data-ttu-id="cf88f-916">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-916">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-917">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-917"></span></span>|
|<span data-ttu-id="cf88f-918">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-918">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-919">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-919"></span></span>|
|<span data-ttu-id="cf88f-920">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-920">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-921">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-921"></span></span>|
|<span data-ttu-id="cf88f-922">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-923">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-923"></span></span>|
|<span data-ttu-id="cf88f-924">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-925">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-925"></span></span>|
|<span data-ttu-id="cf88f-926">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-926">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-927">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-927"></span></span>|
|<span data-ttu-id="cf88f-928">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-929">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-929"></span></span>|
|<span data-ttu-id="cf88f-930">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-931">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-931"></span></span>|
|<span data-ttu-id="cf88f-932">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-933">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-933"></span></span>|
|<span data-ttu-id="cf88f-934">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-935">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-935"></span></span>|
|<span data-ttu-id="cf88f-936">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-937">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-937"></span></span>|
|<span data-ttu-id="cf88f-938">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-938">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-939">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-939"></span></span>|
|<span data-ttu-id="cf88f-940">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-941">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-941"></span></span>|
   
 <span data-ttu-id="cf88f-942">**Microsoft IT TLS Zertifizierungsstelle 2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-943">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-943">**Subject**</span></span>|
|<span data-ttu-id="cf88f-944">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-944"></span></span>|
|<span data-ttu-id="cf88f-945">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-945">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-946">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-946"></span></span>|
|<span data-ttu-id="cf88f-947">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-947">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-948">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-948"></span></span>|
|<span data-ttu-id="cf88f-949">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-949">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-950">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-950"></span></span>|
|<span data-ttu-id="cf88f-951">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-952">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-952"></span></span>|
|<span data-ttu-id="cf88f-953">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-954">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-954"></span></span>|
|<span data-ttu-id="cf88f-955">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-955">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-956">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-956"></span></span>|
|<span data-ttu-id="cf88f-957">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-958">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-958"></span></span>|
|<span data-ttu-id="cf88f-959">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-960">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-960"></span></span>|
|<span data-ttu-id="cf88f-961">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-962">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-962"></span></span>|
|<span data-ttu-id="cf88f-963">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-964">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-964"></span></span>|
|<span data-ttu-id="cf88f-965">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-966">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-966"></span></span>|
|<span data-ttu-id="cf88f-967">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-967">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-968">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-968"></span></span>|
|<span data-ttu-id="cf88f-969">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-970">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-970"></span></span>|
   
 <span data-ttu-id="cf88f-971">**Microsoft IT TLS Zertifizierungsstelle 4**</span><span class="sxs-lookup"><span data-stu-id="cf88f-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-972">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-972">**Subject**</span></span>|
|<span data-ttu-id="cf88f-973">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-973"></span></span>|
|<span data-ttu-id="cf88f-974">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-974">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-975">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-975"></span></span>|
|<span data-ttu-id="cf88f-976">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-976">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-977">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-977"></span></span>|
|<span data-ttu-id="cf88f-978">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-978">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-979">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-979"></span></span>|
|<span data-ttu-id="cf88f-980">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-981">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-981"></span></span>|
|<span data-ttu-id="cf88f-982">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-983">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-983"></span></span>|
|<span data-ttu-id="cf88f-984">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-984">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-985">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-985"></span></span>|
|<span data-ttu-id="cf88f-986">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-987">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-987"></span></span>|
|<span data-ttu-id="cf88f-988">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-989">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-989"></span></span>|
|<span data-ttu-id="cf88f-990">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-991">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-991"></span></span>|
|<span data-ttu-id="cf88f-992">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-993">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-993"></span></span>|
|<span data-ttu-id="cf88f-994">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-995">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-995"></span></span>|
|<span data-ttu-id="cf88f-996">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-996">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-997">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-997"></span></span>|
|<span data-ttu-id="cf88f-998">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-999">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-999"></span></span>|
   
 <span data-ttu-id="cf88f-1000">**Microsoft IT TLS Zertifizierungsstelle 5**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-1001">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1001">**Subject**</span></span>|
|<span data-ttu-id="cf88f-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1002"></span></span>|
|<span data-ttu-id="cf88f-1003">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1003">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1004"></span></span>|
|<span data-ttu-id="cf88f-1005">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1005">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1006"></span></span>|
|<span data-ttu-id="cf88f-1007">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1008"></span></span>|
|<span data-ttu-id="cf88f-1009">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1010"></span></span>|
|<span data-ttu-id="cf88f-1011">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1012"></span></span>|
|<span data-ttu-id="cf88f-1013">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1014"></span></span>|
|<span data-ttu-id="cf88f-1015">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1016"></span></span>|
|<span data-ttu-id="cf88f-1017">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1018"></span></span>|
|<span data-ttu-id="cf88f-1019">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1020"></span></span>|
|<span data-ttu-id="cf88f-1021">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1022"></span></span>|
|<span data-ttu-id="cf88f-1023">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1024"></span></span>|
|<span data-ttu-id="cf88f-1025">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1026"></span></span>|
|<span data-ttu-id="cf88f-1027">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1028"></span></span>|
   
 <span data-ttu-id="cf88f-1029">**Symantec Klasse 3 EV SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-1030">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1030">**Subject**</span></span>|
|<span data-ttu-id="cf88f-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1031"></span></span>|
|<span data-ttu-id="cf88f-1032">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1032">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1033"></span></span>|
|<span data-ttu-id="cf88f-1034">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="cf88f-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1035"></span></span>|
|<span data-ttu-id="cf88f-1036">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1036">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1037"></span></span>|
|<span data-ttu-id="cf88f-1038">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1039"></span></span>|
|<span data-ttu-id="cf88f-1040">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1041"></span></span>|
|<span data-ttu-id="cf88f-1042">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1043"></span></span>|
|<span data-ttu-id="cf88f-1044">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1045"></span></span>|
|<span data-ttu-id="cf88f-1046">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1047"></span></span>|
|<span data-ttu-id="cf88f-1048">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1049"></span></span>|
|<span data-ttu-id="cf88f-1050">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1051"></span></span>|
|<span data-ttu-id="cf88f-1052">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1053"></span></span>|
|<span data-ttu-id="cf88f-1054">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1055"></span></span>|
|<span data-ttu-id="cf88f-1056">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1057"></span></span>|
|<span data-ttu-id="cf88f-1058">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1059"></span></span>|
   
 <span data-ttu-id="cf88f-1060">**Symantec Klasse 3 sicheren Server CA - G4**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-1061">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1061">**Subject**</span></span>|
|<span data-ttu-id="cf88f-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1062"></span></span>|
|<span data-ttu-id="cf88f-1063">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1063">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1064"></span></span>|
|<span data-ttu-id="cf88f-1065">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="cf88f-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1066"></span></span>|
|<span data-ttu-id="cf88f-1067">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1067">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1068"></span></span>|
|<span data-ttu-id="cf88f-1069">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1070"></span></span>|
|<span data-ttu-id="cf88f-1071">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1072"></span></span>|
|<span data-ttu-id="cf88f-1073">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1074"></span></span>|
|<span data-ttu-id="cf88f-1075">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1076"></span></span>|
|<span data-ttu-id="cf88f-1077">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1078"></span></span>|
|<span data-ttu-id="cf88f-1079">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1080"></span></span>|
|<span data-ttu-id="cf88f-1081">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1082"></span></span>|
|<span data-ttu-id="cf88f-1083">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1084"></span></span>|
|<span data-ttu-id="cf88f-1085">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1086"></span></span>|
|<span data-ttu-id="cf88f-1087">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1088"></span></span>|
|<span data-ttu-id="cf88f-1089">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1090"></span></span>|
   
 <span data-ttu-id="cf88f-1091">**Thawte SHA256-SSL-Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-1092">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1092">**Subject**</span></span>|
|<span data-ttu-id="cf88f-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1093"></span></span>|
|<span data-ttu-id="cf88f-1094">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1094">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1095"></span></span>|
|<span data-ttu-id="cf88f-1096">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="cf88f-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1097"></span></span>|
|<span data-ttu-id="cf88f-1098">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1098">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1099"></span></span>|
|<span data-ttu-id="cf88f-1100">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1101"></span></span>|
|<span data-ttu-id="cf88f-1102">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1103"></span></span>|
|<span data-ttu-id="cf88f-1104">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1105"></span></span>|
|<span data-ttu-id="cf88f-1106">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1107"></span></span>|
|<span data-ttu-id="cf88f-1108">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1109"></span></span>|
|<span data-ttu-id="cf88f-1110">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1111"></span></span>|
|<span data-ttu-id="cf88f-1112">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1113"></span></span>|
|<span data-ttu-id="cf88f-1114">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1115"></span></span>|
|<span data-ttu-id="cf88f-1116">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1117"></span></span>|
|<span data-ttu-id="cf88f-1118">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1119"></span></span>|
|<span data-ttu-id="cf88f-1120">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1121"></span></span>|
   
 <span data-ttu-id="cf88f-1122">**Verizon Akamai SureServer Zertifizierungsstelle G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="cf88f-1123">**Subject**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1123">**Subject**</span></span>|
|<span data-ttu-id="cf88f-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1124"></span></span>|
|<span data-ttu-id="cf88f-1125">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1125">**Issuer**</span></span>|
|<span data-ttu-id="cf88f-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1126"></span></span>|
|<span data-ttu-id="cf88f-1127">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1127">**Serial Number**</span></span>|
|<span data-ttu-id="cf88f-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1128"></span></span>|
|<span data-ttu-id="cf88f-1129">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="cf88f-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1130"></span></span>|
|<span data-ttu-id="cf88f-1131">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="cf88f-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1132"></span></span>|
|<span data-ttu-id="cf88f-1133">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="cf88f-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1134"></span></span>|
|<span data-ttu-id="cf88f-1135">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="cf88f-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1136"></span></span>|
|<span data-ttu-id="cf88f-1137">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1138"></span></span>|
|<span data-ttu-id="cf88f-1139">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="cf88f-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1140"></span></span>|
|<span data-ttu-id="cf88f-1141">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="cf88f-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1142"></span></span>|
|<span data-ttu-id="cf88f-1143">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1144"></span></span>|
|<span data-ttu-id="cf88f-1145">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="cf88f-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1146"></span></span>|
|<span data-ttu-id="cf88f-1147">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="cf88f-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1148"></span></span>|
|<span data-ttu-id="cf88f-1149">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="cf88f-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1150"></span></span>|
|<span data-ttu-id="cf88f-1151">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="cf88f-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="cf88f-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="cf88f-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="cf88f-1153">Weiteres Zertifikat Pfade</span><span class="sxs-lookup"><span data-stu-id="cf88f-1153">Additional certificate paths</span></span>
<span data-ttu-id="cf88f-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="cf88f-1154"></span></span>

<span data-ttu-id="cf88f-1155">Folgendes umfassen legacy Zertifikate, die sind nicht über enthalten und mit der obigen Liste über einen Zeitraum zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cf88f-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
```
evsecure-aia.verisign.com
sa.symcb.com
sd.symcb.com
*.omniroot.com
*.verisign.com
*.symcb.com
*.symcd.com
*.verisign.net
*.geotrust.com
*.entrust.net
*.public-trust.com
EVIntl-ocsp.verisign.com
EVSecure-ocsp.verisign.com
isrg.trustid.ocsp.identrust.com
ocsp.digicert.com
ocsp.entrust.net
ocsp.globalsign.com/ExtendedSSLSHA256CACross
ocsp.globalsign.com/rootr1
ocsp.globalsign.com/rootr2
ocsp2.globalsign.com/rootr3
ocsp.int-x3.letsencrypt.org/
ocsp.msocsp.com
ocsp.omniroot.com/baltimoreroot
ocsp2.globalsign.com/gsextendvalsha2g3r3
ocsp2.globalsign.com/gsorganizationvalsha2g2
ocsp2.globalsign.com/gsorganizationvalsha2g3
ocsp2.globalsign.com/rootr3
ocspx.digicert.com
s2.symcb.com
sr.symcd.com
su.symcd.com
vassg142.ocsp.omniroot.com
cdp1.public-trust.com/CRL/Omniroot2025.crl
crl.entrust.net/2048ca.crl
crl.entrust.net/g2ca.crl
crl.entrust.net/level1k.crl
crl.entrust.net/rootca1.crl
crl.globalsign.com/gs/gsextendvalsha2g3r3.crl
crl.globalsign.com/gs/gsorganizationvalsha2g2.crl
crl.globalsign.com/gsorganizationvalsha2g3.crl
crl.globalsign.com/root.crl
crl.globalsign.net/root-r2.crl
crl.globalsign.com/root-r3.crl
crl.globalsign.net/root.crl
crl.identrust.com/DSTROOTCAX3CRL.crl
crl.microsoft.com/pki/mscorp/crl/msitwww1.crl
crl.microsoft.com/pki/mscorp/crl/msitwww2.crl
crl3.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl3.digicert.com/DigiCertGlobalRootCA.crl
crl3.digicert.com/sha2-ev-server-g1.crl
crl3.digicert.com/sha2-ha-server-g5.crl
crl3.digicert.com/ssca-sha2-g5.crl
crl4.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl4.digicert.com/DigiCertGlobalRootCA.crl
crl4.digicert.com/DigiCertHighAssuranceEVRootCA.crl
crl4.digicert.com/sha2-ev-server-g1.crl
crl4.digicert.com/sha2-ha-server-g5.crl
crl4.digicert.com/ssca-sha2-g5.crl
EVIntl-crl.verisign.com/EVIntl2006.crl
EVSecure-crl.verisign.com/pca3-g5.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww1.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww2.crl
s1.symcb.com/pca3-g5.crl
sr.symcb.com/sr.crl
su.symcb.com/su.crl
vassg142.crl.omniroot.com/vassg142.crl
aia.entrust.net/l1k-chain256.cer
apps.identrust.com/roots/dstrootcax3.p7c
https://cacert.a.omniroot.com/vassg142.crt
https://cacert.a.omniroot.com/vassg142.der
https://cacert.omniroot.com/baltimoreroot.crt
https://cacert.omniroot.com/baltimoreroot.der
cacerts.digicert.com/DigiCertCloudServicesCA-1.crt
cacerts.digicert.com/DigiCertSHA2ExtendedValidationServerCA.crt
cacerts.digicert.com/DigiCertSHA2HighAssuranceServerCA.crt
cacerts.digicert.com/DigiCertSHA2SecureServerCA.crt
cert.int-x3.letsencrypt.org/
EVIntl-aia.verisign.com/EVIntl2006.cer
secure.globalsign.com/cacert/gsextendvalsha2g2r2.crt
secure.globalsign.com/cacert/gsextendvalsha2g3r3.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g2r1.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g3.crt
sr.symcb.com/sr.crt
su.symcb.com/su.crt
https://www.digicert.com/CACerts/DigiCertGlobalRootCA.crt
https://www.digicert.com/CACerts/DigiCertHighAssuranceEVRootCA.crt
www.microsoft.com/pki/mscorp/msitwww1.crt
www.microsoft.com/pki/mscorp/msitwww2.crt

```



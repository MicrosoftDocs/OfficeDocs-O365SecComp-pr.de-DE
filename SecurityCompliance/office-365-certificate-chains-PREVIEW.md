---
title: Office 365 Zertifikatketten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen über die Zertifikate müssen Sie möglicherweise in Ihre eigene Infrastruktur installieren, finden Sie unter Plan für Drittanbieter-SSL-Zertifikate für Office 365. Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.
ms.openlocfilehash: 97e00833e57f8f6b7352650b0efdef51ddba77fa
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575359"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="be458-106">Office 365 Zertifikatketten</span><span class="sxs-lookup"><span data-stu-id="be458-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="be458-p102">Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen für die Zertifikate, die Sie in Ihrer eigenen Infrastruktur installieren möchten finden Sie unter [Planen von Drittanbieter - SSL-Zertifikate für Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.</span><span class="sxs-lookup"><span data-stu-id="be458-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="be458-111">**Zertifikattyp**</span><span class="sxs-lookup"><span data-stu-id="be458-111">**Certificate type**</span></span>|<span data-ttu-id="be458-112">**P7b-download**</span><span class="sxs-lookup"><span data-stu-id="be458-112">**P7b download**</span></span>|<span data-ttu-id="be458-113">**CRL-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="be458-113">**CRL Endpoints**</span></span>|<span data-ttu-id="be458-114">**OCSP-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="be458-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="be458-115">**AIA-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="be458-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="be458-116">Öffentlich vertrauenswürdige Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="be458-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="be458-117">Office 365 Root Certificate Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="be458-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="be458-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="be458-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="be458-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="be458-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="be458-120">n. v.</span><span class="sxs-lookup"><span data-stu-id="be458-120">N/A</span></span>  <br/> |<span data-ttu-id="be458-121">n. v.</span><span class="sxs-lookup"><span data-stu-id="be458-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="be458-122">Öffentlich vertrauenswürdigen Zertifikate Intermediate</span><span class="sxs-lookup"><span data-stu-id="be458-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="be458-123">Office 365 Intermediate Zertifikat Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="be458-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="be458-124">cdp1.Public trust.com</span><span class="sxs-lookup"><span data-stu-id="be458-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="be458-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="be458-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="be458-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="be458-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="be458-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="be458-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="be458-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="be458-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="be458-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="be458-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="be458-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="be458-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="be458-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="be458-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="be458-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="be458-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="be458-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="be458-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="be458-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="be458-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="be458-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="be458-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="be458-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="be458-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="be458-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="be458-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="be458-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="be458-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="be458-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="be458-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="be458-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="be458-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="be458-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="be458-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="be458-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="be458-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="be458-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="be458-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="be458-144">Stamm-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="be458-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="be458-145">Root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="be458-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="be458-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="be458-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="be458-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="be458-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="be458-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="be458-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="be458-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="be458-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="be458-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="be458-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="be458-151">Erweitern Sie den Domänenstamm und in intermediate auf Weitere Informationen zu den Zertifikat-Anbietern finden in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="be458-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="be458-152">Office 365-Stamm Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="be458-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="be458-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="be458-153"></span></span>

 <span data-ttu-id="be458-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="be458-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="be458-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="be458-155">|:-----|</span></span>
|<span data-ttu-id="be458-156">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="be458-157">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-157">**Serial Number**</span></span>|
|<span data-ttu-id="be458-158">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-158"></span></span>|
|<span data-ttu-id="be458-159">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-159">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-160">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-160"></span></span>|
|<span data-ttu-id="be458-161">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-162">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-162"></span></span>|
|<span data-ttu-id="be458-163">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-164">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-164"></span></span>|
|<span data-ttu-id="be458-165">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-165">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-166">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-166"></span></span>|
|<span data-ttu-id="be458-167">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-168">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-168"></span></span>|
|<span data-ttu-id="be458-169">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-170">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-170"></span></span>|
|<span data-ttu-id="be458-171">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-172">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-172"></span></span>|
|<span data-ttu-id="be458-173">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-174">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-174"></span></span>|
   
 <span data-ttu-id="be458-175">**CNNIC STAMM**</span><span class="sxs-lookup"><span data-stu-id="be458-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-176">**Subject**</span></span>|
|<span data-ttu-id="be458-177">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-177"></span></span>|
|<span data-ttu-id="be458-178">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-178">**Serial Number**</span></span>|
|<span data-ttu-id="be458-179">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-179"></span></span>|
|<span data-ttu-id="be458-180">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-180">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-181">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-181"></span></span>|
|<span data-ttu-id="be458-182">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-183">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-183"></span></span>|
|<span data-ttu-id="be458-184">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-185">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-185"></span></span>|
|<span data-ttu-id="be458-186">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-186">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-187">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-187"></span></span>|
|<span data-ttu-id="be458-188">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-189">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-189"></span></span>|
|<span data-ttu-id="be458-190">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-191">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-191"></span></span>|
|<span data-ttu-id="be458-192">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-193">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-193"></span></span>|
|<span data-ttu-id="be458-194">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-195">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-195"></span></span>|
|<span data-ttu-id="be458-196">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-197">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-197"></span></span>|
   
 <span data-ttu-id="be458-198">**Globale Stammzertifizierungsstelle DigiCert**</span><span class="sxs-lookup"><span data-stu-id="be458-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-199">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-199">**Subject**</span></span>|
|<span data-ttu-id="be458-200">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-200"></span></span>|
|<span data-ttu-id="be458-201">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-201">**Serial Number**</span></span>|
|<span data-ttu-id="be458-202">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-202"></span></span>|
|<span data-ttu-id="be458-203">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-203">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-204">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-204"></span></span>|
|<span data-ttu-id="be458-205">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-206">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-206"></span></span>|
|<span data-ttu-id="be458-207">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-208">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-208"></span></span>|
|<span data-ttu-id="be458-209">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-209">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-210">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-210"></span></span>|
|<span data-ttu-id="be458-211">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-212">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-212"></span></span>|
|<span data-ttu-id="be458-213">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-214">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-214"></span></span>|
|<span data-ttu-id="be458-215">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-216">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-216"></span></span>|
|<span data-ttu-id="be458-217">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-218">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-218"></span></span>|
|<span data-ttu-id="be458-219">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-220">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-220"></span></span>|
   
 <span data-ttu-id="be458-221">**DigiCert besonders Assurance EV Stammzertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="be458-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-222">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-222">**Subject**</span></span>|
|<span data-ttu-id="be458-223">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-223"></span></span>|
|<span data-ttu-id="be458-224">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-224">**Serial Number**</span></span>|
|<span data-ttu-id="be458-225">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-225"></span></span>|
|<span data-ttu-id="be458-226">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-226">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-227">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-227"></span></span>|
|<span data-ttu-id="be458-228">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-229">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-229"></span></span>|
|<span data-ttu-id="be458-230">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-231">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-231"></span></span>|
|<span data-ttu-id="be458-232">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-232">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-233">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-233"></span></span>|
|<span data-ttu-id="be458-234">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-235">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-235"></span></span>|
|<span data-ttu-id="be458-236">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-237">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-237"></span></span>|
|<span data-ttu-id="be458-238">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-239">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-239"></span></span>|
|<span data-ttu-id="be458-240">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-241">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-241"></span></span>|
|<span data-ttu-id="be458-242">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-243">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-243"></span></span>|
   
 <span data-ttu-id="be458-244">**D-TRUST-Klasse 3 Stammzertifizierungsstelle 2 2009**</span><span class="sxs-lookup"><span data-stu-id="be458-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-245">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-245">**Subject**</span></span>|
|<span data-ttu-id="be458-246">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-246"></span></span>|
|<span data-ttu-id="be458-247">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-247">**Serial Number**</span></span>|
|<span data-ttu-id="be458-248">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-248"></span></span>|
|<span data-ttu-id="be458-249">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-249">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-250">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-250"></span></span>|
|<span data-ttu-id="be458-251">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-252">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-252"></span></span>|
|<span data-ttu-id="be458-253">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-254">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-254"></span></span>|
|<span data-ttu-id="be458-255">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-255">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-256">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-256"></span></span>|
|<span data-ttu-id="be458-257">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-258">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-258"></span></span>|
|<span data-ttu-id="be458-259">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-260">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-260"></span></span>|
|<span data-ttu-id="be458-261">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-262">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-262"></span></span>|
|<span data-ttu-id="be458-263">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-264">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-264"></span></span>|
|<span data-ttu-id="be458-265">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-265">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-266">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-266"></span></span>|
   
 <span data-ttu-id="be458-267">**Klasse 3-D VERTRAUENSWÜRDIGE Stammzertifizierungsstelle 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="be458-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-268">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-268">**Subject**</span></span>|
|<span data-ttu-id="be458-269">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-269"></span></span>|
|<span data-ttu-id="be458-270">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-270">**Serial Number**</span></span>|
|<span data-ttu-id="be458-271">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-271"></span></span>|
|<span data-ttu-id="be458-272">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-272">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-273">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-273"></span></span>|
|<span data-ttu-id="be458-274">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-275">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-275"></span></span>|
|<span data-ttu-id="be458-276">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-277">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-277"></span></span>|
|<span data-ttu-id="be458-278">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-278">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-279">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-279"></span></span>|
|<span data-ttu-id="be458-280">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-281">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-281"></span></span>|
|<span data-ttu-id="be458-282">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-283">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-283"></span></span>|
|<span data-ttu-id="be458-284">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-285">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-285"></span></span>|
|<span data-ttu-id="be458-286">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-287">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-287"></span></span>|
|<span data-ttu-id="be458-288">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-288">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-289">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-289"></span></span>|
   
 <span data-ttu-id="be458-290">**Sommerzeit Stammzertifizierungsstelle X3**</span><span class="sxs-lookup"><span data-stu-id="be458-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-291">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-291">**Subject**</span></span>|
|<span data-ttu-id="be458-292">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-292"></span></span>|
|<span data-ttu-id="be458-293">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-293">**Serial Number**</span></span>|
|<span data-ttu-id="be458-294">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-294"></span></span>|
|<span data-ttu-id="be458-295">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-295">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-296">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-296"></span></span>|
|<span data-ttu-id="be458-297">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-298">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-298"></span></span>|
|<span data-ttu-id="be458-299">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-300">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-300"></span></span>|
|<span data-ttu-id="be458-301">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-301">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-302">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-302"></span></span>|
|<span data-ttu-id="be458-303">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-304">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-304"></span></span>|
|<span data-ttu-id="be458-305">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-306">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-306"></span></span>|
|<span data-ttu-id="be458-307">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-308">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-308"></span></span>|
|<span data-ttu-id="be458-309">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-310">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-310"></span></span>|
   
 <span data-ttu-id="be458-311">**Entrust Stammzertifizierungsstelle - G2**</span><span class="sxs-lookup"><span data-stu-id="be458-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-312">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-312">**Subject**</span></span>|
|<span data-ttu-id="be458-313">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-313"></span></span>|
|<span data-ttu-id="be458-314">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-314">**Serial Number**</span></span>|
|<span data-ttu-id="be458-315">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-315"></span></span>|
|<span data-ttu-id="be458-316">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-316">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-317">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-317"></span></span>|
|<span data-ttu-id="be458-318">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-319">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-319"></span></span>|
|<span data-ttu-id="be458-320">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-321">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-321"></span></span>|
|<span data-ttu-id="be458-322">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-322">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-323">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-323"></span></span>|
|<span data-ttu-id="be458-324">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-325">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-325"></span></span>|
|<span data-ttu-id="be458-326">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-327">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-327"></span></span>|
|<span data-ttu-id="be458-328">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-329">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-329"></span></span>|
|<span data-ttu-id="be458-330">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-331">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-331"></span></span>|
   
 <span data-ttu-id="be458-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="be458-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-333">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-333">**Subject**</span></span>|
|<span data-ttu-id="be458-334">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-334"></span></span>|
|<span data-ttu-id="be458-335">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-335">**Serial Number**</span></span>|
|<span data-ttu-id="be458-336">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-336"></span></span>|
|<span data-ttu-id="be458-337">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-337">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-338">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-338"></span></span>|
|<span data-ttu-id="be458-339">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-340">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-340"></span></span>|
|<span data-ttu-id="be458-341">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-342">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-342"></span></span>|
|<span data-ttu-id="be458-343">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-343">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-344">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-344"></span></span>|
|<span data-ttu-id="be458-345">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-346">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-346"></span></span>|
|<span data-ttu-id="be458-347">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-348">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-348"></span></span>|
|<span data-ttu-id="be458-349">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-350">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-350"></span></span>|
|<span data-ttu-id="be458-351">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-352">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-352"></span></span>|
   
 <span data-ttu-id="be458-353">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="be458-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-354">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-354">**Subject**</span></span>|
|<span data-ttu-id="be458-355">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-355"></span></span>|
|<span data-ttu-id="be458-356">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-356">**Serial Number**</span></span>|
|<span data-ttu-id="be458-357">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-357"></span></span>|
|<span data-ttu-id="be458-358">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-358">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-359">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-359"></span></span>|
|<span data-ttu-id="be458-360">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-361">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-361"></span></span>|
|<span data-ttu-id="be458-362">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-363">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-363"></span></span>|
|<span data-ttu-id="be458-364">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-364">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-365">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-365"></span></span>|
|<span data-ttu-id="be458-366">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-367">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-367"></span></span>|
|<span data-ttu-id="be458-368">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-369">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-369"></span></span>|
|<span data-ttu-id="be458-370">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-371">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-371"></span></span>|
|<span data-ttu-id="be458-372">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-373">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-373"></span></span>|
|<span data-ttu-id="be458-374">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-375">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-375"></span></span>|
|<span data-ttu-id="be458-376">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-376">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-377">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-377"></span></span>|
   
 <span data-ttu-id="be458-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="be458-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-379">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-379">**Subject**</span></span>|
|<span data-ttu-id="be458-380">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-380"></span></span>|
|<span data-ttu-id="be458-381">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-381">**Serial Number**</span></span>|
|<span data-ttu-id="be458-382">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-382"></span></span>|
|<span data-ttu-id="be458-383">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-383">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-384">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-384"></span></span>|
|<span data-ttu-id="be458-385">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-386">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-386"></span></span>|
|<span data-ttu-id="be458-387">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-388">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-388"></span></span>|
|<span data-ttu-id="be458-389">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-389">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-390">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-390"></span></span>|
|<span data-ttu-id="be458-391">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-392">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-392"></span></span>|
|<span data-ttu-id="be458-393">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-394">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-394"></span></span>|
|<span data-ttu-id="be458-395">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-396">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-396"></span></span>|
|<span data-ttu-id="be458-397">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-398">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-398"></span></span>|
   
 <span data-ttu-id="be458-399">**Thawte primären Stammzertifizierungsstelle - G3**</span><span class="sxs-lookup"><span data-stu-id="be458-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-400">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-400">**Subject**</span></span>|
|<span data-ttu-id="be458-401">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-401"></span></span>|
|<span data-ttu-id="be458-402">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-402">**Serial Number**</span></span>|
|<span data-ttu-id="be458-403">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-403"></span></span>|
|<span data-ttu-id="be458-404">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-404">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-405">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-405"></span></span>|
|<span data-ttu-id="be458-406">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-407">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-407"></span></span>|
|<span data-ttu-id="be458-408">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-409">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-409"></span></span>|
|<span data-ttu-id="be458-410">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-410">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-411">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-411"></span></span>|
|<span data-ttu-id="be458-412">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-413">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-413"></span></span>|
|<span data-ttu-id="be458-414">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-415">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-415"></span></span>|
|<span data-ttu-id="be458-416">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-417">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-417"></span></span>|
|<span data-ttu-id="be458-418">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-419">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-419"></span></span>|
   
 <span data-ttu-id="be458-420">**VeriSign Klasse 3 öffentlichen primären Zertifizierungsstelle - G5**</span><span class="sxs-lookup"><span data-stu-id="be458-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-421">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-421">**Subject**</span></span>|
|<span data-ttu-id="be458-422">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-422"></span></span>|
|<span data-ttu-id="be458-423">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-423">**Serial Number**</span></span>|
|<span data-ttu-id="be458-424">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-424"></span></span>|
|<span data-ttu-id="be458-425">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-425">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-426">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-426"></span></span>|
|<span data-ttu-id="be458-427">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-428">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-428"></span></span>|
|<span data-ttu-id="be458-429">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-430">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-430"></span></span>|
|<span data-ttu-id="be458-431">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-431">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-432">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-432"></span></span>|
|<span data-ttu-id="be458-433">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-434">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-434"></span></span>|
|<span data-ttu-id="be458-435">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-436">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-436"></span></span>|
|<span data-ttu-id="be458-437">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-438">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-438"></span></span>|
|<span data-ttu-id="be458-439">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-440">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="be458-441">Office 365 Intermediate Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="be458-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="be458-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="be458-442"></span></span>

 <span data-ttu-id="be458-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="be458-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-444">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-444">**Subject**</span></span>|
|<span data-ttu-id="be458-445">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-445"></span></span>|
|<span data-ttu-id="be458-446">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-446">**Issuer**</span></span>|
|<span data-ttu-id="be458-447">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-447"></span></span>|
|<span data-ttu-id="be458-448">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-448">**Serial Number**</span></span>|
|<span data-ttu-id="be458-449">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-449"></span></span>|
|<span data-ttu-id="be458-450">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-450">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-451">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-451"></span></span>|
|<span data-ttu-id="be458-452">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-453">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-453"></span></span>|
|<span data-ttu-id="be458-454">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-455">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-455"></span></span>|
|<span data-ttu-id="be458-456">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-456">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-457">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-457"></span></span>|
|<span data-ttu-id="be458-458">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-459">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-459"></span></span>|
|<span data-ttu-id="be458-460">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-461">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-461"></span></span>|
|<span data-ttu-id="be458-462">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-463">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-463"></span></span>|
|<span data-ttu-id="be458-464">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-465">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-465"></span></span>|
|<span data-ttu-id="be458-466">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-467">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-467"></span></span>|
|<span data-ttu-id="be458-468">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-468">**AIA URLs**</span></span>|
|<span data-ttu-id="be458-469">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-469"></span></span>|
|<span data-ttu-id="be458-470">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-470">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-471">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-471"></span></span>|
|<span data-ttu-id="be458-472">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-473">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-473"></span></span>|
   
 <span data-ttu-id="be458-474">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 2009**</span><span class="sxs-lookup"><span data-stu-id="be458-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-475">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-475">**Subject**</span></span>|
|<span data-ttu-id="be458-476">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-476"></span></span>|
|<span data-ttu-id="be458-477">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-477">**Issuer**</span></span>|
|<span data-ttu-id="be458-478">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-478"></span></span>|
|<span data-ttu-id="be458-479">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="be458-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="be458-480">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-480"></span></span>|
|<span data-ttu-id="be458-481">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-481">**Serial Number**</span></span>|
|<span data-ttu-id="be458-482">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-482"></span></span>|
|<span data-ttu-id="be458-483">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-483">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-484">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-484"></span></span>|
|<span data-ttu-id="be458-485">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-486">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-486"></span></span>|
|<span data-ttu-id="be458-487">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-488">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-488"></span></span>|
|<span data-ttu-id="be458-489">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-489">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-490">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-490"></span></span>|
|<span data-ttu-id="be458-491">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-492">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-492"></span></span>|
|<span data-ttu-id="be458-493">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-494">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-494"></span></span>|
|<span data-ttu-id="be458-495">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-496">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-496"></span></span>|
|<span data-ttu-id="be458-497">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-498">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-498"></span></span>|
|<span data-ttu-id="be458-499">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-500">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-500"></span></span>|
|<span data-ttu-id="be458-501">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-501">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-502">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-502"></span></span>|
|<span data-ttu-id="be458-503">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-504">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-504"></span></span>|
   
 <span data-ttu-id="be458-505">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="be458-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-506">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-506">**Subject**</span></span>|
|<span data-ttu-id="be458-507">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-507"></span></span>|
|<span data-ttu-id="be458-508">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-508">**Issuer**</span></span>|
|<span data-ttu-id="be458-509">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-509"></span></span>|
|<span data-ttu-id="be458-510">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="be458-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="be458-511">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-511"></span></span>|
|<span data-ttu-id="be458-512">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-512">**Serial Number**</span></span>|
|<span data-ttu-id="be458-513">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-513"></span></span>|
|<span data-ttu-id="be458-514">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-514">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-515">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-515"></span></span>|
|<span data-ttu-id="be458-516">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-517">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-517"></span></span>|
|<span data-ttu-id="be458-518">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-519">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-519"></span></span>|
|<span data-ttu-id="be458-520">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-520">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-521">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-521"></span></span>|
|<span data-ttu-id="be458-522">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-523">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-523"></span></span>|
|<span data-ttu-id="be458-524">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-525">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-525"></span></span>|
|<span data-ttu-id="be458-526">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-527">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-527"></span></span>|
|<span data-ttu-id="be458-528">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-529">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-529"></span></span>|
|<span data-ttu-id="be458-530">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-531">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-531"></span></span>|
|<span data-ttu-id="be458-532">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-532">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-533">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-533"></span></span>|
|<span data-ttu-id="be458-534">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-535">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-535"></span></span>|
   
 <span data-ttu-id="be458-536">**DigiCert Cloud-Dienste CA-1**</span><span class="sxs-lookup"><span data-stu-id="be458-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-537">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-537">**Subject**</span></span>|
|<span data-ttu-id="be458-538">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-538"></span></span>|
|<span data-ttu-id="be458-539">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-539">**Issuer**</span></span>|
|<span data-ttu-id="be458-540">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-540"></span></span>|
|<span data-ttu-id="be458-541">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-541">**Serial Number**</span></span>|
|<span data-ttu-id="be458-542">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-542"></span></span>|
|<span data-ttu-id="be458-543">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-543">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-544">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-544"></span></span>|
|<span data-ttu-id="be458-545">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-546">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-546"></span></span>|
|<span data-ttu-id="be458-547">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-548">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-548"></span></span>|
|<span data-ttu-id="be458-549">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-549">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-550">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-550"></span></span>|
|<span data-ttu-id="be458-551">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-552">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-552"></span></span>|
|<span data-ttu-id="be458-553">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-554">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-554"></span></span>|
|<span data-ttu-id="be458-555">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-556">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-556"></span></span>|
|<span data-ttu-id="be458-557">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-558">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-558"></span></span>|
|<span data-ttu-id="be458-559">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-560">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-560"></span></span>|
|<span data-ttu-id="be458-561">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-561">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-562">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-562"></span></span>|
|<span data-ttu-id="be458-563">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-564">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-564"></span></span>|
   
 <span data-ttu-id="be458-565">**DigiCert SHA2 hohe Assurance Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="be458-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-566">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-566">**Subject**</span></span>|
|<span data-ttu-id="be458-567">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-567"></span></span>|
|<span data-ttu-id="be458-568">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-568">**Issuer**</span></span>|
|<span data-ttu-id="be458-569">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-569"></span></span>|
|<span data-ttu-id="be458-570">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-570">**Serial Number**</span></span>|
|<span data-ttu-id="be458-571">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-571"></span></span>|
|<span data-ttu-id="be458-572">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-572">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-573">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-573"></span></span>|
|<span data-ttu-id="be458-574">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-575">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-575"></span></span>|
|<span data-ttu-id="be458-576">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-577">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-577"></span></span>|
|<span data-ttu-id="be458-578">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-578">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-579">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-579"></span></span>|
|<span data-ttu-id="be458-580">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-581">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-581"></span></span>|
|<span data-ttu-id="be458-582">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-583">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-583"></span></span>|
|<span data-ttu-id="be458-584">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-585">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-585"></span></span>|
|<span data-ttu-id="be458-586">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-587">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-587"></span></span>|
|<span data-ttu-id="be458-588">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-589">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-589"></span></span>|
|<span data-ttu-id="be458-590">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-590">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-591">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-591"></span></span>|
|<span data-ttu-id="be458-592">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-593">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-593"></span></span>|
   
 <span data-ttu-id="be458-594">**DigiCert SHA2 sicheren Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="be458-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-595">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-595">**Subject**</span></span>|
|<span data-ttu-id="be458-596">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-596"></span></span>|
|<span data-ttu-id="be458-597">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-597">**Issuer**</span></span>|
|<span data-ttu-id="be458-598">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-598"></span></span>|
|<span data-ttu-id="be458-599">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-599">**Serial Number**</span></span>|
|<span data-ttu-id="be458-600">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-600"></span></span>|
|<span data-ttu-id="be458-601">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-601">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-602">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-602"></span></span>|
|<span data-ttu-id="be458-603">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-604">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-604"></span></span>|
|<span data-ttu-id="be458-605">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-606">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-606"></span></span>|
|<span data-ttu-id="be458-607">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-607">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-608">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-608"></span></span>|
|<span data-ttu-id="be458-609">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-610">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-610"></span></span>|
|<span data-ttu-id="be458-611">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-612">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-612"></span></span>|
|<span data-ttu-id="be458-613">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-614">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-614"></span></span>|
|<span data-ttu-id="be458-615">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-616">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-616"></span></span>|
|<span data-ttu-id="be458-617">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-618">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-618"></span></span>|
|<span data-ttu-id="be458-619">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-619">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-620">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-620"></span></span>|
|<span data-ttu-id="be458-621">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-622">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-622"></span></span>|
   
 <span data-ttu-id="be458-623">**Entrust Zertifizierungsstelle - L1C**</span><span class="sxs-lookup"><span data-stu-id="be458-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-624">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-624">**Subject**</span></span>|
|<span data-ttu-id="be458-625">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-625"></span></span>|
|<span data-ttu-id="be458-626">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-626">**Issuer**</span></span>|
|<span data-ttu-id="be458-627">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-627"></span></span>|
|<span data-ttu-id="be458-628">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-628">**Serial Number**</span></span>|
|<span data-ttu-id="be458-629">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-629"></span></span>|
|<span data-ttu-id="be458-630">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-630">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-631">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-631"></span></span>|
|<span data-ttu-id="be458-632">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-633">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-633"></span></span>|
|<span data-ttu-id="be458-634">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-635">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-635"></span></span>|
|<span data-ttu-id="be458-636">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-636">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-637">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-637"></span></span>|
|<span data-ttu-id="be458-638">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-639">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-639"></span></span>|
|<span data-ttu-id="be458-640">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-641">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-641"></span></span>|
|<span data-ttu-id="be458-642">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-643">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-643"></span></span>|
|<span data-ttu-id="be458-644">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-645">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-645"></span></span>|
|<span data-ttu-id="be458-646">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-647">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-647"></span></span>|
|<span data-ttu-id="be458-648">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-648">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-649">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-649"></span></span>|
|<span data-ttu-id="be458-650">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-651">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-651"></span></span>|
   
 <span data-ttu-id="be458-652">**Entrust Zertifizierungsstelle - L1K**</span><span class="sxs-lookup"><span data-stu-id="be458-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-653">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-653">**Subject**</span></span>|
|<span data-ttu-id="be458-654">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-654"></span></span>|
|<span data-ttu-id="be458-655">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-655">**Issuer**</span></span>|
|<span data-ttu-id="be458-656">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-656"></span></span>|
|<span data-ttu-id="be458-657">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-657">**Serial Number**</span></span>|
|<span data-ttu-id="be458-658">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-658"></span></span>|
|<span data-ttu-id="be458-659">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-659">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-660">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-660"></span></span>|
|<span data-ttu-id="be458-661">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-662">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-662"></span></span>|
|<span data-ttu-id="be458-663">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-664">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-664"></span></span>|
|<span data-ttu-id="be458-665">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-665">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-666">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-666"></span></span>|
|<span data-ttu-id="be458-667">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-668">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-668"></span></span>|
|<span data-ttu-id="be458-669">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-670">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-670"></span></span>|
|<span data-ttu-id="be458-671">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-672">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-672"></span></span>|
|<span data-ttu-id="be458-673">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-674">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-674"></span></span>|
|<span data-ttu-id="be458-675">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-676">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-676"></span></span>|
|<span data-ttu-id="be458-677">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-677">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-678">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-678"></span></span>|
|<span data-ttu-id="be458-679">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-680">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-680"></span></span>|
   
 <span data-ttu-id="be458-681">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="be458-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-682">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-682">**Subject**</span></span>|
|<span data-ttu-id="be458-683">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-683"></span></span>|
|<span data-ttu-id="be458-684">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-684">**Issuer**</span></span>|
|<span data-ttu-id="be458-685">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-685"></span></span>|
|<span data-ttu-id="be458-686">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-686">**Serial Number**</span></span>|
|<span data-ttu-id="be458-687">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-687"></span></span>|
|<span data-ttu-id="be458-688">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-688">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-689">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-689"></span></span>|
|<span data-ttu-id="be458-690">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-691">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-691"></span></span>|
|<span data-ttu-id="be458-692">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-693">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-693"></span></span>|
|<span data-ttu-id="be458-694">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-694">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-695">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-695"></span></span>|
|<span data-ttu-id="be458-696">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-697">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-697"></span></span>|
|<span data-ttu-id="be458-698">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-699">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-699"></span></span>|
|<span data-ttu-id="be458-700">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-701">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-701"></span></span>|
|<span data-ttu-id="be458-702">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-703">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-703"></span></span>|
|<span data-ttu-id="be458-704">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-705">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-705"></span></span>|
|<span data-ttu-id="be458-706">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-706">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-707">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-707"></span></span>|
|<span data-ttu-id="be458-708">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-709">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-709"></span></span>|
   
 <span data-ttu-id="be458-710">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G2 Informationen**</span><span class="sxs-lookup"><span data-stu-id="be458-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-711">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-711">**Subject**</span></span>|
|<span data-ttu-id="be458-712">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-712"></span></span>|
|<span data-ttu-id="be458-713">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-713">**Issuer**</span></span>|
|<span data-ttu-id="be458-714">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-714"></span></span>|
|<span data-ttu-id="be458-715">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-715">**Serial Number**</span></span>|
|<span data-ttu-id="be458-716">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-716"></span></span>|
|<span data-ttu-id="be458-717">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-717">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-718">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-718"></span></span>|
|<span data-ttu-id="be458-719">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-720">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-720"></span></span>|
|<span data-ttu-id="be458-721">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-722">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-722"></span></span>|
|<span data-ttu-id="be458-723">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-723">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-724">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-724"></span></span>|
|<span data-ttu-id="be458-725">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-726">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-726"></span></span>|
|<span data-ttu-id="be458-727">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-728">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-728"></span></span>|
|<span data-ttu-id="be458-729">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-730">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-730"></span></span>|
|<span data-ttu-id="be458-731">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-732">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-732"></span></span>|
|<span data-ttu-id="be458-733">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-734">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-734"></span></span>|
|<span data-ttu-id="be458-735">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-735">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-736">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-736"></span></span>|
|<span data-ttu-id="be458-737">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-738">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-738"></span></span>|
   
 <span data-ttu-id="be458-739">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G3 Informationen**</span><span class="sxs-lookup"><span data-stu-id="be458-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-740">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-740">**Subject**</span></span>|
|<span data-ttu-id="be458-741">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-741"></span></span>|
|<span data-ttu-id="be458-742">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-742">**Issuer**</span></span>|
|<span data-ttu-id="be458-743">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-743"></span></span>|
|<span data-ttu-id="be458-744">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-744">**Serial Number**</span></span>|
|<span data-ttu-id="be458-745">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-745"></span></span>|
|<span data-ttu-id="be458-746">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-746">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-747">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-747"></span></span>|
|<span data-ttu-id="be458-748">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-749">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-749"></span></span>|
|<span data-ttu-id="be458-750">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-751">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-751"></span></span>|
|<span data-ttu-id="be458-752">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-752">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-753">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-753"></span></span>|
|<span data-ttu-id="be458-754">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-755">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-755"></span></span>|
|<span data-ttu-id="be458-756">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-757">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-757"></span></span>|
|<span data-ttu-id="be458-758">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-759">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-759"></span></span>|
|<span data-ttu-id="be458-760">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-761">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-761"></span></span>|
|<span data-ttu-id="be458-762">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-763">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-763"></span></span>|
|<span data-ttu-id="be458-764">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-764">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-765">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-765"></span></span>|
|<span data-ttu-id="be458-766">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-767">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-767"></span></span>|
   
 <span data-ttu-id="be458-768">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="be458-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-769">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-769">**Subject**</span></span>|
|<span data-ttu-id="be458-770">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-770"></span></span>|
|<span data-ttu-id="be458-771">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-771">**Issuer**</span></span>|
|<span data-ttu-id="be458-772">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-772"></span></span>|
|<span data-ttu-id="be458-773">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-773">**Serial Number**</span></span>|
|<span data-ttu-id="be458-774">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-774"></span></span>|
|<span data-ttu-id="be458-775">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-775">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-776">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-776"></span></span>|
|<span data-ttu-id="be458-777">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-778">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-778"></span></span>|
|<span data-ttu-id="be458-779">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-780">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-780"></span></span>|
|<span data-ttu-id="be458-781">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-781">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-782">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-782"></span></span>|
|<span data-ttu-id="be458-783">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-784">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-784"></span></span>|
|<span data-ttu-id="be458-785">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-786">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-786"></span></span>|
|<span data-ttu-id="be458-787">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-788">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-788"></span></span>|
|<span data-ttu-id="be458-789">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-790">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-790"></span></span>|
|<span data-ttu-id="be458-791">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-792">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-792"></span></span>|
|<span data-ttu-id="be458-793">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-793">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-794">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-794"></span></span>|
|<span data-ttu-id="be458-795">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-796">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-796"></span></span>|
   
 <span data-ttu-id="be458-797">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="be458-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-798">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-798">**Subject**</span></span>|
|<span data-ttu-id="be458-799">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-799"></span></span>|
|<span data-ttu-id="be458-800">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-800">**Issuer**</span></span>|
|<span data-ttu-id="be458-801">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-801"></span></span>|
|<span data-ttu-id="be458-802">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-802">**Serial Number**</span></span>|
|<span data-ttu-id="be458-803">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-803"></span></span>|
|<span data-ttu-id="be458-804">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-804">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-805">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-805"></span></span>|
|<span data-ttu-id="be458-806">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-807">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-807"></span></span>|
|<span data-ttu-id="be458-808">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-809">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-809"></span></span>|
|<span data-ttu-id="be458-810">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-810">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-811">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-811"></span></span>|
|<span data-ttu-id="be458-812">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-813">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-813"></span></span>|
|<span data-ttu-id="be458-814">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-815">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-815"></span></span>|
|<span data-ttu-id="be458-816">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-817">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-817"></span></span>|
|<span data-ttu-id="be458-818">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-819">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-819"></span></span>|
|<span data-ttu-id="be458-820">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-821">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-821"></span></span>|
|<span data-ttu-id="be458-822">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-822">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-823">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-823"></span></span>|
|<span data-ttu-id="be458-824">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-825">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-825"></span></span>|
   
 <span data-ttu-id="be458-826">**Lassen Sie uns Behörde X3 verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="be458-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-827">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-827">**Subject**</span></span>|
|<span data-ttu-id="be458-828">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-828"></span></span>|
|<span data-ttu-id="be458-829">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-829">**Issuer**</span></span>|
|<span data-ttu-id="be458-830">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-830"></span></span>|
|<span data-ttu-id="be458-831">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-831">**Serial Number**</span></span>|
|<span data-ttu-id="be458-832">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-832"></span></span>|
|<span data-ttu-id="be458-833">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-833">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-834">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-834"></span></span>|
|<span data-ttu-id="be458-835">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-836">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-836"></span></span>|
|<span data-ttu-id="be458-837">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-838">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-838"></span></span>|
|<span data-ttu-id="be458-839">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-839">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-840">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-840"></span></span>|
|<span data-ttu-id="be458-841">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-842">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-842"></span></span>|
|<span data-ttu-id="be458-843">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-844">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-844"></span></span>|
|<span data-ttu-id="be458-845">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-846">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-846"></span></span>|
|<span data-ttu-id="be458-847">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-848">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-848"></span></span>|
|<span data-ttu-id="be458-849">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-850">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-850"></span></span>|
|<span data-ttu-id="be458-851">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-851">**AIA URLs**</span></span>|
|<span data-ttu-id="be458-852">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-852"></span></span>|
|<span data-ttu-id="be458-853">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-853">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-854">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-854"></span></span>|
|<span data-ttu-id="be458-855">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-856">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-856"></span></span>|
   
 <span data-ttu-id="be458-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="be458-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-858">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-858">**Subject**</span></span>|
|<span data-ttu-id="be458-859">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-859"></span></span>|
|<span data-ttu-id="be458-860">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-860">**Issuer**</span></span>|
|<span data-ttu-id="be458-861">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-861"></span></span>|
|<span data-ttu-id="be458-862">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-862">**Serial Number**</span></span>|
|<span data-ttu-id="be458-863">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-863"></span></span>|
|<span data-ttu-id="be458-864">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-864">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-865">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-865"></span></span>|
|<span data-ttu-id="be458-866">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-867">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-867"></span></span>|
|<span data-ttu-id="be458-868">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-869">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-869"></span></span>|
|<span data-ttu-id="be458-870">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-870">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-871">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-871"></span></span>|
|<span data-ttu-id="be458-872">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-873">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-873"></span></span>|
|<span data-ttu-id="be458-874">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-875">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-875"></span></span>|
|<span data-ttu-id="be458-876">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-877">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-877"></span></span>|
|<span data-ttu-id="be458-878">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-879">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-879"></span></span>|
|<span data-ttu-id="be458-880">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-881">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-881"></span></span>|
|<span data-ttu-id="be458-882">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-882">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-883">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-883"></span></span>|
   
 <span data-ttu-id="be458-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="be458-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-885">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-885">**Subject**</span></span>|
|<span data-ttu-id="be458-886">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-886"></span></span>|
|<span data-ttu-id="be458-887">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-887">**Issuer**</span></span>|
|<span data-ttu-id="be458-888">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-888"></span></span>|
|<span data-ttu-id="be458-889">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-889">**Serial Number**</span></span>|
|<span data-ttu-id="be458-890">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-890"></span></span>|
|<span data-ttu-id="be458-891">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-891">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-892">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-892"></span></span>|
|<span data-ttu-id="be458-893">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-894">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-894"></span></span>|
|<span data-ttu-id="be458-895">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-896">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-896"></span></span>|
|<span data-ttu-id="be458-897">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-897">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-898">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-898"></span></span>|
|<span data-ttu-id="be458-899">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-900">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-900"></span></span>|
|<span data-ttu-id="be458-901">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-902">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-902"></span></span>|
|<span data-ttu-id="be458-903">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-904">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-904"></span></span>|
|<span data-ttu-id="be458-905">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-906">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-906"></span></span>|
|<span data-ttu-id="be458-907">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-908">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-908"></span></span>|
|<span data-ttu-id="be458-909">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-909">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-910">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-910"></span></span>|
|<span data-ttu-id="be458-911">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-912">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-912"></span></span>|
   
 <span data-ttu-id="be458-913">**Microsoft IT TLS Zertifizierungsstelle 1**</span><span class="sxs-lookup"><span data-stu-id="be458-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-914">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-914">**Subject**</span></span>|
|<span data-ttu-id="be458-915">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-915"></span></span>|
|<span data-ttu-id="be458-916">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-916">**Issuer**</span></span>|
|<span data-ttu-id="be458-917">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-917"></span></span>|
|<span data-ttu-id="be458-918">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-918">**Serial Number**</span></span>|
|<span data-ttu-id="be458-919">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-919"></span></span>|
|<span data-ttu-id="be458-920">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-920">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-921">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-921"></span></span>|
|<span data-ttu-id="be458-922">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-923">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-923"></span></span>|
|<span data-ttu-id="be458-924">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-925">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-925"></span></span>|
|<span data-ttu-id="be458-926">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-926">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-927">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-927"></span></span>|
|<span data-ttu-id="be458-928">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-929">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-929"></span></span>|
|<span data-ttu-id="be458-930">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-931">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-931"></span></span>|
|<span data-ttu-id="be458-932">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-933">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-933"></span></span>|
|<span data-ttu-id="be458-934">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-935">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-935"></span></span>|
|<span data-ttu-id="be458-936">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-937">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-937"></span></span>|
|<span data-ttu-id="be458-938">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-938">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-939">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-939"></span></span>|
|<span data-ttu-id="be458-940">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-941">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-941"></span></span>|
   
 <span data-ttu-id="be458-942">**Microsoft IT TLS Zertifizierungsstelle 2**</span><span class="sxs-lookup"><span data-stu-id="be458-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-943">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-943">**Subject**</span></span>|
|<span data-ttu-id="be458-944">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-944"></span></span>|
|<span data-ttu-id="be458-945">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-945">**Issuer**</span></span>|
|<span data-ttu-id="be458-946">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-946"></span></span>|
|<span data-ttu-id="be458-947">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-947">**Serial Number**</span></span>|
|<span data-ttu-id="be458-948">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-948"></span></span>|
|<span data-ttu-id="be458-949">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-949">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-950">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-950"></span></span>|
|<span data-ttu-id="be458-951">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-952">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-952"></span></span>|
|<span data-ttu-id="be458-953">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-954">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-954"></span></span>|
|<span data-ttu-id="be458-955">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-955">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-956">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-956"></span></span>|
|<span data-ttu-id="be458-957">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-958">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-958"></span></span>|
|<span data-ttu-id="be458-959">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-960">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-960"></span></span>|
|<span data-ttu-id="be458-961">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-962">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-962"></span></span>|
|<span data-ttu-id="be458-963">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-964">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-964"></span></span>|
|<span data-ttu-id="be458-965">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-966">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-966"></span></span>|
|<span data-ttu-id="be458-967">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-967">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-968">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-968"></span></span>|
|<span data-ttu-id="be458-969">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-970">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-970"></span></span>|
   
 <span data-ttu-id="be458-971">**Microsoft IT TLS Zertifizierungsstelle 4**</span><span class="sxs-lookup"><span data-stu-id="be458-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-972">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-972">**Subject**</span></span>|
|<span data-ttu-id="be458-973">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-973"></span></span>|
|<span data-ttu-id="be458-974">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-974">**Issuer**</span></span>|
|<span data-ttu-id="be458-975">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-975"></span></span>|
|<span data-ttu-id="be458-976">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-976">**Serial Number**</span></span>|
|<span data-ttu-id="be458-977">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-977"></span></span>|
|<span data-ttu-id="be458-978">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-978">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-979">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-979"></span></span>|
|<span data-ttu-id="be458-980">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-981">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-981"></span></span>|
|<span data-ttu-id="be458-982">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-983">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-983"></span></span>|
|<span data-ttu-id="be458-984">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-984">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-985">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-985"></span></span>|
|<span data-ttu-id="be458-986">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-987">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-987"></span></span>|
|<span data-ttu-id="be458-988">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-989">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-989"></span></span>|
|<span data-ttu-id="be458-990">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-991">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-991"></span></span>|
|<span data-ttu-id="be458-992">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-993">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-993"></span></span>|
|<span data-ttu-id="be458-994">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-995">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-995"></span></span>|
|<span data-ttu-id="be458-996">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-996">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-997">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-997"></span></span>|
|<span data-ttu-id="be458-998">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-999">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-999"></span></span>|
   
 <span data-ttu-id="be458-1000">**Microsoft IT TLS Zertifizierungsstelle 5**</span><span class="sxs-lookup"><span data-stu-id="be458-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-1001">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-1001">**Subject**</span></span>|
|<span data-ttu-id="be458-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1002"></span></span>|
|<span data-ttu-id="be458-1003">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-1003">**Issuer**</span></span>|
|<span data-ttu-id="be458-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1004"></span></span>|
|<span data-ttu-id="be458-1005">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-1005">**Serial Number**</span></span>|
|<span data-ttu-id="be458-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1006"></span></span>|
|<span data-ttu-id="be458-1007">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1008"></span></span>|
|<span data-ttu-id="be458-1009">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1010"></span></span>|
|<span data-ttu-id="be458-1011">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1012"></span></span>|
|<span data-ttu-id="be458-1013">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1014"></span></span>|
|<span data-ttu-id="be458-1015">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1016"></span></span>|
|<span data-ttu-id="be458-1017">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1018"></span></span>|
|<span data-ttu-id="be458-1019">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1020"></span></span>|
|<span data-ttu-id="be458-1021">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1022"></span></span>|
|<span data-ttu-id="be458-1023">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1024"></span></span>|
|<span data-ttu-id="be458-1025">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1026"></span></span>|
|<span data-ttu-id="be458-1027">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1028"></span></span>|
   
 <span data-ttu-id="be458-1029">**Symantec Klasse 3 EV SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="be458-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-1030">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-1030">**Subject**</span></span>|
|<span data-ttu-id="be458-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1031"></span></span>|
|<span data-ttu-id="be458-1032">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-1032">**Issuer**</span></span>|
|<span data-ttu-id="be458-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1033"></span></span>|
|<span data-ttu-id="be458-1034">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="be458-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="be458-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1035"></span></span>|
|<span data-ttu-id="be458-1036">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-1036">**Serial Number**</span></span>|
|<span data-ttu-id="be458-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1037"></span></span>|
|<span data-ttu-id="be458-1038">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1039"></span></span>|
|<span data-ttu-id="be458-1040">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1041"></span></span>|
|<span data-ttu-id="be458-1042">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1043"></span></span>|
|<span data-ttu-id="be458-1044">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1045"></span></span>|
|<span data-ttu-id="be458-1046">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1047"></span></span>|
|<span data-ttu-id="be458-1048">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1049"></span></span>|
|<span data-ttu-id="be458-1050">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1051"></span></span>|
|<span data-ttu-id="be458-1052">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1053"></span></span>|
|<span data-ttu-id="be458-1054">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1055"></span></span>|
|<span data-ttu-id="be458-1056">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1057"></span></span>|
|<span data-ttu-id="be458-1058">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1059"></span></span>|
   
 <span data-ttu-id="be458-1060">**Symantec Klasse 3 sicheren Server CA - G4**</span><span class="sxs-lookup"><span data-stu-id="be458-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-1061">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-1061">**Subject**</span></span>|
|<span data-ttu-id="be458-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1062"></span></span>|
|<span data-ttu-id="be458-1063">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-1063">**Issuer**</span></span>|
|<span data-ttu-id="be458-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1064"></span></span>|
|<span data-ttu-id="be458-1065">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="be458-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="be458-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1066"></span></span>|
|<span data-ttu-id="be458-1067">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-1067">**Serial Number**</span></span>|
|<span data-ttu-id="be458-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1068"></span></span>|
|<span data-ttu-id="be458-1069">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1070"></span></span>|
|<span data-ttu-id="be458-1071">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1072"></span></span>|
|<span data-ttu-id="be458-1073">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1074"></span></span>|
|<span data-ttu-id="be458-1075">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1076"></span></span>|
|<span data-ttu-id="be458-1077">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1078"></span></span>|
|<span data-ttu-id="be458-1079">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1080"></span></span>|
|<span data-ttu-id="be458-1081">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1082"></span></span>|
|<span data-ttu-id="be458-1083">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1084"></span></span>|
|<span data-ttu-id="be458-1085">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1086"></span></span>|
|<span data-ttu-id="be458-1087">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1088"></span></span>|
|<span data-ttu-id="be458-1089">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1090"></span></span>|
   
 <span data-ttu-id="be458-1091">**Thawte SHA256-SSL-Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="be458-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-1092">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-1092">**Subject**</span></span>|
|<span data-ttu-id="be458-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1093"></span></span>|
|<span data-ttu-id="be458-1094">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-1094">**Issuer**</span></span>|
|<span data-ttu-id="be458-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1095"></span></span>|
|<span data-ttu-id="be458-1096">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="be458-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="be458-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1097"></span></span>|
|<span data-ttu-id="be458-1098">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-1098">**Serial Number**</span></span>|
|<span data-ttu-id="be458-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1099"></span></span>|
|<span data-ttu-id="be458-1100">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1101"></span></span>|
|<span data-ttu-id="be458-1102">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1103"></span></span>|
|<span data-ttu-id="be458-1104">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1105"></span></span>|
|<span data-ttu-id="be458-1106">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1107"></span></span>|
|<span data-ttu-id="be458-1108">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1109"></span></span>|
|<span data-ttu-id="be458-1110">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1111"></span></span>|
|<span data-ttu-id="be458-1112">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1113"></span></span>|
|<span data-ttu-id="be458-1114">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1115"></span></span>|
|<span data-ttu-id="be458-1116">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1117"></span></span>|
|<span data-ttu-id="be458-1118">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1119"></span></span>|
|<span data-ttu-id="be458-1120">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1121"></span></span>|
   
 <span data-ttu-id="be458-1122">**Verizon Akamai SureServer Zertifizierungsstelle G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="be458-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="be458-1123">**Subject**</span><span class="sxs-lookup"><span data-stu-id="be458-1123">**Subject**</span></span>|
|<span data-ttu-id="be458-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1124"></span></span>|
|<span data-ttu-id="be458-1125">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="be458-1125">**Issuer**</span></span>|
|<span data-ttu-id="be458-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1126"></span></span>|
|<span data-ttu-id="be458-1127">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="be458-1127">**Serial Number**</span></span>|
|<span data-ttu-id="be458-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1128"></span></span>|
|<span data-ttu-id="be458-1129">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="be458-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="be458-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1130"></span></span>|
|<span data-ttu-id="be458-1131">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="be458-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="be458-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1132"></span></span>|
|<span data-ttu-id="be458-1133">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="be458-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="be458-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1134"></span></span>|
|<span data-ttu-id="be458-1135">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="be458-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="be458-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1136"></span></span>|
|<span data-ttu-id="be458-1137">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="be458-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1138"></span></span>|
|<span data-ttu-id="be458-1139">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="be458-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="be458-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1140"></span></span>|
|<span data-ttu-id="be458-1141">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="be458-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="be458-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1142"></span></span>|
|<span data-ttu-id="be458-1143">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1144"></span></span>|
|<span data-ttu-id="be458-1145">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="be458-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="be458-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1146"></span></span>|
|<span data-ttu-id="be458-1147">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="be458-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1148"></span></span>|
|<span data-ttu-id="be458-1149">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="be458-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1150"></span></span>|
|<span data-ttu-id="be458-1151">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="be458-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="be458-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="be458-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="be458-1153">Weiteres Zertifikat Pfade</span><span class="sxs-lookup"><span data-stu-id="be458-1153">Additional certificate paths</span></span>
<span data-ttu-id="be458-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="be458-1154"></span></span>

<span data-ttu-id="be458-1155">Folgendes umfassen legacy Zertifikate, die sind nicht über enthalten und mit der obigen Liste über einen Zeitraum zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be458-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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



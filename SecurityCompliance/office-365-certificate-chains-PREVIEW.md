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
ms.sourcegitcommit: 13f40ff7c1799152bf45af2d8110f4f3235b770a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25549753"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="30895-106">Office 365 Zertifikatketten</span><span class="sxs-lookup"><span data-stu-id="30895-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="30895-p102">Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen für die Zertifikate, die Sie in Ihrer eigenen Infrastruktur installieren möchten finden Sie unter [Planen von Drittanbieter - SSL-Zertifikate für Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.</span><span class="sxs-lookup"><span data-stu-id="30895-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="30895-111">**Zertifikattyp**</span><span class="sxs-lookup"><span data-stu-id="30895-111">**Certificate type**</span></span>|<span data-ttu-id="30895-112">**P7b-download**</span><span class="sxs-lookup"><span data-stu-id="30895-112">**P7b download**</span></span>|<span data-ttu-id="30895-113">**CRL-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="30895-113">**CRL Endpoints**</span></span>|<span data-ttu-id="30895-114">**OCSP-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="30895-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="30895-115">**AIA-Endpunkte**</span><span class="sxs-lookup"><span data-stu-id="30895-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="30895-116">Öffentlich vertrauenswürdige Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="30895-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="30895-117">Office 365 Root Certificate Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="30895-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="30895-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="30895-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="30895-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="30895-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="30895-120">n. v.</span><span class="sxs-lookup"><span data-stu-id="30895-120">N/A</span></span>  <br/> |<span data-ttu-id="30895-121">n. v.</span><span class="sxs-lookup"><span data-stu-id="30895-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="30895-122">Öffentlich vertrauenswürdigen Zertifikate Intermediate</span><span class="sxs-lookup"><span data-stu-id="30895-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="30895-123">Office 365 Intermediate Zertifikat Bundle (P7B)</span><span class="sxs-lookup"><span data-stu-id="30895-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="30895-124">cdp1.Public trust.com</span><span class="sxs-lookup"><span data-stu-id="30895-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="30895-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="30895-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="30895-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="30895-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="30895-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="30895-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="30895-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="30895-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="30895-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="30895-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="30895-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="30895-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="30895-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="30895-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="30895-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="30895-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="30895-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="30895-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="30895-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="30895-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="30895-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="30895-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="30895-136">OCSP.digicert.com</span><span class="sxs-lookup"><span data-stu-id="30895-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="30895-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="30895-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="30895-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="30895-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="30895-139">OCSP.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="30895-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="30895-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="30895-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="30895-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="30895-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="30895-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="30895-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="30895-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="30895-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="30895-144">Stamm-c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="30895-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="30895-145">Root-C3-ca2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="30895-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="30895-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="30895-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="30895-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="30895-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="30895-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="30895-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="30895-149">cacert.OmniRoot.com</span><span class="sxs-lookup"><span data-stu-id="30895-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="30895-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="30895-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="30895-151">Erweitern Sie den Domänenstamm und in intermediate auf Weitere Informationen zu den Zertifikat-Anbietern finden in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="30895-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="30895-152">Office 365-Stamm Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="30895-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="30895-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="30895-153"></span></span>

 <span data-ttu-id="30895-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="30895-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="30895-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="30895-155">|:-----|</span></span>
|<span data-ttu-id="30895-156">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="30895-157">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-157">**Serial Number**</span></span>|
|<span data-ttu-id="30895-158">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-158"></span></span>|
|<span data-ttu-id="30895-159">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-159">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-160">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-160"></span></span>|
|<span data-ttu-id="30895-161">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-162">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-162"></span></span>|
|<span data-ttu-id="30895-163">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-164">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-164"></span></span>|
|<span data-ttu-id="30895-165">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-165">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-166">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-166"></span></span>|
|<span data-ttu-id="30895-167">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-168">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-168"></span></span>|
|<span data-ttu-id="30895-169">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-170">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-170"></span></span>|
|<span data-ttu-id="30895-171">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-172">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-172"></span></span>|
|<span data-ttu-id="30895-173">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-174">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-174"></span></span>|
   
 <span data-ttu-id="30895-175">**CNNIC STAMM**</span><span class="sxs-lookup"><span data-stu-id="30895-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-176">**Subject**</span></span>|
|<span data-ttu-id="30895-177">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-177"></span></span>|
|<span data-ttu-id="30895-178">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-178">**Serial Number**</span></span>|
|<span data-ttu-id="30895-179">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-179"></span></span>|
|<span data-ttu-id="30895-180">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-180">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-181">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-181"></span></span>|
|<span data-ttu-id="30895-182">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-183">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-183"></span></span>|
|<span data-ttu-id="30895-184">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-185">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-185"></span></span>|
|<span data-ttu-id="30895-186">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-186">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-187">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-187"></span></span>|
|<span data-ttu-id="30895-188">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-189">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-189"></span></span>|
|<span data-ttu-id="30895-190">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-191">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-191"></span></span>|
|<span data-ttu-id="30895-192">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-193">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-193"></span></span>|
|<span data-ttu-id="30895-194">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-195">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-195"></span></span>|
|<span data-ttu-id="30895-196">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-197">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-197"></span></span>|
   
 <span data-ttu-id="30895-198">**Globale Stammzertifizierungsstelle DigiCert**</span><span class="sxs-lookup"><span data-stu-id="30895-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-199">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-199">**Subject**</span></span>|
|<span data-ttu-id="30895-200">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-200"></span></span>|
|<span data-ttu-id="30895-201">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-201">**Serial Number**</span></span>|
|<span data-ttu-id="30895-202">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-202"></span></span>|
|<span data-ttu-id="30895-203">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-203">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-204">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-204"></span></span>|
|<span data-ttu-id="30895-205">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-206">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-206"></span></span>|
|<span data-ttu-id="30895-207">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-208">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-208"></span></span>|
|<span data-ttu-id="30895-209">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-209">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-210">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-210"></span></span>|
|<span data-ttu-id="30895-211">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-212">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-212"></span></span>|
|<span data-ttu-id="30895-213">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-214">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-214"></span></span>|
|<span data-ttu-id="30895-215">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-216">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-216"></span></span>|
|<span data-ttu-id="30895-217">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-218">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-218"></span></span>|
|<span data-ttu-id="30895-219">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-220">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-220"></span></span>|
   
 <span data-ttu-id="30895-221">**DigiCert besonders Assurance EV Stammzertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="30895-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-222">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-222">**Subject**</span></span>|
|<span data-ttu-id="30895-223">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-223"></span></span>|
|<span data-ttu-id="30895-224">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-224">**Serial Number**</span></span>|
|<span data-ttu-id="30895-225">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-225"></span></span>|
|<span data-ttu-id="30895-226">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-226">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-227">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-227"></span></span>|
|<span data-ttu-id="30895-228">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-229">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-229"></span></span>|
|<span data-ttu-id="30895-230">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-231">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-231"></span></span>|
|<span data-ttu-id="30895-232">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-232">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-233">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-233"></span></span>|
|<span data-ttu-id="30895-234">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-235">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-235"></span></span>|
|<span data-ttu-id="30895-236">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-237">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-237"></span></span>|
|<span data-ttu-id="30895-238">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-239">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-239"></span></span>|
|<span data-ttu-id="30895-240">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-241">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-241"></span></span>|
|<span data-ttu-id="30895-242">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-243">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-243"></span></span>|
   
 <span data-ttu-id="30895-244">**D-TRUST-Klasse 3 Stammzertifizierungsstelle 2 2009**</span><span class="sxs-lookup"><span data-stu-id="30895-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-245">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-245">**Subject**</span></span>|
|<span data-ttu-id="30895-246">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-246"></span></span>|
|<span data-ttu-id="30895-247">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-247">**Serial Number**</span></span>|
|<span data-ttu-id="30895-248">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-248"></span></span>|
|<span data-ttu-id="30895-249">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-249">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-250">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-250"></span></span>|
|<span data-ttu-id="30895-251">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-252">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-252"></span></span>|
|<span data-ttu-id="30895-253">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-254">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-254"></span></span>|
|<span data-ttu-id="30895-255">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-255">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-256">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-256"></span></span>|
|<span data-ttu-id="30895-257">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-258">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-258"></span></span>|
|<span data-ttu-id="30895-259">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-260">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-260"></span></span>|
|<span data-ttu-id="30895-261">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-262">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-262"></span></span>|
|<span data-ttu-id="30895-263">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-264">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-264"></span></span>|
|<span data-ttu-id="30895-265">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-265">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-266">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-266"></span></span>|
   
 <span data-ttu-id="30895-267">**Klasse 3-D VERTRAUENSWÜRDIGE Stammzertifizierungsstelle 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="30895-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-268">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-268">**Subject**</span></span>|
|<span data-ttu-id="30895-269">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-269"></span></span>|
|<span data-ttu-id="30895-270">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-270">**Serial Number**</span></span>|
|<span data-ttu-id="30895-271">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-271"></span></span>|
|<span data-ttu-id="30895-272">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-272">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-273">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-273"></span></span>|
|<span data-ttu-id="30895-274">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-275">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-275"></span></span>|
|<span data-ttu-id="30895-276">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-277">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-277"></span></span>|
|<span data-ttu-id="30895-278">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-278">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-279">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-279"></span></span>|
|<span data-ttu-id="30895-280">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-281">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-281"></span></span>|
|<span data-ttu-id="30895-282">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-283">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-283"></span></span>|
|<span data-ttu-id="30895-284">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-285">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-285"></span></span>|
|<span data-ttu-id="30895-286">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-287">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-287"></span></span>|
|<span data-ttu-id="30895-288">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-288">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-289">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-289"></span></span>|
   
 <span data-ttu-id="30895-290">**Sommerzeit Stammzertifizierungsstelle X3**</span><span class="sxs-lookup"><span data-stu-id="30895-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-291">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-291">**Subject**</span></span>|
|<span data-ttu-id="30895-292">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-292"></span></span>|
|<span data-ttu-id="30895-293">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-293">**Serial Number**</span></span>|
|<span data-ttu-id="30895-294">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-294"></span></span>|
|<span data-ttu-id="30895-295">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-295">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-296">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-296"></span></span>|
|<span data-ttu-id="30895-297">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-298">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-298"></span></span>|
|<span data-ttu-id="30895-299">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-300">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-300"></span></span>|
|<span data-ttu-id="30895-301">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-301">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-302">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-302"></span></span>|
|<span data-ttu-id="30895-303">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-304">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-304"></span></span>|
|<span data-ttu-id="30895-305">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-306">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-306"></span></span>|
|<span data-ttu-id="30895-307">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-308">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-308"></span></span>|
|<span data-ttu-id="30895-309">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-310">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-310"></span></span>|
   
 <span data-ttu-id="30895-311">**Entrust Stammzertifizierungsstelle - G2**</span><span class="sxs-lookup"><span data-stu-id="30895-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-312">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-312">**Subject**</span></span>|
|<span data-ttu-id="30895-313">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-313"></span></span>|
|<span data-ttu-id="30895-314">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-314">**Serial Number**</span></span>|
|<span data-ttu-id="30895-315">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-315"></span></span>|
|<span data-ttu-id="30895-316">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-316">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-317">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-317"></span></span>|
|<span data-ttu-id="30895-318">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-319">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-319"></span></span>|
|<span data-ttu-id="30895-320">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-321">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-321"></span></span>|
|<span data-ttu-id="30895-322">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-322">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-323">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-323"></span></span>|
|<span data-ttu-id="30895-324">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-325">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-325"></span></span>|
|<span data-ttu-id="30895-326">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-327">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-327"></span></span>|
|<span data-ttu-id="30895-328">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-329">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-329"></span></span>|
|<span data-ttu-id="30895-330">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-331">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-331"></span></span>|
   
 <span data-ttu-id="30895-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="30895-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-333">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-333">**Subject**</span></span>|
|<span data-ttu-id="30895-334">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-334"></span></span>|
|<span data-ttu-id="30895-335">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-335">**Serial Number**</span></span>|
|<span data-ttu-id="30895-336">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-336"></span></span>|
|<span data-ttu-id="30895-337">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-337">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-338">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-338"></span></span>|
|<span data-ttu-id="30895-339">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-340">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-340"></span></span>|
|<span data-ttu-id="30895-341">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-342">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-342"></span></span>|
|<span data-ttu-id="30895-343">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-343">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-344">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-344"></span></span>|
|<span data-ttu-id="30895-345">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-346">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-346"></span></span>|
|<span data-ttu-id="30895-347">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-348">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-348"></span></span>|
|<span data-ttu-id="30895-349">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-350">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-350"></span></span>|
|<span data-ttu-id="30895-351">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-352">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-352"></span></span>|
   
 <span data-ttu-id="30895-353">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="30895-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-354">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-354">**Subject**</span></span>|
|<span data-ttu-id="30895-355">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-355"></span></span>|
|<span data-ttu-id="30895-356">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-356">**Serial Number**</span></span>|
|<span data-ttu-id="30895-357">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-357"></span></span>|
|<span data-ttu-id="30895-358">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-358">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-359">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-359"></span></span>|
|<span data-ttu-id="30895-360">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-361">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-361"></span></span>|
|<span data-ttu-id="30895-362">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-363">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-363"></span></span>|
|<span data-ttu-id="30895-364">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-364">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-365">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-365"></span></span>|
|<span data-ttu-id="30895-366">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-367">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-367"></span></span>|
|<span data-ttu-id="30895-368">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-369">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-369"></span></span>|
|<span data-ttu-id="30895-370">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-371">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-371"></span></span>|
|<span data-ttu-id="30895-372">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-373">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-373"></span></span>|
|<span data-ttu-id="30895-374">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-375">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-375"></span></span>|
|<span data-ttu-id="30895-376">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-376">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-377">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-377"></span></span>|
   
 <span data-ttu-id="30895-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="30895-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-379">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-379">**Subject**</span></span>|
|<span data-ttu-id="30895-380">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-380"></span></span>|
|<span data-ttu-id="30895-381">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-381">**Serial Number**</span></span>|
|<span data-ttu-id="30895-382">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-382"></span></span>|
|<span data-ttu-id="30895-383">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-383">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-384">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-384"></span></span>|
|<span data-ttu-id="30895-385">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-386">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-386"></span></span>|
|<span data-ttu-id="30895-387">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-388">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-388"></span></span>|
|<span data-ttu-id="30895-389">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-389">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-390">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-390"></span></span>|
|<span data-ttu-id="30895-391">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-392">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-392"></span></span>|
|<span data-ttu-id="30895-393">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-394">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-394"></span></span>|
|<span data-ttu-id="30895-395">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-396">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-396"></span></span>|
|<span data-ttu-id="30895-397">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-398">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-398"></span></span>|
   
 <span data-ttu-id="30895-399">**Thawte primären Stammzertifizierungsstelle - G3**</span><span class="sxs-lookup"><span data-stu-id="30895-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-400">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-400">**Subject**</span></span>|
|<span data-ttu-id="30895-401">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-401"></span></span>|
|<span data-ttu-id="30895-402">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-402">**Serial Number**</span></span>|
|<span data-ttu-id="30895-403">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-403"></span></span>|
|<span data-ttu-id="30895-404">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-404">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-405">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-405"></span></span>|
|<span data-ttu-id="30895-406">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-407">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-407"></span></span>|
|<span data-ttu-id="30895-408">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-409">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-409"></span></span>|
|<span data-ttu-id="30895-410">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-410">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-411">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-411"></span></span>|
|<span data-ttu-id="30895-412">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-413">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-413"></span></span>|
|<span data-ttu-id="30895-414">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-415">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-415"></span></span>|
|<span data-ttu-id="30895-416">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-417">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-417"></span></span>|
|<span data-ttu-id="30895-418">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-419">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-419"></span></span>|
   
 <span data-ttu-id="30895-420">**VeriSign Klasse 3 öffentlichen primären Zertifizierungsstelle - G5**</span><span class="sxs-lookup"><span data-stu-id="30895-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-421">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-421">**Subject**</span></span>|
|<span data-ttu-id="30895-422">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-422"></span></span>|
|<span data-ttu-id="30895-423">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-423">**Serial Number**</span></span>|
|<span data-ttu-id="30895-424">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-424"></span></span>|
|<span data-ttu-id="30895-425">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-425">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-426">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-426"></span></span>|
|<span data-ttu-id="30895-427">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-428">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-428"></span></span>|
|<span data-ttu-id="30895-429">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-430">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-430"></span></span>|
|<span data-ttu-id="30895-431">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-431">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-432">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-432"></span></span>|
|<span data-ttu-id="30895-433">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-434">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-434"></span></span>|
|<span data-ttu-id="30895-435">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-436">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-436"></span></span>|
|<span data-ttu-id="30895-437">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-438">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-438"></span></span>|
|<span data-ttu-id="30895-439">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-440">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="30895-441">Office 365 Intermediate Zertifikatdetails</span><span class="sxs-lookup"><span data-stu-id="30895-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="30895-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="30895-442"></span></span>

 <span data-ttu-id="30895-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="30895-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-444">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-444">**Subject**</span></span>|
|<span data-ttu-id="30895-445">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-445"></span></span>|
|<span data-ttu-id="30895-446">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-446">**Issuer**</span></span>|
|<span data-ttu-id="30895-447">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-447"></span></span>|
|<span data-ttu-id="30895-448">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-448">**Serial Number**</span></span>|
|<span data-ttu-id="30895-449">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-449"></span></span>|
|<span data-ttu-id="30895-450">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-450">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-451">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-451"></span></span>|
|<span data-ttu-id="30895-452">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-453">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-453"></span></span>|
|<span data-ttu-id="30895-454">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-455">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-455"></span></span>|
|<span data-ttu-id="30895-456">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-456">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-457">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-457"></span></span>|
|<span data-ttu-id="30895-458">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-459">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-459"></span></span>|
|<span data-ttu-id="30895-460">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-461">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-461"></span></span>|
|<span data-ttu-id="30895-462">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-463">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-463"></span></span>|
|<span data-ttu-id="30895-464">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-465">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-465"></span></span>|
|<span data-ttu-id="30895-466">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-467">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-467"></span></span>|
|<span data-ttu-id="30895-468">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-468">**AIA URLs**</span></span>|
|<span data-ttu-id="30895-469">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-469"></span></span>|
|<span data-ttu-id="30895-470">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-470">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-471">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-471"></span></span>|
|<span data-ttu-id="30895-472">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-473">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-473"></span></span>|
   
 <span data-ttu-id="30895-474">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 2009**</span><span class="sxs-lookup"><span data-stu-id="30895-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-475">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-475">**Subject**</span></span>|
|<span data-ttu-id="30895-476">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-476"></span></span>|
|<span data-ttu-id="30895-477">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-477">**Issuer**</span></span>|
|<span data-ttu-id="30895-478">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-478"></span></span>|
|<span data-ttu-id="30895-479">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="30895-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="30895-480">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-480"></span></span>|
|<span data-ttu-id="30895-481">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-481">**Serial Number**</span></span>|
|<span data-ttu-id="30895-482">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-482"></span></span>|
|<span data-ttu-id="30895-483">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-483">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-484">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-484"></span></span>|
|<span data-ttu-id="30895-485">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-486">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-486"></span></span>|
|<span data-ttu-id="30895-487">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-488">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-488"></span></span>|
|<span data-ttu-id="30895-489">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-489">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-490">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-490"></span></span>|
|<span data-ttu-id="30895-491">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-492">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-492"></span></span>|
|<span data-ttu-id="30895-493">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-494">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-494"></span></span>|
|<span data-ttu-id="30895-495">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-496">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-496"></span></span>|
|<span data-ttu-id="30895-497">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-498">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-498"></span></span>|
|<span data-ttu-id="30895-499">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-500">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-500"></span></span>|
|<span data-ttu-id="30895-501">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-501">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-502">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-502"></span></span>|
|<span data-ttu-id="30895-503">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-504">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-504"></span></span>|
   
 <span data-ttu-id="30895-505">**D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="30895-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-506">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-506">**Subject**</span></span>|
|<span data-ttu-id="30895-507">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-507"></span></span>|
|<span data-ttu-id="30895-508">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-508">**Issuer**</span></span>|
|<span data-ttu-id="30895-509">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-509"></span></span>|
|<span data-ttu-id="30895-510">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="30895-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="30895-511">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-511"></span></span>|
|<span data-ttu-id="30895-512">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-512">**Serial Number**</span></span>|
|<span data-ttu-id="30895-513">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-513"></span></span>|
|<span data-ttu-id="30895-514">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-514">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-515">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-515"></span></span>|
|<span data-ttu-id="30895-516">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-517">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-517"></span></span>|
|<span data-ttu-id="30895-518">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-519">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-519"></span></span>|
|<span data-ttu-id="30895-520">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-520">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-521">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-521"></span></span>|
|<span data-ttu-id="30895-522">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-523">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-523"></span></span>|
|<span data-ttu-id="30895-524">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-525">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-525"></span></span>|
|<span data-ttu-id="30895-526">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-527">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-527"></span></span>|
|<span data-ttu-id="30895-528">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-529">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-529"></span></span>|
|<span data-ttu-id="30895-530">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-531">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-531"></span></span>|
|<span data-ttu-id="30895-532">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-532">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-533">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-533"></span></span>|
|<span data-ttu-id="30895-534">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-535">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-535"></span></span>|
   
 <span data-ttu-id="30895-536">**DigiCert Cloud-Dienste CA-1**</span><span class="sxs-lookup"><span data-stu-id="30895-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-537">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-537">**Subject**</span></span>|
|<span data-ttu-id="30895-538">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-538"></span></span>|
|<span data-ttu-id="30895-539">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-539">**Issuer**</span></span>|
|<span data-ttu-id="30895-540">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-540"></span></span>|
|<span data-ttu-id="30895-541">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-541">**Serial Number**</span></span>|
|<span data-ttu-id="30895-542">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-542"></span></span>|
|<span data-ttu-id="30895-543">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-543">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-544">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-544"></span></span>|
|<span data-ttu-id="30895-545">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-546">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-546"></span></span>|
|<span data-ttu-id="30895-547">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-548">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-548"></span></span>|
|<span data-ttu-id="30895-549">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-549">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-550">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-550"></span></span>|
|<span data-ttu-id="30895-551">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-552">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-552"></span></span>|
|<span data-ttu-id="30895-553">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-554">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-554"></span></span>|
|<span data-ttu-id="30895-555">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-556">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-556"></span></span>|
|<span data-ttu-id="30895-557">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-558">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-558"></span></span>|
|<span data-ttu-id="30895-559">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-560">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-560"></span></span>|
|<span data-ttu-id="30895-561">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-561">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-562">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-562"></span></span>|
|<span data-ttu-id="30895-563">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-564">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-564"></span></span>|
   
 <span data-ttu-id="30895-565">**DigiCert SHA2 hohe Assurance Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="30895-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-566">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-566">**Subject**</span></span>|
|<span data-ttu-id="30895-567">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-567"></span></span>|
|<span data-ttu-id="30895-568">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-568">**Issuer**</span></span>|
|<span data-ttu-id="30895-569">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-569"></span></span>|
|<span data-ttu-id="30895-570">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-570">**Serial Number**</span></span>|
|<span data-ttu-id="30895-571">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-571"></span></span>|
|<span data-ttu-id="30895-572">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-572">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-573">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-573"></span></span>|
|<span data-ttu-id="30895-574">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-575">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-575"></span></span>|
|<span data-ttu-id="30895-576">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-577">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-577"></span></span>|
|<span data-ttu-id="30895-578">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-578">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-579">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-579"></span></span>|
|<span data-ttu-id="30895-580">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-581">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-581"></span></span>|
|<span data-ttu-id="30895-582">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-583">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-583"></span></span>|
|<span data-ttu-id="30895-584">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-585">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-585"></span></span>|
|<span data-ttu-id="30895-586">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-587">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-587"></span></span>|
|<span data-ttu-id="30895-588">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-589">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-589"></span></span>|
|<span data-ttu-id="30895-590">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-590">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-591">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-591"></span></span>|
|<span data-ttu-id="30895-592">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-593">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-593"></span></span>|
   
 <span data-ttu-id="30895-594">**DigiCert SHA2 sicheren Server Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="30895-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-595">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-595">**Subject**</span></span>|
|<span data-ttu-id="30895-596">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-596"></span></span>|
|<span data-ttu-id="30895-597">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-597">**Issuer**</span></span>|
|<span data-ttu-id="30895-598">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-598"></span></span>|
|<span data-ttu-id="30895-599">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-599">**Serial Number**</span></span>|
|<span data-ttu-id="30895-600">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-600"></span></span>|
|<span data-ttu-id="30895-601">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-601">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-602">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-602"></span></span>|
|<span data-ttu-id="30895-603">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-604">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-604"></span></span>|
|<span data-ttu-id="30895-605">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-606">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-606"></span></span>|
|<span data-ttu-id="30895-607">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-607">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-608">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-608"></span></span>|
|<span data-ttu-id="30895-609">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-610">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-610"></span></span>|
|<span data-ttu-id="30895-611">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-612">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-612"></span></span>|
|<span data-ttu-id="30895-613">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-614">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-614"></span></span>|
|<span data-ttu-id="30895-615">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-616">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-616"></span></span>|
|<span data-ttu-id="30895-617">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-618">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-618"></span></span>|
|<span data-ttu-id="30895-619">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-619">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-620">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-620"></span></span>|
|<span data-ttu-id="30895-621">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-622">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-622"></span></span>|
   
 <span data-ttu-id="30895-623">**Entrust Zertifizierungsstelle - L1C**</span><span class="sxs-lookup"><span data-stu-id="30895-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-624">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-624">**Subject**</span></span>|
|<span data-ttu-id="30895-625">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-625"></span></span>|
|<span data-ttu-id="30895-626">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-626">**Issuer**</span></span>|
|<span data-ttu-id="30895-627">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-627"></span></span>|
|<span data-ttu-id="30895-628">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-628">**Serial Number**</span></span>|
|<span data-ttu-id="30895-629">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-629"></span></span>|
|<span data-ttu-id="30895-630">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-630">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-631">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-631"></span></span>|
|<span data-ttu-id="30895-632">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-633">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-633"></span></span>|
|<span data-ttu-id="30895-634">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-635">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-635"></span></span>|
|<span data-ttu-id="30895-636">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-636">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-637">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-637"></span></span>|
|<span data-ttu-id="30895-638">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-639">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-639"></span></span>|
|<span data-ttu-id="30895-640">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-641">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-641"></span></span>|
|<span data-ttu-id="30895-642">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-643">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-643"></span></span>|
|<span data-ttu-id="30895-644">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-645">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-645"></span></span>|
|<span data-ttu-id="30895-646">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-647">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-647"></span></span>|
|<span data-ttu-id="30895-648">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-648">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-649">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-649"></span></span>|
|<span data-ttu-id="30895-650">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-651">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-651"></span></span>|
   
 <span data-ttu-id="30895-652">**Entrust Zertifizierungsstelle - L1K**</span><span class="sxs-lookup"><span data-stu-id="30895-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-653">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-653">**Subject**</span></span>|
|<span data-ttu-id="30895-654">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-654"></span></span>|
|<span data-ttu-id="30895-655">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-655">**Issuer**</span></span>|
|<span data-ttu-id="30895-656">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-656"></span></span>|
|<span data-ttu-id="30895-657">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-657">**Serial Number**</span></span>|
|<span data-ttu-id="30895-658">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-658"></span></span>|
|<span data-ttu-id="30895-659">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-659">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-660">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-660"></span></span>|
|<span data-ttu-id="30895-661">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-662">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-662"></span></span>|
|<span data-ttu-id="30895-663">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-664">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-664"></span></span>|
|<span data-ttu-id="30895-665">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-665">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-666">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-666"></span></span>|
|<span data-ttu-id="30895-667">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-668">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-668"></span></span>|
|<span data-ttu-id="30895-669">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-670">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-670"></span></span>|
|<span data-ttu-id="30895-671">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-672">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-672"></span></span>|
|<span data-ttu-id="30895-673">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-674">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-674"></span></span>|
|<span data-ttu-id="30895-675">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-676">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-676"></span></span>|
|<span data-ttu-id="30895-677">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-677">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-678">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-678"></span></span>|
|<span data-ttu-id="30895-679">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-680">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-680"></span></span>|
   
 <span data-ttu-id="30895-681">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="30895-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-682">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-682">**Subject**</span></span>|
|<span data-ttu-id="30895-683">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-683"></span></span>|
|<span data-ttu-id="30895-684">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-684">**Issuer**</span></span>|
|<span data-ttu-id="30895-685">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-685"></span></span>|
|<span data-ttu-id="30895-686">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-686">**Serial Number**</span></span>|
|<span data-ttu-id="30895-687">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-687"></span></span>|
|<span data-ttu-id="30895-688">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-688">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-689">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-689"></span></span>|
|<span data-ttu-id="30895-690">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-691">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-691"></span></span>|
|<span data-ttu-id="30895-692">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-693">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-693"></span></span>|
|<span data-ttu-id="30895-694">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-694">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-695">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-695"></span></span>|
|<span data-ttu-id="30895-696">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-697">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-697"></span></span>|
|<span data-ttu-id="30895-698">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-699">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-699"></span></span>|
|<span data-ttu-id="30895-700">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-701">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-701"></span></span>|
|<span data-ttu-id="30895-702">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-703">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-703"></span></span>|
|<span data-ttu-id="30895-704">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-705">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-705"></span></span>|
|<span data-ttu-id="30895-706">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-706">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-707">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-707"></span></span>|
|<span data-ttu-id="30895-708">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-709">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-709"></span></span>|
   
 <span data-ttu-id="30895-710">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G2 Informationen**</span><span class="sxs-lookup"><span data-stu-id="30895-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-711">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-711">**Subject**</span></span>|
|<span data-ttu-id="30895-712">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-712"></span></span>|
|<span data-ttu-id="30895-713">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-713">**Issuer**</span></span>|
|<span data-ttu-id="30895-714">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-714"></span></span>|
|<span data-ttu-id="30895-715">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-715">**Serial Number**</span></span>|
|<span data-ttu-id="30895-716">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-716"></span></span>|
|<span data-ttu-id="30895-717">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-717">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-718">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-718"></span></span>|
|<span data-ttu-id="30895-719">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-720">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-720"></span></span>|
|<span data-ttu-id="30895-721">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-722">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-722"></span></span>|
|<span data-ttu-id="30895-723">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-723">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-724">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-724"></span></span>|
|<span data-ttu-id="30895-725">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-726">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-726"></span></span>|
|<span data-ttu-id="30895-727">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-728">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-728"></span></span>|
|<span data-ttu-id="30895-729">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-730">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-730"></span></span>|
|<span data-ttu-id="30895-731">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-732">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-732"></span></span>|
|<span data-ttu-id="30895-733">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-734">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-734"></span></span>|
|<span data-ttu-id="30895-735">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-735">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-736">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-736"></span></span>|
|<span data-ttu-id="30895-737">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-738">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-738"></span></span>|
   
 <span data-ttu-id="30895-739">**Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G3 Informationen**</span><span class="sxs-lookup"><span data-stu-id="30895-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-740">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-740">**Subject**</span></span>|
|<span data-ttu-id="30895-741">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-741"></span></span>|
|<span data-ttu-id="30895-742">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-742">**Issuer**</span></span>|
|<span data-ttu-id="30895-743">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-743"></span></span>|
|<span data-ttu-id="30895-744">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-744">**Serial Number**</span></span>|
|<span data-ttu-id="30895-745">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-745"></span></span>|
|<span data-ttu-id="30895-746">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-746">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-747">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-747"></span></span>|
|<span data-ttu-id="30895-748">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-749">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-749"></span></span>|
|<span data-ttu-id="30895-750">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-751">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-751"></span></span>|
|<span data-ttu-id="30895-752">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-752">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-753">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-753"></span></span>|
|<span data-ttu-id="30895-754">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-755">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-755"></span></span>|
|<span data-ttu-id="30895-756">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-757">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-757"></span></span>|
|<span data-ttu-id="30895-758">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-759">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-759"></span></span>|
|<span data-ttu-id="30895-760">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-761">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-761"></span></span>|
|<span data-ttu-id="30895-762">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-763">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-763"></span></span>|
|<span data-ttu-id="30895-764">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-764">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-765">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-765"></span></span>|
|<span data-ttu-id="30895-766">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-767">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-767"></span></span>|
   
 <span data-ttu-id="30895-768">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="30895-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-769">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-769">**Subject**</span></span>|
|<span data-ttu-id="30895-770">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-770"></span></span>|
|<span data-ttu-id="30895-771">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-771">**Issuer**</span></span>|
|<span data-ttu-id="30895-772">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-772"></span></span>|
|<span data-ttu-id="30895-773">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-773">**Serial Number**</span></span>|
|<span data-ttu-id="30895-774">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-774"></span></span>|
|<span data-ttu-id="30895-775">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-775">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-776">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-776"></span></span>|
|<span data-ttu-id="30895-777">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-778">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-778"></span></span>|
|<span data-ttu-id="30895-779">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-780">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-780"></span></span>|
|<span data-ttu-id="30895-781">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-781">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-782">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-782"></span></span>|
|<span data-ttu-id="30895-783">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-784">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-784"></span></span>|
|<span data-ttu-id="30895-785">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-786">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-786"></span></span>|
|<span data-ttu-id="30895-787">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-788">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-788"></span></span>|
|<span data-ttu-id="30895-789">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-790">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-790"></span></span>|
|<span data-ttu-id="30895-791">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-792">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-792"></span></span>|
|<span data-ttu-id="30895-793">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-793">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-794">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-794"></span></span>|
|<span data-ttu-id="30895-795">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-796">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-796"></span></span>|
   
 <span data-ttu-id="30895-797">**Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="30895-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-798">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-798">**Subject**</span></span>|
|<span data-ttu-id="30895-799">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-799"></span></span>|
|<span data-ttu-id="30895-800">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-800">**Issuer**</span></span>|
|<span data-ttu-id="30895-801">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-801"></span></span>|
|<span data-ttu-id="30895-802">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-802">**Serial Number**</span></span>|
|<span data-ttu-id="30895-803">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-803"></span></span>|
|<span data-ttu-id="30895-804">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-804">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-805">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-805"></span></span>|
|<span data-ttu-id="30895-806">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-807">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-807"></span></span>|
|<span data-ttu-id="30895-808">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-809">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-809"></span></span>|
|<span data-ttu-id="30895-810">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-810">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-811">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-811"></span></span>|
|<span data-ttu-id="30895-812">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-813">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-813"></span></span>|
|<span data-ttu-id="30895-814">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-815">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-815"></span></span>|
|<span data-ttu-id="30895-816">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-817">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-817"></span></span>|
|<span data-ttu-id="30895-818">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-819">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-819"></span></span>|
|<span data-ttu-id="30895-820">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-821">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-821"></span></span>|
|<span data-ttu-id="30895-822">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-822">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-823">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-823"></span></span>|
|<span data-ttu-id="30895-824">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-825">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-825"></span></span>|
   
 <span data-ttu-id="30895-826">**Lassen Sie uns Behörde X3 verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="30895-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-827">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-827">**Subject**</span></span>|
|<span data-ttu-id="30895-828">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-828"></span></span>|
|<span data-ttu-id="30895-829">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-829">**Issuer**</span></span>|
|<span data-ttu-id="30895-830">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-830"></span></span>|
|<span data-ttu-id="30895-831">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-831">**Serial Number**</span></span>|
|<span data-ttu-id="30895-832">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-832"></span></span>|
|<span data-ttu-id="30895-833">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-833">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-834">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-834"></span></span>|
|<span data-ttu-id="30895-835">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-836">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-836"></span></span>|
|<span data-ttu-id="30895-837">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-838">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-838"></span></span>|
|<span data-ttu-id="30895-839">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-839">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-840">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-840"></span></span>|
|<span data-ttu-id="30895-841">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-842">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-842"></span></span>|
|<span data-ttu-id="30895-843">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-844">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-844"></span></span>|
|<span data-ttu-id="30895-845">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-846">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-846"></span></span>|
|<span data-ttu-id="30895-847">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-848">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-848"></span></span>|
|<span data-ttu-id="30895-849">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-850">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-850"></span></span>|
|<span data-ttu-id="30895-851">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-851">**AIA URLs**</span></span>|
|<span data-ttu-id="30895-852">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-852"></span></span>|
|<span data-ttu-id="30895-853">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-853">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-854">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-854"></span></span>|
|<span data-ttu-id="30895-855">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-856">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-856"></span></span>|
   
 <span data-ttu-id="30895-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="30895-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-858">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-858">**Subject**</span></span>|
|<span data-ttu-id="30895-859">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-859"></span></span>|
|<span data-ttu-id="30895-860">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-860">**Issuer**</span></span>|
|<span data-ttu-id="30895-861">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-861"></span></span>|
|<span data-ttu-id="30895-862">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-862">**Serial Number**</span></span>|
|<span data-ttu-id="30895-863">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-863"></span></span>|
|<span data-ttu-id="30895-864">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-864">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-865">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-865"></span></span>|
|<span data-ttu-id="30895-866">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-867">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-867"></span></span>|
|<span data-ttu-id="30895-868">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-869">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-869"></span></span>|
|<span data-ttu-id="30895-870">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-870">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-871">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-871"></span></span>|
|<span data-ttu-id="30895-872">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-873">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-873"></span></span>|
|<span data-ttu-id="30895-874">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-875">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-875"></span></span>|
|<span data-ttu-id="30895-876">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-877">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-877"></span></span>|
|<span data-ttu-id="30895-878">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-879">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-879"></span></span>|
|<span data-ttu-id="30895-880">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-881">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-881"></span></span>|
|<span data-ttu-id="30895-882">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-882">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-883">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-883"></span></span>|
   
 <span data-ttu-id="30895-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="30895-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-885">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-885">**Subject**</span></span>|
|<span data-ttu-id="30895-886">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-886"></span></span>|
|<span data-ttu-id="30895-887">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-887">**Issuer**</span></span>|
|<span data-ttu-id="30895-888">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-888"></span></span>|
|<span data-ttu-id="30895-889">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-889">**Serial Number**</span></span>|
|<span data-ttu-id="30895-890">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-890"></span></span>|
|<span data-ttu-id="30895-891">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-891">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-892">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-892"></span></span>|
|<span data-ttu-id="30895-893">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-894">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-894"></span></span>|
|<span data-ttu-id="30895-895">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-896">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-896"></span></span>|
|<span data-ttu-id="30895-897">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-897">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-898">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-898"></span></span>|
|<span data-ttu-id="30895-899">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-900">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-900"></span></span>|
|<span data-ttu-id="30895-901">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-902">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-902"></span></span>|
|<span data-ttu-id="30895-903">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-904">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-904"></span></span>|
|<span data-ttu-id="30895-905">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-906">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-906"></span></span>|
|<span data-ttu-id="30895-907">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-908">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-908"></span></span>|
|<span data-ttu-id="30895-909">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-909">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-910">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-910"></span></span>|
|<span data-ttu-id="30895-911">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-912">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-912"></span></span>|
   
 <span data-ttu-id="30895-913">**Microsoft IT TLS Zertifizierungsstelle 1**</span><span class="sxs-lookup"><span data-stu-id="30895-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-914">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-914">**Subject**</span></span>|
|<span data-ttu-id="30895-915">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-915"></span></span>|
|<span data-ttu-id="30895-916">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-916">**Issuer**</span></span>|
|<span data-ttu-id="30895-917">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-917"></span></span>|
|<span data-ttu-id="30895-918">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-918">**Serial Number**</span></span>|
|<span data-ttu-id="30895-919">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-919"></span></span>|
|<span data-ttu-id="30895-920">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-920">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-921">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-921"></span></span>|
|<span data-ttu-id="30895-922">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-923">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-923"></span></span>|
|<span data-ttu-id="30895-924">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-925">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-925"></span></span>|
|<span data-ttu-id="30895-926">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-926">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-927">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-927"></span></span>|
|<span data-ttu-id="30895-928">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-929">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-929"></span></span>|
|<span data-ttu-id="30895-930">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-931">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-931"></span></span>|
|<span data-ttu-id="30895-932">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-933">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-933"></span></span>|
|<span data-ttu-id="30895-934">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-935">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-935"></span></span>|
|<span data-ttu-id="30895-936">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-937">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-937"></span></span>|
|<span data-ttu-id="30895-938">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-938">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-939">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-939"></span></span>|
|<span data-ttu-id="30895-940">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-941">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-941"></span></span>|
   
 <span data-ttu-id="30895-942">**Microsoft IT TLS Zertifizierungsstelle 2**</span><span class="sxs-lookup"><span data-stu-id="30895-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-943">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-943">**Subject**</span></span>|
|<span data-ttu-id="30895-944">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-944"></span></span>|
|<span data-ttu-id="30895-945">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-945">**Issuer**</span></span>|
|<span data-ttu-id="30895-946">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-946"></span></span>|
|<span data-ttu-id="30895-947">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-947">**Serial Number**</span></span>|
|<span data-ttu-id="30895-948">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-948"></span></span>|
|<span data-ttu-id="30895-949">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-949">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-950">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-950"></span></span>|
|<span data-ttu-id="30895-951">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-952">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-952"></span></span>|
|<span data-ttu-id="30895-953">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-954">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-954"></span></span>|
|<span data-ttu-id="30895-955">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-955">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-956">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-956"></span></span>|
|<span data-ttu-id="30895-957">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-958">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-958"></span></span>|
|<span data-ttu-id="30895-959">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-960">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-960"></span></span>|
|<span data-ttu-id="30895-961">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-962">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-962"></span></span>|
|<span data-ttu-id="30895-963">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-964">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-964"></span></span>|
|<span data-ttu-id="30895-965">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-966">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-966"></span></span>|
|<span data-ttu-id="30895-967">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-967">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-968">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-968"></span></span>|
|<span data-ttu-id="30895-969">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-970">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-970"></span></span>|
   
 <span data-ttu-id="30895-971">**Microsoft IT TLS Zertifizierungsstelle 4**</span><span class="sxs-lookup"><span data-stu-id="30895-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-972">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-972">**Subject**</span></span>|
|<span data-ttu-id="30895-973">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-973"></span></span>|
|<span data-ttu-id="30895-974">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-974">**Issuer**</span></span>|
|<span data-ttu-id="30895-975">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-975"></span></span>|
|<span data-ttu-id="30895-976">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-976">**Serial Number**</span></span>|
|<span data-ttu-id="30895-977">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-977"></span></span>|
|<span data-ttu-id="30895-978">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-978">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-979">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-979"></span></span>|
|<span data-ttu-id="30895-980">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-981">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-981"></span></span>|
|<span data-ttu-id="30895-982">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-983">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-983"></span></span>|
|<span data-ttu-id="30895-984">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-984">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-985">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-985"></span></span>|
|<span data-ttu-id="30895-986">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-987">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-987"></span></span>|
|<span data-ttu-id="30895-988">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-989">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-989"></span></span>|
|<span data-ttu-id="30895-990">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-991">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-991"></span></span>|
|<span data-ttu-id="30895-992">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-993">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-993"></span></span>|
|<span data-ttu-id="30895-994">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-995">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-995"></span></span>|
|<span data-ttu-id="30895-996">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-996">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-997">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-997"></span></span>|
|<span data-ttu-id="30895-998">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-999">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-999"></span></span>|
   
 <span data-ttu-id="30895-1000">**Microsoft IT TLS Zertifizierungsstelle 5**</span><span class="sxs-lookup"><span data-stu-id="30895-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-1001">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-1001">**Subject**</span></span>|
|<span data-ttu-id="30895-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1002"></span></span>|
|<span data-ttu-id="30895-1003">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-1003">**Issuer**</span></span>|
|<span data-ttu-id="30895-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1004"></span></span>|
|<span data-ttu-id="30895-1005">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-1005">**Serial Number**</span></span>|
|<span data-ttu-id="30895-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1006"></span></span>|
|<span data-ttu-id="30895-1007">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1008"></span></span>|
|<span data-ttu-id="30895-1009">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1010"></span></span>|
|<span data-ttu-id="30895-1011">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1012"></span></span>|
|<span data-ttu-id="30895-1013">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1014"></span></span>|
|<span data-ttu-id="30895-1015">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1016"></span></span>|
|<span data-ttu-id="30895-1017">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1018"></span></span>|
|<span data-ttu-id="30895-1019">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1020"></span></span>|
|<span data-ttu-id="30895-1021">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1022"></span></span>|
|<span data-ttu-id="30895-1023">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1024"></span></span>|
|<span data-ttu-id="30895-1025">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1026"></span></span>|
|<span data-ttu-id="30895-1027">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1028"></span></span>|
   
 <span data-ttu-id="30895-1029">**Symantec Klasse 3 EV SSL CA - G3**</span><span class="sxs-lookup"><span data-stu-id="30895-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-1030">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-1030">**Subject**</span></span>|
|<span data-ttu-id="30895-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1031"></span></span>|
|<span data-ttu-id="30895-1032">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-1032">**Issuer**</span></span>|
|<span data-ttu-id="30895-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1033"></span></span>|
|<span data-ttu-id="30895-1034">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="30895-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="30895-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1035"></span></span>|
|<span data-ttu-id="30895-1036">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-1036">**Serial Number**</span></span>|
|<span data-ttu-id="30895-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1037"></span></span>|
|<span data-ttu-id="30895-1038">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1039"></span></span>|
|<span data-ttu-id="30895-1040">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1041"></span></span>|
|<span data-ttu-id="30895-1042">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1043"></span></span>|
|<span data-ttu-id="30895-1044">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1045"></span></span>|
|<span data-ttu-id="30895-1046">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1047"></span></span>|
|<span data-ttu-id="30895-1048">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1049"></span></span>|
|<span data-ttu-id="30895-1050">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1051"></span></span>|
|<span data-ttu-id="30895-1052">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1053"></span></span>|
|<span data-ttu-id="30895-1054">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1055"></span></span>|
|<span data-ttu-id="30895-1056">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1057"></span></span>|
|<span data-ttu-id="30895-1058">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1059"></span></span>|
   
 <span data-ttu-id="30895-1060">**Symantec Klasse 3 sicheren Server CA - G4**</span><span class="sxs-lookup"><span data-stu-id="30895-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-1061">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-1061">**Subject**</span></span>|
|<span data-ttu-id="30895-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1062"></span></span>|
|<span data-ttu-id="30895-1063">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-1063">**Issuer**</span></span>|
|<span data-ttu-id="30895-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1064"></span></span>|
|<span data-ttu-id="30895-1065">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="30895-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="30895-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1066"></span></span>|
|<span data-ttu-id="30895-1067">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-1067">**Serial Number**</span></span>|
|<span data-ttu-id="30895-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1068"></span></span>|
|<span data-ttu-id="30895-1069">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1070"></span></span>|
|<span data-ttu-id="30895-1071">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1072"></span></span>|
|<span data-ttu-id="30895-1073">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1074"></span></span>|
|<span data-ttu-id="30895-1075">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1076"></span></span>|
|<span data-ttu-id="30895-1077">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1078"></span></span>|
|<span data-ttu-id="30895-1079">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1080"></span></span>|
|<span data-ttu-id="30895-1081">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1082"></span></span>|
|<span data-ttu-id="30895-1083">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1084"></span></span>|
|<span data-ttu-id="30895-1085">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1086"></span></span>|
|<span data-ttu-id="30895-1087">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1088"></span></span>|
|<span data-ttu-id="30895-1089">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1090"></span></span>|
   
 <span data-ttu-id="30895-1091">**Thawte SHA256-SSL-Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="30895-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-1092">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-1092">**Subject**</span></span>|
|<span data-ttu-id="30895-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1093"></span></span>|
|<span data-ttu-id="30895-1094">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-1094">**Issuer**</span></span>|
|<span data-ttu-id="30895-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1095"></span></span>|
|<span data-ttu-id="30895-1096">**Alternativer Antragstellername**</span><span class="sxs-lookup"><span data-stu-id="30895-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="30895-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1097"></span></span>|
|<span data-ttu-id="30895-1098">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-1098">**Serial Number**</span></span>|
|<span data-ttu-id="30895-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1099"></span></span>|
|<span data-ttu-id="30895-1100">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1101"></span></span>|
|<span data-ttu-id="30895-1102">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1103"></span></span>|
|<span data-ttu-id="30895-1104">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1105"></span></span>|
|<span data-ttu-id="30895-1106">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1107"></span></span>|
|<span data-ttu-id="30895-1108">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1109"></span></span>|
|<span data-ttu-id="30895-1110">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1111"></span></span>|
|<span data-ttu-id="30895-1112">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1113"></span></span>|
|<span data-ttu-id="30895-1114">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1115"></span></span>|
|<span data-ttu-id="30895-1116">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1117"></span></span>|
|<span data-ttu-id="30895-1118">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1119"></span></span>|
|<span data-ttu-id="30895-1120">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1121"></span></span>|
   
 <span data-ttu-id="30895-1122">**Verizon Akamai SureServer Zertifizierungsstelle G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="30895-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="30895-1123">**Subject**</span><span class="sxs-lookup"><span data-stu-id="30895-1123">**Subject**</span></span>|
|<span data-ttu-id="30895-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1124"></span></span>|
|<span data-ttu-id="30895-1125">**Aussteller**</span><span class="sxs-lookup"><span data-stu-id="30895-1125">**Issuer**</span></span>|
|<span data-ttu-id="30895-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1126"></span></span>|
|<span data-ttu-id="30895-1127">**Seriennummer**</span><span class="sxs-lookup"><span data-stu-id="30895-1127">**Serial Number**</span></span>|
|<span data-ttu-id="30895-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1128"></span></span>|
|<span data-ttu-id="30895-1129">**Länge des öffentlichen Schlüssels**</span><span class="sxs-lookup"><span data-stu-id="30895-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="30895-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1130"></span></span>|
|<span data-ttu-id="30895-1131">**Signaturalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="30895-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="30895-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1132"></span></span>|
|<span data-ttu-id="30895-1133">**Gültigkeit nicht vorher**</span><span class="sxs-lookup"><span data-stu-id="30895-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="30895-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1134"></span></span>|
|<span data-ttu-id="30895-1135">**Nicht nach Gültigkeit**</span><span class="sxs-lookup"><span data-stu-id="30895-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="30895-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1136"></span></span>|
|<span data-ttu-id="30895-1137">**Schüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="30895-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1138"></span></span>|
|<span data-ttu-id="30895-1139">**Autorität Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="30895-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="30895-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1140"></span></span>|
|<span data-ttu-id="30895-1141">**Fingerabdruck (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="30895-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="30895-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1142"></span></span>|
|<span data-ttu-id="30895-1143">**Fingerabdruck (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1144"></span></span>|
|<span data-ttu-id="30895-1145">**PIN-Nummer (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="30895-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="30895-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1146"></span></span>|
|<span data-ttu-id="30895-1147">**AIA-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="30895-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1148"></span></span>|
|<span data-ttu-id="30895-1149">**Zertifikatsperrlisten-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="30895-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1150"></span></span>|
|<span data-ttu-id="30895-1151">**OCSP-URLs**</span><span class="sxs-lookup"><span data-stu-id="30895-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="30895-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="30895-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="30895-1153">Weiteres Zertifikat Pfade</span><span class="sxs-lookup"><span data-stu-id="30895-1153">Additional certificate paths</span></span>
<span data-ttu-id="30895-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="30895-1154"></span></span>

<span data-ttu-id="30895-1155">Folgendes umfassen legacy Zertifikate, die sind nicht über enthalten und mit der obigen Liste über einen Zeitraum zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="30895-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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



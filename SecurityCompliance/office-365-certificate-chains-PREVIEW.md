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
# <a name="office-365-certificate-chains"></a>Office 365 Zertifikatketten

Office 365 nutzt eine Anzahl von anderen Anbietern. Im folgenden wird beschrieben, die vollständige Liste der bekannten Stammzertifikate für Office 365, die Kunden auftreten können, wenn Sie Office 365 zugreifen. Informationen für die Zertifikate, die Sie in Ihrer eigenen Infrastruktur installieren möchten finden Sie unter [Planen von Drittanbieter - SSL-Zertifikate für Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Die folgenden Zertifikatinformationen gilt für alle weltweit und nationale Cloud Instanzen von Office 365.
  

|**Zertifikattyp**|**P7b-download**|**CRL-Endpunkte**|**OCSP-Endpunkte**|**AIA-Endpunkte**|
|:-----|:-----|:-----|:-----|:-----|
|[Öffentlich vertrauenswürdige Stammzertifikate](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[Office 365 Root Certificate Bundle (P7B)](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |CRL.GlobalSign.NET  <br/> www.d-Trust.NET  <br/> |n. v.  <br/> |n. v.  <br/> |
|[Öffentlich vertrauenswürdigen Zertifikate Intermediate](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[Office 365 Intermediate Zertifikat Bundle (P7B)](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |cdp1.Public trust.com  <br/> CRL.cnnic.CN  <br/> CRL.Entrust.NET  <br/> CRL.GlobalSign.com  <br/> CRL.GlobalSign.NET  <br/> CRL.identrust.com  <br/> CRL.Thawte.com  <br/> crl3.digicert.com  <br/> crl4.digicert.com  <br/> s1.symcb.com  <br/> www.d-Trust.NET  <br/> |isrg.trustid.OCSP.identrust.com  <br/> OCSP.digicert.com  <br/> OCSP.Entrust.NET  <br/> OCSP.GlobalSign.com  <br/> OCSP.OmniRoot.com  <br/> OCSP.startssl.com  <br/> OCSP.Thawte.com  <br/> ocsp2.GlobalSign.com  <br/> ocspcnnicroot.cnnic.CN  <br/> Stamm-c3-ca2-2009.ocsp.d-trust.net  <br/> Root-C3-ca2-EV-2009.OCSP.d-Trust.NET  <br/> s2.symcb.com  <br/> |AIA.startssl.com  <br/> Apps.identrust.com  <br/> cacert.OmniRoot.com  <br/> www.cnnic.CN  <br/> |
   
Erweitern Sie den Domänenstamm und in intermediate auf Weitere Informationen zu den Zertifikat-Anbietern finden in den folgenden Abschnitten.
  
## <a name="office-365-root-certificate-details"></a>Office 365-Stamm Zertifikatdetails
<a name="RootCerts"> </a>

 **Baltimore CyberTrust Root**
  
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **CNNIC STAMM**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **Globale Stammzertifizierungsstelle DigiCert**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **DigiCert besonders Assurance EV Stammzertifizierungsstelle**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **D-TRUST-Klasse 3 Stammzertifizierungsstelle 2 2009**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
   
 **Klasse 3-D VERTRAUENSWÜRDIGE Stammzertifizierungsstelle 2 EV 2009**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
   
 **Sommerzeit Stammzertifizierungsstelle X3**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **Entrust Stammzertifizierungsstelle - G2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **Entrust.net Certification Authority (2048)**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **Informationen**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
   
 **GlobalSign Root CA**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **Thawte primären Stammzertifizierungsstelle - G3**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
 **VeriSign Klasse 3 öffentlichen primären Zertifizierungsstelle - G5**
  
||
|:-----|
|**Subject**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
   
## <a name="office-365-intermediate-certificate-details"></a>Office 365 Intermediate Zertifikatdetails
<a name="IntermediateCerts"> </a>

 **CNNIC SHA256 SSL**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**AIA-URLs**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 2009**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Alternativer Antragstellername**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **D-TRUST SSL-Klasse 3 Zertifizierungsstelle 1 EV 2009**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Alternativer Antragstellername**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **DigiCert Cloud-Dienste CA-1**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **DigiCert SHA2 hohe Assurance Server Zertifizierungsstelle**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **DigiCert SHA2 sicheren Server Zertifizierungsstelle**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Entrust Zertifizierungsstelle - L1C**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Entrust Zertifizierungsstelle - L1K**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Informationen**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G2 Informationen**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Erweiterte Überprüfung Zertifizierungsstelle - SHA256 - G3 Informationen**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Informationen Organisation Validierung Zertifizierungsstelle - SHA256 - G2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Lassen Sie uns Behörde X3 verschlüsseln**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**AIA-URLs**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Microsoft IT TLS Zertifizierungsstelle 1**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Microsoft IT TLS Zertifizierungsstelle 2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Microsoft IT TLS Zertifizierungsstelle 4**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Microsoft IT TLS Zertifizierungsstelle 5**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Symantec Klasse 3 EV SSL CA - G3**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Alternativer Antragstellername**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Symantec Klasse 3 sicheren Server CA - G4**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Alternativer Antragstellername**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Thawte SHA256-SSL-Zertifizierungsstelle**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Alternativer Antragstellername**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
 **Verizon Akamai SureServer Zertifizierungsstelle G14-SHA2**
  
||
|:-----|
|**Subject**|
|:-----|
|**Aussteller**|
|:-----|
|**Seriennummer**|
|:-----|
|**Länge des öffentlichen Schlüssels**|
|:-----|
|**Signaturalgorithmus**|
|:-----|
|**Gültigkeit nicht vorher**|
|:-----|
|**Nicht nach Gültigkeit**|
|:-----|
|**Schüssel-ID**|
|:-----|
|**Autorität Schlüssel-ID**|
|:-----|
|**Fingerabdruck (SHA-1)**|
|:-----|
|**Fingerabdruck (SHA-256)**|
|:-----|
|**PIN-Nummer (SHA-256)**|
|:-----|
|**AIA-URLs**|
|:-----|
|**Zertifikatsperrlisten-URLs**|
|:-----|
|**OCSP-URLs**|
|:-----|
   
## <a name="additional-certificate-paths"></a>Weiteres Zertifikat Pfade
<a name="IntermediateCerts"> </a>

Folgendes umfassen legacy Zertifikate, die sind nicht über enthalten und mit der obigen Liste über einen Zeitraum zusammengeführt werden.
  
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



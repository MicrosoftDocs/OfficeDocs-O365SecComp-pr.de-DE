---
title: Technische Referenz Details über die Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Technische Details zu Verschlüsselung in Office 365 anzeigen.
ms.openlocfilehash: d86692119f7558d74e2083165b4eb6ab4a07da70
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529854"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Technische Referenz Details über die Verschlüsselung in Office 365

In diesem Artikel erfahren Sie mehr Informationen zu Zertifikaten finden Sie unter, Technologien und TLS für die [Verschlüsselung in Office 365](encryption.md)Suiten der Verschlüsselung. Dieser Artikel enthält auch Informationen zu geplanten veraltete.
  
- Wenn Sie weitere Informationen benötigen, finden Sie unter [Verschlüsselung in Office 365](encryption.md).
    
- Wenn Sie Informationen zum Setup angezeigt werden, finden Sie unter [Einrichten von Verschlüsselung in Office 365 Enterprise](set-up-encryption.md).
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Eigentümerschaft und Verwaltung des Microsoft Office 365-Zertifikats

Sie müssen keine Zertifikate für Office 365 kaufen oder verwalten, da Microsoft eigene Zertifikate verwendet.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>Aktuelle Verschlüsselungsstandards und geplante veraltete

Um weiterhin in puncto Verschlüsselung für Office 365 bereitstellen, prüft Microsoft regelmäßig unterstützte Verschlüsselungsstandards. In manchen Fällen müssen Sie die alte Standards verwerfen der, sobald sie veraltet und daher nicht so sicher sind. In diesem Thema werden derzeit unterstützte Verschlüsselungsanbieter-Suites und andere Standards sowie Details zu geplanten veraltete.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Von Office 365 unterstützte TLS-Versionen

Transport Layer Security (TLS) und SSL (vor TLS) sind kryptografische Protokolle, die die Kommunikation über ein Netzwerk mithilfe von Sicherheitszertifikaten sichern, die eine Verbindung zwischen Computern verschlüsseln. Office 365 unterstützt mehrere TLS-Versionen, darunter auch:
  
- TLS-Version 1.2 (TLS 1.2)
    
- TLS-Version 1.1 (TLS 1.1)
    
- TLS-Version 1.0 (TLS 1.0)
    
 Unterstützung für TLS 1.0 und TLS 1.1 wird 31 Oktober 2018 veraltet sein. Weitere Informationen finden Sie unter [Deprecating Unterstützung für TLS 1.0 und 1.1 und bedeutet für Sie](technical-reference-details-about-encryption.md#TLS11and12deprecation) . 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>Unterstützung für TLS 1.0 und 1.1 und bedeutet für Sie veralteter
<a name="TLS11and12deprecation"> </a>

Wichtige Änderungen werden zu unterstützten Optionen für Office 365 stehen zur Verfügung. Ab dem 31 Oktober 2018 unterstützt Office 365 nicht mehr die Verwendung von TLS 1.0 oder 1.1 für die Kommunikation mit Office 365. Nach Office 365 Unterstützung für diese Protokolle deprecates, wird die gesamte Kommunikation zu und von Office 365-Servern müssen TLS 1.2 verwenden. Informationen dazu, wie dies auswirkt finden Sie unter [Vorbereitung für die obligatorische Verwendung von TLS 1.2 in Office 365](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365). Server und Clients, die bei der Kommunikation mit Office 365 nach diesem Datum müssen TLS 1.2 unterstützen.
  
## <a name="deprecating-support-for-3des"></a>Unterstützung für 3DES veralteter
<a name="TLS11and12deprecation"> </a>

Ab dem 31 Oktober 2018 unterstützt Office 365 nicht mehr die Verwendung von 3DES Verschlüsselungsanbieter-Versionen für die Kommunikation mit Office 365. Genauer gesagt, wird in Office 365 TLS_RSA_WITH_3DES_EDE_CBC_SHA Chiffre-Suite nicht mehr unterstützt. Clients und Servern, die Kommunikation mit Office 365 nach diesem Datum mindestens eines der sicherer Chiffre unterstützen muss, die in diesem Thema aufgeführten (siehe [TLS-Verschlüsselung Suites von Office 365 unterstützt](technical-reference-details-about-encryption.md#TLSCipherSuites)).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Ende der SHA-1-Zertifikatunterstützung in Office 365
<a name="TLS11and12deprecation"> </a>

Ab Juni 2016 akzeptiert der Office 365 nicht mehr ein SHA-1-Zertifikat für ausgehend oder eingehend Verbindungen. Wenn Sie in der Zertifikatkette derzeit ein Zertifikat mit SHA-1 verwenden, müssen Sie zum Aktualisieren der Kette um SHA-2 (Secure Hash-Algorithmus-2) oder eine stärkere Hashalgorithmus verwenden.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Ende der RC4-Unterstützung in Office 365
<a name="TLS11and12deprecation"> </a>

Ab Juli 2015 endet die Unterstützung für die folgenden RC4-Verschlüsselungssammlungen:
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>Veralteter Secure Sockets Layer (SSL) 3.0-Unterstützung in Office 365
<a name="TLS11and12deprecation"> </a>

Starten 1 Dezember 2014 begann Office 365 das Deaktivieren der Unterstützung für SSL Secure Sockets Layer () 3.0, der Vorgänger TLS. Weitere Informationen finden Sie unter [Security advisory 3009008](https://technet.microsoft.com/library/security/3009008.aspx). Anweisungen zum, um sicherzustellen, dass Clients TLS 1.0 oder höher verwenden und zum Deaktivieren von SSL 3.0 finden Sie unter [Schützen von SSL 3.0 Sicherheitsrisiko](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/).
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>TLS-Verschlüsselung-Versionen von Office 365 unterstützt werden
<a name="TLSCipherSuites"> </a>

Eine Verschlüsselungssammlung ist eine Sammlung von Verschlüsselungsalgorithmen, die TLS verwendet, um sichere Verbindungen herzustellen. Von Office 365 unterstützte Verschlüsselungssammlungen werden in der folgenden Tabelle nach der Stärke aufgeführt, wobei die stärkste Verschlüsselungssammlung an erster Stelle steht. Wenn Office 365 eine Verbindungsanforderung empfängt, versucht Office 365 zunächst eine Verbindung mithilfe der obersten Verschlüsselungssammlung herzustellen. Falls dies nicht erfolgreich ist, wird die zweite Verschlüsselungssammlung in der Liste verwendet und so weiter. Wenn Office 365 eine Verbindungsanforderung an einen anderen Server oder einen Client sendet, wählt der empfangende Server oder Client die Verschlüsselungssammlung aus oder ob TLS überhaupt verwendet wird.
  
|**Protokolle**|**Name der Verschlüsselungssammlung**|**Schlüsselaustauschalgorithmus/Stärke**|**Unterstützung von Perfect Forward Secrecy**|**Authentifizierungsalgorithmus/Stärke**|**Verschlüsselung/Stärke**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |Ja  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |Ja  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |Ja  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |Ja  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_3DES_EDE_CBC_SHA  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |3DES/192  <br/> |
   
## <a name="related-topics"></a>Verwandte Themen
<a name="TLSCipherSuites"> </a>

[Verschlüsselung in Office 365](encryption.md)
  
[Einrichten von Verschlüsselung in Office 365 Enterprise.](set-up-encryption.md)
  
[Schannel-Implementierung von TLS 1.0 in Windows Sicherheitsupdate Status: 24 November 2015](https://support.microsoft.com/kb/3117336)
  
[Kryptografische TLS/SSL-Erweiterungen (Windows IT Center)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  


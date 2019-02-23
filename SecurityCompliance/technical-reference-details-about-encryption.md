---
title: Technische Details zur Verschlüsselung in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/15/2019
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Hier finden Sie technische Details zu Verschlüsselungs in Office 365.
ms.openlocfilehash: 77e12d0d4872d29e9cc33571b2cd5040d8d45677
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213625"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Technische Details zur Verschlüsselung in Office 365

In diesem Artikel erfahren Sie mehr über Zertifikate, Technologien und TLS-Verschlüsselungs Pakete [in Office 365](encryption.md). Dieser Artikel enthält auch Details zu geplanten Abschreibungen.
  
- Weitere Informationen finden Sie unter [Encryption in Office 365](encryption.md).
- Weitere Informationen finden Sie unter [Einrichten der Verschlüsselung in Office 365 Enterprise](set-up-encryption.md).
- Informationen zu Verschlüsselungs Paketen, die von bestimmten Windows-Versionen unterstützt werden, finden Sie unter [Cipher Suites in TLS/SSL (Schannel SSP)](https://docs.microsoft.com/windows/desktop/SecAuthN/cipher-suites-in-schannel).
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Eigentümerschaft und Verwaltung des Microsoft Office 365-Zertifikats

Sie müssen keine Zertifikate für Office 365 kaufen oder verwalten, da Microsoft eigene Zertifikate verwendet.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>Aktuelle Verschlüsselungsstandards und geplante veraltetkeiten

Um weiterhin die erstklassige Verschlüsselung für Office 365 zu gewährleisten, prüft Microsoft regelmäßig die unterstützten Verschlüsselungsstandards. In einigen Fällen müssen alte Standards veraltet und daher nicht mehr gesichert werden. In diesem Thema werden derzeit unterstützte Verschlüsselungs Pakete und andere Standards sowie Details zu geplanten veraltetkeiten beschrieben. 

## <a name="fips-compliance-for-office-365"></a>FIPS-Konformität für Office 365
Alle von Office 365 unterstützten Verschlüsselungs Pakete verwenden Algorithmen, die unter FIPS 140-2 akzeptabel sind. Office 365 erbt FIPS-Validierungen von Windows (über SChannel). Weitere Informationen zu SChannel finden Sie unter [Cipher Suites in TLS/SSL (Schannel SSP)](https://docs.microsoft.com/windows/desktop/SecAuthN/cipher-suites-in-schannel).
  
## <a name="versions-of-tls-supported-by-office-365"></a>Von Office 365 unterstützte TLS-Versionen

Transport Layer Security (TLS) und SSL (vor TLS) sind kryptografische Protokolle, die die Kommunikation über ein Netzwerk mithilfe von Sicherheitszertifikaten sichern, die eine Verbindung zwischen Computern verschlüsseln. Office 365 unterstützt mehrere TLS-Versionen, darunter auch:
  
- TLS-Version 1.2 (TLS 1.2)
    
- TLS-Version 1.1 (TLS 1.1)
    
- TLS-Version 1.0 (TLS 1.0)
    
 TLS 1,0-und TLS 1,1-Unterstützung ist veraltet, 31. Oktober 2018. Weitere Informationen finden Sie unter [deprecated Support for TLS 1,0 and 1,1 und was das für Sie ist](technical-reference-details-about-encryption.md#TLS11and12deprecation) . 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>Veraltet Unterstützung für TLS 1,0 und 1,1 und was das für Sie ist
<a name="TLS11and12deprecation"> </a>

Vom 31. Oktober 2018 wird Office 365 nicht mehr unterstützt TLS 1,0 und 1,1. Dies führt dazu, dass Microsoft keine neuen Probleme beheben kann, die in Clients, Geräten oder Diensten gefunden werden, die eine Verbindung mit Office 365 mithilfe von TLS 1,0 und 1,1 herstellen.

Hinweis Dies bedeutet nicht, dass Office 365 TLS 1,0-und 1,1-Verbindungen blockiert. Es gibt kein offizielles Datum für das Deaktivieren oder Entfernen von TLS 1,0 und 1,1 im TLS-Dienst für Kundenverbindungen. Das endgültige Datum der Abwertung wird durch die Telemetrie des Kunden bestimmt und ist noch nicht bekannt. Nachdem eine Entscheidung getroffen wurde, wird es sechs Monate im Voraus eine Ankündigung geben, es sei denn, wir werden uns eines bekannten Kompromisses bewusst, in dem wir möglicherweise in weniger als sechs Monaten handeln müssen, um Kunden zu schützen, die die Dienste nutzen.

Sie sollten sicherstellen, dass alle Client-Server-und Browser-Server-Kombinationen TLS 1,2 (oder eine höhere Version) verwenden, um die Verbindung zu Office 365-Diensten zu gewährleisten. Möglicherweise müssen Sie bestimmte Kombinationen für Client-Server und Browser-Server aktualisieren. Informationen dazu, wie sich dies auf Sie auswirkt, finden Sie unter [Vorbereiten der obligatorischen Verwendung von TLS 1,2 in Office 365](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365).
  
## <a name="deprecating-support-for-3des"></a>VerAltete Unterstützung für 3DES
<a name="TLS11and12deprecation"> </a>

Vom 31. Oktober 2018 wird Office 365 die Verwendung von 3DES-Verschlüsselungs Paketen für die Kommunikation mit Office 365 nicht mehr unterstützen. Genauer gesagt, Office 365 unterstützt die TLS_RSA_WITH_3DES_EDE_CBC_SHA-Verschlüsselungssuite nicht mehr. Clients und Server, die mit O365 kommunizieren, müssen nach diesem Datum mindestens einen der sichereren Chiffren unterstützen, die in diesem Thema aufgeführt sind (siehe [von Office 365 unterstützte TLS-Verschlüsselungs Pakete](technical-reference-details-about-encryption.md#TLSCipherSuites)).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Ende der SHA-1-Zertifikatunterstützung in Office 365
<a name="TLS11and12deprecation"> </a>

Ab Juni 2016 akzeptiert Office 365 kein SHA-1-Zertifikat mehr für ausgehende oder eingehende Verbindungen. Wenn Sie derzeit ein Zertifikat mit SHA-1 in der Zertifikatkette verwenden, müssen Sie die Kette so aktualisieren, dass Sie SHA-2 (Secure Hash Algorithm 2) oder einen stärkeren Hashalgorithmus verwendet.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Ende der RC4-Unterstützung in Office 365
<a name="TLS11and12deprecation"> </a>

Ab Juli 2015 endet die Unterstützung für die folgenden RC4-Verschlüsselungssammlungen:
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>VerAltete SSL-Unterstützung (Secure Sockets Layer) 3,0 in Office 365
<a name="TLS11and12deprecation"> </a>

Ab dem 1. Dezember 2014 begann Office 365 mit der Deaktivierung der Unterstützung für Secure Sockets Layer (SSL) 3,0, dem Vorgänger von TLS. Weitere Informationen finden Sie unter [security advisory 3009008](https://technet.microsoft.com/library/security/3009008.aspx). Anweisungen dazu, wie Sie sicherstellen, dass Clients TLS 1,0 oder höher verwenden und SSL 3,0 deaktivieren, finden Sie unter [protectING ssl 3,0 Vulnerability](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/).
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Von Office 365 unterstützte TLS-Verschlüsselungs Pakete
<a name="TLSCipherSuites"> </a>

Eine Verschlüsselungssammlung ist eine Sammlung von Verschlüsselungsalgorithmen, die TLS verwendet, um sichere Verbindungen herzustellen. Von Office 365 unterstützte Verschlüsselungssammlungen werden in der folgenden Tabelle nach der Stärke aufgeführt, wobei die stärkste Verschlüsselungssammlung an erster Stelle steht. Wenn Office 365 eine Verbindungsanforderung empfängt, versucht Office 365 zunächst eine Verbindung mithilfe der obersten Verschlüsselungssammlung herzustellen. Falls dies nicht erfolgreich ist, wird die zweite Verschlüsselungssammlung in der Liste verwendet und so weiter. Wenn Office 365 eine Verbindungsanforderung an einen anderen Server oder einen Client sendet, wählt der empfangende Server oder Client die Verschlüsselungssammlung aus oder ob TLS überhaupt verwendet wird.

> [!IMPORTANT]
> Beachten Sie, dass die TLS-Versionen veraltet sind und dass veraltete Versionen *nicht verwendet werden sollten* , wenn neuere Versionen verfügbar sind. In anderen Worten: überall dort, wo es aufgeführt ist, dass TLS 1,0, 1,1 und 1,2 unterstützt werden, wählen Sie die *neueste* Version (TLS 1,2) aus.
  
|**Protokolle**|**Name der Verschlüsselungssammlung**|**Schlüsselaustauschalgorithmus/Stärke**|**Unterstützung von Perfect Forward Secrecy**|**Authentifizierungsalgorithmus/Stärke**|**Verschlüsselung/Stärke**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384  <br/> |ECDH/192  <br/> |Ja  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256  <br/> |ECDH/128  <br/> |Ja  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |Ja  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |Ja  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |Ja  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |Ja  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |Nein  <br/> |RSA/112  <br/> |AES/128  <br/> |
   
## <a name="related-topics"></a>Verwandte Themen
[TLS-Verschlüsselungs Pakete in Windows 10 v1607](https://docs.microsoft.com/windows/desktop/SecAuthN/tls-cipher-suites-in-windows-10-v1607)

[Verschlüsselung in Office 365](encryption.md)
  
[Einrichten der Verschlüsselung in Office 365 Enterprise](set-up-encryption.md)
  
[SChannel-Implementierung von TLS 1,0 im Windows-Sicherheitsstatus Update: 24. November 2015](https://support.microsoft.com/kb/3117336)
  
[TLS/SSL-VerschlüsselungsErweiterungen (Windows IT Center)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  


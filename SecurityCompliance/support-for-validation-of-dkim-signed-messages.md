---
title: Unterstützung für die Validierung von mit DKIM signierten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: Exchange Online Protection (EOP) und Exchange Online unterstützen die eingehende Validierung von Domain Keys Identified Mail(DKIM)-Nachrichten. DKIM ist eine Methode, anhand derer validiert wird, dass eine Nachricht von der angegebenen Domian stammt und nicht von jemand anderem gefälscht wurde. Durch sie wird eine E-Mail mit der Organisation verbunden, die für deren Senden verantwortlich ist. Die DKIM-Verifizierung steht automatisch für alle Nachrichten zur Verfügung, die über IPv6 gesendet werden. Weitere Informationen zur Unterstützung von IPv6 finden Sie unter Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6.
ms.openlocfilehash: d2fab69847732bb7ed54f943d2c7845e06084936
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002260"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Unterstützung für die Validierung von mit DKIM signierten Nachrichten

Exchange Online Protection (EOP) und Exchange Online unterstützen die eingehende Validierung von Domain Keys Identified Mail([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt))-Nachrichten. DKIM ist eine Methode, anhand derer validiert wird, dass eine Nachricht von der angegebenen Domian stammt und nicht von jemand anderem gefälscht wurde. Durch sie wird eine E-Mail mit der Organisation verbunden, die für deren Senden verantwortlich ist. Die DKIM-Verifizierung steht automatisch für alle Nachrichten zur Verfügung, die über IPv6 gesendet werden. Weitere Informationen zur Unterstützung von IPv6 finden Sie unter [Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).
  
DKIM validiert eine digital signierte Nachricht, die im DKIM-Signaturkopf in Nachrichtenkopfzeilen angezeigt wird. Die Ergebnisse einer DKIM-Signaturvalidierung werden in den Kopf mit Authentifizierungsergebnissen gestempelt, der RFC 7001 ([Nachrichtenkopfzeilenfeld für die Angabe des Authentifizierungsstatus der Nachricht](https://www.rfc-editor.org/rfc/rfc7001.txt)) entspricht. Der Nachrichtenkopftext sieht in etwa folgendermaßen aus (wobei "contoso.com" der Sender ist):
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Administratoren können Exchange-[Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) für die Ergebnisse einer DKIM-Validierung erstellen, um Nachrichten bei Bedarf zu filtern oder weiterzuleiten. 
  


---
title: Unterstützung für die Validierung von mit DKIM signierten Nachrichten
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: Informationen zur Validierung von DKIM-signierten Nachrichten in Exchange Online Protection und Exchange Online
ms.openlocfilehash: b1e2af0511c3aa9eb819206aa859ad96e834e3ec
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260243"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Unterstützung für die Validierung von mit DKIM signierten Nachrichten

Exchange Online Protection (EOP) und Exchange Online unterstützen die eingehende Validierung von Domain Keys Identified Mail([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt))-Nachrichten. DKIM ist eine Methode, anhand derer validiert wird, dass eine Nachricht von der angegebenen Domian stammt und nicht von jemand anderem gefälscht wurde. Durch sie wird eine E-Mail mit der Organisation verbunden, die für deren Senden verantwortlich ist. Die DKIM-Verifizierung steht automatisch für alle Nachrichten zur Verfügung, die über IPv6 gesendet werden. Weitere Informationen zur Unterstützung von IPv6 finden Sie unter [Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).
  
DKIM validiert eine digital signierte Nachricht, die im DKIM-Signaturkopf in Nachrichtenkopfzeilen angezeigt wird. Die Ergebnisse einer DKIM-Signaturvalidierung werden in den Kopf mit Authentifizierungsergebnissen gestempelt, der RFC 7001 ([Nachrichtenkopfzeilenfeld für die Angabe des Authentifizierungsstatus der Nachricht](https://www.rfc-editor.org/rfc/rfc7001.txt)) entspricht. Der Nachrichtenkopftext sieht in etwa folgendermaßen aus (wobei "contoso.com" der Sender ist):
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Administratoren können Exchange [-Nachrichtenfluss Regeln](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) (auch bekannt als Transportregeln) für die Ergebnisse einer DKIM-Validierung erstellen, um Nachrichten bei Bedarf zu filtern oder weiterzuleiten. 
  


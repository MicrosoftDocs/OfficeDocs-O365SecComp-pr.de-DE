---
title: Unterstützung für die Validierung von mit DKIM signierten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: Erfahren Sie mehr über die Validierung von mit DKIM signierten Nachrichten in Exchange Online Protection und Exchange Online
ms.openlocfilehash: 22f0d1c4fdd6b1e159db732d6ef3d956efbf99c9
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255830"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Unterstützung für die Validierung von mit DKIM signierten Nachrichten

Exchange Online Protection (EOP) und Exchange Online unterstützen die eingehende Validierung von Domain Keys Identified Mail([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt))-Nachrichten. DKIM ist eine Methode, anhand derer validiert wird, dass eine Nachricht von der angegebenen Domian stammt und nicht von jemand anderem gefälscht wurde. Durch sie wird eine E-Mail mit der Organisation verbunden, die für deren Senden verantwortlich ist. Die DKIM-Verifizierung steht automatisch für alle Nachrichten zur Verfügung, die über IPv6 gesendet werden. Weitere Informationen zur Unterstützung von IPv6 finden Sie unter [Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).
  
DKIM validiert eine digital signierte Nachricht, die im DKIM-Signaturkopf in Nachrichtenkopfzeilen angezeigt wird. Die Ergebnisse einer DKIM-Signaturvalidierung werden in den Kopf mit Authentifizierungsergebnissen gestempelt, der RFC 7001 ([Nachrichtenkopfzeilenfeld für die Angabe des Authentifizierungsstatus der Nachricht](https://www.rfc-editor.org/rfc/rfc7001.txt)) entspricht. Der Nachrichtenkopftext sieht in etwa folgendermaßen aus (wobei "contoso.com" der Sender ist):
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Administratoren können Exchange [Mail Flow Regeln](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) (auch als Transportregeln bezeichnet) für die Ergebnisse einer DKIM-Validierung gefiltert oder Weiterleiten von Nachrichten als erforderlich. 
  


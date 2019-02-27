---
title: Vermeiden von ungültigen Zeichen in ihren spamfilterregeln und der Spamfilter Richtlinie
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Stellt Hilfe für Administratoren bereit, die in ihrer Antispamsoftware ungültige Zeichen enthalten und beim Versuch, das Security &amp; Compliance Center zu verwenden, Probleme auftreten.
ms.openlocfilehash: 90cf89d019a34658b676f02baa84c70f27200262
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276076"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Vermeiden ungültiger Zeichen in den spamfilterregeln und der Spamfilter Richtlinie 

Zuvor richteten Office 365-Administratoren die spamfilterregeln und die Spamfilter Richtlinie mithilfe der Exchange-Verwaltungskonsole ein. Verwenden Sie jetzt das Security &amp; Compliance Center, um die Antispamsoftware zu verwalten. Die folgenden Zeichen wurden in der Exchange-verwaltungsKONSOLE unterstützt, werden jedoch für die &amp; Verwendung im Security Compliance Center nicht unterstützt.  

**Ungültige Zeichen:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Wenn Ihre spamfilterregeln oder Ihre Spamfilter Richtlinie ungültige Zeichen enthält, können die folgenden Probleme auftreten:
- Möglicherweise können Sie die Richtlinie oder Regeln im Security &amp; Compliance Center nicht finden.
- Möglicherweise erhalten Sie Fehler, wenn Sie versuchen, die Regeln oder Richtlinien mithilfe von Windows PowerShell abzurufen.
- Möglicherweise stellen Sie fest, dass die Richtlinie oder die Einstellungen nicht wie erwartet ausgeführt werden.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Entfernen der ungültigen Zeichen aus der Spamfilter Richtlinie und den Regeln

Nachdem Sie die Richtlinie und Regeln identifiziert haben, die ungültige Zeichen enthalten, können Sie die Namen mithilfe der Windows PowerShell-Cmdlets ändern. 

1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Führen Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum wie folgt aus, um den Namen der Spamfilter Richtlinie zu ändern:
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Führen Sie das Cmdlet Set-HostedContentFilterRule wie folgt aus, um den Namen einer Spamfilter Regel zu ändern:
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Weitere Informationen

[Bedrohungs Verwaltung im Security &amp; Compliance Center](threat-management.md)
  
[Set-Hostedcontentfilterpolicy dient zum](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Set-HostedContentFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)

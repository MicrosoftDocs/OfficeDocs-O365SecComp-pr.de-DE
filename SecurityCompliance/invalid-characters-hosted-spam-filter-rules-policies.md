---
title: Vermeiden Sie ungültige Zeichen in Ihre Spam-Filter-Regeln und die Filterrichtlinie für spam
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Bietet Unterstützung für Administratoren, die ungültige Zeichen in ihrer Konfiguration Anti-Spam- und ausgeführt haben Probleme bei dem Versuch, verwenden Sie die Sicherheit &amp; Compliance Center.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018734"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Ungültige Zeichen in Ihren Spam-Filter-Regeln zu vermeiden und Spam-Filterrichtlinie 

Bisher Office 365-Administratoren eingerichtet und konfiguriert Spam-Filterregeln und die Spam-Filter-Richtlinie mithilfe der Exchange Admin Center (EAC). Nun, verwenden Sie die Sicherheit &amp; Compliance Center zum Verwalten der Ihr Anti-Spam-Konfiguration. Die folgenden Zeichen wurden in der Exchange-Verwaltungskonsole unterstützt jedoch nicht für die Verwendung in das Wertpapier &amp; Compliance Center.  

**Ungültige Zeichen:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Wenn Ihre Spam-Filter-Regeln oder Ihre Spam-Filter-Richtlinie die ungültige Zeichen enthält, können Sie einige oder alle der folgenden Probleme auftreten:
- Eventuell ist es nicht den Richtlinien oder Regeln in das Wertpapier gefunden &amp; Compliance Center.
- Sie erhalten Fehler, wenn Sie versuchen, die Regeln oder Richtlinien mithilfe von Windows PowerShell abrufen.
- Sie möglicherweise feststellen, dass die Richtlinie oder Einstellungen nicht ausgeführt oder wie erwartet ausgeführt werden.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Entfernen Sie die ungültigen Zeichen aus der Richtlinie für Spam-Filter und Regeln

Nachdem Sie die Richtlinien und Regeln, die ungültige Zeichen enthalten, identifiziert haben, können Sie die Namen mithilfe von Windows PowerShell-Cmdlets ändern. 

1. [Verbindung mit Exchange Online mit Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Führen Sie das Cmdlet Set-HostedContentFilterPolicy, um den Namen der Richtlinie Spam-Filter zu ändern, wie folgt aus:
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Führen Sie das Cmdlet Set-HostedContentFilterRule, um den Namen der Regel ein Spam-Filter zu ändern, wie folgt aus:
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Weitere Informationen

[Verfahren zum Erstellen von Management in das Wertpapier &amp; Compliance Center](threat-management.md)
  
[Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Set-HostedContentFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)

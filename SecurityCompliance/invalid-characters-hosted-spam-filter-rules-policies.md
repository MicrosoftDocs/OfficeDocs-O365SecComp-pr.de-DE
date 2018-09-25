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
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="d3eab-103">Ungültige Zeichen in Ihren Spam-Filter-Regeln zu vermeiden und Spam-Filterrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d3eab-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="d3eab-p101">Bisher Office 365-Administratoren eingerichtet und konfiguriert Spam-Filterregeln und die Spam-Filter-Richtlinie mithilfe der Exchange Admin Center (EAC). Nun, verwenden Sie die Sicherheit &amp; Compliance Center zum Verwalten der Ihr Anti-Spam-Konfiguration. Die folgenden Zeichen wurden in der Exchange-Verwaltungskonsole unterstützt jedoch nicht für die Verwendung in das Wertpapier &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="d3eab-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="d3eab-107">**Ungültige Zeichen:**</span><span class="sxs-lookup"><span data-stu-id="d3eab-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="d3eab-108">Wenn Ihre Spam-Filter-Regeln oder Ihre Spam-Filter-Richtlinie die ungültige Zeichen enthält, können Sie einige oder alle der folgenden Probleme auftreten:</span><span class="sxs-lookup"><span data-stu-id="d3eab-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="d3eab-109">Eventuell ist es nicht den Richtlinien oder Regeln in das Wertpapier gefunden &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="d3eab-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="d3eab-110">Sie erhalten Fehler, wenn Sie versuchen, die Regeln oder Richtlinien mithilfe von Windows PowerShell abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3eab-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="d3eab-111">Sie möglicherweise feststellen, dass die Richtlinie oder Einstellungen nicht ausgeführt oder wie erwartet ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3eab-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="d3eab-112">Entfernen Sie die ungültigen Zeichen aus der Richtlinie für Spam-Filter und Regeln</span><span class="sxs-lookup"><span data-stu-id="d3eab-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="d3eab-113">Nachdem Sie die Richtlinien und Regeln, die ungültige Zeichen enthalten, identifiziert haben, können Sie die Namen mithilfe von Windows PowerShell-Cmdlets ändern.</span><span class="sxs-lookup"><span data-stu-id="d3eab-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="d3eab-114">[Verbindung mit Exchange Online mit Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d3eab-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="d3eab-115">Führen Sie das Cmdlet Set-HostedContentFilterPolicy, um den Namen der Richtlinie Spam-Filter zu ändern, wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d3eab-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="d3eab-116">Führen Sie das Cmdlet Set-HostedContentFilterRule, um den Namen der Regel ein Spam-Filter zu ändern, wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d3eab-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="d3eab-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3eab-117">For more information</span></span>

[<span data-ttu-id="d3eab-118">Verfahren zum Erstellen von Management in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d3eab-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="d3eab-119">Set-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="d3eab-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="d3eab-120">Set-HostedContentFilterRule</span><span class="sxs-lookup"><span data-stu-id="d3eab-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)

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
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="62a82-103">Vermeiden ungültiger Zeichen in den spamfilterregeln und der Spamfilter Richtlinie</span><span class="sxs-lookup"><span data-stu-id="62a82-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="62a82-p101">Zuvor richteten Office 365-Administratoren die spamfilterregeln und die Spamfilter Richtlinie mithilfe der Exchange-Verwaltungskonsole ein. Verwenden Sie jetzt das Security &amp; Compliance Center, um die Antispamsoftware zu verwalten. Die folgenden Zeichen wurden in der Exchange-verwaltungsKONSOLE unterstützt, werden jedoch für die &amp; Verwendung im Security Compliance Center nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62a82-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="62a82-107">**Ungültige Zeichen:**</span><span class="sxs-lookup"><span data-stu-id="62a82-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="62a82-108">Wenn Ihre spamfilterregeln oder Ihre Spamfilter Richtlinie ungültige Zeichen enthält, können die folgenden Probleme auftreten:</span><span class="sxs-lookup"><span data-stu-id="62a82-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="62a82-109">Möglicherweise können Sie die Richtlinie oder Regeln im Security &amp; Compliance Center nicht finden.</span><span class="sxs-lookup"><span data-stu-id="62a82-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="62a82-110">Möglicherweise erhalten Sie Fehler, wenn Sie versuchen, die Regeln oder Richtlinien mithilfe von Windows PowerShell abzurufen.</span><span class="sxs-lookup"><span data-stu-id="62a82-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="62a82-111">Möglicherweise stellen Sie fest, dass die Richtlinie oder die Einstellungen nicht wie erwartet ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="62a82-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="62a82-112">Entfernen der ungültigen Zeichen aus der Spamfilter Richtlinie und den Regeln</span><span class="sxs-lookup"><span data-stu-id="62a82-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="62a82-113">Nachdem Sie die Richtlinie und Regeln identifiziert haben, die ungültige Zeichen enthalten, können Sie die Namen mithilfe der Windows PowerShell-Cmdlets ändern.</span><span class="sxs-lookup"><span data-stu-id="62a82-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="62a82-114">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="62a82-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="62a82-115">Führen Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum wie folgt aus, um den Namen der Spamfilter Richtlinie zu ändern:</span><span class="sxs-lookup"><span data-stu-id="62a82-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="62a82-116">Führen Sie das Cmdlet Set-HostedContentFilterRule wie folgt aus, um den Namen einer Spamfilter Regel zu ändern:</span><span class="sxs-lookup"><span data-stu-id="62a82-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="62a82-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62a82-117">For more information</span></span>

[<span data-ttu-id="62a82-118">Bedrohungs Verwaltung im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="62a82-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="62a82-119">Set-Hostedcontentfilterpolicy dient zum</span><span class="sxs-lookup"><span data-stu-id="62a82-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="62a82-120">Set-HostedContentFilterRule</span><span class="sxs-lookup"><span data-stu-id="62a82-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)

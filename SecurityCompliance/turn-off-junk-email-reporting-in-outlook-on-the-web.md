---
title: Deaktivieren der junk-e-Berichte in Outlook im Web
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Als ein Office 365-Administrator können Sie die Möglichkeit für die Personen auf Bericht e-Mails als Junk-e-deaktivieren.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272040"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="1aa74-103">Deaktivieren der junk-e-Berichte in Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="1aa74-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="1aa74-p101">Sie können für die Analyse mithilfe der Outlook auf das Web junk-e-Optionen, reporting, wie beschrieben in den [junk-e-Bericht und Phishing-Mails in Outlook im Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)Junk, Phishing und nicht-junknachrichten an Microsoft senden. Wenn Sie keine dieser Optionen verwenden möchten, können Administratoren diese über das Cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1aa74-p101">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1aa74-106">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="1aa74-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="1aa74-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="1aa74-107"></span></span>

- <span data-ttu-id="1aa74-108">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="1aa74-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="1aa74-p102">Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "Outlook Web App-Postfachrichtlinien" im Thema [Outlook Web App-Berechtigungen](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) .</span><span class="sxs-lookup"><span data-stu-id="1aa74-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Outlook Web App mailbox policies" entry in the [Outlook Web App permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 
    
- <span data-ttu-id="1aa74-111">Vor dem Ausführen der Cmdlets zum Deaktivieren von Berichten zur junk-e-Mail-erforderlich sind, kann es hilfreich sein, lesen Sie die Informationen in den Themen [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) und [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) sein.</span><span class="sxs-lookup"><span data-stu-id="1aa74-111">Before you run the cmdlets required to turn off junk email reporting, it might be helpful to review the reference information in the [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) topics.</span></span> 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="1aa74-112">Schalten Sie junk, Phishing und keine Junk-Mails an Microsoft</span><span class="sxs-lookup"><span data-stu-id="1aa74-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="1aa74-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="1aa74-113"></span></span>

<span data-ttu-id="1aa74-114">Führen Sie zuerst das folgende Cmdlet aus, um die virtuellen Verzeichnisse abzurufen, für die Sie die Meldung deaktivieren möchten:</span><span class="sxs-lookup"><span data-stu-id="1aa74-114">First, run the following cmdlet to get the virtual directories for which you want to turn off reporting:</span></span>
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

<span data-ttu-id="1aa74-115">Führen Sie dann das folgende Cmdlet aus, um die Meldung von Junk- und Nicht-Junk-E-Mails an Microsoft zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="1aa74-115">Next, run the following cmdlet to turn off junk and not junk reporting to Microsoft:</span></span>
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

<span data-ttu-id="1aa74-116">Mit dem folgenden Cmdlet wird beispielsweise die Meldung für das virtuelle Verzeichnis "Contoso\owa" deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="1aa74-116">For example, the following cmdlet turns off reporting for virtual directory Contoso\owa:</span></span>
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="1aa74-117">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="1aa74-117">How do you know this worked?</span></span>
<span data-ttu-id="1aa74-118"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="1aa74-118"></span></span>

<span data-ttu-id="1aa74-p103">Führen Sie Get-OWAMailboxPolicy, um die Parameterwerte zu prüfen und dann Outlook im Web zugreifen, und stellen Sie sicher, dass die Optionen zum Melden von Junk-e-, Phishing, und nicht auf Junk-e-nicht verfügbar sind. Sie werden möglicherweise trotzdem Nachrichten als Junk-e-, Phishing markieren und keine Junk-e-, aber nicht möglich, diese zu melden.</span><span class="sxs-lookup"><span data-stu-id="1aa74-p103">Run Get-OWAMailboxPolicy to check the parameter values, and then access Outlook on the web and verify that the options to report junk, phishing, and not junk are not available. You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
  


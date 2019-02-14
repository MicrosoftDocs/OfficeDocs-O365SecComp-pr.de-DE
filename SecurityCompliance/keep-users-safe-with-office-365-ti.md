---
title: Schützen von Office 365-Benutzern mit Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection: M365-security-compliance
description: Hier erfahren Sie, wie Office 365 Bedrohungsanalyse Ihrer Organisation Angriffe und Bedrohungen, erkennen und schnell zu mindern und Wiederherstellen von Bedrohungen helfen kann.
ms.openlocfilehash: c049e6f811eec8a30eb2b94361f8cdcbdaa8ac49
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995366"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="bc81a-103">Schützen von Office 365-Benutzern mit Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="bc81a-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="bc81a-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bc81a-104">Overview</span></span>

<span data-ttu-id="bc81a-p101">Wissen Sie, welche Benutzer Office 365-Angriff erfolgt sind, oder schlechter - gefährdet? Wissen zu mindern und vor Angriffen, auf die Ihre Benutzer abzielen wiederherstellen? Wussten Sie, dass Sie genau mit Sicherheitsfunktionen möglich, die bereits im Office 365 verfügbar sind?</span><span class="sxs-lookup"><span data-stu-id="bc81a-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="bc81a-p102">[Office 365 Bedrohungsanalyse](office-365-ti.md) ist eine Reihe von Funktionen in Ihrem Office 365 E5 Abonnement enthalten. Office 365 Bedrohungsanalyse hat Microsoft IT durchschnittliche Zeit für Social-Engineering Vorfälle um 80 % und höheren Durchsatz Groß-/Kleinschreibung 37 % pro Monat im Vergleich zu den vorherigen 2 Quartale Problembehebung geholfen!</span><span class="sxs-lookup"><span data-stu-id="bc81a-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="bc81a-p103">Im Februar 2019 beginnen und anschließend in den nächsten Monaten einführen, gewinnt Office 365 Bedrohungsanalyse Office 365 erweiterte Threat Protection Plan 2, mit zusätzlichen Bedrohung Schutzfunktionen. Finden Sie weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="bc81a-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="bc81a-p104">Wir haben kürzlich neue Funktionen zur Verbesserung von zum Erkennen und Wiederherstellen von Bedrohungen hinzugefügt! Hier ist eine schnelle Einführung in der wie der aktualisierte Bedrohungsanalyse Dienst noch effizienter werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="bc81a-114">Angriffe und Bedrohungen erkennen</span><span class="sxs-lookup"><span data-stu-id="bc81a-114">Detect intrusions and threats</span></span>

<span data-ttu-id="bc81a-p105">[Explorer](use-explorer-in-security-and-compliance.md) (auch als Bedrohung Explorer bezeichnet) unterstützt Sie bei Security-Admins und Analysten identifizieren und verstehen Bedrohungen, die in Ihrem Unternehmen aktiviert sind, da die komplexen Sicherheitseinstellungen durch scheinbar harmlose Benutzerkonfigurationen wie sichere umgangen werden können weißen Liste der Absender. Explorer hilft bei Office 365 globaler oder Sicherheit-Admins schnell ermitteln, ob Benutzer von Bedrohungen wie Malware oder Phishing gefährdet sind. Auf diese Weise priorisieren die Benutzer am häufigsten für eine Bedrohung und die erforderlichen Antwort gefährdet sind.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="bc81a-p106">Explorer kann Administratoren die Beziehungen zwischen Benutzer und e-Mail zu navigieren. Eine bestimmte e-Mail-Nachricht, die falsche wurde bekannt? Suchen Sie nach, um herauszufinden, welche Benutzer die e-Mail-Nachricht erhalten, führen Sie die Reihe von Ereignissen und finden Sie unter Was diese Benutzer wiederum getan haben.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="bc81a-p107">Wenn Sie Bedrohungsanalyse, [versuchen Sie es jetzt](https://aka.ms/tryo365threatintel3)noch nicht! Und [erfahren Sie mehr über Office 365 Bedrohungsanalyse](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="bc81a-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Screenshot der Bedrohung Explorer in Office 365, farbcodierte durch Malware-Familie](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="bc81a-124">Schnell zu mindern und Wiederherstellen von Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="bc81a-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="bc81a-p108">Sobald-Admins Sicherheit etwas verdächtigen oder böswilliges passiert in ihre Mandanten identifiziert haben, können sie schnell enthalten und reagieren auf diese Bedrohung mit **Vorfall Framework**. Gruppieren von unerwünschten Nachrichten mit nur einem Klick und schnell entfernen, die e-Mail-Nachrichten des Benutzers Postfächer.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="bc81a-p109">**UPDATE:** Wir haben die Möglichkeit zum Löschen (oder weiche löschen)-e-Mails direkt aus dem Vorfall Framework kürzlich hinzugefügt. Zuvor konnte Administratoren nur e-Mails in Junk-e-Ordner eines Benutzers, verschieben, in dem Benutzer das Element wiederherstellen können. Mit den Funktionen für neu veröffentlichten löschen können Sie jetzt sicher sein, dass ein bösartiger oder unerwünschten e-Mail-Nachrichten dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="bc81a-p110">Wenn Sie Bedrohungsanalyse, [versuchen Sie es jetzt](https://aka.ms/tryo365threatintel3)noch nicht! Und [erfahren Sie mehr über Office 365 Bedrohungsanalyse](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="bc81a-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Screenshot der e-Mail-Liste der Vorfall-Wartung](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="bc81a-133">Nutzen Sie die Bedrohung Telemetrie von Microsoft</span><span class="sxs-lookup"><span data-stu-id="bc81a-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="bc81a-p111">Office 365 Bedrohungsanalyse eingeschaltet mit Daten aus dem Microsoft Intelligent Sicherheit Diagramm. Das Diagramm erhält das neueste Bedrohung Signal aus mehr als 1 Milliarde Windows-Geräten, 450 Milliarden monatliche Azure Anmeldungen und 400 Milliarden monatliche e-Mail-Nachrichten in Office 365. Dieses Signal hervorragende Bedrohung ist, was die Tiefe Einblicke in einen Mandanten Kunden ermöglicht, die für Administratoren und Sicherheit Analysten haben eine vollständige Übersicht über die Bedrohungen Beeinträchtigung ihrer Organisation entscheidend ist.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="bc81a-137">Weitere Informationen folgen</span><span class="sxs-lookup"><span data-stu-id="bc81a-137">More to come</span></span>

<span data-ttu-id="bc81a-p112">Dies sind nur einige Beispiele für Office 365 Bedrohungsanalyse Sie Ihrem Unternehmen secure Schutzmechanismen in! In den nächsten Wochen werden wir erhebliche Verbesserungen einschließlich das Produkt hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bc81a-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="bc81a-140">Liefert Einblicke in potenziell gefährliche Aktionen, die für Exchange Online-e-Mail- und SharePoint Online-Dokumente</span><span class="sxs-lookup"><span data-stu-id="bc81a-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="bc81a-141">Was einen Einblick in böswilliger Phishing-e-Mails, die an Benutzer gesendet wurden, einschließlich derjenigen, die haben möglicherweise wurde empfangen und Lesen von Benutzern, bevor sie weaponized wurden</span><span class="sxs-lookup"><span data-stu-id="bc81a-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="bc81a-142">Erhöhen den Satz von Aktionen-Admins durchführen kann, um auf Vorfälle zu reagieren</span><span class="sxs-lookup"><span data-stu-id="bc81a-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="bc81a-143">Warum Bedrohung Intelligence?</span><span class="sxs-lookup"><span data-stu-id="bc81a-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="bc81a-p113">Gartner schätzt, dass im 2017 allein über $90B für Sicherheit im Internet ausgegeben wurde. SID Deshpande, principal Research Analyst bei Gartner, ist eine in Anführungszeichen als besagt, dass "der Branche Verbreitung von Erkennung und Antwort... sendet eine klare Meldung, dass Prevention zwecklos ist, es sei denn, es in einer Funktion Erkennung und Antwort gebunden ist." Bedrohungsanalyse ist ein wichtiger Bestandteil jedes Unternehmen Portfolio von Diensten und als eigenständigen Dienst oder als Teil von Office 365 E5 verbraucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc81a-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="bc81a-148">Was kommt als nächstes</span><span class="sxs-lookup"><span data-stu-id="bc81a-148">What's Next</span></span>

- <span data-ttu-id="bc81a-149">Erfahren Sie mehr über Office 365 Bedrohungsanalyse in dieser Sitzung aufgezeichneten: [Hingegen bleiben, der die Cyber mit Office 365 Bedrohungsanalyse](https://myignite.microsoft.com/videos/53723)</span><span class="sxs-lookup"><span data-stu-id="bc81a-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="bc81a-150">[Probieren Sie nun für Office 365 Threat Intelligence](https://aka.ms/tryo365threatintel3) oder Ihre Testversion von Office E5 heute beginnen!</span><span class="sxs-lookup"><span data-stu-id="bc81a-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    


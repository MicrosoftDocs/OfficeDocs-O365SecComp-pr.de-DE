---
title: Schützen von Office 365-Benutzern mit Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie mit Office 365 Threat Intelligence Ihr Unternehmen bei der Erkennung von Intrusionen und Bedrohungen unterstützen und schnell Bedrohungen verringern und wiederherstellen können.
ms.openlocfilehash: 40b39cc7f388152bd95000e2653ef94b970a6fa3
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241957"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="24ae0-103">Schützen von Office 365-Benutzern mit Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="24ae0-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="24ae0-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="24ae0-104">Overview</span></span>

<span data-ttu-id="24ae0-p101">Wissen Sie, welche Ihrer Office 365-Benutzer angegriffen oder verschlechtert werden? Wissen Sie, wie Sie Angriffe, die für Ihre Benutzer geeignet sind, verringern und wiederherstellen können? Wussten Sie, dass Sie genau dies mit Sicherheitsfunktionen tun können, die Ihnen in Office 365 bereits zur Verfügung stehen?</span><span class="sxs-lookup"><span data-stu-id="24ae0-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="24ae0-p102">[Office 365 Threat Intelligence](office-365-ti.md) ist eine Reihe von Funktionen, die in ihrem Office 365 E5-Abonnement enthalten sind. Office 365 Threat Intelligence hat dazu beigetragen, dass Microsoft IT die durchschnittliche Zeit bis zur Lösung von Social Engineering-Vorfällen um 80% und den Fall Durchsatz um 37% pro Monat im Vergleich zu den vorherigen 2 Quartalen gesenkt hat.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="24ae0-p103">Beginnend im Februar 2019 und über die nächsten Monate hinaus wird Office 365 Threat Intelligence zu Office 365 Advanced Threat Protection Plan 2 mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="24ae0-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="24ae0-p104">Wir haben vor kurzem neue Funktionen hinzugefügt, um zu verbessern, wie Sie Bedrohungen aufspüren und wiederherstellen können. Hier erfahren Sie, wie Sie mit dem aktualisierten Threat Intelligence Service noch effizienter arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="24ae0-114">Erkennung von Intrusionen und Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="24ae0-114">Detect intrusions and threats</span></span>

<span data-ttu-id="24ae0-p105">[Explorer](use-explorer-in-security-and-compliance.md) (auch als Bedrohungs-Explorer bezeichnet) unterstützt Sicherheitsadministratoren und Analysten bei der Identifizierung und dem Verständnis von Bedrohungen, die in Ihrem Unternehmen aktiv sind, da selbst die komplexesten Sicherheitseinstellungen durch scheinbar harmlose Benutzerkonfigurationen wie Safe umgangen werden können. Absender-Whitelists. Explorer hilft Office 365 globale oder Sicherheitsadministratoren schnell festzustellen, ob Benutzer durch Bedrohungen wie Schadsoftware oder Phishing kompromittiert wurden. Dies hilft bei der Priorisierung der Benutzer, die am stärksten gefährdet sind, und der erforderlichen Antwort.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="24ae0-p106">Der Explorer unterstützt auch Administratoren beim Navigieren in den Beziehungen zwischen Benutzern und e-Mails. Kennen Sie eine bestimmte e-Mail, die schlecht war? Suchen Sie nach der Nachricht, um zu sehen, welche Benutzer die e-Mail erhalten haben, und folgen Sie dann den Ereignisserien, und sehen Sie, was diese Benutzer wiederum getan haben.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="24ae0-p107">Wenn Sie noch keine Bedrohungsanalyse haben, [probieren Sie es](https://aka.ms/tryo365threatintel3)aus! Und [erfahren Sie mehr über Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="24ae0-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Screenshot von Threat Explorer in Office 365, farbig codiert nach Schadsoftware-Familie](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="24ae0-124">Schnelles verringern und Wiederherstellen von Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="24ae0-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="24ae0-p108">Sobald Sicherheitsadministratoren etwas verdächtiges oder böswilliges in Ihrem Mandanten erkannt haben, können Sie diese Bedrohung schnell mit dem **Vorfall Framework**enthalten und darauf reagieren. Gruppieren Sie unerwünschte Nachrichten mit einem Mausklick, und entfernen Sie die e-Mail-Nachrichten schnell aus den Postfächern Ihrer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="24ae0-p109">**Update:** Wir haben vor kurzem die Möglichkeit hinzugefügt, e-Mails (Soft oder Hard Delete) direkt aus dem Incident Framework zu löschen. Zuvor konnten Administratoren nur e-Mails in den Junk-Ordner eines Benutzers verschieben, in dem die Benutzer das Element wiederherstellen konnten. Mit den neu veröffentlichten Löschfunktionen können Sie nun sicher sein, dass eine böswillige oder unerwünschte e-Mail dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="24ae0-p110">Wenn Sie noch keine Bedrohungsanalyse haben, [probieren Sie es](https://aka.ms/tryo365threatintel3)aus! Und [erfahren Sie mehr über Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="24ae0-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Screenshot der e-Mail-Liste der Vorfall Sanierung](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="24ae0-133">Nutzen der Bedrohungs-Telemetrie von Microsoft</span><span class="sxs-lookup"><span data-stu-id="24ae0-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="24ae0-p111">Office 365 Threat Intelligence wird mit Daten aus dem Microsoft Intelligent Security-Diagramm betrieben. Der Graph erhält das neueste Bedrohungs Signal von über 1 Milliarde Windows-Geräten, 450 Milliarden monatlichen Azure-Anmeldungen und 400 Milliarden monatlichen e-Mail-Nachrichten in Office 365. Dieses unübertroffene Bedrohungs Signal gibt der umfassenden Sichtbarkeit eines Kundenmandanten, der für Administratoren und Sicherheitsanalysten entscheidend ist, eine umfassende Übersicht über die Bedrohungen, die sich auf Ihre Organisation auswirken.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="24ae0-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="24ae0-137">More to come</span></span>

<span data-ttu-id="24ae0-p112">Dies sind nur einige Beispiele dafür, wie Sie mit Office 365 Threat Intelligence Ihr Unternehmen sichern können. In den kommenden Wochen werden wesentliche Verbesserungen am Produkt hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="24ae0-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="24ae0-140">Bereitstellen von Einblicken in potenziell riskante Aktionen in Exchange Online-e-Mail-und SharePoint Online-Dokumenten</span><span class="sxs-lookup"><span data-stu-id="24ae0-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="24ae0-141">Bereitstellen von Einblicken in böswillige Phishing-e-Mail-Nachrichten, die an Benutzer gesendet wurden, einschließlich einiger, die möglicherweise von Benutzern empfangen und gelesen wurden, bevor Sie bewaffnet wurden</span><span class="sxs-lookup"><span data-stu-id="24ae0-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="24ae0-142">Erhöhen der Gruppe von Aktionen, die Administratoren ausführen können, um auf Vorfälle zu reagieren</span><span class="sxs-lookup"><span data-stu-id="24ae0-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="24ae0-143">Warum Threat Intelligence?</span><span class="sxs-lookup"><span data-stu-id="24ae0-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="24ae0-p113">Gartner schätzt, dass in 2017 allein mehr als $90B für Cyber verwendet wurde. Sid Deshpande, Principal Research Analyst bei Gartner, wird mit den Worten zitiert, dass "die Branche den Wechsel zu Erkennung und Antwort... sendet eine klare Meldung, dass die Prävention vergeblich ist, es sei denn, Sie ist an eine Erkennungs-und Reaktionsfunktion gebunden. " Threat Intelligence ist ein wichtiger Bestandteil des Portfolios an Diensten jedes Unternehmens und kann als eigenständiger Dienst oder als Teil von Office 365 E5 genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="24ae0-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="24ae0-148">Was kommt als nächstes</span><span class="sxs-lookup"><span data-stu-id="24ae0-148">What's Next</span></span>

- <span data-ttu-id="24ae0-149">Weitere Informationen zu Office 365 Threat Intelligence finden Sie in dieser aufgezeichneten Sitzung: [vor der Cyberattacken mit office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span><span class="sxs-lookup"><span data-stu-id="24ae0-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="24ae0-150">[Testen Sie jetzt office 365 Threat Intelligence](https://aka.ms/tryo365threatintel3) , oder starten Sie Ihren Office E5-Test noch heute!</span><span class="sxs-lookup"><span data-stu-id="24ae0-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    


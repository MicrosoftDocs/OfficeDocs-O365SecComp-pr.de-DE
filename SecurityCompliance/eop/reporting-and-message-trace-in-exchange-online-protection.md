---
title: Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft Exchange Online Protection (EOP) bietet viele verschiedene Berichte an, mit deren Hilfe Sie den allgemeinen Status und die Integrität Ihrer Organisation ermitteln können. Außerdem gibt es Tools, mit denen Sie die Problembehebung für bestimmte Ereignisse (wenn beispielsweise eine Nachricht nicht beim gewünschten Empfänger ankommt) durchführen können, sowie Überwachungsberichte zur Einhaltung von Vorschriften. In der folgenden Tabelle sind die für EOP-Administratoren verfügbaren Berichte und Problembehandlungstools beschrieben.
ms.openlocfilehash: fcefa14991d074f1f4459007c16dd7f4df1cedd1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256273"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="8606a-105">Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8606a-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="8606a-106">Microsoft Exchange Online Protection (EOP) bietet viele verschiedene Berichte an, mit deren Hilfe Sie den allgemeinen Status und die Integrität Ihrer Organisation ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="8606a-106">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="8606a-107">Außerdem gibt es Tools, mit denen Sie die Problembehebung für bestimmte Ereignisse (wenn beispielsweise eine Nachricht nicht beim gewünschten Empfänger ankommt) durchführen können, sowie Überwachungsberichte zur Einhaltung von Vorschriften.</span><span class="sxs-lookup"><span data-stu-id="8606a-107">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="8606a-108">Verwendungsberichte</span><span class="sxs-lookup"><span data-stu-id="8606a-108">Usage reports</span></span>

<span data-ttu-id="8606a-109">**Office 365-Gruppen-Aktivitäten** Anzeigen von Informationen zur Anzahl der Office 365-Gruppen, die erstellt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8606a-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="8606a-110">**E-Mail-Aktivität** Informationen zur Anzahl der Nachrichten, die in der gesamten Organisation sowie von einem bestimmten Benutzer gesendet, empfangen und gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="8606a-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="8606a-p103">**Nutzung der E-Mail-Apps** Zeigen Sie Informationen zu den verwendeten E-Mail-Apps an. Diese umfassen die Gesamtzahl der Verbindungen für die einzelnen Apps und die Versionen von Outlook, die eine Verbindung herstellen.  </span><span class="sxs-lookup"><span data-stu-id="8606a-p103">**Email app usage** View information about the email apps that are used. This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="8606a-113">**Postfachnutzung** Informationen zum verwendeten Speicherplatz, Verbrauch von Kontingenten, zur Elementanzahl und zu letzten Aktivitäten für Postfächer (Senden oder Lesen).</span><span class="sxs-lookup"><span data-stu-id="8606a-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="8606a-114">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="8606a-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="8606a-115">Office 365-Berichte im Admin Center-Office 365-Gruppen</span><span class="sxs-lookup"><span data-stu-id="8606a-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="8606a-116">Office 365-Berichte im Admin Center - E-Mail-Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="8606a-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="8606a-117">Office 365-Berichte im Admin Center - Nutzung der E-Mail-Apps</span><span class="sxs-lookup"><span data-stu-id="8606a-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="8606a-118">Office 365-Berichte im Admin Center - Postfachnutzung</span><span class="sxs-lookup"><span data-stu-id="8606a-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="8606a-119">Sicherheits &amp; Kompatibilitätsberichte im Microsoft 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="8606a-119">Security &amp; compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="8606a-120">Diese erweiterten Berichte bieten eine interaktive Berichterstellung für EOP-Administratoren, die Zusammenfassungsinformationen und das Anzeigen von Detailinformationen umfasst.</span><span class="sxs-lookup"><span data-stu-id="8606a-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="8606a-121">**Advanced Threat Protection (ATP)** Zeigt Informationen über sichere Links und sichere Anlagen, die zu ATP gehören.</span><span class="sxs-lookup"><span data-stu-id="8606a-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="8606a-122">**EoP** Informationen zu Malware-Entdeckungen, gefälschten e-Mails, Spam Entdeckungen und Nachrichtenübermittlung an und von Ihrer Organisation anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8606a-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="8606a-123">Anzeigen der Berichte zu Advanced Threat Protection und Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8606a-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="8606a-124">Benutzerdefinierte Berichte mithilfe von Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8606a-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="8606a-125">Programmgesteuertes Erstellen von Berichten, die im Microsoft 365 Admin Center mithilfe von Microsoft Graph verfügbar sind siehe Unterthemen zum [Arbeiten mit Office 365-Nutzungsberichten in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span><span class="sxs-lookup"><span data-stu-id="8606a-125">Programmatically create reports that are available in the Microsoft 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="8606a-126">Benutzerdefinierte Berichte mit Berichtswebdiensten</span><span class="sxs-lookup"><span data-stu-id="8606a-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="8606a-127">Erstellen Sie programmgesteuert Berichte aus den verfügbaren PowerShell-Cmdlets für Exchange Online Protection mithilfe der REST/ODATA2-Abfrage Filterung.</span><span class="sxs-lookup"><span data-stu-id="8606a-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="8606a-128">Weitere Informationen finden Sie unter [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span><span class="sxs-lookup"><span data-stu-id="8606a-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="8606a-129">Nachrichtenablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="8606a-129">Message trace</span></span>

<span data-ttu-id="8606a-p104">Ermöglicht das Nachverfolgen von E-Mails auf dem Weg durch EOP. Sie können ermitteln, ob eine E-Mail vom Dienst empfangen, abgelehnt, zurückgestellt oder zugestellt wurde. Außerdem werden die Aktionen der Nachricht gezeigt, bevor diese ihren finalen Status erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="8606a-p104">Follows email messages as they travel through EOP. You can determine if an email message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="8606a-133">Mit diesen Informationen können Sie in effizienter Weise Fragen der Benutzer beantworten, Probleme mit dem Nachrichtenfluss behandeln und Richtlinienänderungen überprüfen und müssen seltener den technischen Support um Unterstützung bitten.</span><span class="sxs-lookup"><span data-stu-id="8606a-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="8606a-134">Siehe [Ablaufverfolgung einer e-Mail-Nachricht](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span><span class="sxs-lookup"><span data-stu-id="8606a-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="8606a-135">Überwachungsprotokollierung</span><span class="sxs-lookup"><span data-stu-id="8606a-135">Audit logging</span></span>

<span data-ttu-id="8606a-136">Verfolgt bestimmte Änderungen durch Administratoren Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="8606a-136">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="8606a-137">Diese Berichte können Sie zum Behandeln von Konfigurationsproblemen sowie zum Ermitteln der Ursache von Sicherheits- oder Kompatibilitätsproblemen heranziehen.</span><span class="sxs-lookup"><span data-stu-id="8606a-137">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span>  <span data-ttu-id="8606a-138">Weitere Informationen finden Sie unter [Auditing Reports in EoP](auditing-reports-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="8606a-138">see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="8606a-139">Meldung und Verfügbarkeit und Latenz Nachrichtenverfolgungsdaten</span><span class="sxs-lookup"><span data-stu-id="8606a-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="8606a-140">In der folgenden Tabelle wird beschrieben, wann und für wie lange EOP-Berichte und Nachrichtenverfolgungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8606a-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="8606a-141">**Berichttyp**</span><span class="sxs-lookup"><span data-stu-id="8606a-141">**Report type**</span></span> <br/> |<span data-ttu-id="8606a-142">**Daten verfügbar für (Rückwirkungsfrist)**</span><span class="sxs-lookup"><span data-stu-id="8606a-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="8606a-143">**Latenz**</span><span class="sxs-lookup"><span data-stu-id="8606a-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="8606a-144">Zusammenfassungsberichte zum E-Mail-Schutz</span><span class="sxs-lookup"><span data-stu-id="8606a-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="8606a-145">90 Tage</span><span class="sxs-lookup"><span data-stu-id="8606a-145">90 days</span></span>  <br/> |<span data-ttu-id="8606a-p106">Die Aggregation von Nachrichtendaten ist meistens innerhalb von 24 bis 48 Stunden abgeschlossen. Kleinere inkrementelle, aggregierte Änderungen können bis zu 5 Tage lang auftreten.</span><span class="sxs-lookup"><span data-stu-id="8606a-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="8606a-148">Detailberichte zum E-Mail-Schutz</span><span class="sxs-lookup"><span data-stu-id="8606a-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="8606a-149">90 Tage</span><span class="sxs-lookup"><span data-stu-id="8606a-149">90 days</span></span>  <br/> |<span data-ttu-id="8606a-p107">Bei Detaildaten, die weniger als 7 Tage alt sind, sollten Daten innerhalb von 24 Stunden erscheinen, sind aber möglicherweise erst 48 Stunden später abgeschlossen. Einige kleinere schrittweise Änderungen können bis zu 5 Tagen dauern.</span><span class="sxs-lookup"><span data-stu-id="8606a-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="8606a-152">Zum Anzeigen von Detailberichten für Nachrichten, die älter als 7 Tage sind, kann es einige Stunden dauern, bis die Ergebnisse der Nachrichtenablaufverfolgung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8606a-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="8606a-153">Daten der Nachrichtenablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="8606a-153">Message trace data</span></span>  <br/> |<span data-ttu-id="8606a-154">90 Tage</span><span class="sxs-lookup"><span data-stu-id="8606a-154">90 days</span></span>  <br/> |<span data-ttu-id="8606a-155">Wenn Sie eine Nachrichtenverfolgung für Nachrichten starten, die weniger als 7 Tage alt sind, sollten die Nachrichten innerhalb von 5-30 Minuten erscheinen.</span><span class="sxs-lookup"><span data-stu-id="8606a-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="8606a-156">Wenn Sie eine Ablaufverfolgung für Nachrichten ausführen, die älter als 7 Tage sind, kann es einige Stunden dauern, bis Ergebnisse ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8606a-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8606a-157">Datenverfügbarkeit und Latenz sind identisch, unabhängig davon, ob Sie über das Microsoft 365 Admin Center oder die Remote-PowerShell angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8606a-157">Data availability and latency is the same whether requested via the Microsoft 365 admin center or remote PowerShell.</span></span> 
  


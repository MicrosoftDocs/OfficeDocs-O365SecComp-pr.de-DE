---
title: Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection: M365-security-compliance
description: Erfahren Sie, wie Sie e-Mail-Sicherheitsberichte für Ihre Organisation mit Office 365 Enterprise suchen und verwenden. E-Mail-Sicherheitsberichte sind im &amp; Security Compliance Center verfügbar.
ms.openlocfilehash: 809bfbdfdda8bd1ed9b88c9bca7e9ce14d774868
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216415"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="33776-104">Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="33776-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="33776-p102">Im [ &amp; Security Compliance Center](https://security.microsoft.com) stehen eine Reihe von e-Mail-Sicherheitsberichten zur Verfügung, die Ihnen helfen, zu sehen, wie Antispam-und Antischadsoftware-Features in Office 365 Ihre Organisation schützen. Wenn Sie über die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie diese Berichte &amp; im Security Compliance Center anzeigen, indem Sie zum **Dashboard**für **Berichte** \> wechseln.</span><span class="sxs-lookup"><span data-stu-id="33776-p102">A variety of email security reports are available in the [Security &amp; Compliance Center](https://security.microsoft.com) to help you see how anti-spam and anti-malware features in Office 365 are protecting your organization. If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![Mit dem &amp; Security Compliance Center-Dashboard können Sie erkennen, wo Advanced Threat Protection funktioniert.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="33776-108">Zu Ihren e-Mail-Sicherheitsberichten gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="33776-108">Your email security reports include the following:</span></span>
  
- [<span data-ttu-id="33776-109">Status Bericht zum BedrohungsSchutz</span><span class="sxs-lookup"><span data-stu-id="33776-109">Threat Protection Status report</span></span>](view-email-security-reports.md#tps) 
    
- [<span data-ttu-id="33776-110">Bericht über Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="33776-110">Malware Detections report</span></span>](view-email-security-reports.md#maldet)
    
- [<span data-ttu-id="33776-111">Häufigster Schadsoftware-Bericht</span><span class="sxs-lookup"><span data-stu-id="33776-111">Top Malware report</span></span>](#top-malware-report)
    
- [<span data-ttu-id="33776-112">Bericht "häufigste Absender und Empfänger"</span><span class="sxs-lookup"><span data-stu-id="33776-112">Top Senders and Recipients report</span></span>](view-email-security-reports.md#topsenders)
    
- [<span data-ttu-id="33776-113">Spoof-e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="33776-113">Spoof Mail report</span></span>](#spoof-mail-report)
    
- [<span data-ttu-id="33776-114">Bericht über Spam-Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="33776-114">Spam Detections report</span></span>](#spam-detections-report)
    
- [<span data-ttu-id="33776-115">Gesendete und empfangene e-Mail-Berichte</span><span class="sxs-lookup"><span data-stu-id="33776-115">Sent and received email report</span></span>](view-email-security-reports.md#sentreceivedemail)
    
- <span data-ttu-id="33776-116">[Bericht über vom Benutzer gemeldete Nachrichten](view-email-security-reports.md#userreported) (neu!)</span><span class="sxs-lookup"><span data-stu-id="33776-116">[User-reported messages report](view-email-security-reports.md#userreported) (new!)</span></span> 
    
## <a name="threat-protection-status-report"></a><span data-ttu-id="33776-117">Status Bericht zum BedrohungsSchutz</span><span class="sxs-lookup"><span data-stu-id="33776-117">Threat Protection Status report</span></span>

<span data-ttu-id="33776-p103">Der neue **Status Bericht Threat Protection** ist ein intelligenter Bericht, der schädliche e-Mails zeigt, die von Exchange Online Protection erkannt und blockiert wurden. Dieser Bericht enthält Informationen zu e-Mails, die als Schadsoftware oder als Phishing-Versuch identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-p103">The new **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection. This report shows information about email identified as malware or a phishing attempt.</span></span> 

> [!NOTE]
> <span data-ttu-id="33776-p104">Ein Bericht über den BedrohungsSchutz steht Kunden zur Verfügung, die entweder [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) haben; die Informationen, die im Status Bericht zur Gefahrenabwehr für ATP-Kunden angezeigt werden, enthalten jedoch wahrscheinlich unterschiedliche Daten als die EOP-Kunden. EOP-Kunden können beispielsweise Informationen über in e-Mails erkannte Schadsoftware anzeigen, jedoch keine Informationen zu böswilligen Dateien, die [in SharePoint Online, OneDrive oder Microsoft Teams erkannt](atp-for-spo-odb-and-teams.md)wurden, eine ATP-spezifische Funktion. ([Erfahren Sie mehr über ATP-Berichte](view-reports-for-atp.md).)</span><span class="sxs-lookup"><span data-stu-id="33776-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md), an ATP-specific capability. ([Learn more about ATP reports](view-reports-for-atp.md).)</span></span>
  
<span data-ttu-id="33776-123">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zum Status des \> **Threat Protection**-Dashboards für **Berichte** \> \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="33776-123">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Status Bericht zum BedrohungsSchutz](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="33776-p105">Wenn Sie den Status Bericht zum ersten Mal öffnen, zeigt der Bericht standardmäßig Daten für die letzten sieben Tage an; Sie können jedoch auf **Filter** klicken und den Datums Umfang für bis zu 90 Tage ändern. Dieser Bericht ist nützlich, um die Effektivität und die Auswirkungen der Exchange Online Protection-Features in Ihrer Organisation sowie für längerfristige Trends anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="33776-p105">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail. This report is useful for viewing the effectiveness and impact of your organization's Exchange Online Protection features, and for longer-term trending.</span></span> 
  
![Status Berichtsfilter für den BedrohungsSchutz](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="33776-128">Sie können auch auswählen, ob Daten für als böswillig identifizierte e-Mails, als Phishing-Versuche identifizierte e-Mails oder als Schadsoftware identifizierte e-Mails angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="33776-128">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![Status Berichts Ansichtsoptionen für den BedrohungsSchutz](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="33776-130">Bericht über Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="33776-130">Malware Detections report</span></span>

<span data-ttu-id="33776-131">Der \*\*\*\* Bericht über Schadsoftware zeigt, wie viele eingehende und ausgehende Nachrichten erkannt wurden, die Schadsoftware für Ihre Organisation enthalten.</span><span class="sxs-lookup"><span data-stu-id="33776-131">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="33776-132">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu " **Berichte** \> - **Dashboard** \> -Schadsoftware- **Entdeckungen**".</span><span class="sxs-lookup"><span data-stu-id="33776-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![Beispiel für Schadsoftware-Erkennungsberichte](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="33776-p106">Ähnlich wie bei anderen Berichten zeigt der Bericht standardmäßig Daten für die letzten sieben Tage an. Sie können jedoch auch **Filter** auswählen, um den Datums Umfang zu ändern.</span><span class="sxs-lookup"><span data-stu-id="33776-p106">Similar to other reports, like the Threat Protection Status report, the report displays data for the past seven days by default. However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="33776-136">Häufigster Schadsoftware-Bericht</span><span class="sxs-lookup"><span data-stu-id="33776-136">Top Malware report</span></span>

<span data-ttu-id="33776-137">Der **häufigste Malware** Bericht zeigt die verschiedenen Arten von Schadsoftware, die von Exchange Online erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-137">The **Top Malware** report shows the various kinds of malware that was detected by Exchange Online.</span></span> 
  
<span data-ttu-id="33776-138">Um \*\*\*\* \> diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu den **Top**-Schadsoftware- **Dashboards** \> .</span><span class="sxs-lookup"><span data-stu-id="33776-138">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![SCC-EOP – häufigste Schadsoftware](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="33776-140">Wenn Sie im Kreisdiagramm auf einen Keil zeigen, sehen Sie den Namen einer Art von Schadsoftware und die Anzahl der Nachrichten, die als Schadsoftware erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-140">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="33776-141">Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.</span><span class="sxs-lookup"><span data-stu-id="33776-141">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Dieser Bericht zeigt die häufigste Schadsoftware, die für Ihre Organisation erkannt wurde.](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="33776-143">Unterhalb des Diagramms wird eine Liste der erkannten Schadsoftware und der Anzahl der Nachrichten angezeigt, die als Schadsoftware erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-143">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="33776-144">Bericht "häufigste Absender und Empfänger"</span><span class="sxs-lookup"><span data-stu-id="33776-144">Top Senders and Recipients report</span></span>

<span data-ttu-id="33776-145">Der Bericht " **häufigste Absender und Empfänger** " ist ein Kreisdiagramm, in dem die wichtigsten e-Mail-Absender angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33776-145">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="33776-146">\*\*\*\* \> Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu den Top-Absendern **und Empfängern**des Dashboards. \*\*\*\* \></span><span class="sxs-lookup"><span data-stu-id="33776-146">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zu den Top \> - \> Absendern und Empfängern des Berichte-Dashboards.](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="33776-148">Wenn Sie den Mauszeiger über einen Keil im Kreisdiagramm bewegen, wird die Anzahl der gesendeten oder empfangenen Nachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33776-148">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="33776-149">Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.</span><span class="sxs-lookup"><span data-stu-id="33776-149">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="33776-p107">Verwenden Sie die Liste **Daten für anzeigen** , um auszuwählen, ob Daten für die wichtigsten Absender, Empfänger, Spamempfänger und Schadsoftware-Empfänger angezeigt werden sollen. Sie können auch sehen, wer Malware erhalten hat, die von Advanced Threat Protection erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="33776-p107">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients. You can also see who received malware that was detected by Advanced Threat Protection.</span></span> 
  
![Verwenden der Liste "Daten für anzeigen" zum Anzeigen bestimmter Informationen](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="33776-153">Unter dem Diagramm sehen Sie, wer die häufigsten e-Mail-Absender oder Empfänger waren, zusammen mit der Anzahl der Nachrichten, die für den angegebenen Zeitraum gesendet oder empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-153">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-mail-report"></a><span data-ttu-id="33776-154">Spoof-e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="33776-154">Spoof Mail report</span></span>

<span data-ttu-id="33776-155">Der **Spoof-e-Mail-** Bericht zeigt, wie viele Spoof-e-Mail-Nachrichten erkannt wurden, und von denen, die als "gut" galten (Spoof-e-Mails aus berechtigten geschäftlichen Gründen).</span><span class="sxs-lookup"><span data-stu-id="33776-155">The **Spoof Mail** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="33776-156">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> - **Dashboard** \> **-Spoof-e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="33776-156">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zu Berichte \> -Dashboard \> -Spoof-e-Mail](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="33776-158">Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, sehen Sie, wie viele Spoof-e-Mail-Nachrichten durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="33776-158">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="33776-159">Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.</span><span class="sxs-lookup"><span data-stu-id="33776-159">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="33776-160">Bericht über Spam-Entdeckungen</span><span class="sxs-lookup"><span data-stu-id="33776-160">Spam Detections report</span></span>

<span data-ttu-id="33776-161">Der Bericht über **Spam Entdeckungen** enthält alle Spam-Inhalte, die von Exchange Online blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-161">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> 
  
<span data-ttu-id="33776-162">Um \*\*\*\* \> diesen Bericht anzuzeigen, gehen Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Spam Entdeckungen**im **Dashboard** \> .</span><span class="sxs-lookup"><span data-stu-id="33776-162">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zu den Berichten \> Dashboard \> EoP Spam Detections](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="33776-p108">Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Elemente an diesem Tag blockiert wurden, und wie diese Elemente kategorisiert werden. Sie können beispielsweise sehen, wie viele Spamnachrichten gefiltert wurden und wie viele Elemente aus einer blockierten IP-Adresse (Internet Protocol) stammten.</span><span class="sxs-lookup"><span data-stu-id="33776-p108">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized. For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="33776-166">Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.</span><span class="sxs-lookup"><span data-stu-id="33776-166">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Der Bericht über Spam Entdeckungen gibt an, wie viele Spamnachrichten blockiert oder herausgefiltert wurden.](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="33776-p109">Unterhalb des Diagramms wird eine Liste der gefundenen Spam Elemente angezeigt. Wählen Sie ein Element aus, um zusätzliche Informationen anzuzeigen, beispielsweise ob es sich bei dem Spam Element um ein-oder ausgehend, um die Nachrichten-ID und den Empfänger handelt.</span><span class="sxs-lookup"><span data-stu-id="33776-p109">Below the chart, you'll see a list of spam items that were detected. Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="33776-170">Gesendete und empfangene e-Mail-Berichte</span><span class="sxs-lookup"><span data-stu-id="33776-170">Sent and received email report</span></span>

<span data-ttu-id="33776-171">Der **gesendete und empfangene e-Mail-** Bericht ist ein intelligenter Bericht mit Informationen zu eingehenden und ausgehenden e-Mails, einschließlich Spamerkennungen, Schadsoftware und e-Mails, die als "gut" identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-171">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="33776-172">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zum **Berichte** \> - **Dashboard** \> **gesendet und empfangen per e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="33776-172">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zum Berichte \> -Dashboard \> gesendet und empfangen per e-Mail.](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="33776-p110">Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Nachrichten eingehen und wie diese Nachrichten kategorisiert werden. Sie können beispielsweise sehen, wie viele Nachrichten mit Schadsoftware erkannt wurden und wie viele als Spam identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-p110">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized. For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="33776-176">Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.</span><span class="sxs-lookup"><span data-stu-id="33776-176">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="33776-177">Mithilfe der Liste nach **unten** nach können Sie Informationen nach Typ oder nach Richtung (ein-und ausgehend) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="33776-177">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![Verwenden der aufSchlüsselung nach Liste zum Anzeigen von Informationen nach Typ oder Richtung](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="33776-p111">Unterhalb des Diagramms sehen Sie eine Liste der e-Mail-Kategorien, wie **GoodMail**, **SpamContentFiltered**usw. Wählen Sie eine Kategorie aus, um zusätzliche Informationen anzuzeigen, beispielsweise Aktionen, die für Schadsoftware ergriffen wurden, und ob e-Mails ein-oder ausgehen.</span><span class="sxs-lookup"><span data-stu-id="33776-p111">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on. Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![Dieser Bericht informiert Sie über Antischadsoftware, Antispam und andere Nachrichten Entdeckungen.](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a><span data-ttu-id="33776-182">Bericht über vom Benutzer gemeldete Nachrichten (neu!)</span><span class="sxs-lookup"><span data-stu-id="33776-182">User-reported messages report (new!)</span></span>

<span data-ttu-id="33776-183">Der Bericht vom **Benutzer gemeldete Nachrichten** enthält Informationen zu e-Mail-Nachrichten, die von Benutzern als Junk-, Phishing-oder gute e-Mails mithilfe des [Add-Ins "Berichtnachricht](enable-the-report-message-add-in.md)" gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="33776-183">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md).</span></span>
  
<span data-ttu-id="33776-p112">Für jede Nachricht stehen Details zur Verfügung, einschließlich des Liefer Grunds, einer Spam Richtlinienausnahme oder einer Nachrichtenfluss Regel, die für Ihre Organisation konfiguriert ist. Zum Anzeigen von Details wählen Sie ein Element in der Liste Benutzer Berichte aus, und zeigen Sie die Informationen auf den Registerkarten **Zusammenfassung** und **Details** an.</span><span class="sxs-lookup"><span data-stu-id="33776-p112">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization. To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![Der Bericht vom Benutzer gemeldete Nachrichten zeigt Benutzer, die als Junk-, nicht Junk-oder Phishing-Versuche gekennzeichnet sind.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="33776-187">Führen Sie im [ &amp; Security Compliance Center](https://protection.office.com)einen der folgenden Schritte aus, um diesen Bericht anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="33776-187">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), do one of the following:</span></span>
  
- <span data-ttu-id="33776-188">Wechseln Sie zu vom **Benutzer gemeldeten Nachrichten**des **Threat Management** \> - **Dashboards** \> .</span><span class="sxs-lookup"><span data-stu-id="33776-188">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="33776-189">Gehen Sie zu **Threat Management** \> **Review** \> vom **Benutzer gemeldete Nachrichten**.</span><span class="sxs-lookup"><span data-stu-id="33776-189">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![Wählen Sie im &amp; Security Compliance Center die Option \> Bedrohungs \> Verwaltung Überprüfung der gemeldeten Nachrichten aus.](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="33776-p113">Damit der Bericht vom Benutzer gemeldete Nachrichten ordnungsgemäß funktioniert, **muss die Überwachungsprotokollierung** für ihre Office 365-Umgebung aktiviert sein. Dies erfolgt in der Regel durch einen Benutzer, dem die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen wurde. Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="33776-p113">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="33776-194">Welche Berechtigungen sind erforderlich, um diese Berichte anzuzeigen?</span><span class="sxs-lookup"><span data-stu-id="33776-194">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="33776-195">Um die in diesem Artikel beschriebenen Berichte anzuzeigen und zu verwenden, **müssen Sie eine entsprechende Rolle sowohl für das Security &amp; Compliance Center als auch für das Exchange Admin Center zugewiesen haben**.</span><span class="sxs-lookup"><span data-stu-id="33776-195">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="33776-196">Für das Security &amp; Compliance Center muss eine der folgenden Rollen zugewiesen sein:</span><span class="sxs-lookup"><span data-stu-id="33776-196">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="33776-197">Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="33776-197">Organization Management</span></span>
    - <span data-ttu-id="33776-198">Sicherheits Administrator (Dies kann im Azure Active Directory Admin Center zugewiesen werden ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="33776-198">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>
    - <span data-ttu-id="33776-199">Sicherheits Leser</span><span class="sxs-lookup"><span data-stu-id="33776-199">Security Reader</span></span>

- <span data-ttu-id="33776-200">Für Exchange Online müssen Sie über eine der folgenden Rollen verfügen, die entweder in der Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() oder mit PowerShell-Cmdlets zugewiesen sind (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="33776-200">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="33776-201">Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="33776-201">Organization Management</span></span>
    - <span data-ttu-id="33776-202">Organisationsverwaltung mit Leserechten</span><span class="sxs-lookup"><span data-stu-id="33776-202">View-only Organization Management</span></span>
    - <span data-ttu-id="33776-203">Rolle „Empfänger mit Leserechten“</span><span class="sxs-lookup"><span data-stu-id="33776-203">View-Only Recipients role</span></span>
    - <span data-ttu-id="33776-204">Verwaltung der Richtlinientreue</span><span class="sxs-lookup"><span data-stu-id="33776-204">Compliance Management</span></span>

<span data-ttu-id="33776-205">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="33776-205">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="33776-206">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="33776-206">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="33776-207">Featureberechtigungen in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="33776-207">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="33776-208">Was geschieht, wenn die Berichte keine Daten anzeigen?</span><span class="sxs-lookup"><span data-stu-id="33776-208">What if the reports aren't showing data?</span></span>

<span data-ttu-id="33776-p114">Wenn in ihren Berichten keine Daten angezeigt werden, überprüfen Sie, ob Ihre Richtlinien ordnungsgemäß eingerichtet sind. Weitere Informationen finden Sie unter [Antispam-und Antischadsoftware-Schutz in Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="33776-p114">If you are not seeing data in your reports, double-check that your policies are set up correctly. To learn more, see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="33776-211">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="33776-211">Related topics</span></span>

[<span data-ttu-id="33776-212">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="33776-212">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="33776-213">Berichte und Einblicke im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="33776-213">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="33776-214">Erstellen eines Zeitplans für einen Bericht im &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="33776-214">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="33776-215">Einrichten und Herunterladen eines benutzerdefinierten Berichts im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="33776-215">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  


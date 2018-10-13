---
title: Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
description: Informationen Sie zum Suchen und Verwenden von e-Mail-Sicherheitsberichte für Ihre Organisation mit Office 365 Enterprise. E-Mail-Sicherheitsberichte stehen in der Sicherheit &amp; Compliance Center.
ms.openlocfilehash: ea5d60393809ef924d51435b695062fe51e772bd
ms.sourcegitcommit: e0c6f99d5514d8da8a70d9bd3616d1a1c0851254
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2018
ms.locfileid: "25552393"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="23908-104">Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="23908-p102">Eine Vielzahl von e-Mail-Sicherheit meldet stehen in der Sicherheit &amp; Compliance Center, mit denen Sie die finden Sie unter wie Antispam- und Antischadsoftware-Features in Office 365 Ihrer Organisation geschützt sind. Wenn Sie die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie diese Berichte anzeigen, in das Wertpapier &amp; Compliance Center auf **Berichte** zugreifen, indem \> **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="23908-p102">A variety of email security reports are available in the Security &amp; Compliance Center to help you see how anti-spam and anti-malware features in Office 365 are protecting your organization. If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="23908-108">Ihre e-Mail-Sicherheitsberichte umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="23908-108">Your email security reports include the following:</span></span>
  
- <span data-ttu-id="23908-109">[Threat Protection Statusbericht](view-email-security-reports.md#tps) (neu!)</span><span class="sxs-lookup"><span data-stu-id="23908-109">[Threat Protection Status report](view-email-security-reports.md#tps) (new!)</span></span> 
    
- [<span data-ttu-id="23908-110">Erkannte Schadsoftware Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-110">Malware Detections report</span></span>](view-email-security-reports.md#maldet)
    
- [<span data-ttu-id="23908-111">Top-Schadsoftware-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-111">Top Malware report</span></span>](#top-malware-report)
    
- [<span data-ttu-id="23908-112">Obere Absendern und Empfängern Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-112">Top Senders and Recipients report</span></span>](view-email-security-reports.md#topsenders)
    
- [<span data-ttu-id="23908-113">Spoofing der e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-113">Spoof Mail report</span></span>](#spoof-mail-report)
    
- [<span data-ttu-id="23908-114">Bericht Spamerkennungen</span><span class="sxs-lookup"><span data-stu-id="23908-114">Spam Detections report</span></span>](#spam-detections-report)
    
- [<span data-ttu-id="23908-115">Gesendete und empfangene e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-115">Sent and received email report</span></span>](view-email-security-reports.md#sentreceivedemail)
    
- <span data-ttu-id="23908-116">[Benutzer gemeldete Nachrichten Bericht](view-email-security-reports.md#userreported) (neu!)</span><span class="sxs-lookup"><span data-stu-id="23908-116">[User-reported messages report](view-email-security-reports.md#userreported) (new!)</span></span> 
    
## <a name="threat-protection-status-report-new"></a><span data-ttu-id="23908-117">Verfahren Sie zum Erstellen von Schutz Statusbericht (neu!)</span><span class="sxs-lookup"><span data-stu-id="23908-117">Threat Protection Status report (new!)</span></span>

<span data-ttu-id="23908-p103">Der neue **Threat Protection** Statusbericht ist smart Bericht mit böswilligen Absichten e-Mail, die erkannt und von Exchange Online Protection blockiert wurde. In diesem Bericht werden Informationen zu e-Mails, die als Malware oder Phishing-Versuch identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23908-p103">The new **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection. This report shows information about email identified as malware or a phishing attempt.</span></span> 

> [!NOTE]
> <span data-ttu-id="23908-p104">Ein Bericht Bedrohung Schutzstatus steht Kunden mit [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Allerdings werden die Informationen, die im Bericht Schutzstatus Bedrohung für ATP-Kunden angezeigt wird wahrscheinlich andere Daten als was EOP-Kunden finden Sie unter möglicherweise enthalten. EOP-Kunden können beispielsweise Schadsoftware erkannt in e-Mails, die aber nicht Informationen zu [schädliche Dateien in SharePoint Online, OneDrive, oder Microsoft-Teams erkannt](atp-for-spo-odb-and-teams.md), eine Funktion ATP-spezifische Informationen anzeigen. ([Erfahren Sie mehr über Berichte ATP](view-reports-for-atp.md)).</span><span class="sxs-lookup"><span data-stu-id="23908-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md), an ATP-specific capability. ([Learn more about ATP reports](view-reports-for-atp.md).)</span></span>
  
<span data-ttu-id="23908-123">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Bedrohung Schutzstatus**.</span><span class="sxs-lookup"><span data-stu-id="23908-123">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Threat Protection Statusbericht](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="23908-p105">Wenn Sie den Threat Protection Statusbericht zum ersten Mal öffnen, zeigt der Bericht Daten für die letzten sieben Tage standardmäßig; Sie können jedoch auf **Filter** und den Datumsbereich für bis zu 90 Tage Detailebene ändern. In diesem Bericht eignet sich für die Anzeige der Effizienz und der Auswirkung von Ihrer Organisation Exchange Online Protection Features und für längerfristige Trend.</span><span class="sxs-lookup"><span data-stu-id="23908-p105">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail. This report is useful for viewing the effectiveness and impact of your organization's Exchange Online Protection features, and for longer-term trending.</span></span> 
  
![Bedrohung Schutzstatus Berichtsfilter](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="23908-128">Sie können auch auswählen, ob zum Anzeigen von Daten für e-Mails, die als böswillige e-Mail identifiziert, wie ein Phishing versucht, oder e-Mail identifiziert Schadsoftware enthält.</span><span class="sxs-lookup"><span data-stu-id="23908-128">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![Bedrohung Schutzstatus Bericht anzeigen von Optionen](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="23908-130">Erkannte Schadsoftware Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-130">Malware Detections report</span></span>

<span data-ttu-id="23908-131">Der **Erkannte Schadsoftware** Bericht zeigt, wie viele ein- und ausgehende Nachrichten als mit Malware für Ihre Organisation erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="23908-131">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="23908-132">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Erkannte Schadsoftware**.</span><span class="sxs-lookup"><span data-stu-id="23908-132">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![Beispiel für Schadsoftware erkannte Bericht](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="23908-p106">Andere Berichte, wie ein Bericht Bedrohung Schutzstatus ähnelt der Bericht Daten für die letzten sieben Tage standardmäßig angezeigt. Sie können jedoch **Filter** , um den Datumsbereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="23908-p106">Similar to other reports, like the Threat Protection Status report, the report displays data for the past seven days by default. However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="23908-136">Top-Schadsoftware-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-136">Top Malware report</span></span>

<span data-ttu-id="23908-137">Der **Oben Malware** Bericht werden die verschiedenen Arten von Schadsoftware, die von Exchange Online gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="23908-137">The **Top Malware** report shows the various kinds of malware that was detected by Exchange Online.</span></span> 
  
<span data-ttu-id="23908-138">Zum Anzeigen dieses Berichts, in das Wertpapier &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Oben Malware**.</span><span class="sxs-lookup"><span data-stu-id="23908-138">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![SCC - EOP wichtigste Schadsoftware](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="23908-140">Wenn Sie über eine Keil im Kreisdiagramm bewegen, sehen Sie den Namen von der Art der Malware und wie viele Nachrichten mit, dass Malware erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="23908-140">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="23908-141">Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="23908-141">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![In diesem Bericht werden die wichtigste Schadsoftware erkannt für Ihre Organisation](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="23908-143">Unter dem Diagramm sehen Sie eine Liste der erkannten Malware und wie viele Nachrichten mit, dass Malware erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="23908-143">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="23908-144">Obere Absendern und Empfängern Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-144">Top Senders and Recipients report</span></span>

<span data-ttu-id="23908-145">Der **häufigste Absender und Empfänger** Bericht ist ein Kreisdiagramm Ihre oberen e-Mail-Absender angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23908-145">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="23908-146">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **häufigste Absender und Empfänger**.</span><span class="sxs-lookup"><span data-stu-id="23908-146">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> häufigste Absender und Empfänger](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="23908-148">Wenn Sie über eine Keil im Kreisdiagramm bewegen, sehen Sie die Anzahl der Nachrichten gesendet oder empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23908-148">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="23908-149">Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="23908-149">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="23908-p107">Verwenden Sie die Liste **Anzeigen von Daten für** , ob Sie Daten für häufigste Absender, Empfänger, Spamempfänger und schadsoftwareempfänger anzeigen möchten. Sie können auch sehen, wer Malware erhalten, die von der erweiterte Schutz erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="23908-p107">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients. You can also see who received malware that was detected by Advanced Threat Protection.</span></span> 
  
![Mithilfe der Liste Anzeigen von Daten für spezifische Informationen anzuzeigen](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="23908-153">Unterhalb des Diagramms angezeigt, die die oberen e-Mail-Absender oder Empfänger wurden, zusammen mit der Anzahl der Nachrichten gesendet oder empfangen wurden, für den angegebenen Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="23908-153">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-mail-report"></a><span data-ttu-id="23908-154">Spoofing der e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-154">Spoof Mail report</span></span>

<span data-ttu-id="23908-155">Der **Spoofing Mail** Bericht zeigt, wie viele e-Mail-Nachrichten von Spoofing erkannt wurden, wurden, welche "gut" (Spoofing Mail legitimen geschäftlichen Gründen geschehen) betrachtet und.</span><span class="sxs-lookup"><span data-stu-id="23908-155">The **Spoof Mail** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="23908-156">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Spoofing Mail**.</span><span class="sxs-lookup"><span data-stu-id="23908-156">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> Spoofing Mail](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="23908-158">Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Spoofing e-Mail-Nachrichten über stammt.</span><span class="sxs-lookup"><span data-stu-id="23908-158">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="23908-159">Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="23908-159">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="23908-160">Bericht Spamerkennungen</span><span class="sxs-lookup"><span data-stu-id="23908-160">Spam Detections report</span></span>

<span data-ttu-id="23908-161">Der Bericht **Spamerkennungen** zeigt alle Spam-Inhalt von Exchange Online blockiert.</span><span class="sxs-lookup"><span data-stu-id="23908-161">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> 
  
<span data-ttu-id="23908-162">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **Spamerkennungen**.</span><span class="sxs-lookup"><span data-stu-id="23908-162">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> EOP Spamerkennungen](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="23908-p108">Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Elemente dieses Tages blockiert wurden, wie diese Elemente kategorisiert werden. Beispielsweise können Sie sehen, wie viele Spamnachrichten gefiltert wurden, und wie viele Elemente eine blockierte IP (Internet Protocol) Adresse stammt.</span><span class="sxs-lookup"><span data-stu-id="23908-p108">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized. For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="23908-166">Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="23908-166">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Der Bericht Spamerkennungen erfahren Sie, wie viele Spamnachrichten herausgefiltert oder blockiert wurden](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="23908-p109">Unter dem Diagramm sehen Sie eine Liste der Spam-Objekte, die erkannt wurden. Wählen Sie ein Element aus, um zusätzliche Informationen wie gibt an, ob das Element Spam eingehend oder ausgehend war, die Nachrichten-ID und der Empfänger anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="23908-p109">Below the chart, you'll see a list of spam items that were detected. Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="23908-170">Gesendete und empfangene e-Mail-Bericht</span><span class="sxs-lookup"><span data-stu-id="23908-170">Sent and received email report</span></span>

<span data-ttu-id="23908-171">Der Bericht **gesendete und empfangene e-Mail** ist smart Bericht mit Informationen zu eingehender und ausgehender e-Mails, einschließlich spamerkennungen, Malware und e-Mails, die als "gut".</span><span class="sxs-lookup"><span data-stu-id="23908-171">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="23908-172">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur **Berichte** \> **Dashboard** \> **gesendete und empfangene e-Mail**.</span><span class="sxs-lookup"><span data-stu-id="23908-172">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> gesendete und empfangene e-Mail](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="23908-p110">Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Nachrichten geliefert wurde und wie diese Nachrichten kategorisiert werden. Beispielsweise können Sie sehen, wie viele Nachrichten als mit Schadsoftware erkannt wurden, und wie viele als Spam identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="23908-p110">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized. For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="23908-176">Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="23908-176">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="23908-177">Die Liste **nach aufgliedern** können zum Anzeigen von Informationen nach Typ oder nach Richtung (eingehend und ausgehend).</span><span class="sxs-lookup"><span data-stu-id="23908-177">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![Verwenden Sie die Liste unterbrechen nach unten durch, zum Anzeigen von Informationen vom Typ oder die Richtung](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="23908-p111">Unter dem Diagramm sehen Sie eine Liste von e-Mail-Kategorien, wie **GoodMail**, **SpamContentFiltered**und So weiter. Wählen Sie eine Kategorie anzeigen zusätzlicher Informationen, wie beispielsweise für Schadsoftware, durchgeführten Aktionen und gibt an, ob e-Mail-wurde eingehend oder ausgehend.</span><span class="sxs-lookup"><span data-stu-id="23908-p111">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on. Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![In diesem Bericht erfahren Sie mehr über Schadsoftware, Anti-Spam- und andere erkannte Nachricht](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a><span data-ttu-id="23908-182">Benutzer gemeldete Nachrichten Bericht (neu!)</span><span class="sxs-lookup"><span data-stu-id="23908-182">User-reported messages report (new!)</span></span>

<span data-ttu-id="23908-183">Der **Benutzer gemeldete Nachrichten** -Bericht enthält Informationen zu e-Mail-Nachrichten, die Benutzer mit dem [Bericht-add-in](enable-the-report-message-add-in.md)als Junk, Phishing-Versuche oder unbedenkliche e-Mails gemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="23908-183">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md).</span></span>
  
<span data-ttu-id="23908-p112">Details sind für jede Nachricht, einschließlich der Übermittlung Grund, einen solchen Spam-Richtlinie Ausnahme oder e-Mail-Flussregel für Ihre Organisation konfiguriert. Um Details anzuzeigen, wählen Sie ein Element in der Liste Benutzer-Berichte, und klicken Sie dann zeigen Sie die Informationen auf den Registerkarten **Zusammenfassung** und **Details an** .</span><span class="sxs-lookup"><span data-stu-id="23908-p112">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization. To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![Bericht User-Reported Nachrichten werden Nachrichten, die Benutzer mit der Bezeichnung als Junk, keine Junk-e- oder Phishing Versuche.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="23908-187">So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="23908-187">To view this report, in the Security &amp; Compliance Center, do one of the following:</span></span>
  
- <span data-ttu-id="23908-188">Wechseln Sie zu **Threat Management** \> **Dashboard** \> **Nachrichten Benutzer gemeldet**.</span><span class="sxs-lookup"><span data-stu-id="23908-188">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="23908-189">Wechseln Sie zu **Threat Management** \> **Überprüfung** \> **Nachrichten Benutzer gemeldet**.</span><span class="sxs-lookup"><span data-stu-id="23908-189">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![In das Wertpapier &amp; Compliance Center, wählen Sie Threat Management \> Überprüfung \> Benutzer gemeldete Nachrichten](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="23908-p113">In Reihenfolge für den Benutzer gemeldete Nachrichten Bericht ordnungsgemäß funktioniert für Ihre Office 365-Umgebung **muss die überwachungsprotokollierung aktiviert werden** . Dies erfolgt normalerweise von einem Benutzer, der Rolle für Überwachungsprotokolle im Exchange Online zugewiesen hat. Weitere Informationen finden Sie unter [Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="23908-p113">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="23908-194">Welche Berechtigungen sind erforderlich, damit diese Berichte anzeigen?</span><span class="sxs-lookup"><span data-stu-id="23908-194">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="23908-195">Um anzuzeigen, und die e-Mail-Sicherheitsberichte in diesem Artikel beschriebenen verwenden, benötigen Sie eine entsprechende Rolle zugewiesen sind, in das Wertpapier &amp; Compliance Center und in der Exchange-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="23908-195">In order to view and use the email security reports described in this article, you must have an appropriate role assigned in the Security &amp; Compliance Center and in the Exchange Admin Center.</span></span>
  
|<span data-ttu-id="23908-196">**Rollengruppe**</span><span class="sxs-lookup"><span data-stu-id="23908-196">**Role group**</span></span>|<span data-ttu-id="23908-197">**Wobei zugewiesen**</span><span class="sxs-lookup"><span data-stu-id="23908-197">**Where assigned**</span></span>|<span data-ttu-id="23908-198">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="23908-198">**Learn more**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="23908-199">Eine der folgenden Varianten:</span><span class="sxs-lookup"><span data-stu-id="23908-199">One of the following:</span></span>  <br/><br/><span data-ttu-id="23908-200">--Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="23908-200">--Organization Management</span></span>  <br/><span data-ttu-id="23908-201">--Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="23908-201">--Security Administrator</span></span>  <br/><span data-ttu-id="23908-202">– Leser Sicherheit</span><span class="sxs-lookup"><span data-stu-id="23908-202">--Security Reader</span></span>  <br/> |<span data-ttu-id="23908-203">Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-203">Security &amp; Compliance Center</span></span>  <br/> |[<span data-ttu-id="23908-204">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-204">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md) <br/> |
| <span data-ttu-id="23908-205">Eine der folgenden Varianten:</span><span class="sxs-lookup"><span data-stu-id="23908-205">One of the following:</span></span>  <br/><br/><span data-ttu-id="23908-206">--Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="23908-206">--Organization Management</span></span>  <br/><span data-ttu-id="23908-207">– Organisationsverwaltung nur Ansicht</span><span class="sxs-lookup"><span data-stu-id="23908-207">--View-only Organization Management</span></span>  <br/><span data-ttu-id="23908-208">--Kontaktobjekts Empfänger-Rolle</span><span class="sxs-lookup"><span data-stu-id="23908-208">--View-Only Recipients role</span></span>  <br/><span data-ttu-id="23908-209">--Verwaltung der Richtlinientreue</span><span class="sxs-lookup"><span data-stu-id="23908-209">--Compliance Management</span></span>  <br/> |<span data-ttu-id="23908-210">Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="23908-210">Exchange Admin Center</span></span>  <br/> |[<span data-ttu-id="23908-211">Featureberechtigungen in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="23908-211">Feature permissions in Exchange Online</span></span>](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="23908-212">Was passiert, wenn nicht die Berichte Daten angezeigt?</span><span class="sxs-lookup"><span data-stu-id="23908-212">What if the reports aren't showing data?</span></span>

<span data-ttu-id="23908-p114">Wenn Sie Daten in den Berichten nicht angezeigt werden, überprüfen Sie, dass Ihre Richtlinien ordnungsgemäß eingerichtet wurden. Weitere Informationen finden Sie unter [Anti-Spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="23908-p114">If you are not seeing data in your reports, double-check that your policies are set up correctly. To learn more, see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="23908-215">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="23908-215">Related topics</span></span>

[<span data-ttu-id="23908-216">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="23908-216">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="23908-217">Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-217">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="23908-218">Erstellen Sie einen Zeitplan für einen Bericht in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-218">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="23908-219">Einrichten von, und Laden Sie einen benutzerdefinierten Bericht in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="23908-219">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  


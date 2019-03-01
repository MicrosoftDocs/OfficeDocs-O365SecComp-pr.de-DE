---
title: Nachrichtenablaufverfolgung im Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Administratoren können die Nachrichtenablaufverfolgung im Security & Compliance Center verwenden, um herauszufinden, was mit Nachrichten passiert ist.
ms.openlocfilehash: 95682b02f50996594650ac5d3aebf18f795efd65
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341566"
---
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="c5214-103">Nachrichtenablaufverfolgung im Security & Compliance Center</span><span class="sxs-lookup"><span data-stu-id="c5214-103">Message trace in the Security & Compliance Center</span></span>

<span data-ttu-id="c5214-p101">Die Nachrichtenablaufverfolgung im Security & Compliance Center befolgt e-Mail-Nachrichten, während Sie über Ihre Exchange Online-Organisation Reisen. Sie können ermitteln, ob eine Nachricht empfangen, abgelehnt, zurückgestellt oder vom Dienst übermittelt wurde. Außerdem wird gezeigt, welche Aktionen für die Nachricht ausgeführt wurden, bevor Sie ihren endgültigen Status erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="c5214-p101">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization. You can determine if a message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="c5214-p102">Die Nachrichtenablaufverfolgung im Security & Compliance Center verbessert die Nachrichtenablaufverfolgung, die im Exchange Admin Center (EAC) verfügbar war. Sie können die Informationen aus der Nachrichtenablaufverfolgung verwenden, um Benutzer Fragen zu ihren Nachrichten zu beantworten, Probleme mit dem Nachrichtenfluss zu beheben und Richtlinienänderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c5214-p102">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC). You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="c5214-109">Nachrichtenablaufverfolgung öffnen</span><span class="sxs-lookup"><span data-stu-id="c5214-109">Open message trace</span></span>

1. <span data-ttu-id="c5214-110">[Melden Sie sich bei Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) mit Ihrem Firmen- oder Schulkonto an.</span><span class="sxs-lookup"><span data-stu-id="c5214-110">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="c5214-111">Wählen Sie das Symbol für das App-Startfeld ![Symbol für Office 365-App-Startfeld](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in der oberen linken Ecke und dann **Administrator** aus.</span><span class="sxs-lookup"><span data-stu-id="c5214-111">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="c5214-112">Erweitern Sie in der unteren linken Navigationsleiste **Admin Center** , und wählen Sie **Security & Compliance**aus.</span><span class="sxs-lookup"><span data-stu-id="c5214-112">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="c5214-113">Erweitern Sie auf der Seite **Sicherheit &-Konformität** , die geöffnet wird, die Option Nachrichten **Fluss**, und wählen Sie dann **Meldungsablauf Verfolgung**aus.</span><span class="sxs-lookup"><span data-stu-id="c5214-113">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="c5214-114">Seite "Nachrichtenablaufverfolgung"</span><span class="sxs-lookup"><span data-stu-id="c5214-114">Message trace page</span></span>

<span data-ttu-id="c5214-p103">Von hier aus können Sie eine neue Standardablaufverfolgung starten, indem Sie auf die Schaltfläche **Trace starten** klicken. Dadurch werden alle Nachrichten für alle Absender und Empfänger für die letzten zwei Tage gesucht. Sie können auch eine der gespeicherten Abfragen aus den verfügbaren Abfrage Kategorien verwenden und diese entweder wie folgt ausführen oder als Ausgangspunkt für eigene Abfragen verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5214-p103">From here you can start a new default trace by clicking on the **Start a trace** button. This will search for all messages for all senders and recipients for the last two days. Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="c5214-118">**Standardabfragen**: integrierte Abfragen, die von Office 365 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5214-118">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="c5214-119">**Benutzerdefinierte Abfragen**: von Administratoren in Ihrer Organisation gespeicherte Abfragen zur späteren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c5214-119">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="c5214-p104">**Autosaved Queries**: die letzten zehn zuletzt ausgeführten Abfragen. Diese Liste erleichtert die Abholung, wo Sie aufgehört haben.</span><span class="sxs-lookup"><span data-stu-id="c5214-p104">**Autosaved queries**: The last ten most recently run queries. This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="c5214-122">Auch auf dieser Seite finden Sie einen Abschnitt zum **Herunterladen von Berichten** für die von Ihnen übermittelten Anforderungen sowie die Berichte selbst, wenn der Download verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c5214-122">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="c5214-123">Optionen für eine neue Nachrichtenablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="c5214-123">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="c5214-124">Filtern nach Absender und Empfänger</span><span class="sxs-lookup"><span data-stu-id="c5214-124">Filter by senders and recipients</span></span>

<span data-ttu-id="c5214-125">Die Standardwerte sind **alle Absender** und **alle Empfänger**, aber Sie können die folgenden Felder zum Filtern der Ergebnisse verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5214-125">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="c5214-p105">**Von diesen Personen**: Klicken Sie in dieses Feld, um einen oder mehrere Absender aus Ihrer Organisation auszuwählen. Sie können auch beginnen, einen Namen einzugeben, und die Elemente in der Liste werden nach Ihren Eingaben gefiltert, ähnlich wie bei einer Such Seite.</span><span class="sxs-lookup"><span data-stu-id="c5214-p105">**By these people**: Click in this field to select one or more senders from your organization. You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="c5214-128">**Für diese Personen**: Klicken Sie in dieses Feld, um einen oder mehrere Empfänger in Ihrer Organisation auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c5214-128">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

<span data-ttu-id="c5214-p106">Sie können auch die e-Mail-Adressen von externen Absendern und Empfängern eingeben. Platzhalter werden unterstützt`*@contoso.com` ( `scot?@contoso.com`oder), aber Sie können nicht gleichzeitig mehrere Platzhaltereinträge im gleichen Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5214-p106">You can also type the email addresses of external senders and recipients. Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span>

### <a name="time-range"></a><span data-ttu-id="c5214-131">Zeitspanne</span><span class="sxs-lookup"><span data-stu-id="c5214-131">Time range</span></span>

<span data-ttu-id="c5214-p107">Der Standardwert beträgt **2 Tage**, Sie können jedoch Datums-und Zeitbereiche von bis zu 90 Tagen angeben. Berücksichtigen Sie bei der Verwendung von Datums-und Zeitbereichen folgende Probleme:</span><span class="sxs-lookup"><span data-stu-id="c5214-p107">The default value is **2 days**, but you can specify date/time ranges of up to 90 days. When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="c5214-p108">Standardmäßig wählen Sie den Zeitintervall in der **Schiebe** Ansicht mit einer Zeitlinie aus. Sie können nur die angezeigten Tages-oder Uhrzeiteinstellungen auswählen. Wenn Sie versuchen, einen dazwischen liegenden Wert auszuwählen, wird die Start/End-Blase an die nächste angezeigte Einstellung ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="c5214-p108">By default, you select the time range in **Slider** view using a time line. You can only select the day or time settings that are displayed. Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![Ein Slider-Zeitbereich in einer neuen Nachrichtenablaufverfolgung im Security & Compliance Center](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="c5214-p109">Sie können jedoch auch zur **benutzerdefinierten** Ansicht wechseln, in der Sie die Werte für **Start Datum** und Enddatum (einschließlich Zeiten) angeben können, und Sie können \*\*\*\* auch die Zeitzone für den Datums-und Uhrzeitbereich auswählen. \*\*\*\* Beachten Sie, dass die **Zeit Zonen** Einstellung sowohl für die Abfrage Eingaben als auch für die Abfrageergebnisse gilt.</span><span class="sxs-lookup"><span data-stu-id="c5214-p109">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range. Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![Ein benutzerdefinierter Zeitbereich in einer neuen Nachrichtenablaufverfolgung im Security & Compliance Center](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="c5214-p110">Für maximal 10 Tage stehen die Ergebnisse sofort als Zusammenfassungsbericht zur \*\*\*\* Verfügung. Wenn Sie einen Zeitabstand angeben, der sogar etwas größer als 10 Tage ist, werden die Ergebnisse verzögert, da Sie nur als herunterladbare CSV-Datei ( **Erweiterte Zusammenfassung** oder **Erweiterte** Berichte) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5214-p110">For 10 days or less, the results are available instantly as a **Summary** report. If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="c5214-143">Weitere Informationen zu den verschiedenen Berichtstypen finden Sie im Abschnitt [berichtsTyp auswählen](#choose-report-type) in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="c5214-143">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="c5214-p111">**Hinweis**: erweiterte Zusammenfassung und erweiterte Berichte werden mit archivierten Nachrichtenablauf Verfolgungsdaten erstellt, und es kann bis zu mehreren Stunden dauern, bis der Bericht zum Download verfügbar ist. Je nachdem, wie viele andere Administratoren auch Berichtsanforderungen gleichzeitig übermittelt haben, wird möglicherweise auch eine Verzögerung festgestellt, bevor die Verarbeitung für die Warteschlangen Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c5214-p111">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="c5214-p112">Beim Speichern einer Abfrage \*\*\*\* in der Schiebe Ansicht wird der relative Zeitintervall (beispielsweise 3 Tage von heute) gespeichert. Beim Speichern einer Abfrage in einer **benutzerdefinierten** Ansicht wird der absolute Datum/Uhrzeit-Zeitraum (beispielsweise 2018-05-06 13:00 bis 2018-05-08 18:00) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c5214-p112">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today). Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="c5214-148">Weitere Suchoptionen</span><span class="sxs-lookup"><span data-stu-id="c5214-148">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="c5214-149">ZuStellungsstatus</span><span class="sxs-lookup"><span data-stu-id="c5214-149">Delivery status</span></span>

<span data-ttu-id="c5214-150">Sie können den Standardwert **alle** ausgewählt lassen, oder Sie können einen der folgenden Werte auswählen, um die Ergebnisse zu filtern:</span><span class="sxs-lookup"><span data-stu-id="c5214-150">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="c5214-151">**Zustellung**: die Nachricht wurde erfolgreich an das vorgesehene Ziel übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c5214-151">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="c5214-152">**Pending**: die Übermittlung der Nachricht wird versucht oder erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="c5214-152">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="c5214-153">**Expanded**: ein Verteilergruppenempfänger wurde vor der Übergabe an die einzelnen Mitglieder der Gruppe erweitert.</span><span class="sxs-lookup"><span data-stu-id="c5214-153">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="c5214-154">**Fehler**: die Nachricht wurde nicht zugestellt.</span><span class="sxs-lookup"><span data-stu-id="c5214-154">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="c5214-p113">**Isoliert**: die Nachricht wurde isoliert (als Spam, Massenmail oder Phishing). Weitere Informationen finden Sie unter [Isolieren von e-Mail-Nachrichten in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5214-p113">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing). For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="c5214-157">**Gefiltert als Spam**: die Nachricht wurde als Spam identifiziert und wurde zurückgewiesen oder blockiert (nicht isoliert).</span><span class="sxs-lookup"><span data-stu-id="c5214-157">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="c5214-p114">**Status:** Die Nachricht wurde kürzlich von Office 365 empfangen, aber es sind noch keine anderen Statusdaten verfügbar. Checken Sie in wenigen Minuten.</span><span class="sxs-lookup"><span data-stu-id="c5214-p114">**Getting status:** The message was recently received by Office 365, but no other status data is yet available. Check back in a few minutes.</span></span>

<span data-ttu-id="c5214-p115">**Hinweis**: die Werte **Ausstehend,** **isoliert**und **Filter als Spam** sind nur für Suchvorgänge kleiner als 10 Tage verfügbar. Außerdem kann es eine Verzögerung von 5 bis 10 Minuten zwischen dem tatsächlichen und dem gemeldeten Zustellungsstatus geben.</span><span class="sxs-lookup"><span data-stu-id="c5214-p115">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days. Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="c5214-162">Nachrichten-ID</span><span class="sxs-lookup"><span data-stu-id="c5214-162">Message ID</span></span>

<span data-ttu-id="c5214-p116">Hierbei handelt es sich um die Internet Nachrichten-ID (auch als Client-ID bezeichnet), die im Nachrichtenkopf im Message **-ID:-** Kopfzeilenfeld gefunden wird. Benutzer können diesen Wert zur Untersuchung bestimmter Nachrichten angeben.</span><span class="sxs-lookup"><span data-stu-id="c5214-p116">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header. Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="c5214-p117">Dieser Wert ist für die Lebensdauer der Nachricht konstant. Bei Nachrichten, die in Office 365 oder Exchange erstellt wurden, hat der `<GUID@ServerFQDN>`Wert das Format, einschließlich der\< \>spitzen Klammern (). Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Andere Messagingsysteme verwenden möglicherweise unterschiedliche Syntax oder Werte. Dieser Wert soll eindeutig sein, aber nicht alle e-Mail-Systeme folgen genau dieser Anforderung. Wenn das **Message-ID:-** Kopfzeilenfeld für eingehende Nachrichten aus externen Quellen nicht vorhanden oder leer ist, wird ein beliebiger Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c5214-p117">This value is constant for the lifetime of the message. For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>). For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Other messaging systems might use different syntax or values. This value is supposed to be unique, but not all email systems strictly follow this requirement. If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="c5214-171">Wenn Sie die nach **richten-ID** zum Filtern der Ergebnisse verwenden, achten Sie darauf, dass Sie die vollständige Zeichenfolge einschließlich aller eckigen Klammern einschließen.</span><span class="sxs-lookup"><span data-stu-id="c5214-171">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="c5214-172">Direction</span><span class="sxs-lookup"><span data-stu-id="c5214-172">Direction</span></span>

<span data-ttu-id="c5214-173">Sie können den Standardwert **alle** ausgewählt lassen, oder Sie können **eingehende** (an Empfänger in Ihrer Organisation gesendete Nachrichten) oder **ausgehende** (Nachrichten, die von Benutzern in Ihrer Organisation gesendet werden) zum Filtern der Ergebnisse auswählen.</span><span class="sxs-lookup"><span data-stu-id="c5214-173">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="c5214-174">Ursprüngliche Client-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="c5214-174">Original client IP address</span></span>

<span data-ttu-id="c5214-p118">Sie können die Ergebnisse nach Client-IP-Adresse einreichen, um gehackte Computer zu untersuchen, die große Mengen an Spam oder Schadsoftware senden. Obwohl die Nachrichten scheinbar von mehreren Absendern stammen, ist es wahrscheinlich, dass der gleiche Computer alle Nachrichten generiert.</span><span class="sxs-lookup"><span data-stu-id="c5214-p118">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware. Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="c5214-177">**Hinweis**: die Client-IP-Adressinformationen sind nur 10 Tage lang verfügbar und stehen nur in den **erweiterten Zusammenfassungen** oder **erweiterten** Berichten (herunterladbare CSV-Dateien) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c5214-177">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="c5214-178">Berichtstyp auswählen</span><span class="sxs-lookup"><span data-stu-id="c5214-178">Choose report type</span></span>

<span data-ttu-id="c5214-179">Die verfügbaren Berichtstypen sind:</span><span class="sxs-lookup"><span data-stu-id="c5214-179">The available report types are:</span></span>

- <span data-ttu-id="c5214-p119">**Zusammenfassung**: verfügbar, wenn der Zeitintervall kürzer als 10 Tage ist und keine zusätzlichen Filteroptionen erforderlich sind. Die Ergebnisse sind fast unmittelbar nach dem Klicken auf **Suche**verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5214-p119">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options. The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="c5214-p120">**Erweiterte Zusammenfassung** oder **erweitert**: Diese Berichte sind nur als herunterladbare CSV-Dateien verfügbar und erfordern eine oder mehrere der folgenden Filteroptionen unabhängig vom Zeitintervall: **von diesen Personen** **zu diesen Personen**oder \*\* NachRichten-ID\*\*. Sie können Platzhalter für Absender oder Empfänger verwenden (beispielsweise \*@contoso. com).</span><span class="sxs-lookup"><span data-stu-id="c5214-p120">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**. You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="c5214-184">**Hinweise**:</span><span class="sxs-lookup"><span data-stu-id="c5214-184">**Notes**:</span></span>

- <span data-ttu-id="c5214-p121">Erweiterte Zusammenfassung und erweiterte Berichte werden mit archivierten Nachrichtenablauf Verfolgungsdaten erstellt, und es kann bis zu mehreren Stunden dauern, bis der Bericht zum Herunterladen verfügbar ist. Je nachdem, wie viele andere Administratoren auch Berichtsanforderungen gleichzeitig übermittelt haben, wird möglicherweise auch eine Verzögerung festgestellt, bevor die Verarbeitung der Warteschlangen Anforderung beginnt.</span><span class="sxs-lookup"><span data-stu-id="c5214-p121">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="c5214-187">Während Sie eine erweiterte Zusammenfassung oder einen erweiterten Bericht für einen beliebigen Datum/Uhrzeit-Zeitraum auswählen können, sind die letzten vier Stunden archivierter Daten für diese beiden Berichtstypen noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5214-187">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="c5214-p122">Wenn Sie auf **weiter**klicken, wird eine Zusammenfassungsseite mit den ausgewählten Filteroptionen, einem eindeutigen (bearbeitbaren) Titel für den Bericht und der e-Mail-Adresse angezeigt, die die Benachrichtigung erhält, wenn die Nachrichtenablaufverfolgung abgeschlossen ist (auch bearbeitbar, und muss sich in einer der akzeptierten Domänen Ihrer Organisation befinden). Klicken Sie auf **Bericht vorbereiten** , um die Nachrichtenablaufverfolgung zu übermitteln. Auf der Hauptseite der **Nachrichtenablaufverfolgung** wird der Status des Berichts im Abschnitt **zum Herunterladen von Berichten** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5214-p122">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains). Click **Prepare report** to submit the message trace. On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="c5214-191">Weitere Informationen zu den Informationen, die in den verschiedenen Berichtstypen zurückgegeben werden, finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="c5214-191">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="c5214-192">Ergebnisse der Nachrichtenablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="c5214-192">Message trace results</span></span>

<span data-ttu-id="c5214-p123">Die verschiedenen Berichtstypen geben unterschiedliche Informationsebenen zurück. Die in den verschiedenen Berichten verfügbaren Informationen werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5214-p123">The different report types return different levels of information. The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="c5214-195">Zusammenfassungsbericht Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c5214-195">Summary report output</span></span>

<span data-ttu-id="c5214-196">Nach dem Ausführen der Nachrichtenablaufverfolgung werden die Ergebnisse aufgelistet, sortiert nach absteigenden Datum/Uhrzeit (zuletzt zuerst).</span><span class="sxs-lookup"><span data-stu-id="c5214-196">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![Zusammenfassungsbericht Ergebnisse für die Nachrichtenablaufverfolgung im Security & Compliance Center](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="c5214-198">Der Zusammenfassungsbericht enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="c5214-198">The summary report contains the following information:</span></span>

- <span data-ttu-id="c5214-199">**Date**: das Datum und die Uhrzeit, zu der die Nachricht vom Dienst empfangen wurde, unter Verwendung der KONFIGURIERTen UTC-Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c5214-199">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="c5214-200">**Absender**: die e-Mail-Adresse des Absenders (*Alias*@*Domäne*).</span><span class="sxs-lookup"><span data-stu-id="c5214-200">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="c5214-p124">**Empfänger**: die e-Mail-Adresse des Empfängers oder Empfängers. Für eine Nachricht, die an mehrere Empfänger gesendet wird, gibt es eine Leitung pro Empfänger. Wenn es sich bei dem Empfänger um eine Verteilergruppe, eine dynamische Verteilergruppe oder eine e-Mail-aktivierte Sicherheitsgruppe handelt, ist die Gruppe der erste Empfänger, und dann befindet sich jedes Mitglied der Gruppe in einer separaten Leitung.</span><span class="sxs-lookup"><span data-stu-id="c5214-p124">**Recipient**: The email address of the recipient or recipients. For a message sent to multiple recipients, there's one line per recipient. If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="c5214-204">**Betreff**: die ersten 256 Zeichen des **Subject** -Felds der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c5214-204">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="c5214-205">**Status**: diese Werte werden im Abschnitt Zustellungs [Status](#delivery-status) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5214-205">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="c5214-p125">Standardmäßig werden die ersten 250-Ergebnisse geladen und stehen sofort zur Verfügung. Wenn Sie nach unten scrollen, gibt es eine leichte Pause, wenn der nächste Ergebnis Batch geladen wird. Anstatt einen Bildlauf durchzuführen, können Sie auf **alle laden** klicken, um alle Ergebnisse auf maximal 10.000 zu laden.</span><span class="sxs-lookup"><span data-stu-id="c5214-p125">By default, the first 250 results are loaded and readily available. When you scroll down, there's a slight pause as the next batch of results are loaded. Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="c5214-209">Sie können auf die Spaltenüberschriften klicken, um die Ergebnisse nach den Werten in dieser Spalte in aufsteigender oder absteigender Reihenfolge zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c5214-209">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="c5214-210">Sie können auf **Ergebnisse filtern** klicken, um die Ergebnisse nach einer oder mehreren Spalten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c5214-210">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="c5214-211">Sie können die Ergebnisse exportieren, nachdem Sie eine oder mehrere Zeilen ausgewählt haben, indem Sie auf **Ergebnisse exportieren** und dann **alle Ergebnisse**exportieren, geladene **Ergebnisse exportieren**oder **ausgewählte**exportieren auswählen.</span><span class="sxs-lookup"><span data-stu-id="c5214-211">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="c5214-212">Suchen nach verwandten Datensätzen für diese Nachricht</span><span class="sxs-lookup"><span data-stu-id="c5214-212">Find related records for this message</span></span>

<span data-ttu-id="c5214-p126">Verknüpfte Nachrichtendatensätze sind Datensätze, die dieselbe nachRichten-ID gemeinsam verwendet haben. Denken Sie daran, dass auch eine einzelne Nachricht, die zwischen zwei Personen gesendet wurde, mehrere Datensätze generieren kann. Die Anzahl der Datensätze wird erhöht, wenn die Nachricht von Verteilergruppenerweiterungen, Weiterleitung, Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) usw. beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="c5214-p126">Related message records are records that shared the same Message ID. Remember, even a single message sent between two people can generate multiple records. The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="c5214-216">Nachdem Sie das Kontrollkästchen einer Zeile ausgewählt haben, finden Sie verknüpfte Datensätze für die Nachricht, indem Sie auf die Schaltfläche **Verwandte Suchen** klicken, die angezeigt wird, oder indem Sie **Weitere Optionen** ![weitere](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Suche in Verbindung stehende Datensätze für diese Nachricht**auswählen.</span><span class="sxs-lookup"><span data-stu-id="c5214-216">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="c5214-217">Weitere Informationen zur nachRichten-ID finden Sie im Abschnitt nachRichten-ID weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="c5214-217">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="c5214-218">Details der Nachrichtenablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="c5214-218">Message trace details</span></span>

<span data-ttu-id="c5214-219">In der Ausgabe des Zusammenfassungsberichts können Sie Details zu einer Nachricht mit einer der folgenden Methoden anzeigen:</span><span class="sxs-lookup"><span data-stu-id="c5214-219">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="c5214-220">Wählen Sie die Zeile aus (Klicken Sie an eine beliebige Stelle in der Zeile mit Ausnahme des Kontrollkästchens).</span><span class="sxs-lookup"><span data-stu-id="c5214-220">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="c5214-221">Aktivieren Sie das Kontrollkästchen der Zeile, und klicken Sie auf **Weitere Optionen** ![mehr](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Ansichts Nachrichtendetails**.</span><span class="sxs-lookup"><span data-stu-id="c5214-221">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![Details nach dem Doppelklicken auf eine Zeile in der Zusammenfassungsbericht-Nachrichtenablaufverfolgung Ergebnisse im Security & Compliance Center](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="c5214-223">Die Details der Nachrichtenablaufverfolgung enthalten die folgenden zusätzlichen Informationen, die im Zusammenfassungsbericht nicht vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="c5214-223">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="c5214-p127">**Nachrichten Ereignisse**: Dieser Abschnitt enthält Klassifikationen, mit denen die Aktionen kategorisiert werden, die der Dienst für Nachrichten ausführt. Einige der interessantesten Ereignisse, die auftreten können, sind:</span><span class="sxs-lookup"><span data-stu-id="c5214-p127">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages. Some of the more interesting events that you might encounter are:</span></span>

   - <span data-ttu-id="c5214-226">**Receive**: die Nachricht wurde vom Dienst empfangen.</span><span class="sxs-lookup"><span data-stu-id="c5214-226">**Receive**: The message was received by the service.</span></span>

   - <span data-ttu-id="c5214-227">**Send**: die Nachricht wurde vom Dienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5214-227">**Send**: The message was sent by the service.</span></span>

   - <span data-ttu-id="c5214-228">**Fehler**: die Nachricht konnte nicht zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5214-228">**Fail**: The message failed to be delivered.</span></span>

   - <span data-ttu-id="c5214-229">**Deliver**: die Nachricht wurde an ein Postfach zugestellt.</span><span class="sxs-lookup"><span data-stu-id="c5214-229">**Deliver**: The message was delivered to a mailbox.</span></span>

   - <span data-ttu-id="c5214-230">**Expand**: die Nachricht wurde an eine erweiterte Verteilergruppe gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5214-230">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

   - <span data-ttu-id="c5214-231">**Übertragung**: Empfänger wurden aufgrund von Inhaltskonvertierung, Grenzwerten für Nachrichtenempfänger oder Agents zu einer gegabelten Nachricht verschoben.</span><span class="sxs-lookup"><span data-stu-id="c5214-231">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

   - <span data-ttu-id="c5214-232">\*\*\*\* Zurückstellen: die Nachrichtenübermittlung wurde verschoben und kann später erneut versucht werden.</span><span class="sxs-lookup"><span data-stu-id="c5214-232">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

   - <span data-ttu-id="c5214-p128">**Behoben**: die Nachricht wurde an eine neue Empfängeradresse umgeleitet, die auf einer Active Directory-Suche basiert. In diesem Fall wird die ursprüngliche Empfängeradresse zusammen mit dem endgültigen Übermittlungsstatus für die Nachricht in einer separaten Zeile in der Nachrichtenablaufverfolgung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5214-p128">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up. When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

   <span data-ttu-id="c5214-235">Beachten Sie, dass auch eine ereignislose Nachricht, die erfolgreich übermittelt wird, mehrere **Ereignis** Einträge in der Nachrichtenablaufverfolgung generiert.</span><span class="sxs-lookup"><span data-stu-id="c5214-235">Note that even an uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

- <span data-ttu-id="c5214-236">**Weitere Informationen**: Dieser Abschnitt enthält die folgenden Details:</span><span class="sxs-lookup"><span data-stu-id="c5214-236">**More information**: This section contains the following details:</span></span>

   - <span data-ttu-id="c5214-p129">Nach **richten-ID**: dieser Wert wird im Abschnitt nach [richten-ID](#message-id) weiter oben in diesem Thema beschrieben. Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="c5214-p129">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

   - <span data-ttu-id="c5214-239">**Nachrichtengröße**</span><span class="sxs-lookup"><span data-stu-id="c5214-239">**Message size**</span></span>

   - <span data-ttu-id="c5214-p130">**Von IP**: die IP-Adresse des Computers, von dem die Nachricht gesendet wurde. Für ausgehende Nachrichten, die von Exchange Online gesendet werden, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="c5214-p130">**From IP**: The IP address of the computer that sent the message. For outbound messages sent from Exchange Online, this value is blank.</span></span>

   - <span data-ttu-id="c5214-p131">**Zu IP**: die IP-Adresse oder die Adressen, an denen der Dienst versucht hat, die Nachricht zuzustellen. Wenn die Nachricht mehrere Empfänger hat, werden diese angezeigt. Für eingehende Nachrichten, die an Exchange Online gesendet werden, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="c5214-p131">**To IP**: The IP address or addresses where the service attempted to deliver the message. If the message has multiple recipients, these are displayed. For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="c5214-245">Erweiterte Zusammenfassungsberichte</span><span class="sxs-lookup"><span data-stu-id="c5214-245">Enhanced summary reports</span></span>

<span data-ttu-id="c5214-p132">Verfügbare (abgeschlossene) erweiterte Zusammenfassungsberichte stehen im Abschnitt zum **Herunterladen von Berichten** am Anfang der Nachrichtenablaufverfolgung zur Verfügung. Die folgenden Informationen sind im Bericht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c5214-p132">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace. The following information is available in the report:</span></span>

- <span data-ttu-id="c5214-248">**origin_timestamp**<sup>\*</sup>: das Datum und die Uhrzeit, zu der die Nachricht anfänglich vom Dienst empfangen wurde, unter Verwendung der konfigurierten UTC-Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c5214-248">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="c5214-249">**sender_address**: die e-Mail-Adresse des Absenders (*Alias*@*Domäne*).</span><span class="sxs-lookup"><span data-stu-id="c5214-249">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="c5214-p133">**Recipient_status**: der Status der Übermittlung der Nachricht an den Empfänger. Wenn die Nachricht an mehrere Empfänger gesendet wurde, werden alle Empfänger und der entsprechende Status für jeden im Format: \< *e-Mail-Adress*\>##\<*Status*\>angezeigt. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c5214-p133">**Recipient_status**: The status of the delivery of the message to the recipient. If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>. For example:</span></span>

   - <span data-ttu-id="c5214-253">**# #Receive, Send,** dass die Nachricht vom Dienst empfangen und an das vorgesehene Ziel gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-253">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

   - <span data-ttu-id="c5214-254">**# #Receive, Fail,** dass die Nachricht vom Dienst empfangen wurde, aber die Zustellung an das vorgesehene Ziel fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="c5214-254">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

   - <span data-ttu-id="c5214-255">**# #Receive, Deliver** : die Nachricht wurde vom Dienst empfangen und an das Postfach des Empfängers übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c5214-255">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="c5214-256">**message_subject**: die ersten 256 Zeichen des **Betreff** -Felds der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c5214-256">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="c5214-257">**total_bytes**: die Größe der Nachricht in Byte, einschließlich Anlagen.</span><span class="sxs-lookup"><span data-stu-id="c5214-257">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="c5214-p134">**message_id**: dieser Wert wird im Abschnitt nach [richten-ID](#message-id) weiter oben in diesem Thema beschrieben. Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="c5214-p134">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="c5214-p135">**network_message_id**: ein eindeutiger Wert für die Nachrichten-ID, der für alle Kopien der Nachricht beibehalten wird, die aufgrund von Verzweigungs-oder Verteilergruppenerweiterungen erstellt werden können. Ein Beispielwert ist `1341ac7b13fb42ab4d4408cf7f55890f`.</span><span class="sxs-lookup"><span data-stu-id="c5214-p135">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion. An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="c5214-262">**original_client_ip**: die IP-Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="c5214-262">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="c5214-263">**Direktionalität**: gibt an, ob die Nachricht eingehend (1) an Ihre Organisation gesendet wurde oder ob Sie ausgehend (2) von Ihrer Organisation gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-263">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="c5214-p136">**connector_id**: der Name des Quell-oder Ziel-Konnektors. Weitere Informationen zu Connectors in Exchange Online finden Sie unter [Configure Mail Flow using Connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span><span class="sxs-lookup"><span data-stu-id="c5214-p136">**connector_id**: The name of the source or destination connector. For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="c5214-266">**delivery_priority**<sup>\*</sup>: gibt an, ob die Nachricht mit **hoher**, **niedriger**oder **normaler** Priorität gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-266">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="c5214-267"><sup>\*</sup>Diese Eigenschaften sind nur in erweiterten Zusammenfassungsberichten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5214-267"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="c5214-268">Erweiterte Berichte</span><span class="sxs-lookup"><span data-stu-id="c5214-268">Extended reports</span></span>

<span data-ttu-id="c5214-p137">Verfügbare (abgeschlossene) Erweiterte Berichte stehen am Anfang der Nachrichtenablaufverfolgung im Abschnitt zum **Herunterladen von Berichten** zur Verfügung. Praktisch alle Informationen aus einem erweiterten Zusammenfassungsbericht stehen in einem erweiterten Bericht (mit Ausnahme von **origin_timestamp** und **delivery_priority**) zur Verfügung. Die folgenden zusätzlichen Informationen stehen nur in einem erweiterten Bericht zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c5214-p137">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace. Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**). The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="c5214-272">**client_ip**: die IP-Adresse des e-Mail-Servers oder Messaging-Clients, der die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="c5214-272">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="c5214-273">**client_hostname**: der Hostname oder FQDN des e-Mail-Servers oder des Messagingclients, der die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="c5214-273">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="c5214-274">**server_ip**: die IP-Adresse des Quell-oder Zielservers.</span><span class="sxs-lookup"><span data-stu-id="c5214-274">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="c5214-275">**server_hostname**: der Hostname oder FQDN des Zielservers.</span><span class="sxs-lookup"><span data-stu-id="c5214-275">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="c5214-p138">**source_context**: zusätzliche Informationen, die dem **Quellfeld** zugeordnet sind. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c5214-p138">**source_context**: Extra information associated with the **source** field. For example:</span></span>

   - `Protocol Filter Agent`

   - `3489061114359050000`

- <span data-ttu-id="c5214-p139">**Quelle**: die Exchange Online-Komponente, die für das Ereignis zuständig ist. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c5214-p139">**source**: The Exchange Online component that's responsible for the event. For example:</span></span>

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- <span data-ttu-id="c5214-280">**event_id**: Diese entsprechen den **Nachrichtenereignis** Werten, die im Abschnitt [verwandte Datensätze für diese Nachricht suchen](#find-related-records-for-this-message) erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="c5214-280">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="c5214-281">**internal_message_id**: eine Nachrichten-ID, die vom Exchange Online-Server zugewiesen wird, der die Nachricht derzeit verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c5214-281">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="c5214-p140">**recipient_address**: die e-Mail-Adressen der Empfänger der Nachricht. Mehrere e-Mail-Adressen werden durch das Semikolon (;) getrennt.</span><span class="sxs-lookup"><span data-stu-id="c5214-p140">**recipient_address**: The email addresses of the message's recipients. Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="c5214-284">**recipient_count**: die Gesamtzahl der Empfänger in der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c5214-284">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="c5214-285">**related_recipient_address**: wird mit `EXPAND`, `REDIRECT`und `RESOLVE` Ereignissen verwendet, um andere Empfänger-e-Mail-Adressen anzuzeigen, die der Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c5214-285">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="c5214-p141">**Referenz**: Dieses Feld enthält zusätzliche Informationen für bestimmte Ereignistypen. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c5214-p141">**reference**: This field contains additional information for specific types of events. For example:</span></span>

   - <span data-ttu-id="c5214-p142">**DSN**: enthält den Bericht Link, bei dem es sich um den **message_id** -Wert der zugehörigen Benachrichtigung über den Zustellungsstatus (auch als DSN, Unzustellbarkeitsbericht, NDR oder Bounce-Nachricht bezeichnet) handelt, wenn nach diesem Ereignis ein DSN generiert wird. Wenn es sich um eine DSN-Nachricht handelt, enthält dieses Feld den **message_id** -Wert der ursprünglichen Nachricht, für die der DSN generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-p142">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event. If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

   - <span data-ttu-id="c5214-290">**Expand**: enthält den **related_recipient_address** -Wert der zugehörigen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c5214-290">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

   - <span data-ttu-id="c5214-291">**Receive**: kann den **message_id** -Wert der zugehörigen Nachricht enthalten, wenn die Nachricht von anderen Prozessen generiert wurde (beispielsweise Posteingangsregeln).</span><span class="sxs-lookup"><span data-stu-id="c5214-291">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

   - <span data-ttu-id="c5214-292">**Send**: enthält den **internal_message_id** -Wert aller DSN-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c5214-292">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

   - <span data-ttu-id="c5214-293">**Transfer**: enthält den **internal_message_id** -Wert der Nachricht, die verzweigt wird (beispielsweisedurch Inhaltskonvertierung, Limits für Nachrichtenempfänger oder Agents).</span><span class="sxs-lookup"><span data-stu-id="c5214-293">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

   - <span data-ttu-id="c5214-294">**MAILBOXRULE**: enthält den **internal_message_id** -Wert der eingehenden Nachricht, die dazu geführt hat, dass die Posteingangsregel die ausgehende Nachricht generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c5214-294">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

   <span data-ttu-id="c5214-295">Für andere Ereignistypen ist dieses Feld zumeist leer.</span><span class="sxs-lookup"><span data-stu-id="c5214-295">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="c5214-p143">**return_path**: die Absender-e-Mail-Adresse, die vom Befehl **Mail from** angegeben wurde, der die Nachricht gesendet hat. Obwohl dieses Feld nie leer ist, kann es den Wert der NULL-Absenderadresse haben `<>`, der als angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5214-p143">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message. Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="c5214-p144">**message_info**: zusätzliche Informationen zur Nachricht. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c5214-p144">**message_info**: Additional information about the message. For example:</span></span>

   - <span data-ttu-id="c5214-p145">Die Datum-Uhrzeit der Nachrichtenerstellung in UTC für `DELIVER` und `SEND` Ereignisse. Die Datum-Uhrzeit der Entstehung ist der Zeitpunkt, zu dem die Nachricht zuerst in die Exchange Online-Organisation eingegeben wurde. Die UTC-Datums-und-Uhrzeit wird im ISO 8601 Date-Time- `yyyy-mm-ddThh:mm:ss.fffZ`Format dargestellt `yyyy` :, where `mm` = Year, `dd` = month, `T` = Day, gibt den Anfang der Zeit `hh` Komponente an, `mm` = Stunde, `ss` = Minute, `fff` = Sekunde, = Sekundenbruchteile und `Z` gibt an `Zulu`, was eine andere Möglichkeit zum bezeichnen der UTC ist.</span><span class="sxs-lookup"><span data-stu-id="c5214-p145">The message origination date-time in UTC for `DELIVER` and `SEND` events. The origination date-time is the time when the message first entered the Exchange Online organization. The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

   - <span data-ttu-id="c5214-p146">Authentifizierungsfehler. Möglicherweise wird der Wert `11a` und der Authentifizierungstyp angezeigt, der beim Auftreten des Authentifizierungsfehlers verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-p146">Authentication errors. For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="c5214-305">**tenant_id**: ein GUID-Wert, der die Exchange Online-Organisation darstellt ( `39238e87-b5ab-4ef6-a559-af54c6b07b42`beispielsweise).</span><span class="sxs-lookup"><span data-stu-id="c5214-305">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="c5214-306">**original_server_ip**: die IP-Adresse des ursprünglichen Servers.</span><span class="sxs-lookup"><span data-stu-id="c5214-306">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="c5214-p147">**custom_data**: enthält Daten zu bestimmten Ereignistypen. Weitere Informationen finden Sie in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="c5214-p147">**custom_data**: Contains data related to specific event types. For more information, see the following sections.</span></span>

#### <a name="customdata-values"></a><span data-ttu-id="c5214-309">custom_data-Werte</span><span class="sxs-lookup"><span data-stu-id="c5214-309">custom_data values</span></span>

<span data-ttu-id="c5214-p148">Das **Custom_data** -Feld für `AGENTINFO` ein Ereignis wird von einer Vielzahl von Exchange Online-Agents verwendet, um Details zur Nachrichtenverarbeitung zu protokollieren. Einige der interessantesten Agents werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5214-p148">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details. Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="c5214-312">Spam Filter-Agent</span><span class="sxs-lookup"><span data-stu-id="c5214-312">Spam filter agent</span></span>

<span data-ttu-id="c5214-p149">Ein **custom_data** -Wert, der `S:SFA` mit beginnt, stammt vom Spamfilter-Agent. Die wichtigsten Details werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c5214-p149">A **custom_data** value that starts with `S:SFA` is from the spam filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="c5214-315">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c5214-315">**Value**</span></span>|<span data-ttu-id="c5214-316">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5214-316">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="c5214-317">Die Nachricht wurde als "Nicht-Spam" markiert und an die vorgesehenen Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5214-317">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="c5214-318">Die Nachricht wurde vom Inhaltsfilter als Spam markiert.</span><span class="sxs-lookup"><span data-stu-id="c5214-318">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="c5214-319">Die Filterung wurde übergangen, und die Nachricht wurde gesperrt, da sie von einem gesperrten Absender stammt.</span><span class="sxs-lookup"><span data-stu-id="c5214-319">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="c5214-p150">Die Nachricht wurde bereits als Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Spam markiert und alle zusätzlichen Filterungen umgeht.</span><span class="sxs-lookup"><span data-stu-id="c5214-p150">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="c5214-322">Weitere Informationen zu den verschiedenen SCL-Werten und deren Bedeutung finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5214-322">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="c5214-p151">Der PCL-Wert (Phishing Confidence Level) der Nachricht. Diese Werte können auf die gleiche Weise interpretiert werden wie die in [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx) dokumentierten SCL-Werte.  </span><span class="sxs-lookup"><span data-stu-id="c5214-p151">The Phishing Confidence Level (PCL) value of the message. These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="c5214-325">Der Absender der Nachricht wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="c5214-325">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="c5214-326">Die Nachricht wurde unter Quarantäne gestellt.</span><span class="sxs-lookup"><span data-stu-id="c5214-326">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="c5214-327">Die Nachricht wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c5214-327">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="c5214-328">Die Nachricht wurde an den Ordner "Junk-E-Mail" des Empfängers gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5214-328">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="c5214-p152">Die Nachricht wurde über den Pool mit höherem risikobereit gestellt. Weitere Informationen finden Sie unter [High-Risk-Übermittlungs Pool für ausgehende Nachrichten](https://technet.microsoft.com/library/jj200746.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5214-p152">The message was routed through the higher risk delivery pool. For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="c5214-331">Die Nachricht wurde durch den normalen Pool für ausgehende Zustellungen geleitet.</span><span class="sxs-lookup"><span data-stu-id="c5214-331">The message was routed through the normal outbound delivery pool.</span></span>|
|`SFS=[a]|SFS=[b]`|<span data-ttu-id="c5214-332">Dies bedeutet, dass Übereinstimmungen mit den Spam-Regeln gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="c5214-332">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="c5214-333">Die Nachricht wurde durch die Spam-Filter gelassen, weil die IP-Adrese in einer IP-Zulassungsliste im Verbindungsfilter angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-333">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="c5214-334">Die HELO-oder EHLO-Zeichenfolge des verbundenen e-Mail-Servers.</span><span class="sxs-lookup"><span data-stu-id="c5214-334">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="c5214-335">Der PTR-Eintrag der IP-Adresse des Absenders, auch bekannt als Reverse-DNS-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c5214-335">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="c5214-336">Ein Beispiel für einen **custom_data** -Wert für eine Nachricht, die wie folgt gefiltert wird:</span><span class="sxs-lookup"><span data-stu-id="c5214-336">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="c5214-337">Malware Filter-Agent</span><span class="sxs-lookup"><span data-stu-id="c5214-337">Malware filter agent</span></span>

<span data-ttu-id="c5214-p153">Ein **custom_data** -Wert, der `S:AMA` mit beginnt, stammt vom Malware Filter-Agent. Die wichtigsten Details werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c5214-p153">A **custom_data** value that starts with `S:AMA` is from the malware filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="c5214-340">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c5214-340">**Value**</span></span>|<span data-ttu-id="c5214-341">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5214-341">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5214-342">`AMA=SUM|v=1|`oder`AMA=EV|v=1`</span><span class="sxs-lookup"><span data-stu-id="c5214-342">`AMA=SUM|v=1|` or `AMA=EV|v=1`</span></span>|<span data-ttu-id="c5214-p154">Die Nachricht wurde als Schadsoftware festgelegt. `SUM` gibt an, dass die Schadsoftware von einer beliebigen Anzahl von Modulen erkannt wurde. `EV` gibt an, dass die Schadsoftware von einem bestimmten Modul erkannt wurde. Wenn Schadsoftware von einem Modul erkannt wird, löst dies die nachfolgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="c5214-p154">The message was determined to contain malware. `SUM` indicates the malware could've been detected by any number of engines. `EV` indicates the malware was detected by a specific engine. When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="c5214-347">Die Nachricht wurde ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c5214-347">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="c5214-348">Die Nachricht wurde umgangen.</span><span class="sxs-lookup"><span data-stu-id="c5214-348">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="c5214-349">Die Nachricht wurde zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="c5214-349">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="c5214-350">Die Nachricht wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c5214-350">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="c5214-351">Die Nachricht wurde umgangen.</span><span class="sxs-lookup"><span data-stu-id="c5214-351">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="c5214-352">Die Nachricht wurde umgangen.</span><span class="sxs-lookup"><span data-stu-id="c5214-352">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="c5214-353">Die Nachricht wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="c5214-353">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="c5214-354">Die Nachricht wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="c5214-354">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="c5214-355">Die Nachricht wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="c5214-355">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="c5214-356">Der Name der Schadsoftware, die gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-356">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="c5214-357">Der Name der Datei, welche die Schadsoftware enthielt.</span><span class="sxs-lookup"><span data-stu-id="c5214-357">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="c5214-358">Ein Beispiel für einen **custom_data** -Wert für eine Nachricht mit Schadsoftware sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c5214-358">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="c5214-359">Transport Regel-Agent</span><span class="sxs-lookup"><span data-stu-id="c5214-359">Transport Rule agent</span></span>

<span data-ttu-id="c5214-p155">Ein **custom_data** -Wert, der`S:TRA` mit beginnt, stammt aus dem Transportregel-Agent für Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet). Die wichtigsten Details werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c5214-p155">A **custom_data** value that starts with`S:TRA` is from the Transport Rule agent for mail flow rules (also known as transport rules). The key details are described in the following table:</span></span>

|<span data-ttu-id="c5214-362">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c5214-362">**Value**</span></span>|<span data-ttu-id="c5214-363">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5214-363">**Description**</span></span>|
|:-----|:-----|
|`ETR|ruleId=<guid>`|<span data-ttu-id="c5214-364">Die ID der Regel, die abgeglichen wurde.</span><span class="sxs-lookup"><span data-stu-id="c5214-364">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="c5214-365">Das Datum und die Uhrzeit in UTC, als die Regelübereinstimmung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c5214-365">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="c5214-p156">Die Aktion, die angewendet wurde. Eine Liste der verfügbaren Aktionen finden Sie unter [Aktionen für Nachrichtenfluss Regeln in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5214-p156">The action that was applied. For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="c5214-p157">Der Modus der Regel. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c5214-p157">The mode of the rule. Valid values are: </span></span><br/><span data-ttu-id="c5214-370">• **Erzwingen**: alle Aktionen für die Regel werden erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c5214-370">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="c5214-371">• **Test mit Richtlinien Tipps:**: alle richtlinientipp Aktionen werden gesendet, aber andere Durchsetzungs Aktionen werden nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5214-371">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="c5214-372">• **Test ohne Richtlinien Tipps**: Aktionen werden in einer Protokolldatei aufgelistet, aber die Absender werden nicht benachrichtigt, und es werden keine Durchsetzungs Aktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5214-372">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="c5214-373">Ein Beispiel für einen **custom_data** -Wert für eine Nachricht, die den Bedingungen einer Nachrichtenfluss Regel entspricht, sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c5214-373">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`

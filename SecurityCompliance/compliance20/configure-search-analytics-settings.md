---
title: Konfigurieren der Such- und Analyseeinstellungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 253650bb9916da8260491870d1a0bc899d6245c8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217105"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="8eb65-102">Konfigurieren der Such- und Analyseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="8eb65-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="8eb65-103">Near-Duplikate und e-Mail-Threading</span><span class="sxs-lookup"><span data-stu-id="8eb65-103">Near duplicates and email threading</span></span>

<span data-ttu-id="8eb65-104">In diesem Abschnitt können Sie Parameter für die doppelte Erkennung, fast doppelt Erkennung und e-Mail-Threading festlegen.</span><span class="sxs-lookup"><span data-stu-id="8eb65-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="8eb65-p101">Aktivieren/deaktivieren: doppelte Erkennung, Erkennung in der Nähe von Duplikaten und e-Mail-Threading als Teil des Analyse Flusses, falls aktiviert, einbeziehen. Da Sie sich übereinander aufbauen, müssen Sie alle aktivieren oder alle deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8eb65-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="8eb65-107">Schwellenwert: Wenn die Ähnlichkeits Stufe zweier Dokumente über dem Schwellenwert liegt, werden Sie in derselben fast doppelt vorhandenen Gruppe platziert.</span><span class="sxs-lookup"><span data-stu-id="8eb65-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="8eb65-p102">Duplikate standardmäßig ausblenden: Wenn diese Einstellung aktiviert ist, wird standardmäßig ein Filter zum Ausblenden doppelter Dokumente angewendet. Der Filter kann bei Bedarf manuell im Arbeitssatz entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8eb65-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="8eb65-p103">Minimale/maximale Anzahl von Wörtern: in der Nähe von Duplikaten und e-Mail-Threading wird nur für Dokumente ausgeführt, die mindestens die Mindestanzahl von Wörtern und höchstens die maximale Anzahl von Wörtern aufweisen. Weitere Informationen finden Sie unter [near Duplicate Detection](near-duplicates.md) and [Email Threading](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="8eb65-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="8eb65-112">Designs</span><span class="sxs-lookup"><span data-stu-id="8eb65-112">Themes</span></span>

<span data-ttu-id="8eb65-113">In diesem Abschnitt können Sie Parameter für Designs festlegen.</span><span class="sxs-lookup"><span data-stu-id="8eb65-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="8eb65-114">Aktivieren/deaktivieren: Thema-Clustering als Teil des Analyse Flusses einbeziehen, falls aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8eb65-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="8eb65-p104">Stellen Sie die maximale Anzahl von Designs dynamisch dynamisch ein: in bestimmten Fällen gibt es nicht genügend Dokumente, um die gewünschte Anzahl von Designs zu erzeugen. Wenn diese Einstellung aktiviert ist, wird anstelle der gewünschten maximalen Anzahl von Designs das System die maximale Anzahl von Designs dynamisch angepasst.</span><span class="sxs-lookup"><span data-stu-id="8eb65-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="8eb65-117">Maximale Anzahl von Designs: gewünschte Anzahl von Designs</span><span class="sxs-lookup"><span data-stu-id="8eb65-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="8eb65-118">Zahlen in Designs einbeziehen: Wenn diese Option aktiviert ist, werden beim Generieren von Designs Zahlen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8eb65-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="8eb65-119">Optische Zeichenerkennung (OCR)</span><span class="sxs-lookup"><span data-stu-id="8eb65-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="8eb65-120">Wenn diese Einstellung aktiviert ist, wird die OCR auf Bildern ausgeführt, die in Arbeitsmappen aufgenommen werden, damit Sie durchsuchbar werden können.</span><span class="sxs-lookup"><span data-stu-id="8eb65-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="8eb65-121">Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="8eb65-121">Ignore text</span></span>

<span data-ttu-id="8eb65-p105">Es gibt Fälle, in denen bestimmte Texte die Qualität der Analysen verringern, wie lange Haftungsausschlüsse, die zu bestimmten e-Mails hinzugefügt werden, unabhängig vom Inhalt der e-Mail. Wenn Sie solche Fälle wissen, können Sie diesen Text aus der Analyse ausschließen, indem Sie den Text angeben (RegEx wird unterstützt) und für welche Module Dieser Text ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8eb65-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>
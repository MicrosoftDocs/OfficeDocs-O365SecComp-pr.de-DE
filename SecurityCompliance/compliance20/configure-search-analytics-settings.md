---
title: Konfigurieren der Suche und-Analyse
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607787"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="9aab9-102">Konfigurieren der Suche und-Analyse</span><span class="sxs-lookup"><span data-stu-id="9aab9-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="9aab9-103">In der Nähe von Duplikaten und threading-e-Mail</span><span class="sxs-lookup"><span data-stu-id="9aab9-103">Near duplicates and email threading</span></span>

<span data-ttu-id="9aab9-104">In diesem Abschnitt können Sie die Parameter für die Erkennung von Duplikaten, in der Nähe Erkennung von Duplikaten und e-Mail-threading festlegen.</span><span class="sxs-lookup"><span data-stu-id="9aab9-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="9aab9-p101">Aktivieren/deaktivieren: enthalten Sie Erkennung von Duplikaten, in der Nähe Erkennung von Duplikaten und e-Mail-threading als Teil des Analytics Ablauf aktiviert. Da sie übereinander erstellen, müssen Sie alle diese aktivieren oder Deaktivieren aller Folien.</span><span class="sxs-lookup"><span data-stu-id="9aab9-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="9aab9-107">Schwellenwert: Wenn die Ebene der Ähnlichkeit von zwei Dokumenten oberhalb der Schwelle sind, werden sie in der gleichen nahezu doppelte Set versetzt.</span><span class="sxs-lookup"><span data-stu-id="9aab9-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="9aab9-p102">Ausblenden von Duplikaten standardmäßig: Wenn diese Einstellung aktiviert ist, wird ein Filter, um doppelte Dokumente ausblenden in die Arbeitsseiten standardmäßig angewendet werden. Der Filter kann manuell in die Arbeitsseiten bei Bedarf entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9aab9-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="9aab9-p103">Minimale/maximale Anzahl von Wörtern: in der Nähe von Duplikaten und e-Mail-threading nur bei Dokumenten mit mindestens die minimale Anzahl von Wörtern und höchstens die maximale Anzahl von Wörtern ausgeführt wird. Weitere Informationen finden Sie [in der Nähe Erkennung von Duplikaten](near-duplicates.md) und [threading-e-Mail](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="9aab9-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="9aab9-112">Designs</span><span class="sxs-lookup"><span data-stu-id="9aab9-112">Themes</span></span>

<span data-ttu-id="9aab9-113">In diesem Abschnitt können Sie die Parameter für Designs festlegen.</span><span class="sxs-lookup"><span data-stu-id="9aab9-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="9aab9-114">Aktivieren/deaktivieren: enthalten Sie Designs clustering als Teil des Analytics Ablauf aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9aab9-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="9aab9-p104">Maximale Anzahl von Designs dynamisch dynamisch anpassen: in bestimmten Fällen sind nicht genügend Dokumente, um die gewünschte Anzahl von Designs zu erstellen. Wenn diese Einstellung aktiviert ist, klicken Sie dann statt So erzwingen Sie die gewünschte maximale Anzahl von Designs, versucht das System maximale Anzahl von Designs passt dynamisch an.</span><span class="sxs-lookup"><span data-stu-id="9aab9-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="9aab9-117">Maximale Anzahl von Designs: gewünschte Anzahl der Designs</span><span class="sxs-lookup"><span data-stu-id="9aab9-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="9aab9-118">Zahlen in Designs enthalten: Wenn aktiviert, wird es Zahlen in einschließen, wenn Designs zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9aab9-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="9aab9-119">Optische zeichenerkennung (OCR)</span><span class="sxs-lookup"><span data-stu-id="9aab9-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="9aab9-120">Wenn diese Einstellung aktiviert ist, wird OCR auf Bilder ausgeführt werden, die in Arbeitsseiten aufgenommen werden, damit sie durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="9aab9-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="9aab9-121">Ignorieren von text</span><span class="sxs-lookup"><span data-stu-id="9aab9-121">Ignore text</span></span>

<span data-ttu-id="9aab9-p105">Es gibt Situationen, in dem bestimmte Texte die Qualität der Analyse, wie lange Haftungsausschlüssen abnehmen, die auf bestimmte unabhängig vom Inhalt der e-Mail-e-Mails hinzugefügt werden. Wenn Sie solchen Fällen kennen, können Sie diesen Text aus Analytics ausschließen, indem Text (RegEx wird unterstützt) und dem angibt Module, die für Text ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9aab9-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>
---
title: Verwenden des Kommunikations-Editors
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
ms.openlocfilehash: b148ff1a77cd9225a26f98e7612e9fb5b57331e3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706056"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="92a83-102">Verwenden des Kommunikations-Editors</span><span class="sxs-lookup"><span data-stu-id="92a83-102">Use the communications editor</span></span>

<span data-ttu-id="92a83-103">Wie Sie den Inhalt Ihrer Portalinhalt definieren, Legal halten, Benachrichtigungen und Erinnerungen/Eskalationen Verwandte, und Sie können den Communications-Editor, formatieren und dynamisch anpassen Ihrer Inhalte nutzen.</span><span class="sxs-lookup"><span data-stu-id="92a83-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="92a83-104">Rich-Text-editor</span><span class="sxs-lookup"><span data-stu-id="92a83-104">Rich text editor</span></span> 

<span data-ttu-id="92a83-p101">Der Communications-Editor können Benutzer zum Anpassen des Texts mithilfe der Editoroptionen. Benutzer können beispielsweise Schriftarttypen ändern, Erstellen von Listen mit Aufzählungszeichen, Hervorheben Inhalts- und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="92a83-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="92a83-107">Zusammenführen von Feldvariablen</span><span class="sxs-lookup"><span data-stu-id="92a83-107">Merge field variables</span></span>

<span data-ttu-id="92a83-p102">Sie können e-Mail-Zusammenführung Variablen aus dem Communications-Editor angepassten Verwaltungsberechtigter Attribute in Textkörper eine Mitteilung einbetten nutzen. Wenn an der Verwaltungsberechtigte gesendet wird, wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt werden. Beispielsweise würde beim an Verwaltungsberechtigter John Smith gesendet, das Seriendruckfeld [Verwaltungsberechtigter Name] mit dem entsprechenden Namen übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="92a83-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="92a83-p103">E-Mail-zusammenführungsfelds können, indem Sie die Symbole **Seriendruckfeld** am oberen Rand der Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird je deaktiviert den Speicherort der Cursor des Benutzers hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="92a83-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="92a83-113">Liste der Merge Feldvariablen</span><span class="sxs-lookup"><span data-stu-id="92a83-113">List of merge field variables</span></span>

| <span data-ttu-id="92a83-114">Feldname</span><span class="sxs-lookup"><span data-stu-id="92a83-114">Field name</span></span>                  | <span data-ttu-id="92a83-115">Feld-details</span><span class="sxs-lookup"><span data-stu-id="92a83-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="92a83-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="92a83-116">Display Name</span></span>  | <span data-ttu-id="92a83-117">Der Verwaltungsberechtigte vor- und Nachname.</span><span class="sxs-lookup"><span data-stu-id="92a83-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="92a83-118">Bestätigung Link</span><span class="sxs-lookup"><span data-stu-id="92a83-118">Acknowledgement Link</span></span> | <span data-ttu-id="92a83-119">Angepasste Link zu jedem Verwaltungsberechtigter Bestätigung aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="92a83-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="92a83-120">Portal-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="92a83-120">Portal Link</span></span>     | <span data-ttu-id="92a83-121">Eine benutzerdefinierte Verknüpfung für der Verwaltungsberechtigte Compliance-Portal.</span><span class="sxs-lookup"><span data-stu-id="92a83-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="92a83-122">Ausstellen Officer</span><span class="sxs-lookup"><span data-stu-id="92a83-122">Issuing Officer</span></span>                   | <span data-ttu-id="92a83-123">Die e-Mail-Adresse von der angegebenen ausstellenden Officer.</span><span class="sxs-lookup"><span data-stu-id="92a83-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="92a83-124">Ausstellen von Datum</span><span class="sxs-lookup"><span data-stu-id="92a83-124">Issuing Date</span></span>                   | <span data-ttu-id="92a83-125">Das Datum, das die Bekanntmachung (UTC) ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="92a83-125">The date that the notice was issued (UTC).</span></span>              |
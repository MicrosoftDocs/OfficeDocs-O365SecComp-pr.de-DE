---
title: Verwenden des Kommunikations-Editors
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
ms.openlocfilehash: 967320aeb960258d77d90cca4e3b681849f9952e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215805"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="216f8-102">Verwenden des Kommunikations-Editors</span><span class="sxs-lookup"><span data-stu-id="216f8-102">Use the communications editor</span></span>

<span data-ttu-id="216f8-103">Wenn Sie den Inhalt Ihres Portalinhalts, rechtliche Aufbewahrungs Benachrichtigungen und zugehörige Erinnerungen/Eskalationen definieren, können Sie den Kommunikations-Editor nutzen, um Ihre Inhalte zu formatieren und dynamisch anzupassen.</span><span class="sxs-lookup"><span data-stu-id="216f8-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="216f8-104">Rich-Text-Editor</span><span class="sxs-lookup"><span data-stu-id="216f8-104">Rich text editor</span></span> 

<span data-ttu-id="216f8-p101">Der Kommunikations-Editor ermöglicht es dem Benutzer, den Text mithilfe der Editor-Optionen anzupassen. Benutzer können beispielsweise Schriftarten ändern, Aufzählungslisten erstellen, Inhalte hervorheben und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="216f8-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="216f8-107">Feld Variablen zusammenführen</span><span class="sxs-lookup"><span data-stu-id="216f8-107">Merge field variables</span></span>

<span data-ttu-id="216f8-p102">Sie können die e-Mail-Zusammenführungs Variablen aus dem Kommunikations-Editor nutzen, um angepasste Depot Attribute in den Textkörper einer Kommunikation einzubetten. Bei der Übermittlung an die Depotbank wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt. Wenn Sie beispielsweise an Depotbank John Smith gesendet haben, würde das Seriendruckfeld [Depot Name] mit dem entsprechenden Namen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="216f8-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="216f8-p103">Sie können e-Mail-Seriendruckfelder verwenden, indem Sie die Symbole für das **Seriendruckfeld** oben im Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird basierend auf dem Speicherort des Cursors der Benutzer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="216f8-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="216f8-113">Liste der Seriendruckfeld Variablen</span><span class="sxs-lookup"><span data-stu-id="216f8-113">List of merge field variables</span></span>

| <span data-ttu-id="216f8-114">Feldname</span><span class="sxs-lookup"><span data-stu-id="216f8-114">Field name</span></span>                  | <span data-ttu-id="216f8-115">Feld Details</span><span class="sxs-lookup"><span data-stu-id="216f8-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="216f8-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="216f8-116">Display Name</span></span>  | <span data-ttu-id="216f8-117">Der vor-und Nachname der Depotbank.</span><span class="sxs-lookup"><span data-stu-id="216f8-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="216f8-118">Bestätigungs Link</span><span class="sxs-lookup"><span data-stu-id="216f8-118">Acknowledgement Link</span></span> | <span data-ttu-id="216f8-119">Ein benutzerdefinierter Link zum Aufzeichnen der Bestätigung der einzelnen depotverwalter.</span><span class="sxs-lookup"><span data-stu-id="216f8-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="216f8-120">Portal Link</span><span class="sxs-lookup"><span data-stu-id="216f8-120">Portal Link</span></span>     | <span data-ttu-id="216f8-121">Ein angepasster Link für das Compliance-Portal des Depotbank.</span><span class="sxs-lookup"><span data-stu-id="216f8-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="216f8-122">AusStellende Offizier</span><span class="sxs-lookup"><span data-stu-id="216f8-122">Issuing Officer</span></span>                   | <span data-ttu-id="216f8-123">Die e-Mail-Adresse des angegebenen ausstellenden Offiziers.</span><span class="sxs-lookup"><span data-stu-id="216f8-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="216f8-124">AusStellendes Datum</span><span class="sxs-lookup"><span data-stu-id="216f8-124">Issuing Date</span></span>                   | <span data-ttu-id="216f8-125">Das Datum, an dem der Hinweis ausgegeben wurde (UTC).</span><span class="sxs-lookup"><span data-stu-id="216f8-125">The date that the notice was issued (UTC).</span></span>              |
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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c2957c88217bce4c9a34f8d3f9a9e291f1223cc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241242"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="6e614-102">Verwenden des Kommunikations-Editors</span><span class="sxs-lookup"><span data-stu-id="6e614-102">Use the communications editor</span></span>

<span data-ttu-id="6e614-103">Wenn Sie den Inhalt Ihres Portalinhalts, rechtliche Aufbewahrungs Benachrichtigungen und zugehörige Erinnerungen/Eskalationen definieren, können Sie den Kommunikations-Editor nutzen, um Ihre Inhalte zu formatieren und dynamisch anzupassen.</span><span class="sxs-lookup"><span data-stu-id="6e614-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="6e614-104">Rich-Text-Editor</span><span class="sxs-lookup"><span data-stu-id="6e614-104">Rich text editor</span></span> 

<span data-ttu-id="6e614-105">Der Kommunikations-Editor ermöglicht es dem Benutzer, den Text mithilfe der Editor-Optionen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="6e614-105">The Communications Editor allows user to customize the text using the editor options.</span></span> <span data-ttu-id="6e614-106">Benutzer können beispielsweise Schriftarten ändern, Aufzählungslisten erstellen, Inhalte hervorheben und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="6e614-106">For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="6e614-107">Feld Variablen zusammenführen</span><span class="sxs-lookup"><span data-stu-id="6e614-107">Merge field variables</span></span>

<span data-ttu-id="6e614-108">Sie können die e-Mail-Zusammenführungs Variablen aus dem Kommunikations-Editor nutzen, um angepasste Depot Attribute in den Textkörper einer Kommunikation einzubetten.</span><span class="sxs-lookup"><span data-stu-id="6e614-108">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text.</span></span> <span data-ttu-id="6e614-109">Bei der Übermittlung an die Depotbank wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6e614-109">When sent to the custodian, the merge field will be populated with the corresponding field.</span></span> <span data-ttu-id="6e614-110">Wenn Sie beispielsweise an Depotbank John Smith gesendet haben, würde das Seriendruckfeld [Depot Name] mit dem entsprechenden Namen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="6e614-110">For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="6e614-111">Sie können e-Mail-Seriendruckfelder verwenden, indem Sie die Symbole für das **Seriendruckfeld** oben im Rich-Text-Editor-Steuerelement auswählen.</span><span class="sxs-lookup"><span data-stu-id="6e614-111">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control.</span></span> <span data-ttu-id="6e614-112">Der Platzhalter wird basierend auf dem Speicherort des Cursors der Benutzer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6e614-112">The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="6e614-113">Liste der Seriendruckfeld Variablen</span><span class="sxs-lookup"><span data-stu-id="6e614-113">List of merge field variables</span></span>

| <span data-ttu-id="6e614-114">Feldname</span><span class="sxs-lookup"><span data-stu-id="6e614-114">Field name</span></span>                  | <span data-ttu-id="6e614-115">Feld Details</span><span class="sxs-lookup"><span data-stu-id="6e614-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="6e614-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="6e614-116">Display Name</span></span>  | <span data-ttu-id="6e614-117">Der vor-und Nachname der Depotbank.</span><span class="sxs-lookup"><span data-stu-id="6e614-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="6e614-118">Bestätigungs Link</span><span class="sxs-lookup"><span data-stu-id="6e614-118">Acknowledgement Link</span></span> | <span data-ttu-id="6e614-119">Ein benutzerdefinierter Link zum Aufzeichnen der Bestätigung der einzelnen depotverwalter.</span><span class="sxs-lookup"><span data-stu-id="6e614-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="6e614-120">Portal Link</span><span class="sxs-lookup"><span data-stu-id="6e614-120">Portal Link</span></span>     | <span data-ttu-id="6e614-121">Ein angepasster Link für das Compliance-Portal des Depotbank.</span><span class="sxs-lookup"><span data-stu-id="6e614-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="6e614-122">AusStellende Offizier</span><span class="sxs-lookup"><span data-stu-id="6e614-122">Issuing Officer</span></span>                   | <span data-ttu-id="6e614-123">Die e-Mail-Adresse des angegebenen ausstellenden Offiziers.</span><span class="sxs-lookup"><span data-stu-id="6e614-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="6e614-124">AusStellendes Datum</span><span class="sxs-lookup"><span data-stu-id="6e614-124">Issuing Date</span></span>                   | <span data-ttu-id="6e614-125">Das Datum, an dem der Hinweis ausgegeben wurde (UTC).</span><span class="sxs-lookup"><span data-stu-id="6e614-125">The date that the notice was issued (UTC).</span></span>              |
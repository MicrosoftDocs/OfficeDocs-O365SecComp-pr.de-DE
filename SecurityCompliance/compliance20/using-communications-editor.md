---
title: Verwenden des Editors communications
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
ms.openlocfilehash: 107f45510bcf70942c6f03bdfed0a9090f1d83c0
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607797"
---
# <a name="using-the-communications-editor"></a><span data-ttu-id="e8a90-102">Verwenden des Editors Communications</span><span class="sxs-lookup"><span data-stu-id="e8a90-102">Using the Communications Editor</span></span>
<span data-ttu-id="e8a90-103">Wie Sie den Inhalt Ihrer Portalinhalt definieren, Legal halten, Benachrichtigungen und Erinnerungen/Eskalationen Verwandte, und Sie können den Communications-Editor, formatieren und dynamisch anpassen Ihrer Inhalte nutzen.</span><span class="sxs-lookup"><span data-stu-id="e8a90-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="e8a90-104">Rich-Text-Editor</span><span class="sxs-lookup"><span data-stu-id="e8a90-104">Rich-Text Editor</span></span> 

<span data-ttu-id="e8a90-p101">Der Communications-Editor können Benutzer zum Anpassen des Texts mithilfe der Editoroptionen. Benutzer können beispielsweise Schriftarttypen ändern, Erstellen von Listen mit Aufzählungszeichen, Hervorheben Inhalts- und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="e8a90-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

<<include screenshot>>

## <a name="merge-field-variables"></a><span data-ttu-id="e8a90-107">Zusammenführen von Feldvariablen</span><span class="sxs-lookup"><span data-stu-id="e8a90-107">Merge Field Variables</span></span>

<span data-ttu-id="e8a90-p102">Sie können e-Mail-Zusammenführung Variablen aus dem Communications-Editor angepassten Verwaltungsberechtigter Attribute in Textkörper eine Mitteilung einbetten nutzen. Wenn an der Verwaltungsberechtigte gesendet wird, wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt werden. Beispielsweise würde beim an Verwaltungsberechtigter John Smith gesendet, das Seriendruckfeld [Verwaltungsberechtigter Name] mit dem entsprechenden Namen übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e8a90-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="e8a90-p103">E-Mail-zusammenführungsfelds können, indem Sie die Symbole **Seriendruckfeld** am oberen Rand der Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird je deaktiviert den Speicherort der Cursor des Benutzers hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e8a90-p103">You can use email merge fields by selecting the **Merge Field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="e8a90-113">Liste der Merge Feldvariablen</span><span class="sxs-lookup"><span data-stu-id="e8a90-113">List of Merge Field Variables</span></span>
| <span data-ttu-id="e8a90-114">Name des Felds</span><span class="sxs-lookup"><span data-stu-id="e8a90-114">Field Name</span></span>                  | <span data-ttu-id="e8a90-115">Feld-Details</span><span class="sxs-lookup"><span data-stu-id="e8a90-115">Field Details</span></span> | 
| :------------------- | :-------------------: |
| <span data-ttu-id="e8a90-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="e8a90-116">Display Name</span></span>  | <span data-ttu-id="e8a90-117">Verwaltungsberechtigter vor- und Nachname</span><span class="sxs-lookup"><span data-stu-id="e8a90-117">Custodian's first and last name</span></span> | 
| <span data-ttu-id="e8a90-118">Bestätigung Link</span><span class="sxs-lookup"><span data-stu-id="e8a90-118">Acknowledgement Link</span></span>                 | <span data-ttu-id="e8a90-119">Benutzerdefinierte Verknüpfung zu notieren Sie jeden Verwaltungsberechtigter Bestätigung</span><span class="sxs-lookup"><span data-stu-id="e8a90-119">Customized link to record each custodian's acknowledgement</span></span>                 |
| <span data-ttu-id="e8a90-120">Portal-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="e8a90-120">Portal Link</span></span>     | <span data-ttu-id="e8a90-121">Benutzerdefinierte Verknüpfung für der Verwaltungsberechtigte Compliance-Portal</span><span class="sxs-lookup"><span data-stu-id="e8a90-121">Customized link for the custodian's Compliance Portal</span></span>                 |
| <span data-ttu-id="e8a90-122">Ausstellen Officer</span><span class="sxs-lookup"><span data-stu-id="e8a90-122">Issuing Officer</span></span>                   | <span data-ttu-id="e8a90-123">E-Mail-Adresse von der angegebenen ausstellenden officer</span><span class="sxs-lookup"><span data-stu-id="e8a90-123">Email address of the specified issuing officer</span></span>                   |
| <span data-ttu-id="e8a90-124">Ausstellen von Datum</span><span class="sxs-lookup"><span data-stu-id="e8a90-124">Issuing Date</span></span>                   | <span data-ttu-id="e8a90-125">Datum, an dem die Anmerkung (UTC) ausgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="e8a90-125">date that the notice was issued (UTC)</span></span>              |
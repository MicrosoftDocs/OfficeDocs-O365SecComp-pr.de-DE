---
title: Einrichten der Rechtsanwalt-Client-Berechtigungs Erkennung in Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835065"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="01cc8-102">Einrichten der Anwalts-Client-Berechtigungs Erkennung (Preview) in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="01cc8-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="01cc8-103">Ein wichtiger und kostspieliger Aspekt bei der Überprüfung eines beliebigen Ermittlungsprozesses ist die Überprüfung für privilegierte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="01cc8-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="01cc8-104">Advanced eDiscovery bietet eine AI-basierte Erkennung von privilegierten Inhalten in Ihrem Fall, damit Sie diesen Prozess effizienter gestalten können.</span><span class="sxs-lookup"><span data-stu-id="01cc8-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="01cc8-105">Da sich diese Funktion derzeit in der Betaphase befindet, muss ein eDiscovery-Administrator sich für die Funktion für die Verwendung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="01cc8-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="01cc8-106">Wie funktioniert dies?</span><span class="sxs-lookup"><span data-stu-id="01cc8-106">How does it work?</span></span>

<span data-ttu-id="01cc8-107">Wenn die Funktion aktiviert ist und Sie einen Überprüfungs Satz in einem Fall analysieren, werden alle Dokumente über das Anwalts-Client-Berechtigungs Erkennungs Modell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01cc8-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="01cc8-108">Das Modell sieht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="01cc8-108">The model looks at two things:</span></span>

- <span data-ttu-id="01cc8-109">Inhalt: das ml-Modell bestimmt die Wahrscheinlichkeit, dass der Inhalt des Dokuments legal ist.</span><span class="sxs-lookup"><span data-stu-id="01cc8-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="01cc8-110">Teilnehmer: Wenn eine Liste mit vom Benutzer hochgeladenen Anwälten für den Mandanten vorhanden ist, vergleicht das Modell die Teilnehmer des Dokuments mit der Liste, um zu bestimmen, ob das Dokument mindestens einen Anwalts Teilnehmer hat.</span><span class="sxs-lookup"><span data-stu-id="01cc8-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="01cc8-111">Das Modell gibt drei Werte für jedes Dokument aus, die alle in einem Übersichts Satz durchsuchbar sind:</span><span class="sxs-lookup"><span data-stu-id="01cc8-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="01cc8-112">Inhaltsbewertung: die Wahrscheinlichkeit, dass das Dokument rechtsverbindlich ist (Ergebnis zwischen 0 und 1)</span><span class="sxs-lookup"><span data-stu-id="01cc8-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="01cc8-113">Hat Anwalt: true, wenn einer der Teilnehmer in der hochgeladenen anwaltsliste gefunden wird, andernfalls false, oder wenn es keine anwaltsliste gibt.</span><span class="sxs-lookup"><span data-stu-id="01cc8-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="01cc8-114">Potenziell privileged: true, wenn die Inhaltsbewertung über dem Schwellenwert liegt oder ein Rechtsanwalts Teilnehmer ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="01cc8-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="01cc8-115">Opting-in-Client-Berechtigungs Erkennung</span><span class="sxs-lookup"><span data-stu-id="01cc8-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="01cc8-116">Schritt 1: Opt-in-Client-Berechtigungs Erkennung (eDiscovery-Administrator)</span><span class="sxs-lookup"><span data-stu-id="01cc8-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="01cc8-117">Da die Erkennung von Anwalts-und Client Rechten eine Vorschaufunktion ist, muss der eDiscovery-Administrator sich anmelden, um die Funktion in ihren Fällen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="01cc8-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="01cc8-118">Wechseln Sie zu "Konfigurieren von experimentellen Features" auf der Seite Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="01cc8-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="01cc8-119">Klicken Sie auf "Attorney-Client-Berechtigungs Erkennung verwalten".</span><span class="sxs-lookup"><span data-stu-id="01cc8-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="01cc8-120">Klicken Sie auf die Umschaltfläche, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="01cc8-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="01cc8-121">Schritt 2: Hochladen einer Liste von Anwälten (optional)</span><span class="sxs-lookup"><span data-stu-id="01cc8-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="01cc8-122">Zur vollständigen Nutzung der Rechtsanwalts-Client-Berechtigungs Erkennung empfehlen wir die Bereitstellung einer Liste von e-Mail-Adressen Juristen oder juristische Personen, die für das Unternehmen tätig sind.</span><span class="sxs-lookup"><span data-stu-id="01cc8-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="01cc8-123">Bei der Liste muss es sich um eine Kopfzeilen lose CSV-Datei mit einer e-Mail-Adresse pro Zeile handeln.</span><span class="sxs-lookup"><span data-stu-id="01cc8-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="01cc8-124">Nutzen der Anwalts-Client-Berechtigungs Erkennung</span><span class="sxs-lookup"><span data-stu-id="01cc8-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="01cc8-125">Schritt 1: Analysieren eines Übersichts Satzes</span><span class="sxs-lookup"><span data-stu-id="01cc8-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="01cc8-126">Wenn Sie Ihren Überprüfungs Satz analysieren, wird auch die Erkennung von Anwalts-und Client Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01cc8-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="01cc8-127">Weitere Informationen zum Analysieren von Daten im Übersichts Satz finden Sie unter [analyze Data in a Review Set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="01cc8-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="01cc8-128">Schritt 2: Erstellen einer smarttaggruppe mit Attorney-Client-Berechtigungs Erkennungs Modell</span><span class="sxs-lookup"><span data-stu-id="01cc8-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="01cc8-129">Eine der Hauptmethoden zum Nutzen der Ergebnisse der Erkennung von Anwalts-Client-Berechtigungen in Ihrem Überprüfungsprozess ist die Verwendung einer smarttaggruppe.</span><span class="sxs-lookup"><span data-stu-id="01cc8-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="01cc8-130">Smarttaggruppen nehmen die Ergebnisse eines ml-Modells und zeigen die Ergebnisse des Modells Inline neben den Tags an, sodass Sie die Ergebnisse des Modells gegebenenfalls problemlos nutzen können, und verwenden Sie die Tags im Übersichts Prozess wie alle anderen Tags in Ihrem Tag-Panel.</span><span class="sxs-lookup"><span data-stu-id="01cc8-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span>

- <span data-ttu-id="01cc8-131">Klicken Sie unter "Tags verwalten" auf "Smarttagbereich hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="01cc8-131">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="01cc8-132">Wählen Sie "Attorney-Client-Berechtigungs Erkennung" aus.</span><span class="sxs-lookup"><span data-stu-id="01cc8-132">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="01cc8-133">Sie werden feststellen, dass eine Transpondergruppe und zwei Tags, die den möglichen Ergebnissen des Modells entsprechen, erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="01cc8-133">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="01cc8-134">Benennen Sie die Transpondergruppe und die Tags so um, wie Sie für Ihre Überprüfungen geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="01cc8-134">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="01cc8-135">Schritt 3: Verwenden der smarttaggruppe für die Überprüfungen von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="01cc8-135">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="01cc8-136">Wenn Sie ein Dokument überprüfen, wenn das Modell bestimmt hat, dass das Dokument potenziell privilegiert ist, wird das entsprechende Smarttag das ergebnisoffen legen:</span><span class="sxs-lookup"><span data-stu-id="01cc8-136">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="01cc8-137">Wenn das Dokumentinhalte enthält, die möglicherweise rechtlich zulässig sind, wird neben dem entsprechenden Smarttag eine Bezeichnung für rechtliche Inhalte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01cc8-137">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="01cc8-138">Wenn das Dokument einen Teilnehmer hat, der in der Liste der hochgeladenen Anwälte gefunden wird, wird neben dem entsprechenden Smarttag eine "Anwalts Bezeichnung" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01cc8-138">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>
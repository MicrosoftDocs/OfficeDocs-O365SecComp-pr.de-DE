---
title: Einrichten der Erkennung von Anwalts Mandanten-Berechtigungen in Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
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
ms.openlocfilehash: ee5f2257e73467c50a0ecc296d8d3b70b7c3d0f8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155187"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="a074c-102">Einrichten der Anwalts-Client-Berechtigungs Erkennung (Preview) in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a074c-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="a074c-103">Ein wichtiger und kostspieliger Aspekt des Überprüfungs Bereichs eines beliebigen Ermittlungsprozesses ist die Überprüfung auf privilegierte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="a074c-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="a074c-104">Advanced eDiscovery bietet eine AI-basierte Erkennung von privilegierten Inhalten in Ihrem Fall, sodass Sie diesen Prozess effizienter gestalten können.</span><span class="sxs-lookup"><span data-stu-id="a074c-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="a074c-105">Da sich dieses Feature derzeit in der Betaphase befindet, muss ein eDiscovery-Administrator das Feature für die Verwendung auswählen.</span><span class="sxs-lookup"><span data-stu-id="a074c-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="a074c-106">Wie funktioniert dies?</span><span class="sxs-lookup"><span data-stu-id="a074c-106">How does it work?</span></span>

<span data-ttu-id="a074c-107">Wenn das Feature aktiviert ist und Sie einen Überprüfungs Sätze in einem Fall analysieren, werden alle Dokumente über das Erkennungs Modell für das Anwalts Client-Recht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a074c-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="a074c-108">Das Modell sieht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="a074c-108">The model looks at two things:</span></span>

- <span data-ttu-id="a074c-109">Inhalt: das ml-Modell bestimmt die Wahrscheinlichkeit, dass der Inhalt des Dokuments legal in der Natur ist.</span><span class="sxs-lookup"><span data-stu-id="a074c-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="a074c-110">Teilnehmer: Wenn es eine vom Benutzer hochgeladene anwaltsliste für den Mandanten gibt, vergleicht das Modell die Teilnehmer des Dokuments mit der Liste, um zu bestimmen, ob das Dokument mindestens einen Anwalts Teilnehmer hat.</span><span class="sxs-lookup"><span data-stu-id="a074c-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="a074c-111">Das Modell gibt drei Werte für jedes Dokument aus, die alle innerhalb eines Überprüfungs Satzes durchsuchbar sind:</span><span class="sxs-lookup"><span data-stu-id="a074c-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="a074c-112">Inhaltsbewertung: die Wahrscheinlichkeit, dass das Dokument rechtsverbindlich ist (Bewertung zwischen 0 und 1)</span><span class="sxs-lookup"><span data-stu-id="a074c-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="a074c-113">Hat Anwalt: true, wenn einer der Teilnehmer in der hochgeladenen anwaltsliste gefunden wird, andernfalls false, oder wenn es keine anwaltsliste gibt.</span><span class="sxs-lookup"><span data-stu-id="a074c-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="a074c-114">Potenziell privilegiert: true, wenn das Inhalts Ergebnis über dem Schwellenwert liegt oder ein Rechtsanwalts Teilnehmer ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="a074c-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="a074c-115">Entscheidung für die Erkennung von Anwalts-Client-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a074c-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="a074c-116">Schritt 1: Opt in Attorney-Client Privilege Detection (eDiscovery admin)</span><span class="sxs-lookup"><span data-stu-id="a074c-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="a074c-117">Da die Erkennung von Anwalts Mandanten-Berechtigungen eine Vorschaufunktion ist, muss Ihr eDiscovery-Administrator sich dafür entscheiden, das Feature in ihren Fällen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="a074c-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="a074c-118">Wechseln Sie zu "Konfigurieren von experimentellen Features" von der erweiterten eDiscovery-Seite</span><span class="sxs-lookup"><span data-stu-id="a074c-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="a074c-119">Klicken Sie auf "Verwalten der Anwalts-Client-Berechtigungs Erkennung".</span><span class="sxs-lookup"><span data-stu-id="a074c-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="a074c-120">Klicken Sie auf die Umschaltfläche, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a074c-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="a074c-121">Schritt 2: Hochladen einer Liste von Anwälten (optional)</span><span class="sxs-lookup"><span data-stu-id="a074c-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="a074c-122">Um die Erkennung von Anwalts-Client-Berechtigungen in vollem Umfang nutzen zu können, wird empfohlen, eine Liste von e-Mail-Adressen für Anwälte oder juristische Personen, die für das Unternehmen arbeiten, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a074c-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="a074c-123">Die Liste sollte eine Kopfzeilen lose CSV-Datei mit einer e-Mail-Adresse pro Zeile sein.</span><span class="sxs-lookup"><span data-stu-id="a074c-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="a074c-124">Nutzung der Erkennung von Anwalts-Client-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a074c-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="a074c-125">Schritt 1: Analysieren eines Überprüfungs Satzes</span><span class="sxs-lookup"><span data-stu-id="a074c-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="a074c-126">Wenn Sie den Überprüfungs analysieren, wird auch die Erkennung von Anwalts-und Client Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a074c-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="a074c-127">Weitere Informationen zum Analysieren von Daten in der Überprüfungsgruppe finden Sie unter [Analysieren von Daten in einer Überprüfungsgruppe in Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="a074c-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="a074c-128">Schritt 2: Erstellen einer smarttaggruppe mit dem Anwalt-Client-Berechtigungs Erkennungs Modell</span><span class="sxs-lookup"><span data-stu-id="a074c-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="a074c-129">Eine der wichtigsten Methoden, um die Ergebnisse der Anwalts-Client-Berechtigungs Erkennung in Ihrem Überprüfungsprozess zu nutzen, ist die Verwendung einer smarttaggruppe.</span><span class="sxs-lookup"><span data-stu-id="a074c-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="a074c-130">Smarttaggruppen nehmen die Ergebnisse eines ml-Modells an und zeigen die Ergebnisse des Modells Inline neben den Tags an, sodass Sie die Ergebnisse des Modells auf einfache Weise nutzen können, und verwenden Sie die Tags in Ihrem Überprüfungsprozess wie andere Tags in Ihrem taggingbereich.</span><span class="sxs-lookup"><span data-stu-id="a074c-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span> <span data-ttu-id="a074c-131">Weitere Informationen finden Sie unter [Einrichten von Smarttags für ml-Assisted Review in Advanced eDiscovery](smart-tags.md) .</span><span class="sxs-lookup"><span data-stu-id="a074c-131">Please refer to [Set up smart tags for ML-assisted review in Advanced eDiscovery](smart-tags.md) for more information.</span></span>

- <span data-ttu-id="a074c-132">Klicken Sie in "Tags verwalten" auf "Smarttag-Abschnitt hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="a074c-132">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="a074c-133">Wählen Sie "Anwalts Kunde-Berechtigungs Erkennung" aus.</span><span class="sxs-lookup"><span data-stu-id="a074c-133">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="a074c-134">Sie werden sehen, dass eine Tag-Gruppe und zwei Tags entsprechend den möglichen Ergebnissen des Modells erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a074c-134">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="a074c-135">Benennen Sie die Tag-Gruppe und die-Tags so um, dass Sie für Ihre Überprüfung geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="a074c-135">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="a074c-136">Schritt 3: Verwenden Sie die Smarttag-Gruppe für die Überprüfung von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a074c-136">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="a074c-137">Wenn Sie ein Dokument überprüfen, wenn das Modell festgestellt hat, dass das Dokument möglicherweise privilegiert ist, wird das entsprechende Smarttag das Ergebnis verfügbar machen:</span><span class="sxs-lookup"><span data-stu-id="a074c-137">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="a074c-138">Wenn das Dokumentinhalte enthält, die möglicherweise legal sind, wird neben dem entsprechenden Smarttag eine Bezeichnung "legaler Inhalt" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a074c-138">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="a074c-139">Wenn das Dokument über einen Teilnehmer verfügt, der in der Liste der hochgeladenen Rechtsanwälte gefunden wird, wird neben dem entsprechenden Smarttag eine "Anwalts Bezeichnung" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a074c-139">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>
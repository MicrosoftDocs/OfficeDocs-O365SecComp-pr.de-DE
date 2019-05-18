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
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a>Einrichten der Anwalts-Client-Berechtigungs Erkennung (Preview) in Advanced eDiscovery

Ein wichtiger und kostspieliger Aspekt des Überprüfungs Bereichs eines beliebigen Ermittlungsprozesses ist die Überprüfung auf privilegierte Inhalte. Advanced eDiscovery bietet eine AI-basierte Erkennung von privilegierten Inhalten in Ihrem Fall, sodass Sie diesen Prozess effizienter gestalten können. Da sich dieses Feature derzeit in der Betaphase befindet, muss ein eDiscovery-Administrator das Feature für die Verwendung auswählen.

## <a name="how-does-it-work"></a>Wie funktioniert dies?

Wenn das Feature aktiviert ist und Sie einen Überprüfungs Sätze in einem Fall analysieren, werden alle Dokumente über das Erkennungs Modell für das Anwalts Client-Recht ausgeführt. Das Modell sieht zwei Dinge:

- Inhalt: das ml-Modell bestimmt die Wahrscheinlichkeit, dass der Inhalt des Dokuments legal in der Natur ist.

- Teilnehmer: Wenn es eine vom Benutzer hochgeladene anwaltsliste für den Mandanten gibt, vergleicht das Modell die Teilnehmer des Dokuments mit der Liste, um zu bestimmen, ob das Dokument mindestens einen Anwalts Teilnehmer hat.
Das Modell gibt drei Werte für jedes Dokument aus, die alle innerhalb eines Überprüfungs Satzes durchsuchbar sind:

- Inhaltsbewertung: die Wahrscheinlichkeit, dass das Dokument rechtsverbindlich ist (Bewertung zwischen 0 und 1)

- Hat Anwalt: true, wenn einer der Teilnehmer in der hochgeladenen anwaltsliste gefunden wird, andernfalls false, oder wenn es keine anwaltsliste gibt.

-  Potenziell privilegiert: true, wenn das Inhalts Ergebnis über dem Schwellenwert liegt oder ein Rechtsanwalts Teilnehmer ist, andernfalls false.

## <a name="opting-into-attorney-client-privilege-detection"></a>Entscheidung für die Erkennung von Anwalts-Client-Berechtigungen

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a>Schritt 1: Opt in Attorney-Client Privilege Detection (eDiscovery admin)

Da die Erkennung von Anwalts Mandanten-Berechtigungen eine Vorschaufunktion ist, muss Ihr eDiscovery-Administrator sich dafür entscheiden, das Feature in ihren Fällen verfügbar zu machen.

- Wechseln Sie zu "Konfigurieren von experimentellen Features" von der erweiterten eDiscovery-Seite

- Klicken Sie auf "Verwalten der Anwalts-Client-Berechtigungs Erkennung".

- Klicken Sie auf die Umschaltfläche, um das Feature zu aktivieren.

### <a name="step-2-upload-a-list-of-attorneys-optional"></a>Schritt 2: Hochladen einer Liste von Anwälten (optional)

Um die Erkennung von Anwalts-Client-Berechtigungen in vollem Umfang nutzen zu können, wird empfohlen, eine Liste von e-Mail-Adressen für Anwälte oder juristische Personen, die für das Unternehmen arbeiten, bereitzustellen. Die Liste sollte eine Kopfzeilen lose CSV-Datei mit einer e-Mail-Adresse pro Zeile sein.

## <a name="leveraging-attorney-client-privilege-detection"></a>Nutzung der Erkennung von Anwalts-Client-Berechtigungen 

### <a name="step-1-analyze-a-review-set"></a>Schritt 1: Analysieren eines Überprüfungs Satzes

Wenn Sie den Überprüfungs analysieren, wird auch die Erkennung von Anwalts-und Client Rechten ausgeführt. Weitere Informationen zum Analysieren von Daten in der Überprüfungsgruppe finden Sie unter [Analysieren von Daten in einer Überprüfungsgruppe in Advanced eDiscovery](analyzing-data-in-review-set.md).

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a>Schritt 2: Erstellen einer smarttaggruppe mit dem Anwalt-Client-Berechtigungs Erkennungs Modell

Eine der wichtigsten Methoden, um die Ergebnisse der Anwalts-Client-Berechtigungs Erkennung in Ihrem Überprüfungsprozess zu nutzen, ist die Verwendung einer smarttaggruppe. Smarttaggruppen nehmen die Ergebnisse eines ml-Modells an und zeigen die Ergebnisse des Modells Inline neben den Tags an, sodass Sie die Ergebnisse des Modells auf einfache Weise nutzen können, und verwenden Sie die Tags in Ihrem Überprüfungsprozess wie andere Tags in Ihrem taggingbereich. Weitere Informationen finden Sie unter [Einrichten von Smarttags für ml-Assisted Review in Advanced eDiscovery](smart-tags.md) .

- Klicken Sie in "Tags verwalten" auf "Smarttag-Abschnitt hinzufügen".

- Wählen Sie "Anwalts Kunde-Berechtigungs Erkennung" aus. Sie werden sehen, dass eine Tag-Gruppe und zwei Tags entsprechend den möglichen Ergebnissen des Modells erstellt wurden.

- Benennen Sie die Tag-Gruppe und die-Tags so um, dass Sie für Ihre Überprüfung geeignet sind.

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a>Schritt 3: Verwenden Sie die Smarttag-Gruppe für die Überprüfung von Berechtigungen

Wenn Sie ein Dokument überprüfen, wenn das Modell festgestellt hat, dass das Dokument möglicherweise privilegiert ist, wird das entsprechende Smarttag das Ergebnis verfügbar machen:

- Wenn das Dokumentinhalte enthält, die möglicherweise legal sind, wird neben dem entsprechenden Smarttag eine Bezeichnung "legaler Inhalt" angezeigt.

- Wenn das Dokument über einen Teilnehmer verfügt, der in der Liste der hochgeladenen Rechtsanwälte gefunden wird, wird neben dem entsprechenden Smarttag eine "Anwalts Bezeichnung" angezeigt.
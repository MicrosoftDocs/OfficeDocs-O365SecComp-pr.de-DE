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
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a>Einrichten der Anwalts-Client-Berechtigungs Erkennung (Preview) in Advanced eDiscovery

Ein wichtiger und kostspieliger Aspekt bei der Überprüfung eines beliebigen Ermittlungsprozesses ist die Überprüfung für privilegierte Inhalte. Advanced eDiscovery bietet eine AI-basierte Erkennung von privilegierten Inhalten in Ihrem Fall, damit Sie diesen Prozess effizienter gestalten können. Da sich diese Funktion derzeit in der Betaphase befindet, muss ein eDiscovery-Administrator sich für die Funktion für die Verwendung entscheiden.

## <a name="how-does-it-work"></a>Wie funktioniert dies?

Wenn die Funktion aktiviert ist und Sie einen Überprüfungs Satz in einem Fall analysieren, werden alle Dokumente über das Anwalts-Client-Berechtigungs Erkennungs Modell ausgeführt. Das Modell sieht zwei Dinge:

- Inhalt: das ml-Modell bestimmt die Wahrscheinlichkeit, dass der Inhalt des Dokuments legal ist.

- Teilnehmer: Wenn eine Liste mit vom Benutzer hochgeladenen Anwälten für den Mandanten vorhanden ist, vergleicht das Modell die Teilnehmer des Dokuments mit der Liste, um zu bestimmen, ob das Dokument mindestens einen Anwalts Teilnehmer hat.
Das Modell gibt drei Werte für jedes Dokument aus, die alle in einem Übersichts Satz durchsuchbar sind:

- Inhaltsbewertung: die Wahrscheinlichkeit, dass das Dokument rechtsverbindlich ist (Ergebnis zwischen 0 und 1)

- Hat Anwalt: true, wenn einer der Teilnehmer in der hochgeladenen anwaltsliste gefunden wird, andernfalls false, oder wenn es keine anwaltsliste gibt.

-  Potenziell privileged: true, wenn die Inhaltsbewertung über dem Schwellenwert liegt oder ein Rechtsanwalts Teilnehmer ist, andernfalls false.

## <a name="opting-into-attorney-client-privilege-detection"></a>Opting-in-Client-Berechtigungs Erkennung

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a>Schritt 1: Opt-in-Client-Berechtigungs Erkennung (eDiscovery-Administrator)

Da die Erkennung von Anwalts-und Client Rechten eine Vorschaufunktion ist, muss der eDiscovery-Administrator sich anmelden, um die Funktion in ihren Fällen zur Verfügung zu stellen.

- Wechseln Sie zu "Konfigurieren von experimentellen Features" auf der Seite Advanced eDiscovery.

- Klicken Sie auf "Attorney-Client-Berechtigungs Erkennung verwalten".

- Klicken Sie auf die Umschaltfläche, um das Feature zu aktivieren.

### <a name="step-2-upload-a-list-of-attorneys-optional"></a>Schritt 2: Hochladen einer Liste von Anwälten (optional)

Zur vollständigen Nutzung der Rechtsanwalts-Client-Berechtigungs Erkennung empfehlen wir die Bereitstellung einer Liste von e-Mail-Adressen Juristen oder juristische Personen, die für das Unternehmen tätig sind. Bei der Liste muss es sich um eine Kopfzeilen lose CSV-Datei mit einer e-Mail-Adresse pro Zeile handeln.

## <a name="leveraging-attorney-client-privilege-detection"></a>Nutzen der Anwalts-Client-Berechtigungs Erkennung 

### <a name="step-1-analyze-a-review-set"></a>Schritt 1: Analysieren eines Übersichts Satzes

Wenn Sie Ihren Überprüfungs Satz analysieren, wird auch die Erkennung von Anwalts-und Client Rechten ausgeführt. Weitere Informationen zum Analysieren von Daten im Übersichts Satz finden Sie unter [analyze Data in a Review Set in Advanced eDiscovery](analyzing-data-in-review-set.md).

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a>Schritt 2: Erstellen einer smarttaggruppe mit Attorney-Client-Berechtigungs Erkennungs Modell

Eine der Hauptmethoden zum Nutzen der Ergebnisse der Erkennung von Anwalts-Client-Berechtigungen in Ihrem Überprüfungsprozess ist die Verwendung einer smarttaggruppe. Smarttaggruppen nehmen die Ergebnisse eines ml-Modells und zeigen die Ergebnisse des Modells Inline neben den Tags an, sodass Sie die Ergebnisse des Modells gegebenenfalls problemlos nutzen können, und verwenden Sie die Tags im Übersichts Prozess wie alle anderen Tags in Ihrem Tag-Panel.

- Klicken Sie unter "Tags verwalten" auf "Smarttagbereich hinzufügen".

- Wählen Sie "Attorney-Client-Berechtigungs Erkennung" aus. Sie werden feststellen, dass eine Transpondergruppe und zwei Tags, die den möglichen Ergebnissen des Modells entsprechen, erstellt wurden.

- Benennen Sie die Transpondergruppe und die Tags so um, wie Sie für Ihre Überprüfungen geeignet sind.

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a>Schritt 3: Verwenden der smarttaggruppe für die Überprüfungen von Berechtigungen

Wenn Sie ein Dokument überprüfen, wenn das Modell bestimmt hat, dass das Dokument potenziell privilegiert ist, wird das entsprechende Smarttag das ergebnisoffen legen:

- Wenn das Dokumentinhalte enthält, die möglicherweise rechtlich zulässig sind, wird neben dem entsprechenden Smarttag eine Bezeichnung für rechtliche Inhalte angezeigt.

- Wenn das Dokument einen Teilnehmer hat, der in der Liste der hochgeladenen Anwälte gefunden wird, wird neben dem entsprechenden Smarttag eine "Anwalts Bezeichnung" angezeigt.
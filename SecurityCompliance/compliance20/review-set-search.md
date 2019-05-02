---
title: Abfragen der Daten in einem Übersichts Satz
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
ms.openlocfilehash: 395cc01238f4dbc91de5dd652e10121f5e0cc926
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527174"
---
# <a name="query-the-data-in-a-review-set"></a>Abfragen der Daten in einem Übersichts Satz

In den meisten Fällen ist es hilfreich, tiefer in die in einem Übersichts Satz zu überprüfenden Inhalte einzudringen und diese effizienter zu überarbeiten. Mithilfe von Abfragen in einem Übersichts Satz können Sie sich auf eine Teilmenge von Dokumenten konzentrieren, die den von Ihnen festgelegten Kriterien entsprechen.

## <a name="creating-and-running-a-query-within-a-review-set"></a>Erstellen und Durchführen einer Abfrage in einem Übersichts Satz

Klicken Sie im Übersichts Satz auf "neue Abfrage", um eine Abfrage in Ihrem Übersichts Satz zu erstellen und auszuführen. Nachdem Sie die Abfrage benannt und die Bedingungen definiert haben, klicken Sie auf "Speichern", um die Abfrage auszuführen. Klicken Sie zum Ausführen einer zuvor gespeicherten Abfrage einfach auf die gespeicherte Abfrage. Eine Liste der Metadaten, nach denen Sie suchen können, finden Sie unter [Document Metadata fields](document-metadata-fields.md) .

## <a name="building-your-query"></a>Erstellen der Abfrage

Sie können Ihre Abfrage mit einer Kombination aus Bedingungs Karten und Abfragesprache in der Bedingungs Karte für Schlüsselwörter erstellen. Sie können Bedingungs Karten als Block gruppieren, um eine komplexere Abfrage zu gestalten.

### <a name="condition-card"></a>Bedingungs Karte

Jedes durchsuchbare Feld in einem Übersichts Satz verfügt über eine entsprechende Konditions Karte, die Sie zum Erstellen der Abfrage verwenden können.

Es gibt mehrere Arten von Bedingungs Karten:
- FREETEXT: FREETEXT-Bedingungs Karte wird für Textfelder wie Subject verwendet. Sie können mehrere Suchbegriffe auflisten, indem Sie Sie mit einem Komma voneinander trennen.
- Datum: die Bedingungs Karte für das Datum wird für Datumsfelder wie Datum der letzten Änderung verwendet.
- Suchoptionen: die Bedingungs Karte für Suchoptionen enthält eine Liste der möglichen Werte für das jeweilige Feld in Ihrem Übersichts Satz. Dieser Wert wird für Felder wie "Sender" verwendet, bei denen eine begrenzte Anzahl von möglichen Werten in Ihrem Übersichts Satz vorhanden ist.
- Stichwort: Stichwort Bedingungs Karte ist eine bestimmte Instanz von FREETEXT-Bedingungs Karte, die Sie für die Suche nach Begriffen verwenden können, oder verwenden Sie die KQL-ähnliche Abfragesprache in. Weitere Informationen finden Sie weiter unten.

### <a name="query-language"></a>Abfragesprache

Zusätzlich zu den Bedingungs Karten können Sie eine KQL-ähnliche Abfragesprache in der Stichwörter Karte verwenden, um Ihre Abfrage zu gestalten. Die Abfragesprache unterstützt die standardmäßige KQL-Syntax wie and, or, Not und Near (n). Außerdem werden Platzhalter mit einem Zeichen (?) und Platzhalter mit mehreren Zeichen (*) unterstützt.

## <a name="filter"></a>Filter

Zusätzlich zu den Abfragen, die Sie speichern können, können Sie mithilfe von Filtern zusätzliche Bedingungen direkt an die Abfrageergebnisse überlagern. Filter unterscheiden sich von Abfragen in einigen wichtigen Bereichen:
- Filter sind vorübergehend (d. h., Sie werden nicht über verschiedene Sitzungen beibehalten), während Abfragen im Übersichts Satz gespeichert werden.
- Filter sind immer Additiv; Filter gelten im oberen Bereich der Abfrage, die Sie derzeit anwenden, wohingegen durch das Anwenden einer Abfrage die Abfrage wirksam ersetzt wird.
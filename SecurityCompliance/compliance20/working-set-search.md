---
title: Abfragen der Daten in einem Arbeitssatz
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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454987"
---
# <a name="query-the-data-in-a-working-set"></a>Abfragen der Daten in einem Arbeitssatz

In den meisten Fällen ist es hilfreich, tiefer in die in einem Workingset enthaltenen Elemente einzudringen und diese effizienter zu gestalten. Mit Abfragen in einem Arbeitssatz können Sie sich auf eine Teilmenge von Dokumenten konzentrieren, die den von Ihnen definierten Kriterien entsprechen.

## <a name="creating-and-running-a-query-within-a-working-set"></a>Erstellen und Durchführen einer Abfrage in einem Arbeitssatz

Klicken Sie im Arbeitsbereich auf "neue Abfrage", um eine Abfrage in Ihrem Arbeitssatz zu erstellen und auszuführen. Nachdem Sie die Abfrage benannt und die Bedingungen definiert haben, klicken Sie auf "Speichern", um die Abfrage auszuführen. Klicken Sie zum Ausführen einer zuvor gespeicherten Abfrage einfach auf die gespeicherte Abfrage. Eine Liste der Metadaten, nach denen Sie suchen können, finden Sie unter [Document Metadata fields](document-metadata-fields.md) .

## <a name="building-your-query"></a>Erstellen der Abfrage

Sie können Ihre Abfrage mit einer Kombination aus Bedingungs Karten und Abfragesprache in der Bedingungs Karte für Schlüsselwörter erstellen.

### <a name="condition-card"></a>Bedingungs Karte

Jedes durchsuchbare Feld in einem Arbeitssatz verfügt über eine entsprechende Konditions Karte, die Sie zum Erstellen der Abfrage verwenden können.

Es gibt mehrere Arten von Bedingungs Karten:
- FREETEXT: FREETEXT-Bedingungs Karte wird für Textfelder wie Subject verwendet. Sie können mehrere Suchbegriffe auflisten, indem Sie Sie mit einem Komma voneinander trennen.
- Datum: die Bedingungs Karte für das Datum wird für Datumsfelder wie Datum der letzten Änderung verwendet.
- Suchoptionen: die Bedingungs Karte für Suchoptionen enthält eine Liste der möglichen Werte für das jeweilige Feld in Ihrem Arbeitssatz. Dies wird für Felder wie "Sender" verwendet, bei denen eine begrenzte Anzahl von möglichen Werten in Ihrem Workingset vorhanden ist.
- Stichwort: Stichwort Bedingungs Karte ist eine bestimmte Instanz von FREETEXT-Bedingungs Karte, die Sie für die Suche nach Begriffen verwenden können, oder verwenden Sie die KQL-ähnliche Abfragesprache in. Weitere Informationen finden Sie weiter unten.

### <a name="query-language"></a>Abfragesprache

Zusätzlich zu den Bedingungs Karten können Sie eine KQL-ähnliche Abfragesprache in der Stichwörter Karte verwenden, um Ihre Abfrage zu gestalten. Die Abfragesprache unterstützt die standardmäßige KQL-Syntax wie AND, OR, NOT und NEAR (n). Außerdem werden Platzhalter mit einem Zeichen (?) und Platzhalter mit mehreren Zeichen (*) unterstützt.
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
# <a name="use-the-communications-editor"></a>Verwenden des Kommunikations-Editors

Wie Sie den Inhalt Ihrer Portalinhalt definieren, Legal halten, Benachrichtigungen und Erinnerungen/Eskalationen Verwandte, und Sie können den Communications-Editor, formatieren und dynamisch anpassen Ihrer Inhalte nutzen.

## <a name="rich-text-editor"></a>Rich-Text-editor 

Der Communications-Editor können Benutzer zum Anpassen des Texts mithilfe der Editoroptionen. Benutzer können beispielsweise Schriftarttypen ändern, Erstellen von Listen mit Aufzählungszeichen, Hervorheben Inhalts- und vieles mehr. 

## <a name="merge-field-variables"></a>Zusammenführen von Feldvariablen

Sie können e-Mail-Zusammenführung Variablen aus dem Communications-Editor angepassten Verwaltungsberechtigter Attribute in Textkörper eine Mitteilung einbetten nutzen. Wenn an der Verwaltungsberechtigte gesendet wird, wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt werden. Beispielsweise würde beim an Verwaltungsberechtigter John Smith gesendet, das Seriendruckfeld [Verwaltungsberechtigter Name] mit dem entsprechenden Namen übersetzt werden. 

E-Mail-zusammenführungsfelds können, indem Sie die Symbole **Seriendruckfeld** am oberen Rand der Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird je deaktiviert den Speicherort der Cursor des Benutzers hinzugefügt. 

### <a name="list-of-merge-field-variables"></a>Liste der Merge Feldvariablen

| Feldname                  | Feld-details | 
| :------------------- | :------------------- |
| Anzeigename  | Der Verwaltungsberechtigte vor- und Nachname. | 
| Bestätigung Link | Angepasste Link zu jedem Verwaltungsberechtigter Bestätigung aufzeichnen.|                 |
| Portal-Verknüpfung     | Eine benutzerdefinierte Verknüpfung für der Verwaltungsberechtigte Compliance-Portal.|                |
| Ausstellen Officer                   | Die e-Mail-Adresse von der angegebenen ausstellenden Officer.|                   |
| Ausstellen von Datum                   | Das Datum, das die Bekanntmachung (UTC) ausgestellt wurde.              |
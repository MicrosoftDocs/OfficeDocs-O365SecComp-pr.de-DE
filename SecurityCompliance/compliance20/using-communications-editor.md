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
# <a name="using-the-communications-editor"></a>Verwenden des Editors Communications
Wie Sie den Inhalt Ihrer Portalinhalt definieren, Legal halten, Benachrichtigungen und Erinnerungen/Eskalationen Verwandte, und Sie können den Communications-Editor, formatieren und dynamisch anpassen Ihrer Inhalte nutzen.

## <a name="rich-text-editor"></a>Rich-Text-Editor 

Der Communications-Editor können Benutzer zum Anpassen des Texts mithilfe der Editoroptionen. Benutzer können beispielsweise Schriftarttypen ändern, Erstellen von Listen mit Aufzählungszeichen, Hervorheben Inhalts- und vieles mehr. 

<<include screenshot>>

## <a name="merge-field-variables"></a>Zusammenführen von Feldvariablen

Sie können e-Mail-Zusammenführung Variablen aus dem Communications-Editor angepassten Verwaltungsberechtigter Attribute in Textkörper eine Mitteilung einbetten nutzen. Wenn an der Verwaltungsberechtigte gesendet wird, wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt werden. Beispielsweise würde beim an Verwaltungsberechtigter John Smith gesendet, das Seriendruckfeld [Verwaltungsberechtigter Name] mit dem entsprechenden Namen übersetzt werden. 

E-Mail-zusammenführungsfelds können, indem Sie die Symbole **Seriendruckfeld** am oberen Rand der Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird je deaktiviert den Speicherort der Cursor des Benutzers hinzugefügt. 

### <a name="list-of-merge-field-variables"></a>Liste der Merge Feldvariablen
| Name des Felds                  | Feld-Details | 
| :------------------- | :-------------------: |
| Anzeigename  | Verwaltungsberechtigter vor- und Nachname | 
| Bestätigung Link                 | Benutzerdefinierte Verknüpfung zu notieren Sie jeden Verwaltungsberechtigter Bestätigung                 |
| Portal-Verknüpfung     | Benutzerdefinierte Verknüpfung für der Verwaltungsberechtigte Compliance-Portal                 |
| Ausstellen Officer                   | E-Mail-Adresse von der angegebenen ausstellenden officer                   |
| Ausstellen von Datum                   | Datum, an dem die Anmerkung (UTC) ausgestellt wurde              |
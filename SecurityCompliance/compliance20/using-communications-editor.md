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
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30294968"
---
# <a name="use-the-communications-editor"></a>Verwenden des Kommunikations-Editors

Wenn Sie den Inhalt Ihres Portalinhalts, rechtliche Aufbewahrungs Benachrichtigungen und zugehörige Erinnerungen/Eskalationen definieren, können Sie den Kommunikations-Editor nutzen, um Ihre Inhalte zu formatieren und dynamisch anzupassen.

## <a name="rich-text-editor"></a>Rich-Text-Editor 

Der Kommunikations-Editor ermöglicht es dem Benutzer, den Text mithilfe der Editor-Optionen anzupassen. Benutzer können beispielsweise Schriftarten ändern, Aufzählungslisten erstellen, Inhalte hervorheben und vieles mehr. 

## <a name="merge-field-variables"></a>Feld Variablen zusammenführen

Sie können die e-Mail-Zusammenführungs Variablen aus dem Kommunikations-Editor nutzen, um angepasste Depot Attribute in den Textkörper einer Kommunikation einzubetten. Bei der Übermittlung an die Depotbank wird das Seriendruckfeld mit dem entsprechenden Feld aufgefüllt. Wenn Sie beispielsweise an Depotbank John Smith gesendet haben, würde das Seriendruckfeld [Depot Name] mit dem entsprechenden Namen übersetzt. 

Sie können e-Mail-Seriendruckfelder verwenden, indem Sie die Symbole für das **Seriendruckfeld** oben im Rich-Text-Editor-Steuerelement auswählen. Der Platzhalter wird basierend auf dem Speicherort des Cursors der Benutzer hinzugefügt. 

### <a name="list-of-merge-field-variables"></a>Liste der Seriendruckfeld Variablen

| Feldname                  | Feld Details | 
| :------------------- | :------------------- |
| Anzeigename  | Der vor-und Nachname der Depotbank. | 
| Bestätigungs Link | Ein benutzerdefinierter Link zum Aufzeichnen der Bestätigung der einzelnen depotverwalter.|                 |
| Portal Link     | Ein angepasster Link für das Compliance-Portal des Depotbank.|                |
| AusStellende Offizier                   | Die e-Mail-Adresse des angegebenen ausstellenden Offiziers.|                   |
| AusStellendes Datum                   | Das Datum, an dem der Hinweis ausgegeben wurde (UTC).              |
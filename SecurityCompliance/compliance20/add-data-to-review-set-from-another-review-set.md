---
title: Hinzufügen von Daten aus einem Übersichts Satz zu einem anderen überprüfungssatz
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
ms.openlocfilehash: 3a4d0d309daa5af9830f98215ca09321429785ee
ms.sourcegitcommit: 25595bc8fae96bc23b7b6d7102a22f37878987c0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "33641651"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a>Hinzufügen von Daten zu einem Übersichts Satz aus einem anderen überprüfungssatz

In einigen Fällen kann es erforderlich sein, einen Teil der Dokumente aus einem Übersichts Satz zu schnitzen und einzeln in einem anderen Übersichts Satz zusammenzuarbeiten.  Dies ist besonders nützlich, wenn Sie Inhalte in einem Übersichts Satz abgeschlachtet haben und Analytics für die Teilmenge der Daten ausführen möchten.

Folgen Sie dem Workflow in diesem Artikel, um Inhalt von einem Übersichts Satz zu einem anderen hinzuzufügen.

## <a name="before-you-begin"></a>Bevor Sie beginnen

Bevor Sie beginnen, müssen Sie einen neuen Übersichts Satz erstellen, dem Sie die Daten hinzufügen können.  Auf der Registerkarte Übersichts **Sätze** des Falls kann ein neuer Übersichts Satz hinzugefügt werden. Weitere Informationen finden Sie unter [Erstellen eines](managing-review-sets.md#create-a-review-set)Übersichts Satzes.

## <a name="step-1-identify-content-to-add-to-another-review-set"></a>Schritt 1: Identifizieren von Inhalten, die einem anderen überprüfungssatz hinzugefügt werden sollen

Sie können Inhalte aus einem Übersichts Satz zu einem anderen hinzufügen, indem Sie bestimmte Dokumente im Quell Übersichts Satz oder b seleting alle Elemente auswählen, die von der Übersichts Satz Abfrage zurückgegeben werden.  Wenn Sie ausgewählte Elemente hinzufügen, wählen Sie die Elemente aus, klicken Sie auf **Aktion**, und klicken Sie dann auf **zu einem anderen überprüfungssatz hinzufügen**.

![Zu einem anderen Übersichts Satz hinzufügen](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a>Schritt 2: Angeben von Optionen für das Hinzufügen zu einem anderen überprüfungssatz

Wählen Sie auf der Seite **zu einer anderen Option für Übersichts Optionen hinzufügen** den Übersichts Satz aus, dem Sie die Elemente hinzufügen möchten. Wählen Sie aus, ob **alle Suchergebnisse** oder **ausgewählte Elemente**hinzugefügt werden sollen.  Zusätzliche Informationen bieten Optionen zum Einbeziehen aller Metadaten aus den Elementen und die Angabe, ob die Tags (durch Aktivieren des Kontrollkästchens **Beschriftungen** ) aus dem Quell Übersichts Satz eingeschlossen werden sollen, wenn die Dokumente dem neuen überprüfungssatz hinzugefügt werden.  

![Zu einem anderen Übersichts Satz hinzufügen](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

Nachdem Sie auf **OK**geklickt haben, wird ein neuer Auftrag (mit dem Namen **Hinzufügen von Daten zu einem anderen**überprüfungssatz) erstellt, um den Inhalt zu einem anderen Übersichts Satz hinzuzufügen.  Sie können zur Registerkarte **Jobs** wechseln und den Fortschritt dieses Auftrags überwachen. Weitere Informationen finden Sie unter [Manage Jobs](managing-jobs-ediscovery20.md).

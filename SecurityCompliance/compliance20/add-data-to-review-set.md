---
title: Hinzufügen von Suchergebnissen zu einem Prüfdateisatz
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
description: ''
ms.openlocfilehash: 4de390972672509422e055cd3fd6a9f65d54a7ba
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155237"
---
# <a name="add-search-results-to-a-review-set"></a>Hinzufügen von Suchergebnissen zu einem Prüfdateisatz

Wenn Sie mit den Ergebnissen einer Suche zufrieden sind und Sie diese Suchergebnisse überprüfen und analysieren möchten, können Sie Sie zu einem Überprüfungs in dem Fall hinzufügen. Durch das Kopieren der ursprünglichen Daten in den Überprüfungs wird auch der Überprüfungs-und Analyseprozess erleichtert, indem Ihnen erweiterte Analysetools bereitgestellt werden, beispielsweise die Erkennung von Designs, die Erkennung praktischer Duplikate und die e-Mail-Threadidentifikation. Sie können auch Daten aus nicht Office 365 Datenquellen zu einem Überprüfungs Satz hinzufügen, damit Sie diese Daten zusätzlich zu den von Office 365 gesammelten Daten überprüfen können.

Wenn Sie die Ergebnisse einer Suche zu einem Überprüfungs Satz hinzufügen (Überprüfungs Sätze befinden sich auf der Registerkarte Überprüfungs **Sätze** des Falles), treten die folgenden zwei Dinge auf:

- Alle Elemente in den Suchergebnissen werden aus der ursprünglichen Datenquelle in den Live Office 365-Diensten kopiert und in einen sicheren Azure-Speicherort in der Microsoft-Cloud kopiert.

- Alle Elemente (einschließlich der Inhalte und Metadaten) werden erneut indiziert, sodass alle Daten in der Überprüfungsgruppe während der Überprüfung der Falldaten vollständig durchsuchbar sind. Das erneute Indizieren der Daten führt zu einer gründlichen und sehr schnellen Suche, wenn Sie die Daten im Überprüfungspaket während der Fallprüfung durchsuchen.

Klicken Sie zum Hinzufügen von Daten zu einem Überprüfungs Satzes auf der Registerkarte **Suchen** auf eine Suche, und klicken Sie dann auf der Flyout-Seite auf **zu überprüfende Ergebnisse hinzufügen** .

![Hinzufügen von Daten zu einem Überprüfungs Satzes](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

Beachten Sie, dass Sie zu einer vorhandenen Überprüfungsgruppe hinzufügen oder einen neuen Überprüfungs erstellen können.  Wenn Sie zu einem neuen Überprüfungs Sätze hinzufügen, geben Sie den Namen an, und klicken Sie dann auf **Hinzufügen**.

![Auswählen eines Überprüfungs Satzes](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

Das Hinzufügen von Daten zu einem Überprüfungs Satzes ist ein langwieriger Prozess. Dieser Prozess umfasst das Sammeln von Elementen aus den ursprünglichen Datenquellen in Office 365 (beispielsweise von Postfächern und Websites), das Kopieren dieser Elemente in den Azure-Speicherort (dieser Kopiervorgang wird auch als *Einnahme*bezeichnet) und anschließendes Erneutes Indizieren der Elemente. Sie können den Fortschritt auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchen** überwachen, indem Sie den Status in der Spalte **hinzugefügte Daten zum Überprüfen des Satzes über** wachen. Klicken Sie nach Abschluss der Überarbeitungs Satzverarbeitung in der Anfrage auf die Registerkarte Überprüfungs **Sätze** , und klicken Sie dann auf den Überprüfungs Satz, um die Prozess Filterung, Überprüfung, Kennzeichnung und das Exportieren von Daten in der Überprüfungsgruppe zu starten.

## <a name="add-a-sample-to-a-review-set"></a>Hinzufügen eines Beispiels zu einem Überprüfungs Satzes

Wenn Sie die Ergebnisse einer Suche gründlicher überprüfen möchten, bevor Sie Sie einer Überprüfungsgruppe hinzufügen, können Sie ein Beispiel der Suchergebnisse zu einer Überprüfungsgruppe hinzufügen, anstatt alles hinzuzufügen.

Wenn Sie einem Überprüfungs Satzes ein Beispiel hinzufügen möchten, klicken Sie auf der Registerkarte **Suchen** auf eine Suche, und klicken Sie auf der Flyout-Seite auf **Sample** . Wählen Sie auf der Seite **Stichproben Parameter** eine der folgenden Optionen aus:

- **Konfidenz Stufe%** und **Konfidenzintervall%** – die der Überprüfungsgruppe hinzugefügten Elemente werden durch die von Ihnen festgelegten statistischen Parameter bestimmt. Wenn Sie normalerweise bei Sampling-Ergebnissen eine Konfidenz Stufe und ein Intervall verwenden, geben Sie diese in den Dropdownfeldern an. Verwenden Sie andernfalls einfach die Standardeinstellungen.

- **Zufalls Beispiel%** – die Elemente, die dem Überprüfungs Satz hinzugefügt wurden, basieren auf einer zufälligen Auswahl des angegebenen Prozentsatzes der Gesamtzahl der Elemente, die von der Suche zurückgegeben wurden.

Nachdem Sie eine der vorherigen Optionen ausgewählt und konfiguriert haben, wählen Sie eine vorhandene Überprüfungsgruppe aus, um das Beispiel hinzuzufügen, und klicken Sie dann auf **senden**. Sie können den Fortschritt auch wieder auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchen** verfolgen, indem Sie den Status in der Spalte **hinzugefügte Daten zum Überprüfen des Satzes über** wachen.
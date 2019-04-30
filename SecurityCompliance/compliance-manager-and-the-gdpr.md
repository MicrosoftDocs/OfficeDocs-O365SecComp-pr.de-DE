---
title: Microsoft Compliance-Manager und die DSGVO
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: 10579edea5a36686b8b19cafd9d3d6e148cfdcd3
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473092"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a>Microsoft Compliance-Manager und die DSGVO

Die allgemeine Datenschutzverordnung (DSGVO), die von der Europäischen Union verabschiedet wurde, kann sich auf Ihre Compliance-Strategie auswirken und die erforderlichen Aktionen zur Verwaltung von Benutzer-und Kundeninformationen im Compliance-Manager ausführen.

## <a name="user-privacy-settings"></a>Datenschutzeinstellungen

Bestimmte Bestimmungen erfordern, dass eine Organisation Benutzer Verlaufsdaten löschen kann. Compliance-Manager bietet Funktionen für die **Datenschutzeinstellungen des Benutzers** , mit denen Administratoren folgende Aufgaben erfüllen können:
  
- [Suchen eines Benutzers](#search-for-a-user)
- [Exportieren eines Berichts mit Kontoverlaufsdaten](#export-a-report-of-account-data-history)
- [Löschen der Verlaufsdaten von Benutzern](#delete-user-data-history)
  
## <a name="search-for-a-user"></a>Suchen eines Benutzers

So suchen Sie nach einem Benutzerkonto
  
1. Geben Sie den Benutzer-e-Mail-Alias (die Informationen links vom @-Symbol) ein, und wählen Sie den Domänennamen aus der Liste Domänensuffix auf der rechten Seite aus. Für Organisationen mit mehreren registrierten Domänen müssen Sie das Domänennamensuffix überprüfen, um sicherzustellen, dass es korrekt ist.

2. Wenn Sie den Benutzernamen richtig eingegeben haben, wählen Sie **Suchen**aus.

3. Für Benutzerkonten, die nicht zurückgegeben werden, wird "Benutzer nicht gefunden" auf der Seite angezeigt. Überprüfen Sie die e-Mail-Adressinformationen des Benutzers, und nehmen Sie Korrekturen vor. Zum Wiederholen wählen Sie **Suchen**aus.

4. Für Benutzerkonten wird der Text der Schaltfläche von der **Suche** in **Clear**geändert. Dies gibt an, dass das zurückgegebene Benutzerkonto der Betriebs Kontext für die zusätzlichen Funktionen ist und diese Funktionen für dieses Benutzerkonto gelten.

5. Wählen Sie **Löschen**aus, um die Suchergebnisse zu löschen und nach einem anderen Benutzer zu suchen.

## <a name="export-a-report-of-account-data-history"></a>Exportieren eines Berichts mit Kontoverlaufsdaten

Für jedes identifizierte Benutzerkonto können Sie einen Bericht über Abhängigkeiten generieren, die mit diesem Konto verknüpft sind. Mit diesen Informationen können Sie geöffnete Aktionselemente erneut zuweisen oder den Zugriff auf zuvor hochgeladene Nachweise sicherstellen.
  
 So generieren und exportieren Sie einen Bericht
  
1. Wählen Sie **exportieren** aus, um einen Bericht über die aktuell dem zurückgegebenen Benutzerkonto zugewiesenen Compliance Manager-Steuerelement Aktionen und die Liste der von diesem Benutzer hochgeladenen Dokumente zu generieren und herunterzuladen. Wenn keine zugeordneten Aktionen oder hochgeladenen Dokumente vorhanden sind, gibt eine Fehlermeldung "keine Daten für diesen Benutzer" an.

2. Der Bericht wird im Hintergrund des aktiven Browserfensters heruntergeladen, wenn ein Download-Popup nicht angezeigt wird, das Sie in Ihrem Browser-Downloadverlauf überprüfen möchten.

3. Öffnen Sie das Dokument, um die Daten des Berichts zu überprüfen.

> [!IMPORTANT]
> Hierbei handelt es sich nicht um einen Verlaufsbericht, der Statusänderungen am Zuordnungs Verlauf für die Aktionselemente beibehält und anzeigt. Der generierte Bericht ist eine Momentaufnahme der Steuerelement-Aktionselemente, die zum Zeitpunkt der Ausführung des Berichts zugewiesen wurden (Datums-und Zeitstempel in den Bericht). Eine spätere erneute Zuweisung von Aktionselementen führt beispielsweise zu unterschiedlichen Snapshotbericht-Daten, wenn dieser Bericht erneut für denselben Benutzer generiert wird.
  
## <a name="delete-user-data-history"></a>Löschen der Verlaufsdaten von Benutzern

Legt alle Steuerelement-Aktionselemente fest, die dem zurückgegebenen Benutzer zugewiesen sind. Legt den **hoch** geladenen Wert für alle Dokumente fest, die der zurückgegebene Benutzer an ' Benutzer entfernt ' hochgeladen hat.
  
So löschen Sie das Aktionselement und den Dokumentupload-Verlauf des Benutzerkontos:
  
1. Wählen Sie **Löschen**aus.

    Ein Bestätigungsdialogfeld wird angezeigt, "*dadurch werden alle Aufgaben des Steuerelement-Aktionselements und der Dokumentupload-Verlauf für den ausgewählten Benutzer entfernt. Diese Aktion ist dauerhaft. Sind Sie sicher, dass Sie den Vorgang fortsetzen möchten?*"

2. Um fortzufahren, wählen Sie **OK**aus, andernfalls wählen Sie **Abbrechen**aus.
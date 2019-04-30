---
title: Microsoft Compliance Manager – Versionshinweise
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473090"
---
# <a name="release-notes-for-compliance-manager-preview"></a>Versionshinweise für Compliance-Manager (Preview)

Mit der öffentlichen Vorschau des Compliance-Managers erhalten Sie frühzeitigen Zugriff auf bevorstehende Funktionen und Updates.

Sie können das aktualisierte [Compliance-Manager-](https://servicetrust.microsoft.com/ComplianceManager) Tool im [Service Trust Portal](https://servicetrust.microsoft.com) verwenden, um behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachzuverfolgen, zuzuweisen und zu überprüfen.

## <a name="whats-new-in-compliance-manager-preview"></a>Neuigkeiten im Compliance-Manager (Preview)

- **Integration in Microsoft Secure Score:** Compliance-Manager unterstützt die Integration in [Microsoft Secure Score](microsoft-secure-score.md) , indem Kunden verwaltete Aktionen auf mehr als 50 Secure Score-Aktionen zugeordnet werden. Wenn Sie eine zugeordnete Aktion in Secure Score ausführen, wird die entsprechende Compliance-Manager-Aktion automatisch aktualisiert.

- **Importieren von benutzerdefinierten Bewertungen:** Zusätzlich zu den integrierten Bewertungen unterstützt Compliance Manager jetzt das Importieren von benutzerdefinierten Vorlagen, sodass Sie benutzerdefinierte Bewertungen für ein beliebiges Produkt oder einen Dienst sowie alle Standard-oder Regulierungen erstellen können.

- **Aktionselemente:** Aktionselemente sind jetzt einzelne Elemente, und viele enthalten Telemetrie-Sammlung von der Microsoft Secure Score Graph-API. Soweit möglich, haben die Empfehlungen für Technische Aktionen jetzt Links zur entsprechenden Konfigurationsseite im Office 365-Dienst.

- **Mandantenverwaltung:** Neue Schnittstelle zum Verwalten neuer Datenelemente im Compliance-Manager (Preview):
    - **Dimensionen:** Anzeigen, hinzufügen und Anpassen von Metadaten für Vorlagen, BEWERTUNGEN und Aktionselemente, mit denen Sie benutzerdefinierte Pivots für Filter erstellen können.
    - **Besitzer:** Geben Sie einen Besitzer für jedes Aktionselement an.
    - **Kundenaktionen:** Verwalten der vollständigen Liste der im Compliance-Manager (Preview) enthaltenen Aktionen und aktivieren/deaktivieren der Überwachung der sicheren Bewertung für Aktionselemente, die mit Secure Score integriert sind.

- **Aktualisierte Kompatibilitätsbewertung**: die Methodik wurde geändert, um die Synchronisierung mit Microsoft Secure Score zu unterstützen. Das scoringsystem entfernt die von Microsoft verwalteten Steuerelemente und konzentriert sich ausschließlich auf den Abschluss von vom Kunden verwalteten Steuerelementen.

## <a name="known-issues-in-compliance-manager-preview"></a>Bekannte Probleme im Compliance-Manager (Preview)

In den folgenden Abschnitten werden bekannte Probleme behandelt, die in kommenden Versionen von Compliance-Manager behoben werden müssen.

### <a name="compliance-score"></a>KonformitätsBewertung

- Wenn Aktionselemente als **nicht im Bereich**gekennzeichnet sind, wird die dem Aktionselement zugewiesene Bewertung nicht aus der Berechnung der Kompatibilitätsbewertung ausgeschlossen. Aktionselemente, die **nicht im Bereich** markiert sind, sollten ihre Konformitätsbewertung nicht verlängern.

### <a name="microsoft-managed-controls"></a>Von Microsoft verwaltete Steuerelemente

- Das Test Datum für von Microsoft verwaltete Steuerelemente wird nicht auf der Benutzeroberfläche angezeigt, selbst wenn diese in die Bewertung einbezogen werden. Zum Anzeigen von Informationen zum Test Datum müssen Sie die Bewertung exportieren.

### <a name="customization"></a>Anpassung

- Durch das Hinzufügen von benutzerdefinierten Steuerelementen kann ein neues Steuerelement zu einer vorhandenen Steuerelement Familie hinzugefügt werden, es ist jedoch nicht möglich, eine neue Steuerelement Familie hinzuzufügen.
- Diese Release unterstützt keine Verknüpfung von Aktionselementen oder Hinzufügen von Aktionen Elemente oder Steuerelemente zu einer Bewertung.
- Wenn Sie eine benutzerdefinierte Aktion erstellen, können Sie Sie nicht bearbeiten oder löschen.

### <a name="control-families-not-shown-in-assessments"></a>Steuern von Familien, die nicht in Bewertungen angezeigt werden

- Wenn Sie eine Vorlage importieren, reflektieren alle auf dieser Vorlage basierenden Bewertungen alle Steuerelementfamilien, die Teil der Vorlage sind. Wenn Sie jedoch der Vorlage neue Steuerelementfamilien hinzufügen, werden die Änderungen durch vorhandene Bewertungen nicht widergespiegelt. Nur neue Bewertungen, die aus der aktualisierten Vorlage erstellt wurden, spiegeln die Änderungen wider.

### <a name="filters"></a>Filter

- Das Filtern von Aktionselementen oder Steuerelementen führt nicht konsistent zu korrekten Ergebnissen.

### <a name="templates"></a>Vorlagen

- Archivierte Vorlagen können nicht bearbeitet werden.
- Gesperrte Vorlagen ermöglichen die Erstellung von Bewertungen, wenn Sie dies nicht tun sollten. Das Sperren einer Vorlage soll verhindern, dass Sie zum Erstellen von Bewertungen verwendet wird.

### <a name="export"></a>Exportieren

- Der Vorlagenexport in JSON schlägt fehl, wenn der Vorlagenstatus auf " **importiert** " oder "Ausstehend" festgelegt ist. ****

### <a name="supported-browsers"></a>Unterstützte Browser

- Die neuesten Versionen von Microsoft Edge, Chrome und Safari werden unterstützt.
- Es kann vorkommen, dass aktualisierte Daten erst angezeigt werden, wenn Ihr Browser aktualisiert wird.
- Die Vorschauversion von Microsoft Edge wird nicht unterstützt, hat aber keine bekannten Probleme.
- Internet Explorer wird nicht unterstützt.

### <a name="session-timeout"></a>Sitzungstimeout

- Wenn eine Sitzung ausläuft, wird möglicherweise ein Fehler "etwas schief gelaufen" angezeigt. Wechseln Sie zur Lösung des [Kompatibilitäts-Managers](https://servicetrust.microsoft.com/ComplianceManager) , und melden Sie sich erneut an.
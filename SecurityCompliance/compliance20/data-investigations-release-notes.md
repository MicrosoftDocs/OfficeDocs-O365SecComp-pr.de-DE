---
title: Versionshinweise für Daten Untersuchungen (Preview) in Microsoft 365
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
description: Dieser Artikel beschreibt die neue Version des erweiterten eDiscovery (Preview) in Microsoft 365.
ms.openlocfilehash: bcf10f5154723709b1cde761b0e8d02540341a26
ms.sourcegitcommit: 98ec28932ae20e848f9f489c3c78e4a7edab6d18
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "29636621"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Versionshinweise für Daten Untersuchungen (Preview) in Microsoft 365

Das neue Tool Daten Untersuchungen (Preview) können in Microsoft 365 selektieren, untersuchen und Warten von Daten miteinander verknüpft, Vorfälle, wie eine Daten stellen Vorfall oder einer internen Untersuchung. Die öffentliche Datenvorschau Untersuchungen enthält frühe Zugriff auf die in Kürze verfügbare Funktionalität und Updates. Um frühen Zugriff auf die neuesten Funktionen erhalten möchten, erstellen Sie eine neue Untersuchung in Daten Untersuchungen (Preview) in die Office 365-Sicherheit & Compliance Center. Informationen hierzu finden Sie unter [Verwalten von einem Daten stellen Vorfall in Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Neuigkeiten 

- **Untersuchungen** - können Sie Suchvorgänge und Vorfälle durch Erstellen einer Untersuchung gruppieren. Verwalten Sie, wer die Untersuchung durch Hinzufügen oder Entfernen von Mitgliedern zugreifen kann.  Sie können auch auswählen und Ihre bevorzugten Untersuchungen zu kennzeichnen. Zurückverfolgen und überwachen-Aktivität innerhalb und zwischen Untersuchungen neue Dashboards verwenden. Nachdem Sie Ihre Untersuchung abgeschlossen haben, können Sie schließen oder löschen Sie ihn.

- **Interessante Menschen** – Wenn Sie Untersuchungen als interessante Menschen Benutzer hinzufügen, können Sie ihr Postfach, OneDrive for Business-Konto und Microsoft-Teams, Websites anzeigen. Sie können genauer von Suchvorgängen Gültigkeitsbereich festgelegt. Sie können auch anzeigen, um eine Person von Interesse weiter zu untersuchen, audit-Datensätze im Zusammenhang mit deren Aktivitäten in Office 365 und anderen Microsoft-Diensten.

- **Suche** – erstellen eine unternehmensweite Suche mit verschiedenen Suchoptionen Bedingung. Wenn Sie wissen Benutzer oder Websites, die Sie suchen möchten, können Sie dazu hinzufügen, die diese Benutzer Personen von Interesse oder angeben Standorte im Assistenten zum Erstellen der Suche. 

- **Vorfälle** – erstellen einen neuen Vorfall und fügen Suchergebnisse, die Sie überprüfen möchten. Einzelne Dokumente überprüfen können, um Untersuchung Notes lassen Kommentieren und exportieren die Ergebnisse in einer anderen Umgebung verschieben. 

- **Überprüfen Sie** – verwenden eine systemeigene, Text und in der Nähe Native anzeigen, lesen Sie die Dokumente auf einen Vorfall hinzugefügt. Sie können auch zu Dokumenten zum Gruppieren von Elementen Analytics anwenden, indem Duplikate, e-Mail-Threads und Designs, die die Überprüfung des Vorfalls unterstützen kann. 

- **Redact, markieren, und mit Anmerkungen versehen** – Schwärzen Text und Anwenden von Tags Anmerkungen machen, wie Sie Dokumente lesen.
  
- **Tiefe Indizierung** – Wenn eine beliebige teilweise indizierte Elemente vorhanden sind, bei Bedarf neu indiziert werden, damit alle Daten für die Suche zur Verfügung stehen.

- **Error Remediation** – Remediate oder herunterladen, die Verarbeitung von Fehlern. Hierzu zählen außerdem Unterstützung für große Dateitypen Remediation, kennwortgeschützte Dateien und andere Probleme im Zusammenhang mit der Indizierung Fehler. 

- **Aufträge** – Status langer-Prozessen zu verfolgen.

- **Postfachelemente Festplatten-Delete** - In dringenden Fällen müssen Sie fehlende Elemente endgültig löschen. Zu diesem Zweck führen Sie die **neu ComplianceSearchAction-löschen - PurgeType HardDelete** Command in Security & Compliance Center PowerShell Elemente dauerhaft aus Postfächer zu entfernen. Weitere Informationen finden Sie unter [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).

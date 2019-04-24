---
title: Versionshinweise zu Daten Untersuchungen (Preview) in Microsoft 365
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
description: In diesem Artikel wird das neue Tool für Daten Untersuchungen (Preview) in Microsoft 365 beschrieben.
ms.openlocfilehash: 648f223c136007e88a3beb6b58e692b758b5d27f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258983"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Versionshinweise zu Daten Untersuchungen (Preview) in Microsoft 365

Sie können das neue Tool für Daten Untersuchungen (Preview) in in Microsoft 365 verwenden, um datenbezogene Vorfälle, wie beispielsweise einen Vorfall mit Datenausfällen oder interne Untersuchungen, zu selektieren, zu untersuchen und zu beheben. Die öffentliche Vorschau der Daten Untersuchungen bietet Ihnen frühzeitigen Zugriff auf die bevorstehenden Funktionen und Updates. Um frühzeitig Zugriff auf die neuesten Features zu erhalten, erstellen Sie eine neue Untersuchung in Daten Untersuchungen (Preview) im Security & Compliance Center. Weitere Informationen finden Sie unter [manage a Data Spilling Incident in Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Neuigkeiten 

- **** Untersuchungen – Sie können Suchvorgänge und Vorfälle gruppieren, indem Sie eine Überprüfung erstellen. Verwalten der Benutzer, die auf die Untersuchung zugreifen können, indem Sie Mitglieder hinzufügen oder entfernen.  Sie können Ihre bevorzugten Untersuchungen auch markieren und markieren. Verfolgen und Überwachen von Aktivitäten innerhalb und zwischen den Untersuchungen mithilfe neuer Dashboards. Nachdem Sie die Untersuchung abgeschlossen haben, können Sie Sie schließen oder löschen.

- **Personen von Interesse** – Wenn Sie Benutzer zu Untersuchungen als Interessengruppen hinzufügen, können Sie die Websites Mailbox, OneDrive for Business und Microsoft Teams anzeigen. Sie können Sie verwenden, um die Suche nach Inhalten zu bereichern. Um eine Person weiter zu untersuchen, können Sie auch Überwachungsdatensätze anzeigen, die sich auf ihre Aktivitäten in Office 365 und anderen Microsoft-Diensten beziehen.

- **** Suchen – erstellen Sie eine organisationsweite Suche mit verschiedenen Suchbedingungen. Wenn Sie wissen, Benutzer oder Websites, die Sie durchsuchen möchten, können Sie dies tun, indem Sie diese Benutzer als interessante Personen hinzufügen oder Websitespeicher Orte im Such Erstellungs-Assistenten angeben. 

- **Evidence** – erstellen Sie einen neuen Beweissatz, und fügen Sie Suchergebnisse hinzu, die Sie überarbeiten möchten. Sie können einzelne Dokumente überarbeiten, Anmerkungen hinzufügen, um Untersuchungen zu hinterlassen und Ergebnisse zu exportieren, um in eine andere Umgebung zu wechseln. 

- **Review** – verwenden Sie eine native, Text und in der Nähe von Native Ansichten, um die zu einem Vorfall hinzugefügten Dokumente zu überarbeiten. Sie können Analysen auch auf Dokumente anwenden, um Elemente nach Duplikaten, e-Mail-Threads und Designs zu gruppieren, was Ihnen helfen kann, den Vorfall zu überarbeiten. 

- **Redact, Tags und Anmerkungen** – Redact Text, wendet Tags an und macht Anmerkungen, wenn Sie Dokumente überprüfen.
  
- **Erweiterte Indizierung** – wenn teilweise indizierte Elemente vorhanden sind, werden Sie bei Bedarf erneut indiziert, sodass alle Daten für die Suche zur Verfügung stehen.

- **Fehler** Korrektur – beheben oder Herunterladen von Verarbeitungsfehlern. Dies umfasst die Behebung der Unterstützung für umfangreiche Dateitypen, kennwortgeschützte Dateien und andere Probleme im Zusammenhang mit Indizierungs Fehlern. 

- **Jobs** – verfolgen Sie den Status lang andauernder Prozesse.

- **Löschen von Postfachelementen** – in dringenden Situationen müssen Sie möglicherweise nicht verlegte Elemente endgültig löschen. Hierzu können Sie den Befehl **New-ComplianceSearchAction-Purge-purgeType HardDelete** in Security _AMP_ Compliance Center PowerShell ausführen, um Elemente dauerhaft aus Postfächern zu entfernen. Weitere Informationen finden Sie unter [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).

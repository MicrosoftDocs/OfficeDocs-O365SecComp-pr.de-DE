---
title: Suchen Sie nach Inhalten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/4/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Verwenden Sie das Inhaltssuche eDiscovery-Tool in der Office 365-Sicherheit &amp; Compliance Center e-Mail in Exchange-Postfächer schnell finden Dokumente in SharePoint-Websites und Speicherorte OneDrive und Sofortnachrichtenunterhaltungen führen in Skype für Unternehmen.
ms.openlocfilehash: 96a30bfe7b7cc5a1398cafa66577f0b7dc681d23
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238397"
---
# <a name="search-for-content-in-office-365"></a>Suchen Sie nach Inhalten in Office 365

Verwenden Sie das Tool Inhaltssuche in das Wertpapier &amp; Compliance Center e-Mail in Exchange-Postfächer schnell finden Dokumente in SharePoint-Websites und Speicherorte OneDrive und Sofortnachrichtenunterhaltungen führen in Skype für Unternehmen. Das Inhaltssuche-Tool können Sie um nach e-Mails, Dokumenten und Sofortnachrichtenunterhaltungen führen in Office 365 für die Zusammenarbeitstools wie Microsoft-Teams und Office 365 Gruppen zu suchen.
  
## <a name="search-for-content"></a>Suchen nach Inhalten

Der erste Schritt besteht darin starten Auswählen der Speicherorte für Inhalte zu suchen und Konfigurieren einer Stichwortabfrage zum Suchen nach bestimmten Objekten mit der Suchfunktion von Inhalten. Oder Sie einfach die Abfrage leer lassen und alle Elemente in der Zielspeicherorte zurück.
  
- [Erstellen und Ausführen](content-search.md) einer Inhaltssuche 
    
- [Build Suchabfragen und Bedingungen verwenden](keyword-queries-and-search-conditions.md) , um die Suche einzugrenzen 
    
- [Configure Search Berechtigungen filtern](permissions-filtering-for-content-search.md) , damit ein eDiscovery-Manager nur Teilmenge von Postfächern oder Websites in Ihrer Organisation durchsuchen kann 
    
- [Führen Sie eine ID-Liste Suche](csv-file-for-an-id-list-content-search.md) nach bestimmten e-Mail-Nachrichten suchen 
    
- [Suche cloudbasierten Postfächer](search-cloud-based-mailboxes-for-on-premises-users.md) für lokale Benutzer in Office 365

- [Ansicht schlüsselwortstatistiken](view-keyword-statistics-for-content-search.md) für die Ergebnisse einer Suche und dann Eingrenzen der Abfrage bei Bedarf 
    
- [Suche für Drittanbieter - Daten](use-content-search-to-search-third-party-data-that-was-imported.md) , die Ihre Organisation in Office 365 importiert wurde 
    
- Die Abfrage [massenbearbeitung](bulk-edit-content-searches.md) und Speicherorte für Inhalte für mehrere Suchvorgänge 
    
- [Beibehalten Bcc-Empfänger](https://docs.microsoft.com/exchange/policy-and-compliance/holds/preserve-bcc-recipients-and-group-members) , damit Sie suchen können 

## <a name="perform-actions-on-content-you-find"></a>Ausführen von Aktionen für Inhalte, die Sie gefunden

Nachdem Sie eine Suche ausführen und sie nach Bedarf optimieren, besteht der nächste Schritt etwas mit der von der Suche zurückgegebenen Ergebnisse möchten. Exportieren und die Ergebnisse an den lokalen Computer oder im Fall einer e-Mail-Angriff auf Ihre Organisation herunterladen, können Sie die Ergebnisse einer Suche aus Benutzerpostfächern löschen.
  
- [Exportieren Sie die Ergebnisse einer Suche Content](export-search-results.md) und auf dem lokalen Computer herunterladen 
    
- [Zum Suchen und Löschen von e-Mail-Nachrichten](search-for-and-delete-messages-in-your-organization.md) , wie Nachrichten, die Inhalte eines Virus, gefährliche Anlage oder Phishing-Nachrichten 
    
- [Exportieren eines Berichts](export-a-content-search-report.md) zu den Ergebnissen einer Inhaltssuche, ohne die tatsächliche Ergebnisse exportieren 
    
- [Die Download-Leistung zu steigern](increase-download-speeds-when-exporting-ediscovery-results.md) , wenn Sie Suchergebnisse exportieren 
    
## <a name="learn-more-about-content-search"></a>Erfahren Sie mehr über die Inhaltssuche

Inhaltssuche ist einfach zu verwenden, aber es ist außerdem ein leistungsfähiges Tool. Im Hintergrund, passiert eine Menge vorhanden ist. Je mehr sie kennen und verstehen, ihr Verhalten und seinen Beschränkungen, desto erfolgreicher werden verwenden Sie es für die Suche und Untersuchung Anforderungen Ihrer Organisation. Erfahren Sie mehr über:
  
- [Teilweise indizierte Elemente in Exchange und SharePoint](partially-indexed-items-in-content-search.md) sowie zum ein- oder auszuschließen, wenn Sie exportieren, und Laden Sie Suchergebnisse 
    
- [Untersuchen teilweise indizierte Elemente](investigating-partially-indexed-items-in-ediscovery.md) und Ihrer Organisation zu deren ermitteln 
    
- [Grenzen eines das Suchtool Inhalte](limits-for-content-search.md)wie beispielsweise die maximale Anzahl der Suchvorgänge, die gleichzeitig ausgeführt werden können und die maximale Anzahl der Speicherorte für Inhalte, die Sie in einem einzelnen Suchvorgang hinzufügen können 
    
- [Geschätzte und tatsächliche Suchergebnisse](differences-between-estimated-and-actual-ediscovery-search-results.md) und die Gründe, warum unterscheiden, wenn Sie exportieren, und Laden Sie die Suchergebnisse möglicherweise 
    
- [Deduplizierung in den Suchergebnissen](de-duplication-in-ediscovery-search-results.md) , die Sie aktivieren können, wenn Sie e-Mail-Nachrichten exportieren, die die Ergebnisse einer Suche sind 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Verwenden von Skripts für erweiterte Szenarien

In einigen Fällen müssen Sie weitere erweiterte, komplexe und wiederkehrende Aufgaben Inhaltssuche ausführen. In diesen Fällen ist es einfacher und Verwenden von PowerShell-Befehlen in das Wertpapier fast &amp; Compliance Center. Damit gewährleistet ist dies zu erleichtern, haben wir eine Reihe von Sicherheitsoptionen erstellt &amp; Compliance Center PowerShell-Skripts komplexe Content suchbezogene Aufgaben erleichtern.
  
- [Bestimmte Search-Mailbox und Websiteordner](use-content-search-for-targeted-collections.md) (eine *Auflistung zielorientierten* genannt) Wenn Sie sicher sind, dass Elemente, die auf eine Anfrage reagieren, in dem Ordner befinden 
    
- Eine Liste der Benutzer [für das Postfach und OneDrive Speicherort suchen](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) 
    
- [Erstellen, melden, und Löschen mehrere Suchvorgänge](create-report-on-and-delete-multiple-content-searches.md) , um schnell und effizient zu identifizieren und ausgemerzte suchbezogene Daten 
    
- [Klonen einer Inhaltssuche](clone-a-content-search.md) und schnell vergleichen Sie die Ergebnisse der verschiedenen Schlüsselwort Suchabfragen führen Sie auf der gleichen Speicherorte für Inhalte; oder verwenden Sie das Skript um zu sparen Sie Zeit, ohne eine große Anzahl von Speicherorte für Inhalte erneut eingeben, wenn Sie eine neue Suche erstellen 
    


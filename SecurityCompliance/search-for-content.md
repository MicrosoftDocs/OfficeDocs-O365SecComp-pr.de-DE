---
title: Suchen nach Inhalten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/4/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Verwenden Sie das eDiscovery-Tool für die Inhaltssuche im Security & Compliance Center, um schnell e-Mails in Exchange-Postfächern, Dokumenten in SharePoint-Websites und OneDrive-Standorten sowie Sofortnachrichtenunterhaltungen in Skype for Business zu finden.
ms.openlocfilehash: fc0bea90ce9cbfc27f894985c7d3083756ab108a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261353"
---
# <a name="search-for-content-in-office-365"></a>Suchen nach Inhalten in Office 365

Verwenden Sie das Tool für die Inhaltssuche im Security & Compliance Center, um schnell e-Mails in Exchange-Postfächern, Dokumenten in SharePoint-Websites und OneDrive-Standorten sowie Sofortnachrichtenunterhaltungen in Skype for Business zu finden. Sie können das Inhaltssuche-Tool verwenden, um nach e-Mails, Dokumenten und Sofortnachrichtenunterhaltungen in Office 365-Zusammenarbeitstools wie Microsoft Teams und Office 365-Gruppen zu suchen.
  
## <a name="search-for-content"></a>Suchen nach Inhalten

Der erste Schritt besteht darin, mit dem Inhaltssuche-Tool zu beginnen, inhaltsspeicherorte auszuwählen und eine Stichwortabfrage zu konfigurieren, um nach bestimmten Elementen zu suchen. Oder Sie können die Abfrage leer lassen und alle Elemente an den Zielstandorten zurückgeben.
  
- [Erstellen und ausführen](content-search.md) einer Inhaltssuche 
    
- [Erstellen von Suchabfragen und Verwenden von Bedingungen](keyword-queries-and-search-conditions.md) zum Einschränken der Suche 
    
- [Konfigurieren der Filterung von Suchberechtigungen](permissions-filtering-for-content-search.md) , sodass ein eDiscovery-Manager nur eine Teilmenge von Postfächern oder Websites in Ihrer Organisation durchsuchen kann 
    
- [Ausführen einer ID-Listensuche](csv-file-for-an-id-list-content-search.md) für die Suche nach bestimmten e-Mail-Nachrichten 
    
- [Durchsuchen von Cloud-basierten Postfächern](search-cloud-based-mailboxes-for-on-premises-users.md) für lokale Benutzer in Office 365

- [Anzeigen von Schlüsselwort Statistiken](view-keyword-statistics-for-content-search.md) für die Ergebnisse einer Suche und anschließende Verfeinerung der Abfrage 
    
- [Suchen nach drittanbieterdaten](use-content-search-to-search-third-party-data-that-was-imported.md) , die Ihre Organisation in Office 365 importiert hat 
    
- [Massenbearbeitung](bulk-edit-content-searches.md) der Abfrage-und inhaltsspeicherorte für mehrere Suchvorgänge 
    
- [Bcc-Empfänger beibehalten](https://docs.microsoft.com/exchange/policy-and-compliance/holds/preserve-bcc-recipients-and-group-members) , damit Sie nach diesen suchen können 

## <a name="perform-actions-on-content-you-find"></a>Ausführen von Aktionen für Inhalte, die Sie finden

Nachdem Sie eine Suche ausgeführt und bei Bedarf optimiert haben, besteht der nächste Schritt darin, etwas mit den Ergebnissen zu tun, die von der Suche zurückgegeben werden. Sie können die Ergebnisse auf Ihren lokalen Computer exportieren und herunterladen, oder im Fall eines e-Mail-Angriffs auf Ihre Organisation können Sie die Ergebnisse einer Suche aus Benutzerpostfächern löschen.
  
- [Exportieren der Ergebnisse einer Inhaltssuche](export-search-results.md) und herunterladen auf dem lokalen Computer 
    
- [Suchen und Löschen von e-Mail-nach](search-for-and-delete-messages-in-your-organization.md) richten wie Nachrichten, die Inhalte eines Virus, gefährliche Anlage oder Phishing-Nachrichten 
    
- [Exportieren eines Berichts](export-a-content-search-report.md) zu den Ergebnissen einer Inhaltssuche, ohne die tatsächlichen Ergebnisse zu exportieren 
    
- [Höhere Downloadgeschwindigkeit](increase-download-speeds-when-exporting-ediscovery-results.md) beim Exportieren von Suchergebnissen 
    
## <a name="learn-more-about-content-search"></a>Weitere Informationen zur Inhaltssuche

Die Inhaltssuche ist einfach zu verwenden, aber Sie ist auch ein leistungsstarkes Tool. Hinter den Kulissen gibt es viel zu tun. Je mehr Sie darüber wissen, und verstehen Sie sein Verhalten und seine Einschränkungen, desto erfolgreicher werden Sie es für die Such-und Ermittlungsanforderungen Ihrer Organisation verwenden. Informieren Sie sich über folgende Themen:
  
- [Teilweise indizierte Elemente in Exchange und SharePoint](partially-indexed-items-in-content-search.md) und wie Sie diese beim Exportieren und Herunterladen von Suchergebnissen einschließen oder ausschließen 
    
- [Untersuchen von teilweise indizierten Elementen](investigating-partially-indexed-items-in-ediscovery.md) und bestimmen der Exposition ihrer Organisation 
    
- [Grenzen des Inhalts](limits-for-content-search.md)Suchtools, wie beispielsweise die maximale Anzahl von Suchvorgängen, die gleichzeitig ausgeführt werden können, und die maximale Anzahl von Inhaltsspeicherorten, die Sie in eine einzelne Suche einbeziehen können 
    
- [Geschätzte und tatsächliche Suchergebnisse](differences-between-estimated-and-actual-ediscovery-search-results.md) und die Gründe, warum es Unterschiede zwischen diesen beim Exportieren und Herunterladen von Suchergebnissen geben kann 
    
- [Deduplizierung in Suchergebnissen](de-duplication-in-ediscovery-search-results.md) , die Sie beim Exportieren von e-Mail-Nachrichten, die die Ergebnisse einer Suche sind, aktivieren können 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Verwenden von Skripts für erweiterte Szenarien

Manchmal müssen Sie fortgeschrittenere, komplexere und sich wiederholende Inhalts Suchaufgaben ausführen. In diesen Fällen ist es einfacher und schneller, PowerShell-Befehle im Security & Compliance Center zu verwenden. Um dies zu vereinfachen, haben wir eine Reihe von Security & Compliance Center PowerShell-Skripts erstellt, die Sie bei der Durchführung komplexer Aufgaben im Zusammenhang mit der Inhaltssuche unterstützen.
  
- [Suchen bestimmter Postfach-und Websiteordner](use-content-search-for-targeted-collections.md) (als *Zielsammlung* bezeichnet), wenn Sie sicher sind, dass Elemente, die auf einen Fall reagieren, sich in diesem Ordner befinden. 
    
- [Durchsuchen des Postfach-und OneDrive-Speicherorts](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) für eine Liste der Benutzer 
    
- [Erstellen, melden Sie und löschen Sie mehrere Suchvorgänge](create-report-on-and-delete-multiple-content-searches.md) , um Such Daten schnell und effizient zu identifizieren und zu ermitteln. 
    
- [Klonen einer Inhaltssuche](clone-a-content-search.md) und schnelles vergleichen der Ergebnisse unterschiedlicher Keyword-Suchabfragen, die an denselben Inhaltsspeicherorten ausgeführt werden oder verwenden Sie das Skript, um Zeit zu sparen, da Sie beim Erstellen einer neuen Suche nicht die Anzahl der inhaltsspeicherorte erneut eingeben müssen. 
    


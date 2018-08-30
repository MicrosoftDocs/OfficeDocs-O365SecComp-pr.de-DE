---
title: Office 365 eDiscovery und Suche Features (Übersicht)
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Übersicht über das eDiscovery-Feature und andere Features für die Suche in Office 365 für Audit und Transparenz.
ms.openlocfilehash: 2d5cc2533c195b51f685aebd8da4462518116905
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529483"
---
# <a name="ediscovery-and-search-features"></a>eDiscovery und Features für die Suche 

## <a name="ediscovery"></a>eDiscovery
Das Feature für eDiscovery bietet eine zentrale Stelle für Administratoren, Compliance-beauftragte und andere autorisierte Benutzer eine umfassende Untersuchung in Office 365 Benutzeraktivität durchführen. Sicherheits-Managern mit den entsprechenden Berechtigungen können Suchvorgänge ausführen und Place-Haltebereiche auf Inhalte. Die Suchergebnisse sind die gleichen Ergebnisse, die Sie aus einem Inhaltssuche erhalten, mit der Ausnahme, dass ein eDiscovery-Fall für Haltebereiche erstellt wird, die angewendet werden. Die Ergebnisse von eDiscovery-suchen aus Sicherheitsgründen verschlüsselt werden, und die exportierten Daten können mit [erweiterten eDiscovery](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4)analysiert werden.

## <a name="content-search"></a>Inhaltssuche
[Inhaltssuche](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) ist eine neue eDiscovery-Suchfunktion im Sicherheit & Compliance Center, das bietet verbesserte Skalierung und Leistungsfähigkeit über frühere eDiscovery Suchtools. Inhaltssuche können Sie um Postfächer, Öffentliche Ordner, SharePoint Online-Websites und OneDrive for Business-Standorte zu suchen. Inhaltssuche wurde speziell für sehr umfangreiche suchen. Es gibt keine Grenzwerte für die Anzahl der Postfächer und Websites, die durchsucht werden. Es gibt auch keine Grenzwerte für die Anzahl der Suchvorgänge, die gleichzeitig ausgeführt werden können. Nach dem Ausführen einer Suche, die Anzahl der Inhaltsquellen und eine geschätzte Anzahl der Suche, die Ergebnisse im Detailbereich auf der Seite Suche angezeigt werden, in dem die Ergebnisse eine Vorschau anzeigen können, oder in einem lokalen Computer zu exportieren. Wenn Ihre Organisation über ein Office 365 Enterprise E5-Abonnement umfasst, können Sie auch [die Ergebnisse vorbereiten](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) , für die Analyse, die mit den leistungsstarken Analytics-Features von [Office 365 erweiterte eDiscovery](http://go.microsoft.com/fwlink/p/?LinkID=620116).

## <a name="audit-log-search"></a>Audit Log-Suche
Zusätzlich zum Nachverfolgen von Änderungen in ihre Office 365-Organisation, können Kunden auch anzeigen von Überwachungsberichten und Überwachungsprotokolle exportieren. Nachdem Überwachung für ein Office 365-Mandanten aktiviert ist, werden Benutzer und administrative Aktivität für diese Mandanten in den Ereignisprotokollen aufgezeichnet und durchsuchbar vorgenommen. Beispielsweise können Sie die postfachüberwachungsprotokollierung zum Nachverfolgen von Aktionen, die für ein Postfach von Benutzer, die nicht der Postfachbesitzer durchgeführt. Darüber hinaus können Compliance Officer die suchen und Filtern Funktionen verwenden, um festzustellen, ob ein Benutzer angezeigt oder ein bestimmtes Dokument heruntergeladen wurde oder wenn ein Administrator Management Benutzeraktivitäten ausgeführt oder die Mandantenkonfiguration in der letzten 90 Tage geändert hat. Suchergebnisse können wertvolle gerichtlichen Informationen zu bestimmten Aktivitäten enthalten, die von einem Benutzer oder Administrator durchgeführt wurden. Finden Sie unter [Löschvorgänge Aktivitäten in Office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) für eine Beschreibung des Benutzers und administrative Aktivitäten, die in Office 365 angemeldet sind.

Ereignisse aus SharePoint Online und OneDrive für Unternehmen werden innerhalb von 30 Minuten ihres Vorkommens im Protokoll angezeigt. Ereignisse von Exchange Online werden in die Überwachungsprotokolle innerhalb von 24 Stunden vorkommen. Anmeldung Ereignisse aus dem Azure Active Directory stehen innerhalb von Minuten vorkommen, und andere Verzeichnisereignisse aus dem Azure Active Directory verfügbar sind, innerhalb von 24 Stunden vorkommen. Ereignisse in Audit Log Suchergebnisse können auch zur weiteren Analyse exportiert werden. (Maximal 50.000 Einträge kann von einer einzigen Audit Log-Suche exportiert werden. Um weitere Einträge, die dies einschränken zu exportieren, entweder Reduzieren des Datumsbereichs, oder führen mehrere überwachungsprotokollsuchvorgänge.)

In der folgenden Tabelle sind einige der Informationen, die in Aktivitätsberichten angezeigt wird. Finden Sie in das [Überwachungsprotokoll Detailangaben zu den Eigenschaften in Office 365](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) für Weitere Informationen zu den Eigenschaften von jeder Office 365-Arbeitslast gesammelt werden.

| Eigenschaft | Beschreibung |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Datum | Datum und Uhrzeit des Ereignisses |
| User | Benutzer, der die ausgeführte Aktion |
| ClientIP | IPv4 oder IPv6-Adresse des Geräts, das verwendet wurde, wenn die Aktivität protokolliert wurde. |
| CreationTime | Datum und Uhrzeit in koordinierter Weltzeit (UTC), wenn der Benutzer die Aktivität ausgeführt. |
| Ereignisquelle | Gibt an, dass ein Ereignis aufgetreten ist. Mögliche Werte sind SharePoint- und ObjectModel. |
| ID | Die ID des Berichts-Eintrags. Die ID identifiziert eindeutig den Eintrag Bericht. |
| Vorgang | Name des Benutzers oder der Aktivität, die sich auf den Wert in den Ergebnissen Anzeige für diese Benutzeraktivität ausgewählten entspricht. |
| Organisations-ID an | Die GUID für die Organisation-Office 365-Dienst, in dem das Ereignis aufgetreten ist. |
| UserAgent | Informationen zum Browser des Benutzers, wie durch den Browser bereitgestellt. |
| Benutzer-ID | Benutzer, die (in der Operation-Eigenschaft angegeben) ausgeführte Aktion, die den Datensatz protokolliert geführt haben. |
| UserType | Typ des Benutzers, der der Vorgang ausgeführt wird. Die folgenden Werte geben den Benutzer. |
|  | 0 gibt einen regulären Benutzer an. |
|  | 2 gibt einem Administrator in Office 365-Organisation an. |
|  | 3 gibt ein Microsoft-Datencenter-Administrator oder Datacenter die Systemkonto an. |
| Arbeitslast | Office 365-Dienst in der die Aktivität aufgetreten ist. Mögliche Werte für diese Eigenschaft sind: |
|  | Exchange Online |
|  | SharePoint Online |
|  | OneDrive for Business |
|  | Azure Active Directory-Berichte |


Ausführliche Schritte zum Suchen von Office 365 Überwachungsprotokolle, finden Sie unter [Suchen von Überwachungsprotokollen in der Office 365-Sicherheit und Compliance Center](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c).

## <a name="search-unified-audit-log"></a>Suche Unified Überwachungsprotokoll
Die Audit Log-Suchfunktion im Compliance Center & Sicherheit kann verwendet werden, um das Überwachungsprotokoll unified zu suchen. Office 365 bietet auch die Möglichkeit, diese melden Sie sich mit remote-PowerShell zu durchsuchen. Insbesondere kann das [Cmdlet Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) in Exchange Online PowerShell unified Überwachungsprotokoll von Ereignissen im Zusammenhang mit Benutzervorgänge von Exchange Online, SharePoint Online, OneDrive für Unternehmen und Azure AD-Suche verwendet werden. Die Suche nach allen Ereignissen in einem bestimmten Zeitraum können, oder Sie können die Ergebnisse anhand bestimmter Kriterien, wie etwa eine bestimmte Aktion, die der Benutzer, der die Aktion oder das Zielobjekt durchgeführt filtern. Administratoren können bis zu 3 Exchange Online PowerShell-Sitzungen gleichzeitig ausgeführt große Datum Bereich Suchvorgänge aufteilen.

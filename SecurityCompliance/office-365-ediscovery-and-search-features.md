---
title: Office 365 eDiscovery und Such Features (Übersicht)
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über die eDiscovery-Funktion und andere Suchfeatures in Office 365 für die Überwachung und Transparenz.
ms.openlocfilehash: 5bab284c5fb66e50c945091766a329de7628abed
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091067"
---
# <a name="ediscovery-and-search-features"></a>eDiscovery und Suchfunktionen 

## <a name="ediscovery"></a>eDiscovery
Mit der eDiscovery-Funktion können Administratoren, Compliance Officer und andere autorisierte Benutzer eine umfassende Untersuchung der Benutzeraktivität von Office 365 durchführen. Sicherheitsbeauftragte mit den entsprechenden Berechtigungen können Suchvorgänge durchführen und Inhalte speichern. Die Suchergebnisse sind die gleichen Ergebnisse, die Sie von einer Inhaltssuche erhalten, mit der Ausnahme, dass ein eDiscovery-Fall für alle zugewiesenen Haltebereiche erstellt wird. Die Ergebnisse aus eDiscovery-suchen werden aus Sicherheitsgründen verschlüsselt, und die exportierten Daten können mit [Advanced eDiscovery](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4)analysiert werden.

## <a name="content-search"></a>Inhaltssuche
Die [Inhaltssuche](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) ist ein neues eDiscovery-Such Tool im Security _AMP_ Compliance Center, das verbesserte Skalierungs-und Leistungsfunktionen für frühere eDiscovery-Such Tools bietet. Sie können die Inhaltssuche zum Durchsuchen von Postfächern, öffentlichen Ordnern, SharePoint Online-Websites und OneDrive für Geschäftsstandorte verwenden. Die Inhaltssuche wurde speziell für sehr große Suchvorgänge entwickelt. Die Anzahl von Postfächern und Websites, die Sie durchsuchen können, ist unbegrenzt. Außerdem gibt es keine Begrenzung für die Anzahl der Suchvorgänge, die gleichzeitig ausgeführt werden können. Nachdem Sie eine Suche ausgeführt haben, wird die Anzahl der Inhaltsquellen und eine geschätzte Anzahl von Suchergebnissen im Detailbereich auf der Suchseite angezeigt, auf der Sie eine Vorschau der Ergebnisse anzeigen oder Sie auf einen lokalen Computer exportieren können. Wenn Ihre Organisation über ein Office 365 Enterprise E5-Abonnement verfügt, können Sie [die Ergebnisse](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) auch mithilfe der leistungsstarken Analysefunktionen von [Office 365 Advanced eDiscovery](http://go.microsoft.com/fwlink/p/?LinkID=620116)vorbereiten.

## <a name="audit-log-search"></a>Überwachungsprotokollsuche
Zusätzlich zum Nachverfolgen von Änderungen in Ihrer Office 365-Organisation können Kunden auch Überwachungsberichte anzeigen und Überwachungsprotokolle exportieren. Sobald die Überwachung für einen Office 365-Mandanten aktiviert ist, werden Benutzer-und Verwaltungsaktivitäten für diesen Mandanten in Ereignisprotokollen aufgezeichnet und durchsuchbar gemacht. Sie können beispielsweise die postfachüberwachungsprotokollierung verwenden, um die Aktionen nachzuverfolgen, die für ein Postfach durch andere Benutzer als den Postfachbesitzer durchgeführt wurden. Außerdem können Compliance Officer die Such-und Filterfunktionen verwenden, um zu sehen, ob ein Benutzer ein bestimmtes Dokument angezeigt oder heruntergeladen hat, oder ob ein Administrator Benutzer Verwaltungsaktivitäten durchgeführt oder Änderungen an der Mandanten Konfiguration in den letzten 90 Tagen vorgenommen hat. Suchergebnisse können wertvolle forensische Informationen zu bestimmten Aktivitäten enthalten, die von einem Benutzer oder Administrator durchgeführt wurden. Eine Beschreibung der Benutzer-und Verwaltungsaktivitäten, die in Office 365 protokolliert werden, finden Sie unter über [wachte Aktivitäten in office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) .

Ereignisse aus SharePoint Online und OneDrive for Business werden innerhalb von 30 Minuten nach ihrem Auftreten im Protokoll angezeigt. Ereignisse von Exchange Online werden innerhalb von 24 Stunden nach dem Auftreten in den Überwachungsprotokollen angezeigt. Anmeldeereignisse von Azure AD stehen innerhalb von Minuten zur Verfügung, und andere Verzeichnis Ereignisse von Azure AD stehen innerhalb von 24 Stunden zur Verfügung. Ereignisse in den Überwachungsprotokoll-Suchergebnissen können auch zur weiteren Analyse exportiert werden. (Maximal 50.000 Einträge können aus einer einzelnen Überwachungsprotokoll Suche exportiert werden. Um mehr Einträge zu exportieren, die diesen Grenzwert aufweisen, verringern Sie den Datumsbereich, oder führen Sie mehrere Überwachungsprotokoll suchen aus.)

In der folgenden Tabelle sind einige der Informationen aufgeführt, die in Aktivitätsberichten angezeigt werden. Weitere Informationen dazu, welche Eigenschaften von jeder Office 365-Arbeitsauslastung gesammelt werden, finden Sie [in den detaillierten Eigenschaften im office 365-Überwachungsprotokoll](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) .

| Eigenschaft | Beschreibung |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Datum | Datum und Uhrzeit des Ereignisses |
| User | Benutzer, der die Aktion ausgeführt hat |
| ClientIP | IPv4-oder IPv6-Adresse des Geräts, das verwendet wurde, als die Aktivität protokolliert wurde. |
| CreationTime | Datum und Uhrzeit in koordinierter weltZeit (UTC), als der Benutzer die Aktivität ausgeführt hat. |
| EventSource | Gibt an, dass ein Ereignis aufgetreten ist. Mögliche Werte sind SharePoint und objectModel. |
| ID | ID des Berichts Eintrags. Die ID identifiziert den Bericht Eintrag eindeutig. |
| Vorgang | Der Name des Benutzers oder der Aktivität, der dem in der Anzeigeergebnisse für diese Benutzeraktivität ausgewählten Wert entspricht. |
| Organisations | GUID für den Office 365-Dienst der Organisation, in dem das Ereignis aufgetreten ist. |
| UserAgent | Informationen zum Browser des Benutzers, die vom Browser bereitgestellt werden. |
| UserId | Der Benutzer, der die Aktion (in der Eigenschaft "Operation" angegeben) ausgeführt hat, die dazu geführt hat, dass der Datensatz protokolliert wird. |
| UserType | Der Benutzertyp, der den Vorgang ausgeführt hat. Die folgenden Werte geben den Benutzertyp an. |
|  | 0 gibt einen regulären Benutzer an. |
|  | 2 gibt einen Administrator in Ihrer Office 365-Organisation an. |
|  | 3 gibt einen Microsoft-Datencenter-Administrator oder ein Rechenzentrum-Systemkonto an. |
| Arbeitslast | Office 365-Dienst, in dem die Aktivität aufgetreten ist. Mögliche Werte für diese Eigenschaft sind: |
|  | Exchange Online |
|  | SharePoint Online |
|  | OneDrive for Business |
|  | Azure Active Directory-Berichte |


Ausführliche Schritte zum Durchsuchen von Office 365-Überwachungsprotokollen finden Sie unter durch [Suchen von Überwachungsprotokollen im office 365 Security _AMP_ Compliance Center](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c).

## <a name="search-unified-audit-log"></a>Einheitliches Überwachungsprotokoll durchsuchen
Die Suchfunktion des Überwachungsprotokolls im Security & Compliance Center kann zum Durchsuchen des einheitlichen Überwachungsprotokolls verwendet werden. Office 365 bietet außerdem die Möglichkeit, dieses Protokoll mithilfe der Remote-PowerShell zu durchsuchen. Insbesondere kann das [Cmdlet Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) in Exchange Online PowerShell zum Durchsuchen des vereinheitlichten Überwachungsprotokolls von Ereignissen im Zusammenhang mit Benutzervorgängen aus Exchange Online, SharePoint Online, OneDrive for Business und Azure AD verwendet werden. Sie können nach allen Ereignissen in einem angegebenen Zeitraum suchen, oder Sie können die Ergebnisse basierend auf bestimmten Kriterien filtern, beispielsweise eine bestimmte Aktion, der Benutzer, der die Aktion ausgeführt hat, oder das Zielobjekt. Administratoren können bis zu drei gleichzeitig ausgeführte Exchange Online PowerShell-Sitzungen verwenden, um große Datumsbereiche zu unterteilen.

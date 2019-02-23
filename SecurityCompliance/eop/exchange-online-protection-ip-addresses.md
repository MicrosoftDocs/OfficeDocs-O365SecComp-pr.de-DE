---
title: Exchange Online Protection-IP-Adressen
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Die folgenden Microsoft-Rechenzentrums-IP-Adresse verwendet Microsoft Exchange Online Protection (EOP) beim Senden von E-Mails, beim Empfangen von E-Mails sowie für die Portal- und Administrationsdienste von Exchange Online Protection. Damit Sie Nachrichten über EOP versenden und empfangen oder die Administrationsdienste nutzen können, müssen Sie in Ihrem Netzwerk Verbindungen von diesen IP-Adresse erlauben.
ms.openlocfilehash: 6c7d8c78a012be3928317eac1e9b6fcdeab64a24
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222824"
---
# <a name="exchange-online-protection-ip-addresses"></a>Exchange Online Protection-IP-Adressen

Die folgenden Microsoft-Rechenzentrums-IP-Adresse verwendet Microsoft Exchange Online Protection (EOP) beim Senden von E-Mails, beim Empfangen von E-Mails sowie für die Portal- und Administrationsdienste von Exchange Online Protection. Damit Sie Nachrichten über EOP versenden und empfangen oder die Administrationsdienste nutzen können, müssen Sie in Ihrem Netzwerk Verbindungen von diesen IP-Adresse erlauben.
 
> [!NOTE]
> Microsoft hat einen REST-basierten Webdienst für die Einträge IP-Adresse und FQDN auf dieser Seite entwickelt. Dieser neue Dienst unterstützt Sie beim Konfigurieren und Aktualisieren von Netzwerkumkreis Geräten wie Firewalls und Proxyservern. Sie können die Liste der Endpunkte, die aktuelle Version der Liste oder bestimmte Änderungen herunterladen. Dieser Dienst ersetzt das XML-Dokument, den RSS-Feed und die Einträge für die IP-Adresse und den FQDN auf dieser Seite. Um diesen neuen Dienst auszuprobieren, wechseln Sie zum [Office 365-IP-Adress-und-URL-](https://docs.microsoft.com/office365/enterprise/office-365-ip-web-service)Webdienst. 
 
## <a name="eop-ip-address-ranges"></a>EOP-IP-Adressbereiche

||||
|:-----|:-----|:-----|
|**IPv4-Adressbereiche** <br/> |**IPv6-Adressbereiche** <br/> |
| 23.103.132.0/22 | 2a01:111: F400:7c00::/54 |
| 23.103.136.0/21 | 2a01:111: F400: FC00::/54 |
| 23.103.144.0/20 | 2a01:111: F403::/48 |
| 23.103.198.0/23 |  |
| 23.103.200.0/22 |  |
| 40.92.0.0/14 |  |
| 40.107.0.0/17 |  |
| 52.100.0.0/14 |  |
| 52.238.78.88/32 |  |
| 65.55.88.0/24 |  |
| 65.55.169.0/24 |  |
| 94.245.120.64/26 |  |
| 104.47.0.0/17 |  |
| 157.55.234.0/24 |  |
| 157.56.110.0/23 |  |
| 157.56.112.0/24 |  |
| 207.46.100.0/24 |  |
| 207.46.163.0/24 |  |
| 213.199.154.0/24 |  |
| 213.199.180.128/26 |  |
| 216.32.180.0/23 |  |
||||
 
> [!IMPORTANT]
> Die hier angegebenen IP-Adressbereiche werden nur für Relay über Kunden-Connectors verwendet. Änderungen an der Liste der IP-Adressen sind selten und werden im Voraus mitgeteilt. Um sicherzustellen, dass Nachrichten, die Sie an Ihre Geschäftspartner, einen Smarthost oder eine lokale Umgebung weiterleiten, über den veröffentlichten IP-Adressbereich des Diensts gesendet werden, müssen Sie den richtigen Connector für das Routing an jedes Ziel konfigurieren. Weitere Informationen zu Connectors finden Sie unter [entscheiden, welcher Connector verwendet werden soll](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). die IP-Adressen in diesem Thema können sich im Laufe der Zeit ändern.  
 
Informationen zu IP-Adressen, die von Microsoft Office 365 verwendet werden, finden Sie unter [Von Office 365 verwendete IP-Adressen und URLs](https://go.microsoft.com/fwlink/p/?LinkId=324165).


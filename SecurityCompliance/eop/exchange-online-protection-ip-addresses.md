---
title: Exchange Online Protection-IP-Adressen
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Die folgenden Microsoft-Rechenzentrums-IP-Adresse verwendet Microsoft Exchange Online Protection (EOP) beim Senden von E-Mails, beim Empfangen von E-Mails sowie für die Portal- und Administrationsdienste von Exchange Online Protection. Damit Sie Nachrichten über EOP versenden und empfangen oder die Administrationsdienste nutzen können, müssen Sie in Ihrem Netzwerk Verbindungen von diesen IP-Adresse erlauben.
ms.openlocfilehash: 853b64410969fcc2f3c9ef238d2e9f4a4bb36e7b
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230007"
---
# <a name="exchange-online-protection-ip-addresses"></a>Exchange Online Protection-IP-Adressen

Die folgenden Microsoft-Rechenzentrums-IP-Adresse verwendet Microsoft Exchange Online Protection (EOP) beim Senden von E-Mails, beim Empfangen von E-Mails sowie für die Portal- und Administrationsdienste von Exchange Online Protection. Damit Sie Nachrichten über EOP versenden und empfangen oder die Administrationsdienste nutzen können, müssen Sie in Ihrem Netzwerk Verbindungen von diesen IP-Adresse erlauben.
 
> [!NOTE]
> Microsoft entwickelt einen REST-basierten Webdienst für die Einträge der IP-Adresse des FQDN auf dieser Seite. Mithilfe dieses neuen Diensts können Sie Geräte im Netzwerkumkreis konfigurieren und aktualisieren, z. B.Firewalls und Proxyserver. Die Liste mit Endpunkten, die aktuelle Version der Liste oder spezifische Änderungen können Sie herunterladen. Dieser Dienst wird irgendwann einmal die Einträge für das XML-Dokument, den RSS-Feed, die IP-Adresse und den FQDN auf dieser Seite ersetzen. Um diesem neuen Dienst auszuprobieren, wechseln Sie zu [Webdienst](https://support.office.com/article/managing-office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#webservice). 
 
## <a name="eop-ip-address-ranges"></a>EOP-IP-Adressbereiche

||||
|:-----|:-----|:-----|
|**IPv4-Adressbereiche** <br/> |**IPv6-Adressbereiche** <br/> |
| 23.103.132.0/22 | 2a01:111:f400:7 c 00:: / 54 |
| 23.103.136.0/21 | 2a01:111:f400:fc00:: / 54 |
| 23.103.144.0/20 | 2a01:111:f403:: / 48 |
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
> Die IP-Adressbereiche hier bereitgestellten dienen nur zur Weiterleitung über Customer Connectors. Änderungen an der Liste der IP-Adressen sind selten und im Voraus kommuniziert werden. So stellen Sie sicher, dass Nachrichten, die Sie an Ihre Geschäftspartner, einen Smarthost oder eine lokale Umgebung Route über den Dienst veröffentlichten IP-Adressen zu senden, der richtige Verbinder für das routing an jeder Ziel konfigurieren müssen. Weitere Informationen zu Connectors finden Sie unter [Entscheiden, die zu verwendende Verbinder](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). IP-Adressen in diesem Thema können mit der Zeit ändern. Für eine Aufzeichnung aller IP-Adressen, die hinzugefügt wurden, geändert oder veraltete im vergangenen Jahr, finden Sie unter [Change Notification EOP-IP-Adressen](change-notification-for-eop-ip-addresses.md). 
 
Informationen zu IP-Adressen, die von Microsoft Office 365 verwendet werden, finden Sie unter [Von Office 365 verwendete IP-Adressen und URLs](https://go.microsoft.com/fwlink/p/?LinkId=324165).
 
## <a name="ip-ranges-by-region"></a>IP-Bereiche nach Region

Exchange Online Protection am effizientesten E-Mails weiter und sorgt für die Einhaltung der vertraglichen Verpflichtungen unseren Kunden gegenüber. Die im Folgenden aufgeführten EOP-Endpunkte stellen die aktuellen regionalen IPv4-Bereiche dar. Diese IP-Adressen können jedoch ohne entsprechende Benachrichtigung an eine andere Funktion innerhalb von EOP zur Unterstützung der Kapazität und Effizienz erneut bereitgestellt werden. In diesen Ereignissen findet der E-Mail-Fluss weiterhin basierend auf unseren vertraglichen Verpflichtungen statt und wir geben unser Bestes, diese Liste von Endpunkten in einer bestimmten Frist zu aktualisieren, nachdem Änderungen vorgenommen wurden. Zu diesem Zeitpunkt verwalten wir keine Listen länderspezifischer Endpunkte für andere Komponenten von Office 365.
 
||||
|:-----|:-----|:-----|
|**Nord- und Südamerika** <br/> |**EMEA** <br/> |**APAC** <br/> |
| 23.103.132.0/22 | 23.103.132.0/22 |23.103.136.0/21 |
| 23.103.136.0/21 | 23.103.144.0/22 |23.103.152.0/22 |
| 23.103.148.0/22 | 40.92.0.0/18 |40.92.128.0/17 |
| 23.103.152.0/21 | 40.93.0.0/18 |40.93.128.0/17 |
| 23.103.156.0/22 | 40.94.0.0/18 |40.94.128.0/17 |
| 23.103.198.0/24 | 40.95.0.0/18 |40.95.128.0/17 |
| 23.103.200.0/22 | 40.107.0.0/18 |52.100.128.0/17 |
| 40.92.64.0/18 | 52.100.0.0/18 |52.101.128.0/17 |
| 40.93.64.0/18 | 52.101.0.0/18 |52.102.128.0/17 |
| 40.94.64.0/18 | 52.102.0.0/18 |52.103.128.0/17 |
| 40.95.64.0/18 | 52.103.0.0/18 |65.55.88.0/24 |
| 40.107.64.0/18 | 94.245.120.64/27 |104.47.64.0/18 |
| 52.100.64.0/18 | 104.47.0.0/19 |2a01:111:f400:7 c 00:: / 54 |
| 52.101.64.0/18 | 157.55.234.0/24 |  |
| 52.102.64.0/18 | 157.56.112.0/24 | |
| 52.103.64.0/18 | 213.199.154.0/24 | |
| 65.55.169.0/24 | 213.199.180.128/26 | |
| 104.47.32.0/19 | 2a01:111:f400:7e00:: / 56 | |
| 157.56.110.0/23 | 2a01:111:f400:fe00:: / 56 | |
| 207.46.100.0/24 |  | |
| 207.46.163.0/24 |  | |
| 216.32.180.0/23 |  | |
| 2a01:111:f400:7 c 00:: / 54 |  | |
||||


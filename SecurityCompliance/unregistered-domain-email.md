---
title: Nicht registrierte Domänen-e-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Wenn Sie ein hohes Volumen an e-Mails mit nicht registrierter Domäne senden, riskieren Sie, dass Ihre e-Mails blockiert werden. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: 207b71ab7e144af9709e7485d61c936e07271a11
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156297"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Nicht registrierte Domänen-e-Mails: was Sie wissen müssen

Office 365 ermöglicht Mandanten das Weiterleiten einiger Nachrichten über Exchange Online Protection (EoP). Ein unterstütztes Beispiel hierfür wäre, wenn Benutzer ein Office 365 Postfach haben und eine externe Person e-Mails sendet, die e-Mail-Weiterleitung jedoch so konfiguriert ist, dass Sie an das externe Postfach des Benutzers zurückgeht. Dies ist am häufigsten in Bildungsumgebungen, in denen Kursteilnehmer ihre persönliche e-Mail-Schnittstelle nutzen, aber immer noch e-Mails im Zusammenhang mit der Schule erhalten möchten. Ein weiteres Beispiel ist, wenn sich Kunden in einem Hybrid Szenario befinden und über lokale Server verfügen, die e-Mails aus EoP senden.

## <a name="problems-with-unregistered-domains"></a>Probleme mit nicht registrierten Domänen

Das Problem besteht darin, dass lokale Server kompromittiert werden und am Ende eine große Menge an Spam von EoP weitergeleitet werden. In fast allen Fällen werden die richtigen Connectors eingerichtet, aber e-Mails werden von nicht registrierten, auch als Nichtbereitstellung bezeichneten Domänen gesendet. Office 365 ermöglicht eine angemessene Menge an e-Mails aus nicht registrierten Domänen, aber eine akzeptierte Domäne sollte im Admin Center für jede Domäne konfiguriert werden, von der Sie den Versand planen.

Nachdem die Mandanten kompromittiert wurden, wird verhindert, dass ausgehende e-Mails für nicht registrierte Domänen gesendet werden. Benutzer erhalten einen Unzustellbarkeitsbericht (Non-Delivery Report, NDR), der Folgendes angibt:

- 550 5.7.750-Dienst ist nicht verfügbar. Vom Senden von nicht registrierten Domänen blockierter Client

## <a name="unblocking-tenant-in-order-to-send-again"></a>Aufheben der Blockierung von Mandanten, um erneut zu senden

Es gibt verschiedene Dinge, die Sie ausführen müssen, wenn Sie für das Senden von nicht registrierten Domänen blockiert werden:

1. Stellen Sie sicher, dass Sie alle Ihre Domänen im Microsoft 365 Admin Center registrieren. Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Suchen Sie nach ungewöhnlichen Konnektoren. Böswillige Akteure erstellen häufig neue eingehende Connectors in Ihrem Office 365 Mandanten, um Spam zu senden. Weitere Informationen zum Überprüfen der Connectors finden Sie [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps). 

3. Sperren Sie Ihre lokalen Server, und stellen Sie sicher, dass Sie nicht beeinträchtigt werden.

> [!TIP]
> Es gibt viele Faktoren, vor allem, wenn es sich um Drittanbieterserver handelt. Unabhängig davon müssen Sie in der Lage sein zu bestätigen, dass alle e-Mails, die Ihre Server verlassen, legitim sind.

4. Sobald Sie fertig sind, müssen Sie den Microsoft-Support anrufen und bitten, ihren Mandanten aufheben zu lassen, dass er von nicht registrierten Domänen erneut gesendet wird.  Die Bereitstellung des Fehlercodes ist hilfreich, aber Sie müssen nachweisen, dass Ihre Umgebung gesichert ist und dass kein Spam mehr gesendet wird. Weitere Informationen zum Öffnen eines Support Falls finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Weitere Informationen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)

[Unzustellbarkeitsberichte für E-Mails in Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Konfigurieren der E-Mail-Weiterleitung für ein Postfach](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mit Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Verwalten von akzeptierten Domänen in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

---
title: Nicht registrierte Domänen-e-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Wenn Sie eine große Anzahl von nicht registrierten Domänen-e-Mails senden, besteht das Risiko, dass Ihre e-Mails blockiert werden. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: 21c403c8072902565f63048782b06c531cdbceb0
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670540"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Nicht registrierte Domänen-e-Mails: was Sie wissen müssen

Office 365 ermöglicht es den Mandanten, einige Nachrichten über Exchange Online Protection (EOP) weiterzuleiten. Ein unterstütztes Beispiel dafür wäre, wenn Benutzer ein Office 365-Postfach haben und eine externe Person e-Mails sendet, die e-Mail-Weiterleitung jedoch so konfiguriert ist, dass Sie an das externe Postfach des Benutzers zurückgegeben wird. Dies ist am häufigsten in Bildungsumgebungen, in denen Schüler ihre persönliche e-Mail-Schnittstelle nutzen möchten, aber immer noch e-Mails im Zusammenhang mit der Schule. Ein weiteres Beispiel ist, wenn sich Kunden in einem Hybrid Szenario befinden und über lokale Server verfügen, die e-Mails aus EOP senden.

## <a name="problems-with-unregistered-domains"></a>Probleme mit nicht registrierten Domänen

Das Problem besteht darin, dass lokale Server kompromittiert werden und am Ende eine umfangreiche Anzahl von Spam-EOP. In fast allen Fällen werden die richtigen Connectors eingerichtet, aber e-Mails werden von nicht registrierten, auch als nicht zugestellt, bezeichneten Domänen gesendet. Office 365 ermöglicht eine angemessene Menge an e-Mails aus nicht registrierten Domänen, aber eine akzeptierte Domäne sollte im Admin Center für jede Domäne konfiguriert werden, von der aus Sie das Senden planen.

Nach der Kompromittierung werden die Mandanten daran gehindert, ausgehende e-Mails für nicht registrierte Domänen zu senden. Benutzer erhalten einen Unzustellbarkeitsbericht (NDR) mit den folgenden Angaben:

- 550 5.7.750-Dienst ist nicht verfügbar. Vom Senden von nicht registrierten Domänen blockierter Client

## <a name="unblocking-tenant-in-order-to-send-again"></a>Aufheben der Blockierung des Mandanten zum erneuten Senden

Es gibt mehrere Schritte, die Sie ausführen müssen, wenn Sie für das Senden von nicht registrierten Domänen gesperrt werden:

1. Stellen Sie sicher, dass Sie alle Ihre Domänen in Microsoft 365 Admin Center registrieren. Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Suchen Sie nach ungewöhnlichen Konnektoren. Böswillige Akteure erstellen häufig neue eingehende Connectors in Ihrem Office 365-Mandanten, um Spam zu senden. Weitere Informationen zur Überprüfung ihrer Konnektoren finden Sie [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps). 

3. Sperren Sie Ihre lokalen Server, und stellen Sie sicher, dass Sie nicht beeinträchtigt werden.

> [!TIP]
> Hier gibt es viele Faktoren, insbesondere, wenn es sich dabei um Drittanbieterserver handelt. Unabhängig davon müssen Sie bestätigen können, dass alle e-Mails, die Ihre Server verlassen, legitim sind.

4. Nachdem Sie fertig sind, müssen Sie den Microsoft-Support anrufen und bitten, ihren Mandanten zu entsperrten, dass er von nicht registrierten Domänen erneut sendet.  Das Bereitstellen des Fehlercodes ist hilfreich, aber Sie müssen nachweisen, dass Ihre Umgebung gesichert ist und dass Spam nicht erneut gesendet wird. Weitere Informationen zum Öffnen eines Support Falls finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Weitere Informationen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)

[Unzustellbarkeitsberichte für E-Mails in Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Konfigurieren der E-Mail-Weiterleitung für ein Postfach](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mit Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Verwalten von akzeptierten Domänen in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

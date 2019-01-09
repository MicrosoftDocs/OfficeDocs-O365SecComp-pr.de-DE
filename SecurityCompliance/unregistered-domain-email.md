---
title: Nicht registrierte Domäne E-Mail
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Wenn Sie eine große Menge von nicht registrierte Domäne e-Mail senden, laufen Sie Gefahr Ihrer e-Mail blockiert. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: f632c5f7ab94a200a364828408b13c0026335869
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769782"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Nicht registrierte Domäne Email: Was Sie wissen müssen

Office 365 ermöglicht Mandanten, einige Nachrichten über Exchange Online Protection (EOP) weiterzuleiten. Unterstützte beispielsweise wäre, wenn Benutzer verfügen über ein Office 365-Postfach und eine externe Person diese e-Mail sendet, aber e-Mail-Weiterleitung konfiguriert ist, sodass es wieder auf das Postfach des Benutzers externen out wechselt. Dies ist die am häufigsten verwendeten in Education-Umgebungen, in dem Kursteilnehmer möchten ihre persönlichen e-Mail-Schnittstelle nutzen erhalten aber immer noch im Zusammenhang mit Schule-e-Mails. Ein weiteres Beispiel ist, wenn Kunden befinden sich in einem hybridszenario und lokalen Servern, die nicht genügend EOP e-Mail senden.

## <a name="problems-with-unregistered-domains"></a>Probleme mit nicht registrierte Domänen

Das Problem ist beim lokalen Servern gefährdet abgerufen und am Ende eine große Menge von Spam aus EOP Weiterleitung. In fast allen Fällen die richtige Verbinder eingerichtet sind, aber von nicht aufgehoben, auch bekannt als vorbereitete Domänen e-Mail gesendet wird. Office 365 lässt einen angemessenen Zeitraum e-Mail-Nachrichten an nicht registrierte Domänen stammen, aber in der Verwaltungskonsole für jede Domäne, die Sie zum Senden von planen sollte eine akzeptierte Domäne konfiguriert werden.

Nachdem gefährdet ist, werden Mandanten senden ausgehenden e-Mails für nicht registrierte Domänen gehindert werden. Benutzer werden ein Unzustellbarkeitsbericht (Non-Delivery Report, NDR) angezeigt, die besagt:

- 550 5.7.750 Dienst nicht verfügbar. Client verhindert, dass nicht registrierte Domänen senden

## <a name="unblocking-tenant-in-order-to-send-again"></a>Aufheben der Blockierung Mandanten, um erneut zu senden

Es gibt verschiedene Dinge tun, wenn Sie zum Senden von nicht registrierte Domänen blockiert werden:

1. Stellen Sie sicher, dass alle Domänen in Office 365 Administrationscenter zu registrieren. Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Suchen Sie nach ungewöhnliche Connectors. Bösartige Akteure erstellt in Ihrer Office 365-Mandanten zum Senden von Spam häufig neue eingehende Connectors. Finden Sie weitere Informationen zum Einchecken Connectors [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps). 

3. Sperren von Ihren lokalen Servern, und stellen Sie sicher, dass sie nicht beeinträchtigt werden.

> [!TIP]
> Sind viele Faktoren hier, insbesondere dann, wenn dies Drittanbieter-Servern sind. Unabhängig davon, Sie müssen in der Lage sein zu bestätigen, dass alle e-Mails, die Ihre Server verlassen legitime sind.

4. Abschließend müssen Sie Microsoft Support anrufen, und bitten Sie abzurufenden Ihres Mandanten nicht mehr blockiert, um erneut aus nicht registrierte Domänen zu senden.  Bereitstellen den Fehlercode ist hilfreich, jedoch müssen Sie nachweisen, dass Ihre Umgebung gesichert wird und dass Spam nicht erneut gesendet werden. Weitere Informationen zum Öffnen einer Supportanfrage finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Weitere Informationen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)

[Unzustellbarkeitsberichte für E-Mails in Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Konfigurieren der E-Mail-Weiterleitung für ein Postfach](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mit Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Verwalten akzeptierte Domänen im Exchange, Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

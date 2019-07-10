---
title: Warteschlangenwarnungen und Warteschlangen
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: 'Administratoren können Informationen zu Warteschlangen Warnungen und Warteschlangen im Nachrichtenfluss-Dashboard im Security #a0 Compliance Center erhalten.'
ms.openlocfilehash: 9ab84c3c1840b3212e67f3a276784284c64e8d2e
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598141"
---
# <a name="queue-alerts-and-queues"></a>Warteschlangenwarnungen und Warteschlangen

## <a name="queue-alerts"></a>Warteschlangen Warnungen

Wenn Nachrichten nicht von Ihrer Office 365 Organisation an Ihre lokalen oder Partner-e-Mail-Server mithilfe von Connectors gesendet werden können, werden die Nachrichten in Office 365 in die Warteschlange eingereiht. Häufige Beispiele, die diese Bedingung verursachen, sind:

- Der Connector ist nicht ordnungsgemäß konfiguriert.

- In Ihrer lokalen Umgebung wurden Netzwerk-oder Firewall-Änderungen vorgenommen.

Office 365 wird die Zustellung für 48 Stunden fortgesetzt. Nach 48 Stunden laufen die Nachrichten ab und werden an die Absender in Unzustellbarkeitsberichten (auch als Unzustellbarkeitsberichte oder Bounce-Nachrichten bezeichnet) zurückgegeben.

Wenn das e-Mail-Volumen in der Warteschlange den vordefinierten Schwellenwert überschreitet (der Standardwert ist 2000 Nachrichten), sind die Warnungen im Nachrichtenfluss-Dashboard bei **den letzten Warnungen**verfügbar, und Administratoren erhalten eine e-Mail-Benachrichtigung (an Ihre alternative e-Mail-Adresse). . Informationen zum Konfigurieren des warnungsschwellenwerts, des täglichen Benachrichtigungs Grenzwerts und/oder der Empfänger der Warnung finden Sie im Abschnitt **Anpassen von Warteschlangen Warnungen** weiter unten.

![Warteschlangen Warnungen im Bereich "zuletzt verwendete Benachrichtigungen" im Nachrichtenfluss-Dashboard im Security #a0 Compliance Center](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a>Anpassen von Warteschlangen Warnungen

Einblicke in den Nachrichtenfluss erstellen eine Warnungs Richtlinie mit dem Namen " **Nachrichten wurden verzögert** (das Kontrollkästchen **e-Mail-Benachrichtigungen senden** " im Beispielbildschirm Screenshot unten) finden Sie unter **Alerts** \> **Alert Policies**. Sie können den Schwellenwert und die Benachrichtigungsempfänger ändern, indem Sie auf die Richtlinie klicken.

![Warnungs Navigation](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

Es wird ein neues Blade für Richtlinieninformationen angezeigt, und Sie können nun auf **Richtlinie bearbeiten**klicken.

![Richtlinie bearbeiten ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

Das Informationsblatt wird in die **Bearbeitungs Richtlinie**geändert. Sie können nun die Empfänger für die Benachrichtigungs-e-Mail, den Grenzwert für die Anzahl der pro Tag gesendeten Benachrichtigungen und den minimalen Schwellenwert für die Auslösung der Warnung ändern (200 oder mehr).

![Bearbeiten des Richtlinien Blatts](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a>Warnungsdetails für Warteschlangen

Wenn Sie auf die Warnung klicken, werden die Warnungsdetails in einem Flyout-Bereich angezeigt.

![Auswählen einer Warteschlangen Warnung im Bereich "zuletzt verwendete Benachrichtigungen" im Nachrichtenfluss-Dashboard im Security #a0 Compliance Center](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Das Flyout "Details zur Warteschlangen Warnung" im Security #a0 Compliance Center](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

Sie können in den Warnungsdetails auf **Warteschlange anzeigen** klicken, um die Warteschlangendetails, Probleme und Links zu den verfügbaren Korrekturen in einem neuen Flyout-Bereich anzuzeigen.

![Das Flyout "Details zur Warteschlangen Warnung" im Security #a0 Compliance Center](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Warteschlange in den Warnungsdetails anzeigen](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a>Warteschlangen

Auch wenn das Nachrichten Volume in der Warteschlange den Schwellenwert nicht überschreitet, können Sie weiterhin den Bereich **Warteschlangen** im Nachrichtenfluss-Dashboard verwenden, um Nachrichten anzuzeigen, die länger als eine Stunde in die Warteschlange gestellt wurden. Sie können den Bereich **warte** Schlangen verwenden, um die Anzahl der in der Warteschlange befindlichen Nachrichten zu überwachen (der Wert 0 gibt an, dass der Nachrichtenfluss ordnungsgemäß ist), und es wird eine Aktion ausgeführt, bevor die Anzahl der Nachrichten

![Warteschlangen im Nachrichtenfluss-Dashboard im Security #a0 Compliance Center](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

Wenn Sie auf die Anzahl der Warteschlangen Nachrichten in **warte**Schlangen klicken, werden die Warteschlangendetails und Anleitungen für die Behebung des Problems in einem Flyout-Bereich angezeigt (dasselbe Flyout, das angezeigt wird, nachdem Sie im Detail einer Warteschlangen Warnung auf **Warteschlange anzeigen** klicken).

![Warteschlangendetails](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen e-Mail-Fluss-Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Mail Flow Insights in the Security #a0 Compliance Center](mail-flow-insights.md).

---
title: Warteschlangenwarnungen und Warteschlangen
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Administratoren können sich über Warteschlangen Warnungen und Warteschlangen im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center informieren.
ms.openlocfilehash: 45c03ae8d5f646c4514b19669ca83b3eac561f68
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220795"
---
# <a name="queue-alerts-and-queues"></a>Warteschlangenwarnungen und Warteschlangen

## <a name="queue-alerts"></a>Warteschlangen Warnungen

Wenn Nachrichten nicht von Ihrer Office 365-Organisation an Ihre lokalen oder Partner-e-Mail-Server über Connectors gesendet werden können, werden die Nachrichten in der Warteschlange in Office 365. Häufige Beispiele, die diese Bedingung verursachen, sind:

- Der Connector ist falsch konfiguriert.

- In Ihrer lokalen Umgebung wurden Netzwerk-oder Firewall-Änderungen vorgenommen.

In Office 365 wird die Übermittlung für 48 Stunden fortgesetzt. Nach 48 Stunden laufen die Nachrichten ab und werden an die Absender in Unzustellbarkeitsberichten (auch als Unzustellbarkeitsberichte bezeichnet) zurückgegeben.

Wenn der e-Mail-Datenträger in der Warteschlange den vordefinierten Schwellenwert überschreitet (standardmäßig 2000 Nachrichten), stehen die Warnungen im e-Mail-Fluss-Dashboard unter **Aktuelle Benachrichtigungen**zur Verfügung, und Administratoren erhalten eine e-Mail-Benachrichtigung (an Ihre alternative e-Mail-Adresse) . Informationen zum Konfigurieren des warnungsschwellenwerts, des täglichen Benachrichtigungslimits und/oder der Empfänger der Warnung finden Sie im Abschnitt **Anpassen der Warteschlangen Warnungen** weiter unten.

![Warteschlangen Warnungen im Bereich "zuletzt verwendete Benachrichtigungen" des e-Mail-Fluss-Dashboards im Office 365 Security & Compliance Center](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a>Anpassen von Warteschlangen Warnungen

Nachrichtenfluss-Einblicke Erstellen einer Warnungs Richtlinie mit dem Namen " **Nachrichten wurden verzögert** " (das Kontrollkästchen **e-Mail-Benachrichtigungen senden** im Beispielbildschirm Foto unten) finden Sie unter Warnungs **Richtlinien**für **Warnungen** \> . Sie können den Schwellenwert und die Warnungsempfänger ändern, indem Sie auf die Richtlinie klicken.

![Benachrichtigungs Navigation](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

Es wird ein neues Blatt mit Richtlinieninformationen angezeigt, und Sie können nun auf **Richtlinie bearbeiten**klicken.

![Richtlinie bearbeiten ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

Das Blattinformationen wird in die **Richtlinie bearbeiten**geändert. Sie können nun die Empfänger für die Warnungs-e-Mail, den Grenzwert für die Anzahl der gesendeten Benachrichtigungen pro Tag und den minimalen Schwellenwert für die Warnung (200 oder mehr) ändern.

![Richtlinien Blatt bearbeiten](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a>Warnungsdetails der Warteschlange

Wenn Sie auf die Benachrichtigung klicken, werden die Warnungsdetails in einem Flyout-Bereich angezeigt.

![Wählen Sie im Bereich "zuletzt verwendete Benachrichtigungen" im e-Mail-Fluss-Dashboard im Office 365 Security & Compliance Center eine Warteschlangen Warnung aus.](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Das Flyout "Queue Alert Details" im Office 365 Security & Compliance Center](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

Sie können in den Warnungsdetails auf **Warteschlange anzeigen** klicken, um die Warteschlangendetails, Probleme und Links zu den verfügbaren Fixes in einem neuen Flyoutbereich anzuzeigen.

![Das Flyout "Queue Alert Details" im Office 365 Security & Compliance Center](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Warteschlange in den Warnungsdetails anzeigen](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a>Warteschlangen

Auch wenn der Nachrichten Datenträger in der Warteschlange den Schwellenwert nicht überschreitet, können Sie Nachrichten, die länger als eine Stunde in die Warteschlange eingereiht wurden, weiterhin im Bereich **Warteschlangen** des Nachrichtenflusses verwenden. Sie können den Bereich **warte** Schlangen verwenden, um die Anzahl der Nachrichten in der Warteschlange zu überwachen (der Wert 0 gibt an, dass der Nachrichtenfluss in Ordnung ist) und Maßnahmen zu ergreifen, bevor die Anzahl der Nachrichten in der Warteschlange zu hoch

![Warteschlangen im Nachrichtenübermittlungs-Dashboard im Office 365 Security & Compliance Center](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

Wenn Sie auf die Anzahl der Warteschlangen Nachrichten in **warte**Schlangen klicken, werden die Warteschlangendetails und Anleitungen zur Behebung des Problems in einem Flyout-Bereich angezeigt (dasselbe Flyout, das angezeigt wird, nachdem Sie in den Details einer Warteschlangen Warnung auf **Warteschlange anzeigen** klicken).

![Warteschlangendetails](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

---
title: Warteschlange Warnungen und Warteschlangen
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Administratoren können über Warteschlange Warnungen und Warteschlangen im Dashboard Mail Flow in die Sicherheit in Office 365 Compliance Center & informieren.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685463"
---
# <a name="queue-alerts-and-queues"></a>Warteschlange Warnungen und Warteschlangen

## <a name="queue-alerts"></a>Warteschlange Benachrichtigungen

Wenn Nachrichten an Ihre lokale von Office 365-Organisation gesendet werden können oder Partner e-Mail-Servern mithilfe von Connectors, werden die Nachrichten in Office 365 in der Warteschlange. Sind gängige Beispiele, die diese Bedingung verursachen:

- Der Verbindung ist nicht richtig konfiguriert.

- Netzwerke oder der Firewall geändert wurden in Ihrer lokalen Umgebung.

Office 365 wird weiterhin bis hin zur Bereitstellung für 48 Stunden wiederholen. Nach 48 Stunden, die Nachrichten läuft und an die Absender in Unzustellbarkeitsberichte zurückgegeben (auch bekannt als eine Unzustellbarkeitsberichte oder aufprallen Nachrichten).

Wenn das Volume e-Mail in der Warteschlange den vordefinierten Schwellenwert überschreitet (der Standardwert ist 2000-Nachrichten), Benachrichtigungen werden in der e-Mail-Fluss Dashboard am **letzten**verfügbar sein, und Administratoren erhalten eine e-Mail-Benachrichtigung (an ihre alternative e-Mail-Adresse) . Konfigurieren der Warnschwellenwert, tägliche Benachrichtigung Grenzwert und/oder Empfänger der Warnung finden Sie weiter unten im Abschnitt **Anpassen Warteschlange Warnungen** .

![Warteschlange Warnungen im Bereich zuletzt verwendete Benachrichtigungen des Dashboards Mail Flow in der Office 365-Sicherheit & Compliance Center](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a>Anpassen der Warteschlange Benachrichtigungen

Mail Flow Insights erstellen Sie eine Warnung Richtlinie benannten **Nachrichten verzögert wurden** ( **senden e-Mail-Benachrichtigungen** das Kontrollkästchen in der Beispiel-Screenshot) **Benachrichtigungen** gefunden \> **Benachrichtigung Richtlinien**. Sie können den Schwellenwert und Benachrichtigung Empfänger geändert werden, indem Sie auf die Richtlinie.

![Alerts-Navigation](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

Sehen Sie einen neue Richtlinie Informationen Blade, Sie können nun auf **Richtlinie bearbeiten**klicken.

![Richtlinie bearbeiten ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

Das Informationen Blade ändert sich der **Richtlinie bearbeiten**. Sie können jetzt die Empfänger für die Warnung e-Mails, die den Grenzwert für die Anzahl der Benachrichtigungen gesendet pro Tag und den kleinsten Schwellenwert zum Auslösen der Benachrichtigung (200 oder mehr) ändern.

![Richtlinie Blade bearbeiten](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a>Warteschlange Warnungsdetails

Wenn Sie die Benachrichtigung klicken, werden die Details der Warnung in einem Dropdown-Bereich angezeigt.

![Wählen Sie eine Warteschlange Warnung im Bereich zuletzt verwendete Benachrichtigungen des Dashboards Mail Flow in der Office 365-Sicherheit & Compliance Center](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Die Warteschlange alert Details flyoutmenü in der Office 365-Sicherheit & Compliance Center](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

Sie können in den Warnungsdetails an die Warteschlange Details, Probleme und Links zu verfügbaren Updates in einen neuen Fensterausschnitt flyoutmenü finden Sie unter **Warteschlange anzeigen** klicken.

![Die Warteschlange alert Details flyoutmenü in der Office 365-Sicherheit & Compliance Center](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Warteschlange in den Warnungsdetails anzeigen](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a>Warteschlangen

Auch wenn die Nachricht in der Warteschlange Lautstärke des Schwellenwerts noch nicht weiterhin können Sie Bereich **Warteschlangen** des e-Mail-Fluss Dashboards Nachrichten anzuzeigen, die für mehr als eine Stunde zurückgestellt wurden. Den Bereich **Warteschlangen** können Sie überwachen die Anzahl der Nachrichten in der Warteschlange (der Wert 0 gibt an, dass e-Mail-Fluss OK ist) und Maßnahmen ergreifen, bevor die Anzahl der Nachrichten in der Warteschlange zu groß wird.

![Warteschlangen im Dashboard Mail Flow in der Office 365-Sicherheit & Compliance Center](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

Wenn Sie die Anzahl der Nachrichten in **Warteschlangen**, die Warteschlange-Details in der Warteschlange klicken, und Richtlinien zum Beheben des Problems in einem Dropdown-Bereich (der gleichen flyoutmenü, die angezeigt wird, klicken Sie in den Details einer Warteschlange Warnung **Warteschlange anzeigen** ) angezeigt.

![Warteschlange-details](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

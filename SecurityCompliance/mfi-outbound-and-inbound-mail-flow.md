---
title: Fluss eingehender und ausgehender E-Mails
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Administratoren können sich über das Widget für ausgehende und eingehende Nachrichten im Nachrichtenfluss-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: 89408618e7c5b3c921382b3efa0257f263509b6d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252213"
---
# <a name="outbound-and-inbound-mail-flow"></a>Fluss eingehender und ausgehender E-Mails

Das Widget für **ausgehende und eingehende Nachrichten** kombiniert die Informationen aus dem **konnektorbericht** und dem früheren TLS-Übersichts **Bericht** an einem Ort.

![Der ausgehende und eingehende e-Mail-Fluss Bericht im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

Die Informationen im Widget beziehen sich auf Connectors und den TLS-Nachrichtenschutz in Office 365. Weitere Informationen finden Sie unter den folgenden Themen:

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Bei der Übertragung geschützte Nachricht (durch TLS)

Das Widget für **ausgehende und eingehende Nachrichtenübermittlung** zeigt die TLS-Verschlüsselung an, die für die Verbindung verwendet wird, wenn Nachrichten an Ihre und von ihrer Office 365-Organisation übermittelt werden. Die Verbindungen, die mit anderen e-Mail-Diensten hergestellt werden, werden durch TLS verschlüsselt, wenn von beiden Seiten TLS angeboten wird. Das Widget bietet eine Momentaufnahme der letzten Woche des Nachrichtenflusses. Wenn Sie auf **Details anzeigen**klicken, wird im Flyout **Nachricht Protected in Transit (by TLS)** der TLS-Schutz für Nachrichten angezeigt, die in Ihrer Organisation eingehen und diese verlassen.

![Das im Transit-Flyout (durch TLS) geschützte Nachrichten im Security & Compliance Center](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Derzeit ist TLS 1,2 die sicherste Version von TLS, die von Office 365 angeboten wird. Häufig müssen Sie die TLS-Verschlüsselung kennen, die für Konformitätsprüfungen verwendet wird. Möglicherweise haben Sie keine direkte Beziehung zu den meisten der Quell-und Ziel-e-Mail-Server (Sie besitzen Sie nicht, und auch nicht Microsoft), sodass Sie nicht über viele Optionen zur Verbesserung der TLS-Verschlüsselung verfügen, die von diesen Servern verwendet wird.

Sie können jedoch Connectors [](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) verwenden, um den bestmöglichen TLS-Schutz für Nachrichten sicherzustellen, die zwischen Ihren e-Mail-Servern und Office 365 gesendet werden. Der Nachrichtenfluss zwischen Office 365 und ihren eigenen e-Mail-Servern oder-Servern, die zu ihren Partnern gehören, ist häufig wichtiger und sensibler als reguläre Nachrichten, sodass Sie zusätzliche Sicherheit und Wachsamkeit für diese Nachrichten anwenden möchten. Sie können Ihre eigenen e-Mail-Server aktualisieren oder korrigieren, um die TLS-Verschlüsselung zu verbessern, die verwendet wird, oder um Ihre Partner dazu zu bringen, dasselbe zu tun. Der **connectorbericht** zeigt sowohl das Nachrichtenfluss Volume als auch die TLS-Verschlüsselung für Nachrichten an, die ihre Office 365-Connectors verwenden.

## <a name="connector-report"></a>Connectorbericht

Wenn Sie auf den Link **konnektorbericht** im Flyout **Nachricht Protected in Transit (by TLS)** klicken, werden im Bericht Informationen zu Nachrichten angezeigt, die über Connectors an Ihre und von Ihrer Office 365-Organisation übermittelt werden. Sie verwenden Connectors zwischen ihren eigenen e-Mail-Servern und Office 365-Servern und Office 365. Der Nachrichten Datenträger für jeden Connector und die TLS-Verschlüsselung für die Verbindung stehen zur Verfügung. Darüber hinaus können Sie auch Daten für Nachrichten anzeigen, die in Office 365 gesendet oder empfangen wurden, ohne einen Connector zu verwenden.

In der Ansicht **Nachrichtenfluss** wird die Anzahl der Nachrichten über den Connector für die vergangene Woche angezeigt. Sie können den Datums Umfang ändern, indem Sie **Filter** auswählen, um den Zeitraum auf maximal 30 Tage zu verlängern. Die Ansicht **alle Nachrichtenfluss** zeigt den gesamten Nachrichtenfluss an und von ihrer Office 365-Organisation über alle Connectors an. Sie können einen bestimmten Konnektor über den Namen im Dropdownmenü auswählen.

Sie können die Ansicht **TLS-Verwendung** aus der Dropdownliste auswählen, um den TLS-Schutz für Nachrichten über den Connector anzuzeigen. Wie im TLS-Übersichts **Bericht** Bericht wird in dieser Ansicht der Prozentsatz der verschiedenen TLS-Versionen angezeigt. Bei TLS 1,0-Verbindungen müssen Sie wirklich ihren e-Mail-Server oder den Server Ihres Partners aktualisieren oder reparieren, um Probleme zu vermeiden, wenn die TLS 1,0-Unterstützung schließlich in Office 365 veraltet ist. Weitere Informationen finden Sie unter [technische Referenzdetails zur Verschlüsselung in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

InSights verweisen auf Connectors, um Ihre Aufmerksamkeit auf mögliche TLS-Verschlüsselungsprobleme für den Connector zu lenken. Die Einblicke sind: **kein TLS ist mehr als 25%** oder **TLS 1,0 liegt über 50%**. Wenn diese Einblicke angezeigt werden, müssen Sie die e-Mail-Server untersuchen, die dem Connector zugeordnet sind, oder Ihre Partnerorganisation erreichen.

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights.md).

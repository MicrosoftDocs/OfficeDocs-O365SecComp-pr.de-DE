---
title: Ausgehenden und eingehenden Nachrichtenfluss
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Administratoren können über den ausgehenden und eingehenden e-Mail-Fluss Widget im Dashboard Mail Flow in die Sicherheit in Office 365 Compliance Center & informieren.
ms.openlocfilehash: 57792c0347490b40f97a8b92945a9c809484ba4f
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685462"
---
# <a name="outbound-and-inbound-mail-flow"></a><span data-ttu-id="93a04-103">Ausgehenden und eingehenden Nachrichtenfluss</span><span class="sxs-lookup"><span data-stu-id="93a04-103">Outbound and inbound mail flow</span></span>

<span data-ttu-id="93a04-104">Das Widget **ausgehenden und eingehenden Nachrichtenfluss** fasst die Informationen aus der **Connector-Bericht** und den früheren **TLS-Übersichtsbericht** an einem Ort.</span><span class="sxs-lookup"><span data-stu-id="93a04-104">The **Outbound and inbound mail flow** widget combines the information from the **Connector Report** and the former **TLS Overview Report** in one place.</span></span>

![Der ausgehenden und eingehenden e-Mail-Fluss Bericht im Dashboard Mail Flow in der Office 365-Sicherheit & Compliance Center](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

<span data-ttu-id="93a04-p101">Die Informationen im Widget bezieht sich auf Connectors und TLS Nachrichtenschutz in Office 365. Weitere Informationen finden Sie unter folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="93a04-p101">The information in the widget is related to connectors and TLS message protection in Office 365. For more information, see these topics:</span></span>

- [<span data-ttu-id="93a04-108">Configure mail flow using connectors in Office 365</span><span class="sxs-lookup"><span data-stu-id="93a04-108">Configure mail flow using connectors in Office 365</span></span>](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [<span data-ttu-id="93a04-109">Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert</span><span class="sxs-lookup"><span data-stu-id="93a04-109">How Exchange Online uses TLS to secure email connections in Office 365</span></span>](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a><span data-ttu-id="93a04-110">Während der Übertragung (per TLS) geschützten Nachricht</span><span class="sxs-lookup"><span data-stu-id="93a04-110">Message protected in transit (by TLS)</span></span>

<span data-ttu-id="93a04-p102">Das Widget **ausgehenden und eingehenden Nachrichtenfluss** zeigt die TLS-Verschlüsselung, die für die Verbindung verwendet wird, wenn Nachrichten an und von Office 365-Organisation übermittelt werden. Die Verbindungen, die mit anderen e-Mail-Diensten eingerichtet werden werden per TLS verschlüsselt, wenn TLS durch beide Seiten angeboten wird. Das Widget bietet eine Momentaufnahme der letzten Woche des e-Mail-Fluss. Wenn Sie auf **Details anzeigen**klicken, zeigt die **Nachricht während der Übertragung (per TLS) geschützten** flyoutmenü, den TLS-Schutz für Nachrichten eingeben und Ihre Organisation verlassen.</span><span class="sxs-lookup"><span data-stu-id="93a04-p102">The **Outbound and inbound mail flow** widget displays the TLS encryption that's used for the connection when messages are delivered to and from your Office 365 organization. The connections that are established with other email services are encrypted by TLS when TLS is offered by both sides. The widget offers a snapshot of the last week of mail flow. When you click **View Details**, the **Message protected in transit (by TLS)** flyout shows you the TLS protection for messages entering and leaving your organization.</span></span>

![Die in während der Übertragung (per TLS) flyoutmenü in die Sicherheit in Office 365 Compliance Center & geschützten Nachrichten](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

<span data-ttu-id="93a04-p103">Derzeit ist TLS 1.2 die sicherste Version von TLS, die von Office 365 angeboten wird. Häufig müssen Sie die TLS-Verschlüsselung kennen, die für die Einhaltung von Bestimmungen Überwachungen verwendet wird. Wahrscheinlich haben Sie keine direkte Beziehung mit Großteil der Quell- und e-Mail-Servern (Sie nicht besitzen, und weder funktioniert Microsoft), sodass Sie nicht viele Optionen zur Verbesserung der TLS-Verschlüsselung, die von diesen Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93a04-p103">Currently, TLS 1.2 is the most secure version of TLS that's offered by Office 365. Often, you'll need to know the TLS encryption that's being used for compliance audits. You probably don't have a direct relationship with most of the source and destination email servers (you don't own them, and neither does Microsoft), so you don't have many options to improve the TLS encryption that's used by those servers.</span></span>

<span data-ttu-id="93a04-p104">Aber Sie können [Connectors](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) verwenden, um sicherzustellen, dass den am besten verfügbaren TLS Schutz für Nachrichten, die zwischen Ihren e-Mail-Servern und Office 365 gesendet werden. Nachrichtenübermittlung zwischen Office 365 und Ihrer eigenen e-Mail-Server oder Server, die an Ihre Partner gehören ist häufig wichtige und vertrauliche als normale Nachrichten, sodass Sie zusätzliche Sicherheit und die Wachsamkeit auf diese Nachrichten anwenden möchten. Sie können aktualisieren oder korrigieren Sie Ihre eigenen e-Mail-Servern zur Verbesserung der TLS-Verschlüsselung, die verwendet wird, oder an Ihre Partner dasselbe treten. Der **Bericht Connector** zeigt Mail Flow Volume und TLS-Verschlüsselung für Nachrichten, die Ihre Office 365-Connectors verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93a04-p104">But, you can use [connectors](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) to ensure the best available TLS protection for messages that are sent between your email servers and Office 365. Mail flow between Office 365 and your own email servers or servers that belong to your partners is often more important and sensitive than regular messages, so you'll want to apply extra security and vigilance to those messages. You can upgrade or fix your own email servers to improve the TLS encryption that's being used, or reach out to your partners to do the same. The **Connector Report** displays both mail flow volume and TLS encryption for messages that use your Office 365 connectors.</span></span>

## <a name="connector-report"></a><span data-ttu-id="93a04-123">Connector-Bericht</span><span class="sxs-lookup"><span data-stu-id="93a04-123">Connector report</span></span>

<span data-ttu-id="93a04-p105">Wenn Sie auf den Link **Connector Bericht** aus der **Nachricht während der Übertragung (per TLS) geschützten** flyoutmenü klicken, zeigt den Bericht Informationen zu Nachrichten, die an und von Connectors mit Office 365-Organisation übermittelt werden. Verwenden Sie Connectors zwischen Ihrem eigenen e-Mail-Servern und Office 365 oder des Partners Servern und Office 365. Die Nachricht Lautstärke für jeden Connector und die TLS-Verschlüsselung für die Verbindung zur Verfügung steht. Darüber hinaus können Sie Daten für Nachrichten anzeigen, die gesendet oder empfangen in Office 365 ohne mithilfe eines Verbinders wurden.</span><span class="sxs-lookup"><span data-stu-id="93a04-p105">When you click on the **Connector Report** link from the **Message protected in transit (by TLS)** flyout, the report displays information about messages that are delivered to and from your Office 365 organization using connectors. You use connectors between your own email servers and Office 365 or your partner's servers and Office 365. The message volume for each connector and the TLS encryption for the connection is available. In addition, you can also view data for messages that were sent or received in Office 365 without using a connector.</span></span>

<span data-ttu-id="93a04-p106">Die **E-Mail-Fluss** Ansicht zeigt die Lautstärke von Nachrichten über den Connector für die vergangenen Woche. Sie können den Datumsbereich ändern, durch Auswählen der **Filter** , in dem Sie den Bereich auf ein Maximum von 30 Tagen erhöhen können. Die Ansicht **Alle E-Mail-Fluss** zeigt alle e-Mail-Fluss zu und von Office 365-Organisation über alle Connectors. Sie können einen bestimmten Connector namentlich im Dropdown-Menü auswählen.</span><span class="sxs-lookup"><span data-stu-id="93a04-p106">The **Mail Flow** view shows the volume of messages through the connector for the past week. You can change the date range by selecting **Filter** where you can increase the range to a maximum of 30 days. The **All Mail Flow** view shows all mail flow to and from your Office 365 organization through all connectors. You can select a specific connector by name in the drop down menu.</span></span>

<span data-ttu-id="93a04-p107">Sie können die **Verwendung von TLS** -Ansicht aus der Dropdown-Liste finden Sie unter Aufschlüsselung der TLS-Schutz für Nachrichten über den Connector auswählen. Als mit dem Bericht **TLS-Übersichtsbericht** zeigt diese Ansicht den Prozentsatz der die verschiedenen Versionen von TLS. Für TLS 1.0-Verbindungen wirklich benötigen Sie Ihr e-Mail-Server oder Server Ihres Partners aktualisiert oder um alle Probleme zu vermeiden, wenn TLS 1.0-Unterstützung in Office 365 schließlich veraltet ist behoben. Weitere Informationen finden Sie unter [Technische Referenz Details über die Verschlüsselung in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).</span><span class="sxs-lookup"><span data-stu-id="93a04-p107">You can select the **TLS usage** view from the drop down to see the breakdown of TLS protection for messages through the connector. As with the **TLS Overview Report** report, this view shows the percentage of the different TLS versions. For TLS 1.0 connections, you really need to get your email server or your partner's server upgraded or fixed to avoid any issues when TLS 1.0 support is eventually deprecated in Office 365. For more information, see [Technical reference details about encryption in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).</span></span>

<span data-ttu-id="93a04-p108">Insights zeigen Sie auf Verbindungen, die Ihre Aufmerksamkeit auf potenzielle Probleme der TLS-Verschlüsselung für den Connector zeichnen unterstützen. Die Insights sind: **No TLS über 25 %** oder **TLS 1.0 ist über 50 %**. Wenn Sie diese Einblicke angezeigt wird, müssen Sie Ihre e-Mail-Server zu untersuchen, die der Verbindung zugeordnet sind, oder organisationsinterne Partner treten.</span><span class="sxs-lookup"><span data-stu-id="93a04-p108">Insights point to connectors to help draw your attention to potential TLS encryption problems for the connector. The insights are: **No TLS is over 25%** or **TLS 1.0 is above 50%**. If you see these insights, you need to investigate your email servers that are associated with the connector, or reach out to your partner organization.</span></span>
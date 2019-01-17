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
# <a name="outbound-and-inbound-mail-flow"></a>Ausgehenden und eingehenden Nachrichtenfluss

Das Widget **ausgehenden und eingehenden Nachrichtenfluss** fasst die Informationen aus der **Connector-Bericht** und den früheren **TLS-Übersichtsbericht** an einem Ort.

![Der ausgehenden und eingehenden e-Mail-Fluss Bericht im Dashboard Mail Flow in der Office 365-Sicherheit & Compliance Center](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

Die Informationen im Widget bezieht sich auf Connectors und TLS Nachrichtenschutz in Office 365. Weitere Informationen finden Sie unter folgenden Themen:

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Wie Exchange Online mithilfe von TLS E-Mail-Verbindungen in Office 365 sichert](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Während der Übertragung (per TLS) geschützten Nachricht

Das Widget **ausgehenden und eingehenden Nachrichtenfluss** zeigt die TLS-Verschlüsselung, die für die Verbindung verwendet wird, wenn Nachrichten an und von Office 365-Organisation übermittelt werden. Die Verbindungen, die mit anderen e-Mail-Diensten eingerichtet werden werden per TLS verschlüsselt, wenn TLS durch beide Seiten angeboten wird. Das Widget bietet eine Momentaufnahme der letzten Woche des e-Mail-Fluss. Wenn Sie auf **Details anzeigen**klicken, zeigt die **Nachricht während der Übertragung (per TLS) geschützten** flyoutmenü, den TLS-Schutz für Nachrichten eingeben und Ihre Organisation verlassen.

![Die in während der Übertragung (per TLS) flyoutmenü in die Sicherheit in Office 365 Compliance Center & geschützten Nachrichten](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Derzeit ist TLS 1.2 die sicherste Version von TLS, die von Office 365 angeboten wird. Häufig müssen Sie die TLS-Verschlüsselung kennen, die für die Einhaltung von Bestimmungen Überwachungen verwendet wird. Wahrscheinlich haben Sie keine direkte Beziehung mit Großteil der Quell- und e-Mail-Servern (Sie nicht besitzen, und weder funktioniert Microsoft), sodass Sie nicht viele Optionen zur Verbesserung der TLS-Verschlüsselung, die von diesen Servern verwendet wird.

Aber Sie können [Connectors](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) verwenden, um sicherzustellen, dass den am besten verfügbaren TLS Schutz für Nachrichten, die zwischen Ihren e-Mail-Servern und Office 365 gesendet werden. Nachrichtenübermittlung zwischen Office 365 und Ihrer eigenen e-Mail-Server oder Server, die an Ihre Partner gehören ist häufig wichtige und vertrauliche als normale Nachrichten, sodass Sie zusätzliche Sicherheit und die Wachsamkeit auf diese Nachrichten anwenden möchten. Sie können aktualisieren oder korrigieren Sie Ihre eigenen e-Mail-Servern zur Verbesserung der TLS-Verschlüsselung, die verwendet wird, oder an Ihre Partner dasselbe treten. Der **Bericht Connector** zeigt Mail Flow Volume und TLS-Verschlüsselung für Nachrichten, die Ihre Office 365-Connectors verwendet werden.

## <a name="connector-report"></a>Connector-Bericht

Wenn Sie auf den Link **Connector Bericht** aus der **Nachricht während der Übertragung (per TLS) geschützten** flyoutmenü klicken, zeigt den Bericht Informationen zu Nachrichten, die an und von Connectors mit Office 365-Organisation übermittelt werden. Verwenden Sie Connectors zwischen Ihrem eigenen e-Mail-Servern und Office 365 oder des Partners Servern und Office 365. Die Nachricht Lautstärke für jeden Connector und die TLS-Verschlüsselung für die Verbindung zur Verfügung steht. Darüber hinaus können Sie Daten für Nachrichten anzeigen, die gesendet oder empfangen in Office 365 ohne mithilfe eines Verbinders wurden.

Die **E-Mail-Fluss** Ansicht zeigt die Lautstärke von Nachrichten über den Connector für die vergangenen Woche. Sie können den Datumsbereich ändern, durch Auswählen der **Filter** , in dem Sie den Bereich auf ein Maximum von 30 Tagen erhöhen können. Die Ansicht **Alle E-Mail-Fluss** zeigt alle e-Mail-Fluss zu und von Office 365-Organisation über alle Connectors. Sie können einen bestimmten Connector namentlich im Dropdown-Menü auswählen.

Sie können die **Verwendung von TLS** -Ansicht aus der Dropdown-Liste finden Sie unter Aufschlüsselung der TLS-Schutz für Nachrichten über den Connector auswählen. Als mit dem Bericht **TLS-Übersichtsbericht** zeigt diese Ansicht den Prozentsatz der die verschiedenen Versionen von TLS. Für TLS 1.0-Verbindungen wirklich benötigen Sie Ihr e-Mail-Server oder Server Ihres Partners aktualisiert oder um alle Probleme zu vermeiden, wenn TLS 1.0-Unterstützung in Office 365 schließlich veraltet ist behoben. Weitere Informationen finden Sie unter [Technische Referenz Details über die Verschlüsselung in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

Insights zeigen Sie auf Verbindungen, die Ihre Aufmerksamkeit auf potenzielle Probleme der TLS-Verschlüsselung für den Connector zeichnen unterstützen. Die Insights sind: **No TLS über 25 %** oder **TLS 1.0 ist über 50 %**. Wenn Sie diese Einblicke angezeigt wird, müssen Sie Ihre e-Mail-Server zu untersuchen, die der Verbindung zugeordnet sind, oder organisationsinterne Partner treten.

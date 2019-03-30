---
title: Bericht über SMTP-AUTH-Clients
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren erfahren mehr über den Bericht über SMTP-AUTH-Clients im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: b6698345a89edf52e4ee14cea144cb88ff080583
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998708"
---
# <a name="smtp-auth-clients-report"></a>Bericht über SMTP-AUTH-Clients

> [!NOTE]
> Die in diesem Thema beschriebenen Features wurden nicht für alle Office 365-Organisationen bereitgestellt und können geändert werden.

Im Bericht **SMTP AUTH Clients** wird die Verwendung des SMTP-AUTH-Client Übermittlungsprotokolls durch Benutzer oder Systemkonten in Ihrer Organisation hervorgehoben. Dieses Legacy Protokoll (das den Endpunkt smtp.office365.com verwendet) bietet nur die Standardauthentifizierung und ist anfällig dafür, von kompromittierten Konten zum Senden von e-Mails verwendet zu werden.  Mit diesem Bericht können Sie nach ungewöhnlichen Aktivitäten suchen. Außerdem werden die TLS-Verwendungsdaten für Clients oder Geräte mit SMTP-Authentifizierung angezeigt.

Das im e-Mail-Fluss-Dashboard angezeigte Widget gibt die Anzahl der Benutzer oder Dienstkonten an, die das SMTP-Authentifizierungsprotokoll in den letzten 7 Tagen verwendet haben.

![Der Bericht über SMTP-AUTH-Clients im Nachrichtenübermittlungs-Dashboard im Security & Compliance Center](media/smtp-auth-clients-report-selected.png)

Wenn Sie auf das Widget klicken, wird ein Flyout geöffnet, das eine aggregierte Ansicht der TLS-Nutzung und-Volumes für die letzte Woche bereitstellt.

![Das Flyout im Bericht über SMTP-AUTH-Clients](media/smtp-auth-clients-flyout.png)

Wenn Sie auf den Link **SMTP-AUTH-Clients melden** klicken, werden zwei Hauptdaten Pivots und zwei Datenansichten angezeigt. Die Daten Pivots sind die **sendelautstärke** und die **TLS-Verwendung**. Die Datenansichten sind das Diagramm und die Detailtabelle.

Die **sendenDe Volumen** Ansicht zeigt die Anzahl der Nachrichten an, die über SMTP-Authentifizierung für den angegebenen Zeitraum gesendet wurden. Sie können den Range anpassen, indem Sie auf **Filter**klicken. Das Diagramm wird nach der Absenderdomäne organisiert. Sie können für jede Domäne separate Daten anzeigen, indem Sie die Domäne in der Dropdownliste **Daten anzeigen für** auswählen.

![Senden von Volumes im SMTP-AUTH-Clientbericht](media/smtp-auth-clients-report-sending-volume.png)

Sie können detaillierte Informationen zu den Absendern und deren Anzahl von Nachrichten anzeigen, indem Sie auf **Details-Tabelle anzeigen**klicken. Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.

![Details-Tabelle zum Senden von Volumes im SMTP-AUTH-Clientbericht](media/smtp-auth-clients-report-details-sending-volume.png)

Die **TLS-Verwendungs** Pivot ist wichtig aufgrund der bevorstehenden veraltet von TLS 1.0 und TLS 1.1 in Office 365. Viele ältere Geräte und Anwendungen können keine e-Mails senden, wenn Sie nur TLS 1.0 mit SMTP-Authentifizierung verwenden können. Mit diesem Pivot können Sie Benutzer und Systemkonten, die noch ältere Versionen von TLS verwenden, identifizieren und Maßnahmen ergreifen.

![TLS-Verwendung im Bericht über SMTP-AUTH-Clients](media/smtp-auth-clients-report-tls-usage.png)

Sie können detaillierte Informationen über die Absender, die Versionen von TLS, die Sie mit SMTP-Authentifizierung verwenden, und ihre Nachrichtenanzahl anzeigen, indem Sie auf **Details anzeigen-Tabelle**klicken. Klicken Sie auf **Bericht anzeigen**, um zum Diagramm zurückzukehren.

Sie können auch eine detailliertere Version des Berichts herunterladen, indem Sie auf Bericht anfordern klicken.

![Details-Tabelle für TLS-Verwendung im Bericht "SMTP-AUTH-Clients"](media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights-v2.md).

---
title: Beheben von Absenderdomänen Einblicken
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Administratoren erfahren mehr über die Fehlerbehebung der Absenderdomäne im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 6d98d2a2660c24a77db58215faa0de1a4a18ea1a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722882"
---
# <a name="fix-sender-domain-insight"></a>Beheben von Absenderdomänen Einblicken

> [!NOTE]
> Die in diesem Thema beschriebenen Features wurden nicht für alle Office 365-Organisationen bereitgestellt und können geändert werden.

Office 365 erfordert Nachrichten, die von internen lokalen e-Mail-Umgebungen an Office 365 gesendet werden, um bestimmte Sicherheitskriterien zu erfüllen:

- Sie haben einen eingehenden Connector in Office 365 erstellt, um SMTP-Verbindungen von Ihrem lokalen e-Mail-Server mithilfe der Quell-IP-Adresse oder eines Zertifikats zu authentifizieren.

- Sie haben ihren lokalen e-Mail-Server so konfiguriert, dass er e-Mails über Office 365 an External World weiterleitet.

- In Ihrer Konfiguration ist eine der folgenden Aussagen true:

  - Die e-Mail-Domäne des Absenders ist in Ihrer Office 365-Organisation registriert. Weitere Informationen finden Sie unter Hinzufügen von Domänen in Office 365.

  - Der lokale e-Mail-Server ist für die Verwendung eines Zertifikats zum Senden von e-Mails an Office 365 konfiguriert, das Zertifikat enthält oder genau mit einem Domänennamen übereinstimmt, den Sie in Office 365 registriert haben, und Sie haben einen zertifikatbasierten Connector in Office 365 mit dem Domänen. 

Nachrichten, die die Kriterien nicht erfüllen, werden der Organisation nicht zugeordnet und können zurückgewiesen werden.

Die Einblicke in die **Absenderdomäne von Fix** zeigen Ihnen e-Mails von Ihrer lokalen Umgebung, die nicht den Kriterien entsprechen, hilft Ihnen bei der Identifizierung potenziell gefährdeter Computer und Benutzerkonten in Ihrer lokalen e-Mail-Umgebung und unterstützt Sie bei der Durchführung Korrekturaktionen.

![Die FehlerbeHebung der Absenderdomäne im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/sender-domain-insight-selected.png)

Wenn Sie auf **Details anzeigen**klicken, werden Sie zu einem anderen Widget mit weiteren Details geführt, wie im folgenden Diagramm dargestellt:

![Das Widget "Details" in der FehlerbeHebung der Absenderdomäne](media/sender-domain-view-details.png)

Der eingehende Connector, der zum übermitteln der Nachrichten an Office 365 verwendet wurde, wird angezeigt. Sie können auch auf **Beispiel Nachrichten-IDs anzeigen** klicken, um Details zu den Nachrichten anzuzeigen, die von Ihrer lokalen e-Mail-Umgebung gesendet wurden. Da diese Nachrichten von Office 365 abgelehnt wurden, können Sie die Nachrichtenablaufverfolgung nicht verwenden, aber die Beispiel Nachrichten-IDs verwenden, um die Nachrichten in Ihrer lokalen e-Mail-Umgebung nachzuverfolgen.

![Anzeigen von Beispiel Nachrichten-IDs in der FehlerbeHebung der Absenderdomäne](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights-v2.md).

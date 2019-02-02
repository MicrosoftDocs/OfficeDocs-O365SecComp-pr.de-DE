---
title: Vergleich der Office 365 Message Encryption version
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Hilft erklären Sie die Unterschiede in der Features, die mit unterschiedlichen Versionen von Office 365 Message Encryption sowie übermittelt werden, wie die beiden weiterhin zusammenarbeiten.
ms.openlocfilehash: a418d840c7e0eb50ae076bf2b03164bef9488058
ms.sourcegitcommit: 88f3982217c29b558e3f9e838bcb425da395dd5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2019
ms.locfileid: "29708542"
---
# <a name="compare-versions-of-ome"></a>Vergleichen von Versionen von OME

In diesem Artikel werden die Vorversion Office 365 Message Encryption auf die neuen OME-Funktionen verglichen. Die neuen Funktionen werden ein Fusion und neuere Version der OME und (Information Rights Management, IRM). Wir auch behandeln wie die beiden in Office 365-Organisation vorhanden sein können.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Fachleute vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Side-by-Side-Vergleich der Features und Funktionen

|                                   |Alte features       |                   |Neue Features              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Funktion**                     | **Legacy-OME**    | **IRM**           | **Neue OME-Funktionen** |
|*Senden einer verschlüsselten e-Mail-Nachrichten*        |Über Exchange Mail Flow Regeln|Endbenutzer initiiert aus Outlook Desktop oder Outlook im Web; oder über Exchange mail Flow Regeln|Endbenutzer initiiert aus Outlook Desktop, Outlook für Mac oder Outlook im Web; über Exchange-Transportregeln und Office 365 Data Loss Prevention (DLP)|
|*Rights Management-Vorlage*       |   –      |Nicht weiterleiten Option und benutzerdefinierte Vorlagen|Führen Sie nicht weiterleiten die Option nur verschlüsseln (Option) und benutzerdefinierte Vorlagen|
|*Empfängertyp*                   |Interne und externe Empfänger|Nur interne Empfänger         |Interne und externe Empfänger|
|*Erfahrung für interne Empfänger*|Empfänger erhalten eine HTML-Nachricht, die sie herunterladen, und öffnen Sie in einem Webbrowser oder mobiler Apps|Systemeigene Inline-Erfahrung im Outlook-clients|Systemeigene Inline-Erfahrung für Office 365-Empfänger. Alle anderen Empfänger können Nachricht über OME-Portal (kein Download oder app erforderlich) lesen.|
|*Erfahrung für externe Empfänger*|Empfänger erhalten eine HTML-Nachricht, die sie herunterladen, und öffnen Sie in einem Webbrowser oder mobiler Apps|–|Systemeigene Inline-Erfahrung für Office 365-Empfänger. Alle anderen Empfänger können Nachricht über OME-Portal (kein Download oder app erforderlich) lesen.|
|*Anlage-Berechtigungen*           |Keine Einschränkungen für Anlagen|Anlagen sind geschützt.|Anlagen sind für die nicht weiterleiten Option und benutzerdefinierte Vorlagen geschützt. Administratoren können auswählen, ob Anlagen für die Option nur verschlüsseln oder nicht geschützt sind.|
|*Bringen Sie Ihre eigenen Schlüssel (BYOK)-Unterstützung*|Keine                |Keine               |BYOK unterstützt          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>Vorteile der Verwendung der neuen OME-Funktionen über ältere OME

Die neuen Funktionen bieten die folgenden Vorteile:

- Verwendung von verschlüsseln-Only (wodurch sichere Zusammenarbeit), nicht weiterleiten, als auch benutzerdefinierte Einschränkungen.
- Absender können mit den neuen Funktionen manuell aus Outlook Desktop, Outlook für Mac und Outlook auf die Webclients verschlüsselten Nachrichten senden.
- Office 365 Empfänger abrufen, um eine Inline wünschen in unterstützten Outlook-Clients verwenden. Alternativ können Administratoren auch an Office 365 Empfängern eine Branding-Benutzeroberfläche angezeigt.
- Konten außerhalb von Office 365, z. B. Gmail und Yahoo zu Microsoft-Konten, Verbundpartner sind mit dem OME-Portal, die eine höhere benutzerfreundlichkeit für diese Empfänger bereitstellt. Alle anderen Identitäten verwenden eine einmalige Kennung auf verschlüsselte Nachrichten zugreifen.
- Administratoren können branding anpassen und Erstellen von mehreren branding Vorlagen.
- Administratoren können mit den neuen Funktionen verschlüsselt-e-Mails widerrufen.
- Die neuen Funktionen bieten ausführliche Berichte über die Sicherheit &amp; Compliance Center.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Koexistenz von legacy OME und die neuen Funktionen in derselben mandantenorganisation

Sie können legacy OME und die neuen Funktionen in derselben mandantenorganisation verwenden. Als Administrator Sie zu diesem Zweck auswählen welche Version der OME, die Sie verwenden, wenn Sie Ihre e-Mail-Flussregeln erstellen möchten.

- Verwenden Sie zum Angeben der älteren Version von OME Exchange Mail Flow Regelaktion "Übernehmen die vorherige Version des OME".
- Um die neuen Funktionen zu anzugeben, verwenden Sie die Exchange Mail Flow Regel Aktion "Apply Office 365 Verschlüsselung und Rechte Nachrichtenschutz".

Benutzer können auch mit den neuen Funktionen manuell aus Outlook Desktop, Outlook für Mac und Outlook auf die Webclients verschlüsselten Nachrichten senden.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>Migrieren von älteren OME zu den neuen Funktionen

Obwohl die beiden Versionen von OME cloudverwaltungskonten vorhanden sein können, empfohlen, dass Sie Ihrer alten e-Mail-Flussregeln, mit denen die Regelaktion bearbeiten "Gelten die vorherige Version des OME" zum Verwenden der neuen Funktionen durch Angabe der e-Mail-Fluss Regelaktion "Anwenden von Office 365-Nachrichtenverschlüsselung und Schutz für Benutzerrechterichtlinien". Anweisungen finden Sie unter [Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="getting-started-with-ome"></a>Erste Schritte mit OME

In der Regel werden die neuen OME-Funktionen für Office 365-Organisation automatisch aktiviert. Wenn Sie den Einstieg in die neuen Funktionen OME innerhalb Ihrer Organisation bereit sind, finden Sie unter [Einrichten von neuen Funktionen von Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).

Die ältere Version von OME ist für Office 365-Organisation automatisch aktiviert, wenn Sie Azure Information Protection aktiviert haben. In der Vergangenheit woher legacy OME, auch wenn Azure Information Protection aktiviert war nicht. Dies ist nicht mehr die Groß-/Kleinschreibung.

Vor der Verwendung von legacy OME, wenn Sie Azure Information Protection aktiviert haben, müssen Sie, nur e-Mail-Flussregeln konfigurieren, die die Regelaktion "Übernehmen die vorherige Version des OME" verwenden. Anweisungen finden Sie unter [Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).
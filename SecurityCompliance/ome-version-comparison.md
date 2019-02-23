---
title: Office 365-Versionsvergleich für Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Erläutert die Unterschiede in den Features, die mit verschiedenen Versionen der Office 365-Nachrichtenverschlüsselung geliefert werden, sowie der Zusammenarbeit der beiden.
ms.openlocfilehash: 477fbe8f9d71bd92225a7ba5043576f164933b4e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216675"
---
# <a name="compare-versions-of-ome"></a>Vergleichen von OME-Versionen

In diesem Artikel wird die ältere Office 365-Nachrichtenverschlüsselung mit den neuen OM-Funktionen verglichen. Die neuen Funktionen sind eine Fusion und eine neuere Version von OM und Information Rights Management (IRM). Außerdem wird erläutert, wie die beiden in Ihrer Office 365-Organisation koexistieren können.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Parallele Vergleich von Features und Funktionen

|                                   |Alte Features       |                   |Neue Features              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Funktion**                     | **Legacy-OM**    | **IRM**           | **Neue OM-Funktionen** |
|*Senden einer verschlüsselten e-Mail*        |Exchange-Nachrichtenfluss Regeln|Endbenutzer, die über Outlook-Desktop oder Outlook im Web initiiert wurden; oder über Exchange-Nachrichtenfluss Regeln|Vom Outlook-Desktop, Outlook für Mac oder Outlook im Web initiierter Endbenutzer Exchange-Transport Regeln und Office 365 Data Loss Prevention (DLP)|
|*Vorlage für Rechteverwaltung*       |   Nicht zutreffend      |Option und benutzerdefinierte Vorlagen nicht weiterleiten|Option, nur verSchlüsselte Option und benutzerdefinierte Vorlagen nicht weiterleiten|
|*Empfängertyp*                   |Interne und externe Empfänger|Nur interne Empfänger         |Interne und externe Empfänger|
|*Erfahrung für interne Empfänger*|Empfänger erhalten eine HTML-Nachricht, die Sie in einem Webbrowser oder in einer mobilen app herunterladen und öffnen.|Native Inline-Erfahrung in Outlook-Clients|Native Inline Experience für Office 365-Empfänger. Alle anderen Empfänger können Nachrichten aus dem OM-Portal lesen (kein Download oder keine app erforderlich).|
|*Erfahrung für externen Empfänger*|Empfänger erhalten eine HTML-Nachricht, die Sie in einem Webbrowser oder in einer mobilen app herunterladen und öffnen.|Nicht zutreffend|Native Inline Experience für Office 365-Empfänger. Alle anderen Empfänger können Nachrichten aus dem OM-Portal lesen (kein Download oder keine app erforderlich).|
|*Anlagen Berechtigungen*           |Keine Einschränkungen für Anlagen|Anlagen sind geschützt|Anlagen sind für die Option "nicht weiterleiten" und benutzerdefinierte Vorlagen geschützt. Administratoren können auswählen, ob Anlagen für die nur-Verschlüsselung-Option geschützt sind oder nicht.|
|*Unterstützung für Ihren eigenen Schlüssel (BYOK)*|Keine                |Keine               |BYOK unterstützt          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>Vorteile der Verwendung der neuen OM-Funktionen über Legacy OM

Die neuen Funktionen bieten die folgenden Vorteile:

- Die Möglichkeit zur Verwendung von nur-Verschlüsselung (was eine sichere Zusammenarbeit ermöglicht), nicht weiterleiten und benutzerdefinierte Einschränkungen.
- Absender können e-Mails, die mit den neuen Funktionen verschlüsselt wurden, manuell über Outlook Desktop, Outlook für Mac und Outlook auf den Webclients senden.
- Office 365-Empfänger erhalten eine Inline-Erfahrung in unterstützten Outlook-Clients. Alternativ dazu können Administratoren Office 365-Empfängern eine Branded Experience anzeigen.
- Konten außerhalb von Office 365, wie Gmail-, Yahoo-und Microsoft-Konten, sind mit dem OM-Portal verbunden, was eine bessere Benutzerfreundlichkeit für diese Empfänger bietet. Alle anderen Identitäten verwenden einen einmaligen Code, um auf verschlüsselte Nachrichten zuzugreifen.
- Administratoren können Branding anpassen und mehrere Branding-Vorlagen erstellen.
- Administratoren können e-Mails, die mit den neuen Funktionen verschlüsselt wurden, widerrufen.
- Die neuen Funktionen bieten detaillierte Nutzungsberichte über das Security &amp; Compliance Center.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Koexistenz von Legacy OM und der neuen Funktionen im selben Mandanten

Sie können sowohl Legacy-OM als auch die neuen Funktionen im selben Mandanten verwenden. Als Administrator können Sie dies tun, indem Sie die Version von OM auswählen, die Sie beim Erstellen der Nachrichtenfluss Regeln verwenden möchten.

- Verwenden Sie die Exchange-Nachrichtenfluss Regelaktion "die vorherige Version von OM anwenden", um die Legacy Version von OM anzugeben.
- Um die neuen Funktionen anzugeben, verwenden Sie die Exchange-Nachrichtenfluss Regelaktion "Office 365-Nachrichtenverschlüsselung und-Rechte Schutz anwenden".

Benutzer können auch e-Mails, die mit den neuen Funktionen verschlüsselt wurden, manuell über Outlook Desktop, Outlook für Mac und Outlook auf den Webclients senden.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>Migrieren von Legacy-OM zu den neuen Funktionen

Auch wenn beide Versionen von OM koexistieren können, wird dringend empfohlen, dass Sie Ihre alten Nachrichtenfluss Regeln bearbeiten, die die Regelaktion "Anwenden der vorherigen Version von OM" verwenden, um die neuen Funktionen zu verwenden, indem Sie die e-Mail-Fluss Regelaktion "Office 365-Nachrichtenverschlüsselung anwenden und Rechte Schutz ". Anweisungen hierzu finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="getting-started-with-ome"></a>Erste Schritte mit OM

In der Regel werden die neuen OM-Funktionen automatisch für Ihre Office 365-Organisation aktiviert. Wenn Sie mit den neuen OM-Funktionen in Ihrer Organisation beginnen möchten, finden Sie weitere Informationen unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).

Die Legacy Version von OM wird für Ihre Office 365-Organisation automatisch aktiviert, wenn Sie Azure Information Protection aktiviert haben. In der Vergangenheit hat Legacy-OM auch dann funktioniert, wenn Azure Information Protection nicht aktiviert wurde. Dies ist nicht mehr der Fall.

Um die Verwendung von Legacy OM zu starten, wenn Sie Azure Information Protection aktiviert haben, müssen Sie nur Nachrichtenfluss Regeln konfigurieren, die die Regelaktion "Anwenden der vorherigen Version von OM" verwenden. Anweisungen hierzu finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).
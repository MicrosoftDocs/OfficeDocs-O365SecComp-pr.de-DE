---
title: Versionsvergleich für Office 365 Message Encryption (OM)
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Erläutert die Unterschiede zwischen den Features, die mit verschiedenen Versionen der Office 365-Nachrichtenverschlüsselung geliefert werden und wie die beiden weiterhin zusammenarbeiten.
ms.openlocfilehash: bb13208e2b630c8a6217b78b48a4cd3bb4b0de79
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262327"
---
# <a name="compare-versions-of-ome"></a>Vergleichen von OME-Versionen

In diesem Artikel wird die ältere Office 365-Nachrichtenverschlüsselung (OM) mit den neuen OM-Funktionen verglichen. Die neuen Funktionen sind eine Fusion und neuere Version von OM und Information Rights Management (IRM). Auch die eindeutigen Merkmale der Bereitstellung in GCC High werden erläutert. Außerdem wird erläutert, wie die beiden in Ihrer Office 365-Organisation koexistieren können.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Parallele Vergleich von Features und Funktionen

|                                   |Alte Features       |                   |Neue Features              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Funktion**                     | **Legacy-OM**    | **IRM**           | **Neue OM-Funktionen** |
|*Senden einer verschlüsselten e-Mail*        |Exchange-Nachrichtenfluss Regeln|Endbenutzer, die über Outlook-Desktop oder Outlook im Web initiiert wurden; oder über Exchange-Nachrichtenfluss Regeln|Vom Outlook-Desktop, Outlook für Mac oder Outlook im Web initiierter Endbenutzer Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) und Office 365 Data Loss Prevention (DLP)|
|*Vorlage für Rechteverwaltung*       |   Nicht zutreffend      |Option und benutzerdefinierte Vorlagen nicht weiterleiten|Option, nur verSchlüsselte Option und benutzerdefinierte Vorlagen nicht weiterleiten|
|*Empfängertyp*                   |Interne und externe Empfänger|Nur interne Empfänger         |Interne und externe Empfänger|
|*Erfahrung für interne Empfänger*|Empfänger erhalten eine HTML-Nachricht, die Sie in einem Webbrowser oder in einer mobilen app herunterladen und öffnen.|Native Inline-Erfahrung in Outlook-Clients|Native Inline Experience für Office 365-Empfänger. Alle anderen Empfänger können Nachrichten aus dem OM-Portal lesen (kein Download oder keine app erforderlich).|
|*Erfahrung für externen Empfänger*|Empfänger erhalten eine HTML-Nachricht, die Sie in einem Webbrowser oder in einer mobilen app herunterladen und öffnen.|Nicht zutreffend|Native Inline Experience für Office 365-Empfänger. Alle anderen Empfänger können Nachrichten aus dem OM-Portal lesen (kein Download oder keine app erforderlich).|
|*Anlagen Berechtigungen*           |Keine Einschränkungen für Anlagen|Anlagen sind geschützt|Anlagen sind für die Option "nicht weiterleiten" und benutzerdefinierte Vorlagen geschützt. Administratoren können auswählen, ob Anlagen für die nur-Verschlüsselung-Option geschützt sind oder nicht.|
|*Unterstützung für Ihren eigenen Schlüssel (BYOK)*|Keine                |Keine               |BYOK unterstützt          |
||

## <a name="advantages-of-the-new-ome-capabilities-over-legacy-ome"></a>Vorteile der neuen OM-Funktionen gegenüber Legacy OM

Die neuen Funktionen bieten die folgenden Vorteile:

- Möglichkeit zur Verwendung von nur-Verschlüsselungs-(was eine sichere Zusammenarbeit ermöglicht), nicht weiterleiten und benutzerdefinierte Einschränkungen.
- Absender können e-Mails, die mit den neuen Funktionen verschlüsselt wurden, manuell über Outlook Desktop, Outlook für Mac und Outlook auf den Webclients senden.
- Office 365-Empfänger erhalten eine Inline-Erfahrung in unterstützten Outlook-Clients. Alternativ dazu können Administratoren Office 365-Empfängern eine Branded Experience anzeigen.
- Konten außerhalb von Office 365, wie Gmail-, Yahoo-und Microsoft-Konten, sind mit dem OM-Portal verbunden, was eine bessere Benutzerfreundlichkeit für diese Empfänger bietet. Alle anderen Identitäten verwenden einen einmaligen Code, um auf verschlüsselte Nachrichten zuzugreifen.
- Administratoren können Branding anpassen und mehrere Branding-Vorlagen erstellen.
- Administratoren können e-Mails, die mit den neuen Funktionen verschlüsselt wurden, widerrufen.
- Die neuen Funktionen bieten detaillierte Nutzungsberichte über das Security &amp; Compliance Center.

## <a name="unique-characteristics-of-office-365-message-encryption-in-a-gcc-high-deployment"></a>Eindeutige Merkmale der Office 365-Nachrichtenverschlüsselung in einer GCC-hohen Bereitstellung

Wenn Sie planen, die Office 365-Nachrichtenverschlüsselung in einer GCC-Umgebung zu verwenden, gibt es einige eindeutige Merkmale der Empfänger Oberfläche.

### <a name="encrypted-email-from-gcc-high-to-gcc-high-recipients"></a>VerSchlüsselte e-Mail vom GCC hoch zu GCC High Recipients

Absender können e-Mails in Outlook für PC und Mac und Outlook im Web manuell verschlüsseln, oder Organisationen können eine Richtlinie einrichten, um e-Mails mithilfe von Exchange-Nachrichtenfluss Regeln zu verschlüsseln.

Empfänger in GCC High erhalten dieselbe Inline Leseerfahrung in Outlook für PC und Mac und Outlook im Web wie alle anderen Office 365-Benutzer.

### <a name="encrypted-email-from-gcc-high-to-non-gcc-high-recipients"></a>VerSchlüsselte e-Mail vom GCC hoch an nicht-GCC-hohe Empfänger

Absender in GCC High können verschlüsselte e-Mails außerhalb der GCC-Obergrenze senden.

Alle Empfänger außerhalb des GCC-hoch, einschließlich kommerzieller Office 365-Benutzer, Outlook.com-Benutzer und anderer Benutzer anderer e-Mail-Anbieter wie Gmail und Yahoo, erhalten eine Wrapper-e-Mail, die den Empfänger an das OM-Portal weiterleitet, in dem der Empfänger lesen und auf Nachricht antworten.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Koexistenz von Legacy OM und der neuen Funktionen im selben Mandanten

Sie können sowohl Legacy-OM als auch die neuen Funktionen im selben Mandanten verwenden. Als Administrator können Sie dies tun, indem Sie die Version von OM auswählen, die Sie beim Erstellen der Nachrichtenfluss Regeln verwenden möchten.

- Verwenden Sie die Exchange-Nachrichtenfluss Regelaktion, um die **frühere**Version von OM anzugeben.
- Um die neuen Funktionen anzugeben, verwenden Sie die Exchange-Nachrichtenfluss Regelaktion **wenden Sie Office 365 Nachrichtenverschlüsselung und Rechte Schutz**an.

Benutzer können e-Mails, die mit den neuen Funktionen von Outlook Desktop, Outlook für Mac und Outlook im Web verschlüsselt wurden, manuell senden.

## <a name="migrate-from-legacy-ome-to-the-new-capabilities"></a>Migrieren von Legacy-OM zu den neuen Funktionen

Auch wenn beide Versionen von OM koexistieren können, wird dringend empfohlen, dass Sie Ihre alten Nachrichtenfluss Regeln bearbeiten, die mit der Regelaktion **die frühere Version von OM anwenden** , um die neuen Funktionen zu verwenden. Diese Regeln aktualisieren um die e-Mail-Fluss Regelaktion zu verwenden, **wenden Sie Office 365 Nachrichtenverschlüsselung und Rechte Schutz**an. Anweisungen hierzu finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="get-started-with-ome"></a>Erste Schritte mit OM

In der Regel werden die neuen OM-Funktionen automatisch für Ihre Office 365-Organisation aktiviert. Weitere Informationen zu den neuen OM-Funktionen in Ihrer Organisation finden Sie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).

Die Legacy Version von OM wird für Ihre Office 365-Organisation automatisch aktiviert, wenn Sie Azure Information Protection aktiviert haben. In der Vergangenheit hat Legacy-OM auch dann funktioniert, wenn Azure Information Protection nicht aktiviert wurde. Dies ist nun nicht mehr der Fall.

Um Legacy OM zu verwenden, wenn Sie Azure Information Protection aktiviert haben, müssen Sie einfach Nachrichtenfluss Regeln konfigurieren, die die Regelaktion verwenden **die vorherige Version von OM anwenden**. Anweisungen hierzu finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).
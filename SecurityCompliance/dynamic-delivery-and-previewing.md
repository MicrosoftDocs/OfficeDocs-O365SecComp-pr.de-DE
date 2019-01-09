---
title: Dynamische Übermittlung und Anzeigen der Vorschau mit Office 365 ATP sichere Anlagen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Wenn Sie Ihre ATP sichere Anlagen Richtlinien eingerichtet haben, wählen Sie dynamische Übermittlung Nachricht Verzögerungen bei der vermieden, und aktivieren Personen für die Vorschau von Anlagen, die gescannt werden.
ms.openlocfilehash: 95c270e871c3febb13eef8c4374d996fc763315b
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769829"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a>Dynamische Übermittlung und Anzeigen der Vorschau mit Office 365 ATP sichere Anlagen

**Zusammenfassung**: Dynamische Übermittlung ist eine Option, die für [Sichere Anlagen ATP](atp-safe-attachments.md)ausgewählt werden kann. In diesem Artikel erfahren Sie mehr über dynamische Übermittlung und Anlage Preview-Funktionen in [ATP sichere Anlagen in Office 365](atp-safe-attachments.md)zu lesen.

Wenn [Richtlinien ATP sichere Anlagen eingerichtet sind](set-up-atp-safe-attachments-policies.md) für Ihre Organisation mehrere Optionen für die Behandlung von e-Mail-Anlagen vorhanden sind. Dazu gehören **Blockieren**, **Ersetzen**und **Dynamische Übermittlung**. Je nach der Richtlinien für sichere Anlagen ATP Konfiguration möglicherweise e-Mail-Empfänger eine geringfügige Verzögerung in e-Mail-Übermittlung bemerken, wenn deren Anhänge überprüft werden. Wählen Sie zum Vermeiden von Nachricht verzögert **Dynamische Übermittlung**.
  
## <a name="how-dynamic-delivery-works"></a>Funktionsweise von dynamische Übermittlung
  
Dynamische Übermittlung entfällt e-Mail Verzögerungen durch den Textkörper einer e-Mail-Nachricht über an den Empfänger mit einem Platzhalter für jede e-Mail-Anlage senden. Der Platzhalter bleibt, bis eine Kopie der Anlage überprüft und sicher durch [ATP sichere Anlagen](atp-safe-attachments.md)bestimmt ist. 

- Jede Anlage deaktiviert ist, steht er öffnen oder herunterladen. 

- Wenn eine Anlage böswilligen werden bestimmt wird, wird es zur Quarantäne, gesendet, in dem eine Person in Ihrer Organisation Security Team (wie ein globaler Office 365-Administrator oder Sicherheitsadministrator) können [Nachrichten in Quarantäne in Office 365 verwalten](manage-quarantined-messages-and-files.md).

Die meisten PDF-Dateien und Office während ATP Überprüfung ausgeführt wird, können Dokumente im abgesicherten Modus angezeigt werden. Wenn eine Anlage nicht kompatibel mit der dynamischen Delivery-Vorschau ist, sehen erst, e-Mail-Empfänger einen Anlage Platzhalter ATP sichere Anlagen Überprüfung abgeschlossen ist.

Mit der dynamischen Übermittlung Personen gelesen und reagieren auf ihre e-Mail-Nachrichten sofort, während die Anlagen analysiert werden. 

ATP sichere Anlagen scannen akzeptiert platzieren im selben Bereich, in dem sich Ihre Office 365-Daten befinden. Weitere Informationen zum Data Center Geografie, finden Sie unter [, wo wird Ihre Daten befinden?](https://products.office.com/where-is-your-data-located?geo=All) 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a>Was geschieht, wenn jemand einer e-Mail, weiterleitet enthält eine Anlage?

Nehmen Sie an, dass eine Organisation dynamische Übermittlung für die [sichere Anlagen ATP-Richtlinie](set-up-atp-safe-attachments-policies.md), und eine Person empfängt eine e-Mail, die eine Anlage enthält. Nun nehmen Sie an die Person die e-Mail-Nachricht an eine andere Person weiterleitet. Was ist los? Das hängt davon ab, ob die zusätzliche Empfänger in ATP sichere Anlagen Richtlinien enthalten sind.
  
- Wenn Sie ein Empfänger über eine sichere Anlagen ATP-Richtlinie mit der Option dynamische Übermittlung sind, sieht der Empfänger den Platzhalter die Möglichkeit, kompatible Dateien eine Vorschau anzeigen.
    
- Wenn Sie ein Empfänger nicht durch eine Richtlinie ATP sichere Anlagen behandelt wird, werden dann der e-Mail- und die Anlage, ohne ATP sichere Anlagen scannen oder Anlage Platzhalter durchlaufen.
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a>Erforderlich für dynamische Übermittlung funktioniert?

- Ihre Organisation muss [Office 365 erweiterte Schutz](office-365-atp.md) verfügen.
    
- Richtlinien müssen für sichere ATP-Anlagen mit der Option dynamische Übermittlung (finden Sie unter [Set up ATP sichere Anlagen Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)) definiert werden
    
- E-Mail von Ihrer Organisation muss in Office 365 gehostet werden
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a>Gibt es Szenarien für die dynamische Übermittlung nicht verfügbar ist?

Es gibt bestimmte Szenarien, in denen dynamische Übermittlung nicht unterstützt wird. Hierzu gehören die folgenden:
  
- E-Mail-Nachrichten in öffentlichen Ordnern
    
- E-Mail-Nachrichten, die nicht weitergeleitet werden und dann wieder in das Postfach des Benutzers mithilfe von benutzerdefinierten Regeln
    
- E-Mail-Nachrichten (automatisch oder manuell) aus dem gehosteten Postfach und in anderen Standorten, einschließlich Archivordner verschoben werden
    
- E-Mail-Nachrichten, die gelöscht werden
    
- Ordner eines Benutzers Postfach suchen, die in einen fehlerhaften Zustand befindet
    
- Umgebungen, in denen ein Exchange Online-Administrator Exclaimer aktiviert hat. Um dieses Problem zu beheben, finden Sie unter [Nachrichten mit Anlagen werden nicht zugestellt werden, wenn ATP dynamische Übermittlung und Exclaimer verwendet werden](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)

- Verschlüsselte Nachrichten mit [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))
    

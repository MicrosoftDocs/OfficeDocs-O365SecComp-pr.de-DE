---
title: Dynamische bereit-und Vorschau mit Office 365 ATP Safe Attachments
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/19/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Bei der Einrichtung Ihrer Richtlinien für sichere ATP-Anlagen wählen Sie dynamische Übermittlung aus, um Verzögerungen bei Nachrichten zu vermeiden und Personen eine Vorschau der zu überprüfenden Anhänge zu ermöglichen.
ms.openlocfilehash: 567b5f0c5bc75123169073bf5dc33de191187846
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958566"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a>Dynamische bereit-und Vorschau mit Office 365 ATP Safe Attachments

## <a name="overview"></a>Übersicht

Die dynamische Bereitstellung kann für [ATP Safe Attachments](atp-safe-attachments.md)ausgewählt werden. Lesen Sie diesen Artikel, um mehr über dynamische zuBereitungen und Anlagenvorschau Funktionen in [ATP Safe Attachments in Office 365](atp-safe-attachments.md)zu erfahren.

Wenn Sie [Richtlinien für sichere Anlagen für ATP](set-up-atp-safe-attachments-policies.md) für Ihre Organisation einrichten, gibt es mehrere Optionen für die Behandlung von e-Mail-Anlagen. Hierzu gehört das **blockieren**, **ersetzen**und die **dynamische Bereitstellung**. Je nach Konfiguration von ATP-Richtlinien für sichere Anlagen können e-Mail-Empfänger bei der Überprüfung ihrer Anlagen möglicherweise eine kleine Verzögerung bei der e-Mail-Zusendung erfahren. Um Verzögerungen bei Nachrichten zu vermeiden, wählen Sie **dynamische Übermittlung**.
  
## <a name="how-dynamic-delivery-works"></a>Funktionsweise der dynamischen zuSendung
  
Die dynamische Zustellung verhindert e-Mail-Verzögerungen, indem der Textkörper einer e-Mail-Nachricht an den Empfänger mit einem Platzhalter für jede e-Mail-Anlage gesendet wird. Der Platzhalter bleibt so lange erhalten, bis eine Kopie der Anlage gescannt und durch [ATP Safe Attachments](atp-safe-attachments.md)sichergestellt wird. 

- Jeder Anhang kann geöffnet oder heruntergeladen werden. 

- Wenn eine Anlage als bösartig festgelegt wird, wird Sie an die Quarantäne gesendet, in der eine Person im Sicherheitsteam Ihrer Organisation (beispielsweise ein globaler Office 365-Administrator oder Sicherheitsadministrator) [isolierte Nachrichten in office 365 verwalten](manage-quarantined-messages-and-files.md)kann.

Die meisten PDFs und Office-Dokumente können während der ATP-Überprüfung im abgesicherten Modus angezeigt werden. Wenn eine Anlage nicht mit der dynamischen zuStellungs Vorschau kompatibel ist, wird den e-Mail-Empfängern ein Anlagen Platzhalter angezeigt, bis die Überprüfung der ATP Safe Attachments abgeschlossen ist.

> [!TIP]
> Wenn Sie ein mobiles Gerät verwenden und PDFs zunächst nicht in der Vorschau für die dynamische Lieferung gerendert werden, versuchen Sie, sich mit Ihrem mobilen Browser bei Office 365 anzumelden.

Bei der dynamischen Bereitstellung können Personen sofort lesen und auf Ihre e-Mail-Nachrichten Antworten, während Ihre Anlagen analysiert werden. 

Die Überprüfung von ATP Safe Attachments erfolgt in derselben Region, in der sich Ihre Office 365-Daten befinden. Weitere Informationen zur Geografie des Rechenzentrums finden Sie unter [wo befinden sich Ihre Daten?](https://products.office.com/where-is-your-data-located?geo=All) 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a>Was geschieht, wenn jemand eine e-Mail weiterleitet, die eine Anlage enthält?

Angenommen, eine Organisation verwendet die dynamische Bereitstellung für Ihre [ATP-Richtlinie für sichere Anlagen](set-up-atp-safe-attachments-policies.md), und jemand erhält eine e-Mail, die eine Anlage enthält. Nehmen wir an, diese Person leitet die e-Mail-Nachricht an einen anderen weiter. Was ist los? Es hängt davon ab, ob die zusätzlichen Empfänger in den Richtlinien für ATP Safe Attachments enthalten sind.
  
- Wenn ein Empfänger von einer Richtlinie für sichere Anlagen mit ATP-Datenträgern unter Verwendung der Option für die dynamische Lieferung abgedeckt wird, sieht der Empfänger den Platzhalter mit der Möglichkeit, eine Vorschau der kompatiblen Dateien anzuzeigen.
    
- Wenn ein Empfänger nicht durch eine ATP-Richtlinie für sichere Anlagen abgedeckt wird, werden die e-Mail und die Anlage durchlaufen, ohne dass ein ATP Safe Attachments-oder Attachment-Platzhalter verwendet wird.
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a>Was ist erforderlich, damit die dynamische bereitgestellt wird?

- Ihre Organisation muss [Office 365 Advanced Threat Protection](office-365-atp.md) besitzen.
    
- Richtlinien müssen für ATP-sichere Anlagen mithilfe der Option für die dynamische Bereitstellung definiert werden (siehe [Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md))
    
- Die e-Mail Ihrer Organisation muss in Office 365 gehostet werden. Obwohl [office 365 Advanced Threat Protection mit einem beliebigen SMTP-e-Mail-Übertragungs-Agent](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#requirements-for-office-365-advanced-threat-protection-atp) (beispielsweise Exchange Server) verwendet werden kann, erfordert die Option für die dynamische Übermittlung für sichere ATP-Anhänge, dass die e-Mails Ihrer Organisation in Office 365 gehostet werden. Wenn Ihre e-Mail-Adresse nicht in Office 365 gehostet wird, wählen Sie eine andere [Richtlinienoption für ATP Safe Attachments](set-up-atp-safe-attachments-policies.md#step-3-learn-about-atp-safe-attachments-policy-options), wie zum Beispiel " **blockieren**".
    
## <a name="additional-considerations"></a>Zusätzliche Überlegungen

Es gibt bestimmte Szenarien, in denen die dynamische Bereitstellungen nicht unterstützt werden. Hierzu gehören:
  
- E-Mail-Nachrichten in öffentlichen Ordnern
    
- E-Mail-Nachrichten, die mithilfe benutzerdefinierter Regeln aus dem Postfach des Benutzers weitergeleitet werden
    
- E-Mail-Nachrichten, die (automatisch oder manuell) aus dem gehosteten Postfach und an andere Speicherorte verschoben werden, einschließlich Archivordnern
    
- Gelöschte e-Mail-Nachrichten
    
- Der Post Fach Suchordner eines Benutzers im Fehlerzustand
    
- Umgebungen, in denen ein Exchange Online-Administrator den ausforderungs Server aktiviert hat. Weitere Informationen finden Sie unter [Nachrichten mit Anlagen werden nicht übermittelt, wenn die dynamische Bereitstellung von ATP und](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery) des Ausweises verwendet wird.

- Mit [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md)verSchlüsselte Nachrichten

- In Fällen, in denen die dynamische bereit Position nicht unterstützt wird, werden e-Mail-Nachrichten von ATP Safe-Anlagen nicht überprüft. Die Übermittlung von e-Mail-Nachrichten mit Anlagen, die URLs enthalten, wird jedoch überprüft, je nachdem, wie Ihre [ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md) konfiguriert werden. In diesen Fällen werden URLs in e-Mail-Nachrichten und Office-Dateien überprüft.

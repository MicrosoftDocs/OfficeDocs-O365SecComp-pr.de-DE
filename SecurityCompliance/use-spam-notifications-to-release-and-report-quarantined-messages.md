---
title: Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/14/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Wenn Ihr Administrator die Benachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach gesendete Nachrichten auflistet, die als Spam, Massen oder Phishing-Nachrichten identifiziert wurden. Sie können Nachrichten nach der Benachrichtigung freigeben oder melden.
ms.openlocfilehash: de67987b0028102bdf61889ce54ca4215182e279
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2019
ms.locfileid: "30638972"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a>Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365

Wenn Ihr Administrator Spambenachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach adressierte Nachrichten auflistet, die als Spam identifiziert und stattdessen isoliert wurden.
  
> [!TIP]
> Wenn Sie ein Administrator sind und dieses Feature aktivieren möchten, können Sie die Option auswählen, wenn Sie [eine standardmäßige Antispampolitik ändern](https://go.microsoft.com/fwlink/?LinkId=800313). 
  
Die Nachricht, die Sie erhalten, enthält die Anzahl von Nachrichten in Spamquarantäne und das Datum und die Uhrzeit (in UTC) der letzten Nachricht in der Liste. Die Liste enthält für jede Nachricht Folgendes:
  
- **Absender** Der Absender Name und die e-Mail-Adresse der isolierten Nachricht. 
    
- **Betreff** Der Betreffzeilentext der in Quarantäne verschobenen Nachricht. 
    
- **Datum** Datum und Uhrzeit (UTC-Angabe) der Verschiebung der Nachricht in Quarantäne. 
    
- **Größe** Die Größe der Nachricht in Kilobyte (KBs). 
    
Dies sind die Aktionen, die Sie mit einer isolierten Nachricht ausführen können:

- Zeigen Sie eine **Vorschau** der Nachricht an, wenn Sie eine Vorschau des Inhalts oder der Kopfzeile vor der Aktion anzeigen möchten.

- **Laden** Sie die Nachricht herunter, wenn Sie die Nachricht und die Anhänge (falls vorhanden) auf Ihrem Gerät vor der Aktion überarbeiten möchten.

- **Release** , wenn es sich bei der Nachricht nicht um Spam handelt und Sie möchten, dass Office 365 die Nachricht an Ihr Postfach sendet.

- **Release _AMP_ Allow Absender** , wenn die Nachricht nicht Spam ist und Sie möchten, dass Office 365 den Absender zur Liste sicherer Absender und Empfänger für zukünftige e-Mails hinzufügt. Denken Sie daran, dass Ihr Administrator möglicherweise andere organisationsweite Allow/Block-Konfigurationen besitzt, die Ihre Liste sicherer Absender außer Kraft setzen.

- **Veröffentlichen Sie _AMP_ Bericht**, wenn es sich bei der Nachricht nicht um Spam handelt und Sie die Nachricht an Ihr Postfach senden und zu Analyseberichten möchten.

- **Blockieren** Wenn Sie möchten, dass Office 365 den Absender zu Ihrer Liste blockierter Absender hinzufügt.

Beachten Sie Folgendes:
  
- Nachrichten, die unter Quarantäne gestellt werden, da Sie mit einer Nachrichtenfluss Regel übereinstimmen, sind nicht in Benutzer isolierten Nachrichten enthalten. Es werden nur Spamquarantäne-Nachrichten aufgeführt.
    
- Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.
    


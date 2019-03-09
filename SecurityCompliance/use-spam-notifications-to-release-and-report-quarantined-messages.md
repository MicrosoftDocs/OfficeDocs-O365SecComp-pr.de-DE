---
title: Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
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
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492724"
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
    
Derzeit gibt es zwei Aktionen, die Sie mit einer isolierten Nachricht durchführen können:
  
- Im **Posteingang freigeben** Wählen Sie diese Option aus, um die Nachricht an Ihren Posteingang zu senden, wo Sie Sie anzeigen können. 
    
- **Bericht als nicht-Junk** Wählen Sie diese Option aus, um eine Kopie der Nachricht zur Analyse an Microsoft zu senden. Das Spamteam bewertet und analysiert die Nachricht und passt, je nach Analyseergebnis, die Antispamfilterregeln so an, dass die Nachricht übergeben wird. 
    
Beachten Sie Folgendes:
  
- Nachrichten, die unter Quarantäne gestellt werden, da Sie mit einer Nachrichtenfluss Regel übereinstimmen, sind nicht in Benutzer isolierten Nachrichten enthalten. Es werden nur Spamquarantäne-Nachrichten aufgeführt.
    
- Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.
    


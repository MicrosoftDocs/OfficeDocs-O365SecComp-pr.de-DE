---
title: Funktionsweise von Office 365 ATP-Sicherheits Links
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Das Feature "sichere Links" bietet eine Zeit-für-Mausklick-Überprüfung von Hyperlinks in Office-Dokumenten und e-Mail-Nachrichten. Lesen Sie diesen Artikel, um zu erfahren, wie ATP-sichere Links funktionieren.
ms.openlocfilehash: 67779560e279028c158179c265196199b5d37d1c
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2019
ms.locfileid: "35792041"
---
# <a name="how-office-365-atp-safe-links-works"></a>Funktionsweise von Office 365 ATP-Sicherheits Links
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>So funktioniert ATP-sichere Links mit URLs in e-Mails

Auf einer hohen Ebene funktioniert der Schutz für [ATP-sichere Links](atp-safe-links.md) für URLs in e-Mails (in Office 365 gehostet, nicht lokal):
  
1. Personen erhalten e-Mail-Nachrichten, von denen einige URLs enthalten.
    
2. Alle e-Mails werden Exchange Online Schutz durchlaufen, wobei IP-und Briefumschlag Filter, signaturbasierter Malware Schutz, Antispam-und Antischadsoftware-Filter angewendet werden. 
    
3. E-Mail kommt in Postfächern der Benutzer.
    
4. Ein Benutzer meldet sich bei Office 365 an und wechselt in den e-Mail-Posteingang.
    
5. Der Benutzer öffnet eine e-Mail-Nachricht und klickt auf eine URL in der e-Mail-Nachricht.
    
6. Das Feature "ATP-sichere Links" überprüft die URL unmittelbar vor dem Öffnen der Website. Die URL wird als blockiert, bösartig oder sicher identifiziert.
    
    - Wenn die URL zu einer Website gehört, die in einer [benutzerdefinierten Liste "nicht umschreiben"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird die Website geöffnet. 
    
    - Wenn die URL zu einer Website gehört, die in der [Liste benutzerdefinierte blockierte URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)der Organisation enthalten ist, wird eine [Warn Seite](atp-safe-links-warning-pages.md) geöffnet. 
    
    - Wenn die URL zu einer Website gehört, die als bösartig eingestuft wurde, wird eine [Warn Seite](atp-safe-links-warning-pages.md) geöffnet. 
    
    - Wenn die URL zu einer herunterladbaren Datei wechselt und die [Richtlinien für ATP-sichere Links](set-up-atp-safe-links-policies.md) in Ihrer Organisation für die Überprüfung solcher Inhalte konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
    - Wenn die URL als sicher eingestuft wird, wird die Website geöffnet.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>So funktioniert ATP-sichere Links mit URLs in Office-Dokumenten

Auf hohem Niveau funktioniert der Schutz von [ATP-Links](atp-safe-links.md) für URLs in Office 365 ProPlus-Anwendungen (aktuelle Versionen von Word, Excel und PowerPoint unter Windows oder Mac, Office-Apps auf IOS-oder Android-Geräten, Visio unter Windows, OneNote in einem Browser und Office in einem Browser):
  
1. Benutzer haben Office 365 ProPlus auf Ihrem Computer, Smartphone oder Tablet installiert. (Oder Sie verwenden Office in Ihrem Browser.)
    
2. Ein Benutzer öffnet ein Word-, Excel-, PowerPoint-oder Visio-Konto und meldet sich bei Office 365 Enterprise mithilfe seines Arbeits-oder Schul Kontos an. Das Dokument enthält URLs.
    
3. Wenn der Benutzer auf eine URL im Dokument klickt, wird der Link vom ATP-Dienst für sichere Links überprüft.
    
      - Wenn die URL zu einer Website gehört, die in einer [benutzerdefinierten Liste "nicht umschreiben"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird dieser Benutzer zur Website geleitet. 
    
      - Wenn die URL zu einer Website gehört, die in der [Liste benutzerdefinierte blockierte URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)der Organisation enthalten ist, wird der Benutzer zu einer [Warnungsseite](atp-safe-links-warning-pages.md)geleitet.
    
      - Wenn die URL zu einer Website gehört, die als bösartig eingestuft wurde, wird der Benutzer zu einer [Warnungsseite](atp-safe-links-warning-pages.md)geleitet.
    
      - Wenn die URL zu einer herunterladbaren Datei wechselt und die [Richtlinien für ATP-sichere Links](set-up-atp-safe-links-policies.md) für die Überprüfung solcher Downloads konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
      - Wenn die URL als sicher eingestuft wird, wird der Benutzer zur Website geleitet.


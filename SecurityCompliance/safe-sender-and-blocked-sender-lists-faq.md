---
title: Listen sicherer und blockierter Absender in Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
ms.collection:
- M365-security-compliance
description: Als Exchange Online- oder Exchange Online Protection-Administrator (EOP) können Sie sicherstellen, dass eine E-Mail-Nachricht, die den Dienst durchläuft, nicht als Spam gekennzeichnet wird. Eine Möglichkeit hierzu ist das Erstellen von Listen mit sicheren Absendern und blockierten Absendern für die Personen in Ihrer Organisation.
ms.openlocfilehash: 11ae38733418bb0842732978512698ca6a6274fd
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692224"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a>Listen sicherer und blockierter Absender in Exchange Online

Als Exchange Online- oder Exchange Online Protection-Administrator (EOP) können Sie sicherstellen, dass eine E-Mail-Nachricht, die den Dienst durchläuft, nicht als Spam gekennzeichnet wird. Eine Möglichkeit hierzu ist das Erstellen von Listen mit sicheren Absendern und blockierten Absendern für die Personen in Ihrer Organisation. 
  
 *Informationen zum Verwenden dieser Listen als Administrator finden Sie in der aktuellen Version der Tipps und Verfahren unter* [Verhindern der Kennzeichnung von falsch positiver E-Mail als Spam mithilfe einer Liste sicherer Adressen oder anderer Techniken](https://go.microsoft.com/fwlink/p/?LinkID=534224). 
  
Wenn Sie kein Administrator sind und einfach nur Ihre eigenen Junk-E-Mails in Outlook mithilfe einer Liste sicherer Absender verwalten möchten, sehen Sie sich die Schritte in diesem Überblick [der Junk-Filter](https://go.microsoft.com/fwlink/?LinkId=817222) an. 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a>Was sind die Grenzwerte sicherer und blockierter Absender in Exchange Online?

Die Grenzwerte sicherer und blockierter Absender in Exchange Online unterscheiden sich von den Grenzwerten von Active Directory und Outlook. Dies sind:
  
- Grenzwert sicherer Absender: 1.024
    
- Grenzwert blockierter Absender: 500
    
Hinweis:
  
Möglicherweise tritt der in [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app)beschriebene Fehler auf. Um dieses Problem zu beheben, deaktivieren Sie das Kontrollkästchen „E-Mails von meinen Kontakten vertrauen". Alternativ können Sie die Anzahl von e-Mail-Adressen im Standardordner Kontakte verringern, um Sie innerhalb des maximal zulässigen Grenzwerts von 1024 in Exchange Online zu übertragen, der für das Attribut "Parameter MaxSafeSenders" festgelegt ist. Weitere Informationen über dieses Attribut und das Cmdlet „Set-Mailbox" finden Sie in dem folgenden Artikel:
  
[Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox)
  
## <a name="see-also"></a>Siehe auch

[Sender filtering in Exchange 2016](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)


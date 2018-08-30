---
title: Listen sicherer und blockierter Absender in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Als Exchange Online- oder Exchange Online Protection-Administrator (EOP) können Sie sicherstellen, dass eine E-Mail-Nachricht, die den Dienst durchläuft, nicht als Spam gekennzeichnet wird. Eine Möglichkeit hierzu ist das Erstellen von Listen mit sicheren Absendern und blockierten Absendern für die Personen in Ihrer Organisation.
ms.openlocfilehash: cbf886bdcc40044a31b285b6806aecbc95f0f97c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003104"
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
  
Möglicherweise tritt der in KB 2590466 beschriebene Fehler auf (Die folgende Fehlermeldung wird in Outlook Web App für Exchange Server 2010 angezeigt: „Junk-E-Mail-Überprüfungsfehler"). Um dieses Problem zu beheben, deaktivieren Sie das Kontrollkästchen „E-Mails von meinen Kontakten vertrauen". Alternativ können Sie auch die Anzahl an E-Mail-Adressen reduzieren, die in dem standardmäßigen Ordner „Kontakte" enthalten sind, damit dieser Wert nicht den Grenzwert von 1.024 in Exchange Online überschreitet, der für das Attribut „MaxSafeSenders" festgelegt ist. Weitere Informationen über dieses Attribut und das Cmdlet „Set-Mailbox" finden Sie in dem folgenden Artikel:
  
[Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a>See also

[Sender filtering in Exchange 2016](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)


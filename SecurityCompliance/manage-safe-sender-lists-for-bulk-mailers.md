---
title: Verwalten sicherer Absenderlisten für Absender von Massen-E-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: 'Wenn Sie Listen sicherer Absender verwenden möchten, sollten Sie wissen, dass die Verarbeitung in Exchange Online Protection (EOP) und Outlook auf verschiedene Weise erfolgt. Der Dienst berücksichtigt sichere Absender und Domänen, indem er die RFC 5321.MailFrom-Adresse und die RFC 5322.From-Adresse prüft, während Outlook die RFC 5322.From-Adresse zur Liste sicherer Absender eines Benutzers hinzufügt. (Anmerkung: Der Dienst prüft sowohl die 5321.MailFrom-Adresse als auch die 5322.From-Adresse auf blockierte Absender und Domänen.)'
ms.openlocfilehash: 27d635ec93dd04df8ebf22d5d3d8f8ead4b7bcf8
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276135"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>Verwalten sicherer Absenderlisten für Absender von Massen-E-Mails

Wenn Sie Listen sicherer Absender verwenden möchten, sollten Sie wissen, dass die Verarbeitung in Exchange Online Protection (EOP) und Outlook auf verschiedene Weise erfolgt. Der Dienst berücksichtigt sichere Absender und Domänen, indem er die RFC 5321.MailFrom-Adresse und die RFC 5322.From-Adresse prüft, während Outlook die RFC 5322.From-Adresse zur Liste sicherer Absender eines Benutzers hinzufügt. (Anmerkung: Der Dienst prüft sowohl die 5321.MailFrom-Adresse als auch die 5322.From-Adresse auf blockierte Absender und Domänen.)
  
Die Adresse SMTP MAIL FROM, auch als RFC 5321.MailFrom-Adresse bekannt, ist die E-Mail-Adresse, die zur Durchführung von SPF-Prüfungen verwendet wird, und, wenn die E-Mail nicht zugestellt werden kann, der Pfad, an den die unzustellbare Nachricht gesendet wird. Es ist diese E-Mail-Adresse, die standardmäßig in den Nachrichtenkopfzeilen im Return-Path angegeben wird, es ist aber möglich, dass der Absender eine andere Return-Path-Adresse festlegt.
  
Die Adresse "Von:" in den Nachrichtenkopfzeilen, auch als RFC 5322.From-Adresse bekannt, ist die E-Mail-Adresse, die im E-Mail-Client, z. B. Outlook, angezeigt wird.
  
Häufig sind die Adressen 5321.MailFrom und 5322.From gleich. Dies ist z. B. bei der Kommunikation zwischen zwei privaten Nutzern normal. Wenn allerdings die E-Mail im Auftrag eines anderen Benutzers gesendet wird, sind die Adressen häufig verschieden. Dies ist am häufigsten bei Massen-E-Mail-Nachrichten der Fall.
  
Nehmen wir z. B. an, dass die Fluglinie Blue Yonder Airlines die Firma Margie's Travel damit beauftragt hat, ihre Werbe-E-Mails zu versenden. Sie finden dann eine E-Mail in Ihrem Posteingang vor, die vom Absender blueyonder@news.blueyonderairlines.com stammt. In diesem Fall ist die 5321.MailFrom-Adresse blueyonder.airlines@margiestravel.com, und blueyonder@news.blueyonderairlines.com ist die 5322.From-Adresse, die Sie in Outlook sehen. Da der Dienst die RFC 5322.From-Adresse akzeptiert, können Sie sie in Outlook einfach als einen sicheren Absender hinzufügen, um zu verhindern, dass diese Nachricht gefiltert wird.
  


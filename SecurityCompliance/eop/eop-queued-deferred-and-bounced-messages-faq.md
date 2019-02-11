---
title: Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
ms.openlocfilehash: 4b2c902adacd6e72e587aadaceecd22dd0084d85
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686425"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten

Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
  
 **F. Warum werden E-Mails in eine Warteschlange eingereiht?**
  
A. Nachrichten werden in eine Warteschlange eingereiht oder zurückgestellt, wenn vom Dienst keine Verbindung zum Server des Empfängers hergestellt werden kann, um sie zuzustellen. Nachrichten werden nicht zurückgestellt, wenn vom Netzwerk des Empfängers ein Fehler der 500er-Serie zurückgegeben wird.
  
 **F. Wie kommt es zu einer Zurückstellung von Nachrichten?**
  
A. Nachrichten werden zurückgehalten, wenn keine Verbindung zum Server des Empfängers hergestellt werden kann und von diesem ein "temporärer Fehler" (z. B. "Verbindungstimeout" oder "Verbindung abgelehnt") oder ein Fehler der 400er-Serie zurückgegeben wird. Liegt ein dauerhafter Fehler vor (z. B. ein Fehler der 500er-Serie), wird die Nachricht an den Absender zurückgesendet.
  
 **F. Wie lange werden Nachrichten zurückgestellt, und in welchem Intervall wird der Übertragungsversuch wiederholt?**
  
A. Nachrichten in Verzögerungen bleibt in unseren Warteschlangen für 2 Tage. Nachricht an Eingabeversuchen basieren auf den Fehler, die wir wieder aus der Aufgabenliste des Empfängers e-Mail-System erhalten. Die ersten Paar Rückstellungen sind 15 Minuten oder weniger mit folgenden Wiederholungen (über die nächste halber zwölf oder dies) erhöhen das Intervall über mehrere Wiederholungsversuche auf ein Maximum von 60 Minuten. Die Erweiterung von Intervall Dauer ist dynamisch, Berücksichtigung mehrerer Variablen wie Warteschlange Größen und interne Nachrichtenpriorität. In Basic ist es 15 Minuten (oder weniger) zum Starten von dort in den nächsten paar Stunden auf erweitert max 60 Minuten.
  
 **F. Wie werden Nachrichten aus einer Warteschlange verteilt, nachdem mein E-Mail-Server wiederhergestellt ist?**
  
A. Nach der Wiederherstellung Ihres E-Mail-Servers werden alle in eine Warteschlange eingereihten Nachrichten automatisch in der Reihenfolge verarbeitet, in der sie empfangen und in die Warteschlange eingereiht wurden, bevor der Server nicht mehr zur Verfügung stand. 
  


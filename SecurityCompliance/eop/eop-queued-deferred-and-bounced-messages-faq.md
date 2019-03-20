---
title: Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
ms.openlocfilehash: e8fdb07d11a1f540e94b82730eb848a97f51523a
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693204"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten

Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
  
 **F. Warum werden E-Mails in eine Warteschlange eingereiht?**
  
A. Nachrichten werden in eine Warteschlange eingereiht oder zurückgestellt, wenn vom Dienst keine Verbindung zum Server des Empfängers hergestellt werden kann, um sie zuzustellen. Nachrichten werden nicht zurückgestellt, wenn vom Netzwerk des Empfängers ein Fehler der 500er-Serie zurückgegeben wird.
  
 **F. Wie kommt es zu einer Zurückstellung von Nachrichten?**
  
A. Nachrichten werden zurückgehalten, wenn keine Verbindung zum Server des Empfängers hergestellt werden kann und von diesem ein "temporärer Fehler" (z. B. "Verbindungstimeout" oder "Verbindung abgelehnt") oder ein Fehler der 400er-Serie zurückgegeben wird. Liegt ein dauerhafter Fehler vor (z. B. ein Fehler der 500er-Serie), wird die Nachricht an den Absender zurückgesendet.
  
 **F. Wie lange werden Nachrichten zurückgestellt, und in welchem Intervall wird der Übertragungsversuch wiederholt?**
  
A. Zurückgestellte Nachrichten bleiben 2 Tage lang in der Warteschlange. Wiederholungsversuche hängen davon ab, welcher Fehler vom E-Mail-System des Empfängers zurückgegeben wird. Die ersten paar Verzögerungen sind 15 Minuten oder weniger, bei nachfolgenden Wiederholungen (in den nächsten zwölf Jahren) wird das Intervall über mehrere Versuche auf maximal 60 Minuten erhöht. Die Intervalldauer-Erweiterung ist dynamisch und unter Berücksichtigung mehrerer Variablen wie Warteschlangengrößen und interner Nachrichtenpriorität. In Basic ist es 15 Minuten (oder weniger), um zu starten und dann von dort in den nächsten Stunden auf 60 Minuten zu erweitern.
  
 **F. Wie werden Nachrichten aus einer Warteschlange verteilt, nachdem mein E-Mail-Server wiederhergestellt ist?**
  
A. Nach der Wiederherstellung Ihres E-Mail-Servers werden alle in eine Warteschlange eingereihten Nachrichten automatisch in der Reihenfolge verarbeitet, in der sie empfangen und in die Warteschlange eingereiht wurden, bevor der Server nicht mehr zur Verfügung stand. 
  


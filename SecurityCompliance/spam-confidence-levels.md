---
title: SCL-Bewertungen (Spam Confidence Level)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
description: Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
ms.openlocfilehash: 4b8eea798bc46396e06da2c6ba0573c019d7a9b7
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002904"
---
# <a name="spam-confidence-levels"></a>SCL-Bewertungen (Spam Confidence Level)

Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
  
|**SCL-Bewertung**|**Spam Confidence-Interpretation**|**Standardaktion**|
|:-----|:-----|:-----|
|-1  <br/> |Kein Spam von einem sicheren Absender, Empfänger oder einer als sicher gelisteten IP-Adresse (vertrauenswürdiger Partner)  <br/> |Die Nachricht wird in das Postfach des Empfängers zugestellt.  <br/> |
|0, 1  <br/> |Kein Spam, weil die Nachricht überprüft und als spamfrei eingestuft wurde  <br/> |Die Nachricht wird in das Postfach des Empfängers zugestellt.  <br/> |
|5, 6  <br/> | Spam  <br/> |Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.  <br/> |
|7, 8, 9  <br/> |Spam mit hoher Vertrauenswürdigkeit  <br/> |Die Nachricht wird in den Ordner "Junk-E-Mail" des Empfängers zugestellt.  <br/> |
   
> [!TIP]
> SCL-Bewertung 2, 3, 4, 7 und 8 werden vom Dienst nicht festgelegt. SCL-Bewertung 5 oder 6 wird als Spam angesehen, das weniger sicher, dass Spam als SCL-Bewertung 9, sein, die bestimmte Spam betrachtet wird. Verschiedene Aktionen für Spam und vertrauenswürdige Spam können über Ihre inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole konfiguriert werden. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](configure-your-spam-filter-policies.md). Sie können auch die SCL-Bewertung für Nachrichten festlegen, die bestimmte Suchkriterien mithilfe von Transportregeln, wie unter [Verwenden von e-Mail-Flussregeln zum Spam Confidence Level (SCL) in Nachrichten festgelegt](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Wenn Sie eine Transportregel verwenden, um die SCL-Wert von 7, 8 und 9 festgelegt wird die Nachricht als vertrauenswürdige Spam behandelt werden. 
  
||
|:-----|
|![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning. |
   


---
title: SCL-Bewertungen (Spam Confidence Level)
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: Wenn eine E-Mail die Spamfilterung passiert, wird ihr eine Spambewertung zugewiesen. Diese Bewertung ist einer individuellen SCL-Bewertung (Spam Confidence Level) zugeordnet und wird als Stempel im X-Header angezeigt. Der Dienst verfährt mit den Nachrichten entsprechend der Spam Confidence-Interpretation der SCL-Bewertung. In der folgenden Tabelle ist aufgeführt, wie die unterschiedlichen SCL-Bewertungen von den Filtern interpretiert werden, und welche Aktionen standardmäßig für eingehende Nachrichten als Reaktion auf die einzelnen Bewertung erfolgen.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275645"
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
> SCL-Bewertungen von 2, 3, 4, 7 und 8 werden vom Dienst nicht festgelegt. Eine SCL-Bewertung von 5 oder 6 wird als mutmaßlicher Spam betrachtet, der weniger sicher ist als Spam als eine SCL-Bewertung von 9, die als bestimmter Spam angesehen wird. Unterschiedliche Aktionen für Spam und Spam mit hoher Vertrauenswürdigkeit können über Ihre Inhaltsfilter Richtlinien in der Exchange-Verwaltungskonsole konfiguriert werden. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md). Sie können die SCL-Bewertung für Nachrichten, die bestimmte Bedingungen erfüllen, auch mithilfe von Transport Regeln festlegen, wie in [Verwenden von Nachrichtenfluss Regeln beschrieben, um SCL (Spam Confidence Level) in Nachrichten festzulegen](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Wenn Sie eine Transportregel zum Festlegen der SCL-Bewertung von 7, 8 oder 9 verwenden, wird die Nachricht als Spam mit hoher Vertrauenswürdigkeit behandelt. 
  
||
|:-----|
|![Das Kurzsymbol für LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Neu bei Office 365?**         Entdecken Sie die kostenlosen Videokurse für **Office 365 admins and IT pros**, präsentiert von LinkedIn Learning. |
   


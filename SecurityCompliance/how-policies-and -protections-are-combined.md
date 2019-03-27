---
title: Kombination von Richtlinien und Schutzmechanismen bei der roten Markierung von e-Mails
description: Welche Richtlinien gelten, und welche Maßnahmen zu ergreifen sind, wenn e-Mails als Schadsoftware, Spam, hoch vertrauenswürdige Spam, Phishing und massenweise EOP und/oder ATP gekennzeichnet sind.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Sicherheitscenter, ATP, Windows Defender ATP, Office 365 ATP, Azure ATP
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 03/26/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 7aa0f89eed379273cb069cd65c083749a9552e91
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2019
ms.locfileid: "30926467"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a>Welche Richtlinie gilt, wenn mehrere Schutzmethoden und Erkennungs Scans in Ihrer e-Mail ausgeführt werden

Möglicherweise werden Ihre eingehenden e-Mails durch mehrere Schutzarten gekennzeichnet (beispielsweise sowohl für EOP ** als auch für ATP) und mehrere Erkennungs Scans (wie Spam *und* Phishing). Dies ist möglich, da es für ATP-Kunden Anti-Phishing-Richtlinien und EOP-Richtlinien für EOP-Kunden gibt. Dies kann auch bedeuten, dass die Nachricht beispielsweise mehrere Erkennungs Scans auf Schadsoftware, Phishing und Benutzeridentitätswechsel steuert. Bei all dieser Aktivität kann es zu Verwirrung darüber geben, welche Richtlinie gilt.

Im Allgemeinen wird die auf eine Nachricht angewendete Richtlinie im Header **X-Forefront-Antispam-Report** in der **Cat (Category)** -Eigenschaft identifiziert. Wenn Sie über mehrere Anti-Phishing-Richtlinien verfügen, gilt diejenige mit der höchsten Priorität.

Die folgenden Richtlinien gelten für _alle Organisationen_.

|Priority |Richtlinie  |Kategorie  |Wo verwaltet |
|---------|---------|---------|---------|
|1     | Schadsoftware      | MALW      | Schadsoftware-Richtlinie   |
|2     | Phishing-E-Mail     | PHSH     | Konfigurieren von Spamfilterrichtlinien     |
|3     | Spam mit hoher Vertrauenswürdigkeit      | HSPM        | Konfigurieren von Spamfilterrichtlinien        |
|4     | Spoofing        | SPOOFING        | Anti-Phishing-Richtlinie, spoof Intelligence        |
|5     | Spam         | SPM         | Konfigurieren von Spamfilterrichtlinien         |
|6     | Massen         | Massen        | Konfigurieren von Spamfilterrichtlinien         |

Darüber hinaus gelten diese Richtlinien für _Organisationen mit ATP_.

|Priority |Richtlinie  |Kategorie  |Wo verwaltet |
|---------|---------|---------|---------|
|7     | Domänen Identitätswechsel         | DIMP         | Einrichten von Office 365 ATP-Antiphishing-und-Phishing-Richtlinien        |
|8     | Benutzeridentitätswechsel        | UIMP         | Einrichten von Office 365 ATP-Antiphishing-und-Phishing-Richtlinien         |

Wenn Sie beispielsweise zwei Richtlinien haben:

|Richtlinie  |Priority  |Identitätswechsel für Benutzer/Domänen  |Antispoofing  |
|---------|---------|---------|---------|
|A     | 1        | On        |Off         |
|B     | 2        | Off        | On        |

Wenn eine Nachricht sowohl als _Benutzeridentitätswechsel_ als auch als Spoofing __ identifiziert wird (siehe Anti-Spoofing in der obigen Tabelle), und die gleiche Gruppe von Benutzern, die auf Richtlinie a ausgelegt ist, auf Richtlinie B festgelegt ist, wird die Nachricht gekennzeichnet und als _Spoof_behandelt, aber keine Aktion wird angewendet, da Antispoofing deaktiviert ist und **Spoofing mit einer höheren Priorität (4) als der Benutzeridentitätswechsel (8) ausgeführt**wird.

Damit andere Arten von Phishing-Richtlinien angewendet werden, müssen Sie die Einstellungen anpassen, für die die verschiedenen Richtlinien gelten.




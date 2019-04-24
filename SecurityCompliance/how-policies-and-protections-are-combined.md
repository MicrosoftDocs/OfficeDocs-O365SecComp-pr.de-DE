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
ms.openlocfilehash: 73f44e747581664f075608d972ee80c8381ca7fd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256313"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a>Welche Richtlinie gilt, wenn mehrere Schutzmethoden und Erkennungs Scans in Ihrer e-Mail ausgeführt werden

Möglicherweise werden Ihre eingehenden e-Mails durch mehrere Schutzarten gekennzeichnet (beispielsweise sowohl für EOP ** als auch für ATP) und mehrere Erkennungs Scans (wie Spam *und* Phishing). Dies ist möglich, da es für ATP-Kunden Anti-Phishing-Richtlinien und EOP-Richtlinien für EOP-Kunden gibt. Dies kann auch bedeuten, dass die Nachricht beispielsweise mehrere Erkennungs Scans auf Schadsoftware, Phishing und Benutzeridentitätswechsel steuert. Bei all dieser Aktivität kann es zu Verwirrung darüber geben, welche Richtlinie gilt.

Im Allgemeinen wird eine auf eine Nachricht angewendete Richtlinie im Header **X-Forefront-Antispam-Report** in der **Cat (Category)** -Eigenschaft identifiziert. Wenn Sie über mehrere Anti-Phishing-Richtlinien verfügen, gilt diejenige mit der höchsten Priorität.

Die folgenden Richtlinien gelten für _alle Organisationen_.

|Priorität |Richtlinie  |Kategorie  |Wo verwaltet |
|---------|---------|---------|---------|
|1     | Schadsoftware      | MALW      | Schadsoftware-Richtlinie   |
|2     | Phishing-E-Mail     | PHSH     | Konfigurieren von Spamfilterrichtlinien     |
|3     | Spam mit hoher Vertrauenswürdigkeit      | HSPM        | Konfigurieren von Spamfilterrichtlinien        |
|4     | Spoofing        | SPOOF        | Anti-Phishing-Richtlinie, spoof Intelligence        |
|5     | Spam         | SPM         | Konfigurieren von Spamfilterrichtlinien         |
|6     | Massen         | Massen        | Konfigurieren von Spamfilterrichtlinien         |

Darüber hinaus gelten diese Richtlinien für _Organisationen mit ATP_.

|Priorität |Richtlinie  |Kategorie  |Wo verwaltet |
|---------|---------|---------|---------|
|7     | Domänen Identitätswechsel         | DIMP         | Einrichten von Office 365 ATP-Antiphishing-und-Phishing-Richtlinien        |
|8     | Benutzeridentitätswechsel        | UIMP         | Einrichten von Office 365 ATP-Antiphishing-und-Phishing-Richtlinien         |

Wenn Sie beispielsweise zwei Richtlinien mit ihren jeweiligen Prioritäten haben:

|Richtlinie  |Priorität  |Identitätswechsel für Benutzer/Domänen  |Antispoofing  |
|---------|---------|---------|---------|
|A     | 1        | Ein        |Off         |
|B     | 2        | Off        | Ein        |

Wenn eine Nachricht sowohl als _Benutzeridentitätswechsel_ als auch als Spoofing __ identifiziert wird (siehe Anti-Spoofing in der obigen Tabelle), und dieselbe Gruppe von Benutzern, die auf Richtlinie a ausgelegt ist, auf Richtlinie B ausgelegt ist, wird die Nachricht als _Spoof_gekennzeichnet und behandelt. Es wird jedoch keine Aktion angewendet, da Spoofing mit höherer Priorität (4) als der Benutzeridentitätswechsel (8) ausgeführt wird.

Beachten Sie, dass Administratoren eine priorisierte Liste mit Richtlinien erstellen können (siehe das Feld Priorität oben), aber nur eine Richtlinie wird ausgeführt und ihre Aktionen angewendet. Das bedeutet, dass ein Benutzer in der Richtlinie A und B die Richtlinie mit höherer Priorität (A ist #1) ausführen muss, und die Nachricht wird nicht durch weitere Richtlinien gefiltert. Wenn die spoofiing deaktiviert ist, werden keine Aktionen ausgeführt.

Da es in vielen Richtlinien ein Potenzial für viele Benutzergruppen gibt, kann es behoove Administratoren ermöglichen, weniger Richtlinien mit mehr Funktionen zu verwenden. Es ist auch wichtig sicherzustellen, dass alle Benutzer von einer umfassenden Richtlinie abgedeckt werden.

Damit andere Arten von Phishing-Richtlinien angewendet werden, müssen Sie die Einstellungen anpassen, für die die verschiedenen Richtlinien gelten.




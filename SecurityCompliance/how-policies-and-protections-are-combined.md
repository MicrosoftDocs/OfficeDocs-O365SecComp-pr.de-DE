---
title: Kombinieren von Richtlinien und Schutzmechanismen bei der roten Kennzeichnung von e-Mails
description: Welche Richtlinien gelten und welche Aktionen ausgeführt werden sollen, wenn e-Mail-Nachrichten als Schadsoftware, Spam, vertrauenswürdiger Spam, Phishing und Massen von EoP und/oder ATP gekennzeichnet sind.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Sicherheitscenter, ATP, Windows Defender ATP, Office 365 ATP, Azure ATP
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 03/26/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 1c2e575a57e1c1118154a912199d9e74cb4ceb4a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152707"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a>Welche Richtlinie gilt, wenn mehrere Schutzmethoden und Erkennungs Scans in Ihren e-Mails ausgeführt werden

Möglicherweise werden Ihre eingehenden e-Mails durch mehrere Schutzformen (beispielsweise EoP *und* ATP) und mehrere Erkennungs Scans (beispielsweise Spam *und* Phishing) gekennzeichnet. Dies ist möglich, da es sich um ATP-AntiPhishing-Richtlinien für ATP-Kunden und EOP-Anti-Phishing-Richtlinien für EoP-Kunden handelt. Dies bedeutet auch, dass die Nachricht möglicherweise mehrere Erkennungs Scans für Malware, Phishing und Benutzeridentitätswechsel durchsucht. Angesichts all dieser Aktivitäten kann es einige Verwirrung darüber geben, welche Richtlinie angewendet wird.

Im Allgemeinen wird eine Richtlinie, die auf eine Nachricht angewendet wird, im **X-Forefront-Antispam-Report-** Header in der Cat-Eigenschaft **(Category)** identifiziert. Wenn Sie über mehrere Anti-Phishing-Richtlinien verfügen, wird diejenige mit der höchsten Priorität angewendet.

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
|7     | Domänen Identitätswechsel         | DIMP         | Einrichten von Office 365 ATP-Richtlinien für Anti-Phishing und Anti-Phishing        |
|8     | Benutzeridentitätswechsel        | Uimp         | Einrichten von Office 365 ATP-Richtlinien für Anti-Phishing und Anti-Phishing         |

Wenn Sie beispielsweise über zwei Richtlinien mit ihren jeweiligen Prioritäten verfügen:

|Richtlinie  |Priorität  |Benutzer/Domänen-Identitätswechsel  |Anti-Spoofing  |
|---------|---------|---------|---------|
|A     | 1        | Ein        |Off         |
|B     | 2        | Off        | Ein        |

Wenn eine Nachricht sowohl als _Benutzeridentitätswechsel_ als auch als Spoofing __ identifiziert wird (siehe Anti-Spoofing in der obigen Tabelle), und die gleiche Gruppe von Benutzern, die auf Richtlinie a Bericht ist, auf Richtlinie B festgelegt ist, wird die Nachricht als _Spoof_gekennzeichnet und behandelt. Es wird jedoch keine Aktion angewendet, da Spoofing zwar mit einer höheren Priorität (4) als mit dem Benutzeridentitätswechsel (8) ausgeführt wird, aber das Spoofing deaktiviert ist.

Beachten Sie, dass Administratoren eine priorisierte Liste von Richtlinien erstellen können (siehe das Feld Priorität oben), aber nur eine Richtlinie ausgeführt wird und ihre Aktionen anwenden. Das bedeutet, dass für einen Benutzer in den Richtlinien a und B die Richtlinie mit höherer Priorität (a ist #1) ausgeführt wird und die Nachricht nicht durch weitere Richtlinien gefiltert wird. Wenn das Anti-spoofiing deaktiviert ist, werden keine Aktionen ausgeführt.

Da es in vielen Richtlinien ein Potenzial gibt, viele Benutzergruppen zu verwenden, kann es sein, dass Administratoren weniger Richtlinien mit mehr Funktionen als behoove. Es ist auch wichtig sicherzustellen, dass alle Benutzer durch eine umfassende Richtlinie abgedeckt sind.

Damit andere Arten von Phishing-Richtlinien angewendet werden können, müssen Sie die Einstellungen anpassen, auf die die verschiedenen Richtlinien zutreffen.




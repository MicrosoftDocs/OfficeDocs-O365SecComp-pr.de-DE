---
title: ATP-Antiphishingfunktionen in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: ATP-AntiPhishing ist Teil von Office 365 Advanced Threat Protection. ATP-AntiPhishing wendet eine Reihe von Computer Lernmodellen zusammen mit Identitätswechsel Erkennungsalgorithmen auf eingehende Nachrichten an, um den Schutz von Commodity-und Spear-Phishing-Angriffen zu gewährleisten. Alle Nachrichten unterliegeneiner umfassenden Reihe von Computer Lernmodellen, die für die Ermittlung von Phishing-Nachrichten ausgebildet wurden, sowie eine Reihe fortschrittlicher Algorithmen, die zum Schutz vor verschiedenen Angriffen auf Benutzer-und Domänenidentitäten verwendet werden.
ms.openlocfilehash: 3cd786de403bd2fe4fcdd5d53f3f825c6e4e8a40
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "29889248"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>ATP-Antiphishingfunktionen in Office 365

ATP-AntiPhishing ist Teil von [Office 365 Advanced Threat Protection](office-365-atp.md). ATP-AntiPhishing wendet eine Reihe von Computer Lernmodellen zusammen mit Identitätswechsel Erkennungsalgorithmen auf eingehende Nachrichten an, um den Schutz von Commodity-und Spear-Phishing-Angriffen zu gewährleisten. Alle Nachrichten unterliegeneiner umfassenden Reihe von Computer Lernmodellen, die für die Ermittlung von Phishing-Nachrichten ausgebildet wurden, sowie eine Reihe fortschrittlicher Algorithmen, die zum Schutz vor verschiedenen Angriffen auf Benutzer-und Domänenidentitäten verwendet werden. ATP-Phishing schützt Ihre Organisation gemäß den Richtlinien, die von Ihren Office 365-globalen oder Sicherheitsadministratoren festgelegt werden.
  
Weitere Informationen finden Sie unter [Einrichten von Richtlinien zum Schutz vor Phishing in Office 365](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> ATP-Phishing ist nur in Advanced Threat Protection verfügbar, das in Abonnements enthalten ist, wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).

## <a name="how-atp-anti-phishing-works"></a>Funktionsweise des ATP-Antiphishings

ATP-Phishing prüft eingehende Nachrichten auf Indikatoren, die möglicherweise Phishing aufweisen. Wenn ein Benutzer von einer ATP-Richtlinie abgedeckt wird (sichere Anlagen, sichere Links oder Phishing), wird die eingehende Nachricht von mehreren maschinellen Lernmodellen ausgewertet, die die Nachricht analysieren, um zu ermitteln, ob die Richtlinie für die Nachricht gilt, und die entsprechende Aktion ist basierend auf der konfigurierten Richtlinie.
  
ATP-AntiPhishing ermöglicht es Office 365-globalen Administratoren oder Sicherheitsadministratoren, Richtlinien zu definieren, die Schutz vor Phishing-Angriffen bieten, die den Identitätswechsel von Benutzern oder Domänen umfassen. (oder beides). Office 365 globale Administratoren oder Sicherheitsadministratoren definieren innerhalb der Richtlinie, welche Benutzer und Domänen vor Identitätswechsel Angriffen mithilfe einer festen Liste von Benutzern oder Domänen oder mithilfe von Mailbox Intelligence geschützt werden sollen. Mailbox Intelligence ist ein erweitertes Verständnis der e-Mail-Gewohnheiten und persönlichen Kontakte eines Benutzers. ATP lernt, wie jeder einzelne Benutzer mit anderen Benutzern innerhalb und außerhalb der Organisation kommuniziert, und erstellt eine Karte dieser Beziehungen. Diese Karte ermöglicht es ATP, mehr darüber zu erfahren, wie Sie sicherstellen, dass die richtigen Nachrichten als Identitätswechsel identifiziert werden.
  
ATP-Phishing-Policies können auf eine bestimmte Gruppe von Personen oder Gruppen in Ihrer Organisation oder auf eine gesamte Domäne oder alle benutzerdefinierten Domänen angewendet werden. Weitere Informationen finden Sie unter [Einrichten von Richtlinien zum Schutz vor Phishing in Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>How to Get ATP Anti-Phishing

ATP-antiPhishingfunktionen gehören zu [Advanced Threat Protection](office-365-atp.md); Allerdings gilt der ATP-Schutz vor Phishing bei der Definition von AntiPhishing-Richtlinien. (Ein Beispiel ist eine Identitätswechsel basierte Richtlinie.) Weitere Informationen finden Sie unter [Einrichten von Richtlinien zum Schutz vor Phishing in Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Wie Sie wissen, ob ATP-AntiPhishing vorhanden ist

ATP-Phishing-Richtlinien müssen definiert werden, damit der Schutz wirksam wird. Aktivieren Sie dieses Kontrollkästchen, um sicherzustellen, dass der Schutz vorhanden ist.

Darüber hinaus stehen Berichte zur Verfügung, um zu veranschaulichen, wie der Dienst für Ihre Organisation funktioniert. Weitere Informationen finden Sie unter [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md).

Damit die Lernmodelle von ATP-antiphishingmaschinen für einen bestimmten Benutzer aktiv sein können, muss dieser Benutzer Teil einer definierten ATP-Anlage für [sichere Anlagen](atp-safe-attachments.md), [ATP-sichere Links](atp-safe-links.md)oder eine ATP-richtLinie zum Schutz vor Phishing sein. 

In der folgenden Tabelle werden einige Beispielszenarien beschrieben. In jedem dieser Beispiele verwendet die Organisation Office 365 Enterprise E5, einschließlich erweiterter BedrohungsSchutz.
  
|**Beispielszenario**|**Gilt in diesem Fall ATP-AntiPhishing?**|
|:-----|:-----|
|Pat es Organisation hat Office 365 Enterprise E5, aber niemand hat irgendwelche Richtlinien für ATP Safe Attachments, ATP Safe Links oder ATP Advanced Phishing definiert.|Nein. Obwohl das Feature verfügbar ist, muss mindestens eine ATP-Richtlinie definiert werden, damit die Lernmodelle für die ATP-Maschine funktionieren. Bei Identitätswechsel muss auch eine ATP-Richtlinie zum Schutz vor Phishing vorhanden sein.|
|Lee ist ein Mitarbeiter in der Vertriebsabteilung bei Contoso. Lees Organisation verfügt über eine Anti-Phishing-Richtlinie für ATP, die nur für Mitarbeiter von Finance gilt.|Nein. In diesem Fall würde ATP-Phishing (Computermodelle und Identitätswechsel Schutz) für Mitarbeiter von Finance gelten, aber andere Mitarbeiter, einschließlich der Vertriebsabteilung, würden dies nicht tun.|
|Gestern richtete ein Office 365-Administrator bei der Organisation von Jean eine ATP-Richtlinie zum Schutz vor Phishing ein, die für alle Mitarbeiter gilt. Heute hat Jean eine e-Mail-Nachricht erhalten, die einen Identitätswechsel enthält, der von der Richtlinie abgedeckt wird.|Ja. In diesem Beispiel verfügt Jean über eine Lizenz für Advanced Threat Protection, und eine ATP-Richtlinie zum Schutz vor Phishing, die Jean enthält, wurde definiert. In der Regel dauert es ungefähr 30 Minuten, bis eine neue Richtlinie über Rechenzentren hinweg wirksam wird. Da in diesem Fall ein Tag vergangen ist, sollte die Richtlinie wirksam sein.|

## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Antiphishingschutz in Office 365](anti-phishing-protection.md)
  
[Einrichten von Richtlinien zum Schutz vor Phishing in Office 365](set-up-anti-phishing-policies.md)
  
[Sichere ATP-Links in Office 365](atp-safe-links.md)
  
[Einrichten von Richtlinien für ATP-sichere Links in Office 365](set-up-atp-safe-links-policies.md)
  
[Sichere ATP-Anlagen in Office 365](atp-safe-attachments.md)
  
[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)

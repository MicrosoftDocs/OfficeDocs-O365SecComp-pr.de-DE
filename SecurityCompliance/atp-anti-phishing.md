---
title: ATP-Antiphishingfunktionen in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: ATP Anti-Phishing wird als Teil von Office 365 erweiterte Schutz angeboten. ATP Anti-Phishing weist der Computer Learning Modelle zusammen mit Identitätswechsel Erkennung Algorithmen auf eingehende Nachrichten für den Schutz für Waren und Spear Phishing-Angriffe. Alle Nachrichten werden eine umfassende Sammlung von Computer Learning Modelle geschulte zum Erkennen von Phishing-Nachrichten, zusammen mit einer Reihe von erweiterten Algorithmen zum Schutz vor Angriffen Identitätswechsel verschiedenen Benutzername und Domäne verwendet. ATP Anti-Phishing schützt Ihre Organisation entsprechend um zu Richtlinien, von Ihrem Office 365 globaler oder Sicherheitsadministratoren festgelegt werden.
ms.openlocfilehash: e7bb4c4a28109c40bf745a25c9c8366558cf2ac7
ms.sourcegitcommit: ba2175e394d0cb9f8ede9206aabb44b5b677fa0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2018
ms.locfileid: "25496889"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>ATP-Antiphishingfunktionen in Office 365

ATP Anti-Phishing wird als Teil von [Office 365 erweiterte Schutz](https://technet.microsoft.com/en-us/library/exchange-online-advanced-threat-protection-service-description.aspx)angeboten. ATP Anti-Phishing weist der Computer Learning Modelle zusammen mit Identitätswechsel Erkennung Algorithmen auf eingehende Nachrichten für den Schutz für Waren und Spear Phishing-Angriffe. Alle Nachrichten werden eine umfassende Sammlung von Computer Learning Modelle geschulte zum Erkennen von Phishing-Nachrichten, zusammen mit einer Reihe von erweiterten Algorithmen zum Schutz vor Angriffen Identitätswechsel verschiedenen Benutzername und Domäne verwendet. ATP Anti-Phishing schützt Ihre Organisation entsprechend um zu Richtlinien, von Ihrem Office 365 globaler oder Sicherheitsadministratoren festgelegt werden.
  
Finden Sie weitere Informationen finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> ATP Anti-Phishing ist nur verfügbar, erweiterte Threat Protection, mit Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann der erweiterte Schutz als Add-on erworben werden. (Als ein globaler Administrator, in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen zu den Optionen zum Plan finden Sie unter [Vergleich alle Office 365 für Unternehmen plant](https://go.microsoft.com/fwlink/?linkid=844053). 
    
## <a name="how-atp-anti-phishing-works"></a>Funktionsweise von ATP Anti-phishing
<a name="Howantiphishworks"> </a>

ATP Anti-Phishing überprüft eingehende Nachrichten für Indikatoren, dass die Nachricht Phishing werden kann. Wenn ein Benutzer durch eine Richtlinie ATP (sichere Anlagen, sicheren Links oder Anti-Phishing) abgedeckt wird die eingehende Nachricht ausgewertet durch mehrere Computer erlernen Modelle, die die Nachricht zu ermitteln, ob die Richtlinie für die Nachricht gilt und die entsprechende Aktion ist analysieren genommen basierend auf die konfigurierte Richtlinie.
  
ATP Anti-Phishing ermöglicht globale Office 365-Administratoren oder Sicherheit-Admins zum Definieren von Richtlinien, die Schutz gegen Phishing-Angriffe bereitstellen, die von Benutzern oder Domänen Identitätswechsel enthalten. (oder beides). Globale Office 365-Administratoren oder Sicherheit-Admins definieren innerhalb der Richtlinie an, welche Benutzer und Domänen vor Angriffen mit Identitätswechsel mit einer geschützt werden sollte, eine feste Liste von Benutzern oder Domänen oder mithilfe von Postfach Intelligence. Postfach Intelligence ist fortgeschrittene Kenntnisse von e-Mail-Gewohnheiten des Benutzers und persönliche Kontakte. ATP lernen, wie jeden einzelnen Benutzer kommuniziert mit anderen Benutzern innerhalb und außerhalb der Organisation und eine Übersicht über diese Beziehungen erstellt. Diese Zuordnung ermöglicht ATP zu verstehen, Weitere Informationen dazu, wie Sie um sicherzustellen, dass die richtigen Nachrichten als Identitätswechsel identifiziert werden.
  
ATP Anti-Phishing-Richtlinien angewendet werden kann, um eine bestimmte Gruppe von Personen oder Gruppen in Ihrer Organisation oder um eine gesamte Domäne oder alle benutzerdefinierten Domänen. Finden Sie weitere Informationen finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Wie ATP Anti-Phishing abrufen
<a name="Howtogetantiphish"> </a>

ATP Anti-Phishing ist Teil der erweiterte Threat Protection, die in Office 365 Enterprise E5 enthalten ist. Erweiterte Schutz kann auch als Add-on für Office 365 Enterprise E1 oder E3 für Office 365 Enterprise erworben werden. Weitere Informationen zu den Optionen zum Plan finden Sie unter [Vergleich alle Office 365 für Unternehmen plant](https://go.microsoft.com/fwlink/?linkid=844053).
  
ATP Anti-Phishing angewendet wird, wenn eine Richtlinie Anti-Phishing wie eine Identitätswechsel-basierten Richtlinie eingerichtet sind. (Finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).)
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Woran ATP Anti-Phishing vorhanden ist
<a name="IsantiphishOn"> </a>

In der Reihenfolge für den Schutz aktiv sein müssen ATP Anti-Phishing-Richtlinien definiert werden. Für ATP Anti-Phishing Computer Learning Modelle für einen Benutzer aktiv sein muss der Benutzer einen definierten sichere Anlage, sicheren Links oder Anti-Phishing-Richtlinie gehören. In der folgenden Tabelle werden einige Beispielszenarien beschrieben. In den einzelnen in diesen Beispielen wird die Office 365 Enterprise E5 verwendet der erweiterte Schutz enthält.
  
|**Beispielszenario**|**In diesem Fall wird ATP Anti-Phishing werden angewendet?**|
|:-----|:-----|
|Pats Organisation hat Office 365 Enterprise E5, aber niemand hat alle Richtlinien für ATP sichere Anlagen, ATP sichere Links oder erweiterte Phishing noch ATP definiert.|Nein. Obwohl das Feature verfügbar ist, muss mindestens eine ATP-Richtlinie in der Reihenfolge für die Modelle erlernen ATP Computer funktionieren definiert werden. Für den Identitätswechsel muss eine ATP Anti-Phishing-Richtlinie auch vorhanden sein.|
|Kelly ist ein Mitarbeiter der Abteilung "sales" bei Contoso. Kelly Organisation hat eine ATP Anti-Phishing-Richtlinie eingeführt, die nur für Mitarbeiter der Finanzabteilung gelten.|Nein. In diesem Fall ATP Anti-Phishing (Computer Modelle und Identitätswechsel Protection) gelten für Mitarbeiter der Finanzabteilung, andere Mitarbeiter, einschließlich der IT-Abteilung, jedoch nicht.|
|Ein Office 365-Administrator bei Jeans Organisation eingerichtet gestern, eine ATP Anti-Phishing-Richtlinie, die für alle Mitarbeiter gilt. Jean empfangen heute, eine e-Mail-Nachricht, die einen Identitätswechsel behandelt, die durch die Richtlinie enthält.|Ja. In diesem Beispiel Jean verfügt über eine Lizenz für erweiterte Threat Protection und eine ATP Anti-Phishing-Richtlinie, die Jean definiert wurde. In der Regel nimmt etwa 30 Minuten für eine neue Richtlinie wirksam in Rechenzentren; Da in diesem Fall ein Tag verstrichen ist, sollte die Richtlinie aktiviert sein.|
   
## <a name="related-topics"></a>Verwandte Themen
<a name="IsantiphishOn"> </a>

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Antiphishingschutz in Office 365](anti-phishing-protection.md)
  
[Einrichten von Anti-Phishing-Richtlinien in Office 365](set-up-anti-phishing-policies.md)
  
[ATP sichere Links in Office 365](atp-safe-links.md)
  
[Einrichten von ATP sichere Links Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
  
[ATP sichere Anlagen in Office 365](atp-safe-attachments.md)
  
[Einrichten von Richtlinien für ATP sichere Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)
  


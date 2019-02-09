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
description: ATP Anti-Phishing ist Teil der Office 365 erweiterte Threat Protection. ATP Anti-Phishing weist der Computer Learning Modelle zusammen mit Identitätswechsel Erkennung Algorithmen auf eingehende Nachrichten für den Schutz für Waren und Spear Phishing-Angriffe. Alle Nachrichten werden eine umfassende Sammlung von Computer Learning Modelle geschulte zum Erkennen von Phishing-Nachrichten, zusammen mit einer Reihe von erweiterten Algorithmen zum Schutz vor Angriffen Identitätswechsel verschiedenen Benutzername und Domäne verwendet.
ms.openlocfilehash: c3e44a313bf9c823fbfda138fc5a10294993d509
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792270"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>ATP-Antiphishingfunktionen in Office 365

ATP Anti-Phishing ist Teil der [Office 365 erweiterte Threat Protection](office-365-atp.md). ATP Anti-Phishing weist der Computer Learning Modelle zusammen mit Identitätswechsel Erkennung Algorithmen auf eingehende Nachrichten für den Schutz für Waren und Spear Phishing-Angriffe. Alle Nachrichten werden eine umfassende Sammlung von Computer Learning Modelle geschulte zum Erkennen von Phishing-Nachrichten, zusammen mit einer Reihe von erweiterten Algorithmen zum Schutz vor Angriffen Identitätswechsel verschiedenen Benutzername und Domäne verwendet. ATP Anti-Phishing schützt Ihre Organisation entsprechend um zu Richtlinien, von Ihrem Office 365 globaler oder Sicherheitsadministratoren festgelegt werden.
  
Finden Sie weitere Informationen finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> ATP Anti-Phishing ist nur verfügbar, erweiterte Threat Protection, die in Abonnements, wie beispielsweise [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten ist. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).

## <a name="how-atp-anti-phishing-works"></a>Funktionsweise von ATP Anti-phishing

ATP Anti-Phishing überprüft eingehende Nachrichten für Indikatoren, dass die Nachricht Phishing werden kann. Wenn ein Benutzer durch eine Richtlinie ATP (sichere Anlagen, sicheren Links oder Anti-Phishing) abgedeckt wird die eingehende Nachricht ausgewertet durch mehrere Computer erlernen Modelle, die die Nachricht zu ermitteln, ob die Richtlinie für die Nachricht gilt und die entsprechende Aktion ist analysieren genommen basierend auf die konfigurierte Richtlinie.
  
ATP Anti-Phishing ermöglicht globale Office 365-Administratoren oder Sicherheit-Admins zum Definieren von Richtlinien, die Schutz gegen Phishing-Angriffe bereitstellen, die von Benutzern oder Domänen Identitätswechsel enthalten. (oder beides). Globale Office 365-Administratoren oder Sicherheit-Admins definieren innerhalb der Richtlinie an, welche Benutzer und Domänen vor Angriffen mit Identitätswechsel mit einer geschützt werden sollte, eine feste Liste von Benutzern oder Domänen oder mithilfe von Postfach Intelligence. Postfach Intelligence ist fortgeschrittene Kenntnisse von e-Mail-Gewohnheiten des Benutzers und persönliche Kontakte. ATP lernen, wie jeden einzelnen Benutzer kommuniziert mit anderen Benutzern innerhalb und außerhalb der Organisation und eine Übersicht über diese Beziehungen erstellt. Diese Zuordnung ermöglicht ATP zu verstehen, Weitere Informationen dazu, wie Sie um sicherzustellen, dass die richtigen Nachrichten als Identitätswechsel identifiziert werden.
  
ATP Anti-Phishing-Richtlinien angewendet werden kann, um eine bestimmte Gruppe von Personen oder Gruppen in Ihrer Organisation oder um eine gesamte Domäne oder alle benutzerdefinierten Domänen. Finden Sie weitere Informationen finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Wie ATP Anti-Phishing abrufen

ATP Anti-Phishing-Features sind Teil der [Erweiterte Schutz](office-365-atp.md); ATP Phishing-Schutz gilt jedoch auch wenn Anti-Phishing Richtlinien definiert sind. (Ein Beispiel ist eine Richtlinie Identitätswechsel-basierte.) Finden Sie unter [Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Woran ATP Anti-Phishing vorhanden ist

ATP Anti-Phishing Richtlinien müssen in der Reihenfolge für den Schutz in Kraft treten definiert werden. Überprüfen Sie, dass dies zuerst auf die Protection überprüfen vorhanden ist.

Darüber hinaus stehen Berichte anzeigen, wie der Dienst für Ihre Organisation arbeitet. Finden Sie weitere Informationen finden Sie unter [Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md).

Für ATP Anti-Phishing Computer erlernen Modelle für einen bestimmten Benutzer aktiv sein muss der Benutzer Teil einer definierten [ATP sicheren Anlagen](atp-safe-attachments.md), [ATP sichere Links](atp-safe-links.md)oder ATP Anti-Phishing-Richtlinie. 

In der folgenden Tabelle werden einige Beispielszenarien beschrieben. In den einzelnen in diesen Beispielen wird die Office 365 Enterprise E5 verwendet der erweiterte Schutz enthält.
  
|**Beispielszenario**|**In diesem Fall wird ATP Anti-Phishing werden angewendet?**|
|:-----|:-----|
|Pats Organisation hat Office 365 Enterprise E5, aber niemand hat alle Richtlinien für ATP sichere Anlagen, ATP sichere Links oder erweiterte Phishing noch ATP definiert.|Nein. Obwohl das Feature verfügbar ist, muss mindestens eine ATP-Richtlinie in der Reihenfolge für die Modelle erlernen ATP Computer funktionieren definiert werden. Für den Identitätswechsel muss eine ATP Anti-Phishing-Richtlinie auch vorhanden sein.|
|Kelly ist ein Mitarbeiter der Abteilung "sales" bei Contoso. Kelly Organisation hat eine ATP Anti-Phishing-Richtlinie eingeführt, die nur für Mitarbeiter der Finanzabteilung gelten.|Nein. In diesem Fall ATP Anti-Phishing (Computer Modelle und Identitätswechsel Protection) gelten für Mitarbeiter der Finanzabteilung, andere Mitarbeiter, einschließlich der IT-Abteilung, jedoch nicht.|
|Ein Office 365-Administrator bei Jeans Organisation eingerichtet gestern, eine ATP Anti-Phishing-Richtlinie, die für alle Mitarbeiter gilt. Jean empfangen heute, eine e-Mail-Nachricht, die einen Identitätswechsel behandelt, die durch die Richtlinie enthält.|Ja. In diesem Beispiel Jean verfügt über eine Lizenz für erweiterte Threat Protection und eine ATP Anti-Phishing-Richtlinie, die Jean definiert wurde. In der Regel nimmt etwa 30 Minuten für eine neue Richtlinie wirksam in Rechenzentren; Da in diesem Fall ein Tag verstrichen ist, sollte die Richtlinie aktiviert sein.|

## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Antiphishingschutz in Office 365](anti-phishing-protection.md)
  
[Einrichten von Anti-Phishing-Richtlinien in Office 365](set-up-anti-phishing-policies.md)
  
[ATP sichere Links in Office 365](atp-safe-links.md)
  
[Einrichten von ATP sichere Links Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
  
[ATP sichere Anlagen in Office 365](atp-safe-attachments.md)
  
[Einrichten von Richtlinien für ATP sichere Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)

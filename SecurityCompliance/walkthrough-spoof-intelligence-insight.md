---
title: Exemplarische Vorgehensweise Spoofing Intelligence Erkenntnisse
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: Sehen Sie, wie die neuen Spoofing Intelligence Einblicke funktioniert.
ms.openlocfilehash: ca9c4ae6f2d65ef2700a2e02acd5b4f1dfbfe903
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22596094"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>Exemplarische Vorgehensweise: Spoofing Intelligence Erkenntnisse

Mithilfe der Spoofing Intelligence Erkenntnisse können Sie schnell ermitteln, welche Absender, dass Sie nicht authentifizierte e-Mail bewusst senden. Durch die Möglichkeit erhalten, gefälschte Nachrichten senden, können Sie das Risiko von alle falsch positive Ergebnisse unterschiedlich sein und sollte Ihre Benutzer reduzieren.
  
Darüber hinaus können Sie auch verwenden Spoofing Intelligence überwachen und verwalten, um eine zusätzliche Sicherheitsebene bereitzustellen und zu verhindern, dass unsichere Nachrichten in Ihrer Organisation eingehenden zulässige Domäne-Paare.
  
Verwenden Sie die Spoofing Intelligence Einblicke in die Sicherheit &amp; Compliance Center, wenn Ihr Konto arbeiten oder Schule globaler Office 365-Administrator, Sicherheitsadministrator oder Sicherheit Leseberechtigungen erteilt wurde. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
Wenn Sie zum ersten Mal [Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), dazu beitragen, finden, wie Sie auf einfache Weise aus einem Dashboard einen Einblick aufrufen können, und empfohlenen Aktionen.
  
Sie können die Spoofing Intelligence Einblicke aus mehr als ein Dashboard in das Wertpapier anzeigen &amp; Compliance Center. Unabhängig von dem Dashboard wird angezeigt, die Einblicke enthält die gleichen Details und ermöglicht es Ihnen, schnell die gleichen Aufgaben auszuführen.
  
Dies ist eine von mehreren exemplarischen Vorgehensweisen für die Sicherheit &amp; Compliance Center. Zum Navigieren in Berichten und Einblicke in die, die exemplarischen Vorgehensweisen im Abschnitt Siehe auch angezeigt.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>Einführung in die Spoofing Intelligence Einblicke in das Wertpapier &amp; Compliance Center

1. Um zu beginnen, müssen Sie [Besuchen Sie die Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md).
    
2. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Threat Management** \> **Dashboard.**
    
3. Suchen Sie in der **Einblicke in die** Zeile für die Spoofing Intelligence Einblicke. Wenn Sie Spoofing Intelligence aktiviert haben, und klicken Sie dann die Insight berechtigt ist **, die Fehler bei der Authentifizierung von den letzten 30 Tagen, gefälschter Domänen**. Wenn Sie Spoofing Schutz noch nicht aktiviert, werden die Einblicke mithilfe des Titels **Aktivieren Spoofing Protection**dazu aufgefordert. 
    
## <a name="about-the-insight-on-the-dashboard"></a>Informationen zu den Einblicke in das dashboard

Die Einblicke in das Dashboard zeigt, wie die folgende Informationen.
  
![Screenshot des Spoofing Intelligence Erkenntnisse](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
Diese Erkenntnisse verfügt über zwei Modi:
  
 **Insight-Modus**. Wenn Sie eine beliebige Spoofing Richtlinie aktiviert haben, zeigt dann die Einblicke, wie viele e-Mails in den letzten 30 Tagen von unseren Spoofing Intelligence-Funktionen betroffen sind. 
  
 **Was passiert, wenn Modus**. Wenn Sie keine Spoofing Richtlinie aktiviert haben, zeigt dann die Einblicke, wie viele e-Mails *würde* durch unsere Spoofing Intelligence-Funktionen in den letzten 30 Tagen betroffene wurde. 
  
In beiden Fällen werden die Domänen mit Spoofing stammen, die in die Einblicke angezeigt in zwei Kategorien getrennt; verdächtige Domäne-Paare und -verdächtigen Domäne-Paare. Diese Kategorien werden weiter in drei verschiedenen Buckets zu prüfende unterteilt. 
  
Ein *Paar Domäne* ist eine Kombination aus der "von:" Adresse und der sendenden-Infrastruktur. 
  
- Die "Von"-Adresse ist die Adresse als von-Adresse Ihre e-Mail-Anwendung angezeigt. Diese Adresse identifiziert den Autor der e-Mail. D. h., das Postfach von der Person oder ein System zum Schreiben der Nachricht verantwortlich. Dies ist die Adresse 5322.From bezeichnet.
    
- Die sendende Infrastruktur oder Absender, ist die organisatorischen Domäne der PTR-Eintrag der sendenden IP-Adresse. Wenn die IP-Adresse des Absenders hat keinen PTR-Eintrag, der Absender wird durch die sendende IP-Adresse identifiziert, mit der 255.255.255.0 Subnetzmaske in CIDR-Notation (/ 24). Beispielsweise ist die IP-Adresse 192.168.100.100 ist die vollständige IP-Adresse des Absenders 192.168.100.100/24.
    
 **Verdächtige Domäne-Paare** enthalten: 
  
- **Vertrauenswürdige Spoofing**. Office 365 empfangen starke Signalen, die diese Domänen verdächtigen, werden basierend auf der historischen sendende Muster und Reputation-Wert der Domänen. Office 365 ist sehr sicher, dass die Domänen spoofing sind und von diesen Domänen gesendete Nachrichten mit weitaus geringerer Wahrscheinlichkeit zu sind. 
    
- **Moderater Confidence Spoofing**. Office 365 empfangen Moderater Signale, die diese Domänen verdächtigen, werden basierend auf zurückliegenden sendenden Muster und Reputation-Wert der Domänen. Office 365 ist einigermaßen sicher, dass die Domänen spoofing sind und von diesen Domänen gesendete Nachrichten legitime sind. Diese Bucket kann möglicherweise falsch positive Ergebnisse (f/s) als vertrauenswürdige Spoofing Bucket enthalten. 
    
 **Nicht-verdächtigen Domäne-Paare** enthalten **Spoofing wiederhergestellt**. Wiederhergestelltes Spoofing sind Domänen, die die explizite Authentifizierung überprüft ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) Fehler, aber unsere erweiterten Authentifizierung überprüft übergeben. Deshalb ist es Office 365 wiederhergestellt, die e-Mail-Nachrichten in Ihrem Auftrag und keine Anti-spoofing-Aktion auf die e-Mail-Nachricht ausgeführt wurde. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>Detaillierte Informationen zu verdächtigen Domäne-Paare aus der Spoofing Intelligence Erkenntnisse anzeigen

1. Klicken Sie auf die Spoofing Intelligence Einblicke klicken Sie auf die Domäne Paare (hoch, Mittel oder wiederhergestellte).
  
Die **Spoofing Intelligence Erkenntnisse** Seite wird angezeigt, das Sie eine Liste der Absender, die nicht authentifizierte Nachrichten in Ihrer Organisation gesendet werden. Die Informationen auf dieser Seite können Sie bestimmen, ob gefälschte Nachrichten oder nicht autorisiert sind, oder wenn Sie weitere Schritte erforderlich müssen. Sie können diese Informationen per Nachrichtenanzahl, das Datum, an das dem Spoofing zuletzt erkannt wurde, das und vieles mehr sortieren. (Klicken Sie auf Spaltenüberschriften, wie etwa **Nachricht zählen** oder **zuletzt gesehen**, zum Beispiel.) 
    
2. Wählen Sie ein Element in der Tabelle auf einen Detailbereich zu öffnen, der umfangreiche Informationen über das Paar Domäne enthält, einschließlich warum wir diese abgefangen, was Sie tun müssen, WhoIs-Daten über den Absender und ähnliche e-Mails, die in Ihrem Mandanten vom selben Absender gesehen haben und eine Zusammenfassung der Domäne. Von hier aus können Sie auch zum Hinzufügen oder Entfernen der Domäne-Paar aus der Liste der sicheren Absender **AllowedToSpoof** wählen. 
  
![Screenshot einer Domäne im Detailfenster Spoofing Intelligence Erkenntnisse](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>Hinzufügen oder Entfernen einer Domäne aus der Liste der sicheren Absender AllowedToSpoof

Sie hinzufügen oder Entfernen einer Domäne aus der Liste der sicheren Absender AllowedToSpoof beim Überprüfen der Domäne Paar im Detailbereich die Spoofing Intelligence Einblicke. Legen Sie einfach die Umschaltfläche entsprechend an.
  
Dies ändert die eindeutige Domäne Paar Kombination aus der Domäne mit Spoofing stammen und die sendende Infrastruktur und bietet keinen Schutz für die gesamte gefälschten Domäne oder der sendenden Infrastruktur isoliert. Angenommen, wenn Sie den folgenden zwei Domäne an den Absender 'AllowedToSpoof' hinzufügen Liste zugelassener: *Manipuliert Domäne* "gmail.com" und *Infrastruktur senden* "Tms *. mx.com",* und klicken Sie dann nur Nachrichten von dieser Domäne Paar Spoofing zugelassen werden soll. Dieser Versuch "tms.mx.com" Spoofing weiterhin weiterer Versuch, "gmail.com" und andere Domänen Spoofing Absender durch Spoofing Intelligence geschützt werden. 
  
## <a name="related-topics"></a>Verwandte Themen

[Erfahren Sie mehr über Spoofing intelligence](learn-about-spoof-intelligence.md)
  
[Anti-spoofing Schutz in Office 365](anti-spoofing-protection.md)
  
[Exemplarische Vorgehensweise - aus einem Dashboard, um einen Einblick](from-a-dashboard-to-an-insight.md)
  
[Exemplarische Vorgehensweise - aus einen detaillierten Bericht zu einer insight](from-a-detailed-report-to-an-insight.md)
  
[Exemplarische Vorgehensweise - aus an einen detaillierten Bericht](from-an-insight-to-a-detailed-report.md)
  


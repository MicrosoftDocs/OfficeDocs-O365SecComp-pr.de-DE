---
title: Exemplarische vorGehensWeise Spoof Intelligence Insight
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: Sehen Sie sich an, wie der neue Spoof Intelligence Insight funktioniert.
ms.openlocfilehash: 83fa1580a0e7c4717581cc5f23b8f525d6b918e0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220325"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>Exemplarische vorGehensWeise: Spoof Intelligence Insight

Mithilfe des Spoof Intelligence-Einblicks können Sie schnell feststellen, welche Absender legitimerweise nicht authentifizierte e-Mails senden. Wenn Sie die Möglichkeit haben, gefälschte Nachrichten zu senden, können Sie das Risiko von falschen positives auf Ihre Benutzer reduzieren.
  
Darüber hinaus können Sie auch Spoof Intelligence-Überwachung verwenden und zulässige Domänen Paare verwalten, um eine zusätzliche Sicherheitsebene bereitzustellen und zu verhindern, dass unsichere Nachrichten in Ihrer Organisation eingehen.
  
Sie können die Spoof Intelligence-Einblicke im &amp; Security Compliance Center verwenden, wenn Ihr Geschäfts-oder Schulkonto Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leserberechtigungen erteilt hat. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).
  
Wenn Sie neue [Berichte und Einblicke im &amp; Office 365 Security Compliance Center](reports-and-insights-in-security-and-compliance.md)haben, kann es hilfreich sein, um zu sehen, wie Sie einfach von einem Dashboard zu einem Einblicks-und empfohlenen Aktionen navigieren können.
  
Sie können die Spoof Intelligence-Einblicke von mehr als einem Dashboard im &amp; Security Compliance Center anzeigen. Unabhängig davon, welches Dashboard Sie sich ansehen, bietet die Insight die gleichen Details und ermöglicht es Ihnen, schnell die gleichen Aufgaben auszuführen.
  
Dies ist eine von mehreren exemplarischen Vorgehens &amp; weisen für das Security Compliance Center. Informationen zum Navigieren in Berichten und Einblicken finden Sie unter Exemplarische Vorgehensweisen im Abschnitt Verwandte Themen.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>Einführung in die Spoof Intelligence-Einblicke &amp; im Security Compliance Center

1. Um zu beginnen, müssen Sie [das Security &amp; Compliance Center besuchen](go-to-the-securitycompliance-center.md).
    
2. Wechseln Sie im &amp; Security Compliance Center zu **Threat Management** \> **Dashboard.**
    
3. Suchen Sie **** in der Zeile Einblicke nach dem Spoof Intelligence Insight. Wenn Sie Spoof Intelligence aktiviert haben, ist die Einsicht berechtigte **gefälschte Domänen, die die Authentifizierung der letzten 30 Tage fehlgeschlagen**. Wenn Sie keinen Spoof-Schutz aktiviert haben, werden Sie von der Insight dazu aufgefordert, indem Sie den Titel **enable Spoof Protection**verwenden. 
    
## <a name="about-the-insight-on-the-dashboard"></a>Informationen zu den Einblicken auf dem Dashboard

Die Einblicke auf das Dashboard zeigen Ihnen Informationen wie diese.
  
![Screenshot von Spoof Intelligence Insight](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
Dieser Einblick hat zwei Modi:
  
 **Insight-Modus**. Wenn Sie eine Spoof-Richtlinie aktiviert haben, zeigt die Einsicht, wie viele e-Mails in den letzten 30 Tagen durch unsere Spoof Intelligence-Funktionen beeinflusst wurden. 
  
 **Was ist, wenn Modus**. Wenn Sie keine Spoof-Richtlinie aktiviert haben, zeigt die Einsicht, wie viele e-Mails ** in den letzten 30 Tagen durch unsere Spoof Intelligence-Funktionen beeinflusst wurden. 
  
In beiden Fällen werden die in der Insight angezeigten Spoof-Domänen in zwei Kategorien unterteilt. verdächtige Domänen Paare und nicht verdächtige Domänen Paare. Diese Kategorien werden weiter in drei verschiedene Buckets unterteilt, die Sie überarbeiten können. 
  
Ein *Domänenpaar* ist eine Kombination aus der "from:"-Adresse und der sendenden Infrastruktur. 
  
- Die "von"-Adresse ist die Adresse, die von Ihrer e-Mail-Anwendung als Absenderadresse angezeigt wird. Diese Adresse identifiziert den Autor der e-Mail. Das heißt, das Postfach der Person oder des Systems, das für das Schreiben der Nachricht zuständig ist. Dies wird manchmal auch als 5322. from-Adresse bezeichnet.
    
- Die sendende Infrastruktur oder der Absender ist die Organisationsdomäne des PTR-Eintrags der sendenden IP-Adresse. Wenn die sendende IP-Adresse keinen PTR-Eintrag enthält, wird der Absender von der sendenden IP mit der Subnetzmaske 255.255.255.0 in CIDR-Notation (/24) identifiziert. Wenn die IP-Adresse beispielsweise 192.168.100.100 lautet, lautet die vollständige IP-Adresse des Absenders 192.168.100.100/24.
    
 Zu den **verdächtigen Domänen Paaren** gehört Folgendes: 
  
- **Spoof mit hoher Vertrauens**Würdigkeit. Office 365 hat starke Signale erhalten, dass diese Domänen aufgrund der historischen Sende Muster und der Reputationsbewertung der Domänen verdächtig sind. Office 365 ist sehr zuversichtlich, dass die Domänen gefälscht sind und dass Nachrichten, die von diesen Domänen gesendet werden, wahrscheinlich nicht legitim sind. 
    
- **Moderate Vertrauens Spoof**. Office 365 hat moderat signalisiert, dass diese Domänen aufgrund der historischen Sende Muster und der Reputationsbewertung der Domänen verdächtig sind. Office 365 ist moderat zuversichtlich, dass die Domänen gefälscht sind und dass Nachrichten, die von diesen Domänen gesendet werden, legitim sind. Dieser Bucket hat eine größere Wahrscheinlichkeit, dass falsch positive Ergebnisse (FPs) enthalten sind als das hoch vertrauenswürdige Spoof-Bucket. 
    
 Bei **nicht verdächtigen Domänen Paaren** handelt es sich um eine **gerettete Spoof**. "Rescued Spoof" sind Domänen, bei denen die expliziten Authentifizierungsprüfungen ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) fehlgeschlagen sind, aber unsere erweiterten Authentifizierungsprüfungen bestanden haben. Als Folge davon hat Office 365 die e-Mails in Ihrem Namen gerettet, und es wurde keine Antispoofing-Aktion für die e-Mail ausgeführt. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>Anzeigen detaillierter Informationen zu verdächtigen Domänen Paaren aus der Spoof Intelligence-Einsicht

1. Klicken Sie auf der Spoof Intelligence-Einblicke auf beliebige Domänen Paare (hoch, moderat oder gerettet).
  
Auf der Seite **Spoof Intelligence Insight** wird eine Liste der Absender angezeigt, die nicht authentifizierte e-Mails an Ihre Organisation senden. Anhand der Informationen auf dieser Seite können Sie ermitteln, ob gefälschte Nachrichten autorisiert sind oder ob Sie weitere Maßnahmen ergreifen müssen. Sie können die Informationen nach Nachrichtenanzahl, das Datum, an dem die Spoof zuletzt erkannt wurde, und vieles mehr sortieren. (Klicken Sie beispielsweise auf Spaltenüberschriften, beispielsweise **Nachrichtenanzahl** oder **zuletzt gesehen**.) 
    
2. Wählen Sie ein Element in der Tabelle aus, um einen Detailbereich zu öffnen, der umfangreiche Informationen über das Domänenpaar enthält, einschließlich der Gründe, warum wir dies erfasst haben, was Sie tun müssen, eine Domänen Zusammenfassung, WhoIs-Daten zum Absender und ähnliche e-Mails, die wir in Ihrem Mandanten vom gleichen Absender gesehen haben. Von hier aus können Sie auch das Domänenpaar aus der Liste der sicheren Absender von **AllowedToSpoof** hinzufügen oder daraus entfernen. 
  
![Screenshot einer Domäne im Detailbereich "Spoof Intelligence Insight"](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>Hinzufügen oder Entfernen einer Domäne aus der Liste der sicheren Absender von AllowedToSpoof

Sie können eine Domäne aus der Liste der sicheren Absender von AllowedToSpoof hinzufügen oder entfernen, während Sie das Domänenpaar im Detailbereich des Spoof Intelligence Insight überprüfen. Legen Sie die Umschaltfläche einfach entsprechend fest.
  
Dadurch wird die Kombination der eindeutigen Domänen Paare der gefälschten Domäne und der sendenden Infrastruktur geändert, und es wird keine Abdeckung der gesamten gefälschten Domäne oder der sendenden Infrastruktur isoliert. Wenn Sie beispielsweise das folgende Domänenpaar der Absender Zulassungsliste "AllowedToSpoof" hinzufügen: *spoofEd Domain* "gmail.com" und " ** TMS *. MX.com",* dann wird nur e-Mails von diesem Domänenpaar gefälscht werden dürfen. Andere Absender, die versuchen, "gmail.com" zu fälschen, und andere Domänen, die "tms.mx.com" versuchen zu spoofen, werden weiterhin durch Spoof-Intelligence geschützt. 
  
## <a name="related-topics"></a>Verwandte Themen

[Weitere Informationen zu Spoofing Intelligence](learn-about-spoof-intelligence.md)
  
[Antispoofingschutz in Office 365](anti-spoofing-protection.md)
  
[Exemplarische Vorgehensweise – Vom Dashboard zum Einblick](from-a-dashboard-to-an-insight.md)
  
[Exemplarische Vorgehensweise – Vom detaillierten Bericht zum Einblick](from-a-detailed-report-to-an-insight.md)
  
[Exemplarische Vorgehensweise – Vom Einblick zum detaillierten Bericht](from-an-insight-to-a-detailed-report.md)
  


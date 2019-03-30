---
title: Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft Exchange Online Protection (EOP) bietet viele verschiedene Berichte an, mit deren Hilfe Sie den allgemeinen Status und die Integrität Ihrer Organisation ermitteln können. Außerdem gibt es Tools, mit denen Sie die Problembehebung für bestimmte Ereignisse (wenn beispielsweise eine Nachricht nicht beim gewünschten Empfänger ankommt) durchführen können, sowie Überwachungsberichte zur Einhaltung von Vorschriften. In der folgenden Tabelle sind die für EOP-Administratoren verfügbaren Berichte und Problembehandlungstools beschrieben.
ms.openlocfilehash: fcefa14991d074f1f4459007c16dd7f4df1cedd1
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000948"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Berichterstellung und Nachrichtenablaufverfolgung in Exchange Online Protection

Microsoft Exchange Online Protection (EOP) bietet viele verschiedene Berichte an, mit deren Hilfe Sie den allgemeinen Status und die Integrität Ihrer Organisation ermitteln können. Außerdem gibt es Tools, mit denen Sie die Problembehebung für bestimmte Ereignisse (wenn beispielsweise eine Nachricht nicht beim gewünschten Empfänger ankommt) durchführen können, sowie Überwachungsberichte zur Einhaltung von Vorschriften. 

## <a name="usage-reports"></a>Verwendungsberichte

**Office 365-Gruppen-Aktivitäten** Anzeigen von Informationen zur Anzahl der Office 365-Gruppen, die erstellt und verwendet werden.  

**E-Mail-Aktivität** Informationen zur Anzahl der Nachrichten, die in der gesamten Organisation sowie von einem bestimmten Benutzer gesendet, empfangen und gelesen wurden.  

**Nutzung der E-Mail-Apps** Zeigen Sie Informationen zu den verwendeten E-Mail-Apps an. Diese umfassen die Gesamtzahl der Verbindungen für die einzelnen Apps und die Versionen von Outlook, die eine Verbindung herstellen.    

**Postfachnutzung** Informationen zum verwendeten Speicherplatz, Verbrauch von Kontingenten, zur Elementanzahl und zu letzten Aktivitäten für Postfächer (Senden oder Lesen).

Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Office 365-Berichte im Admin Center-Office 365-Gruppen](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [Office 365-Berichte im Admin Center - E-Mail-Aktivitäten](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [Office 365-Berichte im Admin Center - Nutzung der E-Mail-Apps](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [Office 365-Berichte im Admin Center - Postfachnutzung](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-microsoft-365-admin-center"></a>Sicherheits &amp; Kompatibilitätsberichte im Microsoft 365 Admin Center

Diese erweiterten Berichte bieten eine interaktive Berichterstellung für EOP-Administratoren, die Zusammenfassungsinformationen und das Anzeigen von Detailinformationen umfasst.  

**Advanced Threat Protection (ATP)** Zeigt Informationen über sichere Links und sichere Anlagen, die zu ATP gehören.  

**EoP** Informationen zu Malware-Entdeckungen, gefälschten e-Mails, Spam Entdeckungen und Nachrichtenübermittlung an und von Ihrer Organisation anzeigen.  

[Anzeigen der Berichte zu Advanced Threat Protection und Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a>Benutzerdefinierte Berichte mithilfe von Microsoft Graph

Programmgesteuertes Erstellen von Berichten, die im Microsoft 365 Admin Center mithilfe von Microsoft Graph verfügbar sind siehe Unterthemen zum [Arbeiten mit Office 365-Nutzungsberichten in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135) 

##<a name="custom-reports-using-reporting-web-services"></a>Benutzerdefinierte Berichte mit Berichtswebdiensten

Erstellen Sie programmgesteuert Berichte aus den verfügbaren PowerShell-Cmdlets für Exchange Online Protection mithilfe der REST/ODATA2-Abfrage Filterung.

Weitere Informationen finden Sie unter [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926) 

##<a name="message-trace"></a>Nachrichtenablaufverfolgung

Ermöglicht das Nachverfolgen von E-Mails auf dem Weg durch EOP. Sie können ermitteln, ob eine E-Mail vom Dienst empfangen, abgelehnt, zurückgestellt oder zugestellt wurde. Außerdem werden die Aktionen der Nachricht gezeigt, bevor diese ihren finalen Status erreicht hat.  

Mit diesen Informationen können Sie in effizienter Weise Fragen der Benutzer beantworten, Probleme mit dem Nachrichtenfluss behandeln und Richtlinienänderungen überprüfen und müssen seltener den technischen Support um Unterstützung bitten.  

Siehe [Ablaufverfolgung einer e-Mail-Nachricht](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 

## <a name="audit-logging"></a>Überwachungsprotokollierung

Verfolgt bestimmte Änderungen durch Administratoren Ihrer Organisation. Diese Berichte können Sie zum Behandeln von Konfigurationsproblemen sowie zum Ermitteln der Ursache von Sicherheits- oder Kompatibilitätsproblemen heranziehen.  Weitere Informationen finden Sie unter [Auditing Reports in EoP](auditing-reports-in-eop.md) 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a>Meldung und Verfügbarkeit und Latenz Nachrichtenverfolgungsdaten

In der folgenden Tabelle wird beschrieben, wann und für wie lange EOP-Berichte und Nachrichtenverfolgungsdaten verfügbar sind.
  
||||
|:-----|:-----|:-----|
|**Berichttyp** <br/> |**Daten verfügbar für (Rückwirkungsfrist)** <br/> |**Latenz** <br/> |
|Zusammenfassungsberichte zum E-Mail-Schutz  <br/> |90 Tage  <br/> |Die Aggregation von Nachrichtendaten ist meistens innerhalb von 24 bis 48 Stunden abgeschlossen. Kleinere inkrementelle, aggregierte Änderungen können bis zu 5 Tage lang auftreten.  <br/> |
|Detailberichte zum E-Mail-Schutz  <br/> |90 Tage  <br/> |Bei Detaildaten, die weniger als 7 Tage alt sind, sollten Daten innerhalb von 24 Stunden erscheinen, sind aber möglicherweise erst 48 Stunden später abgeschlossen. Einige kleinere schrittweise Änderungen können bis zu 5 Tagen dauern.  <br/> Zum Anzeigen von Detailberichten für Nachrichten, die älter als 7 Tage sind, kann es einige Stunden dauern, bis die Ergebnisse der Nachrichtenablaufverfolgung ausgegeben werden.  <br/> |
|Daten der Nachrichtenablaufverfolgung  <br/> |90 Tage  <br/> |Wenn Sie eine Nachrichtenverfolgung für Nachrichten starten, die weniger als 7 Tage alt sind, sollten die Nachrichten innerhalb von 5-30 Minuten erscheinen.  <br/> Wenn Sie eine Ablaufverfolgung für Nachrichten ausführen, die älter als 7 Tage sind, kann es einige Stunden dauern, bis Ergebnisse ausgegeben werden.  <br/> |
   
> [!NOTE]
> Datenverfügbarkeit und Latenz sind identisch, unabhängig davon, ob Sie über das Microsoft 365 Admin Center oder die Remote-PowerShell angefordert werden. 
  


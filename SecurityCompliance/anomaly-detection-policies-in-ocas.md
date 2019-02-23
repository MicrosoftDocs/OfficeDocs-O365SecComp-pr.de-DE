---
title: Anomalieerkennungsrichtlinien in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/15/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: 'Anomalie-Erkennungsrichtlinien in Office 365 Cloud App Security verwenden Sie integrierte Algorithmen, um mögliche Probleme aufzudecken. Sie sollten über mindestens eine Anomalie-Erkennungsrichtlinie verfügen, die Sie (bei der Erstellung) mithilfe von Filtern optimieren können. '
ms.openlocfilehash: 5308af139a46dad0793ed7eedacab0aee62dcc6c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220675"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Anomalieerkennungsrichtlinien in Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](ocas-conditional-access-app-control.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |
   
Beginnend mit der [Microsoft Cloud App Security release 116](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116)enthält Office 365 Cloud App Security mehrere vordefinierte Anomalie-Erkennungsrichtlinien ("Out of the Box"), die Benutzer-und Entitäts Verhaltensanalysen (UEBA) und Maschinelles Lernen (ml) umfassen.
  
![Um Ihre Erkennungsrichtlinien für Anomalien anzuzeigen, wählen \> Sie Steuerungsrichtlinien aus.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Diese Erkennungsrichtlinien für Anomalien bieten sofortige Ergebnisse, indem Sie sofort Erkennungen bereitstellen, die zahlreiche Verhaltensanomalien für Ihre Benutzer und die Computer und Geräte, die mit Ihrem Netzwerk verbunden sind, abzielen. Darüber hinaus werden durch die neuen Richtlinien weitere Daten aus dem Sicherheits Erkennungsmodul für die Cloud-App zur Verfügung gestellt, um den Ermittlungsprozess zu beschleunigen und laufende Bedrohungen einzudämmen.
  
Als globaler Administrator oder Sicherheitsadministrator von Office 365 können Sie die Standardrichtlinien, die mit Office 365 Cloud App Security zur Verfügung stehen, überprüfen und gegebenenfalls überarbeiten.
  
 > [!IMPORTANT]
> Es gibt einen anfänglichen Lernzeitraum von sieben (7) Tagen, in dem anomale Verhaltens Warnungen nicht ausgelöst werden. Der Algorithmus zur Erkennung von Anomalien wurde optimiert, um die Anzahl falsch positiver Warnungen zu reduzieren. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Stellen Sie Folgendes sicher:
  
- Ihre Organisation verfügt über [Office 365 Cloud App Security](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).
    
- Die [Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für ihre Office 365-Umgebung aktiviert. 
    
- Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Anzeigen der Anomalie-Erkennungsrichtlinien

1. Wechseln Sie als globaler Administrator oder Sicherheitsadministrator zum Sicherheitsportal der Cloud-app ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.<br>Dadurch gelangen Sie zur Seite Office 365 Cloud App Security Policies.
    
2. Wählen Sie in der Liste **Typ** die Option **Anomalie-Erkennungsrichtlinie**aus.<br>Die standardmäßigen (oder vorhandenen) Erkennungsrichtlinien für Anomalien Ihrer Organisation werden angezeigt.<br>![Anomalieerkennungsrichtlinien in Office 365 Cloud App Security](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. Wählen Sie eine Richtlinie aus, um Ihre Einstellungen zu überarbeiten.
    
4. Wählen Sie **Update** aus, um die Änderungen zu speichern. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>Weitere Informationen zu Anomalie-Erkennungsrichtlinien

Anomalie-Erkennungsrichtlinien werden automatisch aktiviert; Office 365 Cloud App Security hat jedoch einen anfänglichen Lernzeitraum von sieben Tagen, in dem nicht alle Warnungen zur Anomalie-Erkennung ausgelöst werden. Danach wird jede Sitzung mit der Aktivität verglichen, wenn Benutzer aktiv waren, IP-Adressen, Geräte usw., die im letzten Monat erkannt wurden, und die Risikobewertung dieser Aktivitäten. Diese Erkennungen sind Teil des Erkennungsmoduls für die heuristische Anomalie, das Ihre Umgebung profiliert und Warnungen in Bezug auf eine Baseline auslöst, die für die Aktivität Ihrer Organisation erlernt wurde. Diese Entdeckungen nutzen auch maschinelle Lernalgorithmen, die zum Profilieren der Benutzer und Anmelde Muster entworfen wurden, um falsch positive Ergebnisse zu reduzieren.
  
Anomalien werden durch Überprüfen der Benutzeraktivität erkannt. Das Risiko wird anhand von über 30 verschiedenen Risikoindikatoren bewertet, die in mehrere Risikofaktoren gruppiert sind, wie beispielsweise riskante IP-Adressen, Anmeldefehler, Administrator Aktivität, inaktive Konten, Standort, unmöglich Reisen, Geräte-und Benutzer-Agent und Aktivitätsrate.
  
Basierend auf den Richtlinien Ergebnissen werden Sicherheitswarnungen ausgelöst. Office 365 Cloud App Security sucht bei jeder Benutzersitzung in Office 365 und benachrichtigt Sie, wenn etwas geschieht, das sich von der Grundlinie Ihrer Organisation oder von der regulären Aktivität eines Benutzers unterscheidet.
  
In der folgenden Tabelle werden die standardmäßigen Erkennungsrichtlinien für Anomalien, ihre Funktion und ihre Funktionsweise beschrieben.
  
|**Name der Anomalie-Erkennungsrichtlinie**|**Funktionsweise**|
|:-----|:-----|
|Unmöglich Reisen  <br/> |Identifiziert zwei Benutzeraktivitäten (eine einzelne oder mehrere Sitzungen), die aus geografisch entfernten Standorten innerhalb eines Zeitraums liegen, der kürzer als der Zeitpunkt ist, zu dem der Benutzer von der ersten Stelle zur zweiten zu reisen, was darauf hinweist, dass eine andere der Benutzer verwendet die gleichen Anmeldeinformationen. Diese Erkennung nutzt einen Computer Lernalgorithmus, der offensichtliche "falsch positive Ergebnisse" ignoriert, die zur unmöglichen Reise Bedingung beitragen, beispielsweise VPNs und Standorte, die von anderen Benutzern in der Organisation regelmäßig verwendet werden. Die Erkennung hat einen anfänglichen Lernzeitraum von sieben Tagen, in dem Sie das Aktivitätsmuster eines neuen Benutzers erlernt.  <br/> |
|Aktivität aus unregelmäßigem Land  <br/> |Berücksichtigt vergangene Aktivitäts Standorte, um neue und seltene Standorte zu ermitteln. Das Anomalie-Erkennungsmodul speichert Informationen zu früheren Speicherorten, die von Benutzern in der Organisation verwendet werden. Eine Warnung wird ausgelöst, wenn eine Aktivität an einem Ort stattfindet, der weder vor kurzem noch vom Benutzer oder von einem anderen Benutzer in der Organisation besucht wurde.  <br/> |
|Aktivität von anonymen IP-Adressen  <br/> |Gibt an, dass Benutzer von einer IP-Adresse aktiv waren, die als anonyme Proxy-IP-Adresse identifiziert wurde. Diese Proxys werden von Personen verwendet, die die IP-Adresse Ihres Geräts ausblenden möchten und möglicherweise für böswillige Absicht verwendet werden. Diese Erkennung nutzt einen Computer Lernalgorithmus, der "falsch positive Ergebnisse" reduziert, beispielsweise falsch gekennzeichnete IP-Adressen, die von Benutzern in der Organisation weitgehend verwendet werden.  <br/> |
|Aktivität von verdächtigen IP-Adressen  <br/> |Identifiziert, dass Benutzer von einer IP-Adresse aktiv waren, die von Microsoft Threat Intelligence als riskant identifiziert wurde. Diese IP-Adressen sind an böswilligen Aktivitäten wie Botnet C&amp;c beteiligt und können auf ein kompromittiertes Konto hindeuten. Diese Erkennung nutzt einen Computer Lernalgorithmus, der "falsch positive Ergebnisse" reduziert, beispielsweise falsch gekennzeichnete IP-Adressen, die von Benutzern in der Organisation weitgehend verwendet werden.  <br/> |
|Ungewöhnliche Aktivitäten (nach Benutzer)  <br/> | Identifiziert Benutzer, die ungewöhnliche Aktivitäten wie z. b. ausführen:  <br/>  --Mehrere Dateidownloads  <br/>  --Dateifreigabe Aktivitäten  <br/>  --Löschaktivitäten für Dateien  <br/>  -Identitätswechsel Aktivitäten  <br/>  --Administrative Aktivitäten  <br/>  Diese Richtlinien suchen nach Aktivitäten innerhalb einer einzelnen Sitzung im Hinblick auf die gelernte Grundlinie, die auf einen Verletzungsversuch hinweisen könnte. Diese Entdeckungen nutzen einen Computer Lernalgorithmus, der das Muster der Benutzer protokolliert und falsch positive Ergebnisse reduziert. Diese Erkennungen sind Teil des Erkennungsmoduls für die heuristische Anomalie, das Ihre Umgebung profiliert und Warnungen in Bezug auf eine Baseline auslöst, die für die Aktivität Ihrer Organisation erlernt wurde.  <br/> |
|Mehrere fehlgeschlagene Anmeldeversuche  <br/> |Identifiziert Benutzer, bei denen mehrere Anmeldeversuche in einer einzelnen Sitzung im Hinblick auf die gelernte Grundlinie fehlgeschlagen sind, was auf einen Verletzungsversuch hindeuten könnte.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Erkennung von Anomalien der Erkennungs Warnungen

Sobald Warnungen eingehen, können Sie diese Warnungen schnell selektieren und bestimmen, welche zuerst verarbeitet werden sollen. Wenn Sie Kontext für eine Warnung haben, können Sie das größere Bild sehen und ermitteln, ob tatsächlich etwas bösartiges geschieht. Gehen Sie folgendermaßen vor, um mit der Erkundung einer Warnung zu beginnen:
  
1. Wechseln Sie als globaler Administrator oder Sicherheitsadministrator zum Sicherheitsportal der Cloud-app ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an. 
    
2. Wählen **** Sie Alerts aus, um Ihre Benachrichtigungen anzuzeigen. 
    
3. Führen Sie die folgenden Schritte aus, um den Kontext für eine Warnung abzurufen:
    
4. Wählen Sie **Aktivitätsprotokoll** **untersuchen** \> aus.
    
5. Wählen Sie ein Element aus, beispielsweise einen Benutzer oder eine IP-Adresse. Dadurch wird die relevante Insights-Schublade geöffnet.<br>![Im Aktivitätsprotokoll können Sie eine IP-Adresse untersuchen.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. Klicken Sie in der entsprechenden Einblicke-Schublade auf einen verfügbaren Befehl, beispielsweise ein Symbol im Abschnitt **ähnliche anzeigen** .<br> ![Klicken Sie auf das Symbol Uhr, um Aktivitäten anzuzeigen, die innerhalb von 48 Stunden nach einer ausgewählten Aktivität durchgeführt wurden.](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. Erhalten Sie Einblicke in das ausgewählte Element, indem Sie weitere Details zu diesem Element erkunden.
    
Eine Warnung bei mehreren fehlgeschlagenen Anmeldungen kann in der Tat verdächtig sein und auf einen möglichen Brute-Force-Angriff hindeuten. Eine solche Warnung kann jedoch auch eine Anwendung Fehlkonfiguration sein, wodurch die Warnung als gutartige true positive. Wenn eine Warnung bei mehreren fehlgeschlagenen Anmeldungen mit zusätzlichen verdächtigen Aktivitäten angezeigt wird, besteht eine höhere Wahrscheinlichkeit, dass ein Konto kompromittiert wird. Nehmen wir beispielsweise an, dass eine Warnung mit mehreren fehlgeschlagenen Anmeldeinformationen von Aktivitäten aus einer TOR-IP-Adresse und unmöglichen Reiseaktivitäten, sowohl starke Indikatoren als Kompromiss, gefolgt wird. Möglicherweise sehen Sie sogar, dass derselbe Benutzer eine massendownload Aktivität durchgeführt hat, was oft ein Indikator für die Durchführung der Datenfilterung durch den Angreifer ist. Es handelt sich um solche, die Sie in Office 365 Cloud App Security erkunden können, um Ihre Benachrichtigungen anzuzeigen und zu selektieren und gegebenenfalls Maßnahmen zu ergreifen.
  
## <a name="next-steps"></a>Nächste Schritte

- [Bereitstellen der App-Steuerung für bedingten Zugriff für Office 365-Apps](ocas-deploy-conditional-access-app-control.md)

- [Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)

- [Integrieren Ihres SIEM-Servers](integrate-your-siem-server-with-office-365-cas.md)
    
- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
    


---
title: Anomalieerkennungsrichtlinien in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: 'Anomalie Erkennungsrichtlinien in Office 365-Cloud-App-Sicherheit verwenden integrierte Algorithmen, um potenzielle Probleme aufdecken. Sie sollten mindestens eine Anomalie Erkennung Richtlinie verfügen, die Sie optimiert werden können (bei der Erstellung) mithilfe von Filtern. '
ms.openlocfilehash: 62e2db3ba46f41bce5c5c4fab9e6c685838d68e8
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015076"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Anomalieerkennungsrichtlinien in Office 365 Cloud App Security

Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](integrate-your-siem-server-with-office-365-cas.md) <br/> |[Starten Sie die Nutzung](utilization-activities-for-ocas.md) <br/> |
   
Ab [Microsoft Cloud App-Sicherheit Version 116](https://docs.microsoft.com/cloud-app-security/release-notes), enthält Office 365-Cloud-App-Sicherheit mehrere vordefinierte Anomalie Erkennungsrichtlinien ("sofort einsetzbar"), die Benutzer und Entität Verhalten Analytics (UEBA) und Computer lernen (ML) enthalten.
  
![Wählen Sie zum Anzeigen Ihrer Anomalie Erkennungsrichtlinien Steuerelement \> Richtlinien.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Diese Anomalie Erkennungsrichtlinien bieten sofortige Ergebnisse durch Bereitstellen sofortigen erkannte, Zielgruppenadressierung zahlreiche Verhalten Abweichung über Ihre Benutzer und Computer und Geräte mit dem Netzwerk verbunden. Darüber hinaus stellen die neuen Richtlinien weitere Daten aus der Cloud App Erkennung Engine zur Untersuchung beschleunigen und die laufende Bedrohungen enthalten.
  
Als [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)können Sie überprüfen, und Sie bei Bedarf überarbeiten die Standardrichtlinien, die mit Office 365-Cloud-App-Sicherheit verfügbar sind.
  
 > [!IMPORTANT]
> Es gibt ein Zeitraum anfänglichen Learning sieben (7) Tage in denen abweichendem Verhalten Benachrichtigungen nicht ausgelöst werden. Der Algorithmus Anomalie Erkennung wird zur Verringerung der Anzahl von falsch positiven Warnungen optimiert. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Stellen Sie Folgendes sicher:
  
- Ihre Organisation verfügt [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).
    
- [Protokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Office 365-Umgebung aktiviert. 
    
- Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Zeigen Sie Ihre Anomalie Erkennungsrichtlinien

1. Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
    Dadurch gelangen Sie zur Seite Office 365 Cloud App-Sicherheitsrichtlinien.
    
4. Wählen Sie in der Liste **Typ** **Anomalie Erkennung Richtlinie**aus.
    
    Ihre Organisation Standard (oder einer vorhandenen) Anomalie Erkennungsrichtlinien werden angezeigt.
    
    ![Mehrere Anomalie Erkennungsrichtlinien sind standardmäßig verfügbar in Office 365-Cloud-App-Sicherheit](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
5. Wählen Sie eine Richtlinie zum Lesen oder Bearbeiten der Einstellungen aus.
    
6. Wählen Sie **Update** aus, um die Änderungen zu speichern. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>Erfahren Sie mehr über Anomalie Erkennungsrichtlinien

Anomalie Erkennungsrichtlinien sind automatisch aktiviert. Office 365-Cloud-App-Sicherheit verfügt jedoch über einen Zeitraum anfänglichen Learning sieben Tage, die während der nicht alle, die Anomalie Erkennung Warnungen ausgelöst werden. Danach wird jede Sitzung auf die Aktivität, wenn der Benutzer aktiv waren, IP-Adressen, Geräte usw. erkannt wird, über den letzten Monat und das Risiko Score dieser Aktivitäten verglichen. Diese erkannte sind Teil der heuristische Anomalie Erkennung Engine, die Profile von Ihrer Umgebung und löst die Benachrichtigungen in Bezug auf eine Baseline, die für Ihre Organisation Aktivität ausfindig gemacht wurde. Diese erkannte nutzen auch Computer Learning Algorithmen entwickelt, um die profile der Benutzer und melden Sie sich in Muster, um falsch positive Ergebnisse zu reduzieren.
  
Abweichung werden durch Scannen Benutzeraktivität erkannt. Das Risiko wird ausgewertet, verfolgen über 30 verschiedene Risikoindikatoren in mehrere Risiko Faktoren, wie riskant IP-Adresse, Anmeldefehler, Admin-Aktivität, inaktiven Konten, Speicherort, unmöglich Reisen, Geräte und Benutzer-Agent und Aktivität Rate gruppiert.
  
Basierend auf den Gruppenrichtlinienergebnissen, werden Sicherheitswarnungen ausgelöst. Office 365-Cloud-App-Sicherheit befasst sich mit jeder benutzersitzung in Office 365 und gewarnt, wenn ein Fehler auftritt, die sich aus der Grundlinie Ihrer Organisation oder aus einem regulären Benutzeraktivität unterscheidet.
  
In der folgenden Tabelle werden die Standardrichtlinien für Anomalie Erkennung, ihre Funktion und deren Funktionsweise beschrieben.
  
|**Anomalie Erkennung Richtlinienname**|**Funktionsweise**|
|:-----|:-----|
|Unmöglich travel  <br/> |Identifiziert die zwei Benutzeraktivitäten (ist eine einzelne oder mehrere Sitzungen) stammt geografisch entfernten Standorten innerhalb eines Zeitraums kürzer als die Zeit es würde getroffen haben Reisen aus dem ersten Speicherort der zweiten, das angibt, dass dem Benutzer einen anderen Benutzer wird die gleichen Anmeldeinformationen verwendet. Diese Erkennung nutzt einen Computer erlernen Hashalgorithmus offensichtlich "falsch positive Ergebnisse" Belohnung von der Bedingung unmöglich Geschäftsreisen wie VPNs und Speicherorte von anderen Benutzern in der Organisation regelmäßig verwendet ignoriert. Die Erkennung verfügt über einen Zeitraum anfänglichen Learning sieben Tage in denen sie einen neuen Benutzer Aktivität Muster lernen.  <br/> |
|Aktivität aus seltene Land  <br/> |Ältere Aktivität Speicherorte betrachtet, um neue und seltene Speicherorte zu bestimmen. Das Anomalie Erkennungsmodul speichert Informationen zu vorherigen Speicherorte von Benutzern in der Organisation verwendet. Wenn eine Aktivität von einem Speicherort auftritt, die nicht kürzlich oder nie vom Benutzer oder von jedem Benutzer in der Organisation besucht wurde, wird eine Warnung ausgelöst.  <br/> |
|Aktivität von anonymen IP-Adressen  <br/> |Gibt an, dass Benutzer aus einer IP-Adresse aktiv waren, die als anonyme Proxy IP-Adresse identifiziert wurde. Diese Proxys werden von Personen verwendet, die IP-Adresse des Geräts ausblenden möchten, und für böswilligen Absichten verwendet werden kann. Diese Erkennung nutzt einen Computer erlernen Algorithmus, der reduziert "falsch positive Ergebnisse", wie beispielsweise falsch bereichsspezifische IP-Adressen, die häufig von Benutzern in der Organisation verwendet werden.  <br/> |
|Aktivität von verdächtigen IP-Adressen  <br/> |Gibt an, dass Benutzer aus einer IP-Adresse aktiv waren, die von Microsoft Threat Intelligence als riskant identifiziert wurde. Diese IP-Adressen sind beteiligt böswillige Aktivitäten, wie Botnet C&amp;C, und darauf hinweisen kompromittierten Konto. Diese Erkennung nutzt einen Computer erlernen Algorithmus, der reduziert "falsch positive Ergebnisse", wie beispielsweise falsch bereichsspezifische IP-Adressen, die häufig von Benutzern in der Organisation verwendet werden.  <br/> |
|Ungewöhnliche Aktivitäten (durch Benutzer)  <br/> | Identifiziert die Benutzer, die ungewöhnliche Aktivitäten ausführen:  <br/>  --Mehrere Dateidownloads  <br/>  --Dateifreigabe-Aktivitäten  <br/>  --Datei löschen Aktivitäten  <br/>  --Identitätswechsel Aktivitäten  <br/>  --Administrativer Aktivitäten  <br/>  Diese Richtlinien Suchen nach Aktivitäten innerhalb einer einzelnen Sitzung in Bezug auf die geplante gelernt haben, die auf einer Verletzung Versuch angeben kann. Diese erkannte nutzen ein Computers erlernen Algorithmus, mit dem Muster Profile der Benutzer anmelden und falsch positive Ergebnisse reduziert. Diese erkannte sind Teil der heuristische Anomalie Erkennung Engine, die Profile von Ihrer Umgebung und löst die Benachrichtigungen in Bezug auf eine Baseline, die für Ihre Organisation Aktivität ausfindig gemacht wurde.  <br/> |
|Mehrere fehlgeschlagene Anmeldeversuche  <br/> |Benutzer, die mehrere Anmeldeversuche in einer einzigen Sitzung fehlgeschlagen identifiziert in Bezug auf die geplante gelernt haben, die einer Verletzung Versuch angeben kann.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Ursachenanalyse Anomalie Erkennung Benachrichtigungen

Wie Benachrichtigungen empfangen werden, können Sie diese Warnungen schnell selektieren und bestimmen, welche zuerst behandeln. Mit Kontext für eine Benachrichtigung können Sie finden im Bild, und bestimmen, ob etwas böswilligen tatsächlich geschieht. Verwenden Sie das folgende Verfahren für den Einstieg erkunden eine Warnung:
  
1. Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. 
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
4. Wählen Sie **Benachrichtigungen** , um Warnungen anzuzeigen. 
    
5. Wenn Kontext für eine Benachrichtigung erhalten möchten, gehen Sie folgendermaßen vor:
    
1. Wählen Sie **untersuchen** \> **Aktivitätsprotokolls**.
    
2. Wählen Sie ein Element, wie Sie einen Benutzer oder eine IP-Adresse. Die relevanten Insights Papiereinzug wird geöffnet.
    
    ![Überprüfen Sie im Protokoll Aktivität eine IP-Adresse.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
3. Klicken Sie auf einen verfügbaren Befehl, wie ein Symbol im Abschnitt **Ähnliche Elemente anzeigen** , in der entsprechenden Insights Papiereinzug. 
    
    ![In der entsprechenden Insights Papiereinzug können Sie das Uhrsymbol, um Aktivitäten, die innerhalb einer ausgewählten Aktivität 48 Stunden ausgeführt finden Sie unter klicken.](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
4. Erhalten Sie Einblick in die das ausgewählte Element, indem Sie zum Untersuchen der Details für dieses Element übergehen können.
    
Eine Benachrichtigung auf mehreren fehlgeschlagenen Anmeldungen möglicherweise tatsächlich verdächtigen und einen potenziellen Brute-Force-Angriff kann anzugeben. Eine solche Warnung kann jedoch auch eine Anwendung Konfigurationsfehlers, verursacht die Benachrichtigung duldet falsch positiv sein. Wenn Sie eine Benachrichtigung mehrere Fehler Anmeldungen mit zusätzlichen verdächtigen Aktivitäten angezeigt wird, ist eine höhere Wahrscheinlichkeit, dass ein Konto gefährdet ist. Angenommen Sie, dass eine Warnung mehrere Fehler bei Anmeldung Aktivität aus einer TOR IP-Adresse und unmöglich Geschäftsreisen Aktivität, beide starken Indikatoren für Kompromiss folgen. Sie möglicherweise auch sehen, dass derselbe Benutzer eine Aktivität Masse Download durchgeführt, die häufig ein Indikator der Angreifer Exfiltration der Daten ausgeführt wird. Es handelt sich um Dinge wie, die Sie untersuchen können in Office 365-Cloud-App-Sicherheit zum Anzeigen und Selektieren von Warnungen und Ausführen einer Aktion bei Bedarf.
  
## <a name="next-steps"></a>Nächste Schritte

- [Integrieren von Ihrem Server SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)
    


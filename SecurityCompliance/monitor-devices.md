---
title: Überwachen von Geräten in Microsoft 365 Sicherheit
description: Beschreibt, wie Sie Ihre Geräte sicher, auf dem neuesten Stand halten und potenzielle Bedrohungen in Ihrer Organisation erkennen können.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Sicherheitscenter, Überwachung, Bericht, Geräte
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 43d074a9d42703b60b7b8eb17bdaf83a9360ce2d
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2019
ms.locfileid: "30791722"
---
# <a name="monitor-devices-in-microsoft-365-security"></a>Überwachen von Geräten in Microsoft 365 Sicherheit

[!include[Prerelease�information](prerelease.md)]

Halten Sie Ihre Geräte sicher, auf dem neuesten Stand und stellen Sie potenzielle Bedrohungen im Microsoft 365 Security Center vor.

## <a name="view-device-alerts"></a>Anzeigen von Geräte Warnungen

Informieren Sie sich über aktuelle Warnungen zu Verstößen und anderen Bedrohungen auf Ihren Geräten von Windows Defender ATP (verfügbar mit einer E5-Lizenz). Microsoft 365 Security Center verfügt über mehrere Karten, mit denen Sie diese Warnungen in Abhängigkeit von Ihrem bevorzugten Workflow effektiv überwachen können.

### <a name="monitor-high-impact-alerts"></a>Überwachen von Warnungen mit hoher Auswirkung

Jede Windows Defender-ATP-Warnung weist einen entsprechenden Schweregrad auf – hoch, Mittel, niedrig oder Informationswert –, der die potenziellen Auswirkungen auf Ihr Netzwerk angibt, wenn Sie unbeaufsichtigt bleiben.  

Verwenden Sie die **Geräte Warnungs schwere** Karte, um sich gezielt auf schwerwiegende Warnungen zu konzentrieren, die möglicherweise sofort beantwortet werden müssen. Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.

![Schwerekarte für Geräte Warnungen](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a>Informationen zu Quellen von Warnungen

Windows Defender ATP nutzt Daten aus einer Vielzahl von Sicherheitssensoren und Intelligence-Quellen, um Warnungen zu generieren. Sie können beispielsweise Erkennungsinformationen von Windows Defender Antivirus und Antischadsoftware von Drittanbietern sowie ihre eigenen benutzerdefinierten Bedrohungs Nachrichten verwenden, die über die Webdienst-API bereitgestellt werden.

Die Karte zur **Erkennung von Geräte Warnungen** zeigt die Verteilung der Warnungen nach Quelle. Diese Karte kann Ihnen dabei helfen, Aktivitäten im Zusammenhang mit bestimmten Quellen, insbesondere ihren benutzerdefinierten Quellen nachzuverfolgen. Sie können sich auch auf Warnungen konzentrieren, die von Sensoren stammen, die nicht so konfiguriert sind, dass Sie bösartige Aktivitäten oder Komponenten automatisch blockieren.

![Geräte Warnungs-Erkennungsquellen Karte](./media/security-docs/device-alert-detection-sources.png)

Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a>GrundLegendes zu den Arten von Bedrohungen, die Warnungen auslösen

Windows Defender ATP sortiert jede Warnung in einer Kategorie, die eine bestimmte Stufe in der Angriffs Kette oder eine Art von Bedrohungs Komponente darstellt. Die erkannte Bedrohungsaktivität kann beispielsweise in "Lateral Movement" kategorisiert werden, um anzugeben, dass die Aktivität versucht hat, andere Geräte im Netzwerk zu erreichen, und die Wahrscheinlichkeit aufgetreten ist, nachdem Angreifer eine erste Stütze erhalten haben. Wenn eine Bedrohungs Komponente erkannt wird, kann Sie entweder als "Schadsoftware" oder genauer als "Ransomware", "Diebstahl von Anmeldeinformationen" oder anderen Arten von böswilliger oder unerwünschter Software klassifiziert werden.

Die Karte für die **Geräte Bedrohungskategorien** zeigt die Verteilung von Warnungen in diese Kategorien an. Sie können diese Informationen verwenden, um die Bedrohungsaktivität zu identifizieren, wie beispielsweise Versuche zum Diebstahl von Anmeldeinformationen, die sich im Vergleich zu den versuchen bei Social Engineering zum Beispiel erheblich auswirken können. Sie können dies auch verwenden, um potenziell zerstörerische Bedrohungen wie Ransomware zu überwachen.

![Karte für Geräte Bedrohungskategorien](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a>Überwachen aktiver Warnungen

Die **Geräte Warnungsstatus** Karte gibt die Anzahl der Warnungen an, die nicht aufgelöst wurden und möglicherweise Aufmerksamkeit erfordern. Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.

![Geräte Warnungsstatus Karte](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a>Überwachen der Klassifizierung aufgelöster Warnungen

Wenn Sie eine Windows Defender-ATP-Warnung auflösen, können Ihre Sicherheitsmitarbeiter angeben, ob eine Warnung wie folgt überprüft wurde:

* Eine echte Warnung, die tatsächliche Verletzungs Aktivität oder Bedrohungs Komponenten identifiziert
* Falsche Warnung, die normale Aktivität falsch erkannt hat

Auf der **Device Alert** -Klassifikations Karte wird angezeigt, ob Ihre aufgelöste Warnungen als wahr oder falsch eingestuft wurden. Auf dieser Karte können Sie weitere Informationen im Windows Defender Security Center-Portal anzeigen.

Hinweis: in einigen Fällen sind Klassifizierungsinformationen für bestimmte Warnungen nicht verfügbar.

![Geräte Warnungs-Klassifikations Karte](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a>Überwachen der Ermittlung aufgelöster Warnungen

Zusätzlich zur Klassifizierung, ob eine Warnung während der Auflösung true oder false ist, können Ihre Sicherheitsmitarbeiter eine Bestimmung bereitstellen, die angibt, welche Art von normaler oder bösartiger Aktivität während der Überprüfung der Warnung gefunden wurde.

Auf der **Geräte Warnungs Findungs** Karte wird die für jede Warnung vorgesehene Bestimmung angezeigt, insbesondere:

* **Apt** – Advanced persistent Threat, die darauf hinweist, dass die erkannte Aktivität oder Bedrohungs Komponente Teil einer ausgeklügelten Verletzung ist, die dazu dient, im betroffenen Netzwerk Fuß zu fassen  
* **Schadsoftware** – Schadsoftware oder Code
* **Sicherheitspersonal** – normale Aktivitäten des Sicherheitspersonals
* **Sicherheitstests** – Aktivitäten oder Komponenten zur Simulation von tatsächlichen Bedrohungen und erwarteten Sicherheitssensoren und Warnungen generieren
* **Unerwünschte Software** – apps und andere Software, die nicht als bösartig gelten, aber sonst gegen Richtlinien oder akzeptable Nutzungsstandards verstoßen
* **Andere** – jede andere Bestimmung, die nicht unter die angegebenen Typen fällt

Von dieser Karte aus können Sie weitere Informationen im Windows Defender Security Center anzeigen.

![Geräte Warnungs Findungs Karte](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a>Verstehen der gefährdeten Geräte

**Geräteschutz** zeigt die Risikostufe für Geräte an. Die Risikostufe basiert auf Faktoren wie Typ und Schweregrad der Warnungen auf dem Gerät.

![Geräteschutz Karte](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a>Überwachen und melden des Status von InTune-verwalteten Geräten

Die folgenden Überwachungen und Berichte enthalten Daten von Geräten, die in InTune registriert sind. Daten von nicht registrierten Geräten sind nicht enthalten. Nur globale Administratoren können diese Karten anzeigen.

InTune-Daten für registrierte Geräte umfassen:

* Geräte Konformität
* Geräte mit aktiver Schadsoftware
* Arten von Schadsoftware auf Geräten
* Schadsoftware auf Geräten
* Geräte mit Schadsoftware-Entdeckungen
* Benutzer mit Schadsoftware

### <a name="monitor-device-compliance"></a>Überwachen der Geräte Konformität

**Device Compliance** zeigt, wie viele Geräte, die in InTune registriert sind, Konfigurationsrichtlinien einhalten.

![Geräte Konformitäts Karte](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a>Erkennen von Geräten mit Schadsoftware

**Geräte-Malware** -Entdeckungen bieten die Anzahl von InTune-Geräten, die aufgrund ausstehender Aktionen nicht vollständig aufgelöst wurden – ein Neustart, eine vollständige Überprüfung oder manuelle Benutzeraktionen – oder wenn die Behebungsaktion nicht erfolgreich abgeschlossen wurde.

![Geräte-Malware-Erkennungskarte](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a>GrundLegendes zu den festgestellten Arten

**Arten von Schadsoftware auf Geräten** zeigt verschiedene Arten von Schadsoftware, die auf Geräten erkannt wurden, die in InTune registriert wurden. Sie können jeden Typ im Microsoft 365 Security Center untersuchen.

![Arten von Schadsoftware auf der Geräte Karte](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a>Verstehen der auf Ihren Geräten festgestellten spezifischen Schadsoftware

**Schadsoftware auf Geräten** enthält eine Liste der auf Ihren Geräten erkannten spezifischen Schadsoftware.

![Schadsoftware auf Geräte Karte](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a>Verstehen der Geräte, die die meisten Schadsoftware aufweisen

**Geräte mit Schadsoftware** -Entdeckungen zeigen, welche Geräte die meisten Malware-Entdeckungen aufweisen. In Microsoft 365 Security Center können Sie untersuchen, ob Schadsoftware aktiv ist, wer das Gerät verwendet, und den Verwaltungsstatus in InTune.

![Geräte mit Schadsoftware-Erkennungskarte](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a>Verstehen der Benutzer, die über Geräte mit der meisten Schadsoftware verfügen

**Benutzer mit Schadsoftware** -Entdeckungen zeigen Benutzer mit Geräten, die die meisten Malware-Entdeckungen hatten. In Microsoft 365 Security Center können Sie sehen, wie viele Geräte jedem Benutzer zugewiesen sind, sowie weitere Informationen zu jedem Gerät und zu dem Typ der Schadsoftware.

![Benutzer mit Schadsoftware-Erkennungskarte](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a>Überwachen und Verwalten der Bereitstellung und Erkennung von ASR-Regeln

Mithilfe von Regeln zur anGriffs [Flächen Reduzierung (ASR)](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) können Sie verhindern, dass Aktionen und apps, die in der Regel von Exploit-suchen verwendet werden, Computer infizieren. Diese Regeln steuern, wann und wie ausführbare Dateien ausgeführt werden können. Sie können beispielsweise verhindern, dass JavaScript oder VBScript eine heruntergeladene ausführbare Datei startet, Win32-API-Aufrufe von Office-Makros blockiert oder Prozesse blockiert, die von USB-Laufwerken ausgeführt werden.

![Karte für anGriffsflächen Reduzierung](./media/security-docs/attack-surface-reduction-rules.png)

Die **Regelkarte Angriffsflächen Reduzierung** bietet eine Übersicht über die Bereitstellung von Regeln auf Ihren Geräten.

Auf der oberen Leiste der Karte wird die Gesamtzahl der Geräte angezeigt, die sich in den folgenden Bereitstellungsmodi befinden:

* **Blockierungs Modus** – Geräte mit mindestens einer Regel, die zum Blockieren der erkannten Aktivität konfiguriert ist
* **Überwachungsmodus** – Geräte, für die keine Regeln festgelegt wurden, um erkannte Aktivitäten zu blockieren, aber mindestens eine Regel zum Überwachen erkannter Aktivitäten festgelegt ist  
* **Off** – Geräte, für die alle ASR-Regeln deaktiviert sind

Im unteren Teil dieser Karte werden Einstellungen nach Regel über Ihre Geräte angezeigt. Jeder Balken gibt die Anzahl der Geräte an, die zum Blockieren oder Überwachen der Erkennung oder zur vollständigen Deaktivierung der Regel aktiviert sind.

### <a name="view-asr-detections"></a>Anzeigen von ASR-Erkennungen

Wenn Sie detaillierte Informationen zu ASR-Regel Erkennungen in Ihrem Netzwerk anzeigen möchten, wählen Sie auf der Karte für die anGriffs **Flächen Reduzierungs Regeln** **Ansichts Erkennungen** aus. Die **** Registerkarte "Entdeckungen" auf der Seite "detaillierter Bericht" wird geöffnet.

![Registerkarte "Entdeckungen"](./media/security-docs/detections-tab.png)

Das Diagramm am oberen Rand der Seite zeigt Entdeckungen im Zeitverlauf, die entweder blockiert oder überwacht wurden. In der Tabelle unten sind die neuesten Entdeckungen aufgeführt. Verwenden Sie die folgenden Informationen in der Tabelle, um die Art der Entdeckungen zu verstehen:

* **Erkannte Datei** – die Datei, in der Regel ein Skript oder ein Dokument, deren Inhalt die mutmaßliche Angriffs Aktivität ausgelöst hat
* **Regel** – Name zur Beschreibung der Angriffsaktivitäten, die von der Regel erfasst werden sollen. Informationen zu vorhandenen ASR-Regeln
* **Quell-App** – die Anwendung, die Inhalte geladen oder ausgeführt hat, die die mutmaßliche Angriffs Aktivität auslösen. Dabei kann es sich um eine legitime Anwendung wie Webbrowser, eine Office-Anwendung oder ein System Tool wie PowerShell handeln.
* **Publisher** – der Anbieter, der die Quell-App veröffentlicht hat

### <a name="review-device-asr-rule-settings"></a>Überprüfungen der Einstellungen für die Geräte ASR-Regel

Wechseln Sie auf der Seite Regeln für die anGriffs **Flächen Reduzierung** auf die Registerkarte **Konfiguration** , um die Regeleinstellungen für einzelne Geräte zu überarbeiten. Wählen Sie ein Gerät aus, um detaillierte Informationen dazu abzurufen, ob sich jede Regel im Blockmodus, im Überwachungsmodus oder vollständig deaktiviert befindet.

![Registerkarte "Konfiguration"](./media/security-docs/configuration-tab.png)

Microsoft InTune bietet Verwaltungsfunktionen für Ihre ASR-Regeln. Wenn Sie Ihre Einstellungen aktualisieren möchten, wählen Sie unter **Geräte konfigurieren** auf der Registerkarte **Erste Schritte** , um Geräteverwaltung auf InTune zu öffnen.

### <a name="exclude-files-from-asr-rules"></a>Ausschließen von Dateien aus ASR-Regeln

Durch das Ausschließen von Dateien von Entdeckungen können Sie unerwünschte falsch positive Entdeckungen verhindern und die Regeln zur Angriffsflächen Reduzierung im Blockmodus sicherer bereitstellen.

Während Datei Ausschlüsse für Angriffsflächen Reduzierungs Regeln auf Microsoft InTune verwaltet werden, stellt das Microsoft 365 Security Center ein Analyse Tool bereit, mit dem Sie die Dateien verstehen können, die Entdeckungen auslösen. Außerdem werden die Namen der Dateien, die Sie möglicherweise ausschließen möchten, erfasst.

Wechseln Sie zur Registerkarte **Ausschlüsse hinzufügen** auf der Seite Bericht zur Angriffs **Flächen Reduzierung** , um die Analyse von Entdeckungen und das Sammeln von Dateien zu starten.

![Registerkarte "Ausschlüsse hinzufügen"](./media/security-docs/add-exclusions-tab.png)

In der Tabelle sind alle Dateinamen aufgeführt, die von den Regeln zur Angriffs Oberflächenreduzierung erkannt wurden. Nachdem Sie eine oder mehrere Dateien ausgewählt haben, können Sie die Auswirkungen des Hinzufügens dieser Dateien zu ihren Ausnahmen überarbeiten:

* Die Verringerung der Gesamtanzahl von Entdeckungen
* Die Verringerung der Gesamtzahl der von den Entdeckungen betroffenen Geräte

Wenn Sie eine Liste der ausgewählten Dateien mit den vollständigen Pfaden für den Ausschluss abrufen möchten, wählen Sie **Ausschluss Pfade abrufen**aus.

Weitere Informationen zu Ausschlüssen und ausführlichen Anweisungen zum Hinzufügen finden Sie unter [Problembehandlung bei Angriffs Oberflächenreduzierung](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).

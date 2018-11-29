---
title: Was ist neu in Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 11/28/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d674763c-a4c9-4604-8623-68c1836d27f3
description: Finden Sie unter Neuigkeiten in Office 365-Cloud-App-Sicherheit
ms.openlocfilehash: a3ca4504d80cbb39b51ecbcf3a5165bc5139e07c
ms.sourcegitcommit: bf628da123a89d9422e8cff02165b1e2d35dfe12
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/28/2018
ms.locfileid: "26872013"
---
# <a name="what-is-new-in-office-365-cloud-app-security"></a>Was ist neu in Office 365-Cloud-App-Sicherheit

**Zusammenfassung** Lesen Sie diesen Artikel, um einen schnellen Überblick über Updates und neuen Features in Office 365-Cloud App-Sicherheit (früher als Office 365 Advanced Security Management bezeichnet) abzurufen, die von [Microsoft Cloud App-Sicherheit](https://aka.ms/whatiscas)bereitgestellt wird.
  
In diesem Artikel wird häufig aktualisiert, wie Features hinzugefügt oder verbessert werden. Office 365-Cloud-App-Sicherheits-Updates werden ungefähr zwei Wochen nach Microsoft Cloud App-Sicherheitsupdates freigegeben, und nicht alle Microsoft Cloud App-Sicherheitsupdates gelten für Office 365-Cloud-App-Sicherheit. Darüber hinaus können die neuen Features für mindestens eine Woche nach ihrer Veröffentlichungsdatum in der Cloud App Sicherheit in Office 365-Umgebung angezeigt wird dauern.

## <a name="office-365-cloud-app-security-release-136"></a>Office 365 Cloud App-Sicherheit Version 136

*25 November 2018 veröffentlicht*

**Folgen von [Microsoft Cloud App-Sicherheit Version 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **Cloud-Discovery-updates** Der benutzerdefinierten Log Parser wurde erweitert, um zusätzliche zu unterstützen und komplexere Webdatenverkehr Formate protokolliert. Als Teil des diese Verbesserungen Benutzer jetzt benutzerdefinierter Header für Schema CSV-Protokolldateien eingegeben werden kann, verwenden Sie spezielle Trennzeichen für Schlüssel / Wert-Dateien, verarbeiten Sie Syslog-Dateiformat und vieles mehr zu.

- **Neue Richtlinie für die Erkennung von Anomalien: verdächtigen Manipulation Posteingangsregeln** Diese Richtlinie profiles der Umgebung und Trigger Benachrichtigungen, wenn verdächtige Regeln, die löschen oder Verschieben von Nachrichten oder Ordner, für Posteingang des Benutzers festgelegt sind. Dies kann bedeuten, dass das Konto des Benutzers ist gefährdet, dass Nachrichten werden absichtlich ausgeblendet wird, und das Postfach zum Verteilen von Spam oder Schadsoftware in Ihrer Organisation verwendet wird.

- **Unterstützung für Gruppen in Richtlinien für die app-Berechtigung** Cloud App-Sicherheit bietet jetzt Sie die Möglichkeit zum Definieren von Richtlinien für die app-Berechtigung genauer gesagt, basierend auf den Gruppenmitgliedschaften der Benutzer, die die apps berechtigt. Beispielsweise kann ein Administrator entscheiden Sie sich für eine Richtlinie, die weniger häufiger apps entzieht Frage für hohe Berechtigungen nur, wenn der Benutzer, der die Berechtigungen autorisiert ein Mitglied der Administratorengruppe ist.


## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>133, 134 und 135-Freigaben für Office 365-Cloud-App-Sicherheit

*Veröffentlicht im Oktober-November 2018*

Der **folgende [Microsoft Cloud App-Sicherheit 133, 134, und 135 freizugeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)**:

- **Neue Anomalie Erkennungsrichtlinien** sind Rollout schrittweise:
    
    - Die neue Richtlinie **Daten Exfiltration unbestätigter Apps** wird automatisch für Sie warnen, wenn Sie einen Benutzer oder eine IP-Adresse eine app verwendet, die zum Ausführen einer Aktivitätsfeeds, die beim Versuch, Exfiltrate Informationen aus Ihrer Organisation ähnelt branchenübergreifenden ist nicht aktiviert.
    
    - Die neue Richtlinie **mehrere löschen VM Aktivitäten** profiles Ihrer Umgebung und Warnungen ausgelöst wird, wenn Benutzer mehrere virtuelle Computer in einer einzigen Sitzung, relativ zur Grundlinie in Ihrer Organisation löschen.

- **Cloud-Discovery-Unterstützung für i-Filter** Die Cloud App Sicherheit Cloud Discovery-Funktion wurde Unterstützung für den i-Filter Syslog Parser jetzt erweitert.


## <a name="office-365-cloud-app-security-release-131"></a>Office 365 Cloud App-Sicherheit Version 131

*16 September 2018 veröffentlicht*

**Nach [Microsoft Cloud App-Sicherheit 131 freizugeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **Automatisch Aufheben von Berechtigungen riskant OAuth-apps** Sie können jetzt steuern, welche apps OAuth Ihrer Benutzer haben Zugriff auf, indem das Aufheben von Berechtigungen für apps für Office OAuth app. Wenn Sie eine Berechtigungsrichtlinie App erstellen, können Sie jetzt die Richtlinie so entziehen Sie eine app-Berechtigung festlegen.

- **Zusätzliche integrierten Parser Cloud Discovery unterstützt** Cloud-Ermittlung unterstützt jetzt das Format für Forcepoint Web Sicherheit Cloud.

  
## <a name="office-365-cloud-app-security-release-130"></a>Office 365 Cloud App-Sicherheit Version 130

*5 September 2018 veröffentlicht*

**Folgen von [Microsoft Cloud App-Sicherheit Version 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **Neue Menüleiste** Admin-Benutzeroberfläche konsistenten über Microsoft-365-Produkte bereitstellen, und aktivieren Sie leichter zwischen Microsoft Security-Lösungen von PivotTables, hat die Portal Menüleiste Cloud App-Sicherheit in der linken Seite des Bildschirms verschoben. Diese einheitliche Navigation auftreten können Sie selbst beim Verschieben von einem Microsoft Security Portal ausrichten.<br/>![Menüleiste in Office Cloud App-Sicherheit](media/OCAS-MenuBar.png)<br/>

- **Bewertung der Auswirkung OAuth-app** Sie können jetzt das Teamfeedback Cloud App-Sicherheit, um uns zu informieren, wenn es ist eine OAuth-app in Ihrer Organisation, die böswilligen scheint ermittelt senden. Dieses neue Feature können Sie in unseren Sicherheits-Community werden und OAuth app Risiko Score und Analysen zu verbessern. Weitere Informationen finden Sie unter [app-Berechtigungen verwalten](manage-app-permissions-in-ocas.md).

- **Neue Cloud-Discovery-Parser** Die Cloud-Discovery-Parser unterstützen jetzt Iboss Secure Cloud Gateway und Sophos XG.


## <a name="office-365-cloud-app-security-release-128"></a>Office 365 Cloud App-Sicherheit Version 128

*5 August 2018 veröffentlicht* 
  
Der **folgende [Microsoft Cloud App-Sicherheit 128 freigeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **App-Berechtigungen über mehrere apps** Für apps, die app-Berechtigungen erteilt wurden, können Sie jetzt sperren oder mehrere apps in eine einzelne Aktion genehmigen. Beispielsweise können alle apps, die besitzen die Berechtigung von Benutzern in Ihrer Organisation, wählen Sie alle apps, die Sie sperren möchten, und klicken Sie dann auf Sperren apps für alle Zustimmung erteilt widerrufen überprüfen und können nicht mehr Benutzer Berechtigung für diese apps. 
    
- **Neue vorgeschlagenen Abfrage: GDPR kann jetzt** Es wird eine neue vorgeschlagene Abfrage, mit denen Sie erkannte apps zu identifizieren, die GDPR bereit sind. GDPR wurde vor kurzem oberste Priorität für Sicherheit-Admins änderte. Mit dieser Abfrage können Sie auf einfache Weise identifizieren apps, die GDPR bereit sind, und minimieren Bedrohung Abschätzen des Risikos der apps, die nicht sind. 
    
## <a name="office-365-cloud-app-security-release-126"></a>Office 365 Cloud App-Sicherheit Version 126

*7 Juli 2018 veröffentlicht* 
  
**Nach [Microsoft Cloud App-Sicherheit 126 freizugeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **Automatische Wiederherstellung für verdächtigen Aktivitäten** Sie können jetzt die automatische Wiederherstellung Aktionen für verdächtigen Sitzung ausgelöst, indem die Anomalie Erkennungsrichtlinien festlegen. Mithilfe dieser Verbesserung können Sie benachrichtigt werden, sofort eine Verletzung tritt und Governance Aktionen automatisch anwenden, wie Benutzer anhalten. Weitere Informationen finden Sie unter [Anomalie Erkennungsrichtlinien in Office 365-Cloud-App-Sicherheit](anomaly-detection-policies-in-ocas.md).
    
- **Automatische Erkennung von riskant OAuth-Apps** Zusätzlich zu den vorhandenen Untersuchen des OAuth-apps, die für Ihre Umgebung verbunden ermöglicht Office 365-Cloud-App-Sicherheit jetzt festzulegenden automatische Benachrichtigung, damit Sie wissen, wann eine OAuth-app für bestimmte Kriterien erfüllt. Beispielsweise können Sie automatisch gewarnt werden, wenn es apps sind, die eine hohe Berechtigungsstufe erfordern und mehr als 50 Benutzer autorisiert wurden. Weitere Informationen finden Sie unter [Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit](manage-app-permissions-in-ocas.md).
    
- **Managed Security Service Provider Management (MSSP) unterstützen.** Office 365-Cloud-App-Sicherheit jetzt ermöglicht eine bessere Verwaltung der auf MSSPs, und ermöglicht es Ihnen, externe Partner als Administratoren mit einer der Rollen, die derzeit in Office 365-Cloud-App-Sicherheit konfigurieren. Darüber hinaus können Administratoren mit Zugriffsrechten für mehrere Mandanten jetzt auf einfache Weise zwischen den Mandanten pivotieren. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Office 365 Cloud App-Sicherheit Version 124

*10 Juni 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- **Bereich Bereitstellungen** Unternehmen können detaillierte ermitteln, welche Benutzer zu überwachen und Schützen der Gruppenmitgliedschaft basierend. Dieses Feature kann Benutzer auswählen, deren Aktivitäten aus einem geschützten-Anwendung nicht angezeigt werden. Bereichsbasierte-Überwachung ist besonders für die Einhaltung von Vorschriften und Lizenzierung. Einige Vorschriften erfordern, dass Sie sehen davon ab, von der Überwachung von Benutzern aus bestimmten Ländern aufgrund von lokalen Vorschriften. Und Sie können weniger Benutzer innerhalb der Grenzen Ihrer Sicherheit in Office 365 Cloud App-Lizenzen bleiben überwachen. 
    
- **Neue e-Mail-server** Der e-Mail-Server für Office 365-Cloud-App-Sicherheit geändert hat und andere IP-Adressbereiche verwendet. Stellen Sie sicher, dass die Benachrichtigung zu erhalten, fügen Sie die neuen IP-Adressen zu Ihrer weißen Anti-Spam-Liste. Für Organisationen, die ihre Benachrichtigung anpassen, dadurch die Cloud App-Sicherheit mit MailChimp, einem Drittanbieter-e-Mail-Dienst für Sie. Die Liste der e-Mail-Server-IP-Adressen und Anweisungen für die Arbeit mit MailChimp finden Sie unter [netzwerkanforderungen (Microsoft Cloud App-Sicherheit)](https://docs.microsoft.com/cloud-app-security/network-requirements) und [E-Mail-Einstellungen (Microsoft Cloud App-Sicherheit)](https://docs.microsoft.com/cloud-app-security/mail-settings).
    
## <a name="office-365-cloud-app-security-release-121"></a>Office 365 Cloud App-Sicherheit Version 121

*6 Mai 2018 veröffentlicht* 
  
**Nach [Microsoft Cloud App-Sicherheit 121 freizugeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **Verbesserungen bei Anomalie Erkennung der Richtlinie**. Richtlinien für Office 365 Cloud App des Wertpapiers Anomalie Erkennung wurden verbessert, um zwei neue Typen von Erkennung, die schrittweise Einführung umfassen: 
    
  - **Ransomware Aktivität.** Ransomware Erkennungsfunktionen sind mit Normalbetriebswerte umfassendere Schutz vor Angriffen anspruchsvolle Ransomware zur Verfügung, erweitert. 
    
  - **Aktivität des Benutzers beendet.** Communicator Web Access Benutzer Aktivität ermöglicht, die Sie zum Überwachen der Konten der beendeten Benutzer möglicherweise schon im Unternehmen Applications aufgehoben, die aber, die möglicherweise auch auf bestimmte Unternehmensressourcen zugreifen. 
    
    Wählen Sie zum Anzeigen Ihrer [Anomalie Erkennungsrichtlinien](anomaly-detection-policies-in-ocas.md)in der Cloud App Sicherheit in Office 365-Portal **Steuerelement** \> **Richtlinien**.
    
## <a name="office-365-cloud-app-security-release-120"></a>Office 365 Cloud App-Sicherheit Version 120

*22 April 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **Interne Anwendungen als die Benutzeraktivitäten**. Für Office 365 und Azure Active Directory (AD Azure) werden wir nun schrittweise, die Möglichkeit zum Erkennen von interner Anwendungen als Benutzer Kontoaktivitäten, die von der Office 365 und Azure AD-Anwendung (intern und extern) durchgeführt Gang (engl.). Dadurch können Sie Richtlinien erstellen, um Sie zu warnen, wenn eine Anwendung unerwartete und nicht autorisierte Aktivitäten ausführt. 
    
- **Weitere Felder in der Liste der app-Berechtigungen zu exportieren**. Beim Exportieren einer Liste der app-Berechtigungen CSV, zusätzliche Felder wie Publisher, sind die Berechtigungen Ebene und Community-Nutzung zur Unterstützung bei der Einhaltung von Vorschriften und Untersuchung Prozess enthalten. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Office 365 Cloud App-Sicherheit Version 119

*1 April 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **Verbesserungen in die Cloud Discovery**. Die Cloud Discovery enthält Informationen zur Top-Benutzer und IP-Adressen können Ansicht Verwendungsdetails zu Office 365 und anderen apps vereinfacht. Weitere Informationen finden Sie finden Sie unter [Überprüfen der app Discovery Ergebnisse in Office 365-Cloud-App-Sicherheit](review-app-discovery-findings-in-ocas.md).
    
    ![Wurde aktualisiert, das Cloud-Discovery-dashboard](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Office 365 Cloud App-Sicherheit Version 118

*18 März 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Barracuda unterstützen**. Cloud-Ermittlung unterstützt jetzt Barracuda F Datenreihe Firewalls und das streaming von Barracuda F-Serie Firewall Web Log. 
    
## <a name="office-365-cloud-app-security-release-117"></a>Office 365 Cloud App-Sicherheit Version 117

*6 März 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **i-FILTER unterstützt wird**. Cloud-Ermittlung unterstützt jetzt i-FILTER. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Office 365 Cloud App-Sicherheit Version 116

*18 Februar 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **Erweiterungen der Anomalie Erkennung Richtlinien**. Normalbetriebswerte Richtlinien in Office 365-Cloud-App-Sicherheit mit neuen szenariobasierte erkannte einschließlich unmöglich Reisen, Aktivität von verdächtigen IP-Adresse erweitert wurden und mehrere fehlgeschlagene Anmeldeversuche. Die neuen Richtlinien werden automatisch aktiviert, Out-of-Box Erkennung in der Cloudumgebung bereitstellen. Darüber hinaus stellen die neuen Richtlinien weitere Daten aus dem Office 365-Cloud-App-Sicherheit Erkennung Motor die Untersuchung beschleunigen und die laufende Bedrohungen enthalten kann. Finden Sie weitere Informationen finden Sie im Microsoft Cloud App-Sicherheit-Artikel [sofortige Verhalten Analyse- und Normalbetriebswerte erhalten möchten](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy).
    
- **Log Parser Unterstützung für Formate Prüfpunkt**. Die Cloud Discovery Log Parser unterstützen jetzt zwei zusätzliche Prüfpunkt-Formate: XML- und KPC. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Office 365 Cloud App-Sicherheit Version 114

*21 Januar 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **Dienststatus**. Sie können nun den aktuellen Status der App-Sicherheit für Office 365 Cloud Service suchen, indem Sie ihm **helfen** \> **Systemstatus**. 
    
    ![Klicken Sie auf Hilfe \> Systemstatus zum Anzeigen des Status des Systems](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **Benutzerdefinierte Abfragen Aktivitätsprotokolls**. Ab Version 114, ist die Möglichkeit zum Erstellen und Speichern von benutzerdefinierten Abfragen im Protokoll Aktivität schrittweise Einführung. Benutzerdefinierte Abfragen aktivieren Sie die Filtervorlagen erstellen, die für die Untersuchung im Detail wiederverwendet werden können. Darüber hinaus vorgeschlagene Abfragen wurden hinzugefügt, um die Untersuchung Out-of-Box-Vorlagen zum Filtern der Aktivitäten bieten und apps ermittelt. Vorgeschlagene Abfragen enthalten benutzerdefinierte Filter zum Identifizieren Risiken wie Identitätswechsel Aktivitäten, Administrator Aktivitäten, riskant nicht kompatible Cloud-Speicher-apps, Enterprise-apps mit schwache Verschlüsselung und Sicherheitsrisiken. Verwenden Sie die vorgeschlagenen Abfragen als Ausgangspunkt, Bedarf zu bearbeiten Sie und speichern sie Sie als eine neue Abfrage. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Office 365 Cloud App-Sicherheit Version 113

*8 Januar 2018 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **Log Parser Unterstützung für generische Formate**. Die Cloud Discovery Log Parser unterstützen nun eine generische folgenden Formate: LEEF, CEF und W3C. 
    
## <a name="office-365-cloud-app-security-release-112"></a>Office 365 Cloud App-Sicherheit Version 112

*24 Dezember 2017 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 112](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-112)**: 
  
- **Relevante Erkenntnisse Papiereinzug**. Im Protokoll Aktivität können Sie nun die relevanten Erkenntnisse Papiereinzug, indem Sie auf einen Benutzer- oder IP-Adresse zugreifen. 
    
    ![Klicken Sie auf einen Benutzer- oder IP-Adresse der relevanten Erkenntnisse Papiereinzug im Protokoll Aktivität finden Sie unter.](media/8e32b3fa-8c0c-4c5e-b248-fe7d7e1b516d.png)
  
- Die **Möglichkeit, mehrere Aktivitäten mit einem Klick anzuzeigen**. In der entsprechenden Erkenntnisse Papiereinzug können Sie das Uhrsymbol, um alle Aktivitäten ausgeführt innerhalb von 48 Stunden einer ausgewählten Aktivität anzeigen klicken. 
    
    ![In der entsprechenden Insights Papiereinzug können Sie das Uhrsymbol, um Aktivitäten, die innerhalb einer ausgewählten Aktivität 48 Stunden ausgeführt finden Sie unter klicken.](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
- **Log Parser Verbesserungen für Juniper SRX**. Verbesserungen bei der Cloud Discovery Log Parser für Juniper SRX wurde. 
    
## <a name="office-365-cloud-app-security-release-111"></a>Office 365 Cloud App-Sicherheit Version 111

*10 Dezember 2017 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 111](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-111)**: 
  
- **Zeit Filter Verbesserungen**. Zeitfilter sind nun leichter zu verwenden. Zugriff auf eine Zeitfilter, in einer Ansicht, wie etwa Aktivitätsprotokolls, Richtlinien, Benachrichtigungen, mit der erweiterten Ansicht, wählen Sie in der Liste der Filter **Datum** . Wählen Sie dann eine Option wie vor, nach oder in zwischen den Zeitfilter anwenden. 
    
    ![Verwenden Sie den Datumsfilter, um Informationen vor, nach oder zwischen Datumsangaben anzuzeigen.](media/9dbb2a10-f68f-413b-8b4e-88911152cb92.png)
  
## <a name="office-365-cloud-app-security-release-110"></a>Office 365 Cloud App-Sicherheit Version 110

*26 November 2017 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 110](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-110)**: 
  
- **SIEM-Server-Integration jetzt erhältlich**. Verbinden Sie Ihre Server SIEM mit Office 365-Cloud-App-Sicherheit. Sie können jetzt Warnungen und Aktivitäten automatisch auf Ihrem Server SIEM Wahl senden, SIEM Agents konfigurieren. Finden Sie unter [Integrieren Ihrer SIEM Server mit Office 365-Cloud-App-Sicherheit](integrate-your-siem-server-with-office-365-cas.md).
    
- **Einfacher Zugriff auf Inhalte zu unterstützen**. Verwenden das neue Fragezeichen in der oberen rechten Ecke, können Sie jetzt den Hilfeinhalt von innerhalb der Seiten von der Cloud App Sicherheit in Office 365-Portal zugreifen. Jeder Link ist kontextbezogene, wobei Sie mit den Informationen, die, den Sie benötigen, basierend auf der Seite Sie sich befinden. 
    
- **Senden Sie uns Feedback**. Verwenden das Smiley in der oberen rechten Ecke, können Sie jetzt Feedback von jeder Seite des Office 365-Cloud-App-Sicherheit Portals senden. So können Sie zum Melden von Fehlern, fordern die neuen Features und Ihre Erfahrung direkt mit dem Office 365-Cloud-App-Sicherheit Team freigeben. 
    
## <a name="office-365-cloud-app-security-release-102"></a>Office 365 Cloud App-Sicherheit Version 102

*13 August 2017 veröffentlicht* 
  
**Nach [Microsoft Cloud App-Sicherheit 102 freizugeben](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-102)**: 
  
- **Neue Untersuchung Benutzeraktionen** aktivieren ein höheres Maß an-Drilldown zum Benutzer Untersuchungen. Auf einer Seite untersuchen können und bewegen Sie den Mauszeiger auf eine Aktivität, Benutzer oder Konto als Filter anwenden, und von dort können Sie die zugehörige Aktivitäten oder Ereignisse anzeigen. 
    
## <a name="office-365-cloud-app-security-release-100"></a>Office 365 Cloud App-Sicherheit Version 100

*17 Juli 2017 veröffentlicht* 
  
**Folgen von [Microsoft Cloud App-Sicherheit Version 100](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-100)**: 
  
- **Sicherheit Extensions** ist ein neues Dashboard, in dem Sie alle Ihre Sicherheit Erweiterungen zentral für Office 365 Cloud App-Sicherheit, einschließlich API Token und SIEM Agents verwalten können. Zum Anzeigen eines Dashboards Extensions Sicherheit, gehen Sie folgendermaßen vor: 
    
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie Warnungen \> erweiterte Benachrichtigungen verwalten \> wechseln Sie zur erweiterten Sicherheit-Verwaltung](media/9792b121-9cd4-4faa-a6e0-81cfab4bf2f2.png)
  
4. **Auswählen von** \> **Security Extensions**.
    
    ![Wählen Sie im Portal ASM Einstellungen \> Security-Erweiterungen](media/f03d47a1-91ff-41b9-9baf-b514cffe41a8.png)
  
- **Verbesserte analysieren**. Im Protokoll Cloud Discovery Analyse Mechanismus wurden Verbesserungen vorgenommen. Interne Fehler sind weitaus geringerer Wahrscheinlichkeit auftreten. 
    
- **Erwartete Protokollformate**. Das erwartete Format für Cloud-Discovery-Protokolle enthält nun Beispiele für sowohl Syslog und FTP-Format. 
    
## <a name="related-topics"></a>Verwandte Themen

[Hilfeinhalte für Office 365-Cloud-App-Sicherheit](office-365-cas-help.md)
  
[Nutzungsaktivitäten nach der Einführung von Office 365 Cloud App Security](utilization-activities-for-ocas.md)
  
[Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  


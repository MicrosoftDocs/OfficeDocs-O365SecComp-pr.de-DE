---
title: Was ist neu in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 01/25/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Sehen Sie, was während 2018 für Office 365 Cloud App Security veröffentlicht wurde.
ms.openlocfilehash: 986fb64eedf8184e7835d1fec41845fde13b294b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214345"
---
# <a name="office-365-cloud-app-security-updates-during-2018"></a>Office 365 Cloud App-Sicherheitsupdates während 2018

## <a name="office-365-cloud-app-security-release-138"></a>Office 365 Cloud App Security Release 138

*Veröffentlicht am 2018*

**Folgende [Microsoft Cloud App Security Release 138](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-138)**:

- **Automatischer Protokoll Upload über docker unter Windows** Cloud App Security unterstützt jetzt den automatischen Protokoll Upload für Windows 10 ([Fall Creators Update](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) und neuer) und Windows Server ([Version 1709](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1709) und neuer) mithilfe von Docker unter Windows. In [diesem Artikel](https://docs.microsoft.com/cloud-app-security/discovery-docker-windows) erfahren Sie mehr und Konfigurieren von Docker.  

- **Microsoft Flow-Integration** Cloud App Security ist jetzt in [Microsoft Flow](https://docs.microsoft.com/flow/getting-started) integriert, um benutzerdefinierte Warnungs Automatisierungs-und Orchestrierungs Manuskripte bereitzustellen. In [diesem Artikel](https://docs.microsoft.com/cloud-app-security/flow-integration) erfahren Sie mehr und Konfigurieren der Microsoft-Fluss Integration. 

## <a name="office-365-cloud-app-security-release-137"></a>Office 365 Cloud App Security Release 137

*Veröffentlicht am 8. Dezember 2018*

**Folgende [Microsoft Cloud App Security Release 137](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-137)**:

- **Unterstützung für Dynamics hinzuGefügt** Cloud App Security bietet jetzt Unterstützung für die Microsoft Dynamics-Aktivitäten, die im Office 365-Überwachungsprotokoll unterstützt werden. 

- **Heads up – neue Terminologie!** Der Name der APP-Berechtigungsfunktionen wurde aus Gründen der Übersichtlichkeit geändert – es wird jetzt OAuth-apps genannt. 

## <a name="office-365-cloud-app-security-release-136"></a>Office 365 Cloud App Security Release 136

*Veröffentlicht am 2018*

**Folgende [Microsoft Cloud App Security Release 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **Cloud Discovery-Updates** Der benutzerdefinierte Protokollparser wurde erweitert, um zusätzliche und komplexere Webtraffic-Protokollformate zu unterstützen. Als Teil dieser Verbesserungen können Benutzer benutzerdefinierte Header für Header-basierte CSV-Protokolldateien eingeben, spezielle Trennzeichen für Schlüssel-Wert-Dateien, das Prozess-syslog-Dateiformat und vieles mehr verwenden.

- **Neue Anomalie-Erkennungsrichtlinie: Manipulations Regeln für verdächtige Posteingänge** Diese Richtlinie profiliert Ihre Umgebung und löst Warnungen aus, wenn verdächtige Regeln zum Löschen oder Verschieben von Nachrichten oder Ordnern im Posteingang eines Benutzers festgelegt werden. Dies kann darauf hindeuten, dass das Benutzerkonto kompromittiert ist, dass Nachrichten absichtlich ausgeblendet werden und dass das Postfach zum Verteilen von Spam oder Schadsoftware in Ihrer Organisation verwendet wird.

- **Unterstützung für Gruppen in App-Berechtigungsrichtlinien** Cloud App Security bietet Ihnen jetzt die Möglichkeit, App-Berechtigungsrichtlinien detaillierter zu definieren, basierend auf den Gruppenmitgliedschaften der Benutzer, die die apps autorisiert haben. Beispielsweise kann ein Administrator beschließen, eine Richtlinie festzulegen, die ungewöhnliche apps wider ruft, wenn Sie hohe Berechtigungen verlangen, nur dann, wenn der Benutzer, der die Berechtigungen autorisiert hat, Mitglied der Gruppe Administratoren ist.

## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>Office 365 Cloud-App-Sicherheitsversionen 133, 134 und 135

*Veröffentlicht im Oktober-November, 2018*

**Folgende [Microsoft Cloud App Security Release 133, 134 und 135](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)**:

- **Neue Erkennungsrichtlinien** für Anomalien werden schrittweise eingeführt:
    
    - Die neue **Datenfilterung an nicht sanktionierte apps** -Richtlinie wird automatisch aktiviert, um Sie zu benachrichtigen, wenn ein Benutzer oder eine IP-Adresse eine APP verwendet, die nicht sanktioniert wird, um eine Aktivität auszuführen, die dem Versuch ähnelt, Informationen aus Ihrer Organisation exfiltrieren.
    
    - Die neue Richtlinie zum **Löschen von VM-Aktivitäten** hat ihre Umgebung und löst Warnungen aus, wenn Benutzer mehrere VMs in einer einzigen Sitzung löschen, relativ zur Basislinie in Ihrer Organisation.

- **Unterstützung der Cloud-Erkennung für i-Filter** Die Cloud-App-Sicherheits Cloud-Erkennungsfunktion bietet jetzt erweiterte Unterstützung für den i-Filter-syslog-Parser.

## <a name="office-365-cloud-app-security-release-131"></a>Office 365 Cloud App Security Release 131

*Veröffentlicht am 2018*

**Folgende [Microsoft Cloud App Security Release 131](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **Automatisches widerrufen von Berechtigungen für riskante OAuth-apps** Sie können jetzt steuern, auf welche OAuth-apps Ihre Benutzer Zugriff haben, indem Sie die APP-Berechtigung für OAuth-apps in Office widerrufen. Wenn Sie eine APP-Berechtigungsrichtlinie erstellen, können Sie nun festlegen, dass die Richtlinie die Berechtigung einer APP widerrufen soll.

- **Cloud-Erkennung zusätzlicher integrierter Parser unterstützt** Die Cloud-Erkennung unterstützt jetzt das Forcepoint Web Security-Cloud-Protokollformat.
  
## <a name="office-365-cloud-app-security-release-130"></a>Office 365 Cloud App Security Release 130

*Veröffentlicht am 2018*

**Folgende [Microsoft Cloud App Security Release 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **Neue Menüleiste** Um eine konsistentere Verwaltungserfahrung für Microsoft 365-Produkte zu gewährleisten und eine einfachere Pivotierung zwischen Microsoft-Sicherheitslösungen zu ermöglichen, wurde die Menüleiste Cloud App Security Portal auf der linken Seite des Bildschirms verschoben. Diese konsistente Navigations Umgebung hilft Ihnen beim Übergang von einem Microsoft-Sicherheitsportal zu einem anderen.<br/>![Menüleiste in Office Cloud App Security](media/OCAS-MenuBar.png)<br/>

- **IMPACT OAuth-App-Bewertung** Sie können jetzt das Feedback des Cloud App-Sicherheitsteams senden, um uns zu informieren, ob eine in Ihrer Organisation entdeckte OAuth-app vorhanden ist, die bösartig erscheint. Mit diesem neuen Feature können Sie Teil unserer Sicherheitscommunity sein und die OAuth-App-Risikobewertung und-Analyse erhöhen. Weitere Informationen finden Sie unter [Manage OAuth apps](manage-app-permissions-in-ocas.md).

- **Neue Parser** für die Cloud-Erkennung Die Cloud Discovery-Parser unterstützen jetzt iboss Secure Cloud Gateway und Sophos XG.

## <a name="office-365-cloud-app-security-release-128"></a>Office 365 Cloud App Security Release 128

*Veröffentlicht am 5. August 2018* 
  
**Folgende [Microsoft Cloud App Security Release 128](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **OAuth apps in mehreren apps** Für OAuth-Apps können Sie nun mehrere apps in einer einzigen Aktion verbieten oder genehmigen. Sie können beispielsweise alle apps überarbeiten, denen Berechtigungen von Benutzern in Ihrer Organisation erteilt wurden, alle apps auswählen, die Sie verbieten möchten, und dann auf apps verbieten klicken, um alle erteilten Zustimmungen zu widerrufen, und Benutzern nicht mehr die Berechtigung erteilen, diese apps zu gewähren. Weitere Informationen finden Sie unter [Manage OAuth Apps using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md). 
    
- **Neue vorgeschlagene Abfrage: dsgvo-Ready Cloud apps** Es gibt eine neue vorgeschlagene Abfrage, mit der Sie erkannte apps identifizieren können, die DSGVO bereit sind. Wie Sie wahrscheinlich bereits wissen, hat DSGVO in letzter Zeit eine Priorität für Sicherheitsadministratoren. Diese Abfrage hilft Ihnen dabei, apps, die DSGVO bereit sind, leicht zu erkennen und die Gefahr zu verringern, indem Sie das Risiko der apps bewerten, die es nicht sind. Um die neue Abfrage zu verwenden, wählen Sie **** > im Dashboard für die **Cloud-Suche** auf der Registerkarte **erkannte apps** **dsgvo-Ready Cloud apps**aus.<br/>![DSGVO-Ready Cloud apps-Abfrage](media/OCAS-FindGDPRQueries.png)<br/>
    
## <a name="office-365-cloud-app-security-release-126"></a>Office 365 Cloud App Security Release 126

*Veröffentlicht am 2018* 
  
**Folgende [Microsoft Cloud App Security Release 126](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **Automatische Korrektur für verdächtige Aktivitäten** Sie können jetzt automatische Korrekturaktionen für verdächtige Sitzungen festlegen, die durch die Anomalie-Erkennungsrichtlinien ausgelöst werden. Mit dieser Erweiterung können Sie sofort benachrichtigt werden, wenn ein Verstoß auftritt, und Steuerungsaktionen wie beispielsweise "Benutzer anhalten" automatisch anwenden. Weitere Informationen finden Sie unter [Anomalie Detection Policies in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).
    
- **Automatisierte Erkennung riskantEr OAuth-apps** Zusätzlich zur vorhandenen Untersuchung von OAuth-apps, die mit Ihrer Umgebung verbunden sind, können Sie mit Office 365 Cloud App Security jetzt automatisierte Benachrichtigungen festlegen, um zu erfahren, ob eine OAuth-App bestimmte Kriterien erfüllt. Sie können beispielsweise automatisch gewarnt werden, wenn apps vorhanden sind, die eine hohe Berechtigungsstufe erfordern und von mehr als 50 Benutzern autorisiert wurden. Weitere Informationen finden Sie unter [Manage OAuth Apps using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md).
    
- **Unterstützung für Managed Security Service Provider Management (MSSP)** Office 365 Cloud App Security bietet jetzt eine bessere Verwaltungserfahrung für MSSPs und ermöglicht es Ihnen, externe Partner als Administratoren mit den derzeit in Office 365 Cloud App Security verfügbaren Rollen zu konfigurieren. Darüber hinaus können Administratoren mit Zugriffsrechten auf mehr als einen Mandanten nun problemlos zwischen den Mandanten schwenken. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Office 365 Cloud App Security Release 124

*Veröffentlicht am 2018* 
  
**Folgende [Microsoft Cloud App Security Release 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- **Bereichsbezogene Bereitstellungen** Unternehmensorganisationen können anhand der Gruppenmitgliedschaft detailliert festlegen, welche Benutzer überwacht und geschützt werden sollen. Mit diesem Feature können Sie Benutzer auswählen, deren Aktivitäten für keine der geschützten Anwendungen angezeigt werden. Die bereichsbezogene Überwachung eignet sich besonders für die Kompatibilität und Lizenzierung. Einige Compliance-Bestimmungen erfordern, dass Sie Benutzer aus bestimmten Ländern aufgrund lokaler Bestimmungen nicht überwachen. Und Sie können weniger Benutzer überwachen, um innerhalb der Grenzen Ihrer Office 365 Cloud App-Sicherheits Lizenzen zu bleiben. 
    
- **Neuer e-Mail-Server** Der e-Mail-Server für Office 365 Cloud App Security hat sich geändert und verwendet unterschiedliche IP-Adressbereiche. Um sicherzustellen, dass Sie Benachrichtigungen abrufen können, fügen Sie die neuen IP-Adressen Ihrer Anti-Spam-Whitelist hinzu. Für Organisationen, die Ihre Benachrichtigungen anpassen, ermöglicht Cloud App Security dies für Sie, indem Sie mailSchimpanse, einen Drittanbieter-e-Mail-Dienst verwenden. Eine Liste der e-Mail-Server-IP-Adressen sowie Anweisungen zum Aktivieren der Arbeit mit mailSchimpanse finden Sie unter [Network Requirements (Microsoft Cloud App Security)](https://docs.microsoft.com/cloud-app-security/network-requirements) and [Mail Settings (Microsoft Cloud App Security)](https://docs.microsoft.com/cloud-app-security/mail-settings).
    
## <a name="office-365-cloud-app-security-release-121"></a>Office 365 Cloud App Security Release 121

*Veröffentlicht 6. Mai 2018* 
  
**Folgende [Microsoft Cloud App Security Release 121](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **Verbesserungen**bei der Erkennung von Anomalien. Office 365 Cloud App Security es Anomaly Detection Policies wurden verbessert, um zwei neue Arten der Bedrohungserkennung einzuschließen, die schrittweise ausgeführt werden: 
    
  - **Ransomware-Aktivität.** Ransomware-Erkennungsfunktionen werden mit der Anomalie-Erkennung erweitert, um eine umfassendere Abdeckung für anspruchsvollere Ransomware-Angriffe zu ermöglichen. 
    
  - **Benutzeraktivität wurde beendet.** Mit der Beendigung der Benutzeraktivität können Sie die Konten von Endbenutzern überwachen, die möglicherweise aus Unternehmensanwendungen debereit gestellt wurden, aber noch Zugriff auf bestimmte Unternehmensressourcen haben. 
    
    um ihre [erkennungsrichtlinien](anomaly-detection-policies-in-ocas.md)für anomalien anzuzeigen, wählen sie im Office 365 Cloud App Security-portal **steuerungs** \> **richtlinien**aus.
    
## <a name="office-365-cloud-app-security-release-120"></a>Office 365 Cloud App Security Release 120

*Veröffentlicht am 22. April 2018* 
  
**Folgende [Microsoft Cloud App Security Release 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **Interne Anwendungen als Benutzeraktivitäten**. Für Office 365 und Azure Active Directory (Azure AD) werden wir jetzt schrittweise die Möglichkeit, interne Anwendungen als Benutzerkonto Aktivitäten zu identifizieren, die von den Office 365-und Azure AD-Anwendungen ausgeführt werden (sowohl intern als auch extern). Auf diese Weise können Sie Richtlinien erstellen, um Sie zu benachrichtigen, wenn eine Anwendung unerwartete und nicht autorisierte Aktivitäten ausführt. 
    
- **Weitere Felder im OAuth-apps-Listenexport**. Beim Exportieren einer OAuth-apps-Liste in eine CSV-Datei werden zusätzliche Felder wie Publisher, Berechtigungsstufe und Community-Nutzung zur Unterstützung der Compliance-und Ermittlungsprozesse bereitgestellt. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Office 365 Cloud App Security Release 119

*Veröffentlicht am 1. April 2018* 
  
**Folgende [Microsoft Cloud App Security Release 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **Verbesserungen bei der Cloud-Erkennung**. Die Cloud-Ermittlung bietet weitere Informationen zu den wichtigsten Benutzern und IP-Adressen, sodass die Verwendungsdetails zu Office 365 und anderen apps einfacher angezeigt werden können. Weitere Informationen finden Sie unter [Review Discovery Funds in Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md).
    
    ![Das Cloud Discovery-Dashboard wurde aktualisiert](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Office 365 Cloud App Security Release 118

*Veröffentlicht am 2018* 
  
**Folgende [Microsoft Cloud App Security Release 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Unterstützung für Barracuda**. Cloud Discovery unterstützt jetzt Barracuda F Series Firewalls und Barracuda F-Series Firewall Web Log Streaming. 
    
## <a name="office-365-cloud-app-security-release-117"></a>Office 365 Cloud App Security Release 117

*Veröffentlicht am 6. März 2018* 
  
**Folgende [Microsoft Cloud App Security Release 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **i-Filter-Unterstützung**. Die Cloud-Erkennung unterstützt jetzt i-FILTER. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Office 365 Cloud App Security Release 116

*Veröffentlicht am 2018* 
  
**Folgende [Microsoft Cloud App Security Release 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **Verbesserungen**bei der Erkennung von Anomalien. Anomalie-Erkennungsrichtlinien in Office 365 Cloud-App-Sicherheit wurden mit neuen, auf dem Szenario basierenden Erkennungen einschließlich unmöglicher Reisen, Aktivitäten von einer verdächtigen IP-Adresse und mehreren fehlgeschlagenen Anmeldeversuchen verbessert. Die neuen Richtlinien werden automatisch aktiviert und bieten eine sofort Erkennung in ihrer Cloud-Umgebung. Darüber hinaus stellen die neuen Richtlinien weitere Daten aus dem Sicherheits Erkennungsmodul für die Office 365 Cloud App zur Verfügung, mit denen Sie den Ermittlungsprozess beschleunigen und laufende Bedrohungen eindämmen können. Weitere Informationen finden Sie im Microsoft Cloud App Security-Artikel, [sofortige Verhaltensanalyse und Anomalie-Erkennung](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy).
    
- **Log Parser Unterstützung für Prüf Punkt Formate**. Die Analyse Protokolle für das Cloud Discovery-Protokoll unterstützen jetzt zwei zusätzliche Prüf Punkt Formate: XML und KPC. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Office 365 Cloud App Security Release 114

*Veröffentlicht am 21. Januar 2018* 
  
**Folgende [Microsoft Cloud App Security Release 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **Dienststatus**. sie können jetzt den status des aktuellen Office 365 Cloud App-sicherheitsdiensts überprüfen, indem sie den status des **hilfe** \> **systems**aufrufen. 
    
    ![Klicken Sie \> auf Hilfesystem Status, um den Systemstatus anzuzeigen.](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **Benutzerdefinierte Abfragen für das Aktivitätsprotokoll**. Ab Version 114 wird die Möglichkeit, benutzerdefinierte Abfragen im Aktivitätsprotokoll zu erstellen und zu speichern, schrittweise ausgeführt. Mit benutzerdefinierten Abfragen können Sie Filtervorlagen erstellen, die für tief greifende Untersuchungen wieder verwendet werden. Darüber hinaus wurden vorgeschlagene Abfragen hinzugefügt, um Out-of-the-Box-Untersuchungs Vorlagen zur Filterung ihrer Aktivitäten und erkannten apps bereitzustellen. Zu den vorgeschlagenen Abfragen gehört die Verwendung von benutzerdefinierten Filtern zur Identifizierung von Risiken wie Identitätswechsel Aktivitäten, Administratoraktivitäten, riskanten, nicht kompatiblen Cloud-Speicher-apps, Unternehmensanwendungen mit schwacher Verschlüsselung und Sicherheitsrisiken. Verwenden Sie die vorgeschlagenen Abfragen als Ausgangspunkt, ändern Sie Sie bei Bedarf, und speichern Sie Sie als neue Abfrage. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Office 365 Cloud App Security Release 113

*Veröffentlicht am 8. Januar 2018* 
  
**Folgende [Microsoft Cloud App Security Release 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **Log Parser Unterstützung für generische Formate**. Die Analyse Protokolle für das Cloud Discovery-Protokoll unterstützen jetzt die folgenden generischen Formate: LEEF, CEF und W3C. 

## <a name="related-topics"></a>Verwandte Themen

[Was ist neu in Office 365 Cloud App Security](new-in-office-365-cas.md)

[Weitere Informationen finden Sie im 2017-Updates für Office 365 Cloud App Security](new-in-office-365-cas-2017.md)
    
[Nutzungsaktivitäten nach der Einführung von Office 365 Cloud App Security](utilization-activities-for-ocas.md)
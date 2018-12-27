---
title: Protokolle für Webdatenverkehr und Datenquellen für Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 funktioniert Cloud App-Sicherheit mit Web-Datenverkehr Protokolle aus einer Vielzahl von Anbietern. Lesen Sie diesen Artikel, um weitere Informationen zu Web-Datenverkehr Protokolle und unterstützte Datenquellen für Office 365-Cloud-App-Sicherheit.
ms.openlocfilehash: ab962e4a030d06c133ad9fc4aa62a60755793bc3
ms.sourcegitcommit: 25f72d20e76463c2f0a075dfc0116f00c934bd77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/27/2018
ms.locfileid: "27447053"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Protokolle für Webdatenverkehr und Datenquellen für Office 365 Cloud App Security
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
  
Sie können eine Vielzahl von Protokolldateien für Web-Datenverkehr und Datenquellen mit Office 365-Cloud-App-Sicherheit verwenden. Jedoch die Protokolldateien für Web-Datenverkehr müssen enthalten spezifische Informationen und eine bestimmte Weise, damit sie mit Office 365-Cloud-App-Sicherheit app Discovery-Berichten und das Cloud-Discovery-Dashboard funktionieren formatiert werden. Verwenden Sie diesen Artikel als Leitfaden für die Web-Datenverkehr Protokolle und Datenquellen, die mit Office 365-Cloud-App-Sicherheit verwendet werden.
  
> [!NOTE]
> Sie müssen ein globaler Administrator, Sicherheitsadministrator oder Sicherheit Reader Zugriff auf die Sicherheit sein &amp; Compliance Center und Cloud App Sicherheit in Office 365-Portal. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Melden Sie sich für von Web-Datenverkehr

Office 365 Cloud App-Sicherheit verwendet Daten in Ihre Web-Datenverkehr Protokolle können Sie sehen, welche apps in Ihrer Organisation für die Personensuche verwenden. Weitere Details, die in die Protokolldateien, die eine bessere Sichtbarkeit haben Sie in Benutzeraktivität enthalten sind.
  
Den folgenden Abschnitten sind die erforderlichen Attribute und zusätzliche Anforderungen für die Web-Datenverkehr Protokolle mit Office 365-Cloud-App-Sicherheit ordnungsgemäß funktioniert.

### <a name="attributes"></a>Attribute

Office 365 Cloud App-Sicherheit kann nicht angezeigt oder analysieren Attribute, die nicht in der Web-Datenverkehr Protokolle enthalten sind. Cisco ASA Firewall Standardformat für Protokolldateien Format verfügt beispielsweise nicht die Anzahl der hochgeladenen Bytes pro Transaktion, den Benutzernamen oder ein Ziel-URL (nur eine Ziel-IP). Aus diesem Grund diese Attribute werden nicht angezeigt, in der Cloud-Discovery-Daten und Einblick in die Cloud-apps ist beschränkt. Für Cisco ASA Firewalls muss die Informationen auf 6 festgelegt werden. 

Die Web-Datenverkehr Protokolle sollten die folgenden Attribute enthalten:

- Datum der Transaktion
- Quell-IP
- Benutzer (dringend empfohlen)
- Ziel-IP-Adresse
- Ziel-URL (empfohlen. URLs bereitstellen höhere Genauigkeit für die Erkennung von Cloud-app als IP-Adressen)
- Gesamtmenge der Daten (empfohlen; Dateninformationen sind sehr hilfreiche)
- Umfang der hoch- oder heruntergeladen Daten (empfohlen; bietet Einblicke in die Cloud app Verwendungsmuster)
- Aktion (zulässige oder blockierte)

### <a name="additional-requirements"></a>Zusätzliche Anforderungen 

Zusätzlich zu den weiter oben in diesem Artikel aufgeführten Attribute, sollte die Protokolle der Web-Datenverkehr über die folgenden Anforderungen erfüllen:

- Die Datenquelle für die Protokolldateien muss unterstützt werden.
- Das Format, das die Protokolldateien zu verwenden, muss das Standardformat übereinstimmen. Wenn die Datei hochgeladen wurde, wird app Discovery dies zu überprüfen.
- Die Ereignisse im Protokoll müssen nicht mehr als 90 Tage zurückliegt stattgefunden haben.
- Die Protokolldatei muss ausgehenden Datenverkehr Informationen enthalten, die für die Netzwerkaktivität analysiert werden können.
  
## <a name="data-attributes-for-different-vendors"></a>Data-Attribute für verschiedener Anbieter

In der folgenden Tabelle werden die Informationen im Web Datenverkehr Protokolle aus verschiedenen Anbietern zusammengefasst. **Müssen Sie den Anbieter für die aktuellsten Informationen zu überprüfen.**


|                 Datenquelle                  |    Ziel-App-URL    |    Ziel-IP-App     |       Benutzername       |      Ursprung IP       |    Gesamten Datenverkehrs     |    Hochgeladenen bytes    |
|----------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
|                  Barracuda                   | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |          Nein          |
|                  Blue Coat                   | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Prüfpunkt                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |          Nein          |          Nein          |
|              Cisco ASA (Syslog)              |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|           Cisco ASA mit FirePOWER           | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Cisco FWSM                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|              Cisco Ironport WSA              | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Cisco Meraki                 | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |          Nein          |          Nein          |
|           Clavister NGFW (Syslog)            | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                SonicWall (früher Dell)                | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|            Digitale Kunst i-FILTER             | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Antivirenfirewall                   |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Juniper SRX                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Juniper SSG                  |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  McAfee SWG                  | <strong>Ja</strong> |          Nein          |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                    MS TMG                    | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|              Palo auch Netzwerke              |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                    Sophos                    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|                Kalmare (Allgemein)                | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |
|                Kalmare (systemeigen)                | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |
| Websense - genauer Detailbericht (CSV) | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|    Websense - Aktivität Internet-Protokoll (CEF)    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                   Zscaler                    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Unterstützte Hersteller Firewalls und Proxys

Office 365-Cloud-App-Sicherheit unterstützt die folgenden Firewalls und -Proxys.
  
- Barracuda - Web App Firewall (W3C)  
- Blau Coat Proxy SG - Access-Protokoll (W3C)
- Kontrollkästchen Punkt
- Cisco ASA Firewall (Stellen Sie sicher, dass Sie die Informationen auf 6 festgelegt)
- Cisco ASA mit FirePOWER   
- Cisco IronPort WSA
- Cisco ScanSafe
- Melden Sie Cisco Merkai - URLs
- Clavister NGFW (Syslog)
- Digitale Kunst i-FILTER
- Fortinet Antivirenfirewall
- Iboss Secure Cloud-Gateway
- Juniper SRX
- Juniper SSG
- McAfee sichere Web-Gateway
- Microsoft Forefront Threat Management Gateway (W3C)
- Palo auch Datenreihe Firewall
- SonicWALL (früher Dell)   
- Sophos SG
- Sophos XG
- Sophos Cyberoam
- Kalmare (Allgemein)
- Kalmare (systemeigen)
- Websense - Web Security Solutions - genauer Detailbericht (CSV)
- Websense - Web Security Solutions - Internet-Aktivitätsprotokolls (CEF)
- Zscaler
    
> [!NOTE]
> Wenn eine Datenquelle, die Sie verwenden möchten, hier nicht enthalten ist, können Sie anfordern, dass er die app-Ermittlung hinzugefügt werden. Klicken Sie dazu beim Erstellen eines Berichts, wählen Sie **andere** für **die Datenquelle**. Geben Sie den Namen der Datenquelle, die Sie hochladen möchten. Wir überprüfen Sie das Protokoll und informiert Sie, wenn wir Unterstützung für dieses Protokoll Typs hinzufügen. Alternativ können Sie, Ihr Format passt, [definieren ein benutzerdefiniertes Parsers](https://docs.microsoft.com/cloud-app-security/custom-log-parser) . 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Behandeln von Problemen bei Protokolldateien hochgeladen werden

Nach dem Web-Datenverkehr Protokolldateien hochladen, überprüfen Sie des Protokolls Governance, um festzustellen, ob Fehler aufgetreten sind. Wenn Fehler aufgetreten sind, anhand der Informationen in der folgenden Tabelle, um diesen Fehler zu beheben.
  
|**Fehler**|**Beschreibung**|**Lösung**|
|:-----|:-----|:-----|
|Nicht unterstützte Dateityp  <br/> |Die Datei hochgeladen ist keine gültige Protokolldatei. Beispielsweise eine Bilddatei.  <br/> |Hochladen einer Text, Zip oder Gzip-Datei, die direkt aus Ihrer Firewall oder der Proxyserver exportiert wurde.  <br/> |
|Interner Fehler  <br/> |Es wurde ein Fehler bei der internen Ressourcen erkannt.  <br/> |Klicken Sie auf **Wiederholen** , um den Vorgang erneut auszuführen.  <br/> |
|Das Format stimmt nicht überein.  <br/> |Das Format, das Sie hochgeladen entspricht nicht das erwartete Format für diese Datenquelle.  <br/> |
Stellen Sie sicher, dass das Protokoll nicht beschädigt ist. Vergleichen und match das Format in das Beispiel-Format auf der Seite "Hochladen" angezeigt. |
|Transaktionen sind mehr als 90 Tage  <br/> |Alle Transaktion mehr als 90 Tage alt sind und daher werden ignoriert.  <br/> |Exportieren Sie ein neues Protokoll mit den jüngsten und Sie erneut hochladen.  <br/> |
|Keine Transaktionen Cloud-Katalog-apps  <br/> |Keine Transaktion für alle erkannten Cloud-apps finden Sie im Protokoll.  <br/> |Stellen Sie sicher, dass das Protokoll ausgehenden Datenverkehr Informationen enthält.  <br/> |
|Nicht unterstützte Protokolltyp  <br/> |Bei Auswahl **Datenquelle = andere (nicht unterstützte)**, das Protokoll wird nicht analysiert werden. Stattdessen wird es zur Überprüfung an das Team der [Microsoft Cloud App-Sicherheit](https://aka.ms/whatiscas) technische gesendet.<br/> |Das [Microsoft Cloud App-Sicherheit](https://aka.ms/whatiscas) technische Team erstellt einen dedizierten Parser für jede Datenquelle. Besonders beliebte-Datenquellen werden bereits unterstützt. Wenn eine nicht unterstützte Datenquelle hochgeladen wird, ist es überprüft und die Liste der potenziellen neuen Data Source Parser hinzugefügt.<br/> Wenn ein neuer Parser zu dem Feature hinzugefügt wird, ist eine Benachrichtigung in der Microsoft-Cloud-App-Sicherheit Anmerkungen zu dieser Version enthalten.  <br/> |
   
## <a name="next-steps"></a>Nächste Schritte

- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von Berichten für app-Ermittlung](create-app-discovery-reports-in-ocas.md)
    
- [Überprüfen der Ergebnisse der app-Ermittlung](review-app-discovery-findings-in-ocas.md)
    
- [Überprüfen Sie Ihre Aktivitäten Auslastung für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    


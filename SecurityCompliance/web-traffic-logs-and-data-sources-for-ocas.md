---
title: Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 funktioniert Cloud App-Sicherheit mit Web-Datenverkehr Protokolle aus einer Vielzahl von Anbietern. Lesen Sie diesen Artikel, um weitere Informationen zu Web-Datenverkehr Protokolle und unterstützte Datenquellen für Office 365-Cloud-App-Sicherheit.
ms.openlocfilehash: 09b0358e0d8b9a6ed59393d8771237f7eaf8bb98
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529546"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
  
Sie können eine Vielzahl von Protokolldateien für Web-Datenverkehr und Datenquellen mit Office 365-Cloud-App-Sicherheit verwenden. Jedoch die Protokolldateien für Web-Datenverkehr müssen enthalten spezifische Informationen und eine bestimmte Weise, damit sie mit Office 365-Cloud-App-Sicherheit app Discovery-Berichten und das Cloud-Discovery-Dashboard funktionieren formatiert werden. Verwenden Sie diesen Artikel als Leitfaden für die Web-Datenverkehr Protokolle und Datenquellen, die mit Office 365-Cloud-App-Sicherheit verwendet werden.
  
> [!NOTE]
> Sie müssen ein globaler Administrator, Sicherheitsadministrator oder Sicherheit Reader Zugriff auf die Sicherheit sein &amp; Compliance Center und Cloud App Sicherheit in Office 365-Portal. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Melden Sie sich für von Web-Datenverkehr

Office 365 Cloud App-Sicherheit verwendet Daten in Ihre Web-Datenverkehr Protokolle können Sie sehen, welche apps in Ihrer Organisation für die Personensuche verwenden. Weitere Details, die in die Protokolldateien, die eine bessere Sichtbarkeit haben Sie in Benutzeraktivität enthalten sind.
  
Die folgende Tabelle enthält die Anforderungen und Attribute, die für die Web-Datenverkehr Protokolle ordnungsgemäß funktioniert mit Office 365-Cloud-App-Sicherheit erforderlich sind:
  
|**Attribute**|**Zusätzliche Anforderungen **|
|:-----|:-----|
| Datum der Transaktion  <br/>  Quell-IP  <br/>  Benutzer (empfohlen)  <br/>  Ziel-IP-Adresse  <br/>  Ziel-URL (empfohlen: URLs bereitstellen höhere Genauigkeit für die Erkennung von Cloud-app als IP-Adressen)  <br/>  Gesamtmenge der Daten (empfohlen)  <br/>  Umfang der hoch- oder heruntergeladen Daten (empfohlen: bietet Einblicke in die Cloud app Verwendungsmuster)  <br/>  Aktion (zulässige oder blockierte)  <br/> | Die Datenquelle für die Protokolldateien muss unterstützt werden.  <br/>  Das Format, das die Protokolldateien zu verwenden, muss das Standardformat übereinstimmen. Wenn die Datei hochgeladen wurde, wird app Discovery dies zu überprüfen.  <br/>  Die Ereignisse im Protokoll müssen nicht mehr als 90 Tage zurückliegt stattgefunden haben.  <br/>  Die Protokolldatei muss ausgehenden Datenverkehr Informationen enthalten, die für die Netzwerkaktivität analysiert werden können.  <br/> |
   
Wenn Attribute in die Protokolle enthalten sind, die geladen werden, nicht Office 365-Cloud-App-Sicherheit anzeigen oder die Informationen für Sie analysieren. Cisco ASA Firewall Standardformat für Protokolldateien Format umfasst beispielsweise nicht die Anzahl der hochgeladenen Bytes pro Transaktion, den Benutzernamen oder ein Ziel-URL (nur eine Ziel-IP). Da diese Informationen in den Protokolldateien Cisco nicht, werden nicht Office 365-Cloud-App-Sicherheit es eingebundener Ihrer Organisation den Netzwerkverkehr zu analysieren.
  
> [!NOTE]
> Für bestimmte Arten von Firewalls müssen Sie eine Informationsebene für Web-Datenverkehr Protokolle enthalten die erforderlichen Attribute festlegen. Beispielsweise benötigen Cisco ASA Firewalls der Schweregrad Informationen auf 6 festgelegt. Stellen Sie sicher, dass die richtige Informationen in Ihr Web-Datenverkehr Protokolle Bereitstellen Ihrer Firewalls festgelegt sind. 
  
## <a name="data-attributes-for-different-vendors"></a>Data-Attribute für verschiedener Anbieter
<a name="BKMK_LogAndData"> </a>

In der folgenden Tabelle werden die Informationen im Web Datenverkehr Protokolle aus verschiedenen Anbietern zusammengefasst. **Müssen Sie den Anbieter für die aktuellsten Informationen zu überprüfen.**
  
|**Datenquelle**|**Ziel-app-URL**|**Ziel-app-IP**|**Username**|**Ursprung IP**|**Gesamten Datenverkehrs**|**Hochgeladenen bytes**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Barracuda  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |Nein  <br/> |
|Blue Coat  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Prüfpunkt  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |Nein  <br/> |
|Cisco ASA  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |
|Cisco FWSM  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |
|Cisco Ironport WSA  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Cisco Meraki  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |Nein  <br/> |
|Clavister NGFW (Syslog)  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Dell SonicWall  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Antivirenfirewall  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Juniper SRX  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Juniper SSG  <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|McAfee SWG  <br/> |**Ja** <br/> |Nein  <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Meraki (Cisco)  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |Nein  <br/> |Nein  <br/> |
|Microsoft Threat Management Gateway  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Palo auch Netzwerke  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Sophos  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |
|Kalmare (Allgemein)  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |
|Kalmare (systemeigen)  <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |**Ja** <br/> |Nein  <br/> |**Ja** <br/> |
|Websense - genauer Detailbericht (CSV)  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Websense - Aktivität Internet-Protokoll (CEF)  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
|Zscaler  <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |**Ja** <br/> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Unterstützte Hersteller Firewalls und Proxys
<a name="BKMK_Supported"> </a>

Office 365-Cloud-App-Sicherheit unterstützt die folgenden Firewalls und -Proxys.
  
- Barracuda - Web App Firewall (W3C)
    
- Blau Coat Proxy SG - Access-Protokoll (W3C)
    
- Kontrollkästchen Punkt
    
- Cisco ASA Firewall (Beachten Sie, dass Sie die Informationen auf 6 festgelegt müssen)
    
- Cisco IronPort WSA
    
- Cisco ScanSafe
    
- Melden Sie Cisco Merkai - URLs
    
- Dell Sonicwall
    
- Fortinet Antivirenfirewall
    
- Juniper SRX
    
- Juniper SSG
    
- McAfee sichere Web-Gateway
    
- Microsoft Forefront Threat Management Gateway (W3C)
    
- Palo auch Datenreihe Firewall
    
- Sophos SG
    
- Sophos Cyberoam
    
- Kalmare (Allgemein)
    
- Kalmare (systemeigen)
    
- Websense - Web Security Solutions - genauer Detailbericht (CSV)
    
- Websense - Web Security Solutions - Internet-Aktivitätsprotokolls (CEF)
    
- Zscaler
    
> [!NOTE]
> Wenn eine Datenquelle, die Sie verwenden möchten, hier nicht enthalten ist, können Sie anfordern, dass er die app-Ermittlung hinzugefügt werden. Klicken Sie dazu beim Erstellen eines Berichts, wählen Sie **andere** für **die Datenquelle**. Geben Sie den Namen der Datenquelle, die Sie hochladen möchten. Wir überprüfen Sie das Protokoll und informiert Sie, wenn wir Unterstützung für dieses Protokoll Typs hinzufügen. 
  
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
    


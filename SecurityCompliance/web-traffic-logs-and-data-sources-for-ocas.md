---
title: Protokolle für Webdatenverkehr und Datenquellen für Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 Cloud App Security arbeitet mit Webprotokollen von einer Vielzahl von Anbietern. In diesem Artikel erfahren Sie mehr über Webprotokolle und unterstützte Datenquellen für Office 365 Cloud App Security.
ms.openlocfilehash: 67246ded0e3d39c81b5b906f753b91298309d1d8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266850"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Protokolle für Webdatenverkehr und Datenquellen für Office 365 Cloud App Security
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
  
Sie können eine Vielzahl von Webprotokolldateien und Datenquellen mit Office 365 Cloud App Security verwenden. Ihre Webprotokolldateien müssen jedoch bestimmte Informationen aufweisen und so formatiert werden, dass Sie mit Office 365 Cloud App Security App Discovery Reports und dem Cloud Discovery Dashboard funktionieren. Verwenden Sie diesen Artikel als Referenz für die Webprotokolle und Datenquellen, die Sie mit Office 365 Cloud App Security verwenden.
  
> [!NOTE]
> Sie müssen ein globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser sein, um auf das Security &amp; Compliance Center und das Office 365 Cloud App Security-Portal zugreifen zu können. Weitere Informationen finden Sie unter [Permissions &amp; in the Office 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="web-traffic-log-requirements"></a>Webtraffic-Protokollanforderungen

Office 365 Cloud App Security verwendet Daten in ihren Webprotokollen, um zu verstehen, welche apps Personen in Ihrer Organisation verwenden. Je mehr Details in den Protokolldateien enthalten sind, desto besser ist die Sichtbarkeit in der Benutzeraktivität.
  
In den folgenden Abschnitten werden die erforderlichen Attribute und zusätzlichen Anforderungen aufgeführt, damit Ihre Webprotokolle ordnungsgemäß mit Office 365 Cloud App Security funktionieren.

### <a name="attributes"></a>Attribute

Office 365 Cloud App Security kann Attribute nicht anzeigen oder analysieren, die nicht in ihren Webprotokollen enthalten sind. Das Standardprotokoll Format der Cisco ASA-Firewall hat beispielsweise nicht die Anzahl der hochgeladenen Bytes pro Transaktion, den Benutzernamen oder eine Ziel-URL (nur eine Ziel-IP). Daher werden diese Attribute nicht in Cloud-Ermittlungsdaten angezeigt, und die Sichtbarkeit der Cloud-Apps ist begrenzt. Für Cisco ASA-Firewalls muss die Informationsebene auf 6 festgelegt werden. 

Ihre Webprotokolle sollten folgende Attribute aufweisen:

- Datum der Transaktion
- Quell-IP
- Quellbenutzer (dringend empfohlen)
- Ziel-IP-Adresse
- Ziel-URL (empfohlen; URLs bieten eine höhere Genauigkeit für die Erkennung von Cloud-Apps als IP-Adressen)
- Gesamtmenge an Daten (empfohlen; Daten Informationen sind sehr wertvoll)
- Menge der hochgeladenen oder gedownloadeten Daten (empfohlen; bietet Einblicke in Cloud-App-Nutzungsmuster)
- Aktion ausgeführt (zulässig oder blockiert)

### <a name="additional-requirements"></a>Zusätzliche Anforderungen 

Zusätzlich zu den weiter oben in diesem Artikel aufgeführten Attributen sollten die Webprotokolle die folgenden Anforderungen erfüllen:

- Die Datenquelle für die Protokolldateien muss unterstützt werden.
- Das von den Protokolldateien verwendete Format muss mit dem Standardformat übereinstimmen. Wenn die Datei hochgeladen wird, überprüft die APP-Erkennung dies.
- Die Ereignisse im Protokoll müssen nicht mehr als 90 Tage zurückliegen.
- Die Protokolldatei muss Informationen zum ausgehenden Datenverkehr aufweisen, die für die Netzwerkaktivität analysiert werden können.
  
## <a name="data-attributes-for-different-vendors"></a>Daten Attribute für verschiedene Anbieter

In der folgenden Tabelle werden die Informationen in Webprotokollen von verschiedenen Anbietern zusammengefasst. **Erkundigen Sie sich bei Ihrem Anbieter nach den neuesten Informationen.**


|                 Datenquelle                  |    Ziel-App-URL    |    Ziel-App-IP     |       Username       |      Ursprungs-IP       |    Gesamtdaten Verkehr     |    HochgeLadene bytes    |
|----------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
|                  Barracuda                   | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |          Nein          |
|                  Blaues Fell                   | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Prüf Punkt                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |          Nein          |          Nein          |
|              Cisco ASA (syslog)              |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|           Cisco ASA mit Feuerkraft           | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Cisco FWSM                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|              Cisco IronPort WSA              | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Cisco Meraki                 | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |          Nein          |          Nein          |
|           Clavister-NGFW (syslog)            | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                SonicWall (ehemals Dell)                | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|            Digitaler Kunst-i-FILTER             | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  Fortigate                   |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Juniper SRX                  |          Nein          | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                 Juniper SSG                  |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                  McAfee SWG                  | <strong>Ja</strong> |          Nein          |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                    MS TMG                    | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|              Palo Alto Networks              |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                    Sophos                    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          |
|                Squid (allgemein)                | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |
|                Squid (nativ)                | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> | <strong>Ja</strong> |          Nein          | <strong>Ja</strong> |
| Websense-investigativer Detailbericht (CSV) | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|    Websense-Internet Activity Log (CEF)    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
|                   Zscaler                    | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> | <strong>Ja</strong> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>Unterstützte Anbieter Firewalls und Proxys

Office 365 Cloud App Security unterstützt die folgenden Firewalls und Proxys.
  
- Barracuda-Web App Firewall (W3C)  
- Blue Coat Proxy SG-Access Log (W3C)
- Kontrollpunkt
- Cisco ASA Firewall (stellen Sie sicher, dass Sie die Informationsebene auf 6 festlegen)
- Cisco ASA mit Feuerkraft   
- Cisco IronPort WSA
- Cisco ScanSafe
- Cisco-Merkai-Protokoll für URLs
- Clavister-NGFW (syslog)
- Digitaler Kunst-i-FILTER
- Fortinet Fortigate
- iboss Secure Cloud Gateway
- Juniper SRX
- Juniper SSG
- McAfee Secure Web Gateway
- Microsoft Forefront Threat Management Gateway (W3C)
- Firewall der Palo Alto-Serie
- SonicWALL (ehemals Dell)   
- Sophos SG
- Sophos XG
- Sophos Cyberoam
- Squid (allgemein)
- Squid (nativ)
- Websense-Web Security Solutions-investigativer Detailbericht (CSV)
- Websense-Web Security Solutions-Internet Activity Log (CEF)
- Zscaler
    
> [!NOTE]
> Wenn eine Datenquelle, die Sie verwenden möchten, hier nicht enthalten ist, können Sie die APP-Erkennung hinzufügen. Wählen Sie dazu beim Erstellen eines Berichts für **Datenquelle**die Option **Sonstiges** aus. Geben Sie dann den Namen der Datenquelle ein, die Sie hochladen möchten. Wir überarbeiten das Protokoll und informieren Sie, ob die Unterstützung für diesen Protokolltyp hinzugefügt wird. Alternativ können Sie [einen benutzerdefinierten Parser definieren](https://docs.microsoft.com/cloud-app-security/custom-log-parser) , der mit Ihrem Format übereinstimmt. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>Behandeln von Fehlern beim Hochladen von Protokolldateien

Überprüfen Sie nach dem Hochladen der Webprotokolldateien im Steuerungsprotokoll, ob Fehler aufgetreten sind. Wenn Fehler auftreten, verwenden Sie die Informationen in der folgenden Tabelle, um diese Fehler zu beheben.
  
|**Error**|**Beschreibung**|**Lösung**|
|:-----|:-----|:-----|
|Nicht unterstützter Dateityp  <br/> |Die hochgeladene Datei ist keine gültige Protokolldatei. Beispiel: eine Bilddatei.  <br/> |Laden Sie eine Text-, ZIP-oder gzip-Datei hoch, die direkt aus Ihrer Firewall oder Ihrem Proxy exportiert wurde.  <br/> |
|Interner Fehler  <br/> |Ein interner Ressourcenfehler wurde erkannt.  <br/> |Klicken Sie auf wieder **holen** , um die Aufgabe erneut auszuführen.  <br/> |
|Das Protokollformat stimmt nicht überein  <br/> |Das hochgeladene Protokollformat stimmt nicht mit dem erwarteten Protokollformat für diese Datenquelle überein.  <br/> |
Stellen Sie sicher, dass das Protokoll nicht beschädigt ist. Vergleichen Sie das Protokolldateiformat, und passen Sie es dem auf der Seite hochladen angezeigten Beispielformat an. |
|Transaktionen sind mehr als 90 Tage alt  <br/> |Alle Transaktionen sind mehr als 90 Tage alt und werden daher ignoriert.  <br/> |Exportieren Sie ein neues Protokoll mit den letzten Ereignissen, und laden Sie es erneut hoch.  <br/> |
|Keine Transaktionen zu Katalog Cloud-apps  <br/> |Im Protokoll werden keine Transaktionen zu erkannten Cloud-apps gefunden.  <br/> |Stellen Sie sicher, dass das Protokoll ausgehende Datenverkehrsinformationen enthält.  <br/> |
|Nicht unterstützter Protokolltyp  <br/> |Wenn Sie **Datenquelle = Sonstiges (nicht unterstützt)** auswählen, wird das Protokoll nicht analysiert. Stattdessen wird es zur Überarbeitung an das [Microsoft Cloud App Security](https://aka.ms/whatiscas) Technical-Team gesendet.  <br/> |Das [Microsoft Cloud App Security](https://aka.ms/whatiscas) Technical Team erstellt für jede Datenquelle einen dedizierten Parser. Die beliebtesten Datenquellen werden bereits unterstützt. Wenn eine nicht unterstützte Datenquelle hochgeladen wird, wird Sie überprüft und zur Liste der potenziellen neuen Datenquellen Parser hinzugefügt.  <br/> Wenn dem Feature ein neuer Parser hinzugefügt wird, ist eine Benachrichtigung in den Microsoft Cloud App Security Release Notes enthalten.  <br/> |
   
## <a name="next-steps"></a>Nächste Schritte

- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von App-Ermittlungs Berichten](create-app-discovery-reports-in-ocas.md)
    
- [Überarbeiten der Ergebnisse der APP-Suche](review-app-discovery-findings-in-ocas.md)
    
- [Überwachen Ihrer Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    


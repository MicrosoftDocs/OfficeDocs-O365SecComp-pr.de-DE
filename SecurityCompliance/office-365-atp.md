---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/09/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 erweiterte Threat Protection umfasst Spoofing Intelligence, sicheren Links, sichere Anlagen und erweiterten Anti-Phishing-Funktionen. Erweiterten Schutz ist auch in Dateien in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, erweitert wird.
ms.openlocfilehash: fed816ec8cd0e3e7a6b5118fde35d81647b94f02
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454352"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

Hilft bei der Office 365 erweiterte Threat Protection (ATP) zum Schutz Ihrer Organisation vor Angriffen durch:
  
- Überprüfen von e-Mail-Anlagen für Malware mit [ATP sichere Anlagen](atp-safe-attachments.md)
    
- Scan Webadressen (URLs) in e-Mail-Nachrichten und Office-Dokumenten mit [Sicheren ATP-Links](atp-safe-links.md)
    
- Erkannt und blockiert schädliche Dateien in online Bibliotheken mit [ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md)
    
- Überprüfen von e-Mail-Nachrichten für nicht autorisierten spoofing mit [Spoofing intelligence](learn-about-spoof-intelligence.md)
    
- Erkennen, wenn jemand versucht, Identitätswechsel für Ihre Benutzer und Ihrer Organisation benutzerdefinierte Domänen mit [ATP Anti-Phishing-Funktionen in Office 365](atp-anti-phishing.md)
    
**Schutz über Office 365 ATP ergibt sich Richtlinien, die für sichere Links, sichere Anlagen und Phishing - Security-Team Ihrer Organisation definiert**. Es ist wichtig, regelmäßig zu überprüfen und Überarbeiten Ihrer Richtlinien, um diese auf dem aktuellen Stand zu halten und Vorteile der neuen Features nutzen, die den Dienst hinzugefügt werden. [Berichte sind verfügbar](view-reports-for-atp.md) , um anzuzeigen, wie ATP für Ihre Organisation arbeitet. Diese Berichte können Sie Bereiche anzeigen, in dem Sie möglicherweise überprüfen und aktualisieren Sie Ihre Richtlinien. Und wenn Sie Dateien gespeichert, die gekennzeichnet sind haben, wie Schadsoftware, die Sie Dateien oder sollte nicht Microsoft überprüfen möchten, können Sie [eine Datei an Microsoft zur Analyse senden](#submit-a-suspicious-file-to-microsoft-for-analysis).
      
## <a name="get-office-365-atp"></a>Office 365 ATP abrufen

> [!IMPORTANT]
> Office 365 ATP ist in Abonnements, wie beispielsweise Microsoft 365 Enterprise, Office 365 Enterprise E5, Office 365 Education A5 und [Microsoft 365 Business](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc)enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Office 365 erweiterte Threat Protection Service Description](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx). 

1. Als globaler oder eine Sicherheitsgruppe an, wechseln Sie zur [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365. 
    
2. Wählen Sie **Admin** \> **Abrechnung** sehen, was Ihr aktuelle Abonnement enthält. <br/>![Als ein globaler Administrator, melden Sie sich am portal.office.com, und wechseln Sie zu Admin \> Abrechnung](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Wenn Sie **Office 365 Enterprise E5**, **Office 365 Education A5**oder **Microsoft 365 Business**angezeigt wird, hat Ihre Organisation ATP. <br/>Wenn Sie ein anderes Abonnement, wie **Office 365 Enterprise E3** oder **Office 365 Enterprise E1**, finden Sie unter berücksichtigen Sie ATP hinzufügen. Wählen Sie hierzu **+ Abonnement hinzufügen**.
    
Sobald Sie ATP haben, besteht der nächste Schritt für Ihr Sicherheitsteam zum Definieren von Richtlinien. 
  
## <a name="define-policies-for-atp"></a>Definieren von Richtlinien für ATP

- Vor Angriffen zu schützen, die Senden von e-Mail-Nachrichten, die **[ATP Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-atp-anti-phishing-policies.md)** einschließlich Identitätswechsel-basierten Angriffen aus vertrauenswürdigen Personen oder Domänen werden angezeigt 

- [Benutzerdefinierte Liste der blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md) und [benutzerdefinierte Liste für "Nicht rewrite" URLs](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) Ihrer Organisation einschließlich **[Einstellungsrichtlinien ATP sichere Links in Office 365](set-up-atp-safe-links-policies.md)**
    
- **[Richten Sie sichere Anlagen ATP Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)** , die [Dynamische Übermittlung und Anzeigen der Vorschau](dynamic-delivery-and-previewing.md) hinzufügen können
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Finden Sie unter wie ATP funktioniert, indem Sie Berichte anzeigen

Nach Ihrer Richtlinien ATP vorhanden sind, stehen Berichte anzeigen, wie der Dienst ordnungsgemäß funktioniert.

[![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Stellen Sie sicher, dass Sie ein Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheit Reader sind. (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)
    
2. [Anzeigen von Berichten für erweiterte Threat Protection](view-reports-for-atp.md).
    
3. Falls erforderlich, ändern Sie Ihre Sicherheitsrichtlinien. Finden Sie in den folgenden Ressourcen:

  - [ATP Anti-Phishing-Richtlinien in Office 365](set-up-atp-anti-phishing-policies.md)
    
  - [Sichere Links ATP Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
    
  - [Sichere Anlagen ATP Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Dateien Sie verdächtige an Microsoft zur Analyse

- Wenn Sie eine Datei, die vermutlich Schadsoftware werden konnte abrufen, können Sie diese Datei an Microsoft zur Analyse senden. Besuchen Sie das [Windows Defender Security Intelligence Übermittlung Portal](https://go.microsoft.com/fwlink/?linkid=857185).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlagen), die Sie für die Analyse an Microsoft senden möchten erhalten, verwenden Sie das [Bericht-add-in](enable-the-report-message-add-in.md). 
  
## <a name="related-topics"></a>Verwandte Themen

[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)
  
[Verfahren zum Erstellen von Management in die Office 365-Sicherheit &amp; Compliance Center](threat-management.md)
  


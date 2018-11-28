---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 erweiterte Threat Protection umfasst Spoofing Intelligence, sicheren Links, sichere Anlagen und erweiterten Anti-Phishing-Funktionen. Erweiterten Schutz ist auch in Dateien in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, erweitert wird.
ms.openlocfilehash: c147fde4e470b998a66a2cb456be71f635db25d7
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706309"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

## <a name="overview"></a>Übersicht

Hilft bei der Office 365 erweiterte Threat Protection (ATP) zum Schutz Ihrer Organisation vor Angriffen durch:
  
- Überprüfen von e-Mail-Anlagen für Malware mit [ATP sichere Anlagen](atp-safe-attachments.md)
    
- Scan Webadressen (URLs) in e-Mail-Nachrichten und Office-Dokumenten mit [Sicheren ATP-Links](atp-safe-links.md)
    
- Erkannt und blockiert schädliche Dateien in online Bibliotheken mit [ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md)
    
- Überprüfen von e-Mail-Nachrichten für nicht autorisierten spoofing mit [Spoofing intelligence](learn-about-spoof-intelligence.md)
    
- Erkennen, wenn jemand versucht, Identitätswechsel für Ihre Benutzer und Ihrer Organisation benutzerdefinierte Domänen mit [ATP Anti-Phishing-Funktionen in Office 365](atp-anti-phishing.md)
    
**Schutz über Office 365 ATP ergibt sich Richtlinien, die für sichere Links, sichere Anlagen und Phishing - Security-Team Ihrer Organisation definiert**. Es ist wichtig, regelmäßig zu überprüfen und Überarbeiten Ihrer Richtlinien, um diese auf dem aktuellen Stand zu halten und Vorteile der neuen Features nutzen, die den Dienst hinzugefügt werden. [Berichte sind verfügbar](view-reports-for-atp.md) , um anzuzeigen, wie ATP für Ihre Organisation arbeitet. Diese Berichte können Sie Bereiche anzeigen, in dem Sie möglicherweise überprüfen und aktualisieren Sie Ihre Richtlinien. Und wenn Sie Dateien gespeichert, die gekennzeichnet sind haben, wie Schadsoftware, die Sie Dateien oder sollte nicht Microsoft überprüfen möchten, können Sie [eine Datei an Microsoft zur Analyse senden](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Neue Features werden ständig ATP hinzugefügt wird

Wir bauen zum Hinzufügen neuer Funktionen zu Office 365 sowie ATP enthält. Es folgt eine Liste der verschiedene neue Features, von denen einige rufen Sie für eine Richtlinie ATP geprüft und aktualisiert werden. Weitere Informationen zu neuen Features der ATP (oder Microsoft 365 im Allgemeinen) finden Sie auf der [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).
  
- Verspätete Oktober 2017 ab, ist sicherer Links ATP erweitertem Schutz um URLs in e-Mail-als auch URLs in Office 365 ProPlus-Dokumenten, beispielsweise Word, Excel, PowerPoint und Visio auf Windows als auch Office apps auf iOS und Android-Geräte zuweisen. (Stellen Sie sicher, dass Sie [Modernen für Office-Authentifizierung](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)verwenden.)
    
- März 2018 ab, ist sicherer Links ATP Schutz erweitert, um auf zwischen Personen innerhalb einer Organisation gesendeten e-Mails anwenden. (Stellen Sie sicher [Überprüfen](set-up-atp-safe-links-policies.md)und Bearbeiten Ihrer Richtlinien ATP sichere Links.)

- Ende Mai 2018, [Quarantäne](quarantine-email-messages.md) -Funktionen in die Sicherheit ab &amp; Compliance Center sind auf [ATP für SharePoint Online, OneDrive für Unternehmen, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md)erweitert wird.
 
- In der zweiten Hälfte des 2018 beginnen, ist sicherer Links ATP Schutz erweitert, um URLs in Office Online (Online Word, Excel Online, Online PowerPoint und OneNote Online) und Office 365 ProPlus auf einem Mac gilt (Stellen Sie sicher [Überprüfen](set-up-atp-safe-links-policies.md)und Bearbeiten Ihrer Richtlinien ATP sichere Links.)

- Anfang im September 2018, [Office 365 ATP Warnung Seiten](atp-safe-links-warning-pages.md) Feature ein neues Farbschema, Weitere Informationen und die Möglichkeit, die auf einer Website trotz fortgesetzt werden, wenn Warnungen und Empfehlungen. 
 
- Im Oktober 2018 beginnen und anschließend in den nächsten Monaten einführen, umgeschrieben Wenn Personen mit Outlook Web Application (OWA) oder Outlook, ATP sichere Links rendert ursprünglichen URLs nicht URLs. (Wir Aufrufen dieser systemeigene Link Sichtbarkeit.)

      
## <a name="get-office-365-atp"></a>Office 365 ATP abrufen

> [!IMPORTANT]
> Office 365 ATP ist in Abonnements, wie beispielsweise Microsoft 365 Enterprise, Office 365 Enterprise E5, Office 365 Education A5 und [Microsoft 365 Business](https://docs.microsoft.com/en-us/microsoft-365/business/security-features)enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

1. Als globaler oder eine Sicherheitsgruppe an, wechseln Sie zur [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365. 
    
2. Wählen Sie **Admin** \> **Abrechnung** sehen, was Ihr aktuelle Abonnement enthält. <br/>![Als ein globaler Administrator, melden Sie sich am portal.office.com, und wechseln Sie zu Admin \> Abrechnung](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Wenn Sie **Office 365 Enterprise E5**, **Office 365 Education A5**oder **Microsoft 365 Business**angezeigt wird, hat Ihre Organisation ATP. <br/>Wenn Sie ein anderes Abonnement, wie **Office 365 Enterprise E3** oder **Office 365 Enterprise E1**, finden Sie unter berücksichtigen Sie ATP hinzufügen. Wählen Sie hierzu **+ Abonnement hinzufügen**.
    
Sobald Sie ATP haben, besteht der nächste Schritt für Ihr Sicherheitsteam zum Definieren von Richtlinien. 
  
## <a name="define-policies-for-atp"></a>Definieren von Richtlinien für ATP

- Vor Angriffen zu schützen, die Senden von e-Mail-Nachrichten, die **[ATP Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md)** einschließlich Identitätswechsel-basierten Angriffen aus vertrauenswürdigen Personen oder Domänen werden angezeigt 

- [Benutzerdefinierte Liste der blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md) und [benutzerdefinierte Liste für "Nicht rewrite" URLs](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) Ihrer Organisation einschließlich **[Einstellungsrichtlinien ATP sichere Links in Office 365](set-up-atp-safe-links-policies.md)**
    
- **[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)** , die [Dynamische Übermittlung und Anzeigen der Vorschau](dynamic-delivery-and-previewing.md) hinzufügen können
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Finden Sie unter wie ATP funktioniert, indem Sie Berichte anzeigen

Nach Ihrer Richtlinien ATP vorhanden sind, stehen Berichte anzeigen, wie der Dienst ordnungsgemäß funktioniert.

[![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Stellen Sie sicher, dass Sie ein Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheit Reader sind. (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)
    
2. [Anzeigen von Berichten für erweiterte Threat Protection](view-reports-for-atp.md).
    
3. Falls erforderlich, ändern Sie Ihre Sicherheitsrichtlinien. Finden Sie in den folgenden Ressourcen:

  - [ATP Anti-Phishing-Richtlinien in Office 365](set-up-anti-phishing-policies.md)
    
  - [Sichere Links ATP Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
    
  - [Sichere Anlagen ATP Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Dateien Sie verdächtige an Microsoft zur Analyse

- Wenn Sie eine Datei, die vermutlich Schadsoftware werden konnte abrufen, können Sie diese Datei an Microsoft zur Analyse senden. Besuchen Sie das [Windows Defender Security Intelligence Übermittlung Portal](https://go.microsoft.com/fwlink/?linkid=857185).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlagen), die Sie für die Analyse an Microsoft senden möchten erhalten, verwenden Sie das [Bericht-add-in](enable-the-report-message-add-in.md). 
  


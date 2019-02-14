---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 erweiterte Threat Protection umfasst Spoofing Intelligence, sicheren Links, sichere Anlagen, erweiterte Anti-Phishing-Funktionen und Bedrohungsanalyse.
ms.openlocfilehash: 4899073247f4b39e7cda39f8f35544c436c0b2d7
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995216"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

> [!IMPORTANT]
> In diesem Artikel wird für Unternehmenskunden vorgesehen. Wenn Sie eine Suche nach Informationen zu sicheren Links in Outlook Privatbenutzer sind, finden Sie unter [Outlook.com erweiterte Sicherheit](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview-of-office-365-advanced-threat-protection"></a>Übersicht über Office 365 erweiterten Schutz

Hilft bei der Office 365 erweiterte Threat Protection (ATP) zum Schutz Ihrer Organisation vor Angriffen durch:
  
- Überprüfen von e-Mail-Anlagen für Malware mit [ATP sichere Anlagen](atp-safe-attachments.md)
    
- Scan Webadressen (URLs) in e-Mail-Nachrichten und Office-Dokumenten mit [Sicheren ATP-Links](atp-safe-links.md)
    
- Erkannt und blockiert schädliche Dateien in online Bibliotheken mit [ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md)
    
- Überprüfen von e-Mail-Nachrichten für nicht autorisierten spoofing mit [Spoofing intelligence](learn-about-spoof-intelligence.md)
    
- Erkennen, wenn jemand versucht, Identitätswechsel für Ihre Benutzer und Ihrer Organisation benutzerdefinierte Domänen mit [ATP Anti-Phishing-Funktionen in Office 365](atp-anti-phishing.md)
    
**Schutz über Office 365 ATP ergibt sich Richtlinien, die für sichere Links, sichere Anlagen und Phishing - Security-Team Ihrer Organisation definiert**. Es ist wichtig, zum Definieren von Richtlinien, um regelmäßig zu überprüfen und Überarbeiten diese Richtlinien, um diese auf dem aktuellen Stand zu halten und Vorteile der neuen Features nutzen, die den Dienst hinzugefügt werden. 

[Berichte sind verfügbar](view-reports-for-atp.md) , um anzuzeigen, wie ATP für Ihre Organisation arbeitet. Diese Berichte können Sie Bereiche anzeigen, in dem Sie möglicherweise überprüfen und aktualisieren Sie Ihre Richtlinien. Und wenn Sie Dateien gespeichert, die gekennzeichnet sind haben, wie Schadsoftware, die Sie Dateien oder sollte nicht Microsoft überprüfen möchten, können Sie [eine Datei an Microsoft zur Analyse senden](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Neue Features werden ständig ATP hinzugefügt wird

Wir bauen zum Hinzufügen neuer Funktionen zu Office 365 sowie ATP enthält. Es folgt eine Liste der verschiedene neue Features, von denen einige rufen Sie für eine Richtlinie ATP geprüft und aktualisiert werden. Weitere Informationen zu neuen Features der ATP (oder Microsoft 365 im Allgemeinen) finden Sie auf der [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Featureupdates  |Aktionselemente  |
|---------|---------|
|Im Februar 2019 beginnen und anschließend in den nächsten Monaten einführen, sind ATP Threat Intelligence-Funktionen hinzugefügt wird. Darüber hinaus Wenn Ihre Organisation ATP derzeit nicht vorhanden ist, müssen neue Optionen zu berücksichtigen sind, Sie einschließlich ATP Plan 1 und ATP Plan 2. Finden Sie weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). |Überprüfen des Abonnements der Organisation, und gegebenenfalls [gekauft oder ein Add-on bearbeiten](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).  |
|Im Oktober 2018 beginnen und anschließend in den nächsten Monaten einführen, umgeschrieben Wenn Personen Outlook oder Outlook Web Application (OWA), ATP sichere Links rendert ursprünglichen URLs nicht URLs. (Wir Aufrufen dieses systemeigenen Link Rendering.)<br>Wenn systemeigene Link Rendering für Ihre Organisation verfügbar ist, wird dieses Feature in Outlook 365 (Klick-und-Los) und OWA arbeiten.|Keine         |
|Anfang im September 2018, [Office 365 ATP Warnung Seiten](atp-safe-links-warning-pages.md) Feature ein neues Farbschema, Weitere Informationen und die Möglichkeit, die auf einer Website trotz fortgesetzt werden, wenn Warnungen und Empfehlungen. |Keine         |
|In der zweiten Hälfte des 2018 beginnen, ist sicherer Links ATP Schutz erweitert, um URLs in Office Online (Online Word, Excel Online, Online PowerPoint und OneNote Online) und Office 365 ProPlus auf einem Mac gilt   |[Überprüfen Sie und bearbeiten Sie Ihrer Richtlinien ATP sichere Links](set-up-atp-safe-links-policies.md)  |
|Ende Mai 2018, [Quarantäne](quarantine-email-messages.md) -Funktionen in die Sicherheit ab &amp; Compliance Center sind auf [ATP für SharePoint Online, OneDrive für Unternehmen, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md)erweitert wird. |[Überprüfen Sie und bearbeiten Sie Ihrer Richtlinien ATP sichere Anlagen](set-up-atp-safe-attachments-policies.md) |
|März 2018 ab, ist sicherer Links ATP Schutz erweitert, um auf zwischen Personen innerhalb einer Organisation gesendeten e-Mails anwenden. |[Überprüfen Sie und bearbeiten Sie Ihrer Richtlinien ATP sichere Links](set-up-atp-safe-links-policies.md) |
|Verspätete Oktober 2017 ab, ist sicherer Links ATP erweitertem Schutz um URLs in e-Mail-als auch URLs in Office 365 ProPlus-Dokumenten, beispielsweise Word, Excel, PowerPoint und Visio auf Windows als auch Office apps auf iOS und Android-Geräte zuweisen.  |Stellen Sie sicher, dass Sie [Modernen für Office-Authentifizierung](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) verwenden |


      
## <a name="get-office-365-atp"></a>Office 365 ATP abrufen

Office 365 ATP ist in Abonnements, wie beispielsweise [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5 und Office 365 Education A5 enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Definieren von Richtlinien für ATP

Um ATP Richtlinien definieren (oder bearbeiten), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen zugewiesen werden:

|Rolle  |WHERE/wie zugewiesen.  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die zum Erwerben von Office 365 angemeldet ist ein globaler Administrator in der Standardeinstellung. (Siehe [zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) , um mehr zu erfahren.)         |
|Sicherheitsadministrator |Azure Active Directory-Verwaltungskonsole ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Verwaltung von Exchange Online-Organisation |Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).

Es gibt mehrere Arten von Richtlinien zum Definieren und überprüfen Sie regelmäßig ATP.

1. **[ATP Anti-Phishing-Richtlinien in Office 365 einrichten](set-up-anti-phishing-policies.md)** einschließlich Identitätswechsel-basierte Angriffe vor Angriffen zu schützen, die Senden von e-Mail-Nachrichten, die von vertrauenswürdigen Personen oder Domänen werden angezeigt. 

2. [Benutzerdefinierte Liste der blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md) und [benutzerdefinierte Liste für "Nicht rewrite" URLs](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)Ihrer Organisation einschließlich **[Einstellungsrichtlinien ATP sichere Links in Office 365](set-up-atp-safe-links-policies.md)** .
    
3. **[Einrichten von Richtlinien für sichere ATP-Anlagen in Office 365](set-up-atp-safe-attachments-policies.md)** , und wählen Sie mehrere Optionen für [Dynamische Übermittlung und Anzeigen der Vorschau](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Finden Sie unter wie ATP funktioniert, indem Sie Berichte anzeigen

Nach Ihrer Richtlinien ATP vorhanden sind, stehen Berichte anzeigen, wie der Dienst ordnungsgemäß funktioniert. (Navigieren Sie in der & Sicherheit in Office 365 Compliance Center auf **Berichte** > **Dashboard**.)

[![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Als ein globaler Office 365-Administrator, einen Sicherheitsadministrator oder ein Leser Sicherheit, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und zur Anmeldung.
    
2. Wechseln Sie zu **Berichte** > **Dashboard**. (Mit diesen Berichten Hilfe hierzu finden Sie unter [Anzeigen von Berichten für erweiterte Threat Protection](view-reports-for-atp.md).)
    
3. Falls erforderlich, ändern Sie Ihre Sicherheitsrichtlinien. Hilfe hierzu finden Sie unter den folgenden Ressourcen:
      - [ATP Anti-Phishing-Richtlinien in Office 365](set-up-anti-phishing-policies.md)
      - [Sichere Links ATP Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
      - [Sichere Anlagen ATP Richtlinien in Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Dateien Sie verdächtige an Microsoft zur Analyse

- Wenn Sie eine Datei, die vermutlich Schadsoftware werden konnte abrufen, können Sie diese Datei an Microsoft zur Analyse senden. Besuchen Sie das [Windows Defender Security Intelligence Übermittlung Portal](https://go.microsoft.com/fwlink/?linkid=857185).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlagen), die Sie für die Analyse an Microsoft senden möchten erhalten, verwenden Sie das [Bericht-add-in](enable-the-report-message-add-in.md). 
  


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
description: Office 365 Advanced Threat Protection umfasst Spoof-Intelligence, sichere Links, sichere Anlagen, erweiterte Antiphishingfunktionen und Bedrohungs Intelligenz.
ms.openlocfilehash: d78b37ca048187a298b6e083b54ad68b949638ef
ms.sourcegitcommit: 2af6c3e8a74995294a67429530af8f085e6ca136
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051176"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

## <a name="overview-of-office-365-advanced-threat-protection"></a>Übersicht über Office 365 Advanced Threat Protection

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden. Wenn Sie ein Benutzer sind, der nach Informationen zu sicheren Links in Outlook sucht, lesen Sie den Thema [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 Advanced Threat Protection (ATP) hilft Ihnen, Ihre Organisation vor böswilligen Angriffen zu schützen, indem Sie:
  
- ÜberPrüfen von e-Mail-Anlagen für Schadsoftware mit [ATP Safe Attachments](atp-safe-attachments.md)
    
- Überprüfen von Webadressen (URLs) in e-Mail-Nachrichten und Office-Dokumenten mit [ATP-sicheren Links](atp-safe-links.md)
    
- Identifizieren und Blockieren von schädlichen Dateien in Online Bibliotheken mit [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md)
    
- Überprüfen von e-Mail-Nachrichten für unbefugte Spoofing mit [Spoof Intelligence](learn-about-spoof-intelligence.md)
    
- Ermittlung, wenn jemand versucht, die Identität der Benutzer und der benutzerdefinierten Domänen Ihrer Organisation mit den [ATP-Antiphishingfunktionen in Office 365](atp-anti-phishing.md) zu imitieren
    
Der **Schutz durch Office 365 ATP wird durch Richtlinien bestimmt, die das Sicherheitsteam Ihrer Organisation für sichere Links, sichere Anlagen und Antiphishing definiert**. Es ist wichtig, Richtlinien zu definieren und diese Richtlinien regelmäßig zu überprüfen und zu überarbeiten, um Sie auf dem neuesten Stand zu halten und die Vorteile neuer Features zu nutzen, die dem Dienst hinzugefügt werden. 

[Berichte sind verfügbar](view-reports-for-atp.md) , um zu zeigen, wie ATP für Ihre Organisation funktioniert. Diese Berichte können auch Bereiche anzeigen, in denen Sie Ihre Richtlinien überarbeiten und aktualisieren müssen. Und wenn Sie Dateien haben, die als Schadsoftware gekennzeichnet sind, die nicht sein sollte, oder Dateien, die von Microsoft untersucht werden sollen, können Sie [eine Datei zur Analyse an Microsoft übermitteln](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Neue Features werden fortlaufend zu ATP hinzugefügt

Es werden weiterhin neue Features zu Office 365 hinzugefügt, einschließlich ATP. Nachfolgend finden Sie eine Liste mit verschiedenen neuen Features, von denen einige erfordern, dass eine ATP-Richtlinie überprüft und aktualisiert wird. Weitere Informationen zu neuen Features in ATP (oder Microsoft 365 im allgemeinen) finden Sie im [microsoft 365-Fahrplan](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Featureupdates  |Aktionselemente  |
|---------|---------|
|Ab Februar 2019 werden in den nächsten Monaten die Funktionen für Threat Intelligence hinzugefügt. Wenn Ihre Organisation derzeit nicht über ATP verfügt, haben Sie darüber hinaus neue Optionen zu berücksichtigen, einschließlich ATP-Plan 1 und ATP-Plan 2. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). |Überarbeiten Sie das Abonnement Ihrer Organisation, und [kaufen oder bearbeiten Sie, falls erforderlich, ein Add-on](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).  |
|Beginnend im Oktober 2018 und über die nächsten Monate hinaus, wenn Personen Outlook oder Outlook Web Application (OWA) verwenden, rendert ATP Safe Links ursprüngliche URLs, nicht umgeschriebene URLs. (Wir nennen dies Native Link Rendering.)<br>Wenn Native Link Rendering für Ihre Organisation verfügbar ist, funktioniert dieses Feature in Outlook 365 (Click-to-Run) und OWA.|Keine         |
|Beginnend im September 2018, [Office 365 ATP Warning Pages](atp-safe-links-warning-pages.md) Feature ein neues Farbschema, weitere Details und die Möglichkeit, eine Website trotz der Warnungen und Empfehlungen weiterhin. |Keine         |
|Ab der zweiten Hälfte von 2018 wird der ATP-Schutz für sichere Links auf URLs in Office Online (Word Online, Excel Online, PowerPoint Online und OneNote Online) und Office 365 proPlus unter Mac erweitert.   |[Überarbeiten und Bearbeiten Ihrer ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md)  |
|Ab Ende Mai 2018 werden die [Quarantäne](quarantine-email-messages.md) Funktionen im Security &amp; Compliance Center auf [ATP für SharePoint Online, OneDrive for Business und Microsoft Teams](atp-for-spo-odb-and-teams.md)ausgedehnt. |[Überarbeiten und Bearbeiten Ihrer ATP-Richtlinien für sichere Anlagen](set-up-atp-safe-attachments-policies.md) |
|Ab März 2018 wird ATP Safe Links Protection auf e-Mails ausgedehnt, die zwischen Personen innerhalb einer Organisation gesendet werden. |[Überarbeiten und Bearbeiten Ihrer ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md) |
|Ab Ende Oktober 2017 wird der ATP Safe Links Protection auf URLs in e-Mails sowie URLs in Office 365 proPlus-Dokumenten wie Word, Excel, PowerPoint und Visio unter Windows sowie auf Office-Apps auf iOS-und Android-Geräten ausgedehnt.  |Stellen Sie sicher, dass Sie die [moderne Authentifizierung für Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) verwenden. |

## <a name="get-office-365-atp"></a>Office 365 ATP abrufen

Office 365 ATP ist in Abonnements enthalten, wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5 und Office 365 Education a5. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Definieren von Richtlinien für ATP

Um ATP-Richtlinien zu definieren (oder zu bearbeiten), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen besitzen:

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Weitere Informationen zu Rollen und Berechtigungen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).

Es gibt verschiedene Arten von ATP-Richtlinien, die definiert und periodisch überprüft werden sollen.

1. **[Einrichten von ATP-Phishing-Richtlinien in Office 365](set-up-anti-phishing-policies.md)** , einschließlich Identitätswechsel basierten Angriffen zum Schutz vor Angreifern, die e-Mail-Nachrichten senden, die scheinbar von vertrauenswürdigen Personen oder Domänen stammen. 

2. **[Einrichten von Richtlinien für ATP-sichere Links in Office 365](set-up-atp-safe-links-policies.md)** einschließlich der [Liste der benutzerDefinierten blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md) Ihrer Organisation und der [benutzerdefinierten Liste "nicht umschreiben"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
3. **[Richten Sie die Richtlinien für sichere Anlagen in Office 365 ein](set-up-atp-safe-attachments-policies.md)** , und wählen Sie eine der folgenden Optionen aus: [dynamische Bereitstellung und Vorschau](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Anzeigen von Berichten über die ATP-Funktion

Nachdem Sie Ihre ATP-Richtlinien eingerichtet haben, können Berichte angezeigt werden, wie der Dienst funktioniert. (im Office 365 Security & Compliance Center wechseln sie zum Dashboard **berichte** > ****.)

[![Mit dem &amp; Security Compliance Center-Dashboard können Sie erkennen, wo Advanced Threat Protection funktioniert.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Wechseln Sie als globaler Office 365-Administrator, als Sicherheitsadministrator oder als Sicherheits Leser zu und [https://protection.office.com](https://protection.office.com) melden Sie sich an.
    
2. Wechseln Sie zum**Dashboard** **Berichte** > . (Hilfe zu diesen Berichten finden Sie unter [Anzeigen von Berichten für Advanced Threat Protection](view-reports-for-atp.md).)
    
3. Nehmen Sie gegebenenfalls Anpassungen an Ihren Sicherheitsrichtlinien vor. Hilfe hierzu finden Sie in den folgenden Ressourcen:
    - [Anti-Phishing-Richtlinien für ATP](set-up-anti-phishing-policies.md)
    - [Richtlinien für ATP-sichere Links](set-up-atp-safe-links-policies.md)
    - [Richtlinien für ATP-sichere Anlagen](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Übermitteln einer verdächtigen Datei zur Analyse an Microsoft

- Wenn Sie eine Datei erhalten, von der Sie vermuten, dass Sie Schadsoftware sein könnte, können Sie diese Datei zur Analyse an Microsoft übermitteln. Besuchen Sie das [Windows Defender Security Intelligence Submission Portal](https://go.microsoft.com/fwlink/?linkid=857185).

- Wenn Sie eine e-Mail-Nachricht (mit oder ohne Anlage) erhalten, die Sie zur Analyse an Microsoft übermitteln möchten, verwenden Sie das [Add-in Berichtnachricht](enable-the-report-message-add-in.md). 
  


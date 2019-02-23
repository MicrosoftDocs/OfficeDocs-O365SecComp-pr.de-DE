---
title: FAQ zur Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 02/11/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Haben Sie Fragen zur Funktionsweise der neuen Nachrichtenschutzfunktionen in Office 365? Hier finden Sie eine Antwort.
ms.openlocfilehash: 651d3f5953f0a6864259ed3a0c8ecde79f40d631
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217115"
---
# <a name="office-365-message-encryption-faq"></a>FAQ zur Office 365-Nachrichtenverschlüsselung

Haben Sie Fragen zur Funktionsweise der neuen Nachrichtenschutzfunktionen in Office 365? Hier finden Sie eine Antwort. Sehen Sie sich auch die [häufig gestellten Fragen zum Datenschutz in Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/faqs-rms) für Antworten auf Fragen zum Datenschutzdienst, Azure Rights Management, in Azure Information Protection an.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a>Was ist Office 365-Nachrichtenverschlüsselung (OM)?

OM kombiniert Funktionen für die e-Mail-Verschlüsselung und Rechteverwaltung. Rechte Verwaltungsfunktionen werden von Azure Information Protection unterstützt.
  
## <a name="who-can-use-ome"></a>Wer kann OM verwenden?

Sie können die neuen Funktionen für OM unter den folgenden Bedingungen verwenden:
  
- Wenn Sie noch nie OM oder IRM für Exchange Online in Office 365 eingerichtet haben.
    
- Wenn Sie OM und IRM eingerichtet haben, können Sie diese Schritte verwenden, wenn Sie den Azure Rights Management-Dienst von Azure Information Protection verwenden.
    
- Wenn Sie Exchange Online mit Active Directory Rights Management Service (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS zuerst zu Azure Information Protection migrieren](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . Wenn Sie die Migration abgeschlossen haben, können Sie OM erfolgreich einrichten. 
    
    Wenn Sie sich entscheiden, weiterhin lokale AD RMS mit Exchange Online zu verwenden, statt zu Azure Information Protection zu migrieren, können Sie diese neuen Funktionen nicht verwenden.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Welche Abonnements benötige ich, um die neuen OM-Funktionen verwenden zu können?

Um die neuen OM-Funktionen verwenden zu können, benötigen Sie einen der folgenden Pläne:
  
- Office 365 Nachrichtenverschlüsselung wird als Teil von Office 365 Enterprise E3 und E5, Microsoft Enterprise E3 und E5, Microsoft 365 Business, Office 365 a1, a3 und A5 sowie Office 365 Government G3 und G5 angeboten. Kunden benötigen keine zusätzlichen Lizenzen, um die neuen Schutzfunktionen von Azure Information Protection zu erhalten. 
    
- Sie können auch Azure Information Protection-Plan 1 zu den folgenden Plänen hinzufügen, um die neuen Office 365-Nachrichten Verschlüsselungsfunktionen zu erhalten: Exchange Online-Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium oder Office 365 Enterprise E1.
    
- Jeder Benutzer, der von der Office 365-Nachrichtenverschlüsselung profitiert, muss lizenziert sein, damit er von der Funktion abgedeckt wird.
    
- Die vollständige Liste finden Sie in den [Exchange Online-Dienstbeschreibungen](https://technet.microsoft.com/library/exchange-online-service-description.aspx) für die Office 365-Nachrichtenverschlüsselung. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Kann ich Exchange Online mit Ihrem eigenen Schlüssel (BYOK) in Azure Information Protection verwenden?

Ja! Microsoft empfiehlt, dass Sie die Schritte zum Einrichten von BYOK ausführen, bevor Sie OM einrichten.
  
Weitere Informationen zu BYOK finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ändern OM und BYOK mit Azure Information Protection den Ansatz von Microsoft zu Drittanbieter-Datenanforderungen wie Vorladungen?

Nein. OM und die Option zum Bereitstellen und Steuern ihrer eigenen Verschlüsselungsschlüssel, genannt BYOK, von Azure Information Protection wurden nicht entwickelt, um auf Strafverfolgungsbehörden Vorladungen zu reagieren. OM wurde mit BYOK für Azure Information Protection für Compliance-orientierte Kunden entwickelt. Microsoft übernimmt Drittanbieter Anforderungen für Kundendaten sehr ernst. Als Cloud-Dienstanbieter befürworten wir stets den Schutz von Kundendaten. Für den Fall, dass eine Vorladung vorliegt, versuchen wir immer, den dritten an den Kunden zu leiten, um die Informationen zu erhalten. (Lesen Sie den Blog zu Brad Smith: [Schützen von Kundendaten vor der Regierung Snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen in regelmäßigen Abständen detaillierte Informationen zu der Anforderung, die wir erhalten. Weitere Informationen zu Anforderungen von drittanbieterdaten finden Sie unter [Antworten auf Behörden-und Strafverfolgungs Anforderungen für den Zugriff auf Kundendaten](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) im Microsoft Trust Center. Weitere Informationen finden Sie unter "Offenlegung von Kundendaten" im [Online Services Terms (Ost)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>Wie ist dieses Feature mit Legacy Office 365 Message Encryption (OM) und IRM-Funktionen (Information Rights Management, Verwaltung von Informationsrechten) verbunden?

Die neuen Funktionen für die Nachrichtenverschlüsselung von Office 365 sind eine Weiterentwicklung der vorhandenen IRM-und Legacy-Lösungen. Die folgende Tabelle enthält weitere Details.
  
**Vergleich der Funktionen von Legacy OM, IRM und New OM**

|**Funktion**|**Frühere Versionen von OM**|**IRM**|**Neue OM-Funktionen**|
|:-----|:-----|:-----|:-----|
|**Senden einer verschlüsselten e-Mail**|Nur über Exchange-Nachrichtenfluss Regeln|Endbenutzer, die von Outlook für PC, Outlook für Mac oder Outlook im Web initiiert wurden; oder über Exchange-Nachrichtenfluss Regeln|Endbenutzer, die von Outlook für PC, Outlook für Mac oder Outlook im Web initiiert wurden; oder durch Nachrichtenfluss Regeln|
|**Rechteverwaltung**|-|Option und benutzerdefinierte Vorlagen nicht weiterleiten|Option, nur verschlüsselte Option, Standard-und benutzerdefinierte Vorlagen nicht weiterleiten|
|**Unterstützter Empfängertyp**|Nur externe Empfänger|Nur interne Empfänger|Interne und externe Empfänger|
|**Erfahrung für Empfänger**|Externe Empfänger haben eine HTML-Nachricht erhalten, die Sie heruntergeladen und in einem Browser oder einer heruntergeladenen mobilen APP geöffnet haben.|Interne Empfänger haben nur verschlüsselte e-Mails in Outlook für PC, Outlook für Mac und Outlook im Web erhalten.|Interne und externe Empfänger erhalten e-Mails in Outlook für PC, Outlook für Mac, Outlook im Web, Outlook für Android und Outlook für iOS oder über ein Webportal, unabhängig davon, ob Sie sich in derselben Office 365-Organisation oder in einem beliebigen Office 365 befinden. Organisation. Das OM-Portal erfordert keinen separaten Download.|
|**Bringen Sie Ihre eigene Schlüssel Unterstützung mit.**|Nicht verfügbar|Nicht verfügbar| BYOK unterstützt|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Wie aktiviere ich die neuen OM-Funktionen für meine Organisation?

Weitere Informationen finden Sie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>Ist die frühere Version von OM veraltet?

Sie können die frühere Version von OM weiterhin verwenden, Sie ist zu diesem Zeitpunkt nicht veraltet. Wir ermutigen Organisationen jedoch dringend, die neue und verbesserte OM-Lösung zu verwenden. Kunden, die OM noch nicht bereitgestellt haben, können keine neue Bereitstellung der vorherigen Version von OM einrichten.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Meine Organisation verwendet die Active Directory-Rechteverwaltung, kann ich diese Funktion nutzen?

Nein. Wenn Sie Exchange Online mit Active Directory Rights Management Service (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS zuerst zu Azure Information Protection migrieren](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Meine Organisation verfügt über eine Exchange-Hybrid Bereitstellung. Kann ich diese Funktion verwenden?

Lokale Benutzer können verschlüsselte e-Mails mithilfe von Exchange Online-Nachrichtenfluss Regeln senden. Zu diesem Zweck müssen Sie e-Mails über Exchange Online weiterleiten. Weitere Informationen finden Sie unter [Abschnitt 2: Konfigurieren von e-Mails für den Fluss von Ihrem e-Mail-Server zu Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>Welchen e-Mail-Client muss ich verwenden, um eine verschlüsselte Nachricht zu erstellen? Welche Anwendungen werden für das Senden geschützter Nachrichten unterstützt?

Sie können geschützte Nachrichten aus Outlook 2016 und Outlook 2013 für PC und Mac und aus Outlook im Web erstellen.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Welche e-Mail-Clients werden zum Lesen und beantworten geschützter e-Mails unterstützt?

Sie können von Outlook für PC und Mac (2013 und 2016), Outlook im Web und Outlook Mobile (Android und iOS) lesen und darauf antworten, wenn Sie ein Office 365-Benutzer sind. Sie können den systemeigenen e-Mail-Client von iOS auch verwenden, wenn Ihre Organisation dies zulässt. Wenn Sie ein nicht-Office 365-Benutzer sind, können Sie verschlüsselte Nachrichten im Web über Ihren Webbrowser lesen und auf diese Antworten.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Welche Dateitypen werden als Anlagen in geschützten e-Mails unterstützt? Erben Anlagen die Schutzrichtlinien, die mit geschützten e-Mails verbunden sind?

Sie können einen beliebigen Dateityp an eine geschützte e-Mail anfügen, jedoch gelten Schutzrichtlinien nur für die [hier](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)aufgeführten Dateiformate. 
  
Wenn ein Dateiformat wie eine Word-, Excel-oder PowerPoint-Datei unterstützt wird, wird die Datei immer geschützt, auch wenn die Anlage vom Empfänger heruntergeladen wurde. Wenn eine Anlage beispielsweisedurch "nicht weiterleiten" geschützt ist und der ursprüngliche Empfänger die Anlage an einen neuen Empfänger herunterlädt und weiterleitet, kann der neue Empfänger die geschützte Datei nicht öffnen.
  
## <a name="are-pdf-file-attachments-supported"></a>Werden PDF-Dateianhänge unterstützt?

Wenn Sie eine PDF-Datei an eine geschützte Nachricht anfügen, wird die Nachricht selbst geschützt, aber es wird kein zusätzlicher Schutz auf die PDF-Datei angewendet, nachdem Sie vom Empfänger empfangen wurde. Dies führt dazu, dass der Empfänger die PDF-Datei speichern, weiterleiten, kopieren und drucken kann.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>Werden OneDrive for Business-Anhänge unterstützt?

Noch nicht. OneDrive for Business-Anhänge werden nicht unterstützt, und Endbenutzer können keine e-Mails mit einer Cloud-OneDrive for Business-Anlage verschlüsseln.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Kann ich Nachrichten automatisch durch Einrichten von Richtlinien verschlüsseln?

Ja. Verwenden Sie Nachrichtenfluss Regeln in Exchange Online, um eine Nachricht auf der Grundlage bestimmter Bedingungen automatisch zu verschlüsseln. Beispielsweise können Sie Richtlinien erstellen, die auf der Empfänger-ID, der Empfängerdomäne oder auf dem Inhalt im Textkörper oder Betreff der Nachricht basieren. Siehe [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Kann ich Nachrichten automatisch verschlüsseln, indem ich Richtlinien in Data Loss Prevention (DLP &amp; ) über das Security Compliance Center einrichte?

Ja! Sie können Nachrichtenfluss Regeln in Exchange Online oder mithilfe von DLP im Security &amp; Compliance Center einrichten.
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>Können verschlüsselte Nachrichten an ein FreigeGebenes Postfach gesendet werden?

Derzeit verschlüsselte Nachrichten werden für ein FreigeGebenes Postfach nicht unterstützt.

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Kann ich verschlüsselte Nachrichten mit meinem Unternehmensbranding anpassen?

Ja! Weitere Informationen zum Anpassen von e-Mail-Nachrichten und dem OM-Portal finden Sie unter Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten. Weitere Informationen finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Gibt es Berichterstellungsfunktionen oder Einblicke für verschlüsselte e-Mails?

Nicht zu diesem Zeitpunkt, aber bald verfügbar.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Kann ich die Nachrichtenverschlüsselung mit Compliance-Funktionen wie eDiscovery verwenden?

Ja. Alle verschlüsselten e-Mail-Nachrichten sind durch die Office 365-Kompatibilitätsfeatures auffindbar.
  


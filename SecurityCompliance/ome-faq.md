---
title: FAQ zur Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Fragen zur Funktionsweise von der neuen Nachricht Schutzfunktionen in Office 365? Überprüfen Sie nach einer Antwort hier.
ms.openlocfilehash: e35495106b44ccb566f4da743264def8c7d4f96f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696269"
---
# <a name="office-365-message-encryption-faq"></a>FAQ zur Office 365-Nachrichtenverschlüsselung

Fragen zur Funktionsweise von der neuen Nachricht Schutzfunktionen in Office 365? Überprüfen Sie nach einer Antwort hier. Darüber hinaus sehen Sie sich [häufig gestellte Fragen zum Datenschutz in Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/faqs-rms) für Antworten auf Fragen zu Data Protection Service Azure Rights Management in Azure Information Protection.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Fachleute vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht. |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a>Was ist Office 365 Message Encryption (OME)?

OME kombiniert e-Mail-Verschlüsselung und Rights Management-Funktionen. Rights Management-Funktionen werden von Azure Information Protection bereitgestellt.
  
## <a name="who-can-use-ome"></a>Wer OME verwenden können?

Sie können die neuen Funktionen für OME unter den folgenden Umständen verwenden:
  
- Wenn Sie noch nie OME oder IRM für Exchange Online in Office 365 eingerichtet haben.
    
- Wenn Sie OME und IRM eingerichtet haben, können Sie die folgenden Schritte aus, bei der Verwendung des Azure Rights Management-Diensts von Azure Information Protection.
    
- Wenn Sie Exchange Online mit Active Directory-Rechteverwaltungsdienste-Dienst (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) migrieren. Wenn Sie die Migration abgeschlossen haben, können Sie erfolgreich OME einrichten. 
    
    Wenn Sie angeben, dass auch weiterhin mithilfe der lokale AD RMS mit Exchange Online anstelle der Migration zu Azure Information Protection nicht werden diese neuen Funktionen verwenden können.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Welche Abonnements benötige ich zum Verwenden der neuen OME-Funktionen?

Um die neuen OME-Funktionen zu verwenden, benötigen Sie einen der folgenden Pläne:
  
- Office 365 Message Encryption wird als Teil von Office 365 E3 und E5, Microsoft E3 und E5, Office 365 A1, A3, und A5 und Office 365 G3 und G5 angeboten werden. Kunden benötigen keine zusätzliche Lizenzen die neuen Schutzfunktionen unterstützt von Azure Information Protection empfangen. 
    
- Sie können auch die Azure Informationen Protection Plan 1 die folgenden Pläne erhalten Sie die neuen Funktionen von Office 365 Message Encryption hinzufügen: Exchange Online – Plan 1, Exchange Online – Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium oder Office 365 Enterprise E1.
    
- Jeder Benutzer profitieren von Office 365 Message Encryption muss lizenziert werden, um die vom Feature abgedeckt werden.
    
- Die vollständige Liste finden Sie unter den [Exchange Online-dienstbeschreibungen](https://technet.microsoft.com/library/exchange-online-service-description.aspx) für Office 365 Message Encryption. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Kann ich verwenden, Exchange Online mit Ihren eigenen Schlüssel (BYOK) in Azure Information Protection zu bringen?

Ja! Microsoft empfiehlt, dass Sie die Schritte BYOK einrichten, bevor Sie OME einrichten.
  
Weitere Informationen zu BYOK finden Sie unter [Planung und Implementierung Ihrer mandantenschlüssel Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Ändere OME und BYOK mit Azure Information Protection Microsofts Ansatz zur Drittanbieter-Daten von Anforderungen wie Anträge?

Nein. OME und die Option bereitgestellt und steuern Ihre eigene Verschlüsselungsschlüssel BYOK, von Azure Information Protection aufgerufen wurden nicht zur Beantwortung Recht Erzwingung Anträge entwickelt. OME, mit BYOK zum Schutz der Azure-Daten, wurde für Kunden Compliance-Experten entwickelt. Microsoft nimmt sehr stark Drittanbieter-Anforderungen für die Kundendaten. Als Cloud-Dienstanbieter Vertreter wir immer für die Vertraulichkeit der Kundendaten. In der Ereignisprozedur wir eine Vorladung erhalten möchten, versuchen wir immer zur Umleitung von Drittanbieter an den Kunden, die Informationen zu erhalten. (Brad Smith Blog lesen: [Protecting Kundendaten von Behörden snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen regelmäßig detaillierte Informationen der Anforderung, die wir empfangen. Weitere Informationen zu Drittanbieter-Daten Anforderungen finden Sie unter [Reagieren auf Behörden und Recht Erzwingung der Anforderungen an die Kundendaten zugreifen](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) auf die Microsoft-Trust Center. Darüber hinaus finden Sie unter "Offenlegung von Kundendaten" in der [Online Services-Begriffe (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>Bezieht dieses Feature sich wie auf ältere Features von Office 365 Message Encryption (OME) und (Information Rights Management, IRM)?

Die neuen Funktionen für Office 365-Nachrichtenverschlüsselung sind eine Weiterentwicklung von der vorhandenen IRM und ältere OME-Lösungen. Die folgende Tabelle enthält weitere Details.
  
**Vergleich der Vorversion OME IRM und neuen OME-Funktionen**

|**Funktion**|**Frühere Versionen von OME**|**IRM**|**Neue OME-Funktionen**|
|:-----|:-----|:-----|:-----|
|**Eine verschlüsselte e-Mail senden.**|Nur über Exchange Mail Flow Regeln|Endbenutzer, die in Outlook für PC, Outlook für Mac oder Outlook im Web initiiert; oder über Exchange mail Flow Regeln|Endbenutzer, die in Outlook für PC, Outlook für Mac oder Outlook im Web initiiert; oder über e-Mail-Flussregeln|
|**Rechteverwaltung**|-|Nicht weiterleiten Option und benutzerdefinierte Vorlagen|Nicht weiterleiten Option, Option nur zu verschlüsseln, Standard und benutzerdefinierten Vorlagen|
|**Unterstützte Empfängertyp**|Nur externe Empfänger|Nur interne Empfänger|Interne und externe Empfänger|
|**Erfahrung für Empfänger**|Externe Empfänger empfangen eine HTML-Nachricht, dass sie heruntergeladen und in einem Browser geöffnet oder mobile app heruntergeladen.|Interne Empfänger empfangen nur verschlüsselten e-Mail in Outlook für PC, Outlook für Mac und Outlook im Web.|Interne und externe Empfänger empfangen von e-Mails in Outlook für PC, Outlook für Mac, Outlook im Web, für Android Outlook und Outlook für iOS oder über ein Webportal, unabhängig davon, ob sie in der gleichen Office 365-Organisation oder in eine beliebige Office 365 sind Organisation. Das OME-Portal ist kein separaten Download erforderlich.|
|**Bringen Sie Ihre eigenen Schlüssel-Unterstützung**|Nicht verfügbar|Nicht verfügbar| BYOK unterstützt|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Wie aktiviere ich die neuen OME-Funktionen für meine Organisation?

Finden Sie unter [Einrichten von neuen Funktionen von Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>Wird die vorherige Version des OME nicht mehr werden verwendet?

Sie können weiterhin die vorherige Version des OME verwenden, wird zu diesem Zeitpunkt nicht verworfen werden. Allerdings empfehlen wir dringend Organisationen, die neue und verbesserte OME-Lösung verwenden. Kunden, die nicht bereits OME bereitgestellt haben, können keine neue Bereitstellung der vorherigen Version von OME einrichten.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Verwendet Meine Organisation Active Directory Rights Management, können diese Funktion verwenden?

Nein. Wenn Sie Exchange Online mit Active Directory-Rechteverwaltungsdienste-Dienst (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) migrieren. 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Meine Organisation hat eine hybride Exchange-Bereitstellung. Kann ich diese Funktion verwenden?

In der lokalen Benutzer mit Exchange Online e-Mail-Flussregeln für verschlüsselte e-Mails senden können. Zu diesem Zweck müssen Sie zum Weiterleiten von e-Mails über Exchange Online. Weitere Informationen finden Sie unter [Teil 2: Konfigurieren von Mail flow von Ihrem e-Mail-Server zu Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>Welche e-Mail-Client verwenden, um eine verschlüsselte Nachricht OME erstellen müssen? Welche Anwendungen zum Senden von unterstützt werden geschützte Nachrichten?

Sie können geschützte Nachrichten von Outlook 2016 und Outlook 2013 für PCs und Mac und von Outlook im Web erstellen.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Welche e-Mail-Clients werden zum Lesen und Antworten auf geschützte e-Mails unterstützt?

Sie können lesen und Beantworten von Outlook für PC und Mac (2013 und 2016), Outlook im Web und Outlook mobile (Android und iOS) Wenn Sie ein Office 365-Benutzer sind. Sie können auch den systemeigene iOS-Mailclient verwenden, wenn Ihre Organisation dies zulässt. Wenn Sie einen nicht - Office 365-Benutzer sind, können Sie lesen und beantworten verschlüsselter Nachrichten im Web über den Webbrowser.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Welche Dateitypen als Anlagen in geschützte e-Mails unterstützt werden? Erben Anlagen die Protection-Richtlinien geschützte e-Mails zugeordnet?

Sie können eine geschützte e-Mail, jeden Dateityp zuordnen, jedoch nur auf die Dateiformate weiter oben erwähnt [hier](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)Protection-Richtlinien angewendet werden. 
  
Wenn ein Dateiformat, wie etwa Word, Excel oder PowerPoint-Datei unterstützt wird ist die Datei immer geschützt, auch wenn die Anlage vom Empfänger heruntergeladen wurde. Beispielsweise wird, wenn eine Anlage durch nicht weiterleiten geschützt ist, und der ursprüngliche Empfänger downloads und die Anlage an einen neuen Empfänger weiterleitet, der neue Empfänger nicht die geschützte Datei öffnen können.
  
## <a name="are-pdf-file-attachments-supported"></a>Werden PDF-Dateianlagen werden unterstützt?

Wenn Sie eine PDF-Datei zu einer geschützten Nachricht angefügt werden, wird die Nachricht selbst geschützt werden, aber keine zusätzlicher Schutz wird in das PDF-Datei angewendet werden, nachdem der Empfänger es erhalten hat. Dies bedeutet, dass der Empfänger kann speichern unter, weiterleiten, kopieren und Drucken der PDF-Datei.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>Sind Sie OneDrive for Business-Anlagen unterstützt?

Noch nicht. OneDrive for Business-Anlagen werden nicht unterstützt und Endbenutzer können nicht Verschlüsseln einer e-Mails, die eine Cloud OneDrive for Business-Anlage enthält.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Kann ich automatisch Verschlüsseln von Nachrichten durch Richtlinien einrichten?

Ja. Verwenden von e-Mail-Flussregeln in Exchange Online zum Verschlüsseln von automatisch basierten auf bestimmten Umständen einer Meldung. Sie können beispielsweise erstellen Richtlinien, die auf Empfänger basieren Domäne des Empfängers,-ID oder des Inhalts in der Nachrichtentext oder Betreff der Nachricht. Finden Sie unter [e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365 definieren.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Kann ich automatisch Verschlüsseln von Nachrichten durch Einrichten von Richtlinien in Data Loss Prevention (DLP) über die Sicherheit &amp; Compliance Center?

Ja! Sie können e-Mail-Flussregeln in Exchange Online oder über DLP in das Wertpapier einrichten &amp; Compliance Center.
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>Kann ich verschlüsselte Nachrichten mit einem freigegebenen Postfach öffnen?

Derzeit verschlüsselte Nachrichten werden für ein Postfach Shared nicht unterstützt.

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Kann ich mit meinem Unternehmen branding verschlüsselte Nachrichten anpassen?

Ja! Informationen zum Anpassen von e-Mail-Nachrichten und das OME-Portal finden Sie unter Ihren verschlüsselten Nachrichten Marke Ihres Unternehmens hinzuzufügen. Finden Sie unter [Ihren verschlüsselten Nachrichten Marke Ihres Unternehmens hinzuzufügen.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Gibt es reporting-Funktionen oder Insights für verschlüsselte e-Mails?

Nicht am diesmal aber in Kürze verfügbar.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Kann ich mit Compliance-Funktionen wie eDiscovery-nachrichtenverschlüsselung verwenden?

Ja. Alle verschlüsselten e-Mail-Nachrichten werden von Office 365 Kompatibilitätsfeatures erkannt.
  


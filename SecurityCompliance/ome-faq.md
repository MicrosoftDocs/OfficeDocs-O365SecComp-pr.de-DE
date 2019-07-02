---
title: FAQ zur Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 02/11/2019
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Haben Sie eine Frage zur Funktionsweise der neuen Nachrichtenschutzfunktionen in Office 365? Hier finden Sie eine Antwort.
ms.openlocfilehash: 1625ecd3f2c7991e2726539bcfa0c772d1ffea59
ms.sourcegitcommit: 803baca9f99a6691fb41a3308e799752e4d8f20c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2019
ms.locfileid: "35222259"
---
# <a name="office-365-message-encryption-faq"></a>Häufig gestellte Fragen zur Office 365-Nachrichtenverschlüsselung

Haben Sie eine Frage zur Funktionsweise der neuen Nachrichtenschutzfunktionen in Office 365? Hier finden Sie eine Antwort. Lesen Sie auch die [häufig gestellten Fragen zum Datenschutz in Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/faqs-rms) für Antworten auf Fragen zum Datenschutzdienst, Azure Rights Management, in Azure Information Protection.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln über Office 365 Nachrichtenverschlüsselung. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur auf der Suche nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht sind, lesen Sie die Artikelliste in [Office 365 Nachrichtenverschlüsselung (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a>Was ist Office 365 Nachrichtenverschlüsselung (OM)?

OM kombiniert Funktionen für e-Mail-Verschlüsselung und Rechteverwaltung. Rechte Verwaltungsfunktionen werden von Azure Information Protection betrieben.
  
## <a name="who-can-use-ome"></a>Wer kann OM verwenden?

Sie können die neuen Funktionen für OM unter den folgenden Bedingungen verwenden:
  
- Wenn Sie weder OM noch IRM für Exchange Online in Office 365 eingerichtet haben.

- Wenn Sie "OM" und "IRM" eingerichtet haben, können Sie diese Schritte verwenden, wenn Sie den Azure Rights Management-Dienst von Azure Information Protection verwenden.

- Wenn Sie Exchange Online mit Active Directory Rights Management Service (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS zunächst in Azure Information Protection migrieren](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . Wenn Sie die Migration abgeschlossen haben, können Sie OM erfolgreich einrichten.

    Wenn Sie weiterhin lokale AD RMS mit Exchange Online anstelle der Migration zu Azure Information Protection verwenden möchten, können Sie diese neuen Funktionen nicht verwenden.

## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Welche Abonnements benötige ich für die Verwendung der neuen OM-Funktionen?

Um die neuen OM-Funktionen verwenden zu können, benötigen Sie einen der folgenden Pläne:
  
- Office 365 Nachrichtenverschlüsselung wird im Rahmen von Office 365 Enterprise E3 und E5, Microsoft Enterprise E3 und E5, Microsoft 365 Business, Office 365 a1, a3 und A5 sowie Office 365 Government G3 und G5 angeboten. Kunden benötigen keine zusätzlichen Lizenzen, um die neuen Schutzfunktionen zu erhalten, die von Azure Information Protection betrieben werden.

- Sie können auch Azure Information Protection Plan 1 zu den folgenden Plänen hinzufügen, um die neuen Office 365 Nachrichten Verschlüsselungsfunktionen zu erhalten: Exchange Online Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium oder Office 365 Enterprise E1.

- Jeder Benutzer, der von Office 365 Nachrichtenverschlüsselung profitiert, muss lizenziert sein, damit er von der Funktion abgedeckt wird.

- Eine vollständige Liste finden Sie in den [Exchange Online-Dienstbeschreibungen](https://technet.microsoft.com/library/exchange-online-service-description.aspx) für Office 365 Nachrichtenverschlüsselung.

## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Kann ich Exchange Online mit "eigenen Schlüssel holen" (BYOK) in Azure Information Protection verwenden?

Ja! Microsoft empfiehlt, die Schritte zum Einrichten von BYOK vor dem Einrichten von OM abzuschließen.
  
Weitere Informationen zu BYOK finden Sie unter [Planung und Implementierung Ihres Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Haben OM und BYOK mit Azure Information Protection den Ansatz von Microsoft für Drittanbieter-Datenanforderungen wie beispielsweise Vorladungen geändert?

Nein. OM und die Option zum Bereitstellen und Steuern ihrer eigenen Verschlüsselungsschlüssel, genannt BYOK, von Azure Information Protection wurden nicht entwickelt, um auf Strafverfolgungs Vorladungen zu reagieren. OM mit BYOK für Azure Information Protection wurde für Compliance-orientierte Kunden entwickelt. Microsoft nimmt Anfragen von Drittanbietern für Kundendaten sehr ernst. Als Anbieter von Cloud-Diensten plädieren wir immer für den Schutz von Kundendaten. Für den Fall, dass wir eine Vorladung erhalten, versuchen wir immer, den dritten an den Kunden umzuleiten, um die Informationen zu erhalten. (Lesen Sie bitte Brad Smith es Blog: [Schützen von Kundendaten vor Regierungs snoopings](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Wir veröffentlichen regelmäßig detaillierte Informationen über die Anforderung, die wir erhalten. Weitere Informationen zu Datenanforderungen von Drittanbietern finden Sie unter [reagieren auf Behörden-und Strafverfolgungs Anfragen für den Zugriff auf Kundendaten](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) im Microsoft Trust Center. Siehe auch "Offenlegung von Kundendaten" in den [Online Dienste-Bedingungen (Ost)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>Wie ist dieses Feature im Zusammenhang mit Legacy-Office 365 Nachrichtenverschlüsselung (OM) und IRM-Funktionen (Information Rights Management, Verwaltung von Informationsrechten)?

Die neuen Funktionen für Office 365 Nachrichtenverschlüsselung stellen eine Weiterentwicklung der vorhandenen IRM-und Legacy-OM-Lösungen dar. In der folgenden Tabelle finden Sie weitere Details.
  
**Vergleich von Legacy-OM-, IRM-und neuen OM-Funktionen**

|**Funktion**|**Frühere Versionen von OM**|**IRM**|**Neue OM-Funktionen**|
|:-----|:-----|:-----|:-----|
|**Senden einer verschlüsselten e-Mail**|Nur über Exchange-Nachrichtenfluss Regeln|Von Outlook für PC, Outlook für Mac oder Outlook im Internet initiierter Endbenutzer; oder über Exchange-Nachrichtenfluss Regeln|Von Outlook für PC, Outlook für Mac oder Outlook im Internet initiierter Endbenutzer; oder über Nachrichtenfluss Regeln|
|**Rechteverwaltung**|-|Option und benutzerdefinierte Vorlagen nicht weiterleiten|Option "nicht weiterleiten", Option "nur verschlüsseln", Standard-und benutzerdefinierte Vorlagen|
|**Unterstützte Empfängertypen**|Nur externe Empfänger|Nur interne Empfänger|Interne und externe Empfänger|
|**Erfahrung für Empfänger**|Externe Empfänger haben eine HTML-Nachricht erhalten, die Sie heruntergeladen und in einem Browser geöffnet oder Mobile App heruntergeladen haben.|Interne Empfänger haben nur verschlüsselte e-Mails in Outlook für PC, Outlook für Mac und Outlook im Internet erhalten.|Interne und externe Empfänger empfangen e-Mails in Outlook für PC, Outlook für Mac, Outlook im Internet, Outlook für Android und Outlook für IOS oder über ein Webportal, unabhängig davon, ob Sie sich in derselben Office 365 Organisation oder in einer Office 365 Organisation. Das OM-Portal erfordert keinen separaten Download.|
|**Holen Sie sich Ihre eigene Schlüssel Unterstützung**|Nicht verfügbar|Nicht verfügbar| BYOK unterstützt|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Wie aktiviere ich die neuen OM-Funktionen für meine Organisation?

Weitere Informationen finden Sie unter [Einrichten neuer Office 365 Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>Wird die vorherige Version von OM veraltet?

Sie können die vorherige Version von OM weiterhin verwenden, Sie wird derzeit nicht als veraltet markiert. Wir ermutigen Organisationen jedoch sehr, die neue und verbesserte Lösung für den OM zu verwenden. Kunden, die nicht bereits OM bereitgestellt haben, können keine neue Bereitstellung der vorherigen Version von OM einrichten.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Kann meine Organisation Active Directory Rechteverwaltung verwenden?

Nein. Wenn Sie Exchange Online mit Active Directory Rights Management Service (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie [AD RMS zunächst in Azure Information Protection migrieren](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Meine Organisation verfügt über eine Exchange-Hybrid Bereitstellung. Kann ich dieses Feature verwenden?

Lokale Benutzer können verschlüsselte e-Mails mit Exchange Online Nachrichtenfluss Regeln senden. Um dies zu erreichen, müssen Sie e-Mails über Exchange Online weiterleiten. Weitere Informationen finden Sie unter [Part 2: Konfigurieren von e-Mail-Fluss von Ihrem e-Mail-Server zu Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>Welchen e-Mail-Client muss ich verwenden, um eine OM-verschlüsselte Nachricht zu erstellen? Welche Anwendungen werden für das Senden geschützter Nachrichten unterstützt?

Sie können geschützte Nachrichten aus Outlook 2016 und Outlook 2013 für PC und Mac und aus Outlook im Internet erstellen.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Welche e-Mail-Clients werden zum Lesen und beantworten geschützter e-Mails unterstützt?

Sie können Outlook für PC und Mac (2013 und 2016), Outlook im Web und Outlook Mobile (Android und IOS) lesen und darauf antworten, wenn Sie ein Office 365er Benutzer sind. Sie können auch den IOS-systemeigenen e-Mail-Client verwenden, wenn Ihre Organisation dies zulässt. Wenn Sie ein nicht Office 365er Benutzer sind, können Sie verschlüsselte Nachrichten im Web über Ihren Webbrowser lesen und beantworten.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Welche Dateitypen werden als Anlagen in geschützten e-Mail-Nachrichten unterstützt? Erben Anlagen die Schutzrichtlinien, die geschützten e-Mails zugeordnet sind?

Sie können einen beliebigen Dateityp an eine geschützte e-Mail-Nachricht anfügen, aber Schutzrichtlinien werden nur auf die [hier](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)erwähnten Dateiformate angewendet. 
  
Wenn ein Dateiformat unterstützt wird, beispielsweise eine Word-, Excel-oder PowerPoint-Datei, ist die Datei immer geschützt, auch wenn die Anlage vom Empfänger heruntergeladen wurde. Wenn beispielsweise eine Anlage durch do not Forward geschützt ist und der ursprüngliche Empfänger die Anlage an einen neuen Empfänger herunterlädt und leitet, kann der neue Empfänger die geschützte Datei nicht öffnen.
  
## <a name="are-pdf-file-attachments-supported"></a>Werden PDF-Dateianlagen unterstützt?

Wenn Sie eine PDF-Datei an eine geschützte Nachricht anfügen, wird die Nachricht selbst geschützt, aber kein zusätzlicher Schutz wird auf die PDF-Datei angewendet, nachdem der Empfänger Sie empfangen hat. Dies bedeutet, dass der Empfänger die PDF-Datei speichern, weiterleiten, kopieren und ausdrucken kann.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>Werden OneDrive für Unternehmen Anlagen unterstützt?

Not yet. OneDrive für Unternehmen Anlagen werden nicht unterstützt, und Endbenutzer können keine e-Mails verschlüsseln, die eine Cloud OneDrive für Unternehmen Anlage enthalten.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Kann ich Nachrichten automatisch verschlüsseln, indem ich Richtlinien einrichte?

Ja. Verwenden von Nachrichtenfluss Regeln in Exchange Online zum automatischen Verschlüsseln einer Nachricht basierend auf bestimmten Bedingungen. Sie können beispielsweise Richtlinien erstellen, die auf der Empfänger-ID, der Empfängerdomäne oder auf dem Inhalt im Textkörper oder Betreff der Nachricht basieren. Siehe [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Kann ich Nachrichten automatisch verschlüsseln, indem ich Richtlinien in Data Loss Prevention (DLP &amp; ) über das Security Compliance Center einrichtete?

Ja! Sie können Nachrichtenfluss Regeln in Exchange Online oder mithilfe von DLP im Security &amp; Compliance Center einrichten.
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>Kann ich an ein freigegebenes Postfach gesendete verschlüsselte Nachrichten öffnen?

Derzeit verschlüsselte Nachrichten werden für ein freigegebenes Postfach nicht unterstützt.

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Kann ich verschlüsselte Nachrichten mit dem Branding meines Unternehmens anpassen?

Ja! Informationen zum Anpassen von e-Mail-Nachrichten und zum OM-Portal finden Sie unter Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten. Weitere Informationen finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu verschlüsselten Nachrichten.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Gibt es Berichtsfunktionen oder Einblicke in verschlüsselte e-Mails?

Es gibt einen Verschlüsselungs Bericht im Security and Compliance Center. Weitere Informationen finden Sie unter [Anzeigen von e-Mail-Sicherheitsberichten im Security #a0 Compliance Center.](view-email-security-reports.md)
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Kann ich Nachrichtenverschlüsselung mit Compliance-Features wie eDiscovery verwenden?

Ja. Alle verschlüsselten e-Mail-Nachrichten können durch Office 365 Compliance-Features erkannt werden.

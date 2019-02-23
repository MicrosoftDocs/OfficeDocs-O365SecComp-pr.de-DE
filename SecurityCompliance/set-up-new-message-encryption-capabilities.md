---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Neue Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren, kann Ihre Organisation geschützte e-Mail-Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation verwenden. Die neuen OM-Funktionen funktionieren mit anderen Office 365-Organisationen, Outlook.com, Gmail und anderen e-Mail-Diensten.
ms.openlocfilehash: eddafca15fa4efdd3f929145e7933a3b7dfb5f27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220645"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen

Mit den neuen Funktionen von Office 365 Message Encryption (OM), die die Schutzfunktionen von Azure Information Protection nutzen, kann Ihre Organisation geschützte e-Mails problemlos für alle Benutzer auf einem beliebigen Gerät freigeben. Benutzer können mit Outlook.com, Gmail und anderen e-Mail-Diensten geschützte Nachrichten mit anderen Office 365-Organisationen sowie nicht-Office 365-Kunden senden und empfangen.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Erste Schritte mit OM durch Aktivieren von Azure Rights Management, Teil von Azure Information Protection

Es ist jetzt einfach, mit den neuen OM-Funktionen zu beginnen. Ab Februar 2018 aktiviert Office 365 automatisch die neuen OM-Funktionen für berechtigte Organisationen in unseren Rechenzentren. Ihre Organisation ist berechtigt, wenn es sich um einen neuen Office 365-Mandanten handelt und Ihre Organisation über die entsprechenden Abonnements verfügt. **Wenn Sie Azure Rights Management (Azure RMS), Teil von Azure Information Protection, aktiviert haben, aktivieren wir die Office 365-Nachrichtenverschlüsselung automatisch für Sie.** Sie müssen nichts weiter tun, um OM zu aktivieren. Informationen zur Aktivierung der Azure-Rechteverwaltung finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Informationen zu Abonnements finden Sie in den häufig gestellten [Fragen zur Office 365-Nachrichtenverschlüsselung](ome-faq.md)unter "welche Abonnements brauche ich, um die neue OM-capabilities? zu verwenden. Informationen zum Erwerb eines Abonnements für Azure Information Protection finden Sie unter [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).
  
Wenn Sie Exchange Online mit Active Directory Rights Management Service (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie zuerst von AD RMS zu Azure Information Protection migrieren. Nachdem Sie die Migration abgeschlossen haben, können Sie diese Schritte erfolgreich ausführen.
  
Wenn Sie sich entscheiden, weiterhin lokale AD RMS mit Exchange Online zu verwenden, statt zu Azure Information Protection zu migrieren, können Sie diese neuen Funktionen nicht verwenden.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Funktionsweise der neuen Funktionen für OM

Die neuen Office 365-Nachrichten Verschlüsselungsfunktionen verwenden die Schutzfunktionen, auch Azure Rights Management (Azure RMS), von Azure Information Protection. Hierzu gehören Verschlüsselungs-, Identitäts-und Autorisierungsrichtlinien, um Ihre e-Mails zu schützen. Sie können Nachrichten verschlüsseln, indem Sie Vorlagen für die Rechteverwaltung, die [Option nicht weiterleiten](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)und die [Option nur](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)verschlüsseln verwenden. Mithilfe dieser Optionen können Benutzer e-Mail-Nachrichten und eine Vielzahl von Office 365-Anlagen verschlüsseln. Eine vollständige Liste der unterstützten Anlagentypen finden Sie unter ["Dateitypen, die von IRM-Richtlinien abgedeckt werden, wenn Sie an Nachrichten angefügt werden" in Einführung in IRM für e-Mail-Nachrichten](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). Als Administrator können Sie auch Nachrichtenfluss Regeln definieren, um diesen Schutz anzuwenden. Sie können beispielsweise eine Regel definieren, bei der alle ungeschützten Nachrichten, die an einen bestimmten Empfänger adressiert sind oder bestimmte Wörter in der Betreffzeile enthalten, vor nicht autorisiertem Zugriff geschützt sind und die Empfänger den Inhalt der Nachricht nicht kopieren oder ausdrucken können.
  
Anders als bei der früheren Version von OM bieten diese neuen Funktionen eine einheitliche Absender Erfahrung, unabhängig davon, ob Sie e-Mails innerhalb Ihrer Organisation oder an Empfänger außerhalb von Office 365 senden. Darüber hinaus müssen Empfänger, die eine geschützte e-Mail-Nachricht erhalten, die an ein Office 365-Konto in Outlook 2016 oder Outlook im Web gesendet wird, keine zusätzlichen Aktionen ausführen, um die Nachricht anzuzeigen. Es funktioniert nahtlos. Empfänger, die andere e-Mail-Clients und e-Mail-Dienstanbieter verwenden, haben ebenfalls eine verbesserte Erfahrung. Weitere Informationen finden Sie unter [erfahren Sie mehr über geschützte Nachrichten in Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) und [wie öffne ich eine geschützte Nachricht](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).

Eine detaillierte Liste der Unterschiede zwischen der vorherigen Version von OM und den neuen OM-Funktionen finden Sie unter [Compare Versionen of OM](ome-version-comparison.md).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>Schritte zum manuellen Einrichten der neuen Funktionen für OM

Die neuen OM-Funktionen werden für die meisten Office 365-Organisationen automatisch aktiviert. Führen Sie die folgenden Schritte aus, um die neuen Funktionen für OM manuell einzurichten, wenn Ihre Organisation nicht automatisch aktiviert ist oder Sie die neuen Funktionen von OM deaktiviert haben.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>So richten Sie die neuen Funktionen für OM manuell ein

1. Stellen Sie sicher, dass Sie das richtige Abonnement für Ihre Organisation haben. Informationen zu Abonnements finden Sie unter "welche Abonnements brauche ich, um die neue OM-capabilities?" in den [Office 365-Nachrichten Verschlüsselungs Fragen](ome-faq.md)zu verwenden. Informationen zum Erwerb eines Abonnements für Azure Information Protection finden Sie unter [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

2. Entscheiden Sie, ob Sie möchten, dass Microsoft den Stammschlüssel für Azure Information Protection (Standard) verwaltet, oder generieren und verwalten Sie diesen Schlüssel selbst (bekannt als bringen Sie Ihren eigenen Schlüssel, oder BYOK). Wenn Sie diesen Schlüssel selbst generieren und verwalten möchten, müssen Sie einige Schritte ausführen, bevor Sie die neuen Funktionen für OM einrichten. Weitere Informationen finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft empfiehlt, dass Sie diese Schritte ausführen, bevor Sie OM einrichten.

3. Aktivieren Sie die neuen Funktionen für OM, indem Sie Azure Rights Management aktivieren. Anweisungen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Wenn Sie dies tun, aktiviert Office 365 automatisch die neuen OM-Funktionen für Sie.

    > [!TIP]
    > Outlook im Web speichert die Benutzeroberfläche zwischen, daher empfiehlt es sich, einen Tag zu warten, bevor Sie versuchen, die neuen Funktionen für Om auf e-Mail-Nachrichten mit diesem Client anzuwenden. Bevor die Benutzeroberfläche aktualisiert wird, um die neue Konfiguration widerzuspiegeln, stehen die neuen Funktionen für om nicht zur Verfügung. Nach der Aktualisierung der Benutzeroberfläche können Benutzer e-Mail-Nachrichten mithilfe der neuen Funktionen für OM schützen.
  
4. Optional Richten Sie neue Nachrichtenfluss Regeln ein, oder aktualisieren Sie vorhandene Nachrichtenfluss Regeln, die definieren, wie und wann Office 365 Nachrichten verschlüsseln soll, die von Ihrer Organisation gesendet werden.

## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Überprüfen, ob die neuen Funktionen für OM mithilfe von Windows PowerShell ordnungsgemäß konfiguriert sind

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihr Mandant ordnungsgemäß für die Verwendung der neuen Funktionen für OM über Exchange Online PowerShell konfiguriert ist.
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   Beispiel:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

    Dabei ist die e-Mail-Adresse die e-Mail-Adresse eines Benutzers in Ihrer Office 365-Organisation. Während optional eine Absender-e-Mail-Adresse bereitstellt, wird das System gezwungen, zusätzliche Prüfungen durchzuführen. Ihre Ergebnisse sollten wie folgt aussehen:

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

    Wobei *contoso* durch den Namen ihrer Office 365-Organisation ersetzt wird.

    Die Namen der Standardvorlagen, die in den Ergebnissen zurückgegeben werden, können sich von denen in den Ergebnissen unterscheiden.

    Eine Einführung in Vorlagen und Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zur Option "nicht weiterleiten", "nur verschlüsseln" und wie Sie zusätzliche Vorlagen erstellen, oder um herauszufinden, welche Rechte in einer vorhandenen Vorlage enthalten sind, finden Sie unter [Configuring Usage Rights for Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).

3. Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rechteverwaltungsdienst zu trennen.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Nächste Schritte: Definieren neuer Nachrichtenfluss Regeln, die die neuen OM-Funktionen verwenden

Dieser Schritt ist optional für neue OM-Bereitstellungen, dieser Schritt ist jedoch für vorhandene OM-Bereitstellungen erforderlich, für die bereits Nachrichtenfluss Regeln zum Verschlüsseln ausgehender e-Mails eingerichtet sind. Wenn Sie die neuen OM-Funktionen nutzen möchten, müssen Sie Ihre vorhandenen Nachrichtenfluss Regeln aktualisieren. Andernfalls erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat anstelle der neuen, nahtlosen OM-Umgebung verwenden.
  
Nachrichtenfluss Regeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden sollen, sowie Bedingungen zum Entfernen dieser Verschlüsselung. Wenn Sie eine Aktion für eine Regel festlegen, werden alle Nachrichten, die den Regelbedingungen entsprechen, beim Senden verschlüsselt.
  
Weitere Informationen zu Nachrichtenfluss Regeln finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Senden, anzeigen und beantworten von verschlüsselten Nachrichten in Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm aus](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
  
[Definieren von Nachrichtenflussregeln zum Verschlüsseln von E-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md)

---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Neue Office 365 Message Encryption Funktionen auf der Basis Azure Information Protection Ihrer Organisation verwendeten geschützten Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation per e-Mail. Die neuen Funktionen für OME arbeiten mit anderen Office 365-Organisationen, Outlook.com, Google Mail und anderen e-Mail-Dienste.
ms.openlocfilehash: c24b2f9b612b863217df8afd951424d1a89295c9
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955417"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen

Mit den neuen Funktionen von Office 365 Message Encryption (OME), die die Schutzfunktionen in Azure Information Protection nutzen, kann in Ihrer Organisation auf einfache Weise geschützte e-Mails mit jedem beliebigen Gerät freigeben. Benutzer können Nachrichten senden und empfangen geschützte mit anderen Office 365-Organisationen sowie nicht - Office 365-Kunden mit Outlook.com, Google Mail und anderen e-Mail-Dienste.
  
## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Erste Schritte mit OME mit der Aktivierung der Azure Rights Management, die Teil von Azure Information Protection

Es ist jetzt einfach Einstieg in die neuen OME-Funktionen. Ab Februar 2018 ermöglicht Office 365 automatisch die neuen OME-Funktionen für qualifizierte Organisationen in unseren Rechenzentren. Ihre Organisation ist berechtigt, wenn es eine neue Office 365-Mandanten ist und Ihre Organisation die entsprechenden Abonnements hat. **Wenn Sie Azure Rights Management (Azure RMS), Teil des Azure Information Protection, aktiviert haben, und klicken Sie dann wir Office 365 Message Encryption automatisch für Sie aktiviert.** Sie müssen keine andere Person zur OME aktivieren. Zum Aktivieren der Azure-Rechteverwaltung finden Sie unter [Aktivieren von Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Informationen zu Abonnements finden Sie unter "welche Abonnements muss ich verwenden Sie die neue OME Capabilities?" in [Office 365 Message Encryption – Häufig gestellte Fragen](ome-faq.md). Informationen zum Erwerben eines Abonnements für Azure Information Protection finden Sie unter [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).
  
Wenn Sie Exchange Online mit Active Directory-Rechteverwaltungsdienste-Dienst (AD RMS) verwenden, können Sie diese neuen Funktionen nicht sofort aktivieren. Stattdessen müssen Sie zuerst AD RMS zur Azure Information Protection migrieren. Wenn Sie die Migration abgeschlossen haben, können Sie diese Schritte ausgeführt haben.
  
Wenn Sie angeben, dass auch weiterhin mithilfe der lokale AD RMS mit Exchange Online anstelle der Migration zu Azure Information Protection nicht werden diese neuen Funktionen verwenden können.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Informationen zur Verwendung der neuen Funktionen für OME

Verwenden Sie die neuen Funktionen von Office 365 Message Encryption die Schutzfunktionen Azure Rights Management (Azure RMS), auch von Azure Information Protection aufgerufen. Dazu gehören Verschlüsselung, Identity und Autorisierung Richtlinien, um Ihre e-Mails zu schützen. Sie können mithilfe von Rights Management Vorlagen, die [nicht weiterleiten Option](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)und die [Option nur zum Verschlüsseln von](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)Nachrichten verschlüsseln. Benutzer können Sie e-Mail-Nachrichten sowie einer Reihe von Office 365 Anlagen mit diesen Optionen verschlüsseln. Eine vollständige Liste der Anlagen in unterstützten Typen finden Sie unter ["Dateitypen behandelt durch IRM-Richtlinien, wenn sie Nachrichten zugeordnet sind" in der Einführung von IRM für e-Mail-Nachrichten](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). Als Administrator können Sie auch e-Mail-Flussregeln zum Anwenden von diesem Schutz definieren. Beispielsweise können Sie eine Regel definieren, wobei alle ungeschützte Nachrichten, die an einen bestimmten Empfänger adressiert sind oder bestimmte Wörter in der Betreffzeile enthalten, sind vor nicht autorisiertem Zugriff geschützt und der Empfänger können nicht kopiert oder Drucken des Inhalts der Nachricht.
  
Anders als die vorherige Version des OME bieten diese neuen Funktionen eine einheitliche Absender Erfahrung, ob Sie e-Mail-Nachrichten innerhalb Ihrer Organisation oder an Empfänger außerhalb von Office 365 senden. Darüber hinaus Empfänger, die eine geschützte e-Mail-Nachricht, die mit Office 365-Konto in Outlook 2016 oder in Outlook im Web erhalten keine zusätzliche Aktionen, die Nachricht anzuzeigen. Er arbeitet nahtlos. Empfänger auch mithilfe von anderen e-Mail-Clients und e-Mail-Dienstanbieter haben eine verbesserte wünschen. Informationen finden Sie unter [Informationen zu geschützten Nachrichten in Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) und [wie kann ich eine geschützte Nachricht öffnen](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>So richten Sie die neuen Funktionen für OME manuell ein Schritte

Folgendermaßen Sie Wenn Ihre Organisation nicht automatisch OME aktiviert haben, oder Sie OME deaktiviert aktiviert, vor, So richten Sie die neuen Funktionen für OME manuell ein.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>So richten Sie die neuen Funktionen für OME manuell ein

1. Stellen Sie sicher, dass Sie für Ihre Organisation das richtige Abonnement verfügen. Informationen zu Abonnements, finden Sie unter "welche Abonnements muss ich verwenden Sie die neue OME Capabilities?" in der [Office 365 Message Encryption – Häufig gestellte Fragen.](ome-faq.md) Informationen zum Erwerben eines Abonnements für Azure Information Protection finden Sie unter [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).
    
2. Entscheiden Sie, ob Microsoft Verwalten des Stamm-Schlüssels zum Schutz der Azure-Daten (Standard) oder generiert und Verwalten dieser Schlüssel selbst (auch bekannt als eigene Taste oder BYOK schalten) werden sollen. Wenn Sie generieren und dieser Schlüssel zu verwalten möchten, müssen Sie einige Schritte vor dem Einrichten der neuen Funktionen für OME ausführen. Weitere Informationen finden Sie unter [Planung und Implementierung Ihrer mandantenschlüssel Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft empfiehlt, dass Sie diese Schritte ausführen, bevor Sie OME einrichten.
    
3. Aktivieren Sie die neuen Funktionen für OME mit der Aktivierung der Azure Rights Management. Anweisungen finden Sie unter [Aktivieren von Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Wenn Sie dies tun, die neuen Funktionen OME automatisch von Office 365 für Sie aktiviert.
    
    > [!TIP]
    > Outlook im Web speichert die Benutzeroberfläche, daher es ratsam ist, warten Sie einen Tag, bevor Sie versuchen, e-Mail-Nachrichten, die mithilfe dieser Client die neuen Funktionen für OME zuweisen. Bevor Sie die Benutzeroberfläche aktualisiert und der neue Konfiguration entsprechen, werden nicht die neuen Funktionen für OME verfügbar sein. Nachdem die Benutzeroberfläche aktualisiert werden, können Benutzer e-Mail-Nachrichten mithilfe der neuen Funktionen für OME schützen. 
  
4. (Optional) Einrichten von neuen e-Mail-Flussregeln, oder aktualisieren Sie vorhandene e-Mail-Flussregeln, die definieren, wie und wann Sie Office 365 zum Verschlüsseln von Nachrichten, die von Ihrer Organisation gesendet werden soll.
    
## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Stellen Sie sicher, dass die neuen Funktionen für OME ordnungsgemäß konfiguriert sind, mithilfe von Windows PowerShell

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihre Mandanten ordnungsgemäß konfiguriert ist, um die neuen Funktionen für OME über Exchange Online PowerShell verwenden.
  
1. Verwenden ein Arbeit oder Schule Konto, die in Office 365-Organisation über globaler Administrator-Berechtigungen verfügt, eine Windows PowerShell-Sitzung zu starten und eine Verbindung mit Exchange Online. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Führen Sie das Cmdlet "Test-IRMConfiguration" mithilfe der folgenden Syntax aus:
    
    ```Test-IRMConfiguration [-Sender <email address >]```  

   Beispiel:
    
    ```Test-IRMConfiguration -Sender securityadmin@contoso.com```

    Dabei ist e-Mail-Adresse die e-Mail-Adresse eines Benutzers in Office 365-Organisation. Während des optional, sofern eine e-Mail-Adresse des Absenders erzwingt, dass das System zusätzliche überprüft werden soll.
    
    Das Ergebnis sollte diese aussehen:
    
    ```
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

    Wobei *Contoso* durch den Namen des Office 365-Organisation ersetzt wird. 
    
    Die Namen der Standardvorlagen für in den Ergebnissen zurückgegeben können von denen in den oben genannten Ergebnissen abweichen.
    
    Eine Einführung in Formularvorlagen und Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zu den Do Not Forward option Option nur zu verschlüsseln, und wie zusätzliche Vorlagen oder finden Sie heraus, welche Rechte sind so erstellen Sie in eine vorhandene Vorlage enthalten, finden Sie unter [Konfigurieren von Nutzungsrechte für Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).
    
3. Führen Sie das Cmdlet Remove-PSSession So trennen Sie die Verwaltung von Informationsrechten-Dienst.
    
    ```Remove-PSSession $session```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Nächste Schritte: Definieren Sie die neue e-Mail-Flussregeln, die die neuen OME-Funktionen verwenden
<a name="Rules_1"> </a>

Dieser Schritt ist optional für neue OME-Bereitstellungen, jedoch dieser Schritt ist erforderlich für vorhandene OME-Bereitstellungen, die bereits für e-Mail-Flussregeln eingerichtet ausgehenden e-Mail-Nachrichten verschlüsseln. Wenn Sie die neuen OME-Funktionen nutzen möchten, müssen Sie Ihre vorhandenen e-Mail-Flussregeln aktualisieren. Andernfalls erhalten Ihre Benutzer weiterhin verschlüsselten e-Mail-Nachrichten, die das vorherige HTML-Anlagenformat anstelle der neuen, nahtlosen OME-Umgebung verwendet wird.
  
E-Mail-Flussregeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden soll, sowie die Bedingungen für die Verschlüsselung entfernen. Wenn Sie eine Aktion für eine Regel festlegen, werden alle Nachrichten, die die regelbedingungen entsprechen verschlüsselt, wenn sie gesendet werden.
  
Weitere Informationen zu e-Mail-Flussregeln finden Sie unter [Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Verwandte Themen
<a name="Rules_1"> </a>

[Senden Sie, zeigen Sie an und beantworten Sie verschlüsselter Nachrichten in Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
  
[Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md)
  


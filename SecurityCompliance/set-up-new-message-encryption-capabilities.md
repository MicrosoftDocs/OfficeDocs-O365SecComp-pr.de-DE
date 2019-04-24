---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Neue Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren, kann Ihre Organisation geschützte e-Mail-Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation verwenden. Die neuen OM-Funktionen funktionieren mit anderen Office 365-Organisationen, Outlook.com, Gmail und anderen e-Mail-Diensten.
ms.openlocfilehash: ea8756d08b1c172c433d6cd8ad1752c4c7ad64e9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260753"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen

Mit den neuen Funktionen von Office 365 Message Encryption (OM) können Organisationen geschützte e-Mails für alle Benutzer auf einem beliebigen Gerät freigeben. Benutzer können geschützte Nachrichten mit anderen Office 365-Organisationen und nicht-Office 365-Kunden mithilfe von Outlook.com, Gmail und anderen e-Mail-Diensten austauschen.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und IT-Experten. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die neuen OM-Funktionen in Ihrer Office 365-Organisation verfügbar sind.

## <a name="verify-that-azure-rights-management-is-active"></a>Überprüfen, ob die Azure-Rechteverwaltung aktiv ist

Die neuen OM-Funktionen nutzen die Schutzfunktionen in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), die von [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) zum Schutz von e-Mails und Dokumenten über Verschlüsselung und Zugriffssteuerung verwendet werden.

Die einzige Voraussetzung für die Verwendung der neuen OM-Funktionen besteht darin, dass die [Azure-Rechteverwaltung](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) im Mandanten Ihrer Organisation aktiviert werden muss. Wenn dies der Fall ist, aktiviert Office 365 die neuen OM-Funktionen automatisch, und Sie müssen nichts tun.

Azure RMS wird auch automatisch für die meisten berechtigten Pläne aktiviert, daher müssen Sie in dieser Hinsicht möglicherweise keine weiteren Schritte ausführen. Weitere Informationen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .

>[!IMPORTANT]
>Wenn Sie Active Directory-Rechteverwaltungsdienst (AD RMS) mit Exchange Online verwenden, müssen Sie [zu Azure Information Protection migrieren](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , bevor Sie die neuen OM-Funktionen verwenden können. OM ist nicht mit AD RMS kompatibel.  

Weitere Informationen finden Sie unter:

- [Welche Abonnements benötige ich, um die neuen OM-Funktionen verwenden zu können?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) So überprüfen Sie, ob Ihr Abonnementplan Azure Information Protection (einschließlich Azure RMS-Funktionalität) enthält.
- [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) für Informationen zum Erwerb eines berechtigten Abonnements.  

### <a name="manually-activating-azure-rights-management"></a>Manuelles Aktivieren der Azure-Rechteverwaltung

Wenn Sie Azure RMS deaktiviert haben oder wenn es aus irgendeinem Grund nicht automatisch aktiviert wurde, können Sie es manuell im folgenden aktivieren:

- **Office 365 Admin Center**: Informationen zum [Aktivieren der Azure-Rechteverwaltung im Office 365 Admin Center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .
- **Azure-Portal**: Informationen zum [Aktivieren der Azure-Rechteverwaltung aus dem Azure-Portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) .

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Konfigurieren der Verwaltung Ihres Azure Information Protection-Mandanten Schlüssels

Der folgende Schritt ist optional. Microsoft die Verwaltung des Stammschlüssels für Azure Information Protection ist die Standardeinstellung und empfohlene bewährte Methode für die meisten Office 365-Mandanten. Wenn dies der Fall ist, müssen Sie nichts tun.

Es gibt viele Gründe, beispielsweise Compliance-Anforderungen, die dazu führen können, dass Sie Ihren eigenen Stammschlüssel generieren und verwalten (auch bekannt als bringen Sie Ihren eigenen Schlüssel (BYOK)). Wenn dies der Fall ist, empfehlen wir, dass Sie die erforderlichen Schritte ausführen, bevor Sie die neuen OM-Funktionen einrichten. Weitere Informationen finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Überprüfen der neuen OM-Konfiguration in Exchange Online PowerShell

Sie können überprüfen, ob Ihr Office 365-Mandant ordnungsgemäß für die Verwendung der neuen OM-Funktionen in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)konfiguriert ist.
  
1. Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.

2. Führen Sie das Cmdlet Get-IRMConfiguration aus.

     Für den AzureRMSEnabled-Parameter sollte der Wert $True angezeigt werden, der angibt, dass om in Ihrem Mandanten konfiguriert ist. Wenn dies nicht der Fall ist, verwenden Sie Set-IRMConfiguration, um den Wert von AzureRMSEnabled auf $True festzulegen, um OM zu aktivieren.

3. Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Beispiel**:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - Das Bereitstelleneiner Absender-e-Mail ist optional, zwingt das System jedoch, zusätzliche Prüfungen durchzuführen. Verwenden Sie die e-Mail-Adresse eines beliebigen Benutzers in Ihrem Office 365-Mandanten.

     Ihre Ergebnisse sollten wie folgt aussehen:

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

   - Der Name Ihrer Office 365-Organisation ersetzt *contoso*.

   - Die Standardvorlagen Namen können sich von den oben dargestellten unterscheiden. Weitere Informationen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .

4. Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rechteverwaltungsdienst zu trennen.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Nächste Schritte: Definieren von Nachrichtenfluss Regeln zur Verwendung neuer OM-Funktionen

Wenn zuvor konfigurierte e-Mail-Flussregeln zum Verschlüsseln von e-Mails in Ihrer Office 365-Organisation konfiguriert sind, müssen Sie die vorhandenen Regeln aktualisieren, um die neuen OM-Funktionen zu verwenden. Für neue Bereitstellungen müssen Sie neue Nachrichtenfluss Regeln erstellen.

>[!IMPORTANT]
>Wenn Sie keine vorhandenen Nachrichtenfluss Regeln aktualisieren, erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat verwenden, anstelle der neuen nahtlosen OM-Umgebung.

Nachrichtenfluss Regeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden sollen, sowie Bedingungen zum Entfernen dieser Verschlüsselung. Wenn Sie eine Aktion für eine Regel festlegen, werden alle Nachrichten, die den Regelbedingungen entsprechen, beim Senden verschlüsselt.
  
Schritte zum Erstellen von Nachrichtenfluss Regeln für OM finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

So aktualisieren Sie vorhandene Regeln, um die neuen OM-Funktionen zu verwenden:

1. Wechseln Sie im Office 365 Admin Center zu **Admin Center _GT_ Exchange**.
2. Wechseln Sie im Exchange Admin Center zu **Nachrichtenfluss-_GT_-Regeln**.
3. **Führen Sie**für jede Regel Folgendes aus:
    - Wählen Sie **Nachrichtensicherheit ändern**aus.
    - Wählen Sie **Office 365-Nachrichtenverschlüsselung und-Rechte Schutz anwenden**aus.
    - Wählen Sie in der Liste eine RMS-Vorlage aus.
    - Klicken Sie auf **Speichern**.
    - Wählen Sie **OK** aus.

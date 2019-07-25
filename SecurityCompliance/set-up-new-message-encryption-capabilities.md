---
title: Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Neue Office 365 Nachrichten Verschlüsselungsfunktionen, die auf dem Schutz von Azure Information basieren, kann Ihre Organisation geschützte e-Mail-Kommunikation mit Personen innerhalb und außerhalb Ihrer Organisation verwenden. Die neuen OM-Funktionen funktionieren mit anderen Office 365 Organisationen, Outlook.com, Gmail und anderen e-Mail-Diensten.
ms.openlocfilehash: 835b1d6f40868684536dbea8f75dab0665950210
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854799"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen

Die neuen Funktionen für die Office 365 Nachrichtenverschlüsselung (OM) ermöglichen es Organisationen, geschützte e-Mails für alle Benutzer auf jedem Gerät freizugeben. Benutzer können geschützte Nachrichten mit anderen Office 365-Organisationen sowie nicht-Office 365-Kunden mit Outlook.com, Gmail und anderen e-Mail-Diensten austauschen.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln über Office 365 Nachrichtenverschlüsselung. Dieser Artikel richtet sich an Administratoren und IT-Experten. Wenn Sie nur auf der Suche nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht sind, lesen Sie die Artikelliste in [Office 365 Nachrichtenverschlüsselung (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die neuen OM-Funktionen in Ihrer Office 365 Organisation zur Verfügung stehen.

## <a name="verify-that-azure-rights-management-is-active"></a>Überprüfen, ob Azure Rights Management aktiv ist

Die neuen OM-Funktionen nutzen die Schutzfunktionen in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), die von [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) verwendete Technologie zum Schutz von e-Mails und Dokumenten über Verschlüsselung und Zugriffssteuerung.

Die einzige Voraussetzung für die Verwendung der neuen OM-Funktionen besteht darin, dass die [Azure-Rechteverwaltung](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) im Mandanten Ihrer Organisation aktiviert werden muss. Wenn dies der Fall ist, aktiviert Office 365 die neuen OM-Funktionen automatisch, und Sie müssen nichts tun.

Azure RMS wird auch automatisch für die meisten berechtigten Pläne aktiviert, daher müssen Sie in diesem Zusammenhang möglicherweise auch nichts tun. Weitere Informationen finden Sie unter [Aktivieren von Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .

>[!IMPORTANT]
>Wenn Sie Active Directory Rights Management Service (AD RMS) mit Exchange Online verwenden, müssen Sie [zu Azure Information Protection migrieren](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , bevor Sie die neuen OM-Funktionen verwenden können. OM ist nicht mit AD RMS kompatibel.  

Weitere Informationen finden Sie unter:

- [Welche Abonnements benötige ich für die Verwendung der neuen OM-Funktionen?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) So überprüfen Sie, ob Ihr Abonnementplan Azure Information Protection umfasst (einschließlich Azure RMS-Funktionalität).
- [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) für Informationen zum Erwerb eines berechtigten Abonnements.  

### <a name="manually-activating-azure-rights-management"></a>Manuelles Aktivieren von Azure Rights Management

Wenn Sie Azure RMS deaktiviert haben oder es aus irgendeinem Grund nicht automatisch aktiviert wurde, können Sie es manuell im folgenden aktivieren:

- **Microsoft 365 Admin Center**: Informationen zum [Aktivieren von Azure Rights Management aus dem Admin Center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) finden Sie unter Anweisungen.
- **Azure-Portal**: Weitere Informationen finden Sie unter [Aktivieren von Azure Rights Management aus dem Azure-Portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) .

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Konfigurieren der Verwaltung Ihres Azure Information Protection-Mandanten Schlüssels

Der folgende Schritt ist optional. Microsoft die Verwaltung des Stammschlüssels für Azure Information Protection zu ermöglichen, ist die Standardeinstellung und empfohlene bewährte Methode für die meisten Office 365 Mandanten. Wenn dies der Fall ist, müssen Sie nichts tun.

Es gibt viele Gründe, beispielsweise Compliance-Anforderungen, die Sie zum Generieren und Verwalten Ihres eigenen Stammschlüssels (auch bekannt als Bring your own Key (BYOK)) erfordern. Wenn dies der Fall ist, wird empfohlen, dass Sie die erforderlichen Schritte ausführen, bevor Sie die neuen OM-Funktionen einrichten. Weitere Informationen finden Sie unter [Planen und Implementieren Ihres Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Überprüfen der neuen OM-Konfiguration in Exchange Online PowerShell

Sie können überprüfen, ob der Office 365 Mandant ordnungsgemäß für die Verwendung der neuen OM-Funktionen in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)konfiguriert ist.
  
1. Stellen Sie eine [Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) mithilfe eines Kontos mit globalen Administratorberechtigungen in Ihrem Office 365-Mandanten her.

2. Führen Sie das Cmdlet Get-IRMConfiguration aus.

     Für den AzureRMSLicensingEnabled-Parameter sollte der Wert $true angezeigt werden, der angibt, dass om in Ihrem Mandanten konfiguriert ist. Wenn dies nicht der Fall ist, verwenden Sie IRMConfiguration, um den Wert von AzureRMSLicensingEnabled auf $true festzulegen, um OM zu aktivieren.

3. Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Beispiel**:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - Das Bereitstelleneiner Absender-e-Mail ist optional, zwingt das System jedoch, zusätzliche Prüfungen durchzuführen. Verwenden Sie die e-Mail-Adresse eines beliebigen Benutzers in Ihrem Office 365 Mandanten.

     Die Ergebnisse sollten etwa wie folgt aussehen:

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

   - Der Name Ihrer Office 365 Organisation wird *contoso*ersetzen.

   - Die Standardvorlagen Namen unterscheiden sich möglicherweise von den oben angezeigten. Weitere Informationen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .

4. Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rights Management-Dienst zu trennen.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Nächste Schritte: Definieren von Nachrichtenfluss Regeln für die Verwendung neuer OM-Funktionen

Wenn zuvor konfigurierte Nachrichtenfluss Regeln zum Verschlüsseln von e-Mails in Ihrer Office 365 Organisation konfiguriert sind, müssen Sie die vorhandenen Regeln aktualisieren, um die neuen OM-Funktionen zu verwenden. Für neue Bereitstellungen müssen Sie neue Nachrichtenfluss Regeln erstellen.

>[!IMPORTANT]
>Wenn Sie vorhandene Nachrichtenfluss Regeln nicht aktualisieren, erhalten die Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat verwenden, statt das neue nahtlose OM-Erlebnis.

Nachrichtenfluss Regeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden sollen, sowie Bedingungen für das Entfernen dieser Verschlüsselung. Wenn Sie eine Aktion für eine Regel festlegen, werden alle Nachrichten, die mit den Regelbedingungen übereinstimmen, verschlüsselt, wenn Sie gesendet werden.
  
Schritte zum Erstellen von Nachrichtenfluss Regeln für OM finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

So aktualisieren Sie vorhandene Regeln für die Verwendung der neuen OM-Funktionen:

1. Wechseln Sie im Microsoft 365 Admin Center zu **Admin Centers #a0 Exchange**.
2. Wechseln Sie im Exchange Admin Center zu **Nachrichtenfluss #a0 Regeln**.
3. **Geben Sie**für jede Regel Folgendes ein:
    - Wählen Sie **die Option Nachrichtensicherheit ändern**aus.
    - Wählen Sie **Office 365 Nachrichtenverschlüsselung und Rechte Schutz anwenden**aus.
    - Wählen Sie in der Liste eine RMS-Vorlage aus.
    - Klicken Sie auf **Speichern**.
    - Wählen Sie **OK** aus.

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
ms.openlocfilehash: 90247a7e3cd7e5978eb144a2b6f66a9de21a8f96
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296188"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Einrichten neuer Office 365-Nachrichtenverschlüsselungsfunktionen

Mit den neuen Funktionen von Office 365 Message Encryption (OM) können Organisationen geschützte e-Mails für alle Benutzer auf einem beliebigen Gerät freigeben. Benutzer können geschützte Nachrichten mit anderen Office 365-Organisationen und nicht-Office 365-Kunden mithilfe von Outlook.com, Gmail und anderen e-Mail-Diensten austauschen.


>[!NOTE]
>Dieser Artikel richtet sich an Administratoren und IT-Experten. Wenn Sie ein Endbenutzer sind, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) für entsprechende Lösungen.

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die neuen OM-Funktionen in Ihrem Office 365-Mandanten verfügbar sind. 

## <a name="verify-azure-rights-management-arm-is-active"></a>Überprüfen der Azure-Rechteverwaltung (ARM) ist aktiv

>[!NOTE]
>Die neuen OM-Funktionen nutzen die Schutzfunktionen von [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), die von [Azure Rights Management (Arm)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms)verwendet werden.

Die einzige Voraussetzung für die Verwendung der neuen OM-Funktionen ist, dass [Azure Rights Management (Arm)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) in ihrem Office 365-Mandanten aktiviert werden muss. Wenn dies der Fall ist, aktiviert Office 365 die neuen OM-Funktionen automatisch, und Sie müssen nichts tun. 

Der ARM wird auch automatisch für die meisten berechtigten Pläne aktiviert, daher müssen Sie in dieser Hinsicht möglicherweise nichts Unternehmen. Weitere Informationen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .

>[!IMPORTANT]
>Wenn Sie Active Directory-Rechteverwaltungsdienst (AD RMS) mit Exchange Online verwenden, müssen Sie [zu Azure Information Protection migrieren](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , bevor Sie die neuen OM-Funktionen verwenden können. AD RMS ist nicht kompatibel mit ARM.  

Weitere Informationen finden Sie unter:

- [Welche Abonnements benötige ich, um die neuen OM-Funktionen verwenden zu können?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) um zu überprüfen, ob Ihr Abonnementplan Azure Information Protection (einschließlich ARM) enthält.   
-  [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) für Informationen zum Erwerb eines berechtigten Abonnements.  

### <a name="manually-activating-arm"></a>Manuelles Aktivieren des Arms

Wenn Sie den ARM deaktiviert haben oder er aus irgendeinem Grund nicht automatisch aktiviert wurde, können Sie ihn manuell im folgenden aktivieren:

- **Office 365 Admin Center**: Weitere Informationen finden Sie unter [How to Activate Azure Rights Management from the Office 365 Admin Center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions
- **Azure-Portal**: Informationen zum [Aktivieren der Azure-Rechteverwaltung aus dem Azure-Portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) . 


## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Konfigurieren der Verwaltung Ihres Azure Information Protection-Mandanten Schlüssels

Dies ist ein optionaler Schritt. Microsoft die Verwaltung des Stammschlüssels für Azure Information Protection ist die Standardeinstellung und empfohlene bewährte Methode für die meisten Office 365-Mandanten. Wenn dies der Fall ist, müssen Sie nichts tun. 

Es gibt viele Gründe, beispielsweise Compliance-Anforderungen, die dazu führen können, dass Sie Ihren eigenen Stammschlüssel generieren und verwalten (auch bekannt als bringen Sie Ihren eigenen Schlüssel (BYOK)). Wenn dies der Fall ist, empfehlen wir, dass Sie die erforderlichen Schritte ausführen, bevor Sie die neuen OM-Funktionen einrichten. Weitere Informationen finden Sie unter [Planen und Implementieren des Azure Information Protection-Mandanten Schlüssels](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) . 


## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Überprüfen der neuen OM-Konfiguration in Exchange Online PowerShell

Sie können überprüfen, ob Ihr Office 365-Mandant ordnungsgemäß für die Verwendung der neuen OM-Funktionen in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)konfiguriert ist.
  
1. Stellen Sie eine [Verbindung mit Exchange Online PowerShell her,](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) indem Sie ein Konto mit globalen Administratorberechtigungen in ihrem Office 365-Mandanten verwenden.

2. Führen Sie das Cmdlet Test-IRMConfiguration mit der folgenden Syntax aus:

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

3. Führen Sie das Cmdlet Remove-PSSession aus, um die Verbindung mit dem Rechteverwaltungsdienst zu trennen.
    
     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a>Aktualisieren von Nachrichtenfluss Regeln zur Verwendung neuer OM-Funktionen

Wenn zuvor konfigurierte e- [Mail-Flussregeln zum](define-mail-flow-rules-to-encrypt-email.md) Verschlüsseln von e-Mails in ihrem Office 365-Mandanten konfiguriert sind, müssen Sie diese vorhandenen Regeln aktualisieren, um die neuen OM-Funktionen zu verwenden. Bei neuen Bereitstellungen ist dieser Schritt zu diesem Zeitpunkt nicht erforderlich.   

>[!Note]
>Nachrichtenfluss Regeln definieren die Bedingungen, unter denen e-Mail-Nachrichten verschlüsselt werden, und wann die Verschlüsselung entfernt werden soll. Weitere Informationen finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md) .

So aktualisieren Sie vorhandene Regeln, um die neuen OM-Funktionen zu verwenden:

1. Wechseln Sie im Office 365 Admin Center zu **Admin Center _GT_ Exchange**.

2. Wechseln Sie im Exchange Admin Center zu **Nachrichtenfluss-_GT_-Regeln**. 
3. **Führen Sie**für jede Regel Folgendes aus:
    - Wählen Sie **Nachrichtensicherheit ändern**aus.
    - Wählen Sie **Office 365-Nachrichtenverschlüsselung und-Rechte Schutz anwenden**aus.
    - Auswählen einer RMS-Vorlage aus der Liste
    - Wählen Sie **Speichern** aus.
    - Wählen Sie **OK** aus.
  
>[!IMPORTANT]
>Wenn Sie keine vorhandenen Nachrichtenfluss Regeln aktualisieren, erhalten Ihre Benutzer weiterhin verschlüsselte e-Mails, die das vorherige HTML-Anlagenformat verwenden, anstelle der neuen OM-Funktionen.

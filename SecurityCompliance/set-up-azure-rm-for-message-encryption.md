---
title: Einrichten der Azure-Rechteverwaltung für Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: 'Office 365 Message Encryption hängt von Microsoft Azure Rights Management (zuvor bekannt als Windows Azure Active Directory Rights Management). '
ms.openlocfilehash: 99c8de49330cf99545d28d81e0c99c2138797356
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529501"
---
# <a name="set-up-azure-rights-management-for-office-365-message-encryption"></a>Einrichten der Azure-Rechteverwaltung für Office 365-Nachrichtenverschlüsselung

In diesem Thema werden die Schritte, die Sie benötigen, denen Sie folgen, um aktivieren, und legen Sie dann von Azure Rights Management (RMS), Teil des Azure Information Protection, für die Verwendung mit Office 365 Message Encryption (OME).
  
## <a name="prerequisites-for-using-office-365-message-encryption"></a>Voraussetzungen für die Verwendung der Office 365-Nachrichtenverschlüsselung
<a name="warmprereqs"> </a>

Office 365 Message Encryption (OME), einschließlich IRM, hängt von Azure-Rechteverwaltung (RMS Azure). Azure RMS ist die Protection-Technologie von Azure Information Protection verwendet. Um OME verwenden zu können, muss Office 365-Organisation ein Exchange Online oder Exchange Online Protection-Abonnement enthalten, die wiederum eine Azure Rights Management Abonnement enthält.
  
- Wenn Sie nicht sicher was Ihr Abonnement umfasst sind, finden Sie in der Exchange Online-dienstbeschreibungen für [Nachrichtenrichtlinien, Wiederherstellung und Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).
    
- Wenn Sie nicht über die ein RMS Azure-Abonnement für Exchange Online oder Exchange Online Protection verfügen, müssen Sie ein Abonnement erwerben und zuerst zu aktivieren.
    
    Informationen zum Erwerb von ein Abonnement für Azure Rights Management finden Sie unter [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). Im nächste Abschnitt erhalten Sie Informationen zum Aktivieren von Azure Rights Management.
    
- Wenn Ihnen Azure Rights Management, aber nicht für Exchange Online oder Exchange Online Protection eingerichtet, wird in diesem Artikel erläutert, wie Azure Rights Management aktivieren und dann die beschreibt der besten Möglichkeit zum Einrichten OME Azure Rights Management entwickelt.
    
- Wenn Sie bereits OME eingerichtet haben, arbeiten mit Azure-Rechteverwaltung für Exchange Online oder Exchange Online Protection, je nachdem, wie Sie es, einrichten möglicherweise Sie beginnen, OME und neuen Features sofort nutzen. In diesem Artikel wird erläutert, wie Sie ermitteln, ob Sie OME ordnungsgemäß eingerichtet haben, wie Sie vorgehen, wenn Sie das Setup ändern müssen und was geschieht, wenn Sie nicht die Installation zu ändern. Um die neuen Funktionen verwenden, müssen Sie beispielsweise Azure RMS mit OME verwenden. Sie können nicht mit einer lokalen Active Directory-RMS die neuen Funktionen verwenden.
    
## <a name="activate-azure-rights-management-for-ome-in-office-365"></a>Aktivieren der Azure-Rechteverwaltung für OME in Office 365
<a name="activatewarm"> </a>

Sie müssen Azure Rights Management aktivieren, damit die Benutzer in Ihrer Organisation gelten Schutz von Informationen für Nachrichten, die sie senden können, und Öffnen von Nachrichten und Dateien, die vom Dienst Azure-Rechteverwaltung geschützt sind. Anweisungen finden Sie unter [Aktivieren von Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Nachdem Sie die Aktivierung abgeschlossen haben, wird dieser Seite zurückkehren, und die Aufgaben in diesem Artikel fort.
  
## <a name="set-up-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Richten Sie OME Azure RMS durch Vertrauenswürdige Veröffentlichungsdomänen (Vertrauenswürdige Veröffentlichungsdomänen) importieren
<a name="importTPDs"> </a>

Eine vertrauenswürdige Veröffentlichungsdomäne ist eine XML-Datei, die Informationen zu Ihrer Organisation Rights Management Einstellungen enthält. Beispielsweise der TPD enthält Informationen über das lizenzgebende Serverzertifikat (SLC) zum Signieren und Verschlüsseln von Zertifikaten und Lizenzen, die URLs für Lizenzierung und Veröffentlichung verwendet, und so weiter. Importieren Sie die vertrauenswürdige Veröffentlichungsdomäne in Office 365-Organisation, mithilfe von Windows PowerShell.
  
> [!IMPORTANT]
> In früheren Versionen können Sie auswählen, um Vertrauenswürdige Veröffentlichungsdomänen aus dem Active Directory-Rechteverwaltungsdienste-Dienst (AD RMS) in Office 365-Organisation zu importieren. Jedoch auf diese Weise und verhindert, dass Sie die neuen Funktionen von OME wird nicht empfohlen. Wenn Ihre Office 365-Organisation derzeit ist auf diese Weise konfiguriert haben, empfiehlt es sich, dass Sie einen Plan zum Migrieren von Ihrer lokalen Active Directory-RMS zu Cloud-basierten Azure Information Protection erstellen. Weitere Informationen finden Sie unter [Migrieren von AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Sie werden nicht die neuen OME-Funktionen verwenden, bevor Sie die Migration zu Azure Information Protection abgeschlossen haben. 
  
 **So importieren Sie Vertrauenswürdige Veröffentlichungsdomänen von Azure RMS**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Wählen Sie die Key-sharing-URL, die Ihre Office 365-Organisation geografischen Standort entspricht:
    
|**Standort**|**Key-sharing-URL des Speicherorts**|
|:-----|:-----|
|Nordamerika  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Europäische Union  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Asien  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Südamerika  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 für Behörden (Community-Cloud der US-Regierung)  <br/> Diesen RMS-Key-sharing-Speicherort ist für Kunden vorgesehen, die Office 365 für Behörden SKUs erworben haben.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Konfigurieren Sie den Key-sharing-Speicherort, indem Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) wie folgt ausführen: 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Wenn Sie beispielsweise die Key-sharing-Location Ihrer Organisation befindet sich in Nordamerika zu konfigurieren:
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Führen Sie das Cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) , mit der Option - RMSOnline für den import der TPD aus Azure Rights Management: 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Wobei *TPDName* der Name ist, die Sie für die vertrauenswürdige Veröffentlichungsdomäne verwenden möchten. Beispielsweise "Contoso TPD Nordamerika". 
    
5. Führen Sie das Cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) um zu überprüfen, dass die Verwendung des Diensts Azure Rights Management zum Office 365-Organisation erfolgreich, wie folgt mit der Option - RMSOnline fest: 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Dieses Cmdlet unter anderem überprüft die Konnektivität mit dem Dienst Azure Rights Management, downloads der TPD und ihre Gültigkeit überprüft.
    
6. Führen Sie das [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) -Cmdlet wie folgt zum Deaktivieren von Azure Rights Management-Vorlagen werden in Outlook im Web und Outlook zur Verfügung: 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt, um Azure-Rechteverwaltung für Ihre Cloud-basierte e-Mail-Organisation aktivieren und Konfigurieren der Verwendung der Azure-Rechteverwaltung für Office 365 Message Encryption aus: 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Um sicherzustellen, dass Sie erfolgreich der TPD importiert und Azure Rights Management aktiviert haben, verwenden Sie das Cmdlet Test-IRMConfiguration, um Azure Rights Management-Funktionen zu testen. Weitere Informationen hierzu finden Sie unter "Beispiel 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>Ich habe OME mit Active Directory-Rechteverwaltungsdienste nicht Azure Information Protection eingerichtet, was kann ich tun?
<a name="importTPDs"> </a>

Sie können auch weiterhin Ihre vorhandenen Office 365 Message Encryption Mail Flow Regeln mit Active Directory Rights Management verwenden, aber Sie nicht konfigurieren oder verwenden Sie die neuen OME-Funktionen. Stattdessen müssen Sie auf Azure Information Protection migrieren. Informationen zur Migration und für Ihre Organisation Dies bedeutet finden Sie unter [Migrieren von AD RMS auf Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Nächste Schritte
<a name="importTPDs"> </a>

Wenn Sie Azure Rights Management-Setup abgeschlossen haben, sollten Sie die neuen OME-Funktionen zu aktivieren, finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
Nachdem Sie Ihre Organisation zum Verwenden der neuen OME-Funktionen eingerichtet haben, können Sie zum [Definieren von e-Mail-Flussregeln zum Schutz von e-Mail-Nachrichten mit neuen OME-Funktionen](define-mail-flow-rules-to-encrypt-email.md)bereit.
  
## <a name="related-topics"></a>Verwandte Themen
<a name="importTPDs"> </a>

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Referenz Details über die Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Was ist Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  


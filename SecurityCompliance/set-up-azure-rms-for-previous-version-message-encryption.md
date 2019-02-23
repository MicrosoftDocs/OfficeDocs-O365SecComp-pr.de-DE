---
title: Einrichten von Azure Rights Management für die vorherige Version der Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Die frühere Version der Office 365-Nachrichtenverschlüsselung hängt von der Microsoft Azure Rights Management (früher als Windows Azure Active Directory Rights Management bezeichnet) ab.
ms.openlocfilehash: 89b86035f57699457c86fefb49888b8428f4e01c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214375"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a>Einrichten von Azure Rights Management für die vorherige Version der Office 365-Nachrichtenverschlüsselung

In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um die Azure Rights Management (RMS), ein Teil von Azure Information Protection, für die Verwendung mit der vorherigen Version von Office 365 Message Encryption (OM) zu aktivieren und anschließend einzurichten.

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a>Dieser Artikel bezieht sich nur auf die frühere Version von OM.
Wenn Sie Ihre Office 365-Organisation noch nicht in die neuen OM-Funktionen verschoben haben, aber bereits OM bereitgestellt haben, beziehen sich die Informationen in diesem Artikel auf Ihre Organisation. Microsoft empfiehlt, einen Plan für die Umstellung auf die neuen Funktionen von OM zu erstellen, sobald es für Ihre Organisation sinnvoll ist. Weitere Informationen finden Sie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md). Wenn Sie mehr über die Funktionsweise der neuen Funktionen erfahren möchten, lesen Sie [Office 365-Nachrichtenverschlüsselung](ome.md). Der Rest dieses Artikels bezieht sich auf das Verhalten von OM vor der Freigabe der neuen OM-Funktionen.

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a>VoraussetZungen für die Verwendung der vorherigen Version von Office 365 Nachrichtenverschlüsselung
<a name="warmprereqs"> </a>

Office 365 Nachrichtenverschlüsselung (OM), einschließlich IRM, hängt von Azure Rights Management (Azure RMS) ab. Azure RMS ist die Schutztechnologie, die von Azure Information Protection verwendet wird. Zur Verwendung von OM muss Ihre Office 365-Organisation ein Exchange Online-oder Exchange Online Protection-Abonnement enthalten, das wiederum ein Azure Rights Management-Abonnement enthält.
  
- Wenn Sie nicht sicher sind, was Ihr Abonnement enthält, finden Sie in den Exchange Online-Dienstbeschreibungen für [Nachrichtenrichtlinien, Wiederherstellung und Kompatibilität](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).

- Wenn Sie nicht über ein Azure RMS-Abonnement für Exchange Online oder Exchange Online Protection verfügen, müssen Sie ein Abonnement erwerben und es zuerst aktivieren.

    Informationen zum Erwerb eines Abonnements für die Azure-Rechteverwaltung finden Sie unter [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). Im nächsten Abschnitt erhalten Sie Informationen zum Aktivieren der Azure-Rechteverwaltung.

- Wenn Sie über Azure Rights Management verfügen, es aber nicht für Exchange Online oder Exchange Online Protection eingerichtet ist, wird in diesem Artikel erläutert, wie Sie die Azure-Rechteverwaltung aktivieren und dann die beste Möglichkeit zum Einrichten von OM für die Verwendung der Azure-Rechteverwaltung.

- Wenn Sie bereits OM für die Zusammenarbeit mit Azure Rights Management für Exchange Online oder Exchange Online Protection eingerichtet haben, können Sie, je nachdem, wie Sie es einrichten, möglicherweise sofort mit der Verwendung von OM und den neuen Funktionen beginnen. In diesem Artikel wird erläutert, wie Sie feststellen, ob Sie "OM" ordnungsgemäß eingerichtet haben, was Sie tun müssen, wenn Sie das Setup ändern möchten und was passiert, wenn Sie das Setup nicht ändern möchten. Um die neuen Funktionen verwenden zu können, müssen Sie beispielsweise Azure RMS mit OM verwenden. Die neuen Funktionen können nicht mit einem lokalen Active Directory-RMS verwendet werden.

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a>Aktivieren der Azure-Rechteverwaltung für die frühere Version von om in Office 365

Sie müssen die Azure-Rechteverwaltung aktivieren, damit die Benutzer in Ihrer Organisation den Informationsschutz auf Nachrichten anwenden können, die Sie senden, sowie Nachrichten und Dateien öffnen, die durch den Azure Rights Management-Dienst geschützt wurden. Anweisungen finden Sie unter [Aktivieren der Azure-Rechteverwaltung](https://go.microsoft.com/fwlink/p/?LinkId=525775). Nachdem Sie die Aktivierung abgeschlossen haben, kehren Sie hierhin zurück, und fahren Sie mit den Aufgaben in diesem Artikel fort.
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Einrichten der vorherigen Version von OM zur Verwendung von Azure RMS durch Importieren von vertrauenswürdigen Veröffentlichungsdomänen (vor)

Ein TPD ist eine XML-Datei, die Informationen zu den Einstellungen für die Rechteverwaltung Ihrer Organisation enthält. Beispielsweise enthält das TPD Informationen zum Server-Lizenzgeberzertifikat (SLC), das zum Signieren und Verschlüsseln von Zertifikaten und Lizenzen verwendet wird, zu den URLs, die für die Lizenzierung und Veröffentlichung verwendet werden usw. Sie importieren das TPD mithilfe von Windows PowerShell in Ihre Office 365-Organisation.
  
> [!IMPORTANT]
> Zuvor konnten Sie vor aus dem Active Directory-Rechteverwaltungsdienst (AD RMS) in Ihre Office 365-Organisation importieren. Dies verhindert jedoch, dass Sie die neuen OM-Funktionen verwenden und wird nicht empfohlen. Wenn Ihre Office 365-Organisation auf diese Weise konfiguriert ist, empfiehlt Microsoft, einen Plan für die Migration von Ihrem lokalen Active Directory-RMS zu Cloud-basierten Azure Information Protection zu erstellen. Weitere Informationen finden Sie unter [Migrieren von AD RMS zu Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Sie können die neuen OM-Funktionen erst verwenden, nachdem Sie die Migration zu Azure Information Protection abgeschlossen haben.
  
 **So importieren Sie vor aus Azure RMS**
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Wählen Sie die URL für die Schlüssel Freigabe aus, die dem geografischen Standort Ihrer Office 365-Organisation entspricht:

|**Standort**|**URL für die Schlüssel Freigabeadresse**|
|:-----|:-----|
|Nordamerika  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Europäische Union  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Asien  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Südamerika  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 für Behörden (Community-Cloud der US-Regierung)  <br/> Dieser RMS-Freigabespeicherort ist für Kunden reserviert, die Office 365 für staatliche SKUs erworben haben.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Konfigurieren Sie den Speicherort für die Schlüssel Freigabe, indem Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) wie folgt ausführen: 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Beispielsweise können Sie den Speicherort für die Schlüssel Freigabe konfigurieren, wenn sich Ihre Organisation in Nordamerika befindet:
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Führen Sie das Cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) mit der Option-RMSOnline aus, um das TPD aus der Azure-Rechteverwaltung zu importieren: 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Dabei ist *TPDName* der Name, den Sie für die TPD verwenden möchten. Beispiel: "Contoso North American TPD". 
    
5. Führen Sie das Cmdlet [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) mit der Option-RMSOnline wie folgt aus, um zu überprüfen, ob die Office 365-Organisation erfolgreich für die Verwendung des Azure Rights Management-Diensts konfiguriert wurde: 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Unter anderem prüft dieses Cmdlet die Konnektivität mit dem Azure-Rechteverwaltungsdienst, lädt das TPD herunter und überprüft die Gültigkeit.
    
6. Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt aus, um die Verfügbarkeit von Azure Rights Management-Vorlagen in Outlook im Web und Outlook zu deaktivieren: 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Führen Sie das Cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) wie folgt aus, um die Azure-Rechteverwaltung für Ihre Cloud-basierte e-Mail-Organisation zu aktivieren und für die Verwendung der Azure Rights Management für Office 365-Nachrichtenverschlüsselung zu konfigurieren: 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Verwenden Sie das Cmdlet Test-IRMConfiguration, um zu überprüfen, ob Sie die TPD und die Azure-Rechteverwaltung aktiviert haben, um die Azure-Rechte Verwaltungsfunktion zu testen. Weitere Informationen finden Sie unter "Beispiel 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>Ich habe die frühere Version von OM mit der Active Directory-Rechteverwaltung eingerichtet, nicht mit Azure Information Protection, was kann ich tun?
<a name="importTPDs"> </a>

Sie können weiterhin Ihre vorhandenen Office 365-Nachrichten Verschlüsselungsregeln mit der Active Directory-Rechteverwaltung verwenden, aber die neuen OM-Funktionen nicht konfigurieren oder verwenden. Stattdessen müssen Sie zu Azure Information Protection migrieren. Informationen zur Migration und zur Bedeutung für Ihre Organisation finden Sie unter [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Nächste Schritte
<a name="importTPDs"> </a>

Wenn Sie das Azure Rights Management-Setup abgeschlossen haben, finden Sie weitere [Informationen unter Einrichten neuer Office 365-Nachrichten Verschlüsselungsfunktionen, die auf Azure Information Protection basieren.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
Nachdem Sie Ihre Organisation für die Verwendung der neuen OM-Funktionen eingerichtet haben, können Sie [Nachrichtenfluss Regeln definieren, um e-Mail-Nachrichten mit neuen OM-Funktionen zu schützen](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Verwandte Themen
<a name="importTPDs"> </a>

[Verschlüsselung in Office 365](encryption.md)
  
[Technische Details zur Verschlüsselung in Office 365](technical-reference-details-about-encryption.md)
  
[Was ist Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  


---
title: Features zum Schutz in Azure Information Protection Einführung bei vorhandenen Office 365-Mandanten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
description: Um Hilfe bei der erste Schritt zum Schutz Ihrer Informationen, beginnend Juli 2018 alle qualifizierten Azure Information Protection-Mandanten werden die Schutzfunktionen in Azure Information Protection standardmäßig aktiviert haben. Die Schutzfunktionen in Azure Information Protection wurden in Office 365 als Rights Management oder Azure RMS früher bezeichnet. Wenn Ihre Organisation eine Dienstplan Office E3 oder eine höhere Dienstplan verfügt erhalten Sie jetzt, Informationen über Azure Information Protection schützen, wenn wir diese Features Rollout Head beginnen.
ms.openlocfilehash: be0200da3032dccbcf54e67f3bdfbac800b65526
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529181"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Features zum Schutz in Azure Information Protection Einführung bei vorhandenen Office 365-Mandanten

Um Hilfe bei der erste Schritt zum Schutz Ihrer Informationen, beginnend Juli 2018 alle qualifizierten Azure Information Protection-Mandanten werden die Schutzfunktionen in Azure Information Protection standardmäßig aktiviert haben. Die Schutzfunktionen in Azure Information Protection wurden in Office 365 als Rights Management oder Azure RMS früher bezeichnet. Wenn Ihre Organisation eine Dienstplan Office E3 oder eine höhere Dienstplan verfügt erhalten Sie jetzt, Informationen über Azure Information Protection schützen, wenn wir diese Features Rollout Head beginnen.
  
## <a name="changes-beginning-july-1-2018"></a>Änderungen, die 1 Juli 2018 ab

Starten von 1 Juli 2018, Microsoft die Protection-Funktion in Azure Information Protection für alle Office 365-Mandanten zu aktivieren, die über eine der folgenden Abonnementpläne verfügen:
  
- Office 365 Message Encryption wird als Teil von Office 365 E3 und E5, Microsoft E3 und E5, Office 365 A1, A3, und A5 und Office 365 G3 und G5 angeboten werden. Weitere Lizenzen empfangen die neuen Schutzfunktionen unterstützt von Azure Information Protection erforderlich nicht. 
    
- Sie können auch die Azure Informationen Protection Plan 1 die folgenden Pläne erhalten Sie die neuen Funktionen von Office 365 Message Encryption hinzufügen: Exchange Online – Plan 1, Exchange Online – Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium oder Office 365 Enterprise E1.
    
- Jeder Benutzer profitieren von Office 365 Message Encryption muss lizenziert werden, um die vom Feature abgedeckt werden.
    
- Die vollständige Liste finden Sie unter den [Exchange Online-dienstbeschreibungen](https://technet.microsoft.com/library/exchange-online-service-description.aspx) für Office 365 Message Encryption. 
    
Mandantenadministratoren können den Schutzstatus in Office 365-Administratorportal überprüfen. 
  
![Screenshot, der anzeigt, dass die Verwaltung von Informationsrechten in Office 365 aktiviert wird.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Warum sind wir diese Änderung vornehmen?

Office 365 Message Encryption nutzt die Protection-Funktionen in Azure Information Protection. Im Wesentlichen die letzten Verbesserungen in Office 365 Message Encryption und unsere breiteren Investitionen zum Schutz von Informationen in Microsoft 365 sind wir erleichtern für Organisationen zu aktivieren, und verwenden Sie unsere Schutzfunktionen als in der Vergangenheit Verschlüsselung Technologien wurden schwierig, eingerichtet. Aktivieren der Schutzfunktionen in Azure Information Protection standardmäßig, können Sie schnellen Einstieg um vertraulichen Daten zu schützen.
  
## <a name="does-this-impact-me"></a>Wirkt dies mich sich?

Wenn Ihre Office 365-Organisation eine Anspruch Office 365-Lizenz erworben hat, wird durch diese Änderung Ihres Mandanten beeinträchtigt werden.
  
 **Wichtig!** Wenn Sie Active Directory-Rechteverwaltungsdienste (AD RMS) in Ihrer lokalen Umgebung verwenden, müssen entweder melden Sie sich über diese Änderung sofort oder nach Azure Information Protection migrieren, bevor wir diese Änderung innerhalb der nächsten 30 Tage Rollout. Informationen zum Melden Sie sich, finden Sie unter "Ich AD RMS verwenden, wie bestätigen Out?" weiter unten in diesem Artikel. Wenn Sie migrieren möchten, finden Sie unter [Migrieren von AD RMS zu Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Kann ich mit Active Directory-Rechteverwaltungsdienste (AD RMS) Azure Information Protection verwenden?

Nein. Dies ist kein unterstütztes Bereitstellungsszenario. Ohne zusätzliche Schritte für melden Sie sich möglicherweise einige Computer automatisch starten mithilfe des Diensts für Azure Rights Management und auch Verbinden mit Ihrer AD RMS-Cluster. In diesem Szenario wird nicht unterstützt und unzuverlässige Ergebnisse hat, damit es wichtig ist, dass Sie diese Änderung innerhalb der nächsten 30 Tage bevor wir diese neuen Features Rollout abwählen. Informationen zum Melden Sie sich, finden Sie unter "Ich AD RMS verwenden, wie bestätigen Out?" weiter unten in diesem Artikel. Wenn Sie migrieren möchten, finden Sie unter [Migrieren von AD RMS zu Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Wie weiß ich, wenn ich AD RMS verwende?

Gehen Sie folgendermaßen vor, von der [Vorbereitung der Umgebung für Azure Rights Management, wenn Sie auch über Active Directory-Rechteverwaltungsdienste (AD RMS) verfügen](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) , um zu überprüfen, ob Sie AD RMS bereitgestellt haben: 
  
1. Zwar optional, veröffentlichen die meisten AD RMS-Bereitstellungen den Dienstverbindungspunkt (SCP) in Active Directory, sodass Domänencomputer AD RMS-Cluster ermitteln können. 
  
ADSI-Bearbeitung verwenden, um festzustellen, ob Sie einen Dienstverbindungspunkt in Active Directory veröffentlicht haben: CN = Configuration [Servername] CN = Services, CN = RightsManagementServices, CN = SCP
    
2. Wenn Sie einen Dienstverbindungspunkt nicht verwenden, müssen Windows-Computern, die Verbindung mit einer AD RMS-Cluster für die Suche mithilfe der clientseitigen oder Lizenzierung Umleitung konfiguriert werden, mithilfe der Windows-Registrierungs: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation oder HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Weitere Informationen zu diesen Registrierungsschlüssel Konfigurationen finden Sie unter [Aktivieren des clientseitigen Dienstsuche mithilfe der Windows-Registrierungs](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) und [Umleiten Lizenzierung Datenverkehr vom Server](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic).
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>AD RMS, wie ich nachholen verwendet werden?

Wenn Sie um die bevorstehende Änderung zu bestätigen, führen Sie diese Schritte aus:
  
1. Verwenden ein Arbeit oder Schule Konto, die in Office 365-Organisation über globaler Administrator-Berechtigungen verfügt, eine Windows PowerShell-Sitzung zu starten und eine Verbindung mit Exchange Online. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Führen Sie das Cmdlet "Set-IRMConfiguration" mithilfe der folgenden Syntax aus:
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>Was kann ich erwarte, dass nach dieser Änderung?

Nachdem Sie diese Option aktiviert ist, sofern Sie noch nicht bestätigt, können Sie beginnen, mithilfe der neuen Version von Office 365 Message Encryption, die auf [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) vorgestellt wurde und nutzt die Funktionen Verschlüsselung und dem Schutz der Azure-Informationen Schutz. 
  
![Screenshot, der ein OME zeigt geschützten Nachricht in Outlook im Web.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Weitere Informationen über die neuen Funktionen finden Sie unter [Office 365 Message Encryption](ome.md).
  


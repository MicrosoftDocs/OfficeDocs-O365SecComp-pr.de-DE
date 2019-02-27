---
title: Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 'Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. '
ms.openlocfilehash: 870e5eabca9e799dfca1e99846a5bfe845f65df4
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275935"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten

Wenn ein Benutzer ununterbrochen e-Mail-Nachrichten aus Office 365 sendet, die als Spam klassifiziert sind, wird verhindert, dass Sie weitere Nachrichten senden. Der Benutzer wird als ungültiger ausgehender Absender im Dienst aufgeführt und erhält einen Unzustellbarkeitsbericht (NDR), der Folgendes angibt:

- Ihre Nachricht konnte nicht zugestellt werden, da Sie nicht als gültiger Absender erkannt wurden. Der häufigste Grund dafür ist, dass Ihre e-Mail-Adresse verdächtigt wird, Spam zu senden, und dass es nicht mehr möglich ist, Nachrichten außerhalb Ihrer Organisation zu senden. Wenden Sie sich an Ihren e-Mail-Administrator.  Der Remote Server hat "550 5.1.8 Access denied, Ungültiger Absender" zurückgegeben.

Die mandantenadministratoren erhalten außerdem eine Warnung, dass der Benutzer nicht mehr ausgehende Nachrichten senden kann.

## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Antispam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

Das folgende Verfahren kann auch über Remote-PowerShell ausgeführt werden. Verwenden Sie das Cmdlet Get-BlockedSenderAddress, um die Liste der eingeschränkten Benutzer abzurufen und Remove-BlockedSenderAddress, um die Einschränkung zu entfernen. Informationen zur Verwendung von Windows PowerShell zum Herstellen einer Verbindung mit Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Entfernen von Einschränkungen für ein gesperrtes Office 365-e-Mail-Konto

Sie führen diese Aufgabe im Office 365 Security & Compliance Center (SCC) aus. Weitere Informationen zu SCC [finden Sie im Office 365 Security _AMP_ Compliance Center](go-to-the-securitycompliance-center.md) . Sie müssen sich in der Rollengruppe " **Organisationsverwaltung** " oder " **Sicherheits Administrator** " befinden, um diese Funktionen ausführen zu können. Weitere Informationen zu SCC-Rollengruppen [finden Sie unter Berechtigungen im Office 365 Security _AMP_ Compliance Center](permissions-in-the-security-and-compliance-center.md) .

1. Melden Sie sich mit einem Arbeits-oder Schulkonto mit globalen Administratorrechten von Office 365 an dem Office 365 Security and Compliance Center an, und klicken Sie in der Liste auf der linken Seite auf **Bedrohungs Verwaltung**, wählen Sie **Überprüfung**, und wählen Sie dann **eingeschränkt Benutzer**.
    
    > [!TIP]
    > Verwenden Sie die folgende URL, um direkt zur Seite " **eingeschränkte Benutzer** " (früher als Aktions &amp; Center bezeichnet) im Security Compliance Center zu wechseln: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Diese Seite enthält die Liste der Benutzer, für die das Senden von e-Mails an außerhalb Ihrer Organisation blockiert wurde.  Suchen Sie den Benutzer, für den Sie Einschränkungen entfernen möchten, und klicken Sie dann auf **entsperren**.

3. Klicken Sie zur Bestätigung der Änderung auf **Ja**. 
    
> [!NOTE]
> Es gibt eine Grenze für die Häufigkeit, mit der ein Konto vom mandantenadministrator aufgehoben werden kann. Wenn der Grenzwert für einen Benutzer überschritten wurde, wird eine Fehlermeldung angezeigt. Sie müssen dann den Support kontaktieren, um den Benutzer aufzuheben.<br/><br/> Es kann bis zu einer Stunde dauern, bis der Benutzer blockiert wurde.
  
## <a name="third-party-block-lists"></a>Drittanbieter-Blockierungslisten

Exchange Online Protection verwendet auch Sperrlisten von Drittanbietern, um Entscheidungen bei der Spamfilterung zu treffen. Benutzer, Websites, Domänen und IP-Adressen können Blocklisten hinzugefügt werden, nur um in einer Spamnachricht zu erscheinen. Als Office 365-Administrator sollten Sie versuchen, diese Objekte aus den Drittanbieter-Listen Anbietern zu entfernen, wenn Sie zu Ihnen gehören.

> [!NOTE]
> Wenn ein Benutzer außerhalb von Office 365 Nachrichten nicht an Ihr Office 365-Konto senden kann, kann sich dessen Konto in der Liste der externen blockierten Absender befinden. Benutzer außerhalb von Office 365 können sich selbst mithilfe des [Self-Service-Delisting-Portals](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)entfernen. 

## <a name="for-more-information"></a>Weitere Informationen

[Antworten auf ein kompromittiertes e-Mail-Konto](responding-to-a-compromised-email-account.md)

[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  
[Pool für besonders riskante Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)

[Berechtigungen im Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md)

  


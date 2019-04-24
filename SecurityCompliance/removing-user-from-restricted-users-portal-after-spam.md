---
title: Entfernen eines Benutzers aus dem Portal für Benutzer mit eingeschränktem Zugriff nach dem Senden von Spam-E-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Wenn ein Benutzer ununterbrochen e-Mails von Office 365 sendet, die als Spam klassifiziert werden, werden Sie nicht mehr Nachrichten senden.
ms.openlocfilehash: a4f22b4d5192df202c1caa19714e8b5476dd8205
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264937"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Entfernen eines Benutzers aus dem Portal für Benutzer mit eingeschränktem Zugriff nach dem Senden von Spam-E-Mails

Wenn ein Benutzer ununterbrochen e-Mails von Office 365 sendet, die als Spam klassifiziert werden, werden Sie nicht mehr ausgehende Nachrichten senden. Der Benutzer wird als ungültiger ausgehender Absender im Dienst aufgeführt und erhält einen Unzustellbarkeitsbericht (NDR), der Folgendes angibt:

- Ihre Nachricht konnte nicht zugestellt werden, da Sie nicht als gültiger Absender erkannt wurden. Der häufigste Grund dafür ist, dass Ihre e-Mail-Adresse verdächtigt wird, Spam zu senden, und dass es nicht mehr möglich ist, Nachrichten außerhalb Ihrer Organisation zu senden. Wenden Sie sich an Ihren e-Mail-Administrator. Der Remote Server hat "550 5.1.8 Access denied, Ungültiger Absender" zurückgegeben.

## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Antispam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

Das folgende Verfahren kann auch über Remote-PowerShell erfolgen. Verwenden Sie das Cmdlet Get-BlockedSenderAddress, um die Liste der eingeschränkten Benutzer abzurufen und Remove-BlockedSenderAddress, um die Einschränkung zu entfernen. Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Entfernen von Einschränkungen für ein gesperrtes Office 365-e-Mail-Konto

Sie führen diese Aufgabe im Security & Compliance Center (SCC) aus. Weitere Informationen zu SCC [finden Sie im Security _AMP_ Compliance Center](go-to-the-securitycompliance-center.md) . Sie müssen sich in der Rollengruppe " **Organisationsverwaltung** " oder " **Sicherheits Administrator** " befinden, um diese Funktionen ausführen zu können. Weitere Informationen zu SCC-Rollengruppen [finden Sie unter Berechtigungen im Security _AMP_ Compliance Center](permissions-in-the-security-and-compliance-center.md) .

1. Melden Sie sich mit einem Arbeits-oder Schulkonto mit globalen Administratorrechten von Office 365 an dem Office 365 Security and Compliance Center an, und klicken Sie in der Liste auf der linken Seite auf **Bedrohungs Verwaltung**, wählen Sie **Überprüfung**, und wählen Sie dann **eingeschränkt Benutzer**.
    
    > [!TIP]
    > Verwenden Sie die folgende URL, um direkt zur Seite " **eingeschränkte Benutzer** " (früher als Aktions &amp; Center bezeichnet) im Security Compliance Center zu wechseln: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Diese Seite enthält die Liste der Benutzer, für die das Senden von e-Mails an außerhalb Ihrer Organisation blockiert wurde.  Suchen Sie den Benutzer, für den Sie Einschränkungen entfernen möchten, und klicken Sie dann auf **entsperren**.

3. Ein Fly-Out geht in die Details zu dem Konto ein, dessen senden eingeschränkt ist. Sie sollten die Empfehlungen durchgehen, um sicherzustellen, dass Sie die richtigen Maßnahmen ergreifen, falls das Konto tatsächlich kompromittiert wird. Klicken Sie nach Abschluss auf **weiter** .

4. Der nächste Bildschirm enthält Empfehlungen, um zukünftige Kompromisse zu vermeiden. Das Aktivieren der mehrstufigen Authentifizierung (MFA) und Ändern der Kennwörter ist eine gute Verteidigung. Klicken Sie auf **Benutzer aufheben** , wenn Sie fertig sind.

5. Klicken Sie zur Bestätigung der Änderung auf **Ja**.

    > [!NOTE]
    > Es kann bis zu 30 Minuten dauern, bis Einschränkungen entfernt wurden. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>Sicherstellen, dass Administratoren gewarnt werden, wenn dies der Fall ist

Die mandantenadministratoren erhalten außerdem eine Warnung, dass der Benutzer nicht mehr ausgehende Nachrichten senden kann. Es handelt sich um eine Standardwarnung, die für alle Mandanten bereitgestellt wird und auf der Seite mit den SCC-Warnungsrichtlinien mit dem Titel "Benutzer wird nicht mehr gesendet werden" aufgeführt ist. Weitere Informationen zur Warnung finden Sie unter [Warnungsrichtlinien im Security _AMP_ Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) .

## <a name="for-more-information"></a>Weitere Informationen

[Antworten auf ein kompromittiertes e-Mail-Konto](responding-to-a-compromised-email-account.md)

[Grundlegendes zum Senden von e-Mail-Benachrichtigungen durch Benutzer](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[Pool für besonders riskante Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)

[Berechtigungen im Security & Compliance Center](permissions-in-the-security-and-compliance-center.md)

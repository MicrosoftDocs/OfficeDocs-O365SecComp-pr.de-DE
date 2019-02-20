---
title: Sperren oder Wiederherstellen eines Benutzerkontos in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Mit Office 365 Cloud App Security können Sie ein Benutzerkonto anhalten oder aufheben. '
ms.openlocfilehash: 6c34c04b6a1e389809b611db0ca2f30ecd8c0ada
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087394"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Sperren oder Wiederherstellen eines Benutzerkontos in Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
Angenommen, Sie erhalten eine Warnung, dass eines der Benutzerkonten Ihrer Organisation für Office 365 kompromittiert wurde. Oder nehmen wir an, Sie haben eine Warnung erhalten, die angibt, dass mit einem Benutzerkonto ein Fehler aufgetreten ist. Mit Office 365 Cloud App Security können Sie ein Benutzerkonto anhalten und später wiederherstellen, nachdem Sie die empfangenen Warnungen untersucht haben.
  
> [!NOTE]
> Office 365 Cloud App Security ist in Office 365 Enterprise E5 verfügbar. Wenn Ihre Organisation ein anderes Office 365 Enterprise-Abonnement verwendet, kann Office 365 Cloud App Security als Add-on erworben werden. (klicken sie als globaler administrator im Office 365 admin center auf **abrechnungs** \> **abonnements hinzufügen**.) Weitere Informationen finden Sie unter [office 365 Platform Service Description: office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [kaufen oder Bearbeiten eines add-ons für Office 365 for Business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>So unterbrechen Sie ein Benutzerkonto in Office 365 Cloud App Security

Wenn Sie ein Benutzerkonto anhalten, verhindern Sie, dass der Benutzer sich erneut anmeldet. Dies entspricht dem Bearbeiten des Benutzerkontos direkt in Office 365, um den Anmeldestatus auf " **angemeldet**" festzulegen.
  
> [!NOTE]
> Wenn Sie verhindern möchten, dass ein Benutzer sich bei Office 365 anmeldet, indem Sie ihn anhalten oder den Anmeldestatus bearbeiten, beachten Sie, dass es eine Stunde dauern kann, bis alle Benutzer Geräte und-Clients wirksam werden ([Bearbeiten oder Ändern eines Benutzers in office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). Wenn der Benutzer bei Office 365 angemeldet ist, wird der Block wirksam, wenn sich Office 365 erneut anmelden muss. 
  
1. Gehen Sie als [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)zu und [https://protection.office.com](https://protection.office.com) melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an. (Dadurch gelangen Sie zum Security &amp; Compliance Center.) 
    
2. Wählen Sie im &amp; Security Compliance Center **Alerts** \> **Manage Advanced Alerts**aus.
    
3. Wählen Sie **Gehe zu Office 365 Cloud App Security**.<br>![Wählen Sie im &amp; Security Compliance Center erweiterte Warnungen verwalten aus, um zu Office 365 Cloud App Security zu wechseln.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>
  
4. Klicken Sie in der Navigationsleiste am oberen Rand des Bildschirms auf **Benachrichtigungen**.
    
5. Doppelklicken Sie in der Spalte **Warnung** auf eine Warnung, die sich auf ein bestimmtes Benutzerkonto bezieht. 
    
6. Wählen Sie unter **Konten**in der Spalte **Status** die Option ![Einstellungs Einstellungen](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> Symbol **Benutzer anhalten**aus.
    
## <a name="to-restore-a-user-account"></a>So stellen Sie ein Benutzerkonto wieder her

Weitere Informationen finden Sie unter [Wiederherstellen eines Benutzers in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Nächste Schritte

- [Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security](review-office-365-cas-alerts.md)
    
- [Verwalten von OAuth-Apps mit Office 365 Cloud App Security](manage-app-permissions-in-ocas.md)
    
- Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    


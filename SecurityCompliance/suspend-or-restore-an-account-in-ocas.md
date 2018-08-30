---
title: Anhalten oder Wiederherstellen eines Benutzerkontos in Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Governance Aktionen, die Sie ergreifen können, werden mit Office 365 Cloud App-Sicherheit unterbrechen oder Fortsetzen eines Benutzerkontos. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529044"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Anhalten oder Wiederherstellen eines Benutzerkontos in Office 365-Cloud-App-Sicherheit

Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
Nehmen Sie an, dass Sie eine Benachrichtigung, dass eine der Benutzerkonten für Office 365 Ihrer Organisation gefährdet. Oder nehmen Sie an, dass Sie eine Benachrichtigung erhalten haben, die angibt, dass etwas mit einem Benutzerkonto falsch ist. Mit Office 365 Cloud App-Sicherheit können anhalten ein Benutzerkontos und einem späteren Zeitpunkt wiederherstellen, nachdem Sie die Benachrichtigungen erhalten Sie untersucht haben.
  
> [!NOTE]
> Office 365-Cloud-App-Sicherheit ist in Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann Office 365-Cloud-App-Sicherheit als Add-on erworben werden. (Als ein globaler Administrator in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Anhalten ein Benutzerkontos in Office 365-Cloud-App-Sicherheit

Wenn Sie ein Benutzerkonto anhalten, verhindern, dass Sie den Benutzer erneut anmelden. Es ist identisch mit der Bearbeitung des Benutzerkontos direkt in Office 365 für festzulegen, dass der Anmeldestatus **- Anmeldung blockiert**.
  
> [!NOTE]
> Wenn Sie einen Benutzer aus anmelden bei Office 365, indem ihre Anmeldestatus, bearbeiten oder unterbrechen sie blockieren Beachten Sie, dass es eine Stunde oder dies wirksam auf allen Geräten und Clients ([Bearbeiten oder ändern ein Benutzers in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) des Benutzers übernehmen kann. Wenn der Benutzer zu Office 365 angemeldet ist, wird der Block wirksam wird, wenn Office 365 erneut anmelden müssen. 
  
1. Als [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md), wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Wählen Sie in der Navigationsleiste oben auf dem Bildschirm **Benachrichtigungen**.
    
5. Doppelklicken Sie in der Spalte **Warnung** auf eine Warnung, die für ein bestimmtes Benutzerkonto relevant ist. 
    
6. Wählen Sie unter **Konten**in der Spalte **Status** Einstellungen ![einstellungssymbol](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend-Benutzer**.
    
## <a name="to-restore-a-user-account"></a>Wiederherstellen ein Benutzerkontos

Finden Sie unter [Wiederherstellen eines Benutzers in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Nächste Schritte

- [Lesen Sie und führen Sie einer Aktion Warnungen in Office 365-Cloud-App-Sicherheit aus](review-office-365-cas-alerts.md)
    
- [Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit](manage-app-permissions-in-ocas.md)
    
- Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    


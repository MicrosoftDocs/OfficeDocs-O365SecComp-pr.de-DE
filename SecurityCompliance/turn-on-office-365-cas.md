---
title: Aktivieren der Office 365 Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: In diesem Artikel erfahren Sie, wie Sie die Sicherheit von Office 365 Cloud-Apps aktivieren, die von Cloud App Security in Microsoft Azure unterstützt wird.
ms.openlocfilehash: 1227545b1e4d1521dc1820342f09aabdf16ec2c6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264127"
---
# <a name="turn-on-office-365-cloud-app-security"></a>Aktivieren der Office 365 Cloud-App-Sicherheit
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächster Schritt](activity-policies-and-alerts.md) <br/> |[Verwendung beginnen](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a>Aktivieren der Office 365 Cloud-App-Sicherheit

> [!IMPORTANT]
> Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die folgende Aufgabe ausführen zu können. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md). Damit Office 365 Cloud App Security korrekt funktioniert, **muss die Überwachungsprotokollierung** für ihre Office 365-Umgebung aktiviert sein. Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md). 
  
1. Gehen Sie als globaler Administrator oder Sicherheitsadministrator zu und [https://protection.office.com](https://security.microsoft.com) melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an. (Dadurch gelangen Sie zum Security &amp; Compliance Center.) 
    
2. Wechseln Sie zu **Warnungen** \> **Verwalten erweiterter Warnungen**.
    
3. Wählen Sie **Office 365 Cloud App Security**aktivieren aus.
    
4. Wählen Sie **Gehe zu Office 365 Cloud App Security**.<br/>![Wählen Sie im &amp; Security Compliance Center erweiterte Warnungen verwalten aus, um zu Office 365 Cloud App Security zu wechseln.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>Dadurch gelangen Sie zum Office 365 Cloud App-Sicherheitsportal, in dem Sie Berichte anzeigen und Richtlinien erstellen oder bearbeiten können.

Nachdem Sie Office 365 Cloud App Security aktiviert haben, können Sie zum Cloud App Security Portal navigieren, indem [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) Sie sich anmelden.
    
> [!NOTE]
> Wenn Sie Office 365 Cloud App Security aktivieren, werden Überwachungsinformationen zu Ihren Office 365-Benutzerkonten und Benutzeraktivitäten an [Microsoft Cloud App Security](https://aka.ms/whatiscas)übertragen. Dadurch kann Office 365 erweiterte Warnungen, Filterung und andere Features bereitstellen, damit Sie Informationen abrufen und Maßnahmen zu verdächtigen Aktivitäten ergreifen können. 
  
## <a name="next-steps"></a>Nächste Schritte

- [Aktivitätsrichtlinien](activity-policies-and-alerts.md)
    
- [Erkennungsrichtlinien für Anomalien](anomaly-detection-policies-in-ocas.md)
    
- [Integrieren Ihres SIEM-Servers](integrate-your-siem-server-with-office-365-cas.md)
    
- [Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung](group-your-ip-addresses-in-ocas.md)
    


---
title: Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security
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
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Verwenden Sie die Seite "Benachrichtigungen" in Office 365 Cloud App Security, um potenzielle Probleme anzuzeigen und Maßnahmen zu ergreifen. Sie können Benachrichtigungen schließen oder auflösen und gegebenenfalls ein Benutzerkonto anhalten.
ms.openlocfilehash: 6c2f9788cb238e86abc347a3a118eb08fa84e971
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213165"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
   
Sie können die Seite "Benachrichtigungen" in Office 365 Cloud App Security verwenden, um potenzielle Probleme anzuzeigen und gegebenenfalls Maßnahmen zu ergreifen.
  
> [!NOTE]
> Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die Aufgaben in diesem Artikel ausführen zu können. Weitere Informationen finden Sie unter [Permissions &amp; in the Office 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-to-get-to-the-alerts-page"></a>So gelangen Sie zur Seite "Benachrichtigungen"

1. Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.
  
2. Klicken Sie in der Navigationsleiste am oberen Rand des Bildschirms auf **Benachrichtigungen**.<br/>![Auf der Seite Warnungen werden Warnungen angezeigt, die ausgelöst wurden, und alle ausgeführten Aktionen.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a>Überarbeiten und behandeln von Warnungen

Warnungen helfen Ihnen dabei, Aktivitäten in Ihrer Office 365-Cloud-Umgebung zu identifizieren, die Sie möglicherweise weiter untersuchen möchten. Sie können auch beschließen, neue Richtlinien zu erstellen oder vorhandene Richtlinien basierend auf den Warnungen zu bearbeiten, die Ihnen angezeigt werden. Wenn ein Administrator sich beispielsweise an einem seltsamen Ort anmeldet, können Sie eine Richtlinie einrichten, die verhindert, dass Administratoren sich an bestimmten Standorten bei Office 365 anmelden.
  
> [!TIP]
> Sie können die Warnungen nach **Kategorie** oder nach **Schweregrad** filtern, damit Sie die wichtigsten zuerst verwalten können. 
  
Untersuchen Sie für jede Warnung, was Sie verursacht hat, damit Sie entscheiden können, welche Aktion ausgeführt werden soll. Wenn Sie weitere Details zu einer Warnung anzeigen und Maßnahmen ergreifen möchten, wie beispielsweise das Auflösen der Warnung oder das Anhalten eines Benutzerkontos, wählen Sie die Warnung aus, um eine Detailseite zu öffnen. Auf der Seite Details können Sie das Aktivitätsprotokoll, die Konten und Benutzer, die mit der Benachrichtigung verbunden sind, überwachen und folgende Aktionen ausführen:
  
- **Entlassen** Wenn die Warnung falsch positiv war, schließen Sie Sie. Sie können optional einen Kommentar hinzufügen, der erklärt, warum Sie ihn entlassen haben. 
    
- **Warnung auflösen** Wenn die Warnung durch eine Aktivität ausgelöst wurde, von der Sie wissen, dass es sich nicht um eine Bedrohung handelt, beheben Sie Sie. Sie können optional einen Kommentar hinzufügen, der erklärt, warum Sie ihn aufgelöst haben. 
    
- **Anhalten** Wenn Sie vermuten, dass unbefugte Benutzer sich für ein Konto anmelden, beispielsweise jemanden, der sich in einem anderen Land anmeldet, wenn Sie wissen, dass sich diese Person physisch in einem lokalen Büro befindet, können Sie [das Konto anhalten](suspend-or-restore-an-account-in-ocas.md) , während Sie untersuchen, was vor sich geht. 
    
## <a name="next-steps"></a>Nächste Schritte

- [Untersuchen einer Aktivität](investigate-an-activity-in-office-365-cas.md)
    
- [Anhalten oder Wiederherstellen eines Benutzerkontos](suspend-or-restore-an-account-in-ocas.md)
    
- Anzeigen einer Liste unterstützter [Webdatenverkehr-Protokolle und Datenquellen](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    


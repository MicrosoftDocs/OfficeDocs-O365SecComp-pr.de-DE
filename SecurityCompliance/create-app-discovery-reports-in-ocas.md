---
title: Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Erstellen Sie Berichte mit Office 365 Cloud App Security, mit denen Sie verstehen können, wie Personen in Ihrer Organisation Office 365 und andere apps verwenden.
ms.openlocfilehash: 23165a52a09e5bcde46ee3ab2110dc17d0faf7f4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259638"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security

|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
   
Office 365 Cloud App Security unterstützt globale Administratoren, Sicherheitsadministratoren und Sicherheits Leser bei der Nutzung von Cloud-Diensten, die in einer Organisation verwendet werden. So können Sie beispielsweise sehen, wo Benutzer Dokumente speichern und zusammenarbeiten und wie viele Daten in Apps oder Dienste hochgeladen werden, die sich außerhalb von Office 365 befinden.
  
Wenn Sie einen app-Ermittlungsbericht generieren möchten, laden Sie Ihre Webprotokolldateien manuell aus Ihren Firewalls und Proxys hoch, und anschließend werden die Dateien für Ihren Bericht von der Office 365 Cloud App Security analysiert und analysiert.
  
> [!NOTE]
> Sie müssen ein globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Erstellen eines Berichts mit der APP-Ermittlung

Wenn Sie einen app-Ermittlungsbericht erstellen möchten, identifizieren Sie die Herstellerdaten Quelle für die Protokolldateien, die Sie analysieren möchten, wählen Sie die Protokolldateien aus, und fordern Sie den Bericht an.
  
> [!NOTE]
> Verwenden Sie Webdatenverkehr-Protokolldateien, die Spitzenauslastungszeiten enthalten, um die optimale Darstellung der Nutzung in Ihrer Organisation zu erhalten. 
  
1. Sammeln Sie Ihre [Webtraffic-Protokolle und Datenquellen für Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an. 
       
3. Wählen Sie **Discover** \> **Create New Report**aus. <br>![Wählen Sie im Office 365-CAS-Portal Discover aus.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)<br>
  
4. Geben Sie einen Namen und eine Beschreibung für den Bericht an, und wählen Sie dann in der Liste **Datenquelle** die Datenquelle für die Webdatenverkehr aus. <br>![Wählen Sie in O365-CAS \> die Option Discover Create New Report aus.](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)<br>Wenn eine Datenquelle, die Sie verwenden möchten, nicht aufgeführt wird, können Sie diese hinzufügen. Wählen Sie **andere** für **Datenquelle**aus, und geben Sie dann den Namen der Datenquelle ein, die Sie hochladen möchten. Wir überarbeiten das Protokoll und informieren Sie, ob die Unterstützung für die Datenquelle hinzugefügt wird, die Sie generiert hat. 
  
5. Navigieren Sie zum Speicherort der gesammelten Protokolldateien, und wählen Sie die Dateien aus. Die Protokolldateien müssen von der Datenquelle generiert worden sein, die Sie für den Bericht ausgewählt haben.
    
6. Klicken Sie auf **Erstellen** , um den Berichterstellungsprozess zu starten. 
    
7. Klicken Sie auf **Snapshot-Berichte verwalten**, um den Status des Berichts anzuzeigen. Wenn ein Bericht fertig ist, wird die Option **Bericht anzeigen** angezeigt. 
    
## <a name="next-steps"></a>Nächste Schritte

- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
- Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    


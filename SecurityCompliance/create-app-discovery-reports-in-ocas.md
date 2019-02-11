---
title: Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Erstellen von Berichten mit Office 365 Cloud App-Sicherheit, mit denen Sie zu verstehen, wie Benutzern in Ihrer Organisation Office 365 und andere apps verwendet werden.
ms.openlocfilehash: 543a194ec9d441a4feea97b8ad49022094565d7a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603716"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security

Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
   
Office 365-Cloud-App-Sicherheit können globale Administratoren Sicherheitsadministratoren und Sicherheit Leser Einblick in die Clouddienste, die Benutzern in einer Organisation verwendet werden. Beispielsweise können Sie sehen, in dem Benutzer speichern und Zusammenarbeit an Dokumenten und wie viele Daten hochgeladen werden, apps oder Diensten, die außerhalb von Office 365 sind.
  
Um ein app-Discovery-Bericht generiert werden soll, Sie die Protokolldateien für Web-Datenverkehr vom Firewalls und -Proxys manuell hochladen, und klicken Sie dann Office 365-Cloud-App-Sicherheit analysiert und analysiert die Dateien für den Bericht.
  
> [!NOTE]
> Sie müssen ein globaler Administrator Sicherheitsadministrator oder Sicherheit Reader zum Ausführen der Aufgaben in diesem Artikel beschriebenen sein. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Erstellen eines Berichts mit app-Ermittlung

Um ein app-Discovery-Bericht erstellen, geben Sie die Hersteller-Datenquelle für die Protokolldateien, die Sie analysiert haben, wählen die Protokolldateien, und klicken Sie dann den Bericht anfordern möchten.
  
> [!NOTE]
> Verwenden Sie die Web-Datenverkehr-Protokolldateien, die Zeiten, in denen die optimale Darstellung der Verwendung in Ihrer Organisation zu erhalten, um Datenverkehr enthalten. 
  
1. Erfassen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung. 
       
3. Wählen Sie **Discover** \> **erstellt einen neuen Bericht**. <br>![Wählen Sie im Office 365 CAS-Portal Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)<br>
  
4. Geben Sie einen Namen und eine Beschreibung für den Bericht, und wählen Sie dann die Datenquelle für die Web-Datenverkehr Protokolle in der Liste **Datenquelle** aus. <br>![Wählen Sie in Office 365-CAS Discover \> erstellen neuen Bericht](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)<br>Wenn eine Datenquelle, die Sie verwenden möchten, nicht aufgeführt ist, können Sie anfordern, dass er hinzugefügt werden. Wählen Sie **andere** für die **Datenquelle**aus, und geben Sie den Namen der Datenquelle, die Sie hochladen möchten. Wir überprüfen Sie das Protokoll und informiert Sie, wenn die Unterstützung für die Datenquelle hinzugefügt werden, die es generiert. 
  
5. Navigieren Sie zum Speicherort der Protokolldateien, die Sie gesammelt, und wählen Sie die Dateien. Die Protokolldateien müssen von der Datenquelle erstellt worden sein, die Sie für den Bericht ausgewählt haben.
    
6. Klicken Sie auf **Erstellen** , um dem Bericht erstellen zu beginnen. 
    
7. Um den Status des Berichts angezeigt wird, klicken Sie auf **die Momentaufnahme Berichte verwalten**. Wenn ein Bericht bereit ist, sehen Sie die Option **Bericht anzeigen** . 
    
## <a name="next-steps"></a>Nächste Schritte

- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security](review-app-discovery-findings-in-ocas.md)
    
- Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    


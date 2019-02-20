---
title: Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Überprüfen der APP-Ermittlungsberichte in Office 365 Cloud-App-Sicherheit kann Ihnen helfen, mehr darüber zu erfahren, wie Personen in Ihrer Organisation Cloud-Apps verwenden. Nachdem Sie die APP-Ermittlungsberichte mithilfe von Protokolldateien aus Ihren Firewalls und Proxys erstellt haben, überarbeiten Sie die Ergebnisse im Dashboard App Discovery.
ms.openlocfilehash: fa5ab7c6cd734feb26878cf1a97f7ce708aa1478
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087334"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security
  
|Auswertung * *\>**|Planung * *\>**|Bereitstellung * *\>**|Auslastung * * * *|
|:-----|:-----|:-----|:-----|
|[Evaluierung starten](office-365-cas-overview.md) <br/> |[Planung starten](get-ready-for-office-365-cas.md) <br/> |[Starten der Bereitstellung](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
   
Das Cloud Discovery-Dashboard arbeitet mit den Webtraffic-Protokollen Ihrer Organisation zusammen, um detaillierte Informationen zur Verwendung von Cloud-apps bereitzustellen. Wenn Sie globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser sind und Ihre Organisation [App-Ermittlungsberichte in Office 365 Cloud App Security erstellt](create-app-discovery-reports-in-ocas.md)hat, können Sie mithilfe des Cloud Discovery-Dashboards Einblicke in die Benutzer in Ihrem die Organisation verwendet Office 365 und andere Cloud-apps. (Das Cloud Discovery-Dashboard wird auch als Produktivitäts-App-Erkennung bezeichnet).
  
 Mit dem Cloud Discovery Dashboard können Sie detaillierte Informationen dazu anzeigen, wie Personen in Ihrer Organisation Office 365 und andere apps verwenden. 
  
![Das Cloud Discovery-Dashboard wurde aktualisiert](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Wechseln zum Dashboard für die Cloud-Suche

1. Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.
    
2. Wechseln **Sie zu Discover** \> **Cloud Discovery Dashboard**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Anzeigen der wichtigsten Benutzer, IP-Adressen, Apps und Risikostufen

Das Cloud Discovery Dashboard bietet Ihnen eine übersichtliche Übersicht über apps, die in Ihrer Organisation mit Office 365 verwendet werden, mit offenen Warnungen, Top-Benutzern und Risikostufen.
  
![Cloud Discovery dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Sehen Sie sich auf der Registerkarte **Dashboard** die allgemeine Cloud-App-Verwendung in Ihrer Organisation im Abschnitt Übersicht am oberen Rand des Bildschirms an. 
    
2. In den **Office 365-Kategorien** finden Sie apps, die in Ihrer Organisation verwendet werden. 
    
3. Sehen Sie sich das Widget " **erkannte apps** " an, um die Verwendung von Office 365 und anderen apps in dieser Ansicht anzuzeigen. 
    
4. Sehen Sie sich das Widget **Top users** and **Top IP Address** an, um diejenigen zu identifizieren, die Office 365 und Cloud-apps am meisten in Ihrer Organisation verwenden. 
    
5. Sehen Sie, wo die apps, die Personen verwenden, nach geographischem Standort mithilfe der Standort Karte für **apps** verwendet werden. 
    
6. Sehen Sie sich über dem Kartenbereich die Risikobewertung der erkannten apps in der Übersicht **Risikostufen** an. Sie können Risiken anhand der gleichen Gruppen und Kategorien anzeigen, die Sie im Bereich **erkannte apps** verwendet haben. Sie können beispielsweise sehen, wie viel Datenverkehr in jeder Gruppierung aus hoch-, Mittel-oder risikoarmen apps stammt. 
    
## <a name="dive-deeper-into-the-information"></a>Tiefer in die Informationen einTauchen

Sie können die Cloud-Ermittlung verwenden, um apps, Unterdomänen, IP-Adressen und Benutzer genauer zu betrachten.
  
1. Wählen Sie im Dashboard Cloud Discovery die Registerkarte **entdeckte apps** aus. 
    
2. Verwenden Sie den Abschnitt Filter, um apps nach Name, Kategorie, Verwendungsebene oder Datum der letzten Anzeige anzuzeigen.
    
3. Hovern Sie in der Ergebnisliste nach einem APP-Namen, um den Link **Unterdomänen anzeigen anzuzeigen** .<br/> ![Hover neben einer APP, um einen Link zum Anzeigen von Unterdomänen Details anzuzeigen](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>Detaillierte Informationen über die ausgewählte App werden angezeigt.
    
4. Um Details zu IP-Adressen anzuzeigen, wählen Sie die Registerkarte **IP-Adressen** .<br/>![Cloud Discovery zeigt detaillierte Informationen zu IP-Adressen](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>Wählen Sie in der Ergebnisliste eine einzelne IP-Adresse aus, um detailliertere Informationen anzuzeigen.
    
5. Um Details zu Office 365-Benutzern in Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Benutzer** aus.<br/>![Cloud Discovery-Benutzerinformationen](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Entitäten ausschließen

Sie können bestimmte Systembenutzer oder IP-Adressen ausschließen, um sich auf genauere Informationen zu konzentrieren.
  
1. Wählen Sie **Einstellungen** \> für die **Cloud-Erkennung**aus.
    
2. Wählen Sie **Entitäten ausschließen**aus.
    
3. Wählen Sie **Ausgeschlossene Benutzer** oder **ausgeschlossene IP-Adressen**aus.
    
4. Geben Sie die Benutzer oder IP-Adressen an, und geben Sie im Feld **Kommentare** Informationen dazu ein, warum Sie diese Benutzer oder IP-Adressen ausschließen. 
    
5. Wählen Sie **Add** aus.
    
## <a name="next-steps"></a>Nächste Schritte

- [Überarbeiten und Aktionen für Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von App-Ermittlungs Berichten](create-app-discovery-reports-in-ocas.md)
    
- Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    


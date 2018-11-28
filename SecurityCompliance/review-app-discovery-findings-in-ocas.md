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
description: Überprüfen von app-Discovery-Berichten in Advanced Security Management kann Ihnen weitere Informationen zur Verwendung von Personen in Ihrer Organisation Cloud-apps. Nachdem Sie die app-Discovery-Berichte mithilfe von Protokolldateien von Firewalls und Proxys erstellt haben, überprüfen Sie die Ergebnisse in das app-Discovery-Dashboard.
ms.openlocfilehash: ddf3826f5aac9d3c837cf66f1b97b4650df70f32
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706259"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security
  
|Auswertung **\>**|Planen der **\>**|Bereitstellung **\>**|Auslastung ***|
|:-----|:-----|:-----|:-----|
|[Starten Sie auswerten](office-365-cas-overview.md) <br/> |[Starten der Planung](get-ready-for-office-365-cas.md) <br/> |[Starten Sie Bereitstellen von](turn-on-office-365-cas.md) <br/> |Sie sind hier!  <br/> [Nächste Schritte](#next-steps) <br/> |
   
Das Cloud-Discovery-Dashboard funktioniert mit Ihrer Organisation Web Datenverkehr Protokolle mit detaillierten Informationen zur Verwendung von Cloud-app. Wenn Sie ein globaler Administrator, Sicherheitsadministrator oder Sicherheit-Reader sind und Ihre Organisation hat die [app-Discovery-Berichte in Office 365-Cloud-App-Sicherheit erstellt](create-app-discovery-reports-in-ocas.md), können Sie das Dashboard Cloud Discovery Einblick in festlegen, wie Benutzer Ihrer Office 365 und anderen apps Cloud Organisation verwenden. (Das Cloud-Discovery-Dashboard ist auch bekannt als Produktivität App Discovery).
  
 **Ab März 2018, das Cloud-Discovery-Dashboard verfügt über neue Features** , mit denen leichter wie Benutzern in Ihrer Organisation Office 365 und andere apps verwendet werden detaillierte Informationen anzeigen. 
  
![Wurde aktualisiert, das Cloud-Discovery-dashboard](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Wechseln Sie zu dem Cloud-Discovery-dashboard

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.) 
    
2. In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.<br/>(Falls die Office 365-Cloud-App-Sicherheit noch nicht aktiviert, und Sie sind ein globaler Administrator, [Office 365-Cloud-App-Sicherheit zu aktivieren](turn-on-office-365-cas.md).)
    
3. Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.
    
4. Wechseln Sie zu **Discover** \> **Cloud Discovery-Dashboard**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Finden Sie unter der Top-Benutzer, IP-Adressen, apps und Risikoebenen

Das Cloud-Discovery-Dashboard enthält eine Übersicht auf einen Blick von apps, die in Ihrer Organisation, alle geöffneten Benachrichtigungen, Top-Benutzer und Risikoebenen mit Office 365 verwendet werden.
  
![Cloud-Discovery-dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Klicken Sie auf der Registerkarte **Dashboard** betrachten Sie am oberen Rand des Bildschirms die gesamte Cloud app-Verwendung in Ihrer Organisation im Abschnitt Übersicht. 
    
2. Finden Sie in der **Office 365-Kategorien** für apps, die in Ihrer Organisation verwendet werden. 
    
3. Sehen Sie sich das Widget **ermittelte apps** Verwendung von Office 365 und andere apps in dieser Ansicht angezeigt. 
    
4. Sehen Sie sich das Widget **Top-Benutzer** und **Top IP-Adressen** , die identifizieren, die Office 365 verwenden und cloud-apps in den in Ihrer Organisation. 
    
5. Finden Sie unter apps, die Benutzern verwendet werden, wo nach dem geografischen Standort befinden, mithilfe der Zuordnung **Hauptsitz Apps** . 
    
6. Sehen Sie über dem Bereich Maps sich die Risiko Bewertung der erkannten apps in der Übersicht über die **Risikoebenen** . Sie können betrachten Sie Risiken nach den Gruppen und Kategorien, die Sie im Bereich **ermittelte apps** verwendet. Beispielsweise können Sie sehen, wie viel Datenverkehr in jeder Gruppierung hoch, Mittel oder niedrig riskante apps stammt. 
    
## <a name="dive-deeper-into-the-information"></a>Detaillierte Informationen zu der information

Cloud-Erkennung können Sie um einen genaueren Einblick in apps, Unterdomänen, IP-Adressen und Benutzer zu übernehmen.
  
1. Wählen Sie in der Cloud-Discovery-Dashboard der Registerkarte **ermittelte apps** . 
    
2. Verwenden Sie den Abschnitt Filter, um apps nach Name, Kategorie, Auslastung oder Datum der letzten gesehen anzuzeigen.
    
3. Zeigen Sie in der Liste der Ergebnisse durch eine app-Name auf den Link **Anzeigen Unterdomänen** anzuzeigen.<br/> ![Bewegen Sie den Mauszeiger neben einer app aus, um einen Link zur Detailansicht Unterdomäne anzuzeigen](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>Ausführliche Informationen über die gewählte app wird angezeigt.
    
4. Um Details zu IP-Adressen anzuzeigen, wählen Sie die Registerkarte **IP-Adressen** .<br/>![Cloud-Discovery zeigt detaillierte Informationen zu IP-Adressen](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>Wählen Sie in der Liste der Ergebnisse eine einzelne IP-Adresse Ausführlichere Informationen anzeigen.
    
5. Um Details zu Office 365-Benutzer in Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Benutzer** .<br/>![Cloud-Discovery - Benutzer-info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Ausschließen von Entitäten

Sie können bestimmte Benutzer oder die IP-Adressen, um auf bestimmte Informationen konzentrieren ausschließen.
  
1. **Auswählen von** \> **Cloud Discovery-Einstellungen**.
    
2. Wählen Sie die **Entitäten ausschließen**.
    
3. Wählen Sie **Ausgeschlossene Benutzer** oder **Ausgeschlossene IP-Adressen**.
    
4. Geben Sie den Benutzer oder die IP-Adressen, und geben Sie in das Feld **Kommentare** Informationen, warum Sie die Benutzer oder die IP-Adressen ausschließen. 
    
5. Wählen Sie **Add** aus.
    
## <a name="next-steps"></a>Nächste Schritte

- [Lesen und Ausführen einer Aktion Warnungen](review-office-365-cas-alerts.md)
    
- [Erstellen von Berichten für app-Ermittlung](create-app-discovery-reports-in-ocas.md)
    
- Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)
    


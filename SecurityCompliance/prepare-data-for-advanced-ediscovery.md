---
title: Vorbereiten von Daten für Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Informationen zur Verwendung des Office 365 Security &amp; Compliance Center zum Vorbereiten von Office 365-Daten für die Analyse mit Office 365 Advanced eDiscovery. '
ms.openlocfilehash: 8ede0f0cb97e1b49297b66fb2b929b3cb292ed52
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218795"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Vorbereiten von Daten für Office 365 Advanced eDiscovery

In diesem Thema wird beschrieben, wie Sie die Ergebnisse einer Inhaltssuche in einen Fall in Advanced eDiscovery laden. 
  
> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>Schritt 1: Vorbereiten von Office 365-Daten für erweiterte eDiscovery

Um Daten mit Advanced eDiscovery zu analysieren, können Sie die Ergebnisse einer Inhaltssuche verwenden, die Sie im Office 365 Security &amp; Compliance Center (auf der Seite " **Inhaltssuche** " im Office 365 Security &amp; Compliance Center) ausführen oder eine Suche mit einem eDiscovery-Fall verknüpft (auf der **eDiscovery** -Seite im Security &amp; Compliance Center aufgeführt). 
  
Die detaillierten Schritte zum Vorbereiten der Suchergebnisse für die Analyse in Advanced eDiscovery finden Sie unter [Prepare Search results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).
  
> [!NOTE]
> Wenn Sie Daten außerhalb von Office 365 haben und Sie in Office 365 importieren möchten, damit Sie Sie in Advanced eDiscovery vorbereiten und analysieren können, finden Sie unter [Übersicht über das Importieren von PST-Dateien in office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) und das Archivieren von [drittanbieterdaten in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918). 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>Schritt 2: Laden der Suchergebnis Daten in einen Fall in Advanced eDiscovery

Nachdem Sie die Suchergebnisse im Security &amp; Compliance Center für die Analyse vorbereitet haben, besteht der nächste Schritt darin, die Suchergebnisse in einen Fall in Advanced eDiscovery zu laden. Ausführlichere Informationen finden Sie unter [Run the Process Module](run-the-process-module-in-advanced-ediscovery.md).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.
    
3. Klicken Sie im Security &amp; Compliance Center auf **Suche &amp; Untersuchung** \> **eDiscovery**, um die Liste der Fälle in Ihrem Unternehmen anzuzeigen. 
    
4. Klicken Sie neben dem Fall, in den Sie Daten laden möchten, in Advanced eDiscovery auf **Öffnen** . 
    
5. Klicken Sie auf der Seite **Start** für den Fall auf **Advanced eDiscovery**. 
    
    ![Klicken Sie auf zu Advanced eDiscovery wechseln, um den Fall in Advanced eDiscovery zu öffnen.](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    Die Statusleiste **Verbinden mit Advanced eDiscovery** wird angezeigt. Wenn Sie mit Advanced eDiscovery verbunden sind, wird auf der Setup Seite für den Fall eine Liste der Container angezeigt. 
    
    ![Die Groß-/Kleinschreibung wird in Advanced eDiscovery angezeigt.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Diese Container stellen die Suchergebnisse dar, die Sie in Schritt 1 für die Analyse in Advanced eDiscovery vorbereitet haben. Beachten Sie, dass der Name des Containers den gleichen Namen wie die Inhaltssuche im Fall im Security &amp; Compliance Center hat. Die Container in der Liste sind diejenigen, die Sie vorbereitet haben. Wenn ein anderer Benutzer Suchergebnisse für Advanced eDiscovery vorbereitet hat, werden die entsprechenden Container nicht in die Liste aufgenommen. 
    
6. Wenn Sie die Suchergebnis Daten aus einem Container in den Fall in Advanced eDiscovery laden möchten, wählen Sie einen Container aus, und klicken Sie dann auf **verarbeiten**.
    
Nachdem die Suchergebnisse aus dem Security &amp; Compliance Center zu dem Fall in Advanced eDiscovery hinzugefügt wurden, besteht der nächste Schritt darin, die Tools in Advanced eDiscovery zum Analysieren und Ausmerzen der für den Fall relevanten Daten zu verwenden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Einrichten von Benutzern und Fällen](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[Analysieren von Falldaten](analyze-case-data-with-advanced-ediscovery.md)
  
[Verwalten des Relevanz-Setups](manage-relevance-setup-in-advanced-ediscovery.md)
  
[Verwenden des Relevanzmoduls](use-relevance-in-advanced-ediscovery.md)
  
[Exportieren von Falldaten](export-case-data-in-advanced-ediscovery.md)


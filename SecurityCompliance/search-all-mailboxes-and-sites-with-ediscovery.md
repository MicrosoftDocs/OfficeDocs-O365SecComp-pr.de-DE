---
title: Durchsuchen aller Postfächer und Websites mit dem eDiscovery Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: In der eDiscovery Center in Office 365 können Sie alle Postfächer von Exchange Online, SharePoint Online-Websites und OneDrive for Business-Websites in einer einzigen eDiscovery-Suche suchen. Um alle Inhaltsquellen in der Organisation zu suchen, muss ein eDiscovery-Manager die entsprechenden eDiscovery-Berechtigungen für jede Inhaltsquelle zugewiesen werden.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529292"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a>Durchsuchen aller Postfächer und Websites mit dem eDiscovery Center

In der eDiscovery Center in Office 365 können Sie alle Postfächer von Exchange Online, SharePoint Online-Websites und OneDrive for Business-Websites in einer einzigen eDiscovery-Suche suchen. Um alle Inhaltsquellen in der Organisation zu suchen, muss ein eDiscovery-Manager die entsprechenden eDiscovery-Berechtigungen für jede Inhaltsquelle zugewiesen werden. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Ein eDiscovery-Manager muss über die entsprechenden Berechtigungen zum Durchsuchen einer Inhaltsquelle verfügen. Weitere Informationen zum Zuweisen von eDiscovery-Berechtigungen für Postfächer und Websites finden Sie in den folgenden Ressourcen: 
    
  - [Zuweisen von eDiscovery-Berechtigungen in Exchange](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [Zuweisen von eDiscovery-Berechtigungen in SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites](assign-permissions-to-onedrive-for-business-sites.md)
    
- Sie können maximal 10.000 Postfächer und eine unbegrenzte Anzahl von SharePoint Online und OneDrive for Business-Websites in einer einzigen eDiscovery Search-Abfrage suchen. Wenn Sie die bestimmter Websites suchen angeben, ist der Grenzwert jedoch 100 Websites.
    
- Finden Sie [Weitere Informationen](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) im Abschnitt für eine Beschreibung der Grenzen, bei der Anzeige der Ergebnisse der bei der Suche alle Postfächer und Websites. 
    
- Weitere Informationen zum Erstellen von Suchabfragen in das eDiscovery Center finden Sie unter [Erstellen und Ausführen von eDiscovery-Abfragen](https://go.microsoft.com/fwlink/p/?LinkID=404032).
    
## <a name="search-all-locations"></a>Durchsuchen aller Speicherorte

1. Öffnen Sie im eDiscovery Center den eDiscovery-Fall, für den die Suchabfrage ausgeführt werden soll.
    
2. Klicken Sie unter **Suchen und Exportieren**klicken Sie auf eine vorhandene Abfrage oder klicken Sie auf **Neues Element** , um eine neue Suchabfrage zu erstellen. 
    
3. Klicken Sie auf der Seite „Suchabfrage“ im Abschnitt **Quellen** auf **Abfragebereich ändern**.
    
4. Klicken Sie auf der Seite **Abfragebereich ändern** auf **Alles durchsuchen**, und wählen Sie die zu durchsuchenden Speicherorte für Inhalte.
    
  - Wählen Sie **Exchange** um alle Postfächer zu suchen. 
    
  - Wählen Sie **SharePoint** , alle SharePoint Online und OneDrive for Business-Websites zu durchsuchen. 
    
  - Wählen Sie sowohl **Exchange** und **SharePoint** aus, um alle Speicherorte für Inhalte in Ihrer Organisation zu suchen. 
    
![Durchsuchen aller Postfächer und Websites](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. Klicken Sie auf **OK**, um die Änderungen zu speichern. 
    
6. Schließen Sie die Suchabfrage ab, oder überprüfen Sie weitere Informationen auf der Seite „Suchabfrage“, z. B. Schlüsselwortabfrage, Datumsbereich, Eingrenzen bestimmter zu durchsuchenden Inhaltstypen. Klicken Sie auf **Suche**, wenn Sie die Abfrage ausführen möchten. 
    
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

- Die ersten 500 Postfächer und die ersten 500 Websites mit den meisten Ergebnissen sind auf der Seite **Abfrage** unter **Quellen** aufgeführt. 
    
- Die Gesamtanzahl der in allen Inhaltsquellen gefundenen Elemente und deren kombinierte Gesamtgröße werden auf der Seite **Abfrage** unter **Quellen** angezeigt. 
 
    
- Sie können eine Vorschau der 200 neuesten Suchergebnisse aus Exchange-Postfächern oder SharePoint-Websites auf der Seite **Abfrage** anzeigen. 
    
    Der folgende Screenshot zeigt ein Beispiel für die Suchergebnisse, die auf der Seite **Abfrage** beim Durchsuchen aller Postfächer und Websites angezeigt werden. 
    
    ![Screenshot der Ergebnisse beim Durchsuchen aller Standorte](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  


---
title: Funktionsweise von DLP zwischen der Sicherheit &amp; Compliance Center und Exchange-Verwaltungskonsole
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Hier erfahren Sie, wie in das Wertpapier DLP &amp; Compliance Center arbeitet mit DLP und Transport Rules in der Exchange-Verwaltungskonsole.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529728"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>Funktionsweise von DLP zwischen der Sicherheit &amp; Compliance Center und Exchange-Verwaltungskonsole

In Office 365 können Sie eine Data Loss Prevention (DLP) Richtlinie in zwei verschiedenen Admin Center erstellen:
  
- In der **Sicherheit &amp; Compliance Center**, können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive und Exchange erstellen. Wenn möglich, sollten Sie eine DLP-Richtlinie erstellen. Weitere Informationen finden Sie unter [DLP in das Wertpapier &amp; Compliance Center](data-loss-prevention-policies.md).
    
- In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen. Mit dieser Richtlinie können Exchange-Transportregeln, dies ist Weitere Optionen für die Verarbeitung von e-Mail. Weitere Informationen finden Sie unter [DLP in der Exchange-Verwaltungskonsole](https://go.microsoft.com/fwlink/?linkid=852311).
    
DLP-Richtlinien in diesen Admin erstellten Arbeitsplätze nebeneinander - in diesem Thema wird erläutert, wie.
  
![DLP-Seiten auf Sicherheit und Compliance Center und Exchange-Verwaltungskonsole](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>Wie DLP in das Wertpapier &amp; Compliance Center arbeitet mit DLP und Transport Rules in der Exchange-Verwaltungskonsole

Nach der Erstellung einer DLP-Richtlinie in das Wertpapier &amp; Compliance Center, die Richtlinie für alle Standorte in der Richtlinie enthalten bereitgestellt wird. Wenn die Richtlinie Exchange Online enthält, wird der Richtlinie synchronisierter vorhanden und genau die gleiche Weise wie eine DLP-Richtlinie in der Exchange-Verwaltungskonsole erstellt erzwungen. 
  
Wenn Sie die DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, diese Richtlinien funktionieren weiterhin, Anzeigemodus alle Richtlinien für e-Mail, die Sie in das Wertpapier erstellen &amp; Compliance Center. Aber beachten Sie, dass in der Exchange-Verwaltungskonsole erstellte Regeln Vorrang haben. Alle Exchange-Transportregeln werden zuerst verarbeitet, und klicken Sie dann die DLP-Regeln aus der Sicherheit &amp; Compliance Center verarbeitet werden.
  
Dies bedeutet, dass:
  
- Nachrichten, die vom Exchange-Transportregeln blockiert sind wird nicht durch eine in das Wertpapier erstellten DLP-Regeln überprüft abrufen &amp; Compliance Center.
    
- Wenn eine Exchange-Transportregel eine Nachricht in einer Weise ändert, die aufgrund eine DLP-Richtlinie in das Wertpapier match &amp; Compliance Center – beispielsweise das Hinzufügen von externen Benutzern - und dann die DLP-Regeln erkennt dies und erzwingen die Richtlinie wie gewünscht.
    
Beachten Sie, dass der Exchange-Transportregeln, die die Aktion "Beenden der Verarbeitung" verwenden, die Verarbeitung von DLP keine Auswirkung auf Regeln für die auch in das Wertpapier &amp; Compliance Center - wird noch verarbeitet.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>Richtlinie in das Wertpapier Tipps &amp; Compliance Center im Vergleich mit der Exchange-Verwaltungskonsole

Tipps zu Richtlinien können arbeiten entweder mit DLP-Richtlinien und e-Mail Flussregeln erstellt, in der Exchange-Verwaltungskonsole oder mit DLP-Richtlinien in das Wertpapier erstellt &amp; Compliance Center, jedoch nicht beide. Dies ist, da diese Richtlinien werden an unterschiedlichen Standorten gespeichert, aber richtlinientipps können nur von einem einzigen Standort zeichnen.
  
Wenn Sie in der Exchange-Verwaltungskonsole eine beliebige richtlinientipps richtlinientipps konfiguriert haben, die Sie in das Wertpapier konfigurieren &amp; Compliance Center wird nicht angezeigt, für die Benutzer in Outlook im Web und Outlook 2013 und höher, bis Sie die Tipps in der Exchange-Verwaltungskonsole deaktivieren. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Transportregeln funktionsfähig weiterhin, bis Sie entscheiden, ob die Sicherheit zu wechseln &amp; Compliance Center.
  
Notiz, die während der richtlinientipps nur von einem einzigen Standort, zeichnen können e-Mail-Benachrichtigungen werden immer gesendet, selbst wenn Sie sowohl die Sicherheit DLP-Richtlinien verwenden, &amp; Compliance Center und der Exchange-Verwaltungskonsole.
  


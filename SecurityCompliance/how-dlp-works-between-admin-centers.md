---
title: FunktionsWeise von DLP zwischen Security &amp; Compliance Center und Exchange Admin Center
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Erfahren Sie, wie DLP im &amp; Security Compliance Center mit DLP-und Transportregeln im Exchange Admin Center funktioniert.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215645"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>FunktionsWeise von DLP zwischen Security &amp; Compliance Center und Exchange Admin Center

In Office 365 können Sie eine DLP-Richtlinie (Data Loss Prevention, Datenverlust-Verhinderung) in zwei verschiedenen Verwaltungs Centern erstellen:
  
- Im ** &amp; Security Compliance Center**können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive und Exchange erstellen. Wenn möglich, empfehlen wir, dass Sie hier eine DLP-Richtlinie erstellen. Weitere Informationen finden Sie unter [DLP im Security &amp; Compliance Center](data-loss-prevention-policies.md).
    
- In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen. Diese Richtlinie kann Exchange-Transportregeln verwenden, sodass Sie mehr Optionen für die e-Mail-Verarbeitung hat. Weitere Informationen finden Sie unter [DLP im Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).
    
In diesen Verwaltungs Centern erstellte DLP-Richtlinien arbeiten nebeneinander – in diesem Thema wird erläutert, wie.
  
![DLP-Seiten im Security and Compliance Center und Exchange Admin Center](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>FunktionsWeise von DLP im &amp; Security Compliance Center mit DLP-und Transportregeln im Exchange Admin Center

Nachdem Sie im Security &amp; Compliance Center eine DLP-Richtlinie erstellt haben, wird die Richtlinie für alle in der Richtlinie enthaltenen Standorte bereitgestellt. Wenn die Richtlinie Exchange Online enthält, wird die Richtlinie dort synchronisiert und auf genau dieselbe Weise erzwungen wie eine im Exchange Admin Center erstellte DLP-Richtlinie. 
  
Wenn Sie DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, funktionieren diese Richtlinien weiterhin mit allen Richtlinien für e-Mails, die Sie im Security &amp; Compliance Center erstellen. Beachten Sie jedoch, dass Regeln, die in der Exchange-Verwaltungskonsole erstellt wurden, Vorrang haben. Alle Exchange-Transportregeln werden zuerst verarbeitet, und anschließend werden die DLP-Regeln &amp; aus dem Security Compliance Center verarbeitet.
  
Dies führt dazu, dass:
  
- Nachrichten, die durch Exchange-Transportregeln blockiert werden, werden nicht von im Security &amp; Compliance Center erstellten DLP-Regeln gescannt.
    
- Wenn eine Nachricht in einer Exchange-Transportregel so geändert wird, dass Sie eine DLP-Richtlinie im Security &amp; Compliance Center (beispielsweise Hinzufügen externer Benutzer) abstimmt, werden die DLP-Regeln dies erkennen und die Richtlinie nach Bedarf erzwingen.
    
Beachten Sie, dass Exchange-Transportregeln, die die Aktion "Verarbeitung beenden" verwenden, keine Auswirkungen auf die Verarbeitung von &amp; DLP-Regeln im Security Compliance Center haben – Sie werden weiterhin verarbeitet.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>Richtlinien Tipps im Security &amp; Compliance Center im Vergleich zur Exchange-Verwaltungskonsole

Richtlinien Tipps können entweder mit DLP-Richtlinien und Nachrichtenfluss Regeln im Exchange Admin Center oder mit im Security &amp; Compliance Center erstellten DLP-Richtlinien funktionieren, jedoch nicht mit beiden. Der Grund hierfür liegt darin, dass diese Richtlinien an unterschiedlichen Speicherorten gespeichert werden, Richtlinien Tipps können jedoch nur von einem Speicherort aus erstellt werden.
  
Wenn Sie im Exchange Admin Center Richtlinien Tipps konfiguriert haben, werden alle Richtlinien Tipps, die Sie im Security &amp; Compliance Center konfigurieren, nicht für Benutzer in Outlook im Web und Outlook 2013 und höher angezeigt, bis Sie die Tipps im Exchange Admin Center deaktiviert haben. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Transportregeln weiterhin funktionieren, bis Sie sich für das Security &amp; Compliance Center entscheiden.
  
Beachten Sie, dass während Richtlinien Tipps nur von einem einzigen Ort aus gezeichnet werden können, e-Mail-Benachrichtigungen auch dann immer gesendet werden, wenn Sie &amp; DLP-Richtlinien sowohl im Security Compliance Center als auch im Exchange Admin Center verwenden.
  


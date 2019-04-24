---
title: Funktionsweise von DLP zwischen dem Security & Compliance Center und Exchange Admin Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Erfahren Sie, wie DLP im Security & Compliance Center mit DLP-und Nachrichtenfluss Regeln (Transportregeln) in der Exchange-Verwaltungskonsole arbeitet.
ms.openlocfilehash: 66dceb447e02eb01810997c23644c76f68795844
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254928"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a>Funktionsweise von DLP zwischen dem Security & Compliance Center und Exchange Admin Center

In Office 365 können Sie eine DLP-Richtlinie (Data Loss Prevention, Datenverlust-Verhinderung) in zwei verschiedenen Verwaltungs Centern erstellen:
  
- Im **Security _AMP_ Compliance Center**können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive und Exchange erstellen. Wenn möglich, empfehlen wir, dass Sie hier eine DLP-Richtlinie erstellen. Weitere Informationen finden Sie unter [DLP im Security _AMP_ Compliance Center](data-loss-prevention-policies.md).
    
- In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen. Diese Richtlinie kann Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) verwenden, sodass Sie mehr Optionen für die e-Mail-Verarbeitung hat. Weitere Informationen finden Sie unter [DLP im Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).
    
In diesen Verwaltungs Centern erstellte DLP-Richtlinien arbeiten nebeneinander – in diesem Thema wird erläutert, wie.
  
![DLP-Seiten im Security and Compliance Center und Exchange Admin Center](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a>FunktionsWeise von DLP im Security & Compliance Center mit DLP-und Nachrichtenfluss Regeln im Exchange Admin Center

Nachdem Sie im Security & Compliance Center eine DLP-Richtlinie erstellt haben, wird die Richtlinie für alle in der Richtlinie enthaltenen Standorte bereitgestellt. Wenn die Richtlinie Exchange Online enthält, wird die Richtlinie dort synchronisiert und auf genau dieselbe Weise erzwungen wie eine im Exchange Admin Center erstellte DLP-Richtlinie. 
  
Wenn Sie DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, funktionieren diese Richtlinien weiterhin mit allen Richtlinien für e-Mails, die Sie im Security & Compliance Center erstellen. Beachten Sie jedoch, dass Regeln, die in der Exchange-Verwaltungskonsole erstellt wurden, Vorrang haben. Alle Exchange-Nachrichtenfluss Regeln werden zuerst verarbeitet, und anschließend werden die DLP-Regeln aus dem Security & Compliance Center verarbeitet.
  
Dies führt dazu, dass:
  
- Nachrichten, die durch Exchange-Nachrichtenfluss Regeln blockiert werden, werden nicht von DLP-Regeln überprüft, die im Security & Compliance Center erstellt wurden.
    
- Wenn eine Nachricht in einer Exchange-Nachrichtenfluss Regel so geändert wird, dass Sie eine DLP-Richtlinie im Security & Compliance Center (beispielsweise Hinzufügen externer Benutzer) abstimmt, werden die DLP-Regeln dies erkennen und die Richtlinie nach Bedarf erzwingen.
    
Beachten Sie, dass Exchange-Nachrichtenfluss Regeln, die die Aktion "Verarbeitung beenden" verwenden, keine Auswirkungen auf die Verarbeitung von DLP-Regeln im Security & Compliance Center haben – Sie werden weiterhin verarbeitet.
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a>Richtlinien Tipps im Security & Compliance Center im Vergleich zur Exchange-Verwaltungskonsole

Richtlinien Tipps können entweder mit DLP-Richtlinien und Nachrichtenfluss Regeln funktionieren, die im Exchange Admin Center erstellt wurden, oder mit DLP-Richtlinien, die im Security & Compliance Center erstellt wurden, aber nicht in beiden. Der Grund hierfür liegt darin, dass diese Richtlinien an unterschiedlichen Speicherorten gespeichert werden, Richtlinien Tipps können jedoch nur von einem Speicherort aus erstellt werden.
  
Wenn Sie im Exchange Admin Center Richtlinien Tipps konfiguriert haben, werden alle Richtlinien Tipps, die Sie im Security & Compliance Center konfigurieren, nicht Benutzern in Outlook im Web und Outlook 2013 und höher angezeigt, bis Sie die Tipps im Exchange Admin Center deaktiviert haben. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Nachrichtenfluss Regeln weiterhin funktionieren, bis Sie sich für das Security & Compliance Center entscheiden.
  
Beachten Sie, dass während Richtlinien Tipps nur von einem einzigen Ort aus gezeichnet werden können, e-Mail-Benachrichtigungen auch dann immer gesendet werden, wenn Sie DLP-Richtlinien sowohl im Security & Compliance Center als auch im Exchange Admin Center verwenden.
  


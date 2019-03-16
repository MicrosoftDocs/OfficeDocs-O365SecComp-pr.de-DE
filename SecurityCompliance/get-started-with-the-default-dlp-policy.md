---
title: Erste Schritte mit der standardmäßigen DLP-Richtlinie
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
ms.collection:
- M365-security-compliance
description: Bevor Sie Ihre erste DLP-Richtlinie (Data Loss Prevention, Datenverlust) erstellen, hilft DLP, Ihre vertraulichen Informationen mit einer Standardrichtlinie zu schützen. Diese Standardrichtlinie und ihre Empfehlung (siehe unten) helfen Ihnen, Ihre vertraulichen Inhalte zu schützen, indem Sie benachrichtigt werden, wenn e-Mails oder Dokumente, die eine Kreditkartennummer enthalten, für eine andere Person außerhalb Ihrer Organisation freigegeben wurden.
ms.openlocfilehash: fa48025a7b979ad69c600b21a10fbb62567234c3
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2019
ms.locfileid: "30638942"
---
# <a name="get-started-with-the-default-dlp-policy"></a>Erste Schritte mit der standardmäßigen DLP-Richtlinie

Bevor Sie Ihre erste DLP-Richtlinie (Data Loss Prevention, Datenverlust) erstellen, hilft DLP, Ihre vertraulichen Informationen mit einer Standardrichtlinie zu schützen. Diese Standardrichtlinie und ihre Empfehlung (siehe unten) helfen Ihnen, Ihre vertraulichen Inhalte zu schützen, indem Sie benachrichtigt werden, wenn e-Mails oder Dokumente, die eine Kreditkartennummer enthalten, für eine andere Person außerhalb Ihrer Organisation freigegeben wurden. Diese Empfehlung wird auf der **Start** Seite des Security &amp; Compliance Centers angezeigt. 
  
Sie können dieses Widget verwenden, um schnell anzuzeigen, wann und wie viele vertrauliche Informationen freigegeben wurden, und dann die standardmäßige DLP-Richtlinie in nur einem oder zwei Klicken verfeinern. Sie können die Standard-DLP-Richtlinie auch jederzeit bearbeiten, da Sie vollständig anpassbar ist. Beachten Sie, dass wenn die Empfehlung zunächst nicht angezeigt wird, klicken Sie unten im Abschnitt **Empfohlene für Sie** auf **+ mehr** . 
  
![Widget mit dem Namen weiter schützen freigegebene Inhalte](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a>Anzeigen des Berichts und verfeinern der standardmäßigen DLP-Richtlinie

Wenn das Widget zeigt, dass Benutzer vertrauliche Informationen für Personen außerhalb Ihrer Organisation freigegeben haben, wählen Sie unten die Option **DLP-Richtlinie verfeinern** aus. 
  
Der ausführliche Bericht zeigt Ihnen, wann und wie viele Inhalte mit Kreditkartennummern in den letzten 30 Tagen freigegeben wurden. Beachten Sie, dass Regel Übereinstimmungen bis zu 48 Stunden dauern können, bis Sie im Widget angezeigt werden.
  
Zum Schutz der vertraulichen Informationen, die standardmäßige DLP-Richtlinie:
  
- Erkennt, wenn Inhalte in Exchange, SharePoint und OneDrive, die mindestens eine Kreditkartennummer enthalten, für Personen außerhalb Ihrer Organisation freigegeben werden.
    
- Zeigt einen richtlinientipp an und sendet eine e-Mail-Benachrichtigung an Benutzer, wenn Sie versuchen, diese vertraulichen Informationen für Personen außerhalb Ihrer Organisation freizugeben. Weitere Informationen zu diesen Optionen finden Sie unter [Senden von e-Mail-Benachrichtigungen und Anzeigen von Richtlinien Tipps für DLP-Richtlinien](use-notifications-and-policy-tips.md).
    
- Generiert detaillierte Aktivitätsberichte, mit denen Sie nachverfolgen können, wer die Inhalte für Personen außerhalb Ihrer Organisation freigegeben hat. Sie können die [DLP-Berichte](view-the-dlp-reports.md) und [Überwachungsprotokolldaten](search-the-audit-log-in-security-and-compliance.md) (bei **Aktivitäts** = -**DLP**) verwenden, um diese Informationen anzuzeigen.
    
Um die standardmäßige DLP-Richtlinie schnell zu verfeinern, haben Sie folgende Möglichkeiten:
  
- Senden Sie einen Vorfall Bericht per e-Mail, wenn Benutzer diese vertraulichen Informationen für Personen außerhalb Ihrer Organisation freigeben.
    
- Fügen Sie dem e-Mail-Vorfall Bericht weitere Benutzer hinzu.
    
- Blockieren des Zugriffs auf den Inhalt, der die vertraulichen Informationen enthält, aber es dem Benutzer ermöglichen, zu überschreiben und freizugeben oder zu senden, wenn Sie dies benötigen.
    
Weitere Informationen zu Vorfall Berichten oder zum Einschränken des Zugriffs finden Sie unter [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md).
  
Wenn Sie diese Optionen später ändern möchten, können Sie die Standard-DLP-Richtlinie jederzeit bearbeiten – weitere Informationen finden Sie im nächsten Abschnitt.
  
![Einstellungen für das benannte Widget weiter schützen von freigegebenen Inhalten](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a>Bearbeiten der standardmäßigen DLP-Richtlinie

Diese Richtlinie heißt **default Office 365 DLP Policy** und wird unter **Data Loss Prevention** auf der Seite **Richtlinie** des Security &amp; Compliance Centers angezeigt. 
  
Diese Richtlinie ist vollständig anpassbar, genauso wie alle DLP-Richtlinien, die Sie selbst neu erstellen. Sie können die Richtlinie auch deaktivieren oder löschen, damit Ihre Benutzer keine Richtlinien Tipps oder e-Mail-Benachrichtigungen mehr erhalten.
  
![DLP-Richtlinie namens "Standard Office 365 DLP-Richtlinie"](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Wenn das Widget nicht angezeigt wird

Das Widget **Weitere Schutz freigegebene Inhalte** wird im Abschnitt **Empfohlene für Sie** auf der **Start** Seite des Security &amp; Compliance Centers angezeigt. 
  
Dieses Widget wird nur angezeigt, wenn:
  
- Im Security &amp; Compliance Center oder Exchange Admin Center gibt es keine Richtlinien zur Verhinderung von Datenverlust. Dieses Widget soll Ihnen die ersten Schritte mit DLP erleichtern, sodass es nicht angezeigt wird, wenn Sie bereits über DLP-Richtlinien verfügen.
    
- Inhalte, die mindestens eine Kreditkarte enthalten, wurden in den letzten 30 Tagen für eine andere Person außerhalb Ihrer Organisation freigegeben.
    
Beachten Sie, dass Regel Übereinstimmungen bis zu 48 Stunden dauern können, um für das Widget verfügbar zu sein, daher kann es bis zu zwei Tage dauern, bis die Empfehlung angezeigt wird, nachdem vertrauliche Informationen extern freigegeben wurden.
  
Nachdem Sie das Widget zum Verfeinern der standardmäßigen DLP-Richtlinie verwendet haben, wird das Widget auf der **Homepage** ausgeblendet. 
  


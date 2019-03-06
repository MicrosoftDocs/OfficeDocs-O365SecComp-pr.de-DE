---
title: Erste Schritte mit DLP-Richtlinienempfehlungen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Diese Insight-basierte Empfehlung hilft Ihrer Organisation, vertrauliche Inhalte zu schützen, wenn Sie in Office 365 gespeichert und freigegeben wird, indem Sie darüber informiert werden, wenn eine mögliche Lücke in der DLP-Richtlinien Abdeckung vorliegt. Diese Empfehlung wird auf der Startseite des Security &amp; Compliance Centers angezeigt, wenn Ihre Dokumente eine der fünf häufigsten Arten vertraulicher Informationen enthalten, aber nicht durch eine DLP-Richtlinie geschützt sind.
ms.openlocfilehash: ed1140a4f5e09a21aa358564992acd97cd006ba8
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410820"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>Erste Schritte mit DLP-Richtlinienempfehlungen

Diese Insight-basierte Empfehlung hilft Ihrer Organisation, vertrauliche Inhalte zu schützen, wenn Sie in Office 365 gespeichert und freigegeben wird, indem Sie darüber informiert werden, wenn eine mögliche Lücke in der DLP-Richtlinien Abdeckung vorliegt. Diese Empfehlung wird auf der **Start** Seite des Security &amp; Compliance Centers angezeigt, wenn Ihre Dokumente eine der fünf häufigsten Arten von vertraulichen Informationen enthalten, jedoch nicht durch eine DLP-Richtlinie geschützt sind. 
  
Sie können dieses Widget verwenden, um schnell eine angepasste DLP-Richtlinie in nur einem Klick oder zwei zu erstellen, und nachdem Sie diese DLP-Richtlinie erstellt haben, ist sie vollständig anpassbar. Beachten Sie, dass wenn die Empfehlung zunächst nicht angezeigt wird, klicken Sie unten im Abschnitt **Empfohlene für Sie** auf **+ mehr** . 
  
![Widget mit dem Namen "ungeschützte vertrauliche Informationen"](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>Erstellen der empfohlenen DLP-Richtlinie

Wenn das Widget ungeschützte vertrauliche Informationen anzeigt, wählen Sie unten **beginnen** , um schnell eine DLP-Richtlinie zu erstellen. 
  
Um die vertraulichen Informationen zu schützen, müssen Sie diese DLP-Richtlinie:
  
- Erkennt, wann Inhalte in Exchange, SharePoint und OneDrive, die einen der ungeschützten Arten vertraulicher Informationen enthalten, für Personen außerhalb Ihrer Organisation freigegeben werden.
    
- Generiert detaillierte Aktivitätsberichte, mit denen Sie nachverfolgen können, wer die Inhalte für Personen außerhalb Ihrer Organisation freigegeben hat. Sie können die [DLP-Berichte](view-the-dlp-reports.md) und [Überwachungsprotokolldaten](search-the-audit-log-in-security-and-compliance.md) (bei **Aktivitäts** = -**DLP**) verwenden, um diese Informationen anzuzeigen.
    
Sie können auch die DLP-Richtlinie auswählen:
  
- Senden Sie Ihnen eine Vorfall Bericht-e-Mail, wenn Benutzer viele dieser vertraulichen Informationen für Personen außerhalb Ihrer Organisation freigeben.
    
- Fügen Sie dem e-Mail-Vorfall Bericht weitere Benutzer hinzu.
    
- Zeigen Sie einen richtlinientipp an, und senden Sie eine e-Mail-Benachrichtigung an die Benutzer, wenn Sie versuchen, diese vertraulichen Informationen für Personen außerhalb Ihrer Organisation freizugeben. Weitere Informationen zu diesen Optionen finden Sie unter [Senden von e-Mail-Benachrichtigungen und Anzeigen von Richtlinien Tipps für DLP-Richtlinien](use-notifications-and-policy-tips.md).
    
Wenn Sie diese Optionen später ändern möchten, können Sie die DLP-Richtlinie nach der Erstellung bearbeiten. Sie können die Richtlinie beispielsweise restriktiver machen, indem Sie sogar Benutzer daran hindern, Inhalte freizugeben, die vertrauliche Informationen enthalten – lesen Sie den nächsten Abschnitt.
  
![Einstellungen für das Widget mit dem Namen "ungeschützte vertrauliche Informationen"](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>Bearbeiten der empfohlenen DLP-Richtlinie

Nachdem Sie das Widget zum Erstellen einer DLP-Richtlinie verwendet haben, wird die Richtlinie unter Verhinderung von **Datenverlust** auf der Seite **Richtlinie** des Security &amp; Compliance Centers angezeigt. 
  
Standardmäßig wird die Richtlinie **als System empfohlene Richtlinie für die Freigabe vertraulichEr Informationen**bezeichnet. Diese Richtlinie ist vollständig anpassbar, genauso wie alle DLP-Richtlinien, die Sie selbst neu erstellen. Wenn Sie beispielsweise entschieden haben, bei der Verwendung des Widgets keine vorfallberichte und Richtlinien Tipps zu aktivieren, können Sie die Richtlinie jederzeit bearbeiten und diese Optionen jederzeit aktivieren.
  
![Vom System empfohlene Richtlinie für die Freigabe vertraulicher Informationen](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Wenn das Widget nicht angezeigt wird

Das Widget ungeschützte **vertrauliche Informationen** wird im Abschnitt **Empfohlene für Sie** auf der **Start** Seite des Security &amp; Compliance Centers angezeigt. 
  
Dieses Widget wird nur angezeigt, wenn:
  
- Neue Dokumente mit einem der fünf häufigsten Arten von vertraulichen Informationen werden in SharePoint oder OneDrive in den letzten 30 Tagen erkannt.
    
- Vertrauliche Informationen sind nicht bereits durch eine vorhandene DLP-Richtlinie geschützt.
    
Im Gegensatz zu DLP-Richtlinien, die Ihre Daten ständig überprüfen, sucht diese Empfehlung nach Lücken in ihrer DLP-Richtlinien Abdeckung ungefähr alle 48 Stunden, sodass nach der hochgeladenen neuen Inhalte bis zu zwei Tage dauern können, bis die Empfehlung angezeigt wird.
  
Nachdem Sie das Widget zum Erstellen einer empfohlenen DLP-Richtlinie verwendet haben, wird das Widget schließlich auf der **Homepage** ausgeblendet. 
  


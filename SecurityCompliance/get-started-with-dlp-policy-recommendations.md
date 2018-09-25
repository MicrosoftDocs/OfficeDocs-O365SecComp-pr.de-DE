---
title: Erste Schritte mit DLP-Richtlinienempfehlungen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea4459b-cb13-4ce2-b9d1-0619316df88c
description: Diese Empfehlung Insight-gesteuerte kann sich Organisationen vertrauliche Inhalte schützen, wenn es gespeichert und in Office 365 durch Sie darüber informiert, wenn es besteht eine mögliche Lücke in freigegebenen Abdeckung Ihrer DLP-Richtlinie. Sehen Sie auf der Homepage der Sicherheit diese Empfehlung &amp; Compliance Center, wenn Ihre Dokumente die fünf am häufigsten verwendeten Arten von vertraulichen Informationen enthalten, jedoch werden nicht durch eine DLP-Richtlinie geschützt.
ms.openlocfilehash: fcd3a5a3a12932b22c310938c12f71fb01019411
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002628"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>Erste Schritte mit DLP-Richtlinienempfehlungen

Diese Empfehlung Insight-gesteuerte kann sich Organisationen vertrauliche Inhalte schützen, wenn es gespeichert und in Office 365 durch Sie darüber informiert, wenn es besteht eine mögliche Lücke in freigegebenen Abdeckung Ihrer DLP-Richtlinie. Sehen Sie auf **der Homepage der Sicherheit** diese Empfehlung &amp; Compliance Center, wenn Ihre Dokumente die fünf am häufigsten verwendeten Arten von vertraulichen Informationen enthalten, jedoch werden nicht durch eine Data Loss Prevention (DLP) Richtlinie geschützt. 
  
Sie können dieses Widget verwenden, um eine benutzerdefinierte DLP-Richtlinie in einem Mausklick oder zwei schnell zu erstellen, und nach der Erstellung dieses DLP-Richtlinie ist vollständig anpassbar. Beachten Sie, die Wenn Sie nicht zuerst mit dieser Empfehlung sehen klicken Sie auf **+ Weitere** am unteren Rand der Abschnitt **empfohlen für Sie** . 
  
![Widget mit der Bezeichnung ungeschützten vertraulichen Informationen](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>Die empfohlene DLP-Richtlinie erstellen

Wenn das Widget angezeigt, dass Sie vertraulichen Informationen nicht geschützt wird, wählen Sie **Erste Schritte** unten, um schnell zu eine DLP-Richtlinie erstellen. 
  
Schützen Sie wichtige Informationen in DLP-Richtlinie:
  
- Erkennt, wenn Inhalte in Exchange, SharePoint und OneDrive, die eine der ungeschützten Arten von vertraulichen Informationen enthält mit Personen außerhalb Ihrer Organisation gemeinsam genutzt wird.
    
- Generiert ausführliche Berichte an, sodass Sie nachzuverfolgen können, die den Inhalt für Personen außerhalb Ihrer Organisation freigegeben und beim auftreten. Können die [DLP-Berichte](view-the-dlp-reports.md) und [Überwachen von Protokolldaten](search-the-audit-log-in-security-and-compliance.md) (wobei **Aktivität** = **DLP**) auf diese Informationen angezeigt.
    
Sie können auch die DLP-Richtlinie haben:
  
- Senden Sie Ihnen eine e-Mail schadensbericht, wenn Benutzer eine Vielzahl von dieser vertrauliche Informationen mit Personen außerhalb Ihrer Organisation freigeben.
    
- Die e-Mail-schadensbericht andere Benutzer hinzufügen.
    
- Zeigen Sie einen richtlinientipp an und senden Sie eine e-Mail-Benachrichtigung an Benutzer, wenn sie versuchen, diese vertraulichen Informationen mit Personen außerhalb Ihrer Organisation freigeben. Weitere Informationen zu diesen Optionen finden Sie unter [Senden von e-Mail-Benachrichtigungen und richtlinientipps für DLP-Richtlinien anzeigen](use-notifications-and-policy-tips.md).
    
Wenn Sie diese Optionen später ändern möchten, können Sie die DLP-Richtlinie bearbeiten, nachdem er erstellt wurde. Angenommen, Sie können, die Richtlinie restriktiver sogar blockieren Personen aus Freigeben von Inhalten, die sensible Informationen enthält in erster Linie - finden Sie im nächsten Abschnitt.
  
![Einstellungen für das Widget mit der Bezeichnung ungeschützten vertraulichen Informationen](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>Die empfohlene DLP-Richtlinie bearbeiten

Nachdem Sie das Widget verwenden, um eine DLP-Richtlinie zu erstellen, die Richtlinie wird unter **Verhinderung von Datenverlust** auf der Seite **Richtlinie** für die Sicherheit &amp; Compliance Center. 
  
Standardmäßig lautet die Richtlinie **Empfohlen Systemrichtlinie für vertrauliche Informationen freigeben**. Diese Richtlinie ist vollständig anpassbar, die gleiche wie alle DLP-Richtlinie, dass Sie selbst von Grund auf neu erstellen. Beispielsweise wenn Sie nicht, wenn Sie das Widget verwendet Vorfall Berichte sowie Tipps zu Richtlinien zu aktivieren, können Sie immer die Richtlinie bearbeiten und zu diesen Optionen können Sie jederzeit aktivieren.
  
![System empfohlene Richtlinien für die Freigabe von vertraulichen Informationen](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Wenn das Widget ist und wird nicht angezeigt

Das Widget mit der Bezeichnung **Ungeschützte vertrauliche Informationen** im Abschnitt **empfohlen für Sie** von **der Homepage der Sicherheit** angezeigt &amp; Compliance Center. 
  
Dieses Widget erscheint nur, wenn:
  
- Neue Dokumente mit den fünf am häufigsten verwendeten Arten von vertraulichen Informationen werden in den letzten 30 Tagen in SharePoint oder OneDrive erkannt.
    
- Dass vertraulicher Informationen nicht bereits durch eine vorhandene DLP-Richtlinie geschützt sind.
    
Im Gegensatz zu DLP-Richtlinien, die Ihre Daten ständig scannen, diese Empfehlung führt eine Überprüfung auf Lücken in Ihrer DLP-Richtlinie Abdeckung etwa alle 48 Stunden, damit nach neuen Inhalten hochgeladen wird, für die Empfehlung angezeigt werden bis zu zwei Tage dauern kann.
  
Nachdem Sie das Widget verwenden, um eine empfohlene DLP-Richtlinie zu erstellen, verschwindet das Widget schließlich aus **der Homepage** . 
  


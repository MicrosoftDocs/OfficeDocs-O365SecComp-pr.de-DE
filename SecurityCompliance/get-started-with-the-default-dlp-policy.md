---
title: Erste Schritte mit der standardmäßigen DLP-Richtlinie
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Bevor Sie Ihre erste Data Loss Prevention (DLP) Richtlinie selbst erstellen, trägt DLP zum Schutz Ihrer vertraulichen Informationen mit als Standardrichtlinie behandelt. Diese Standardrichtlinie und seine Empfehlung (siehe unten) Hilfe Keep Ihrer sicher aufgefordert werden, wenn e-Mail oder Dokumente, die ein Credit Anzahl Karte vertrauliche Inhalte mit einer anderen Person außerhalb Ihrer Organisation freigegeben wurden.
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530114"
---
# <a name="get-started-with-the-default-dlp-policy"></a>Erste Schritte mit der standardmäßigen DLP-Richtlinie

Bevor Sie Ihre erste Data Loss Prevention (DLP) Richtlinie selbst erstellen, trägt DLP zum Schutz Ihrer vertraulichen Informationen mit als Standardrichtlinie behandelt. Diese Standardrichtlinie und seine Empfehlung (siehe unten) Hilfe Keep Ihrer sicher aufgefordert werden, wenn e-Mail oder Dokumente, die ein Credit Anzahl Karte vertrauliche Inhalte mit einer anderen Person außerhalb Ihrer Organisation freigegeben wurden. Sehen Sie auf **der Homepage der Sicherheit** diese Empfehlung &amp; Compliance Center. 
  
Sie können dieses Widget verwenden, um schnell anzuzeigen, wann und wie viel vertraulicher Informationen freigegeben wurde, und Optimieren Sie die standardmäßige DLP-Richtlinie in einem Mausklick oder zwei. Sie können auch die standardmäßige DLP-Richtlinie können Sie jederzeit bearbeiten, da es vollständig anpassbar ist. Beachten Sie, die Wenn Sie nicht zuerst mit dieser Empfehlung sehen klicken Sie auf **+ Weitere** am unteren Rand der Abschnitt **empfohlen für Sie** . 
  
![Mit dem Namen weiterführende Widget schützen freigegebenen Inhalt](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a>Zeigen Sie des Berichts an und Optimieren Sie die standardmäßige DLP-Richtlinie

Wenn das Widget zeigt, dass Benutzer mit Personen außerhalb Ihrer Organisation vertraulichen Informationen freigegeben haben, wählen Sie am unteren **verfeinern DLP-Richtlinie** . 
  
Der detaillierte Bericht zeigt an, wann und wie viel Inhalt mit Kreditkarte Zahlen in den letzten 30 Tagen freigegeben wurde. Beachten Sie, dass regelübereinstimmungen, bis zu 48 Stunden in das Widget angezeigt ergreifen können wird.
  
Zum Schutz den vertraulichen Informationen, die Standard-DLP-Richtlinie:
  
- Erkennt, wenn Inhalte in Exchange, SharePoint und OneDrive, die mindestens eine Kreditkartennummer enthält mit Personen außerhalb Ihrer Organisation gemeinsam genutzt wird.
    
- Zeigt einen richtlinientipp und sendet eine e-Mail-Benachrichtigung an Benutzer, wenn sie versuchen, diese vertraulichen Informationen mit Personen außerhalb Ihrer Organisation freigeben. Weitere Informationen zu diesen Optionen finden Sie unter [Senden von e-Mail-Benachrichtigungen und richtlinientipps für DLP-Richtlinien anzeigen](use-notifications-and-policy-tips.md).
    
- Generiert ausführliche Berichte an, sodass Sie nachzuverfolgen können, die den Inhalt für Personen außerhalb Ihrer Organisation freigegeben und beim auftreten. Können die [DLP-Berichte](view-the-dlp-reports.md) und [Überwachen von Protokolldaten](search-the-audit-log-in-security-and-compliance.md) (wobei **Aktivität** = **DLP**) auf diese Informationen angezeigt.
    
Um die standardmäßige DLP-Richtlinie zu optimieren, können Sie auswählen, damit diese:
  
- Senden Sie Ihnen eine e-Mail schadensbericht, wenn der Benutzer diese vertraulichen Informationen mit Personen außerhalb Ihrer Organisation freigeben.
    
- Die e-Mail-schadensbericht andere Benutzer hinzufügen.
    
- Blockieren Sie den Zugriff auf den Inhalt, die vertrauliche Informationen enthält, jedoch durch den Benutzer außer Kraft setzen und freigeben oder senden, wenn dies erforderlich ist.
    
Weitere Informationen zu Vorfall Berichte oder Beschränkung des Zugriffs finden Sie unter [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md).
  
Wenn Sie diese Optionen später ändern möchten, können Sie die Standardeinstellung bearbeiten DLP-Richtlinie zu einem beliebigen Zeitpunkt - finden Sie im nächsten Abschnitt.
  
![Einstellungen für weitere namens Widget schützen freigegebenen Inhalt](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a>Bearbeiten Sie die standardmäßige DLP-Richtlinie

Diese Richtlinie ist mit dem Namen **Default Office 365 DLP-Richtlinie** und unter **Verhinderung von Datenverlust** angezeigt wird, auf der Seite **Richtlinie** für die Sicherheit &amp; Compliance Center. 
  
Diese Richtlinie ist vollständig anpassbar, die gleiche wie alle DLP-Richtlinie, dass Sie selbst von Grund auf neu erstellen. Sie können auch deaktivieren oder löschen die Richtlinie so, dass Ihre Benutzer nicht mehr erhalten Tipps zu Richtlinien, oder e-Mail-Benachrichtigungen.
  
![DLP-Richtlinie mit dem Namen Default Office 365 DLP-Richtlinie](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Wenn das Widget ist und wird nicht angezeigt

Das Widget mit dem Namen **weiteren Schutz freigegebenen Inhalt** angezeigt wird, im Abschnitt **empfohlen, für die Sie** **der Homepage der Sicherheit** &amp; Compliance Center. 
  
Dieses Widget erscheint nur, wenn:
  
- Es werden keine Richtlinien zur Verhinderung von Datenverlust in das Wertpapier &amp; Compliance Center oder die Exchange-Verwaltungskonsole. Dieses Widget soll Ihnen dabei helfen mit DLP beginnen, damit es nicht angezeigt wird, wenn Sie bereits über DLP-Richtlinien verfügen.
    
- Inhalte mit mindestens einem Kreditkarte wurde mit einer anderen Person außerhalb Ihrer Organisation in den letzten 30 Tagen freigegeben.
    
Beachten Sie, dass regelübereinstimmungen für das Widget verfügbar sein, damit nach sensible Informationen extern erkannt wird, für die Empfehlung angezeigt werden bis zu zwei Tage dauern kann bis zu 48 Stunden dauern können.
  
Nachdem Sie das Widget verwenden, um die standardmäßige DLP-Richtlinie verfeinern, verschwindet das Widget schließlich aus **der Homepage** . 
  


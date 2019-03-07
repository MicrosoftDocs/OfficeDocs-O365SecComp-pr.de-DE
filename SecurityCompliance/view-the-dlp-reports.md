---
title: Anzeigen der Berichtr zur Verhinderung von Datenverlust
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: Mit den DLP-Berichten in Office 365 können Sie schnell die Anzahl der Übereinstimmungen, Überschreibungen oder falsch positiver DLP-Richtlinien anzeigen. sehen Sie nach, ob Sie im Laufe der Zeit nach oben oder unten tendieren; Filtern Sie den Bericht auf unterschiedliche Weise. , und zeigen Sie zusätzliche Details an, indem Sie einen Punkt auf einer Position im Diagramm auswählen.
ms.openlocfilehash: 6f97a29b5a80eeff60b13ba4467d44e3ef87b028
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454847"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>Anzeigen der Berichtr zur Verhinderung von Datenverlust

Nachdem Sie die Data Loss Prevention (DLP)-Richtlinien erstellt haben, sollten Sie sicherstellen, dass Sie wie gewünscht funktionieren und Ihnen helfen, die Kompatibilität zu behalten. Mit den DLP-Berichten im Office 365 Security &amp; Compliance Center können Sie schnell Folgendes anzeigen:
  
- **DLP-Richtlinien Übereinstimmungen** Dieser Bericht zeigt die Anzahl der DLP-Richtlinien Übereinstimmungen im Laufe der Zeit an. Sie können den Bericht nach Datum, Ort, Richtlinie oder Aktion filtern. Sie können diesen Bericht verwenden, um Folgendes zu tun: 
    
  - Optimieren oder optimieren Sie Ihre DLP-Richtlinien im Testmodus. Sie können die spezifische Regel anzeigen, die mit dem Inhalt übereinstimmte.
    
  - Sie können sich auf bestimmte Zeiträume konzentrieren und so mehr über die Gründe für Spitzen und Trends erfahren.
    
  - Entdecken Sie Geschäftsprozesse, die die DLP-Richtlinien Ihrer Organisation verletzen.
    
  - Verstehen Sie alle geschäftlichen Auswirkungen der DLP-Richtlinien, indem Sie sehen, welche Aktionen auf Inhalte angewendet werden.
    
  - Sie können die Einhaltung einer bestimmten DLP-Richtlinie durch Anzeigen von Übereinstimmungen für diese Richtlinie überprüfen.
    
  - Hier finden Sie eine Liste der wichtigsten Benutzer und Benutzer, die zu Vorfällen in Ihrer Organisation beitragen.
    
  - Zeigen Sie eine Liste der wichtigsten Arten von vertraulichen Informationen in Ihrer Organisation an.
    
- **DLP** -Vorfälle Dieser Bericht zeigt auch Richtlinien Übereinstimmungen im Laufe der Zeit, wie der Bericht mit den Richtlinien Übereinstimmungen. Der Bericht mit den Richtlinien Übereinstimmungen zeigt jedoch Übereinstimmungen auf Regelebene an; Wenn beispielsweise eine e-Mail mit drei verschiedenen Regeln übereinstimmt, werden im Bericht mit den Richtlinien Übereinstimmungen drei verschiedene Einzelposten angezeigt. Im Gegensatz dazu zeigt der Vorfall Bericht Übereinstimmungen auf Elementebene an; Wenn beispielsweise eine e-Mail mit drei verschiedenen Regeln übereinstimmt, zeigt der Vorfall Bericht ein einzelnes Einzelteil für diesen Inhalt an. 
    
  Da die Anzahl der Berichte unterschiedlich aggregiert ist, ist der Bericht "Richtlinien Übereinstimmungen" besser zur Identifizierung von Übereinstimmungen mit bestimmten Regeln und zur Optimierung von DLP-Richtlinien. Der Vorfall Bericht eignet sich besser für die Identifizierung bestimmter Inhaltsteile, die für ihre DLP-Richtlinien problematisch sind.
    
- **DLP-falsch positive und-außer Kraft** setzungen Wenn Ihre DLP-Richtlinie es Benutzern ermöglicht, Sie zu überschreiben oder ein falsch positives Ergebnis zu melden, wird in diesem Bericht die Anzahl solcher Instanzen im Laufe der Zeit angezeigt. Sie können den Bericht nach Datum, Ort oder Richtlinie filtern. Sie können diesen Bericht verwenden, um Folgendes zu tun: 
    
  - Optimieren oder optimieren Sie Ihre DLP-Richtlinien, indem Sie erkennen, welche Richtlinien eine hohe Anzahl falsch positiver Ergebnisse verursachen.
    
  - Zeigen Sie die von Benutzern übermittelten Begründungen an, wenn Sie einen richtlinientipp auflösen, indem Sie die Richtlinie überschreiben.
    
  - Stellen Sie fest, wo DLP-Richtlinien mit gültigen Geschäftsprozessen in Konflikt stehen, indem Sie eine hohe Anzahl von Benutzerüberschreibungen verursachen.
    
Alle DLP-Berichte können Daten aus dem letzten viermonatigen Zeitraum anzeigen. Die neuesten Daten können bis zu 24 Stunden dauern, bis Sie in den Berichten angezeigt werden.
  
Diese Berichte finden Sie im **Dashboard**für Security &amp; Compliance Center \> - **Berichte** \> .
  
![Bericht zu DLP-Richtlinien Übereinstimmungen](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>Anzeigen der von einem Benutzer für eine Außerkraftsetzung übermittelten Ausrichtung

Wenn Ihre DLP-Richtlinie es Benutzern ermöglicht, diese zu überschreiben, können Sie den Bericht falsch positiv und außer Kraft setzen verwenden, um den von Benutzern im richtlinientipp übermittelten Text anzuzeigen.
  
![Feld "Ausrichtung" in Details des DLP-falsch positiven und-Außerkraftsetzungs Berichts](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>Ergreifen von Einblicken und Empfehlungen

Berichte können Einblicke und Empfehlungen enthalten, mit denen Sie auf das rote Warnsymbol klicken können, um Details zu potenziellen Problemen anzuzeigen und mögliche Abhilfemaßnahmen zu ergreifen.
  
![Klicken auf ein Einblicke-Symbol, um Details und auszuführende Aktionen anzuzeigen](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a>Suchen der Cmdlets für die DLP-Berichte

Um die meisten Cmdlets für das Security &amp; Compliance Center zu verwenden, müssen Sie Folgendes tun:
  
1. [Eine Verbindung zum Office 365 Security &amp; Compliance Center mithilfe von Remote-PowerShell herstellen](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Verwenden eines dieser [Office 365 Security &amp; Compliance Center](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409) -Cmdlets
    
DLP-Berichte benötigen jedoch Pull-Daten von über Office 365, einschließlich Exchange Online. Aus diesem Grund stehen die Cmdlets für die DLP-Berichte in Exchange Online PowerShell zur Verfügung, nicht &amp; im Security Compliance Center PowerShell. Um die Cmdlets für die DLP-Berichte zu verwenden, müssen Sie daher Folgendes tun:
  
1. [Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Verwenden Sie eines dieser Cmdlets für die DLP-Berichte:
    
      - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    


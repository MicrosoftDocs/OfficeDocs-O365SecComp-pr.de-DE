---
title: Anzeigen der Berichtr zur Verhinderung von Datenverlust
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Mit der DLP-Berichte in Office 365 können Sie schnell die Anzahl der DLP-Richtlinie entspricht, überschreibt oder falsch positive Ergebnisse anzeigen; sehen Sie, ob sie über einen Zeitraum nach oben oder unten Trend sind; Filtern Sie den Bericht auf unterschiedliche Weise. und weitere Details durch Auswählen eines Punkts in einer Zeile im Diagramm anzeigen.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013909"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>Anzeigen der Berichtr zur Verhinderung von Datenverlust

Nachdem Sie Ihre Data Loss Prevention (DLP) Richtlinien erstellen, sollten Sie sicherstellen, dass sie als Sie für die direkte Verwendung und hilft Ihnen, kompatibel bleiben arbeiten. Mit der DLP-Berichte in die Office 365-Sicherheit &amp; Compliance Center, Sie können schnell anzeigen:
  
- **DLP-richtlinienübereinstimmungen** In diesem Bericht werden die Anzahl der Übereinstimmungen mit DLP-Richtlinie über einen Zeitraum. Sie können den Bericht nach Datum, Position, Richtlinie oder Aktion filtern. Sie können diesen Bericht verwenden: 
    
  - Feinabstimmung oder verfeinern Ihrer DLP-Richtlinien, wie Sie sie im Testmodus ausführen. Sie können die Regel anzeigen, die den Inhalt abgeglichen.
    
  - Sie können sich auf bestimmte Zeiträume konzentrieren und so mehr über die Gründe für Spitzen und Trends erfahren.
    
  - Entdecken von Geschäftsprozessen, die Ihre Organisation DLP-Richtlinien verletzen.
    
  - Verstehen Sie alle geschäftliche Relevanz des DLP-Richtlinien von sehen, welche Aktionen auf Inhalte angewendet werden.
    
  - Sie können die Einhaltung einer bestimmten DLP-Richtlinie durch Anzeigen von Übereinstimmungen für diese Richtlinie überprüfen.
    
  - Anzeigen einer Liste der wichtigsten Benutzer, und wiederholen Sie die Benutzer, die auf Vorfälle in Ihrer Organisation beitragen.
    
  - Hier wird eine Liste der oberen Arten von vertraulichen Informationen in Ihrer Organisation.
    
- **DLP-Vorfälle** In diesem Bericht werden auch Richtlinie Übereinstimmungen im Laufe der Zeit ein, wie die Richtlinie Bericht übereinstimmt. Die Richtlinie entspricht jedoch Bericht zeigt Übereinstimmungen auf einer Regelebene. Wenn eine e-Mail-Nachricht auf drei verschiedene Regeln entspricht, entspricht die Richtlinie beispielsweise Bericht zeigt drei verschiedene Zeilenelemente. Im Gegensatz dazu zeigt der Bericht Vorfälle Übereinstimmungen auf einer Elementebene; Beispielsweise zeigt Übereinstimmung eine e-Mail mit drei verschiedene Regeln, der Bericht Vorfälle ein einzelnes Line-Element für diesen Teil des Inhalts. 
    
  Da die Zahlen im Bericht unterschiedlich aggregiert werden, ist der Richtlinie Übereinstimmungen Bericht besser zum Identifizieren von Übereinstimmungen mit bestimmten Regeln und Feinabstimmung DLP-Richtlinien. Der Bericht Vorfälle ist besser geeignet, die bestimmte Teile des Inhalts, die für die DLP-Richtlinien problematisch sind identifiziert.
    
- **Falsch positive Ergebnisse DLP und überschreibt** Wenn DLP-Richtlinie Benutzern ermöglicht das Überschreiben oder ein falsch positives Ergebnis angeben, wird in diesem Bericht Anzahl der solche Instanzen im Zeitverlauf. Sie können den Bericht nach Datum, Standort oder Richtlinie filtern. Sie können diesen Bericht verwenden: 
    
  - Feinabstimmung oder Ihrer DLP-Richtlinien verfeinern, indem Sie sehen, welche Richtlinien eine hohe Anzahl von falsch positive Ergebnisse entstehen.
    
  - Zeigen Sie die Nachweise von Benutzern gesendet werden, wenn sie einen richtlinientipp beheben, indem Sie die Richtlinie zu überschreiben.
    
  - Entdecken Sie die DLP-Richtlinien Konflikt mit gültigen Geschäftsprozesse durch eine hohe Anzahl von Benutzer tätigen, in dem außer Kraft gesetzt.
    
Alle DLP-Berichte können Daten aus der letzten vier Monat Zeitraum anzeigen. Die aktuellsten Daten dauert bis zu 24 Stunden in den Berichten angezeigt werden.
  
Sie finden diese Berichte in das Wertpapier &amp; Compliance Center \> **Berichte** \> **Dashboard**.
  
![DLP-richtlinienübereinstimmungen Bericht](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>Zeigen Sie die Ausrichtung eines Benutzers für eine Außerkraftsetzung übermittelten an

Wenn DLP-Richtlinie außer Kraft setzen, Benutzer zulässt, können Sie das false positive Ergebnis verwenden und Überschreiben des Berichts, um den Text von Benutzern in den richtlinientipp übermittelt anzuzeigen.
  
![Begründung Feld in den Details der DLP falsch positives Ergebnis und Außerkraftsetzung Bericht](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>Ausführen einer Aktion auf Insights und Empfehlungen

Berichte können anzeigen, Insights und Empfehlungen, in dem können Sie auf das rote Symbol finden Sie unter Details zur Ermittlung möglicher Probleme und mögliche Abhilfemaßnahmen übernehmen klicken.
  
![Durch Klicken auf ein Insights-Symbol, um Details und Aktionen finden Sie unter](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a>Hier finden Sie die Cmdlets für die DLP-Berichte

Die meisten der Cmdlets für die Sicherheit zu verwendenden &amp; Compliance Center, müssen Sie:
  
1. [Verbinden mit der Office 365-Sicherheit &amp; Compliance Center mit remote-PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Verwenden Sie eine der folgenden [Sicherheit in Office 365 &amp; Compliance Center Cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
DLP-Berichte müssen jedoch Daten aus über Office 365, einschließlich Exchange Online ziehen. Aus diesem Grund stehen die Cmdlets für die DLP-Berichte in Exchange Online Powershell – nicht in Security &amp; Compliance Center Powershell. Aus diesem Grund müssen für die Verwendung von Cmdlets für die DLP-Berichte:
  
1. [Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Verwenden Sie eine dieser Cmdlets für die DLP-Berichte:
    
      - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    


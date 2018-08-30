---
title: Deaktivieren der junk-e-Berichte in Outlook im Web
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Als ein Office 365-Administrator können Sie die Möglichkeit für die Personen auf Bericht e-Mails als Junk-e-deaktivieren.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272040"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Deaktivieren der junk-e-Berichte in Outlook im Web

Sie können für die Analyse mithilfe der Outlook auf das Web junk-e-Optionen, reporting, wie beschrieben in den [junk-e-Bericht und Phishing-Mails in Outlook im Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)Junk, Phishing und nicht-junknachrichten an Microsoft senden. Wenn Sie keine dieser Optionen verwenden möchten, können Administratoren diese über das Cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) deaktivieren. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
    
- Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "Outlook Web App-Postfachrichtlinien" im Thema [Outlook Web App-Berechtigungen](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 
    
- Vor dem Ausführen der Cmdlets zum Deaktivieren von Berichten zur junk-e-Mail-erforderlich sind, kann es hilfreich sein, lesen Sie die Informationen in den Themen [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) und [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) sein. 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Schalten Sie junk, Phishing und keine Junk-Mails an Microsoft
<a name="sectionSection1"> </a>

Führen Sie zuerst das folgende Cmdlet aus, um die virtuellen Verzeichnisse abzurufen, für die Sie die Meldung deaktivieren möchten:
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

Führen Sie dann das folgende Cmdlet aus, um die Meldung von Junk- und Nicht-Junk-E-Mails an Microsoft zu deaktivieren:
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

Mit dem folgenden Cmdlet wird beispielsweise die Meldung für das virtuelle Verzeichnis "Contoso\owa" deaktiviert:
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?
<a name="sectionSection2"> </a>

Führen Sie Get-OWAMailboxPolicy, um die Parameterwerte zu prüfen und dann Outlook im Web zugreifen, und stellen Sie sicher, dass die Optionen zum Melden von Junk-e-, Phishing, und nicht auf Junk-e-nicht verfügbar sind. Sie werden möglicherweise trotzdem Nachrichten als Junk-e-, Phishing markieren und keine Junk-e-, aber nicht möglich, diese zu melden. 
  


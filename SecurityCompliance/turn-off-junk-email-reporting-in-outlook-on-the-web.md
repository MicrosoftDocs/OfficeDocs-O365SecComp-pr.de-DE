---
title: Deaktivieren der Junk-e-Mail-Berichterstellung in Outlook im Internet
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
ms.collection:
- M365-security-compliance
description: Als Office 365 Administrator können Sie die Möglichkeit deaktivieren, dass Personen e-Mails als Junk-e-Mails melden.
ms.openlocfilehash: a33e43444225cd3c23bc5d40cbf8581d19df2489
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156287"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Deaktivieren der Junk-e-Mail-Berichterstellung in Outlook im Internet

Sie können Junk-e-Mails, Phishing-und nicht-Junk-Nachrichten zur Analyse mithilfe der Optionen für Junk-e-Mail-Berichte im Outlook im Internet (früher als Outlook Web App bezeichnet) senden, wie in [melden von Junk-e-Mails und Phishing-Scams in Outlook im Internet ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)beschrieben. Wenn Sie diese Optionen nicht verwenden möchten, können Administratoren Sie über das Cmdlet "Cmdlet [festlegen-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) " deaktivieren. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Outlook im webpostfach-Richtlinien" im Thema [Berechtigungen für Outlook im Internet](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 

- Wie Sie eine Verbindung mit Exchange Online PowerShell herstellen, finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Deaktivieren von Junk-, Phishing-und nicht-Junk-Berichten an Microsoft
<a name="sectionSection1"> </a>

Führen Sie zunächst den folgenden Befehl aus, um die Namen der verfügbaren Outlook im webpostfach-Richtlinien abzurufen:
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

Verwenden Sie als nächstes die folgende Syntax, um Junk-und nicht-Junk-Berichte an Microsoft in Outlook im Internet zu aktivieren oder zu deaktivieren:
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

In diesem Beispiel wird die Berichterstellung in der standardmäßigen Outlook-Webanwendung-Postfachrichtlinie deaktiviert:
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) und [Sets-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).

## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?
<a name="sectionSection2"> </a>

Führen Sie **Get-OwaMailboxPolicy** aus, um die Parameterwerte zu überprüfen, und öffnen Sie dann Outlook im Internet für einen betroffenen Benutzer (auf den die Outlook im WebPost Fach Richtlinie angewendet wurde), und stellen Sie sicher, dass die Optionen zum Melden von Junk-, Phishing-und nicht-Junk-e-Mails nicht verfügbar sind. Sie können Nachrichten weiterhin als Junk, Phishing und nicht als Junk markieren, aber Sie können Sie nicht melden. 

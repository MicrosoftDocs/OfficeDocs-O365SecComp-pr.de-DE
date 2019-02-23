---
title: Deaktivieren von Junk-e-Mail-Berichten in Outlook im Web
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Als Office 365-Administrator können Sie die Möglichkeit für Personen, e-Mails als Junk-e-Mails zu melden, deaktivieren.
ms.openlocfilehash: efe898f57fdf322ce49edd9e2577daab46dd8d8f
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223824"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Deaktivieren von Junk-e-Mail-Berichten in Outlook im Web

Sie können Junk-, Phishing-und nicht-Junk-e-Mail-Nachrichten mithilfe der Optionen Outlook im Web (früher als Outlook Web App bezeichnet) Junk-Email-Berichterstellung an Microsoft senden, wie in [Bericht Junk-e-Mail und Phishing-Scams in Outlook im Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)beschrieben. Wenn Sie diese Optionen nicht verwenden möchten, können Administratoren Sie über das Cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) deaktivieren. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
    
- Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Outlook im Web-Postfachrichtlinien" im Thema [Outlook im Web Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 

- Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Deaktivieren von Junk-, Phishing-und nicht Junk-Berichterstellung an Microsoft
<a name="sectionSection1"> </a>

Führen Sie zunächst den folgenden Befehl aus, um die Namen der verfügbaren Outlook im Web-Postfachrichtlinien abzurufen:
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

Verwenden Sie als nächstes die folgende Syntax, um Junk-und nicht Junk-Berichte zu Microsoft in Outlook im Web zu aktivieren oder zu deaktivieren:
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

In diesem Beispiel wird die Berichterstellung in der Outlook Web App-Standardpostfachrichtlinie deaktiviert:
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) und [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).

## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?
<a name="sectionSection2"> </a>

Führen Sie **Get-OwaMailboxPolicy** aus, um die Parameterwerte zu überprüfen, und öffnen Sie dann Outlook im Web für einen betroffenen Benutzer (auf den die Outlook in der Web-Postfachrichtlinie angewendet wurde), und stellen Sie sicher, dass die Optionen zum Melden von Junk-, Phishing-und nicht Junk-e-Mails nicht verfügbar sind. Sie können Nachrichten weiterhin als Junk-e-Mail, als Phishing und nicht als Junk markieren, aber Sie können Sie nicht melden. 

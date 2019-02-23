---
title: Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: Die standardmäßige Antispamaktion für EOP-Kunden ist das Verschieben von Spamnachrichten in den Junk-E-Mail-Ordner der Empfänger. Für diese Arbeit mit lokalen Postfächern müssen Sie Exchange-Transportrichtlinien auf Ihren lokalen Edge- oder Hub-Servern konfigurieren, um von EOP hinzugefügte Spam-Kopfzeilen zu erkennen. Über diese Transportregeln wird der von der SclJunkThreshold-Eigenschaft des Set-OrganizationConfig-Cmdlets verwendete SCL-Wert so festgelegt, dass Spam in den Junk-E-Mail-Ordner der einzelnen Postfächer verschoben wird.
ms.openlocfilehash: f712e66934956bcf46215e4016501003ce9b1725
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222884"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird

> [!IMPORTANT]
> Dieses Thema bezieht sich nur auf Exchange Online Protection (EOP)-Kunden, die Postfächer lokal in einer Hybridbereitstellung hosten. Exchange Online-Kunden, deren Postfächer vollständig in Office 365 gehostet werden, müssen diese Befehle nicht ausführen. 
  
Die standardmäßige Antispamaktion für EOP-Kunden ist das Verschieben von Spamnachrichten in den Junk-E-Mail-Ordner der Empfänger. Für diese Arbeit mit lokalen Postfächern müssen Sie Exchange-Transportrichtlinien auf Ihren lokalen Edge- oder Hub-Servern konfigurieren, um von EOP hinzugefügte Spam-Kopfzeilen zu erkennen. Über diese Transportregeln wird der von der SclJunkThreshold-Eigenschaft des Set-OrganizationConfig-Cmdlets verwendete SCL-Wert so festgelegt, dass Spam in den Junk-E-Mail-Ordner der einzelnen Postfächer verschoben wird. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>So fügen Sie mithilfe der Windows PowerShell Transportregeln hinzu, um sicherzustellen, dass Spam in den Junk-E-Mail-Ordner verschoben wird

1. Greifen Sie auf den Exchange-Verwaltungsshell für den lokalen Exchange-Server zu. Wie eine Exchange-Verwaltungsshell in Ihrer lokalen Exchange-Organisation geöffnet wird, erfahren Sie unter **Open the Shell**.
    
2. Führen Sie den folgenden Befehl aus, um bei der Inhaltsfilterung erkannte Spamnachrichten in den Junk-E-Mail-Ordner weiterzuleiten:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkContentFilteredMail". 
    
3. Führen Sie den folgenden Befehl aus, um als Spam markierte Nachrichten vor dem Erreichen des Inhaltsfilters in den Junk-E-Mail-Ordner weiterzuleiten:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkMailBeforeReachingContentFilter". 
    
4. Führen Sie den folgenden Befehl aus, um sicherzustellen, dass Nachrichten von Absendern in einer Sperrliste in der Spamfilterrichtlinie, z. B. in der Liste **blockierter Absender**, in den Junk-E-Mail-Ordner weitergeleitet werden: 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkMailInSenderBlockList". 
    
Wenn die Aktion **Nachricht in Junk-E-Mail-Ordner verschieben** nicht verwendet werden soll, können Sie eine andere Aktion in den Inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole auswählen. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md). Weitere Informationen zu diesen Feldern in der Nachrichtenkopfzeile finden Sie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md).
  
## <a name="see-also"></a>See also

[New-TransportRule-Cmdlet](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)


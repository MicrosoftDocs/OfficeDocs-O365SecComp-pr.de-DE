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
description: Administratoren erfahren, wie Sie Spam an Benutzer-Junk-e-Mail-Ordner in Exchange Online Protection weiterleiten können.
ms.openlocfilehash: 80c3e3cab1bdaf85e815ab1acc790cc907ebbb91
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341376"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird

> [!IMPORTANT]
> Dieses Thema bezieht sich nur auf Exchange Online Protection (EOP)-Kunden, die Postfächer lokal in einer Hybridbereitstellung hosten. Exchange Online-Kunden, deren Postfächer vollständig in Office 365 gehostet werden, müssen diese Befehle nicht ausführen. 
  
Die standardmäßige Antispam-Aktion für EOP-Kunden besteht darin, Spamnachrichten in den Junk-e-Mail-Ordner der Empfänger zu verschieben. Damit diese Aktion mit lokalen Postfächern funktioniert, müssen Sie Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Edge-oder Hub-Servern konfigurieren, um von EOP hinzugefügte Spam Kopfzeilen zu identifizieren. Diese Nachrichtenfluss Regeln legen die SCL-Bewertung (Spam Confidence Level) fest, die von der SclJunkThreshold-Eigenschaft des Set-OrganizationConfig-Cmdlets verwendet wird, um Spam in den Junk-e-Mail-Ordner jedes Postfachs zu verschieben. 
  
### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>So fügen Sie Nachrichtenfluss Regeln hinzu, um sicherzustellen, dass Spam mithilfe von Windows PowerShell in den Junk-e-Mail-Ordner verschoben wird

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


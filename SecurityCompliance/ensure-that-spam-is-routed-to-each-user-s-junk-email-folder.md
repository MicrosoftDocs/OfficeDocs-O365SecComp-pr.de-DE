---
title: Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 7/16/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: Administratoren können erfahren, wie Sie Spam an Benutzer-Junk-e-Mail-Ordner in Exchange Online Schutz weiterleiten.
ms.openlocfilehash: dc37f2428e009f00a2d6d9dd15d5d2cd505f267a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599851"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird

> [!IMPORTANT]
> Dieses Thema bezieht sich nur auf Exchange Online Protection (EOP)-Kunden, die Postfächer lokal in einer Hybridbereitstellung hosten. Exchange Online-Kunden, deren Postfächer vollständig in Office 365 gehostet werden, müssen diese Befehle nicht ausführen. 
  
Die standardmäßige Antispamaktion für EOP-Kunden ist das Verschieben von Spamnachrichten in den Junk-E-Mail-Ordner der Empfänger. Damit diese Aktion mit lokalen Postfächern funktioniert, müssen Sie Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Edge-oder Hub-Servern konfigurieren, um von EoP hinzugefügte Spam Kopfzeilen zu erkennen. Mit diesen Nachrichtenfluss Regeln wird die SCL-Bewertung (Spam Confidence Level) festgelegt, die von der SclJunkThreshold-Eigenschaft des Cmdlets-OrganizationConfig verwendet wird, um Spam in den Junk-e-Mail-Ordner jedes Postfachs zu übertragen. 
  
### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>So fügen Sie Nachrichtenfluss Regeln hinzu, um sicherzustellen, dass Spam mithilfe von Windows PowerShell in den Junk-e-Mail-Ordner verschoben wird

1. Greifen Sie auf den Exchange-Verwaltungsshell für den lokalen Exchange-Server zu. Wie eine Exchange-Verwaltungsshell in Ihrer lokalen Exchange-Organisation geöffnet wird, erfahren Sie unter **Open the Shell**.
    
2. Führen Sie den folgenden Befehl aus, um bei der Inhaltsfilterung erkannte Spamnachrichten in den Junk-E-Mail-Ordner weiterzuleiten:
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkContentFilteredMail". 
    
3. Führen Sie den folgenden Befehl aus, um als Spam markierte Nachrichten vor dem Erreichen des Inhaltsfilters in den Junk-E-Mail-Ordner weiterzuleiten:
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkMailBeforeReachingContentFilter". 
    
4. Führen Sie den folgenden Befehl aus, um sicherzustellen, dass Nachrichten von Absendern in einer Sperrliste in der Spamfilterrichtlinie, z. B. in der Liste **blockierter Absender**, in den Junk-E-Mail-Ordner weitergeleitet werden: 
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Dabei ist  _NameForRule_ der Name für die neue Regel, z. B. „JunkMailInSenderBlockList". 
    
Wenn die Aktion **Nachricht in Junk-E-Mail-Ordner verschieben** nicht verwendet werden soll, können Sie eine andere Aktion in den Inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole auswählen. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md). Weitere Informationen zu diesen Feldern in der Nachrichtenkopfzeile finden Sie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md).
  

> [!TIP]
> Wenn Sie die Aktion **Nachricht in Junk-e-Mail-Ordner bewegen** nicht verwenden möchten, können Sie eine andere Aktion in den Inhaltsfilter Richtlinien im Exchange Admin Center auswählen. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md). Weitere Informationen zu diesen Feldern in der Nachrichtenkopfzeile finden Sie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md).
> 
## <a name="see-also"></a>Siehe auch

[New-TransportRule-Cmdlet](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)


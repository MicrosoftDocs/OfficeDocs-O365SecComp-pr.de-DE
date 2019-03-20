---
title: Häufig gestellte Fragen (FAQ) zur Quarantäne
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt.
ms.openlocfilehash: 9a9673b3360a9a8b6bf837e09b49aca7a38e2172
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693264"
---
# <a name="quarantine-faq"></a>Häufig gestellte Fragen (FAQ) zur Quarantäne

Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt. Die Antworten richten sich an Kunden von Microsoft Exchange Online und Exchange Online Protection.
  
 **F: Wie kann ich Nachrichten mit Schadsoftware in Quarantäne verwalten?**
  
Sie müssen das Security &amp; Compliance Center verwenden, um Nachrichten anzuzeigen und zu arbeiten, die in Quarantäne gesendet wurden, da Sie Schadsoftware enthalten. Weitere Informationen finden Sie unter [Isolieren von e-Mail-Nachrichten in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
 **F. Wie wird der Dienst konfiguriert, damit Spamnachrichten in Quarantäne gesendet werden?**
  
A. Standardmäßig werden durch die Inhaltsfilterung abgefangene Nachrichten an den Junk-E-Mail-Ordner des Empfängers gesendet. Als Administrator können Sie Richtlinien für die Inhaltsfilterung jedoch auch so konfigurieren, dass Spamnachrichten stattdessen in Quarantäne verschoben werden. Weitere Informationen zu den verschiedenen Aktionen, die bei inhaltsgefilterten Nachrichten durchgeführt werden können, finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).
  
 **F. Bietet der Dienst Administrator- und Endbenutzerverwaltung von Nachrichten in der Spamquarantäne?**
  
A. Administratoren können in der Exchange-Verwaltungskonsole nach E-Mails suchen, die sich in Quarantäne befinden, und Details zu diesen Nachrichten anzeigen. Nach dem Auffinden der Nachricht können Sie sie für bestimmte Benutzer freigeben und dem Microsoft-Spamanalyseteam optional als falsch positiv (kein Junk) melden. Weitere Informationen finden Sie unter [Finden und Freigeben von Nachrichten in Quarantäne als Administrator](find-and-release-quarantined-messages-as-an-administrator.md).
  
Als Endbenutzer können Sie Ihre eigenen Nachrichten in der Spamquarantäne verwalten über: 
  
- Der Spam-Quarantäne-Benutzeroberfläche. Weitere Informationen finden Sie unter [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).
        
 **Wie gewähre ich meinen Endbenutzern Zugriff auf die Spamquarantäne?**
  
A. Für den Zugriff auf die Spam-Quarantäne von Endbenutzern benötigen Endbenutzer eine gültige Office 365-Benutzer-ID samt Kennwort. EOP-Kunden, die lokale Postfächer schützen, müssen gültige e-Mail-Benutzer sein, die über die Verzeichnissynchronisierung oder die EAC erstellt werden. Weitere Informationen zum Verwalten von Benutzern finden Sie unter EOP-Administratoren unter [Verwalten von e-Mail-Benutzern in EoP](eop/manage-mail-users-in-eop.md). Für eigenständige EOP-Kunden empfehlen wir die Verwendung der Verzeichnissynchronisierung und die Aktivierung der verzeichnisbasierten Edge-Blockierung; Weitere Informationen finden Sie unter [Use Directory based Edge Blocking to Reject Messages Sent to invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
 **Q. Können auch andere Nachrichten als Spam in Quarantäne gesendet werden?**
  
A. Nachrichten, die einer e-Mail-Fluss Regel (auch als Transportregel bezeichnet) entsprechen, können auch an die Administrator Quarantäne gesendet werden, wenn dies die konfigurierte Aktion ist. Die Endbenutzer-Quarantäne ist nur für Spam vorgesehen.
  
 **F. Wie lange bleiben Nachrichten in der Quarantäne?**
  
A. Standardmäßig werden Nachrichten in Spamquarantäne in der Quarantäne für 30 Tage aufbewahrt, während isolierte Nachrichten, die mit einer Nachrichtenfluss Regel übereinstimmen, 7 Tage lang in der Quarantäne aufbewahrt werden. Nach diesem Zeitraum werden die Nachrichten gelöscht und können nicht abgerufen werden. Der Aufbewahrungszeitraum für isolierte Nachrichten, die mit einer Nachrichtenfluss Regel übereinstimmen, ist nicht konfigurierbar. Die Aufbewahrungsdauer für Nachrichten in Spam-Quarantäne kann jedoch über die Einstellung **Spam für (Tage)** in ihren Inhaltsfilter Richtlinien gesenkt werden. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).
  
 **F. Kann ich mehr als eine Quarantänenachricht gleichzeitig freigeben oder melden?**
  
A. Im EAC oder der Spamquarantäne für Endbenutzer können derzeit nicht mehrere Nachrichten gleichzeitig freigegeben oder gemeldet werden. Administratoren können dazu allerdings ein Windows Remote-PowerShell-Skript erstellen. Verwenden Sie das [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx)-Cmdlet, um nach Nachrichten zu suchen, und das [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx)-Cmdlet, um sie freizugeben. 
  
 **F. Werden bei der Suche nach in der Quarantäne isolierte Nachrichten Platzhalterzeichen unterstützt? Kann ich für eine bestimmte Domäne nach Nachricht in Quarantäne suchen?**
  
A. Platzhalterzeichen werden bei der Angabe von Suchkriterien im Admin Center von Exchange nicht unterstützt. Wenn Sie beispielsweise nach einem Absender suchen, müssen Sie die vollständige E-Mail-Adresse angeben.
  
Administratoren können Windows Remote-PowerShell verwenden, um mit dem Cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) nach Nachrichten in Quarantäne für eine bestimmte Domäne (z. B. "contoso.com") zu suchen: 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

Die Ergebnisse können an das Cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) übergeben werden. Fügen Sie den Parameter "-ReleaseToAll" hinzu, um die Nachricht für alle Empfänger freizugeben. Nachdem eine Nachricht freigegeben wurde, kann nicht nicht nochmals freigegeben werden. 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```



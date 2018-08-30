---
title: Häufig gestellte Fragen (FAQ) zur Quarantäne
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
description: Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt.
ms.openlocfilehash: cc8a05b575e17dbc71d4b9e214cb29a4cafe8b6b
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003194"
---
# <a name="quarantine-faq"></a>Häufig gestellte Fragen (FAQ) zur Quarantäne

Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt. Die Antworten richten sich an Kunden von Microsoft Exchange Online und Exchange Online Protection.
  
 **F: wie verwalten kann ich Malware isolierte Nachrichten in Quarantäne?**
  
Sie müssen die Sicherheit verwenden &amp; Compliance Center, um das Anzeigen von und Arbeiten mit Nachrichten, die isoliert werden, da sie Schadsoftware gesendet wurden. Weitere Informationen finden Sie unter [Quarantäne e-Mail-Nachrichten in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
 **F. Wie wird der Dienst konfiguriert, damit Spamnachrichten in Quarantäne gesendet werden?**
  
A. Standardmäßig werden durch die Inhaltsfilterung abgefangene Nachrichten an den Junk-E-Mail-Ordner des Empfängers gesendet. Als Administrator können Sie Richtlinien für die Inhaltsfilterung jedoch auch so konfigurieren, dass Spamnachrichten stattdessen in Quarantäne verschoben werden. Weitere Informationen zu den verschiedenen Aktionen, die bei inhaltsgefilterten Nachrichten durchgeführt werden können, finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).
  
 **F. Bietet der Dienst Administrator- und Endbenutzerverwaltung von Nachrichten in der Spamquarantäne?**
  
A. Administratoren können in der Exchange-Verwaltungskonsole nach E-Mails suchen, die sich in Quarantäne befinden, und Details zu diesen Nachrichten anzeigen. Nach dem Auffinden der Nachricht können Sie sie für bestimmte Benutzer freigeben und dem Microsoft-Spamanalyseteam optional als falsch positiv (kein Junk) melden. Weitere Informationen finden Sie unter [Finden und Freigeben von Nachrichten in Quarantäne als Administrator](find-and-release-quarantined-messages-as-an-administrator.md).
  
Als Endbenutzer können Sie Ihre eigenen Nachrichten in der Spamquarantäne verwalten über: 
  
- Der Spam-Quarantäne-Benutzeroberfläche. Weitere Informationen finden Sie unter [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).
        
 **Wie gewähre ich meinen Endbenutzern Zugriff auf die Spamquarantäne?**
  
A: um die Endbenutzer-Spamquarantäne zugreifen zu können, benötigen Endbenutzer einen gültigen Office 365-Benutzer-ID und ein Kennwort. Schützen von lokalen Postfächern EOP-Kunden müssen gültige e-Mail-Benutzer erstellt wurden, über die verzeichnissynchronisierung oder der Exchange-Verwaltungskonsole sein. EOP-Administratoren können zum [Verwalten von e-Mail-Benutzern in EOP](eop/manage-mail-users-in-eop.md)finden Sie weitere Informationen zum Verwalten von Benutzern. Für eigenständige EOP-Kunden wird empfohlen, verzeichnissynchronisierung und verzeichnisbasierte Edge-Blockierung aktivieren; Weitere Informationen finden Sie unter [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
 **Q. Können auch andere Nachrichten als Spam in Quarantäne gesendet werden?**
  
A. Nachrichten, die der Transportregel entsprechen, können ebenfalls in Administrator-Quarantäne gesendet werden, wenn die Aktion entsprechend konfiguriert ist. Die Endbenutzer-Quarantäne ist nur für Spam vorgesehen.
  
 **F. Wie lange bleiben Nachrichten in der Quarantäne?**
  
A. Standardmäßig werden in den Quarantäneordner verschobene Spamnachrichten 15 Tage lang aufbewahrt. Nachrichten im Quarantäneordner, die eine Transportregel erfüllen, werden 7 Tage lang aufbewahrt. Nach Ablauf dieses Zeitraums werden die Nachrichten gelöscht und können nicht mehr wiederhergestellt werden. Der Aufbewahrungszeitraum für Nachrichten im Quarantäneordner, die eine Transportregel erfüllt haben, ist nicht konfigurierbar. Der Aufbewahrungszeitraum für Nachrichten in der Spamquarantäne kann allerdings über die Einstellung **Spamnachrichten aufbewahren für (Tage)** in Ihren Inhaltsfilterrichtlinien verkürzt werden. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).
  
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



---
title: Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. '
ms.openlocfilehash: ff5bb010f45b0c89e08239f0e37885bd7ae5c7cd
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875787"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten

Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können.  
  

Wenn Absender blockiert sind und keine E-Mails senden können, erhalten sie einen Unzustellbarkeitsbericht (oder eine Meldung, dass beim Senden der Nachricht ein Fehler aufgetreten ist) mit Informationen, wie sie vorgehen müssen, um die Blockierung aufzuheben.
  
Nicht nur können einzelne Benutzern durch die Domänen Service, sondern auf bestimmte Websites blockiert und IP-Adressen können auch blockiert werden. In einigen Fällen können Domänen oder Websites einer Sperrliste hinzugefügt werden einfach, da sie in einer Spam-Nachricht angezeigt werden. Als der Office 365-Administrator können Sie versuchen, erhalten Benutzer, Websites, Domänen und IP-Adressen von Drittanbieter-Sperrlisten entfernt. Verwenden Sie die Links in der Tabelle unten in diesem Thema, um jede Drittanbieter zu kontaktieren, und folgen Sie den Anweisungen. Wenn eine Person außerhalb von Office 365 mit Ihrem Office 365-Konto Nachrichten senden kann, ihr Konto möglicherweise auf die Liste der blockierten Absender externe beendet wurden einrichten. Benutzer außerhalb von Office 365 können sich selbst aus der Liste blockierter Absender So entfernen Sie mithilfe der [Self-service-delisting Portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)versuchen.
  
Sie können ausgehende Spameinstellungen konfigurieren, damit Sie eine Benachrichtigung erhalten, wenn ein Office 365-Benutzer blockiert ist und keine E-Mail senden kann, die als Spam klassifiziert wurden. Wenn das Problem mit dem Benutzerpostfach behoben ist, können Sie die Blockierung für diesen Absender aufheben.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>Aufheben der Blockierung eines gesperrten Office 365-E-Mail-Kontos

Sie führen Sie diese Aufgabe in der Office 365-Sicherheit und Compliance Center (SCC). [Wechseln Sie zu der Office 365-Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md) , ausführliche Informationen zum SCC.

1. Unter Verwendung eines Kontos arbeiten oder Schule, die über Office 365 globaler Administrator verfügt, melden Sie sich bei Office 365-Sicherheit und Compliance Center und erweitern in der Liste auf der linken Seite **Threat Management**, wählen Sie **Überprüfen**und wählen Sie dann **eingeschränkt Benutzer**.
    
    > [!TIP]
    > Fahren Sie direkt mit der **Benutzer mit eingeschränkten Rechten** Seite in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Diese Seite enthält die Liste der Benutzer, die am Senden von e-Mails an außerhalb Ihrer Organisation blockiert wurden.  Suchen Sie den Benutzer, die, den Sie auf **Zulassen**Einschränkungen auf Entfernen, und klicken Sie dann auf möchten.

3. Klicken Sie zur Bestätigung der Änderung auf **Ja**. 
    
> [!NOTE]
> Es besteht ein Grenzwert auf die Anzahl der Versuche, die ein Konto durch den Administrator des Mandanten entsperrt werden können Wenn der Grenzwert für einen Benutzer überschritten wurde, wird eine Fehlermeldung angezeigt. Sie müssen dann Support wenden, um den Benutzer aufheben der Blockierung. 
  
## <a name="third-party-block-lists"></a>Drittanbieter-Blockierungslisten

|**Name der Liste**|**Abwahlportal**|**Weitere Informationen**|
|:-----|:-----|:-----|
|URIBL  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[URIBL-website](https://uribl.com/) <br/> |
|SURBL  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[Einführung in SURBL URI Reputation Daten](http://www.surbl.org/) <br/> |
|Spamhaus   <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[Grundlegendes zu DNSBL filtern](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|Invaluement  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[Anti Anti-Spam-Liste](http://dnsbl.invaluement.com/) <br/> |
|Phishtank  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[PhishTank – häufig gestellte Fragen](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> Exchange Online Protection verwendet auch Drittanbieter-Sperrlisten für Spam-Filterung. 
   
## <a name="for-more-information"></a>Weitere Informationen

[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  
[Pool für besonders riskante Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)

[Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  


---
title: Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. '
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026332"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten

Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können.  
  

Wenn Absender blockiert sind und keine E-Mails senden können, erhalten sie einen Unzustellbarkeitsbericht (oder eine Meldung, dass beim Senden der Nachricht ein Fehler aufgetreten ist) mit Informationen, wie sie vorgehen müssen, um die Blockierung aufzuheben.
  
Nicht nur können einzelne Benutzern durch die Domänen Service, sondern auf bestimmte Websites blockiert und IP-Adressen können auch blockiert werden. In einigen Fällen können Domänen oder Websites einer Sperrliste hinzugefügt werden einfach, da sie in einer Spam-Nachricht angezeigt werden. Als der Office 365-Administrator können Sie versuchen, erhalten Benutzer, Websites, Domänen und IP-Adressen von Drittanbieter-Sperrlisten entfernt. Verwenden Sie die Links in der Tabelle unten in diesem Thema, um jede Drittanbieter zu kontaktieren, und folgen Sie den Anweisungen. Wenn eine Person außerhalb von Office 365 mit Ihrem Office 365-Konto Nachrichten senden kann, ihr Konto möglicherweise auf die Liste der blockierten Absender externe beendet wurden einrichten. Benutzer außerhalb von Office 365 können sich selbst aus der Liste blockierter Absender So entfernen Sie mithilfe der [Self-service-delisting Portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)versuchen.
  
Sie können ausgehende Spameinstellungen konfigurieren, damit Sie eine Benachrichtigung erhalten, wenn ein Office 365-Benutzer blockiert ist und keine E-Mail senden kann, die als Spam klassifiziert wurden. Wenn das Problem mit dem Benutzerpostfach behoben ist, können Sie die Blockierung für diesen Absender aufheben.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>Aufheben der Blockierung eines gesperrten Office 365-E-Mail-Kontos

Sie führen Sie diese Aufgabe in der Exchange-Verwaltungskonsole (EAC). Checken Sie [Exchange-Verwaltungskonsole in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) ausführliche Informationen zu der Exchange-Verwaltungskonsole. 
  
> [!NOTE]
> Das Wartungscenter wird nur angezeigt, wenn Sie sich im EAC für Exchange Online befinden. 
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Aktion Center**.
    
    ![Navigieren Sie im Exchange Admin Center zum Wartungscenter](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. Wählen Sie das Symbol **Suche** aus, und geben Sie die SMTP-Adresse des blockierten Benutzers ein. 
    
    ![Suchen nach einem gesperrten Benutzer im Wartungscenter](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. Klicken Sie im Bereich „Beschreibung“ auf **Sperrung des Kontos aufheben**. 
    
    ![Aufheben der Blockierung eines Benutzers im Wartungscenter](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. Klicken Sie zur Bestätigung der Änderung auf **Ja**. 
    
> [!NOTE]
> Es gibt eine Einschränkung dabei, wie oft ein Mandantenadministrator die Blockierung für ein Konto aufheben darf. Wenn der Grenzwert für einen Benutzer überschritten wurde, wird eine Fehlermeldung angezeigt. Wenden Sie sich an den Support, um den Benutzer zu entsperren. 
  
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
  

  


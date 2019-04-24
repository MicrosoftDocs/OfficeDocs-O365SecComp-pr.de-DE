---
title: EOP - Allgemeine häufig gestellte Fragen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9dbff00a-474e-4452-aeb5-5be9a6b8c6d5
description: 'Hier werden die häufigsten allgemeinen Fragen zum cloudgehosteten E-Mail-Filterdienst Microsoft Exchange Online Protection (EOP) beantwortet. Themen mit weiteren häufig gestellten Fragen (FAQs) finden Sie unter den folgenden Links:'
ms.openlocfilehash: 00618618d251e1478cb0dc0a0fbb116db2565fad
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256603"
---
# <a name="eop-general-faq"></a>EOP – Allgemeine häufig gestellte Fragen

Hier werden die häufigsten allgemeinen Fragen zum cloudgehosteten E-Mail-Filterdienst Microsoft Exchange Online Protection (EOP) beantwortet. Themen mit weiteren häufig gestellten Fragen (FAQs) finden Sie unter den folgenden Links:
  
- [Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten](eop-queued-deferred-and-bounced-messages-faq.md)
    
- [Häufig gestellte Fragen zur delegierten Verwaltung](delegated-administration-faq.md)
    
- [HÄUFIG gestellte Fragen zum Antispamschutz](../anti-spam-protection-faq.md)
    
- [Listen sicherer und blockierter Absender in Exchange Online](../safe-sender-and-blocked-sender-lists-faq.md)
    
- [Häufig gestellte Fragen (FAQ) zur Quarantäne](../quarantine-faq.md)
    
- [HÄUFIG gestellte Fragen zum Schutz vor Schadsoftware](../anti-malware-protection-faq-eop.md)
    
- [Message Trace FAQ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx)
    
- [Häufig gestellte Fragen zum Übergang von FOPE zu EOP](http://technet.microsoft.com/library/e0e76b89-b0d3-4c0a-bfc8-137b579e983b.aspx)
    
 **F. Was ist EOP?**
  
A. EOP ist ein cloudgehosteter E-Mail-Filterdienst zum Schutz von Kunden vor Spam und Malware sowie zur Implementierung von benutzerdefinierten Richtlinienregeln.
  
 **F. Wie kann ich mich für eine EOP-Testversion anmelden oder EOP kaufen?**
  
A. Sie können sich über das Web auf der [Exchange Online Protection-Homepage](https://go.microsoft.com/fwlink/p/?LinkId=279912) für eine EOP-Testversion anmelden oder EOP kaufen. Beachten Sie, dass die Funktionalität einer Testversion der eines bezahlten Abonnements entspricht und außerdem die Zusatzfeatures umfasst, die mit dem Abonnementplan [Exchange Enterprise CAL mit Service](https://go.microsoft.com/fwlink/p/?LinkId=320619) geboten werden. 
  
 **F. Was kostet EOP?**
  
A. EOP wird auf Benutzerbasis lizenziert. Die aktuellen Preisinformationen finden Sie auf der [Exchange Online Protection-Homepage](https://go.microsoft.com/fwlink/p/?LinkId=279912).
  
 **F. Wie lange dauert es, um EOP in Produktion zu setzen?**
  
A. Wenn Sie den MX-Eintrag gemäß den Anweisungen unter [Einrichten Ihres EOP-Diensts](set-up-your-eop-service.md) ändern, werden E-Mails sofort beim Durchlaufen von EOP gefiltert. Die Übertragung des MX-Eintrags über DNS kann 24 bis 48 Stunden dauern. Die Schutzeinstellungen in der Exchange-Verwaltungskonsole (EAC) können während dieses Vorgangs jederzeit angepasst werden.
  
 **F. Benötige ich alle Funktionen von Microsoft Office 365, um EOP verwenden zu können? Was ist, wenn ich nur den EOP-Schutz nutzen möchte und sonst nichts?**
  
A. Sie können EOP zum Schutz lokaler Postfächer nutzen, ohne andere Funktionen von Office 365 zu verwenden. Dies wird als "eigenständiges Abonnement" bezeichnet. Eine Liste der EOP-Features finden Sie in der [Exchange Online Protection-Dienstbeschreibung](https://go.microsoft.com/fwlink/p/?LinkId=320619).
  
 **F. Weshalb benötige ich einen Office 365-Mandanten, wenn ich mich für die E-Mail-Filterung über EOP anmelde?**
  
A. Office 365 ist der Name einer Kollektion von Produkten und Dienstleistungen, auf die über einen Office 365-Mandanten zugegriffen werden kann. Sie sollten den Office 365-Mandanten als Ausgangspunkt betrachten, zu dem Sie Lizenzen für die E-Mail-Filterung hinzufügen können.
  
 **F. Verfügt EOP über ein Kommunikationsportal, auf dem ich Informationen über bekannte Probleme und die zu erwartenden Lösungen abrufen kann? Wie verhält es sich mit neuen Funktionen?**
  
A. Das Microsoft 365 Admin Center hat einige dieser Informationen. Wenn Sie von einem Service Level-Ereignis betroffen sind, sollte eine Kommunikations Warnung angezeigt werden (in der Regel mit einem Bell-Symbol verbunden), nachdem Sie sich im Microsoft 365 Admin Center angemeldet haben. Es wird empfohlen, dass Sie sämtliche zugehörigen Hinweise lesen und entsprechend vorgehen.
  
Was neue EOP-Funktionen angeht, ist die [Office 365-Roadmap](https://office.microsoft.com/en-us/products/office-365-roadmap-FX104343353.aspx) eine gute Ressource für Informationen zu bevorstehenden neuen Funktionen. Außerdem stellen wir auf der Website [Office-Blogs](https://go.microsoft.com/fwlink/p/?LinkId=392724) Blogbeiträge zu den neuen Features bereit. 
  
 **F. Funktioniert der Dienst mit älteren Exchange-Versionen (z. B. Exchange Server 2010) und in Umgebungen, die nicht auf Exchange basieren?**
  
A. Ja, der Dienst ist serveragnostisch und kann mit einem beliebigen SMTP-E-Mail-Übertragungs-Agent verwendet werden.
  
 **F. Welche Größe muss eine Organisation haben, um den Dienst verwenden zu können?**
  
A. Die Größe spielt keine Rolle. Das EOP-Netzwerk bietet für das Wachstum Ihrer Organisation ausreichend Kapazität - unabhängig davon, wie schnell es erfolgt.
  
 **Welche Berechtigungen müssen für EOP eingerichtet werden?**
  
Zum Konfigurieren von EOP (Exchange Online Protection) müssen Sie globaler Office 365-Administrator oder Exchange-Unternehmensadministrator (Rollengruppe "Organisationsverwaltung") sein.
  
 **F. Woher weiß ich, ob meine Daten und persönlichen Informationen sicher sind?**
  
A. Informationen zu den Maßnahmen, die zum Schutz Ihrer Daten und persönlichen Informationen ergriffen wurden, sowie zu Vereinbarungen zum Servicelevel (Service Level Agreements, SLAs) finden Sie im [Office 365 Trust Center](https://go.microsoft.com/fwlink/p/?LinkId=285405).
  
 **F: Gibt es Obergrenzen, die ich kennen sollte, z. B. bei der Nachrichtengröße?**
  
A. Ja. Weitere Informationen zu Grenzen in EOP finden Sie unter [Beschränkungen von Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=402617). 
  
 **F. Wird Windows Remote-PowerShell von EOP unterstützt?**
  
A. Ja, über Windows Remote-PowerShell sind sämtliche EOP-Funktionen verfügbar. Weitere Informationen finden Sie unter [PowerShell in Exchange Online Protection](http://technet.microsoft.com/library/f7918a88-774a-405e-945b-bc2f5ee9f748.aspx).
  


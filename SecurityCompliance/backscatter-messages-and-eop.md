---
Title: "Backscatter Messages and EOP" MS. Author: krowley Author: kccross Manager: laurawi ms. Date: 12/9/2016 ms. Audience: ITPro ms. Topic: article ms. Service: O365-seccomp ms. Custom: TN2DMC localization_priority: normal Search. appverid:
- MET150 ms. Asset-Nr.: 6f64f2de-D626-48ed-8084-03cc72301aa4 ms. Collection:
    - M365-Security-Compliance Description: "Backscatter-Nachrichten sind die automatisierten Bounce-Nachrichten, die von e-Mail-Servern gesendet werden, in der Regel als Ergebnis eingehender Spam-Mails. Die BACKSCATTERER-DNSBL ist eine Liste von IP-Adressen, die Rückläufer Nachrichten senden. Es handelt sich nicht um eine Spammer-Liste, und wir versuchen nicht, unsere Server aus der BACKSCATTERER-DNSBL zu entfernen. "
---

# <a name="backscatter-messages-and-eop"></a>Rückläufernachrichten und EOP

Rückläufernachrichten sind die automatischen Unzustellbarkeitsnachrichten, die von E-Mail-Servern, meist als Reaktion auf eingehende Spamnachrichten, gesendet werden. Da Exchange Online Protection (EOP) ein Spamfilterdienst ist, werden E-Mail-Nachrichten an nicht vorhandene Empfänger und andere verdächtige Ziele von dem Dienst zurückgewiesen. In diesem Fall generiert EOP eine Unzustellbarkeitsnachricht (Non-Delivery Report, NDR) und übermittelt sie zurück an den „Absender". Da Spammer häufig gefälschte oder ungültige Absenderadressen in ihren Nachrichten verwenden, verursacht die Absenderadresse, an die die Unzustellbarkeitsnachricht gesendet wird, möglicherweise eine Rückläufernachricht. Daraufhin können Postausgangsserver, die mit dem EOP-Netzwerk verbunden sind, auf der Backscatterer DNSBL (DNS Block List, DNS-basierte Sperrliste) gelistet werden. Die Backscatterer DNSBL ist eine Liste von IP-Adressen, von denen Rückläufernachrichten gesendet werden. Es ist keine Spammerliste, daher versuchen wir nicht, unsere Server aus der Backscatterer DNSBL zu löschen. 
  
> [!TIP]
> Laut den Anweisungen auf der Backscatterer-Website stellt die Verwendung des Zurückweisungsmodus für alle eingehenden E-Mails keine empfohlene Konfiguration oder Verwendung des Diensts dar. Er sollte stattdessen im sicheren Modus verwendet werden. Weitere Informationen zum Implementieren der richtigen Rückläuferkonfiguration finden Sie auf der [Website Backscatterer.org](http://www.backscatterer.org/?target=usage). 
  
## <a name="for-more-information"></a>Weitere Informationen

[Der Backscatterer.org Liste von IP](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
Siehe "NDR-Rückläufer" in [Advanced Spam Filtering Options](advanced-spam-filtering-asf-options.md)
  


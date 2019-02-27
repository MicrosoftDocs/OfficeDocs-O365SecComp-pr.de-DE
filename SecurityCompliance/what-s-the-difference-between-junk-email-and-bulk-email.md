---
title: Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
description: Kunden askwhat manchmal der Unterschied zwischen Junk-e-Mail und Massen-e-Mail-Nachrichten? In diesem Thema wird der Unterschied erläutert und Informationen zu den verschiedenen Optionen bereitgestellt, die für Exchange Online und Exchange Online Protection (EOP) verfügbar sind.
ms.openlocfilehash: 877912c94af5d4b399769759189d091c62d50075
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275715"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a>Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?

Kunden fragen mitunter, worin der Unterschied zwischen Junk-E-Mail und Massen-E-Mail bestehe. Zweck dieses Themas ist die Erläuterung des Unterschieds und Bereitstellung von Informationen zu den verschiedenen Optionen, die sowohl in Exchange Online als auch Exchange Online Protection (EOP) zur Verfügung stehen.
  
 **Was ist Junk-E-Mail?**
  
Junk-E-Mail-Nachrichten sind Spamnachrichten, d. h. unerwünschte E-Mail-Nachrichten, die vom Dienst herausgefiltert werden. Standardmäßig weist der Dienst Spamnachrichten basierend auf der Zuverlässigkeit der IP-Adresse des Absenders zurück. Doch wenn eine Nachricht die IP-Adressüberprüfung besteht, aber von den Inhaltsfiltern als Spam eingestuft wird, dann wird die Nachricht in den Junk-E-Mail-Ordner der vorgesehenen Empfänger gesendet. 
  
> [!NOTE]
> Die Aktion, die auf Nachrichten angewendet wird, die die Inhaltsfilterung durchlaufen haben, kann mithilfe von Inhaltsfilterrichtlinien im Exchange Admin Center (EAC) konfiguriert werden (siehe [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)). Wenn Sie mit der Spameinstufung nicht einverstanden sind, können Sie Nachrichten, die Sie für Spam bzw. nicht für Spam halten, Microsoft auf mehrere Weisen melden (siehe [Übermitteln von Spam-, Nicht-Spamnachrichten und Nachrichten, die als betrügerische Phishing-Angriffe angesehen werden, an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)). 
  
 **Was ist Massen-E-Mail?**
  
Massen-E-Mail ist ein Typ von E-Mail-Nachrichten, der schwieriger zu klassifizieren ist. Während Junk-E-Mail eine ständige Bedrohung darstellt, enthalten Massen-E-Mails eine Werbe- oder Marketingbotschaft, die meist nicht wiederholt gesendet wird. Massen-E-Mail wird von einigen Benutzern gewünscht, die sich ggf. sogar absichtlich für den Empfang dieser Nachrichten angemeldet haben, während andere Benutzer diese Nachrichtentypen als Spam betrachten. Einige Benutzer möchten beispielsweise Werbe-E-Mails von der Contoso Corporation oder Einladungen zu einer bevorstehenden Konferenz zur Internetsicherheit erhalten, während für andere Benutzer diese Nachrichten Spam sind.
  
## <a name="how-to-manage-bulk-email"></a>Umgang mit Massen-E-Mails

Der Umgang mit Massen-E-Mails ist nicht ganz einfach, denn wenn alle Massen-E-Mails als Spam eingestuft werden, beschweren sich ggf. die Benutzer, die diese erhalten möchten, und melden sie als falsch positive (Nicht-Spam) Nachricht, die fälschlicherweise als Spam eingestuft wurde. Wenn sämtliche Massen-E-Mails dagegen zugelassen werden, beschweren sich ggf. die Benutzer, die diese nicht wollen, und melden sie als nicht abgefangene Spamnachricht, die fälschlicherweise in ihrem Posteingang gelandet ist.
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a>Aktivieren der erweiterten Option zur Filterung von Spam-Massensendungen

Abhängig von der Richtlinie Ihres Unternehmens für Massen-e-Mail-Nachrichten können Administratoren einen Schwellenwert für die Zuweisung der Massen-e-Mails auswählen. Die Einstellung kann über Inhaltsfilter Richtlinien in der Exchange-verwaltungsKONSOLE konfiguriert werden. AusChecken [Konfigurieren der Spamfilter Richtlinien](configure-your-spam-filter-policies.md) für die Schritte. Sie können eine Schwellenwerteinstellung von 1-9 auswählen, wobei 1 die meisten Massen-e-Mails als Spam markiert und 9 die Zustellung der meisten Massen-e-Mails zulässt. Der Dienst führt dann die konfigurierte Aktion aus, beispielsweise das Senden der Nachricht an den Junk-e-Mail-Ordner des Empfängers. 
  


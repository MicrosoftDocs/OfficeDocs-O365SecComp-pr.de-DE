---
title: Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?
ms.author: krowley
author: kccross
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
description: Kunden in einigen Fällen des Askwhat der Unterschied zwischen Junk-e-Mail und Massen-e-Mails? Der Zweck dieses Themas wird um den Unterschied zu erläutern und Informationen über die verschiedenen Optionen bereitzustellen, die für beide in Exchange Online und Exchange Online Protection (EOP) verfügbar sind.
ms.openlocfilehash: 87f946c7309589595efd3e11e998e0a9f503b651
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003154"
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

In Abhängigkeit der Richtlinie Ihres Unternehmens in Bezug auf Massen-E-Mails können Administratoren einen Schwellenwert auswählen, die der Massen-E-Mail zugewiesen wird. Die Einstellungen kann über Inhaltsfilterrichtlinien im EAC konfiguriert werden. Unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) finden Sie die entsprechenden Schritte. Sie können eine Schwellenwerteinstellung zwischen 1-9 auswählen, wobei 1 die meisten Massensendungen als Spam markiert und 9 die meisten Massensendungen als übermittelbar zulässt. Der Dienst führt dann die konfigurierte Aktion aus, z. B. das Senden der Nachricht in den Junk-E-Mail-Ordner des Empfängers. 
  


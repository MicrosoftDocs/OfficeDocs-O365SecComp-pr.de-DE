---
title: Konfigurieren der Antispamrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: Die Spamfilterung wird durch die standardmäßigen Antispamrichtlinien automatisch unternehmensweit aktiviert (Verbindungsfilter, Spamfilter und ausgehende Spamnachrichten). Als Administrator können Sie die standardmäßigen Antispamrichtlinien zwar nicht löschen, aber anzeigen und bearbeiten, sodass Sie sie optimal an die Anforderungen Ihrer Organisation anpassen können. Für eine höhere Granularität können Sie auch benutzerdefinierte Richtlinien erstellen und diese bestimmten Benutzern, Gruppen oder Domänen in Ihrer Organisation zuweisen. Standardmäßig haben die benutzerdefinierten Richtlinien Vorrang vor den Standardrichtlinien. Sie können die Prioritäten Ihrer Richtlinien jedoch verändern.
ms.openlocfilehash: ebd65050fb5a0d3862653e0279ef530fbcabc042
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215425"
---
# <a name="configure-the-anti-spam-policies"></a>Konfigurieren der Antispamrichtlinien

Die Spamfilterung wird durch die standardmäßigen Antispamrichtlinien automatisch unternehmensweit aktiviert (Verbindungsfilter, Spamfilter und ausgehende Spamnachrichten). Als Administrator können Sie die standardmäßigen Antispamrichtlinien zwar nicht löschen, aber anzeigen und bearbeiten, sodass Sie sie optimal an die Anforderungen Ihrer Organisation anpassen können. Für eine höhere Granularität können Sie auch benutzerdefinierte Richtlinien erstellen und diese bestimmten Benutzern, Gruppen oder Domänen in Ihrer Organisation zuweisen. Standardmäßig haben die benutzerdefinierten Richtlinien Vorrang vor den Standardrichtlinien. Sie können die Prioritäten Ihrer Richtlinien jedoch verändern. 
  
Weitere Informationen zum Konfigurieren der Antispamrichtlinien finden Sie unter den folgenden Themen:
  
[Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md)
  
[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Für Kunden der eigenständigen EOP-Lösung: Standardmäßig leiten die EOP-Inhaltsfilter als Spam erkannte Nachrichten an den Junk-E-Mail-Ordner der einzelnen Empfänger weiter. Damit die Aktion **Nachricht in Junk-E-Mail-Ordner verschieben** jedoch bei lokalen Postfächern angewendet wird, müssen Sie auf Ihren lokalen Servern zwei Exchange-Transportregeln konfigurieren, um Spamkopfzeilen zu erkennen, die von EOP hinzugefügt wurden. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  


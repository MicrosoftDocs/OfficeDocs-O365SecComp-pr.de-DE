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
ms.openlocfilehash: 3e972a150b70f1081cb4c3b5e3672a3acba34785
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30340966"
---
# <a name="configure-the-anti-spam-policies"></a>Konfigurieren der Antispamrichtlinien

Die Spamfilterung wird durch die standardmäßigen Antispamrichtlinien automatisch unternehmensweit aktiviert (Verbindungsfilter, Spamfilter und ausgehende Spamnachrichten). Als Administrator können Sie die standardmäßigen Antispamrichtlinien zwar nicht löschen, aber anzeigen und bearbeiten, sodass Sie sie optimal an die Anforderungen Ihrer Organisation anpassen können. Für eine höhere Granularität können Sie auch benutzerdefinierte Richtlinien erstellen und diese bestimmten Benutzern, Gruppen oder Domänen in Ihrer Organisation zuweisen. Standardmäßig haben die benutzerdefinierten Richtlinien Vorrang vor den Standardrichtlinien. Sie können die Prioritäten Ihrer Richtlinien jedoch verändern. 
  
Weitere Informationen zum Konfigurieren der Antispamrichtlinien finden Sie unter den folgenden Themen:
  
[Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md)
  
[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Für eigenständige EOP-Kunden: Standardmäßig senden die EOP-Inhaltsfilter Spam erkannte Nachrichten an den Junk-e-Mail-Ordner der Empfänger. Um jedoch sicherzustellen, dass die Aktion **Nachricht in Junk-e-Mail-Ordner verschieben** mit lokalen Postfächern funktioniert, müssen Sie zwei Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Servern konfigurieren, um die von EoP. Weitere Informationen finden Sie unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner der einzelnen Benutzer weitergeleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  


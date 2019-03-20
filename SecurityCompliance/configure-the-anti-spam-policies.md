---
title: Konfigurieren der Antispamrichtlinien
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: Die Spamfilterung wird durch die standardmäßigen Antispamrichtlinien automatisch unternehmensweit aktiviert (Verbindungsfilter, Spamfilter und ausgehende Spamnachrichten). Als Administrator können Sie die standardmäßigen Antispamrichtlinien zwar nicht löschen, aber anzeigen und bearbeiten, sodass Sie sie optimal an die Anforderungen Ihrer Organisation anpassen können. Für eine höhere Granularität können Sie auch benutzerdefinierte Richtlinien erstellen und diese bestimmten Benutzern, Gruppen oder Domänen in Ihrer Organisation zuweisen. Standardmäßig haben die benutzerdefinierten Richtlinien Vorrang vor den Standardrichtlinien. Sie können die Prioritäten Ihrer Richtlinien jedoch verändern.
ms.openlocfilehash: 992885a394031e133008f28a455383fc2f3f0616
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30691754"
---
# <a name="configure-the-anti-spam-policies"></a>Konfigurieren der Antispamrichtlinien

Die Spamfilterung wird durch die standardmäßigen Antispamrichtlinien automatisch unternehmensweit aktiviert (Verbindungsfilter, Spamfilter und ausgehende Spamnachrichten). Als Administrator können Sie die standardmäßigen Antispamrichtlinien zwar nicht löschen, aber anzeigen und bearbeiten, sodass Sie sie optimal an die Anforderungen Ihrer Organisation anpassen können. Für eine höhere Granularität können Sie auch benutzerdefinierte Richtlinien erstellen und diese bestimmten Benutzern, Gruppen oder Domänen in Ihrer Organisation zuweisen. Standardmäßig haben die benutzerdefinierten Richtlinien Vorrang vor den Standardrichtlinien. Sie können die Prioritäten Ihrer Richtlinien jedoch verändern. 
  
Weitere Informationen zum Konfigurieren der Antispamrichtlinien finden Sie unter den folgenden Themen:
  
[Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md)
  
[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Für Kunden der eigenständigen EOP-Lösung: Standardmäßig leiten die EOP-Inhaltsfilter als Spam erkannte Nachrichten an den Junk-E-Mail-Ordner der einzelnen Empfänger weiter. Um jedoch sicherzustellen, dass die Aktion **Nachricht in Junk-e-Mail-Ordner verschieben** mit lokalen Postfächern funktioniert, müssen Sie zwei Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Servern konfigurieren, um die von EoP. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md)
  


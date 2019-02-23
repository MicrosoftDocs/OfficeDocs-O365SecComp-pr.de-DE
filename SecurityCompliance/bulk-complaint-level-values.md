---
title: BCL-Werte (Bulk Complaint Level)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: Massenversender unterscheiden sich in ihren Sende-, tterns-, Inhalts Erstellungs-und Listen Erwerbs Praktiken. Einige sind gute Massenversender, die gewünschte Nachrichten mit relevanten Inhalten an Ihre Abonnenten senden. Diese Nachrichten generieren nur wenige Beschwerden von Empfängern. Andere Massenversender senden unerbetene Nachrichten, die Spam ähneln und viele Beschwerden von Empfängern auslösen. Um diese Art von Massen-e-Mailern zu unterscheiden, werden Nachrichten von Massen-e-Mailern eine BCL-Bewertung (Bulk Complaint Level) zugewiesen. BCL-Bewertungen reichen von 1 bis 9, je nachdem, wie wahrscheinlich der Massenversand ist, um Beschwerden zu generieren. Ein Absender mit einer Bewertung von BCL 9 kann viele Beschwerden von Empfängern generieren, wohingegen eine Bewertung von BCL 3 wahrscheinlich viele Reklamationen nicht generieren kann. Microsoft verwendet sowohl interne als auch Drittanbieterquellen, um Massensendungen zu identifizieren und die entsprechende BCL zu bestimmen. Diese Bewertung wird in der X-Microsoft-Antispam-Kopfzeile jeder Nachricht angezeigt. Weitere Informationen zu diesem Nachrichtenkopf finden Sie unter Antispam-Nachrichtenkopfzeilen.
ms.openlocfilehash: 9947c0f36681126748e8617d67116c6932209760
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222924"
---
# <a name="bulk-complaint-level-values"></a>BCL-Werte (Bulk Complaint Level)

Versender von Massen-E-Mails arbeiten mit verschiedenen Sendemustern, Inhalterstellungsverfahren und Listenbeschaffungsarten. Einige von ihnen sind gute Absender, die erwünschte Nachrichten mit relevantem Inhalt an Ihre Abonnenten senden. Diese Nachrichten führen zu wenigen Beschwerden von Empfängern. Andere Absender verwenden unerwünschte Nachrichten, die den Kriterien für Spam sehr nahekommen und zu vielen Beschwerden von Empfängern führen. Um zwischen diesen Typen von Massen-E-Mail-Absendern zu unterscheiden, werden ihren Nachrichten BCL-Bewertungen (Bulk Complaint Level) zugewiesen. BCL-Bewertungen können zwischen 1 und 9 liegen - je nachdem, wie wahrscheinlich es ist, dass die Massen-E-Mail zu Beschwerden führen. Ein Absender mit dem BCL-Wert 9 wird wahrscheinlich mehr Beschwerden von Empfängern erhalten, was mit einem BCL-Wert von 3 wahrscheinlich nicht der Fall ist. Microsoft arbeitet sowohl mit internen Quellen als auch mit Quellen von Drittanbietern, um die Absender von Massen-E-Mails zu identifizieren und den passenden BCL-Wert zu bestimmen. Diese Bewertung wird in der **X-Microsoft-Antispam**-Kopfzeile jeder Nachricht angezeigt. Weitere Informationen zu dieser Nachrichtenkopfzeile finden Sie unter [Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md). 
  
Sie können BCL-Werte verwenden, um die für Ihre Organisation gewünschte Massenfilterungsebene festzulegen, indem Sie die Schritte unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) befolgen.
  
Weitere BCL-Werte werden hinzugefügt und hier in Zukunft eingeschlossen. In der folgenden Tabelle werden die aktuell verwendeten BCL-Werte aufgelistet und beschrieben.
  
|||
|:-----|:-----|
|**BCL-Wert** <br/> |**Beschreibung** <br/> |
|0  <br/> |Die Nachricht stammt nicht von einem Massen-E-Mail-Absender.  <br/> |
|1, 2, 3  <br/> |Die Nachricht stammt von einem Massen-E-Mail-Absender, aber führt zu wenigen Beschwerden.  <br/> |
|4, 5, 6, 7  <br/> |Die Nachricht stammt von einem Massen-E-Mail-Absender und führt zu einer gemischten Anzahl von Beschwerden.  <br/> |
|8, 9  <br/> |Die Nachricht stammt von einem Massen-E-Mail-Absender und führt zu einer hohen Anzahl von Beschwerden.  <br/> |
   


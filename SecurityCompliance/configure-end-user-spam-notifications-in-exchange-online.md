---
title: Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Inhaltsfilterrichtlinie oder für benutzerdefinierte Inhaltsfilterrichtlinien, die auf Domänen angewendet werden, konfigurieren.
ms.openlocfilehash: da370497f78d7f253276c908061a9a80e2f74938
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002745"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online

> [!IMPORTANT]
> Dieses Thema ist für Exchange Online-Postfächer schützen Kunden. Exchange Online Protection (EOP) Standalone-Kunden, die Schützen von lokalen Postfächern sollten stattdessen das folgende Thema lesen: [Configure End-User Spam Notifications in EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Inhaltsfilterrichtlinie oder für benutzerdefinierte Inhaltsfilterrichtlinien, die auf Domänen angewendet werden, konfigurieren. Wenn Sie Spambenachrichtigungen für Endbenutzer aktivieren, können Ihre Endbenutzer ihre Nachrichten in der Spamquarantäne selbst verwalten. Spambenachrichtigungen für Endbenutzer können nicht bei Richtlinien angewendet werden, die auf Benutzer oder Gruppen oder eine Richtlinie mit Ausnahmen angewendet werden.
  
Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.
  
Nach dem Empfang einer Benachrichtigung, Endbenutzer können klicken, um die Spam-e-Mail-in ihren Posteingang zu verschieben, oder Bericht Spam per e-Mail als keine Junk, in diesem Fall wird auf der Microsoft-Spamanalyseteam gesendet werden. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten
  
Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Inhaltsfilter**.
    
2. Wählen Sie die Inhaltsfilterrichtlinie aus, für die Sie Spambenachrichtigungen für Endbenutzer aktivieren möchten (sie sind standardmäßig deaktiviert).
    
3. Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren). 
    
4. Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:
    
1. **Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.) 
    
2. **Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden. 
    
3. **Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen. 
    
5. Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Inhaltsfilter-Richtlinieneinstellungen angezeigt, einschließlich der Einstellungen für Endbenutzer-Spambenachrichtigungen.
    
> [!NOTE]
>  Spambenachrichtigungen für Endbenutzer können nur bei Inhaltsfilterrichtlinien verwendet werden, die aktiviert sind. >  Spam Endbenutzerbenachrichtigungen sind nur einmal pro Tag versendet. Die Zustellungszeit der Benachrichtigung kann für einen bestimmten Kunden nicht garantiert werden und kann nicht konfiguriert werden. 
  
 **Tipp:** Wenn Sie Spambenachrichtigungen für Endbenutzer testen möchten, indem Sie sie an eine begrenzte Gruppe von Benutzern senden, bevor Sie sie implementieren, erstellen Sie eine benutzerdefinierte Inhaltsfilterrichtlinie, die Spambenachrichtigungen für Endbenutzer für die Domänen aktiviert, in denen sich die Benutzer befinden. Erstellen Sie anschließend in der EAC unter **Nachrichtenfluss \> Regeln** eine Transportregel, um Nachrichten von quarantine@messaging.microsoft.com (der E-Mail-Adresse, die Benachrichtigungen sendet) mit Ausnahmen für Benutzer, die die Benachrichtigungen erhalten sollen, zu blockieren. Die folgende Abbildung zeigt ein Beispiel für die Erstellung einer Ausnahme für zwei Benutzer (SaraD and AlexD) in der Domäne Contoso.com: 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Weitere Informationen

[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  
---
title: Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
ms.collection:
- M365-security-compliance
description: Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Spamfilter Richtlinie oder für benutzerdefinierte Spamfilter Richtlinien konfigurieren, die auf Domänen angewendet werden.
ms.openlocfilehash: 00ce151ab355efb419d483a17aaeeb26dfc71c0d
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699280"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online

> [!IMPORTANT]
> Dieses Thema richtet sich an Exchange Online-Kunden, die cloudgehostete Postfächer schützen. Selbstständige Kunden mit Exchange Online Protection (EoP), die lokale Postfächer schützen, sollten stattdessen das folgende Thema lesen: [configure End-User Spam Notifications in EoP](configure-end-user-spam-notifications-in-eop.md). 
  
Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Spamfilter Richtlinie oder für benutzerdefinierte Spamfilter Richtlinien konfigurieren, die auf Domänen angewendet werden. Wenn Sie Spambenachrichtigungen für Endbenutzer aktivieren, können Ihre Endbenutzer ihre Nachrichten in der Spamquarantäne selbst verwalten. Spambenachrichtigungen für Endbenutzer können nicht bei Richtlinien angewendet werden, die auf Benutzer oder Gruppen oder eine Richtlinie mit Ausnahmen angewendet werden.
  
Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.
  
Nach dem Empfang einer Benachrichtigung können Endbenutzer eine der folgenden Optionen auswählen:

Zeigen Sie **eine Vorschau** der Nachricht an, wenn Sie eine Vorschau des Inhalts oder des Headers vor dem Ausführen der Aktion anzeigen möchten.

**Laden** Sie die Nachricht herunter, wenn Sie die Nachricht und Anlagen (falls vorhanden) auf Ihrem Gerät überprüfen möchten, bevor Sie Maßnahmen ergreifen.

**Release** wenn es sich bei der Nachricht nicht um Spam handelt und Sie möchten, dass Office 365 die Nachricht an Ihr Postfach sendet.

**Freigabe #a0 Absender zulassen** , wenn die Nachricht kein Spam ist, und Sie möchten, dass Office 365 den Absender zu Ihrer Liste sicherer Absender und Empfänger für zukünftige e-Mails hinzufügen. Beachten Sie, dass Ihr Administrator möglicherweise andere organisationsweite Allow/Block-Konfigurationen hat, die Ihre Liste sicherer Absender außer Kraft setzen.

Geben Sie **#a0 Bericht frei**, wenn es sich bei der Nachricht nicht um Spam handelt und Sie die Nachricht an Ihr Postfach senden und an Microsoft zur Analyse melden möchten.

**Blockieren** Sie, wenn Office 365 den Absender zu Ihrer Liste blockierter Absender hinzufügen möchten.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten
  
Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Anti-Spam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen, die möglicherweise für die Verfahren in diesem Thema gelten, finden Sie unter [Tastenkombinationen für das Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spamfilter**.
    
2. Wählen Sie die Spamfilter Richtlinie aus, für die Sie Spambenachrichtigungen für Endbenutzer aktivieren möchten (Sie sind standardmäßig deaktiviert).
    
3. Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren). 
    
4. Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:
    
1. **Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.) 
    
2. **Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden. 
    
3. **Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen. 
    
5. Klicken Sie auf **Speichern**. Eine Zusammenfassung der Einstellungen für Spamfilter Richtlinien, einschließlich der Einstellungen für Spambenachrichtigungen für Endbenutzer, wird im rechten Bereich angezeigt.
    
> [!NOTE]
>  Spambenachrichtigungen für Endbenutzer sind nur für aktivierte Spamfilter Richtlinien funktionsfähig. >  Spam Endbenutzerbenachrichtigungen sind nur einmal pro Tag versendet. Die Zustellungszeit der Benachrichtigung kann für einen bestimmten Kunden nicht garantiert werden und kann nicht konfiguriert werden. 
  
 **Tipp:** Wenn Sie Spambenachrichtigungen für Endbenutzer testen möchten, indem Sie Sie an eine beschränkte Gruppe von Benutzern senden, bevor Sie sie vollständig implementieren, erstellen Sie eine benutzerdefinierte Spamfilter Richtlinie, die Endbenutzer-Spambenachrichtigungen für die Domänen ermöglicht, in denen sich die Benutzer befinden. Erstellen Sie dann in der Exchange-Verwaltungskonsole unter **Nachrichtenfluss \> Regeln**eine Nachrichtenfluss Regel (auch als Transportregel bezeichnet), um Nachrichten von Quarantine@Messaging.Microsoft.com (die e-Mail-Adresse, die Benachrichtigungen sendet) mit Ausnahmen für die Benutzer zu blockieren, die Sie möchten. , um die Benachrichtigungen zu empfangen. Die folgende Abbildung zeigt ein Beispiel für die Erstellung einer Ausnahme für zwei Benutzer (SaraD and AlexD) in der Domäne Contoso.com: 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Weitere Informationen

[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  

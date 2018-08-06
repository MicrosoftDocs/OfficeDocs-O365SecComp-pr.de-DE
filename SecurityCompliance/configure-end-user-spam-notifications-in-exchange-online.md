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
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Sie können Konfigurieren von spambenachrichtigungen für die Standardrichtlinie für unternehmensweite Spam-Filter oder benutzerdefinierte Spam-Filter-Richtlinien, die auf Domänen angewendet werden.
ms.openlocfilehash: 4a4c7c6b139fe0f8b0a1f6b69c1b95e321293af5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027532"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online

> [!IMPORTANT]
> Dieses Thema ist für Exchange Online-Postfächer schützen Kunden. Exchange Online Protection (EOP) Standalone-Kunden, die Schützen von lokalen Postfächern sollten stattdessen das folgende Thema lesen: [Configure End-User Spam Notifications in EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Sie können Konfigurieren von spambenachrichtigungen für die Standardrichtlinie für unternehmensweite Spam-Filter oder benutzerdefinierte Spam-Filter-Richtlinien, die auf Domänen angewendet werden. Spambenachrichtigungen aktiviert werden, können die Endbenutzer ihre eigenen Nachrichten in Spam-Quarantäne selbst verwalten. Spambenachrichtigungen können nicht mit den Benutzern oder Gruppen oder auf eine Richtlinie mit Ausnahmen angewendeten Richtlinien verwendet werden.
  
Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.
  
Nach dem Empfang einer Benachrichtigung, Endbenutzer können klicken, um die Spam-e-Mail-in ihren Posteingang zu verschieben, oder Bericht Spam per e-Mail als keine Junk, in diesem Fall wird auf der Microsoft-Spamanalyseteam gesendet werden. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten
  
Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole

1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spamfilter**.
    
2. Wählen Sie die Spam-Filter-Richtlinie für die End-User Spam Notifications aktivieren (sie sind standardmäßig deaktiviert) werden soll.
    
3. Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren). 
    
4. Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:
    
1. **Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.) 
    
2. **Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden. 
    
3. **Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen. 
    
5. Klicken Sie auf **Speichern**. Eine Zusammenfassung der Richtlinieneinstellungen für Ihre Spam-Filter Ihre Benachrichtigung-Einstellungen Endbenutzer Spam, einschließlich im rechten Bereich angezeigt wird.
    
> [!NOTE]
>  Spambenachrichtigungen werden nur für Spam-Filterrichtlinien funktionsfähig sein, die aktiviert sind. > Spambenachrichtigungen sind nur einmal pro Tag versendet. Die Zeit der Zustellung der Benachrichtigung kann nicht garantiert werden, für bestimmte kundenspezifischen und ist nicht konfigurierbar. 
  
 **Tipp:** Wenn Sie spambenachrichtigungen testen, indem Sie sie an eine begrenzte Auswahl von Benutzern gesendet werden, bevor Sie vollständig zu implementieren möchten, erstellen Sie eine benutzerdefinierte Spam-Filter-Richtlinie, die spambenachrichtigungen für die Domänen ermöglicht, in denen die Benutzer befinden. Klicken Sie dann in der Exchange-Verwaltungskonsole unter **E-Mail-Fluss \> Regeln**, erstellen Sie eine Transportregel zum Blockieren von Nachrichten aus quarantine@messaging.microsoft.com (die e-Mail-Adresse, die Benachrichtigung sendet) mit Ausnahmen für die Benutzer, die Sie an die Benachrichtigungen erhalten möchten. In der folgenden Abbildung ist ein Beispiel für eine Ausnahme für zwei Benutzer (SaraD und AlexD) zu erstellen, von der Domäne "contoso.com": 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Weitere Informationen

[Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)
  

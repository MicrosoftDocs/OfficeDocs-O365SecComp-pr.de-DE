---
title: Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Sie können Konfigurieren von spambenachrichtigungen für die Standardrichtlinie für unternehmensweite Spam-Filter oder benutzerdefinierte Spam-Filter-Richtlinien, die auf Domänen angewendet werden.
ms.openlocfilehash: 77ca32224cecaca2f558119db909ad74fdb6e858
ms.sourcegitcommit: cc8550452d099b4c5852c6559f6ca94a77f1d93b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2018
ms.locfileid: "27134769"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="25ae4-103">Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="25ae4-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25ae4-p101">Dieses Thema ist für Exchange Online-Postfächer schützen Kunden. Exchange Online Protection (EOP) Standalone-Kunden, die Schützen von lokalen Postfächern sollten stattdessen das folgende Thema lesen: [Configure End-User Spam Notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="25ae4-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="25ae4-p102">Sie können Konfigurieren von spambenachrichtigungen für die Standardrichtlinie für unternehmensweite Spam-Filter oder benutzerdefinierte Spam-Filter-Richtlinien, die auf Domänen angewendet werden. Spambenachrichtigungen aktiviert werden, können die Endbenutzer ihre eigenen Nachrichten in Spam-Quarantäne selbst verwalten. Spambenachrichtigungen können nicht mit den Benutzern oder Gruppen oder auf eine Richtlinie mit Ausnahmen angewendeten Richtlinien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="25ae4-p103">Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="25ae4-111">Endbenutzer können nach dem Empfang einer Benachrichtigung, aus den folgenden Optionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="25ae4-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="25ae4-112">**Vorschau** der Nachricht, wenn Sie eine Vorschau des Inhalts oder der Header vor der Aktion anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="25ae4-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="25ae4-113">**Laden Sie** die Nachricht, wenn Sie die Nachricht und Anlagen (falls vorhanden) auf dem Gerät vor der Aktion überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="25ae4-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="25ae4-114">**Version** Wenn die Nachricht ist nicht-Spam- und Office 365 ein, um die Nachricht an Ihr Postfach senden möchten.</span><span class="sxs-lookup"><span data-stu-id="25ae4-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="25ae4-p104">**Version & Absender zulassen** , wenn die Nachricht ist nicht-Spam- und Office 365 ein, um den Absender Ihrer sicherer Absender und Empfänger für zukünftige e-Mails hinzufügen möchten. Beachten Sie, dass Ihre Admin andere Organisation breit zulassen/blockieren-Konfigurationen, die die Liste der sicheren Absender überschreiben möglicherweise beibehalten.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p104">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails. Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="25ae4-117">**Version & Bericht**, wenn die Nachricht Spam und Sie nicht möchten, senden die Nachricht an Ihr Postfach und zur Analyse an Microsoft melden.</span><span class="sxs-lookup"><span data-stu-id="25ae4-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="25ae4-118">**Blockieren** , wenn Sie Office 365 an den Absender zur Liste blockierter Absender hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="25ae4-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="25ae4-119">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="25ae4-119">What do you need to know before you begin?</span></span>

<span data-ttu-id="25ae4-120">Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten</span><span class="sxs-lookup"><span data-stu-id="25ae4-120">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="25ae4-p105">Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25ae4-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="25ae4-123">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="25ae4-123">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="25ae4-124">Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="25ae4-124">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="25ae4-125">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spamfilter**.</span><span class="sxs-lookup"><span data-stu-id="25ae4-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="25ae4-126">Wählen Sie die Spam-Filter-Richtlinie für die End-User Spam Notifications aktivieren (sie sind standardmäßig deaktiviert) werden soll.</span><span class="sxs-lookup"><span data-stu-id="25ae4-126">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="25ae4-127">Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren).</span><span class="sxs-lookup"><span data-stu-id="25ae4-127">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="25ae4-128">Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="25ae4-128">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="25ae4-p106">**Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.)</span><span class="sxs-lookup"><span data-stu-id="25ae4-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="25ae4-p107">**Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="25ae4-135">**Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25ae4-135">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="25ae4-p108">Klicken Sie auf **Speichern**. Eine Zusammenfassung der Richtlinieneinstellungen für Ihre Spam-Filter Ihre Benachrichtigung-Einstellungen Endbenutzer Spam, einschließlich im rechten Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p108">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="25ae4-p109">Spambenachrichtigungen werden nur für Spam-Filterrichtlinien funktionsfähig sein, die aktiviert sind. > Spambenachrichtigungen sind nur einmal pro Tag versendet. Die Zeit der Zustellung der Benachrichtigung kann nicht garantiert werden, für bestimmte kundenspezifischen und ist nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="25ae4-p109">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="25ae4-p110">**Tipp:** Wenn Sie spambenachrichtigungen testen, indem Sie sie an eine begrenzte Auswahl von Benutzern gesendet werden, bevor Sie vollständig zu implementieren möchten, erstellen Sie eine benutzerdefinierte Spam-Filter-Richtlinie, die spambenachrichtigungen für die Domänen ermöglicht, in denen die Benutzer befinden. Klicken Sie dann in der Exchange-Verwaltungskonsole unter **E-Mail-Fluss \> Regeln**, erstellen Sie eine Transportregel zum Blockieren von Nachrichten aus quarantine@messaging.microsoft.com (die e-Mail-Adresse, die Benachrichtigung sendet) mit Ausnahmen für die Benutzer, die Sie an die Benachrichtigungen erhalten möchten. In der folgenden Abbildung ist ein Beispiel für eine Ausnahme für zwei Benutzer (SaraD und AlexD) zu erstellen, von der Domäne "contoso.com":</span><span class="sxs-lookup"><span data-stu-id="25ae4-p110">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="25ae4-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25ae4-145">For more information</span></span>

[<span data-ttu-id="25ae4-146">Konfigurieren von Spamfilterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="25ae4-146">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  

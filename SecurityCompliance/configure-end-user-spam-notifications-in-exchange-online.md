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
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="3f34d-103">Konfigurieren von Spambenachrichtigungen für Endbenutzer in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3f34d-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f34d-p101">Dieses Thema ist für Exchange Online-Postfächer schützen Kunden. Exchange Online Protection (EOP) Standalone-Kunden, die Schützen von lokalen Postfächern sollten stattdessen das folgende Thema lesen: [Configure End-User Spam Notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="3f34d-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="3f34d-p102">Sie können Konfigurieren von spambenachrichtigungen für die Standardrichtlinie für unternehmensweite Spam-Filter oder benutzerdefinierte Spam-Filter-Richtlinien, die auf Domänen angewendet werden. Spambenachrichtigungen aktiviert werden, können die Endbenutzer ihre eigenen Nachrichten in Spam-Quarantäne selbst verwalten. Spambenachrichtigungen können nicht mit den Benutzern oder Gruppen oder auf eine Richtlinie mit Ausnahmen angewendeten Richtlinien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f34d-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="3f34d-p103">Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3f34d-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="3f34d-111">Nach dem Empfang einer Benachrichtigung, Endbenutzer können klicken, um die Spam-e-Mail-in ihren Posteingang zu verschieben, oder Bericht Spam per e-Mail als keine Junk, in diesem Fall wird auf der Microsoft-Spamanalyseteam gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f34d-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="3f34d-112">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="3f34d-112">What do you need to know before you begin?</span></span>

<span data-ttu-id="3f34d-113">Geschätzte Zeit bis zum Abschließen des Vorgangs: 2 Minuten</span><span class="sxs-lookup"><span data-stu-id="3f34d-113">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="3f34d-p104">Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter den Eintrag "AntiSpam" im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3f34d-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="3f34d-116">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="3f34d-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="3f34d-117">Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3f34d-117">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="3f34d-118">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Spamfilter**.</span><span class="sxs-lookup"><span data-stu-id="3f34d-118">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="3f34d-119">Wählen Sie die Spam-Filter-Richtlinie für die End-User Spam Notifications aktivieren (sie sind standardmäßig deaktiviert) werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f34d-119">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="3f34d-120">Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren).</span><span class="sxs-lookup"><span data-stu-id="3f34d-120">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="3f34d-121">Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="3f34d-121">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="3f34d-p105">**Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.)</span><span class="sxs-lookup"><span data-stu-id="3f34d-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="3f34d-p106">**Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f34d-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="3f34d-128">**Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f34d-128">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="3f34d-p107">Klicken Sie auf **Speichern**. Eine Zusammenfassung der Richtlinieneinstellungen für Ihre Spam-Filter Ihre Benachrichtigung-Einstellungen Endbenutzer Spam, einschließlich im rechten Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f34d-p107">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="3f34d-p108">Spambenachrichtigungen werden nur für Spam-Filterrichtlinien funktionsfähig sein, die aktiviert sind. > Spambenachrichtigungen sind nur einmal pro Tag versendet. Die Zeit der Zustellung der Benachrichtigung kann nicht garantiert werden, für bestimmte kundenspezifischen und ist nicht konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="3f34d-p108">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="3f34d-p109">**Tipp:** Wenn Sie spambenachrichtigungen testen, indem Sie sie an eine begrenzte Auswahl von Benutzern gesendet werden, bevor Sie vollständig zu implementieren möchten, erstellen Sie eine benutzerdefinierte Spam-Filter-Richtlinie, die spambenachrichtigungen für die Domänen ermöglicht, in denen die Benutzer befinden. Klicken Sie dann in der Exchange-Verwaltungskonsole unter **E-Mail-Fluss \> Regeln**, erstellen Sie eine Transportregel zum Blockieren von Nachrichten aus quarantine@messaging.microsoft.com (die e-Mail-Adresse, die Benachrichtigung sendet) mit Ausnahmen für die Benutzer, die Sie an die Benachrichtigungen erhalten möchten. In der folgenden Abbildung ist ein Beispiel für eine Ausnahme für zwei Benutzer (SaraD und AlexD) zu erstellen, von der Domäne "contoso.com":</span><span class="sxs-lookup"><span data-stu-id="3f34d-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="3f34d-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f34d-138">For more information</span></span>

[<span data-ttu-id="3f34d-139">Konfigurieren von Spamfilterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3f34d-139">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  

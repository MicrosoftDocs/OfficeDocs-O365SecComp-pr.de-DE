---
title: Konfigurieren von Spambenachrichtigungen für Endbenutzer in EOP
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
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Inhaltsfilterrichtlinie oder für benutzerdefinierte Inhaltsfilterrichtlinien, die auf Domänen angewendet werden, konfigurieren.
ms.openlocfilehash: 87a55de49a01c69f3392a3740e19e52630f4dcc8
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341296"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="d13ba-103">Konfigurieren von Spambenachrichtigungen für Endbenutzer in EOP</span><span class="sxs-lookup"><span data-stu-id="d13ba-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d13ba-p101">Dieses Thema richtet sich an eigenständige Exchange Online Protection (EOP)-Kunden, die lokale Postfächer schützen. Exchange Online-Kunden, die in der Cloud gehostete Postfächer schützen, sollten stattdessen das folgende Thema lesen: [configure End-User Spam Notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="d13ba-p101">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes. Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="d13ba-p102">Sie können Spambenachrichtigungen für Endbenutzer für die standardmäßige unternehmensweite Inhaltsfilterrichtlinie oder für benutzerdefinierte Inhaltsfilterrichtlinien, die auf Domänen angewendet werden, konfigurieren. Wenn Sie Spambenachrichtigungen für Endbenutzer aktivieren, können Ihre Endbenutzer ihre Nachrichten in der Spamquarantäne selbst verwalten. Spambenachrichtigungen für Endbenutzer können nicht bei Richtlinien angewendet werden, die auf Benutzer oder Gruppen oder eine Richtlinie mit Ausnahmen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="d13ba-p103">Spambenachrichtigungen für Endbenutzer enthalten eine Liste aller Nachrichten in der Spamquarantäne, die der Endbenutzer in dem von Ihnen konfigurierten Zeitraum (zwischen 1 und 15 Tagen) erhalten hat. Sie können auch die Sprache festlegen, in der die Benachrichtigung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="d13ba-111">Nach dem Empfang einer Benachrichtigung können Endbenutzer aus den folgenden Optionen wählen:</span><span class="sxs-lookup"><span data-stu-id="d13ba-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="d13ba-112">Zeigen Sie eine **Vorschau** der Nachricht an, wenn Sie eine Vorschau des Inhalts oder der Kopfzeile vor der Aktion anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d13ba-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="d13ba-113">**Laden** Sie die Nachricht herunter, wenn Sie die Nachricht und die Anhänge (falls vorhanden) auf Ihrem Gerät vor der Aktion überarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d13ba-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="d13ba-114">**Release** , wenn es sich bei der Nachricht nicht um Spam handelt und Sie möchten, dass Office 365 die Nachricht an Ihr Postfach sendet.</span><span class="sxs-lookup"><span data-stu-id="d13ba-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="d13ba-p104">**Release _AMP_ Allow Absender** , wenn die Nachricht nicht Spam ist und Sie möchten, dass Office 365 den Absender zur Liste sicherer Absender und Empfänger für zukünftige e-Mails hinzufügt. Denken Sie daran, dass Ihr Administrator möglicherweise andere organisationsweite Allow/Block-Konfigurationen besitzt, die Ihre Liste sicherer Absender außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p104">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails. Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="d13ba-117">**Veröffentlichen Sie _AMP_ Bericht**, wenn es sich bei der Nachricht nicht um Spam handelt und Sie die Nachricht an Ihr Postfach senden und zu Analyseberichten möchten.</span><span class="sxs-lookup"><span data-stu-id="d13ba-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="d13ba-118">**Blockieren** Wenn Sie möchten, dass Office 365 den Absender zu Ihrer Liste blockierter Absender hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d13ba-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d13ba-119">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="d13ba-119">What do you need to know before you begin?</span></span>
<span data-ttu-id="d13ba-120"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d13ba-120"></span></span>

<span data-ttu-id="d13ba-121">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="d13ba-121">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="d13ba-p105">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Antispam" im Thema [Featureberechtigungen in EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="d13ba-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](eop/feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="d13ba-124">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="d13ba-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="d13ba-125">Konfigurieren von Spambenachrichtigungen für Endbenutzer über die Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="d13ba-125">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="d13ba-126">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Inhaltsfilter**.</span><span class="sxs-lookup"><span data-stu-id="d13ba-126">In the Exchange admin center (EAC), navigate to **Protection** \> **Content filter**.</span></span>
    
2. <span data-ttu-id="d13ba-127">Wählen Sie die Inhaltsfilterrichtlinie aus, für die Sie Spambenachrichtigungen für Endbenutzer aktivieren möchten (sie sind standardmäßig deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="d13ba-127">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="d13ba-128">Klicken Sie im rechten Teilfenster, in dem eine Übersicht über Ihre Richtlinie angezeigt wird, auf den Link **Configure End-user spam notifications** (Spambenachrichtigungen für Endbenutzer konfigurieren).</span><span class="sxs-lookup"><span data-stu-id="d13ba-128">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="d13ba-129">Konfigurieren Sie im daraufhin angezeigten Dialogfeld die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d13ba-129">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="d13ba-p106">**Enable end-user spam notifications** (Spambenachrichtigungen für Endbenutzer aktivieren) Markieren Sie dieses Kontrollkästchen, um Benachrichtigungen an Endbenutzer für diese Richtlinie zu aktivieren. (Wenn diese Richtlinie aktiviert ist, können Sie auf das Kontrollkästchen klicken, um Spambenachrichtigungen an Endbenutzer für diese Richtlinie zu deaktivieren.)</span><span class="sxs-lookup"><span data-stu-id="d13ba-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="d13ba-p107">**Send end-user spam notifications every (days)** (Spambenachrichtigungen an Endbenutzer senden alle ... Tage) Gibt an, wie oft Spambenachrichtigungen an Endbenutzer gesendet werden sollen. Der Standardwert beträgt 3 Tage. Sie können zwischen 1 und 15 Tagen angeben. Wenn Sie beispielsweise 7 Tage angeben, enthält die Benachrichtigung eine Liste aller Nachrichten der letzten 7 Tage für diesen Benutzer, die stattdessen in die Spamquarantäne verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="d13ba-136">**Notification language** (Benachrichtigungssprache) Wählen Sie in der Dropdown-Liste die Sprache aus, in der Endbenutzer-Spambenachrichtigungen für diese Richtlinie geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d13ba-136">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="d13ba-p108">Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Inhaltsfilter-Richtlinieneinstellungen angezeigt, einschließlich der Einstellungen für Endbenutzer-Spambenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p108">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="d13ba-p109">Spambenachrichtigungen für Endbenutzer können nur bei Inhaltsfilterrichtlinien verwendet werden, die aktiviert sind. >  Spam Endbenutzerbenachrichtigungen sind nur einmal pro Tag versendet. Die Zustellungszeit der Benachrichtigung kann für einen bestimmten Kunden nicht garantiert werden und kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d13ba-p109">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="d13ba-p110">**Tipp:** Wenn Sie Spambenachrichtigungen für Endbenutzer testen möchten, indem Sie Sie an eine begrenzte Anzahl von Benutzern senden, bevor Sie sie vollständig implementieren, erstellen Sie eine benutzerdefinierte Inhaltsfilter Richtlinie, mit der Endbenutzer-Spambenachrichtigungen für die Domänen aktiviert werden, in denen sich die Benutzer befinden. Erstellen Sie dann in der Exchange-verwaltungsKONSOLE unter **Nachrichtenfluss \> Regeln**eine e-Mail-Fluss Regel (auch als Transportregel bezeichnet), um Nachrichten von Quarantine@messaging.microsoft.com (die e-Mail-Adresse, die Benachrichtigungen sendet) mit Ausnahmen für die gewünschten Benutzer zu blockieren. , um die Benachrichtigungen zu empfangen. Die folgende Abbildung ist ein Beispiel für das Erstellen einer Ausnahme für zwei Benutzer (Sarad und ALEXD) aus der Domänen Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="d13ba-p110">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a mail flow rule (also known as a transport rule) to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Transportregel zum Testen von Spambenachrichtigungen für Endbenutzer](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="d13ba-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d13ba-146">For more information</span></span>

[<span data-ttu-id="d13ba-147">Konfigurieren von Spamfilterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d13ba-147">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  

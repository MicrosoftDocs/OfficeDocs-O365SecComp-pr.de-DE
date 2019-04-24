---
title: Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
ms.collection:
- M365-security-compliance
description: Informiert Office 365-und EOP-Administratoren über die Aktivierung und Deaktivierung von Sicherheitstipps in e-Mail-Nachrichten.
ms.openlocfilehash: 9be9c4cd7fc8e94208aac2ad8812c93a3465f58b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256948"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="b0a45-103">Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365</span><span class="sxs-lookup"><span data-stu-id="b0a45-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="b0a45-104">Exchange Online Protection (EOP) fügt einen Sicherheitstipp für von ihm übermittelte e-Mail-Nachrichten hinzu oder stempelt diesen.</span><span class="sxs-lookup"><span data-stu-id="b0a45-104">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers.</span></span> <span data-ttu-id="b0a45-105">Diese Sicherheitstipps bieten den Empfängern eine schnelle und visuelle Möglichkeit, um festzustellen, ob eine Nachricht von einem sicheren, überprüften Absender stammt, wenn die Nachricht von Office 365 als Spam gekennzeichnet wurde, wenn die Nachricht etwas Verdächtiges enthält, beispielsweise einen Phishing-Betrug, oder wenn externe Bilder blockiert.</span><span class="sxs-lookup"><span data-stu-id="b0a45-105">These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked.</span></span> <span data-ttu-id="b0a45-106">Office 365-und EOP-eigenständige Administratoren können eine Spam Richtlinieneinstellung bearbeiten, um zu aktivieren oder zu deaktivieren, dass Sicherheitstipps in Outlook und anderen Desktop-e-Mail-Clients in e-Mails angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0a45-106">Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="b0a45-107">Office 365 ermöglicht Sicherheitstipps standardmäßig für Ihre Organisation, und es wird empfohlen, dass Sie aktiviert bleiben, um Spam-und Phishing-Angriffe zu bekämpfen.</span><span class="sxs-lookup"><span data-stu-id="b0a45-107">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks.</span></span> <span data-ttu-id="b0a45-108">Sie können Sicherheitstipps für Outlook im Web nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0a45-108">You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="b0a45-109">Beispiele und Informationen zu den in Sicherheitstipps angezeigten Daten finden Sie unter [Sicherheitstipps in e-Mail-Nachrichten in Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="b0a45-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="b0a45-110">Inhalt dieses Themas:</span><span class="sxs-lookup"><span data-stu-id="b0a45-110">In this topic:</span></span>
  
- [<span data-ttu-id="b0a45-111">So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe des Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="b0a45-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="b0a45-112">So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0a45-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="b0a45-113">So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe des Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="b0a45-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="b0a45-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="b0a45-114"></span></span>

1. <span data-ttu-id="b0a45-115">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="b0a45-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="b0a45-116">Melden Sie sich mit Ihrem Geschäfts- oder Schulkonto bei Office 365 an.</span><span class="sxs-lookup"><span data-stu-id="b0a45-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="b0a45-117">Wählen Sie **Richtlinie**für die **Bedrohungs Verwaltung** \> aus.</span><span class="sxs-lookup"><span data-stu-id="b0a45-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="b0a45-118">Wählen Sie auf der Seite **Richtlinie** die Option **Antispam**aus.</span><span class="sxs-lookup"><span data-stu-id="b0a45-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![Dieser Screenshot zeigt, wie Sie im Security &amp; Compliance Center auf die Seite Anti-Spam-Einstellungen gelangen.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="b0a45-120">Klicken Sie auf der Seite **Anti-Spam-Einstellungen** auf die Registerkarte **Benutzerdefiniert** .</span><span class="sxs-lookup"><span data-stu-id="b0a45-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![Dieser Screenshot zeigt den Speicherort der benutzerdefinierten Registerkarte auf der Seite Anti-Spam-Einstellungen im &amp; Security Compliance Center.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="b0a45-122">Falls erforderlich, wählen Sie die Option **benutzerdefinierte Einstellungen** aus, um benutzerdefinierte Einstellungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0a45-122">If necessary, choose the **Custom settings** switch to turn on custom settings.</span></span> <span data-ttu-id="b0a45-123">Wenn die Option benutzerdefinierte Einstellungen auf **aus**festgelegt ist, können Sie keine Spamfilter Richtlinien ändern.</span><span class="sxs-lookup"><span data-stu-id="b0a45-123">If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![Dieser Screenshot zeigt, dass benutzerdefinierte Anti-Spam-Filterrichtlinien Einstellungen deaktiviert wurden.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="b0a45-125">Erweitern Sie die zu ändernde Spam Richtlinie, und wählen Sie dann **Richtlinie bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="b0a45-125">Expand the spam policy you want to modify and then choose **Edit policy**.</span></span> <span data-ttu-id="b0a45-126">Wählen Sie beispielsweise den Pfeil nach unten neben **Standardrichtlinie für Spamfilter**aus.</span><span class="sxs-lookup"><span data-stu-id="b0a45-126">For example, choose the down arrow next to **Default spam filter policy**.</span></span> <span data-ttu-id="b0a45-127">Sie können auch eine neue Richtlinie erstellen, indem Sie **eine Richtlinie hinzufügen**auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0a45-127">Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="b0a45-128">Erweitern Sie **Spam-und Massen** Aktionen.</span><span class="sxs-lookup"><span data-stu-id="b0a45-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="b0a45-129">Aktivieren Sie zur Aktivierung von Sicherheitstipps unter **Sicherheitstipps**das Kontrollkästchen **ein** .</span><span class="sxs-lookup"><span data-stu-id="b0a45-129">To enable safety tips, under **Safety Tips**, check the **On** checkbox.</span></span> <span data-ttu-id="b0a45-130">Um Sicherheitstipps zu deaktivieren, deaktivieren Sie das Kontrollkästchen **ein** .</span><span class="sxs-lookup"><span data-stu-id="b0a45-130">To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="b0a45-131">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b0a45-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="b0a45-132">So aktivieren oder deaktivieren Sie Sicherheitstipps mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0a45-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="b0a45-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="b0a45-133"></span></span>

<span data-ttu-id="b0a45-134">Administratoren können Exchange Online PowerShell verwenden, um Sicherheitstipps zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0a45-134">Admins can use Exchange Online PowerShell to enable or disable safety tips.</span></span> <span data-ttu-id="b0a45-135">Verwenden Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum, um Sicherheitstipps in einer Spamfilter Richtlinie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0a45-135">Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="b0a45-136">Stellen Sie eine Verbindung mit Exchange Online PowerShell her.</span><span class="sxs-lookup"><span data-stu-id="b0a45-136">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="b0a45-137">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="b0a45-137">For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="b0a45-138">Führen Sie das Cmdlet Set-Hostedcontentfilterpolicy dient zum aus, um Sicherheitstipps zu aktivieren oder zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="b0a45-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="b0a45-139">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="b0a45-139">Where:</span></span>
    
  -  <span data-ttu-id="b0a45-140">*Richtlinienname* ist der Name der Richtlinie, die Sie ändern möchten, beispielsweise **default**.</span><span class="sxs-lookup"><span data-stu-id="b0a45-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="b0a45-141">`$true`aktiviert Sicherheitstipps für die Spamfilter Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b0a45-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="b0a45-142">`$false`deaktiviert Sicherheitstipps für die Spamfilter Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b0a45-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="b0a45-143">Führen Sie beispielsweise den folgenden Befehl aus, um Sicherheitstipps für die standardmäßige Spamfilter Richtlinie zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="b0a45-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="b0a45-144">Weitere Informationen zu diesem Cmdlet finden Sie unter [Set-hostedcontentfilterpolicy dient zum](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0a45-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="b0a45-145">Benötigen Sie weitere Hilfe?</span><span class="sxs-lookup"><span data-stu-id="b0a45-145">Still need help?</span></span>
<span data-ttu-id="b0a45-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="b0a45-146"></span></span>

<span data-ttu-id="b0a45-147">Wenn Sie Sicherheitstipps deaktiviert haben, diese jedoch weiterhin in Ihren e-Mail-Nachrichten angezeigt werden, überprüfen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b0a45-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="b0a45-148">Sie können Sicherheitstipps für Outlook im Web nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0a45-148">You can't disable safety tips for Outlook on the web.</span></span> <span data-ttu-id="b0a45-149">Versuchen Sie, dieselbe e-Mail in einem anderen Client wie Outlook anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0a45-149">Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="b0a45-150">Sicherheitstipps sind standardmäßig aktiviert für jeden Benutzer, der EOP verwendet, umfasst dies alle Benutzer von Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0a45-150">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365.</span></span> <span data-ttu-id="b0a45-151">Um zu verhindern, dass Sicherheitstipps in e-Mails angezeigt werden, müssen Sie Sie mithilfe einer Spamfilter Richtlinie deaktivieren, wie in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0a45-151">In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic.</span></span> <span data-ttu-id="b0a45-152">Nachdem Sie die Richtlinie eingerichtet haben, stellen Sie sicher, dass Sie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b0a45-152">Once you've set up the policy, ensure that it is enabled.</span></span> <span data-ttu-id="b0a45-153">Informationen zum Aktivieren von Spamfilter Richtlinien finden Sie unter [configure your Spamfilter Policies](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0a45-153">For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="b0a45-154">Weitere Möglichkeiten zum bekämpfen von Spam und Phishing finden Sie unter [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="b0a45-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  


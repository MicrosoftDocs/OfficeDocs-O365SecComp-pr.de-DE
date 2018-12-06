---
title: Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Office 365 und EOP-Admins erfahren, wie Sie aktivieren und Deaktivieren der Sicherheitstipps in e-Mail-Nachrichten.
ms.openlocfilehash: 8e5d8bf1d2f831b5d74ca3accd8b434519bfeaab
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180855"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="d59df-103">Aktivieren oder Deaktivieren von Sicherheitstipps in Office 365</span><span class="sxs-lookup"><span data-stu-id="d59df-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="d59df-p101">Fügt der Exchange Online Protection (EOP) oder Stempel, eine Safety Tipp, um e-Mail-Nachrichten, die sie bietet. Absender, Safety Tipps bieten eine schnelle, visuelle Möglichkeit, zu bestimmen, ob eine Nachricht aus einer sicheren Empfänger überprüft werden, wenn die Nachricht als Spam von Office 365, markiert wurde, wenn die Nachricht enthält etwas wie Phishing-Betrug verdächtigen oder externe Bilder haben blockiert wurden. Office 365 und EOP-Standalone-Admins können bearbeiten eine richtlinieneinstellung Spam zum Aktivieren oder Deaktivieren der Sicherheitstipps von e-Mail in Outlook und anderen desktop-e-Mail-Clients angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d59df-p101">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers. These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked. Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="d59df-p102">Office 365 Safety Tipps für Ihre Organisation standardmäßig aktiviert, und es wird empfohlen, dass Sie diese aktiviert gegen Spam und Phishing-Angriffen zu lassen. Sie können keine Sicherheitstipps für Outlook im Web deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d59df-p102">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks. You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="d59df-109">Beispiele finden Sie unter und lernen Sie die Informationen im Safety Tipps, finden Sie unter [Sicherheit in e-Mail-Nachrichten in Office 365 Tipps.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="d59df-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="d59df-110">Inhalt dieses Themas:</span><span class="sxs-lookup"><span data-stu-id="d59df-110">In this topic:</span></span>
  
- [<span data-ttu-id="d59df-111">So aktivieren oder Deaktivieren von Safety Tipps mithilfe der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d59df-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="d59df-112">Tipps zu aktivieren oder deaktivieren die Sicherheit mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d59df-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="d59df-113">So aktivieren oder Deaktivieren von Safety Tipps mithilfe der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d59df-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="d59df-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="d59df-114"></span></span>

1. <span data-ttu-id="d59df-115">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="d59df-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="d59df-116">Melden Sie sich bei Office 365 mit Ihrem Geschäfts, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="d59df-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="d59df-117">Wählen Sie **Threat Management** \> **Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="d59df-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="d59df-118">Wählen Sie auf der Seite **Richtlinie** **Anti-Spam**aus.</span><span class="sxs-lookup"><span data-stu-id="d59df-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![Dieser Screenshot zeigt, wie Sie auf der Seite Anti-Spam Settings in das Wertpapier abrufen &amp; Compliance Center.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="d59df-120">Wählen Sie auf der Seite **Anti-Spam Settings** die Registerkarte **Benutzerdefiniert** .</span><span class="sxs-lookup"><span data-stu-id="d59df-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![Dieser Screenshot zeigt den Speicherort der benutzerdefinierten Registerkarte auf der Seite Anti-Spam Settings in das Wertpapier &amp; Compliance Center.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="d59df-p103">Falls erforderlich, wählen Sie die Option **Benutzerdefinierte Einstellungen** , um benutzerdefinierte Einstellungen zu aktivieren. Wenn die Option Benutzerdefinierte Einstellungen auf **deaktiviert**festgelegt ist, werden Sie kann nicht zum Ändern von Richtlinien für Spam-Filter.</span><span class="sxs-lookup"><span data-stu-id="d59df-p103">If necessary, choose the **Custom settings** switch to turn on custom settings. If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![Dieser Screenshot zeigt benutzerdefinierten Anti-Spam-Filter Richtlinieneinstellungen deaktiviert.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="d59df-p104">Erweitern Sie die Spam-Richtlinie, den, die Sie ändern, und wählen Sie dann auf **Richtlinie bearbeiten**möchten. Wählen Sie beispielsweise den Pfeil nach unten neben der **Standard-Spam-Richtlinie zu filtern**. Oder, wenn Sie möchten, können Sie eine neue Richtlinie erstellen, indem Sie **eine Richtlinie hinzufügen**auswählen.</span><span class="sxs-lookup"><span data-stu-id="d59df-p104">Expand the spam policy you want to modify and then choose **Edit policy**. For example, choose the down arrow next to **Default spam filter policy**. Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="d59df-128">Erweitern Sie **Spam und Massen** -Aktionen.</span><span class="sxs-lookup"><span data-stu-id="d59df-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="d59df-p105">Aktivieren Sie das Kontrollkästchen **auf** , um Sicherheitstipps, unter **Safety Tipps**zu aktivieren. Deaktivieren Sie das Kontrollkästchen **auf** , um Sicherheitstipps zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d59df-p105">To enable safety tips, under **Safety Tips**, check the **On** checkbox. To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="d59df-131">Klicken Sie auf **Save**.</span><span class="sxs-lookup"><span data-stu-id="d59df-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="d59df-132">Tipps zu aktivieren oder deaktivieren die Sicherheit mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d59df-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="d59df-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="d59df-133"></span></span>

<span data-ttu-id="d59df-p106">Administratoren können Exchange Online PowerShell aktivieren oder Deaktivieren der Sicherheitstipps. Verwenden Sie das Cmdlet Set-hostedcontentfilterpolicy dient zum Aktivieren oder Deaktivieren der Sicherheitstipps in einer Spam-Filter-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d59df-p106">Admins can use Exchange Online PowerShell to enable or disable safety tips. Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="d59df-p107">Herstellen einer Verbindung mit Exchange Online PowerShell. Informationen finden Sie unter [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="d59df-p107">Connect to Exchange Online PowerShell. For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="d59df-138">Führen Sie das Cmdlet Set-hostedcontentfilterpolicy dient zum Aktivieren oder Deaktivieren der Sicherheitstipps aus:</span><span class="sxs-lookup"><span data-stu-id="d59df-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="d59df-139">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="d59df-139">Where:</span></span>
    
  -  <span data-ttu-id="d59df-140">*Richtlinienname* ist der Name der Richtlinie, die Sie ändern beispielsweise **Standard, möchten**.</span><span class="sxs-lookup"><span data-stu-id="d59df-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="d59df-141">`$true`Sicherheitstipps für die Spam-Filter-Richtlinie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d59df-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="d59df-142">`$false`Sicherheitstipps für die Spam-Filter-Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d59df-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="d59df-143">Führen Sie beispielsweise den folgenden Befehl, um Sicherheitstipps für die Standardrichtlinie für Spam-Filter zu deaktivieren, aus:</span><span class="sxs-lookup"><span data-stu-id="d59df-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="d59df-144">Weitere Informationen zu diesem Cmdlet finden Sie unter [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="d59df-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="d59df-145">Benötigen Sie weitere Hilfe?</span><span class="sxs-lookup"><span data-stu-id="d59df-145">Still need help?</span></span>
<span data-ttu-id="d59df-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="d59df-146"></span></span>

<span data-ttu-id="d59df-147">Wenn Sie Sicherheitstipps deaktiviert, aber sind weiterhin in Ihre e-Mail-Nachrichten, überprüfen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d59df-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="d59df-p108">Sie können keine Sicherheitstipps für Outlook im Web deaktivieren. Versuchen Sie die gleiche e-Mail in einem anderen Client wie Outlook anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d59df-p108">You can't disable safety tips for Outlook on the web. Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="d59df-p109">Sicherheitstipps sind standardmäßig für jedes, EOP verwendet, einschließlich jeder, der Office 365. Um die Sicherheitstipps in e-Mail angezeigt deaktiviert haben, müssen Sie sie mithilfe einer Filterrichtlinie für Spam, wie in diesem Thema beschrieben deaktivieren. Nachdem Sie die Richtlinie eingerichtet haben, stellen Sie sicher, dass es aktiviert ist. Informationen zu Richtlinien für Spam-Filter aktivieren finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="d59df-p109">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365. In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic. Once you've set up the policy, ensure that it is enabled. For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="d59df-154">Weitere Methoden zum Spam und Phishing zu bekämpfen finden Sie unter [Office 365 E-Mail Anti-Spam-Schutz](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="d59df-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  


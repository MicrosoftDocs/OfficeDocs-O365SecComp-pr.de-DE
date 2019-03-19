---
title: Verschieben von Domänen und Einstellungen zwischen EOP-Organisationen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d64867b-ebdb-4323-8e30-4560d76b4c97
description: Änderungen in den Geschäftsanforderungen können manchmal erfordern, dass eine Microsoft Exchange Online Protection (EOP)-Organisation (ein Mandant) in zwei separate Organisationen unterteilt wird, zwei Organisationen in einer zusammengefasst oder Ihre Domänen und EOP-Einstellungen von einer Organisation zu einer anderen verschoben werden.
ms.openlocfilehash: 4cc3c7273a06374050f705f51d6b3d85fa8e037c
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670590"
---
# <a name="move-domains-and-settings-from-one-eop-organization-to-another-eop-organization"></a><span data-ttu-id="c028c-103">Verschieben von Domänen und Einstellungen zwischen EOP-Organisationen</span><span class="sxs-lookup"><span data-stu-id="c028c-103">Move domains and settings from one EOP organization to another EOP organization</span></span>

<span data-ttu-id="c028c-p101">Änderungen in den Geschäftsanforderungen können manchmal erfordern, dass eine Microsoft Exchange Online Protection (EOP)-Organisation (ein Mandant) in zwei separate Organisationen unterteilt wird, zwei Organisationen in einer zusammengefasst oder Ihre Domänen und EOP-Einstellungen von einer Organisation zu einer anderen verschoben werden. Das Verschieben einer EOP-Organisaton zu einer zweiten EOP-Organisation kann ein Problem darstellen, doch mit ein paar einfachen Remote Windows PowerShell-Skripts und etwas Vorbereitung kann dies in einem relativ kleinen Wartungszeitfenster erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="c028c-p101">Changing business requirements can sometimes require splitting one Microsoft Exchange Online Protection (EOP) organization (tenant) into two separate organizations, merging two organizations into one, or moving your domains and EOP settings from one organization to another organization. Moving from one EOP organization to a second EOP organization can be challenging, but with a few basic remote Windows PowerShell scripts and a small amount of preparation, this can be achieved with a relatively small maintenance window.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="c028c-106">Einstellungen können auf zuverlässige Weise nur von einer eigenständigen EOP (Standard)-Organisation zu entweder einer anderen EOP Standard-Organisation oder einer EOP Premium-Organisation (Exchange Enterprise CAL mit Diensten) oder von einer EOP Premium-Organisation zu einer anderen EOP Premium-Organisation verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c028c-106">Settings can be reliably moved only from an EOP standalone (Standard) organization to either another EOP Standard or an Exchange Enterprise CAL with Services (EOP Premium) organization, or from an EOP Premium organization to another EOP Premium organization.</span></span> <span data-ttu-id="c028c-107">Da einige Premium-Features in EOP-Standardorganisationen nicht unterstützt werden, sind die Verschiebungen von einer EOP Premium-Organisation zu einer EOP-Standardorganisation möglicherweise nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c028c-107">Because some premium features are not supported in EOP Standard organizations, moves from an EOP Premium organization to an EOP Standard organization might not be successful.</span></span> <span data-ttu-id="c028c-108">>  Diese Anweisungen gelten nur für filternde EOP-Organisationen.</span><span class="sxs-lookup"><span data-stu-id="c028c-108">>  These instructions are for EOP filtering-only organizations.</span></span> <span data-ttu-id="c028c-109">Es gibt weitere Überlegungen beim Verschieben zwischen Exchange Online-Organisationen.</span><span class="sxs-lookup"><span data-stu-id="c028c-109">There are additional considerations in moving from one Exchange Online organization to another Exchange Online organization.</span></span> <span data-ttu-id="c028c-110">Exchange Online-Organisationen werden in diesen Anweisungen nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c028c-110">Exchange Online organizations are out of scope for these instructions.</span></span> 
  
<span data-ttu-id="c028c-p103">Im folgenden Beispiel wurde Contoso, Ltd. mit Contoso Suites zusammengeführt. Auf dem folgenden Bild ist der Prozess für das Verschieben von Domänen, E-Mail-Benutzern und Gruppen sowie Einstellungen aus der EOP-Quellorganisation (contoso.onmicrosoft.com) zur EOP-Zielorganisation (contososuites.onmicrosoft.com) dargestellt:</span><span class="sxs-lookup"><span data-stu-id="c028c-p103">In the following example, Contoso, Ltd. has merged with Contoso Suites. The following image shows the process of moving domains, mail users and groups, and settings from the source EOP organization (contoso.onmicrosoft.com) to the target EOP organization (contososuites.onmicrosoft.com):</span></span>
  
![EOP-Domänen und -Einstellungen verschieben](../media/EOP-Move-domains-and-settings.jpg)
  
<span data-ttu-id="c028c-p104">Das Problem beim Verschieben von Domänen zwischen Organisationen besteht darin, dass eine überprüfte Domäne nicht gleichzeitig in zwei Organisationen vorhanden sein kann. Die folgenden Schritte unterstützen Sie bei diesem Prozess.</span><span class="sxs-lookup"><span data-stu-id="c028c-p104">The challenge in moving domains from one organization to another is that a verified domain can't exist in two organizations at the same time. The following steps help you work through this.</span></span>
      
## <a name="step-1-collect-data-from-the-source-organization"></a><span data-ttu-id="c028c-116">Schritt 1: Sammeln von Daten aus der Quellorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-116">Step 1: Collect data from the source organization</span></span>

<span data-ttu-id="c028c-117">Um die Quellorganisation in der Zielorganisation erneut zu erstellen, müssen Sie zunächst die folgenden Informationen über die Quellorganisation sammeln und speichern:</span><span class="sxs-lookup"><span data-stu-id="c028c-117">In order to re-create the source organization in the target organization, make sure that you collect and store the following information about the source organization:</span></span>
  
- <span data-ttu-id="c028c-118">Domänen</span><span class="sxs-lookup"><span data-stu-id="c028c-118">Domains</span></span>
    
- <span data-ttu-id="c028c-119">E-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="c028c-119">Mail users</span></span>
    
- <span data-ttu-id="c028c-120">Gruppen</span><span class="sxs-lookup"><span data-stu-id="c028c-120">Groups</span></span>
    
- <span data-ttu-id="c028c-121">Antispam-Inhaltsfilter</span><span class="sxs-lookup"><span data-stu-id="c028c-121">Anti-spam content filters</span></span>
    
- <span data-ttu-id="c028c-122">Anti-Malware-Inhaltsfilter</span><span class="sxs-lookup"><span data-stu-id="c028c-122">Anti-malware content filters</span></span>
    
- <span data-ttu-id="c028c-123">Connectors</span><span class="sxs-lookup"><span data-stu-id="c028c-123">Connectors</span></span>
    
- <span data-ttu-id="c028c-124">Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="c028c-124">Mail flow rules (also known as transport rules)</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c028c-125">Die Unterstützung von Cmdlets für den Export und Import der Nachrichtenfluss Regelsammlung wird derzeit nur für EOP Premium-Abonnement Pläne unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c028c-125">Cmdlet support for the export and import of the mail flow rule collection is currently only supported for EOP Premium subscription plans.</span></span> 
  
<span data-ttu-id="c028c-p105">Am einfachsten können Sie all Ihre Einstellungen mithilfe der Remote Windows PowerShell sammeln. Weitere Informationen über die Verbindungsherstellung zu EOP über die Remote Windows PowerShell finden Sie unter [Herstellen einer Verbindung mit Exchange Online Protection mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="c028c-p105">The easiest way to collect all of your settings is to use remote Windows PowerShell. To connect to EOP by using remote Windows PowerShell, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
  
<span data-ttu-id="c028c-p106">Als Nächstes können Sie alle Einstellungen sammeln und sie in eine XML-Datei exportieren, um sie in den Zielmandanten zu importieren. Im Allgemeinen können Sie bei jeder Einstellung die Ausgabe des Cmdlets **Get** in das Cmdlet **Export-Clixml** übergeben, um die Einstellungen in XML-Dateien zu speichern, wie im folgenden Beispielcode dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c028c-p106">Next, you can collect all your settings and export them to an .xml file to be imported into the target tenant. In general, you can pipe the output of the **Get** cmdlet for each setting to the **Export-Clixml** cmdlet to save the settings in .xml files, as shown in the following code sample.</span></span> 
  
<span data-ttu-id="c028c-p107">Nachdem Sie eine Verbindung mit der Remote Windows PowerShell hergestellt haben, erstellen Sie in einem leicht zu findenden Speicherort ein Verzeichnis mit dem Namen "Export", und wechseln Sie in dieses Verzeichnis. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c028c-p107">After you've connected to remote Windows PowerShell, create a directory called Export in a location that's easy to find and change to that directory. For example:</span></span>
  
```Powershell
mkdir C:\EOP\Export
```

```Powershell
cd C:\EOP\Export
```

<span data-ttu-id="c028c-132">Das folgende Skript kann verwendet werden, um alle e-Mail-Benutzer, Gruppen, Antispam-Einstellungen, Antischadsoftware-Einstellungen, Connectors und Nachrichtenfluss Regeln in der Quellorganisation zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c028c-132">The following script can be used to collect all the mail users, groups, anti-spam settings, anti-malware settings, connectors, and mail flow rules in the source organization.</span></span> <span data-ttu-id="c028c-133">Kopieren Sie den folgenden Text, fügen Sie ihn in einem Texteditor ein, z. B. Editor, speichern Sie die Datei als Source_EOP_Settings.ps1 im eben erstellten Verzeichnis "Export", und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c028c-133">Copy and paste the following text into a text editor like Notepad, save the file as Source_EOP_Settings.ps1 in the Export directory you just created, and run the following command:</span></span>
  
```Powershell
& "C:\EOP\Export\Source_EOP_Settings.ps1"

```

```Powershell
#****************************************************************************
# Export Domains
#*****************************************************************************
Get-AcceptedDomain | Export-Clixml Domains.xml
#****************************************************************************
# Export mail users
#
#****************************************************************************
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUser | Export-Clixml MailUsers.xml
#****************************************************************************
# Groups
#
# If you're using directory synchronization, you can skip this step and 
# simply sync to the target 
# tenant.
# First, you need to capture information about the distribution groups.
#****************************************************************************
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUniversalDistributionGroup | Export-Clixml DistributionGroups.xml
Get-Recipient -ResultSize unlimited -RecipientTypeDetails MailUniversalSecurityGroup | Export-Clixml SecurityGroups.xml 
#****************************************************************************
# And then we'll use that output to loop through each group and get the 
# members.
#****************************************************************************
$DGs = Import-Clixml .\DistributionGroups.xml
ForEach ($dg in $DGs) {Get-DistributionGroupMember -Identity $dg.name | Export-Clixml $dg.ExternalDirectoryObjectId}
$SGs = Import-Clixml .\SecurityGroups.xml
ForEach ($sg in $SGs) {Get-DistributionGroupMember -Identity $sg.name | Export-Clixml $sg.ExternalDirectoryObjectId} 
#*****************************************************************************
# Export dynamic distribution groups - EOP Premium Only
#
# If you're using directory synchronization, then you can skip this step and simply 
# sync to the target tenant.
#*****************************************************************************
Get-DynamicDistributionGroup -ResultSize unlimited | Export-Clixml DynamicDistributionGroups.xml
#*****************************************************************************
# Export mail contacts - EOP Premium Only
#
# If you're using directory synchronization, then you can skip this step and simply 
# sync to the target tenant.
#*****************************************************************************
Get-MailContact -ResultSize unlimited -RecipientTypeDetails MailContact | Export-Clixml MailContacts.xml
#****************************************************************************
# Anti-spam
#****************************************************************************
Get-HostedConnectionFilterPolicy | Export-Clixml HostedConnectionFilterPolicy.xml
Get-HostedContentFilterPolicy | Export-Clixml HostedContentFilterPolicy.xml
Get-HostedContentFilterRule | Export-Clixml HostedContentFilterRule.xml
Get-HostedOutboundSpamFilterPolicy | Export-Clixml HostedOutboundSpamFilterPolicy.xml
#****************************************************************************
# Anti-malware content filters
#****************************************************************************
Get-MalwareFilterPolicy | Export-Clixml MalwareFilterPolicy.xml
Get-MalwareFilterRule | Export-Clixml MalwareFilterRule.xml
#****************************************************************************
# Connectors
#****************************************************************************
Get-InboundConnector | Export-Clixml InboundConnector.xml
Get-OutboundConnector | Export-Clixml OutboundConnector.xml
#****************************************************************************
# Exchange mail flow rules
#****************************************************************************
$file = Export-TransportRuleCollection
Set-Content -Path ".TransportRules.xml" -Value $file.FileData -Encoding Byte
```

<span data-ttu-id="c028c-p109">Führen Sie die folgenden Befehle im Export-Verzeichnis aus, um die XML-Dateien mit der Zielorganisation zu aktualisieren. Ersetzen Sie contoso.onmicrosoft.com und contososuites.onmicrosoft.com durch Ihre Quell- und Zielorganisationsnamen.</span><span class="sxs-lookup"><span data-stu-id="c028c-p109">Run the following commands from the Export directory to update the .xml files with the target organization. Replace contoso.onmicrosoft.com and contososuites.onmicrosoft.com with your source and target organization names.</span></span>
  
```Powershell
$files = ls
ForEach ($file in $files) { (Get-Content $file.Name) | Foreach-Object {$_ -replace 'contoso.onmicrosoft.com', 'contososuites.onmicrosoft.com'} | Set-Content $file.Name}
```

## <a name="step-2-add-domains-to-the-target-organization"></a><span data-ttu-id="c028c-136">Schritt 2: Hinzufügen von Domänen zur Zielorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-136">Step 2: Add domains to the target organization</span></span>

<span data-ttu-id="c028c-p110">Fügen Sie Domänen zur Zielorganisation hinzu, indem Sie das folgende Skript verwenden. Kopieren Sie den Text, fügen Sie ihn in einem Texteditor ein, z. B. Editor, speichern Sie das Skript unter C:\EOP\Export\Add_Domains.ps1, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c028c-p110">Add domains to the target organization by using the following script. Copy and paste the text into a text editor like Notepad, save the script as C:\EOP\Export\Add_Domains.ps1, and run the following command:</span></span>
  
```Powershell
&amp; "C:\EOP\Export\Add_Domains.ps1"
```

<span data-ttu-id="c028c-139">Diese Domänen werden nicht überprüft und können nicht zum Weiterleiten von E-Mails verwendet werden. Sie können aber die benötigten Informationen sammeln, um die Domänen zu überprüfen, und schließlich Ihre MX-Einträge für den neuen Mandanten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c028c-139">These domains won't be verified and can't be used to route mail, but after the domains are added, you can collect the information needed to verify the domains and eventually update your MX records for the new tenant.</span></span>
  
```Powershell
#***********************************************************************
# Login to Azure Active Directory
#*****************************************************************************
$msolcred = Get-Credential
connect-msolservice -credential $msolcred
#****************************************************************************
# Add domains
#****************************************************************************
$Domains = Import-Clixml ".\Domains.xml"
Foreach ($domain in $Domains) {
    New-MsolDomain -Name $domain.Name
} 

```

<span data-ttu-id="c028c-140">Jetzt können Sie die Informationen aus dem Microsoft 365 Admin Center ihrer Zielorganisation überprüfen und sammeln, damit Sie Ihre Domänen schnell überprüfen können, wenn der Zeitpunkt gekommen ist:</span><span class="sxs-lookup"><span data-stu-id="c028c-140">Now, you can review and collect the information from the Microsoft 365 admin center of your target organization so that you can quickly verify your domains when the time comes:</span></span>
  
1. <span data-ttu-id="c028c-141">Melden Sie sich im Microsoft 365 Admin Center unter [https://portal.office.com](https://portal.office.com)an.</span><span class="sxs-lookup"><span data-stu-id="c028c-141">Sign in to the Microsoft 365 admin center at [https://portal.office.com](https://portal.office.com).</span></span>
    
2. <span data-ttu-id="c028c-142">Klicken Sie auf **Domänen**.</span><span class="sxs-lookup"><span data-stu-id="c028c-142">Click **Domains**.</span></span>
    
3. <span data-ttu-id="c028c-143">Klicken Sie auf die einzelnen **Setup starten**-Links, und fahren Sie dann mit dem Setup-Assistenten fort.</span><span class="sxs-lookup"><span data-stu-id="c028c-143">Click each **Start setup** link, and then proceed through the setup wizard.</span></span> 
    
4. <span data-ttu-id="c028c-144">On the **Confirm ownership** page, for **See step-by-step instructions for performing this step with**, select **General instructions**.</span><span class="sxs-lookup"><span data-stu-id="c028c-144">On the **Confirm ownership** page, for **See step-by-step instructions for performing this step with**, select **General instructions**.</span></span>
    
5. <span data-ttu-id="c028c-145">Protokollieren Sie den MX- oder TXT-Eintrag, den Sie für die Überprüfung Ihrer Domäne benötigen, und beenden Sie den Setup-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="c028c-145">Record the MX record or TXT record that you'll use to verify your domain, and finish the setup wizard.</span></span>
    
6. <span data-ttu-id="c028c-p111">Fügen Sie die TXT-Überprüfungseinträge zu Ihren DNS-Einträgen hinzu. Dadurch können Sie die Domänen in der Quellorganisation schneller überprüfen, nachdem sie aus der Zielorganisation entfernt wurden. Weitere Informationen über das Konfigurieren des DNS finden Sie unter [Erstellen von DNS-Einträgen für Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span><span class="sxs-lookup"><span data-stu-id="c028c-p111">Add the verification TXT records to your DNS records. This will let you more quickly verify the domains in the source organization after they're removed from the target organization. For more information about configuring DNS, see [Create DNS records for Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span></span>
    
## <a name="step-3-force-senders-to-queue-mail"></a><span data-ttu-id="c028c-149">Schritt 3: Erzwingen, dass Absender-E-Mails in die Warteschlange kommen</span><span class="sxs-lookup"><span data-stu-id="c028c-149">Step 3: Force senders to queue mail</span></span>

<span data-ttu-id="c028c-p112">Beim Verschieben Ihrer Domänen von einem Mandanten zu einem anderen müssen Sie die Domänen aus der Quellorganisation löschen und sie in Ihrer Zielorganisation überprüfen. Bei diesem Vorgang können keine E-Mails über EOP weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c028c-p112">While moving your domains from one tenant to another, you'll need to delete the domains from the source organization and then verify them in your target organization. During this time, you won't be able to route mail through EOP.</span></span>
  
<span data-ttu-id="c028c-152">Eine Möglichkeit, wie Sie die Einreihung von Absender-E-Mails in die Warteschlange erzwingen, ist die Aktualisierung Ihrer MX-Einträge, sodass sie direkt auf Ihren lokalen E-Mail-Server verweisen.</span><span class="sxs-lookup"><span data-stu-id="c028c-152">One option to force senders to queue mail is to update your MX records to point directly to your on-premises mail server.</span></span>
  
<span data-ttu-id="c028c-p113">Eine andere Möglichkeit ist das Setzen eines ungültigen MX-Eintrags in den einzelnen Domänen, in denen sich die DNS-Einträge für Ihre Domäne befinden (auch als DNS-Hostingdienst bezeichnet). Dadurch werden die Absender-E-Mails in die Warteschlange eingereiht, und das Senden wird erneut versucht (in der Regel erfolgen Wiederholungsversuche 48 Stunden lang, das kann aber je nach Anbieter variieren). Sie können invalid.outlook.com als ein ungültiges MX-Ziel verwenden. Wenn Sie den TTL-Wert (Time to Live) für den MX-Eintrag auf fünf Minuten heruntersetzen, wird die Verteilung der Änderung an die DNS-Anbieter beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="c028c-p113">Another option is to put an invalid MX record in each domain where the DNS records for your domain are kept (also known as your DNS hosting service). This will cause the sender to queue your mail and retry (typical retry attempts are for 48 hours, but this might vary from provider to provider). You can use invalid.outlook.com as an invalid MX target. Lowering the Time to Live (TTL) value to five minutes on the MX record will help the change propagate to DNS providers more quickly.</span></span>
  
<span data-ttu-id="c028c-157">Weitere Informationen über das Konfigurieren des DNS finden Sie unter [Erstellen von DNS-Einträgen für Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span><span class="sxs-lookup"><span data-stu-id="c028c-157">For more information about configuring DNS, see [Create DNS records for Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c028c-p114">Andere Anbieter reihen E-Mails unterschiedlich lang in die Warteschlange ein. Sie müssen Ihren neuen Mandanten schnell einrichten und Ihre DNS-Einstellungen wiederherstellen, um zu verhindern, dass Unzustellbarkeitsberichte an den Absender gesendet werden, wenn die Warteschlangenzeit ausläuft.</span><span class="sxs-lookup"><span data-stu-id="c028c-p114">Different providers queue mail for different periods of time. You'll need to set up your new tenant quickly and revert your DNS settings to avoid non-delivery reports (NDRs) from being sent to the sender if the queuing time expires.</span></span> 
  
## <a name="step-4-remove-users-groups-and-domains-from-the-source-organization"></a><span data-ttu-id="c028c-160">Schritt 4: Entfernen von Benutzern, Gruppen und Domänen aus der Quellorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-160">Step 4: Remove users, groups, and domains from the source organization</span></span>

<span data-ttu-id="c028c-p115">Das folgende Skript entfernt Benutzer, Gruppen und Domänen aus dem Quellmandanten, indem die Remote Windows PowerShell für Windows Azure Active Directory verwendet wird. Kopieren Sie den folgenden Text, fügen Sie ihn in einem Texteditor ein, z. B. Editor, speichern Sie die Datei unter C:\EOP\Export\Remove_Users_and_Groups.ps1, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c028c-p115">The following script removes users, groups, and domains from the source tenant by using Azure Active Directory remote Windows PowerShell. Copy and paste the following text into a text editor like Notepad, save the file as C:\EOP\Export\Remove_Users_and_Groups.ps1, and run the following command:</span></span>
  
```Powershell
& "C:\EOP\Export\Remove_Users_and_Groups.ps1"
```

```Powershell
#*****************************************************************************
# Login to Azure Active Directory
#*****************************************************************************
$msolcred= Get-Credential
connect-msolservice -credential $msolcred
#*****************************************************************************
# Remove users
#*****************************************************************************
$Users = Get-MSOLUser -All | sort UserPrincipalName
$user_count = $Users.count
write-host "Removing $user_count users."
Foreach ($User in $Users) {
write-host $User.UserPrincipalName
$User | Remove-MSOLUser -Force
}
#*****************************************************************************
# Remove groups
#*****************************************************************************
Get-MSOLGroup | Remove-MSOLGroup -Force
#*****************************************************************************
# Remove domains
# Note: Your onmicrosoft.com domain should be the default domain
#*****************************************************************************
$Domains = Get-MsolDomain
$Domain_count = $Domains.count
write-host "Removing $Domain_count domains."
Foreach ($Domain in $Domains) {
write-host $Domain.Name
Remove-MsolDomain -DomainName $Domain.Name -Force
} 

```

## <a name="step-5-verify-domains-for-the-target-organization"></a><span data-ttu-id="c028c-163">Schritt 5: Überprüfen von Domänen für die Zielorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-163">Step 5: Verify domains for the target organization</span></span>

1. <span data-ttu-id="c028c-164">Melden Sie sich im Admin Center unter [https://portal.office.com](https://portal.office.com)an.</span><span class="sxs-lookup"><span data-stu-id="c028c-164">Sign in to the admin center at [https://portal.office.com](https://portal.office.com).</span></span>
    
2. <span data-ttu-id="c028c-165">Klicken Sie auf **Domänen**.</span><span class="sxs-lookup"><span data-stu-id="c028c-165">Click **Domains**.</span></span>
    
3. <span data-ttu-id="c028c-166">Klicken Sie auf die einzelnen **Setup starten**-Links für die Zieldomäne, und fahren Sie mit dem Setup-Assistenten fort.</span><span class="sxs-lookup"><span data-stu-id="c028c-166">Click each **Start setup** link for the target domain and proceed through the setup wizard.</span></span> 
    
## <a name="step-6-add-mail-users-and-groups-to-the-target-organization"></a><span data-ttu-id="c028c-167">Schritt 6: Hinzufügen von E-Mail-Benutzern und Gruppen zur Zielorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-167">Step 6: Add mail users and groups to the target organization</span></span>

<span data-ttu-id="c028c-p116">Eine bewährte Methode für EOP ist die Verwendung von Azure Active Directory für die Synchronisierung Ihres lokalen Active Directory mit Ihrem Zielmandanten. Weitere Informationen über die Vorgehensweise finden Sie unter "Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung" in [Verwalten von E-Mail-Benutzern in EOP](manage-mail-users-in-eop.md). Sie können auch das folgende Skript verwenden, um Ihre Benutzer und Gruppen aus dem Quellmandanten erneut zu erstellen. Hinweis: Benutzerkennwörter können nicht verschoben werden. Neue Benutzerkennwörter werden in der Datei UsersAndGroups.ps1 erstellt und gespeichert. (Weitere Informationen über das Zurücksetzen von Benutzerkennwörtern finden Sie unter [Zurücksetzen von Benutzerkennwörtern](https://office.microsoft.com/en-us/office365-suite-help/reset-a-user-s-password-HA102816058.aspx).)</span><span class="sxs-lookup"><span data-stu-id="c028c-p116">A best practice for EOP is to use Azure Active Directory to sync your on-premises Active Directory to your target tenant. For more information about how to do this, see "Use directory synchronization to manage mail users" in [Manage mail users in EOP](manage-mail-users-in-eop.md). You can also use the following script to recreate your users and groups from your source tenant. Note: User passwords cannot be moved. New user passwords are created and saved in the file named UsersAndGroups.ps1. (For more information about resetting your password, see [Reset a user's password](https://office.microsoft.com/en-us/office365-suite-help/reset-a-user-s-password-HA102816058.aspx).)</span></span>
  
<span data-ttu-id="c028c-174">Kopieren Sie für die Verwendung des Skripts den folgenden Text, fügen Sie ihn in einem Texteditor ein, z. B. Editor, speichern Sie die Datei unter C:\EOP\Export\Add_Users_and_Groups.ps1, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c028c-174">To use the script, copy and paste the following text into a text editor like Notepad, save the file as C:\EOP\Export\Add_Users_and_Groups.ps1, and run the following command:</span></span>
  
```Powershell
& "C:\EOP\Export\Add_Users_and_Groups.ps1"
```

```Powershell
#***********************************************************************
# makeparam helper function
#****************************************************************************
function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam       
 } 
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\UsersAndGroups.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# Add mail users
#****************************************************************************
$rand = New-Object System.Random -ArgumentList (get-date).millisecond
$MailUsers = Import-Clixml ".\MailUsers.xml"
$MailUsersCount = $MailUsers.Name.Count
if($MailUsersCount -gt 0){
    Write-Host "Importing $MailUsersCount Mail Users"
    ForEach ($MailUser in $MailUsers) {
        $MailUsersCmdlet = "New-MailUser"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPMailUser"
        }
        $MailUsersCmdlet += makeparam "LastName" $MailUser.LastName
        $MailUsersCmdlet += makeparam "FirstName" $MailUser.FirstName
        $MailUsersCmdlet += makeparam "DisplayName" $MailUser.DisplayName
        $MailUsersCmdlet += makeparam "Name" $MailUser.Name
        $MailUsersCmdlet += makeparam "Alias" $MailUser.Alias
        $MailUsersCmdlet += makeparam "MicrosoftOnlineServicesID" $MailUser.MicrosoftOnlineServicesID
        $MailUsersCmdlet += makeparam "ExternalEmailAddress" $MailUser.ExternalEmailAddress
        
        # Generate a new 10 character password
        $NewPassword = ""
        1..10 | ForEach { $NewPassword = $NewPassword + [char]$rand.next(40,127) }
        
        $MailUsersCmdlet += " -Password (ConvertTo-SecureString -String '$NewPassword' -AsPlainText -Force)"
        Add-Content $outfile "`n$MailUsersCmdlet"
    }
}
#****************************************************************************
# Add distribution groups
#****************************************************************************
$DistributionGroups = Import-Clixml ".\DistributionGroups.xml"
$DistributionGroupsCount = $DistributionGroups.Name.Count
if($DistributionGroupsCount -gt 0){
    Write-Host "Importing $DistributionGroupsCount Distribution Groups"
    ForEach ($DistributionGroup in $DistributionGroups) {
        $DistributionGroupsCmdlet = "New-DistributionGroup"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPDistributionGroup"
        }
        $DistributionGroupsCmdlet += makeparam "Name" $DistributionGroup.Name
        $DistributionGroupsCmdlet += makeparam "Alias" $DistributionGroup.Alias
        $DistributionGroupsCmdlet += makeparam "DisplayName" $DistributionGroup.DisplayName
        $DistributionGroupsCmdlet += makeparam "ManagedBy" $DistributionGroup.ManagedBy
        
        $DistributionGroupsCmdlet += makeparam "Notes" $DistributionGroup.Notes
        $DistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DistributionGroup.PrimarySmtpAddress
        $DistributionGroupsCmdlet += makeparam "Type" $DistributionGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $DistributionGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$DistributionGroupsCmdlet"
}
#****************************************************************************
# Add security groups
#****************************************************************************
$SecurityGroups = Import-Clixml ".\SecurityGroups.xml"
$SecurityGroupsCount = $SecurityGroups.Name.Count
if($SecurityGroupsCount -gt 0){
    Write-Host "Importing $SecurityGroupsCount Security Groups"
    ForEach ($SecurityGroup in $SecurityGroups) {
        $SecurityGroupsCmdlet = "New-SecurityGroup"
        If((Get-PSSession).ComputerName.Contains("ps.protection")) {
            $DistributionGroupsCmdlet = "New-EOPSecurityGroup"
        }
        $SecurityGroupsCmdlet += makeparam "Name" $SecurityGroup.Name
        $SecurityGroupsCmdlet += makeparam "Alias" $SecurityGroup.Alias
        $SecurityGroupsCmdlet += makeparam "DisplayName" $SecurityGroup.DisplayName
        $SecurityGroupsCmdlet += makeparam "ManagedBy" $SecurityGroup.ManagedBy
        
        $SecurityGroupsCmdlet += makeparam "Notes" $SecurityGroup.Notes
        $SecurityGroupsCmdlet += makeparam "PrimarySmtpAddress" $SecurityGroup.PrimarySmtpAddress
        $SecurityGroupsCmdlet += makeparam "Type" $SecurityGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $SecurityGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$SecurityGroupsCmdlet"
}
#****************************************************************************
# Add Dynamic Distribution Groups
#****************************************************************************
If((Get-PSSession).ComputerName.Contains("ps.protection")) {
    write-Host "No Synamic Distribution Groups for EOP Standard organizations."
}else{
    $DynamicDistributionGroups = Import-Clixml ".\DynamicDistributionGroups.xml"
    $DynamicDistributionGroupsCount = $DynamicDistributionGroups.Name.Count
    if($DynamicDistributionGroupsCount -gt 0){
        Write-Host "Importing $DynamicDistributionGroupsCount Dynamic Distribution Groups"
        foreach ($DynamicDistributionGroup in $DynamicDistributionGroups) {
            $DynamicDistributionGroupsCmdlet = "New-DynamicDistributionGroup" 
            $DynamicDistributionGroupsCmdlet += " -Confirm:`$False"
            $DynamicDistributionGroupsCmdlet += makeparam "DisplayName" $DynamicDistributionGroup.DisplayName 
            $DynamicDistributionGroupsCmdlet += makeparam "ModeratedBy" $DynamicDistributionGroup.ModeratedBy 
            $DynamicDistributionGroupsCmdlet += makeparam "ModerationEnabled" $DynamicDistributionGroup.ModerationEnabled 
            $DynamicDistributionGroupsCmdlet += makeparam "Name" $DynamicDistributionGroup.Name 
            $DynamicDistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DynamicDistributionGroup.PrimarySmtpAddress 
            $DynamicDistributionGroupsCmdlet += makeparam "RecipientContainer" $DynamicDistributionGroup.RecipientContainer
            $RecipientFilterParam =  makeparam "RecipientFilter" $DynamicDistributionGroup.RecipientFilter
            $RecipientFilterParam = " -RecipientFilter {" + $RecipientFilterParam.Substring(19)
            $RecipientFilterParam = $RecipientFilterParam.Substring(0,$RecipientFilterParam.Length-1)
            $RecipientFilterParam += "}"
            $DynamicDistributionGroupsCmdlet +=  $RecipientFilterParam
            $DynamicDistributionGroupsCmdlet += makeparam "SendModerationNotifications" $DynamicDistributionGroup.SendModerationNotifications 
            Add-Content $outfile "`n$DynamicDistributionGroupsCmdlet"
        }
    
    }else{ 
        Write-Host "No Dynamic Distribution Groups to add."
    }
} 
#****************************************************************************
# Add Mail Contacts
#****************************************************************************
If((Get-PSSession).ComputerName.Contains("ps.protection")) {
    write-Host "No Mail Contact for EOP Standard organizations."
}else{
    $MailContacts = Import-Clixml ".\MailContacts.xml"
    $MailContactsCount = $MailContacts.Name.Count
    if($MailContactsCount -gt 0){
        Write-Host "Importing $MailContactsCount Dynamic Distribution Groups"
        foreach ($MailContact in $MailContacts) {
            $MailContactsCmdlet = "New-MailContact" 
            $MailContactsCmdlet += makeparam "UsePreferMessageFormat" $MailContact.UsePreferMessageFormat
            $MailContactsCmdlet += makeparam "DisplayName" $MailContact.DisplayName
            $MailContactsCmdlet += makeparam "ModeratedBy" $MailContact.ModeratedBy
            $MailContactsCmdlet += makeparam "Name" $MailContact.Name
            $MailContactsCmdlet += makeparam "MessageBodyFormat" $MailContact.MessageBodyFormat
            $MailContactsCmdlet += makeparam "OrganizationalUnit" $MailContact.OrganizationalUnit
            $MailContactsCmdlet += makeparam "Initials" $MailContact.Initials
            $MailContactsCmdlet += makeparam "MessageFormat" $MailContact.MessageFormat
            $MailContactsCmdlet += makeparam "ModerationEnabled" $MailContact.ModerationEnabled
            $MailContactsCmdlet += makeparam "MacAttachmentFormat" $MailContact.MacAttachmentFormat
            $MailContactsCmdlet += makeparam "SendModerationNotifications" $MailContact.SendModerationNotifications
            $MailContactsCmdlet += " -Confirm:`$False"
            $MailContactsCmdlet += makeparam "ExternalEmailAddress" $MailContact.ExternalEmailAddress
            $MailContactsCmdlet += makeparam "FirstName" $MailContact.FirstName
            $MailContactsCmdlet += makeparam "Alias" $MailContact.Alias
            Add-Content $outfile "`n$MailContactsCmdlet"
        }
    
    }else{ 
        Write-Host "No Mail Contacts to add."
    }
}
#***********************************************************************
# makeparam helper function
#************************************************************************
 function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam       
 } 
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\UsersAndGroups.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# Add mail users
#****************************************************************************
$rand = New-Object System.Random -ArgumentList (get-date).millisecond
$MailUsers = Import-Clixml ".\MailUsers.xml"
$MailUsersCount = $MailUsers.Name.Count
if($MailUsersCount -gt 0){
    Write-Host "Importing $MailUsersCount Mail Users"
    ForEach ($MailUser in $MailUsers) {
        $MailUsersCmdlet = "New-EOPMailUser"
        $MailUsersCmdlet += makeparam "LastName" $MailUser.LastName
        $MailUsersCmdlet += makeparam "FirstName" $MailUser.FirstName
        $MailUsersCmdlet += makeparam "DisplayName" $MailUser.DisplayName
        $MailUsersCmdlet += makeparam "Name" $MailUser.Name
        $MailUsersCmdlet += makeparam "Alias" $MailUser.Alias
        $MailUsersCmdlet += makeparam "MicrosoftOnlineServicesID" $MailUser.MicrosoftOnlineServicesID
        $MailUsersCmdlet += makeparam "ExternalEmailAddress" $MailUser.ExternalEmailAddress
        
        # Generate a new 10 character password
        $NewPassword = ""
        1..10 | ForEach { $NewPassword = $NewPassword + [char]$rand.next(40,127) }
        
        $MailUsersCmdlet += " -Password (ConvertTo-SecureString -String '$NewPassword' -AsPlainText -Force)"
        Add-Content $outfile "`n$MailUsersCmdlet"
    }
}
#****************************************************************************
# Add distribution groups
#****************************************************************************
$DistributionGroups = Import-Clixml ".\DistributionGroups.xml"
$DistributionGroupsCount = $DistributionGroups.Name.Count
if($DistributionGroupsCount -gt 0){
    Write-Host "Importing $DistributionGroupsCount Distribution Groups"
    ForEach ($DistributionGroup in $DistributionGroups) {
        $DistributionGroupsCmdlet = "New-EOPDistributionGroup"
        $DistributionGroupsCmdlet += makeparam "Name" $DistributionGroup.Name
        $DistributionGroupsCmdlet += makeparam "Alias" $DistributionGroup.Alias
        $DistributionGroupsCmdlet += makeparam "DisplayName" $DistributionGroup.DisplayName
        $DistributionGroupsCmdlet += makeparam "ManagedBy" $DistributionGroup.ManagedBy
        
        $DistributionGroupsCmdlet += makeparam "Notes" $DistributionGroup.Notes
        $DistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DistributionGroup.PrimarySmtpAddress
        $DistributionGroupsCmdlet += makeparam "Type" $DistributionGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $DistributionGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$DistributionGroupsCmdlet"
}
#****************************************************************************
# Add security groups
#****************************************************************************
$SecurityGroups = Import-Clixml ".\SecurityGroups.xml"
$SecurityGroupsCount = $SecurityGroups.Name.Count
if($SecurityGroupsCount -gt 0){
    Write-Host "Importing $SecurityGroupsCount Security Groups"
    ForEach ($SecurityGroup in $SecurityGroups) {
        $SecurityGroupsCmdlet = "New-EOPSecurityGroup"
        $SecurityGroupsCmdlet += makeparam "Name" $SecurityGroup.Name
        $SecurityGroupsCmdlet += makeparam "Alias" $SecurityGroup.Alias
        $SecurityGroupsCmdlet += makeparam "DisplayName" $SecurityGroup.DisplayName
        $SecurityGroupsCmdlet += makeparam "ManagedBy" $SecurityGroup.ManagedBy
        
        $SecurityGroupsCmdlet += makeparam "Notes" $SecurityGroup.Notes
        $SecurityGroupsCmdlet += makeparam "PrimarySmtpAddress" $SecurityGroup.PrimarySmtpAddress
        $SecurityGroupsCmdlet += makeparam "Type" $SecurityGroup.Type
        $MembersCmdlet = "@("
        $memberslist = Import-Clixml $SecurityGroup.ExternalDirectoryObjectId
        ForEach ($user in $memberslist) {
            $MembersCmdlet += "`"$user.Name`","
        }
        $MembersCmdlet = $MembersCmdlet.TrimEnd(",")
        $MembersCmdlet += ")"
    }
    Add-Content $outfile "`n$SecurityGroupsCmdlet"
}
#****************************************************************************
# Add Dynamic Distribution Groups
#****************************************************************************
$DynamicDistributionGroups = Import-Clixml ".\DynamicDistributionGroups.xml"
$DynamicDistributionGroupsCount = $DynamicDistributionGroups.Name.Count
if($DynamicDistributionGroupsCount -gt 0){
    Write-Host "Importing $DynamicDistributionGroupsCount Dynamic Distribution Groups"
    foreach ($DynamicDistributionGroup in $DynamicDistributionGroups) {
        $DynamicDistributionGroupsCmdlet = "New-DynamicDistributionGroup" 
        $DynamicDistributionGroupsCmdlet += " -Confirm:`$False"
        $DynamicDistributionGroupsCmdlet += makeparam "DisplayName" $DynamicDistributionGroup.DisplayName 
        $DynamicDistributionGroupsCmdlet += makeparam "ModeratedBy" $DynamicDistributionGroup.ModeratedBy 
        $DynamicDistributionGroupsCmdlet += makeparam "ModerationEnabled" $DynamicDistributionGroup.ModerationEnabled 
        $DynamicDistributionGroupsCmdlet += makeparam "Name" $DynamicDistributionGroup.Name 
        $DynamicDistributionGroupsCmdlet += makeparam "PrimarySmtpAddress" $DynamicDistributionGroup.PrimarySmtpAddress 
        $DynamicDistributionGroupsCmdlet += makeparam "RecipientContainer" $DynamicDistributionGroup.RecipientContainer
        $RecipientFilterParam =  makeparam "RecipientFilter" $DynamicDistributionGroup.RecipientFilter
        $RecipientFilterParam = " -RecipientFilter {" + $RecipientFilterParam.Substring(19)
        $RecipientFilterParam = $RecipientFilterParam.Substring(0,$RecipientFilterParam.Length-1)
        $RecipientFilterParam += "}"
        $DynamicDistributionGroupsCmdlet +=  $RecipientFilterParam
        $DynamicDistributionGroupsCmdlet += makeparam "SendModerationNotifications" $DynamicDistributionGroup.SendModerationNotifications 
        Add-Content $outfile "`n$DynamicDistributionGroupsCmdlet"
    }
    
}else{ 
    Write-Host "No Dynamic Distribution Groups to add."
} 
#****************************************************************************
# Add Mail Contacts
#****************************************************************************
$MailContacts = Import-Clixml ".\MailContacts.xml"
$MailContactsCount = $MailContacts.Name.Count
if($MailContactsCount -gt 0){
    Write-Host "Importing $MailContactsCount Dynamic Distribution Groups"
    foreach ($MailContact in $MailContacts) {
        $MailContactsCmdlet = "New-MailContact" 
        $MailContactsCmdlet += makeparam "UsePreferMessageFormat" $MailContact.UsePreferMessageFormat
        $MailContactsCmdlet += makeparam "DisplayName" $MailContact.DisplayName
        $MailContactsCmdlet += makeparam "ModeratedBy" $MailContact.ModeratedBy
        $MailContactsCmdlet += makeparam "Name" $MailContact.Name
        $MailContactsCmdlet += makeparam "MessageBodyFormat" $MailContact.MessageBodyFormat
        $MailContactsCmdlet += makeparam "OrganizationalUnit" $MailContact.OrganizationalUnit
        $MailContactsCmdlet += makeparam "Initials" $MailContact.Initials
        $MailContactsCmdlet += makeparam "MessageFormat" $MailContact.MessageFormat
        $MailContactsCmdlet += makeparam "ModerationEnabled" $MailContact.ModerationEnabled
        $MailContactsCmdlet += makeparam "MacAttachmentFormat" $MailContact.MacAttachmentFormat
        $MailContactsCmdlet += makeparam "SendModerationNotifications" $MailContact.SendModerationNotifications
        $MailContactsCmdlet += " -Confirm:`$False"
        $MailContactsCmdlet += makeparam "ExternalEmailAddress" $MailContact.ExternalEmailAddress
        $MailContactsCmdlet += makeparam "FirstName" $MailContact.FirstName
        $MailContactsCmdlet += makeparam "Alias" $MailContact.Alias
        Add-Content $outfile "`n$MailContactsCmdlet"
    }
    
}else{ 
    Write-Host "No Mail Contacts to add."
} 

```

## <a name="step-7-add-protection-settings-to-the-target-organization"></a><span data-ttu-id="c028c-175">Schritt 7: Hinzufügen von Schutzeinstellungen zur Zielorganisation</span><span class="sxs-lookup"><span data-stu-id="c028c-175">Step 7: Add protection settings to the target organization</span></span>

<span data-ttu-id="c028c-176">Sie können das folgende Skript aus dem Export-Verzeichnis ausführen, während Sie in Ihrer Zielorganisation angemeldet sind, um die zuvor aus der Quellorganisation in die XML-Dateien exportierten Einstellungen erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c028c-176">You can run the following script from the Export directory while logged in to your target organization to recreate the settings exported to .xml files earlier from the source organization.</span></span>
  
<span data-ttu-id="c028c-177">Kopieren Sie den Skripttext, fügen Sie ihn in einem Texteditor ein, z. B. Editor, speichern Sie die Datei unter C:\EOP\Export\Import_Settings.ps1, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c028c-177">Copy and paste the script text into a text editor like Notepad, save the file as C:\EOP\Export\Import_Settings.ps1, and run the following command:</span></span>
  
```Powershell
& "C:\EOP\Export\Import_Settings.ps1"
```

<span data-ttu-id="c028c-178">Dieses Skript importiert die XML-Dateien und erstellt eine Windows PowerShell-Skriptdatei mit dem Namen Settings.ps1, die Sie überprüfen, bearbeiten und dann ausführen können, um Ihre Schutz- und Nachrichtenübermittlungseinstellungen erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c028c-178">This script imports the .xml files and create a Windows PowerShell script file called Settings.ps1 that you can review, edit, and then run to recreate your protection and mail-flow settings.</span></span>
  
```Powershell
#***********************************************************************
# makeparam helper function
#****************************************************************************
 function makeparam ([string]$ParamName, [string[]] $ParamValue) {
    $FormattedParam = ""
    If($ParamValue.Count -gt 0) {
        $FormattedParam = " -$ParamName "
        Foreach ($value in $ParamValue) {
        If($value -eq "True") {$FormattedParam = " -$ParamName" + ":`$True,"}
        else{
            If($value -eq "False") {$FormattedParam = " -$ParamName" + ":`$False,"}
                else{$FormattedParam += "`"$value`","}
            }
        }
        $FormattedParam = $FormattedParam.TrimEnd(",")
    }
    Return $FormattedParam       
 }
#****************************************************************************
# Variables
#****************************************************************************
$outfile = ".\Settings.ps1"
rm -erroraction 'silentlycontinue' $outfile
#****************************************************************************
# HostedContentFilterPolicy
#****************************************************************************
$HostedContentFilterPolicys = Import-Clixml ".\HostedContentFilterPolicy.xml"
$HostedContentFilterPolicyCount = $HostedContentFilterPolicys.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedContentFilterPolicyCount Inbound Connectors"
    ForEach ($HostedContentFilterPolicy in $HostedContentFilterPolicys) {
        $HostedContentFilterPolicyCmdlet = "New-HostedContentFilterPolicy"
        if($HostedContentFilterPolicy.Name -eq "Default") {$HostedContentFilterPolicyCmdlet = "Set-HostedContentFilterPolicy -Identity Default"}
        else {
        $HostedContentFilterPolicyCmdlet += makeparam "Name" $HostedContentFilterPolicy.Name
        }
        $HostedContentFilterPolicyCmdlet += makeparam "AddXHeaderValue" $HostedContentFilterPolicy.AddXHeaderValue 
        $HostedContentFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedContentFilterPolicy.AdminDisplayName
        $HostedContentFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedContentFilterPolicyCmdlet += makeparam "DownloadLink" $HostedContentFilterPolicy.DownloadLink 
        $HostedContentFilterPolicyCmdlet += makeparam "EnableEndUserSpamNotifications" $HostedContentFilterPolicy.EnableEndUserSpamNotifications 
        $HostedContentFilterPolicyCmdlet += makeparam "EnableLanguageBlockList" $HostedContentFilterPolicy.EnableLanguageBlockList 
        $HostedContentFilterPolicyCmdlet += makeparam "EnableRegionBlockList" $HostedContentFilterPolicy.EnableRegionBlockList
        if($HostedContentFilterPolicy.EndUserSpamNotificationCustomFromAddress.Length -gt 0)
        {
            $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomFromAddress" $HostedContentFilterPolicy.EndUserSpamNotificationCustomFromAddress
        }
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomFromName" $HostedContentFilterPolicy.EndUserSpamNotificationCustomFromName 
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationCustomSubject" $HostedContentFilterPolicy.EndUserSpamNotificationCustomSubject 
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationFrequency" $HostedContentFilterPolicy.EndUserSpamNotificationFrequency 
        $HostedContentFilterPolicyCmdlet += makeparam "EndUserSpamNotificationLanguage" $HostedContentFilterPolicy.EndUserSpamNotificationLanguage
        $HostedContentFilterPolicyCmdlet += makeparam "LanguageBlockList" $HostedContentFilterPolicy.LanguageBlockList
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamBulkMail" $HostedContentFilterPolicy.MarkAsSpamBulkMail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamEmbedTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamEmbedTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamEmptyMessages" $HostedContentFilterPolicy.MarkAsSpamEmptyMessages
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFormTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamFormTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFramesInHtml" $HostedContentFilterPolicy.MarkAsSpamFramesInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamFromAddressAuthFail" $HostedContentFilterPolicy.MarkAsSpamFromAddressAuthFail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamJavaScriptInHtml" $HostedContentFilterPolicy.MarkAsSpamJavaScriptInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamNdrBackscatter" $HostedContentFilterPolicy.MarkAsSpamNdrBackscatter
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamObjectTagsInHtml" $HostedContentFilterPolicy.MarkAsSpamObjectTagsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamSensitiveWordList" $HostedContentFilterPolicy.MarkAsSpamSensitiveWordList
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamSpfRecordHardFail" $HostedContentFilterPolicy.MarkAsSpamSpfRecordHardFail
        $HostedContentFilterPolicyCmdlet += makeparam "MarkAsSpamWebBugsInHtml" $HostedContentFilterPolicy.MarkAsSpamWebBugsInHtml
        $HostedContentFilterPolicyCmdlet += makeparam "ModifySubjectValue" $HostedContentFilterPolicy.ModifySubjectValue
        $HostedContentFilterPolicyCmdlet += makeparam "Organization" $HostedContentFilterPolicy.Organization
        $HostedContentFilterPolicyCmdlet += makeparam "QuarantineRetentionPeriod" $HostedContentFilterPolicy.QuarantineRetentionPeriod
        $HostedContentFilterPolicyCmdlet += makeparam "RedirectToRecipients" $HostedContentFilterPolicy.RedirectToRecipients
        $HostedContentFilterPolicyCmdlet += makeparam "RegionBlockList" $HostedContentFilterPolicy.RegionBlockList
        $HostedContentFilterPolicyCmdlet += makeparam "SpamAction" $HostedContentFilterPolicy.SpamAction
        $HostedContentFilterPolicyCmdlet += makeparam "TestModeBccToRecipients" $HostedContentFilterPolicy.TestModeBccToRecipients
        Add-Content $outfile "`n$HostedContentFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Content Policy Filters to add."
 }
#****************************************************************************
# HostedContentFilterRule
#****************************************************************************
$HostedContentFilterRules = Import-Clixml ".\HostedContentFilterRule.xml"
$HostedContentFilterRuleCount = $HostedContentFilterRules.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedContentFilterRuleCount Hosted Content Filter Rules"
    ForEach ($HostedContentFilterRule in $HostedContentFilterRules) {
        $HostedContentFilterRuleCmdlet = "New-HostedContentFilterRule"
        if($HostedContentFilterRule.Name -eq "Default") {$HostedContentFilterRuleCmdlet = "Set-HostedContentFilterRule Default"}
        $HostedContentFilterRuleCmdlet += makeparam "Name" $HostedContentFilterRule.Name
        $HostedContentFilterRuleCmdlet  += makeparam "HostedContentFilterPolicy" $HostedContentFilterRule.HostedContentFilterPolicy
        $HostedContentFilterRuleCmdlet += makeparam "Comments" $HostedContentFilterRule.Comments
        $HostedContentFilterRuleCmdlet += " -Confirm:`$False"
        $HostedContentFilterRuleCmdlet += makeparam "Enabled" $HostedContentFilterRule.Enabled
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfRecipientDomainIs" $HostedContentFilterRule.ExceptIfRecipientDomainIs
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfSentTo" $HostedContentFilterRule.ExceptIfSentTo
        $HostedContentFilterRuleCmdlet += makeparam "ExceptIfSentToMemberOf" $HostedContentFilterRule.ExceptIfSentToMemberOf
        $HostedContentFilterRuleCmdlet += makeparam "Priority" $HostedContentFilterRule.Priority
        $HostedContentFilterRuleCmdlet += makeparam "RecipientDomainIs" $HostedContentFilterRule.RecipientDomainIs
        $HostedContentFilterRuleCmdlet += makeparam "SentTo" $HostedContentFilterRule.SentTo
        $HostedContentFilterRuleCmdlet += makeparam "SentToMemberOf" $HostedContentFilterRule.SentToMemberOf        
        Add-Content $outfile "`n$HostedContentFilterRuleCmdlet"
    }
 }else{
    Write-Host "No Hosted Content Filter Rules to add."
 }
#****************************************************************************
# HostedOutboundSpamFilterPolicy
#****************************************************************************
$HostedOutboundSpamFilterPolicys = Import-Clixml ".\HostedOutboundSpamFilterPolicy.xml"
$HostedOutboundSpamFilterPolicyCount = $HostedOutboundSpamFilterPolicys.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedOutboundSpamFilterPolicyCount Hosted Outbound Spam Filter Policies"
    ForEach ($HostedOutboundSpamFilterPolicy in $HostedOutboundSpamFilterPolicys) {
        $HostedOutboundSpamFilterPolicyCmdlet = "Set-HostedOutboundSpamFilterPolicy Default"
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedOutboundSpamFilterPolicy.AdminDisplayName
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "BccSuspiciousOutboundAdditionalRecipients" $HostedOutboundSpamFilterPolicy.BccSuspiciousOutboundAdditionalRecipients 
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "BccSuspiciousOutboundMail" $HostedOutboundSpamFilterPolicy.BccSuspiciousOutboundMail
        $HostedOutboundSpamFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedOutboundSpamFilterPolicyCmdlet += makeparam "NotifyOutboundSpam" $HostedOutboundSpamFilterPolicy.NotifyOutboundSpam
        $NotifyOutboundSpamRecipients  += makeparam "NotifyOutboundSpamRecipients" $HostedOutboundSpamFilterPolicy.NotifyOutboundSpamRecipients
        Add-Content $outfile "`n$HostedOutboundSpamFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Outbound Spam Filter Policies to add."
 }
#****************************************************************************
# HostedConnectionFilterPolicy
#****************************************************************************
$HostedConnectionFilterPolicys = Import-Clixml ".\HostedConnectionFilterPolicy.xml"
$HostedConnectionFilterPolicyCount = $HostedConnectionFilterPolicys.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $HostedConnectionFilterPolicyCount Hosted Connection Filter Policies"
    ForEach ($HostedConnectionFilterPolicy in $HostedConnectionFilterPolicys) {
        $HostedConnectionFilterPolicyCmdlet = "Set-HostedConnectionFilterPolicy"
        $HostedConnectionFilterPolicyCmdlet += makeparam "Identity" $HostedConnectionFilterPolicy.Name
        $HostedConnectionFilterPolicyCmdlet += makeparam "AdminDisplayName" $HostedConnectionFilterPolicy.AdminDisplayName
        $HostedConnectionFilterPolicyCmdlet += " -Confirm:`$False"
        $HostedConnectionFilterPolicyCmdlet += makeparam "EnableSafeList" $HostedConnectionFilterPolicy.EnableSafeList
        $HostedConnectionFilterPolicyCmdlet += makeparam "IPAllowList" $HostedConnectionFilterPolicy.IPAllowList
        $HostedConnectionFilterPolicyCmdlet += makeparam "IPBlockList" $HostedConnectionFilterPolicy.IPBlockList
        
        Add-Content $outfile "`n$HostedConnectionFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Hosted Connection Filter Policies to add."
 }
#****************************************************************************
# MalwareFilterPolicy
#****************************************************************************
$MalwareFilterPolicys = Import-Clixml ".\MalwareFilterPolicy.xml"
$MalwareFilterPolicyCount = $MalwareFilterPolicys.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $MalwareFilterPolicyCount Malware Filter Policies"
    ForEach ($MalwareFilterPolicy in $MalwareFilterPolicys) {
        $MalwareFilterPolicyCmdlet = "New-MalwareFilterPolicy"
        if($MalwareFilterPolicy.Name -eq "Default") {$MalwareFilterPolicyCmdlet = "Set-MalwareFilterPolicy Default"}
        else {
        $MalwareFilterPolicyCmdlet += makeparam "Name" $MalwareFilterPolicy.Name
        }
        $MalwareFilterPolicyCmdlet += makeparam "Action" $MalwareFilterPolicy.Action
        $MalwareFilterPolicyCmdlet += makeparam "DeleteAttachmentAndUseDefaultAlertText" $MalwareFilterPolicy.DeleteAttachmentAndUseDefaultAlertText
        $MalwareFilterPolicyCmdlet += makeparam "DeleteAttachmentAndUseCustomAlertText" $MalwareFilterPolicy.DeleteAttachmentAndUseCustomAlertText
        $MalwareFilterPolicyCmdlet += makeparam "AdminDisplayName" $MalwareFilterPolicy.AdminDisplayName
        $MalwareFilterPolicyCmdlet += " -Confirm:`$False"
        $MalwareFilterPolicyCmdlet += makeparam "CustomAlertText" $MalwareFilterPolicy.CustomAlertText
        $MalwareFilterPolicyCmdlet += makeparam "CustomExternalBody" $MalwareFilterPolicy.CustomExternalBody
        $MalwareFilterPolicyCmdlet += makeparam "CustomExternalSubject" $MalwareFilterPolicy.CustomExternalSubject
        if($MalwareFilterPolicy.CustomFromAddress.Length -gt 0) {
            $MalwareFilterPolicyCmdlet += makeparam "CustomFromAddress" $MalwareFilterPolicy.CustomFromAddress
        }
        $MalwareFilterPolicyCmdlet += makeparam "CustomFromName" $MalwareFilterPolicy.CustomFromName
        $MalwareFilterPolicyCmdlet += makeparam "CustomInternalBody" $MalwareFilterPolicy.CustomInternalBody
        $MalwareFilterPolicyCmdlet += makeparam "CustomInternalSubject" $MalwareFilterPolicy.CustomInternalSubject
        $MalwareFilterPolicyCmdlet += makeparam "CustomNotifications" $MalwareFilterPolicy.CustomNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableExternalSenderAdminNotifications" $MalwareFilterPolicy.EnableExternalSenderAdminNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableExternalSenderNotifications" $MalwareFilterPolicy.EnableExternalSenderNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableInternalSenderAdminNotifications" $MalwareFilterPolicy.EnableInternalSenderAdminNotifications
        $MalwareFilterPolicyCmdlet += makeparam "EnableInternalSenderNotifications" $MalwareFilterPolicy.EnableInternalSenderNotifications
        if($MalwareFilterPolicy.ExternalSenderAdminAddress.Length -gt 0) {
        $MalwareFilterPolicyCmdlet += makeparam "ExternalSenderAdminAddress" $MalwareFilterPolicy.ExternalSenderAdminAddress
        }
        if($MalwareFilterPolicy.InternalSenderAdminAddress.Length -gt 0) {
        $MalwareFilterPolicyCmdlet += makeparam "InternalSenderAdminAddress" $MalwareFilterPolicy.InternalSenderAdminAddress
        }
        Add-Content $outfile "`n$MalwareFilterPolicyCmdlet"
    }
 }else{
    Write-Host "No Malware Filter Policies to add."
 }
#****************************************************************************
# MalwareFilterRule
#****************************************************************************
$MalwareFilterRules = Import-Clixml ".\MalwareFilterRule.xml"
$MalwareFilterRuleCount = $MalwareFilterRules.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $MalwareFilterRuleCount Malware Filter Rules"
    ForEach ($MalwareFilterRule in $MalwareFilterRules) {
        $MalwareFilterRuleCmdlet = "New-MalwareFilterRule"
        if($MalwareFilterRule.Name -eq "Default") {$MalwareFilterRuleCmdlet = "Set-MalwareFilterPolicy Default"}
        $MalwareFilterRuleCmdlet += makeparam "Name" $MalwareFilterRule.Name
        $MalwareFilterRuleCmdlet += makeparam "MalwareFilterPolicy" $MalwareFilterRule.MalwareFilterPolicy
        $MalwareFilterRuleCmdlet += makeparam "Comments" $MalwareFilterRule.Comments
        $MalwareFilterRuleCmdlet += " -Confirm:`$False"
        $MalwareFilterRuleCmdlet += makeparam "Enabled" $MalwareFilterRule.Enabled
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfRecipientDomainIs" $MalwareFilterRule.ExceptIfRecipientDomainIs
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfSentTo" $MalwareFilterRule.ExceptIfSentTo
        $MalwareFilterRuleCmdlet += makeparam "ExceptIfSentToMemberOf" $MalwareFilterRule.ExceptIfSentToMemberOf
        $MalwareFilterRuleCmdlet += makeparam "RecipientDomainIs" $MalwareFilterRule.RecipientDomainIs
        $MalwareFilterRuleCmdlet += makeparam "SentTo" $MalwareFilterRule.SentTo
        $MalwareFilterRuleCmdlet += makeparam "SentToMemberOf" $MalwareFilterRule.SentToMemberOf       
        Add-Content $outfile "`n$MalwareFilterRuleCmdlet"
    }
 }else{
    Write-Host "No Malware Filter Rules to add."
 }
#****************************************************************************
# InboundConnectors
#****************************************************************************
$InboundConnectors = Import-Clixml ".\InboundConnector.xml"
$InboundConnectorCount = $InboundConnectors.Name.Count
if($InboundConnectorCount -gt 0){
    Write-Host "Importing $InboundConnectorCount Inbound Connectors"
    ForEach ($InboundConnector in $InboundConnectors) {
        $InboundConnectorCmdlet = "New-InboundConnector"
        $InboundConnectorCmdlet += makeparam "Name" $InboundConnector.Name
        $InboundConnectorCmdlet += makeparam "SenderDomains" $InboundConnector.SenderDomains
        
        If($InboundConnector.AssociatedAcceptedDomains.Count -gt 0) {
            If($InboundConnector.AssociatedAcceptedDomains[0].Contains("/")) {
                # This connector was created in an EOP Standard tenant
                # Strip out just the domain name
                $InboundConnectorCmdlet += " -AssociatedAcceptedDomains "
                ForEach  ($accepteddomain in $InboundConnectors.AssociatedAcceptedDomains) {
                    $accepteddomain = $accepteddomain.SubString($accepteddomain.LastIndexOf("/")+1)
                    $InboundConnectorCmdlet += "`"$accepteddomain`","
                }
                $InboundConnectorCmdlet = $InboundConnectorCmdlet.TrimEnd(",")
            }else{
                $InboundConnectorCmdlet += makeparam "AssociatedAcceptedDomains" $InboundConnector.AssociatedAcceptedDomains
            }
        }
        
        $InboundConnectorCmdlet += makeparam "CloudServicesMailEnabled" $InboundConnector.CloudServicesMailEnabled 
        $InboundConnectorCmdlet += makeparam "Comment" $InboundConnector.Comment 
        $InboundConnectorCmdlet += " -Confirm:`$False"
        $InboundConnectorCmdlet += makeparam "ConnectorSource" $InboundConnector.ConnectorSource
        $InboundConnectorCmdlet += makeparam "ConnectorType" $InboundConnector.ConnectorType
        $InboundConnectorCmdlet += makeparam "Enabled" $InboundConnector.Enabled
        $InboundConnectorCmdlet += makeparam "RequireTls" $InboundConnector.RequireTls 
        $InboundConnectorCmdlet += makeparam "RestrictDomainsToCertificate" $InboundConnector.RestrictDomainsToCertificate
        $InboundConnectorCmdlet += makeparam "RestrictDomainsToIPAddresses" $InboundConnector.RestrictDomainsToIPAddresses
        $InboundConnectorCmdlet += makeparam "SenderIPAddresses" $InboundConnector.SenderIPAddresses
        $InboundConnectorCmdlet += makeparam "TlsSenderCertificateName" $InboundConnector.TlsSenderCertificateName
        Add-Content $outfile "`n$InboundConnectorCmdlet"
     }
}else{
    Write-Host "No Inbound Connectors to add."
 }
#****************************************************************************
# OutboundConnector
#****************************************************************************
$OutboundConnectors = Import-Clixml ".\OutboundConnector.xml"
$OutboundConnectorCount = $OutboundConnectors.Name.Count
if($OutboundConnectorCount -gt 0){
    Write-Host "Importing $OutboundConnectorCount Outbound Connectors"
    ForEach ($OutboundConnector in $OutboundConnectors) {
        $OutboundConnectorCmdlet = "New-OutboundConnector"
        $OutboundConnectorCmdlet += makeparam "Name" $OutboundConnector.Name
        $OutboundConnectorCmdlet += makeparam "AllAcceptedDomains" $OutboundConnector.AllAcceptedDomains
        $OutboundConnectorCmdlet += makeparam "BypassValidation" $OutboundConnector.BypassValidation
        $OutboundConnectorCmdlet += makeparam "CloudServicesMailEnabled" $OutboundConnector.CloudServicesMailEnabled
        $OutboundConnectorCmdlet += makeparam "Comment" $OutboundConnector.Comment
        $OutboundConnectorCmdlet += " -Confirm:`$False"
        $OutboundConnectorCmdlet += makeparam "ConnectorSource" $OutboundConnector.ConnectorSource
        $OutboundConnectorCmdlet += makeparam "ConnectorType" $OutboundConnector.ConnectorType
        $OutboundConnectorCmdlet += makeparam "IsTransportRuleScoped" $OutboundConnector.IsTransportRuleScoped
        $OutboundConnectorCmdlet += makeparam "RecipientDomains" $OutboundConnector.RecipientDomains
        $OutboundConnectorCmdlet += makeparam "RouteAllMessagesViaOnPremises" $OutboundConnector.RouteAllMessagesViaOnPremises
        $OutboundConnectorCmdlet += makeparam "SmartHosts" $OutboundConnector.SmartHosts
        $OutboundConnectorCmdlet += makeparam "TlsDomain" $OutboundConnector.TlsDomain
        $OutboundConnectorCmdlet += makeparam "TlsSettings" $OutboundConnector.TlsSettings
        $OutboundConnectorCmdlet += makeparam "UseMXRecord" $OutboundConnector.UseMXRecord
        Add-Content $outfile "`n$OutboundConnectorCmdlet"
    }
 }else{
    Write-Host "No Outbound Connectors to add."
 }
#*****************************************************************************
# TransportRule
#*****************************************************************************
Add-Content $outfile "`n[Byte[]]$Data = Get-Content -Path `".TransportRules.xml`" -Encoding Byte -ReadCount 0"
Add-Content $outfile "`nImport-TransportRuleCollection -FileData $Data"
#****************************************************************************
# Domain Type
#****************************************************************************
$Domains = Import-Clixml ".\Domains.xml"
$DomainCount = $Domains.Name.Count
if($HostedContentFilterPolicyCount -gt 0){
    Write-Host "Importing $DomainCount Domains"
    ForEach ($Domain in $Domains) {
        $DomainCmdlet = "Set-AcceptedDomain"
        $DomainCmdlet += makeparam "Identity" $Domain.Name
        $DomainCmdlet += makeparam "DomainType" $Domain.DomainType
        Add-Content $outfile "`n$DomainCmdlet"
    }
 }else{
    Write-Host "No Domains to add."
 } 
 
```

## <a name="step-8-revert-your-dns-settings-to-stop-mail-queuing"></a><span data-ttu-id="c028c-179">Schritt 8: Wiederherstellen Ihrer DNS-Einstellungen zum Beenden der E-Mail-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="c028c-179">Step 8: Revert your DNS settings to stop mail queuing</span></span>

<span data-ttu-id="c028c-180">Wenn Sie Ihre MX-Einträge auf eine ungültige Adresse festlegen, damit die Absender e-Mails während des Übergangs in die Warteschlange eingereiht werden, müssen Sie Sie auf den richtigen Wert festlegen, wie im [Admin Center](https://admin.microsoft.com)angegeben.</span><span class="sxs-lookup"><span data-stu-id="c028c-180">If you chose to set your MX records to an invalid address to cause the senders to queue mail during your transition, you'll need to set them back to the correct value as specified in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="c028c-181">Weitere Informationen über das Konfigurieren des DNS finden Sie unter [Erstellen von DNS-Einträgen für Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span><span class="sxs-lookup"><span data-stu-id="c028c-181">For more information about configuring DNS, see [Create DNS records for Office 365](https://go.microsoft.com/fwlink/p/?LinkId=304219).</span></span>
  


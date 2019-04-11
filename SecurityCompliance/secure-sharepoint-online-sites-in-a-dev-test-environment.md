---
title: Sichern von SharePoint Online-Websites in einer Entwicklungs-/Testumgebung
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/09/2019
ms.audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 06af70f3-e7dc-4ee2-a385-fb4d61a5e93b
description: 'Zusammenfassung: Informationen zum Erstellen von öffentlichen, privaten, vertraulichen und streng vertraulichen SharePoint Online-Teamwebsites in einer Entwicklungs-/Testumgebung.'
ms.openlocfilehash: e1d5e6f98679e2efb4d5048009971d88f90181e8
ms.sourcegitcommit: 19d27ff836ee7fa1f8a4e761e04d928f13f4bfd8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2019
ms.locfileid: "31745307"
---
# <a name="secure-sharepoint-online-sites-in-a-devtest-environment"></a><span data-ttu-id="129ee-103">Sichern von SharePoint Online-Websites in einer Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="129ee-103">Secure SharePoint Online sites in a dev/test environment</span></span>

 <span data-ttu-id="129ee-104">**Zusammenfassung:** Informationen zum Erstellen von öffentlichen, privaten, vertraulichen und streng vertraulichen SharePoint Online-Teamwebsites in einer Entwicklungs-/Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="129ee-104">**Summary:** Create public, private, sensitive, and highly confidential SharePoint Online team sites in a dev/test environment.</span></span>
  
<span data-ttu-id="129ee-105">In diesem Artikel finden Sie Schritt-für-Schritt-Anleitungen zum Erstellen einer Entwicklungs-/Testumgebung, die vier verschiedene Typen von SharePoint Online-Teamwebsites für die [Sichern von SharePoint Online-Websites und -Dateien](secure-sharepoint-online-sites-and-files.md)-Lösung enthält.</span><span class="sxs-lookup"><span data-stu-id="129ee-105">This article provides step-by-step instructions to create a dev/test environment that includes the four different types of SharePoint Online team sites for the [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md) solution.</span></span>
  
![Alle vier Teamwebsites in der sicheren Entwicklungs-/Testumgebung von SharePoint Online.](media/b0fea489-359c-4c85-a0ad-e4efb4a1e47f.png)
  
<span data-ttu-id="129ee-107">Verwenden Sie diese Entwicklungs-/Testumgebung zum Experimentieren mit den Verhaltensweisen beim Schutz von Informationen und zur Feinabstimmung der Einstellungen für Ihre spezifischen Anforderungen vor der Bereitstellung von SharePoint Online-Teamwebsites in der Produktion.</span><span class="sxs-lookup"><span data-stu-id="129ee-107">Use this dev/test environment to experiment with the information protection behaviors and fine-tune settings for your specific needs before deploying SharePoint Online team sites in production.</span></span>
  
## <a name="phase-1-create-your-devtest-environment"></a><span data-ttu-id="129ee-108">Phase 1: Erstellen Ihrer Dev/Test-Umgebung</span><span class="sxs-lookup"><span data-stu-id="129ee-108">Phase 1: Create your dev/test environment</span></span>

<span data-ttu-id="129ee-109">In dieser Phase erhalten Sie Testabonnements für Office 365 und Enterprise Mobility + Security (EMS) für eine fiktive Organisation.</span><span class="sxs-lookup"><span data-stu-id="129ee-109">In this phase, you obtain trial subscriptions for Office 365 and Enterprise Mobility + Security for a fictional organization.</span></span>
  
<span data-ttu-id="129ee-110">Folgen Sie zunächst den Anweisungen in **Phase 2** des Artikels [Office 365-Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="129ee-110">First, follow the instructions in **Phase 2** of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="129ee-111">Als Nächstes registrieren Sie sich für das EMS-Testabonnement und fügen es derselben Organisation wie Ihr Office 365-Testabonnement hinzu.</span><span class="sxs-lookup"><span data-stu-id="129ee-111">Next, sign up for the EMS trial subscription and add it to the same organization as your Office 365 trial subscription.</span></span>
  
1. <span data-ttu-id="129ee-112">Falls erforderlich, melden Sie sich im [Microsoft 365 Admin Center](https://admin.microsoft.com) mit den Anmeldeinformationen des globalen Administratorkontos für Ihr Testabonnement an.</span><span class="sxs-lookup"><span data-stu-id="129ee-112">If needed, sign in to the admin center with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-113">Klicken Sie im linken Navigationsbereich auf **Abrechnung > Dienste kaufen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-113">On the Office 365 Admin tab, in the left navigation, click **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="129ee-p101">Suchen Sie auf der Seite **Dienste kaufen** den Artikel **Enterprise Mobility + Security E5**. Platzieren Sie den Mauszeiger auf dem Artikelnamen, und klicken Sie auf **Start free trial**.</span><span class="sxs-lookup"><span data-stu-id="129ee-p101">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>
    
4. <span data-ttu-id="129ee-116">Klicken Sie auf der Seite für die **Bestätigung Ihrer Bestellung** auf **Jetzt versuchen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-116">On the **Confirm your order** page, click **Try now**.</span></span>
    
5. <span data-ttu-id="129ee-117">Klicken Sie auf der Seite **Bestellbestätigung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-117">On the **Order receipt** page, click **Continue**.</span></span>
    
<span data-ttu-id="129ee-118">Aktivieren Sie als Nächstes die Enterprise Mobility + Security E5-Lizenz für Ihr globales Administratorkonto.</span><span class="sxs-lookup"><span data-stu-id="129ee-118">Next, enable the Enterprise Mobility + Security E5 license for your global administrator account.</span></span>
  
1. <span data-ttu-id="129ee-119">Klicken Sie auf der Registerkarte **Microsoft 365 Admin Center** in Ihrem Browser im linken Navigationsbereich auf **Benutzer > Aktive Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="129ee-119">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>
    
2. <span data-ttu-id="129ee-120">Klicken Sie auf Ihr globales Administratorkonto und dann auf **Bearbeiten**, um die **Produktlizenzen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="129ee-120">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>
    
3. <span data-ttu-id="129ee-121">Setzen Sie im Bereich **Product licenses** die Produktlizenz für **Enterprise Mobility + Security E5** auf **On**. Klicken Sie auf **Speichern** und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-121">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups-and-users"></a><span data-ttu-id="129ee-122">Phase 2: Erstellen und Konfigurieren der Azure Active Directory(AD)-Gruppen und -Benutzer</span><span class="sxs-lookup"><span data-stu-id="129ee-122">Phase 2: Create and configure your Azure Active Directory (AD) groups and users</span></span>

<span data-ttu-id="129ee-123">In dieser Phase erstellen und konfigurieren Sie die Azure AD-Gruppen und -Benutzer für eine fiktive Organisation.</span><span class="sxs-lookup"><span data-stu-id="129ee-123">In this phase, you create and configure the Azure AD groups and users for your fictional organization.</span></span>
  
<span data-ttu-id="129ee-124">Erstellen Sie zuerst eine Reihe von Gruppen für eine typische Organisation mit dem Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="129ee-124">First, create a set of groups for a typical organization with the Azure portal.</span></span>
  
1. <span data-ttu-id="129ee-p102">Erstellen Sie eine neue Registerkarte im Browser, und wechseln Sie dann zum Azure-Portal unter [https://portal.azure.com](https://portal.azure.com). Falls erforderlich, melden Sie sich mit den Anmeldeinformationen des globalen Administratorkontos für Ihr Office 365 E5-Testabonnement an.</span><span class="sxs-lookup"><span data-stu-id="129ee-p102">Create a separate tab in your browser, and then go to the Azure portal at [https://portal.azure.com](https://portal.azure.com). If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-127">Klicken Sie im Azure-Portal auf **Azure Active Directory > Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-127">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="129ee-128">Klicken Sie auf dem Blatt **Gruppen - Alle Gruppen** auf **+ Neue Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="129ee-128">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="129ee-129">Auf dem Blatt **Gruppe**:</span><span class="sxs-lookup"><span data-stu-id="129ee-129">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="129ee-130">Wählen Sie **Office 365** unter **Gruppentyp** aus.</span><span class="sxs-lookup"><span data-stu-id="129ee-130">Select **Office 365** in **Group type**.</span></span>
    
  - <span data-ttu-id="129ee-131">Geben **C-Suite** unter **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-131">Type **C-Suite** in **Name**.</span></span>
    
  - <span data-ttu-id="129ee-132">Wählen Sie **Zugewiesen** unter **Mitgliedschaftstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="129ee-132">Select **Assigned** in **Membership type**.</span></span>
      
5. <span data-ttu-id="129ee-133">Klicken Sie auf **Erstellen**, und schließen Sie dann das Blatt **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="129ee-133">Click **Create**, and then close the **Group** blade.</span></span>
    
6. <span data-ttu-id="129ee-134">Wiederholen Sie die Schritte 3 bis 5 für die folgenden Gruppennamen:</span><span class="sxs-lookup"><span data-stu-id="129ee-134">Repeat steps 3-5 for the following group names:</span></span>
    
  - <span data-ttu-id="129ee-135">IT-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-135">IT staff</span></span>
    
  - <span data-ttu-id="129ee-136">Forschungsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-136">Research staff</span></span>
    
  - <span data-ttu-id="129ee-137">Reguläre Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-137">Regular staff</span></span>
    
  - <span data-ttu-id="129ee-138">Marketingmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-138">Marketing staff</span></span>
    
  - <span data-ttu-id="129ee-139">Vertriebsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-139">Sales staff</span></span>
    
7. <span data-ttu-id="129ee-140">Lassen Sie die Registerkarte für das Azure-Portal in Ihrem Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="129ee-140">Keep the Azure portal tab in your browser open.</span></span>
    
<span data-ttu-id="129ee-141">Im nächsten Schritt wird die automatische Lizenzierung konfiguriert, sodass Mitgliedern von Gruppen automatisch Lizenzen für Ihre Office 365- und EMS-Abonnements zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="129ee-141">Next, you configure automatic licensing so that members of your groups are automatically assigned licenses for your Office 365 and EMS subscriptions.</span></span>
  
1. <span data-ttu-id="129ee-142">Klicken Sie im Azure-Portal auf **Azure Active Directory > Lizenzen > Alle Produkte**.</span><span class="sxs-lookup"><span data-stu-id="129ee-142">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="129ee-143">Wählen Sie in der Liste **Enterprise Mobility + Security E5** und **Office 365 Enterprise E5** aus, und klicken Sie dann auf **Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-143">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **Assign**.</span></span>
    
3. <span data-ttu-id="129ee-144">Klicken Sie auf dem Blatt **Lizenz zuweisen** auf **Benutzer und Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-144">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="129ee-145">Wählen Sie in der Liste der Gruppen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="129ee-145">In the list of groups, select the following:</span></span>
    
  - <span data-ttu-id="129ee-146">C-Suite</span><span class="sxs-lookup"><span data-stu-id="129ee-146">C-Suite</span></span>
    
  - <span data-ttu-id="129ee-147">IT-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-147">IT staff</span></span>
    
  - <span data-ttu-id="129ee-148">Forschungsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-148">Research staff</span></span>
    
  - <span data-ttu-id="129ee-149">Reguläre Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-149">Regular staff</span></span>
    
  - <span data-ttu-id="129ee-150">Marketingmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-150">Marketing staff</span></span>
    
  - <span data-ttu-id="129ee-151">Vertriebsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="129ee-151">Sales staff</span></span>
    
5. <span data-ttu-id="129ee-152">Klicken Sie auf **Auswählen** und dann auf **Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-152">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="129ee-153">Schließen Sie die Registerkarte für das Azure Portal in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="129ee-153">Close the Azure portal tab in your browser.</span></span>
    
<span data-ttu-id="129ee-154">Danach müssen Sie [eine Verbindung mit dem Azure Active Directory PowerShell für Graph-Module herstellen](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="129ee-154">Next, you [Connect with the Azure Active Directory V2 PowerShell module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="129ee-155">Geben Sie den Namen Ihrer Organisation, Ihren Standort und ein gemeinsames Kennwort ein, und führen Sie dann die folgenden Befehle über die PowerShell-Eingabeaufforderung oder in der ISE-Umgebung (Integrated Script Environment) aus, um Benutzerkonten zu erstellen und sie zu den Gruppen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="129ee-155">Fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE) to create user accounts and add them to their groups:</span></span>
  
```
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$groupName="C-Suite"
$userNames=@("CEO","CFO","CIO") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Research staff"
$userNames=@("Researcher1") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Regular staff"
$userNames=@("Regular1", "Regular2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Marketing staff"
$userNames=@("Marketing1", "Marketing2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Sales staff"
$userNames=@("SalesPerson1") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
```

> [!NOTE]
> <span data-ttu-id="129ee-156">Für die Automatisierung und Vereinfachung der Konfiguration einer Dev/Test-Umgebung wird hier ein gemeinsames Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="129ee-156">The use of a common password here is for automation and ease of configuration for a dev/test environment.</span></span> <span data-ttu-id="129ee-157">Natürlich ist davon bei Produktionsabonnements dringend abzuraten.</span><span class="sxs-lookup"><span data-stu-id="129ee-157">Obviously, this is highly discouraged for production subscriptions.</span></span> 
  
<span data-ttu-id="129ee-158">Gehen Sie folgendermaßen vor, um sicherzustellen, dass die gruppenbasierte Lizenzierung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="129ee-158">Use these steps to verify that group-based licensing is working correctly.</span></span>
  
1. <span data-ttu-id="129ee-159">Klicken Sie auf der Registerkarte **Microsoft Office Home** in Ihrem Browser auf die Kachel **Admin**.</span><span class="sxs-lookup"><span data-stu-id="129ee-159">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="129ee-160">Klicken Sie auf der neuen Registerkarte **Office Admin Center** des Browsers auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="129ee-160">From the new **Office Admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="129ee-161">Klicken Sie in der Liste der Benutzer auf **CEO**.</span><span class="sxs-lookup"><span data-stu-id="129ee-161">In the list of users, click **CEO**.</span></span>
    
4. <span data-ttu-id="129ee-162">Stellen Sie im Bereich, der die Eigenschaften des Benutzerkontos **CEO** anzeigt, sicher, dass ihm die Lizenzen **Enterprise Mobility + Security E5** und **Office 365 Enterprise E5** zugewiesen wurden (in **Produktlizenzen**).</span><span class="sxs-lookup"><span data-stu-id="129ee-162">In the pane that lists the properties of the **CEO** user account, verify that it has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>
    
## <a name="phase-3-create-office-365-retention-labels"></a><span data-ttu-id="129ee-163">Phase 3: Erstellen von Office 365-Aufbewahrungsbezeichnungen</span><span class="sxs-lookup"><span data-stu-id="129ee-163">Phase 3: Create Office 365 labels</span></span>

<span data-ttu-id="129ee-164">In dieser Phase erstellen Sie die Aufbewahrungsbezeichnungen für die verschiedenen Sicherheitsstufen für Dokumentordner für SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="129ee-164">In this phase, you create the labels for the different levels of security for SharePoint Online team site documents folders.</span></span>


1. <span data-ttu-id="129ee-165">Melden Sie sich beim [Microsoft 365 Compliance-Portal](https://compliance.microsoft.com) mit Ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="129ee-165">Sign in to the Microsoft 365 admin center (  ) with your global administrator account.</span></span>
    
2. <span data-ttu-id="129ee-166">Klicken Sie auf der Registerkarte \*\*Start – Microsoft 365 Compliance \*\* im Browser auf **Klassifizierungen > Bezeichnungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-166">From the **Home - Microsoft 365 Security** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="129ee-167">Klicken Sie auf **Aufbewahrungsbezeichnung > Erstellen einer Bezeichnung**.</span><span class="sxs-lookup"><span data-stu-id="129ee-167">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="129ee-168">Geben Sie im Bereich **Name für Bezeichnung\*\*\*\*Intern Öffentlich** ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-168">On the **Name your label** pane, type **Internal Public**, and then click **Next**.</span></span>

5. <span data-ttu-id="129ee-169">Klicken Sie im Bereich **Dateiplanbeschreibungen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-169">On the **File plan descriptors** pane, fill in as needed, and then click **Next**.</span></span>
    
6. <span data-ttu-id="129ee-170">Legen Sie im Bereich **Bezeichnungseigenschaften**, falls erforderlich, **Aufbewahrung** auf **Ein** fest, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-170">On the Label settings pane, if needed, set Retention to On and configure retention settings.</span></span>
    
7. <span data-ttu-id="129ee-171">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Beschriftung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-171">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="129ee-172">Für die zusätzlichen Beschriftungen klicken Sie auf **Beschriftung erstellen**, und wiederholen Sie dann die Schritte 3 bis 7.</span><span class="sxs-lookup"><span data-stu-id="129ee-172">For your additional labels, click **Create a label**, and then repeat steps 4-7..</span></span>

9. <span data-ttu-id="129ee-173">Wiederholen Sie die Schritte 3 bis 8 für die zusätzlichen Bezeichnungen mit diesen Namen:</span><span class="sxs-lookup"><span data-stu-id="129ee-173">Repeat steps 3-8 for additional labels with these names:</span></span>
    
  - <span data-ttu-id="129ee-174">Private</span><span class="sxs-lookup"><span data-stu-id="129ee-174">Private</span></span>
    
  - <span data-ttu-id="129ee-175">Vertraulich</span><span class="sxs-lookup"><span data-stu-id="129ee-175">Sensitive</span></span>
    
  - <span data-ttu-id="129ee-176">Streng vertraulich</span><span class="sxs-lookup"><span data-stu-id="129ee-176">Highly Confidential</span></span>
  
10. <span data-ttu-id="129ee-177">Klicken Sie im Bereich **Startseite > Bezeichnungen** auf **Bezeichnungen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-177">From the **Home > Labels** pane, click **Publish labels**.</span></span>
    
11. <span data-ttu-id="129ee-178">Klicken Sie im Bereich **Zu veröffentlichende Bezeichnungen wählen** auf **Zu veröffentlichende Bezeichnungen wählen**</span><span class="sxs-lookup"><span data-stu-id="129ee-178">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
12. <span data-ttu-id="129ee-179">Klicken Sie im Bereich **Choose labels** (Bezeichnungen auswählen) auf **Hinzufügen**, wählen Sie alle vier Bezeichnungen aus.</span><span class="sxs-lookup"><span data-stu-id="129ee-179">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
13. <span data-ttu-id="129ee-180">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="129ee-180">Click **Done**.</span></span>
    
14. <span data-ttu-id="129ee-181">Klicken Sie im Bereich **Zu veröffentlichende Bezeichnungen wählen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-181">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
15. <span data-ttu-id="129ee-182">Klicken Sie im Bereich **Speicherorte auswählen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-182">On the **Choose locations** pane, click **Next**.</span></span>
    
16. <span data-ttu-id="129ee-183">Geben Sie im Bereich **Richtlinie benennen** **Beispielorganisation** unter **Name** ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-183">On the **Name your policy** pane, type **Example organization** in **Name**, and then click **Next**.</span></span>
    
17. <span data-ttu-id="129ee-184">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Bezeichnungen veröffentlichen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-184">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>
    
## <a name="phase-4-create-your-sharepoint-online-team-sites"></a><span data-ttu-id="129ee-185">Phase 4: Erstellen von SharePoint Online-Teamwebsites</span><span class="sxs-lookup"><span data-stu-id="129ee-185">Phase 4: Create your SharePoint Online team sites</span></span>

<span data-ttu-id="129ee-186">In dieser Phase erstellen und konfigurieren Sie die vier Typen von SharePoint Online-Teamwebsites für Ihre Beispielorganisation.</span><span class="sxs-lookup"><span data-stu-id="129ee-186">In this phase, you create and configure the four types of SharePoint Online team sites for your example organization.</span></span>
  
### <a name="organization-wide-team-site"></a><span data-ttu-id="129ee-187">Organisationsweite Teamwebsite</span><span class="sxs-lookup"><span data-stu-id="129ee-187">Organization wide team site</span></span>

<span data-ttu-id="129ee-188">Führen Sie folgende Schritte aus, um eine öffentliche SharePoint Online-Basis-Teamwebsite zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="129ee-188">To create a baseline public SharePoint Online team site, do the following:</span></span>
  
1. <span data-ttu-id="129ee-189">Melden Sie sich bei Bedarf mit den Anmeldeinformationen des globalen Administratorkontos beim [Office 365-Portal](https://portal.office.com) Ihres Testabonnements an.</span><span class="sxs-lookup"><span data-stu-id="129ee-189">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-190">Klicken Sie in der Liste der Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="129ee-190">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="129ee-191">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-191">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="129ee-192">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="129ee-192">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="129ee-193">Geben Sie in **Standortname** **Organisationsweit** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-193">In **Site name**, type **Organization wide**.</span></span> 
    
6. <span data-ttu-id="129ee-194">Geben Sie unter **Beschreibung der Teamwebsite** den Text **SharePoint-Website für die gesamte Organisation** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-194">In **Team site description**, type **SharePoint site for the entire organization**.</span></span>
    
7. <span data-ttu-id="129ee-195">Wählen Sie unter **Datenschutzeinstellungen** die Option **Öffentlich - Alle Benutzer in der Organisation können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-195">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-196">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-196">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="129ee-197">Konfigurieren Sie anschließend den Ordner „Dokumente“ der organisationsweiten Teamwebsite für die Bezeichnung „Intern Öffentlich“.</span><span class="sxs-lookup"><span data-stu-id="129ee-197">Next, configure the documents folder of the Organization wide team site for the Internal Public label.</span></span>
  
1. <span data-ttu-id="129ee-198">Klicken Sie auf der Registerkarte **Organisationsweit - Startseite** in Ihrem Browser auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="129ee-198">In the **Organization wide-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="129ee-199">Klicken Sie auf das Symbol für Einstellungen und anschließend auf **Bibliothekeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-199">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="129ee-200">Klicken Sie unter **Berechtigungen und Verwaltung** auf **Bezeichnung auf Elemente in dieser Bibliothek anwenden**.</span><span class="sxs-lookup"><span data-stu-id="129ee-200">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="129ee-201">Wählen Sie unter **Einstellungen -Bezeichnung anwenden** die Option **Intern Öffentlich**, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-201">In **Settings-Apply Label**, select **Internal Public**, and then click **Save**.</span></span>
    
### <a name="project-1-team-site"></a><span data-ttu-id="129ee-202">Teamwebsite für Projekt 1</span><span class="sxs-lookup"><span data-stu-id="129ee-202">Project 1 team site</span></span>

<span data-ttu-id="129ee-203">Führen Sie die folgenden Schritte durch, um eine private SharePoint Online-Basis-Teamwebsite für ein Projekt innerhalb der Organisation zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="129ee-203">To create a baseline private SharePoint Online team site for a project within the organization, do the following:</span></span>
  
1. <span data-ttu-id="129ee-204">Melden Sie sich bei Bedarf mit den Anmeldeinformationen des globalen Administratorkontos beim [Office 365-Portal](https://portal.office.com) Ihres Testabonnements an.</span><span class="sxs-lookup"><span data-stu-id="129ee-204">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-205">Klicken Sie in der Liste der Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="129ee-205">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="129ee-206">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-206">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="129ee-207">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="129ee-207">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="129ee-208">Geben Sie unter **Websitename** den Namen **Projekt 1** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-208">In **Site name**, type **Project 1**.</span></span> 
    
6. <span data-ttu-id="129ee-209">Geben Sie unter **Beschreibung der Teamwebsite** den Text **SharePoint-Website für das Projekt 1** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-209">In **Team site description,** type **SharePoint site for Project 1**.</span></span>
    
7. <span data-ttu-id="129ee-210">Wählen Sie unter **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-210">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-211">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-211">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="129ee-212">Als Nächstes konfigurieren Sie den Ordner „Dokumente“ für die Teamwebsite des Projekts 1 für die private Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="129ee-212">Next, configure the documents folder of the Project 1 team site for the Private label.</span></span>
  
1. <span data-ttu-id="129ee-213">Klicken Sie auf der Registerkarte **Projekt 1 - Startseite** in Ihrem Browser auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="129ee-213">In the **Project 1-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="129ee-214">Klicken Sie auf das Symbol für Einstellungen und anschließend auf **Bibliothekeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-214">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="129ee-215">Klicken Sie unter **Berechtigungen und Verwaltung** auf **Bezeichnung auf Elemente in dieser Bibliothek anwenden**.</span><span class="sxs-lookup"><span data-stu-id="129ee-215">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="129ee-216">Wählen Sie unter **Einstellungen –Bezeichnung anwenden** die Option **Privat**, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-216">In **Settings-Apply Label**, select **Private**, and then click **Save**.</span></span>
    
### <a name="marketing-campaigns-team-site"></a><span data-ttu-id="129ee-217">Marketingkampagnen – Teamwebsite</span><span class="sxs-lookup"><span data-stu-id="129ee-217">Marketing campaigns team site</span></span>

<span data-ttu-id="129ee-218">Führen Sie die folgenden Schritte durch, um eine isolierte, vertrauliche SharePoint Online-Teamwebsite für Marketingkampagnenressourcen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="129ee-218">To create a sensitive-level isolated SharePoint Online team site for marketing campaign resources, do the following:</span></span>

 
1. <span data-ttu-id="129ee-219">Melden Sie sich bei Bedarf mit den Anmeldeinformationen des globalen Administratorkontos beim [Office 365-Portal](https://portal.office.com) Ihres Testabonnements an.</span><span class="sxs-lookup"><span data-stu-id="129ee-219">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-220">Klicken Sie in der Liste der Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="129ee-220">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="129ee-221">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-221">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="129ee-222">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="129ee-222">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="129ee-223">Geben Sie unter **Name der Teamwebsite** **Marketingkampagnen** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-223">In **Team site name**, type **Marketing campaigns**.</span></span>
    
6. <span data-ttu-id="129ee-224">Geben Sie unter **Beschreibung der Teamwebsite** den Text **SharePoint-Website für Marketingkampagnenressourcen (vertraulich)** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-224">In **Team site description**, type **SharePoint site for marketing campaign resources (sensitive)**.</span></span>
    
7.  <span data-ttu-id="129ee-225">Wählen Sie unter **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-225">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-226">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-226">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
9. <span data-ttu-id="129ee-227">Klicken Sie auf der neuen Registerkarte **Marketingkampagnen** in Ihrem Browser auf der Symbolleiste auf das Symbol „Einstellungen", und klicken Sie dann auf **Websiteberechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-227">On the new **Marketing campaigns** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
10. <span data-ttu-id="129ee-228">Klicken Sie im Bereich **Websiteberechtigungen** auf **Erweiterte Berechtigungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-228">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
11. <span data-ttu-id="129ee-229">Klicken Sie auf der neuen Registerkarte **Berechtigungen** in Ihrem Browser auf **Einstellungen für Zugriffsrechteanforderungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-229">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>
    
12. <span data-ttu-id="129ee-230">Deaktivieren Sie im Dialogfeld **Einstellungen für Zugriffsrechteanforderungen** die Kontrollkästchen **Mitgliedern das Freigeben der Website sowie einzelner Dateien und Ordner erlauben** und **Mitgliedern das Einladen von anderen zur Websitemitglieder-Gruppe erlauben**, geben Sie **ITAdmin1@**\<Name Ihrer Organisation>**.onmicrosoft.com** unter **Alle Zugriffsanforderungen an die folgende E-Mail-Adresse senden:** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-230">In the **Access Request Settings** dialog box, clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes, type **ITAdmin1@**\<your organization name>**.onmicrosoft.com** in **Send all requests for access**, and then click **OK**.</span></span>
    
13. <span data-ttu-id="129ee-231">Klicken Sie in der Liste auf **Marketingkampagnenmitglieder**.</span><span class="sxs-lookup"><span data-stu-id="129ee-231">Click **Marketing campaigns Members** in the list.</span></span>
    
14. <span data-ttu-id="129ee-232">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="129ee-232">On the **People and Groups** page, click **New**.</span></span>
    
15. <span data-ttu-id="129ee-233">Geben Sie im Dialogfeld **Freigeben** **Marketing-Mitarbeiter** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="129ee-233">In the **Share** dialog box, type **Marketing staff**, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="129ee-234">Wiederholen Sie die Schritte 14 und 15 für das Benutzerkonto **Researcher1**.</span><span class="sxs-lookup"><span data-stu-id="129ee-234">Repeat steps 14 and 15 for the **Researcher1** user account.</span></span>
    
17. <span data-ttu-id="129ee-235">Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="129ee-235">Click the back button on your browser.</span></span>
    
18. <span data-ttu-id="129ee-236">Klicken Sie in der Liste auf **Marketingkampagnen - Besitzer**.</span><span class="sxs-lookup"><span data-stu-id="129ee-236">Click **Marketing campaigns Owners** in the list.</span></span>
    
19. <span data-ttu-id="129ee-237">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="129ee-237">On the **People and Groups** page, click **New**.</span></span>
    
20. <span data-ttu-id="129ee-238">Geben Sie im Dialogfeld **Freigeben** **IT-Mitarbeiter** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="129ee-238">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>
    
21. <span data-ttu-id="129ee-239">Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="129ee-239">Click the back button on your browser.</span></span>
    
22. <span data-ttu-id="129ee-240">Schließen Sie die Registerkarte **Benutzer und Gruppen** in Ihrem Browser, klicken Sie auf die Registerkarte **Marketingkampagnen - Startseite** in Ihrem Browser, und schließen Sie dann den Bereich **Websiteberechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-240">Close the **People and Groups** tab in your browser, click the **Marketing campaigns-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="129ee-241">Ergebnisse der Konfiguration von Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="129ee-241">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="129ee-242">Die SharePoint-Gruppe **Marketingkampagnen – Mitglieder** enthält nur die Gruppe **Marketingkampagnen** (die das globale Administratorkonto des Benutzers enthält), die Gruppe **Marketingmitarbeiter** (die die Benutzerkonten Marketing1 und Marketing2 enthält), und das Benutzerkonto **Forscher1**.</span><span class="sxs-lookup"><span data-stu-id="129ee-242">The **Marketing campaigns-Members** SharePoint group contains only the **Marketing campaigns** group (which contains the global administrator user account), the **Marketing staff** group (which contains the Marketing1 and Marketing2 user accounts), and the **Researcher1** user account.</span></span>
    
- <span data-ttu-id="129ee-243">Die SharePoint-Gruppe **Marketingkampagnen – Eigentümer** enthält nur die Gruppe **IT-Mitarbeiter** (die nur die Benutzerkonten ITAdmin1 und ITAdmin2 enthält).</span><span class="sxs-lookup"><span data-stu-id="129ee-243">The **Marketing campaigns-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>
    
- <span data-ttu-id="129ee-244">Die SharePoint-Gruppe **Marketingkampagnen – Besucher** enthält keine Gruppen oder Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="129ee-244">The **Marketing campaigns-Visitors** SharePoint group contains no groups or user accounts.</span></span>
    
- <span data-ttu-id="129ee-245">Mitglieder können keine Berechtigungen auf Websiteebene ändern (dies kann nur von Mitgliedern der Gruppe **Marketingkampagnen - Besitzer** ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="129ee-245">Members cannot modify site-level permissions (this can only be done by members of the **Marketing campaigns-Owners** group).</span></span>
    
- <span data-ttu-id="129ee-246">Andere Benutzerkonten können nicht auf die Website oder die zugehörigen Ressourcen zugreifen, Sie können jedoch Zugriff auf die Website anfordern. Dabei wird eine E-Mail an das Postfach des ITAdmin1-Benutzerkontos gesendet.</span><span class="sxs-lookup"><span data-stu-id="129ee-246">Other user accounts cannot access the site or its resources, but can request access to the site, which will send an email to the ITAdmin1 user account mailbox.</span></span>
    
<span data-ttu-id="129ee-247">Konfigurieren Sie anschließend den Ordner „Dokumente“ der Marketingkampagnen-Teamwebsite für die Bezeichnung „Vertraulich“.</span><span class="sxs-lookup"><span data-stu-id="129ee-247">Next, configure the documents folder of the Marketing campaigns team site for the Sensitive label.</span></span>
  
1. <span data-ttu-id="129ee-248">Klicken Sie auf der Registerkarte **Marketingkampagnen - Startseite** in Ihrem Browser auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="129ee-248">In the **Marketing campaigns-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="129ee-249">Klicken Sie auf das Symbol für Einstellungen und anschließend auf **Bibliothekeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-249">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="129ee-250">Klicken Sie unter **Berechtigungen und Verwaltung** auf **Bezeichnung auf Elemente in dieser Bibliothek anwenden**.</span><span class="sxs-lookup"><span data-stu-id="129ee-250">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="129ee-251">Wählen Sie unter **Einstellungen -Bezeichnung anwenden** die Option **Vertraulich**, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-251">In **Settings-Apply Label**, select **Sensitive**, and then click **Save**.</span></span>
    
<span data-ttu-id="129ee-252">Konfigurieren Sie als Nächstes eine Richtlinie zur Verhinderung von Datenverlust (Data Loss Prevention, DLP), die Benutzer benachrichtigt, wenn sie ein Dokument auf einer SharePoint Online-Teamwebsite mit der Bezeichnung „Vertraulich“ freigeben, die die Marketingkampagnenwebsite enthält (außerhalb der Organisation).</span><span class="sxs-lookup"><span data-stu-id="129ee-252">Next, configure a data loss prevention (DLP) policy that notifies users when they share a document on a SharePoint Online team site with the Sensitive label, which includes the Marketing campaigns site, outside the organization.</span></span>

1. <span data-ttu-id="129ee-253">Melden Sie sich beim [Microsoft 365 Compliance-Portal](https://compliance.microsoft.com/) mit Ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="129ee-253">Sign in to the Microsoft 365 admin center (  ) with your global administrator account.</span></span>
    
2. <span data-ttu-id="129ee-254">Klicken Sie auf der Registerkarte **Microsoft 365 Compliance** in Ihrem Browser auf **Richtlinien > Verhinderung von Datenverlust**.</span><span class="sxs-lookup"><span data-stu-id="129ee-254">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="129ee-255">Klicken Sie im Bereich **Verhinderung von Datenverlust** auf **Richtlinie erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-255">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="129ee-256">Klicken Sie im Bereich **Mit einer Vorlage beginnen oder eine benutzerdefinierte Richtlinie erstellen** auf **Benutzerdefiniert**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-256">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="129ee-257">Geben Sie im Bereich **Ihre Richtlinie benennen** den Namen **Bezeichnung „Vertraulich" - SharePoint Online-Teamwebsites** bei **Name** ein, und klicken Sie dann auf **Weiter**</span><span class="sxs-lookup"><span data-stu-id="129ee-257">In the **Name your policy** pane, type **Sensitive label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="129ee-258">Klicken Sie im Bereich **Speicherorte auswählen** auf **Bestimmte Speicherorte auswählen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-258">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="129ee-259">Deaktivieren Sie in der Liste der Speicherorte **Exchange-E-Mail**, **OneDrive-Konten** und **Teams-Chat- und Kanalnachrichten**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-259">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-260">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="129ee-260">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="129ee-261">In der **wählen Sie die Typen der Inhalte zum Schutz** Bereich, klicken Sie auf **hinzufügen** im Dropdown-Listenfeld, und klicken Sie dann auf **Aufbewahrungsbezeichnungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-261">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="129ee-262">Klicken Sie im Bereich **Aufbewahrungsbezeichnungen** auf **Hinzufügen**, wählen Sie die Bezeichnung **Vertraulich** aus, klicken Sie auf **Hinzufügen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="129ee-262">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="129ee-263">Klicken Sie im Bereich **Typen des zu schützenden Inhalts auswählen** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-263">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="129ee-264">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-264">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="129ee-265">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-265">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="129ee-266">Klicken Sie im Bereich **Richtlinentipps und E-Mail-Benachrichtigungen anpassen** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-266">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="129ee-267">Geben oder fügen Sie in das Textfeld einen der folgenden Tipps ein, abhängig davon, ob Sie Azure Information Protection zum Schutz streng vertraulicher Dateien implementiert haben:</span><span class="sxs-lookup"><span data-stu-id="129ee-267">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="129ee-p104">Wenn Sie eine Datei für einen Benutzer außerhalb der Organisation freigeben möchten, laden Sie die Datei herunter, und öffnen Sie sie. Klicken Sie auf „Datei“ > „Dokument schützen“ > „Mit Kennwort verschlüsseln“, und geben Sie dann ein sicheres Kennwort ein. Senden Sie das Kennwort in einer separaten E-Mail oder auf andere Weise.</span><span class="sxs-lookup"><span data-stu-id="129ee-p104">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="129ee-271">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-271">Click **OK**.</span></span>
    
17. <span data-ttu-id="129ee-272">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-272">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="129ee-273">Klicken Sie im Bereich **Möchten Sie die Richtlinie aktivieren oder zunächst testen?** auf **Ja, Richtlinie aktivieren**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-273">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="129ee-274">Klicken Sie im Bereich**Einstellungen überprüfen** auf **Erstellen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-274">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
  
### <a name="company-strategy-team-site"></a><span data-ttu-id="129ee-275">Teamwebsite für Unternehmensstrategie</span><span class="sxs-lookup"><span data-stu-id="129ee-275">Company strategy team site</span></span>

<span data-ttu-id="129ee-276">Führen Sie die folgenden Schritte durch, um eine isolierte, streng vertrauliche SharePoint Online-Teamwebsite für strategische Unternehmensressourcen der Geschäftsführer der Organisation zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="129ee-276">To create an isolated SharePoint Online team site at the highly confidential level for strategic company resources of the chief executives of the organization, do the following:</span></span>
  
1. <span data-ttu-id="129ee-277">Melden Sie sich bei Bedarf mit den Anmeldeinformationen des globalen Administratorkontos beim [Office 365-Portal](https://portal.office.com) Ihres Testabonnements an.</span><span class="sxs-lookup"><span data-stu-id="129ee-277">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="129ee-278">Klicken Sie in der Liste der Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="129ee-278">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="129ee-279">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-279">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="129ee-280">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="129ee-280">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="129ee-281">Geben Sie in **Name der Teamwebsite** **Unternehmensstrategie** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-281">In **Team site name**, type **Company strategy**.</span></span>
    
6. <span data-ttu-id="129ee-282">Geben Sie unter **Beschreibung der Teamwebsite** den Text **SharePoint-Website für Unternehmensstrategie (streng vertraulich)** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-282">In **Team site description**, type **SharePoint site for company strategy (highly confidential)**.</span></span>
    
7.  <span data-ttu-id="129ee-283">Wählen Sie unter **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-283">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-284">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-284">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
9. <span data-ttu-id="129ee-285">Klicken Sie auf der neuen Registerkarte **Unternehmensstrategie** in Ihrem Browser auf der Symbolleiste auf das Symbol „Einstellungen", und klicken Sie dann auf **Websiteberechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-285">On the new **Company strategy** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
10. <span data-ttu-id="129ee-286">Klicken Sie im Bereich **Websiteberechtigungen** auf **Erweiterte Berechtigungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-286">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
11. <span data-ttu-id="129ee-287">Klicken Sie auf der neuen Registerkarte **Berechtigungen** in Ihrem Browser auf **Einstellungen für Zugriffsrechteanforderungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-287">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>
    
12. <span data-ttu-id="129ee-288">Deaktivieren Sie im Dialogfeld **Einstellungen für Zugriffsrechteanforderungen** die Optionen **Mitgliedern das Freigeben der Website sowie einzelner Dateien und Ordner erlauben** und **Mitgliedern das Einladen von anderen zur Websitemitglieder-Gruppe erlauben** (sodass alle drei Kontrollkästchen deaktiviert sind), und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-288">In the **Access Request Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
13. <span data-ttu-id="129ee-289">Klicken Sie in der Liste auf **Unternehmensstrategiemitglieder**.</span><span class="sxs-lookup"><span data-stu-id="129ee-289">Click **Company strategy Members** in the list.</span></span>
    
14. <span data-ttu-id="129ee-290">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="129ee-290">On the **People and Groups** page, click **New**.</span></span>
    
15. <span data-ttu-id="129ee-291">Geben Sie im Dialogfeld **Freigeben** **C-Suite** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="129ee-291">In the **Share** dialog box, type **C-Suite**, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="129ee-292">Klicken Sie in der Liste auf **Unternehmensstrategie - Besitzer**.</span><span class="sxs-lookup"><span data-stu-id="129ee-292">Click **Company strategy Owners** in the list.</span></span>
    
17. <span data-ttu-id="129ee-293">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="129ee-293">On the **People and Groups** page, click **New**.</span></span>
    
18. <span data-ttu-id="129ee-294">Geben Sie im Dialogfeld **Freigeben** **IT-Mitarbeiter** ein, wählen Sie die Option aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="129ee-294">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>
    
19. <span data-ttu-id="129ee-295">Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="129ee-295">Click the back button on your browser.</span></span>
    
20. <span data-ttu-id="129ee-296">Schließen Sie die Registerkarte **Benutzer und Gruppen** in Ihrem Browser, klicken Sie auf die Registerkarte **Unternehmensstrategie - Startseite** in Ihrem Browser, und schließen Sie dann den Bereich **Websiteberechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-296">Close the **People and Groups** tab in your browser, click the **Company strategy-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="129ee-297">Ergebnisse der Konfiguration von Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="129ee-297">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="129ee-298">Die SharePoint-Gruppe **Unternehmensstrategie - Mitglieder** enthält nur die Gruppe **C-Suite** (mit den Benutzerkonten CEO, CFO und CIO) und die Gruppe **Unternehmensstrategie** (mit dem globalen Administratorkonto).</span><span class="sxs-lookup"><span data-stu-id="129ee-298">The **Company strategy-Members** SharePoint group contains only the **C-Suite** group (which contains only the CEO, CFO, and CIO user accounts) and the **Company strategy** group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="129ee-299">Die SharePoint-Gruppe **Unternehmensstrategie - Besitzer** enthält nur die Gruppe **IT-Mitarbeiter** (nur mit den ITAdmin1- und ITAdmin2-Benutzerkonten).</span><span class="sxs-lookup"><span data-stu-id="129ee-299">The **Company strategy-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>
    
- <span data-ttu-id="129ee-300">Die SharePoint-Gruppe **Unternehmensstrategie - Besucher** enthält keine Gruppen oder Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="129ee-300">The **Company strategy-Visitors** SharePoint group contains no groups or user accounts.</span></span>
    
- <span data-ttu-id="129ee-301">Mitglieder können keine Berechtigungen auf Websiteebene ändern (dies kann nur von Mitgliedern der Gruppe **Unternehmensstrategie - Besitzer** ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="129ee-301">Members cannot modify site-level permissions (this can only be done by members of the **Company strategy-Owners** group).</span></span>
    
- <span data-ttu-id="129ee-p105">Andere Benutzerkonten können nicht auf die Website oder ihre Ressourcen zugreifen oder Zugriff auf die Website anfordern. Zusätzliche Berechtigungen für die Website müssen vom globalen Administrator oder von einem Mitglied der Gruppe **Unternehmensstrategie - Besitzer** gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="129ee-p105">Other user accounts cannot access the site or its resources or request access to the site. Additional permissions to the site must be done by the global administrator or by a member of the **Company strategy-Owners** group.</span></span>
    
<span data-ttu-id="129ee-304">Konfigurieren Sie anschließend den Ordner „Dokumente“ der Unternehmensstrategie-Teamwebsite für die Bezeichnung „Streng vertraulich“.</span><span class="sxs-lookup"><span data-stu-id="129ee-304">Next, configure the documents folder of the Company strategy team site for the Highly Confidential label.</span></span>
  
1. <span data-ttu-id="129ee-305">Klicken Sie auf der Registerkarte **Unternehmensstrategie - Startseite** in Ihrem Browser auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="129ee-305">In the **Company strategy-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="129ee-306">Klicken Sie auf das Symbol für Einstellungen und anschließend auf **Bibliothekeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-306">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="129ee-307">Klicken Sie unter **Berechtigungen und Verwaltung** auf **Bezeichnung auf Elemente in dieser Bibliothek anwenden**.</span><span class="sxs-lookup"><span data-stu-id="129ee-307">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="129ee-308">Wählen Sie unter **Einstellungen -Bezeichnung anwenden** die Option **Streng vertraulich**, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-308">In **Settings-Apply Label**, select **Highly Confidential**, and then click **Save**.</span></span>
    
<span data-ttu-id="129ee-309">Konfigurieren Sie als Nächstes eine DLP-Richtlinie, die Benutzer blockiert, wenn sie ein Dokument auf einer SharePoint Online-Teamwebsite mit der Bezeichnung „Streng vertraulich" freigeben, die die Unternehmensstrategiewebsite enthält (außerhalb der Organisation).</span><span class="sxs-lookup"><span data-stu-id="129ee-309">Next, configure a DLP policy that blocks users when they share a document on a SharePoint Online team site with the Highly Confidential label, which includes the Company strategy site, outside the organization.</span></span>
  
1. <span data-ttu-id="129ee-310">Melden Sie sich beim [Microsoft 365 Compliance-Portal](https://compliance.microsoft.com/) mit Ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="129ee-310">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with your global admin.</span></span>
    
2. <span data-ttu-id="129ee-311">Klicken Sie auf der Registerkarte **Microsoft 365 Compliance** in Ihrem Browser auf **Richtlinien > Verhinderung von Datenverlust**.</span><span class="sxs-lookup"><span data-stu-id="129ee-311">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="129ee-312">Klicken Sie im Bereich **Verhinderung von Datenverlust** auf **Richtlinie erstellen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-312">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="129ee-313">Klicken Sie im Bereich **Mit einer Vorlage beginnen oder eine benutzerdefinierte Richtlinie erstellen** auf **Benutzerdefiniert**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-313">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="129ee-314">Geben Sie im Bereich **Ihre Richtlinie benennen** den Namen **Bezeichnung „Streng vertraulich" - SharePoint Online-Teamwebsites** bei **Name** ein, und klicken Sie dann auf **Weiter**</span><span class="sxs-lookup"><span data-stu-id="129ee-314">In the **Name your policy** pane, type **Highly Confidential label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="129ee-315">Klicken Sie im Bereich **Speicherorte auswählen** auf **Bestimmte Speicherorte auswählen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-315">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="129ee-316">Deaktivieren Sie in der Liste der Speicherorte **Exchange-E-Mail**, **OneDrive-Konten** und **Teams-Chat- und Kanalnachrichten**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-316">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="129ee-317">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="129ee-317">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="129ee-318">In der **wählen Sie die Typen der Inhalte zum Schutz** Bereich, klicken Sie auf **hinzufügen** im Dropdown-Listenfeld, und klicken Sie dann auf **Aufbewahrungsbezeichnungen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-318">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="129ee-319">Klicken Sie im Bereich **Aufbewahrungsbezeichnungen** auf **Hinzufügen**, wählen Sie die Bezeichnung **Streng vertraulich** aus, klicken Sie auf **Hinzufügen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="129ee-319">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="129ee-320">Klicken Sie im Bereich **Typen des zu schützenden Inhalts auswählen** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="129ee-320">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="129ee-321">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-321">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="129ee-322">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-322">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="129ee-323">Klicken Sie im Bereich **Richtlinentipps und E-Mail-Benachrichtigungen anpassen** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-323">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="129ee-324">Geben oder fügen Sie in das Textfeld einen der folgenden Tipps ein, abhängig davon, ob Sie Azure Information Protection zum Schutz streng vertraulicher Dateien implementiert haben:</span><span class="sxs-lookup"><span data-stu-id="129ee-324">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="129ee-p106">Wenn Sie eine Datei für einen Benutzer außerhalb der Organisation freigeben möchten, laden Sie die Datei herunter, und öffnen Sie sie. Klicken Sie auf „Datei“ > „Dokument schützen“ > „Mit Kennwort verschlüsseln“, und geben Sie dann ein sicheres Kennwort ein. Senden Sie das Kennwort in einer separaten E-Mail oder auf andere Weise.</span><span class="sxs-lookup"><span data-stu-id="129ee-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="129ee-328">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-328">Click **OK**.</span></span>
    
17. <span data-ttu-id="129ee-329">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-329">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="129ee-330">Klicken Sie im Bereich **Möchten Sie die Richtlinie aktivieren oder zunächst testen?** auf **Ja, Richtlinie aktivieren**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="129ee-330">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="129ee-331">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Erstellen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-331">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
   
    
<span data-ttu-id="129ee-332">Befolgen Sie als Nächstes die Anweisungen unter [Aktivieren von Azure RMS mit dem Microsoft 365 Admin Center](https://docs.microsoft.com/information-protection/deploy-use/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="129ee-332">Next, follow the instructions in [Activate Azure RMS with the Microsoft 365 admin center](https://docs.microsoft.com/information-protection/deploy-use/activate-office365).</span></span>
  
<span data-ttu-id="129ee-333">Konfigurieren Sie als Nächstes Azure Information Protection mit einer neuen Richtlinie und einer untergeordneten Bezeichnung für die C-Suite-Gruppe für Schutz und Berechtigungen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="129ee-333">Next, configure Azure Information Protection with a new policy and sub-label scoped for the C-Suite group for protection and permissions with the following steps:</span></span>
  
1. <span data-ttu-id="129ee-334">Melden Sie sich bei Bedarf beim [Microsoft 365 Admin Center](https://admin.microsoft.com) mit Ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="129ee-334">Sign in to the Microsoft 365 admin center (  ) with your global administrator account.</span></span>
    
2. <span data-ttu-id="129ee-335">Wechseln Sie auf einer separaten Registerkarte im Browser zum Azure-Portal unter [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="129ee-335">In a separate tab of your browser, go to the Azure portal ([https://portal.azure.com](https://portal.azure.com)).</span></span>
    
3. <span data-ttu-id="129ee-336">Wenn Sie Azure Information Protection zum ersten Mal konfigurieren, befolgen Sie diese [Anweisungen](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span><span class="sxs-lookup"><span data-stu-id="129ee-336">If this is the first time you are configuring Azure Information Protection, see these [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span></span>
    
4. <span data-ttu-id="129ee-337">Klicken Sie im Listenbereich auf **Alle Dienste**, geben Sie **Information** ein, und klicken Sie dann auf **Azure Information Protection**.</span><span class="sxs-lookup"><span data-stu-id="129ee-337">In the list pane, click **All services**, type **information**, and then click **Azure Information Protection**.</span></span>

5. <span data-ttu-id="129ee-338">Klicken Sie auf **Etiketten**.</span><span class="sxs-lookup"><span data-stu-id="129ee-338">Click **Labels**.</span></span>
    
6. <span data-ttu-id="129ee-339">Klicken Sie mit der rechten Maustaste auf die Bezeichnung **Streng vertraulich**, und klicken Sie dann auf **Unterbezeichnung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-339">Right-click the **Highly Confidential** label, and then click **Add a sub-label**.</span></span>
    
7. <span data-ttu-id="129ee-340">Geben Sie **C-Suite-Mitglieder** unter **Name** und **Beschreibung** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-340">Type **C-Suite members** in **Name** and **Description**.</span></span>
    
8. <span data-ttu-id="129ee-341">Klicken Sie unter **Berechtigungen für Dokumente und E-Mails mit dieser Bezeichnung festlegen** auf **Schützen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-341">In **Set permissions for documents and emails containing this label**, click **Protect**.</span></span>
    
9. <span data-ttu-id="129ee-342">Klicken Sie im Abschnitt **Schutz** auf **Azure (Cloudschlüssel)**.</span><span class="sxs-lookup"><span data-stu-id="129ee-342">In the **Protection** section, click **Azure (cloud key)**.</span></span>
    
10. <span data-ttu-id="129ee-343">Klicken Sie im Blatt **Schützen** unter **Schutzeinstellungen** auf **+ Berechtigungen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-343">On the **Protection** blade, under **Protection settings**, click **+ Add permissions**.</span></span>
    
11. <span data-ttu-id="129ee-344">Klicken Sie auf dem Blatt **Berechtigungen hinzufügen** unter **Benutzer und Gruppen angeben** auf **+ Verzeichnis durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-344">On the **Add permissions** blade, under **Specify users and groups**, click **+ Browse directory**.</span></span>
    
12. <span data-ttu-id="129ee-345">Wählen Sie im Bereich **AAD-Benutzer und -Gruppen** die Option **C-Suite**, und klicken Sie dann auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-345">On the **AAD Users and Groups** pane, select **C-Suite**, and then click **Select**.</span></span>
    
13. <span data-ttu-id="129ee-346">Klicken Sie unter **Aus voreingestellten Berechtigungen wählen oder Benutzerdefiniert festlegen** auf **Benutzerdefiniert**, und aktivieren Sie dann die Kontrollkästchen **Rechte anzeigen**, **Inhalt bearbeiten**, \*\* Speichern\*\*, **Antworten** und **Allen antworten**.</span><span class="sxs-lookup"><span data-stu-id="129ee-346">Under **Choose permissions from the preset or set custom**, click **Custom**, and then click the **View Rights**, **Edit Content**, **Save**, **Reply**, and **Reply all** check boxes.</span></span>
    
14. <span data-ttu-id="129ee-347">Klicken Sie zweimal auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-347">Click **OK** twice.</span></span>
    
15. <span data-ttu-id="129ee-348">Klicken Sie auf dem Blatt **Untergeordnete Bezeichnung** auf **Speichern** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-348">On the **Sub-label** blade, click **Save**, and then click **OK**.</span></span>

16. <span data-ttu-id="129ee-349">Klicken Sie auf dem Blatt **Azure Information Protection** auf **Richtlinien > + Neue Richtlinie hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="129ee-349">On the **Azure Information protection** blade, click **Policies > + Add a new policy**.</span></span>
    
17. <span data-ttu-id="129ee-350">Geben Sie unter **Richtlinienname\*\*\*\*CompanyStrategy** und unter **Beschreibung\*\*\*\*Dokumente in der Teamwebsite für Kampagnenstrategie** ein.</span><span class="sxs-lookup"><span data-stu-id="129ee-350">Type **CompanyStrategy** in **Policy name** and **Documents in the Company strategy team site** in **Description**.</span></span>
    
18. <span data-ttu-id="129ee-351">Klicken Sie auf **Wählen Sie aus, welche Benutzer oder Gruppen diese Richtlinie erhalten. > Benutzer/Gruppen**, und wählen Sie dann **C-Suite** aus.</span><span class="sxs-lookup"><span data-stu-id="129ee-351">Click **Select which users or groups get this policy > User/Groups**, and then select **C-Suite**.</span></span>
    
19. <span data-ttu-id="129ee-352">Klicken Sie auf **Auswählen > OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-352">Click **Select > OK**.</span></span>

20. <span data-ttu-id="129ee-p107">Klicken Sie auf **Bezeichnungen hinzufügen oder entfernen**. Klicken Sie im Bereich **Richtlinie: Richtlinie: Bezeichnungen hinzufügen oder entfernen** auf **C-Suite-** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-p107">Click **Add or remove labels**. In the **Policy: Add or remove labels** pane, click **C-Suite**, and then click **OK**.</span></span>   

21. <span data-ttu-id="129ee-355">Klicken Sie auf **Speichern** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="129ee-355">Click **Save**, and then click **OK**.</span></span>
    
<span data-ttu-id="129ee-356">Um ein Dokument mit Azure Information Protection und mit dieser neuen Bezeichnung zu schützen, müssen Sie [den Azure Information Protection-Client](https://docs.microsoft.com/information-protection/rms-client/install-client-app) auf einem Testcomputer installieren, Office vom Admin Center installieren und sich dann aus Microsoft Word mit einem Konto in der Gruppe **C-Suite** Ihres Testabonnements anmelden.</span><span class="sxs-lookup"><span data-stu-id="129ee-356">To protect a document with Azure Information Protection and this new label, you must [install the Azure Information Protection client](https://docs.microsoft.com/information-protection/rms-client/install-client-app) on a test machine, install Office from the admin center, and then sign in from Microsoft Word with an account in the **C-Suite** group of your trial subscription.</span></span>
  
<span data-ttu-id="129ee-357">Sie können jetzt mit dem Erstellen von Dokumenten in diesen vier Websites beginnen und den Zugriff mit verschiedenen Benutzerkonten in Ihrem Testabonnement testen.</span><span class="sxs-lookup"><span data-stu-id="129ee-357">You are now ready to create documents in these four sites and test access to them with various user accounts in your trial subscription.</span></span>
  
<span data-ttu-id="129ee-358">Nachfolgend sehen Sie die gesamte Konfiguration für alle vier SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="129ee-358">Here is the overall configuration for all four SharePoint Online team sites.</span></span>
  
![Alle vier Teamwebsites in der sicheren Entwicklungs-/Testumgebung von SharePoint Online.](media/b0fea489-359c-4c85-a0ad-e4efb4a1e47f.png)
  
## <a name="next-step"></a><span data-ttu-id="129ee-360">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="129ee-360">Next step</span></span>

<span data-ttu-id="129ee-361">Wenn Sie für die Produktionsbereitstellung sicherer SharePoint Online-Websites bereit sind, erhalten Sie unter [Sichern von SharePoint Online-Websites und -Dateien](secure-sharepoint-online-sites-and-files.md) detaillierte Informationen und Links zu Schritt-für-Schritt-Bereitstellungsartikeln.</span><span class="sxs-lookup"><span data-stu-id="129ee-361">When you are ready for production deployment of secure SharePoint Online sites, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md) for detailed information and links to step-by-step deployment articles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="129ee-362">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="129ee-362">See Also</span></span>

[<span data-ttu-id="129ee-363">Sichern von SharePoint Online-Websites und -Dateien</span><span class="sxs-lookup"><span data-stu-id="129ee-363">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="129ee-364">Cloudakzeptanz und Hybridlösungen</span><span class="sxs-lookup"><span data-stu-id="129ee-364">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="129ee-365">Microsoft-Sicherheitsleitfaden für politische Kampagnen, gemeinnützigen Organisationen und andere agile Organisationen</span><span class="sxs-lookup"><span data-stu-id="129ee-365">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)





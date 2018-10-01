---
title: Konfigurieren von Gruppen und Benutzern für eine politische Kampagne in einer Entwicklungs-/Testumgebung
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.custom: ''
ms.assetid: 0e22bcf3-bad3-42a4-b44f-276e0cf4790f
description: 'Zusammenfassung: Informationen zum Erstellen von Office 365- und Enterprise Mobility + Security-Testabonnements (EMS) mit Benutzern und Gruppen für eine Entwicklungs-/Testumgebung für eine politische Kampagne.'
ms.openlocfilehash: 6035fa5c525e840d12f734dbab4fb6d3b84e6afe
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345987"
---
# <a name="configure-groups-and-users-for-a-political-campaign-devtest-environment"></a><span data-ttu-id="298db-103">Konfigurieren von Gruppen und Benutzern für eine politische Kampagne in einer Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="298db-103">Configure groups and users for a political campaign dev/test environment</span></span>

 <span data-ttu-id="298db-104">**Zusammenfassung:** Informationen zum Erstellen von Office 365- und Enterprise Mobility + Security-Testabonnements (EMS) mit Benutzern und Gruppen für eine Entwicklungs-/Testumgebung für eine politische Kampagne.</span><span class="sxs-lookup"><span data-stu-id="298db-104">**Summary:** Create Office 365 and Enterprise Mobility + Security (EMS) trial subscriptions with users and groups for a political campaign dev/test environment.</span></span>
  
<span data-ttu-id="298db-105">Folgen Sie den Anweisungen in diesem Artikel beim Erstellen einer Entwicklungs-/Testumgebung, die vereinfachte Benutzerkonten und Gruppen für die Lösung [Microsoft-Sicherheitsleitfaden für politische Kampagnen, gemeinnützige Organisationen und andere agile Organisationen](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="298db-105">Use the instructions in this article to create a dev/test environment that includes simplified user accounts and groups for the [Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) solution.</span></span>
  
## <a name="phase-1-create-your-office-365-devtest-environment"></a><span data-ttu-id="298db-106">Phase 1: Erstellen Ihrer Office 365-Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="298db-106">Phase 1: Create your Office 365 dev/test environment</span></span>

<span data-ttu-id="298db-107">In dieser Phase erhalten Sie Testabonnements für Office 365 E5 und Enterprise Mobility + Security (EMS) E5 für eine fiktive Organisation, die eine politische Kampagne darstellt.</span><span class="sxs-lookup"><span data-stu-id="298db-107">In this phase, you obtain trial subscriptions for Office 365 E5 and Enterprise Mobility + Security (EMS) E5 for a fictional organization that represents a political campaign.</span></span>
  
<span data-ttu-id="298db-108">Folgen Sie zunächst den Anweisungen in **Phase 2** des Artikels [Office 365-Entwicklungs-/Testumgebung](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="298db-108">First, follow the instructions in **Phase 2** of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="298db-109">Als Nächstes registrieren Sie sich für das EMS E5-Testabonnement und fügen es derselben Organisation wie Ihr Office 365-Testabonnement hinzu.</span><span class="sxs-lookup"><span data-stu-id="298db-109">Next, sign up for the EMS E5 trial subscription and add it to the same organization as your Office 365 trial subscription.</span></span>
  
1. <span data-ttu-id="298db-p101">Falls erforderlich, melden Sie sich mit den Anmeldeinformationen des globalen Administratorkontos für Ihr Testabonnement beim Office 365-Portal an. Hilfe finden Sie unter [Wo kann ich mich bei Office 365 Business anmelden?](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="298db-p101">If needed, sign in to the Office 365 portal with the credentials of the global administrator account of your trial subscription. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="298db-112">Klicken Sie auf die Kachel **Admin**.</span><span class="sxs-lookup"><span data-stu-id="298db-112">Click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="298db-113">Klicken Sie auf der Registerkarte **Office Admin Center** in Ihrem Browser im linken Navigationsbereich auf **Abrechnung > Dienste kaufen**.</span><span class="sxs-lookup"><span data-stu-id="298db-113">On the **Office Admin center** tab in your browser, in the left navigation, click **Billing > Purchase services**.</span></span>
    
4. <span data-ttu-id="298db-p102">Suchen Sie auf der Seite **Dienste kaufen** den Artikel **Enterprise Mobility + Security E5**. Platzieren Sie den Mauszeiger auf dem Artikelnamen, und klicken Sie auf **Start free trial**.</span><span class="sxs-lookup"><span data-stu-id="298db-p102">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>
    
5. <span data-ttu-id="298db-116">Klicken Sie auf der Seite für die **Bestätigung Ihrer Bestellung** auf **Jetzt versuchen**.</span><span class="sxs-lookup"><span data-stu-id="298db-116">On the **Confirm your order** page, click **Try now**.</span></span>
    
6. <span data-ttu-id="298db-117">Klicken Sie auf der Seite **Bestellbestätigung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="298db-117">On the **Order receipt** page, click **Continue**.</span></span>
    
<span data-ttu-id="298db-118">Aktivieren Sie als Nächstes die EMS E5-Lizenz für Ihr globales Administratorkonto.</span><span class="sxs-lookup"><span data-stu-id="298db-118">Next, enable the EMS E5 license for your global administrator account.</span></span>
  
1. <span data-ttu-id="298db-119">Klicken Sie auf der Registerkarte **Office 365 Admin Center** in Ihrem Browser im linken Navigationsbereich auf **Benutzer > Aktive Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="298db-119">On the **Office 365 Admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>
    
2. <span data-ttu-id="298db-120">Klicken Sie auf Ihr globales Administratorkonto und dann auf **Bearbeiten**, um die **Produktlizenzen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="298db-120">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>
    
3. <span data-ttu-id="298db-121">Setzen Sie im Bereich **Product licenses** die Produktlizenz für **Enterprise Mobility + Security E5** auf **On**. Klicken Sie auf **Speichern** und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="298db-121">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups"></a><span data-ttu-id="298db-122">Phase 2: Erstellen und Konfigurieren der Azure Active Directory(AD)-Gruppen</span><span class="sxs-lookup"><span data-stu-id="298db-122">Phase 2: Create and configure your Azure Active Directory (AD) groups</span></span>

<span data-ttu-id="298db-123">In dieser Phase werden die Azure AD-Gruppen für Ihre Kampagne erstellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="298db-123">In this phase, you create and configure the Azure AD groups for your campaign.</span></span>
  
<span data-ttu-id="298db-124">Erstellen Sie zuerst eine Reihe von Gruppen für eine typische politische Kampagne mit dem Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="298db-124">First, create a set of groups for a typical political campaign with the Azure portal.</span></span>
  
1. <span data-ttu-id="298db-p103">Wechseln Sie auf einer neuen Registerkarte im Browser zum Azure-Portal unter [https://portal.azure.com](https://portal.azure.com). Falls erforderlich, melden Sie sich mit den Anmeldeinformationen des globalen Administratorkontos für Ihr Office 365 E5-Testabonnement an.</span><span class="sxs-lookup"><span data-stu-id="298db-p103">On a separate tab in your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com). If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>
    
2. <span data-ttu-id="298db-127">Klicken Sie im Azure-Portal auf **Azure Active Directory > Benutzer und Gruppen > Alle Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="298db-127">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>
    
3. <span data-ttu-id="298db-128">Führen Sie die folgenden Schritte für jeden Gruppenname in dieser Liste durch:</span><span class="sxs-lookup"><span data-stu-id="298db-128">Do the following steps for each group name in this list:</span></span>
    
  - <span data-ttu-id="298db-129">Senior-Mitarbeiter und strategische Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-129">Senior and strategic staff</span></span>
    
  - <span data-ttu-id="298db-130">IT-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-130">IT staff</span></span>
    
  - <span data-ttu-id="298db-131">Analytiker</span><span class="sxs-lookup"><span data-stu-id="298db-131">Analytics staff</span></span>
    
  - <span data-ttu-id="298db-132">Stammpersonal</span><span class="sxs-lookup"><span data-stu-id="298db-132">Regular core staff</span></span>
    
  - <span data-ttu-id="298db-133">Betriebspersonal</span><span class="sxs-lookup"><span data-stu-id="298db-133">Operations staff</span></span>
    
  - <span data-ttu-id="298db-134">Außendienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-134">Field staff</span></span>
    
1. <span data-ttu-id="298db-135">Klicken Sie auf dem Blatt **Alle Gruppen** auf **+ Neue Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="298db-135">On the **All groups** blade, click **+ New group**.</span></span>
    
2. <span data-ttu-id="298db-136">Geben Sie den Gruppennamen aus der Liste unter **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="298db-136">Type the group name from the list in **Name**.</span></span>
    
3. <span data-ttu-id="298db-137">Wählen Sie unter **Mitgliedschaft** **Dynamischer Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="298db-137">Select **Dynamic user** in **Membership**.</span></span>
    
4. <span data-ttu-id="298db-138">Klicken Sie auf **Ja** für **Office-Features aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="298db-138">Click **Yes** for **Enable Office features**.</span></span>
    
5. <span data-ttu-id="298db-139">Klicken Sie auf **Dynamische Abfrage hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="298db-139">Click **Add dynamic query**.</span></span>
    
6. <span data-ttu-id="298db-140">Wählen Sie unter **Benutzer hinzufügen**die Option **Abteilung** aus.</span><span class="sxs-lookup"><span data-stu-id="298db-140">In **Add users where**, select **department**.</span></span>
    
7. <span data-ttu-id="298db-141">Wählen Sie im nächsten Feld **Gleich** aus.</span><span class="sxs-lookup"><span data-stu-id="298db-141">In the next field, select **Equals**.</span></span>
    
8. <span data-ttu-id="298db-142">Geben Sie im nächsten Feld den Gruppennamen aus der Liste ein.</span><span class="sxs-lookup"><span data-stu-id="298db-142">In the next field, type the group name from the list.</span></span>
    
9. <span data-ttu-id="298db-143">Klicken Sie auf **Abfrage hinzufügen**, und klicken Sie dann auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="298db-143">Click **Add query**, and then click **Create**.</span></span>
    
10. <span data-ttu-id="298db-144">Klicken Sie auf **Benutzer und Gruppen – Alle Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="298db-144">Click **Users and groups - All groups**.</span></span>
    
<span data-ttu-id="298db-145">Konfigurieren Sie als Nächstes die Gruppen so, dass Mitgliedern automatisch Office 365 E5- und EMS E5-Lizenzen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="298db-145">Next, you configure the groups so that members are automatically assigned Office 365 E5 and EMS E5 licenses.</span></span>
  
1. <span data-ttu-id="298db-146">Klicken Sie im Azure-Portal auf **Azure Active Directory > Lizenzen > Alle Produkte**.</span><span class="sxs-lookup"><span data-stu-id="298db-146">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="298db-147">Wählen Sie in der Liste **Enterprise Mobility + Security E5** und **Office 365 Enterprise E5** aus, und klicken Sie dann auf **+ Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="298db-147">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **+ Assign**.</span></span>
    
3. <span data-ttu-id="298db-148">Klicken Sie auf dem Blatt **Lizenz zuweisen** auf **Benutzer und Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="298db-148">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="298db-149">Wählen Sie in der Liste der Gruppen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="298db-149">In the list of groups, select the following:</span></span>
    
  - <span data-ttu-id="298db-150">Analytiker</span><span class="sxs-lookup"><span data-stu-id="298db-150">Analytics staff</span></span>
    
  - <span data-ttu-id="298db-151">Außendienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-151">Field staff</span></span>
    
  - <span data-ttu-id="298db-152">IT-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-152">IT staff</span></span>
    
  - <span data-ttu-id="298db-153">Betriebspersonal</span><span class="sxs-lookup"><span data-stu-id="298db-153">Operations staff</span></span>
    
  - <span data-ttu-id="298db-154">Stammpersonal</span><span class="sxs-lookup"><span data-stu-id="298db-154">Regular core staff</span></span>
    
  - <span data-ttu-id="298db-155">Senior-Mitarbeiter und strategische Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="298db-155">Senior and strategic staff</span></span>
    
5. <span data-ttu-id="298db-156">Klicken Sie auf **Auswählen** und dann auf **Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="298db-156">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="298db-157">Schließen Sie die Registerkarte für das Azure Portal in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="298db-157">Close the Azure portal tab in your browser.</span></span>
    
## <a name="phase-3-add-your-user-accounts"></a><span data-ttu-id="298db-158">Phase 3: Hinzufügen von Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="298db-158">Phase 3: Add your user accounts</span></span>

<span data-ttu-id="298db-159">In dieser Phase werden beispielhafte Benutzerkonten für Ihre politische Kampagne hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="298db-159">In this phase, you add the example user accounts for your political campaign.</span></span>
  
<span data-ttu-id="298db-160">Zunächst müssen Sie [eine Verbindung mit dem Azure Active Directory V2 PowerShell-Modul herstellen](https://go.microsoft.com/fwlink/?linkid=842218).</span><span class="sxs-lookup"><span data-stu-id="298db-160">First, you [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218).</span></span>
  
<span data-ttu-id="298db-161">Geben Sie anschließend den Namen Ihrer Organisation, Ihren Standort und ein gemeinsames Kennwort ein, und führen Sie dann die folgenden Befehle an der PowerShell-Eingabeaufforderung oder in der ISE-Umgebung ein (Integrated Script Environment) aus:</span><span class="sxs-lookup"><span data-stu-id="298db-161">Next, you fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE):</span></span>
  
```
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$deptName="Senior and strategic staff"
$userNames=@("Candidate","ChiefOfStaff","Strategic1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Analytics staff"
$userNames=@("DataScientist1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Regular core staff"
$userNames=@("Regular1","Regular2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Operations staff"
$userNames=@("Operations1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Field staff"
$userNames=@("FieldConsultant1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }

```

> [!IMPORTANT]
> <span data-ttu-id="298db-p104">Die Verwendung eines gemeinsamen Kennworts an dieser Stelle dient der Automatisierung und einfacher Konfiguration für eine Entwicklungs-/Testumgebung. Für die Verwendung in Produktionsabonnements wird dies nicht empfohlen. Beim Anmelden mit einem dieser neuen Benutzerkonten werden Sie dazu aufgefordert, das Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="298db-p104">The use of a common password here is for automation and ease of configuration for a dev/test environment. This is not recommended for production subscriptions. As you sign in with each of these new user accounts, you will be prompted to change the password.</span></span> 
  
<span data-ttu-id="298db-165">Gehen Sie folgendermaßen vor, um sicherzustellen, dass die dynamische Gruppenmitgliedschaft und gruppenbasierte Lizenzierung ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="298db-165">Use these steps to verify that dynamic group membership and group-based licensing are working correctly.</span></span>
  
1. <span data-ttu-id="298db-166">Klicken Sie auf der Registerkarte **Microsoft Office Home** in Ihrem Browser auf die Kachel **Admin**.</span><span class="sxs-lookup"><span data-stu-id="298db-166">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="298db-167">Klicken Sie auf der neuen Registerkarte **Office Admin Center** des Browsers auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="298db-167">From the new **Office Admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="298db-168">Klicken Sie in der Benutzerliste auf **Kandidat**.</span><span class="sxs-lookup"><span data-stu-id="298db-168">In the list of users, click **Candidate**.</span></span>
    
4. <span data-ttu-id="298db-169">Stellen Sie im Bereich mit den Eigenschaften für das Benutzerkonto **Kandidat** Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="298db-169">In the pane that lists the properties of the **Candidate** user account, verify that:</span></span>
    
  - <span data-ttu-id="298db-170">Ist Mitglied der Gruppe **Senior-Mitarbeiter und strategische Mitarbeiter** (unter **Gruppenmitgliedschaften**).</span><span class="sxs-lookup"><span data-stu-id="298db-170">It is a member of the **Senior and strategic staff** group (in **Group memberships**).</span></span>
    
  - <span data-ttu-id="298db-171">Dem Benutzerkonto wurden **Enterprise Mobilität + Security E5**- und **Office 365 Enterprise E5**-Lizenzen (unter **Produktlizenzen**) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="298db-171">It has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>
    
5. <span data-ttu-id="298db-172">Schließen Sie den Bereich für das Benutzerkonto **Kandidat**.</span><span class="sxs-lookup"><span data-stu-id="298db-172">Close the **Candidate** user account pane.</span></span>
    
## <a name="record-values-for-future-reference"></a><span data-ttu-id="298db-173">Notieren von Werten für zukünftige Verwendung</span><span class="sxs-lookup"><span data-stu-id="298db-173">Record values for future reference</span></span>

<span data-ttu-id="298db-174">Notieren Sie diese Werte für die Arbeit mit Office 365- und EMS-Testabonnements für diese Entwicklung-/Testumgebung:</span><span class="sxs-lookup"><span data-stu-id="298db-174">Record these values for working with the Office 365 and EMS trial subscriptions for this dev/test environment:</span></span>
  
- <span data-ttu-id="298db-175">Organisationsname für das Testabonnement: ![](./media/Common-Images/TableLine.png)</span><span class="sxs-lookup"><span data-stu-id="298db-175">Your trial subscription organization name: ![](./media/Common-Images/TableLine.png)</span></span> 
    
    <span data-ttu-id="298db-176">Für den Domänennamen contoso.onmicrosoft.com des Testabonnements lautet der Name der Organisation zum Beispiel „contoso“.</span><span class="sxs-lookup"><span data-stu-id="298db-176">For example, for the trial subscription domain name of contoso.onmicrosoft.com, the organization name is "contoso".</span></span>
    
- <span data-ttu-id="298db-177">Der Name des globalen Office 365-Administrators: ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="298db-177">The Office 365 global administrator name: ![](./media/Common-Images/TableLine.png).onmicrosoft.com</span></span>
    
    <span data-ttu-id="298db-178">Notieren Sie sich das Kennwort für dieses Konto und das gemeinsame ursprüngliche Kennwort für die anderen Benutzerkonten, und bewahren Sie diese an einem sicheren Ort auf.</span><span class="sxs-lookup"><span data-stu-id="298db-178">Record the password for this account and the common initial password for the other user accounts in a secure location.</span></span>
    
## <a name="next-step"></a><span data-ttu-id="298db-179">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="298db-179">Next step</span></span>

<span data-ttu-id="298db-180">Erstellen Sie die vier verschiedenen Arten von SharePoint Online-Teamwebsites in dieser Entwicklungs-/Testumgebung mit [Create team sites in a political campaign dev/test environment](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="298db-180">Build the four different types of SharePoint Online team sites in this dev/test environment with [Create team sites in a political campaign dev/test environment](create-team-sites-in-a-political-campaign-dev-test-environment.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="298db-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="298db-181">See also</span></span>

[<span data-ttu-id="298db-182">Microsoft-Sicherheitsleitfaden für politische Kampagnen, gemeinnützigen Organisationen und andere agile Organisationen</span><span class="sxs-lookup"><span data-stu-id="298db-182">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="298db-183">Erstellen von Teamwebsites in einer Entwicklungs-/Testumgebung für eine politische Kampagne</span><span class="sxs-lookup"><span data-stu-id="298db-183">Create team sites in a political campaign dev/test environment</span></span>](create-team-sites-in-a-political-campaign-dev-test-environment.md)
  
[<span data-ttu-id="298db-184">Testumgebungsanleitungen (TLGs) zur Cloudakzeptanz</span><span class="sxs-lookup"><span data-stu-id="298db-184">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="298db-185">Cloudakzeptanz und Hybridlösungen</span><span class="sxs-lookup"><span data-stu-id="298db-185">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)





---
title: Suche, Schutz und Berichterstellung für die DSGVO in der Office 365-Entwicklungs-/Testumgebung
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
description: Veranschaulichung von DSGVO-Funktionen in Office 365
ms.openlocfilehash: d4d4113f6d78069a150e13c32ab192571671d986
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30955278"
---
# <a name="gdpr-discovery-protection-and-reporting-in-the-office-365-devtest-environment"></a><span data-ttu-id="b87b1-103">Suche, Schutz und Berichterstellung für die DSGVO in der Office 365-Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="b87b1-103">GDPR discovery, protection, and reporting in the Office 365 dev/test environment</span></span>

 <span data-ttu-id="b87b1-104">**Zusammenfassung:** Veranschaulichung von DSGVO-Funktionen in Office 365</span><span class="sxs-lookup"><span data-stu-id="b87b1-104">**Summary:** Demonstrate GDPR capabilities in Office 365.</span></span> 
  
<span data-ttu-id="b87b1-105">Dieser Artikel beschreibt die Konfiguration und Veranschaulichung von Suche, Schutz und Berichterstellung für personenbezogene Informationen (PII) für die Datenschutz-Grundverordnung (DSGVO) in einer Office 365-Entwicklungs-/Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="b87b1-105">This article describes how you configure and demonstrate personally identifiable information (PII) discovery, protection, and reporting for the General Data Protection Regulation (GDPR) in an Office 365 dev/test environment.</span></span>
  
## <a name="phase-1-create-and-configure-your-trial-office-365-subscription"></a><span data-ttu-id="b87b1-106">Phase 1: Erstellen und Konfigurieren Ihres Office 365-Testabonnements</span><span class="sxs-lookup"><span data-stu-id="b87b1-106">Phase 1: Create and configure your trial Office 365 subscription</span></span>

<span data-ttu-id="b87b1-107">Führen Sie zunächst die Schritte in [Phase 2 des Artikels „Office 365-Entwicklungs-/Testumgebung“](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) aus.</span><span class="sxs-lookup"><span data-stu-id="b87b1-107">First, follow the steps in [Phase 2 of the Office 365 dev/test environment](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) article.</span></span>

<span data-ttu-id="b87b1-108">Konfigurieren Sie dann mit den folgenden Schritte den eDiscovery-Manager:</span><span class="sxs-lookup"><span data-stu-id="b87b1-108">Next, use these steps to configure the eDiscovery manager:</span></span>

1. <span data-ttu-id="b87b1-109">Melden Sie sich mit Ihrem globalen Administratorkonto bei Ihrem Office 365-Testmandanten an.</span><span class="sxs-lookup"><span data-stu-id="b87b1-109">Sign in to your Office 365 trial tenant with your global administrator account.</span></span>
2. <span data-ttu-id="b87b1-110">Klicken Sie auf der Office 365-Startseite auf **Sicherheit und Compliance**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-110">From the Office 365 home page, click **Security & Compliance**.</span></span>
3. <span data-ttu-id="b87b1-111">Klicken Sie auf der neuen Registerkarte „Sicherheit und Compliance“ auf **Berechtigungen** > **eDiscovery-Manager**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-111">From the new Security & Compliance tab, click **Permissions** > **eDiscovery Manager**.</span></span>
4. <span data-ttu-id="b87b1-112">Klicken Sie für eDiscovery-Manager auf **Bearbeiten**, und klicken Sie dann auf **eDiscovery-Manager auswählen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-112">Click **Edit** for eDiscovery Manager, and then click **Choose eDiscovery Manager**.</span></span>
5. <span data-ttu-id="b87b1-113">Klicken Sie auf **+ Hinzufügen**, suchen Sie nach dem Namen Ihres globalen Administratorkontos, und fügen Sie dieses als eDiscovery-Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="b87b1-113">Click **+ Add**, search for your global administrator account name and add your global administrator account as an eDiscovery Manager.</span></span>
6. <span data-ttu-id="b87b1-114">Klicken Sie auf **Fertig** > **Speichern** > **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-114">Click **Done** > **Save** > **Close**.</span></span>
  
## <a name="phase-2-add-personally-identifiable-information-to-your-tenant"></a><span data-ttu-id="b87b1-115">Phase 2: Hinzufügen von personenbezogenen Informationen zu Ihrem Mandanten</span><span class="sxs-lookup"><span data-stu-id="b87b1-115">Phase 2: Add personally identifiable information to your tenant</span></span>

<span data-ttu-id="b87b1-116">In dieser Phase erstellen Sie ein Dokument mit PII für eine Reihe von Beispielen für internationale Kontonummern (International Banking Account Numbers, IBANs) und speichern es auf einer SharePoint Online-Website in Ihrer Office 365-Entwicklungs-/Testumgebung.</span><span class="sxs-lookup"><span data-stu-id="b87b1-116">In this phase, you create a document with PII for a set of example International Banking Account Numbers (IBANs) and store it on a SharePoint Online site in your Office 365 dev/test environment.</span></span>

1. <span data-ttu-id="b87b1-117">Öffnen Sie Microsoft Word auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="b87b1-117">On your local computer, open Microsoft Word.</span></span>
2. <span data-ttu-id="b87b1-118">Fügen Sie die folgende Tabelle in die Word-Datei ein, und speichern Sie sie als „IBANs.docx“ auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="b87b1-118">Paste the following table in the Word file and save it as ‘IBANs.docx’ on your local computer.</span></span>
    
    <span data-ttu-id="b87b1-119">Nummer</span><span class="sxs-lookup"><span data-stu-id="b87b1-119">Number</span></span>  |<span data-ttu-id="b87b1-120">Land</span><span class="sxs-lookup"><span data-stu-id="b87b1-120">Country</span></span>  |<span data-ttu-id="b87b1-121">Code</span><span class="sxs-lookup"><span data-stu-id="b87b1-121">Code</span></span> |<span data-ttu-id="b87b1-122">IBAN</span><span class="sxs-lookup"><span data-stu-id="b87b1-122">IBAN</span></span>  |
    |---------|---------|---------|---------|
    |<span data-ttu-id="b87b1-123">1</span><span class="sxs-lookup"><span data-stu-id="b87b1-123">-1</span></span>     |  <span data-ttu-id="b87b1-124">Österreich SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-124">Austria SEPA</span></span>      | <span data-ttu-id="b87b1-125">AT</span><span class="sxs-lookup"><span data-stu-id="b87b1-125">AT</span></span>            |<span data-ttu-id="b87b1-126">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="b87b1-126">AT611904300234573201</span></span>       |
    |<span data-ttu-id="b87b1-127">2</span><span class="sxs-lookup"><span data-stu-id="b87b1-127">2.</span></span>     |  <span data-ttu-id="b87b1-128">Bulgarien SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-128">Bulgaria SEPA</span></span>       |<span data-ttu-id="b87b1-129">BG</span><span class="sxs-lookup"><span data-stu-id="b87b1-129">BG</span></span>    |<span data-ttu-id="b87b1-130">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="b87b1-130">BG80BNBG96611020345678</span></span>      |
    |<span data-ttu-id="b87b1-131">3</span><span class="sxs-lookup"><span data-stu-id="b87b1-131">3.</span></span>     |  <span data-ttu-id="b87b1-132">Dänemark SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-132">Denmark SEPA</span></span>      |   <span data-ttu-id="b87b1-133">DK</span><span class="sxs-lookup"><span data-stu-id="b87b1-133">DK</span></span>      |<span data-ttu-id="b87b1-134">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="b87b1-134">DK5000400440116243</span></span>      |
    |<span data-ttu-id="b87b1-135">4</span><span class="sxs-lookup"><span data-stu-id="b87b1-135">4.</span></span>     |  <span data-ttu-id="b87b1-136">Finnland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-136">Finland SEPA</span></span>      |   <span data-ttu-id="b87b1-137">FI</span><span class="sxs-lookup"><span data-stu-id="b87b1-137">FI</span></span>      |<span data-ttu-id="b87b1-138">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="b87b1-138">FI2112345600000785</span></span>         |
    |<span data-ttu-id="b87b1-139">5</span><span class="sxs-lookup"><span data-stu-id="b87b1-139">5.</span></span>     |  <span data-ttu-id="b87b1-140">Frankreich SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-140">France SEPA</span></span>       |   <span data-ttu-id="b87b1-141">FR</span><span class="sxs-lookup"><span data-stu-id="b87b1-141">FR</span></span>      |<span data-ttu-id="b87b1-142">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="b87b1-142">FR1420041010050500013M02606</span></span>         |
    |<span data-ttu-id="b87b1-143">6</span><span class="sxs-lookup"><span data-stu-id="b87b1-143">6.</span></span>     |  <span data-ttu-id="b87b1-144">Deutschland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-144">Germany SEPA</span></span>      |   <span data-ttu-id="b87b1-145">DE</span><span class="sxs-lookup"><span data-stu-id="b87b1-145">DE</span></span>      |<span data-ttu-id="b87b1-146">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="b87b1-146">DE89370400440532013000</span></span>         |
    |<span data-ttu-id="b87b1-147">7</span><span class="sxs-lookup"><span data-stu-id="b87b1-147">7.</span></span>     |  <span data-ttu-id="b87b1-148">Griechenland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-148">Greece SEPA</span></span>       |   <span data-ttu-id="b87b1-149">GR</span><span class="sxs-lookup"><span data-stu-id="b87b1-149">GR</span></span>      |<span data-ttu-id="b87b1-150">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="b87b1-150">GR1601101250000000012300695</span></span>         |
    |<span data-ttu-id="b87b1-151">8</span><span class="sxs-lookup"><span data-stu-id="b87b1-151">8.</span></span>     |  <span data-ttu-id="b87b1-152">Italien SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-152">Italy SEPA</span></span>       |    <span data-ttu-id="b87b1-153">IT</span><span class="sxs-lookup"><span data-stu-id="b87b1-153">IT</span></span>     |<span data-ttu-id="b87b1-154">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="b87b1-154">GR1601101250000000012300695</span></span>         |
    |<span data-ttu-id="b87b1-155">9</span><span class="sxs-lookup"><span data-stu-id="b87b1-155">9.</span></span>     |  <span data-ttu-id="b87b1-156">Niederlande SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-156">Netherlands SEPA</span></span>      |   <span data-ttu-id="b87b1-157">NL</span><span class="sxs-lookup"><span data-stu-id="b87b1-157">NL</span></span>      |    <span data-ttu-id="b87b1-158">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="b87b1-158">NL91ABNA0417164300</span></span>     |
    |<span data-ttu-id="b87b1-159">10</span><span class="sxs-lookup"><span data-stu-id="b87b1-159">1.0</span></span>     | <span data-ttu-id="b87b1-160">Polen SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-160">Poland SEPA</span></span>       |  <span data-ttu-id="b87b1-161">PL</span><span class="sxs-lookup"><span data-stu-id="b87b1-161">PL</span></span>       | <span data-ttu-id="b87b1-162">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="b87b1-162">PL27114020040000300201355387</span></span>        |

<span data-ttu-id="b87b1-163">Hinweis: Dieser Beispieldatensatz wird von öffentlich verfügbaren Informationen abgeleitet und soll nur für Testzwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-163">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

3. <span data-ttu-id="b87b1-164">Geben Sie auf einer neuen Browserregisterkarte die folgende Adresse ein: **https://**\<NameIhresMandanten\>**.sharepoint.com**</span><span class="sxs-lookup"><span data-stu-id="b87b1-164">In a new tab of your browser, type:  **https://**\<YourTenantName\>**.sharepoint.com**</span></span>
4. <span data-ttu-id="b87b1-p101">Klicken Sie auf **Dokumente**, um die Dokumentbibliothek für diese Website zu öffnen. Wenn Sie zu einer Tour über neue Listen aufgefordert werden, klicken Sie auf **Weiter**, bis sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p101">Click **Documents** to open the document library for this site. If you’re prompted for a new list experience tour, click **Next** until it’s finished.</span></span>
5.  <span data-ttu-id="b87b1-167">Klicken Sie auf **Hochladen** > **Dateien**, und wählen Sie die Datei „IBANs.docx“ aus, die Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b87b1-167">Click **Upload** > **Files** and select the IBANs.docx you created in step 2.</span></span>

  
## <a name="phase-3-demonstrate-data-discovery"></a><span data-ttu-id="b87b1-168">Phase 3: Veranschaulichen der Datenermittlung</span><span class="sxs-lookup"><span data-stu-id="b87b1-168">Phase 3: Demonstrate data discovery</span></span>

<span data-ttu-id="b87b1-169">In dieser Phase veranschaulichen Sie die Suche nach dem in Schritt 2 erstellten und gespeicherten Dokument basierend auf dessen Inhalt (IBANs).</span><span class="sxs-lookup"><span data-stu-id="b87b1-169">In this phase, you demonstrate search to find the document created and stored in Phase 2, based on its content containing IBANs.</span></span>

1. <span data-ttu-id="b87b1-170">Klicken Sie auf der Registerkarte „Sicherheit und Compliance“ auf **Start**, und klicken Sie dann auf **Suche und Untersuchung** > **Inhaltssuche**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-170">From the Security & Compliance tab, click **Home**, and then click **Search & investigation** > **Content search**.</span></span>
2. <span data-ttu-id="b87b1-171">Erstellen Sie ein neues Suchelement, indem Sie auf **+** klicken.</span><span class="sxs-lookup"><span data-stu-id="b87b1-171">Create a new search item by clicking on **+**.</span></span>
3. <span data-ttu-id="b87b1-172">Geben Sie in einem neuen Fenster die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="b87b1-172">In a new window, provide the following information:</span></span>  
    <span data-ttu-id="b87b1-p102">a. Name: IBAN-Suche</span><span class="sxs-lookup"><span data-stu-id="b87b1-p102">a. Name: IBAN Search</span></span>  
    <span data-ttu-id="b87b1-p103">b. Wo sollen wir suchen?: **Wählen Sie die zu durchsuchenden Websites** (klicken Sie auf **+**), und geben Sie dann die URL der Website ein: **https://** \< NameIhresMandanten\>**.sharepoint.com/**</span><span class="sxs-lookup"><span data-stu-id="b87b1-p103">b. Where do you want us to look?: **Choose specific sites to search** (click **+**), and then enter the site's URL: **https://**\<YourTenantName\>**.sharepoint.com/**</span></span>  
    <span data-ttu-id="b87b1-p104">c. Klicken Sie auf **Hinzufügen** und dann auf **OK**. Wenn eine Warnung angezeigt wird, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p104">c. Click **Add**, and then click **OK**. If you see a Warning, click **OK**.</span></span>  
    <span data-ttu-id="b87b1-p105">d. Klicken Sie in einem **neuen Suchfenster** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p105">d. Click **Next** on a **New search** window.</span></span>  
    <span data-ttu-id="b87b1-p106">e. Geben Sie für **Wonach sollen wir suchen?**: **SensitiveType: „International Banking Account Number (IBAN)“** ein, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p106">e. For **What do you want us to look for?**: **SensitiveType:"International Banking Account Number (IBAN)"**, and then click **Search**.</span></span>

4. <span data-ttu-id="b87b1-184">Stellen Sie sicher, dass mindestens ein Element in den **IBAN-Suchergebnissen** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="b87b1-184">Make sure you see at least one item listed in the **IBAN Search** results.</span></span>


## <a name="phase-4-create-a-custom-sensitive-information-type-via-powershell"></a><span data-ttu-id="b87b1-185">Phase 4: Erstellen eines benutzerdefinierten vertraulichen Informationstyps über PowerShell</span><span class="sxs-lookup"><span data-stu-id="b87b1-185">Phase 4: Create a custom sensitive information type via PowerShell</span></span>

<span data-ttu-id="b87b1-p107">In dieser Phase erstellen Sie einen benutzerdefinierten vertraulichen Informationstyp für die fiktive Contoso Corporation mithilfe von Microsoft PowerShell. Contoso verwendet einer Contoso-Kundennummer (Contoso Customer Number, CCN) zur Identifizierung der einzelnen Kunden in seiner Kundendatenbank. Eine CCN weist die folgende Struktur auf:</span><span class="sxs-lookup"><span data-stu-id="b87b1-p107">In this phase, you create a custom sensitive information type for the fictional Contoso Corporation using Microsoft PowerShell.  Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following structure:</span></span>
- <span data-ttu-id="b87b1-189">Zwei Ziffern, die für das Jahr stehen, in dem der Datensatz erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="b87b1-189">Two digits to represent the year that the record was created.</span></span>
    - <span data-ttu-id="b87b1-190">Contoso wurde 2002 gegründet, daher wäre der früheste mögliche Wert „02“.</span><span class="sxs-lookup"><span data-stu-id="b87b1-190">Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span> 
- <span data-ttu-id="b87b1-191">Drei Ziffern, die für die Partneragentur stehen, die den Datensatz erstellt hat</span><span class="sxs-lookup"><span data-stu-id="b87b1-191">Three digits to represent the partner agency that created the record.</span></span>
    - <span data-ttu-id="b87b1-192">Mögliche Agenturwerte liegen zwischen 000 bis 999.</span><span class="sxs-lookup"><span data-stu-id="b87b1-192">Possible agency values range from 000 to 999.</span></span> 
- <span data-ttu-id="b87b1-193">Ein alphabetisches Zeichen, das für die Branche steht</span><span class="sxs-lookup"><span data-stu-id="b87b1-193">An alphabetic character to represent the line of business.</span></span>
    - <span data-ttu-id="b87b1-194">Mögliche Werte sind a-z, Groß- und Kleinschreibung soll nicht berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-194">Possible values are a-z and should be case insensitive.</span></span>
- <span data-ttu-id="b87b1-195">Eine vierstellige Seriennummer</span><span class="sxs-lookup"><span data-stu-id="b87b1-195">A four-digit serial number.</span></span> 
    - <span data-ttu-id="b87b1-196">Mögliche Werte für Seriennummern liegen zwischen 0000 und 9999.</span><span class="sxs-lookup"><span data-stu-id="b87b1-196">Possible serial number values range from 0000 to 9999.</span></span>   

<span data-ttu-id="b87b1-p108">Contoso verwendet immer eine CCN beim Verweisen auf Kunden in der internen Korrespondenz, externen Korrespondenz, in Dokumenten und andere Formularen. Contoso benötigt einen benutzerdefinierten vertraulichen Informationstyp, um die Verwendung von CCNs in Office 365-Inhalt zu ermitteln, um einen möglichen Schutz für die Verwendung dieser personenbezogenen Informationen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p108">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, and other forms. Contoso needs a custom sensitive item type to detect the use of CCNs in Office 365 content so that they may apply protection to the use of this form of personal identifiable information.</span></span>

1. <span data-ttu-id="b87b1-199">Folgen Sie den Anweisungen in [Verbinden mit PowerShell für Office 365 Security & Compliance Center über Multi-Factor Authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell?view=exchange-ps), und stellen Sie mit dem UPN Ihres globalen Administratorkontos eine Verbindung mit Security & Compliance Center her.</span><span class="sxs-lookup"><span data-stu-id="b87b1-199">Use the instructions in [Connect to Office 365 Security & Compliance Center PowerShell using multi-factor authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell?view=exchange-ps) and connect to the Security & Compliance Center with UPN of your global administrator account.</span></span>
2. <span data-ttu-id="b87b1-200">Führen Sie die folgenden PowerShell-Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="b87b1-200">Run the following PowerShell commands.</span></span>

     ```
    #Create & start search for sample data
    $searchName = "Sample Customer Information Search"
    $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
    New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
    Start-ComplianceSearch -Identity $searchName#Create & start search for sample data
    $searchName = "Sample Customer Information Search"
    $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
    New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
    Start-ComplianceSearch -Identity $searchName
    ```
3. <span data-ttu-id="b87b1-201">Führen Sie die folgenden PowerShell-Befehle aus, und kopieren Sie die generierten GUIDs in der Reihenfolge, in der sie aufgelistet sind, in eine offene Instanz von Editor auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="b87b1-201">Run the following PowerShell commands and copy the generated GUIDs to an open instance of Notepad on your computer in the order in which they are listed.</span></span>
    ```
    #Generate three unique GUIDs
    Write-Host "GUID1 = "([guid]::NewGuid().Guid)
    Write-Host "GUID2 = "([guid]::NewGuid().Guid)
    Write-Host "GUID3 = "([guid]::NewGuid().Guid)
    ```
4. <span data-ttu-id="b87b1-202">Öffnen Sie auf dem lokalen Computer eine weitere Instanz von Editor, und fügen Sie den folgenden Inhalt ein:</span><span class="sxs-lookup"><span data-stu-id="b87b1-202">On your local computer, open another instance of Notepad and paste in the following content:</span></span>

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce"> 
    <RulePack id="GUID1">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id="GUID2" />
    <Details defaultLangCode="en"> 
    <LocalizedDetails langcode="en"> 
    <PublisherName>Contoso Ltd.</PublisherName> 
    <Name>Contoso Rule Package</Name> 
    <Description>Defines Contoso's custom set of classification rules</Description>
    </LocalizedDetails>
    </Details>
    </RulePack>
    <Rules>
    <!-- Contoso Customer Number (CCN) -->
    <Entity id="GUID3" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
    <IdMatch idRef="Regex_contoso_ccn" />
    <Match idRef="Keyword_contoso_ccn" />
    <Match idRef="Regex_eu_date" />
    </Pattern>
    </Entity>
    <Regex id="Regex_contoso_ccn">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</Regex>
    <Keyword id="Keyword_contoso_ccn">
    <Group matchStyle="word">
    <Term caseSensitive="false">customer number</Term>
    <Term caseSensitive="false">customer no</Term>
    <Term caseSensitive="false">customer #</Term>
    <Term caseSensitive="false">customer#</Term>
    <Term caseSensitive="false">Contoso customer</Term>
    </Group>
    </Keyword>
    <Regex id="Regex_eu_date"> (0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)? |feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|apr(ile|il)?|abr(il)?|avril |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)? |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}</Regex>
    <LocalizedStrings>
    <Resource idRef="GUID3">
    <Name default="true" langcode="en-us">Contoso Customer Number (CCN)</Name>
    <Description default="true" langcode="en-us">Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</Description>
    </Resource>
    </LocalizedStrings>
    </Rules>
    </RulePackage>
    ```
5. <span data-ttu-id="b87b1-203">Ersetzen Sie die Werte von GUID1, GUID2 und GUID3 im XML-Text von Schritt 4 durch deren Werte aus Schritt 3, und speichern Sie dann die Inhalte mit dem Namen „ContosoCCN.xml“ auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="b87b1-203">Replace the values of GUID1, GUID2, and GUID3 in the XML text of step 4 with their values from step 3, and then save the contents on your local computer with the name ContosoCCN.xml.</span></span>
6. <span data-ttu-id="b87b1-204">Geben Sie den Pfad zur Datei „ContosoCCN.xml“ ein, und führen Sie die folgenden Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="b87b1-204">Fill in the path to your ContosoCCN.xml file and run the following commands.</span></span>
    ```
    #Create new Sensitive Information Type
    $path="<path to the ContosoCCN.xml file, such as C:\Scripts\ContosoCCN.xml>"
    New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path $path -Encoding Byte -ReadCount 0)
    ```
7. <span data-ttu-id="b87b1-p109">Klicken Sie auf der Registerkarte „Sicherheit und Compliance“ auf **Klassifizierungen** > **Typen vertraulicher Informationen**. Die Contoso-Kundennummer (CCN) sollte in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p109">From the Security & Compliance tab, click **Classifications** > **Sensitive information types**. You should see the Contoso Customer Number (CCN) in the list.</span></span>

## <a name="phase-5-demonstrate-data-protection"></a><span data-ttu-id="b87b1-207">Phase 5: Veranschaulichen des Datenschutzes</span><span class="sxs-lookup"><span data-stu-id="b87b1-207">Phase 5: Demonstrate data protection</span></span>

<span data-ttu-id="b87b1-208">Schutz von personenbezogenen Informationen in Office 365 umfasst Funktionen, um Datenverlust zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-208">Protection of personal information in Office 365 includes using data loss prevention (DLP) capabilities.</span></span>  <span data-ttu-id="b87b1-209">Mit DLP-Richtlinien können Sie automatisch in Office 365 vertrauliche Informationen schützen.</span><span class="sxs-lookup"><span data-stu-id="b87b1-209">With DLP policies, you can automatically protect sensitive information across Office 365.</span></span>

<span data-ttu-id="b87b1-p111">Es gibt mehrere Methoden zum Anwenden des Schutzes. Die Aufklärung und Bewusstseinsbildung in Bezug auf Daten von EU-Bürgern, die in Ihrer Umgebung gespeichert werden, sowie den Umgang von Mitarbeitern mit diesen stellen eine Ebene des Informationsschutzes unter Verwendung von DLP von Office 365 dar.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p111">There are multiple ways you can apply the protection. Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Office 365 DLP.</span></span>

<span data-ttu-id="b87b1-212">In dieser Phase erstellen Sie eine neue DLP-Richtlinie und veranschaulichen, wie sie auf die Datei „IBANs.docx“ angewendet wird, die Sie in Phase 2 in SharePoint Online gespeichert haben, und wie sie angewendet wird, wenn Sie versuchen, eine E-Mail mit IBANs zu versenden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-212">In this phase, you create a new DLP policy and demonstrate how it gets applied to the IBANs.docx file you stored in SharePoint Online in Phase 2 and when you attempt to send an email containing IBANs.</span></span>

1. <span data-ttu-id="b87b1-213">Klicken Sie auf der Registerkarte „Sicherheit und Compliance“ im Browser auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-213">From the Security & Compliance tab of your browser, click **Home**.</span></span>
2. <span data-ttu-id="b87b1-214">Klicken Sie auf **Verhinderung von Datenverlust** > **Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-214">Click **Data loss prevention** > **Policy**.</span></span>
3. <span data-ttu-id="b87b1-215">Klicken Sie auf **+ Erstellen einer Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-215">Click **+ Create a policy**.</span></span>
4. <span data-ttu-id="b87b1-216">Klicken Sie in **Mit einer Vorlage beginnen oder eine benutzerdefinierte Richtlinie erstellen** auf **Benutzerdefiniert** > **Benutzerdefinierte Richtlinie** > **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-216">In **Start with a template or create a custom policy**, click **Custom** > **Custom policy** > **Next**.</span></span>
5. <span data-ttu-id="b87b1-p112">Geben Sie in **Richtlinie benennen** die folgenden Details an, und klicken Sie dann auf **Weiter**: a. Name: **PII-Richtlinie für EU-Bürger** b. Beschreibung: **Schützen der personenbezogenen Informationen von EU-Bürgern**</span><span class="sxs-lookup"><span data-stu-id="b87b1-p112">In **Name your policy**, provide the following details and then click **Next**:  a. Name: **EU Citizen PII Policy** b. Description: **Protect the personally identifiable information of European citizens**</span></span>
6. <span data-ttu-id="b87b1-p113">Wählen Sie in **Speicherorte auswählen** die Option **Alle Speicherorte in Office 365** aus. Dies beinhaltet Inhalt in Exchange-E-Mail- sowie OneDrive- und SharePoint-Dokumenten. Klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p113">In **Choose locations**, select **All locations in Office 365**. This will include content in Exchange email and OneDrive and SharePoint documents. And then click **Next**.</span></span>
7. <span data-ttu-id="b87b1-223">Klicken Sie in **Anpassen des zu schützenden Inhaltstyps** auf **Nach Inhalten suchen, die Folgendes enthalten:**, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-223">In **Customize the type of content you want to protect**, click **Find content that contains:** and then click **Edit**.</span></span>
8. <span data-ttu-id="b87b1-224">Klicken Sie in **Auswählen des zu schützenden Inhaltstyps** auf **Hinzufügen** > **Typen vertraulicher Informationen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-224">In **Choose the types of content to protect**, click **Add** > **Sensitive info types**.</span></span>
9. <span data-ttu-id="b87b1-225">Klicken Sie in **Typen vertraulicher Informationen** auf **+ Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-225">In **Sensitive info types**, click **+ Add**.</span></span>
10. <span data-ttu-id="b87b1-226">Suchen Sie in **Typen vertraulicher Informationen** nach **IBAN**, aktivieren Sie das Kontrollkästchen für **International Banking Account Number (IBAN)**, und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-226">In **Sensitive info types**, search for **IBAN**, select the check box for **International Banking Account Number (IBAN)**, and then click **Add**.</span></span>
11. <span data-ttu-id="b87b1-227">Vergewissern Sie sich, dass **International Banking Account Number (IBAN)** als Typ vertraulicher hinzugefügt wurde, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-227">Confirm that the **International Banking Account Number (IBAN)** sensitive information type was added, and then click **Done**.</span></span>
12. <span data-ttu-id="b87b1-228">Vergewissern Sie sich in **Inhalt enthält**, dass die Typen vertraulicher Informationen hinzugefügt wurden, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-228">In **Content contains**, confirm that the sensitive information types were added and then click **Save**.</span></span>
13. <span data-ttu-id="b87b1-229">Stellen Sie in **Anpassen des zu schützenden Inhaltstyps** sicher, dass **Nach Inhalten suchen, die Folgendes enthalten:** die **internationale Bankkontonummer (IBAN)** enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-229">In **Customize the type of content you want to protect**, confirm  **Find content that contains:** contains the **International Banking Account Number (IBAN)**, and then click **Next**.</span></span>
14. <span data-ttu-id="b87b1-230">Ändern Sie in **Erkennen, wenn Inhalte, die freigegeben werden, Folgendes enthalten:** den Wert von **10** in **1**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-230">In **Detect when content that's being shared contains:**, change the value from **10** to **1**, and then click **Next**.</span></span>
15. <span data-ttu-id="b87b1-231">Wählen Sie in **Möchten Sie die Richtlinie aktivieren oder sie zuerst ausprobieren?** die folgenden Einstellungen aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-231">In **Do you want to turn on the policy or test things out first?**, choose the following settings, and then click **Next**.</span></span>  
    <span data-ttu-id="b87b1-p114">a. Wählen Sie die Option für **Ich möchte sie zuerst testen** aus.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p114">a. Select the option for **I'd like to test it out first**</span></span>  
    <span data-ttu-id="b87b1-p115">b. Aktivieren Sie das Kontrollkästchen für **Anzeigen von Richtlinientipps im Testmodus**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p115">b. Select the check box for **Show policy tips while in test mode**</span></span> 
16. <span data-ttu-id="b87b1-p116">Klicken Sie in **Überprüfen Sie Ihre Einstellungen** auf **Erstellen**, nachdem Sie die Einstellungen überprüft haben. HINWEIS: Nach dem Erstellen einer neuen DLP-Richtlinie dauert es eine Weile, bis diese wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p116">In **Review your settings**, click **Create** after reviewing the settings. NOTE: After you create a new DLP policy, it will take a while for it to take effect.</span></span>
17. <span data-ttu-id="b87b1-238">Öffnen Sie auf dem lokalen Computer eine private Instanz des Browsers.</span><span class="sxs-lookup"><span data-stu-id="b87b1-238">On your local computer, open a private instance of your browser.</span></span>
18. <span data-ttu-id="b87b1-239">Geben Sie in der Adressleiste **https://**\<NameIhresMandanten\>**. sharepoint.com** ein, und melden Sie sich mit Ihrem globalen Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="b87b1-239">In the address bar, type **https://**\<YourTenantName\>**.sharepoint.com** and sign in using your global administrator account.</span></span>
19. <span data-ttu-id="b87b1-240">Klicken Sie auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-240">Click **Documents**.</span></span>
20. <span data-ttu-id="b87b1-p117">Klicken Sie auf die Datei mit dem Namen „IBANs.docx“. „Richtlinientipp für IBANs.docx“ sollte angezeigt werden. Die Datei „IBANs.docx“ wurde an externe Empfänger versendet, was gegen die DLP-Richtlinie verstößt.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p117">Click the file named ‘IBANs.docx’. You should see ‘Policy tip for IBANs.docx’.  The IBANs.docx file was shared with external recipients, which violates the DLP policy.</span></span> 
21. <span data-ttu-id="b87b1-244">Geben Sie in der Adressleiste Folgendes ein: `https://outlook.office365.com`</span><span class="sxs-lookup"><span data-stu-id="b87b1-244">In the address bar, type: `https://outlook.office365.com`</span></span>
22. <span data-ttu-id="b87b1-245">Klicken Sie auf **Neu** - **E-Mail-Nachricht**, und geben Sie Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="b87b1-245">Click **New** - **Email message** and provide the following:</span></span>  
    - <span data-ttu-id="b87b1-246">**An:** \< eine persönliche E-Mail-Adresse\></span><span class="sxs-lookup"><span data-stu-id="b87b1-246">**To:** \<a personal email address\></span></span>  
    - <span data-ttu-id="b87b1-247">**Betreff:** DSGVO-Test</span><span class="sxs-lookup"><span data-stu-id="b87b1-247">**Subject:** GDPR Test</span></span>  
    - <span data-ttu-id="b87b1-248">**Text:** Kopieren Sie die unten gezeigte Tabelle mit Werten, und fügen Sie sie ein.</span><span class="sxs-lookup"><span data-stu-id="b87b1-248">**Body:** Copy in the table of values shown below.</span></span>
  
        |<span data-ttu-id="b87b1-249">Nummer</span><span class="sxs-lookup"><span data-stu-id="b87b1-249">Number</span></span>  |<span data-ttu-id="b87b1-250">Land</span><span class="sxs-lookup"><span data-stu-id="b87b1-250">Country</span></span>  |<span data-ttu-id="b87b1-251">Code</span><span class="sxs-lookup"><span data-stu-id="b87b1-251">Code</span></span> |<span data-ttu-id="b87b1-252">IBAN</span><span class="sxs-lookup"><span data-stu-id="b87b1-252">IBAN</span></span>  |
        |---------|---------|---------|---------|
        |<span data-ttu-id="b87b1-253">1</span><span class="sxs-lookup"><span data-stu-id="b87b1-253">-1</span></span>     |  <span data-ttu-id="b87b1-254">Österreich SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-254">Austria SEPA</span></span>      | <span data-ttu-id="b87b1-255">AT</span><span class="sxs-lookup"><span data-stu-id="b87b1-255">AT</span></span>            |<span data-ttu-id="b87b1-256">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="b87b1-256">AT611904300234573201</span></span>       |
        |<span data-ttu-id="b87b1-257">2</span><span class="sxs-lookup"><span data-stu-id="b87b1-257">2.</span></span>     |  <span data-ttu-id="b87b1-258">Bulgarien SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-258">Bulgaria SEPA</span></span>       |<span data-ttu-id="b87b1-259">BG</span><span class="sxs-lookup"><span data-stu-id="b87b1-259">BG</span></span>    |<span data-ttu-id="b87b1-260">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="b87b1-260">BG80BNBG96611020345678</span></span>      |
        |<span data-ttu-id="b87b1-261">3</span><span class="sxs-lookup"><span data-stu-id="b87b1-261">3.</span></span>     |  <span data-ttu-id="b87b1-262">Dänemark SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-262">Denmark SEPA</span></span>      |   <span data-ttu-id="b87b1-263">DK</span><span class="sxs-lookup"><span data-stu-id="b87b1-263">DK</span></span>      |<span data-ttu-id="b87b1-264">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="b87b1-264">DK5000400440116243</span></span>      |
        |<span data-ttu-id="b87b1-265">4</span><span class="sxs-lookup"><span data-stu-id="b87b1-265">4.</span></span>     |  <span data-ttu-id="b87b1-266">Finnland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-266">Finland SEPA</span></span>      |   <span data-ttu-id="b87b1-267">FI</span><span class="sxs-lookup"><span data-stu-id="b87b1-267">FI</span></span>      |<span data-ttu-id="b87b1-268">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="b87b1-268">FI2112345600000785</span></span>         |
        |<span data-ttu-id="b87b1-269">5</span><span class="sxs-lookup"><span data-stu-id="b87b1-269">5.</span></span>     |  <span data-ttu-id="b87b1-270">Frankreich SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-270">France SEPA</span></span>       |   <span data-ttu-id="b87b1-271">FR</span><span class="sxs-lookup"><span data-stu-id="b87b1-271">FR</span></span>      |<span data-ttu-id="b87b1-272">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="b87b1-272">FR1420041010050500013M02606</span></span>         |
        |<span data-ttu-id="b87b1-273">6</span><span class="sxs-lookup"><span data-stu-id="b87b1-273">6.</span></span>     |  <span data-ttu-id="b87b1-274">Deutschland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-274">Germany SEPA</span></span>      |   <span data-ttu-id="b87b1-275">DE</span><span class="sxs-lookup"><span data-stu-id="b87b1-275">DE</span></span>      |<span data-ttu-id="b87b1-276">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="b87b1-276">DE89370400440532013000</span></span>         |
        |<span data-ttu-id="b87b1-277">7</span><span class="sxs-lookup"><span data-stu-id="b87b1-277">7.</span></span>     |  <span data-ttu-id="b87b1-278">Griechenland SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-278">Greece SEPA</span></span>       |   <span data-ttu-id="b87b1-279">GR</span><span class="sxs-lookup"><span data-stu-id="b87b1-279">GR</span></span>      |<span data-ttu-id="b87b1-280">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="b87b1-280">GR1601101250000000012300695</span></span>         |
        |<span data-ttu-id="b87b1-281">8</span><span class="sxs-lookup"><span data-stu-id="b87b1-281">8.</span></span>     |  <span data-ttu-id="b87b1-282">Italien SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-282">Italy SEPA</span></span>       |    <span data-ttu-id="b87b1-283">IT</span><span class="sxs-lookup"><span data-stu-id="b87b1-283">IT</span></span>     |<span data-ttu-id="b87b1-284">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="b87b1-284">GR1601101250000000012300695</span></span>         |
        |<span data-ttu-id="b87b1-285">9</span><span class="sxs-lookup"><span data-stu-id="b87b1-285">9.</span></span>     |  <span data-ttu-id="b87b1-286">Niederlande SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-286">Netherlands SEPA</span></span>      |   <span data-ttu-id="b87b1-287">NL</span><span class="sxs-lookup"><span data-stu-id="b87b1-287">NL</span></span>      |   <span data-ttu-id="b87b1-288">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="b87b1-288">NL91ABNA0417164300</span></span>      |
        |<span data-ttu-id="b87b1-289">10</span><span class="sxs-lookup"><span data-stu-id="b87b1-289">1.0</span></span>     | <span data-ttu-id="b87b1-290">Polen SEPA</span><span class="sxs-lookup"><span data-stu-id="b87b1-290">Poland SEPA</span></span>       |  <span data-ttu-id="b87b1-291">PL</span><span class="sxs-lookup"><span data-stu-id="b87b1-291">PL</span></span>       | <span data-ttu-id="b87b1-292">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="b87b1-292">PL27114020040000300201355387</span></span>        |

<span data-ttu-id="b87b1-293">Hinweis: Dieser Beispieldatensatz wird von öffentlich verfügbaren Informationen abgeleitet und soll nur für Testzwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b87b1-293">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

23. <span data-ttu-id="b87b1-294">Sie sehen, dass die DLP-Richtlinie erkannt hat, dass der Text der E-Mail IBANs enthält und Ihnen am oberen Rand des Nachrichtenfensters den Richtlinientipp bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b87b1-294">You will see that the DLP policy recognized that body of the email contains IBANs and provides you with the policy tip at the top of the message window.</span></span>
24. <span data-ttu-id="b87b1-295">Schließen Sie die private Instanz des Browsers.</span><span class="sxs-lookup"><span data-stu-id="b87b1-295">Close the private instance of your browser.</span></span>


## <a name="phase-6-demonstrate-reporting"></a><span data-ttu-id="b87b1-296">Phase 6: Veranschaulichen der Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="b87b1-296">Phase 6: Demonstrate reporting</span></span>
 
<span data-ttu-id="b87b1-297">In dieser Phase veranschaulichen Sie die Office 365-Berichterstellung basierend auf der in Phase 5 konfigurierten DLP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b87b1-297">In this phase, you demonstrate Office 365 reporting based on the DLP policy configured in Phase 5.</span></span>

   1. <span data-ttu-id="b87b1-298">Klicken Sie auf der Registerkarte „Sicherheit und Compliance“ im Browser auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-298">From the Security & Compliance tab of your browser, click **Home**.</span></span>
   2. <span data-ttu-id="b87b1-299">Klicken Sie auf **Berichte** > **Dashboard** > **DLP-Richtlinienübereinstimmungen**.</span><span class="sxs-lookup"><span data-stu-id="b87b1-299">Click **Reports** > **Dashboard** > **DLP policy matches**.</span></span>
   3. <span data-ttu-id="b87b1-p118">Ihre DLP-Richtlinie trägt zum Identifizieren und Schützen vertraulicher Informationen der Organisation bei. Beispielsweise sehen Sie im Bericht, dass die Richtlinie das Dokuments identifiziert hat, das in SharePoint Online gespeicherte IBANs enthält.</span><span class="sxs-lookup"><span data-stu-id="b87b1-p118">Your DLP policy helps identify and protect organization's sensitive information. For example, in the report you will see that the policy identified the document that contains IBANs stored in SharePoint Online.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b87b1-302">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b87b1-302">See Also</span></span>

[<span data-ttu-id="b87b1-303">Schutz von Informationen in Office 365 für die DSGVO</span><span class="sxs-lookup"><span data-stu-id="b87b1-303">Office 365 Information Protection for GDPR</span></span>](office-365-information-protection-for-gdpr.md)

[<span data-ttu-id="b87b1-304">DSGVO für Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b87b1-304">GDPR for Microsoft 365</span></span>](https://docs.microsoft.com/microsoft-365/compliance/gdpr?toc=/microsoft-365/enterprise/toc.json)

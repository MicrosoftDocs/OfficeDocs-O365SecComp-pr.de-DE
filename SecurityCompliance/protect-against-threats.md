---
title: Schutz vor Bedrohungen in Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Verwenden Sie diesen Artikel als Leitfaden für die Konfiguration Ihrer Threat Protection-Features.
ms.openlocfilehash: 065071999130f209d63bcafc09ad72daceceac04
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261633"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="fc8a4-103">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="fc8a4-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="fc8a4-104">Office 365 umfasst eine Vielzahl von Funktionen zum Schutz vor Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="fc8a4-105">Hier finden Sie eine Schnellstartanleitung, die Sie als Prüfliste verwenden können, um sicherzustellen, dass Ihre Bedrohungsschutz Funktionen für Ihre Organisation eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="fc8a4-106">Wenn Sie neue Features für den Schutz vor Bedrohungen in Office 365 haben oder Sie nur nicht sicher sind, wo Sie anfangen sollen, verwenden Sie die folgenden Anweisungen als Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fc8a4-107">Die **anfänglichen empfohlenen Einstellungen sind für jede Art von Richtlinie enthalten; es stehen jedoch viele Optionen zur Verfügung, und Sie können Ihre Einstellungen entsprechend den Anforderungen Ihrer Organisation anpassen**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="fc8a4-108">Lassen Sie ungefähr 30 Minuten zu, bis Ihre Richtlinien oder Änderungen sich im Rechenzentrum durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8a4-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-109">Requirements</span></span>

### <a name="licenses"></a><span data-ttu-id="fc8a4-110">Lizenzen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-110">Licenses</span></span>

<span data-ttu-id="fc8a4-111">Threat Protection-Funktionen sind in allen Office 365-Abonnements enthalten; Einige Abonnements verfügen jedoch über erweiterte Funktionen wie die in Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features, such as those in Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="fc8a4-112">In diesem Artikel werden die Abonnementanforderungen für jeden Schutzbereich berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-112">In this article we include subscription requirements for each protection area.</span></span>

<span data-ttu-id="fc8a4-113">Weitere Informationen zu Threat Protection-Features und subsriptions finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-113">To learn more about threat protection features and subsriptions, see the following resources:</span></span>
- [<span data-ttu-id="fc8a4-114">Office 365 Advanced Threat Protection-Dienstbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fc8a4-114">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
- [<span data-ttu-id="fc8a4-115">Exchange Online Protection-Dienstbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fc8a4-115">Exchange Online Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-service-description)
- [<span data-ttu-id="fc8a4-116">Office 365 Security & Compliance Center</span><span class="sxs-lookup"><span data-stu-id="fc8a4-116">Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)

### <a name="roles-and-permissions"></a><span data-ttu-id="fc8a4-117">Rollen und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-117">Roles and permissions</span></span>

<span data-ttu-id="fc8a4-118">Sie müssen eine entsprechende Rolle zugewiesen sein, um Richtlinien im [Security _AMP_ Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-118">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="fc8a4-119">Die folgende Tabelle enthält einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-119">The following table includes some examples:</span></span> 

|<span data-ttu-id="fc8a4-120">Rolle oder Rollengruppe</span><span class="sxs-lookup"><span data-stu-id="fc8a4-120">Role or role group</span></span>  |<span data-ttu-id="fc8a4-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-121">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="fc8a4-122">Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="fc8a4-122">Office 365 Global Administrator</span></span> |[<span data-ttu-id="fc8a4-123">Informationen zu Administratorrollen von Office 365</span><span class="sxs-lookup"><span data-stu-id="fc8a4-123">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="fc8a4-124">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="fc8a4-124">Security Administrator</span></span> |[<span data-ttu-id="fc8a4-125">Berechtigungen für Administrator Rollen in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc8a4-125">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="fc8a4-126">Exchange Online-Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="fc8a4-126">Exchange Online Organization Management</span></span> |[<span data-ttu-id="fc8a4-127">Berechtigungen in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fc8a4-127">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="fc8a4-128">und</span><span class="sxs-lookup"><span data-stu-id="fc8a4-128">and</span></span><br> [<span data-ttu-id="fc8a4-129">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc8a4-129">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="fc8a4-130">Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-130">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="fc8a4-131">Abschnitt 1-Antischadsoftware</span><span class="sxs-lookup"><span data-stu-id="fc8a4-131">Part 1 - Anti-malware</span></span>

<span data-ttu-id="fc8a4-132">Der [Schutz](anti-malware-protection.md) vor Schadsoftware ist in Abonnements mit [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EoP) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-132">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="fc8a4-133">Wählen Sie im [Security & Compliance Center](https://protection.office.com) **Threat Management** > **Policy** > **Anti-Schadsoftware**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-133">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="fc8a4-134">Doppelklicken Sie auf die **Standard** Richtlinie, und wählen Sie dann **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-134">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="fc8a4-135">Geben Sie die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-135">Specify the following settings:</span></span>
    
    - <span data-ttu-id="fc8a4-136">Behalten Sie im Abschnitt **Malware Erkennungs Antwort** die Standardeinstellung **Nein**bei.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-136">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
   
    - <span data-ttu-id="fc8a4-137">Wählen Sie im Abschnitt **Filter für allgemeine Anlagentypen** die Option **ein**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-137">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="fc8a4-138">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-138">Click **Save**.</span></span>

<span data-ttu-id="fc8a4-139">Weitere Informationen zu Optionen für Antischadsoftware finden Sie unter [configure Anti-Malware Policies](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-139">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="fc8a4-140">Abschnitt 2-Zero-Day-Schutz</span><span class="sxs-lookup"><span data-stu-id="fc8a4-140">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="fc8a4-141">Zero-Day Protection steht in Abonnements zur Verfügung, die [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP) und die Richtlinien für ATP [Safe Attachments](atp-safe-attachments.md) und [ATP Safe Links](atp-safe-links.md) einrichten.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-141">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="fc8a4-142">Richtlinien für ATP-sichere Anlagen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-142">ATP Safe Attachments policies</span></span>

<span data-ttu-id="fc8a4-143">Zum Einrichten von [ATP Safe Attachments](atp-safe-attachments.md)müssen Sie mindestens eine ATP-Richtlinie für sichere Anlagen definieren.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-143">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="fc8a4-144">Wählen Sie im [Security & Compliance Center](https://protection.office.com)" **Threat Management** > **Policy** > **ATP Safe Attachments**" aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-144">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="fc8a4-145">Aktivieren Sie die Option **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-145">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="fc8a4-146">Klicken Sie im Abschnitt **e-Mail-Anlagen schützen** auf das**+** Pluszeichen ().</span><span class="sxs-lookup"><span data-stu-id="fc8a4-146">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="fc8a4-147">Geben Sie die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-147">Specify the following settings:</span></span>

    - <span data-ttu-id="fc8a4-148">Geben `Block malware`Sie in das Feld **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-148">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="fc8a4-149">Wählen Sie im Abschnitt Antwort die Option **Block**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-149">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="fc8a4-150">Wählen Sie im Abschnitt **Anlage umleiten** die Option **Umleitung aktivieren**aus, und geben Sie dann die e-Mail-Adresse des Sicherheitsadministrators oder-Operators Ihrer Organisation an, der erkannte Dateien überprüft.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-150">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="fc8a4-151">Wählen Sie im Abschnitt **angewendet auf** **die Empfängerdomäne ist**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-151">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="fc8a4-152">Wählen Sie dann Ihre Domäne aus, wählen Sie **Hinzufügen**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-152">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="fc8a4-153">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-153">Click **Save**.</span></span>

6. <span data-ttu-id="fc8a4-154">(**Empfohlener zusätzlicher Schritt**) Führen Sie als globaler Administrator oder SharePoint Online-Administrator das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** aus, wobei der Parameter **DisallowInfectedFileDownload** für Ihre Office 365-Umgebung auf *true* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-154">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="fc8a4-155">(Dadurch wird verhindert, dass Benutzer Dateien, die als bösartig erkannt werden, öffnen, bewegen, kopieren oder freigeben.)</span><span class="sxs-lookup"><span data-stu-id="fc8a4-155">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="fc8a4-156">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-156">To learn more, see:</span></span> 
- [<span data-ttu-id="fc8a4-157">Einrichten von Office 365 ATP-Richtlinien für sichere Anlagen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-157">Set up Office 365 ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md)
- [<span data-ttu-id="fc8a4-158">Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fc8a4-158">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)

### <a name="atp-safe-links-policies"></a><span data-ttu-id="fc8a4-159">Richtlinien für ATP-sichere Links</span><span class="sxs-lookup"><span data-stu-id="fc8a4-159">ATP Safe Links policies</span></span>

<span data-ttu-id="fc8a4-160">Um ATP- [sichere Links](atp-safe-links.md)einzurichten, überarbeiten Sie Ihre Standardrichtlinie und fügen Sie eine Richtlinie für bestimmte Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-160">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="fc8a4-161">Klicken Sie im [Security & Compliance Center](https://protection.office.com)auf **Threat Management** > **Policy** > **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-161">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="fc8a4-162">Doppelklicken Sie auf die **Standard** Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-162">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="fc8a4-163">Wählen Sie im Abschnitt **sichere Links verwenden in** die option **Office 365 ProPlus, Office für IOS und Android**aus, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-163">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="fc8a4-164">Klicken Sie im Abschnitt **Richtlinien für bestimmte Empfänger** auf das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-164">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="fc8a4-165">Geben Sie die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-165">Specify the following settings:</span></span>

    - <span data-ttu-id="fc8a4-166">Geben Sie in das Feld **Name** einen Namen ein `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-166">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="fc8a4-167">Klicken Sie im Abschnitt **Aktion auswählen** **auf ein**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-167">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="fc8a4-168">Wählen Sie die folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-168">Select these options:</span></span>

        - <span data-ttu-id="fc8a4-169">**Verwenden sicherer Anlagen zum Überprüfen von herunterladbaren Inhalten**</span><span class="sxs-lookup"><span data-stu-id="fc8a4-169">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="fc8a4-170">**Anwenden sicherer Links auf innerhalb der Organisation gesendete e-Mail-Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="fc8a4-170">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="fc8a4-171">**Nicht zulassen, dass Benutzer auf sichere Links mit ursprünglicher URL klicken**</span><span class="sxs-lookup"><span data-stu-id="fc8a4-171">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="fc8a4-172">Wählen Sie im Abschnitt **angewendet auf** **die Empfängerdomäne ist**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-172">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="fc8a4-173">Wählen Sie dann Ihre Domäne aus, wählen Sie **Hinzufügen**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-173">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="fc8a4-174">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-174">Click **Save**.</span></span>

<span data-ttu-id="fc8a4-175">Weitere Informationen finden Sie unter [Einrichten von Office 365 ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-175">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="fc8a4-176">Abschnitt 3-AntiPhishing</span><span class="sxs-lookup"><span data-stu-id="fc8a4-176">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="fc8a4-177">Der [Schutz vor Phishing](anti-phishing-protection.md) ist in Abonnements mit [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-177">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="fc8a4-178">Advanced Anti-Phishing Protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-178">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="fc8a4-179">Im folgenden Verfahren wird beschrieben, wie Sie eine ATP-Richtlinie zum Schutz vor Phishing konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-179">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="fc8a4-180">Die Schritte sind für die Konfiguration einer Richtlinie zum Schutz vor Phishing (ohne ATP) ähnlich.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-180">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="fc8a4-181">Wählen Sie im [Security & Compliance Center](https://protection.office.com)die Option **Threat Management** > **Policy** > **ATP Anti-Phishing**aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-181">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="fc8a4-182">Klicken Sie auf **Standardrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-182">Click **Default policy**.</span></span>

3. <span data-ttu-id="fc8a4-183">Klicken Sie im Abschnitt **Identitätswechsel** auf **Bearbeiten**, und geben Sie dann die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-183">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    -  <span data-ttu-id="fc8a4-184">Aktivieren Sie auf der Registerkarte **zu schützende Benutzer hinzufügen** den Schutz.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-184">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="fc8a4-185">Fügen Sie dann Benutzer wie die Vorstandsmitglieder Ihrer Organisation, ihren CEO, CFO und andere Führungskräfte hinzu.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-185">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="fc8a4-186">(Sie können eine einzelne e-Mail-Adresse eingeben oder auf klicken, um eine Liste anzuzeigen.)</span><span class="sxs-lookup"><span data-stu-id="fc8a4-186">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="fc8a4-187">Aktivieren Sie auf der Registerkarte **zu schützende Domänen hinzufügen** **die Option automatisch die Domänen**, denen ich angehört.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-187">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="fc8a4-188">Wenn Sie über benutzerdefinierte Domänen verfügen, fügen Sie diese ebenfalls hinzu.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-188">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="fc8a4-189">Wählen Sie auf der Registerkarte **Aktionen** die Option **Nachricht in den Junk-e-Mail-Ordner der Empfänger** sowohl für den imitierten Benutzer als auch für die Identität der Domäne aus, und aktivieren Sie Sicherheitstipps.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-189">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="fc8a4-190">Stellen Sie auf der Registerkarte **Mailbox Intelligence** sicher, dass die Option Mailbox Intelligence aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-190">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="fc8a4-191">Klicken Sie auf der Registerkarte **Überprüfen der Einstellungen** auf **Speichern**, nachdem Sie die Einstellungen überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-191">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="fc8a4-192">Klicken Sie im Abschnitt **Spoof** auf **Bearbeiten**, und geben Sie dann die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-192">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="fc8a4-193">Stellen Sie auf der Registerkarte Spoofing- **Filtereinstellungen** sicher, dass der Schutz vor Spoofing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-193">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="fc8a4-194">Klicken Sie auf der Registerkarte **Aktionen** auf Nachricht in die Junk-e-Mail-Ordner der Empfänger verschieben.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-194">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="fc8a4-195">Klicken Sie auf der Registerkarte **Überprüfen der Einstellungen** auf **Speichern**, nachdem Sie die Einstellungen überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-195">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="fc8a4-196">(Wenn Sie keine Änderungen vorgenommen haben, klicken Sie auf **Abbrechen**.)</span><span class="sxs-lookup"><span data-stu-id="fc8a4-196">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="fc8a4-197">Beenden Sie die Seite Standardrichtlinieneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-197">Close the default policy settings page.</span></span>

<span data-ttu-id="fc8a4-198">Weitere Informationen zu den Optionen für die Anti-Phishing-Richtlinie finden Sie unter [Einrichten von Richtlinien zum Schutz](set-up-anti-phishing-policies.md)vor Phishing.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-198">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="fc8a4-199">Abschnitt 4-Antispam</span><span class="sxs-lookup"><span data-stu-id="fc8a4-199">Part 4 - Anti-spam</span></span>

<span data-ttu-id="fc8a4-200">[](anti-spam-protection.md) Antispamschutz ist in Abonnements mit [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-200">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="fc8a4-201">Wählen Sie im [Security & Compliance Center](https://protection.office.com)**Anti-Spam**für **Threat Management** > **Policy** > aus.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-201">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="fc8a4-202">Aktivieren Sie auf der Registerkarte **benutzerdefinierte** **Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="fc8a4-202">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="fc8a4-203">Erweitern Sie **Standard-Spamfilter Richtlinie**, klicken Sie auf **Richtlinie bearbeiten**, und geben Sie dann die folgenden Einstellungen an:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-203">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="fc8a4-204">Legen Sie im Abschnitt **Spam-und Massenaktionen** den Schwellenwert auf 5 oder 6 fest.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-204">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="fc8a4-205">Überarbeiten Sie im Abschnitt **Zulassungslisten** die zulässigen Absender und Domänen, und bearbeiten Sie Sie gegebenenfalls.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-205">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="fc8a4-206">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-206">Click **Save**.</span></span>

<span data-ttu-id="fc8a4-207">Weitere Informationen zu ihren Antispampolitik-Optionen finden Sie unter [configure the Anti-Spam](configure-the-anti-spam-policies.md)Policys.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-207">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="fc8a4-208">Abschnitt 5-dienstweite Einstellungen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-208">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="fc8a4-209">Automatische Bereinigung ohne Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="fc8a4-209">Zero-hour auto purge</span></span>

<span data-ttu-id="fc8a4-210">[Automatische Bereinigung ohne Uhrzeit](zero-hour-auto-purge.md) (ZAP) ist in Abonnements verfügbar, die [EoP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)enthält.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-210">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="fc8a4-211">Dieser Schutz ist standardmäßig aktiviert. die folgenden Bedingungen müssen jedoch erfüllt sein, damit der Schutz wirksam wird:</span><span class="sxs-lookup"><span data-stu-id="fc8a4-211">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="fc8a4-212">Spam Aktionen sind so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner verschoben** wird. [](anti-spam-protection.md)</span><span class="sxs-lookup"><span data-stu-id="fc8a4-212">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="fc8a4-213">Benutzer haben Ihre Standard [Einstellungen für Junk-e-Mails](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-213">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="fc8a4-214">Weitere Informationen finden Sie unter [Zero-Hour-automatische Bereinigung – Schutz vor Spam und Schadsoftware](zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-214">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="fc8a4-215">Überwachungsprotokollierung</span><span class="sxs-lookup"><span data-stu-id="fc8a4-215">Audit logging</span></span>

<span data-ttu-id="fc8a4-216">Die Überwachungsprotokollierung ist in Abonnements verfügbar, die [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-216">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="fc8a4-217">Um Daten in Bedrohungsschutz Berichten wie [Sicherheits Dashboard](security-dashboard.md), [e-Mail-Sicherheitsberichte](view-email-security-reports.md)und [Explorer](use-explorer-in-security-and-compliance.md)anzuzeigen, muss die Überwachungsprotokollierung für Ihre Organisation aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-217">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="fc8a4-218">Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="fc8a4-218">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="fc8a4-219">Aufgaben nach der Installation</span><span class="sxs-lookup"><span data-stu-id="fc8a4-219">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="fc8a4-220">Überwachen von neuen Features und dienstupdates</span><span class="sxs-lookup"><span data-stu-id="fc8a4-220">Watch for new features and service updates</span></span>

- [<span data-ttu-id="fc8a4-221">Einrichten der Standard-oder Zielfreigabe Optionen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-221">Set up the Standard or Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)

- [<span data-ttu-id="fc8a4-222">Navigieren Sie zu Ihrem Nachrichtencenter, um die Funktions Ankündigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-222">Go to your Message center to view feature announcements</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide) 

- [<span data-ttu-id="fc8a4-223">Besuchen Sie die Microsoft 365-Roadmap, um den Status neuer Features anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-223">Visit the Microsoft 365 Roadmap to see status of new features</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="fc8a4-224">Lesen Sie die Office 365-Dienstbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="fc8a4-224">Review the Office 365 Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)

### <a name="see-how-threat-protection-features-are-working-for-your-organization"></a><span data-ttu-id="fc8a4-225">Informationen zur Funktionsweise von Threat Protection-Funktionen für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="fc8a4-225">See how threat protection features are working for your organization</span></span>

- [<span data-ttu-id="fc8a4-226">Besuchen Sie Ihr Sicherheits Dashboard</span><span class="sxs-lookup"><span data-stu-id="fc8a4-226">Visit your security dashboard</span></span>](security-dashboard.md)

- <span data-ttu-id="fc8a4-227">[Anzeigen der Berichte für Office 365 ATP](view-reports-for-atp.md), einschließlich [Explorer](use-explorer-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="fc8a4-227">[View the reports for Office 365 ATP](view-reports-for-atp.md), including [Explorer](use-explorer-in-security-and-compliance.md)</span></span>

- [<span data-ttu-id="fc8a4-228">Anzeigen Ihrer e-Mail-Sicherheitsberichte</span><span class="sxs-lookup"><span data-stu-id="fc8a4-228">View your email security reports</span></span>](view-email-security-reports.md)

### <a name="periodically-review-and-revise-your-threat-protection-policies"></a><span data-ttu-id="fc8a4-229">Regelmäßiges Überprüfen und Überarbeiten der Bedrohungsschutz Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fc8a4-229">Periodically review and revise your threat protection policies</span></span>

- [<span data-ttu-id="fc8a4-230">Überwachen des sicheren Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="fc8a4-230">Review your Secure Score</span></span>](microsoft-secure-score.md)

- [<span data-ttu-id="fc8a4-231">Verwenden ihrer intelligenten Berichte und Einblicke im &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="fc8a4-231">Use your smart reports and insights in the Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 

- [<span data-ttu-id="fc8a4-232">Schützen von Benutzern mit Office 365 Bedrohungs Ermittlungs-und-Antwortfunktionen</span><span class="sxs-lookup"><span data-stu-id="fc8a4-232">Keep users safe with Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md) 
 
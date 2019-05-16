---
title: Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
description: Hier erfahren Sie, wie Sie ATP für SharePoint, OneDrive und Teams aktivieren, einschließlich der Festlegung von Warnungen für erkannte Dateien.
ms.openlocfilehash: 6b7403ceff810d96c677fc6af7673547424346b8
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077241"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="bc938-103">Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bc938-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="bc938-104">[Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor versehentlicher Freigabe schädlicher Dateien.</span><span class="sxs-lookup"><span data-stu-id="bc938-104">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="bc938-105">Wenn eine bösartige Datei erkannt wird, wird diese Datei blockiert, sodass niemand Sie öffnen, kopieren, verschieben oder freigeben kann, bis weitere Aktionen des Sicherheitsteams der Organisation durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc938-105">When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team.</span></span> <span data-ttu-id="bc938-106">Lesen Sie diesen Artikel, um ATP für SharePoint, OneDrive und Teams zu aktivieren, Warnungen für die Erkennung von Dateien einzurichten und die nächsten Schritte zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="bc938-106">Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="bc938-107">Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bc938-107">To define (or edit) ATP policies, you must be assigned an appropriate role.</span></span> <span data-ttu-id="bc938-108">Einige Beispiele werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="bc938-108">Some examples are described in the following table:</span></span>

|<span data-ttu-id="bc938-109">Rolle</span><span class="sxs-lookup"><span data-stu-id="bc938-109">Role</span></span>  |<span data-ttu-id="bc938-110">Wo/wie zugewiesen</span><span class="sxs-lookup"><span data-stu-id="bc938-110">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="bc938-111">Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="bc938-111">Office 365 Global Administrator</span></span> |<span data-ttu-id="bc938-112">Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator.</span><span class="sxs-lookup"><span data-stu-id="bc938-112">The person who signs up to buy Office 365 is a global admin by default.</span></span> <span data-ttu-id="bc938-113">(Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="bc938-113">(See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="bc938-114">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="bc938-114">Security Administrator</span></span> |<span data-ttu-id="bc938-115">Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="bc938-115">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="bc938-116">Exchange Online-Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="bc938-116">Exchange Online Organization Management</span></span> |<span data-ttu-id="bc938-117">Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)()</span><span class="sxs-lookup"><span data-stu-id="bc938-117">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="bc938-118">oder</span><span class="sxs-lookup"><span data-stu-id="bc938-118">or</span></span> <br>  <span data-ttu-id="bc938-119">PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="bc938-119">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="bc938-120">Aktivieren von ATP für SharePoint, OneDrive und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bc938-120">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="bc938-121">**Bevor Sie mit diesem Verfahren beginnen, sollten Sie sicherstellen, dass die Überwachungsprotokollierung für Ihre Office 365-Umgebung bereits aktiviert ist**.</span><span class="sxs-lookup"><span data-stu-id="bc938-121">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**.</span></span> <span data-ttu-id="bc938-122">Dies erfolgt in der Regel durch einen Benutzer, dem die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="bc938-122">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="bc938-123">Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="bc938-123">For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="bc938-124">Wechseln Sie [https://protection.office.com](https://protection.office.com)zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.</span><span class="sxs-lookup"><span data-stu-id="bc938-124">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="bc938-125">Wählen Sie im Office 365 &amp; Security Compliance Center im linken Navigationsbereich unter Bedrohungs **Verwaltung**die Option **Richtlinie** \> für **sichere Anlagen**aus.</span><span class="sxs-lookup"><span data-stu-id="bc938-125">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="bc938-126">![Wählen Sie im &amp; Security Compliance Center die Option Threat \> Management Policy aus.](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="bc938-126">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="bc938-127">Wählen Sie **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="bc938-127">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="bc938-128">![Aktivieren von Advanced Threat Protection für SharePoint Online, OneDrive for Business und Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="bc938-128">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="bc938-129">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bc938-129">Click **Save**.</span></span>
    
5. <span data-ttu-id="bc938-130">Überarbeiten Sie die Richt [Linien zu sicheren Anlagen](set-up-atp-safe-attachments-policies.md) und Richtlinien für [sichere Links](set-up-atp-safe-links-policies.md)in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="bc938-130">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="bc938-131">Empfohlen Führen Sie als globaler Administrator oder SharePoint Online-Administrator das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** aus, wobei der Parameter **DisallowInfectedFileDownload** auf *true*festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bc938-131">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="bc938-132">Wenn der Parameter auf *true* festgelegt wird, werden alle Aktionen (außer DELETE) für erkannte Dateien blockiert.</span><span class="sxs-lookup"><span data-stu-id="bc938-132">Setting the parameter to *true* blocks all actions (except Delete) for detected files.</span></span> <span data-ttu-id="bc938-133">Personen können erkannte Dateien nicht öffnen, verschieben, kopieren oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="bc938-133">People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="bc938-134">Wenn der Parameter auf *false* festgelegt wird, werden alle Aktionen außer löschen und herunterladen blockiert.</span><span class="sxs-lookup"><span data-stu-id="bc938-134">Setting the parameter to *false* blocks all actions except Delete and Download.</span></span> <span data-ttu-id="bc938-135">Personen können das Risiko annehmen und eine erkannte Datei herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bc938-135">People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="bc938-136">Sie können bis zu 30 Minuten dauern, bis Ihre Änderungen auf alle Office 365-Rechenzentren verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="bc938-136">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="bc938-137">Empfohlen Gehen Sie vor, um Warnungen für erkannte Dateien einzurichten.</span><span class="sxs-lookup"><span data-stu-id="bc938-137">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="bc938-138">Weitere Informationen zur Verwendung von PowerShell mit Office 365 finden Sie unter [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="bc938-138">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="bc938-139">Weitere Informationen zur Benutzererfahrung, wenn eine Datei als bösartig erkannt wurde, finden Sie unter [Vorgehensweise, wenn eine bösartige Datei in SharePoint Online, OneDrive oder Microsoft Teams gefunden wird](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="bc938-139">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="bc938-140">Einrichten von Warnungen für erkannte Dateien</span><span class="sxs-lookup"><span data-stu-id="bc938-140">Set up alerts for detected files</span></span>

<span data-ttu-id="bc938-141">Um eine Benachrichtigung zu erhalten, wenn eine Datei in SharePoint Online, OneDrive for Business oder Microsoft Teams als bösartig identifiziert wurde, können Sie eine Warnung einrichten.</span><span class="sxs-lookup"><span data-stu-id="bc938-141">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="bc938-142">Wählen Sie im [Office 365 &amp; Security Compliance Center](https://protection.office.com) **Alerts** \> **Manage Alerts**aus.</span><span class="sxs-lookup"><span data-stu-id="bc938-142">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="bc938-143">Wählen Sie **neue Warnungs Richtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="bc938-143">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="bc938-144">Geben Sie einen Namen für die Warnung an.</span><span class="sxs-lookup"><span data-stu-id="bc938-144">Specify a name for the alert.</span></span> <span data-ttu-id="bc938-145">Sie können beispielsweise schädliche Dateien in Bibliotheken eingeben.</span><span class="sxs-lookup"><span data-stu-id="bc938-145">For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="bc938-146">Geben Sie eine Beschreibung für die Warnung ein.</span><span class="sxs-lookup"><span data-stu-id="bc938-146">Type a description for the alert.</span></span> <span data-ttu-id="bc938-147">Beispielsweisekönnten Sie benachrichtigt Administratoren eingeben, wenn schädliche Dateien in SharePoint Online, OneDrive oder Microsoft Teams erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="bc938-147">For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="bc938-148">Führen Sie im Abschnitt **Diese Warnung senden, wenn...** die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="bc938-148">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="bc938-149">a.</span><span class="sxs-lookup"><span data-stu-id="bc938-149">a.</span></span> <span data-ttu-id="bc938-150">Wählen Sie in der Liste **Aktivitäten** die Option **erkannte Schadsoftware in Datei**aus.</span><span class="sxs-lookup"><span data-stu-id="bc938-150">In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="bc938-151">b.</span><span class="sxs-lookup"><span data-stu-id="bc938-151">b.</span></span> <span data-ttu-id="bc938-152">Lassen Sie das Feld **Benutzer** leer.</span><span class="sxs-lookup"><span data-stu-id="bc938-152">Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="bc938-153">Wählen Sie im Abschnitt **diese Benachrichtigung senden an** einen oder mehrere globale Administratoren, Sicherheitsadministratoren oder Sicherheits Leser aus, die Benachrichtigungen erhalten sollen, wenn eine bösartige Datei erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bc938-153">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="bc938-154">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bc938-154">Click **Save**.</span></span>
    
<span data-ttu-id="bc938-155">Weitere Informationen zu Warnungen finden Sie unter [Create Activity Alerts in the Office 365 &amp; Security Compliance Center](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="bc938-155">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="bc938-156">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="bc938-156">Next steps</span></span>

1. [<span data-ttu-id="bc938-157">Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden</span><span class="sxs-lookup"><span data-stu-id="bc938-157">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="bc938-158">Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365</span><span class="sxs-lookup"><span data-stu-id="bc938-158">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  


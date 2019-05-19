---
title: Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Sie können das Feature für die Überwachungsprotokoll Suche im Security & Compliance Center aktivieren. Wenn Sie Ihre Meinung ändern, können Sie jederzeit deaktivieren. Wenn die Überwachungsprotokoll Suche deaktiviert ist, können Administratoren das Office 365 Überwachungsprotokoll nicht nach Benutzer-und Administratoraktivitäten in Ihrer Organisation durchsuchen.
ms.openlocfilehash: c5e1106617aa4828ec2db5afcc44ac55e91f2383
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158297"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="c67ec-105">Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche</span><span class="sxs-lookup"><span data-stu-id="c67ec-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="c67ec-106">Sie (oder ein anderer Administrator) müssen die Überwachungsprotokollierung aktivieren, bevor Sie mit der Suche im Office 365 Überwachungsprotokoll beginnen können.</span><span class="sxs-lookup"><span data-stu-id="c67ec-106">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log.</span></span> <span data-ttu-id="c67ec-107">Wenn die Überwachungsprotokoll Suche im Security & Compliance Center aktiviert ist, werden Benutzer-und Administratoraktivitäten aus Ihrer Organisation im Überwachungsprotokoll aufgezeichnet und für 90 Tage aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="c67ec-107">When audit log search in the Security & Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days.</span></span> <span data-ttu-id="c67ec-108">Ihre Organisation möchte jedoch möglicherweise keine Überwachungsprotokolldaten aufzeichnen und aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-108">However, your organization might not want to record and retain audit log data.</span></span> <span data-ttu-id="c67ec-109">Oder Sie verwenden möglicherweise eine Siem-Anwendung (Security Information and Event Management) eines Drittanbieters, um auf Ihre Überwachungsdaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c67ec-109">Or you might be using a third-party security information and event management (SIEM) application to access your auditing data.</span></span> <span data-ttu-id="c67ec-110">In diesen Fällen kann ein globaler Administrator die Überwachungsprotokoll Suche in Office 365 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-110">In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="c67ec-111">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="c67ec-111">Before you begin</span></span>

- <span data-ttu-id="c67ec-112">Sie müssen die Rolle Überwachungsprotokolle in Exchange Online zugewiesen haben, um die Überwachungsprotokoll Suche in Ihrer Office 365 Organisation ein-oder auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="c67ec-112">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization.</span></span> <span data-ttu-id="c67ec-113">Diese Rolle wird standardmäßig der Rollengruppe Compliance Management und Organisationsverwaltung auf der Seite **Berechtigungen** im Exchange Admin Center zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c67ec-113">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="c67ec-114">Globale Administratoren in Office 365 sind Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c67ec-114">Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="c67ec-115">Benutzern müssen Berechtigungen in Exchange Online zugewiesen sein, um die Überwachungsprotokoll Suche ein-oder auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="c67ec-115">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="c67ec-116">Wenn Sie den Benutzern die Rolle "Überwachungsprotokolle" auf der Seite **Berechtigungen** im Security & Compliance Center zuweisen, kann die Überwachungsprotokoll Suche nicht aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c67ec-116">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="c67ec-117">Dies liegt daran, dass das zugrunde liegende Cmdlet ein Exchange Online-Cmdlet ist.</span><span class="sxs-lookup"><span data-stu-id="c67ec-117">This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="c67ec-118">Wenn Sie die Überwachungsprotokoll Suche in Office 365 deaktivieren, können Sie die Office 365-Verwaltungs Aktivitäts-API nicht verwenden, um auf Überwachungsdaten für Ihre Organisation zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c67ec-118">If you turn off audit log search in Office 365, you won't be able to use the Office 365 Management Activity API to access auditing data for your organization.</span></span> <span data-ttu-id="c67ec-119">Das Deaktivieren der Suche im Überwachungsprotokoll durch Befolgen der Schritte in diesem Artikel bedeutet, dass beim Durchsuchen des Überwachungsprotokolls mit dem Security & Compliance Center oder beim Ausführen des Cmdlets **Search-UnifiedAuditLog** in Exchange Online keine Ergebnisse zurückgegeben werden. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c67ec-119">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="c67ec-120">Dies bedeutet auch, dass Ihre Überwachungsprotokolle nicht über die Office 365 Verwaltungs Aktivitäts-API verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c67ec-120">This also means that your audit logs won't be available through the Office 365 Management Activity API.</span></span>  
    
- <span data-ttu-id="c67ec-121">Eine Schritt-für-Schritt-Anleitung zum Durchsuchen des Office 365 Überwachungsprotokolls finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="c67ec-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="c67ec-122">Aktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="c67ec-122">Turn on audit log search</span></span>

<span data-ttu-id="c67ec-123">Sie können das Security & Compliance Center oder die PowerShell verwenden, um die Überwachungsprotokoll Suche in Office 365 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-123">You can use the Security & Compliance Center or PowerShell to turn on audit log search in Office 365.</span></span> <span data-ttu-id="c67ec-124">Es kann mehrere Stunden dauern, nachdem Sie die Überwachungsprotokoll Suche aktiviert haben, bevor Sie Ergebnisse zurückgeben können, wenn Sie das Überwachungsprotokoll durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c67ec-124">It might take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span> <span data-ttu-id="c67ec-125">Sie müssen der Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen sein, um die Überwachungsprotokoll Suche zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-125">You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="c67ec-126">Verwenden des Security & Compliance Center zum Aktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="c67ec-126">Use the Security & Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="c67ec-127">Wechseln Sie im Security & Compliance Center zu **Such** \> **Überwachungsprotokoll-Suche**.</span><span class="sxs-lookup"><span data-stu-id="c67ec-127">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="c67ec-128">Klicken Sie auf **Aufzeichnung von Benutzer-und Administratoraktivitäten starten**.</span><span class="sxs-lookup"><span data-stu-id="c67ec-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Klicken Sie auf Aufzeichnung von Benutzer-und Administratoraktivitäten starten, um die Überwachung zu aktivieren](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="c67ec-130">Es wird ein Dialogfeld angezeigt, das besagt, dass Benutzer-und Administratoraktivitäten in Ihrer Organisation im Office 365 Überwachungsprotokoll aufgezeichnet und in einem Bericht angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="c67ec-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="c67ec-131">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="c67ec-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="c67ec-132">Es wird eine Meldung angezeigt, die besagt, dass das Überwachungsprotokoll vorbereitet wird und dass Sie eine Suche in einigen Stunden nach Abschluss der Vorbereitung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c67ec-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="c67ec-133">Aktivieren der Überwachungsprotokoll Suche mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c67ec-133">Use PowerShell to turn on audit log search</span></span>

1. <span data-ttu-id="c67ec-134">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="c67ec-134">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="c67ec-135">Führen Sie den folgenden PowerShell-Befehl aus, um die Überwachungsprotokoll Suche in Office 365 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="c67ec-136">Es wird eine Meldung angezeigt, die besagt, dass es bis zu 60 Minuten dauern kann, bis die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="c67ec-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="c67ec-137">Deaktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="c67ec-137">Turn off audit log search</span></span>

<span data-ttu-id="c67ec-138">Sie müssen Remote-PowerShell verwenden, die mit Ihrer Exchange Online Organisation verbunden ist, um die Überwachungsprotokoll Suche zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-138">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search.</span></span> <span data-ttu-id="c67ec-139">Ähnlich wie beim Aktivieren der Überwachungsprotokoll Suche müssen Sie der Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen sein, um die Überwachungsprotokoll Suche zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-139">Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. <span data-ttu-id="c67ec-140">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="c67ec-140">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="c67ec-141">Führen Sie den folgenden PowerShell-Befehl aus, um die Überwachungsprotokoll Suche in Office 365 zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c67ec-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="c67ec-142">Überprüfen Sie nach einer Weile, ob die Überwachungsprotokoll Suche deaktiviert (disabled) ist.</span><span class="sxs-lookup"><span data-stu-id="c67ec-142">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="c67ec-143">Sie können auf zwei Arten vorgehen:</span><span class="sxs-lookup"><span data-stu-id="c67ec-143">There are two ways to do this:</span></span>
    
    - <span data-ttu-id="c67ec-144">Führen Sie in PowerShell den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c67ec-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="c67ec-145">Der Wert von `False` für die _UnifiedAuditLogIngestionEnabled_ -Eigenschaft gibt an, dass die Überwachungsprotokoll Suche deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c67ec-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="c67ec-146">Wechseln Sie im Security & Compliance Center zu **Such** \> **Überwachungsprotokoll Suche**, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="c67ec-146">In the Security & Compliance Center, go to **Search** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="c67ec-147">Es wird eine Meldung angezeigt, die besagt, dass die Überwachungsprotokoll Suche nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c67ec-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Wenn die Überwachung deaktiviert ist, wird eine Meldung angezeigt.](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)

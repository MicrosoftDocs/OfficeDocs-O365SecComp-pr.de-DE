---
title: Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Sie können die Audit Log-Suchfunktion in die Office 365-Sicherheit aktivieren &amp; Compliance Center. Wenn Sie Sie überlegen, können Sie aktivieren If deaktiviert zu einem beliebigen Zeitpunkt. Wenn Audit Log Suche deaktiviert ist, können nicht Administratoren das Office 365-Überwachungsprotokoll für Benutzer- und Admin-Aktivität in Ihrer Organisation suchen.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529466"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="d974b-105">Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche</span><span class="sxs-lookup"><span data-stu-id="d974b-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="d974b-p102">Protokollierung, bevor Sie beginnen können, suchen das Office 365-Überwachungsprotokoll müssen Sie (oder ein anderes Admin) aktivieren. Wenn audit Log-Suche in der Office 365-Sicherheit &amp; Compliance Center aktiviert ist, Benutzer und Admin-Aktivität aus Ihrer Organisation ist im Überwachungsprotokoll aufgezeichnet und 90 Tage lang aufbewahrt. Allerdings sollten Ihrer Organisation nicht zum Aufzeichnen und Aufbewahren von Audit Log-Daten. Oder möglicherweise verwenden Sie eine Anwendung Drittanbieter-Sicherheit und Ereignissen Management (SIEM) auf die Überwachung von Daten zugreifen. In diesen Fällen kann ein globaler Administrator Audit Log Suche in Office 365 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d974b-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="d974b-111">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="d974b-111">Before you begin</span></span>

- <span data-ttu-id="d974b-p103">Sie müssen die Rolle des überwachen Protokolle im Exchange Online zu Audit Log Suche aktivieren oder deaktivieren Sie in Office 365-Organisation zugewiesen werden. Standardmäßig wird die Verwaltung der Richtlinientreue und Organization Management Rollengruppen auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole dieser Rolle zugewiesen. Globale Administratoren in Office 365 gehören die Rollengruppe "Organisationsverwaltung" im Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d974b-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="d974b-p104">Benutzer müssen Berechtigungen in Exchange Online um zu aktivieren oder deaktivieren Sie Audit Log Suche zugewiesen werden. Wenn Sie Benutzern die Rolle überwachen Protokolle auf der Seite **Berechtigungen** in das Wertpapier zuweisen &amp; Compliance Center, sie nicht möglich Audit Log Suche aktivieren oder deaktivieren. Dies ist, da das zugrunde liegende Cmdlet Exchange Online-Cmdlet ist.</span><span class="sxs-lookup"><span data-stu-id="d974b-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="d974b-p105">Wenn Sie den Audit Log Suche in Office 365 deaktivieren, können Sie weiterhin die Office 365-Verwaltungs-Aktivität-API verwenden, Überwachung von Daten für Ihre Organisation Zugriff auf. Deaktivieren von Audit Log Suche mithilfe der Schritte in diesem Artikel bedeutet, dass keine Ergebnisse zurückgegeben werden, wenn Sie das Überwachungsprotokoll mithilfe der Sicherheits suchen &amp; Compliance Center oder bei der Ausführung des Cmdlets **Search-UnifiedAuditLog** in Exchange Online PowerShell. Wenn Sie jeder Anwendung zur Überwachung Ihrer Organisation von Daten über die Office 365-Verwaltungs-Aktivität API Zugriff erteilt haben, werden jedoch Anwendungsbereiche fortgesetzt, funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d974b-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="d974b-121">Eine schrittweise Anleitung zum Suchen der Office 365 in das Überwachungsprotokoll, finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="d974b-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="d974b-122">Schalten Sie Audit Log-Suche</span><span class="sxs-lookup"><span data-stu-id="d974b-122">Turn on audit log search</span></span>

<span data-ttu-id="d974b-p106">Sie können die Sicherheit &amp; Compliance Center oder PowerShell, um Audit Log Suche in Office 365 zu aktivieren. Es kann einige Stunden, nachdem Sie Audit Log Suche aktivieren, bevor Sie Ergebnisse zurückgeben können, wenn Sie das Überwachungsprotokoll durchsuchen dauern. Sie müssen die Protokolle überwachen Rolle im Exchange Online zugewiesen werden um Audit Log Suche zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d974b-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="d974b-126">Verwenden Sie die Sicherheit &amp; Compliance Center Audit Log Suche aktivieren</span><span class="sxs-lookup"><span data-stu-id="d974b-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="d974b-127">In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Audit Log suchen**.</span><span class="sxs-lookup"><span data-stu-id="d974b-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="d974b-128">Klicken Sie auf **Benutzer und Admin Aktivitäten Aufzeichnung starten**.</span><span class="sxs-lookup"><span data-stu-id="d974b-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Klicken Sie auf „Aufzeichnung von Benutzer- und Administratoraktivitäten beginnen“, um die Überwachung zu aktivieren.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="d974b-130">Ein Dialogfeld wird angezeigt, dass Benutzer und die Admin-Aktivitäten in Ihrer Organisation in das Office 365-Überwachungsprotokoll aufgezeichneten und zum Anzeigen von in einem Bericht verfügbar sein werden.</span><span class="sxs-lookup"><span data-stu-id="d974b-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="d974b-131">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="d974b-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="d974b-132">Eine Meldung wird angezeigt, die besagt, das Überwachungsprotokoll vorbereitet wird und dass Sie eine Suche, in ein paar Stunden ausführen können nach Abschluss die Vorbereitung.</span><span class="sxs-lookup"><span data-stu-id="d974b-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="d974b-133">Verwenden von PowerShell, Audit Log Suche aktivieren</span><span class="sxs-lookup"><span data-stu-id="d974b-133">Use PowerShell to turn on audit log search</span></span>

1. <span data-ttu-id="d974b-134">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="d974b-134">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="d974b-135">Führen Sie den folgenden PowerShell-Befehl, um Audit Log Suche in Office 365 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d974b-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="d974b-136">Eine Meldung wird angezeigt, die besagt, dass dauert bis zu 60 Minuten, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="d974b-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="d974b-137">Audit Log Suche deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d974b-137">Turn off audit log search</span></span>

<span data-ttu-id="d974b-p107">Sie müssen remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden zu Audit Log deaktivieren verwenden. Ähnliche Audit Log Suche aktivieren, müssen Sie die Protokolle überwachen Rolle in Exchange Online zu Audit Log deaktivieren zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d974b-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. <span data-ttu-id="d974b-140">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="d974b-140">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="d974b-141">Führen Sie den folgenden PowerShell-Befehl zu Audit Log in Office 365 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d974b-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="d974b-p108">Nach einer gewissen stellen Sie sicher, dass die Audit Log Suche deaktiviert (Disabled) aktiviert ist. Es gibt zwei Methoden, um diese Schritte durchführen:</span><span class="sxs-lookup"><span data-stu-id="d974b-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="d974b-144">Führen Sie in PowerShell den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="d974b-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="d974b-145">Der Wert der `False` für die _UnifiedAuditLogIngestionEnabled_ -Eigenschaft gibt an, dass die Audit Log Suche ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d974b-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="d974b-146">In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Audit Log suchen**, und klicken Sie auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="d974b-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="d974b-147">Eine Meldung wird angezeigt, die besagt, dass Audit Log die Suche nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d974b-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Eine Nachricht ist Dispayed, wenn die Überwachung deaktiviert ist](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)

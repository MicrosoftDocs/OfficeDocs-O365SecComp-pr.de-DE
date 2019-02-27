---
title: Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
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
description: Sie können die Suchfunktion des Überwachungsprotokolls im Office 365 Security &amp; Compliance Center aktivieren. Wenn Sie es ändern, können Sie jederzeit deaktivieren. Wenn die Überwachungsprotokoll Suche deaktiviert ist, können Administratoren das Office 365-Überwachungsprotokoll nicht nach Benutzer-und Administratoraktivitäten in Ihrer Organisation durchsuchen.
ms.openlocfilehash: 17b98cce26054d073006fa78c55fe418b5f327d8
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295458"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="8f484-105">Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche</span><span class="sxs-lookup"><span data-stu-id="8f484-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="8f484-p102">Sie (oder ein anderer Administrator) muss die Überwachungsprotokollierung aktivieren, bevor Sie mit der Durchsuchung des Office 365-Überwachungsprotokolls beginnen können. Wenn die Überwachungsprotokoll Suche im Office 365 Security &amp; Compliance Center aktiviert ist, werden die Benutzer-und Administratoraktivitäten Ihrer Organisation im Überwachungsprotokoll aufgezeichnet und für 90 Tage aufbewahrt. Ihre Organisation möchte jedoch möglicherweise keine Überwachungsprotokolldaten aufzeichnen und aufbewahren. Oder Sie verwenden möglicherweise eine Drittanbieter-App für das Security Information and Event Management (SIEM), um auf Ihre Überwachungsdaten zuzugreifen. In diesen Fällen kann ein globaler Administrator die Suchprotokoll Suche in Office 365 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f484-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="8f484-111">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="8f484-111">Before you begin</span></span>

- <span data-ttu-id="8f484-p103">Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" verfügen, um die Überwachungsprotokoll Suche in Ihrer Office 365-Organisation zu aktivieren oder zu deaktivieren. Diese Rolle wird standardmäßig der Rollengruppe "Compliance-Management" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Globale Administratoren in Office 365 sind Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8f484-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="8f484-p104">Benutzer müssen in Exchange Online über Berechtigungen verfügen, um die Überwachungsprotokoll Suche ein-oder auszuschalten. Wenn Sie Benutzern die Rolle Überwachungsprotokolle auf der Seite **Berechtigungen** im Security &amp; Compliance Center zuweisen, können Sie die Überwachungsprotokoll Suche nicht aktivieren oder deaktivieren. Dies liegt daran, dass das zugrunde liegende Cmdlet ein Exchange Online-Cmdlet ist.</span><span class="sxs-lookup"><span data-stu-id="8f484-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="8f484-p105">Wenn Sie die Überwachungsprotokoll Suche in Office 365 deaktivieren, können Sie weiterhin die Office 365-Verwaltungs Aktivitäts-API verwenden, um auf Überwachungsdaten für Ihre Organisation zuzugreifen. Durch das Deaktivieren der Überwachungsprotokoll Suche mithilfe der Schritte in diesem Artikel werden keine Ergebnisse zurückgegeben, wenn Sie das Überwachungsprotokoll mithilfe des Security &amp; Compliance Center durchsuchen oder wenn Sie das Cmdlet **Search-UnifiedAuditLog** in Exchange Online ausführen. PowerShell. Wenn Sie jedoch eine Anwendung autorisiert haben, über die Office 365-Verwaltungs Aktivitäts-API auf die Überwachungsdaten Ihrer Organisation zuzugreifen, funktionieren diese Anwendungen weiterhin.</span><span class="sxs-lookup"><span data-stu-id="8f484-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="8f484-121">Schrittweise Anleitungen zum Durchsuchen des Office 365-Überwachungsprotokolls finden Sie unter durch [Suchen des Überwachungsprotokolls im office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="8f484-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="8f484-122">Aktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="8f484-122">Turn on audit log search</span></span>

<span data-ttu-id="8f484-p106">Sie können das Security &amp; Compliance Center oder PowerShell verwenden, um die Suche nach Überwachungsprotokollen in Office 365 zu aktivieren. Es kann mehrere Stunden dauern, bis Sie die Überwachungsprotokoll Suche aktiviert haben, bevor Sie beim Durchsuchen des Überwachungsprotokolls Ergebnisse zurückgeben können. Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" verfügen, um die Suche nach Überwachungsprotokollen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f484-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="8f484-126">Verwenden des Security &amp; Compliance Center zum Aktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="8f484-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="8f484-127">Wechseln Sie im &amp; Security Compliance Center zur Such \*\* &amp; Untersuchungs\*\* \> - **Überwachungsprotokoll**Suche.</span><span class="sxs-lookup"><span data-stu-id="8f484-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="8f484-128">Klicken Sie auf **Aufzeichnung von Benutzer-und Administratoraktivitäten starten**.</span><span class="sxs-lookup"><span data-stu-id="8f484-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Klicken Sie auf „Aufzeichnung von Benutzer- und Administratoraktivitäten beginnen“, um die Überwachung zu aktivieren.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="8f484-130">Es wird ein Dialogfeld mit der Meldung angezeigt, dass die Benutzer-und Administratoraktivitäten in Ihrer Organisation im Office 365-Überwachungsprotokoll aufgezeichnet werden und in einem Bericht angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="8f484-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="8f484-131">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="8f484-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="8f484-132">Es wird eine Meldung angezeigt, die besagt, dass das Überwachungsprotokoll vorbereitet wird, und dass Sie eine Suche nach Abschluss der Vorbereitung in wenigen Stunden ausführen können.</span><span class="sxs-lookup"><span data-stu-id="8f484-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="8f484-133">Verwenden von PowerShell zum Aktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="8f484-133">Use PowerShell to turn on audit log search</span></span>

1. <span data-ttu-id="8f484-134">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="8f484-134">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="8f484-135">Führen Sie den folgenden PowerShell-Befehl aus, um die Suche in Office 365 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f484-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="8f484-136">Es wird eine Meldung angezeigt, dass es möglicherweise bis zu 60 Minuten dauert, bis die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="8f484-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="8f484-137">Deaktivieren der Überwachungsprotokoll Suche</span><span class="sxs-lookup"><span data-stu-id="8f484-137">Turn off audit log search</span></span>

<span data-ttu-id="8f484-p107">Sie müssen die mit Ihrer Exchange Online-Organisation verbundene Remote-PowerShell verwenden, um die Überwachungsprotokoll Suche zu deaktivieren. Ähnlich wie beim Aktivieren der Überwachungsprotokoll Suche muss Ihnen die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen werden, um die Suche nach Überwachungsprotokollen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f484-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. <span data-ttu-id="8f484-140">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).</span><span class="sxs-lookup"><span data-stu-id="8f484-140">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)</span></span>
    
2. <span data-ttu-id="8f484-141">Führen Sie den folgenden PowerShell-Befehl aus, um die Suche in Office 365 zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f484-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="8f484-p108">Stellen Sie nach einer Weile sicher, dass die Überwachungsprotokoll Suche deaktiviert ist. Hierzu gibt es zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="8f484-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="8f484-144">Führen Sie in PowerShell den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="8f484-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="8f484-145">Der Wert der `False` für die _UnifiedAuditLogIngestionEnabled_ -Eigenschaft gibt an, dass die Überwachungsprotokoll Suche deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8f484-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="8f484-146">Wechseln Sie im &amp; Security Compliance Center zur Such \*\* &amp; Untersuchung\*\* \> - **Überwachungsprotokoll**Suche, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="8f484-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="8f484-147">Es wird eine Meldung angezeigt, die besagt, dass die Überwachungsprotokoll Suche nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8f484-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Eine Nachricht wird nicht bezahlt, wenn die Überwachung deaktiviert ist.](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)

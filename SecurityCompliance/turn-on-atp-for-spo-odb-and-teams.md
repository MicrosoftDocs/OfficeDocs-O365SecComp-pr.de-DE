---
title: Aktivieren Sie Office 365 ATP für SharePoint, OneDrive und Microsoft-Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Informationen Sie zum Aktivieren der ATP für SharePoint, OneDrive und Teams, einschließlich wie Warnungen für erkannten Dateien festgelegt.
ms.openlocfilehash: 770af7078166857bcb9784112710262b7de788bb
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014887"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="e6b7f-103">Aktivieren Sie Office 365 ATP für SharePoint, OneDrive und Microsoft-Teams</span><span class="sxs-lookup"><span data-stu-id="e6b7f-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="e6b7f-p101">[Office 365 ATP für SharePoint, OneDrive, und Microsoft-Teams,](atp-for-spo-odb-and-teams.md) wird verhindert, dass Ihre Organisation versehentliches schädliche Dateien freigeben. Wenn eine solche Datei erkannt wird, wird diese Datei blockiert, damit niemand öffnen, kopieren, verschieben oder freigeben, bis der Organisation Security Team Weitere Aktionen ausgeführt werden. Lesen Sie diesen Artikel zum Aktivieren der ATP für SharePoint, OneDrive und Teams, richten Sie Warnungen zur erkannten Dateien benachrichtigt werden, und die nächsten Schritte.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="e6b7f-107">Um die in diesem Artikel beschriebenen Aufgaben durchführen zu können, benötigen Sie die erforderlichen Berechtigungen zugewiesen in Office 365 und die Sicherheit &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-107">In order to perform the tasks described in this article, you must have the necessary permissions assigned in Office 365 and in the Security &amp; Compliance Center.</span></span>
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="e6b7f-108">Aktivieren von ATP für SharePoint, OneDrive und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e6b7f-108">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

 <span data-ttu-id="e6b7f-p102">**Vor Beginn dieses Verfahrens stellen Sie sicher, dass die überwachungsprotokollierung für Ihre Office 365-Umgebung bereits aktiviert ist**. Dies erfolgt normalerweise von einem Benutzer, der Rolle für Überwachungsprotokolle im Exchange Online zugewiesen hat. Weitere Informationen finden Sie unter [Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p102">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="e6b7f-112">Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com), und melden Sie sich mit Ihrem Konto arbeiten oder Schule.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-112">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="e6b7f-113">In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie im linken Navigationsbereich unter **Threat Management** **Policy** \> **Sichere Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-113">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="e6b7f-114">![In das Wertpapier &amp; Compliance Center, wählen Sie Threat Management \> Richtlinie](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="e6b7f-114">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="e6b7f-115">Aktivieren Sie das Kontrollkästchen Sie **auf ATP für SharePoint, OneDrive, und Microsoft-Teams**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-115">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="e6b7f-116">![Aktivieren Sie erweiterte Bedrohungsschutz für SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="e6b7f-116">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="e6b7f-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-117">Click **Save**.</span></span>
    
5. <span data-ttu-id="e6b7f-118">Überprüfen Sie (und gegebenenfalls bearbeiten Sie) [sichere Anlagen Richtlinien](set-up-atp-safe-attachments-policies.md) und [sichere Links Richtlinien](set-up-atp-safe-links-policies.md)Ihres Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-118">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="e6b7f-119">(Empfohlen) Führen Sie das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** als ein globaler Administrator oder eine SharePoint Online-Administrator mit dem **DisallowInfectedFileDownload** -Parameter auf *true*festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-119">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="e6b7f-p103">Festlegen des Parameters auf *true* Blöcke (mit Ausnahme von löschen) alle Aktionen für erkannt Dateien. Personen können nicht öffnen, verschieben, kopieren oder erkannte Dateien freigeben.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p103">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="e6b7f-p104">Wenn der Parameter auf *"false"* blockiert alle Aktionen mit Ausnahme von löschen und herunterladen. Personen können das Risiko übernehmen möchten, und Laden Sie eine gefundene Datei.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p104">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="e6b7f-124">Können Sie bis zu 30 Minuten, damit die Änderungen in allen Office 365-Rechenzentren verteilen.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-124">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="e6b7f-125">(Empfohlen) Fahren Sie fort, um Benachrichtigungen zu erkannten Dateien einrichten.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-125">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="e6b7f-126">Weitere Informationen zum Verwenden von PowerShell mit Office 365 finden Sie unter [Verwalten von Office 365 mit PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="e6b7f-126">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="e6b7f-127">Um erfahren Sie mehr über die Benutzeroberfläche, wenn eine Datei als böswilligen entdeckt wurde, finden Sie unter [was geschehen soll, wenn eine solche Datei in SharePoint Online, OneDrive, oder Microsoft-Teams gefunden wird](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="e6b7f-127">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="e6b7f-128">Einrichten von Benachrichtigungen für erkannten Dateien</span><span class="sxs-lookup"><span data-stu-id="e6b7f-128">Set up alerts for detected files</span></span>

<span data-ttu-id="e6b7f-129">Um die Benachrichtigung, wenn eine Datei in SharePoint Online, OneDrive for Business oder Microsoft-Teams, als bösartige angegeben wurde, können Sie eine Warnung einrichten.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-129">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="e6b7f-130">In der [Sicherheit in Office 365 &amp; Compliance Center](https://protection.office.com), wählen Sie **Warnungen** \> **Benachrichtigungen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-130">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="e6b7f-131">Wählen Sie **Neue Benachrichtigung Richtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-131">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="e6b7f-p105">Geben Sie einen Namen für die Benachrichtigung. Beispielsweise können Sie schädliche Dateien in Bibliotheken eingeben.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p105">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="e6b7f-p106">Geben Sie eine Beschreibung für die Benachrichtigung. Beispielsweise können Sie Administratoren benachrichtigt eingeben, wenn schädliche Dateien in SharePoint Online, OneDrive oder Microsoft-Teams, erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p106">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="e6b7f-136">Klicken Sie im Abschnitt **senden diese Warnung, wenn...** folgendermaßen Sie vor:</span><span class="sxs-lookup"><span data-stu-id="e6b7f-136">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="e6b7f-p107">a wählen Sie in der Liste der **Aktivitäten** , **erkannte Schadsoftware in Datei**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p107">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="e6b7f-p108">b. lassen Sie b. das Feld **Benutzer** leer.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-p108">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="e6b7f-141">Wählen Sie im Abschnitt **dieser Warnung... senden** eine oder mehrere globale Administratoren, Sicherheitsadministratoren oder Sicherheit Leser, die benachrichtigt werden soll, wenn eine solche Datei erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-141">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="e6b7f-142">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-142">Click **Save**.</span></span>
    
<span data-ttu-id="e6b7f-143">Weitere Informationen zu Benachrichtigungen finden Sie unter [Aktivität Benachrichtigungen erstellen, in die Office 365-Sicherheit &amp; Compliance Center](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="e6b7f-143">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="e6b7f-144">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e6b7f-144">Next steps</span></span>

1. [<span data-ttu-id="e6b7f-145">Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt</span><span class="sxs-lookup"><span data-stu-id="e6b7f-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="e6b7f-146">Verwalten von in Quarantäne verschobenen Nachrichten und Dateien als Administrator in Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b7f-146">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  


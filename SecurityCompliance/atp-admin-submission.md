---
title: Übermittlungen von Administratoren in Office 365 ATP
ms.author: brwilcox
author: briwilcox
manager: dansimp
ms.date: 07/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Hier erfahren Sie, wie Sie potenziell schädliche Nachrichten, URLs und Dateien an Microsoft übermitteln.
ms.openlocfilehash: 6f7ea63cae4d7cafb0d1386b29d99101d290ef30
ms.sourcegitcommit: 9e2df36b05a2c93ce2629a7a5eda8f44159d114d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "35632225"
---
# <a name="admin-submissions-in-office-365-atp"></a><span data-ttu-id="894fa-103">Übermittlungen von Administratoren in Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="894fa-103">Admin submissions in Office 365 ATP</span></span>

<span data-ttu-id="894fa-104">Administratoren können jetzt e-Mails senden, indem Sie die Datei-oder Netzwerknachrichten-ID, URLs und Dateien für die Überprüfung durch Microsoft in Office 365 verwenden.</span><span class="sxs-lookup"><span data-stu-id="894fa-104">Admins can now send emails by using file or network message ID, URLs, and files for scanning by Microsoft in Office 365.</span></span> <span data-ttu-id="894fa-105">Der Abschnitt aktualisierte Übermittlungen enthält weiterhin von Benutzern gemeldete Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="894fa-105">The updated submissions section still includes user reported messages.</span></span> 

<span data-ttu-id="894fa-106">Wenn Sie eine e-Mail übermitteln, erhalten Sie Informationen zu allen Richtlinien, die möglicherweise die eingehenden e-Mails in ihren Mandanten zugelassen haben, sowie über die Untersuchung von URLs und Anlagen in der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="894fa-106">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="894fa-107">Richtlinien, die möglicherweise eine e-Mail zugelassen haben, enthalten die Liste sicherer Absender eines einzelnen Benutzers sowie Richtlinien auf Mandantenebene wie ETR-Regeln.</span><span class="sxs-lookup"><span data-stu-id="894fa-107">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as ETR rules.</span></span> 


## <a name="how-to-submit-content"></a><span data-ttu-id="894fa-108">Vorgehensweise zum Übermitteln von Inhalten</span><span class="sxs-lookup"><span data-stu-id="894fa-108">How to submit content</span></span>

<span data-ttu-id="894fa-109">Um Inhalte an Microsoft zu übermitteln, klicken Sie auf die Schaltfläche **neue Übermittlung** in der linken oberen Ecke der Seite Übermittlungen.</span><span class="sxs-lookup"><span data-stu-id="894fa-109">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="894fa-110">Ein Flyout auf der rechten Seite der Seite wird mit der Option zum Senden einer e-Mail, einer URL oder einer Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="894fa-110">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span> 

### <a name="email"></a><span data-ttu-id="894fa-111">E-Mail</span><span class="sxs-lookup"><span data-stu-id="894fa-111">Email</span></span>
![Beispiel für eine e-Mail-Übermittlung](media/submission-flyout-email.PNG)
1. <span data-ttu-id="894fa-113">Um eine e-Mail zu senden, wählen Sie **e-Mail** und geben Sie die e-Mail- **Netzwerknachrichten-ID** an, oder laden Sie die e-Mail-Datei</span><span class="sxs-lookup"><span data-stu-id="894fa-113">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span> 

2. <span data-ttu-id="894fa-114">Geben Sie die Empfänger an, für die Sie die Richtlinienüberprüfung ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="894fa-114">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="894fa-115">Durch die Richtlinienüberprüfung wird ermittelt, ob die e-Mail-Überprüfung aufgrund von Richtlinien auf Benutzer-oder Mandantenebene umgangen wurde.</span><span class="sxs-lookup"><span data-stu-id="894fa-115">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span> 

3. <span data-ttu-id="894fa-116">Geben Sie an, ob die e-Mail-Nachricht blockiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="894fa-116">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="894fa-117">Wenn die e-Mail blockiert wurde, geben Sie an, ob Sie als Spam, Phishing oder Schadsoftware blockiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="894fa-117">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="894fa-118">Wenn Sie nicht sicher sind, welche Art Sie haben könnten, verwenden Sie Ihr Bestes Urteil.</span><span class="sxs-lookup"><span data-stu-id="894fa-118">If you are not sure what type it might be, use your best judgement.</span></span>  

* <span data-ttu-id="894fa-119">Wenn der Filter aufgrund von Richtlinien bei der Übermittlung umgangen wurde, werden Informationen zu dieser Richtlinie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="894fa-119">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

* <span data-ttu-id="894fa-120">Wenn der Filter aufgrund einer oder mehrerer Richtlinien nicht umgangen wurde, wird die Überprüfung in einigen Minuten abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="894fa-120">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="894fa-121">Sie erhalten zusätzliche Informationen über die Übermittlung, indem Sie auf den Link Status klicken.</span><span class="sxs-lookup"><span data-stu-id="894fa-121">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="894fa-122">Dies beinhaltet die Ergebnisse der Richtlinienüberprüfung und das Ergebnis der erneuten Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="894fa-122">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="894fa-123">Hinweis Dadurch wird die e-Mail-Nachricht nicht über den Office 365 ATP-voll Filter Stapel erneut ausgeführt, es wird jedoch ein partieller erneuter Scan auf der Grundlage bestimmter Attribute der e-Mail, der URL oder der Datei ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="894fa-123">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span> 

4. <span data-ttu-id="894fa-124">Klicken Sie \*\*\*\* auf die Schaltfläche Absenden.</span><span class="sxs-lookup"><span data-stu-id="894fa-124">Click the **Submit** button.</span></span>

### <a name="url"></a><span data-ttu-id="894fa-125">URL</span><span class="sxs-lookup"><span data-stu-id="894fa-125">URL</span></span>
![Beispiel für eine e-Mail-Übermittlung](media/submission-url-flyout.png)
1. <span data-ttu-id="894fa-127">So übermitteln Sie eine URL wählen Sie **URL** aus dem Flyout aus.</span><span class="sxs-lookup"><span data-stu-id="894fa-127">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="894fa-128">Geben Sie die vollständige URL einschließlich des Protokolls (**https://**) ein.</span><span class="sxs-lookup"><span data-stu-id="894fa-128">Type in the full URL including the protocol (**https://**).</span></span> 

* <span data-ttu-id="894fa-129">Wenn Sie die Option **gefiltert haben ausgewählt haben**, geben Sie an, ob die URL Phishing oder Schadsoftware ist.</span><span class="sxs-lookup"><span data-stu-id="894fa-129">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="894fa-130">Klicken Sie \*\*\*\* auf die Schaltfläche Absenden.</span><span class="sxs-lookup"><span data-stu-id="894fa-130">Click the **Submit** button.</span></span> 


### <a name="file"></a><span data-ttu-id="894fa-131">Datei</span><span class="sxs-lookup"><span data-stu-id="894fa-131">File</span></span>
![Beispiel für eine e-Mail-Übermittlung](media/submission-file-flyout.PNG)
1. <span data-ttu-id="894fa-133">Um eine Datei zu übermitteln, wählen Sie **Datei** aus dem Flyout aus, und laden Sie die Datei hoch, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="894fa-133">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span> 

2. <span data-ttu-id="894fa-134">Klicken Sie \*\*\*\* auf die Schaltfläche Absenden.</span><span class="sxs-lookup"><span data-stu-id="894fa-134">Click the **Submit** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="894fa-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="894fa-135">Related topics</span></span>

[<span data-ttu-id="894fa-136">Office 365 Advanced Threat Protection-Plan 2</span><span class="sxs-lookup"><span data-stu-id="894fa-136">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="894fa-137">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="894fa-137">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="894fa-138">Anzeigen von Berichten für Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="894fa-138">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  


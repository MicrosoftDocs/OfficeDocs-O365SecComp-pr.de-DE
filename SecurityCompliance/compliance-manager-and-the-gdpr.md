---
title: Microsoft Compliance-Manager und die DSGVO
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: 10579edea5a36686b8b19cafd9d3d6e148cfdcd3
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473092"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="4d8b1-104">Microsoft Compliance-Manager und die DSGVO</span><span class="sxs-lookup"><span data-stu-id="4d8b1-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="4d8b1-105">Die allgemeine Datenschutzverordnung (DSGVO), die von der Europäischen Union verabschiedet wurde, kann sich auf Ihre Compliance-Strategie auswirken und die erforderlichen Aktionen zur Verwaltung von Benutzer-und Kundeninformationen im Compliance-Manager ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate actions needed to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="4d8b1-106">Datenschutzeinstellungen</span><span class="sxs-lookup"><span data-stu-id="4d8b1-106">User Privacy settings</span></span>

<span data-ttu-id="4d8b1-107">Bestimmte Bestimmungen erfordern, dass eine Organisation Benutzer Verlaufsdaten löschen kann.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="4d8b1-108">Compliance-Manager bietet Funktionen für die **Datenschutzeinstellungen des Benutzers** , mit denen Administratoren folgende Aufgaben erfüllen können:</span><span class="sxs-lookup"><span data-stu-id="4d8b1-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="4d8b1-109">Suchen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="4d8b1-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="4d8b1-110">Exportieren eines Berichts mit Kontoverlaufsdaten</span><span class="sxs-lookup"><span data-stu-id="4d8b1-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="4d8b1-111">Löschen der Verlaufsdaten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="4d8b1-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="4d8b1-112">Suchen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="4d8b1-112">Search for a user</span></span>

<span data-ttu-id="4d8b1-113">So suchen Sie nach einem Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="4d8b1-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="4d8b1-114">Geben Sie den Benutzer-e-Mail-Alias (die Informationen links vom @-Symbol) ein, und wählen Sie den Domänennamen aus der Liste Domänensuffix auf der rechten Seite aus.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="4d8b1-115">Für Organisationen mit mehreren registrierten Domänen müssen Sie das Domänennamensuffix überprüfen, um sicherzustellen, dass es korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="4d8b1-116">Wenn Sie den Benutzernamen richtig eingegeben haben, wählen Sie **Suchen**aus.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="4d8b1-117">Für Benutzerkonten, die nicht zurückgegeben werden, wird "Benutzer nicht gefunden" auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-117">For user accounts not returned, 'User not found' is displayed on the page.</span></span> <span data-ttu-id="4d8b1-118">Überprüfen Sie die e-Mail-Adressinformationen des Benutzers, und nehmen Sie Korrekturen vor.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="4d8b1-119">Zum Wiederholen wählen Sie **Suchen**aus.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="4d8b1-120">Für Benutzerkonten wird der Text der Schaltfläche von der **Suche** in **Clear**geändert.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="4d8b1-121">Dies gibt an, dass das zurückgegebene Benutzerkonto der Betriebs Kontext für die zusätzlichen Funktionen ist und diese Funktionen für dieses Benutzerkonto gelten.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="4d8b1-122">Wählen Sie **Löschen**aus, um die Suchergebnisse zu löschen und nach einem anderen Benutzer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="4d8b1-123">Exportieren eines Berichts mit Kontoverlaufsdaten</span><span class="sxs-lookup"><span data-stu-id="4d8b1-123">Export a report of account data history</span></span>

<span data-ttu-id="4d8b1-124">Für jedes identifizierte Benutzerkonto können Sie einen Bericht über Abhängigkeiten generieren, die mit diesem Konto verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-124">For each user account identified, you can generate a report of dependencies linked to this account.</span></span> <span data-ttu-id="4d8b1-125">Mit diesen Informationen können Sie geöffnete Aktionselemente erneut zuweisen oder den Zugriff auf zuvor hochgeladene Nachweise sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="4d8b1-126">So generieren und exportieren Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="4d8b1-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="4d8b1-127">Wählen Sie **exportieren** aus, um einen Bericht über die aktuell dem zurückgegebenen Benutzerkonto zugewiesenen Compliance Manager-Steuerelement Aktionen und die Liste der von diesem Benutzer hochgeladenen Dokumente zu generieren und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="4d8b1-128">Wenn keine zugeordneten Aktionen oder hochgeladenen Dokumente vorhanden sind, gibt eine Fehlermeldung "keine Daten für diesen Benutzer" an.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="4d8b1-129">Der Bericht wird im Hintergrund des aktiven Browserfensters heruntergeladen, wenn ein Download-Popup nicht angezeigt wird, das Sie in Ihrem Browser-Downloadverlauf überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="4d8b1-130">Öffnen Sie das Dokument, um die Daten des Berichts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d8b1-131">Hierbei handelt es sich nicht um einen Verlaufsbericht, der Statusänderungen am Zuordnungs Verlauf für die Aktionselemente beibehält und anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-131">This is not a historical report that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="4d8b1-132">Der generierte Bericht ist eine Momentaufnahme der Steuerelement-Aktionselemente, die zum Zeitpunkt der Ausführung des Berichts zugewiesen wurden (Datums-und Zeitstempel in den Bericht).</span><span class="sxs-lookup"><span data-stu-id="4d8b1-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="4d8b1-133">Eine spätere erneute Zuweisung von Aktionselementen führt beispielsweise zu unterschiedlichen Snapshotbericht-Daten, wenn dieser Bericht erneut für denselben Benutzer generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if this report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="4d8b1-134">Löschen der Verlaufsdaten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="4d8b1-134">Delete user data history</span></span>

<span data-ttu-id="4d8b1-135">Legt alle Steuerelement-Aktionselemente fest, die dem zurückgegebenen Benutzer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="4d8b1-136">Legt den **hoch** geladenen Wert für alle Dokumente fest, die der zurückgegebene Benutzer an ' Benutzer entfernt ' hochgeladen hat.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="4d8b1-137">So löschen Sie das Aktionselement und den Dokumentupload-Verlauf des Benutzerkontos:</span><span class="sxs-lookup"><span data-stu-id="4d8b1-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="4d8b1-138">Wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-138">Select **Delete**.</span></span>

    <span data-ttu-id="4d8b1-139">Ein Bestätigungsdialogfeld wird angezeigt, "*dadurch werden alle Aufgaben des Steuerelement-Aktionselements und der Dokumentupload-Verlauf für den ausgewählten Benutzer entfernt. Diese Aktion ist dauerhaft. Sind Sie sicher, dass Sie den Vorgang fortsetzen möchten?*"</span><span class="sxs-lookup"><span data-stu-id="4d8b1-139">A confirmation dialog is displayed, "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="4d8b1-140">Um fortzufahren, wählen Sie **OK**aus, andernfalls wählen Sie **Abbrechen**aus.</span><span class="sxs-lookup"><span data-stu-id="4d8b1-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
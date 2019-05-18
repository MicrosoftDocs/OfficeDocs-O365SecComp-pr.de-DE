---
title: Microsoft Compliance Manager und die dsgvo
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Der Microsoft Compliance-Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft-Dienst Vertrauensstellungs Portal. Mit dem Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: a082d069aced13aa9260a1a856d942c4feb7dd4b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152094"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="cf93d-104">Microsoft Compliance Manager und die dsgvo</span><span class="sxs-lookup"><span data-stu-id="cf93d-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="cf93d-105">Die allgemeine Datenschutzverordnung (dsgvo), die von der Europäischen Union erlassen wird, kann sich auf Ihre Compliance-Strategie auswirken und die erforderlichen Aktionen zum Verwalten von Benutzer-und Kundeninformationen im Compliance-Manager betreffen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate actions needed to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="cf93d-106">Datenschutzeinstellungen</span><span class="sxs-lookup"><span data-stu-id="cf93d-106">User Privacy settings</span></span>

<span data-ttu-id="cf93d-107">Für bestimmte Richtlinien ist es erforderlich, dass eine Organisation Benutzer Verlaufsdaten löschen kann.</span><span class="sxs-lookup"><span data-stu-id="cf93d-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="cf93d-108">Compliance-Manager bietet Funktionen für **Benutzerdaten Schutzeinstellungen** , die Administratoren Folgendes ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="cf93d-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="cf93d-109">Suchen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="cf93d-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="cf93d-110">Exportieren eines Berichts mit Kontoverlaufsdaten</span><span class="sxs-lookup"><span data-stu-id="cf93d-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="cf93d-111">Löschen der Verlaufsdaten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="cf93d-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="cf93d-112">Suchen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="cf93d-112">Search for a user</span></span>

<span data-ttu-id="cf93d-113">So suchen Sie nach einem Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="cf93d-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="cf93d-114">Geben Sie den Benutzer-e-Mail-Alias (die Informationen links neben dem @-Symbol) ein, und wählen Sie den Domänennamen aus der Liste Domänensuffix auf der rechten Seite aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="cf93d-115">Für Organisationen mit mehreren registrierten Domänen überprüfen Sie das Domänennamensuffix doppelt, um sicherzustellen, dass es richtig ist.</span><span class="sxs-lookup"><span data-stu-id="cf93d-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="cf93d-116">Wenn Sie den Benutzernamen richtig eingegeben haben, wählen Sie **Suchen**aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="cf93d-117">Für Benutzerkonten, die nicht zurückgegeben werden, wird auf der Seite "Benutzer nicht gefunden" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-117">For user accounts not returned, 'User not found' is displayed on the page.</span></span> <span data-ttu-id="cf93d-118">Überprüfen Sie die e-Mail-Adressinformationen des Benutzers, und nehmen Sie bei Bedarf Korrekturen vor.</span><span class="sxs-lookup"><span data-stu-id="cf93d-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="cf93d-119">Zum Wiederholen wählen Sie **Suchen**aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="cf93d-120">Für Benutzerkonten, die zurückgegeben werden, ändert sich der Text der Schaltfläche von **Suche** zu **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="cf93d-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="cf93d-121">Dies deutet darauf hin, dass das zurückgegebene Benutzerkonto der Betriebs Kontext für die zusätzlichen Funktionen ist und dass diese Funktionen für dieses Benutzerkonto gelten.</span><span class="sxs-lookup"><span data-stu-id="cf93d-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="cf93d-122">Um Suchergebnisse zu löschen und nach einem anderen Benutzer zu suchen, wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="cf93d-123">Exportieren eines Berichts mit Kontoverlaufsdaten</span><span class="sxs-lookup"><span data-stu-id="cf93d-123">Export a report of account data history</span></span>

<span data-ttu-id="cf93d-124">Sie können für jedes identifizierte Benutzerkonto einen Bericht über Abhängigkeiten generieren, die mit diesem Konto verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cf93d-124">For each user account identified, you can generate a report of dependencies linked to this account.</span></span> <span data-ttu-id="cf93d-125">Mit diesen Informationen können Sie offene Aktionselemente neu zuweisen oder den Zugriff auf zuvor hochgeladene Beweise sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="cf93d-126">So generieren und exportieren Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="cf93d-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="cf93d-127">Wählen Sie **exportieren** aus, um einen Bericht der Compliance-Manager-Steuerelement Aktionselemente zu generieren und herunterzuladen, die dem zurückgegebenen Benutzerkonto derzeit zugewiesen sind, und die Liste der Dokumente, die von diesem Benutzer hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="cf93d-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="cf93d-128">Wenn keine Aktionen oder hochgeladenen Dokumente zugeordnet sind, wird in einer Fehlermeldung "keine Daten für diesen Benutzer" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="cf93d-129">Der Bericht lädt im Hintergrund des aktiven Browserfensters herunter – wenn kein Popup zum Herunterladen angezeigt wird, in dem Sie den Downloadverlauf Ihres Browsers überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="cf93d-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="cf93d-130">Öffnen Sie das Dokument, um die Daten des Berichts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf93d-131">Hierbei handelt es sich nicht um einen Verlaufsbericht, der Statusänderungen an Aktionselement-Zuordnungs Verlauf aufrecht erhalten und anzeigt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-131">This is not a historical report that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="cf93d-132">Der generierte Bericht ist eine Momentaufnahme der Steuerungs Aktionselemente, die zum Zeitpunkt der Ausführung des Berichts zugewiesen wurden (Datum und Zeitstempel in den Bericht).</span><span class="sxs-lookup"><span data-stu-id="cf93d-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="cf93d-133">Beispielsweise ergeben alle nachfolgenden Neuzuweisungen von Aktionselementen unterschiedliche Momentaufnahme Berichtsdaten, wenn dieser Bericht für denselben Benutzer erneut generiert wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if this report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="cf93d-134">Löschen der Verlaufsdaten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="cf93d-134">Delete user data history</span></span>

<span data-ttu-id="cf93d-135">Legt alle dem zurückgegebenen Benutzer zugewiesenen Steuerungs Aktionselemente auf "nicht zugewiesen" fest.</span><span class="sxs-lookup"><span data-stu-id="cf93d-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="cf93d-136">Legt den Wert für **hoch** geladene nach Werte für alle Dokumente fest, die vom zurückgegebenen Benutzer auf "Benutzer entfernt" hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="cf93d-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="cf93d-137">So löschen Sie das Benutzerkonto-Aktionselement und den Dokumentupload-Verlauf:</span><span class="sxs-lookup"><span data-stu-id="cf93d-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="cf93d-138">Wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-138">Select **Delete**.</span></span>

    <span data-ttu-id="cf93d-139">Es wird ein Bestätigungsdialogfeld angezeigt, "*dadurch werden alle Aktionselement Zuweisungen des Steuerelements und der Verlauf des dokumentuploads für den ausgewählten Benutzer entfernt. Diese Aktion ist dauerhaft. Möchten Sie wirklich fortfahren?*"</span><span class="sxs-lookup"><span data-stu-id="cf93d-139">A confirmation dialog is displayed, "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="cf93d-140">Um fortzufahren, wählen Sie **OK**, andernfalls **Abbrechen**aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
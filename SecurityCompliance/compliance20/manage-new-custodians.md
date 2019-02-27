---
title: Verwalten von Verwaltern in einem erweiterten eDiscovery-Fall (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 95a1bcbbc279ad4e476fc479e701b0f8a921c83b
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295678"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="00dad-102">Verwalten von Verwaltern in einem erweiterten eDiscovery-Fall (Preview)</span><span class="sxs-lookup"><span data-stu-id="00dad-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="00dad-p101">Die Registerkarte Depotbanken enthält eine sortierbare Liste aller Verwalter in dem Fall. Nachdem Sie einem Fall Verwalter hinzugefügt haben, werden die Details zu den einzelnen Depotbanken automatisch aus Azure Active Directory gesammelt.</span><span class="sxs-lookup"><span data-stu-id="00dad-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="00dad-105">Anzeigen von Depot Details</span><span class="sxs-lookup"><span data-stu-id="00dad-105">Viewing custodian details</span></span>

<span data-ttu-id="00dad-p102">Die Flyout-Seite mit Depot Details wird angezeigt, nachdem Sie einen Verwalter zu einem Fall hinzugefügt haben, und wählen Sie ihn in der Liste auf der Registerkarte **Verwalter** aus. Von hier aus können Sie alle Details zu diesem Verwalter anzeigen. Die Flyout-Seite enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="00dad-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="00dad-108">Kontaktinformationen</span><span class="sxs-lookup"><span data-stu-id="00dad-108">Contact information</span></span>

  - <span data-ttu-id="00dad-p103">**Anzeigename**: der Name, der im Adressbuch für die Depotbank angezeigt wird. Dies ist normalerweise die Kombination aus Vornamen, mittlerem und Nachnamen.</span><span class="sxs-lookup"><span data-stu-id="00dad-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="00dad-111">**Mail/SMTP**: die SMTP-Adresse für die Depotbank, beispielsweise Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="00dad-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="00dad-112">**Title**: die Position des Depotbank-Titels.</span><span class="sxs-lookup"><span data-stu-id="00dad-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="00dad-113">**Abteilung**: der Name der Abteilung, in der die Depotbank arbeitet.</span><span class="sxs-lookup"><span data-stu-id="00dad-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="00dad-p104">**Manager**: Manager der Depotbank. Der designierte Vorgesetzte erhält eine Eskalations Kommunikation für diesen Verwalter.</span><span class="sxs-lookup"><span data-stu-id="00dad-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="00dad-116">Standortinformationen</span><span class="sxs-lookup"><span data-stu-id="00dad-116">Location information</span></span>

  - <span data-ttu-id="00dad-117">**Ort**: die Stadt, in der sich die Depotbank befindet.</span><span class="sxs-lookup"><span data-stu-id="00dad-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="00dad-118">**Bundes**Land: Bundesland oder Kanton in der Depotbank-Adresse.</span><span class="sxs-lookup"><span data-stu-id="00dad-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="00dad-119">**Land/Region**: das Land/die Region, in der sich die Depotbank befindet; zum Beispiel "US" oder "UK".</span><span class="sxs-lookup"><span data-stu-id="00dad-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="00dad-120">**Office**: der Bürostandort im Geschäftssitz des Depotbank.</span><span class="sxs-lookup"><span data-stu-id="00dad-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="00dad-121">Fall Informationen</span><span class="sxs-lookup"><span data-stu-id="00dad-121">Case information</span></span>

  - <span data-ttu-id="00dad-122">**Status halten**: gibt an, ob die Depotbank in der Warteschleife gehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="00dad-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="00dad-p105">**Kommunikationsstatus**: gibt an, ob der Depotbank eine Hold-Benachrichtigung ausgegeben wurde. Wenn der Depotbank eine Benachrichtigung ausgegeben wurde, wird diese als *veröffentlicht*gekennzeichnet. Wenn der Depotbank nicht eine Benachrichtigung ausgegeben wurde, wird dieser Status nicht *veröffentlicht*.</span><span class="sxs-lookup"><span data-stu-id="00dad-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="00dad-p106">**Status**: der Status der Depotbank innerhalb des Falls. Dies ist *aktiv* , wenn die Depotbank noch für den Fall in der Warteschleife ist. Wenn ein Depot aus einem Fall entfernt wird, wird der Status in *veröffentlicht*geändert.</span><span class="sxs-lookup"><span data-stu-id="00dad-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="00dad-129">Verarbeitungsstatus</span><span class="sxs-lookup"><span data-stu-id="00dad-129">Processing status</span></span>

  - <span data-ttu-id="00dad-130">**Indizierungsstatus**: gibt den Status des Deep Indexing-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="00dad-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="00dad-131">**IndexIng Last updated Time**: gibt den DATESTAMP an, in dem der Deep Indexing-Auftrag zuletzt ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="00dad-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="00dad-132">**Datenquellen**: zeigt die Anzahl von Postfächern, Websites und Teams an, die für die Depotbank ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="00dad-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="00dad-133">Aktualisieren einer Depotbank</span><span class="sxs-lookup"><span data-stu-id="00dad-133">Updating a custodian</span></span>

<span data-ttu-id="00dad-p107">Wenn Ihr Fall fortgeschritten ist, können Sie feststellen, dass möglicherweise zusätzliche Datenquellen relevant für eine bestimmte Depotbank & Ihrem Fall. In anderen Szenarien möchten Sie möglicherweise bestimmte Datenquellen entfernen, die überprüft und als nicht relevant eingestuft wurden.</span><span class="sxs-lookup"><span data-stu-id="00dad-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="00dad-136">So aktualisieren Sie einen Depotbank und die ausgewählten Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="00dad-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="00dad-137">Wählen Sie einen vorhandenen Fall aus der **eDiscovery-_GT_ Advanced eDiscovery (Preview)** aus.</span><span class="sxs-lookup"><span data-stu-id="00dad-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="00dad-138">Klicken Sie in dem Fall auf die Registerkarte **depotverwalter** .</span><span class="sxs-lookup"><span data-stu-id="00dad-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="00dad-139">Wählen Sie die Verwalter aus der Liste aus, und klicken Sie auf **Quellen bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="00dad-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="00dad-140">Aktualisieren Sie die Auswahl für Exchange-und OneDrive-Speicherorte, indem **Sie auf Datenquellen auswählen**klicken.</span><span class="sxs-lookup"><span data-stu-id="00dad-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="00dad-p108">Hinzufügen oder Entfernen von Teams, SharePoint oder Exchange-Postfächern der Benutzer wird durch Klicken auf **zusätzliche Datenquellen**zugeordnet. Weitere Informationen dazu, wie Sie Datenquellen einem depotverwalter zuordnen, finden Sie unter Hinzufügen von Bewahrern [zu einem Fall](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="00dad-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="00dad-143">Um den Status der Depotbank zu aktualisieren, \*\*\*\* klicken Sie auf Depot Aufbewahrung und aktivieren oder deaktivieren Sie die Aufbewahrung für Verwalter.</span><span class="sxs-lookup"><span data-stu-id="00dad-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="00dad-144">Sie können mehrere Verwalter auswählen, um Massenaktionen durchzuführen, wie beispielsweise die erneute Indizierung, Freigabe oder Bearbeitung einer Reihe von Verwalter.</span><span class="sxs-lookup"><span data-stu-id="00dad-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="00dad-145">Beheben von Fehlern bei der Depot Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="00dad-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="00dad-p109">In den meisten legalen Workflows wird eine Teilmenge der Benutzerdaten durchsucht, nachdem Verwalter für eine bestimmte Untersuchung hinzugefügt wurden. Aufgrund von großen Dateigrößen oder möglicher Beschädigung können einige Elemente innerhalb der Datenquellen der Depotbank teilweise indiziert werden. Mithilfe der erweiterten eDiscovery (Preview) Deep Indexing-Funktion können diese teilweise indizierten Elemente durch erneutes Crawlen und Erneutes Indizieren dieser Elemente bei Bedarf automatisch wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="00dad-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="00dad-p110">Wenn einem Fall eine Depotbank hinzugefügt wird, werden Ihre Daten automatisch "tief indiziert", sodass Benutzer diese teilweise indizierten Elemente beibehalten können, anstatt Suchvorgänge außerhalb von Office 365 herunterzuladen, zu beheben und erneut auszuführen. Während des Lebenszyklus eines Falls kann ein Benutzer Elemente korrigieren oder neue Datenquellen für eine bestimmte Depotbank hinzufügen. Möglicherweise muss der Depotbank-Index aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="00dad-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="00dad-152">So lösen Sie einen erneuten Indizierungsprozess für teilweise indizierte Elemente aus:</span><span class="sxs-lookup"><span data-stu-id="00dad-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="00dad-153">Wechseln Sie zu **eDiscovery _GT_ Advanced eDiscovery (Preview)** , und wählen Sie einen vorhandenen Fall aus.</span><span class="sxs-lookup"><span data-stu-id="00dad-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="00dad-154">Klicken Sie in diesem Fall auf die **Registerkarte depotverwalter**.</span><span class="sxs-lookup"><span data-stu-id="00dad-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="00dad-155">Wählen Sie die Depotbanken aus, die erneut indiziert werden müssen, und klicken Sie dann auf der Seite Flyout auf **Index aktualisieren** .</span><span class="sxs-lookup"><span data-stu-id="00dad-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="00dad-156">Überprüfen Sie den Status des Depot Indexes, indem Sie auf der Registerkarte **Depotbanken** auf den Link in der Spalte **Status des Indizierungs Auftrags** klicken.</span><span class="sxs-lookup"><span data-stu-id="00dad-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="00dad-157">Der Status für den erneuten Indizierungsprozess kann auch auf der Registerkarte **Aufträge** nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="00dad-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="00dad-158">Weitere Informationen zum erneuten indizieren und korrigieren von teilweise indizierten Elementen finden Sie unter [Beheben von Verarbeitungsfehlern](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="00dad-158">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="00dad-159">Freigeben eines Depotbank aus einem Fall</span><span class="sxs-lookup"><span data-stu-id="00dad-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="00dad-160">Eine Depotbank wird in Situationen freigegeben, in denen ein Fall geschlossen ist, eine Depotbank nicht mehr zur Aufbewahrung von Inhalten für einen Fall verpflichtet ist oder wenn eine Depotbank als nicht mehr relevant für einen bestimmten Fall erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="00dad-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="00dad-p111">Wenn Sie einen Verwalter freigeben, nachdem ein Aufbewahrungs Hinweis veröffentlicht wurde, wird eine Veröffentlichungs Benachrichtigung an die Depotbank gesendet. Darüber hinaus werden alle Depotinhaber, die den freigegebenen depotbanks zugeordnet sind, ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="00dad-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="00dad-163">Wenn die Depotbank in einem Stillstand gehalten wurde, in dem Sie keine zugelassenen Haltestatus Benachrichtigungen ausgegeben haben, werden alle Freiheitsentzug, die den freigegebenen Verwaltern zugeordnet sind, entfernt.</span><span class="sxs-lookup"><span data-stu-id="00dad-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="00dad-164">So geben Sie eine Depotbank frei</span><span class="sxs-lookup"><span data-stu-id="00dad-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="00dad-165">Wechseln Sie zur Registerkarte **depotverwalter** .</span><span class="sxs-lookup"><span data-stu-id="00dad-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="00dad-166">Wählen Sie den Verwalter aus der Liste aus, und klicken Sie auf der Seite Flyout auf **Freigabe Verwalter** .</span><span class="sxs-lookup"><span data-stu-id="00dad-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="00dad-167">Der Status der Depotbank auf der Register \*\*\*\* Karte depotbanks ist auf **Released** festgelegt, und der **Haltestatus** auf der Flyout-Seite wird in **inaktiv**geändert.</span><span class="sxs-lookup"><span data-stu-id="00dad-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="00dad-p112">Eine Depotbank kann an mehreren rechtlichen Aufbewahrungs Fragen beteiligt sein. Wenn ein Depot aus einem Fall entlassen wird, werden die Aufbewahrungs-und Benachrichtigungen in anderen Angelegenheiten nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="00dad-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="00dad-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00dad-170">Related information</span></span>

 - [<span data-ttu-id="00dad-171">Beheben von Fehlern beim Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="00dad-171">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="00dad-172">Arbeiten mit Kommunikation</span><span class="sxs-lookup"><span data-stu-id="00dad-172">Work with communications</span></span>](managing-custodian-communications.md)

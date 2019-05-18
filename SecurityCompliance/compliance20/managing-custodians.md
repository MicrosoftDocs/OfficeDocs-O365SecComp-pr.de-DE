---
title: Arbeiten mit Verwaltern in Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Mit dem Verwalter Verwaltungstool in Advanced eDiscovery können Sie den Workflow verwalten, um Daten zu identifizieren, zu erhalten und zu sammeln, die den Interessen Personen in einem Rechtsfall zugeordnet sind.
ms.openlocfilehash: 6e365f0b7f80a0a5caa050b2e0b08c94dbed4746
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151597"
---
# <a name="work-with-custodians-in-advanced-ediscovery"></a><span data-ttu-id="e4534-103">Arbeiten mit Verwaltern in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e4534-103">Work with custodians in Advanced eDiscovery</span></span>

<span data-ttu-id="e4534-104">Wenn eine Organisation auf eine rechtliche Untersuchung reagiert, basiert der Workflow rund um das identifizieren, beibehalten und erfassen potenziell relevanter Inhalte auf den Personen in der Organisation, die die Verwalter relevanter Daten sind.</span><span class="sxs-lookup"><span data-stu-id="e4534-104">When an organization responds to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based on the people in the organization who are the custodians of relevant data.</span></span> <span data-ttu-id="e4534-105">In eDiscovery werden diese Personen als *Datenverwalter* (oder nur *Verwalter*) bezeichnet und als "Personen mit administrativer Kontrolle über ein Dokument oder eine elektronische Datei" definiert.</span><span class="sxs-lookup"><span data-stu-id="e4534-105">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file".</span></span> <span data-ttu-id="e4534-106">Beispielsweise kann der Verwalter einer e-Mail-Nachricht der Besitzer des Postfachs sein, das die entsprechende Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="e4534-106">For example, the custodian of an email message could be the owner of the mailbox that contains the relevant message.</span></span>  

<span data-ttu-id="e4534-107">Wenn eine Untersuchung beginnt, muss das eDiscovery-Team schnell alle relevanten Verwalter und Datenquellen identifizieren, die sich auf den Fall beziehen.</span><span class="sxs-lookup"><span data-stu-id="e4534-107">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case.</span></span> <span data-ttu-id="e4534-108">Im Laufe der Zeit kann die Liste der Verwalter und ihrer Datenquellen zunehmen oder decreasse.</span><span class="sxs-lookup"><span data-stu-id="e4534-108">Over time, the list of custodians and their data sources may increase or decreasse.</span></span> <span data-ttu-id="e4534-109">Daher müssen Organisationen einen kontrollierten Prozess aufrecht erhalten, um den Aufbewahrungs Inhalt während des gesamten Lebenszyklus eines Falles zu identifizieren, zu erhalten und zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="e4534-109">As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the life cycle of a case.</span></span>

<span data-ttu-id="e4534-110">In einem erweiterten eDiscovery-Fall können Legal Teams Personen in Ihrer Organisation als Verwalter hinzufügen und automatisch Datenquellen wie Exchange-Postfächer, OneDrive-Konten und SharePoint-und Microsoft Teams-Websites identifizieren und beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e4534-110">In an Advanced eDiscovery case, legal teams can add individuals in their organization as custodians, and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="e4534-111">Mithilfe des integrierten Verwaltungstools in der erweiterten eDiscovery können Organisationen elektronisch gespeicherte Informationen vor versehentlicher (oder vorsätzlicher) Löschung schützen.</span><span class="sxs-lookup"><span data-stu-id="e4534-111">By using the built-in custodian management tool in Advanced eDiscovery, organizations can secure electronically stored information from inadvertent (or intentional) deletion.</span></span> <span data-ttu-id="e4534-112">Auf diese Weise können Sie den zeitaufwändigen und fehleranfälligen Prozess der manuellen Ausführung der legalen Aufbewahrungs Prozesse vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e4534-112">This lets you eliminate the time-consuming and error-prone process of manually having to perform the legal hold processes.</span></span> 

<span data-ttu-id="e4534-113">Weitere Informationen zum Arbeiten mit Depotbanken finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e4534-113">For more information about working with custodians, see the following:</span></span> 

- [<span data-ttu-id="e4534-114">Hinzufügen von Verwaltungsberechtigten zu einem Fall</span><span class="sxs-lookup"><span data-stu-id="e4534-114">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="e4534-115">Verwalten von Depotbanken in einem Fall</span><span class="sxs-lookup"><span data-stu-id="e4534-115">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="e4534-116">Anzeigen der Aktivitäten von Verwaltungsberechtigten</span><span class="sxs-lookup"><span data-stu-id="e4534-116">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="advanced-ediscovery-permissions"></a><span data-ttu-id="e4534-117">Erweiterte eDiscovery-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e4534-117">Advanced eDiscovery permissions</span></span>

<span data-ttu-id="e4534-118">In Advanced eDiscovery können Sie die integrierte eDiscovery-Manager-Rollengruppe verwenden, um juristischen Ermittlern die erforderlichen Berechtigungen zu erteilen, damit Sie den End-to-End-Workflow in Advanced eDiscovery verwalten können.</span><span class="sxs-lookup"><span data-stu-id="e4534-118">In Advanced eDiscovery, you can use the built-in eDiscovery Manager role group to assign the necessary permissions to legal investigators so they can manage the end-to-end workflow in Advanced eDiscovery.</span></span> <span data-ttu-id="e4534-119">Alternativ können Sie benutzerdefinierte Rollengruppen mit einer Teilmenge der Rollen erstellen, die zum Ausführen bestimmter Aktionen in einem Fall in Advanced eDiscovery erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e4534-119">Alternatively, you can create custom role groups with a subset of the roles necessary to perform certain actions in a case in Advanced eDiscovery.</span></span> <span data-ttu-id="e4534-120">Weitere Informationen zu eDiscovery-bezogenen Rollen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Security & Compliance Center](../assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e4534-120">For more information about eDiscovery-related roles, see [Assign eDiscovery permissions in the Security & Compliance Center](../assign-ediscovery-permissions.md).</span></span>

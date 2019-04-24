---
title: Versionshinweise zu Advanced eDiscovery (Preview)
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
description: Dieser Artikel enthält die Versionshinweise zu Advanced eDiscovery (Preview).
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240940"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a><span data-ttu-id="b2a44-103">Versionshinweise zu Advanced eDiscovery (Preview)</span><span class="sxs-lookup"><span data-stu-id="b2a44-103">Release notes for Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="b2a44-104">Das öffentliche Vorschauprogramm für Advanced eDiscovery ist die Möglichkeit, frühzeitig Zugriff auf die bevorstehenden Funktionen und Updates zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2a44-104">The Public Preview program for Advanced eDiscovery is the way to get early access to the upcoming functionality and updates.</span></span> <span data-ttu-id="b2a44-105">Wenn Sie frühzeitig auf die neuesten Funktionen zugreifen möchten, erstellen Sie einfach einen Advanced eDiscovery (Preview)-Fall im Office 365 Security & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="b2a44-105">To get early access to the newest features, just create and use an Advanced eDiscovery (Preview) case in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="b2a44-106">Weitere Informationen finden Sie unter [Create a New Case](create-new-ediscovery-case.md).</span><span class="sxs-lookup"><span data-stu-id="b2a44-106">See [Create a new case](create-new-ediscovery-case.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="b2a44-107">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b2a44-107">Known issues</span></span>

<span data-ttu-id="b2a44-108">**Microsoft Forms**</span><span class="sxs-lookup"><span data-stu-id="b2a44-108">**Microsoft Forms**</span></span>

- <span data-ttu-id="b2a44-109">Die Daten, die einem Formular entsprechen, das vor dem 31. Januar 2019 erstellt wurde, können nicht durchsucht werden, wenn das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2a44-109">The data corresponding to a form created before January 31, 2019 will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="b2a44-110">Nach diesem Datum erstellte Formulare stehen für die Suche zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b2a44-110">Forms created after this date will be available to search.</span></span>

- <span data-ttu-id="b2a44-111">Ein von einem Benutzer erstelltes Formular kann weiterhin Antworten erhalten, auch wenn der Benutzer, der das Formular erstellt hat, gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b2a44-111">A form created by a user can still receive responses even after the user who created the Form is deleted.</span></span> <span data-ttu-id="b2a44-112">Die entsprechenden Daten für diese Antworten (die nach dem Löschen des Depotbank-Postfachs aufgetreten sind) können jedoch nicht durchsucht werden, wenn das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2a44-112">However, the corresponding data for those responses (that occurred after the custodian mailbox was deleted) will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span>
 
<span data-ttu-id="b2a44-113">**Microsoft Sway**</span><span class="sxs-lookup"><span data-stu-id="b2a44-113">**Microsoft Sway**</span></span>

- <span data-ttu-id="b2a44-114">Wenn ein Benutzer eine Sway unmittelbar vor dem Löschen des Benutzerkontos für den Besitzer dieser Sway bearbeitet, sind diese Änderungen möglicherweise nicht durchsuchbar, wenn Sie das Such Tool in Advanced eDiscovery (Preview) zum Durchsuchen von Depot Postfächern verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2a44-114">If a user edits a sway just prior to the deletion of the user account for the owner of that sway, then those changes may not be be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="b2a44-115">Sway blockiert Änderungen zu einem Sway, sobald es ein Signal empfängt, dass das Konto gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b2a44-115">Sway blocks changes to to a sway as soon as it receives a signal that the account was deleted.</span></span> <span data-ttu-id="b2a44-116">Es gibt jedoch eine geringe Wahrscheinlichkeit, dass ein Sway bearbeitet werden kann, bevor dieses Signal empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="b2a44-116">However, there's a small chance that a sway can be edited before this signal is received.</span></span>

## <a name="issues-fixed-in-this-release"></a><span data-ttu-id="b2a44-117">In dieser Ausgabe behobene Probleme</span><span class="sxs-lookup"><span data-stu-id="b2a44-117">Issues fixed in this release</span></span>

- <span data-ttu-id="b2a44-118">DCR: Ausnahmebehandlung für nicht indizierte Elemente und verwaiste Elemente</span><span class="sxs-lookup"><span data-stu-id="b2a44-118">DCR: Exception handling for unindexed items and orphaned items</span></span>
- <span data-ttu-id="b2a44-119">DCR: Benachrichtigungen halten</span><span class="sxs-lookup"><span data-stu-id="b2a44-119">DCR: Hold notifications</span></span>
- <span data-ttu-id="b2a44-120">DCR: Verwalter in eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b2a44-120">DCR: Custodians in eDiscovery</span></span>

## <a name="whats-new"></a><span data-ttu-id="b2a44-121">Neuigkeiten</span><span class="sxs-lookup"><span data-stu-id="b2a44-121">What’s new</span></span>

- <span data-ttu-id="b2a44-122">**Die neu gestaltete Navigation im Security _AMP_ Compliance Center** – Advanced EDiscovery (Preview) hat ein neues Aussehen und Verhalten.</span><span class="sxs-lookup"><span data-stu-id="b2a44-122">**Redesigned navigation in the Security & Compliance Center** – Advanced eDiscovery (Preview) has a new look and feel.</span></span> <span data-ttu-id="b2a44-123">Verwenden Sie Advanced eDiscovery (Preview), um einen größeren Fall Workflow zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b2a44-123">Use Advanced eDiscovery (Preview) to manage more of your case workflow.</span></span>

- <span data-ttu-id="b2a44-124">**Case Management** – zusätzliche Unterstützung für neue Falltypen.</span><span class="sxs-lookup"><span data-stu-id="b2a44-124">**Case management** – There’s additional support for new case types.</span></span> <span data-ttu-id="b2a44-125">Sie können auch Ihre letzten und bevorzugten Fälle auswählen und speichern.</span><span class="sxs-lookup"><span data-stu-id="b2a44-125">You can also select and save your recent and favorite cases.</span></span> <span data-ttu-id="b2a44-126">Verfolgen und Überwachen von Aktivitäten innerhalb und über die Fälle mithilfe neuer Dashboards.</span><span class="sxs-lookup"><span data-stu-id="b2a44-126">Track and monitor activity within and across cases using new dashboards.</span></span>

- <span data-ttu-id="b2a44-127">**Depotverwaltung** – hinzufügen und Entfernen von Benutzern als Datenverwalter innerhalb eines Falls.</span><span class="sxs-lookup"><span data-stu-id="b2a44-127">**Custodian management** – Add and remove users as data custodians within a case.</span></span>

- <span data-ttu-id="b2a44-128">**Exchange-, OneDrive-und Teams-Integration** – fügen Sie automatisch die aktuellen Postfach-, OneDrive for Business-und Microsoft Teams-Websites eines Benutzers zu einem Fall hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2a44-128">**Exchange, OneDrive, and Teams Integration** – Automatically add a user’s current mailbox, OneDrive for Business account, and Microsoft Teams sites to a case.</span></span> 

- <span data-ttu-id="b2a44-129">**Depot Kommunikation** – senden und Verwalten von Benachrichtigungen für zugelassene Aufbewahrungsdaten im Namen Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a44-129">**Custodian communications** – Send and manage legal hold notifications on behalf of your organization.</span></span>

- <span data-ttu-id="b2a44-130">**Depot Portal** – neues Portal für Verwalter für den Zugriff auf Ihre Active Hold-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="b2a44-130">**Custodian portal** – New portal for custodians to access their active hold notices.</span></span>

- <span data-ttu-id="b2a44-131">**Deep Indexing** – beim erneuten durchforsten teilweise indizierter Elemente bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="b2a44-131">**Deep indexing** – Re-crawl partially indexed items on demand.</span></span>

- <span data-ttu-id="b2a44-132">**Fehler** Korrektur – beheben oder Herunterladen von Verarbeitungsfehlern; Hierzu gehört die Korrektur Unterstützung für umfangreiche Dateitypen, kennwortgeschützte Dateien und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="b2a44-132">**Error remediation** – Remediate or download processing errors; this include remediation support for large file types, password protected files, and more.</span></span> 

- <span data-ttu-id="b2a44-133">**Verbesserungen bei der Suche** – erstellen Sie eine Suche, indem Sie Verwalter und/oder Standorte identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b2a44-133">**Improvements to search** – Create a search by identifying custodians and/or locations.</span></span>

- <span data-ttu-id="b2a44-134">**Arbeitsmappen** – verwalten, nachverfolgen und Überwachen von statischen Dokumentsätzen.</span><span class="sxs-lookup"><span data-stu-id="b2a44-134">**Working sets** – Manage, track, and audit static sets of documents.</span></span>

- <span data-ttu-id="b2a44-135">**Review** – verwenden Sie eine native, Text-und systemeigene Ansicht, um Dokumente zu überprüfen, die Ihrem Workingset hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b2a44-135">**Review** – Use a native, text, and near-native view to review documents added to your working set.</span></span>

- <span data-ttu-id="b2a44-136">**Redact, Tags und Anmerkungen** – Redact Text, wendet Tags an und macht Anmerkungen, wenn Sie Dokumente überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b2a44-136">**Redact, tag, and annotate** – Redact text, apply tags, and make annotations as you review documents.</span></span>
  
- <span data-ttu-id="b2a44-137">**Analytics-powered Review**– Nutzung von eDiscovery-Analysen zum Suchen, suchen und Ausschlachten von Ergebnissen in einem Arbeitssatz.</span><span class="sxs-lookup"><span data-stu-id="b2a44-137">**Analytics-powered review**– Leverage eDiscovery analytics to find, search, and cull results within a working set.</span></span>

- <span data-ttu-id="b2a44-138">**Jobs** – verfolgen Sie den Status lang andauernder Prozesse.</span><span class="sxs-lookup"><span data-stu-id="b2a44-138">**Jobs** – Track status of long-running processes.</span></span>

- <span data-ttu-id="b2a44-139">**Neue Überwachungsaktivitäten** – verfolgen und Anzeigen neuer Überwachungsaktivitäten für erweiterte eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b2a44-139">**New audit activities** – Track and view new audit activity for Advanced eDiscovery.</span></span>

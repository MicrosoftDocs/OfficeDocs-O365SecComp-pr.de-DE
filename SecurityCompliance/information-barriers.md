---
title: Übersicht über Informationsbarrieren
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Verwenden Sie Informationsbarrieren, um die Kommunikation mit Microsoft Teams in Ihrer Organisation sicherzustellen.
ms.openlocfilehash: a2c202d08f1de60f92f13b2ac4c2b9d3c7f900e8
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935937"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="4b9ed-103">Informationsbarrieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="4b9ed-103">Information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="4b9ed-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4b9ed-104">Overview</span></span>

<span data-ttu-id="4b9ed-105">Microsoft Cloud Services umfassen leistungsstarke Funktionen für Kommunikation und Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-105">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="4b9ed-106">Angenommen, Sie möchten die Kommunikation zwischen zwei Gruppen einschränken, um zu verhindern, dass in Ihrer Organisation ein Interessenkonflikt auftritt.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-106">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="4b9ed-107">Oder Sie möchten möglicherweise die Kommunikation zwischen bestimmten Personen innerhalb Ihrer Organisation einschränken, um interne Informationen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-107">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="4b9ed-108">Microsoft 365 ermöglicht die Kommunikation und Zusammenarbeit zwischen Gruppen und Organisationen, gibt es also eine Möglichkeit, die Kommunikation zwischen bestimmten Benutzergruppen einzuschränken, wenn dies erforderlich ist?</span><span class="sxs-lookup"><span data-stu-id="4b9ed-108">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="4b9ed-109">Mit Informationsbarrieren, können Sie!</span><span class="sxs-lookup"><span data-stu-id="4b9ed-109">With information barriers, you can!</span></span> 

<span data-ttu-id="4b9ed-110">Informationsbarrieren befinden sich jetzt in der Vorschau, beginnend mit Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-110">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="4b9ed-111">Wenn diese Features für Ihre Organisation verfügbar sind, kann ein Administrator für Compliance-oder Informationsbarrieren Richtlinien definieren, um die Kommunikation zwischen Benutzergruppen in Microsoft Teams zuzulassen oder zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-111">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="4b9ed-112">Richtlinien für Informationsbarrieren können für Situationen wie diese verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4b9ed-112">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="4b9ed-113">Ein Day Trader kann keine Person im Marketing Team anrufen</span><span class="sxs-lookup"><span data-stu-id="4b9ed-113">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="4b9ed-114">Finanz Personal, das an vertraulichen Unternehmensinformationen arbeitet, kann keine Anrufe von bestimmten Gruppen innerhalb Ihrer Organisation empfangen.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-114">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="4b9ed-115">Ein internes Team mit Geschäfts geheimem Material kann nicht online mit Personen in bestimmten Gruppen innerhalb Ihrer Organisation anrufen oder chatten.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-115">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="4b9ed-116">Ein Forschungsteam kann nur online mit einem Produktentwicklungsteam anrufen oder chatten</span><span class="sxs-lookup"><span data-stu-id="4b9ed-116">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="4b9ed-117">Für alle diese Beispielszenarien (und mehr) können Richtlinien für Informationsbarrieren definiert werden, um die Kommunikation in Microsoft Teams zu verhindern oder zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-117">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="4b9ed-118">Mithilfe solcher Richtlinien kann verhindert werden, dass Personen Anrufe oder Chats mit Personen durchlaufen, die Sie nicht haben sollten, oder dass Personen nur mit bestimmten Gruppen in Microsoft Teams kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-118">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="4b9ed-119">Wenn die Richtlinien für Informationsbarrieren wirksam sind und Benutzer, die von diesen Richtlinien abgedeckt werden, versuchen, mit anderen Personen in Microsoft Teams zu kommunizieren, werden Überprüfungen durchgeführt, um die Kommunikation zu verhindern (oder zulassen) (gemäß den Richtlinien für Informationsbarrieren).</span><span class="sxs-lookup"><span data-stu-id="4b9ed-119">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> <span data-ttu-id="4b9ed-120">Weitere Informationen zur Benutzererfahrung mit Informationsbarrieren finden Sie unter [Information Barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span><span class="sxs-lookup"><span data-stu-id="4b9ed-120">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

> [!NOTE]
> <span data-ttu-id="4b9ed-121">Informationsbarrieren gelten nicht für e-Mail-Kommunikationen oder für die Dateifreigabe über SharePoint Online oder OneDrive.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-121">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="4b9ed-122">Erforderliche Lizenzen und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4b9ed-122">Required licenses and permissions</span></span>

<span data-ttu-id="4b9ed-123">**Derzeit befindet sich das Feature "Informations Barriere" in privater Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-123">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="4b9ed-124">Wenn diese Features allgemein verfügbar sind, werden Sie in Abonnements eingeschlossen, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="4b9ed-124">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="4b9ed-125">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="4b9ed-125">Microsoft 365 E5</span></span>
- <span data-ttu-id="4b9ed-126">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="4b9ed-126">Office 365 E5</span></span>
- <span data-ttu-id="4b9ed-127">Office 365 Erweiterte Compliance</span><span class="sxs-lookup"><span data-stu-id="4b9ed-127">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="4b9ed-128">Microsoft 365 E5 – Informationsschutz und Compliance</span><span class="sxs-lookup"><span data-stu-id="4b9ed-128">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="4b9ed-129">Weitere Informationen finden Sie unter [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span><span class="sxs-lookup"><span data-stu-id="4b9ed-129">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="4b9ed-130">Um [Richtlinien für Informationsbarrieren zu definieren oder zu bearbeiten](information-barriers-policies.md), muss Ihnen eine der folgenden Rollen zugewiesen sein:</span><span class="sxs-lookup"><span data-stu-id="4b9ed-130">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="4b9ed-131">Microsoft 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="4b9ed-131">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="4b9ed-132">Globaler Office 365-Administrator\ </span><span class="sxs-lookup"><span data-stu-id="4b9ed-132">Office 365 global administrator</span></span>
- <span data-ttu-id="4b9ed-133">Compliance-Administrator</span><span class="sxs-lookup"><span data-stu-id="4b9ed-133">Compliance administrator</span></span>
- <span data-ttu-id="4b9ed-134">Administrator für Informationsbarrieren</span><span class="sxs-lookup"><span data-stu-id="4b9ed-134">Information barriers administrator</span></span>

<span data-ttu-id="4b9ed-135">Sie müssen mit PowerShell-Cmdlets vertraut sein, um Richtlinien für Informationsbarrieren zu definieren, zu validieren oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-135">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="4b9ed-136">Obwohl in den [Gewusst-wie-Informationen](information-barriers-policies.md)mehrere Beispiele für PowerShell-Cmdlets bereitgestellt werden, müssen Sie zusätzliche Details wie Parameter für Ihre Organisation kennen.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-136">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4b9ed-137">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="4b9ed-137">Next steps</span></span>

- [<span data-ttu-id="4b9ed-138">Weitere Informationen zu Informationsbarrieren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4b9ed-138">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="4b9ed-139">Siehe die Attribute, die für Richtlinien für Informationsbarrieren verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4b9ed-139">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="4b9ed-140">Definieren von Richtlinien für Informationsbarrieren</span><span class="sxs-lookup"><span data-stu-id="4b9ed-140">Define policies for information barriers</span></span>](information-barriers-policies.md) 


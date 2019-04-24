---
title: Einrichten von Benutzern und Fällen in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Erfahren Sie, wie Sie Benutzerrollen konfigurieren, Fälle erstellen und Benutzer zu Fällen in Office 365 Advanced eDiscovery zuweisen.  '
ms.openlocfilehash: 5a22e0683e49ebdaf8391e092aeb101386e0636b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260703"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ba2ca-103">Einrichten von Benutzern und Fällen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ba2ca-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="ba2ca-104">In diesem Thema wird beschrieben, wie Sie Benutzer und Fälle für Office 365 Advanced eDiscovery einrichten.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ba2ca-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ba2ca-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="ba2ca-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ba2ca-107">Prerequisites</span></span>

<span data-ttu-id="ba2ca-108">Bevor Sie Fälle und Benutzer in Advanced eDiscovery einrichten, ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="ba2ca-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="ba2ca-109">Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-109">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license.</span></span> <span data-ttu-id="ba2ca-110">Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-110">Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license.</span></span> <span data-ttu-id="ba2ca-111">Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-111">Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="ba2ca-112">Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Office 365 Security &amp; Compliance Center sein, um einen eDiscovery-Fall zu erstellen und ihm Mitglieder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-112">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it.</span></span> <span data-ttu-id="ba2ca-113">Um sich selbst der eDiscovery-Manager-Rollengruppe im &amp; Security Compliance Center hinzuzufügen, müssen Sie ein globaler Administrator in ihrer Office 365-Organisation sein.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-113">To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization.</span></span> <span data-ttu-id="ba2ca-114">Wenn Sie kein globaler Administrator sind, müssen Sie einen globalen Administrator bitten, Sie der Rollengruppe "eDiscovery-Manager" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-114">If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group.</span></span> <span data-ttu-id="ba2ca-115">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ba2ca-115">For more information, see:</span></span>
    
  - [<span data-ttu-id="ba2ca-116">Berechtigungen im Microsoft 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="ba2ca-116">Permissions in the Microsoft 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="ba2ca-117">Zuweisen von eDiscovery-Berechtigungen im Microsoft 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="ba2ca-117">Assign eDiscovery permissions in the Microsoft‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="ba2ca-118">Schritt 1: Zuweisen von eDiscovery-Berechtigungen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="ba2ca-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="ba2ca-119">Der erste Schritt besteht darin, Benutzern die Anforderungs Berechtigungen im Security &amp; Compliance Center zuzuweisen, damit Sie als Mitglied eines eDiscovery-Falls hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-119">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case.</span></span> <span data-ttu-id="ba2ca-120">Nachdem ein Benutzer als Mitglied eines Falls im Security &amp; Compliance Center hinzugefügt wurde, kann er in Advanced eDiscovery auf den Fall zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-120">After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="ba2ca-121">Wenn Sie einem Benutzer die erforderlichen Berechtigungen zuweisen möchten, damit er als Mitglied eines eDiscovery-Falls hinzugefügt werden kann, lesen Sie Schritt 1 in [eDiscovery- &amp; fällen im Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="ba2ca-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="ba2ca-122">Schritt 2: Erstellen eines eDiscovery-Falls und Hinzufügen von Mitgliedern</span><span class="sxs-lookup"><span data-stu-id="ba2ca-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="ba2ca-123">Im nächsten Schritt erstellen Sie einen neuen eDiscovery-Fall im Security &amp; Compliance Center und fügen Mitglieder hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-123">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members.</span></span> <span data-ttu-id="ba2ca-124">Die Mitglieder des Falles können dann in Advanced eDiscovery auf den Fall zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-124">Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="ba2ca-125">Informationen zum Erstellen eines neuen eDiscovery-Falls finden Sie unter Schritt 2 in [eDiscovery-Fällen im &amp; Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="ba2ca-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="ba2ca-126">Informationen zum Hinzufügen von Mitgliedern zu einem eDiscovery-Fall finden Sie unter Schritt 3 in [eDiscovery- &amp; fällen im Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case) .</span><span class="sxs-lookup"><span data-stu-id="ba2ca-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="ba2ca-127">Schritt 3: gehen Sie zu einem Fall in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ba2ca-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="ba2ca-128">Nachdem Sie einen eDiscovery-Fall erstellt und Mitglieder hinzugefügt haben, können Sie (oder ein beliebiger Member) in Advanced eDiscovery auf den entsprechenden Fall zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-128">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery.</span></span> <span data-ttu-id="ba2ca-129">Informationen zum Zugriff auf einen Fall in Advanced eDiscovery finden Sie in Schritt 8 in [eDiscovery-Fällen im &amp; Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="ba2ca-129">To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba2ca-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba2ca-130">See also</span></span>

[<span data-ttu-id="ba2ca-131">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ba2ca-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ba2ca-132">Vorbereiten der Daten</span><span class="sxs-lookup"><span data-stu-id="ba2ca-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
 
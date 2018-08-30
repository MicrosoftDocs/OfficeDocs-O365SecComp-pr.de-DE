---
title: Einrichten von Benutzern und in Office 365 erweiterte eDiscovery-Fälle
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Informationen Sie zum Konfigurieren von Benutzerrollen, Fälle erstellen und Zuweisen von Benutzern zu Fällen in Office 365 erweiterte eDiscovery.  '
ms.openlocfilehash: 49f76b415d86035cecafc19c23b36c413f7576e5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529708"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="57ca5-103">Einrichten von Benutzern und in Office 365 erweiterte eDiscovery-Fälle</span><span class="sxs-lookup"><span data-stu-id="57ca5-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="57ca5-104">In diesem Thema wird beschrieben, wie Benutzer und für Office 365 erweiterte eDiscovery-Fälle einrichten.</span><span class="sxs-lookup"><span data-stu-id="57ca5-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="57ca5-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="57ca5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="57ca5-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="57ca5-107">Prerequisites</span></span>

<span data-ttu-id="57ca5-108">Vor dem Einrichten von Fällen und Benutzer in erweiterten eDiscovery, ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="57ca5-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="57ca5-p102">Um eine erweiterte eDiscovery mit Benutzerdaten zu analysieren, muss der Benutzer (der Verwaltungsberechtigte der Daten) eine Lizenz für Office 365 E5 zugewiesen werden. Alternativ können der Benutzer mit einer Lizenz für Office 365 E1 oder E3 eine erweiterte eDiscovery eigenständige Lizenz zugewiesen werden. Administratoren und Compliance Officer, die zugewiesenen Fällen und erweiterte eDiscovery verwenden, um Daten zu analysieren erforderlich keine E5-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="57ca5-p102">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="57ca5-p103">Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in der Office 365-Sicherheit sein &amp; Compliance Center zum Erstellen eines eDiscovery-Fall und Mitglieder hinzufügen. Selbst bei der Sicherheit der eDiscovery-Manager-Rollengruppe hinzufügen &amp; Compliance Center, Sie müssen ein globaler Administrator in Office 365-Organisation sein. Wenn Sie kein globaler Administrator angemeldet sind, müssen Sie bitten Sie einen globalen Administrator So fügen Sie der eDiscovery-Manager-Rollengruppe hinzu. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="57ca5-p103">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it. To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization. If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group. For more information, see:</span></span>
    
  - [<span data-ttu-id="57ca5-116">Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="57ca5-116">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="57ca5-117">Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="57ca5-117">Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="57ca5-118">Schritt 1: Zuweisen von Benutzern Berechtigungen für eDiscovery</span><span class="sxs-lookup"><span data-stu-id="57ca5-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="57ca5-p104">Der erste Schritt besteht, Benutzern die Anforderung Zuweisen von Berechtigungen in das Wertpapier &amp; Compliance Center, damit sie können mich als Mitglied einer eDiscovery-Fall hinzugefügt. Nachdem ein Benutzer, als Mitglied einer Anfrage in das Wertpapier hinzugefügt wird &amp; Compliance Center, werden auf die Groß-/Kleinschreibung im erweiterten eDiscovery zugreifen.</span><span class="sxs-lookup"><span data-stu-id="57ca5-p104">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case. After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="57ca5-121">Wenn einem Benutzer die erforderlichen Berechtigungen zuweisen, damit sie als Mitglied einer eDiscovery-Fall hinzugefügt werden können, finden Sie unter Schritt 1 in [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="57ca5-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="57ca5-122">Schritt 2: Erstellen einen eDiscovery-Fall und Hinzufügen von Mitgliedern</span><span class="sxs-lookup"><span data-stu-id="57ca5-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="57ca5-p105">Im nächste Schritt ist die Erstellung einen neuen eDiscovery-Fall in das Wertpapier &amp; Compliance Center und Hinzufügen von Mitgliedern. Mitglieder der Groß-/Kleinschreibung werden klicken Sie dann auf die Groß-/Kleinschreibung im erweiterten eDiscovery zugreifen.</span><span class="sxs-lookup"><span data-stu-id="57ca5-p105">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members. Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="57ca5-125">Erstellen einen neue eDiscovery-Fall, finden Sie unter Schritt2 im [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="57ca5-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="57ca5-126">Zum Hinzufügen von Mitgliedern zu einem eDiscovery-Fall finden Sie unter Schritt 3 in [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="57ca5-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="57ca5-127">Schritt 3: Eine Anfrage in erweiterten eDiscovery wechseln</span><span class="sxs-lookup"><span data-stu-id="57ca5-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="57ca5-p106">Nachdem Sie einen eDiscovery-Fall erstellen und Hinzufügen von Mitgliedern, können Sie (oder ein beliebiges Element von der Groß-/Kleinschreibung) die entsprechende Groß-/Kleinschreibung im erweiterten eDiscovery zugreifen. Zugriff auf eine Anfrage in erweiterten eDiscovery finden Sie in Schritt 8 in [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="57ca5-p106">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery. To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57ca5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ca5-130">See also</span></span>

[<span data-ttu-id="57ca5-131">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="57ca5-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="57ca5-132">Vorbereiten von Daten</span><span class="sxs-lookup"><span data-stu-id="57ca5-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
  
[<span data-ttu-id="57ca5-133">Benutzerrollen und access</span><span class="sxs-lookup"><span data-stu-id="57ca5-133">User roles and access</span></span>](user-roles-and-access-in-advanced-ediscovery.md)


---
title: Zugriffsrichtlinien in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud App-Sicherheitszugriffs Richtlinien ermöglichen die Echtzeitüberwachung und Steuerung des Zugriffs auf Cloud-apps basierend auf Benutzer, Standort, Gerät und App. Sie können Zugriffsrichtlinien für ein beliebiges Gerät erstellen, einschließlich der Geräte, für die keine Domäne verbunden ist, und die nicht von Windows InTune verwaltet werden, indem Sie Clientzertifikate auf verwalteten Geräten oder mithilfe vorhandener Zertifikate wie Drittanbieter-MDM-Zertifikate bereitstellen. Sie können beispielsweise Clientzertifikate auf verwalteten Geräten bereitstellen und dann den Zugriff von Geräten ohne Zertifikat blockieren.
ms.openlocfilehash: a8651cb51419c93998f2ce6e176fab7c1651b6ea
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219775"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a><span data-ttu-id="220cc-105">Zugriffsrichtlinien in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="220cc-105">Access policies in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="220cc-106">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="220cc-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="220cc-107">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="220cc-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="220cc-108">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="220cc-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="220cc-109">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="220cc-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="220cc-110">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="220cc-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="220cc-111">Planung starten</span><span class="sxs-lookup"><span data-stu-id="220cc-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="220cc-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="220cc-112">You are here!</span></span>  <br/> [<span data-ttu-id="220cc-113">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="220cc-113">Next step</span></span>](group-your-ip-addresses-in-ocas.md) <br/> |[<span data-ttu-id="220cc-114">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="220cc-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="220cc-p102">Office 365 Cloud App-Sicherheitszugriffs Richtlinien ermöglichen die Echtzeitüberwachung und Steuerung des Zugriffs auf Cloud-apps basierend auf Benutzer, Standort, Gerät und App. Sie können Zugriffsrichtlinien für ein beliebiges Gerät erstellen, einschließlich der Geräte, für die keine Domäne verbunden ist, und die nicht von Windows InTune verwaltet werden, indem Sie Clientzertifikate auf verwalteten Geräten oder mithilfe vorhandener Zertifikate wie Drittanbieter-MDM-Zertifikate bereitstellen. Sie können beispielsweise Clientzertifikate auf verwalteten Geräten bereitstellen und dann den Zugriff von Geräten ohne Zertifikat blockieren.</span><span class="sxs-lookup"><span data-stu-id="220cc-p102">Office 365 Cloud App Security access policies enable real-time monitoring and control over access to cloud apps based on user, location, device, and app. You can create access policies for any device, including devices that aren't domain joined, and not managed by Windows Intune by rolling out client certificates to managed devices or by using existing certificates, such as third-party MDM certificates. For example, you can deploy client certificates to managed devices, and then block access from devices without a certificate.</span></span>

<span data-ttu-id="220cc-118">Anstatt den Zugriff vollständig zuzulassen oder zu blockieren, können Sie mit [Sitzungs Richtlinien](ocas-session-policies.md) Zugriff gewähren, während Sie die Sitzung überwachen und/oder bestimmte Sitzungsaktivitäten einschränken.</span><span class="sxs-lookup"><span data-stu-id="220cc-118">Instead of allowing or blocking access completely, with [session policies](ocas-session-policies.md) you can allow access while monitoring the session and/or limit specific session activities.</span></span>

## <a name="prerequisites-to-using-access-policies"></a><span data-ttu-id="220cc-119">VoraussetZungen für die Verwendung von Zugriffsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="220cc-119">Prerequisites to using access policies</span></span>

- <span data-ttu-id="220cc-120">Azure AD Premium P1-Lizenz</span><span class="sxs-lookup"><span data-stu-id="220cc-120">Azure AD Premium P1 license</span></span>

- <span data-ttu-id="220cc-121">Die relevanten apps sollten [mit Conditional Access-App-Steuerelement bereitgestellt](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad) werden.</span><span class="sxs-lookup"><span data-stu-id="220cc-121">The relevant apps should be [deployed with Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span></span>

- <span data-ttu-id="220cc-122">eine [richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den Azure AD-bedingten zugriff sollte vorhanden sein, die benutzer wie unten beschrieben zu Office 365 Cloud App Security umleitet.</span><span class="sxs-lookup"><span data-stu-id="220cc-122">An [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) should be in place that redirects users to Office 365 Cloud App Security, as described below.</span></span>

## <a name="create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="220cc-123">Erstellen einer Richtlinie für den Azure AD-bedingten Zugriff</span><span class="sxs-lookup"><span data-stu-id="220cc-123">Create an Azure AD conditional access policy</span></span>

<span data-ttu-id="220cc-p103">Azure Active Directory-Richtlinien für den bedingten Zugriff und Cloud-App-Sicherheits Sitzungs Richtlinien arbeiten zusammen, um jede Benutzersitzung zu überprüfen und Richtlinien Entscheidungen für jede APP zu treffen. Gehen Sie folgendermaßen vor, um eine Richtlinie für den bedingten Zugriff in Azure AD einzurichten:</span><span class="sxs-lookup"><span data-stu-id="220cc-p103">Azure Active Directory conditional access policies and Cloud App Security session policies work in tandem to examine each user session and make policy decisions for each app. To set up a conditional access policy in Azure AD, follow this procedure:</span></span>

1. <span data-ttu-id="220cc-126">Konfigurieren Sie eine [Azure AD-Richtlinie](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) für den bedingten Zugriff mit Zuweisungen für Benutzer oder Gruppen von Benutzern und die APP, die Sie mit der APP-Steuerelement Steuerung für bedingte Zugriffssteuerung steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="220cc-126">Configure an [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) with assignments for user or group of users and the app you want to control with Conditional Access App Control.</span></span><br><span data-ttu-id="220cc-127">Hinweis: nur apps, die [mit Conditional Access-App-Steuerelement bereitgestellt](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)wurden, sind von dieser Richtlinie betroffen.</span><span class="sxs-lookup"><span data-stu-id="220cc-127">NOTE: Only apps that were [deployed with Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) will be affected by this policy.</span></span>

2. <span data-ttu-id="220cc-128">leiten sie benutzer an Office 365 Cloud app Security weiter, indem sie unter **sitzung**die option **Conditional Access-app-steuerelement mit bedingtem zugriff verwenden**aktivieren.</span><span class="sxs-lookup"><span data-stu-id="220cc-128">Route users to Office 365 Cloud App Security by selecting the **Use Conditional Access App Control enforced restrictions** under **Session**.</span></span>

## <a name="create-a-cloud-app-security-access-policy"></a><span data-ttu-id="220cc-129">Erstellen einer Cloud-App-Sicherheitszugriffs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="220cc-129">Create a Cloud App Security access policy</span></span>

<span data-ttu-id="220cc-130">Gehen Sie folgendermaßen vor, um eine neue Zugriffsrichtlinie zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="220cc-130">To create a new access policy, follow this procedure:</span></span>

1. <span data-ttu-id="220cc-131">Wählen Sie im Portal **Steuerelement** gefolgt von **Richtlinien**aus.</span><span class="sxs-lookup"><span data-stu-id="220cc-131">In the portal, select **Control** followed by **Policies**.</span></span>

2. <span data-ttu-id="220cc-132">Klicken Sie auf der Seite **Richtlinien** auf **Richtlinie** erstellen, und wählen Sie **Zugriffsrichtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="220cc-132">In the **Policies** page, click **Create policy** and select **Access policy**.</span></span>

3. <span data-ttu-id="220cc-133">Weisen Sie im Fenster **Zugriffsrichtlinie** einen Namen für die Richtlinie zu, beispielsweise den *Zugriff auf nicht verwalteten Geräten blockieren*.</span><span class="sxs-lookup"><span data-stu-id="220cc-133">In the **Access policy** window, assign a name for your policy, such as *Block access from unmanaged devices*.</span></span>

4. <span data-ttu-id="220cc-p104">Wählen Sie in den Aktivitäten, die mit dem **folgenden** Abschnitt übereinstimmen, unter **Aktivitäts Quelle**die Option Weitere Aktivitäts Filter aus, die auf die Richtlinie angewendet werden sollen. Zu den Filtern gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="220cc-p104">In the **Activities matching all of the following** section, Under **Activity source**, select additional activity filters to apply to the policy. Filters include the following options:</span></span>
    
    - <span data-ttu-id="220cc-136">**Geräte Tags**: Verwenden Sie diesen Filter, um nicht verwaltete Geräte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="220cc-136">**Device tags**: Use this filter to identify unmanaged devices.</span></span>
    
    - <span data-ttu-id="220cc-137">**Speicherort**: Verwenden Sie diesen Filter, um unbekannte (und daher riskante) Speicherorte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="220cc-137">**Location**: Use this filter to identify unknown (and therefore risky) locations.</span></span>
    
    - <span data-ttu-id="220cc-138">**IP-Adresse**: Verwenden Sie diesen Filter, um nach IP-Adressen zu filtern oder zuvor zugewiesene IP-Adress Tags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="220cc-138">**IP address**: Use this filter to filter per IP addresses or use previously assigned IP address tags.</span></span>
    
    - <span data-ttu-id="220cc-p105">**Benutzer-Agent-Tag**: Verwenden Sie diesen Filter, um die Heuristik zur Identifizierung mobiler und Desktop-Apps zu aktivieren. Dieser Filter kann auf Equals oder ungleich festgelegt werden. Die Werte sollten für jede Cloud-App mit ihren mobilen und Desktop-Apps getestet werden.</span><span class="sxs-lookup"><span data-stu-id="220cc-p105">**User agent tag**: Use this filter to enable the heuristic to identify mobile and desktop apps. This filter can be set to equals or does not equal. The values should be tested against your mobile and desktop apps for each cloud app.</span></span>

5. <span data-ttu-id="220cc-142">Wählen Sie unter **Aktionen**eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="220cc-142">Under **Actions**, select one of the following options:</span></span>
    
    - <span data-ttu-id="220cc-143">**Zulassen**: Legen Sie diese Aktion so fest, dass der Zugriff entsprechend den von Ihnen festgelegten Richtlinien Filtern explizit zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="220cc-143">**Allow**: Set this action to explicitly allow access according to the policy filters you set.</span></span>
    
    - <span data-ttu-id="220cc-144">**Blockieren**: Legen Sie diese Aktion so fest, dass der Zugriff entsprechend den festgelegten Richtlinien Filtern explizit blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="220cc-144">**Block**: Set this action to explicitly block access according to the policy filters you set.</span></span>

6. <span data-ttu-id="220cc-145">Sie können **eine Warnung für jedes übereinstimmende Ereignis mit dem Schweregrad der Richtlinie erstellen**und einen Warnungsgrenzwert festlegen und auswählen, ob die Warnung als e-Mail, als Textnachricht oder als beides angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="220cc-145">You can **Create an alert for each matching event with the policy's severity** and set an alert limit and select whether you want the alert as an email, a text message or both.</span></span>

## <a name="next-steps"></a><span data-ttu-id="220cc-146">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="220cc-146">Next steps</span></span>

- [<span data-ttu-id="220cc-147">Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="220cc-147">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)
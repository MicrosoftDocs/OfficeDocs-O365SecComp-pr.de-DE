---
title: Bereitstellen der App-Steuerung für bedingten Zugriff für Office 365-Apps
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Führen Sie die folgenden Schritte aus, um Azure AD Office 365-apps so zu konfigurieren, dass Sie von der Office 365 Cloud App Security Conditional Access-App-Steuerung gesteuert werden.
ms.openlocfilehash: cfb3d885fdfaf0e4698b1f8f9a0e13baacf43f66
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221055"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a><span data-ttu-id="d259e-103">Bereitstellen der App-Steuerung für bedingten Zugriff für Office 365-Apps</span><span class="sxs-lookup"><span data-stu-id="d259e-103">Deploy Conditional Access App Control for Office 365 apps</span></span>

|<span data-ttu-id="d259e-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d259e-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="d259e-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d259e-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="d259e-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="d259e-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="d259e-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d259e-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d259e-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="d259e-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="d259e-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="d259e-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="d259e-110">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="d259e-110">You are here!</span></span>  <br/> [<span data-ttu-id="d259e-111">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="d259e-111">Next step</span></span>](ocas-session-policies.md) <br/> |[<span data-ttu-id="d259e-112">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="d259e-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="d259e-113">Führen Sie die folgenden Schritte aus, um Azure AD Office 365-apps so zu konfigurieren, dass Sie von der Office 365 Cloud App Security Conditional Access-App-Steuerung gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="d259e-113">Follow these steps to configure Azure AD Office 365 apps to be controlled by Office 365 Cloud App Security Conditional Access App Control.</span></span>

<span data-ttu-id="d259e-114">**Schritt 1: [Erstellen einer Azure AD-Richtlinie für den bedingten Zugriff](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span><span class="sxs-lookup"><span data-stu-id="d259e-114">**Step 1: [Create an Azure AD conditional access test policy](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span></span>

<span data-ttu-id="d259e-115">**Schritt 2: [melden Sie sich mit einem Benutzer an, der auf die Richtlinie in den apps beschränkt](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps) ist.**</span><span class="sxs-lookup"><span data-stu-id="d259e-115">**Step 2: [Sign in with a user scoped to the policy in the apps](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span></span>

<span data-ttu-id="d259e-116">**Schritt 3: Wenn Sie keine integrierte Sicherheitsrichtlinie für die Cloud-app in Azure AD ausgewählt haben oder wenn Sie die Richtlinie auf eine nicht-featured-app anwenden möchten, [Konfigurieren Sie erweiterte Steuerelemente im Sicherheitsportal der Cloud-App](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal) .**</span><span class="sxs-lookup"><span data-stu-id="d259e-116">**Step 3: If you did not select a built-in Cloud App Security policy in Azure AD or if you want to apply the policy to a non-featured app, [Configure advanced controls in the Cloud App Security portal](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span></span>

<span data-ttu-id="d259e-117">**Schritt 4: [Testen der Bereitstellung](#step-4-test-the-deployment)**</span><span class="sxs-lookup"><span data-stu-id="d259e-117">**Step 4: [Test the deployment](#step-4-test-the-deployment)**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d259e-118">für die bereitstellung von app-steuerelement für den bedingten zugriff für office 365-apps benötigen sie eine gültige [lizenz für Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) sowie eine Office 365 Cloud app-sicherheitslizenz.</span><span class="sxs-lookup"><span data-stu-id="d259e-118">To deploy Conditional Access App Control for Office 365 apps, you need a valid [license for Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) as well as a Office 365 Cloud App Security license.</span></span>

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a><span data-ttu-id="d259e-119">Schritt 1: Erstellen einer Azure AD-Richtlinie für den bedingten Zugriff</span><span class="sxs-lookup"><span data-stu-id="d259e-119">Step 1: Create an Azure AD conditional access test policy</span></span> 

1. <span data-ttu-id="d259e-120">Klicken Sie in Azure Active Directory unter **Sicherheit**auf **bedingter Zugriff**.</span><span class="sxs-lookup"><span data-stu-id="d259e-120">In Azure Active Directory, under **Security**, click on **Conditional access**.</span></span>

2. <span data-ttu-id="d259e-121">Klicken Sie auf **neue Richtlinie** , und erstellen Sie eine neue Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d259e-121">Click **New policy** and create a new policy.</span></span>

3. <span data-ttu-id="d259e-122">Weisen Sie in der Testrichtlinie unter **Benutzer**einen Test Benutzer oder Benutzer zu, der für eine erstmalige Anmeldung und Überprüfung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d259e-122">In the TEST policy, under **Users**, assign a test user or user that can be used for an initial sign-on and verification.</span></span>

4. <span data-ttu-id="d259e-123">Weisen Sie in der TEST Richtlinie unter **Cloud-App**die apps zu, die Sie mit Conditional Access-App-Steuerelement steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="d259e-123">In the TEST policy, under **Cloud app**, assign the apps you want to control with Conditional Access App Control.</span></span>

5. <span data-ttu-id="d259e-p101">Legen Sie unter **Sitzung**fest, dass die Richtlinie eine der integrierten Richtlinien, **nur** überwachen oder **Blockieren von Downloads**verwendet. Oder wählen Sie **benutzerdefinierte Richtlinie** verwenden aus, um eine erweiterte Richtlinie im Sicherheitsportal der Cloud-App festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d259e-p101">Under **Session**, set the policy to use either of the built-in policies, **Monitor only** or **Block downloads**. Or select **Use custom policy** to set an advanced policy in the Cloud App Security portal.</span></span>

6. <span data-ttu-id="d259e-126">Fügen Sie alle \*\*\*\* anwendbaren Bedingungs Zuweisungen oder **Grant-Steuerelemente** hinzu (optional).</span><span class="sxs-lookup"><span data-stu-id="d259e-126">Add any applicable **Condition assignments** or **Grant controls** (optional).</span></span>

> ![Bedingter Zugriff durch Azure AD](media/image1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a><span data-ttu-id="d259e-128">Schritt 2: Melden Sie sich mit einem Benutzer an, der auf die Richtlinie in den apps beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="d259e-128">Step 2: Sign in with a user scoped to the policy in the apps</span></span> 

<span data-ttu-id="d259e-p102">Nachdem Sie die Richtlinie erstellt haben, melden Sie sich bei jeder in dieser Richtlinie konfigurierten APP an. Stellen Sie sicher, dass Sie sich mit einem in der Richtlinie konfigurierten Benutzer angemeldet haben. Stellen Sie sicher, dass Sie sich zuerst bei vorhandenen Sitzungen abmelden.</span><span class="sxs-lookup"><span data-stu-id="d259e-p102">After you've created the policy, sign in to each app configured in that policy. Make sure you sign in using a user configured in the policy. Make sure to first sign out of existing sessions.</span></span>

<span data-ttu-id="d259e-p103">Cloud App Security synchronisiert Ihre Richtliniendetails mit ihren Servern für jede neue APP, bei der Sie sich anmelden. Dies kann bis zu einer Minute dauern.</span><span class="sxs-lookup"><span data-stu-id="d259e-p103">Cloud App Security will sync your policy details to its servers for each new app you log in to. This may take up to one minute.</span></span>

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a><span data-ttu-id="d259e-134">Schritt 3: Konfigurieren erweiterter Steuerelemente im Cloud-App-Sicherheitsportal</span><span class="sxs-lookup"><span data-stu-id="d259e-134">Step 3: Configure advanced controls in the Cloud App Security portal</span></span> 

<span data-ttu-id="d259e-135">Die obigen Anweisungen unterstützten Sie beim Erstellen einer integrierten Cloud-App-Sicherheitsrichtlinie für empfohlene apps direkt in Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d259e-135">The instructions above helped you create a built-in Cloud App Security policy for featured apps directly in Azure AD.</span></span>

<span data-ttu-id="d259e-136">erstellen sie eine [zugriffsrichtlinie](ocas-access-policies.md) oder eine [sitzungsrichtlinie](ocas-session-policies.md) im Office 365 Cloud App Security portal, um eine erweiterte richtlinie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d259e-136">To configure an advanced policy, create an [access policy](ocas-access-policies.md) or a [session policy](ocas-session-policies.md) in the Office 365 Cloud App Security portal.</span></span>

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a><span data-ttu-id="d259e-137">So identifizieren Sie Geräte mit Clientzertifikaten (optional):</span><span class="sxs-lookup"><span data-stu-id="d259e-137">To identify devices using client certificates (this is optional):</span></span>

1. <span data-ttu-id="d259e-138">Wechseln Sie zum COG Einstellungen und wählen Sie **Geräteidentifizierung**aus.</span><span class="sxs-lookup"><span data-stu-id="d259e-138">Go to the settings cog and choose **Device identification**.</span></span>

2. <span data-ttu-id="d259e-139">Laden Sie ein oder mehrere Zwischenzertifikate hoch.</span><span class="sxs-lookup"><span data-stu-id="d259e-139">Upload one or more root or intermediate certificates.</span></span>

3. <span data-ttu-id="d259e-140">Nachdem das Zertifikat hochgeladen wurde, können Sie Zugriffsrichtlinien und Sitzungs Richtlinien basierend auf **Device-Tag** und **gültigem Clientzertifikat**erstellen.</span><span class="sxs-lookup"><span data-stu-id="d259e-140">After the certificate is uploaded, you can create access policies and session policies based on **Device tag** and **Valid client certificate**.</span></span>

![App-Steuerelement-ID für bedingten Zugriff](media/image2.png)

> [!NOTE]
> <span data-ttu-id="d259e-142">Ein Zertifikat wird nur von einem Benutzer angefordert, wenn die Sitzung einer Richtlinie entspricht, die den gültigen Clientzertifikat Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="d259e-142">A certificate is only requested from a user if the session matches a policy that uses the valid client certificate filter.</span></span>
> 
## <a name="step-4-test-the-deployment"></a><span data-ttu-id="d259e-143">Schritt 4: Testen der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d259e-143">Step 4: Test the deployment</span></span> 

1. <span data-ttu-id="d259e-p104">Melden Sie sich zuerst bei vorhandenen Sitzungen ab. Versuchen Sie dann, sich bei jeder erfolgreich bereitgestellten App anzumelden. Melden Sie sich mit einem Benutzer an, der mit der in Azure AD konfigurierten Richtlinie übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d259e-p104">First sign out of any existing sessions. Then, try to sign in to each app that was successfully deployed. Sign in using a user that matches the policy configured in Azure AD.</span></span>

2. <span data-ttu-id="d259e-147">Wählen Sie im Sicherheitsportal Cloud app unter **untersuchen**die Option **Aktivitätsprotokoll**aus, und stellen Sie sicher, dass die Anmeldeaktivitäten für jede APP erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="d259e-147">In the Cloud App Security portal, under **Investigate**, select **Activity log**, and make sure the login activities are captured for each app.</span></span>

3. <span data-ttu-id="d259e-148">Sie können filtern, indem Sie auf **erweitert**klicken und dann mithilfe von **Source Equals Zugriffssteuerung**filtern.</span><span class="sxs-lookup"><span data-stu-id="d259e-148">You can filter by clicking on **Advanced**, and then filtering using **Source equals Access control**.</span></span>

4. <span data-ttu-id="d259e-p105">Es wird empfohlen, sich bei mobilen und Desktop-Apps über verwaltete und nicht verwaltete Geräte anzumelden. Dadurch wird sichergestellt, dass die Aktivitäten im Aktivitätsprotokoll korrekt erfasst werden. Um zu überprüfen, ob die Aktivität korrekt erfasst wurde, klicken Sie auf eine Aktivität für einmaliges Anmelden, damit die Aktivitäts Schublade geöffnet wird. Stellen Sie sicher, dass das **Benutzer-Agent-Tag** ordnungsgemäß reflektiert, ob es sich um einen nativen Client handelt (also eine Mobile oder Desktop-App) oder dass es sich bei dem Gerät um ein verwaltetes Gerät handelt (kompatibel, mit der Domäne verbunden oder ein gültiges Clientzertifikat)</span><span class="sxs-lookup"><span data-stu-id="d259e-p105">It's recommended that you sign into mobile and desktop apps from managed and unmanaged devices. This is to make sure that the activities are properly captured in the activity log. To verify that the activity is properly captured, click on a single sign-on log on activity so that it opens the activity drawer. Make sure the **User agent tag** properly reflects whether the device is a native client (meaning either a mobile or desktop app) or the device is a managed device (compliant, domain joined, or valid client certificate).</span></span>

> [!NOTE]
> <span data-ttu-id="d259e-p106">Nach der Bereitstellung können Sie eine APP nicht aus der APP-Steuerelement Seite für den bedingten Zugriff entfernen. Solange Sie keine Sitzungs-oder Zugriffsrichtlinie für die APP festlegen, ändert das Steuerelement der Conditional Access-App kein Verhalten für die app.</span><span class="sxs-lookup"><span data-stu-id="d259e-p106">After it is deployed, you can't remove an app from the Conditional Access App Control page. As long as you don't set a session or access policy on the app, the Conditional Access App Control won't change any behavior for the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d259e-155">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d259e-155">Next steps</span></span>

- [<span data-ttu-id="d259e-156">Informationen zu Sitzungs Richtlinien in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d259e-156">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="d259e-157">Informationen zu Zugriffsrichtlinien in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d259e-157">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 

- [<span data-ttu-id="d259e-158">Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d259e-158">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)
---
title: Schützen von Apps mit der App-Steuerung für bedingten Zugriff in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Stop Verstöße und Lecks in Echtzeit mit Office 365 Cloud App Security Conditional Access app Control.
ms.openlocfilehash: 23c4b29e86eb8ba92cfa8a544d6484965ec6372b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217085"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a><span data-ttu-id="75f2a-103">Schützen von Apps mit der App-Steuerung für bedingten Zugriff in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="75f2a-103">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>

|<span data-ttu-id="75f2a-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75f2a-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="75f2a-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75f2a-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="75f2a-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="75f2a-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="75f2a-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="75f2a-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="75f2a-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="75f2a-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="75f2a-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="75f2a-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="75f2a-110">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="75f2a-110">You are here!</span></span>  <br/> [<span data-ttu-id="75f2a-111">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="75f2a-111">Next step</span></span>](ocas-deploy-conditional-access-app-control.md) <br/> |[<span data-ttu-id="75f2a-112">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="75f2a-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="75f2a-p101">Am heutigen Arbeitsplatz ist es oft nicht genug, nach der Tatsache zu wissen, was in ihrer Cloud-Umgebung passiert. Sie möchten Verstöße und Lecks in Echtzeit beenden, bevor Mitarbeiter absichtlich oder versehentlich Ihre Daten und Ihre Organisation gefährden. Es ist wichtig, Benutzern in Ihrer Organisation zu ermöglichen, die Dienste und Tools, die Ihnen in Cloud-Apps zur Verfügung stehen, optimal zu nutzen und ihre eigenen Geräte zum laufen zu bringen. Gleichzeitig benötigen Sie Tools, mit denen Sie Ihre Organisation vor Datenlecks und Datendiebstahl in Echtzeit schützen können. Zusammen mit Azure Active Directory bietet Office 365 Cloud App Security diese Funktionen in einer ganzheitlichen und integrierten Erfahrung mit Conditional Access app Control.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p101">In today’s workplace, it’s often not enough to know what’s happening in your cloud environment after the fact. You want to stop breaches and leaks in real time, before employees intentionally or inadvertently put your data and your organization at risk. It's important to enable users in your organization to make the most of the services and tools available to them in cloud apps, and let them bring their own devices to work. At the same time, you need tools to help protect your organization from data leaks, and data theft, in real time. Together with Azure Active Directory, Office 365 Cloud App Security delivers these capabilities in a holistic and integrated experience with Conditional Access App Control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75f2a-118">zur verwendung der cloud app security Conditional Access-app-steuerung benötigen sie eine [Azure active Directory P1-lizenz](https://azure.microsoft.com/pricing/details/active-directory/) und ein active [Office 365 cloud app security](office-365-cas-overview.md) -abonnement.</span><span class="sxs-lookup"><span data-stu-id="75f2a-118">To use Cloud App Security Conditional Access App Control, you need an [Azure Active Directory P1 license](https://azure.microsoft.com/pricing/details/active-directory/) and an active [Office 365 Cloud App Security](office-365-cas-overview.md) subscription.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="75f2a-119">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="75f2a-119">How it works</span></span>

<span data-ttu-id="75f2a-p102">Die APP-Steuerelement für die Conditional Access-Anwendung verwendet eine Reverse-Proxy-Architektur und ist in Azure AD Conditional Access integriert. Mit dem bedingten Zugriff von Azure AD können Sie Zugriffssteuerungen für die Apps ihrer Organisation basierend auf bestimmten Bedingungen erzwingen. Die Bedingungen definieren *, wer* (Benutzer oder Gruppe von Benutzern) und *was* (welche Cloud-Apps) und *wo* (an welchen Standorten und Netzwerken) eine Richtlinie für den bedingten Zugriff angewendet wird. Nachdem Sie die Bedingungen festgelegt haben, können Sie Benutzer an Office 365 Cloud App Security weiterleiten, in dem Sie Daten mit der APP-Steuerelement für die bedingte Zugriffssteuerung schützen können, indem Sie Zugriffs-und Sitzungs Steuerelemente anwenden.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p102">Conditional Access App Control uses a reverse proxy architecture and is uniquely integrated with Azure AD conditional access. Azure AD conditional access allows you to enforce access controls on your organization’s apps based on certain conditions. The conditions define *who* (user or group of users) and *what* (which cloud apps) and *where* (which locations and networks) a conditional access policy is applied to. After you’ve determined the conditions, you can route users to Office 365 Cloud App Security where you can protect data with Conditional Access App Control by applying access and session controls.</span></span>

<span data-ttu-id="75f2a-p103">Mit der APP-Steuerelement für die bedingte Zugriffssteuerung können Benutzer-App-Zugriff und-Sitzungen basierend auf Zugriffs-und Sitzungs Richtlinien in Echtzeit überwacht und gesteuert werden. Zugriffs-und Sitzungs Richtlinien werden innerhalb des Cloud-App-Sicherheits Portals verwendet, um Filter weiter zu verfeinern und Aktionen für einen Benutzer festzulegen. Mit den Zugriffs-und Sitzungs Richtlinien können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="75f2a-p103">Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies. Access and session policies are used within the Cloud App Security portal to further refine filters and set actions to be taken on a user. With the access and session policies, you can:</span></span>

- <span data-ttu-id="75f2a-p104">**Blockieren beim Herunterladen**: Sie können den Download vertraulicher Dokumente blockieren. Beispielsweise auf nicht verwalteten Geräten.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p104">**Block on download**: You can block the download of sensitive documents. For example, on unmanaged devices.</span></span>

- <span data-ttu-id="75f2a-p105">**Protect on Download**: anstatt den Download vertraulicher Dokumente zu blockieren, können Sie festlegen, dass Dokumente per Verschlüsselung beim Download geschützt werden müssen. Diese Verschlüsselung stellt sicher, dass das Dokument geschützt ist und der Benutzer Zugriff authentifiziert wird, wenn die Daten auf ein nicht vertrauenswürdiges Gerät heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p105">**Protect on download**: Instead of blocking the download of sensitive documents, you can require documents to be protected via encryption on download. This encryption makes sure the document is protected and user access is authenticated if the data is downloaded to an untrusted device.</span></span>

- <span data-ttu-id="75f2a-p106">**Überwachen von Benutzersitzungen mit niedriger Vertrauens**Ebene: riskante Benutzer werden überwachen, wenn Sie sich bei Apps anmelden und ihre Aktionen innerhalb der Sitzung protokolliert werden. Sie können das Benutzerverhalten untersuchen und analysieren, um zu verstehen, wo und unter welchen Bedingungen die Sitzungs Richtlinien zukünftig angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p106">**Monitor low-trust user sessions**: Risky users are monitored when they sign into apps and their actions are logged from within the session. You can investigate and analyze user behavior to understand where, and under what conditions, session policies should be applied in the future.</span></span>

- <span data-ttu-id="75f2a-133">**Zugriff blockieren**: Sie können den Zugriff auf bestimmte Apps für Benutzer, die von nicht verwalteten Geräten oder von nicht-Unternehmensnetzwerken kommen, vollständig blockieren.</span><span class="sxs-lookup"><span data-stu-id="75f2a-133">**Block access**: You can completely block access to specific apps for users coming from unmanaged devices or from non-corporate networks.</span></span>

- <span data-ttu-id="75f2a-134">**Schreibgeschützten Modus erstellen**: durch überwachen und blockieren benutzerdefinierter in-App-Aktivitäten können Sie einen schreibgeschützten Modus für bestimmte Apps für bestimmte Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="75f2a-134">**Create read-only mode**: By monitoring and blocking custom in-app activities, you can create a read-only mode to specific apps for specific users.</span></span>

- <span data-ttu-id="75f2a-p107">**Einschränken von Benutzersitzungen von nicht-Unternehmensnetzwerken**: Benutzer, die über einen Standort, der nicht Teil Ihres Unternehmensnetzwerks ist, auf eine geschützte App zugreifen, haben Zugriff auf eingeschränkte Berechtigungen. Der Download von vertraulichen Materialien wird blockiert oder geschützt.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p107">**Restrict user sessions from non-corporate networks**: Users accessing a protected app from a location that isn't part of your corporate network are allowed restricted access. The download of sensitive materials is blocked or protected.</span></span>

### <a name="how-session-control-works"></a><span data-ttu-id="75f2a-137">FunktionsWeise der Sitzungssteuerung</span><span class="sxs-lookup"><span data-stu-id="75f2a-137">How session control works</span></span>

<span data-ttu-id="75f2a-p108">Durch das Erstellen einer Sitzungsrichtlinie mit der APP-Steuerelement für den bedingten Zugriff können Sie Benutzersitzungen steuern, indem Sie den Benutzer über einen Reverseproxy statt direkt an die APP umleiten. Von nun an gehen Benutzeranfragen und-Antworten durch Office 365 Cloud App Security anstatt direkt an die app.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p108">Creating a session policy with Conditional Access App Control enables you to control user sessions by redirecting the user through a reverse proxy instead of directly to the app. From then on, user requests and responses go through Office 365 Cloud App Security rather than directly to the app.</span></span>

<span data-ttu-id="75f2a-p109">Um den Benutzer innerhalb der Sitzung beizubehalten, werden alle relevanten URLs, Java-Skripts und Cookies innerhalb der App-Sitzung durch Office 365 Cloud App Security-URLs ersetzt. Wenn die APP beispielsweise eine Seite mit Links zurückgibt, deren Domänen mit myapp.com enden, wird die Verknüpfung durch Domänen beendet, die mit ungefähr folgendem enden: myapp.com.us.cas.ms</span><span class="sxs-lookup"><span data-stu-id="75f2a-p109">To keep the user within the session, all the relevant URLs, Java scripts, and cookies within the app session are replaced with Office 365 Cloud App Security URLs. For example, if the app returns a page with links whose domains end with myapp.com, the link is replaced with domains ending with something like: myapp.com.us.cas.ms</span></span>

<span data-ttu-id="75f2a-p110">Bei dieser Methode müssen Sie nichts auf dem Gerät installieren. Diese Methode eignet sich ideal zum Überwachen von Sitzungen von nicht verwalteten Geräten.</span><span class="sxs-lookup"><span data-stu-id="75f2a-p110">This method doesn't require you to install anything on the device. This method is ideal when monitoring sessions from unmanaged devices.</span></span>

<span data-ttu-id="75f2a-144">Nachdem eine Sitzung durch Office 365 Cloud App Security geleitet wurde, können die folgenden Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="75f2a-144">After a session is directed through Office 365 Cloud App Security, the following actions can be done:</span></span>

1. <span data-ttu-id="75f2a-145">Überprüfen des Datenverkehrs für Benutzeraktivitäten</span><span class="sxs-lookup"><span data-stu-id="75f2a-145">Inspect the traffic for user activities</span></span>

2. <span data-ttu-id="75f2a-146">Anzeigen der identifizierten Aktivitäten im Sicherheits Aktivitätsprotokoll der Office 365 Cloud-App</span><span class="sxs-lookup"><span data-stu-id="75f2a-146">Display the identified activities in the Office 365 Cloud App Security Activity log</span></span>

3. <span data-ttu-id="75f2a-147">Speichern der Datenverkehrs Protokolle und analysieren</span><span class="sxs-lookup"><span data-stu-id="75f2a-147">Save the traffic logs and analyze them</span></span>

4. <span data-ttu-id="75f2a-148">Aktivieren des Administrators zum Exportieren der Datenverkehrs Protokolle</span><span class="sxs-lookup"><span data-stu-id="75f2a-148">Enable the admin to export the traffic logs</span></span>

5. <span data-ttu-id="75f2a-149">Erzwingen von Richtlinien für die Sitzung</span><span class="sxs-lookup"><span data-stu-id="75f2a-149">Enforce policies on the session</span></span>

## <a name="managed-device-identification"></a><span data-ttu-id="75f2a-150">Erkennung verwalteter Geräte</span><span class="sxs-lookup"><span data-stu-id="75f2a-150">Managed device identification</span></span>

<span data-ttu-id="75f2a-p111">Mit der APP-Steuerelement für die bedingte Zugriffssteuerung können Sie Richtlinien erstellen, die berücksichtigen, ob ein Gerät verwaltet wird. Um zu ermitteln, ob ein Gerät verwaltet wird, verwendet die Funktion Folgendes:</span><span class="sxs-lookup"><span data-stu-id="75f2a-p111">Conditional Access App Control enables you to create policies that take into account whether a device is managed or not. To identify whether a device is managed or not, the feature uses:</span></span>

- <span data-ttu-id="75f2a-153">Kompatible Geräte</span><span class="sxs-lookup"><span data-stu-id="75f2a-153">Compliant devices</span></span>

- <span data-ttu-id="75f2a-154">Domänen verbundene Geräte</span><span class="sxs-lookup"><span data-stu-id="75f2a-154">Domain-joined devices</span></span>

- <span data-ttu-id="75f2a-155">Bereitstellung von Client Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="75f2a-155">Client certificates deployment</span></span>

### <a name="compliant-and-domain-joined-devices"></a><span data-ttu-id="75f2a-156">Kompatible und Domänen verbundene Geräte</span><span class="sxs-lookup"><span data-stu-id="75f2a-156">Compliant and domain-joined devices</span></span>

<span data-ttu-id="75f2a-p112">Mit dem bedingten Zugriff von Azure AD können kompatible und Domänen verbundene Geräteinformationen direkt an Office 365 Cloud App Security übergeben werden. Von dort kann eine Zugriffsrichtlinie oder eine Sitzungsrichtlinie entwickelt werden, die den Gerätestatus als Filter verwendet. Weitere Informationen finden Sie in der [Einführung in die Geräteverwaltung in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="75f2a-p112">Azure AD conditional access enables compliant and domain-joined device information to be passed directly to Office 365 Cloud App Security. From there, an access policy or a session policy can be developed that uses device state as a filter. For more information, see the [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>

### <a name="client-certificate-authenticated-devices"></a><span data-ttu-id="75f2a-160">Authentifizierte Geräte mit Client Zertifikat</span><span class="sxs-lookup"><span data-stu-id="75f2a-160">Client-certificate authenticated devices</span></span>

<span data-ttu-id="75f2a-p113">Der Mechanismus zur Geräteidentifizierung kann die Authentifizierung von relevanten Geräten mithilfe von Clientzertifikaten anfordern. Sie können entweder vorhandene Clientzertifikate, die bereits in Ihrer Organisation bereitgestellt werden, oder neue Clientzertifikate auf verwalteten Geräten verwenden. Anschließend verwenden Sie das vorhanden sein dieser Zertifikate, um Zugriffs-und Sitzungs Richtlinien festzulegen. Informationen zur Bereitstellung von Clientzertifikaten finden Sie unter [Deploy Conditional Access app Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span><span class="sxs-lookup"><span data-stu-id="75f2a-p113">The device identification mechanism can request authentication from relevant devices using client certificates. You can either use existing client certificates already deployed in your organization or roll out new client certificates to managed devices. You then use the presence of those certificates to set access and session policies. For information on how to deploy client certificates see [Deploy Conditional Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span></span>

## <a name="supported-apps-and-clients"></a><span data-ttu-id="75f2a-165">Unterstützte apps und Clients</span><span class="sxs-lookup"><span data-stu-id="75f2a-165">Supported apps and clients</span></span>

<span data-ttu-id="75f2a-166">Die APP-Steuerelement für die bedingte Zugriffssteuerung für Office 365 unterstützt die folgenden vorgestellten Apps:</span><span class="sxs-lookup"><span data-stu-id="75f2a-166">Conditional Access App Control for Office 365 supports the following featured apps:</span></span>

- <span data-ttu-id="75f2a-167">Exchange Online (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-167">Exchange Online (preview)</span></span>

- <span data-ttu-id="75f2a-168">OneDrive for Business (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-168">OneDrive for Business (preview)</span></span>

- <span data-ttu-id="75f2a-169">Power BI (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-169">Power BI (preview)</span></span>

- <span data-ttu-id="75f2a-170">SharePoint Online (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-170">SharePoint Online (preview)</span></span>

- <span data-ttu-id="75f2a-171">Microsoft Teams (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-171">Microsoft Teams (preview)</span></span>

- <span data-ttu-id="75f2a-172">Jammern (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="75f2a-172">Yammer (preview)</span></span>

<span data-ttu-id="75f2a-173">Weitere apps werden kontinuierlich an die Sitzungssteuerung weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="75f2a-173">Additional apps are being continuously on-boarded to session control.</span></span>

## <a name="next-steps"></a><span data-ttu-id="75f2a-174">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="75f2a-174">Next steps</span></span>

- [<span data-ttu-id="75f2a-175">Bereitstellen der App-Steuerung für bedingten Zugriff für Office 365-Apps</span><span class="sxs-lookup"><span data-stu-id="75f2a-175">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

- [<span data-ttu-id="75f2a-176">Informationen zu Sitzungs Richtlinien in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="75f2a-176">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="75f2a-177">Informationen zu Zugriffsrichtlinien in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="75f2a-177">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 
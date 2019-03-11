---
title: Integrieren von Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Integrieren Sie Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection, um detailliertere Informationen zur Bedrohungs Verwaltung zu erhalten.
ms.openlocfilehash: bbbb42c9d0f37ab33323b2fa1dd071bd5ee16829
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2019
ms.locfileid: "30523979"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="a45f8-103">Integrieren von Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a45f8-103">Integrate Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="a45f8-104">Wenn Sie Teil des Sicherheitsteams Ihrer Organisation sind, können Sie Office 365 Advanced Threat Protection und zugehörige unter Such-und Antwortfunktionen mit Windows Defender Advanced Threat Protection integrieren.</span><span class="sxs-lookup"><span data-stu-id="a45f8-104">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and related investigation and response features with Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="a45f8-105">Auf diese Weise können Sie schnell erkennen, ob die Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a45f8-105">This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365.</span></span> <span data-ttu-id="a45f8-106">Sobald die Integration aktiviert ist, können Sie beispielsweise eine Liste der Computer anzeigen, die von den Empfängern einer erkannten e-Mail-Nachricht verwendet werden, sowie die Anzahl der letzten Benachrichtigungen, die diese Computer in Windows Defender Advanced Threat Protection haben.</span><span class="sxs-lookup"><span data-stu-id="a45f8-106">For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="a45f8-107">Die folgende Abbildung zeigt die Registerkarte **Geräte** , die angezeigt werden, wenn die Integration von Windows Defender Advanced Threat Protection aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="a45f8-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Wenn Windows Defender ATP aktiviert ist, können Sie eine Liste der Computer mit Warnungen anzeigen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="a45f8-109">In diesem Beispiel können Sie sehen, dass die Empfänger der e-Mail-Nachricht vier Geräte haben und einer eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="a45f8-109">In this example, you can see that the recipients of the email message have four devices and one has an alert.</span></span> <span data-ttu-id="a45f8-110">Wenn Sie auf den Link für ein Gerät klicken, wird die zugehörige Seite im Windows Defender Advanced Threat Protection-Portal geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a45f8-110">Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="a45f8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a45f8-111">Requirements</span></span>

- <span data-ttu-id="a45f8-112">Ihre Organisation muss über Office 365 Advanced Threat Protection Plan 2 (oder Office 365 E5) und Windows Defender ATP verfügen.</span><span class="sxs-lookup"><span data-stu-id="a45f8-112">Your organization must have Office 365 Advanced Threat Protection Plan 2 (or Office 365 E5) and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="a45f8-113">Sie müssen ein globaler Office 365-Administrator sein oder über eine Sicherheitsadministrator Rolle (wie Sicherheitsadministrator) im [ &amp; Security Compliance Center](https://protection.office.com)verfügen.</span><span class="sxs-lookup"><span data-stu-id="a45f8-113">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="a45f8-114">(Siehe [Berechtigungen im Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="a45f8-114">(See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="a45f8-115">Sie benötigen Zugriff auf sowohl Office 365 Threat Explorer im Security & Compliance Center als auch auf dem Windows Defender Advanced Threat Protection-Portal.</span><span class="sxs-lookup"><span data-stu-id="a45f8-115">You must have access to both Office 365 Threat Explorer in the Security & Compliance Center and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a><span data-ttu-id="a45f8-116">So integrieren Sie Office 365 Advanced Threat Protection in Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="a45f8-116">To integrate Office 365 Advanced Threat Protection with Windows Defender ATP</span></span>

<span data-ttu-id="a45f8-117">Die Integration von Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection wird mithilfe des Office 365 Security & Compliance Center und des Windows Defender Advanced Threat Protection-Portals eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a45f8-117">Integrating Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="a45f8-118">Wechseln Sie als globaler Office 365-Administrator oder als Sicherheitsadministrator zu [https://protection.office.com](https://protection.office.com) Ihrem Geschäfts-oder Schulkonto für Office 365, und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="a45f8-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="a45f8-119">Wählen Sie **Threat Management** \> **Explorer**aus.</span><span class="sxs-lookup"><span data-stu-id="a45f8-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="a45f8-120">![Explorer im Menü "Bedrohungs Verwaltung"](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="a45f8-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="a45f8-121">Wählen Sie in der oberen rechten Ecke des Bildschirms **WDATP Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a45f8-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="a45f8-122">Aktivieren Sie im Dialogfeld Windows Defender ATP-Verbindung die Verbindung mit Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="a45f8-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Windows Defender ATP-Verbindung](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="a45f8-124">Aktivieren Sie die Verbindung in Windows Defender Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="a45f8-124">Enable the connection in Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="a45f8-125">Weitere Informationen finden Sie unter [Verwenden des Windows Defender Advanced Threat Protection](https://go.microsoft.com/fwlink/?linkid=859690)-Portals.</span><span class="sxs-lookup"><span data-stu-id="a45f8-125">See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="a45f8-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a45f8-126">Related topics</span></span>

[<span data-ttu-id="a45f8-127">Office 365 Bedrohungs Ermittlung und-Antwort</span><span class="sxs-lookup"><span data-stu-id="a45f8-127">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)
  
[<span data-ttu-id="a45f8-128">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a45f8-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  


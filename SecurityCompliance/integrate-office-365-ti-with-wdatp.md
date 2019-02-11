---
title: Integrieren von Office 365 Threat Intelligence in Windows Defender Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Integrieren von Office 365 erweiterte Threat Protection in Windows Defender erweiterte Threat Protection ausführlichere Threat Management Informationen angezeigt.
ms.openlocfilehash: e5070e003972ae5308415dcdcca85b069d1163ac
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382538"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="a48e7-103">Integrieren von Office 365 Threat Intelligence in Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a48e7-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="a48e7-p101">Wenn Sie Teil Ihrer Organisation Security Team sind, können Sie Office 365 erweiterte Threat Protection und Bedrohungsanalyse Funktionen mit Windows Defender erweiterte Schutz integrieren. Dadurch können Sie schnell zu verstehen, wenn Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Beispielsweise nach Integration aktiviert ist, können Sie eine Liste mit Computern, die die Empfänger einer Nachricht gefundene e-Mail verwendet auch sehen, wie viele letzten die Computern in Windows Defender erweiterte Threat Protection haben.</span><span class="sxs-lookup"><span data-stu-id="a48e7-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="a48e7-107">Die folgende Abbildung zeigt der Registerkarte **Geräte** , sehen Sie, wenn Windows Defender erweiterte Threat Protection-Integration aktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="a48e7-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Wenn Windows Defender ATP aktiviert ist, sehen Sie eine Liste der Computer, auf denen Warnungen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="a48e7-p102">In diesem Beispiel sehen Sie sich, dass der Empfänger der e-Mail-Nachricht vier Geräte haben und eine Benachrichtigung hat. Durch Klicken auf den Link für ein Gerät wird eine Seite im Portal Windows Defender erweiterte Threat Protection geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a48e7-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="a48e7-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a48e7-111">Requirements</span></span>

- <span data-ttu-id="a48e7-112">Ihre Organisation muss Bedrohungsanalyse für Office 365 und Windows Defender ATP verfügen.</span><span class="sxs-lookup"><span data-stu-id="a48e7-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="a48e7-p103">Wenn Sie ein Office 365 globaler Administrator angemeldet sein oder eine Administrator Sicherheitsrolle (beispielsweise Sicherheitsadministrator) in die [Sicherheit &amp; Compliance Center](https://protection.office.com). (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="a48e7-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="a48e7-115">Sie benötigen Zugriff auf Office 365 Bedrohungsanalyse und das Windows Defender erweiterte Threat Protection-Portal.</span><span class="sxs-lookup"><span data-stu-id="a48e7-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="a48e7-116">Office 365 Bedrohungsanalyse mit Windows Defender ATP integriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a48e7-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="a48e7-117">Integrieren von Office 365 Bedrohungsanalyse in Windows Defender erweiterter Schutz eingerichtet ist sowohl die Sicherheit in Office 365 & Compliance Center und das Windows Defender erweiterte Threat Protection-Portal mit.</span><span class="sxs-lookup"><span data-stu-id="a48e7-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="a48e7-118">Als ein globaler Office 365-Administrator oder ein Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365.</span><span class="sxs-lookup"><span data-stu-id="a48e7-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="a48e7-119">Wählen Sie **Threat Management** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="a48e7-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="a48e7-120">![Explorer im Menü Threat Management](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="a48e7-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="a48e7-121">Wählen Sie in der oberen rechten Ecke des Bildschirms **WDATP-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a48e7-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="a48e7-122">Aktivieren Sie im Dialogfeld Windows Defender ATP Verbindung mit Windows ATP verbinden.</span><span class="sxs-lookup"><span data-stu-id="a48e7-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Windows Defender ATP-Verbindung](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="a48e7-p104">Aktivieren Sie die Verbindung in Windows Defender erweiterte Threat Protection. Finden Sie unter [Verwenden der Windows Defender erweiterte Threat Protection-Portal](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="a48e7-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="a48e7-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a48e7-126">Related topics</span></span>

[<span data-ttu-id="a48e7-127">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="a48e7-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="a48e7-128">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a48e7-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  


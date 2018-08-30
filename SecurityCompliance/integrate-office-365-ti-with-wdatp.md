---
title: Integrieren von Office 365 Bedrohungsanalyse in Windows Defender erweiterte Schutz
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Integrieren von Office 365 erweiterte Threat Protection in Windows Defender erweiterte Threat Protection ausführlichere Threat Management Informationen angezeigt.
ms.openlocfilehash: 574594d5881853b268713e0bb74444ae80ffcf46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529160"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="471a9-103">Integrieren von Office 365 Bedrohungsanalyse in Windows Defender erweiterte Schutz</span><span class="sxs-lookup"><span data-stu-id="471a9-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="471a9-p101">Wenn Sie in Ihrer Organisation Security Team sind, können Sie Office 365 mit Windows Defender erweiterte Threat Protection (ATP) integrieren. Dadurch können Sie schnell zu verstehen, wenn Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Beispielsweise nach Integration aktiviert ist, können Sie eine Liste mit Computern, die die Empfänger einer Nachricht gefundene e-Mail verwendet auch sehen, wie viele letzten die Computern in Windows Defender ATP haben.</span><span class="sxs-lookup"><span data-stu-id="471a9-p101">If you are part of your organization's security team, you can integrate Office 365 with Windows Defender Advanced Threat Protection (ATP). This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender ATP.</span></span>
  
<span data-ttu-id="471a9-107">Die folgende Abbildung zeigt der Registerkarte **Geräte** , sehen Sie, wenn Windows Defender ATP-Integration aktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="471a9-107">The following image shows the **Devices** tab that you'll see when have Windows Defender ATP integration enabled:</span></span> 
  
![Wenn Windows Defender ATP aktiviert ist, sehen Sie eine Liste der Computer, auf denen Warnungen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="471a9-p102">In diesem Beispiel sehen Sie sich, dass der Empfänger der e-Mail-Nachricht vier Computern haben und eine Benachrichtigung in Windows Defender ATP hat. Auf den Link zu einem Computer wird die Computer Seite in Windows Defender ATP in einer neuen Registerkarte geöffnet.</span><span class="sxs-lookup"><span data-stu-id="471a9-p102">In this example, you can see that the recipients of the email message have four machines and one has an alert in Windows Defender ATP. Clicking the link to a machine opens the machine page in Windows Defender ATP in a new tab.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="471a9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="471a9-111">Requirements</span></span>

- <span data-ttu-id="471a9-112">Ihre Organisation muss Bedrohungsanalyse für Office 365 und Windows Defender ATP verfügen.</span><span class="sxs-lookup"><span data-stu-id="471a9-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="471a9-p103">Wenn Sie ein Office 365 globaler Administrator angemeldet sein oder eine Administrator Sicherheitsrolle in das Wertpapier &amp; Compliance Center. (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="471a9-p103">You must be an Office 365 global administrator or have a security administrator role assigned in the Security &amp; Compliance Center. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="471a9-115">Sie benötigen Zugriff auf Office 365 Bedrohungsanalyse und das Windows Defender ATP-Portal.</span><span class="sxs-lookup"><span data-stu-id="471a9-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender ATP portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="471a9-116">Office 365 Bedrohungsanalyse mit Windows Defender ATP integriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="471a9-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="471a9-117">Integrieren von Office 365 Bedrohungsanalyse in Windows Defender ATP ist sowohl in Office 365 und im Windows Defender ATP-Portal eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="471a9-117">Integrating Office 365 Threat Intelligence with Windows Defender ATP is set up both in Office 365 and in the Windows Defender ATP portal.</span></span>
  
1. <span data-ttu-id="471a9-118">Als ein globaler Office 365 oder ein Sicherheitsadministrator, wechseln Sie zur [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365.</span><span class="sxs-lookup"><span data-stu-id="471a9-118">As an Office 365 global or a security administrator, go to [https://portal.office.com](https://portal.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="471a9-119">Wählen Sie **Threat Management** \> **Bedrohung Explorer**.</span><span class="sxs-lookup"><span data-stu-id="471a9-119">Choose **Threat management** \> **Threat explorer**.</span></span>
    
3. <span data-ttu-id="471a9-120">Wählen Sie im Menü **Weitere** **WDATP Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="471a9-120">On the **More** menu, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="471a9-121">Wählen Sie **eine Verbindung mit Windows ATP**aus.</span><span class="sxs-lookup"><span data-stu-id="471a9-121">Select **Connect to Windows ATP**.</span></span>
    
<span data-ttu-id="471a9-p104">Nachdem Sie die Einstellungen in Office 365 geändert haben, müssen Sie die Verbindung von Windows Defender ATP aktivieren. Klicken Sie dazu finden Sie unter [Verwendung der Windows Defender erweiterte Threat Protection-Portal](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="471a9-p104">After you have changed the settings in Office 365, you must enable the connection from Windows Defender ATP. To do that, see [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="471a9-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="471a9-124">Related topics</span></span>

[<span data-ttu-id="471a9-125">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="471a9-125">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="471a9-126">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="471a9-126">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  


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
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a>Integrieren von Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection

Wenn Sie Teil des Sicherheitsteams Ihrer Organisation sind, können Sie Office 365 Advanced Threat Protection und zugehörige unter Such-und Antwortfunktionen mit Windows Defender Advanced Threat Protection integrieren. Auf diese Weise können Sie schnell erkennen, ob die Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Sobald die Integration aktiviert ist, können Sie beispielsweise eine Liste der Computer anzeigen, die von den Empfängern einer erkannten e-Mail-Nachricht verwendet werden, sowie die Anzahl der letzten Benachrichtigungen, die diese Computer in Windows Defender Advanced Threat Protection haben.
  
Die folgende Abbildung zeigt die Registerkarte **Geräte** , die angezeigt werden, wenn die Integration von Windows Defender Advanced Threat Protection aktiviert ist: 
  
![Wenn Windows Defender ATP aktiviert ist, können Sie eine Liste der Computer mit Warnungen anzeigen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
In diesem Beispiel können Sie sehen, dass die Empfänger der e-Mail-Nachricht vier Geräte haben und einer eine Warnung. Wenn Sie auf den Link für ein Gerät klicken, wird die zugehörige Seite im Windows Defender Advanced Threat Protection-Portal geöffnet.
  
## <a name="requirements"></a>Anforderungen

- Ihre Organisation muss über Office 365 Advanced Threat Protection Plan 2 (oder Office 365 E5) und Windows Defender ATP verfügen.
    
- Sie müssen ein globaler Office 365-Administrator sein oder über eine Sicherheitsadministrator Rolle (wie Sicherheitsadministrator) im [ &amp; Security Compliance Center](https://protection.office.com)verfügen. (Siehe [Berechtigungen im Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md))
    
- Sie benötigen Zugriff auf sowohl Office 365 Threat Explorer im Security & Compliance Center als auch auf dem Windows Defender Advanced Threat Protection-Portal.
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a>So integrieren Sie Office 365 Advanced Threat Protection in Windows Defender ATP

Die Integration von Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection wird mithilfe des Office 365 Security & Compliance Center und des Windows Defender Advanced Threat Protection-Portals eingerichtet.
  
1. Wechseln Sie als globaler Office 365-Administrator oder als Sicherheitsadministrator zu [https://protection.office.com](https://protection.office.com) Ihrem Geschäfts-oder Schulkonto für Office 365, und melden Sie sich an. 
    
2. Wählen Sie **Threat Management** \> **Explorer**aus.<br>![Explorer im Menü "Bedrohungs Verwaltung"](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. Wählen Sie in der oberen rechten Ecke des Bildschirms **WDATP Einstellungen**.
    
4. Aktivieren Sie im Dialogfeld Windows Defender ATP-Verbindung die Verbindung mit Windows ATP.<br>![Windows Defender ATP-Verbindung](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Aktivieren Sie die Verbindung in Windows Defender Advanced Threat Protection. Weitere Informationen finden Sie unter [Verwenden des Windows Defender Advanced Threat Protection](https://go.microsoft.com/fwlink/?linkid=859690)-Portals.

  
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Bedrohungs Ermittlung und-Antwort](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  


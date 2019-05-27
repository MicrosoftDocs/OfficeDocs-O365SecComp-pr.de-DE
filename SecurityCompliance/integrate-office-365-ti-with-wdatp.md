---
title: Integration Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Integrieren Sie Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection, um detaillierte Informationen zur Bedrohungs Verwaltung zu erhalten.
ms.openlocfilehash: 8fbbc8beeeba6cfee0e87ee44f99819094d5569e
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408270"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a>Integration Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection

Wenn Sie Teil des Sicherheitsteams Ihrer Organisation sind, können Sie Office 365 Advanced Threat Protection und zugehörige Ermittlungs-und Antwortfunktionen mit erweitertem Bedrohungsschutz von Windows Defender integrieren. Dies kann Ihnen helfen, schnell zu verstehen, ob die Computer der Benutzer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Wenn die Integration beispielsweise aktiviert ist, können Sie eine Liste der Computer anzeigen, die von den Empfängern einer erkannten e-Mail-Nachricht verwendet werden, sowie die Anzahl der letzten Warnungen, die diese Computer in Advanced Threat Protection von Windows Defender haben.
  
Die folgende Abbildung zeigt die Registerkarte **Geräte** , die angezeigt wird, wenn die Integration von Windows Defender Advanced Threat Protection aktiviert ist: 
  
![Wenn Windows Defender ATP aktiviert ist, können Sie eine Liste der Computer mit Warnungen anzeigen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
In diesem Beispiel können Sie sehen, dass die Empfänger der e-Mail-Nachricht vier Geräte und eine Warnung besitzen. Durch Klicken auf den Link für ein Gerät wird die Seite im Windows Defender Advanced Threat Protection-Portal geöffnet.
  
## <a name="requirements"></a>Voraussetzungen

- Ihre Organisation muss Office 365 Advanced Threat Protection Plan 2 (oder Office 365 E5) und Windows Defender ATP haben.
    
- Sie müssen ein Office 365 globaler Administrator sein oder über eine Sicherheitsadministrator Rolle (beispielsweise Sicherheitsadministrator) verfügen, die [im &amp; Security Compliance Center](https://protection.office.com)zugewiesen ist. (Siehe [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))
    
- Sie benötigen Zugriff auf beide [Explorer-(oder Echt Zeit Erkennungen)](threat-explorer.md) im Security & Compliance Center und im Windows Defender Advanced Threat Protection-Portal.
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a>So integrieren Sie Office 365 Advanced Threat Protection mit Windows Defender ATP

Integration Office 365 Advanced Threat Protection mit Windows Defender Advanced Threat Protection wird mithilfe des Security & Compliance Centers und des Windows Defender Advanced Threat Protection-Portals eingerichtet.
  
1. Wechseln Sie als globaler Office 365 Administrator oder Sicherheitsadministrator zu [https://protection.office.com](https://protection.office.com) ihrem geschäftlichen oder Schulkonto, und melden Sie sich für Office 365 an. 
    
2. Wählen Sie **Threat Management** \> **Explorer**aus.<br>![Explorer im Menü "Threat Management"](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. Wählen Sie in der oberen rechten Ecke des Bildschirms **Einstellungen für WDATP**aus.
    
4. Aktivieren Sie im Dialogfeld Windows Defender ATP Connection die Option Connect to Windows ATP.<br>![Windows Defender ATP-Verbindung](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Aktivieren Sie die Verbindung in Windows Defender Advanced Threat Protection. Siehe [Verwenden des Advanced Threat Protection-Portals von Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Verwandte Themen

[Untersuchung und Reaktion der Office 365 Bedrohung](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  


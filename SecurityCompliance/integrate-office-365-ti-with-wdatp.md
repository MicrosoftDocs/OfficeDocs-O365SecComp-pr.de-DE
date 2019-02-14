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
ms.collection: M365-security-compliance
description: Integrieren von Office 365 erweiterte Threat Protection in Windows Defender erweiterte Threat Protection ausführlichere Threat Management Informationen angezeigt.
ms.openlocfilehash: f8f5f50af10fb668aa67b68604e95e8dd19c9e69
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995206"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Integrieren von Office 365 Threat Intelligence in Windows Defender Advanced Threat Protection

Wenn Sie Teil Ihrer Organisation Security Team sind, können Sie Office 365 erweiterte Threat Protection und Bedrohungsanalyse Funktionen mit Windows Defender erweiterte Schutz integrieren. Dadurch können Sie schnell zu verstehen, wenn Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Beispielsweise nach Integration aktiviert ist, können Sie eine Liste mit Computern, die die Empfänger einer Nachricht gefundene e-Mail verwendet auch sehen, wie viele letzten die Computern in Windows Defender erweiterte Threat Protection haben.
  
Die folgende Abbildung zeigt der Registerkarte **Geräte** , sehen Sie, wenn Windows Defender erweiterte Threat Protection-Integration aktiviert haben: 
  
![Wenn Windows Defender ATP aktiviert ist, sehen Sie eine Liste der Computer, auf denen Warnungen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
In diesem Beispiel sehen Sie sich, dass der Empfänger der e-Mail-Nachricht vier Geräte haben und eine Benachrichtigung hat. Durch Klicken auf den Link für ein Gerät wird eine Seite im Portal Windows Defender erweiterte Threat Protection geöffnet.
  
## <a name="requirements"></a>Anforderungen

- Ihre Organisation muss Bedrohungsanalyse für Office 365 und Windows Defender ATP verfügen.
    
- Wenn Sie ein Office 365 globaler Administrator angemeldet sein oder eine Administrator Sicherheitsrolle (beispielsweise Sicherheitsadministrator) in die [Sicherheit &amp; Compliance Center](https://protection.office.com). (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))
    
- Sie benötigen Zugriff auf Office 365 Bedrohungsanalyse und das Windows Defender erweiterte Threat Protection-Portal.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Office 365 Bedrohungsanalyse mit Windows Defender ATP integriert werden soll.

Integrieren von Office 365 Bedrohungsanalyse in Windows Defender erweiterter Schutz eingerichtet ist sowohl die Sicherheit in Office 365 & Compliance Center und das Windows Defender erweiterte Threat Protection-Portal mit.
  
1. Als ein globaler Office 365-Administrator oder ein Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365. 
    
2. Wählen Sie **Threat Management** \> **Explorer**.<br>![Explorer im Menü Threat Management](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. Wählen Sie in der oberen rechten Ecke des Bildschirms **WDATP-Einstellungen**.
    
4. Aktivieren Sie im Dialogfeld Windows Defender ATP Verbindung mit Windows ATP verbinden.<br>![Windows Defender ATP-Verbindung](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Aktivieren Sie die Verbindung in Windows Defender erweiterte Threat Protection. Finden Sie unter [Verwenden der Windows Defender erweiterte Threat Protection-Portal](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  


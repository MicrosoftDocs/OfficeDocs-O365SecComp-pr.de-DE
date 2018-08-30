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
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Integrieren von Office 365 Bedrohungsanalyse in Windows Defender erweiterte Schutz

Wenn Sie in Ihrer Organisation Security Team sind, können Sie Office 365 mit Windows Defender erweiterte Threat Protection (ATP) integrieren. Dadurch können Sie schnell zu verstehen, wenn Benutzer Computer gefährdet sind, wenn Sie Bedrohungen in Office 365 untersuchen. Beispielsweise nach Integration aktiviert ist, können Sie eine Liste mit Computern, die die Empfänger einer Nachricht gefundene e-Mail verwendet auch sehen, wie viele letzten die Computern in Windows Defender ATP haben.
  
Die folgende Abbildung zeigt der Registerkarte **Geräte** , sehen Sie, wenn Windows Defender ATP-Integration aktiviert haben: 
  
![Wenn Windows Defender ATP aktiviert ist, sehen Sie eine Liste der Computer, auf denen Warnungen.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
In diesem Beispiel sehen Sie sich, dass der Empfänger der e-Mail-Nachricht vier Computern haben und eine Benachrichtigung in Windows Defender ATP hat. Auf den Link zu einem Computer wird die Computer Seite in Windows Defender ATP in einer neuen Registerkarte geöffnet.
  
## <a name="requirements"></a>Anforderungen

- Ihre Organisation muss Bedrohungsanalyse für Office 365 und Windows Defender ATP verfügen.
    
- Wenn Sie ein Office 365 globaler Administrator angemeldet sein oder eine Administrator Sicherheitsrolle in das Wertpapier &amp; Compliance Center. (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))
    
- Sie benötigen Zugriff auf Office 365 Bedrohungsanalyse und das Windows Defender ATP-Portal.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Office 365 Bedrohungsanalyse mit Windows Defender ATP integriert werden soll.

Integrieren von Office 365 Bedrohungsanalyse in Windows Defender ATP ist sowohl in Office 365 und im Windows Defender ATP-Portal eingerichtet.
  
1. Als ein globaler Office 365 oder ein Sicherheitsadministrator, wechseln Sie zur [https://portal.office.com](https://portal.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule für Office 365. 
    
2. Wählen Sie **Threat Management** \> **Bedrohung Explorer**.
    
3. Wählen Sie im Menü **Weitere** **WDATP Einstellungen**aus.
    
4. Wählen Sie **eine Verbindung mit Windows ATP**aus.
    
Nachdem Sie die Einstellungen in Office 365 geändert haben, müssen Sie die Verbindung von Windows Defender ATP aktivieren. Klicken Sie dazu finden Sie unter [Verwendung der Windows Defender erweiterte Threat Protection-Portal](https://go.microsoft.com/fwlink/?linkid=859690).
  
## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  


---
title: Einrichten von Benutzern und Fällen in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Erfahren Sie, wie Sie Benutzerrollen konfigurieren, Fälle erstellen und Benutzer zu Fällen in Office 365 Advanced eDiscovery zuweisen.  '
ms.openlocfilehash: 5a22e0683e49ebdaf8391e092aeb101386e0636b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260703"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a>Einrichten von Benutzern und Fällen in Office 365 Advanced eDiscovery

In diesem Thema wird beschrieben, wie Sie Benutzer und Fälle für Office 365 Advanced eDiscovery einrichten.
  
> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie Fälle und Benutzer in Advanced eDiscovery einrichten, ist Folgendes erforderlich:
  
- Um die Daten eines Benutzers mithilfe von Advanced eDiscovery zu analysieren, muss dem Benutzer (der Depotbank der Daten) eine Office 365 E5-Lizenz zugewiesen werden. Alternativ können Benutzern mit einer Office 365 E1-oder E3-Lizenz eine erweiterte eDiscovery-Standalone-Lizenz zugewiesen werden. Administratoren und Compliance Officer, denen Fälle zugeordnet sind und die erweiterte eDiscovery zur Analyse von Daten verwenden, benötigen keine E5-Lizenz. 
    
- Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Office 365 Security &amp; Compliance Center sein, um einen eDiscovery-Fall zu erstellen und ihm Mitglieder hinzuzufügen. Um sich selbst der eDiscovery-Manager-Rollengruppe im &amp; Security Compliance Center hinzuzufügen, müssen Sie ein globaler Administrator in ihrer Office 365-Organisation sein. Wenn Sie kein globaler Administrator sind, müssen Sie einen globalen Administrator bitten, Sie der Rollengruppe "eDiscovery-Manager" hinzuzufügen. Weitere Informationen finden Sie unter:
    
  - [Berechtigungen im Microsoft 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
    
  - [Zuweisen von eDiscovery-Berechtigungen im Microsoft 365 &amp; Security Compliance Center](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen für Benutzer

Der erste Schritt besteht darin, Benutzern die Anforderungs Berechtigungen im Security &amp; Compliance Center zuzuweisen, damit Sie als Mitglied eines eDiscovery-Falls hinzugefügt werden können. Nachdem ein Benutzer als Mitglied eines Falls im Security &amp; Compliance Center hinzugefügt wurde, kann er in Advanced eDiscovery auf den Fall zugreifen.
  
Wenn Sie einem Benutzer die erforderlichen Berechtigungen zuweisen möchten, damit er als Mitglied eines eDiscovery-Falls hinzugefügt werden kann, lesen Sie Schritt 1 in [eDiscovery- &amp; fällen im Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a>Schritt 2: Erstellen eines eDiscovery-Falls und Hinzufügen von Mitgliedern

Im nächsten Schritt erstellen Sie einen neuen eDiscovery-Fall im Security &amp; Compliance Center und fügen Mitglieder hinzu. Die Mitglieder des Falles können dann in Advanced eDiscovery auf den Fall zugreifen.
  
1. Informationen zum Erstellen eines neuen eDiscovery-Falls finden Sie unter Schritt 2 in [eDiscovery-Fällen im &amp; Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).
    
2. Informationen zum Hinzufügen von Mitgliedern zu einem eDiscovery-Fall finden Sie unter Schritt 3 in [eDiscovery- &amp; fällen im Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case) .
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a>Schritt 3: gehen Sie zu einem Fall in Advanced eDiscovery

Nachdem Sie einen eDiscovery-Fall erstellt und Mitglieder hinzugefügt haben, können Sie (oder ein beliebiger Member) in Advanced eDiscovery auf den entsprechenden Fall zugreifen. Informationen zum Zugriff auf einen Fall in Advanced eDiscovery finden Sie in Schritt 8 in [eDiscovery-Fällen im &amp; Microsoft 365 Security Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Vorbereiten der Daten](prepare-data-for-advanced-ediscovery.md)
 